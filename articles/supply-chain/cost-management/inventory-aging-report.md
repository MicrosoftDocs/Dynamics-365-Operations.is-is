---
title: Dæmi og rök fyrir aldursgreiningarskýrslu birgða
description: Í þessu efnisatriði er að finna dæmi sem sýna hvernig á að túlka niðurstöður aldursgreiningarskýrslu.
author: RichardLuan
manager: AnnBe
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6c165599c11b84e4064a9303d8b1f59558fc6b9d
ms.sourcegitcommit: 6bf8602333191e5161ba3a9ceecf160c85ff7e79
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/19/2020
ms.locfileid: "3484531"
---
# <a name="inventory-aging-report-examples-and-logic"></a><span data-ttu-id="01855-103">Dæmi og rök fyrir aldursgreiningarskýrslu birgða</span><span class="sxs-lookup"><span data-stu-id="01855-103">Inventory aging report examples and logic</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01855-104">Í þessu efnisatriði er að finna dæmi sem sýna hvernig á að túlka niðurstöður skýrslu **Aldursgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="01855-104">This topic presents some examples that show how to interpret the results of an **Inventory aging** report.</span></span> <span data-ttu-id="01855-105">Þessi skýrsla flokkar lagerbirgðir og birgðavirði fyrir valda vöru eða vöruflokk í nokkra tímaramma.</span><span class="sxs-lookup"><span data-stu-id="01855-105">This report categorizes on-hand quantity and inventory values for a selected item or item group into several period buckets.</span></span> <span data-ttu-id="01855-106">Í þessu efnisatriði eru einnig innri rök skýrslunnar sýnd.</span><span class="sxs-lookup"><span data-stu-id="01855-106">This topic also shows the internal logic of the report.</span></span>

<span data-ttu-id="01855-107">Dæmin í þessu efnisatriði sýna niðurstöður sem eru birtar í staðlaðri skýrslu **Aldursgreiningarskýrslu**.</span><span class="sxs-lookup"><span data-stu-id="01855-107">The examples in this topic show results that are presented on a standard **Inventory aging** report.</span></span> <span data-ttu-id="01855-108">Við mælum hinsvegar almennt með því að notuð sé útgáfan [Skýrsla um aldursgreiningu birgða](inventory-aging-report-storage.md) fyrir þessa skýrslu, sérstaklega þegar þarf að vinna úr mörgum vörum og vöruhúsum.</span><span class="sxs-lookup"><span data-stu-id="01855-108">However, in general, we recommend that you use the [Inventory aging report storage](inventory-aging-report-storage.md) version of this report, especially when you have many items and warehouses that must be processed.</span></span> <span data-ttu-id="01855-109">Skýrsla um aldursgreiningu birgða vistar hverja skýrslu sem búin er til, sýnir niðurstöðurnar sem gagnvirka síðu og graf, og gerir kleift að flytja út allar vistaðar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="01855-109">Inventory aging report storage saves each report that you generate, shows the results as an interactive page and a chart, and lets you export any saved report.</span></span>

## <a name="sample-data-that-is-used-in-these-examples"></a><span data-ttu-id="01855-110">Sýnidæmi sem er notað í þessum dæmum</span><span class="sxs-lookup"><span data-stu-id="01855-110">Sample data that is used in these examples</span></span>

<span data-ttu-id="01855-111">Dæmin í þessu efnisatriði byggja á dæmi um birgðafærslugögnin sem lýst er í þessum hluta.</span><span class="sxs-lookup"><span data-stu-id="01855-111">The examples in this topic are based on the sample inventory transaction data that is described in this section.</span></span>

### <a name="storage-dimension-setup"></a><span data-ttu-id="01855-112">Uppsetning geymsluvíddar</span><span class="sxs-lookup"><span data-stu-id="01855-112">Storage dimension setup</span></span>

<span data-ttu-id="01855-113">Dæmi kerfisins inniheldur eftirfarandi uppsetningu geymsluvídda.</span><span class="sxs-lookup"><span data-stu-id="01855-113">The example system contains the following setup of storage dimensions.</span></span>

| <span data-ttu-id="01855-114">Nafn</span><span class="sxs-lookup"><span data-stu-id="01855-114">Name</span></span>      | <span data-ttu-id="01855-115">Í gangi</span><span class="sxs-lookup"><span data-stu-id="01855-115">Active</span></span> | <span data-ttu-id="01855-116">Efnislegar birgðir</span><span class="sxs-lookup"><span data-stu-id="01855-116">Physical inventory</span></span> | <span data-ttu-id="01855-117">Fjárhagslegar birgðir</span><span class="sxs-lookup"><span data-stu-id="01855-117">Financial inventory</span></span> |
|-----------|--------|--------------------|---------------------|
| <span data-ttu-id="01855-118">Svæði</span><span class="sxs-lookup"><span data-stu-id="01855-118">Site</span></span>      | <span data-ttu-id="01855-119">Já</span><span class="sxs-lookup"><span data-stu-id="01855-119">Yes</span></span>    | <span data-ttu-id="01855-120">Já</span><span class="sxs-lookup"><span data-stu-id="01855-120">Yes</span></span>                | <span data-ttu-id="01855-121">Já</span><span class="sxs-lookup"><span data-stu-id="01855-121">Yes</span></span>                 |
| <span data-ttu-id="01855-122">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="01855-122">Warehouse</span></span> | <span data-ttu-id="01855-123">Já</span><span class="sxs-lookup"><span data-stu-id="01855-123">Yes</span></span>    | <span data-ttu-id="01855-124">Já</span><span class="sxs-lookup"><span data-stu-id="01855-124">Yes</span></span>                | <span data-ttu-id="01855-125">Ekkert</span><span class="sxs-lookup"><span data-stu-id="01855-125">No</span></span>                  |

