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
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294101"
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
