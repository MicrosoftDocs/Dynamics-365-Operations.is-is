---
title: ORDERBY ER-aðgerð
description: Í þessari grein er að finna upplýsingar um hvernig ORDERBY rafræn skýrslugerðarvirkni (ER) er notuð.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 23ace859bf75b2adb6ef8604475519a015486948
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282562"
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
> Þessi málskipan studd fyrir Microsoft Dynamics 365 Finance útgáfu 10.0.25 og síðar.

## <a name="arguments"></a>Frumbreytur

`location`: *[Strengur](er-formula-supported-data-types-primitive.md#string)*

Staðsetningin þar sem á að keyra röðunina. Eftirtaldir valkostir eru gildir:

- "Query"
- "InMemory"

`list`: *[Færslulisti](er-formula-supported-data-types-composite.md#record-list)*

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

Gagnaröðun er alltaf gerð í minni forritaþjónsins. Nánari upplýsingar er að finna í [dæmi 1](#example-1).

### <a name="syntax-2"></a>Málskipun 2

### <a name="sorting-in-memory"></a>Röðun í minni

Þegar `location` frumbreytan er tilgreind sem **InMemory** er gagnaröðun gerð í minni forritsþjónsins. Nánari upplýsingar er að finna í [dæmi 2](#example-2).

### <a name="sorting-in-database"></a>Flokkun í gagnagrunni

Þegar `location` frumbreytan er tilgreind sem **Fyrirspurn** er gagnaröðun gerð á stigi gagnagrunns. Þá verður `list` frumbreytan að benda á einn af eftirfarandi gagnagjöfum [Rafrænnar skýrslugerðar](general-electronic-reporting.md) sem tilgreinir forritsupprunann sem hægt er að gera beina fyrirspurn á gagnagrunn fyrir:

- Gagnagjafi af gerðinni *Töfluskrár*.
- Tengsl gagnagjafa af gerðinni *Töflufærslur*.
- Gagnagjafi af gerðinni *Útreikningsreitur*.

Frumbreyturnar `expression 1` og `expression N` verða að benda á reiti í gagnagjafa rafrænnar skýrslugerðar sem tilgreina viðeigandi reiti forritsupprunans sem einnig er hægt að gera bein fyrirspurn gagnagrunns fyrir.

Ef ekki er hægt að koma á fót beinni gagnagrunnsfyrirspurn kemur upp [villa](er-components-inspections.md#i18) við villuleit í hönnuði líkanavörpunar rafrænnar skýrslugerðar. Skilaboðin sem birtast gefa til kynna að segð rafrænnar skýrslugerðar sem inniheldur `ORDERBY`-aðgerðina sé ekki hægt að keyra við keyrslu.

Fyrir betri afköst er mælt með að nota valkostinn **Fyrirspurn** þegar röðun er skilgreind fyrir uppruna forritsgagna sem gæti innihaldið mikinn fjölda af færslum (til dæmis fyrir færslutengdar forritstöflur).

> [!NOTE]
> Ekki er hægt að þýða `ORDEBY` aðgerðina sjálfa yfir í beina gagnagrunnsfyrirspurn. Því er ekki hægt að spyrjast fyrir um gagnagjafa rafrænnar skýrslugerðar sem inniheldur þessa aðgerð. Ekki er heldur hægt að nota hann í umfangi rafrænnar skýrslugerðarvirkni eins og [FILTER](er-functions-list-filter.md) og [ALLITEMSQUERY](er-functions-list-allitemsquery.md) þar sem aðeins er hægt að nota einn fyrirspurnarhæfan gagnagjafa.

Frekari upplýsingar er að finna í [dæmi 3](#example-3) og [dæmi 4](#example-4).

### <a name="comparability"></a>Samanburðarhæfi

Fyrst að SQL-gagnagrunnsvél og Finance-forritsþjónn geta notað mismunandi röðunargildi fyrir einn staf getur niðurstaða röðunar á sama færslulista verið mismunandi þegar reiturinn [Strengur](er-formula-supported-data-types-primitive.md#string) er notaður fyrir röðun. Nánari upplýsingar er að finna í [dæmi 5](#example-5).

## <a name="example-1-in-memory-default-execution"></a><a name="example-1"></a>Dæmi 1: Sjálfgefin keyrsla í minni

Ef þú slærð inn gagnagjafann **DS** af gerðinni *Reiknaður reitur* og hann inniheldur segðina `SPLIT ("C|B|A", "|")` skilar segðin `FIRST( ORDERBY( DS, DS. Value)).Value` textagildinu **"A"**.

## <a name="example-2-in-memory-explicit-execution"></a><a name="example-2"></a>Dæmi 2: Keyrsla í minni

Ef **Lánardrottinn** er stilltur sem gagnagjafi rafrænnar skýrslugerðar (ER) gerðarinnar *Töflufærslur* sem vísar til töflunnar **VendTable** skilar segðin `ORDERBY (Vendor, Vendor.'name()')` og segðin `ORDERBY ("InMemory", Vendor, Vendor.'name()')` lista yfir lánardrottna sem er raðað eftir nafni í lækkandi röð.

Þegar þú skilgreinir segðina `ORDERBY ("Query", Vendor, Vendor.'name()')` í hönnuði líkanavörpunar rafrænnar skýrslugerðar kemur upp [staðfestingarvilla](er-components-inspections.md#i8) á hönnunartíma því að `Vendor.'name()'` slóðin vísar í forritsaðferð sem er með rök sem ekki er hægt að þýða á beina fyrirspurn gagnagrunns.

## <a name="example-3-database-query"></a><a name="example-3"></a>Dæmi 3: Gagnagrunnsfyrirspurn

Ef **TaxTransaction** er skilgreint sem gagnagjafi rafrænnar skýrslugerðar af gerðinni *Töflufærslur* sem vísar í töfluna **TaxTrans** mun segðin `ORDERBY ("Query", TaxTransaction, TaxTransaction.TaxCode)` raða færslum á gagnagrunnsstigi forritsins og skila lista yfir skattfærslur sem er raðað eftir skattkóða í hækkandi röð.

## <a name="example-4-queryable-data-sources"></a><a name="example-4"></a>Dæmi 4: Fyrirspurnarhæfir gagnagjafar

Ef **TaxTransaction** er skilgreint sem gagnagjafi rafrænnar skýrslugerðar af gerðinni *Töflufærslur* sem vísar í töfluna **TaxTrans** er hægt að skilgreina gagnagjafann **TaxTransactionFiltered** fyrir rafræna skýrslugerð þannig að hann innihaldi segðina `FILTER(TaxTransaction, TaxCode="VAT19")` sem mun sækja færslur fyrir tiltekinn skattkóða. Þar sem skilgreindi gagnagjafinn **TaxTransactionFiltered** fyrir rafræna skýrslugerð er fyrirspurnarhæfur er hægt að skilgreina segðina `ORDERBY ("Query", TaxTransactionFiltered, TaxTransactionFiltered.TransDate)` á að skila lista yfir síaðar skattfærslur sem er raðað eftir færsludagsetningu í hækkandi röð.

Ef þú skilgreinir **TaxTransactionOrdered** sem gagnagjafa rafrænnar skýrslugerðar af gerðinni *Reiknaður reitur* sem inniheldur segðina `ORDERBY ("Query", TaxTransaction, TaxTransaction.TransDate)` og gagnagjafa rafrænnar skýrslugerðar af gerðinni *Reiknaður reitur* sem inniheldur segðina `FILTER(TaxTransactionOrdered, TaxCode="VAT19")` kemur upp [staðfestingarvilla](er-components-inspections.md#i18) á hönnunartíma í hönnuði líkanavörpunar rafrænnar skýrslugerðar. Þessi villa kemur upp vegna þess að fyrsta frumbreytan fyrir [FILTER](er-functions-list-filter.md#usage-notes) aðgerðina verður að vísa í fyrirspurnarhæfan gagnagjafa rafrænnar skýrslugerðar en gagnagjafinn **TaxTransactionOrdered** sem inniheldur `ORDERBY` aðgerðina er ekki fyrirspurnarhæfur.

## <a name="example-5-comparability"></a><a name="example-5"></a>Dæmi 5: Samanburður

### <a name="prerequisites"></a>Forkröfur

1. Færið inn gagnagjafa **DS1** af gerðinni *Reiknað svæði* sem inniheldur segðina `SPLIT ("D1|_D2|D3", "|")`.
2. Opnaðu síðuna **[Fjárhagsvíddargildi](../../../finance/general-ledger/financial-dimensions.md)** og veldu víddina **CostCenter**.
3. Sláðu inn eftirfarandi víddargildi: **D1**, **\_D2** og **D3**.

### <a name="sorting-in-memory"></a>Röðun í minni

1. Skilgreina gagnagjafa **DS2** af gerðinni *Reiknað svæði* sem inniheldur segðina `ORDERBY("InMemory", DS1, DS1.Value)`
2. Taktu eftir að segðin `FIRST(DS2).Value` skilar textagildinu **„D1“**, segðin `INDEX(DS2, COUNT(DS2)).Value` skilar textagildinu **„\_D2“** og segðin `STRINGJOIN(DS2, DS2.Value, "|")` skilar textagildinu **„D1\|D3\|\_D2“**.

### <a name="sorting-in-database"></a>Flokkun í gagnagrunni

1. Færið inn gagnagjafinn **DS3** af gerðinni *Töflufærslur* sem vísar til einingarinnar **FinancialDimensionValueEntity**.
2. Skilgreina gagnagjafa **DS4** af gerðinni *Reiknað svæði* sem inniheldur segðina `FILTER(DS3, DS3.FinancialDimension="CostCenter")`
3. Skilgreina gagnagjafa **DS5** af gerðinni *Reiknað svæði* sem inniheldur segðina `ORDERBY(DS4, DS4.DimensionValue)`
4. Taktu eftir að segðin `FIRST(DS5).Value` skilar textagildinu **„\_D2“**, segðin `INDEX(DS5, COUNT(DS5)).Value` skilar textagildinu **„D3“** og segðin `STRINGJOIN(DS5, DS5.Value, "|")` skilar textagildinu **„\_D2\|D1\|D3“**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Listaaðgerðir](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
