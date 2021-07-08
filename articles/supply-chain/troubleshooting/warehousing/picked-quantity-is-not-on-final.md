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
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301306"
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
- Staðsetningarleiðbeiningin hefur verið skilgreind með pökkunarstaðsetningu sem lokastaðsetning sendingar á meðan gámun bylgjusniðmáts var notuð.

## <a name="resolution"></a>Lausn

Hleðslan eða sendingin er í stöðu þar sem staðfesting á sendingu mistókst. Til að leysa þetta vandamál þarf að ljúka við eitt af eftirfarandi verkum:

- Farið yfir hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi.
- Hættið við vinnukennin sem hafa verið stofnuð með pökkunarstaðsetningunni sem lokastaðsetning sendingar, endurstillið staðsetningarleiðbeininguna og losið hleðsluna aftur.

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a>Farið yfir hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi

Notið eftirfarandi ferli til að yfirfara hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi.

1. Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.
1. Veljið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.
1. Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu.
1. Gera skal athugasemd um gildið í reitnum **Magn stofnaðs verks**.
1. Á aðgerðasvæðinu, í flipanum **Hleðslur**, í flokknum **Tengdar upplýsingar**, skal velja **Verk**.
1. Staðfestið að verkinu sé lokið á lokastaðsetningu sendingar og að tínt magn verksins stemmi við magn stofnaðs verks í hleðslulínunni.
1. Þetta ferli er endurtekið fyrir allar hleðslulínur til að ganga úr skugga um að öll viðmið séu uppfyllt.

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a>Hættið við vinnukennin sem hafa verið stofnuð með pökkunarstaðsetningunni sem lokastaðsetning sendingar, endurstillið staðsetningarleiðbeininguna og losið hleðsluna aftur

Notið eftirfarandi aðferð til að hætta við vinnukennin sem eru með pökkunarstaðsetninguna sem lokastaðsetning frágangs með sjálfvirka gámun í gangi.

1. Fara í **Vöruhússtjórn \> Reglubundin verkefni \> Hreinsa \> Hætta við vinnu**.
1. Svarglugginn **Hætta við vinnu** opnast. Tilgreinið kenni verksins sem á að hætta við í svæðinu **Vinnukenni**. Valið vinnukenni verður að vera með gildi fyrir **Staða verks** sem *Opin*, *Í vinnslu*, *Hætt við*, *Sameinað* eða *Lokað*.
1. Veljið **Í lagi**.
1. Veljið **Já** til að staðfesta að hætta skuli við verkið.
1. Endurtakið þetta ferli fyrir hin vinnukennin eftir því sem þörf krefur.

Frekari upplýsingar er að finna á [Hætta við vöruhúsavinnu vegna frábrigðameðhöndlunar](../../warehousing/cancel-warehouse-work.md).

Notið eftirfarandi ferli til að endurstilla staðsetningarleiðbeininguna þannig að hún noti ekki pökkunarstaðsetninguna sem lokastaðsetningu sendingar þegar sjálfvirk gámun er uppsett fyrir bylgjusniðmátið.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.
1. Í reitnum **Gerð verkbeiðni** velurðu *Sölupantanir*.
1. Veljið staðsetningarleiðbeininguna sem er verið að nota fyrir sjálfvirka gámun.
1. Í tækjastiku flýtiflipans **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Breyta fyrirspurn**.
1. Í glugga fyrirspurnarritilsins, í flipanum **Svið**, skal finna línuna þar sem **Reitur** er stilltur á *Staðsetningarforstilling* og staðfestið að reiturinn **Skilyrði** fyrir þá línu sé ekki stilltur á staðsetningarforstillingu sem er með **Staðsetningargerðina** *Pökkun*. Stillið reitinn **Skilyrði** til að leiðrétta lokastaðsetningu frágangs.

Notið eftirfarandi ferli til að losa hleðsluna aftur og stofna vinnukenni með réttri lokastaðsetningu sendingar.

1. Farið í **Vöruhúsakerfi \> Hleðsla \> Vinnusvæði hleðsluáætlunar**.
1. Í hlutanum **Hleðslur** skal finna hleðsluna sem þarf að losa.
1. Í tækjastiku hlutans **Hleðslur** skal velja **Losa \> Losa í vöruhús** til að losa valda hleðslu í vöruhúsið.
1. Endurtakið þetta ferli fyrir hinar hleðslurnar eftir því sem þörf krefur.
