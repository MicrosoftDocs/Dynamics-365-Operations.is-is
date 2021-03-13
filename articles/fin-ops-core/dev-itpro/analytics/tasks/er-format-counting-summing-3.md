---
title: Rafræn skýrslugerð skilgreingasnið sér um að telja og leggja saman (Hluti 3 - Nota útreikninga til að búa til úttak)
description: Í þessu efni er útskýrt hvernig á að skilgreina snið rafrænnar skýrslugerðar til að telja og gera samantekt sem byggist á gögnum fyrir þegar myndað úttak texta. (Hluti 3)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a69dd28051d8e98643eb95c663525075bed8dec
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092973"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="14f79-104">Rafræn skýrslugerð skilgreingasnið sér um að telja og leggja saman (Hluti 3 - Nota útreikninga til að búa til úttak)</span><span class="sxs-lookup"><span data-stu-id="14f79-104">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="14f79-105">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað.</span><span class="sxs-lookup"><span data-stu-id="14f79-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="14f79-106">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="14f79-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="14f79-107">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð skilgreingasnið sér um að telja og taka saman (Hluti 2: skilgreina útreikninga)”.</span><span class="sxs-lookup"><span data-stu-id="14f79-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="14f79-108">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="14f79-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="14f79-109">Skilgreina þessa skýrslu til að nota upplýsingar um talningu og samlagningu</span><span class="sxs-lookup"><span data-stu-id="14f79-109">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="14f79-110">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="14f79-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="14f79-111">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="14f79-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="14f79-112">Í trénu skal víkka út 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="14f79-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="14f79-113">Í trénu skal víkka út 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="14f79-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="14f79-114">Í trénu skal velja „Intrastat model\Intrastat (DE)\Intrastat (DE) með talningu & samlagningu“.</span><span class="sxs-lookup"><span data-stu-id="14f79-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="14f79-115">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="14f79-115">Click Designer.</span></span>
7. <span data-ttu-id="14f79-116">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="14f79-116">Click the Mapping tab.</span></span>
8. <span data-ttu-id="14f79-117">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="14f79-117">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="14f79-118">Bæta við nýjum gagnagjafa til að fá lista yfir blokkir sem voru lagðar á minni.</span><span class="sxs-lookup"><span data-stu-id="14f79-118">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="14f79-119">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="14f79-119">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="14f79-120">Í svæðið Heiti, færðu inn '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="14f79-120">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="14f79-121">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="14f79-121">$BlocksList</span></span>  
11. <span data-ttu-id="14f79-122">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="14f79-122">Click Edit formula.</span></span>
12. <span data-ttu-id="14f79-123">Í trénu skal velja 'Data collection functions\COLLECTEDLIST'.</span><span class="sxs-lookup"><span data-stu-id="14f79-123">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="14f79-124">Smelltu á Bæta við Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="14f79-124">Click Add function.</span></span>
14. <span data-ttu-id="14f79-125">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="14f79-125">Click Add data source.</span></span>
15. <span data-ttu-id="14f79-126">Í Formúlu svæðinu, færið inn 'COLLECTEDLIST('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="14f79-126">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="14f79-127">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="14f79-127">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="14f79-128">Í Formúlu svæðinu, færið inn 'COLLECTEDLIST('$BlockName', "\*")'.</span><span class="sxs-lookup"><span data-stu-id="14f79-128">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="14f79-129">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="14f79-129">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="14f79-130">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="14f79-130">Click Save.</span></span>
    * <span data-ttu-id="14f79-131">Mynstrið „\*” þýðir að allar blokkir verða teknar með í lista fyrir þessa skrá.</span><span class="sxs-lookup"><span data-stu-id="14f79-131">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="14f79-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="14f79-132">Close the page.</span></span>
