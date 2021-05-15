---
title: Birgðaleiðrétting vöruhúss
description: Í þessu efnisatriði er að finna upplýsingar um birgðaleiðréttingabók vöruhúss og úrvinnslu þegar einingakvarðar eru notaðir.
author: perlynne
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: be386539ea7addf20256ac2b1f8a2a72736fcbec
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938227"
---
# <a name="warehouse-inventory-adjustment"></a><span data-ttu-id="74263-103">Birgðaleiðrétting vöruhúss</span><span class="sxs-lookup"><span data-stu-id="74263-103">Warehouse inventory adjustment</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="74263-104">Birgðaleiðréttingareiginleiki vöruhúss er notaður þegar einingakvarðar skýs og jaðra er keyrt fyrir [vinnuálag framleiðslu](cloud-edge-workload-manufacturing.md) og [vinnuálag vöruhúsakerfis](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="74263-104">The Warehouse inventory adjustment feature is used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="74263-105">Þegar starfsmaður framkvæmir birgðaleiðréttingu með því að nota vöruhúsaforritið gagnvart einingakvarða vinnuálags vöruhúsakerfis verður runuvinnslan **Birgðaleiðréttingabók vöruhúss** að vinna úr uppfærslu efnislegra birgða sem er keyrð og tímasett með því að fara í **Vöruhúsakerfi > Reglubundin verk > Birgðaleiðréttingabók vöruhúss**.</span><span class="sxs-lookup"><span data-stu-id="74263-105">When a worker does an inventory adjustment using the warehouse app against a scale unit warehouse management workload, the physical on-hand update must be processed by the **Warehouse inventory adjustment journal** batch job, which you run and schedule by going to **Warehouse management > Periodic tasks > Warehouse inventory adjustment journal**.</span></span>

<span data-ttu-id="74263-106">Eftirfarandi vinnuferli vöruhúsaforrits notar **Birgðaleiðréttingabók vöruhúss** í vinnuálagi einingakvarða:</span><span class="sxs-lookup"><span data-stu-id="74263-106">The following warehouse app work processes currently use the **Warehouse inventory adjustment journal** on scale unit workloads:</span></span>

- <span data-ttu-id="74263-107">Leiðrétting (inn/út)</span><span class="sxs-lookup"><span data-stu-id="74263-107">Adjustment in/out</span></span>
- <span data-ttu-id="74263-108">Regluleg talning</span><span class="sxs-lookup"><span data-stu-id="74263-108">Cycle counting</span></span>
- <span data-ttu-id="74263-109">Hleðsla númeraplötu</span><span class="sxs-lookup"><span data-stu-id="74263-109">License plate loading</span></span>

<span data-ttu-id="74263-110">Nokkrar birgðafærslur eru stofnaðar sem hluti af skýi og jaðri í ferli birgðaleiðréttingar vegna þess að uppsetningar miðstöðvar og einingakvarða deila birgðafærslum.</span><span class="sxs-lookup"><span data-stu-id="74263-110">Several inventory transactions are created as part of cloud and edge an inventory adjustment process because the hub and scale unit deployments share the inventory records.</span></span>

## <a name="inventory-adjustment-example"></a><span data-ttu-id="74263-111">Dæmi um birgðaleiðréttingu</span><span class="sxs-lookup"><span data-stu-id="74263-111">Inventory adjustment example</span></span>

<span data-ttu-id="74263-112">Í þessu dæmi hefur starfsmaður í vöruhúsi notað vöruhúsaforritið til að skrá lagerbirgðir sem bætt er við.</span><span class="sxs-lookup"><span data-stu-id="74263-112">In this example, a warehouse worker has used the warehouse app to register the adding of on-hand inventory.</span></span>

<span data-ttu-id="74263-113">Fyrst býr vinnuálag einingakvarða til birgðaleiðréttingafærslu vöruhúss fyrir jákvæða efnislega leiðréttingu sem er síðan samstillt við miðstöðina og leiðir til aukningar á lagerbirgðum í miðstöðinni.</span><span class="sxs-lookup"><span data-stu-id="74263-113">First, the scale unit workload creates a warehouse inventory adjustment transaction for the positive physical adjustment, which is then synchronized to the hub and results in an increase of the on-hand inventory on the hub.</span></span>

