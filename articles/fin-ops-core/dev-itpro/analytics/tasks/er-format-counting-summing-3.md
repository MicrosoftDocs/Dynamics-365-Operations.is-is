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
ms.openlocfilehash: 7bbef7048488056f50ec8967a9af53d468666856
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550764"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="05e8b-103">Rafræn skýrslugerð skilgreingasnið sér um að telja og leggja saman (Hluti 3 - Nota útreikninga til að búa til úttak)</span><span class="sxs-lookup"><span data-stu-id="05e8b-103">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="05e8b-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað.</span><span class="sxs-lookup"><span data-stu-id="05e8b-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="05e8b-105">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="05e8b-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="05e8b-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á "Rafræn skýrslugerð skilgreingasnið sér um að telja og taka saman (Hluti 2: skilgreina útreikninga)" ferli.</span><span class="sxs-lookup"><span data-stu-id="05e8b-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="05e8b-107">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="05e8b-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="05e8b-108">Skilgreina þessa skýrslu til að nota upplýsingar um talningu og samlagningu</span><span class="sxs-lookup"><span data-stu-id="05e8b-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="05e8b-109">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="05e8b-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="05e8b-110">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="05e8b-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="05e8b-111">Í trénu skal víkka út 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="05e8b-112">Í trénu skal víkka út 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="05e8b-113">Í trénu skal velja „Intrastat model\Intrastat (DE)\Intrastat (DE) með talningu & samlagningu“.</span><span class="sxs-lookup"><span data-stu-id="05e8b-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="05e8b-114">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="05e8b-114">Click Designer.</span></span>
7. <span data-ttu-id="05e8b-115">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="05e8b-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="05e8b-116">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="05e8b-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="05e8b-117">Bæta við nýjum gagnagjafa til að fá lista yfir blokkir sem voru lagðar á minni.</span><span class="sxs-lookup"><span data-stu-id="05e8b-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="05e8b-118">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="05e8b-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="05e8b-119">Í svæðið Heiti, færðu inn '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="05e8b-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="05e8b-120">$BlocksList</span></span>  
11. <span data-ttu-id="05e8b-121">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="05e8b-121">Click Edit formula.</span></span>
12. <span data-ttu-id="05e8b-122">Í trénu skal velja 'Data collection functions\COLLECTEDLIST'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="05e8b-123">Smelltu á Bæta við Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="05e8b-123">Click Add function.</span></span>
14. <span data-ttu-id="05e8b-124">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="05e8b-124">Click Add data source.</span></span>
15. <span data-ttu-id="05e8b-125">Í Formúlu svæðinu, færið inn 'COLLECTEDLIST('$BlockName', '.</span><span class="sxs-lookup"><span data-stu-id="05e8b-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="05e8b-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="05e8b-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="05e8b-127">Í Formúlu svæðinu, færið inn 'COLLECTEDLIST('$BlockName', "\*")'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="05e8b-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="05e8b-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="05e8b-129">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="05e8b-129">Click Save.</span></span>
    * <span data-ttu-id="05e8b-130">Mynstrið “\*” þýðir að allar blokkir verða teknar með í lista fyrir þessa færslu.</span><span class="sxs-lookup"><span data-stu-id="05e8b-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="05e8b-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="05e8b-131">Close the page.</span></span>
