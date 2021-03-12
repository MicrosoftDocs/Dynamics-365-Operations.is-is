---
title: Færa áætlaðar kanban-vinnslur
description: Þetta ferli leggur áherslu á að færa áætluðum ferli kanban-vinnslum á annað tímabil.
author: ChristianRytt
manager: tfehr
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2769a7d519e12613796025b658db0b08cdfc4fde
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4961641"
---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="ee5ec-103">Færa áætlaðar kanban-vinnslur</span><span class="sxs-lookup"><span data-stu-id="ee5ec-103">Move scheduled kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee5ec-104">Þetta ferli leggur áherslu á að færa áætluðum ferli kanban-vinnslum á annað tímabil.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="ee5ec-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ee5ec-106">Þetta ferli er ætluð fyrir yfirmaður vinnusals eða framleiðslustjóri sem vinnur með kanban.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="ee5ec-107">Velja áætlaðar kanban-vinnslur.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="ee5ec-108">Opna **Framleiðslustýring > Kanban > Kanban-vinnsluröðun**.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="ee5ec-109">Í reitnum **Vinnuflokkur** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="ee5ec-110">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="ee5ec-111">Velja vinnuflokkur 1250.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="ee5ec-112">Smellið á **Velja**.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-112">Click **Select**.</span></span> 

5. <span data-ttu-id="ee5ec-113">Í reitnum **Birta stöðu á vinnslu** skal velja **Áætlað**.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="ee5ec-114">Þetta síar vinnslu til að birta aðeins áætlað kanban-vinnslurnar.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="ee5ec-115">Flytja kanban-vinnslur á annað tímabil.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="ee5ec-116">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="ee5ec-117">Veljið vinnslu sem er með stöðuna **Áætluð vinnsla**, t.d. vinnslu sem er tímasett 20. desember 2012 í reitnum **Áætlað tímabil**.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="ee5ec-118">Færið síðan vinnsluna í fyrra tímabil</span><span class="sxs-lookup"><span data-stu-id="ee5ec-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="ee5ec-119">Smellið á **Fyrra tímabil**.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="ee5ec-120">Smellið á **Aftast** til að færa vinnsluna aftast í vinnslulista og gera hana að síðustu vinnslunni á fyrra tímabili.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="ee5ec-121">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="ee5ec-122">Veljið vinnslu sem er með stöðuna **Áætluð vinnsla**, t.d. vinnslu sem er tímasett 18. desember 2012 í reitnum **Áætlað tímabil**.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="ee5ec-123">Færið síðan vinnsluna í næsta tímabil.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="ee5ec-124">Smellið á **Næsta tímabil**.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="ee5ec-125">Smellið á **Fremst** til að færa vinnsluna fremst í vinnslulista og gera hana að fyrstu vinnslunni á fyrra tímabili.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="ee5ec-126">Færa vinnslu innan tímabils.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="ee5ec-127">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="ee5ec-128">Veljið vinnslu sem er með stöðuna „Áætluð vinnsla“, t.d. önnur vinnslan sem er tímasett 19. desember 2012 í reitnum **Áætlað tímabil**.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="ee5ec-129">Færa næst vinnslu innan þess tímabils sem er áætlað.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="ee5ec-130">Smellið á **Áfram**.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-130">Click **Forward**.</span></span> <span data-ttu-id="ee5ec-131">Athugað að vinnslan er fluttur einnar línu niður á listanum.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="ee5ec-132">Smellið á **Til baka**.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-132">Click **Backward**.</span></span> <span data-ttu-id="ee5ec-133">Athugaðu að vinnslan er fluttur einnar línu upp á listanum.</span><span class="sxs-lookup"><span data-stu-id="ee5ec-133">Notice that the job is moved one line up on the list.</span></span>