| <span data-ttu-id="74263-114">Gerð</span><span class="sxs-lookup"><span data-stu-id="74263-114">Type</span></span>                                    | <span data-ttu-id="74263-115">Kvörðunareining</span><span class="sxs-lookup"><span data-stu-id="74263-115">Scale unit</span></span> | <span data-ttu-id="74263-116">Stefna</span><span class="sxs-lookup"><span data-stu-id="74263-116">Direction</span></span> | <span data-ttu-id="74263-117">Stöð</span><span class="sxs-lookup"><span data-stu-id="74263-117">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="74263-118">Birgðaleiðrétting vöruhúss</span><span class="sxs-lookup"><span data-stu-id="74263-118">Warehouse inventory adjustment</span></span>          | <span data-ttu-id="74263-119">+1</span><span class="sxs-lookup"><span data-stu-id="74263-119">+1</span></span>         | ->        | <span data-ttu-id="74263-120">+1</span><span class="sxs-lookup"><span data-stu-id="74263-120">+1</span></span>  |

<span data-ttu-id="74263-121">Miðstöðin vinnur síðan úr bókun talningabókar sem er síðan móttekin í gegnum [skilaboð skilaboðaúrvinnslu](cloud-edge-message-processor-messages.md).</span><span class="sxs-lookup"><span data-stu-id="74263-121">The hub then processes a counting journal posting, which is received through [message processor messages](cloud-edge-message-processor-messages.md).</span></span> <span data-ttu-id="74263-122">Þetta uppfærir viðbótarbirgðir á lager.</span><span class="sxs-lookup"><span data-stu-id="74263-122">This updates the additional inventory on hand.</span></span> <span data-ttu-id="74263-123">Til að koma í veg fyrir tvöfladar birgðir á lager býr miðstöðin til mótfærslu sem hluta af þessu ferli og fjarlægir fyrri skráðar lagerbirgðir sem tengjast birgðaleiðréttingu vöruhússins.</span><span class="sxs-lookup"><span data-stu-id="74263-123">To prevent double inventory on hand, the hub creates an offset transaction as part of this process and removes the previously recorded on-hand inventory that is related to the warehouse inventory adjustment.</span></span>

| <span data-ttu-id="74263-124">Gerð</span><span class="sxs-lookup"><span data-stu-id="74263-124">Type</span></span>                                    | <span data-ttu-id="74263-125">Kvörðunareining</span><span class="sxs-lookup"><span data-stu-id="74263-125">Scale unit</span></span> | <span data-ttu-id="74263-126">Stefna</span><span class="sxs-lookup"><span data-stu-id="74263-126">Direction</span></span> | <span data-ttu-id="74263-127">Stöð</span><span class="sxs-lookup"><span data-stu-id="74263-127">Hub</span></span> |
|-----------------------------------------|------------|-----------|-----|
| <span data-ttu-id="74263-128">Talning</span><span class="sxs-lookup"><span data-stu-id="74263-128">Counting</span></span>                                | <span data-ttu-id="74263-129">+1</span><span class="sxs-lookup"><span data-stu-id="74263-129">+1</span></span>         | <-        | <span data-ttu-id="74263-130">+1</span><span class="sxs-lookup"><span data-stu-id="74263-130">+1</span></span>  |
| <span data-ttu-id="74263-131">Birgðaleiðrétting vöruhúss (mótfærsla)</span><span class="sxs-lookup"><span data-stu-id="74263-131">Warehouse inventory adjustment (Offset)</span></span> | <span data-ttu-id="74263-132">-1</span><span class="sxs-lookup"><span data-stu-id="74263-132">-1</span></span>         | <-        | <span data-ttu-id="74263-133">-1</span><span class="sxs-lookup"><span data-stu-id="74263-133">-1</span></span>  |

<span data-ttu-id="74263-134">Þegar einingakvarði hefur búið til **Birgðaleiðréttingabók vöruhúss** í miðstöðinni er hægt að yfirfara bæði **Talningarbók** og **Jöfnunarbók** sem miðstöðin stofnar sem hluta af breytingaferlinu.</span><span class="sxs-lookup"><span data-stu-id="74263-134">After a scale unit has created a **Warehouse inventory adjustment journal** on the hub, you can review both the **Counting journal** and the **Offset journal**, which are created by the hub as part of the adjustment process.</span></span>

