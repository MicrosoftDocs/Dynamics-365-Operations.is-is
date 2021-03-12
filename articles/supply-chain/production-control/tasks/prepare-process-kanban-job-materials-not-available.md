---
title: Undirbúa kanban-vinnslu ferlis þegar efni er ekki tiltækt fyrir vinnuflokk
description: Þetta ferli leggur áherslu á undirbúning kanban-vinnslu þegar einhver hráefni eru ekki tiltækar fyrir vinnuflokkur, þar af leiðandi nauðsynlegt er að taka til efni úr vöruhúsi.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: df0396a1d00e61ad82e52fc07779e239cd811ab8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994092"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="afdfb-103">Undirbúa kanban-vinnslu ferlis þegar efni er ekki tiltækt fyrir vinnuflokk</span><span class="sxs-lookup"><span data-stu-id="afdfb-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="afdfb-104">Þetta ferli leggur áherslu á undirbúning kanban-vinnslu þegar einhver hráefni eru ekki tiltækar fyrir vinnuflokkur, þar af leiðandi nauðsynlegt er að taka til efni úr vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="afdfb-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="afdfb-105">Ferli "Undirbúa á kanban-vinnslu þegar efni er tiltækt" er skilyrði fyrir stofnun þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="afdfb-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="afdfb-106">Þetta ferli er ætluð fyrir á starfsmaður á vél.</span><span class="sxs-lookup"><span data-stu-id="afdfb-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="afdfb-107">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="afdfb-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="afdfb-108">Fara í Framleiðslustýring > Kanban > Kanban-spjald fyrir ferlisvinnslur.</span><span class="sxs-lookup"><span data-stu-id="afdfb-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="afdfb-109">Í reitnum vinnuflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="afdfb-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="afdfb-110">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="afdfb-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="afdfb-111">Velja vinnuflokkur 1250.</span><span class="sxs-lookup"><span data-stu-id="afdfb-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="afdfb-112">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="afdfb-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="afdfb-113">Velja Kanban 000356.</span><span class="sxs-lookup"><span data-stu-id="afdfb-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="afdfb-114">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="afdfb-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="afdfb-115">Í listanum skal afvelja línu 4.</span><span class="sxs-lookup"><span data-stu-id="afdfb-115">In the list, deselect row 4.</span></span> <span data-ttu-id="afdfb-116">eða Velja línu 4 ef þú hefur ekki lokið verkefninu "Undirbúa á kanban-vinnslu þegar efni er tiltækt."</span><span class="sxs-lookup"><span data-stu-id="afdfb-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="afdfb-117">Víxla útvíkkun á liðnum tiltektarlisti.</span><span class="sxs-lookup"><span data-stu-id="afdfb-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="afdfb-118">Táknið Engin færsla í birgðastaða gefir til kynna að 48 ea fyrir vöru P0002 vantar fyrir vinnuflokkur.</span><span class="sxs-lookup"><span data-stu-id="afdfb-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="afdfb-119">Flytja efni til vinnuflokkur</span><span class="sxs-lookup"><span data-stu-id="afdfb-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="afdfb-120">Víxla útvíkkun á liðnum millifærsla vinnslu.</span><span class="sxs-lookup"><span data-stu-id="afdfb-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="afdfb-121">Notið flýtiafmörkun til að sía á vörunúmerasvæðinu með gildinu „P0002“.</span><span class="sxs-lookup"><span data-stu-id="afdfb-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="afdfb-122">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="afdfb-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="afdfb-123">Smellið á „Byrja“.</span><span class="sxs-lookup"><span data-stu-id="afdfb-123">Click Start.</span></span>
    * <span data-ttu-id="afdfb-124">Flutningur er í gangi.</span><span class="sxs-lookup"><span data-stu-id="afdfb-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="afdfb-125">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="afdfb-125">Click Complete.</span></span>
    * <span data-ttu-id="afdfb-126">Nú er tiltækur á tiltektarlista kanban-vinnslu P0002 vöru.</span><span class="sxs-lookup"><span data-stu-id="afdfb-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="afdfb-127">Þetta þýðir að við getum undirbúa kanban með öllum nauðsynlegum efni.</span><span class="sxs-lookup"><span data-stu-id="afdfb-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="afdfb-128">Smellt er á Undirbúa.</span><span class="sxs-lookup"><span data-stu-id="afdfb-128">Click Prepare.</span></span>
    * <span data-ttu-id="afdfb-129">Athugið að tákn í vinnslustöðu tilgreinir vinnslan er nú tilbúið.</span><span class="sxs-lookup"><span data-stu-id="afdfb-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  

