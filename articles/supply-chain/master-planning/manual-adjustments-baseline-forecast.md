---
title: "Gera handvirkar leiðréttingar á grunnlínuspánni"
description: "Þessi grein útskýrir hvernig á að gera handvirkar leiðréttingar á grunnlínuspá og skoða upplýsingar um spá."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 72704
ms.assetid: e7c5d44e-07bc-40b1-a4b3-8ba46483ef9e
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 218374cdb6b5588648422d97c04fb60f26e47ac7
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---

# <a name="make-manual-adjustments-to-the-baseline-forecast"></a><span data-ttu-id="b6863-103">Gera handvirkar leiðréttingar á grunnlínuspánni</span><span class="sxs-lookup"><span data-stu-id="b6863-103">Make manual adjustments to the baseline forecast</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b6863-104">Þessi grein útskýrir hvernig á að gera handvirkar leiðréttingar á grunnlínuspá og skoða upplýsingar um spá.</span><span class="sxs-lookup"><span data-stu-id="b6863-104">This article explains how you can make manual adjustments to a baseline forecast and view details of the forecast.</span></span> 

<span data-ttu-id="b6863-105">Áður en handvirkar leiðréttingar eru gerðar er mikilvægt að skilja nokkur hugtök útskýrð í mismunandi síður.</span><span class="sxs-lookup"><span data-stu-id="b6863-105">Before you make manual adjustments, it's important that you understand a few concepts on various pages.</span></span>

## <a name="grid-on-the-adjusted-demand-forecast-page"></a><span data-ttu-id="b6863-106">Hnitanetið á leiðréttri eftirspurnarspársíðu</span><span class="sxs-lookup"><span data-stu-id="b6863-106">Grid on the Adjusted demand forecast page</span></span>
<span data-ttu-id="b6863-107">**Leiðrétt eftirspurnarspá** síða inniheldur hnitanet sem hefur eftirfarandi skipulag:</span><span class="sxs-lookup"><span data-stu-id="b6863-107">The **Adjusted demand forecast** page includes a grid that has the following structure:</span></span>

-   <span data-ttu-id="b6863-108">Fyrsti dálkurinn sýnir vörur, úthlutunarlykla vöru, fyrirtæki og svo framvegis sem spáin hefur verið myndaður fyrir.</span><span class="sxs-lookup"><span data-stu-id="b6863-108">The first column shows the items, item allocation keys, companies, and so on, that the forecast has been generated for.</span></span> <span data-ttu-id="b6863-109">Undirfyrirsögn síðu gefur lýsingu á gildandi spávíddir sem birtast í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="b6863-109">The subtitle of the page provides a description of the current forecast dimensions that are shown in the grid.</span></span> <span data-ttu-id="b6863-110">Til dæmis, ef undirfyrirsögn síðu er **Fyrirtæki / Svæði / úthlutunarlykill Vöru**, og ein hausalínan í hnitanetinu er **USMF / 1 / D\_Alloc** sýnir sú lína spána fyrir USMF fyrirtækis , svæði 1, og **D\_Alloc** úthlutunarlykil vöru.</span><span class="sxs-lookup"><span data-stu-id="b6863-110">For example, if the subtitle of the page is **Company / Site / Item allocation key**, and one of the row headers in the grid is **USMF / 1 / D\_Alloc**, that row shows the forecast for the USMF company, site 1, and the **D\_Alloc** item allocation key.</span></span>
-   <span data-ttu-id="b6863-111">Síðari dálkar tákna spárammana sem spáin hefur verið myndaður fyrir.</span><span class="sxs-lookup"><span data-stu-id="b6863-111">Subsequent columns represent the forecast buckets that the forecast has been generated for.</span></span> <span data-ttu-id="b6863-112">Hver dálkhaus er fyrsta dagsetning spáramma sem dálkurinn sýnir.</span><span class="sxs-lookup"><span data-stu-id="b6863-112">Each column header is the first date of the forecast bucket that the column shows.</span></span>
-   <span data-ttu-id="b6863-113">Gildin í reitirnir standa fyrir spá fyrir eina vöru, úthlutunarlykill vöru og svo framvegis fyrir tiltekna spáramma.</span><span class="sxs-lookup"><span data-stu-id="b6863-113">The values in the cells represent the forecast for one item, item allocation key, and so on, for that specific forecast bucket.</span></span>

