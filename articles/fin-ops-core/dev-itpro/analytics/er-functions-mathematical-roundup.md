---
title: ROUNDUP ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ROUNDUP í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 83262a11f92a924e5e49461cf414fb07ab278541
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744504"
---
# <a name="roundup-er-function"></a>ROUNDUP ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `ROUNDUP` skilar tilgreindri tölu sem *Raun*-gildi eftir að hún hefur verið námunduð upp að tilgreindum fjölda aukastafa.

## <a name="syntax"></a>Málskipun

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Frumbreytur

`number`: *Rauntala*

Tölugildi sem verður að vera sléttað upp.

`decimals`: *Heiltala*

Tölugildi sem stendur fyrir fjölda aukastafa.

## <a name="return-values"></a>Skilagildi

*Rauntala*

Tölugildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Þessi aðgerð hegðar sér eins og [ROUND](er-functions-mathematical-round.md), en hún námundar tilgreindri tölu upp (í átt frá núlli).

## <a name="example-1"></a>Dæmi 1

`ROUNDUP (1200.763, 2)` sléttar upp um tvo aukastafi og skilar **1200.77**.

## <a name="example-2"></a>Dæmi 2

`ROUNDUP (1200.767, -3)` sléttar upp að næsta margfeldi svæðisins 1.000 og skilar **2000**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Reikniaðgerðir](er-functions-category-mathematical.md)
