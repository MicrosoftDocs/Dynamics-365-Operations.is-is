---
title: Rafræn skýrslugerð skilgreingasnið sér um að telja og leggja saman (Hluti 3 - Nota útreikninga til að búa til úttak)
description: Í þessu efni er útskýrt hvernig á að skilgreina snið rafrænnar skýrslugerðar til að telja og gera samantekt sem byggist á gögnum fyrir þegar myndað úttak texta. (Hluti 3)
author: NickSelin
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
ms.openlocfilehash: 7073539ed4c1d9d5acbb0ca84b43538d87fc8b4b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748998"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="6d4e4-104">Rafræn skýrslugerð skilgreingasnið sér um að telja og leggja saman (Hluti 3 - Nota útreikninga til að búa til úttak)</span><span class="sxs-lookup"><span data-stu-id="6d4e4-104">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6d4e4-105">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="6d4e4-106">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="6d4e4-107">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð skilgreingasnið sér um að telja og taka saman (Hluti 2: skilgreina útreikninga)”.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="6d4e4-108">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="6d4e4-109">Skilgreina þessa skýrslu til að nota upplýsingar um talningu og samlagningu</span><span class="sxs-lookup"><span data-stu-id="6d4e4-109">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="6d4e4-110">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="6d4e4-111">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="6d4e4-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="6d4e4-112">Í trénu skal víkka út 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="6d4e4-113">Í trénu skal víkka út 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="6d4e4-114">Í trénu skal velja „Intrastat model\Intrastat (DE)\Intrastat (DE) með talningu & samlagningu“.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="6d4e4-115">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-115">Click Designer.</span></span>
7. <span data-ttu-id="6d4e4-116">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-116">Click the Mapping tab.</span></span>
8. <span data-ttu-id="6d4e4-117">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-117">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="6d4e4-118">Bæta við nýjum gagnagjafa til að fá lista yfir blokkir sem voru lagðar á minni.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-118">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="6d4e4-119">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-119">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="6d4e4-120">Í svæðið Heiti, færðu inn '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-120">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="6d4e4-121">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="6d4e4-121">$BlocksList</span></span>  
11. <span data-ttu-id="6d4e4-122">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-122">Click Edit formula.</span></span>
12. <span data-ttu-id="6d4e4-123">Í trénu skal velja 'Data collection functions\COLLECTEDLIST'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-123">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="6d4e4-124">Smelltu á Bæta við Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-124">Click Add function.</span></span>
14. <span data-ttu-id="6d4e4-125">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-125">Click Add data source.</span></span>
15. <span data-ttu-id="6d4e4-126">Í Formúlu svæðinu, færið inn 'COLLECTEDLIST('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-126">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="6d4e4-127">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="6d4e4-127">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="6d4e4-128">Í Formúlu svæðinu, færið inn 'COLLECTEDLIST('$BlockName', "\*")'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-128">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="6d4e4-129">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="6d4e4-129">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="6d4e4-130">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-130">Click Save.</span></span>
    * <span data-ttu-id="6d4e4-131">Mynstrið „\*” þýðir að allar blokkir verða teknar með í lista fyrir þessa skrá.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-131">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="6d4e4-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-132">Close the page.</span></span>
19. <span data-ttu-id="6d4e4-133">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-133">Click OK.</span></span>
20. <span data-ttu-id="6d4e4-134">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-134">Click the Format tab.</span></span>
21. <span data-ttu-id="6d4e4-135">Í trénu skal velja 'Intrastat\Data'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-135">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="6d4e4-136">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-136">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="6d4e4-137">Í trénu skal velja 'Text\Sequence'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-137">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="6d4e4-138">Í svæðið Heiti, færðu inn 'Samtölur eftir blokkum'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-138">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="6d4e4-139">Samtölur eftir blokkum</span><span class="sxs-lookup"><span data-stu-id="6d4e4-139">Totals by blocks</span></span>  
25. <span data-ttu-id="6d4e4-140">Í reitnum sérstafir skal velja "ný lína - Windows (CR LF)".</span><span class="sxs-lookup"><span data-stu-id="6d4e4-140">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="6d4e4-141">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-141">Click OK.</span></span>
27. <span data-ttu-id="6d4e4-142">Í trénu skal velja 'Intrastat\Data\Totals by blocks'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-142">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="6d4e4-143">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-143">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="6d4e4-144">Í trénu skal velja ‚Texti/Strengur'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-144">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="6d4e4-145">Í svæðið Heiti, færðu inn "kóði blokkar"</span><span class="sxs-lookup"><span data-stu-id="6d4e4-145">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="6d4e4-146">Kóði blokkar</span><span class="sxs-lookup"><span data-stu-id="6d4e4-146">Block code</span></span>  
31. <span data-ttu-id="6d4e4-147">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-147">Click OK.</span></span>
32. <span data-ttu-id="6d4e4-148">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-148">Click Add String.</span></span>
33. <span data-ttu-id="6d4e4-149">Í svæðið Heiti, færðu inn 'talning lína'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-149">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="6d4e4-150">Talning lína</span><span class="sxs-lookup"><span data-stu-id="6d4e4-150">Lines counting</span></span>  
34. <span data-ttu-id="6d4e4-151">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-151">Click OK.</span></span>
35. <span data-ttu-id="6d4e4-152">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-152">Click Add String.</span></span>
36. <span data-ttu-id="6d4e4-153">Í svæðið Heiti, færðu inn 'heildarupphæð'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-153">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="6d4e4-154">Heildarfjöldi</span><span class="sxs-lookup"><span data-stu-id="6d4e4-154">Total amount</span></span>  
37. <span data-ttu-id="6d4e4-155">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-155">Click OK.</span></span>
38. <span data-ttu-id="6d4e4-156">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-156">Click the Mapping tab.</span></span>
39. <span data-ttu-id="6d4e4-157">Í trénu skal velja '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-157">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="6d4e4-158">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-158">Click Bind.</span></span>
    * <span data-ttu-id="6d4e4-159">Stofna línu fyrir hverja blokk sem er lögð á minni.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-159">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="6d4e4-160">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-160">Click the Format tab.</span></span>
