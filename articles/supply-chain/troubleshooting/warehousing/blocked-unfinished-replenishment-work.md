---
title: Lokað fyrir tiltektarvinnu vegna ólokinnar áfyllingarvinnu
description: Tiltektarvinna er hugsanlega lokuð vegna háðrar áfyllingarvinnu. Ljúka skal áfyllingarvinnu og vinna síðan tiltektarverk.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 53b50d1e3e2d7bb64e78514affe80076ddcb9052
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476706"
---
# <a name="picking-work-cant-be-unblocked-because-of-unfinished-replenishment-work"></a>Ekki er hægt að opna fyrir tiltektarvinnu vegna ólokinnar áfyllingarvinnu

## <a name="symptoms"></a>Einkenni

Þegar eftirspurnaráfylling bylgju er notuð er hægt að loka fyrir tiltektarvinnu vegna háðrar áfyllingarvinnu. Ef fylla verður á tiltektarstaðsetningu til að uppfylla eftirspurn upprunapöntunar, stofnar kerfið bæði áfyllingarvinnu og tiltektarvinnu. Hins vegar lokar það tiltektarvinnu þar til áfyllingarvinnu er lokið og þú færð eftirfarandi villuboð:

> Ekki er hægt að opna fyrir vinnu %1 vegna þess að hún inniheldur ólokna áfyllingarvinnu.

## <a name="resolution"></a>Lausn

Þessi hegðun er innbyggð, vegna þess að tiltektarstaðsetningin mun ekki innihalda nægar birgðir nema áfyllingarvinnu sé lokið. Ljúka skal áfyllingarvinnu og vinna síðan tiltektarverk.
