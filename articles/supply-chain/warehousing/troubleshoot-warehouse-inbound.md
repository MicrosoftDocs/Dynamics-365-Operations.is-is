---
title: Úrræðaleit fyrir vöruhúsaaðgerðir á innleið
description: Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með vöruhúsaaðgerðir á innleið i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f0ea2ee208cdbb8f9fa6668bbcb6e15252a7c1b1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828227"
---
# <a name="troubleshoot-inbound-warehouse-operations"></a><span data-ttu-id="5b204-103">Úrræðaleit fyrir vöruhúsaaðgerðir á innleið</span><span class="sxs-lookup"><span data-stu-id="5b204-103">Troubleshoot inbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b204-104">Í þessu efnisatriði er því lýst hvernig á að laga vandamál sem kunna að koma upp þegar unnið er með vöruhúsaaðgerðir á innleið i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="5b204-104">This topic describes how to fix common issues that you might encounter while you work with inbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-quality-order-1-has-been-generated-cluster-profile-could-not-be-found-please-check-your-configuration"></a><span data-ttu-id="5b204-105">Ég fæ eftirfarandi villuskilaboð: „Gæðapöntun %1 var búin til.</span><span class="sxs-lookup"><span data-stu-id="5b204-105">I receive the following error message: "Quality order %1 has been generated.</span></span> <span data-ttu-id="5b204-106">Klasaprófíll fannst ekki, athuga skal grunnstillinguna.</span><span class="sxs-lookup"><span data-stu-id="5b204-106">Cluster profile could not be found please check your configuration."</span></span>

### <a name="issue-description"></a><span data-ttu-id="5b204-107">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="5b204-107">Issue description</span></span>

<span data-ttu-id="5b204-108">Þessi villuboð tengjast móttökuferli þar sem kveikt er á gæðastjórnun (QMS).</span><span class="sxs-lookup"><span data-stu-id="5b204-108">This error message is related to a receiving process where quality management (QMS) is turned on.</span></span> <span data-ttu-id="5b204-109">Frekari upplýsingar um færsluna sem myndar villuboðin gætu hjálpað við að lagfæra vandamálið, allt eftir skilgreiningum í umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="5b204-109">Depending on the configurations in your environment, additional details about the transaction that is generating the error message might help fix the issue.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5b204-110">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="5b204-110">Issue resolution</span></span>

<span data-ttu-id="5b204-111">Fyrst skal yfirfara uppsetningu [Klasatiltekt](set-up-cluster-picking.md) og ganga úr skugga um að klasaforstillingar séu rétt uppsettar.</span><span class="sxs-lookup"><span data-stu-id="5b204-111">First, review the [cluster picking](set-up-cluster-picking.md) setup, and make sure that your cluster profiles are set up correctly.</span></span> <span data-ttu-id="5b204-112">Ekki er hægt að nota valmyndaratriði fartækis fyrir klasatiltekt nema klasaforstillingar séu settar upp.</span><span class="sxs-lookup"><span data-stu-id="5b204-112">You can't use a mobile device menu item for cluster picking unless cluster profiles are set up.</span></span> <span data-ttu-id="5b204-113">Einnig gæti verið nauðsynlegt að fara yfir aðrar tengdar skilgreiningar í samræmi við umhverfinu.</span><span class="sxs-lookup"><span data-stu-id="5b204-113">Depending on your environment, you might also have to review other related configurations.</span></span>

## <a name="mixed-license-plate-receiving-doesnt-work-for-any-disposition-code-except-credit"></a><span data-ttu-id="5b204-114">Móttaka blandaðrar númeraplötu virkar ekki fyrir neinn ráðstöfunarkóða fyrir utan Kredit.</span><span class="sxs-lookup"><span data-stu-id="5b204-114">Mixed license plate receiving doesn't work for any disposition code except Credit.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5b204-115">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="5b204-115">Issue description</span></span>

<span data-ttu-id="5b204-116">Þegar svæðið **Aðgerð** fyrir ráðstöfunarkóða er stillt á *Kredit* eða *Úrkast* er aðeins hægt að nota valmyndina [Móttaka blandaðrar númeraplötu](mixed-license-plate-receiving.md) valmyndaratriði til að vinna úr skilavörum.</span><span class="sxs-lookup"><span data-stu-id="5b204-116">When the **Action** field for a disposition code is set to *Credit* or *Scrap*, you can use only the [Mixed license plate receiving](mixed-license-plate-receiving.md) menu item to process returned items.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5b204-117">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="5b204-117">Issue resolution</span></span>

