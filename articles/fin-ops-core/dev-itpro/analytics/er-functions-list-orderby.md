---
title: ORDERBY ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ORDERBY í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 963d55bcf98a9109c8b6ceb57edf5b55f15a2b0f
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075175"
---
# <a name="orderby-er-function"></a>ORDERBY ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `ORDERBY` skilar tilgreindum lista sem *Skráalista*-gildi eftir að því hefur verið raðað í samræmi við tilgreindar frumbreytur. Þessi frumbreytur geta verið skilgreindar sem segðir.

## <a name="syntax-1"></a><a name="syntax-1"></a>Málskipun 1

```vb
ORDERBY (list, expression 1[, expression 2, …, expression N])
```

## <a name="syntax-2"></a><a name="syntax-2"></a>Málskipun 2

```vb
ORDERBY (location, list, expression 1[, expression 2, …, expression N])
```

> [!NOTE]
> Þessi setningafræði er studd fyrir Microsoft Dynamics 365 Finance útgáfu 10.0.25 og síðar.

## <a name="arguments"></a>Frumbreytur

`location`:*[Strengur](er-formula-supported-data-types-primitive.md#string)*

Staðurinn þar sem flokkun ætti að fara fram. Eftirfarandi valkostir gilda:

- "Fyrirspurn"
- "InMemory"

`list`:*[Met listi](er-formula-supported-data-types-composite.md#record-list)*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.

`expression 1`: *Reitur*

Gild slóð á reit gagnagjafans sem vísað er til af frumbreytunni `list` af kallaðri aðgerð. Tilvísaður reitur verður að vera reitur af frumstæðri gagnagerð. Þessi frumbreyta er áskilin.

`expression N`: *Reitur*

Gild slóð á reit gagnagjafans sem vísað er til af frumbreytunni `list` af kallaðri aðgerð. Tilvísaður reitur verður að vera reitur af frumstæðri gagnagerð. Þessar viðbótarfrumbreytur eru valkvæðar.

## <a name="return-values"></a>Skilagildi

*Færslulisti*

Sá listi yfir skrár sem er búinn til.

## <a name="usage-notes"></a>Notkunarbréf

### <a name="syntax-1"></a>Málskipun 1

Gagnaflokkun fer alltaf fram í minni forritaþjónsins. Fyrir frekari upplýsingar, sjá [dæmi 1](#example-1).

### <a name="syntax-2"></a>Málskipun 2

### <a name="sorting-in-memory"></a>Flokkun í minni

Þegar`location` rök eru tilgreind sem **InMemory**, gagnaflokkun fer fram í minni forritaþjóns. Fyrir frekari upplýsingar, sjá [dæmi 2](#example-2).

### <a name="sorting-in-database"></a>Flokkun í gagnagrunni

Þegar`location` rök eru tilgreind sem **Fyrirspurn**, gagnaflokkun er gerð á gagnagrunnsstigi. Í þessu tilviki er`list` rök verða að benda á eitt af eftirfarandi [Rafræn skýrslugerð (ER)](general-electronic-reporting.md) gagnagjafar sem tilgreina forritsuppsprettu sem hægt er að koma á beinni gagnagrunnsfyrirspurn fyrir:

- Uppspretta gagna *Taflaskrár* tegund
- Tengsl gagnagjafa *Taflaskrár* tegund
- Uppspretta gagna *Reikningsreitur* tegund

The`expression 1` og`expression N` rök verða að benda á reiti ER gagnagjafa sem tilgreinir viðeigandi reiti forritsuppsprettu sem einnig er hægt að stofna beina gagnagrunnsfyrirspurn fyrir.

Ef ekki er hægt að koma á beinni gagnagrunnsfyrirspurn, er staðfesting [villa](er-components-inspections.md#i18) á sér stað í ER líkanskortahönnuðinum. Skilaboðin sem birtast gefa til kynna að segð rafrænnar skýrslugerðar sem inniheldur `ORDERBY`-aðgerðina sé ekki hægt að keyra við keyrslu.

Fyrir betri frammistöðu mælum við með að þú notir **Fyrirspurn** valmöguleika þegar flokkunin er stillt fyrir gagnagjafa forrita sem gætu innihaldið mikinn fjölda skráa (til dæmis fyrir viðskiptaforritstöflur).

> [!NOTE]
> The`ORDEBY` Ekki er hægt að þýða aðgerðina sjálfa yfir á beina gagnagrunnsfyrirspurn. Þess vegna er ekki hægt að spyrjast fyrir um ER gagnagjafa sem inniheldur þessa aðgerð. Það er heldur ekki hægt að nota það í umfangi ER aðgerðir eins og [SÍA](er-functions-list-filter.md) og [ALLITEMSQUERY](er-functions-list-allitemsquery.md), þar sem aðeins er hægt að nota gagnagjafa sem hægt er að spyrja um.

Fyrir frekari upplýsingar, sjá [dæmi 3](#example-3) og [dæmi 4](#example-4).

### <a name="comparability"></a>Sambærileiki

Þar sem SQL gagnagrunnsvélin og Finance forritaþjónninn geta notað mismunandi röðunargildi fyrir einn staf, getur flokkunarniðurstaða sama lista yfir færslur verið mismunandi þegar [Strengur](er-formula-supported-data-types-primitive.md#string) reiturinn er notaður til flokkunar. Fyrir frekari upplýsingar, sjá [dæmi 5](#example-5).

## <a name="example-1-in-memory-default-execution"></a><a name="example-1"></a> Dæmi 1: Sjálfgefin framkvæmd í minni

Ef þú slærð inn gagnagjafann **DS** af gerðinni *Reiknaður reitur* og hann inniheldur segðina `SPLIT ("C|B|A", "|")` skilar segðin `FIRST( ORDERBY( DS, DS. Value)).Value` textagildinu **"A"**.

## <a name="example-2-in-memory-explicit-execution"></a><a name="example-2"></a> Dæmi 2: In-memory skýr framkvæmd

Ef **Seljandi** er stillt sem ER gagnagjafi *Taflaskrár* gerð sem vísar til **VendTable** borð, bæði tjáning`ORDERBY (Vendor, Vendor.'name()')` og tjáningin`ORDERBY ("InMemory", Vendor, Vendor.'name()')` skila lista yfir söluaðila sem er raðað eftir nafni í hækkandi röð.

Þegar þú stillir tjáninguna`ORDERBY ("Query", Vendor, Vendor.'name()')` í ER módel kortlagningarhönnuður, löggilding [villa](er-components-inspections.md#i8) á sér stað á hönnunartíma, vegna þess að`Vendor.'name()'` slóð vísar til umsóknaraðferðar sem hefur rökfræði sem ekki er hægt að þýða í beina gagnagrunnsfyrirspurn.

## <a name="example-3-database-query"></a><a name="example-3"></a> Dæmi 3: Gagnagrunnsfyrirspurn

Ef **Skattaviðskipti** er stillt sem ER gagnagjafi *Taflaskrár* gerð sem vísar til **TaxTrans** borð, tjáningin`ORDERBY ("Query", TaxTransaction, TaxTransaction.TaxCode)` flokkar færslur á stigi umsóknargagnagrunnsins og skilar lista yfir skattfærslur sem eru flokkaðar eftir skattkóða í hækkandi röð.

## <a name="example-4-queryable-data-sources"></a><a name="example-4"></a> Dæmi 4: Fyrirspurnar gagnaheimildir

Ef **Skattaviðskipti** er stillt sem ER gagnagjafi *Taflaskrár* gerð sem vísar til **TaxTrans** borð, the **TaxTransactionFiltered** Hægt er að stilla ER gagnagjafa þannig að hann innihaldi tjáninguna`FILTER(TaxTransaction, TaxCode="VAT19")` sem mun sækja færslur fyrir tiltekinn skattkóða. Vegna þess að stillt **TaxTransactionFiltered** ER gagnagjafinn er hægt að spyrjast fyrir, tjáningin`ORDERBY ("Query", TaxTransactionFiltered, TaxTransactionFiltered.TransDate)` er hægt að stilla til að skila lista yfir síaðar skattfærslur sem er raðað eftir færsludegi í hækkandi röð.

Ef þú stillir **TaxTransactionOrdered** sem ER gagnagjafi *Reiknaður reitur* gerð sem inniheldur tjáninguna`ORDERBY ("Query", TaxTransaction, TaxTransaction.TransDate)` og ER gagnauppspretta *Reiknaður reitur* gerð sem inniheldur tjáninguna`FILTER(TaxTransactionOrdered, TaxCode="VAT19")`, staðfesting [villa](er-components-inspections.md#i18) á sér stað á hönnunartíma í ER líkanskortahönnuðinum. Þessi villa kemur upp vegna þess að fyrstu rökin í [SÍA](er-functions-list-filter.md#usage-notes) aðgerð verður að vísa til fyrirspurnarhæfs ER gagnagjafa, en **TaxTransactionOrdered** gagnagjafi sem inniheldur`ORDERBY` aðgerð er ekki hægt að spyrja um.

## <a name="example-5-comparability"></a><a name="example-5"></a> Dæmi 5: Samanburður

### <a name="prerequisites"></a>Forkröfur

1. Sláðu inn gagnagjafa **DS1** af *Reiknaður reitur* gerð sem inniheldur tjáninguna `SPLIT ("D1|_D2|D3", "|")`.
2. Opnaðu **[Fjárhagsvíddargildi](../../../finance/general-ledger/financial-dimensions.md)** síðu og veldu **Kostnaðarmiðstöð** vídd.
3. Sláðu inn eftirfarandi víddargildi: **D1**,**\_ D2**, og **D3**.

### <a name="sorting-in-memory"></a>Flokkun í minni

1. Stilla gagnagjafa **DS2** af *Reiknaður reitur* gerð sem inniheldur tjáninguna `ORDERBY("InMemory", DS1, DS1.Value)`.
2. Taktu eftir því að tjáningin`FIRST(DS2).Value` skilar textagildinu **"D1"**, tjáningin`INDEX(DS2, COUNT(DS2)).Value` skilar textagildinu **"\_ D2"**, og tjáningin`STRINGJOIN(DS2, DS2.Value, "|")` skilar textagildinu **„D1\| D3\|\_ D2"**.

### <a name="sorting-in-database"></a>Flokkun í gagnagrunni

1. Sláðu inn gagnagjafa **DS3** af *Taflaskrár* gerð sem vísar til **FinancialDimensionValueEntity** aðila.
2. Stilla gagnagjafa **DS4** af *Reiknaður reitur* gerð sem inniheldur tjáninguna `FILTER(DS3, DS3.FinancialDimension="CostCenter")`.
3. Stilla gagnagjafa **DS5** af *Reiknaður reitur* gerð sem inniheldur tjáninguna `ORDERBY(DS4, DS4.DimensionValue)`.
4. Taktu eftir því að tjáningin`FIRST(DS5).Value` skilar textagildinu **"\_ D2"**, tjáningin`INDEX(DS5, COUNT(DS5)).Value` skilar textagildinu **"D3"**, og tjáningin`STRINGJOIN(DS5, DS5.Value, "|")` skilar textagildinu **"\_ D2\| D1\| D3"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Listaaðgerðir](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
