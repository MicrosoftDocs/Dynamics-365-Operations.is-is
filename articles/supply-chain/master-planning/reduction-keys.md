---
title: Minnkunarlyklar
description: Þessi grein gefur dæmi um hvernig eigi að setja upp minnkunarlykil. Hún felur í sér upplýsingar um mismunandi stillingar minnkunarlykla og niðurstöður hverrar fyrir sig. Hægt er að nota minnkunarlykil til að skilgreina hvernig á að lækka spárþarfir.
author: roxanadiaconu
manager: AnnBe
ms.date: 02/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7457aca4ca4d5188bafb497d3052276cfc154ad1
ms.sourcegitcommit: 704d273485dcdc25c97a222bc0ef0695aad334d2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/28/2019
ms.locfileid: "770917"
---
# <a name="reduction-keys"></a><span data-ttu-id="0bc35-105">Minnkunarlyklar</span><span class="sxs-lookup"><span data-stu-id="0bc35-105">Reduction keys</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0bc35-106">Þessi grein gefur dæmi um hvernig eigi að setja upp minnkunarlykil.</span><span class="sxs-lookup"><span data-stu-id="0bc35-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="0bc35-107">Hún felur í sér upplýsingar um mismunandi stillingar minnkunarlykla og niðurstöður hverrar fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="0bc35-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="0bc35-108">Hægt er að nota minnkunarlykil til að skilgreina hvernig á að lækka spárþarfir.</span><span class="sxs-lookup"><span data-stu-id="0bc35-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="0bc35-109">Dæmi 1: Prósenta - minnkunarlykill spá lækkunarregla</span><span class="sxs-lookup"><span data-stu-id="0bc35-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="0bc35-110">Þetta dæmi sýnir hvernig minnkunarlykill minnkar kröfur eftirspurnarspá í samræmi við prósentur og tímabil sem eru skilgreind af minnkunarlykli.</span><span class="sxs-lookup"><span data-stu-id="0bc35-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1. <span data-ttu-id="0bc35-111">Á **Minnkunarlyklar** síðunni, setjið upp eftirfarandi línur.</span><span class="sxs-lookup"><span data-stu-id="0bc35-111">On the **Reduction keys** page, set up the following lines.</span></span>

   | <span data-ttu-id="0bc35-112">Skiptimynt</span><span class="sxs-lookup"><span data-stu-id="0bc35-112">Change</span></span> | <span data-ttu-id="0bc35-113">Eining</span><span class="sxs-lookup"><span data-stu-id="0bc35-113">Unit</span></span>  | <span data-ttu-id="0bc35-114">Prósent</span><span class="sxs-lookup"><span data-stu-id="0bc35-114">Percent</span></span> |
   |--------|-------|---------|
   |   <span data-ttu-id="0bc35-115">1</span><span class="sxs-lookup"><span data-stu-id="0bc35-115">1</span></span>    | <span data-ttu-id="0bc35-116">Mánuður</span><span class="sxs-lookup"><span data-stu-id="0bc35-116">Month</span></span> |   <span data-ttu-id="0bc35-117">100</span><span class="sxs-lookup"><span data-stu-id="0bc35-117">100</span></span>   |
   |   <span data-ttu-id="0bc35-118">2</span><span class="sxs-lookup"><span data-stu-id="0bc35-118">2</span></span>    | <span data-ttu-id="0bc35-119">Mánuður</span><span class="sxs-lookup"><span data-stu-id="0bc35-119">Month</span></span> |   <span data-ttu-id="0bc35-120">75</span><span class="sxs-lookup"><span data-stu-id="0bc35-120">75</span></span>    |
   |   <span data-ttu-id="0bc35-121">3</span><span class="sxs-lookup"><span data-stu-id="0bc35-121">3</span></span>    | <span data-ttu-id="0bc35-122">Mánuður</span><span class="sxs-lookup"><span data-stu-id="0bc35-122">Month</span></span> |   <span data-ttu-id="0bc35-123">50</span><span class="sxs-lookup"><span data-stu-id="0bc35-123">50</span></span>    |
   |   <span data-ttu-id="0bc35-124">4</span><span class="sxs-lookup"><span data-stu-id="0bc35-124">4</span></span>    | <span data-ttu-id="0bc35-125">Mánuður</span><span class="sxs-lookup"><span data-stu-id="0bc35-125">Month</span></span> |   <span data-ttu-id="0bc35-126">25</span><span class="sxs-lookup"><span data-stu-id="0bc35-126">25</span></span>    |


