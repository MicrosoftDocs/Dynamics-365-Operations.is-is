---
title: INT64VALUE ER aðgerð
description: Þessi grein veitir upplýsingar um hvernig INT64VALUE rafræn skýrslugerð (ER) aðgerðin er notuð.
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
ms.openlocfilehash: 37fae9cdc5a833009b0ca1cbeb851e5e6e1b6608
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892165"
---
# <a name="int64value-er-function"></a>INT64VALUE ER aðgerð

[!include [banner](../includes/banner.md)]

Aðerðin `INT64VALUE` skilar *Int64*-gildi sem táknar tilgreindan streng.

## <a name="syntax-1"></a>Málskipun 1

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a>Málskipun 2

```vb
INT64VALUE (number)
```

## <a name="arguments"></a>Frumbreytur

`text`: *Strengur*

Textagildi sem þarf umreikna í *Int64*-tölu.

`number`: *Raun* eða *Heiltala*

Tölugildið *Rauntala* eða *Heitala* sem þarf umreikna í *Int64*-tölu.

## <a name="return-values"></a>Skilagildi

*Int64*

Tölugildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Allir aukastafir eru styttir.

## <a name="example-1"></a>Dæmi 1

`INT64VALUE ("22565422744")` skilar *Int64*-gildinu **-22565422744**.

## <a name="example-2"></a>Dæmi 2

`INT64VALUE ( VALUE("22565422744.77"))` skilar *Int64*-gildinu **-22565422744**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Aðgerðir fyrir umbreytingu á gerð](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]