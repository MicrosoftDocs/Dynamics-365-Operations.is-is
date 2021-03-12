---
title: Sameina sendingar handvirkt með því að nota síðuna „Sameina sendingar“
description: Þetta efnisatriði sýnir aðstæður þar sem margar pantanir eru losaðar í vöruhúsið og sameinaðar seinna með því að nota síðuna „Sameina sendingar“.
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
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 0e580253de0d787b721c2f729ecc96db56b91af0
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983016"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a><span data-ttu-id="39fbf-103">Sameina sendingar handvirkt með því að nota síðuna „Sameina sendingar“</span><span class="sxs-lookup"><span data-stu-id="39fbf-103">Consolidate shipments manually by using the Consolidate shipments page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="39fbf-104">Þetta efnisatriði sýnir aðstæður þar sem margar pantanir eru losaðar í vöruhúsið og sameinaðar seinna með því að nota síðuna **Sameina sendingar**.</span><span class="sxs-lookup"><span data-stu-id="39fbf-104">This topic presents a scenario where multiple orders are released to the warehouse and then consolidated later by using the **Consolidate shipments** page.</span></span>

## <a name="make-demo-data-available"></a><span data-ttu-id="39fbf-105">Bjóða upp á sýnigögn</span><span class="sxs-lookup"><span data-stu-id="39fbf-105">Make demo data available</span></span>

<span data-ttu-id="39fbf-106">Aðstæður í þessu efnisatriði vísa í gildi og færslur sem eru innifaldar í stöðluðum sýnigögnum fyrir Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="39fbf-106">The scenario in this topic references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="39fbf-107">Ef nota á gildin sem er boðið upp á hér eins og í æfingunum skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett og stilla lögaðilann á **USMF** áður en hafist er handa.</span><span class="sxs-lookup"><span data-stu-id="39fbf-107">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a><span data-ttu-id="39fbf-108">Setja upp samstæðureglur sendingar og afurðarsíur</span><span class="sxs-lookup"><span data-stu-id="39fbf-108">Set up shipment consolidation policies and product filters</span></span>

<span data-ttu-id="39fbf-109">Aðstæðurnar sem hér er lýst gera ráð fyrir að þegar hafi verið kveikt á eiginleikanum, farið hafi verið í gegnum æfingarnar í [Skilgreina samstæðureglur sendingar](configure-shipment-consolidation-policies.md) og reglur og aðrar færslur sem þar er lýst stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="39fbf-109">The scenario that is described here assumes that you've already turned on the feature, done the exercises in [Configure shipment consolidation policies](configure-shipment-consolidation-policies.md), and created the policies and other records that are described there.</span></span> <span data-ttu-id="39fbf-110">Gætið þess að gera þessar æfingar áður en haldið er áfram með þessar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="39fbf-110">Be sure to do those exercises before you continue with this scenario.</span></span>

## <a name="create-the-sales-orders-for-this-scenario"></a><span data-ttu-id="39fbf-111">Búa til sölupantanir fyrir þessar aðstæður</span><span class="sxs-lookup"><span data-stu-id="39fbf-111">Create the sales orders for this scenario</span></span>

<span data-ttu-id="39fbf-112">Byrjaðu á því að stofna safn af sölupöntunum sem hægt er að vinna með.</span><span class="sxs-lookup"><span data-stu-id="39fbf-112">Start by creating a collection of sales orders that you can work with.</span></span> <span data-ttu-id="39fbf-113">Vinna verður með vöruhús sem er virkt fyrir ítarlegt ferli vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="39fbf-113">You must work with a warehouse that is enabled for advanced warehouse (WMS) processes.</span></span> <span data-ttu-id="39fbf-114">Nema annað vöruhús er tilgreint með skýrum hætti verður að nota sama vöruhúsið fyrir hvert eftirtalinna pöntunarsetta.</span><span class="sxs-lookup"><span data-stu-id="39fbf-114">Unless a different warehouse is explicitly mentioned, that same warehouse must be used for each of the following sets of orders.</span></span>

<span data-ttu-id="39fbf-115">Opnaðu **Viðskiptakröfur \> Pantanir \> Allar sölupantanir** og búðu til safn sölupantana sem eru með stillingarnar sem lýst er í eftirfarandi undirhlutum.</span><span class="sxs-lookup"><span data-stu-id="39fbf-115">Go to **Accounts receivable \> Orders \> All sales orders**, and create a collection of sales orders that have the settings that are described in the following subsections.</span></span>

