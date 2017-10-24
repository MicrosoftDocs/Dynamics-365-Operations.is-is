---
title: "Kostnaðarfærslur"
description: "Þessi grein veitir upplýsingar um kostnaðarfærslur og þegar þær eru stofnaðir. Kostnaðarfærslu er færsla sem skráir magni og kostnað á tilteknu tilviki."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19131
ms.assetid: dd2663d8-bcc0-47b1-b36d-57433143487c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a61761a5c9d98befd67682e1790af5377b7a55e1
ms.openlocfilehash: 38fedcb2f482296b1c88dda98d34dd8b7debf555
ms.contentlocale: is-is
ms.lasthandoff: 10/13/2017

---

# <a name="cost-entries"></a><span data-ttu-id="1c2eb-104">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="1c2eb-104">Cost entries</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1c2eb-105">Þessi grein veitir upplýsingar um kostnaðarfærslur og þegar þær eru stofnaðir.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-105">This article provides information about cost entries and when they are created.</span></span> <span data-ttu-id="1c2eb-106">Kostnaðarfærslu er færsla sem skráir magni og kostnað á tilteknu tilviki.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-106">A cost entry is a record that registers the quantity and cost of a given event.</span></span>

<span data-ttu-id="1c2eb-107">Kostnaðarfærslur eru uppsöfnun birgðafærslna sem eru skráðar á virkar fjárhagslegar birgðavíddir.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-107">Cost entries are aggregations of inventory transactions that are recorded on active financial inventory dimensions.</span></span>

## <a name="examples"></a><span data-ttu-id="1c2eb-108">Dæmi</span><span class="sxs-lookup"><span data-stu-id="1c2eb-108">Examples</span></span>
### <a name="example-1-no-cost-entries-are-created"></a><span data-ttu-id="1c2eb-109">Dæmi 1: Engin kostnaðarfærslur eru stofnaðar</span><span class="sxs-lookup"><span data-stu-id="1c2eb-109">Example 1: No cost entries are created</span></span>

<span data-ttu-id="1c2eb-110">Tilvik flutnings færslubókar er skráð.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-110">A transfer journal event is registered.</span></span> <span data-ttu-id="1c2eb-111">Tilvikið flytur eitt stykki af vöru A frá staðsetningu A til staðsetningar B. birgðavídd Staðsetningar er ekki talin hluti af kostnaðarhlut.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-111">The event transfers one piece of item A from location A to location B. The Location inventory dimension isn't considered part of the cost object.</span></span> <span data-ttu-id="1c2eb-112">Þess vegna stofnar tilvikið engar kostnaðarfærslur og tvær birgðafærslur.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-112">Therefore, the event creates two inventory transactions and no cost entries.</span></span>

### <a name="example-2-cost-entries-are-created"></a><span data-ttu-id="1c2eb-113">Dæmi 2: kostnaðarfærslur eru stofnaðar</span><span class="sxs-lookup"><span data-stu-id="1c2eb-113">Example 2: Cost entries are created</span></span>

<span data-ttu-id="1c2eb-114">Tilvik flutnings færslubókar er skráð.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-114">A transfer journal event is registered.</span></span> <span data-ttu-id="1c2eb-115">Tilvikið flytur eitt stykki af vöru A frá staðsetningu 1 til staðsetningar 2.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-115">The event transfers one piece of item A from site 1 to site 2.</span></span> <span data-ttu-id="1c2eb-116">Birgðavídd Staðsetningar er talin hluti af hluti af kostnaðarhlut.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-116">The Site inventory dimension is considered part of the cost object.</span></span> <span data-ttu-id="1c2eb-117">Þess vegna stofnar tilvikið tvær kostnaðarfærslur og tvær birgðafærslur.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-117">Therefore, the event creates two inventory transactions and two cost entries.</span></span>

### <a name="example-3-one-cost-entry-is-created"></a><span data-ttu-id="1c2eb-118">Dæmi 3: ein kostnaðarfærsla er stofnaðar</span><span class="sxs-lookup"><span data-stu-id="1c2eb-118">Example 3: One cost entry is created</span></span>

