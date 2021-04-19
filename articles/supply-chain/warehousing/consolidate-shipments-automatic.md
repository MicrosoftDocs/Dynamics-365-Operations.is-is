---
title: Sameina sendingar þegar þær eru losaðar í vöruhús með því að nota sjálfvirka losun sölupantana
description: Þetta efnisatriði sýnir aðstæður þar sem margar pantanir eru losaðar í vöruhúsið í sama sjálfvirka ferli vöruhúsakerfis.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 82a95ecf196ef7c33831da7f4d03df629b17fa53
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807561"
---
# <a name="consolidate-shipments-when-they-are-released-to-the-warehouse-by-using-automatic-release-of-sales-orders"></a><span data-ttu-id="21122-103">Sameina sendingar þegar þær eru losaðar í vöruhús með því að nota sjálfvirka losun sölupantana</span><span class="sxs-lookup"><span data-stu-id="21122-103">Consolidate shipments when they are released to the warehouse by using Automatic release of sales orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21122-104">Þetta efnisatriði sýnir aðstæður þar sem margar pantanir eru losaðar í vöruhúsið í sama sjálfvirka ferli vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="21122-104">This topic presents a scenario where multiple orders are released to the warehouse in the same automated release-to-warehouse periodic procedure.</span></span> <span data-ttu-id="21122-105">Pantanirnar verða sameinaðar sjálfkrafa í sendingar, samkvæmt reglum sem eru skilgreindar sem samstæðureglur sendingar.</span><span class="sxs-lookup"><span data-stu-id="21122-105">The orders will automatically be consolidated into shipments, based on rules that are defined as shipment consolidation policies.</span></span>

<span data-ttu-id="21122-106">Meðan á atburðarásinni stendur verða söfn sölupantana stofnuð og hvert safn losað til vöruhússins.</span><span class="sxs-lookup"><span data-stu-id="21122-106">During the scenario, you will create sets of sales orders and release each set to the warehouse.</span></span> <span data-ttu-id="21122-107">Þú munt síðan yfirfara sendingar sem eru stofnaðar eða uppfærðar meðan á sendingarsamstæðu stendur, með hliðsjón af skilgreindum stefnum.</span><span class="sxs-lookup"><span data-stu-id="21122-107">You will then review the shipments that are created or updated during shipment consolidation, based on the configured policies.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="21122-108">Bjóða upp á sýnigögn</span><span class="sxs-lookup"><span data-stu-id="21122-108">Make demo data available</span></span>

<span data-ttu-id="21122-109">Aðstæður í þessu efnisatriði vísa í gildi og færslur sem eru innifaldar í stöðluðum sýnigögnum fyrir Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="21122-109">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="21122-110">Ef nota á gildin sem er boðið upp á hér eins og í æfingunum skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett og stilla lögaðilann á **USMF** áður en hafist er handa.</span><span class="sxs-lookup"><span data-stu-id="21122-110">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="21122-111">Setja upp samstæðureglur sendingar og afurðarsíur</span><span class="sxs-lookup"><span data-stu-id="21122-111">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="21122-112">Aðstæðurnar sem hér er lýst gera ráð fyrir að þegar hafi verið kveikt á eiginleikanum, farið hafi verið í gegnum æfingarnar í [Skilgreina samstæðureglur sendingar](configure-shipment-consolidation-policies.md) og reglur og aðrar færslur sem þar er lýst stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="21122-112">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="21122-113">Gætið þess að gera þessar æfingar áður en haldið er áfram með þessar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="21122-113">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="21122-114">Búa til sölupantanir fyrir þessar aðstæður</span><span class="sxs-lookup"><span data-stu-id="21122-114">Create the sales orders for this scenario</span></span>

