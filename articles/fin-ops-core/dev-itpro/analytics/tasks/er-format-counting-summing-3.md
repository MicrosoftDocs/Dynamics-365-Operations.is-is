---
title: Rafræn skýrslugerð skilgreingasnið sér um að telja og leggja saman (Hluti 3 - Nota útreikninga til að búa til úttak)
description: Í þessu efni er útskýrt hvernig á að skilgreina snið rafrænnar skýrslugerðar til að telja og gera samantekt sem byggist á gögnum fyrir þegar myndað úttak texta. (Hluti 3)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af95399118b9059b9bead3a1b84203cf3b6e74c2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567117"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="12261-104">Rafræn skýrslugerð skilgreingasnið sér um að telja og leggja saman (Hluti 3 - Nota útreikninga til að búa til úttak)</span><span class="sxs-lookup"><span data-stu-id="12261-104">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="12261-105">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað.</span><span class="sxs-lookup"><span data-stu-id="12261-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="12261-106">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="12261-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="12261-107">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð skilgreingasnið sér um að telja og taka saman (Hluti 2: skilgreina útreikninga)”.</span><span class="sxs-lookup"><span data-stu-id="12261-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="12261-108">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="12261-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="12261-109">Skilgreina þessa skýrslu til að nota upplýsingar um talningu og samlagningu</span><span class="sxs-lookup"><span data-stu-id="12261-109">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="12261-110">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="12261-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="12261-111">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="12261-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="12261-112">Í trénu skal víkka út 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="12261-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="12261-113">Í trénu skal víkka út 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="12261-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="12261-114">Í trénu skal velja „Intrastat model\Intrastat (DE)\Intrastat (DE) með talningu & samlagningu“.</span><span class="sxs-lookup"><span data-stu-id="12261-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="12261-115">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="12261-115">Click Designer.</span></span>
7. <span data-ttu-id="12261-116">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="12261-116">Click the Mapping tab.</span></span>
8. <span data-ttu-id="12261-117">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="12261-117">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="12261-118">Bæta við nýjum gagnagjafa til að fá lista yfir blokkir sem voru lagðar á minni.</span><span class="sxs-lookup"><span data-stu-id="12261-118">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="12261-119">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="12261-119">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="12261-120">Í svæðið Heiti, færðu inn '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="12261-120">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="12261-121">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="12261-121">$BlocksList</span></span>  
11. <span data-ttu-id="12261-122">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="12261-122">Click Edit formula.</span></span>
12. <span data-ttu-id="12261-123">Í trénu skal velja 'Data collection functions\COLLECTEDLIST'.</span><span class="sxs-lookup"><span data-stu-id="12261-123">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="12261-124">Smelltu á Bæta við Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="12261-124">Click Add function.</span></span>
14. <span data-ttu-id="12261-125">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="12261-125">Click Add data source.</span></span>
15. <span data-ttu-id="12261-126">Í Formúlu svæðinu, færið inn 'COLLECTEDLIST('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="12261-126">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="12261-127">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="12261-127">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="12261-128">Í Formúlu svæðinu, færið inn 'COLLECTEDLIST('$BlockName', "\*")'.</span><span class="sxs-lookup"><span data-stu-id="12261-128">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="12261-129">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="12261-129">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="12261-130">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="12261-130">Click Save.</span></span>
    * <span data-ttu-id="12261-131">Mynstrið „\*” þýðir að allar blokkir verða teknar með í lista fyrir þessa skrá.</span><span class="sxs-lookup"><span data-stu-id="12261-131">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="12261-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="12261-132">Close the page.</span></span>
