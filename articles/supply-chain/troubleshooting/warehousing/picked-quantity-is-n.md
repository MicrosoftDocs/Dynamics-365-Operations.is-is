---
title: Ekki er nægjanlegt tiltektarmagn við myndun fylgiseðils
description: Þegar fylgiseðill er búinn til inniheldur hleðslan á útleið tiltektarmagn sem passar ekki við stofnað vinnumagn í hleðslulínunni.
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
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249120"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a><span data-ttu-id="72a76-103">Ekki er nægjanlegt tiltektarmagn við myndun fylgiseðils</span><span class="sxs-lookup"><span data-stu-id="72a76-103">Picked quantity isn't sufficient during packing slip generation</span></span>

<span data-ttu-id="72a76-104">Villukóði SYS54073</span><span class="sxs-lookup"><span data-stu-id="72a76-104">Error code: SYS54073</span></span>

## <a name="symptoms"></a><span data-ttu-id="72a76-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="72a76-105">Symptoms</span></span>

<span data-ttu-id="72a76-106">Þegar fylgiseðill er búinn til inniheldur hleðslan á útleið tiltektarmagn sem passar ekki við stofnað vinnumagn í hleðslulínunni.</span><span class="sxs-lookup"><span data-stu-id="72a76-106">When you generate a packing slip, the outbound load contains a picked quantity that doesn't match the created work quantity on the load line.</span></span>

<span data-ttu-id="72a76-107">Þegar reynt er að búa til fylgiseðil sýnir kerfið eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="72a76-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="72a76-108">Þar sem %1 hefur verið tekið til, er ekki nóg af því til að uppfæra %2, þegar afgangurinn þarf að vera %3.</span><span class="sxs-lookup"><span data-stu-id="72a76-108">As %1 have been picked, it is not sufficient to update %2, when, subsequently, the remainder must be %3.</span></span>

<span data-ttu-id="72a76-109">Því er ekki hægt að búa til fylgiseðil fyrir hleðsluna.</span><span class="sxs-lookup"><span data-stu-id="72a76-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="72a76-110">Orsök</span><span class="sxs-lookup"><span data-stu-id="72a76-110">Cause</span></span>

<span data-ttu-id="72a76-111">Ekki er hægt að búa til fylgiseðilinn í núgildandi stöðu vegna þess að eitt af eftirfarandi skilyrðum gæti verið til:</span><span class="sxs-lookup"><span data-stu-id="72a76-111">The packing slip can't be generated in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="72a76-112">Tengt verk hefur ekki enn verið tínt og fært yfir á lokastaðsetningu sendingar.</span><span class="sxs-lookup"><span data-stu-id="72a76-112">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="72a76-113">Tiltekið vinnumagn passar ekki við vinnumagn sem var búið til á farmlínunni.</span><span class="sxs-lookup"><span data-stu-id="72a76-113">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="72a76-114">Magn hleðslulínu, stofnað vinnslumagn og tiltektarmagn passa ekki sama.</span><span class="sxs-lookup"><span data-stu-id="72a76-114">The load line quantity, work created quantity, and picked quantity don't match.</span></span>

## <a name="resolution"></a><span data-ttu-id="72a76-115">Lausn</span><span class="sxs-lookup"><span data-stu-id="72a76-115">Resolution</span></span>

