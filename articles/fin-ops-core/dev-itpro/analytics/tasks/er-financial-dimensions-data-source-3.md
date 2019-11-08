---
title: Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 3 - hanna skýrslu)
description: Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 77f1f2d6390a1d99b22d6eab9f0cae30f9760cc8
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550580"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="b3d05-103">Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 3 - hanna skýrslu)</span><span class="sxs-lookup"><span data-stu-id="b3d05-103">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b3d05-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="b3d05-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="b3d05-105">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="b3d05-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="b3d05-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á "Rafræn skýrslugerð notar fjárhagsvíddir sem gagnaveitu (Hluti 2: líkanavörpun) ferli.</span><span class="sxs-lookup"><span data-stu-id="b3d05-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="b3d05-107">Hannaðu skýrslu til að birta fjárhagsvíddir</span><span class="sxs-lookup"><span data-stu-id="b3d05-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="b3d05-108">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="b3d05-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="b3d05-109">Veljið 'dæmi um líkan fyrir fjárhagsvíddir', í trénu.</span><span class="sxs-lookup"><span data-stu-id="b3d05-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="b3d05-110">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="b3d05-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="b3d05-111">Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkaninu dæmalíkan fjárhagsvídda“.</span><span class="sxs-lookup"><span data-stu-id="b3d05-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="b3d05-112">Nota líkan sem var stofnað fyrirfram sem gagnagjafa fyrir nýju skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="b3d05-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="b3d05-113">Í svæðið Heiti, færðu inn 'skýrsla um færslubók fjárhags'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="b3d05-114">Í reitnum skilgriening gagnalíkans er valið „færsla“.</span><span class="sxs-lookup"><span data-stu-id="b3d05-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="b3d05-115">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="b3d05-115">Click Create configuration.</span></span>
8. <span data-ttu-id="b3d05-116">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="b3d05-116">Click Designer.</span></span>
9. <span data-ttu-id="b3d05-117">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b3d05-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="b3d05-118">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="b3d05-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="b3d05-119">Í reitnum Heiti skal færa inn ‚rót'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="b3d05-120">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="b3d05-120">Click OK.</span></span>
13. <span data-ttu-id="b3d05-121">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b3d05-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="b3d05-122">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="b3d05-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="b3d05-123">Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.</span><span class="sxs-lookup"><span data-stu-id="b3d05-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="b3d05-124">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="b3d05-124">Click OK.</span></span>
17. <span data-ttu-id="b3d05-125">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b3d05-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="b3d05-126">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="b3d05-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="b3d05-127">Í reitnum Heiti skal færa inn 'færslubók'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="b3d05-128">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="b3d05-128">Click OK.</span></span>
21. <span data-ttu-id="b3d05-129">Í trénu, skal velja 'Root: XML Element\Journal: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="b3d05-130">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b3d05-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="b3d05-131">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="b3d05-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="b3d05-132">Í reitnum Heiti skal færa inn 'runa'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="b3d05-133">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="b3d05-133">Click OK.</span></span>
26. <span data-ttu-id="b3d05-134">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b3d05-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="b3d05-135">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="b3d05-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="b3d05-136">Í reitnum Heiti skal færa inn ‚færsla'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="b3d05-137">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="b3d05-137">Click OK.</span></span>
30. <span data-ttu-id="b3d05-138">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="b3d05-139">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b3d05-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="b3d05-140">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="b3d05-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="b3d05-141">Í reitnum Heiti skal færa inn ‚fylgiskjal'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="b3d05-142">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b3d05-142">Click OK.</span></span>
35. <span data-ttu-id="b3d05-143">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="b3d05-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="b3d05-144">Í reitnum Heiti skal færa inn ‚dagsetning'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="b3d05-145">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b3d05-145">Click OK.</span></span>
38. <span data-ttu-id="b3d05-146">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="b3d05-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="b3d05-147">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="b3d05-148">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b3d05-148">Click OK.</span></span>
41. <span data-ttu-id="b3d05-149">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="b3d05-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="b3d05-150">Í svæðið Heiti, færðu inn 'Dt'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="b3d05-151">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b3d05-151">Click OK.</span></span>
44. <span data-ttu-id="b3d05-152">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="b3d05-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="b3d05-153">Í reitinn Heiti skal slá inn 'Ct'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="b3d05-154">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b3d05-154">Click OK.</span></span>
47. <span data-ttu-id="b3d05-155">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b3d05-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="b3d05-156">Í trénu skal velja „XML/Element“.</span><span class="sxs-lookup"><span data-stu-id="b3d05-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="b3d05-157">Í reitnum Heiti skal færa inn 'víddir'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="b3d05-158">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="b3d05-158">Click OK.</span></span>
51. <span data-ttu-id="b3d05-159">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="b3d05-160">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b3d05-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="b3d05-161">Í trénu skal velja „XML/Attribute“.</span><span class="sxs-lookup"><span data-stu-id="b3d05-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="b3d05-162">Í reitnum Heiti skal færa inn 'kóði'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="b3d05-163">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b3d05-163">Click OK.</span></span>
56. <span data-ttu-id="b3d05-164">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="b3d05-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="b3d05-165">Í svæðið Heiti, færðu inn 'Gildi'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="b3d05-166">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b3d05-166">Click OK.</span></span>
59. <span data-ttu-id="b3d05-167">Smella á Bæta við eigind.</span><span class="sxs-lookup"><span data-stu-id="b3d05-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="b3d05-168">Í svæðið Heiti, færðu inn 'lýsing'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="b3d05-169">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b3d05-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="b3d05-170">Varpa skýrslueiningum í gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="b3d05-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="b3d05-171">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="b3d05-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="b3d05-172">Í trénu, skal víkka út 'model: Data model Financial dimensions sample model'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="b3d05-173">Í trénu, skal víkka út 'model: Data model Financial dimensions sample model\Journal: Record list'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="b3d05-174">Í trénu, skal víkka út 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="b3d05-175">Í trénu, skal víkka út 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="b3d05-176">Í trénu, skal velja ' Rót: XML Element\Journal: xml-Eininguna '.</span><span class="sxs-lookup"><span data-stu-id="b3d05-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="b3d05-177">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="b3d05-178">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="b3d05-178">Click Bind.</span></span>
9. <span data-ttu-id="b3d05-179">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="b3d05-180">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="b3d05-181">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="b3d05-181">Click Bind.</span></span>
12. <span data-ttu-id="b3d05-182">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="b3d05-183">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="b3d05-184">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="b3d05-184">Click Bind.</span></span>
15. <span data-ttu-id="b3d05-185">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="b3d05-186">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="b3d05-187">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="b3d05-187">Click Bind.</span></span>
18. <span data-ttu-id="b3d05-188">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="b3d05-189">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="b3d05-190">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="b3d05-190">Click Bind.</span></span>
21. <span data-ttu-id="b3d05-191">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="b3d05-192">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="b3d05-193">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="b3d05-193">Click Bind.</span></span>
24. <span data-ttu-id="b3d05-194">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="b3d05-195">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="b3d05-196">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="b3d05-196">Click Bind.</span></span>
27. <span data-ttu-id="b3d05-197">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="b3d05-198">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="b3d05-199">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="b3d05-199">Click Bind.</span></span>
30. <span data-ttu-id="b3d05-200">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="b3d05-201">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="b3d05-202">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="b3d05-202">Click Bind.</span></span>
33. <span data-ttu-id="b3d05-203">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="b3d05-204">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="b3d05-205">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="b3d05-205">Click Bind.</span></span>
36. <span data-ttu-id="b3d05-206">Í trénu, skal velja 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="b3d05-207">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="b3d05-208">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="b3d05-208">Click Bind.</span></span>
39. <span data-ttu-id="b3d05-209">Í trénu, skal velja 'Root: XML Element\Journal: XML Element'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="b3d05-210">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Journal: Record list'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="b3d05-211">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="b3d05-211">Click Bind.</span></span>
42. <span data-ttu-id="b3d05-212">Í trénu, skal velja 'Root: XML Element\Company: XML Attribute'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="b3d05-213">Í trénu, skal velja 'model: Data model Financial dimensions sample model\Company: String'.</span><span class="sxs-lookup"><span data-stu-id="b3d05-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="b3d05-214">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="b3d05-214">Click Bind.</span></span>
45. <span data-ttu-id="b3d05-215">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b3d05-215">Click Save.</span></span>
46. <span data-ttu-id="b3d05-216">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b3d05-216">Close the page.</span></span>

