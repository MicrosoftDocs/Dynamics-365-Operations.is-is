---
title: Gildi birgðahlutar
description: Þessi grein veitir upplýsingar um hvernig gildi birgðahlutar eru reiknuð.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventCostOnhandItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19111
ms.assetid: 56a7c8ba-bf4a-4b1d-918d-56bb96926c4f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ff3a21e87b9cb0bb371b0772c948cb62a4cb36b1
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214620"
---
# <a name="inventory-object-values"></a><span data-ttu-id="cc5b0-103">Gildi birgðahlutar</span><span class="sxs-lookup"><span data-stu-id="cc5b0-103">Inventory object values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc5b0-104">Þessi grein veitir upplýsingar um hvernig gildi birgðahlutar eru reiknuð.</span><span class="sxs-lookup"><span data-stu-id="cc5b0-104">This article provides information about how the values of an inventory object are calculated.</span></span> 

<span data-ttu-id="cc5b0-105">Ný aðgerð sem kallast **efnislegt magn** gerir það mögulegt að sjá gildi tilgreinds birgðahutar.</span><span class="sxs-lookup"><span data-stu-id="cc5b0-105">A new functionality that is named **physical quantity** lets you see the values of a specific inventory object.</span></span> 

<span data-ttu-id="cc5b0-106">Kostnaðarhlutur táknar einingarstig þar sem birgðabókhald er framkvæmt.</span><span class="sxs-lookup"><span data-stu-id="cc5b0-106">A cost object represents the entity level where inventory accounting is performed.</span></span> <span data-ttu-id="cc5b0-107">Nánari upplýsingar um kostnaðarhluti er í [Kostnaðarhlutir](cost-object.md).</span><span class="sxs-lookup"><span data-stu-id="cc5b0-107">For more information about cost objects, see [Cost objects](cost-object.md).</span></span> 

<span data-ttu-id="cc5b0-108">Til að sjá gildi tiltekins birgðahlutar skal smella á **Efnislegt magn** á síðunni **Kostnaðarhlutur**.</span><span class="sxs-lookup"><span data-stu-id="cc5b0-108">To see the values of a specific inventory object, click **Physical quantity** on the **Cost object** page.</span></span> <span data-ttu-id="cc5b0-109">Hér er sýnt hvernig gildi birgðahlutar er reiknað:</span><span class="sxs-lookup"><span data-stu-id="cc5b0-109">Here is how the value of an inventory object is calculated:</span></span> 

<span data-ttu-id="cc5b0-110">Birgðahlutur.Virði = Kostnaðarhlutur.Meðaltal einingarkostnaðar x Birgðahlutur.Magn</span><span class="sxs-lookup"><span data-stu-id="cc5b0-110">Inventory object.Value = Cost object.Average unit cost × Inventory object.Quantity</span></span> 

<span data-ttu-id="cc5b0-111">Sem eftirfarandi dæmi sýnir hvernig gildi birgðahlutar og kostnaðarhlutar eru reiknuð.</span><span class="sxs-lookup"><span data-stu-id="cc5b0-111">The following example shows how the values of an inventory object and a cost object are calculated.</span></span> <span data-ttu-id="cc5b0-112">Tvö innhreyfingarskjöl afurða eru skráð á vöru A:</span><span class="sxs-lookup"><span data-stu-id="cc5b0-112">Two product receipt events are registered on item A:</span></span>

-   <span data-ttu-id="cc5b0-113">Innhreyfingarskjal afurða 1: Magn = 100 stykki, Upphæð = $1000,00, Svæði = 1, Vöruhús = 11, Rununr.</span><span class="sxs-lookup"><span data-stu-id="cc5b0-113">Product receipt 1: Quantity = 100 pcs., Amount = $1,000.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="cc5b0-114">= B1</span><span class="sxs-lookup"><span data-stu-id="cc5b0-114">= B1</span></span>
-   <span data-ttu-id="cc5b0-115">Innhreyfingarskjal afurða 2: Magn = 50 stykki, Upphæð = $800,00, Svæði = 1, Vöruhús = 11, Rununr.</span><span class="sxs-lookup"><span data-stu-id="cc5b0-115">Product receipt 2: Quantity = 50 pcs., Amount = $800.00, Site = 1, Warehouse =11, Batch No.</span></span> <span data-ttu-id="cc5b0-116">= B2</span><span class="sxs-lookup"><span data-stu-id="cc5b0-116">= B2</span></span>

