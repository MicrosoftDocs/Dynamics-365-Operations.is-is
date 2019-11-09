---
title: Sölu- og arðsemisframmistaða Power BI efni
description: Þetta efnisatriði lýsir því sem er innifalið í Sölu- og arðsemisframmistaða Power BI efni. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnið.
author: ShylaThompson
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SalesProfitabilityPerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e74edfc5cf17499c080e825cf4b1fd39b6063e35
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182762"
---
# <a name="sales-and-profitability-performance-power-bi-content"></a><span data-ttu-id="41a56-104">Sölu- og arðsemisframmistaða Power BI efni</span><span class="sxs-lookup"><span data-stu-id="41a56-104">Sales and profitability performance Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41a56-105">Þetta efnisatriði lýsir því hvað er innifalið í **Sölu- og arðsemisframmistöðu** Microsoft Power BI efnis.</span><span class="sxs-lookup"><span data-stu-id="41a56-105">This topic describes what is included in the **Sales and profitability performance** Microsoft Power BI content.</span></span> <span data-ttu-id="41a56-106">Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnið.</span><span class="sxs-lookup"><span data-stu-id="41a56-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="41a56-107">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="41a56-107">Overview</span></span>

<span data-ttu-id="41a56-108">**Sölu- og arðsemisframmistaða** Power BI efnið var stofnað fyrir sölustjórnendur til að fylgjast með lykilmælikvörðum sölu yfir tekjur, brúttóhagnaði og hagnaðarhlutföllum.</span><span class="sxs-lookup"><span data-stu-id="41a56-108">The **Sales and profitability performance** Power BI content was created so that sales managers can monitor the key sales metrics of revenue, gross profit, and profit margins.</span></span> <span data-ttu-id="41a56-109">Hann notar færslugögn sölu og veitir bæði samanlagt yfirlit yfir sölutölur fyrirtækisins og sundurliðun söluafkomu fyrir viðskiptavini og afurðir.</span><span class="sxs-lookup"><span data-stu-id="41a56-109">It uses sales transactional data, and provides both an aggregate view of the company-wide sales figures and a breakdown of sales performance for customers and products.</span></span>

<span data-ttu-id="41a56-110">Skýrslur merkið breytingar á tekjur og hagnað vöxtur tímanum.</span><span class="sxs-lookup"><span data-stu-id="41a56-110">Reports highlight changes in revenue and profit growth over time.</span></span> <span data-ttu-id="41a56-111">Þannig má nota skýrslurnar til að gera stjórnendum viðvart um jákvæða og neikvæða þróun fyrir einstaka viðskiptamenn og afurðir.</span><span class="sxs-lookup"><span data-stu-id="41a56-111">Therefore, the reports can be used to alert managers about positive and negative trends for individual customers and products.</span></span> <span data-ttu-id="41a56-112">Þar að auki gröf bera saman tekjur og arðsemi framleiðslulíkans mismunandi tegundir og þá viðskiptavinaflokka hvor við aðra.</span><span class="sxs-lookup"><span data-stu-id="41a56-112">Additionally, charts compare the revenue and profitability of different product categories and customer groups to each other.</span></span> <span data-ttu-id="41a56-113">Þar af leiðandi tegund og svæðisbundnum stjórnendur geta auðkenna laggards og leaders.</span><span class="sxs-lookup"><span data-stu-id="41a56-113">Therefore, category and regional managers can identify laggards and leaders.</span></span> <span data-ttu-id="41a56-114">Að lokum setur ítarleg skýrsla upp tekjur viðskiptavinar á móti hagnaðarhlutfalli.</span><span class="sxs-lookup"><span data-stu-id="41a56-114">Finally, a comprehensive report plots an individual customer's revenue versus profit margin.</span></span> <span data-ttu-id="41a56-115">Þess vegna hafa yfirmenn reikninga gagnaafritaðan grunn sem þeir geta notað til að fínstilla sölu- og markaðsstarf sitt fyrir hvern viðskiptavin fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="41a56-115">Therefore, account managers have a data-backed foundation that they can use to tune their sales and marketing efforts to each customer's profile.</span></span>

<span data-ttu-id="41a56-116">Efnið **Sölu- og arðsemisafkoma** gerir sölustjórum kleift að greina söluafkomu á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="41a56-116">The **Sales and profitability performance** content lets sales managers analyze sales performance in the following ways:</span></span>

