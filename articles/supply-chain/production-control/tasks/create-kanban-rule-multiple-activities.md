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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558462"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="bdddd-103">Stofna kanban-reglu fyrir marga verkþætti</span><span class="sxs-lookup"><span data-stu-id="bdddd-103">Create a kanban rule for multiple activities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bdddd-104">Þessi verklýsing sýnir hvernig á að stofna kanban-reglu sem inniheldur marga verkþætti úr framleiðsluflæði.</span><span class="sxs-lookup"><span data-stu-id="bdddd-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="bdddd-105">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="bdddd-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="bdddd-106">Þetta verkefni er ætlað fyrir Ferlishönnuð eða Virðisstraumsstjóra, þar sem þau undirbúa framleiðslu nýja eða breytta afurðar í lean-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="bdddd-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="bdddd-107">Stofna nýja kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="bdddd-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="bdddd-108">Farið í upplýsingar um afurðarstjórnun > Lean-framleiðsla > Kanban-reglur.</span><span class="sxs-lookup"><span data-stu-id="bdddd-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="bdddd-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="bdddd-109">Click New.</span></span>
3. <span data-ttu-id="bdddd-110">Velja 'reglubundið' í reitnum Áfyllingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="bdddd-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="bdddd-111">Færa inn eða velja gildi í reitnum Fyrsta áætlun verkþáttarins.</span><span class="sxs-lookup"><span data-stu-id="bdddd-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="bdddd-112">Sláið inn SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="bdddd-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="bdddd-113">Veljið gátreitinn margir verkþættir.</span><span class="sxs-lookup"><span data-stu-id="bdddd-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="bdddd-114">Tilgangurinn er að láta fleiri ein eina aðgerð vera í kanban-reglunni.</span><span class="sxs-lookup"><span data-stu-id="bdddd-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="bdddd-115">Þú Velja slóð í framleiðsluflæði þegar síðasti áætlunarverkþátturinn er valinn.</span><span class="sxs-lookup"><span data-stu-id="bdddd-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="bdddd-116">Færa inn eða velja gildi í reitnum síðasti áætlunarverkþáttur.</span><span class="sxs-lookup"><span data-stu-id="bdddd-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="bdddd-117">Veldu SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="bdddd-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="bdddd-118">Eftir að gildið er valið opnast síðu sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="bdddd-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="bdddd-119">Veldu kanban-flæði SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="bdddd-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="bdddd-120">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="bdddd-120">Click OK.</span></span>  
7. <span data-ttu-id="bdddd-121">Útvíkka hlutann Upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="bdddd-121">Expand the Details section.</span></span>
8. <span data-ttu-id="bdddd-122">Sláðu inn eða veldu gildi í reitnum Afurð.</span><span class="sxs-lookup"><span data-stu-id="bdddd-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="bdddd-123">Velja vöru L0006.</span><span class="sxs-lookup"><span data-stu-id="bdddd-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="bdddd-124">Stofna kanbön og skoða vinnslur</span><span class="sxs-lookup"><span data-stu-id="bdddd-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="bdddd-125">Útvíkkar kanban-hlutann.</span><span class="sxs-lookup"><span data-stu-id="bdddd-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="bdddd-126">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="bdddd-126">Click Add.</span></span>
3. <span data-ttu-id="bdddd-127">Í reitnum Fjöldi kanbana skal færa inn ‚1‘.</span><span class="sxs-lookup"><span data-stu-id="bdddd-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="bdddd-128">Þetta stofnar eitt kanbön.</span><span class="sxs-lookup"><span data-stu-id="bdddd-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="bdddd-129">Setja afurðarmagn á "3".</span><span class="sxs-lookup"><span data-stu-id="bdddd-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="bdddd-130">Kanban mun vinna 3 afurðir.</span><span class="sxs-lookup"><span data-stu-id="bdddd-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="bdddd-131">Færa inn dagsetningu og tíma í reitnum Lokadagsetning og -tími.</span><span class="sxs-lookup"><span data-stu-id="bdddd-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="bdddd-132">Hægt er að færa inn Í dag.</span><span class="sxs-lookup"><span data-stu-id="bdddd-132">You can enter Today.</span></span>  
6. <span data-ttu-id="bdddd-133">Smellið á „Stofna“.</span><span class="sxs-lookup"><span data-stu-id="bdddd-133">Click Create.</span></span>
7. <span data-ttu-id="bdddd-134">Smellið á Details.</span><span class="sxs-lookup"><span data-stu-id="bdddd-134">Click Details.</span></span>
    * <span data-ttu-id="bdddd-135">Athugaðu að Kanbanið hefur tvær ferlisvinnslur úr framleiðsluflæði.</span><span class="sxs-lookup"><span data-stu-id="bdddd-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="bdddd-136">Sá fyrri er SpeakerAssemblyAndPolish og sá seinni er SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="bdddd-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="bdddd-137">Þetta er síðasta skrefið!</span><span class="sxs-lookup"><span data-stu-id="bdddd-137">This is the last step!</span></span>  

