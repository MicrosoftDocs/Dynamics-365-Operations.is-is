--- 
title: "Stofna skilgreiningu sniðs fyrir rafræna skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarsnið fyrir rafræna skýrslugerð (ER)."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 04817d1f1851e43679995641e8b0ff99edaa83ad
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a><span data-ttu-id="56972-103">Stofna skilgreiningu sniðs fyrir rafræna skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="56972-103">Create a format configuration for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="56972-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarsnið fyrir rafræna skýrslugerð (ER).</span><span class="sxs-lookup"><span data-stu-id="56972-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="56972-105">Þessa sniðsskilgreiningu mun skilgreina snið rafræn skjöl sem eru notaðar til að vinna greiðslur.</span><span class="sxs-lookup"><span data-stu-id="56972-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="56972-106">Í þessu dæmi stofnar þú skilgreiningu á sniði fyrir dæmi um fyrirtæki, í þessu dæmi Litware, Inc. Til að ljúka þessum skrefum, þarf fyrst að ljúka við skref í ferlinu „Varpa líkani á valda gagnaveitu".</span><span class="sxs-lookup"><span data-stu-id="56972-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="56972-107">Stofna nýja skilgreiningu á sniði</span><span class="sxs-lookup"><span data-stu-id="56972-107">Create a new format configuration</span></span>
1. <span data-ttu-id="56972-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="56972-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="56972-109">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="56972-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="56972-110">Veljið 'Greiðslur (einfaldað líkan)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="56972-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="56972-111">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="56972-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="56972-112">Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkani PaymentModel“.</span><span class="sxs-lookup"><span data-stu-id="56972-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="56972-113">Í reitinn Heiti skal slá inn 'BACS (UK uppspunnið)'.</span><span class="sxs-lookup"><span data-stu-id="56972-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="56972-114">BACS (UK Upphugsað)</span><span class="sxs-lookup"><span data-stu-id="56972-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="56972-115">Færið inn 'BACS greiðslusnið lánardrottins (UK uppspunnið)' í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="56972-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="56972-116">Greiðslusnið lánardrottins BACS (UK Upphugsað)</span><span class="sxs-lookup"><span data-stu-id="56972-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="56972-117">Virkt skilgreiningarveitu er sjálfkrafa færð inn hér.</span><span class="sxs-lookup"><span data-stu-id="56972-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="56972-118">Þessa veitu mun geta unnið með þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="56972-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="56972-119">Önnur veitur er hægt að nota þetta skilgreining, en geta ekki unnið með hana.</span><span class="sxs-lookup"><span data-stu-id="56972-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="56972-120">Hægt er að skilgreina ákveðið snið rafrænt skjal.</span><span class="sxs-lookup"><span data-stu-id="56972-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="56972-121">Þetta svæði er skilið eftir autt ef óskað er að velja snið á tíma keyrslu.</span><span class="sxs-lookup"><span data-stu-id="56972-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="56972-122">Í reitinn Skilgreining Gagnalíkans skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="56972-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="56972-123">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="56972-123">Click Create configuration.</span></span>
    * <span data-ttu-id="56972-124">Ný Skilgreining hefur verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="56972-124">A new configuration has been created.</span></span> <span data-ttu-id="56972-125">Hægt er að nota sem útgáfuna drög til að vista hannað snið fyrir umsjón með rafrænum skjölum.</span><span class="sxs-lookup"><span data-stu-id="56972-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="56972-126">Hanna snið rafrænts skjals</span><span class="sxs-lookup"><span data-stu-id="56972-126">Design format of electronic document</span></span>
