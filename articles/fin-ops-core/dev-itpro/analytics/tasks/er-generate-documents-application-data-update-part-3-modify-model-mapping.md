---
title: Breyta líkani og vörpun til að búa til skjöl sem eru með forritsgögnum
description: 'Til að ljúka skrefunum í þessu ferli verður fyrst að ljúka við ferlið, „Rafræn skýrslugerð Búa til skjöl með gagnauppfærslum fyrir forrit (Hluti 2: Búa til skjöl)“.'
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5df6128228b9ff620c606c550c5eb7a6039b915
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182302"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="4a2ce-103">Breyta líkani og vörpun til að búa til skjöl sem eru með forritsgögnum</span><span class="sxs-lookup"><span data-stu-id="4a2ce-103">Modify models and mappings to generate documents that have application data</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4a2ce-104">Til að ljúka skrefunum í þessu ferli verður fyrst að ljúka við ferlið, „Rafræn skýrslugerð Búa til skjöl með gagnauppfærslum fyrir forrit (Hluti 2: Búa til skjöl)“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 2: Generate documents)”.</span></span> 

<span data-ttu-id="4a2ce-105">Skrefin í þessu ferli sýna hvernig skal hanna Rafræna skýrslugerð (ER) grunnstillingar þannig að þær búi til rafræn skjöl og uppfæri gögn fyrir forrit.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="4a2ce-106">Í þessu ferli muntu breyta Rafræna skýrslugerð (ER) grunnstillingar þannig að hægt sé að byrja að nota þær til að búa til rafræn skjöl og uppfæra gögn fyrir forrit.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="4a2ce-107">Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="4a2ce-108">Skrefin er hægt að klára með því að nota DEMF gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="4a2ce-109">Breyta gagnalíkani</span><span class="sxs-lookup"><span data-stu-id="4a2ce-109">Modify data model</span></span>
1. <span data-ttu-id="4a2ce-110">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="4a2ce-111">Í trénu skal velja „Intrastat (líkan)“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="4a2ce-112">Þú munt útvíkka það hvernig þú notar gagnalíkanið.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-112">You will extend how you use the data model.</span></span> <span data-ttu-id="4a2ce-113">Fyrir utan að nota það sem gagnaveitu til að búa til Intrastat skýrsluna, verður gagnalíkanið notað til að safna upplýsingum um Instrastat skýrslugerðarferlið.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="4a2ce-114">Upplýsingarnar verða síðan notaðar til að uppfæra gögn fyrir forrit.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="4a2ce-115">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-115">Click Designer.</span></span>
4. <span data-ttu-id="4a2ce-116">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="4a2ce-117">Í svæði Nýr hnútur sem, slá inn „Líkanshnútur“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="4a2ce-118">Í reitnum Heiti skal færa inn „Fyrir gagnauppfærslu fyrir forrit“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="4a2ce-119">Fyrir uppfærsla gagna hugbúnaðarins</span><span class="sxs-lookup"><span data-stu-id="4a2ce-119">For application data update</span></span>  
7. <span data-ttu-id="4a2ce-120">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-120">Click Add.</span></span>
8. <span data-ttu-id="4a2ce-121">Í trénu skal velja „Fyrir gagnauppfærslu fyrir forrit“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="4a2ce-122">Þessu nýja rótaratriði er bætt við til að tilgreina gagnaflæði fyrir gögn á hreyfingu frá Intrastat skýrslunni (notuð sem gagnaveitu) til tafla forrits (áfangastaður uppfærslu).</span><span class="sxs-lookup"><span data-stu-id="4a2ce-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="4a2ce-123">Athugið að mismunandi rótaratriði verður að nota til að sækja gögn sem eru bókuð í skjal á útleið og til að sækja gögn frá skjalinu sem er notað til að uppfæra gögn fyrir forrit.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="4a2ce-124">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="4a2ce-125">Í svæðið Heiti, færðu inn „Safn haus“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="4a2ce-126">Safnshaus</span><span class="sxs-lookup"><span data-stu-id="4a2ce-126">Archive header</span></span>  
11. <span data-ttu-id="4a2ce-127">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="4a2ce-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="4a2ce-128">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-128">Click Add.</span></span>
    * <span data-ttu-id="4a2ce-129">Þú munt stofna skrá fyrir hverja Intrastat skýrslu sem er búin til, og þess vegna þarftu að búa til nýtt atriði fyrir það.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="4a2ce-130">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="4a2ce-131">Í svæðið Heiti, færðu inn 'skrárnafn'.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="4a2ce-132">Skrárnafn</span><span class="sxs-lookup"><span data-stu-id="4a2ce-132">File name</span></span>  
