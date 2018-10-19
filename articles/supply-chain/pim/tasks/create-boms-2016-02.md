--- 
title: "Stofna uppskriftir (febrúar 2016)"
description: "Þetta verk einblínir á að búa til uppbygging uppskriftar fyrir fullunnin vara og hálfunnin vara."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 6c5cfb8aae1a61d14f7a7969f688cb282530840d
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---
# <a name="create-boms-february-2016"></a><span data-ttu-id="b1cac-103">Stofna uppskriftir (febrúar 2016)</span><span class="sxs-lookup"><span data-stu-id="b1cac-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b1cac-104">Þetta verk einblínir á að búa til uppbygging uppskriftar fyrir fullunnin vara og hálfunnin vara.</span><span class="sxs-lookup"><span data-stu-id="b1cac-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="b1cac-105">Þetta er fjórða verkið í línunni Útreikningur uppskrifta.</span><span class="sxs-lookup"><span data-stu-id="b1cac-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="b1cac-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="b1cac-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="b1cac-107">Búa til uppskrift fyrir hálfunnin vara</span><span class="sxs-lookup"><span data-stu-id="b1cac-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="b1cac-108">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="b1cac-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="b1cac-109">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="b1cac-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b1cac-110">Veljið vörunúmer BOM_2.</span><span class="sxs-lookup"><span data-stu-id="b1cac-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="b1cac-111">Smellið á tæknifræðingur á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="b1cac-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="b1cac-112">Smellt er á uppskriftarútgáfur.</span><span class="sxs-lookup"><span data-stu-id="b1cac-112">Click BOM versions.</span></span>
5. <span data-ttu-id="b1cac-113">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="b1cac-113">Click New.</span></span>
6. <span data-ttu-id="b1cac-114">Smellt er á uppskrift og uppskriftarútgáfa</span><span class="sxs-lookup"><span data-stu-id="b1cac-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="b1cac-115">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b1cac-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="b1cac-116">Til dæmis, slá inn BOM_2.</span><span class="sxs-lookup"><span data-stu-id="b1cac-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="b1cac-117">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="b1cac-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="b1cac-118">Í þessu dæmi, slá inn eða velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="b1cac-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="b1cac-119">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b1cac-119">Click OK.</span></span>
10. <span data-ttu-id="b1cac-120">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="b1cac-120">Click New.</span></span>
11. <span data-ttu-id="b1cac-121">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b1cac-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="b1cac-122">Í þessu dæmi, slá inn ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="b1cac-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="b1cac-123">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="b1cac-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="b1cac-124">Í þessu dæmi, slá inn eða velja 11.</span><span class="sxs-lookup"><span data-stu-id="b1cac-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="b1cac-125">Smellið á Haus.</span><span class="sxs-lookup"><span data-stu-id="b1cac-125">Click Header.</span></span>
14. <span data-ttu-id="b1cac-126">Smellt er á Samþykki til að samþykkja uppskriftir.</span><span class="sxs-lookup"><span data-stu-id="b1cac-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="b1cac-127">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b1cac-127">Click OK.</span></span>
16. <span data-ttu-id="b1cac-128">Smellið á Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="b1cac-128">Click Approve.</span></span>
    * <span data-ttu-id="b1cac-129">Hnappur Samþykkja er á verkfæraslá í hlutanum Uppskriftaútgáfur.</span><span class="sxs-lookup"><span data-stu-id="b1cac-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="b1cac-130">Ef hann sést ekki, smella á Haus efst hægra megin á síðunni Uppskriftir til að birta Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="b1cac-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="b1cac-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b1cac-131">Click OK.</span></span>
