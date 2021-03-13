---
title: Skýrsluskilgreiningar í hönnunarviðmót fyrir fjárhagsskýrslur
description: Þessi grein veitir upplýsingar um skýrsluskilgreiningar.
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
ms.custom: 59131
ms.assetid: 966a3f1d-c59c-4a84-acd4-5bb7e65144c8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 7d5531112cfb803912849af3af785b2a69a79f3d
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093415"
---
# <a name="report-definitions-in-financial-report-designer"></a><span data-ttu-id="aa7a3-103">Skýrsluskilgreiningar í hönnunarviðmót fyrir fjárhagsskýrslur</span><span class="sxs-lookup"><span data-stu-id="aa7a3-103">Report definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa7a3-104">Þessi grein veitir upplýsingar um skýrsluskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="aa7a3-104">This article provides information about report definitions.</span></span> <span data-ttu-id="aa7a3-105">Skýrsluskilgreining er skýrsluhlutur (eða eining) sem notast við línuskilgreiningu, dálkskilgreiningu og valfrjálsa skipuritsskilgreiningu til að búa til skýrslu.</span><span class="sxs-lookup"><span data-stu-id="aa7a3-105">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="aa7a3-106">Skilgreining skýrslu jafnframt veitir valkosti og stillingar fyrir sérsníða skýrslu.</span><span class="sxs-lookup"><span data-stu-id="aa7a3-106">A report definition also provides options and settings that for customizing a report.</span></span> 

<span data-ttu-id="aa7a3-107">Skýrsluskilgreining er skýrsluhlutur (eða eining) sem notast við línuskilgreiningu, dálkskilgreiningu og valfrjálsa skipuritsskilgreiningu til að búa til skýrslu.</span><span class="sxs-lookup"><span data-stu-id="aa7a3-107">A report definition is a report component (or building block) that uses a row definition, a column definition, and an optional reporting tree definition to create a report.</span></span> <span data-ttu-id="aa7a3-108">Skýrsluskilgreining veitir einnig valkosti og stillingar sem hægt er að nota til að sérsníða skýrslu.</span><span class="sxs-lookup"><span data-stu-id="aa7a3-108">A report definition also provides options and settings that you can use to customize a report.</span></span> <span data-ttu-id="aa7a3-109">Þegar búið er að skilgreina línuskilgreiningar og dálkaskilgreiningar, verður að sameina þau í skýrsluskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="aa7a3-109">After you define row definitions and column definitions, you must combine them in a report definition.</span></span> <span data-ttu-id="aa7a3-110">Á þessum tímapunkti, er einnig skilgreint aðrir þættir skilgreiningar, eins og upplýsingastig og dagsetning skýrslu.</span><span class="sxs-lookup"><span data-stu-id="aa7a3-110">At this point, you also define other aspects of the definitions, such as the detail level and report date.</span></span> <span data-ttu-id="aa7a3-111">Svo er hægt að vista og búa til skýrslu.</span><span class="sxs-lookup"><span data-stu-id="aa7a3-111">You can then save and generate a report.</span></span> <span data-ttu-id="aa7a3-112">Fjárhagsskýrslugerð býður upp á eftirfarandi upplýsingastig:</span><span class="sxs-lookup"><span data-stu-id="aa7a3-112">Financial reporting offers the following levels of detail:</span></span>

- <span data-ttu-id="aa7a3-113">Fjármál</span><span class="sxs-lookup"><span data-stu-id="aa7a3-113">Financial</span></span>
- <span data-ttu-id="aa7a3-114">Fjárhagur og lykill</span><span class="sxs-lookup"><span data-stu-id="aa7a3-114">Financial and Account</span></span>
- <span data-ttu-id="aa7a3-115">Fjárhagur, lyklar og færslur</span><span class="sxs-lookup"><span data-stu-id="aa7a3-115">Financial, Account, and Transaction</span></span>

<span data-ttu-id="aa7a3-116">Hins vegar eru færsluupplýsingar hugsanlega ekki tiltækar í skýrslum, sem veltur á því hvernig gögn eru geymd í Microsoft Dynamics ERP kerfinu.</span><span class="sxs-lookup"><span data-stu-id="aa7a3-116">However, depending on how data is stored in the Microsoft Dynamics ERP system, transaction details might not be available in reports.</span></span>

## <a name="create-a-report-definition"></a><span data-ttu-id="aa7a3-117">Stofna skýrsluskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="aa7a3-117">Create a report definition</span></span>
1. <span data-ttu-id="aa7a3-118">Á valmyndinni **Skrá** í Skýrsluhönnun er smellt á **Nýtt** og svo er **Skýrsluskilgreining** valin.</span><span class="sxs-lookup"><span data-stu-id="aa7a3-118">In Report Designer, on the **File** menu, click **New**, and then select **Report Definition**.</span></span>
2. <span data-ttu-id="aa7a3-119">Tilgreinið viðeigandi upplýsingar í **Skýrsla**, **Úttak og dreifing**, **Fyrirsagnir og síðufætur** og **stillingar** flipunum.</span><span class="sxs-lookup"><span data-stu-id="aa7a3-119">Specify the appropriate information on the **Report**, **Output and Distribution**, **Headers and Footers**, and **Settings** tabs.</span></span>

