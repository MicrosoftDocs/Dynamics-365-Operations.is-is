---
title: Setja upp bókunarreglur fyrir eignir
description: Þessi leiðarvísi fyrir verk setja upp bókunarreglur eigna.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 286c8732c1f2c92d0f16582b0b9de41990280e5a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "351103"
---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="616aa-103">Setja upp bókunarreglur fyrir eignir</span><span class="sxs-lookup"><span data-stu-id="616aa-103">Set up fixed asset posting profiles</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="616aa-104">Þessi leiðarvísi fyrir verk setja upp bókunarreglur eigna.</span><span class="sxs-lookup"><span data-stu-id="616aa-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="616aa-105">Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila.</span><span class="sxs-lookup"><span data-stu-id="616aa-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="616aa-106">Dæmi í leiðarvísi fyrir verk eru fyrir grunn bókunarreglu, þó verður að stofna bókunarreglur fyrir tiltekinn bókhaldslykil og kröfur fyrir fjárhagsskýrslu.</span><span class="sxs-lookup"><span data-stu-id="616aa-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="616aa-107">Fara í eignir > Uppsetning > Bókunarreglur eigna.</span><span class="sxs-lookup"><span data-stu-id="616aa-107">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="616aa-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="616aa-108">Click New.</span></span>
3. <span data-ttu-id="616aa-109">Í reitinn bókunarregla skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="616aa-109">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="616aa-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="616aa-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="616aa-111">Þarf að stofna bókunarreglu fyrir hverja tegund eignafærslu sem verður notuð þegar unnið er með eignir.</span><span class="sxs-lookup"><span data-stu-id="616aa-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span>  <span data-ttu-id="616aa-112">Þessi leiðarvísi fyrir verk byrja á ferðinni kaupfærsla.</span><span class="sxs-lookup"><span data-stu-id="616aa-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="616aa-113">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="616aa-113">Click Add.</span></span>
6. <span data-ttu-id="616aa-114">Sláið inn eða veldu gildi í reitnum Bók.</span><span class="sxs-lookup"><span data-stu-id="616aa-114">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="616aa-115">svæðið Flokkanir gerir kleift að skilgreina bókunarreglu niður í Töflu (einum lykli sett upp fyrir hverja eign) eða Flokkur (einum lykli sett upp fyrir hvern eignaflokk).</span><span class="sxs-lookup"><span data-stu-id="616aa-115">The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span>  <span data-ttu-id="616aa-116">Í þessum verkefnaleiðbeiningar skilja eftir gildið stillt á „Allt“ til að nota á allar eignir í tilgreindan bók.</span><span class="sxs-lookup"><span data-stu-id="616aa-116">For this task guide I will leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="616aa-117">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-117">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="616aa-118">Fyrir Kaup, hægt að færa inn mótlykil eða hafa það autt til að fylla út fyrir tiltekna færslu.</span><span class="sxs-lookup"><span data-stu-id="616aa-118">For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="616aa-119">Í reitnum færslugerð er valinn leiðrétting kaupa.</span><span class="sxs-lookup"><span data-stu-id="616aa-119">In the Transaction type field, select 'Acquisition adjustment'.</span></span>
    * <span data-ttu-id="616aa-120">Fyrir Leiðréttingarfærslna kaupa, nota sömu lyklar sem notað fyrir kaupfærsla.</span><span class="sxs-lookup"><span data-stu-id="616aa-120">For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="616aa-121">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="616aa-121">Click Add.</span></span>
10. <span data-ttu-id="616aa-122">Sláið inn eða veldu gildi í reitnum Bók.</span><span class="sxs-lookup"><span data-stu-id="616aa-122">In the Book field, enter or select a value.</span></span>
11. <span data-ttu-id="616aa-123">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-123">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="616aa-124">Fyrir leiðréttingar Kaupa hægt að færa inn mótlykil eða skilja eftir autt til að fylla út fyrir tiltekna færslu.</span><span class="sxs-lookup"><span data-stu-id="616aa-124">For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="616aa-125">Í reitnum færslugerð er valinn afskrift.</span><span class="sxs-lookup"><span data-stu-id="616aa-125">In the Transaction type field, select 'Depreciation'.</span></span>
13. <span data-ttu-id="616aa-126">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="616aa-126">Click Add.</span></span>
14. <span data-ttu-id="616aa-127">Sláið inn eða veldu gildi í reitnum Bók.</span><span class="sxs-lookup"><span data-stu-id="616aa-127">In the Book field, enter or select a value.</span></span>
15. <span data-ttu-id="616aa-128">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-128">In the Main account field, specify the desired values.</span></span>
16. <span data-ttu-id="616aa-129">Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-129">In the Offset account field, specify the desired values.</span></span>
17. <span data-ttu-id="616aa-130">Í reitnum færslugerð er valinn leiðrétting afskriftar.</span><span class="sxs-lookup"><span data-stu-id="616aa-130">In the Transaction type field, select 'Depreciation adjustment'.</span></span>
    * <span data-ttu-id="616aa-131">Fyrir Leiðréttingarfærslna afskrift, nota sömu lyklar sem notað fyrir afskriftarfærsla.</span><span class="sxs-lookup"><span data-stu-id="616aa-131">For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="616aa-132">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="616aa-132">Click Add.</span></span>
