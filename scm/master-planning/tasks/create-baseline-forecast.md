--- 
title: "Búa til grunnlínuspá"
description: "Skipuleggjandi framleiðslu getur stofna grunnlínuspá með því að nota annað hvort spálíkön tímaraðar eða með því að afrita söguleg eftirspurn."
author: YuyuScheller
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e6363ee48c0d13c79a6c623205dfa10f50d6070f
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-baseline-forecast"></a><span data-ttu-id="43b5e-103">Búa til grunnlínuspá</span><span class="sxs-lookup"><span data-stu-id="43b5e-103">Create a baseline forecast</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43b5e-104">Skipuleggjandi framleiðslu getur stofna grunnlínuspá með því að nota annað hvort spálíkön tímaraðar eða með því að afrita söguleg eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="43b5e-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="43b5e-105">Þessi verklýsing sýnir hvernig á að stofna grunnlínuspá fyrir allar afurðir með því að nota eitt úthlutunarlykill vöru með því að afrita söguleg eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="43b5e-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span> 


## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="43b5e-106">Uppsetning vöruúthlutunarlykils</span><span class="sxs-lookup"><span data-stu-id="43b5e-106">Set up an item allocation key</span></span>
1. <span data-ttu-id="43b5e-107">Fara í Aðaláætlanagerð > Uppsetning > Áætlunarhópar innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="43b5e-107">Go to Master planning > Setup > Intercompany planning groups.</span></span>
2. <span data-ttu-id="43b5e-108">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="43b5e-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="43b5e-109">Til dæmis, sía svæðið Heiti með virði '10'.</span><span class="sxs-lookup"><span data-stu-id="43b5e-109">For example, filter on the Name field with a value of '10'.</span></span>
    * <span data-ttu-id="43b5e-110">Eftirspurnarspá keyrir milli lögaðila.</span><span class="sxs-lookup"><span data-stu-id="43b5e-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="43b5e-111">Þess vegna þarf að setja upp öll fyrirtæki sem á að mynda spár fyrir í eina áætlunarhóp innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="43b5e-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="43b5e-112">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="43b5e-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="43b5e-113">Smellt er á úthlutunarlykla vöru</span><span class="sxs-lookup"><span data-stu-id="43b5e-113">Click Item allocation keys.</span></span>
    * <span data-ttu-id="43b5e-114">Velja allar á úthlutunarlykla vöru sem á að stofna spá fyrir.</span><span class="sxs-lookup"><span data-stu-id="43b5e-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="43b5e-115">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="43b5e-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="43b5e-116">Veljið D_Aloc úthlutunarlykil vöru.</span><span class="sxs-lookup"><span data-stu-id="43b5e-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="43b5e-117">Smellt er á >.</span><span class="sxs-lookup"><span data-stu-id="43b5e-117">Click >.</span></span>
