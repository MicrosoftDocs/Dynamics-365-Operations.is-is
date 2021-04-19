---
title: Bakfæra stöðu kanban-vinnslu
description: Þetta ferli leggur áherslu á skipti aftur rangt staða kanban-vinnsla.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ee0ace8ff57b91828eb055658af5c8ecc50064ad
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831915"
---
# <a name="revert-kanban-job-status"></a><span data-ttu-id="135d5-103">Bakfæra stöðu kanban-vinnslu</span><span class="sxs-lookup"><span data-stu-id="135d5-103">Revert kanban job status</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="135d5-104">Þetta ferli leggur áherslu á skipti aftur rangt staða kanban-vinnsla.</span><span class="sxs-lookup"><span data-stu-id="135d5-104">This procedure focuses on reverting an incorrect kanban job status.</span></span> <span data-ttu-id="135d5-105">Þetta er gagnlegt í tilfellum starfsmaður á vél uppfærir röng vinnslu eða stillir ranga stöðu fyrir mistök.</span><span class="sxs-lookup"><span data-stu-id="135d5-105">This is useful in case the machine operator updates the wrong job, or sets the wrong status by mistake.</span></span> <span data-ttu-id="135d5-106">Í þessu ferli kanban-vinnsla er skráð sem undirbjó fyrir mistök og stöðu hefur verið snúa aftur.</span><span class="sxs-lookup"><span data-stu-id="135d5-106">In this procedure, a kanban job is registered as prepared by mistake, and the status is reverted.</span></span> <span data-ttu-id="135d5-107">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="135d5-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="135d5-108">Þetta ferli er ætluð fyrir verkstæðisstjóri eða starfsmaður á vél í lean-framleiðsla fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="135d5-108">This procedure is intended for the shop supervisor or machine operator working in a lean manufacturing company.</span></span>


## <a name="open-process-board-for-the-work-cell"></a><span data-ttu-id="135d5-109">Opna ferilspjald fyrir vinnuflokki</span><span class="sxs-lookup"><span data-stu-id="135d5-109">Open process board for the work cell</span></span>
1. <span data-ttu-id="135d5-110">Fara í Kanban-spjald fyrir vinnslukenni verks</span><span class="sxs-lookup"><span data-stu-id="135d5-110">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="135d5-111">Sláið inn eða veldu gildi í reitnum vinnuflokkur.</span><span class="sxs-lookup"><span data-stu-id="135d5-111">In the Work cell field, enter or select a value.</span></span>
    * <span data-ttu-id="135d5-112">Velja vinnuflokkur 1260.</span><span class="sxs-lookup"><span data-stu-id="135d5-112">Select work cell 1260.</span></span>  

## <a name="prepare-kanban-job"></a><span data-ttu-id="135d5-113">Undirbúa kanban-vinnslu</span><span class="sxs-lookup"><span data-stu-id="135d5-113">Prepare kanban job</span></span>
1. <span data-ttu-id="135d5-114">Smellt er á Undirbúa.</span><span class="sxs-lookup"><span data-stu-id="135d5-114">Click Prepare.</span></span>
    * <span data-ttu-id="135d5-115">Ef ekki er hægt að smella á Undirbúa þar sem hún er grátóna, ganga úr skugga um að valin kanban-vinnsla hefur stöðuna Áætlaðar, sem er tilgreind með því tóma kanban-tákn.</span><span class="sxs-lookup"><span data-stu-id="135d5-115">If you can't click Prepare because it is grayed out, make sure that the selected kanban job has status Planned, which is indicated by the empty kanban icon.</span></span> <span data-ttu-id="135d5-116">Ef ekki tekst að Undirbúa, ganga úr skugga um að allt efni í tiltektarlistanum eru tiltækar.</span><span class="sxs-lookup"><span data-stu-id="135d5-116">If Prepare fails, make sure that all materials in the Picking list are available.</span></span>  
