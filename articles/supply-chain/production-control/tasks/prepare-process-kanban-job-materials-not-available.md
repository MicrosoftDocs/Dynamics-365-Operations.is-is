---
title: Undirbúa kanban-vinnslu ferlis þegar efni er ekki tiltækt fyrir vinnuflokk
description: Þetta ferli leggur áherslu á undirbúning kanban-vinnslu þegar einhver hráefni eru ekki tiltækar fyrir vinnuflokkur, þar af leiðandi nauðsynlegt er að taka til efni úr vöruhúsi.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bba9e5cb7dfddd2a80a37e7a57fdf94a91341e8f
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843626"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="80bb6-103">Undirbúa kanban-vinnslu ferlis þegar efni er ekki tiltækt fyrir vinnuflokk</span><span class="sxs-lookup"><span data-stu-id="80bb6-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="80bb6-104">Þetta ferli leggur áherslu á undirbúning kanban-vinnslu þegar einhver hráefni eru ekki tiltækar fyrir vinnuflokkur, þar af leiðandi nauðsynlegt er að taka til efni úr vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="80bb6-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="80bb6-105">Ferli "Undirbúa á kanban-vinnslu þegar efni er tiltækt" er skilyrði fyrir stofnun þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="80bb6-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="80bb6-106">Þetta ferli er ætluð fyrir á starfsmaður á vél.</span><span class="sxs-lookup"><span data-stu-id="80bb6-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="80bb6-107">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="80bb6-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="80bb6-108">Fara í Framleiðslustýring > Kanban > Kanban-spjald fyrir ferlisvinnslur.</span><span class="sxs-lookup"><span data-stu-id="80bb6-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="80bb6-109">Í reitnum vinnuflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="80bb6-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="80bb6-110">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="80bb6-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="80bb6-111">Velja vinnuflokkur 1250.</span><span class="sxs-lookup"><span data-stu-id="80bb6-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="80bb6-112">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="80bb6-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="80bb6-113">Velja Kanban 000356.</span><span class="sxs-lookup"><span data-stu-id="80bb6-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="80bb6-114">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="80bb6-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="80bb6-115">Í listanum skal afvelja línu 4.</span><span class="sxs-lookup"><span data-stu-id="80bb6-115">In the list, deselect row 4.</span></span> <span data-ttu-id="80bb6-116">eða Velja línu 4 ef þú hefur ekki lokið verkefninu "Undirbúa á kanban-vinnslu þegar efni er tiltækt."</span><span class="sxs-lookup"><span data-stu-id="80bb6-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="80bb6-117">Víxla útvíkkun á liðnum tiltektarlisti.</span><span class="sxs-lookup"><span data-stu-id="80bb6-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="80bb6-118">Táknið Engin færsla í birgðastaða gefir til kynna að 48 ea fyrir vöru P0002 vantar fyrir vinnuflokkur.</span><span class="sxs-lookup"><span data-stu-id="80bb6-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="80bb6-119">Flytja efni til vinnuflokkur</span><span class="sxs-lookup"><span data-stu-id="80bb6-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="80bb6-120">Víxla útvíkkun á liðnum millifærsla vinnslu.</span><span class="sxs-lookup"><span data-stu-id="80bb6-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="80bb6-121">Notið flýtiafmörkun til að sía á vörunúmerasvæðinu með gildinu „P0002“.</span><span class="sxs-lookup"><span data-stu-id="80bb6-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="80bb6-122">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="80bb6-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="80bb6-123">Smellið á „Byrja“.</span><span class="sxs-lookup"><span data-stu-id="80bb6-123">Click Start.</span></span>
    * <span data-ttu-id="80bb6-124">Flutningur er í gangi.</span><span class="sxs-lookup"><span data-stu-id="80bb6-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="80bb6-125">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="80bb6-125">Click Complete.</span></span>
    * <span data-ttu-id="80bb6-126">Nú er tiltækur á tiltektarlista kanban-vinnslu P0002 vöru.</span><span class="sxs-lookup"><span data-stu-id="80bb6-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="80bb6-127">Þetta þýðir að við getum undirbúa kanban með öllum nauðsynlegum efni.</span><span class="sxs-lookup"><span data-stu-id="80bb6-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="80bb6-128">Smellt er á Undirbúa.</span><span class="sxs-lookup"><span data-stu-id="80bb6-128">Click Prepare.</span></span>
    * <span data-ttu-id="80bb6-129">Athugið að tákn í vinnslustöðu tilgreinir vinnslan er nú tilbúið.</span><span class="sxs-lookup"><span data-stu-id="80bb6-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  

