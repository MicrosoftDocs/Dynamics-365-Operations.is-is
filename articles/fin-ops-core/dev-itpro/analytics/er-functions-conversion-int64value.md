---
title: INT64VALUE ER aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin INT64VALUE í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 75df802b75454baeea75a8ceb32d5d045a77a3a0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916546"
---
# <a name="INT64VALUE">INT64VALUE ER aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðerðin `INT64VALUE` skilar *Int64*-gildi sem táknar tilgreindan streng.

## <a name="syntax-1"></a>Málskipun 1

```
INT64VALUE (text)
```

## <a name="syntax-2"></a>Málskipun 2

```
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
