---
title: Breyta kanban-reglum fyrir vinnsluverk
description: Þetta ferli leggur áherslu á að breyta kanban-reglu fyrir ákveðið kanban.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 485afff3747a87a6e36f0249b146a39361d81b23
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147136"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="67e86-103">Breyta kanban-reglum fyrir vinnsluverk</span><span class="sxs-lookup"><span data-stu-id="67e86-103">Change kanban rules for a process job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="67e86-104">Þetta ferli leggur áherslu á að breyta kanban-reglu fyrir ákveðið kanban.</span><span class="sxs-lookup"><span data-stu-id="67e86-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="67e86-105">Þetta er gagnlegt til að hlaða tilföng eða við bilun.</span><span class="sxs-lookup"><span data-stu-id="67e86-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="67e86-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="67e86-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="67e86-107">Þetta ferli er ætluð fyrir skipuleggjandann, sem vinnur hjá lean framleiðslufyrirtæki, og ber ábyrgð á virðisstraumnum.</span><span class="sxs-lookup"><span data-stu-id="67e86-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="67e86-108">Afrita kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="67e86-108">Copy kanban rule</span></span>
1. <span data-ttu-id="67e86-109">Fara á kanban-reglur.</span><span class="sxs-lookup"><span data-stu-id="67e86-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="67e86-110">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="67e86-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="67e86-111">Velja tilviksreglur kanbans 000022 L0001.</span><span class="sxs-lookup"><span data-stu-id="67e86-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="67e86-112">Smellt er á Afrita kanban-reglu.</span><span class="sxs-lookup"><span data-stu-id="67e86-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="67e86-113">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="67e86-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="67e86-114">Breyta kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="67e86-114">Change kanban rule</span></span>
1. <span data-ttu-id="67e86-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="67e86-115">Close the page.</span></span>
2. <span data-ttu-id="67e86-116">Fara í vinnsluröðun kanban</span><span class="sxs-lookup"><span data-stu-id="67e86-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="67e86-117">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="67e86-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="67e86-118">Velja línuna með Kanban 000177.</span><span class="sxs-lookup"><span data-stu-id="67e86-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="67e86-119">Smellt er á nota aðra kanban-regla.</span><span class="sxs-lookup"><span data-stu-id="67e86-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="67e86-120">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="67e86-120">Click Next.</span></span>
6. <span data-ttu-id="67e86-121">Sláðu inn eða veldu gildi í reitnum kanban-regla.</span><span class="sxs-lookup"><span data-stu-id="67e86-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="67e86-122">Velja kanban-reglu sem áður var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="67e86-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="67e86-123">Þetta er kanban-regla með hæsta númer.</span><span class="sxs-lookup"><span data-stu-id="67e86-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="67e86-124">Smellt er á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="67e86-124">Click Finish.</span></span>
    * <span data-ttu-id="67e86-125">Nú er kanban-vinnslu með annarri kanban-reglu.</span><span class="sxs-lookup"><span data-stu-id="67e86-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="67e86-126">Þetta getur verið jafna út hleðslu vinnuflokkana .</span><span class="sxs-lookup"><span data-stu-id="67e86-126">This can be useful to level load work cells.</span></span>  

