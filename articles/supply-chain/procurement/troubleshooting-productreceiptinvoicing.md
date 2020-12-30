---
title: Villuelita innhreyfingarskjöl og reikningsfærslur
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með innhreyfingarskjöl og reikningsfærslur.
author: SmithaNataraj
manager: tfehr
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: a89effb686d60dde9d11f99be51d4101897ad4ea
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430758"
---
# <a name="troubleshoot-product-receipts-and-invoicing"></a><span data-ttu-id="e3adc-103">Villuelita innhreyfingarskjöl og reikningsfærslur</span><span class="sxs-lookup"><span data-stu-id="e3adc-103">Troubleshoot product receipts and invoicing</span></span>

<span data-ttu-id="e3adc-104">Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með innhreyfingarskjöl og reikningsfærslur.</span><span class="sxs-lookup"><span data-stu-id="e3adc-104">This topic describes how to fix issues that you might encounter while you work with product receipts and invoicing.</span></span>

## <a name="i-cant-post-more-than-one-invoice-for-a-purchase-order-line-that-has-category-based-items"></a><span data-ttu-id="e3adc-105">Ég get ekki bókað meira en einn reikning fyrir innkaupapöntunarlínu sem er með vörur flokkaðar eftir tegund.</span><span class="sxs-lookup"><span data-stu-id="e3adc-105">I can't post more than one invoice for a purchase order line that has category-based items.</span></span>

<span data-ttu-id="e3adc-106">Magn er áskilið ef bóka á reikninga.</span><span class="sxs-lookup"><span data-stu-id="e3adc-106">A quantity is mandatory if you want to post invoices.</span></span> <span data-ttu-id="e3adc-107">Ef fullt magn línu hefur verið reikningsfært fyrir aðeins hluta af upphæð, geturðu þar af leiðandi ekki reikningsfært eftirstandandi upphæð á öðrum reikningi.</span><span class="sxs-lookup"><span data-stu-id="e3adc-107">Therefore, if the full quantity of a line has been invoiced for only a partial amount, you won't be able to invoice the remaining amount on another invoice.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="e3adc-108">Ég fæ upp villuna „Tilvísun hlutar ekki stillt“ við staðfestingu á innkaupapöntun, eða undantekningin „Exception has been thrown by the target of an invocation“ kemur upp við bókun lánardrottnareiknings.</span><span class="sxs-lookup"><span data-stu-id="e3adc-108">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="e3adc-109">Þetta vandamál getur komið upp vegna ósamræmis í dreifingum innkaupapantana.</span><span class="sxs-lookup"><span data-stu-id="e3adc-109">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="e3adc-110">Til að afblokka þetta vandamál og endurstilla innkaupapöntunina á stöðuna *Drög* skal fara í **Innkaup og aðföng \> Reglubundnar vinnslur \> Hreinsun \> Endurstilling á dreifingu innkaupapöntunar**.</span><span class="sxs-lookup"><span data-stu-id="e3adc-110">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="e3adc-111">Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Leysa úr dreifingarvillum innkaupapöntunar í Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="e3adc-111">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="i-cant-consolidate-multiple-product-receipts-into-a-single-purchase-order"></a><span data-ttu-id="e3adc-112">Ég get ekki sameinað mörg innhreyfingarskjöl í eina innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="e3adc-112">I can't consolidate multiple product receipts into a single purchase order.</span></span>

<span data-ttu-id="e3adc-113">Ekki er hægt að sameina mörg innhreyfingarskjöl í eina innkaupapöntun ef mismunandi línur innhreyfingarskjals eru með mismunandi dagsetningar reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="e3adc-113">You can't consolidate multiple product receipts into a single purchase order if the different product receipt lines have different accounting dates.</span></span>

<span data-ttu-id="e3adc-114">Í fyrri útgáfum af Microsoft Dynamics 365 Supply Chain Management var sameining leyfð í þessum aðstæðum.</span><span class="sxs-lookup"><span data-stu-id="e3adc-114">In earlier versions of Microsoft Dynamics 365 Supply Chain Management, consolidation was allowed in this situation.</span></span> <span data-ttu-id="e3adc-115">Hins vegar komu oft upp villur þegar það var gert.</span><span class="sxs-lookup"><span data-stu-id="e3adc-115">However, the practice is prone to error.</span></span> <span data-ttu-id="e3adc-116">Dagsetning reikningsskila á innkaupapöntunarlínunum sem eru stofnaðar ættu ekki að vera frábrugðnar dagsetningu reikningsskila í línum innhreyfingarskjals sem þessar innkaupapöntunarlínur voru stofnaðar úr.</span><span class="sxs-lookup"><span data-stu-id="e3adc-116">The accounting date on the purchase order lines that are created should not differ from the accounting date on the product receipt lines that those purchase order lines were created from.</span></span> <span data-ttu-id="e3adc-117">(Dagsetning reikningsskila á innkaupapöntunarlínum samsvarar dagsetningu reikningsskila í haus innkaupapöntunarinnar.) Þess vegna er sameining margra innhreyfingarskjala í eina innkaupapöntun ekki lengur leyfð.</span><span class="sxs-lookup"><span data-stu-id="e3adc-117">(The accounting date on the purchase order lines matches the accounting date on the purchase order header.) Therefore, the consolidation of multiple product receipts into a single purchase orders is no longer allowed.</span></span>

