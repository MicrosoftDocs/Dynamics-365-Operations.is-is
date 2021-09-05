---
title: Ekki er hægt að staðfesta sendingu vegna þess að hleðslulínurnar eru núll
description: Ekki er hægt að staðfesta sendingu vegna þess að hleðslulínurnar eru núll.
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
ms.openlocfilehash: 15aa7f5e72ff8f2c027b5b020a23328978aa02b0
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/13/2021
ms.locfileid: "7344235"
---
# <a name="you-cant-confirm-a-shipment-because-load-lines-have-zero-quantity"></a>Ekki er hægt að staðfesta sendingu vegna þess að hleðslulínurnar eru núll

Villukóði: WAX:LoadTableWarningAllLinesZero, WAX2543

## <a name="symptoms"></a>Einkenni

Þegar reynt er að staðfesta sendingu sýnir kerfið eftirfarandi villuboð:

> Allar línurnar í hleðslu %1 eru með núllmagn.  
> Ekki var hægt að staðfesta sendinguna fyrir farm %1.

Því er ekki hægt að staðfesta sendinguna fyrir farminn.

## <a name="cause"></a>Orsök

Kerfið metur hvort hægt sé að staðfesta hleðslulínu fyrir sendingu út frá vinnukennum sem eru búin til, magni hleðslulínu og prósentu vanafhendingar. Ef kerfið kemst að því að engin vinnukenni er til og ef prósenta vanafhendingar er stillt á 100 prósent, getur þú ekki staðfest sendinguna.

Til dæmis gæti þetta vandamál komið upp ef hætt hefur verið við vinnu og prósenta vanafhendingar í hleðslulínunni er 100 prósent.

## <a name="resolution"></a>Lausn

Hleðslan eða sendingin er í stöðu þar sem staðfesting á sendingu mistókst. Til að leysa þetta vandamál þarf að ljúka við eitt af eftirfarandi verkum:

- Farið yfir hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið passi.
- Athugið hleðslulínurnar til að ganga úr skugga um að prósenta vanafhendingar og magn séu í samræmi við tiltektarvinnuna.

### <a name="review-your-load-lines-to-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Farið yfir hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi

Notið eftirfarandi ferli til að yfirfara hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Opnið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.
1. Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu.
1. Gera skal athugasemd um gildið í reitnum **Magn stofnaðs verks**.
1. Á aðgerðasvæðinu, í flipanum **Hleðslur**, í flokknum **Tengdar upplýsingar**, skal velja **Verk**.
1. Staðfestið að verkinu sé lokið á lokastaðsetningu sendingar og að tínt magn verksins stemmi við magn stofnaðs verks í hleðslulínunni.
1. Ef þú finnur misræmi skaltu hætta við viðkomandi verk, stilla aftur staðsetningarleiðbeininguna og losa hleðsluna aftur. Upplýsingar er að finna í [Ekki er hægt að staðfesta sendingu vegna þess að ekki er búið að taka vörurnar til](picked-quantity-is-not-on-final.md).
1. Þetta ferli er endurtekið fyrir allar hleðslulínur til að ganga úr skugga um að öll viðmið séu uppfyllt.

### <a name="review-your-load-lines-to-make-sure-that-the-underdelivery-percentage-and-quantities-are-aligned-with-the-picked-work"></a>Farðu yfir hleðslulínurnar til að ganga úr skugga um að prósenta vanafhendingar og magn séu í samræmi við tiltektarvinnuna

Notið eftirfarandi aðgerðir til að fara yfir hleðslulínurnar til að ganga úr skugga um að prósenta vanafhendingar og magn séu í samræmi við tiltektarvinnuna.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Opnið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.
1. Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu fyrir vöruna sem fer umfram prósentu vanafhendingar.
1. Breytið gildinu í reitnum **Vanafhending** eða reitnum **Magn** eins og þörf er á.

> [!TIP]
> Ef vandamálið er enn til staðar gæti þurft að ljúka meira en einni tiltekt fyrir tengdar sölupantanir eða flutningspantanir þar til tiltækt magn er í samræmi vð hleðsluna eða sendinguna.
