---
title: Stofna kanban-reglu úttektar
description: Þessi ferli sýnir uppsetningu sem þarf til að stofna afturköllun kanban-reglu til að flytja efni í lean-umhverfi.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a77c66b64512274f2703543293c2f48f2df2acf5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570142"
---
# <a name="create-a-withdrawal-kanban-rule"></a><span data-ttu-id="f7511-103">Stofna kanban-reglu úttektar</span><span class="sxs-lookup"><span data-stu-id="f7511-103">Create a withdrawal kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f7511-104">Þessi ferli sýnir uppsetningu sem þarf til að stofna afturköllun kanban-reglu til að flytja efni í lean-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="f7511-104">This procedure shows the setup that is needed to create a withdrawal kanban rule for transferring material in a lean environment.</span></span> <span data-ttu-id="f7511-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="f7511-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f7511-106">Þetta ferli er ætlað fyrir Ferlishönnuð eða Virðisstraumsstjóra, þar sem þau undirbúa áfyllingu nýja eða breytta efna.</span><span class="sxs-lookup"><span data-stu-id="f7511-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare replenishment of new or modified material.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="f7511-107">Stofna nýja kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="f7511-107">Create new kanban rule</span></span>
1. <span data-ttu-id="f7511-108">Fara á kanban-reglur.</span><span class="sxs-lookup"><span data-stu-id="f7511-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="f7511-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f7511-109">Click New.</span></span>
3. <span data-ttu-id="f7511-110">Veljið í svæðinu gerð „afturköllun".</span><span class="sxs-lookup"><span data-stu-id="f7511-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="f7511-111">Afturköllun gerð er notuð fyrir kanban-reglur til að flytja efni eða vörur.</span><span class="sxs-lookup"><span data-stu-id="f7511-111">The Withdrawal type is used for kanban rules to transfer material or goods.</span></span>  
4. <span data-ttu-id="f7511-112">Færa inn eða velja gildi í reitnum Fyrsta áætlun verkþáttarins.</span><span class="sxs-lookup"><span data-stu-id="f7511-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="f7511-113">Veldu ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="f7511-113">Select ReplenishSpeakerComponents.</span></span>   <span data-ttu-id="f7511-114">Þessi verkþáttur er sett upp til að flytja hluti úr vöruhúsi 11, staðsetning 11 í 12 vöruhús og staðsetning 12.</span><span class="sxs-lookup"><span data-stu-id="f7511-114">This activity is set up to move components from warehouse 11, location 11 to warehouse 12, and location 12.</span></span>  
5. <span data-ttu-id="f7511-115">Sláðu inn eða veldu gildi í reitnum Afurð.</span><span class="sxs-lookup"><span data-stu-id="f7511-115">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="f7511-116">Veldu M0007.</span><span class="sxs-lookup"><span data-stu-id="f7511-116">Select M0007.</span></span>  
6. <span data-ttu-id="f7511-117">Í reitinn Afhendingartími skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f7511-117">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="f7511-118">Til dæmis 60.</span><span class="sxs-lookup"><span data-stu-id="f7511-118">For example, 60.</span></span>  
7. <span data-ttu-id="f7511-119">Færðu inn eða veldu gildi í reitnum Mælieining.</span><span class="sxs-lookup"><span data-stu-id="f7511-119">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="f7511-120">Til dæmis, Mínútur.</span><span class="sxs-lookup"><span data-stu-id="f7511-120">For example, Minutes.</span></span>  

## <a name="set-quantities-for-kanban"></a><span data-ttu-id="f7511-121">Velja Kanban-magn</span><span class="sxs-lookup"><span data-stu-id="f7511-121">Set quantities for kanban</span></span>
1. <span data-ttu-id="f7511-122">Stilla Sjálfgefið magn á '5'.</span><span class="sxs-lookup"><span data-stu-id="f7511-122">Set Default quantity to '5'.</span></span>
    * <span data-ttu-id="f7511-123">Þetta er magnið sem verður flutt fyrir hverja kanban.</span><span class="sxs-lookup"><span data-stu-id="f7511-123">This is the quantity that will be transferred for each kanban.</span></span>  
