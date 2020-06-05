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
ms.author: v-olbara
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: b1a2c9506b4444fc98a9e4f0389cbd69db4ce052
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383793"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="7bd13-103">Sameina sendingar með því að nota samstæðuvinnusvæði sendinga</span><span class="sxs-lookup"><span data-stu-id="7bd13-103">Consolidate shipments by using the shipment consolidation workbench</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7bd13-104">Þetta efnisatriði sýnir aðstæður þar sem margar pantanir eru losaðar í vöruhúsið og síðan sameinaðar í sendingar síðar með því að nota samstæðuvinnusvæði sendingar.</span><span class="sxs-lookup"><span data-stu-id="7bd13-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated into shipments later by using the shipment consolidation workbench.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="7bd13-105">Bjóða upp á sýnigögn</span><span class="sxs-lookup"><span data-stu-id="7bd13-105">Make demo data available</span></span>

<span data-ttu-id="7bd13-106">Aðstæður í þessu efnisatriði vísa í gildi og færslur sem eru innifaldar í stöðluðum sýnigögnum fyrir Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="7bd13-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="7bd13-107">Ef nota á gildin sem er boðið upp á hér eins og í æfingunum skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett og stilla lögaðilann á **USMF** áður en hafist er handa.</span><span class="sxs-lookup"><span data-stu-id="7bd13-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="7bd13-108">Setja upp samstæðureglur sendingar og afurðarsíur</span><span class="sxs-lookup"><span data-stu-id="7bd13-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="7bd13-109">Aðstæðurnar sem hér er lýst gera ráð fyrir að þegar hafi verið kveikt á eiginleikanum, farið hafi verið í gegnum æfingarnar í [Skilgreina samstæðureglur sendingar](configure-shipment-consolidation-policies.md) og reglur og aðrar færslur sem þar er lýst stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="7bd13-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="7bd13-110">Gætið þess að gera þessar æfingar áður en haldið er áfram með þessar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="7bd13-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="turn-on-the-manual-shipment-consolidation-feature"></a><span data-ttu-id="7bd13-111">Kveikja á eiginleika handvirkri sameiningu sendingar</span><span class="sxs-lookup"><span data-stu-id="7bd13-111">Turn on the manual shipment consolidation feature</span></span>

<span data-ttu-id="7bd13-112">Áður en hægt er að nota eiginleikann *Handvirk sameining sendingar* þarf að kveikja á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="7bd13-112">Before you can use the *Manual shipment consolidation* feature, you must turn it on in your system.</span></span> <span data-ttu-id="7bd13-113">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum.</span><span class="sxs-lookup"><span data-stu-id="7bd13-113">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="7bd13-114">Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="7bd13-114">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="7bd13-115">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="7bd13-115">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="7bd13-116">**Heiti eiginleika:** *Handvirk sameining sendingar*</span><span class="sxs-lookup"><span data-stu-id="7bd13-116">**Feature name:** *Manual shipment consolidation*</span></span>

<span data-ttu-id="7bd13-117">Eins og var getið í [Skilgreina samstæðureglur sendingar](configure-shipment-consolidation-policies.md) þarf einnig að kveikja á eiginleikanum *Sameina sendingar* áður en hægt er að stofna stefnur.</span><span class="sxs-lookup"><span data-stu-id="7bd13-117">As was mentioned in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), you must also turn on the *Consolidate shipment* feature before you can create policies.</span></span> <span data-ttu-id="7bd13-118">Hins vegar ætti þegar að vera búið að ljúka þessu skrefi.</span><span class="sxs-lookup"><span data-stu-id="7bd13-118">However, you should already have completed that step.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="7bd13-119">Búa til sölupantanir fyrir þessar aðstæður</span><span class="sxs-lookup"><span data-stu-id="7bd13-119">Create the sales orders for this scenario</span></span>

<span data-ttu-id="7bd13-120">Byrjaðu á því að stofna safn af sölupöntunum sem hægt er að vinna með.</span><span class="sxs-lookup"><span data-stu-id="7bd13-120">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="7bd13-121">Vinna verður með vöruhús sem er virkt fyrir ítarlegt ferli vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="7bd13-121">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="7bd13-122">Nema annað vöruhús er tilgreint með skýrum hætti verður að nota sama vöruhúsið fyrir hvert eftirtalinna pöntunarsetta.</span><span class="sxs-lookup"><span data-stu-id="7bd13-122">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="7bd13-123">Opnaðu **Viðskiptakröfur \> Pantanir \> Allar sölupantanir** og búðu til safn sölupantana sem eru með stillingarnar sem lýst er í eftirfarandi undirhlutum.</span><span class="sxs-lookup"><span data-stu-id="7bd13-123">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="7bd13-124">Búa til pöntunarsett 1</span><span class="sxs-lookup"><span data-stu-id="7bd13-124">Create order set 1</span></span>

