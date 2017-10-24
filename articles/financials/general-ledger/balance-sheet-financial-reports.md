---
title: "Fjárhagsskýrslur efnahagsreikninga"
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
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6323a2bf40a853edff4b3cef31eea7e95542a92e
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="balance-sheet-financial-reports"></a><span data-ttu-id="d4da2-104">Fjárhagsskýrslur efnahagsreikninga</span><span class="sxs-lookup"><span data-stu-id="d4da2-104">Balance sheet financial reports</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d4da2-105">Þessi grein lýsir sjálfgefnum skýrslum fyrir efnahagsreikninga.</span><span class="sxs-lookup"><span data-stu-id="d4da2-105">This article describes the default reports for balance sheets.</span></span> <span data-ttu-id="d4da2-106">Hún lýsir einnig einingum sem tengjast þessum skýrslum.</span><span class="sxs-lookup"><span data-stu-id="d4da2-106">It also describes the building blocks that are associated with these reports.</span></span> 

<a name="default-balance-sheet-reports"></a><span data-ttu-id="d4da2-107">Sjálfgefnar skýrslur efnahagsreikninga</span><span class="sxs-lookup"><span data-stu-id="d4da2-107">Default balance sheet reports</span></span>
-----------------------------

<span data-ttu-id="d4da2-108">Það eru tvær sjálfgefnar skýrslur efnahagsreikninga.</span><span class="sxs-lookup"><span data-stu-id="d4da2-108">There are two default balance sheet reports.</span></span> <span data-ttu-id="d4da2-109">Í einni skýrslunni er köflunum staflað.</span><span class="sxs-lookup"><span data-stu-id="d4da2-109">On one report, the sections are stacked.</span></span> <span data-ttu-id="d4da2-110">Í hinni skýrslunni eru kaflarnir hlið við hlið.</span><span class="sxs-lookup"><span data-stu-id="d4da2-110">On the other report, the sections are side by side.</span></span>

| <span data-ttu-id="d4da2-111">Sjálfgefin skýrsla</span><span class="sxs-lookup"><span data-stu-id="d4da2-111">Default report</span></span>                       | <span data-ttu-id="d4da2-112">Það sem hún gerir</span><span class="sxs-lookup"><span data-stu-id="d4da2-112">What it does</span></span>                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4da2-113">Efnahagsreikningur - Sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="d4da2-113">Balance Sheet – Default</span></span>              | <span data-ttu-id="d4da2-114">Veitir yfirsýn yfir fjárhagslega stöðu fyrirtækisins fyrir árið.</span><span class="sxs-lookup"><span data-stu-id="d4da2-114">Provides a view of the organization's financial position for the year.</span></span>                                                                 |
| <span data-ttu-id="d4da2-115">Efnahagsreikningur hlið við Hlið – Sjálfgefin</span><span class="sxs-lookup"><span data-stu-id="d4da2-115">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="d4da2-116">Veitir yfirsýn yfir fjárhagslega stöðu fyrirtækisins fyrir árið.</span><span class="sxs-lookup"><span data-stu-id="d4da2-116">Provides a view of the organization's financial position for the year.</span></span> <span data-ttu-id="d4da2-117">Eignir og skuldir og eigið fé hluthafa er hlið við hlið.</span><span class="sxs-lookup"><span data-stu-id="d4da2-117">Assets and liability and shareholder’s equity are side by side.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="d4da2-118">Einingar</span><span class="sxs-lookup"><span data-stu-id="d4da2-118">Building blocks</span></span>
<span data-ttu-id="d4da2-119">Fjárhagsskýrslur efnahagsreikninga nota eftirfarandi grunneiningar.</span><span class="sxs-lookup"><span data-stu-id="d4da2-119">The balance sheet financial reports use the following building blocks.</span></span>

