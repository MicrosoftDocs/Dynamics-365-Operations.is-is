---
title: Eyðslugreining innkaupa Power BI efni
description: Þetta efnisatriði lýsir því hvað er innifalið í efnispakka eyðslugreiningar fyrir Power BI. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru í efnispakkanum og veitir upplýsingar um gagnalíkan og einingar sem eru notaðar til að búa til efnið.
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 069c4dc21959ab603ba6ca3da0ac68ef20325265
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "313843"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="6fa60-104">Eyðslugreining innkaupa Power BI efni</span><span class="sxs-lookup"><span data-stu-id="6fa60-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fa60-105">Þetta efnisatriði lýsir því hvað er innifalið í **Eyðslugreining innkaupa** Microsoft Power BI efni.</span><span class="sxs-lookup"><span data-stu-id="6fa60-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="6fa60-106">Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnið.</span><span class="sxs-lookup"><span data-stu-id="6fa60-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="6fa60-107">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="6fa60-107">Overview</span></span>

<span data-ttu-id="6fa60-108">**Efnispakki eyðslugreiningar innkaupa** Power BI-efni var stofnaður fyrir innkaupastjóra og stjórnendur sem bera ábyrgð á áætlunum.</span><span class="sxs-lookup"><span data-stu-id="6fa60-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="6fa60-109">Stjórnendur geta greint útgjöld við innkaup á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="6fa60-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="6fa60-110">Innkaup á árinu (eftir lánardrottnaflokki og stökum lánardrottnum, innkaupategund og stökum afurðum og staðsetningu lánardrottins)</span><span class="sxs-lookup"><span data-stu-id="6fa60-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="6fa60-111">Breytingar á innkaupum ár frá ári (eftir lánardrottnaflokki og innkaupategund)</span><span class="sxs-lookup"><span data-stu-id="6fa60-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="6fa60-112">Efnið notast við innkaupafærslugögn og gefur bæði samantekið yfirlit yfir innkaupatölur fyrirtækisins og sundurliðun á útgjöldum við innkaup eftir lánardrottnum og afurðum.</span><span class="sxs-lookup"><span data-stu-id="6fa60-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="6fa60-113">Skýrslur auðkenna breytingar í útgjöldum innkaupa yfir tíma.</span><span class="sxs-lookup"><span data-stu-id="6fa60-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="6fa60-114">Þannig má nota skýrslurnar til að gera stjórnendum viðvart um jákvæða og neikvæða útgjaldaþróun fyrir einstaka lánardrottna og afurðir.</span><span class="sxs-lookup"><span data-stu-id="6fa60-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="6fa60-115">Ennfremur sýna gröf innkaupaútgjöld fyrir mismunandi innkaupaflokka og lánardrottnahópa.</span><span class="sxs-lookup"><span data-stu-id="6fa60-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="6fa60-116">Því geta flokka- og svæðastjórnendur notað gröfin til að finna breytingar á útgjaldahegðun.</span><span class="sxs-lookup"><span data-stu-id="6fa60-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="6fa60-117">Aðgangur að Power BI efni</span><span class="sxs-lookup"><span data-stu-id="6fa60-117">Accessing the Power BI content</span></span>
<span data-ttu-id="6fa60-118">**Eyðslugreining innkaupa** Power BI-efni er sýnt á **Greining á innkaupum og eyðslu** síðunni (**Innkaup og aðföng** \> **Fyrirspurnir og skýrslur** \> **Greining á innkaupaárangri** \> **Greining á innkaupum og eyðslu**).</span><span class="sxs-lookup"><span data-stu-id="6fa60-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="6fa60-119">Mælikvarðar sem eru hafðir með í Power BI efni</span><span class="sxs-lookup"><span data-stu-id="6fa60-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="6fa60-120">**Eyðslugreining innkaupa** Power BI efni inniheldur skýrslu sem samanstendur af safni mælikvarða.</span><span class="sxs-lookup"><span data-stu-id="6fa60-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="6fa60-121">Þessir mælikvarðar eru birtir sem myndrit, reitir og töflur.</span><span class="sxs-lookup"><span data-stu-id="6fa60-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="6fa60-122">Eftirfarandi tafla sýnir myndræna framsetningu.</span><span class="sxs-lookup"><span data-stu-id="6fa60-122">The following table provides an overview of the visualizations.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="6fa60-123">Skýrslusíða</span><span class="sxs-lookup"><span data-stu-id="6fa60-123">Report page</span></span></th>
<th><span data-ttu-id="6fa60-124">Gröf</span><span class="sxs-lookup"><span data-stu-id="6fa60-124">Charts</span></span></th>
<th><span data-ttu-id="6fa60-125">Reitir</span><span class="sxs-lookup"><span data-stu-id="6fa60-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="6fa60-126">Innkaup eftir lánardrottni</span><span class="sxs-lookup"><span data-stu-id="6fa60-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="6fa60-127">Efstu 10 lánardrottnar eftir innkaupum (staflað súlurit)</span><span class="sxs-lookup"><span data-stu-id="6fa60-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="6fa60-128">Samtals innkaup eftir lánardrottnaflokki / landi / heiti (skífurit)</span><span class="sxs-lookup"><span data-stu-id="6fa60-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="6fa60-129">Innkaup eftir lánardrottnaflokki / landi / heiti (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="6fa60-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="6fa60-130">Meðaltal innkaupa eftir lánardrottnaflokki / landi / heiti (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="6fa60-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6fa60-131">Heildarinnkaup</span><span class="sxs-lookup"><span data-stu-id="6fa60-131">Total purchase</span></span></li>
<li><span data-ttu-id="6fa60-132">Vöxtur í innkaupum ár frá ári</span><span class="sxs-lookup"><span data-stu-id="6fa60-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="6fa60-133">Samtala # lánardrottna</span><span class="sxs-lookup"><span data-stu-id="6fa60-133">Total # vendors</span></span></li>
<li><span data-ttu-id="6fa60-134">Samtala # virkra lánardrottna</span><span class="sxs-lookup"><span data-stu-id="6fa60-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="6fa60-135">Innkaup eftir afurðum</span><span class="sxs-lookup"><span data-stu-id="6fa60-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="6fa60-136">Innkaup eftir innkaupategund / afurðarheiti (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="6fa60-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="6fa60-137">Heildarinnkaup eftir innkaupategund / afurðarheiti (skífurit)</span><span class="sxs-lookup"><span data-stu-id="6fa60-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="6fa60-138">Efstu 10 afurðir eftir innkaupum (staflað súlurit)</span><span class="sxs-lookup"><span data-stu-id="6fa60-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6fa60-139">Samtala # afurða</span><span class="sxs-lookup"><span data-stu-id="6fa60-139">Total # of products</span></span></li>
<li><span data-ttu-id="6fa60-140">Samtala prósentu virkra afurða af samtölu # afurða</span><span class="sxs-lookup"><span data-stu-id="6fa60-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="6fa60-141">Fjöldi afurða fyrir 80% innkaupa</span><span class="sxs-lookup"><span data-stu-id="6fa60-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="6fa60-142">Innkaup eftir tímabili\*</span><span class="sxs-lookup"><span data-stu-id="6fa60-142">Purchase by period\*</span></span></td>
<td><ul>
<li><span data-ttu-id="6fa60-143">Innkaup eftir mánuði / degi (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="6fa60-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="6fa60-144">Uppsöfnuð frávik á innkaupum ár frá ári (fossarit)</span><span class="sxs-lookup"><span data-stu-id="6fa60-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="6fa60-145">Vöxtur í heildarinnkaupum ár frá ári (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="6fa60-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="6fa60-146">Innkaupayfirlit (fylki)</span><span class="sxs-lookup"><span data-stu-id="6fa60-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6fa60-147">Vöxtur í innkaupum ár frá ári</span><span class="sxs-lookup"><span data-stu-id="6fa60-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="6fa60-148">Ár frá ári vöxtur í innkaupum</span><span class="sxs-lookup"><span data-stu-id="6fa60-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="6fa60-149">Innkaupaáætlun eftir staðsetningu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="6fa60-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="6fa60-150">Innkaup eftir borg</span><span class="sxs-lookup"><span data-stu-id="6fa60-150">Purchase by city</span></span></li>
<li><span data-ttu-id="6fa60-151">Vöxtur í innkaupum ár frá ári í %</span><span class="sxs-lookup"><span data-stu-id="6fa60-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="6fa60-152">Innkaup eftir landi</span><span class="sxs-lookup"><span data-stu-id="6fa60-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="6fa60-153">Eyðslugreining innkaupa eftir tíma</span><span class="sxs-lookup"><span data-stu-id="6fa60-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="6fa60-154">Innkaup núverandi árs eftir mánuðum / degi (línurit)</span><span class="sxs-lookup"><span data-stu-id="6fa60-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="6fa60-155">Innkaup núverandi og síðasta árs (línu- og stöplarit)</span><span class="sxs-lookup"><span data-stu-id="6fa60-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="6fa60-156">Eyðslugreining innkaupa eftir lánardrottni</span><span class="sxs-lookup"><span data-stu-id="6fa60-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="6fa60-157">Efstu 10 innkaup lánardrottna % innkaupa (trekt)</span><span class="sxs-lookup"><span data-stu-id="6fa60-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="6fa60-158">Efstu 10 lánardrottnar með aukna eyðslu ár frá ári</span><span class="sxs-lookup"><span data-stu-id="6fa60-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="6fa60-159">Efstu 10 lánardrottnar með minnkaða eyðslu ár frá ári</span><span class="sxs-lookup"><span data-stu-id="6fa60-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="6fa60-160">\*Innkaup þessa árs og síðasta árs og vöxtur eftir innkaupategund</span><span class="sxs-lookup"><span data-stu-id="6fa60-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="6fa60-161">Gagnalíkan og einingar</span><span class="sxs-lookup"><span data-stu-id="6fa60-161">Data model and entities</span></span>
<span data-ttu-id="6fa60-162">Eftirfarandi gögn eru notuð til að fylla út skýrslusíður í **Eyðslugreining innkaupa** Power BI efni.</span><span class="sxs-lookup"><span data-stu-id="6fa60-162">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="6fa60-163">Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni.</span><span class="sxs-lookup"><span data-stu-id="6fa60-163">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="6fa60-164">Einingaverslunin er Microsoft SQL Server gagnagrunnur sem er fínstillt fyrir greiningar.</span><span class="sxs-lookup"><span data-stu-id="6fa60-164">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="6fa60-165">Frekari upplýsingar eru í [Yfirlit yfir samþættingu Power BI við einingaverslun](power-bi-integration-entity-store.md)</span><span class="sxs-lookup"><span data-stu-id="6fa60-165">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="6fa60-166">Uppsafnaðar mælingar í þessum efnispakka eru undirflokkur uppsafnaðra mælinga sem voru tiltækar í Innkaupateningur í Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="6fa60-166">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="6fa60-167">Til að stilla uppsafnaðar mælingar tenings í einingaverslun verður að gera þær virkjanlegir.</span><span class="sxs-lookup"><span data-stu-id="6fa60-167">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="6fa60-168">Sjá frekari upplýsingar um ferli fyrir sviðsetningu uppsafnaðra mælinga í einingarverlsu í [Yfirlit yfir Power BI samþættingu við einingaverslun ](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="6fa60-168">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="6fa60-169">Eftirfarandi uppsafnaðar lykilmælingar eru tiltækar beint úr reikningslínueiningunni og eru grunnur þessa efnispakka.</span><span class="sxs-lookup"><span data-stu-id="6fa60-169">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="6fa60-170">Eining</span><span class="sxs-lookup"><span data-stu-id="6fa60-170">Entity</span></span>        | <span data-ttu-id="6fa60-171">Lykiluppsafnaðar mælingar</span><span class="sxs-lookup"><span data-stu-id="6fa60-171">Key aggregate measurements</span></span> | <span data-ttu-id="6fa60-172">Uppruni gagna</span><span class="sxs-lookup"><span data-stu-id="6fa60-172">Data source</span></span>                                 | <span data-ttu-id="6fa60-173">Svæði</span><span class="sxs-lookup"><span data-stu-id="6fa60-173">Field</span></span>              | <span data-ttu-id="6fa60-174">lýsing</span><span class="sxs-lookup"><span data-stu-id="6fa60-174">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="6fa60-175">Reikningslínur</span><span class="sxs-lookup"><span data-stu-id="6fa60-175">Invoice lines</span></span> | <span data-ttu-id="6fa60-176">Innkaup</span><span class="sxs-lookup"><span data-stu-id="6fa60-176">Purchase</span></span>                   | <span data-ttu-id="6fa60-177">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="6fa60-177">VendInvoiceTrans</span></span>                            | <span data-ttu-id="6fa60-178">SAMTALA(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="6fa60-178">SUM(LineAmountMST)</span></span> | <span data-ttu-id="6fa60-179">Upphæðin í bókhaldsgjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="6fa60-179">The amount in the accounting currency.</span></span> |

<span data-ttu-id="6fa60-180">Eftirfarandi tafla sýnir lykilmælingarnar í efnispakkanum sem eru reiknaðar úr reikningslínueiningunni.</span><span class="sxs-lookup"><span data-stu-id="6fa60-180">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="6fa60-181">Mæla</span><span class="sxs-lookup"><span data-stu-id="6fa60-181">Measure</span></span>               | <span data-ttu-id="6fa60-182">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="6fa60-182">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6fa60-183">Innkaup núverandi árs</span><span class="sxs-lookup"><span data-stu-id="6fa60-183">Purchase current year</span></span> | <span data-ttu-id="6fa60-184">Innkaup núverandi árs = SAMTALA ('Reikningslínur'\[Innkaupa\])</span><span class="sxs-lookup"><span data-stu-id="6fa60-184">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="6fa60-185">Innkaup síðasta árs</span><span class="sxs-lookup"><span data-stu-id="6fa60-185">Purchase last year</span></span>    | <span data-ttu-id="6fa60-186">Innkaup síðasta ár = REIKNA (SAMTALA ('Reikningslínur'\[Innkaupa\]), SAMEPERIODLASTYEAR (Dagsetningar\[Dagsetning\]))</span><span class="sxs-lookup"><span data-stu-id="6fa60-186">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="6fa60-187">Vöxtur í innkaupum ár frá ári</span><span class="sxs-lookup"><span data-stu-id="6fa60-187">YOY purchase growth</span></span>   | <span data-ttu-id="6fa60-188">Vöxtur í innkaupum ár frá ári = \[Innkaupa núverandi árs\] – \[Innkaupa síðasta árs\]</span><span class="sxs-lookup"><span data-stu-id="6fa60-188">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="6fa60-189">Eftirfarandi lykilvíddir í efnispakkanum eru notaðar sem síur til að sneiða uppsafnaðar mælingar þannig að hægt sé að ná meiri uppskiptingu og öðlast dýpri greiningarinnsýn.</span><span class="sxs-lookup"><span data-stu-id="6fa60-189">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="6fa60-190">Eining</span><span class="sxs-lookup"><span data-stu-id="6fa60-190">Entity</span></span>                 | <span data-ttu-id="6fa60-191">Dæmi um eigindir</span><span class="sxs-lookup"><span data-stu-id="6fa60-191">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="6fa60-192">Lánardrottnar</span><span class="sxs-lookup"><span data-stu-id="6fa60-192">Vendors</span></span>                | <span data-ttu-id="6fa60-193">Lánardrottnaflokkar, Lánardrottnaland eða -svæði, nafn Lánardrottins</span><span class="sxs-lookup"><span data-stu-id="6fa60-193">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="6fa60-194">Afurðir</span><span class="sxs-lookup"><span data-stu-id="6fa60-194">Products</span></span>               | <span data-ttu-id="6fa60-195">Afurðarnúmer, afurðarheiti, heiti vöruflokka</span><span class="sxs-lookup"><span data-stu-id="6fa60-195">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="6fa60-196">Innkaupaflokkar</span><span class="sxs-lookup"><span data-stu-id="6fa60-196">Procurement categories</span></span> | <span data-ttu-id="6fa60-197">Innkaupategund, nöfn innkaupategunda</span><span class="sxs-lookup"><span data-stu-id="6fa60-197">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="6fa60-198">Lögaðilar</span><span class="sxs-lookup"><span data-stu-id="6fa60-198">Legal entities</span></span>         | <span data-ttu-id="6fa60-199">Heiti lögaðila</span><span class="sxs-lookup"><span data-stu-id="6fa60-199">Legal entity name</span></span>                                     |
| <span data-ttu-id="6fa60-200">Dagsetningar</span><span class="sxs-lookup"><span data-stu-id="6fa60-200">Dates</span></span>                  | <span data-ttu-id="6fa60-201">Dagsetningar, Mótbókun árs</span><span class="sxs-lookup"><span data-stu-id="6fa60-201">Dates, Year offset</span></span>                                    |

<span data-ttu-id="6fa60-202">Sjálfgefið er að efnispakkinn sýni gögn fyrir núgildandi almanaksár.</span><span class="sxs-lookup"><span data-stu-id="6fa60-202">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="6fa60-203">Hins vegar er hægt að breyta dagsetningasíunni í síuhluta skýrslu.</span><span class="sxs-lookup"><span data-stu-id="6fa60-203">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="6fa60-204">Einnig er hægt að breyta síu fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="6fa60-204">You can also change the company filter.</span></span>
