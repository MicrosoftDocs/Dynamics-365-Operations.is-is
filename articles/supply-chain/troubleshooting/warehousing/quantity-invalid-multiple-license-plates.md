---
title: Magn er ekki gilt fyrir tiltektarvinnu með mörgum númeraplötum
description: Þegar til er tiltektarvinna með mörgum númeraplötum á einni staðsetningu er magnið ekki gilt fyrir einingu ea. Staðfestu að eftirfarandi reitir séu réttir.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5b245f71e80339fee3e42cfffa0396078a56926e
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476619"
---
# <a name="quantity-not-valid-when-theres-picking-work-with-multiple-lps-in-one-location"></a>Magn er ekki gilt þegar til er tiltektarvinna með margar númeraplötur á einni staðsetningu

## <a name="symptoms"></a>Einkenni

Þegar til er tiltektarvinna með mörgum númeraplötum á einni staðsetningu er magnið ekki gilt fyrir einingu *ea* og þú færð eftirfarandi villuboð:

> Magnið er ekki gilt fyrir einingu 1%.

## <a name="resolution"></a>Lausn

Gangið úr skugga um að **Auðkenni röðunarflokks einingar** og **Einingaumreikningar** reitir á útgefnu afurðina eða afurðarafbrigðið séu rétt stillt.

Athugið að villuboðin hafa verið endurbætt í útgáfu 10.0.15 til að sýna vænt magn (sjá [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Nýju villuboðin eru:

> Magnið er ekki gilt. Væntanlegt %1 %2.
