---
title: Villuleita innkaupapantanir
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með innkaupapantanir.
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
ms.openlocfilehash: 234458f865e37a2d962aee8ab218b9521847081d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430756"
---
# <a name="troubleshoot-purchase-orders"></a><span data-ttu-id="7bbeb-103">Villuleita innkaupapantanir</span><span class="sxs-lookup"><span data-stu-id="7bbeb-103">Troubleshoot purchase orders</span></span>

<span data-ttu-id="7bbeb-104">Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-104">This topic describes how to fix issues that you might encounter while you work with purchase orders.</span></span>

## <a name="an-action-can-be-completed-only-after-the-line-number-is-fully-distributed"></a><span data-ttu-id="7bbeb-105">Aðeins er hægt að ljúka aðgerð eftir að línunúmeri er að fullu dreift.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-105">An action can be completed only after the line number is fully distributed.</span></span>

<span data-ttu-id="7bbeb-106">Þetta vandamál getur komið upp vegna ósamræmis í dreifingum innkaupapantana.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-106">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="7bbeb-107">Til að afblokka þetta vandamál og endurstilla innkaupapöntunina á stöðuna *Drög* skal fara í **Innkaup og aðföng \> Reglubundnar vinnslur \> Hreinsun \> Endurstilling á dreifingu innkaupapöntunar**.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-107">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="7bbeb-108">Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Leysa úr dreifingarvillum innkaupapöntunar í Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="7bbeb-108">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="when-purchase-orders-are-imported-through-data-management-purchase-order-line-numbers-dont-follow-the-increment-that-defined-in-system-parameters"></a><span data-ttu-id="7bbeb-109">Þegar innkaupapantanir eru fluttar inn í gegnum gagnastjórnun, fylgja númer innkaupapöntunarlínu ekki hækkun sem er skilgreint í kerfisfæribreytum.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-109">When purchase orders are imported through data management, purchase order line numbers don't follow the increment that defined in system parameters.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7bbeb-110">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="7bbeb-110">Issue description</span></span>

<span data-ttu-id="7bbeb-111">Sjálfgefið er að línunúmer sem eru búin til sjálfkrafa fyrir innkaupapöntunarlínur sem eru fluttar inn í gegnum gagnaeininguna *Innkaupapöntunarlínur V2* noti ekki línunúmerahækkun kerfisins sem er tilgreind í kerfisfæribreytum.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-111">By default, automatically generated line numbers for purchase order lines that are imported through the *Purchase order lines V2* data entity don't use the system line number increment that is specified in system parameters.</span></span> <span data-ttu-id="7bbeb-112">Ef innkaupapöntun er búin til handvirkt og línum bætt við í gegnum notandaviðmótið, hækka línunúmerin á réttan hátt.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-112">If you manually create a purchase order and add lines through the user interface (UI), the line numbers are incremented correctly.</span></span> <span data-ttu-id="7bbeb-113">Hins vegar ef gagnastjórnunarramminn (DMF) er notaður, hækka þau ekki á réttan hátt.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-113">However, if you use the Data management framework (DMF), they aren't incremented correctly.</span></span>

<span data-ttu-id="7bbeb-114">Þetta vandamál á sér stað vegna þess að þegar innflutningslínur eru fluttar inn í gegnum DMF, ef línunúmerum hefur ekki þegar verið úthlutað á innflutta einingu, notar kerfið DMF-aðferð til að úthluta þeim.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-114">This issue occurs because, when you import lines via DMF, if line numbers aren't already assigned in the imported entity, the system uses DMF's method for assigning them.</span></span> <span data-ttu-id="7bbeb-115">Línunúmer hækka alltaf um einn með þessari aðferð.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-115">That method always increments line numbers by one.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="7bbeb-116">Lausn á vandamálinu</span><span class="sxs-lookup"><span data-stu-id="7bbeb-116">Issue workaround</span></span>

<span data-ttu-id="7bbeb-117">Gangið úr skugga um að æskileg línunúmer séu þegar gefin upp í línunúmerareitum gagnaeiningarinnar þegar innkaupapöntunarlínurnar eru fluttar inn.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-117">Make sure that the desired line numbers are already given in the data entity line number fields when you import the purchase order lines.</span></span> <span data-ttu-id="7bbeb-118">Í þessu tilfelli skrifar DMF ekki yfir línunúmerin.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-118">In this case, DMF won't overwrite the line numbers.</span></span>