7. <span data-ttu-id="43b5e-118">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="43b5e-118">Close the page.</span></span>
8. <span data-ttu-id="43b5e-119">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="43b5e-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-paramters"></a><span data-ttu-id="43b5e-120">Setja upp færibreytur eftirspurnarspár</span><span class="sxs-lookup"><span data-stu-id="43b5e-120">Set up the demand forecasting paramters</span></span>
1. <span data-ttu-id="43b5e-121">Fara í Aðaláætlanagerð > Uppsetning > Eftirspurnarspá > Færibreytur eftirspurnarspár.</span><span class="sxs-lookup"><span data-stu-id="43b5e-121">Go to Master planning > Setup > Demand forecasting > Demand forecasting parameters.</span></span>
2. <span data-ttu-id="43b5e-122">Útvíkka hlutann Færibreytur reiknirita fyrir spá.</span><span class="sxs-lookup"><span data-stu-id="43b5e-122">Expand the Forecast algorithm parameters section.</span></span>
3. <span data-ttu-id="43b5e-123">Í stjórnunarstefnu Spármyndunar svæðinu, veljið 'Afrita yfir sögulega eftirspurn'.</span><span class="sxs-lookup"><span data-stu-id="43b5e-123">In the Forecast generation strategy field, select 'Copy over historical demand'.</span></span>
4. <span data-ttu-id="43b5e-124">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="43b5e-124">Click Save.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="43b5e-125">Búa til grunnlínuspá</span><span class="sxs-lookup"><span data-stu-id="43b5e-125">Create a baseline forecast</span></span>
1. <span data-ttu-id="43b5e-126">Fara í Aðaláætlanagerð > Spá > Eftirspurnarspá > Mynda tölfræðilega grunnlínuspá.</span><span class="sxs-lookup"><span data-stu-id="43b5e-126">Go to Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast.</span></span>
2. <span data-ttu-id="43b5e-127">Dagsetning er rituð í reitinn Frá dags.</span><span class="sxs-lookup"><span data-stu-id="43b5e-127">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="43b5e-128">Ef þú ert með sölupantanir sem byrja frá 1. Janúar, 2015, færðu inn þessa dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="43b5e-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="43b5e-129">Ef ekki, skal færa inn fyrstu dagsetningu sölupantanirnar.</span><span class="sxs-lookup"><span data-stu-id="43b5e-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="43b5e-130">Í reitinn Til dagsetningar skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="43b5e-130">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="43b5e-131">Færið inn síðustu dagsetningu sölupantana þinna, til dæmis '2015-03-31'..</span><span class="sxs-lookup"><span data-stu-id="43b5e-131">Enter the last date of your sales orders, for example '2015-03-31'.</span></span>  
4. <span data-ttu-id="43b5e-132">Dagsetning er rituð í reitinn Frá dags.</span><span class="sxs-lookup"><span data-stu-id="43b5e-132">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="43b5e-133">Færðu inn '2015-04-01'.</span><span class="sxs-lookup"><span data-stu-id="43b5e-133">Enter '2015-04-01'.</span></span> <span data-ttu-id="43b5e-134">Þessi dagsetning verður reiknaður sjálfvirkt sem upphafsdagsetning fyrir næsta tímaramma eftirspurnarspár.</span><span class="sxs-lookup"><span data-stu-id="43b5e-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="43b5e-135">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="43b5e-135">Expand the Records to include section.</span></span>
6. <span data-ttu-id="43b5e-136">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="43b5e-136">Click Filter.</span></span>
7. <span data-ttu-id="43b5e-137">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="43b5e-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="43b5e-138">Merkja línuna þar sem Svæðið = áætlunarhóp innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="43b5e-138">Mark the row where Field = Intercompany planning group.</span></span>  
8. <span data-ttu-id="43b5e-139">Í reitinn Skilyrði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="43b5e-139">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="43b5e-140">Færðu inn áætlunarhó innan samstæðu, t.d. 10, sem notað er í fyrsta verkefninu.</span><span class="sxs-lookup"><span data-stu-id="43b5e-140">Type the intercompany planning group, for example, 10, that you used in the first task.</span></span>  
9. <span data-ttu-id="43b5e-141">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="43b5e-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="43b5e-142">Veljið línuna þar sem Svæðið = úthlutunarlykil Vöru.</span><span class="sxs-lookup"><span data-stu-id="43b5e-142">Select the row where Field = Item allocation key.</span></span>  
10. <span data-ttu-id="43b5e-143">Í reitinn Skilyrði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="43b5e-143">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="43b5e-144">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="43b5e-144">Click OK.</span></span>
12. <span data-ttu-id="43b5e-145">Útvíkka hlutann Ítarlegar færibreytur.</span><span class="sxs-lookup"><span data-stu-id="43b5e-145">Expand the Advanced parameters section.</span></span>
13. <span data-ttu-id="43b5e-146">Veljið 'Mánuð' í svæði spárrammi.</span><span class="sxs-lookup"><span data-stu-id="43b5e-146">In the Forecast bucket field, select 'Month'.</span></span>
14. <span data-ttu-id="43b5e-147">Færa inn "3" í spátími svæði.</span><span class="sxs-lookup"><span data-stu-id="43b5e-147">In the Forecast horizon field, enter '3'.</span></span>
15. <span data-ttu-id="43b5e-148">Í svæði Frysta tímamörk , færið inn '1'.</span><span class="sxs-lookup"><span data-stu-id="43b5e-148">In the Freeze time fence field, enter '1'.</span></span>
16. <span data-ttu-id="43b5e-149">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="43b5e-149">Click OK.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="43b5e-150">Myndgera eftirspurnarspá</span><span class="sxs-lookup"><span data-stu-id="43b5e-150">Visualize the demand forecast</span></span>
1. <span data-ttu-id="43b5e-151">Fara í Aðaláætlanagerð > Spá > Eftirspurnarspá > Leiðrétt eftirspurnarspá.</span><span class="sxs-lookup"><span data-stu-id="43b5e-151">Go to Master planning > Forecasting > Demand forecasting > Adjusted demand forecast.</span></span>
2. <span data-ttu-id="43b5e-152">Í töflunni samanlagt yfirlit skal velja hólfið í línu 1 og dálki 2.</span><span class="sxs-lookup"><span data-stu-id="43b5e-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="43b5e-153">Þetta er annar mánuðinum sem búið er að stofna spá fyrir.</span><span class="sxs-lookup"><span data-stu-id="43b5e-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="43b5e-154">Stilla QtyCell á '400'.</span><span class="sxs-lookup"><span data-stu-id="43b5e-154">Set QtyCell to '400'.</span></span>
    * <span data-ttu-id="43b5e-155">Í reitnum, færa inn annað númer en það sem var spáð, til dæmis 400.</span><span class="sxs-lookup"><span data-stu-id="43b5e-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="43b5e-156">handvirkar leiðréttingar voru gerðar á Spá.</span><span class="sxs-lookup"><span data-stu-id="43b5e-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="43b5e-157">Athugið myndræna tilkynning í næsta þrepi.</span><span class="sxs-lookup"><span data-stu-id="43b5e-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="43b5e-158">Smellt er á Upplýsingar spárlínu</span><span class="sxs-lookup"><span data-stu-id="43b5e-158">Click Forecast line details.</span></span>
    * <span data-ttu-id="43b5e-159">Á þessari síðu er hægt að sjá nákvæmnisgildi, söguleg eftirspurn og spár.</span><span class="sxs-lookup"><span data-stu-id="43b5e-159">In this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="43b5e-160">Hægt er að gera breytingar á spá einnig.</span><span class="sxs-lookup"><span data-stu-id="43b5e-160">You can make changes to the forecast as well.</span></span>  


