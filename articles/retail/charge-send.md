---
title: "Senda pöntun frá annarri verslun"
description: "Þetta efnisatriði lýsir Hleðslusending eiginleikanum."
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Core, Retail
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 986ec7835dac52c326085c47313205d08b1bafa8
ms.openlocfilehash: d217bc31ad9d93c5440e5329f7b7327d089137f4
ms.contentlocale: is-is
ms.lasthandoff: 10/10/2017

---

# <a name="ship-an-order-from-a-different-store"></a>Senda pöntun frá annarri verslun

Með Hleðslusending eiginleikanum í Dynamics 365 for Retail getur viðskiptavinarpantanir verið sett í eina verslun og send frá öðrum verslun. Viðskiptavinapantanir á sölustað (POS) biðlari styðja margskonar uppfyllingarkosti. Nokkur dæmi um valkosti uppfyllingar eru:
-   Sækja frá sömu verslun á annan dag.
-   Sækja frá annarri verslun á sama degi eða öðrum degi.
-   Senda frá sjálfgefna afhendingarvöruhúsinu sem er úthlutað til verslunarinnar, og afhenda á tilteknum degi.

Hleðslusending eiginleikinn notar eftirfarandi POS aðgerðir: Senda allar vörur og Senda valdar vörur. Þetta gerir afgreiðslustarfsmanni kleift að velja „senda frá“ staðsetninguna, þaðan sem hægt er að uppfylla pöntunina eða pöntunarlínuna. „Senda frá“ staðsetningin er að sjálfgefnu afhendingarvöruhús sem tengist versluninni. Hins vegar getur afgreiðslustarfsmaðurinn breytt þessari staðsetningu og valið hvaða verslun sem er skilgreindur í hópnum verslanaleit, sem er úthlutað til verslunarinnar. 

Hæfni til að velja „senda til" heimilisföng er óbreytt. 

Afhendingaraðferðirnar, sem hægt er að nota til að uppfylla pöntunarlínuna, eru byggðar á grunnstillingum gildra afhendingarmáta fyrir vörur og heimilisföng. Vegna þess að reglunum um gilda afhendingarmáta eru aðeins viðhaldið í Retail Headquarters (HQ), framkvæmir POS viðskiptavinurinn rauntímasímtal til að sækja gilda afhendingarmáta fyrir sendingarlínu. 


