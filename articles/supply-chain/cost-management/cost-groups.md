---
title: Kostnaðarflokkar
description: Kostnaðarflokkar veita grunn fyrir sundurliðun og greiningu kostnaðarframlegðar í útreiknuðum kostnaði framleiddrar vöru, svo sem kostnaðarframlegðar fyrir efni, vinnu og óbeinan kostnað. Sundurliðun kostnaðarflokka hefur nokkur samheiti í framleiðsluumhverfi, til dæmis niðurbrot kostnaðar eða flokkun kostnaðar.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCostGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 50871
ms.assetid: 1855f744-f73f-4fa8-8290-a7ee126d368b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b60c8a353a4c545cf5c1f1b1e5565d0d7e2a5bb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7572147"
---
# <a name="cost-groups"></a>Kostnaðarflokkar

[!include [banner](../includes/banner.md)]

Kostnaðarflokkar veita grunn fyrir sundurliðun og greiningu kostnaðarframlegðar í útreiknuðum kostnaði framleiddrar vöru, svo sem kostnaðarframlegðar fyrir efni, vinnu og óbeinan kostnað. Sundurliðun kostnaðarflokka hefur nokkur samheiti í framleiðsluumhverfi, til dæmis niðurbrot kostnaðar eða flokkun kostnaðar. 

Sundurliðun kostnaðarflokka hefur nokkur samheiti í framleiðsluumhverfi, til dæmis niðurbrot kostnaðar eða flokkun kostnaðar. Hlutun kostnaðarflokks getur þjónað ýmsum tilgangi. Hér eru nokkur dæmi:

-   Það getur Sundurliðað kostnaðar fyrir ólíkar efnisgerðir, til dæmis innihald og umbúðir fyrir dósavöru, byggð á þeim kostnaðarflokkum sem eru tengdir vörunum.
-   Það getur Sundurliðað kostnaðar fyrir ólíkar gerðir rekstrartilfanga, til dæmis ólíkar gerðir af vinnu og vélum, byggð á kostnaðarflokkum tengdum kostnaðartegundum sem eru venslaðar rekstrartilföngum og leiðaaðgerðum.
-   Það getur Sundurliðað kostnað fyrir uppsetningartíma og keyrslutíma í leiðaaðgerðum, byggð á kostnaðarflokkum tengdum kostnaðartegundum sem eru venslaðar leiðaaðgerðunum.
-   Það getur Sundurliðað kostnað fyrir mismunandi gerðir rekstrarkostnaðar, til dæmis óbeinan framleiðslukostnað vegna vinnu og véla, byggð á kostnaðarflokkum sem tengdir eru óbeinum kostnaði í uppsetningu kostnaðarskjals.
-   Það getur þjónað sem grundvöllur útreikninga á ýmis konar rekstrarkostnaði við framleiðslu í uppsetningu kostnaðarskjals. Þessi rekstrarkostnaður getur tekið með mismunandi rekstrarkostnaði sem tengist leiðarupplýsingum um rekstrartilföngum eða upplýsingar um uppsetningar- og keyrslutíma. framleiðslurekstrarkostnaður getur líka verið tengdur kostnaðarframlagi íhluta efnis, og það endurspeglar lean-framleiðsli heimspeki sem útrýmir þörfinni fyrir leiðaupplýsingar.

Sundurliðun kostnaðarflokka á við um útreiknaðan kostnað framleiddrar vöru hvort sem þeir byggjast á stöðluðum kostnaði eða áætluðum kostnaði. **Samantekt** síða sýnir þessa sundurliðun eftir kostnaðarflokki, stigi eða eftir bæði eftir kostnaðarflokks og stigs. 

Getan til að halda eftir kostnaðarflokkum þvert á mörg stig í framleiðsluskipulagi er þekkt sem *skipting*, Skipta á einungis við um framleiddar vörur sem nota birgðalíkan staðalkostnaðar. Ef skiptingar er ekki notuð, er kostnaður fyrir framleidda þætti meðhöndlaður sem efniskostnaðarframlag. Færibreytunni fyrir sundurliðun kostnaðar eftir undirbókar gefur til kynna að sundurliðun kostnaðarflokka varðveitt þvert á mörg stig í útreikningi staðlaðs kostnaðar. Hins vegar hafi regla engin stig, skiptingu kostnaðarflokks gildir aðeins um eins-stigs útreikninga. Til dæmis, , til dæmis **samantekt kostnaðar eftir kostnaðarflokki**, sýnir sundurliðun á kostnaðarflokki á mörgum stigum fyrir stöðluðum kostnaðarliði. 

Sundurliðun kostnaðarflokka getur líka átt við um frávik fyrir staðlaða kostnaðarvöru. Önnur birgðafæribreyta skilgreinir hvort frávik verða greind af kostnaðarflokkur, eða einfaldlega tekin saman. 

Hægt er að úthluta kostnaðarflokki gerð og hegðun í tilgangi fyrir aukalega sundurliðun.

-   **Gerð kostnaðarflokks** - Hverjum kostnaðarflokki verður að úthluta gerð kostnaðarflokkstil aða tilgreina að kostnaðarflokk gildir um beinu efni, beinni framleiðslu, beinni útvistun,eða að tilgreina hana sem óbeinni eða óskilgreindri. kostnaðarflokki sem er tilgreindur sem beint efni er hægt að úthluta á vörur. Kostnaðarflokki beinnar framleiðslu er hægt að úthluta til kostnaðartegunda. Hægt er að úthluta kostnaðarflokk beinnar útvistunar við afurðargerð þjónustu, sem gerir kleift að flokka kostnað sem tengist innkaupapöntun þjónustu til verkþátta undirverktaka . Óbeinum kostnaðarflokki er hægt að úthluta til óbeins kostnaðar fyrir álag eða taxta. Kostnaðarflokki sem er tilgreindur sem óskilgreindur er hægt að úthluta á vörur, kostnaðarflokk, eða óbeinn kostnaður Úthlutun á gerð kostnaðarflokks þjónar nokkur málefni. Fyrst, það takmarkar getuna til að úthluta kostnaðarflokki og skoða fellilista yfir viðeigandi kostnaðarflokka. Önnur, býður upp á viðbótar sundurliðun fyrir skýrslugerð. Þriðji, hún er notuð til að úthluta fjárhagslyklum fyrir frávik.
-   **Hegðun** − Hægt er að velja hegðun til að úthluta hverjum kostnaðarflokki en hún tilgreinir það hvort kostnaðarflokkurinn eigi við um fastan kostnað eða breytilegan kostnað. Kostnaðarflokkur með núllgildi hegðunar er meðhöndlaður sem breytilegur kostnaður Úthlutun hegðunar þjónar er eingöngu fyrir skýrslugerð. Til dæmis er hægt að birta kostnað með sundurliðun fasts og breytilegs kostnaðar á kostnaðarskjalinu og í skjámyndinni **samantekt kostnaðar eftir kostnaðarflokki**. Ef þú gefur upp hagnað-stilling prósenta á hverjum kostnaður hópinn BOM útreikning veitir leiðbeinandi söluverð, byggðri á kostnað plús-álagningar nálgun.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]