---
title: "Stofna reikningur viðskiptavinar."
description: 
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2a668e390935e157d9fc7f0ef597f25c2a7b9950
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="create-a-customer-invoice"></a><span data-ttu-id="fa719-102">Stofna reikningur viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="fa719-102">Create a customer invoice</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="fa719-103">**Reikningur viðskiptavinar fyrir sölupöntun** er reikningur sem tengist sölunni og sem fyrirtæki gefur viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="fa719-103">A **customer invoice for a sales order** is a bill that is related to a sale, and that an organization gives to a customer.</span></span> <span data-ttu-id="fa719-104">Þessi gerð reikningur viðskiptavinar er stofnaður á grundvelli sölupöntunar, sem felur í sér pöntunarlínur og vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="fa719-104">This type of customer invoice is created based on a sales order, which includes order lines and item numbers.</span></span> <span data-ttu-id="fa719-105">Vörunúmer eru tilgreind og bókuð í fjárhaginn.</span><span class="sxs-lookup"><span data-stu-id="fa719-105">Item numbers are specified and posted in the ledger.</span></span> <span data-ttu-id="fa719-106">Færslur undirbókar eru ekki tiltæk fyrir reikning viðskiptavinar fyrir sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="fa719-106">Subledger journal entries aren't available for a customer invoice for a sales order.</span></span> <span data-ttu-id="fa719-107">Frekari upplýsingar má sjá í [Stofna sölupöntunarreikninga](tasks/create-sales-order-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="fa719-107">For more information, see [Create sales order invoices](tasks/create-sales-order-invoices.md).</span></span>

<span data-ttu-id="fa719-108">**Reikningur með frjálsum texta** er ekki tengdur sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="fa719-108">A **free text invoice** isn't related to a sales order.</span></span> <span data-ttu-id="fa719-109">Hann inniheldur pöntunarlínur sem fela í sér fjárhagslykla, frjálsar textalýsingar, og söluupphæð sem maður færir inn sjálfur.</span><span class="sxs-lookup"><span data-stu-id="fa719-109">It contains order lines that include ledger accounts, free-text descriptions, and a sales amount that you enter.</span></span> <span data-ttu-id="fa719-110">Ekki er hægt að færa inn vörunúmer á þessa gerð reiknings.</span><span class="sxs-lookup"><span data-stu-id="fa719-110">You can't enter an item number on this kind of invoice.</span></span> <span data-ttu-id="fa719-111">Skylda er að færa inn viðeigandi VSK-upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="fa719-111">You must enter the appropriate sales tax information.</span></span> <span data-ttu-id="fa719-112">Aðallykill fyrir söluna tilgreindur á hverri reikningslínu sem hægt er að dreifa á mörgum fjárhagslykla með því að smella **Dreifingarupphæðir** á síðunni **reikningur með frjálsum texta**.</span><span class="sxs-lookup"><span data-stu-id="fa719-112">A main account for the sale is indicated on each invoice line, which you can distribute to multiple ledger accounts by clicking **Distribute amounts** on the **Free text invoice** page.</span></span> <span data-ttu-id="fa719-113">Þar að auki er staða viðskiptavinarins bókuð í safnlykil úr bókunarregla sem notuð er fyrir reikningur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="fa719-113">Additionally, the customer balance is posted to the summary account from the posting profile that is used for the free text invoice.</span></span>

<span data-ttu-id="fa719-114">Frekari upplýsingar er að finna á: </span><span class="sxs-lookup"><span data-stu-id="fa719-114">For more information see:</span></span>

[<span data-ttu-id="fa719-115">Stofna reikning með frjálsum texta</span><span class="sxs-lookup"><span data-stu-id="fa719-115">Create a free text invoice</span></span>](tasks/create-free-text-invoice.md)

[<span data-ttu-id="fa719-116">Stofna sniðmát með frjálsum texta</span><span class="sxs-lookup"><span data-stu-id="fa719-116">Create a free text template</span></span>](tasks/create-free-text-invoice-template.md)