<span data-ttu-id="21122-115">Byrjaðu á því að stofna safn af sölupöntunum sem hægt er að vinna með.</span><span class="sxs-lookup"><span data-stu-id="21122-115">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="21122-116">Vinna verður með vöruhús sem er virkt fyrir ítarlegt ferli vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="21122-116">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="21122-117">Nema annað vöruhús er tilgreint með skýrum hætti verður að nota sama vöruhúsið fyrir hvert eftirtalinna pöntunarsetta.</span><span class="sxs-lookup"><span data-stu-id="21122-117">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="21122-118">Opnaðu **Viðskiptakröfur \> Pantanir \> Allar sölupantanir** og búðu til safn sölupantana sem eru með stillingarnar sem lýst er í eftirfarandi undirhlutum.</span><span class="sxs-lookup"><span data-stu-id="21122-118">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-order-set-1"></a><span data-ttu-id="21122-119">Búa til pöntunarsett 1</span><span class="sxs-lookup"><span data-stu-id="21122-119">Create order set 1</span></span>

#### <a name="sales-order-1-1"></a><span data-ttu-id="21122-120">Sölupöntun 1-1</span><span class="sxs-lookup"><span data-stu-id="21122-120">Sales order 1-1</span></span>

1. <span data-ttu-id="21122-121">Stofna sölupöntun sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-121">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="21122-122">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="21122-122">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="21122-123">**Afhendingarmáti:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="21122-123">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="21122-124">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-124">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="21122-125">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="21122-125">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="21122-126">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="21122-126">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-2"></a><span data-ttu-id="21122-127">Sölupöntun 1-2</span><span class="sxs-lookup"><span data-stu-id="21122-127">Sales order 1-2</span></span>

1. <span data-ttu-id="21122-128">Stofna sölupöntun sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-128">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="21122-129">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="21122-129">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="21122-130">**Afhendingarmáti:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="21122-130">**Mode of delivery:** *Airwa-Air*</span></span>

1. <span data-ttu-id="21122-131">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-131">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="21122-132">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="21122-132">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="21122-133">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="21122-133">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-1-3"></a><span data-ttu-id="21122-134">Sölupöntun 1-3</span><span class="sxs-lookup"><span data-stu-id="21122-134">Sales order 1-3</span></span>

1. <span data-ttu-id="21122-135">Stofna sölupöntun sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-135">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="21122-136">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="21122-136">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="21122-137">**Afhendingarmáti:** *10*</span><span class="sxs-lookup"><span data-stu-id="21122-137">**Mode of delivery:** *10*</span></span>

1. <span data-ttu-id="21122-138">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-138">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="21122-139">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="21122-139">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="21122-140">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="21122-140">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="21122-141">Bæta við annarri pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-141">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="21122-142">**Vörunúmer:** *A0002* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="21122-142">**Item number:** *A0002* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="21122-143">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="21122-143">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="21122-144">**Afhendingarmáti:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="21122-144">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-2"></a><span data-ttu-id="21122-145">Búa til pöntunarsett 2</span><span class="sxs-lookup"><span data-stu-id="21122-145">Create order set 2</span></span>

#### <a name="sales-orders-2-1-and-2-2"></a><span data-ttu-id="21122-146">Sölupantanir 2-1 og 2-2</span><span class="sxs-lookup"><span data-stu-id="21122-146">Sales orders 2-1 and 2-2</span></span>

1. <span data-ttu-id="21122-147">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-147">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="21122-148">**Viðskiptavinalykill:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="21122-148">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="21122-149">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-149">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="21122-150">**Vörunúmer:** *M9200* (vara þar sem sía fyrir **kóða 4** er stillt á *eldfimt*)</span><span class="sxs-lookup"><span data-stu-id="21122-150">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="21122-151">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="21122-151">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="21122-152">Bæta við annarri pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-152">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="21122-153">**Vörunúmer:** *M9201* (vara þar sem sía fyrir **kóða 4** er stillt á *sprengifimt*)</span><span class="sxs-lookup"><span data-stu-id="21122-153">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="21122-154">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="21122-154">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="21122-155">**Afhendingarmáti:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="21122-155">**Mode of delivery:** *Airwa-Air*</span></span>

### <a name="create-order-set-3"></a><span data-ttu-id="21122-156">Búa til pöntunarsett 3</span><span class="sxs-lookup"><span data-stu-id="21122-156">Create order set 3</span></span>

