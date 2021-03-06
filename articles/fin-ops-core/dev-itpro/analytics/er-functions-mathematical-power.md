---
title: POWER ER-aðgerð
description: Þetta efni inniheldur upplýsingar um hvernig aðgerðin POWER í rafrænni skýrslugerð (ER) er notuð.
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
ms.openlocfilehash: ce1f4c735f815c46003ded35156bb47febf177a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750157"
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