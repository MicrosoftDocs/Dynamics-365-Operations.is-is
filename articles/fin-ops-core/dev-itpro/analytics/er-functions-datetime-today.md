---
title: TODAY ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin TODAY í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 9288baf4e6123a7c03152f524a852eae9b671dde
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567917"
---
# <a name="today-er-function"></a>TODAY ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerð `TODAY` skilar *Date*-gildi sem táknar netþjónsdagsetningu núverandi hugbúnaðar.

## <a name="syntax"></a>Málskipun

```xpp
TODAY ()
```

## <a name="return-values"></a>Skilagildi

*Dagsetning*

Dagsetningargildið sem verður til.

## <a name="example"></a>Dæmi

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` skilar núverandi dagsetningargildi hugbúnaðarþjóns, 24. desember, 2015, sem strenginn **"24-12-2015"**, miðað við tilgreint sérsniðið snið.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar og tímavirkni](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]