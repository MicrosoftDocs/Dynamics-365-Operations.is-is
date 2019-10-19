---
title: Um bókhaldsfærslur dreifingar og undirbókar færslubók fyrir reikningur með frjálsum texta
description: Dreifingar á fjárhagsupphæð eru notaðar til að skilgreina hvernig gert verður grein fyrir upphæð, eins og hvernig gert verður grein fyrir tekjur, skatta eða gjöld á reikningi með frjálsum texta Hver upphæð sem verður að gera grein fyrir þegar reikningur með frjálsum texta er skráður mun hafa eina eða fleiri dreifingar á fjárhagsupphæð.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 515d0a9c35507fad04b776e1f0b6225ac5a162d3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189247"
---
# <a name="accounting-distributions-and-subledger-journal-entries-for-free-text-invoices"></a><span data-ttu-id="634d6-104">Um bókhaldsfærslur dreifingar og undirbókar færslubók fyrir reikningur með frjálsum texta</span><span class="sxs-lookup"><span data-stu-id="634d6-104">Accounting distributions and subledger journal entries for free text invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="634d6-105">Dreifingar á fjárhagsupphæð eru notaðar til að skilgreina hvernig gert verður grein fyrir upphæð, eins og hvernig gert verður grein fyrir tekjur, skatta eða gjöld á reikningi með frjálsum texta</span><span class="sxs-lookup"><span data-stu-id="634d6-105">Accounting distributions are used to define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span> <span data-ttu-id="634d6-106">Hver upphæð sem verður að gera grein fyrir þegar reikningur með frjálsum texta er skráður mun hafa eina eða fleiri dreifingar á fjárhagsupphæð.</span><span class="sxs-lookup"><span data-stu-id="634d6-106">Every amount that must be accounted for when the free text invoice is journalized will have one or more accounting distributions.</span></span>

<a name="accounting-distributions"></a><span data-ttu-id="634d6-107">Dreifing á fjárhagsupphæðum</span><span class="sxs-lookup"><span data-stu-id="634d6-107">Accounting distributions</span></span>
------------------------

<span data-ttu-id="634d6-108">Hægt er að nota eftirfarandi hnappanna í reikningur með frjálsum texta síðunni reikningur lánardrottins til að skoða og mögulega breyta, dreifingar á fjárhagsupphæð síða fyrir hverja upphæð á reikningur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="634d6-108">You can use the following buttons in the Free text invoice page to view, and possibly change, the accounting distributions for each amount on the free text invoice.</span></span>

