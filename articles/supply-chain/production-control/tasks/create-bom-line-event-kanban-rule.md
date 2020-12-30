---
title: Stofna tilviksreglu kanbans fyrir uppskriftarlínu
description: Þetta verk leggur áherslu á uppsetningu þarf að stofna kanban-tilviksreglu til að tryggja að birgðir fyrir framleiðsluuppskriftarlínur í blönduðum lean og classic vinnsluumhverfi.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdTable, ProdBOM, ProdParmCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 698b7af3bc8e2146aaf86fb5e04dd123ea6d5153
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430057"
---
# <a name="create-a-bom-line-event-kanban-rule"></a><span data-ttu-id="ef7cd-103">Stofna tilviksreglu kanbans fyrir uppskriftarlínu</span><span class="sxs-lookup"><span data-stu-id="ef7cd-103">Create a BOM line event kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ef7cd-104">Þetta verk leggur áherslu á uppsetningu þarf að stofna kanban-tilviksreglu til að tryggja að birgðir fyrir framleiðsluuppskriftarlínur í blönduðum lean og classic vinnsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-104">This task focuses on the setup needed to create an event kanban rule to ensure supply for production BOM lines in a mixed lean and classic production environment.</span></span> <span data-ttu-id="ef7cd-105">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="ef7cd-106">Þetta verkefni er ætlað fyrir Ferlishönnuð eða Virðisstraumsstjóra, þar sem þau undirbúa framleiðslu nýja eða breytta afurðar.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="ef7cd-107">Stofna nýja kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="ef7cd-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="ef7cd-108">Fara í framleiðslustýringar > Reglubundin verkefni > Útreikning kanban-magns > kanban-regla.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-108">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban rules.</span></span>
2. <span data-ttu-id="ef7cd-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-109">Click New.</span></span>
3. <span data-ttu-id="ef7cd-110">Veljið í svæðinu gerð „afturköllun".</span><span class="sxs-lookup"><span data-stu-id="ef7cd-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="ef7cd-111">Afturköllunar gerð er notuð til að stofna flutnings kanban.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-111">The Withdrawal type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="ef7cd-112">Velja 'Tilvik' í reitnum Áfyllingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-112">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="ef7cd-113">Tilviksáætlunin er valinn til að stofna flutning á kanbans byggt á tilviki.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-113">The Event strategy is selected to create the transfer of kanbans based on an event.</span></span> <span data-ttu-id="ef7cd-114">Seinna í verkefnaleiðbeiningar, munum við virkja það með því að meta framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-114">Later in the task guide, we will trigger it by estimating a production order.</span></span>  
5. <span data-ttu-id="ef7cd-115">Færa inn eða velja gildi í reitnum Fyrsta áætlun verkþáttarins.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-115">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="ef7cd-116">Sláið inn eða Veljið ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-116">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="ef7cd-117">Þessi flutningsverkþátt hefur innhreyfingar (úttak) vöruhús og staðsetning 12, sem þýðir að efni verður að flytja staðsetning 12 í vöruhúsi 12.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-117">This transfer activity has receipt (output) warehouse and location 12, which means that material will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="ef7cd-118">Útvíkka hlutann Upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-118">Expand the Details section.</span></span>
7. <span data-ttu-id="ef7cd-119">Sláðu inn eða veldu M0001 í reitnum Afurð.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-119">In the Product field, enter or select M0001.</span></span>
8. <span data-ttu-id="ef7cd-120">Útvíkka hlutann Tilvik.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-120">Expand the Events section.</span></span>
9. <span data-ttu-id="ef7cd-121">Í reitnum uppskriftarlínutilvik skal velja ‚Sjálfvirkt‘.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-121">In the BOM line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="ef7cd-122">Uppskriftarlínu tilvik svæðið með stillt á Sjálfvirk, kanban stofnuð til að uppfylla þarfir efnis fyrir uppskriftarlínur í Framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-122">With the BOM line event field set to Automatic, kanban will be created to fulfill material needs for production order BOM lines.</span></span>  
10. <span data-ttu-id="ef7cd-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-123">Close the page.</span></span>

