---
title: Bæta við gagnareitum í samþættingu skatts með því að nota viðbætur
description: Þetta efnisatriði útskýrir hvernig á að nota X++ viðbætur til að bæta við gagnareitum í skattasamþættingu.
author: qire
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a3da8e1b8176eb25fe4e0a320aa3e907c06e09c5
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021393"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a>Bæta við gagnareitum í samþættingu skatts með því að nota viðbót

[!include [banner](../includes/banner.md)]


Þetta efnisatriði útskýrir hvernig á að nota X++ viðbætur til að bæta við gagnareitum í skattasamþættingu. Hægt er að stækka þessa reiti í skattgagnalíkan skattþjónustunnar og nota þá til að ákveða skattkóða. Frekari upplýsingar eru í [Bæta við gagnareitum í skattaskilgreiningum](tax-service-add-data-fields-tax-configurations.md).

## <a name="data-model"></a>Gagnalíkan

Gögnin í gagnalíkaninu eru flutt af hlutum og innleidd af klösum.

Hér er listi yfir stærstu hlutina:

* AxClass/TaxIntegration **Document** Object
* AxClass/TaxIntegration **Line** Object
* AxClass/TaxIntegration **TaxLine** Object

Eftirfarandi mynd sýnir hvernig þessir hlutir tengjast.

