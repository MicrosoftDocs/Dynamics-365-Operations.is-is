---
title: Sameina sendingar með því að nota „Losa í vöruhús“ á vinnusvæði farmáætlunar
description: Þetta efnisatriði sýnir aðstæður þar sem margar pantanir eru losaðar í vöruhúsið í sömu hleðslu og eru svo sameinaðar sjálfkrafa í sendingar.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 2f1dd5c743664e638c043b600ae7b0f6bce5ddcd
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986841"
---
# <a name="consolidate-shipments-by-using-release-to-warehouse-from-the-load-planning-workbench"></a><span data-ttu-id="a7aef-103">Sameina sendingar með því að nota „Losa í vöruhús“ á vinnusvæði farmáætlunar</span><span class="sxs-lookup"><span data-stu-id="a7aef-103">Consolidate shipments by using Release to warehouse from the load planning workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a7aef-104">Þetta efnisatriði sýnir aðstæður þar sem margar pantanir eru losaðar í vöruhúsið í sömu hleðslu og eru svo sameinaðar sjálfkrafa í sendingar.</span><span class="sxs-lookup"><span data-stu-id="a7aef-104">This topic presents a scenario where multiple orders are released to the warehouse in the same load and are then automatically consolidated into shipments.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="a7aef-105">Bjóða upp á sýnigögn</span><span class="sxs-lookup"><span data-stu-id="a7aef-105">Make demo data available</span></span>

<span data-ttu-id="a7aef-106">Aðstæður í þessu efnisatriði vísa í gildi og færslur sem eru innifaldar í stöðluðum sýnigögnum fyrir Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a7aef-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a7aef-107">Ef nota á gildin sem er boðið upp á hér eins og í æfingunum skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett og stilla lögaðilann á **USMF** áður en hafist er handa.</span><span class="sxs-lookup"><span data-stu-id="a7aef-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="a7aef-108">Setja upp samstæðureglur sendingar og afurðarsíur</span><span class="sxs-lookup"><span data-stu-id="a7aef-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="a7aef-109">Aðstæðurnar sem hér er lýst gera ráð fyrir að þegar hafi verið kveikt á eiginleikanum, farið hafi verið í gegnum æfingarnar í [Skilgreina samstæðureglur sendingar](configure-shipment-consolidation-policies.md) og reglur og aðrar færslur sem þar er lýst stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="a7aef-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="a7aef-110">Gætið þess að gera þessar æfingar áður en haldið er áfram með þessar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="a7aef-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="a7aef-111">Búa til sölupantanir fyrir þessar aðstæður</span><span class="sxs-lookup"><span data-stu-id="a7aef-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="a7aef-112">Byrjaðu á því að stofna safn af sölupöntunum sem hægt er að vinna með.</span><span class="sxs-lookup"><span data-stu-id="a7aef-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="a7aef-113">Vinna verður með vöruhús sem er virkt fyrir ítarlegt ferli vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="a7aef-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="a7aef-114">Nema annað vöruhús er tilgreint með skýrum hætti verður að nota sama vöruhúsið fyrir hvert eftirtalinna pöntunarsetta.</span><span class="sxs-lookup"><span data-stu-id="a7aef-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="a7aef-115">Opnaðu **Viðskiptakröfur \> Pantanir \> Allar sölupantanir** og búðu til safn sölupantana sem eru með stillingarnar sem lýst er í eftirfarandi undirhlutum.</span><span class="sxs-lookup"><span data-stu-id="a7aef-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="a7aef-116">Búa til pöntunarsett 1</span><span class="sxs-lookup"><span data-stu-id="a7aef-116">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="a7aef-117">Sölupöntun 1-1</span><span class="sxs-lookup"><span data-stu-id="a7aef-117">Sales order 1-1</span></span>

1. <span data-ttu-id="a7aef-118">Stofna sölupöntun sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-118">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="a7aef-119">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a7aef-119">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a7aef-120">**Afhendingarmáti:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="a7aef-120">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="a7aef-121">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-121">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a7aef-122">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="a7aef-122">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a7aef-123">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a7aef-123">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a7aef-124">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="a7aef-124">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="a7aef-125">Sölupöntun 1-2</span><span class="sxs-lookup"><span data-stu-id="a7aef-125">Sales order 1-2</span></span>

1. <span data-ttu-id="a7aef-126">Stofna sölupöntun sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-126">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="a7aef-127">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a7aef-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a7aef-128">**Afhendingarmáti:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="a7aef-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="a7aef-129">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a7aef-130">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="a7aef-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a7aef-131">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a7aef-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a7aef-132">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="a7aef-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="a7aef-133">Sölupöntun 1-3</span><span class="sxs-lookup"><span data-stu-id="a7aef-133">Sales order 1-3</span></span>

