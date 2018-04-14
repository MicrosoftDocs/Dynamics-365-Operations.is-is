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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ef33fec0162e3b379bc8fe563d37a88fa35dfc85
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a><span data-ttu-id="a729a-103">Stofna skilgreiningu sniðs fyrir rafræna skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="a729a-103">Create a format configuration for electronic reporting (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a729a-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarsnið fyrir rafræna skýrslugerð (ER).</span><span class="sxs-lookup"><span data-stu-id="a729a-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="a729a-105">Þessa sniðsskilgreiningu mun skilgreina snið rafræn skjöl sem eru notaðar til að vinna greiðslur.</span><span class="sxs-lookup"><span data-stu-id="a729a-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="a729a-106">Í þessu dæmi stofnar þú skilgreiningu á sniði fyrir dæmi um fyrirtæki, í þessu dæmi Litware, Inc. Til að ljúka þessum skrefum, þarf fyrst að ljúka við skref í ferlinu „Varpa líkani á valda gagnaveitu".</span><span class="sxs-lookup"><span data-stu-id="a729a-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="a729a-107">Stofna nýja skilgreiningu á sniði</span><span class="sxs-lookup"><span data-stu-id="a729a-107">Create a new format configuration</span></span>
1. <span data-ttu-id="a729a-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="a729a-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a729a-109">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="a729a-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="a729a-110">Veljið 'Greiðslur (einfaldað líkan)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="a729a-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="a729a-111">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="a729a-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="a729a-112">Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkani PaymentModel“.</span><span class="sxs-lookup"><span data-stu-id="a729a-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="a729a-113">Í reitinn Heiti skal slá inn 'BACS (UK uppspunnið)'.</span><span class="sxs-lookup"><span data-stu-id="a729a-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="a729a-114">BACS (UK Upphugsað)</span><span class="sxs-lookup"><span data-stu-id="a729a-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="a729a-115">Færið inn 'BACS greiðslusnið lánardrottins (UK uppspunnið)' í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="a729a-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="a729a-116">Greiðslusnið lánardrottins BACS (UK Upphugsað)</span><span class="sxs-lookup"><span data-stu-id="a729a-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="a729a-117">Virkt skilgreiningarveitu er sjálfkrafa færð inn hér.</span><span class="sxs-lookup"><span data-stu-id="a729a-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="a729a-118">Þessa veitu mun geta unnið með þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="a729a-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="a729a-119">Önnur veitur er hægt að nota þetta skilgreining, en geta ekki unnið með hana.</span><span class="sxs-lookup"><span data-stu-id="a729a-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="a729a-120">Hægt er að skilgreina ákveðið snið rafrænt skjal.</span><span class="sxs-lookup"><span data-stu-id="a729a-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="a729a-121">Þetta svæði er skilið eftir autt ef óskað er að velja snið á tíma keyrslu.</span><span class="sxs-lookup"><span data-stu-id="a729a-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="a729a-122">Í reitinn Skilgreining Gagnalíkans skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="a729a-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="a729a-123">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="a729a-123">Click Create configuration.</span></span>
    * <span data-ttu-id="a729a-124">Ný Skilgreining hefur verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="a729a-124">A new configuration has been created.</span></span> <span data-ttu-id="a729a-125">Hægt er að nota sem útgáfuna drög til að vista hannað snið fyrir umsjón með rafrænum skjölum.</span><span class="sxs-lookup"><span data-stu-id="a729a-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="a729a-126">Hanna snið rafrænts skjals</span><span class="sxs-lookup"><span data-stu-id="a729a-126">Design format of electronic document</span></span>
1. <span data-ttu-id="a729a-127">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="a729a-127">Click Designer.</span></span>
2. <span data-ttu-id="a729a-128">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="a729a-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="a729a-129">Veljið 'Common\File', í trénu.</span><span class="sxs-lookup"><span data-stu-id="a729a-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="a729a-130">Í reitnum Heiti skal færa inn ‚Xml‘.</span><span class="sxs-lookup"><span data-stu-id="a729a-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="a729a-131">Xml</span><span class="sxs-lookup"><span data-stu-id="a729a-131">Xml</span></span>  
5. <span data-ttu-id="a729a-132">Í reitinn Kóðun skal slá inn „UTF-8“.</span><span class="sxs-lookup"><span data-stu-id="a729a-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="a729a-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="a729a-133">UTF-8</span></span>  
6. <span data-ttu-id="a729a-134">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a729a-134">Click OK.</span></span>
7. <span data-ttu-id="a729a-135">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="a729a-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="a729a-136">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="a729a-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="a729a-137">Í reitnum Heiti skal færa inn ‚Skilaboð‘.</span><span class="sxs-lookup"><span data-stu-id="a729a-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="a729a-138">Skilaboð</span><span class="sxs-lookup"><span data-stu-id="a729a-138">Message</span></span>  
10. <span data-ttu-id="a729a-139">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a729a-139">Click OK.</span></span>
11. <span data-ttu-id="a729a-140">Í trénu skal velja 'Xml\Message'.</span><span class="sxs-lookup"><span data-stu-id="a729a-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="a729a-141">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="a729a-141">Click Add Element.</span></span>
13. <span data-ttu-id="a729a-142">Í reitnum Heiti skal færa inn ‚ProcessingDate‘.</span><span class="sxs-lookup"><span data-stu-id="a729a-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="a729a-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="a729a-143">ProcessingDate</span></span>  
14. <span data-ttu-id="a729a-144">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a729a-144">Click OK.</span></span>
15. <span data-ttu-id="a729a-145">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="a729a-145">Click Add Element.</span></span>
16. <span data-ttu-id="a729a-146">Í svæðið Heiti, færðu inn 'MessageId'.</span><span class="sxs-lookup"><span data-stu-id="a729a-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="a729a-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="a729a-147">MessageId</span></span>  
17. <span data-ttu-id="a729a-148">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a729a-148">Click OK.</span></span>
18. <span data-ttu-id="a729a-149">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="a729a-149">Click Add Element.</span></span>
19. <span data-ttu-id="a729a-150">Í svæðið Heiti, færðu inn 'Greiðslur'.</span><span class="sxs-lookup"><span data-stu-id="a729a-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="a729a-151">Greiðslur</span><span class="sxs-lookup"><span data-stu-id="a729a-151">Payments</span></span>  
20. <span data-ttu-id="a729a-152">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a729a-152">Click OK.</span></span>
21. <span data-ttu-id="a729a-153">Í trénu skal velja 'Xml\Message\Payments'.</span><span class="sxs-lookup"><span data-stu-id="a729a-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="a729a-154">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="a729a-154">Click Add Element.</span></span>
23. <span data-ttu-id="a729a-155">Í reitnum Heiti skal færa inn ‚Atriði.</span><span class="sxs-lookup"><span data-stu-id="a729a-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="a729a-156">vara</span><span class="sxs-lookup"><span data-stu-id="a729a-156">Item</span></span>  
24. <span data-ttu-id="a729a-157">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a729a-157">Click OK.</span></span>
25. <span data-ttu-id="a729a-158">Í trénu skal velja 'Xml\Message\Payments\Item'.</span><span class="sxs-lookup"><span data-stu-id="a729a-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="a729a-159">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="a729a-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="a729a-160">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="a729a-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="a729a-161">Í reitnum Heiti skal færa inn ‚Id‘.</span><span class="sxs-lookup"><span data-stu-id="a729a-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="a729a-162">Auðkenni</span><span class="sxs-lookup"><span data-stu-id="a729a-162">Id</span></span>  
29. <span data-ttu-id="a729a-163">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a729a-163">Click OK.</span></span>
30. <span data-ttu-id="a729a-164">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="a729a-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="a729a-165">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="a729a-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="a729a-166">Í reitnum Heiti skal færa inn ‚lánardrottinn‘.</span><span class="sxs-lookup"><span data-stu-id="a729a-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="a729a-167">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="a729a-167">Vendor</span></span>  
33. <span data-ttu-id="a729a-168">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a729a-168">Click OK.</span></span>
34. <span data-ttu-id="a729a-169">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor'.</span><span class="sxs-lookup"><span data-stu-id="a729a-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="a729a-170">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="a729a-170">Click Add Element.</span></span>
36. <span data-ttu-id="a729a-171">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="a729a-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="a729a-172">Nafn</span><span class="sxs-lookup"><span data-stu-id="a729a-172">Name</span></span>  
37. <span data-ttu-id="a729a-173">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a729a-173">Click OK.</span></span>
38. <span data-ttu-id="a729a-174">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="a729a-174">Click Add Element.</span></span>
39. <span data-ttu-id="a729a-175">Í reitnum Heiti skal færa inn ‚Banki'.</span><span class="sxs-lookup"><span data-stu-id="a729a-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="a729a-176">Banki</span><span class="sxs-lookup"><span data-stu-id="a729a-176">Bank</span></span>  
40. <span data-ttu-id="a729a-177">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a729a-177">Click OK.</span></span>
41. <span data-ttu-id="a729a-178">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank'.</span><span class="sxs-lookup"><span data-stu-id="a729a-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="a729a-179">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="a729a-179">Click Add Element.</span></span>
43. <span data-ttu-id="a729a-180">Í svæðið Heiti, færðu inn 'RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="a729a-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="a729a-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="a729a-181">RoutingNumber</span></span>  
44. <span data-ttu-id="a729a-182">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a729a-182">Click OK.</span></span>
45. <span data-ttu-id="a729a-183">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="a729a-183">Click Add Element.</span></span>
46. <span data-ttu-id="a729a-184">Í svæðið Heiti, færðu inn ‚AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="a729a-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="a729a-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="a729a-185">AccountNumber</span></span>  
47. <span data-ttu-id="a729a-186">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a729a-186">Click OK.</span></span>
48. <span data-ttu-id="a729a-187">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor'.</span><span class="sxs-lookup"><span data-stu-id="a729a-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="a729a-188">Smellið á Afrit.</span><span class="sxs-lookup"><span data-stu-id="a729a-188">Click Copy.</span></span>
50. <span data-ttu-id="a729a-189">Í trénu skal velja 'Xml\Message\Payments\Item'.</span><span class="sxs-lookup"><span data-stu-id="a729a-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="a729a-190">Smellt er á Líma.</span><span class="sxs-lookup"><span data-stu-id="a729a-190">Click Paste.</span></span>
52. <span data-ttu-id="a729a-191">Í reitnum Heiti skal færa inn ‚Greiðandi‘.</span><span class="sxs-lookup"><span data-stu-id="a729a-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="a729a-192">Greiðandi</span><span class="sxs-lookup"><span data-stu-id="a729a-192">Payer</span></span>  
53. <span data-ttu-id="a729a-193">Í trénu skal velja 'Xml\Message\Payments\Item'.</span><span class="sxs-lookup"><span data-stu-id="a729a-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="a729a-194">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="a729a-194">Click Add Element.</span></span>
55. <span data-ttu-id="a729a-195">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="a729a-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="a729a-196">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="a729a-196">Currency</span></span>  
56. <span data-ttu-id="a729a-197">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a729a-197">Click OK.</span></span>
57. <span data-ttu-id="a729a-198">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="a729a-198">Click Add Element.</span></span>
58. <span data-ttu-id="a729a-199">Í reitnum Heiti skal færa inn ‚Lýsing'.</span><span class="sxs-lookup"><span data-stu-id="a729a-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="a729a-200">lýsing</span><span class="sxs-lookup"><span data-stu-id="a729a-200">Description</span></span>  
59. <span data-ttu-id="a729a-201">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a729a-201">Click OK.</span></span>
60. <span data-ttu-id="a729a-202">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="a729a-202">Click Add Element.</span></span>
61. <span data-ttu-id="a729a-203">Í svæðið Heiti, færðu inn ‚TransDate'.</span><span class="sxs-lookup"><span data-stu-id="a729a-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="a729a-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="a729a-204">TransDate</span></span>  
62. <span data-ttu-id="a729a-205">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a729a-205">Click OK.</span></span>
63. <span data-ttu-id="a729a-206">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="a729a-206">Click Add Element.</span></span>
64. <span data-ttu-id="a729a-207">Í reitnum Heiti skal færa inn ‚Upphæð'.</span><span class="sxs-lookup"><span data-stu-id="a729a-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="a729a-208">Upphæð</span><span class="sxs-lookup"><span data-stu-id="a729a-208">Amount</span></span>  
65. <span data-ttu-id="a729a-209">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a729a-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="a729a-210">Undirbúa íhluti sniðs fyrir vörpun í einingar gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="a729a-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="a729a-211">Í trénu skal velja 'Xml\Message\ProcessingDate'.</span><span class="sxs-lookup"><span data-stu-id="a729a-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="a729a-212">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="a729a-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="a729a-213">Í trénu skal velja 'Text\DateTime'.</span><span class="sxs-lookup"><span data-stu-id="a729a-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="a729a-214">Í svæðinu Snið 'áááá-MM-dd' skal fært inn.</span><span class="sxs-lookup"><span data-stu-id="a729a-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="a729a-215">áááá-MM-dd</span><span class="sxs-lookup"><span data-stu-id="a729a-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="a729a-216">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a729a-216">Click OK.</span></span>
6. <span data-ttu-id="a729a-217">Í trénu skal velja 'Xml\Message\Payments\Item\TransDate'.</span><span class="sxs-lookup"><span data-stu-id="a729a-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="a729a-218">Smella á Bæta við dagsetning/tími.</span><span class="sxs-lookup"><span data-stu-id="a729a-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="a729a-219">Í svæðinu Snið 'áááá-MM-dd' skal fært inn.</span><span class="sxs-lookup"><span data-stu-id="a729a-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="a729a-220">áááá-MM-dd</span><span class="sxs-lookup"><span data-stu-id="a729a-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="a729a-221">Í svæði Gerð dagsetning/tími skal velja „Dagsetning“.</span><span class="sxs-lookup"><span data-stu-id="a729a-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="a729a-222">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a729a-222">Click OK.</span></span>
11. <span data-ttu-id="a729a-223">Í trénu skal velja 'Xml\Message\MessageId'.</span><span class="sxs-lookup"><span data-stu-id="a729a-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="a729a-224">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="a729a-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="a729a-225">Í trénu skal velja ‚Texti/Strengur'.</span><span class="sxs-lookup"><span data-stu-id="a729a-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="a729a-226">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="a729a-226">Click OK.</span></span>
15. <span data-ttu-id="a729a-227">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Name'.</span><span class="sxs-lookup"><span data-stu-id="a729a-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="a729a-228">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="a729a-228">Click Add String.</span></span>
17. <span data-ttu-id="a729a-229">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="a729a-229">Click OK.</span></span>
18. <span data-ttu-id="a729a-230">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="a729a-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="a729a-231">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="a729a-231">Click Add String.</span></span>
20. <span data-ttu-id="a729a-232">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="a729a-232">Click OK.</span></span>
21. <span data-ttu-id="a729a-233">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="a729a-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="a729a-234">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="a729a-234">Click Add String.</span></span>
23. <span data-ttu-id="a729a-235">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="a729a-235">Click OK.</span></span>
24. <span data-ttu-id="a729a-236">Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Name'.</span><span class="sxs-lookup"><span data-stu-id="a729a-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="a729a-237">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="a729a-237">Click Add String.</span></span>
26. <span data-ttu-id="a729a-238">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="a729a-238">Click OK.</span></span>
27. <span data-ttu-id="a729a-239">Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="a729a-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="a729a-240">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="a729a-240">Click Add String.</span></span>
29. <span data-ttu-id="a729a-241">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="a729a-241">Click OK.</span></span>
30. <span data-ttu-id="a729a-242">Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="a729a-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="a729a-243">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="a729a-243">Click Add String.</span></span>
32. <span data-ttu-id="a729a-244">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="a729a-244">Click OK.</span></span>
33. <span data-ttu-id="a729a-245">Í trénu skal velja 'Xml\Message\Payments\Item\Currency'.</span><span class="sxs-lookup"><span data-stu-id="a729a-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="a729a-246">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="a729a-246">Click Add String.</span></span>
35. <span data-ttu-id="a729a-247">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="a729a-247">Click OK.</span></span>
36. <span data-ttu-id="a729a-248">Í trénu skal velja 'Xml\Message\Payments\Item\Description'.</span><span class="sxs-lookup"><span data-stu-id="a729a-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="a729a-249">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="a729a-249">Click Add String.</span></span>
38. <span data-ttu-id="a729a-250">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="a729a-250">Click OK.</span></span>
39. <span data-ttu-id="a729a-251">Í trénu skal velja 'Xml\Message\Payments\Item\Amount'.</span><span class="sxs-lookup"><span data-stu-id="a729a-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="a729a-252">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="a729a-252">Click Add String.</span></span>
41. <span data-ttu-id="a729a-253">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="a729a-253">Click OK.</span></span>
42. <span data-ttu-id="a729a-254">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a729a-254">Click Save.</span></span>
43. <span data-ttu-id="a729a-255">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a729a-255">Close the page.</span></span>