<span data-ttu-id="e3adc-118">Dagsetning reikningsskila er notuð, til dæmis fyrir frátektir fjárhagsáætlunar og fjárúthlutunar.</span><span class="sxs-lookup"><span data-stu-id="e3adc-118">The accounting date is used, for example, for budget reservations and encumbrance.</span></span> <span data-ttu-id="e3adc-119">Því ætti að halda henni við umbreytingu úr innhreyfingarskjali í innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="e3adc-119">Therefore, it should be kept during the transition from product receipt to purchase order.</span></span>

## <a name="when-product-receipts-are-canceled-transactions-can-be-posted-to-a-suspended-ledger-account"></a><span data-ttu-id="e3adc-120">Þegar hætt er við innhreyfingarskjöl er hægt að bóka færslur á frestaðan fjárhagslykil.</span><span class="sxs-lookup"><span data-stu-id="e3adc-120">When product receipts are canceled, transactions can be posted to a suspended ledger account.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e3adc-121">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="e3adc-121">Issue description</span></span>

<span data-ttu-id="e3adc-122">Ef hætt er við innhreyfingarskjal, gerir kerfið kleift að bóka færslur á frestaða fjárhagslykla jafnvel þótt aðallyklum sé frestað.</span><span class="sxs-lookup"><span data-stu-id="e3adc-122">If a product receipt is canceled, the system allows transactions to be posted to suspended ledger accounts, even though the main accounts are suspended.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="e3adc-123">Framkallaðu vandamálið</span><span class="sxs-lookup"><span data-stu-id="e3adc-123">Reproduce the issue</span></span>

<span data-ttu-id="e3adc-124">Eftirfarandi ferli sýnir eina leið til að endurtaka málið.</span><span class="sxs-lookup"><span data-stu-id="e3adc-124">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="e3adc-125">Á síðunni **Færibreytur viðskiptaskulda**, í flipanum **Almennt**, skal ganga úr skugga um að valkosturinn **Bóka innhreyfingarskjal afurða í fjárhag** sé stilltur á *Já*.</span><span class="sxs-lookup"><span data-stu-id="e3adc-125">On the **Accounts payable parameters** page, on the **General** tab, make sure that the **Post product receipt in ledger** option is set to *Yes*.</span></span>
1. <span data-ttu-id="e3adc-126">Stofnið innkaupapöntun og bætið við pöntunarlínu sem er með magnið *1000* fyrir afurð.</span><span class="sxs-lookup"><span data-stu-id="e3adc-126">Create a purchase order, and add an order line that has a quantity of *1,000* for a product.</span></span>
1. <span data-ttu-id="e3adc-127">Staðfesta innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="e3adc-127">Confirm the purchase order.</span></span>
1. <span data-ttu-id="e3adc-128">Bókið innhreyfingarskjalið og athugið fylgiskjölin.</span><span class="sxs-lookup"><span data-stu-id="e3adc-128">Post the product receipt, and check the vouchers.</span></span>
1. <span data-ttu-id="e3adc-129">Frestið viðkomandi aðallyklum, *200140* og *140200*.</span><span class="sxs-lookup"><span data-stu-id="e3adc-129">Suspend the relevant main accounts, *200140* and *140200*.</span></span>
1. <span data-ttu-id="e3adc-130">Hættið við bókað innhreyfingarskjal afurðar.</span><span class="sxs-lookup"><span data-stu-id="e3adc-130">Cancel the posted product receipt.</span></span>
1. <span data-ttu-id="e3adc-131">Takið eftir að hægt er að bóka færslur á frestaða fjárhagslykla.</span><span class="sxs-lookup"><span data-stu-id="e3adc-131">Notice that transactions can be posted to the suspended leger accounts.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e3adc-132">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="e3adc-132">Issue resolution</span></span>

