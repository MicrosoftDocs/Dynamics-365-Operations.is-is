---
title: FIRSTORNULL ER-aðgerð
description: Þetta efni útskýrir hvernig aðgerðin FIRSTORNULL í rafrænni skýrslugerð (ER) er notuð
author: NickSelin
ms.date: 11/29/2019
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
ms.openlocfilehash: 1ccc094fc468470ffc857c729b6d8402796785d7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753217"
---
# <a name="firstornull-er-function"></a>FIRSTORNULL ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerð `FIRSTORNULL` skilar fyrstu skrá yfir tilgreinda listann sem gildinu *Ílát (skrá)*, ef skráin er ekki tóm. Ef skráin er tóm skilar þessi aðgerð núll *Ílát (skrá)* gildi.

## <a name="syntax"></a>Málskipun

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a>Frumbreytur

`list`: *Skráalisti*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.

## <a name="return-values"></a>Skilagildi

*Gámur (skrá)*

Skráargildið sem verður til.

## <a name="example"></a>Dæmi

Segðin `FIRSTORNULL(SPLIT("",1)).Value` skilar tómum streng (**""**).

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]