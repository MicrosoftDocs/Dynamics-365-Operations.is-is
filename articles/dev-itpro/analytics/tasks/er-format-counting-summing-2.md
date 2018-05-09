--- 
title: "Grunnstilla útreikninga fyrir talningu og samlagningu"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 06a9f544bebfa1990783e35065c843b937c5b3e4
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="configure-computations-to-do-counting-and-summing"></a><span data-ttu-id="b1a9e-103">Grunnstilla útreikninga fyrir talningu og samlagningu</span><span class="sxs-lookup"><span data-stu-id="b1a9e-103">Configure computations to do counting and summing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b1a9e-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="b1a9e-105">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="b1a9e-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á “Rafræn skýrslugerð skilgreingasnið sér um að telja og taka saman (Hluti 1: stofna snið)” ferli.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 1: Create format)” procedure.</span></span>

<span data-ttu-id="b1a9e-107">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="b1a9e-108">Stofna skilgreiningu á sniði til að bæta við upplýsingar um talningu og samlagningu</span><span class="sxs-lookup"><span data-stu-id="b1a9e-108">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="b1a9e-109">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="b1a9e-110">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="b1a9e-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="b1a9e-111">Í trénu skal víkka út 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="b1a9e-112">Í trénu skal velja 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-112">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="b1a9e-113">Gefum okkur að sérsníða þurfi sniðið sem Microsoft útvegar með því að bæta línum með samantektarupplýsingum við lok intrastat-skýrslu.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-113">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="b1a9e-114">Þú gerir það með því að sækja okkar eigin tilvik af intrastat-skilgreiningu úr Microsoft-tilvikinu til að gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-114">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="b1a9e-115">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="b1a9e-116">Í svæðinu Nýtt, veljið 'Leiða af nafni: Intrastat (DE), Microsoft'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-116">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="b1a9e-117">Í svæðið Heiti, sláðu inn „Intrastat (DE) með talningu & samlagningu“.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-117">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="b1a9e-118">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-118">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="b1a9e-119">Skilgreina þessa skýrslu til að gera talningu og samlagningu á grundvelli upplýsinga um úttak.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-119">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="b1a9e-120">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-120">Click Designer.</span></span>
2. <span data-ttu-id="b1a9e-121">Veldu Já í reitnum safna saman upplýsingum um framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-121">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="b1a9e-122">Þetta flagg virkjar ferlið við að safna saman úttaksupplýsingum til að mynda intrastat-skrána á keyrslutima.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-122">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="b1a9e-123">Þú þarft að telja fyrir mismunandi intrastat-stefnur, svo bæta skal sérstakri tölusetningu fyrir líkan við lista gagnaveitu fyrir þessa skilgreiningu sniðs.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-123">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources’ list of this format configuration.</span></span>  
3. <span data-ttu-id="b1a9e-124">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-124">Click the Mapping tab.</span></span>
4. <span data-ttu-id="b1a9e-125">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-125">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="b1a9e-126">Í trénu skal velja 'Data model\Enumeration '.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-126">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="b1a9e-127">Í reitnum Heiti skal færa inn ‚Stefna'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-127">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="b1a9e-128">Sláið inn eða veldu gildi í reitnum tölusetning líkans.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-128">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="b1a9e-129">Veldu gildið Stefna.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-129">Select the value Direction.</span></span>  
8. <span data-ttu-id="b1a9e-130">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-130">Click OK.</span></span>
9. <span data-ttu-id="b1a9e-131">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-131">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="b1a9e-132">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-132">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="b1a9e-133">Í svæðið Heiti, færðu inn '$BlockName'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-133">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="b1a9e-134">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-134">Click Edit formula.</span></span>
13. <span data-ttu-id="b1a9e-135">Í reitinn Formúla skal færa inn '"block"'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-135">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="b1a9e-136">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-136">Click Save.</span></span>
15. <span data-ttu-id="b1a9e-137">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-137">Close the page.</span></span>
16. <span data-ttu-id="b1a9e-138">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-138">Click OK.</span></span>
17. <span data-ttu-id="b1a9e-139">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-139">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="b1a9e-140">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-140">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="b1a9e-141">Í svæðið Heiti, færðu inn '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-141">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="b1a9e-142">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-142">Click Edit formula.</span></span>
21. <span data-ttu-id="b1a9e-143">Í reitinn Formúla skal færa inn '"record"'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-143">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="b1a9e-144">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-144">Click Save.</span></span>
23. <span data-ttu-id="b1a9e-145">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-145">Close the page.</span></span>
24. <span data-ttu-id="b1a9e-146">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-146">Click OK.</span></span>
25. <span data-ttu-id="b1a9e-147">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-147">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="b1a9e-148">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-148">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="b1a9e-149">Í svæðið Heiti, færðu inn '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-149">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="b1a9e-150">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-150">Click Edit formula.</span></span>
29. <span data-ttu-id="b1a9e-151">Í reitinn Formúla skal færa inn '"InvoicedAmountEUR"'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-151">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="b1a9e-152">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-152">Click Save.</span></span>
31. <span data-ttu-id="b1a9e-153">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-153">Close the page.</span></span>
32. <span data-ttu-id="b1a9e-154">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-154">Click OK.</span></span>
33. <span data-ttu-id="b1a9e-155">Í trénu skal velja 'Intrastat\Data'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-155">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="b1a9e-156">Smeltu á hnappinn breyta fyrir reitinn ‘heiti lykils fyrir söfnuð gögn’.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-156">Click Edit button for the ‘Collected data key name’ field</span></span>
35. <span data-ttu-id="b1a9e-157">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-157">Click Add data source.</span></span>
    * <span data-ttu-id="b1a9e-158">$BlockName</span><span class="sxs-lookup"><span data-stu-id="b1a9e-158">$BlockName</span></span>  
