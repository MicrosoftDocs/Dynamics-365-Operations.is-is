---
title: Breyta líkani og vörpun til að búa til skjöl sem eru með forritsgögnum
description: Í þessu efni er útskýrt hvernig á að hanna skilgreiningar skýrslugerðar til að mynda rafrænt skjal og uppfæra forritsgögn. (Hluti 2 - Mynda skjöl).
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64bcf885fe2f5fca6b91589171b5e539eff2c3e5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567093"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="e7b00-104">Breyta líkani og vörpun til að búa til skjöl sem eru með forritsgögnum</span><span class="sxs-lookup"><span data-stu-id="e7b00-104">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e7b00-105">Til að ljúka skrefunum í þessu ferli verður fyrst að ljúka við ferlið „ER Búa til skjöl með gagnauppfærslum fyrir forrit (Hluti 2: Búa til skjöl)“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-105">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="e7b00-106">Skrefin í þessu ferli sýna hvernig skal hanna Rafræna skýrslugerð (ER) grunnstillingar þannig að þær búi til rafræn skjöl og uppfæri gögn fyrir forrit.</span><span class="sxs-lookup"><span data-stu-id="e7b00-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="e7b00-107">Í þessu ferli muntu breyta Rafræna skýrslugerð (ER) grunnstillingar þannig að hægt sé að byrja að nota þær til að búa til rafræn skjöl og uppfæra gögn fyrir forrit.</span><span class="sxs-lookup"><span data-stu-id="e7b00-107">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="e7b00-108">Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="e7b00-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="e7b00-109">Skrefin er hægt að klára með því að nota DEMF gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="e7b00-109">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="e7b00-110">Breyta gagnalíkani</span><span class="sxs-lookup"><span data-stu-id="e7b00-110">Modify data model</span></span>
1. <span data-ttu-id="e7b00-111">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="e7b00-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="e7b00-112">Í trénu skal velja „Intrastat (líkan)“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-112">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="e7b00-113">Þú munt útvíkka það hvernig þú notar gagnalíkanið.</span><span class="sxs-lookup"><span data-stu-id="e7b00-113">You will extend how you use the data model.</span></span> <span data-ttu-id="e7b00-114">Fyrir utan að nota það sem gagnaveitu til að búa til Intrastat skýrsluna, verður gagnalíkanið notað til að safna upplýsingum um Instrastat skýrslugerðarferlið.</span><span class="sxs-lookup"><span data-stu-id="e7b00-114">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="e7b00-115">Upplýsingarnar verða síðan notaðar til að uppfæra gögn fyrir forrit.</span><span class="sxs-lookup"><span data-stu-id="e7b00-115">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="e7b00-116">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="e7b00-116">Click Designer.</span></span>
4. <span data-ttu-id="e7b00-117">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="e7b00-117">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="e7b00-118">Í svæði Nýr hnútur sem, slá inn „Líkanshnútur“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-118">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="e7b00-119">Í reitnum Heiti skal færa inn „Fyrir gagnauppfærslu fyrir forrit“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-119">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="e7b00-120">Fyrir uppfærsla gagna hugbúnaðarins</span><span class="sxs-lookup"><span data-stu-id="e7b00-120">For application data update</span></span>  
7. <span data-ttu-id="e7b00-121">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="e7b00-121">Click Add.</span></span>
8. <span data-ttu-id="e7b00-122">Í trénu skal velja „Fyrir gagnauppfærslu fyrir forrit“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-122">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="e7b00-123">Þessu nýja rótaratriði er bætt við til að tilgreina gagnaflæði fyrir gögn á hreyfingu frá Intrastat skýrslunni (notuð sem gagnaveitu) til tafla forrits (áfangastaður uppfærslu).</span><span class="sxs-lookup"><span data-stu-id="e7b00-123">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="e7b00-124">Athugið að mismunandi rótaratriði verður að nota til að sækja gögn sem eru bókuð í skjal á útleið og til að sækja gögn frá skjalinu sem er notað til að uppfæra gögn fyrir forrit.</span><span class="sxs-lookup"><span data-stu-id="e7b00-124">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="e7b00-125">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="e7b00-125">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="e7b00-126">Í svæðið Heiti, færðu inn „Safn haus“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-126">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="e7b00-127">Safnshaus</span><span class="sxs-lookup"><span data-stu-id="e7b00-127">Archive header</span></span>  
11. <span data-ttu-id="e7b00-128">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="e7b00-128">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="e7b00-129">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="e7b00-129">Click Add.</span></span>
    * <span data-ttu-id="e7b00-130">Þú munt stofna skrá fyrir hverja Intrastat skýrslu sem er búin til, og þess vegna þarftu að búa til nýtt atriði fyrir það.</span><span class="sxs-lookup"><span data-stu-id="e7b00-130">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="e7b00-131">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="e7b00-131">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="e7b00-132">Í svæðið Heiti, færðu inn 'skrárnafn'.</span><span class="sxs-lookup"><span data-stu-id="e7b00-132">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="e7b00-133">Skrárnafn</span><span class="sxs-lookup"><span data-stu-id="e7b00-133">File name</span></span>  
