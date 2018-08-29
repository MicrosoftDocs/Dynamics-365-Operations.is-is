--- 
title: "Búa til skilgreiningarsnið fyrir rafræna skýrslugerð (ER)"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8c11f64fd899b8be4e6c3179913787eb2c32c6c6
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---
# <a name="create-electronic-reporting-er-format-configurations"></a><span data-ttu-id="83b26-103">Búa til skilgreiningarsnið fyrir rafræna skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="83b26-103">Create Electronic reporting (ER) format configurations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="83b26-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað skilgreiningarsnið fyrir rafræna skýrslugerð (ER).</span><span class="sxs-lookup"><span data-stu-id="83b26-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="83b26-105">Þessa sniðsskilgreiningu mun skilgreina snið rafræn skjöl sem eru notaðar til að vinna greiðslur.</span><span class="sxs-lookup"><span data-stu-id="83b26-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="83b26-106">Í þessu dæmi stofnar þú skilgreiningu á sniði fyrir dæmi um fyrirtæki, í þessu dæmi Litware, Inc. Til að ljúka þessum skrefum, þarf fyrst að ljúka við skref í ferlinu „Varpa líkani á valda gagnaveitu".</span><span class="sxs-lookup"><span data-stu-id="83b26-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="83b26-107">Stofna nýja skilgreiningu á sniði</span><span class="sxs-lookup"><span data-stu-id="83b26-107">Create a new format configuration</span></span>
1. <span data-ttu-id="83b26-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="83b26-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="83b26-109">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="83b26-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="83b26-110">Veljið 'Greiðslur (einfaldað líkan)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="83b26-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="83b26-111">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="83b26-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="83b26-112">Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkani PaymentModel“.</span><span class="sxs-lookup"><span data-stu-id="83b26-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="83b26-113">Í reitinn Heiti skal slá inn 'BACS (UK uppspunnið)'.</span><span class="sxs-lookup"><span data-stu-id="83b26-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="83b26-114">BACS (UK Upphugsað)</span><span class="sxs-lookup"><span data-stu-id="83b26-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="83b26-115">Færið inn 'BACS greiðslusnið lánardrottins (UK uppspunnið)' í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="83b26-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="83b26-116">Greiðslusnið lánardrottins BACS (UK Upphugsað)</span><span class="sxs-lookup"><span data-stu-id="83b26-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="83b26-117">Virkt skilgreiningarveitu er sjálfkrafa færð inn hér.</span><span class="sxs-lookup"><span data-stu-id="83b26-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="83b26-118">Þessa veitu mun geta unnið með þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="83b26-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="83b26-119">Önnur veitur er hægt að nota þetta skilgreining, en geta ekki unnið með hana.</span><span class="sxs-lookup"><span data-stu-id="83b26-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="83b26-120">Hægt er að skilgreina ákveðið snið rafrænt skjal.</span><span class="sxs-lookup"><span data-stu-id="83b26-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="83b26-121">Þetta svæði er skilið eftir autt ef óskað er að velja snið á tíma keyrslu.</span><span class="sxs-lookup"><span data-stu-id="83b26-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="83b26-122">Í reitinn Skilgreining Gagnalíkans skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="83b26-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="83b26-123">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="83b26-123">Click Create configuration.</span></span>
    * <span data-ttu-id="83b26-124">Ný Skilgreining hefur verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="83b26-124">A new configuration has been created.</span></span> <span data-ttu-id="83b26-125">Hægt er að nota sem útgáfuna drög til að vista hannað snið fyrir umsjón með rafrænum skjölum.</span><span class="sxs-lookup"><span data-stu-id="83b26-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="83b26-126">Hanna snið rafrænts skjals</span><span class="sxs-lookup"><span data-stu-id="83b26-126">Design format of electronic document</span></span>
