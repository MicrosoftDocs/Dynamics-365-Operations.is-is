--- 
title: "Rafræn skýrslugerð stofna grunnstilling sniðs (nóvember 2016)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarsnið fyrir rafræna skýrslugerð (ER)."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 803ed4a1018d344f1b40fa1f2338fc066e784c3c
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="ff424-103">Rafræn skýrslugerð stofna grunnstilling sniðs (nóvember 2016)</span><span class="sxs-lookup"><span data-stu-id="ff424-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ff424-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarsnið fyrir rafræna skýrslugerð (ER).</span><span class="sxs-lookup"><span data-stu-id="ff424-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="ff424-105">Þessa sniðsskilgreiningu mun skilgreina snið rafræn skjöl sem eru notaðar til að vinna greiðslur.</span><span class="sxs-lookup"><span data-stu-id="ff424-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="ff424-106">Í þessu dæmi stofnar þú skilgreiningu á sniði fyrir dæmi um fyrirtæki, í þessu dæmi Litware, Inc. Til að ljúka þessum skrefum, þarf fyrst að ljúka við skref í ferlinu „Varpa líkani á valda gagnaveitu".</span><span class="sxs-lookup"><span data-stu-id="ff424-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="ff424-107">Stofna nýja skilgreiningu á sniði</span><span class="sxs-lookup"><span data-stu-id="ff424-107">Create a new format configuration</span></span>
1. <span data-ttu-id="ff424-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="ff424-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="ff424-109">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="ff424-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="ff424-110">Veljið 'Greiðslur (einfaldað líkan)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="ff424-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="ff424-111">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="ff424-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="ff424-112">Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkani PaymentModel“.</span><span class="sxs-lookup"><span data-stu-id="ff424-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="ff424-113">Í reitinn Heiti skal slá inn 'BACS (UK uppspunnið)'.</span><span class="sxs-lookup"><span data-stu-id="ff424-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="ff424-114">BACS (UK Upphugsað)</span><span class="sxs-lookup"><span data-stu-id="ff424-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="ff424-115">Færið inn 'BACS greiðslusnið lánardrottins (UK uppspunnið)' í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="ff424-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="ff424-116">Greiðslusnið lánardrottins BACS (UK Upphugsað)</span><span class="sxs-lookup"><span data-stu-id="ff424-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="ff424-117">Virkt skilgreiningarveitu er sjálfkrafa færð inn hér.</span><span class="sxs-lookup"><span data-stu-id="ff424-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="ff424-118">Þessa veitu mun geta unnið með þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="ff424-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="ff424-119">Önnur veitur er hægt að nota þetta skilgreining, en geta ekki unnið með hana.</span><span class="sxs-lookup"><span data-stu-id="ff424-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="ff424-120">Hægt er að skilgreina ákveðið snið rafrænt skjal.</span><span class="sxs-lookup"><span data-stu-id="ff424-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="ff424-121">Þetta svæði er skilið eftir autt ef óskað er að velja snið á tíma keyrslu.</span><span class="sxs-lookup"><span data-stu-id="ff424-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="ff424-122">Í reitinn Skilgreining Gagnalíkans skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="ff424-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="ff424-123">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="ff424-123">Click Create configuration.</span></span>
    * <span data-ttu-id="ff424-124">Ný Skilgreining hefur verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="ff424-124">A new configuration has been created.</span></span> <span data-ttu-id="ff424-125">Hægt er að nota sem útgáfuna drög til að vista hannað snið fyrir umsjón með rafrænum skjölum.</span><span class="sxs-lookup"><span data-stu-id="ff424-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="ff424-126">Hanna snið rafrænts skjals</span><span class="sxs-lookup"><span data-stu-id="ff424-126">Design format of electronic document</span></span>
