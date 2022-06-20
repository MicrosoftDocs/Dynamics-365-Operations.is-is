---
title: SPLIT ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig SPLIT rafræn skýrslugerð (ER) aðgerðin er notuð.
author: NickSelin
ms.date: 04/01/2021
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
ms.openlocfilehash: 2acd93b645121b577d516d3ce29a3d05069b8de9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906830"
---
# <a name="split-er-function"></a>SPLIT ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `SPLIT` skiptir upp tilteknum ílagsstreng í undirstrengi og skilar niðurstöðunni sem nýju *Skráalista*-gildi.

## <a name="syntax-1"></a>Málskipun 1

```vb
SPLIT (input, length)
```

Þessi málskipan er notuð til að skipta tilgreindum intaksstreng í undirstrengi, sem hvert um sig hefur tilgreinda lengd.

## <a name="syntax-2"></a>Málskipun 2

```vb
SPLIT (input, delimiter)
```

Þessi málskipan er notuð til að skipta tilgreindum innsláttarstreng í undirstrengi, byggt á tilgreindu skiltákni.

## <a name="arguments"></a>Frumbreytur

`input`: *Strengur*

Textinn sem á að skipta.

`length`: *Heiltala*

Hámarkslengd staks undirstrengs.

`delimiter`: *Strengur*

Afmarkari sem er notaður til að aðgreina undirstrengi.

## <a name="return-values"></a>Skilagildi

*Skráalisti*

Sá listi yfir skrár sem er búinn til.

## <a name="usage-notes"></a>Notkunarbréf

Skráaskipulag listans sem er skilað samanstendur af reitnum **Gildi** af gerðinni *Strengur*. Sérhver skrá yfir listann sem er skilað inniheldur myndaða undirstrengi í þessum reit.

Ef frumbreytan `delimiter` er tóm samantendur nýi listinn sem er skilað af einni skrá sem inniheldur reitinn **Gildi** af gerðinni *Strengur*. Þessi reitur inniheldur innsláttartexta.

Ef frumbreytan `input` er tóm er nýjum tómum lista skilað. Ef annaðhvort frumbreyta `input` eða `delimiter` er óskilgreind (núll) er gerð undantekning í hugbúnaðinum.

## <a name="example-1"></a>Dæmi 1

`SPLIT ("abcd", 3)` skilar nýjum lista sem samanstendur af tveimur skrám sem eru með reitinn **Gildi** af gerðinni *Strengur*. Reiturinn **Gildi** í fyrstu skránni inniheldur textann **"abc"** og reiturinn **Gildi** í annarri skránni inniheldur textann **"d"**.

## <a name="example-2"></a>Dæmi 2

`SPLIT ("XAb aBy", "aB")` skilar nýjum lista sem samanstendur af þremur skrám sem eru með reitinn **Gildi** af gerðinni *Strengur*. Reiturinn **Gildi** í fyrstu skránni inniheldur textann **"X"**, reiturinn **Gildi** í annarri skránni inniheldur textann **"&nbsp;"**, og reiturinn **Gildi** í þriðju skránni inniheldur textann **"y"**. 

## <a name="example-3"></a>Dæmi 3

Hægt er að nota aðgerðina [INDEX](er-functions-list-index.md) til að fá aðgang að einstaka þáttum tiltekins innsláttarstrengs. Ef slegið er inn gagnaveitunni **MyList** af gerðinni **Reiknaður reitur** og segðin `SPLIT("abc", 1)` er skilgreind fyrir hann, skilar segðin `INDEX(MyList,2).Value` textanum **„b“**.

## <a name="example-4"></a>Dæmi 4

Aðgerðin [ENUMERATE](er-functions-list-enumerate.md) hjálpar einnig til við að fá aðgang að einstaka þáttum tiltekins innsláttarstrengs. Ef gagnaveitan **MyList** er slegin inn fyrst af gerðinni **Reiknaður reitur** og segðin `SPLIT("abc", 1)` er skilgreind fyrir hann og svo er slegið inn gagnaveituna **EnumeratedList** af gerðinni **Reiknaður reitur** og segðin `ENUMERATE(MyList)` er skilgreind fyrir hann, skilar segðin `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` textanum **„b“**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Listaaðgerðir](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