<span data-ttu-id="5b204-118">Microsoft hefur metið þetta mál og hefur ákvarðað að þetta sé takmörkun eiginleika.</span><span class="sxs-lookup"><span data-stu-id="5b204-118">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="5b204-119">Sem stendur eru aðeins [ráðstöfunarkóðar](../service-management/set-up-disposition-codes.md) þar sem reiturinn **Aðgerð** er stilltur á *Kredit* eða *Rýrnun* studdir fyrir móttöku blandaðrar númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="5b204-119">Currently, only [disposition codes](../service-management/set-up-disposition-codes.md) where the **Action** field is set to *Credit* or *Scrap* are supported for mixed license plate receiving.</span></span>

## <a name="when-i-run-the-update-product-receipts-periodic-task-unconfirmed-purchase-orders-are-confirmed"></a><span data-ttu-id="5b204-120">Þegar reglubundna verkið Uppfæra innhreyfingarskjöl afurða er keyrt eru óstaðfestar innkaupapantanir staðfestar.</span><span class="sxs-lookup"><span data-stu-id="5b204-120">When I run the Update product receipts periodic task, unconfirmed purchase orders are confirmed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="5b204-121">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="5b204-121">Issue description</span></span>

<span data-ttu-id="5b204-122">Þegar búið er að keyra reglubundna verkið *Uppfæra innhreyfingarskjöl afurða* staðfestir kerfið sjálfkrafa óstaðfestar innkaupapantanir sem eru með birgðafærslustöðu *Skráð*.</span><span class="sxs-lookup"><span data-stu-id="5b204-122">After you run the *Update product receipts* periodic task, the system automatically confirms unconfirmed purchase orders that have an inventory transaction status of *Registered*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5b204-123">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="5b204-123">Issue resolution</span></span>

<span data-ttu-id="5b204-124">Nýr eiginleiki fyrir meðhöndlun á innleið, *Umframmóttaka á hleðslumagni*, lagar þetta vandamál.</span><span class="sxs-lookup"><span data-stu-id="5b204-124">A new inbound load handling feature, *Over receipt of load quantities*, fixes this issue.</span></span> <span data-ttu-id="5b204-125">Til að kveikja á þessum eiginleika skal fara í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eftirfarandi eiginleikum (í þeirri röð sem þeir eru sýndir).</span><span class="sxs-lookup"><span data-stu-id="5b204-125">To turn on this feature, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the following features (in the order that they are listed in):</span></span>

1. <span data-ttu-id="5b204-126">Tengja birgðafærslur innkaupapöntunar við farm</span><span class="sxs-lookup"><span data-stu-id="5b204-126">Associate purchase order inventory transactions with load</span></span>
1. <span data-ttu-id="5b204-127">Umframmóttaka á hleðslumagni</span><span class="sxs-lookup"><span data-stu-id="5b204-127">Over receipt of load quantities</span></span>

