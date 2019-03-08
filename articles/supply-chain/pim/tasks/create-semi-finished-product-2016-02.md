---
title: Stofna hálfunnin vara (febrúar 2016)
description: Þetta verk einblínir á að búa til hálfunnin vara.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9caeae552471eed1cb1d8630f387ca31107fcece
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "362856"
---
# <a name="create-a-semi-finished-product-february-2016"></a><span data-ttu-id="7eb95-103">Stofna hálfunnin vara (febrúar 2016)</span><span class="sxs-lookup"><span data-stu-id="7eb95-103">Create a semi-finished product (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7eb95-104">Þetta verk einblínir á að búa til hálfunnin vara.</span><span class="sxs-lookup"><span data-stu-id="7eb95-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="7eb95-105">Þetta er annað verkið í línunni Útreikningur uppskrifta.</span><span class="sxs-lookup"><span data-stu-id="7eb95-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="7eb95-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="7eb95-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="7eb95-107">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="7eb95-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="7eb95-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7eb95-108">Click New.</span></span>
3. <span data-ttu-id="7eb95-109">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7eb95-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="7eb95-110">Í þessu dæmi, slá inn BOM_2.</span><span class="sxs-lookup"><span data-stu-id="7eb95-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="7eb95-111">Í reitinn Vörulíkanaflokkur skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="7eb95-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="7eb95-112">Veldu STD.</span><span class="sxs-lookup"><span data-stu-id="7eb95-112">Select STD.</span></span> <span data-ttu-id="7eb95-113">STD stendur fyrir staðalkostnaður og er mest notaða líkan þegar unnið með kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="7eb95-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="7eb95-114">Í reitinn Vöruflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7eb95-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="7eb95-115">Veljið t.d. Hljóðvinnsla.</span><span class="sxs-lookup"><span data-stu-id="7eb95-115">For example, select Audio.</span></span> <span data-ttu-id="7eb95-116">Þetta hefur engin áhrif á kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="7eb95-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="7eb95-117">Í reitinn Geymsluvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7eb95-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7eb95-118">Velja SiteWH.</span><span class="sxs-lookup"><span data-stu-id="7eb95-118">Select SiteWH.</span></span> <span data-ttu-id="7eb95-119">Aðeins Svæði og vöruhús verður notað í þessu dæmi.</span><span class="sxs-lookup"><span data-stu-id="7eb95-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="7eb95-120">Í reitinn Rakningarvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7eb95-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7eb95-121">Rakningarvíddir verða ekki notað í þessu dæmi, velja skal Ekkert.</span><span class="sxs-lookup"><span data-stu-id="7eb95-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="7eb95-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7eb95-122">Click OK.</span></span>
9. <span data-ttu-id="7eb95-123">Á Aðgerðasvæðinu skal smella á Stjórna birgðum.</span><span class="sxs-lookup"><span data-stu-id="7eb95-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="7eb95-124">Smellt er á sjálfgefnar pöntunarstillingar.</span><span class="sxs-lookup"><span data-stu-id="7eb95-124">Click Default order settings.</span></span>
11. <span data-ttu-id="7eb95-125">Í svæði Sjálfgefin pöntunargerð skal velja „Framleiðsla“.</span><span class="sxs-lookup"><span data-stu-id="7eb95-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="7eb95-126">Vegna þess að þetta er hálfunnin vara sem verður framleidd, velja Framleiðsla.</span><span class="sxs-lookup"><span data-stu-id="7eb95-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="7eb95-127">Í svæði „Innkaupasvæði“ slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7eb95-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="7eb95-128">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7eb95-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="7eb95-129">Í svæði Birgðasvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7eb95-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="7eb95-130">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7eb95-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="7eb95-131">Í svæði Sölusvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7eb95-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="7eb95-132">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7eb95-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="7eb95-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7eb95-133">Close the page.</span></span>
16. <span data-ttu-id="7eb95-134">Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.</span><span class="sxs-lookup"><span data-stu-id="7eb95-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="7eb95-135">Smellt er á Verð vöru.</span><span class="sxs-lookup"><span data-stu-id="7eb95-135">Click Item price.</span></span>
18. <span data-ttu-id="7eb95-136">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7eb95-136">Click New.</span></span>
19. <span data-ttu-id="7eb95-137">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="7eb95-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="7eb95-138">Í svæði Útgáfa, slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7eb95-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="7eb95-139">Í þessu dæmi, velja Útgáfa 10.</span><span class="sxs-lookup"><span data-stu-id="7eb95-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="7eb95-140">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="7eb95-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7eb95-141">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7eb95-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="7eb95-142">Stilla verð á „10“.</span><span class="sxs-lookup"><span data-stu-id="7eb95-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="7eb95-143">Í þessu dæmi, slá inn kostnaðarverð 10.</span><span class="sxs-lookup"><span data-stu-id="7eb95-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="7eb95-144">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="7eb95-144">Click Save.</span></span>
24. <span data-ttu-id="7eb95-145">Smellt er á Virk vöruverð.</span><span class="sxs-lookup"><span data-stu-id="7eb95-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="7eb95-146">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7eb95-146">Close the page.</span></span>
26. <span data-ttu-id="7eb95-147">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7eb95-147">Close the page.</span></span>
27. <span data-ttu-id="7eb95-148">Smellt er á BOM_2 til að opna það.</span><span class="sxs-lookup"><span data-stu-id="7eb95-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="7eb95-149">Stækka hlutann Vinna með kostnað.</span><span class="sxs-lookup"><span data-stu-id="7eb95-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="7eb95-150">Sláið inn eða veldu gildi í reitnum Kostnaðarflokkur.</span><span class="sxs-lookup"><span data-stu-id="7eb95-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="7eb95-151">Í þessu dæmi, velja Kostnaðarflokkur M1.</span><span class="sxs-lookup"><span data-stu-id="7eb95-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="7eb95-152">Nota má flýtileiðina til að vista færslu.</span><span class="sxs-lookup"><span data-stu-id="7eb95-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="7eb95-153">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7eb95-153">Close the page.</span></span>

