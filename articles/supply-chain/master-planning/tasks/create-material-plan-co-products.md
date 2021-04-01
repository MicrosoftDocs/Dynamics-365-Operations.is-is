---
title: Stofna efnisáætlun fyrir aukaafurðir.
description: Framleiðslustjóri áætlar efnisþarfir fyrir vörur sem eru aukaafurðir formúlu.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a87935f8f30d909f1a6a62ed7be00c83476a36a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214371"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="0876f-103">Stofna efnisáætlun fyrir aukaafurðir.</span><span class="sxs-lookup"><span data-stu-id="0876f-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0876f-104">Framleiðslustjóri áætlar efnisþarfir fyrir vörur sem eru aukaafurðir formúlu.</span><span class="sxs-lookup"><span data-stu-id="0876f-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="0876f-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USP2.</span><span class="sxs-lookup"><span data-stu-id="0876f-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="0876f-106">Stofna þörf fyrir aukaafurð</span><span class="sxs-lookup"><span data-stu-id="0876f-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="0876f-107">Farðu í Sjálfgefið mælaborð.</span><span class="sxs-lookup"><span data-stu-id="0876f-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="0876f-108">Smellt er á Vinnsla og fyrirspurnir sölupantana.</span><span class="sxs-lookup"><span data-stu-id="0876f-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="0876f-109">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="0876f-109">Click New.</span></span>
4. <span data-ttu-id="0876f-110">Smellt er á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="0876f-110">Click Sales order.</span></span>
5. <span data-ttu-id="0876f-111">Í reitinn Reikningur viðskiptavinar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="0876f-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="0876f-112">Dæmi: US-001</span><span class="sxs-lookup"><span data-stu-id="0876f-112">Example: US-001</span></span>  
6. <span data-ttu-id="0876f-113">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="0876f-113">Click OK.</span></span>
7. <span data-ttu-id="0876f-114">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="0876f-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="0876f-115">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="0876f-115">Example: P6003</span></span>  
8. <span data-ttu-id="0876f-116">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="0876f-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="0876f-117">Til dæmis: 50000.</span><span class="sxs-lookup"><span data-stu-id="0876f-117">Example: 50000</span></span>  
9. <span data-ttu-id="0876f-118">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="0876f-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="0876f-119">Búa til efnisáætlun fyrir aukaafurðir</span><span class="sxs-lookup"><span data-stu-id="0876f-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="0876f-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0876f-120">Close the page.</span></span>
2. <span data-ttu-id="0876f-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0876f-121">Close the page.</span></span>
3. <span data-ttu-id="0876f-122">Smellt er á aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="0876f-122">Click Master planning.</span></span>
4. <span data-ttu-id="0876f-123">Í reitnum Áætlun skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="0876f-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0876f-124">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0876f-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0876f-125">Dæmi: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="0876f-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="0876f-126">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="0876f-126">Click Run.</span></span>
7. <span data-ttu-id="0876f-127">Útvíkka eða draga saman Færslur sem á að taka með hluta.</span><span class="sxs-lookup"><span data-stu-id="0876f-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="0876f-128">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="0876f-128">Click Filter.</span></span>
9. <span data-ttu-id="0876f-129">Á listanum, Velja línuna fyrir svæðið = vörunúmer</span><span class="sxs-lookup"><span data-stu-id="0876f-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="0876f-130">Í reitinn Skilyrði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="0876f-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="0876f-131">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="0876f-131">Example: P6003</span></span>  
11. <span data-ttu-id="0876f-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="0876f-132">Click OK.</span></span>
12. <span data-ttu-id="0876f-133">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="0876f-133">Click OK.</span></span>
13. <span data-ttu-id="0876f-134">Smellt er á Áætlaðar pantanir.</span><span class="sxs-lookup"><span data-stu-id="0876f-134">Click Planned orders.</span></span>
14. <span data-ttu-id="0876f-135">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="0876f-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0876f-136">Til dæmis, sía svæðið vörunúmer með gildið 'P6000'.</span><span class="sxs-lookup"><span data-stu-id="0876f-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="0876f-137">Sía eftir formúluvöru sem hefur aukaafurð vöru sem stofnuð var sölupöntun fyrir.</span><span class="sxs-lookup"><span data-stu-id="0876f-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="0876f-138">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="0876f-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0876f-139">Velja allar línur sem sían skilaði.</span><span class="sxs-lookup"><span data-stu-id="0876f-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="0876f-140">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0876f-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="0876f-141">Útvíkka eða draga saman hlutann Þarfarakning.</span><span class="sxs-lookup"><span data-stu-id="0876f-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="0876f-142">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0876f-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0876f-143">Áætluð pöntun er fest við sölupöntun fyrir aukaafurðina.</span><span class="sxs-lookup"><span data-stu-id="0876f-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="0876f-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0876f-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="0876f-145">Stofna þörf fyrir aukaafurð</span><span class="sxs-lookup"><span data-stu-id="0876f-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="0876f-146">Farðu í Sjálfgefið mælaborð.</span><span class="sxs-lookup"><span data-stu-id="0876f-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="0876f-147">Smellt er á Vinnsla og fyrirspurnir sölupantana.</span><span class="sxs-lookup"><span data-stu-id="0876f-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="0876f-148">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="0876f-148">Click New.</span></span>
4. <span data-ttu-id="0876f-149">Smellt er á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="0876f-149">Click Sales order.</span></span>
5. <span data-ttu-id="0876f-150">Í reitinn Reikningur viðskiptavinar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="0876f-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="0876f-151">Dæmi: US-001</span><span class="sxs-lookup"><span data-stu-id="0876f-151">Example: US-001</span></span>  
6. <span data-ttu-id="0876f-152">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="0876f-152">Click OK.</span></span>
7. <span data-ttu-id="0876f-153">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="0876f-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="0876f-154">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="0876f-154">Example: P6003</span></span>  
8. <span data-ttu-id="0876f-155">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="0876f-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="0876f-156">Til dæmis: 50000.</span><span class="sxs-lookup"><span data-stu-id="0876f-156">Example: 50000</span></span>  
9. <span data-ttu-id="0876f-157">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="0876f-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="0876f-158">Búa til efnisáætlun fyrir aukaafurðir</span><span class="sxs-lookup"><span data-stu-id="0876f-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="0876f-159">Í reitnum Áætlun skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="0876f-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="0876f-160">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0876f-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0876f-161">Dæmi: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="0876f-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="0876f-162">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="0876f-162">Click Run.</span></span>
4. <span data-ttu-id="0876f-163">Útvíkka eða draga saman Færslur sem á að taka með hluta.</span><span class="sxs-lookup"><span data-stu-id="0876f-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="0876f-164">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="0876f-164">Click Filter.</span></span>
6. <span data-ttu-id="0876f-165">Á listanum, Velja línuna fyrir svæðið = vörunúmer</span><span class="sxs-lookup"><span data-stu-id="0876f-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="0876f-166">Í reitinn Skilyrði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="0876f-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="0876f-167">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="0876f-167">Example: P6003</span></span>  
8. <span data-ttu-id="0876f-168">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="0876f-168">Click OK.</span></span>
9. <span data-ttu-id="0876f-169">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="0876f-169">Click OK.</span></span>
10. <span data-ttu-id="0876f-170">Smellt er á Áætlaðar pantanir.</span><span class="sxs-lookup"><span data-stu-id="0876f-170">Click Planned orders.</span></span>
11. <span data-ttu-id="0876f-171">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="0876f-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0876f-172">Til dæmis, sía svæðið vörunúmer með gildið 'P6000'.</span><span class="sxs-lookup"><span data-stu-id="0876f-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="0876f-173">Sía eftir formúluvöru sem hefur aukaafurð vöru sem stofnuð var sölupöntun fyrir.</span><span class="sxs-lookup"><span data-stu-id="0876f-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="0876f-174">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="0876f-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="0876f-175">Velja allar línur sem sían skilaði.</span><span class="sxs-lookup"><span data-stu-id="0876f-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="0876f-176">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0876f-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="0876f-177">Útvíkka eða draga saman hlutann Þarfarakning.</span><span class="sxs-lookup"><span data-stu-id="0876f-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="0876f-178">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0876f-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0876f-179">Áætluð pöntun er fest við sölupöntun fyrir aukaafurðina.</span><span class="sxs-lookup"><span data-stu-id="0876f-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="0876f-180">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0876f-180">Close the page.</span></span>
17. <span data-ttu-id="0876f-181">Smellt er á aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="0876f-181">Click Master planning.</span></span>
18. <span data-ttu-id="0876f-182">Fara í Aðaláætlunargerð > Uppsetning > Færibreytur áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="0876f-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="0876f-183">Veljið Nei í reitnum Slökkva á öllum ferlum áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="0876f-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="0876f-184">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0876f-184">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]