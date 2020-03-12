---
title: NUMBERVALUE ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NUMBERVALUE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 6eeb66f4206eb39141a5b2573fcb9d15428ae52a
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042657"
---
# <a name="NUMBERVALUE">NUMBERVALUE ER aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `NUMBERVALUE` skilar *Raun*-gildi sem er umreiknað úr tilgreindu *Streng*-gildi. Við umreikning er tekið tillit til tilgreindra flokkunarskiltákna aukastafa og tölustafa.

## <a name="syntax"></a>Málskipun

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a>Frumbreytur

`text`: *Strengur*

Textagildi sem þarf umreikna í *Raun*-tölu.

`decimal separator`: Strengur

Skiltákn fyrir aukastaf. Það er notað til að aðgreina heiltölur og aukastafi brota.

`digit grouping separator`: *Strengur*

Flokkunarskiltákn fyrir tölustafi. Það er notað sem þúsundaskiltákn.

## <a name="return-values"></a>Skilagildi

*Rauntala*

Tölugildið sem verður til.

## <a name="example"></a>Dæmi

`NUMBERVALUE( "1 234,56", ",", " ")` skilar **1234,56**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Aðgerðir fyrir umbreytingu á gerð](er-functions-category-type-conversion.md)
