---
title: SESSIONNOW ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin SESSIONNOW í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 4dff6daa8fbd60ef1fc84d783e428d69477aac6d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916270"
---
# <a name="">SESSIONNOW ER aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `SESSIONNOW` skilar *DateTime*-gildi sem táknar setudagsetningu og -tíma núverandi hugbúnaðar.

## <a name="syntax"></a>Málskipun

```
SESSIONNOW ()
```

## <a name="return-values"></a>Skilagildi

*DateTime*

Dagsetningar-/tímagildið sem verður til.

## <a name="example"></a>Dæmi

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` skilar núverandi dagsetningar-/tímagildi setu hugbúnaðar, 24. desember 2015, sem **"24.12.2015"**, byggt á valinni þýskri menningu og tilgreindu sniði.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar og tímavirkni](er-functions-category-datetime.md)