<span data-ttu-id="1c2eb-119">Tilvik innhreyfingarskjals afurðar er skráð fyrir innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-119">A product receipt event is registered for a purchase order.</span></span> <span data-ttu-id="1c2eb-120">Tilvikið skráir 100 stykki af vöru A á einingarkostnaði uppá 10,00 bandarískum dollurum (USD).</span><span class="sxs-lookup"><span data-stu-id="1c2eb-120">The event registers 100 pieces of item A at a unit cost of 10.00 U.S. dollars (USD).</span></span> <span data-ttu-id="1c2eb-121">Þar sem vöru A notar raðnúmer til að rekja málefni birgðastjórnunar, er stofnað einkvæmt raðnúmer fyrir hverja vöru sem er móttekin.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-121">Because item A uses a serial number to track the purpose of inventory management, a unique serial number is created for each item that is received.</span></span> <span data-ttu-id="1c2eb-122">Þess vegna stofnar tilvikið 100 birgðafærslur og eina kostnaðarfærslu.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-122">Therefore, the event creates 100 inventory transactions and one cost entry.</span></span>

## <a name="cost-entries-page"></a><span data-ttu-id="1c2eb-123">Kostnaðarfærslusíður</span><span class="sxs-lookup"><span data-stu-id="1c2eb-123">Cost entries page</span></span>
<span data-ttu-id="1c2eb-124">Nýja **Kostnaðarfærslu** síðu gerir kleift að skoða og stýra skráningar á kostnaði og magni.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-124">The new **Cost entries** page lets you view and control registrations of quantities and costs.</span></span> <span data-ttu-id="1c2eb-125">Þessi síða er viðbót við **Birgðafærslu** og **Birgðajöfnunar** síður.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-125">This page complements the **Inventory transaction** and **Inventory settlement** pages.</span></span> <span data-ttu-id="1c2eb-126">Færslur eru skráðar í tímaröð fyrir tilvik.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-126">Records are registered in chronological order for an event.</span></span> <span data-ttu-id="1c2eb-127">Þess vegna er hægt að finna og stjórna uppsafnaðan kostnað á skjótan hátt fyrir ákveðinn viðburð eða öll atvik sem eru tengdar við skjal.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-127">Therefore, you can quickly find and control the accumulated costs of a specific event or all events that are related to a document.</span></span> <span data-ttu-id="1c2eb-128">Eftirfarandi er dæmi:</span><span class="sxs-lookup"><span data-stu-id="1c2eb-128">Here is an example:</span></span>

-   <span data-ttu-id="1c2eb-129">Tilvik innhreyfingarskjals afurðar er skráð fyrir vöru A. Hundrað stykki eru mótteknar með einingarkostnað 10,00 usd.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-129">A product receipt event is registered for item A. One hundred pieces are received at a unit cost of 10.00 USD.</span></span>
-   <span data-ttu-id="1c2eb-130">Nokkrar dögum eftir að reikningstilvikið er skráð, eykst kostnaður í USD 11.00.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-130">A few days after the invoice event is registered, the cost increases to 11.00 USD.</span></span> <span data-ttu-id="1c2eb-131">Þess vegna er heildarupphæðin 1.100.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-131">Therefore, the total amount is 1,100 USD.</span></span> <span data-ttu-id="1c2eb-132">Önnur fylgiskjal er stofnuð til að útskýra mismuninn uppá 100 usd.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-132">A second voucher is created to account for the difference of 100 USD.</span></span>
-   <span data-ttu-id="1c2eb-133">Nokkrar dögum síðar er óflokkað gjald upp á USD 15.00 til að ná yfir flutningskostnað er skráður á innkaupapöntuninni.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-133">A few days later, a miscellaneous charge of 15.00 USD to cover the transportation cost is registered on the purchase order.</span></span>