1. <span data-ttu-id="a7aef-134">Stofna sölupöntun sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="a7aef-135">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a7aef-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a7aef-136">**Afhendingarmáti:** *10*</span><span class="sxs-lookup"><span data-stu-id="a7aef-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="a7aef-137">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a7aef-138">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="a7aef-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a7aef-139">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a7aef-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a7aef-140">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="a7aef-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="a7aef-141">Bæta við annarri pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="a7aef-142">**Vörunúmer:** *A0002* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="a7aef-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a7aef-143">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a7aef-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="a7aef-144">**Afhendingarmáti:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="a7aef-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="a7aef-145">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá aðra pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="a7aef-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="a7aef-146">Búa til pöntunarsett 2</span><span class="sxs-lookup"><span data-stu-id="a7aef-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="a7aef-147">Sölupantanir 2-1 og 2-2</span><span class="sxs-lookup"><span data-stu-id="a7aef-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="a7aef-148">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a7aef-149">**Viðskiptavinalykill:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="a7aef-149">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="a7aef-150">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-150">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a7aef-151">**Vörunúmer:** *M9200* (vara þar sem sía fyrir **kóða 4** er stillt á *eldfimt*)</span><span class="sxs-lookup"><span data-stu-id="a7aef-151">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="a7aef-152">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a7aef-152">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a7aef-153">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="a7aef-153">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="a7aef-154">Bæta við annarri pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-154">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="a7aef-155">**Vörunúmer:** *M9201* (vara þar sem sía fyrir **kóða 4** er stillt á *sprengifimt*)</span><span class="sxs-lookup"><span data-stu-id="a7aef-155">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="a7aef-156">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a7aef-156">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="a7aef-157">**Afhendingarmáti:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="a7aef-157">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="a7aef-158">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá aðra pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="a7aef-158">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="a7aef-159">Búa til pöntunarsett 3</span><span class="sxs-lookup"><span data-stu-id="a7aef-159">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="a7aef-160">Sölupantanir 3-1 og 3-2</span><span class="sxs-lookup"><span data-stu-id="a7aef-160">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="a7aef-161">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-161">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a7aef-162">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a7aef-162">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a7aef-163">**Innkaupabeiðni viðskiptavinar:** *1*</span><span class="sxs-lookup"><span data-stu-id="a7aef-163">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="a7aef-164">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-164">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a7aef-165">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="a7aef-165">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a7aef-166">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a7aef-166">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a7aef-167">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="a7aef-167">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="a7aef-168">Sölupantanir 3-3 og 3-4</span><span class="sxs-lookup"><span data-stu-id="a7aef-168">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="a7aef-169">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-169">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a7aef-170">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="a7aef-170">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="a7aef-171">**Innkaupabeiðni viðskiptavinar:** *2*</span><span class="sxs-lookup"><span data-stu-id="a7aef-171">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="a7aef-172">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-172">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a7aef-173">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="a7aef-173">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a7aef-174">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a7aef-174">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a7aef-175">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="a7aef-175">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="a7aef-176">Búa til pöntunarsett 4</span><span class="sxs-lookup"><span data-stu-id="a7aef-176">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="a7aef-177">Sölupantanir 4-1 og 4-2</span><span class="sxs-lookup"><span data-stu-id="a7aef-177">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="a7aef-178">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-178">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a7aef-179">**Viðskiptavinalykill:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="a7aef-179">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="a7aef-180">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-180">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a7aef-181">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="a7aef-181">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a7aef-182">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a7aef-182">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a7aef-183">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="a7aef-183">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="a7aef-184">Sölupantanir 4-3 og 4-4</span><span class="sxs-lookup"><span data-stu-id="a7aef-184">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="a7aef-185">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-185">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a7aef-186">**Viðskiptavinalykill:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="a7aef-186">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="a7aef-187">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-187">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a7aef-188">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="a7aef-188">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a7aef-189">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a7aef-189">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a7aef-190">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="a7aef-190">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="a7aef-191">Sölupantanir 4-5 og 4-6</span><span class="sxs-lookup"><span data-stu-id="a7aef-191">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="a7aef-192">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-192">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a7aef-193">**Viðskiptavinalykill:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="a7aef-193">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="a7aef-194">**Svæði:** *6*</span><span class="sxs-lookup"><span data-stu-id="a7aef-194">**Site:** *6*</span></span>
    - <span data-ttu-id="a7aef-195">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="a7aef-195">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="a7aef-196">**Hópur:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="a7aef-196">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="a7aef-197">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a7aef-198">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="a7aef-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a7aef-199">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a7aef-199">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a7aef-200">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="a7aef-200">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="a7aef-201">Sölupantanir 4-7 og 4-8</span><span class="sxs-lookup"><span data-stu-id="a7aef-201">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="a7aef-202">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-202">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="a7aef-203">**Viðskiptavinalykill:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="a7aef-203">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="a7aef-204">**Svæði:** *6*</span><span class="sxs-lookup"><span data-stu-id="a7aef-204">**Site:** *6*</span></span>
    - <span data-ttu-id="a7aef-205">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="a7aef-205">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="a7aef-206">**Hópur:** – Hafa þennan reit auðan.</span><span class="sxs-lookup"><span data-stu-id="a7aef-206">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="a7aef-207">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-207">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="a7aef-208">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="a7aef-208">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="a7aef-209">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="a7aef-209">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="a7aef-210">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="a7aef-210">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a><span data-ttu-id="a7aef-211">Nota vinnusvæði hleðsluáætlunar til að búa til hleðslur og losa þær í vöruhúsið</span><span class="sxs-lookup"><span data-stu-id="a7aef-211">Use the load planning workbench to create loads and release them to the warehouse</span></span>

