--- 
title: Keyra kanban-vinnsluverk
description: "Þetta ferli leggur áherslu á framkvæmd kanban-ferlisvinnslu."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 4f0579e9bccdcf240d33bb7b936bd9f9f7619028
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="execute-kanban-process-jobs"></a><span data-ttu-id="9f799-103">Keyra kanban-vinnsluverk</span><span class="sxs-lookup"><span data-stu-id="9f799-103">Execute kanban process jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f799-104">Þetta ferli leggur áherslu á framkvæmd kanban-ferlisvinnslu.</span><span class="sxs-lookup"><span data-stu-id="9f799-104">This procedure focuses on executing kanban process jobs.</span></span> <span data-ttu-id="9f799-105">Fyrsta vinnslan er lokið með áætlað magn og hefur engar villur.</span><span class="sxs-lookup"><span data-stu-id="9f799-105">The first job is completed with the expected quantity and has no errors.</span></span> <span data-ttu-id="9f799-106">Annari vinnslu er lokið með villum.</span><span class="sxs-lookup"><span data-stu-id="9f799-106">The second job is completed with errors.</span></span> <span data-ttu-id="9f799-107">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="9f799-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="9f799-108">Þetta ferli er ætluð fyrir á starfsmaður á vél.</span><span class="sxs-lookup"><span data-stu-id="9f799-108">This procedure is intended for the machine operator.</span></span>


## <a name="select-a-kanban-job"></a><span data-ttu-id="9f799-109">Veljið kanban-vinnslu.</span><span class="sxs-lookup"><span data-stu-id="9f799-109">Select a kanban job</span></span>
1. <span data-ttu-id="9f799-110">Fara í Framleiðslustýring > Kanban > Kanban-spjald fyrir ferlisvinnslur.</span><span class="sxs-lookup"><span data-stu-id="9f799-110">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="9f799-111">Í reitnum vinnuflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="9f799-111">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="9f799-112">Smellt er á línuna með 1250 tilfangaflokki.</span><span class="sxs-lookup"><span data-stu-id="9f799-112">Click the row with resource group 1250.</span></span> <span data-ttu-id="9f799-113">Þetta síar vinnslu til að birta aðeins vinnslur fyrir vinnuflokk 1250.</span><span class="sxs-lookup"><span data-stu-id="9f799-113">This filters the Jobs list to display only the jobs for work cell 1250.</span></span>
    * <span data-ttu-id="9f799-114">Merkja línuna sem hefur stöðuna Áætluð vinnslu.</span><span class="sxs-lookup"><span data-stu-id="9f799-114">Mark the row that has the Planned job status.</span></span>  

## <a name="complete-a-job-with-expected-quantity"></a><span data-ttu-id="9f799-115">Ljúka vinnslu með áætlað magn</span><span class="sxs-lookup"><span data-stu-id="9f799-115">Complete a job with expected quantity</span></span>
1. <span data-ttu-id="9f799-116">Stækka eða fella saman hlutann Upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="9f799-116">Expand or collapse the Details section.</span></span>
    * <span data-ttu-id="9f799-117">Þessi hluti sýnir mikilvægar upplýsingar um kortanúmer, vörunúmer, pantað magn, og aðgerðaheiti.</span><span class="sxs-lookup"><span data-stu-id="9f799-117">This section displays important information about card number, item number, quantity ordered, and activity name.</span></span>  
2. <span data-ttu-id="9f799-118">Útvíkka eða draga saman hlutann leiðbeiningar fyrir framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="9f799-118">Expand or collapse the Production instructions section.</span></span>
    * <span data-ttu-id="9f799-119">Þessi hluti sýnir leiðbeiningar fyrir framleiðslu fyrir aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="9f799-119">This section displays production instructions for the activity.</span></span> <span data-ttu-id="9f799-120">Leiðbeiningarnar má vera texta, myndir, teikningar og önnur skjöl.</span><span class="sxs-lookup"><span data-stu-id="9f799-120">The instructions can be text, pictures, drawings, and other documents.</span></span>  
3. <span data-ttu-id="9f799-121">Smellið á „Byrja“.</span><span class="sxs-lookup"><span data-stu-id="9f799-121">Click Start.</span></span>
    * <span data-ttu-id="9f799-122">Velja vinnsla sem ekki er kláruð.</span><span class="sxs-lookup"><span data-stu-id="9f799-122">Select a job that is not completed.</span></span> <span data-ttu-id="9f799-123">Nota stöðutákn í svæðinu staða vinnslu til að skoða stöðu vinnslunnar.</span><span class="sxs-lookup"><span data-stu-id="9f799-123">Use status icons in the Job status field to view job status.</span></span>      
4. <span data-ttu-id="9f799-124">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="9f799-124">Click Complete.</span></span>
    * <span data-ttu-id="9f799-125">Vinnslu er lokið með áætlaða gæði.</span><span class="sxs-lookup"><span data-stu-id="9f799-125">The job is completed with the expected quality.</span></span>  

## <a name="complete-a-job-with-errors"></a><span data-ttu-id="9f799-126">Ljúka vinnslu með villum</span><span class="sxs-lookup"><span data-stu-id="9f799-126">Complete a job with errors</span></span>
1. <span data-ttu-id="9f799-127">Smellið á „Byrja“.</span><span class="sxs-lookup"><span data-stu-id="9f799-127">Click Start.</span></span>
    * <span data-ttu-id="9f799-128">Þegar vinnslu er lokið er næstu vinnslu á listanum sjálfkrafa valið.</span><span class="sxs-lookup"><span data-stu-id="9f799-128">When a job is completed, the next job on the list is selected automatically.</span></span> <span data-ttu-id="9f799-129">Þess vegna þarf ekki vinnsla vera valin áður en smellt er á Ræsa.</span><span class="sxs-lookup"><span data-stu-id="9f799-129">This is why you don't need to select a job before you click Start.</span></span>  
2. <span data-ttu-id="9f799-130">Í aðgerðasvæðinu er smellt á framleiðsla</span><span class="sxs-lookup"><span data-stu-id="9f799-130">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="9f799-131">Smella á Lokið (upplýsingar)</span><span class="sxs-lookup"><span data-stu-id="9f799-131">Click Complete (details).</span></span>
4. <span data-ttu-id="9f799-132">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="9f799-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="9f799-133">Í reitnum gallað magn, skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="9f799-133">In the Error quantity field, enter a number.</span></span>
6. <span data-ttu-id="9f799-134">Í reitnum gallalaust magn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="9f799-134">In the Good quantity field, enter a number.</span></span>
7. <span data-ttu-id="9f799-135">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9f799-135">Click OK.</span></span>