1. <span data-ttu-id="56972-127">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="56972-127">Click Designer.</span></span>
2. <span data-ttu-id="56972-128">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="56972-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="56972-129">Veljið 'Common\File', í trénu.</span><span class="sxs-lookup"><span data-stu-id="56972-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="56972-130">Í reitnum Heiti skal færa inn ‚Xml‘.</span><span class="sxs-lookup"><span data-stu-id="56972-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="56972-131">Xml</span><span class="sxs-lookup"><span data-stu-id="56972-131">Xml</span></span>  
5. <span data-ttu-id="56972-132">Í reitinn Kóðun skal slá inn „UTF-8“.</span><span class="sxs-lookup"><span data-stu-id="56972-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="56972-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="56972-133">UTF-8</span></span>  
6. <span data-ttu-id="56972-134">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="56972-134">Click OK.</span></span>
7. <span data-ttu-id="56972-135">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="56972-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="56972-136">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="56972-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="56972-137">Í reitnum Heiti skal færa inn ‚Skilaboð‘.</span><span class="sxs-lookup"><span data-stu-id="56972-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="56972-138">Skilaboð</span><span class="sxs-lookup"><span data-stu-id="56972-138">Message</span></span>  
10. <span data-ttu-id="56972-139">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="56972-139">Click OK.</span></span>
11. <span data-ttu-id="56972-140">Í trénu skal velja 'Xml\Message'.</span><span class="sxs-lookup"><span data-stu-id="56972-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="56972-141">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="56972-141">Click Add Element.</span></span>
13. <span data-ttu-id="56972-142">Í reitnum Heiti skal færa inn ‚ProcessingDate‘.</span><span class="sxs-lookup"><span data-stu-id="56972-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="56972-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="56972-143">ProcessingDate</span></span>  
14. <span data-ttu-id="56972-144">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="56972-144">Click OK.</span></span>
15. <span data-ttu-id="56972-145">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="56972-145">Click Add Element.</span></span>
16. <span data-ttu-id="56972-146">Í svæðið Heiti, færðu inn 'MessageId'.</span><span class="sxs-lookup"><span data-stu-id="56972-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="56972-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="56972-147">MessageId</span></span>  
17. <span data-ttu-id="56972-148">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="56972-148">Click OK.</span></span>
18. <span data-ttu-id="56972-149">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="56972-149">Click Add Element.</span></span>
19. <span data-ttu-id="56972-150">Í svæðið Heiti, færðu inn 'Greiðslur'.</span><span class="sxs-lookup"><span data-stu-id="56972-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="56972-151">Greiðslur</span><span class="sxs-lookup"><span data-stu-id="56972-151">Payments</span></span>  
20. <span data-ttu-id="56972-152">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="56972-152">Click OK.</span></span>
21. <span data-ttu-id="56972-153">Í trénu skal velja 'Xml\Message\Payments'.</span><span class="sxs-lookup"><span data-stu-id="56972-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="56972-154">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="56972-154">Click Add Element.</span></span>
23. <span data-ttu-id="56972-155">Í reitnum Heiti skal færa inn ‚Atriði.</span><span class="sxs-lookup"><span data-stu-id="56972-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="56972-156">vara</span><span class="sxs-lookup"><span data-stu-id="56972-156">Item</span></span>  
24. <span data-ttu-id="56972-157">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="56972-157">Click OK.</span></span>
25. <span data-ttu-id="56972-158">Í trénu skal velja 'Xml\Message\Payments\Item'.</span><span class="sxs-lookup"><span data-stu-id="56972-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="56972-159">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="56972-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="56972-160">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="56972-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="56972-161">Í reitnum Heiti skal færa inn ‚Id‘.</span><span class="sxs-lookup"><span data-stu-id="56972-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="56972-162">Auðkenni</span><span class="sxs-lookup"><span data-stu-id="56972-162">Id</span></span>  
29. <span data-ttu-id="56972-163">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="56972-163">Click OK.</span></span>
30. <span data-ttu-id="56972-164">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="56972-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="56972-165">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="56972-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="56972-166">Í reitnum Heiti skal færa inn ‚lánardrottinn‘.</span><span class="sxs-lookup"><span data-stu-id="56972-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="56972-167">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="56972-167">Vendor</span></span>  
33. <span data-ttu-id="56972-168">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="56972-168">Click OK.</span></span>
34. <span data-ttu-id="56972-169">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor'.</span><span class="sxs-lookup"><span data-stu-id="56972-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="56972-170">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="56972-170">Click Add Element.</span></span>
36. <span data-ttu-id="56972-171">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="56972-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="56972-172">Nafn</span><span class="sxs-lookup"><span data-stu-id="56972-172">Name</span></span>  
37. <span data-ttu-id="56972-173">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="56972-173">Click OK.</span></span>
38. <span data-ttu-id="56972-174">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="56972-174">Click Add Element.</span></span>
39. <span data-ttu-id="56972-175">Í reitnum Heiti skal færa inn ‚Banki'.</span><span class="sxs-lookup"><span data-stu-id="56972-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="56972-176">Banki</span><span class="sxs-lookup"><span data-stu-id="56972-176">Bank</span></span>  
40. <span data-ttu-id="56972-177">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="56972-177">Click OK.</span></span>
41. <span data-ttu-id="56972-178">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank'.</span><span class="sxs-lookup"><span data-stu-id="56972-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="56972-179">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="56972-179">Click Add Element.</span></span>
43. <span data-ttu-id="56972-180">Í svæðið Heiti, færðu inn 'RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="56972-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="56972-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="56972-181">RoutingNumber</span></span>  
44. <span data-ttu-id="56972-182">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="56972-182">Click OK.</span></span>
45. <span data-ttu-id="56972-183">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="56972-183">Click Add Element.</span></span>
46. <span data-ttu-id="56972-184">Í svæðið Heiti, færðu inn ‚AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="56972-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="56972-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="56972-185">AccountNumber</span></span>  
47. <span data-ttu-id="56972-186">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="56972-186">Click OK.</span></span>
48. <span data-ttu-id="56972-187">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor'.</span><span class="sxs-lookup"><span data-stu-id="56972-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="56972-188">Smellið á Afrit.</span><span class="sxs-lookup"><span data-stu-id="56972-188">Click Copy.</span></span>
50. <span data-ttu-id="56972-189">Í trénu skal velja 'Xml\Message\Payments\Item'.</span><span class="sxs-lookup"><span data-stu-id="56972-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="56972-190">Smellt er á Líma.</span><span class="sxs-lookup"><span data-stu-id="56972-190">Click Paste.</span></span>
52. <span data-ttu-id="56972-191">Í reitnum Heiti skal færa inn ‚Greiðandi‘.</span><span class="sxs-lookup"><span data-stu-id="56972-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="56972-192">Greiðandi</span><span class="sxs-lookup"><span data-stu-id="56972-192">Payer</span></span>  
53. <span data-ttu-id="56972-193">Í trénu skal velja 'Xml\Message\Payments\Item'.</span><span class="sxs-lookup"><span data-stu-id="56972-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="56972-194">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="56972-194">Click Add Element.</span></span>
55. <span data-ttu-id="56972-195">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="56972-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="56972-196">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="56972-196">Currency</span></span>  
56. <span data-ttu-id="56972-197">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="56972-197">Click OK.</span></span>
57. <span data-ttu-id="56972-198">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="56972-198">Click Add Element.</span></span>
58. <span data-ttu-id="56972-199">Í reitnum Heiti skal færa inn ‚Lýsing'.</span><span class="sxs-lookup"><span data-stu-id="56972-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="56972-200">lýsing</span><span class="sxs-lookup"><span data-stu-id="56972-200">Description</span></span>  
59. <span data-ttu-id="56972-201">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="56972-201">Click OK.</span></span>
60. <span data-ttu-id="56972-202">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="56972-202">Click Add Element.</span></span>
61. <span data-ttu-id="56972-203">Í svæðið Heiti, færðu inn ‚TransDate'.</span><span class="sxs-lookup"><span data-stu-id="56972-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="56972-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="56972-204">TransDate</span></span>  
62. <span data-ttu-id="56972-205">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="56972-205">Click OK.</span></span>
63. <span data-ttu-id="56972-206">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="56972-206">Click Add Element.</span></span>
64. <span data-ttu-id="56972-207">Í reitnum Heiti skal færa inn ‚Upphæð'.</span><span class="sxs-lookup"><span data-stu-id="56972-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="56972-208">Upphæð</span><span class="sxs-lookup"><span data-stu-id="56972-208">Amount</span></span>  
65. <span data-ttu-id="56972-209">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="56972-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="56972-210">Undirbúa íhluti sniðs fyrir vörpun í einingar gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="56972-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="56972-211">Í trénu skal velja 'Xml\Message\ProcessingDate'.</span><span class="sxs-lookup"><span data-stu-id="56972-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="56972-212">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="56972-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="56972-213">Í trénu skal velja 'Text\DateTime'.</span><span class="sxs-lookup"><span data-stu-id="56972-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="56972-214">Í svæðinu Snið 'áááá-MM-dd' skal fært inn.</span><span class="sxs-lookup"><span data-stu-id="56972-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="56972-215">áááá-MM-dd</span><span class="sxs-lookup"><span data-stu-id="56972-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="56972-216">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="56972-216">Click OK.</span></span>
6. <span data-ttu-id="56972-217">Í trénu skal velja 'Xml\Message\Payments\Item\TransDate'.</span><span class="sxs-lookup"><span data-stu-id="56972-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="56972-218">Smella á Bæta við dagsetning/tími.</span><span class="sxs-lookup"><span data-stu-id="56972-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="56972-219">Í svæðinu Snið 'áááá-MM-dd' skal fært inn.</span><span class="sxs-lookup"><span data-stu-id="56972-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="56972-220">áááá-MM-dd</span><span class="sxs-lookup"><span data-stu-id="56972-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="56972-221">Í svæði Gerð dagsetning/tími skal velja „Dagsetning“.</span><span class="sxs-lookup"><span data-stu-id="56972-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="56972-222">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="56972-222">Click OK.</span></span>
11. <span data-ttu-id="56972-223">Í trénu skal velja 'Xml\Message\MessageId'.</span><span class="sxs-lookup"><span data-stu-id="56972-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="56972-224">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="56972-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="56972-225">Í trénu skal velja ‚Texti/Strengur'.</span><span class="sxs-lookup"><span data-stu-id="56972-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="56972-226">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="56972-226">Click OK.</span></span>
15. <span data-ttu-id="56972-227">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Name'.</span><span class="sxs-lookup"><span data-stu-id="56972-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="56972-228">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="56972-228">Click Add String.</span></span>
17. <span data-ttu-id="56972-229">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="56972-229">Click OK.</span></span>
18. <span data-ttu-id="56972-230">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="56972-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="56972-231">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="56972-231">Click Add String.</span></span>
20. <span data-ttu-id="56972-232">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="56972-232">Click OK.</span></span>
21. <span data-ttu-id="56972-233">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="56972-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="56972-234">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="56972-234">Click Add String.</span></span>
23. <span data-ttu-id="56972-235">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="56972-235">Click OK.</span></span>
24. <span data-ttu-id="56972-236">Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Name'.</span><span class="sxs-lookup"><span data-stu-id="56972-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="56972-237">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="56972-237">Click Add String.</span></span>
26. <span data-ttu-id="56972-238">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="56972-238">Click OK.</span></span>
27. <span data-ttu-id="56972-239">Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="56972-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="56972-240">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="56972-240">Click Add String.</span></span>
29. <span data-ttu-id="56972-241">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="56972-241">Click OK.</span></span>
30. <span data-ttu-id="56972-242">Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="56972-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="56972-243">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="56972-243">Click Add String.</span></span>
32. <span data-ttu-id="56972-244">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="56972-244">Click OK.</span></span>
33. <span data-ttu-id="56972-245">Í trénu skal velja 'Xml\Message\Payments\Item\Currency'.</span><span class="sxs-lookup"><span data-stu-id="56972-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="56972-246">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="56972-246">Click Add String.</span></span>
35. <span data-ttu-id="56972-247">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="56972-247">Click OK.</span></span>
36. <span data-ttu-id="56972-248">Í trénu skal velja 'Xml\Message\Payments\Item\Description'.</span><span class="sxs-lookup"><span data-stu-id="56972-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="56972-249">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="56972-249">Click Add String.</span></span>
38. <span data-ttu-id="56972-250">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="56972-250">Click OK.</span></span>
39. <span data-ttu-id="56972-251">Í trénu skal velja 'Xml\Message\Payments\Item\Amount'.</span><span class="sxs-lookup"><span data-stu-id="56972-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="56972-252">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="56972-252">Click Add String.</span></span>
41. <span data-ttu-id="56972-253">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="56972-253">Click OK.</span></span>
42. <span data-ttu-id="56972-254">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="56972-254">Click Save.</span></span>
43. <span data-ttu-id="56972-255">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="56972-255">Close the page.</span></span>