15. <span data-ttu-id="e7b00-134">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="e7b00-134">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="e7b00-135">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="e7b00-135">Click Add.</span></span>
17. <span data-ttu-id="e7b00-136">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="e7b00-136">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="e7b00-137">Í svæðið Heiti, færðu inn “Númer lína“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-137">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="e7b00-138">Línufjöldi</span><span class="sxs-lookup"><span data-stu-id="e7b00-138">Number of lines</span></span>  
19. <span data-ttu-id="e7b00-139">Velja „Heiltala“ í svæðinu gerð Vöru.</span><span class="sxs-lookup"><span data-stu-id="e7b00-139">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="e7b00-140">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="e7b00-140">Click Add.</span></span>
    * <span data-ttu-id="e7b00-141">Bættu þessu atriði við til að tákna númer Intrastat færslnanna sem eru skráðar á meðan núverandi skráningarferli stendur.</span><span class="sxs-lookup"><span data-stu-id="e7b00-141">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="e7b00-142">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="e7b00-142">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="e7b00-143">Í svæðið Heiti, færðu inn „Safn línur“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-143">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="e7b00-144">Safnslínur</span><span class="sxs-lookup"><span data-stu-id="e7b00-144">Archive lines</span></span>  
23. <span data-ttu-id="e7b00-145">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="e7b00-145">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="e7b00-146">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="e7b00-146">Click Add.</span></span>
    * <span data-ttu-id="e7b00-147">Bættu þessu atriði við til að tákna lista Intrastat færslnanna sem eru skráðar á meðan núverandi skráningarferli stendur.</span><span class="sxs-lookup"><span data-stu-id="e7b00-147">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="e7b00-148">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="e7b00-148">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="e7b00-149">Í reitnum Heiti skal færa inn ‚Upphæð'.</span><span class="sxs-lookup"><span data-stu-id="e7b00-149">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="e7b00-150">Upphæð</span><span class="sxs-lookup"><span data-stu-id="e7b00-150">Amount</span></span>  
