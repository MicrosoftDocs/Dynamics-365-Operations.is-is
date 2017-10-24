--- 
title: "Hanna skýrslu til að nota fjárhagsvíddir sem gagnaveitu í rafrænni skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur."
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: c67bf235f3514a19893bcefcaae6e3bb11bbb151
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="design-a-report-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="9eaf8-103">Hanna skýrslu til að nota fjárhagsvíddir sem gagnaveitu í rafrænni skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="9eaf8-103">Design a report to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9eaf8-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="9eaf8-105">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="9eaf8-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á "Rafræn skýrslugerð notar fjárhagsvíddir sem gagnaveitu (Hluti 2: líkanavörpun) ferli.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="9eaf8-107">Hannaðu skýrslu til að birta fjárhagsvíddir</span><span class="sxs-lookup"><span data-stu-id="9eaf8-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="9eaf8-108">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="9eaf8-109">Veljið 'dæmi um líkan fyrir fjárhagsvíddir', í trénu.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="9eaf8-110">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="9eaf8-111">Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkaninu dæmalíkan fjárhagsvídda“.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="9eaf8-112">Nota líkan sem var stofnað fyrirfram sem gagnagjafa fyrir nýju skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="9eaf8-113">Í svæðið Heiti, færðu inn 'skýrsla um færslubók fjárhags'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="9eaf8-114">Í reitnum skilgriening gagnalíkans er valið „færsla“.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="9eaf8-115">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-115">Click Create configuration.</span></span>
8. <span data-ttu-id="9eaf8-116">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-116">Click Designer.</span></span>
9. <span data-ttu-id="9eaf8-117">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="9eaf8-118">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="9eaf8-119">Í reitnum Heiti skal færa inn ‚rót'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="9eaf8-120">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-120">Click OK.</span></span>
13. <span data-ttu-id="9eaf8-121">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="9eaf8-122">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="9eaf8-123">Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="9eaf8-124">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-124">Click OK.</span></span>
17. <span data-ttu-id="9eaf8-125">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="9eaf8-126">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="9eaf8-127">Í reitnum Heiti skal færa inn 'færslubók'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="9eaf8-128">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-128">Click OK.</span></span>
21. <span data-ttu-id="9eaf8-129">Í trénu, skal velja 'Root: XML Element\Journal: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="9eaf8-130">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="9eaf8-131">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="9eaf8-132">Í reitnum Heiti skal færa inn 'runa'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="9eaf8-133">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-133">Click OK.</span></span>
26. <span data-ttu-id="9eaf8-134">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="9eaf8-135">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="9eaf8-136">Í reitnum Heiti skal færa inn ‚færsla'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="9eaf8-137">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-137">Click OK.</span></span>
30. <span data-ttu-id="9eaf8-138">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="9eaf8-139">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="9eaf8-140">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="9eaf8-141">Í reitnum Heiti skal færa inn ‚fylgiskjal'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="9eaf8-142">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-142">Click OK.</span></span>
35. <span data-ttu-id="9eaf8-143">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="9eaf8-144">Í reitnum Heiti skal færa inn ‚dagsetning'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="9eaf8-145">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-145">Click OK.</span></span>
38. <span data-ttu-id="9eaf8-146">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="9eaf8-147">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="9eaf8-148">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-148">Click OK.</span></span>
41. <span data-ttu-id="9eaf8-149">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="9eaf8-150">Í svæðið Heiti, færðu inn 'Dt'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="9eaf8-151">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-151">Click OK.</span></span>
44. <span data-ttu-id="9eaf8-152">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="9eaf8-153">Í reitinn Heiti skal slá inn 'Ct'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="9eaf8-154">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-154">Click OK.</span></span>
47. <span data-ttu-id="9eaf8-155">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="9eaf8-156">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="9eaf8-157">Í reitnum Heiti skal færa inn 'víddir'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="9eaf8-158">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-158">Click OK.</span></span>
51. <span data-ttu-id="9eaf8-159">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="9eaf8-160">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="9eaf8-161">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="9eaf8-162">Í reitnum Heiti skal færa inn 'kóði'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="9eaf8-163">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-163">Click OK.</span></span>
56. <span data-ttu-id="9eaf8-164">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="9eaf8-165">Í svæðið Heiti, færðu inn 'Gildi'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="9eaf8-166">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-166">Click OK.</span></span>
59. <span data-ttu-id="9eaf8-167">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="9eaf8-168">Í svæðið Heiti, færðu inn 'lýsing'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="9eaf8-169">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="9eaf8-170">Varpa skýrslueiningum í gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="9eaf8-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="9eaf8-171">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="9eaf8-172">Í trénu, skal víkka út 'model: Data model Financial dimensions sample model'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="9eaf8-173">Í trénu, skal víkka út 'model: Data model Financial dimensions sample model\Journal: Record list'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="9eaf8-174">Í trénu, skal víkka út 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="9eaf8-175">Í trénu, skal víkka út 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="9eaf8-176">Í trénu, skal velja ' Rót: XML Element\Journal: xml-Eininguna '.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="9eaf8-177">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="9eaf8-178">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-178">Click Bind.</span></span>
9. <span data-ttu-id="9eaf8-179">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="9eaf8-180">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="9eaf8-181">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-181">Click Bind.</span></span>
12. <span data-ttu-id="9eaf8-182">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="9eaf8-183">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="9eaf8-184">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-184">Click Bind.</span></span>
15. <span data-ttu-id="9eaf8-185">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="9eaf8-186">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="9eaf8-187">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-187">Click Bind.</span></span>
18. <span data-ttu-id="9eaf8-188">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="9eaf8-189">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="9eaf8-190">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-190">Click Bind.</span></span>
21. <span data-ttu-id="9eaf8-191">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="9eaf8-192">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="9eaf8-193">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-193">Click Bind.</span></span>
24. <span data-ttu-id="9eaf8-194">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="9eaf8-195">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="9eaf8-196">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-196">Click Bind.</span></span>
27. <span data-ttu-id="9eaf8-197">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="9eaf8-198">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="9eaf8-199">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-199">Click Bind.</span></span>
30. <span data-ttu-id="9eaf8-200">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="9eaf8-201">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="9eaf8-202">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-202">Click Bind.</span></span>
33. <span data-ttu-id="9eaf8-203">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="9eaf8-204">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="9eaf8-205">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-205">Click Bind.</span></span>
36. <span data-ttu-id="9eaf8-206">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="9eaf8-207">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="9eaf8-208">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-208">Click Bind.</span></span>
39. <span data-ttu-id="9eaf8-209">Í trénu, skal velja 'Root: XML Element\Journal: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="9eaf8-210">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="9eaf8-211">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-211">Click Bind.</span></span>
42. <span data-ttu-id="9eaf8-212">Í trénu, skal velja 'Root: XML Element\Company: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="9eaf8-213">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Company: String'.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="9eaf8-214">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-214">Click Bind.</span></span>
45. <span data-ttu-id="9eaf8-215">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-215">Click Save.</span></span>
46. <span data-ttu-id="9eaf8-216">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9eaf8-216">Close the page.</span></span>


