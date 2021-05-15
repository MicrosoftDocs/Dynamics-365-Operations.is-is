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
ms.openlocfilehash: b51e4b4d00da2babb5128d8c4c22139b0c1853d4
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920730"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="29e42-103">Stofna efnisáætlun fyrir aukaafurðir.</span><span class="sxs-lookup"><span data-stu-id="29e42-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="29e42-104">Framleiðslustjóri áætlar efnisþarfir fyrir vörur sem eru aukaafurðir formúlu.</span><span class="sxs-lookup"><span data-stu-id="29e42-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="29e42-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USP2.</span><span class="sxs-lookup"><span data-stu-id="29e42-105">The demo data company used to create this procedure is USP2.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="29e42-106">Stofna þörf fyrir aukaafurð</span><span class="sxs-lookup"><span data-stu-id="29e42-106">Create requirement for a co-product</span></span>

1. <span data-ttu-id="29e42-107">Farið í **Sala og markaðssetning \> Vinnusvæði \> Vinnsla og fyrirspurnir sölupantana**.</span><span class="sxs-lookup"><span data-stu-id="29e42-107">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="29e42-108">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="29e42-108">Select **New**.</span></span>
1. <span data-ttu-id="29e42-109">Veldu **Velja sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="29e42-109">Select **Sales order**.</span></span>
1. <span data-ttu-id="29e42-110">Í reitinn **Viðskiptavinalykill** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="29e42-110">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="29e42-111">Dæmi: US-001</span><span class="sxs-lookup"><span data-stu-id="29e42-111">Example: US-001</span></span>  
1. <span data-ttu-id="29e42-112">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="29e42-112">Select **OK**.</span></span>
1. <span data-ttu-id="29e42-113">Í reitnum **Vörunúmer** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="29e42-113">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="29e42-114">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="29e42-114">Example: P6003</span></span>  
1. <span data-ttu-id="29e42-115">Í reitnum **Magn** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="29e42-115">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="29e42-116">Til dæmis: 50000.</span><span class="sxs-lookup"><span data-stu-id="29e42-116">Example: 50000</span></span>  
1. <span data-ttu-id="29e42-117">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="29e42-117">Select **Save**.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="29e42-118">Búa til efnisáætlun fyrir aukaafurðir</span><span class="sxs-lookup"><span data-stu-id="29e42-118">Create a material plan for co-products</span></span>

1. <span data-ttu-id="29e42-119">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="29e42-119">Close the page.</span></span>
1. <span data-ttu-id="29e42-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="29e42-120">Close the page.</span></span>
1. <span data-ttu-id="29e42-121">Veljið **Aðaláætlanagerð**.</span><span class="sxs-lookup"><span data-stu-id="29e42-121">Select **Master planning**.</span></span>
1. <span data-ttu-id="29e42-122">Í reitnum **Áætlun** velurðu fellilistahnappinn til að opna uppflettinguna.</span><span class="sxs-lookup"><span data-stu-id="29e42-122">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
1. <span data-ttu-id="29e42-123">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="29e42-123">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="29e42-124">Dæmi: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="29e42-124">Example: MasterPlan</span></span>  
1. <span data-ttu-id="29e42-125">Veljið **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="29e42-125">Select **Run**.</span></span>
1. <span data-ttu-id="29e42-126">Útvíkka eða draga saman **Færslur sem á að taka með** hlutann.</span><span class="sxs-lookup"><span data-stu-id="29e42-126">Expand or collapse the **Records to include** section.</span></span>
1. <span data-ttu-id="29e42-127">Velja **Síu**.</span><span class="sxs-lookup"><span data-stu-id="29e42-127">Select **Filter**.</span></span>
1. <span data-ttu-id="29e42-128">Í listanum skal velja línuna fyrir **Reitur** = *Vörunúmer*.</span><span class="sxs-lookup"><span data-stu-id="29e42-128">In the list, select the row for **Field** = *Item number*.</span></span>
1. <span data-ttu-id="29e42-129">Í reitnum **Skilyrði** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="29e42-129">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="29e42-130">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="29e42-130">Example: P6003</span></span>  
1. <span data-ttu-id="29e42-131">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="29e42-131">Select **OK**.</span></span>
1. <span data-ttu-id="29e42-132">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="29e42-132">Select **OK**.</span></span>
1. <span data-ttu-id="29e42-133">Veldu **Tillögur**.</span><span class="sxs-lookup"><span data-stu-id="29e42-133">Select **Planned orders**.</span></span>
1. <span data-ttu-id="29e42-134">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="29e42-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="29e42-135">Til dæmis, sía svæðið **Vörunúmer** með gildið 'P6000'.</span><span class="sxs-lookup"><span data-stu-id="29e42-135">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="29e42-136">Sía eftir formúluvöru sem hefur aukaafurð vöru sem stofnuð var sölupöntun fyrir.</span><span class="sxs-lookup"><span data-stu-id="29e42-136">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
1. <span data-ttu-id="29e42-137">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="29e42-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="29e42-138">Velja allar línur sem sían skilaði.</span><span class="sxs-lookup"><span data-stu-id="29e42-138">Select any of the rows returned by the filter.</span></span>  
1. <span data-ttu-id="29e42-139">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="29e42-139">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="29e42-140">Víkkið út hlutann **Þarfarakning**.</span><span class="sxs-lookup"><span data-stu-id="29e42-140">Expand the **Pegging** section.</span></span>
1. <span data-ttu-id="29e42-141">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="29e42-141">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="29e42-142">Áætluð pöntun er fest við sölupöntun fyrir aukaafurðina.</span><span class="sxs-lookup"><span data-stu-id="29e42-142">The planned order is pegged to the sales order for the co-product.</span></span>  
1. <span data-ttu-id="29e42-143">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="29e42-143">Close the page.</span></span>

