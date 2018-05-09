---
title: "Setja upp gæðapantanir"
description: "Þessi verklýsing sýnir hvernig á að virkja gæðastjórnunarferli þar sem innhreyfingar birgða verða skoðaðar strax eftir komuskráningu."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e44b585c6e6e86d244328e73846a5c91f94233eb
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-quality-orders"></a><span data-ttu-id="8383a-103">Setja upp gæðapantanir</span><span class="sxs-lookup"><span data-stu-id="8383a-103">Set up quality orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8383a-104">Þessi verklýsing sýnir hvernig á að virkja gæðastjórnunarferli þar sem innhreyfingar birgða verða skoðaðar strax eftir komuskráningu.</span><span class="sxs-lookup"><span data-stu-id="8383a-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="8383a-105">Ferlið er yfirleitt framkvæma með gæðastjóra.</span><span class="sxs-lookup"><span data-stu-id="8383a-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="8383a-106">Ferlið inniheldur stofnun gæðaflokks til að skilgreina vörurnar sem á að nota sem sýni, og prófunarflokk til að flokka prófanir sem á að framkvæma á vörum í gæðaflokkinn.</span><span class="sxs-lookup"><span data-stu-id="8383a-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="8383a-107">Hægt er að keyra þessari leiðbeiningar í sýnigögnum USMF-fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="8383a-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="8383a-108">Gæðastjórnun virkjuð</span><span class="sxs-lookup"><span data-stu-id="8383a-108">Enable quality management</span></span>
1. <span data-ttu-id="8383a-109">Fara í Birgðastjórnun > Uppsetning > Birgðir og færibreytur vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="8383a-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="8383a-110">Smellið á flipann gæðastjórnun.</span><span class="sxs-lookup"><span data-stu-id="8383a-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="8383a-111">Setja skal Nota gæðastjórnun valkosturinn á Já.</span><span class="sxs-lookup"><span data-stu-id="8383a-111">Set the Use quality management option to Yes.</span></span>
4. <span data-ttu-id="8383a-112">Smellt er á uppsetningu Skýrslu.</span><span class="sxs-lookup"><span data-stu-id="8383a-112">Click Report setup.</span></span>
    * <span data-ttu-id="8383a-113">Á USMF, er skýrsluuppsetning fyrir gæðastjórnun er þegar skilgreind.</span><span class="sxs-lookup"><span data-stu-id="8383a-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="8383a-114">Hafi þetta ekki verið gert myndirðu bæta við nýjum línum hér fyrir mismunandi skýrslugerðir, og veldu gerð skjals sem á að nota fyrir hverja skýrslu.</span><span class="sxs-lookup"><span data-stu-id="8383a-114">If this wasn’t done, you’d add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="8383a-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8383a-115">Close the page.</span></span>
6. <span data-ttu-id="8383a-116">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8383a-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="8383a-117">Stofna próf</span><span class="sxs-lookup"><span data-stu-id="8383a-117">Create a test</span></span>
1. <span data-ttu-id="8383a-118">Fara í Birgðastjórnun > Uppsetning > gæðaeftirlit > prófanir</span><span class="sxs-lookup"><span data-stu-id="8383a-118">Go to Inventory management > Setup > Quality control > Tests.</span></span>
2. <span data-ttu-id="8383a-119">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="8383a-119">Click New.</span></span>
3. <span data-ttu-id="8383a-120">Í reitinn Prófun skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8383a-120">In the Test field, type a value.</span></span>
4. <span data-ttu-id="8383a-121">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="8383a-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8383a-122">Í reitnum Tegund skal velja „valkostur“.</span><span class="sxs-lookup"><span data-stu-id="8383a-122">In the Type field, select 'Option'.</span></span>
    * <span data-ttu-id="8383a-123">Í þessu dæmi veljum við valkosturinn sem munu gera það mögulegt að úthluta niðurstöðurnar prófana byggt á fyrirframskilgreindu gildi.</span><span class="sxs-lookup"><span data-stu-id="8383a-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="8383a-124">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="8383a-124">Click Save.</span></span>
