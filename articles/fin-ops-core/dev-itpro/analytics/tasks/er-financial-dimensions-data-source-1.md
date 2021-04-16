---
title: Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 1 - hanna gagnalíkan)
description: Þetta efni útskýrir hvernig á að skilgreina líkan rafrænnar skýrslugerðar til að nota fjárhagsvíddir sem gagnagjafa fyrir skýrslur rafrænnar skýrslugerðar. (Hluti 1)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92b44532dfae70f03d6686ca1d2f8b6f74345ee6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752461"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="ea82a-104">Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 1 - hanna gagnalíkan)</span><span class="sxs-lookup"><span data-stu-id="ea82a-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ea82a-105">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="ea82a-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="ea82a-106">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="ea82a-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="ea82a-107">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka”.</span><span class="sxs-lookup"><span data-stu-id="ea82a-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="ea82a-108">Búa til nýtt gagnalíkan</span><span class="sxs-lookup"><span data-stu-id="ea82a-108">Create a new data model</span></span>
1. <span data-ttu-id="ea82a-109">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="ea82a-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="ea82a-110">Gakktu úr skugga um að „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="ea82a-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="ea82a-111">veitandi sé tiltæk og merkt Virk.</span><span class="sxs-lookup"><span data-stu-id="ea82a-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="ea82a-112">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="ea82a-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="ea82a-113">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="ea82a-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="ea82a-114">Í svæðið Heiti, Færðu inn 'Dæmi um líkan fyrir fjárhagsvíddir'.</span><span class="sxs-lookup"><span data-stu-id="ea82a-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="ea82a-115">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="ea82a-115">Click Create configuration.</span></span>
6. <span data-ttu-id="ea82a-116">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="ea82a-116">Click Designer.</span></span>
7. <span data-ttu-id="ea82a-117">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ea82a-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="ea82a-118">Í reitnum Heiti skal færa inn 'Færsla'.</span><span class="sxs-lookup"><span data-stu-id="ea82a-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="ea82a-119">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="ea82a-119">Click Add.</span></span>
10. <span data-ttu-id="ea82a-120">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ea82a-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="ea82a-121">Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.</span><span class="sxs-lookup"><span data-stu-id="ea82a-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="ea82a-122">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="ea82a-122">Click Add.</span></span>
    * <span data-ttu-id="ea82a-123">Við bætum nýjum skáarlista við líkanið okkar.</span><span class="sxs-lookup"><span data-stu-id="ea82a-123">We will add to our model a new record list.</span></span> <span data-ttu-id="ea82a-124">Listinn mun sýna (fyrir allar rafrænar skýrslur sem nota þetta líkan sem gagnagjafa) stillingar fyrir valdar fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="ea82a-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="ea82a-125">Hver fjárhagsvídd verða sýnd á þessum lista sem færsla með viðeigandi svæði sem tákna stillingar víddar.</span><span class="sxs-lookup"><span data-stu-id="ea82a-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="ea82a-126">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ea82a-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="ea82a-127">Í reitnum Heiti skal færa inn 'Grunnstilling vídda'.</span><span class="sxs-lookup"><span data-stu-id="ea82a-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="ea82a-128">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="ea82a-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="ea82a-129">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="ea82a-129">Click Add.</span></span>
