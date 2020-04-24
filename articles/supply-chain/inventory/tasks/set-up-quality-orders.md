---
title: Setja upp gæðapantanir
description: Þessi verklýsing sýnir hvernig á að virkja gæðastjórnunarferli þar sem innhreyfingar birgða verða skoðaðar strax eftir komuskráningu.
author: perlynne
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 679448255bd85aafb07270f4858d4b83d2fe643b
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204034"
---
# <a name="set-up-quality-orders"></a><span data-ttu-id="863c0-103">Setja upp gæðapantanir</span><span class="sxs-lookup"><span data-stu-id="863c0-103">Set up quality orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="863c0-104">Þessi verklýsing sýnir hvernig á að virkja gæðastjórnunarferli þar sem innhreyfingar birgða verða skoðaðar strax eftir komuskráningu.</span><span class="sxs-lookup"><span data-stu-id="863c0-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="863c0-105">Ferlið er yfirleitt framkvæma með gæðastjóra.</span><span class="sxs-lookup"><span data-stu-id="863c0-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="863c0-106">Ferlið inniheldur stofnun gæðaflokks til að skilgreina vörurnar sem á að nota sem sýni, og prófunarflokk til að flokka prófanir sem á að framkvæma á vörum í gæðaflokkinn.</span><span class="sxs-lookup"><span data-stu-id="863c0-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="863c0-107">Hægt er að keyra þessari leiðbeiningar í sýnigögnum USMF-fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="863c0-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="863c0-108">Gæðastjórnun virkjuð</span><span class="sxs-lookup"><span data-stu-id="863c0-108">Enable quality management</span></span>
1. <span data-ttu-id="863c0-109">Farðu í **Skoðunarrúðu > Kerifseiningar > Birgðastýring > Uppsetning > Birgðir og færibreytur vöruhúsakerfis**.</span><span class="sxs-lookup"><span data-stu-id="863c0-109">Go to **Navigation pane > Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="863c0-110">Smelltu á flipann **Gæðastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="863c0-110">Click the **Quality management** tab.</span></span>
3. <span data-ttu-id="863c0-111">Setja skal **Nota gæðastjórnun** valkosturinn á Já.</span><span class="sxs-lookup"><span data-stu-id="863c0-111">Set the **Use quality management option** to 'Yes'.</span></span>
4. <span data-ttu-id="863c0-112">Smelltu á **Uppsetningu Skýrslu**.</span><span class="sxs-lookup"><span data-stu-id="863c0-112">Click **Report setup**.</span></span> <span data-ttu-id="863c0-113">Á USMF, er skýrsluuppsetning fyrir gæðastjórnun er þegar skilgreind.</span><span class="sxs-lookup"><span data-stu-id="863c0-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="863c0-114">Ef þetta var ekki gert myndirðu bæta við nýjum línum hér fyrir mismunandi skýrslugerðir, og veldu gerð skjals sem á að nota fyrir hverja skýrslu.</span><span class="sxs-lookup"><span data-stu-id="863c0-114">If this wasn't done, you'd add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="863c0-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="863c0-115">Close the page.</span></span>
6. <span data-ttu-id="863c0-116">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="863c0-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="863c0-117">Stofna próf</span><span class="sxs-lookup"><span data-stu-id="863c0-117">Create a test</span></span>
1. <span data-ttu-id="863c0-118">Farðu í **Birgðastjórnun > Uppsetning > gæðaeftirlit > prófanir**.</span><span class="sxs-lookup"><span data-stu-id="863c0-118">Go to **Inventory management > Setup > Quality control > Tests**.</span></span>
2. <span data-ttu-id="863c0-119">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="863c0-119">Click **New**.</span></span>
3. <span data-ttu-id="863c0-120">Í reitnum **Prófun** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="863c0-120">In the **Test** field, type a value.</span></span>
4. <span data-ttu-id="863c0-121">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="863c0-121">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="863c0-122">Í reitnum **Tegund** skal velja „valkostur“.</span><span class="sxs-lookup"><span data-stu-id="863c0-122">In the **Type** field, select 'Option'.</span></span> <span data-ttu-id="863c0-123">Í þessu dæmi veljum við valkosturinn sem munu gera það mögulegt að úthluta niðurstöðurnar prófana byggt á fyrirframskilgreindu gildi.</span><span class="sxs-lookup"><span data-stu-id="863c0-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="863c0-124">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="863c0-124">Click **Save**.</span></span>
7. <span data-ttu-id="863c0-125">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="863c0-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="863c0-126">Stofna prófunarbreytur til að skilgreina hvernig prófunarniðurstöður eru skráðar</span><span class="sxs-lookup"><span data-stu-id="863c0-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="863c0-127">Fara í **Birgðastjórnun > Uppsetning > gæðaeftirlit > prófunarbreytur**.</span><span class="sxs-lookup"><span data-stu-id="863c0-127">Go to **Inventory management > Setup > Quality control > Test variables**.</span></span>
2. <span data-ttu-id="863c0-128">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="863c0-128">Click **New**.</span></span>
3. <span data-ttu-id="863c0-129">Í reitinn **Breyta** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="863c0-129">In the **Variable** field, type a value.</span></span>
4. <span data-ttu-id="863c0-130">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="863c0-130">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="863c0-131">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="863c0-131">Click **Save**.</span></span>
6. <span data-ttu-id="863c0-132">Smelltu á **Niðurstöður.**</span><span class="sxs-lookup"><span data-stu-id="863c0-132">Click **Outcomes**.</span></span>
7. <span data-ttu-id="863c0-133">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="863c0-133">Click **New**.</span></span>
8. <span data-ttu-id="863c0-134">Í reitinn **Niðurstöðu** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="863c0-134">In the **Outcome** field, type a value.</span></span>
9. <span data-ttu-id="863c0-135">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="863c0-135">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="863c0-136">Í reitnum **Staða niðurstöðu** veljið ‚Stóðst'.</span><span class="sxs-lookup"><span data-stu-id="863c0-136">In the **Outcome status** field, select 'Pass'.</span></span>
11. <span data-ttu-id="863c0-137">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="863c0-137">Click **Save**.</span></span>
12. <span data-ttu-id="863c0-138">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="863c0-138">Click **New**.</span></span>
13. <span data-ttu-id="863c0-139">Í reitinn **Niðurstöðu** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="863c0-139">In the **Outcome** field, type a value.</span></span>
14. <span data-ttu-id="863c0-140">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="863c0-140">In the **Description** field, type a value.</span></span>
15. <span data-ttu-id="863c0-141">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="863c0-141">Click **Save**.</span></span>
16. <span data-ttu-id="863c0-142">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="863c0-142">Close the page.</span></span>
17. <span data-ttu-id="863c0-143">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="863c0-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="863c0-144">Uppsetning vörusýna</span><span class="sxs-lookup"><span data-stu-id="863c0-144">Set up item sampling</span></span>
1. <span data-ttu-id="863c0-145">Fara í **Birgðastjórnun > Uppsetning > gæðaeftirlit > vörusýnishorn**.</span><span class="sxs-lookup"><span data-stu-id="863c0-145">Go to **Inventory management > Setup > Quality control > Item sampling**.</span></span>
2. <span data-ttu-id="863c0-146">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="863c0-146">Click **New**.</span></span>
3. <span data-ttu-id="863c0-147">Í reitnum **vörusýnishorn** færirðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="863c0-147">In the **Item sampling** field, type a value.</span></span>
4. <span data-ttu-id="863c0-148">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="863c0-148">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="863c0-149">Í reitnum **Gildi** skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="863c0-149">In the **Value** field, enter a number.</span></span> <span data-ttu-id="863c0-150">Gildið á við um tilgreint magn sem er valið í aðliggjandi reit.</span><span class="sxs-lookup"><span data-stu-id="863c0-150">This value relates to the Quantity specification that's selected in the adjacent field.</span></span>  
6. <span data-ttu-id="863c0-151">Stækka eða fella saman hlutann **ferli**.</span><span class="sxs-lookup"><span data-stu-id="863c0-151">Expand or collapse the **Process** section.</span></span>
7. <span data-ttu-id="863c0-152">Veljið eða hreinsið gátreitinn **Full lokun**.</span><span class="sxs-lookup"><span data-stu-id="863c0-152">Select or clear the **Full blocking** check box.</span></span> <span data-ttu-id="863c0-153">Ef þessi valkostur er valinn er heil lota eða pöntunarlínumagn læst ef prófun mistókst.</span><span class="sxs-lookup"><span data-stu-id="863c0-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="863c0-154">Ef þú velur hana ekki, eru aðeins vörur í gæðapöntuninni læstar.</span><span class="sxs-lookup"><span data-stu-id="863c0-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="863c0-155">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="863c0-155">Click **Save**.</span></span>
9. <span data-ttu-id="863c0-156">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="863c0-156">Close the page.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="863c0-157">Stofna gæðaflokk</span><span class="sxs-lookup"><span data-stu-id="863c0-157">Create a quality group</span></span>
1. <span data-ttu-id="863c0-158">Fara í **Birgðastjórnun > Uppsetning > gæðaeftirlit > gæðaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="863c0-158">Go to **Inventory management > Setup > Quality control > Quality groups**.</span></span>
2. <span data-ttu-id="863c0-159">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="863c0-159">Click **New**.</span></span>
3. <span data-ttu-id="863c0-160">Færa inn gildi í svæðinu **gæðaflokkur**.</span><span class="sxs-lookup"><span data-stu-id="863c0-160">In the **Quality group** field, type a value.</span></span> <span data-ttu-id="863c0-161">Notkun lýsandi heiti sem auðkennir sem hvers konar vörum flokki inniheldur (Þín úrtaksskilyrði).</span><span class="sxs-lookup"><span data-stu-id="863c0-161">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="863c0-162">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="863c0-162">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="863c0-163">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="863c0-163">Click **Save**.</span></span>
6. <span data-ttu-id="863c0-164">Smellið á **Bæta við vörum**.</span><span class="sxs-lookup"><span data-stu-id="863c0-164">Click **Add items**.</span></span>
7. <span data-ttu-id="863c0-165">Velurðu **línu vörunúmers**.</span><span class="sxs-lookup"><span data-stu-id="863c0-165">Select the **Item number** row.</span></span> <span data-ttu-id="863c0-166">Í þessu dæmi skal sía keyrð byggt á vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="863c0-166">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="863c0-167">Í reitnum **Skilyrði** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="863c0-167">In the **Criteria** field, type a value.</span></span> <span data-ttu-id="863c0-168">Ritið til dæmis T \* til að sía vörunúmer sem byrja T.</span><span class="sxs-lookup"><span data-stu-id="863c0-168">For example, type T\* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="863c0-169">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="863c0-169">Click **OK**.</span></span>
10. <span data-ttu-id="863c0-170">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="863c0-170">Click **OK**.</span></span>
11. <span data-ttu-id="863c0-171">Smelltu á **Gæðaflokkar vöru**.</span><span class="sxs-lookup"><span data-stu-id="863c0-171">Click **Item quality groups**.</span></span>
12. <span data-ttu-id="863c0-172">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="863c0-172">Close the page.</span></span>
13. <span data-ttu-id="863c0-173">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="863c0-173">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="863c0-174">Stofna prófunarflokk</span><span class="sxs-lookup"><span data-stu-id="863c0-174">Create a test group</span></span>
1. <span data-ttu-id="863c0-175">Farðu í **Birgðastjórnun > Uppsetning > gæðaeftirlit > prófunarflokkar**.</span><span class="sxs-lookup"><span data-stu-id="863c0-175">Go to **Inventory management > Setup > Quality control > Test groups**.</span></span>
2. <span data-ttu-id="863c0-176">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="863c0-176">Click **New**.</span></span>
3. <span data-ttu-id="863c0-177">Færa inn gildi í svæðinu **prófunarflokkur**.</span><span class="sxs-lookup"><span data-stu-id="863c0-177">In the **Test group** field, type a value.</span></span> <span data-ttu-id="863c0-178">Gefðu **prófunarflokksins** heiti sem auðveldar að muna hvers konar prófanir verið er að keyra og hvaða gæðaflokk það ætti að vera tengd við.</span><span class="sxs-lookup"><span data-stu-id="863c0-178">Give the **Test group** a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="863c0-179">Til dæmis, það er til að nota með gæðaflokk sem velur vörur frá og með „T”, hægt væri að kalla það „T vöru prófanir”.</span><span class="sxs-lookup"><span data-stu-id="863c0-179">For example, it it's to be used with a quality group that selects items starting with "T", you could call it "T-item tests".</span></span>  
4. <span data-ttu-id="863c0-180">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="863c0-180">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="863c0-181">Í svæðinu **vörusýni**, veljið línu vörusýnis sem var stofnuð áður.</span><span class="sxs-lookup"><span data-stu-id="863c0-181">In the **Item sampling** field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="863c0-182">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="863c0-182">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="863c0-183">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="863c0-183">Click **Add**.</span></span>
8. <span data-ttu-id="863c0-184">Í reitinn **Raðnúmer** skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="863c0-184">In the **Sequence number** field, enter a number.</span></span>
9. <span data-ttu-id="863c0-185">Í reitnum **Prófun** skal velja próf sem áður var stofnað.</span><span class="sxs-lookup"><span data-stu-id="863c0-185">In the **Test** field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="863c0-186">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="863c0-186">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="863c0-187">Smelltu á flipann **Prufa**.</span><span class="sxs-lookup"><span data-stu-id="863c0-187">Click the **Test** tab.</span></span>
12. <span data-ttu-id="863c0-188">Í reitnum **Breyta** skal velja prófunarbreytu sem stofnuð var áður</span><span class="sxs-lookup"><span data-stu-id="863c0-188">In the **Variable** field, select the test variable that you created before</span></span>
13. <span data-ttu-id="863c0-189">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="863c0-189">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="863c0-190">Í reitnum **sjálfgefin niðurstaða** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="863c0-190">In the **Default outcome** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="863c0-191">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="863c0-191">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="863c0-192">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="863c0-192">Click **Save**.</span></span>
17. <span data-ttu-id="863c0-193">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="863c0-193">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="863c0-194">Skilgreina hvenær gæðapantanir eru stofnaðar</span><span class="sxs-lookup"><span data-stu-id="863c0-194">Define when quality orders will be created</span></span>
1. <span data-ttu-id="863c0-195">Fara í **Birgðastjórnun > Uppsetning > gæðaeftirlit > gæðatengingar**.</span><span class="sxs-lookup"><span data-stu-id="863c0-195">Go to **Inventory management > Setup > Quality control > Quality associations**.</span></span>
2. <span data-ttu-id="863c0-196">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="863c0-196">Click **New**.</span></span>
3. <span data-ttu-id="863c0-197">Veljið valkost í svæðinu **Gerð tilvísunar**.</span><span class="sxs-lookup"><span data-stu-id="863c0-197">In the **Reference type** field, select an option.</span></span>
4. <span data-ttu-id="863c0-198">Í reitnum **vörukóði** er valið 'flokkur'.</span><span class="sxs-lookup"><span data-stu-id="863c0-198">In the **Item code** field, select 'Group'.</span></span> <span data-ttu-id="863c0-199">Í þessu dæmi veljum við „Flokkur” og notum gæðaflokkinn sem var stofnaður áður.</span><span class="sxs-lookup"><span data-stu-id="863c0-199">In this example, we'll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="863c0-200">Þú gæti einnig stillt þetta á "Töflu" til að tilgreina vörur handvirkt eða velja "Allt" til að bæta öllum vörum við gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="863c0-200">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="863c0-201">Í svæðinu **vara**, veljið gæðaflokk sem var stofnuð áður.</span><span class="sxs-lookup"><span data-stu-id="863c0-201">In the **Item** field, select the quality group that you created before.</span></span> <span data-ttu-id="863c0-202">Tiltækir valkostir í svæðinu Vöru eru háð stillingu í svæðinu fyrir vörukóði.</span><span class="sxs-lookup"><span data-stu-id="863c0-202">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="863c0-203">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="863c0-203">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="863c0-204">Stækka eða fella saman hlutann ferli.</span><span class="sxs-lookup"><span data-stu-id="863c0-204">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="863c0-205">Í reitnum **Gerð tilviks** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="863c0-205">In the **Event type** field, select an option.</span></span> <span data-ttu-id="863c0-206">Það er þá atburðurinn sem ræsir prófið.</span><span class="sxs-lookup"><span data-stu-id="863c0-206">This is the event that triggers the test.</span></span> <span data-ttu-id="863c0-207">Tiltæk valkostir hér velta á hvaða vinnslu var valið í svæðinu gerð Tilvísunar.</span><span class="sxs-lookup"><span data-stu-id="863c0-207">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="863c0-208">Í reitnum **Framkvæmd** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="863c0-208">In the **Execution** field, select an option.</span></span>
10. <span data-ttu-id="863c0-209">Stækka eða fella saman hlutann **ferli gæðapöntunar**.</span><span class="sxs-lookup"><span data-stu-id="863c0-209">Expand or collapse the **Quality order process** section.</span></span>
11. <span data-ttu-id="863c0-210">Í reitnum **tilvikslokun** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="863c0-210">In the **Event blocking** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="863c0-211">Þetta svæði sýnir lista yfir ferli sem hægt er að læsa ef gæðapöntunin er enn opin.</span><span class="sxs-lookup"><span data-stu-id="863c0-211">This field shows the list of processes that it's possible to block if the quality order is still open.</span></span> <span data-ttu-id="863c0-212">Valkostir fara eftir því hvað var valið í svæðinu gerð Tilviks.</span><span class="sxs-lookup"><span data-stu-id="863c0-212">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="863c0-213">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="863c0-213">In the list, click the link in the selected row.</span></span> <span data-ttu-id="863c0-214">Þetta mun velta á fyrri gildum sem valin voru.</span><span class="sxs-lookup"><span data-stu-id="863c0-214">This will be depending on the previous selected values.</span></span> <span data-ttu-id="863c0-215">Veljið ef eftirfarandi ferlum verður að læsa meðan með verið er að tengja opnar gæðapantanir við upprunaskjalslínu.</span><span class="sxs-lookup"><span data-stu-id="863c0-215">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="863c0-216">Víkka eða draga saman hlutann **lýsing**.</span><span class="sxs-lookup"><span data-stu-id="863c0-216">Expand or collapse the **Specifications** section.</span></span>
14. <span data-ttu-id="863c0-217">í svæðinu **prófunarflokkur** Veljið prófunarflokk sem var stofnuð áður.</span><span class="sxs-lookup"><span data-stu-id="863c0-217">In the **Test group** field, select the test group that you created before.</span></span>
15. <span data-ttu-id="863c0-218">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="863c0-218">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="863c0-219">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="863c0-219">Click **Save**.</span></span>
17. <span data-ttu-id="863c0-220">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="863c0-220">Close the page.</span></span>

