---
title: Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 3 - hanna skýrslu)
description: Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cef61787e50561eaac4fd52741ab5f90d9c4171d
ms.sourcegitcommit: d9125c20b21459076e4fd92fd9ebfe2e53a0431b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406498"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="6b525-103">Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 3 - hanna skýrslu)</span><span class="sxs-lookup"><span data-stu-id="6b525-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6b525-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="6b525-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="6b525-105">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="6b525-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="6b525-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð notar fjárhagsvíddir sem gagnaveitu (Hluti 2: líkanavörpun)”.</span><span class="sxs-lookup"><span data-stu-id="6b525-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="6b525-107">Hannaðu skýrslu til að birta fjárhagsvíddir</span><span class="sxs-lookup"><span data-stu-id="6b525-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="6b525-108">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="6b525-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="6b525-109">Veljið 'dæmi um líkan fyrir fjárhagsvíddir', í trénu.</span><span class="sxs-lookup"><span data-stu-id="6b525-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="6b525-110">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="6b525-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="6b525-111">Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkaninu dæmalíkan fjárhagsvídda“.</span><span class="sxs-lookup"><span data-stu-id="6b525-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="6b525-112">Nota líkan sem var stofnað fyrirfram sem gagnagjafa fyrir nýju skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="6b525-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="6b525-113">Í svæðið Heiti, færðu inn 'skýrsla um færslubók fjárhags'.</span><span class="sxs-lookup"><span data-stu-id="6b525-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="6b525-114">Í reitnum skilgriening gagnalíkans er valið „færsla“.</span><span class="sxs-lookup"><span data-stu-id="6b525-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="6b525-115">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="6b525-115">Click Create configuration.</span></span>
8. <span data-ttu-id="6b525-116">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="6b525-116">Click Designer.</span></span>
9. <span data-ttu-id="6b525-117">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="6b525-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="6b525-118">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="6b525-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="6b525-119">Í reitnum Heiti skal færa inn ‚rót'.</span><span class="sxs-lookup"><span data-stu-id="6b525-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="6b525-120">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="6b525-120">Click OK.</span></span>
13. <span data-ttu-id="6b525-121">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="6b525-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="6b525-122">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="6b525-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="6b525-123">Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.</span><span class="sxs-lookup"><span data-stu-id="6b525-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="6b525-124">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="6b525-124">Click OK.</span></span>
17. <span data-ttu-id="6b525-125">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="6b525-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="6b525-126">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="6b525-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="6b525-127">Í reitnum Heiti skal færa inn 'færslubók'.</span><span class="sxs-lookup"><span data-stu-id="6b525-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="6b525-128">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="6b525-128">Click OK.</span></span>
21. <span data-ttu-id="6b525-129">Í trénu, skal velja 'Root: XML Element\Journal: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="6b525-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="6b525-130">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="6b525-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="6b525-131">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="6b525-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="6b525-132">Í reitnum Heiti skal færa inn 'runa'.</span><span class="sxs-lookup"><span data-stu-id="6b525-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="6b525-133">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="6b525-133">Click OK.</span></span>
26. <span data-ttu-id="6b525-134">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="6b525-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="6b525-135">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="6b525-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="6b525-136">Í reitnum Heiti skal færa inn ‚færsla'.</span><span class="sxs-lookup"><span data-stu-id="6b525-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="6b525-137">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="6b525-137">Click OK.</span></span>
30. <span data-ttu-id="6b525-138">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="6b525-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="6b525-139">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="6b525-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="6b525-140">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="6b525-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="6b525-141">Í reitnum Heiti skal færa inn ‚fylgiskjal'.</span><span class="sxs-lookup"><span data-stu-id="6b525-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="6b525-142">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6b525-142">Click OK.</span></span>
35. <span data-ttu-id="6b525-143">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="6b525-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="6b525-144">Í reitnum Heiti skal færa inn ‚dagsetning'.</span><span class="sxs-lookup"><span data-stu-id="6b525-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="6b525-145">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6b525-145">Click OK.</span></span>
38. <span data-ttu-id="6b525-146">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="6b525-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="6b525-147">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="6b525-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="6b525-148">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6b525-148">Click OK.</span></span>
41. <span data-ttu-id="6b525-149">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="6b525-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="6b525-150">Í svæðið Heiti, færðu inn 'Dt'.</span><span class="sxs-lookup"><span data-stu-id="6b525-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="6b525-151">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6b525-151">Click OK.</span></span>
44. <span data-ttu-id="6b525-152">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="6b525-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="6b525-153">Í reitinn Heiti skal slá inn 'Ct'.</span><span class="sxs-lookup"><span data-stu-id="6b525-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="6b525-154">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6b525-154">Click OK.</span></span>
47. <span data-ttu-id="6b525-155">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="6b525-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="6b525-156">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="6b525-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="6b525-157">Í reitnum Heiti skal færa inn 'víddir'.</span><span class="sxs-lookup"><span data-stu-id="6b525-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="6b525-158">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="6b525-158">Click OK.</span></span>
51. <span data-ttu-id="6b525-159">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="6b525-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="6b525-160">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="6b525-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="6b525-161">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="6b525-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="6b525-162">Í reitnum Heiti skal færa inn 'kóði'.</span><span class="sxs-lookup"><span data-stu-id="6b525-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="6b525-163">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6b525-163">Click OK.</span></span>
56. <span data-ttu-id="6b525-164">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="6b525-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="6b525-165">Í svæðið Heiti, færðu inn 'Gildi'.</span><span class="sxs-lookup"><span data-stu-id="6b525-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="6b525-166">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6b525-166">Click OK.</span></span>
59. <span data-ttu-id="6b525-167">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="6b525-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="6b525-168">Í svæðið Heiti, færðu inn 'lýsing'.</span><span class="sxs-lookup"><span data-stu-id="6b525-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="6b525-169">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="6b525-169">Click OK.</span></span>
<span data-ttu-id="6b525-170">![Síða aðgerðarhönnuðar rafrænnar skýrslugerðar](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="6b525-170">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="6b525-171">Varpa skýrslueiningum í gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="6b525-171">Map report elements to data sources</span></span>
1. <span data-ttu-id="6b525-172">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="6b525-172">Click the Mapping tab.</span></span>
2. <span data-ttu-id="6b525-173">Í trénu, skal víkka út 'model: Data model Financial dimensions sample model'.</span><span class="sxs-lookup"><span data-stu-id="6b525-173">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="6b525-174">Í trénu, skal víkka út 'model: Data model Financial dimensions sample model\Journal: Record list'.</span><span class="sxs-lookup"><span data-stu-id="6b525-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="6b525-175">Í trénu, skal víkka út 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span><span class="sxs-lookup"><span data-stu-id="6b525-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="6b525-176">Í trénu, skal víkka út 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span><span class="sxs-lookup"><span data-stu-id="6b525-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="6b525-177">Í trénu, skal velja ' Rót: XML Element\Journal: xml-Eininguna '.</span><span class="sxs-lookup"><span data-stu-id="6b525-177">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="6b525-178">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span><span class="sxs-lookup"><span data-stu-id="6b525-178">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="6b525-179">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6b525-179">Click Bind.</span></span>
9. <span data-ttu-id="6b525-180">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="6b525-180">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="6b525-181">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span><span class="sxs-lookup"><span data-stu-id="6b525-181">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="6b525-182">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6b525-182">Click Bind.</span></span>
12. <span data-ttu-id="6b525-183">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="6b525-183">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="6b525-184">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span><span class="sxs-lookup"><span data-stu-id="6b525-184">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="6b525-185">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6b525-185">Click Bind.</span></span>
15. <span data-ttu-id="6b525-186">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span><span class="sxs-lookup"><span data-stu-id="6b525-186">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="6b525-187">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="6b525-187">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="6b525-188">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6b525-188">Click Bind.</span></span>
18. <span data-ttu-id="6b525-189">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="6b525-189">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="6b525-190">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span><span class="sxs-lookup"><span data-stu-id="6b525-190">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="6b525-191">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6b525-191">Click Bind.</span></span>
21. <span data-ttu-id="6b525-192">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="6b525-192">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="6b525-193">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span><span class="sxs-lookup"><span data-stu-id="6b525-193">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="6b525-194">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6b525-194">Click Bind.</span></span>
24. <span data-ttu-id="6b525-195">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="6b525-195">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="6b525-196">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span><span class="sxs-lookup"><span data-stu-id="6b525-196">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="6b525-197">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6b525-197">Click Bind.</span></span>
27. <span data-ttu-id="6b525-198">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="6b525-198">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="6b525-199">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span><span class="sxs-lookup"><span data-stu-id="6b525-199">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="6b525-200">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6b525-200">Click Bind.</span></span>
30. <span data-ttu-id="6b525-201">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="6b525-201">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="6b525-202">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span><span class="sxs-lookup"><span data-stu-id="6b525-202">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="6b525-203">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6b525-203">Click Bind.</span></span>
33. <span data-ttu-id="6b525-204">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="6b525-204">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="6b525-205">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span><span class="sxs-lookup"><span data-stu-id="6b525-205">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="6b525-206">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6b525-206">Click Bind.</span></span>
36. <span data-ttu-id="6b525-207">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="6b525-207">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="6b525-208">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span><span class="sxs-lookup"><span data-stu-id="6b525-208">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="6b525-209">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6b525-209">Click Bind.</span></span>
39. <span data-ttu-id="6b525-210">Í trénu, skal velja 'Root: XML Element\Journal: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="6b525-210">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="6b525-211">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list'.</span><span class="sxs-lookup"><span data-stu-id="6b525-211">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="6b525-212">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6b525-212">Click Bind.</span></span>
42. <span data-ttu-id="6b525-213">Í trénu, skal velja 'Root: XML Element\Company: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="6b525-213">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="6b525-214">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Company: String'.</span><span class="sxs-lookup"><span data-stu-id="6b525-214">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="6b525-215">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6b525-215">Click Bind.</span></span>
45. <span data-ttu-id="6b525-216">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="6b525-216">Click Save.</span></span>
46. <span data-ttu-id="6b525-217">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6b525-217">Close the page.</span></span>
<span data-ttu-id="6b525-218">![Síða aðgerðarhönnuðar rafrænnar skýrslugerðar](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="6b525-218">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

