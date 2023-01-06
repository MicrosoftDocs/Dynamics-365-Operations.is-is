---
title: LISTJOIN ER-aðgerð
description: Í þessari grein er að finna upplýsingar um hvernig LISTJOIN rafræn skýrslugerðarvirkni (ER) er notuð.
author: kfend
ms.date: 04/01/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: ec8a5985277de8036ec8ad51b947a8bab098a1c3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291205"
---
# <a name="listjoin-er-function"></a>LISTJOIN ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `LISTJOIN` skilar *Skráalista*-gildi sem samanstendur af nýjum sameinuðum lista yfir skrár sem er stofnaður úr tilgreindum frumbreytum.

## <a name="syntax"></a>Málskipun

```vb
LISTJOIN (list 1 [, list 2, …, list N])
```

## <a name="arguments"></a>Frumbreytur

`list 1`: *Skráalisti*

Tilvísun í gagnagjafa af gagnagerðinni *Skráalisti*. Þessi frumbreyta er skylda.

`list N`: *Skráalisti*

Tilvísun í gagnagjafa af gagnagerðinni *Skráalisti*. Þessar viðbótarfrumbreytur eru valkvæðar.

## <a name="return-values"></a>Skilagildi

*Skráalisti*

Sá listi yfir skrár sem er búinn til.

## <a name="usage-notes"></a>Notkunarbréf

Skipulag listans sem er stofnað inniheldur aðeins reitina sem eru settir fram í skipulagi hvers skráalista sem vísað er til í frumbreytunum.

## <a name="example"></a>Dæmi

Þú slærð inn gagnagjafann **Skrá 1** af gerðinni `Container`. Þessi gagnagjafi inniheldur eftirfarandi ívafna reiti af gerðinni `Calculated field`:

- **Kóði**: Þessi reitur inniheldur segð sem skilar gildi af gerðinni `String`.
- **Upphæð**: Þessi reitur inniheldur segð sem skilar gildi af gerðinni `Real`.

Síðan slærðu inn gagnagjafann **Skrá 2** af gerðinni `Container`. Þessi gagnagjafi inniheldur eftirfarandi ívafna reiti af gerðinni `Calculated field`:

- **Upphæð**: Þessi reitur inniheldur segð sem skilar gildi af gerðinni `Real`.
- **IsValid**: Þessi reitur inniheldur segð sem skilar gildi af gerðinni `Boolean`.

![Hönnuðarsíða ER-líkanavörpunar.](./media/er-functions-list-listjoin-image1.gif)

Í þessu tilfelli skilar segðin `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` nýjum lista sem inniheldur tvær skrár.

![Hönnuðarsíða ER-líkanavörpunar með tveimur færslum.](./media/er-functions-list-listjoin-image2.gif)

Skipulag listans samanstendur af staka reitnum **Upphæð** af gerðinni `Real` þar sem þessi reitur er eini reiturinn sem er settur fram í öllum frumbreytum sem kalla aðgerðina.

![Reit upphæðar á hönnuðarsíðu líkanavörpunar rafrænnar skýrslugerðar.](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>Frekari upplýsingar

[Listaaðgerðir](er-functions-category-list.md)

[Kemba gagnagjafa af keyrðu sniði rafrænnar skýrslugerðar til að greina gagnaflæði og umbreytingu](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
