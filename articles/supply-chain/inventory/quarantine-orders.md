---
title: "Biðgeymslupantanir"
description: "Þetta efnisatriði lýsir því hvernig biðgeymslupantanir eru notaðar til að loka birgðum."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventLocation, InventModelGroup, InventQuarantineOrder, InventQuarantineParmEnd, InventQuarantineParmReportFinished, InventQuarantineParmStartUp, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 30021
ms.assetid: d5047727-653c-49da-b489-6fd3fe50445e
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 523e51c705d76b6e8624887292395f8f239bcb65
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---

# <a name="quarantine-orders"></a><span data-ttu-id="96f27-103">Biðgeymslupantanir</span><span class="sxs-lookup"><span data-stu-id="96f27-103">Quarantine orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96f27-104">Þetta efnisatriði lýsir því hvernig biðgeymslupantanir eru notaðar til að loka birgðum.</span><span class="sxs-lookup"><span data-stu-id="96f27-104">This topic describes how quarantine orders are used to block inventory.</span></span>

<span data-ttu-id="96f27-105">Hægt er að nota Biðgeymslupantanir til að loka birgðum.</span><span class="sxs-lookup"><span data-stu-id="96f27-105">Quarantine orders can be used to block inventory.</span></span> <span data-ttu-id="96f27-106">Til dæmis gætir þú viljað láta vörur í biðgeymslu vegna gæðaeftirlits.</span><span class="sxs-lookup"><span data-stu-id="96f27-106">For example, you might want to quarantine items for quality control reasons.</span></span> <span data-ttu-id="96f27-107">Birgðir sem hafa verið settar í biðgeymslu eru fluttar í biðgeymsluvöruhús.</span><span class="sxs-lookup"><span data-stu-id="96f27-107">Inventory that has been quarantined is transferred to a quarantine warehouse.</span></span> <span data-ttu-id="96f27-108">**Athugasemd:** Ef verið er að nota ítarlegt vöruhúsakerfisferli (í vöruhúsakerfi) er vinnsla pantana í biðgeymslu einungis notuð fyrir skil á sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="96f27-108">**Note:** If you're using advanced warehouse management processes (in Warehouse management), quarantine order processing is used only for return sales orders.</span></span>

## <a name="quarantine-on-hand-inventory-items"></a><span data-ttu-id="96f27-109">Vörur biðgeymslubirgða á lager</span><span class="sxs-lookup"><span data-stu-id="96f27-109">Quarantine on-hand inventory items</span></span>
<span data-ttu-id="96f27-110">Þegar vara er sett í biðgeymslu geturðu annað hvort stofnað biðgeymslupantanir handvirkt eða stillt kerfið til að stofna biðgeymslupantanir sjálfkrafa við ferli á innleið.</span><span class="sxs-lookup"><span data-stu-id="96f27-110">When you quarantine items, you can either create the quarantine orders manually or set up the system to create the quarantine orders automatically during inbound processing.</span></span> <span data-ttu-id="96f27-111">Til að stofna biðgeymslupantanir sjálfkrafa, veljið **Stjórnun Biðgeymslu** valkostinn í flipanum **Birgðareglur** á síðunni **Vörulíkanaflokkar**.</span><span class="sxs-lookup"><span data-stu-id="96f27-111">To create quarantine orders automatically, select the **Quarantine management** option on the **Inventory policies** tab on the **Item model groups** page.</span></span> <span data-ttu-id="96f27-112">Einnig þarf að tilgreina sjálfgefið biðgeymsluvöruhús í svæðinu **Biðgeymsluvöruhús** fyrir móttökuvöruhúsin.</span><span class="sxs-lookup"><span data-stu-id="96f27-112">You must also specify a default quarantine warehouse in the **Quarantine warehouse** field for the receiving warehouses.</span></span> <span data-ttu-id="96f27-113">Í Microsoft Dynamics 365 for Finance and Operations eru vörur í biðgeymslu sjálkrafa settar í biðgeymsluvöruhús þegar efnislegar birgðir á lager eru skráðar með innkaupapöntun eða framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="96f27-113">When the physically on-hand inventory is recorded in a purchase order or production order, quarantined items are automatically moved to a quarantine warehouse in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="96f27-114">Þessa hreyfing gerist vegna þess að stöðu biðgeymslupöntunar hefur verið breytt í **Byrjað**.</span><span class="sxs-lookup"><span data-stu-id="96f27-114">This movement occurs because the status of the quarantine order is changed to **Started**.</span></span> <span data-ttu-id="96f27-115">Þegar þú stofnar biðgeymslupantanir handvirkt, þarf varan ekki að vera sett upp fyrir biðgeymslustjórnun í tengdum vörulíkanaflokkum.</span><span class="sxs-lookup"><span data-stu-id="96f27-115">When you create quarantine orders manually, the item doesn't have to be set up for quarantine management in the associated item model group.</span></span> <span data-ttu-id="96f27-116">Fyrir þetta ferli þarf að tilgreina biðgeymsluvöruhús sem á að nota og birgðir á lager sem á að setja í biðgeymslu.</span><span class="sxs-lookup"><span data-stu-id="96f27-116">For this process, you must specify the on-hand inventory that should be quarantined and the quarantine warehouse that should be used.</span></span> <span data-ttu-id="96f27-117">Það er hægt að nota stöðu biðgeymslupöntunar til að auðvelda áætlun ferlisins.</span><span class="sxs-lookup"><span data-stu-id="96f27-117">You can use the quarantine order statuses to help plan the process.</span></span>

