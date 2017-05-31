---
title: "Fjárhagsvíddir"
description: "Þessi grein útskýrir mismunandi gerðir fjárhagsvídda og hvernig þær eru settar upp."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 01f189b8de3f0cc707dcc54f4cde75aed95b8e3f
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="financial-dimensions"></a>Fjárhagsvíddir

[!include[banner](../includes/banner.md)]


Þessi grein útskýrir mismunandi gerðir fjárhagsvídda og hvernig þær eru settar upp.

Nota skal skjámyndina fjárhagsvíddir til að stofna fjárhagsvíddir sem nota má sem hluta lykils fyrir bókhaldslykla. Til eru tvær gerðir fjárhagsvídda, sérsniðnar víddir og afritaðar víddir. Sérsniðnar víddir eru samnýttar á milli lögaðila og gildi eru færð inn og þeim stjórnað af notanda. Afritaðar víddir eru víddir hvers gildi eru skilgreind annars staðar í kerfinu, eins og Viðskiptavinum eða Verslunum. Sumar afritaðar víddir eru samnýttar á milli lögaðila og sumar afritaðar víddir eru bundnar fyrirtækjum. 

Eftir að búið er að stofna fjárhagsvíddir skal nota síðuna fjárhagsvíddargildi til að úthluta fleiri eiginleikum fyrir hverja fjárhagsvídd. 

Þó að þú getir notað fjárhagsvíddir til að tákna lögaðila án þess að stofna lögaðila í Microsoft Dynamics 365 for Operations, eru fjárhagsvíddir ekki hannaðar til að takast á við reksturs- eða viðskiptaþarfir lögaðila. Millieiningabókhaldseiginleikinn í Microsoft Dynamics 365 fyrir Operations er hannaður til að eiga aðeins við bókhaldsfærslur sem eru stofnaðar fyrir hverja færslu. 

Áður en að setja upp fjárhagsvíddir sem lögaðila , skal meta viðskiptaferlunum í eftirfarandi svæði til að ákvarða ef þessi uppsetning mun gagnast fyrir fyrirtækið:

-   Birgðir
-   Sölu og innkaup milli fjárhagsvíddir og lögaðila
-   útreikningur VSK og skýrslugerð
-   Aðgerðaskýrslugerð

Nokkur dæmi um takmarkanirnar innifela eftirfarandi:

-   Hægt er að nota virkni virðisaukaskatts ekki með fjárhagsvíddum, aðeins við lögaðila.
-   Sumar skýrslur hafa ekki fjárhagsvíddir, svo ekki er alltaf hægt að gefa skýrsluna eftir fjárhagsvídd nema þessar skýrslur hafi verið breytt.

**Sérsniðnar víddir** 

Til að stofna notandaskilgreinda fjárhagsvídd, í Nota gildi frá reit skal velja &lt; Sérsniðin vídd &gt;. Einnig er hægt að tilgreina lykilsíu til að takmarka magn og gerð upplýsinga sem hægt er að færa inn víddargildi fyrir. Hægt er að færa inn stafi sem eru þeir sömu og fyrir hvert víddargildi eins og stafi eða bandstrik. Einnig er hægt að slá inn tölumerki (\#) og og-merki (&) sem frátakara fyrir stafi og tölur sem breytast í hvert skipti sem víddargildi er stofnað. Notaðu tölumerki (\#) sem frátakara fyrir tölu og og-merki (&) sem frátakara fyrir staf. 

**Dæmi** 

Til að takmarka víddargildi við stafina CC og þrjár tölur færirðu inn CC-\#\#\# sem sniðsíu. Þessi reitur er tiltækt aðeins þegar valið &lt; Sérsniðin vídd &gt; í reitur Nota gildi frá. 

**Einingarstuddar víddir** 

Að búa til einingarstudd fjárhagsvíddir, í svæðinu Nota gildi frá, veljið kerfisskilgreindar einingar til að byggja fjárhagsvídd á. Fjárhagsvíddargildi eru stofnuð úr þessu vali. Til dæmis skal velja Verk tila ð stofna víddargildi fyrir verk. Víddargildi verða stofnuð fyrir hvert heiti verks. Víddargildi síðan sýnir gildi fyrir eininguna og ef þær eru bundin fyrirtæki, fyrirtækið fyrir gildið. 

**Notkun vídda** 

Virkjun fjárhagsvíddar uppfærir töflu með fjárhagsvíddarheitinu og fjarlægir eyddum víddum. Hægt er að færa inn víddargildi áður en fjárhagsvídd er virkjuð en fjárhagsvídd er ekki hægt að nota fyrr en hún er virkjuð. Til dæmis geturðu ekki gætt við fjárhagsvídd við lykilskipulag þar til fjárhagsvídd hefur verið virkjuð. Smella á virkja uppfærir allar víddir með stöðubreytingar. 

**Þýðingar** 

Textaþýðingasíðan leyfir þér að færa inn texta til að birtast á mismunandi tungumálum fyrir valda fjárhagsvídd. þýðingasíðan aðallykils er þar sem þú getur færa inn texta til að birtast á mismunandi tungumálum fyrir aðallykill. 

**Hnekkingar lögaðila** 

Ekki allar víddir eru gildar fyrir alla lögaðila og sumar eiga aðeins við fyrir ákveðið tímabil. Í þessum aðstæðum Lögaðili hnekkir getur verið notað til að auðkenna hvaða fyrirtæki ætti ekki að nota víddir fyrir, hver er eigandi og tímabilið sem víddin er virk.