#### <a name="sales-order-3-1"></a><span data-ttu-id="21122-157">Sölupöntun 3-1</span><span class="sxs-lookup"><span data-stu-id="21122-157">Sales order 3-1</span></span>

1. <span data-ttu-id="21122-158">Stofna sölupöntun sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-158">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="21122-159">**Viðskiptavinalykill:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="21122-159">**Customer account:** *US-002*</span></span>

1. <span data-ttu-id="21122-160">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-160">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="21122-161">**Vörunúmer:** *M9200* (vara þar sem sía fyrir **kóða 4** er stillt á *eldfimt*)</span><span class="sxs-lookup"><span data-stu-id="21122-161">**Item number:** *M9200* (an item where the **Code 4** filter is set to *Flammable*)</span></span>
    - <span data-ttu-id="21122-162">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="21122-162">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="21122-163">Bæta við annarri pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-163">Add a second order line that has the following settings:</span></span>

    - <span data-ttu-id="21122-164">**Vörunúmer:** *M9201* (vara þar sem sía fyrir **kóða 4** er stillt á *sprengifimt*)</span><span class="sxs-lookup"><span data-stu-id="21122-164">**Item number:** *M9201* (an item where the **Code 4** filter is set to *Explosive*)</span></span>
    - <span data-ttu-id="21122-165">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="21122-165">**Quantity:** *1.00*</span></span>
    - <span data-ttu-id="21122-166">**Afhendingarmáti:** *Airwa-Air*</span><span class="sxs-lookup"><span data-stu-id="21122-166">**Mode of delivery:** *Airwa-Air*</span></span>

> [!NOTE]
> <span data-ttu-id="21122-167">Þessi pöntun er eins og pantanirnar tvær sem voru stofnaðar fyrir pantanasett 2.</span><span class="sxs-lookup"><span data-stu-id="21122-167">This order is identical to the two orders that you created for order set 2.</span></span> <span data-ttu-id="21122-168">Það er hins vegar skráð sem eigin pantanasett vegna þess að það verður gefið út sérstaklega síðar í þessari atburðarás.</span><span class="sxs-lookup"><span data-stu-id="21122-168">However, it's listed as its own order set because you will release it separately later in this scenario.</span></span>

### <a name="create-order-set-4"></a><span data-ttu-id="21122-169">Búa til pöntunarsett 4</span><span class="sxs-lookup"><span data-stu-id="21122-169">Create order set 4</span></span>

#### <a name="sales-order-4-1"></a><span data-ttu-id="21122-170">Sölupöntun 4-1</span><span class="sxs-lookup"><span data-stu-id="21122-170">Sales order 4-1</span></span>

1. <span data-ttu-id="21122-171">Stofna sölupöntun sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-171">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="21122-172">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="21122-172">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="21122-173">**Innkaupabeiðni viðskiptavinar:** *1*</span><span class="sxs-lookup"><span data-stu-id="21122-173">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="21122-174">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-174">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="21122-175">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="21122-175">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="21122-176">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="21122-176">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-5"></a><span data-ttu-id="21122-177">Búa til pöntunarsett 5</span><span class="sxs-lookup"><span data-stu-id="21122-177">Create order set 5</span></span>

#### <a name="sales-orders-5-1-and-5-2"></a><span data-ttu-id="21122-178">Sölupantanir 5-1 og 5-2</span><span class="sxs-lookup"><span data-stu-id="21122-178">Sales orders 5-1 and 5-2</span></span>

1. <span data-ttu-id="21122-179">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-179">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="21122-180">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="21122-180">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="21122-181">**Innkaupabeiðni viðskiptavinar:** *2*</span><span class="sxs-lookup"><span data-stu-id="21122-181">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="21122-182">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-182">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="21122-183">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="21122-183">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="21122-184">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="21122-184">**Quantity:** *1.00*</span></span>

#### <a name="sales-order-5-3"></a><span data-ttu-id="21122-185">Sölupöntun 5-3</span><span class="sxs-lookup"><span data-stu-id="21122-185">Sales order 5-3</span></span>

