---
title: Uppsetning ferðar með mörgum leggjum
description: Þetta efnisatriði lýsir því hvernig setja á upp ferðir með mörgum leggjum í gegnum Heildarkostnaður eininguna.
author: sherry-zheng
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMLegTable, ITMJourneyTable, ITMActivityTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-04
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: e1377b7453622e5bed711753fc2d99258d3c5951
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833762"
---
# <a name="multi-leg-journey-setup"></a>Uppsetning ferðar með mörgum leggjum

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig setja á upp ferðir með mörgum leggjum í gegnum **Heildarkostnaður** eininguna.

## <a name="legs"></a>Leggir

Leggir eru notaðir til að auðkenna aðskilda hluta ferðar. Hver leggur er búinn til með því að velja „til“ og „frá“ afhendingarhafnir og flutningsaðferðina sem er notuð fyrir þann legg. Hægt er að tengja afhendingartíma við hvern legg. Afhendingartímar geta hjálpað við að rekja sendingu og einnig er hægt að nota þá til að reikna út áætlaða afhendingardagsetningu á vörum í ferð. Þar að auki, þegar legg ferðar er lokið, er hægt að uppfæra stöðu á ferð, gámi og tengdra innkaupapöntunarlína með uppsetningu rakningarstýringar. Hægt er að nota leggi með einu sniðmáti ferðar eða endurnota þá af mörgum sniðmátum ferða. Hleðsla gáms, tollar og staðbundinn flutningur er yfirleitt sett upp sem leggir og einhver afhendingarhöfn er notuð fyrir það.

Til að vinnna með leggjum skal opna **Heildarkostnaður \> Uppsetning ferðar með mörgum leggjum \> Leggir**. Þar er hægt að skoða, opna, stofna og eyða færslum fyrir leggi. Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.

| Svæði | lýsing |
|---|---|
| Leggur | Færið inn einkvæmt auðkennisheiti/-númer ferðarinnar fyrir legginn. |
| lýsing | Færið inn lýsingu á legg ferðar. Yfirleitt auðkennir þessi lýsing „til“ og „frá“ hafnir eða skref á leiðinni. |
| Frá höfn | Sláið inn upprunastað varanna í leggnum. |
| Til hafnar | Sláið inn áfangastað varanna á leggnum. |
| Afhendingaraðferð | Sláið inn flutningsmáta fyrir legginn. |

## <a name="journey-templates"></a>Sniðmát ferða

Ferðasniðmát skilgreinir ferð með mörgum leggjum á milli tveggja hafna sem vörur fara á milli í ferð. Leggir ferðarinnar eru sameinaðir til að auðkenna þann tíma sem verður krafist fyrir vörur til að fara á milli upprunastaðs lánardrottins og endanlegs áfangastaðar vöruhúss. Þegar leggirnir eru settir í sniðmát ferðar í ákveðinni röð munu afhendingartímarnir gefa til kynna dagsetningu hvers leggs og stöðu ferðarinnar, gámsins og innkaupalínanna fyrir ferðina. [Stjórnstöð rakningar](delivery-information-setup.md) er notuð til að setja upp afhendingartíma sem tengajst hverjum legg sem myndar sniðmát ferðarinnar. Sniðmát ferðarinnar er einnig notað þegar sjálfvirkur kostnaður ferðar er settur upp. Þegar ferð er skilgreind er hægt að skilgreina kostnað sem tengist flutningi varanna á síðu sjálfvirks kostnaðar.

Til að vinna með ferðasniðmát skal fara í **Heildarkostnaður \> Uppsetning ferðar með mörgum leggjum \> Ferðasniðmát**. Þar er hægt að skoða, opna, stofna og eyða ferðasniðmátum.

Fyrir hvert sniðmát ferðar skal stilla eftirfarandi reiti í hausnum.

| Svæði | lýsing |
|---|---|
| Sniðmát ferðar | Færið inn einkvæmt auðkennisheiti/-númer ferðasniðmátsins. Ferðasniðmátið lýsir yfirleitt upprunastað og áfangastað ferðarinnar. |
| lýsing | Færið inn lýsingu á sniðmáti ferðarinnar. Lýsingin táknar yfirleitt „til“ og „frá“ hafnir og hvers kyns ferð er um að ræða. |

Í hlutanum **Línur** skal bæta við línu fyrir hvernn legg ferðarinnar og raða línunum í rétta röð. Notið örvarnar **Upp** og **Niður** á tækjastikunni til að breyta röð línanna. Eftirfarandi tafla lýsir svæðunum sem eru tiltæk fyrir hverja lína.

| Svæði | lýsing |
|---|---|
| Leggur | Veljið legg til að bæta við ferðina. |
| lýsing | Lýsing á leggnum. |
| Frá höfn | Höfnin sem er upprunastaður varanna í leggnum. Þessi höfn er „til“ höfn sem er notuð til að ákvarða sjálfvirkan kostnað ferðar. |
| Til hafnar | Höfn endanlegs áfangastaðar fyrir vörurnar í leggnum. |
| Afhendingarmáti | Afhendingarmátinn sem er notaður fyrir legginn. |
| Ferð frá höfn | Ef höfnin sem er tilgreind fyrir legginn er notuð til að ákvarða sjálfvirkan kostnað skal velja þennan gátreit til að auðkenna hann sem „ferð frá“ höfn. Þessi höfn verður sýnd í haus ferðarinnar. |
| Ferð til hafnar | Ef höfnin sem er tilgreind fyrir legginn er notuð til að ákvarða sjálfvirkan kostnað skal velja þennan gátreit til að auðkenna hann sem „ferð til“ höfn. Þessi höfn verður sýnd í haus ferðarinnar. |
| Flutningsfyrirtæki | Veljið flutningsfyrirtækið sem notað er fyrir legginn. |

## <a name="activities"></a>Verkþættir

Stillingarnar á síðunni **Verkþættir** gefa upp gerðir verkþátta sem geta átt sér stað á höfn áfangastaðar fyrir legginn. Notendur sem vinna á síðunni **Allir gámar** geta valið úr þessum gildum þegar þeir leggja mat á tímalengd hvers verkþáttar og skrá rauntíma til samanburðar.

Til að setja upp verkþætti skal fara í **Heildarkostnaður \> Uppsetning ferðar með mörgum leggjum \> Verkþættir**. Þar er hægt að bæta við, fjarlægja og breyta aðgerðum með því að nota hnappana á aðgerðarúðunni.

Eftirfarandi tafla lýsir reitinum sem eru tiltæk fyrir hverja aðgerð í hnitanetinu.

| Svæði | lýsing |
|---|---|
| Aðgerð | Heiti verkþáttarins. |
| lýsing | Lýsing á verkþættinum. |
| Flutningsfyrirtæki | Lánardrottnalykill flutningsfyrirtækisins sem tengist verkþættinum. |