27. <span data-ttu-id="e7b00-151">Veljið 'Raunveruleg' í svæðinu gerð vöru.</span><span class="sxs-lookup"><span data-stu-id="e7b00-151">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="e7b00-152">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="e7b00-152">Click Add.</span></span>
29. <span data-ttu-id="e7b00-153">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="e7b00-153">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="e7b00-154">Í svæðið Heiti, færðu inn „Grunnvara skrá kenni“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-154">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="e7b00-155">Vöru skrá kenni</span><span class="sxs-lookup"><span data-stu-id="e7b00-155">Commodity rec id</span></span>  
31. <span data-ttu-id="e7b00-156">Velja „Int64“ í svæðinu gerð Vöru.</span><span class="sxs-lookup"><span data-stu-id="e7b00-156">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="e7b00-157">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="e7b00-157">Click Add.</span></span>
33. <span data-ttu-id="e7b00-158">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="e7b00-158">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="e7b00-159">Í reitnum Heiti skal færa inn „Númer afurðar“</span><span class="sxs-lookup"><span data-stu-id="e7b00-159">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="e7b00-160">Vörunúmer</span><span class="sxs-lookup"><span data-stu-id="e7b00-160">Item number</span></span>  
35. <span data-ttu-id="e7b00-161">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="e7b00-161">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="e7b00-162">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="e7b00-162">Click Add.</span></span>
37. <span data-ttu-id="e7b00-163">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-163">Click Save.</span></span>
38. <span data-ttu-id="e7b00-164">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e7b00-164">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="e7b00-165">Breyta Vörpun líkans</span><span class="sxs-lookup"><span data-stu-id="e7b00-165">Modify model mapping</span></span>
1. <span data-ttu-id="e7b00-166">Í trénu skal víkka út „Intrastat (líkan)“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-166">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="e7b00-167">Í trénu skal velja „Intrastat (líkan)\Intrastat (vörpun)“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-167">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="e7b00-168">Breyta fyrirliggjandi vörpun líkans til að hefja notkun þess fyrir uppfærslu gagna fyrir forrit og til að skjala upplýsingar um Intrastat skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="e7b00-168">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="e7b00-169">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="e7b00-169">Click Designer.</span></span>
4. <span data-ttu-id="e7b00-170">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-170">Click New.</span></span>
5. <span data-ttu-id="e7b00-171">Í svæðið Heiti, færðu inn „Uppfæra safn“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-171">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="e7b00-172">Uppfæra safn</span><span class="sxs-lookup"><span data-stu-id="e7b00-172">Update archive</span></span>  
6. <span data-ttu-id="e7b00-173">Í reitnum Stefna skal velja „Til viðtökustaðar".</span><span class="sxs-lookup"><span data-stu-id="e7b00-173">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="e7b00-174">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-174">Click Save.</span></span>
    * <span data-ttu-id="e7b00-175">Þessu nýja rótaratriði er bætt við til að tilgreina gagnaflæði fyrir gögn á hreyfingu frá Intrastat skýrslunni (notuð sem gagnaveitu) til tafla forrits (áfangastaður uppfærslu).</span><span class="sxs-lookup"><span data-stu-id="e7b00-175">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="e7b00-176">Athugið að mismunandi rótaratriði líkans verður að nota til að sækja gögn frá forritinu fyrir skýrslugerðarferlið og síðan nota gögnin úr gagnalíkaninu fyrir uppfærslu hugbúnaðargagna.</span><span class="sxs-lookup"><span data-stu-id="e7b00-176">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="e7b00-177">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="e7b00-177">Click Designer.</span></span>
9. <span data-ttu-id="e7b00-178">Í trénu skal velja „Gagnalíkan\Gagnalíkan“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-178">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="e7b00-179">Bættu við þeirri gagnaveitu sem er krafist</span><span class="sxs-lookup"><span data-stu-id="e7b00-179">Add the required data source.</span></span> <span data-ttu-id="e7b00-180">Þetta er gagnalíkanið sem inniheldur upplýsingar um skráðar Intrastat færslur sem verða að vera skjalaðar.</span><span class="sxs-lookup"><span data-stu-id="e7b00-180">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="e7b00-181">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="e7b00-181">Click Add root.</span></span>
11. <span data-ttu-id="e7b00-182">Í reitnum Heiti skal færa inn „líkan“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-182">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="e7b00-183">líkan</span><span class="sxs-lookup"><span data-stu-id="e7b00-183">model</span></span>  
12. <span data-ttu-id="e7b00-184">Sláið inn eða veldu gildið „Fyrir gagnauppfærslu fyrir forrit“ í reitnum Skilgreining.</span><span class="sxs-lookup"><span data-stu-id="e7b00-184">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="e7b00-185">Fyrir uppfærsla gagna hugbúnaðarins</span><span class="sxs-lookup"><span data-stu-id="e7b00-185">For application data update</span></span>  
13. <span data-ttu-id="e7b00-186">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="e7b00-186">Click OK.</span></span>
14. <span data-ttu-id="e7b00-187">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="e7b00-187">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="e7b00-188">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="e7b00-188">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="e7b00-189">Í trénu skal velja „Líkan\Safn haus“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-189">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="e7b00-190">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="e7b00-190">Click Add.</span></span>
    * <span data-ttu-id="e7b00-191">Þar sem þú vilt tölusetja skráðar Intrastat færslur í skjölun, verður að bæta við viðeigandi gagnaveitu.</span><span class="sxs-lookup"><span data-stu-id="e7b00-191">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="e7b00-192">Í svæðið Heiti, færðu inn „Tölusettar línur“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-192">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="e7b00-193">Tölusettar línur</span><span class="sxs-lookup"><span data-stu-id="e7b00-193">Enumerated lines</span></span>  
