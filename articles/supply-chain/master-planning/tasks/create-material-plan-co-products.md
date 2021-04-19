---
title: Stofna efnisáætlun fyrir aukaafurðir.
description: Framleiðslustjóri áætlar efnisþarfir fyrir vörur sem eru aukaafurðir formúlu.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d910b89330865b0bcf3f6cd05b761506f339a45f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841672"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="e2257-103">Stofna efnisáætlun fyrir aukaafurðir.</span><span class="sxs-lookup"><span data-stu-id="e2257-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e2257-104">Framleiðslustjóri áætlar efnisþarfir fyrir vörur sem eru aukaafurðir formúlu.</span><span class="sxs-lookup"><span data-stu-id="e2257-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="e2257-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USP2.</span><span class="sxs-lookup"><span data-stu-id="e2257-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="e2257-106">Stofna þörf fyrir aukaafurð</span><span class="sxs-lookup"><span data-stu-id="e2257-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="e2257-107">Farðu í Sjálfgefið mælaborð.</span><span class="sxs-lookup"><span data-stu-id="e2257-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="e2257-108">Smellt er á Vinnsla og fyrirspurnir sölupantana.</span><span class="sxs-lookup"><span data-stu-id="e2257-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="e2257-109">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="e2257-109">Click New.</span></span>
4. <span data-ttu-id="e2257-110">Smellt er á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="e2257-110">Click Sales order.</span></span>
5. <span data-ttu-id="e2257-111">Í reitinn Reikningur viðskiptavinar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e2257-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="e2257-112">Dæmi: US-001</span><span class="sxs-lookup"><span data-stu-id="e2257-112">Example: US-001</span></span>  
6. <span data-ttu-id="e2257-113">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e2257-113">Click OK.</span></span>
7. <span data-ttu-id="e2257-114">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e2257-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="e2257-115">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="e2257-115">Example: P6003</span></span>  
8. <span data-ttu-id="e2257-116">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="e2257-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="e2257-117">Til dæmis: 50000.</span><span class="sxs-lookup"><span data-stu-id="e2257-117">Example: 50000</span></span>  
9. <span data-ttu-id="e2257-118">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e2257-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="e2257-119">Búa til efnisáætlun fyrir aukaafurðir</span><span class="sxs-lookup"><span data-stu-id="e2257-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="e2257-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e2257-120">Close the page.</span></span>
2. <span data-ttu-id="e2257-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e2257-121">Close the page.</span></span>
3. <span data-ttu-id="e2257-122">Smellt er á aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="e2257-122">Click Master planning.</span></span>
4. <span data-ttu-id="e2257-123">Í reitnum Áætlun skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="e2257-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e2257-124">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e2257-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e2257-125">Dæmi: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="e2257-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="e2257-126">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="e2257-126">Click Run.</span></span>
7. <span data-ttu-id="e2257-127">Útvíkka eða draga saman Færslur sem á að taka með hluta.</span><span class="sxs-lookup"><span data-stu-id="e2257-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="e2257-128">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="e2257-128">Click Filter.</span></span>
9. <span data-ttu-id="e2257-129">Á listanum, Velja línuna fyrir svæðið = vörunúmer</span><span class="sxs-lookup"><span data-stu-id="e2257-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="e2257-130">Í reitinn Skilyrði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e2257-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="e2257-131">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="e2257-131">Example: P6003</span></span>  
11. <span data-ttu-id="e2257-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e2257-132">Click OK.</span></span>
12. <span data-ttu-id="e2257-133">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e2257-133">Click OK.</span></span>
13. <span data-ttu-id="e2257-134">Smellt er á Áætlaðar pantanir.</span><span class="sxs-lookup"><span data-stu-id="e2257-134">Click Planned orders.</span></span>
14. <span data-ttu-id="e2257-135">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="e2257-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e2257-136">Til dæmis, sía svæðið vörunúmer með gildið 'P6000'.</span><span class="sxs-lookup"><span data-stu-id="e2257-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="e2257-137">Sía eftir formúluvöru sem hefur aukaafurð vöru sem stofnuð var sölupöntun fyrir.</span><span class="sxs-lookup"><span data-stu-id="e2257-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="e2257-138">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="e2257-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e2257-139">Velja allar línur sem sían skilaði.</span><span class="sxs-lookup"><span data-stu-id="e2257-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="e2257-140">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e2257-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="e2257-141">Útvíkka eða draga saman hlutann Þarfarakning.</span><span class="sxs-lookup"><span data-stu-id="e2257-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="e2257-142">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e2257-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e2257-143">Áætluð pöntun er fest við sölupöntun fyrir aukaafurðina.</span><span class="sxs-lookup"><span data-stu-id="e2257-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="e2257-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e2257-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="e2257-145">Stofna þörf fyrir aukaafurð</span><span class="sxs-lookup"><span data-stu-id="e2257-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="e2257-146">Farðu í Sjálfgefið mælaborð.</span><span class="sxs-lookup"><span data-stu-id="e2257-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="e2257-147">Smellt er á Vinnsla og fyrirspurnir sölupantana.</span><span class="sxs-lookup"><span data-stu-id="e2257-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="e2257-148">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="e2257-148">Click New.</span></span>
4. <span data-ttu-id="e2257-149">Smellt er á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="e2257-149">Click Sales order.</span></span>
5. <span data-ttu-id="e2257-150">Í reitinn Reikningur viðskiptavinar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e2257-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="e2257-151">Dæmi: US-001</span><span class="sxs-lookup"><span data-stu-id="e2257-151">Example: US-001</span></span>  
6. <span data-ttu-id="e2257-152">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e2257-152">Click OK.</span></span>
7. <span data-ttu-id="e2257-153">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e2257-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="e2257-154">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="e2257-154">Example: P6003</span></span>  
8. <span data-ttu-id="e2257-155">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="e2257-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="e2257-156">Til dæmis: 50000.</span><span class="sxs-lookup"><span data-stu-id="e2257-156">Example: 50000</span></span>  
9. <span data-ttu-id="e2257-157">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e2257-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="e2257-158">Búa til efnisáætlun fyrir aukaafurðir</span><span class="sxs-lookup"><span data-stu-id="e2257-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="e2257-159">Í reitnum Áætlun skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="e2257-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="e2257-160">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e2257-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e2257-161">Dæmi: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="e2257-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="e2257-162">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="e2257-162">Click Run.</span></span>
4. <span data-ttu-id="e2257-163">Útvíkka eða draga saman Færslur sem á að taka með hluta.</span><span class="sxs-lookup"><span data-stu-id="e2257-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="e2257-164">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="e2257-164">Click Filter.</span></span>
6. <span data-ttu-id="e2257-165">Á listanum, Velja línuna fyrir svæðið = vörunúmer</span><span class="sxs-lookup"><span data-stu-id="e2257-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="e2257-166">Í reitinn Skilyrði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e2257-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="e2257-167">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="e2257-167">Example: P6003</span></span>  
8. <span data-ttu-id="e2257-168">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e2257-168">Click OK.</span></span>
9. <span data-ttu-id="e2257-169">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e2257-169">Click OK.</span></span>
10. <span data-ttu-id="e2257-170">Smellt er á Áætlaðar pantanir.</span><span class="sxs-lookup"><span data-stu-id="e2257-170">Click Planned orders.</span></span>
11. <span data-ttu-id="e2257-171">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="e2257-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e2257-172">Til dæmis, sía svæðið vörunúmer með gildið 'P6000'.</span><span class="sxs-lookup"><span data-stu-id="e2257-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="e2257-173">Sía eftir formúluvöru sem hefur aukaafurð vöru sem stofnuð var sölupöntun fyrir.</span><span class="sxs-lookup"><span data-stu-id="e2257-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="e2257-174">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="e2257-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e2257-175">Velja allar línur sem sían skilaði.</span><span class="sxs-lookup"><span data-stu-id="e2257-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="e2257-176">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e2257-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="e2257-177">Útvíkka eða draga saman hlutann Þarfarakning.</span><span class="sxs-lookup"><span data-stu-id="e2257-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="e2257-178">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e2257-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e2257-179">Áætluð pöntun er fest við sölupöntun fyrir aukaafurðina.</span><span class="sxs-lookup"><span data-stu-id="e2257-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="e2257-180">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e2257-180">Close the page.</span></span>
17. <span data-ttu-id="e2257-181">Smellt er á aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="e2257-181">Click Master planning.</span></span>
18. <span data-ttu-id="e2257-182">Fara í Aðaláætlunargerð > Uppsetning > Færibreytur áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="e2257-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="e2257-183">Veljið Nei í reitnum Slökkva á öllum ferlum áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="e2257-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="e2257-184">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e2257-184">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]