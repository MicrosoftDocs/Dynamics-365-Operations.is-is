---
title: Minnkunarlyklar
description: "Þessi grein gefur dæmi um hvernig eigi að setja upp minnkunarlykil. Hún felur í sér upplýsingar um mismunandi stillingar minnkunarlykla og niðurstöður hverrar fyrir sig. Hægt er að nota minnkunarlykil til að skilgreina hvernig á að lækka spárþarfir."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqPlanSched
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19251
ms.assetid: aa9e0dfb-6052-4a2e-9378-89507c02fdf2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 506ca3aac7ad271ca7472f3b74627e94d97a74ee
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="reduction-keys"></a><span data-ttu-id="5d5b5-105">Minnkunarlyklar</span><span class="sxs-lookup"><span data-stu-id="5d5b5-105">Reduction keys</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5d5b5-106">Þessi grein gefur dæmi um hvernig eigi að setja upp minnkunarlykil.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-106">This articles provides examples that show how to set up a reduction key.</span></span> <span data-ttu-id="5d5b5-107">Hún felur í sér upplýsingar um mismunandi stillingar minnkunarlykla og niðurstöður hverrar fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-107">It includes information about the various reduction key settings and the results of each.</span></span> <span data-ttu-id="5d5b5-108">Hægt er að nota minnkunarlykil til að skilgreina hvernig á að lækka spárþarfir.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-108">You can use a reduction key to define how to reduce forecast requirements.</span></span>

<a name="example-1-percent---reduction-key-forecast-reduction-principle"></a><span data-ttu-id="5d5b5-109">Dæmi 1: Prósenta - minnkunarlykill spá lækkunarregla</span><span class="sxs-lookup"><span data-stu-id="5d5b5-109">Example 1: Percent - reduction key forecast reduction principle</span></span>
---------------------------------------------------------------

<span data-ttu-id="5d5b5-110">Þetta dæmi sýnir hvernig minnkunarlykill minnkar kröfur eftirspurnarspá í samræmi við prósentur og tímabil sem eru skilgreind af minnkunarlykli.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-110">This example shows how a reduction key reduces demand forecast requirements according to the percentages and periods that are defined by the reduction key.</span></span>

1.  <span data-ttu-id="5d5b5-111">Á **Minnkunarlyklar** síðunni, setjið upp eftirfarandi línur.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-111">On the **Reduction keys** page, set up the following lines.</span></span>
    | <span data-ttu-id="5d5b5-112">Skiptimynt</span><span class="sxs-lookup"><span data-stu-id="5d5b5-112">Change</span></span> | <span data-ttu-id="5d5b5-113">Eining</span><span class="sxs-lookup"><span data-stu-id="5d5b5-113">Unit</span></span>  | <span data-ttu-id="5d5b5-114">Prósent</span><span class="sxs-lookup"><span data-stu-id="5d5b5-114">Percent</span></span> |
    |--------|-------|---------|
    | <span data-ttu-id="5d5b5-115">1</span><span class="sxs-lookup"><span data-stu-id="5d5b5-115">1</span></span>      | <span data-ttu-id="5d5b5-116">Mánuður</span><span class="sxs-lookup"><span data-stu-id="5d5b5-116">Month</span></span> | <span data-ttu-id="5d5b5-117">100</span><span class="sxs-lookup"><span data-stu-id="5d5b5-117">100</span></span>     |
    | <span data-ttu-id="5d5b5-118">2</span><span class="sxs-lookup"><span data-stu-id="5d5b5-118">2</span></span>      | <span data-ttu-id="5d5b5-119">Mánuður</span><span class="sxs-lookup"><span data-stu-id="5d5b5-119">Month</span></span> | <span data-ttu-id="5d5b5-120">75</span><span class="sxs-lookup"><span data-stu-id="5d5b5-120">75</span></span>      |
    | <span data-ttu-id="5d5b5-121">3</span><span class="sxs-lookup"><span data-stu-id="5d5b5-121">3</span></span>      | <span data-ttu-id="5d5b5-122">Mánuður</span><span class="sxs-lookup"><span data-stu-id="5d5b5-122">Month</span></span> | <span data-ttu-id="5d5b5-123">50</span><span class="sxs-lookup"><span data-stu-id="5d5b5-123">50</span></span>      |
    | <span data-ttu-id="5d5b5-124">4</span><span class="sxs-lookup"><span data-stu-id="5d5b5-124">4</span></span>      | <span data-ttu-id="5d5b5-125">Mánuður</span><span class="sxs-lookup"><span data-stu-id="5d5b5-125">Month</span></span> | <span data-ttu-id="5d5b5-126">25</span><span class="sxs-lookup"><span data-stu-id="5d5b5-126">25</span></span>      |