2. <span data-ttu-id="0bc35-127">Tengja þarf minnkunarlykilinn við þekjuflokk vöru.</span><span class="sxs-lookup"><span data-stu-id="0bc35-127">Link the reduction key to the item's coverage group.</span></span>
3. <span data-ttu-id="0bc35-128">Á **Aðaláætlanir** síðunni,°í **Lækkunarreglu** svæðinu, veljið **Prósenta - minnkunarlykill**.</span><span class="sxs-lookup"><span data-stu-id="0bc35-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4. <span data-ttu-id="0bc35-129">Stofnið söluspá fyrir 1.000 stykki á mánuði.</span><span class="sxs-lookup"><span data-stu-id="0bc35-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="0bc35-130">Ef spárröðun er keyrð 1. Janúar, eru spáþarfir eftirspurnar nýttar samkvæmt prósentum sem settar eru upp á **Minnkunarlyklar** síðu.</span><span class="sxs-lookup"><span data-stu-id="0bc35-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="0bc35-131">Eftirfarandi þarfamagn er fært í aðaláætlun.</span><span class="sxs-lookup"><span data-stu-id="0bc35-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="0bc35-132">Mánuður</span><span class="sxs-lookup"><span data-stu-id="0bc35-132">Month</span></span>                | <span data-ttu-id="0bc35-133">Fjöldi eintaka sem óskað er eftir</span><span class="sxs-lookup"><span data-stu-id="0bc35-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="0bc35-134">janúar</span><span class="sxs-lookup"><span data-stu-id="0bc35-134">January</span></span>              | <span data-ttu-id="0bc35-135">0</span><span class="sxs-lookup"><span data-stu-id="0bc35-135">0</span></span>                         |
| <span data-ttu-id="0bc35-136">febrúar</span><span class="sxs-lookup"><span data-stu-id="0bc35-136">February</span></span>             | <span data-ttu-id="0bc35-137">250</span><span class="sxs-lookup"><span data-stu-id="0bc35-137">250</span></span>                       |
| <span data-ttu-id="0bc35-138">mars</span><span class="sxs-lookup"><span data-stu-id="0bc35-138">March</span></span>                | <span data-ttu-id="0bc35-139">500</span><span class="sxs-lookup"><span data-stu-id="0bc35-139">500</span></span>                       |
| <span data-ttu-id="0bc35-140">Apríl</span><span class="sxs-lookup"><span data-stu-id="0bc35-140">April</span></span>                | <span data-ttu-id="0bc35-141">750</span><span class="sxs-lookup"><span data-stu-id="0bc35-141">750</span></span>                       |
| <span data-ttu-id="0bc35-142">Maí til og með desember</span><span class="sxs-lookup"><span data-stu-id="0bc35-142">May through December</span></span> | <span data-ttu-id="0bc35-143">1.000</span><span class="sxs-lookup"><span data-stu-id="0bc35-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="0bc35-144">Dæmi 2: Færslur  minnkunarlykill spá lækkunarreglu</span><span class="sxs-lookup"><span data-stu-id="0bc35-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="0bc35-145">Þetta dæmi sýnir hvernig raunverulegar pantanir sem eiga sér stað á tímabilum sem eru skilgreind af minnkunarlykli minnka kröfur eftirspurnarskrár.</span><span class="sxs-lookup"><span data-stu-id="0bc35-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="0bc35-146">Á **Aðaláætlanir** síðunni,°í **Lækkunarreglu** svæðinu, veljið **Færslur - minnkunarlykill**.</span><span class="sxs-lookup"><span data-stu-id="0bc35-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="0bc35-147">Eftirfarandi sölupantanir eru tiltækar 1. janúar.</span><span class="sxs-lookup"><span data-stu-id="0bc35-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="0bc35-148">Mánuður</span><span class="sxs-lookup"><span data-stu-id="0bc35-148">Month</span></span>    | <span data-ttu-id="0bc35-149">Fjöldi pantaðar stykkja</span><span class="sxs-lookup"><span data-stu-id="0bc35-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="0bc35-150">janúar</span><span class="sxs-lookup"><span data-stu-id="0bc35-150">January</span></span>  | <span data-ttu-id="0bc35-151">956</span><span class="sxs-lookup"><span data-stu-id="0bc35-151">956</span></span>                      |
| <span data-ttu-id="0bc35-152">febrúar</span><span class="sxs-lookup"><span data-stu-id="0bc35-152">February</span></span> | <span data-ttu-id="0bc35-153">1,176</span><span class="sxs-lookup"><span data-stu-id="0bc35-153">1,176</span></span>                    |
| <span data-ttu-id="0bc35-154">mars</span><span class="sxs-lookup"><span data-stu-id="0bc35-154">March</span></span>    | <span data-ttu-id="0bc35-155">451</span><span class="sxs-lookup"><span data-stu-id="0bc35-155">451</span></span>                      |
| <span data-ttu-id="0bc35-156">apríl</span><span class="sxs-lookup"><span data-stu-id="0bc35-156">April</span></span>    | <span data-ttu-id="0bc35-157">119</span><span class="sxs-lookup"><span data-stu-id="0bc35-157">119</span></span>                      |