36. <span data-ttu-id="b1a9e-159">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-159">Click Save.</span></span>
37. <span data-ttu-id="b1a9e-160">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-160">Close the page.</span></span>
38. <span data-ttu-id="b1a9e-161">Smellið á hnappinn Breyta fyrir reitinn gildi lykils uppsafnaðra gagna</span><span class="sxs-lookup"><span data-stu-id="b1a9e-161">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="b1a9e-162">Í reitinn Formúlu skal færa inn 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-162">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="b1a9e-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, “Import”, “Export”)</span><span class="sxs-lookup"><span data-stu-id="b1a9e-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="b1a9e-164">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-164">Click Save.</span></span>
41. <span data-ttu-id="b1a9e-165">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-165">Close the page.</span></span>
    * <span data-ttu-id="b1a9e-166">Telja línur í þessari röð.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-166">Count the lines of this sequence.</span></span> <span data-ttu-id="b1a9e-167">Niðurstöður verður notað með heitinu "útiloka" aðskilið fyrir mismunandi stefnur.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-167">The results will be used with the name “block” separately for different directions.</span></span> <span data-ttu-id="b1a9e-168">Gildið “Innflutningur” verður notað fyrir allar intrastat-færslur fyrir komur.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-168">Value “Import” will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="b1a9e-169">Gildið “Útflutningur” verður notað fyrir allar intrastat-færslur fyrir sendingar.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-169">The value “Export” will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="b1a9e-170">Líttu á þetta sem sýndar Excel-töflu.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-170">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="b1a9e-171">Fyrir hverja færslu er lína þar sem fyrsta “blokk” dálkinn er fyllt út með gildunum “Innflutningur” og “Útflutning” til samræmis.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-171">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span>  
42. <span data-ttu-id="b1a9e-172">Í trénu skal víkka út 'Intrastat\Data: Sequence'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-172">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="b1a9e-173">Í trénu skal velja 'Intrastat\Data: Sequence\Arrivals?'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-173">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="b1a9e-174">Smeltu á hnappinn breyta fyrir reitinn ‘heiti lykils fyrir söfnuð gögn’.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-174">Click Edit button for the ‘Collected data key name’ field.</span></span>
    * <span data-ttu-id="b1a9e-175">Telja línur í þessari röð.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-175">Count the lines of this sequence.</span></span> <span data-ttu-id="b1a9e-176">Niðurstöðurnar eru geymdar í minni með því að nota skrána “færsla”.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-176">The results will be memorized using the name “record”.</span></span>  
45. <span data-ttu-id="b1a9e-177">Í trénu skal velja '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-177">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="b1a9e-178">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-178">Click Add data source.</span></span>
47. <span data-ttu-id="b1a9e-179">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-179">Click Save.</span></span>
48. <span data-ttu-id="b1a9e-180">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-180">Close the page.</span></span>
49. <span data-ttu-id="b1a9e-181">Smeltu á hnappinn breyta fyrir reitinn "gildi lykils fyrir söfnuð gögn".</span><span class="sxs-lookup"><span data-stu-id="b1a9e-181">Click Edit button for the ‘Collected data key value’ field</span></span>
50. <span data-ttu-id="b1a9e-182">Í Formúlu svæðinu, færið inn 'Intrastat.CommodityRecord.CommodityCode'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-182">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="b1a9e-183">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-183">Click Save.</span></span>
52. <span data-ttu-id="b1a9e-184">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-184">Close the page.</span></span>
    * <span data-ttu-id="b1a9e-185">Telja línur í þessari röð.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-185">Count the lines of this sequence.</span></span> <span data-ttu-id="b1a9e-186">Niðurstöður verður notað með heitinu “færsla” aðskilið fyrir mismunandi vörukóða.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-186">The results will be used with the name “record” separately for different commodity codes.</span></span> <span data-ttu-id="b1a9e-187">Líttu á þetta sem sýndar Excel-töflu.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-187">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="b1a9e-188">Fyrir hverja færslu er lína þar sem fyrsta “blokk” dálkinn er fyllt út með gildunum "Innflutningur" og “Útflutning” til samræmis og næsta blokkin “færsla” er fyllt með gildi vörukóða.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-188">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly and the second block “record” is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="b1a9e-189">Í trénu skal velja 'Intrastat\Data: Sequence\Dispatches?'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-189">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="b1a9e-190">Smeltu á hnappinn breyta fyrir reitinn ‘heiti lykils fyrir söfnuð gögn’.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-190">Click Edit button for the ‘Collected data key name’ field</span></span>
