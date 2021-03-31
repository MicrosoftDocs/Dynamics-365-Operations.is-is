---
title: Afgreiða pantanir frá annarri verslun með því að nota eiginleikann Hleðslusending
description: Þetta efnisatriði lýsir Hleðslusending eiginleikanum.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 37ef0234df4ee983c44c183fe884c73b17eb0e06
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5219030"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>Afgreiða pantanir frá annarri verslun með því að nota eiginleikann Hleðslusending

[!include [banner](includes/banner.md)]

Með Hleðslusending eiginleikanum í Commerce getur viðskiptavinarpantanir verið sett í eina verslun og send frá öðrum verslun.

Viðskiptavinapantanir á sölustað (POS) biðlari styðja margskonar uppfyllingarkosti. Nokkur dæmi um valkosti uppfyllingar eru:

- Sækja frá sömu verslun á annan dag.
- Sækja frá annarri verslun á sama degi eða öðrum degi.
- Senda frá sjálfgefna afhendingarvöruhúsinu sem er úthlutað til verslunarinnar, og afhenda á tilteknum degi.

Hleðslusending eiginleikinn notar eftirfarandi POS aðgerðir: Senda allar vörur og Senda valdar vörur. Þetta gerir afgreiðslustarfsmanni kleift að velja „senda frá“ staðsetninguna, þaðan sem hægt er að uppfylla pöntunina eða pöntunarlínuna. „Senda frá“ staðsetningin er að sjálfgefnu afhendingarvöruhús sem tengist versluninni. Hins vegar getur afgreiðslustarfsmaðurinn breytt þessari staðsetningu og valið hvaða verslun sem er skilgreindur í hópnum verslanaleit, sem er úthlutað til verslunarinnar.

Hæfni til að velja „senda til" heimilisföng er óbreytt.

Afhendingaraðferðirnar, sem hægt er að nota til að uppfylla pöntunarlínuna, eru byggðar á grunnstillingum gildra afhendingarmáta fyrir vörur og heimilisföng. Vegna þess að reglunum um gilda afhendingarmáta eru aðeins viðhaldið í bakvinnslu (HQ), framkvæmir POS viðskiptavinurinn rauntímasímtal til að sækja gilda afhendingarmáta fyrir sendingarlínu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]