<span data-ttu-id="0bc35-158">Ef sama söluspá fyrir 1.000 stykki á mánuði er notuð er eftirfarandi þarfamagn fært í aðaláætlun.</span><span class="sxs-lookup"><span data-stu-id="0bc35-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="0bc35-159">Mánuður</span><span class="sxs-lookup"><span data-stu-id="0bc35-159">Month</span></span>                | <span data-ttu-id="0bc35-160">Fjöldi eintaka sem óskað er eftir</span><span class="sxs-lookup"><span data-stu-id="0bc35-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="0bc35-161">janúar</span><span class="sxs-lookup"><span data-stu-id="0bc35-161">January</span></span>              | <span data-ttu-id="0bc35-162">44</span><span class="sxs-lookup"><span data-stu-id="0bc35-162">44</span></span>                        |
| <span data-ttu-id="0bc35-163">febrúar</span><span class="sxs-lookup"><span data-stu-id="0bc35-163">February</span></span>             | <span data-ttu-id="0bc35-164">0</span><span class="sxs-lookup"><span data-stu-id="0bc35-164">0</span></span>                         |
| <span data-ttu-id="0bc35-165">mars</span><span class="sxs-lookup"><span data-stu-id="0bc35-165">March</span></span>                | <span data-ttu-id="0bc35-166">549</span><span class="sxs-lookup"><span data-stu-id="0bc35-166">549</span></span>                       |
| <span data-ttu-id="0bc35-167">Apríl</span><span class="sxs-lookup"><span data-stu-id="0bc35-167">April</span></span>                | <span data-ttu-id="0bc35-168">881</span><span class="sxs-lookup"><span data-stu-id="0bc35-168">881</span></span>                       |
| <span data-ttu-id="0bc35-169">Maí til og með desember</span><span class="sxs-lookup"><span data-stu-id="0bc35-169">May through December</span></span> | <span data-ttu-id="0bc35-170">1.000</span><span class="sxs-lookup"><span data-stu-id="0bc35-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="0bc35-171">Dæmi 3: Færslur breytileg tímabil spá lækkunarreglu</span><span class="sxs-lookup"><span data-stu-id="0bc35-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="0bc35-172">Í flestum tilvikum eru kerfi sett upp þannig að færslur minnka eftirspurnarspár innan tiltekna spátímabila: vikur, mánuðir, og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="0bc35-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="0bc35-173">Þessi tímabil eru skilgreind í minnkunarlyklinum.</span><span class="sxs-lookup"><span data-stu-id="0bc35-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="0bc35-174">Hins vegar getur tíminn milli tveggja eftirspurnarspárlína einnig *gefið til kynna* tímabil.</span><span class="sxs-lookup"><span data-stu-id="0bc35-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1. <span data-ttu-id="0bc35-175">Stofna eftirspurnarspá fyrir eftirfarandi dagsetningar og magn.</span><span class="sxs-lookup"><span data-stu-id="0bc35-175">Create a demand forecast for the following dates and quantities.</span></span>

   | <span data-ttu-id="0bc35-176">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="0bc35-176">Date</span></span>       | <span data-ttu-id="0bc35-177">Eftirspurnarspá</span><span class="sxs-lookup"><span data-stu-id="0bc35-177">Demand forecast</span></span> |
   |------------|-----------------|
   | <span data-ttu-id="0bc35-178">1. janúar</span><span class="sxs-lookup"><span data-stu-id="0bc35-178">January 1</span></span>  | <span data-ttu-id="0bc35-179">1.000</span><span class="sxs-lookup"><span data-stu-id="0bc35-179">1,000</span></span>           |
   | <span data-ttu-id="0bc35-180">5. janúar</span><span class="sxs-lookup"><span data-stu-id="0bc35-180">January 5</span></span>  | <span data-ttu-id="0bc35-181">500</span><span class="sxs-lookup"><span data-stu-id="0bc35-181">500</span></span>             |
   | <span data-ttu-id="0bc35-182">12. janúar</span><span class="sxs-lookup"><span data-stu-id="0bc35-182">January 12</span></span> | <span data-ttu-id="0bc35-183">1.000</span><span class="sxs-lookup"><span data-stu-id="0bc35-183">1,000</span></span>           |

   <span data-ttu-id="0bc35-184">Í þessari spá það er ekki greinilegt tímabil milli spádagsetninganna: Milli fyrstu og annarrar dagsetningar er°fjögurra daga bil og milli annarrar og þriðju dagsetningar er°sjö daga bil.</span><span class="sxs-lookup"><span data-stu-id="0bc35-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="0bc35-185">Þessi mismunandi bil eru breytileg tímabil.</span><span class="sxs-lookup"><span data-stu-id="0bc35-185">These various spans are the dynamic periods.</span></span>
