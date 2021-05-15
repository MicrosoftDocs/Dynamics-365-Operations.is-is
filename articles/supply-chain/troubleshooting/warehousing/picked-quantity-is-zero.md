---
title: Ekki er hægt að staðfesta sendingu vegna þess að magnið er núll
description: Ekki er hægt að staðfesta sendingu vegna þess að magnið er núll
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
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938489"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a>Ekki er hægt að staðfesta sendingu vegna þess að magnið er núll

Villukóði: LoadLineWarningUpdatedToZero

## <a name="symptoms"></a>Einkenni

Þegar reynt er að staðfesta sendingu sýnir kerfið eftirfarandi villuboð:

> Hleðslulína fyrir atriði %1 og sendingu %2 hefur verið uppfærð til að hafa núllmagn þar sem uppsetning vanafhendingar leyfir ekki sendingu magns fyrir þetta atriði.

Því er ekki hægt að staðfesta sendinguna fyrir farminn.

## <a name="cause"></a>Orsök

Kerfið metur hvort tiltektarmagnið sé innan væntanlegra marka út frá tiltektarmagni, magni hleðslulínu og prósentu vanafhendingar. Ef kerfið finnur að valið magn í hleðslulínunni sé 0 (núll) er ekki hægt að staðfesta sendinguna. Til dæmis gæti þetta vandamál komið upp ef hætt hefur verið við vinnu og prósenta vanafhendingar í hleðslulínunni er 100 prósent.

## <a name="resolution"></a>Upplausn

Athugið hleðslulínurnar til að ganga úr skugga um að prósenta vanafhendingar og magn séu í samræmi við tiltektarvinnuna.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Veljið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.
1. Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu fyrir vöruna sem fer umfram prósentu vanafhendingar.
1. Breytið gildinu í reitnum **Vanafhending** eða reitnum **Magn** eins og þörf er á.

> [!TIP]
> Ef vandamálið er enn til staðar gæti þurft að ljúka meira en einni tiltekt fyrir tengdar sölupantanir eða flutningspantanir þar til tiltækt magn er í samræmi vð hleðsluna eða sendinguna.
