---
title: "Sjálfgefnir mótlyklar fyrir reikningabók lánardrottins og færslubókarsamþykkt reiknings"
description: "Þetta efnisatriði aðstoðar við að ákveða hvar á að úthluta sjálfgefnum lyklum fyrir reikningabækur."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62093
ms.assetid: 553933ca-928d-4031-bb8c-f9cff458320b
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: bf7af869e44a60d07d66e83bfb55bd0cc7edfb91
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="default-offset-accounts-for-vendor-invoice-journals-and-invoice-approval-journals"></a><span data-ttu-id="c345e-103">Sjálfgefnir mótlyklar fyrir reikningabók lánardrottins og færslubókarsamþykkt reiknings</span><span class="sxs-lookup"><span data-stu-id="c345e-103">Default offset accounts for vendor invoice journals and invoice approval journals</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="c345e-104">Sjálfgefnir mótlyklar eru notaðir á eftirfarandi færslubókarsíðum reiknings lánardrottins:</span><span class="sxs-lookup"><span data-stu-id="c345e-104">Default offset accounts are used on the following vendor invoice journal pages:</span></span>

-   <span data-ttu-id="c345e-105">Reikningabók</span><span class="sxs-lookup"><span data-stu-id="c345e-105">Invoice journal</span></span>
-   <span data-ttu-id="c345e-106">Staðfestingarbók</span><span class="sxs-lookup"><span data-stu-id="c345e-106">Invoice approval journal</span></span>