2. <span data-ttu-id="f7511-124">Í svæðinu fast kanban-magn, færið inn '2'.</span><span class="sxs-lookup"><span data-stu-id="f7511-124">In the Fixed kanban quantity field, enter '2'.</span></span>
    * <span data-ttu-id="f7511-125">Þetta er upphæð kanbana sem á að vera virk.</span><span class="sxs-lookup"><span data-stu-id="f7511-125">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="f7511-126">Í þessu tilfelli flytja 2 kanban 5 hvert um sig.</span><span class="sxs-lookup"><span data-stu-id="f7511-126">In this case, 2 kanbans transferring 5 each.</span></span>  
3. <span data-ttu-id="f7511-127">Í reitnum Lágmark viðvörunarmarka skal færa inn ‚1‘.</span><span class="sxs-lookup"><span data-stu-id="f7511-127">In the Alert boundary minimum field, enter '1'.</span></span>
    * <span data-ttu-id="f7511-128">Notað til að fylgjast með lágmarksupphæð fullra kanbana sem eiga að vera á ákvörðunarstað.</span><span class="sxs-lookup"><span data-stu-id="f7511-128">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="f7511-129">Þetta er til dæmis notað á yfirlit yfir magn kanbans.</span><span class="sxs-lookup"><span data-stu-id="f7511-129">For example, this is used on the kanban quantity overview.</span></span>  
4. <span data-ttu-id="f7511-130">Í reitnum Hámark viðvörunarmarka skal færa inn ‚2‘.</span><span class="sxs-lookup"><span data-stu-id="f7511-130">In the Alert boundary maximum field, enter '2'.</span></span>
    * <span data-ttu-id="f7511-131">Notað til að fylgjast með hámarksupphæð fullra kanbana sem eiga að vera á ákvörðunarstað.</span><span class="sxs-lookup"><span data-stu-id="f7511-131">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="f7511-132">Þetta er til dæmis notað á yfirlit yfir magn kanbans.</span><span class="sxs-lookup"><span data-stu-id="f7511-132">For example, this is used on the kanban quantity overview.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="f7511-133">Stofna kanbön</span><span class="sxs-lookup"><span data-stu-id="f7511-133">Create kanbans</span></span>
1. <span data-ttu-id="f7511-134">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f7511-134">Click Save.</span></span>
    * <span data-ttu-id="f7511-135">Vista þarf kanban-regluna vista áður en hægt er að stofna kanban.</span><span class="sxs-lookup"><span data-stu-id="f7511-135">The kanban rule needs to be saved before kanbans can be created.</span></span>  
2. <span data-ttu-id="f7511-136">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f7511-136">Click Add.</span></span>
    * <span data-ttu-id="f7511-137">Athugaðu að það eru engin virk kanban, vegna þess að ráðlagður ‚Fjöldi nýrra kanbana‘ er 2. Þetta er jafnt og ‚Fast kanban-magn‘.</span><span class="sxs-lookup"><span data-stu-id="f7511-137">Note that there are no active kanbans because the suggested 'Number of new kanbans' is 2, which is equal to the 'Fixed kanban quantity'.</span></span>  
3. <span data-ttu-id="f7511-138">Smellið á „Stofna“.</span><span class="sxs-lookup"><span data-stu-id="f7511-138">Click Create.</span></span>
    * <span data-ttu-id="f7511-139">Þetta stofnar tvö kanbön.</span><span class="sxs-lookup"><span data-stu-id="f7511-139">This will create two kanbans.</span></span>  
    * <span data-ttu-id="f7511-140">Athugið að 2 kanbön, fyrir hver 5, voru stofnuð fyrir þessa kanban-reglu afturköllun.</span><span class="sxs-lookup"><span data-stu-id="f7511-140">Note that 2 kanbans, for 5 each, was created for this withdrawal kanban rule.</span></span>  <span data-ttu-id="f7511-141">Þetta er síðasta skrefið í þessu ferli.</span><span class="sxs-lookup"><span data-stu-id="f7511-141">This is the last step in this procedure.</span></span>  

