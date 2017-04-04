---
title: "Fjárhagsvíddir"
description: "Þessi grein útskýrir mismunandi gerðir fjárhagsvídda og hvernig þær eru settar upp."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: DimensionDetails, DimensionValueDetails, SysTranslationDetail
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 25871
ms.assetid: af54621c-c8be-4b72-b6df-dcf886c40ce4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: f849b98cac88d182875aca88aaf04cd3575ed99f
ms.lasthandoff: 03/31/2017


---

# <a name="financial-dimensions"></a>Fjárhagsvíddir

Þessi grein útskýrir mismunandi gerðir fjárhagsvídda og hvernig þær eru settar upp.

Nota skal skjámyndina fjárhagsvíddir til að stofna fjárhagsvíddir sem nota má sem hluta lykils fyrir bókhaldslykla. Til eru tvær gerðir fjárhagsvídda, sérsniðnar víddir og afritaðar víddir. Sérsniðnar víddir eru samnýttar á milli lögaðila og gildi eru færð inn og þeim stjórnað af notanda. Afritaðar víddir eru víddir hvers gildi eru skilgreind annars staðar í kerfinu, eins og Viðskiptavinum eða Verslunum. Sumar afritaðar víddir eru samnýttar á milli lögaðila og sumar afritaðar víddir eru bundnar fyrirtækjum. 

Eftir að búið er að stofna fjárhagsvíddir skal nota síðuna fjárhagsvíddargildi til að úthluta fleiri eiginleikum fyrir hverja fjárhagsvídd. 

Þó að hægt er að nota fjárhagsvíddir stendur lögaðila án þess að stofna lögaðila í Microsoft Dynamics 365 aðgerða fjárhagsvíddir ekki eru kostnaðarjafnaðar hannað til að sem um aðsetur eða viðskiptaferli þarf lögaðila. Interunit úthlutunarkostnaðar í Microsoft Dynamics 365 aðgerða er hannað til aðsetur aðeins bókhaldsfærslur sem eru stofnaðar eftir hverja færslu. 

Áður en að setja upp fjárhagsvíddir sem lögaðila , skal meta viðskiptaferlunum í eftirfarandi svæði til að ákvarða ef þessi uppsetning mun gagnast fyrir fyrirtækið:

-   Birgðir
-   Sölu og innkaup milli fjárhagsvíddir og lögaðila
-   útreikningur VSK og skýrslugerð
-   Aðgerðaskýrslugerð

Nokkur dæmi um takmarkanirnar innifela eftirfarandi:

-   Hægt er að nota virkni virðisaukaskatts ekki með fjárhagsvíddum, aðeins við lögaðila.
-   Sumar skýrslur hafa ekki fjárhagsvíddir, svo ekki er alltaf hægt að gefa skýrsluna eftir fjárhagsvídd nema þessar skýrslur hafi verið breytt.

**Custom dimensions** 

Stofna notandaskilgreindur fjárhagsvídd, í svæðinu Nota virði frá valið &lt;Sérsniðna vídd&gt;. Einnig er hægt að tilgreina lykilsíu til að takmarka magn og gerð upplýsinga sem hægt er að færa inn víddargildi fyrir. Hægt er að færa inn stafi sem eru þeir sömu og fyrir hvert víddargildi eins og stafi eða bandstrik. Einnig er hægt að færa inn númer formerki (\#) og og-merki (&) og staðgenglar fyrir bókstafi og tölustafi breytast í hvert sinn sem stofnuð er víddargildi. Nota sem númerstákn (\#) sem frátakara tölu-og í ampersand (&) frátakara fyrir bréf sem. 

**Dæmi** 

Til að takmarka víddargildi þrjár tölur og bókstafi CC, er að færa inn CC -\#\#\# og snið sniðmáts. Þetta svæði er tiltækt þegar valið &lt;Sérsniðna vídd &gt;í svæðinu Nota virði frá. 

**Afrita einingu víddir** 

Til að stofna til að afrita einingu fjárhagsvídd, í svæðinu Nota virði frá, veljið kerfisskilgreindar einingar sem byggja á fjárhagsvídd á. Fjárhagsvíddargildi eru stofnuð úr þessu vali. Til dæmis skal velja Verk tila ð stofna víddargildi fyrir verk. Víddargildi verða stofnuð fyrir hvert heiti verks. Víddargildi síðan sýnir gildi fyrir eininguna og ef þær eru bundin fyrirtæki, fyrirtækið fyrir gildið. 

**Virkjun vídda** 

Virkjun fjárhagsvíddar uppfærir töflu með fjárhagsvíddarheitinu og fjarlægir eyddum víddum. Hægt er að færa inn víddargildi áður en fjárhagsvídd er virkjuð en fjárhagsvídd er ekki hægt að nota fyrr en hún er virkjuð. Til dæmis geturðu ekki gætt við fjárhagsvídd við lykilskipulag þar til fjárhagsvídd hefur verið virkjuð. Smella á virkja uppfærir allar víddir með stöðubreytingar. 

**Translations** 

Þýðing síðan Texta gerir kleift að færa inn texta sem birtist á mismunandi tungumálum fyrir valda fjárhagsvídd. þýðingasíðan aðallykils er þar sem þú getur færa inn texta til að birtast á mismunandi tungumálum fyrir aðallykill. 

**Legal entity overrides** 

Ekki allar víddir eru gildar fyrir alla lögaðila og sumar má aðeins vera máli fyrir ákveðið tímabil. Í þessum aðstæðum Lögaðili hnekkir getur verið notað til að auðkenna hvaða fyrirtæki ætti ekki að nota víddir fyrir, hver er eigandi og tímabilið sem víddin er virk.




