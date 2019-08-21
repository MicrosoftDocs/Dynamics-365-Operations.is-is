---
title: Eyðslugreining innkaupa Power BI efni
description: Þetta efnisatriði lýsir því hvað er innifalið í efnispakka eyðslugreiningar fyrir Power BI. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru í efnispakkanum og veitir upplýsingar um gagnalíkan og einingar sem eru notaðar til að búa til efnið.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 571f443b02268cbee8fe787f25419e046ba99aeb
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850020"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="94217-104">Eyðslugreining innkaupa Power BI efni</span><span class="sxs-lookup"><span data-stu-id="94217-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94217-105">Þetta efnisatriði lýsir því hvað er innifalið í **Eyðslugreining innkaupa** Microsoft Power BI efni.</span><span class="sxs-lookup"><span data-stu-id="94217-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="94217-106">Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnið.</span><span class="sxs-lookup"><span data-stu-id="94217-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="94217-107">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="94217-107">Overview</span></span>

<span data-ttu-id="94217-108">**Efnispakki eyðslugreiningar innkaupa** Power BI-efni var stofnaður fyrir innkaupastjóra og stjórnendur sem bera ábyrgð á áætlunum.</span><span class="sxs-lookup"><span data-stu-id="94217-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="94217-109">Stjórnendur geta greint útgjöld við innkaup á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="94217-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="94217-110">Innkaup á árinu (eftir lánardrottnaflokki og stökum lánardrottnum, innkaupategund og stökum afurðum og staðsetningu lánardrottins)</span><span class="sxs-lookup"><span data-stu-id="94217-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="94217-111">Breytingar á innkaupum ár frá ári (eftir lánardrottnaflokki og innkaupategund)</span><span class="sxs-lookup"><span data-stu-id="94217-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="94217-112">Efnið notast við innkaupafærslugögn og gefur bæði samantekið yfirlit yfir innkaupatölur fyrirtækisins og sundurliðun á útgjöldum við innkaup eftir lánardrottnum og afurðum.</span><span class="sxs-lookup"><span data-stu-id="94217-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="94217-113">Skýrslur auðkenna breytingar í útgjöldum innkaupa yfir tíma.</span><span class="sxs-lookup"><span data-stu-id="94217-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="94217-114">Þannig má nota skýrslurnar til að gera stjórnendum viðvart um jákvæða og neikvæða útgjaldaþróun fyrir einstaka lánardrottna og afurðir.</span><span class="sxs-lookup"><span data-stu-id="94217-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="94217-115">Ennfremur sýna gröf innkaupaútgjöld fyrir mismunandi innkaupaflokka og lánardrottnahópa.</span><span class="sxs-lookup"><span data-stu-id="94217-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="94217-116">Því geta flokka- og svæðastjórnendur notað gröfin til að finna breytingar á útgjaldahegðun.</span><span class="sxs-lookup"><span data-stu-id="94217-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="94217-117">Aðgangur að Power BI efni</span><span class="sxs-lookup"><span data-stu-id="94217-117">Accessing the Power BI content</span></span>
<span data-ttu-id="94217-118">**Eyðslugreining innkaupa** Power BI-efni er sýnt á **Greining á innkaupum og eyðslu** síðunni (**Innkaup og aðföng** \> **Fyrirspurnir og skýrslur** \> **Greining á innkaupaárangri** \> **Greining á innkaupum og eyðslu**).</span><span class="sxs-lookup"><span data-stu-id="94217-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="94217-119">Mælikvarðar sem eru hafðir með í Power BI efni</span><span class="sxs-lookup"><span data-stu-id="94217-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="94217-120">**Eyðslugreining innkaupa** Power BI efni inniheldur skýrslu sem samanstendur af safni mælikvarða.</span><span class="sxs-lookup"><span data-stu-id="94217-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="94217-121">Þessir mælikvarðar eru birtir sem myndrit, reitir og töflur.</span><span class="sxs-lookup"><span data-stu-id="94217-121">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="94217-122">Eftirfarandi hlutar veita yfirlit yfir myndrænar framsetningar.</span><span class="sxs-lookup"><span data-stu-id="94217-122">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="94217-123">Skýrslusíða fyrir innkaup eftir lánardrottni</span><span class="sxs-lookup"><span data-stu-id="94217-123">Purchase by vendor report page</span></span>
<span data-ttu-id="94217-124">**Gröf**</span><span class="sxs-lookup"><span data-stu-id="94217-124">**Charts**</span></span>
- <span data-ttu-id="94217-125">Efstu 10 lánardrottnar eftir innkaupum (staflað súlurit)</span><span class="sxs-lookup"><span data-stu-id="94217-125">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="94217-126">Samtals innkaup eftir lánardrottnaflokki / landi / heiti (skífurit)</span><span class="sxs-lookup"><span data-stu-id="94217-126">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="94217-127">Innkaup eftir lánardrottnaflokki / landi / heiti (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="94217-127">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="94217-128">Meðaltal innkaupa eftir lánardrottnaflokki / landi / heiti (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="94217-128">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="94217-129">**Reitir**</span><span class="sxs-lookup"><span data-stu-id="94217-129">**Tiles**</span></span>
- <span data-ttu-id="94217-130">Heildarinnkaup</span><span class="sxs-lookup"><span data-stu-id="94217-130">Total purchase</span></span>
- <span data-ttu-id="94217-131">Vöxtur í innkaupum ár frá ári</span><span class="sxs-lookup"><span data-stu-id="94217-131">YOY purchase growth</span></span>
- <span data-ttu-id="94217-132">Samtala # lánardrottna</span><span class="sxs-lookup"><span data-stu-id="94217-132">Total # vendors</span></span>
- <span data-ttu-id="94217-133">Samtala # virkra lánardrottna</span><span class="sxs-lookup"><span data-stu-id="94217-133">Total # of active vendors</span></span>

<span data-ttu-id="94217-134">**Dæmi**</span><span class="sxs-lookup"><span data-stu-id="94217-134">**Example**</span></span>
<img src="media/spend1.PNG" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="94217-135">Skýrslusíða fyrir innkaup eftir afurðum</span><span class="sxs-lookup"><span data-stu-id="94217-135">Purchase by product report page</span></span>

<span data-ttu-id="94217-136">**Gröf**</span><span class="sxs-lookup"><span data-stu-id="94217-136">**Charts**</span></span>
- <span data-ttu-id="94217-137">Innkaup eftir innkaupategund / afurðarheiti (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="94217-137">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="94217-138">Heildarinnkaup eftir innkaupategund / afurðarheiti (skífurit)</span><span class="sxs-lookup"><span data-stu-id="94217-138">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="94217-139">Efstu 10 afurðir eftir innkaupum (staflað súlurit)</span><span class="sxs-lookup"><span data-stu-id="94217-139">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="94217-140">**Reitir**</span><span class="sxs-lookup"><span data-stu-id="94217-140">**Tiles**</span></span>
- <span data-ttu-id="94217-141">Samtala # afurða</span><span class="sxs-lookup"><span data-stu-id="94217-141">Total # of products</span></span></li>
- <span data-ttu-id="94217-142">Samtala prósentu virkra afurða af samtölu # afurða</span><span class="sxs-lookup"><span data-stu-id="94217-142">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="94217-143">Fjöldi afurða fyrir 80% innkaupa</span><span class="sxs-lookup"><span data-stu-id="94217-143">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="94217-144">**Dæmi**</span><span class="sxs-lookup"><span data-stu-id="94217-144">**Example**</span></span>


<img src="media/purchaseByProduct.PNG" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="94217-145">Skýrslusíða fyrir innkaup eftir tímabili</span><span class="sxs-lookup"><span data-stu-id="94217-145">Purchase by period report page</span></span>
<span data-ttu-id="94217-146">Þessi síða sýnir innkaup þessa árs og síðasta árs og vöxtur eftir innkaupategund.</span><span class="sxs-lookup"><span data-stu-id="94217-146">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="94217-147">**Gröf**</span><span class="sxs-lookup"><span data-stu-id="94217-147">**Charts**</span></span> 
- <span data-ttu-id="94217-148">Innkaup eftir mánuði / degi (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="94217-148">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="94217-149">Uppsöfnuð frávik á innkaupum ár frá ári (fossarit)</span><span class="sxs-lookup"><span data-stu-id="94217-149">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="94217-150">Vöxtur í heildarinnkaupum ár frá ári (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="94217-150">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="94217-151">Innkaupayfirlit (fylki)</span><span class="sxs-lookup"><span data-stu-id="94217-151">Procurement statement (matrix)</span></span>

<span data-ttu-id="94217-152">**Reitir**</span><span class="sxs-lookup"><span data-stu-id="94217-152">**Tiles**</span></span>
- <span data-ttu-id="94217-153">Vöxtur í innkaupum ár frá ári</span><span class="sxs-lookup"><span data-stu-id="94217-153">YOY purchase growth</span></span>
- <span data-ttu-id="94217-154">Ár frá ári vöxtur í innkaupum</span><span class="sxs-lookup"><span data-stu-id="94217-154">YOY purchase growth %</span></span>

<span data-ttu-id="94217-155">**Dæmi**</span><span class="sxs-lookup"><span data-stu-id="94217-155">**Example**</span></span>
<img src="media/purchaseByPeriod.PNG" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="94217-156">Skýrslusíða fyrir innkaup eftir staðsetningu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="94217-156">Purchase by vendor location report page</span></span>

<span data-ttu-id="94217-157">**Gröf**</span><span class="sxs-lookup"><span data-stu-id="94217-157">**Charts**</span></span>
- <span data-ttu-id="94217-158">Innkaup eftir borg</span><span class="sxs-lookup"><span data-stu-id="94217-158">Purchase by city</span></span>
- <span data-ttu-id="94217-159">Vöxtur í innkaupum ár frá ári í %</span><span class="sxs-lookup"><span data-stu-id="94217-159">Purchase YOY growth %</span></span>
- <span data-ttu-id="94217-160">Innkaup eftir landi</span><span class="sxs-lookup"><span data-stu-id="94217-160">Purchase by country</span></span>

<span data-ttu-id="94217-161">**Dæmi**</span><span class="sxs-lookup"><span data-stu-id="94217-161">**Example**</span></span>
<img src="media/purchByVendorLocation.PNG" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="94217-162">Skýrslusíða fyrir eyðslugreiningu innkaupa eftir tíma</span><span class="sxs-lookup"><span data-stu-id="94217-162">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="94217-163">**Gröf**</span><span class="sxs-lookup"><span data-stu-id="94217-163">**Charts**</span></span> 
- <span data-ttu-id="94217-164">Innkaup núverandi árs eftir mánuðum / degi (línurit)</span><span class="sxs-lookup"><span data-stu-id="94217-164">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="94217-165">Innkaup núverandi og síðasta árs (línu- og stöplarit)</span><span class="sxs-lookup"><span data-stu-id="94217-165">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="94217-166">**Dæmi**</span><span class="sxs-lookup"><span data-stu-id="94217-166">**Example**</span></span>
<img src="media/PurchByTIme.PNG" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="94217-167">Skýrslusíða fyrir eyðslugreiningu innkaupa eftir lánardrottni</span><span class="sxs-lookup"><span data-stu-id="94217-167">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="94217-168">**Gröf**</span><span class="sxs-lookup"><span data-stu-id="94217-168">**Charts**</span></span> 
- <span data-ttu-id="94217-169">Efstu 10 innkaup lánardrottna % innkaupa (trekt)</span><span class="sxs-lookup"><span data-stu-id="94217-169">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="94217-170">Efstu 10 lánardrottnar með aukna eyðslu ár frá ári</span><span class="sxs-lookup"><span data-stu-id="94217-170">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="94217-171">Efstu 10 lánardrottnar með minnkaða eyðslu ár frá ári</span><span class="sxs-lookup"><span data-stu-id="94217-171">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="94217-172">**Dæmi** 
</span><span class="sxs-lookup"><span data-stu-id="94217-172">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.PNG" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="94217-173">Gagnalíkan og einingar</span><span class="sxs-lookup"><span data-stu-id="94217-173">Data model and entities</span></span>
<span data-ttu-id="94217-174">Eftirfarandi gögn eru notuð til að fylla út skýrslusíður í **Eyðslugreining innkaupa** Power BI efni.</span><span class="sxs-lookup"><span data-stu-id="94217-174">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="94217-175">Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni.</span><span class="sxs-lookup"><span data-stu-id="94217-175">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="94217-176">Einingaverslunin er Microsoft SQL Server gagnagrunnur sem er fínstillt fyrir greiningar.</span><span class="sxs-lookup"><span data-stu-id="94217-176">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="94217-177">Frekari upplýsingar eru í [Yfirlit yfir samþættingu Power BI við einingaverslun](power-bi-integration-entity-store.md)</span><span class="sxs-lookup"><span data-stu-id="94217-177">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="94217-178">Uppsafnaðar mælingar í þessum efnispakka eru undirflokkur uppsafnaðra mælinga sem voru tiltækar í Innkaupateningur í Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="94217-178">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="94217-179">Til að stilla uppsafnaðar mælingar tenings í einingaverslun verður að gera þær virkjanlegir.</span><span class="sxs-lookup"><span data-stu-id="94217-179">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="94217-180">Sjá frekari upplýsingar um ferli fyrir sviðsetningu uppsafnaðra mælinga í einingarverlsu í [Yfirlit yfir Power BI samþættingu við einingaverslun](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="94217-180">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="94217-181">Eftirfarandi uppsafnaðar lykilmælingar eru tiltækar beint úr reikningslínueiningunni og eru grunnur þessa efnispakka.</span><span class="sxs-lookup"><span data-stu-id="94217-181">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="94217-182">Eining</span><span class="sxs-lookup"><span data-stu-id="94217-182">Entity</span></span>        | <span data-ttu-id="94217-183">Lykiluppsafnaðar mælingar</span><span class="sxs-lookup"><span data-stu-id="94217-183">Key aggregate measurements</span></span> | <span data-ttu-id="94217-184">Uppruni gagna</span><span class="sxs-lookup"><span data-stu-id="94217-184">Data source</span></span>                                 | <span data-ttu-id="94217-185">Svæði</span><span class="sxs-lookup"><span data-stu-id="94217-185">Field</span></span>              | <span data-ttu-id="94217-186">lýsing</span><span class="sxs-lookup"><span data-stu-id="94217-186">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="94217-187">Reikningslínur</span><span class="sxs-lookup"><span data-stu-id="94217-187">Invoice lines</span></span> | <span data-ttu-id="94217-188">Innkaup</span><span class="sxs-lookup"><span data-stu-id="94217-188">Purchase</span></span>                   | <span data-ttu-id="94217-189">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="94217-189">VendInvoiceTrans</span></span>                            | <span data-ttu-id="94217-190">SAMTALA(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="94217-190">SUM(LineAmountMST)</span></span> | <span data-ttu-id="94217-191">Upphæðin í bókhaldsgjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="94217-191">The amount in the accounting currency.</span></span> |

<span data-ttu-id="94217-192">Eftirfarandi tafla sýnir lykilmælingarnar í efnispakkanum sem eru reiknaðar úr reikningslínueiningunni.</span><span class="sxs-lookup"><span data-stu-id="94217-192">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="94217-193">Mæla</span><span class="sxs-lookup"><span data-stu-id="94217-193">Measure</span></span>               | <span data-ttu-id="94217-194">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="94217-194">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94217-195">Innkaup núverandi árs</span><span class="sxs-lookup"><span data-stu-id="94217-195">Purchase current year</span></span> | <span data-ttu-id="94217-196">Innkaup núverandi árs = SAMTALA ('Reikningslínur'\[Innkaupa\])</span><span class="sxs-lookup"><span data-stu-id="94217-196">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="94217-197">Innkaup síðasta árs</span><span class="sxs-lookup"><span data-stu-id="94217-197">Purchase last year</span></span>    | <span data-ttu-id="94217-198">Innkaup síðasta ár = REIKNA (SAMTALA ('Reikningslínur'\[Innkaupa\]), SAMEPERIODLASTYEAR (Dagsetningar\[Dagsetning\]))</span><span class="sxs-lookup"><span data-stu-id="94217-198">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="94217-199">Vöxtur í innkaupum ár frá ári</span><span class="sxs-lookup"><span data-stu-id="94217-199">YOY purchase growth</span></span>   | <span data-ttu-id="94217-200">Vöxtur í innkaupum ár frá ári = \[Innkaupa núverandi árs\] – \[Innkaupa síðasta árs\]</span><span class="sxs-lookup"><span data-stu-id="94217-200">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="94217-201">Eftirfarandi lykilvíddir í efnispakkanum eru notaðar sem síur til að sneiða uppsafnaðar mælingar þannig að hægt sé að ná meiri uppskiptingu og öðlast dýpri greiningarinnsýn.</span><span class="sxs-lookup"><span data-stu-id="94217-201">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="94217-202">Eining</span><span class="sxs-lookup"><span data-stu-id="94217-202">Entity</span></span>                 | <span data-ttu-id="94217-203">Dæmi um eigindir</span><span class="sxs-lookup"><span data-stu-id="94217-203">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="94217-204">Lánardrottnar</span><span class="sxs-lookup"><span data-stu-id="94217-204">Vendors</span></span>                | <span data-ttu-id="94217-205">Lánardrottnaflokkar, Lánardrottnaland eða -svæði, nafn Lánardrottins</span><span class="sxs-lookup"><span data-stu-id="94217-205">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="94217-206">Afurðir</span><span class="sxs-lookup"><span data-stu-id="94217-206">Products</span></span>               | <span data-ttu-id="94217-207">Afurðarnúmer, afurðarheiti, heiti vöruflokka</span><span class="sxs-lookup"><span data-stu-id="94217-207">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="94217-208">Innkaupaflokkar</span><span class="sxs-lookup"><span data-stu-id="94217-208">Procurement categories</span></span> | <span data-ttu-id="94217-209">Innkaupategund, nöfn innkaupategunda</span><span class="sxs-lookup"><span data-stu-id="94217-209">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="94217-210">Lögaðilar</span><span class="sxs-lookup"><span data-stu-id="94217-210">Legal entities</span></span>         | <span data-ttu-id="94217-211">Heiti lögaðila</span><span class="sxs-lookup"><span data-stu-id="94217-211">Legal entity name</span></span>                                     |
| <span data-ttu-id="94217-212">Dagsetningar</span><span class="sxs-lookup"><span data-stu-id="94217-212">Dates</span></span>                  | <span data-ttu-id="94217-213">Dagsetningar, Mótbókun árs</span><span class="sxs-lookup"><span data-stu-id="94217-213">Dates, Year offset</span></span>                                    |

<span data-ttu-id="94217-214">Sjálfgefið er að efnispakkinn sýni gögn fyrir núgildandi almanaksár.</span><span class="sxs-lookup"><span data-stu-id="94217-214">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="94217-215">Hins vegar er hægt að breyta dagsetningasíunni í síuhluta skýrslu.</span><span class="sxs-lookup"><span data-stu-id="94217-215">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="94217-216">Einnig er hægt að breyta síu fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="94217-216">You can also change the company filter.</span></span>