### <a name="create-sales-orders-1-and-2"></a><span data-ttu-id="39fbf-116">Búa til sölupöntun 1 og 2</span><span class="sxs-lookup"><span data-stu-id="39fbf-116">Create sales orders 1 and 2</span></span>

1. <span data-ttu-id="39fbf-117">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="39fbf-117">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="39fbf-118">**Viðskiptavinalykill:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="39fbf-118">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="39fbf-119">**Hópur:** *ShipCons*</span><span class="sxs-lookup"><span data-stu-id="39fbf-119">**Pool:** *ShipCons*</span></span>

1. <span data-ttu-id="39fbf-120">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="39fbf-120">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="39fbf-121">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="39fbf-121">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="39fbf-122">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="39fbf-122">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="39fbf-123">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="39fbf-123">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

### <a name="create-sales-orders-3-and-4"></a><span data-ttu-id="39fbf-124">Búa til sölupöntun 3 og 4</span><span class="sxs-lookup"><span data-stu-id="39fbf-124">Create sales orders 3 and 4</span></span>

1. <span data-ttu-id="39fbf-125">Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="39fbf-125">Create two identical sales orders that have the following settings:</span></span>

    - <span data-ttu-id="39fbf-126">**Viðskiptavinalykill:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="39fbf-126">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="39fbf-127">**Hópur:** – Hafa þennan reit auðan.</span><span class="sxs-lookup"><span data-stu-id="39fbf-127">**Pool:** Leave this field blank.</span></span>

1. <span data-ttu-id="39fbf-128">Bættu við pöntunarlínu sem er með eftirfarandi stillingar:</span><span class="sxs-lookup"><span data-stu-id="39fbf-128">Add an order line that has the following settings:</span></span>

    - <span data-ttu-id="39fbf-129">**Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)</span><span class="sxs-lookup"><span data-stu-id="39fbf-129">**Item number:** *A0001* (an item that no **Code 4** filter is assigned to)</span></span>
    - <span data-ttu-id="39fbf-130">**Magn:** *1.00*</span><span class="sxs-lookup"><span data-stu-id="39fbf-130">**Quantity:** *1.00*</span></span>

1. <span data-ttu-id="39fbf-131">Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="39fbf-131">Select **Inventory \> Reservation**, and then, on the Action Pane, select **Reserve lot** to reserve the order line.</span></span>

## <a name="release-the-orders-to-the-warehouse"></a><span data-ttu-id="39fbf-132">Losa pantanirnar í vöruhúsið</span><span class="sxs-lookup"><span data-stu-id="39fbf-132">Release the orders to the warehouse</span></span>

<span data-ttu-id="39fbf-133">Fylgdu þessum skrefum til að losa hverja sölupöntun sem þú bjóst til fyrir þessar aðstæður í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="39fbf-133">Follow these steps to release each sales order that you created for this scenario to the warehouse.</span></span>

1. <span data-ttu-id="39fbf-134">Opna **Viðskiptakröfur \> Pantanir \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="39fbf-134">Go to **Accounts receivable \> Orders \> All sales orders**.</span></span>
1. <span data-ttu-id="39fbf-135">Finnið og veljið sölupöntun sem á að losa.</span><span class="sxs-lookup"><span data-stu-id="39fbf-135">Find and select the sales order to release.</span></span>
1. <span data-ttu-id="39fbf-136">Á aðgerðasvæðinu, á flipanum **Vöruhús**, skal velja **Aðgerðir \> Losa í vöruhús** til að losa valda sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="39fbf-136">On the Action Pane, on the **Warehouse** tab, select **Actions \> Release to warehouse** to release the selected sales order.</span></span>
1. <span data-ttu-id="39fbf-137">Endurtakið þetta ferli fyrir hverja sölupöntun sem var stofnuð fyrir þessar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="39fbf-137">Repeat this procedure for every other sales order that you created for this scenario.</span></span>

## <a name="consolidate-shipments"></a><span data-ttu-id="39fbf-138">Sameina sendingar</span><span class="sxs-lookup"><span data-stu-id="39fbf-138">Consolidate shipments</span></span>