| <span data-ttu-id="d4da2-120">Sjálfgefin skýrsla</span><span class="sxs-lookup"><span data-stu-id="d4da2-120">Default report</span></span>                       | <span data-ttu-id="d4da2-121">Skilgreining línu</span><span class="sxs-lookup"><span data-stu-id="d4da2-121">Row definition</span></span>                       | <span data-ttu-id="d4da2-122">Skilgreining dálks</span><span class="sxs-lookup"><span data-stu-id="d4da2-122">Column definition</span></span>             |
|--------------------------------------|--------------------------------------|-------------------------------|
| <span data-ttu-id="d4da2-123">Efnahagsreikningur - Sjálfgildi</span><span class="sxs-lookup"><span data-stu-id="d4da2-123">Balance Sheet - Default</span></span>              | <span data-ttu-id="d4da2-124">Efnahagsreikningur - Sjálfgildi</span><span class="sxs-lookup"><span data-stu-id="d4da2-124">Balance Sheet - Default</span></span>              | <span data-ttu-id="d4da2-125">YTD og frávik - Sjálfgildi</span><span class="sxs-lookup"><span data-stu-id="d4da2-125">YTD and Variance - Default</span></span>    |
| <span data-ttu-id="d4da2-126">Efnahagsreikningur hlið við Hlið – Sjálfgefin</span><span class="sxs-lookup"><span data-stu-id="d4da2-126">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="d4da2-127">Efnahagsreikningur hlið við Hlið – Sjálfgefin</span><span class="sxs-lookup"><span data-stu-id="d4da2-127">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="d4da2-128">Dálkurinn Það sem af er ári - Sjálfgildi</span><span class="sxs-lookup"><span data-stu-id="d4da2-128">Year to Date Column - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="d4da2-129">Skilgreining línu</span><span class="sxs-lookup"><span data-stu-id="d4da2-129">Row definition</span></span>

<span data-ttu-id="d4da2-130">Línuskilgreiningar fyrir báðar skýrslur efnahagsreikninga innihalda hluta fyrir hvern hluta venjulegs efnahagsreiknings.</span><span class="sxs-lookup"><span data-stu-id="d4da2-130">The row definitions for both balance sheet reports contain sections for each part of a traditional balance sheet.</span></span> <span data-ttu-id="d4da2-131">Hlið við hlið skýrslan inniheldur dálkaskil, þannig að skuld og eigið fé eiganda birtast við eigna.</span><span class="sxs-lookup"><span data-stu-id="d4da2-131">The side-by-side report includes a column break, so that liability and the owner’s equity appear next to assets.</span></span> <span data-ttu-id="d4da2-132">Víddin Tegund aðallykils er notuð til að búa til báðar línuskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="d4da2-132">The Main Account Category dimension is used to build both row definitions.</span></span> <span data-ttu-id="d4da2-133">Þess vegna getur hver sem er myndað skýrslu án þess að þurfa að gera neinar breytingar.</span><span class="sxs-lookup"><span data-stu-id="d4da2-133">Therefore, anyone can generate the reports without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="d4da2-134">Skilgreining dálks</span><span class="sxs-lookup"><span data-stu-id="d4da2-134">Column definition</span></span>

<span data-ttu-id="d4da2-135">Dálkskilgreiningar innihalda mismunandi gerðir dálka til að veita mismunandi stig upplýsinga og fjárhagsgagna.</span><span class="sxs-lookup"><span data-stu-id="d4da2-135">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="d4da2-136">**YTD og frávik - Sjálfgefnar gerðir dálka:**</span><span class="sxs-lookup"><span data-stu-id="d4da2-136">**YTD and Variance – Default column types:**</span></span>
    -   <span data-ttu-id="d4da2-137">**DESC** – Lýsing úr línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="d4da2-137">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="d4da2-138">**FD** – Fjárhagsgögn til dags. fyrir gildandi ár</span><span class="sxs-lookup"><span data-stu-id="d4da2-138">**FD** – Year-to-date financial data for the current year</span></span>
    -   <span data-ttu-id="d4da2-139">**FD** – Fjárhagsgögn til dags. fyrir síðasta ár</span><span class="sxs-lookup"><span data-stu-id="d4da2-139">**FD** – Year-to-date financial data for the last year</span></span>
    -   <span data-ttu-id="d4da2-140">**CALC** – Frávik frá frádregnu síðasta ári frá þessu ári</span><span class="sxs-lookup"><span data-stu-id="d4da2-140">**CALC** – The variance from subtracting last year from this year</span></span>

<!-- -->

-   <span data-ttu-id="d4da2-141">**Dálkurinn Það sem af er ári - Sjálfgildi:**</span><span class="sxs-lookup"><span data-stu-id="d4da2-141">**Year to Date Column – Default:**</span></span>
    -   <span data-ttu-id="d4da2-142">**DESC** – Lýsing úr línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="d4da2-142">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="d4da2-143">**FD** – Fjárhagsgögn til dags. fyrir gildandi ár</span><span class="sxs-lookup"><span data-stu-id="d4da2-143">**FD** – Year-to-date financial data for the current year</span></span>

 

<a name="see-also"></a><span data-ttu-id="d4da2-144">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d4da2-144">See also</span></span>
--------

[<span data-ttu-id="d4da2-145">Fjárhagsskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="d4da2-145">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="d4da2-146">Skoða fjárhagsskýrslur</span><span class="sxs-lookup"><span data-stu-id="d4da2-146">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="d4da2-147">Dynamics Financial Reporting-blogg</span><span class="sxs-lookup"><span data-stu-id="d4da2-147">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




