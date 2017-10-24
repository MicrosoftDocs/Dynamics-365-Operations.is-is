--- 
title: "Stofna hráefni (aðeins febrúar 2016)"
description: "Þetta verk einblínir á að búa til íhluti fullunnin vara og hálfunnin vara."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3d77dcc20fe7402af83dd724e7fef848977e5bf8
ms.openlocfilehash: f6af7b93d8d1d9a6f7474f24177b16e5295e90d6
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="7cbb4-103">Stofna hráefni (aðeins febrúar 2016)</span><span class="sxs-lookup"><span data-stu-id="7cbb4-103">Create raw materials (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7cbb4-104">Þetta verk einblínir á að búa til íhluti fullunnin vara og hálfunnin vara.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="7cbb4-105">Þetta er þriðja verkið í línunni Útreikningur uppskrifta.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="7cbb4-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="7cbb4-107">Stofna fyrsta hráefni</span><span class="sxs-lookup"><span data-stu-id="7cbb4-107">Create the first material</span></span>
1. <span data-ttu-id="7cbb4-108">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="7cbb4-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-109">Click New.</span></span>
3. <span data-ttu-id="7cbb4-110">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="7cbb4-111">Í þessu dæmi, slá inn ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="7cbb4-112">Í reitinn Vörulíkanaflokkur skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-113">Veldu STD.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-113">Select STD.</span></span> <span data-ttu-id="7cbb4-114">STD stendur fyrir staðalkostnaður og er mest notaða líkan þegar unnið með kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="7cbb4-115">Í reitinn Vöruflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-116">Veljið t.d. Hljóðvinnsla.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-116">For example, select Audio.</span></span> <span data-ttu-id="7cbb4-117">Þetta hefur engin áhrif á kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="7cbb4-118">Í reitinn Geymsluvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-119">Velja SiteWH.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-119">Select SiteWH.</span></span> <span data-ttu-id="7cbb4-120">Aðeins Svæði og vöruhús verður notað í kynning.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="7cbb4-121">Í reitinn Rakningarvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-122">Rakningarvíddir verða ekki notað í þessa dæmi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="7cbb4-123">Velja engar.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-123">Select None.</span></span>  
8. <span data-ttu-id="7cbb4-124">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-124">Click OK.</span></span>
9. <span data-ttu-id="7cbb4-125">Á Aðgerðasvæðinu skal smella á Stjórna birgðum.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="7cbb4-126">Smellt er á sjálfgefnar pöntunarstillingar.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-126">Click Default order settings.</span></span>
11. <span data-ttu-id="7cbb4-127">Í svæði „Innkaupasvæði“ slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-128">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="7cbb4-129">Í svæði Birgðasvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-130">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="7cbb4-131">Í svæði Sölusvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-132">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="7cbb4-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-133">Close the page.</span></span>
15. <span data-ttu-id="7cbb4-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-134">Close the page.</span></span>
16. <span data-ttu-id="7cbb4-135">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7cbb4-136">Smellt er á ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="7cbb4-137">Stækka hlutann Vinna með kostnað.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="7cbb4-138">Í svæði Kostnaðarflokkur, slærðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="7cbb4-139">Í þessu dæmi, slá inn M2.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="7cbb4-140">Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="7cbb4-141">Smellt er á Verð vöru.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-141">Click Item price.</span></span>
21. <span data-ttu-id="7cbb4-142">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-142">Click New.</span></span>
22. <span data-ttu-id="7cbb4-143">Í svæði Útgáfa, slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-144">Í þessu dæmi, velja 10, sem er staðalkostnaður í þessari kostnaðargerð.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="7cbb4-145">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-146">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="7cbb4-147">Í reitinn Verð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="7cbb4-148">Í þessu dæmi, slá inn 10.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="7cbb4-149">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-149">Click Save.</span></span>
26. <span data-ttu-id="7cbb4-150">Smellt er á Virk vöruverð.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="7cbb4-151">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-151">Close the page.</span></span>
28. <span data-ttu-id="7cbb4-152">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="7cbb4-153">Stofna annað hráefni</span><span class="sxs-lookup"><span data-stu-id="7cbb4-153">Create the second material</span></span>
1. <span data-ttu-id="7cbb4-154">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-154">Click New.</span></span>
2. <span data-ttu-id="7cbb4-155">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="7cbb4-156">Í þessu dæmi, slá inn ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="7cbb4-157">Í reitinn Vörulíkanaflokkur skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-158">Veldu STD.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-158">Select STD.</span></span> <span data-ttu-id="7cbb4-159">STD stendur fyrir staðalkostnaður og er mest notaða líkan þegar unnið með kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="7cbb4-160">Í reitinn Vöruflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-161">Veljið t.d. Hljóðvinnsla.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-161">For example, select Audio.</span></span> <span data-ttu-id="7cbb4-162">Þetta hefur engin áhrif á kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="7cbb4-163">Í reitinn Geymsluvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-164">Velja SiteWH.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-164">Select SiteWH.</span></span> <span data-ttu-id="7cbb4-165">Aðeins Svæði og vöruhús verður notað í þessu dæmi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="7cbb4-166">Í reitinn Rakningarvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-167">Rakningarvíddir verða ekki notað í þessa dæmi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="7cbb4-168">Velja engar.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-168">Select None.</span></span>  
7. <span data-ttu-id="7cbb4-169">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-169">Click OK.</span></span>
8. <span data-ttu-id="7cbb4-170">Á Aðgerðasvæðinu skal smella á Stjórna birgðum.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="7cbb4-171">Smellt er á sjálfgefnar pöntunarstillingar.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-171">Click Default order settings.</span></span>
10. <span data-ttu-id="7cbb4-172">Í svæði „Innkaupasvæði“ slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-173">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="7cbb4-174">Í svæði Birgðasvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-175">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="7cbb4-176">Í svæði Sölusvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-177">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="7cbb4-178">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-178">Close the page.</span></span>
14. <span data-ttu-id="7cbb4-179">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-179">Close the page.</span></span>
15. <span data-ttu-id="7cbb4-180">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7cbb4-181">Smellt er á ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="7cbb4-182">Stækka hlutann Vinna með kostnað.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="7cbb4-183">Í svæði Kostnaðarflokkur, slærðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="7cbb4-184">Í þessu dæmi, slá inn M2.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="7cbb4-185">Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="7cbb4-186">Smellt er á Verð vöru.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-186">Click Item price.</span></span>
20. <span data-ttu-id="7cbb4-187">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-187">Click New.</span></span>
21. <span data-ttu-id="7cbb4-188">Í svæði Útgáfa, slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-189">Í þessu dæmi, velja 10.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-189">For this example, select 10.</span></span> <span data-ttu-id="7cbb4-190">Þetta er kostnaðargerðin Staðalkostnaður.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="7cbb4-191">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-192">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="7cbb4-193">Í reitinn Verð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="7cbb4-194">Fyrir kynningu, slærðu inn 10.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="7cbb4-195">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-195">Click Save.</span></span>
25. <span data-ttu-id="7cbb4-196">Smellt er á Virk vöruverð.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="7cbb4-197">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-197">Close the page.</span></span>
27. <span data-ttu-id="7cbb4-198">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="7cbb4-199">Stofna þriðja hráefni</span><span class="sxs-lookup"><span data-stu-id="7cbb4-199">Create the third material</span></span>
1. <span data-ttu-id="7cbb4-200">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-200">Click New.</span></span>
2. <span data-ttu-id="7cbb4-201">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="7cbb4-202">Fyrir kynningu, slærðu inn ITEM_C</span><span class="sxs-lookup"><span data-stu-id="7cbb4-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="7cbb4-203">Í reitinn Vörulíkanaflokkur skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-204">Veldu STD.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-204">Select STD.</span></span> <span data-ttu-id="7cbb4-205">STD stendur fyrir staðalkostnaður og er mest notaða líkan þegar unnið með kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="7cbb4-206">Í reitinn Vöruflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-207">Veljið t.d. Hljóðvinnsla.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-207">For example, select Audio.</span></span> <span data-ttu-id="7cbb4-208">Þetta hefur engin áhrif á kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="7cbb4-209">Í reitinn Geymsluvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-210">Velja SiteWH.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-210">Select SiteWH.</span></span> <span data-ttu-id="7cbb4-211">Aðeins Svæði og vöruhús verður notað í kynning.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="7cbb4-212">Í reitinn Rakningarvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-213">Rakningarvíddir verða ekki notað í þessa dæmi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="7cbb4-214">Velja engar.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-214">Select None.</span></span>  
7. <span data-ttu-id="7cbb4-215">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-215">Click OK.</span></span>
8. <span data-ttu-id="7cbb4-216">Á Aðgerðasvæðinu skal smella á Stjórna birgðum.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="7cbb4-217">Smellt er á sjálfgefnar pöntunarstillingar.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-217">Click Default order settings.</span></span>
10. <span data-ttu-id="7cbb4-218">Í svæði „Innkaupasvæði“ slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-219">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="7cbb4-220">Í svæði Birgðasvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-221">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="7cbb4-222">Í svæði Sölusvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-223">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="7cbb4-224">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-224">Close the page.</span></span>
14. <span data-ttu-id="7cbb4-225">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-225">Close the page.</span></span>
15. <span data-ttu-id="7cbb4-226">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7cbb4-227">Smellt er á ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="7cbb4-228">Stækka hlutann Vinna með kostnað.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="7cbb4-229">Í svæði Kostnaðarflokkur, slærðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="7cbb4-230">Í þessu dæmi, slá inn M1.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="7cbb4-231">Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="7cbb4-232">Smellt er á Verð vöru.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-232">Click Item price.</span></span>
20. <span data-ttu-id="7cbb4-233">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-233">Click New.</span></span>
21. <span data-ttu-id="7cbb4-234">Í svæði Útgáfa, slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-235">Í þessu dæmi, velja 10.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-235">For this example, select 10.</span></span> <span data-ttu-id="7cbb4-236">Þetta er kostnaðargerðin Staðalkostnaður.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="7cbb4-237">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7cbb4-238">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="7cbb4-239">Í reitinn Verð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="7cbb4-240">Í þessu dæmi, slá inn 10.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="7cbb4-241">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-241">Click Save.</span></span>
25. <span data-ttu-id="7cbb4-242">Smellt er á Virk vöruverð.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="7cbb4-243">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-243">Close the page.</span></span>
27. <span data-ttu-id="7cbb4-244">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-244">Close the page.</span></span>


