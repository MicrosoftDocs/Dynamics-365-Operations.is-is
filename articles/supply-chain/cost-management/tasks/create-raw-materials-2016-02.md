---
title: Stofna hráefni (aðeins febrúar 2016)
description: Þetta verk einblínir á að búa til íhluti fullunnin vara og hálfunnin vara.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 869acddf6f7e9754bb4952176ded4b22c74eaffd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "327298"
---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="5b2d9-103">Stofna hráefni (aðeins febrúar 2016)</span><span class="sxs-lookup"><span data-stu-id="5b2d9-103">Create raw materials (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5b2d9-104">Þetta verk einblínir á að búa til íhluti fullunnin vara og hálfunnin vara.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="5b2d9-105">Þetta er þriðja verkið í línunni Útreikningur uppskrifta.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="5b2d9-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="5b2d9-107">Stofna fyrsta hráefni</span><span class="sxs-lookup"><span data-stu-id="5b2d9-107">Create the first material</span></span>
1. <span data-ttu-id="5b2d9-108">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="5b2d9-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-109">Click New.</span></span>
3. <span data-ttu-id="5b2d9-110">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="5b2d9-111">Í þessu dæmi, slá inn ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="5b2d9-112">Í reitinn Vörulíkanaflokkur skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-113">Veldu STD.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-113">Select STD.</span></span> <span data-ttu-id="5b2d9-114">STD stendur fyrir staðalkostnaður og er mest notaða líkan þegar unnið með kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="5b2d9-115">Í reitinn Vöruflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-116">Veljið t.d. Hljóðvinnsla.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-116">For example, select Audio.</span></span> <span data-ttu-id="5b2d9-117">Þetta hefur engin áhrif á kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="5b2d9-118">Í reitinn Geymsluvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-119">Velja SiteWH.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-119">Select SiteWH.</span></span> <span data-ttu-id="5b2d9-120">Aðeins Svæði og vöruhús verður notað í kynning.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="5b2d9-121">Í reitinn Rakningarvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-122">Rakningarvíddir verða ekki notað í þessa dæmi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="5b2d9-123">Velja engar.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-123">Select None.</span></span>  
8. <span data-ttu-id="5b2d9-124">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-124">Click OK.</span></span>
9. <span data-ttu-id="5b2d9-125">Á Aðgerðasvæðinu skal smella á Stjórna birgðum.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="5b2d9-126">Smellt er á sjálfgefnar pöntunarstillingar.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-126">Click Default order settings.</span></span>
11. <span data-ttu-id="5b2d9-127">Í svæði „Innkaupasvæði“ slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-128">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="5b2d9-129">Í svæði Birgðasvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-130">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="5b2d9-131">Í svæði Sölusvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-132">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="5b2d9-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-133">Close the page.</span></span>
15. <span data-ttu-id="5b2d9-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-134">Close the page.</span></span>
16. <span data-ttu-id="5b2d9-135">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5b2d9-136">Smellt er á ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="5b2d9-137">Stækka hlutann Vinna með kostnað.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="5b2d9-138">Í svæði Kostnaðarflokkur, slærðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="5b2d9-139">Í þessu dæmi, slá inn M2.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="5b2d9-140">Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="5b2d9-141">Smellt er á Verð vöru.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-141">Click Item price.</span></span>
21. <span data-ttu-id="5b2d9-142">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-142">Click New.</span></span>
22. <span data-ttu-id="5b2d9-143">Í svæði Útgáfa, slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-144">Í þessu dæmi, velja 10, sem er staðalkostnaður í þessari kostnaðargerð.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="5b2d9-145">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-146">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="5b2d9-147">Í reitinn Verð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="5b2d9-148">Í þessu dæmi, slá inn 10.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="5b2d9-149">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-149">Click Save.</span></span>
26. <span data-ttu-id="5b2d9-150">Smellt er á Virk vöruverð.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="5b2d9-151">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-151">Close the page.</span></span>
28. <span data-ttu-id="5b2d9-152">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="5b2d9-153">Stofna annað hráefni</span><span class="sxs-lookup"><span data-stu-id="5b2d9-153">Create the second material</span></span>
1. <span data-ttu-id="5b2d9-154">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-154">Click New.</span></span>
2. <span data-ttu-id="5b2d9-155">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="5b2d9-156">Í þessu dæmi, slá inn ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="5b2d9-157">Í reitinn Vörulíkanaflokkur skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-158">Veldu STD.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-158">Select STD.</span></span> <span data-ttu-id="5b2d9-159">STD stendur fyrir staðalkostnaður og er mest notaða líkan þegar unnið með kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="5b2d9-160">Í reitinn Vöruflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-161">Veljið t.d. Hljóðvinnsla.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-161">For example, select Audio.</span></span> <span data-ttu-id="5b2d9-162">Þetta hefur engin áhrif á kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="5b2d9-163">Í reitinn Geymsluvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-164">Velja SiteWH.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-164">Select SiteWH.</span></span> <span data-ttu-id="5b2d9-165">Aðeins Svæði og vöruhús verður notað í þessu dæmi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="5b2d9-166">Í reitinn Rakningarvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-167">Rakningarvíddir verða ekki notað í þessa dæmi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="5b2d9-168">Velja engar.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-168">Select None.</span></span>  
7. <span data-ttu-id="5b2d9-169">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-169">Click OK.</span></span>
8. <span data-ttu-id="5b2d9-170">Á Aðgerðasvæðinu skal smella á Stjórna birgðum.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="5b2d9-171">Smellt er á sjálfgefnar pöntunarstillingar.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-171">Click Default order settings.</span></span>
10. <span data-ttu-id="5b2d9-172">Í svæði „Innkaupasvæði“ slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-173">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="5b2d9-174">Í svæði Birgðasvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-175">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="5b2d9-176">Í svæði Sölusvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-177">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="5b2d9-178">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-178">Close the page.</span></span>
14. <span data-ttu-id="5b2d9-179">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-179">Close the page.</span></span>
15. <span data-ttu-id="5b2d9-180">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5b2d9-181">Smellt er á ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="5b2d9-182">Stækka hlutann Vinna með kostnað.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="5b2d9-183">Í svæði Kostnaðarflokkur, slærðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="5b2d9-184">Í þessu dæmi, slá inn M2.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="5b2d9-185">Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="5b2d9-186">Smellt er á Verð vöru.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-186">Click Item price.</span></span>
20. <span data-ttu-id="5b2d9-187">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-187">Click New.</span></span>
21. <span data-ttu-id="5b2d9-188">Í svæði Útgáfa, slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-189">Í þessu dæmi, velja 10.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-189">For this example, select 10.</span></span> <span data-ttu-id="5b2d9-190">Þetta er kostnaðargerðin Staðalkostnaður.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="5b2d9-191">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-192">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="5b2d9-193">Í reitinn Verð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="5b2d9-194">Fyrir kynningu, slærðu inn 10.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="5b2d9-195">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-195">Click Save.</span></span>
25. <span data-ttu-id="5b2d9-196">Smellt er á Virk vöruverð.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="5b2d9-197">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-197">Close the page.</span></span>
27. <span data-ttu-id="5b2d9-198">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="5b2d9-199">Stofna þriðja hráefni</span><span class="sxs-lookup"><span data-stu-id="5b2d9-199">Create the third material</span></span>
1. <span data-ttu-id="5b2d9-200">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-200">Click New.</span></span>
2. <span data-ttu-id="5b2d9-201">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="5b2d9-202">Fyrir kynningu, slærðu inn ITEM_C</span><span class="sxs-lookup"><span data-stu-id="5b2d9-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="5b2d9-203">Í reitinn Vörulíkanaflokkur skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-204">Veldu STD.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-204">Select STD.</span></span> <span data-ttu-id="5b2d9-205">STD stendur fyrir staðalkostnaður og er mest notaða líkan þegar unnið með kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="5b2d9-206">Í reitinn Vöruflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-207">Veljið t.d. Hljóðvinnsla.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-207">For example, select Audio.</span></span> <span data-ttu-id="5b2d9-208">Þetta hefur engin áhrif á kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="5b2d9-209">Í reitinn Geymsluvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-210">Velja SiteWH.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-210">Select SiteWH.</span></span> <span data-ttu-id="5b2d9-211">Aðeins Svæði og vöruhús verður notað í kynning.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="5b2d9-212">Í reitinn Rakningarvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-213">Rakningarvíddir verða ekki notað í þessa dæmi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="5b2d9-214">Velja engar.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-214">Select None.</span></span>  
7. <span data-ttu-id="5b2d9-215">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-215">Click OK.</span></span>
8. <span data-ttu-id="5b2d9-216">Á Aðgerðasvæðinu skal smella á Stjórna birgðum.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="5b2d9-217">Smellt er á sjálfgefnar pöntunarstillingar.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-217">Click Default order settings.</span></span>
10. <span data-ttu-id="5b2d9-218">Í svæði „Innkaupasvæði“ slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-219">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="5b2d9-220">Í svæði Birgðasvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-221">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="5b2d9-222">Í svæði Sölusvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-223">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="5b2d9-224">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-224">Close the page.</span></span>
14. <span data-ttu-id="5b2d9-225">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-225">Close the page.</span></span>
15. <span data-ttu-id="5b2d9-226">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="5b2d9-227">Smellt er á ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="5b2d9-228">Stækka hlutann Vinna með kostnað.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="5b2d9-229">Í svæði Kostnaðarflokkur, slærðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="5b2d9-230">Í þessu dæmi, slá inn M1.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="5b2d9-231">Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="5b2d9-232">Smellt er á Verð vöru.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-232">Click Item price.</span></span>
20. <span data-ttu-id="5b2d9-233">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-233">Click New.</span></span>
21. <span data-ttu-id="5b2d9-234">Í svæði Útgáfa, slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-235">Í þessu dæmi, velja 10.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-235">For this example, select 10.</span></span> <span data-ttu-id="5b2d9-236">Þetta er kostnaðargerðin Staðalkostnaður.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="5b2d9-237">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="5b2d9-238">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="5b2d9-239">Í reitinn Verð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="5b2d9-240">Í þessu dæmi, slá inn 10.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="5b2d9-241">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-241">Click Save.</span></span>
25. <span data-ttu-id="5b2d9-242">Smellt er á Virk vöruverð.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="5b2d9-243">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-243">Close the page.</span></span>
27. <span data-ttu-id="5b2d9-244">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5b2d9-244">Close the page.</span></span>

