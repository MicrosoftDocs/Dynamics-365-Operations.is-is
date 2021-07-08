---
title: Pökkunarstefnur gáms
description: Þetta efnisatriði lýsir muninum á pökkunarstefnum gáms og gefur dæmi.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f481f6ca047ee0285fe0e81d8fa96665e9d27cee
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292762"
---
# <a name="container-packing-strategies"></a><span data-ttu-id="43d5f-103">Pökkunarstefnur gáms</span><span class="sxs-lookup"><span data-stu-id="43d5f-103">Container packing strategies</span></span>

<span data-ttu-id="43d5f-104">*Pökkunarstefna gáms* er aðferð sem hægt er að nota til að skilgreina vöruúthlutanir í gáma.</span><span class="sxs-lookup"><span data-stu-id="43d5f-104">A *container packing strategy* is a strategy that you can use to define item allocations across containers.</span></span> <span data-ttu-id="43d5f-105">Í þessu efnisatriði er útskýrður munurinn á stefnunum *Pakka í alla opna gáma* og *Pakka aðeins í núgildandi gám*.</span><span class="sxs-lookup"><span data-stu-id="43d5f-105">This topic explains the differences between the *Pack into all open containers* and *Pack into current container only* strategies.</span></span>

- <span data-ttu-id="43d5f-106">**Pakka í alla opna gáma** – Kerfið verður að athuga alla opna gáma sem hafa verið búnir til í gámunarferlinu til að ganga úr skugga um að varan passi inn í einn af þeim.</span><span class="sxs-lookup"><span data-stu-id="43d5f-106">**Pack into all open containers** – The system must check all open containers that have already been created during the containerization cycle, to make sure that the item will fit into one of them.</span></span> <span data-ttu-id="43d5f-107">Meðan á pökkun stendur athugar kerfið hverja vöru til að ákvarða hvort hún passi í áður útbúinn gám.</span><span class="sxs-lookup"><span data-stu-id="43d5f-107">During packing, the system checks each item to determine whether it will fit into any of the previously created containers.</span></span> <span data-ttu-id="43d5f-108">Ef varan passar ekki í fyrirliggjandi gám býr kerfið til nýjan gám og heldur áfram þar til búið er að pakka allri pöntuninni.</span><span class="sxs-lookup"><span data-stu-id="43d5f-108">If the item won't fit into an existing container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="43d5f-109">Til dæmis þurfa *n* pantaðar vörur að fara í gám.</span><span class="sxs-lookup"><span data-stu-id="43d5f-109">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="43d5f-110">Í versta falli, í hvert skipti sem kerfið vinnur úr vöru sem passar ekki í neinn gám sem þegar er til staðar, mun það gera alls (\[(*n* – 1) × (*n* + 1)\] ÷ 2) athuganir til að meta hvort varan passi í gámana sem þegar eru til staðar.</span><span class="sxs-lookup"><span data-stu-id="43d5f-110">In the worst case, every time that the system processes an item that doesn't fit into any existing container, it will do a total of (\[(*n* – 1) × (*n* + 1)\] ÷ 2) checks to evaluate whether the item fits into the existing containers.</span></span>

- <span data-ttu-id="43d5f-111">**Pakka aðeins í núverandi gám** – Kerfið verður að athuga aðeins nýjasta gáminn til að ganga úr skugga um hvort varan passi í hann.</span><span class="sxs-lookup"><span data-stu-id="43d5f-111">**Pack into current container only** – The system must check only the most recently created container to make sure that the item will fit into it.</span></span> <span data-ttu-id="43d5f-112">Meðan á pökkun stendur athugar kerfið hverja vöru til að ákvarða hvort hún passi í nýjasta gáminn.</span><span class="sxs-lookup"><span data-stu-id="43d5f-112">During packing, the system checks each item to determine whether it will fit into the most recently created container.</span></span> <span data-ttu-id="43d5f-113">Ef varan passar ekki í þann gám býr kerfið til nýjan gám og heldur áfram þar til búið er að pakka allri pöntuninni.</span><span class="sxs-lookup"><span data-stu-id="43d5f-113">If the item won't fit into that container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="43d5f-114">Til dæmis þurfa *n* pantaðar vörur að fara í gám.</span><span class="sxs-lookup"><span data-stu-id="43d5f-114">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="43d5f-115">Í versta falli mun kerfið gera samtals (*n* - 1) athuganir til að meta hvort varan passi í gámana.</span><span class="sxs-lookup"><span data-stu-id="43d5f-115">In the worst case, the system will do a total of (*n* – 1) checks to evaluate whether the item fits into the containers.</span></span>

## <a name="example-of-the-flow-for-container-packing-strategies"></a><span data-ttu-id="43d5f-116">Dæmi um flæði fyrir pökkunaraðferðir gáms</span><span class="sxs-lookup"><span data-stu-id="43d5f-116">Example of the flow for container packing strategies</span></span>

<span data-ttu-id="43d5f-117">Eftirfarandi vörur eru settar upp fyrir gámapökkun.</span><span class="sxs-lookup"><span data-stu-id="43d5f-117">You set up the following items for containerization.</span></span>

| <span data-ttu-id="43d5f-118">vara</span><span class="sxs-lookup"><span data-stu-id="43d5f-118">Item</span></span> | <span data-ttu-id="43d5f-119">Efnislegar víddir (breidd × dýpt × hæð)</span><span class="sxs-lookup"><span data-stu-id="43d5f-119">Physical dimensions (width × depth × height)</span></span> | <span data-ttu-id="43d5f-120">Vægi</span><span class="sxs-lookup"><span data-stu-id="43d5f-120">Weight</span></span> |
|---|---|---|
| <span data-ttu-id="43d5f-121">HDMI kapall 6'</span><span class="sxs-lookup"><span data-stu-id="43d5f-121">HDMI Cable 6'</span></span> | <span data-ttu-id="43d5f-122">1 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="43d5f-122">1 × 1 × 1</span></span> | <span data-ttu-id="43d5f-123">1</span><span class="sxs-lookup"><span data-stu-id="43d5f-123">1</span></span> |
| <span data-ttu-id="43d5f-124">HDMI kapall 12'</span><span class="sxs-lookup"><span data-stu-id="43d5f-124">HDMI Cable 12'</span></span> | <span data-ttu-id="43d5f-125">2 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="43d5f-125">2 × 1 × 1</span></span> | <span data-ttu-id="43d5f-126">1</span><span class="sxs-lookup"><span data-stu-id="43d5f-126">1</span></span> |
| <span data-ttu-id="43d5f-127">HDMI kapall 18'</span><span class="sxs-lookup"><span data-stu-id="43d5f-127">HDMI Cable 18'</span></span> | <span data-ttu-id="43d5f-128">3 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="43d5f-128">3 × 1 × 1</span></span> | <span data-ttu-id="43d5f-129">2</span><span class="sxs-lookup"><span data-stu-id="43d5f-129">2</span></span> |

<span data-ttu-id="43d5f-130">Einnig er hægt að setja upp eftirfarandi kassa sem verða notaðir fyrir pökkun.</span><span class="sxs-lookup"><span data-stu-id="43d5f-130">You also set up the following box that will be used for packaging.</span></span>

