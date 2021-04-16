---
title: Rafræn skýrslugerð Skilgreina snið til að gera talningu og samlagningu (Hluti 2 - skilgreina útreikninga)
description: Í þessu efni er útskýrt hvernig á að skilgreina snið rafrænnar skýrslugerðar til að telja og gera samantekt sem byggist á gögnum fyrir þegar myndað úttak texta. (Hluti 2)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a14fe079515b176cbcda74852ae2ad456dd6434a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749022"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="a2bbf-104">Rafræn skýrslugerð Skilgreina snið til að gera talningu og samlagningu (Hluti 2 - skilgreina útreikninga)</span><span class="sxs-lookup"><span data-stu-id="a2bbf-104">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a2bbf-105">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="a2bbf-106">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="a2bbf-107">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð skilgreingasnið sér um að telja og taka saman (Hluti 1: stofna snið)”.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="a2bbf-108">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="a2bbf-109">Stofna skilgreiningu á sniði til að bæta við upplýsingar um talningu og samlagningu</span><span class="sxs-lookup"><span data-stu-id="a2bbf-109">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="a2bbf-110">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a2bbf-111">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="a2bbf-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="a2bbf-112">Í trénu skal víkka út 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="a2bbf-113">Í trénu skal velja 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-113">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="a2bbf-114">Gefum okkur að sérsníða þurfi sniðið sem Microsoft útvegar með því að bæta línum með samantektarupplýsingum við lok intrastat-skýrslu.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-114">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="a2bbf-115">Þú gerir það með því að sækja okkar eigin tilvik af intrastat-skilgreiningu úr Microsoft-tilvikinu til að gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-115">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="a2bbf-116">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-116">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="a2bbf-117">Í svæðinu Nýtt, veljið 'Leiða af nafni: Intrastat (DE), Microsoft'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-117">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="a2bbf-118">Í svæðið Heiti, sláðu inn „Intrastat (DE) með talningu & samlagningu“.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-118">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="a2bbf-119">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-119">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="a2bbf-120">Skilgreina þessa skýrslu til að gera talningu og samlagningu á grundvelli upplýsinga um úttak.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-120">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="a2bbf-121">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-121">Click Designer.</span></span>
2. <span data-ttu-id="a2bbf-122">Veldu Já í reitnum safna saman upplýsingum um framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-122">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="a2bbf-123">Þetta flagg virkjar ferlið við að safna saman úttaksupplýsingum til að mynda intrastat-skrána á keyrslutima.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-123">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="a2bbf-124">Þú þarft að telja fyrir mismunandi intrastat-stefnur, svo bæta skal sérstakri tölusetningu fyrir líkan við lista gagnaveitu fyrir þessa skilgreiningu sniðs.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-124">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="a2bbf-125">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-125">Click the Mapping tab.</span></span>
4. <span data-ttu-id="a2bbf-126">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-126">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="a2bbf-127">Í trénu skal velja 'Data model\Enumeration '.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-127">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="a2bbf-128">Í reitnum Heiti skal færa inn ‚Stefna'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-128">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="a2bbf-129">Sláið inn eða veldu gildi í reitnum tölusetning líkans.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-129">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="a2bbf-130">Veldu gildið Stefna.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-130">Select the value Direction.</span></span>  
8. <span data-ttu-id="a2bbf-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-131">Click OK.</span></span>
9. <span data-ttu-id="a2bbf-132">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-132">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="a2bbf-133">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-133">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="a2bbf-134">Í svæðið Heiti, færðu inn '$BlockName'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-134">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="a2bbf-135">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-135">Click Edit formula.</span></span>
13. <span data-ttu-id="a2bbf-136">Í reitinn Formúla skal færa inn '"block"'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-136">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="a2bbf-137">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-137">Click Save.</span></span>
15. <span data-ttu-id="a2bbf-138">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-138">Close the page.</span></span>
16. <span data-ttu-id="a2bbf-139">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-139">Click OK.</span></span>
17. <span data-ttu-id="a2bbf-140">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-140">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="a2bbf-141">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-141">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="a2bbf-142">Í svæðið Heiti, færðu inn '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-142">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="a2bbf-143">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-143">Click Edit formula.</span></span>
21. <span data-ttu-id="a2bbf-144">Í reitinn Formúla skal færa inn '"record"'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-144">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="a2bbf-145">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-145">Click Save.</span></span>
23. <span data-ttu-id="a2bbf-146">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-146">Close the page.</span></span>
24. <span data-ttu-id="a2bbf-147">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-147">Click OK.</span></span>
25. <span data-ttu-id="a2bbf-148">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-148">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="a2bbf-149">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-149">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="a2bbf-150">Í svæðið Heiti, færðu inn '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-150">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="a2bbf-151">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-151">Click Edit formula.</span></span>
29. <span data-ttu-id="a2bbf-152">Í reitinn Formúla skal færa inn '"InvoicedAmountEUR"'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-152">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="a2bbf-153">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-153">Click Save.</span></span>
31. <span data-ttu-id="a2bbf-154">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-154">Close the page.</span></span>
32. <span data-ttu-id="a2bbf-155">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-155">Click OK.</span></span>
33. <span data-ttu-id="a2bbf-156">Í trénu skal velja 'Intrastat\Data'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-156">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="a2bbf-157">Smeltu á hnappinn breyta fyrir reitinn „Heiti lykils fyrir söfnuð gögn”.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-157">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="a2bbf-158">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-158">Click Add data source.</span></span>
    * <span data-ttu-id="a2bbf-159">$BlockName</span><span class="sxs-lookup"><span data-stu-id="a2bbf-159">$BlockName</span></span>  