#### <a name="sales-orders-1-1-and-1-2"></a><span data-ttu-id="7bd13-125">Sölupantanir 1-1 og 1-2</span><span class="sxs-lookup"><span data-stu-id="7bd13-125">Sales orders 1-1 and 1-2</span></span>

1. <span data-ttu-id="7bd13-126">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-126">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7bd13-127">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="7bd13-127">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="7bd13-128">**Afhendingarmáti:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="7bd13-128">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="7bd13-129">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-129">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7bd13-130">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="7bd13-130">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7bd13-131">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7bd13-131">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7bd13-132">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="7bd13-132">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="7bd13-133">Sölupöntun 1-3</span><span class="sxs-lookup"><span data-stu-id="7bd13-133">Sales order 1-3</span></span>

1. <span data-ttu-id="7bd13-134">Stofna sölupöntun sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-134">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="7bd13-135">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="7bd13-135">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="7bd13-136">**Afhendingarmáti:** *10*</span><span class="sxs-lookup"><span data-stu-id="7bd13-136">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="7bd13-137">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-137">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7bd13-138">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="7bd13-138">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7bd13-139">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7bd13-139">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7bd13-140">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="7bd13-140">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="7bd13-141">Bæta við annarri pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="7bd13-142">**Vörunúmer:** *A0002* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="7bd13-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7bd13-143">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7bd13-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="7bd13-144">**Afhendingarmáti:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="7bd13-144">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="7bd13-145">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá aðra pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="7bd13-145">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="7bd13-146">Búa til pöntunarsett 2</span><span class="sxs-lookup"><span data-stu-id="7bd13-146">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="7bd13-147">Sölupantanir 2-1 og 2-2</span><span class="sxs-lookup"><span data-stu-id="7bd13-147">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="7bd13-148">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-148">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7bd13-149">**Viðskiptavinalykill:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="7bd13-149">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="7bd13-150">**Afhendingarmáti:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="7bd13-150">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="7bd13-151">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-151">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7bd13-152">**Vörunúmer:** *M9200* (vara þar sem sía fyrir **kóða 4** er stillt á *eldfimt*)</span><span class="sxs-lookup"><span data-stu-id="7bd13-152">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="7bd13-153">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7bd13-153">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7bd13-154">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="7bd13-154">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>
1. <span data-ttu-id="7bd13-155">Bæta við annarri pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-155">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="7bd13-156">**Vörunúmer:** *M9201* (vara þar sem sía fyrir **kóða 4** er stillt á *sprengifimt*)</span><span class="sxs-lookup"><span data-stu-id="7bd13-156">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="7bd13-157">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7bd13-157">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="7bd13-158">**Afhendingarmáti:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="7bd13-158">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="7bd13-159">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá aðra pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="7bd13-159">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the second order line.</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="7bd13-160">Búa til pöntunarsett 3</span><span class="sxs-lookup"><span data-stu-id="7bd13-160">Create order set 3</span></span>

#### <a name="sales-orders-3-1-and-3-2"></a><span data-ttu-id="7bd13-161">Sölupantanir 3-1 og 3-2</span><span class="sxs-lookup"><span data-stu-id="7bd13-161">Sales orders 3-1 and 3-2</span></span>

1. <span data-ttu-id="7bd13-162">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-162">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7bd13-163">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="7bd13-163">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="7bd13-164">**Innkaupabeiðni viðskiptavinar:** *1*</span><span class="sxs-lookup"><span data-stu-id="7bd13-164">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="7bd13-165">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-165">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7bd13-166">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="7bd13-166">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7bd13-167">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7bd13-167">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7bd13-168">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="7bd13-168">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-3-3-and-3-4"></a><span data-ttu-id="7bd13-169">Sölupantanir 3-3 og 3-4</span><span class="sxs-lookup"><span data-stu-id="7bd13-169">Sales orders 3-3 and 3-4</span></span>

