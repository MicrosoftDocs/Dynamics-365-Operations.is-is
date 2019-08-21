---
title: Skýrsluskilgreiningar í hönnunarviðmót fyrir fjárhagsskýrslur
description: Þessi grein veitir upplýsingar um skýrsluskilgreiningar. Skýrsluskilgreining er skýrsluhlutur (eða eining) sem notast við línuskilgreiningu, dálkskilgreiningu og valfrjálsa skipuritsskilgreiningu til að búa til skýrslu. Skilgreining skýrslu jafnframt veitir valkosti og stillingar fyrir sérsníða skýrslu.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 07f49e63fc2e0410d2673f3ca9378325e9b4ebf8
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2019
ms.locfileid: "1848342"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="b9e6a-105">Skýrsluskilgreiningar í hönnunarviðmót fyrir fjárhagsskýrslur</span><span class="sxs-lookup"><span data-stu-id="b9e6a-105">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9e6a-106">Þessi grein veitir upplýsingar um skýrsluskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-106">This article provides information about report definitions.</span></span> <span data-ttu-id="b9e6a-107">Skýrsluskilgreining er skýrsluhlutur (eða eining) sem notast við línuskilgreiningu, dálkskilgreiningu og valfrjálsa skipuritsskilgreiningu til að búa til skýrslu.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="b9e6a-108">Skilgreining skýrslu jafnframt veitir valkosti og stillingar fyrir sérsníða skýrslu.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-108">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="b9e6a-109">Skýrsluskilgreining er skýrsluhlutur (eða eining) sem notast við línuskilgreiningu, dálkskilgreiningu og valfrjálsa skipuritsskilgreiningu til að búa til skýrslu.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-109">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="b9e6a-110">Skýrsluskilgreining veitir einnig valkosti og stillingar sem hægt er að nota til að sérsníða skýrslu.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-110">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="b9e6a-111">Þegar búið er að skilgreina línuskilgreiningar og dálkaskilgreiningar, verður að sameina þau í skýrsluskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-111">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="b9e6a-112">Á þessum tímapunkti, er einnig skilgreint aðrir þættir skilgreiningar, eins og upplýsingastig og dagsetning skýrslu.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-112">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="b9e6a-113">Svo er hægt að vista og búa til skýrslu.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-113">You can then save and generate a report.</span></span> <span data-ttu-id="b9e6a-114">Fjárhagsskýrslugerð býður upp á eftirfarandi upplýsingastig:</span><span class="sxs-lookup"><span data-stu-id="b9e6a-114">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="b9e6a-115">Fjármál</span><span class="sxs-lookup"><span data-stu-id="b9e6a-115">Financial</span></span>
- <span data-ttu-id="b9e6a-116">Fjárhagur og lykill</span><span class="sxs-lookup"><span data-stu-id="b9e6a-116">Financial and Account</span></span>
- <span data-ttu-id="b9e6a-117">Fjárhagur, lyklar og færslur</span><span class="sxs-lookup"><span data-stu-id="b9e6a-117">Financial, Account, and Transaction</span></span>

<span data-ttu-id="b9e6a-118">Hins vegar eru færsluupplýsingar hugsanlega ekki tiltækar í skýrslum, sem veltur á því hvernig gögn eru geymd í Microsoft Dynamics ERP kerfinu.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-118">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="b9e6a-119">Stofna skýrsluskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="b9e6a-119">Create a report definition</span></span>
1. <span data-ttu-id="b9e6a-120">Á valmyndinni **Skrá** í Skýrsluhönnun er smellt á **Nýtt** og svo er **Skýrsluskilgreining** valin.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-120">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="b9e6a-121">Tilgreinið viðeigandi upplýsingar í **Skýrsla**, **Úttak og dreifing**, **Fyrirsagnir og síðufætur** og **stillingar** flipunum.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-121">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="b9e6a-122">Innihald skýrsluskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="b9e6a-122">Contents of a report definition</span></span>
<span data-ttu-id="b9e6a-123">Eftirfarandi tafla lýsir flipunum í skýrsluskilgreiningu og hvernig upplýsingarnar eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-123">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b9e6a-124">Dálklykill</span><span class="sxs-lookup"><span data-stu-id="b9e6a-124">Tab</span></span></th>
<th><span data-ttu-id="b9e6a-125">Lýsing</span><span class="sxs-lookup"><span data-stu-id="b9e6a-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b9e6a-126">Skýrsla</span><span class="sxs-lookup"><span data-stu-id="b9e6a-126">Report</span></span></td>
<td><span data-ttu-id="b9e6a-127">Stofna skýrslu, grunnstilla skýrslu eða breyta fyrirliggjandi skýrslu.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-127">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b9e6a-128">Frálag og dreifing</span><span class="sxs-lookup"><span data-stu-id="b9e6a-128">Output and Distribution</span></span></td>
<td><span data-ttu-id="b9e6a-129">Breyta úttaksgerð og áfangastað fyrir skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-129">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b9e6a-130">Hausar og fætur</span><span class="sxs-lookup"><span data-stu-id="b9e6a-130">Headers and Footers</span></span></td>
<td><span data-ttu-id="b9e6a-131">Skilgreina og sníða fyrirsagnir og síðufætur fyrir skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-131">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="b9e6a-132">Til dæmis er hægt að bæta texta eða myndum við hausa eða fætur.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-132">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="b9e6a-133">Fjárhagsskýrslugerð styður .bmp, .jpg, og .png myndaskrár.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-133">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="b9e6a-134">Einnig er hægt að bæta við autotext-kóða til að setja inn aðrar upplýsingar, eins og nafn fyrirtækis, skýrsluheiti eða blaðsíðunúmer.</span><span class="sxs-lookup"><span data-stu-id="b9e6a-134">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b9e6a-135">Stillingar</span><span class="sxs-lookup"><span data-stu-id="b9e6a-135">Settings</span></span></td>
<td><span data-ttu-id="b9e6a-136">Tilgreina skýrsluskilgreiningarstillingar, til dæmis eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="b9e6a-136">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="b9e6a-137">Snið og sléttunarupphæðir</span><span class="sxs-lookup"><span data-stu-id="b9e6a-137">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="b9e6a-138">Sníða upplýsingaskýrslur</span><span class="sxs-lookup"><span data-stu-id="b9e6a-138">Format detail reports</span></span></li>
<li><span data-ttu-id="b9e6a-139">Sníða skipurit</span><span class="sxs-lookup"><span data-stu-id="b9e6a-139">Format reporting trees</span></span></li>
<li><span data-ttu-id="b9e6a-140">Mynda undantekningarskýrslu</span><span class="sxs-lookup"><span data-stu-id="b9e6a-140">Generate an exception report</span></span></li>
<li><span data-ttu-id="b9e6a-141">Tilgreina umreikning gjaldmiðils</span><span class="sxs-lookup"><span data-stu-id="b9e6a-141">Specify currency conversion</span></span></li>
<li><span data-ttu-id="b9e6a-142">Upplýsingar um millisamtölu og afmörkun reiknings</span><span class="sxs-lookup"><span data-stu-id="b9e6a-142">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="b9e6a-143">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b9e6a-143">Additional resources</span></span>

[<span data-ttu-id="b9e6a-144">Fjárhagsskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="b9e6a-144">Financial reporting</span></span>](financial-reporting-intro.md)