17. <span data-ttu-id="ea82a-130">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ea82a-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="ea82a-131">Í reitnum Heiti skal færa inn 'kóði'.</span><span class="sxs-lookup"><span data-stu-id="ea82a-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="ea82a-132">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="ea82a-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="ea82a-133">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="ea82a-133">Click Add.</span></span>
21. <span data-ttu-id="ea82a-134">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ea82a-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="ea82a-135">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="ea82a-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="ea82a-136">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="ea82a-136">Click Add.</span></span>
24. <span data-ttu-id="ea82a-137">Í trénu skal velja „færsla“.</span><span class="sxs-lookup"><span data-stu-id="ea82a-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="ea82a-138">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ea82a-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="ea82a-139">Í reitnum Heiti skal færa inn 'færslubók'.</span><span class="sxs-lookup"><span data-stu-id="ea82a-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="ea82a-140">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="ea82a-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="ea82a-141">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="ea82a-141">Click Add.</span></span>
29. <span data-ttu-id="ea82a-142">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ea82a-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="ea82a-143">Í reitnum Heiti skal færa inn 'runa'.</span><span class="sxs-lookup"><span data-stu-id="ea82a-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="ea82a-144">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="ea82a-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="ea82a-145">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="ea82a-145">Click Add.</span></span>
33. <span data-ttu-id="ea82a-146">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ea82a-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="ea82a-147">Í reitnum Heiti skal færa inn ‚færsla'.</span><span class="sxs-lookup"><span data-stu-id="ea82a-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="ea82a-148">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="ea82a-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="ea82a-149">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="ea82a-149">Click Add.</span></span>
37. <span data-ttu-id="ea82a-150">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ea82a-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="ea82a-151">Í reitnum Heiti skal færa inn ‚dagsetning'.</span><span class="sxs-lookup"><span data-stu-id="ea82a-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="ea82a-152">Velja 'Dagsetning' í svæðinu gerð vöru.</span><span class="sxs-lookup"><span data-stu-id="ea82a-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="ea82a-153">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="ea82a-153">Click Add.</span></span>
41. <span data-ttu-id="ea82a-154">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ea82a-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="ea82a-155">Í reitnum Heiti skal færa inn ‚debetfæra'.</span><span class="sxs-lookup"><span data-stu-id="ea82a-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="ea82a-156">Veljið 'Raunveruleg' í svæðinu gerð vöru.</span><span class="sxs-lookup"><span data-stu-id="ea82a-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="ea82a-157">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="ea82a-157">Click Add.</span></span>
45. <span data-ttu-id="ea82a-158">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ea82a-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="ea82a-159">Í svæðið Heiti, færðu inn 'kreditfæra'.</span><span class="sxs-lookup"><span data-stu-id="ea82a-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="ea82a-160">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="ea82a-160">Click Add.</span></span>
48. <span data-ttu-id="ea82a-161">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ea82a-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="ea82a-162">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="ea82a-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="ea82a-163">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="ea82a-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="ea82a-164">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="ea82a-164">Click Add.</span></span>
52. <span data-ttu-id="ea82a-165">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ea82a-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="ea82a-166">Í reitnum Heiti skal færa inn ‚fylgiskjal'.</span><span class="sxs-lookup"><span data-stu-id="ea82a-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="ea82a-167">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="ea82a-167">Click Add.</span></span>
55. <span data-ttu-id="ea82a-168">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ea82a-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="ea82a-169">Í reitnum Heiti skal færa inn 'gögn um víddir'.</span><span class="sxs-lookup"><span data-stu-id="ea82a-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="ea82a-170">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="ea82a-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="ea82a-171">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="ea82a-171">Click Add.</span></span>
    * <span data-ttu-id="ea82a-172">Við bættum nýjum færslulista við líkanið okkar.</span><span class="sxs-lookup"><span data-stu-id="ea82a-172">We added to our model a new record list.</span></span> <span data-ttu-id="ea82a-173">Listinn mun sýna (fyrir allar rafrænar skýrslur sem nota þetta líkan sem gagnagjafa) gildi fyrir valdar fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="ea82a-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="ea82a-174">Hver fjárhagsvídd verða sýnd á þessum lista sem færsla með viðeigandi svæði sem tákna Gildi víddar.</span><span class="sxs-lookup"><span data-stu-id="ea82a-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="ea82a-175">Heiti víddar verður einnig sýnt í þessari færslu sem svæði til að nota, ef þörf krefur, til að geta valið úr.</span><span class="sxs-lookup"><span data-stu-id="ea82a-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="ea82a-176">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ea82a-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="ea82a-177">Í reitnum Heiti skal færa inn 'kóði'.</span><span class="sxs-lookup"><span data-stu-id="ea82a-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="ea82a-178">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="ea82a-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="ea82a-179">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="ea82a-179">Click Add.</span></span>
63. <span data-ttu-id="ea82a-180">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ea82a-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="ea82a-181">Í reitnum Heiti skal færa inn ‚Lýsing'.</span><span class="sxs-lookup"><span data-stu-id="ea82a-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="ea82a-182">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="ea82a-182">Click Add.</span></span>
66. <span data-ttu-id="ea82a-183">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="ea82a-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="ea82a-184">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="ea82a-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="ea82a-185">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="ea82a-185">Click Add.</span></span>
69. <span data-ttu-id="ea82a-186">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="ea82a-186">Click Save.</span></span>
70. <span data-ttu-id="ea82a-187">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ea82a-187">Close the page.</span></span>

![Hönnuðarsíðan ER-gagnavörpun](../media/er-financial-dimensions-guides-data-model.png)



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]