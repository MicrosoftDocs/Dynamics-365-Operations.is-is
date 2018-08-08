--- 
title: "Stofna kanban-reglu úttektar"
description: "Þessi ferli sýnir uppsetningu sem þarf til að stofna afturköllun kanban-reglu til að flytja efni í lean-umhverfi."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 5c1dbd8e19e2910ad2d1a7ea94ea8ab8ac1cf220
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-withdrawal-kanban-rule"></a><span data-ttu-id="fc04c-103">Stofna kanban-reglu úttektar</span><span class="sxs-lookup"><span data-stu-id="fc04c-103">Create a withdrawal kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fc04c-104">Þessi ferli sýnir uppsetningu sem þarf til að stofna afturköllun kanban-reglu til að flytja efni í lean-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="fc04c-104">This procedure shows the setup that is needed to create a withdrawal kanban rule for transferring material in a lean environment.</span></span> <span data-ttu-id="fc04c-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="fc04c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="fc04c-106">Þetta ferli er ætlað fyrir Ferlishönnuð eða Virðisstraumsstjóra, þar sem þau undirbúa áfyllingu nýja eða breytta efna.</span><span class="sxs-lookup"><span data-stu-id="fc04c-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare replenishment of new or modified material.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="fc04c-107">Stofna nýja kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="fc04c-107">Create new kanban rule</span></span>
1. <span data-ttu-id="fc04c-108">Fara á kanban-reglur.</span><span class="sxs-lookup"><span data-stu-id="fc04c-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="fc04c-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="fc04c-109">Click New.</span></span>
3. <span data-ttu-id="fc04c-110">Veljið í svæðinu gerð „afturköllun".</span><span class="sxs-lookup"><span data-stu-id="fc04c-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="fc04c-111">Afturköllun gerð er notuð fyrir kanban-reglur til að flytja efni eða vörur.</span><span class="sxs-lookup"><span data-stu-id="fc04c-111">The Withdrawal type is used for kanban rules to transfer material or goods.</span></span>  
4. <span data-ttu-id="fc04c-112">Færa inn eða velja gildi í reitnum Fyrsta áætlun verkþáttarins.</span><span class="sxs-lookup"><span data-stu-id="fc04c-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="fc04c-113">Veldu ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="fc04c-113">Select ReplenishSpeakerComponents.</span></span>   <span data-ttu-id="fc04c-114">Þessi verkþáttur er sett upp til að flytja hluti úr vöruhúsi 11, staðsetning 11 í 12 vöruhús og staðsetning 12.</span><span class="sxs-lookup"><span data-stu-id="fc04c-114">This activity is set up to move components from warehouse 11, location 11 to warehouse 12, and location 12.</span></span>  
5. <span data-ttu-id="fc04c-115">Sláðu inn eða veldu gildi í reitnum Afurð.</span><span class="sxs-lookup"><span data-stu-id="fc04c-115">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="fc04c-116">Veldu M0007.</span><span class="sxs-lookup"><span data-stu-id="fc04c-116">Select M0007.</span></span>  
6. <span data-ttu-id="fc04c-117">Í reitinn Afhendingartími skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="fc04c-117">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="fc04c-118">Til dæmis 60.</span><span class="sxs-lookup"><span data-stu-id="fc04c-118">For example, 60.</span></span>  
7. <span data-ttu-id="fc04c-119">Færðu inn eða veldu gildi í reitnum Mælieining.</span><span class="sxs-lookup"><span data-stu-id="fc04c-119">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="fc04c-120">Til dæmis, Mínútur.</span><span class="sxs-lookup"><span data-stu-id="fc04c-120">For example, Minutes.</span></span>  

## <a name="set-quantities-for-kanban"></a><span data-ttu-id="fc04c-121">Velja Kanban-magn</span><span class="sxs-lookup"><span data-stu-id="fc04c-121">Set quantities for kanban</span></span>
1. <span data-ttu-id="fc04c-122">Stilla Sjálfgefið magn á '5'.</span><span class="sxs-lookup"><span data-stu-id="fc04c-122">Set Default quantity to '5'.</span></span>
    * <span data-ttu-id="fc04c-123">Þetta er magnið sem verður flutt fyrir hverja kanban.</span><span class="sxs-lookup"><span data-stu-id="fc04c-123">This is the quantity that will be transferred for each kanban.</span></span>  