18. <span data-ttu-id="b1cac-132">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="b1cac-132">Click Activate.</span></span>
19. <span data-ttu-id="b1cac-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1cac-133">Close the page.</span></span>
20. <span data-ttu-id="b1cac-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1cac-134">Close the page.</span></span>
21. <span data-ttu-id="b1cac-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1cac-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="b1cac-136">Búa til uppskrift fyrir fullunnin vara</span><span class="sxs-lookup"><span data-stu-id="b1cac-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="b1cac-137">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="b1cac-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b1cac-138">Veljið vörunúmer BOM_1.</span><span class="sxs-lookup"><span data-stu-id="b1cac-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="b1cac-139">Smellið á tæknifræðingur á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="b1cac-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="b1cac-140">Smellt er á uppskriftarútgáfur.</span><span class="sxs-lookup"><span data-stu-id="b1cac-140">Click BOM versions.</span></span>
4. <span data-ttu-id="b1cac-141">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="b1cac-141">Click New.</span></span>
5. <span data-ttu-id="b1cac-142">Smellt er á uppskrift og uppskriftarútgáfa</span><span class="sxs-lookup"><span data-stu-id="b1cac-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="b1cac-143">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b1cac-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="b1cac-144">Til dæmis, slá inn BOM_1.</span><span class="sxs-lookup"><span data-stu-id="b1cac-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="b1cac-145">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="b1cac-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="b1cac-146">Í þessu dæmi, slá inn eða velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="b1cac-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="b1cac-147">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b1cac-147">Click OK.</span></span>
9. <span data-ttu-id="b1cac-148">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="b1cac-148">Click New.</span></span>
10. <span data-ttu-id="b1cac-149">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b1cac-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="b1cac-150">Í þessu dæmi, slá inn ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="b1cac-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="b1cac-151">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="b1cac-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="b1cac-152">Í þessu dæmi, velja 11.</span><span class="sxs-lookup"><span data-stu-id="b1cac-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="b1cac-153">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="b1cac-153">Click New.</span></span>
13. <span data-ttu-id="b1cac-154">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b1cac-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="b1cac-155">Í þessu dæmi, slá inn ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="b1cac-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="b1cac-156">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="b1cac-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="b1cac-157">Í þessu dæmi, slá inn eða velja 11.</span><span class="sxs-lookup"><span data-stu-id="b1cac-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="b1cac-158">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="b1cac-158">Click New.</span></span>
16. <span data-ttu-id="b1cac-159">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b1cac-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="b1cac-160">Í þessu dæmi, slá inn BOM_2.</span><span class="sxs-lookup"><span data-stu-id="b1cac-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="b1cac-161">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="b1cac-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="b1cac-162">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="b1cac-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="b1cac-163">Í þessu dæmi, slá inn eða velja vörugeymsla 11.</span><span class="sxs-lookup"><span data-stu-id="b1cac-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="b1cac-164">Smellið á Haus.</span><span class="sxs-lookup"><span data-stu-id="b1cac-164">Click Header.</span></span>
20. <span data-ttu-id="b1cac-165">Smellt er á Samþykki til að samþykkja uppskriftir.</span><span class="sxs-lookup"><span data-stu-id="b1cac-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="b1cac-166">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b1cac-166">Click OK.</span></span>
22. <span data-ttu-id="b1cac-167">Smellið á Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="b1cac-167">Click Approve.</span></span>
    * <span data-ttu-id="b1cac-168">Hnappur Samþykkja er á verkfæraslá í hlutanum Uppskriftaútgáfur.</span><span class="sxs-lookup"><span data-stu-id="b1cac-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="b1cac-169">Ef hann sést ekki, smella á Haus efst hægra megin á síðunni Uppskriftir til að birta Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="b1cac-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="b1cac-170">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b1cac-170">Click OK.</span></span>
24. <span data-ttu-id="b1cac-171">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="b1cac-171">Click Activate.</span></span>
25. <span data-ttu-id="b1cac-172">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1cac-172">Close the page.</span></span>
26. <span data-ttu-id="b1cac-173">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1cac-173">Close the page.</span></span>
27. <span data-ttu-id="b1cac-174">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1cac-174">Close the page.</span></span>


