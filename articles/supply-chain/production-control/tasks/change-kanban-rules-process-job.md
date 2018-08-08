--- 
title: Breyta kanban-reglum fyrir vinnsluverk
description: "Þetta ferli áherslu á að breyta kanban-reglu fyrir ákveðið kanban."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
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
ms.openlocfilehash: 8fc47751534af69300bf8f0bdb7424043cab7b26
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="6e19e-103">Breyta kanban-reglum fyrir vinnsluverk</span><span class="sxs-lookup"><span data-stu-id="6e19e-103">Change kanban rules for a process job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e19e-104">Þetta ferli áherslu á að breyta kanban-reglu fyrir ákveðið kanban.</span><span class="sxs-lookup"><span data-stu-id="6e19e-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="6e19e-105">Þetta er gagnlegt til að hlaða tilföng eða við bilun.</span><span class="sxs-lookup"><span data-stu-id="6e19e-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="6e19e-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="6e19e-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="6e19e-107">Þetta ferli er ætluð fyrir skipuleggjandann, sem vinnur hjá lean framleiðslufyrirtæki, og ber ábyrgð á virðisstraumnum.</span><span class="sxs-lookup"><span data-stu-id="6e19e-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="6e19e-108">Afrita kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="6e19e-108">Copy kanban rule</span></span>
1. <span data-ttu-id="6e19e-109">Fara á kanban-reglur.</span><span class="sxs-lookup"><span data-stu-id="6e19e-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="6e19e-110">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="6e19e-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6e19e-111">Velja tilviksreglur kanbans 000022 L0001.</span><span class="sxs-lookup"><span data-stu-id="6e19e-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="6e19e-112">Smellt er á Afrita kanban-reglu.</span><span class="sxs-lookup"><span data-stu-id="6e19e-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="6e19e-113">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6e19e-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="6e19e-114">Breyta kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="6e19e-114">Change kanban rule</span></span>
1. <span data-ttu-id="6e19e-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6e19e-115">Close the page.</span></span>
2. <span data-ttu-id="6e19e-116">Fara í vinnsluröðun kanban</span><span class="sxs-lookup"><span data-stu-id="6e19e-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="6e19e-117">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="6e19e-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6e19e-118">Velja línuna með Kanban 000177.</span><span class="sxs-lookup"><span data-stu-id="6e19e-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="6e19e-119">Smellt er á nota aðra kanban-regla.</span><span class="sxs-lookup"><span data-stu-id="6e19e-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="6e19e-120">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="6e19e-120">Click Next.</span></span>
6. <span data-ttu-id="6e19e-121">Sláðu inn eða veldu gildi í reitnum kanban-regla.</span><span class="sxs-lookup"><span data-stu-id="6e19e-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="6e19e-122">Velja kanban-reglu sem áður var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="6e19e-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="6e19e-123">Þetta er kanban-regla með hæsta númer.</span><span class="sxs-lookup"><span data-stu-id="6e19e-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="6e19e-124">Smellt er á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="6e19e-124">Click Finish.</span></span>
    * <span data-ttu-id="6e19e-125">Nú er kanban-vinnslu með annarri kanban-reglu.</span><span class="sxs-lookup"><span data-stu-id="6e19e-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="6e19e-126">Þetta getur verið jafna út hleðslu vinnuflokkana .</span><span class="sxs-lookup"><span data-stu-id="6e19e-126">This can be useful to level load work cells.</span></span>  


