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
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a><span data-ttu-id="cc1d9-103">Bæta við gagnareitum í samþættingu skatts með því að nota viðbót</span><span class="sxs-lookup"><span data-stu-id="cc1d9-103">Add data fields in the tax integration by using extension</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="cc1d9-104">Þetta efnisatriði útskýrir hvernig á að nota X++ viðbætur til að bæta við gagnareitum í skattasamþættingu.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-104">This topic explains how to use X++ extensions to add data fields in the tax integration.</span></span> <span data-ttu-id="cc1d9-105">Hægt er að stækka þessa reiti í skattgagnalíkan skattþjónustunnar og nota þá til að ákveða skattkóða.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-105">These fields can be extended to the tax data model of the tax service and used to determine tax codes.</span></span> <span data-ttu-id="cc1d9-106">Frekari upplýsingar eru í [Bæta við gagnareitum í skattaskilgreiningum](tax-service-add-data-fields-tax-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="cc1d9-106">For more information, see [Add data fields in tax configurations](tax-service-add-data-fields-tax-configurations.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="cc1d9-107">Gagnalíkan</span><span class="sxs-lookup"><span data-stu-id="cc1d9-107">Data model</span></span>

<span data-ttu-id="cc1d9-108">Gögnin í gagnalíkaninu eru flutt af hlutum og innleidd af klösum.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-108">The data in the data model is carried by objects and implemented by classes.</span></span>

<span data-ttu-id="cc1d9-109">Hér er listi yfir stærstu hlutina:</span><span class="sxs-lookup"><span data-stu-id="cc1d9-109">Here is a list of the major objects:</span></span>

* <span data-ttu-id="cc1d9-110">AxClass/TaxIntegration **Document** Object</span><span class="sxs-lookup"><span data-stu-id="cc1d9-110">AxClass/TaxIntegration **Document** Object</span></span>
* <span data-ttu-id="cc1d9-111">AxClass/TaxIntegration **Line** Object</span><span class="sxs-lookup"><span data-stu-id="cc1d9-111">AxClass/TaxIntegration **Line** Object</span></span>
* <span data-ttu-id="cc1d9-112">AxClass/TaxIntegration **TaxLine** Object</span><span class="sxs-lookup"><span data-stu-id="cc1d9-112">AxClass/TaxIntegration **TaxLine** Object</span></span>

<span data-ttu-id="cc1d9-113">Eftirfarandi mynd sýnir hvernig þessir hlutir tengjast.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-113">The following illustration shows how these objects are related.</span></span>

<span data-ttu-id="cc1d9-114">[![Vensl gagnalíkanshluta](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span><span class="sxs-lookup"><span data-stu-id="cc1d9-114">[![Data model object relationship](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span></span>

<span data-ttu-id="cc1d9-115">**Skjalahlutur** getur innihaldið marga **Línuhluti**.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-115">A **Document** object can contain many **Line** objects.</span></span> <span data-ttu-id="cc1d9-116">Hver hlutur inniheldur lýsigögn fyrir skattþjónustu.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-116">Each object contains metadata for the tax service.</span></span>

- <span data-ttu-id="cc1d9-117">`TaxIntegrationDocumentObject` er með `originAddress` lýsigögn sem innihalda upplýsingar um upprunaaðsetur og `includingTax` lýsigögn sem gefa til kynna hvort línuupphæðin innihaldi söluskatt.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-117">`TaxIntegrationDocumentObject` has `originAddress` metadata, which contains information about the source address, and `includingTax` metadata, which indicates whether the line amount includes sales tax.</span></span>
- <span data-ttu-id="cc1d9-118">`TaxIntegrationLineObject` er með `itemId`, `quantity`, og `categoryId` lýsigögn.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-118">`TaxIntegrationLineObject` has `itemId`, `quantity`, and `categoryId` metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="cc1d9-119">`TaxIntegrationLineObject` innleiðir einnig **Gjaldahluti**.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-119">`TaxIntegrationLineObject` also implements **Charge** objects.</span></span>

## <a name="integration-flow"></a><span data-ttu-id="cc1d9-120">Samþættingarferli</span><span class="sxs-lookup"><span data-stu-id="cc1d9-120">Integration flow</span></span>

<span data-ttu-id="cc1d9-121">Gögnum í flæðinu er stjórnað með aðgerðum.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-121">The data in the flow is manipulated by activities.</span></span>

### <a name="key-activities"></a><span data-ttu-id="cc1d9-122">Helstu aðgerðir</span><span class="sxs-lookup"><span data-stu-id="cc1d9-122">Key activities</span></span>

* <span data-ttu-id="cc1d9-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="cc1d9-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span></span>
* <span data-ttu-id="cc1d9-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="cc1d9-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span></span>
* <span data-ttu-id="cc1d9-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="cc1d9-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span></span>
* <span data-ttu-id="cc1d9-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="cc1d9-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span></span>
* <span data-ttu-id="cc1d9-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="cc1d9-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span></span>

<span data-ttu-id="cc1d9-128">Aðgerðir eru keyrðar í eftirfarandi röð:</span><span class="sxs-lookup"><span data-stu-id="cc1d9-128">Activities are run in the following order:</span></span>

1. <span data-ttu-id="cc1d9-129">Stilling endurheimtar</span><span class="sxs-lookup"><span data-stu-id="cc1d9-129">Setting Retrieval</span></span>
2. <span data-ttu-id="cc1d9-130">Endurheimt gagna</span><span class="sxs-lookup"><span data-stu-id="cc1d9-130">Data Retrieval</span></span>
3. <span data-ttu-id="cc1d9-131">Útreikningsþjónusta</span><span class="sxs-lookup"><span data-stu-id="cc1d9-131">Calculation Service</span></span>
4. <span data-ttu-id="cc1d9-132">Gjaldmiðlar</span><span class="sxs-lookup"><span data-stu-id="cc1d9-132">Currency Exchange</span></span>
5. <span data-ttu-id="cc1d9-133">Varanleiki gagna</span><span class="sxs-lookup"><span data-stu-id="cc1d9-133">Data Persistence</span></span>

<span data-ttu-id="cc1d9-134">Til dæmis þarf að stækka **Endurheimt gagna** á undan **Útreikningsþjónustu**.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-134">For example, extend **Data Retrieval** before **Calculation Service**.</span></span>

#### <a name="data-retrieval-activities"></a><span data-ttu-id="cc1d9-135">Aðgerðir gagnaendurheimtar</span><span class="sxs-lookup"><span data-stu-id="cc1d9-135">Data Retrieval activities</span></span>

<span data-ttu-id="cc1d9-136">Aðgerðir **Gagnaendurheimtar** sækir gögn úr gagnagrunni.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-136">**Data Retrieval** activities retrieve data from the database.</span></span> <span data-ttu-id="cc1d9-137">Gagnabreytar fyrir mismunandi færslur eru í boði til að sækja gögn úr mismunandi færslutöflum:</span><span class="sxs-lookup"><span data-stu-id="cc1d9-137">Adapters for different transactions are available to retrieve data from different transaction tables:</span></span>

- <span data-ttu-id="cc1d9-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="cc1d9-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span></span>
- <span data-ttu-id="cc1d9-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="cc1d9-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span></span>
- <span data-ttu-id="cc1d9-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="cc1d9-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span></span>
- <span data-ttu-id="cc1d9-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="cc1d9-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span></span>
- <span data-ttu-id="cc1d9-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="cc1d9-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span></span>
- <span data-ttu-id="cc1d9-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="cc1d9-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span></span>
- <span data-ttu-id="cc1d9-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="cc1d9-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span></span>

<span data-ttu-id="cc1d9-145">Í þessum aðgerðum **Gagnaendurheimtar** eru gögn afrituð úr gagnagrunninum í `TaxIntegrationDocumentObject` og `TaxIntegrationLineObject`.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-145">In these **Data Retrieval** activities, data is copied from the database to `TaxIntegrationDocumentObject` and `TaxIntegrationLineObject`.</span></span> <span data-ttu-id="cc1d9-146">Þar sem allar þessar aðgerðir stækka sama abstrakt sniðmátsklasann, notast þær við sömu aðferðirnar.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-146">Because all these activities extend the same abstract template class, they have common methods.</span></span>

#### <a name="calculation-service-activities"></a><span data-ttu-id="cc1d9-147">Aðgerðir útreikningsþjónustu</span><span class="sxs-lookup"><span data-stu-id="cc1d9-147">Calculation Service activities</span></span>

<span data-ttu-id="cc1d9-148">Aðgerðin **Útreikningsþjónusta** er tengillinn milli skattþjónustunnar og skattsamþættingarinnar.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-148">The **Calculation Service** activity is the link between the tax service and the tax integration.</span></span> <span data-ttu-id="cc1d9-149">Þessi aðgerð ber ábyrgð á eftirfarandi virkni:</span><span class="sxs-lookup"><span data-stu-id="cc1d9-149">This activity is responsible for the following functions:</span></span>

1. <span data-ttu-id="cc1d9-150">Setjið saman beiðnina.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-150">Construct the request.</span></span>
2. <span data-ttu-id="cc1d9-151">Birta beiðnina til skattþjónustu.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-151">Post the request to the tax service.</span></span>
3. <span data-ttu-id="cc1d9-152">Fá svar frá skattsþjónustunni.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-152">Get the response from the tax service.</span></span>
4. <span data-ttu-id="cc1d9-153">Þátta svarið.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-153">Parse the response.</span></span>

<span data-ttu-id="cc1d9-154">Gagnareitur sem bætt er við beiðnina verður bókaður saman með öðrum lýsigögnum.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-154">A data field that you add to the request will be posted together with other metadata.</span></span> 

## <a name="extension-implementation"></a><span data-ttu-id="cc1d9-155">Innleiðing viðbótar</span><span class="sxs-lookup"><span data-stu-id="cc1d9-155">Extension implementation</span></span>

<span data-ttu-id="cc1d9-156">Í þessum hluta eru ítarlegar leiðbeiningar sem útskýra hvernig á að innleiða viðbótina.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-156">This section provides detailed steps that explain how to implement the extension.</span></span> <span data-ttu-id="cc1d9-157">Hann notar fjárhagsvíddirnar **Kostnaðarstaður** og **Verk** sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-157">It uses the **Cost center** and **Project** financial dimensions as examples.</span></span>

### <a name="step-1-add-the-data-variable-in-the-object-class"></a><span data-ttu-id="cc1d9-158">1.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-158">Step 1.</span></span> <span data-ttu-id="cc1d9-159">Bætið gagnabreytunni við hlutaklasann</span><span class="sxs-lookup"><span data-stu-id="cc1d9-159">Add the data variable in the object class</span></span>

<span data-ttu-id="cc1d9-160">Hlutaklasinn inniheldur gagnabreytuna og sótt/sett aðferðir fyrir gögnin.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-160">The object class contains the data variable and getter/setter methods for the data.</span></span> <span data-ttu-id="cc1d9-161">Bætið gagnareitunum við annaðhvort `TaxIntegrationDocumentObject` eða `TaxIntegrationLineObject` eftir því hvert stig reitsins er.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-161">Add the data field to either `TaxIntegrationDocumentObject` or `TaxIntegrationLineObject`, depending on the level of the field.</span></span> <span data-ttu-id="cc1d9-162">Eftirfarandi dæmi notar línustigið og skráarheitið er `TaxIntegrationLineObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-162">The following example uses the line level, and the file name is `TaxIntegrationLineObject_Extension.xpp`.</span></span>

> [!NOTE]
> <span data-ttu-id="cc1d9-163">Ef gagnareiturinn sem verið er að bæta við er á stigi skjals skal breyta skráarheitinu í `TaxIntegrationDocumentObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-163">If the data field that you're adding is at the document level, change the file name to `TaxIntegrationDocumentObject_Extension.xpp`.</span></span>

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

<span data-ttu-id="cc1d9-164">**Kostnaðarstað** og **Verki** er bætt við sem einkabreytum.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-164">**Cost center** and **Project** are added as private variables.</span></span> <span data-ttu-id="cc1d9-165">Búið til sótt og sett aðferðir fyrir þessa gagnareiti til að vinna með gögnin.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-165">Create getter and setter methods for these data fields to manipulate the data.</span></span>

### <a name="step-2-retrieve-data-from-the-database"></a><span data-ttu-id="cc1d9-166">2.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-166">Step 2.</span></span> <span data-ttu-id="cc1d9-167">Sækja gögn úr gagnagrunni</span><span class="sxs-lookup"><span data-stu-id="cc1d9-167">Retrieve data from the database</span></span>

<span data-ttu-id="cc1d9-168">Tilgreinið færsluna og stækkið viðeigandi breytiklasa til að sækja gögnin.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-168">Specify the transaction, and extend the appropriate adapter classes to retrieve the data.</span></span> <span data-ttu-id="cc1d9-169">Ef **Innkaupapöntunar** færsla er t.d. notuð þarf að stækka `TaxIntegrationPurchTableDataRetrieval` og `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-169">For example, if you use a **Purchase order** transaction, you must extend `TaxIntegrationPurchTableDataRetrieval` and `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span></span> 

> [!NOTE]
> <span data-ttu-id="cc1d9-170">`TaxIntegrationPurchParmTableDataRetrieval` erfist frá `TaxIntegrationPurchTableDataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-170">`TaxIntegrationPurchParmTableDataRetrieval` is inherited from `TaxIntegrationPurchTableDataRetrieval`.</span></span> <span data-ttu-id="cc1d9-171">Ekki ætti að breyta henni nema regla í töflunum `purchTable` og `purchParmTable` er mismunandi.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-171">It should not be changed unless the logic of the `purchTable` and `purchParmTable` tables differs.</span></span>

<span data-ttu-id="cc1d9-172">Ef bæta á við gagnareit fyrir allar færslur skal stækka alla `DataRetrieval` klasa.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-172">If the data field should be added for all transactions, extend all `DataRetrieval` classes.</span></span>

<span data-ttu-id="cc1d9-173">Þar sem allar aðgerðir **Gagnaendurheimtar** stækka sama sniðmátsklasann, eru klasaskipulag, breytur og aðferðir svipaðar.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-173">Because all **Data Retrieval** activities extend the same template class, the class structures, variables, and methods are similar.</span></span>

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

<span data-ttu-id="cc1d9-174">Eftirfarandi dæmi sýnir grunnskipulagið þegar `PurchTable` taflan er notuð.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-174">The following example shows the basic structure when the `PurchTable` table is used.</span></span>

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

<span data-ttu-id="cc1d9-175">Þegar kallað er á `CopyToDocument` aðferðina er `this.purchTable` biðminnið þegar til staðar.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-175">When the `CopyToDocument` method is called, the `this.purchTable` buffer already exists.</span></span> <span data-ttu-id="cc1d9-176">Tilgangur þessarar aðferðar er að afrita öll áskilin gögn úr `this.purchTable` í `document` hlutinn með því að nota sett-aðferðina sem var búin til í `DocumentObject`-klasanum.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-176">The purpose of this method is to copy all the required data from `this.purchTable` to the `document` object by using the setter method that was created in the `DocumentObject` class.</span></span>

<span data-ttu-id="cc1d9-177">Á sama hátt er `this.purchLine` biðminni þegar til staðar í `CopyToLine` aðferðinni.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-177">Likewise, a `this.purchLine` buffer already exists in the `CopyToLine` method.</span></span> <span data-ttu-id="cc1d9-178">Tilgangur þessarar aðferðar er að afrita öll áskilin gögn úr `this.purchLine` í `_line` hlutinn með því að nota sett-aðferðina sem var búin til í `LineObject`-klasanum.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-178">The purpose of this method is to copy all the required data from `this.purchLine` to the `_line` object by using the setter method that was created in the `LineObject` class.</span></span>

<span data-ttu-id="cc1d9-179">Einfaldasta nálgunin er að stækka aðferðirnar `CopyToDocument` og `CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-179">The most straightforward approach is to extend the `CopyToDocument` and `CopyToLine` methods.</span></span> <span data-ttu-id="cc1d9-180">Hins vegar mælum við með því að reyna að nota `copyToDocumentFromHeaderTable` og `copyToLineFromLineTable` aðferðirnar fyrst.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-180">However, we recommend that you try the `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable` methods first.</span></span> <span data-ttu-id="cc1d9-181">Ef þær virka ekki sem skyldi skal innleiða eigin aðferð og kalla á hana í `CopyToDocument` og `CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-181">If they don't work as you require, implement your own method, and call it in `CopyToDocument` and `CopyToLine`.</span></span> <span data-ttu-id="cc1d9-182">Þrjár algengar aðstæður eru til staðar þar sem þessi nálgun gæti verið notuð:</span><span class="sxs-lookup"><span data-stu-id="cc1d9-182">There are three common situations where you might use this approach:</span></span>

- <span data-ttu-id="cc1d9-183">Áskilinn reitur er í `PurchTable` eða `PurchLine`.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-183">The required field is in `PurchTable` or `PurchLine`.</span></span> <span data-ttu-id="cc1d9-184">Í þessum aðstæðum er hægt að víkka `copyToDocumentFromHeaderTable` og `copyToLineFromLineTable`.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-184">In this situation, you can extend `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable`.</span></span> <span data-ttu-id="cc1d9-185">Hér er dæmakóði.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-185">Here is the sample code.</span></span>

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

- <span data-ttu-id="cc1d9-186">Áskilin gögn eru ekki í sjálfgefinni töflu færslunnar.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-186">The required data isn't in the default table of the transaction.</span></span> <span data-ttu-id="cc1d9-187">Hins vegar eru nokkur vensl töflutenginga við sjálfgefnu töfluna og reiturinn er áskilinn í flestum línum.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-187">However, there are some join relationships with the default table, and the field is required on most lines.</span></span> <span data-ttu-id="cc1d9-188">Í þessum aðstæðum skal skipta út `getDocumentQueryObject` eða `getLineObject` til að senda fyrirspurn á töfluna eftir venslum tengingar.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-188">In this situation, replace `getDocumentQueryObject` or `getLineObject` to query the table by join relationship.</span></span> <span data-ttu-id="cc1d9-189">Í eftirfarandi dæmi er reiturinn **Afhenda nú** samþættur við sölupöntunina á línustiginu.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-189">In the following example, the **Deliver Now** field is integrated with the sales order at the line level.</span></span>

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

    <span data-ttu-id="cc1d9-190">Í þessu dæmi er `mcrSalesLineDropShipment` biðminni gefið upp og fyrirspurnin er skilgreind í `getLineQueryObject`.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-190">In this example, a `mcrSalesLineDropShipment` buffer is declared, and the query is defined in `getLineQueryObject`.</span></span> <span data-ttu-id="cc1d9-191">Fyrirspurnin notar venslin `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-191">The query uses the relationship `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span></span> <span data-ttu-id="cc1d9-192">Meðan verið er að stækka í þessum aðstæðum er hægt að skipta út `getLineQueryObject` fyrir eiginn samansettan fyrirspurnarhlut.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-192">While you're extending in this situation, you can replace `getLineQueryObject` with your own constructed query object.</span></span> <span data-ttu-id="cc1d9-193">Athugið hins vegar eftirfarandi atriði:</span><span class="sxs-lookup"><span data-stu-id="cc1d9-193">However, note the following points:</span></span>

    * <span data-ttu-id="cc1d9-194">Vegna þess að skilagildi `getLineQueryObject` aðferðarinnar er `SysDaQueryObject` þarf að setja saman þennan hlut með því að nota SysDa nálgun.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-194">Because the return value of the `getLineQueryObject` method is `SysDaQueryObject`, you must construct this object by using the SysDa approach.</span></span>
    * <span data-ttu-id="cc1d9-195">Ekki er hægt að fjarlægja fyrirliggjandi töflu.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-195">Can't remove existed table.</span></span>

- <span data-ttu-id="cc1d9-196">Nauðsynleg gögn tengjast flutningstöflunni með flóknum venslum töflutengingar eða venslin eru ekki ein á móti einu (1:1) heldur ein á móti mörgum (1:N).</span><span class="sxs-lookup"><span data-stu-id="cc1d9-196">The required data is related to the transaction table by a complicated join relationship, or the relation isn't one to one (1:1) but one to many (1:N).</span></span> <span data-ttu-id="cc1d9-197">Í þessum aðstæðum flækjast málin aðeins.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-197">In this situation, things become a little complicated.</span></span> <span data-ttu-id="cc1d9-198">Þessar aðstæður eiga við um dæmið um fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-198">This situation applies to the example of financial dimensions.</span></span> 

    <span data-ttu-id="cc1d9-199">Í þessum aðstæðum er hægt að innleiða eigin aðferð til að sækja gögnin.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-199">In this situation, you can implement your own method to retrieve the data.</span></span> <span data-ttu-id="cc1d9-200">Hér er dæmakóðinn í `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` skránni.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-200">Here is the sample code in the `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` file.</span></span>

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

### <a name="step-3-add-data-to-the-request"></a><span data-ttu-id="cc1d9-201">Skref 3.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-201">Step 3.</span></span> <span data-ttu-id="cc1d9-202">Bæta gögnum við beiðnina</span><span class="sxs-lookup"><span data-stu-id="cc1d9-202">Add data to the request</span></span>

<span data-ttu-id="cc1d9-203">Framlengið `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` eða `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` aðferðina til að bæta gögnum við beiðnina.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-203">Extend the `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` or `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method to add data to the request.</span></span> <span data-ttu-id="cc1d9-204">Hér er dæmakóðinn í `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` skránni.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-204">Here is the sample code in the `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` file.</span></span>

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

<span data-ttu-id="cc1d9-205">Í þessum kóða er `_destination` pökkunarhluturinn sem er notaður til að búa til bókunarbeiðnina og `_source` er `TaxIntegrationLineObject` hluturinn.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-205">In this code, `_destination` is the wrapper object that is used to generate the post request, and `_source` is the `TaxIntegrationLineObject` object.</span></span> 

> [!NOTE]
> * <span data-ttu-id="cc1d9-206">Skilgreinið lykilinn sem er notaður í skjámynd beiðninnar sem `private const str`.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-206">Define the key that is used in the request form as `private const str`.</span></span>
> * <span data-ttu-id="cc1d9-207">Stillið reitinn í `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` aðferðinni með því að nota `SetField` aðferðina.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-207">Set the field in the `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method by using the `SetField` method.</span></span> <span data-ttu-id="cc1d9-208">Gagnagerð seinni færibreytunnar á að vera `string`.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-208">The data type of the second parameter should be `string`.</span></span> <span data-ttu-id="cc1d9-209">Ef gagnagerðin er ekki `string` skal umbreyta henni í `string`.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-209">If the data type isn't `string`, convert it to `string`.</span></span>

## <a name="appendix"></a><span data-ttu-id="cc1d9-210">Viðauki</span><span class="sxs-lookup"><span data-stu-id="cc1d9-210">Appendix</span></span>

<span data-ttu-id="cc1d9-211">Þessi viðauki sýnir ítarlegan sýnishornakóða fyrir samþættingu fjárhagsvídda (**Kostnaðarstaður** og **Verk**) á línustiginu.</span><span class="sxs-lookup"><span data-stu-id="cc1d9-211">This appendix shows the complete sample code for the integration of financial dimensions (**Cost center** and **Project**) at the line level.</span></span>

### <a name="taxintegrationlineobject_extensionxpp"></a><span data-ttu-id="cc1d9-212">TaxIntegrationLineObject_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="cc1d9-212">TaxIntegrationLineObject_Extension.xpp</span></span>

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

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a><span data-ttu-id="cc1d9-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="cc1d9-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span></span>

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

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a><span data-ttu-id="cc1d9-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="cc1d9-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span></span>

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
