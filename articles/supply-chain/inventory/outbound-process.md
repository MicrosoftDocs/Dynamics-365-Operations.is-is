---
title: Yfirlit útleiðarferlis
description: Þetta efnisatriði veitir yfirsýn yfir útleiðarferli í birgðastjórnun.
author: perlynne
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSOrder, WMSShipment, MCRPickingWorkbench, WMSPickingRegistration, CustomFilterGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274363
ms.assetid: 375807b2-a426-4f1b-bc1f-2fe00fd48413
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 27596bf260c069af4a7457c0eb8d02c45e5202b9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000235"
---
# <a name="outbound-process-overview"></a><span data-ttu-id="9aca9-103">Yfirlit útleiðarferlis</span><span class="sxs-lookup"><span data-stu-id="9aca9-103">Outbound process overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9aca9-104">Þetta efnisatriði veitir yfirsýn yfir útleiðarferli í birgðastjórnun.</span><span class="sxs-lookup"><span data-stu-id="9aca9-104">This topic provides an overview of the outbound process in Inventory management.</span></span>

## <a name="output-orders"></a><span data-ttu-id="9aca9-105">Úttakspantanir</span><span class="sxs-lookup"><span data-stu-id="9aca9-105">Output orders</span></span>

<span data-ttu-id="9aca9-106">Úttakspantanir eru notaðir til að tengja sölulínur og flytja pöntunarlínur með útleiðarferli sem notast við tiltektarlista.</span><span class="sxs-lookup"><span data-stu-id="9aca9-106">Output orders are used to link sales order lines and transfer order lines with the outbound picking processes that use picking lists.</span></span>

<span data-ttu-id="9aca9-107">Þegar tiltektarlistar eru myndaðar úr annaðhvort sölupöntun eða flutningsfyrirmæli eru úttakspantanir og sendingar sjálfkrafa búnar til.</span><span class="sxs-lookup"><span data-stu-id="9aca9-107">When picking lists are generated from either sales orders or transfer orders, output orders and shipments are automatically created.</span></span> <span data-ttu-id="9aca9-108">Tiltektarlisti er í einkvæmum tengslum við sendingu.</span><span class="sxs-lookup"><span data-stu-id="9aca9-108">A picking list has a one-to-one relationship with a shipment.</span></span> <span data-ttu-id="9aca9-109">Millifærslupöntun er hægt að búa til þaðan sem millifært er frá eða þaðan sem millifært er til.</span><span class="sxs-lookup"><span data-stu-id="9aca9-109">The transfer order shipment or the sales order packing slip can be processed from the shipment.</span></span> 

<span data-ttu-id="9aca9-110">Eftirfarandi skýringarmynd sýnir yfirlit yfir útleiðarferli pantana:</span><span class="sxs-lookup"><span data-stu-id="9aca9-110">The following diagram shows an overview of the process for outbound orders.</span></span> 

<span data-ttu-id="9aca9-111">[![Yfirlit yfir útleiðarferli pantana](./media/outbound-order.png)](./media/outbound-order.png)</span><span class="sxs-lookup"><span data-stu-id="9aca9-111">[![Overview of the outbound order process](./media/outbound-order.png)](./media/outbound-order.png)</span></span>

<span data-ttu-id="9aca9-112">Hægt er að setja upp útleiðarreglur til að ákvarða hvernig forritið á að vinna útleiðarferlið.</span><span class="sxs-lookup"><span data-stu-id="9aca9-112">You can set up outbound rules to define how the program should handle the outbound process.</span></span> <span data-ttu-id="9aca9-113">Þessar reglur má nota til að stýra sendingarferlinu.</span><span class="sxs-lookup"><span data-stu-id="9aca9-113">You can use these rules to control the shipment process.</span></span> <span data-ttu-id="9aca9-114">Sérstaklega er hægt að nota reglurnar til að stjórna á hvaða stigi er hægt að senda sendingu á meðan ferli stendur yfir.</span><span class="sxs-lookup"><span data-stu-id="9aca9-114">In particular, you can use the rules to control which stage in the process a shipment can be sent during.</span></span> <span data-ttu-id="9aca9-115">Eftirfarandi stillingar skilgreina hvernig útleiðarferli er stjórnað.</span><span class="sxs-lookup"><span data-stu-id="9aca9-115">The following settings define how the outbound processes are handled.</span></span>

## <a name="picking-route-status-for-sales-and-transfer-orders"></a><span data-ttu-id="9aca9-116">Staða tiltektarleiðar fyrir sölu- og flutningspantanir</span><span class="sxs-lookup"><span data-stu-id="9aca9-116">Picking route status for sales and transfer orders</span></span> 

