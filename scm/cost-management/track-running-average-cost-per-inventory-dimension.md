---
title: "Rakning hlaupandi meðaltalskostnaðar á hverja birgðavídd"
description: "Hver einstök birgðavara verður að vera tengd við ákveðinn birgðavíddarflokk. Hlaupandi meðaltal kostnaðarverðs fyrir vöru er þess vegna reiknað út miðað við val birgðavídda sem er verið að rekja fjárhagslega."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventOnhandItem
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4f5ca047835fcbb2567f0b97347b356e1b594980
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="tracking-running-average-cost-per-inventory-dimension"></a>Rakning hlaupandi meðaltalskostnaðar á hverja birgðavídd

[!include[banner](../includes/banner.md)]


Hver einstök birgðavara verður að vera tengd við ákveðinn birgðavíddarflokk. Hlaupandi meðaltal kostnaðarverðs fyrir vöru er þess vegna reiknað út miðað við val birgðavídda sem er verið að rekja fjárhagslega.

Það eru þrjár gerðir af birgðavíddum: afurð, geymsla og rakning. Vöruvíddir innihalda skilgreiningu, stærð, og lit. Vöruvíddir eru alltaf raktar fjárhagslega. Geymsluvíddir og rakningarvíddir innihalda staðsetningu, vöruhús, birgðastöðu, númeraplötu, rununúmer og raðnúmer. Hægt er að velja hvaða geymsluvíddir og rakningarvíddir verða raktar fjárhagslega. 

**Dæmi 1** 

Ef birgðavíddarflokkurinn sem er tengdur vörunni er rakinn fjárhagslega af vöruhúsinu, er hlaupandi meðaltal kostnaðarverðs reiknað út fyrir hvert vöruhús fyrir sig. Eftirfarandi innkaupapantanir hafa verið reikningsfærðar:

-   Innkaupapöntun fyrir magnið 2 á kostnaðarverði 10,00 USD hefur verið reikningsfærð fyrir vöruhús GW.
-   Innkaupapöntun fyrir magnið 3 á kostnaðarverði 12,00 USD hefur verið reikningsfærð fyrir vöruhús GW.
-   Innkaupapöntun fyrir magnið 5 á kostnaðarverði 15,00 USD hefur verið reikningsfærð fyrir vöruhús MW.

Hlaupandi meðaltal kostnaðarverðs fyrir vöruhús GW er 11,20 USD og hlaupandi meðaltal kostnaðarverðs fyrir vöruhús MW er 15,00 USD. Sölupöntunarreikningur er bókaður fyrir vöruhús GW. Verðmæti birgða og kostnaður seldrar vöru (áður en birgðalokun er keyrð og án merkingar) er 11,20 USD. Önnur sölupöntun er bókuð fyrir vöruhús MW. Verðmæti birgða og kostnaður seldrar vöru (áður en birgðalokun er keyrð og án merkingar) er 15,00 USD. 

**Dæmi 2** Ef geymsluvíddaflokkur sem tengist vörunni er rakinn fjárhagslega af vöruhúsinu og rakningarvíddaflokkur er rakinn fjárhagslega af rununúmeri, reiknast hlaupandi meðaltal kostnaðarverðs fyrir hverja runu. 

**Ábending:**Mælt er með því að kostnaðarverð sé alltaf skoðað fyrir allar fjárhagsvíddir sem er verið að rekja. Eftirfarandi innkaupapantanir hafa verið reikningsfærðar:

-   Innkaupapöntun fyrir magnið 2 á kostnaðarverði 10,00 USD, hefur verið reikningsfært fyrir vöruhús GW og runu AAA.
-   Innkaupapöntun fyrir magnið 3 á kostnaðarverði 12,00 USD, hefur verið reikningsfært fyrir vöruhús GW og runu AAA.
-   Innkaupapöntun fyrir magnið 2 á kostnaðarverði 15,00 USD, hefur verið reikningsfært fyrir vöruhús GW og runu BBB.

Hlaupandi meðaltal kostnaðarverðs fyrir vöruhús GW og runu AAA er 11,20 USD og hlaupandi meðaltal kostnaðarverðs fyrir vöruhús GW og runu BBB er 15,00 USD.