| <span data-ttu-id="43d5f-131">Gamur</span><span class="sxs-lookup"><span data-stu-id="43d5f-131">Container</span></span> | <span data-ttu-id="43d5f-132">Efnislegar víddir (lengd × breidd × hæð)</span><span class="sxs-lookup"><span data-stu-id="43d5f-132">Physical dimensions (length × width × height)</span></span> | <span data-ttu-id="43d5f-133">Vægi</span><span class="sxs-lookup"><span data-stu-id="43d5f-133">Weight</span></span> | <span data-ttu-id="43d5f-134">Magn</span><span class="sxs-lookup"><span data-stu-id="43d5f-134">Volume</span></span> |
|---|---|---|---|
| <span data-ttu-id="43d5f-135">Miðlungsstór kassi</span><span class="sxs-lookup"><span data-stu-id="43d5f-135">Medium Box</span></span> | <span data-ttu-id="43d5f-136">6 × 3 × 2</span><span class="sxs-lookup"><span data-stu-id="43d5f-136">6 × 3 × 2</span></span> | <span data-ttu-id="43d5f-137">10</span><span class="sxs-lookup"><span data-stu-id="43d5f-137">10</span></span> | <span data-ttu-id="43d5f-138">100</span><span class="sxs-lookup"><span data-stu-id="43d5f-138">100</span></span> |

<span data-ttu-id="43d5f-139">Að lokum seturðu upp pöntun sem er með eftirfarandi afurðir og magn.</span><span class="sxs-lookup"><span data-stu-id="43d5f-139">Finally, you set up an order that has the following products and quantities.</span></span>

| <span data-ttu-id="43d5f-140">Sölupöntunarlína</span><span class="sxs-lookup"><span data-stu-id="43d5f-140">Sales order line</span></span> | <span data-ttu-id="43d5f-141">Magn</span><span class="sxs-lookup"><span data-stu-id="43d5f-141">Quantity</span></span> |
|---|---|
| <span data-ttu-id="43d5f-142">HDMI kapall 12'</span><span class="sxs-lookup"><span data-stu-id="43d5f-142">HDMI Cable 12'</span></span> | <span data-ttu-id="43d5f-143">9</span><span class="sxs-lookup"><span data-stu-id="43d5f-143">9</span></span> |
| <span data-ttu-id="43d5f-144">HDMI kapall 18'</span><span class="sxs-lookup"><span data-stu-id="43d5f-144">HDMI Cable 18'</span></span> | <span data-ttu-id="43d5f-145">8</span><span class="sxs-lookup"><span data-stu-id="43d5f-145">8</span></span> |
| <span data-ttu-id="43d5f-146">HDMI kapall 6'</span><span class="sxs-lookup"><span data-stu-id="43d5f-146">HDMI Cable 6'</span></span> | <span data-ttu-id="43d5f-147">13</span><span class="sxs-lookup"><span data-stu-id="43d5f-147">13</span></span> |

<span data-ttu-id="43d5f-148">Í eftirfarandi töflu er tekið saman hvernig gámapökkun virkar þegar aðferðin *Pakka í alla opna gáma* er notuð og þegar aðfeðrin *Pakka aðeins í núgildandi gám* er notuð.</span><span class="sxs-lookup"><span data-stu-id="43d5f-148">The following table summarizes how containerization works when you use the *Pack into all open containers* strategy and when you use the *Pack into current container only* strategy.</span></span>

| <span data-ttu-id="43d5f-149">Pakka í alla opna gáma</span><span class="sxs-lookup"><span data-stu-id="43d5f-149">Pack into all open containers</span></span> | <span data-ttu-id="43d5f-150">Pakka í núgildandi gám</span><span class="sxs-lookup"><span data-stu-id="43d5f-150">Pack into current container</span></span> |
|---|---|
| <p><span data-ttu-id="43d5f-151">HDMI kapall 12':</span><span class="sxs-lookup"><span data-stu-id="43d5f-151">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="43d5f-152">Stofna nýjan gám, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="43d5f-152">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="43d5f-153">Setjið 9 ea í gám CONT0001.</span><span class="sxs-lookup"><span data-stu-id="43d5f-153">Put 9 ea into container CONT0001.</span></span></li></ol> | <p><span data-ttu-id="43d5f-154">HDMI kapall 12':</span><span class="sxs-lookup"><span data-stu-id="43d5f-154">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="43d5f-155">Stofna nýjan gám, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="43d5f-155">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="43d5f-156">Setjið 9 ea í gám CONT0001.</span><span class="sxs-lookup"><span data-stu-id="43d5f-156">Put 9 ea into container CONT0001.</span></span></li></ol> |
| <p><span data-ttu-id="43d5f-157">HDMI kapall 18'':</span><span class="sxs-lookup"><span data-stu-id="43d5f-157">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="43d5f-158">Athuga hvort hluturinn geti passað í gám CONT0001.</span><span class="sxs-lookup"><span data-stu-id="43d5f-158">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="43d5f-159">Stofna nýjan gám, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="43d5f-159">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="43d5f-160">Setjið 5 ea í gám CONT0002.</span><span class="sxs-lookup"><span data-stu-id="43d5f-160">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="43d5f-161">Stofna nýjan gám, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="43d5f-161">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="43d5f-162">Setjið 3 ea í gám CONT0003.</span><span class="sxs-lookup"><span data-stu-id="43d5f-162">Put 3 ea into container CONT0003.</span></span></li></ol> | <p><span data-ttu-id="43d5f-163">HDMI kapall 18'':</span><span class="sxs-lookup"><span data-stu-id="43d5f-163">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="43d5f-164">Athuga hvort hluturinn geti passað í gám CONT0001.</span><span class="sxs-lookup"><span data-stu-id="43d5f-164">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="43d5f-165">Stofna nýjan gám, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="43d5f-165">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="43d5f-166">Setjið 5 ea í gám CONT0002.</span><span class="sxs-lookup"><span data-stu-id="43d5f-166">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="43d5f-167">Stofna nýjan gám, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="43d5f-167">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="43d5f-168">Setjið 3 ea í gám CONT0003.</span><span class="sxs-lookup"><span data-stu-id="43d5f-168">Put 3 ea into container CONT0003.</span></span></li></ol> |
| <p><span data-ttu-id="43d5f-169">HDMI kapall 6'':</span><span class="sxs-lookup"><span data-stu-id="43d5f-169">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="43d5f-170">Athuga hvort hluturinn geti passað í gám CONT0001.</span><span class="sxs-lookup"><span data-stu-id="43d5f-170">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="43d5f-171">Setjið 1 ea í gám CONT0001.</span><span class="sxs-lookup"><span data-stu-id="43d5f-171">Put 1 ea into container CONT0001.</span></span></li><li><span data-ttu-id="43d5f-172">Athuga hvort hluturinn geti passað í gám CONT0002.</span><span class="sxs-lookup"><span data-stu-id="43d5f-172">Check whether the item can fit into container CONT0002.</span></span></li><li><span data-ttu-id="43d5f-173">Athuga hvort hluturinn geti passað í gám CONT0003.</span><span class="sxs-lookup"><span data-stu-id="43d5f-173">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="43d5f-174">Setjið 4 ea í gám CONT0003.</span><span class="sxs-lookup"><span data-stu-id="43d5f-174">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="43d5f-175">Stofna nýjan gám, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="43d5f-175">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="43d5f-176">Setjið 8 ea í gám CONT0004.</span><span class="sxs-lookup"><span data-stu-id="43d5f-176">Put 8 ea into container CONT0004.</span></span></li></ol> | <p><span data-ttu-id="43d5f-177">HDMI kapall 6'':</span><span class="sxs-lookup"><span data-stu-id="43d5f-177">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="43d5f-178">Athuga hvort hluturinn geti passað í gám CONT0003.</span><span class="sxs-lookup"><span data-stu-id="43d5f-178">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="43d5f-179">Setjið 4 ea í gám CONT0003.</span><span class="sxs-lookup"><span data-stu-id="43d5f-179">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="43d5f-180">Stofna nýjan gám, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="43d5f-180">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="43d5f-181">Setjið 9 ea í gám CONT0004.</span><span class="sxs-lookup"><span data-stu-id="43d5f-181">Put 9 ea into container CONT0004.</span></span></li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a><span data-ttu-id="43d5f-182">Dæmi: Pakka stökum pöntunum í gám</span><span class="sxs-lookup"><span data-stu-id="43d5f-182">Example scenario: Pack single orders per container</span></span>

