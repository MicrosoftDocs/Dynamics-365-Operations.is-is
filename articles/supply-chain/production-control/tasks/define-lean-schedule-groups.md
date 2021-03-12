---
title: Skilgreina flokka í markvissri áætlanagerð
description: flokkur í markvissri áætlanagerð eru skilgreind til að flokka og greina afurðir í áætlun kanban.
author: cvocph
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: acdaa3c9ee927b5c333b41927b2a6d245c02b4d8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977889"
---
# <a name="define-lean-schedule-groups"></a><span data-ttu-id="d2cbf-103">Skilgreina flokka í markvissri áætlanagerð</span><span class="sxs-lookup"><span data-stu-id="d2cbf-103">Define lean schedule groups</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d2cbf-104">flokkur í markvissri áætlanagerð eru skilgreind til að flokka og greina afurðir í áætlun kanban.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-104">Lean schedule groups are defined to group and distinguish products in kanban scheduling.</span></span> <span data-ttu-id="d2cbf-105">Hægt er að gera flokkunina sem almennan tengingu fyrir hvert fyrirtæki eða við vinnuflokkur.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-105">The grouping can be done as generic association per company or specific to a work cell.</span></span> <span data-ttu-id="d2cbf-106">Hver flokkur hefur litakóði sem úthlutað er fyrir sjónræn lýsing á lístasíðum kanban-röðunar.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-106">Each group has a color code assigned for visual indication in the kanban scheduling listpage.</span></span> <span data-ttu-id="d2cbf-107">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="define-lean-scheduling-group"></a><span data-ttu-id="d2cbf-108">Skilgreina flokkur í markvissri áætlanagerð</span><span class="sxs-lookup"><span data-stu-id="d2cbf-108">Define lean scheduling group</span></span>
1. <span data-ttu-id="d2cbf-109">Fara í Afurðaupplýsingastjórnun > Lean-framleiðsla > Lean-áætlunarflokkar.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-109">Go to Product information management > Lean manufacturing > Lean schedule groups.</span></span>
2. <span data-ttu-id="d2cbf-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-110">Click New.</span></span>
3. <span data-ttu-id="d2cbf-111">Færa inn gildi í svæðinu áætlunarflokkur.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-111">In the Schedule group field, type a value.</span></span>
    * <span data-ttu-id="d2cbf-112">Áætlunarflokkur getur verið skilgreind sem altæka flokka eða við vinnuflokks.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-112">A schedule group can be defined as global group or specific to a work cell.</span></span> <span data-ttu-id="d2cbf-113">Í þessu dæmi skilgreina altæka flokka og vinnuflokkurinn er haldið eftir autt.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-113">In this simple example, we define a global group, and the work cell is kept empty.</span></span> <span data-ttu-id="d2cbf-114">Stillingar fyrir þennan flokk eiga við allar vinnuflokkana sem ekki hafa flokka tiltekna áætlunarflokk.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-114">The settings of this group apply to all work cells that do not have specific schedule groups.</span></span>  
4. <span data-ttu-id="d2cbf-115">Veljið lit úr valinu lit.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-115">Select a color from the color selection.</span></span>
    * <span data-ttu-id="d2cbf-116">Litir eru notaðir til að auðkenna störf á listasíðu áætlunar fyrir kanban eða spjald kanban ferlis.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-116">The colors are used to highlight the jobs on the kanban schedule list page or the kanban process board.</span></span>  
5. <span data-ttu-id="d2cbf-117">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="d2cbf-118">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-118">In the list, click the link in the selected row.</span></span>

## <a name="associate-product"></a><span data-ttu-id="d2cbf-119">Tengja afurð</span><span class="sxs-lookup"><span data-stu-id="d2cbf-119">Associate product</span></span>
1. <span data-ttu-id="d2cbf-120">Tengja tiltekna afurð</span><span class="sxs-lookup"><span data-stu-id="d2cbf-120">Associate a specific product</span></span>
    * <span data-ttu-id="d2cbf-121">Til eru tvær leiðir til að tengja afurðir við flokkur í markvissri áætlanagerð, annaðhvort sem tiltekinni vöru (venslagerð Vöru = Vöru) eða sem hluta af úthlutunarlykil vöru (venslagerð vöru= flokk).</span><span class="sxs-lookup"><span data-stu-id="d2cbf-121">There are two ways to associate products to lean schedule groups, either as a specific product (Item relation type = Item) or as part of an item allocation key (item relation type = group).</span></span>    
2. <span data-ttu-id="d2cbf-122">velja Vöru í Venslagerðarsvæði Vöru</span><span class="sxs-lookup"><span data-stu-id="d2cbf-122">In the Item relation type field, select Item</span></span>
3. <span data-ttu-id="d2cbf-123">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-123">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="d2cbf-124">Í reitinn afkastageta skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-124">In the Throughput ratio field, enter a number.</span></span>
    * <span data-ttu-id="d2cbf-125">Sjálfgefin afkastahlutfall er 1, sem þýðir að tengdar afurðir nota nákvæmlega afköst tilgreind í vinnsluaðgerðum framleiðsluflæðis.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-125">The default Throughput ratio is 1, which means that the related products consume exactly the capacity specified in the process activites of the production flows.</span></span> <span data-ttu-id="d2cbf-126">Afkastahlutfall > 1 tilgreinir hærri tilfanganotkun, afkastahlutfall < 1 tilgreinir lægri notkun tilfanga.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-126">Throughput ratio > 1 defines a higher resource consumption, Throughput ratio < 1 defines a lower resource consumption.</span></span> <span data-ttu-id="d2cbf-127">Hlutfallið er notað í útreikningi kanban-vinnslunotkun og í útreikningi kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-127">The ratio is used in the cost calculation and in the calculation of the kanban job consumption.</span></span>  

## <a name="associate-item-allocation-key"></a><span data-ttu-id="d2cbf-128">Úthluta úthlutunarlykil vöru</span><span class="sxs-lookup"><span data-stu-id="d2cbf-128">Associate item allocation key</span></span>
1. <span data-ttu-id="d2cbf-129">Tengja úthlutunarlykil vöru</span><span class="sxs-lookup"><span data-stu-id="d2cbf-129">Associate an item allocation key</span></span>
    * <span data-ttu-id="d2cbf-130">Bæta tengingu við úthlutunarlykil vöru með því að nota hópagerð vöruvensla.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-130">Add an association to an item allocation key by using the Item relation type Group.</span></span>   <span data-ttu-id="d2cbf-131">Athugið að fyrir þetta ferli þarf að spár úthlutunarlykli vöru skilgreindum í gögnin þín.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-131">Note that for this process, you need a forecast item alllocation key defined in your data.</span></span>  
2. <span data-ttu-id="d2cbf-132">Velja flokk í Venslagerðarsvæði Vöru</span><span class="sxs-lookup"><span data-stu-id="d2cbf-132">In the Item relation type field, select Group</span></span>
3. <span data-ttu-id="d2cbf-133">Í reitnum úthlutunarlykill vöru skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-133">In the Item allocation key field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="d2cbf-134">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d2cbf-134">In the list, click the link in the selected row.</span></span>

