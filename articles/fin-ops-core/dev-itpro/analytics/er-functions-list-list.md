---
title: LIST ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin LIST í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 6848fe535a6a588eaf06f96e93f28db9ef304940
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917282"
---
# <a name="LIST">LIST ER aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `LIST` skilar *Skráalista*-gildi sem samanstendur af nýjum lista yfir skrár sem er stofnaður úr tilgreindum frumbreytum.

## <a name="syntax"></a>Málskipun

```
LIST (record 1 [, record 2, …, record N])
```

## <a name="arguments"></a>Frumbreytur

`record 1`: *Gámur (skrá)*

Tilvísun í gagnagjafa af gagnagerðinni *Skrá*. Þessi frumbreyta er áskilin.

`record N`: *Gámur (skrá)*

Tilvísun í gagnagjafa af gagnagerðinni *Skrá*. Þessar viðbótarfrumbreytur eru valkvæðar.

## <a name="return-values"></a>Skilagildi

*Skráalisti*

Sá listi yfir skrár sem er búinn til.

## <a name="usage-notes"></a>Notkunarbréf

Skipulag listans sem er stofnað inniheldur aðeins reitina sem eru settir fram í skipulagi hverrar skráar sem nefnd er í frumbreytunum.

## <a name="example"></a>Dæmi

Þú slærð inn gagnagjafann **Skrá 1** af gerðinni *Ílát*. Þessi gagnagjafi inniheldur eftirfarandi ívafna reiti af gerðinni *Reiknaður reitur*:

- **Kóði:** Þessi reitur inniheldur segð sem skilar gildi af gerðinni *Strengur*.
- **Upphæð:** Þessi reitur inniheldur segð sem skilar gildi af gerðinni *Raun*.

Síðan slærðu inn gagnagjafann **Skrá 2** af gerðinni *Ílát*. Þessi gagnagjafi inniheldur eftirfarandi ívafna reiti af gerðinni *Reiknaður reitur*:

- **Upphæð:** Þessi reitur inniheldur segð sem skilar gildi af gerðinni *Raun*.
- **ISValid:** Þessi reitur inniheldur segð sem skilar gildi af gerðinni *Boolean*.

Í þessu tilfelli skilar segðin `LIST('Record 1', 'Record 2')` nýjum lista sem inniheldur tvær skrár. Skipulag listans samanstendur af staka reitnum **Upphæð** af gerðinni *Raun* þar sem þessi reitur er eini reiturinn sem er settur fram í öllum frumbreytum sem kalla aðgerðina.

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)