19. <span data-ttu-id="12261-133">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="12261-133">Click OK.</span></span>
20. <span data-ttu-id="12261-134">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="12261-134">Click the Format tab.</span></span>
21. <span data-ttu-id="12261-135">Í trénu skal velja 'Intrastat\Data'.</span><span class="sxs-lookup"><span data-stu-id="12261-135">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="12261-136">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="12261-136">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="12261-137">Í trénu skal velja 'Text\Sequence'.</span><span class="sxs-lookup"><span data-stu-id="12261-137">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="12261-138">Í svæðið Heiti, færðu inn 'Samtölur eftir blokkum'.</span><span class="sxs-lookup"><span data-stu-id="12261-138">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="12261-139">Samtölur eftir blokkum</span><span class="sxs-lookup"><span data-stu-id="12261-139">Totals by blocks</span></span>  
25. <span data-ttu-id="12261-140">Í reitnum sérstafir skal velja "ný lína - Windows (CR LF)".</span><span class="sxs-lookup"><span data-stu-id="12261-140">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="12261-141">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="12261-141">Click OK.</span></span>
27. <span data-ttu-id="12261-142">Í trénu skal velja 'Intrastat\Data\Totals by blocks'.</span><span class="sxs-lookup"><span data-stu-id="12261-142">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="12261-143">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="12261-143">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="12261-144">Í trénu skal velja ‚Texti/Strengur'.</span><span class="sxs-lookup"><span data-stu-id="12261-144">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="12261-145">Í svæðið Heiti, færðu inn "kóði blokkar"</span><span class="sxs-lookup"><span data-stu-id="12261-145">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="12261-146">Kóði blokkar</span><span class="sxs-lookup"><span data-stu-id="12261-146">Block code</span></span>  
31. <span data-ttu-id="12261-147">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="12261-147">Click OK.</span></span>
32. <span data-ttu-id="12261-148">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="12261-148">Click Add String.</span></span>
33. <span data-ttu-id="12261-149">Í svæðið Heiti, færðu inn 'talning lína'.</span><span class="sxs-lookup"><span data-stu-id="12261-149">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="12261-150">Talning lína</span><span class="sxs-lookup"><span data-stu-id="12261-150">Lines counting</span></span>  
34. <span data-ttu-id="12261-151">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="12261-151">Click OK.</span></span>
35. <span data-ttu-id="12261-152">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="12261-152">Click Add String.</span></span>
36. <span data-ttu-id="12261-153">Í svæðið Heiti, færðu inn 'heildarupphæð'.</span><span class="sxs-lookup"><span data-stu-id="12261-153">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="12261-154">Heildarfjöldi</span><span class="sxs-lookup"><span data-stu-id="12261-154">Total amount</span></span>  
37. <span data-ttu-id="12261-155">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="12261-155">Click OK.</span></span>
38. <span data-ttu-id="12261-156">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="12261-156">Click the Mapping tab.</span></span>
39. <span data-ttu-id="12261-157">Í trénu skal velja '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="12261-157">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="12261-158">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="12261-158">Click Bind.</span></span>
    * <span data-ttu-id="12261-159">Stofna línu fyrir hverja blokk sem er lögð á minni.</span><span class="sxs-lookup"><span data-stu-id="12261-159">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="12261-160">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="12261-160">Click the Format tab.</span></span>