19. <span data-ttu-id="14f79-133">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="14f79-133">Click OK.</span></span>
20. <span data-ttu-id="14f79-134">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="14f79-134">Click the Format tab.</span></span>
21. <span data-ttu-id="14f79-135">Í trénu skal velja 'Intrastat\Data'.</span><span class="sxs-lookup"><span data-stu-id="14f79-135">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="14f79-136">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="14f79-136">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="14f79-137">Í trénu skal velja 'Text\Sequence'.</span><span class="sxs-lookup"><span data-stu-id="14f79-137">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="14f79-138">Í svæðið Heiti, færðu inn 'Samtölur eftir blokkum'.</span><span class="sxs-lookup"><span data-stu-id="14f79-138">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="14f79-139">Samtölur eftir blokkum</span><span class="sxs-lookup"><span data-stu-id="14f79-139">Totals by blocks</span></span>  
25. <span data-ttu-id="14f79-140">Í reitnum sérstafir skal velja "ný lína - Windows (CR LF)".</span><span class="sxs-lookup"><span data-stu-id="14f79-140">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="14f79-141">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="14f79-141">Click OK.</span></span>
27. <span data-ttu-id="14f79-142">Í trénu skal velja 'Intrastat\Data\Totals by blocks'.</span><span class="sxs-lookup"><span data-stu-id="14f79-142">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="14f79-143">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="14f79-143">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="14f79-144">Í trénu skal velja ‚Texti/Strengur'.</span><span class="sxs-lookup"><span data-stu-id="14f79-144">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="14f79-145">Í svæðið Heiti, færðu inn "kóði blokkar"</span><span class="sxs-lookup"><span data-stu-id="14f79-145">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="14f79-146">Kóði blokkar</span><span class="sxs-lookup"><span data-stu-id="14f79-146">Block code</span></span>  
31. <span data-ttu-id="14f79-147">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="14f79-147">Click OK.</span></span>
32. <span data-ttu-id="14f79-148">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="14f79-148">Click Add String.</span></span>
33. <span data-ttu-id="14f79-149">Í svæðið Heiti, færðu inn 'talning lína'.</span><span class="sxs-lookup"><span data-stu-id="14f79-149">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="14f79-150">Talning lína</span><span class="sxs-lookup"><span data-stu-id="14f79-150">Lines counting</span></span>  
34. <span data-ttu-id="14f79-151">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="14f79-151">Click OK.</span></span>
35. <span data-ttu-id="14f79-152">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="14f79-152">Click Add String.</span></span>
36. <span data-ttu-id="14f79-153">Í svæðið Heiti, færðu inn 'heildarupphæð'.</span><span class="sxs-lookup"><span data-stu-id="14f79-153">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="14f79-154">Heildarfjöldi</span><span class="sxs-lookup"><span data-stu-id="14f79-154">Total amount</span></span>  
37. <span data-ttu-id="14f79-155">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="14f79-155">Click OK.</span></span>
38. <span data-ttu-id="14f79-156">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="14f79-156">Click the Mapping tab.</span></span>
39. <span data-ttu-id="14f79-157">Í trénu skal velja '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="14f79-157">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="14f79-158">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="14f79-158">Click Bind.</span></span>
    * <span data-ttu-id="14f79-159">Stofna línu fyrir hverja blokk sem er lögð á minni.</span><span class="sxs-lookup"><span data-stu-id="14f79-159">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="14f79-160">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="14f79-160">Click the Format tab.</span></span>
