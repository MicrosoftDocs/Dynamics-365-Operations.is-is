---
title: Verkið „Uppfæra innhreyfingarskjöl afurða“ staðfestir óstaðfestar pantanir
description: Eftir að hafa keyrt „Uppfæra innhreyfingarskjöl afurða“ staðfestir kerfið óstaðfestar pantanir sem hafa stöðuna „Skráð“. Frekari upplýsingar um eiginleikann sem lagar þetta vandamál.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 171a978efc6b55b92f429381e72036cb1b3296c6
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/07/2021
ms.locfileid: "7476625"
---
# <a name="unconfirmed-purchase-orders-are-confirmed-after-running-update-product-receipts"></a>Óstaðfestar innkaupapantanir eru staðfestar eftir að uppfærsla innhreyfingarskjala afurða er keyrð

## <a name="symptoms"></a>Einkenni

Þegar búið er að keyra reglubundna verkið *Uppfæra innhreyfingarskjöl afurða* staðfestir kerfið sjálfkrafa óstaðfestar innkaupapantanir sem eru með birgðafærslustöðu *Skráð*.

## <a name="resolution"></a>Lausn

Nýr eiginleiki fyrir meðhöndlun á innleið, *Umframmóttaka á hleðslumagni*, lagar þetta vandamál. Til að kveikja á þessum eiginleika skal fara í [Eiginleikastjórnun](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) vinnusvæðið og kveikja á eftirfarandi eiginleikum í þeirri röð sem þeir eru skráðir:

1. Tengja birgðafærslur innkaupapöntunar við farm
2. Umframmóttaka á hleðslumagni

Frekari upplýsingar er að finna á [Bóka skráð afurðamagn á móti innkaupapöntunum](/dynamics365/supply-chain/warehousing/inbound-load-handling).
