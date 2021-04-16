---
title: NUMBERFORMAT ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin NUMBERFORMAT í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 8de57d8b0a45b8b58849a24f2d8f0cde41e0ea3a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746216"
---
# <a name="numberformat-er-function"></a>NUMBERFORMAT ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `NUMBERFORMAT` skilar *String*-gildi sem setur fram tilgreinda tölu á tilgreindu sniði og í valinni tiltekinni [menningu](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Fyrir upplýsingar um studd snið skal sjá [staðlað](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) og [sérsniðna](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).

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