36. <span data-ttu-id="a2bbf-160">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-160">Click Save.</span></span>
37. <span data-ttu-id="a2bbf-161">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-161">Close the page.</span></span>
38. <span data-ttu-id="a2bbf-162">Smellið á hnappinn Breyta fyrir reitinn gildi lykils uppsafnaðra gagna</span><span class="sxs-lookup"><span data-stu-id="a2bbf-162">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="a2bbf-163">Í reitinn Formúlu skal færa inn 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-163">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="a2bbf-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, “Import”, “Export”)</span><span class="sxs-lookup"><span data-stu-id="a2bbf-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="a2bbf-165">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-165">Click Save.</span></span>
41. <span data-ttu-id="a2bbf-166">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-166">Close the page.</span></span>
    * <span data-ttu-id="a2bbf-167">Telja línur í þessari röð.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-167">Count the lines of this sequence.</span></span> <span data-ttu-id="a2bbf-168">Niðurstöður verður notað með heitinu „útiloka” aðskilið fyrir mismunandi stefnur.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-168">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="a2bbf-169">Gildið „Innflutningur” verður notað fyrir allar intrastat-færslur fyrir komur.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-169">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="a2bbf-170">Gildið „Útflutningur” verður notað fyrir allar intrastat-færslur fyrir færslur.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-170">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="a2bbf-171">Líttu á þetta sem sýndar Excel-töflu.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-171">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="a2bbf-172">Fyrir hverja færslu er lína þar sem fyrsti dálkurinn „blokk” er fylltur út með gildunum „Innflutningur” og „Útflutningur” til samræmis.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-172">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="a2bbf-173">Í trénu skal víkka út 'Intrastat\Data: Sequence'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-173">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="a2bbf-174">Í trénu skal velja 'Intrastat\Data: Sequence\Arrivals?'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-174">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="a2bbf-175">Smeltu á hnappinn breyta fyrir reitinn „Heiti lykils fyrir söfnuð gögn”.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-175">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="a2bbf-176">Telja línur í þessari röð.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-176">Count the lines of this sequence.</span></span> <span data-ttu-id="a2bbf-177">Niðurstöðurnar eru geymdar í minni með því að nota heitið „skrá”.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-177">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="a2bbf-178">Í trénu skal velja '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-178">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="a2bbf-179">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-179">Click Add data source.</span></span>
