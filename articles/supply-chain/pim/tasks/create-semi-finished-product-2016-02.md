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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 39fb652d704da33d24a206da2c18cc2a7a50e9e4
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844514"
---
# <a name="create-a-semi-finished-product-february-2016"></a><span data-ttu-id="7127f-103">Stofna hálfunnin vara (febrúar 2016)</span><span class="sxs-lookup"><span data-stu-id="7127f-103">Create a semi-finished product (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7127f-104">Þetta verk einblínir á að búa til hálfunnin vara.</span><span class="sxs-lookup"><span data-stu-id="7127f-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="7127f-105">Þetta er annað verkið í línunni Útreikningur uppskrifta.</span><span class="sxs-lookup"><span data-stu-id="7127f-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="7127f-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="7127f-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="7127f-107">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="7127f-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="7127f-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7127f-108">Click New.</span></span>
3. <span data-ttu-id="7127f-109">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7127f-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="7127f-110">Í þessu dæmi, slá inn BOM_2.</span><span class="sxs-lookup"><span data-stu-id="7127f-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="7127f-111">Í reitinn Vörulíkanaflokkur skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="7127f-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="7127f-112">Veldu STD.</span><span class="sxs-lookup"><span data-stu-id="7127f-112">Select STD.</span></span> <span data-ttu-id="7127f-113">STD stendur fyrir staðalkostnaður og er mest notaða líkan þegar unnið með kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="7127f-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="7127f-114">Í reitinn Vöruflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7127f-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="7127f-115">Veljið t.d. Hljóðvinnsla.</span><span class="sxs-lookup"><span data-stu-id="7127f-115">For example, select Audio.</span></span> <span data-ttu-id="7127f-116">Þetta hefur engin áhrif á kostnaðarútreikningur.</span><span class="sxs-lookup"><span data-stu-id="7127f-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="7127f-117">Í reitinn Geymsluvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7127f-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7127f-118">Velja SiteWH.</span><span class="sxs-lookup"><span data-stu-id="7127f-118">Select SiteWH.</span></span> <span data-ttu-id="7127f-119">Aðeins Svæði og vöruhús verður notað í þessu dæmi.</span><span class="sxs-lookup"><span data-stu-id="7127f-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="7127f-120">Í reitinn Rakningarvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7127f-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7127f-121">Rakningarvíddir verða ekki notað í þessu dæmi, velja skal Ekkert.</span><span class="sxs-lookup"><span data-stu-id="7127f-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="7127f-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7127f-122">Click OK.</span></span>
9. <span data-ttu-id="7127f-123">Á Aðgerðasvæðinu skal smella á Stjórna birgðum.</span><span class="sxs-lookup"><span data-stu-id="7127f-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="7127f-124">Smellt er á sjálfgefnar pöntunarstillingar.</span><span class="sxs-lookup"><span data-stu-id="7127f-124">Click Default order settings.</span></span>
11. <span data-ttu-id="7127f-125">Í svæði Sjálfgefin pöntunargerð skal velja „Framleiðsla“.</span><span class="sxs-lookup"><span data-stu-id="7127f-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="7127f-126">Vegna þess að þetta er hálfunnin vara sem verður framleidd, velja Framleiðsla.</span><span class="sxs-lookup"><span data-stu-id="7127f-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="7127f-127">Í svæði „Innkaupasvæði“ slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7127f-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="7127f-128">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7127f-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="7127f-129">Í svæði Birgðasvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7127f-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="7127f-130">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7127f-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="7127f-131">Í svæði Sölusvæði slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7127f-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="7127f-132">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7127f-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="7127f-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7127f-133">Close the page.</span></span>
16. <span data-ttu-id="7127f-134">Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.</span><span class="sxs-lookup"><span data-stu-id="7127f-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="7127f-135">Smellt er á Verð vöru.</span><span class="sxs-lookup"><span data-stu-id="7127f-135">Click Item price.</span></span>
18. <span data-ttu-id="7127f-136">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7127f-136">Click New.</span></span>
19. <span data-ttu-id="7127f-137">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="7127f-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="7127f-138">Í svæði Útgáfa, slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7127f-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="7127f-139">Í þessu dæmi, velja Útgáfa 10.</span><span class="sxs-lookup"><span data-stu-id="7127f-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="7127f-140">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="7127f-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7127f-141">Í þessu dæmi skal velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7127f-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="7127f-142">Stilla verð á „10“.</span><span class="sxs-lookup"><span data-stu-id="7127f-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="7127f-143">Í þessu dæmi, slá inn kostnaðarverð 10.</span><span class="sxs-lookup"><span data-stu-id="7127f-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="7127f-144">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="7127f-144">Click Save.</span></span>
24. <span data-ttu-id="7127f-145">Smellt er á Virk vöruverð.</span><span class="sxs-lookup"><span data-stu-id="7127f-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="7127f-146">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7127f-146">Close the page.</span></span>
26. <span data-ttu-id="7127f-147">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7127f-147">Close the page.</span></span>
27. <span data-ttu-id="7127f-148">Smellt er á BOM_2 til að opna það.</span><span class="sxs-lookup"><span data-stu-id="7127f-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="7127f-149">Stækka hlutann Vinna með kostnað.</span><span class="sxs-lookup"><span data-stu-id="7127f-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="7127f-150">Sláið inn eða veldu gildi í reitnum Kostnaðarflokkur.</span><span class="sxs-lookup"><span data-stu-id="7127f-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="7127f-151">Í þessu dæmi, velja Kostnaðarflokkur M1.</span><span class="sxs-lookup"><span data-stu-id="7127f-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="7127f-152">Nota má flýtileiðina til að vista færslu.</span><span class="sxs-lookup"><span data-stu-id="7127f-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="7127f-153">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7127f-153">Close the page.</span></span>

