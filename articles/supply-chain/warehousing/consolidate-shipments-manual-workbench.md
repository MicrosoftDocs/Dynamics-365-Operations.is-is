---
title: Sameina sendingar með því að nota samstæðuvinnusvæði sendinga
description: Þetta efnisatriði sýnir aðstæður þar sem margar pantanir eru losaðar í vöruhúsið og síðan sameinaðar í sendingar síðar með því að nota samstæðuvinnusvæði sendingar.
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
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 8320c8aab82a39a8a5565e6b3e805e1065c67453
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986817"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="db244-103">Sameina sendingar með því að nota samstæðuvinnusvæði sendinga</span><span class="sxs-lookup"><span data-stu-id="db244-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db244-104">Þetta efnisatriði sýnir aðstæður þar sem margar pantanir eru losaðar í vöruhúsið og síðan sameinaðar í sendingar síðar með því að nota samstæðuvinnusvæði sendingar.</span><span class="sxs-lookup"><span data-stu-id="db244-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="db244-105">Bjóða upp á sýnigögn</span><span class="sxs-lookup"><span data-stu-id="db244-105">Make demo data available</span></span>

<span data-ttu-id="db244-106">Aðstæður í þessu efnisatriði vísa í gildi og færslur sem eru innifaldar í stöðluðum sýnigögnum fyrir Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="db244-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="db244-107">Ef nota á gildin sem er boðið upp á hér eins og í æfingunum skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett og stilla lögaðilann á **USMF** áður en hafist er handa.</span><span class="sxs-lookup"><span data-stu-id="db244-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="db244-108">Setja upp samstæðureglur sendingar og afurðarsíur</span><span class="sxs-lookup"><span data-stu-id="db244-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="db244-109">Aðstæðurnar sem hér er lýst gera ráð fyrir að þegar hafi verið kveikt á eiginleikanum, farið hafi verið í gegnum æfingarnar í [Skilgreina samstæðureglur sendingar](configure-shipment-consolidation-policies.md) og reglur og aðrar færslur sem þar er lýst stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="db244-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="db244-110">Gætið þess að gera þessar æfingar áður en haldið er áfram með þessar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="db244-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="db244-111">Kveikja á eiginleika handvirkri sameiningu sendingar</span><span class="sxs-lookup"><span data-stu-id="db244-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="db244-112">Áður en hægt er að nota eiginleikann *Handvirk sameining sendingar* þarf að kveikja á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="db244-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="db244-113">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum.</span><span class="sxs-lookup"><span data-stu-id="db244-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="db244-114">Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="db244-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="db244-115">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="db244-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="db244-116">**Heiti eiginleika:** *Handvirk sameining sendingar*</span><span class="sxs-lookup"><span data-stu-id="db244-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="db244-117">Eins og var getið í [Skilgreina samstæðureglur sendingar](configure-shipment-consolidation-policies.md) þarf einnig að kveikja á eiginleikanum *Sameina sendingar* áður en hægt er að stofna stefnur.</span><span class="sxs-lookup"><span data-stu-id="db244-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="db244-118">Hins vegar ætti þegar að vera búið að ljúka þessu skrefi.</span><span class="sxs-lookup"><span data-stu-id="db244-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="db244-119">Búa til sölupantanir fyrir þessar aðstæður</span><span class="sxs-lookup"><span data-stu-id="db244-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="db244-120">Byrjaðu á því að stofna safn af sölupöntunum sem hægt er að vinna með.</span><span class="sxs-lookup"><span data-stu-id="db244-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="db244-121">Vinna verður með vöruhús sem er virkt fyrir ítarlegt ferli vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="db244-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="db244-122">Nema annað vöruhús er tilgreint með skýrum hætti verður að nota sama vöruhúsið fyrir hvert eftirtalinna pöntunarsetta.</span><span class="sxs-lookup"><span data-stu-id="db244-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="db244-123">Opnaðu **Viðskiptakröfur \> Pantanir \> Allar sölupantanir** og búðu til safn sölupantana sem eru með stillingarnar sem lýst er í eftirfarandi undirhlutum.</span><span class="sxs-lookup"><span data-stu-id="db244-123">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="db244-124">Búa til pöntunarsett 1</span><span class="sxs-lookup"><span data-stu-id="db244-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="db244-125">Sölupantanir 1-1 og 1-2</span><span class="sxs-lookup"><span data-stu-id="db244-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="db244-126">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="db244-127">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="db244-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="db244-128">**Afhendingarmáti:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="db244-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="db244-129">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="db244-130">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="db244-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="db244-131">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="db244-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="db244-132">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="db244-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="db244-133">Sölupöntun 1-3</span><span class="sxs-lookup"><span data-stu-id="db244-133">Sales order 1-3</span></span>