## <a name="forecast-aggregation-and-deaggregation"></a><span data-ttu-id="b6863-114">Uppsöfnun spár og af-uppsöfnun</span><span class="sxs-lookup"><span data-stu-id="b6863-114">Forecast aggregation and deaggregation</span></span>
<span data-ttu-id="b6863-115">Undirfyrirsögn síðu sýnir stigið fyrir uppsöfnun spár.</span><span class="sxs-lookup"><span data-stu-id="b6863-115">The subtitle of the page shows the level of forecast aggregation.</span></span> 

<span data-ttu-id="b6863-116">Til dæmis, ef undirfyrirsögn síðu er **Fyrirtæki / Svæði / úthlutunarlykil / Vörunúmer / Litur / Stærð / Skilgreiningu / Stíll**, er engin uppsöfnun spár og spá er sýnd á stigi vöru víddar hennar.</span><span class="sxs-lookup"><span data-stu-id="b6863-116">For example, if the subtitle of the page is **Company / Site / Allocation key / Item number / Color / Size / Configuration / Style**, there is no forecast aggregation, and the forecast is shown at the level of the item and its dimensions.</span></span> <span data-ttu-id="b6863-117">Ef breyta á uppsöfnun er að nota í **Breytingu spávíddir** síðu sem hægt er að opna úr hugbúnaðarvalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="b6863-117">To change the aggregation, use the **Change forecast dimensions** page, which you can open from the application menu.</span></span> 

<span data-ttu-id="b6863-118">Til að breyta spánni, smellið á eitthvað hólf sem er tiltækt, og slá inn leiðrétt spárgildi.</span><span class="sxs-lookup"><span data-stu-id="b6863-118">To modify the forecast, click in any of the cells that are available, and type the adjusted forecast value.</span></span> <span data-ttu-id="b6863-119">Nýju hólf verður strax feitletrað til að tilgreina að spá sem hún sýnir er ekki spáin sem þjónusta eftirspurnarspár stofnaði, en hefur verið leiðrétt handvirkt.</span><span class="sxs-lookup"><span data-stu-id="b6863-119">The edited cell immediately becomes bold to indicate that the forecast that it shows isn't the forecast that the demand forecasting service created, but has been manually adjusted.</span></span> 

<span data-ttu-id="b6863-120">Ef þú breytir uppsöfnun til að sýna fleiri uppsöfnuð gögn, er hægt að nota síðuna **eftirspurnarspálínur** síðu til sjá einstaka spárlínur sem mynda uppsafnaða spá.</span><span class="sxs-lookup"><span data-stu-id="b6863-120">If you change the aggregation to make the page show more aggregated data, you can use the **Demand forecast lines** page to see the individual forecast lines that make up the aggregated forecast.</span></span> 