1. <span data-ttu-id="39fbf-139">Opnið **Vöruhúsakerfi \> Sendingar \> Allar sendingar**.</span><span class="sxs-lookup"><span data-stu-id="39fbf-139">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="39fbf-140">Finnið og veljið sendingu sem var stofnuð þegar sölupöntun 1 var losuð í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="39fbf-140">Find and select a shipment that was created when sales order 1 was released to the warehouse.</span></span> <span data-ttu-id="39fbf-141">(Reiturinn **Samstæðuregla sendingar** ætti að vera stilltur á *Pöntunarhópur*.)</span><span class="sxs-lookup"><span data-stu-id="39fbf-141">(Its **Shipment consolidation policy** field should be set to *Order pool*.)</span></span>
1. <span data-ttu-id="39fbf-142">Á aðgerðasvæðinu, á flipanum **Sendingar**, skal velja **Sendingar \> Sameina sendingar**.</span><span class="sxs-lookup"><span data-stu-id="39fbf-142">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="39fbf-143">Staðfestið sendingarnar sem lagðar eru til fyrir sameiningu.</span><span class="sxs-lookup"><span data-stu-id="39fbf-143">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="39fbf-144">Aðeins ætti að mæla með einni sendingu með sömu reglu fyrir sameiningu.</span><span class="sxs-lookup"><span data-stu-id="39fbf-144">Only one shipment that has the same policy should be suggested for consolidation.</span></span>
1. <span data-ttu-id="39fbf-145">Lokið síðunni **Sendingarsamstæða**.</span><span class="sxs-lookup"><span data-stu-id="39fbf-145">Close the **Shipment consolidation** page.</span></span>
1. <span data-ttu-id="39fbf-146">Finndu og veldu sendingu sem var stofnuð þegar sölupöntun 3 var losuð í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="39fbf-146">Find and select a shipment that was created when sales order 3 was released to the warehouse.</span></span> <span data-ttu-id="39fbf-147">(Reiturinn **Samstæðuregla sendingar** ætti að vera stilltur á *Sjálfgefið*.)</span><span class="sxs-lookup"><span data-stu-id="39fbf-147">(Its **Shipment consolidation policy** field should be set to *Default*.)</span></span>
1. <span data-ttu-id="39fbf-148">Á aðgerðasvæðinu, á flipanum **Sendingar**, skal velja **Sendingar \> Sameina sendingar**.</span><span class="sxs-lookup"><span data-stu-id="39fbf-148">On the Action Pane, on the **Shipments** tab, select **Shipments \> Consolidate shipments**.</span></span>
1. <span data-ttu-id="39fbf-149">Gangið úr skugga um að engar sendingar séu ráðlagðar fyrir sameiningu.</span><span class="sxs-lookup"><span data-stu-id="39fbf-149">Verify that no shipments are suggested for consolidation.</span></span>
1. <span data-ttu-id="39fbf-150">Velja **Sýna síur**.</span><span class="sxs-lookup"><span data-stu-id="39fbf-150">Select **Show filters**.</span></span>
1. <span data-ttu-id="39fbf-151">Á svæðinu **Síur** skal fjarlægja síuna **Pöntunarnúmer** og velja **Nota**.</span><span class="sxs-lookup"><span data-stu-id="39fbf-151">In the **Filters** pane, remove the **Order number** filter, and then select **Apply**.</span></span>
1. <span data-ttu-id="39fbf-152">Staðfestið sendingarnar sem lagðar eru til fyrir sameiningu.</span><span class="sxs-lookup"><span data-stu-id="39fbf-152">Verify the shipments that are suggested for consolidation.</span></span> <span data-ttu-id="39fbf-153">Aðeins ætti að mæla með einni sendingu með sömu reglu fyrir sameiningu.</span><span class="sxs-lookup"><span data-stu-id="39fbf-153">Only one shipment that has the same policy should be suggested for consolidation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39fbf-154">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="39fbf-154">Additional resources</span></span>

- [<span data-ttu-id="39fbf-155">Samstæðureglur sendingar</span><span class="sxs-lookup"><span data-stu-id="39fbf-155">Shipment consolidation policies</span></span>](about-shipment-consolidation-policies.md)
- [<span data-ttu-id="39fbf-156">Skilgreina samstæðureglur sendingar</span><span class="sxs-lookup"><span data-stu-id="39fbf-156">Configure shipment consolidation policies</span></span>](configure-shipment-consolidation-policies.md)