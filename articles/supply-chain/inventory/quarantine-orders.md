---
title: Biðgeymslupantanir
description: Í þessu efnisatriði er lýst hvernig eigi að nota biðgeymslupantanir til að loka fyrir birgðaskráningu.
author: perlynne
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e1eed14b7d38cf569af7192dec9580e771f06df
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956183"
---
# <a name="quarantine-orders"></a><span data-ttu-id="f3eb3-103">Biðgeymslupantanir</span><span class="sxs-lookup"><span data-stu-id="f3eb3-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f3eb3-104">Í þessu efnisatriði er lýst hvernig eigi að nota biðgeymslupantanir til að loka fyrir birgðaskráningu.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-104">This topic describes how to use quarantine orders to block inventory.</span></span>

<span data-ttu-id="f3eb3-105">Með biðgeymslupöntun geturðu lokað á birgðir.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-105">Quarantine orders let you block inventory.</span></span> <span data-ttu-id="f3eb3-106">Til dæmis gætir þú viljað láta vörur í biðgeymslu vegna gæðaeftirlits.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="f3eb3-107">Birgðir sem hafa verið settar í biðgeymslu eru fluttar í biðgeymsluvöruhús.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span>

> [!NOTE]
> <span data-ttu-id="f3eb3-108">Ef verið er að nota ítarlegt vöruhúsakerfisferli (í vöruhúsakerfi) er vinnsla pantana í biðgeymslu einungis notuð fyrir skil á sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-108">If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="f3eb3-109">Vörur biðgeymslubirgða á lager</span><span class="sxs-lookup"><span data-stu-id="f3eb3-109">Quarantine on-hand inventory items</span></span>

<span data-ttu-id="f3eb3-110">Þegar vörur eru settar í biðgeymslu geturðu annaðhvort stofnað biðgeymslupantanir handvirkt eða sett upp kerfið til að stofna þær sjálfkrafa í ferli á innleið.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-110">When you quarantine items, you can either manually create the quarantine orders or set up the system to automatically create them during inbound processing.</span></span>

<span data-ttu-id="f3eb3-111">Fylgið eftirfarandi skrefum til að setja kerfið upp þannig að það búi sjálfkrafa til biðgeymslupantanir.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-111">To set up the system to automatically generate quarantine orders, follow these steps.</span></span>

1. <span data-ttu-id="f3eb3-112">Opnið **Birgðastjórnun \> Uppsetning \> Birgðir \> Vörulíkanaflokkar.**</span><span class="sxs-lookup"><span data-stu-id="f3eb3-112">Go to **Inventory management \> Setup \> Inventory \> Item model groups**.</span></span>
1. <span data-ttu-id="f3eb3-113">Veljið viðeigandi líkanahóp á listasvæði eða stofnið nýjan líkanahóp.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-113">Select a relevant model group in the list pane, or create a new model group.</span></span>
1. <span data-ttu-id="f3eb3-114">Í flýtiflipanum **Birgðareglur** skal velja gátreitinn **Biðgeymslustjórnun**.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-114">On the **Inventory policies** FastTab, select the **Quarantine management** check box.</span></span>
1. <span data-ttu-id="f3eb3-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-115">Close the page.</span></span>
1. <span data-ttu-id="f3eb3-116">Tilgreinið sjálfgefið biðgeymsluvöruhús í svæðinu **Biðgeymsluvöruhús** fyrir móttökuvöruhúsin.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-116">In the **Quarantine warehouse** field for the receiving warehouses, specify a default quarantine warehouse.</span></span>

<span data-ttu-id="f3eb3-117">Þegar var sem er skráð sem móttekin í vöruhúsinu sem tilheyrir líkanaflokki þar sem gátreiturinn **Biðgeymslustjórnun** er valinn, býr kerfið til biðgeymslupöntun fyrir hana.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-117">When an item that is registered as received at the warehouse belongs to a model group where the **Quarantine management** check box is selected, the system generates a quarantine order for it.</span></span> <span data-ttu-id="f3eb3-118">Í biðgeymslupöntuninni er starfskröftum gefin fyrirmæli um að flytja vöruna í biðgeymsluvöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-118">The quarantine order instructs workers to move the item to the quarantine warehouse.</span></span>

<span data-ttu-id="f3eb3-119">Þegar þú stofnar biðgeymslupantanir handvirkt á síðunni **Biðgeymslupantanir** þarf varan ekki að vera sett upp fyrir biðgeymslustjórnun í tengdum vörulíkanaflokki.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-119">When you manually create quarantine orders on the **Quarantine orders** page, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="f3eb3-120">Fyrir þetta ferli þarf að tilgreina biðgeymsluvöruhús sem á að nota og birgðir á lager sem á að setja í biðgeymslu.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-120">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="f3eb3-121">Það er hægt að nota stöðu biðgeymslupöntunar til að auðvelda áætlun ferlisins.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-121">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="f3eb3-122">Staða biðgeymslupöntunar.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-122">Quarantine order statuses</span></span>

<span data-ttu-id="f3eb3-123">Biðgeymslupantanir geta haft eftirfarandi stöðu:</span><span class="sxs-lookup"><span data-stu-id="f3eb3-123">Quarantine orders can have the following statuses:</span></span>