## <a name="a-default-tax-group-and-a-default-cash-discount-arent-filled-in-from-the-invoice-account"></a><span data-ttu-id="7bbeb-119">Sjálfgefinn skattflokkur og sjálfgefinn staðgreiðsluafsláttur eru ekki fyllt út í reikningslyklinum.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-119">A default tax group and a default cash discount aren't filled in from the invoice account.</span></span>

<span data-ttu-id="7bbeb-120">Ef reikningslykill er notaður sem er frábrugðinn lykli viðskiptavinar, er ekki fyllt út í sjálfgefinn skattflokk og sjálfgefinn staðgreiðsluafslátt í reikningslyklinum þegar innkaupapöntun er búin til.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-120">If you're using an invoice account that differs from the customer account, a default tax group and a default cash discount aren't filled in from the invoice account when a purchase order is created.</span></span>

<span data-ttu-id="7bbeb-121">Þessi hegðun er samkvæmt hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-121">This behavior is by design.</span></span> <span data-ttu-id="7bbeb-122">Sjálfgefin gildi fyrir skattflokkinn, staðgreiðsluafslætti og aðrar verðupplýsingar byggja á viðskiptavinalyklinum, ekki reikningslyklinum.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-122">The default values for the tax group, cash discounts, and other price information are based on the customer account, not the invoice account.</span></span>

## <a name="i-receive-an-object-reference-not-set-error-during-purchase-order-confirmation-or-an-exception-has-been-thrown-by-the-target-of-an-invocation-exception-occurs-during-vendor-invoice-posting"></a><span data-ttu-id="7bbeb-123">Ég fæ upp villuna „Tilvísun hlutar ekki stillt“ við staðfestingu á innkaupapöntun, eða undantekningin „Exception has been thrown by the target of an invocation“ kemur upp við bókun lánardrottnareiknings.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-123">I receive an "Object reference not set" error during purchase order confirmation, or an "Exception has been thrown by the target of an invocation" exception occurs during vendor invoice posting.</span></span>

<span data-ttu-id="7bbeb-124">Þetta vandamál getur komið upp vegna ósamræmis í dreifingum innkaupapantana.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-124">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="7bbeb-125">Til að afblokka þetta vandamál og endurstilla innkaupapöntunina á stöðuna *Drög* skal fara í **Innkaup og aðföng \> Reglubundnar vinnslur \> Hreinsun \> Endurstilling á dreifingu innkaupapöntunar**.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-125">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="7bbeb-126">Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Leysa úr dreifingarvillum innkaupapöntunar í Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="7bbeb-126">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="7bbeb-127">Ein eða fleiri dreifingar á fjárhagsupphæð eru annaðhvort yfir- eða undirdreifðar.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-127">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7bbeb-128">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="7bbeb-128">Issue description</span></span>

<span data-ttu-id="7bbeb-129">Eftirfarandi villa kemur upp: „Ein eða fleiri dreifingar á fjárhagsupphæð er annaðhvort yfir- eða undirdreifðar.“</span><span class="sxs-lookup"><span data-stu-id="7bbeb-129">You receive the following error: "One or more accounting distributions is either over-distributed or under-distributed."</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7bbeb-130">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="7bbeb-130">Issue resolution</span></span>

<span data-ttu-id="7bbeb-131">Þetta vandamál getur komið upp vegna ósamræmis í dreifingum innkaupapantana.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-131">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="7bbeb-132">Til að afblokka þetta vandamál og endurstilla innkaupapöntunina á stöðuna *Drög* skal fara í **Innkaup og aðföng \> Reglubundnar vinnslur \> Hreinsun \> Endurstilling á dreifingu innkaupapöntunar**.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-132">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="7bbeb-133">Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Leysa úr dreifingarvillum innkaupapöntunar í Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="7bbeb-133">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="can-i-show-only-purchase-orders-that-i-created"></a><span data-ttu-id="7bbeb-134">Get ég birt aðeins innkaupapantanir sem ég stofnaði?</span><span class="sxs-lookup"><span data-stu-id="7bbeb-134">Can I show only purchase orders that I created?</span></span>

