--- 
title: "Nota grunnstillingar líkanavörpunar fyrir samanlagða útreikninga á gagnagrunnsstigi (rafrænnar skýrslugerðar)"
description: "Þessi aðferð gefur upplýsingar um hvernig á að hanna nýja stillingu fyrir vörpun rafrænnar skýrslugerðar og nota innbyggðar aðgerðir rafrænnar skýrslugerðar fyrir skilvirka samanlagða útreikninga."
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 74606b1378e94e8a6945a408520c8b68648970d8
ms.openlocfilehash: 3c3558d9e25dcfd56f3306e69884528d01324cbd
ms.contentlocale: is-is
ms.lasthandoff: 02/07/2018

---
# <a name="use-a-model-mapping-configuration-for-aggregate-calculations-at-the-database-leveler"></a><span data-ttu-id="d0ca3-103">Nota grunnstillingar líkanavörpunar fyrir samanlagða útreikninga á gagnagrunnsstigi (rafrænnar skýrslugerðar)</span><span class="sxs-lookup"><span data-stu-id="d0ca3-103">Use a model mapping configuration for aggregate calculations at the database level(ER)</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d0ca3-104">Þessi aðferð gefur upplýsingar um hvernig á að hanna nýja stillingu fyrir vörpun rafrænnar skýrslugerðar og nota innbyggðar aðgerðir rafrænnar skýrslugerðar fyrir skilvirka samanlagða útreikninga.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-104">This procedure provides information about how to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="d0ca3-105">Í þessu dæmi muntu stofna skilgreiningu fyrir sýnifyrirtækið, Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-105">In this procedure you will create a configuration for the sample company, Litware, Inc.</span></span> 

<span data-ttu-id="d0ca3-106">Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-106">This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> <span data-ttu-id="d0ca3-107">Skrefin er hægt að klára með því að nota hvaða gagnasafn sem er.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-107">These steps can be completed using any dataset.</span></span>

 <span data-ttu-id="d0ca3-108">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð bætir virkni samanlagðra útreikninga með því að framkvæma hann á gagnagrunnsstigi (hluti 1, Undirbúningur skilgreininga).“</span><span class="sxs-lookup"><span data-stu-id="d0ca3-108">To complete these steps, you must first complete the steps in the procedure, “ER improves the efficiency of aggregate calculations by performing them on database level (Part 1: Prepare configurations).”</span></span>

1. <span data-ttu-id="d0ca3-109">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="d0ca3-110">Í trénu skal víkka út 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-110">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="d0ca3-111">Í trénu skal velja „Intrastat-model\Intrastat-sýnivörpun“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-111">In the tree, select 'Intrastat model\Intrastat sample mapping'.</span></span>
4. <span data-ttu-id="d0ca3-112">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-112">Click Designer.</span></span>
5. <span data-ttu-id="d0ca3-113">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-113">Click Designer.</span></span>
6. <span data-ttu-id="d0ca3-114">Í trénu skal velja „Dynamics 365 for Operations\Tafla færslur“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-114">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
7. <span data-ttu-id="d0ca3-115">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-115">Click Add root.</span></span>
    * <span data-ttu-id="d0ca3-116">Bæta nýjum gagnagjafa við sem stendur fyrir færslur sem þú vilt flokka.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-116">Add a new data source representing records you want to group.</span></span>  
8. <span data-ttu-id="d0ca3-117">Í reitnum Heiti skal færa inn ‚færslur'.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-117">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="d0ca3-118">Færslur</span><span class="sxs-lookup"><span data-stu-id="d0ca3-118">Transactions</span></span>  
9. <span data-ttu-id="d0ca3-119">Í reitnum Tafla skal færa inn „Intrastat“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-119">In the Table field, type 'Intrastat'.</span></span>
    * <span data-ttu-id="d0ca3-120">Intrastat</span><span class="sxs-lookup"><span data-stu-id="d0ca3-120">Intrastat</span></span>  
10. <span data-ttu-id="d0ca3-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-121">Click OK.</span></span>
11. <span data-ttu-id="d0ca3-122">Í trénu skal velja „virkni\Flokka eftir“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-122">In the tree, select 'Functions\Group by'.</span></span>
    * <span data-ttu-id="d0ca3-123">Þessi gerð gagnagjafa er notuð til að kynna nýjan gagnagjafa á keyrslutíma til að flokka færslur og reikna út áskilda uppsöfnun.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-123">This data source type is used to introduce a new data source at run-time to group records and to calculate required aggregations.</span></span>  
