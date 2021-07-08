---
title: Magn fer yfir undirafhendingarprósentu við myndun fylgiseðils
description: Þegar fylgiseðill er búinn til inniheldur hleðsla á útleið magn sem fer umfram prósentu undirafhendingar.
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
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249116"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="8e6b5-103">Magn fer yfir undirafhendingarprósentu við myndun fylgiseðils</span><span class="sxs-lookup"><span data-stu-id="8e6b5-103">Quantity exceeds under-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="8e6b5-104">Villukóði SYS24921</span><span class="sxs-lookup"><span data-stu-id="8e6b5-104">Error code: SYS24921</span></span>

## <a name="symptoms"></a><span data-ttu-id="8e6b5-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="8e6b5-105">Symptoms</span></span>

<span data-ttu-id="8e6b5-106">Þegar fylgiseðill er búinn til inniheldur hleðsla á útleið magn sem fer umfram prósentu undirafhendingar.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the under-delivery percentage.</span></span>

<span data-ttu-id="8e6b5-107">Þegar reynt er að búa til fylgiseðil sýnir kerfið eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="8e6b5-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="8e6b5-108">Vanafhending línu er %1 prósent, en leyfileg vanafhending er aðeins %2 prósent.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-108">Underdelivery of line is %1 percent, but the allowed underdelivery is only %2 percent.</span></span>

<span data-ttu-id="8e6b5-109">Því er ekki hægt að búa til fylgiseðil fyrir hleðsluna.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="8e6b5-110">Orsök</span><span class="sxs-lookup"><span data-stu-id="8e6b5-110">Cause</span></span>

<span data-ttu-id="8e6b5-111">Tiltektarmagn fyrir hleðsluna eða sendinguna er minna en pantað magn og er ekki innan marka fyrir prósentu vanafhendingar.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-111">The picked quantity for the load or shipment is less than the ordered quantity and isn't within the range of the under-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="8e6b5-112">Lausn</span><span class="sxs-lookup"><span data-stu-id="8e6b5-112">Resolution</span></span>

<span data-ttu-id="8e6b5-113">Hleðslan eða sendingin er sem stendur í stöðu þar sem myndun fylgiseðils mistekst.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="8e6b5-114">Til að leysa þetta vandamál þarf að ljúka við eitt af eftirfarandi verkum:</span><span class="sxs-lookup"><span data-stu-id="8e6b5-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="8e6b5-115">Stillið prósentu vanafhendingar.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-115">Adjust the under-delivery percentage.</span></span>
- <span data-ttu-id="8e6b5-116">Bakfærið og gerið leiðréttingar.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-116">Reverse and make adjustments.</span></span>

### <a name="adjust-the-under-delivery-percentage"></a><span data-ttu-id="8e6b5-117">Stilla prósentu vanafhendingar</span><span class="sxs-lookup"><span data-stu-id="8e6b5-117">Adjust the under-delivery percentage</span></span>

<span data-ttu-id="8e6b5-118">Notaðu eftirfarandi ferli til að stilla prósentu vanafhendingar.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-118">Use the following procedure to adjust the under-delivery percentage.</span></span>

1. <span data-ttu-id="8e6b5-119">Farið í **Viðskiptakröfur \> Pantanir \> Allar pantanir**.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-119">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="8e6b5-120">Veljið sölupöntunina þar sem ekki er hægt að bóka fylgiseðil fyrir hleðsluna.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-120">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="8e6b5-121">Í flipanum  **Sölupöntunarlínur** skal velja sölupöntunarlínuna fyrir vöruna sem fer umfram prósentu vanafhendingar.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-121">On the **Sales order lines** tab, select the sales order line for the item that exceeds the under-delivery percentage.</span></span>
1. <span data-ttu-id="8e6b5-122">Í flipanum  **Línuupplýsingar** skal velja **Afhending**.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-122">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="8e6b5-123">Stillið gildið í reitnum **Vanafhending** á hærri prósentu sem nær utan um magnið sem var tínt gagnvart hleðslumagninu, þannig að myndun fylgiseðils geti átt sér stað.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-123">Set the **Underdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="8e6b5-124">Bakfæra og gera leiðréttingar</span><span class="sxs-lookup"><span data-stu-id="8e6b5-124">Reverse and make adjustments</span></span>

<span data-ttu-id="8e6b5-125">Bakfærið allt sem hefur verið bókað fyrir hleðsluna (til dæmis fylgiseðilinn, staðfestingu sendingar og vinnu), gerið leiðréttingar á sölupöntun, losið pöntunina aftur í vöruhúsið og ljúkið sendingarferlinu.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-125">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="8e6b5-126">Notið eftirfarandi ferli til að hætta við fylgiseðil.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-126">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="8e6b5-127">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-127">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="8e6b5-128">Á aðgerðasvæðinu, í flipanum  **Senda og móttaka**, í flokknum  **Bakfæra**, skal velja  **Hætta við fylgiseðla**.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-128">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="8e6b5-129">Notið eftirfarandi ferli til að afturkalla staðfestingu sendingar.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-129">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="8e6b5-130">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="8e6b5-131">Á aðgerðasvæðinu, í flipanum  **Senda og móttaka**, í flokknum  **Bakfæra**, skal velja  **Bakfæra staðfestingu sendingar**.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-131">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="8e6b5-132">Notið eftirfarandi ferli til að bakfæra vinnu.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-132">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="8e6b5-133">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-133">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="8e6b5-134">Á aðgerðasvæðinu, í flipanum  **Hleðslur**, í flokknum  **Vinna**, skal velja  **Bakfæra vinnu**.</span><span class="sxs-lookup"><span data-stu-id="8e6b5-134">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
