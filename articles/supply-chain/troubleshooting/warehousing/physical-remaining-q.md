---
title: Eftirstöðvar efnislegs magns í einingunni má ekki vera núll
description: Þegar fylgiseðill er myndaður hafa gögnin sem fylgja honum birgðamagn sem er ekki núll heldur sölumagn sem er núll.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248786"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a><span data-ttu-id="c2599-103">Eftirstöðvar efnislegs magns í einingunni má ekki vera núll</span><span class="sxs-lookup"><span data-stu-id="c2599-103">Physical remaining quantity in the unit must not be zero</span></span>

<span data-ttu-id="c2599-104">Villukóði SYS19591</span><span class="sxs-lookup"><span data-stu-id="c2599-104">Error code: SYS19591</span></span>

## <a name="symptoms"></a><span data-ttu-id="c2599-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="c2599-105">Symptoms</span></span>

<span data-ttu-id="c2599-106">Þegar fylgiseðill er myndaður hafa gögnin sem fylgja honum birgðamagn sem er ekki núll heldur sölumagn sem er núll.</span><span class="sxs-lookup"><span data-stu-id="c2599-106">When you generate a packing slip, the data that is supplied to it has a non-zero inventory quantity but a zero sales quantity.</span></span>

<span data-ttu-id="c2599-107">Þegar reynt er að búa til fylgiseðilinn sýnir kerfið eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="c2599-107">When you try to generate the packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="c2599-108">Efnislegar eftirstöðvar í einingunni %1 verða að vera annað en núll.</span><span class="sxs-lookup"><span data-stu-id="c2599-108">Physical remaining quantity in the unit %1 must be other than zero.</span></span>

<span data-ttu-id="c2599-109">Því er ekki hægt að búa til fylgiseðil fyrir hleðsluna.</span><span class="sxs-lookup"><span data-stu-id="c2599-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="c2599-110">Orsök</span><span class="sxs-lookup"><span data-stu-id="c2599-110">Cause</span></span>

<span data-ttu-id="c2599-111">Kerfið metur eftirstandandi efnislegt magn í birgðaeiningunni og eftirstandandi efnislegt magn í sendingareiningunni.</span><span class="sxs-lookup"><span data-stu-id="c2599-111">The system evaluates the physical remaining quantity in the inventory unit and the physical remaining quantity in the shipping unit.</span></span> <span data-ttu-id="c2599-112">Ef kerfið kemst að því að eftirstandandi magn í sendingareiningunni er 0 (núll), en eftirstandandi efnislegt magn í birgðaeiningunni er ekki 0, getur þú ekki búið til fylgiseðilinn.</span><span class="sxs-lookup"><span data-stu-id="c2599-112">If the system finds that the physical remaining quantity in the shipping unit is 0 (zero), but the physical remaining quantity in the inventory unit isn't 0, you can't generate the packing slip.</span></span> <span data-ttu-id="c2599-113">Þetta vandamál gæti til dæmis komið upp ef sölueining og birgðaeining fyrir vöruna eru frábrugðnar og umreikningur milli eininga er ekki nákvæmur.</span><span class="sxs-lookup"><span data-stu-id="c2599-113">For example, this issue might occur if the sales unit and inventory unit for the item differ, and the conversion between units isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="c2599-114">Lausn</span><span class="sxs-lookup"><span data-stu-id="c2599-114">Resolution</span></span>

<span data-ttu-id="c2599-115">Hleðslan eða sendingin er sem stendur í stöðu þar sem myndun fylgiseðils mistekst.</span><span class="sxs-lookup"><span data-stu-id="c2599-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="c2599-116">Til að leysa þetta vandamál þarf að ljúka við eitt af eftirfarandi verkum:</span><span class="sxs-lookup"><span data-stu-id="c2599-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="c2599-117">Farið yfir hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi.</span><span class="sxs-lookup"><span data-stu-id="c2599-117">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="c2599-118">Farið yfir hleðslulínurnar og gerið leiðréttingar til að tryggja að hægt sé að umreikna magnið á hreinlegan hátt án vandamála með sléttun.</span><span class="sxs-lookup"><span data-stu-id="c2599-118">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>
- <span data-ttu-id="c2599-119">Farið yfir hleðslulínurnar og gerið leiðréttingar til að tryggja að einingin og magnið séu í takt við nákvæmni aukastafa í einingunni.</span><span class="sxs-lookup"><span data-stu-id="c2599-119">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>
- <span data-ttu-id="c2599-120">Gangið úr skugga um að mælieining birgða sé minni en mælieining sölu.</span><span class="sxs-lookup"><span data-stu-id="c2599-120">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="c2599-121">Farið yfir hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi</span><span class="sxs-lookup"><span data-stu-id="c2599-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="c2599-122">Notið eftirfarandi ferli til að yfirfara hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi.</span><span class="sxs-lookup"><span data-stu-id="c2599-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="c2599-123">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="c2599-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="c2599-124">Veljið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.</span><span class="sxs-lookup"><span data-stu-id="c2599-124">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="c2599-125">Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu.</span><span class="sxs-lookup"><span data-stu-id="c2599-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="c2599-126">Gera skal athugasemd um gildið í reitnum **Magn stofnaðs verks**.</span><span class="sxs-lookup"><span data-stu-id="c2599-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="c2599-127">Á aðgerðasvæðinu, í flipanum **Hleðslur**, í flokknum **Tengdar upplýsingar**, skal velja **Verk**.</span><span class="sxs-lookup"><span data-stu-id="c2599-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="c2599-128">Staðfestið að verkinu sé lokið á lokastaðsetningu sendingar og að tínt magn verksins stemmi við magn stofnaðs verks í hleðslulínunni.</span><span class="sxs-lookup"><span data-stu-id="c2599-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="c2599-129">Þetta ferli er endurtekið fyrir allar hleðslulínur til að ganga úr skugga um að öll viðmið séu uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="c2599-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a><span data-ttu-id="c2599-130">Farið yfir hleðslulínurnar og gerið leiðréttingar til að tryggja að hægt sé að umreikna magnið á hreinlegan hátt án vandamála með sléttun</span><span class="sxs-lookup"><span data-stu-id="c2599-130">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues</span></span>

