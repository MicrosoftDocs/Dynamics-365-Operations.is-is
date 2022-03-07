---
title: FIRST ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin FIRST í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: f108676c2ff8801fddc0a72be3f75d212582efe6b5d96f7515354739eb446532
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6740991"
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