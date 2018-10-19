--- 
title: "Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 1 - hanna gagnalíkan)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 84f546b73eefe3ead78c6ab3fdbbc05d0db5fef5
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1-design-data-model"></a><span data-ttu-id="f1550-103">Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 1: Hanna gagnalíkan)</span><span class="sxs-lookup"><span data-stu-id="f1550-103">ER Use financial dimensions as a data source (Part 1: Design data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1550-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="f1550-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="f1550-105">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="f1550-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="f1550-106">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu “Stofna skilgreiningarveitu og merkja hana sem virka”.</span><span class="sxs-lookup"><span data-stu-id="f1550-106">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="f1550-107">Búa til nýtt gagnalíkan</span><span class="sxs-lookup"><span data-stu-id="f1550-107">Create a new data model</span></span>
1. <span data-ttu-id="f1550-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="f1550-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="f1550-109">Gakktu úr skugga um að „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="f1550-109">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="f1550-110">veitandi sé tiltæk og merkt Virk.</span><span class="sxs-lookup"><span data-stu-id="f1550-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="f1550-111">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="f1550-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="f1550-112">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="f1550-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="f1550-113">Í svæðið Heiti, Færðu inn 'Dæmi um líkan fyrir fjárhagsvíddir'.</span><span class="sxs-lookup"><span data-stu-id="f1550-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="f1550-114">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="f1550-114">Click Create configuration.</span></span>
6. <span data-ttu-id="f1550-115">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="f1550-115">Click Designer.</span></span>
7. <span data-ttu-id="f1550-116">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f1550-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="f1550-117">Í reitnum Heiti skal færa inn 'Færsla'.</span><span class="sxs-lookup"><span data-stu-id="f1550-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="f1550-118">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f1550-118">Click Add.</span></span>
10. <span data-ttu-id="f1550-119">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f1550-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="f1550-120">Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.</span><span class="sxs-lookup"><span data-stu-id="f1550-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="f1550-121">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f1550-121">Click Add.</span></span>
    * <span data-ttu-id="f1550-122">Við bætum nýjum skáarlista við líkanið okkar.</span><span class="sxs-lookup"><span data-stu-id="f1550-122">We will add to our model a new record list.</span></span> <span data-ttu-id="f1550-123">Listinn mun sýna (fyrir allar rafrænar skýrslur sem nota þetta líkan sem gagnagjafa) stillingar fyrir valdar fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="f1550-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="f1550-124">Hver fjárhagsvídd verða sýnd á þessum lista sem færsla með viðeigandi svæði sem tákna stillingar víddar.</span><span class="sxs-lookup"><span data-stu-id="f1550-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s setting.</span></span>  
