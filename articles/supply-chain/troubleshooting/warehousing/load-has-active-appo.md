---
title: Ekki er hægt að staðfesta sendingu vegna dagatalsvandamáls
description: Ekki er hægt að staðfesta sendingu vegna dagatalsvandamáls
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8aae45beeef1934760d620874897f46a1cf901995e2b83e148a1d56898d9c717
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735945"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a>Ekki er hægt að staðfesta sendingu vegna dagatalsvandamáls

Villukóði TRX2716

## <a name="symptoms"></a>Einkenni

Þegar reynt er að staðfesta sendingu sýnir kerfið eftirfarandi villuboð:

> Dagatalsgerðin %1 krefst þess að mót %2 sé skráð inn og út.

Því er ekki hægt að staðfesta sendinguna fyrir farminn.

## <a name="cause"></a>Orsök

Virkt erindi fyrir hleðsluna er til. Til dæmis er regla sem gerir kröfu um innskráningu ökumanns. Þar af leiðandi er hleðslan eða sendingin í stöðu þar sem staðfesting á sendingu mistekst.

## <a name="resolution"></a>Upplausn

Þú verður að kanna og laga öll vandamál með virk erindi sem eru tengd við hleðsluna.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Veljið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.
1. Á aðgerðasvæðinu, í flipanum **Flutningur**, í flokknum **Erindi**, skal velja **Tímasetning erindis**.
1. Fylgið einu af eftirfarandi skrefum:

    - Gakktu úr skugga um að inn-/útskráning ökumanns sé lokið fyrir erindið.
    - Ljúktu eða hættu við erindið.
    - Gera valkostinn **Innskráning ökumanns nauðsynleg** óvirkan fyrir tengda reglu um erindi.