42. <span data-ttu-id="6d4e4-161">Í trénu skal velja 'Intrastat\Data\Totals by blocks\Block code'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-161">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="6d4e4-162">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-162">Click the Mapping tab.</span></span>
44. <span data-ttu-id="6d4e4-163">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-163">Click Edit formula.</span></span>
45. <span data-ttu-id="6d4e4-164">Í reitinn Formúla skal færa inn „„Kenni blokkar: “ & “.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-164">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="6d4e4-165">„Kenni blokkar: “ &</span><span class="sxs-lookup"><span data-stu-id="6d4e4-165">"Block id: " &</span></span>  
46. <span data-ttu-id="6d4e4-166">Í trénu skal víkka út '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-166">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="6d4e4-167">Í trénu skal velja '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-167">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="6d4e4-168">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-168">Click Add data source.</span></span>
49. <span data-ttu-id="6d4e4-169">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-169">Click Save.</span></span>
50. <span data-ttu-id="6d4e4-170">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-170">Close the page.</span></span>
51. <span data-ttu-id="6d4e4-171">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-171">Click the Format tab.</span></span>
52. <span data-ttu-id="6d4e4-172">Í trénu skal velja 'Intrastat\Data\Totals by blocks\Lines counting'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-172">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="6d4e4-173">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-173">Click the Mapping tab.</span></span>
54. <span data-ttu-id="6d4e4-174">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-174">Click Edit formula.</span></span>
    * <span data-ttu-id="6d4e4-175">Stofna úttak fyrir fjölda lína fyrir hverja blokk sem er sýnd í þessari skýrslu.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-175">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="6d4e4-176">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& “.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-176">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="6d4e4-177">„Fjöldi lína í þessari blokk“ &</span><span class="sxs-lookup"><span data-stu-id="6d4e4-177">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="6d4e4-178">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(“.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-178">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="6d4e4-179">„fjöldi lína í þessari blokk:“ .& TEXT(</span><span class="sxs-lookup"><span data-stu-id="6d4e4-179">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="6d4e4-180">Í trénu skal velja 'Data collection functions\COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-180">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="6d4e4-181">Smelltu á Bæta við Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-181">Click Add function.</span></span>
59. <span data-ttu-id="6d4e4-182">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-182">Click Add data source.</span></span>
60. <span data-ttu-id="6d4e4-183">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(COUNTIFS(„$BlockName“, “.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-183">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="6d4e4-184">„Fjöldi lína í þessari blokk: “ & TEXT(COUNTIFS(„$BlockName“,</span><span class="sxs-lookup"><span data-stu-id="6d4e4-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="6d4e4-185">Í trénu skal víkka út '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-185">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="6d4e4-186">Í trénu skal velja '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-186">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="6d4e4-187">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-187">Click Add data source.</span></span>
64. <span data-ttu-id="6d4e4-188">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value, “.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-188">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="6d4e4-189">„Fjöldi lína í þessari blokk: “ & TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value,</span><span class="sxs-lookup"><span data-stu-id="6d4e4-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="6d4e4-190">Í trénu skal velja '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-190">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="6d4e4-191">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-191">Click Add data source.</span></span>
67. <span data-ttu-id="6d4e4-192">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))“.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-192">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="6d4e4-193">„Fjöldi lína í þessari blokk: “ & TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))</span><span class="sxs-lookup"><span data-stu-id="6d4e4-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="6d4e4-194">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-194">Click Save.</span></span>
69. <span data-ttu-id="6d4e4-195">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-195">Close the page.</span></span>
70. <span data-ttu-id="6d4e4-196">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-196">Click the Format tab.</span></span>
71. <span data-ttu-id="6d4e4-197">Í trénu skal velja 'Intrastat\Data\Totals by blocks\Total amount'.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-197">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="6d4e4-198">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-198">Click the Mapping tab.</span></span>
73. <span data-ttu-id="6d4e4-199">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-199">Click Edit formula.</span></span>
    * <span data-ttu-id="6d4e4-200">Stofna úttak sem verður heildarupphæð reikningsfærðrar upphæðar fyrir hverja blokk sem er sýnd í þessari skýrslu.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-200">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="6d4e4-201">Í reitnum formúla skal færa inn „„Samtala reikningsfærðra upphæða:" TEXT(SUMIFS(„$InvName“, „$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))“.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-201">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="6d4e4-202">„Samtala reikningsfærðra upphæða:" TEXT(SUMIFS(„$InvName“, „$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))</span><span class="sxs-lookup"><span data-stu-id="6d4e4-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="6d4e4-203">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-203">Click Save.</span></span>
76. <span data-ttu-id="6d4e4-204">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-204">Close the page.</span></span>
77. <span data-ttu-id="6d4e4-205">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-205">Click Save.</span></span>
78. <span data-ttu-id="6d4e4-206">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6d4e4-206">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]