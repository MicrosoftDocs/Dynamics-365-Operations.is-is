---
title: Áætla kanban-vinnslu
description: Þetta ferli leggur áherslu á röðun ferlis kanban-vinnslur fyrir tiltekna vinnuflokkur.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c8c088e7f70303aae9f106f627778108062a073f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811015"
---
# <a name="schedule-kanban-jobs"></a><span data-ttu-id="93905-103">Áætla kanban-vinnslu</span><span class="sxs-lookup"><span data-stu-id="93905-103">Schedule kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="93905-104">Þetta ferli leggur áherslu á röðun ferlis kanban-vinnslur fyrir tiltekna vinnuflokkur.</span><span class="sxs-lookup"><span data-stu-id="93905-104">This procedure focuses on scheduling process kanban jobs for a specific work cell.</span></span> <span data-ttu-id="93905-105">Ferli "Undirbúa ferli kanban-vinnslu þegar efni er tiltækt" er skilyrði fyrir stofnun þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="93905-105">The procedure "Prepare a process kanban job when materials are not available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="93905-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="93905-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="93905-107">Þetta verk er ætluð fyrir yfirmaður vinnusals og framleiðslustjóri sem vinnur með kanban.</span><span class="sxs-lookup"><span data-stu-id="93905-107">This task is intended for the shop floor supervisor and production planner working with kanbans.</span></span>


## <a name="select-kanban-jobs-for-a-work-cell"></a><span data-ttu-id="93905-108">Velja kanban-vinnslur fyrir vinnuflokks</span><span class="sxs-lookup"><span data-stu-id="93905-108">Select kanban jobs for a work cell</span></span>
1. <span data-ttu-id="93905-109">Fara í Framleiðslustýringar > Kanban > Áætlun kanban-vinnslu.</span><span class="sxs-lookup"><span data-stu-id="93905-109">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="93905-110">Útvíkka upplýsingakassa Afkastageta Tímabilsins</span><span class="sxs-lookup"><span data-stu-id="93905-110">Expand the Period capacity fact box</span></span>
    * <span data-ttu-id="93905-111">Útvíkka kanban-upplýsingakassa.</span><span class="sxs-lookup"><span data-stu-id="93905-111">Expand the Kanban FactBox.</span></span>  
3. <span data-ttu-id="93905-112">Í reitnum vinnuflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="93905-112">In the Work cell field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="93905-113">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="93905-113">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="93905-114">Velja vinnuflokkur 1250.</span><span class="sxs-lookup"><span data-stu-id="93905-114">Select work cell 1250.</span></span> <span data-ttu-id="93905-115">Þetta sía yfirlitið til að birta aðeins vinnslur fyrir vinnuflokk 1250.</span><span class="sxs-lookup"><span data-stu-id="93905-115">This will filter the view to display only the jobs for work cell 1250.</span></span>  
5. <span data-ttu-id="93905-116">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="93905-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="93905-117">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="93905-117">Click Select.</span></span>

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a><span data-ttu-id="93905-118">Áætlun kanban-vinnslu í fyrsta tímabilinu tiltæk</span><span class="sxs-lookup"><span data-stu-id="93905-118">Schedule a kanban job in the first available period</span></span>
1. <span data-ttu-id="93905-119">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="93905-119">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="93905-120">Veljið fyrstu línunni á listanum sem hefur stöðuna Ekki áætlað.</span><span class="sxs-lookup"><span data-stu-id="93905-120">Select the first row in the list that has the Not planned status.</span></span> <span data-ttu-id="93905-121">Brotinni línu í reitnum staða Vinnslu gefur til kynna Ekki áætluð.</span><span class="sxs-lookup"><span data-stu-id="93905-121">The dotted icon in the Job status field indicates not planned.</span></span>  
2. <span data-ttu-id="93905-122">Smellt er á Áætlun.</span><span class="sxs-lookup"><span data-stu-id="93905-122">Click Schedule.</span></span>
    * <span data-ttu-id="93905-123">Þetta mun áætla kanban-vinnslu á fyrsta tiltæka tímabili.</span><span class="sxs-lookup"><span data-stu-id="93905-123">This will schedule the kanban job in the first available period.</span></span>  
    * <span data-ttu-id="93905-124">Athugið að kanban-vinnslu er fluttur í lok lista þar sem hún hefur verið bætt við tímabil sem hefjast frá dagsetningunni í dag.</span><span class="sxs-lookup"><span data-stu-id="93905-124">Notice that the kanban job is moved to the end of the list because it has been added to the period starting from today.</span></span>  
    * <span data-ttu-id="93905-125">Ef tímabil sem hefjast frá dagsetningunni í dag er bókað til fulls mun vinnslu færð á fyrsta tiltæka tímabils.</span><span class="sxs-lookup"><span data-stu-id="93905-125">If the period starting from today is fully booked, the job will be moved to the first available period.</span></span>  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a><span data-ttu-id="93905-126">Raða tvær kanban-vinnslur fyrir tiltekinn dag</span><span class="sxs-lookup"><span data-stu-id="93905-126">Schedule two kanban jobs for a specific day</span></span>