7. <span data-ttu-id="8383a-125">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8383a-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="8383a-126">Stofna prófunarbreytur til að skilgreina hvernig prófunarniðurstöður eru skráðar</span><span class="sxs-lookup"><span data-stu-id="8383a-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="8383a-127">Fara í Birgðastjórnun > Uppsetning > gæðaeftirlit >  prófunarbreytur</span><span class="sxs-lookup"><span data-stu-id="8383a-127">Go to Inventory management > Setup > Quality control > Test variables.</span></span>
2. <span data-ttu-id="8383a-128">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="8383a-128">Click New.</span></span>
3. <span data-ttu-id="8383a-129">Í reitinn breyta skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8383a-129">In the Variable field, type a value.</span></span>
4. <span data-ttu-id="8383a-130">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="8383a-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8383a-131">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="8383a-131">Click Save.</span></span>
6. <span data-ttu-id="8383a-132">Smelltu á Niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="8383a-132">Click Outcomes.</span></span>
7. <span data-ttu-id="8383a-133">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="8383a-133">Click New.</span></span>
8. <span data-ttu-id="8383a-134">Í reitinn niðurstöðu skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8383a-134">In the Outcome field, type a value.</span></span>
9. <span data-ttu-id="8383a-135">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="8383a-135">In the Description field, type a value.</span></span>
10. <span data-ttu-id="8383a-136">Í reitnum staða niðurstöðu, veljið ‚Stóðst'.</span><span class="sxs-lookup"><span data-stu-id="8383a-136">In the Outcome status field, select 'Pass'.</span></span>
11. <span data-ttu-id="8383a-137">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="8383a-137">Click Save.</span></span>
12. <span data-ttu-id="8383a-138">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="8383a-138">Click New.</span></span>
13. <span data-ttu-id="8383a-139">Í reitinn niðurstöðu skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8383a-139">In the Outcome field, type a value.</span></span>
14. <span data-ttu-id="8383a-140">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="8383a-140">In the Description field, type a value.</span></span>
15. <span data-ttu-id="8383a-141">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="8383a-141">Click Save.</span></span>
16. <span data-ttu-id="8383a-142">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8383a-142">Close the page.</span></span>
17. <span data-ttu-id="8383a-143">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8383a-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="8383a-144">Uppsetning vörusýna</span><span class="sxs-lookup"><span data-stu-id="8383a-144">Set up item sampling</span></span>
1. <span data-ttu-id="8383a-145">Fara í Birgðastjórnun > Uppsetning > gæðaeftirlit >  vörusýnishorn</span><span class="sxs-lookup"><span data-stu-id="8383a-145">Go to Inventory management > Setup > Quality control > Item sampling.</span></span>
2. <span data-ttu-id="8383a-146">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="8383a-146">Click New.</span></span>
3. <span data-ttu-id="8383a-147">Færa inn gildi í svæðið vörusýnishorn.</span><span class="sxs-lookup"><span data-stu-id="8383a-147">In the Item sampling field, type a value.</span></span>
4. <span data-ttu-id="8383a-148">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="8383a-148">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8383a-149">Í reitinn Gildi skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="8383a-149">In the Value field, enter a number.</span></span>
    * <span data-ttu-id="8383a-150">Gildið á við um tilgreint magn sem er valin í aðliggjandi svæði.</span><span class="sxs-lookup"><span data-stu-id="8383a-150">This value relates to the Quantity specification that’s selected in the adjacent field.</span></span>  
6. <span data-ttu-id="8383a-151">Stækka eða fella saman hlutann ferli.</span><span class="sxs-lookup"><span data-stu-id="8383a-151">Expand or collapse the Process section.</span></span>
7. <span data-ttu-id="8383a-152">Veljið eða hreinsið gátreitinn  Fullt lokun.</span><span class="sxs-lookup"><span data-stu-id="8383a-152">Select or clear the Full blocking check box.</span></span>
    * <span data-ttu-id="8383a-153">Ef þessi valkostur er valinn er heil lota eða pöntunarlínumagn læst ef prófun mistókst.</span><span class="sxs-lookup"><span data-stu-id="8383a-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="8383a-154">Ef þú velur hana ekki, eru aðeins vörur í gæðapöntuninni læstar.</span><span class="sxs-lookup"><span data-stu-id="8383a-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="8383a-155">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="8383a-155">Click Save.</span></span>
9. <span data-ttu-id="8383a-156">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8383a-156">Close the page.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="8383a-157">Stofna gæðaflokk</span><span class="sxs-lookup"><span data-stu-id="8383a-157">Create a quality group</span></span>
1. <span data-ttu-id="8383a-158">Fara í Birgðastjórnun > Uppsetning > gæðaeftirlit > gæðaflokkar</span><span class="sxs-lookup"><span data-stu-id="8383a-158">Go to Inventory management > Setup > Quality control > Quality groups.</span></span>
2. <span data-ttu-id="8383a-159">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="8383a-159">Click New.</span></span>
3. <span data-ttu-id="8383a-160">Færa inn gildi í svæðinu gæðaflokkur.</span><span class="sxs-lookup"><span data-stu-id="8383a-160">In the Quality group field, type a value.</span></span>
    * <span data-ttu-id="8383a-161">Notkun lýsandi heiti sem auðkennir sem hvers konar vörum flokki inniheldur (Þín úrtaksskilyrði).</span><span class="sxs-lookup"><span data-stu-id="8383a-161">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="8383a-162">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="8383a-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8383a-163">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="8383a-163">Click Save.</span></span>
