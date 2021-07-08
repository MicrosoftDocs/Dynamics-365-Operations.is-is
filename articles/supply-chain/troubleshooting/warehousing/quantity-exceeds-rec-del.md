---
title: Magnið sem reynt er að uppfæra er meira en móttekið/afhent magn.
description: Þegar fylgiseðill er búinn til inniheldur hleðsla á útleið magn sem fer umfram vinnumagnið sem var tínt og tekið frá fyrir sölupöntunina.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249121"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a><span data-ttu-id="28ec2-103">Magnið sem reynt er að uppfæra er meira en móttekið/afhent magn</span><span class="sxs-lookup"><span data-stu-id="28ec2-103">Quantity that you're trying to update exceeds the received/delivered quantity</span></span>

<span data-ttu-id="28ec2-104">Villukóði SYS7676</span><span class="sxs-lookup"><span data-stu-id="28ec2-104">Error code: SYS7676</span></span>

## <a name="symptoms"></a><span data-ttu-id="28ec2-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="28ec2-105">Symptoms</span></span>

<span data-ttu-id="28ec2-106">Þegar fylgiseðill er búinn til inniheldur hleðsla á útleið magn sem fer umfram vinnumagnið sem var tínt og tekið frá fyrir sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="28ec2-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the work quantity that was picked and reserved for the sales order.</span></span>

<span data-ttu-id="28ec2-107">Þegar reynt er að búa til fylgiseðil sýnir kerfið eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="28ec2-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="28ec2-108">Magnið sem reynt var að uppfæra er meira en móttekið/afhent magn.</span><span class="sxs-lookup"><span data-stu-id="28ec2-108">The quantity that you are trying to update exceeds the quantity received/delivered.</span></span>

<span data-ttu-id="28ec2-109">Því er ekki hægt að búa til fylgiseðil fyrir hleðsluna.</span><span class="sxs-lookup"><span data-stu-id="28ec2-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="28ec2-110">Orsök</span><span class="sxs-lookup"><span data-stu-id="28ec2-110">Cause</span></span>

<span data-ttu-id="28ec2-111">Tiltekið vinnumagn passar ekki við vinnumagn sem var búið til á farmlínunni.</span><span class="sxs-lookup"><span data-stu-id="28ec2-111">The picked work quantity doesn't match the created work quantity on the load line.</span></span> <span data-ttu-id="28ec2-112">Þetta vandamál gæti til dæmis komið upp ef magn hleðslulínu, magn vinnu sem er búin til eða tiltektarmagn er ekki nákvæmt.</span><span class="sxs-lookup"><span data-stu-id="28ec2-112">For example, this issue might occur if the load line quantity, work created quantity, or picked quantity isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="28ec2-113">Lausn</span><span class="sxs-lookup"><span data-stu-id="28ec2-113">Resolution</span></span>

<span data-ttu-id="28ec2-114">Hleðslan eða sendingin er sem stendur í stöðu þar sem myndun fylgiseðils mistekst.</span><span class="sxs-lookup"><span data-stu-id="28ec2-114">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="28ec2-115">Til að leysa þetta vandamál þarf að ljúka við eitt af eftirfarandi verkum:</span><span class="sxs-lookup"><span data-stu-id="28ec2-115">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="28ec2-116">Farið yfir hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi.</span><span class="sxs-lookup"><span data-stu-id="28ec2-116">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="28ec2-117">Stillið magn hleðslulínunnar.</span><span class="sxs-lookup"><span data-stu-id="28ec2-117">Adjust the load line quantity.</span></span>
- <span data-ttu-id="28ec2-118">Bakfærið allar tiltektarskráningar og endurtakið tiltekt.</span><span class="sxs-lookup"><span data-stu-id="28ec2-118">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="28ec2-119">Farið yfir hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi</span><span class="sxs-lookup"><span data-stu-id="28ec2-119">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="28ec2-120">Notið eftirfarandi ferli til að yfirfara hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi.</span><span class="sxs-lookup"><span data-stu-id="28ec2-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="28ec2-121">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="28ec2-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="28ec2-122">Veljið hleðsluna sem ekki er hægt að mynda sendinguna fyrir.</span><span class="sxs-lookup"><span data-stu-id="28ec2-122">Select the load that the shipment can't be generated for.</span></span>
1. <span data-ttu-id="28ec2-123">Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu.</span><span class="sxs-lookup"><span data-stu-id="28ec2-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="28ec2-124">Gera skal athugasemd um gildið í reitnum **Magn stofnaðs verks**.</span><span class="sxs-lookup"><span data-stu-id="28ec2-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="28ec2-125">Á aðgerðasvæðinu, í flipanum **Hleðslur**, í flokknum **Tengdar upplýsingar**, skal velja **Verk**.</span><span class="sxs-lookup"><span data-stu-id="28ec2-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="28ec2-126">Staðfestið að verkinu sé lokið á lokastaðsetningu sendingar og að tínt magn verksins stemmi við magn stofnaðs verks í hleðslulínunni.</span><span class="sxs-lookup"><span data-stu-id="28ec2-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="28ec2-127">Þetta ferli er endurtekið fyrir allar hleðslulínur til að ganga úr skugga um að öll viðmið séu uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="28ec2-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="28ec2-128">Stilla magn hleðslulínunnar</span><span class="sxs-lookup"><span data-stu-id="28ec2-128">Adjust the load line quantity</span></span>

