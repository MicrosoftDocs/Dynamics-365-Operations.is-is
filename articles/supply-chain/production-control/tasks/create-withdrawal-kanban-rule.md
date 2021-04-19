---
title: Stofna kanban-reglu úttektar
description: Þessi ferli sýnir uppsetningu sem þarf til að stofna afturköllun kanban-reglu til að flytja efni í lean-umhverfi.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2adbcdbb2d278b25dce1d8c027e66367e9c0930e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828827"
---
# <a name="create-a-withdrawal-kanban-rule"></a>Stofna kanban-reglu úttektar

[!include [banner](../../includes/banner.md)]

Þessi ferli sýnir uppsetningu sem þarf til að stofna afturköllun kanban-reglu til að flytja efni í lean-umhverfi. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta ferli er ætlað fyrir Ferlishönnuð eða Virðisstraumsstjóra, þar sem þau undirbúa áfyllingu nýja eða breytta efna.


## <a name="create-new-kanban-rule"></a>Stofna nýja kanban-reglu
1. Fara á kanban-reglur.
2. Smellið á „Nýtt“.
3. Veljið í svæðinu gerð „afturköllun".
    * Afturköllun gerð er notuð fyrir kanban-reglur til að flytja efni eða vörur.  
4. Færa inn eða velja gildi í reitnum Fyrsta áætlun verkþáttarins.
    * Veldu ReplenishSpeakerComponents.   Þessi verkþáttur er sett upp til að flytja hluti úr vöruhúsi 11, staðsetning 11 í 12 vöruhús og staðsetning 12.  
5. Sláðu inn eða veldu gildi í reitnum Afurð.
    * Veldu M0007.  
6. Í reitinn Afhendingartími skal slá inn númer.
    * Til dæmis 60.  
7. Færðu inn eða veldu gildi í reitnum Mælieining.
    * Til dæmis, Mínútur.  

## <a name="set-quantities-for-kanban"></a>Velja Kanban-magn
1. Stilla Sjálfgefið magn á '5'.
    * Þetta er magnið sem verður flutt fyrir hverja kanban.  
2. Í svæðinu fast kanban-magn, færið inn '2'.
    * Þetta er upphæð kanbana sem á að vera virk. Í þessu tilfelli flytja 2 kanban 5 hvert um sig.  
3. Í reitnum Lágmark viðvörunarmarka skal færa inn ‚1‘.
    * Notað til að fylgjast með lágmarksupphæð fullra kanbana sem eiga að vera á ákvörðunarstað. Þetta er til dæmis notað á yfirlit yfir magn kanbans.  
4. Í reitnum Hámark viðvörunarmarka skal færa inn ‚2‘.
    * Notað til að fylgjast með hámarksupphæð fullra kanbana sem eiga að vera á ákvörðunarstað. Þetta er til dæmis notað á yfirlit yfir magn kanbans.  

## <a name="create-kanbans"></a>Stofna kanbön
1. Smellið á „Vista“.
    * Vista þarf kanban-regluna vista áður en hægt er að stofna kanban.  
2. Smelltu á Bæta við.
    * Athugaðu að það eru engin virk kanban, vegna þess að ráðlagður ‚Fjöldi nýrra kanbana‘ er 2. Þetta er jafnt og ‚Fast kanban-magn‘.  
3. Smellið á „Stofna“.
    * Þetta stofnar tvö kanbön.  
    * Athugið að 2 kanbön, fyrir hver 5, voru stofnuð fyrir þessa kanban-reglu afturköllun.  Þetta er síðasta skrefið í þessu ferli.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]