---
title: Ekki er hægt að staðfesta sendingu vegna þess að ekki er búið að taka vörurnar til
description: Ekki er hægt að staðfesta sendingu vegna þess að ekki er búið að taka vörurnar til
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
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938490"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>Ekki er hægt að staðfesta sendingu vegna þess að ekki er búið að taka vörurnar til

Villukóði: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>Einkenni

Þegar reynt er að staðfesta sendingu sýnir kerfið eftirfarandi villuboð:

> Sumar vörurnar sem þarf að nota fyrir farm %1 hafa ekki enn verið teknar til og færðar á endanlegan sendingarstað.

Því er ekki hægt að staðfesta sendinguna fyrir farminn.

## <a name="cause"></a>Orsök

Ekki er hægt að staðfesta hleðsluna eða sendinguna í núverandi stöðu vegna þess að eitt eftirfarandi skilyrða gæti verið til staðar:

- Tengt verk hefur ekki enn verið tínt og fært yfir á lokastaðsetningu sendingar.
- Tiltekið vinnumagn passar ekki við vinnumagn sem var búið til á farmlínunni.

## <a name="resolution"></a>Upplausn

Athugaðu tengdar sölupantanir eða flutningspantanir fyrir farminn eða sendinguna. Gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Veljið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.
1. Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu.
1. Gera skal athugasemd um gildið í reitnum **Magn stofnaðs verks**.
1. Á aðgerðasvæðinu, í flipanum **Hleðslur**, í flokknum **Tengdar upplýsingar**, skal velja **Verk**.
1. Staðfestið að verkinu sé lokið á lokastaðsetningu sendingar og að tínt magn verksins stemmi við magn stofnaðs verks í hleðslulínunni.
1. Þetta ferli er endurtekið fyrir allar hleðslulínur til að ganga úr skugga um að öll viðmið séu uppfyllt.
