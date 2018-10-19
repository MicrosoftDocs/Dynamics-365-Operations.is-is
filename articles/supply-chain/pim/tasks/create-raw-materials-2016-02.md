--- 
title: "Stofna hráefni (febrúar 2016)"
description: "Þetta verk einblínir á að búa til íhluti fullunnin vara og hálfunnin vara."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 091b6edaf43e86e6e3665bf79871648473e284c7
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="e38f5-103">Stofna hráefni (febrúar 2016)</span><span class="sxs-lookup"><span data-stu-id="e38f5-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e38f5-104">Þetta verk einblínir á að búa til íhluti fullunnin vara og hálfunnin vara.</span><span class="sxs-lookup"><span data-stu-id="e38f5-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="e38f5-105">Þetta er þriðja verkið í línunni Útreikningur uppskrifta.</span><span class="sxs-lookup"><span data-stu-id="e38f5-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="e38f5-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="e38f5-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="e38f5-107">Stofna fyrsta hráefni</span><span class="sxs-lookup"><span data-stu-id="e38f5-107">Create the first material</span></span>
1. <span data-ttu-id="e38f5-108">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="e38f5-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="e38f5-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e38f5-109">Click New.</span></span>
3. <span data-ttu-id="e38f5-110">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="e38f5-111">Í þessu dæmi, slá inn ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="e38f5-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="e38f5-112">Í reitinn Vörulíkanaflokkur skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-113">Veldu STD.</span><span class="sxs-lookup"><span data-stu-id="e38f5-113">Select STD.</span></span> <span data-ttu-id="e38f5-114">STD stendur fyrir staðalkostnaður og er mest notaða líkan þegar unnið með kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="e38f5-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="e38f5-115">Í reitinn Vöruflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-116">Veljið t.d. Hljóðvinnsla.</span><span class="sxs-lookup"><span data-stu-id="e38f5-116">For example, select Audio.</span></span> <span data-ttu-id="e38f5-117">Þetta hefur engin áhrif á kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="e38f5-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="e38f5-118">Í reitinn Geymsluvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-119">Velja SiteWH.</span><span class="sxs-lookup"><span data-stu-id="e38f5-119">Select SiteWH.</span></span> <span data-ttu-id="e38f5-120">Aðeins Svæði og vöruhús verður notað í kynning.</span><span class="sxs-lookup"><span data-stu-id="e38f5-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="e38f5-121">Í reitinn Rakningarvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-122">Rakningarvíddir verða ekki notað í þessa dæmi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="e38f5-123">Velja engar.</span><span class="sxs-lookup"><span data-stu-id="e38f5-123">Select None.</span></span>  
8. <span data-ttu-id="e38f5-124">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e38f5-124">Click OK.</span></span>
9. <span data-ttu-id="e38f5-125">Á Aðgerðasvæðinu skal smella á Stjórna birgðum.</span><span class="sxs-lookup"><span data-stu-id="e38f5-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="e38f5-126">Smellt er á sjálfgefnar pöntunarstillingar.</span><span class="sxs-lookup"><span data-stu-id="e38f5-126">Click Default order settings.</span></span>
11. <span data-ttu-id="e38f5-127">Í svæði „Innkaupasvæði“ slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-128">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="e38f5-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="e38f5-129">Í svæði Birgðasvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-130">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="e38f5-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="e38f5-131">Í svæði Sölusvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-132">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="e38f5-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="e38f5-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e38f5-133">Close the page.</span></span>
15. <span data-ttu-id="e38f5-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e38f5-134">Close the page.</span></span>
16. <span data-ttu-id="e38f5-135">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e38f5-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e38f5-136">Smellt er á ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="e38f5-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="e38f5-137">Stækka hlutann Vinna með kostnað.</span><span class="sxs-lookup"><span data-stu-id="e38f5-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="e38f5-138">Í svæði Kostnaðarflokkur, slærðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="e38f5-139">Í þessu dæmi, slá inn M2.</span><span class="sxs-lookup"><span data-stu-id="e38f5-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="e38f5-140">Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.</span><span class="sxs-lookup"><span data-stu-id="e38f5-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="e38f5-141">Smellt er á Verð vöru.</span><span class="sxs-lookup"><span data-stu-id="e38f5-141">Click Item price.</span></span>
21. <span data-ttu-id="e38f5-142">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e38f5-142">Click New.</span></span>
22. <span data-ttu-id="e38f5-143">Í svæði Útgáfa, slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-144">Í þessu dæmi, velja 10, sem er staðalkostnaður í þessari kostnaðargerð.</span><span class="sxs-lookup"><span data-stu-id="e38f5-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="e38f5-145">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="e38f5-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-146">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="e38f5-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="e38f5-147">Í reitinn Verð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="e38f5-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="e38f5-148">Í þessu dæmi, slá inn 10.</span><span class="sxs-lookup"><span data-stu-id="e38f5-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="e38f5-149">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e38f5-149">Click Save.</span></span>
26. <span data-ttu-id="e38f5-150">Smellt er á Virk vöruverð.</span><span class="sxs-lookup"><span data-stu-id="e38f5-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="e38f5-151">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e38f5-151">Close the page.</span></span>
28. <span data-ttu-id="e38f5-152">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e38f5-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="e38f5-153">Stofna annað hráefni</span><span class="sxs-lookup"><span data-stu-id="e38f5-153">Create the second material</span></span>
1. <span data-ttu-id="e38f5-154">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e38f5-154">Click New.</span></span>
2. <span data-ttu-id="e38f5-155">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="e38f5-156">Í þessu dæmi, slá inn ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="e38f5-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="e38f5-157">Í reitinn Vörulíkanaflokkur skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-158">Veldu STD.</span><span class="sxs-lookup"><span data-stu-id="e38f5-158">Select STD.</span></span> <span data-ttu-id="e38f5-159">STD stendur fyrir staðalkostnaður og er mest notaða líkan þegar unnið með kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="e38f5-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="e38f5-160">Í reitinn Vöruflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-161">Veljið t.d. Hljóðvinnsla.</span><span class="sxs-lookup"><span data-stu-id="e38f5-161">For example, select Audio.</span></span> <span data-ttu-id="e38f5-162">Þetta hefur engin áhrif á kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="e38f5-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="e38f5-163">Í reitinn Geymsluvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-164">Velja SiteWH.</span><span class="sxs-lookup"><span data-stu-id="e38f5-164">Select SiteWH.</span></span> <span data-ttu-id="e38f5-165">Aðeins Svæði og vöruhús verður notað í þessu dæmi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="e38f5-166">Í reitinn Rakningarvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-167">Rakningarvíddir verða ekki notað í þessa dæmi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="e38f5-168">Velja engar.</span><span class="sxs-lookup"><span data-stu-id="e38f5-168">Select None.</span></span>  
7. <span data-ttu-id="e38f5-169">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e38f5-169">Click OK.</span></span>
8. <span data-ttu-id="e38f5-170">Á Aðgerðasvæðinu skal smella á Stjórna birgðum.</span><span class="sxs-lookup"><span data-stu-id="e38f5-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="e38f5-171">Smellt er á sjálfgefnar pöntunarstillingar.</span><span class="sxs-lookup"><span data-stu-id="e38f5-171">Click Default order settings.</span></span>
10. <span data-ttu-id="e38f5-172">Í svæði „Innkaupasvæði“ slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-173">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="e38f5-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="e38f5-174">Í svæði Birgðasvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-175">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="e38f5-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="e38f5-176">Í svæði Sölusvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-177">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="e38f5-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="e38f5-178">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e38f5-178">Close the page.</span></span>
14. <span data-ttu-id="e38f5-179">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e38f5-179">Close the page.</span></span>
15. <span data-ttu-id="e38f5-180">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e38f5-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e38f5-181">Smellt er á ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="e38f5-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="e38f5-182">Stækka hlutann Vinna með kostnað.</span><span class="sxs-lookup"><span data-stu-id="e38f5-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="e38f5-183">Í svæði Kostnaðarflokkur, slærðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="e38f5-184">Í þessu dæmi, slá inn M2.</span><span class="sxs-lookup"><span data-stu-id="e38f5-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="e38f5-185">Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.</span><span class="sxs-lookup"><span data-stu-id="e38f5-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="e38f5-186">Smellt er á Verð vöru.</span><span class="sxs-lookup"><span data-stu-id="e38f5-186">Click Item price.</span></span>
20. <span data-ttu-id="e38f5-187">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e38f5-187">Click New.</span></span>
21. <span data-ttu-id="e38f5-188">Í svæði Útgáfa, slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-189">Í þessu dæmi, velja 10.</span><span class="sxs-lookup"><span data-stu-id="e38f5-189">For this example, select 10.</span></span> <span data-ttu-id="e38f5-190">Þetta er kostnaðargerðin Staðalkostnaður.</span><span class="sxs-lookup"><span data-stu-id="e38f5-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="e38f5-191">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="e38f5-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-192">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="e38f5-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="e38f5-193">Í reitinn Verð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="e38f5-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="e38f5-194">Fyrir kynningu, slærðu inn 10.</span><span class="sxs-lookup"><span data-stu-id="e38f5-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="e38f5-195">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e38f5-195">Click Save.</span></span>
25. <span data-ttu-id="e38f5-196">Smellt er á Virk vöruverð.</span><span class="sxs-lookup"><span data-stu-id="e38f5-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="e38f5-197">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e38f5-197">Close the page.</span></span>
27. <span data-ttu-id="e38f5-198">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e38f5-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="e38f5-199">Stofna þriðja hráefni</span><span class="sxs-lookup"><span data-stu-id="e38f5-199">Create the third material</span></span>
1. <span data-ttu-id="e38f5-200">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e38f5-200">Click New.</span></span>
2. <span data-ttu-id="e38f5-201">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="e38f5-202">Fyrir kynningu, slærðu inn ITEM_C</span><span class="sxs-lookup"><span data-stu-id="e38f5-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="e38f5-203">Í reitinn Vörulíkanaflokkur skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-204">Veldu STD.</span><span class="sxs-lookup"><span data-stu-id="e38f5-204">Select STD.</span></span> <span data-ttu-id="e38f5-205">STD stendur fyrir staðalkostnaður og er mest notaða líkan þegar unnið með kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="e38f5-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="e38f5-206">Í reitinn Vöruflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-207">Veljið t.d. Hljóðvinnsla.</span><span class="sxs-lookup"><span data-stu-id="e38f5-207">For example, select Audio.</span></span> <span data-ttu-id="e38f5-208">Þetta hefur engin áhrif á kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="e38f5-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="e38f5-209">Í reitinn Geymsluvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-210">Velja SiteWH.</span><span class="sxs-lookup"><span data-stu-id="e38f5-210">Select SiteWH.</span></span> <span data-ttu-id="e38f5-211">Aðeins Svæði og vöruhús verður notað í kynning.</span><span class="sxs-lookup"><span data-stu-id="e38f5-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="e38f5-212">Í reitinn Rakningarvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-213">Rakningarvíddir verða ekki notað í þessa dæmi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="e38f5-214">Velja engar.</span><span class="sxs-lookup"><span data-stu-id="e38f5-214">Select None.</span></span>  
7. <span data-ttu-id="e38f5-215">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e38f5-215">Click OK.</span></span>
8. <span data-ttu-id="e38f5-216">Á Aðgerðasvæðinu skal smella á Stjórna birgðum.</span><span class="sxs-lookup"><span data-stu-id="e38f5-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="e38f5-217">Smellt er á sjálfgefnar pöntunarstillingar.</span><span class="sxs-lookup"><span data-stu-id="e38f5-217">Click Default order settings.</span></span>
10. <span data-ttu-id="e38f5-218">Í svæði „Innkaupasvæði“ slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-219">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="e38f5-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="e38f5-220">Í svæði Birgðasvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-221">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="e38f5-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="e38f5-222">Í svæði Sölusvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-223">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="e38f5-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="e38f5-224">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e38f5-224">Close the page.</span></span>
14. <span data-ttu-id="e38f5-225">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e38f5-225">Close the page.</span></span>
15. <span data-ttu-id="e38f5-226">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e38f5-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e38f5-227">Smellt er á ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="e38f5-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="e38f5-228">Stækka hlutann Vinna með kostnað.</span><span class="sxs-lookup"><span data-stu-id="e38f5-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="e38f5-229">Í svæði Kostnaðarflokkur, slærðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="e38f5-230">Í þessu dæmi, slá inn M1.</span><span class="sxs-lookup"><span data-stu-id="e38f5-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="e38f5-231">Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.</span><span class="sxs-lookup"><span data-stu-id="e38f5-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="e38f5-232">Smellt er á Verð vöru.</span><span class="sxs-lookup"><span data-stu-id="e38f5-232">Click Item price.</span></span>
20. <span data-ttu-id="e38f5-233">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e38f5-233">Click New.</span></span>
21. <span data-ttu-id="e38f5-234">Í svæði Útgáfa, slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e38f5-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-235">Í þessu dæmi, velja 10.</span><span class="sxs-lookup"><span data-stu-id="e38f5-235">For this example, select 10.</span></span> <span data-ttu-id="e38f5-236">Þetta er kostnaðargerðin Staðalkostnaður.</span><span class="sxs-lookup"><span data-stu-id="e38f5-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="e38f5-237">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="e38f5-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="e38f5-238">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="e38f5-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="e38f5-239">Í reitinn Verð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="e38f5-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="e38f5-240">Í þessu dæmi, slá inn 10.</span><span class="sxs-lookup"><span data-stu-id="e38f5-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="e38f5-241">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e38f5-241">Click Save.</span></span>
25. <span data-ttu-id="e38f5-242">Smellt er á Virk vöruverð.</span><span class="sxs-lookup"><span data-stu-id="e38f5-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="e38f5-243">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e38f5-243">Close the page.</span></span>
27. <span data-ttu-id="e38f5-244">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e38f5-244">Close the page.</span></span>


