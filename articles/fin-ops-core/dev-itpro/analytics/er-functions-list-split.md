---
title: SPLIT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin SPLIT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52a89f744cd37c543294522cc706ae7f47660e75
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070622"
---
# <a name="SPLIT">SPLIT ER-aðgerð</a>

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

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)
