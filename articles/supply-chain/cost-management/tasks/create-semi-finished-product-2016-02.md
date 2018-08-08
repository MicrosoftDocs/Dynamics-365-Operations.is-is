--- 
title: "Stofna hálftilbúna afurð (aðeins febrúar 2016)"
description: "Þetta verk einblínir á að búa til hálfunnin vara."
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 76fcba3732879f85c9bf0faa6d2481b9c5313a17
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-semi-finished-product-february-2016-only"></a><span data-ttu-id="314c0-103">Stofna hálftilbúna afurð (aðeins febrúar 2016)</span><span class="sxs-lookup"><span data-stu-id="314c0-103">Create a semi-finished product (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="314c0-104">Þetta verk einblínir á að búa til hálfunnin vara.</span><span class="sxs-lookup"><span data-stu-id="314c0-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="314c0-105">Þetta er annað verkið í línunni Útreikningur uppskrifta.</span><span class="sxs-lookup"><span data-stu-id="314c0-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="314c0-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="314c0-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="314c0-107">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="314c0-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="314c0-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="314c0-108">Click New.</span></span>
3. <span data-ttu-id="314c0-109">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="314c0-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="314c0-110">Í þessu dæmi, slá inn BOM_2.</span><span class="sxs-lookup"><span data-stu-id="314c0-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="314c0-111">Í reitinn Vörulíkanaflokkur skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="314c0-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="314c0-112">Veldu STD.</span><span class="sxs-lookup"><span data-stu-id="314c0-112">Select STD.</span></span> <span data-ttu-id="314c0-113">STD stendur fyrir staðalkostnaður og er mest notaða líkan þegar unnið með kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="314c0-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="314c0-114">Í reitinn Vöruflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="314c0-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="314c0-115">Veljið t.d. Hljóðvinnsla.</span><span class="sxs-lookup"><span data-stu-id="314c0-115">For example, select Audio.</span></span> <span data-ttu-id="314c0-116">Þetta hefur engin áhrif á kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="314c0-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="314c0-117">Í reitinn Geymsluvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="314c0-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="314c0-118">Velja SiteWH.</span><span class="sxs-lookup"><span data-stu-id="314c0-118">Select SiteWH.</span></span> <span data-ttu-id="314c0-119">Aðeins Svæði og vöruhús verður notað í þessu dæmi.</span><span class="sxs-lookup"><span data-stu-id="314c0-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="314c0-120">Í reitinn Rakningarvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="314c0-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="314c0-121">Rakningarvíddir verða ekki notað í þessu dæmi, velja skal Ekkert.</span><span class="sxs-lookup"><span data-stu-id="314c0-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="314c0-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="314c0-122">Click OK.</span></span>
9. <span data-ttu-id="314c0-123">Á Aðgerðasvæðinu skal smella á Stjórna birgðum.</span><span class="sxs-lookup"><span data-stu-id="314c0-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="314c0-124">Smellt er á sjálfgefnar pöntunarstillingar.</span><span class="sxs-lookup"><span data-stu-id="314c0-124">Click Default order settings.</span></span>
11. <span data-ttu-id="314c0-125">Í svæði Sjálfgefin pöntunargerð skal velja „Framleiðsla“.</span><span class="sxs-lookup"><span data-stu-id="314c0-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="314c0-126">Vegna þess að þetta er hálfunnin vara sem verður framleidd, velja Framleiðsla.</span><span class="sxs-lookup"><span data-stu-id="314c0-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="314c0-127">Í svæði „Innkaupasvæði“ slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="314c0-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="314c0-128">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="314c0-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="314c0-129">Í svæði Birgðasvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="314c0-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="314c0-130">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="314c0-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="314c0-131">Í svæði Sölusvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="314c0-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="314c0-132">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="314c0-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="314c0-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="314c0-133">Close the page.</span></span>
16. <span data-ttu-id="314c0-134">Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.</span><span class="sxs-lookup"><span data-stu-id="314c0-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="314c0-135">Smellt er á Verð vöru.</span><span class="sxs-lookup"><span data-stu-id="314c0-135">Click Item price.</span></span>
18. <span data-ttu-id="314c0-136">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="314c0-136">Click New.</span></span>
19. <span data-ttu-id="314c0-137">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="314c0-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="314c0-138">Í svæði Útgáfa, slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="314c0-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="314c0-139">Í þessu dæmi, velja Útgáfa 10.</span><span class="sxs-lookup"><span data-stu-id="314c0-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="314c0-140">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="314c0-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="314c0-141">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="314c0-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="314c0-142">Stilla verð á „10“.</span><span class="sxs-lookup"><span data-stu-id="314c0-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="314c0-143">Í þessu dæmi, slá inn kostnaðarverð 10.</span><span class="sxs-lookup"><span data-stu-id="314c0-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="314c0-144">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="314c0-144">Click Save.</span></span>
24. <span data-ttu-id="314c0-145">Smellt er á Virk vöruverð.</span><span class="sxs-lookup"><span data-stu-id="314c0-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="314c0-146">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="314c0-146">Close the page.</span></span>
26. <span data-ttu-id="314c0-147">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="314c0-147">Close the page.</span></span>
27. <span data-ttu-id="314c0-148">Smellt er á BOM_2 til að opna það.</span><span class="sxs-lookup"><span data-stu-id="314c0-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="314c0-149">Stækka hlutann Vinna með kostnað.</span><span class="sxs-lookup"><span data-stu-id="314c0-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="314c0-150">Sláið inn eða veldu gildi í reitnum Kostnaðarflokkur.</span><span class="sxs-lookup"><span data-stu-id="314c0-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="314c0-151">Í þessu dæmi, velja Kostnaðarflokkur M1.</span><span class="sxs-lookup"><span data-stu-id="314c0-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="314c0-152">Nota má flýtileiðina til að vista færslu.</span><span class="sxs-lookup"><span data-stu-id="314c0-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="314c0-153">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="314c0-153">Close the page.</span></span>


