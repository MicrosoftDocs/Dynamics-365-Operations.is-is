---
title: Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 3 - hanna skýrslu)
description: Þetta efni útskýrir hvernig á að skilgreina líkan rafrænnar skýrslugerðar til að nota fjárhagsvíddir sem gagnagjafa fyrir skýrslur rafrænnar skýrslugerðar. (Hluti 3)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9594a12c28109d80c6ee07a9ee38f4923963dca
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565239"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="7af38-104">Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 3 - hanna skýrslu)</span><span class="sxs-lookup"><span data-stu-id="7af38-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7af38-105">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="7af38-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="7af38-106">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="7af38-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="7af38-107">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð notar fjárhagsvíddir sem gagnaveitu (Hluti 2: líkanavörpun)”.</span><span class="sxs-lookup"><span data-stu-id="7af38-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="7af38-108">Hannaðu skýrslu til að birta fjárhagsvíddir</span><span class="sxs-lookup"><span data-stu-id="7af38-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="7af38-109">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="7af38-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="7af38-110">Veljið 'dæmi um líkan fyrir fjárhagsvíddir', í trénu.</span><span class="sxs-lookup"><span data-stu-id="7af38-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="7af38-111">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="7af38-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="7af38-112">Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkaninu dæmalíkan fjárhagsvídda“.</span><span class="sxs-lookup"><span data-stu-id="7af38-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="7af38-113">Nota líkan sem var stofnað fyrirfram sem gagnagjafa fyrir nýju skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="7af38-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="7af38-114">Í svæðið Heiti, færðu inn 'skýrsla um færslubók fjárhags'.</span><span class="sxs-lookup"><span data-stu-id="7af38-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="7af38-115">Í reitnum skilgriening gagnalíkans er valið „færsla“.</span><span class="sxs-lookup"><span data-stu-id="7af38-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="7af38-116">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="7af38-116">Click Create configuration.</span></span>
8. <span data-ttu-id="7af38-117">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="7af38-117">Click Designer.</span></span>
9. <span data-ttu-id="7af38-118">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7af38-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="7af38-119">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="7af38-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="7af38-120">Í reitnum Heiti skal færa inn ‚rót'.</span><span class="sxs-lookup"><span data-stu-id="7af38-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="7af38-121">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="7af38-121">Click OK.</span></span>
13. <span data-ttu-id="7af38-122">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7af38-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="7af38-123">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="7af38-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="7af38-124">Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.</span><span class="sxs-lookup"><span data-stu-id="7af38-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="7af38-125">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="7af38-125">Click OK.</span></span>
17. <span data-ttu-id="7af38-126">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7af38-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="7af38-127">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="7af38-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="7af38-128">Í reitnum Heiti skal færa inn 'færslubók'.</span><span class="sxs-lookup"><span data-stu-id="7af38-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="7af38-129">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="7af38-129">Click OK.</span></span>
21. <span data-ttu-id="7af38-130">Í trénu, skal velja 'Root: XML Element\Journal: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="7af38-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="7af38-131">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7af38-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="7af38-132">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="7af38-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="7af38-133">Í reitnum Heiti skal færa inn 'runa'.</span><span class="sxs-lookup"><span data-stu-id="7af38-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="7af38-134">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="7af38-134">Click OK.</span></span>
26. <span data-ttu-id="7af38-135">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7af38-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="7af38-136">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="7af38-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="7af38-137">Í reitnum Heiti skal færa inn ‚færsla'.</span><span class="sxs-lookup"><span data-stu-id="7af38-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="7af38-138">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="7af38-138">Click OK.</span></span>
30. <span data-ttu-id="7af38-139">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="7af38-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="7af38-140">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7af38-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="7af38-141">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="7af38-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="7af38-142">Í reitnum Heiti skal færa inn ‚fylgiskjal'.</span><span class="sxs-lookup"><span data-stu-id="7af38-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="7af38-143">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7af38-143">Click OK.</span></span>
35. <span data-ttu-id="7af38-144">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="7af38-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="7af38-145">Í reitnum Heiti skal færa inn ‚dagsetning'.</span><span class="sxs-lookup"><span data-stu-id="7af38-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="7af38-146">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7af38-146">Click OK.</span></span>
38. <span data-ttu-id="7af38-147">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="7af38-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="7af38-148">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="7af38-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="7af38-149">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7af38-149">Click OK.</span></span>
41. <span data-ttu-id="7af38-150">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="7af38-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="7af38-151">Í svæðið Heiti, færðu inn 'Dt'.</span><span class="sxs-lookup"><span data-stu-id="7af38-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="7af38-152">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7af38-152">Click OK.</span></span>
44. <span data-ttu-id="7af38-153">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="7af38-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="7af38-154">Í reitinn Heiti skal slá inn 'Ct'.</span><span class="sxs-lookup"><span data-stu-id="7af38-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="7af38-155">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7af38-155">Click OK.</span></span>
47. <span data-ttu-id="7af38-156">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7af38-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="7af38-157">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="7af38-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="7af38-158">Í reitnum Heiti skal færa inn 'víddir'.</span><span class="sxs-lookup"><span data-stu-id="7af38-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="7af38-159">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="7af38-159">Click OK.</span></span>
51. <span data-ttu-id="7af38-160">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="7af38-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="7af38-161">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="7af38-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="7af38-162">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="7af38-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="7af38-163">Í reitnum Heiti skal færa inn 'kóði'.</span><span class="sxs-lookup"><span data-stu-id="7af38-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="7af38-164">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7af38-164">Click OK.</span></span>
56. <span data-ttu-id="7af38-165">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="7af38-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="7af38-166">Í svæðið Heiti, færðu inn 'Gildi'.</span><span class="sxs-lookup"><span data-stu-id="7af38-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="7af38-167">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7af38-167">Click OK.</span></span>
59. <span data-ttu-id="7af38-168">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="7af38-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="7af38-169">Í svæðið Heiti, færðu inn 'lýsing'.</span><span class="sxs-lookup"><span data-stu-id="7af38-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="7af38-170">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="7af38-170">Click OK.</span></span>
<span data-ttu-id="7af38-171">![Síða aðgerðarhönnuðar rafrænnar skýrslugerðar](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="7af38-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="7af38-172">Varpa skýrslueiningum í gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="7af38-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="7af38-173">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="7af38-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="7af38-174">Í trénu, skal víkka út 'model: Data model Financial dimensions sample model'.</span><span class="sxs-lookup"><span data-stu-id="7af38-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="7af38-175">Í trénu, skal víkka út 'model: Data model Financial dimensions sample model\Journal: Record list'.</span><span class="sxs-lookup"><span data-stu-id="7af38-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="7af38-176">Í trénu, skal víkka út 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span><span class="sxs-lookup"><span data-stu-id="7af38-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="7af38-177">Í trénu, skal víkka út 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span><span class="sxs-lookup"><span data-stu-id="7af38-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="7af38-178">Í trénu, skal velja ' Rót: XML Element\Journal: xml-Eininguna '.</span><span class="sxs-lookup"><span data-stu-id="7af38-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="7af38-179">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span><span class="sxs-lookup"><span data-stu-id="7af38-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="7af38-180">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="7af38-180">Click Bind.</span></span>
9. <span data-ttu-id="7af38-181">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="7af38-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="7af38-182">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span><span class="sxs-lookup"><span data-stu-id="7af38-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="7af38-183">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="7af38-183">Click Bind.</span></span>
12. <span data-ttu-id="7af38-184">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="7af38-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="7af38-185">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span><span class="sxs-lookup"><span data-stu-id="7af38-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="7af38-186">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="7af38-186">Click Bind.</span></span>
15. <span data-ttu-id="7af38-187">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span><span class="sxs-lookup"><span data-stu-id="7af38-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="7af38-188">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="7af38-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="7af38-189">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="7af38-189">Click Bind.</span></span>
18. <span data-ttu-id="7af38-190">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="7af38-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="7af38-191">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span><span class="sxs-lookup"><span data-stu-id="7af38-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="7af38-192">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="7af38-192">Click Bind.</span></span>
21. <span data-ttu-id="7af38-193">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="7af38-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="7af38-194">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span><span class="sxs-lookup"><span data-stu-id="7af38-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="7af38-195">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="7af38-195">Click Bind.</span></span>
24. <span data-ttu-id="7af38-196">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="7af38-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="7af38-197">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span><span class="sxs-lookup"><span data-stu-id="7af38-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="7af38-198">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="7af38-198">Click Bind.</span></span>
27. <span data-ttu-id="7af38-199">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="7af38-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="7af38-200">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span><span class="sxs-lookup"><span data-stu-id="7af38-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="7af38-201">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="7af38-201">Click Bind.</span></span>
30. <span data-ttu-id="7af38-202">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="7af38-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="7af38-203">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span><span class="sxs-lookup"><span data-stu-id="7af38-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="7af38-204">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="7af38-204">Click Bind.</span></span>
33. <span data-ttu-id="7af38-205">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="7af38-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="7af38-206">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span><span class="sxs-lookup"><span data-stu-id="7af38-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="7af38-207">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="7af38-207">Click Bind.</span></span>
36. <span data-ttu-id="7af38-208">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="7af38-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="7af38-209">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span><span class="sxs-lookup"><span data-stu-id="7af38-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="7af38-210">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="7af38-210">Click Bind.</span></span>
39. <span data-ttu-id="7af38-211">Í trénu, skal velja 'Root: XML Element\Journal: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="7af38-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="7af38-212">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list'.</span><span class="sxs-lookup"><span data-stu-id="7af38-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="7af38-213">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="7af38-213">Click Bind.</span></span>
42. <span data-ttu-id="7af38-214">Í trénu, skal velja 'Root: XML Element\Company: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="7af38-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="7af38-215">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Company: String'.</span><span class="sxs-lookup"><span data-stu-id="7af38-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="7af38-216">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="7af38-216">Click Bind.</span></span>
45. <span data-ttu-id="7af38-217">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="7af38-217">Click Save.</span></span>
46. <span data-ttu-id="7af38-218">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7af38-218">Close the page.</span></span>
<span data-ttu-id="7af38-219">![Síða aðgerðarhönnuðar rafrænnar skýrslugerðar](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="7af38-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]