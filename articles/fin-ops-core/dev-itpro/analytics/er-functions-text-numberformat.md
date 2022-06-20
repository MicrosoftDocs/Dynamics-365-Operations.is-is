---
title: NUMBERFORMAT ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig NUMBERFORMAT rafræn skýrslugerð (ER) aðgerðin er notuð.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 3e6fa4cbdfb2509418a40980aa29894b5e531bbb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862191"
---
# <a name="numberformat-er-function"></a>NUMBERFORMAT ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `NUMBERFORMAT` skilar *String*-gildi sem setur fram tilgreinda tölu á tilgreindu sniði og í valinni tiltekinni [menningu](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Fyrir upplýsingar um studd snið skal sjá [staðlað](/dotnet/standard/base-types/standard-numeric-format-strings) og [sérsniðna](/dotnet/standard/base-types/custom-numeric-format-strings).

## <a name="syntax-1"></a>Málskipun 1

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>Málskipun 2

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a>Frumbreytur

`number`: *Heiltala* eða *Raun*

Tölugildi sem tilgreinir töluna sem verður að forsníða.

`format`: *Strengur*

Gildið *Strengur* sem táknar sniðmátið.

`culture`: *Strengur*

Gildið *Strengur* sem táknar menninguna sem á að nota til að forsníða.

## <a name="return-values"></a>Skilagildi

*Strengur*

Textagildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Ef menningin er ekki skilgreind sem frumbreyta kallaðrar aðgerðar ákvarðar samhengið sem þessari aðgerð er keyrt í hvaða menning er notuð til að forsníða tölur.

## <a name="example-1"></a>Dæmi 1

Fyrir menninguna **EN-US** skilar `NUMBERFORMAT (0.45, "p")` **"45,00 %"** og `NUMBERFORMAT (10.45, "#")` skilar **"10"**.

## <a name="example-2"></a>Dæmi 2

`NUMBERFORMAT (10/3, "F2", "de")` skilar **3,33** en `NUMBERFORMAT (10/3, "F2", "en-us")` skilar **3,33**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Textavirkni](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]