<span data-ttu-id="a7aef-212">Fylgið eftirfarandi skrefum til að búa til hleðslu fyrir hvert pöntunarsett sem stofnað var fyrir þessar aðstæður og losið hana síðan í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="a7aef-212">Follow these steps to create a load for each order set that you created for this scenario and then release it to the warehouse.</span></span>

1. <span data-ttu-id="a7aef-213">Farið í **Vöruhúsakerfi \> Hleðsla \> Vinnusvæði hleðsluáætlunar**.</span><span class="sxs-lookup"><span data-stu-id="a7aef-213">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="a7aef-214">Á flipanum **Sölulínur** skal finna og velja allar sölupöntunarlínur úr einni af pöntunarsettunum sem voru stofnuð fyrir þessar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="a7aef-214">On the **Sales lines** tab, find and select all the sales order lines from one of the order sets that you created for this scenario.</span></span>
1. <span data-ttu-id="a7aef-215">Í aðgerðasvæði, á flipanum **Framboð og eftirspurn** skal velja **Bæta við \> Við nýja hleðslu** til að bæta völdum pöntunarlínum við nýja hleðslu.</span><span class="sxs-lookup"><span data-stu-id="a7aef-215">On the Action Pane, on the **Supply and demand** tab, select **Add \> To new load** to add the selected order lines to a new Load.</span></span>
1. <span data-ttu-id="a7aef-216">Í svarglugganum **Úthlutun hleðslusniðmáts** í reitnum **Kenni hleðslusniðmáts** skal velja hleðslusniðmát, svo sem *Stnd hleðslusniðmát*.</span><span class="sxs-lookup"><span data-stu-id="a7aef-216">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *Stnd Load Template*.</span></span>
1. <span data-ttu-id="a7aef-217">Veldu **Í lagi** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="a7aef-217">Select **OK** to close the dialog box.</span></span> 
1. <span data-ttu-id="a7aef-218">Í hlutanum **Hleðsla** er hægt að finna og velja hleðsluna sem var verið að stofna.</span><span class="sxs-lookup"><span data-stu-id="a7aef-218">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="a7aef-219">Veljið **Losa \> Losa í vöruhús** til að losa valda hleðslu í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="a7aef-219">Select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="a7aef-220">Endurtakið þetta ferli fyrir hin þrjú pantanamengi sem voru stofnuð fyrir þessar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="a7aef-220">Repeat this procedure for the other three order sets that you created for this scenario.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="a7aef-221">Staðfesta sendingar</span><span class="sxs-lookup"><span data-stu-id="a7aef-221">Verify the shipments</span></span>

<span data-ttu-id="a7aef-222">Eftirfarandi ferli gerir kleift að staðfesta sendingarnar sem hafa verið stofnaðar eða uppfærðar í kjölfar sendingarsameiningar.</span><span class="sxs-lookup"><span data-stu-id="a7aef-222">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="a7aef-223">Notið það til að yfirfara hvert pöntunarsett sem var stofnað fyrir þessar aðstæður og skoðið síðan undirhlutana sem fylgja til að ganga úr skugga um réttar niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="a7aef-223">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="a7aef-224">Opnið **Vöruhúsakerfi \> Sendingar \> Allar sendingar**.</span><span class="sxs-lookup"><span data-stu-id="a7aef-224">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="a7aef-225">Finnið og veljið þá sendingu sem um ræðir.</span><span class="sxs-lookup"><span data-stu-id="a7aef-225">Find and select the required shipment.</span></span>
1. <span data-ttu-id="a7aef-226">Ef samstæðuregla var notuð þegar sendingin var stofnuð eða hún var uppfærð ætti hún að koma fram í reitnum **Samstæðuregla sendingar**.</span><span class="sxs-lookup"><span data-stu-id="a7aef-226">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-order-set-1-in-one-load"></a><span data-ttu-id="a7aef-227">Losunarpantanasett 1 í einum farmi</span><span class="sxs-lookup"><span data-stu-id="a7aef-227">Release order set 1 in one load</span></span>

