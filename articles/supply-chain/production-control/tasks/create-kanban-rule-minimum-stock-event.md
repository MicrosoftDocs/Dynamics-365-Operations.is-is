---
title: Stofna kanban-reglu með lágmarksbirgðatilviki
description: Þetta ferli leggur áherslu á uppsetningu sem þarf til að stofna kanban-regla með því að nota tilvik lágmarksbirgða til að tryggja að tiltekinni vöru sé alltaf tiltækt á tiltekinn stað.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 297ee73daf10dffd027dadec11725ae6f0408d4c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255158"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="c8b17-103">Stofna kanban-reglu með lágmarksbirgðatilviki</span><span class="sxs-lookup"><span data-stu-id="c8b17-103">Create a kanban rule using a minimum stock event</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c8b17-104">Þetta ferli leggur áherslu á uppsetningu sem þarf til að stofna kanban-regla með því að nota tilvik lágmarksbirgða til að tryggja að tiltekinni vöru sé alltaf tiltækt á tiltekinn stað.</span><span class="sxs-lookup"><span data-stu-id="c8b17-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="c8b17-105">Kanban-regla er stofnuð til að flytja efni til staðsetningar þegar birgðastigið fer niður fyrir 200 stykki.</span><span class="sxs-lookup"><span data-stu-id="c8b17-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="c8b17-106">Með því að keyra vinnslu þarfarakningartilviks, eru nauðsynleg kanbön stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="c8b17-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="c8b17-107">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="c8b17-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="c8b17-108">Þetta verkefni er ætlað fyrir Ferlishönnuð eða Virðisstraumsstjóra, þar sem þau undirbúa framleiðslu nýja eða breytta afurðar í lean-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="c8b17-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="c8b17-109">Stofna nýja kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="c8b17-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="c8b17-110">Farið í upplýsingar um afurðarstjórnun > Lean-framleiðsla > Kanban-reglur.</span><span class="sxs-lookup"><span data-stu-id="c8b17-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="c8b17-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="c8b17-111">Click New.</span></span>
3. <span data-ttu-id="c8b17-112">Veljið í svæðinu gerð „afturköllun".</span><span class="sxs-lookup"><span data-stu-id="c8b17-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="c8b17-113">Þessi gerð er notuð til að stofna flutnings kanban.</span><span class="sxs-lookup"><span data-stu-id="c8b17-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="c8b17-114">Velja 'Tilvik' í reitnum Áfyllingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="c8b17-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="c8b17-115">Tilviksáætlunin er notuð til að stofna flutnings kanban byggt á tilviki.</span><span class="sxs-lookup"><span data-stu-id="c8b17-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="c8b17-116">Seinna í ferlinu, muntu virkja flytnings kanban með því að nota birgðaáfyllingar.</span><span class="sxs-lookup"><span data-stu-id="c8b17-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="c8b17-117">Færa inn eða velja gildi í reitnum Fyrsta áætlun verkþáttarins.</span><span class="sxs-lookup"><span data-stu-id="c8b17-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="c8b17-118">Sláið inn eða Veljið ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="c8b17-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="c8b17-119">Þessi flutningsverkþátt hefur innhreyfingar (úttak) vöruhús og staðsetning 12, sem þýðir að efni verður að flytja staðsetning 12 í vöruhúsi 12.</span><span class="sxs-lookup"><span data-stu-id="c8b17-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="c8b17-120">Útvíkka hlutann Upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="c8b17-120">Expand the Details section.</span></span>
7. <span data-ttu-id="c8b17-121">Sláðu inn eða veldu gildi í reitnum Afurð.</span><span class="sxs-lookup"><span data-stu-id="c8b17-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="c8b17-122">Veldu M0007.</span><span class="sxs-lookup"><span data-stu-id="c8b17-122">Select M0007.</span></span>  
8. <span data-ttu-id="c8b17-123">Útvíkka hlutann Tilvik.</span><span class="sxs-lookup"><span data-stu-id="c8b17-123">Expand the Events section.</span></span>
9. <span data-ttu-id="c8b17-124">Í reitnum tilvik birgðaáfyllingar, skal velja ‚runa.</span><span class="sxs-lookup"><span data-stu-id="c8b17-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="c8b17-125">Þetta stofnar Kanban til að uppfylla efnisþörfum tengdri staðsetningu meðan stendur á vinnsla Þarfarakningartilvika.</span><span class="sxs-lookup"><span data-stu-id="c8b17-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="c8b17-126">Stilltu Lágmarksmagn vöru</span><span class="sxs-lookup"><span data-stu-id="c8b17-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="c8b17-127">Smellið til að elta tengilinn í reitnum afurð.</span><span class="sxs-lookup"><span data-stu-id="c8b17-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="c8b17-128">Smellið til að elta tengilinn í reitnum vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="c8b17-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="c8b17-129">Útvíkka Upplýsingakassa mynd Afurðar.</span><span class="sxs-lookup"><span data-stu-id="c8b17-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="c8b17-130">Smellið á „Áætlun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="c8b17-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="c8b17-131">Smellt er á vöruþekju.</span><span class="sxs-lookup"><span data-stu-id="c8b17-131">Click Item coverage.</span></span>
6. <span data-ttu-id="c8b17-132">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="c8b17-132">Click New.</span></span>
7. <span data-ttu-id="c8b17-133">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="c8b17-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="c8b17-134">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="c8b17-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="c8b17-135">Stilltu Vöruhús á 12.</span><span class="sxs-lookup"><span data-stu-id="c8b17-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="c8b17-136">Lágmark er stillt á "200".</span><span class="sxs-lookup"><span data-stu-id="c8b17-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="c8b17-137">Keyra vinnsluna stofnun runutilviks</span><span class="sxs-lookup"><span data-stu-id="c8b17-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="c8b17-138">Fara í Framleiðslustýringar > Reglubundin verkefni > Runuvinnsla Kanban-vinnslu > Vinnsla þarfarakningartilvika.</span><span class="sxs-lookup"><span data-stu-id="c8b17-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="c8b17-139">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c8b17-139">Click OK.</span></span>
3. <span data-ttu-id="c8b17-140">Farið í upplýsingar um afurðarstjórnun > Lean-framleiðsla > Kanban-reglur.</span><span class="sxs-lookup"><span data-stu-id="c8b17-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="c8b17-141">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="c8b17-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c8b17-142">Velja kanban-reglu sem áður var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="c8b17-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="c8b17-143">Útvíkkar kanban-hlutann.</span><span class="sxs-lookup"><span data-stu-id="c8b17-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="c8b17-144">Athugið að búinn var til kanban til að flytja nauðsynlegt efni í vöruhús 12 .</span><span class="sxs-lookup"><span data-stu-id="c8b17-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]