42. <span data-ttu-id="12261-161">Í trénu skal velja 'Intrastat\Data\Totals by blocks\Block code'.</span><span class="sxs-lookup"><span data-stu-id="12261-161">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="12261-162">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="12261-162">Click the Mapping tab.</span></span>
44. <span data-ttu-id="12261-163">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="12261-163">Click Edit formula.</span></span>
45. <span data-ttu-id="12261-164">Í reitinn Formúla skal færa inn „„Kenni blokkar: “ & “.</span><span class="sxs-lookup"><span data-stu-id="12261-164">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="12261-165">„Kenni blokkar: “ &</span><span class="sxs-lookup"><span data-stu-id="12261-165">"Block id: " &</span></span>  
46. <span data-ttu-id="12261-166">Í trénu skal víkka út '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="12261-166">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="12261-167">Í trénu skal velja '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="12261-167">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="12261-168">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="12261-168">Click Add data source.</span></span>
49. <span data-ttu-id="12261-169">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="12261-169">Click Save.</span></span>
50. <span data-ttu-id="12261-170">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="12261-170">Close the page.</span></span>
51. <span data-ttu-id="12261-171">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="12261-171">Click the Format tab.</span></span>
52. <span data-ttu-id="12261-172">Í trénu skal velja 'Intrastat\Data\Totals by blocks\Lines counting'.</span><span class="sxs-lookup"><span data-stu-id="12261-172">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="12261-173">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="12261-173">Click the Mapping tab.</span></span>
54. <span data-ttu-id="12261-174">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="12261-174">Click Edit formula.</span></span>
    * <span data-ttu-id="12261-175">Stofna úttak fyrir fjölda lína fyrir hverja blokk sem er sýnd í þessari skýrslu.</span><span class="sxs-lookup"><span data-stu-id="12261-175">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="12261-176">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& “.</span><span class="sxs-lookup"><span data-stu-id="12261-176">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="12261-177">„Fjöldi lína í þessari blokk“ &</span><span class="sxs-lookup"><span data-stu-id="12261-177">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="12261-178">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(“.</span><span class="sxs-lookup"><span data-stu-id="12261-178">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="12261-179">„fjöldi lína í þessari blokk:“ .& TEXT(</span><span class="sxs-lookup"><span data-stu-id="12261-179">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="12261-180">Í trénu skal velja 'Data collection functions\COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="12261-180">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="12261-181">Smelltu á Bæta við Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="12261-181">Click Add function.</span></span>
59. <span data-ttu-id="12261-182">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="12261-182">Click Add data source.</span></span>
60. <span data-ttu-id="12261-183">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(COUNTIFS(„$BlockName“, “.</span><span class="sxs-lookup"><span data-stu-id="12261-183">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="12261-184">„Fjöldi lína í þessari blokk: “ & TEXT(COUNTIFS(„$BlockName“,</span><span class="sxs-lookup"><span data-stu-id="12261-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="12261-185">Í trénu skal víkka út '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="12261-185">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="12261-186">Í trénu skal velja '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="12261-186">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="12261-187">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="12261-187">Click Add data source.</span></span>
64. <span data-ttu-id="12261-188">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value, “.</span><span class="sxs-lookup"><span data-stu-id="12261-188">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="12261-189">„Fjöldi lína í þessari blokk: “ & TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value,</span><span class="sxs-lookup"><span data-stu-id="12261-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="12261-190">Í trénu skal velja '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="12261-190">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="12261-191">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="12261-191">Click Add data source.</span></span>
67. <span data-ttu-id="12261-192">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))“.</span><span class="sxs-lookup"><span data-stu-id="12261-192">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="12261-193">„Fjöldi lína í þessari blokk: “ & TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))</span><span class="sxs-lookup"><span data-stu-id="12261-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="12261-194">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="12261-194">Click Save.</span></span>
69. <span data-ttu-id="12261-195">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="12261-195">Close the page.</span></span>
70. <span data-ttu-id="12261-196">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="12261-196">Click the Format tab.</span></span>
71. <span data-ttu-id="12261-197">Í trénu skal velja 'Intrastat\Data\Totals by blocks\Total amount'.</span><span class="sxs-lookup"><span data-stu-id="12261-197">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="12261-198">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="12261-198">Click the Mapping tab.</span></span>
73. <span data-ttu-id="12261-199">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="12261-199">Click Edit formula.</span></span>
    * <span data-ttu-id="12261-200">Stofna úttak sem verður heildarupphæð reikningsfærðrar upphæðar fyrir hverja blokk sem er sýnd í þessari skýrslu.</span><span class="sxs-lookup"><span data-stu-id="12261-200">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="12261-201">Í reitnum formúla skal færa inn „„Samtala reikningsfærðra upphæða:" TEXT(SUMIFS(„$InvName“, „$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))“.</span><span class="sxs-lookup"><span data-stu-id="12261-201">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="12261-202">„Samtala reikningsfærðra upphæða:" TEXT(SUMIFS(„$InvName“, „$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))</span><span class="sxs-lookup"><span data-stu-id="12261-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="12261-203">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="12261-203">Click Save.</span></span>
76. <span data-ttu-id="12261-204">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="12261-204">Close the page.</span></span>
77. <span data-ttu-id="12261-205">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="12261-205">Click Save.</span></span>
78. <span data-ttu-id="12261-206">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="12261-206">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]