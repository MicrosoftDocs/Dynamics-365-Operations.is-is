--- 
# required metadata 
title: Áætla kanban-vinnslu
description: Þetta ferli leggur áherslu á röðun ferlis kanban-vinnslur fyrir tiltekna vinnuflokkur.
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: null
ms.service: dynamics-ax-applications
ms.technology: null
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: '2016-06-30'
ms.dyn365.ops.version: AX 7.0.0
---
# <a name="schedule-kanban-jobs"></a><span data-ttu-id="afe17-103">Áætla kanban-vinnslu</span><span class="sxs-lookup"><span data-stu-id="afe17-103">Schedule kanban jobs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="afe17-104">Þetta ferli leggur áherslu á röðun ferlis kanban-vinnslur fyrir tiltekna vinnuflokkur.</span><span class="sxs-lookup"><span data-stu-id="afe17-104">This procedure focuses on scheduling process kanban jobs for a specific work cell.</span></span> <span data-ttu-id="afe17-105">Ferli "Undirbúa ferli kanban-vinnslu þegar efni er tiltækt" er skilyrði fyrir stofnun þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="afe17-105">The procedure "Prepare a process kanban job when materials are not available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="afe17-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="afe17-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="afe17-107">Þetta verk er ætluð fyrir yfirmaður vinnusals og framleiðslustjóri sem vinnur með kanban.</span><span class="sxs-lookup"><span data-stu-id="afe17-107">This task is intended for the shop floor supervisor and production planner working with kanbans.</span></span>


## <a name="select-kanban-jobs-for-a-work-cell"></a><span data-ttu-id="afe17-108">Velja kanban-vinnslur fyrir vinnuflokks</span><span class="sxs-lookup"><span data-stu-id="afe17-108">Select kanban jobs for a work cell</span></span>
1. <span data-ttu-id="afe17-109">Fara í Framleiðslustýringar > Kanban > Áætlun kanban-vinnslu.</span><span class="sxs-lookup"><span data-stu-id="afe17-109">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="afe17-110">Útvíkka upplýsingakassa Afkastageta Tímabilsins</span><span class="sxs-lookup"><span data-stu-id="afe17-110">Expand the Period capacity fact box</span></span>
    * <span data-ttu-id="afe17-111">Útvíkka kanban-upplýsingakassa.</span><span class="sxs-lookup"><span data-stu-id="afe17-111">Expand the Kanban FactBox.</span></span>  
3. <span data-ttu-id="afe17-112">Í reitnum vinnuflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="afe17-112">In the Work cell field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="afe17-113">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="afe17-113">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="afe17-114">Velja vinnuflokkur 1250.</span><span class="sxs-lookup"><span data-stu-id="afe17-114">Select work cell 1250.</span></span> <span data-ttu-id="afe17-115">Þetta sía yfirlitið til að birta aðeins vinnslur fyrir vinnuflokk 1250.</span><span class="sxs-lookup"><span data-stu-id="afe17-115">This will filter the view to display only the jobs for work cell 1250.</span></span>  
5. <span data-ttu-id="afe17-116">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="afe17-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="afe17-117">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="afe17-117">Click Select.</span></span>

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a><span data-ttu-id="afe17-118">Áætlun kanban-vinnslu í fyrsta tímabilinu tiltæk</span><span class="sxs-lookup"><span data-stu-id="afe17-118">Schedule a kanban job in the first available period</span></span>
1. <span data-ttu-id="afe17-119">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="afe17-119">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="afe17-120">Veljið fyrstu línunni á listanum sem hefur stöðuna Ekki áætlað.</span><span class="sxs-lookup"><span data-stu-id="afe17-120">Select the first row in the list that has the Not planned status.</span></span> <span data-ttu-id="afe17-121">Brotinni línu í reitnum staða Vinnslu gefur til kynna Ekki áætluð.</span><span class="sxs-lookup"><span data-stu-id="afe17-121">The dotted icon in the Job status field indicates not planned.</span></span>  
2. <span data-ttu-id="afe17-122">Smellt er á Áætlun.</span><span class="sxs-lookup"><span data-stu-id="afe17-122">Click Schedule.</span></span>
    * <span data-ttu-id="afe17-123">Þetta mun áætla kanban-vinnslu á fyrsta tiltæka tímabili.</span><span class="sxs-lookup"><span data-stu-id="afe17-123">This will schedule the kanban job in the first available period.</span></span>  
    * <span data-ttu-id="afe17-124">Athugið að kanban-vinnslu er fluttur í lok lista þar sem hún hefur verið bætt við tímabil sem hefjast frá dagsetningunni í dag.</span><span class="sxs-lookup"><span data-stu-id="afe17-124">Notice that the kanban job is moved to the end of the list because it has been added to the period starting from today.</span></span>  
    * <span data-ttu-id="afe17-125">Ef tímabil sem hefjast frá dagsetningunni í dag er bókað til fulls mun vinnslu færð á fyrsta tiltæka tímabils.</span><span class="sxs-lookup"><span data-stu-id="afe17-125">If the period starting from today is fully booked, the job will be moved to the first available period.</span></span>  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a><span data-ttu-id="afe17-126">Raða tvær kanban-vinnslur fyrir tiltekinn dag</span><span class="sxs-lookup"><span data-stu-id="afe17-126">Schedule two kanban jobs for a specific day</span></span>