## <a name="quarantine-order-statuses"></a><span data-ttu-id="96f27-118">Staða biðgeymslupöntunar.</span><span class="sxs-lookup"><span data-stu-id="96f27-118">Quarantine order statuses</span></span>
<span data-ttu-id="96f27-119">Biðgeymslupantanir geta haft eftirfarandi stöðu:</span><span class="sxs-lookup"><span data-stu-id="96f27-119">Quarantine orders can have the following statuses:</span></span>

-   <span data-ttu-id="96f27-120">Stofnaður</span><span class="sxs-lookup"><span data-stu-id="96f27-120">Created</span></span>
-   <span data-ttu-id="96f27-121">Hafin</span><span class="sxs-lookup"><span data-stu-id="96f27-121">Started</span></span>
-   <span data-ttu-id="96f27-122">Tilgreint sem tilbúið</span><span class="sxs-lookup"><span data-stu-id="96f27-122">Reported as finished</span></span>
-   <span data-ttu-id="96f27-123">Lokið</span><span class="sxs-lookup"><span data-stu-id="96f27-123">Ended</span></span>

### <a name="created"></a><span data-ttu-id="96f27-124">Stofnaður</span><span class="sxs-lookup"><span data-stu-id="96f27-124">Created</span></span>

<span data-ttu-id="96f27-125">Þegar Biðgeymslupöntunin er stofnuð handvirkt en varan er ekki enn staðsett í biðgeymsluvöruhúsinu, fær biðgeymslupöntunin stöðuna **Stofnað**.</span><span class="sxs-lookup"><span data-stu-id="96f27-125">When a quarantine order has been created manually, but the item isn't yet in the quarantine warehouse, the quarantine order has a status of **Created**.</span></span> <span data-ttu-id="96f27-126">Tvær birgðafærslur eru myndaðar:</span><span class="sxs-lookup"><span data-stu-id="96f27-126">Two inventory transactions are generated.</span></span> <span data-ttu-id="96f27-127">Ein færslan er úthreyfingarfærsla sem getur haft stöðuna **Í pöntun**, **Frátekið á lager**, eða **Tiltekið**.</span><span class="sxs-lookup"><span data-stu-id="96f27-127">One transaction is an issue transaction that can have a status of **On order**, **Reserved physical**, or **Picked**.</span></span> <span data-ttu-id="96f27-128">Hin færslan er innhreyfingarfærsla sem getur haft stöðuna **Pantað** eða **Skráð** í biðgeymsluvöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="96f27-128">The other transaction is a receipt transaction that can have a status of **Ordered** or **Registered** at the quarantine warehouse.</span></span> <span data-ttu-id="96f27-129">Hægt er að taka frá, taka til og skrá uppfærslur á birgðum með því að nota vanalegt ferli.</span><span class="sxs-lookup"><span data-stu-id="96f27-129">You can reserve, pick, and register updates to the inventory by using the usual processes.</span></span>

### <a name="started"></a><span data-ttu-id="96f27-130">Hafin</span><span class="sxs-lookup"><span data-stu-id="96f27-130">Started</span></span>