19. <span data-ttu-id="05e8b-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="05e8b-132">Click OK.</span></span>
20. <span data-ttu-id="05e8b-133">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="05e8b-133">Click the Format tab.</span></span>
21. <span data-ttu-id="05e8b-134">Í trénu skal velja 'Intrastat\Data'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="05e8b-135">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="05e8b-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="05e8b-136">Í trénu skal velja 'Text\Sequence'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="05e8b-137">Í svæðið Heiti, færðu inn 'Samtölur eftir blokkum'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="05e8b-138">Samtölur eftir blokkum</span><span class="sxs-lookup"><span data-stu-id="05e8b-138">Totals by blocks</span></span>  
25. <span data-ttu-id="05e8b-139">Í reitnum sérstafir skal velja "ný lína - Windows (CR LF)".</span><span class="sxs-lookup"><span data-stu-id="05e8b-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="05e8b-140">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="05e8b-140">Click OK.</span></span>
27. <span data-ttu-id="05e8b-141">Í trénu skal velja 'Intrastat\Data\Totals by blocks'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="05e8b-142">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="05e8b-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="05e8b-143">Í trénu skal velja ‚Texti/Strengur'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="05e8b-144">Í svæðið Heiti, færðu inn "kóði blokkar"</span><span class="sxs-lookup"><span data-stu-id="05e8b-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="05e8b-145">Kóði blokkar</span><span class="sxs-lookup"><span data-stu-id="05e8b-145">Block code</span></span>  
31. <span data-ttu-id="05e8b-146">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="05e8b-146">Click OK.</span></span>
32. <span data-ttu-id="05e8b-147">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="05e8b-147">Click Add String.</span></span>
33. <span data-ttu-id="05e8b-148">Í svæðið Heiti, færðu inn 'talning lína'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="05e8b-149">Talning lína</span><span class="sxs-lookup"><span data-stu-id="05e8b-149">Lines counting</span></span>  
34. <span data-ttu-id="05e8b-150">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="05e8b-150">Click OK.</span></span>
35. <span data-ttu-id="05e8b-151">Smella á bæta Við Streng.</span><span class="sxs-lookup"><span data-stu-id="05e8b-151">Click Add String.</span></span>
36. <span data-ttu-id="05e8b-152">Í svæðið Heiti, færðu inn 'heildarupphæð'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="05e8b-153">Heildarfjöldi</span><span class="sxs-lookup"><span data-stu-id="05e8b-153">Total amount</span></span>  
37. <span data-ttu-id="05e8b-154">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="05e8b-154">Click OK.</span></span>
38. <span data-ttu-id="05e8b-155">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="05e8b-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="05e8b-156">Í trénu skal velja '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="05e8b-157">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="05e8b-157">Click Bind.</span></span>
    * <span data-ttu-id="05e8b-158">Stofna línu fyrir hverja blokk sem er lögð á minni.</span><span class="sxs-lookup"><span data-stu-id="05e8b-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="05e8b-159">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="05e8b-159">Click the Format tab.</span></span>