6. <span data-ttu-id="8383a-164">Smellið á Bæta við vörum.</span><span class="sxs-lookup"><span data-stu-id="8383a-164">Click Add items.</span></span>
7. <span data-ttu-id="8383a-165">Velurðu línu vörunúmers.</span><span class="sxs-lookup"><span data-stu-id="8383a-165">Select the Item number row</span></span>
    * <span data-ttu-id="8383a-166">Í þessu dæmi skal sía keyrð byggt á vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="8383a-166">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="8383a-167">Í reitinn Skilyrði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="8383a-167">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="8383a-168">Ritið til dæmis T \* til að sía vörunúmer sem byrja T.</span><span class="sxs-lookup"><span data-stu-id="8383a-168">For example, type T\* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="8383a-169">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8383a-169">Click OK.</span></span>
10. <span data-ttu-id="8383a-170">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8383a-170">Click OK.</span></span>
11. <span data-ttu-id="8383a-171">Smellt er á Gæðaflokkar vöru</span><span class="sxs-lookup"><span data-stu-id="8383a-171">Click Item quality groups.</span></span>
12. <span data-ttu-id="8383a-172">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8383a-172">Close the page.</span></span>
13. <span data-ttu-id="8383a-173">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8383a-173">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="8383a-174">Stofna prófunarflokk</span><span class="sxs-lookup"><span data-stu-id="8383a-174">Create a test group</span></span>
1. <span data-ttu-id="8383a-175">Fara í Birgðastjórnun > Uppsetning > gæðaeftirlit > prófunarflokkar</span><span class="sxs-lookup"><span data-stu-id="8383a-175">Go to Inventory management > Setup > Quality control > Test groups.</span></span>
2. <span data-ttu-id="8383a-176">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="8383a-176">Click New.</span></span>
3. <span data-ttu-id="8383a-177">Færa inn gildi í svæðinu prófunarflokkur.</span><span class="sxs-lookup"><span data-stu-id="8383a-177">In the Test group field, type a value.</span></span>
    * <span data-ttu-id="8383a-178">Gefðu prófunarflokksins heiti sem auðveldar að muna hvers konar prófanir verið er að keyra og hvaða gæðaflokk það ætti að vera tengd við.</span><span class="sxs-lookup"><span data-stu-id="8383a-178">Give the Test group a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="8383a-179">Til dæmis, það er til að nota með gæðaflokk sem velur vörur frá og með "T", hægt væri að kalla það "T vöru prófanir".</span><span class="sxs-lookup"><span data-stu-id="8383a-179">For example, it it’s to be used with a quality group that selects items starting with “T”, you could call it “T-item tests”.</span></span>  
