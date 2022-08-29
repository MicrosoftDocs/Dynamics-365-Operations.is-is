---
title: Runulosun flutningspantana sem eru fráteknar að hluta
description: Þessi grein lýsir því hvernig á að setja upp og beita lotuútgáfu á hluta fráteknum flutningspöntunum úr farsíma.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2022
ms.locfileid: "9218683"
---
# <a name="batch-release-of-partially-reserved-transfer-orders"></a>Runulosun flutningspantana sem eru fráteknar að hluta

[!include [banner](../includes/banner.md)]

Virkni fyrir runulosun hlutafrátekinna flutningspantana gerir klefit að losa að hluta flutningspantanir til vöruhúss með því að nota runuvinnsla.
Þar sem í boði er að losa hluta magns þarf ekki að bíða eftir því að allt magn pöntunar verði tiltækt í vöruhúsi áður en pöntun er losuð.

Losun pantana í vöruhús er vöruhússtjórnunarferli (WMS). Þetta ferli felur í sér aðgerðir svo sem tiltekt, pökkun og sendingu sem starfsmaður í vöruhúsi getur framkvæmt með fartæki.

## <a name="where-it-applies"></a>Þar sem það á við

Fyrir þessa virkni eru flutningspantanir losaðar í vöruhús með því að nota runuvinnsla. Þessi virkni er gagnleg þegar ekki eru nægilegar birgðir í vöruhúsi en þú vilt samt flytja vörur úr einu vöruhúsi í annað.

## <a name="how-it-is-set-up"></a>Hvernig er það sett upp

### <a name="specify-fulfillment-criteria-for-transfer-orders-and-sales-orders"></a>Tilgreina þarf uppfyllingarskilyrði fyrir flutningspantanir og sölupantanir

Áður en losa má pöntun að hluta í vöruhús í runu verður að uppfylla uppfyllingarskilyrði. Þessi uppfyllingarskilyrði eru ákvörðuð með uppfyllingarstefnu.

Tilgreina þarf uppfyllingarskilyrði fyrir flutningspantanir og sölupantanir á fyrirtækisstigi Allt eftir uppsetning uppfyllingarreglna verður losun pantana í runu samþykkt eða hafnað. Pantanir verða unnar í samræmi við það.

- Til að búa til uppfyllingarreglur fyrir millifærslupantanir og sölupantanir, farðu á **Vöruhússtjórnun \> Uppsetning \> Losa á lager \> Uppfyllingarstefnur**, og búðu til uppfyllingarstefnu með því að slá inn nafn og lýsingu.
- Til að tilgreina uppfyllingarhlutfall, gildistegund og skilaboðin sem birtast ef uppfyllingarstefnan er brotin, farðu á **Vöruhússtjórnun \> Uppsetning \> Losa á lager \> Uppfyllingarstefnur**, og stilltu **Uppfyllingarhlutfall**, **·**, og **Skilaboð um uppfyllingu brot** sviðum.

### <a name="set-the-fulfillment-policies-for-transfer-orders-and-sales-orders"></a>Stilla þarf uppfyllingarskilyrði fyrir flutningspantanir og sölupantanir

- Til að stilla uppfyllingarreglur fyrir flutningspantanir skaltu fara á **Vörustjórnun \> Uppsetning \> Birgða- og vöruhúsastjórnunarfæribreytur**, og síðan, á **Flytja pantanir** flipa, í **Vöruhússtjórnun** kafla, veldu uppfyllingarstefnu millifærslupöntunar.
- Til að stilla uppfyllingarreglur fyrir sölupantanir skaltu fara á **Reikningur fáanlegur \> Uppsetning \> Færibreytur viðskiptakrafna**, og síðan, á **Vöruhússtjórnun** flipanum, veldu uppfyllingarstefnu sölupöntunar.

## <a name="allow-release-in-a-batch-and-specify-the-quantity-that-should-be-released-in-a-batch"></a>Leyfa losun í lotu og tilgreina magn sem á að losa í lotu

Runuvinnsla er notuð til að losa pantanir í vöruhús í runum. Færibreytur sem greina að pantanir sem á að keyra í runuvinnsla eru stilltar í runuvinnslunni sjálfri.

Færibreytan **Magn** tilgreinir hvort losa á í runu allt magnið eða efnislega frátekið magn. Færibreytan **Leyfa losun pantana sem hafa verið losaðar að hluta** ákvarðar hvort pantanir í runu á að samþykkja eða hafna ef þær voru losaðar að hluta fyrr.

- Til að stilla **Magn** og **Leyfa losun pantana sem hafa verið losaðar að hluta** færibreytur fyrir millifærslupantanir, farðu í **Vöruhússtjórnun \> Losa á lager \> Sjálfvirk losun millifærslupantana**.
- Til að stilla **Magn** og **Leyfa losun pantana sem hafa verið losaðar að hluta** færibreytur fyrir sölupantanir, farðu í **Vöruhússtjórnun \> Losa á lager \> Sjálfvirk losun sölupantana**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