<span data-ttu-id="43d5f-183">Í þessum hluta eru sýndar aðstæður þar sem kerfið er sett upp til að sameina margar pantanir í eina sendingu.</span><span class="sxs-lookup"><span data-stu-id="43d5f-183">This section presents a scenario where the system is set up to consolidate multiple orders into one shipment.</span></span> <span data-ttu-id="43d5f-184">Því verður gámapökkunin gerð úr sölupöntuninni til að tryggja að hver pöntun sem inniheldur margar afurðir sé pakkað í eigin gám.</span><span class="sxs-lookup"><span data-stu-id="43d5f-184">Therefore, containerization will be done from the sales order to ensure that every order that contains multiple products is packed into its own container.</span></span>

<span data-ttu-id="43d5f-185">Þessi virkni gerir kleift að takast á við aðstæður þar sem aðeins á að pakka einni sölupöntun í hvern gám þannig að dreifingarmiðstöðin geti hjáskipað fulla gáma milli smásöluverslana.</span><span class="sxs-lookup"><span data-stu-id="43d5f-185">This functionality lets you handle scenarios where you must pack only one sales order into each container, so that the distribution center can cross-dock full containers between retail stores.</span></span> <span data-ttu-id="43d5f-186">Til viðbótar við smásöluaðstæður (pöntun fyrir hverja smásöluverslun og sendingu í dreifingarmiðstöð fyrir hjáskipun) er þessi aðferð einnig algeng í venjubundinni aðfangakeðju (sölupöntun í tímanlegri framleiðslulínu).</span><span class="sxs-lookup"><span data-stu-id="43d5f-186">In addition to the retail scenarios (order per retail store and shipping to a distribution center for cross-docking) this technique is also commonly used in lean supply chains (sales order per just-in-time production line).</span></span>

<span data-ttu-id="43d5f-187">Þessar aðstæður sýna hvernig hægt er að fækka fjölda gáma sem eru metnir við pökkun með því að nota stefnuna *Pakka aðeins í núgildandi gám* fyrir gámapökkun.</span><span class="sxs-lookup"><span data-stu-id="43d5f-187">This scenario shows how you can decrease the number of containers that are evaluated during packing by using the *Pack into current container only* strategy for containerization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="43d5f-188">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="43d5f-188">Prerequisites</span></span>

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a><span data-ttu-id="43d5f-189">Kveikja á eiginleika fyrir sameiningu sendingar í kerfinu</span><span class="sxs-lookup"><span data-stu-id="43d5f-189">Turn on the Consolidate shipments feature in your system</span></span>

