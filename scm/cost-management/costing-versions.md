---
title: "Kostnaðarútgáfa"
description: "Þessi grein veitir upplýsingar um kostnaðarútgáfur, hvernig á að viðhalda þeim og tegundir gagna sem þú getur haft í þeim. Grunntilgangur kostnaðarútgáfu er að innihalda kostnaðarfærslur um hluti, kostnaðarflokka, og útreikningsformúlur fyrir óbeinan kostnað."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 54532
ms.assetid: cd239da5-f434-4d1b-8196-5414c888d76d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ce1f0c2107b701f12c18646ff4369e543bec7c97
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="costing-versions"></a>Kostnaðarútgáfa

[!include[banner](../includes/banner.md)]


Þessi grein veitir upplýsingar um kostnaðarútgáfur, hvernig á að viðhalda þeim og tegundir gagna sem þú getur haft í þeim. Grunntilgangur kostnaðarútgáfu er að innihalda kostnaðarfærslur um hluti, kostnaðarflokka, og útreikningsformúlur fyrir óbeinan kostnað.

Kostnaðarútgáfa getur þjónað einum tilgangi eða fleiri eftir því hvaða gögn eru innan kostnaðarútgáfunnar. Grunntilgangur kostnaðarútgáfu er að innihalda kostnaðarfærslur um hluti, kostnaðarflokka, og útreikningsformúlur fyrir óbeinan kostnað. Kostnaðarútgáfa getur innihaldið færslur staðlaðs kostnaðar eða áætlaðs kostnaðar sem eru byggðar á kostnaðargerðinni sem kostnaðarútgáfunni er úthlutað.

## <a name="costing-versions-for-standard-or-planned-costs"></a>Kostnaðarútgáfa fyrir staðlaðan eða áætlaðan kostnað
### <a name="standard-costs"></a>Staðalkostnaður

Kostnaðarútgáfa getur stutt birgðalíkan staðlaðs kostnaðar fyrir vörur, þar sem kostnaðarútgáfan inniheldur safn af færslum staðlaðs kostnaðar um vörur og framleiðsluferli. Kostnaðargögn um framleiðsluferli birtast í kostnaðartegundum fyrir leiðaaðgerðir og reikningsformúlum fyrir óbeinan framleiðslukostnað.

### <a name="planned-costs"></a>Áætlaður kostnaður

Kostnaðarútgáfa getur innihaldið færslur áætlaðs kostnaðar um vörur og framleiðsluferli. Kostnaðarútgáfa með áætluðum kostnaði er oft notuð til að styðja hermun kostnaðarútreikninga, til dæmis til að herma eftir°áhrifum kostnaðarbreytinga á innkeypt efni eða framleiðsluferla á útreiknaðan kostnað framleiddra vara. Kostnaðarfærslur vöru fyrir áætlaðan kostnað er einnig hægt að nota til að styðja birgðalíkön raunverulegs kostnaðar með því að úthluta upphafsgildum fyrir kostnað vöru. Þessi gildi eru meðal annars útreikningur áætlaðs kostnaðar fyrir framleiddar vörur.

## <a name="entering-costs"></a>Færa inn kostnað
Viðhald á kostnaðarfærslum innan kostnaðarútgáfu felur í sér að færa inn kostnað fyrir innkeyptar vörur og fyrir vörur sem eru fluttar á milli svæða. Frekara viðhald gagna fyrir framleiðendur felur í sér að færa inn kostnað fyrir kostnaðartegundir (tengdar við leiðaaðgerðir), færa inn reikniformúlur fyrir óbeinan kostnað sem endurspeglar framleiðslurekstrarkostnað og reikna út kostnað fyrir framleiddar vörur. 

