---
title: WHERE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin WHERE í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 50d90697f522f3c4d7b62190928008b6d923ffc6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916086"
---
# <a name="WHERE">WHERE ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `WHERE` skilar tilgreindum lista sem *Skráalista*-gildi eftir að það hefur verið síað í samræmi við tilgreind skilyrði.

## <a name="syntax"></a>Málskipun

```
WHERE (list, condition)
```

## <a name="arguments"></a>Frumbreytur

`list`: *Skráalisti*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.

`condition`: *Boole-gildi*

Gild skilyrt tjáning sem er notuð til að sía skrár yfir tiltekinn lista.

## <a name="return-values"></a>Skilagildi

*Skráalisti*

Sá listi yfir skrár sem er búinn til.

## <a name="usage-notes"></a>Notkunarbréf

Þessi aðgerð er frábrugðin [FILTER](er-functions-list-filter.md) aðgerðinni, vegna þess að tilgreint skilyrði er beitt á hvaða gagnagjafa rafrænnar skýrslugerðar (ER) af gerðinni *Skráalisti* sem er til staðar í minninu.

Ef frumbreyturnar sem eru stilltar fyrir þessa aðgerð (`list` og `condition`) leyfa að þýða þessa beiðni yfir í beint SQL-kall eru send viðvörunarboð á hönnunartíma. Þessi skilaboð upplýsa notandann um að árangur gæti verið betri ef aðgerðin [FILTER](er-functions-list-filter.md) er notuð í staðinn fyrir `WHERE`.

## <a name="example-1"></a>Dæmi 1

Ef **Lánardrottinn** er stilltur sem ER-gagnagjafi sem vísar til VendTable-töflunnar skilar segðin `WHERE (Vendors, Vendors.VendGroup = "40")` lista yfir aðeins lánardrottna sem tilheyra lánardrottnaflokki 40.

## <a name="example-2"></a>Dæmi 2

Ef þú slærð inn gagnagjafann **DS** af gerðinni *Reiknaður reitur* og hann inniheldur segðina `SPLIT ("A|B|C", "|")` skilar segðin `WHERE( DS, DS.Value = "B")` lista yfir aðeins eina skrá sem inniheldur textann **"B"** í reitnum **Gildi**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)
