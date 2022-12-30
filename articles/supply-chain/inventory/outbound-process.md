---
title: Yfirlit útleiðarferlis
description: Þessi grein veitir yfirsýn yfir útleiðarferli í birgðastjórnun.
author: yufeihuang
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "274363"
- intro-internal
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 4e3c97862858e219d98b4ef9a81b52c6ab1623ab
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852477"
---
# <a name="outbound-process-overview"></a>Yfirlit útleiðarferlis

[!include [banner](../includes/banner.md)]

Þessi grein veitir yfirsýn yfir útleiðarferli í birgðastjórnun.

## <a name="output-orders"></a>Úttakspantanir

Úttakspantanir eru notaðir til að tengja sölulínur og flytja pöntunarlínur með útleiðarferli sem notast við tiltektarlista.

Þegar tiltektarlistar eru myndaðar úr annaðhvort sölupöntun eða flutningsfyrirmæli eru úttakspantanir og sendingar sjálfkrafa búnar til. Tiltektarlisti er í einkvæmum tengslum við sendingu. Millifærslupöntun er hægt að búa til þaðan sem millifært er frá eða þaðan sem millifært er til. 

Eftirfarandi skýringarmynd sýnir yfirlit yfir útleiðarferli pantana: 

[![Yfirlit yfir útleiðarferli pantana.](./media/outbound-order.png)](./media/outbound-order.png)

Hægt er að setja upp útleiðarreglur til að ákvarða hvernig forritið á að vinna útleiðarferlið. Þessar reglur má nota til að stýra sendingarferlinu. Sérstaklega er hægt að nota reglurnar til að stjórna á hvaða stigi er hægt að senda sendingu á meðan ferli stendur yfir. Eftirfarandi stillingar skilgreina hvernig útleiðarferli er stjórnað.

## <a name="picking-route-status-for-sales-and-transfer-orders"></a>Staða tiltektarleiðar fyrir sölu- og flutningspantanir 

Farðu í **Viðskiptakröfur** \> **Uppsetning** \> **Færibreytur viðskiptakrafna** og veldu svo, í flipanum **Uppfærslur** gildi í svæðinu **Staða tiltektarleiðar** .

[![Staða tiltektarleiðar fyrir sölupantanir.](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)

Ef stillingarreiturinn **Staða tiltektarleiðar** er stillt á **Lokið** fer tiltektarferlið sjálfkrafa af stað sem sem hluti af því að búa til tiltektarlista. Ef reitur er stilltur á **Kveikt**, þarf að uppfæra tiltektarlistalínurnar handvirkt.

Sama á við um flutningspantanir. Farðu í **Birgðastjórnun** \> **Uppsetning** \> **Færibreytur birgða- og vöruhúsakerfis** og veldu svo, í flipanum **Flutningur** gildi í svæðinu **Staða tiltektarleiðar** .

[![Staða tiltektarleiðar fyrir flutningspantanir.](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)

## <a name="end-output-inventory-orders"></a>Ljúka birgðapöntun

Farðu í **Birgðastjórnun** \> **Uppsetning** \> **Færibreytur birgða- og vöruhúsakerfis** og veldu svo, í flipanum **Almennt**, valkostinn **Ljúka úttaksbirgðapöntun** .

[![Ljúka úttaksbirgðapöntun.](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)

Þegar starfsmaður vöruhúss minnkar magn á tiltektarlista, þá verður samsvarandi magn birgðapantana fjarlægt úr sendingu. Þegar tiltektarlistinn er uppfærður á einhverjum tímapunkti, verða eftirstandandi magn tilkynnt aftur á pöntunarstig ef valkosturinn **Ljúka úttaksbirgðapöntun** er stillt á **Já**. Ef valkosturinn **Ljúka úttaksbirgðapöntun** er stilltur á **Nei**, er eftirstandandi magn geymt sem opið úttakspöntunarmagn og verður að vera bætt við nýjan tiltektarlista, sem hluta af virkninni **Opna úttakspantanir**. 

[![Skipunin Opna úttakspantanir á valmynd fyrir Aðgerðir.](./media/open-output-order.png)](./media/open-output-order.png)

[![Aðgerðavalmyndin á síðunni Opna úttakspantanir.](./media/open-output-order-function.png)](./media/open-output-order-function.png)

## <a name="reduce-quantity"></a>Minnka magn

Þriðja færibreytan sem nota má sem hluta af ferlinu við að búa til tiltektarlista er færibreytan **Minnka magn** . Stillingar þessa færibreytu vinna með stillingunni **Frátekning** sem setur af stað frátekningarferli sem er hluti af losun til vöruhúss.

[![Færibreyta minnkaðs magns.](./media/reduce-quantity.png)](./media/reduce-quantity.png)

## <a name="example-of-an-outbound-process-for-a-sales-order"></a>Dæmi um útleiðarferli fyrir sölupöntun

Í þessu dæmi er sölupöntun með tveimur vörum. Við myndun tiltektarlista er valin færibreytan **Minnka magn** . Þess vegna losar þú og stofnar aðeins tiltektarlínur fyrir tiltækar birgðir. Tilkynna verður tiltekt með skráningarferli fyrir tiltektarlista (**Staða tiltektarleiðar** = **Virkt**).

Birgðir sem ekki hafa verið fráteknar verða fráteknar við myndun tiltektarlista. Ótiltækar birgðir er hægt að fjarlægja annaðhvort úr sölustað eða út í vöruhús til útleiðarferlis síðar, þegar birgðir eru tiltækar til að tína.

[![Uppfæra tiltektarlistann.](./media/update-picking-list.png)](./media/update-picking-list.png)

Um leið og allar tiltektarlínur hafa verið teknar til á síðunni **Skráning tiltektarlista** er tengdri afhendingu lokið. Hægt er að hefja ferli fyrir fylgiseðla sölupantana með hliðsjón af völdum birgðum.

[![Uppfæra sendingar á útleið.](./media/outbound-shipments.png)](./media/outbound-shipments.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]