### <a name="inventory-model"></a><span data-ttu-id="01855-126">Birgðalíkan</span><span class="sxs-lookup"><span data-stu-id="01855-126">Inventory model</span></span>

<span data-ttu-id="01855-127">Fyrir dæmi kerfisins er birgðalíkan útgefinna afurða *FIFO* og stillingin **Kostnaðarverð** fyrir birgðalíkanið er *Taka efnislegt virði með*.</span><span class="sxs-lookup"><span data-stu-id="01855-127">For the example system, the inventory model for the released products is *FIFO*, and the **Cost price** setting for the inventory model is *Include physical value*.</span></span>

### <a name="inventory-transactions"></a><span data-ttu-id="01855-128">Birgðafærslur</span><span class="sxs-lookup"><span data-stu-id="01855-128">Inventory transactions</span></span>

<span data-ttu-id="01855-129">Dæmi kerfisins inniheldur eftirfarandi birgðafærslur fyrir útgefna afurð sem er með vörunúmerið *1000*.</span><span class="sxs-lookup"><span data-stu-id="01855-129">The example system contains the following inventory transactions for a released product that has the item number *1000*.</span></span>

| <span data-ttu-id="01855-130">Tilvísun</span><span class="sxs-lookup"><span data-stu-id="01855-130">Reference</span></span>      | <span data-ttu-id="01855-131">Svæði</span><span class="sxs-lookup"><span data-stu-id="01855-131">Site</span></span> | <span data-ttu-id="01855-132">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="01855-132">Warehouse</span></span> | <span data-ttu-id="01855-133">Innhreyfing</span><span class="sxs-lookup"><span data-stu-id="01855-133">Receipt</span></span>   | <span data-ttu-id="01855-134">Úthreyfing</span><span class="sxs-lookup"><span data-stu-id="01855-134">Issue</span></span> | <span data-ttu-id="01855-135">Efnisleg dagsetning</span><span class="sxs-lookup"><span data-stu-id="01855-135">Physical date</span></span> | <span data-ttu-id="01855-136">Fjárhagsdagsetning</span><span class="sxs-lookup"><span data-stu-id="01855-136">Financial date</span></span> | <span data-ttu-id="01855-137">Magn</span><span class="sxs-lookup"><span data-stu-id="01855-137">Quantity</span></span> | <span data-ttu-id="01855-138">Kostnaðarupphæð</span><span class="sxs-lookup"><span data-stu-id="01855-138">Cost amount</span></span> | <span data-ttu-id="01855-139">Efnisleg kostnaðarupphæð</span><span class="sxs-lookup"><span data-stu-id="01855-139">Physical cost amount</span></span> |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| <span data-ttu-id="01855-140">Innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="01855-140">Purchase order</span></span> | <span data-ttu-id="01855-141">1</span><span class="sxs-lookup"><span data-stu-id="01855-141">1</span></span>    | <span data-ttu-id="01855-142">11</span><span class="sxs-lookup"><span data-stu-id="01855-142">11</span></span>        | <span data-ttu-id="01855-143">Innkeypt</span><span class="sxs-lookup"><span data-stu-id="01855-143">Purchased</span></span> |       | <span data-ttu-id="01855-144">15. mars</span><span class="sxs-lookup"><span data-stu-id="01855-144">March 15</span></span>      | <span data-ttu-id="01855-145">15. mars</span><span class="sxs-lookup"><span data-stu-id="01855-145">March 15</span></span>       | <span data-ttu-id="01855-146">10</span><span class="sxs-lookup"><span data-stu-id="01855-146">10</span></span>       | <span data-ttu-id="01855-147">1.000</span><span class="sxs-lookup"><span data-stu-id="01855-147">1,000</span></span>       | <span data-ttu-id="01855-148">1.000</span><span class="sxs-lookup"><span data-stu-id="01855-148">1,000</span></span>                |
| <span data-ttu-id="01855-149">Innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="01855-149">Purchase order</span></span> | <span data-ttu-id="01855-150">2</span><span class="sxs-lookup"><span data-stu-id="01855-150">2</span></span>    | <span data-ttu-id="01855-151">21</span><span class="sxs-lookup"><span data-stu-id="01855-151">21</span></span>        | <span data-ttu-id="01855-152">Innkeypt</span><span class="sxs-lookup"><span data-stu-id="01855-152">Purchased</span></span> |       | <span data-ttu-id="01855-153">15. mars</span><span class="sxs-lookup"><span data-stu-id="01855-153">March 15</span></span>      | <span data-ttu-id="01855-154">15. mars</span><span class="sxs-lookup"><span data-stu-id="01855-154">March 15</span></span>       | <span data-ttu-id="01855-155">10</span><span class="sxs-lookup"><span data-stu-id="01855-155">10</span></span>       | <span data-ttu-id="01855-156">2,000</span><span class="sxs-lookup"><span data-stu-id="01855-156">2,000</span></span>       | <span data-ttu-id="01855-157">2,000</span><span class="sxs-lookup"><span data-stu-id="01855-157">2,000</span></span>                |
| <span data-ttu-id="01855-158">Innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="01855-158">Purchase order</span></span> | <span data-ttu-id="01855-159">1</span><span class="sxs-lookup"><span data-stu-id="01855-159">1</span></span>    | <span data-ttu-id="01855-160">11</span><span class="sxs-lookup"><span data-stu-id="01855-160">11</span></span>        | <span data-ttu-id="01855-161">Móttekið</span><span class="sxs-lookup"><span data-stu-id="01855-161">Received</span></span>  |       | <span data-ttu-id="01855-162">15. apríl</span><span class="sxs-lookup"><span data-stu-id="01855-162">April 15</span></span>      |                | <span data-ttu-id="01855-163">5</span><span class="sxs-lookup"><span data-stu-id="01855-163">5</span></span>        |             | <span data-ttu-id="01855-164">375</span><span class="sxs-lookup"><span data-stu-id="01855-164">375</span></span>                  |
| <span data-ttu-id="01855-165">Flutningspöntun</span><span class="sxs-lookup"><span data-stu-id="01855-165">Transfer order</span></span> | <span data-ttu-id="01855-166">1</span><span class="sxs-lookup"><span data-stu-id="01855-166">1</span></span>    | <span data-ttu-id="01855-167">11</span><span class="sxs-lookup"><span data-stu-id="01855-167">11</span></span>        |           | <span data-ttu-id="01855-168">Selt</span><span class="sxs-lookup"><span data-stu-id="01855-168">Sold</span></span>  | <span data-ttu-id="01855-169">2. maí</span><span class="sxs-lookup"><span data-stu-id="01855-169">May 2</span></span>         | <span data-ttu-id="01855-170">2. maí</span><span class="sxs-lookup"><span data-stu-id="01855-170">May 2</span></span>          | <span data-ttu-id="01855-171">-5</span><span class="sxs-lookup"><span data-stu-id="01855-171">-5</span></span>       | <span data-ttu-id="01855-172">-458,33</span><span class="sxs-lookup"><span data-stu-id="01855-172">-458.33</span></span>     | <span data-ttu-id="01855-173">-458,33</span><span class="sxs-lookup"><span data-stu-id="01855-173">-458.33</span></span>              |
| <span data-ttu-id="01855-174">Flutningspöntun</span><span class="sxs-lookup"><span data-stu-id="01855-174">Transfer order</span></span> | <span data-ttu-id="01855-175">1</span><span class="sxs-lookup"><span data-stu-id="01855-175">1</span></span>    | <span data-ttu-id="01855-176">12</span><span class="sxs-lookup"><span data-stu-id="01855-176">12</span></span>        | <span data-ttu-id="01855-177">Innkeypt</span><span class="sxs-lookup"><span data-stu-id="01855-177">Purchased</span></span> |       | <span data-ttu-id="01855-178">2. maí</span><span class="sxs-lookup"><span data-stu-id="01855-178">May 2</span></span>         | <span data-ttu-id="01855-179">2. maí</span><span class="sxs-lookup"><span data-stu-id="01855-179">May 2</span></span>          | <span data-ttu-id="01855-180">5</span><span class="sxs-lookup"><span data-stu-id="01855-180">5</span></span>        | <span data-ttu-id="01855-181">458.33</span><span class="sxs-lookup"><span data-stu-id="01855-181">458.33</span></span>      | <span data-ttu-id="01855-182">458.33</span><span class="sxs-lookup"><span data-stu-id="01855-182">458.33</span></span>               |
| <span data-ttu-id="01855-183">Sölupöntun</span><span class="sxs-lookup"><span data-stu-id="01855-183">Sales order</span></span>    | <span data-ttu-id="01855-184">1</span><span class="sxs-lookup"><span data-stu-id="01855-184">1</span></span>    | <span data-ttu-id="01855-185">12</span><span class="sxs-lookup"><span data-stu-id="01855-185">12</span></span>        |           | <span data-ttu-id="01855-186">Selt</span><span class="sxs-lookup"><span data-stu-id="01855-186">Sold</span></span>  | <span data-ttu-id="01855-187">3. maí</span><span class="sxs-lookup"><span data-stu-id="01855-187">May 3</span></span>         | <span data-ttu-id="01855-188">3. maí</span><span class="sxs-lookup"><span data-stu-id="01855-188">May 3</span></span>          | <span data-ttu-id="01855-189">-1</span><span class="sxs-lookup"><span data-stu-id="01855-189">-1</span></span>       | <span data-ttu-id="01855-190">-91,67</span><span class="sxs-lookup"><span data-stu-id="01855-190">-91.67</span></span>      | <span data-ttu-id="01855-191">-91,67</span><span class="sxs-lookup"><span data-stu-id="01855-191">-91.67</span></span>               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a><span data-ttu-id="01855-192">Hvernig magn og upphæðir í hverjum tímaramma er reiknað</span><span class="sxs-lookup"><span data-stu-id="01855-192">How quantities and amounts in each period bucket are calculated</span></span>

