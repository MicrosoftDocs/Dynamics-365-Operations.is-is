---
title: Kostnaðarskjöl
description: Uppsetning á kostnaðarskjali felur í sér tvö viðföng. Fyrsta viðfangið er að skilgreina sniðið til að birta upplýsingar um kostnað af seldum vörum um framleidda vöru eða framleiðslupöntun. Sniðna skjámyndin nefnist kostnaðarskjal. Annað viðfangið er að skilgreina grunn útreiknings óbeins kostnaðar. Uppsetning kostnaðarskjals byggir á aðgerðum kostnaðarflokka til að birta upplýsingar og reikniformúlur óbeins kostnaðar. Tveimur viðföngum uppsetningar kostnaðarskjals er lýst í þessari grein.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostSheetDesigner, CostSheetCalculationFactor
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53201
ms.assetid: e7d72b43-3892-49ae-8821-9eede3f4d24a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f83c18bb8700e274bcf8cb369a7436a17450bf7
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979258"
---
# <a name="costing-sheets"></a>Kostnaðarskjöl

[!include [banner](../includes/banner.md)]

Uppsetning á kostnaðarskjali felur í sér tvö viðföng. Fyrsta viðfangið er að skilgreina sniðið til að birta upplýsingar um kostnað af seldum vörum um framleidda vöru eða framleiðslupöntun. Sniðna skjámyndin nefnist kostnaðarskjal. Annað viðfangið er að skilgreina grunn útreiknings óbeins kostnaðar. Uppsetning kostnaðarskjals byggir á aðgerðum kostnaðarflokka til að birta upplýsingar og reikniformúlur óbeins kostnaðar. Tveimur viðföngum uppsetningar kostnaðarskjals er lýst í þessari grein. 

Kostnaðarskjal er sniðsýning á upplýsingum um kostnað af vörum sem eru seldar fyrir framleidda vöru eða framleiðslupöntun. Þegar°kostnaðarskjal er sett upp er skilgrein snið fyrir upplýsingar og einnig°þarf að skilgreina grunn útreiknings óbeins kostnaðar. Uppsetning kostnaðarskjals byggir á aðgerðum kostnaðarflokka til að birta upplýsingar og reikniformúlur óbeins kostnaðar. Hér eru frekari upplýsingar um tvö viðföng uppsetningar kostnaðarskjals:
-   **Skilgreinið snið kostnaðarskjalsins.** Notandaskilgreint snið fyrir kostnaðarskjal tilgreinir niðurhlutun kostnaðar sem innihalda kostnað seldra vara fyrir framleiddra vöru. Til dæmis, geta upplýsingar um kostnað seldra vara verið sundurliðaðar í efni, vinnu og sameiginlegan kostnað byggt á kostnaðarflokkum. Þessir kostnaðarflokkur eru úthlutaðir á afurðir, kostnaðartegundir fyrir leiðaraðgerðir, og formúla útreikninga óbeins kostnaðar. Snið kostnaðarskjalsins þarfnast vanalega millisamtalna þegar margir kostnaðarflokkar hafa verið skilgreindir. Til dæmis er hægt að leggja saman marga kostnaðarflokka sem tengjast efni. Skilgreining á sniði kostnaðarskjals er valfrjáls, en ef reikna á út óbeinan kostnað verður að skilgreina snið kostnaðarskjals.
-   **Skilgreinið grundvöll útreiknings óbeins kostnaðar.** Óbeinn kostnaður endurspeglar framleiðslurekstrarkostnað sem er tengdur framleiðslu á°vöru. Hægt er að sýna reikniformúlur óbeins kostnaðar sem álag eða taxta. Álag birtir prósentu gildis, en taxti birtir upphæð fyrir hverja klukkustund fyrir leiðaaðgerð. Kostnaðarflokkur skilgreinir grundvöllinn fyrir reikniformúluna, til dæmis 100 prósent álag fyrir vinnukostnaðarflokk eða tímagjaldið 50,00 USD fyrir vélakostnaðarflokk. Til að hægt sé að skilgreina reikniformúlu og grunn kostnaðarflokks hennar verður uppsetning kostnaðarskjals að hafa kenni kostnaðarflokksins sem birtir óbeinan kostnað og val° á milli álags og taxta.

Færa verður inn hverja reikniformúlu sem kostnaðarfærslu. Kostnaðarfærslan samanstendur af tilgreindri kostnaðarútgáfu, álagsprósentu eða taxtaupphæð, grunni kostnaðarflokks, stöðu og upphafsdagsetningu. Þegar kostnaðarfærsla er upphaflega færð inn hefur hún stöðuna **Í biðstöðu** og°upphafsdagsetningu. Þegar kostnaðarfærsla er virkjuð er staðan uppfærð til að færslan sé núgildandi virk færsla og uppfærist gildisdagsetningu í virkjunardagsetningu. Kostnaðarfærslurnar geta tilgreint ákveðið svæði fyrir reikniformúlu háða svæði. Einnig er hægt að skilja svæðið í **Svæði** eftir autt til að tilgreina°að útreikningsjafnan sé formúla fyrir allt fyrirtækið. Kostnaðarfærslan getur samanstaðið af tilgreindri vöru eða vöruflokki þegar reikniformúlan hefur verið merkt sem fyrir hverja vöru. 

Núverandi virkar kostnaðarfærslur fyrir reikniformúlur°óbeins kostnaðar verða notaðar til að meta kostnað framleiðslupöntunar. Einnig eru þær notaðar til að reikna út raunkostnað sem tengist raunverulegri notkun á tíma og efni. Færslur biðkostnaðar verða notaðar í uppskriftarútreikningi á dagsetningu í framtíðinni. 

Tvær lokunarstefnur fyrir kostnaðarútgáfu ákvarða hvort hægt sé að viðhalda kostnaði í bið og hvort hægt sé að hefja kostnað í bið. Notaðu lokunarstefnur til að heimila gagnaviðhald og síðan til að koma í veg fyrir gagnaviðhald á kostnaðargögnum í kostnaðarútgáfu. 

Þegar búið er að skilgreina snið kostnaðarskjalsins og útreikninga óbeins kostnaðar verður að framkvæma sérstakar aðgerðir til að virkja og vista upplýsingarnar. Kostnaðarskjalið birtir snið fyrir allt fyrirtækið með því að birta í öllum tilfellum upplýsingar um kostnað seldra vara. 

Kostnaðarskjalið er birt sem hluti af síðunni **Reikna vörukostnað**. Kostnaðarskjalið getur verið birt fyrir útreiknaðar kostnaðarfærslur framleiddra vara á síðunni **Vöruverð**, eða fyrir útreikning ákveðnar pöntunar á síðunni **Niðurstöður úr útreikningi uppskrifta**. Það getur líka verið sýnt sem hluti af síðunni **Verðútreikningur**fyrir framleiðslupöntun.





