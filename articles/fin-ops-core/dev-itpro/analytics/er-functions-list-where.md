---
title: WHERE ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig WHERE rafræn skýrslugerð (ER) aðgerðin er notuð.
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
ms.openlocfilehash: b3f8b01bffd0c530e5095531fc184c960744e751
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273159"
---
# <a name="where-er-function"></a>WHERE ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `WHERE` skilar tilgreindum lista sem *Skráalista*-gildi eftir að það hefur verið síað í samræmi við tilgreind skilyrði.

## <a name="syntax"></a>Málskipun

```vb
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