1. <span data-ttu-id="7bd13-170">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-170">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7bd13-171">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="7bd13-171">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="7bd13-172">**Innkaupabeiðni viðskiptavinar:** *2*</span><span class="sxs-lookup"><span data-stu-id="7bd13-172">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="7bd13-173">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-173">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7bd13-174">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="7bd13-174">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7bd13-175">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7bd13-175">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7bd13-176">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="7bd13-176">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="7bd13-177">Búa til pöntunarsett 4</span><span class="sxs-lookup"><span data-stu-id="7bd13-177">Create order set 4</span></span>

#### <a name="sales-orders-4-1-and-4-2"></a><span data-ttu-id="7bd13-178">Sölupantanir 4-1 og 4-2</span><span class="sxs-lookup"><span data-stu-id="7bd13-178">Sales orders 4-1 and 4-2</span></span>

1. <span data-ttu-id="7bd13-179">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7bd13-180">**Viðskiptavinalykill:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="7bd13-180">**Customer account:** *US-003*</span></span>

1. <span data-ttu-id="7bd13-181">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-181">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7bd13-182">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="7bd13-182">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7bd13-183">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7bd13-183">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7bd13-184">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="7bd13-184">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-3-and-4-4"></a><span data-ttu-id="7bd13-185">Sölupantanir 4-3 og 4-4</span><span class="sxs-lookup"><span data-stu-id="7bd13-185">Sales orders 4-3 and 4-4</span></span>

1. <span data-ttu-id="7bd13-186">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-186">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7bd13-187">**Viðskiptavinalykill:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="7bd13-187">**Customer account:** *US-004*</span></span>

1. <span data-ttu-id="7bd13-188">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-188">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7bd13-189">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="7bd13-189">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7bd13-190">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7bd13-190">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7bd13-191">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="7bd13-191">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-5-and-4-6"></a><span data-ttu-id="7bd13-192">Sölupantanir 4-5 og 4-6</span><span class="sxs-lookup"><span data-stu-id="7bd13-192">Sales orders 4-5 and 4-6</span></span>

1. <span data-ttu-id="7bd13-193">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-193">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7bd13-194">**Viðskiptavinalykill:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="7bd13-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="7bd13-195">**Svæði:** *6*</span><span class="sxs-lookup"><span data-stu-id="7bd13-195">**Site:** *6*</span></span>
    - <span data-ttu-id="7bd13-196">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="7bd13-196">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="7bd13-197">**Hópur:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="7bd13-197">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="7bd13-198">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-198">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7bd13-199">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="7bd13-199">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7bd13-200">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7bd13-200">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7bd13-201">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="7bd13-201">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

#### <a name="sales-orders-4-7-and-4-8"></a><span data-ttu-id="7bd13-202">Sölupantanir 4-7 og 4-8</span><span class="sxs-lookup"><span data-stu-id="7bd13-202">Sales orders 4-7 and 4-8</span></span>

1. <span data-ttu-id="7bd13-203">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-203">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="7bd13-204">**Viðskiptavinalykill:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="7bd13-204">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="7bd13-205">**Svæði:** *6*</span><span class="sxs-lookup"><span data-stu-id="7bd13-205">**Site:** *6*</span></span>
    - <span data-ttu-id="7bd13-206">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="7bd13-206">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="7bd13-207">**Hópur:** – Hafa þennan reit auðan.</span><span class="sxs-lookup"><span data-stu-id="7bd13-207">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="7bd13-208">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-208">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="7bd13-209">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="7bd13-209">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="7bd13-210">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="7bd13-210">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="7bd13-211">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="7bd13-211">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="7bd13-212">Losa pantanirnar í vöruhúsið</span><span class="sxs-lookup"><span data-stu-id="7bd13-212">Release the orders to the warehouse</span></span>

<span data-ttu-id="7bd13-213">Fylgdu þessum skrefum til að losa hverja sölupöntun sem þú bjóst til fyrir þessar aðstæður í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="7bd13-213">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="7bd13-214">Opna **Viðskiptakröfur \> Pantanir \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="7bd13-214">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="7bd13-215">Finnið og veljið sölupöntun sem á að losa.</span><span class="sxs-lookup"><span data-stu-id="7bd13-215">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="7bd13-216">Á aðgerðasvæðinu, á flipanum **Vöruhús**, skal velja **Aðgerðir \> Losa í vöruhús** til að losa valda sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="7bd13-216">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="7bd13-217">Endurtakið þetta ferli fyrir hverja sölupöntun sem var stofnuð fyrir þessar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="7bd13-217">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a><span data-ttu-id="7bd13-218">Sameina sendingarnar með því að nota samstæðuvinnusvæði sendinga</span><span class="sxs-lookup"><span data-stu-id="7bd13-218">Consolidate the shipments by using the shipment consolidation workbench</span></span>