- <span data-ttu-id="f3eb3-124">Stofnaður</span><span class="sxs-lookup"><span data-stu-id="f3eb3-124">Created</span></span>
- <span data-ttu-id="f3eb3-125">Hafin</span><span class="sxs-lookup"><span data-stu-id="f3eb3-125">Started</span></span>
- <span data-ttu-id="f3eb3-126">Tilgreint sem tilbúið</span><span class="sxs-lookup"><span data-stu-id="f3eb3-126">Reported as finished</span></span>
- <span data-ttu-id="f3eb3-127">Lokið</span><span class="sxs-lookup"><span data-stu-id="f3eb3-127">Ended</span></span>

### <a name="created"></a><span data-ttu-id="f3eb3-128">Stofnaður</span><span class="sxs-lookup"><span data-stu-id="f3eb3-128">Created</span></span>

<span data-ttu-id="f3eb3-129">Þegar Biðgeymslupöntunin er stofnuð handvirkt en varan er ekki enn staðsett í biðgeymsluvöruhúsinu, fær biðgeymslupöntunin stöðuna **Stofnað**.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-129">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="f3eb3-130">Tvær birgðafærslur eru myndaðar:</span><span class="sxs-lookup"><span data-stu-id="f3eb3-130">Two inventory transactions are generated.</span></span> <span data-ttu-id="f3eb3-131">Ein færslan er úthreyfingarfærsla sem getur haft stöðuna **Í pöntun**, **Frátekið á lager**, eða **Tiltekið**.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-131">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="f3eb3-132">Hin færslan er innhreyfingarfærsla sem getur haft stöðuna **Pantað** eða **Skráð** í biðgeymsluvöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-132">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="f3eb3-133">Hægt er að taka frá, taka til og skrá uppfærslur á birgðum með því að nota vanalegt ferli.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-133">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="f3eb3-134">Hafin</span><span class="sxs-lookup"><span data-stu-id="f3eb3-134">Started</span></span>

<span data-ttu-id="f3eb3-135">Þegar biðgeymslupöntun er í stöðunni **Hafin** eru vörurnar færðar úr hefðbundna vöruhúsinu í biðgeymsluvöruhúsið og eru tvær birgðafærslur myndaðar.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-135">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="f3eb3-136">Ein færsla hefur stöðuna **Frádregið**, og önnur færslan hefur stöðuna **Móttekið**.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-136">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="f3eb3-137">Á sama tíma eru einnig tvær birgðafærslur myndaðar til að annast skilafærsluna.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-137">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="f3eb3-138">Þessar færslur fá ekki dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-138">These transactions aren't dated.</span></span> <span data-ttu-id="f3eb3-139">Ein færsla hefur stöðuna **efnislega frátekið**, og önnur færslan hefur stöðuna **pantað**.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-139">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="f3eb3-140">Tilbúið</span><span class="sxs-lookup"><span data-stu-id="f3eb3-140">Reported as finished</span></span>

<span data-ttu-id="f3eb3-141">Til að tilkynna hafna biðgeymslupöntun sem lokna er hún opnuð og valið **Tilkynna sem lokið** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-141">To report a started quarantine order as finished, open the order, and select **Report as finished** on the Action Pane.</span></span> <span data-ttu-id="f3eb3-142">Varan er leyst úr biðgeymslu en hún er ekki færð aftur í vanalega vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-142">The item is released from quarantine, but it isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="f3eb3-143">Þetta er hægt að vinna með vörukomubók sem má frumstilla á meðan ferlið Bóka sem tilbúið er enn í gangi.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-143">The movement back to the regular warehouse can be processed via an item arrival journal that can be initialized during the report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="f3eb3-144">Búið</span><span class="sxs-lookup"><span data-stu-id="f3eb3-144">Ended</span></span>

<span data-ttu-id="f3eb3-145">Þegar biðgeymslupöntun er lokið er vara færð úr biðgeymsluvöruhúsi og aftur í vanalegt vöruhús.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-145">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="f3eb3-146">Staða vörufærslunnar er stillt á *Selt* í biðgeymsluvöruhúsinu og *Keypt* í venjulegt vöruhús.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-146">The status of the item transaction is set to *Sold* at the quarantine warehouse and *Purchased* at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="f3eb3-147">Rýrnun Biðgeymslupöntunar</span><span class="sxs-lookup"><span data-stu-id="f3eb3-147">Quarantine order scrap</span></span>

<span data-ttu-id="f3eb3-148">Hægt er að rýra birgðir sem hluta af biðgeymslupöntunarferlinu.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-148">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="f3eb3-149">Við vinnslu á rýrnun er staða birgða stillt á *Selt* með úthreyfingarfærslu úr biðgeymsluvöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="f3eb3-149">When you process scrap, the status of the inventory is set to *Sold* by an issue transaction from the quarantine warehouse.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f3eb3-150">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f3eb3-150">Additional resources</span></span>

- [<span data-ttu-id="f3eb3-151">Stöðvun í birgðum</span><span class="sxs-lookup"><span data-stu-id="f3eb3-151">Inventory blocking</span></span>](inventory-blocking.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
