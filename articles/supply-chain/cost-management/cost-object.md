---
title: "Kostnaðarhlutir"
description: "Þetta grein veitir upplýsingar um kostnaðarhlutum og útskýrir hvernig kostnaði og magni eru uppsafnað. Kostnaðarhlutar er einingar sem kostnaður og magn er safnað upp fyrir. Eining kostnaðarhlutar geta verið annað hvort afurðarafbrigði eða afurð, eins og afbrigði stíls og litar."
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
ms.custom: 19451
ms.assetid: ec776b98-813a-490d-848f-468452d98fac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a61761a5c9d98befd67682e1790af5377b7a55e1
ms.openlocfilehash: 13efb284c24c20cf4115ce2dd50be31dd3e5543e
ms.contentlocale: is-is
ms.lasthandoff: 10/13/2017

---

# <a name="cost-objects"></a><span data-ttu-id="54e60-105">Kostnaðarhlutir</span><span class="sxs-lookup"><span data-stu-id="54e60-105">Cost objects</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="54e60-106">Þetta grein veitir upplýsingar um kostnaðarhlutum og útskýrir hvernig kostnaði og magni eru uppsafnað.</span><span class="sxs-lookup"><span data-stu-id="54e60-106">This article provides information about costs objects, and explains how costs and quantities are accumulated.</span></span> <span data-ttu-id="54e60-107">Kostnaðarhlutar er einingar sem kostnaður og magn er safnað upp fyrir.</span><span class="sxs-lookup"><span data-stu-id="54e60-107">A cost object is an entity that costs and quantities are accumulated for.</span></span> <span data-ttu-id="54e60-108">Eining kostnaðarhlutar geta verið annað hvort afurðarafbrigði eða afurð, eins og afbrigði stíls og litar.</span><span class="sxs-lookup"><span data-stu-id="54e60-108">A cost object entity can be either a product or product variants, such as variants for style and color.</span></span>  

## <a name="cost-objects"></a><span data-ttu-id="54e60-109">Kostnaðarhlutir</span><span class="sxs-lookup"><span data-stu-id="54e60-109">Cost objects</span></span>

<span data-ttu-id="54e60-110">Síðan **Kostnaðarhlutir** inniheldur lista yfir alla kostnaðarhluti sem eru skráðir á afurð.</span><span class="sxs-lookup"><span data-stu-id="54e60-110">The **Cost objects** page lists all cost objects that are registered on a product.</span></span> <span data-ttu-id="54e60-111">Kostnaðarhlutir eru skilgreindir með gögnum úr eftirfarandi upprunum:</span><span class="sxs-lookup"><span data-stu-id="54e60-111">The cost objects are defined by data from the following sources:</span></span>

-   <span data-ttu-id="54e60-112">Vara</span><span class="sxs-lookup"><span data-stu-id="54e60-112">Product</span></span>
-   <span data-ttu-id="54e60-113">Afurðavíddaflokkur</span><span class="sxs-lookup"><span data-stu-id="54e60-113">Product dimension group</span></span>
-   <span data-ttu-id="54e60-114">Geymsluvíddarflokkur</span><span class="sxs-lookup"><span data-stu-id="54e60-114">Storage dimension group</span></span>
-   <span data-ttu-id="54e60-115">Rakningarvíddarflokkur</span><span class="sxs-lookup"><span data-stu-id="54e60-115">Tracking dimension group</span></span>

<span data-ttu-id="54e60-116">**Ábending:** Kostnaðarhlutur stendur fyrir aðeins fyrir kostnaðareiningu af gerðinni **Bein efni**.</span><span class="sxs-lookup"><span data-stu-id="54e60-116">**Note:** A cost object represents a cost element of the **Direct material** type only.</span></span> <span data-ttu-id="54e60-117">Kostnaðarhlutur og birgðahlutur eru ólíkir á þann hátt að kostnaður hlutar er skilgreindur með birgðavíddum sem eru valdar fyrir fjárhagslegar birgðar.</span><span class="sxs-lookup"><span data-stu-id="54e60-117">A cost object and an inventory object differ in the way that a cost object is defined by the inventory dimensions that are selected for financial inventory.</span></span> <span data-ttu-id="54e60-118">Til dæmis, hefur vara eftirfarandi skilgreiningu:</span><span class="sxs-lookup"><span data-stu-id="54e60-118">For example, an item has the following configuration:</span></span>

-   <span data-ttu-id="54e60-119">**Svæði:** Efnislegar birgðir = Já, Fjárhagslegar birgðir = Já</span><span class="sxs-lookup"><span data-stu-id="54e60-119">**Site:** Physical inventory = Yes, Financial inventory = Yes</span></span>
-   <span data-ttu-id="54e60-120">**Vöruhús:** Efnislegar birgðir = Já, Fjárhagslegar birgðir = Nei</span><span class="sxs-lookup"><span data-stu-id="54e60-120">**Warehouse:** Physical inventory = Yes, Financial inventory = No</span></span>
-   <span data-ttu-id="54e60-121">**Rununr.:** Efnislegar birgðir = Já, Fjárhagslegar birgðir = Nei</span><span class="sxs-lookup"><span data-stu-id="54e60-121">**Batch No.:** Physical inventory = Yes, Financial inventory = No</span></span>

<span data-ttu-id="54e60-122">Eftirfarandi tafla sýnir hvað er kostnaðarhlutur og hvað birgðahlutur.</span><span class="sxs-lookup"><span data-stu-id="54e60-122">The following table shows what is a cost object and what is an inventory object.</span></span>

