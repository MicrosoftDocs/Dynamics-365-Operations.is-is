---
title: Rafræn skýrslugerð skilgreingasnið sér um að telja og leggja saman (Hluti 3 - Nota útreikninga til að búa til úttak)
description: Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c870c134a9dae81cd619268bed7ce545bdd5f52
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "347078"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3-use-computations-to-make-the-output"></a><span data-ttu-id="40b16-103">Rafræn skýrslugerð skilgreingasnið sér um að telja og leggja saman (Hluti 3: Nota útreikninga til að búa til úttak)</span><span class="sxs-lookup"><span data-stu-id="40b16-103">ER Configure format to do counting and summing (Part 3: Use computations to make the output)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="40b16-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað.</span><span class="sxs-lookup"><span data-stu-id="40b16-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="40b16-105">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="40b16-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="40b16-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á "Rafræn skýrslugerð skilgreingasnið sér um að telja og taka saman (Hluti 2: skilgreina útreikninga)" ferli.</span><span class="sxs-lookup"><span data-stu-id="40b16-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="40b16-107">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="40b16-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="40b16-108">Skilgreina þessa skýrslu til að nota upplýsingar um talningu og samlagningu</span><span class="sxs-lookup"><span data-stu-id="40b16-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="40b16-109">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="40b16-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="40b16-110">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="40b16-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="40b16-111">Í trénu skal víkka út 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="40b16-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="40b16-112">Í trénu skal víkka út 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="40b16-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="40b16-113">Í trénu skal velja „Intrastat model\Intrastat (DE)\Intrastat (DE) með talningu & samlagningu“.</span><span class="sxs-lookup"><span data-stu-id="40b16-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="40b16-114">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="40b16-114">Click Designer.</span></span>
7. <span data-ttu-id="40b16-115">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="40b16-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="40b16-116">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="40b16-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="40b16-117">Bæta við nýjum gagnagjafa til að fá lista yfir blokkir sem voru lagðar á minni.</span><span class="sxs-lookup"><span data-stu-id="40b16-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="40b16-118">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="40b16-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="40b16-119">Í svæðið Heiti, færðu inn '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="40b16-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="40b16-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="40b16-120">$BlocksList</span></span>  
11. <span data-ttu-id="40b16-121">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="40b16-121">Click Edit formula.</span></span>
12. <span data-ttu-id="40b16-122">Í trénu skal velja 'Data collection functions\COLLECTEDLIST'.</span><span class="sxs-lookup"><span data-stu-id="40b16-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="40b16-123">Smelltu á Bæta við Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="40b16-123">Click Add function.</span></span>
14. <span data-ttu-id="40b16-124">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="40b16-124">Click Add data source.</span></span>
15. <span data-ttu-id="40b16-125">Í Formúlu svæðinu, færið inn 'COLLECTEDLIST('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="40b16-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="40b16-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="40b16-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="40b16-127">Í Formúlu svæðinu, færið inn 'COLLECTEDLIST('$BlockName', "\*")'.</span><span class="sxs-lookup"><span data-stu-id="40b16-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="40b16-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="40b16-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="40b16-129">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="40b16-129">Click Save.</span></span>
    * <span data-ttu-id="40b16-130">Mynstrið “\*” þýðir að allar blokkir verða teknar með í lista fyrir þessa færslu.</span><span class="sxs-lookup"><span data-stu-id="40b16-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="40b16-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="40b16-131">Close the page.</span></span>
