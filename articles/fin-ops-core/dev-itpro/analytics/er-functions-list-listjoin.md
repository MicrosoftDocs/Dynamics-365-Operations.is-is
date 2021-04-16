---
title: LISTJOIN ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin LISTJOIN í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efee93df7d1cf40d016b36042bb5e7f33c47ae44
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743800"
---
# <a name="listjoin-er-function"></a>LISTJOIN ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `LISTJOIN` skilar *Skráalista*-gildi sem samanstendur af nýjum sameinuðum lista yfir skrár sem er stofnaður úr tilgreindum frumbreytum.

## <a name="syntax"></a>Málskipun

```vb
LIST (list 1 [, list 2, …, list N])
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

![Hönnuðarsíðan ER-líkanavörpun](./media/er-functions-list-listjoin-image1.gif)

Í þessu tilfelli skilar segðin `LISTJOIN(LIST('Record 1'), LIST('Record 2'))` nýjum lista sem inniheldur tvær skrár.

![ER vörpun líkans hönnuður síða með tveimur færslum](./media/er-functions-list-listjoin-image2.gif)

Skipulag listans samanstendur af staka reitnum **Upphæð** af gerðinni `Real` þar sem þessi reitur er eini reiturinn sem er settur fram í öllum frumbreytum sem kalla aðgerðina.

![ER vörpun líkans hönnuður síða reitur upphæðar](./media/er-functions-list-listjoin-image3.gif)

## <a name="additional-resources"></a>Frekari upplýsingar

[Listaaðgerðir](er-functions-category-list.md)

[Kemba gagnagjafa af keyrðu sniði rafrænnar skýrslugerðar til að greina gagnaflæði og umbreytingu](er-debug-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]