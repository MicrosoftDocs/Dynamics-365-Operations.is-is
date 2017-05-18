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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: a62d8d453be096dda221415437e78c695f3e5cf7
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="adjust-on-hand-inventory-cost-values"></a>Leiðrétta kostnaðarvirði lagerbirgða

[!include[banner](../includes/banner.md)]


Hægt er að nota síðuna Leiðrétting á lagermagni til að leiðrétta kostnaðargildi magns lagerbirgða eftir að birgðalokun vinnslu er keyrð.

Hægt er að nota **Leiðrétting á lagerbirgðum** síðuna til að leiðrétta kostnaðargildi magns lagerbirgða eftir að birgðalokunarvinnsla er keyrð. **Ábending:** til Að opna síðuna **Leiðrétting á lagerbirgðum** veljið skýrsluna um lokið birgðalokunarferli á síðunni **Lokun og leiðrétting** og smellið síðan á **Leiðrétting** &gt; **Lager**. **Dæmi:**Eftirfarandi færslur eru í febrúar:

-   1. febrúar: Fjárhagsleg innhreyfing birgða með magninu 2 á verðinu USD 10,00.
-   5. febrúar: Fjárhagsleg innhreyfing birgða með magninu 1 á verðinu USD 13,00.
-   19. febrúar: Fjárhagsleg úthreyfing birgða með magninu 1 á meðalkostnaðarverðinu USD 11,00.

Þessi vara var sett upp með birgðalíkaninu Fyrst inn, fyrst út (FIFO), og birgðalokunin var framkvæmd frá og með 28. febrúar. Fjárhagsleg úthreyfingarfærsla upp á 11.00 USD verður jöfnuð við fjárhagslegu innhreyfinguna þann 1. febrúar og gerð verður jöfnun upp á 1,00 USD. Eftirfarandi birgðainnhreyfingar munu þá innihalda opið birgðamagn:

-   1. febrúar: Magnið 1 á verðinu 10.00 USD
-   5. febrúar: Magnið 1 á verðinu 13.00 USD

Ef stilla á kostnað þessara tveggja vara á USD 15.00 skal nota valkostinn um leiðréttingu lagerbirgða til að leiðrétta opna lagerbirgðamagnið frá síðasta birgðalokunartímabili. **Ábending:**Bókunardagsetning lagerbirgðaleiðréttingarfærslunnar verður dagsetning síðustu birgðalokunar. Ekki er hægt að breyta þessari dagsetningu.




