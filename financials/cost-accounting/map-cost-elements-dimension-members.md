---
title: "Varpa öðrum víddarstökum kostnaðareiningar á almennt safn víddarstaka"
description: "Vörpun mismunandi víddarstök kostnaðareiningar á almenn sett víddarstök kostnaðareiningar, þannig sameinar þú gögn í almennt snið í greiningartilgangi."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-11-01 13 - 45 - 07
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: a1e9817b6ee596ad516531d7597a2a39e115749c
ms.lasthandoff: 03/31/2017


---

# <a name="map-different-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a>Varpa öðrum víddarstökum kostnaðareiningar á almennt safn víddarstaka

Vörpun mismunandi víddarstök kostnaðareiningar á almenn sett víddarstök kostnaðareiningar, þannig sameinar þú gögn í almennt snið í greiningartilgangi.

Ef þú ert alþjóðlegt fyrirtæki og uppfylli lögboðnar kröfur um bókhald, gætir þú notað margar bókhaldslykla. Þegar þú flytur inn víddarstök kostnaðareiningar úr mismunandi bókhaldslyklum, geturðu endað með blöndu lykla. Hins vegar gætu þessir reikningar í raun hafa sömu náttúru, og þú gætir vilja greina og úthluta kostnaði fyrir þá með því að nota sameiginlegt snið.

## <a name="map-cost-element-dimension-members-to-a-common-format"></a>Varpa víddarstök kostnaðareiningar á almennt snið
Eftirfarandi dæmi sýnir hvernig þú, sem fjármálastjóri, getur stofnað nýja vídd kostnaðareiningar í kostnaðarbókhaldi sem varpar víddarstök kostnaðareiningar úr Bandarísk skipulag bókhaldslykils og Franska skipulag bókhaldslykils í almenn sett víddarstaka kostnaðareiningar. Síðan er hægt að nota almennt safn víddarstök kostnaðareiningar til að greina kostnaðargögn úr tveimur lögaðila í fjárhag kostnaðarbókhalds.

| Uppspretta: Bandaríkin bókhaldslykil                                          | Uppspretta: franska bókhaldslykil                                          | Ný almennt sett víddarstaka kostnaðareiningar                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Innflutt víddarstök kostnaðareiningar úr bandaríska bókhaldslykli | Innflutt víddarstök kostnaðareiningar úr franska bókhaldslykli | Varpa bandaríska og franska víddarstök kostnaðareiningar á almennt sett |
| 5001: Sala                                                           | 5001: Sala og auglýsingar                                               | 5000: Sala og auglýsingar                                             |
| 5030: Auglýsingar                                                     | 6390: birgðakaup\*                                                    | 7000: Ræstikostnaður                                                 |
| 7001: Ræstikostnaður                                               | 7001: Ferðakostnaður                                                      | 7001: Ferðakostnaður                                                   |

\*Franska víddarstak kostnaðareiningar fyrir birgðakaup er ekki varpað.

## <a name="currency-conversion"></a>Umreikningur gjaldmiðils
Mismunandi bókhaldslykil sem þú notar gætu setja upp til að nota aðra gjaldmiðla. Í þessu tilfelli gætið þess að tilgreina umreikningur fyrirtækisgjaldmiðils þannig að kostnaðargögn er unnin með réttum gjaldmiðli, eins og skilgreint er í fjárhag kostnaðarbókhalds þar sem víddarstök kostnaðareiningar eru notaðar. Í fyrrgreint dæmi, ef Bandarískum dollurum (USD) eru notaðar í fjárhag kostnaðarbókhalds verður að stofna gjaldmiðilsumreikning frá USD að evrur (EUR) til að vinna færslur fyrir varpaðar víddarstök kostnaðareiningar .

## <a name="update-mappings-at-any-time"></a>Uppfæra varpanir hvenær sem er.
Hægt er að uppfæra skilgreiningar vörpunar fyrir vídd kostnaðareiningar hvenær sem er. Þar sem varpanir eru ekki virkjaðar samkvæmt dagsetningum, eru breytingar notaðar í næsta sinn sem þú vinnur úr kostnaðarfærslur eða keyra kostnaðarútreikninga.


