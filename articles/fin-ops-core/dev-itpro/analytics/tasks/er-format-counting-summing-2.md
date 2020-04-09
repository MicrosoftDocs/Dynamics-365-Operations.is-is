---
title: Rafræn skýrslugerð Skilgreina snið til að gera talningu og samlagningu (Hluti 2 - skilgreina útreikninga)
description: Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 20188438a4ca623fc926e6c373fb002f148c3df4
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142479"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="9448b-103">Rafræn skýrslugerð Skilgreina snið til að gera talningu og samlagningu (Hluti 2 - skilgreina útreikninga)</span><span class="sxs-lookup"><span data-stu-id="9448b-103">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9448b-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað.</span><span class="sxs-lookup"><span data-stu-id="9448b-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="9448b-105">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="9448b-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="9448b-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð skilgreingasnið sér um að telja og taka saman (Hluti 1: stofna snið)”.</span><span class="sxs-lookup"><span data-stu-id="9448b-106">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="9448b-107">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="9448b-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="9448b-108">Stofna skilgreiningu á sniði til að bæta við upplýsingar um talningu og samlagningu</span><span class="sxs-lookup"><span data-stu-id="9448b-108">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="9448b-109">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="9448b-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="9448b-110">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="9448b-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="9448b-111">Í trénu skal víkka út 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="9448b-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="9448b-112">Í trénu skal velja 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="9448b-112">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="9448b-113">Gefum okkur að sérsníða þurfi sniðið sem Microsoft útvegar með því að bæta línum með samantektarupplýsingum við lok intrastat-skýrslu.</span><span class="sxs-lookup"><span data-stu-id="9448b-113">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="9448b-114">Þú gerir það með því að sækja okkar eigin tilvik af intrastat-skilgreiningu úr Microsoft-tilvikinu til að gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="9448b-114">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="9448b-115">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="9448b-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="9448b-116">Í svæðinu Nýtt, veljið 'Leiða af nafni: Intrastat (DE), Microsoft'.</span><span class="sxs-lookup"><span data-stu-id="9448b-116">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="9448b-117">Í svæðið Heiti, sláðu inn „Intrastat (DE) með talningu & samlagningu“.</span><span class="sxs-lookup"><span data-stu-id="9448b-117">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="9448b-118">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="9448b-118">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="9448b-119">Skilgreina þessa skýrslu til að gera talningu og samlagningu á grundvelli upplýsinga um úttak.</span><span class="sxs-lookup"><span data-stu-id="9448b-119">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="9448b-120">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="9448b-120">Click Designer.</span></span>
2. <span data-ttu-id="9448b-121">Veldu Já í reitnum safna saman upplýsingum um framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="9448b-121">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="9448b-122">Þetta flagg virkjar ferlið við að safna saman úttaksupplýsingum til að mynda intrastat-skrána á keyrslutima.</span><span class="sxs-lookup"><span data-stu-id="9448b-122">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="9448b-123">Þú þarft að telja fyrir mismunandi intrastat-stefnur, svo bæta skal sérstakri tölusetningu fyrir líkan við lista gagnaveitu fyrir þessa skilgreiningu sniðs.</span><span class="sxs-lookup"><span data-stu-id="9448b-123">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="9448b-124">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="9448b-124">Click the Mapping tab.</span></span>
4. <span data-ttu-id="9448b-125">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9448b-125">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="9448b-126">Í trénu skal velja 'Data model\Enumeration '.</span><span class="sxs-lookup"><span data-stu-id="9448b-126">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="9448b-127">Í reitnum Heiti skal færa inn ‚Stefna'.</span><span class="sxs-lookup"><span data-stu-id="9448b-127">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="9448b-128">Sláið inn eða veldu gildi í reitnum tölusetning líkans.</span><span class="sxs-lookup"><span data-stu-id="9448b-128">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="9448b-129">Veldu gildið Stefna.</span><span class="sxs-lookup"><span data-stu-id="9448b-129">Select the value Direction.</span></span>  
8. <span data-ttu-id="9448b-130">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9448b-130">Click OK.</span></span>
9. <span data-ttu-id="9448b-131">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9448b-131">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="9448b-132">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="9448b-132">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="9448b-133">Í svæðið Heiti, færðu inn '$BlockName'.</span><span class="sxs-lookup"><span data-stu-id="9448b-133">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="9448b-134">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="9448b-134">Click Edit formula.</span></span>
13. <span data-ttu-id="9448b-135">Í reitinn Formúla skal færa inn '"block"'.</span><span class="sxs-lookup"><span data-stu-id="9448b-135">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="9448b-136">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9448b-136">Click Save.</span></span>
15. <span data-ttu-id="9448b-137">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9448b-137">Close the page.</span></span>
16. <span data-ttu-id="9448b-138">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9448b-138">Click OK.</span></span>
17. <span data-ttu-id="9448b-139">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9448b-139">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="9448b-140">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="9448b-140">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="9448b-141">Í svæðið Heiti, færðu inn '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="9448b-141">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="9448b-142">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="9448b-142">Click Edit formula.</span></span>
21. <span data-ttu-id="9448b-143">Í reitinn Formúla skal færa inn '"record"'.</span><span class="sxs-lookup"><span data-stu-id="9448b-143">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="9448b-144">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9448b-144">Click Save.</span></span>
23. <span data-ttu-id="9448b-145">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9448b-145">Close the page.</span></span>
24. <span data-ttu-id="9448b-146">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9448b-146">Click OK.</span></span>
25. <span data-ttu-id="9448b-147">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9448b-147">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="9448b-148">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="9448b-148">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="9448b-149">Í svæðið Heiti, færðu inn '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="9448b-149">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="9448b-150">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="9448b-150">Click Edit formula.</span></span>
29. <span data-ttu-id="9448b-151">Í reitinn Formúla skal færa inn '"InvoicedAmountEUR"'.</span><span class="sxs-lookup"><span data-stu-id="9448b-151">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="9448b-152">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9448b-152">Click Save.</span></span>
31. <span data-ttu-id="9448b-153">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9448b-153">Close the page.</span></span>
32. <span data-ttu-id="9448b-154">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9448b-154">Click OK.</span></span>
33. <span data-ttu-id="9448b-155">Í trénu skal velja 'Intrastat\Data'.</span><span class="sxs-lookup"><span data-stu-id="9448b-155">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="9448b-156">Smeltu á hnappinn breyta fyrir reitinn „Heiti lykils fyrir söfnuð gögn”.</span><span class="sxs-lookup"><span data-stu-id="9448b-156">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="9448b-157">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="9448b-157">Click Add data source.</span></span>
    * <span data-ttu-id="9448b-158">$BlockName</span><span class="sxs-lookup"><span data-stu-id="9448b-158">$BlockName</span></span>  