[<span data-ttu-id="fa719-117">Úthluta sniðmáti reiknings með frjálsum texta á viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="fa719-117">Assign a free text invoice tempate to a customer</span></span>](tasks/assign-free-text-invoice-template-customer.md)

[<span data-ttu-id="fa719-118">Mynda og bóka endurtekna reikninga með frjálsum texta</span><span class="sxs-lookup"><span data-stu-id="fa719-118">Generate and post recurring free text invoices</span></span>](tasks/post-recurring-free-text-invoices.md)


<span data-ttu-id="fa719-119">**Bráðabirgðareikningur** er reikningur sem er útbúinn sem mat á raunverulegu reikningsupphæðinni áður en reikningurinn er bókaður.</span><span class="sxs-lookup"><span data-stu-id="fa719-119">A **pro forma invoice** is an invoice that is prepared as an estimate of the actual invoice amounts before the invoice is posted.</span></span> <span data-ttu-id="fa719-120">Hægt er að prenta út bráðabirgðareikning fyrir annað hvort sölureikning eða reikningur með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="fa719-120">You can print a pro forma invoice either for a customer invoice for a sales order or for a free text invoice.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a><span data-ttu-id="fa719-121">Bóka og prenta einstaka reikningur viðskiptavinar sem byggðir eru á sölupöntunum</span><span class="sxs-lookup"><span data-stu-id="fa719-121">Post and print individual customer invoices that are based on sales orders</span></span>
<span data-ttu-id="fa719-122">Notið þetta ferli til að stofna reikning sem byggist á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="fa719-122">Use this process to create an invoice that is based on a sales order.</span></span> <span data-ttu-id="fa719-123">Hægt er að gera þetta ef ákveðið er að reikningsfæra viðskiptamann áður en vörurnar eða þjónustan eru afhent.</span><span class="sxs-lookup"><span data-stu-id="fa719-123">You might do this if you decide to invoice the customer before you deliver the goods or services.</span></span> 

<span data-ttu-id="fa719-124">Þegar reikningur er bókaður er magn **reikningsafgangs** fyrir hverja vöru uppfært með samtölu reikningsfærðs magns úr völdum sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="fa719-124">When you post an invoice, the **Invoice remainder** quantity for each item is updated with the total of the invoiced quantities from the selected sales order.</span></span> <span data-ttu-id="fa719-125">Ef bæði magnið **Reikningsafgangur** og magnið **Eftirstöðvar afhendingar** fyrir allar og vörur á sölupöntuninni jafngildir 0 (núlli), breytist staða sölupöntunarinnar í **Reikningsfært**.</span><span class="sxs-lookup"><span data-stu-id="fa719-125">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="fa719-126">Ef magn **reikningsafgangs** er ekki núll (0), er staða innkaupapöntunarinnar óbreytt og hægt er að færa inn viðbótarreikninga fyrir hann.</span><span class="sxs-lookup"><span data-stu-id="fa719-126">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="fa719-127">Á listasíðunni **Allar sölupantanir** er hægt að skoða stöðu sölupantana.</span><span class="sxs-lookup"><span data-stu-id="fa719-127">You can view the status of the sales orders on the **All sales orders** list page.</span></span> <span data-ttu-id="fa719-128">Nota **Opnir reikningar viðskiptavina** listasíður til að skoða reikningana sem bókaðir voru.</span><span class="sxs-lookup"><span data-stu-id="fa719-128">Use the **Open customer invoices** list page to view the invoices that you posted.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a><span data-ttu-id="fa719-129">Bóka og prenta einstaka reikningur viðskiptavinar sem byggðir eru á fylgiseðlum og dagsetningunni.</span><span class="sxs-lookup"><span data-stu-id="fa719-129">Post and print individual customer invoices that are based on packing slips and the date</span></span>
<span data-ttu-id="fa719-130">Notaðu þessa aðferð þegar einn eða fleiri fylgiseðlar hafa verið bókaðir fyrir sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="fa719-130">Use this process when one or more packing slips have been posted for the sales order.</span></span> <span data-ttu-id="fa719-131">Reikningur viðskiptamanns er byggður á viðkomandi fylgiseðlum og endurspeglar magnið á þeim.</span><span class="sxs-lookup"><span data-stu-id="fa719-131">The customer invoice is based on these packing slips and reflects the quantities from them.</span></span> <span data-ttu-id="fa719-132">Fjárhagslegar upplýsingar sem koma fram á reikningnum eru byggðar á upplýsingunum sem færðar eru inn þegar reikningurinn er bókaður.</span><span class="sxs-lookup"><span data-stu-id="fa719-132">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span> 

