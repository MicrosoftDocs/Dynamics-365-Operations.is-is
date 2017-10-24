---
title: "Útleiðarferli"
description: "Þetta efnisatriði veitir yfirsýn yfir útleiðarferli í birgðastjórnun."
author: perlynne
manager: AnnBe
ms.date: 10/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: HT
ms.sourcegitcommit: 9c09a7bd314bb9005eb0b6c69d7cccad1c30cfdb
ms.openlocfilehash: 7b395cab2184f8f9f3f50a7a595c6ed782645323
ms.contentlocale: is-is
ms.lasthandoff: 10/04/2017

---

# <a name="outbound-process"></a><span data-ttu-id="d8652-103">Útleiðarferli</span><span class="sxs-lookup"><span data-stu-id="d8652-103">Outbound process</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d8652-104">Þetta efnisatriði veitir yfirsýn yfir útleiðarferli í birgðastjórnun.</span><span class="sxs-lookup"><span data-stu-id="d8652-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="d8652-105">Úttakspantanir</span><span class="sxs-lookup"><span data-stu-id="d8652-105">Output orders</span></span>

<span data-ttu-id="d8652-106">Úttakspantanir eru notaðir til að tengja sölulínur og flytja pöntunarlínur með útleiðarferli sem notast við tiltektarlista.</span><span class="sxs-lookup"><span data-stu-id="d8652-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="d8652-107">Þegar tiltektarlistar eru myndaðar úr annaðhvort sölupöntun eða flutningsfyrirmæli eru úttakspantanir og sendingar sjálfkrafa búnar til.</span><span class="sxs-lookup"><span data-stu-id="d8652-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="d8652-108">Tiltektarlisti er í einkvæmum tengslum við sendingu.</span><span class="sxs-lookup"><span data-stu-id="d8652-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="d8652-109">Millifærslupöntun er hægt að búa til þaðan sem millifært er frá eða þaðan sem millifært er til.</span><span class="sxs-lookup"><span data-stu-id="d8652-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="d8652-110">Eftirfarandi skýringarmynd sýnir yfirlit yfir útleiðarferli pantana:</span><span class="sxs-lookup"><span data-stu-id="d8652-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="d8652-111">[![Yfirlit yfir útleiðarferli pantana](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="d8652-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="d8652-112">Hægt er að setja upp útleiðarreglur til að ákvarða hvernig forritið á að vinna útleiðarferlið.</span><span class="sxs-lookup"><span data-stu-id="d8652-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="d8652-113">Þessar reglur má nota til að stýra sendingarferlinu.</span><span class="sxs-lookup"><span data-stu-id="d8652-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="d8652-114">Sérstaklega er hægt að nota reglurnar til að stjórna á hvaða stigi er hægt að senda sendingu á meðan ferli stendur yfir.</span><span class="sxs-lookup"><span data-stu-id="d8652-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="d8652-115">Eftirfarandi stillingar skilgreina hvernig útleiðarferli er stjórnað.</span><span class="sxs-lookup"><span data-stu-id="d8652-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="d8652-116">Staða tiltektarleiðar fyrir sölu- og flutningspantanir</span><span class="sxs-lookup"><span data-stu-id="d8652-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="d8652-117">Farðu í **Viðskiptakröfur** \> **Uppsetning** \> **Færibreytur viðskiptakrafna** og veldu svo, í flipanum  **Uppfærslur** gildi í svæðinu **Staða tiltektarleiðar** .</span><span class="sxs-lookup"><span data-stu-id="d8652-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="d8652-118">[![Staða tiltektarleiðar fyrir sölupantanir](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="d8652-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="d8652-119">Ef stillingarreiturinn **Staða tiltektarleiðar**er stillt á **Lokið** fer tiltektarferlið sjálfkrafa af stað sem sem hluti af því að búa til tiltektarlista.</span><span class="sxs-lookup"><span data-stu-id="d8652-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="d8652-120">Ef reitur er stilltur á **Kveikt**, þarf að uppfæra tiltektarlistalínurnar handvirkt.</span><span class="sxs-lookup"><span data-stu-id="d8652-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="d8652-121">Sama á við um flutningspantanir.</span><span class="sxs-lookup"><span data-stu-id="d8652-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="d8652-122">Farðu í **Birgðastjórnun** \> **Uppsetning** \> **Færibreytur birgða- og vöruhúsakerfis** og veldu svo, í flipanum  **Flutningur** gildi í svæðinu **Staða tiltektarleiðar** .</span><span class="sxs-lookup"><span data-stu-id="d8652-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="d8652-123">[![Staða tiltektarleiðar fyrir flutningspantanir](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="d8652-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="d8652-124">Ljúka birgðapöntun</span><span class="sxs-lookup"><span data-stu-id="d8652-124">End output inventory orders</span></span>

<span data-ttu-id="d8652-125">Farðu í **Birgðastjórnun** \> **Uppsetning** \> **Færibreytur birgða- og vöruhúsakerfis** og veldu svo, í flipanum  **Almennt**, valkostinn **Ljúka úttaksbirgðapöntun** .</span><span class="sxs-lookup"><span data-stu-id="d8652-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="d8652-126">[![Ljúka úttaksbirgðapöntun](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="d8652-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="d8652-127">Stundum er ekki hægt að tína öll atriði í birgðum sem hluta af tiltektarlista.</span><span class="sxs-lookup"><span data-stu-id="d8652-127">Sometimes, some items in inventory can't be picked as part of the picking list process.</span></span> <span data-ttu-id="d8652-128">Til dæmis gæti þetta ástand komið fram ef starfsmaður í vöruhúsi dregur úr magni á tiltektarlínur og vinnur svo úr tiltektarlistanum.</span><span class="sxs-lookup"><span data-stu-id="d8652-128">For example, this situation might occur if a warehouse worker reduces the quantities on picking lines and processes the picking list.</span></span> <span data-ttu-id="d8652-129">Ef valkosturinn **Ljúka úttaksbirgðapöntun** er stillt á **Já**, verða eftirstandandi ótiltekið magn tilkynnt aftur á pöntunarstig.</span><span class="sxs-lookup"><span data-stu-id="d8652-129">If the **End output inventory order** option is set to **Yes**, the remaining unpicked quantities are reported back to the order level.</span></span> <span data-ttu-id="d8652-130">Ef valkosturinn er stilltur á  **Nei**, er eftirstandandi ótiltekið magn geym sem opið úttakspöntunarmagn.</span><span class="sxs-lookup"><span data-stu-id="d8652-130">If the option is set to **No**, the remaining unpicked quantities are kept as an open output order quantity.</span></span> <span data-ttu-id="d8652-131">Í því tilviki verður magnið áfram losað í vöruhús og verður að bæta við nýjan tiltektarlista sem hluta af aðgerðinni **Opna úttakspantanir** .</span><span class="sxs-lookup"><span data-stu-id="d8652-131">In this case, the quantities remain released to the warehouse and must be added to a new picking list as part of the **Open output orders** functionality.</span></span>

<span data-ttu-id="d8652-132">Skipunin [![Opna úttakspantanir á valmynd fyrir Aðgerðir](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="d8652-132">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="d8652-133">[![Aðgerðavalmyndin á síðunni Opna ](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="d8652-133">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="d8652-134">Minnka magn</span><span class="sxs-lookup"><span data-stu-id="d8652-134">Reduce quantity</span></span>

<span data-ttu-id="d8652-135">Þriðja færibreytan sem nota má sem hluta af ferlinu við að búa til tiltektarlista er færibreytan **Minnka magn** .</span><span class="sxs-lookup"><span data-stu-id="d8652-135">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="d8652-136">Stillingar þessa færibreytu vinna með stillingunni**Frátekning** sem setur af stað frátekningarferli sem er hluti af losun til vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="d8652-136">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="d8652-137">[![Færibreytan Minnka magn](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="d8652-137">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="d8652-138">Dæmi um útleiðarferli fyrir  sölupöntun</span><span class="sxs-lookup"><span data-stu-id="d8652-138">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="d8652-139">Í þessu dæmi er sölupöntun með tveimur vörum.</span><span class="sxs-lookup"><span data-stu-id="d8652-139">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="d8652-140">Við myndun tiltektarlista er valin færibreytan **Minnka magn** .</span><span class="sxs-lookup"><span data-stu-id="d8652-140">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="d8652-141">Þess vegna losar þú og stofnar aðeins tiltektarlínur fyrir tiltækar birgðir.</span><span class="sxs-lookup"><span data-stu-id="d8652-141">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="d8652-142">Tilkynna verður tiltekt með skráningarferli fyrir tiltektarlista (**Staða tiltektarleiðar** = **Virkt**).</span><span class="sxs-lookup"><span data-stu-id="d8652-142">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="d8652-143">Birgðir sem ekki hafa verið fráteknar verða fráteknar við myndun tiltektarlista.</span><span class="sxs-lookup"><span data-stu-id="d8652-143">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="d8652-144">Ótiltækar birgðir er hægt að fjarlægja annaðhvort úr sölustað eða út í vöruhús til útleiðarferlis síðar, þegar birgðir eru tiltækar til að tína.</span><span class="sxs-lookup"><span data-stu-id="d8652-144">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="d8652-145">[![Uppfæra tiltektarlistann](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="d8652-145">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="d8652-146">Um leið og allar tiltektarlínur hafa verið teknar til á síðunni **Skráning tiltektarlista** er tengdri afhendingu lokið.</span><span class="sxs-lookup"><span data-stu-id="d8652-146">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="d8652-147">Hægt er að hefja ferli fyrir fylgiseðla sölupantana með hliðsjón af völdum birgðum.</span><span class="sxs-lookup"><span data-stu-id="d8652-147">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="d8652-148">[![Uppfæra sendingar á útleið](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="d8652-148">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>