| <span data-ttu-id="54e60-123">Gerð hlutar</span><span class="sxs-lookup"><span data-stu-id="54e60-123">Object type</span></span>      | <span data-ttu-id="54e60-124">Vörunúmer</span><span class="sxs-lookup"><span data-stu-id="54e60-124">Item number</span></span> | <span data-ttu-id="54e60-125">Svæði</span><span class="sxs-lookup"><span data-stu-id="54e60-125">Site</span></span> | <span data-ttu-id="54e60-126">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="54e60-126">Warehouse</span></span> | <span data-ttu-id="54e60-127">Rununr.</span><span class="sxs-lookup"><span data-stu-id="54e60-127">Batch No.</span></span> |
|------------------|-------------|------|-----------|-----------|
| <span data-ttu-id="54e60-128">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="54e60-128">Cost object</span></span>      | <span data-ttu-id="54e60-129">x</span><span class="sxs-lookup"><span data-stu-id="54e60-129">x</span></span>           | <span data-ttu-id="54e60-130">x</span><span class="sxs-lookup"><span data-stu-id="54e60-130">x</span></span>    |           |           |
| <span data-ttu-id="54e60-131">Birgðahlutur</span><span class="sxs-lookup"><span data-stu-id="54e60-131">Inventory object</span></span> | <span data-ttu-id="54e60-132">x</span><span class="sxs-lookup"><span data-stu-id="54e60-132">x</span></span>           | <span data-ttu-id="54e60-133">x</span><span class="sxs-lookup"><span data-stu-id="54e60-133">x</span></span>    |  <span data-ttu-id="54e60-134">x</span><span class="sxs-lookup"><span data-stu-id="54e60-134">x</span></span>        | <span data-ttu-id="54e60-135">x</span><span class="sxs-lookup"><span data-stu-id="54e60-135">x</span></span>         |

## <a name="accumulation-of-costs-and-quantities"></a><span data-ttu-id="54e60-136">Uppsöfnun á kostnaði og magni</span><span class="sxs-lookup"><span data-stu-id="54e60-136">Accumulation of costs and quantities</span></span>
-   <span data-ttu-id="54e60-137">Gildið í reitnum **Gildi** er samtala eftirfarandi gilda:</span><span class="sxs-lookup"><span data-stu-id="54e60-137">The value in the **Value** fieldis a sum of the following values:</span></span>
    -   <span data-ttu-id="54e60-138">Efnisleg kostnaðarupphæð</span><span class="sxs-lookup"><span data-stu-id="54e60-138">Physical cost amount</span></span>
    -   <span data-ttu-id="54e60-139">Fjárhagsleg kostnaðarupphæð</span><span class="sxs-lookup"><span data-stu-id="54e60-139">Financial cost amount</span></span>
    -   <span data-ttu-id="54e60-140">Leiðréttingar</span><span class="sxs-lookup"><span data-stu-id="54e60-140">Adjustments</span></span>
-   <span data-ttu-id="54e60-141">Gildið í reitnum **Magn** er samtala eftirfarandi gilda:</span><span class="sxs-lookup"><span data-stu-id="54e60-141">The value in the **Quantity** field is a sum of the following values:</span></span>
    -   <span data-ttu-id="54e60-142">Móttekið</span><span class="sxs-lookup"><span data-stu-id="54e60-142">Received</span></span>
    -   <span data-ttu-id="54e60-143">Frádregið</span><span class="sxs-lookup"><span data-stu-id="54e60-143">Deducted</span></span>
    -   <span data-ttu-id="54e60-144">Bókað magn</span><span class="sxs-lookup"><span data-stu-id="54e60-144">Posted quantity</span></span>
-   <span data-ttu-id="54e60-145">Reiturinn **Meðaleiningarkostnaður** er reiknaður reitur.</span><span class="sxs-lookup"><span data-stu-id="54e60-145">The **Average unit cost** field is a calculated field.</span></span> <span data-ttu-id="54e60-146">Gildið er reiknað með því að deila gildinu **Gildi** með gildinu **Magn**.</span><span class="sxs-lookup"><span data-stu-id="54e60-146">The value is calculated by dividing the **Value** value by the **Quantity** value.</span></span>

<span data-ttu-id="54e60-147">**Ábending:** Færibreytan **Taka efnislegt virði með** hefur engin áhrif á fyrri útreikninga.</span><span class="sxs-lookup"><span data-stu-id="54e60-147">**Note:** The **Include physical value **parameter has no effect on the preceding calculations.</span></span>

<a name="see-also"></a><span data-ttu-id="54e60-148">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="54e60-148">See also</span></span>
--------

[<span data-ttu-id="54e60-149">Afurðavíddaflokkur</span><span class="sxs-lookup"><span data-stu-id="54e60-149">Product dimension group</span></span>](https://technet.microsoft.com/en-us/library/aa499382.aspx)

[<span data-ttu-id="54e60-150">Geymsluvíddarflokkur</span><span class="sxs-lookup"><span data-stu-id="54e60-150">Storage dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209317.aspx)

[<span data-ttu-id="54e60-151">Rakningarvíddarflokkur</span><span class="sxs-lookup"><span data-stu-id="54e60-151">Tracking dimension group</span></span>](https://technet.microsoft.com/en-us/library/hh209465.aspx)

[<span data-ttu-id="54e60-152">Nýjungar eða breytingar</span><span class="sxs-lookup"><span data-stu-id="54e60-152">What's new or changed</span></span>](../../fin-and-ops/get-started/whats-new-changed.md)

[<span data-ttu-id="54e60-153">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="54e60-153">Cost entries</span></span>](cost-entries.md)