<span data-ttu-id="01855-193">Með því að nota sýnigögnin sem lýst er í fyrri hlutunum er hægt að keyra skýrsluna **Aldursgreining** sem er með eftirfarandi stillingum:</span><span class="sxs-lookup"><span data-stu-id="01855-193">By using the sample data that is described in the previous sections, you can run an **Inventory aging** report that has the following settings:</span></span>

- <span data-ttu-id="01855-194">**Frá og með dagsetningunni:** *9. maí 2020*</span><span class="sxs-lookup"><span data-stu-id="01855-194">**As of date:** *May 9, 2020*</span></span>
- <span data-ttu-id="01855-195">**Svæði:** *Yfirlit*</span><span class="sxs-lookup"><span data-stu-id="01855-195">**Site:** *View*</span></span>
- <span data-ttu-id="01855-196">**Vöruhús:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="01855-196">**Warehouse:** *No*</span></span>
- <span data-ttu-id="01855-197">**Vörunúmer:** *Samtala*</span><span class="sxs-lookup"><span data-stu-id="01855-197">**Item number:** *Total*</span></span>
- <span data-ttu-id="01855-198">**Aldursgreiningartímabil:** Stillið þennan reit til að búa til mánaðarramma.</span><span class="sxs-lookup"><span data-stu-id="01855-198">**Aging period:** Set this field to generate monthly buckets.</span></span>