- <span data-ttu-id="41a56-117">Tekjur, á árinu (með viðskiptavinaflokk og einstaka viðskiptavini, sölutegundir, og stakar afurðir og landsvæði)</span><span class="sxs-lookup"><span data-stu-id="41a56-117">Revenue, year-to-date (by customer group and individual customers, sales categories, and individual products and geographies)</span></span>
- <span data-ttu-id="41a56-118">Tekjubreytingar, ár frá ári (eftir svæði viðskiptavina og söluflokkum)</span><span class="sxs-lookup"><span data-stu-id="41a56-118">Revenue change, year-over-year (by customer regions and sales categories)</span></span>

<span data-ttu-id="41a56-119">Hægt er að greina arðsemi á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="41a56-119">Profitability can be analyzed in these ways:</span></span>

- <span data-ttu-id="41a56-120">Brúttóhagnaði og hagnaðarframlegð (með því að flokka viðskiptavina og afurðaflokka sölu)</span><span class="sxs-lookup"><span data-stu-id="41a56-120">Gross profit and profit margin (by customer groups and product sales categories)</span></span>
- <span data-ttu-id="41a56-121">Breyting á brúttóframlegð, ár frá ári</span><span class="sxs-lookup"><span data-stu-id="41a56-121">Gross profit change, year-over-year</span></span>
- <span data-ttu-id="41a56-122">Arðsemi viðskiptavinar (eftir tekjum á móti brúttóframlegð)</span><span class="sxs-lookup"><span data-stu-id="41a56-122">Customer profitability (by revenue versus gross margin)</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="41a56-123">Aðgangur að Power BI efni</span><span class="sxs-lookup"><span data-stu-id="41a56-123">Accessing the Power BI content</span></span>
<span data-ttu-id="41a56-124">**Sölu- og arðsemisframmistaða** Power BI-efni er sýnt á **Sölu- og arðsemisframmistaða** síðunni (**Sölu- og markaðsstarf** \> **Fyrirspurnir og skýrslur** \> **Söluárangur** \> **Sölu- og arðsemisframmistaða**).</span><span class="sxs-lookup"><span data-stu-id="41a56-124">The **Sales and profitability performance** Power BI content is shown on the **Sales and profitability performance** page (**Sales and marketing** \> **Inquiries and reports** \> **Sales performance analysis** \> **Sales and profitability performance**).</span></span>

## <a name="metricsthat-are-included-in-the-power-bi-content"></a><span data-ttu-id="41a56-125">Mælikvarðar sem eru hafðir með í Power BI efni</span><span class="sxs-lookup"><span data-stu-id="41a56-125">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="41a56-126">**Sölu- og arðsemisframmistaða** Power BI efnið inniheldur skýrslu sem samanstendur af safni mælikvarða.</span><span class="sxs-lookup"><span data-stu-id="41a56-126">The **Sales and profitability performance** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="41a56-127">Þessir mælikvarðar eru birtir sem myndrit, reitir og töflur.</span><span class="sxs-lookup"><span data-stu-id="41a56-127">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="41a56-128">Í eftirfarandi töflu er yfirlit yfir myndbirtingar í efninu.</span><span class="sxs-lookup"><span data-stu-id="41a56-128">The following table provides an overview of the visualizations in the content.</span></span>

