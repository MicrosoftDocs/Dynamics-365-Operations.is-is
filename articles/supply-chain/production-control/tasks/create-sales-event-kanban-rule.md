---
title: Stofna kanban-regla sölutilviks
description: Þetta ferli leggur áherslu á uppsetningu sem þarf til að stofna kanban-reglu sem er ræst við stofnun sölupöntunar.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1759adea6db8120078e2f32bff79178545c2328a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430046"
---
# <a name="create-a-sales-event-kanban-rule"></a><span data-ttu-id="07a86-103">Stofna kanban-regla sölutilviks</span><span class="sxs-lookup"><span data-stu-id="07a86-103">Create a sales event kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="07a86-104">Þetta ferli leggur áherslu á uppsetningu sem þarf til að stofna kanban-reglu sem er ræst við stofnun sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="07a86-104">This procedure focuses on the setup needed to create a kanban rule that is triggered during sales order creation.</span></span> <span data-ttu-id="07a86-105">Tilviksreglur kanbans fylla á kröfur sem eiga upphaf sitt í sölupöntunarlínum.</span><span class="sxs-lookup"><span data-stu-id="07a86-105">The event kanban rule replenishes requirements that originate from sales order lines.</span></span> <span data-ttu-id="07a86-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="07a86-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="07a86-107">Það er ætlað fyrir ferlishönnuð eða virðisstraumsstjóra þegar þeir undirbúa framleiðslu nýrrar eða breyttrar afurðar.</span><span class="sxs-lookup"><span data-stu-id="07a86-107">It is intended for the process engineer or the value stream manager as they prepare production of a new or modified product.</span></span>




## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="07a86-108">Stofna nýja kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="07a86-108">Create a new kanban rule</span></span>
1. <span data-ttu-id="07a86-109">Fara á kanban-reglur.</span><span class="sxs-lookup"><span data-stu-id="07a86-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="07a86-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="07a86-110">Click New.</span></span>
3. <span data-ttu-id="07a86-111">Velja 'Tilvik' í reitnum Áfyllingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="07a86-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="07a86-112">Velja Tilvik þýðir kanban-reglan er ræst með tilviki, til dæmis stofnun sölupöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="07a86-112">Selecting Event means that the kanban rule is triggered by an event, for example, creation of a sales order line.</span></span>   <span data-ttu-id="07a86-113">Þessu er beitt á svæðum þar sem hvert kanban á að ná yfir tiltekna eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="07a86-113">This is applied to areas where each kanban should cover a specific demand.</span></span>  
4. <span data-ttu-id="07a86-114">Færa inn eða velja gildi í reitnum Fyrsta áætlun verkþáttarins.</span><span class="sxs-lookup"><span data-stu-id="07a86-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="07a86-115">Velja Lokasamsetningu.</span><span class="sxs-lookup"><span data-stu-id="07a86-115">Select Final assembly.</span></span>  
5. <span data-ttu-id="07a86-116">Útvíkka hlutann Upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="07a86-116">Expand the Details section.</span></span>
6. <span data-ttu-id="07a86-117">Sláðu inn eða veldu gildi í reitnum Afurð.</span><span class="sxs-lookup"><span data-stu-id="07a86-117">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="07a86-118">Veldu L0050.</span><span class="sxs-lookup"><span data-stu-id="07a86-118">Select L0050.</span></span>  

## <a name="define-an-event"></a><span data-ttu-id="07a86-119">Skilgreina tilvik</span><span class="sxs-lookup"><span data-stu-id="07a86-119">Define an event</span></span>
1. <span data-ttu-id="07a86-120">Útvíkka hlutann Tilvik.</span><span class="sxs-lookup"><span data-stu-id="07a86-120">Expand the Events section.</span></span>
2. <span data-ttu-id="07a86-121">Í reitnum Sölutilvik skal velja ‚Sjálfvirkt‘.</span><span class="sxs-lookup"><span data-stu-id="07a86-121">In the Sales event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="07a86-122">Með því að velja sölutilvikið Sjálfvirkt verður þessi kanban-regla ræst sjálfkrafa þegar sölulína samræmist staðsetningu afurðar og móttöku.</span><span class="sxs-lookup"><span data-stu-id="07a86-122">By selecting the sales event Automatic, this kanban rule will be triggered automatically when a sales line matches the product and receipt location.</span></span> <span data-ttu-id="07a86-123">Í þessu ferli er afurð L0050 í vöruhúsi 13.</span><span class="sxs-lookup"><span data-stu-id="07a86-123">In this procedure, it is product L0050 on warehouse 13.</span></span>  
3. <span data-ttu-id="07a86-124">Stilla lágmarksmagn tilviks á ‚50‘.</span><span class="sxs-lookup"><span data-stu-id="07a86-124">Set Minimum event quantity to '50'.</span></span>
    * <span data-ttu-id="07a86-125">Með lágmarksmagni tilviks upp á 50 verður kanban-reglan aðeins ræst af tilvikum með magninu 50 eða meira.</span><span class="sxs-lookup"><span data-stu-id="07a86-125">With a minimum event quantity of 50, the kanban rule will only be triggered by events with a quantity of 50 or more.</span></span>  