1. <span data-ttu-id="db244-134">Stofna sölupöntun sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="db244-135">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="db244-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="db244-136">**Afhendingarmáti:** *10*</span><span class="sxs-lookup"><span data-stu-id="db244-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="db244-137">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="db244-138">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="db244-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="db244-139">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="db244-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="db244-140">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="db244-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="db244-141">Bæta við annarri pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="db244-142">**Vörunúmer:** *A0002* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="db244-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="db244-143">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="db244-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="db244-144">**Afhendingarmáti:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="db244-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="db244-145">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá aðra pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="db244-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="db244-146">Búa til pöntunarsett 2</span><span class="sxs-lookup"><span data-stu-id="db244-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="db244-147">Sölupantanir 2-1 og 2-2</span><span class="sxs-lookup"><span data-stu-id="db244-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="db244-148">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="db244-149">**Viðskiptavinalykill:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="db244-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="db244-150">**Afhendingarmáti:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="db244-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="db244-151">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="db244-152">**Vörunúmer:** *M9200* (vara þar sem sía fyrir **kóða 4** er stillt á *eldfimt*)</span><span class="sxs-lookup"><span data-stu-id="db244-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="db244-153">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="db244-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="db244-154">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="db244-154">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="db244-155">Bæta við annarri pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="db244-156">**Vörunúmer:** *M9201* (vara þar sem sía fyrir **kóða 4** er stillt á *sprengifimt*)</span><span class="sxs-lookup"><span data-stu-id="db244-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="db244-157">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="db244-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="db244-158">**Afhendingarmáti:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="db244-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="db244-159">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá aðra pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="db244-159">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="db244-160">Búa til pöntunarsett 3</span><span class="sxs-lookup"><span data-stu-id="db244-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="db244-161">Sölupantanir 3-1 og 3-2</span><span class="sxs-lookup"><span data-stu-id="db244-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="db244-162">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="db244-163">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="db244-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="db244-164">**Innkaupabeiðni viðskiptavinar:** *1*</span><span class="sxs-lookup"><span data-stu-id="db244-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="db244-165">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="db244-166">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="db244-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="db244-167">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="db244-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="db244-168">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="db244-168">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="db244-169">Sölupantanir 3-3 og 3-4</span><span class="sxs-lookup"><span data-stu-id="db244-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="db244-170">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="db244-171">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="db244-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="db244-172">**Innkaupabeiðni viðskiptavinar:** *2*</span><span class="sxs-lookup"><span data-stu-id="db244-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="db244-173">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="db244-174">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="db244-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="db244-175">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="db244-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="db244-176">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="db244-176">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="db244-177">Búa til pöntunarsett 4</span><span class="sxs-lookup"><span data-stu-id="db244-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="db244-178">Sölupantanir 4-1 og 4-2</span><span class="sxs-lookup"><span data-stu-id="db244-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="db244-179">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="db244-180">**Viðskiptavinalykill:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="db244-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="db244-181">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="db244-182">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="db244-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="db244-183">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="db244-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="db244-184">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="db244-184">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="db244-185">Sölupantanir 4-3 og 4-4</span><span class="sxs-lookup"><span data-stu-id="db244-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="db244-186">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="db244-187">**Viðskiptavinalykill:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="db244-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="db244-188">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="db244-189">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="db244-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="db244-190">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="db244-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="db244-191">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="db244-191">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="db244-192">Sölupantanir 4-5 og 4-6</span><span class="sxs-lookup"><span data-stu-id="db244-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="db244-193">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="db244-194">**Viðskiptavinalykill:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="db244-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="db244-195">**Svæði:** *6*</span><span class="sxs-lookup"><span data-stu-id="db244-195">**Site:** *6*</span></span>
    - <span data-ttu-id="db244-196">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="db244-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="db244-197">**Hópur:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="db244-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="db244-198">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="db244-199">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="db244-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="db244-200">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="db244-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="db244-201">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="db244-201">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="db244-202">Sölupantanir 4-7 og 4-8</span><span class="sxs-lookup"><span data-stu-id="db244-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="db244-203">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="db244-204">**Viðskiptavinalykill:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="db244-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="db244-205">**Svæði:** *6*</span><span class="sxs-lookup"><span data-stu-id="db244-205">**Site:** *6*</span></span>
    - <span data-ttu-id="db244-206">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="db244-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="db244-207">**Hópur:** – Hafa þennan reit auðan.</span><span class="sxs-lookup"><span data-stu-id="db244-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="db244-208">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="db244-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="db244-209">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="db244-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="db244-210">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="db244-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="db244-211">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="db244-211">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="db244-212">Losa pantanirnar í vöruhúsið</span><span class="sxs-lookup"><span data-stu-id="db244-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="db244-213">Fylgdu þessum skrefum til að losa hverja sölupöntun sem þú bjóst til fyrir þessar aðstæður í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="db244-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="db244-214">Opna **Viðskiptakröfur \> Pantanir \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="db244-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="db244-215">Finnið og veljið sölupöntun sem á að losa.</span><span class="sxs-lookup"><span data-stu-id="db244-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="db244-216">Á aðgerðasvæðinu, á flipanum **Vöruhús**, skal velja **Aðgerðir \> Losa í vöruhús** til að losa valda sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="db244-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="db244-217">Endurtakið þetta ferli fyrir hverja sölupöntun sem var stofnuð fyrir þessar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="db244-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="db244-218">Sameina sendingarnar með því að nota samstæðuvinnusvæði sendinga</span><span class="sxs-lookup"><span data-stu-id="db244-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="db244-219">Opnaðu **Vöruhúsakerfi \> Losa í vöruhús \> Samstæðuvinnusvæði sendinga**.</span><span class="sxs-lookup"><span data-stu-id="db244-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="db244-220">Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="db244-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="db244-221">Í svarglugga fyrirspurnarritils á flipanum **Svið** skal velja **Bæta við** til að bæta við línu sem er með eftirfarandi stillingar á hnitanetinu:</span><span class="sxs-lookup"><span data-stu-id="db244-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="db244-222">**Tafla:** *Sölupantanir*</span><span class="sxs-lookup"><span data-stu-id="db244-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="db244-223">**Svæði:** *Sölupöntun*</span><span class="sxs-lookup"><span data-stu-id="db244-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="db244-224">**Skilyrði:** Færa skal inn kommuaðgreinda lista yfir sölupöntunarnúmer fyrir hvert pöntunarsett sem var búið til fyrir aðstæðurnar.</span><span class="sxs-lookup"><span data-stu-id="db244-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="db244-225">Velja skal **Í lagi** til að vista fyrirspurnina og loka glugganum.</span><span class="sxs-lookup"><span data-stu-id="db244-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="db244-226">Á aðgerðasvæðinu skal velja **Sameina sendingar**.</span><span class="sxs-lookup"><span data-stu-id="db244-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="db244-227">Veljið allar sendingar og síðan, á aðgerðasvæðinu, veljið **Sameina**.</span><span class="sxs-lookup"><span data-stu-id="db244-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="db244-228">Staðfesta sendingar</span><span class="sxs-lookup"><span data-stu-id="db244-228">Verify the shipments</span></span>