-   <span data-ttu-id="634d6-109">**Dreifa fjárhæðir**— Skoða og breyta dreifingum á fjárhagsupphæð fyrir einstakar línur og allar undirlínur, svo sem skatta eða gjöld.</span><span class="sxs-lookup"><span data-stu-id="634d6-109">**Distribute amounts**—View and change the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="634d6-110">Einnig er hægt að skoða og breyta dreifingar á fjárhagsupphæð fyrir línu undirstig beint í frá síðunni VSK-færsla eða síðunni Gjaldfærslur.</span><span class="sxs-lookup"><span data-stu-id="634d6-110">You can also view and change the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="634d6-111">Breyta upphæðum í haus reikningur með frjálsum texta, svo sem gjöldum eða sléttuðum gjaldeyrisupphæðum.</span><span class="sxs-lookup"><span data-stu-id="634d6-111">Change free text invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="634d6-112">Breyta upphæðum í reikningi með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="634d6-112">Change free text invoice line amounts.</span></span>
-   <span data-ttu-id="634d6-113">**Skoða dreifingu** - Skoða dreifingu á fjárhagsupphæð fyrir allar línur skjals.</span><span class="sxs-lookup"><span data-stu-id="634d6-113">**View distributions**—View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="634d6-114">Ekki er hægt að breyta dreifingu fjárhagsupphæða í þessu yfirliti.</span><span class="sxs-lookup"><span data-stu-id="634d6-114">You can't change the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="634d6-115">Skoða hausupplýsingar og línuupphæðir.</span><span class="sxs-lookup"><span data-stu-id="634d6-115">View header and line amounts.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="634d6-116">Dreifing upphæða</span><span class="sxs-lookup"><span data-stu-id="634d6-116">Distributing amounts</span></span>
<span data-ttu-id="634d6-117">Þegar reikningur með frjálsum texta verður hverri upphæð dreift á eftirfarandi hátt.</span><span class="sxs-lookup"><span data-stu-id="634d6-117">When you enter a free text invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="634d6-118">Gerð peningaupphæðar</span><span class="sxs-lookup"><span data-stu-id="634d6-118">Type of monetary amount</span></span></th>
<th><span data-ttu-id="634d6-119">Hvaðan aðallykill er birtur</span><span class="sxs-lookup"><span data-stu-id="634d6-119">Where the main account is displayed from</span></span></th>
<th><span data-ttu-id="634d6-120">Forgangsröð sem ákvarðar hvaða fjárhagsvídd sjálfgefna er birt</span><span class="sxs-lookup"><span data-stu-id="634d6-120">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="634d6-121">Lína Reiknings með frjálsum texta</span><span class="sxs-lookup"><span data-stu-id="634d6-121">Free text invoice line</span></span></td>
<td><span data-ttu-id="634d6-122">Fjárhagslykill á reikningur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="634d6-122">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="634d6-123">Ef aðallykils er úthlutunarlykill er að nota sjálfgefna gildið úr skilgreiningu úthlutunar lykil.</span><span class="sxs-lookup"><span data-stu-id="634d6-123">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="634d6-124">Ef aðallykils er ekki úthlutunarlykill, notið sjálfgefin sniðmát fjárhagsvídda á línu í reikningur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="634d6-124">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="634d6-125">Nota sjálfgefin gildi fjárhagsvídda á reikningur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="634d6-125">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="634d6-126">Nota sjálfgefin gildi fjárhagsvídda frá fjárhagslykill í síðu bókhaldslykils.</span><span class="sxs-lookup"><span data-stu-id="634d6-126">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="634d6-127">Lína Reiknings með frjálsum texta fyrir eignarnúmer og samsetningu virðislíkans</span><span class="sxs-lookup"><span data-stu-id="634d6-127">Free text invoice line for a fixed asset number and value model combination</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="634d6-128"><strong>Ábending</strong></span><span class="sxs-lookup"><span data-stu-id="634d6-128"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="634d6-129">Aðallykillinn í línu reiknings með frjálsum texta verður afskráningarlykill eigna.</span><span class="sxs-lookup"><span data-stu-id="634d6-129">The main account on the free text invoice line will be the fixed asset disposal account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
<td><span data-ttu-id="634d6-130">Fjárhagslykill á reikningur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="634d6-130">The ledger account on the free text invoice line.</span></span></td>
<td><ol>
<li><span data-ttu-id="634d6-131">Nota sjálfgefin gildi fjárhagsvídda á reikningur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="634d6-131">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="634d6-132">Nota sjálfgefin gildi fjárhagsvídda frá fjárhagslykill í síðu bókhaldslykils.</span><span class="sxs-lookup"><span data-stu-id="634d6-132">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="634d6-133">Afsláttarupphæð Reiknings með frjálsum texta</span><span class="sxs-lookup"><span data-stu-id="634d6-133">Free text invoice discount amount</span></span></td>
<td><span data-ttu-id="634d6-134">Aðallykill fyrir svæði afsláttar viðskiptavina í síðunni staðgreiðsluafslættir.</span><span class="sxs-lookup"><span data-stu-id="634d6-134">The Main account for customer discounts field in the Cash discounts page.</span></span></td>
<td><ol>
<li><span data-ttu-id="634d6-135">Ef aðallykils er úthlutunarlykill er að nota sjálfgefna gildið úr skilgreiningu úthlutunar lykil.</span><span class="sxs-lookup"><span data-stu-id="634d6-135">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="634d6-136">Ef aðallykils er ekki úthlutunarlykill, notið sjálfgefin sniðmát fjárhagsvídda á línu í reikningur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="634d6-136">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="634d6-137">Nota sjálfgefin gildi fjárhagsvídda á reikningur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="634d6-137">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="634d6-138">Nota sjálfgefin gildi fjárhagsvídda frá fjárhagslykill í síðu bókhaldslykils.</span><span class="sxs-lookup"><span data-stu-id="634d6-138">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="634d6-139">Upphæð virðisaukaskatts á reikningur með frjálsum texta</span><span class="sxs-lookup"><span data-stu-id="634d6-139">Free text invoice sales tax amount</span></span></td>
<td><span data-ttu-id="634d6-140">Reiturinn VSK-til greiðslu í fjárhagsbókunarflokki síðu.</span><span class="sxs-lookup"><span data-stu-id="634d6-140">The Sales tax payable field in the Ledger posting groups page.</span></span></td>
<td><ol>
<li><span data-ttu-id="634d6-141">Nota fjárhagsvíddiir sem eru skilgreindar á upphæð reiknings með frjálsum texta eða dreifingum fyrir upphæð gjaldlínunnar.</span><span class="sxs-lookup"><span data-stu-id="634d6-141">Use the financial dimensions that are defined on the free text invoice line amount or the distributions for the charge line amount.</span></span></li>
<li><span data-ttu-id="634d6-142">Nota sjálfgefin gildi fjárhagsvídda á reikningur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="634d6-142">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="634d6-143">Nota sjálfgefin gildi fjárhagsvídda frá fjárhagslykill í síðu bókhaldslykils.</span><span class="sxs-lookup"><span data-stu-id="634d6-143">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="634d6-144">Upphæð gjaldlínu á reikningur með frjálsum texta</span><span class="sxs-lookup"><span data-stu-id="634d6-144">Free text invoice charge line amount</span></span></td>
<td><span data-ttu-id="634d6-145">Svæði kreditlykils á síðunni Gjaldakóðar.</span><span class="sxs-lookup"><span data-stu-id="634d6-145">The Credit account field in the Charges code page.</span></span></td>
<td><ol>
<li><span data-ttu-id="634d6-146">Ef aðallykils er úthlutunarlykill er að nota sjálfgefna gildið úr skilgreiningu úthlutunar lykil.</span><span class="sxs-lookup"><span data-stu-id="634d6-146">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="634d6-147">Ef aðallykils er ekki úthlutunarlykill, notið sjálfgefin sniðmát fjárhagsvídda á línu í reikningur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="634d6-147">If the main account is not an allocation account, use the financial dimension default template on the free text invoice line.</span></span></li>
<li><span data-ttu-id="634d6-148">Nota sjálfgefin gildi fjárhagsvídda á reikningur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="634d6-148">Use the default financial dimension values on the free text invoice line.</span></span></li>
<li><span data-ttu-id="634d6-149">Nota sjálfgefin gildi fjárhagsvídda frá fjárhagslykill í síðu bókhaldslykils.</span><span class="sxs-lookup"><span data-stu-id="634d6-149">Use the default financial dimension values from the ledger account in the Chart of accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a><span data-ttu-id="634d6-150">Dreifing skatta</span><span class="sxs-lookup"><span data-stu-id="634d6-150">Distributing taxes</span></span>
<span data-ttu-id="634d6-151">Ekki er hægt að stofna dreifingu á fjárhagsupphæð fyrr en skattar hafa verið reiknaðir.</span><span class="sxs-lookup"><span data-stu-id="634d6-151">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="634d6-152">Til að reikna virðisaukaskatt, verður að ljúka einu af eftirtöldum verkefnum í skjámyndinni reikningur með frjálsum texta:</span><span class="sxs-lookup"><span data-stu-id="634d6-152">To calculate sales taxes, you must complete one of the following tasks in the Free text invoice form:</span></span>
-   <span data-ttu-id="634d6-153">Skoða VSK.</span><span class="sxs-lookup"><span data-stu-id="634d6-153">View the sales tax.</span></span>
-   <span data-ttu-id="634d6-154">Skoða samtölu reiknings.</span><span class="sxs-lookup"><span data-stu-id="634d6-154">View the invoice total.</span></span>
-   <span data-ttu-id="634d6-155">Skoða sjóðstreymi.</span><span class="sxs-lookup"><span data-stu-id="634d6-155">View the cash flow.</span></span>
-   <span data-ttu-id="634d6-156">Skoða dreifingu á fjárhagsupphæðum fyrir allan reikning með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="634d6-156">View accounting distributions for the whole free text invoice.</span></span>
-   <span data-ttu-id="634d6-157">Skoða færslubók undirfjárhags.</span><span class="sxs-lookup"><span data-stu-id="634d6-157">View the subledger journal.</span></span>

