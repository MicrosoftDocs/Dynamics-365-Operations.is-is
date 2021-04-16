---
title: ROUNDDOWN ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ROUNDDOWN í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 89fc134ec11a47506211ce68ec3aaf966d9a308b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744464"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]