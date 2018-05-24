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
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 9310508082ff710cd040b74519044f5a90c23988
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="income-statement-financial-report"></a><span data-ttu-id="e675e-104">Fjárhagsskýrsla rekstrarreiknings</span><span class="sxs-lookup"><span data-stu-id="e675e-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e675e-105">Þessi grein lýsir sjálfgefnum skýrslum fyrir efnahagsreikninga.</span><span class="sxs-lookup"><span data-stu-id="e675e-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="e675e-106">Hún lýsir einnig einingum sem tengjast þessum skýrslum.</span><span class="sxs-lookup"><span data-stu-id="e675e-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="e675e-107">Rekstrarreikningsskýrsla sjálfgefin.</span><span class="sxs-lookup"><span data-stu-id="e675e-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="e675e-108">Sjálfgefin skýrsla</span><span class="sxs-lookup"><span data-stu-id="e675e-108">Default report</span></span>             | <span data-ttu-id="e675e-109">Það sem hún gerir</span><span class="sxs-lookup"><span data-stu-id="e675e-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e675e-110">Rekstrarreikningur – Sjálfgefin</span><span class="sxs-lookup"><span data-stu-id="e675e-110">Income Statement – Default</span></span> | <span data-ttu-id="e675e-111">Veitir yfirsýn yfir arðsemi fyrirtækisins fyrir gildandi tímabil og einnig það sem af er ári.</span><span class="sxs-lookup"><span data-stu-id="e675e-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="e675e-112">Einingar</span><span class="sxs-lookup"><span data-stu-id="e675e-112">Building blocks</span></span>
<span data-ttu-id="e675e-113">Fjárhagsskýrslur fyrir rekstrarreikning nota eftirfarandi grunneiningar.</span><span class="sxs-lookup"><span data-stu-id="e675e-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="e675e-114">Sjálfgefin skýrsla</span><span class="sxs-lookup"><span data-stu-id="e675e-114">Default report</span></span>             | <span data-ttu-id="e675e-115">Skilgreining línu</span><span class="sxs-lookup"><span data-stu-id="e675e-115">Row definition</span></span>                     | <span data-ttu-id="e675e-116">Skilgreining dálks</span><span class="sxs-lookup"><span data-stu-id="e675e-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="e675e-117">Rekstrarreikningur - sjálfgefinn.</span><span class="sxs-lookup"><span data-stu-id="e675e-117">Income Statement - Default</span></span> | <span data-ttu-id="e675e-118">Samantekt rekstrarreiknings – sjálfgefin.</span><span class="sxs-lookup"><span data-stu-id="e675e-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="e675e-119">Reglubundið og það sem af er ári - sjálfgildi</span><span class="sxs-lookup"><span data-stu-id="e675e-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="e675e-120">Skilgreining línu</span><span class="sxs-lookup"><span data-stu-id="e675e-120">Row definition</span></span>

<span data-ttu-id="e675e-121">Línuskilgreiningin Samantekt rekstrarreiknings – sjálfgefin, inniheldur hluta fyrir hvern hluta venjulegs rekstrarreiknings..</span><span class="sxs-lookup"><span data-stu-id="e675e-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="e675e-122">Víddin Tegund aðallykils°er notuð til að búa til þessa línuskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="e675e-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="e675e-123">Þess vegna getur hver sem er búið til skýrslu án þess að þurfa að gera neinar breytingar.</span><span class="sxs-lookup"><span data-stu-id="e675e-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="e675e-124">Dálkskilgreining.</span><span class="sxs-lookup"><span data-stu-id="e675e-124">Column Definition</span></span>

<span data-ttu-id="e675e-125">Dálkskilgreiningar innihalda mismunandi gerðir dálka til að veita mismunandi stig upplýsinga og fjárhagsgagna.</span><span class="sxs-lookup"><span data-stu-id="e675e-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="e675e-126">**Reglubundið og það sem af er ári – Sjálfgefnar gerðir dálka:**</span><span class="sxs-lookup"><span data-stu-id="e675e-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="e675e-127">**DESC** – Lýsing úr línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="e675e-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="e675e-128">**FD** – fjárhagsgögn fyrir gildandi tímabil</span><span class="sxs-lookup"><span data-stu-id="e675e-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="e675e-129">**FD** – fjárhagsgögn fyrir það sem af er ári</span><span class="sxs-lookup"><span data-stu-id="e675e-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="e675e-130">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e675e-130">Additional resources</span></span>
--------

[<span data-ttu-id="e675e-131">Fjárhagsskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="e675e-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="e675e-132">Skoðun fjárhagsskýrslna</span><span class="sxs-lookup"><span data-stu-id="e675e-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="e675e-133">Dynamics Financial Reporting-blogg</span><span class="sxs-lookup"><span data-stu-id="e675e-133">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