<span data-ttu-id="96f27-131">Þegar biðgeymslupöntun er í stöðunni **Hafin** eru vörurnar færðar úr hefðbundna vöruhúsinu í biðgeymsluvöruhúsið og eru tvær birgðafærslur myndaðar.</span><span class="sxs-lookup"><span data-stu-id="96f27-131">When a quarantine order has a status of **Started**, the inventory is transferred from the regular warehouse to the quarantine warehouse, and two inventory transactions are generated.</span></span> <span data-ttu-id="96f27-132">Ein færsla hefur stöðuna **Frádregið**, og önnur færslan hefur stöðuna **Móttekið**.</span><span class="sxs-lookup"><span data-stu-id="96f27-132">One transaction has a status of **Deducted**, and the other transaction has a status of **Received**.</span></span> <span data-ttu-id="96f27-133">Á sama tíma eru einnig tvær birgðafærslur myndaðar til að annast skilafærsluna.</span><span class="sxs-lookup"><span data-stu-id="96f27-133">At the same time, two inventory transactions are created to handle the return transfer.</span></span> <span data-ttu-id="96f27-134">Þessar færslur fá ekki dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="96f27-134">These transactions aren't dated.</span></span> <span data-ttu-id="96f27-135">Ein færsla hefur stöðuna **efnislega frátekið**, og önnur færslan hefur stöðuna **pantað**.</span><span class="sxs-lookup"><span data-stu-id="96f27-135">One transaction has a status of **Reserved physical**, and the other transaction has a status of **Ordered**.</span></span>

### <a name="reported-as-finished"></a><span data-ttu-id="96f27-136">Tilgreint sem tilbúið</span><span class="sxs-lookup"><span data-stu-id="96f27-136">Reported as finished</span></span>

<span data-ttu-id="96f27-137">Með því að smella á **Bóka sem tilbúið** er hægt að tilkynna byrjaða biðgeymslupöntun sem tilbúna.</span><span class="sxs-lookup"><span data-stu-id="96f27-137">By clicking **Report as finished**, you can report a started quarantine order as finished.</span></span> <span data-ttu-id="96f27-138">Varan er leyst úr biðgeymslu en hún er ekki færð aftur í vanalega vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="96f27-138">The item is released from quarantine but isn't yet moved back to the regular warehouse.</span></span> <span data-ttu-id="96f27-139">Þetta er hægt að vinna með vörukomubók sem má frumstilla á meðan ferlið Bóka sem tilbúið er enn í gangi.</span><span class="sxs-lookup"><span data-stu-id="96f27-139">The movement back to the regular warehouse can be processed via an Item arrival journal that can be initialized during the Report as finished process.</span></span>

### <a name="ended"></a><span data-ttu-id="96f27-140">Lokið</span><span class="sxs-lookup"><span data-stu-id="96f27-140">Ended</span></span>

<span data-ttu-id="96f27-141">Þegar biðgeymslupöntun er lokið er vara færð úr biðgeymsluvöruhúsi og aftur í vanalegt vöruhús.</span><span class="sxs-lookup"><span data-stu-id="96f27-141">When a quarantine order is ended, the item is moved from the quarantine warehouse back to the regular warehouse.</span></span> <span data-ttu-id="96f27-142">Staða vörufærslunnar er stillt á **Selt** í biðgeymsluvöruhúsinu og **Keypt** í venjulegt vöruhús.</span><span class="sxs-lookup"><span data-stu-id="96f27-142">The status of the item transaction is set to **Sold** at the quarantine warehouse and **Purchased** at the regular warehouse.</span></span>

## <a name="quarantine-order-scrap"></a><span data-ttu-id="96f27-143">Rýrnun Biðgeymslupöntunar</span><span class="sxs-lookup"><span data-stu-id="96f27-143">Quarantine order scrap</span></span>
<span data-ttu-id="96f27-144">Hægt er að rýra birgðir sem hluta af biðgeymslupöntunarferlinu.</span><span class="sxs-lookup"><span data-stu-id="96f27-144">As part of the quarantine order process, you can scrap inventory.</span></span> <span data-ttu-id="96f27-145">Við vinnslu á rýrnun verður staða birgða stillt á **Selt** með úthreyfingarfærslu úr biðgeymsluvöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="96f27-145">When you process scrap, the status of the inventory will be set to **Sold** by an issue transaction from the quarantine warehouse.</span></span>

<a name="additional-resources"></a><span data-ttu-id="96f27-146">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="96f27-146">Additional resources</span></span>
--------

[<span data-ttu-id="96f27-147">Stöðvun í birgðum</span><span class="sxs-lookup"><span data-stu-id="96f27-147">Inventory blocking</span></span>](inventory-blocking.md)