2. <span data-ttu-id="0bc35-186">Stofna Sölupöntunarlínur á eftirfarandi hátt.</span><span class="sxs-lookup"><span data-stu-id="0bc35-186">Create sales order lines as follows.</span></span>

   | <span data-ttu-id="0bc35-187">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="0bc35-187">Date</span></span>                             | <span data-ttu-id="0bc35-188">Sölupöntunarmagn</span><span class="sxs-lookup"><span data-stu-id="0bc35-188">Sales order quantity</span></span> |
   |----------------------------------|----------------------|
   | <span data-ttu-id="0bc35-189">15. Desember á fyrra ári</span><span class="sxs-lookup"><span data-stu-id="0bc35-189">December 15 in the previous year</span></span> | <span data-ttu-id="0bc35-190">500</span><span class="sxs-lookup"><span data-stu-id="0bc35-190">500</span></span>                  |
   | <span data-ttu-id="0bc35-191">3. janúar</span><span class="sxs-lookup"><span data-stu-id="0bc35-191">January 3</span></span>                        | <span data-ttu-id="0bc35-192">100</span><span class="sxs-lookup"><span data-stu-id="0bc35-192">100</span></span>                  |
   | <span data-ttu-id="0bc35-193">10. janúar</span><span class="sxs-lookup"><span data-stu-id="0bc35-193">January 10</span></span>                       | <span data-ttu-id="0bc35-194">200</span><span class="sxs-lookup"><span data-stu-id="0bc35-194">200</span></span>                  |