47. <span data-ttu-id="a2bbf-180">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-180">Click Save.</span></span>
48. <span data-ttu-id="a2bbf-181">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-181">Close the page.</span></span>
49. <span data-ttu-id="a2bbf-182">Smeltu á hnappinn breyta fyrir reitinn „Gildi lykils fyrir söfnuð gögn”.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-182">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="a2bbf-183">Í Formúlu svæðinu, færið inn 'Intrastat.CommodityRecord.CommodityCode'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-183">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="a2bbf-184">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-184">Click Save.</span></span>
52. <span data-ttu-id="a2bbf-185">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-185">Close the page.</span></span>
    * <span data-ttu-id="a2bbf-186">Telja línur í þessari röð.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-186">Count the lines of this sequence.</span></span> <span data-ttu-id="a2bbf-187">Niðurstöður verður notað með heitinu „skrá” aðskilið fyrir mismunandi vörukóða.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-187">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="a2bbf-188">Líttu á þetta sem sýndar Excel-töflu.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-188">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="a2bbf-189">Fyrir hverja færslu er lína þar sem fyrsti dálkurinn „blokk” er fylltur út með gildunum „Innflutningur” og „Útflutningur” til samræmis og næsta blokkin „skrá” er fyllt með gildi vörukóða.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-189">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="a2bbf-190">Í trénu skal velja 'Intrastat\Data: Sequence\Dispatches?'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-190">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="a2bbf-191">Smeltu á hnappinn breyta fyrir reitinn „Heiti lykils fyrir söfnuð gögn”.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-191">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="a2bbf-192">Í trénu skal velja '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-192">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="a2bbf-193">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-193">Click Add data source.</span></span>
57. <span data-ttu-id="a2bbf-194">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-194">Click Save.</span></span>
58. <span data-ttu-id="a2bbf-195">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-195">Close the page.</span></span>
59. <span data-ttu-id="a2bbf-196">Smeltu á hnappinn breyta fyrir reitinn „Gildi lykils fyrir söfnuð gögn”.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-196">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="a2bbf-197">Í Formúlu svæðinu, færið inn 'Intrastat.CommodityRecord.CommodityCode'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-197">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="a2bbf-198">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-198">Click Save.</span></span>
62. <span data-ttu-id="a2bbf-199">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-199">Close the page.</span></span>
63. <span data-ttu-id="a2bbf-200">Í trénu skal víkka út 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="a2bbf-201">Í trénu skal víkka út 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record = Intrastat.CommodityRecord'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-201">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="a2bbf-202">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-202">Click the Format tab.</span></span>
66. <span data-ttu-id="a2bbf-203">Í trénu skal velja 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-203">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="a2bbf-204">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-204">Click the Mapping tab.</span></span>
68. <span data-ttu-id="a2bbf-205">Smeltu á hnappinn breyta fyrir reitinn „Heiti lykils fyrir söfnuð gögn”.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-205">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="a2bbf-206">Í trénu skal velja '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-206">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="a2bbf-207">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-207">Click Add data source.</span></span>
71. <span data-ttu-id="a2bbf-208">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-208">Click Save.</span></span>
72. <span data-ttu-id="a2bbf-209">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-209">Close the page.</span></span>
    * <span data-ttu-id="a2bbf-210">Taka saman gildi reikningsfærð upphæð fyrir línur í þessari röð.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-210">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="a2bbf-211">Niðurstöður verður notað með heitinu „InvoicedAmountEUR” aðskilið fyrir mismunandi intrastat-stefnur og vörukóða.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-211">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="a2bbf-212">Líttu á þetta sem sýndarsköpun í Excel-töflu.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-212">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="a2bbf-213">Fyrir hverja færslu er lína þar sem fyrsti dálkurinn „blokk” er fylltur út með gildunum „Innflutningur” og „Útflutningur” til samræmis.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-213">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="a2bbf-214">Önnur blokk „skrá” er fyllt út með gildi vörukóða og þriðja dálkinn „InvoicedAmountEUR” er fyllt út með gildi upphæðar reiknings.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-214">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="a2bbf-215">Í trénu skal víkka út 'Intrastat\Data\Arrivals?'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-215">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="a2bbf-216">Í trénu skal víkka út 'Intrastat\Data\Arrivals?\Record = Intrastat.CommodityRecord'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-216">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="a2bbf-217">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-217">Click the Format tab.</span></span>
76. <span data-ttu-id="a2bbf-218">Í trénu skal velja 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-218">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="a2bbf-219">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-219">Click the Mapping tab.</span></span>
78. <span data-ttu-id="a2bbf-220">Smeltu á hnappinn breyta fyrir reitinn „Heiti lykils fyrir söfnuð gögn”.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-220">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="a2bbf-221">Í trénu skal velja '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-221">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="a2bbf-222">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-222">Click Add data source.</span></span>
81. <span data-ttu-id="a2bbf-223">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-223">Click Save.</span></span>
82. <span data-ttu-id="a2bbf-224">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-224">Close the page.</span></span>
83. <span data-ttu-id="a2bbf-225">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-225">Click Save.</span></span>
84. <span data-ttu-id="a2bbf-226">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a2bbf-226">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]