<span data-ttu-id="01855-199">Í þessu tilfelli mun innihald skýrslunnar sem búin er til líkjast eftirfarandi dæmi.</span><span class="sxs-lookup"><span data-stu-id="01855-199">In this case, the content of the report that is generated will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="01855-200">Vörunúmer</span><span class="sxs-lookup"><span data-stu-id="01855-200">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-201">Svæði</span><span class="sxs-lookup"><span data-stu-id="01855-201">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-202">Lagerbirgðir</span><span class="sxs-lookup"><span data-stu-id="01855-202">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-203">Virði á lager</span><span class="sxs-lookup"><span data-stu-id="01855-203">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-204">Magn birgðavirðis</span><span class="sxs-lookup"><span data-stu-id="01855-204">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-205">Birgðavirði</span><span class="sxs-lookup"><span data-stu-id="01855-205">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-206">Meðaleiningarkostnaður</span><span class="sxs-lookup"><span data-stu-id="01855-206">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="01855-207">8.5.2020–1.5.2020</span><span class="sxs-lookup"><span data-stu-id="01855-207">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="01855-208">30.4.2020–1.4.2020</span><span class="sxs-lookup"><span data-stu-id="01855-208">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="01855-209">31.3.2020–1.3.2020</span><span class="sxs-lookup"><span data-stu-id="01855-209">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="01855-210">P1:Magn</span><span class="sxs-lookup"><span data-stu-id="01855-210">P1:Quantity</span></span></th>
    <th><span data-ttu-id="01855-211">P1:Upphæð</span><span class="sxs-lookup"><span data-stu-id="01855-211">P1:Amount</span></span></th>
    <th><span data-ttu-id="01855-212">P2:Magn</span><span class="sxs-lookup"><span data-stu-id="01855-212">P2:Quantity</span></span></th>
    <th><span data-ttu-id="01855-213">P2:Upphæð</span><span class="sxs-lookup"><span data-stu-id="01855-213">P2:Amount</span></span></th>
    <th><span data-ttu-id="01855-214">P3:Magn</span><span class="sxs-lookup"><span data-stu-id="01855-214">P3:Quantity</span></span></th>
    <th><span data-ttu-id="01855-215">P3:Upphæð</span><span class="sxs-lookup"><span data-stu-id="01855-215">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="01855-216">1000</span><span class="sxs-lookup"><span data-stu-id="01855-216">1000</span></span></td>
    <td><span data-ttu-id="01855-217">1</span><span class="sxs-lookup"><span data-stu-id="01855-217">1</span></span></td>
    <td><span data-ttu-id="01855-218">14</span><span class="sxs-lookup"><span data-stu-id="01855-218">14</span></span></td>
    <td><span data-ttu-id="01855-219">1,283.33</span><span class="sxs-lookup"><span data-stu-id="01855-219">1,283.33</span></span></td>
    <td><span data-ttu-id="01855-220">14</span><span class="sxs-lookup"><span data-stu-id="01855-220">14</span></span></td>
    <td><span data-ttu-id="01855-221">1,283.33</span><span class="sxs-lookup"><span data-stu-id="01855-221">1,283.33</span></span></td>
    <td><span data-ttu-id="01855-222">91.67</span><span class="sxs-lookup"><span data-stu-id="01855-222">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="01855-223">5.00</span><span class="sxs-lookup"><span data-stu-id="01855-223">5.00</span></span></td>
    <td><span data-ttu-id="01855-224">458.33</span><span class="sxs-lookup"><span data-stu-id="01855-224">458.33</span></span></td>
    <td><span data-ttu-id="01855-225">9.00</span><span class="sxs-lookup"><span data-stu-id="01855-225">9.00</span></span></td>
    <td><span data-ttu-id="01855-226">825.00</span><span class="sxs-lookup"><span data-stu-id="01855-226">825.00</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="01855-227">1000</span><span class="sxs-lookup"><span data-stu-id="01855-227">1000</span></span></td>
    <td><span data-ttu-id="01855-228">2</span><span class="sxs-lookup"><span data-stu-id="01855-228">2</span></span></td>
    <td><span data-ttu-id="01855-229">10</span><span class="sxs-lookup"><span data-stu-id="01855-229">10</span></span></td>
    <td><span data-ttu-id="01855-230">2,000.00</span><span class="sxs-lookup"><span data-stu-id="01855-230">2,000.00</span></span></td>
    <td><span data-ttu-id="01855-231">10</span><span class="sxs-lookup"><span data-stu-id="01855-231">10</span></span></td>
    <td><span data-ttu-id="01855-232">2,000.00</span><span class="sxs-lookup"><span data-stu-id="01855-232">2,000.00</span></span></td>
    <td><span data-ttu-id="01855-233">200.00</span><span class="sxs-lookup"><span data-stu-id="01855-233">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="01855-234">10,00</span><span class="sxs-lookup"><span data-stu-id="01855-234">10.00</span></span></td>
    <td><span data-ttu-id="01855-235">2,000.00</span><span class="sxs-lookup"><span data-stu-id="01855-235">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="01855-236"><strong>1000 samtals</strong></span><span class="sxs-lookup"><span data-stu-id="01855-236"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td><span data-ttu-id="01855-237"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="01855-237"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="01855-238"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="01855-238"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="01855-239"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="01855-239"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="01855-240"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="01855-240"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="01855-241"><strong>19</strong></span><span class="sxs-lookup"><span data-stu-id="01855-241"><strong>19</strong></span></span></td>
    <td><span data-ttu-id="01855-242"><strong>2,825.00</strong></span><span class="sxs-lookup"><span data-stu-id="01855-242"><strong>2,825.00</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="01855-243">Athugið eftirfarandi upplýsingar í þessari sýniskýrslu:</span><span class="sxs-lookup"><span data-stu-id="01855-243">Note the following details in this example report:</span></span>