<span data-ttu-id="db244-229">Eftirfarandi ferli gerir kleift að staðfesta sendingarnar sem hafa verið stofnaðar eða uppfærðar í kjölfar sendingarsameiningar.</span><span class="sxs-lookup"><span data-stu-id="db244-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="db244-230">Notið það til að yfirfara hvert pöntunarsett sem var stofnað fyrir þessar aðstæður og skoðið síðan undirhlutana sem fylgja til að ganga úr skugga um réttar niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="db244-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="db244-231">Opnið **Vöruhúsakerfi \> Sendingar \> Allar sendingar**.</span><span class="sxs-lookup"><span data-stu-id="db244-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="db244-232">Finnið og veljið þá sendingu sem um ræðir.</span><span class="sxs-lookup"><span data-stu-id="db244-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="db244-233">Ef samstæðuregla var notuð þegar sendingin var stofnuð eða hún var uppfærð ætti hún að koma fram í reitnum **Samstæðuregla sendingar**.</span><span class="sxs-lookup"><span data-stu-id="db244-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="db244-234">Tengdar sendingar fyrir pöntunarsett 1</span><span class="sxs-lookup"><span data-stu-id="db244-234">Related shipments for order set 1</span></span>

<span data-ttu-id="db244-235">Tvær sendingar ættu að hafa verið stofnaðar:</span><span class="sxs-lookup"><span data-stu-id="db244-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="db244-236">Fyrsta sendingin inniheldur þrjár línur og var búin til með því að nota samstæðureglu sendingar *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="db244-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="db244-237">Önnur sendingin, sem notar ekki flutningsmátann *Flugfélög*, var stofnuð með því að nota samstæðureglu sendingar *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="db244-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="db244-238">Tengdar sendingar fyrir pöntunarsett 2</span><span class="sxs-lookup"><span data-stu-id="db244-238">Related shipments for order set 2</span></span>