36. <span data-ttu-id="9448b-159">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="9448b-159">Click Save.</span></span>
37. <span data-ttu-id="9448b-160">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9448b-160">Close the page.</span></span>
38. <span data-ttu-id="9448b-161">Smellið á hnappinn Breyta fyrir reitinn gildi lykils uppsafnaðra gagna</span><span class="sxs-lookup"><span data-stu-id="9448b-161">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="9448b-162">Í reitinn Formúlu skal færa inn 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span><span class="sxs-lookup"><span data-stu-id="9448b-162">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="9448b-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, “Import”, “Export”)</span><span class="sxs-lookup"><span data-stu-id="9448b-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="9448b-164">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9448b-164">Click Save.</span></span>
41. <span data-ttu-id="9448b-165">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9448b-165">Close the page.</span></span>
    * <span data-ttu-id="9448b-166">Telja línur í þessari röð.</span><span class="sxs-lookup"><span data-stu-id="9448b-166">Count the lines of this sequence.</span></span> <span data-ttu-id="9448b-167">Niðurstöður verður notað með heitinu „útiloka” aðskilið fyrir mismunandi stefnur.</span><span class="sxs-lookup"><span data-stu-id="9448b-167">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="9448b-168">Gildið „Innflutningur” verður notað fyrir allar intrastat-færslur fyrir komur.</span><span class="sxs-lookup"><span data-stu-id="9448b-168">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="9448b-169">Gildið „Útflutningur” verður notað fyrir allar intrastat-færslur fyrir færslur.</span><span class="sxs-lookup"><span data-stu-id="9448b-169">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="9448b-170">Líttu á þetta sem sýndar Excel-töflu.</span><span class="sxs-lookup"><span data-stu-id="9448b-170">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="9448b-171">Fyrir hverja færslu er lína þar sem fyrsti dálkurinn „blokk” er fylltur út með gildunum „Innflutningur” og „Útflutningur” til samræmis.</span><span class="sxs-lookup"><span data-stu-id="9448b-171">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="9448b-172">Í trénu skal víkka út 'Intrastat\Data: Sequence'.</span><span class="sxs-lookup"><span data-stu-id="9448b-172">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="9448b-173">Í trénu skal velja 'Intrastat\Data: Sequence\Arrivals?'.</span><span class="sxs-lookup"><span data-stu-id="9448b-173">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="9448b-174">Smeltu á hnappinn breyta fyrir reitinn „Heiti lykils fyrir söfnuð gögn”.</span><span class="sxs-lookup"><span data-stu-id="9448b-174">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="9448b-175">Telja línur í þessari röð.</span><span class="sxs-lookup"><span data-stu-id="9448b-175">Count the lines of this sequence.</span></span> <span data-ttu-id="9448b-176">Niðurstöðurnar eru geymdar í minni með því að nota heitið „skrá”.</span><span class="sxs-lookup"><span data-stu-id="9448b-176">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="9448b-177">Í trénu skal velja '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="9448b-177">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="9448b-178">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="9448b-178">Click Add data source.</span></span>
