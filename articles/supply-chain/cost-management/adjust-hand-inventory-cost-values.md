---
title: Leiðrétta kostnaðarvirði lagerbirgða
description: Hægt er að nota síðuna Leiðrétting á lagermagni til að leiðrétta kostnaðargildi magns lagerbirgða eftir að birgðalokun vinnslu er keyrð.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a702a083d60bdb289712027fbaee5c0a72e60cb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4963839"
---
# <a name="adjust-on-hand-inventory-cost-values"></a>Leiðrétta kostnaðarvirði lagerbirgða

[!include [banner](../includes/banner.md)]

Hægt er að nota síðuna Leiðrétting á lagermagni til að leiðrétta kostnaðargildi magns lagerbirgða eftir að birgðalokun vinnslu er keyrð.

Hægt er að nota **Leiðrétting á lagerbirgðum** síðuna til að leiðrétta kostnaðargildi magns lagerbirgða eftir að birgðalokunarvinnsla er keyrð. **Ábending:** Til að opna síðuna **Leiðrétting á lagerbirgðum** veljið skýrsluna um lokið birgðalokunarferli á síðunni **Lokun og leiðrétting** og smellið síðan á **Leiðrétting** &gt; **Lager**. **Dæmi:** Eftirfarandi færslur eru í febrúar:

-   1. febrúar: Fjárhagsleg innhreyfing birgða með magninu 2 á verðinu USD 10,00.
-   5. febrúar: Fjárhagsleg innhreyfing birgða með magninu 1 á verðinu USD 13,00.
-   19. febrúar: Fjárhagsleg úthreyfing birgða með magninu 1 á meðalkostnaðarverðinu USD 11,00.

Þessi vara var sett upp með birgðalíkaninu Fyrst inn, fyrst út (FIFO), og birgðalokunin var framkvæmd frá og með 28. febrúar. Fjárhagsleg úthreyfingarfærsla upp á 11.00 USD verður jöfnuð við fjárhagslegu innhreyfinguna þann 1. febrúar og gerð verður jöfnun upp á 1,00 USD. Eftirfarandi birgðainnhreyfingar munu þá innihalda opið birgðamagn:

-   1. febrúar: Magnið 1 á verðinu 10.00 USD
-   5. febrúar: Magnið 1 á verðinu 13.00 USD

Ef stilla á kostnað þessara tveggja vara á USD 15.00 skal nota valkostinn um leiðréttingu lagerbirgða til að leiðrétta opna lagerbirgðamagnið frá síðasta birgðalokunartímabili. **Ábending:** Bókunardagsetning lagerbirgðaleiðréttingarfærslunnar verður dagsetning síðustu birgðalokunar. Ekki er hægt að breyta þessari dagsetningu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]