<span data-ttu-id="74263-135">Þú getur farið yfir allar þessar dagbókarfærslur og færslur í Supply Chain Management með því að gera framkvæma skref:</span><span class="sxs-lookup"><span data-stu-id="74263-135">You can review each of these journal entries and transaction in Supply Chain Management by doing the following steps:</span></span>

1. <span data-ttu-id="74263-136">Skráðu þig inn á kvörðunareiningu.</span><span class="sxs-lookup"><span data-stu-id="74263-136">Sign in on the scale unit.</span></span>
1. <span data-ttu-id="74263-137">Farið í **Vöruhúsakerfi \> Reglubundin verk \> Birgðaleiðréttingabók vöruhúss**.</span><span class="sxs-lookup"><span data-stu-id="74263-137">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="74263-138">Á síðunni **Birgðaleiðréttingabók vöruhúss** skal finna og opna færslubókina sem skráði breytingu lagerbirgða.</span><span class="sxs-lookup"><span data-stu-id="74263-138">On the **Warehouse inventory adjustment journal** page, find and open the journal that recorded the on-hand inventory change.</span></span> <span data-ttu-id="74263-139">Hlutinn **Færslubókarlínur** sýnir hverja leiðréttingu sem þessi færslubók hefur skráð.</span><span class="sxs-lookup"><span data-stu-id="74263-139">The **Journal lines** section shows each adjustment recorded by this journal.</span></span>
1. <span data-ttu-id="74263-140">Skráðu þig inn í miðstöðina.</span><span class="sxs-lookup"><span data-stu-id="74263-140">Sign in on the hub.</span></span>
1. <span data-ttu-id="74263-141">Farið í **Vöruhúsakerfi \> Reglubundin verk \> Birgðaleiðréttingabók vöruhúss**.</span><span class="sxs-lookup"><span data-stu-id="74263-141">Go to **Warehouse management \> Periodic tasks \> Warehouse inventory adjustment journal**.</span></span>
1. <span data-ttu-id="74263-142">Á síðunni **Birgðaleiðréttingabók vöruhúss** ættirðu að sjá sömu færslubókina sýnda ef miðstöðin og einingakvarðinn eru samstillt.</span><span class="sxs-lookup"><span data-stu-id="74263-142">On the **Warehouse inventory adjustment journal** page, you should see the same journal listed if the hub and scale unit have synced.</span></span>
1. <span data-ttu-id="74263-143">Opna færslubókina</span><span class="sxs-lookup"><span data-stu-id="74263-143">Open the journal.</span></span> <span data-ttu-id="74263-144">Ef unnið hefur verið úr [skilaboðum skilaboðaúrvinnslu](cloud-edge-message-processor-messages.md) sjást tenglar á **Talningarbókina** og **Jöfnunarbókina** í hausnum.</span><span class="sxs-lookup"><span data-stu-id="74263-144">If the [message processor messages](cloud-edge-message-processor-messages.md) have been processed, you will see links to the **Counting journal** and the **Offset journal** in the header.</span></span>
    - <span data-ttu-id="74263-145">**Talningarbókin** á að sýna sömu víddargildin og færslubókarlínurnar.</span><span class="sxs-lookup"><span data-stu-id="74263-145">The **Counting journal** should show the same dimension values as the journal lines.</span></span>
    - <span data-ttu-id="74263-146">**Jöfnunarbókin** á að sýna mótfærsluna, sem fjarlægir tvöföldu birgðaleiðréttinguna.</span><span class="sxs-lookup"><span data-stu-id="74263-146">The **Offset journal** should show the offset, which removes the double inventory adjustment.</span></span>
    > [!NOTE]
    > <span data-ttu-id="74263-147">Þegar allri samstillingu og úrvinnslu er lokið eru **Talningarbókin** og **Jöfnunarbókin** samstillt aftur í einingakvarðann.</span><span class="sxs-lookup"><span data-stu-id="74263-147">When all syncing and processing is complete, the **Counting journal** and the **Offset journal** are synced back to the scale unit.</span></span> <span data-ttu-id="74263-148">Þessar upplýsingar er einnig hægt að skoða á viðkomandi **Birgðaleiðréttingabók vöruhúss** síðu.</span><span class="sxs-lookup"><span data-stu-id="74263-148">These can also be viewed from the relevant **Warehouse inventory adjustment journal** page.</span></span>