2.  <span data-ttu-id="5d5b5-127">Tengja þarf minnkunarlykilinn við þekjuflokk vöru.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-127">Link the reduction key to the item's coverage group.</span></span>
3.  <span data-ttu-id="5d5b5-128">Á **Aðaláætlanir** síðunni,°í **Lækkunarreglu** svæðinu, veljið **Prósenta - minnkunarlykill**.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-128">On the **Master plans** page, in the **Reduction principle** field, select **Percent - reduction key**.</span></span>
4.  <span data-ttu-id="5d5b5-129">Stofnið söluspá fyrir 1.000 stykki á mánuði.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-129">Create a demand forecast of 1,000 pieces per month.</span></span>

<span data-ttu-id="5d5b5-130">Ef spárröðun er keyrð 1. Janúar, eru spáþarfir eftirspurnar nýttar samkvæmt prósentum sem settar eru upp á **Minnkunarlyklar** síðu.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-130">If you run forecast scheduling on January 1, the demand forecast requirements are consumed according to the percentages that you set up on the **Reduction keys** page.</span></span> <span data-ttu-id="5d5b5-131">Eftirfarandi þarfamagn er fært í aðaláætlun.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-131">The following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="5d5b5-132">Mánuður</span><span class="sxs-lookup"><span data-stu-id="5d5b5-132">Month</span></span>                | <span data-ttu-id="5d5b5-133">Fjöldi eintaka sem óskað er eftir</span><span class="sxs-lookup"><span data-stu-id="5d5b5-133">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="5d5b5-134">janúar</span><span class="sxs-lookup"><span data-stu-id="5d5b5-134">January</span></span>              | <span data-ttu-id="5d5b5-135">0</span><span class="sxs-lookup"><span data-stu-id="5d5b5-135">0</span></span>                         |
| <span data-ttu-id="5d5b5-136">febrúar</span><span class="sxs-lookup"><span data-stu-id="5d5b5-136">February</span></span>             | <span data-ttu-id="5d5b5-137">250</span><span class="sxs-lookup"><span data-stu-id="5d5b5-137">250</span></span>                       |
| <span data-ttu-id="5d5b5-138">mars</span><span class="sxs-lookup"><span data-stu-id="5d5b5-138">March</span></span>                | <span data-ttu-id="5d5b5-139">500</span><span class="sxs-lookup"><span data-stu-id="5d5b5-139">500</span></span>                       |
| <span data-ttu-id="5d5b5-140">Apríl</span><span class="sxs-lookup"><span data-stu-id="5d5b5-140">April</span></span>                | <span data-ttu-id="5d5b5-141">750</span><span class="sxs-lookup"><span data-stu-id="5d5b5-141">750</span></span>                       |
| <span data-ttu-id="5d5b5-142">Maí til og með desember</span><span class="sxs-lookup"><span data-stu-id="5d5b5-142">May through December</span></span> | <span data-ttu-id="5d5b5-143">1.000</span><span class="sxs-lookup"><span data-stu-id="5d5b5-143">1,000</span></span>                     |

## <a name="example-2-transactions--reduction-key-forecast-reduction-principle"></a><span data-ttu-id="5d5b5-144">Dæmi 2: Færslur  minnkunarlykill spá lækkunarreglu</span><span class="sxs-lookup"><span data-stu-id="5d5b5-144">Example 2: Transactions  reduction key forecast reduction principle</span></span>
<span data-ttu-id="5d5b5-145">Þetta dæmi sýnir hvernig raunverulegar pantanir sem eiga sér stað á tímabilum sem eru skilgreind af minnkunarlykli minnka kröfur eftirspurnarskrár.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-145">This example shows how actual orders that occur during the periods that are defined by the reduction key reduce demand forecast requirements.</span></span>

-   <span data-ttu-id="5d5b5-146">Á **Aðaláætlanir** síðunni,°í **Lækkunarreglu** svæðinu, veljið **Færslur - minnkunarlykill**.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-146">On the **Master plans** page, in the **Reduction principle** field, select **Transactions - reduction key**.</span></span>

<span data-ttu-id="5d5b5-147">Eftirfarandi sölupantanir eru tiltækar 1. janúar.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-147">The following sales orders exist on January 1.</span></span>