- <span data-ttu-id="01855-244">Gildin **Magn birgðavirðis**, **Birgðavirði** og **Meðalkostnaður einingar** sem sýnd eru í skýrslunni eru gildi fyrir fjárhagsbirgðavíddina (**Svæði**, í þessu tilfelli).</span><span class="sxs-lookup"><span data-stu-id="01855-244">The **Inventory value quantity**, **Inventory value**, and **Average unit cost** values that are shown on the report are values for the financial inventory dimension (**Site**, in this case).</span></span>

    <span data-ttu-id="01855-245">Til dæmis, fyrir svæði 1, sýnir skýrslan eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="01855-245">For example, for site 1, the report shows the following information:</span></span>

    - <span data-ttu-id="01855-246">Gildið **Magn birgðavirðis** er *14* (= 10 + 5 – 5 + 5 – 1).</span><span class="sxs-lookup"><span data-stu-id="01855-246">The **Inventory value quantity** value is *14* (= 10 + 5 – 5 + 5 – 1).</span></span>
    - <span data-ttu-id="01855-247">Gildið **Birgðavirði** er *1283,33* (= 1000 + 375 – 458,33 + 458,33 – 91,67).</span><span class="sxs-lookup"><span data-stu-id="01855-247">The **Inventory value** value is *1,283.33* (= 1,000 + 375 – 458.33 + 458.33 – 91.67).</span></span>
    - <span data-ttu-id="01855-248">Gildið **Meðalkostnaður einingar** er *91,67*.</span><span class="sxs-lookup"><span data-stu-id="01855-248">The **Average unit cost** value is *91.67*.</span></span>
    - <span data-ttu-id="01855-249">Gildið **Virði á lager** og gildið **Upphæð** í hverjum tímaramma eru reiknuð með því að nota gildið **Meðalkostnaður einingar**.</span><span class="sxs-lookup"><span data-stu-id="01855-249">The **On-hand value** value and the **Amount** value in each period bucket are calculated by using the **Average unit cost** value.</span></span>

- <span data-ttu-id="01855-250">Skýrslan ákvarðar magn á lager fyrir hvern tímaramma með því að draga saman heildarmagn móttekið af birgðum fyrir hvern tímaramma.</span><span class="sxs-lookup"><span data-stu-id="01855-250">The report determines the on-hand quantity for each period bucket by summarizing the total received inventory quantity for each period bucket.</span></span> <span data-ttu-id="01855-251">Hún notar fyrst inn, fyrst út (FIFO) regluna til að draga frá heildarmagn losunar, óháð birgðalíkaninu sem varan notar.</span><span class="sxs-lookup"><span data-stu-id="01855-251">It then applies the first in, first out (FIFO) principle to deduct the total issued quantity, regardless of the inventory model that the items use.</span></span>

