---
title: Uppsetning afurða sem hægt er að framleiða eða kaupa
description: Vörur geta verið virkjaðar á ýmsa vegu - Hægt er að búa þær til (framleiða) eða versla þær (kaupa). Þessi grein lýsir nokkrum dæmigerðum atriðum til að hafa í huga þegar vörur eru skilgreindar til að styðja fjöl-uppruna.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4910faa2e66cb61f6064e686c49369d14526cc1f
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674506"
---
# <a name="set-up-products-that-can-be-produced-or-procured"></a>Uppsetning afurða sem hægt er að framleiða eða kaupa

[!include [banner](../includes/banner.md)]

Vörur geta verið virkjaðar á ýmsa vegu - Hægt er að búa þær til (framleiða) eða versla þær (kaupa). Þessi grein lýsir nokkrum dæmigerðum atriðum til að hafa í huga þegar vörur eru skilgreindar til að styðja fjöl-uppruna. 

Fjöl-uppruni er yfirleitt notað fyrir keypta vöru sem er stundum framleidd eða þegar vara var sem var upprunalega framleidd vara er breytt þannig að hún er nú aðallega keypt vara. Varan er fyrst skilgreind sem framleidd vara svo hægt sé að skilgreina uppskrift (BOM)°og leiðarupplýsingar og til að styðja framleiðslupantanir fyrir vöruna. Framleiðslugerðina ætti að stilla á **BOM** (eða, fyrir framleiðsluferli,°**Formúlu** eða **Aukaafurð**).

Þegar staðlaður kostnaður er notaður er hægt að reikna vörukostnaðarfærslu fyrir framleiddu vöruna. Samt sem áður gæti vörukostnaðarfærsla ekki passað við staðalkostnaðinn sem óskað er eftir fyrir kaup. Í því tilfelli þarf að færa staðalkostnaðinn inn handvirkt og hann þarf að vera virkjaður fyrir vörukostnaðarfærsluna. Við útreikning kostnaðar ætti að íhuga að nota sérstaka Uppskrift og leið sem tákna blandað framboð afurðar yfir fjárhagstímabil til að lágmarka frávik yfir ákveðið tímabil. Þar að auki er hægt að flytja framleidda vöru á einu svæði yfir á annað. Þess vegna verður að skrá kostnað vörunnar handvirkt inn og virkja fyrir svæðið sem varan er flutt til. Þegar framleidda varan er notuð sem íhlutur í flóknari vörum skal fara með kostnað íhlutarins sem keypta vöru. Þessi viðmið gilda óháð því°hvort kostnaður íhlutarins var reiknaður eða færður inn handvirkt. Uppskriftarútreikningur ætti sem sagt að líta á kostnað vörunnar sem keyptan íhlut frekar en að reikna út kostnað sem°byggist°á uppskriftar- og leiðarupplýsingum hans. 

Hægt er að koma í veg fyrir þennan útreikning með því að velja fánann **Stöðva niðurbrot** sem er felldur inn í flokk uppskriftarútreiknings sem er úthlutaður vörunni. Til°að koma í veg fyrir að útreikningar aðalröðunar brjóti kröfur niður í gegnum vöruna, skal stilla niðurbrotsmarkið á 0 (núll) daga í vöruþekju eða vöruþekjuflokki. Útreikningur aðalröðunarinnar mun síðan fara með vöruna sem keypta vöru og ekki framkvæma frekari útreikninga fyrir upplýsingar um leið og Uppskrift vörunnar.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]