47. <span data-ttu-id="9448b-179">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="9448b-179">Click Save.</span></span>
48. <span data-ttu-id="9448b-180">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9448b-180">Close the page.</span></span>
49. <span data-ttu-id="9448b-181">Smeltu á hnappinn breyta fyrir reitinn „Gildi lykils fyrir söfnuð gögn”.</span><span class="sxs-lookup"><span data-stu-id="9448b-181">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="9448b-182">Í Formúlu svæðinu, færið inn 'Intrastat.CommodityRecord.CommodityCode'.</span><span class="sxs-lookup"><span data-stu-id="9448b-182">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="9448b-183">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9448b-183">Click Save.</span></span>
52. <span data-ttu-id="9448b-184">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9448b-184">Close the page.</span></span>
    * <span data-ttu-id="9448b-185">Telja línur í þessari röð.</span><span class="sxs-lookup"><span data-stu-id="9448b-185">Count the lines of this sequence.</span></span> <span data-ttu-id="9448b-186">Niðurstöður verður notað með heitinu „skrá” aðskilið fyrir mismunandi vörukóða.</span><span class="sxs-lookup"><span data-stu-id="9448b-186">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="9448b-187">Líttu á þetta sem sýndar Excel-töflu.</span><span class="sxs-lookup"><span data-stu-id="9448b-187">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="9448b-188">Fyrir hverja færslu er lína þar sem fyrsti dálkurinn „blokk” er fylltur út með gildunum „Innflutningur” og „Útflutningur” til samræmis og næsta blokkin „skrá” er fyllt með gildi vörukóða.</span><span class="sxs-lookup"><span data-stu-id="9448b-188">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="9448b-189">Í trénu skal velja 'Intrastat\Data: Sequence\Dispatches?'.</span><span class="sxs-lookup"><span data-stu-id="9448b-189">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="9448b-190">Smeltu á hnappinn breyta fyrir reitinn „Heiti lykils fyrir söfnuð gögn”.</span><span class="sxs-lookup"><span data-stu-id="9448b-190">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="9448b-191">Í trénu skal velja '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="9448b-191">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="9448b-192">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="9448b-192">Click Add data source.</span></span>
