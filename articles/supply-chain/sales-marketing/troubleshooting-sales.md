---
title: Villuleita sölupantanir
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með sölupantanir.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTable, SalesTableListPage, SalesTableListPage_SalesCancelOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b5389b0d5a8ff68a3c16dedd2d8bb62f6e99af4f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824727"
---
# <a name="troubleshoot-sales-orders"></a><span data-ttu-id="54f32-103">Villuleita sölupantanir</span><span class="sxs-lookup"><span data-stu-id="54f32-103">Troubleshoot sales orders</span></span>

<span data-ttu-id="54f32-104">Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="54f32-104">This topic describes how to fix issues that you might encounter while you work with sales orders.</span></span>

## <a name="the-tax-information-isnt-updated-if-i-change-the-location-on-a-sales-order-header"></a><span data-ttu-id="54f32-105">Skattaupplýsingarnar eru ekki uppfærðar ef ég breyti staðsetningunni í sölupöntunarhaus.</span><span class="sxs-lookup"><span data-stu-id="54f32-105">The tax information isn't updated if I change the location on a sales order header.</span></span>

### <a name="issue-description"></a><span data-ttu-id="54f32-106">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="54f32-106">Issue description</span></span>

<span data-ttu-id="54f32-107">Ef svæði, vöruhúsi eða afhendingaraðsetri er breytt annaðhvort í sölupöntunarhaus eða á línustigi, uppfærast skattaupplýsingarnar ekki sjálfkrafa fyrir línurnar.</span><span class="sxs-lookup"><span data-stu-id="54f32-107">If the site, warehouse, or delivery address is changed either on a sales order header or at the line level, the case tax information isn't automatically updated for the lines.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="54f32-108">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="54f32-108">Issue resolution</span></span>

<span data-ttu-id="54f32-109">Þessi hegðun er samkvæmt hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="54f32-109">This behavior is by design.</span></span> <span data-ttu-id="54f32-110">Vandamálið stafar af því að afhendingaraðsetri, svæði og vöruhúsi er ekki breytt sjálfkrafa á línustigi heldur.</span><span class="sxs-lookup"><span data-stu-id="54f32-110">The issue occurs because the delivery address, site, and warehouse aren't automatically changed at the line level either.</span></span> <span data-ttu-id="54f32-111">Uppfæra verður handvirkt.</span><span class="sxs-lookup"><span data-stu-id="54f32-111">You must update them manually.</span></span>

## <a name="if-there-are-two-trade-agreements-for-the-same-period-or-overlapping-periods-the-same-agreement-line-is-always-selected"></a><span data-ttu-id="54f32-112">Ef það eru tveir viðskiptasamningar fyrir sama tímabil eða tímabil sem skarast er sama samningslínan alltaf valin.</span><span class="sxs-lookup"><span data-stu-id="54f32-112">If there are two trade agreements for the same period or overlapping periods, the same agreement line is always selected.</span></span>

### <a name="issue-description"></a><span data-ttu-id="54f32-113">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="54f32-113">Issue description</span></span>

<span data-ttu-id="54f32-114">Ef tveir viðskiptasamningar eru skilgreindir fyrir sama tímabil eða tímabil sem skarast, virðist sami viðskiptasamningur vera valinn í hvert skipti sem stofnaðar eru sölupöntunarlínur sem innihalda þessar vörur.</span><span class="sxs-lookup"><span data-stu-id="54f32-114">If two trade agreements are defined for the same period or overlapping periods, the same trade agreement seems to be selected every time when you create sales order lines that contain those items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="54f32-115">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="54f32-115">Issue resolution</span></span>