<span data-ttu-id="fa719-133">Hægt er að stofna reikningur viðskiptavinar út frá línuvörum fylgiseðils sem sendar hafa verið fram að þessu, jafnvel þótt allar vörur tiltekinnar sölupöntunar hafi ekki verið sendar ennþá.</span><span class="sxs-lookup"><span data-stu-id="fa719-133">You can create a customer invoice that is based on the packing slip line items that have been shipped to date, even if all the items for a particular sales order haven't yet been shipped.</span></span> <span data-ttu-id="fa719-134">Þetta gæti til dæmis átt við, ef fyrirtækið gefur út einn reikning fyrir viðskiptavin mánaðarlega sem nær yfir allar afhendingar sem sendar eru þann mánuð.</span><span class="sxs-lookup"><span data-stu-id="fa719-134">You might do this if, for example, your legal entity issues one invoice per customer per month that covers all the deliveries that you ship during that month.</span></span> <span data-ttu-id="fa719-135">Hver fylgiseðill stendur fyrir hlutaafhendingu eða fulla afhendingu á vörum í sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="fa719-135">Each packing slip represents a partial or complete delivery of the items on the sales order.</span></span> 

<span data-ttu-id="fa719-136">Þegar reikningur er bókaður er magn **reikningsafgangs** fyrir hverja vöru uppfært með samtölu afhents magns úr völdum fylgiseðlum.</span><span class="sxs-lookup"><span data-stu-id="fa719-136">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the delivered quantities from the selected packing slips.</span></span> <span data-ttu-id="fa719-137">Ef bæði **Reikningsafgangur** magnið og **Eftirstöðvar afendingar** magnið fyrir allar vörur á sölupöntuninni jafngildir núlli (0), breytist staða sölupöntunarinnar í  **Reikningsfært**.</span><span class="sxs-lookup"><span data-stu-id="fa719-137">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="fa719-138">Ef magn **reikningsafgangs** er ekki núll (0), er staða innkaupapöntunarinnar óbreytt og hægt er að færa inn viðbótarreikninga fyrir hann.</span><span class="sxs-lookup"><span data-stu-id="fa719-138">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span> 

<span data-ttu-id="fa719-139">Birgðafærslur eru uppfærðar með reikningsnúmeri og staðan í svæðinu **Staða línu** í sölupöntuninni breytist í **Reikningsfært**.</span><span class="sxs-lookup"><span data-stu-id="fa719-139">Inventory transactions are updated with the invoice number, and the status in the **Line status** field on the sales order is changed to **Invoiced**.</span></span> 

<span data-ttu-id="fa719-140">Á listasíðunni **Allar sölupantanir** er hægt að skoða stöðu sölupantana.</span><span class="sxs-lookup"><span data-stu-id="fa719-140">View the status of the sales orders in the **All sales orders** list page.</span></span>

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a><span data-ttu-id="fa719-141">Sameina sölupantanir eða fylgiseðla við bókun</span><span class="sxs-lookup"><span data-stu-id="fa719-141">Consolidate sales orders or packing slips for posting</span></span>
<span data-ttu-id="fa719-142">Notið þetta ferli þegar ein eða fleiri sölupantanir eru tilbúnar til bókunar og að sameina á þau í einn reikning.</span><span class="sxs-lookup"><span data-stu-id="fa719-142">Use this process when one or more sales orders are ready to be invoiced, and you want to consolidate them into a single invoice.</span></span> 