1. <span data-ttu-id="7bd13-219">Opnaðu **Vöruhúsakerfi \> Losa í vöruhús \> Samstæðuvinnusvæði sendinga**.</span><span class="sxs-lookup"><span data-stu-id="7bd13-219">Go to **Warehouse management \> Release to warehouse \> Shipment consolidation workbench**.</span></span>
1. <span data-ttu-id="7bd13-220">Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="7bd13-220">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="7bd13-221">Í svarglugga fyrirspurnarritils á flipanum **Svið** skal velja **Bæta við** til að bæta við línu sem er með eftirfarandi stillingar á hnitanetinu:</span><span class="sxs-lookup"><span data-stu-id="7bd13-221">In the query editor dialog box, on the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="7bd13-222">**Tafla:** *Sölupantanir*</span><span class="sxs-lookup"><span data-stu-id="7bd13-222">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="7bd13-223">**Svæði:** *Sölupöntun*</span><span class="sxs-lookup"><span data-stu-id="7bd13-223">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="7bd13-224">**Skilyrði:** Færa skal inn kommuaðgreinda lista yfir sölupöntunarnúmer fyrir hvert pöntunarsett sem var búið til fyrir aðstæðurnar.</span><span class="sxs-lookup"><span data-stu-id="7bd13-224">**Criteria:** Enter a comma-separated list of the sales order numbers for each order set that you created for this scenario.</span></span>

1. <span data-ttu-id="7bd13-225">Velja skal **Í lagi** til að vista fyrirspurnina og loka glugganum.</span><span class="sxs-lookup"><span data-stu-id="7bd13-225">Select **OK** to save your query and close the dialog box.</span></span>
1. <span data-ttu-id="7bd13-226">Á aðgerðasvæðinu skal velja **Sameina sendingar**.</span><span class="sxs-lookup"><span data-stu-id="7bd13-226">On the Action Pane, select **Consolidate shipments**.</span></span>
1. <span data-ttu-id="7bd13-227">Veljið allar sendingar og síðan, á aðgerðasvæðinu, veljið **Sameina**.</span><span class="sxs-lookup"><span data-stu-id="7bd13-227">Select all the shipments, and then, on the Action Pane, select **Consolidate**.</span></span>

## <a name="verify-the-shipments"></a><span data-ttu-id="7bd13-228">Staðfesta sendingar</span><span class="sxs-lookup"><span data-stu-id="7bd13-228">Verify the shipments</span></span>

<span data-ttu-id="7bd13-229">Eftirfarandi ferli gerir kleift að staðfesta sendingarnar sem hafa verið stofnaðar eða uppfærðar í kjölfar sendingarsameiningar.</span><span class="sxs-lookup"><span data-stu-id="7bd13-229">The following procedure lets you verify the shipments that have been created or updated as a result of shipment consolidation.</span></span> <span data-ttu-id="7bd13-230">Notið það til að yfirfara hvert pöntunarsett sem var stofnað fyrir þessar aðstæður og skoðið síðan undirhlutana sem fylgja til að ganga úr skugga um réttar niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="7bd13-230">Use it to review each order set that you created for this scenario, and then review the subsections that follow to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="7bd13-231">Opnið **Vöruhúsakerfi \> Sendingar \> Allar sendingar**.</span><span class="sxs-lookup"><span data-stu-id="7bd13-231">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="7bd13-232">Finnið og veljið þá sendingu sem um ræðir.</span><span class="sxs-lookup"><span data-stu-id="7bd13-232">Find and select the required shipment.</span></span>
1. <span data-ttu-id="7bd13-233">Ef samstæðuregla var notuð þegar sendingin var stofnuð eða hún var uppfærð ætti hún að koma fram í reitnum **Samstæðuregla sendingar**.</span><span class="sxs-lookup"><span data-stu-id="7bd13-233">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="related-shipments-for-order-set-1"></a><span data-ttu-id="7bd13-234">Tengdar sendingar fyrir pöntunarsett 1</span><span class="sxs-lookup"><span data-stu-id="7bd13-234">Related shipments for order set 1</span></span>

