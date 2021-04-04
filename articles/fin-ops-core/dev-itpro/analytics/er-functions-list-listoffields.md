---
title: LISTOFFIELDS ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin LISTOFFIELDS í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
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
ms.openlocfilehash: 494dc347fadf44121c7eae0acf8c30768c58f035
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567665"
---
# <a name="listoffields-er-function"></a>LISTOFFIELDS ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `LISTOFFIELDS` skilar *Skráalista*-gildi sem er stofnað byggt á skipulagi tilgreindrar segðar af gerðinni *Upptalning* eða *Ílát (skrá)*.

## <a name="syntax-1"></a>Málskipun 1

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a>Málskipun 2

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a>Frumbreytur

`path`: Tilvísun í gagnagjafa

Gild tilvísunarslóð gagnagjafa af einni af eftirfarandi gagnagerðum:

- Tölusetning líkans
- Tölusetning sniðs
- Upptalning forrita
- Gámur (skrá)

`language`: *Strengur*

Texti sem táknar tungumálakóða.

## <a name="return-values"></a>Skilagildi

*Skráalisti*

Sá listi yfir skrár sem er búinn til.

## <a name="usage-notes"></a>Notkunarbréf

Listinn sem er búinn til samanstendur af færslum sem hafa eftirfarandi svæði:

- **Heiti** (gagnagerðin *Strengur*)
- **Merki** (gagnagerðin *Strengur*)
- **Lýsing** (gagnagerðin *Strengur*)
- **IsTranslated** (gagnagerðin *Boolean*)

Ef frumbreytan `path` vísar til gagnagjafa af gerðinni *Gámur (skrá)* er nýrri skrá bætt við listann sem var stofnaður fyrir hvern reit í gámaskránni sem vísað er til. Fyrir hverja skrá sem er búin til skilar reiturinn **Heiti** heitinu á reit tilvísaðrar gámaskráar sem núverandi skrá var búin til fyrir.

Ef frumbreytan `path` vísar til gagnagjafa eins af gerðunum *Upptalning* er nýrri skrá bætt við listann sem var stofnaður fyrir hvert upptalningargildi í upptalningunni sem vísað er til. Fyrir hverja skrá sem er búin til skilar reiturinn **Heiti** gildi tilvísunarupptalningarinnar sem núverandi skrá var stofnuð fyrir, reiturinn **Lýsing** skilar lýsingunni á þeirri upptalningu og reiturinn **Merki** skilar merki þeirrar upptalningar.

Á keyrslutíma, þegar málskipan 1 er notuð, verða reitirnir **Merki** og **Lýsing** að skila gildum sem eru byggðir á tungumálastillingum í sniði rafrænnar skýrslugerðar (ER) sem er í keyrslu:

- Ef merki og lýsingar fyrir umbeðið tungumál eru í boði skila reitirnir **Merki** og **Lýsing** gildum sem byggjast á því tungumáli og reiturinn **IsTranslated** skilar **True**.
- Ef merki og lýsingar fyrir umbeðið tungumál eru ekki í boði skila reitirnir **Merki** og **Lýsing** gildum sem byggjast á sjálfgefnu tungumáli **EN-US** og reiturinn **IsTranslated** skilar **False**.

Á keyrslutíma, þegar málskipan 2 er notuð, verða reitirnir **Merki** og **Lýsing** að skila gildum sem eru byggðir á tungumáli sem er skilgreint sem seinni frumgerð kallaðrar aðgerðar:

- Ef merki og lýsingar fyrir umbeðið tungumál eru í boði skila reitirnir **Merki** og **Lýsing** gildum sem byggjast á því tungumáli og reiturinn **IsTranslated** skilar **True**.
- Ef merki og lýsingar fyrir umbeðið tungumál eru ekki í boði skila reitirnir **Merki** og **Lýsing** gildum sem byggjast á tungumáli **EN-US** og reiturinn **IsTranslated** skilar **False**.

## <a name="example-1"></a>Dæmi 1

Í eftirfarandi mynd er kynnt upptalning í ER-gagnalíkönum.

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

Eftirfarandi mynd sýnir þessar upplýsingar:

- Upptalning líkans er sett í skýrslu sem gagnagjafi.
- Segð rafrænnar skýrslugerðar notar tölusetningarlíkanið sem breytu á `LISTOFFIELDS`-aðgerðinni.
- Gagnagjafi af gerðinni *skráalisti* er settur í skýrslu með því að nota stofnaða segð rafrænnar skýrslugerðar.

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

Eftirfarandi dæmi sýnir sniðseiningar rafrænnar skýrslugerðar sem eru bundin við gagnagjafa af gerðinni *skráalisti* sem var búin til með því að nota `LISTOFFIELDS`-aðgerðina.

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

Eftirfarandi mynd sýnir niðurstöðuna þegar hannaða sniðið er keyrt.

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> Byggt á tungumálastillingum á yfirsniðseiningum **FILE** og **FOLDER**, er þýddur texti fyrir merki og lýsingar sleginn inn sem úttak ER-sniðs.

## <a name="example-2"></a>Dæmi 2

Þú notar gagnagjafagerðina *Útreiknað svæði* til að stilla gagnagjafa **enumType\_de** og **enumType\_deCH** fyrir tölusetningu gagnalíkansins **enumType**:

- **enumType\_de** = `LISTOFFIELDS (enumType, "de")`
- **enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`

Í þessu tilfelli er hægt að nota eftirfarandi segð til að fá merkið á tölusetningargildinu á svissneskri þýsku, ef sú þýðing er í boði. Ef svissnesk þýska þýðingin er ekki tiltæk er merkið á þýsku.

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]