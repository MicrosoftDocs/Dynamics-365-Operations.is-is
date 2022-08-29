---
title: POWER ER-aðgerð
description: Þessi grein veitir upplýsingar um hvernig POWER rafræn skýrslugerð (ER) aðgerðin er notuð.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 9b6693d7c1afebcf9c30d1bf8d72950053c305bd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273997"
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
