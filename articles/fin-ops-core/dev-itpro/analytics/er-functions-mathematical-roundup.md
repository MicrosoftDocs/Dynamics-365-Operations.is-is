---
title: ROUNDUP ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ROUNDUP í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: 0d397a43712b349bc6eb5e88f38dbc7d8a5231a909f38608d45b4e08861b6b7b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743240"
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