---
title: ABS ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ABS í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 9b32c5e8a413be3583177f565e2d4909330ad1e0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917098"
---
# <a name="ABS">ABS ER aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `ABS` skilar algeru gildi (leifastofn) tiltekins fjölda sem *Raun*-gildi. Með öðrum orðum skilar hún tölunni án táknsins.

## <a name="syntax"></a>Málskipun

```
ABS (number)
```

## <a name="arguments"></a>Frumbreytur

`number`: *Rauntala*

Tölugildi sem þú vilt fá stuðullinn á.

## <a name="return-values"></a>Skilagildi

*Rauntala*

Tölugildið sem verður til.

## <a name="example"></a>Dæmi

`ABS (-1)` skilar **1**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Reikniaðgerðir](er-functions-category-mathematical.md)