<span data-ttu-id="7bbeb-135">Þessi virkni er ekki tiltæk sem stendur.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-135">This functionality isn't currently available.</span></span>

## <a name="can-i-reserve-inventory-and-create-transactions-against-registered-inventory-on-a-purchase-order"></a><span data-ttu-id="7bbeb-136">Get ég tekið frá birgðir og stofnað færslur á móti skráðum birgðum í innkaupapöntun?</span><span class="sxs-lookup"><span data-stu-id="7bbeb-136">Can I reserve inventory and create transactions against registered inventory on a purchase order?</span></span>

### <a name="issue-description"></a><span data-ttu-id="7bbeb-137">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="7bbeb-137">Issue description</span></span>

<span data-ttu-id="7bbeb-138">Jafnvel þegar vörur eru með stöðuna *Skráð* í innkaupapöntun, er enn hægt að taka frá birgðirnar.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-138">Even when items are in a *Registered* state on a purchase order, you can still reserve the inventory.</span></span> <span data-ttu-id="7bbeb-139">Með öðrum orðum er hægt að stofna færslur gagnvart skráðum birgðum.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-139">In other words, you can create transactions against the registered inventory.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="7bbeb-140">Framkallaðu vandamálið</span><span class="sxs-lookup"><span data-stu-id="7bbeb-140">Reproduce the issue</span></span>

<span data-ttu-id="7bbeb-141">Eftirfarandi ferli sýnir eina leið til að endurtaka málið.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-141">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="7bbeb-142">Stofna innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-142">Create a purchase order.</span></span>
2. <span data-ttu-id="7bbeb-143">Skráið innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-143">Register the purchase order line.</span></span>
3. <span data-ttu-id="7bbeb-144">Takið eftir því að hægt er að mynda frátekningar og færslur gagnvart skráðum birgðum.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-144">Notice that you can generate reservations or transactions against the registered inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7bbeb-145">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="7bbeb-145">Issue resolution</span></span>

<span data-ttu-id="7bbeb-146">Þessi hegðun er samkvæmt hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-146">This behavior is by design.</span></span> <span data-ttu-id="7bbeb-147">Væntingin er sú að skráðar vörur séu efnislega komnar í vöruhúsið eða birgðirnar og að hægt sé þar af leiðandi að taka þær frá.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-147">The expectation is that the registered items have physically arrived in the warehouse or inventory, and that they are therefore available for reservation.</span></span>

## <a name="purchase-orders-dont-reflect-the-language-settings-of-the-legal-entity"></a><span data-ttu-id="7bbeb-148">Innkaupapantanir endurspegla ekki tungumálastillingar lögaðilans.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-148">Purchase orders don't reflect the language settings of the legal entity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7bbeb-149">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="7bbeb-149">Issue description</span></span>

<span data-ttu-id="7bbeb-150">Afurðarheitið á innkaupapöntun er sýnt á tungumáli kerfisins í staðinn fyrir tungumálið sem er stillt fyrir lögaðilann þar sem innkaupapöntunin var búin til.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-150">The product name on a purchase order is shown in the system language instead of the language that is set for the legal entity where the purchase order was created.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="7bbeb-151">Framkallaðu vandamálið</span><span class="sxs-lookup"><span data-stu-id="7bbeb-151">Reproduce the issue</span></span>

<span data-ttu-id="7bbeb-152">Eftirfarandi ferli sýnir eina leið til að endurtaka málið.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-152">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="7bbeb-153">Stillið kerfistungumálið á *EN-US* (bandaríska ensku).</span><span class="sxs-lookup"><span data-stu-id="7bbeb-153">Set the system language to *EN-US* (US English).</span></span>
1. <span data-ttu-id="7bbeb-154">Gangið úr skugga um að það sé til afurð þar sem tungumálin *EN-US* og *DE* (þýska) eru notuð fyrir þýðingar á afurðarheiti.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-154">Make sure that there is a product where the *EN-US* and *DE* (German) languages are maintained for translations of the product name.</span></span>
1. <span data-ttu-id="7bbeb-155">Breytið tungumáli fyrir lögaðila í *DE*.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-155">Change the language of a legal entity to *DE*.</span></span>
1. <span data-ttu-id="7bbeb-156">Í lögaðilanum þar sem *DE* er stillt sem tungumál skal stofna innkaupapöntun sem inniheldur afurðina.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-156">In the legal entity where *DE* is set as the language, create a purchase order that includes the product.</span></span>
1. <span data-ttu-id="7bbeb-157">Takið eftir því að afurðarheitið er enn sýnt á bandarískri ensku (kerfistungumálinu).</span><span class="sxs-lookup"><span data-stu-id="7bbeb-157">Notice that the product name is still shown in US English (the system language).</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7bbeb-158">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="7bbeb-158">Issue resolution</span></span>