<span data-ttu-id="c345e-107">Eftirfarandi tafla er notuð til að aðstoða við að ákveða hvar á að úthluta sjálfgefnum lyklum fyrir reikningabækur.</span><span class="sxs-lookup"><span data-stu-id="c345e-107">Use the following table to help decide where you should assign default accounts for invoice journals.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c345e-108">Setja upp sjálfgefna lykla hér</span><span class="sxs-lookup"><span data-stu-id="c345e-108">Set up default accounts here</span></span></th>
<th><span data-ttu-id="c345e-109">Þar sem sjálfgefnir lyklar eru veittir</span><span class="sxs-lookup"><span data-stu-id="c345e-109">Where default accounts are provided</span></span></th>
<th><span data-ttu-id="c345e-110">Hvernig þessi valkostur hefur áhrif á vinnslu</span><span class="sxs-lookup"><span data-stu-id="c345e-110">How this option affects processing</span></span></th>
<th><span data-ttu-id="c345e-111">Hvenær á að nota þennan möguleika</span><span class="sxs-lookup"><span data-stu-id="c345e-111">When you should use this option</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c345e-112"><strong>Lánardrottnaflokkur</strong> – Setja upp sjálfgefna mótlykla fyrir flokka lánardrottna á síðunni <strong>Sjálfgefin lykiluppsetning</strong> sem hægt er að opna af síðunni <strong>Lánardrottnaflokkar</strong>.</span><span class="sxs-lookup"><span data-stu-id="c345e-112"><strong>Vendor group</strong> – Set up default offset accounts for vendor groups on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendor groups</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="c345e-113">Lykill lánardrottins</span><span class="sxs-lookup"><span data-stu-id="c345e-113">Vendor account</span></span></li>
<li><span data-ttu-id="c345e-114">Færslubókarfærslur fyrir lánardrottnareikninga í lánardrottnahópnum, ef sjálfgefnir reikningar eru ekki tilgreindir fyrir lánardrottnareikninga</span><span class="sxs-lookup"><span data-stu-id="c345e-114">Journal entries for vendor accounts in the vendor group, if default accounts aren’t specified for vendor accounts</span></span></li>
</ul></td>
<td><span data-ttu-id="c345e-115">Sjálfgefnir mótlyklar fyrir flokka lánardrottna eru sýndir sem sjálfgefnir mótlyklar fyrir lánardrottna á síðunni <strong>Sjálfgefin lykiluppsetning</strong>.</span><span class="sxs-lookup"><span data-stu-id="c345e-115">The default offset accounts for vendor groups are shown as default offset accounts for vendors on the <strong>Default account setup</strong> page.</span></span> <span data-ttu-id="c345e-116">Hægt er að opna þessa síðu af listasíðunni <strong>Allir lánardrottnar</strong>.</span><span class="sxs-lookup"><span data-stu-id="c345e-116">You can open this page from the <strong>All vendors</strong> list page.</span></span></td>
<td><span data-ttu-id="c345e-117">Notaðu þennan valkost ef yfirleitt er greitt fyrir sömu gerðir af hlutum úr sömu lánardrottnaflokkum með tímanum.</span><span class="sxs-lookup"><span data-stu-id="c345e-117">Use this option if you typically pay for the same types of things from the same vendor groups over time.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c345e-118"><strong>Lánardrottnalykill</strong> – Setja upp sjálfgefna lykla fyrir flokka lánardrottna á síðunni <strong>Sjálfgefin lykiluppsetning</strong> sem hægt er að opna af síðunni <strong>Lánardrottnar</strong>.</span><span class="sxs-lookup"><span data-stu-id="c345e-118"><strong>Vendor account</strong> – Set up default accounts for vendor accounts on the <strong>Default account setup</strong> page, which you can open from the <strong>Vendors</strong> page.</span></span></td>
<td><span data-ttu-id="c345e-119">Færslubókarfærslur fyrir lánardrottnareikning</span><span class="sxs-lookup"><span data-stu-id="c345e-119">Journal entries for the vendor account</span></span></td>
<td><span data-ttu-id="c345e-120">Sjálfgefnir mótlyklar fyrir lykla lánardrottna eru sýndir sem sjálfgefnir mótlyklar fyrir bókarfærslur fyrir lánardrottnalykilinn.</span><span class="sxs-lookup"><span data-stu-id="c345e-120">The default offset accounts for vendor accounts are shown as default offset accounts for journal entries for the vendor account.</span></span></td>
<td><span data-ttu-id="c345e-121">Notaðu þennan valkost ef yfirleitt er greitt fyrir sömu gerðir af hlutum frá sömu lánardrottnum með tímanum.</span><span class="sxs-lookup"><span data-stu-id="c345e-121">Use this option if you typically pay for the same types of things from the same vendors over time.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c345e-122"><strong>Færslubókaheiti</strong> – Setja upp sjálfgefna mótlykla fyrir færslubækur á síðunni <strong>Færslubókarheiti</strong>.</span><span class="sxs-lookup"><span data-stu-id="c345e-122"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="c345e-123">Velja skal valkostinn <strong>Fastur mótlykill</strong>.</span><span class="sxs-lookup"><span data-stu-id="c345e-123">Select the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="c345e-124">Athugaðu að ekki er hægt að tilgreina sjálfgefna mótlykla á færslubókarheiti ef færslubókargerð þeirra er <strong>Komubók</strong> eða <strong>Samþykki</strong>.</span><span class="sxs-lookup"><span data-stu-id="c345e-124">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="c345e-125">Færslubókarhaus sem notar færslubókarheiti</span><span class="sxs-lookup"><span data-stu-id="c345e-125">Journal header that uses the journal name</span></span></li>
<li><span data-ttu-id="c345e-126">Færslubókarfærslur í tímaritum sem nota færslubókarheiti</span><span class="sxs-lookup"><span data-stu-id="c345e-126">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="c345e-127">Ef valkosturinn <strong>Fastur mótlykill</strong> á síðunni <strong>Færslubókaheiti</strong> er valinn, hnekkir mótlykill fyrir færslubókarheiti sjálfgefnum mótlykli fyrir lánardrottinn eða lánardrottnaflokk.</span><span class="sxs-lookup"><span data-stu-id="c345e-127">If the <strong>Fixed offset account</strong> option on the <strong>Journal names</strong> page is selected, the offset account for the journal name overrides the default offset account for the vendor or vendor group.</span></span></td>
<td><span data-ttu-id="c345e-128">Notið þennan valkost til að setja upp færslubækur fyrir tiltekinn kostnað og kostnað sem er gjaldfærður á tiltekna lykla, án tillits til lánardrottins eða lánardrottnaflokks sem lánardrottinn tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="c345e-128">Use this option to set up journals for specific costs and expenses that are charged to specific accounts, regardless of the vendor or the vendor group that the vendor belongs to.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c345e-129"><strong>Færslubókaheiti</strong> – Setja upp sjálfgefna mótlykla fyrir færslubækur á síðunni <strong>Færslubókarheiti</strong>.</span><span class="sxs-lookup"><span data-stu-id="c345e-129"><strong>Journal names</strong> – Set up default offset accounts for journals on the <strong>Journal names</strong> page.</span></span> <span data-ttu-id="c345e-130">Hreinsaðu valkostinn <strong>Fastur mótlykill</strong>.</span><span class="sxs-lookup"><span data-stu-id="c345e-130">Clear the <strong>Fixed offset account</strong> option.</span></span> <span data-ttu-id="c345e-131">Athugaðu að ekki er hægt að tilgreina sjálfgefna mótlykla á færslubókarheiti ef færslubókargerð þeirra er <strong>Komubók</strong> eða <strong>Samþykki</strong>.</span><span class="sxs-lookup"><span data-stu-id="c345e-131">Note that you can't specify default offset accounts on journal names if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><ul>
<li><span data-ttu-id="c345e-132">Færslubókarhaus</span><span class="sxs-lookup"><span data-stu-id="c345e-132">Journal header</span></span></li>
<li><span data-ttu-id="c345e-133">Færslubókarfærslur í tímaritum sem nota færslubókarheiti</span><span class="sxs-lookup"><span data-stu-id="c345e-133">Journal entries in journals that use the journal name</span></span></li>
</ul></td>
<td><span data-ttu-id="c345e-134">Þessar sjálfgefnu færslur eru notaðar í færsluhaus á síðum og mótlykill í haus færslubókarsíðu er notaður sem sjálfgefin færsla í fylgiskjali færslubókarsíðna.</span><span class="sxs-lookup"><span data-stu-id="c345e-134">These default entries are used on journal header pages, and the offset account on the journal header page is used as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="c345e-135">Sjálfgefnir lyklar af síðunni <strong>Færslubókaheiti </strong>eru aðeins notaðir ef sjálfgefnir lyklar ekki eru uppsettir fyrir lykil lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="c345e-135">Default accounts from the <strong>Journal names </strong>page are used only if default accounts aren’t set up for the vendor account.</span></span></td>
<td><span data-ttu-id="c345e-136">Notið þennan valkost til að setja upp sjálfgefna lykla sem eru notaðir þegar sjálfgefnum mótlykli lánardrottins er ekki úthlutað.</span><span class="sxs-lookup"><span data-stu-id="c345e-136">Use this option to set up default accounts that are used when a default vendor offset account isn't assigned.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c345e-137"><strong>Færslubókarhaus</strong> – Setja upp sjálfgefinn mótlykil fyrir færslubókina sem á að nota sem sjálfgefna færslu í fylgiskjali færslubókarsíðna.</span><span class="sxs-lookup"><span data-stu-id="c345e-137"><strong>Journal header</strong> – Set up a default offset account for a journal as a default entry on the journal voucher pages.</span></span> <span data-ttu-id="c345e-138">Athugaðu að ekki er hægt að tilgreina sjálfgefna mótlykla á færslubókarhaus ef færslubókargerð þeirra er <strong>Komubók</strong> eða <strong>Samþykki</strong>.</span><span class="sxs-lookup"><span data-stu-id="c345e-138">Note that you can't specify default offset accounts on the journal header if the journal type of the journal names is <strong>Invoice register</strong> or <strong>Approval</strong>.</span></span></td>
<td><span data-ttu-id="c345e-139">Færslubókar færslur í færslubók</span><span class="sxs-lookup"><span data-stu-id="c345e-139">Journal entries in the journal</span></span></td>
<td><span data-ttu-id="c345e-140">Sjálfgefinn mótlykill í færslubók er notaður sem sjálfgefin færsla á síðum fylgiskjals færslubókar.</span><span class="sxs-lookup"><span data-stu-id="c345e-140">The default offset account for a journal is used as the default entry on the journal voucher pages.</span></span></td>
<td><span data-ttu-id="c345e-141">Notið þennan valkost til að hraða gagnainnfærslu ef flestar færslur í færslubók eru með sama mótlykilinn.</span><span class="sxs-lookup"><span data-stu-id="c345e-141">Use this option to help speed up data entry if most entries in a journal have the same offset account.</span></span></td>
</tr>
</tbody>
</table>