| <span data-ttu-id="5d5b5-148">Mánuður</span><span class="sxs-lookup"><span data-stu-id="5d5b5-148">Month</span></span>    | <span data-ttu-id="5d5b5-149">Fjöldi pantaðar stykkja</span><span class="sxs-lookup"><span data-stu-id="5d5b5-149">Number of pieces ordered</span></span> |
|----------|--------------------------|
| <span data-ttu-id="5d5b5-150">janúar</span><span class="sxs-lookup"><span data-stu-id="5d5b5-150">January</span></span>  | <span data-ttu-id="5d5b5-151">956</span><span class="sxs-lookup"><span data-stu-id="5d5b5-151">956</span></span>                      |
| <span data-ttu-id="5d5b5-152">febrúar</span><span class="sxs-lookup"><span data-stu-id="5d5b5-152">February</span></span> | <span data-ttu-id="5d5b5-153">1,176</span><span class="sxs-lookup"><span data-stu-id="5d5b5-153">1,176</span></span>                    |
| <span data-ttu-id="5d5b5-154">mars</span><span class="sxs-lookup"><span data-stu-id="5d5b5-154">March</span></span>    | <span data-ttu-id="5d5b5-155">451</span><span class="sxs-lookup"><span data-stu-id="5d5b5-155">451</span></span>                      |
| <span data-ttu-id="5d5b5-156">apríl</span><span class="sxs-lookup"><span data-stu-id="5d5b5-156">April</span></span>    | <span data-ttu-id="5d5b5-157">119</span><span class="sxs-lookup"><span data-stu-id="5d5b5-157">119</span></span>                      |

<span data-ttu-id="5d5b5-158">Ef sama söluspá fyrir 1.000 stykki á mánuði er notuð er eftirfarandi þarfamagn fært í aðaláætlun.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-158">If you use the same demand forecast of 1,000 pieces per month, the following requirement quantities are transferred to the master plan.</span></span>

| <span data-ttu-id="5d5b5-159">Mánuður</span><span class="sxs-lookup"><span data-stu-id="5d5b5-159">Month</span></span>                | <span data-ttu-id="5d5b5-160">Fjöldi eintaka sem óskað er eftir</span><span class="sxs-lookup"><span data-stu-id="5d5b5-160">Number of pieces required</span></span> |
|----------------------|---------------------------|
| <span data-ttu-id="5d5b5-161">janúar</span><span class="sxs-lookup"><span data-stu-id="5d5b5-161">January</span></span>              | <span data-ttu-id="5d5b5-162">44</span><span class="sxs-lookup"><span data-stu-id="5d5b5-162">44</span></span>                        |
| <span data-ttu-id="5d5b5-163">febrúar</span><span class="sxs-lookup"><span data-stu-id="5d5b5-163">February</span></span>             | <span data-ttu-id="5d5b5-164">0</span><span class="sxs-lookup"><span data-stu-id="5d5b5-164">0</span></span>                         |
| <span data-ttu-id="5d5b5-165">mars</span><span class="sxs-lookup"><span data-stu-id="5d5b5-165">March</span></span>                | <span data-ttu-id="5d5b5-166">549</span><span class="sxs-lookup"><span data-stu-id="5d5b5-166">549</span></span>                       |
| <span data-ttu-id="5d5b5-167">Apríl</span><span class="sxs-lookup"><span data-stu-id="5d5b5-167">April</span></span>                | <span data-ttu-id="5d5b5-168">881</span><span class="sxs-lookup"><span data-stu-id="5d5b5-168">881</span></span>                       |
| <span data-ttu-id="5d5b5-169">Maí til og með desember</span><span class="sxs-lookup"><span data-stu-id="5d5b5-169">May through December</span></span> | <span data-ttu-id="5d5b5-170">1.000</span><span class="sxs-lookup"><span data-stu-id="5d5b5-170">1,000</span></span>                     |

## <a name="example-3-transactions--dynamic-period-forecast-reduction-principle"></a><span data-ttu-id="5d5b5-171">Dæmi 3: Færslur breytileg tímabil spá lækkunarreglu</span><span class="sxs-lookup"><span data-stu-id="5d5b5-171">Example 3: Transactions  dynamic period forecast reduction principle</span></span>
<span data-ttu-id="5d5b5-172">Í flestum tilvikum eru kerfi sett upp þannig að færslur minnka eftirspurnarspár innan tiltekna spátímabila: vikur, mánuðir, og svo framvegis.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-172">In most cases, systems are set up so that transactions reduce demand forecast within specific forecast periods: weeks, months, and so on.</span></span> <span data-ttu-id="5d5b5-173">Þessi tímabil eru skilgreind í minnkunarlyklinum.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-173">These periods are defined in the reduction key.</span></span> <span data-ttu-id="5d5b5-174">Hins vegar getur tíminn milli tveggja eftirspurnarspárlína einnig *gefið til kynna* tímabil.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-174">However, the time between two demand forecast lines can also *imply* a period.</span></span>

