--- 
title: "Færa áætlaðar kanban-vinnslur"
description: "Þetta ferli leggur áherslu á að færa áætluðum ferli kanban-vinnslum á annað tímabil."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 6461e5638eaddeaeaef82304b7976bad350b331e
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="fb901-103">Færa áætlaðar kanban-vinnslur</span><span class="sxs-lookup"><span data-stu-id="fb901-103">Move scheduled kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fb901-104">Þetta ferli leggur áherslu á að færa áætluðum ferli kanban-vinnslum á annað tímabil.</span><span class="sxs-lookup"><span data-stu-id="fb901-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="fb901-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="fb901-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="fb901-106">Þetta ferli er ætluð fyrir yfirmaður vinnusals eða framleiðslustjóri sem vinnur með kanban.</span><span class="sxs-lookup"><span data-stu-id="fb901-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>


## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="fb901-107">Veljið áætlað kanban-vinnslur</span><span class="sxs-lookup"><span data-stu-id="fb901-107">Select scheduled kanban jobs</span></span>
1. <span data-ttu-id="fb901-108">Fara í framleiðslustýringu > Kanban > Tímaáætlun Kanban-vinnslu.</span><span class="sxs-lookup"><span data-stu-id="fb901-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span></span>
2. <span data-ttu-id="fb901-109">!MtCMR!Í reitnum vinnuflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="fb901-109">!MtCMR!In the Work cell field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="fb901-110">áçêìõý!</span><span class="sxs-lookup"><span data-stu-id="fb901-110">áçêìõý !</span></span>
3. <span data-ttu-id="fb901-111">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="fb901-111">Markér den valgte række på listen.</span></span>
    * <span data-ttu-id="fb901-112">Velja vinnuflokkur 1250.</span><span class="sxs-lookup"><span data-stu-id="fb901-112">Select work cell 1250.</span></span>  
4. <span data-ttu-id="fb901-113">Klik på Velja.</span><span class="sxs-lookup"><span data-stu-id="fb901-113">Klik på Select.</span></span>
5. <span data-ttu-id="fb901-114">Vælg 'Planlagt' i feltet Display job status.</span><span class="sxs-lookup"><span data-stu-id="fb901-114">Vælg 'Planlagt' i feltet Display job status.</span></span>
    * <span data-ttu-id="fb901-115">Þetta síar vinnslu til að birta aðeins áætlað kanban-vinnslurnar.</span><span class="sxs-lookup"><span data-stu-id="fb901-115">This filters the job list to display only the scheduled kanban jobs.</span></span>  

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="fb901-116">Flytja kanban-vinnslum á annað tímabil</span><span class="sxs-lookup"><span data-stu-id="fb901-116">Move kanban jobs to a different period</span></span>
1. <span data-ttu-id="fb901-117">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="fb901-117">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="fb901-118">Veljið vinnslu sem er með stöðuna Áætluð vinnsa, t.d. með vinnsluraðað á 20 Desember 2012 í Áætluð svæðinu áætlað tímabil.</span><span class="sxs-lookup"><span data-stu-id="fb901-118">Select a job that has the Planned job status, for example, a job scheduled on December 20, 2012  in the Planned period field.</span></span> <span data-ttu-id="fb901-119">Færið síðan vinnsluna í fyrra tímabil</span><span class="sxs-lookup"><span data-stu-id="fb901-119">Then move the job to the previous period.</span></span>  
2. <span data-ttu-id="fb901-120">Klik på Fyrra tímabil.</span><span class="sxs-lookup"><span data-stu-id="fb901-120">Klik på Previous period.</span></span>
3. <span data-ttu-id="fb901-121">Klik på Lok.</span><span class="sxs-lookup"><span data-stu-id="fb901-121">Klik på End.</span></span>
    * <span data-ttu-id="fb901-122">Þetta mun flytja starf í lok vinnslulistanum sem síðustu vinnslu í fyrra tímabili.</span><span class="sxs-lookup"><span data-stu-id="fb901-122">This will move the job to the end of the job list as the last job in the previous period.</span></span>  
4. <span data-ttu-id="fb901-123">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="fb901-123">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="fb901-124">Veljið vinnslu sem er með stöðuna Áætluð vinnsla, t.d. með vinnsluraðað á 18. Desember 2012 í svæðinu Áætlað tímabil.</span><span class="sxs-lookup"><span data-stu-id="fb901-124">Select a job that has the Planned job status, for example, a job scheduled on December 18, 2012 in the Planned period field.</span></span> <span data-ttu-id="fb901-125">Færið síðan vinnsluna í næsta tímabil.</span><span class="sxs-lookup"><span data-stu-id="fb901-125">Then move the job to the next period.</span></span>  
5. <span data-ttu-id="fb901-126">Klik på Næsta tímabils.</span><span class="sxs-lookup"><span data-stu-id="fb901-126">Klik på Next period.</span></span>
6. <span data-ttu-id="fb901-127">Klik på Upphaf.</span><span class="sxs-lookup"><span data-stu-id="fb901-127">Klik på Start.</span></span>
    * <span data-ttu-id="fb901-128">Þetta mun flytja starf í byrjun vinnslulistanum sem fyrstu vinnslu í fyrra tímabili.</span><span class="sxs-lookup"><span data-stu-id="fb901-128">This will move the job to the start of the job list as the first job in the previous period.</span></span>  

## <a name="task-move-a-job-within-a-period"></a><span data-ttu-id="fb901-129">Verk: Færa vinnslu innan tímabils</span><span class="sxs-lookup"><span data-stu-id="fb901-129">Task: Move a job within a period</span></span>
1. <span data-ttu-id="fb901-130">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="fb901-130">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="fb901-131">Veljið vinnslu sem er með stöðuna Áætluð vinnsla, t.d. með annað vinnsluraðað verk á 19 Desember 2012 í svæðinu Áætlað tímabil.</span><span class="sxs-lookup"><span data-stu-id="fb901-131">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the Planned period field.</span></span> <span data-ttu-id="fb901-132">Færa næst vinnslu innan þess tímabils sem er áætlað.</span><span class="sxs-lookup"><span data-stu-id="fb901-132">Then move the job within the planned period.</span></span>  
2. <span data-ttu-id="fb901-133">Klik på Áfram.</span><span class="sxs-lookup"><span data-stu-id="fb901-133">Klik på Forward.</span></span>
    * <span data-ttu-id="fb901-134">Athugað að vinnslan er fluttur einnar línu niður á listanum.</span><span class="sxs-lookup"><span data-stu-id="fb901-134">Notice that the job is moved one line down on the list.</span></span>  
3. <span data-ttu-id="fb901-135">Klik på Aftur.</span><span class="sxs-lookup"><span data-stu-id="fb901-135">Klik på Backward.</span></span>
    * <span data-ttu-id="fb901-136">Athugaðu að vinnslan er fluttur einnar línu upp á listanum.</span><span class="sxs-lookup"><span data-stu-id="fb901-136">Notice that the job is moved one line up on the list.</span></span>  