55. <span data-ttu-id="b1a9e-191">Í trénu skal velja '$RecName'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-191">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="b1a9e-192">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-192">Click Add data source.</span></span>
57. <span data-ttu-id="b1a9e-193">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-193">Click Save.</span></span>
58. <span data-ttu-id="b1a9e-194">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-194">Close the page.</span></span>
59. <span data-ttu-id="b1a9e-195">Smeltu á hnappinn breyta fyrir reitinn "gildi lykils fyrir söfnuð gögn".</span><span class="sxs-lookup"><span data-stu-id="b1a9e-195">Click the Edit button for the ‘Collected data key value’ field.</span></span>
60. <span data-ttu-id="b1a9e-196">Í Formúlu svæðinu, færið inn 'Intrastat.CommodityRecord.CommodityCode'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-196">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="b1a9e-197">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-197">Click Save.</span></span>
62. <span data-ttu-id="b1a9e-198">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-198">Close the page.</span></span>
63. <span data-ttu-id="b1a9e-199">Í trénu skal víkka út 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-199">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="b1a9e-200">Í trénu skal víkka út 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record = Intrastat.CommodityRecord'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="b1a9e-201">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-201">Click the Format tab.</span></span>
66. <span data-ttu-id="b1a9e-202">Í trénu skal velja 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-202">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="b1a9e-203">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-203">Click the Mapping tab.</span></span>
68. <span data-ttu-id="b1a9e-204">Smeltu á hnappinn breyta fyrir reitinn ‘heiti lykils fyrir söfnuð gögn’.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-204">Click the Edit button for the ‘Collected data key name’ field.</span></span>
69. <span data-ttu-id="b1a9e-205">Í trénu skal velja '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-205">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="b1a9e-206">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-206">Click Add data source.</span></span>
71. <span data-ttu-id="b1a9e-207">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-207">Click Save.</span></span>
72. <span data-ttu-id="b1a9e-208">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-208">Close the page.</span></span>
    * <span data-ttu-id="b1a9e-209">Taka saman gildi reikningsfærð upphæð fyrir línur í þessari röð.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-209">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="b1a9e-210">Niðurstöður verður notað með heitinu “InvoicedAmountEUR” aðskilið fyrir mismunandi intrastat-stefnur og vörukóða.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-210">The results will be used with the name “InvoicedAmountEUR” separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="b1a9e-211">Líttu á þetta sem sýndarsköpun í Excel-töflu.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-211">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="b1a9e-212">Fyrir hverja færslu er lína þar sem fyrsta “blokk” dálkinn er fyllt út með gildunum “Innflutningur” og “Útflutning” til samræmis.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-212">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span> <span data-ttu-id="b1a9e-213">Önnur blokk "færsla" er fyllt út með gildi vörukóða og þriðja dálkinn "InvoicedAmountEUR" er fyllt út með gildi upphæðar reiknings.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-213">The second block “record” is filled with the commodity code value, and the third column “InvoicedAmountEUR” is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="b1a9e-214">Í trénu skal víkka út 'Intrastat\Data\Arrivals?'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-214">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="b1a9e-215">Í trénu skal víkka út 'Intrastat\Data\Arrivals?\Record = Intrastat.CommodityRecord'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-215">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="b1a9e-216">Smellið á flipann snið.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-216">Click the Format tab.</span></span>
76. <span data-ttu-id="b1a9e-217">Í trénu skal velja 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-217">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="b1a9e-218">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-218">Click the Mapping tab.</span></span>
78. <span data-ttu-id="b1a9e-219">Smeltu á hnappinn breyta fyrir reitinn ‘heiti lykils fyrir söfnuð gögn’.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-219">Click the Edit button for the ‘Collected data key name’ field.</span></span>
79. <span data-ttu-id="b1a9e-220">Í trénu skal velja '$InvName'.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-220">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="b1a9e-221">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-221">Click Add data source.</span></span>
81. <span data-ttu-id="b1a9e-222">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-222">Click Save.</span></span>
82. <span data-ttu-id="b1a9e-223">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-223">Close the page.</span></span>
83. <span data-ttu-id="b1a9e-224">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-224">Click Save.</span></span>
84. <span data-ttu-id="b1a9e-225">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1a9e-225">Close the page.</span></span>


