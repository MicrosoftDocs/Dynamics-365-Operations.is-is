--- 
title: "Áætla framleiðslupöntun með rekstrar- og vinnuröðun"
description: "Þetta ferli áherslu á röðun á framleiðslupöntun með aðgerðaröðun og vinnsluröðun."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d4aac437876862e9f776264fc81f246c820bdf45
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="b269b-103">Áætla framleiðslupöntun með rekstrar- og vinnuröðun</span><span class="sxs-lookup"><span data-stu-id="b269b-103">Schedule a production order with operations and job scheduling</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b269b-104">Þetta ferli áherslu á röðun á framleiðslupöntun með aðgerðaröðun og vinnsluröðun.</span><span class="sxs-lookup"><span data-stu-id="b269b-104">This procedure focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="b269b-105">Engar vinnslur eru stofnaðar með aðgerðaröðun meðan störf eru stofnuð með vinnsluröðun.</span><span class="sxs-lookup"><span data-stu-id="b269b-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="b269b-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="b269b-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="b269b-107">Þetta ferli er ætluð fyrir framleiðslustjóri skipuleggjandi framleiðslu eða vinnusalarstjórnun yfirmaður sem unnið er í framleiðsluumhverfi afmörkuð.</span><span class="sxs-lookup"><span data-stu-id="b269b-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="b269b-108">Stofna framleiðslupöntun</span><span class="sxs-lookup"><span data-stu-id="b269b-108">Create a production order</span></span>
1. <span data-ttu-id="b269b-109">Fara í Framleiðslustýringar > Framleiðslupantanir > Allar framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="b269b-109">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="b269b-110">Smella á Ný framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="b269b-110">Click New production order.</span></span>
3. <span data-ttu-id="b269b-111">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="b269b-111">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="b269b-112">Veldu vörunúmer D0001.</span><span class="sxs-lookup"><span data-stu-id="b269b-112">Select Item number D0001.</span></span>  
4. <span data-ttu-id="b269b-113">Smellið á „Stofna“.</span><span class="sxs-lookup"><span data-stu-id="b269b-113">Click Create.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="b269b-114">Ef framkvæma á aðgerðaröðun fyrir framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="b269b-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="b269b-115">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="b269b-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b269b-116">Veljið framleiðslupöntun sem hefur verið rétt stofnuð.</span><span class="sxs-lookup"><span data-stu-id="b269b-116">Select the production order that you have just created.</span></span> <span data-ttu-id="b269b-117">Það ætti að vera efst á listanum.</span><span class="sxs-lookup"><span data-stu-id="b269b-117">It should be at the top of the list.</span></span>      
2. <span data-ttu-id="b269b-118">Í Aðgerðarrúðunni er smellt á Áætlun.</span><span class="sxs-lookup"><span data-stu-id="b269b-118">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="b269b-119">smella Raða aðgerðum</span><span class="sxs-lookup"><span data-stu-id="b269b-119">Click Schedule operations.</span></span>
4. <span data-ttu-id="b269b-120">Í reitnum röðunarstefna er valið „áfram frá röðunardagsetningu“.</span><span class="sxs-lookup"><span data-stu-id="b269b-120">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
5. <span data-ttu-id="b269b-121">Dagsetning er rituð í reitinn röðunardagsetning.</span><span class="sxs-lookup"><span data-stu-id="b269b-121">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="b269b-122">Velja dagsetningu í framtíðinni, til dæmis í dag plús ein vika.</span><span class="sxs-lookup"><span data-stu-id="b269b-122">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="b269b-123">Með valda Röðun stefnu framleiðslupöntun verður raðað áfram frá þessari dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="b269b-123">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="b269b-124">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b269b-124">Click OK.</span></span>
7. <span data-ttu-id="b269b-125">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="b269b-125">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b269b-126">Athugið Stöðu framleiðslu er breytt í áætlað</span><span class="sxs-lookup"><span data-stu-id="b269b-126">Note that the status is changed to Scheduled.</span></span>  
8. <span data-ttu-id="b269b-127">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="b269b-127">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b269b-128">Smellt er á Allar vinnslur.</span><span class="sxs-lookup"><span data-stu-id="b269b-128">Click All jobs.</span></span>
    * <span data-ttu-id="b269b-129">Athugið að engar vinnslur eru stofnaðar með aðgerðaröðun.</span><span class="sxs-lookup"><span data-stu-id="b269b-129">Note that no jobs are created with operations scheduling.</span></span>  
10. <span data-ttu-id="b269b-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b269b-130">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="b269b-131">Ef framkvæma á aðgerðaröðun fyrir framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="b269b-131">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="b269b-132">Í Aðgerðarrúðunni er smellt á Áætlun.</span><span class="sxs-lookup"><span data-stu-id="b269b-132">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="b269b-133">Smella á Áætla verk.</span><span class="sxs-lookup"><span data-stu-id="b269b-133">Click Schedule jobs.</span></span>
3. <span data-ttu-id="b269b-134">Í reitnum röðunarstefna er valið „áfram frá röðunardagsetningu“.</span><span class="sxs-lookup"><span data-stu-id="b269b-134">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
4. <span data-ttu-id="b269b-135">Dagsetning er rituð í reitinn röðunardagsetning.</span><span class="sxs-lookup"><span data-stu-id="b269b-135">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="b269b-136">Velja dagsetningu í framtíðinni, til dæmis í dag plús ein vika.</span><span class="sxs-lookup"><span data-stu-id="b269b-136">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="b269b-137">Með valda Röðun stefnu framleiðslupöntun verður raðað áfram frá þessari dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="b269b-137">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="b269b-138">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b269b-138">Click OK.</span></span>
6. <span data-ttu-id="b269b-139">Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="b269b-139">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="b269b-140">Smellt er á Allar vinnslur.</span><span class="sxs-lookup"><span data-stu-id="b269b-140">Click All jobs.</span></span>
    * <span data-ttu-id="b269b-141">Athugið samkvæmt virk leið 5 störf eru stofnuð með vinnsluröðun.</span><span class="sxs-lookup"><span data-stu-id="b269b-141">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  


