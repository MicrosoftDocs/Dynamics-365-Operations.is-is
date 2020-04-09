---
title: Stofna kanban-reglu með kanban-línutilviki
description: Þetta ferli stofnar kanban-reglu með því að nota stillinguna línutilvik kanbans til að virkja sækja úr ferlisverkþætti.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b8f56877d499efa6bd635b4d8b5f7dc78a7f78ae
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147044"
---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a><span data-ttu-id="50f37-103">Stofna kanban-reglu með kanban-línutilviki</span><span class="sxs-lookup"><span data-stu-id="50f37-103">Create a kanban rule using a kanban line event</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="50f37-104">Þetta ferli stofnar kanban-reglu með því að nota stillinguna línutilvik kanbans til að virkja sækja úr ferlisverkþætti.</span><span class="sxs-lookup"><span data-stu-id="50f37-104">This procedure creates a kanban rule by using the kanban line event setting to trigger pull from a process activity.</span></span> <span data-ttu-id="50f37-105">Kanban-reglu virkjast af kanban ferlisverkþætti, með magnið það sama eða hærri en 25 hvert.</span><span class="sxs-lookup"><span data-stu-id="50f37-105">The kanban rule is triggered by a kanban process activity, with a quantity equal to or greater than 25 each.</span></span> <span data-ttu-id="50f37-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="50f37-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="50f37-107">Þetta verkefni er ætlað fyrir Ferlishönnuð eða Virðisstraumsstjóra, þar sem þau undirbúa framleiðslu nýja eða breytta afurðar í lean-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="50f37-107">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-kanban-rule"></a><span data-ttu-id="50f37-108">Stofna kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="50f37-108">Create a kanban rule</span></span>
1. <span data-ttu-id="50f37-109">Farið í upplýsingar um afurðarstjórnun > Lean-framleiðsla > Kanban-reglur.</span><span class="sxs-lookup"><span data-stu-id="50f37-109">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="50f37-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="50f37-110">Click New.</span></span>
3. <span data-ttu-id="50f37-111">Velja 'Tilvik' í reitnum Áfyllingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="50f37-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="50f37-112">Þetta myndar kanban beint úr eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="50f37-112">This generates kanbans directly from demand.</span></span> <span data-ttu-id="50f37-113">Hann er notaður til að setja upp reglur sem skilgreina framleiða eftir pöntun-aðstæður.</span><span class="sxs-lookup"><span data-stu-id="50f37-113">It is used to set up rules that define a make-to-order scenario.</span></span>  
4. <span data-ttu-id="50f37-114">Færa inn eða velja gildi í reitnum Fyrsta áætlun verkþáttarins.</span><span class="sxs-lookup"><span data-stu-id="50f37-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="50f37-115">Sláið inn eða Veljið SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="50f37-115">Enter or select SpeakerAssemblyAndPolish.</span></span> <span data-ttu-id="50f37-116">Fyrsti verkþáttur kanban-reglu framleiðslu er ferlisverkþáttur í framleiðsluflæðinu.</span><span class="sxs-lookup"><span data-stu-id="50f37-116">The first activity of a manufacturing kanban rule is a process activity in the production flow.</span></span> <span data-ttu-id="50f37-117">Þegar þú velur aðgerð, eru gildisdagsetningar verkþáttar afrituð í gildisdagsetningar kanban-reglu.</span><span class="sxs-lookup"><span data-stu-id="50f37-117">When you select the activity, the validity dates of the activity are copied to the validity dates of the kanban rule.</span></span>  
5. <span data-ttu-id="50f37-118">Útvíkka hlutann Upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="50f37-118">Expand the Details section.</span></span>
6. <span data-ttu-id="50f37-119">Í reitinn afurð skal færa inn ‚L0001‘.</span><span class="sxs-lookup"><span data-stu-id="50f37-119">In the Product field, type 'L0001'.</span></span>
7. <span data-ttu-id="50f37-120">Útvíkka hlutann Tilvik.</span><span class="sxs-lookup"><span data-stu-id="50f37-120">Expand the Events section.</span></span>
8. <span data-ttu-id="50f37-121">Í reitnum línutilvik kanbans skal velja ‚Sjálfvirkt‘.</span><span class="sxs-lookup"><span data-stu-id="50f37-121">In the Kanban line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="50f37-122">Þetta myndar tilvikskanban eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="50f37-122">This generates event kanbans on demand.</span></span>  <span data-ttu-id="50f37-123">Þessi reitur er notuð til að stilla kanban-reglur sem fylla efni á sem krafist er fyrir úrvinnsluaðgerð.</span><span class="sxs-lookup"><span data-stu-id="50f37-123">The field is used to configure kanban rules that replenish material that is required for a downstream process activity.</span></span> <span data-ttu-id="50f37-124">Þegar Sjálfvirk er valið, eru tilvikskanbön stofnaðar með eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="50f37-124">When you select Automatic, the event kanbans are created with the demand.</span></span> <span data-ttu-id="50f37-125">Mælt er með þessari stillingu ef búist er við að keyra framleiðslu sama dag.</span><span class="sxs-lookup"><span data-stu-id="50f37-125">This setting is recommended if you expect to execute production on the same day.</span></span>  
9. <span data-ttu-id="50f37-126">Stilla lágmarksmagn tilviks á ‚25‘.</span><span class="sxs-lookup"><span data-stu-id="50f37-126">Set Minimum event quantity to '25'.</span></span>
    * <span data-ttu-id="50f37-127">Tilvikskanban eru myndaðar þegar eftirspurnarmagn er jafnt eða meira en þetta svæði.</span><span class="sxs-lookup"><span data-stu-id="50f37-127">Event kanbans are generated when the demand quantity is equal to or more than this field.</span></span> <span data-ttu-id="50f37-128">Þetta er hentugt ef á að framleiða pöntunarmagn sem er minna en þetta svæði á einni vél og meira en þetta svæði á annarri vél.</span><span class="sxs-lookup"><span data-stu-id="50f37-128">This is useful if you want to produce an order quantity less than this field on one machine and more than this field on another machine.</span></span>  