| <span data-ttu-id="1c2eb-134">Fylgiskjal</span><span class="sxs-lookup"><span data-stu-id="1c2eb-134">Voucher</span></span> | <span data-ttu-id="1c2eb-135">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="1c2eb-135">Date</span></span>       | <span data-ttu-id="1c2eb-136">Tilvísun</span><span class="sxs-lookup"><span data-stu-id="1c2eb-136">Reference</span></span>      | <span data-ttu-id="1c2eb-137">Númer</span><span class="sxs-lookup"><span data-stu-id="1c2eb-137">Number</span></span> | <span data-ttu-id="1c2eb-138">Lotukenni</span><span class="sxs-lookup"><span data-stu-id="1c2eb-138">Lot ID</span></span>  | <span data-ttu-id="1c2eb-139">Magn</span><span class="sxs-lookup"><span data-stu-id="1c2eb-139">Quantity</span></span> | <span data-ttu-id="1c2eb-140">Upphæð</span><span class="sxs-lookup"><span data-stu-id="1c2eb-140">Amount</span></span>  |
|---------|------------|----------------|--------|---------|---------------|----|
| <span data-ttu-id="1c2eb-141">00001</span><span class="sxs-lookup"><span data-stu-id="1c2eb-141">00001</span></span>   | <span data-ttu-id="1c2eb-142">01/01/2015</span><span class="sxs-lookup"><span data-stu-id="1c2eb-142">01-01-2015</span></span> | <span data-ttu-id="1c2eb-143">Innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="1c2eb-143">Purchase order</span></span> | <span data-ttu-id="1c2eb-144">100001</span><span class="sxs-lookup"><span data-stu-id="1c2eb-144">100001</span></span> | <span data-ttu-id="1c2eb-145">0000101</span><span class="sxs-lookup"><span data-stu-id="1c2eb-145">0000101</span></span> | <span data-ttu-id="1c2eb-146">100,00</span><span class="sxs-lookup"><span data-stu-id="1c2eb-146">100.00</span></span>   | <span data-ttu-id="1c2eb-147">1000,00</span><span class="sxs-lookup"><span data-stu-id="1c2eb-147">1000.00</span></span> |
| <span data-ttu-id="1c2eb-148">00002</span><span class="sxs-lookup"><span data-stu-id="1c2eb-148">00002</span></span>   | <span data-ttu-id="1c2eb-149">20/01/2015</span><span class="sxs-lookup"><span data-stu-id="1c2eb-149">20-01-2015</span></span> | <span data-ttu-id="1c2eb-150">Innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="1c2eb-150">Purchase order</span></span> | <span data-ttu-id="1c2eb-151">100001</span><span class="sxs-lookup"><span data-stu-id="1c2eb-151">100001</span></span> | <span data-ttu-id="1c2eb-152">0000101</span><span class="sxs-lookup"><span data-stu-id="1c2eb-152">0000101</span></span> |          | <span data-ttu-id="1c2eb-153">100,00</span><span class="sxs-lookup"><span data-stu-id="1c2eb-153">100.00</span></span>  |
| <span data-ttu-id="1c2eb-154">00003</span><span class="sxs-lookup"><span data-stu-id="1c2eb-154">00003</span></span>   | <span data-ttu-id="1c2eb-155">31-01-2015</span><span class="sxs-lookup"><span data-stu-id="1c2eb-155">31-01-2015</span></span> | <span data-ttu-id="1c2eb-156">Leiðrétting</span><span class="sxs-lookup"><span data-stu-id="1c2eb-156">Adjustment</span></span>     | <span data-ttu-id="1c2eb-157">100001</span><span class="sxs-lookup"><span data-stu-id="1c2eb-157">100001</span></span> | <span data-ttu-id="1c2eb-158">0000101</span><span class="sxs-lookup"><span data-stu-id="1c2eb-158">0000101</span></span> |          | <span data-ttu-id="1c2eb-159">15:00</span><span class="sxs-lookup"><span data-stu-id="1c2eb-159">15.00</span></span>   |

<span data-ttu-id="1c2eb-160">**Kostnaðarfærslur** síðu gerir kleift að sía eftir Skjalakenni og dagsetningu skjals.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-160">The **Cost entries** page enables filtering by document ID and document date.</span></span> 

> [!NOTE]
> <span data-ttu-id="1c2eb-161">Kostnaðarfærslur eru aðeins tiltækar fyrir [kostnaðarhluti](cost-object.md) eða útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="1c2eb-161">Cost entries are available only for [cost objects](cost-object.md) or released products.</span></span>

<a name="see-also"></a><span data-ttu-id="1c2eb-162">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="1c2eb-162">See also</span></span>
--------

[<span data-ttu-id="1c2eb-163">Kostnaðarhlutir</span><span class="sxs-lookup"><span data-stu-id="1c2eb-163">Cost objects</span></span>](cost-object.md)




