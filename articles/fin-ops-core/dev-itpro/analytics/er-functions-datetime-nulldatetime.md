---
title: NULLDATETIME ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NULLDATETIME í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: f7282b7c161b6e183186ba81e6bcf7b34ce6e612
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746820"
---
# <a name="nulldatetime-er-function"></a>NULLDATETIME ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `NULLDATETIME` skilar *DateTime*-gildi sem táknar **núll** dagsetningar-/tímagildi (1. janúar, 1900) í samræmdum alþjóðlegum tíma (Greenwich-tími \[GMT\]).

## <a name="syntax"></a>Málskipun

```vb
NULLDATETIME ()
```

## <a name="return-values"></a>Skilagildi

*DateTime*

Dagsetningar-/tímagildið sem verður til.

## <a name="example"></a>Dæmi

`DATETIMEFORMAT( NULLDATETIME(), "O")` skilar strengjagildinu **1900-01-01T00:00:00.0000000+00:00** þegar það er kallað í ferli sem hafið var af notanda forrits sem hefur tímabeltisgildið **(GMT) Samræmdur alþjóðlegur tími** í hlutanum **Kjörstillingar tungumála og lands/svæðis**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Dagsetningar og tímavirkni](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]