19. <span data-ttu-id="40b16-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="40b16-132">Click OK.</span></span>
20. <span data-ttu-id="40b16-133">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="40b16-133">Click the Format tab.</span></span>
21. <span data-ttu-id="40b16-134">Í trénu skal velja 'Intrastat\Data'.</span><span class="sxs-lookup"><span data-stu-id="40b16-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="40b16-135">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="40b16-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="40b16-136">Í trénu skal velja 'Text\Sequence'.</span><span class="sxs-lookup"><span data-stu-id="40b16-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="40b16-137">Í svæðið Heiti, færðu inn 'Samtölur eftir blokkum'.</span><span class="sxs-lookup"><span data-stu-id="40b16-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="40b16-138">Samtölur eftir blokkum</span><span class="sxs-lookup"><span data-stu-id="40b16-138">Totals by blocks</span></span>  
25. <span data-ttu-id="40b16-139">Í reitnum sérstafir skal velja "ný lína - Windows (CR LF)".</span><span class="sxs-lookup"><span data-stu-id="40b16-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="40b16-140">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="40b16-140">Click OK.</span></span>
27. <span data-ttu-id="40b16-141">Í trénu skal velja 'Intrastat\Data\Totals by blocks'.</span><span class="sxs-lookup"><span data-stu-id="40b16-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="40b16-142">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="40b16-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="40b16-143">Í trénu skal velja ‚Texti/Strengur'.</span><span class="sxs-lookup"><span data-stu-id="40b16-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="40b16-144">Í svæðið Heiti, færðu inn "kóði blokkar"</span><span class="sxs-lookup"><span data-stu-id="40b16-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="40b16-145">Kóði blokkar</span><span class="sxs-lookup"><span data-stu-id="40b16-145">Block code</span></span>  
31. <span data-ttu-id="40b16-146">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="40b16-146">Click OK.</span></span>
32. <span data-ttu-id="40b16-147">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="40b16-147">Click Add String.</span></span>
33. <span data-ttu-id="40b16-148">Í svæðið Heiti, færðu inn 'talning lína'.</span><span class="sxs-lookup"><span data-stu-id="40b16-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="40b16-149">Talning lína</span><span class="sxs-lookup"><span data-stu-id="40b16-149">Lines counting</span></span>  
34. <span data-ttu-id="40b16-150">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="40b16-150">Click OK.</span></span>
35. <span data-ttu-id="40b16-151">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="40b16-151">Click Add String.</span></span>
36. <span data-ttu-id="40b16-152">Í svæðið Heiti, færðu inn 'heildarupphæð'.</span><span class="sxs-lookup"><span data-stu-id="40b16-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="40b16-153">Heildarfjöldi</span><span class="sxs-lookup"><span data-stu-id="40b16-153">Total amount</span></span>  
37. <span data-ttu-id="40b16-154">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="40b16-154">Click OK.</span></span>
38. <span data-ttu-id="40b16-155">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="40b16-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="40b16-156">Í trénu skal velja '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="40b16-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="40b16-157">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="40b16-157">Click Bind.</span></span>
    * <span data-ttu-id="40b16-158">Stofna línu fyrir hverja blokk sem er lögð á minni.</span><span class="sxs-lookup"><span data-stu-id="40b16-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="40b16-159">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="40b16-159">Click the Format tab.</span></span>