19. <span data-ttu-id="616aa-133">Sláið inn eða veldu gildi í reitnum Bók.</span><span class="sxs-lookup"><span data-stu-id="616aa-133">In the Book field, enter or select a value.</span></span>
20. <span data-ttu-id="616aa-134">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-134">In the Main account field, specify the desired values.</span></span>
21. <span data-ttu-id="616aa-135">Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-135">In the Offset account field, specify the desired values.</span></span>
22. <span data-ttu-id="616aa-136">Í reitnum færslugerð er valinn afskráning - Sala.</span><span class="sxs-lookup"><span data-stu-id="616aa-136">In the Transaction type field, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="616aa-137">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="616aa-137">Click Add.</span></span>
24. <span data-ttu-id="616aa-138">Sláið inn eða veldu gildi í reitnum Bók.</span><span class="sxs-lookup"><span data-stu-id="616aa-138">In the Book field, enter or select a value.</span></span>
25. <span data-ttu-id="616aa-139">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-139">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="616aa-140">Fyrir afskráningar, hægt að færa inn mótlykil eða skilja eftir autt til að fylla út fyrir tiltekna færslu.</span><span class="sxs-lookup"><span data-stu-id="616aa-140">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="616aa-141">Í reitnum færslugerð er valinn afskráning - rýrnun.</span><span class="sxs-lookup"><span data-stu-id="616aa-141">In the Transaction type field, select 'Disposal - scrap'.</span></span>
    * <span data-ttu-id="616aa-142">nota sömu lyklar fyrir Losun sölu og Losun rýrnunar.</span><span class="sxs-lookup"><span data-stu-id="616aa-142">We will use the same accounts for Disposal sale and Disposal scrap.</span></span>  
27. <span data-ttu-id="616aa-143">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="616aa-143">Click Add.</span></span>
28. <span data-ttu-id="616aa-144">Sláið inn eða veldu gildi í reitnum Bók.</span><span class="sxs-lookup"><span data-stu-id="616aa-144">In the Book field, enter or select a value.</span></span>
29. <span data-ttu-id="616aa-145">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-145">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="616aa-146">Fyrir afskráningar, hægt að færa inn mótlykil eða skilja eftir autt til að fylla út fyrir tiltekna færslu.</span><span class="sxs-lookup"><span data-stu-id="616aa-146">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="616aa-147">Víkka hlutann Förgun.</span><span class="sxs-lookup"><span data-stu-id="616aa-147">Expand the Disposal section.</span></span>
    * <span data-ttu-id="616aa-148">Setja verður upp bókunarreglur afskráningar fyrir sölu og rýrnun.</span><span class="sxs-lookup"><span data-stu-id="616aa-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="616aa-149">byrjað verður á sölufærslu afskráningar</span><span class="sxs-lookup"><span data-stu-id="616aa-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="616aa-150">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="616aa-150">Click Add.</span></span>
