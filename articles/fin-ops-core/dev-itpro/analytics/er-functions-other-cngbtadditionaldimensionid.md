---
title: CN_GBT_ADDITIONALDIMENSIONID ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig CN_GBT_ADDITIONALDIMENSIONID rafræn skýrslugerð (ER) aðgerðin er notuð.
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
ms.openlocfilehash: 0ed2593f865a4764b1c6172722d701a0a10ba5f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281753"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a>CN_GBT_ADDITIONALDIMENSIONID ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `CN_GBT_ADDITIONALDIMENSIONID` skilar *Streng*-gildi sem táknar stakt fjárhagsvíddarkenni sem er tekið úr tilgreindum streng. Tilgreindur strengur sýnir allar víddir sem kommuaðskilinn lista yfir kenni.

## <a name="syntax"></a>Málskipun

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a>Frumbreytur

`text`: *Strengur*

*Strengjagildi* sem sýnir allar víddir sem kommuaðskilinn lista yfir kenni.

`number`: Heiltala

Gildi *heiltölu* skilgreinir kóða númeraraðar af umbeðinni vídd í tilgreindum streng.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="example"></a>Dæmi

`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` skilar **"CC"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Other (lénsértæk virkni fyrir viðskipti)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
