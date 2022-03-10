---
title: INTVALUE ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin INTVALUE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 5d54543a6f9878feb3482c1c1e6c1f1f468718489fbc46aded84a5a84bdfb04e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745941"
---
# <a name="intvalue-er-function"></a>INTVALUE ER aðgerð

[!include [banner](../includes/banner.md)]

Aðerðin `INTVALUE` skilar *Int*-gildi sem táknar tilgreindan streng.

## <a name="syntax-1"></a>Málskipun 1

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a>Málskipun 2

```vb
INTVALUE (number)
```

## <a name="arguments"></a>Frumbreytur

`text`: *Strengur*

Textagildi sem þarf umreikna í *Int*-tölu.

`number`: *Raun* eða *Heiltala*

Tölugildið *Rauntala* eða *Heitala* sem þarf umreikna í *Int*-tölu.

## <a name="return-values"></a>Skilagildi

*Int*

Tölugildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Allir aukastafir eru styttir.

## <a name="example-1"></a>Dæmi 1

`INTVALUE ("100.77")` skilar *Int*-gildinu **100**.

## <a name="example-2"></a>Dæmi 2

`INTVALUE (-100.77)` skilar *Int*-gildinu **-100**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Aðgerðir fyrir umbreytingu á gerð](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]