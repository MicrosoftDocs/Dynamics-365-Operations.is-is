---
title: Vara má ekki hafa uppskrift eða formúlu
description: Þegar reynt er að festa pöntun berast villuboð við staðfestingu vöru. Þar kemur fram að varan má ekki vera með uppskrift eða formúlu.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1e946adc3a04db60bf15ac7bb44163085e1c19802872964877d3929b1f79bf7d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730107"
---
# <a name="item-cant-have-a-bom-or-formula"></a>Vara má ekki hafa uppskrift eða formúlu

Villukóði PRO2614

## <a name="symptoms"></a>Einkenni

Þegar reynt er að festa pöntun berast eftirfarandi villuboð við staðfestingu vöru:

> Vara má hvorki hafa uppskrift né formúlu

## <a name="resolution"></a>Lausn

Vörur sem eru með uppskriftir eða formúlu verða að vera af gerðinni *Áætlunarvara*, *Uppskrift* eða *Formúla*. Til að breyta gerð vörunnar skal fylgja þessum skrefum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Viðeigandi vara er opnuð.
1. Í flýtiflipanum **Hönnuður** skal stilla reitinn **Framleiðslugerð** á *Áætlunarvara*, *Uppskrift* eða *Formúlu*.