1. <span data-ttu-id="21122-186">Stofna sölupöntun sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-186">Create a sales order that has the following settings:</span></span>

    - <span data-ttu-id="21122-187">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="21122-187">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="21122-188">**Innkaupabeiðni viðskiptavinar:** *1*</span><span class="sxs-lookup"><span data-stu-id="21122-188">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="21122-189">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-189">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="21122-190">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="21122-190">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="21122-191">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="21122-191">**Quantity:** *1.00*</span></span>

### <a name="create-order-set-6"></a><span data-ttu-id="21122-192">Búa til pöntunarsett 6</span><span class="sxs-lookup"><span data-stu-id="21122-192">Create order set 6</span></span>

#### <a name="sales-orders-6-1-and-6-2"></a><span data-ttu-id="21122-193">Sölupantanir 6-1 og 6-2</span><span class="sxs-lookup"><span data-stu-id="21122-193">Sales orders 6-1 and 6-2</span></span>

1. <span data-ttu-id="21122-194">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-194">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="21122-195">**Viðskiptavinalykill:** *US-003*</span><span class="sxs-lookup"><span data-stu-id="21122-195">**Customer account:** *US-003*</span></span>
    - <span data-ttu-id="21122-196">**Innkaupabeiðni viðskiptavinar:** *2*</span><span class="sxs-lookup"><span data-stu-id="21122-196">**Customer requisition:** *2*</span></span>

1. <span data-ttu-id="21122-197">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-197">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="21122-198">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="21122-198">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="21122-199">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="21122-199">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-3-and-6-4"></a><span data-ttu-id="21122-200">Sölupantanir 6-3 og 6-4</span><span class="sxs-lookup"><span data-stu-id="21122-200">Sales orders 6-3 and 6-4</span></span>

1. <span data-ttu-id="21122-201">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-201">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="21122-202">**Viðskiptavinalykill:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="21122-202">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="21122-203">**Innkaupabeiðni viðskiptavinar:** *1*</span><span class="sxs-lookup"><span data-stu-id="21122-203">**Customer requisition:** *1*</span></span>

1. <span data-ttu-id="21122-204">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-204">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="21122-205">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="21122-205">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="21122-206">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="21122-206">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-5-and-6-6"></a><span data-ttu-id="21122-207">Sölupantanir 6-5 og 6-6</span><span class="sxs-lookup"><span data-stu-id="21122-207">Sales orders 6-5 and 6-6</span></span>

1. <span data-ttu-id="21122-208">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-208">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="21122-209">**Viðskiptavinalykill:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="21122-209">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="21122-210">**Svæði:** *6*</span><span class="sxs-lookup"><span data-stu-id="21122-210">**Site:** *6*</span></span>
    - <span data-ttu-id="21122-211">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="21122-211">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="21122-212">**Hópur:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="21122-212">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="21122-213">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-213">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="21122-214">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="21122-214">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="21122-215">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="21122-215">**Quantity:** *1.00*</span></span>

#### <a name="sales-orders-6-7-and-6-8"></a><span data-ttu-id="21122-216">Sölupantanir 6-7 og 6-8</span><span class="sxs-lookup"><span data-stu-id="21122-216">Sales orders 6-7 and 6-8</span></span>

1. <span data-ttu-id="21122-217">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-217">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="21122-218">**Viðskiptavinalykill:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="21122-218">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="21122-219">**Svæði:** *6*</span><span class="sxs-lookup"><span data-stu-id="21122-219">**Site:** *6*</span></span>
    - <span data-ttu-id="21122-220">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="21122-220">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="21122-221">**Hópur:** – Hafa þennan reit auðan.</span><span class="sxs-lookup"><span data-stu-id="21122-221">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="21122-222">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="21122-222">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="21122-223">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="21122-223">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="21122-224">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="21122-224">**Quantity:** *1.00*</span></span>

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a><span data-ttu-id="21122-225">Sjálfvirk losun á sölupöntunum í vöruhúsið</span><span class="sxs-lookup"><span data-stu-id="21122-225">Automatic release of sales orders to the warehouse</span></span>