15. <span data-ttu-id="4a2ce-133">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="4a2ce-134">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-134">Click Add.</span></span>
17. <span data-ttu-id="4a2ce-135">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="4a2ce-136">Í svæðið Heiti, færðu inn “Númer lína“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="4a2ce-137">Línufjöldi</span><span class="sxs-lookup"><span data-stu-id="4a2ce-137">Number of lines</span></span>  
19. <span data-ttu-id="4a2ce-138">Velja „Heiltala“ í svæðinu gerð Vöru.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="4a2ce-139">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-139">Click Add.</span></span>
    * <span data-ttu-id="4a2ce-140">Bættu þessu atriði við til að tákna númer Intrastat færslnanna sem eru skráðar á meðan núverandi skráningarferli stendur.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="4a2ce-141">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="4a2ce-142">Í svæðið Heiti, færðu inn „Safn línur“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="4a2ce-143">Safnslínur</span><span class="sxs-lookup"><span data-stu-id="4a2ce-143">Archive lines</span></span>  
23. <span data-ttu-id="4a2ce-144">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="4a2ce-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="4a2ce-145">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-145">Click Add.</span></span>
    * <span data-ttu-id="4a2ce-146">Bættu þessu atriði við til að tákna lista Intrastat færslnanna sem eru skráðar á meðan núverandi skráningarferli stendur.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="4a2ce-147">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="4a2ce-148">Í reitnum Heiti skal færa inn ‚Upphæð'.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="4a2ce-149">Upphæð</span><span class="sxs-lookup"><span data-stu-id="4a2ce-149">Amount</span></span>  
27. <span data-ttu-id="4a2ce-150">Veljið 'Raunveruleg' í svæðinu gerð vöru.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="4a2ce-151">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-151">Click Add.</span></span>
29. <span data-ttu-id="4a2ce-152">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="4a2ce-153">Í svæðið Heiti, færðu inn „Grunnvara skrá kenni“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="4a2ce-154">Vöru skrá kenni</span><span class="sxs-lookup"><span data-stu-id="4a2ce-154">Commodity rec id</span></span>  
31. <span data-ttu-id="4a2ce-155">Velja „Int64“ í svæðinu gerð Vöru.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="4a2ce-156">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-156">Click Add.</span></span>
33. <span data-ttu-id="4a2ce-157">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="4a2ce-158">Í reitnum Heiti skal færa inn „Númer afurðar“</span><span class="sxs-lookup"><span data-stu-id="4a2ce-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="4a2ce-159">Vörunúmer</span><span class="sxs-lookup"><span data-stu-id="4a2ce-159">Item number</span></span>  
35. <span data-ttu-id="4a2ce-160">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="4a2ce-161">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-161">Click Add.</span></span>
37. <span data-ttu-id="4a2ce-162">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-162">Click Save.</span></span>
38. <span data-ttu-id="4a2ce-163">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="4a2ce-164">Breyta Vörpun líkans</span><span class="sxs-lookup"><span data-stu-id="4a2ce-164">Modify model mapping</span></span>
1. <span data-ttu-id="4a2ce-165">Í trénu skal víkka út „Intrastat (líkan)“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="4a2ce-166">Í trénu skal velja „Intrastat (líkan)\Intrastat (vörpun)“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="4a2ce-167">Breyta fyrirliggjandi vörpun líkans til að hefja notkun þess fyrir uppfærslu gagna fyrir forrit og til að skjala upplýsingar um Intrastat skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="4a2ce-168">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-168">Click Designer.</span></span>
4. <span data-ttu-id="4a2ce-169">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-169">Click New.</span></span>
5. <span data-ttu-id="4a2ce-170">Í svæðið Heiti, færðu inn „Uppfæra safn“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="4a2ce-171">Uppfæra safn</span><span class="sxs-lookup"><span data-stu-id="4a2ce-171">Update archive</span></span>  
6. <span data-ttu-id="4a2ce-172">Í reitnum Stefna skal velja „Til viðtökustaðar".</span><span class="sxs-lookup"><span data-stu-id="4a2ce-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="4a2ce-173">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-173">Click Save.</span></span>
    * <span data-ttu-id="4a2ce-174">Þessu nýja rótaratriði er bætt við til að tilgreina gagnaflæði fyrir gögn á hreyfingu frá Intrastat skýrslunni (notuð sem gagnaveitu) til tafla forrits (áfangastaður uppfærslu).</span><span class="sxs-lookup"><span data-stu-id="4a2ce-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="4a2ce-175">Athugið að mismunandi rótaratriði líkans verður að nota til að sækja gögn frá forritinu fyrir skýrslugerðarferlið og síðan nota gögnin úr gagnalíkaninu fyrir uppfærslu hugbúnaðargagna.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-175">Note that different model’s root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="4a2ce-176">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-176">Click Designer.</span></span>