57. <span data-ttu-id="9448b-193">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="9448b-193">Click Save.</span></span>
58. <span data-ttu-id="9448b-194">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9448b-194">Close the page.</span></span>
59. <span data-ttu-id="9448b-195">Smeltu á hnappinn breyta fyrir reitinn „Gildi lykils fyrir söfnuð gögn”.</span><span class="sxs-lookup"><span data-stu-id="9448b-195">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="9448b-196">Í Formúlu svæðinu, færið inn 'Intrastat.CommodityRecord.CommodityCode'.</span><span class="sxs-lookup"><span data-stu-id="9448b-196">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="9448b-197">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="9448b-197">Click Save.</span></span>
62. <span data-ttu-id="9448b-198">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9448b-198">Close the page.</span></span>
63. <span data-ttu-id="9448b-199">Í trénu skal víkka út 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span><span class="sxs-lookup"><span data-stu-id="9448b-199">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="9448b-200">Í trénu skal víkka út 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record = Intrastat.CommodityRecord'.</span><span class="sxs-lookup"><span data-stu-id="9448b-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="9448b-201">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="9448b-201">Click the Format tab.</span></span>
66. <span data-ttu-id="9448b-202">Í trénu skal velja 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span><span class="sxs-lookup"><span data-stu-id="9448b-202">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="9448b-203">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="9448b-203">Click the Mapping tab.</span></span>
68. <span data-ttu-id="9448b-204">Smeltu á hnappinn breyta fyrir reitinn „Heiti lykils fyrir söfnuð gögn”.</span><span class="sxs-lookup"><span data-stu-id="9448b-204">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="9448b-205">Í trénu skal velja '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="9448b-205">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="9448b-206">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="9448b-206">Click Add data source.</span></span>
71. <span data-ttu-id="9448b-207">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9448b-207">Click Save.</span></span>
72. <span data-ttu-id="9448b-208">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9448b-208">Close the page.</span></span>
    * <span data-ttu-id="9448b-209">Taka saman gildi reikningsfærð upphæð fyrir línur í þessari röð.</span><span class="sxs-lookup"><span data-stu-id="9448b-209">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="9448b-210">Niðurstöður verður notað með heitinu „InvoicedAmountEUR” aðskilið fyrir mismunandi intrastat-stefnur og vörukóða.</span><span class="sxs-lookup"><span data-stu-id="9448b-210">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="9448b-211">Líttu á þetta sem sýndarsköpun í Excel-töflu.</span><span class="sxs-lookup"><span data-stu-id="9448b-211">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="9448b-212">Fyrir hverja færslu er lína þar sem fyrsti dálkurinn „blokk” er fylltur út með gildunum „Innflutningur” og „Útflutningur” til samræmis.</span><span class="sxs-lookup"><span data-stu-id="9448b-212">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="9448b-213">Önnur blokk „skrá” er fyllt út með gildi vörukóða og þriðja dálkinn „InvoicedAmountEUR” er fyllt út með gildi upphæðar reiknings.</span><span class="sxs-lookup"><span data-stu-id="9448b-213">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="9448b-214">Í trénu skal víkka út 'Intrastat\Data\Arrivals?'.</span><span class="sxs-lookup"><span data-stu-id="9448b-214">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="9448b-215">Í trénu skal víkka út 'Intrastat\Data\Arrivals?\Record = Intrastat.CommodityRecord'.</span><span class="sxs-lookup"><span data-stu-id="9448b-215">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="9448b-216">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="9448b-216">Click the Format tab.</span></span>
76. <span data-ttu-id="9448b-217">Í trénu skal velja 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span><span class="sxs-lookup"><span data-stu-id="9448b-217">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="9448b-218">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="9448b-218">Click the Mapping tab.</span></span>
78. <span data-ttu-id="9448b-219">Smeltu á hnappinn breyta fyrir reitinn „Heiti lykils fyrir söfnuð gögn”.</span><span class="sxs-lookup"><span data-stu-id="9448b-219">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="9448b-220">Í trénu skal velja '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="9448b-220">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="9448b-221">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="9448b-221">Click Add data source.</span></span>
81. <span data-ttu-id="9448b-222">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9448b-222">Click Save.</span></span>
82. <span data-ttu-id="9448b-223">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9448b-223">Close the page.</span></span>
83. <span data-ttu-id="9448b-224">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9448b-224">Click Save.</span></span>
84. <span data-ttu-id="9448b-225">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9448b-225">Close the page.</span></span>

