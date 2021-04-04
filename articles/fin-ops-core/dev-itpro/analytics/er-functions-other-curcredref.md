---
title: CURCREDREF ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin CURCREDREF í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: d5f126d71abdc9e3e488b4e8476850dc7763fe5a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567617"
---
# <a name="curcredref-er-function"></a>CURCREDREF ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `CURCREDREF` skilar *Streng*-gildi sem táknar tilvísun kröfuhafa, byggða á tölustöfum tilgreinds reikningsnúmers.

## <a name="syntax"></a>Málskipun

```vb
CURCREDREF (invoice number digits)
```

## <a name="arguments"></a>Frumbreytur

`invoice number digits`: *Strengur*

Textagildi sem stendur fyrir tölustafi reikningsnúmers.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="example"></a>Dæmi

`CURCredRef ("VEND-200002")` skilar **"2200002"**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Other (lénsértæk virkni fyrir viðskipti)](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]