32. <span data-ttu-id="616aa-151">Sláið inn eða veldu gildi í reitnum Bók.</span><span class="sxs-lookup"><span data-stu-id="616aa-151">In the Book field, enter or select a value.</span></span>
33. <span data-ttu-id="616aa-152">í svæðinu Bóka gildi Veljið 'Kaupvirði'.</span><span class="sxs-lookup"><span data-stu-id="616aa-152">In the Post value field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="616aa-153">Kaupvirði verður á við um Kaup og leiðréttinggildi kaupa fyrir öll árin.</span><span class="sxs-lookup"><span data-stu-id="616aa-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span>  <span data-ttu-id="616aa-154">Einnig er hægt að skilgreina lykla fyrir þessar færslugerð sérstaklega.</span><span class="sxs-lookup"><span data-stu-id="616aa-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="616aa-155">Hægt er að setja afskráningarferlið til að nota á mismunandi lykla eftir því hvort afskráning leiðir hagnaður eða taps.</span><span class="sxs-lookup"><span data-stu-id="616aa-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span>  <span data-ttu-id="616aa-156">Gerð söluvirði verður stillt á "Allt" til að nota sömu lyklar fyrir allar gerðir afskráningar.</span><span class="sxs-lookup"><span data-stu-id="616aa-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="616aa-157">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-157">In the Main account field, specify the desired values.</span></span>
35. <span data-ttu-id="616aa-158">Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-158">In the Offset account field, specify the desired values.</span></span>
36. <span data-ttu-id="616aa-159">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="616aa-159">Click Add.</span></span>
37. <span data-ttu-id="616aa-160">Sláið inn eða veldu gildi í reitnum Bók.</span><span class="sxs-lookup"><span data-stu-id="616aa-160">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="616aa-161">Veljið 'Afskriftir (fyrri ár)' í svæðinu Bóka gildi.</span><span class="sxs-lookup"><span data-stu-id="616aa-161">In the Post value field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="616aa-162">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-162">In the Main account field, specify the desired values.</span></span>
39. <span data-ttu-id="616aa-163">Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-163">In the Offset account field, specify the desired values.</span></span>
40. <span data-ttu-id="616aa-164">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="616aa-164">Click Add.</span></span>
41. <span data-ttu-id="616aa-165">Sláið inn eða veldu gildi í reitnum Bók.</span><span class="sxs-lookup"><span data-stu-id="616aa-165">In the Book field, enter or select a value.</span></span>
42. <span data-ttu-id="616aa-166">Veljið 'Afskriftir (fyrri ár)' í svæðinu Bóka gildi.</span><span class="sxs-lookup"><span data-stu-id="616aa-166">In the Post value field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="616aa-167">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-167">In the Main account field, specify the desired values.</span></span>
44. <span data-ttu-id="616aa-168">Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-168">In the Offset account field, specify the desired values.</span></span>
45. <span data-ttu-id="616aa-169">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="616aa-169">Click Add.</span></span>
46. <span data-ttu-id="616aa-170">Sláið inn eða veldu gildi í reitnum Bók.</span><span class="sxs-lookup"><span data-stu-id="616aa-170">In the Book field, enter or select a value.</span></span>
47. <span data-ttu-id="616aa-171">Veljið í svæðinu Bóka gildi 'Afskriftaleiðréttingar (fyrra árs)'.</span><span class="sxs-lookup"><span data-stu-id="616aa-171">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="616aa-172">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-172">In the Main account field, specify the desired values.</span></span>
49. <span data-ttu-id="616aa-173">Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-173">In the Offset account field, specify the desired values.</span></span>
50. <span data-ttu-id="616aa-174">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="616aa-174">Click Add.</span></span>
51. <span data-ttu-id="616aa-175">Sláið inn eða veldu gildi í reitnum Bók.</span><span class="sxs-lookup"><span data-stu-id="616aa-175">In the Book field, enter or select a value.</span></span>
52. <span data-ttu-id="616aa-176">Veljið í svæðinu Bóka gildi 'Afskriftaleiðréttingar (þessa árs)'.</span><span class="sxs-lookup"><span data-stu-id="616aa-176">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="616aa-177">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-177">In the Main account field, specify the desired values.</span></span>
54. <span data-ttu-id="616aa-178">Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-178">In the Offset account field, specify the desired values.</span></span>
55. <span data-ttu-id="616aa-179">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="616aa-179">Click Add.</span></span>
56. <span data-ttu-id="616aa-180">Sláið inn eða veldu gildi í reitnum Bók.</span><span class="sxs-lookup"><span data-stu-id="616aa-180">In the Book field, enter or select a value.</span></span>
57. <span data-ttu-id="616aa-181">Veljið "Bókað nettóvirði" í svæðinu Bóka gildi.</span><span class="sxs-lookup"><span data-stu-id="616aa-181">In the Post value field, select 'Net book value'.</span></span>
58. <span data-ttu-id="616aa-182">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-182">In the Main account field, specify the desired values.</span></span>
59. <span data-ttu-id="616aa-183">Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-183">In the Offset account field, specify the desired values.</span></span>
60. <span data-ttu-id="616aa-184">Veljið "Rýrnun" í reitnum Sala eða rýrnun.</span><span class="sxs-lookup"><span data-stu-id="616aa-184">In the Sale or scrap field, select 'Scrap'.</span></span>
61. <span data-ttu-id="616aa-185">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="616aa-185">Click Add.</span></span>
62. <span data-ttu-id="616aa-186">Sláið inn eða veldu gildi í reitnum Bók.</span><span class="sxs-lookup"><span data-stu-id="616aa-186">In the Book field, enter or select a value.</span></span>
63. <span data-ttu-id="616aa-187">í svæðinu Bóka gildi Veljið 'Kaupvirði'.</span><span class="sxs-lookup"><span data-stu-id="616aa-187">In the Post value field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="616aa-188">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-188">In the Main account field, specify the desired values.</span></span>
65. <span data-ttu-id="616aa-189">Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-189">In the Offset account field, specify the desired values.</span></span>
66. <span data-ttu-id="616aa-190">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="616aa-190">Click Add.</span></span>
67. <span data-ttu-id="616aa-191">Sláið inn eða veldu gildi í reitnum Bók.</span><span class="sxs-lookup"><span data-stu-id="616aa-191">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="616aa-192">Í svæðinu Bóka gildi, veljið "Afskriftir (fyrri ár)".</span><span class="sxs-lookup"><span data-stu-id="616aa-192">In Post value field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="616aa-193">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-193">In the Main account field, specify the desired values.</span></span>
69. <span data-ttu-id="616aa-194">Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-194">In the Offset account field, specify the desired values.</span></span>
70. <span data-ttu-id="616aa-195">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="616aa-195">Click Add.</span></span>
71. <span data-ttu-id="616aa-196">Sláið inn eða veldu gildi í reitnum Bók.</span><span class="sxs-lookup"><span data-stu-id="616aa-196">In the Book field, enter or select a value.</span></span>
72. <span data-ttu-id="616aa-197">Veljið 'Afskriftir (fyrri ár)' í svæðinu Bóka gildi.</span><span class="sxs-lookup"><span data-stu-id="616aa-197">In the Post value field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="616aa-198">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-198">In the Main account field, specify the desired values.</span></span>
74. <span data-ttu-id="616aa-199">Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-199">In the Offset account field, specify the desired values.</span></span>
75. <span data-ttu-id="616aa-200">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="616aa-200">Click Add.</span></span>
76. <span data-ttu-id="616aa-201">Sláið inn eða veldu gildi í reitnum Bók.</span><span class="sxs-lookup"><span data-stu-id="616aa-201">In the Book field, enter or select a value.</span></span>
77. <span data-ttu-id="616aa-202">Veljið í svæðinu Bóka gildi 'Afskriftaleiðréttingar (fyrra árs)'.</span><span class="sxs-lookup"><span data-stu-id="616aa-202">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="616aa-203">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-203">In the Main account field, specify the desired values.</span></span>
79. <span data-ttu-id="616aa-204">Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-204">In the Offset account field, specify the desired values.</span></span>
80. <span data-ttu-id="616aa-205">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="616aa-205">Click Add.</span></span>
81. <span data-ttu-id="616aa-206">Sláið inn eða veldu gildi í reitnum Bók.</span><span class="sxs-lookup"><span data-stu-id="616aa-206">In the Book field, enter or select a value.</span></span>
82. <span data-ttu-id="616aa-207">Veljið í svæðinu Bóka gildi 'Afskriftaleiðréttingar (þessa árs)'.</span><span class="sxs-lookup"><span data-stu-id="616aa-207">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="616aa-208">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-208">In the Main account field, specify the desired values.</span></span>
84. <span data-ttu-id="616aa-209">Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-209">In the Offset account field, specify the desired values.</span></span>
85. <span data-ttu-id="616aa-210">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="616aa-210">Click Add.</span></span>
86. <span data-ttu-id="616aa-211">Sláið inn eða veldu gildi í reitnum Bók.</span><span class="sxs-lookup"><span data-stu-id="616aa-211">In the Book field, enter or select a value.</span></span>
87. <span data-ttu-id="616aa-212">Veljið "Bókað nettóvirði" í svæðinu Bóka gildi.</span><span class="sxs-lookup"><span data-stu-id="616aa-212">In the Post value field, select 'Net book value'.</span></span>
88. <span data-ttu-id="616aa-213">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-213">In the Main account field, specify the desired values.</span></span>
89. <span data-ttu-id="616aa-214">Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="616aa-214">In the Offset account field, specify the desired values.</span></span>