1. <span data-ttu-id="ff424-127">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="ff424-127">Click Designer.</span></span>
2. <span data-ttu-id="ff424-128">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ff424-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="ff424-129">Veljið 'Common\File', í trénu.</span><span class="sxs-lookup"><span data-stu-id="ff424-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="ff424-130">Í reitnum Heiti skal færa inn ‚Xml‘.</span><span class="sxs-lookup"><span data-stu-id="ff424-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="ff424-131">Xml</span><span class="sxs-lookup"><span data-stu-id="ff424-131">Xml</span></span>  
5. <span data-ttu-id="ff424-132">Í reitinn Kóðun skal slá inn „UTF-8“.</span><span class="sxs-lookup"><span data-stu-id="ff424-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="ff424-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="ff424-133">UTF-8</span></span>  
6. <span data-ttu-id="ff424-134">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ff424-134">Click OK.</span></span>
7. <span data-ttu-id="ff424-135">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ff424-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="ff424-136">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="ff424-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="ff424-137">Í reitnum Heiti skal færa inn ‚Skilaboð‘.</span><span class="sxs-lookup"><span data-stu-id="ff424-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="ff424-138">Skilaboð</span><span class="sxs-lookup"><span data-stu-id="ff424-138">Message</span></span>  
10. <span data-ttu-id="ff424-139">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ff424-139">Click OK.</span></span>
11. <span data-ttu-id="ff424-140">Í trénu skal velja 'Xml\Message'.</span><span class="sxs-lookup"><span data-stu-id="ff424-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="ff424-141">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="ff424-141">Click Add Element.</span></span>
13. <span data-ttu-id="ff424-142">Í reitnum Heiti skal færa inn ‚ProcessingDate‘.</span><span class="sxs-lookup"><span data-stu-id="ff424-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="ff424-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="ff424-143">ProcessingDate</span></span>  
14. <span data-ttu-id="ff424-144">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ff424-144">Click OK.</span></span>
15. <span data-ttu-id="ff424-145">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="ff424-145">Click Add Element.</span></span>
16. <span data-ttu-id="ff424-146">Í svæðið Heiti, færðu inn 'MessageId'.</span><span class="sxs-lookup"><span data-stu-id="ff424-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="ff424-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="ff424-147">MessageId</span></span>  
17. <span data-ttu-id="ff424-148">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ff424-148">Click OK.</span></span>
18. <span data-ttu-id="ff424-149">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="ff424-149">Click Add Element.</span></span>
19. <span data-ttu-id="ff424-150">Í svæðið Heiti, færðu inn 'Greiðslur'.</span><span class="sxs-lookup"><span data-stu-id="ff424-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="ff424-151">Greiðslur</span><span class="sxs-lookup"><span data-stu-id="ff424-151">Payments</span></span>  
20. <span data-ttu-id="ff424-152">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ff424-152">Click OK.</span></span>
21. <span data-ttu-id="ff424-153">Í trénu skal velja 'Xml\Message\Payments'.</span><span class="sxs-lookup"><span data-stu-id="ff424-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="ff424-154">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="ff424-154">Click Add Element.</span></span>
23. <span data-ttu-id="ff424-155">Í reitnum Heiti skal færa inn ‚Atriði.</span><span class="sxs-lookup"><span data-stu-id="ff424-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="ff424-156">vara</span><span class="sxs-lookup"><span data-stu-id="ff424-156">Item</span></span>  
24. <span data-ttu-id="ff424-157">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ff424-157">Click OK.</span></span>
25. <span data-ttu-id="ff424-158">Í trénu skal velja 'Xml\Message\Payments\Item'.</span><span class="sxs-lookup"><span data-stu-id="ff424-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="ff424-159">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ff424-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="ff424-160">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="ff424-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="ff424-161">Í reitnum Heiti skal færa inn ‚Id‘.</span><span class="sxs-lookup"><span data-stu-id="ff424-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="ff424-162">Auðkenni</span><span class="sxs-lookup"><span data-stu-id="ff424-162">Id</span></span>  
29. <span data-ttu-id="ff424-163">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ff424-163">Click OK.</span></span>
30. <span data-ttu-id="ff424-164">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ff424-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="ff424-165">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="ff424-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="ff424-166">Í reitnum Heiti skal færa inn ‚lánardrottinn‘.</span><span class="sxs-lookup"><span data-stu-id="ff424-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="ff424-167">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="ff424-167">Vendor</span></span>  
33. <span data-ttu-id="ff424-168">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ff424-168">Click OK.</span></span>
34. <span data-ttu-id="ff424-169">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor'.</span><span class="sxs-lookup"><span data-stu-id="ff424-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="ff424-170">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="ff424-170">Click Add Element.</span></span>
36. <span data-ttu-id="ff424-171">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="ff424-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="ff424-172">Nafn</span><span class="sxs-lookup"><span data-stu-id="ff424-172">Name</span></span>  
37. <span data-ttu-id="ff424-173">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ff424-173">Click OK.</span></span>
38. <span data-ttu-id="ff424-174">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="ff424-174">Click Add Element.</span></span>
39. <span data-ttu-id="ff424-175">Í reitnum Heiti skal færa inn ‚Banki'.</span><span class="sxs-lookup"><span data-stu-id="ff424-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="ff424-176">Banki</span><span class="sxs-lookup"><span data-stu-id="ff424-176">Bank</span></span>  
40. <span data-ttu-id="ff424-177">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ff424-177">Click OK.</span></span>
41. <span data-ttu-id="ff424-178">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank'.</span><span class="sxs-lookup"><span data-stu-id="ff424-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="ff424-179">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="ff424-179">Click Add Element.</span></span>
43. <span data-ttu-id="ff424-180">Í svæðið Heiti, færðu inn 'RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="ff424-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="ff424-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="ff424-181">RoutingNumber</span></span>  
44. <span data-ttu-id="ff424-182">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ff424-182">Click OK.</span></span>
45. <span data-ttu-id="ff424-183">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="ff424-183">Click Add Element.</span></span>
46. <span data-ttu-id="ff424-184">Í svæðið Heiti, færðu inn ‚AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="ff424-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="ff424-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="ff424-185">AccountNumber</span></span>  
47. <span data-ttu-id="ff424-186">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ff424-186">Click OK.</span></span>
48. <span data-ttu-id="ff424-187">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor'.</span><span class="sxs-lookup"><span data-stu-id="ff424-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="ff424-188">Smellið á Afrit.</span><span class="sxs-lookup"><span data-stu-id="ff424-188">Click Copy.</span></span>
50. <span data-ttu-id="ff424-189">Í trénu skal velja 'Xml\Message\Payments\Item'.</span><span class="sxs-lookup"><span data-stu-id="ff424-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="ff424-190">Smellt er á Líma.</span><span class="sxs-lookup"><span data-stu-id="ff424-190">Click Paste.</span></span>
52. <span data-ttu-id="ff424-191">Í reitnum Heiti skal færa inn ‚Greiðandi‘.</span><span class="sxs-lookup"><span data-stu-id="ff424-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="ff424-192">Greiðandi</span><span class="sxs-lookup"><span data-stu-id="ff424-192">Payer</span></span>  
53. <span data-ttu-id="ff424-193">Í trénu skal velja 'Xml\Message\Payments\Item'.</span><span class="sxs-lookup"><span data-stu-id="ff424-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="ff424-194">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="ff424-194">Click Add Element.</span></span>
55. <span data-ttu-id="ff424-195">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="ff424-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="ff424-196">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="ff424-196">Currency</span></span>  
56. <span data-ttu-id="ff424-197">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ff424-197">Click OK.</span></span>
57. <span data-ttu-id="ff424-198">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="ff424-198">Click Add Element.</span></span>
58. <span data-ttu-id="ff424-199">Í reitnum Heiti skal færa inn ‚Lýsing'.</span><span class="sxs-lookup"><span data-stu-id="ff424-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="ff424-200">lýsing</span><span class="sxs-lookup"><span data-stu-id="ff424-200">Description</span></span>  
59. <span data-ttu-id="ff424-201">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ff424-201">Click OK.</span></span>
60. <span data-ttu-id="ff424-202">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="ff424-202">Click Add Element.</span></span>
61. <span data-ttu-id="ff424-203">Í svæðið Heiti, færðu inn ‚TransDate'.</span><span class="sxs-lookup"><span data-stu-id="ff424-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="ff424-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="ff424-204">TransDate</span></span>  
62. <span data-ttu-id="ff424-205">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ff424-205">Click OK.</span></span>
63. <span data-ttu-id="ff424-206">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="ff424-206">Click Add Element.</span></span>
64. <span data-ttu-id="ff424-207">Í reitnum Heiti skal færa inn ‚Upphæð'.</span><span class="sxs-lookup"><span data-stu-id="ff424-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="ff424-208">Upphæð</span><span class="sxs-lookup"><span data-stu-id="ff424-208">Amount</span></span>  
65. <span data-ttu-id="ff424-209">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ff424-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="ff424-210">Undirbúa íhluti sniðs fyrir vörpun í einingar gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="ff424-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="ff424-211">Í trénu skal velja 'Xml\Message\ProcessingDate'.</span><span class="sxs-lookup"><span data-stu-id="ff424-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="ff424-212">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ff424-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="ff424-213">Í trénu skal velja 'Text\DateTime'.</span><span class="sxs-lookup"><span data-stu-id="ff424-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="ff424-214">Í svæðinu Snið 'áááá-MM-dd' skal fært inn.</span><span class="sxs-lookup"><span data-stu-id="ff424-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="ff424-215">áááá-MM-dd</span><span class="sxs-lookup"><span data-stu-id="ff424-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="ff424-216">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ff424-216">Click OK.</span></span>
6. <span data-ttu-id="ff424-217">Í trénu skal velja 'Xml\Message\Payments\Item\TransDate'.</span><span class="sxs-lookup"><span data-stu-id="ff424-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="ff424-218">Smella á Bæta við dagsetning/tími.</span><span class="sxs-lookup"><span data-stu-id="ff424-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="ff424-219">Í svæðinu Snið 'áááá-MM-dd' skal fært inn.</span><span class="sxs-lookup"><span data-stu-id="ff424-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="ff424-220">áááá-MM-dd</span><span class="sxs-lookup"><span data-stu-id="ff424-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="ff424-221">Í svæði Gerð dagsetning/tími skal velja „Dagsetning“.</span><span class="sxs-lookup"><span data-stu-id="ff424-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="ff424-222">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ff424-222">Click OK.</span></span>
11. <span data-ttu-id="ff424-223">Í trénu skal velja 'Xml\Message\MessageId'.</span><span class="sxs-lookup"><span data-stu-id="ff424-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="ff424-224">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ff424-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="ff424-225">Í trénu skal velja ‚Texti/Strengur'.</span><span class="sxs-lookup"><span data-stu-id="ff424-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="ff424-226">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="ff424-226">Click OK.</span></span>
15. <span data-ttu-id="ff424-227">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Name'.</span><span class="sxs-lookup"><span data-stu-id="ff424-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="ff424-228">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="ff424-228">Click Add String.</span></span>
17. <span data-ttu-id="ff424-229">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="ff424-229">Click OK.</span></span>
18. <span data-ttu-id="ff424-230">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="ff424-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="ff424-231">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="ff424-231">Click Add String.</span></span>
20. <span data-ttu-id="ff424-232">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="ff424-232">Click OK.</span></span>
21. <span data-ttu-id="ff424-233">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="ff424-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="ff424-234">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="ff424-234">Click Add String.</span></span>
23. <span data-ttu-id="ff424-235">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="ff424-235">Click OK.</span></span>
24. <span data-ttu-id="ff424-236">Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Name'.</span><span class="sxs-lookup"><span data-stu-id="ff424-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="ff424-237">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="ff424-237">Click Add String.</span></span>
26. <span data-ttu-id="ff424-238">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="ff424-238">Click OK.</span></span>
27. <span data-ttu-id="ff424-239">Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="ff424-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="ff424-240">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="ff424-240">Click Add String.</span></span>
29. <span data-ttu-id="ff424-241">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="ff424-241">Click OK.</span></span>
30. <span data-ttu-id="ff424-242">Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="ff424-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="ff424-243">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="ff424-243">Click Add String.</span></span>
32. <span data-ttu-id="ff424-244">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="ff424-244">Click OK.</span></span>
33. <span data-ttu-id="ff424-245">Í trénu skal velja 'Xml\Message\Payments\Item\Currency'.</span><span class="sxs-lookup"><span data-stu-id="ff424-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="ff424-246">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="ff424-246">Click Add String.</span></span>
35. <span data-ttu-id="ff424-247">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="ff424-247">Click OK.</span></span>
36. <span data-ttu-id="ff424-248">Í trénu skal velja 'Xml\Message\Payments\Item\Description'.</span><span class="sxs-lookup"><span data-stu-id="ff424-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="ff424-249">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="ff424-249">Click Add String.</span></span>
38. <span data-ttu-id="ff424-250">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="ff424-250">Click OK.</span></span>
39. <span data-ttu-id="ff424-251">Í trénu skal velja 'Xml\Message\Payments\Item\Amount'.</span><span class="sxs-lookup"><span data-stu-id="ff424-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="ff424-252">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="ff424-252">Click Add String.</span></span>
41. <span data-ttu-id="ff424-253">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="ff424-253">Click OK.</span></span>
42. <span data-ttu-id="ff424-254">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="ff424-254">Click Save.</span></span>
43. <span data-ttu-id="ff424-255">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ff424-255">Close the page.</span></span>


