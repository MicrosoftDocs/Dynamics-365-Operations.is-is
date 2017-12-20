---
title: "Efni Power BI eyðslugreining innkaupa"
description: "Þetta efnisatriði lýsir því hvað er innifalið í Power BI efninu Greining á innkaupaútgjöldum Það lýsir einnig hvernig eigi að fara í skýrslur sem eru í efnispakkanum og veitir upplýsingar um gagnalíkan og einingar sem eru notaðar til að búa til efnið."
author: FrankDahl
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: f38f82b4275599a6b958c495f32b72778b400024
ms.contentlocale: is-is
ms.lasthandoff: 12/01/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="116f6-104">Efni Power BI eyðslugreining innkaupa</span><span class="sxs-lookup"><span data-stu-id="116f6-104">Purchase spend analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="116f6-105">Þetta efnisatriði lýsir því hvað er innifalið í Power BI efninu **Greining á innkaupaútgjöldum**.</span><span class="sxs-lookup"><span data-stu-id="116f6-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="116f6-106">Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnið.</span><span class="sxs-lookup"><span data-stu-id="116f6-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="116f6-107">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="116f6-107">Overview</span></span>

<span data-ttu-id="116f6-108">Power BI efnið **Greining á innkaupaútgjöldum** var hannað til að auðvelda innkaupastjórum og stjórnendum sem bera ábyrgð á fjárhagsáætlunum að fylgjast með innkaupaútgjöldum.</span><span class="sxs-lookup"><span data-stu-id="116f6-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="116f6-109">Stjórnendur geta greint útgjöld við innkaup á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="116f6-109">Managers can analyze purchase spending in the following ways:</span></span>