<span data-ttu-id="b6863-121">Til dæmis, þú hefur búið spá á stigi vörunnar, en þú veist að eftirspurn eftir þessari vöru mun aukast á öllum staðsetningum vegna kynningar eða annan svipaðan viðburð.</span><span class="sxs-lookup"><span data-stu-id="b6863-121">For example, you've generated the forecast at the item level, but you know that the demand for this item will increase across all sites because of a promotion or another similar event.</span></span> <span data-ttu-id="b6863-122">Í þessu tilfelli er hægt að stilla uppsöfnun á **Fyrirtæki / Vöru úthlutun skilgreiningarlykils / Vöru** á **Breyta spávíddum** síðu.</span><span class="sxs-lookup"><span data-stu-id="b6863-122">In this case, you can set the aggregation to **Company / Item allocation key / Item** on the **Change forecast dimensions** page.</span></span> <span data-ttu-id="b6863-123">Hægt er að leiðrétta altæka spá fyrir vöruna yfir öll svæði í **Leiðrétt eftirspurnarspá** hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="b6863-123">You can adjust the global forecast for the item across all sites in the **Adjusted demand forecast** grid.</span></span> <span data-ttu-id="b6863-124">Til að sjá áhrifin af breytingu þinni yfir öll svæði, opna í **eftirspurnarspálínur** síðu.</span><span class="sxs-lookup"><span data-stu-id="b6863-124">To see the effect of your change across all sites, open the **Demand forecast lines** page.</span></span> <span data-ttu-id="b6863-125">Á þessari síðu birtist ein lína fyrir vöruna fyrir hvert svæði, leiðrétt spármagn og upprunalet spármagn.</span><span class="sxs-lookup"><span data-stu-id="b6863-125">On this page, you will see one line for the item for each site, the adjusted forecast quantity, and the original forecast quantity.</span></span> 

<span data-ttu-id="b6863-126">Þegar spáð magn er leiðrétt á uppsöfnuðum stigum notar kerfið vegna úthlutun til að dreifa breytingu á milli lína sem stofna uppsöfnunina.</span><span class="sxs-lookup"><span data-stu-id="b6863-126">When the adjustment of the forecasted quantity is made at an aggregated level, the system uses weighted allocation to distribute the change among the lines that create the aggregation.</span></span> 

<span data-ttu-id="b6863-127">Einnig er hægt að gera handvirkar leiðréttingar á á **eftirspurnarspálínur** síðu með því að breyta annað hvort **Heildarmagn** gildi eða **Magn** hólfum í af-uppsöfnunar hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="b6863-127">You can also make manual adjustments on the **Demand forecast lines** page, by modifying either the **Total quantity** value or the **Quantity** cells in the de-aggregation grid.</span></span>

## <a name="viewing-details-of-the-forecast"></a><span data-ttu-id="b6863-128">Skoða upplýsingar um spá</span><span class="sxs-lookup"><span data-stu-id="b6863-128">Viewing details of the forecast</span></span>
<span data-ttu-id="b6863-129">Hægt er að opna **upplýsingar eftirspurnarspár** síðu til að skoða frekari upplýsingar um spá.</span><span class="sxs-lookup"><span data-stu-id="b6863-129">You can open the **Demand forecast details** page to view more information about the forecast.</span></span> 

<span data-ttu-id="b6863-130">**upplýsingar eftirspurnarspár** síða sýnir eftirfarandi upplýsingar í myndrænu og töflulegu sniði:</span><span class="sxs-lookup"><span data-stu-id="b6863-130">The **Demand forecast details** page shows the following information in graphical and tabular formats:</span></span>

-   <span data-ttu-id="b6863-131">Söguleg eftirspurn sem spáreru byggðar á.</span><span class="sxs-lookup"><span data-stu-id="b6863-131">The historical demand that the forecast predictions are based on.</span></span>
-   <span data-ttu-id="b6863-132">Núverandi spá sem er notað með aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="b6863-132">The current forecast that is used by Master planning.</span></span>
-   <span data-ttu-id="b6863-133">Ný gildi eftirspurnarspár og upphæðir sem þeir hafa verið breytt handvirkt eftir.</span><span class="sxs-lookup"><span data-stu-id="b6863-133">The new demand forecast values and the amounts they have been manually adjusted by.</span></span>
-   <span data-ttu-id="b6863-134">Áreiðanleikabil fyrir spáð gildi.</span><span class="sxs-lookup"><span data-stu-id="b6863-134">The confidence interval for the forecasted values.</span></span>
-   <span data-ttu-id="b6863-135">Spárlíkan sem var notað til að búa til spá.</span><span class="sxs-lookup"><span data-stu-id="b6863-135">The forecast model that was used to generate the forecast.</span></span> <span data-ttu-id="b6863-136">Ef verið er að skoða uppsöfnuð gögn , sérðu lista yfir allar aðferðir sem voru notaðir fyrir allar uppsafnaðar tímaraðir.</span><span class="sxs-lookup"><span data-stu-id="b6863-136">If you're viewing aggregated data, you will see the list of all the methods that were used for all the aggregated time series.</span></span>
-   <span data-ttu-id="b6863-137">Innri nákvæmni líkans (MAPE).</span><span class="sxs-lookup"><span data-stu-id="b6863-137">The internal model accuracy (MAPE).</span></span> <span data-ttu-id="b6863-138">Nánari upplýsingar um nákvæmni eftirspurnarspár í [eftirlit með nákvæmni spár](monitor-forecast-accuracy.md).</span><span class="sxs-lookup"><span data-stu-id="b6863-138">For more information about forecast accuracy, see [Monitoring forecast accuracy](monitor-forecast-accuracy.md).</span></span>

