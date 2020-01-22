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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e3d3ff87a59632d58a7c34ef96f856b38f005651
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915764"
---
# <a name="CONCATENATE">CONCATENATE ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `CONCATENATE` skilar öllum tilgreindum textastrengjum sem *Strengja*-gildi eftir að þeir hafa verið sameinaðir í einn streng.

## <a name="syntax"></a>Málskipun

```
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
