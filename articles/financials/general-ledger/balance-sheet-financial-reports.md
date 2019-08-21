---
title: Fjárhagsskýrslur efnahagsreikninga
description: Þessi grein lýsir sjálfgefnum skýrslum fyrir efnahagsreikninga. Hún lýsir einnig einingum sem tengjast þessum skýrslum.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9dcac902118c643b9a9d783c12f02fa5c90827b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839570"
---
# <a name="balance-sheet-financial-reports"></a><span data-ttu-id="28a6e-104">Fjárhagsskýrslur efnahagsreikninga</span><span class="sxs-lookup"><span data-stu-id="28a6e-104">Balance sheet financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28a6e-105">Þessi grein lýsir sjálfgefnum skýrslum fyrir efnahagsreikninga.</span><span class="sxs-lookup"><span data-stu-id="28a6e-105">This article describes the default reports for balance sheets.</span></span> <span data-ttu-id="28a6e-106">Hún lýsir einnig einingum sem tengjast þessum skýrslum.</span><span class="sxs-lookup"><span data-stu-id="28a6e-106">It also describes the building blocks that are associated with these reports.</span></span> 

<a name="default-balance-sheet-reports"></a><span data-ttu-id="28a6e-107">Sjálfgefnar skýrslur efnahagsreikninga</span><span class="sxs-lookup"><span data-stu-id="28a6e-107">Default balance sheet reports</span></span>
-----------------------------

<span data-ttu-id="28a6e-108">Það eru tvær sjálfgefnar skýrslur efnahagsreikninga.</span><span class="sxs-lookup"><span data-stu-id="28a6e-108">There are two default balance sheet reports.</span></span> <span data-ttu-id="28a6e-109">Í einni skýrslunni er köflunum staflað.</span><span class="sxs-lookup"><span data-stu-id="28a6e-109">On one report, the sections are stacked.</span></span> <span data-ttu-id="28a6e-110">Í hinni skýrslunni eru kaflarnir hlið við hlið.</span><span class="sxs-lookup"><span data-stu-id="28a6e-110">On the other report, the sections are side by side.</span></span>

| <span data-ttu-id="28a6e-111">Sjálfgefin skýrsla</span><span class="sxs-lookup"><span data-stu-id="28a6e-111">Default report</span></span>                       | <span data-ttu-id="28a6e-112">Það sem hún gerir</span><span class="sxs-lookup"><span data-stu-id="28a6e-112">What it does</span></span>                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28a6e-113">Efnahagsreikningur - Sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="28a6e-113">Balance Sheet – Default</span></span>              | <span data-ttu-id="28a6e-114">Veitir yfirsýn yfir fjárhagslega stöðu fyrirtækisins fyrir árið.</span><span class="sxs-lookup"><span data-stu-id="28a6e-114">Provides a view of the organization's financial position for the year.</span></span>                                                                 |
| <span data-ttu-id="28a6e-115">Efnahagsreikningur hlið við Hlið – Sjálfgefin</span><span class="sxs-lookup"><span data-stu-id="28a6e-115">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="28a6e-116">Veitir yfirsýn yfir fjárhagslega stöðu fyrirtækisins fyrir árið.</span><span class="sxs-lookup"><span data-stu-id="28a6e-116">Provides a view of the organization's financial position for the year.</span></span> <span data-ttu-id="28a6e-117">Eignir og skuldir og eigið fé hluthafa er hlið við hlið.</span><span class="sxs-lookup"><span data-stu-id="28a6e-117">Assets and liability and shareholder’s equity are side by side.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="28a6e-118">Einingar</span><span class="sxs-lookup"><span data-stu-id="28a6e-118">Building blocks</span></span>
<span data-ttu-id="28a6e-119">Fjárhagsskýrslur efnahagsreikninga nota eftirfarandi grunneiningar.</span><span class="sxs-lookup"><span data-stu-id="28a6e-119">The balance sheet financial reports use the following building blocks.</span></span>

