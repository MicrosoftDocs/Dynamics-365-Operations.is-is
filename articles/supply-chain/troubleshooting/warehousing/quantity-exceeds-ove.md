---
title: Ekki er hægt að staðfesta sendingu vegna þess að magnið er hærra en hlutfall ofafhendingar
description: Ekki er hægt að staðfesta sendingu vegna þess að magnið er hærra en hlutfall ofafhendingar
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
ms.openlocfilehash: c9b5ba8dedb927ee049d7e53e9a666902f563f49
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938493"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-overdelivery-percentage"></a>Ekki er hægt að staðfesta sendingu vegna þess að magnið er hærra en hlutfall ofafhendingar

Villukóði WAX1687

## <a name="symptoms"></a>Einkenni

Þegar reynt er að staðfesta sendingu sýnir kerfið eftirfarandi villuboð:

> Ekki var hægt að staðfesta sendinguna fyrir farm %1 vegna þess að magnið fyrir vöru %2 fer yfir þá prósentu sem skilgreind er fyrir ofafhendingu.

Því er ekki hægt að staðfesta sendinguna fyrir farminn.

## <a name="cause"></a>Orsök

Magn hleðslunnar eða sendingarinnar hefur aðeins verið tínd að hluta til. Magnið er í augnablikinu hærra en tiltektarmagn um prósentu sem er utan við leyfða ofafhendingu.

## <a name="resolution"></a>Upplausn

Til að leysa þetta vandamál þarf að ljúka við eitt af eftirfarandi verkum:

- Stillið magn hleðslulínunnar.
- Stillið prósentu ofafhendingar.

### <a name="set-the-load-line-quantity"></a>Stilla magn hleðslulínunnar

Til að stilla magn hleðslulínu skal fylgja eftirfarandi skrefum.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Veljið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.
1. Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu fyrir vöruna sem fer umfram prósentu ofafhendingar.
1. Á flipanum **Línuupplýsingar** skal velja **Pöntun**.
1. Í reitnum **Magn** skal stilla gildið á tiltektarmagnið (þ.e. á gildið í **Magn stofnaðs verks**) þannig að staðfesta megi sendingu.

### <a name="set-the-overdelivery-percentage"></a>Stilla prósentu ofafhendingar

Til að stilla vanafhendingarhlutfall skal fylgja eftirfarandi skrefum.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Veljið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.
1. Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu fyrir vöruna sem fer umfram prósentu ofafhendingar.
1. Á flýtiflipanum **Línuupplýsingar** skal velja **Almennt**.
1. Í reitnum **Ofafhending** skal stilla gildið á hærri prósentu sem nær utan um magnið sem er tínt gagnvart hleðslumagninu, þannig að staðfesting sendingar geti átt sér stað.