<span data-ttu-id="01855-252">Ef sama skýrslan er keyrð aftur, en í þetta skipti eru báðir reitirnir **Svæði** og **Vöruhús** eru stilltir á *Skoða*, mun nýja skýrslan líkjast eftirfarandi dæmi.</span><span class="sxs-lookup"><span data-stu-id="01855-252">If you run the same report again, but this time you set both the **Site** and **Warehouse** fields to *View*, the new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="01855-253">Vörunúmer</span><span class="sxs-lookup"><span data-stu-id="01855-253">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-254">Svæði</span><span class="sxs-lookup"><span data-stu-id="01855-254">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-255">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="01855-255">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-256">Lagerbirgðir</span><span class="sxs-lookup"><span data-stu-id="01855-256">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-257">Virði á lager</span><span class="sxs-lookup"><span data-stu-id="01855-257">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-258">Magn birgðavirðis</span><span class="sxs-lookup"><span data-stu-id="01855-258">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-259">Birgðavirði</span><span class="sxs-lookup"><span data-stu-id="01855-259">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-260">Meðaleiningarkostnaður</span><span class="sxs-lookup"><span data-stu-id="01855-260">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="01855-261">8.5.2020–1.5.2020</span><span class="sxs-lookup"><span data-stu-id="01855-261">5/8/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="01855-262">30.4.2020–1.4.2020</span><span class="sxs-lookup"><span data-stu-id="01855-262">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="01855-263">31.3.2020–1.3.2020</span><span class="sxs-lookup"><span data-stu-id="01855-263">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="01855-264">P1:Magn</span><span class="sxs-lookup"><span data-stu-id="01855-264">P1:Quantity</span></span></th>
    <th><span data-ttu-id="01855-265">P1:Upphæð</span><span class="sxs-lookup"><span data-stu-id="01855-265">P1:Amount</span></span></th>
    <th><span data-ttu-id="01855-266">P2:Magn</span><span class="sxs-lookup"><span data-stu-id="01855-266">P2:Quantity</span></span></th>
    <th><span data-ttu-id="01855-267">P2:Upphæð</span><span class="sxs-lookup"><span data-stu-id="01855-267">P2:Amount</span></span></th>
    <th><span data-ttu-id="01855-268">P3:Magn</span><span class="sxs-lookup"><span data-stu-id="01855-268">P3:Quantity</span></span></th>
    <th><span data-ttu-id="01855-269">P3:Upphæð</span><span class="sxs-lookup"><span data-stu-id="01855-269">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="01855-270">1000</span><span class="sxs-lookup"><span data-stu-id="01855-270">1000</span></span></td>
    <td><span data-ttu-id="01855-271">1</span><span class="sxs-lookup"><span data-stu-id="01855-271">1</span></span></td>
    <td><span data-ttu-id="01855-272">11</span><span class="sxs-lookup"><span data-stu-id="01855-272">11</span></span></td>
    <td><span data-ttu-id="01855-273">10</span><span class="sxs-lookup"><span data-stu-id="01855-273">10</span></span></td>
    <td><span data-ttu-id="01855-274">916.67</span><span class="sxs-lookup"><span data-stu-id="01855-274">916.67</span></span></td>
    <td><span data-ttu-id="01855-275">14</span><span class="sxs-lookup"><span data-stu-id="01855-275">14</span></span></td>
    <td><span data-ttu-id="01855-276">1,283.33</span><span class="sxs-lookup"><span data-stu-id="01855-276">1,283.33</span></span></td>
    <td><span data-ttu-id="01855-277">91.67</span><span class="sxs-lookup"><span data-stu-id="01855-277">91.67</span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="01855-278">5.00</span><span class="sxs-lookup"><span data-stu-id="01855-278">5.00</span></span></td>
    <td><span data-ttu-id="01855-279">458.33</span><span class="sxs-lookup"><span data-stu-id="01855-279">458.33</span></span></td>
    <td><span data-ttu-id="01855-280">5.00</span><span class="sxs-lookup"><span data-stu-id="01855-280">5.00</span></span></td>
    <td><span data-ttu-id="01855-281">458.33</span><span class="sxs-lookup"><span data-stu-id="01855-281">458.33</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="01855-282">1000</span><span class="sxs-lookup"><span data-stu-id="01855-282">1000</span></span></td>
    <td><span data-ttu-id="01855-283">1</span><span class="sxs-lookup"><span data-stu-id="01855-283">1</span></span></td>
    <td><span data-ttu-id="01855-284">12</span><span class="sxs-lookup"><span data-stu-id="01855-284">12</span></span></td>
    <td><span data-ttu-id="01855-285">4</span><span class="sxs-lookup"><span data-stu-id="01855-285">4</span></span></td>
    <td><span data-ttu-id="01855-286">366.67</span><span class="sxs-lookup"><span data-stu-id="01855-286">366.67</span></span></td>
    <td><span data-ttu-id="01855-287">14</span><span class="sxs-lookup"><span data-stu-id="01855-287">14</span></span></td>
    <td><span data-ttu-id="01855-288">1,283.33</span><span class="sxs-lookup"><span data-stu-id="01855-288">1,283.33</span></span></td>
    <td><span data-ttu-id="01855-289">91.67</span><span class="sxs-lookup"><span data-stu-id="01855-289">91.67</span></span></td>
    <td><span data-ttu-id="01855-290">4.00</span><span class="sxs-lookup"><span data-stu-id="01855-290">4.00</span></span></td>
    <td><span data-ttu-id="01855-291">366.67</span><span class="sxs-lookup"><span data-stu-id="01855-291">366.67</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="01855-292">1000</span><span class="sxs-lookup"><span data-stu-id="01855-292">1000</span></span></td>
    <td><span data-ttu-id="01855-293">2</span><span class="sxs-lookup"><span data-stu-id="01855-293">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="01855-294">10</span><span class="sxs-lookup"><span data-stu-id="01855-294">10</span></span></td>
    <td><span data-ttu-id="01855-295">2,000.00</span><span class="sxs-lookup"><span data-stu-id="01855-295">2,000.00</span></span></td>
    <td><span data-ttu-id="01855-296">10</span><span class="sxs-lookup"><span data-stu-id="01855-296">10</span></span></td>
    <td><span data-ttu-id="01855-297">2,000.00</span><span class="sxs-lookup"><span data-stu-id="01855-297">2,000.00</span></span></td>
    <td><span data-ttu-id="01855-298">200.00</span><span class="sxs-lookup"><span data-stu-id="01855-298">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="01855-299">10,00</span><span class="sxs-lookup"><span data-stu-id="01855-299">10.00</span></span></td>
    <td><span data-ttu-id="01855-300">2,000.00</span><span class="sxs-lookup"><span data-stu-id="01855-300">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="01855-301"><strong>1000 samtals</strong></span><span class="sxs-lookup"><span data-stu-id="01855-301"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="01855-302"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="01855-302"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="01855-303"><strong>3,283.33</strong></span><span class="sxs-lookup"><span data-stu-id="01855-303"><strong>3,283.33</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="01855-304"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="01855-304"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="01855-305"><strong>366.67</strong></span><span class="sxs-lookup"><span data-stu-id="01855-305"><strong>366.67</strong></span></span></td>
    <td><span data-ttu-id="01855-306"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="01855-306"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="01855-307"><strong>458.33</strong></span><span class="sxs-lookup"><span data-stu-id="01855-307"><strong>458.33</strong></span></span></td>
    <td><span data-ttu-id="01855-308"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="01855-308"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="01855-309"><strong>2,458.33</strong></span><span class="sxs-lookup"><span data-stu-id="01855-309"><strong>2,458.33</strong></span></span></td>
</tr>
</tfoot>
</table>

<span data-ttu-id="01855-310">Í þetta skipti er svæði 1 skipt niður í tvær raðir, ein fyrir vöruhús 11 og ein fyrir vöruhús 12.</span><span class="sxs-lookup"><span data-stu-id="01855-310">This time, site 1 is split into two rows, one for warehouse 11 and one for warehouse 12.</span></span> <span data-ttu-id="01855-311">Hinsvegar eru gildin **Magn birgðavirðis**, **Birgðavirði** og **Meðalkostnaður einingar** enn þau sömu vegna þess að **Vöruhús** er ekki fjárhagsbirgðavídd.</span><span class="sxs-lookup"><span data-stu-id="01855-311">However, the **Inventory value quantity**, **Inventory value**, and **Average unit cost** values are the same, because **Warehouse** isn't a financial inventory dimension.</span></span>

