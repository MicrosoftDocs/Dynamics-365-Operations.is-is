---
title: NUMBERFORMAT ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig NUMBERFORMAT rafræn skýrslugerð (ER) aðgerðin er notuð.
author: kfend
ms.date: 12/10/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 5519f549c10ba5c02e249592d040582c3f8dc44f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274796"
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