<span data-ttu-id="7bd13-235">Tvær sendingar ættu að hafa verið stofnaðar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-235">Two shipments should have been created:</span></span>

- <span data-ttu-id="7bd13-236">Fyrsta sendingin inniheldur þrjár línur og var búin til með því að nota samstæðureglu sendingar *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="7bd13-236">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="7bd13-237">Önnur sendingin, sem notar ekki flutningsmátann *Flugfélög*, var stofnuð með því að nota samstæðureglu sendingar *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="7bd13-237">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="related-shipments-for-order-set-2"></a><span data-ttu-id="7bd13-238">Tengdar sendingar fyrir pöntunarsett 2</span><span class="sxs-lookup"><span data-stu-id="7bd13-238">Related shipments for order set 2</span></span>

<span data-ttu-id="7bd13-239">Þrjár sendingar ættu að hafa verið stofnaðar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-239">Three shipments should have been created:</span></span>

- <span data-ttu-id="7bd13-240">Fyrsta sendingin inniheldur vörur sem eru *eldfimar*.</span><span class="sxs-lookup"><span data-stu-id="7bd13-240">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="7bd13-241">Hvor hinna sendinganna tveggja inniheldur eina línu með vöru sem er *sprengifim*.</span><span class="sxs-lookup"><span data-stu-id="7bd13-241">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="related-shipments-for-order-set-3"></a><span data-ttu-id="7bd13-242">Tengdar sendingar fyrir pöntunarsett 3</span><span class="sxs-lookup"><span data-stu-id="7bd13-242">Related shipments for order set 3</span></span>

<span data-ttu-id="7bd13-243">Tvær sendingar ættu að hafa verið stofnaðar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-243">Two shipments should have been created:</span></span>

- <span data-ttu-id="7bd13-244">Fyrsta sendingin inniheldur pöntunarlínur úr sölupöntuninni þar sem reiturinn **Innkaupabeiðni viðskiptavinar** er stilltur á *1*.</span><span class="sxs-lookup"><span data-stu-id="7bd13-244">The first shipment contains order lines from the sales order where the **Customer requisition** field is set to *1*.</span></span>
- <span data-ttu-id="7bd13-245">Önnur sendingin inniheldur pöntunarlínur úr sölupöntun þar sem reiturinn **Innkaupabeiðni viðskiptavinar** er stilltur á *2*.</span><span class="sxs-lookup"><span data-stu-id="7bd13-245">The second shipment contains order lines from sales order where the **Customer requisition** field is set to *2*.</span></span>

### <a name="related-shipments-for-order-set-4"></a><span data-ttu-id="7bd13-246">Tengdar sendingar fyrir pöntunarsett 4</span><span class="sxs-lookup"><span data-stu-id="7bd13-246">Related shipments for order set 4</span></span>

<span data-ttu-id="7bd13-247">Fjórar sendingar ættu að hafa verið stofnaðar:</span><span class="sxs-lookup"><span data-stu-id="7bd13-247">Four shipments should have been created:</span></span>

- <span data-ttu-id="7bd13-248">Línur úr tveimur pöntunum fyrir viðskiptavin *US-003* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.</span><span class="sxs-lookup"><span data-stu-id="7bd13-248">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="7bd13-249">Línur úr tveimur pöntunum fyrir viðskiptavin *US-004* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.</span><span class="sxs-lookup"><span data-stu-id="7bd13-249">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="7bd13-250">Línur úr sölupöntun 4-5 og 4-6 fyrir viðskiptavin *US-007* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.</span><span class="sxs-lookup"><span data-stu-id="7bd13-250">Lines from sales orders 4-5 and 4-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="7bd13-251">Línur úr sölupöntun 4-7 og 4-8 fyrir viðskiptavin *US-007* voru settar saman í sendingu með því að nota *CrossOrder* úr samstæðureglu sendingar.</span><span class="sxs-lookup"><span data-stu-id="7bd13-251">Lines from sales orders 4-7 and 4-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7bd13-252">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7bd13-252">Additional resources</span></span>

- [<span data-ttu-id="7bd13-253">Samstæðureglur sendingar</span><span class="sxs-lookup"><span data-stu-id="7bd13-253">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="7bd13-254">Skilgreina samstæðureglur sendingar</span><span class="sxs-lookup"><span data-stu-id="7bd13-254">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)