13. <span data-ttu-id="f1550-125">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f1550-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="f1550-126">Í reitnum Heiti skal færa inn 'Grunnstilling vídda'.</span><span class="sxs-lookup"><span data-stu-id="f1550-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="f1550-127">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="f1550-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="f1550-128">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f1550-128">Click Add.</span></span>
17. <span data-ttu-id="f1550-129">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f1550-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="f1550-130">Í reitnum Heiti skal færa inn 'kóði'.</span><span class="sxs-lookup"><span data-stu-id="f1550-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="f1550-131">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="f1550-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="f1550-132">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f1550-132">Click Add.</span></span>
21. <span data-ttu-id="f1550-133">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f1550-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="f1550-134">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="f1550-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="f1550-135">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f1550-135">Click Add.</span></span>
24. <span data-ttu-id="f1550-136">Í trénu skal velja „færsla“.</span><span class="sxs-lookup"><span data-stu-id="f1550-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="f1550-137">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f1550-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="f1550-138">Í reitnum Heiti skal færa inn 'færslubók'.</span><span class="sxs-lookup"><span data-stu-id="f1550-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="f1550-139">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="f1550-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="f1550-140">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f1550-140">Click Add.</span></span>
29. <span data-ttu-id="f1550-141">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f1550-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="f1550-142">Í reitnum Heiti skal færa inn 'runa'.</span><span class="sxs-lookup"><span data-stu-id="f1550-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="f1550-143">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="f1550-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="f1550-144">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f1550-144">Click Add.</span></span>
33. <span data-ttu-id="f1550-145">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f1550-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="f1550-146">Í reitnum Heiti skal færa inn ‚færsla'.</span><span class="sxs-lookup"><span data-stu-id="f1550-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="f1550-147">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="f1550-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="f1550-148">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f1550-148">Click Add.</span></span>
37. <span data-ttu-id="f1550-149">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f1550-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="f1550-150">Í reitnum Heiti skal færa inn ‚dagsetning'.</span><span class="sxs-lookup"><span data-stu-id="f1550-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="f1550-151">Velja 'Dagsetning' í svæðinu gerð vöru.</span><span class="sxs-lookup"><span data-stu-id="f1550-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="f1550-152">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f1550-152">Click Add.</span></span>
41. <span data-ttu-id="f1550-153">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f1550-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="f1550-154">Í reitnum Heiti skal færa inn ‚debetfæra'.</span><span class="sxs-lookup"><span data-stu-id="f1550-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="f1550-155">Veljið 'Raunveruleg' í svæðinu gerð vöru.</span><span class="sxs-lookup"><span data-stu-id="f1550-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="f1550-156">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f1550-156">Click Add.</span></span>
45. <span data-ttu-id="f1550-157">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f1550-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="f1550-158">Í svæðið Heiti, færðu inn 'kreditfæra'.</span><span class="sxs-lookup"><span data-stu-id="f1550-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="f1550-159">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f1550-159">Click Add.</span></span>
48. <span data-ttu-id="f1550-160">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f1550-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="f1550-161">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="f1550-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="f1550-162">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="f1550-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="f1550-163">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f1550-163">Click Add.</span></span>
52. <span data-ttu-id="f1550-164">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f1550-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="f1550-165">Í reitnum Heiti skal færa inn ‚fylgiskjal'.</span><span class="sxs-lookup"><span data-stu-id="f1550-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="f1550-166">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f1550-166">Click Add.</span></span>
55. <span data-ttu-id="f1550-167">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f1550-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="f1550-168">Í reitnum Heiti skal færa inn 'gögn um víddir'.</span><span class="sxs-lookup"><span data-stu-id="f1550-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="f1550-169">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="f1550-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="f1550-170">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f1550-170">Click Add.</span></span>
    * <span data-ttu-id="f1550-171">Við bættum nýjum færslulista við líkanið okkar.</span><span class="sxs-lookup"><span data-stu-id="f1550-171">We added to our model a new record list.</span></span> <span data-ttu-id="f1550-172">Listinn mun sýna (fyrir allar rafrænar skýrslur sem nota þetta líkan sem gagnagjafa) gildi fyrir valdar fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="f1550-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="f1550-173">Hver fjárhagsvídd verða sýnd á þessum lista sem færsla með viðeigandi svæði sem tákna Gildi víddar.</span><span class="sxs-lookup"><span data-stu-id="f1550-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s values.</span></span> <span data-ttu-id="f1550-174">Heiti víddar verður einnig sýnt í þessari færslu sem svæði til að nota, ef þörf krefur, til að geta valið úr.</span><span class="sxs-lookup"><span data-stu-id="f1550-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="f1550-175">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f1550-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="f1550-176">Í reitnum Heiti skal færa inn 'kóði'.</span><span class="sxs-lookup"><span data-stu-id="f1550-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="f1550-177">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="f1550-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="f1550-178">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f1550-178">Click Add.</span></span>
63. <span data-ttu-id="f1550-179">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f1550-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="f1550-180">Í reitnum Heiti skal færa inn ‚Lýsing'.</span><span class="sxs-lookup"><span data-stu-id="f1550-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="f1550-181">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f1550-181">Click Add.</span></span>
66. <span data-ttu-id="f1550-182">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f1550-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="f1550-183">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="f1550-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="f1550-184">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="f1550-184">Click Add.</span></span>
69. <span data-ttu-id="f1550-185">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f1550-185">Click Save.</span></span>
70. <span data-ttu-id="f1550-186">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f1550-186">Close the page.</span></span>