<span data-ttu-id="db244-239">Þrjár sendingar ættu að hafa verið stofnaðar:</span><span class="sxs-lookup"><span data-stu-id="db244-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="db244-240">Fyrsta sendingin inniheldur vörur sem eru *eldfimar*.</span><span class="sxs-lookup"><span data-stu-id="db244-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="db244-241">Hvor hinna sendinganna tveggja inniheldur eina línu með vöru sem er *sprengifim*.</span><span class="sxs-lookup"><span data-stu-id="db244-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="db244-242">Tengdar sendingar fyrir pöntunarsett 3</span><span class="sxs-lookup"><span data-stu-id="db244-242">Related shipments for order set 3</span></span>

<span data-ttu-id="db244-243">Tvær sendingar ættu að hafa verið stofnaðar:</span><span class="sxs-lookup"><span data-stu-id="db244-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="db244-244">Fyrsta sendingin inniheldur pöntunarlínur úr sölupöntuninni þar sem reiturinn **Innkaupabeiðni viðskiptavinar** er stilltur á *1*.</span><span class="sxs-lookup"><span data-stu-id="db244-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="db244-245">Önnur sendingin inniheldur pöntunarlínur úr sölupöntun þar sem reiturinn **Innkaupabeiðni viðskiptavinar** er stilltur á *2*.</span><span class="sxs-lookup"><span data-stu-id="db244-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="db244-246">Tengdar sendingar fyrir pöntunarsett 4</span><span class="sxs-lookup"><span data-stu-id="db244-246">Related shipments for order set 4</span></span>

<span data-ttu-id="db244-247">Fjórar sendingar ættu að hafa verið stofnaðar:</span><span class="sxs-lookup"><span data-stu-id="db244-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="db244-248">Línur úr tveimur pöntunum fyrir viðskiptavin *US-003* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.</span><span class="sxs-lookup"><span data-stu-id="db244-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="db244-249">Línur úr tveimur pöntunum fyrir viðskiptavin *US-004* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.</span><span class="sxs-lookup"><span data-stu-id="db244-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="db244-250">Línur úr sölupöntun 4-5 og 4-6 fyrir viðskiptavin *US-007* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.</span><span class="sxs-lookup"><span data-stu-id="db244-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="db244-251">Línur úr sölupöntun 4-7 og 4-8 fyrir viðskiptavin *US-007* voru settar saman í sendingu með því að nota *CrossOrder* úr samstæðureglu sendingar.</span><span class="sxs-lookup"><span data-stu-id="db244-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db244-252">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="db244-252">Additional resources</span></span>

- [<span data-ttu-id="db244-253">Samstæðureglur sendingar</span><span class="sxs-lookup"><span data-stu-id="db244-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="db244-254">Skilgreina samstæðureglur sendingar</span><span class="sxs-lookup"><span data-stu-id="db244-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