[![Vensl gagnalíkanshluta](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)

**Skjalahlutur** getur innihaldið marga **Línuhluti**. Hver hlutur inniheldur lýsigögn fyrir skattþjónustu.

- `TaxIntegrationDocumentObject` er með `originAddress` lýsigögn sem innihalda upplýsingar um upprunaaðsetur og `includingTax` lýsigögn sem gefa til kynna hvort línuupphæðin innihaldi söluskatt.
- `TaxIntegrationLineObject` er með `itemId`, `quantity`, og `categoryId` lýsigögn.

> [!NOTE]
> `TaxIntegrationLineObject` innleiðir einnig **Gjaldahluti**.

## <a name="integration-flow"></a>Samþættingarferli

Gögnum í flæðinu er stjórnað með aðgerðum.

### <a name="key-activities"></a>Helstu aðgerðir

* AxClass/TaxIntegration **Calculation** ActivityOnDocument
* AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument
* AxClass/TaxIntegration **DataPersistence** ActivityOnDocument
* AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument
* AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument

Aðgerðir eru keyrðar í eftirfarandi röð:

1. Stilling endurheimtar
2. Endurheimt gagna
3. Útreikningsþjónusta
4. Gjaldmiðlar
5. Varanleiki gagna

Til dæmis þarf að stækka **Endurheimt gagna** á undan **Útreikningsþjónustu**.

#### <a name="data-retrieval-activities"></a>Aðgerðir gagnaendurheimtar

Aðgerðir **Gagnaendurheimtar** sækir gögn úr gagnagrunni. Gagnabreytar fyrir mismunandi færslur eru í boði til að sækja gögn úr mismunandi færslutöflum:

- AxClass/TaxIntegration **PurchTable** DataRetrieval
- AxClass/TaxIntegration **PurchParmTable** DataRetrieval
- AxClass/TaxIntegration **PurchREQTable** DataRetrieval
- AxClass/TaxIntegration **PurchRFQTable** DataRetrieval
- AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval
- AxClass/TaxIntegration **SalesTable** DataRetrieval
- AxClass/TaxIntegration **SalesParm** DataRetrieval

Í þessum aðgerðum **Gagnaendurheimtar** eru gögn afrituð úr gagnagrunninum í `TaxIntegrationDocumentObject` og `TaxIntegrationLineObject`. Þar sem allar þessar aðgerðir stækka sama abstrakt sniðmátsklasann, notast þær við sömu aðferðirnar.

#### <a name="calculation-service-activities"></a>Aðgerðir útreikningsþjónustu

Aðgerðin **Útreikningsþjónusta** er tengillinn milli skattþjónustunnar og skattsamþættingarinnar. Þessi aðgerð ber ábyrgð á eftirfarandi virkni:

1. Setjið saman beiðnina.
2. Birta beiðnina til skattþjónustu.
3. Fá svar frá skattsþjónustunni.
4. Þátta svarið.

Gagnareitur sem bætt er við beiðnina verður bókaður saman með öðrum lýsigögnum. 

## <a name="extension-implementation"></a>Innleiðing viðbótar

Í þessum hluta eru ítarlegar leiðbeiningar sem útskýra hvernig á að innleiða viðbótina. Hann notar fjárhagsvíddirnar **Kostnaðarstaður** og **Verk** sem dæmi.

### <a name="step-1-add-the-data-variable-in-the-object-class"></a>1. Bætið gagnabreytunni við hlutaklasann

Hlutaklasinn inniheldur gagnabreytuna og sótt/sett aðferðir fyrir gögnin. Bætið gagnareitunum við annaðhvort `TaxIntegrationDocumentObject` eða `TaxIntegrationLineObject` eftir því hvert stig reitsins er. Eftirfarandi dæmi notar línustigið og skráarheitið er `TaxIntegrationLineObject_Extension.xpp`.

> [!NOTE]
> Ef gagnareiturinn sem verið er að bæta við er á stigi skjals skal breyta skráarheitinu í `TaxIntegrationDocumentObject_Extension.xpp`.

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

**Kostnaðarstað** og **Verki** er bætt við sem einkabreytum. Búið til sótt og sett aðferðir fyrir þessa gagnareiti til að vinna með gögnin.

### <a name="step-2-retrieve-data-from-the-database"></a>2. Sækja gögn úr gagnagrunni

Tilgreinið færsluna og stækkið viðeigandi breytiklasa til að sækja gögnin. Ef **Innkaupapöntunar** færsla er t.d. notuð þarf að stækka `TaxIntegrationPurchTableDataRetrieval` og `TaxIntegrationVendInvoiceInfoTableDataRetrieval`. 

> [!NOTE]
> `TaxIntegrationPurchParmTableDataRetrieval` erfist frá `TaxIntegrationPurchTableDataRetrieval`. Ekki ætti að breyta henni nema regla í töflunum `purchTable` og `purchParmTable` er mismunandi.

Ef bæta á við gagnareit fyrir allar færslur skal stækka alla `DataRetrieval` klasa.

Þar sem allar aðgerðir **Gagnaendurheimtar** stækka sama sniðmátsklasann, eru klasaskipulag, breytur og aðferðir svipaðar.

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

Eftirfarandi dæmi sýnir grunnskipulagið þegar `PurchTable` taflan er notuð.

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

Þegar kallað er á `CopyToDocument` aðferðina er `this.purchTable` biðminnið þegar til staðar. Tilgangur þessarar aðferðar er að afrita öll áskilin gögn úr `this.purchTable` í `document` hlutinn með því að nota sett-aðferðina sem var búin til í `DocumentObject`-klasanum.

Á sama hátt er `this.purchLine` biðminni þegar til staðar í `CopyToLine` aðferðinni. Tilgangur þessarar aðferðar er að afrita öll áskilin gögn úr `this.purchLine` í `_line` hlutinn með því að nota sett-aðferðina sem var búin til í `LineObject`-klasanum.

Einfaldasta nálgunin er að stækka aðferðirnar `CopyToDocument` og `CopyToLine`. Hins vegar mælum við með því að reyna að nota `copyToDocumentFromHeaderTable` og `copyToLineFromLineTable` aðferðirnar fyrst. Ef þær virka ekki sem skyldi skal innleiða eigin aðferð og kalla á hana í `CopyToDocument` og `CopyToLine`. Þrjár algengar aðstæður eru til staðar þar sem þessi nálgun gæti verið notuð:

- Áskilinn reitur er í `PurchTable` eða `PurchLine`. Í þessum aðstæðum er hægt að víkka `copyToDocumentFromHeaderTable` og `copyToLineFromLineTable`. Hér er dæmakóði.

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- Áskilin gögn eru ekki í sjálfgefinni töflu færslunnar. Hins vegar eru nokkur vensl töflutenginga við sjálfgefnu töfluna og reiturinn er áskilinn í flestum línum. Í þessum aðstæðum skal skipta út `getDocumentQueryObject` eða `getLineObject` til að senda fyrirspurn á töfluna eftir venslum tengingar. Í eftirfarandi dæmi er reiturinn **Afhenda nú** samþættur við sölupöntunina á línustiginu.

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    Í þessu dæmi er `mcrSalesLineDropShipment` biðminni gefið upp og fyrirspurnin er skilgreind í `getLineQueryObject`. Fyrirspurnin notar venslin `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`. Meðan verið er að stækka í þessum aðstæðum er hægt að skipta út `getLineQueryObject` fyrir eiginn samansettan fyrirspurnarhlut. Athugið hins vegar eftirfarandi atriði:

    * Vegna þess að skilagildi `getLineQueryObject` aðferðarinnar er `SysDaQueryObject` þarf að setja saman þennan hlut með því að nota SysDa nálgun.
    * Ekki er hægt að fjarlægja fyrirliggjandi töflu.

- Nauðsynleg gögn tengjast flutningstöflunni með flóknum venslum töflutengingar eða venslin eru ekki ein á móti einu (1:1) heldur ein á móti mörgum (1:N). Í þessum aðstæðum flækjast málin aðeins. Þessar aðstæður eiga við um dæmið um fjárhagsvíddir. 

    Í þessum aðstæðum er hægt að innleiða eigin aðferð til að sækja gögnin. Hér er dæmakóðinn í `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` skránni.

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a>Skref 3. Bæta gögnum við beiðnina

Framlengið `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` eða `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` aðferðina til að bæta gögnum við beiðnina. Hér er dæmakóðinn í `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` skránni.

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```

Í þessum kóða er `_destination` pökkunarhluturinn sem er notaður til að búa til bókunarbeiðnina og `_source` er `TaxIntegrationLineObject` hluturinn. 

> [!NOTE]
> * Skilgreinið lykilinn sem er notaður í skjámynd beiðninnar sem `private const str`.
> * Stillið reitinn í `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` aðferðinni með því að nota `SetField` aðferðina. Gagnagerð seinni færibreytunnar á að vera `string`. Ef gagnagerðin er ekki `string` skal umbreyta henni í `string`.

## <a name="appendix"></a>Viðauki

Þessi viðauki sýnir ítarlegan sýnishornakóða fyrir samþættingu fjárhagsvídda (**Kostnaðarstaður** og **Verk**) á línustiginu.

### <a name="taxintegrationlineobject_extensionxpp"></a>TaxIntegrationLineObject_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a>TaxIntegrationPurchTableDataRetrieval_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a>TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```
