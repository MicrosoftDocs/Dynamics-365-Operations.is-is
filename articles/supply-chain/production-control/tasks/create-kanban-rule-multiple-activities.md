---
title: Stofna kanban-reglu fyrir marga verkþætti
description: Þessi verklýsing sýnir hvernig á að stofna kanban-reglu sem inniheldur marga verkþætti úr framleiðsluflæði.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fe7e1c67161bd77e6ddc5d7c9f1607fe895ce21
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "331254"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a>Stofna kanban-reglu fyrir marga verkþætti

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að stofna kanban-reglu sem inniheldur marga verkþætti úr framleiðsluflæði. Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF. Þetta verkefni er ætlað fyrir Ferlishönnuð eða Virðisstraumsstjóra, þar sem þau undirbúa framleiðslu nýja eða breytta afurðar í lean-umhverfi.


## <a name="create-a-new-kanban-rule"></a>Stofna nýja kanban-reglu
1. Farið í upplýsingar um afurðarstjórnun > Lean-framleiðsla > Kanban-reglur.
2. Smellið á „Nýtt“.
3. Velja 'reglubundið' í reitnum Áfyllingaráætlun.
4. Færa inn eða velja gildi í reitnum Fyrsta áætlun verkþáttarins.
    * Sláið inn SpeakerAssemblyAndPolish.  
5. Veljið gátreitinn margir verkþættir.
    * Tilgangurinn er að láta fleiri ein eina aðgerð vera í kanban-reglunni. Þú Velja slóð í framleiðsluflæði þegar síðasti áætlunarverkþátturinn er valinn.  
6. Færa inn eða velja gildi í reitnum síðasti áætlunarverkþáttur.
    * Veldu SpeakerTestAndPackaging. Eftir að gildið er valið opnast síðu sjálfkrafa. Veldu kanban-flæði SpeakerAssemblyAndPolish > SpeakerTestAndPackaging. Smellið á „Í lagi“.  
7. Útvíkka hlutann Upplýsingar.
8. Sláðu inn eða veldu gildi í reitnum Afurð.
    * Velja vöru L0006.  

## <a name="create-kanban-and-view-jobs"></a>Stofna kanbön og skoða vinnslur
1. Útvíkkar kanban-hlutann.
2. Smelltu á Bæta við.
3. Í reitnum Fjöldi kanbana skal færa inn ‚1‘.
    * Þetta stofnar eitt kanbön.  
4. Setja afurðarmagn á "3".
    * Kanban mun vinna 3 afurðir.  
5. Færa inn dagsetningu og tíma í reitnum Lokadagsetning og -tími.
    * Hægt er að færa inn Í dag.  
6. Smellið á „Stofna“.
7. Smellið á Details.
    * Athugaðu að Kanbanið hefur tvær ferlisvinnslur úr framleiðsluflæði. Sá fyrri er SpeakerAssemblyAndPolish og sá seinni er SpeakerTestAndPackaging.  
    * Þetta er síðasta skrefið!  

