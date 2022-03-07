---
title: CN_GBT_ADDITIONALDIMENSIONID ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin CN_GBT_ADDITIONALDIMENSIONID í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 9217b70076a369c18a94f820f19ca371c2d8aca61ab72b6be762592f39fa1160
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731546"
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