<span data-ttu-id="c2599-131">Notið eftirfarandi aðferð til að fara yfir hleðslulínurnar og gera leiðréttingar til að tryggja að hægt sé að umreikna magnið á hreinlegan hátt án vandamála með sléttun</span><span class="sxs-lookup"><span data-stu-id="c2599-131">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>

1. <span data-ttu-id="c2599-132">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="c2599-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="c2599-133">Veljið hleðsluna sem ekki er hægt að mynda fylgiseðilinn fyrir.</span><span class="sxs-lookup"><span data-stu-id="c2599-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="c2599-134">Á aðgerðasvæðinu, í flipanum  **Senda og móttaka**, í flokknum  **Bakfæra**, skal velja  **Bakfæra staðfestingu sendingar**.</span><span class="sxs-lookup"><span data-stu-id="c2599-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="c2599-135">Í flipanum  **Hleðslulínur** skal velja hleðslulínu fyrir vöruna sem fer umfram ofafhendingu.</span><span class="sxs-lookup"><span data-stu-id="c2599-135">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery.</span></span>
1. <span data-ttu-id="c2599-136">Veljið **Minnka tiltektarmagn** til að laga tiltektarmagnið.</span><span class="sxs-lookup"><span data-stu-id="c2599-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="c2599-137">Í flipanum  **Línuupplýsingar** skal velja **Pöntun**.</span><span class="sxs-lookup"><span data-stu-id="c2599-137">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="c2599-138">Stillið reitinn **Magn** á tiltektarmagnið (þ.e. gildið í reitnum **Magn stofnaðs verks**) svo hægt sé að halda áfram með myndun fylgiseðils.</span><span class="sxs-lookup"><span data-stu-id="c2599-138">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="c2599-139">Farið yfir hleðslulínurnar og gerið leiðréttingar til að tryggja að einingin og magnið séu í takt við nákvæmni aukastafa í einingunni</span><span class="sxs-lookup"><span data-stu-id="c2599-139">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="c2599-140">Notið eftirfarandi aðferðir til að fara yfir hleðslulínurnar og gera leiðréttingar til að tryggja að einingin og magnið séu í takt við nákvæmni aukastafa í einingunni.</span><span class="sxs-lookup"><span data-stu-id="c2599-140">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="c2599-141">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="c2599-141">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="c2599-142">Veljið hleðsluna sem ekki er hægt að mynda fylgiseðilinn fyrir.</span><span class="sxs-lookup"><span data-stu-id="c2599-142">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="c2599-143">Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu fyrir vöruna þar sem vandamál kemur upp.</span><span class="sxs-lookup"><span data-stu-id="c2599-143">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="c2599-144">Gera skal athugasemd um gildið í reitunum **Magn** og **Eining**.</span><span class="sxs-lookup"><span data-stu-id="c2599-144">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="c2599-145">Farið í **Fyrirtækisstjórnun \> Einingar \> Einingar**.</span><span class="sxs-lookup"><span data-stu-id="c2599-145">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="c2599-146">Veljið eininguna sem ekki er hægt að búa til fylgiseðil fyrir.</span><span class="sxs-lookup"><span data-stu-id="c2599-146">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="c2599-147">Stillið gildið í reitnum **Nákvæmni aukastafa** eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="c2599-147">Adjust the value of the **Decimal precision** field as required.</span></span>

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a><span data-ttu-id="c2599-148">Gangið úr skugga um að mælieining birgða sé minni en mælieining sölu</span><span class="sxs-lookup"><span data-stu-id="c2599-148">Make sure that the inventory unit of measure is smaller than the sales unit of measure</span></span>

<span data-ttu-id="c2599-149">Gangið úr skugga um að mælieining birgða sé minni en mælieining sölu.</span><span class="sxs-lookup"><span data-stu-id="c2599-149">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span> <span data-ttu-id="c2599-150">Íhugið að endurstilla mælieininguna fyrir vöruna eins og þarf.</span><span class="sxs-lookup"><span data-stu-id="c2599-150">Consider reconfiguring the unit of measure for the item as required.</span></span>
