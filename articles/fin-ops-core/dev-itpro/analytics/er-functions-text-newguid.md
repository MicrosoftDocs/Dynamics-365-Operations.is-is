---
title: NEWGUID-aðgerð rafrænnar skýrslugerðar
description: Þessi grein veitir upplýsingar um hvernig aðgerðin NEWGUID rafræn skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 321e2eda4accf9c8fe33b5a4c092c7be55276f26
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861817"
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