42. <span data-ttu-id="14f79-161">Í trénu skal velja 'Intrastat\Data\Totals by blocks\Block code'.</span><span class="sxs-lookup"><span data-stu-id="14f79-161">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="14f79-162">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="14f79-162">Click the Mapping tab.</span></span>
44. <span data-ttu-id="14f79-163">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="14f79-163">Click Edit formula.</span></span>
45. <span data-ttu-id="14f79-164">Í reitinn Formúla skal færa inn „„Kenni blokkar: “ & “.</span><span class="sxs-lookup"><span data-stu-id="14f79-164">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="14f79-165">„Kenni blokkar: “ &</span><span class="sxs-lookup"><span data-stu-id="14f79-165">"Block id: " &</span></span>  
46. <span data-ttu-id="14f79-166">Í trénu skal víkka út '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="14f79-166">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="14f79-167">Í trénu skal velja '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="14f79-167">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="14f79-168">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="14f79-168">Click Add data source.</span></span>
49. <span data-ttu-id="14f79-169">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="14f79-169">Click Save.</span></span>
50. <span data-ttu-id="14f79-170">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="14f79-170">Close the page.</span></span>
51. <span data-ttu-id="14f79-171">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="14f79-171">Click the Format tab.</span></span>
52. <span data-ttu-id="14f79-172">Í trénu skal velja 'Intrastat\Data\Totals by blocks\Lines counting'.</span><span class="sxs-lookup"><span data-stu-id="14f79-172">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="14f79-173">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="14f79-173">Click the Mapping tab.</span></span>
54. <span data-ttu-id="14f79-174">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="14f79-174">Click Edit formula.</span></span>
    * <span data-ttu-id="14f79-175">Stofna úttak fyrir fjölda lína fyrir hverja blokk sem er sýnd í þessari skýrslu.</span><span class="sxs-lookup"><span data-stu-id="14f79-175">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="14f79-176">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& “.</span><span class="sxs-lookup"><span data-stu-id="14f79-176">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="14f79-177">„Fjöldi lína í þessari blokk“ &</span><span class="sxs-lookup"><span data-stu-id="14f79-177">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="14f79-178">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(“.</span><span class="sxs-lookup"><span data-stu-id="14f79-178">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="14f79-179">„fjöldi lína í þessari blokk:“ .& TEXT(</span><span class="sxs-lookup"><span data-stu-id="14f79-179">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="14f79-180">Í trénu skal velja 'Data collection functions\COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="14f79-180">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="14f79-181">Smelltu á Bæta við Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="14f79-181">Click Add function.</span></span>
59. <span data-ttu-id="14f79-182">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="14f79-182">Click Add data source.</span></span>
60. <span data-ttu-id="14f79-183">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(COUNTIFS(„$BlockName“, “.</span><span class="sxs-lookup"><span data-stu-id="14f79-183">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="14f79-184">„Fjöldi lína í þessari blokk: “ & TEXT(COUNTIFS(„$BlockName“,</span><span class="sxs-lookup"><span data-stu-id="14f79-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="14f79-185">Í trénu skal víkka út '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="14f79-185">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="14f79-186">Í trénu skal velja '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="14f79-186">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="14f79-187">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="14f79-187">Click Add data source.</span></span>
64. <span data-ttu-id="14f79-188">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value, “.</span><span class="sxs-lookup"><span data-stu-id="14f79-188">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="14f79-189">„Fjöldi lína í þessari blokk: “ & TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value,</span><span class="sxs-lookup"><span data-stu-id="14f79-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="14f79-190">Í trénu skal velja '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="14f79-190">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="14f79-191">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="14f79-191">Click Add data source.</span></span>
67. <span data-ttu-id="14f79-192">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))“.</span><span class="sxs-lookup"><span data-stu-id="14f79-192">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="14f79-193">„Fjöldi lína í þessari blokk: “ & TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))</span><span class="sxs-lookup"><span data-stu-id="14f79-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="14f79-194">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="14f79-194">Click Save.</span></span>
69. <span data-ttu-id="14f79-195">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="14f79-195">Close the page.</span></span>
70. <span data-ttu-id="14f79-196">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="14f79-196">Click the Format tab.</span></span>
71. <span data-ttu-id="14f79-197">Í trénu skal velja 'Intrastat\Data\Totals by blocks\Total amount'.</span><span class="sxs-lookup"><span data-stu-id="14f79-197">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="14f79-198">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="14f79-198">Click the Mapping tab.</span></span>
73. <span data-ttu-id="14f79-199">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="14f79-199">Click Edit formula.</span></span>
    * <span data-ttu-id="14f79-200">Stofna úttak sem verður heildarupphæð reikningsfærðrar upphæðar fyrir hverja blokk sem er sýnd í þessari skýrslu.</span><span class="sxs-lookup"><span data-stu-id="14f79-200">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="14f79-201">Í reitnum formúla skal færa inn „„Samtala reikningsfærðra upphæða:" TEXT(SUMIFS(„$InvName“, „$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))“.</span><span class="sxs-lookup"><span data-stu-id="14f79-201">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="14f79-202">„Samtala reikningsfærðra upphæða:" TEXT(SUMIFS(„$InvName“, „$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))</span><span class="sxs-lookup"><span data-stu-id="14f79-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="14f79-203">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="14f79-203">Click Save.</span></span>
76. <span data-ttu-id="14f79-204">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="14f79-204">Close the page.</span></span>
77. <span data-ttu-id="14f79-205">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="14f79-205">Click Save.</span></span>
78. <span data-ttu-id="14f79-206">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="14f79-206">Close the page.</span></span>