10. <span data-ttu-id="50f37-129">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="50f37-129">Click Save.</span></span>

## <a name="create-sales-order-and-trigger-kanban-chain"></a><span data-ttu-id="50f37-130">Stofna sölupöntun og virkja kanban keðju</span><span class="sxs-lookup"><span data-stu-id="50f37-130">Create sales order and trigger kanban chain</span></span>
1. <span data-ttu-id="50f37-131">Fara í Sölu og markaðssetningu > sölupöntun > Allar sölupantanir</span><span class="sxs-lookup"><span data-stu-id="50f37-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="50f37-132">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="50f37-132">Click New.</span></span>
3. <span data-ttu-id="50f37-133">Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="50f37-133">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="50f37-134">Veljið viðskiptavinalykill US-003 Forest Wholesales.</span><span class="sxs-lookup"><span data-stu-id="50f37-134">Select Customer account US-003, Forest Wholesales.</span></span>  
4. <span data-ttu-id="50f37-135">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="50f37-135">Click OK.</span></span>
5. <span data-ttu-id="50f37-136">Sláið inn „L0001“ á svæðinu „Vörunúmer“.</span><span class="sxs-lookup"><span data-stu-id="50f37-136">In the Item number field, type 'L0001'.</span></span>
    * <span data-ttu-id="50f37-137">L0001 er varan sem kanban-regla er stofnuð fyrir.</span><span class="sxs-lookup"><span data-stu-id="50f37-137">L0001 is the item for which you created the kanban rule.</span></span>  
6. <span data-ttu-id="50f37-138">Stillið magn á „27“.</span><span class="sxs-lookup"><span data-stu-id="50f37-138">Set Quantity to '27'.</span></span>
    * <span data-ttu-id="50f37-139">Þar sem 27 er hærri en lágmarksmagnið 25 á kanban-reglu, mun þetta virkja tilvikskanban.</span><span class="sxs-lookup"><span data-stu-id="50f37-139">Because 27 is higher than the minimum quantity of 25 on the kanban rule, this will trigger an event kanban.</span></span>  
7. <span data-ttu-id="50f37-140">Ritað er ‚1‘ í reitnum Svæði.</span><span class="sxs-lookup"><span data-stu-id="50f37-140">In the Site field, type '1'.</span></span>
8. <span data-ttu-id="50f37-141">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="50f37-141">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="50f37-142">Velja vöruhús 13.</span><span class="sxs-lookup"><span data-stu-id="50f37-142">Select warehouse 13.</span></span>  
9. <span data-ttu-id="50f37-143">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="50f37-143">Click Save.</span></span>

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a><span data-ttu-id="50f37-144">Skoða kanban sem var myndað af kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="50f37-144">View the kanban generated by the kanban rule</span></span>
1. <span data-ttu-id="50f37-145">Farið í upplýsingar um afurðarstjórnun > Lean-framleiðsla > Kanban-reglur.</span><span class="sxs-lookup"><span data-stu-id="50f37-145">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="50f37-146">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="50f37-146">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="50f37-147">Útvíkkar kanban-hlutann.</span><span class="sxs-lookup"><span data-stu-id="50f37-147">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="50f37-148">Athugið að kanban fyrir 27 var stofnað til að vinna verkþátt á grunni stofnaðrar kanban-reglu.</span><span class="sxs-lookup"><span data-stu-id="50f37-148">Notice that a kanban for 27 was created to process the  activity based on the created kanban rule.</span></span>  
    * <span data-ttu-id="50f37-149">Þetta er síðasta skrefið</span><span class="sxs-lookup"><span data-stu-id="50f37-149">This is the last step.</span></span>  