## <a name="contents-of-a-report-definition"></a><span data-ttu-id="aa7a3-120">Innihald skýrsluskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="aa7a3-120">Contents of a report definition</span></span>
<span data-ttu-id="aa7a3-121">Eftirfarandi tafla lýsir flipunum í skýrsluskilgreiningu og hvernig upplýsingarnar eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="aa7a3-121">The following table describes the tabs in a report definition and how the information is used.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="aa7a3-122">Dálklykill</span><span class="sxs-lookup"><span data-stu-id="aa7a3-122">Tab</span></span></th>
<th><span data-ttu-id="aa7a3-123">Lýsing</span><span class="sxs-lookup"><span data-stu-id="aa7a3-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="aa7a3-124">Skýrsla</span><span class="sxs-lookup"><span data-stu-id="aa7a3-124">Report</span></span></td>
<td><span data-ttu-id="aa7a3-125">Stofna skýrslu, grunnstilla skýrslu eða breyta fyrirliggjandi skýrslu.</span><span class="sxs-lookup"><span data-stu-id="aa7a3-125">Create a report, configure a report, or modify an existing report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa7a3-126">Frálag og dreifing</span><span class="sxs-lookup"><span data-stu-id="aa7a3-126">Output and Distribution</span></span></td>
<td><span data-ttu-id="aa7a3-127">Breyta úttaksgerð og áfangastað fyrir skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="aa7a3-127">Change the output type and destination of the report.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa7a3-128">Hausar og fætur</span><span class="sxs-lookup"><span data-stu-id="aa7a3-128">Headers and Footers</span></span></td>
<td><span data-ttu-id="aa7a3-129">Skilgreina og sníða fyrirsagnir og síðufætur fyrir skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="aa7a3-129">Define and format the headers and footers for the report.</span></span> <span data-ttu-id="aa7a3-130">Til dæmis er hægt að bæta texta eða myndum við hausa eða fætur.</span><span class="sxs-lookup"><span data-stu-id="aa7a3-130">For example, you can add text or images to the header or footer.</span></span> <span data-ttu-id="aa7a3-131">Fjárhagsskýrslugerð styður .bmp, .jpg, og .png myndaskrár.</span><span class="sxs-lookup"><span data-stu-id="aa7a3-131">Financial reporting supports .bmp, .jpg, and .png files for images.</span></span> <span data-ttu-id="aa7a3-132">Einnig er hægt að bæta við autotext-kóða til að setja inn aðrar upplýsingar, eins og nafn fyrirtækis, skýrsluheiti eða blaðsíðunúmer.</span><span class="sxs-lookup"><span data-stu-id="aa7a3-132">You can also add autotext codes to insert other information, such as a company name, report name, or page number.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="aa7a3-133">Stillingar</span><span class="sxs-lookup"><span data-stu-id="aa7a3-133">Settings</span></span></td>
<td><span data-ttu-id="aa7a3-134">Tilgreina skýrsluskilgreiningarstillingar, til dæmis eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="aa7a3-134">Specify report definition settings, such as the following settings:</span></span>
<ul>
<li><span data-ttu-id="aa7a3-135">Snið og sléttunarupphæðir</span><span class="sxs-lookup"><span data-stu-id="aa7a3-135">Formatting and rounding amounts</span></span></li>
<li><span data-ttu-id="aa7a3-136">Sníða upplýsingaskýrslur</span><span class="sxs-lookup"><span data-stu-id="aa7a3-136">Format detail reports</span></span></li>
<li><span data-ttu-id="aa7a3-137">Sníða skipurit</span><span class="sxs-lookup"><span data-stu-id="aa7a3-137">Format reporting trees</span></span></li>
<li><span data-ttu-id="aa7a3-138">Mynda undantekningarskýrslu</span><span class="sxs-lookup"><span data-stu-id="aa7a3-138">Generate an exception report</span></span></li>
<li><span data-ttu-id="aa7a3-139">Tilgreina umreikning gjaldmiðils</span><span class="sxs-lookup"><span data-stu-id="aa7a3-139">Specify currency conversion</span></span></li>
<li><span data-ttu-id="aa7a3-140">Upplýsingar um millisamtölu og afmörkun reiknings</span><span class="sxs-lookup"><span data-stu-id="aa7a3-140">Subtotal and filter account details</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="aa7a3-141">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="aa7a3-141">Additional resources</span></span>

[<span data-ttu-id="aa7a3-142">Fjárhagsskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="aa7a3-142">Financial reporting</span></span>](financial-reporting-intro.md)