Kostnaðargögn vöru innan kostnaðarútgáfu samanstanda af einni eða fleiri kostnaðarfærslum fyrir hverja vöru. Kostnaðarfærsla vöru er upphaflega færð inn með stöðuna **Í biðstöðu** og ætlaða upphafsdagsetningu. Þegar kostnaðarfærsla vöru er virkjuð uppfærist staðan í **Virk** og gildisdagsetningin er uppfærð í virkjunardagsetningu. Mismunandi kostnaðarfærslur fyrir vöru geta endurspeglað ólík svæði, gildisdagsetningu eða stöðu. Þegar kostnaður er reiknaður fyrir framleiddar vörur og framtíðardagsetningu, notar uppskriftarútreikningurinn kostnaðarfærslur með viðeigandi gildisdagsetningu hvort sem°staðan er **Í biðstöðu** eða **Virk**. Virk kostnaðarfærsla vöru verður notuð til að meta framleiðslupöntunarkostnað og virði birgðafærslna í birgðalíkani staðlaðs kostnaðar. Viðhald kostnaðarfærslna fyrir kostnaðartegundir og reikniformúlur óbeins kostnaðar er svipað og viðhald kostnaðarfærslna vöru. 

Tvær lokunarreglur fyrir kostnaðarútgáfu ákvarða hvort hægt sé að viðhalda biðkostnaði og hvort hægt sé að gera biðkostnað virkan. Notið lokunarreglur til að heimila viðhald gagna og til að koma í veg fyrir gagnaviðhald fyrir kostnaðarfærslur innan kostnaðarútgáfu. 

Kostnaðarútgáfa getur einnig innihaldið gögn um söluverð vöru eða innkaupaverð fyrir uppskriftarútreikninga.

## <a name="item-sales-prices-for-bom-calculations"></a>Söluverð vöru fyrir uppskriftarútreikninga
Aðal ástæða þess að taka með gögn um söluverð er að viðhalda útreiknuðu söluverði framleiddrar vöru. Síðan er hægt að greina útreiknað söluverð til að ákvarða hvernig íhlutir, leiðaraðgerðir og rekstrarkostnaður hefur áhrif á kostnað og söluverð. 

Önnur ástæða þess að taka með gögn um söluverð er að skilgreina söluverðsfærslur fyrir íhlutavörur. Síðan er hægt að nota þessar færslur til að reikna út söluverð framleiddra vara. Fyrst þarf að skilgreina söluverðslíkan sem eru innfelld í uppskriftarútreikningsflokk og tengja flokk uppskriftarútreiknings keyptum vörum. Síðan, þegar framkvæmdir eru uppskriftarútreikninga sem nota áætlaðan kostnað, skal velja kostnaðarverðslíkan útreikningsflokks Uppskriftar. 

Að öðru leyti eru söluverðsfærslur vöru aðeins notaðar í upplýsingarskyni, hvort sem þær eru færðar inn handvirkt eða reiknaðar út. Með virkjun söluverðsfærslu vöru, er hægt að uppfæra grunnsöluverð vörunnar. Hins vegar er grunnsöluverðið ekki svæðisbundið og hægt er að hnekkja því handvirkt. Grunnsöluverð vöru virkar sem sjálfgefið söluverð á sölupöntunum og sölutilboðum.

## <a name="item-purchase-prices-for-bom-calculations"></a>Innkaupaverð vöru fyrir uppskriftarútreikninga
Aðaltilgangur þess að leyfa gögn°um innkaupsverð er að skilgreina innkaupaverðsfærslur fyrir íhlutavörur sem er svo hægt að nota til að reikna út kostnað framleiddra vara. Færslur innkaupaverðs vöru verður að færa inn handvirkt. 

Til að virkja innihald innkaupaverðs þarf fyrst að skilgreina uppskriftarútreikningsflokk sem inniheldur kostnaðarverðslíkan fyrir innkaupaverð vöru, og úthluta útreikningaflokkur Uppskriftar til innkeyptra vara. Síðan skal nota kostnaðarverðslíkan fyrir flokk uppskriftarútreikningsins þegar uppskriftarútreikningar eru gerðir sem nota áætlaðan kostnað til að reikna út söluverð framleiddra vara. 

Innkaupsverðsfærslurnar eru einnig aðeins notaðar til upplýsingar. Með því að breyta stöðu skýrslu innkaupsverðs vöru úr **í Biðstöðu** í **Virkt**, er hægt að uppfæra grunn innkaupsverð vöru. Hins vegar er grunnsöluverðið ekki svæðisbundið og hægt er að hnekkja því handvirkt. Grunninnkaupsverð vöru er notað sem sjálfgefið innkaupsverð í innkaupapöntunum.




