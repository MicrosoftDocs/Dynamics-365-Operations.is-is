---
title: ROUNDUP ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig aðgerðin ROUNDUP rafræn skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: ec4fdce6f072c5c3d87b139c8f64bd63a8a3eccd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855646"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]