<span data-ttu-id="a7aef-228">Tvær sendingar ættu að hafa verið stofnaðar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-228">Two shipments should have been created:</span></span>

- <span data-ttu-id="a7aef-229">Fyrsta sendingin inniheldur þrjár línur og var búin til með því að nota samstæðureglu sendingar *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="a7aef-229">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="a7aef-230">Önnur sendingin, sem notar ekki flutningsmátann *Flugfélög*, var stofnuð með því að nota samstæðureglu sendingar *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="a7aef-230">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-order-set-2-in-one-load"></a><span data-ttu-id="a7aef-231">Losunarpantanasett 2 í einum farmi</span><span class="sxs-lookup"><span data-stu-id="a7aef-231">Release order set 2 in one load</span></span>

<span data-ttu-id="a7aef-232">Þrjár sendingar ættu að hafa verið stofnaðar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-232">Three shipments should have been created:</span></span>

- <span data-ttu-id="a7aef-233">Fyrsta sendingin inniheldur *eldfimu* vörurnar.</span><span class="sxs-lookup"><span data-stu-id="a7aef-233">The first shipment contains the *Flammable* items.</span></span>
- <span data-ttu-id="a7aef-234">Hvor hinna sendinganna tveggja inniheldur eina línu með vöru sem er *sprengifim*.</span><span class="sxs-lookup"><span data-stu-id="a7aef-234">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-order-set-3-in-one-load"></a><span data-ttu-id="a7aef-235">Losunarpantanasett 3 í einum farmi</span><span class="sxs-lookup"><span data-stu-id="a7aef-235">Release order set 3 in one load</span></span>

<span data-ttu-id="a7aef-236">Tvær sendingar ættu að hafa verið stofnaðar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-236">Two shipments should have been created:</span></span>

- <span data-ttu-id="a7aef-237">Fyrsta sendingin inniheldur pöntunarlínur úr sölupöntuninni þar sem reiturinn **Innkaupabeiðni viðskiptavinar** er stilltur á *1*.</span><span class="sxs-lookup"><span data-stu-id="a7aef-237">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="a7aef-238">Önnur sendingin inniheldur pöntunarlínur úr sölupöntun þar sem reiturinn **Innkaupabeiðni viðskiptavinar** er stilltur á *2*.</span><span class="sxs-lookup"><span data-stu-id="a7aef-238">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="release-order-set-4-in-one-load"></a><span data-ttu-id="a7aef-239">Losunarpantanasett 4 í einum farmi</span><span class="sxs-lookup"><span data-stu-id="a7aef-239">Release order set 4 in one load</span></span>

<span data-ttu-id="a7aef-240">Fjórar sendingar ættu að hafa verið stofnaðar:</span><span class="sxs-lookup"><span data-stu-id="a7aef-240">Four shipments should have been created:</span></span>

- <span data-ttu-id="a7aef-241">Línur úr tveimur pöntunum fyrir viðskiptavinalykil *US-003* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.</span><span class="sxs-lookup"><span data-stu-id="a7aef-241">Lines from two orders for customer account *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="a7aef-242">Línur úr tveimur pöntunum fyrir viðskiptavinalykil *US-004* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.</span><span class="sxs-lookup"><span data-stu-id="a7aef-242">Lines from two orders for customer account *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="a7aef-243">Línur úr sölupöntun 4-5 og 4-6 fyrir viðskiptavinalykil *US-007* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.</span><span class="sxs-lookup"><span data-stu-id="a7aef-243">Lines from sales orders 4-5 and 4-6 for customer account *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="a7aef-244">Línur úr sölupöntun 4-7 og 4-8 fyrir viðskiptavinlykil *US-007* voru settar saman í sendingu með því að nota *CrossOrder* úr samstæðureglu sendingar.</span><span class="sxs-lookup"><span data-stu-id="a7aef-244">Lines from sales orders 4-7 and 4-8 for customer account *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a7aef-245">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a7aef-245">Additional resources</span></span>

- [<span data-ttu-id="a7aef-246">Samstæðureglur sendingar</span><span class="sxs-lookup"><span data-stu-id="a7aef-246">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="a7aef-247">Skilgreina samstæðureglur sendingar</span><span class="sxs-lookup"><span data-stu-id="a7aef-247">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
