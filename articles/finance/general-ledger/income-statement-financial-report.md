---
title: Fjárhagsskýrsla rekstrarreiknings
description: Þessi grein lýsir sjálfgefnum skýrslum fyrir efnahagsreikninga. Hún lýsir einnig einingum sem tengjast þessum skýrslum.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7c5d27d43b287aef87f5ead7f469d5465dd2dcb
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178238"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="3a7e5-104">Fjárhagsskýrsla rekstrarreiknings</span><span class="sxs-lookup"><span data-stu-id="3a7e5-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a7e5-105">Þessi grein lýsir sjálfgefnum skýrslum fyrir efnahagsreikninga.</span><span class="sxs-lookup"><span data-stu-id="3a7e5-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="3a7e5-106">Hún lýsir einnig einingum sem tengjast þessum skýrslum.</span><span class="sxs-lookup"><span data-stu-id="3a7e5-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="3a7e5-107">Rekstrarreikningsskýrsla sjálfgefin.</span><span class="sxs-lookup"><span data-stu-id="3a7e5-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="3a7e5-108">Sjálfgefin skýrsla</span><span class="sxs-lookup"><span data-stu-id="3a7e5-108">Default report</span></span>             | <span data-ttu-id="3a7e5-109">Það sem hún gerir</span><span class="sxs-lookup"><span data-stu-id="3a7e5-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a7e5-110">Rekstrarreikningur – Sjálfgefin</span><span class="sxs-lookup"><span data-stu-id="3a7e5-110">Income Statement – Default</span></span> | <span data-ttu-id="3a7e5-111">Veitir yfirsýn yfir arðsemi fyrirtækisins fyrir gildandi tímabil og einnig það sem af er ári.</span><span class="sxs-lookup"><span data-stu-id="3a7e5-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="3a7e5-112">Einingar</span><span class="sxs-lookup"><span data-stu-id="3a7e5-112">Building blocks</span></span>
<span data-ttu-id="3a7e5-113">Fjárhagsskýrslur fyrir rekstrarreikning nota eftirfarandi grunneiningar.</span><span class="sxs-lookup"><span data-stu-id="3a7e5-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="3a7e5-114">Sjálfgefin skýrsla</span><span class="sxs-lookup"><span data-stu-id="3a7e5-114">Default report</span></span>             | <span data-ttu-id="3a7e5-115">Skilgreining línu</span><span class="sxs-lookup"><span data-stu-id="3a7e5-115">Row definition</span></span>                     | <span data-ttu-id="3a7e5-116">Skilgreining dálks</span><span class="sxs-lookup"><span data-stu-id="3a7e5-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="3a7e5-117">Rekstrarreikningur - sjálfgefinn.</span><span class="sxs-lookup"><span data-stu-id="3a7e5-117">Income Statement - Default</span></span> | <span data-ttu-id="3a7e5-118">Samantekt rekstrarreiknings – sjálfgefin.</span><span class="sxs-lookup"><span data-stu-id="3a7e5-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="3a7e5-119">Reglubundið og það sem af er ári - sjálfgildi</span><span class="sxs-lookup"><span data-stu-id="3a7e5-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="3a7e5-120">Skilgreining línu</span><span class="sxs-lookup"><span data-stu-id="3a7e5-120">Row definition</span></span>

<span data-ttu-id="3a7e5-121">Línuskilgreiningin Samantekt rekstrarreiknings – sjálfgefin, inniheldur hluta fyrir hvern hluta venjulegs rekstrarreiknings..</span><span class="sxs-lookup"><span data-stu-id="3a7e5-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="3a7e5-122">Víddin Tegund aðallykils°er notuð til að búa til þessa línuskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="3a7e5-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="3a7e5-123">Þess vegna getur hver sem er búið til skýrslu án þess að þurfa að gera neinar breytingar.</span><span class="sxs-lookup"><span data-stu-id="3a7e5-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="3a7e5-124">Dálkskilgreining.</span><span class="sxs-lookup"><span data-stu-id="3a7e5-124">Column Definition</span></span>

<span data-ttu-id="3a7e5-125">Dálkskilgreiningar innihalda mismunandi gerðir dálka til að veita mismunandi stig upplýsinga og fjárhagsgagna.</span><span class="sxs-lookup"><span data-stu-id="3a7e5-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="3a7e5-126">**Reglubundið og það sem af er ári – Sjálfgefnar gerðir dálka:**</span><span class="sxs-lookup"><span data-stu-id="3a7e5-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="3a7e5-127">**DESC** – Lýsing úr línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="3a7e5-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="3a7e5-128">**FD** – fjárhagsgögn fyrir gildandi tímabil</span><span class="sxs-lookup"><span data-stu-id="3a7e5-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="3a7e5-129">**FD** – fjárhagsgögn fyrir það sem af er ári</span><span class="sxs-lookup"><span data-stu-id="3a7e5-129">**FD** – Financial data for the year to date</span></span>



<a name="additional-resources"></a><span data-ttu-id="3a7e5-130">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="3a7e5-130">Additional resources</span></span>
--------

[<span data-ttu-id="3a7e5-131">Fjárhagsskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="3a7e5-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="3a7e5-132">Skoðun fjárhagsskýrslna</span><span class="sxs-lookup"><span data-stu-id="3a7e5-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="3a7e5-133">Dynamics Financial Reporting-blogg</span><span class="sxs-lookup"><span data-stu-id="3a7e5-133">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



