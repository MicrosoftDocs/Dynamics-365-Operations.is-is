---
title: Afstemming farms í flutningsstjórnun
description: Þetta efni útskýrir ferli afstemmingar farms.
author: MarkusFogelberg
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSAuditMaster, TMSFreightBillInvoiceReconcile, TMSFreightBillSummary, TMSFreightBillType, TMSFreightMatchReason, TMSFBDetailReconcile, TMSInvoiceTable,TMSInvoiceLineReconcile,TMSReconcileInvoice, TMSFreightBillDetail, TMSFreightBillTypeAssignment, TMSRejectInvoiceLine, TMSMiscellaneousCharge
audience: Application User
ms.reviewer: kamaybac
ms.custom: 89983
ms.assetid: bc34a9b1-0c11-4797-b463-25409cf98ca8
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d523af235d645bd282af07d6a1f617bca5fba2dc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809087"
---
# <a name="reconcile-freight-in-transportation-management"></a><span data-ttu-id="043e4-103">Afstemming farms í flutningsstjórnun</span><span class="sxs-lookup"><span data-stu-id="043e4-103">Reconcile freight in transportation management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="043e4-104">Þetta efni útskýrir ferli afstemmingar farms.</span><span class="sxs-lookup"><span data-stu-id="043e4-104">This topic describes the freight reconciliation process.</span></span>

<span data-ttu-id="043e4-105">Afstemming farms hægt að gera handvirkt eða hægt er að setja hann upp til að eiga sér stað sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="043e4-105">Freight reconciliation can be done manually, or it can be set up to occur automatically.</span></span> <span data-ttu-id="043e4-106">Til að nota afstemmingu farms sjálfvirk, verður að setja upp aðalgögn endurskoðunar þar sem hægt er að skilgreina skilyrði sem ákvarða hvaða farmbréf jafnað sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="043e4-106">To use automatic freight reconciliation, you must set up an audit master where you can define criteria that determine which freight bills are matched automatically.</span></span>

## <a name="the-freight-reconciliation-process"></a><span data-ttu-id="043e4-107">Ferli afstemmingar farms</span><span class="sxs-lookup"><span data-stu-id="043e4-107">The freight reconciliation process</span></span>

<span data-ttu-id="043e4-108">Farmgjöld eru reiknaðar af taxtavél sem tengist viðkomandi farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="043e4-108">Freight rates are calculated by the rate engine that is associated with the relevant shipping carrier.</span></span> <span data-ttu-id="043e4-109">Þegar farmur er staðfest farmbréfs er mynduð og farmgjöld eru fluttar í honum.</span><span class="sxs-lookup"><span data-stu-id="043e4-109">When a load is confirmed, a freight bill is generated, and the freight rates are transferred to it.</span></span> <span data-ttu-id="043e4-110">Skatthlutfall farms eru skipts sem ýmis gjöld fyrir viðkomandi upprunaskjalið (innkaupapöntun, sölupöntun, og/eða flutningspöntun), eftir uppsetningu sem er notuð fyrir venjulegum reikningsferli.</span><span class="sxs-lookup"><span data-stu-id="043e4-110">The freight rates are apportioned as miscellaneous charges to the relevant source document (purchase order, sales order, and/or transfer order), depending on the setup that is used for the regular billing process.</span></span> <span data-ttu-id="043e4-111">Ferli afstemmingar farms (sem er einnig þekkt sem samsvarandi) getur hafist þegar farmreikninginn berst frá farmflytjandanum.</span><span class="sxs-lookup"><span data-stu-id="043e4-111">The freight reconciliation process (which is also known as the matching process) can start as soon as the freight invoice arrives from the shipping carrier.</span></span> <span data-ttu-id="043e4-112">Hægt er að fá reikningsins rafrænt eða á pappír.</span><span class="sxs-lookup"><span data-stu-id="043e4-112">The invoice can be received electronically or on paper.</span></span> <span data-ttu-id="043e4-113">Ef reikningurinn er móttekin á pappír, hægt er að mynda rafræna reikninga með því að nota farmbréfið sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="043e4-113">If the invoice is received on paper, you can generate an electronic invoice by using the freight bill as a template.</span></span>