1. <span data-ttu-id="afe17-127">Í listanum skal velja línu 1.</span><span class="sxs-lookup"><span data-stu-id="afe17-127">In the list, select row 1.</span></span>
    * <span data-ttu-id="afe17-128">Þú ættir að sjá í fyrstu línunni hefur það staða Ekki áætluð í Vinnslustöðusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="afe17-128">You should see that the first row has the Not planned status in the Job status field.</span></span>  
2. <span data-ttu-id="afe17-129">Í listanum skal velja línu 2.</span><span class="sxs-lookup"><span data-stu-id="afe17-129">In the list, select row 2.</span></span>
    * <span data-ttu-id="afe17-130">Þú ættir að sjá í annarri línunni hefur það staða Ekki áætluð í Vinnslustöðusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="afe17-130">You should see that the second row has the Not planned status in the Job status field.</span></span> <span data-ttu-id="afe17-131">Nú ertu með fyrstu tveimur vinnslum sem valin.</span><span class="sxs-lookup"><span data-stu-id="afe17-131">Now you have the first two jobs selected.</span></span>  
3. <span data-ttu-id="afe17-132">Smellt er á Áætlun frá dagsetningu til að opna svargluggann fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="afe17-132">Click Schedule from date to open the drop dialog.</span></span>
4. <span data-ttu-id="afe17-133">Merkja eða afmerkja Hnekkja viðbrögðum við skorti á afkastagetu reitnum.</span><span class="sxs-lookup"><span data-stu-id="afe17-133">Check or uncheck the Override capacity shortage reaction box.</span></span>
    * <span data-ttu-id="afe17-134">Þessi valkostur gerir kleift að hnekkja sjálfgefin viðbrögð við skorti á afköstum.</span><span class="sxs-lookup"><span data-stu-id="afe17-134">This option allows you to override the default capacity shortage reaction.</span></span>  
5. <span data-ttu-id="afe17-135">Í reitnum viðbrögð við skorti á afkastagetu Velja 'Bæta við umbeðið tímabil'.</span><span class="sxs-lookup"><span data-stu-id="afe17-135">In the Capacity shortage reaction field, select 'Add to the requested period'.</span></span>
    * <span data-ttu-id="afe17-136">Þessi valkostur munu tryggja að vinnslunni er bætt við umbeðið tímabil, óháð því ef vinnuflokkur gæti verið ofhlaðinn.</span><span class="sxs-lookup"><span data-stu-id="afe17-136">This option will ensure that the job is added to the requested period, regardless if the work cell might be overloaded.</span></span>  
6. <span data-ttu-id="afe17-137">Smellt er á Áætlun.</span><span class="sxs-lookup"><span data-stu-id="afe17-137">Click Schedule.</span></span>
    * <span data-ttu-id="afe17-138">Athugið að báðir vinnslur er bætt við umbeðið tímabil.</span><span class="sxs-lookup"><span data-stu-id="afe17-138">Notice that both jobs are added to the desired period.</span></span>  
    * <span data-ttu-id="afe17-139">Hægt er að sjá álag fyrir hvert tímabil í hlutanum afkastageta Tímabilsins.</span><span class="sxs-lookup"><span data-stu-id="afe17-139">In the Period capacity section, you can see the load for each period.</span></span> <span data-ttu-id="afe17-140">Reiturinn Notkun sýnir áætlaða notkun á þessu tímabili.</span><span class="sxs-lookup"><span data-stu-id="afe17-140">The Consumption field shows the scheduled consumption in this period.</span></span> <span data-ttu-id="afe17-141">Ef áætluð notkun er hærri en tiltæk afkastageta í þetta tímabil er valið ofhlaðin notkun.</span><span class="sxs-lookup"><span data-stu-id="afe17-141">If the scheduled consumption is higher than the available capacity in this period, the overloaded consumption will be selected.</span></span>  