2. <span data-ttu-id="135d5-117">Á listanum, veljið undirbúin vinnslu.</span><span class="sxs-lookup"><span data-stu-id="135d5-117">In the list, select the prepared job.</span></span>
    * <span data-ttu-id="135d5-118">Veljið vinnsluna sem hefur nýlega verið undirbúið.</span><span class="sxs-lookup"><span data-stu-id="135d5-118">Select the first job that you have just prepared.</span></span>  
    * <span data-ttu-id="135d5-119">Athugið að staða vinnslur er undirbúin, sem er tilgreint með þríhyrningur innan kanban-tákn.</span><span class="sxs-lookup"><span data-stu-id="135d5-119">Notice that the jobs status is prepared, which is indicated with a triangle inside the kanban icon.</span></span>  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a><span data-ttu-id="135d5-120">Snúa aftur stöðu undirbúin kanban-vinnslu</span><span class="sxs-lookup"><span data-stu-id="135d5-120">Revert the status of the prepared kanban job</span></span>
1. <span data-ttu-id="135d5-121">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="135d5-121">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="135d5-122">Veljið fyrsta vinnslan sem var undirbúin.</span><span class="sxs-lookup"><span data-stu-id="135d5-122">Select the first job that was prepared.</span></span>  
2. <span data-ttu-id="135d5-123">Í aðgerðasvæðinu er smellt á framleiðsla</span><span class="sxs-lookup"><span data-stu-id="135d5-123">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="135d5-124">Smellt er á stöðu snúa aftur.</span><span class="sxs-lookup"><span data-stu-id="135d5-124">Click Revert status.</span></span>
    * <span data-ttu-id="135d5-125">Hægt er að nota annarri kanban-reglu þegar eftirfarandi skilyrði eru sönn:-áfyllingaráætlun er sama fyrir bæði reglur.</span><span class="sxs-lookup"><span data-stu-id="135d5-125">You can use an alternative kanban rule when the following conditions are true:  - The replenishment strategy is the same for both rules.</span></span>  <span data-ttu-id="135d5-126">- Útgáfa framleiðsluflæði er það sama fyrir bæði reglur.</span><span class="sxs-lookup"><span data-stu-id="135d5-126">- The version of the production flow is the same for both rules.</span></span>  <span data-ttu-id="135d5-127">- Afurð sem er uppgefið er það sama fyrir bæði reglur.</span><span class="sxs-lookup"><span data-stu-id="135d5-127">- The product that is supplied is the same for both rules.</span></span>  <span data-ttu-id="135d5-128">- Niður á við verkþætti sem eru skilgreind fyrir síðustu aðgerð kanban-reglur verður að vera það sama fyrir bæði reglur.</span><span class="sxs-lookup"><span data-stu-id="135d5-128">- Any downstream activities that are configured for the last activity of the kanban rules must be the same for both rules.</span></span>  <span data-ttu-id="135d5-129">- Skilgreina verður sama uppgefin birgðavíddir fyrir báðar reglurnar.</span><span class="sxs-lookup"><span data-stu-id="135d5-129">- The same supplied inventory dimensions must be configured for both rules.</span></span>  <span data-ttu-id="135d5-130">- Staða afgreiðslueiningar verður að vera Ekki úthlutað.</span><span class="sxs-lookup"><span data-stu-id="135d5-130">- The status of the handling unit must be Not assigned.</span></span>  <span data-ttu-id="135d5-131">- Skilgreining fyrir tilvikskanbön verður að vera það sama.</span><span class="sxs-lookup"><span data-stu-id="135d5-131">- The configuration for event kanbans must be the same.</span></span>  
    * <span data-ttu-id="135d5-132">Tryggja skal að nýja staðan er Áætluð.</span><span class="sxs-lookup"><span data-stu-id="135d5-132">Ensure that the new status is Planned.</span></span>  
4. <span data-ttu-id="135d5-133">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="135d5-133">Click OK.</span></span>
5. <span data-ttu-id="135d5-134">Í listanum skal afmerkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="135d5-134">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="135d5-135">Velja sömu vinnslu.</span><span class="sxs-lookup"><span data-stu-id="135d5-135">Select the same job.</span></span>  
    * <span data-ttu-id="135d5-136">Athugið staða vinnslu fyrir kanban-vinnsla hefur verið breytt í áætlað, sem er tilgreind með tómu kanban tákn.</span><span class="sxs-lookup"><span data-stu-id="135d5-136">Notice that the job status for the kanban job is reverted to Planned, which is indicated by an empty kanban icon.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]