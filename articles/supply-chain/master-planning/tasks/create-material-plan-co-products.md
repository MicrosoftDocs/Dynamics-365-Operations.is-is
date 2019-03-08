---
title: Stofna efnisáætlun fyrir aukaafurðir.
description: Framleiðslustjóri áætlar efnisþarfir fyrir vörur sem eru aukaafurðir formúlu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2958f1e5c2e8a0cfa9cc6312f688d3b11b8e013c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "337142"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="9a396-103">Stofna efnisáætlun fyrir aukaafurðir.</span><span class="sxs-lookup"><span data-stu-id="9a396-103">Create a material plan for co products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9a396-104">Framleiðslustjóri áætlar efnisþarfir fyrir vörur sem eru aukaafurðir formúlu.</span><span class="sxs-lookup"><span data-stu-id="9a396-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="9a396-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USP2.</span><span class="sxs-lookup"><span data-stu-id="9a396-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="9a396-106">Stofna þörf fyrir aukaafurð</span><span class="sxs-lookup"><span data-stu-id="9a396-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="9a396-107">Farðu í Sjálfgefið mælaborð.</span><span class="sxs-lookup"><span data-stu-id="9a396-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="9a396-108">Smellt er á Vinnsla og fyrirspurnir sölupantana.</span><span class="sxs-lookup"><span data-stu-id="9a396-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="9a396-109">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="9a396-109">Click New.</span></span>
4. <span data-ttu-id="9a396-110">Smellt er á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="9a396-110">Click Sales order.</span></span>
5. <span data-ttu-id="9a396-111">Í reitinn Reikningur viðskiptavinar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9a396-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="9a396-112">Dæmi: US-001</span><span class="sxs-lookup"><span data-stu-id="9a396-112">Example: US-001</span></span>  
6. <span data-ttu-id="9a396-113">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9a396-113">Click OK.</span></span>
7. <span data-ttu-id="9a396-114">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9a396-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="9a396-115">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="9a396-115">Example: P6003</span></span>  
8. <span data-ttu-id="9a396-116">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="9a396-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="9a396-117">Til dæmis: 50000.</span><span class="sxs-lookup"><span data-stu-id="9a396-117">Example: 50000</span></span>  
9. <span data-ttu-id="9a396-118">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9a396-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="9a396-119">Búa til efnisáætlun fyrir aukaafurðir</span><span class="sxs-lookup"><span data-stu-id="9a396-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="9a396-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9a396-120">Close the page.</span></span>
2. <span data-ttu-id="9a396-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9a396-121">Close the page.</span></span>
3. <span data-ttu-id="9a396-122">Smellt er á aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="9a396-122">Click Master planning.</span></span>
4. <span data-ttu-id="9a396-123">Í reitnum Áætlun skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="9a396-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="9a396-124">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9a396-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9a396-125">Dæmi: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="9a396-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="9a396-126">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="9a396-126">Click Run.</span></span>
7. <span data-ttu-id="9a396-127">Útvíkka eða draga saman Færslur sem á að taka með hluta.</span><span class="sxs-lookup"><span data-stu-id="9a396-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="9a396-128">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="9a396-128">Click Filter.</span></span>
9. <span data-ttu-id="9a396-129">Á listanum, Velja línuna fyrir svæðið = vörunúmer</span><span class="sxs-lookup"><span data-stu-id="9a396-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="9a396-130">Í reitinn Skilyrði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9a396-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="9a396-131">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="9a396-131">Example: P6003</span></span>  
11. <span data-ttu-id="9a396-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9a396-132">Click OK.</span></span>
12. <span data-ttu-id="9a396-133">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9a396-133">Click OK.</span></span>
13. <span data-ttu-id="9a396-134">Smellt er á Áætlaðar pantanir.</span><span class="sxs-lookup"><span data-stu-id="9a396-134">Click Planned orders.</span></span>
14. <span data-ttu-id="9a396-135">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="9a396-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9a396-136">Til dæmis, sía svæðið vörunúmer með gildið 'P6000'.</span><span class="sxs-lookup"><span data-stu-id="9a396-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="9a396-137">Sía eftir formúluvöru sem hefur aukaafurð vöru sem stofnuð var sölupöntun fyrir.</span><span class="sxs-lookup"><span data-stu-id="9a396-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="9a396-138">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="9a396-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9a396-139">Velja allar línur sem sían skilaði.</span><span class="sxs-lookup"><span data-stu-id="9a396-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="9a396-140">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9a396-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="9a396-141">Útvíkka eða draga saman hlutann Þarfarakning.</span><span class="sxs-lookup"><span data-stu-id="9a396-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="9a396-142">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9a396-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9a396-143">Áætluð pöntun er fest við sölupöntun fyrir aukaafurðina.</span><span class="sxs-lookup"><span data-stu-id="9a396-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="9a396-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9a396-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="9a396-145">Stofna þörf fyrir aukaafurð</span><span class="sxs-lookup"><span data-stu-id="9a396-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="9a396-146">Farðu í Sjálfgefið mælaborð.</span><span class="sxs-lookup"><span data-stu-id="9a396-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="9a396-147">Smellt er á Vinnsla og fyrirspurnir sölupantana.</span><span class="sxs-lookup"><span data-stu-id="9a396-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="9a396-148">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="9a396-148">Click New.</span></span>
4. <span data-ttu-id="9a396-149">Smellt er á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="9a396-149">Click Sales order.</span></span>
5. <span data-ttu-id="9a396-150">Í reitinn Reikningur viðskiptavinar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9a396-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="9a396-151">Dæmi: US-001</span><span class="sxs-lookup"><span data-stu-id="9a396-151">Example: US-001</span></span>  
6. <span data-ttu-id="9a396-152">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9a396-152">Click OK.</span></span>
7. <span data-ttu-id="9a396-153">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9a396-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="9a396-154">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="9a396-154">Example: P6003</span></span>  
8. <span data-ttu-id="9a396-155">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="9a396-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="9a396-156">Til dæmis: 50000.</span><span class="sxs-lookup"><span data-stu-id="9a396-156">Example: 50000</span></span>  
9. <span data-ttu-id="9a396-157">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9a396-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="9a396-158">Búa til efnisáætlun fyrir aukaafurðir</span><span class="sxs-lookup"><span data-stu-id="9a396-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="9a396-159">Í reitnum Áætlun skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="9a396-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="9a396-160">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9a396-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9a396-161">Dæmi: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="9a396-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="9a396-162">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="9a396-162">Click Run.</span></span>
4. <span data-ttu-id="9a396-163">Útvíkka eða draga saman Færslur sem á að taka með hluta.</span><span class="sxs-lookup"><span data-stu-id="9a396-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="9a396-164">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="9a396-164">Click Filter.</span></span>
6. <span data-ttu-id="9a396-165">Á listanum, Velja línuna fyrir svæðið = vörunúmer</span><span class="sxs-lookup"><span data-stu-id="9a396-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="9a396-166">Í reitinn Skilyrði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9a396-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="9a396-167">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="9a396-167">Example: P6003</span></span>  
8. <span data-ttu-id="9a396-168">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9a396-168">Click OK.</span></span>
9. <span data-ttu-id="9a396-169">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9a396-169">Click OK.</span></span>
10. <span data-ttu-id="9a396-170">Smellt er á Áætlaðar pantanir.</span><span class="sxs-lookup"><span data-stu-id="9a396-170">Click Planned orders.</span></span>
11. <span data-ttu-id="9a396-171">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="9a396-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9a396-172">Til dæmis, sía svæðið vörunúmer með gildið 'P6000'.</span><span class="sxs-lookup"><span data-stu-id="9a396-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="9a396-173">Sía eftir formúluvöru sem hefur aukaafurð vöru sem stofnuð var sölupöntun fyrir.</span><span class="sxs-lookup"><span data-stu-id="9a396-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="9a396-174">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="9a396-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9a396-175">Velja allar línur sem sían skilaði.</span><span class="sxs-lookup"><span data-stu-id="9a396-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="9a396-176">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9a396-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="9a396-177">Útvíkka eða draga saman hlutann Þarfarakning.</span><span class="sxs-lookup"><span data-stu-id="9a396-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="9a396-178">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9a396-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9a396-179">Áætluð pöntun er fest við sölupöntun fyrir aukaafurðina.</span><span class="sxs-lookup"><span data-stu-id="9a396-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="9a396-180">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9a396-180">Close the page.</span></span>
17. <span data-ttu-id="9a396-181">Smellt er á aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="9a396-181">Click Master planning.</span></span>
18. <span data-ttu-id="9a396-182">Fara í Aðaláætlunargerð > Uppsetning > Færibreytur áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="9a396-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="9a396-183">Veljið Nei í reitnum Slökkva á öllum ferlum áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="9a396-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="9a396-184">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9a396-184">Close the page.</span></span>