42. <span data-ttu-id="40b16-160">Í trénu skal velja 'Intrastat\Data\Totals by blocks\Block code'.</span><span class="sxs-lookup"><span data-stu-id="40b16-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="40b16-161">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="40b16-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="40b16-162">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="40b16-162">Click Edit formula.</span></span>
45. <span data-ttu-id="40b16-163">Í reitinn Formúla skal færa inn „„Kenni blokkar: “ & “.</span><span class="sxs-lookup"><span data-stu-id="40b16-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="40b16-164">„Kenni blokkar: “ &</span><span class="sxs-lookup"><span data-stu-id="40b16-164">"Block id: " &</span></span>  
46. <span data-ttu-id="40b16-165">Í trénu skal víkka út '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="40b16-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="40b16-166">Í trénu skal velja '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="40b16-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="40b16-167">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="40b16-167">Click Add data source.</span></span>
49. <span data-ttu-id="40b16-168">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="40b16-168">Click Save.</span></span>
50. <span data-ttu-id="40b16-169">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="40b16-169">Close the page.</span></span>
51. <span data-ttu-id="40b16-170">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="40b16-170">Click the Format tab.</span></span>
52. <span data-ttu-id="40b16-171">Í trénu skal velja 'Intrastat\Data\Totals by blocks\Lines counting'.</span><span class="sxs-lookup"><span data-stu-id="40b16-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="40b16-172">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="40b16-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="40b16-173">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="40b16-173">Click Edit formula.</span></span>
    * <span data-ttu-id="40b16-174">Stofna úttak fyrir fjölda lína fyrir hverja blokk sem er sýnd í þessari skýrslu.</span><span class="sxs-lookup"><span data-stu-id="40b16-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="40b16-175">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& “.</span><span class="sxs-lookup"><span data-stu-id="40b16-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="40b16-176">„Fjöldi lína í þessari blokk“ &</span><span class="sxs-lookup"><span data-stu-id="40b16-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="40b16-177">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(“.</span><span class="sxs-lookup"><span data-stu-id="40b16-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="40b16-178">„fjöldi lína í þessari blokk:“ .& TEXT(</span><span class="sxs-lookup"><span data-stu-id="40b16-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="40b16-179">Í trénu skal velja 'Data collection functions\COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="40b16-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="40b16-180">Smelltu á Bæta við Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="40b16-180">Click Add function.</span></span>
59. <span data-ttu-id="40b16-181">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="40b16-181">Click Add data source.</span></span>
60. <span data-ttu-id="40b16-182">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(COUNTIFS(„$BlockName“, “.</span><span class="sxs-lookup"><span data-stu-id="40b16-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="40b16-183">„Fjöldi lína í þessari blokk: “ & TEXT(COUNTIFS(„$BlockName“,</span><span class="sxs-lookup"><span data-stu-id="40b16-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="40b16-184">Í trénu skal víkka út '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="40b16-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="40b16-185">Í trénu skal velja '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="40b16-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="40b16-186">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="40b16-186">Click Add data source.</span></span>
64. <span data-ttu-id="40b16-187">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value, “.</span><span class="sxs-lookup"><span data-stu-id="40b16-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="40b16-188">„Fjöldi lína í þessari blokk: “ & TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value,</span><span class="sxs-lookup"><span data-stu-id="40b16-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="40b16-189">Í trénu skal velja '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="40b16-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="40b16-190">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="40b16-190">Click Add data source.</span></span>
67. <span data-ttu-id="40b16-191">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))“.</span><span class="sxs-lookup"><span data-stu-id="40b16-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="40b16-192">„Fjöldi lína í þessari blokk: “ & TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))</span><span class="sxs-lookup"><span data-stu-id="40b16-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="40b16-193">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="40b16-193">Click Save.</span></span>
69. <span data-ttu-id="40b16-194">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="40b16-194">Close the page.</span></span>
70. <span data-ttu-id="40b16-195">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="40b16-195">Click the Format tab.</span></span>
71. <span data-ttu-id="40b16-196">Í trénu skal velja 'Intrastat\Data\Totals by blocks\Total amount'.</span><span class="sxs-lookup"><span data-stu-id="40b16-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="40b16-197">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="40b16-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="40b16-198">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="40b16-198">Click Edit formula.</span></span>
    * <span data-ttu-id="40b16-199">Stofna úttak sem verður heildarupphæð reikningsfærðrar upphæðar fyrir hverja blokk sem er sýnd í þessari skýrslu.</span><span class="sxs-lookup"><span data-stu-id="40b16-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="40b16-200">Í reitnum formúla skal færa inn „„Samtala reikningsfærðra upphæða:"  TEXT(SUMIFS(„$InvName“, „$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))“.</span><span class="sxs-lookup"><span data-stu-id="40b16-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="40b16-201">„Samtala reikningsfærðra upphæða:"  TEXT(SUMIFS(„$InvName“, „$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))</span><span class="sxs-lookup"><span data-stu-id="40b16-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="40b16-202">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="40b16-202">Click Save.</span></span>
76. <span data-ttu-id="40b16-203">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="40b16-203">Close the page.</span></span>
77. <span data-ttu-id="40b16-204">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="40b16-204">Click Save.</span></span>
78. <span data-ttu-id="40b16-205">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="40b16-205">Close the page.</span></span>