| <span data-ttu-id="41a56-129">Skýrslusíða</span><span class="sxs-lookup"><span data-stu-id="41a56-129">Report page</span></span>            | <span data-ttu-id="41a56-130">Gröf</span><span class="sxs-lookup"><span data-stu-id="41a56-130">Charts</span></span>                                     | <span data-ttu-id="41a56-131">Reitir</span><span class="sxs-lookup"><span data-stu-id="41a56-131">Tiles</span></span>                                                   |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="41a56-132">Tekjur eftir viðskiptavini</span><span class="sxs-lookup"><span data-stu-id="41a56-132">Revenue by customer</span></span>    | <span data-ttu-id="41a56-133">Efstu tíu viðskiptamenn eftir tekjum</span><span class="sxs-lookup"><span data-stu-id="41a56-133">Top 10 customers by revenue</span></span>                | <span data-ttu-id="41a56-134">Heildartekjur</span><span class="sxs-lookup"><span data-stu-id="41a56-134">Total revenue</span></span>                                           |
|                        | <span data-ttu-id="41a56-135">Heildartekjur eftir viðskiptavinaflokki</span><span class="sxs-lookup"><span data-stu-id="41a56-135">Total revenue by customer group</span></span>            | <span data-ttu-id="41a56-136">Vöxtur í tekjum ár frá ári</span><span class="sxs-lookup"><span data-stu-id="41a56-136">YOY revenue growth</span></span>                                      |
|                        | <span data-ttu-id="41a56-137">Heildartekjur viðskiptavina eftir viðskiptavinaflokki</span><span class="sxs-lookup"><span data-stu-id="41a56-137">Average customer revenue by customer group</span></span> | <span data-ttu-id="41a56-138">Brúttóframlegð</span><span class="sxs-lookup"><span data-stu-id="41a56-138">Gross margin</span></span>                                            |
|                        | <span data-ttu-id="41a56-139">Tekjur & brúttóframlegð eftir viðskiptavinaflokki</span><span class="sxs-lookup"><span data-stu-id="41a56-139">Revenue & gross profit by customer group</span></span>   |                                                         |
| <span data-ttu-id="41a56-140">Tekjur eftir afurðum</span><span class="sxs-lookup"><span data-stu-id="41a56-140">Revenue by product</span></span>     | <span data-ttu-id="41a56-141">Tekjur & brúttóframlegð eftir söluflokki</span><span class="sxs-lookup"><span data-stu-id="41a56-141">Revenue & gross profit by sales category</span></span>   | <span data-ttu-id="41a56-142">Samtala \# aukaafurða</span><span class="sxs-lookup"><span data-stu-id="41a56-142">Total \# of products</span></span>                                    |
|                        | <span data-ttu-id="41a56-143">Efstu tíu afurðir eftir tekjum</span><span class="sxs-lookup"><span data-stu-id="41a56-143">Top 10 products by revenue</span></span>                 | <span data-ttu-id="41a56-144">Heildarfjöldi virkra afurða og prósenta af samtölu</span><span class="sxs-lookup"><span data-stu-id="41a56-144">Total number of active products and percentage of total</span></span> |
|                        | <span data-ttu-id="41a56-145">Heildartekjur eftir söluflokki</span><span class="sxs-lookup"><span data-stu-id="41a56-145">Total revenue by sales category</span></span>            | <span data-ttu-id="41a56-146">Fjöldi afurða fyrir 80% tekna</span><span class="sxs-lookup"><span data-stu-id="41a56-146">Number of products accounting for 80% revenue</span></span>           |
| <span data-ttu-id="41a56-147">Tekjur eftir tímabili\*</span><span class="sxs-lookup"><span data-stu-id="41a56-147">Revenue by period\*</span></span>    | <span data-ttu-id="41a56-148">Tekjur eftir mánuði</span><span class="sxs-lookup"><span data-stu-id="41a56-148">Revenue by month</span></span>                           | <span data-ttu-id="41a56-149">Vöxtur í tekjum ár frá ári</span><span class="sxs-lookup"><span data-stu-id="41a56-149">YOY revenue growth</span></span>                                      |
|                        | <span data-ttu-id="41a56-150">Eftirliggjandi tekjufrávik</span><span class="sxs-lookup"><span data-stu-id="41a56-150">Trailing revenue variance, YOY</span></span>             | <span data-ttu-id="41a56-151">Vöxtur í tekjum ár frá ári %</span><span class="sxs-lookup"><span data-stu-id="41a56-151">YOY revenue growth %</span></span>                                    |
|                        | <span data-ttu-id="41a56-152">Heildarfrávik sölu eftir landsvæði viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="41a56-152">Total sales variance by customer region</span></span>    |                                                         |
| <span data-ttu-id="41a56-153">Tekjur eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="41a56-153">Revenue by location</span></span>    | <span data-ttu-id="41a56-154">Sölutekjur eftir borg</span><span class="sxs-lookup"><span data-stu-id="41a56-154">Sales revenue by city</span></span>                      |                                                         |
|                        | <span data-ttu-id="41a56-155">Vöxtur í tekjum ár frá ári %</span><span class="sxs-lookup"><span data-stu-id="41a56-155">YOY revenue growth %</span></span>                       |                                                         |
|                        | <span data-ttu-id="41a56-156">Sölutekjur eftir svæðum</span><span class="sxs-lookup"><span data-stu-id="41a56-156">Sales revenue by region</span></span>                    |                                                         |
| <span data-ttu-id="41a56-157">Arðsemi viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="41a56-157">Customer profitability</span></span> | <span data-ttu-id="41a56-158">Brúttóframlegð á móti tekjum, viðskiptavinum</span><span class="sxs-lookup"><span data-stu-id="41a56-158">Gross margin versus revenue, by customer</span></span>   | <span data-ttu-id="41a56-159">Brúttóhagnaður, brúttóframlegð, vöxtur í tekjum ár frá ári</span><span class="sxs-lookup"><span data-stu-id="41a56-159">Gross profit, gross margin, YOY revenue growth</span></span>          |
| <span data-ttu-id="41a56-160">Arðsemisgreining</span><span class="sxs-lookup"><span data-stu-id="41a56-160">Profitability analysis</span></span> | <span data-ttu-id="41a56-161">Tekjur og brúttóhagnaður eftir mánuði</span><span class="sxs-lookup"><span data-stu-id="41a56-161">Revenue and gross profit by month</span></span>          |                                                         |
|                        | <span data-ttu-id="41a56-162">Efstu 15 viðskiptamenn eftir brúttóframlegð</span><span class="sxs-lookup"><span data-stu-id="41a56-162">Top 15 customers by gross margin</span></span>           |                                                         |
|                        | <span data-ttu-id="41a56-163">Brúttóhagnaður eftir mánuði, ár frá ári</span><span class="sxs-lookup"><span data-stu-id="41a56-163">Gross profit by month, YOY</span></span>                 |                                                         |

