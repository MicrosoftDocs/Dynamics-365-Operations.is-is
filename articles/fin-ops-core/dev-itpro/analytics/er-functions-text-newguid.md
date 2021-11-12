---
title: NEWGUID-aðgerð rafrænnar skýrslugerðar
description: Þetta efnisatriði inniheldur upplýsingar um hvernig NEWGUID-aðgerð rafrænnar skýrslugerðar er notuð.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: 5856a4d765f5136ecb11a34e0255c1ba88818f2c
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647940"
---
# <a name="newguid-er-function"></a>NEWGUID-aðgerð rafrænnar skýrslugerðar

[!include [banner](../includes/banner.md)]

Fallið `NEWGUID` myndar nýtt altækt einkvæmt kennimerki (GUID) og skilar því sem *[GUID-gildi](er-formula-supported-data-types-primitive.md#guid)*.

## <a name="syntax"></a>Málskipun

```vb
NEWGUID ()
```

## <a name="return-values"></a>Skilagildi

*GUID*

GUID-gildið sem myndast.

## <a name="example"></a>Dæmi

`NEWGUID()` skilar alltaf nýju *GUID-gildi* á borð við **3afcf7ff-af10-ec11-b6e6-000d3a13209e**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textaaðgerðir](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