42. <span data-ttu-id="05e8b-160">Í trénu skal velja 'Intrastat\Data\Totals by blocks\Block code'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="05e8b-161">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="05e8b-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="05e8b-162">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="05e8b-162">Click Edit formula.</span></span>
45. <span data-ttu-id="05e8b-163">Í reitinn Formúla skal færa inn „„Kenni blokkar: “ & “.</span><span class="sxs-lookup"><span data-stu-id="05e8b-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="05e8b-164">„Kenni blokkar: “ &</span><span class="sxs-lookup"><span data-stu-id="05e8b-164">"Block id: " &</span></span>  
46. <span data-ttu-id="05e8b-165">Í trénu skal víkka út '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="05e8b-166">Í trénu skal velja '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="05e8b-167">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="05e8b-167">Click Add data source.</span></span>
49. <span data-ttu-id="05e8b-168">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="05e8b-168">Click Save.</span></span>
50. <span data-ttu-id="05e8b-169">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="05e8b-169">Close the page.</span></span>
51. <span data-ttu-id="05e8b-170">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="05e8b-170">Click the Format tab.</span></span>
52. <span data-ttu-id="05e8b-171">Í trénu skal velja 'Intrastat\Data\Totals by blocks\Lines counting'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="05e8b-172">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="05e8b-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="05e8b-173">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="05e8b-173">Click Edit formula.</span></span>
    * <span data-ttu-id="05e8b-174">Stofna úttak fyrir fjölda lína fyrir hverja blokk sem er sýnd í þessari skýrslu.</span><span class="sxs-lookup"><span data-stu-id="05e8b-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="05e8b-175">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& “.</span><span class="sxs-lookup"><span data-stu-id="05e8b-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="05e8b-176">„Fjöldi lína í þessari blokk“ &</span><span class="sxs-lookup"><span data-stu-id="05e8b-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="05e8b-177">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(“.</span><span class="sxs-lookup"><span data-stu-id="05e8b-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="05e8b-178">„fjöldi lína í þessari blokk:“ .& TEXT(</span><span class="sxs-lookup"><span data-stu-id="05e8b-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="05e8b-179">Í trénu skal velja 'Data collection functions\COUNTIFS'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="05e8b-180">Smelltu á Bæta við Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="05e8b-180">Click Add function.</span></span>
59. <span data-ttu-id="05e8b-181">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="05e8b-181">Click Add data source.</span></span>
60. <span data-ttu-id="05e8b-182">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(COUNTIFS(„$BlockName“, “.</span><span class="sxs-lookup"><span data-stu-id="05e8b-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="05e8b-183">„Fjöldi lína í þessari blokk: “ & TEXT(COUNTIFS(„$BlockName“,</span><span class="sxs-lookup"><span data-stu-id="05e8b-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="05e8b-184">Í trénu skal víkka út '$BlocksList'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="05e8b-185">Í trénu skal velja '$BlocksList\Value'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="05e8b-186">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="05e8b-186">Click Add data source.</span></span>
64. <span data-ttu-id="05e8b-187">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value, “.</span><span class="sxs-lookup"><span data-stu-id="05e8b-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="05e8b-188">„Fjöldi lína í þessari blokk: “ & TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value,</span><span class="sxs-lookup"><span data-stu-id="05e8b-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="05e8b-189">Í trénu skal velja '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="05e8b-190">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="05e8b-190">Click Add data source.</span></span>
67. <span data-ttu-id="05e8b-191">Í reitnum Formúla skal færa inn „„fjöldi lína í þessari blokk: “ .& TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))“.</span><span class="sxs-lookup"><span data-stu-id="05e8b-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="05e8b-192">„Fjöldi lína í þessari blokk: “ & TEXT(COUNTIFS(„$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))</span><span class="sxs-lookup"><span data-stu-id="05e8b-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="05e8b-193">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="05e8b-193">Click Save.</span></span>
69. <span data-ttu-id="05e8b-194">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="05e8b-194">Close the page.</span></span>
70. <span data-ttu-id="05e8b-195">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="05e8b-195">Click the Format tab.</span></span>
71. <span data-ttu-id="05e8b-196">Í trénu skal velja 'Intrastat\Data\Totals by blocks\Total amount'.</span><span class="sxs-lookup"><span data-stu-id="05e8b-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="05e8b-197">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="05e8b-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="05e8b-198">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="05e8b-198">Click Edit formula.</span></span>
    * <span data-ttu-id="05e8b-199">Stofna úttak sem verður heildarupphæð reikningsfærðrar upphæðar fyrir hverja blokk sem er sýnd í þessari skýrslu.</span><span class="sxs-lookup"><span data-stu-id="05e8b-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="05e8b-200">Í reitnum formúla skal færa inn „„Samtala reikningsfærðra upphæða:" TEXT(SUMIFS(„$InvName“, „$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))“.</span><span class="sxs-lookup"><span data-stu-id="05e8b-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="05e8b-201">„Samtala reikningsfærðra upphæða:" TEXT(SUMIFS(„$InvName“, „$BlockName“, „$BlocksList“.Value, „$RecName“, „\*“))</span><span class="sxs-lookup"><span data-stu-id="05e8b-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="05e8b-202">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="05e8b-202">Click Save.</span></span>
76. <span data-ttu-id="05e8b-203">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="05e8b-203">Close the page.</span></span>
77. <span data-ttu-id="05e8b-204">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="05e8b-204">Click Save.</span></span>
78. <span data-ttu-id="05e8b-205">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="05e8b-205">Close the page.</span></span>

