---
title: OR ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin OR í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 81a596f5206b23001feea553adcdf6c904572775
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917121"
---
# <a name="OR">OR ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `OR` skilar *Boolean*-gildinu **FALSE** ef öll tilgreind skilyrði eru ósönn. Ef eitthvert tilgreint skilyrði er satt skilar aðgerðin *Boolean*-gildinu **TRUE** ef öll tilgreind skilyrði eru sönn.

## <a name="syntax"></a>Málskipun

```
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Frumbreytur

`condition 1`: *Boole-gildi*

Gild skilyrt segð sem verður að prófa. Þessi frumbreyta er áskilin.

`condition N`: *Boole-gildi*

Gild skilyrt segð sem verður að prófa. Þessar viðbótarfrumbreytur eru valkvæðar.

## <a name="return-values"></a>Skilagildi

*Boole*

*Boole*-gildið sem myndast.

## <a name="example"></a>Dæmi

`OR (1=2, "a"="a")` skilar **TRUE**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Rökvirkni](er-functions-category-logical.md)