| <span data-ttu-id="28a6e-120">Sjálfgefin skýrsla</span><span class="sxs-lookup"><span data-stu-id="28a6e-120">Default report</span></span>                       | <span data-ttu-id="28a6e-121">Skilgreining línu</span><span class="sxs-lookup"><span data-stu-id="28a6e-121">Row definition</span></span>                       | <span data-ttu-id="28a6e-122">Skilgreining dálks</span><span class="sxs-lookup"><span data-stu-id="28a6e-122">Column definition</span></span>             |
|--------------------------------------|--------------------------------------|-------------------------------|
| <span data-ttu-id="28a6e-123">Efnahagsreikningur - Sjálfgildi</span><span class="sxs-lookup"><span data-stu-id="28a6e-123">Balance Sheet - Default</span></span>              | <span data-ttu-id="28a6e-124">Efnahagsreikningur - Sjálfgildi</span><span class="sxs-lookup"><span data-stu-id="28a6e-124">Balance Sheet - Default</span></span>              | <span data-ttu-id="28a6e-125">YTD og frávik - Sjálfgildi</span><span class="sxs-lookup"><span data-stu-id="28a6e-125">YTD and Variance - Default</span></span>    |
| <span data-ttu-id="28a6e-126">Efnahagsreikningur hlið við Hlið – Sjálfgefin</span><span class="sxs-lookup"><span data-stu-id="28a6e-126">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="28a6e-127">Efnahagsreikningur hlið við Hlið – Sjálfgefin</span><span class="sxs-lookup"><span data-stu-id="28a6e-127">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="28a6e-128">Dálkurinn Það sem af er ári - Sjálfgildi</span><span class="sxs-lookup"><span data-stu-id="28a6e-128">Year to Date Column - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="28a6e-129">Skilgreining línu</span><span class="sxs-lookup"><span data-stu-id="28a6e-129">Row definition</span></span>

<span data-ttu-id="28a6e-130">Línuskilgreiningar fyrir báðar skýrslur efnahagsreikninga innihalda hluta fyrir hvern hluta venjulegs efnahagsreiknings.</span><span class="sxs-lookup"><span data-stu-id="28a6e-130">The row definitions for both balance sheet reports contain sections for each part of a traditional balance sheet.</span></span> <span data-ttu-id="28a6e-131">Hlið við hlið skýrslan inniheldur dálkaskil, þannig að skuld og eigið fé eiganda birtast við eigna.</span><span class="sxs-lookup"><span data-stu-id="28a6e-131">The side-by-side report includes a column break, so that liability and the owner’s equity appear next to assets.</span></span> <span data-ttu-id="28a6e-132">Víddin Tegund aðallykils er notuð til að búa til báðar línuskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="28a6e-132">The Main Account Category dimension is used to build both row definitions.</span></span> <span data-ttu-id="28a6e-133">Þess vegna getur hver sem er myndað skýrslu án þess að þurfa að gera neinar breytingar.</span><span class="sxs-lookup"><span data-stu-id="28a6e-133">Therefore, anyone can generate the reports without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="28a6e-134">Skilgreining dálks</span><span class="sxs-lookup"><span data-stu-id="28a6e-134">Column definition</span></span>

<span data-ttu-id="28a6e-135">Dálkskilgreiningar innihalda mismunandi gerðir dálka til að veita mismunandi stig upplýsinga og fjárhagsgagna.</span><span class="sxs-lookup"><span data-stu-id="28a6e-135">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="28a6e-136">**YTD og frávik - Sjálfgefnar gerðir dálka:**</span><span class="sxs-lookup"><span data-stu-id="28a6e-136">**YTD and Variance – Default column types:**</span></span>
    -   <span data-ttu-id="28a6e-137">**DESC** – Lýsing úr línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="28a6e-137">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="28a6e-138">**FD** – Fjárhagsgögn til dags. fyrir gildandi ár</span><span class="sxs-lookup"><span data-stu-id="28a6e-138">**FD** – Year-to-date financial data for the current year</span></span>
    -   <span data-ttu-id="28a6e-139">**FD** – Fjárhagsgögn til dags. fyrir síðasta ár</span><span class="sxs-lookup"><span data-stu-id="28a6e-139">**FD** – Year-to-date financial data for the last year</span></span>
    -   <span data-ttu-id="28a6e-140">**CALC** – Frávik frá frádregnu síðasta ári frá þessu ári</span><span class="sxs-lookup"><span data-stu-id="28a6e-140">**CALC** – The variance from subtracting last year from this year</span></span>

<!-- -->

-   <span data-ttu-id="28a6e-141">**Dálkurinn Það sem af er ári - Sjálfgildi:**</span><span class="sxs-lookup"><span data-stu-id="28a6e-141">**Year to Date Column – Default:**</span></span>
    -   <span data-ttu-id="28a6e-142">**DESC** – Lýsing úr línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="28a6e-142">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="28a6e-143">**FD** – Fjárhagsgögn til dags. fyrir gildandi ár</span><span class="sxs-lookup"><span data-stu-id="28a6e-143">**FD** – Year-to-date financial data for the current year</span></span>



<a name="additional-resources"></a><span data-ttu-id="28a6e-144">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="28a6e-144">Additional resources</span></span>
--------

[<span data-ttu-id="28a6e-145">Fjárhagsskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="28a6e-145">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="28a6e-146">Skoðun fjárhagsskýrslna</span><span class="sxs-lookup"><span data-stu-id="28a6e-146">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="28a6e-147">Dynamics Financial Reporting-blogg</span><span class="sxs-lookup"><span data-stu-id="28a6e-147">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



