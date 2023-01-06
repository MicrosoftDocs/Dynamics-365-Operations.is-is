---
title: NEWGUID-aðgerð rafrænnar skýrslugerðar
description: Í þessari grein er að finna upplýsingar um hvernig NEWGUID rafræn skýrslugerðarvirkni (ER) er notuð.
author: kfend
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 381dbcbe816c189c1966ffe962020d5aa2b1f3eb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274773"
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