19. <span data-ttu-id="e7b00-194">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="e7b00-194">Click Edit formula.</span></span>
20. <span data-ttu-id="e7b00-195">Í trénu skal velja „Listi\TÖLUSETJA“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-195">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="e7b00-196">Smelltu á Bæta við Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="e7b00-196">Click Add function.</span></span>
22. <span data-ttu-id="e7b00-197">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="e7b00-197">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="e7b00-198">Í trénu skal víkka út „Líkan\Safn haus“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-198">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="e7b00-199">Í trénu skal víkka út „Líkan\Safn haus\Safn línur“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-199">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="e7b00-200">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="e7b00-200">Click Add data source.</span></span>
26. <span data-ttu-id="e7b00-201">Í svæði Formúla slá inn „SKEYTA SAMAN(líkan.„Safn haus“ „Safn línur“)“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-201">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="e7b00-202">TÖLUSETJA(líkan.„Safn haus“ „Safn línur“)</span><span class="sxs-lookup"><span data-stu-id="e7b00-202">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="e7b00-203">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-203">Click Save.</span></span>
28. <span data-ttu-id="e7b00-204">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e7b00-204">Close the page.</span></span>
29. <span data-ttu-id="e7b00-205">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-205">Click OK.</span></span>
30. <span data-ttu-id="e7b00-206">Smelltu á Bæta við Áfangastað</span><span class="sxs-lookup"><span data-stu-id="e7b00-206">Click Add destination.</span></span>
    * <span data-ttu-id="e7b00-207">Bæta við forritstöflum sem áskildum viðtökustað sem krefst uppfærslna til að skjala upplýsingar um skráðar Instrastat færslur.</span><span class="sxs-lookup"><span data-stu-id="e7b00-207">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="e7b00-208">Í svæðið Heiti, færðu inn „Safn“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-208">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="e7b00-209">Safnvista</span><span class="sxs-lookup"><span data-stu-id="e7b00-209">Archive</span></span>  