1. <span data-ttu-id="83b26-127">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="83b26-127">Click Designer.</span></span>
2. <span data-ttu-id="83b26-128">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="83b26-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="83b26-129">Veljið 'Common\File', í trénu.</span><span class="sxs-lookup"><span data-stu-id="83b26-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="83b26-130">Í reitnum Heiti skal færa inn ‚Xml‘.</span><span class="sxs-lookup"><span data-stu-id="83b26-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="83b26-131">Xml</span><span class="sxs-lookup"><span data-stu-id="83b26-131">Xml</span></span>  
5. <span data-ttu-id="83b26-132">Í reitinn Kóðun skal slá inn „UTF-8“.</span><span class="sxs-lookup"><span data-stu-id="83b26-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="83b26-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="83b26-133">UTF-8</span></span>  
6. <span data-ttu-id="83b26-134">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="83b26-134">Click OK.</span></span>
7. <span data-ttu-id="83b26-135">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="83b26-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="83b26-136">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="83b26-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="83b26-137">Í reitnum Heiti skal færa inn ‚Skilaboð‘.</span><span class="sxs-lookup"><span data-stu-id="83b26-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="83b26-138">Skilaboð</span><span class="sxs-lookup"><span data-stu-id="83b26-138">Message</span></span>  
10. <span data-ttu-id="83b26-139">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="83b26-139">Click OK.</span></span>
11. <span data-ttu-id="83b26-140">Í trénu skal velja 'Xml\Message'.</span><span class="sxs-lookup"><span data-stu-id="83b26-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="83b26-141">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="83b26-141">Click Add Element.</span></span>
13. <span data-ttu-id="83b26-142">Í reitnum Heiti skal færa inn ‚ProcessingDate‘.</span><span class="sxs-lookup"><span data-stu-id="83b26-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="83b26-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="83b26-143">ProcessingDate</span></span>  
14. <span data-ttu-id="83b26-144">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="83b26-144">Click OK.</span></span>
15. <span data-ttu-id="83b26-145">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="83b26-145">Click Add Element.</span></span>
16. <span data-ttu-id="83b26-146">Í svæðið Heiti, færðu inn 'MessageId'.</span><span class="sxs-lookup"><span data-stu-id="83b26-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="83b26-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="83b26-147">MessageId</span></span>  
17. <span data-ttu-id="83b26-148">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="83b26-148">Click OK.</span></span>
18. <span data-ttu-id="83b26-149">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="83b26-149">Click Add Element.</span></span>
19. <span data-ttu-id="83b26-150">Í svæðið Heiti, færðu inn 'Greiðslur'.</span><span class="sxs-lookup"><span data-stu-id="83b26-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="83b26-151">Greiðslur</span><span class="sxs-lookup"><span data-stu-id="83b26-151">Payments</span></span>  
20. <span data-ttu-id="83b26-152">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="83b26-152">Click OK.</span></span>
21. <span data-ttu-id="83b26-153">Í trénu skal velja 'Xml\Message\Payments'.</span><span class="sxs-lookup"><span data-stu-id="83b26-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="83b26-154">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="83b26-154">Click Add Element.</span></span>
23. <span data-ttu-id="83b26-155">Í reitnum Heiti skal færa inn ‚Atriði.</span><span class="sxs-lookup"><span data-stu-id="83b26-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="83b26-156">vara</span><span class="sxs-lookup"><span data-stu-id="83b26-156">Item</span></span>  
24. <span data-ttu-id="83b26-157">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="83b26-157">Click OK.</span></span>
25. <span data-ttu-id="83b26-158">Í trénu skal velja 'Xml\Message\Payments\Item'.</span><span class="sxs-lookup"><span data-stu-id="83b26-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="83b26-159">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="83b26-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="83b26-160">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="83b26-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="83b26-161">Í reitnum Heiti skal færa inn ‚Id‘.</span><span class="sxs-lookup"><span data-stu-id="83b26-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="83b26-162">Auðkenni</span><span class="sxs-lookup"><span data-stu-id="83b26-162">Id</span></span>  
29. <span data-ttu-id="83b26-163">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="83b26-163">Click OK.</span></span>
30. <span data-ttu-id="83b26-164">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="83b26-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="83b26-165">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="83b26-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="83b26-166">Í reitnum Heiti skal færa inn ‚lánardrottinn‘.</span><span class="sxs-lookup"><span data-stu-id="83b26-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="83b26-167">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="83b26-167">Vendor</span></span>  
33. <span data-ttu-id="83b26-168">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="83b26-168">Click OK.</span></span>
34. <span data-ttu-id="83b26-169">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor'.</span><span class="sxs-lookup"><span data-stu-id="83b26-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="83b26-170">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="83b26-170">Click Add Element.</span></span>
36. <span data-ttu-id="83b26-171">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="83b26-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="83b26-172">Nafn</span><span class="sxs-lookup"><span data-stu-id="83b26-172">Name</span></span>  
37. <span data-ttu-id="83b26-173">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="83b26-173">Click OK.</span></span>
38. <span data-ttu-id="83b26-174">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="83b26-174">Click Add Element.</span></span>
39. <span data-ttu-id="83b26-175">Í reitnum Heiti skal færa inn ‚Banki'.</span><span class="sxs-lookup"><span data-stu-id="83b26-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="83b26-176">Banki</span><span class="sxs-lookup"><span data-stu-id="83b26-176">Bank</span></span>  
40. <span data-ttu-id="83b26-177">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="83b26-177">Click OK.</span></span>
41. <span data-ttu-id="83b26-178">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank'.</span><span class="sxs-lookup"><span data-stu-id="83b26-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="83b26-179">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="83b26-179">Click Add Element.</span></span>
43. <span data-ttu-id="83b26-180">Í svæðið Heiti, færðu inn 'RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="83b26-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="83b26-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="83b26-181">RoutingNumber</span></span>  
44. <span data-ttu-id="83b26-182">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="83b26-182">Click OK.</span></span>
45. <span data-ttu-id="83b26-183">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="83b26-183">Click Add Element.</span></span>
46. <span data-ttu-id="83b26-184">Í svæðið Heiti, færðu inn ‚AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="83b26-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="83b26-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="83b26-185">AccountNumber</span></span>  
47. <span data-ttu-id="83b26-186">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="83b26-186">Click OK.</span></span>
48. <span data-ttu-id="83b26-187">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor'.</span><span class="sxs-lookup"><span data-stu-id="83b26-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="83b26-188">Smellið á Afrit.</span><span class="sxs-lookup"><span data-stu-id="83b26-188">Click Copy.</span></span>
50. <span data-ttu-id="83b26-189">Í trénu skal velja 'Xml\Message\Payments\Item'.</span><span class="sxs-lookup"><span data-stu-id="83b26-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="83b26-190">Smellt er á Líma.</span><span class="sxs-lookup"><span data-stu-id="83b26-190">Click Paste.</span></span>
52. <span data-ttu-id="83b26-191">Í reitnum Heiti skal færa inn ‚Greiðandi‘.</span><span class="sxs-lookup"><span data-stu-id="83b26-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="83b26-192">Greiðandi</span><span class="sxs-lookup"><span data-stu-id="83b26-192">Payer</span></span>  
53. <span data-ttu-id="83b26-193">Í trénu skal velja 'Xml\Message\Payments\Item'.</span><span class="sxs-lookup"><span data-stu-id="83b26-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="83b26-194">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="83b26-194">Click Add Element.</span></span>
55. <span data-ttu-id="83b26-195">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="83b26-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="83b26-196">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="83b26-196">Currency</span></span>  
56. <span data-ttu-id="83b26-197">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="83b26-197">Click OK.</span></span>
57. <span data-ttu-id="83b26-198">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="83b26-198">Click Add Element.</span></span>
58. <span data-ttu-id="83b26-199">Í reitnum Heiti skal færa inn ‚Lýsing'.</span><span class="sxs-lookup"><span data-stu-id="83b26-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="83b26-200">lýsing</span><span class="sxs-lookup"><span data-stu-id="83b26-200">Description</span></span>  
59. <span data-ttu-id="83b26-201">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="83b26-201">Click OK.</span></span>
60. <span data-ttu-id="83b26-202">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="83b26-202">Click Add Element.</span></span>
61. <span data-ttu-id="83b26-203">Í svæðið Heiti, færðu inn ‚TransDate'.</span><span class="sxs-lookup"><span data-stu-id="83b26-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="83b26-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="83b26-204">TransDate</span></span>  
62. <span data-ttu-id="83b26-205">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="83b26-205">Click OK.</span></span>
63. <span data-ttu-id="83b26-206">Smella á bæta Við einingu.</span><span class="sxs-lookup"><span data-stu-id="83b26-206">Click Add Element.</span></span>
64. <span data-ttu-id="83b26-207">Í reitnum Heiti skal færa inn ‚Upphæð'.</span><span class="sxs-lookup"><span data-stu-id="83b26-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="83b26-208">Upphæð</span><span class="sxs-lookup"><span data-stu-id="83b26-208">Amount</span></span>  
65. <span data-ttu-id="83b26-209">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="83b26-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="83b26-210">Undirbúa íhluti sniðs fyrir vörpun í einingar gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="83b26-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="83b26-211">Í trénu skal velja 'Xml\Message\ProcessingDate'.</span><span class="sxs-lookup"><span data-stu-id="83b26-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="83b26-212">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="83b26-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="83b26-213">Í trénu skal velja 'Text\DateTime'.</span><span class="sxs-lookup"><span data-stu-id="83b26-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="83b26-214">Í svæðinu Snið 'áááá-MM-dd' skal fært inn.</span><span class="sxs-lookup"><span data-stu-id="83b26-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="83b26-215">áááá-MM-dd</span><span class="sxs-lookup"><span data-stu-id="83b26-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="83b26-216">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="83b26-216">Click OK.</span></span>
6. <span data-ttu-id="83b26-217">Í trénu skal velja 'Xml\Message\Payments\Item\TransDate'.</span><span class="sxs-lookup"><span data-stu-id="83b26-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="83b26-218">Smella á Bæta við dagsetning/tími.</span><span class="sxs-lookup"><span data-stu-id="83b26-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="83b26-219">Í svæðinu Snið 'áááá-MM-dd' skal fært inn.</span><span class="sxs-lookup"><span data-stu-id="83b26-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="83b26-220">áááá-MM-dd</span><span class="sxs-lookup"><span data-stu-id="83b26-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="83b26-221">Í svæði Gerð dagsetning/tími skal velja „Dagsetning“.</span><span class="sxs-lookup"><span data-stu-id="83b26-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="83b26-222">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="83b26-222">Click OK.</span></span>
11. <span data-ttu-id="83b26-223">Í trénu skal velja 'Xml\Message\MessageId'.</span><span class="sxs-lookup"><span data-stu-id="83b26-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="83b26-224">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="83b26-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="83b26-225">Í trénu skal velja ‚Texti/Strengur'.</span><span class="sxs-lookup"><span data-stu-id="83b26-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="83b26-226">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="83b26-226">Click OK.</span></span>
15. <span data-ttu-id="83b26-227">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Name'.</span><span class="sxs-lookup"><span data-stu-id="83b26-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="83b26-228">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="83b26-228">Click Add String.</span></span>
17. <span data-ttu-id="83b26-229">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="83b26-229">Click OK.</span></span>
18. <span data-ttu-id="83b26-230">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="83b26-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="83b26-231">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="83b26-231">Click Add String.</span></span>
20. <span data-ttu-id="83b26-232">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="83b26-232">Click OK.</span></span>
21. <span data-ttu-id="83b26-233">Í trénu skal velja 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="83b26-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="83b26-234">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="83b26-234">Click Add String.</span></span>
23. <span data-ttu-id="83b26-235">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="83b26-235">Click OK.</span></span>
24. <span data-ttu-id="83b26-236">Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Name'.</span><span class="sxs-lookup"><span data-stu-id="83b26-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="83b26-237">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="83b26-237">Click Add String.</span></span>
26. <span data-ttu-id="83b26-238">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="83b26-238">Click OK.</span></span>
27. <span data-ttu-id="83b26-239">Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="83b26-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="83b26-240">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="83b26-240">Click Add String.</span></span>
29. <span data-ttu-id="83b26-241">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="83b26-241">Click OK.</span></span>
30. <span data-ttu-id="83b26-242">Í trénu skal velja 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="83b26-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="83b26-243">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="83b26-243">Click Add String.</span></span>
32. <span data-ttu-id="83b26-244">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="83b26-244">Click OK.</span></span>
33. <span data-ttu-id="83b26-245">Í trénu skal velja 'Xml\Message\Payments\Item\Currency'.</span><span class="sxs-lookup"><span data-stu-id="83b26-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="83b26-246">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="83b26-246">Click Add String.</span></span>
35. <span data-ttu-id="83b26-247">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="83b26-247">Click OK.</span></span>
36. <span data-ttu-id="83b26-248">Í trénu skal velja 'Xml\Message\Payments\Item\Description'.</span><span class="sxs-lookup"><span data-stu-id="83b26-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="83b26-249">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="83b26-249">Click Add String.</span></span>
38. <span data-ttu-id="83b26-250">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="83b26-250">Click OK.</span></span>
39. <span data-ttu-id="83b26-251">Í trénu skal velja 'Xml\Message\Payments\Item\Amount'.</span><span class="sxs-lookup"><span data-stu-id="83b26-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="83b26-252">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="83b26-252">Click Add String.</span></span>
41. <span data-ttu-id="83b26-253">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="83b26-253">Click OK.</span></span>
42. <span data-ttu-id="83b26-254">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="83b26-254">Click Save.</span></span>
43. <span data-ttu-id="83b26-255">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="83b26-255">Close the page.</span></span>


