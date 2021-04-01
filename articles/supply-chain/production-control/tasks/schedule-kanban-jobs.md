---
title: Áætla kanban-vinnslu
description: Þetta ferli leggur áherslu á röðun ferlis kanban-vinnslur fyrir tiltekna vinnuflokkur.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 30f7c431b3d27a534e53540c41768ea55c8dd39f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222802"
---
# <a name="schedule-kanban-jobs"></a><span data-ttu-id="cc2aa-103">Áætla kanban-vinnslu</span><span class="sxs-lookup"><span data-stu-id="cc2aa-103">Schedule kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cc2aa-104">Þetta ferli leggur áherslu á röðun ferlis kanban-vinnslur fyrir tiltekna vinnuflokkur.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-104">This procedure focuses on scheduling process kanban jobs for a specific work cell.</span></span> <span data-ttu-id="cc2aa-105">Ferli "Undirbúa ferli kanban-vinnslu þegar efni er tiltækt" er skilyrði fyrir stofnun þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-105">The procedure "Prepare a process kanban job when materials are not available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="cc2aa-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="cc2aa-107">Þetta verk er ætluð fyrir yfirmaður vinnusals og framleiðslustjóri sem vinnur með kanban.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-107">This task is intended for the shop floor supervisor and production planner working with kanbans.</span></span>


## <a name="select-kanban-jobs-for-a-work-cell"></a><span data-ttu-id="cc2aa-108">Velja kanban-vinnslur fyrir vinnuflokks</span><span class="sxs-lookup"><span data-stu-id="cc2aa-108">Select kanban jobs for a work cell</span></span>
1. <span data-ttu-id="cc2aa-109">Fara í Framleiðslustýringar > Kanban > Áætlun kanban-vinnslu.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-109">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="cc2aa-110">Útvíkka upplýsingakassa Afkastageta Tímabilsins</span><span class="sxs-lookup"><span data-stu-id="cc2aa-110">Expand the Period capacity fact box</span></span>
    * <span data-ttu-id="cc2aa-111">Útvíkka kanban-upplýsingakassa.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-111">Expand the Kanban FactBox.</span></span>  
3. <span data-ttu-id="cc2aa-112">Í reitnum vinnuflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-112">In the Work cell field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="cc2aa-113">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-113">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="cc2aa-114">Velja vinnuflokkur 1250.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-114">Select work cell 1250.</span></span> <span data-ttu-id="cc2aa-115">Þetta sía yfirlitið til að birta aðeins vinnslur fyrir vinnuflokk 1250.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-115">This will filter the view to display only the jobs for work cell 1250.</span></span>  
5. <span data-ttu-id="cc2aa-116">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="cc2aa-117">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-117">Click Select.</span></span>

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a><span data-ttu-id="cc2aa-118">Áætlun kanban-vinnslu í fyrsta tímabilinu tiltæk</span><span class="sxs-lookup"><span data-stu-id="cc2aa-118">Schedule a kanban job in the first available period</span></span>
1. <span data-ttu-id="cc2aa-119">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-119">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="cc2aa-120">Veljið fyrstu línunni á listanum sem hefur stöðuna Ekki áætlað.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-120">Select the first row in the list that has the Not planned status.</span></span> <span data-ttu-id="cc2aa-121">Brotinni línu í reitnum staða Vinnslu gefur til kynna Ekki áætluð.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-121">The dotted icon in the Job status field indicates not planned.</span></span>  
2. <span data-ttu-id="cc2aa-122">Smellt er á Áætlun.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-122">Click Schedule.</span></span>
    * <span data-ttu-id="cc2aa-123">Þetta mun áætla kanban-vinnslu á fyrsta tiltæka tímabili.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-123">This will schedule the kanban job in the first available period.</span></span>  
    * <span data-ttu-id="cc2aa-124">Athugið að kanban-vinnslu er fluttur í lok lista þar sem hún hefur verið bætt við tímabil sem hefjast frá dagsetningunni í dag.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-124">Notice that the kanban job is moved to the end of the list because it has been added to the period starting from today.</span></span>  
    * <span data-ttu-id="cc2aa-125">Ef tímabil sem hefjast frá dagsetningunni í dag er bókað til fulls mun vinnslu færð á fyrsta tiltæka tímabils.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-125">If the period starting from today is fully booked, the job will be moved to the first available period.</span></span>  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a><span data-ttu-id="cc2aa-126">Raða tvær kanban-vinnslur fyrir tiltekinn dag</span><span class="sxs-lookup"><span data-stu-id="cc2aa-126">Schedule two kanban jobs for a specific day</span></span>