<span data-ttu-id="0bc35-195">Spáin verður lækkuð sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="0bc35-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="0bc35-196">Fyrsta sölupöntun er ekki innan neins tímabils svo það ekki að draga úr neinni spá.</span><span class="sxs-lookup"><span data-stu-id="0bc35-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="0bc35-197">Önnur sölupöntun er á milli 1. Janúar og 5. Janúar, þannig að hún lækkar spá fyrir 1. Janúar um 100.</span><span class="sxs-lookup"><span data-stu-id="0bc35-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="0bc35-198">Þriðja sölupöntun er á milli 5. Janúar og 12. Janúar, þannig að hún lækkar spá fyrir 5. Janúar um 200.</span><span class="sxs-lookup"><span data-stu-id="0bc35-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="0bc35-199">Eftirfarandi áætluð pöntun verður stofnuð til að uppfylla spána.</span><span class="sxs-lookup"><span data-stu-id="0bc35-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="0bc35-200">Dagsetning eftirspurnarspár</span><span class="sxs-lookup"><span data-stu-id="0bc35-200">Demand forecast date</span></span> | <span data-ttu-id="0bc35-201">Minnkað magn</span><span class="sxs-lookup"><span data-stu-id="0bc35-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="0bc35-202">1. janúar</span><span class="sxs-lookup"><span data-stu-id="0bc35-202">January 1</span></span>            | <span data-ttu-id="0bc35-203">900</span><span class="sxs-lookup"><span data-stu-id="0bc35-203">900</span></span>              |
| <span data-ttu-id="0bc35-204">5. janúar</span><span class="sxs-lookup"><span data-stu-id="0bc35-204">January 5</span></span>            | <span data-ttu-id="0bc35-205">300</span><span class="sxs-lookup"><span data-stu-id="0bc35-205">300</span></span>              |
| <span data-ttu-id="0bc35-206">12. janúar</span><span class="sxs-lookup"><span data-stu-id="0bc35-206">January 12</span></span>           | <span data-ttu-id="0bc35-207">1.000</span><span class="sxs-lookup"><span data-stu-id="0bc35-207">1,000</span></span>            |

<span data-ttu-id="0bc35-208">Hér er samantekt af°**Færslur - breytilegt tímabil** lækkun:</span><span class="sxs-lookup"><span data-stu-id="0bc35-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="0bc35-209">Spáþarfir eru minnkaðar við raunverulega pöntunarfærslur sem koma upp við breytilegt tímabil.</span><span class="sxs-lookup"><span data-stu-id="0bc35-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="0bc35-210">Breytilegt tímabil nær yfir núgildandi spá dagsetningar og lýkur við upphaf næstu spár.</span><span class="sxs-lookup"><span data-stu-id="0bc35-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="0bc35-211">Þessi aðferð notar hvorki né krefst minnkunarlykils.</span><span class="sxs-lookup"><span data-stu-id="0bc35-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="0bc35-212">Þegar þessi valkostur er notaður gerist eftirfarandi virkni:</span><span class="sxs-lookup"><span data-stu-id="0bc35-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="0bc35-213">Ef spá er alveg minnkuð verða spárþarfir gildandi spá 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="0bc35-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="0bc35-214">Ef það er engin komandi spá eru spáþarfir frá síðustu spá sem var færð inn minnkaðar.</span><span class="sxs-lookup"><span data-stu-id="0bc35-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="0bc35-215">Tímamörk eru hafðar með í útreikningi á lækkun spár.</span><span class="sxs-lookup"><span data-stu-id="0bc35-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="0bc35-216">Jákvæðir dagar eru hafðir með í útreikningi á lækkun spár.</span><span class="sxs-lookup"><span data-stu-id="0bc35-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="0bc35-217">Ef raunverulegar pöntunarfærslur°fara fram úr spáþörfum, eru eftirstandandi færslur ekki sendar áfram í næsta spátímabil.</span><span class="sxs-lookup"><span data-stu-id="0bc35-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="additional-resources"></a><span data-ttu-id="0bc35-218">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="0bc35-218">Additional resources</span></span>
--------

[<span data-ttu-id="0bc35-219">Aðaláætlanir</span><span class="sxs-lookup"><span data-stu-id="0bc35-219">Master plans</span></span>](master-plans.md)



