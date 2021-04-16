---
title: CONCATENATE ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin CONCATENATE í rafrænni skýrslugerð (ER) er notuð
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
ms.openlocfilehash: f1a47a05127412588f4628cb425eab0379493c3c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746483"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]