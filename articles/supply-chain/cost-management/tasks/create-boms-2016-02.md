--- 
title: "Stofna uppskriftir (aðeins febrúar 2016)"
description: "Þetta verk einblínir á að búa til uppbygging uppskriftar fyrir fullunnin vara og hálfunnin vara."
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
ms.openlocfilehash: f132a3865b180a74d328ebc76ca29b2fc8aee85f
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---
# <a name="create-boms-february-2016-only"></a><span data-ttu-id="7e4a9-103">Stofna uppskriftir (aðeins febrúar 2016)</span><span class="sxs-lookup"><span data-stu-id="7e4a9-103">Create BOMs (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7e4a9-104">Þetta verk einblínir á að búa til uppbygging uppskriftar fyrir fullunnin vara og hálfunnin vara.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="7e4a9-105">Þetta er fjórða verkið í línunni Útreikningur uppskrifta.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="7e4a9-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="7e4a9-107">Búa til uppskrift fyrir hálfunnin vara</span><span class="sxs-lookup"><span data-stu-id="7e4a9-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="7e4a9-108">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="7e4a9-109">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7e4a9-110">Veljið vörunúmer BOM_2.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="7e4a9-111">Smellið á tæknifræðingur á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="7e4a9-112">Smellt er á uppskriftarútgáfur.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-112">Click BOM versions.</span></span>
5. <span data-ttu-id="7e4a9-113">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-113">Click New.</span></span>
6. <span data-ttu-id="7e4a9-114">Smellt er á uppskrift og uppskriftarútgáfa</span><span class="sxs-lookup"><span data-stu-id="7e4a9-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="7e4a9-115">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="7e4a9-116">Til dæmis, slá inn BOM_2.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="7e4a9-117">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7e4a9-118">Í þessu dæmi, slá inn eða velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="7e4a9-119">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-119">Click OK.</span></span>
10. <span data-ttu-id="7e4a9-120">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-120">Click New.</span></span>
11. <span data-ttu-id="7e4a9-121">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="7e4a9-122">Í þessu dæmi, slá inn ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="7e4a9-123">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="7e4a9-124">Í þessu dæmi, slá inn eða velja 11.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="7e4a9-125">Smellið á Haus.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-125">Click Header.</span></span>
14. <span data-ttu-id="7e4a9-126">Smellt er á Samþykki til að samþykkja uppskriftir.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="7e4a9-127">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-127">Click OK.</span></span>
16. <span data-ttu-id="7e4a9-128">Smellið á Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-128">Click Approve.</span></span>
    * <span data-ttu-id="7e4a9-129">Hnappur Samþykkja er á verkfæraslá í hlutanum Uppskriftaútgáfur.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="7e4a9-130">Ef hann sést ekki, smella á Haus efst hægra megin á síðunni Uppskriftir til að birta Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="7e4a9-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-131">Click OK.</span></span>
18. <span data-ttu-id="7e4a9-132">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-132">Click Activate.</span></span>
19. <span data-ttu-id="7e4a9-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-133">Close the page.</span></span>
20. <span data-ttu-id="7e4a9-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-134">Close the page.</span></span>
21. <span data-ttu-id="7e4a9-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="7e4a9-136">Búa til uppskrift fyrir fullunnin vara</span><span class="sxs-lookup"><span data-stu-id="7e4a9-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="7e4a9-137">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7e4a9-138">Veljið vörunúmer BOM_1.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="7e4a9-139">Smellið á tæknifræðingur á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="7e4a9-140">Smellt er á uppskriftarútgáfur.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-140">Click BOM versions.</span></span>
4. <span data-ttu-id="7e4a9-141">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-141">Click New.</span></span>
5. <span data-ttu-id="7e4a9-142">Smellt er á uppskrift og uppskriftarútgáfa</span><span class="sxs-lookup"><span data-stu-id="7e4a9-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="7e4a9-143">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="7e4a9-144">Til dæmis, slá inn BOM_1.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="7e4a9-145">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7e4a9-146">Í þessu dæmi, slá inn eða velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="7e4a9-147">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-147">Click OK.</span></span>
9. <span data-ttu-id="7e4a9-148">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-148">Click New.</span></span>
10. <span data-ttu-id="7e4a9-149">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="7e4a9-150">Í þessu dæmi, slá inn ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="7e4a9-151">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="7e4a9-152">Í þessu dæmi, velja 11.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="7e4a9-153">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-153">Click New.</span></span>
13. <span data-ttu-id="7e4a9-154">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="7e4a9-155">Í þessu dæmi, slá inn ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="7e4a9-156">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="7e4a9-157">Í þessu dæmi, slá inn eða velja 11.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="7e4a9-158">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-158">Click New.</span></span>
16. <span data-ttu-id="7e4a9-159">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="7e4a9-160">Í þessu dæmi, slá inn BOM_2.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="7e4a9-161">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="7e4a9-162">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="7e4a9-163">Í þessu dæmi, slá inn eða velja vörugeymsla 11.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="7e4a9-164">Smellið á Haus.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-164">Click Header.</span></span>
20. <span data-ttu-id="7e4a9-165">Smellt er á Samþykki til að samþykkja uppskriftir.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="7e4a9-166">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-166">Click OK.</span></span>
22. <span data-ttu-id="7e4a9-167">Smellið á Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-167">Click Approve.</span></span>
    * <span data-ttu-id="7e4a9-168">Hnappur Samþykkja er á verkfæraslá í hlutanum Uppskriftaútgáfur.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="7e4a9-169">Ef hann sést ekki, smella á Haus efst hægra megin á síðunni Uppskriftir til að birta Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="7e4a9-170">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-170">Click OK.</span></span>
24. <span data-ttu-id="7e4a9-171">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-171">Click Activate.</span></span>
25. <span data-ttu-id="7e4a9-172">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-172">Close the page.</span></span>
26. <span data-ttu-id="7e4a9-173">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-173">Close the page.</span></span>
27. <span data-ttu-id="7e4a9-174">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7e4a9-174">Close the page.</span></span>