9. <span data-ttu-id="4a2ce-177">Í trénu skal velja „Gagnalíkan\Gagnalíkan“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="4a2ce-178">Bættu við þeirri gagnaveitu sem er krafist</span><span class="sxs-lookup"><span data-stu-id="4a2ce-178">Add the required data source.</span></span> <span data-ttu-id="4a2ce-179">Þetta er gagnalíkanið sem inniheldur upplýsingar um skráðar Intrastat færslur sem verða að vera skjalaðar.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="4a2ce-180">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-180">Click Add root.</span></span>
11. <span data-ttu-id="4a2ce-181">Í reitnum Heiti skal færa inn „líkan“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="4a2ce-182">líkan</span><span class="sxs-lookup"><span data-stu-id="4a2ce-182">model</span></span>  
12. <span data-ttu-id="4a2ce-183">Sláið inn eða veldu gildið „Fyrir gagnauppfærslu fyrir forrit“ í reitnum Skilgreining.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-183">In the Definition field, enter or select the value ‘For application data update’.</span></span>
    * <span data-ttu-id="4a2ce-184">Fyrir uppfærsla gagna hugbúnaðarins</span><span class="sxs-lookup"><span data-stu-id="4a2ce-184">For application data update</span></span>  
13. <span data-ttu-id="4a2ce-185">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-185">Click OK.</span></span>
14. <span data-ttu-id="4a2ce-186">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="4a2ce-187">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="4a2ce-188">Í trénu skal velja „Líkan\Safn haus“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="4a2ce-189">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-189">Click Add.</span></span>
    * <span data-ttu-id="4a2ce-190">Þar sem þú vilt tölusetja skráðar Intrastat færslur í skjölun, verður að bæta við viðeigandi gagnaveitu.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="4a2ce-191">Í svæðið Heiti, færðu inn „Tölusettar línur“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="4a2ce-192">Tölusettar línur</span><span class="sxs-lookup"><span data-stu-id="4a2ce-192">Enumerated lines</span></span>  
19. <span data-ttu-id="4a2ce-193">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-193">Click Edit formula.</span></span>
20. <span data-ttu-id="4a2ce-194">Í trénu skal velja „Listi\TÖLUSETJA“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="4a2ce-195">Smelltu á Bæta við Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-195">Click Add function.</span></span>
22. <span data-ttu-id="4a2ce-196">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="4a2ce-197">Í trénu skal víkka út „Líkan\Safn haus“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="4a2ce-198">Í trénu skal víkka út „Líkan\Safn haus\Safn línur“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="4a2ce-199">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-199">Click Add data source.</span></span>
26. <span data-ttu-id="4a2ce-200">Í svæði Formúla slá inn „SKEYTA SAMAN(líkan.„Safn haus“ „Safn línur“)“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="4a2ce-201">TÖLUSETJA(líkan.„Safn haus“ „Safn línur“)</span><span class="sxs-lookup"><span data-stu-id="4a2ce-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="4a2ce-202">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-202">Click Save.</span></span>
28. <span data-ttu-id="4a2ce-203">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-203">Close the page.</span></span>
29. <span data-ttu-id="4a2ce-204">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-204">Click OK.</span></span>
30. <span data-ttu-id="4a2ce-205">Smelltu á Bæta við Áfangastað</span><span class="sxs-lookup"><span data-stu-id="4a2ce-205">Click Add destination.</span></span>
    * <span data-ttu-id="4a2ce-206">Bæta við forritstöflum sem áskildum viðtökustað sem krefst uppfærslna til að skjala upplýsingar um skráðar Instrastat færslur.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="4a2ce-207">Í svæðið Heiti, færðu inn „Safn“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="4a2ce-208">Safnvista</span><span class="sxs-lookup"><span data-stu-id="4a2ce-208">Archive</span></span>  
