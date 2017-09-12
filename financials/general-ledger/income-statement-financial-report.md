---
title: "Fjárhagsskýrsla rekstrarreiknings"
description: "Þessi grein lýsir sjálfgefnum skýrslum fyrir efnahagsreikninga. Hún lýsir einnig einingum sem tengjast þessum skýrslum."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0017d13b7f7594462dfff4ef896f4139607d4bc5
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---

# <a name="income-statement-financial-report"></a><span data-ttu-id="a0094-104">Fjárhagsskýrsla rekstrarreiknings</span><span class="sxs-lookup"><span data-stu-id="a0094-104">Income statement financial report</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a0094-105">Þessi grein lýsir sjálfgefnum skýrslum fyrir efnahagsreikninga.</span><span class="sxs-lookup"><span data-stu-id="a0094-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="a0094-106">Hún lýsir einnig einingum sem tengjast þessum skýrslum.</span><span class="sxs-lookup"><span data-stu-id="a0094-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="a0094-107">Rekstrarreikningsskýrsla sjálfgefin.</span><span class="sxs-lookup"><span data-stu-id="a0094-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="a0094-108">Sjálfgefin skýrsla</span><span class="sxs-lookup"><span data-stu-id="a0094-108">Default report</span></span>             | <span data-ttu-id="a0094-109">Það sem hún gerir</span><span class="sxs-lookup"><span data-stu-id="a0094-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0094-110">Rekstrarreikningur – Sjálfgefin</span><span class="sxs-lookup"><span data-stu-id="a0094-110">Income Statement – Default</span></span> | <span data-ttu-id="a0094-111">Veitir yfirsýn yfir arðsemi fyrirtækisins fyrir gildandi tímabil og einnig það sem af er ári.</span><span class="sxs-lookup"><span data-stu-id="a0094-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="a0094-112">Einingar</span><span class="sxs-lookup"><span data-stu-id="a0094-112">Building blocks</span></span>
<span data-ttu-id="a0094-113">Fjárhagsskýrslur fyrir rekstrarreikning nota eftirfarandi grunneiningar.</span><span class="sxs-lookup"><span data-stu-id="a0094-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="a0094-114">Sjálfgefin skýrsla</span><span class="sxs-lookup"><span data-stu-id="a0094-114">Default report</span></span>             | <span data-ttu-id="a0094-115">Skilgreining línu</span><span class="sxs-lookup"><span data-stu-id="a0094-115">Row definition</span></span>                     | <span data-ttu-id="a0094-116">Skilgreining dálks</span><span class="sxs-lookup"><span data-stu-id="a0094-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="a0094-117">Rekstrarreikningur - sjálfgefinn.</span><span class="sxs-lookup"><span data-stu-id="a0094-117">Income Statement - Default</span></span> | <span data-ttu-id="a0094-118">Samantekt rekstrarreiknings – sjálfgefin.</span><span class="sxs-lookup"><span data-stu-id="a0094-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="a0094-119">Reglubundið og það sem af er ári - sjálfgildi</span><span class="sxs-lookup"><span data-stu-id="a0094-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="a0094-120">Skilgreining línu</span><span class="sxs-lookup"><span data-stu-id="a0094-120">Row definition</span></span>

<span data-ttu-id="a0094-121">Línuskilgreiningin Samantekt rekstrarreiknings – sjálfgefin, inniheldur hluta fyrir hvern hluta venjulegs rekstrarreiknings..</span><span class="sxs-lookup"><span data-stu-id="a0094-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="a0094-122">Víddin Tegund aðallykils°er notuð til að búa til þessa línuskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="a0094-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="a0094-123">Þess vegna getur hver sem er búið til skýrslu án þess að þurfa að gera neinar breytingar.</span><span class="sxs-lookup"><span data-stu-id="a0094-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="a0094-124">Dálkskilgreining.</span><span class="sxs-lookup"><span data-stu-id="a0094-124">Column Definition</span></span>

<span data-ttu-id="a0094-125">Dálkskilgreiningar innihalda mismunandi gerðir dálka til að veita mismunandi stig upplýsinga og fjárhagsgagna.</span><span class="sxs-lookup"><span data-stu-id="a0094-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="a0094-126">**Reglubundið og það sem af er ári – Sjálfgefnar gerðir dálka:**</span><span class="sxs-lookup"><span data-stu-id="a0094-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="a0094-127">**DESC** – Lýsing úr línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="a0094-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="a0094-128">**FD** – fjárhagsgögn fyrir gildandi tímabil</span><span class="sxs-lookup"><span data-stu-id="a0094-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="a0094-129">**FD** – fjárhagsgögn fyrir það sem af er ári</span><span class="sxs-lookup"><span data-stu-id="a0094-129">**FD** – Financial data for the year to date</span></span>

 

<a name="see-also"></a><span data-ttu-id="a0094-130">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="a0094-130">See also</span></span>
--------

[<span data-ttu-id="a0094-131">Fjárhagsskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="a0094-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="a0094-132">Skoðun fjárhagsskýrslna</span><span class="sxs-lookup"><span data-stu-id="a0094-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="a0094-133">Dynamics Financial Reporting-blogg</span><span class="sxs-lookup"><span data-stu-id="a0094-133">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




