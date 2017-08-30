---
title: "Sýnishorn af rafrænni skýrslugerð ávísanir lánardrottins"
description: "Þetta efni inniheldur almennar upplýsingar um hvernig á að nota sýnishornasnið rafrænnar skýrslugerðar ávísana."
author: twheeloc
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: a8ba439ff643fce4811be9224a3edf96b2b9025c
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---

[!include[banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-check-formats"></a>Sýnishorn af ávísanasniðum skýrslugerðar

Hægt er að nota rafræna skýrslugerð (ER) til að sníða ávísanir lánardrottna. Mörg bankasértæk og ávísanaveitusértæk ávísunarsnið eru í boði á markaðnum. Sýnishorn af ávísunarsniðum hafa verið höfð með í ávísanagreiðslulíkani í verkfæri geymslustaðurinn ER. Þessi sýnishorn ávísana eru merkt **Ávísun í miðju (Bandaríkin)** og **Ávísun í efsta stubbi undir (Bandaríkin)**.

## <a name="what-check-formats-are-currently-supported"></a>Hvað ávísanasnið eru studd eins og stendur?

Alltaf skal fara eignasafnið Samnýtt eign í Microsoft Dynamics Lifecycle services (LCS) og skoða núverandi lista yfir tiltækar skrár af eignargerðinni **GER-skilgreining**. Næsti hluti „Hvað þarf að setja upp?“ veitir tengla í efnisatriði þar sem útskýrt er hvernig búa á til LCS-geymslu svo að hægt sé að fara yfir tiltækar stillingar og flytja inn valdar stillingar.

Microsoft Dynamics 365 til Fjármála og Aðgerðir Enterprise edition, inniheldur sýnishorn af sniði þar sem ávísunin er efst, með tvo kafla greiðslu. Það felur líka í sér sýnishorn snið þar sem ávísun er í miðju, á milli tveggja greiðsluhluta. Þessa sýnishornasnið samsvara ávísanasniðum Deluxe viðskipta.

## <a name="what-do-i-have-to-set-up"></a>Hvað þarf að setja upp?

- Áður en hægt er að prenta ávísanir með því að nota rafræna skýrslugerð verður a.m.k. ein virk skilgreining ávísunar flutt í stillingar á rafrænum skýrslum. Hægt er að skoða leiðbeiningar í [Niðurhal skilgreininga fyrir rafræna skýrslugerð af Lifecycle Services](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs)
- Þegar stilltar eru ávísanir Lausafjár og stjórnun banka fyrir bankareikninginn skal velja gátreitinn **Almenn rafræn útflutningssnið** og velja síðan viðeigandi ávísunarsnið og útflutning skilgreiningarsniðið.
- Einnig þarf að tilgreina fjölda innborgunarseðlalína sem verða prentaðar á greiðslu. Gangið úr skugga um að taka með hausar raða þegar þessi tala er reiknuð út. Fyrir tvö sýnishorn ávísunarsniða er ráðlagður línufjöldi fylgiseðils 17. Hins vegar verður þessi tala breytileg eftir ávísunarbirgðum og prentarareklum.
- Ráðlagt er að prenta ávísanaprufu til að villuleita útlit ávísunarinnar. Til að prenta ávísanaprufu skal velja valkostinn **Prentprufa**. Sýnishorn ávísanasniða virkar best þegar **Framlegð** er stillt á **Ekkert** í ítarlega prentara eiginleikar fyrir Microsoft Excel. Eftir að ávísunarprufan hefur verið mynduð gera breytingar á úttakið í Excel og skilgreina útliti síðu þannig að framlegð allra eru stilltir á **0** (núll). Berðu saman ávísanaprufuna við ávísanabirgðirnar og lagaðu stillingarnar þangað til að þú ert ánægð(ur) með niðurröðina.
- Þegar greiðslur eru myndaðar fyrir skilgreindan bankareikning í greiðslubók verða ávísanirnar prentaðar með sniði sem tilgreint er.

Nánari upplýsingar eru í [Breyta sniði rafrænnar skýrslugerðar](/dynamics365/unified-operations/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template).

