--- 
title: "Hanna gagnalíkan til að nota fjárhagsvíddir sem gagnaveitu"
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3e55eedba1955ae79733afee1a0b3c7072147bb5
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="design-data-model-to-use-financial-dimensions-as-a-data-source"></a><span data-ttu-id="df6cc-103">Hanna gagnalíkan til að nota fjárhagsvíddir sem gagnaveitu</span><span class="sxs-lookup"><span data-stu-id="df6cc-103">Design data model to use financial dimensions as a data source</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="df6cc-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="df6cc-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="df6cc-105">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="df6cc-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="df6cc-106">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu “Stofna skilgreiningarveitu og merkja hana sem virka”.</span><span class="sxs-lookup"><span data-stu-id="df6cc-106">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="df6cc-107">Búa til nýtt gagnalíkan</span><span class="sxs-lookup"><span data-stu-id="df6cc-107">Create a new data model</span></span>
1. <span data-ttu-id="df6cc-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="df6cc-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="df6cc-109">Gakktu úr skugga um að „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="df6cc-109">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="df6cc-110">veitandi sé tiltæk og merkt Virk.</span><span class="sxs-lookup"><span data-stu-id="df6cc-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="df6cc-111">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="df6cc-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="df6cc-112">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="df6cc-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="df6cc-113">Í svæðið Heiti, Færðu inn 'Dæmi um líkan fyrir fjárhagsvíddir'.</span><span class="sxs-lookup"><span data-stu-id="df6cc-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="df6cc-114">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="df6cc-114">Click Create configuration.</span></span>
6. <span data-ttu-id="df6cc-115">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="df6cc-115">Click Designer.</span></span>
7. <span data-ttu-id="df6cc-116">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="df6cc-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="df6cc-117">Í reitnum Heiti skal færa inn 'Færsla'.</span><span class="sxs-lookup"><span data-stu-id="df6cc-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="df6cc-118">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="df6cc-118">Click Add.</span></span>
10. <span data-ttu-id="df6cc-119">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="df6cc-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="df6cc-120">Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.</span><span class="sxs-lookup"><span data-stu-id="df6cc-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="df6cc-121">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="df6cc-121">Click Add.</span></span>
    * <span data-ttu-id="df6cc-122">Við bætum nýjum skáarlista við líkanið okkar.</span><span class="sxs-lookup"><span data-stu-id="df6cc-122">We will add to our model a new record list.</span></span> <span data-ttu-id="df6cc-123">Listinn mun sýna (fyrir allar rafrænar skýrslur sem nota þetta líkan sem gagnagjafa) stillingar fyrir valdar fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="df6cc-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="df6cc-124">Hver fjárhagsvídd verða sýnd á þessum lista sem færsla með viðeigandi svæði sem tákna stillingar víddar.</span><span class="sxs-lookup"><span data-stu-id="df6cc-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s setting.</span></span>  