## <a name="create-a-second-requirement-for-a-co-product"></a><span data-ttu-id="29e42-144">Stofna aðra þörf fyrir aukaafurð</span><span class="sxs-lookup"><span data-stu-id="29e42-144">Create a second requirement for a co-product</span></span>

1. <span data-ttu-id="29e42-145">Farið í **Sala og markaðssetning \> Vinnusvæði \> Vinnsla og fyrirspurnir sölupantana**.</span><span class="sxs-lookup"><span data-stu-id="29e42-145">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="29e42-146">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="29e42-146">Select **New**.</span></span>
1. <span data-ttu-id="29e42-147">Veldu **Velja sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="29e42-147">Select **Sales order**.</span></span>
1. <span data-ttu-id="29e42-148">Í reitinn **Viðskiptavinalykill** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="29e42-148">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="29e42-149">Dæmi: US-001</span><span class="sxs-lookup"><span data-stu-id="29e42-149">Example: US-001</span></span>  
1. <span data-ttu-id="29e42-150">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="29e42-150">Select **OK**.</span></span>
1. <span data-ttu-id="29e42-151">Í reitnum **Vörunúmer** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="29e42-151">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="29e42-152">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="29e42-152">Example: P6003</span></span>  
1. <span data-ttu-id="29e42-153">Í reitnum **Magn** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="29e42-153">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="29e42-154">Til dæmis: 50000.</span><span class="sxs-lookup"><span data-stu-id="29e42-154">Example: 50000</span></span>  
1. <span data-ttu-id="29e42-155">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="29e42-155">Select **Save**.</span></span>

## <a name="create-a-second-material-plan-for-co-products"></a><span data-ttu-id="29e42-156">Stofna aðra efnisáætlun fyrir aukaafurðir</span><span class="sxs-lookup"><span data-stu-id="29e42-156">Create a second material plan for co-products</span></span>

1. <span data-ttu-id="29e42-157">Í reitnum **Áætlun** velurðu fellilistahnappinn til að opna uppflettinguna.</span><span class="sxs-lookup"><span data-stu-id="29e42-157">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="29e42-158">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="29e42-158">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="29e42-159">Dæmi: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="29e42-159">Example: MasterPlan</span></span>  
3. <span data-ttu-id="29e42-160">Veljið **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="29e42-160">Select **Run**.</span></span>
4. <span data-ttu-id="29e42-161">Útvíkka eða draga saman **Færslur sem á að taka með** hlutann.</span><span class="sxs-lookup"><span data-stu-id="29e42-161">Expand or collapse the **Records to include** section.</span></span>
5. <span data-ttu-id="29e42-162">Velja **Síu**.</span><span class="sxs-lookup"><span data-stu-id="29e42-162">Select **Filter**.</span></span>
6. <span data-ttu-id="29e42-163">Í listanum skal velja línuna fyrir **Reitur** = *Vörunúmer*.</span><span class="sxs-lookup"><span data-stu-id="29e42-163">In the list, select the row for **Field** = *Item number*.</span></span>
7. <span data-ttu-id="29e42-164">Í reitnum *Skilyrði* skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="29e42-164">In the *Criteria* field, type a value.</span></span>
    * <span data-ttu-id="29e42-165">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="29e42-165">Example: P6003</span></span>  
8. <span data-ttu-id="29e42-166">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="29e42-166">Select **OK**.</span></span>
9. <span data-ttu-id="29e42-167">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="29e42-167">Select **OK**.</span></span>
10. <span data-ttu-id="29e42-168">Veldu **Tillögur**.</span><span class="sxs-lookup"><span data-stu-id="29e42-168">Select **Planned orders**.</span></span>
11. <span data-ttu-id="29e42-169">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="29e42-169">Use the Quick Filter to find records.</span></span> <span data-ttu-id="29e42-170">Til dæmis, sía svæðið **Vörunúmer** með gildið 'P6000'.</span><span class="sxs-lookup"><span data-stu-id="29e42-170">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="29e42-171">Sía eftir formúluvöru sem hefur aukaafurð vöru sem stofnuð var sölupöntun fyrir.</span><span class="sxs-lookup"><span data-stu-id="29e42-171">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="29e42-172">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="29e42-172">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="29e42-173">Velja allar línur sem sían skilaði.</span><span class="sxs-lookup"><span data-stu-id="29e42-173">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="29e42-174">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="29e42-174">In the list, select the link in the selected row.</span></span>
14. <span data-ttu-id="29e42-175">Útvíkka eða draga saman hlutann **Þarfarakning**.</span><span class="sxs-lookup"><span data-stu-id="29e42-175">Expand or collapse the **Pegging** section.</span></span>
15. <span data-ttu-id="29e42-176">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="29e42-176">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="29e42-177">Áætluð pöntun er fest við sölupöntun fyrir aukaafurðina.</span><span class="sxs-lookup"><span data-stu-id="29e42-177">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="29e42-178">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="29e42-178">Close the page.</span></span>
17. <span data-ttu-id="29e42-179">Veljið **Aðaláætlanagerð**.</span><span class="sxs-lookup"><span data-stu-id="29e42-179">Select **Master planning**.</span></span>
18. <span data-ttu-id="29e42-180">Farið í **Aðaláætlanagerð \> Uppsetning \> Færibreytur aðaláætlanagerðar**.</span><span class="sxs-lookup"><span data-stu-id="29e42-180">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
19. <span data-ttu-id="29e42-181">Veljið *Nei* í reitnum **Slökkva á öllum ferlum áætlanagerðar**.</span><span class="sxs-lookup"><span data-stu-id="29e42-181">Select *No* in the **Disable all planning processes** field.</span></span>
20. <span data-ttu-id="29e42-182">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="29e42-182">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]