1. <span data-ttu-id="93905-127">Í listanum skal velja línu 1.</span><span class="sxs-lookup"><span data-stu-id="93905-127">In the list, select row 1.</span></span>
    * <span data-ttu-id="93905-128">Þú ættir að sjá í fyrstu línunni hefur það staða Ekki áætluð í Vinnslustöðusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="93905-128">You should see that the first row has the Not planned status in the Job status field.</span></span>  
2. <span data-ttu-id="93905-129">Í listanum skal velja línu 2.</span><span class="sxs-lookup"><span data-stu-id="93905-129">In the list, select row 2.</span></span>
    * <span data-ttu-id="93905-130">Þú ættir að sjá í annarri línunni hefur það staða Ekki áætluð í Vinnslustöðusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="93905-130">You should see that the second row has the Not planned status in the Job status field.</span></span> <span data-ttu-id="93905-131">Nú ertu með fyrstu tveimur vinnslum sem valin.</span><span class="sxs-lookup"><span data-stu-id="93905-131">Now you have the first two jobs selected.</span></span>  
3. <span data-ttu-id="93905-132">Smellt er á Áætlun frá dagsetningu til að opna svargluggann fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="93905-132">Click Schedule from date to open the drop dialog.</span></span>
4. <span data-ttu-id="93905-133">Merkja eða afmerkja Hnekkja viðbrögðum við skorti á afkastagetu reitnum.</span><span class="sxs-lookup"><span data-stu-id="93905-133">Check or uncheck the Override capacity shortage reaction box.</span></span>
    * <span data-ttu-id="93905-134">Þessi valkostur gerir kleift að hnekkja sjálfgefin viðbrögð við skorti á afköstum.</span><span class="sxs-lookup"><span data-stu-id="93905-134">This option allows you to override the default capacity shortage reaction.</span></span>  
5. <span data-ttu-id="93905-135">Í reitnum viðbrögð við skorti á afkastagetu Velja 'Bæta við umbeðið tímabil'.</span><span class="sxs-lookup"><span data-stu-id="93905-135">In the Capacity shortage reaction field, select 'Add to the requested period'.</span></span>
    * <span data-ttu-id="93905-136">Þessi valkostur munu tryggja að vinnslunni er bætt við umbeðið tímabil, óháð því ef vinnuflokkur gæti verið ofhlaðinn.</span><span class="sxs-lookup"><span data-stu-id="93905-136">This option will ensure that the job is added to the requested period, regardless if the work cell might be overloaded.</span></span>  
6. <span data-ttu-id="93905-137">Smellt er á Áætlun.</span><span class="sxs-lookup"><span data-stu-id="93905-137">Click Schedule.</span></span>
    * <span data-ttu-id="93905-138">Athugið að báðir vinnslur er bætt við umbeðið tímabil.</span><span class="sxs-lookup"><span data-stu-id="93905-138">Notice that both jobs are added to the desired period.</span></span>  
    * <span data-ttu-id="93905-139">Hægt er að sjá álag fyrir hvert tímabil í hlutanum afkastageta Tímabilsins.</span><span class="sxs-lookup"><span data-stu-id="93905-139">In the Period capacity section, you can see the load for each period.</span></span> <span data-ttu-id="93905-140">Reiturinn Notkun sýnir áætlaða notkun á þessu tímabili.</span><span class="sxs-lookup"><span data-stu-id="93905-140">The Consumption field shows the scheduled consumption in this period.</span></span> <span data-ttu-id="93905-141">Ef áætluð notkun er hærri en tiltæk afkastageta í þetta tímabil er valið ofhlaðin notkun.</span><span class="sxs-lookup"><span data-stu-id="93905-141">If the scheduled consumption is higher than the available capacity in this period, the overloaded consumption will be selected.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]