---
title: Eyðslugreining innkaupa Power BI efni
description: Þetta efnisatriði lýsir því hvað er innifalið í efnispakka eyðslugreiningar fyrir Power BI.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a4149b13754b544558dbb5666fbec7df97e5c5d8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559550"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="b9721-103">Eyðslugreining innkaupa Power BI efni</span><span class="sxs-lookup"><span data-stu-id="b9721-103">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9721-104">Þetta efnisatriði lýsir því hvað er innifalið í **Eyðslugreining innkaupa** Microsoft Power BI efni.</span><span class="sxs-lookup"><span data-stu-id="b9721-104">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="b9721-105">Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnið.</span><span class="sxs-lookup"><span data-stu-id="b9721-105">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="b9721-106">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="b9721-106">Overview</span></span>

<span data-ttu-id="b9721-107">**Efnispakki eyðslugreiningar innkaupa** Power BI-efni var stofnaður fyrir innkaupastjóra og stjórnendur sem bera ábyrgð á áætlunum.</span><span class="sxs-lookup"><span data-stu-id="b9721-107">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="b9721-108">Stjórnendur geta greint útgjöld við innkaup á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="b9721-108">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="b9721-109">Innkaup á árinu (eftir lánardrottnaflokki og stökum lánardrottnum, innkaupategund og stökum afurðum og staðsetningu lánardrottins)</span><span class="sxs-lookup"><span data-stu-id="b9721-109">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="b9721-110">Breytingar á innkaupum ár frá ári (eftir lánardrottnaflokki og innkaupategund)</span><span class="sxs-lookup"><span data-stu-id="b9721-110">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="b9721-111">Efnið notast við innkaupafærslugögn og gefur bæði samantekið yfirlit yfir innkaupatölur fyrirtækisins og sundurliðun á útgjöldum við innkaup eftir lánardrottnum og afurðum.</span><span class="sxs-lookup"><span data-stu-id="b9721-111">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="b9721-112">Skýrslur auðkenna breytingar í útgjöldum innkaupa yfir tíma.</span><span class="sxs-lookup"><span data-stu-id="b9721-112">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="b9721-113">Þannig má nota skýrslurnar til að gera stjórnendum viðvart um jákvæða og neikvæða útgjaldaþróun fyrir einstaka lánardrottna og afurðir.</span><span class="sxs-lookup"><span data-stu-id="b9721-113">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="b9721-114">Ennfremur sýna gröf innkaupaútgjöld fyrir mismunandi innkaupaflokka og lánardrottnahópa.</span><span class="sxs-lookup"><span data-stu-id="b9721-114">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="b9721-115">Því geta flokka- og svæðastjórnendur notað gröfin til að finna breytingar á útgjaldahegðun.</span><span class="sxs-lookup"><span data-stu-id="b9721-115">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="b9721-116">Aðgangur að Power BI efni</span><span class="sxs-lookup"><span data-stu-id="b9721-116">Accessing the Power BI content</span></span>
<span data-ttu-id="b9721-117">**Eyðslugreining innkaupa** Power BI-efni er sýnt á **Greining á innkaupum og eyðslu** síðunni (**Innkaup og aðföng** \> **Fyrirspurnir og skýrslur** \> **Greining á innkaupaárangri** \> **Greining á innkaupum og eyðslu**).</span><span class="sxs-lookup"><span data-stu-id="b9721-117">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="b9721-118">Mælikvarðar sem eru hafðir með í Power BI efni</span><span class="sxs-lookup"><span data-stu-id="b9721-118">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="b9721-119">**Eyðslugreining innkaupa** Power BI efni inniheldur skýrslu sem samanstendur af safni mælikvarða.</span><span class="sxs-lookup"><span data-stu-id="b9721-119">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="b9721-120">Þessir mælikvarðar eru birtir sem myndrit, reitir og töflur.</span><span class="sxs-lookup"><span data-stu-id="b9721-120">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="b9721-121">Eftirfarandi hlutar veita yfirlit yfir myndrænar framsetningar.</span><span class="sxs-lookup"><span data-stu-id="b9721-121">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="b9721-122">Skýrslusíða fyrir innkaup eftir lánardrottni</span><span class="sxs-lookup"><span data-stu-id="b9721-122">Purchase by vendor report page</span></span>
<span data-ttu-id="b9721-123">**Gröf**</span><span class="sxs-lookup"><span data-stu-id="b9721-123">**Charts**</span></span>
- <span data-ttu-id="b9721-124">Efstu 10 lánardrottnar eftir innkaupum (staflað súlurit)</span><span class="sxs-lookup"><span data-stu-id="b9721-124">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="b9721-125">Samtals innkaup eftir lánardrottnaflokki / landi / heiti (skífurit)</span><span class="sxs-lookup"><span data-stu-id="b9721-125">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="b9721-126">Innkaup eftir lánardrottnaflokki / landi / heiti (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="b9721-126">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="b9721-127">Meðaltal innkaupa eftir lánardrottnaflokki / landi / heiti (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="b9721-127">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="b9721-128">**Reitir**</span><span class="sxs-lookup"><span data-stu-id="b9721-128">**Tiles**</span></span>
- <span data-ttu-id="b9721-129">Heildarinnkaup</span><span class="sxs-lookup"><span data-stu-id="b9721-129">Total purchase</span></span>
- <span data-ttu-id="b9721-130">Vöxtur í innkaupum ár frá ári</span><span class="sxs-lookup"><span data-stu-id="b9721-130">YOY purchase growth</span></span>
- <span data-ttu-id="b9721-131">Samtala # lánardrottna</span><span class="sxs-lookup"><span data-stu-id="b9721-131">Total # vendors</span></span>
- <span data-ttu-id="b9721-132">Samtala # virkra lánardrottna</span><span class="sxs-lookup"><span data-stu-id="b9721-132">Total # of active vendors</span></span>

<span data-ttu-id="b9721-133">**Dæmi**</span><span class="sxs-lookup"><span data-stu-id="b9721-133">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="b9721-134">Skýrslusíða fyrir innkaup eftir afurðum</span><span class="sxs-lookup"><span data-stu-id="b9721-134">Purchase by product report page</span></span>

<span data-ttu-id="b9721-135">**Gröf**</span><span class="sxs-lookup"><span data-stu-id="b9721-135">**Charts**</span></span>
- <span data-ttu-id="b9721-136">Innkaup eftir innkaupategund / afurðarheiti (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="b9721-136">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="b9721-137">Heildarinnkaup eftir innkaupategund / afurðarheiti (skífurit)</span><span class="sxs-lookup"><span data-stu-id="b9721-137">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="b9721-138">Efstu 10 afurðir eftir innkaupum (staflað súlurit)</span><span class="sxs-lookup"><span data-stu-id="b9721-138">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="b9721-139">**Reitir**</span><span class="sxs-lookup"><span data-stu-id="b9721-139">**Tiles**</span></span>
- <span data-ttu-id="b9721-140">Samtala # afurða</span><span class="sxs-lookup"><span data-stu-id="b9721-140">Total # of products</span></span></li>
- <span data-ttu-id="b9721-141">Samtala prósentu virkra afurða af samtölu # afurða</span><span class="sxs-lookup"><span data-stu-id="b9721-141">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="b9721-142">Fjöldi afurða fyrir 80% innkaupa</span><span class="sxs-lookup"><span data-stu-id="b9721-142">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="b9721-143">**Dæmi**</span><span class="sxs-lookup"><span data-stu-id="b9721-143">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="b9721-144">Skýrslusíða fyrir innkaup eftir tímabili</span><span class="sxs-lookup"><span data-stu-id="b9721-144">Purchase by period report page</span></span>
<span data-ttu-id="b9721-145">Þessi síða sýnir innkaup þessa árs og síðasta árs og vöxtur eftir innkaupategund.</span><span class="sxs-lookup"><span data-stu-id="b9721-145">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="b9721-146">**Gröf**</span><span class="sxs-lookup"><span data-stu-id="b9721-146">**Charts**</span></span> 
- <span data-ttu-id="b9721-147">Innkaup eftir mánuði / degi (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="b9721-147">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="b9721-148">Uppsöfnuð frávik á innkaupum ár frá ári (fossarit)</span><span class="sxs-lookup"><span data-stu-id="b9721-148">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="b9721-149">Vöxtur í heildarinnkaupum ár frá ári (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="b9721-149">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="b9721-150">Innkaupayfirlit (fylki)</span><span class="sxs-lookup"><span data-stu-id="b9721-150">Procurement statement (matrix)</span></span>

<span data-ttu-id="b9721-151">**Reitir**</span><span class="sxs-lookup"><span data-stu-id="b9721-151">**Tiles**</span></span>
- <span data-ttu-id="b9721-152">Vöxtur í innkaupum ár frá ári</span><span class="sxs-lookup"><span data-stu-id="b9721-152">YOY purchase growth</span></span>
- <span data-ttu-id="b9721-153">Ár frá ári vöxtur í innkaupum</span><span class="sxs-lookup"><span data-stu-id="b9721-153">YOY purchase growth %</span></span>

<span data-ttu-id="b9721-154">**Dæmi**</span><span class="sxs-lookup"><span data-stu-id="b9721-154">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="b9721-155">Skýrslusíða fyrir innkaup eftir staðsetningu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="b9721-155">Purchase by vendor location report page</span></span>

<span data-ttu-id="b9721-156">**Gröf**</span><span class="sxs-lookup"><span data-stu-id="b9721-156">**Charts**</span></span>
- <span data-ttu-id="b9721-157">Innkaup eftir borg</span><span class="sxs-lookup"><span data-stu-id="b9721-157">Purchase by city</span></span>
- <span data-ttu-id="b9721-158">Vöxtur í innkaupum ár frá ári í %</span><span class="sxs-lookup"><span data-stu-id="b9721-158">Purchase YOY growth %</span></span>
- <span data-ttu-id="b9721-159">Innkaup eftir landi</span><span class="sxs-lookup"><span data-stu-id="b9721-159">Purchase by country</span></span>

<span data-ttu-id="b9721-160">**Dæmi**</span><span class="sxs-lookup"><span data-stu-id="b9721-160">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="b9721-161">Skýrslusíða fyrir eyðslugreiningu innkaupa eftir tíma</span><span class="sxs-lookup"><span data-stu-id="b9721-161">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="b9721-162">**Gröf**</span><span class="sxs-lookup"><span data-stu-id="b9721-162">**Charts**</span></span> 
- <span data-ttu-id="b9721-163">Innkaup núverandi árs eftir mánuðum / degi (línurit)</span><span class="sxs-lookup"><span data-stu-id="b9721-163">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="b9721-164">Innkaup núverandi og síðasta árs (línu- og stöplarit)</span><span class="sxs-lookup"><span data-stu-id="b9721-164">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="b9721-165">**Dæmi**</span><span class="sxs-lookup"><span data-stu-id="b9721-165">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="b9721-166">Skýrslusíða fyrir eyðslugreiningu innkaupa eftir lánardrottni</span><span class="sxs-lookup"><span data-stu-id="b9721-166">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="b9721-167">**Gröf**</span><span class="sxs-lookup"><span data-stu-id="b9721-167">**Charts**</span></span> 
- <span data-ttu-id="b9721-168">Efstu 10 innkaup lánardrottna % innkaupa (trekt)</span><span class="sxs-lookup"><span data-stu-id="b9721-168">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="b9721-169">Efstu 10 lánardrottnar með aukna eyðslu ár frá ári</span><span class="sxs-lookup"><span data-stu-id="b9721-169">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="b9721-170">Efstu 10 lánardrottnar með minnkaða eyðslu ár frá ári</span><span class="sxs-lookup"><span data-stu-id="b9721-170">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="b9721-171">**Dæmi** 
</span><span class="sxs-lookup"><span data-stu-id="b9721-171">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="b9721-172">Gagnalíkan og einingar</span><span class="sxs-lookup"><span data-stu-id="b9721-172">Data model and entities</span></span>
<span data-ttu-id="b9721-173">Eftirfarandi gögn eru notuð til að fylla út skýrslusíður í **Eyðslugreining innkaupa** Power BI efni.</span><span class="sxs-lookup"><span data-stu-id="b9721-173">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="b9721-174">Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni.</span><span class="sxs-lookup"><span data-stu-id="b9721-174">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="b9721-175">Einingaverslunin er Microsoft SQL Server gagnagrunnur sem er fínstillt fyrir greiningar.</span><span class="sxs-lookup"><span data-stu-id="b9721-175">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="b9721-176">Nánari upplýsingar er að finna í [Power BI samþætting við einingaverslun](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="b9721-176">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="b9721-177">Uppsafnaðar mælingar í þessum efnispakka eru undirflokkur uppsafnaðra mælinga sem voru tiltækar í Innkaupateningur í Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="b9721-177">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="b9721-178">Til að stilla uppsafnaðar mælingar tenings í einingaverslun verður að gera þær virkjanlegir.</span><span class="sxs-lookup"><span data-stu-id="b9721-178">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="b9721-179">Sjá frekari upplýsingar um ferli fyrir sviðsetningu uppsafnaðra mælinga í einingarverlsun í [Power BI-samþættingu við einingaverslun](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="b9721-179">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="b9721-180">Eftirfarandi uppsafnaðar lykilmælingar eru tiltækar beint úr reikningslínueiningunni og eru grunnur þessa efnispakka.</span><span class="sxs-lookup"><span data-stu-id="b9721-180">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="b9721-181">Eining</span><span class="sxs-lookup"><span data-stu-id="b9721-181">Entity</span></span>        | <span data-ttu-id="b9721-182">Lykiluppsafnaðar mælingar</span><span class="sxs-lookup"><span data-stu-id="b9721-182">Key aggregate measurements</span></span> | <span data-ttu-id="b9721-183">Uppruni gagna</span><span class="sxs-lookup"><span data-stu-id="b9721-183">Data source</span></span>                                 | <span data-ttu-id="b9721-184">Svæði</span><span class="sxs-lookup"><span data-stu-id="b9721-184">Field</span></span>              | <span data-ttu-id="b9721-185">lýsing</span><span class="sxs-lookup"><span data-stu-id="b9721-185">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="b9721-186">Reikningslínur</span><span class="sxs-lookup"><span data-stu-id="b9721-186">Invoice lines</span></span> | <span data-ttu-id="b9721-187">Innkaup</span><span class="sxs-lookup"><span data-stu-id="b9721-187">Purchase</span></span>                   | <span data-ttu-id="b9721-188">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="b9721-188">VendInvoiceTrans</span></span>                            | <span data-ttu-id="b9721-189">SAMTALA(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="b9721-189">SUM(LineAmountMST)</span></span> | <span data-ttu-id="b9721-190">Upphæðin í bókhaldsgjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="b9721-190">The amount in the accounting currency.</span></span> |

<span data-ttu-id="b9721-191">Eftirfarandi tafla sýnir lykilmælingarnar í efnispakkanum sem eru reiknaðar úr reikningslínueiningunni.</span><span class="sxs-lookup"><span data-stu-id="b9721-191">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="b9721-192">Mæla</span><span class="sxs-lookup"><span data-stu-id="b9721-192">Measure</span></span>               | <span data-ttu-id="b9721-193">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="b9721-193">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9721-194">Innkaup núverandi árs</span><span class="sxs-lookup"><span data-stu-id="b9721-194">Purchase current year</span></span> | <span data-ttu-id="b9721-195">Innkaup núverandi árs = SAMTALA ('Reikningslínur'\[Innkaupa\])</span><span class="sxs-lookup"><span data-stu-id="b9721-195">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="b9721-196">Innkaup síðasta árs</span><span class="sxs-lookup"><span data-stu-id="b9721-196">Purchase last year</span></span>    | <span data-ttu-id="b9721-197">Innkaup síðasta ár = REIKNA (SAMTALA ('Reikningslínur'\[Innkaupa\]), SAMEPERIODLASTYEAR (Dagsetningar\[Dagsetning\]))</span><span class="sxs-lookup"><span data-stu-id="b9721-197">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="b9721-198">Vöxtur í innkaupum ár frá ári</span><span class="sxs-lookup"><span data-stu-id="b9721-198">YOY purchase growth</span></span>   | <span data-ttu-id="b9721-199">Vöxtur í innkaupum ár frá ári = \[Innkaupa núverandi árs\] – \[Innkaupa síðasta árs\]</span><span class="sxs-lookup"><span data-stu-id="b9721-199">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="b9721-200">Eftirfarandi lykilvíddir í efnispakkanum eru notaðar sem síur til að sneiða uppsafnaðar mælingar þannig að hægt sé að ná meiri uppskiptingu og öðlast dýpri greiningarinnsýn.</span><span class="sxs-lookup"><span data-stu-id="b9721-200">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="b9721-201">Eining</span><span class="sxs-lookup"><span data-stu-id="b9721-201">Entity</span></span>                 | <span data-ttu-id="b9721-202">Dæmi um eigindir</span><span class="sxs-lookup"><span data-stu-id="b9721-202">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="b9721-203">Lánardrottnar</span><span class="sxs-lookup"><span data-stu-id="b9721-203">Vendors</span></span>                | <span data-ttu-id="b9721-204">Lánardrottnaflokkar, Lánardrottnaland eða -svæði, nafn Lánardrottins</span><span class="sxs-lookup"><span data-stu-id="b9721-204">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="b9721-205">Afurðir</span><span class="sxs-lookup"><span data-stu-id="b9721-205">Products</span></span>               | <span data-ttu-id="b9721-206">Afurðarnúmer, afurðarheiti, heiti vöruflokka</span><span class="sxs-lookup"><span data-stu-id="b9721-206">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="b9721-207">Innkaupaflokkar</span><span class="sxs-lookup"><span data-stu-id="b9721-207">Procurement categories</span></span> | <span data-ttu-id="b9721-208">Innkaupategund, nöfn innkaupategunda</span><span class="sxs-lookup"><span data-stu-id="b9721-208">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="b9721-209">Lögaðilar</span><span class="sxs-lookup"><span data-stu-id="b9721-209">Legal entities</span></span>         | <span data-ttu-id="b9721-210">Heiti lögaðila</span><span class="sxs-lookup"><span data-stu-id="b9721-210">Legal entity name</span></span>                                     |
| <span data-ttu-id="b9721-211">Dagsetningar</span><span class="sxs-lookup"><span data-stu-id="b9721-211">Dates</span></span>                  | <span data-ttu-id="b9721-212">Dagsetningar, Mótbókun árs</span><span class="sxs-lookup"><span data-stu-id="b9721-212">Dates, Year offset</span></span>                                    |

<span data-ttu-id="b9721-213">Sjálfgefið er að efnispakkinn sýni gögn fyrir núgildandi almanaksár.</span><span class="sxs-lookup"><span data-stu-id="b9721-213">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="b9721-214">Hins vegar er hægt að breyta dagsetningasíunni í síuhluta skýrslu.</span><span class="sxs-lookup"><span data-stu-id="b9721-214">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="b9721-215">Einnig er hægt að breyta síu fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="b9721-215">You can also change the company filter.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]