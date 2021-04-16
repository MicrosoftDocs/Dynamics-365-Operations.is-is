---
title: FIRST ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin FIRST í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
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
ms.openlocfilehash: d30c8481866ccf3f7080197b37586a0460a4ad2c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746580"
---
# <a name="first-er-function"></a>FIRST ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `FIRST` skilar fyrstu skrá yfir tilgreinda listann sem gildinu *Ílát (skrá)*, ef listinn er ekki tómur. Ef listinn er tómur kastar þessi aðgerð frá sér undantekningu.

## <a name="syntax"></a>Málskipun

```vb
FIRST (list)
```

## <a name="arguments"></a>Frumbreytur

`list`: *Skráalisti*

Gild slóð í gagnagjafa af gagnagerðinni *Skráalisti*.

## <a name="return-values"></a>Skilagildi

*Gámur (skrá)*

Skráargildið sem verður til.

## <a name="example-1"></a>Dæmi 1

Segðin `FIRST(SPLIT("ABC",1)).Value` skilar textagildinu **"A"**.

## <a name="example-2"></a>Dæmi 2

Segðin `FIRST(SPLIT("",1)).Value` gerir undantekningu á keyrslutíma.

## <a name="additional-resources"></a>Frekari upplýsingar

[Listavirkni](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]