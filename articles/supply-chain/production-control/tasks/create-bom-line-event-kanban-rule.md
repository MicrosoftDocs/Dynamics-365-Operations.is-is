--- 
title: "Stofna tilviksreglu kanbans fyrir uppskriftarlínu"
description: "Þetta verk leggur áherslu á uppsetningu þarf að stofna kanban-tilviksreglu til að tryggja að birgðir fyrir framleiðsluuppskriftarlínur í blönduðum lean og classic vinnsluumhverfi."
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 452cc5cf6060b71f91ad43e39e756dc23d759448
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-bom-line-event-kanban-rule"></a>Stofna tilviksreglu kanbans fyrir uppskriftarlínu

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Þetta verk leggur áherslu á uppsetningu þarf að stofna kanban-tilviksreglu til að tryggja að birgðir fyrir framleiðsluuppskriftarlínur í blönduðum lean og classic vinnsluumhverfi. Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF. Þetta verkefni er ætlað fyrir Ferlishönnuð eða Virðisstraumsstjóra, þar sem þau undirbúa framleiðslu nýja eða breytta afurðar.


## <a name="create-a-new-kanban-rule"></a>Stofna nýja kanban-reglu
1. Fara í framleiðslustýringar > Reglubundin verkefni > Útreikning kanban-magns > kanban-regla.
2. Smellið á „Nýtt“.
3. Veljið í svæðinu gerð „afturköllun".
    * Afturköllunar gerð er notuð til að stofna flutnings kanban.  
4. Velja 'Tilvik' í reitnum Áfyllingaráætlun.
    * Tilviksáætlunin er valinn til að stofna flutning á kanbans byggt á tilviki. Seinna í verkefnaleiðbeiningar, munum við virkja það með því að meta framleiðslupöntun.  
5. Færa inn eða velja gildi í reitnum Fyrsta áætlun verkþáttarins.
    * Sláið inn eða Veljið ReplenishSpeakerComponents. Þessi flutningsverkþátt hefur innhreyfingar (úttak) vöruhús og staðsetning 12, sem þýðir að efni verður að flytja staðsetning 12 í vöruhúsi 12.  
6. Útvíkka hlutann Upplýsingar.
7. Sláðu inn eða veldu M0001 í reitnum Afurð.
8. Útvíkka hlutann Tilvik.
9. Í reitnum uppskriftarlínutilvik skal velja ‚Sjálfvirkt‘.
    * Uppskriftarlínu tilvik svæðið með stillt á Sjálfvirk, kanban stofnuð til að uppfylla þarfir efnis fyrir uppskriftarlínur í Framleiðslupöntun.  
10. Lokið síðunni.

## <a name="create-and-modify-a-new-production-order"></a>Stofna og breyta nýja framleiðslupöntun.
1. Fara í Framleiðslustýringar > Framleiðslupantanir > Allar framleiðslupantanir.
2. Smella á Ný framleiðslupöntun.
3. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
    * Veljið eða ritið L0001 Við notum vöru L0001 vegna þess að vara M0001 er ekki með í uppskriftinni fyrir vöru L0001.  
4. Smellið á „Stofna“.
5. Í listanum skal smella á tengilinn í línu L0001.
6. Smellt er á uppskrift.
7. Í listanum skal smella á tengilinn í valinni línu.
8. Smellið á „Breyta“.
9. Veljið Fest framboð í reitnum Gerð línu.
    * Fast framboð er valið til að setja af stað kanban-framboðsmyndun  
10. Veljið Nei í svæðinu notkun tilfangs
    * Hreinsa gátreitinn tilfanganotkunar gerir kleift að breyta vöruhúsi.  
11. Útvíkka hlutann birgðavíddir
12. Í reitnum Vöruhús skal færa inn ‚12‘.
    * Vöruhúsið er stillt á 12 þar sem þetta er úttaksvöruhúss afturköllun verkþáttarins.  
13. Í svæðinu staðsetningar, færið inn '12'.
    * Vöruhúsið er stillt á 12 þar sem þetta er úttaksvöruhúss afturköllun verkþáttarins.  
14. Lokið síðunni.
15. Lokið síðunni.

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a>Framleiðslupöntunin er metin og skoða stofnað kanban
1. Smellt er á Mat.
    * Mat á framleiðslupöntun mun virkja stofnun tengda kanban til að útvega vöru M0001.  
2. Smellið á „Í lagi“.
3. Lokið síðunni.
4. Lokið síðunni.
5. Farið í upplýsingar um afurðarstjórnun > Lean-framleiðsla > Kanban-reglur.
6. Í listanum skal smella á tengilinn í valinni línu.
    * Velja tilviksreglu kabans fyrir vöru M0001.  
7. Útvíkkar kanban-hlutann.
8. Í listanum skal merkja valda línu.
    * Athugaðu kanban sem var stofnað til að veita framboð fyrir M0001 fyrir áætlaða framleiðslupöntun.  
    * Þetta er síðasta skrefið!  


