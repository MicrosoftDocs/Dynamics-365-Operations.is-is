---
title: POWER ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig POWER rafræn skýrslugerð (ER) aðgerðin er notuð.
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
ms.openlocfilehash: da3ae988b57cb5588de1e2fd8ee962b77b5534ff
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864689"
---
# <a name="power-er-function"></a>POWER ER-aðgerð

[!include [banner](../includes/banner.md)]

Aðgerðin `POWER` skilar *Raun*-gildi sem táknar niðurstöðuna af því að hækka tilgreinda jákvæða tölu upp að tilgreindri valheimild.

## <a name="syntax"></a>Málskipun

```vb
POWER (number, power)
```

## <a name="arguments"></a>Frumbreytur

`number`: *Raun* eða *Heiltala*

Tölugildi sem þarf að hækka í tiltekinn kraft.

`power`: *Raun* eða *Heiltala*

Tölugildi sem táknar tiltekinn kraft.

## <a name="return-values"></a>Skilagildi

*Rauntala*

Tölugildið sem verður til.

## <a name="example-1"></a>Dæmi 1

`POWER (10, 2)` skilar **100**.

## <a name="example-2"></a>Dæmi 2

`POWER (4, 0.5)` skilar **2**.

## <a name="additional-resources"></a>Frekari upplýsingar

[Reikniaðgerðir](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]