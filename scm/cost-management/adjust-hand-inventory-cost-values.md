---
title: "Leiðrétta kostnaðarvirði lagerbirgða"
description: "Hægt er að nota síðuna Leiðrétting á lagermagni til að leiðrétta kostnaðargildi magns lagerbirgða eftir að birgðalokun vinnslu er keyrð."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d1ef775c9783b975fd0f852dc7112506d3897605
ms.lasthandoff: 03/31/2017


---

# <a name="adjust-on-hand-inventory-cost-values"></a>Leiðrétta kostnaðarvirði lagerbirgða

Hægt er að nota síðuna Leiðrétting á lagermagni til að leiðrétta kostnaðargildi magns lagerbirgða eftir að birgðalokun vinnslu er keyrð.

Hægt er að nota **Leiðrétting á lagerbirgðum** síðuna til að leiðrétta kostnaðargildi magns lagerbirgða eftir að birgðalokunarvinnsla er keyrð. **Athugasemd:** til Að opna í **Leiðrétting á lagermagni** á síðunni á **Lokun og leiðrétting** síðunni velja lokið birgðalokunarferli og smellið síðan á **Leiðrétting**&gt;**á lager**. **Dæmi:**Eftirfarandi færslur eru í febrúar:

-   1. febrúar: Fjárhagsleg innhreyfing birgða með magninu 2 á verðinu USD 10,00.
-   5. febrúar: Fjárhagsleg innhreyfing birgða með magninu 1 á verðinu USD 13,00.
-   19. febrúar: Fjárhagsleg úthreyfing birgða með magninu 1 á meðalkostnaðarverðinu USD 11,00.

Þessi vara var sett upp með fyrsta inn, fyrst út (FIFO) birgðalíkaninu og birgðalokun var framkvæmd frá og með 28. Febrúar. Fjárhagsleg úthreyfingarfærsla upp á USD 11.00 verða jafnaðar á móti fjárhagslega innhreyfingu sem er dagsett 1. Febrúar og leiðrétting USD 1.00 er gerð. Eftirfarandi birgðainnhreyfingar munu þá innihalda opið birgðamagn:

-   1. febrúar: Magnið 1 á verðinu 10.00 USD
-   5. febrúar: Magnið 1 á verðinu 13.00 USD

Ef stilla á kostnað þessara tveggja vara á USD 15.00 skal nota valkostinn um leiðréttingu lagerbirgða til að leiðrétta opna lagerbirgðamagnið frá síðasta birgðalokunartímabili. **Ábending:**Bókunardagsetning lagerbirgðaleiðréttingarfærslunnar verður dagsetning síðustu birgðalokunar. Ekki er hægt að breyta þessari dagsetningu.