<span data-ttu-id="fa719-143">Hægt er að velja marga reikninga í á **sölupöntun** listasíða og nota svo **Mynda reikninga** til að sameina þau.</span><span class="sxs-lookup"><span data-stu-id="fa719-143">You can select multiple invoices on the **Sales order** list page and then use **Generate invoices** to consolidate them.</span></span> <span data-ttu-id="fa719-144">Á **Bókun reiknings** síðu er hægt að breyta stillingu fyrir **samantektarröðun** til að draga saman eftir pöntunarnúmeri (þar sem það eru margir fylgiseðlar fyrir eina sölupöntun ) eða eftir reikningslykli (þar sem það eru margar sölupantanir fyrir einn reikningslykil).</span><span class="sxs-lookup"><span data-stu-id="fa719-144">On the **Posting invoice** page, you can change the **Summary order** setting to summarize by order number (where there are multiple packing slips for a single sales order) or by invoice account (where there are multiple sales orders for a single invoice account).</span></span> <span data-ttu-id="fa719-145">Nota skal **Skipulag** hnappinn til að sameina sölupantanir í einn reikninga sem byggjast á í stillingar fyrir **samantektarröðun** .</span><span class="sxs-lookup"><span data-stu-id="fa719-145">Use the **Arrange** button to consolidate sales orders into single invoices, based on the **Summary order** settings.</span></span>

