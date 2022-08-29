---
title: OR ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig OR rafræn skýrslugerð (ER) aðgerðin er notuð.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 99b5ee37af1ea1a69985fb79b762b31561334fd6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268087"
---
# <a name="or-er-function"></a>OR ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `OR` skilar *Boolean*-gildinu **FALSE** ef öll tilgreind skilyrði eru ósönn. Ef eitthvert tilgreint skilyrði er satt skilar aðgerðin *Boolean*-gildinu **TRUE** ef öll tilgreind skilyrði eru sönn.

## <a name="syntax"></a>Málskipun

```vb
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
