---
title: ROUND ER-aðgerð
description: Í þessari grein er að finna upplýsingar um hvernig ROUND rafræn skýrslugerðarvirkni (ER) er notuð.
author: kfend
ms.date: 10/21/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 57d41ed92a5577fdc5fffeccef2834e9b6fb5197
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286060"
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