<span data-ttu-id="5b204-128">Frekari upplýsingar er að finna á [Bóka skráð afurðamagn á móti innkaupapöntunum](inbound-load-handling.md#post-registered-quantities).</span><span class="sxs-lookup"><span data-stu-id="5b204-128">For more information, see [Post registered product quantities against purchase orders](inbound-load-handling.md#post-registered-quantities).</span></span>

## <a name="when-i-register-inbound-orders-i-receive-the-following-error-message-the-quantity-is-not-valid"></a><span data-ttu-id="5b204-129">Þegar pantanir á innleið eru skráðar birtast eftirfarandi villuskilaboð: „Magnið er ekki gilt fyrir einingu“.</span><span class="sxs-lookup"><span data-stu-id="5b204-129">When I register inbound orders, I receive the following error message: "The quantity is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="5b204-130">Lýsing á úrlausnaratriði</span><span class="sxs-lookup"><span data-stu-id="5b204-130">Issue description</span></span>

<span data-ttu-id="5b204-131">Ef reiturinn **Regla um flokkun númeraplötu** er stilltur á *Skilgreint af notanda* fyrir valmyndaratriði fartækis sem er notað til að skrá pantanir á innleið, koma upp villuboð („Magnið er ekki gilt“) og ekki verður hægt að ljúka skráningunni.</span><span class="sxs-lookup"><span data-stu-id="5b204-131">If the **License plate grouping policy** field is set to *User defined* for a mobile device menu item that is used to register inbound orders, you receive an error message ("The quantity is not valid"), and you can't complete the registration.</span></span>

### <a name="issue-cause"></a><span data-ttu-id="5b204-132">Ástæða vandamáls</span><span class="sxs-lookup"><span data-stu-id="5b204-132">Issue cause</span></span>

<span data-ttu-id="5b204-133">Þegar *Skilgreint af notanda* er notað sem regla um flokkun númeraplötu, skiptir kerfið væntanlegum birgðum niður á aðskildar númeraplötur eins og röðunarflokkur einingar gefur til kynna.</span><span class="sxs-lookup"><span data-stu-id="5b204-133">When *User defined* is used as a license plate grouping policy, the system splits the incoming inventory into separate license plates, as indicated by the unit sequence group.</span></span> <span data-ttu-id="5b204-134">Ef runu- og raðnúmer eru notuð til að rekja vöruna sem tekið er á móti þarf að tilgreina magn hverrar runu eða raðnúmers fyrir hverja númeraplötu sem er skráð.</span><span class="sxs-lookup"><span data-stu-id="5b204-134">If batch or serial numbers are used to track the item that is being received, the quantities of each batch or serial must be specified per license plate that is registered.</span></span> <span data-ttu-id="5b204-135">Ef magnið sem er tilgreint fyrir númeraplötu er umfram magnið sem þarf enn að taka á móti fyrir núverandi víddir, koma upp villuboð.</span><span class="sxs-lookup"><span data-stu-id="5b204-135">If the quantity that is specified for a license plate exceeds the quantity that must still be received for the current dimensions, you receive the error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="5b204-136">Úrlausn úrlausnaratriðis</span><span class="sxs-lookup"><span data-stu-id="5b204-136">Issue resolution</span></span>

<span data-ttu-id="5b204-137">Þegar vara er skráð með því að nota valmyndaratriði fartækis þar sem reiturinn **Regla um flokkun númeraplötu** er stilltur á *Skilgreint af notanda*, gæti kerfið gert kröfu um að númeraplötunúmer, rununúmer eða raðnúmer verði staðfest eða slegin inn.</span><span class="sxs-lookup"><span data-stu-id="5b204-137">When you register an item by using a mobile device menu item where the **License plate grouping policy** field is set to *User defined*, the system might require that you confirm or enter license plate numbers, batch numbers, or serial numbers.</span></span>

<span data-ttu-id="5b204-138">Á staðfestingarsíðu númeraplötu sýnir kerfið magnið sem er úthlutað fyrir núverandi númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="5b204-138">On the license plate confirmation page, the system will show the quantity that is allocated for the current license plate.</span></span> <span data-ttu-id="5b204-139">Á staðfestingarsíðum rununúmers og raðnúmers sýnir kerfið magnið sem þarf enn að taka á móti á núverandi númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="5b204-139">On the batch or serial confirmation pages, the system will show the quantity that must still be received on the current license plate.</span></span> <span data-ttu-id="5b204-140">Þar verður einnig reitur þar sem hægt er að slá inn magnið til að skrá fyrir þá samsetningu af númeraplötu og runu- eða raðnúmeri.</span><span class="sxs-lookup"><span data-stu-id="5b204-140">It will also include a field where you can enter the quantity to register for that combination of license plate and batch or serial number.</span></span> <span data-ttu-id="5b204-141">Í þessu tilfelli skal ganga úr skugga um magnið sem verið er að skrá fyrir númeraplötuna fari ekki umfram magnið sem þarf enn að taka á móti.</span><span class="sxs-lookup"><span data-stu-id="5b204-141">In this case, make sure that the quantity that is being registered for the license plate doesn't exceed the quantity that must still be received.</span></span>

<span data-ttu-id="5b204-142">Ef verið er að búa til of margar númeraplötur við skráningu á pöntun á innleið verður hægt að breyta gildinu í reitnum **Regla um flokkun númeraplötu** í *Flokkun númeraplötu*, hægt verður að úthluta nýjum röðunarflokki einingar á vöruna eða hægt verður að gera valkostinn **Flokkun númeraplötu** fyrir röðunarflokk einingar óvirkan.</span><span class="sxs-lookup"><span data-stu-id="5b204-142">Alternatively, if too many license plates are being generated on inbound order registration, the value of the **License plate grouping policy** field can be changed to *License plate grouping*, a new unit sequence group can be assigned to the item, or the **License plate grouping** option for the unit sequence group can be inactivated.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
