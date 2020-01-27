---
title: NULLDATETIME ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NULLDATETIME í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 4165f6e064d12200907ac76b6779d35bc578daba
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917489"
---
# <a name="NULLDATETIME">NULLDATETIME ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `NULLDATETIME` skilar *DateTime*-gildi sem táknar **núll** dagsetningar-/tímagildi (1. janúar, 1900) í samræmdum alþjóðlegum tíma (Greenwich-tími \[GMT\]).

## <a name="syntax"></a>Málskipun

```
NULLDATETIME ()
```

## <a name="return-values"></a>Skilagildi

*DateTime*

Dagsetningar-/tímagildið sem verður til.

## <a name="example"></a>Dæmi

`DATETIMEFORMAT( NULLDATETIME(), "O")` skilar strengjagildinu **1900-01-01T00:00:00.0000000+00:00** þegar það er kallað í ferli sem hafið var af notanda forrits sem hefur tímabeltisgildið **(GMT) Samræmdur alþjóðlegur tími** í hlutanum **Kjörstillingar tungumála og lands/svæðis**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar og tímavirkni](er-functions-category-datetime.md)