<span data-ttu-id="72a76-116">Hleðslan eða sendingin er sem stendur í stöðu þar sem myndun fylgiseðils mistekst.</span><span class="sxs-lookup"><span data-stu-id="72a76-116">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="72a76-117">Til að leysa þetta vandamál þarf að ljúka við eitt af eftirfarandi verkum:</span><span class="sxs-lookup"><span data-stu-id="72a76-117">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="72a76-118">Farið yfir hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi.</span><span class="sxs-lookup"><span data-stu-id="72a76-118">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="72a76-119">Stillið magn hleðslulínunnar.</span><span class="sxs-lookup"><span data-stu-id="72a76-119">Adjust the load line quantity.</span></span>
- <span data-ttu-id="72a76-120">Bakfærið allar tiltektarskráningar og endurtakið tiltekt.</span><span class="sxs-lookup"><span data-stu-id="72a76-120">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="72a76-121">Farið yfir hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi</span><span class="sxs-lookup"><span data-stu-id="72a76-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="72a76-122">Notið eftirfarandi ferli til að yfirfara hleðslulínurnar og gangið úr skugga um að tengdu verki hafi verið lokið á lokastaðsetningu sendingar og að magnið stemmi.</span><span class="sxs-lookup"><span data-stu-id="72a76-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="72a76-123">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="72a76-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="72a76-124">Veljið hleðsluna sem ekki er hægt að mynda fylgiseðilinn fyrir.</span><span class="sxs-lookup"><span data-stu-id="72a76-124">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="72a76-125">Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu.</span><span class="sxs-lookup"><span data-stu-id="72a76-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="72a76-126">Gera skal athugasemd um gildið í reitnum **Magn stofnaðs verks**.</span><span class="sxs-lookup"><span data-stu-id="72a76-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="72a76-127">Á aðgerðasvæðinu, í flipanum **Hleðslur**, í flokknum **Tengdar upplýsingar**, skal velja **Verk**.</span><span class="sxs-lookup"><span data-stu-id="72a76-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="72a76-128">Staðfestið að verkinu sé lokið á lokastaðsetningu sendingar og að tínt magn verksins stemmi við magn stofnaðs verks í hleðslulínunni.</span><span class="sxs-lookup"><span data-stu-id="72a76-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="72a76-129">Þetta ferli er endurtekið fyrir allar hleðslulínur til að ganga úr skugga um að öll viðmið séu uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="72a76-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="72a76-130">Stilla magn hleðslulínunnar</span><span class="sxs-lookup"><span data-stu-id="72a76-130">Adjust the load line quantity</span></span>

<span data-ttu-id="72a76-131">Notið eftirfarandi ferli til að stilla magn farmlínu.</span><span class="sxs-lookup"><span data-stu-id="72a76-131">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="72a76-132">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="72a76-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="72a76-133">Veljið hleðsluna sem ekki er hægt að mynda fylgiseðilinn fyrir.</span><span class="sxs-lookup"><span data-stu-id="72a76-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="72a76-134">Á aðgerðasvæðinu, í flipanum  **Senda og móttaka**, í flokknum  **Bakfæra**, skal velja  **Bakfæra staðfestingu sendingar**.</span><span class="sxs-lookup"><span data-stu-id="72a76-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="72a76-135">Í flipanum  **Hleðslulínur** skal velja hleðslulínu fyrir vöruna þar sem vandamál kemur upp.</span><span class="sxs-lookup"><span data-stu-id="72a76-135">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="72a76-136">Veljið **Minnka tiltektarmagn** til að laga tiltektarmagnið.</span><span class="sxs-lookup"><span data-stu-id="72a76-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="72a76-137">Stillið reitinn **Minnka hleðslulínu** til að endurspegla leiðréttingar á hleðslulínunni.</span><span class="sxs-lookup"><span data-stu-id="72a76-137">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="72a76-138">Bakfæra allar tiltektarskráningar og endurtaka tiltekt</span><span class="sxs-lookup"><span data-stu-id="72a76-138">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="72a76-139">Vandamálið gæti komið upp vegna þess að einhver notaði skráningu tiltektar til að loka hleðslulínu án vinnu.</span><span class="sxs-lookup"><span data-stu-id="72a76-139">The issue might occur because someone used pick registration to close a load line without work.</span></span> <span data-ttu-id="72a76-140">Í þessu tilviki þarf að bakfæra handvirka skráningu tiltektar og síðan þarf að ljúka tiltekt með farsímaforriti Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="72a76-140">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="72a76-141">Notið eftirfarandi ferli til að bakfæra skráningu tiltektar.</span><span class="sxs-lookup"><span data-stu-id="72a76-141">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="72a76-142">Farið í **Viðskiptakröfur \> Pantanir \> Allar pantanir**.</span><span class="sxs-lookup"><span data-stu-id="72a76-142">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="72a76-143">Veljið sölupöntunina þar sem ekki er hægt að bóka fylgiseðil fyrir hleðsluna.</span><span class="sxs-lookup"><span data-stu-id="72a76-143">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="72a76-144">Í flipanum  **Sölupöntunarlínur** skal velja sölupöntunarlínuna sem skráning tiltektar var gerð fyrir.</span><span class="sxs-lookup"><span data-stu-id="72a76-144">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="72a76-145">Veljið **Uppfæra línu \> Tiltekt** til að afturkalla tiltekt á vörunum.</span><span class="sxs-lookup"><span data-stu-id="72a76-145">Select **Update line \> Pick** to unpick the items.</span></span>
