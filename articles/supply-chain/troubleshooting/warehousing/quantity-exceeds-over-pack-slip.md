---
title: Magn fer yfir umframafhendingarprósentu við myndun fylgiseðils
description: Þegar fylgiseðill er búinn til inniheldur hleðsla á útleið magn sem fer umfram prósentu ofafhendingar.
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
ms.openlocfilehash: 1106322cc3772c1b671b7fa82fb74039c028ba35
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249118"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="339a1-103">Magn fer yfir umframafhendingarprósentu við myndun fylgiseðils</span><span class="sxs-lookup"><span data-stu-id="339a1-103">Quantity exceeds over-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="339a1-104">Villukóði SYS24920</span><span class="sxs-lookup"><span data-stu-id="339a1-104">Error code: SYS24920</span></span>

## <a name="symptoms"></a><span data-ttu-id="339a1-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="339a1-105">Symptoms</span></span>

<span data-ttu-id="339a1-106">Þegar fylgiseðill er búinn til inniheldur hleðsla á útleið magn sem fer umfram prósentu ofafhendingar.</span><span class="sxs-lookup"><span data-stu-id="339a1-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the over-delivery percentage.</span></span>

<span data-ttu-id="339a1-107">Þegar reynt er að búa til fylgiseðil sýnir kerfið eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="339a1-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="339a1-108">Ofafhending línu er %1 prósent, en leyfileg ofafhending er aðeins %2 prósent.</span><span class="sxs-lookup"><span data-stu-id="339a1-108">Overdelivery of line is %1 percent, but the allowed overdelivery is only %2 percent.</span></span>

<span data-ttu-id="339a1-109">Því er ekki hægt að búa til fylgiseðil fyrir hleðsluna.</span><span class="sxs-lookup"><span data-stu-id="339a1-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="339a1-110">Orsök</span><span class="sxs-lookup"><span data-stu-id="339a1-110">Cause</span></span>

<span data-ttu-id="339a1-111">Tiltektarmagn fyrir hleðsluna eða sendinguna er meira en pantað magn og er ekki innan marka fyrir prósentu ofafhendingar.</span><span class="sxs-lookup"><span data-stu-id="339a1-111">The picked quantity for the load or shipment is more than the ordered quantity and isn't within the range of the over-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="339a1-112">Lausn</span><span class="sxs-lookup"><span data-stu-id="339a1-112">Resolution</span></span>

<span data-ttu-id="339a1-113">Hleðslan eða sendingin er sem stendur í stöðu þar sem myndun fylgiseðils mistekst.</span><span class="sxs-lookup"><span data-stu-id="339a1-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="339a1-114">Til að leysa þetta vandamál þarf að ljúka við eitt af eftirfarandi verkum:</span><span class="sxs-lookup"><span data-stu-id="339a1-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="339a1-115">Stillið magn hleðslulínunnar.</span><span class="sxs-lookup"><span data-stu-id="339a1-115">Adjust the load line quantity.</span></span>
- <span data-ttu-id="339a1-116">Stilla prósentu ofafhendingar.</span><span class="sxs-lookup"><span data-stu-id="339a1-116">Adjust the over-delivery percentage.</span></span>
- <span data-ttu-id="339a1-117">Bakfærið og gerið leiðréttingar.</span><span class="sxs-lookup"><span data-stu-id="339a1-117">Reverse and make adjustments.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="339a1-118">Stilla magn hleðslulínunnar</span><span class="sxs-lookup"><span data-stu-id="339a1-118">Adjust the load line quantity</span></span>