32. <span data-ttu-id="e7b00-210">Í svæðið Heiti töflu skal færa inn „IntrastatArchiveGeneral“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-210">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="e7b00-211">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="e7b00-211">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="e7b00-212">Haltu skýrsluaðgerðinni „Setja inn“ svo þú getir bætt skýrslum við á meðan skjölun upplýsinga um hvert Intrastat skýrslugerðarferli fer fram.</span><span class="sxs-lookup"><span data-stu-id="e7b00-212">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="e7b00-213">Veljið Já í svæðinu Færsla upplskrá.</span><span class="sxs-lookup"><span data-stu-id="e7b00-213">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="e7b00-214">Veldu Já til að fá upplýsingar um vandkvæði varðandi gagnauppfærslu hugbúnaðarins.</span><span class="sxs-lookup"><span data-stu-id="e7b00-214">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="e7b00-215">Veljið Já í svæðinu Sleppa færsla aðgerð villuleit.</span><span class="sxs-lookup"><span data-stu-id="e7b00-215">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="e7b00-216">Veldu Já til að draga úr villum við villuleit um auða „Intrastat safnkenni“ reitinn.</span><span class="sxs-lookup"><span data-stu-id="e7b00-216">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="e7b00-217">Þetta verður gert eftir að skrám hefur verið bætt við, byggðar á númeraraðastillingum sem eru grunnstilltar fyrir þessa töflu í skjámyndinni Erlend viðskipti færibreytur.</span><span class="sxs-lookup"><span data-stu-id="e7b00-217">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="e7b00-218">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-218">Click OK.</span></span>
    * <span data-ttu-id="e7b00-219">Binda einingar úr viðbættri gagnaveitu (afmarkað líkan byggt á völdu rótaratriði) við einingar frá viðbættum viðtökustað.</span><span class="sxs-lookup"><span data-stu-id="e7b00-219">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="e7b00-220">Í trénu skal víkka út „Safn“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-220">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="e7b00-221">Í trénu skal víkka út „Safn\<Tengsl“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-221">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="e7b00-222">Í trénu skal víkka út „Safn\<Tengsl\IntrastatArchiveDetail“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-222">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="e7b00-223">Í trénu skal velja „Safn\<Tengsl\IntrastatArchiveDetail\Upphæð(UpphæðMST)'.“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-223">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="e7b00-224">Í trénu skal víkka út „Líkan\Safn haus\Tölusettar línur“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-224">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="e7b00-225">Í trénu skal víkka út „Líkan\Safn haus\Tölusettar línur\Gildi“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-225">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="e7b00-226">Í trénu skal víkka út „Líkan\Safn haus\Tölusettar línur\Gildi\Upphæð“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-226">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="e7b00-227">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e7b00-227">Click Bind.</span></span>
44. <span data-ttu-id="e7b00-228">Í trénu skal velja „Safn\<Tengsl\IntrastatArchiveDetail\Grunnvara(IntrastatCommodity)“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-228">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="e7b00-229">Í trénu skal velja „Líkan\Safn haus\Tölusettar línur\Gildi\Grunnvara skrá kenni“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-229">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="e7b00-230">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e7b00-230">Click Bind.</span></span>
47. <span data-ttu-id="e7b00-231">Í trénu skal velja „Safn\<Tengsl\IntrastatArchiveDetail\Afurðanúmer(ItemIdi)“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-231">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="e7b00-232">Í trénu skal velja „Líkan\Safn haus\Tölusettar línur\Gildi\Afurðanúmer“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-232">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="e7b00-233">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e7b00-233">Click Bind.</span></span>
50. <span data-ttu-id="e7b00-234">Í trénu skal velja „Safn\<Tengsl\IntrastatArchiveDetail\Lína númer(LineNumber)“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-234">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="e7b00-235">Í trénu skal velja „Líkan\Safn haus\Tölusettar línur\Númer“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-235">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="e7b00-236">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e7b00-236">Click Bind.</span></span>
53. <span data-ttu-id="e7b00-237">Í trénu skal velja „Safn\<Tengsl\IntrastatArchiveDetail“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-237">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="e7b00-238">Í trénu skal velja „Líkan\Safn haus\Tölusettar línur“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-238">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="e7b00-239">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e7b00-239">Click Bind.</span></span>
56. <span data-ttu-id="e7b00-240">Í trénu skal velja „Safn\Heiti skráar (FileName)“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-240">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="e7b00-241">Í trénu skal velja „Líkan\Safn haus\Heiti skráar“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-241">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="e7b00-242">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e7b00-242">Click Bind.</span></span>
59. <span data-ttu-id="e7b00-243">Í trénu skal velja „Safn\Fjöldi lína(NumberOfLines)“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-243">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="e7b00-244">Í trénu skal velja „Líkan\Safn haus\Fjöldi lína“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-244">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="e7b00-245">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e7b00-245">Click Bind.</span></span>
62. <span data-ttu-id="e7b00-246">Í trénu skal velja „Safn“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-246">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="e7b00-247">Í trénu skal velja „Líkan\Safn haus“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-247">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="e7b00-248">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e7b00-248">Click Bind.</span></span>
65. <span data-ttu-id="e7b00-249">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e7b00-249">Click Save.</span></span>
66. <span data-ttu-id="e7b00-250">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e7b00-250">Close the page.</span></span>
67. <span data-ttu-id="e7b00-251">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e7b00-251">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]