<span data-ttu-id="7bbeb-159">Þessi hegðun er samkvæmt hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-159">This behavior is by design.</span></span> <span data-ttu-id="7bbeb-160">Í innkaupapöntunum er afurðin alltaf sýnd á tungumáli kerfisins.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-160">On purchase orders, the product is always shown in the system language.</span></span> <span data-ttu-id="7bbeb-161">Tungumál innkaupapantana er notað þegar staðfestingarbók er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-161">The purchase order language is used when a confirmation journal is created.</span></span>

## <a name="the-approved-vendor-list-by-product-entity-doesnt-allow-the-effective-date-to-be-changed"></a><span data-ttu-id="7bbeb-162">Listi yfir samþykkta lánardrottna eftir afurðareiningu leyfir ekki að gildisdagsetningunni sé breytt.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-162">The Approved vendor list by product entity doesn't allow the effective date to be changed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7bbeb-163">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="7bbeb-163">Issue description</span></span>

<span data-ttu-id="7bbeb-164">Afurð er með samþykktan lánardrottin sem er með t.d. gildisdagsetningu 11. janúar 2018 (*11/01/2018*), og lokadaginn *Aldrei*.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-164">A product has an approved vendor that has, for example, an effective date of January 11, 2018 (*01/11/2018*), and an expiration date of *Never*.</span></span> <span data-ttu-id="7bbeb-165">Ef reynt er að breyta gildisdagsetningunni í 10. janúar 2018 (*10/01/2018*) eða 12. janúar 2018 (*12/01/2018*) kemur upp eftirfarandi villu:</span><span class="sxs-lookup"><span data-stu-id="7bbeb-165">If you try to change the effective date to January 10, 2018 (*01/10/2018*), or January 12, 2018 (*01/12/2018*), you receive the following error:</span></span>

> <span data-ttu-id="7bbeb-166">Ekki tókst að stofna færslu í lista yfir samþykkta birgja (PdsApproveVendorList).</span><span class="sxs-lookup"><span data-stu-id="7bbeb-166">Cannot create a record in Approved supplier list (PdsApproveVendorList).</span></span> <span data-ttu-id="7bbeb-167">Gildið 'Lokadagsetning' þarf að vera stærra en eða jafnt og gildið fyrir ‚Gildisdagsetning‘.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-167">The 'Expiration' value needs to be greater than or equal to the 'Effective' value.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7bbeb-168">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="7bbeb-168">Issue resolution</span></span>

<span data-ttu-id="7bbeb-169">Aðeins er hægt að framlengja tímabilið þar sem lánardrottinn hefur verið samþykktur.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-169">You can only extend the period that the vendor is approved for.</span></span> <span data-ttu-id="7bbeb-170">Eftirfarandi reglur gilda:</span><span class="sxs-lookup"><span data-stu-id="7bbeb-170">The following rules apply:</span></span>

- <span data-ttu-id="7bbeb-171">Til að breyta gildisdagsetningu þannig að hún sé á undan fyrirliggjandi færslum (tímabilum) fyrir lánardrottin vörunnar, verður lokadagur nýja tímabilsins að vera á undan öllum lokadagsetningum í fyrirliggjandi færslum.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-171">To change the effective date so that it's earlier than any of the existing records (periods) for the item vendor, the expiration date of the new period must be before all the expiration dates in the existing records.</span></span>
- <span data-ttu-id="7bbeb-172">Til að breyta lokadagsetningunni þannig að hún verði síðar en á fyrirliggjandi tímabilum verður gildisdagsetningin að vera á eftir síðustu lokadagsetningunni í fyrirliggjandi færslu.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-172">To change the expiration date so that it's later than any of the existing periods, the effective date must be after the latest expiration date in any existing record.</span></span>
- <span data-ttu-id="7bbeb-173">Til að draga úr heildartímabilinu sem lánardrottinn hefur verið samþykktur fyrir, þarf að eyða eða breyta fyrirliggjandi færslum.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-173">To reduce the overall period that the vendor is approved for, you must delete or modify existing records.</span></span> <span data-ttu-id="7bbeb-174">Að öðrum kosti er hægt að nota rofann **stytta** meðan á innflutningi stendur.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-174">Alternatively, you can use the **truncate** switch during import.</span></span> <span data-ttu-id="7bbeb-175">Þessi rofi eyðir öllum fyrirliggjandi færslum í töflunni fyrir samþykkta lánardrottna eftir vöru.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-175">This switch deletes all existing records in the table for approved vendors by item.</span></span>

