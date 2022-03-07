---
title: Ekki er hægt að taka frá vöru RM þegar framleiðslupöntun er gefin út
description: 'Þegar framleiðslupöntun er gefin út gætir þú fengið villuna: „Ekki var hægt að taka að fullu frá vöru RM“. Gakktu úr skugga um að allt magn sé í boði eða taktu frá vörur handvirkt.'
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 528895252d661bb012f49190c15853989833064d
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476687"
---
# <a name="item-rm-cant-be-fully-reserved-when-a-production-order-is-released"></a>Ekki er hægt að taka vöru RM frá að fullu þegar framleiðslupöntun er gefin út

## <a name="symptoms"></a>Einkenni

Ef það eru ekki allar vörulínur uppskriftar efnislega til staðar þegar framleiðslupöntun er losuð í vöruhús og stefnan **Losa í vöruhús** er stillt á *Fullrar frátekningar er krafist* birtast eftirfarandi villuboð:

> Ekki var hægt að taka vöru RM frá að fullu. Tryggið að fullt magn sé tiltækt eða takið vöruna frá handvirkt ef reiturinn Frátekning á uppskriftarlínunni er stilltur á Handvirkt eða Byrjað. Ekki var hægt að losa pöntunina í vöruhús því að ekki tókst að taka einhver hráefni frá.

## <a name="resolution"></a>Lausn

Þessi hegðun er samkvæmt hönnuninni og virkar eins og búist var við. Til að laga þetta vandamál skal fylgja leiðsögninni sem gefin er upp í villuboðinu: „Tryggið að fullt magn sé tiltækt eða takið vöruna frá handvirkt ef reiturinn Frátekning á uppskriftarlínunni er stilltur á Handvirkt eða Byrjað.“
