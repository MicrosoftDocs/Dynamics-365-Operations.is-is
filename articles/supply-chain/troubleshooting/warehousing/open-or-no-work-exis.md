---
title: Ekki er hægt að staðfesta sendingu vegna ólokinnar vinnu eða vinnu sem vantar
description: Ekki er hægt að staðfesta sendingu vegna ólokinnar vinnu eða vinnu sem vantar
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm, WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 59def4427f9fff32fd3839bb9f9b5d5cccdc7720f92a84f1af3adad596d8b352
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730059"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a>Ekki er hægt að staðfesta sendingu vegna ólokinnar vinnu eða vinnu sem vantar

Villukóði WAX515

## <a name="symptoms"></a>Einkenni

Þegar reynt er að staðfesta sendingu sýnir kerfið eftirfarandi villuboð:

> Ekki var hægt að staðfesta sendinguna fyrir farm %1 vegna þess að ljúka þarf allri vinnu fyrir farminn.

Því er ekki hægt að staðfesta sendinguna fyrir farminn.

## <a name="cause"></a>Orsök

Hleðslan eða sendingin er í stöðu þar sem staðfesting á sendingu mistókst. Áður en þú getur staðfest sendinguna verður að minnsta kosti einhver vinna að vera til fyrir hleðsluna og öll sú vinna verður að vera með stöðuna *Lokuð* eða *Hætt við*.

## <a name="resolution"></a>Upplausn

Athugið tengdar sölupantanir eða flutningspantanir fyrir farminn eða sendinguna og gangið úr skugga um að öll tengd vinna sé lokið eða hætt við.

Hægt er að vinna með sendingar og hleðslur á nokkrum síðum. Eftirfarandi undirhlutar sýna nokkur dæmi.

### <a name="all-loads-page"></a>Síða fyrir allan farm

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Veljið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.
1. Á aðgerðasvæðinu, í flipanum **Hleðslur**, í flokknum **Tengdar upplýsingar**, skal velja **Verk**.
1. Skoðaðu stöðu hvers vinnukennis. Fylgið eftir hverju vinnukenni sem er ekki með stöðuna *Lokið* eða *Hætt við*.
1. Þegar hvert vinnukenni er með stöðuna *Lokað* eða *Hætt við* skaltu aftur reyna að staðfesta sendinguna.

### <a name="all-shipments-page"></a>Síða fyrir allar sendingar

1. Opnið **Vöruhúsakerfi \> Sendingar \> Allar sendingar**.
1. Veljið sendinguna sem ekki er hægt að staðfesta.
1. Á aðgerðasvæðinu, í flipanum **Sendingar**, í flokknum **Vinna**, skal velja **Upplýsingar um verk**.
1. Skoðaðu stöðu hvers vinnukennis. Fylgið eftir hverju vinnukenni sem er ekki með stöðuna *Lokið* eða *Hætt við*.
1. Þegar hvert vinnukenni er með stöðuna *Lokað* eða *Hætt við* skaltu aftur reyna að staðfesta sendinguna.

### <a name="all-work-page"></a>Öll vinnusíða

1. Farið í **Vöruhúsakerfi \> Vinna \> Öll vinna**.
1. Veljið verk fyrir pöntunarnúmerið sem ekki er hægt að staðfesta sendinguna fyrir.
1. Á aðgerðasvæðinu, í flipanum **Sending**, í flokknum **Sending**, skal velja **Staðfesta sendingu**.
1. Skoðaðu stöðu hvers vinnukennis. Fylgið eftir hverju vinnukenni sem er ekki með stöðuna *Lokið* eða *Hætt við*.
1. Þegar hvert vinnukenni er með stöðuna *Lokað* eða *Hætt við* skaltu aftur reyna að staðfesta sendinguna.