<span data-ttu-id="43d5f-190">Í þessum aðstæðum er eiginleikinn *Sameina sendingar* notaður.</span><span class="sxs-lookup"><span data-stu-id="43d5f-190">This scenario uses the *Consolidate shipments* feature.</span></span> <span data-ttu-id="43d5f-191">Ef sá eiginleiki er ekki þegar til staðar í kerfinu þarf að kveikja á honum með því að nota [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="43d5f-191">If that feature isn't already available in your system, you must turn it on by using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

#### <a name="make-demo-data-available"></a><span data-ttu-id="43d5f-192">Bjóða upp á sýnigögn</span><span class="sxs-lookup"><span data-stu-id="43d5f-192">Make demo data available</span></span>

<span data-ttu-id="43d5f-193">Þessar aðstæður vísa í gildi og færslur sem eru innifaldar í stöðluðum sýnigögnum fyrir Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="43d5f-193">This scenario references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="43d5f-194">Ef nota á gildin sem er boðið upp á hér eins og í æfingunum skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett og stilla lögaðilann á **USMF** áður en hafist er handa.</span><span class="sxs-lookup"><span data-stu-id="43d5f-194">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

### <a name="inspect-or-create-container-types"></a><span data-ttu-id="43d5f-195">Kanna eða stofna gámagerðir</span><span class="sxs-lookup"><span data-stu-id="43d5f-195">Inspect or create container types</span></span>

<span data-ttu-id="43d5f-196">Til að kanna gámagerðirnar eða stofna nýjar gámagerðir ef þess gerist þörf skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="43d5f-196">To inspect your container types, or to create new container types if they are required, follow these steps.</span></span>

1. <span data-ttu-id="43d5f-197">Fara í **Vöruhúsakerfi** \> **Uppsetning** \> **Gámar** \> **Gámagerðir**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-197">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>
1. <span data-ttu-id="43d5f-198">Gangið úr skugga um að hver eftirfarandi gámagerð sé í boði í sýnigögnunum.</span><span class="sxs-lookup"><span data-stu-id="43d5f-198">Make sure that each of the following container types is available in your demo data.</span></span> <span data-ttu-id="43d5f-199">Breytið eða stofnið gámagerðir eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="43d5f-199">Edit or create container types as required.</span></span>

    - <span data-ttu-id="43d5f-200">Gámagerð 1:</span><span class="sxs-lookup"><span data-stu-id="43d5f-200">Container type 1:</span></span>

        - <span data-ttu-id="43d5f-201">**Kóði gámagerðar:** *Kassi-stór*</span><span class="sxs-lookup"><span data-stu-id="43d5f-201">**Container type code:** *Box-Large*</span></span>
        - <span data-ttu-id="43d5f-202">**Lýsing:** *Stór kassi*.</span><span class="sxs-lookup"><span data-stu-id="43d5f-202">**Description:** *Large Box*</span></span>
        - <span data-ttu-id="43d5f-203">**Hámarksnettóþyngd:** *100*</span><span class="sxs-lookup"><span data-stu-id="43d5f-203">**Maximum net weight:** *100*</span></span>
        - <span data-ttu-id="43d5f-204">**Magn:** *400*</span><span class="sxs-lookup"><span data-stu-id="43d5f-204">**Volume:** *400*</span></span>
        - <span data-ttu-id="43d5f-205">**Lengd:** *4*</span><span class="sxs-lookup"><span data-stu-id="43d5f-205">**Length:** *4*</span></span>
        - <span data-ttu-id="43d5f-206">**Breidd:** *10*</span><span class="sxs-lookup"><span data-stu-id="43d5f-206">**Width:** *10*</span></span>
        - <span data-ttu-id="43d5f-207">**Hæð:** *10*</span><span class="sxs-lookup"><span data-stu-id="43d5f-207">**Height:** *10*</span></span>

    - <span data-ttu-id="43d5f-208">Gámagerð 2:</span><span class="sxs-lookup"><span data-stu-id="43d5f-208">Container type 2:</span></span>

        - <span data-ttu-id="43d5f-209">**Kóði gámagerðar:** *Kassi-miðlungs*</span><span class="sxs-lookup"><span data-stu-id="43d5f-209">**Container type code:** *Box-Medium*</span></span>
        - <span data-ttu-id="43d5f-210">**Lýsing:** *Miðlungsstór kassi*</span><span class="sxs-lookup"><span data-stu-id="43d5f-210">**Description:** *Medium Box*</span></span>
        - <span data-ttu-id="43d5f-211">**Hámarksnettóþyngd:** *50*</span><span class="sxs-lookup"><span data-stu-id="43d5f-211">**Maximum net weight:** *50*</span></span>
        - <span data-ttu-id="43d5f-212">**Magn:** *200*</span><span class="sxs-lookup"><span data-stu-id="43d5f-212">**Volume:** *200*</span></span>
        - <span data-ttu-id="43d5f-213">**Lengd:** *2*</span><span class="sxs-lookup"><span data-stu-id="43d5f-213">**Length:** *2*</span></span>
        - <span data-ttu-id="43d5f-214">**Breidd:** *10*</span><span class="sxs-lookup"><span data-stu-id="43d5f-214">**Width:** *10*</span></span>
        - <span data-ttu-id="43d5f-215">**Hæð:** *10*</span><span class="sxs-lookup"><span data-stu-id="43d5f-215">**Height:** *10*</span></span>

    - <span data-ttu-id="43d5f-216">Gámagerð 3:</span><span class="sxs-lookup"><span data-stu-id="43d5f-216">Container type 3:</span></span>

        - <span data-ttu-id="43d5f-217">**Kóði gámagerðar:** *Kassi-lítill*</span><span class="sxs-lookup"><span data-stu-id="43d5f-217">**Container type code:** *Box-Small*</span></span>
        - <span data-ttu-id="43d5f-218">**Lýsing:** *Lítill kassi*.</span><span class="sxs-lookup"><span data-stu-id="43d5f-218">**Description:** *Small Box*</span></span>
        - <span data-ttu-id="43d5f-219">**Hámarksnettóþyngd:** *20*</span><span class="sxs-lookup"><span data-stu-id="43d5f-219">**Maximum net weight:** *20*</span></span>
        - <span data-ttu-id="43d5f-220">**Magn:** *100*</span><span class="sxs-lookup"><span data-stu-id="43d5f-220">**Volume:** *100*</span></span>
        - <span data-ttu-id="43d5f-221">**Lengd:** *1*</span><span class="sxs-lookup"><span data-stu-id="43d5f-221">**Length:** *1*</span></span>
        - <span data-ttu-id="43d5f-222">**Breidd:** *10*</span><span class="sxs-lookup"><span data-stu-id="43d5f-222">**Width:** *10*</span></span>
        - <span data-ttu-id="43d5f-223">**Hæð:** *10*</span><span class="sxs-lookup"><span data-stu-id="43d5f-223">**Height:** *10*</span></span>

### <a name="inspect-or-create-container-groups"></a><span data-ttu-id="43d5f-224">Kanna eða stofna gámaflokka</span><span class="sxs-lookup"><span data-stu-id="43d5f-224">Inspect or create container groups</span></span>

<span data-ttu-id="43d5f-225">Til að kanna gámaflokkana eða stofna nýja gámaflokka ef þess gerist þörf skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="43d5f-225">To inspect your container groups, or to create new container groups if they are required, follow these steps.</span></span>

1. <span data-ttu-id="43d5f-226">Fara í **Vöruhúsakerfi** \> **Uppsetning** \> **Gámar** \> **Gámahópar**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-226">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**.</span></span>
1. <span data-ttu-id="43d5f-227">Gangið úr skugga um að eftirfarandi gámagerð sé í boði í sýnigögnunum.</span><span class="sxs-lookup"><span data-stu-id="43d5f-227">Make sure that the following container group is available in your demo data.</span></span> <span data-ttu-id="43d5f-228">Ef hún er ekki tiltæk skal velja **Ný** til að búa hana til.</span><span class="sxs-lookup"><span data-stu-id="43d5f-228">If it isn't available, select **New** to create it.</span></span>

    - <span data-ttu-id="43d5f-229">**Auðkenni gámaflokks:** *Kassar*</span><span class="sxs-lookup"><span data-stu-id="43d5f-229">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="43d5f-230">**Lýsing:** *Kassastærðir*</span><span class="sxs-lookup"><span data-stu-id="43d5f-230">**Description:** *Box sizes*</span></span>

1. <span data-ttu-id="43d5f-231">Í flýtiflipanum **Upplýsingar** fyrir gámaflokkinn *Kassar* skal ganga úr skugga um að eftirfarandi línur séu til.</span><span class="sxs-lookup"><span data-stu-id="43d5f-231">On the **Details** FastTab for the *Boxes* container group, make sure that the following lines exist.</span></span> <span data-ttu-id="43d5f-232">Ef þær eru ekki til skal velja **Ný** til að bæta þeim við.</span><span class="sxs-lookup"><span data-stu-id="43d5f-232">If they don't, select **New** to add them.</span></span>

    - <span data-ttu-id="43d5f-233">Lína 1:</span><span class="sxs-lookup"><span data-stu-id="43d5f-233">Line 1:</span></span>

        - <span data-ttu-id="43d5f-234">**Raðnúmer:** *1*</span><span class="sxs-lookup"><span data-stu-id="43d5f-234">**Sequence number:** *1*</span></span>
        - <span data-ttu-id="43d5f-235">**Gámagerð:** *Kassi-stór*</span><span class="sxs-lookup"><span data-stu-id="43d5f-235">**Container type:** *Box-Large*</span></span>
        - <span data-ttu-id="43d5f-236">**Prósentunýting gáms:** *100*</span><span class="sxs-lookup"><span data-stu-id="43d5f-236">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="43d5f-237">Lína 2:</span><span class="sxs-lookup"><span data-stu-id="43d5f-237">Line 2:</span></span>

        - <span data-ttu-id="43d5f-238">**Raðnúmer:** *2*</span><span class="sxs-lookup"><span data-stu-id="43d5f-238">**Sequence number:** *2*</span></span>
        - <span data-ttu-id="43d5f-239">**Gámagerð:** *Kassi-miðlungs*</span><span class="sxs-lookup"><span data-stu-id="43d5f-239">**Container type:** *Box-Medium*</span></span>
        - <span data-ttu-id="43d5f-240">**Prósentunýting gáms:** *100*</span><span class="sxs-lookup"><span data-stu-id="43d5f-240">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="43d5f-241">Lína 3:</span><span class="sxs-lookup"><span data-stu-id="43d5f-241">Line 3:</span></span>

        - <span data-ttu-id="43d5f-242">**Raðnúmer:** *3*</span><span class="sxs-lookup"><span data-stu-id="43d5f-242">**Sequence number:** *3*</span></span>
        - <span data-ttu-id="43d5f-243">**Gámagerð:** *Kassi-lítill*</span><span class="sxs-lookup"><span data-stu-id="43d5f-243">**Container type:** *Box-Small*</span></span>
        - <span data-ttu-id="43d5f-244">**Prósentunýting gáms:** *100*</span><span class="sxs-lookup"><span data-stu-id="43d5f-244">**Container utilization percentage:** *100*</span></span>

### <a name="create-a-new-container-build-template"></a><span data-ttu-id="43d5f-245">Stofnið nýtt gámaröðunarsniðmát</span><span class="sxs-lookup"><span data-stu-id="43d5f-245">Create a new container build template</span></span>

<span data-ttu-id="43d5f-246">Til að stofna nýtt gámaröðunarsniðmát skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="43d5f-246">To create a new container build template, follow these steps.</span></span>

1. <span data-ttu-id="43d5f-247">Fara í **Vöruhúsakerfi** \> **Uppsetning** \> **Gámar** \> **Gámaröðunarsniðmát**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-247">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container build template**.</span></span>
1. <span data-ttu-id="43d5f-248">Veljið **Nýtt** til að stofna gámaröðunarsniðmát sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="43d5f-248">Select **New** to create a container build template that has the following settings:</span></span>

    - <span data-ttu-id="43d5f-249">**Raðnúmer:** *1*</span><span class="sxs-lookup"><span data-stu-id="43d5f-249">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="43d5f-250">**Kenni gámasniðmáts:** *Kassi*</span><span class="sxs-lookup"><span data-stu-id="43d5f-250">**Container template ID:** *Box*</span></span>
    - <span data-ttu-id="43d5f-251">**Auðkenni gámaflokks:** *Kassar*</span><span class="sxs-lookup"><span data-stu-id="43d5f-251">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="43d5f-252">**Grunngerðir fyrirspurnar:** *Úthlutunarlína sölu*</span><span class="sxs-lookup"><span data-stu-id="43d5f-252">**Base query types:** *Sales allocation line*</span></span>
    - <span data-ttu-id="43d5f-253">**Kóði bylgjuskrefs:** *234*</span><span class="sxs-lookup"><span data-stu-id="43d5f-253">**Wave step code:** *234*</span></span>
    - <span data-ttu-id="43d5f-254">**Leyfa skiptar tiltektir:** *Já*</span><span class="sxs-lookup"><span data-stu-id="43d5f-254">**Allow split picks:** *Yes*</span></span>
    - <span data-ttu-id="43d5f-255">**Aðferð gámapökkunar:** *Pakka aðeins í núgildandi gám*</span><span class="sxs-lookup"><span data-stu-id="43d5f-255">**Container packing strategy:** *Pack into current container only*</span></span>
    - <span data-ttu-id="43d5f-256">**Pakka eftir leiðbeiningareiningu:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="43d5f-256">**Pack by directive unit:** *No*</span></span>

1. <span data-ttu-id="43d5f-257">Á meðan línan fyrir nýja sniðmátið er enn valin skal velja **Breyta fyrirspurn** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="43d5f-257">While the row for the new template is still selected, select **Edit query** on the Action Pane.</span></span>
1. <span data-ttu-id="43d5f-258">Venjulegur svargluggi fyrirspurnarritils birtist.</span><span class="sxs-lookup"><span data-stu-id="43d5f-258">A standard query editor dialog box appears.</span></span> <span data-ttu-id="43d5f-259">Í flipanum **Röðun** skal velja **Bæta við** til að bæta við línu sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="43d5f-259">On the **Sorting** tab, select **Add** to add a row that has the following settings:</span></span>

    - <span data-ttu-id="43d5f-260">**Tafla:** *Tímabundnar vinnufærslur*</span><span class="sxs-lookup"><span data-stu-id="43d5f-260">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="43d5f-261">**Afleidd tafla:** *Tímabundnar vinnufærslur*</span><span class="sxs-lookup"><span data-stu-id="43d5f-261">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="43d5f-262">**Reitur:** *Pöntunarnúmer*</span><span class="sxs-lookup"><span data-stu-id="43d5f-262">**Field:** *Order number*</span></span>
    - <span data-ttu-id="43d5f-263">**Leitarstefna:** *Hækkandi*</span><span class="sxs-lookup"><span data-stu-id="43d5f-263">**Search direction:** *Ascending*</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="43d5f-264">Til að koma í veg fyrir að fara yfir alla aðra opna gáma og til að hraða ferlinu með því að athuga einn gám í einu, skal nota aðferðina *Pakka aðeins í núgildandi gám* ásamt röðun eftir pöntunarnúmeri.</span><span class="sxs-lookup"><span data-stu-id="43d5f-264">To avoid cycling over all the other open containers, and to speed up the process by checking one container at a time, use the *Pack into current container only* strategy in addition to sorting by order number.</span></span> <span data-ttu-id="43d5f-265">Þessi samsetning mun virka eins og vinnuhlé á vinnusniðmáti.</span><span class="sxs-lookup"><span data-stu-id="43d5f-265">This combination will work like a work break on a work template.</span></span>

1. <span data-ttu-id="43d5f-266">Veldu **Í lagi** til að loka svarglugga fyrirspurnarritils.</span><span class="sxs-lookup"><span data-stu-id="43d5f-266">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="43d5f-267">Á meðan línan fyrir nýja sniðmátið er enn valin skal velja **Takmarkanir á blöndun gáma** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="43d5f-267">While the row for the new template is still selected, select **Container mixing constraints** on the Action Pane.</span></span>

    <span data-ttu-id="43d5f-268">Nú bætirðu takmörkun við sem setur vörur úr einni pöntun í einn gám.</span><span class="sxs-lookup"><span data-stu-id="43d5f-268">You will now add a constraint that puts items from a single order into a single container.</span></span> <span data-ttu-id="43d5f-269">Vörur úr öðrum pöntunum verða settar í annan gám.</span><span class="sxs-lookup"><span data-stu-id="43d5f-269">Items from any other order will be put into a separate container.</span></span>

1. <span data-ttu-id="43d5f-270">Veljið **Ný** til að búa til takmörkun blöndunar sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="43d5f-270">Select **New** to create a mixing constraint that has the following settings:</span></span>

    - <span data-ttu-id="43d5f-271">**Tafla:** *Sölupantanir*</span><span class="sxs-lookup"><span data-stu-id="43d5f-271">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="43d5f-272">**Reitur valinn:** *SalesId* (reiturinn birtist sem *Sölupöntun* í hnitanetinu.)</span><span class="sxs-lookup"><span data-stu-id="43d5f-272">**Field select:** *SalesId* (The field will appear as *Sales order* in the grid.)</span></span>

1. <span data-ttu-id="43d5f-273">Veljið **Í lagi** til að bæta takmörkuninni við.</span><span class="sxs-lookup"><span data-stu-id="43d5f-273">Select **OK** to add the constraint.</span></span>
1. <span data-ttu-id="43d5f-274">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="43d5f-274">Close the page.</span></span>

### <a name="set-up-a-wave-template-for-containerization"></a><span data-ttu-id="43d5f-275">Setja upp bylgjusniðmát fyrir gámun</span><span class="sxs-lookup"><span data-stu-id="43d5f-275">Set up a wave template for containerization</span></span>

<span data-ttu-id="43d5f-276">Til að setja upp bylgjusniðmát skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="43d5f-276">To set up a wave template, follow these steps.</span></span>

1. <span data-ttu-id="43d5f-277">Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-277">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="43d5f-278">Í listaglugganum skal stilla reitinn **Gerð bylgjusniðmáts** á *Sending*.</span><span class="sxs-lookup"><span data-stu-id="43d5f-278">In the list pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="43d5f-279">Veljið sniðmátið **63 Gámun** úr listanum.</span><span class="sxs-lookup"><span data-stu-id="43d5f-279">Select the **63 Containerization** template in the list.</span></span>
1. <span data-ttu-id="43d5f-280">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-280">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="43d5f-281">Í flýtiflipanum **Aðferðir**, í dálknum **Valdar aðferðir**, skal finna eftirfarandi línu:</span><span class="sxs-lookup"><span data-stu-id="43d5f-281">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="43d5f-282">**Heiti aðferðar:** *gámun*</span><span class="sxs-lookup"><span data-stu-id="43d5f-282">**Method name:** *containerization*</span></span>
    - <span data-ttu-id="43d5f-283">**Heiti:** *Gámun*</span><span class="sxs-lookup"><span data-stu-id="43d5f-283">**Name:** *Containerization*</span></span>

1. <span data-ttu-id="43d5f-284">Stillið reitinn **Kóði bylgjuskrefs** fyrir þessa línu á *234*.</span><span class="sxs-lookup"><span data-stu-id="43d5f-284">Set the **Wave step code** field for the line to *234*.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="43d5f-285">Setja upp vinnusniðmát</span><span class="sxs-lookup"><span data-stu-id="43d5f-285">Set up a work template</span></span>

<span data-ttu-id="43d5f-286">Fylgið þessum skrefum til þess að setja upp vinnusniðmát.</span><span class="sxs-lookup"><span data-stu-id="43d5f-286">To set up a work template, follow these steps.</span></span>

1. <span data-ttu-id="43d5f-287">Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-287">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="43d5f-288">Stillið reitinn **Gerð verkbeiðni** á *Sölupantanir*.</span><span class="sxs-lookup"><span data-stu-id="43d5f-288">Set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="43d5f-289">Í hnitanetinu **Yfirlit** skal finna og velja vinnusniðmátið sem á að nota fyrir pökun á stökum pöntunum í hvern gám.</span><span class="sxs-lookup"><span data-stu-id="43d5f-289">In the **Overview** grid, find and select the work template that should be used for packing single orders per container.</span></span> <span data-ttu-id="43d5f-290">Fyrir þessar aðstæður skal velja sniðmátið **63 Tiltekt í gám**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-290">For this scenario, select the **63 Pick to container** template.</span></span>
1. <span data-ttu-id="43d5f-291">Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-291">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="43d5f-292">Venjulegur svargluggi fyrirspurnarritils birtist.</span><span class="sxs-lookup"><span data-stu-id="43d5f-292">A standard query editor dialog box appears.</span></span> <span data-ttu-id="43d5f-293">Í flipanum **Röðun** skal bæta við eftirfarandi línum:</span><span class="sxs-lookup"><span data-stu-id="43d5f-293">On the **Sorting** tab, add the following lines:</span></span>

    - <span data-ttu-id="43d5f-294">Lína 1:</span><span class="sxs-lookup"><span data-stu-id="43d5f-294">Line 1:</span></span>

        - <span data-ttu-id="43d5f-295">**Tafla:** *Tímabundnar vinnufærslur*</span><span class="sxs-lookup"><span data-stu-id="43d5f-295">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="43d5f-296">**Afleidd tafla:** *Tímabundnar vinnufærslur*</span><span class="sxs-lookup"><span data-stu-id="43d5f-296">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="43d5f-297">**Reitur:** *Auðkenni sendingar*</span><span class="sxs-lookup"><span data-stu-id="43d5f-297">**Field:** *Shipment ID*</span></span>
        - <span data-ttu-id="43d5f-298">**Leitarstefna:** *Hækkandi*</span><span class="sxs-lookup"><span data-stu-id="43d5f-298">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="43d5f-299">Lína 2:</span><span class="sxs-lookup"><span data-stu-id="43d5f-299">Line 2:</span></span>

        - <span data-ttu-id="43d5f-300">**Tafla:** *Tímabundnar vinnufærslur*</span><span class="sxs-lookup"><span data-stu-id="43d5f-300">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="43d5f-301">**Afleidd tafla:** *Tímabundnar vinnufærslur*</span><span class="sxs-lookup"><span data-stu-id="43d5f-301">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="43d5f-302">**Reitur:** *Pöntunarnúmer*</span><span class="sxs-lookup"><span data-stu-id="43d5f-302">**Field:** *Order number*</span></span>
        - <span data-ttu-id="43d5f-303">**Leitarstefna:** *Hækkandi*</span><span class="sxs-lookup"><span data-stu-id="43d5f-303">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="43d5f-304">Lína 3:</span><span class="sxs-lookup"><span data-stu-id="43d5f-304">Line 3:</span></span>

        - <span data-ttu-id="43d5f-305">**Tafla:** *Tímabundnar vinnufærslur*</span><span class="sxs-lookup"><span data-stu-id="43d5f-305">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="43d5f-306">**Afleidd tafla:** *Tímabundnar vinnufærslur*</span><span class="sxs-lookup"><span data-stu-id="43d5f-306">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="43d5f-307">**Reitur:** *Auðkenni gáms*</span><span class="sxs-lookup"><span data-stu-id="43d5f-307">**Field:** *Container ID*</span></span>
        - <span data-ttu-id="43d5f-308">**Leitarstefna:** *Hækkandi*</span><span class="sxs-lookup"><span data-stu-id="43d5f-308">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="43d5f-309">Veldu **Í lagi** til að loka svarglugga fyrirspurnarritils.</span><span class="sxs-lookup"><span data-stu-id="43d5f-309">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="43d5f-310">Eftirfarandi skilaboð birtast: „Flokkun verður endurstillt, á að halda áfram?"</span><span class="sxs-lookup"><span data-stu-id="43d5f-310">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="43d5f-311">Veldu **Já** til að halda áfram.</span><span class="sxs-lookup"><span data-stu-id="43d5f-311">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="43d5f-312">Á meðan sniðmátið **63 Tiltekt í gám** er enn valið skal velja **Vinnuhausaskil** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="43d5f-312">While the **63 Pick to container** template is still selected, select **Work header breaks** on the Action Pane.</span></span>

    <span data-ttu-id="43d5f-313">Nú notarðu stillingar til að sundurliða vinnunni þannig að hver gámur í pöntuninni er tengdur við eina verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="43d5f-313">You will now apply settings to break the work so that each container in the order is linked to one work order.</span></span>

1. <span data-ttu-id="43d5f-314">Veljið gátreitinn **Flokka eftir þessum reit** fyrir hverja línu á síðunni **Vinnuhausaskil** (**Auðkenni sendingar**, **Pöntunarnúmer** og **Auðkenni gáms**).</span><span class="sxs-lookup"><span data-stu-id="43d5f-314">Select the **Group by this field** checkbox for each row on the **Work header breaks** page (**Shipment ID**, **Order number**, and **Container ID**).</span></span>
1. <span data-ttu-id="43d5f-315">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="43d5f-315">Close the page.</span></span>

### <a name="set-up-shipment-consolidation-policies"></a><span data-ttu-id="43d5f-316">Setja upp samstæðureglur sendingar</span><span class="sxs-lookup"><span data-stu-id="43d5f-316">Set up shipment consolidation policies</span></span>

<span data-ttu-id="43d5f-317">Til að setja upp samstæðureglur sendingar skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="43d5f-317">To set up a shipment consolidation policy, follow these steps.</span></span>

1. <span data-ttu-id="43d5f-318">Opnið **Vöruhúsastjórnun \> Uppsetning \> Losa í vöruhús \> Samstæðureglur sendingar**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-318">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="43d5f-319">Á listasvæðinu skal stilla reitinn **Gerð stefnu** á *Sölupantanir*.</span><span class="sxs-lookup"><span data-stu-id="43d5f-319">In the list pane, set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="43d5f-320">Veljið stefnuna **Sjálfgefið** úr listanum.</span><span class="sxs-lookup"><span data-stu-id="43d5f-320">Select the **Default** policy in the list.</span></span>
1. <span data-ttu-id="43d5f-321">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-321">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="43d5f-322">Í flýtiflipanum **Samstæðureitir**, í listanum **Valdir reitir**, skal velja línuna þar sem reiturinn **Heiti reits** er stilltur á *Pöntun viðskiptavinar*.</span><span class="sxs-lookup"><span data-stu-id="43d5f-322">On the **Consolidation fields** FastTab, in the **Selected fields** list, select the row where the **Field name** field is set to *Order number*.</span></span>
1. <span data-ttu-id="43d5f-323">Veljið hnappinn **Fjarlægja** ![Vinstri ör](media/backward-button.png) til að færa reitinn á listann yfir **Eftirstandandi reiti**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-323">Select the **Remove** button ![Left arrow](media/backward-button.png) to move the field to the **Remaining fields** list.</span></span>
1. <span data-ttu-id="43d5f-324">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-324">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-physical-dimensions-for-the-product"></a><span data-ttu-id="43d5f-325">Setja upp efnislegar víddir fyrir afurðina</span><span class="sxs-lookup"><span data-stu-id="43d5f-325">Set up physical dimensions for the product</span></span>

<span data-ttu-id="43d5f-326">Til að setja upp efnislegar víddir fyrir afurðir sem verða notaðar í þessum aðstæðum skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="43d5f-326">To set up physical dimensions for the products that will be used in this scenario, follow these steps.</span></span>

1. <span data-ttu-id="43d5f-327">Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-327">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="43d5f-328">Veljið afurðina þar sem reiturinn **Vörunúmer** er stilltur á *A0001*.</span><span class="sxs-lookup"><span data-stu-id="43d5f-328">Select the product where the **Item number** field is set to *A0001*.</span></span>
1. <span data-ttu-id="43d5f-329">Á Aðgerðasvæði, á flipanum **Stjórna birgðum**, í flokknum **Vöruhús**, velurðu **Efnislegar víddir**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-329">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="43d5f-330">Á síðunni **Efnislegar víddir** ætti að nota eftirfarandi línu í hnitanetinu:</span><span class="sxs-lookup"><span data-stu-id="43d5f-330">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="43d5f-331">**Eining:** *stk.*</span><span class="sxs-lookup"><span data-stu-id="43d5f-331">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="43d5f-332">**Heildarþyngd:** *3.00*</span><span class="sxs-lookup"><span data-stu-id="43d5f-332">**Gross weight:** *3.00*</span></span>
    - <span data-ttu-id="43d5f-333">**Breidd:** *2.00*</span><span class="sxs-lookup"><span data-stu-id="43d5f-333">**Width:** *2.00*</span></span>
    - <span data-ttu-id="43d5f-334">**Dýpt:** *2.00*</span><span class="sxs-lookup"><span data-stu-id="43d5f-334">**Depth:** *2.00*</span></span>
    - <span data-ttu-id="43d5f-335">**Hæð:** *4.00*</span><span class="sxs-lookup"><span data-stu-id="43d5f-335">**Height:** *4.00*</span></span>
    - <span data-ttu-id="43d5f-336">**Magn:** *16.00*</span><span class="sxs-lookup"><span data-stu-id="43d5f-336">**Volume:** *16.00*</span></span>

1. <span data-ttu-id="43d5f-337">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="43d5f-337">Close the page.</span></span>
1. <span data-ttu-id="43d5f-338">Veljið afurðina þar sem reiturinn **Vörunúmer** er stilltur á *A0002*.</span><span class="sxs-lookup"><span data-stu-id="43d5f-338">Select the product where the **Item number** field is set to *A0002*.</span></span>
1. <span data-ttu-id="43d5f-339">Á Aðgerðasvæði, á flipanum **Stjórna birgðum**, í flokknum **Vöruhús**, velurðu **Efnislegar víddir**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-339">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="43d5f-340">Á síðunni **Efnislegar víddir** ætti að nota eftirfarandi línu í hnitanetinu:</span><span class="sxs-lookup"><span data-stu-id="43d5f-340">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="43d5f-341">**Eining:** *stk.*</span><span class="sxs-lookup"><span data-stu-id="43d5f-341">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="43d5f-342">**Heildarþyngd:** *4.00*</span><span class="sxs-lookup"><span data-stu-id="43d5f-342">**Gross weight:** *4.00*</span></span>
    - <span data-ttu-id="43d5f-343">**Breidd:** *3.00*</span><span class="sxs-lookup"><span data-stu-id="43d5f-343">**Width:** *3.00*</span></span>
    - <span data-ttu-id="43d5f-344">**Dýpt:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="43d5f-344">**Depth:** *1.00*</span></span>
    - <span data-ttu-id="43d5f-345">**Hæð:** *3.00*</span><span class="sxs-lookup"><span data-stu-id="43d5f-345">**Height:** *3.00*</span></span>
    - <span data-ttu-id="43d5f-346">**Magn:** *9.00*</span><span class="sxs-lookup"><span data-stu-id="43d5f-346">**Volume:** *9.00*</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="43d5f-347">Stofna sölupöntun 1</span><span class="sxs-lookup"><span data-stu-id="43d5f-347">Create sales order 1</span></span>

<span data-ttu-id="43d5f-348">Til að stofna sölupöntun, skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="43d5f-348">To create a sales order, follow these steps.</span></span>

1. <span data-ttu-id="43d5f-349">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-349">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="43d5f-350">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-350">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="43d5f-351">Svargluggi fyrir stofnun nýrrar sölupöntunar birtist.</span><span class="sxs-lookup"><span data-stu-id="43d5f-351">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="43d5f-352">Stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="43d5f-352">Set the following values:</span></span>

    - <span data-ttu-id="43d5f-353">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="43d5f-353">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="43d5f-354">**Vöruhús:** *63*</span><span class="sxs-lookup"><span data-stu-id="43d5f-354">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="43d5f-355">Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="43d5f-355">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="43d5f-356">Ný sölupöntun opnast.</span><span class="sxs-lookup"><span data-stu-id="43d5f-356">The new sales order is opened.</span></span> <span data-ttu-id="43d5f-357">Í flýtiflipanum **Sölupöntunarlínur** skal bæta við eftirfarandi sölulínum:</span><span class="sxs-lookup"><span data-stu-id="43d5f-357">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="43d5f-358">Lína 1:</span><span class="sxs-lookup"><span data-stu-id="43d5f-358">Line 1:</span></span>

        - <span data-ttu-id="43d5f-359">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="43d5f-359">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="43d5f-360">**Magn:** *2*</span><span class="sxs-lookup"><span data-stu-id="43d5f-360">**Quantity:** *2*</span></span>

    - <span data-ttu-id="43d5f-361">Lína 2:</span><span class="sxs-lookup"><span data-stu-id="43d5f-361">Line 2:</span></span>

        - <span data-ttu-id="43d5f-362">**Vörunúmer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="43d5f-362">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="43d5f-363">**Magn:** *2*</span><span class="sxs-lookup"><span data-stu-id="43d5f-363">**Quantity:** *2*</span></span>

1. <span data-ttu-id="43d5f-364">Veljið fyrstu línuna og svo **Birgðir \> Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-364">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="43d5f-365">Á síðunni **Frátekning** skal velja **Frátektarlota**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-365">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="43d5f-366">Því næst skal loka síðunni.</span><span class="sxs-lookup"><span data-stu-id="43d5f-366">Then close the page.</span></span>
1. <span data-ttu-id="43d5f-367">Endurtaka skal fyrri tvö skref fyrir seinni línuna.</span><span class="sxs-lookup"><span data-stu-id="43d5f-367">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="43d5f-368">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="43d5f-368">Close the page.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="43d5f-369">Stofna sölupöntun 2</span><span class="sxs-lookup"><span data-stu-id="43d5f-369">Create sales order 2</span></span>

<span data-ttu-id="43d5f-370">Til að stofna aðra sölupöntun skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="43d5f-370">To create a second sales order, follow these steps.</span></span>

1. <span data-ttu-id="43d5f-371">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-371">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="43d5f-372">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-372">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="43d5f-373">Svargluggi fyrir stofnun nýrrar sölupöntunar birtist.</span><span class="sxs-lookup"><span data-stu-id="43d5f-373">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="43d5f-374">Stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="43d5f-374">Set the following values:</span></span>

    - <span data-ttu-id="43d5f-375">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="43d5f-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="43d5f-376">**Vöruhús:** *63*</span><span class="sxs-lookup"><span data-stu-id="43d5f-376">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="43d5f-377">Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="43d5f-377">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="43d5f-378">Ný sölupöntun opnast.</span><span class="sxs-lookup"><span data-stu-id="43d5f-378">The new sales order is opened.</span></span> <span data-ttu-id="43d5f-379">Í flýtiflipanum **Sölupöntunarlínur** skal bæta við eftirfarandi sölulínum:</span><span class="sxs-lookup"><span data-stu-id="43d5f-379">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="43d5f-380">Lína 1:</span><span class="sxs-lookup"><span data-stu-id="43d5f-380">Line 1:</span></span>

        - <span data-ttu-id="43d5f-381">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="43d5f-381">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="43d5f-382">**Magn:** *4*</span><span class="sxs-lookup"><span data-stu-id="43d5f-382">**Quantity:** *4*</span></span>

    - <span data-ttu-id="43d5f-383">Lína 2:</span><span class="sxs-lookup"><span data-stu-id="43d5f-383">Line 2:</span></span>

        - <span data-ttu-id="43d5f-384">**Vörunúmer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="43d5f-384">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="43d5f-385">**Magn:** *4*</span><span class="sxs-lookup"><span data-stu-id="43d5f-385">**Quantity:** *4*</span></span>

1. <span data-ttu-id="43d5f-386">Veljið fyrstu línuna og svo **Birgðir \> Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-386">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="43d5f-387">Á síðunni **Frátekning** skal velja **Frátektarlota**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-387">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="43d5f-388">Því næst skal loka síðunni.</span><span class="sxs-lookup"><span data-stu-id="43d5f-388">Then close the page.</span></span>
1. <span data-ttu-id="43d5f-389">Endurtaka skal fyrri tvö skref fyrir seinni línuna.</span><span class="sxs-lookup"><span data-stu-id="43d5f-389">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="43d5f-390">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="43d5f-390">Close the page.</span></span>

### <a name="create-the-load"></a><span data-ttu-id="43d5f-391">Stofna hleðsluna</span><span class="sxs-lookup"><span data-stu-id="43d5f-391">Create the load</span></span>

<span data-ttu-id="43d5f-392">Fylgið þessum skrefum til að búa til hleðslu fyrir hverja pöntun sem stofnuð var fyrir þessar aðstæður og losa hana síðan í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="43d5f-392">To create a load for each order that you created for this scenario and then release it to the warehouse, follow these steps.</span></span>

1. <span data-ttu-id="43d5f-393">Farið í **Vöruhúsakerfi \> Hleðsla \> Vinnusvæði hleðsluáætlunar**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-393">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="43d5f-394">Í flipanum **Sölulínur** skal finna og velja allar sölupöntunarlínur úr sölupöntununum sem voru stofnaðar fyrir þessar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="43d5f-394">On the **Sales lines** tab, find and select all the sales order lines from the sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="43d5f-395">Á aðgerðasvæðinu, í flipanum **Framboð og eftirspurn**, í flokknum **Bæta við**, skal velja **Við nýjan farm**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-395">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span> <span data-ttu-id="43d5f-396">Völdum pöntunarlínum er bætt við nýja hleðslu.</span><span class="sxs-lookup"><span data-stu-id="43d5f-396">The selected order lines are added to a new load.</span></span>
1. <span data-ttu-id="43d5f-397">Í svarglugganum **Úthlutun hleðslusniðmáts** í reitnum **Kenni hleðslusniðmáts** skal velja hleðslusniðmát, svo sem *40 feta gámur*.</span><span class="sxs-lookup"><span data-stu-id="43d5f-397">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *40' Container*.</span></span>
1. <span data-ttu-id="43d5f-398">Veldu **Í lagi** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="43d5f-398">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="43d5f-399">Í hlutanum **Hleðsla** er hægt að finna og velja hleðsluna sem var verið að stofna.</span><span class="sxs-lookup"><span data-stu-id="43d5f-399">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="43d5f-400">Veljið **Losa \> Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-400">Select **Release \> Release to warehouse**.</span></span>
1. <span data-ttu-id="43d5f-401">Í svarglugganum **Losa í vöruhús** skal velja **Í lagi** til að losa valda hleðslu í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="43d5f-401">In the **Release to warehouse** dialog box, select **OK** to release the selected load to the warehouse.</span></span>

### <a name="verify-the-shipments-and-containers"></a><span data-ttu-id="43d5f-402">Sannreyna sendingar og gáma</span><span class="sxs-lookup"><span data-stu-id="43d5f-402">Verify the shipments and containers</span></span>

<span data-ttu-id="43d5f-403">Eftirfarandi ferli gerir kleift að staðfesta sendingarnar sem hafa verið stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="43d5f-403">The following procedure lets you verify the shipments that have been created.</span></span> <span data-ttu-id="43d5f-404">Notið það til að yfirfara pöntunina sem var stofnuð fyrir þessar aðstæður og gangið úr skugga um að hafa fengið væntanlegar niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="43d5f-404">Use it to review the order that you created for this scenario, to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="43d5f-405">Opnið **Vöruhúsakerfi \> Sendingar \> Allar sendingar**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-405">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="43d5f-406">Finnið og veljið sendinguna sem var stofnuð fyrir hleðsluna sem var verið að losa.</span><span class="sxs-lookup"><span data-stu-id="43d5f-406">Find and select the shipment that was created for the load that you just released.</span></span>
1. <span data-ttu-id="43d5f-407">Á aðgerðasvæðinu, í flipanum **Flutningur**, skal velja **Skoða gáma**.</span><span class="sxs-lookup"><span data-stu-id="43d5f-407">On the Action Pane, on the **Transportation** tab, select **View containers**.</span></span>
1. <span data-ttu-id="43d5f-408">Staðfestið að vörurnar úr sölupöntununum hafi verið pakkaðar í tvo mismunandi gáma.</span><span class="sxs-lookup"><span data-stu-id="43d5f-408">Confirm that the items from the sales orders were containerized into two different containers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="43d5f-409">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="43d5f-409">Additional resources</span></span>

- [<span data-ttu-id="43d5f-410">Gámun</span><span class="sxs-lookup"><span data-stu-id="43d5f-410">Containerization</span></span>](wave-containerization.md)
