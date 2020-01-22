---
title: NOT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NOT í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: b15277dba26dc7864193b11a127944daca6b989f
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916040"
---
# <a name="NOT">NOT ER aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `NOT` skilar bakfærðu röklegu gildi tilgreinds skilyrðis sem *Boolean*-gildi.

## <a name="syntax"></a>Málskipun

```
NOT (condition)
```

## <a name="arguments"></a>Frumbreytur

`condition`: *Boole-gildi*

Gild skilyrt segð sem verður að snúa við.

## <a name="return-values"></a>Skilagildi

*Boole*

*Boole*-gildið sem myndast.

## <a name="example"></a>Dæmi

`NOT (TRUE)` skilar **FALSE**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Rökvirkni](er-functions-category-logical.md)