<span data-ttu-id="21122-226">Fyrir hvert safn af sölupöntunum sem voru stofnaðar áður skal ljúka ferli fyrir sjálfvirka losun í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="21122-226">For each set of sales orders that you created earlier, you will complete a procedure for automatic release to the warehouse.</span></span> <span data-ttu-id="21122-227">Í hverju tilviki verður unnið í gegnum [grunnlosunarferli í vöruhús](#release-procedure) sem er gefið upp hér.</span><span class="sxs-lookup"><span data-stu-id="21122-227">In each case, you will work through the [basic release-to-warehouse procedure](#release-procedure) that is provided here.</span></span>

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a><span data-ttu-id="21122-228">Grunnlosunarferli í vöruhús</span><span class="sxs-lookup"><span data-stu-id="21122-228">Basic release-to-warehouse procedure</span></span>

<span data-ttu-id="21122-229">Fyrir hvert safn af sölupöntunum sem voru stofnuð áður skal ljúka við ferlin þrjú sem er sagt frá í eftirfarandi undirköflum.</span><span class="sxs-lookup"><span data-stu-id="21122-229">For each set of sales orders that you created earlier, you will complete the three procedures that are outlined in the following subsections.</span></span>

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a><span data-ttu-id="21122-230">Uppfæra bylgjusniðmátið sem verður notað við losun</span><span class="sxs-lookup"><span data-stu-id="21122-230">Update the wave template that will be used during release</span></span>

1. <span data-ttu-id="21122-231">Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="21122-231">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="21122-232">Stillið svæðið **gerð bylgjusniðmáts** á *afhendingu*.</span><span class="sxs-lookup"><span data-stu-id="21122-232">Set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="21122-233">Finnið og veljið bylgjusniðmátið sem tengist vöruhúsinu sem var notað í pöntunarsettunum sem voru stofnuð fyrir þessa atburðarás.</span><span class="sxs-lookup"><span data-stu-id="21122-233">Find and select the wave template that is associated with the warehouse that you used in the order sets that you created for this scenario.</span></span> <span data-ttu-id="21122-234">Til dæmis, ef notað er vöruhús *24*, skal velja bylgjusniðmátið **sjálfgefin afhending 24**.</span><span class="sxs-lookup"><span data-stu-id="21122-234">For example, if you used warehouse *24*, select the **24 Shipping Default** wave template.</span></span> <span data-ttu-id="21122-235">Ef notað var vöruhús *61* skal velja bylgjusniðmátið **afhending 61.**</span><span class="sxs-lookup"><span data-stu-id="21122-235">If you used warehouse *61*, select the **61 Shipping** wave template.</span></span>
1. <span data-ttu-id="21122-236">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="21122-236">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="21122-237">Stilla valkostinn fyrir **Vinna úr bylgju við losun í vörugeymslu** á *Nei*.</span><span class="sxs-lookup"><span data-stu-id="21122-237">Set the **Process wave at release to warehouse** option to *No*.</span></span>

#### <a name="release-to-the-warehouse"></a><span data-ttu-id="21122-238">Losa í vöruhús</span><span class="sxs-lookup"><span data-stu-id="21122-238">Release to the warehouse</span></span>

1. <span data-ttu-id="21122-239">Farið í **Vöruhúsakerfi \> Losa í vöruhús \> Sjálfvirk losun sölupantana**.</span><span class="sxs-lookup"><span data-stu-id="21122-239">Go to **Warehouse management \> Release to warehouse \> Automatic release of sales orders**.</span></span>
1. <span data-ttu-id="21122-240">Stillið svæðið **Magn til að losa** á *Allt*.</span><span class="sxs-lookup"><span data-stu-id="21122-240">Set the **Quantity to release** field to *All*.</span></span>
1. <span data-ttu-id="21122-241">Á flýtiflipanum **Færslur til að taka með** skal velja **Sía** til að opna svargluggann „fyrirspurn“.</span><span class="sxs-lookup"><span data-stu-id="21122-241">On the **Records to include** FastTab, select **Filter** to open the query dialog box.</span></span>
1. <span data-ttu-id="21122-242">Veldu **Bæta við** til að bæta við röð á flipanum **Svið** til að bæta við línu sem er með eftirfarandi stillingar á hnitanetinu:</span><span class="sxs-lookup"><span data-stu-id="21122-242">On the **Range** tab, select **Add** to add a row that has the following settings to the grid:</span></span>

    - <span data-ttu-id="21122-243">**tafla:** *Sölupöntun*</span><span class="sxs-lookup"><span data-stu-id="21122-243">**Table:** *Sales order*</span></span>
    - <span data-ttu-id="21122-244">**Afleidd tafla:** *Sölupöntun*</span><span class="sxs-lookup"><span data-stu-id="21122-244">**Derived table:** *Sales order*</span></span>
    - <span data-ttu-id="21122-245">**Svæði:** *Sölupöntun*</span><span class="sxs-lookup"><span data-stu-id="21122-245">**Field:** *Sales order*</span></span>
    - <span data-ttu-id="21122-246">**Skilyrði:** Færa skal inn kommuaðgreinda lista yfir sölupöntunarnúmer úr æskilegu pantanamengi.</span><span class="sxs-lookup"><span data-stu-id="21122-246">**Criteria:** Enter a comma-separated list of the sales order numbers from the desired order set.</span></span>

1. <span data-ttu-id="21122-247">Veljið **Í lagi** til að vista fyrirspurnina.</span><span class="sxs-lookup"><span data-stu-id="21122-247">Select **OK** to save your query.</span></span>
1. <span data-ttu-id="21122-248">Veljið **Í lagi** til að ræsa ferlið *Sjálfvirk losun í vöruhús*.</span><span class="sxs-lookup"><span data-stu-id="21122-248">Select **OK** to start the *Automatic release to warehouse* procedure.</span></span>

#### <a name="review-the-shipment-that-is-created-or-updated"></a><span data-ttu-id="21122-249">Yfirfara sendinguna sem er búin til eða uppfærð</span><span class="sxs-lookup"><span data-stu-id="21122-249">Review the shipment that is created or updated</span></span>

1. <span data-ttu-id="21122-250">Opnið **Vöruhúsakerfi \> Sendingar \> Allar sendingar**.</span><span class="sxs-lookup"><span data-stu-id="21122-250">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="21122-251">Finnið og veljið þá sendingu sem um ræðir.</span><span class="sxs-lookup"><span data-stu-id="21122-251">Find and select the required shipment.</span></span>
1. <span data-ttu-id="21122-252">Ef samstæðuregla var notuð þegar sendingin var stofnuð eða hún var uppfærð ætti hún að koma fram í reitnum **Samstæðuregla sendingar**.</span><span class="sxs-lookup"><span data-stu-id="21122-252">If a consolidation policy was used when the shipment was created or updated, you should see it in the **Shipment consolidation policy** field.</span></span>

### <a name="release-sales-orders-from-order-set-1"></a><span data-ttu-id="21122-253">Losa sölupantanir úr pöntunarsetti 1</span><span class="sxs-lookup"><span data-stu-id="21122-253">Release sales orders from order set 1</span></span>

<span data-ttu-id="21122-254">Farið eftir [Grunnlosunarferli í vöruhús](#release-procedure) til að losa sölupantanir úr pantanasetti 1.</span><span class="sxs-lookup"><span data-stu-id="21122-254">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 1.</span></span>

<span data-ttu-id="21122-255">Þegar því er lokið ættirðu að sjá að tvær sendingar voru búnar til:</span><span class="sxs-lookup"><span data-stu-id="21122-255">When you've finished, you should see that two shipments were created:</span></span>

- <span data-ttu-id="21122-256">Fyrsta sendingin inniheldur þrjár línur og var búin til með því að nota samstæðureglu sendingar *CustomerMode*.</span><span class="sxs-lookup"><span data-stu-id="21122-256">The first shipment contains three lines and was created by using the *CustomerMode* shipment consolidation policy.</span></span>
- <span data-ttu-id="21122-257">Önnur sendingin, sem notar ekki flutningsmátann *Flugfélög*, var stofnuð með því að nota samstæðureglu sendingar *CustomerOrderNo*.</span><span class="sxs-lookup"><span data-stu-id="21122-257">The second shipment, which doesn't use the *Airways* transportation mode of delivery, was created by using the *CustomerOrderNo* shipment consolidation policy.</span></span>

### <a name="release-sales-orders-from-order-set-2"></a><span data-ttu-id="21122-258">Losa sölupantanir úr pöntunarsetti 2</span><span class="sxs-lookup"><span data-stu-id="21122-258">Release sales orders from order set 2</span></span>

<span data-ttu-id="21122-259">Farið eftir [Grunnlosunarferli í vöruhús](#release-procedure) til að losa sölupantanir úr pantanasetti 2.</span><span class="sxs-lookup"><span data-stu-id="21122-259">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 2.</span></span>

<span data-ttu-id="21122-260">Þegar því er lokið ættirðu að sjá að þrjár sendingar voru búnar til:</span><span class="sxs-lookup"><span data-stu-id="21122-260">When you've finished, you should see that three shipments were created:</span></span>

- <span data-ttu-id="21122-261">Fyrsta sendingin inniheldur vörur sem eru *eldfimar*.</span><span class="sxs-lookup"><span data-stu-id="21122-261">The first shipment contains *Flammable* items.</span></span>
- <span data-ttu-id="21122-262">Hvor hinna sendinganna tveggja inniheldur eina línu með vöru sem er *sprengifim*.</span><span class="sxs-lookup"><span data-stu-id="21122-262">Each of the other two shipments contains one line that has the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-3"></a><span data-ttu-id="21122-263">Losa sölupantanir úr pöntunarsetti 3</span><span class="sxs-lookup"><span data-stu-id="21122-263">Release sales orders from order set 3</span></span>

<span data-ttu-id="21122-264">Farið eftir [Grunnlosunarferli í vöruhús](#release-procedure) til að losa sölupantanir úr pantanasetti 3.</span><span class="sxs-lookup"><span data-stu-id="21122-264">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 3.</span></span>

<span data-ttu-id="21122-265">Þegar því er lokið ætti að koma í ljós að eftirfarandi aðgerðir áttu sér stað:</span><span class="sxs-lookup"><span data-stu-id="21122-265">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="21122-266">Ein fyrirliggjandi sending (sendingin sem var stofnuð þegar pöntunarsett 2 var losað í vöruhúsið) var uppfærð.</span><span class="sxs-lookup"><span data-stu-id="21122-266">One existing shipment (the shipment that was created when order set 2 was released to the warehouse) was updated.</span></span> <span data-ttu-id="21122-267">Línu sem er með vöru sem er *eldfim* var bætt við.</span><span class="sxs-lookup"><span data-stu-id="21122-267">A line that has the *Flammable* item was added.</span></span>
- <span data-ttu-id="21122-268">Ein ný sending var búin til sem inniheldur vöruna sem er *sprengifim*.</span><span class="sxs-lookup"><span data-stu-id="21122-268">One new shipment was created that contains the *Explosive* item.</span></span>

### <a name="release-sales-orders-from-order-set-4"></a><span data-ttu-id="21122-269">Losa sölupantanir úr pöntunarsetti 4</span><span class="sxs-lookup"><span data-stu-id="21122-269">Release sales orders from order set 4</span></span>

<span data-ttu-id="21122-270">Farið eftir [Grunnlosunarferli í vöruhús](#release-procedure) til að losa sölupantanir úr pantanasetti 4.</span><span class="sxs-lookup"><span data-stu-id="21122-270">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 4.</span></span>

<span data-ttu-id="21122-271">Þegar því er lokið ætti að koma fram að ein fyrirliggjandi sending (þar sem svæðið **Innkaupabeiðni viðskiptavinar** er stillt á *1*) var uppfærð.</span><span class="sxs-lookup"><span data-stu-id="21122-271">When you've finished, you should see that one existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="21122-272">Einni nýrri línu var bætt við hana.</span><span class="sxs-lookup"><span data-stu-id="21122-272">One new line was added to it.</span></span>

### <a name="release-sales-orders-from-order-set-5"></a><span data-ttu-id="21122-273">Losa sölupantanir úr pöntunarsetti 5</span><span class="sxs-lookup"><span data-stu-id="21122-273">Release sales orders from order set 5</span></span>

<span data-ttu-id="21122-274">Farið eftir [Grunnlosunarferli í vöruhús](#release-procedure) til að losa sölupantanir úr pantanasetti 5.</span><span class="sxs-lookup"><span data-stu-id="21122-274">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 5.</span></span>

<span data-ttu-id="21122-275">Þegar því er lokið ætti að koma í ljós að eftirfarandi aðgerðir áttu sér stað:</span><span class="sxs-lookup"><span data-stu-id="21122-275">When you've finished, you should see that the following actions occurred:</span></span>

- <span data-ttu-id="21122-276">Ein fyrirliggjandi sending (þar sem svæðið **Innkaupabeiðni viðskiptavinar** er stillt á *1*) var uppfærð.</span><span class="sxs-lookup"><span data-stu-id="21122-276">One existing shipment (where the **Customer requisition** field is set to *1*) was updated.</span></span> <span data-ttu-id="21122-277">Línu úr sölupöntun 5-3 (þar sem reiturinn **Innkaupabeiðni viðskiptavinar** er stilltur á *1*) var bætt við hana.</span><span class="sxs-lookup"><span data-stu-id="21122-277">A line from sales order 5-3 (where the **Customer requisition** field is set to *1*) was added to it.</span></span>
- <span data-ttu-id="21122-278">Ein ný sending var stofnuð, þar sem línur úr sölupöntunum 5-1 og 5-2 eru flokkaðar í eina sendingu.</span><span class="sxs-lookup"><span data-stu-id="21122-278">One new shipment was created, where lines from sales orders 5-1 and 5-2 are grouped into one shipment.</span></span>

### <a name="release-sales-orders-from-order-set-6"></a><span data-ttu-id="21122-279">Losa sölupantanir úr pöntunarsetti 6</span><span class="sxs-lookup"><span data-stu-id="21122-279">Release sales orders from order set 6</span></span>

<span data-ttu-id="21122-280">Farið eftir [Grunnlosunarferli í vöruhús](#release-procedure) til að losa sölupantanir úr pantanasetti 6.</span><span class="sxs-lookup"><span data-stu-id="21122-280">Follow the [basic release-to-warehouse procedure](#release-procedure) to release the sales orders from order set 6.</span></span>

<span data-ttu-id="21122-281">Þegar því er lokið ættirðu að sjá að fjórar sendingar voru búnar til:</span><span class="sxs-lookup"><span data-stu-id="21122-281">When you've finished, you should see that four shipments were created:</span></span>

- <span data-ttu-id="21122-282">Línur úr tveimur pöntunum fyrir viðskiptavin *US-003* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.</span><span class="sxs-lookup"><span data-stu-id="21122-282">Lines from two orders for customer *US-003* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="21122-283">Línur úr tveimur pöntunum fyrir viðskiptavin *US-004* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.</span><span class="sxs-lookup"><span data-stu-id="21122-283">Lines from two orders for customer *US-004* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="21122-284">Línur úr sölupöntun 6-5 og 6-6 fyrir viðskiptavin *US-007* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.</span><span class="sxs-lookup"><span data-stu-id="21122-284">Lines from sales orders 6-5 and 6-6 for customer *US-007* were grouped into one shipment by using the *Order pool* shipment consolidation policy.</span></span>
- <span data-ttu-id="21122-285">Línur úr sölupöntun 6-7 og 6-8 fyrir viðskiptavin *US-007* voru settar saman í sendingu með því að nota *CrossOrder* úr samstæðureglu sendingar.</span><span class="sxs-lookup"><span data-stu-id="21122-285">Lines from sales orders 6-7 and 6-8 for customer *US-007* were grouped into one shipment by using the *CrossOrder* shipment consolidation policy.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="21122-286">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="21122-286">Additional resources</span></span>

- [<span data-ttu-id="21122-287">Samstæðureglur sendingar</span><span class="sxs-lookup"><span data-stu-id="21122-287">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="21122-288">Skilgreina samstæðureglur sendingar</span><span class="sxs-lookup"><span data-stu-id="21122-288">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]