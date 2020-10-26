---
title: Stofna úthýstan vinnuflokk fyrir lean-framleiðslu
description: Til að hanna undirverktakavinnu fyrir lean-framleiðslu, verður að stofna vinnuflokk sem tengist lánardrottninum sem útvegar vinnuna.
author: cvocph
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2bc1e8551bbebd11cad18d47f9e74a2dedcb908d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983326"
---
# <a name="create-a-subcontracted-work-cell-for-lean-manufacturing"></a><span data-ttu-id="211e8-103">Stofna úthýstan vinnuflokk fyrir lean-framleiðslu</span><span class="sxs-lookup"><span data-stu-id="211e8-103">Create a subcontracted work cell for lean manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="211e8-104">Til að hanna undirverktakavinnu fyrir lean-framleiðslu, verður að stofna vinnuflokk sem tengist lánardrottninum sem útvegar vinnuna.</span><span class="sxs-lookup"><span data-stu-id="211e8-104">To model subcontracted work for lean manufacturing, you must create a work cell that is associated with the vendor that provides the work.</span></span> <span data-ttu-id="211e8-105">Vinnuflokkur í undirverktöku tengist lánardrottninum í gegnum vensl við tilföng af gerð lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="211e8-105">A subcontracted work cell is linked to the vendor through the association of a resource of the Vendor type.</span></span> <span data-ttu-id="211e8-106">Ef þú spilar þessa upptöku í USMF sýnifyrirtækinu, geturðu valið kenni lánardrottnalykils 1002 og svæði 1.</span><span class="sxs-lookup"><span data-stu-id="211e8-106">If you play this recording in the USMF demo company, you can select vendor account ID 1002 and site 1.</span></span>


## <a name="create-a-vendor-resource"></a><span data-ttu-id="211e8-107">Stofna tilfang lánardrottins</span><span class="sxs-lookup"><span data-stu-id="211e8-107">Create a vendor resource</span></span>
1. <span data-ttu-id="211e8-108">Fara á tilföng</span><span class="sxs-lookup"><span data-stu-id="211e8-108">Go to Resources.</span></span>
2. <span data-ttu-id="211e8-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="211e8-109">Click New.</span></span>
3. <span data-ttu-id="211e8-110">Í reitinn Tilfang skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="211e8-110">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="211e8-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="211e8-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="211e8-112">Í reitnum Tegund skal velja „lánardrottinn“.</span><span class="sxs-lookup"><span data-stu-id="211e8-112">In the Type field, select 'Vendor'.</span></span>
6. <span data-ttu-id="211e8-113">Í reitnum lánardrottinn skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="211e8-113">In the Vendor field, click the drop-down button to open the lookup.</span></span>