32. <span data-ttu-id="4a2ce-209">Í svæðið Heiti töflu skal færa inn „IntrastatArchiveGeneral“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="4a2ce-210">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="4a2ce-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="4a2ce-211">Haltu skýrsluaðgerðinni „Setja inn“ svo þú getir bætt skýrslum við á meðan skjölun upplýsinga um hvert Intrastat skýrslugerðarferli fer fram.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-211">Keep the record action ‘Insert’ so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="4a2ce-212">Veljið Já í svæðinu Færsla upplskrá.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="4a2ce-213">Veldu Já til að fá upplýsingar um vandkvæði varðandi gagnauppfærslu hugbúnaðarins.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="4a2ce-214">Veljið Já í svæðinu Sleppa færsla aðgerð villuleit.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="4a2ce-215">Veldu Já til að draga úr villum við villuleit um auða „Intrastat safnkenni“ reitinn.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-215">Select Yes to suppress validation errors about the empty ‘Intrastat archive ID’ field.</span></span> <span data-ttu-id="4a2ce-216">Þetta verður gert eftir að skrám hefur verið bætt við, byggðar á númeraraðastillingum sem eru grunnstilltar fyrir þessa töflu í skjámyndinni Erlend viðskipti færibreytur.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="4a2ce-217">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-217">Click OK.</span></span>
    * <span data-ttu-id="4a2ce-218">Binda einingar úr viðbættri gagnaveitu (afmarkað líkan byggt á völdu rótaratriði) við einingar frá viðbættum viðtökustað.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="4a2ce-219">Í trénu skal víkka út „Safn“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="4a2ce-220">Í trénu skal víkka út „Safn\<Tengsl“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="4a2ce-221">Í trénu skal víkka út „Safn\<Tengsl\IntrastatArchiveDetail“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="4a2ce-222">Í trénu skal velja „Safn\<Tengsl\IntrastatArchiveDetail\Upphæð(UpphæðMST)'.“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="4a2ce-223">Í trénu skal víkka út „Líkan\Safn haus\Tölusettar línur“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="4a2ce-224">Í trénu skal víkka út „Líkan\Safn haus\Tölusettar línur\Gildi“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="4a2ce-225">Í trénu skal víkka út „Líkan\Safn haus\Tölusettar línur\Gildi\Upphæð“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="4a2ce-226">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-226">Click Bind.</span></span>
44. <span data-ttu-id="4a2ce-227">Í trénu skal velja „Safn\<Tengsl\IntrastatArchiveDetail\Grunnvara(IntrastatCommodity)“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="4a2ce-228">Í trénu skal velja „Líkan\Safn haus\Tölusettar línur\Gildi\Grunnvara skrá kenni“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="4a2ce-229">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-229">Click Bind.</span></span>
47. <span data-ttu-id="4a2ce-230">Í trénu skal velja „Safn\<Tengsl\IntrastatArchiveDetail\Afurðanúmer(ItemIdi)“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="4a2ce-231">Í trénu skal velja „Líkan\Safn haus\Tölusettar línur\Gildi\Afurðanúmer“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="4a2ce-232">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-232">Click Bind.</span></span>
50. <span data-ttu-id="4a2ce-233">Í trénu skal velja „Safn\<Tengsl\IntrastatArchiveDetail\Lína númer(LineNumber)“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="4a2ce-234">Í trénu skal velja „Líkan\Safn haus\Tölusettar línur\Númer“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="4a2ce-235">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-235">Click Bind.</span></span>
53. <span data-ttu-id="4a2ce-236">Í trénu skal velja „Safn\<Tengsl\IntrastatArchiveDetail“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="4a2ce-237">Í trénu skal velja „Líkan\Safn haus\Tölusettar línur“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="4a2ce-238">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-238">Click Bind.</span></span>
56. <span data-ttu-id="4a2ce-239">Í trénu skal velja „Safn\Heiti skráar (FileName)“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="4a2ce-240">Í trénu skal velja „Líkan\Safn haus\Heiti skráar“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="4a2ce-241">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-241">Click Bind.</span></span>
59. <span data-ttu-id="4a2ce-242">Í trénu skal velja „Safn\Fjöldi lína(NumberOfLines)“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="4a2ce-243">Í trénu skal velja „Líkan\Safn haus\Fjöldi lína“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="4a2ce-244">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-244">Click Bind.</span></span>
62. <span data-ttu-id="4a2ce-245">Í trénu skal velja „Safn“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="4a2ce-246">Í trénu skal velja „Líkan\Safn haus“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="4a2ce-247">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-247">Click Bind.</span></span>
65. <span data-ttu-id="4a2ce-248">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-248">Click Save.</span></span>
66. <span data-ttu-id="4a2ce-249">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-249">Close the page.</span></span>
67. <span data-ttu-id="4a2ce-250">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="4a2ce-250">Close the page.</span></span>
