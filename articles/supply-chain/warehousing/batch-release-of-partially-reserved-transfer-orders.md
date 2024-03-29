---
title: Runulosun flutningspantana sem eru fráteknar að hluta
description: Í þessari grein er lýst hvernig eigi að setja upp aog jafna runulosun hlutafrátekinna flutningspantana úr fartæki.
author: perlynne
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadPlanningWorkbench, WHSFulfillmentPolicy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 741377a43e2bfe702b213647cc6460a3d6ad93fb
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218683"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a>Runulosun flutningspantana sem eru fráteknar að hluta

[!include [banner](../includes/banner.md)]

Virkni fyrir runulosun hlutafrátekinna flutningspantana gerir klefit að losa að hluta flutningspantanir til vöruhúss með því að nota runuvinnsla.
Þar sem í boði er að losa hluta magns þarf ekki að bíða eftir því að allt magn pöntunar verði tiltækt í vöruhúsi áður en pöntun er losuð.

Losun á pöntun í vöruhús er ferli í vöruhúsakerfisferli (WMS). Þetta ferli felur í sér aðgerðir svo sem tiltekt, pökkun og sendingu sem starfsmaður í vöruhúsi getur framkvæmt með fartæki.

## <a name="where-it-applies"></a>Þar sem það á við

Fyrir þessa virkni eru flutningspantanir losaðar í vöruhús með því að nota runuvinnsla. Þessi virkni er gagnleg þegar ekki eru nægilegar birgðir í vöruhúsi en þú vilt samt flytja vörur úr einu vöruhúsi í annað.

## <a name="how-it-is-set-up"></a>Hvernig er það sett upp

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>Tilgreina þarf uppfyllingarskilyrði fyrir flutningspantanir og sölupantanir

Áður en losa má pöntun að hluta í vöruhús í runu verður að uppfylla uppfyllingarskilyrði. Þessi uppfyllingarskilyrði eru ákvörðuð með uppfyllingarstefnu.

Tilgreina þarf uppfyllingarskilyrði fyrir flutningspantanir og sölupantanir á fyrirtækisstigi Allt eftir uppsetning uppfyllingarreglna verður losun pantana í runu samþykkt eða hafnað. Pantanir verða unnar í samræmi við það.

- Til að stofna uppfyllingarreglur fyrir flutningspantanir og sölupantanir skal fara í **Vöruhúsakerfi \> Uppsetning \> Losa í vöruhús \> Uppfyllingarreglur**, og stofna uppfyllingarreglu með því að færa inn nafn og lýsingu.
- Til að tilgreina uppfyllingartíðni, gildisgerð og skilaboð sem birtast ef uppfyllingarreglur eru brotnar, opnaðu **Vöruhúsakerfi \> Uppsetning \> Losa í vöruhús \> Uppfyllingarreglur**, og stiltu svo reitina **Uppfyllingartíðni**, **Gerð gildis**, og **Skilaboð vegna brota á uppfyllingu**.

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>Stilla þarf uppfyllingarskilyrði fyrir flutningspantanir og sölupantanir

- Til að stilla uppfyllingarreglur fyrir flutningspantanir skal fara í **Birgðastjórnun \> Uppsetning \> Færibreytur fyrir birgða- og vöruhúsakerfi** og síðan í flipanum **Flutningspantanir** skal í hlutanum **Vöruhúsakerfi** velja uppfyllingarreglu flutningspöntunar.
- Til að stilla uppfyllingarreglur fyrir sölupantanir skal fara í **Viðskiptakröfur \> Uppsetning \> Færibreytur viðskiptakrafna** og síðan skal í flipanum **Vöruhúsakerfi** velja uppfyllingarreglu sölupöntunar.

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-released-in-a-batch"></a>Leyfa losun í runu og tilgreina magn sem á að losa í runu

Runuvinnsla er notuð til að losa pantanir í vöruhús í runum. Færibreytur sem greina að pantanir sem á að keyra í runuvinnsla eru stilltar í runuvinnslunni sjálfri.

Færibreytan **Magn** tilgreinir hvort losa á í runu allt magnið eða efnislega frátekið magn. Færibreytan **Leyfa losun pantana sem hafa verið losaðar að hluta** ákvarðar hvort pantanir í runu á að samþykkja eða hafna ef þær voru losaðar að hluta fyrr.

- Til að stilla færibreyturnar **Magn** og **Leyfa losun pantana sem hafa verið losaðar að hluta** skal opna **Vöruhúsastjórnun \> Losa í vöruhús \> Sjálfvirk losun flutningspantana**.
- Til að stilla færibreyturnar **Magn** og **Leyfa losun pantana sem hafa verið losaðar að hluta** fyrir sölupantanir skal opna **Vöruhúsastjórnun \> Losa í vöruhús \> Sjálfvirk losun flutningspantana**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