## <a name="create-the-resource-group"></a><span data-ttu-id="211e8-114">Stofna tilfangaflokk</span><span class="sxs-lookup"><span data-stu-id="211e8-114">Create the resource group</span></span>
1. <span data-ttu-id="211e8-115">Fara á tilfangaflokkur</span><span class="sxs-lookup"><span data-stu-id="211e8-115">Go to Resource groups.</span></span>
2. <span data-ttu-id="211e8-116">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="211e8-116">Click New.</span></span>
3. <span data-ttu-id="211e8-117">Færa inn gildi í svæðið tilfangaflokkur.</span><span class="sxs-lookup"><span data-stu-id="211e8-117">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="211e8-118">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="211e8-118">In the Description field, type a value.</span></span>
5. <span data-ttu-id="211e8-119">Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="211e8-119">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="211e8-120">Veldu svæðið sem vinnuflokkinum ætti að vera úthlutað til.</span><span class="sxs-lookup"><span data-stu-id="211e8-120">Select the site that the work cell should be allocated to.</span></span> <span data-ttu-id="211e8-121">Svæði getur, fræðilega séð, táknað stakt svæði sem er starfrækt af lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="211e8-121">In theory, a site can represent a single site that is operated by a vendor.</span></span> <span data-ttu-id="211e8-122">Í flestum tilfellum eru tilföng undirverktaka hins vegar úthlutað til svæðisins sem pantar vinnu í undirverktöku.</span><span class="sxs-lookup"><span data-stu-id="211e8-122">However, in most cases, subcontracted resources are just allocated to the site that orders the subcontracted work.</span></span> <span data-ttu-id="211e8-123">Athugið að inntaks og úttaks vöruhúsin fyrir undirverktaka vinnuflokka verða að vera á sama svæðinu.</span><span class="sxs-lookup"><span data-stu-id="211e8-123">Note that the input and output warehouses of subcontracted work cells must be on the same site.</span></span>  
6. <span data-ttu-id="211e8-124">Í reitinn Svæði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="211e8-124">In the Site field, type a value.</span></span>
7. <span data-ttu-id="211e8-125">@SysTaskRecorder:_RequestClose</span><span class="sxs-lookup"><span data-stu-id="211e8-125">@SysTaskRecorder:_RequestClose</span></span>
8. <span data-ttu-id="211e8-126">Velja eða hreinsa gátreitinn vinnuflokkur.</span><span class="sxs-lookup"><span data-stu-id="211e8-126">Select or clear the Work cell check box.</span></span>
9. <span data-ttu-id="211e8-127">Í reitnum inntaksvöruhús skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="211e8-127">In the Input warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="211e8-128">Veljið vöruhúsið og staðsetninguna sem eru notuð til að skipuleggja efni fyrir vinnuflokkana, sem stjórnað er af lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="211e8-128">Select the warehouse and location that are used to stage the material for the vendor-managed work cell.</span></span> <span data-ttu-id="211e8-129">Í mörgum tilfellum er vöruhúsið og staðsetningin gerð með því að nota mismunandi vöruhús fyrir hvern lánardrottinn og eina staðsetningu fyrir hvern vinnuflokk.</span><span class="sxs-lookup"><span data-stu-id="211e8-129">In many cases, the warehouse and location are modeled by using a separate warehouse per vendor and one location per work cell.</span></span>  
10. <span data-ttu-id="211e8-130">Í reitnum inntaksstaðsetning skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="211e8-130">In the Input location field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="211e8-131">Í reitnum úttaksvöruhús skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="211e8-131">In the Output warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="211e8-132">Skilgreinið vöruhúsið og staðsetningu þar sem efnið er bókað þegar verkþættir undirverktaka í vinnuflokki eru bókaðir.</span><span class="sxs-lookup"><span data-stu-id="211e8-132">Define the warehouse and location where the material is posted when the subcontracted activities of the work cell are posted.</span></span> <span data-ttu-id="211e8-133">Vöruhús og staðsetning geta verið á svæði lánardrottins ef lánardrottinn skráir kanban-vinnsluna.</span><span class="sxs-lookup"><span data-stu-id="211e8-133">The warehouse and location can be at the vendor site if the vendor reports the kanban jobs.</span></span> <span data-ttu-id="211e8-134">Að öðrum kosti geta vöruhúsið og staðsetningin verið staðsetningin sem tekur við og er tengd við næsta skref framleiðsluflæðisins.</span><span class="sxs-lookup"><span data-stu-id="211e8-134">Alternatively, the warehouse and location can be the receiving location that is associated with the next step of the production flow.</span></span>  
12. <span data-ttu-id="211e8-135">Í reitnum úttaks staðsetning skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="211e8-135">In the Output location field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="211e8-136">Útvíkka eða draga saman hlutann dagatal.</span><span class="sxs-lookup"><span data-stu-id="211e8-136">Expand or collapse the Calendars section.</span></span>
14. <span data-ttu-id="211e8-137">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="211e8-137">Click Add.</span></span>
15. <span data-ttu-id="211e8-138">Í reitnum dagatal skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="211e8-138">In the Calendar field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="211e8-139">Tengja vinnutímadagatal vinnuflokksins við tilfangaflokkinn.</span><span class="sxs-lookup"><span data-stu-id="211e8-139">Associate the working time calendar of the work cell with the resource group.</span></span> <span data-ttu-id="211e8-140">Fyrir mikilvæg tilföng, mælum við með að þú skilgreinir sérstök dagatöl sem sýna nákvæma tölu vinnutíma og skyldra afkasta vinnuflokksins eða svæði lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="211e8-140">For critical resources, we recommend that you define specific calendars that represent the exact working times and related capacities of the work cell or vendor site.</span></span>  
16. <span data-ttu-id="211e8-141">Stækka eða fella saman hlutann Tilföng</span><span class="sxs-lookup"><span data-stu-id="211e8-141">Expand or collapse the Resources section.</span></span>
17. <span data-ttu-id="211e8-142">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="211e8-142">Click Add.</span></span>
    * <span data-ttu-id="211e8-143">Tilfangaflokkur í undirverktöku verður að hafa tengd tilföng af gerð lánardrottins sem tengir tilfangaflokkinn við lánardrottnalykil.</span><span class="sxs-lookup"><span data-stu-id="211e8-143">A subcontracted resource group must have an associated resource of the Vendor type that links the resource group to the vendor account.</span></span>  
18. <span data-ttu-id="211e8-144">Í reitnum Tilföng skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="211e8-144">In the Resource field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="211e8-145">Smella á eða fara inn á tilföng lánardrottins sem voru stofnuð í síðasta undirverkefni.</span><span class="sxs-lookup"><span data-stu-id="211e8-145">Select or enter the vendor resource that you created in the previous sub-task.</span></span>  
19. <span data-ttu-id="211e8-146">Útvíkka eða draga saman hluta afkastageta vinnuflokks.</span><span class="sxs-lookup"><span data-stu-id="211e8-146">Expand or collapse the Work cell capacity section.</span></span>
20. <span data-ttu-id="211e8-147">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="211e8-147">Click Add.</span></span>
    * <span data-ttu-id="211e8-148">Vinnuflokkur verður að hafa skilgreinda afkastagetu.</span><span class="sxs-lookup"><span data-stu-id="211e8-148">A work cell must have a defined capacity.</span></span> <span data-ttu-id="211e8-149">Í þessu dæmi, sköpum við gegnstreymi afkasta upp á 100 stykki fyrir venjulegan vinnudag.</span><span class="sxs-lookup"><span data-stu-id="211e8-149">In this example, we create a throughput capacity of 100 pieces per standard workday.</span></span>  
21. <span data-ttu-id="211e8-150">Í reitnum líkan framleiðsluflæðis skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="211e8-150">In the Production flow model field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="211e8-151">Í svæðinu tímabil Afkastageta skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="211e8-151">In the Capacity period field, select an option.</span></span>
23. <span data-ttu-id="211e8-152">Færið inn tölu í svæðið Meðaltal gegnumstreymi magn.</span><span class="sxs-lookup"><span data-stu-id="211e8-152">In the Average throughput quantity field, enter a number.</span></span>
24. <span data-ttu-id="211e8-153">Í reitnum Eining skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="211e8-153">In the Unit field, click the drop-down button to open the lookup.</span></span>
25. <span data-ttu-id="211e8-154">Leysa breytir Einingu.</span><span class="sxs-lookup"><span data-stu-id="211e8-154">ResolveChanges the Unit.</span></span>

