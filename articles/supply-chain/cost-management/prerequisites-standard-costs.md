---
title: "Forsendur fyrir staðalkostnaði"
description: "Þetta efnisatriði fjallar um grundvallarskref við notkun staðalkostnaðar."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e63f2b4289b640e601492425331ea8f3804d139a
ms.openlocfilehash: 4f505a2de89863d1a12d415795fdfb82b3557bc0
ms.contentlocale: is-is
ms.lasthandoff: 01/17/2018

---

# <a name="prerequisites-for-standard-costs"></a>Forsendur fyrir staðalkostnaði

[!include[banner](../includes/banner.md)]


Þetta efnisatriði fjallar um grundvallarskref við notkun staðalkostnaðar. Eftirfarandi skref fara eftir starfsemi fyrirtækisins. Til dæmis eru skrefin mismunandi fyrir umhverfi sem er ekki með framleiðslu, framleiðsluumhverfi sem notar ekki leiðir og framleiðsluumhverfi sem notar leiðir. 

Til að setja upp staðalkostnað skal fylgja þessum skrefum.

**1. Búa til vörulíkanaflokk fyrir staðalkostnað.**

Notaðu síðu **Vörulíkanaflokks** til að stofna nýjan flokk fyrir staðalkostnað og úthlutaðu birgðalíkani af **Staðalkostnaði**. Kennimerki vörulíkanaflokksins ætti að hafa einhverja þýðingu, eins og **St.kostn.**. Veldu gátreitina til að gefa til kynna að flokkurinn eigi að leyfa fjárhagslegar neikvæðar birgðir og að hann eigi að bóka efnislegar birgðir og fjárhagslegar birgðir. Þessi flokkur staðalkostnaðar verður úthlutaður vörum.

**2. Skilgreina fjárhagslykla sem tengjast frávikum í staðalkostnaði.** 

Notaðu síðuna **Bókhaldslyklar** til að skilgreina fjárhagslykla sem tengjast frávikum í staðalkostnaði. Skilgreina þarf þessa fjárhagslykla áður en hægt er að úthluta þeim á síðu **Bókunar**. Fjárhagslyklarnir geta endurspeglað vöruflokka og kostnaðarflokka.

**3. Úthluta fjárhagslyklum á vörubókanir sem tengjast frávikum í staðalkostnaði.** 

Notaðu síðu **Bókunar** til að úthluta fjárhagslyklum sem tengjast frávikum í staðalkostnaði. Þú getur tilgreint fjárhagslykil fráviks eftir vöru (eða vöruflokki) og eftir kostnaðarflokki (eða gerð kostnaðarflokks) eða þú getur tilgreint að fjárhagslykillinn eigi við um allar vörur og alla kostnaðarflokka. Þessir valkostir samsvara kostnaðartengslum fyrir töflur, flokka og allt. 

Áður en þú skilgreinir bókunarreglur á vörum skaltu nota síðuna **Færslusamsetningar** til að virkja kostnaðartengsl (fyrir töflur, flokka og allt).

**4. Skilgreina birgðafæribreytur sem tengjast staðalkostnaði.** 

-  Notaðu flipann **Uppskriftir** á síðunni **Birgðafæribreytur** til að skilgreina tvær kostnaðarstýrðar færibreytur sem tengjast staðalkostnaði. 

    -  Í reitnum **Sundurliðun kostnaðar** veldu **Ekkert** eða **Undirfjárhag**. Ef þú velur **Undirfjárhag** er sundurliðun kostnaðar *virk* sundurliðun kostnaðar. Virk sundurliðun kostnaðar er mikilvæg við útreikning, viðhald og yfirlit yfir sundurliðun kostnaðarflokka í margstiga uppbyggingu vöru fyrir staðalkostnaðarvörur. Þegar sundurliðun kostnaðar er virk getur þú skráð og greint birgðir, verk í vinnslu (WIP) og kostnaður seldra vara (COGS) fyrir hvern kostnaðarflokk í einstiga, margstiga eða heildarsniði. Þegar sundurliðun kostnaðar er virk, ef þú virkjar kostnað framleiddra vara, verður sundurliðun kostnaðarflokka geymd í kostnaðarfærslu vörunnar. 

    -  Ef þú velur **Ekkert** verður sundurliðun kostnaðarflokks ekki viðhaldið fyrir staðalkostnaðarvörur. Með öðrum orðum, staðalkostnaður framleiddrar vöru verður reiknaður og honum viðhaldið sem einni upphæð, án sundurliðunar kostnaðarflokka. Kostnaðarframlegð framleiddra hluta verður safnað saman í eina upphæð.

-  Í svæðinu **Frávik frá staðli** skaltu velja **Samantekt** eða **Fyrir hvern kostnaðarflokk**. Ef þú velur **Fyrir hvern kostnaðarflokk** getur þú greint frávik á innkaupaverði og frávik á framleiðslu eftir kostnaðarflokki. Þú getur einnig greint fjórar gerðir frávika á framleiðslu: lotustærð, magn, verð og staðgengilsfrávik. Ef þú velur **Samantekt** getur þú ekki greint frávik eftir kostnaðarflokki og þú getur ekki greint fjórar gerðir frávika á framleiðslu. Þú getur bara skoðað samantekt á frávikum framleiðslu.

-  Reglan um frávik frá staðli virkar óháð reglunni um sundurliðun kostnaðar. Með öðrum orðum er hægt að velja **Ekkert** sem reglu fyrir sundurliðun kostnaðar og velja frávik fyrir hvern kostnaðarhóp, þannig að frávik framleiðslu eftir kostnaðarflokki verður áfram greint.

**5. Stofna kostnaðarútgáfur fyrir staðlalkostnað.** 

Notaðu síðuna **Uppsetningu kostnaðarútgáfu** til að stofna eina eða fleiri kostnaðarútgáfur fyrir staðalkostnað. Úthluta þarf hverri kostnaðarútgáfu gerð kostnaðar sem **Staðalkostnað** og verður að leyfa efni að innihalda kostnaðargögn.

**6. Undirbúa núverandi viðskiptavin til að nota staðalkostnað.** 

Viðskiptavinir sem vilja til að breyta núverandi vörum sínum yfir í birgðalíkan staðalkostnaðar verða að nota síðuna **Umreikningur á staðalkostnaði**.


<a name="related-topics"></a>Tengd efnisatriði
--------

[Yfirlit yfir umreikning staðalkostnaðar](standard-cost-conversion-overview.md)

