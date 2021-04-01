---
title: Villuleita verkflæði innkaupa og aðfanga
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með verkflæði innkaupa og aðfanga.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: d5d688c5769a62580e48908117d0562b26eab10a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222826"
---
# <a name="troubleshoot-procurement-and-sourcing-workflows"></a><span data-ttu-id="5b204-103">Villuleita verkflæði innkaupa og aðfanga</span><span class="sxs-lookup"><span data-stu-id="5b204-103">Troubleshoot procurement and sourcing workflows</span></span>

<span data-ttu-id="5b204-104">Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með verkflæði innkaupa og aðfanga.</span><span class="sxs-lookup"><span data-stu-id="5b204-104">This topic describes how to fix issues that you might encounter while you work with procurement and sourcing workflows.</span></span>

## <a name="error-when-re-submitting-a-purchase-order-to-the-workflow-after-a-change-changes-to-purchase-order-x-are-allowed-only-in-a-draft-state-when-change-management-is-activated"></a><span data-ttu-id="5b204-105">Villa þegar innkaupapöntun er endursend í verkflæðið eftir breytingu: „Breytingar á innkaupapöntun X eru aðeins leyfðar í stöðunni Drög þegar breytingastjórnun er virkjuð“</span><span class="sxs-lookup"><span data-stu-id="5b204-105">Error when re-submitting a purchase order to the workflow after a change: "Changes to purchase order X are allowed only in a Draft state when change management is activated"</span></span>

<span data-ttu-id="5b204-106">Þetta vandamál á sér aðeins stað ef innkaupapöntunin var með stöðuna *Staðfest* áður en óskað var eftir breytingum.</span><span class="sxs-lookup"><span data-stu-id="5b204-106">This issue occurs only if the purchase order was in a *Confirmed* state before you requested changes.</span></span> <span data-ttu-id="5b204-107">Ef beðið er um breytingar á meðan innkaupapöntunin er með stöðuna *Samþykkt*, er hægt að vinna úr verkflæðinu.</span><span class="sxs-lookup"><span data-stu-id="5b204-107">If you request changes while the purchase order is in an *Approved* state, the workflow can be processed successfully.</span></span>

### <a name="error-description"></a><span data-ttu-id="5b204-108">Villulýsing</span><span class="sxs-lookup"><span data-stu-id="5b204-108">Error description</span></span>

<span data-ttu-id="5b204-109">Eftirfarandi villa kemur upp í verkflæðinu þegar innkaupapöntun er send aftur eftir breytingu:</span><span class="sxs-lookup"><span data-stu-id="5b204-109">The following error occurs in the workflow when a purchase order is resubmitted after a change:</span></span>

> <span data-ttu-id="5b204-110">Stöðvað (villa): X++ undantekning: Breytingar á innkaupapöntun PO0000569 eru aðeins leyfðar í stöðunni „Drög“ þegar breytingastjórnun er virkjuð á</span><span class="sxs-lookup"><span data-stu-id="5b204-110">Stopped (error): X++ Exception: Changes to purchase order PO0000569 are only allowed in state Draft when change management is activated at</span></span><br>
<span data-ttu-id="5b204-111">SysWorkflowParticipantProvider-resolve</span><span class="sxs-lookup"><span data-stu-id="5b204-111">SysWorkflowParticipantProvider-resolve</span></span><br>
<span data-ttu-id="5b204-112">SysWorkflowParticipantProvider-resolveParticipants</span><span class="sxs-lookup"><span data-stu-id="5b204-112">SysWorkflowParticipantProvider-resolveParticipants</span></span><br>
<span data-ttu-id="5b204-113">SysWorkflowServiceProvider-resolveParticipant</span><span class="sxs-lookup"><span data-stu-id="5b204-113">SysWorkflowServiceProvider-resolveParticipant</span></span><br>
<span data-ttu-id="5b204-114">SysWorkflowQueue-resume</span><span class="sxs-lookup"><span data-stu-id="5b204-114">SysWorkflowQueue-resume</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5b204-115">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="5b204-115">Issue resolution</span></span>

