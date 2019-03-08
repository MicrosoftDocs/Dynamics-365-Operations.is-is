---
title: Stofna úthýstan vinnuflokk fyrir lean-framleiðslu
description: Til að hanna undirverktakavinnu fyrir lean-framleiðslu, verður að stofna vinnuflokk sem tengist lánardrottninum sem útvegar vinnuna.
author: cvocph
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58b725af456f1a5c7f158f01ffe48a2d8cdf056b
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "319156"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="2923b-103">Stofna úthýstan vinnuflokk fyrir lean-framleiðslu</span><span class="sxs-lookup"><span data-stu-id="2923b-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2923b-104">Til að hanna undirverktakavinnu fyrir lean-framleiðslu, verður að stofna vinnuflokk sem tengist lánardrottninum sem útvegar vinnuna.</span><span class="sxs-lookup"><span data-stu-id="2923b-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="2923b-105">Vinnuflokkur í undirverktöku tengist lánardrottninum í gegnum vensl við tilföng af gerð lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="2923b-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="2923b-106">Ef þú spilar þessa upptöku í USMF sýnifyrirtækinu, geturðu valið kenni lánardrottnalykils 1002 og svæði 1.</span><span class="sxs-lookup"><span data-stu-id="2923b-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="2923b-107">Stofna tilfang lánardrottins</span><span class="sxs-lookup"><span data-stu-id="2923b-107">Create a vendor resource</span></span>
1. <span data-ttu-id="2923b-108">Fara á tilföng</span><span class="sxs-lookup"><span data-stu-id="2923b-108">Go to Resources.</span></span>
2. <span data-ttu-id="2923b-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="2923b-109">Click New.</span></span>
3. <span data-ttu-id="2923b-110">Í reitinn Tilfang skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="2923b-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="2923b-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="2923b-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2923b-112">Í reitnum Tegund skal velja „lánardrottinn“.</span><span class="sxs-lookup"><span data-stu-id="2923b-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="2923b-113">Í reitnum lánardrottinn skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="2923b-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="2923b-114">Stofna tilfangaflokk</span><span class="sxs-lookup"><span data-stu-id="2923b-114">Create the resource group</span></span>
1. <span data-ttu-id="2923b-115">Fara á tilfangaflokkur</span><span class="sxs-lookup"><span data-stu-id="2923b-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="2923b-116">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="2923b-116">Click New.</span></span>
3. <span data-ttu-id="2923b-117">Færa inn gildi í svæðið tilfangaflokkur.</span><span class="sxs-lookup"><span data-stu-id="2923b-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="2923b-118">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="2923b-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="2923b-119">Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="2923b-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2923b-120">Veldu svæðið sem vinnuflokkinum ætti að vera úthlutað til.</span><span class="sxs-lookup"><span data-stu-id="2923b-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="2923b-121">Svæði getur, fræðilega séð, táknað stakt svæði sem er starfrækt af lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="2923b-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="2923b-122">Í flestum tilfellum eru tilföng undirverktaka hins vegar úthlutað til svæðisins sem pantar vinnu í undirverktöku.</span><span class="sxs-lookup"><span data-stu-id="2923b-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="2923b-123">Athugið að inntaks og úttaks vöruhúsin fyrir undirverktaka vinnuflokka verða að vera á sama svæðinu.</span><span class="sxs-lookup"><span data-stu-id="2923b-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="2923b-124">Í reitinn Svæði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="2923b-124">In the Site field, type a value.</span></span>
7. <span data-ttu-id="2923b-125">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="2923b-125">@SysTaskRecorder:_RequestClose</span></span>
8. <span data-ttu-id="2923b-126">Velja eða hreinsa gátreitinn vinnuflokkur.</span><span class="sxs-lookup"><span data-stu-id="2923b-126">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="2923b-127">Í reitnum inntaksvöruhús skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="2923b-127">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2923b-128">Veljið vöruhúsið og staðsetninguna sem eru notuð til að skipuleggja efni fyrir vinnuflokkana, sem stjórnað er af lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="2923b-128">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="2923b-129">Í mörgum tilfellum er vöruhúsið og staðsetningin gerð með því að nota mismunandi vöruhús fyrir hvern lánardrottinn og eina staðsetningu fyrir hvern vinnuflokk.</span><span class="sxs-lookup"><span data-stu-id="2923b-129">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="2923b-130">Í reitnum inntaksstaðsetning skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="2923b-130">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="2923b-131">Í reitnum úttaksvöruhús skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="2923b-131">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2923b-132">Skilgreinið vöruhúsið og staðsetningu þar sem efnið er bókað þegar verkþættir undirverktaka í vinnuflokki eru bókaðir.</span><span class="sxs-lookup"><span data-stu-id="2923b-132">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="2923b-133">Vöruhús og staðsetning geta verið á svæði lánardrottins ef lánardrottinn skráir kanban-vinnsluna.</span><span class="sxs-lookup"><span data-stu-id="2923b-133">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="2923b-134">Að öðrum kosti geta vöruhúsið og staðsetningin verið staðsetningin sem tekur við og er tengd við næsta skref framleiðsluflæðisins.</span><span class="sxs-lookup"><span data-stu-id="2923b-134">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="2923b-135">Í reitnum úttaks staðsetning skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="2923b-135">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="2923b-136">Útvíkka eða draga saman hlutann dagatal.</span><span class="sxs-lookup"><span data-stu-id="2923b-136">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="2923b-137">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="2923b-137">Click Add.</span></span>
15. <span data-ttu-id="2923b-138">Í reitnum dagatal skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="2923b-138">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2923b-139">Tengja vinnutímadagatal vinnuflokksins við tilfangaflokkinn.</span><span class="sxs-lookup"><span data-stu-id="2923b-139">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="2923b-140">Fyrir mikilvæg tilföng, mælum við með að þú skilgreinir sérstök dagatöl sem sýna nákvæma tölu vinnutíma og skyldra afkasta vinnuflokksins eða svæði lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="2923b-140">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="2923b-141">Stækka eða fella saman hlutann Tilföng</span><span class="sxs-lookup"><span data-stu-id="2923b-141">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="2923b-142">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="2923b-142">Click Add.</span></span>
    * <span data-ttu-id="2923b-143">Tilfangaflokkur í undirverktöku verður að hafa tengd tilföng af gerð lánardrottins sem tengir tilfangaflokkinn við lánardrottnalykil.</span><span class="sxs-lookup"><span data-stu-id="2923b-143">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="2923b-144">Í reitnum Tilföng skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="2923b-144">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="2923b-145">Smella á eða fara inn á tilföng lánardrottins sem voru stofnuð í síðasta undirverkefni.</span><span class="sxs-lookup"><span data-stu-id="2923b-145">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="2923b-146">Útvíkka eða draga saman hluta afkastageta vinnuflokks.</span><span class="sxs-lookup"><span data-stu-id="2923b-146">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="2923b-147">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="2923b-147">Click Add.</span></span>
    * <span data-ttu-id="2923b-148">Vinnuflokkur verður að hafa skilgreinda afkastagetu.</span><span class="sxs-lookup"><span data-stu-id="2923b-148">A work cell must have a defined capacity.</span></span> <span data-ttu-id="2923b-149">Í þessu dæmi, sköpum við gegnstreymi afkasta upp á 100 stykki fyrir venjulegan vinnudag.</span><span class="sxs-lookup"><span data-stu-id="2923b-149">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="2923b-150">Í reitnum líkan framleiðsluflæðis skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="2923b-150">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="2923b-151">Í svæðinu tímabil Afkastageta skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="2923b-151">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="2923b-152">Færið inn tölu í svæðið Meðaltal gegnumstreymi magn.</span><span class="sxs-lookup"><span data-stu-id="2923b-152">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="2923b-153">Í reitnum Eining skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="2923b-153">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="2923b-154">Leysa breytir Einingu.</span><span class="sxs-lookup"><span data-stu-id="2923b-154">ResolveChanges the Unit.</span></span>