<span data-ttu-id="043e4-114">[![Afstemmingarferli farms](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span><span class="sxs-lookup"><span data-stu-id="043e4-114">[![Freight reconciliation process](./media/freight-reconcilation-process.jpg)](./media/freight-reconcilation-process.jpg)</span></span>

## <a name="manual-reconciliation"></a><span data-ttu-id="043e4-115">handvirkur afstemmingu</span><span class="sxs-lookup"><span data-stu-id="043e4-115">Manual reconciliation</span></span>

<span data-ttu-id="043e4-116">Ef verið er að afstemmingu farms handvirkt, verður að samsvara hverri reikningslínu með farmbréf línu eða línum fyrir farm sem verið er að reikningsfæra.</span><span class="sxs-lookup"><span data-stu-id="043e4-116">If you're reconciling freight manually, you must match each invoice line with the freight bill line or lines for the load that is being invoiced.</span></span> <span data-ttu-id="043e4-117">Gera þetta jöfnun á **Farmbréf og reikningsjöfnun** síðu.</span><span class="sxs-lookup"><span data-stu-id="043e4-117">You do this matching on the **Freight bill and invoice matching** page.</span></span> <span data-ttu-id="043e4-118">Ef magn á reikningslínu passar ekki við upphæð farmbréf, verður að velja afstemmingarástæða fyrir mismuninn.</span><span class="sxs-lookup"><span data-stu-id="043e4-118">If the amount on the invoice line doesn’t match the freight bill amount, you must select a reconciliation reason for the difference.</span></span> <span data-ttu-id="043e4-119">Ef eru margar ástæður fyrir afstemmingu er hægt að skipta ójöfnuð upphæð á þeim.</span><span class="sxs-lookup"><span data-stu-id="043e4-119">If there are multiple reasons for reconciliation, you can split the unmatched amount across them.</span></span> <span data-ttu-id="043e4-120">Ástæða afstemmingu ákvarðar hvernig mismunur upphæðirnar eru bókaðar í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="043e4-120">The reconciliation reason determines how the difference amounts are posted in the general ledger.</span></span> <span data-ttu-id="043e4-121">Þegar afstemmingu allt reikningsupphæð er tekið, er hún send til samþykkis og síðan bóka færslubókina.</span><span class="sxs-lookup"><span data-stu-id="043e4-121">When the reconciliation of the whole invoice amount is accounted for, it's submitted for approval, and then the journal is posted.</span></span> <span data-ttu-id="043e4-122">Eftirfarandi dæmi sýnir hvernig á að mynda reikning farms og framkvæma afstemmingu farms.</span><span class="sxs-lookup"><span data-stu-id="043e4-122">The following illustration shows how to generate a freight invoice and do freight reconciliation.</span></span>

<span data-ttu-id="043e4-123">[![Afstemmingarverk farms](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span><span class="sxs-lookup"><span data-stu-id="043e4-123">[![Freight reconciliation tasks](./media/processflowforfreightreconciliation.jpg)](./media/processflowforfreightreconciliation.jpg)</span></span>

## <a name="automatic-reconciliation"></a><span data-ttu-id="043e4-124">Sjálfvirka afstemmingu</span><span class="sxs-lookup"><span data-stu-id="043e4-124">Automatic reconciliation</span></span>

<span data-ttu-id="043e4-125">Til að nota sjálfvirka afstemmingu, verður að tilgreina áætlun fyrir afstemmingu, og reikninga og farmflytjendur að nota.</span><span class="sxs-lookup"><span data-stu-id="043e4-125">To use automatic reconciliation, you must specify the schedule for reconciliation, and the invoices and shipping carriers to use.</span></span> <span data-ttu-id="043e4-126">Jöfnun reikningslínur og farmbréf er gert eftir uppsetningu á endurskoðunarsniðmát og farmbréfs gerð.</span><span class="sxs-lookup"><span data-stu-id="043e4-126">The matching of the invoice lines and freight bills is done according to the setup of the audit master and freight bill type.</span></span> <span data-ttu-id="043e4-127">Eftir sjálfvirka afstemmingu er keyrð, verður að meðhöndla hvaða reikninga sem kerfið getur ekki samsvarað.</span><span class="sxs-lookup"><span data-stu-id="043e4-127">After you run the automatic reconciliation, you must handle any invoices that the system can't match.</span></span> <span data-ttu-id="043e4-128">Verður svo að vinna þessar reikninga handvirkt áður en hægt er að bóka reikninga til greiðslu.</span><span class="sxs-lookup"><span data-stu-id="043e4-128">You must then process these invoices manually before you can post all the invoices for payment.</span></span>

## <a name="match-freight-bills-with-freight-invoices-using-automatic-or-manual-reconciliation"></a><span data-ttu-id="043e4-129">Stemma farmbréf við farmreikninga með sjálfvirkri eða handvirkri afstemmingu</span><span class="sxs-lookup"><span data-stu-id="043e4-129">Match freight bills with freight invoices using automatic or manual reconciliation</span></span>

<span data-ttu-id="043e4-130">*Samsvörun* er ferli sem finnur farmbréfin sem stemma við hvern farmreikning.</span><span class="sxs-lookup"><span data-stu-id="043e4-130">*Matching* is the process of finding the freight bills that correspond to each freight invoice.</span></span> <span data-ttu-id="043e4-131">Þetta er hægt að gera með því að samsvara reikningslínurnar hver af annarri (handvirk samsvörun) eða með því að samsvara alla tiltæka reikninga í einu (sjálfvirk samsvörun).</span><span class="sxs-lookup"><span data-stu-id="043e4-131">This can be done by matching the invoice lines one-by-one (manual matching), or by matching all available invoices at once (auto matching).</span></span>

### <a name="auto-matching"></a><span data-ttu-id="043e4-132">Jafna sjálfvirkt</span><span class="sxs-lookup"><span data-stu-id="043e4-132">Auto matching</span></span>

<span data-ttu-id="043e4-133">Þegar margir farmreikningar eru samsvaraðir við sama farmbréfið, þá gengur sjálfvirka samsvörunarferlið svona fyrir sig:</span><span class="sxs-lookup"><span data-stu-id="043e4-133">When matching multiple freight invoices to the same freight bill, the process for auto matching works as follows:</span></span>

1. <span data-ttu-id="043e4-134">Allir farmreikningar sem ekki eru samsvaraðir er raðað eftir upphæð þar sem hæsta upphæðin kemur fyrst.</span><span class="sxs-lookup"><span data-stu-id="043e4-134">All freight invoices not matched are sorted by amount, with largest amount first.</span></span>
1. <span data-ttu-id="043e4-135">Farmreikningarnir eru samsvaraðir einn af einum þar til farmbréfið er ekki lengur með neinar jákvæðar upphæðir.</span><span class="sxs-lookup"><span data-stu-id="043e4-135">The freight invoices are matched one-by-one, until the freight bill has no positive amount remaining.</span></span>
1. <span data-ttu-id="043e4-136">Eftirstandandi upphæð er stillt eftir því hver uppsetning á endurskoðunarsniðmátinu er og eftirstandandi upphæð á farmreikningum.</span><span class="sxs-lookup"><span data-stu-id="043e4-136">Depending on the setup of the audit master and the remaining amount on the freight invoices, the remaining amount is set.</span></span>

### <a name="manual-matching"></a><span data-ttu-id="043e4-137">Handvirk samsvörun</span><span class="sxs-lookup"><span data-stu-id="043e4-137">Manual matching</span></span>

<span data-ttu-id="043e4-138">Öll farmbréf með jákvæðum upphæðum verða hægt að samsvara.</span><span class="sxs-lookup"><span data-stu-id="043e4-138">All freight bills with positive amounts will be available for matching.</span></span> <span data-ttu-id="043e4-139">Notandi getur, með svipuðum hætti og í sjálfvirkri samsvörun, aðeins samsvarað farmreikninga með neikvæðum upphæðum við farmbréf sem ekki eru samsvöruð að fullu.</span><span class="sxs-lookup"><span data-stu-id="043e4-139">Similar to auto matching, the user will only be able to match freight invoices with negative amounts to freight bills not fully matched.</span></span>

### <a name="example"></a><span data-ttu-id="043e4-140">Dæmi</span><span class="sxs-lookup"><span data-stu-id="043e4-140">Example</span></span>

<span data-ttu-id="043e4-141">Segjum að þú sért með farmbréf að upphæð 1500 og þú hefur stofnað þrjá farmreikninga fyrir farmbréfið með einni reikningslínu fyrir hvern reikning með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="043e4-141">Suppose that you have a freight bill (FB) for an amount of 1500 and you have created three freight invoices for the freight bill with one invoice line for each invoice with following settings:</span></span>

- <span data-ttu-id="043e4-142">Upprunalegt farmbréf: Upphæð 1500</span><span class="sxs-lookup"><span data-stu-id="043e4-142">Original freight bill (FB): Amount 1500</span></span>
- <span data-ttu-id="043e4-143">Reikningur 1 (Inv1): Upphæð 1000</span><span class="sxs-lookup"><span data-stu-id="043e4-143">Invoice 1 (Inv1): Amount 1000</span></span>
- <span data-ttu-id="043e4-144">Reikningur 2 (Inv2): Upphæð 600</span><span class="sxs-lookup"><span data-stu-id="043e4-144">Invoice 2 (Inv2): Amount 600</span></span>
- <span data-ttu-id="043e4-145">Reikningur 3 (Inv3): Upphæð -100</span><span class="sxs-lookup"><span data-stu-id="043e4-145">Invoice 3 (Inv3): Amount -100</span></span>

#### <a name="automatic-matching-result"></a><span data-ttu-id="043e4-146">Niðurstöður sjálfvirkrar samsvörunar</span><span class="sxs-lookup"><span data-stu-id="043e4-146">Automatic matching result</span></span>

<span data-ttu-id="043e4-147">Sjálfvirk jöfnun mun keyra í eftirfarandi röð:</span><span class="sxs-lookup"><span data-stu-id="043e4-147">Auto matching will execute in following order:</span></span>

1. <span data-ttu-id="043e4-148">Raða öllum farmreikningum eftir upphæð í lækkandi röð: Inv1 -> Inv2 -> Inv3.</span><span class="sxs-lookup"><span data-stu-id="043e4-148">Sort all freight invoices descending by amount: Inv1 -> Inv2 -> Inv3.</span></span>
1. <span data-ttu-id="043e4-149">Jafna Inv1 við FB.</span><span class="sxs-lookup"><span data-stu-id="043e4-149">Match Inv1 with FB.</span></span> <span data-ttu-id="043e4-150">Inv1 er með 1000 samsvarað og farmbréfið er með upphæð 500 þannig að staðan er stillt á *Samsvörun að hluta til*.</span><span class="sxs-lookup"><span data-stu-id="043e4-150">Inv1 has 1000 matched and FB has 500 amount remaining, so the status is set to *Partially matched*.</span></span>
1. <span data-ttu-id="043e4-151">Jafna Inv2 við FB.</span><span class="sxs-lookup"><span data-stu-id="043e4-151">Match Inv2 with FB.</span></span> <span data-ttu-id="043e4-152">Inv2 er með 500 samsvarað og farmbréfið er með 0 eftirstandandi þannig að staðan er stillt á *Samsvörun að fullu*.</span><span class="sxs-lookup"><span data-stu-id="043e4-152">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="043e4-153">Vegna þess að FB er nú að fullu jafnað verður Inv3 ekki unnið.</span><span class="sxs-lookup"><span data-stu-id="043e4-153">Because FB is now fully matched, Inv3 won't be processed.</span></span>

#### <a name="manual-matching-result"></a><span data-ttu-id="043e4-154">Niðurstöður handvirkrar samsvörunar</span><span class="sxs-lookup"><span data-stu-id="043e4-154">Manual matching result</span></span>

<span data-ttu-id="043e4-155">Fyrir handvirka samsvörun fara niðurstöðurnar eftir röð samsvörunar eins og sýnt er í eftirfarandi dæmum.</span><span class="sxs-lookup"><span data-stu-id="043e4-155">For manual matching, the results vary depending on the order of the matching, as illustrated in the following example cases.</span></span>

##### <a name="manual-matching-case-1"></a><span data-ttu-id="043e4-156">Handvirk samsvörun máls 1</span><span class="sxs-lookup"><span data-stu-id="043e4-156">Manual matching case 1</span></span>

<span data-ttu-id="043e4-157">Ein leið til að gera handvirka samsvörun í þessu dæmi er að halda áfram á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="043e4-157">One way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="043e4-158">Jafna FB með Inv1.</span><span class="sxs-lookup"><span data-stu-id="043e4-158">Match FB with Inv1.</span></span> <span data-ttu-id="043e4-159">Farmbréf er með 500 sem eftirstandandi upphæð þannig að staðan er stillt á *Samsvörun að hluta til*.</span><span class="sxs-lookup"><span data-stu-id="043e4-159">FB has 500 amount remaining, so the status set to *Partially matched*.</span></span>
1. <span data-ttu-id="043e4-160">Jafna Inv2 við FB.</span><span class="sxs-lookup"><span data-stu-id="043e4-160">Match Inv2 with FB.</span></span> <span data-ttu-id="043e4-161">Inv2 er með 500 samsvarað og farmbréfið er með 0 eftirstandandi þannig að staðan er stillt á *Samsvörun að fullu*.</span><span class="sxs-lookup"><span data-stu-id="043e4-161">Inv2 has 500 matched and FB has 0 remaining, so the status is set to *Fully matched*.</span></span>
1. <span data-ttu-id="043e4-162">Við handvirka samsvörun á Inv3 finnurðu engin ójöfnuð farmbréf.</span><span class="sxs-lookup"><span data-stu-id="043e4-162">When manually matching Inv3, you won't find any unmatched freight bills.</span></span>

<span data-ttu-id="043e4-163">Þetta tilfelli er í meginatriðum það sama og sjálfvirk samsvörun</span><span class="sxs-lookup"><span data-stu-id="043e4-163">This case is essentially the same as auto matching</span></span>

##### <a name="manual-matching-case-2"></a><span data-ttu-id="043e4-164">Handvirk samsvörun máls 2</span><span class="sxs-lookup"><span data-stu-id="043e4-164">Manual matching case 2</span></span>

<span data-ttu-id="043e4-165">Önnur leið til að gera handvirka samsvörun í þessu dæmi er að halda áfram á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="043e4-165">Another way to do manual matching for this example is to proceed as follows:</span></span>

1. <span data-ttu-id="043e4-166">Jafna Inv3 við FB.</span><span class="sxs-lookup"><span data-stu-id="043e4-166">Match Inv3 with FB.</span></span> <span data-ttu-id="043e4-167">Nú er farmbréfið með 1600 í eftirstöðvar sem er það sama og að draga frá neikvæða 100 ofan á 1500.</span><span class="sxs-lookup"><span data-stu-id="043e4-167">Now FB has amount remaining 1600, which is the same as subtracting negative 100 on top of 1500.</span></span> <span data-ttu-id="043e4-168">Bæði farmbréfið og Inv3 eru með samsvaraða upphæð -100.</span><span class="sxs-lookup"><span data-stu-id="043e4-168">Both FB and Inv3 have a matched quantity of -100.</span></span>
1. <span data-ttu-id="043e4-169">Jafna Inv1 og Inv 2 við farmbréf eitt á eftir öðru.</span><span class="sxs-lookup"><span data-stu-id="043e4-169">Match Inv1 and Inv 2 with FB one after another.</span></span> <span data-ttu-id="043e4-170">Farmbréf er að samsvarað að fullu.</span><span class="sxs-lookup"><span data-stu-id="043e4-170">FB is fully matched.</span></span>

<span data-ttu-id="043e4-171">Eins og þetta dæmi sýnir á aðeina að samsvara farmreikninga með neikvæðum upphæðum handvirkt.</span><span class="sxs-lookup"><span data-stu-id="043e4-171">As this example shows, matching freight invoices with negative amounts should only be done manually.</span></span> <span data-ttu-id="043e4-172">Þetta tryggir að það sé alltaf hægt að samsvara farmreikninga með neikvæðum upphæðum við farmbréf sem ekki er samsvarað að fullu vegna þess að það gerir notanda kleift að hafa stjórnun á röð samsvörunar.</span><span class="sxs-lookup"><span data-stu-id="043e4-172">This will ensure that it is always possible to match the freight invoices with negative amounts to a freight bill not fully matched because that enables you to control the matching sequence.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]