## <a name="create-and-modify-a-new-production-order"></a><span data-ttu-id="ef7cd-124">Stofna og breyta nýja framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-124">Create and modify a new production order</span></span>
1. <span data-ttu-id="ef7cd-125">Fara í Framleiðslustýringar > Framleiðslupantanir > Allar framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-125">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="ef7cd-126">Smella á Ný framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-126">Click New production order.</span></span>
3. <span data-ttu-id="ef7cd-127">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-127">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="ef7cd-128">Veljið eða ritið L0001</span><span class="sxs-lookup"><span data-stu-id="ef7cd-128">Enter or select 'L0001'.</span></span> <span data-ttu-id="ef7cd-129">Við notum vöru L0001 vegna þess að vara M0001 er ekki með í uppskriftinni fyrir vöru L0001.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-129">We use item L0001 because item M0001 is included in the BOM for item L0001.</span></span>  
4. <span data-ttu-id="ef7cd-130">Smellið á „Stofna“.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-130">Click Create.</span></span>
5. <span data-ttu-id="ef7cd-131">Í listanum skal smella á tengilinn í línu L0001.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-131">In the list, click the link in the row for L0001</span></span>
6. <span data-ttu-id="ef7cd-132">Smellt er á uppskrift.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-132">Click BOM.</span></span>
7. <span data-ttu-id="ef7cd-133">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-133">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="ef7cd-134">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-134">Click Edit.</span></span>
9. <span data-ttu-id="ef7cd-135">Veljið Fest framboð í reitnum Gerð línu.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-135">In the Line type field, select 'Pegged supply'.</span></span>
    * <span data-ttu-id="ef7cd-136">Fast framboð er valið til að setja af stað kanban-framboðsmyndun</span><span class="sxs-lookup"><span data-stu-id="ef7cd-136">Pegged supply is selected to trigger the supply creation of a kanban.</span></span>  
10. <span data-ttu-id="ef7cd-137">Veljið Nei í svæðinu notkun tilfangs</span><span class="sxs-lookup"><span data-stu-id="ef7cd-137">Select No in the Resource consumption field.</span></span>
    * <span data-ttu-id="ef7cd-138">Hreinsa gátreitinn tilfanganotkunar gerir kleift að breyta vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-138">Clearing the check box of Resource consumption lets us change the warehouse.</span></span>  
11. <span data-ttu-id="ef7cd-139">Útvíkka hlutann birgðavíddir</span><span class="sxs-lookup"><span data-stu-id="ef7cd-139">Expand the Inventory dimensions section.</span></span>
12. <span data-ttu-id="ef7cd-140">Í reitnum Vöruhús skal færa inn ‚12‘.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-140">In the Warehouse field, type '12'.</span></span>
    * <span data-ttu-id="ef7cd-141">Vöruhúsið er stillt á 12 þar sem þetta er úttaksvöruhúss afturköllun verkþáttarins.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-141">Warehouse is set to 12 because this is the output warehouse for the withdrawal activity.</span></span>  
13. <span data-ttu-id="ef7cd-142">Í svæðinu staðsetningar, færið inn '12'.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-142">In the Location field, type '12'.</span></span>
    * <span data-ttu-id="ef7cd-143">Vöruhúsið er stillt á 12 þar sem þetta er úttaksvöruhúss afturköllun verkþáttarins.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-143">Location is set to 12 because this is the output location of the withdrawal activity.</span></span>  
14. <span data-ttu-id="ef7cd-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-144">Close the page.</span></span>
15. <span data-ttu-id="ef7cd-145">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-145">Close the page.</span></span>

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a><span data-ttu-id="ef7cd-146">Framleiðslupöntunin er metin og skoða stofnað kanban</span><span class="sxs-lookup"><span data-stu-id="ef7cd-146">Estimate the production order and view the kanban created</span></span>
1. <span data-ttu-id="ef7cd-147">Smellt er á Mat.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-147">Click Estimate.</span></span>
    * <span data-ttu-id="ef7cd-148">Mat á framleiðslupöntun mun virkja stofnun tengda kanban til að útvega vöru M0001.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-148">Estimating the production order will trigger the creation of the associated kanban to supply item M0001.</span></span>  
2. <span data-ttu-id="ef7cd-149">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-149">Click OK.</span></span>
3. <span data-ttu-id="ef7cd-150">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-150">Close the page.</span></span>
4. <span data-ttu-id="ef7cd-151">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-151">Close the page.</span></span>
5. <span data-ttu-id="ef7cd-152">Farið í upplýsingar um afurðarstjórnun > Lean-framleiðsla > Kanban-reglur.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-152">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
6. <span data-ttu-id="ef7cd-153">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-153">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ef7cd-154">Velja tilviksreglu kabans fyrir vöru M0001.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-154">Select the event kanban rule created for item M0001.</span></span>  
7. <span data-ttu-id="ef7cd-155">Útvíkkar kanban-hlutann.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-155">Expand the Kanbans section.</span></span>
8. <span data-ttu-id="ef7cd-156">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-156">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ef7cd-157">Athugaðu kanban sem var stofnað til að veita framboð fyrir M0001 fyrir áætlaða framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="ef7cd-157">Notice the kanban created to supply M0001 for the estimated production order.</span></span>  
    * <span data-ttu-id="ef7cd-158">Þetta er síðasta skrefið!</span><span class="sxs-lookup"><span data-stu-id="ef7cd-158">This is the last step!</span></span>  