<span data-ttu-id="7bbeb-176">Fyrir dæmið sem lýst er í útgáfulýsingunni þar sem færsla er með gildisdagsetningu *11/01/2018* og lokadag *Aldrei*, er hægt að flytja inn nýja færslu sem er með gildisdagsetningu *10/01/2018* og lokadagsetningu *Aldrei*.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-176">For the example scenario that is described in the issue description, where a record has an effective date of *01/11/2018* and an expiration date of *Never*, you can import a new record that has an effective date of *01/10/2018* and an expiration date of *Never*.</span></span> <span data-ttu-id="7bbeb-177">Hins vegar er ekki hægt að stytta tímabilið þannig að gildisdagsetningin uppfærist í *12/01/2018* í gegnum gagnastjórnun.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-177">However, you can't reduce the period so that the effective date is updated to *01/12/2018* via data management.</span></span> <span data-ttu-id="7bbeb-178">Þú verður að gera þessa breytingu í gegnum notandaviðmótið.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-178">You must make this change through the UI.</span></span>

## <a name="after-i-change-the-delivery-address-on-a-purchase-order-header-the-delivery-nameisnt-synced"></a><span data-ttu-id="7bbeb-179">Eftir að ég breyti afhendingaraðsetrinu í haus innkaupapöntunar er afhendingarheitið ekki samstillt.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-179">After I change the delivery address on a purchase order header, the delivery name isn't synced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="7bbeb-180">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="7bbeb-180">Issue description</span></span>

<span data-ttu-id="7bbeb-181">Aðsetrið í haus innkaupapöntunar er uppfært í aðsetur sem er ekki afhendingaraðsetur.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-181">The address on the header of a purchase order is updated to an address that isn't a delivery address.</span></span> <span data-ttu-id="7bbeb-182">Þótt aðsetrið sé uppfært í innkaupapöntuninni er afhendingarheitið ekki uppfært samkvæmt uppfærða aðsetrinu.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-182">Although the address is updated on the purchase order, the delivery name isn't updated based on the updated address.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="7bbeb-183">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="7bbeb-183">Issue resolution</span></span>

<span data-ttu-id="7bbeb-184">Þessi hegðun er samkvæmt hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-184">This behavior is by design.</span></span> <span data-ttu-id="7bbeb-185">Valið aðsetur verður að vera flokkað sem afhendingaraðsetur.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-185">The selected address must be classified as a delivery address.</span></span> <span data-ttu-id="7bbeb-186">Að öðrum kosti er afhendingarheitið ekki uppfært út frá völdu aðsetri.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-186">Otherwise, the delivery name isn't updated based on the selected address.</span></span>

## <a name="can-i-find-the-user-who-canceled-a-purchase-order"></a><span data-ttu-id="7bbeb-187">Get ég fundið notandann sem afturkallaði innkaupapöntunina?</span><span class="sxs-lookup"><span data-stu-id="7bbeb-187">Can I find the user who canceled a purchase order?</span></span>

<span data-ttu-id="7bbeb-188">Þessar upplýsingar eru aðeins raktar ef innkaupapöntunin fellur undir breytingastjórnun.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-188">This information is tracked only if the purchase order is subject to change management.</span></span> <span data-ttu-id="7bbeb-189">Ef breytingastjórnun er notuð, er hægt að sjá hver sendi inn breytinguna (afturköllunina) og hver samþykkti hana.</span><span class="sxs-lookup"><span data-stu-id="7bbeb-189">If you use change management, you can see who submitted the change (the cancellation), and who approved it.</span></span>
