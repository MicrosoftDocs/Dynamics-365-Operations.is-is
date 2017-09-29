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
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7f8b2a67e03a64deae9d4bc9c7e3e714d134443c
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="cee94-103">Breyta kanban-reglum fyrir vinnsluverk</span><span class="sxs-lookup"><span data-stu-id="cee94-103">Change kanban rules for a process job</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cee94-104">Þetta ferli áherslu á að breyta kanban-reglu fyrir ákveðið kanban.</span><span class="sxs-lookup"><span data-stu-id="cee94-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="cee94-105">Þetta er gagnlegt til að hlaða tilföng eða við bilun.</span><span class="sxs-lookup"><span data-stu-id="cee94-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="cee94-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="cee94-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="cee94-107">Þetta ferli er ætluð fyrir skipuleggjandann, sem vinnur hjá lean framleiðslufyrirtæki, og ber ábyrgð á virðisstraumnum.</span><span class="sxs-lookup"><span data-stu-id="cee94-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="cee94-108">Afrita kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="cee94-108">Copy kanban rule</span></span>
1. <span data-ttu-id="cee94-109">Fara á kanban-reglur.</span><span class="sxs-lookup"><span data-stu-id="cee94-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="cee94-110">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="cee94-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="cee94-111">Velja tilviksreglur kanbans 000022 L0001.</span><span class="sxs-lookup"><span data-stu-id="cee94-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="cee94-112">Smellt er á Afrita kanban-reglu.</span><span class="sxs-lookup"><span data-stu-id="cee94-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="cee94-113">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cee94-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="cee94-114">Breyta kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="cee94-114">Change kanban rule</span></span>
1. <span data-ttu-id="cee94-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="cee94-115">Close the page.</span></span>
2. <span data-ttu-id="cee94-116">Fara í vinnsluröðun kanban</span><span class="sxs-lookup"><span data-stu-id="cee94-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="cee94-117">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="cee94-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="cee94-118">Velja línuna með Kanban 000177.</span><span class="sxs-lookup"><span data-stu-id="cee94-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="cee94-119">Smellt er á nota aðra kanban-regla.</span><span class="sxs-lookup"><span data-stu-id="cee94-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="cee94-120">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="cee94-120">Click Next.</span></span>
6. <span data-ttu-id="cee94-121">Sláðu inn eða veldu gildi í reitnum kanban-regla.</span><span class="sxs-lookup"><span data-stu-id="cee94-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="cee94-122">Velja kanban-reglu sem áður var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="cee94-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="cee94-123">Þetta er kanban-regla með hæsta númer.</span><span class="sxs-lookup"><span data-stu-id="cee94-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="cee94-124">Smellt er á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="cee94-124">Click Finish.</span></span>
    * <span data-ttu-id="cee94-125">Nú er kanban-vinnslu með annarri kanban-reglu.</span><span class="sxs-lookup"><span data-stu-id="cee94-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="cee94-126">Þetta getur verið jafna út hleðslu vinnuflokkana .</span><span class="sxs-lookup"><span data-stu-id="cee94-126">This can be useful to level load work cells.</span></span>  


