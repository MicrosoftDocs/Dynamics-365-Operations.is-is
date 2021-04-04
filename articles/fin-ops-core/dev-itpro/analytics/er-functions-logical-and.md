---
title: AND ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin AND í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 068b9a3b2cf2e5bffe895bc4e8a7cbb2d8025ad7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560086"
---
# <a name="and-er-function"></a>AND ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `AND` skilar *Boolean*-gildi **TRUE** ef öll tilgreind skilyrði eru sönn. Að öðrum kosti skilar hún *Boolean* gildinu **FALSE**.

## <a name="syntax"></a>Málskipun

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Frumbreytur

`condition 1`: *Boole-gildi*

Gild skilyrt segð sem verður að prófa. Þessi frumbreyta er áskilin.

`condition N`: *Boole-gildi*

Gild skilyrt segð sem verður að prófa. Þessar viðbótarfrumbreytur eru valkvæðar.

## <a name="return-values"></a>Skilagildi

*Boole*

*Boole*-gildið sem myndast.

## <a name="usage-notes"></a>Notkunarbréf

Í röksemdum rökréttra aðgerða er hægt að nota tilvísanir í gagnagjafa, tölu- og textagildi, Boole-gildi, samanburðarrekstraraðila og aðrar rafrænar skýrslur (ER) aðgerðir. Hins vegar verður að meta allar frumbreyturnar við *Boole*-gildið **TRUE** eða **FALSE**.

## <a name="example"></a>Dæmi

`AND (1=1, "a"="a")` skilar **TRUE**.

`AND (1=2, "a"="a")` skilar **FALSE**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Rökvirkni](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]