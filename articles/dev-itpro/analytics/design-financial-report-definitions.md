---
title: "Skýrsluskilgreiningar í hönnunarviðmót fyrir fjárhagsskýrslur"
description: "Þessi grein veitir upplýsingar um skýrsluskilgreiningar. Skýrsluskilgreining er skýrsluhlutur (eða eining) sem notast við línuskilgreiningu, dálkskilgreiningu og valfrjálsa skipuritsskilgreiningu til að búa til skýrslu. Skilgreining skýrslu jafnframt veitir valkosti og stillingar fyrir sérsníða skýrslu."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 96090a3ae15294d98d6207c8eb4a1e58429ca9eb
ms.contentlocale: is-is
ms.lasthandoff: 07/18/2017

---

# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="f6d13-105">Skýrsluskilgreiningar í hönnunarviðmót fyrir fjárhagsskýrslur</span><span class="sxs-lookup"><span data-stu-id="f6d13-105">Report definitions in financial report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f6d13-106">Þessi grein veitir upplýsingar um skýrsluskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="f6d13-106">This article provides information about report definitions.</span></span> <span data-ttu-id="f6d13-107">Skýrsluskilgreining er skýrsluhlutur (eða eining) sem notast við línuskilgreiningu, dálkskilgreiningu og valfrjálsa skipuritsskilgreiningu til að búa til skýrslu.</span><span class="sxs-lookup"><span data-stu-id="f6d13-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="f6d13-108">Skilgreining skýrslu jafnframt veitir valkosti og stillingar fyrir sérsníða skýrslu.</span><span class="sxs-lookup"><span data-stu-id="f6d13-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="f6d13-109">Skýrsluskilgreining er skýrsluhlutur (eða eining) sem notast við línuskilgreiningu, dálkskilgreiningu og valfrjálsa skipuritsskilgreiningu til að búa til skýrslu.</span><span class="sxs-lookup"><span data-stu-id="f6d13-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="f6d13-110">Skýrsluskilgreining veitir einnig valkosti og stillingar sem hægt er að nota til að sérsníða skýrslu.</span><span class="sxs-lookup"><span data-stu-id="f6d13-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="f6d13-111">Þegar búið er að skilgreina línuskilgreiningar og dálkaskilgreiningar, verður að sameina þau í skýrsluskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="f6d13-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="f6d13-112">Á þessum tímapunkti, er einnig skilgreint aðrir þættir skilgreiningar, eins og upplýsingastig og dagsetning skýrslu.</span><span class="sxs-lookup"><span data-stu-id="f6d13-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="f6d13-113">Svo er hægt að vista og búa til skýrslu.</span><span class="sxs-lookup"><span data-stu-id="f6d13-113">You can then save and generate a report.</span></span> <span data-ttu-id="f6d13-114">Fjárhagsskýrslugerð býður upp á eftirfarandi upplýsingastig:</span><span class="sxs-lookup"><span data-stu-id="f6d13-114">Financial reporting offers the following levels of detail:</span></span>