13. <span data-ttu-id="df6cc-125">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="df6cc-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="df6cc-126">Í reitnum Heiti skal færa inn 'Grunnstilling vídda'.</span><span class="sxs-lookup"><span data-stu-id="df6cc-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="df6cc-127">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="df6cc-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="df6cc-128">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="df6cc-128">Click Add.</span></span>
17. <span data-ttu-id="df6cc-129">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="df6cc-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="df6cc-130">Í reitnum Heiti skal færa inn 'kóði'.</span><span class="sxs-lookup"><span data-stu-id="df6cc-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="df6cc-131">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="df6cc-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="df6cc-132">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="df6cc-132">Click Add.</span></span>
21. <span data-ttu-id="df6cc-133">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="df6cc-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="df6cc-134">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="df6cc-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="df6cc-135">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="df6cc-135">Click Add.</span></span>
24. <span data-ttu-id="df6cc-136">Í trénu skal velja „færsla“.</span><span class="sxs-lookup"><span data-stu-id="df6cc-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="df6cc-137">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="df6cc-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="df6cc-138">Í reitnum Heiti skal færa inn 'færslubók'.</span><span class="sxs-lookup"><span data-stu-id="df6cc-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="df6cc-139">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="df6cc-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="df6cc-140">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="df6cc-140">Click Add.</span></span>
29. <span data-ttu-id="df6cc-141">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="df6cc-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="df6cc-142">Í reitnum Heiti skal færa inn 'runa'.</span><span class="sxs-lookup"><span data-stu-id="df6cc-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="df6cc-143">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="df6cc-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="df6cc-144">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="df6cc-144">Click Add.</span></span>
33. <span data-ttu-id="df6cc-145">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="df6cc-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="df6cc-146">Í reitnum Heiti skal færa inn ‚færsla'.</span><span class="sxs-lookup"><span data-stu-id="df6cc-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="df6cc-147">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="df6cc-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="df6cc-148">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="df6cc-148">Click Add.</span></span>
37. <span data-ttu-id="df6cc-149">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="df6cc-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="df6cc-150">Í reitnum Heiti skal færa inn ‚dagsetning'.</span><span class="sxs-lookup"><span data-stu-id="df6cc-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="df6cc-151">Velja 'Dagsetning' í svæðinu gerð vöru.</span><span class="sxs-lookup"><span data-stu-id="df6cc-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="df6cc-152">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="df6cc-152">Click Add.</span></span>
41. <span data-ttu-id="df6cc-153">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="df6cc-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="df6cc-154">Í reitnum Heiti skal færa inn ‚debetfæra'.</span><span class="sxs-lookup"><span data-stu-id="df6cc-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="df6cc-155">Veljið 'Raunveruleg' í svæðinu gerð vöru.</span><span class="sxs-lookup"><span data-stu-id="df6cc-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="df6cc-156">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="df6cc-156">Click Add.</span></span>
45. <span data-ttu-id="df6cc-157">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="df6cc-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="df6cc-158">Í svæðið Heiti, færðu inn 'kreditfæra'.</span><span class="sxs-lookup"><span data-stu-id="df6cc-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="df6cc-159">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="df6cc-159">Click Add.</span></span>
48. <span data-ttu-id="df6cc-160">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="df6cc-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="df6cc-161">Í svæðið Heiti, færðu inn 'Gjaldmiðils'.</span><span class="sxs-lookup"><span data-stu-id="df6cc-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="df6cc-162">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="df6cc-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="df6cc-163">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="df6cc-163">Click Add.</span></span>
52. <span data-ttu-id="df6cc-164">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="df6cc-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="df6cc-165">Í reitnum Heiti skal færa inn ‚fylgiskjal'.</span><span class="sxs-lookup"><span data-stu-id="df6cc-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="df6cc-166">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="df6cc-166">Click Add.</span></span>
55. <span data-ttu-id="df6cc-167">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="df6cc-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="df6cc-168">Í reitnum Heiti skal færa inn 'gögn um víddir'.</span><span class="sxs-lookup"><span data-stu-id="df6cc-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="df6cc-169">Veljið í svæðinu gerð Vöru „Skrárlisti".</span><span class="sxs-lookup"><span data-stu-id="df6cc-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="df6cc-170">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="df6cc-170">Click Add.</span></span>
    * <span data-ttu-id="df6cc-171">Við bættum nýjum færslulista við líkanið okkar.</span><span class="sxs-lookup"><span data-stu-id="df6cc-171">We added to our model a new record list.</span></span> <span data-ttu-id="df6cc-172">Listinn mun sýna (fyrir allar rafrænar skýrslur sem nota þetta líkan sem gagnagjafa) gildi fyrir valdar fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="df6cc-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="df6cc-173">Hver fjárhagsvídd verða sýnd á þessum lista sem færsla með viðeigandi svæði sem tákna Gildi víddar.</span><span class="sxs-lookup"><span data-stu-id="df6cc-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s values.</span></span> <span data-ttu-id="df6cc-174">Heiti víddar verður einnig sýnt í þessari færslu sem svæði til að nota, ef þörf krefur, til að geta valið úr.</span><span class="sxs-lookup"><span data-stu-id="df6cc-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="df6cc-175">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="df6cc-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="df6cc-176">Í reitnum Heiti skal færa inn 'kóði'.</span><span class="sxs-lookup"><span data-stu-id="df6cc-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="df6cc-177">Veljið 'Strengur' í svæðinu Vöru.</span><span class="sxs-lookup"><span data-stu-id="df6cc-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="df6cc-178">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="df6cc-178">Click Add.</span></span>
63. <span data-ttu-id="df6cc-179">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="df6cc-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="df6cc-180">Í reitnum Heiti skal færa inn ‚Lýsing'.</span><span class="sxs-lookup"><span data-stu-id="df6cc-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="df6cc-181">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="df6cc-181">Click Add.</span></span>
66. <span data-ttu-id="df6cc-182">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="df6cc-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="df6cc-183">Í svæðið Heiti, færðu inn ‚Heiti'.</span><span class="sxs-lookup"><span data-stu-id="df6cc-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="df6cc-184">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="df6cc-184">Click Add.</span></span>
69. <span data-ttu-id="df6cc-185">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="df6cc-185">Click Save.</span></span>
70. <span data-ttu-id="df6cc-186">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="df6cc-186">Close the page.</span></span>