<span data-ttu-id="54f32-116">Ef það eru fleiri en einn viðskiptasamningur fyrir tiltekna dagsetningu er viðskiptasamningurinn sem er með lægsta verðið alltaf valinn.</span><span class="sxs-lookup"><span data-stu-id="54f32-116">If there is more than one trade agreement for a given date, the trade agreement that has the lowest price is always selected.</span></span> <span data-ttu-id="54f32-117">Til að fá frekari upplýsingar skal sækja eftirfarandi hvítbók: [Viðskiptasamningar í Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span><span class="sxs-lookup"><span data-stu-id="54f32-117">For more information, download the following white paper: [Trade agreements in Microsoft Dynamics AX 2012](https://www.axug.com/HigherLogic/System/DownloadDocumentFile.ashx?DocumentFileKey=3396a3a8-1f48-4d85-8cd6-5fa982f62e90).</span></span>

## <a name="can-i-link-a-purchase-order-to-a-sales-order-to-fulfill-demand"></a><span data-ttu-id="54f32-118">Get ég tengt innkaupapöntun við sölupöntunina til að uppfylla eftirspurn?</span><span class="sxs-lookup"><span data-stu-id="54f32-118">Can I link a purchase order to a sales order to fulfill demand?</span></span>

<span data-ttu-id="54f32-119">Hægt er að stofna innkaupapöntun úr sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="54f32-119">You can create a purchase order from a sales order.</span></span> <span data-ttu-id="54f32-120">Frekari upplýsingar er að finna í [Stofna innkaupapöntun úr sölupöntun](tasks/create-purchase-order-sales-order.md).</span><span class="sxs-lookup"><span data-stu-id="54f32-120">For more information, see [Create a purchase order from a sales order](tasks/create-purchase-order-sales-order.md).</span></span>

## <a name="i-cant-cancel-or-delete-a-return-order-or-a-sales-order"></a><span data-ttu-id="54f32-121">Ég get ekki hætt við eða eytt skilapöntun eða sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="54f32-121">I can't cancel or delete a return order or a sales order.</span></span>

<span data-ttu-id="54f32-122">Aðeins er hægt að hætta við sölupantanir og skilapantanir sem eru með stöðuna *Stofnuð*.</span><span class="sxs-lookup"><span data-stu-id="54f32-122">You can cancel only sales orders and return orders that are in a *Created* state.</span></span> <span data-ttu-id="54f32-123">Frekari upplýsingar er að finna í [Hætta við skilapöntun](../service-management/cancel-return-order.md).</span><span class="sxs-lookup"><span data-stu-id="54f32-123">For more information, see [Cancel a return order](../service-management/cancel-return-order.md).</span></span>

## <a name="when-i-try-to-cancel-a-sales-order-i-receive-a-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations-error"></a><span data-ttu-id="54f32-124">Þegar ég reyni að hætta við sölupöntun fæ ég upp villuna „Ekki er hægt að fjarlægja frátekningar vegna þess að búið er að stofna vinnu sem byggir á frátekningunum.“</span><span class="sxs-lookup"><span data-stu-id="54f32-124">When I try to cancel a sales order, I receive a "Reservations cannot be removed because there is work created which relies on the reservations" error.</span></span>

<span data-ttu-id="54f32-125">Villukóði WAX4661</span><span class="sxs-lookup"><span data-stu-id="54f32-125">Error code: WAX4661</span></span>

<span data-ttu-id="54f32-126">Ef vinna tengist sölupöntun er ekki hægt að hætta við sölupöntunina fyrr en hætt er við vinnu og hún bakfærð.</span><span class="sxs-lookup"><span data-stu-id="54f32-126">If work is associated with a sales order, you can't cancel the sales order until the work is canceled and reversed.</span></span> <span data-ttu-id="54f32-127">Þessi krafa gildir jafnvel þótt vinnan sem tengist sölupöntuninni sé lokuð.</span><span class="sxs-lookup"><span data-stu-id="54f32-127">This requirement applies even if the work that is associated with the sales order is closed.</span></span>

<span data-ttu-id="54f32-128">Til að laga þetta vandamál skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="54f32-128">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="54f32-129">Hættið við verkið og setjið birgðir aftur á æskilega staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="54f32-129">Cancel the work, and put inventory back into the desired location.</span></span> <span data-ttu-id="54f32-130">Farið á viðeigandi farm sölupöntunarinnar og veljið annaðhvort **Minnka tiltektarmagn** í farmlínunni eða **Bakfæra vinnu** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="54f32-130">Go to the relevant load of the sales order, and select either **Reduce picked quantity** on the load line or **Reverse work** on the Action Pane.</span></span>

    <span data-ttu-id="54f32-131">Verkið er nú með stöðuna *Hætt við* og ný birgðahreyfingarvinna er sjálfkrafa stofnuð og unnið úr til að setja birgðir aftur í staðsetninguna sem var lýst þegar bakfærslan var gerð.</span><span class="sxs-lookup"><span data-stu-id="54f32-131">The work now has a status of *Canceled*, and new inventory movement work is automatically created and processed to put inventory back into the location that was described at the time of reversal.</span></span>

2. <span data-ttu-id="54f32-132">Eyðið farminum.</span><span class="sxs-lookup"><span data-stu-id="54f32-132">Delete the load.</span></span> <span data-ttu-id="54f32-133">Sendingunni er einnig eytt.</span><span class="sxs-lookup"><span data-stu-id="54f32-133">The shipment is also deleted.</span></span>
3. <span data-ttu-id="54f32-134">Nú ætti að vera hægt að fara í sölupöntunina og hætta við hana.</span><span class="sxs-lookup"><span data-stu-id="54f32-134">You should now be able to go to the sales order and cancel it.</span></span>

## <a name="i-cant-cancel-an-intercompany-purchase-order-that-is-linked-to-a-sales-order"></a><span data-ttu-id="54f32-135">Ekki er hægt að hætta við samstæðuinnkaupapöntun sem er tengd við sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="54f32-135">I can't cancel an intercompany purchase order that is linked to a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="54f32-136">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="54f32-136">Issue description</span></span>

<span data-ttu-id="54f32-137">Ef reynt er að hætta við samstæðuinnkaupapöntun sem tengist sölupöntun, gætu eftirfarandi villuboð borist: „Ekki er hægt að minnka magn, þar sem eftirstöðvar uppfærðs magns breyta um formerki.“</span><span class="sxs-lookup"><span data-stu-id="54f32-137">If you try to cancel an intercompany purchase order that is linked to a sales order, you might receive the following error message: "Quantity cannot be reduced because the remaining update quantity changes sign."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="54f32-138">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="54f32-138">Issue resolution</span></span>

<span data-ttu-id="54f32-139">Þetta vandamál var lagfært í Microsoft Dynamics 365 Supply Chain Management útgáfu 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="54f32-139">This issue was fixed in Microsoft Dynamics 365 Supply Chain Management version 10.0.13.</span></span> <span data-ttu-id="54f32-140">Í þeirri útgáfu og nýrri útgáfum er nú hægt að hætta við samstæðuinnkaupapöntun sem tengist sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="54f32-140">In that version and later versions, you can now cancel an intercompany purchase order that is linked to a sales order.</span></span>

## <a name="can-i-restore-an-invoiced-sales-order-that-was-deleted"></a><span data-ttu-id="54f32-141">Get ég endurheimt reikningsfærða sölupöntun sem var eytt?</span><span class="sxs-lookup"><span data-stu-id="54f32-141">Can I restore an invoiced sales order that was deleted?</span></span>

### <a name="issue-description"></a><span data-ttu-id="54f32-142">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="54f32-142">Issue description</span></span>

<span data-ttu-id="54f32-143">Reikningsfærðri sölupöntun var eytt fyrir mistök og þú vilt endurheimta hana eða skoða upplýsingarnar um hana.</span><span class="sxs-lookup"><span data-stu-id="54f32-143">An invoiced sales order was deleted by mistake, and you want to restore it or view its details.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="54f32-144">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="54f32-144">Issue resolution</span></span>

<span data-ttu-id="54f32-145">Ef eydd sölupöntun hefur þegar verið reikningsfærð skal fara í **Viðskiptavinalykill \> Færslur \> Upprunalegt skjal \> Skoða upplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="54f32-145">If the deleted sales order has already been invoiced, go to **Customer account \> Transactions \> Original document \> View details**.</span></span> <span data-ttu-id="54f32-146">Finnið reikninginn sem leitað er að og veljið hann til að skoða upplýsingarnar.</span><span class="sxs-lookup"><span data-stu-id="54f32-146">Find the invoice that you're looking for, and select it to view its details.</span></span> <span data-ttu-id="54f32-147">Þessar upplýsingar innihalda tilvísun sölupöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="54f32-147">These details include the sales order reference.</span></span> <span data-ttu-id="54f32-148">Einnig ætti að vera hægt að fá aðgang að upplýsingum um sölupöntunina á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="54f32-148">You should also be able to access the sales order details from that page.</span></span>

## <a name="the-deadline-of-a-sales-order-header-cant-be-found-in-the-salesorderheaderv2entity-data-entity"></a><span data-ttu-id="54f32-149">Ekki er hægt að finna tímamörk sölupöntunarhauss í gagnaeiningunni SalesOrderHeaderV2Entity.</span><span class="sxs-lookup"><span data-stu-id="54f32-149">The deadline of a sales order header can't be found in the SalesOrderHeaderV2Entity data entity.</span></span>

<span data-ttu-id="54f32-150">Reiturinn fyrir tímamörk er ekki til í gagnaeiningunni *SalesOrderHeaderV2Entity*.</span><span class="sxs-lookup"><span data-stu-id="54f32-150">The deadline field doesn't exist on the *SalesOrderHeaderV2Entity* entity.</span></span>

## <a name="i-must-delete-orphaned-sales-order-records"></a><span data-ttu-id="54f32-151">Ég verð að eyða sölupöntunarfærslum án tilvísana.</span><span class="sxs-lookup"><span data-stu-id="54f32-151">I must delete orphaned sales order records.</span></span>

<span data-ttu-id="54f32-152">Til að hreinsa upp sölupöntunarfærslur án tilvísana skal keyra reglubundnu vinnsluna *Eyðing sölupöntunar* með því að fara á annan hvorn staðinn:</span><span class="sxs-lookup"><span data-stu-id="54f32-152">To clean up orphaned sales order records, run the *Sales order deletion* periodic job by going to either of the following places:</span></span>

- <span data-ttu-id="54f32-153">Sala og markaðssetning \> Reglubundnar vinnslur \> Hreinsun \> Eyða sölupöntunum</span><span class="sxs-lookup"><span data-stu-id="54f32-153">Sales and marketing \> Periodic tasks \> Clean up \> Delete sales orders</span></span>
- <span data-ttu-id="54f32-154">Smásala og viðskipti \> Upplýsingatækni smásölu og viðskipta \> Hreinsun \> Eyða sölupöntunum</span><span class="sxs-lookup"><span data-stu-id="54f32-154">Retail and commerce \> Retail and commerce IT \> Clean up \> Delete sales orders</span></span>

## <a name="is-there-a-way-to-calculate-commissions-on-invoices-that-have-already-been-posted"></a><span data-ttu-id="54f32-155">Er leið til að reikna út þóknanir á reikningum sem hafa þegar verið bókaðir?</span><span class="sxs-lookup"><span data-stu-id="54f32-155">Is there a way to calculate commissions on invoices that have already been posted?</span></span>

<span data-ttu-id="54f32-156">Supply Chain Management styður ekki útreikning á þóknunum fyrir bókaða reikninga sem stendur.</span><span class="sxs-lookup"><span data-stu-id="54f32-156">Supply Chain Management doesn't currently support the calculation of commissions for posted invoices.</span></span>

## <a name="a-bundle-item-isnt-supported-in-an-intercompany-process"></a><span data-ttu-id="54f32-157">Búntvara er ekki studd í samstæðuferli.</span><span class="sxs-lookup"><span data-stu-id="54f32-157">A bundle item isn't supported in an intercompany process.</span></span>

<span data-ttu-id="54f32-158">Búntvaran er ekki tiltæk fyrir innkaupapöntunina því að ef þú skoðar sölupöntunarlínurnar fyrir búntvöruna muntu taka eftir því að magnið er *0* (núll) og staðan er *Afturkölluð*.</span><span class="sxs-lookup"><span data-stu-id="54f32-158">The bundle item isn't available for the purchase order because, if you examine the sales order lines for the bundle item, you will notice that the quantity is *0* (zero) and the status is *Canceled*.</span></span> <span data-ttu-id="54f32-159">Þessi hegðun er samkvæmt hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="54f32-159">This behavior is by design.</span></span> <span data-ttu-id="54f32-160">Sölupöntunin kaupir aðeins þætti búntvörunnar.</span><span class="sxs-lookup"><span data-stu-id="54f32-160">The sales order buys only the components of the bundle item.</span></span> <span data-ttu-id="54f32-161">Hún kaupir ekki búntvöruna sjálfa.</span><span class="sxs-lookup"><span data-stu-id="54f32-161">It doesn't buy the bundle item itself.</span></span>

<span data-ttu-id="54f32-162">Ef kaupa þarf búnt, þarf að hafa í huga hvort merkja eigi það sem búntvöru, þar sem þessi virkni er hönnuð fyrir aðstæður tekjuskráningar.</span><span class="sxs-lookup"><span data-stu-id="54f32-162">If you must buy a bundle, consider whether you have to mark it as bundle item, because this functionality is designed for revenue recognition scenarios.</span></span> <span data-ttu-id="54f32-163">Frekari upplýsingar um búntvörur er að finna í [Búnt](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span><span class="sxs-lookup"><span data-stu-id="54f32-163">For more information about bundle items, see [Bundles](../../finance/accounts-receivable/revenue-recognition-setup.md#bundles).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]