1. <span data-ttu-id="cc2aa-127">Í listanum skal velja línu 1.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-127">In the list, select row 1.</span></span>
    * <span data-ttu-id="cc2aa-128">Þú ættir að sjá í fyrstu línunni hefur það staða Ekki áætluð í Vinnslustöðusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-128">You should see that the first row has the Not planned status in the Job status field.</span></span>  
2. <span data-ttu-id="cc2aa-129">Í listanum skal velja línu 2.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-129">In the list, select row 2.</span></span>
    * <span data-ttu-id="cc2aa-130">Þú ættir að sjá í annarri línunni hefur það staða Ekki áætluð í Vinnslustöðusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-130">You should see that the second row has the Not planned status in the Job status field.</span></span> <span data-ttu-id="cc2aa-131">Nú ertu með fyrstu tveimur vinnslum sem valin.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-131">Now you have the first two jobs selected.</span></span>  
3. <span data-ttu-id="cc2aa-132">Smellt er á Áætlun frá dagsetningu til að opna svargluggann fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-132">Click Schedule from date to open the drop dialog.</span></span>
4. <span data-ttu-id="cc2aa-133">Merkja eða afmerkja Hnekkja viðbrögðum við skorti á afkastagetu reitnum.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-133">Check or uncheck the Override capacity shortage reaction box.</span></span>
    * <span data-ttu-id="cc2aa-134">Þessi valkostur gerir kleift að hnekkja sjálfgefin viðbrögð við skorti á afköstum.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-134">This option allows you to override the default capacity shortage reaction.</span></span>  
5. <span data-ttu-id="cc2aa-135">Í reitnum viðbrögð við skorti á afkastagetu Velja 'Bæta við umbeðið tímabil'.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-135">In the Capacity shortage reaction field, select 'Add to the requested period'.</span></span>
    * <span data-ttu-id="cc2aa-136">Þessi valkostur munu tryggja að vinnslunni er bætt við umbeðið tímabil, óháð því ef vinnuflokkur gæti verið ofhlaðinn.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-136">This option will ensure that the job is added to the requested period, regardless if the work cell might be overloaded.</span></span>  
6. <span data-ttu-id="cc2aa-137">Smellt er á Áætlun.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-137">Click Schedule.</span></span>
    * <span data-ttu-id="cc2aa-138">Athugið að báðir vinnslur er bætt við umbeðið tímabil.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-138">Notice that both jobs are added to the desired period.</span></span>  
    * <span data-ttu-id="cc2aa-139">Hægt er að sjá álag fyrir hvert tímabil í hlutanum afkastageta Tímabilsins.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-139">In the Period capacity section, you can see the load for each period.</span></span> <span data-ttu-id="cc2aa-140">Reiturinn Notkun sýnir áætlaða notkun á þessu tímabili.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-140">The Consumption field shows the scheduled consumption in this period.</span></span> <span data-ttu-id="cc2aa-141">Ef áætluð notkun er hærri en tiltæk afkastageta í þetta tímabil er valið ofhlaðin notkun.</span><span class="sxs-lookup"><span data-stu-id="cc2aa-141">If the scheduled consumption is higher than the available capacity in this period, the overloaded consumption will be selected.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]