<span data-ttu-id="e3adc-133">Hægt er að bóka færslur á frestaða fjárhagslykla þegar hætt er við innhreyfingarskjöl vegna þess að þessi hegðun leyfir réttar bókanir.</span><span class="sxs-lookup"><span data-stu-id="e3adc-133">Transactions can be posted to the suspended leger accounts when product receipts are canceled, because this behavior allows for correct postings.</span></span>

## <a name="a-product-receipt-voucher-number-is-consumed-even-if-no-financial-voucher-is-generated-during-product-receipt"></a><span data-ttu-id="e3adc-134">Fylgiskjalsnúmer innhreyfingarskjals er notað þótt ekkert fjárhagsskjal sé búið til við móttöku afurðar.</span><span class="sxs-lookup"><span data-stu-id="e3adc-134">A product receipt voucher number is consumed even if no financial voucher is generated during product receipt.</span></span>

<span data-ttu-id="e3adc-135">Ef valkosturinn **Safna upp skuld á innhreyfingarskjali** er stilltur á *Nei* fyrir vörulíkanaflokkinn, munu engar bókanir á fjárhagnum eiga sér stað.</span><span class="sxs-lookup"><span data-stu-id="e3adc-135">If the **Accrue liability on product receipt** option is set to *No* for the item model group, no postings to the general ledger will occur.</span></span> <span data-ttu-id="e3adc-136">Efnislegt tilvik verður hins vegar skráð af bókhaldsástæðum í undirbók og þetta tilvik þarf fylgiskjalsnúmer.</span><span class="sxs-lookup"><span data-stu-id="e3adc-136">However, a physical event will be recorded for the purpose of accounting in a subledger, and that event requires a voucher number.</span></span> <span data-ttu-id="e3adc-137">Þetta fylgiskjalsnúmer er það fylgiskjalsnúmer sem vísað er til í birgðafærslum.</span><span class="sxs-lookup"><span data-stu-id="e3adc-137">This voucher number is the voucher number that is referenced in the inventory transactions.</span></span>

