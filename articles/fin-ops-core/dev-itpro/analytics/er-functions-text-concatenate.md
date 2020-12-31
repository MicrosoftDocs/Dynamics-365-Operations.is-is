---
title: CONCATENATE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin CONCATENATE í rafrænni skýrslugerð (ER) er notuð
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 903429994ae5618b597aa0ab0991e9f6783a96ed
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687939"
---
# <a name="concatenate-er-function"></a>CONCATENATE ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `CONCATENATE` skilar öllum tilgreindum textastrengjum sem *Strengja*-gildi eftir að þeir hafa verið sameinaðir í einn streng.

## <a name="syntax"></a>Málskipun

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a>Frumbreytur

`text 1`: *Strengur*

Tilvísun í gagnagjafa af gagnagerðinni *Strengur*. Þessi frumbreyta er áskilin.

`text N`: *Strengur*

Tilvísun í gagnagjafa af gagnagerðinni *Strengur*. Þessar viðbótarfrumbreytur eru valkvæðar.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="example"></a>Dæmi

`CONCATENATE ("abc", "def")` skilar **"abcdef"**.

## <a name="usage-notes"></a>Notkunarbréf

Segðin `"abc" & "def"` skilar einnig **abcdef**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textavirkni](er-functions-category-text.md)