4. <span data-ttu-id="07a86-126">Útvíkka hlutann Framleiðsluflæði.</span><span class="sxs-lookup"><span data-stu-id="07a86-126">Expand the Production flow section.</span></span>
    * <span data-ttu-id="07a86-127">Athugaðu að staðsetning Innhreyfinga er vöruhús 13.</span><span class="sxs-lookup"><span data-stu-id="07a86-127">Notice that the Receipt location is warehouse 13.</span></span> <span data-ttu-id="07a86-128">Þetta þýðir að þessi kanban-regla verður ræst fyrir þessa staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="07a86-128">This means that this kanban rule will be triggered for this location.</span></span>  
    * <span data-ttu-id="07a86-129">Í þessu dæmi mun sölulína fyrir afurð L0050, með magni 50 eða fleiri á vöruhúsi 13, virkja þessa kanban-reglu.</span><span class="sxs-lookup"><span data-stu-id="07a86-129">In this example, a sales line for product L0050, with a quantity of 50 or more, on warehouse 13, will trigger this kanban rule.</span></span>  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a><span data-ttu-id="07a86-130">Stofna sölulínur til að kveikja tilviksreglur kanbans</span><span class="sxs-lookup"><span data-stu-id="07a86-130">Create sales line to trigger event kanban rule</span></span>
1. <span data-ttu-id="07a86-131">Fara í Allar sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="07a86-131">Go to All sales orders.</span></span>
    * <span data-ttu-id="07a86-132">Viðvörun birtist þegar kanban-reglan er vistuð, sem þýðir að það verður að stofna kanban í rauntíma við stofnun sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="07a86-132">A warning is shown when the kanban rule is saved, which means that kanbans will be created in real-time during sales order creation.</span></span>  
2. <span data-ttu-id="07a86-133">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="07a86-133">Click New.</span></span>
3. <span data-ttu-id="07a86-134">Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="07a86-134">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="07a86-135">Veljið til dæmis US-003.</span><span class="sxs-lookup"><span data-stu-id="07a86-135">For example, select US-003.</span></span>  
4. <span data-ttu-id="07a86-136">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="07a86-136">Click OK.</span></span>
5. <span data-ttu-id="07a86-137">Sláið inn „L0050“ á svæðinu „Vörunúmer“.</span><span class="sxs-lookup"><span data-stu-id="07a86-137">In the Item number field, type 'L0050'.</span></span>
6. <span data-ttu-id="07a86-138">Ritað er ‚1‘ í reitnum Svæði.</span><span class="sxs-lookup"><span data-stu-id="07a86-138">In the Site field, type '1'.</span></span>
    * <span data-ttu-id="07a86-139">Veljið Svæði 1 þar sem Vöruhús 13 er á Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="07a86-139">Select Site 1 because Warehouse 13 is on Site 1.</span></span>  
7. <span data-ttu-id="07a86-140">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="07a86-140">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="07a86-141">Stilltu Vöruhús á 13.</span><span class="sxs-lookup"><span data-stu-id="07a86-141">Set Warehouse to 13.</span></span>  
8. <span data-ttu-id="07a86-142">Stillið magn á „75“.</span><span class="sxs-lookup"><span data-stu-id="07a86-142">Set Quantity to '75'.</span></span>
    * <span data-ttu-id="07a86-143">Færið inn magn 50 eða hærri til að virkja stofnaða kanban-reglu.</span><span class="sxs-lookup"><span data-stu-id="07a86-143">Enter a quantity of 50 or greater, to trigger the created kanban rule.</span></span>  

## <a name="verify-that-kanban-is-created"></a><span data-ttu-id="07a86-144">Staðfestið að kanban sé stofnað</span><span class="sxs-lookup"><span data-stu-id="07a86-144">Verify that kanban is created</span></span>
1. <span data-ttu-id="07a86-145">Smellt er á Afurð og framboð.</span><span class="sxs-lookup"><span data-stu-id="07a86-145">Click Product and supply.</span></span>
2. <span data-ttu-id="07a86-146">Smellt er á Skoða þarfarakningartré.</span><span class="sxs-lookup"><span data-stu-id="07a86-146">Click View pegging tree.</span></span>
    * <span data-ttu-id="07a86-147">Athugið að kanban með sama magni og sölulínan var stofnað.</span><span class="sxs-lookup"><span data-stu-id="07a86-147">Notice that a kanban with the same quantity as the sales line is created.</span></span> <span data-ttu-id="07a86-148">Einnig er hægt að skoða efni sem þarf til að framleiða L0050.</span><span class="sxs-lookup"><span data-stu-id="07a86-148">You can also see the material issues needed to produce L0050.</span></span> <span data-ttu-id="07a86-149">Þetta er síðasta skrefið í þessu ferli.</span><span class="sxs-lookup"><span data-stu-id="07a86-149">This is the last step in this procedure.</span></span>  

