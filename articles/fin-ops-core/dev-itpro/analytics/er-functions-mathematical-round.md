---
title: ROUND ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ROUND í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: c9384d5975e4a25d18ff741f87431daa4b0bbd7e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917075"
---
# <a name="ROUND">ROUND ER-aðgerð</a>

[!include [banner](../includes/banner.md)]

Aðgerðin `ROUND` skilar tilgreindri tölu sem *Raun*-gildi eftir að hún hefur verið námunduð að tilgreindum fjölda aukastafa.

## <a name="syntax"></a>Málskipun

```
ROUND (number, decimals)
```

## <a name="arguments"></a>Frumbreytur

`number`: *Rauntala*

Tölugildi sem verður að vera sléttað.

`decimals`: *Heiltala*

Tölugildi sem stendur fyrir fjölda aukastafa.

## <a name="return-values"></a>Skilagildi

*Rauntala*

Tölugildið sem verður til.

## <a name="usage-notes"></a>Notkunarbréf

Ef gildi frumbreytunnar `decimals` er hærra en 0 (núll), er tilgreind tala námunduð að þetta mörgum aukastöfum.

Ef gildi frumbreytunnar `decimals` er **0** (núll), er tilgreind tala námunduð að næstu heiltölu.

Ef gildi frumbreytunnar `decimals` er lægra en 0 (núll), er tilgreind tala námunduð til vinstri við tugastafinn.

## <a name="example-1"></a>Dæmi 1

`ROUND (1200.767, 2)` sléttar um tvo aukastafi og skilar **1200.77**.

## <a name="example-2"></a>Dæmi 2

`ROUND (1200.767, -3)` sléttar að næsta margfeldi svæðisins 1.000 og skilar **1000**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Reikniaðgerðir](er-functions-category-mathematical.md)
