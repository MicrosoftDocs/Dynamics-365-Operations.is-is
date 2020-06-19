---
title: Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 1 - hanna gagnalíkan)
description: Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b951c9074c68a9f7592c17e0688498880397b223
ms.sourcegitcommit: d9125c20b21459076e4fd92fd9ebfe2e53a0431b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/27/2020
ms.locfileid: "3406544"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="d775b-103">Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 1 - hanna gagnalíkan)</span><span class="sxs-lookup"><span data-stu-id="d775b-103">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d775b-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="d775b-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="d775b-105">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="d775b-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="d775b-106">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka”.</span><span class="sxs-lookup"><span data-stu-id="d775b-106">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="d775b-107">Búa til nýtt gagnalíkan</span><span class="sxs-lookup"><span data-stu-id="d775b-107">Create a new data model</span></span>
1. <span data-ttu-id="d775b-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="d775b-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="d775b-109">Gakktu úr skugga um að „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="d775b-109">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="d775b-110">veitandi sé tiltæk og merkt Virk.</span><span class="sxs-lookup"><span data-stu-id="d775b-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="d775b-111">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="d775b-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="d775b-112">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="d775b-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="d775b-113">Í svæðið Heiti, Færðu inn 'Dæmi um líkan fyrir fjárhagsvíddir'.</span><span class="sxs-lookup"><span data-stu-id="d775b-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="d775b-114">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="d775b-114">Click Create configuration.</span></span>
6. <span data-ttu-id="d775b-115">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="d775b-115">Click Designer.</span></span>
7. <span data-ttu-id="d775b-116">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d775b-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="d775b-117">Í reitnum Heiti skal færa inn 'Færsla'.</span><span class="sxs-lookup"><span data-stu-id="d775b-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="d775b-118">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d775b-118">Click Add.</span></span>
10. <span data-ttu-id="d775b-119">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d775b-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="d775b-120">Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.</span><span class="sxs-lookup"><span data-stu-id="d775b-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="d775b-121">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d775b-121">Click Add.</span></span>
    * <span data-ttu-id="d775b-122">Við bætum nýjum skáarlista við líkanið okkar.</span><span class="sxs-lookup"><span data-stu-id="d775b-122">We will add to our model a new record list.</span></span> <span data-ttu-id="d775b-123">Listinn mun sýna (fyrir allar rafrænar skýrslur sem nota þetta líkan sem gagnagjafa) stillingar fyrir valdar fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="d775b-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="d775b-124">Hver fjárhagsvídd verða sýnd á þessum lista sem færsla með viðeigandi svæði sem tákna stillingar víddar.</span><span class="sxs-lookup"><span data-stu-id="d775b-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="d775b-125">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d775b-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="d775b-126">Í reitnum Heiti skal færa inn 'Grunnstilling vídda'.</span><span class="sxs-lookup"><span data-stu-id="d775b-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="d775b-127">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="d775b-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="d775b-128">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d775b-128">Click Add.</span></span>
