---
title: Stofna uppskriftir (febrúar 2016)
description: Þetta verk einblínir á að búa til uppbygging uppskriftar fyrir fullunnin vara og hálfunnin vara.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c5cfb8aae1a61d14f7a7969f688cb282530840d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568559"
---
# <a name="create-boms-february-2016"></a><span data-ttu-id="2cc0f-103">Stofna uppskriftir (febrúar 2016)</span><span class="sxs-lookup"><span data-stu-id="2cc0f-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2cc0f-104">Þetta verk einblínir á að búa til uppbygging uppskriftar fyrir fullunnin vara og hálfunnin vara.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="2cc0f-105">Þetta er fjórða verkið í línunni Útreikningur uppskrifta.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="2cc0f-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="2cc0f-107">Búa til uppskrift fyrir hálfunnin vara</span><span class="sxs-lookup"><span data-stu-id="2cc0f-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="2cc0f-108">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="2cc0f-109">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2cc0f-110">Veljið vörunúmer BOM_2.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="2cc0f-111">Smellið á tæknifræðingur á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="2cc0f-112">Smellt er á uppskriftarútgáfur.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-112">Click BOM versions.</span></span>
5. <span data-ttu-id="2cc0f-113">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-113">Click New.</span></span>
6. <span data-ttu-id="2cc0f-114">Smellt er á uppskrift og uppskriftarútgáfa</span><span class="sxs-lookup"><span data-stu-id="2cc0f-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="2cc0f-115">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="2cc0f-116">Til dæmis, slá inn BOM_2.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="2cc0f-117">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="2cc0f-118">Í þessu dæmi, slá inn eða velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="2cc0f-119">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-119">Click OK.</span></span>
10. <span data-ttu-id="2cc0f-120">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-120">Click New.</span></span>
11. <span data-ttu-id="2cc0f-121">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="2cc0f-122">Í þessu dæmi, slá inn ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="2cc0f-123">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="2cc0f-124">Í þessu dæmi, slá inn eða velja 11.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="2cc0f-125">Smellið á Haus.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-125">Click Header.</span></span>
14. <span data-ttu-id="2cc0f-126">Smellt er á Samþykki til að samþykkja uppskriftir.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="2cc0f-127">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-127">Click OK.</span></span>
16. <span data-ttu-id="2cc0f-128">Smellið á Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-128">Click Approve.</span></span>
    * <span data-ttu-id="2cc0f-129">Hnappur Samþykkja er á verkfæraslá í hlutanum Uppskriftaútgáfur.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="2cc0f-130">Ef hann sést ekki, smella á Haus efst hægra megin á síðunni Uppskriftir til að birta Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="2cc0f-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-131">Click OK.</span></span>
18. <span data-ttu-id="2cc0f-132">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-132">Click Activate.</span></span>
19. <span data-ttu-id="2cc0f-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-133">Close the page.</span></span>
20. <span data-ttu-id="2cc0f-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-134">Close the page.</span></span>
21. <span data-ttu-id="2cc0f-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="2cc0f-136">Búa til uppskrift fyrir fullunnin vara</span><span class="sxs-lookup"><span data-stu-id="2cc0f-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="2cc0f-137">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2cc0f-138">Veljið vörunúmer BOM_1.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="2cc0f-139">Smellið á tæknifræðingur á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="2cc0f-140">Smellt er á uppskriftarútgáfur.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-140">Click BOM versions.</span></span>
4. <span data-ttu-id="2cc0f-141">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-141">Click New.</span></span>
5. <span data-ttu-id="2cc0f-142">Smellt er á uppskrift og uppskriftarútgáfa</span><span class="sxs-lookup"><span data-stu-id="2cc0f-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="2cc0f-143">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="2cc0f-144">Til dæmis, slá inn BOM_1.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="2cc0f-145">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="2cc0f-146">Í þessu dæmi, slá inn eða velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="2cc0f-147">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-147">Click OK.</span></span>
9. <span data-ttu-id="2cc0f-148">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-148">Click New.</span></span>
10. <span data-ttu-id="2cc0f-149">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="2cc0f-150">Í þessu dæmi, slá inn ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="2cc0f-151">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="2cc0f-152">Í þessu dæmi, velja 11.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="2cc0f-153">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-153">Click New.</span></span>
13. <span data-ttu-id="2cc0f-154">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="2cc0f-155">Í þessu dæmi, slá inn ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="2cc0f-156">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="2cc0f-157">Í þessu dæmi, slá inn eða velja 11.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="2cc0f-158">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-158">Click New.</span></span>
16. <span data-ttu-id="2cc0f-159">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="2cc0f-160">Í þessu dæmi, slá inn BOM_2.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="2cc0f-161">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="2cc0f-162">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="2cc0f-163">Í þessu dæmi, slá inn eða velja vörugeymsla 11.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="2cc0f-164">Smellið á Haus.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-164">Click Header.</span></span>
20. <span data-ttu-id="2cc0f-165">Smellt er á Samþykki til að samþykkja uppskriftir.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="2cc0f-166">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-166">Click OK.</span></span>
22. <span data-ttu-id="2cc0f-167">Smellið á Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-167">Click Approve.</span></span>
    * <span data-ttu-id="2cc0f-168">Hnappur Samþykkja er á verkfæraslá í hlutanum Uppskriftaútgáfur.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="2cc0f-169">Ef hann sést ekki, smella á Haus efst hægra megin á síðunni Uppskriftir til að birta Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="2cc0f-170">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-170">Click OK.</span></span>
24. <span data-ttu-id="2cc0f-171">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-171">Click Activate.</span></span>
25. <span data-ttu-id="2cc0f-172">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-172">Close the page.</span></span>
26. <span data-ttu-id="2cc0f-173">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-173">Close the page.</span></span>
27. <span data-ttu-id="2cc0f-174">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="2cc0f-174">Close the page.</span></span>

