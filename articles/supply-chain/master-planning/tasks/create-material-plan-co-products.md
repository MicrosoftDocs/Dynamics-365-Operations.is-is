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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5915dca3af0650883ef5c90dbc50332af5be6cbd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209675"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="b6da4-103">Stofna efnisáætlun fyrir aukaafurðir.</span><span class="sxs-lookup"><span data-stu-id="b6da4-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b6da4-104">Framleiðslustjóri áætlar efnisþarfir fyrir vörur sem eru aukaafurðir formúlu.</span><span class="sxs-lookup"><span data-stu-id="b6da4-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="b6da4-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USP2.</span><span class="sxs-lookup"><span data-stu-id="b6da4-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="b6da4-106">Stofna þörf fyrir aukaafurð</span><span class="sxs-lookup"><span data-stu-id="b6da4-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="b6da4-107">Farðu í Sjálfgefið mælaborð.</span><span class="sxs-lookup"><span data-stu-id="b6da4-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="b6da4-108">Smellt er á Vinnsla og fyrirspurnir sölupantana.</span><span class="sxs-lookup"><span data-stu-id="b6da4-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="b6da4-109">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="b6da4-109">Click New.</span></span>
4. <span data-ttu-id="b6da4-110">Smellt er á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="b6da4-110">Click Sales order.</span></span>
5. <span data-ttu-id="b6da4-111">Í reitinn Reikningur viðskiptavinar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b6da4-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="b6da4-112">Dæmi: US-001</span><span class="sxs-lookup"><span data-stu-id="b6da4-112">Example: US-001</span></span>  
6. <span data-ttu-id="b6da4-113">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b6da4-113">Click OK.</span></span>
7. <span data-ttu-id="b6da4-114">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b6da4-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="b6da4-115">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="b6da4-115">Example: P6003</span></span>  
8. <span data-ttu-id="b6da4-116">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="b6da4-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="b6da4-117">Til dæmis: 50000.</span><span class="sxs-lookup"><span data-stu-id="b6da4-117">Example: 50000</span></span>  
9. <span data-ttu-id="b6da4-118">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b6da4-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="b6da4-119">Búa til efnisáætlun fyrir aukaafurðir</span><span class="sxs-lookup"><span data-stu-id="b6da4-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="b6da4-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b6da4-120">Close the page.</span></span>
2. <span data-ttu-id="b6da4-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b6da4-121">Close the page.</span></span>
3. <span data-ttu-id="b6da4-122">Smellt er á aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="b6da4-122">Click Master planning.</span></span>
4. <span data-ttu-id="b6da4-123">Í reitnum Áætlun skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="b6da4-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="b6da4-124">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="b6da4-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b6da4-125">Dæmi: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="b6da4-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="b6da4-126">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="b6da4-126">Click Run.</span></span>
7. <span data-ttu-id="b6da4-127">Útvíkka eða draga saman Færslur sem á að taka með hluta.</span><span class="sxs-lookup"><span data-stu-id="b6da4-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="b6da4-128">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="b6da4-128">Click Filter.</span></span>
9. <span data-ttu-id="b6da4-129">Á listanum, Velja línuna fyrir svæðið = vörunúmer</span><span class="sxs-lookup"><span data-stu-id="b6da4-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="b6da4-130">Í reitinn Skilyrði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b6da4-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="b6da4-131">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="b6da4-131">Example: P6003</span></span>  
11. <span data-ttu-id="b6da4-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b6da4-132">Click OK.</span></span>
12. <span data-ttu-id="b6da4-133">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b6da4-133">Click OK.</span></span>
13. <span data-ttu-id="b6da4-134">Smellt er á Áætlaðar pantanir.</span><span class="sxs-lookup"><span data-stu-id="b6da4-134">Click Planned orders.</span></span>
14. <span data-ttu-id="b6da4-135">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="b6da4-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b6da4-136">Til dæmis, sía svæðið vörunúmer með gildið 'P6000'.</span><span class="sxs-lookup"><span data-stu-id="b6da4-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="b6da4-137">Sía eftir formúluvöru sem hefur aukaafurð vöru sem stofnuð var sölupöntun fyrir.</span><span class="sxs-lookup"><span data-stu-id="b6da4-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="b6da4-138">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="b6da4-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b6da4-139">Velja allar línur sem sían skilaði.</span><span class="sxs-lookup"><span data-stu-id="b6da4-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="b6da4-140">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="b6da4-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="b6da4-141">Útvíkka eða draga saman hlutann Þarfarakning.</span><span class="sxs-lookup"><span data-stu-id="b6da4-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="b6da4-142">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="b6da4-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b6da4-143">Áætluð pöntun er fest við sölupöntun fyrir aukaafurðina.</span><span class="sxs-lookup"><span data-stu-id="b6da4-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="b6da4-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b6da4-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="b6da4-145">Stofna þörf fyrir aukaafurð</span><span class="sxs-lookup"><span data-stu-id="b6da4-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="b6da4-146">Farðu í Sjálfgefið mælaborð.</span><span class="sxs-lookup"><span data-stu-id="b6da4-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="b6da4-147">Smellt er á Vinnsla og fyrirspurnir sölupantana.</span><span class="sxs-lookup"><span data-stu-id="b6da4-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="b6da4-148">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="b6da4-148">Click New.</span></span>
4. <span data-ttu-id="b6da4-149">Smellt er á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="b6da4-149">Click Sales order.</span></span>
5. <span data-ttu-id="b6da4-150">Í reitinn Reikningur viðskiptavinar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b6da4-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="b6da4-151">Dæmi: US-001</span><span class="sxs-lookup"><span data-stu-id="b6da4-151">Example: US-001</span></span>  
6. <span data-ttu-id="b6da4-152">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b6da4-152">Click OK.</span></span>
7. <span data-ttu-id="b6da4-153">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b6da4-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="b6da4-154">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="b6da4-154">Example: P6003</span></span>  
8. <span data-ttu-id="b6da4-155">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="b6da4-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="b6da4-156">Til dæmis: 50000.</span><span class="sxs-lookup"><span data-stu-id="b6da4-156">Example: 50000</span></span>  
9. <span data-ttu-id="b6da4-157">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="b6da4-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="b6da4-158">Búa til efnisáætlun fyrir aukaafurðir</span><span class="sxs-lookup"><span data-stu-id="b6da4-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="b6da4-159">Í reitnum Áætlun skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="b6da4-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="b6da4-160">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="b6da4-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b6da4-161">Dæmi: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="b6da4-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="b6da4-162">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="b6da4-162">Click Run.</span></span>
4. <span data-ttu-id="b6da4-163">Útvíkka eða draga saman Færslur sem á að taka með hluta.</span><span class="sxs-lookup"><span data-stu-id="b6da4-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="b6da4-164">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="b6da4-164">Click Filter.</span></span>
6. <span data-ttu-id="b6da4-165">Á listanum, Velja línuna fyrir svæðið = vörunúmer</span><span class="sxs-lookup"><span data-stu-id="b6da4-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="b6da4-166">Í reitinn Skilyrði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b6da4-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="b6da4-167">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="b6da4-167">Example: P6003</span></span>  
8. <span data-ttu-id="b6da4-168">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b6da4-168">Click OK.</span></span>
9. <span data-ttu-id="b6da4-169">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b6da4-169">Click OK.</span></span>
10. <span data-ttu-id="b6da4-170">Smellt er á Áætlaðar pantanir.</span><span class="sxs-lookup"><span data-stu-id="b6da4-170">Click Planned orders.</span></span>
11. <span data-ttu-id="b6da4-171">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="b6da4-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b6da4-172">Til dæmis, sía svæðið vörunúmer með gildið 'P6000'.</span><span class="sxs-lookup"><span data-stu-id="b6da4-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="b6da4-173">Sía eftir formúluvöru sem hefur aukaafurð vöru sem stofnuð var sölupöntun fyrir.</span><span class="sxs-lookup"><span data-stu-id="b6da4-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="b6da4-174">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="b6da4-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="b6da4-175">Velja allar línur sem sían skilaði.</span><span class="sxs-lookup"><span data-stu-id="b6da4-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="b6da4-176">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="b6da4-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="b6da4-177">Útvíkka eða draga saman hlutann Þarfarakning.</span><span class="sxs-lookup"><span data-stu-id="b6da4-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="b6da4-178">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="b6da4-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b6da4-179">Áætluð pöntun er fest við sölupöntun fyrir aukaafurðina.</span><span class="sxs-lookup"><span data-stu-id="b6da4-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="b6da4-180">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b6da4-180">Close the page.</span></span>
17. <span data-ttu-id="b6da4-181">Smellt er á aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="b6da4-181">Click Master planning.</span></span>
18. <span data-ttu-id="b6da4-182">Fara í Aðaláætlunargerð > Uppsetning > Færibreytur áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="b6da4-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="b6da4-183">Veljið Nei í reitnum Slökkva á öllum ferlum áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="b6da4-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="b6da4-184">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b6da4-184">Close the page.</span></span>

