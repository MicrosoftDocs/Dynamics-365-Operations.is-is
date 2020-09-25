---
title: ROUNDDOWN ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ROUNDDOWN í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 7ac559983609d4fdb80c9ac70d84031e4a231889
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744528"
---
# <a name="rounddown-er-function"></a>ROUNDDOWN ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `ROUNDDOWN` skilar tilgreindri tölu sem *Raun*-gildi eftir að hún hefur verið námunduð niður að tilgreindum fjölda aukastafa.

## <a name="syntax"></a>Málskipun

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Frumbreytur

`number`: *Rauntala*

Tölugildi sem verður að vera sléttað niður.

`decimals`: *Heiltala*

Tölugildi sem stendur fyrir fjölda aukastafa.

## <a name="return-values"></a>Skilagildi

*Rauntala*

Tölugildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Þessi aðgerð hegðar sér eins og [ROUND](er-functions-mathematical-round.md), en hún námundar alltaf tilgreindri tölu niður (í átt að núlli).

## <a name="example-1"></a>Dæmi 1

`ROUNDDOWN (1200.767, 2)` sléttar niður um tvo aukastafi og skilar **1200.76**. 

## <a name="example-2"></a>Dæmi 2

`ROUNDDOWN (1700.767, -3)` sléttar niður að næsta margfeldi svæðisins 1.000 og skilar **1000**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Reikniaðgerðir](er-functions-category-mathematical.md)