## <a name="subledger-journals-for-free-text-invoices"></a><span data-ttu-id="634d6-158">Færslubækur undirfjárhags fyrir reikninga með frjálsum texta</span><span class="sxs-lookup"><span data-stu-id="634d6-158">Subledger journals for free text invoices</span></span>
<span data-ttu-id="634d6-159">Áður en þú bóka reikningur með frjálsum texta, er hægt að skoða fulla bókhaldsfærslu, sem felur í sér skuldfærslu og inneignir, til að staðfesta að reikningurinn sé sendur til réttra reikninga.</span><span class="sxs-lookup"><span data-stu-id="634d6-159">Before you post a free text invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="634d6-160">Þetta yfirlit yfir alla lykilfærslu kallast færslubók undirfjárhags.</span><span class="sxs-lookup"><span data-stu-id="634d6-160">This view of the full accounting entry is called a subledger journal.</span></span> <span data-ttu-id="634d6-161">Ef færsla í undirbók er röng þegar hún er forskoðuð áður en reikningur með frjálsum texta eru skráðar, er hægt að breyta færslu í undirbók.</span><span class="sxs-lookup"><span data-stu-id="634d6-161">If the subledger journal entry is incorrect when you preview it before you journalize the free text invoice, you can't change the subledger journal entry.</span></span> <span data-ttu-id="634d6-162">Þess í stað verður þú að breyta dreifingu á fjárhagsupphæð eða bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="634d6-162">Instead, you must change the accounting distributions or the posting profile.</span></span> <span data-ttu-id="634d6-163">Fjárhagsupphæðum er notuð til að skilgreina einni hlið lykilfærslu, debet eða kredit.</span><span class="sxs-lookup"><span data-stu-id="634d6-163">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="634d6-164">Mótfærsla lykilfærslu í undirbókarlykil er stofnuð með því að nota bókunarreglur, eins og úr viðskiptavinalykli eða skatti.</span><span class="sxs-lookup"><span data-stu-id="634d6-164">The offsetting subledger journal account entry is created from the posting profiles, such as from the customer account or the tax.</span></span>



