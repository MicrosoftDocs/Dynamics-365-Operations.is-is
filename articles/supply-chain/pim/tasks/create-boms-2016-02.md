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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0087c53d9cdc3bb65e6fa446c193c752d0f9b4fc
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845090"
---
# <a name="create-boms-february-2016"></a><span data-ttu-id="a4f27-103">Stofna uppskriftir (febrúar 2016)</span><span class="sxs-lookup"><span data-stu-id="a4f27-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a4f27-104">Þetta verk einblínir á að búa til uppbygging uppskriftar fyrir fullunnin vara og hálfunnin vara.</span><span class="sxs-lookup"><span data-stu-id="a4f27-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="a4f27-105">Þetta er fjórða verkið í línunni Útreikningur uppskrifta.</span><span class="sxs-lookup"><span data-stu-id="a4f27-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="a4f27-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="a4f27-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="a4f27-107">Búa til uppskrift fyrir hálfunnin vara</span><span class="sxs-lookup"><span data-stu-id="a4f27-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="a4f27-108">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="a4f27-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="a4f27-109">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="a4f27-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a4f27-110">Veljið vörunúmer BOM_2.</span><span class="sxs-lookup"><span data-stu-id="a4f27-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="a4f27-111">Smellið á tæknifræðingur á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="a4f27-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="a4f27-112">Smellt er á uppskriftarútgáfur.</span><span class="sxs-lookup"><span data-stu-id="a4f27-112">Click BOM versions.</span></span>
5. <span data-ttu-id="a4f27-113">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="a4f27-113">Click New.</span></span>
6. <span data-ttu-id="a4f27-114">Smellt er á uppskrift og uppskriftarútgáfa</span><span class="sxs-lookup"><span data-stu-id="a4f27-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="a4f27-115">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a4f27-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a4f27-116">Til dæmis, slá inn BOM_2.</span><span class="sxs-lookup"><span data-stu-id="a4f27-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="a4f27-117">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="a4f27-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="a4f27-118">Í þessu dæmi, slá inn eða velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="a4f27-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="a4f27-119">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a4f27-119">Click OK.</span></span>
10. <span data-ttu-id="a4f27-120">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="a4f27-120">Click New.</span></span>
11. <span data-ttu-id="a4f27-121">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a4f27-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a4f27-122">Í þessu dæmi, slá inn ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="a4f27-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="a4f27-123">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="a4f27-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a4f27-124">Í þessu dæmi, slá inn eða velja 11.</span><span class="sxs-lookup"><span data-stu-id="a4f27-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="a4f27-125">Smellið á Haus.</span><span class="sxs-lookup"><span data-stu-id="a4f27-125">Click Header.</span></span>
14. <span data-ttu-id="a4f27-126">Smellt er á Samþykki til að samþykkja uppskriftir.</span><span class="sxs-lookup"><span data-stu-id="a4f27-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="a4f27-127">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a4f27-127">Click OK.</span></span>
16. <span data-ttu-id="a4f27-128">Smellið á Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="a4f27-128">Click Approve.</span></span>
    * <span data-ttu-id="a4f27-129">Hnappur Samþykkja er á verkfæraslá í hlutanum Uppskriftaútgáfur.</span><span class="sxs-lookup"><span data-stu-id="a4f27-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="a4f27-130">Ef hann sést ekki, smella á Haus efst hægra megin á síðunni Uppskriftir til að birta Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="a4f27-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="a4f27-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a4f27-131">Click OK.</span></span>
18. <span data-ttu-id="a4f27-132">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="a4f27-132">Click Activate.</span></span>
19. <span data-ttu-id="a4f27-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a4f27-133">Close the page.</span></span>
20. <span data-ttu-id="a4f27-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a4f27-134">Close the page.</span></span>
21. <span data-ttu-id="a4f27-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a4f27-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="a4f27-136">Búa til uppskrift fyrir fullunnin vara</span><span class="sxs-lookup"><span data-stu-id="a4f27-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="a4f27-137">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="a4f27-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a4f27-138">Veljið vörunúmer BOM_1.</span><span class="sxs-lookup"><span data-stu-id="a4f27-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="a4f27-139">Smellið á tæknifræðingur á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="a4f27-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="a4f27-140">Smellt er á uppskriftarútgáfur.</span><span class="sxs-lookup"><span data-stu-id="a4f27-140">Click BOM versions.</span></span>
4. <span data-ttu-id="a4f27-141">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="a4f27-141">Click New.</span></span>
5. <span data-ttu-id="a4f27-142">Smellt er á uppskrift og uppskriftarútgáfa</span><span class="sxs-lookup"><span data-stu-id="a4f27-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="a4f27-143">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a4f27-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a4f27-144">Til dæmis, slá inn BOM_1.</span><span class="sxs-lookup"><span data-stu-id="a4f27-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="a4f27-145">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="a4f27-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="a4f27-146">Í þessu dæmi, slá inn eða velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="a4f27-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="a4f27-147">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a4f27-147">Click OK.</span></span>
9. <span data-ttu-id="a4f27-148">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="a4f27-148">Click New.</span></span>
10. <span data-ttu-id="a4f27-149">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a4f27-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a4f27-150">Í þessu dæmi, slá inn ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="a4f27-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="a4f27-151">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="a4f27-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a4f27-152">Í þessu dæmi, velja 11.</span><span class="sxs-lookup"><span data-stu-id="a4f27-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="a4f27-153">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="a4f27-153">Click New.</span></span>
13. <span data-ttu-id="a4f27-154">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a4f27-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a4f27-155">Í þessu dæmi, slá inn ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="a4f27-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="a4f27-156">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="a4f27-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a4f27-157">Í þessu dæmi, slá inn eða velja 11.</span><span class="sxs-lookup"><span data-stu-id="a4f27-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="a4f27-158">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="a4f27-158">Click New.</span></span>
16. <span data-ttu-id="a4f27-159">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a4f27-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="a4f27-160">Í þessu dæmi, slá inn BOM_2.</span><span class="sxs-lookup"><span data-stu-id="a4f27-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="a4f27-161">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="a4f27-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="a4f27-162">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="a4f27-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="a4f27-163">Í þessu dæmi, slá inn eða velja vörugeymsla 11.</span><span class="sxs-lookup"><span data-stu-id="a4f27-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="a4f27-164">Smellið á Haus.</span><span class="sxs-lookup"><span data-stu-id="a4f27-164">Click Header.</span></span>
20. <span data-ttu-id="a4f27-165">Smellt er á Samþykki til að samþykkja uppskriftir.</span><span class="sxs-lookup"><span data-stu-id="a4f27-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="a4f27-166">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a4f27-166">Click OK.</span></span>
22. <span data-ttu-id="a4f27-167">Smellið á Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="a4f27-167">Click Approve.</span></span>
    * <span data-ttu-id="a4f27-168">Hnappur Samþykkja er á verkfæraslá í hlutanum Uppskriftaútgáfur.</span><span class="sxs-lookup"><span data-stu-id="a4f27-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="a4f27-169">Ef hann sést ekki, smella á Haus efst hægra megin á síðunni Uppskriftir til að birta Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="a4f27-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="a4f27-170">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a4f27-170">Click OK.</span></span>
24. <span data-ttu-id="a4f27-171">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="a4f27-171">Click Activate.</span></span>
25. <span data-ttu-id="a4f27-172">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a4f27-172">Close the page.</span></span>
26. <span data-ttu-id="a4f27-173">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a4f27-173">Close the page.</span></span>
27. <span data-ttu-id="a4f27-174">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a4f27-174">Close the page.</span></span>