17. <span data-ttu-id="d775b-129">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d775b-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="d775b-130">Í reitnum Heiti skal færa inn 'kóði'.</span><span class="sxs-lookup"><span data-stu-id="d775b-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="d775b-131">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="d775b-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="d775b-132">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d775b-132">Click Add.</span></span>
21. <span data-ttu-id="d775b-133">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d775b-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="d775b-134">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="d775b-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="d775b-135">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d775b-135">Click Add.</span></span>
24. <span data-ttu-id="d775b-136">Í trénu skal velja „færsla“.</span><span class="sxs-lookup"><span data-stu-id="d775b-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="d775b-137">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d775b-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="d775b-138">Í reitnum Heiti skal færa inn 'færslubók'.</span><span class="sxs-lookup"><span data-stu-id="d775b-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="d775b-139">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="d775b-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="d775b-140">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d775b-140">Click Add.</span></span>
29. <span data-ttu-id="d775b-141">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d775b-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="d775b-142">Í reitnum Heiti skal færa inn 'runa'.</span><span class="sxs-lookup"><span data-stu-id="d775b-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="d775b-143">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="d775b-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="d775b-144">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d775b-144">Click Add.</span></span>
33. <span data-ttu-id="d775b-145">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d775b-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="d775b-146">Í reitnum Heiti skal færa inn ‚færsla'.</span><span class="sxs-lookup"><span data-stu-id="d775b-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="d775b-147">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="d775b-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="d775b-148">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d775b-148">Click Add.</span></span>
37. <span data-ttu-id="d775b-149">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d775b-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="d775b-150">Í reitnum Heiti skal færa inn ‚dagsetning'.</span><span class="sxs-lookup"><span data-stu-id="d775b-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="d775b-151">Velja 'Dagsetning' í svæðinu gerð vöru.</span><span class="sxs-lookup"><span data-stu-id="d775b-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="d775b-152">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d775b-152">Click Add.</span></span>
41. <span data-ttu-id="d775b-153">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d775b-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="d775b-154">Í reitnum Heiti skal færa inn ‚debetfæra'.</span><span class="sxs-lookup"><span data-stu-id="d775b-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="d775b-155">Veljið 'Raunveruleg' í svæðinu gerð vöru.</span><span class="sxs-lookup"><span data-stu-id="d775b-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="d775b-156">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d775b-156">Click Add.</span></span>
45. <span data-ttu-id="d775b-157">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d775b-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="d775b-158">Í svæðið Heiti, færðu inn 'kreditfæra'.</span><span class="sxs-lookup"><span data-stu-id="d775b-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="d775b-159">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d775b-159">Click Add.</span></span>
48. <span data-ttu-id="d775b-160">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d775b-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="d775b-161">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="d775b-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="d775b-162">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="d775b-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="d775b-163">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d775b-163">Click Add.</span></span>
52. <span data-ttu-id="d775b-164">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d775b-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="d775b-165">Í reitnum Heiti skal færa inn ‚fylgiskjal'.</span><span class="sxs-lookup"><span data-stu-id="d775b-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="d775b-166">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d775b-166">Click Add.</span></span>
55. <span data-ttu-id="d775b-167">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d775b-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="d775b-168">Í reitnum Heiti skal færa inn 'gögn um víddir'.</span><span class="sxs-lookup"><span data-stu-id="d775b-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="d775b-169">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="d775b-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="d775b-170">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d775b-170">Click Add.</span></span>
    * <span data-ttu-id="d775b-171">Við bættum nýjum færslulista við líkanið okkar.</span><span class="sxs-lookup"><span data-stu-id="d775b-171">We added to our model a new record list.</span></span> <span data-ttu-id="d775b-172">Listinn mun sýna (fyrir allar rafrænar skýrslur sem nota þetta líkan sem gagnagjafa) gildi fyrir valdar fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="d775b-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="d775b-173">Hver fjárhagsvídd verða sýnd á þessum lista sem færsla með viðeigandi svæði sem tákna Gildi víddar.</span><span class="sxs-lookup"><span data-stu-id="d775b-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="d775b-174">Heiti víddar verður einnig sýnt í þessari færslu sem svæði til að nota, ef þörf krefur, til að geta valið úr.</span><span class="sxs-lookup"><span data-stu-id="d775b-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="d775b-175">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d775b-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="d775b-176">Í reitnum Heiti skal færa inn 'kóði'.</span><span class="sxs-lookup"><span data-stu-id="d775b-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="d775b-177">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="d775b-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="d775b-178">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d775b-178">Click Add.</span></span>
63. <span data-ttu-id="d775b-179">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d775b-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="d775b-180">Í reitnum Heiti skal færa inn ‚Lýsing'.</span><span class="sxs-lookup"><span data-stu-id="d775b-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="d775b-181">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d775b-181">Click Add.</span></span>
66. <span data-ttu-id="d775b-182">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="d775b-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="d775b-183">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="d775b-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="d775b-184">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d775b-184">Click Add.</span></span>
69. <span data-ttu-id="d775b-185">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="d775b-185">Click Save.</span></span>
70. <span data-ttu-id="d775b-186">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d775b-186">Close the page.</span></span>

![Hönnuðarsíðan ER-gagnavörpun](../media/er-financial-dimensions-guides-data-model.png)

