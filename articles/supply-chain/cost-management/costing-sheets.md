---
title: Kostnaðarskjöl
description: Uppsetning á kostnaðarskjali felur í sér tvö viðföng. Fyrsta viðfangið er að skilgreina sniðið til að birta upplýsingar um kostnað af seldum vörum um framleidda vöru eða framleiðslupöntun. Sniðna skjámyndin nefnist kostnaðarskjal. Annað viðfangið er að skilgreina grunn útreiknings óbeins kostnaðar. Uppsetning kostnaðarskjals byggir á aðgerðum kostnaðarflokka til að birta upplýsingar og reikniformúlur óbeins kostnaðar. Tveimur viðföngum uppsetningar kostnaðarskjals er lýst í þessari grein.
author: AndersGirke
ms.date: 11/18/2021
ms.topic: article
ms.search.form: CostSheetDesigner, CostSheetCalculationFactor
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53201
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64b8a9b8b29193f25e706e52424de2af3454aec8
ms.sourcegitcommit: f11ad8d7ee8a4d2ee1a1bb601622b50e14955c4a
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2021
ms.locfileid: "7825359"
---
# <a name="costing-sheets"></a>Kostnaðarskjöl

[!include [banner](../includes/banner.md)]

Uppsetning á kostnaðarskjali felur í sér tvö viðföng. Fyrsta viðfangið er að skilgreina sniðið til að birta upplýsingar um kostnað af seldum vörum um framleidda vöru eða framleiðslupöntun. Sniðna skjámyndin nefnist kostnaðarskjal. Annað viðfangið er að skilgreina grunn útreiknings óbeins kostnaðar. Uppsetning kostnaðarskjals byggir á aðgerðum kostnaðarflokka til að birta upplýsingar og reikniformúlur óbeins kostnaðar. Tveimur viðföngum uppsetningar kostnaðarskjals er lýst í þessari grein. 

Eftirfarandi tafla sýnir þau öryggishlutverk sem eru utan kassa sem hafa aðgang að kostnaðarblöðum, þar á meðal aðgangsstigið sem veitt er hverju hlutverki með sjálfgefnum stillingum.

| Hlutverk | Aðgangur
|---|---|
| Bókhaldsstjóri | Breyta |
| Starfsmaður birgðabókhaldara | Skoða |
| Bókhaldari birgða | Skoða |

Kostnaðarskjal er sniðsýning á upplýsingum um kostnað af vörum sem eru seldar fyrir framleidda vöru eða framleiðslupöntun. Þegar°kostnaðarskjal er sett upp er skilgrein snið fyrir upplýsingar og einnig°þarf að skilgreina grunn útreiknings óbeins kostnaðar. Uppsetning kostnaðarskjals byggir á aðgerðum kostnaðarflokka til að birta upplýsingar og reikniformúlur óbeins kostnaðar. Hér eru frekari upplýsingar um tvö viðföng uppsetningar kostnaðarskjals:

- **Skilgreinið snið kostnaðarskjalsins.** Notandaskilgreint snið fyrir kostnaðarskjal tilgreinir niðurhlutun kostnaðar sem innihalda kostnað seldra vara fyrir framleiddra vöru. Til dæmis, geta upplýsingar um kostnað seldra vara verið sundurliðaðar í efni, vinnu og sameiginlegan kostnað byggt á kostnaðarflokkum. Þessir kostnaðarflokkur eru úthlutaðir á afurðir, kostnaðartegundir fyrir leiðaraðgerðir, og formúla útreikninga óbeins kostnaðar. Snið kostnaðarskjalsins þarfnast vanalega millisamtalna þegar margir kostnaðarflokkar hafa verið skilgreindir. Til dæmis er hægt að leggja saman marga kostnaðarflokka sem tengjast efni. Skilgreining á sniði kostnaðarskjals er valfrjáls, en ef reikna á út óbeinan kostnað verður að skilgreina snið kostnaðarskjals.
- **Skilgreinið grundvöll útreiknings óbeins kostnaðar.** Óbeinn kostnaður endurspeglar framleiðslurekstrarkostnað sem er tengdur framleiðslu á°vöru. Hægt er að sýna reikniformúlur óbeins kostnaðar sem álag eða taxta. Álag birtir prósentu gildis, en taxti birtir upphæð fyrir hverja klukkustund fyrir leiðaaðgerð. Kostnaðarflokkur skilgreinir grundvöllinn fyrir reikniformúluna, til dæmis 100 prósent álag fyrir vinnukostnaðarflokk eða tímagjaldið 50,00 USD fyrir vélakostnaðarflokk. Til að hægt sé að skilgreina reikniformúlu og grunn kostnaðarflokks hennar verður uppsetning kostnaðarskjals að hafa kenni kostnaðarflokksins sem birtir óbeinan kostnað og val° á milli álags og taxta.

Færa verður inn hverja reikniformúlu sem kostnaðarfærslu. Kostnaðarfærslan samanstendur af tilgreindri kostnaðarútgáfu, álagsprósentu eða taxtaupphæð, grunni kostnaðarflokks, stöðu og upphafsdagsetningu. Þegar kostnaðarfærsla er upphaflega færð inn hefur hún stöðuna **Í biðstöðu** og°upphafsdagsetningu. Þegar kostnaðarfærsla er virkjuð er staðan uppfærð til að færslan sé núgildandi virk færsla og uppfærist gildisdagsetningu í virkjunardagsetningu. Kostnaðarfærslurnar geta tilgreint ákveðið svæði fyrir reikniformúlu háða svæði. Einnig er hægt að skilja svæðið í **Svæði** eftir autt til að tilgreina°að útreikningsjafnan sé formúla fyrir allt fyrirtækið. Kostnaðarfærslan getur samanstaðið af tilgreindri vöru eða vöruflokki þegar reikniformúlan hefur verið merkt sem fyrir hverja vöru. 

Núverandi virkar kostnaðarfærslur fyrir reikniformúlur°óbeins kostnaðar verða notaðar til að meta kostnað framleiðslupöntunar. Einnig eru þær notaðar til að reikna út raunkostnað sem tengist raunverulegri notkun á tíma og efni. Færslur biðkostnaðar verða notaðar í uppskriftarútreikningi á dagsetningu í framtíðinni. 

Tvær lokunarstefnur fyrir kostnaðarútgáfu ákvarða hvort hægt sé að viðhalda kostnaði í bið og hvort hægt sé að hefja kostnað í bið. Notaðu lokunarstefnur til að heimila gagnaviðhald og síðan til að koma í veg fyrir gagnaviðhald á kostnaðargögnum í kostnaðarútgáfu. 

Þegar búið er að skilgreina snið kostnaðarskjalsins og útreikninga óbeins kostnaðar verður að framkvæma sérstakar aðgerðir til að virkja og vista upplýsingarnar. Kostnaðarskjalið birtir snið fyrir allt fyrirtækið með því að birta í öllum tilfellum upplýsingar um kostnað seldra vara. 

Kostnaðarskjalið er birt sem hluti af síðunni **Reikna vörukostnað**. Kostnaðarskjalið getur verið birt fyrir útreiknaðar kostnaðarfærslur framleiddra vara á síðunni **Vöruverð**, eða fyrir útreikning ákveðnar pöntunar á síðunni **Niðurstöður úr útreikningi uppskrifta**. Það getur líka verið sýnt sem hluti af síðunni **Verðútreikningur** fyrir framleiðslupöntun.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