12. <span data-ttu-id="d0ca3-124">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-124">Click Add root.</span></span>
13. <span data-ttu-id="d0ca3-125">Í reitnum Heiti skal færa inn „TransactionsGroups“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-125">In the Name field, type 'TransactionsGroups'.</span></span>
    * <span data-ttu-id="d0ca3-126">TransactionsGroups</span><span class="sxs-lookup"><span data-stu-id="d0ca3-126">TransactionsGroups</span></span>  
14. <span data-ttu-id="d0ca3-127">Smella á Breyta hópi eftir</span><span class="sxs-lookup"><span data-stu-id="d0ca3-127">Click Edit group by.</span></span>
15. <span data-ttu-id="d0ca3-128">Í trénu skal velja „Færslur“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-128">In the tree, select 'Transactions'.</span></span>
    * <span data-ttu-id="d0ca3-129">Veljið viðbættan gagnagjafa af gerðinni „færslulisti“ sem stendur fyrir færslur sem þú vilt flokka.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-129">Select the added data source of the ‘Record list’ type that represents the records that you want to group.</span></span>  
16. <span data-ttu-id="d0ca3-130">Smellt er á Bæta reit við</span><span class="sxs-lookup"><span data-stu-id="d0ca3-130">Click Add field to.</span></span>
17. <span data-ttu-id="d0ca3-131">Veldu hvað skal flokka</span><span class="sxs-lookup"><span data-stu-id="d0ca3-131">Click What to group.</span></span>
18. <span data-ttu-id="d0ca3-132">Í trénu skal víkka út „Færslur“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-132">In the tree, expand 'Transactions'.</span></span>
19. <span data-ttu-id="d0ca3-133">Í trénu skal velja „Færslur\Stefna“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-133">In the tree, select 'Transactions\Direction'.</span></span>
20. <span data-ttu-id="d0ca3-134">Smellt er á Bæta reit við</span><span class="sxs-lookup"><span data-stu-id="d0ca3-134">Click Add field to.</span></span>
21. <span data-ttu-id="d0ca3-135">Smellt er á Flokkaðir reitir</span><span class="sxs-lookup"><span data-stu-id="d0ca3-135">Click Grouped fields.</span></span>
    * <span data-ttu-id="d0ca3-136">Veljið reitinn sem á að tilgreina flokkunarstig.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-136">Select the field to specify the grouping level.</span></span> <span data-ttu-id="d0ca3-137">Byggt á þessu vali munu gögnin koma aftur á keyrslutíma sem margir færsluflokkar þar sem stefnukóðum verður mætt í Intrastat töflunni.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-137">Based on this selection, the data source will return at run-time as many groups of transactions as there are direction codes that will be met in the Intrastat table.</span></span>  
22. <span data-ttu-id="d0ca3-138">Í trénu skal velja „Færslur\Reikningsupphæð(AmountMST)“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-138">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
    * <span data-ttu-id="d0ca3-139">Veljið svæðið til að skilgreina gögn fyrir útreikning á uppsöfnun.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-139">Select the field to specify the source for aggregation calculation.</span></span>  
23. <span data-ttu-id="d0ca3-140">Smellt er á Bæta reit við</span><span class="sxs-lookup"><span data-stu-id="d0ca3-140">Click Add field to.</span></span>
24. <span data-ttu-id="d0ca3-141">Smellt er á Uppsöfnunarreitir</span><span class="sxs-lookup"><span data-stu-id="d0ca3-141">Click Aggregation fields.</span></span>
25. <span data-ttu-id="d0ca3-142">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-142">In the list, mark the selected row.</span></span>
26. <span data-ttu-id="d0ca3-143">Veljið „Samtala“ á svæðinu Aðferð.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-143">In the Method field, select 'Sum'.</span></span>
    * <span data-ttu-id="d0ca3-144">Veljið uppsöfnunargerð.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-144">Select the aggregation type.</span></span>  
27. <span data-ttu-id="d0ca3-145">Í svæðið Heiti skal slá inn „SumOfAmountMST“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-145">In the Name field, type 'SumOfAmountMST'.</span></span>
    * <span data-ttu-id="d0ca3-146">Tilgreinið heiti þessarar uppsöfnunar í stilltum gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-146">Specify the name of this aggregation in the configured data source.</span></span>  
28. <span data-ttu-id="d0ca3-147">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-147">Click Save.</span></span>
    * <span data-ttu-id="d0ca3-148">Athugið að reiturinn „Framkvæmd við“ gefur til kynna að þessi flokkun verði framkvæmd á keyrslutíma í SQL gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-148">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in the SQL database.</span></span>  
