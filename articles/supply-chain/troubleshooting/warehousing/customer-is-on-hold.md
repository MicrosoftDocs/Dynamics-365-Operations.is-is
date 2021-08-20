---
title: Þú getur ekki staðfest sendingu vegna þess að viðskiptavinurinn er í bið
description: Þú getur ekki staðfest sendingu vegna þess að viðskiptavinurinn er í bið.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 82b28e7cfd8c88e453cdd09398f5a92f605eab15a17d33defa0b9729a53c05b6
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012177"
---
# <a name="you-cant-confirm-a-shipment-because-the-customer-is-on-hold"></a>Þú getur ekki staðfest sendingu vegna þess að viðskiptavinurinn er í bið

Villukóði: WAX:CustomerOnHoldShipmentCannotBeConfirmed

## <a name="symptoms"></a>Einkenni

Þegar reynt er að staðfesta sendingu sýnir kerfið eftirfarandi villuboð:

> Ekki er hægt að staðfesta sendingu %1 vegna þess að viðskiptavinur er í bið fyrir %2.

Því er ekki hægt að staðfesta sendinguna fyrir farminn.

## <a name="cause"></a>Orsök

Viðskiptavinaraðgangur hleðslu eða sendingar er í bið. Því kemur staða viðskiptavinar í veg fyrir staðfestingu sendingar.

## <a name="resolution"></a>Lausn

Fylgið eftirfarandi skrefum til að opna aðgang viðskiptavinar.

1. Farðu í **Viðskiptakröfur \> Viðskiptavinir \> Alla viðskiptavini**.
1. Opnið reikning viðskiptavinar sem ekki er hægt að staðfesta sendinguna fyrir.
1. Í flýtiflipanum **Skuldir og innheimta** skal stilla reitinn **Reikningsfærsla og afhending í bið** á *Nei*.
1. Þetta ferli er endurtekið fyrir alla lokaða viðskiptavini fyrir hleðsluna.