<span data-ttu-id="5b204-116">Þetta vandamál getur komið upp vegna ósamræmis í dreifingum innkaupapantana.</span><span class="sxs-lookup"><span data-stu-id="5b204-116">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="5b204-117">Til að afblokka þetta vandamál og endurstilla innkaupapöntunina á stöðuna *Drög* skal fara í **Innkaup og aðföng \> Reglubundnar vinnslur \> Hreinsun \> Endurstilling á dreifingu innkaupapöntunar**.</span><span class="sxs-lookup"><span data-stu-id="5b204-117">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="5b204-118">Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Leysa úr dreifingarvillum innkaupapöntunar í Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="5b204-118">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

<span data-ttu-id="5b204-119">Vandamálið verður lagað í [þessari grein Microsoft Knowledge](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span><span class="sxs-lookup"><span data-stu-id="5b204-119">The issue will be fixed through [this Microsoft Knowledge Base (KB) article](https://msdyneng.visualstudio.com/FinOps/_workitems/edit/467138).</span></span>

## <a name="one-or-more-accounting-distributions-are-either-over-distributed-or-under-distributed"></a><span data-ttu-id="5b204-120">Ein eða fleiri dreifingar á fjárhagsupphæð eru annaðhvort yfir- eða undirdreifðar.</span><span class="sxs-lookup"><span data-stu-id="5b204-120">One or more accounting distributions are either over-distributed or under-distributed.</span></span>

<span data-ttu-id="5b204-121">Þetta vandamál getur komið upp vegna ósamræmis í dreifingum innkaupapantana.</span><span class="sxs-lookup"><span data-stu-id="5b204-121">This issue can occur because of inconsistency in purchase order distributions.</span></span>

<span data-ttu-id="5b204-122">Til að afblokka þetta vandamál og endurstilla innkaupapöntunina á stöðuna *Drög* skal fara í **Innkaup og aðföng \> Reglubundnar vinnslur \> Hreinsun \> Endurstilling á dreifingu innkaupapöntunar**.</span><span class="sxs-lookup"><span data-stu-id="5b204-122">To unblock this issue and reset the purchase order to a *Draft* state, go to **Procurement and sourcing \> Periodic tasks \> Clean up \> Purchase order distribution reset**.</span></span> <span data-ttu-id="5b204-123">Frekari upplýsingar er að finna í eftirfarandi bloggfærslu: [Leysa úr dreifingarvillum innkaupapöntunar í Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span><span class="sxs-lookup"><span data-stu-id="5b204-123">For more information, see the following blog post: [Resolve PO distribution errors in Dynamics 365 Supply Chain Management](https://cloudblogs.microsoft.com/dynamics365/it/2020/08/12/resolve-po-distribution-errors-in-dynamics-365-supply-chain-management/).</span></span>

## <a name="if-a-delivery-remainder-is-canceled-on-a-purchase-order-where-change-management-is-turned-on-the-purchase-order-goes-to-a-confirmed-state"></a><span data-ttu-id="5b204-124">Ef hætt er við eftirstöðvar afhendingar í innkaupapöntun þar sem kveikt er á breytingastjórnun, fer innkaupapöntunin í stöðuna Staðfest.</span><span class="sxs-lookup"><span data-stu-id="5b204-124">If a delivery remainder is canceled on a purchase order where change management is turned on, the purchase order goes to a Confirmed state.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5b204-125">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="5b204-125">Issue description</span></span>

<span data-ttu-id="5b204-126">Fyrir innkaupapöntun sem heyrir undir breytingastjórnun, ef eina breytingin sem beðið er um er afturköllun á eftirstöðvum afhendingar á einni eða fleiri línum, fer innkaupapöntunin beint í stöðuna *Staðfest* þegar hún er samþykkt og engin færslubók verður stofnuð.</span><span class="sxs-lookup"><span data-stu-id="5b204-126">For a purchase order that is subject to change management, if the only change that is requested is the cancellation of a delivery remainder on one or more of the lines, the purchase order will go directly to a *Confirmed* state when it's approved, and no journal will be created.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5b204-127">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="5b204-127">Issue resolution</span></span>

<span data-ttu-id="5b204-128">Afturköllun á eftirstöðvum afhendingar hefur ekki áhrif á innihald staðfestingarbókar.</span><span class="sxs-lookup"><span data-stu-id="5b204-128">Cancellation of a delivery remainder doesn't affect the contents of the confirmation journal.</span></span> <span data-ttu-id="5b204-129">Nota ætti þessa virkni þegar búið er að taka á móti línunni að hluta til og hætta ætti við eftirstandandi magn í vinnsluskrefinu eftir að innkaupapöntunin hefur verið staðfest hjá lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="5b204-129">This functionality should be used when the line has been partially received, and the remainder quality should be canceled in the process step after the purchase order has been confirmed with the vendor.</span></span>

<span data-ttu-id="5b204-130">Ef þetta á að koma fram á staðfestingu innkaupapöntunarinnar ætti að leiðrétta magnið í innkaupapöntunarlínunni svo staðfestingin verði nauðsynleg.</span><span class="sxs-lookup"><span data-stu-id="5b204-130">If this should be reflected on the purchase order confirmation, the quantity should be adjusted on the purchase order line so that the confirmation will be required.</span></span> <span data-ttu-id="5b204-131">Að öðrum kosti, ef ekkert hefur verið móttekið í línunni, er hægt að fjarlægja magnið.</span><span class="sxs-lookup"><span data-stu-id="5b204-131">Alternatively, if nothing has been received on the line, the quantity can be removed.</span></span> <span data-ttu-id="5b204-132">Í þessu tilfelli þarf að staðfesta aftur.</span><span class="sxs-lookup"><span data-stu-id="5b204-132">In this case, reconfirmation will be required.</span></span>

## <a name="canceled-purchase-orders-appear-in-the-draft-list-in-the-purchase-order-preparation-workspace"></a><span data-ttu-id="5b204-133">Afturkallaðar innkaupapantanir birtast í listanum yfir drög á undirbúningssvæði innkaupapöntunar.</span><span class="sxs-lookup"><span data-stu-id="5b204-133">Canceled purchase orders appear in the draft list in the Purchase order preparation workspace.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5b204-134">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="5b204-134">Issue description</span></span>

<span data-ttu-id="5b204-135">Þegar búið er að hætta við innkaupapantanir sem voru með stöðuna *Staðfest*, sjást afturkölluðu innkaupapantanir ennþá í listanum yfir drög að innkaupapöntunum á vinnusvæðinu **Undirbúningur innkaupapöntunar**.</span><span class="sxs-lookup"><span data-stu-id="5b204-135">After you cancel purchase orders that were in a *Confirmed* state, the canceled purchase orders still appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5b204-136">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="5b204-136">Issue resolution</span></span>

<span data-ttu-id="5b204-137">Þetta vandamál á sér aðeins stað fyrir innkaupapantanir sem heyra undir breytingastjórnun.</span><span class="sxs-lookup"><span data-stu-id="5b204-137">This issue occurs only for purchase orders that are subject to change management.</span></span> <span data-ttu-id="5b204-138">Það á sér stað vegna þess að afturköllunin er talin breyta sem þarf að samþykkja.</span><span class="sxs-lookup"><span data-stu-id="5b204-138">It occurs because the cancellation is considered a change that must be approved.</span></span> <span data-ttu-id="5b204-139">Hægt er að framkvæma samþykkið sjálfkrafa af kerfinu.</span><span class="sxs-lookup"><span data-stu-id="5b204-139">The approval can be done automatically by the system.</span></span> <span data-ttu-id="5b204-140">Þess vegna gengur ferlið út á að senda afturkallaða innkaupapöntun til samþykktarverkflæðis þannig að hún geti fengið stöðuna *Samþykkt*.</span><span class="sxs-lookup"><span data-stu-id="5b204-140">Therefore, the process is to submit the canceled purchase order to the approval workflow so that it can go to an *Approved* state.</span></span> <span data-ttu-id="5b204-141">Á þessu stigi sést innkaupapöntunin ekki lengur í listanum yfir drög að innkaupapöntunum á vinnusvæðinu **Undirbúningur innkaupapöntunar**.</span><span class="sxs-lookup"><span data-stu-id="5b204-141">At that point, the purchase order will no longer appear in the list of draft purchase orders in the **Purchase order preparation** workspace.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]