<span data-ttu-id="01855-312">Takið auk þess eftir því að dreift magn á svæði 1 er annað.</span><span class="sxs-lookup"><span data-stu-id="01855-312">Additionally, notice that the quantity distribution of site 1 is different.</span></span> <span data-ttu-id="01855-313">Í fyrstu skýrslunni sem var keyrð hunsaði kerfið millifærslupöntunina sem átti sér stað á sama svæðinu og dró frá magn sölureikningsins frá tímarammanum **31.3.2020 - 1.3.2020** á svæði 1.</span><span class="sxs-lookup"><span data-stu-id="01855-313">In the first report that you ran, the system ignored the transfer order that occurred in the same site and deducted the quantity of the sales invoice from the **3/31/2020 - 3/1/2020** period bucket in site 1.</span></span> <span data-ttu-id="01855-314">Í nýju skýrslunni dregur kerfið hins vegar frá magn sölureikningsins frá tímarammanum **8.5.2020 - 1.5.2020** í vöruhúsi 12.</span><span class="sxs-lookup"><span data-stu-id="01855-314">However, in the new report, the system deducts the quantity of the sales invoice from the **5/8/2020 - 5/1/2020** period bucket in warehouse 12.</span></span>

## <a name="effects-of-inventory-closing"></a><span data-ttu-id="01855-315">Áhrif birgðalokunar</span><span class="sxs-lookup"><span data-stu-id="01855-315">Effects of inventory closing</span></span>

<span data-ttu-id="01855-316">Ef keyrð er birgðalokun fyrir maí og fyrri skýrslan síðan keyrð aftur, en reiturinn **Frá og með dagsetningunni** er stilltur á *31. maí 2020* koma eftirfarandi niðurstöður í ljós:</span><span class="sxs-lookup"><span data-stu-id="01855-316">If you run the inventory closing for May and then run the previous report again, but you set the **As of date** field to *May 31, 2020*, you will notice the following results:</span></span>

- <span data-ttu-id="01855-317">Gildin **Birgðavirði** og **Meðalkostnaður einingar** eru uppfærð.</span><span class="sxs-lookup"><span data-stu-id="01855-317">The **Inventory value** and **Average unit cost** values are updated.</span></span>
- <span data-ttu-id="01855-318">Gildið **Virði á lager** og gildið **Upphæð** í hverjum tímaramma eru uppfærð í samræmi.</span><span class="sxs-lookup"><span data-stu-id="01855-318">The **On-hand value** value and all the **Amount** values in every period bucket are updated accordingly.</span></span>

<span data-ttu-id="01855-319">Nýja skýrslan mun líkjast eftirfarandi dæmi.</span><span class="sxs-lookup"><span data-stu-id="01855-319">The new report will resemble the following example.</span></span>

<table>
<thead>
<tr>
    <th rowspan="2"><span data-ttu-id="01855-320">Vörunúmer</span><span class="sxs-lookup"><span data-stu-id="01855-320">Item number</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-321">Svæði</span><span class="sxs-lookup"><span data-stu-id="01855-321">Site</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-322">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="01855-322">Warehouse</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-323">Lagerbirgðir</span><span class="sxs-lookup"><span data-stu-id="01855-323">On-hand quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-324">Virði á lager</span><span class="sxs-lookup"><span data-stu-id="01855-324">On-hand value</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-325">Magn birgðavirðis</span><span class="sxs-lookup"><span data-stu-id="01855-325">Inventory value quantity</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-326">Birgðavirði</span><span class="sxs-lookup"><span data-stu-id="01855-326">Inventory value</span></span></th>
    <th rowspan="2"><span data-ttu-id="01855-327">Meðaleiningarkostnaður</span><span class="sxs-lookup"><span data-stu-id="01855-327">Average unit cost</span></span></th>
    <th colspan="2"><span data-ttu-id="01855-328">31.5.2020–1.5.2020</span><span class="sxs-lookup"><span data-stu-id="01855-328">5/31/2020 - 5/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="01855-329">30.4.2020–1.4.2020</span><span class="sxs-lookup"><span data-stu-id="01855-329">4/30/2020 - 4/1/2020</span></span></th>
    <th colspan="2"><span data-ttu-id="01855-330">31.3.2020–1.3.2020</span><span class="sxs-lookup"><span data-stu-id="01855-330">3/31/2020 - 3/1/2020</span></span></th>
</tr>
<tr>
    <th><span data-ttu-id="01855-331">P1:Magn</span><span class="sxs-lookup"><span data-stu-id="01855-331">P1:Quantity</span></span></th>
    <th><span data-ttu-id="01855-332">P1:Upphæð</span><span class="sxs-lookup"><span data-stu-id="01855-332">P1:Amount</span></span></th>
    <th><span data-ttu-id="01855-333">P2:Magn</span><span class="sxs-lookup"><span data-stu-id="01855-333">P2:Quantity</span></span></th>
    <th><span data-ttu-id="01855-334">P2:Upphæð</span><span class="sxs-lookup"><span data-stu-id="01855-334">P2:Amount</span></span></th>
    <th><span data-ttu-id="01855-335">P3:Magn</span><span class="sxs-lookup"><span data-stu-id="01855-335">P3:Quantity</span></span></th>
    <th><span data-ttu-id="01855-336">P3:Upphæð</span><span class="sxs-lookup"><span data-stu-id="01855-336">P3:Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
    <td><span data-ttu-id="01855-337">1000</span><span class="sxs-lookup"><span data-stu-id="01855-337">1000</span></span></td>
    <td><span data-ttu-id="01855-338">1</span><span class="sxs-lookup"><span data-stu-id="01855-338">1</span></span></td>
    <td><span data-ttu-id="01855-339">11</span><span class="sxs-lookup"><span data-stu-id="01855-339">11</span></span></td>
    <td><span data-ttu-id="01855-340">10</span><span class="sxs-lookup"><span data-stu-id="01855-340">10</span></span></td>
    <td><span data-ttu-id="01855-341">910.70</span><span class="sxs-lookup"><span data-stu-id="01855-341">910.70</span></span></td>
    <td><span data-ttu-id="01855-342">14</span><span class="sxs-lookup"><span data-stu-id="01855-342">14</span></span></td>
    <td><span data-ttu-id="01855-343">1,275.00</span><span class="sxs-lookup"><span data-stu-id="01855-343">1,275.00</span></span></td>
    <td><span data-ttu-id="01855-344">91.07</span><span class="sxs-lookup"><span data-stu-id="01855-344">91.07</span></span></td>
    <td><span data-ttu-id="01855-345">0,00</span><span class="sxs-lookup"><span data-stu-id="01855-345">0.00</span></span></td>
    <td></td>
    <td><span data-ttu-id="01855-346">5.00</span><span class="sxs-lookup"><span data-stu-id="01855-346">5.00</span></span></td>
    <td><span data-ttu-id="01855-347">455.36</span><span class="sxs-lookup"><span data-stu-id="01855-347">455.36</span></span></td>
    <td><span data-ttu-id="01855-348">5.00</span><span class="sxs-lookup"><span data-stu-id="01855-348">5.00</span></span></td>
    <td><span data-ttu-id="01855-349">455.36</span><span class="sxs-lookup"><span data-stu-id="01855-349">455.36</span></span></td>