<span data-ttu-id="cc5b0-117">Eftirfarandi tafla sýnir niðurstöður útreiknings fyrir kostnaðarhlut.</span><span class="sxs-lookup"><span data-stu-id="cc5b0-117">The following table shows the calculation result for a cost object.</span></span> <span data-ttu-id="cc5b0-118">Hægt er að skoða niðurstöður á síðunni **Kostnaðarhlutur**.</span><span class="sxs-lookup"><span data-stu-id="cc5b0-118">You can view the result on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
<col width="14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cc5b0-119">Gerð hlutar</span><span class="sxs-lookup"><span data-stu-id="cc5b0-119">Object type</span></span></th>
<th><span data-ttu-id="cc5b0-120">Vörunúmer</span><span class="sxs-lookup"><span data-stu-id="cc5b0-120">Item number</span></span></th>
<th><span data-ttu-id="cc5b0-121">Svæði</span><span class="sxs-lookup"><span data-stu-id="cc5b0-121">Site</span></span></th>
<th><span data-ttu-id="cc5b0-122">Magn</span><span class="sxs-lookup"><span data-stu-id="cc5b0-122">Quantity</span></span></th>
<th><span data-ttu-id="cc5b0-123">Birgðaeining</span><span class="sxs-lookup"><span data-stu-id="cc5b0-123">Inventory unit</span></span></th>
<th><span data-ttu-id="cc5b0-124">Gildi</span><span class="sxs-lookup"><span data-stu-id="cc5b0-124">Value</span></span></th>
<th><span data-ttu-id="cc5b0-125">Meðaleiningarkostnaður</span><span class="sxs-lookup"><span data-stu-id="cc5b0-125">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc5b0-126">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cc5b0-126">Cost object</span></span></td>
<td><span data-ttu-id="cc5b0-127">Lista fyrir</span><span class="sxs-lookup"><span data-stu-id="cc5b0-127">A</span></span></td>
<td><span data-ttu-id="cc5b0-128">1</span><span class="sxs-lookup"><span data-stu-id="cc5b0-128">1</span></span></td>
<td><span data-ttu-id="cc5b0-129">150</span><span class="sxs-lookup"><span data-stu-id="cc5b0-129">150</span></span></td>
<td><span data-ttu-id="cc5b0-130">Stk.</span><span class="sxs-lookup"><span data-stu-id="cc5b0-130">Pcs.</span></span></td>
<td><p><span data-ttu-id="cc5b0-131">$1800,00</span><span class="sxs-lookup"><span data-stu-id="cc5b0-131">$1800.00</span></span></p></td>
<td><p><span data-ttu-id="cc5b0-132">$12,00</span><span class="sxs-lookup"><span data-stu-id="cc5b0-132">$12.00</span></span></p></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cc5b0-133">Eftirfarandi tafla sýnir niðurstöður útreiknings fyrir birgðahlut.</span><span class="sxs-lookup"><span data-stu-id="cc5b0-133">The following table shows the calculation result for an inventory object.</span></span> <span data-ttu-id="cc5b0-134">Hægt er að skoða niðurstöðurnar með því að smella á **Efnislegt magn** á síðunni **Kostnaðarhlutur**.</span><span class="sxs-lookup"><span data-stu-id="cc5b0-134">You can view the result by clicking **Physical quantity** on the **Cost object** page.</span></span>

