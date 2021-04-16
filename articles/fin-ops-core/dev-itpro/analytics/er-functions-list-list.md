---
title: LIST ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin LIST í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
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
ms.openlocfilehash: 50cb8858301c030df07ad4af9fe2a9513f41fead
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750413"
---
# <a name="list-er-function"></a>LIST ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `LIST` skilar *Skráalista*-gildi sem samanstendur af nýjum lista yfir skrár sem er stofnaður úr tilgreindum frumbreytum.

## <a name="syntax"></a>Málskipun

```vb
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]