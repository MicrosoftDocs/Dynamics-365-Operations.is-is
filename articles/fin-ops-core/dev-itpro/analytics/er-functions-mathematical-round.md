---
title: ROUND ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin ROUND í rafrænni skýrslugerð (ER) er notuð.
author: NickSelin
ms.date: 10/21/2020
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
ms.openlocfilehash: b0c28ba2faebf117aa008106f8a77f79af8f4de3122df858825aa15a6dae3616
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744411"
---
# <a name="round-er-function"></a>ROUND ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `ROUND` skilar tilgreindri tölu sem *Raun*-gildi eftir að hún hefur verið námunduð að tilgreindum fjölda aukastafa.

## <a name="syntax"></a>Málskipun

```vb
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

Ef gildi `decimals` frumbreytu er **0** (núll), er tilgreind tala námunduð að næstu heiltölu.

Ef gildi frumbreytunnar `decimals` er lægra en 0 (núll), er tilgreind tala námunduð til vinstri við tugastafinn.

## <a name="example-1"></a>Dæmi 1

`ROUND (1200.767, 2)` sléttar um tvo aukastafi og skilar **1200.77**.

## <a name="example-2"></a>Dæmi 2

`ROUND (1200.767, -3)` sléttar að næsta margfeldi svæðisins 1.000 og skilar **1000**.

## <a name="example-3"></a>Dæmi 3

`ROUND (1200.5, 0)` námundar að næstu heilli tölu og skilar **1200**, á meðan `ROUND (1201.5, 0)` gerir það sama og skilar **1202**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Stærðfræðilegar aðgerðir](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]