<table style="width:100%;">
<colgroup>
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
<col width="11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cc5b0-135">Gerð hlutar</span><span class="sxs-lookup"><span data-stu-id="cc5b0-135">Object type</span></span></th>
<th><span data-ttu-id="cc5b0-136">Vörunúmer</span><span class="sxs-lookup"><span data-stu-id="cc5b0-136">Item number</span></span></th>
<th><span data-ttu-id="cc5b0-137">Svæði</span><span class="sxs-lookup"><span data-stu-id="cc5b0-137">Site</span></span></th>
<th><span data-ttu-id="cc5b0-138">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="cc5b0-138">Warehouse</span></span></th>
<th><span data-ttu-id="cc5b0-139">Rununr.</span><span class="sxs-lookup"><span data-stu-id="cc5b0-139">Batch No.</span></span></th>
<th><span data-ttu-id="cc5b0-140">Magn</span><span class="sxs-lookup"><span data-stu-id="cc5b0-140">Quantity</span></span></th>
<th><span data-ttu-id="cc5b0-141">Birgðaeining</span><span class="sxs-lookup"><span data-stu-id="cc5b0-141">Inventory unit</span></span></th>
<th><span data-ttu-id="cc5b0-142">Gildi</span><span class="sxs-lookup"><span data-stu-id="cc5b0-142">Value</span></span></th>
<th><span data-ttu-id="cc5b0-143">Meðaleiningarkostnaður</span><span class="sxs-lookup"><span data-stu-id="cc5b0-143">Average unit cost</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cc5b0-144">Birgðahlutur</span><span class="sxs-lookup"><span data-stu-id="cc5b0-144">Inventory object</span></span></td>
<td><span data-ttu-id="cc5b0-145">Lista fyrir</span><span class="sxs-lookup"><span data-stu-id="cc5b0-145">A</span></span></td>
<td><span data-ttu-id="cc5b0-146">1</span><span class="sxs-lookup"><span data-stu-id="cc5b0-146">1</span></span></td>
<td><span data-ttu-id="cc5b0-147">11</span><span class="sxs-lookup"><span data-stu-id="cc5b0-147">11</span></span></td>
<td><span data-ttu-id="cc5b0-148">B1</span><span class="sxs-lookup"><span data-stu-id="cc5b0-148">B1</span></span></td>
<td><span data-ttu-id="cc5b0-149">100</span><span class="sxs-lookup"><span data-stu-id="cc5b0-149">100</span></span></td>
<td><span data-ttu-id="cc5b0-150">Stk.</span><span class="sxs-lookup"><span data-stu-id="cc5b0-150">Pcs.</span></span></td>
<td><p><span data-ttu-id="cc5b0-151">$1200.00</span><span class="sxs-lookup"><span data-stu-id="cc5b0-151">$1200.00</span></span></p></td>
<td><p><span data-ttu-id="cc5b0-152">$12,00</span><span class="sxs-lookup"><span data-stu-id="cc5b0-152">$12.00</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cc5b0-153">Birgðahlutur</span><span class="sxs-lookup"><span data-stu-id="cc5b0-153">Inventory object</span></span></td>
<td><span data-ttu-id="cc5b0-154">A</span><span class="sxs-lookup"><span data-stu-id="cc5b0-154">A</span></span></td>
<td><span data-ttu-id="cc5b0-155">1</span><span class="sxs-lookup"><span data-stu-id="cc5b0-155">1</span></span></td>
<td><span data-ttu-id="cc5b0-156">11</span><span class="sxs-lookup"><span data-stu-id="cc5b0-156">11</span></span></td>
<td><span data-ttu-id="cc5b0-157">B2</span><span class="sxs-lookup"><span data-stu-id="cc5b0-157">B2</span></span></td>
<td><span data-ttu-id="cc5b0-158">50</span><span class="sxs-lookup"><span data-stu-id="cc5b0-158">50</span></span></td>
<td><span data-ttu-id="cc5b0-159">Stk.</span><span class="sxs-lookup"><span data-stu-id="cc5b0-159">Pcs.</span></span></td>
<td><p><span data-ttu-id="cc5b0-160">$600.00</span><span class="sxs-lookup"><span data-stu-id="cc5b0-160">$600.00</span></span></p></td>
<td><p><span data-ttu-id="cc5b0-161">$12,00</span><span class="sxs-lookup"><span data-stu-id="cc5b0-161">$12.00</span></span></p></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="cc5b0-162">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="cc5b0-162">Additional resources</span></span>
--------

[<span data-ttu-id="cc5b0-163">Kostnaðarhlutir</span><span class="sxs-lookup"><span data-stu-id="cc5b0-163">Cost objects</span></span>](cost-object.md)

[<span data-ttu-id="cc5b0-164">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="cc5b0-164">Cost entries</span></span>](cost-entries.md)

[<span data-ttu-id="cc5b0-165">Nýjungar og breytingar</span><span class="sxs-lookup"><span data-stu-id="cc5b0-165">What's new and changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)