<span data-ttu-id="28ec2-129">Notið eftirfarandi ferli til að stilla magn farmlínu.</span><span class="sxs-lookup"><span data-stu-id="28ec2-129">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="28ec2-130">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="28ec2-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="28ec2-131">Veljið hleðsluna sem ekki er hægt að mynda fylgiseðilinn fyrir.</span><span class="sxs-lookup"><span data-stu-id="28ec2-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="28ec2-132">Á aðgerðasvæðinu, í flipanum  **Senda og móttaka**, í flokknum  **Bakfæra**, skal velja  **Bakfæra staðfestingu sendingar**.</span><span class="sxs-lookup"><span data-stu-id="28ec2-132">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="28ec2-133">Í flipanum  **Hleðslulínur** skal velja hleðslulínu fyrir vöruna þar sem vandamál kemur upp.</span><span class="sxs-lookup"><span data-stu-id="28ec2-133">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="28ec2-134">Veljið **Minnka tiltektarmagn** til að laga tiltektarmagnið.</span><span class="sxs-lookup"><span data-stu-id="28ec2-134">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="28ec2-135">Stillið reitinn **Minnka hleðslulínu** til að endurspegla leiðréttingar á hleðslulínunni.</span><span class="sxs-lookup"><span data-stu-id="28ec2-135">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="28ec2-136">Bakfæra allar tiltektarskráningar og endurtaka tiltekt</span><span class="sxs-lookup"><span data-stu-id="28ec2-136">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="28ec2-137">Ef einhver notaði tiltektarskráningu til að loka hleðslulínu án vinnu getur misræmi komið upp milli magns hleðslulínunnar og tiltektarmagnsins.</span><span class="sxs-lookup"><span data-stu-id="28ec2-137">If someone used pick registration to close a load line without work, a discrepancy can occur between the load line quantity and the picked quantity.</span></span> <span data-ttu-id="28ec2-138">Í þessu tilviki þarf að bakfæra handvirka skráningu tiltektar og síðan þarf að ljúka tiltekt með farsímaforriti Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="28ec2-138">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="28ec2-139">Notið eftirfarandi ferli til að bakfæra skráningu tiltektar.</span><span class="sxs-lookup"><span data-stu-id="28ec2-139">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="28ec2-140">Farið í **Viðskiptakröfur \> Pantanir \> Allar pantanir**.</span><span class="sxs-lookup"><span data-stu-id="28ec2-140">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="28ec2-141">Veljið sölupöntunina þar sem ekki er hægt að bóka fylgiseðil fyrir hleðsluna.</span><span class="sxs-lookup"><span data-stu-id="28ec2-141">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="28ec2-142">Í flipanum  **Sölupöntunarlínur** skal velja sölupöntunarlínuna sem skráning tiltektar var gerð fyrir.</span><span class="sxs-lookup"><span data-stu-id="28ec2-142">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="28ec2-143">Veljið **Uppfæra línu \> Tiltekt** til að afturkalla tiltekt á vörunum.</span><span class="sxs-lookup"><span data-stu-id="28ec2-143">Select **Update line \> Pick** to unpick the items.</span></span>