## <a name="additional-settings-that-change-the-posting-behavior"></a><span data-ttu-id="fa719-146">Frekari stillingar sem breyta bókununarhegðun</span><span class="sxs-lookup"><span data-stu-id="fa719-146">Additional settings that change the posting behavior</span></span>
<span data-ttu-id="fa719-147">Eftirfarandi svæði breyta hegðun bókunarferlanna.</span><span class="sxs-lookup"><span data-stu-id="fa719-147">The following fields change the behavior of the posting process.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fa719-148">Reitur</span><span class="sxs-lookup"><span data-stu-id="fa719-148">Field</span></span></th>
<th><span data-ttu-id="fa719-149">Lýsing</span><span class="sxs-lookup"><span data-stu-id="fa719-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fa719-150">Magn</span><span class="sxs-lookup"><span data-stu-id="fa719-150">Quantity</span></span></td>
<td><span data-ttu-id="fa719-151">Velja magnið sem á að byggja bókun skjalsins á.</span><span class="sxs-lookup"><span data-stu-id="fa719-151">Select the quantities to base the posting of the document on.</span></span> <span data-ttu-id="fa719-152">Valkostirnir sem eru tiltækir eru breytilegir, eftir gerð skjals sem verið er að bóka, eins og fylgiseðil eða reikning.</span><span class="sxs-lookup"><span data-stu-id="fa719-152">The options that are available vary, depending on the type of document that you are posting, such as a packing slip or an invoice.</span></span>
<ul>
<li><span data-ttu-id="fa719-153"><strong>Afhenda nú </strong> – Veljið allt magn sem er fært inn í svæðið <strong>Afhenda nú</strong>.</span><span class="sxs-lookup"><span data-stu-id="fa719-153"><strong>Deliver now</strong> – Select all quantities that are entered in the <strong>Deliver now</strong> field.</span></span> <span data-ttu-id="fa719-154">Notaðu þennan valkostur í staðfesta eða afhenda pöntun að hluta til.</span><span class="sxs-lookup"><span data-stu-id="fa719-154">Use this option to confirm or deliver a partial order.</span></span></li>
<li><span data-ttu-id="fa719-155"><strong>Tiltekið</strong> – Velja allt magn sem hafa verið teknar til.</span><span class="sxs-lookup"><span data-stu-id="fa719-155"><strong>Picked</strong> – Select all quantities that have been picked.</span></span></li>
<li><span data-ttu-id="fa719-156"><strong>Allt </strong>- veldu allt magn á sölupöntun sem þú hefur ekki enn uppfært af núverandi gerð skjals</span><span class="sxs-lookup"><span data-stu-id="fa719-156"><strong>All</strong> – Select all quantities on the sales order that haven't yet been updated by the current document type.</span></span></li>
<li><span data-ttu-id="fa719-157"><strong>Fylgiseðill </strong> – Velja allt magn sem hafa verið uppfærðar af fylgiseðli.</span><span class="sxs-lookup"><span data-stu-id="fa719-157"><strong>Packing slip</strong> – Select all quantities that have been updated by a packing slip.</span></span></li>
<li><span data-ttu-id="fa719-158"><strong>Tiltektarmagn og afurðir sem ekki á lager </strong> – Velja allt magn sem hafa verið teknar til og allt magn vöru sem ekki eru í birgðum.</span><span class="sxs-lookup"><span data-stu-id="fa719-158"><strong>Picked quantity and not stocked products</strong> – Select all quantities that have been picked and all product quantities that aren't stocked.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa719-159">Bókun</span><span class="sxs-lookup"><span data-stu-id="fa719-159">Posting</span></span></td>
<td><ul>
<li><span data-ttu-id="fa719-160">Veljið þennan valkost til að skrá sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="fa719-160">Select this option to journalize the sales order.</span></span></li>
<li><span data-ttu-id="fa719-161">Hreinsið þennan valkost til að prenta bráðabirgðaafrit af sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="fa719-161">Clear this option to print a pro forma sales order.</span></span> <span data-ttu-id="fa719-162"><strong>Athugasemd</strong> Ef samningur hefur verið gerður fyrir greiðsluáætlun, mun greiðsluáætlunin ekki verða sýnd á bráðabirgðasölupöntun.</span><span class="sxs-lookup"><span data-stu-id="fa719-162"><strong>Note:</strong> If you made an agreement for a payment schedule, the payment schedule isn't shown on the pro forma sales order.</span></span> <span data-ttu-id="fa719-163">Greiðsluáætlanir verður einungis sýnd á raunverulegu sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="fa719-163">Payment schedules are shown only on actual sales orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa719-164">Valið síðar</span><span class="sxs-lookup"><span data-stu-id="fa719-164">Late selection</span></span></td>
<td><span data-ttu-id="fa719-165">Velja þennan valkost til að nota völdu fyrirspurnina síðar.</span><span class="sxs-lookup"><span data-stu-id="fa719-165">Select this option to apply the selected query later.</span></span> <span data-ttu-id="fa719-166">Þessi valkostur er notaður fyrir runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="fa719-166">This option is used for batch jobs.</span></span> <span data-ttu-id="fa719-167">Fyrirspurnin er keyrð þegar runuvinnsla er keyrð.</span><span class="sxs-lookup"><span data-stu-id="fa719-167">The query is run when the batch job is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa719-168">Minnka magn</span><span class="sxs-lookup"><span data-stu-id="fa719-168">Reduce quantity</span></span></td>
<td><span data-ttu-id="fa719-169">Veljið þennan valkost til að minnka sjálfvirkt afhent magn þegar skjalið er bókuð, þannig að afhent magn jafngildi tiltækar birgðir.</span><span class="sxs-lookup"><span data-stu-id="fa719-169">Select this option to automatically reduce the delivered quantity when the document is posted, so that the delivered quantity equals the available inventory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa719-170">Prenta</span><span class="sxs-lookup"><span data-stu-id="fa719-170">Print</span></span></td>
<td><span data-ttu-id="fa719-171">Velja hvenær á að prenta skjöl.</span><span class="sxs-lookup"><span data-stu-id="fa719-171">Select when to print documents:</span></span>
<ul>
<li><span data-ttu-id="fa719-172"><strong>Núverandi </strong> - Prenta skjöl eftir að hver reikningur hefur verið uppfærður.</span><span class="sxs-lookup"><span data-stu-id="fa719-172"><strong>Current</strong> – Print documents after each invoice has been updated.</span></span></li>
<li><span data-ttu-id="fa719-173"><strong>Eftir </strong> – Prenta skjöl eftir allar reikningur hafa verið uppfærð.</span><span class="sxs-lookup"><span data-stu-id="fa719-173"><strong>After</strong> – Print documents after all the invoices have been updated.</span></span></li>
</ul><span data-ttu-id="fa719-174">
<strong>Athugasemd</strong> <strong>Prenta </strong> svæðið býðst aðeins ef valkosturinn <strong>Prenta reikninginn</strong>, <strong>Prenta staðfestingu</strong>, <strong>Prenta tiltektarlista </strong> eða <strong>Prenta fylgiseðla </strong> er valið.</span><span class="sxs-lookup"><span data-stu-id="fa719-174">
<strong>Note:</strong> The <strong>Print</strong> field is available only if you select the <strong>Print invoice</strong>, <strong>Print confirmation</strong>, <strong>Print picking list</strong>, or <strong>Print packing slip</strong> option.</span></span> <span data-ttu-id="fa719-175">Til dæmis, á síðunni <strong>Röðunarsíða skjámynda </strong> hefur þú sett kerfið upp til að raða upplýsingum eftir reikningslykli.</span><span class="sxs-lookup"><span data-stu-id="fa719-175">For example, on the <strong>Form sorting</strong> page, you have set up the system to sort the information by invoice account.</span></span> <span data-ttu-id="fa719-176">Þá er hægt að velja <strong>Eftir </strong> til að prenta skjölin í runu sem er flokkuð af reikningslykli.</span><span class="sxs-lookup"><span data-stu-id="fa719-176">You can then select <strong>After</strong> to print the documents in a batch that is sorted by invoice account.</span></span> <span data-ttu-id="fa719-177">Annars eru skjöl prentuð áður en vinnslu er lokið og ekki raðað í þá röð sem tilgreint er á síðunni <strong>Flokkunarsíða skjámynda</strong>.</span><span class="sxs-lookup"><span data-stu-id="fa719-177">Otherwise, the documents are printed before processing is completed, and the documents aren't sorted in the order that is specified on the <strong>Form sorting</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa719-178">Prenta reikning</span><span class="sxs-lookup"><span data-stu-id="fa719-178">Print invoice</span></span></td>
<td><span data-ttu-id="fa719-179">Veljið þennan valkost til að Prenta reikninginn.</span><span class="sxs-lookup"><span data-stu-id="fa719-179">Select this option to print the invoice.</span></span> <span data-ttu-id="fa719-180">Ef þessi valkostur slökkt er hægt að bóka reikning án þess að prenta það.</span><span class="sxs-lookup"><span data-stu-id="fa719-180">If this option is turned off, you can post an invoice without printing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa719-181">Senda tölvupóst</span><span class="sxs-lookup"><span data-stu-id="fa719-181">Send e-mail</span></span></td>
<td><span data-ttu-id="fa719-182">Veljið þennan valkost til að senda reikninginn fyrir sölupöntun til viðskiptavinar sem tölvupóstsviðhengi eftir að reikningur er bókaður.</span><span class="sxs-lookup"><span data-stu-id="fa719-182">Select this option to send the invoice for a sales order to the customer as an email attachment after the invoice is posted.</span></span> <span data-ttu-id="fa719-183">Viðhengi eru send sem PDF og XML skrár.</span><span class="sxs-lookup"><span data-stu-id="fa719-183">Attachments are sent as PDF and XML files.</span></span> <span data-ttu-id="fa719-184">Þessi valkostur er aðeins tiltækt ef valið er <strong>Virkja CFD (rafrænir reikningar)</strong> valkostinn á síðunni <strong>Færibreytur rafrænna reikninga </strong>.</span><span class="sxs-lookup"><span data-stu-id="fa719-184">This option is available only if you select the <strong>Enable CFD (electronic invoices)</strong> option on the <strong>Electronic invoice parameters</strong> page.</span></span> <span data-ttu-id="fa719-185"><strong>Athugasemd</strong> (MEX) Þessi stýring er eingöngu tiltæk fyrir lögaðila með aðalaðsetur í Mexíkó.</span><span class="sxs-lookup"><span data-stu-id="fa719-185"><strong>Note:</strong> (MEX) This control is available only to legal entities whose primary address is in Mexico.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa719-186">Nota ákvörðunarstað prentstýringar</span><span class="sxs-lookup"><span data-stu-id="fa719-186">Use print management destination</span></span></td>
<td><span data-ttu-id="fa719-187">Veljið þennan valkost til að nota prentunarstillingar sem tilgreind eru fyrir færslu, skjali eða kerfiseining á <strong>Prentstjórnunaruppsetning</strong> síðu.</span><span class="sxs-lookup"><span data-stu-id="fa719-187">Select this option to use the print settings that are specified for the transaction, document, or module on the <strong>Print management setup</strong> page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa719-188">Athuga lánamark</span><span class="sxs-lookup"><span data-stu-id="fa719-188">Check credit limit</span></span></td>
<td><span data-ttu-id="fa719-189">Veljið upplýsingar sem verða greindar þegar athugun á lánamarki er framkvæmd.</span><span class="sxs-lookup"><span data-stu-id="fa719-189">Select the information that should be analyzed when a credit limit check is performed.</span></span>
<ul>
<li><span data-ttu-id="fa719-190"><strong>Ekkert </strong> – Engin krafa um athugun á lánamarki.</span><span class="sxs-lookup"><span data-stu-id="fa719-190"><strong>None</strong> – There is no requirement for the credit limit check.</span></span></li>
<li><span data-ttu-id="fa719-191"><strong>Staða </strong> – lánamark er athugað gagnvart staða viðskiptamanns.</span><span class="sxs-lookup"><span data-stu-id="fa719-191"><strong>Balance</strong> – The credit limit is checked against the customer balance.</span></span></li>
<li><span data-ttu-id="fa719-192"><strong> Staða + fylgiseðill eða innhreyfingarskjal afurða </strong> – lánamark er athugað gagnvart stöðu viðskiptavinar og afhendingar.</span><span class="sxs-lookup"><span data-stu-id="fa719-192"><strong>Balance + packing slip or product receipt</strong> – The credit limit is checked against the customer balance and deliveries.</span></span></li>
<li><span data-ttu-id="fa719-193"><strong>Staða + allt </strong> - lánamark er athugað gagnvart staða viðskiptamanns, afhendingar og opnum pöntunum.</span><span class="sxs-lookup"><span data-stu-id="fa719-193"><strong>Balance+All</strong> – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa719-194">Kreditleiðrétting</span><span class="sxs-lookup"><span data-stu-id="fa719-194">Credit correction</span></span></td>
<td><span data-ttu-id="fa719-195">Veljið þennan valkost til að birta kreditnótu sem debet í fylgiskjali færslna.</span><span class="sxs-lookup"><span data-stu-id="fa719-195">Select this option to display the credit note as a debit in the voucher transactions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fa719-196">Kreditfæra eftirstöðvar</span><span class="sxs-lookup"><span data-stu-id="fa719-196">Credit remaining quantity</span></span></td>
<td><span data-ttu-id="fa719-197">Ef verið er að bóka kreditnótu veljið þá þennan valkost til að halda eftirstandandi magni í pöntun.</span><span class="sxs-lookup"><span data-stu-id="fa719-197">If you're posting a credit note, select this option to keep the remaining quantity on order.</span></span> <span data-ttu-id="fa719-198">Ef valmöguleikinn er hreinsaður verða eftirstöðvar settar sem 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="fa719-198">If this option is cleared, the remaining quantity is set to 0 (zero).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fa719-199">Safnuppfærsla fyrir</span><span class="sxs-lookup"><span data-stu-id="fa719-199">Summary update for</span></span></td>
<td><span data-ttu-id="fa719-200">Velja hvernig á að taka saman margar sölupantanir:</span><span class="sxs-lookup"><span data-stu-id="fa719-200">Select how multiple sales orders should be summarized:</span></span>
<ul>
<li><span data-ttu-id="fa719-201"><strong>Ekkert</strong> – Ekki taka saman sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="fa719-201"><strong>None</strong> – Don't summarize sales orders.</span></span> <span data-ttu-id="fa719-202">Til dæmis verður aðskilinn reikningur stofnaður fyrir hverja sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="fa719-202">For example, a separate invoice will be created for each sales order.</span></span></li>
<li><span data-ttu-id="fa719-203"><strong>Reikningslykill</strong> – taka saman öllum völdum pöntunum, samkvæmt skilyrðum sem sett eru upp á síðunni <strong>færibreytur safnuppfærslu</strong>.</span><span class="sxs-lookup"><span data-stu-id="fa719-203"><strong>Invoice account</strong> – Summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span></li>
<li><span data-ttu-id="fa719-204"><strong>Pöntun</strong> – Safna saman völdu sviði pantana í eina tilgreinda pöntun.</span><span class="sxs-lookup"><span data-stu-id="fa719-204"><strong>Order</strong> – Summarize a selected range of orders into one order that you specify.</span></span> <span data-ttu-id="fa719-205">Pantanir sem er safnað saman, samkvæmt skilyrðum sem sett eru upp á síðunni <strong>færibreytur safnuppfærslu </strong>.</span><span class="sxs-lookup"><span data-stu-id="fa719-205">The orders are summarized based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="fa719-206">Ef þessi valkostur er valinn skal velja gildi í svæðið <strong>sölupöntun</strong>.</span><span class="sxs-lookup"><span data-stu-id="fa719-206">If you select this option, you must select a value in the <strong>Sales order</strong> field.</span></span></li>
<li><span data-ttu-id="fa719-207"><strong>Sjálfvirk samantekt </strong> – ef samantektaruppfærslur hafa verið tilgreindar á <strong>safnuppfærslu</strong> síðu, skal safna saman allar valdar pantanir, samkvæmt skilyrðum sem sett eru upp í <strong>færibreytur safnuppfærslu</strong> síðu.</span><span class="sxs-lookup"><span data-stu-id="fa719-207"><strong>Automatic summary</strong> – If summary updates have been specified on the <strong>Summary update</strong> page, summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="fa719-208">Ef safnuppfærsla hefur ekki verið tilgreindur er pöntunin bókuð sér.</span><span class="sxs-lookup"><span data-stu-id="fa719-208">If summary updates haven't been specified, the order is posted separately.</span></span></li>
<li><span data-ttu-id="fa719-209"><strong>Fylgiseðill</strong> – Safna saman valinni röð af pöntunum í einn reikning á hvern fylgiseðil.</span><span class="sxs-lookup"><span data-stu-id="fa719-209"><strong>Packing slip</strong> – Summarize a selected range of orders into one invoice for each packing slip.</span></span> <span data-ttu-id="fa719-210">Þessi valkostur er bara tiltækur ef <strong>fylgiseðill</strong> er valið í svæðinu <strong>Magn</strong>.</span><span class="sxs-lookup"><span data-stu-id="fa719-210">This option is available only if <strong>Packing slip</strong> is selected in the <strong>Quantity</strong> field.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>