<span data-ttu-id="339a1-119">Notið eftirfarandi ferli til að stilla magn farmlínu.</span><span class="sxs-lookup"><span data-stu-id="339a1-119">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="339a1-120">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="339a1-120">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="339a1-121">Veljið hleðsluna sem ekki er hægt að mynda fylgiseðilinn fyrir.</span><span class="sxs-lookup"><span data-stu-id="339a1-121">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="339a1-122">Á aðgerðasvæðinu, í flipanum  **Senda og móttaka**, í flokknum  **Bakfæra**, skal velja  **Bakfæra staðfestingu sendingar**.</span><span class="sxs-lookup"><span data-stu-id="339a1-122">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="339a1-123">Í flipanum  **Hleðslulínur** skal velja hleðslulínu fyrir vöruna sem fer umfram prósentu ofafhendingar.</span><span class="sxs-lookup"><span data-stu-id="339a1-123">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="339a1-124">Veljið **Minnka tiltektarmagn** til að laga tiltektarmagnið.</span><span class="sxs-lookup"><span data-stu-id="339a1-124">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="339a1-125">Í flipanum  **Línuupplýsingar** skal velja **Pöntun**.</span><span class="sxs-lookup"><span data-stu-id="339a1-125">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="339a1-126">Stillið reitinn **Magn** á tiltektarmagnið (þ.e. gildið í reitnum **Magn stofnaðs verks**) svo hægt sé að halda áfram með myndun fylgiseðils.</span><span class="sxs-lookup"><span data-stu-id="339a1-126">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="adjust-the-over-delivery-percentage"></a><span data-ttu-id="339a1-127">Stilla prósentu ofafhendingar</span><span class="sxs-lookup"><span data-stu-id="339a1-127">Adjust the over-delivery percentage</span></span>

<span data-ttu-id="339a1-128">Notið eftirfarandi aðgerð til að stilla prósentu ofafhendingar.</span><span class="sxs-lookup"><span data-stu-id="339a1-128">Use the following procedure to adjust the over-delivery percentage.</span></span>

1. <span data-ttu-id="339a1-129">Farið í **Viðskiptakröfur \> Pantanir \> Allar pantanir**.</span><span class="sxs-lookup"><span data-stu-id="339a1-129">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="339a1-130">Veljið sölupöntunina þar sem ekki er hægt að bóka fylgiseðil fyrir hleðsluna.</span><span class="sxs-lookup"><span data-stu-id="339a1-130">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="339a1-131">Í flipanum  **Sölupöntunarlínur** skal velja sölupöntunarlínuna fyrir vöruna sem fer umfram prósentu ofafhendingar.</span><span class="sxs-lookup"><span data-stu-id="339a1-131">On the **Sales order lines** tab, select the sales order line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="339a1-132">Í flipanum  **Línuupplýsingar** skal velja **Afhending**.</span><span class="sxs-lookup"><span data-stu-id="339a1-132">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="339a1-133">Stillið gildið í reitnum **Ofafhending** á hærri prósentu sem nær utan um magnið sem var tínt gagnvart hleðslumagninu, þannig að myndun fylgiseðils geti átt sér stað.</span><span class="sxs-lookup"><span data-stu-id="339a1-133">Set the **Overdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="339a1-134">Bakfæra og gera leiðréttingar</span><span class="sxs-lookup"><span data-stu-id="339a1-134">Reverse and make adjustments</span></span>

<span data-ttu-id="339a1-135">Bakfærið allt sem hefur verið bókað fyrir hleðsluna (til dæmis fylgiseðilinn, staðfestingu sendingar og vinnu), gerið leiðréttingar á sölupöntun, losið pöntunina aftur í vöruhúsið og ljúkið sendingarferlinu.</span><span class="sxs-lookup"><span data-stu-id="339a1-135">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="339a1-136">Notið eftirfarandi ferli til að hætta við fylgiseðil.</span><span class="sxs-lookup"><span data-stu-id="339a1-136">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="339a1-137">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="339a1-137">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="339a1-138">Á aðgerðasvæðinu, í flipanum  **Senda og móttaka**, í flokknum  **Bakfæra**, skal velja  **Hætta við fylgiseðla**.</span><span class="sxs-lookup"><span data-stu-id="339a1-138">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="339a1-139">Notið eftirfarandi ferli til að afturkalla staðfestingu sendingar.</span><span class="sxs-lookup"><span data-stu-id="339a1-139">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="339a1-140">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="339a1-140">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="339a1-141">Á aðgerðasvæðinu, í flipanum  **Senda og móttaka**, í flokknum  **Bakfæra**, skal velja  **Bakfæra staðfestingu sendingar**.</span><span class="sxs-lookup"><span data-stu-id="339a1-141">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="339a1-142">Notið eftirfarandi ferli til að bakfæra vinnu.</span><span class="sxs-lookup"><span data-stu-id="339a1-142">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="339a1-143">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="339a1-143">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="339a1-144">Á aðgerðasvæðinu, í flipanum  **Hleðslur**, í flokknum  **Vinna**, skal velja  **Bakfæra vinnu**.</span><span class="sxs-lookup"><span data-stu-id="339a1-144">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