-   <span data-ttu-id="f6d13-115">Fjármál</span><span class="sxs-lookup"><span data-stu-id="f6d13-115">Financial</span></span>
-   <span data-ttu-id="f6d13-116">Fjárhagur og lykill</span><span class="sxs-lookup"><span data-stu-id="f6d13-116">Financial and Account</span></span>
-   <span data-ttu-id="f6d13-117">Fjárhagur, lyklar og færslur</span><span class="sxs-lookup"><span data-stu-id="f6d13-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="f6d13-118">Hins vegar eru færsluupplýsingar hugsanlega ekki tiltækar í skýrslum, sem veltur á því hvernig gögn eru geymd í Microsoft Dynamics ERP kerfinu.</span><span class="sxs-lookup"><span data-stu-id="f6d13-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="f6d13-119">Stofna skýrsluskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="f6d13-119">Create a report definition</span></span>
1.  <span data-ttu-id="f6d13-120">Á valmyndinni **Skrá** í Skýrsluhönnun er smellt á **Nýtt** og svo er **Skýrsluskilgreining** valin.</span><span class="sxs-lookup"><span data-stu-id="f6d13-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2.  <span data-ttu-id="f6d13-121">Tilgreinið viðeigandi upplýsingar í **Skýrsla**, **Úttak og dreifing**, **Fyrirsagnir og síðufætur** og **stillingar** flipunum.</span><span class="sxs-lookup"><span data-stu-id="f6d13-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="f6d13-122">Innihald skýrsluskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="f6d13-122">Contents of a report definition</span></span>
<span data-ttu-id="f6d13-123">Eftirfarandi tafla lýsir flipunum í skýrsluskilgreiningu og hvernig upplýsingarnar eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="f6d13-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f6d13-124">Dálkalykill</span><span class="sxs-lookup"><span data-stu-id="f6d13-124">Tab</span></span></th>
<th><span data-ttu-id="f6d13-125">Lýsing</span><span class="sxs-lookup"><span data-stu-id="f6d13-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f6d13-126">Skýrsla</span><span class="sxs-lookup"><span data-stu-id="f6d13-126">Report</span></span></td>
<td><span data-ttu-id="f6d13-127">Stofna skýrslu, grunnstilla skýrslu eða breyta fyrirliggjandi skýrslu.</span><span class="sxs-lookup"><span data-stu-id="f6d13-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6d13-128">Frálag og dreifing</span><span class="sxs-lookup"><span data-stu-id="f6d13-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="f6d13-129">Breyta úttaksgerð og áfangastað fyrir skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="f6d13-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f6d13-130">Hausar og fætur</span><span class="sxs-lookup"><span data-stu-id="f6d13-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="f6d13-131">Skilgreina og sníða fyrirsagnir og síðufætur fyrir skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="f6d13-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="f6d13-132">Til dæmis er hægt að bæta texta eða myndum við hausa eða fætur.</span><span class="sxs-lookup"><span data-stu-id="f6d13-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="f6d13-133">Fjárhagsskýrslugerð styður .bmp, .jpg, og .png myndaskrár.</span><span class="sxs-lookup"><span data-stu-id="f6d13-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="f6d13-134">Einnig er hægt að bæta við autotext-kóða til að setja inn aðrar upplýsingar, eins og nafn fyrirtækis, skýrsluheiti eða blaðsíðunúmer.</span><span class="sxs-lookup"><span data-stu-id="f6d13-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f6d13-135">Stillingar</span><span class="sxs-lookup"><span data-stu-id="f6d13-135">Settings</span></span></td>
<td><span data-ttu-id="f6d13-136">Tilgreina skýrsluskilgreiningarstillingar, til dæmis eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="f6d13-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="f6d13-137">Snið og sléttunarupphæðir</span><span class="sxs-lookup"><span data-stu-id="f6d13-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="f6d13-138">Sníða upplýsingaskýrslur</span><span class="sxs-lookup"><span data-stu-id="f6d13-138">Format detail reports</span></span></li>
<li><span data-ttu-id="f6d13-139">Sníða skipurit</span><span class="sxs-lookup"><span data-stu-id="f6d13-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="f6d13-140">Mynda undantekningarskýrslu</span><span class="sxs-lookup"><span data-stu-id="f6d13-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="f6d13-141">Tilgreina umreikning gjaldmiðils</span><span class="sxs-lookup"><span data-stu-id="f6d13-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="f6d13-142">Upplýsingar um millisamtölu og afmörkun reiknings</span><span class="sxs-lookup"><span data-stu-id="f6d13-142">Subtotal and filter account details</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="f6d13-143">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="f6d13-143">See also</span></span>
--------

[<span data-ttu-id="f6d13-144">Fjárhagsskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="f6d13-144">Financial reporting</span></span>](financial-reporting-intro.md)




