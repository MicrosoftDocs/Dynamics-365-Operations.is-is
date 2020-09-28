---
title: CN_GBT_ADDITIONALDIMENSIONID ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin CN_GBT_ADDITIONALDIMENSIONID í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 7fdc4527bc6115bdb3fca9d6a92d3d77a7c264c2
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744432"
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