<span data-ttu-id="b6863-139">**Athugasemdir :**</span><span class="sxs-lookup"><span data-stu-id="b6863-139">**Notes:**</span></span>

-   <span data-ttu-id="b6863-140">Áreiðanleikabil sem birtist í á **Spá** hluta síðan sýnir mismuninn á milli efri mörk áreiðanleikabils og neðri mörk áreiðanleikabils.</span><span class="sxs-lookup"><span data-stu-id="b6863-140">The confidence interval that appears in the **Forecast** section of the page represents the difference between the confidence interval upper limit and the confidence interval lower limit.</span></span> <span data-ttu-id="b6863-141">Til að sjá gildi fyrir efri og neðri mörk , settu  músabendil yfir línurit í á **söguleg eftirspurn og spá myndrænt** hluta.</span><span class="sxs-lookup"><span data-stu-id="b6863-141">To see the values for the upper and lower limits, hover over the chart in the **Historical demand and forecast graphically** section.</span></span>
-   <span data-ttu-id="b6863-142">Ef verið er að nota eftirspurnarspá Finance and Operations Microsoft Azure Machine-námsþjónustu, er hægt að tilgreina prósentu áreiðanleikastigs sem mynduð spá á að hafa.</span><span class="sxs-lookup"><span data-stu-id="b6863-142">If you use the Finance and Operations Demand forecasting Microsoft Azure Machine Learning service, you can specify the confidence level percentage that the forecast that is generated should have.</span></span> <span data-ttu-id="b6863-143">Áreiðanleikabil samanstendur af sviði gilda sem virka sem áreiðanlegt mat fyrir  eftirspurnarspána.</span><span class="sxs-lookup"><span data-stu-id="b6863-143">A confidence interval consists of a range of values that act as good estimates for the demand forecast.</span></span> <span data-ttu-id="b6863-144">Til dæmis gefur 95% áreiðanleikastig til kynna að það séu 5% líkur á að eftirspurnarspá falli utan sviðs áreiðanleikabils.</span><span class="sxs-lookup"><span data-stu-id="b6863-144">A 95-percent confidence level percentage indicates that there is a 5-percent risk that the demand forecast falls outside the confidence interval range.</span></span>

<span data-ttu-id="b6863-145">Einnig er hægt að gera handvirkar leiðréttingar á spá  í **upplýsingar eftirspurnarspár** síðu með því að breyta gildum í á **Spá** línunni í á **Spá** hluta.</span><span class="sxs-lookup"><span data-stu-id="b6863-145">You can also make manual adjustments to the forecast on the **Demand forecast details** page, by modifying the values in the **Forecast** row in the **Forecast** section.</span></span>

<a name="see-also"></a><span data-ttu-id="b6863-146">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="b6863-146">See also</span></span>
--------

[<span data-ttu-id="b6863-147">Fylgjast með nákvæmni spár</span><span class="sxs-lookup"><span data-stu-id="b6863-147">Monitoring forecast accuracy</span></span>](monitor-forecast-accuracy.md)

[<span data-ttu-id="b6863-148">Mynda tölfræðilega grunnlínuspá</span><span class="sxs-lookup"><span data-stu-id="b6863-148">Generating a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)