<span data-ttu-id="41a56-164">\* Tekjur þessa árs og síðasta árs og vöxtur eftir söluflokki.</span><span class="sxs-lookup"><span data-stu-id="41a56-164">\* Revenue this and last year, and growth by sales category.</span></span>

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="41a56-165">Skilja gagnalíkan og einingar</span><span class="sxs-lookup"><span data-stu-id="41a56-165">Understanding the data model and entities</span></span>
<span data-ttu-id="41a56-166">Eftirfarandi gögn eru notuð til að fylla út skýrsluna í **Sölu- og arðsemisframmistaða** Power BI efnið.</span><span class="sxs-lookup"><span data-stu-id="41a56-166">The following data is used to fill the report in the **Sales and profitability performance** Power BI content.</span></span> <span data-ttu-id="41a56-167">Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni.</span><span class="sxs-lookup"><span data-stu-id="41a56-167">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="41a56-168">Einingaverslunin er Microsoft SQL Server gagnagrunnur sem er fínstillt fyrir greiningar.</span><span class="sxs-lookup"><span data-stu-id="41a56-168">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="41a56-169">Frekari upplýsingar eru í [Yfirlit yfir samþættingu Power BI við einingaverslun](power-bi-integration-entity-store.md)</span><span class="sxs-lookup"><span data-stu-id="41a56-169">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="41a56-170">Uppsafnaðar mælingar í þessum efnispakka eru undirflokkur uppsafnaðra mælinga sem voru tiltækar í söluteningi í Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="41a56-170">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Sales Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="41a56-171">Til að stilla uppsafnaðar mælingar tenings í einingaverslun verður að gera þær virkjanlegir.</span><span class="sxs-lookup"><span data-stu-id="41a56-171">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="41a56-172">Sjá frekari upplýsingar um ferli fyrir sviðsetningu uppsafnaðra mælinga í verslun Einingar í bloggfærslunni [Power BI-samþætting við einingaverslun í Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) fyrir nánari upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="41a56-172">For more information, see the procedure for staging aggregate measurements in the Entity store in the [Power BI integration with Entity Store in Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blog post.</span></span>

<span data-ttu-id="41a56-173">Eftirfarandi lykiluppsafnaðar mælingar á reikningslínueiningunni eru notaðar sem grunnur að efninu.</span><span class="sxs-lookup"><span data-stu-id="41a56-173">The following key aggregate measurements of the Invoice lines entity are used as the basis of the content.</span></span>

| <span data-ttu-id="41a56-174">Eining</span><span class="sxs-lookup"><span data-stu-id="41a56-174">Entity</span></span>        | <span data-ttu-id="41a56-175">Lykiluppsafnaðar mælingar</span><span class="sxs-lookup"><span data-stu-id="41a56-175">Key aggregate measurements</span></span>                   | <span data-ttu-id="41a56-176">Gagnagjafar fyrir Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="41a56-176">Data source for Dynamics 365</span></span> | <span data-ttu-id="41a56-177">Svæði</span><span class="sxs-lookup"><span data-stu-id="41a56-177">Field</span></span>                                        | <span data-ttu-id="41a56-178">lýsing</span><span class="sxs-lookup"><span data-stu-id="41a56-178">Description</span></span>                                       |
|---------------|----------------------------------------------|------------------------------|----------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="41a56-179">Reikningslínur</span><span class="sxs-lookup"><span data-stu-id="41a56-179">Invoice lines</span></span> | <span data-ttu-id="41a56-180">Tekjur</span><span class="sxs-lookup"><span data-stu-id="41a56-180">Revenue</span></span>                                      | <span data-ttu-id="41a56-181">CustInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="41a56-181">CustInvoiceTrans</span></span>             | <span data-ttu-id="41a56-182">SAMTALA(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="41a56-182">SUM(LineAmountMST)</span></span>                           | <span data-ttu-id="41a56-183">Upphæðin í bókhaldsgjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="41a56-183">The amount in the accounting currency.</span></span>            |
|               | <span data-ttu-id="41a56-184">Kostnaður seldra vara</span><span class="sxs-lookup"><span data-stu-id="41a56-184">Cost of goods sold</span></span>                           | <span data-ttu-id="41a56-185">InventTrans</span><span class="sxs-lookup"><span data-stu-id="41a56-185">InventTrans</span></span>                  | <span data-ttu-id="41a56-186">SAMTALA(CostAmountPosted + CostAmountAdjustment)</span><span class="sxs-lookup"><span data-stu-id="41a56-186">SUM(CostAmountPosted + CostAmountAdjustment)</span></span> | <span data-ttu-id="41a56-187">Samtala kostnaðarupphæð og leiðréttingar.</span><span class="sxs-lookup"><span data-stu-id="41a56-187">The sum of the cost amount and the adjustment.</span></span>    |
|               | <span data-ttu-id="41a56-188">Línuupphæð þóknunar – bókhaldsgjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="41a56-188">Commission line amount – accounting currency</span></span> | <span data-ttu-id="41a56-189">CustInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="41a56-189">CustInvoiceTrans</span></span>             | <span data-ttu-id="41a56-190">SUM(CommissAmountMST)</span><span class="sxs-lookup"><span data-stu-id="41a56-190">SUM(CommissAmountMST)</span></span>                        | <span data-ttu-id="41a56-191">Þóknunarupphæð í bókhaldsgjaldmiðlinum.</span><span class="sxs-lookup"><span data-stu-id="41a56-191">The commission amount in the accounting currency.</span></span> |

<span data-ttu-id="41a56-192">Eftirfarandi tafla sýnir lykiluppsafnaðar mælingar reikningslínueiningarinnar sem eru notaðar til að stofna nokkrar útreikningsmælingar í gagnasafni efnis.</span><span class="sxs-lookup"><span data-stu-id="41a56-192">The following table shows the key aggregate measurements of the Invoice lines entity that are used to create several calculated measures in the content's dataset.</span></span>

| <span data-ttu-id="41a56-193">Mæla</span><span class="sxs-lookup"><span data-stu-id="41a56-193">Measure</span></span>           | <span data-ttu-id="41a56-194">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="41a56-194">Calculation</span></span>                                                                                      |
|-------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41a56-195">Brúttóframlegð</span><span class="sxs-lookup"><span data-stu-id="41a56-195">Gross profit</span></span>      | <span data-ttu-id="41a56-196">SUM(Tekjur – COGS – Þóknun – Virðisaukaskattur (talinn með í línuupphæð viðskiptavinareiknings))</span><span class="sxs-lookup"><span data-stu-id="41a56-196">SUM(Revenue – COGS – Commission – Sales tax (included in customer invoice line amount))</span></span>          |
| <span data-ttu-id="41a56-197">Brúttóframlegð</span><span class="sxs-lookup"><span data-stu-id="41a56-197">Gross margin</span></span>      | <span data-ttu-id="41a56-198">SUM(Brúttóhagnaður/ (Tekjur – Virðisaukaskattur (talinn með í línuupphæð viðskiptavinareiknings)))</span><span class="sxs-lookup"><span data-stu-id="41a56-198">SUM(Gross profit / (Revenue - Sales tax (included in customer invoice line amount)))</span></span>             |
| <span data-ttu-id="41a56-199">Tekjur síðasta árs</span><span class="sxs-lookup"><span data-stu-id="41a56-199">Revenue last year</span></span> | <span data-ttu-id="41a56-200">Tekjur síðasta árs = REIKNA (SAMTALA ('Reikningslínur'\[Tekjur\]), SAMEPERIODLASTYEAR (Dagsetningar\[Dagsetning\]))</span><span class="sxs-lookup"><span data-stu-id="41a56-200">Revenue last year = CALCULATE(SUM('Invoice lines'\[Revenue\]), SAMEPERIODLASTYEAR(Dates\[Date\])</span></span> |

<span data-ttu-id="41a56-201">Eftirfarandi lykilvíddir í söluteningnum eru notaðar sem síur til að sneiða uppsafnaðar mælingar þannig að hægt sé að ná meiri uppskiptingu og öðlast betri innsýn í greiningu.</span><span class="sxs-lookup"><span data-stu-id="41a56-201">The following key dimensions in the Sales Cube are used as filters to slice the aggregate measurements, so that you can achieve greater granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="41a56-202">Eining</span><span class="sxs-lookup"><span data-stu-id="41a56-202">Entity</span></span>           | <span data-ttu-id="41a56-203">Dæmi um eigindir</span><span class="sxs-lookup"><span data-stu-id="41a56-203">Examples of attributes</span></span>                               |
|------------------|------------------------------------------------------|
| <span data-ttu-id="41a56-204">Viðskiptavinir</span><span class="sxs-lookup"><span data-stu-id="41a56-204">Customers</span></span>        | <span data-ttu-id="41a56-205">Viðskiptavinaflokkar, Viðskiptavin svæða, Heimilisfang, Atvinnugrein</span><span class="sxs-lookup"><span data-stu-id="41a56-205">Customer groups, Customer regions, Address, Industry</span></span> |
| <span data-ttu-id="41a56-206">Afurðir</span><span class="sxs-lookup"><span data-stu-id="41a56-206">Products</span></span>         | <span data-ttu-id="41a56-207">Afurðarnúmer, afurðarheiti, heiti vöruflokka</span><span class="sxs-lookup"><span data-stu-id="41a56-207">Product number, Product name, Item groups name</span></span>       |
| <span data-ttu-id="41a56-208">Sölutegundir</span><span class="sxs-lookup"><span data-stu-id="41a56-208">Sales categories</span></span> | <span data-ttu-id="41a56-209">Heiti söluflokka</span><span class="sxs-lookup"><span data-stu-id="41a56-209">Sales category names</span></span>                                 |
| <span data-ttu-id="41a56-210">Lögaðilar</span><span class="sxs-lookup"><span data-stu-id="41a56-210">Legal entities</span></span>   | <span data-ttu-id="41a56-211">Heiti lögaðila</span><span class="sxs-lookup"><span data-stu-id="41a56-211">Legal entity names</span></span>                                   |
| <span data-ttu-id="41a56-212">Dagsetningar</span><span class="sxs-lookup"><span data-stu-id="41a56-212">Dates</span></span>            | <span data-ttu-id="41a56-213">Dagsetningar</span><span class="sxs-lookup"><span data-stu-id="41a56-213">Dates</span></span>                                                |

<span data-ttu-id="41a56-214">Sjálfgefið er að efnispakkinn sýni gögn fyrir núgildandi almanaksár.</span><span class="sxs-lookup"><span data-stu-id="41a56-214">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="41a56-215">Hins vegar er hægt að breyta dagsetningasíunni í síuhluta skýrslu.</span><span class="sxs-lookup"><span data-stu-id="41a56-215">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="41a56-216">Einnig er hægt að breyta síu fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="41a56-216">You can also change the company filter.</span></span>