-   <span data-ttu-id="116f6-110">Innkaup á árinu (eftir lánardrottnaflokki og stökum lánardrottnum, innkaupategund og stökum afurðum og staðsetningu lánardrottins)</span><span class="sxs-lookup"><span data-stu-id="116f6-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
-   <span data-ttu-id="116f6-111">Breytingar á innkaupum ár frá ári (eftir lánardrottnaflokki og innkaupategund)</span><span class="sxs-lookup"><span data-stu-id="116f6-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="116f6-112">Efnið notast við innkaupafærslugögn og gefur bæði samantekið yfirlit yfir innkaupatölur fyrirtækisins og sundurliðun á útgjöldum við innkaup eftir lánardrottnum og afurðum.</span><span class="sxs-lookup"><span data-stu-id="116f6-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="116f6-113">Skýrslur auðkenna breytingar í útgjöldum innkaupa yfir tíma.</span><span class="sxs-lookup"><span data-stu-id="116f6-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="116f6-114">Þannig má nota skýrslurnar til að gera stjórnendum viðvart um jákvæða og neikvæða útgjaldaþróun fyrir einstaka lánardrottna og afurðir.</span><span class="sxs-lookup"><span data-stu-id="116f6-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="116f6-115">Ennfremur sýna gröf innkaupaútgjöld fyrir mismunandi innkaupaflokka og lánardrottnahópa.</span><span class="sxs-lookup"><span data-stu-id="116f6-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="116f6-116">Því geta flokka- og svæðastjórnendur notað gröfin til að finna breytingar á útgjaldahegðun.</span><span class="sxs-lookup"><span data-stu-id="116f6-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="116f6-117">Farið í Power BI-efni</span><span class="sxs-lookup"><span data-stu-id="116f6-117">Accessing the Power BI content</span></span>
<span data-ttu-id="116f6-118">**Eyðslugreining innkaupa** Power BI efni er sýnt á **Greining á innkaupum og eyðslu** síðunni (**Innkaup og aðföng** > **Fyrirspurnir og skýrslur** > **Greining á innkaupaárangri** > **Greining á innkaupum og eyðslu**).</span><span class="sxs-lookup"><span data-stu-id="116f6-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** > **Inquiries and reports** > **Purchase performance analysis** > **Purchase and spend analysis**).</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="116f6-119">Mælikvarðar sem eru hafðir með í Power BI-efni</span><span class="sxs-lookup"><span data-stu-id="116f6-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="116f6-120">Power BI efnið **Greining á innkaupaútgjöldum** inniheldur skýrslu sem samanstendur af safni mæligilda.</span><span class="sxs-lookup"><span data-stu-id="116f6-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="116f6-121">Þessir mælikvarðar eru birtir sem myndrit, reitir og töflur.</span><span class="sxs-lookup"><span data-stu-id="116f6-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="116f6-122">Eftirfarandi tafla sýnir myndræna framsetningu.</span><span class="sxs-lookup"><span data-stu-id="116f6-122">The following table provides an overview of the visualizations.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="116f6-123">Skýrslusíða</span><span class="sxs-lookup"><span data-stu-id="116f6-123">Report page</span></span></th>
<th><span data-ttu-id="116f6-124">Gröf</span><span class="sxs-lookup"><span data-stu-id="116f6-124">Charts</span></span></th>
<th><span data-ttu-id="116f6-125">Reitir</span><span class="sxs-lookup"><span data-stu-id="116f6-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="116f6-126">Innkaup eftir lánardrottni</span><span class="sxs-lookup"><span data-stu-id="116f6-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="116f6-127">Efstu 10 lánardrottnar eftir innkaupum (staflað súlurit)</span><span class="sxs-lookup"><span data-stu-id="116f6-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="116f6-128">Samtals innkaup eftir lánardrottnaflokki / landi / heiti (skífurit)</span><span class="sxs-lookup"><span data-stu-id="116f6-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="116f6-129">Innkaup eftir lánardrottnaflokki / landi / heiti (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="116f6-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="116f6-130">Meðaltal innkaupa eftir lánardrottnaflokki / landi / heiti (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="116f6-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="116f6-131">Heildarinnkaup</span><span class="sxs-lookup"><span data-stu-id="116f6-131">Total purchase</span></span></li>
<li><span data-ttu-id="116f6-132">Vöxtur í innkaupum ár frá ári</span><span class="sxs-lookup"><span data-stu-id="116f6-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="116f6-133">Samtala # lánardrottna</span><span class="sxs-lookup"><span data-stu-id="116f6-133">Total # vendors</span></span></li>
<li><span data-ttu-id="116f6-134">Samtala # virkra lánardrottna</span><span class="sxs-lookup"><span data-stu-id="116f6-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="116f6-135">Innkaup eftir afurðum</span><span class="sxs-lookup"><span data-stu-id="116f6-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="116f6-136">Innkaup eftir innkaupategund / afurðarheiti (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="116f6-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="116f6-137">Heildarinnkaup eftir innkaupategund / afurðarheiti (skífurit)</span><span class="sxs-lookup"><span data-stu-id="116f6-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="116f6-138">Efstu 10 afurðir eftir innkaupum (staflað súlurit)</span><span class="sxs-lookup"><span data-stu-id="116f6-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="116f6-139">Samtala # afurða</span><span class="sxs-lookup"><span data-stu-id="116f6-139">Total # of products</span></span></li>
<li><span data-ttu-id="116f6-140">Samtala prósentu virkra afurða af samtölu # afurða</span><span class="sxs-lookup"><span data-stu-id="116f6-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="116f6-141">Fjöldi afurða fyrir 80% innkaupa</span><span class="sxs-lookup"><span data-stu-id="116f6-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="116f6-142">Innkaup eftir tímabili*</span><span class="sxs-lookup"><span data-stu-id="116f6-142">Purchase by period*</span></span></td>
<td><ul>
<li><span data-ttu-id="116f6-143">Innkaup eftir mánuði / degi (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="116f6-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="116f6-144">Uppsöfnuð frávik á innkaupum ár frá ári (fossarit)</span><span class="sxs-lookup"><span data-stu-id="116f6-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="116f6-145">Vöxtur í heildarinnkaupum ár frá ári (stöplarit)</span><span class="sxs-lookup"><span data-stu-id="116f6-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="116f6-146">Innkaupayfirlit (fylki)</span><span class="sxs-lookup"><span data-stu-id="116f6-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="116f6-147">Vöxtur í innkaupum ár frá ári</span><span class="sxs-lookup"><span data-stu-id="116f6-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="116f6-148">Ár frá ári vöxtur í innkaupum</span><span class="sxs-lookup"><span data-stu-id="116f6-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="116f6-149">Innkaupaáætlun eftir staðsetningu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="116f6-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="116f6-150">Innkaup eftir borg</span><span class="sxs-lookup"><span data-stu-id="116f6-150">Purchase by city</span></span></li>
<li><span data-ttu-id="116f6-151">Vöxtur í innkaupum ár frá ári í %</span><span class="sxs-lookup"><span data-stu-id="116f6-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="116f6-152">Innkaup eftir landi</span><span class="sxs-lookup"><span data-stu-id="116f6-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="116f6-153">Eyðslugreining innkaupa eftir tíma</span><span class="sxs-lookup"><span data-stu-id="116f6-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="116f6-154">Innkaup núverandi árs eftir mánuðum / degi (línurit)</span><span class="sxs-lookup"><span data-stu-id="116f6-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="116f6-155">Innkaup núverandi og síðasta árs (línu- og stöplarit)</span><span class="sxs-lookup"><span data-stu-id="116f6-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="116f6-156">Eyðslugreining innkaupa eftir lánardrottni</span><span class="sxs-lookup"><span data-stu-id="116f6-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="116f6-157">Efstu 10 innkaup lánardrottna % innkaupa (trekt)</span><span class="sxs-lookup"><span data-stu-id="116f6-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="116f6-158">Efstu 10 lánardrottnar með aukna eyðslu ár frá ári</span><span class="sxs-lookup"><span data-stu-id="116f6-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="116f6-159">Efstu 10 lánardrottnar með minnkaða eyðslu ár frá ári</span><span class="sxs-lookup"><span data-stu-id="116f6-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="116f6-160">\*Innkaup þessa árs og síðasta árs og vöxtur eftir innkaupategund</span><span class="sxs-lookup"><span data-stu-id="116f6-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="116f6-161">Stækkun efnis Power BI</span><span class="sxs-lookup"><span data-stu-id="116f6-161">Extending the Power BI content</span></span>
<span data-ttu-id="116f6-162">Með því að nota þjónustupakka sem eru í boði í Microsoft Dynamics Lifecycle Services (LCS) er hægt að veita fólki sem skráir sig ekki inn í Microsoft Dynamics 365 öflugri greiningu.</span><span class="sxs-lookup"><span data-stu-id="116f6-162">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="116f6-163">Hægt er að breyta þessum þjónustupökkum þannig að þeir innihaldi skýrslur eða myndræna framsetningu og afhenda svo leigjanda Power BI.com þjónustupakkana.</span><span class="sxs-lookup"><span data-stu-id="116f6-163">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="116f6-164">Hægt er að finna Power BI efnið **Greining á innkaupaútgjöldum** í safninu Samnýttar eignir í LCS.</span><span class="sxs-lookup"><span data-stu-id="116f6-164">You can find the **Purchase spend analysis** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="116f6-165">Upplýsingar um hvernig á að sækja efnið og innleiða það í fyrirtæki er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="116f6-165">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="116f6-166">Til að sjá sýningarmyndband um hvernig innleiða á Power BI-efnið, sjá [Power BI-efni frá Microsoft og samstarfsaðilum þínum í Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) í Office Mix.</span><span class="sxs-lookup"><span data-stu-id="116f6-166">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

<span data-ttu-id="116f6-167">Gangið úr skugga um að sækja efnið **Greining á innkaupaútgjöldum** sem á við um þá útgáfu Dynamics 365 sem verið er að nota.</span><span class="sxs-lookup"><span data-stu-id="116f6-167">Be sure to download the **Purchase spend analysis** content that applies to the version of Dynamics 365 that you're using.</span></span>

> [!NOTE]
> <span data-ttu-id="116f6-168">Ef þú notar Microsoft Dynamics 365 for Operations útgáfu 1611, er KB 4011327 forsenda fyrir þessu Power BI efni.</span><span class="sxs-lookup"><span data-stu-id="116f6-168">If you're using Microsoft Dynamics 365 for Operations version 1611, KB 4011327 is a prerequisite for this Power BI content.</span></span> <span data-ttu-id="116f6-169">Þegar þú hefur skráð þig inn í LCS hefur þú aðgang að KB á https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span><span class="sxs-lookup"><span data-stu-id="116f6-169">After you sign in to LCS, you can access the KB at https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="116f6-170">Gagnalíkan og einingar</span><span class="sxs-lookup"><span data-stu-id="116f6-170">Data model and entities</span></span>
<span data-ttu-id="116f6-171">Eftirfarandi gögn eru notuð til að fylla út skýrslusíður í Power BI efninu **Greining á innkaupaútgjöldum**.</span><span class="sxs-lookup"><span data-stu-id="116f6-171">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="116f6-172">Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni.</span><span class="sxs-lookup"><span data-stu-id="116f6-172">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="116f6-173">Entity-verslunin er Microsoft SQL-gagnagrunnur sem er fínstilltur fyrir greiningu.</span><span class="sxs-lookup"><span data-stu-id="116f6-173">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="116f6-174">Frekari upplýsingar eru í [Yfirlit yfir samþættingu Power BI við einingaverslun](power-bi-integration-entity-store.md)</span><span class="sxs-lookup"><span data-stu-id="116f6-174">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="116f6-175">Uppsafnaðar mælingar í þessum efnispakka eru undirflokkur uppsafnaðra mælinga sem voru tiltækar í Innkaupateningi í Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="116f6-175">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="116f6-176">Til að stilla uppsafnaðar mælingar tenings í einingaverslun, verður að gera þær virkjanlegir.</span><span class="sxs-lookup"><span data-stu-id="116f6-176">To stage the cube’s aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="116f6-177">Sjá frekari upplýsingar um ferli fyrir millistigsvigtun uppsafnaðra mælinga í einingaverslun í [Yfirlit yfir Power BI samþættingu við einingaverslun](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="116f6-177">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="116f6-178">Eftirfarandi uppsafnaðar lykilmælingar eru tiltækar beint úr reikningslínueiningunni og eru grunnur þessa efnispakka.</span><span class="sxs-lookup"><span data-stu-id="116f6-178">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="116f6-179">Eining</span><span class="sxs-lookup"><span data-stu-id="116f6-179">Entity</span></span>        | <span data-ttu-id="116f6-180">Lykiluppsafnaðar mælingar</span><span class="sxs-lookup"><span data-stu-id="116f6-180">Key aggregate measurements</span></span> | <span data-ttu-id="116f6-181">Uppruni gagna</span><span class="sxs-lookup"><span data-stu-id="116f6-181">Data source</span></span>                                 | <span data-ttu-id="116f6-182">Svæði</span><span class="sxs-lookup"><span data-stu-id="116f6-182">Field</span></span>              | <span data-ttu-id="116f6-183">lýsing</span><span class="sxs-lookup"><span data-stu-id="116f6-183">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="116f6-184">Reikningslínur</span><span class="sxs-lookup"><span data-stu-id="116f6-184">Invoice lines</span></span> | <span data-ttu-id="116f6-185">Innkaup</span><span class="sxs-lookup"><span data-stu-id="116f6-185">Purchase</span></span>                   | <span data-ttu-id="116f6-186">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="116f6-186">VendInvoiceTrans</span></span>                            | <span data-ttu-id="116f6-187">SAMTALA(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="116f6-187">SUM(LineAmountMST)</span></span> | <span data-ttu-id="116f6-188">Upphæðin í bókhaldsgjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="116f6-188">The amount in the accounting currency.</span></span> |

<span data-ttu-id="116f6-189">Eftirfarandi tafla sýnir lykilmælingarnar í efnispakkanum sem eru reiknaðar úr reikningslínueiningunni.</span><span class="sxs-lookup"><span data-stu-id="116f6-189">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="116f6-190">Mæla</span><span class="sxs-lookup"><span data-stu-id="116f6-190">Measure</span></span>               | <span data-ttu-id="116f6-191">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="116f6-191">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="116f6-192">Innkaup núverandi árs</span><span class="sxs-lookup"><span data-stu-id="116f6-192">Purchase current year</span></span> | <span data-ttu-id="116f6-193">Innkaup núverandi árs = SAMTALA ('Reikningslínur'\[Innkaupa\])</span><span class="sxs-lookup"><span data-stu-id="116f6-193">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="116f6-194">Innkaup síðasta árs</span><span class="sxs-lookup"><span data-stu-id="116f6-194">Purchase last year</span></span>    | <span data-ttu-id="116f6-195">Innkaup síðasta ár = REIKNA (SAMTALA ('Reikningslínur'\[Innkaupa\]), SAMEPERIODLASTYEAR (Dagsetningar\[Dagsetning\]))</span><span class="sxs-lookup"><span data-stu-id="116f6-195">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="116f6-196">Vöxtur í innkaupum ár frá ári</span><span class="sxs-lookup"><span data-stu-id="116f6-196">YOY purchase growth</span></span>   | <span data-ttu-id="116f6-197">Vöxtur í innkaupum ár frá ári = \[Innkaupa núverandi árs\] – \[Innkaupa síðasta árs\]</span><span class="sxs-lookup"><span data-stu-id="116f6-197">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="116f6-198">Eftirfarandi lykilvíddir í efnispakkanum eru notaðar sem síur til að sneiða uppsafnaðar mælingar þannig að hægt sé að ná meiri uppskiptingu og öðlast dýpri greiningarinnsýn.</span><span class="sxs-lookup"><span data-stu-id="116f6-198">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="116f6-199">Eining</span><span class="sxs-lookup"><span data-stu-id="116f6-199">Entity</span></span>                 | <span data-ttu-id="116f6-200">Dæmi um eigindir</span><span class="sxs-lookup"><span data-stu-id="116f6-200">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="116f6-201">Lánardrottnar</span><span class="sxs-lookup"><span data-stu-id="116f6-201">Vendors</span></span>                | <span data-ttu-id="116f6-202">Lánardrottnaflokkar, Lánardrottnaland eða -svæði, nafn Lánardrottins</span><span class="sxs-lookup"><span data-stu-id="116f6-202">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="116f6-203">Afurðir</span><span class="sxs-lookup"><span data-stu-id="116f6-203">Products</span></span>               | <span data-ttu-id="116f6-204">Afurðarnúmer, afurðarheiti, heiti vöruflokka</span><span class="sxs-lookup"><span data-stu-id="116f6-204">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="116f6-205">Innkaupaflokkar</span><span class="sxs-lookup"><span data-stu-id="116f6-205">Procurement categories</span></span> | <span data-ttu-id="116f6-206">Innkaupategund, nöfn innkaupategunda</span><span class="sxs-lookup"><span data-stu-id="116f6-206">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="116f6-207">Lögaðilar</span><span class="sxs-lookup"><span data-stu-id="116f6-207">Legal entities</span></span>         | <span data-ttu-id="116f6-208">Heiti lögaðila</span><span class="sxs-lookup"><span data-stu-id="116f6-208">Legal entity name</span></span>                                     |
| <span data-ttu-id="116f6-209">Dagsetningar</span><span class="sxs-lookup"><span data-stu-id="116f6-209">Dates</span></span>                  | <span data-ttu-id="116f6-210">Dagsetningar, Mótbókun árs</span><span class="sxs-lookup"><span data-stu-id="116f6-210">Dates, Year offset</span></span>                                    |

<span data-ttu-id="116f6-211">Sjálfgefið er að efnispakkinn sýni gögn fyrir núgildandi almanaksár.</span><span class="sxs-lookup"><span data-stu-id="116f6-211">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="116f6-212">Hins vegar er hægt að breyta dagsetningasíunni í síuhluta skýrslu.</span><span class="sxs-lookup"><span data-stu-id="116f6-212">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="116f6-213">Einnig er hægt að breyta síu fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="116f6-213">You can also change the company filter.</span></span>