29. <span data-ttu-id="d0ca3-149">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-149">Close the page.</span></span>
30. <span data-ttu-id="d0ca3-150">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-150">Click OK.</span></span>
31. <span data-ttu-id="d0ca3-151">Í trénu skal víkka út „Samtölur“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-151">In the tree, expand 'Totals'.</span></span>
32. <span data-ttu-id="d0ca3-152">Í trénu skal víkka út „TransactionsGroups“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-152">In the tree, expand 'TransactionsGroups'.</span></span>
33. <span data-ttu-id="d0ca3-153">Í trénu skal víkka út „Færsluflokkar\samanlagðir“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-153">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
34. <span data-ttu-id="d0ca3-154">Í trénu skal velja „Færsluflokkar\samanlagðir\SumOfAmountMST“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-154">In the tree, select 'TransactionsGroups\aggregated\SumOfAmountMST'.</span></span>
35. <span data-ttu-id="d0ca3-155">Í trénu skal velja „Samtölur\Samtala reikningsgildis(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0,0, IntrastatTotals.aggregated.'$AmountMSTRounded‘)“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-155">In the tree, select 'Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.</span></span>
36. <span data-ttu-id="d0ca3-156">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-156">Click Bind.</span></span>
    * <span data-ttu-id="d0ca3-157">Byggt á þessari stillingu, mun þessi gagnagjafi reikna summuna af gildum „AmountMST“ reitsins fyrir hvern færsluflokk.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-157">Based on this setting, this data source will calculate the sum of values of the ‘AmountMST’ field for each groups of transactions.</span></span> <span data-ttu-id="d0ca3-158">Þessi samanlegðarútreikningur verður tiltækur sem TransactionsGroups.aggregated.TotalAmount-atriði.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-158">This aggregation calculation will be available as TransactionsGroups.aggregated.TotalAmount item.</span></span>  
37. <span data-ttu-id="d0ca3-159">Í trénu skal víkka út „TransactionsGroups“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-159">In the tree, expand 'TransactionsGroups'.</span></span>
38. <span data-ttu-id="d0ca3-160">Í trénu skal velja „TransactionsGroups“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-160">In the tree, select 'TransactionsGroups'.</span></span>
39. <span data-ttu-id="d0ca3-161">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-161">Click Edit.</span></span>
40. <span data-ttu-id="d0ca3-162">Smella á Breyta hópi eftir</span><span class="sxs-lookup"><span data-stu-id="d0ca3-162">Click Edit group by.</span></span>
41. <span data-ttu-id="d0ca3-163">Í trénu skal víkka út „Færslur“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-163">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="d0ca3-164">Í trénu skal velja „Færslur\Reikningsupphæð(AmountMST)“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-164">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
43. <span data-ttu-id="d0ca3-165">Smellt er á Bæta reit við</span><span class="sxs-lookup"><span data-stu-id="d0ca3-165">Click Add field to.</span></span>
44. <span data-ttu-id="d0ca3-166">Smellt er á Uppsöfnunarreitir</span><span class="sxs-lookup"><span data-stu-id="d0ca3-166">Click Aggregation fields.</span></span>
45. <span data-ttu-id="d0ca3-167">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-167">In the list, mark the selected row.</span></span>
46. <span data-ttu-id="d0ca3-168">Veljið „Hámark“ á svæðinu Aðferð.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-168">In the Method field, select 'Max'.</span></span>
47. <span data-ttu-id="d0ca3-169">Í svæðið Heiti skal slá inn „MaxOfAmountMST“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-169">In the Name field, type 'MaxOfAmountMST'.</span></span>
48. <span data-ttu-id="d0ca3-170">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-170">Click Save.</span></span>
    * <span data-ttu-id="d0ca3-171">Eins og er getur framkvæmd GROUPBY gagnagjafa verið þýdd í SQL gagnagrunnsstig með nokkrum takmörkunum.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-171">Currently, the execution of GROUPBY data sources can be translated to the SQL database level with some limitations.</span></span> <span data-ttu-id="d0ca3-172">Þýðingu er hægt að gera fyrir annaðhvort gagnagjafa af gerðinni „Færslulisti“ eða gagnagjafa sem settir eru fram sem tjáning með FILTER aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-172">Translation can be done for either data sources of the ‘Record list’ type or data sources represented as an expression using the FILTER function.</span></span> <span data-ttu-id="d0ca3-173">Það er einnig hægt að gera þegar aðeins ein uppsöfnun er stillt fyrir stakan reit flokkunarfærslna.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-173">It can also be done when the only one aggregation is configured for a single field of the grouping records.</span></span>  
    * <span data-ttu-id="d0ca3-174">Athugaðu að jafnvel þó að fleiri en ein uppsöfnun hafi verið stillt fyrir AmountMST-reitinn, gefur reiturinn „Framkvæmd við“ reiturinn enn frekar til kynna að þessi flokkun verði framkvæmd á keyrslutíma í SQL-gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-174">Note that even though more than one aggregation was configured for the AmountMST field, the ‘Execution at’ field still indicates that this grouping will be performed at run-time in the SQL database.</span></span> <span data-ttu-id="d0ca3-175">Þetta er vegna þess að aðeins ein uppsöfnun er bundin við gagnalíkanahlutann og verður notuð á keyrslutíma til að draga gögn úr þessum gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-175">This is because only one aggregation is bound to the data model item and will be used at run-time to pull data from this data source.</span></span>  
49. <span data-ttu-id="d0ca3-176">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-176">Close the page.</span></span>
50. <span data-ttu-id="d0ca3-177">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-177">Click OK.</span></span>
51. <span data-ttu-id="d0ca3-178">Í trénu skal víkka út „TransactionsGroups“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-178">In the tree, expand 'TransactionsGroups'.</span></span>
52. <span data-ttu-id="d0ca3-179">Í trénu skal víkka út „Færsluflokkar\samanlagðir“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-179">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
53. <span data-ttu-id="d0ca3-180">Í trénu skal velja „Færsluflokkar\samanlagðir\MaxOfAmountMST“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-180">In the tree, select 'TransactionsGroups\aggregated\MaxOfAmountMST'.</span></span>
54. <span data-ttu-id="d0ca3-181">Í trénu skal velja „Samtölur\Samtölur tölfræðigilda(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0,0, IntrastatTotals.aggregated.'$StatisticalValueRounded‘)“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-181">In the tree, select 'Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span></span>
55. <span data-ttu-id="d0ca3-182">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-182">Click Bind.</span></span>
56. <span data-ttu-id="d0ca3-183">Í trénu skal víkka út „TransactionsGroups“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-183">In the tree, expand 'TransactionsGroups'.</span></span>
57. <span data-ttu-id="d0ca3-184">Í trénu skal velja „TransactionsGroups“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-184">In the tree, select 'TransactionsGroups'.</span></span>
58. <span data-ttu-id="d0ca3-185">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-185">Click Edit.</span></span>
59. <span data-ttu-id="d0ca3-186">Smella á Breyta hópi eftir</span><span class="sxs-lookup"><span data-stu-id="d0ca3-186">Click Edit group by.</span></span>
    * <span data-ttu-id="d0ca3-187">Athugaðu að reiturinn „Framkvæmd við“ gefur til kynna að þessi flokkun verði framkvæmd á keyrslutíma í minni vegna þess að báðar uppsafnanir sama svæðis eru bundnar við gagnalíkanahlutana.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-187">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory because both aggregations of the same field are bound to the data model items.</span></span>   
60. <span data-ttu-id="d0ca3-188">Merkið eða afmerkið allar línur í listanum.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-188">In the list, mark or unmark all rows.</span></span>
61. <span data-ttu-id="d0ca3-189">Smellið á Eyða.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-189">Click Delete.</span></span>
62. <span data-ttu-id="d0ca3-190">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-190">Click Yes.</span></span>
63. <span data-ttu-id="d0ca3-191">Smellið á Eyða.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-191">Click Delete.</span></span>
64. <span data-ttu-id="d0ca3-192">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-192">Click Yes.</span></span>
65. <span data-ttu-id="d0ca3-193">Smellt er á Bæta reit við</span><span class="sxs-lookup"><span data-stu-id="d0ca3-193">Click Add field to.</span></span>
66. <span data-ttu-id="d0ca3-194">Veldu hvað skal flokka</span><span class="sxs-lookup"><span data-stu-id="d0ca3-194">Click What to group.</span></span>
67. <span data-ttu-id="d0ca3-195">Í trénu skal víkka út „Grunnvörufærsla(Intrastat)“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-195">In the tree, expand 'Commodity record(Intrastat)'.</span></span>
68. <span data-ttu-id="d0ca3-196">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-196">Click Save.</span></span>
    * <span data-ttu-id="d0ca3-197">Athugaðu að reiturinn „Framkvæmd við“ gefur til kynna að þessi flokkun verði framkvæmd á keyrslutíma í minni þrátt fyrir að engar uppsafnanir séu skilgreindar og valdir gagnagjafar af gerðinni „Töflufærslur“ vísa í sömu „Intrastat“-töflu.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-197">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory even though there are no aggregations defined and the selected data source of ‘Table records’ type refers to the same ‘Intrastat’ table.</span></span> <span data-ttu-id="d0ca3-198">Þetta er vegna þess að gagnagjafinn inniheldur nokkra útreiknaða reiti sem ekki er hægt að þýða yfir í SQL gagnagrunnsstig.</span><span class="sxs-lookup"><span data-stu-id="d0ca3-198">This is because the data source contains some calculated fields which can’t yet be translated to the SQL database level.</span></span>  


