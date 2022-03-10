---
title: Sýnishorn af rafrænni skýrslugerð ávísanir lánardrottins
description: Þetta efni inniheldur almennar upplýsingar um hvernig á að nota sýnishornasnið rafrænnar skýrslugerðar ávísana.
author: sunfzam
ms.date: 06/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.assetid: ''
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 2e1aa349b505713d0502aa90ddd5c3caff1f083c
ms.sourcegitcommit: e40a9fac5bac9f57a6dcfe73a1f21856eab9b6a9
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/02/2021
ms.locfileid: "7595180"
---
# <a name="electronic-reporting-sample-vendor-checks"></a>Sýnishorn af rafrænni skýrslugerð ávísanir lánardrottins

[!include [banner](../includes/banner.md)]

Hægt er að nota rafræna skýrslugerð (ER) til að sníða ávísanir lánardrottna. Mörg bankasértæk og ávísanaveitusértæk ávísunarsnið eru í boði á markaðnum. Sýnishorn af ávísunarsniðum hafa verið höfð með í ávísanagreiðslulíkani í verkfæri geymslustaðurinn ER. Þessi sýnishorn ávísana eru merkt **Ávísun í miðju (Bandaríkin)** og **Ávísun í efsta stubbi undir (Bandaríkin)**.

## <a name="what-check-formats-are-currently-supported"></a>Hvað ávísanasnið eru studd eins og stendur?

Alltaf skal fara eignasafnið Samnýtt eign í Microsoft Dynamics Lifecycle Services (LCS) og skoða nýjasta lista yfir tiltækar skrár af eignargerðinni **GER-skilgreining**. Næsti hluti „Hvað þarf að setja upp?“ veitir tengla í efnisatriði þar sem útskýrt er hvernig búa á til LCS-geymslu svo að hægt sé að fara yfir tiltækar stillingar og flytja inn valdar stillingar.

Microsoft Dynamics 365 Finance inniheldur sýnisnið þar sem ávísunin er efst og síðan fylgja tveir greiðsluhlutar. Það felur líka í sér sýnishorn snið þar sem ávísun er í miðju, á milli tveggja greiðsluhluta. Þessa sýnishornasnið samsvara ávísanasniðum Deluxe viðskipta.

## <a name="what-do-i-have-to-set-up"></a>Hvað þarf að setja upp?

- Áður en hægt er að prenta ávísanir með því að nota rafræna skýrslugerð verður a.m.k. ein virk skilgreining ávísunar flutt í stillingar á rafrænum skýrslum. Hægt er að skoða leiðbeiningar í [Niðurhal skilgreininga fyrir rafræna skýrslugerð af Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
- Þegar stilltar eru ávísanir Lausafjár og stjórnun banka fyrir bankareikninginn skal velja gátreitinn **Almenn rafræn útflutningssnið** og velja síðan viðeigandi ávísunarsnið og útflutning skilgreiningarsniðið.
- Einnig þarf að tilgreina fjölda innborgunarseðlalína sem verða prentaðar á greiðslu. Gangið úr skugga um að taka með hausar raða þegar þessi tala er reiknuð út. Fyrir tvö sýnishorn ávísunarsniða er ráðlagður línufjöldi fylgiseðils 17. Hins vegar verður þessi tala breytileg eftir ávísunarbirgðum og prentarareklum.
- Ráðlagt er að prenta ávísanaprufu til að villuleita útlit ávísunarinnar. Til að prenta ávísanaprufu skal velja valkostinn **Prentprufa**. Sniðmát ávísunardæmis virka best þegar **Mörk** er stillt á **Engin** í ítarlegum eiginleikum prentara fyrir Microsoft Excel. Eftir að ávísunarprufan hefur verið mynduð gera breytingar á úttakið í Excel og skilgreina útliti síðu þannig að framlegð allra eru stilltir á **0** (núll). Berðu saman ávísanaprufuna við ávísanabirgðirnar og lagaðu stillingarnar þangað til að þú ert ánægð(ur) með niðurröðina.
- Þegar greiðslur eru myndaðar fyrir skilgreindan bankareikning í greiðslubók verða ávísanirnar prentaðar með sniði sem tilgreint er.

Nánari upplýsingar eru í [Breyta sniði rafrænnar skýrslugerðar](../../fin-ops-core/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