2. <span data-ttu-id="fc04c-124">Í svæðinu fast kanban-magn, færið inn '2'.</span><span class="sxs-lookup"><span data-stu-id="fc04c-124">In the Fixed kanban quantity field, enter '2'.</span></span>
    * <span data-ttu-id="fc04c-125">Þetta er upphæð kanbana sem á að vera virk.</span><span class="sxs-lookup"><span data-stu-id="fc04c-125">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="fc04c-126">Í þessu tilfelli flytja 2 kanban 5 hvert um sig.</span><span class="sxs-lookup"><span data-stu-id="fc04c-126">In this case, 2 kanbans transferring 5 each.</span></span>  
3. <span data-ttu-id="fc04c-127">Í reitnum Lágmark viðvörunarmarka skal færa inn ‚1‘.</span><span class="sxs-lookup"><span data-stu-id="fc04c-127">In the Alert boundary minimum field, enter '1'.</span></span>
    * <span data-ttu-id="fc04c-128">Notað til að fylgjast með lágmarksupphæð fullra kanbana sem eiga að vera á ákvörðunarstað.</span><span class="sxs-lookup"><span data-stu-id="fc04c-128">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="fc04c-129">Þetta er til dæmis notað á yfirlit yfir magn kanbans.</span><span class="sxs-lookup"><span data-stu-id="fc04c-129">For example, this is used on the kanban quantity overview.</span></span>  
4. <span data-ttu-id="fc04c-130">Í reitnum Hámark viðvörunarmarka skal færa inn ‚2‘.</span><span class="sxs-lookup"><span data-stu-id="fc04c-130">In the Alert boundary maximum field, enter '2'.</span></span>
    * <span data-ttu-id="fc04c-131">Notað til að fylgjast með hámarksupphæð fullra kanbana sem eiga að vera á ákvörðunarstað.</span><span class="sxs-lookup"><span data-stu-id="fc04c-131">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="fc04c-132">Þetta er til dæmis notað á yfirlit yfir magn kanbans.</span><span class="sxs-lookup"><span data-stu-id="fc04c-132">For example, this is used on the kanban quantity overview.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="fc04c-133">Stofna kanbön</span><span class="sxs-lookup"><span data-stu-id="fc04c-133">Create kanbans</span></span>
1. <span data-ttu-id="fc04c-134">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="fc04c-134">Click Save.</span></span>
    * <span data-ttu-id="fc04c-135">Vista þarf kanban-regluna vista áður en hægt er að stofna kanban.</span><span class="sxs-lookup"><span data-stu-id="fc04c-135">The kanban rule needs to be saved before kanbans can be created.</span></span>  
2. <span data-ttu-id="fc04c-136">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="fc04c-136">Click Add.</span></span>
    * <span data-ttu-id="fc04c-137">Athugaðu að það eru engin virk kanban, vegna þess að ráðlagður ‚Fjöldi nýrra kanbana‘ er 2. Þetta er jafnt og ‚Fast kanban-magn‘.</span><span class="sxs-lookup"><span data-stu-id="fc04c-137">Note that there are no active kanbans because the suggested 'Number of new kanbans' is 2, which is equal to the 'Fixed kanban quantity'.</span></span>  
3. <span data-ttu-id="fc04c-138">Smellið á „Stofna“.</span><span class="sxs-lookup"><span data-stu-id="fc04c-138">Click Create.</span></span>
    * <span data-ttu-id="fc04c-139">Þetta stofnar tvö kanbön.</span><span class="sxs-lookup"><span data-stu-id="fc04c-139">This will create two kanbans.</span></span>  
    * <span data-ttu-id="fc04c-140">Athugið að 2 kanbön, fyrir hver 5, voru stofnuð fyrir þessa kanban-reglu afturköllun.</span><span class="sxs-lookup"><span data-stu-id="fc04c-140">Note that 2 kanbans, for 5 each, was created for this withdrawal kanban rule.</span></span>  <span data-ttu-id="fc04c-141">Þetta er síðasta skrefið í þessu ferli.</span><span class="sxs-lookup"><span data-stu-id="fc04c-141">This is the last step in this procedure.</span></span>  