1.  <span data-ttu-id="5d5b5-175">Stofna eftirspurnarspá fyrir eftirfarandi dagsetningar og magn.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-175">Create a demand forecast for the following dates and quantities.</span></span>
    | <span data-ttu-id="5d5b5-176">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="5d5b5-176">Date</span></span>       | <span data-ttu-id="5d5b5-177">Eftirspurnarspá</span><span class="sxs-lookup"><span data-stu-id="5d5b5-177">Demand forecast</span></span> |
    |------------|-----------------|
    | <span data-ttu-id="5d5b5-178">1. janúar</span><span class="sxs-lookup"><span data-stu-id="5d5b5-178">January 1</span></span>  | <span data-ttu-id="5d5b5-179">1.000</span><span class="sxs-lookup"><span data-stu-id="5d5b5-179">1,000</span></span>           |
    | <span data-ttu-id="5d5b5-180">5. janúar</span><span class="sxs-lookup"><span data-stu-id="5d5b5-180">January 5</span></span>  | <span data-ttu-id="5d5b5-181">500</span><span class="sxs-lookup"><span data-stu-id="5d5b5-181">500</span></span>             |
    | <span data-ttu-id="5d5b5-182">12. janúar</span><span class="sxs-lookup"><span data-stu-id="5d5b5-182">January 12</span></span> | <span data-ttu-id="5d5b5-183">1.000</span><span class="sxs-lookup"><span data-stu-id="5d5b5-183">1,000</span></span>           |

    <span data-ttu-id="5d5b5-184">Í þessari spá það er ekki greinilegt tímabil milli spádagsetninganna: Milli fyrstu og annarrar dagsetningar er°fjögurra daga bil og milli annarrar og þriðju dagsetningar er°sjö daga bil.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-184">In this forecast, there isn't a clear period between the forecast dates: between the first and second dates there is a four-day span, and between the second and third dates there is a seven-day span.</span></span> <span data-ttu-id="5d5b5-185">Þessi mismunandi bil eru breytileg tímabil.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-185">These various spans are the dynamic periods.</span></span>
2.  <span data-ttu-id="5d5b5-186">Stofna Sölupöntunarlínur á eftirfarandi hátt.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-186">Create sales order lines as follows.</span></span>
    | <span data-ttu-id="5d5b5-187">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="5d5b5-187">Date</span></span>                             | <span data-ttu-id="5d5b5-188">Sölupöntunarmagn</span><span class="sxs-lookup"><span data-stu-id="5d5b5-188">Sales order quantity</span></span> |
    |----------------------------------|----------------------|
    | <span data-ttu-id="5d5b5-189">15. Desember á fyrra ári</span><span class="sxs-lookup"><span data-stu-id="5d5b5-189">December 15 in the previous year</span></span> | <span data-ttu-id="5d5b5-190">500</span><span class="sxs-lookup"><span data-stu-id="5d5b5-190">500</span></span>                  |
    | <span data-ttu-id="5d5b5-191">3. janúar</span><span class="sxs-lookup"><span data-stu-id="5d5b5-191">January 3</span></span>                        | <span data-ttu-id="5d5b5-192">100</span><span class="sxs-lookup"><span data-stu-id="5d5b5-192">100</span></span>                  |
    | <span data-ttu-id="5d5b5-193">10. janúar</span><span class="sxs-lookup"><span data-stu-id="5d5b5-193">January 10</span></span>                       | <span data-ttu-id="5d5b5-194">200</span><span class="sxs-lookup"><span data-stu-id="5d5b5-194">200</span></span>                  |

<span data-ttu-id="5d5b5-195">Spáin verður lækkuð sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="5d5b5-195">The forecast will be reduced as follows:</span></span>

-   <span data-ttu-id="5d5b5-196">Fyrsta sölupöntun er ekki innan neins tímabils svo það ekki að draga úr neinni spá.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-196">The first sales order isn't within any period, so it won't reduce any forecast.</span></span>
-   <span data-ttu-id="5d5b5-197">Önnur sölupöntun er á milli 1. Janúar og 5. Janúar, þannig að hún lækkar spá fyrir 1. Janúar um 100.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-197">The second sales order is between January 1 and January 5, so it will reduce the forecast for January 1 by 100.</span></span>
-   <span data-ttu-id="5d5b5-198">Þriðja sölupöntun er á milli 5. Janúar og 12. Janúar, þannig að hún lækkar spá fyrir 5. Janúar um 200.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-198">The third sales order is between January 5 and January 12, so it will reduce the forecast for January 5 by 200.</span></span>