4. <span data-ttu-id="8383a-180">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="8383a-180">In the Description field, type a value.</span></span>
5. <span data-ttu-id="8383a-181">Í svæðinu vörusýni, veljið línu vörusýnis sem var stofnuð áður.</span><span class="sxs-lookup"><span data-stu-id="8383a-181">In the Item sampling field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="8383a-182">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="8383a-182">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="8383a-183">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="8383a-183">Click Add.</span></span>
8. <span data-ttu-id="8383a-184">Í reitinn raðnúmer skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="8383a-184">In the Sequence number field, enter a number.</span></span>
9. <span data-ttu-id="8383a-185">Veljið próf sem þú stofnaðir áður í svæðinu Prófun.</span><span class="sxs-lookup"><span data-stu-id="8383a-185">In the Test field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="8383a-186">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="8383a-186">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="8383a-187">Smelltu á flipann Prufa.</span><span class="sxs-lookup"><span data-stu-id="8383a-187">Click the Test tab.</span></span>
12. <span data-ttu-id="8383a-188">Veljið í svæðinu Breyta prófunarbreytu sem var stofnuð áður </span><span class="sxs-lookup"><span data-stu-id="8383a-188">In the Variable field, select the test variable that you created before</span></span>
13. <span data-ttu-id="8383a-189">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="8383a-189">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="8383a-190">Í reitnum sjálfgefin niðurstaða skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="8383a-190">In the Default outcome field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="8383a-191">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="8383a-191">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="8383a-192">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="8383a-192">Click Save.</span></span>
17. <span data-ttu-id="8383a-193">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8383a-193">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="8383a-194">Skilgreina hvenær gæðapantanir eru stofnaðar</span><span class="sxs-lookup"><span data-stu-id="8383a-194">Define when quality orders will be created</span></span>
1. <span data-ttu-id="8383a-195">Fara í Birgðastjórnun > Uppsetning > gæðaeftirlit >  gæðatengingar</span><span class="sxs-lookup"><span data-stu-id="8383a-195">Go to Inventory management > Setup > Quality control > Quality associations.</span></span>
2. <span data-ttu-id="8383a-196">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="8383a-196">Click New.</span></span>
3. <span data-ttu-id="8383a-197">Veljið valkost í svæðinu Gerð tilvísunar.</span><span class="sxs-lookup"><span data-stu-id="8383a-197">In the Reference type field, select an option.</span></span>
4. <span data-ttu-id="8383a-198">Í reitnum vörukóði er valið 'flokkur'.</span><span class="sxs-lookup"><span data-stu-id="8383a-198">In the Item code field, select 'Group'.</span></span>
    * <span data-ttu-id="8383a-199">Í þessu dæmi er velja "Flokkur" og nota gæðaflokkinn sem var stofnuð áður.</span><span class="sxs-lookup"><span data-stu-id="8383a-199">In this example, we’ll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="8383a-200">Þú gæti einnig stillt þetta á "Töflu" til að tilgreina vörur handvirkt eða velja "Allt" til að bæta öllum vörum við gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="8383a-200">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="8383a-201">Í svæðinu vara, veljið gæðaflokk sem var stofnuð áður.</span><span class="sxs-lookup"><span data-stu-id="8383a-201">In the Item field, select the quality group that you created before.</span></span>
    * <span data-ttu-id="8383a-202">Tiltækir valkostir í svæðinu Vöru eru háð stillingu í svæðinu fyrir vörukóði.</span><span class="sxs-lookup"><span data-stu-id="8383a-202">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="8383a-203">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="8383a-203">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="8383a-204">Stækka eða fella saman hlutann ferli.</span><span class="sxs-lookup"><span data-stu-id="8383a-204">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="8383a-205">Veljið valkost í svæðinu gerð tilviks.</span><span class="sxs-lookup"><span data-stu-id="8383a-205">In the Event type field, select an option.</span></span>
    * <span data-ttu-id="8383a-206">Það er þá atburðurinn sem ræsir prófið.</span><span class="sxs-lookup"><span data-stu-id="8383a-206">This is the event that triggers the test.</span></span> <span data-ttu-id="8383a-207">Tiltæk valkostir hér velta á hvaða vinnslu var valið í svæðinu gerð Tilvísunar.</span><span class="sxs-lookup"><span data-stu-id="8383a-207">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="8383a-208">Í reitnum Framkvæmd skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="8383a-208">In the Execution field, select an option.</span></span>
10. <span data-ttu-id="8383a-209">Stækka eða fella saman hlutann ferli gæðapöntunar.</span><span class="sxs-lookup"><span data-stu-id="8383a-209">Expand or collapse the Quality order process section.</span></span>
11. <span data-ttu-id="8383a-210">Í reitnum tilvikslokun skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="8383a-210">In the Event blocking field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8383a-211">Þetta svæði sýnir lista yfir ferli sem hægt er að læsa ef gæðapöntunin er enn opin.</span><span class="sxs-lookup"><span data-stu-id="8383a-211">This field shows the list of processes that it’s possible to block if the quality order is still open.</span></span> <span data-ttu-id="8383a-212">Valkostir fara eftir því hvað var valið í svæðinu gerð Tilviks.</span><span class="sxs-lookup"><span data-stu-id="8383a-212">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="8383a-213">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="8383a-213">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="8383a-214">Þetta mun velta á fyrri gildum sem valin voru.</span><span class="sxs-lookup"><span data-stu-id="8383a-214">This will be depending on the previous selected values.</span></span> <span data-ttu-id="8383a-215">Veljið ef eftirfarandi ferlum verður að læsa meðan með verið er að tengja opnar gæðapantanir við upprunaskjalslínu.</span><span class="sxs-lookup"><span data-stu-id="8383a-215">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="8383a-216">Víkka eða draga saman  hlutann lýsing</span><span class="sxs-lookup"><span data-stu-id="8383a-216">Expand or collapse the Specifications section.</span></span>
14. <span data-ttu-id="8383a-217">í svæðinu prófunarflokkur Veljið prófunarflokk sem var stofnuð áður </span><span class="sxs-lookup"><span data-stu-id="8383a-217">In the Test group field, select the test group that you created before.</span></span>
15. <span data-ttu-id="8383a-218">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="8383a-218">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="8383a-219">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="8383a-219">Click Save.</span></span>
17. <span data-ttu-id="8383a-220">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8383a-220">Close the page.</span></span>