<span data-ttu-id="9aca9-117">Farðu í **Viðskiptakröfur** \> **Uppsetning** \> **Færibreytur viðskiptakrafna** og veldu svo, í flipanum **Uppfærslur** gildi í svæðinu **Staða tiltektarleiðar** .</span><span class="sxs-lookup"><span data-stu-id="9aca9-117">Go to **Account receivable** \> **Setup** \> **Account receivable parameters**, and then, on the **Updates** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="9aca9-118">[![Staða tiltektarleiðar fyrir sölupantanir](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span><span class="sxs-lookup"><span data-stu-id="9aca9-118">[![Picking route status field for sales orders](./media/picking-route-status-sales-order.png)](./media/picking-route-status-sales-order.png)</span></span>

<span data-ttu-id="9aca9-119">Ef stillingarreiturinn **Staða tiltektarleiðar** er stillt á **Lokið** fer tiltektarferlið sjálfkrafa af stað sem sem hluti af því að búa til tiltektarlista.</span><span class="sxs-lookup"><span data-stu-id="9aca9-119">If the **Picking route status** field is set to **Completed**, the picking process occurs automatically as part of the process of generating picking lists.</span></span> <span data-ttu-id="9aca9-120">Ef reitur er stilltur á **Kveikt**, þarf að uppfæra tiltektarlistalínurnar handvirkt.</span><span class="sxs-lookup"><span data-stu-id="9aca9-120">If the field is set to **Activated**, the picking list lines must be manually updated.</span></span>

<span data-ttu-id="9aca9-121">Sama á við um flutningspantanir.</span><span class="sxs-lookup"><span data-stu-id="9aca9-121">The same setup applies to transfer orders.</span></span> <span data-ttu-id="9aca9-122">Farðu í **Birgðastjórnun** \> **Uppsetning** \> **Færibreytur birgða- og vöruhúsakerfis** og veldu svo, í flipanum **Flutningur** gildi í svæðinu **Staða tiltektarleiðar** .</span><span class="sxs-lookup"><span data-stu-id="9aca9-122">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **Transport** tab, select a value in the **Picking route status** field.</span></span>

<span data-ttu-id="9aca9-123">[![Staða tiltektarleiðar fyrir flutningspantanir](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span><span class="sxs-lookup"><span data-stu-id="9aca9-123">[![Picking route status field for transfer orders](./media/picking-route-status-transfer-order.png)](./media/picking-route-status-transfer-order.png)</span></span>

## <a name="end-output-inventory-orders"></a><span data-ttu-id="9aca9-124">Ljúka birgðapöntun</span><span class="sxs-lookup"><span data-stu-id="9aca9-124">End output inventory orders</span></span>

<span data-ttu-id="9aca9-125">Farðu í **Birgðastjórnun** \> **Uppsetning** \> **Færibreytur birgða- og vöruhúsakerfis** og veldu svo, í flipanum **Almennt**, valkostinn **Ljúka úttaksbirgðapöntun** .</span><span class="sxs-lookup"><span data-stu-id="9aca9-125">Go to **Inventory management** \> **Setup** \> **Inventory and warehouse management parameters**, and then, on the **General** tab, set the **End output inventory order** option.</span></span>

<span data-ttu-id="9aca9-126">[![Ljúka úttaksbirgðapöntun](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span><span class="sxs-lookup"><span data-stu-id="9aca9-126">[![End output inventory order option](./media//end-output-inventory-order.png)](./media//end-output-inventory-order.png)</span></span>

<span data-ttu-id="9aca9-127">Þegar starfsmaður vöruhúss minnkar magn á tiltektarlista, þá verður samsvarandi magn birgðapantana fjarlægt úr sendingu.</span><span class="sxs-lookup"><span data-stu-id="9aca9-127">When the warehouse worker reduces the picking list quantities, then the corresponding inventory order quantities will be removed from the shipment.</span></span> <span data-ttu-id="9aca9-128">Þegar tiltektarlistinn er uppfærður á einhverjum tímapunkti, verða eftirstandandi magn tilkynnt aftur á pöntunarstig ef valkosturinn **Ljúka úttaksbirgðapöntun** er stillt á **Já**.</span><span class="sxs-lookup"><span data-stu-id="9aca9-128">When the picking list is updated at a point in time, the remaining quantities get reported back to the order if the **End output inventory order** option is set to **Yes**.</span></span> <span data-ttu-id="9aca9-129">Ef valkosturinn **Ljúka úttaksbirgðapöntun** er stilltur á **Nei**, er eftirstandandi magn geymt sem opið úttakspöntunarmagn og verður að vera bætt við nýjan tiltektarlista, sem hluta af virkninni **Opna úttakspantanir**.</span><span class="sxs-lookup"><span data-stu-id="9aca9-129">If the **End output inventory order** option is set to **No**, the remaining quantities are kept as an open output order quantity and must be added to a new picking list as part of the **Open output orders** functionality.</span></span> 

<span data-ttu-id="9aca9-130">Skipunin [![Opna úttakspantanir á valmynd fyrir Aðgerðir](./media/open-output-order.png)](./media/open-output-order.png)</span><span class="sxs-lookup"><span data-stu-id="9aca9-130">[![Open output orders command on the Functions menu](./media/open-output-order.png)](./media/open-output-order.png)</span></span>

<span data-ttu-id="9aca9-131">[![Aðgerðavalmyndin á síðunni Opna](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span><span class="sxs-lookup"><span data-stu-id="9aca9-131">[![Functions menu on the Open output orders page](./media/open-output-order-function.png)](./media/open-output-order-function.png)</span></span>

## <a name="reduce-quantity"></a><span data-ttu-id="9aca9-132">Minnka magn</span><span class="sxs-lookup"><span data-stu-id="9aca9-132">Reduce quantity</span></span>

<span data-ttu-id="9aca9-133">Þriðja færibreytan sem nota má sem hluta af ferlinu við að búa til tiltektarlista er færibreytan **Minnka magn** .</span><span class="sxs-lookup"><span data-stu-id="9aca9-133">The third parameter that you can use as part of the process of generating picking lists is the **Reduce quantity** parameter.</span></span> <span data-ttu-id="9aca9-134">Stillingar þessa færibreytu vinna með stillingunni **Frátekning** sem setur af stað frátekningarferli sem er hluti af losun til vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="9aca9-134">The setting of this parameter works together with the **Reservation** setting that triggers a reservation process as part of the release to the warehouse.</span></span>

<span data-ttu-id="9aca9-135">[![Færibreytan Minnka magn](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span><span class="sxs-lookup"><span data-stu-id="9aca9-135">[![Reduce quantity parameter](./media/reduce-quantity.png)](./media/reduce-quantity.png)</span></span>

## <a name="example-of-an-outbound-process-for-a-sales-order"></a><span data-ttu-id="9aca9-136">Dæmi um útleiðarferli fyrir sölupöntun</span><span class="sxs-lookup"><span data-stu-id="9aca9-136">Example of an outbound process for a sales order</span></span>

<span data-ttu-id="9aca9-137">Í þessu dæmi er sölupöntun með tveimur vörum.</span><span class="sxs-lookup"><span data-stu-id="9aca9-137">For this example, there is a sales order for two items.</span></span> <span data-ttu-id="9aca9-138">Við myndun tiltektarlista er valin færibreytan **Minnka magn** .</span><span class="sxs-lookup"><span data-stu-id="9aca9-138">During picking list generation, you select the **Reduce quantity** parameter.</span></span> <span data-ttu-id="9aca9-139">Þess vegna losar þú og stofnar aðeins tiltektarlínur fyrir tiltækar birgðir.</span><span class="sxs-lookup"><span data-stu-id="9aca9-139">Therefore, you release and create picking lines only for available on-hand inventory.</span></span> <span data-ttu-id="9aca9-140">Tilkynna verður tiltekt með skráningarferli fyrir tiltektarlista (**Staða tiltektarleiðar** = **Virkt**).</span><span class="sxs-lookup"><span data-stu-id="9aca9-140">The picking must be reported via a registration process for picking lists (**Picking route status** = **Activated**).</span></span>

<span data-ttu-id="9aca9-141">Birgðir sem ekki hafa verið fráteknar verða fráteknar við myndun tiltektarlista.</span><span class="sxs-lookup"><span data-stu-id="9aca9-141">The inventory that hasn't already been reserved is reserved during picking list generation.</span></span> <span data-ttu-id="9aca9-142">Ótiltækar birgðir er hægt að fjarlægja annaðhvort úr sölustað eða út í vöruhús til útleiðarferlis síðar, þegar birgðir eru tiltækar til að tína.</span><span class="sxs-lookup"><span data-stu-id="9aca9-142">The unavailable inventory can be either removed from the sales order or released to the warehouse for outbound processing later, when inventory is available for picking.</span></span>

<span data-ttu-id="9aca9-143">[![Uppfæra tiltektarlistann](./media/update-picking-list.png)](./media/update-picking-list.png)</span><span class="sxs-lookup"><span data-stu-id="9aca9-143">[![Update the picking list](./media/update-picking-list.png)](./media/update-picking-list.png)</span></span>

<span data-ttu-id="9aca9-144">Um leið og allar tiltektarlínur hafa verið teknar til á síðunni **Skráning tiltektarlista** er tengdri afhendingu lokið.</span><span class="sxs-lookup"><span data-stu-id="9aca9-144">As soon as all the picking lines have been picked on the **Picking list registration** page, the associated shipment is completed.</span></span> <span data-ttu-id="9aca9-145">Hægt er að hefja ferli fyrir fylgiseðla sölupantana með hliðsjón af völdum birgðum.</span><span class="sxs-lookup"><span data-stu-id="9aca9-145">The process for sales order packing slips can then be initialized based on the picked inventory.</span></span>

<span data-ttu-id="9aca9-146">[![Uppfæra sendingar á útleið](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span><span class="sxs-lookup"><span data-stu-id="9aca9-146">[![Update outbound shipments](./media/outbound-shipments.png)](./media/outbound-shipments.png)</span></span>