<span data-ttu-id="e3adc-138">Mælt er með því að valkosturinn **Safna upp skuld á innhreyfingarskjali** sé stilltur á *Já* eins og lýst er í eftirfarandi bloggfærslu: [Bóka ýmis gjöld þegar afurð er móttekin](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="e3adc-138">We recommend that you set the **Accrue liability on product receipt** option to *Yes*, as described in the following blog post: [Post Misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a><span data-ttu-id="e3adc-139">Ekki er kveikt á stillingunni Bóka á gjaldalykil í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="e3adc-139">The Post to charge account in ledger setting isn't turned on.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e3adc-140">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="e3adc-140">Issue description</span></span>

<span data-ttu-id="e3adc-141">Þetta vandamál á sér stað þegar innkaupapöntun er reikningsfærð, ef valkosturinn **Bóka á gjaldalykil í fjárhag** er stilltur á *Já* í flipanum **Reikningur** á síðunni **Færibreytur viðskiptaskulda**.</span><span class="sxs-lookup"><span data-stu-id="e3adc-141">This issue occurs when a purchase order is invoiced, if the **Post to charge account in ledger** option is set to *Yes* on the **Invoice** tab of the **Accounts payable parameters** page.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="e3adc-142">Framkallaðu vandamálið</span><span class="sxs-lookup"><span data-stu-id="e3adc-142">Reproduce the issue</span></span>

<span data-ttu-id="e3adc-143">Eftirfarandi ferli sýnir eina leið til að endurtaka málið.</span><span class="sxs-lookup"><span data-stu-id="e3adc-143">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="e3adc-144">Farðu í **Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**.</span><span class="sxs-lookup"><span data-stu-id="e3adc-144">Go to **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
1. <span data-ttu-id="e3adc-145">Í flipanum **Reikningur** skal stilla valkostinn **Bóka á gjaldalykil í fjárhag** á *Já*.</span><span class="sxs-lookup"><span data-stu-id="e3adc-145">On the **Invoice** tab, set the **Post to charge account in ledger** option to *Yes*.</span></span>
1. <span data-ttu-id="e3adc-146">Opnið **Birgðastjórnun \> Uppsetning \> Bókun \> Bókun**.</span><span class="sxs-lookup"><span data-stu-id="e3adc-146">Go to **Inventory management \> Setup \> Posting \> Posting**.</span></span>
1. <span data-ttu-id="e3adc-147">Í flipanum **Innkaupapöntun** skal ganga úr skugga um að öllum línum hafi verið eytt í útgjöldum innkaupa fyrir afurðina.</span><span class="sxs-lookup"><span data-stu-id="e3adc-147">On the **Purchase order** tab, make sure that you've deleted all the lines in the purchase expenditure for the product.</span></span>
1. <span data-ttu-id="e3adc-148">Opnið **Viðskiptaskuldir \> Innkaupapantanir \> Allar innkaupapantanir**.</span><span class="sxs-lookup"><span data-stu-id="e3adc-148">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="e3adc-149">Stofna innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="e3adc-149">Create a purchase order.</span></span> <span data-ttu-id="e3adc-150">Í reitnum **Lánardrottnalykill** skal velja *1001 Acme Skrifstofuvörur*.</span><span class="sxs-lookup"><span data-stu-id="e3adc-150">In the **Vendor account** field, select *1001 Acme Office Supplies*.</span></span>
1. <span data-ttu-id="e3adc-151">Bætið við innpöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="e3adc-151">Add a purchase order line that has the following settings:</span></span>

    - <span data-ttu-id="e3adc-152">**Vörunúmer:** *D0011 Leysiprentari*</span><span class="sxs-lookup"><span data-stu-id="e3adc-152">**Item number:** *D0011 Laser Projector*</span></span>
    - <span data-ttu-id="e3adc-153">**Svæði:** *1*</span><span class="sxs-lookup"><span data-stu-id="e3adc-153">**Site:** *1*</span></span>
    - <span data-ttu-id="e3adc-154">**Vöruhús:** *11*</span><span class="sxs-lookup"><span data-stu-id="e3adc-154">**Warehouse:** *11*</span></span>
    - <span data-ttu-id="e3adc-155">**Magn:** *4*</span><span class="sxs-lookup"><span data-stu-id="e3adc-155">**Quantity:** *4*</span></span>

1. <span data-ttu-id="e3adc-156">Á aðgerðasvæðinu, í flipanum **Innkaup**, í flokknum **Aðgerð**, skal velja **Staðfesta**.</span><span class="sxs-lookup"><span data-stu-id="e3adc-156">On the Action Pane, on the **Purchase** tab, in the **Action** group, select **Confirm**.</span></span>
1. <span data-ttu-id="e3adc-157">Á aðgerðasvæðinu, í flipanum **Móttaka**, í flokknum **Mynda**, skal velja **Innhreyfingarskjal afurðar**.</span><span class="sxs-lookup"><span data-stu-id="e3adc-157">On the Action Pane, on the **Receive** tab, in the **Generate** group, select **Product receipt**.</span></span>
1. <span data-ttu-id="e3adc-158">Í svargluggannn **Bókun innhreyfingarskjals afurða**, í reitinn **Innhreyfingarskjal**, skal færa inn handahófskennt númer og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e3adc-158">In the **Posting product receipt** dialog box, in the **Product receipt** field, enter an arbitrary number, and then select **OK**.</span></span>
1. <span data-ttu-id="e3adc-159">Á aðgerðasvæðinu, í flipanum **Reikningur**, í flokknum **Búa til** skal velja á **Reikningur**.</span><span class="sxs-lookup"><span data-stu-id="e3adc-159">On the Action Pane, on the **Invoice** tab, in the **Generate** group, select **Invoice**.</span></span>
1. <span data-ttu-id="e3adc-160">Í reitinn **Númer** skal færa inn handahófskennt númer sem reikningsnúmerið.</span><span class="sxs-lookup"><span data-stu-id="e3adc-160">In the **Number** field, enter an arbitrary number as the invoice number.</span></span>
1. <span data-ttu-id="e3adc-161">Uppfærið samsvörunarstöðuna og bókið.</span><span class="sxs-lookup"><span data-stu-id="e3adc-161">Update the match status, and post.</span></span>
1. <span data-ttu-id="e3adc-162">Takið eftir því að nú kemur upp eftirfarandi villa þegar reikningur er búinn til úr innkaupapöntun: „Númer lykils fyrir færslugerðin Útgjöld innkaupa fyrir afurð er ekki til.“</span><span class="sxs-lookup"><span data-stu-id="e3adc-162">Notice that you now receive the following error when you generate an invoice from a purchase order: "Account number for transaction type Purchase expenditure for product does not exist."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e3adc-163">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="e3adc-163">Issue resolution</span></span>

<span data-ttu-id="e3adc-164">Þetta fer eftir færibreytustillingunum fyrir reikninga og reikningaflokka.</span><span class="sxs-lookup"><span data-stu-id="e3adc-164">This depends on the parameter settings for invoices and invoice groups.</span></span> <span data-ttu-id="e3adc-165">Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Bókhald fyrir Útgjöld innkaupa og Afbrigði birgða](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span><span class="sxs-lookup"><span data-stu-id="e3adc-165">For more information, see the following blog post: [Accounting for Purchase charge and Stock variation](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).</span></span>