</tr>
<tr>
    <td><span data-ttu-id="01855-350">1000</span><span class="sxs-lookup"><span data-stu-id="01855-350">1000</span></span></td>
    <td><span data-ttu-id="01855-351">1</span><span class="sxs-lookup"><span data-stu-id="01855-351">1</span></span></td>
    <td><span data-ttu-id="01855-352">12</span><span class="sxs-lookup"><span data-stu-id="01855-352">12</span></span></td>
    <td><span data-ttu-id="01855-353">4</span><span class="sxs-lookup"><span data-stu-id="01855-353">4</span></span></td>
    <td><span data-ttu-id="01855-354">364.29</span><span class="sxs-lookup"><span data-stu-id="01855-354">364.29</span></span></td>
    <td><span data-ttu-id="01855-355">14</span><span class="sxs-lookup"><span data-stu-id="01855-355">14</span></span></td>
    <td><span data-ttu-id="01855-356">1,275.00</span><span class="sxs-lookup"><span data-stu-id="01855-356">1,275.00</span></span></td>
    <td><span data-ttu-id="01855-357">91.07</span><span class="sxs-lookup"><span data-stu-id="01855-357">91.07</span></span></td>
    <td><span data-ttu-id="01855-358">4.00</span><span class="sxs-lookup"><span data-stu-id="01855-358">4.00</span></span></td>
    <td><span data-ttu-id="01855-359">364.29</span><span class="sxs-lookup"><span data-stu-id="01855-359">364.29</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td><span data-ttu-id="01855-360">1000</span><span class="sxs-lookup"><span data-stu-id="01855-360">1000</span></span></td>
    <td><span data-ttu-id="01855-361">2</span><span class="sxs-lookup"><span data-stu-id="01855-361">2</span></span></td>
    <td></td>
    <td><span data-ttu-id="01855-362">10</span><span class="sxs-lookup"><span data-stu-id="01855-362">10</span></span></td>
    <td><span data-ttu-id="01855-363">2,000.00</span><span class="sxs-lookup"><span data-stu-id="01855-363">2,000.00</span></span></td>
    <td><span data-ttu-id="01855-364">10</span><span class="sxs-lookup"><span data-stu-id="01855-364">10</span></span></td>
    <td><span data-ttu-id="01855-365">2,000.00</span><span class="sxs-lookup"><span data-stu-id="01855-365">2,000.00</span></span></td>
    <td><span data-ttu-id="01855-366">200.00</span><span class="sxs-lookup"><span data-stu-id="01855-366">200.00</span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="01855-367">10,00</span><span class="sxs-lookup"><span data-stu-id="01855-367">10.00</span></span></td>
    <td><span data-ttu-id="01855-368">2,000.00</span><span class="sxs-lookup"><span data-stu-id="01855-368">2,000.00</span></span></td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><span data-ttu-id="01855-369"><strong>1000 samtals</strong></span><span class="sxs-lookup"><span data-stu-id="01855-369"><strong>1000 Totals</strong></span></span></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="01855-370"><strong>24.00</strong></span><span class="sxs-lookup"><span data-stu-id="01855-370"><strong>24.00</strong></span></span></td>
    <td><span data-ttu-id="01855-371"><strong>3,275.00</strong></span><span class="sxs-lookup"><span data-stu-id="01855-371"><strong>3,275.00</strong></span></span></td>
    <td></td>
    <td></td>
    <td></td>
    <td><span data-ttu-id="01855-372"><strong>4.00</strong></span><span class="sxs-lookup"><span data-stu-id="01855-372"><strong>4.00</strong></span></span></td>
    <td><span data-ttu-id="01855-373"><strong>364.29</strong></span><span class="sxs-lookup"><span data-stu-id="01855-373"><strong>364.29</strong></span></span></td>
    <td><span data-ttu-id="01855-374"><strong>5.00</strong></span><span class="sxs-lookup"><span data-stu-id="01855-374"><strong>5.00</strong></span></span></td>
    <td><span data-ttu-id="01855-375"><strong>455.36</strong></span><span class="sxs-lookup"><span data-stu-id="01855-375"><strong>455.36</strong></span></span></td>
    <td><span data-ttu-id="01855-376"><strong>15</strong></span><span class="sxs-lookup"><span data-stu-id="01855-376"><strong>15</strong></span></span></td>
    <td><span data-ttu-id="01855-377"><strong>2,455.36</strong></span><span class="sxs-lookup"><span data-stu-id="01855-377"><strong>2,455.36</strong></span></span></td>
</tr>
</tfoot>
</table>