<span data-ttu-id="5d5b5-199">Eftirfarandi áætluð pöntun verður stofnuð til að uppfylla spána.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-199">The following planned order will be created to fulfill the forecast.</span></span>

| <span data-ttu-id="5d5b5-200">Dagsetning eftirspurnarspár</span><span class="sxs-lookup"><span data-stu-id="5d5b5-200">Demand forecast date</span></span> | <span data-ttu-id="5d5b5-201">Minnkað magn</span><span class="sxs-lookup"><span data-stu-id="5d5b5-201">Reduced quantity</span></span> |
|----------------------|------------------|
| <span data-ttu-id="5d5b5-202">1. janúar</span><span class="sxs-lookup"><span data-stu-id="5d5b5-202">January 1</span></span>            | <span data-ttu-id="5d5b5-203">900</span><span class="sxs-lookup"><span data-stu-id="5d5b5-203">900</span></span>              |
| <span data-ttu-id="5d5b5-204">5. janúar</span><span class="sxs-lookup"><span data-stu-id="5d5b5-204">January 5</span></span>            | <span data-ttu-id="5d5b5-205">300</span><span class="sxs-lookup"><span data-stu-id="5d5b5-205">300</span></span>              |
| <span data-ttu-id="5d5b5-206">12. janúar</span><span class="sxs-lookup"><span data-stu-id="5d5b5-206">January 12</span></span>           | <span data-ttu-id="5d5b5-207">1.000</span><span class="sxs-lookup"><span data-stu-id="5d5b5-207">1,000</span></span>            |

<span data-ttu-id="5d5b5-208">Hér er samantekt af°**Færslur - breytilegt tímabil** lækkun:</span><span class="sxs-lookup"><span data-stu-id="5d5b5-208">Here is a summary of **Transactions - dynamic period** reduction:</span></span>

-   <span data-ttu-id="5d5b5-209">Spáþarfir eru minnkaðar við raunverulega pöntunarfærslur sem koma upp við breytilegt tímabil.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-209">Forecast requirements are reduced by the actual order transactions that occur during the dynamic period.</span></span> <span data-ttu-id="5d5b5-210">Breytilegt tímabil nær yfir núgildandi spá dagsetningar og lýkur við upphaf næstu spár.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-210">The dynamic period covers the current forecast dates and ends at the start of the next forecast.</span></span>
-   <span data-ttu-id="5d5b5-211">Þessi aðferð notar hvorki né krefst minnkunarlykils.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-211">This method doesn't use or require a reduction key.</span></span>
-   <span data-ttu-id="5d5b5-212">Þegar þessi valkostur er notaður gerist eftirfarandi virkni:</span><span class="sxs-lookup"><span data-stu-id="5d5b5-212">When this option is used, the following behavior occurs:</span></span>
    -   <span data-ttu-id="5d5b5-213">Ef spá er alveg minnkuð verða spárþarfir gildandi spá 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="5d5b5-213">If the forecast is reduced completely, the forecast requirements for the current forecast become 0 (zero).</span></span>
    -   <span data-ttu-id="5d5b5-214">Ef það er engin komandi spá eru spáþarfir frá síðustu spá sem var færð inn minnkaðar.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-214">If there is no future forecast, forecast requirements from the last forecast that was entered are reduced.</span></span>
    -   <span data-ttu-id="5d5b5-215">Tímamörk eru hafðar með í útreikningi á lækkun spár.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-215">Time fences are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="5d5b5-216">Jákvæðir dagar eru hafðir með í útreikningi á lækkun spár.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-216">Positive days are included in the forecast reduction calculation.</span></span>
    -   <span data-ttu-id="5d5b5-217">Ef raunverulegar pöntunarfærslur°fara fram úr spáþörfum, eru eftirstandandi færslur ekki sendar áfram í næsta spátímabil.</span><span class="sxs-lookup"><span data-stu-id="5d5b5-217">If actual order transactions exceed the forecasted requirements, the remaining transactions aren't forwarded to the next forecast period.</span></span>


<a name="see-also"></a><span data-ttu-id="5d5b5-218">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5d5b5-218">See also</span></span>
--------

[<span data-ttu-id="5d5b5-219">Aðaláætlanir</span><span class="sxs-lookup"><span data-stu-id="5d5b5-219">Master plans</span></span>](master-plans.md)




