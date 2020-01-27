---
title: DAYOFYEAR ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin DAYOFYEAR í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 1080a1c2e30cd7ca64ea43120c11eb90d3c99416
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916339"
---
# <a name="DAYOFYEAR">DAYOFYEAR ER aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `DAYOFYEAR` skilar *heiltölu*-gildi sem sýnir fjölda daga milli 1. janúar og tilgreindrar dagsetningar.

## <a name="syntax"></a>Málskipun

```
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a>Frumbreytur

`date`: *Dagsetning*

Dagsetningargildi sem táknar dagsetninguna sem á að nota við útreikning á fjölda daga.

## <a name="return-values"></a>Skilagildi

*Heiltala*

Tölugildið sem verður til.

## <a name="example-1"></a>Dæmi 1

`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` skilar **61**.

## <a name="example-2"></a>Dæmi 2

`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` skilar **1**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar og tímavirkni](er-functions-category-datetime.md)
