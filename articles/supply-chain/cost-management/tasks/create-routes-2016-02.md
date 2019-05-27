---
title: Stofna leiðir (aðeins febrúar 2016)
description: Þetta verk einblínir á að búa til framleiðsluleiðir fyrir fullunnin vara og hálfunnin vara.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 63ad2cc0c41a5931750dffbfc64bc7ce965a1da4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563205"
---
# <a name="create-routes-february-2016-only"></a><span data-ttu-id="dacbc-103">Stofna leiðir (aðeins febrúar 2016)</span><span class="sxs-lookup"><span data-stu-id="dacbc-103">Create routes (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dacbc-104">Þetta verk einblínir á að búa til framleiðsluleiðir fyrir fullunnin vara og hálfunnin vara.</span><span class="sxs-lookup"><span data-stu-id="dacbc-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="dacbc-105">Þetta er fimmta verkið í línunni Útreikningur uppskrifta.</span><span class="sxs-lookup"><span data-stu-id="dacbc-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="dacbc-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="dacbc-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="dacbc-107">Búa til leið fyrir hálfunnin vara</span><span class="sxs-lookup"><span data-stu-id="dacbc-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="dacbc-108">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="dacbc-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="dacbc-109">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="dacbc-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dacbc-110">Veljið vörunúmer BOM_2.</span><span class="sxs-lookup"><span data-stu-id="dacbc-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="dacbc-111">Smellið á tæknifræðingur á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="dacbc-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="dacbc-112">Smellt er á Leiðinni.</span><span class="sxs-lookup"><span data-stu-id="dacbc-112">Click Route.</span></span>
5. <span data-ttu-id="dacbc-113">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="dacbc-113">Click New.</span></span>
6. <span data-ttu-id="dacbc-114">Smellt er á Leið og leiðarútgáfa.</span><span class="sxs-lookup"><span data-stu-id="dacbc-114">Click Route and route version.</span></span>
7. <span data-ttu-id="dacbc-115">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="dacbc-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="dacbc-116">Til dæmis, slá inn ROUTE_2.</span><span class="sxs-lookup"><span data-stu-id="dacbc-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="dacbc-117">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="dacbc-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="dacbc-118">Í þessu dæmi, slá inn eða velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="dacbc-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="dacbc-119">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="dacbc-119">Click OK.</span></span>
10. <span data-ttu-id="dacbc-120">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="dacbc-120">Click New.</span></span>
11. <span data-ttu-id="dacbc-121">Færa inn eða veljið gildi í svæðinu aðgerð.</span><span class="sxs-lookup"><span data-stu-id="dacbc-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="dacbc-122">Í þessu dæmi, velja Samsetning.</span><span class="sxs-lookup"><span data-stu-id="dacbc-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="dacbc-123">Í reitinn keyrslutími skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="dacbc-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="dacbc-124">Til dæmis, skrifið 1.</span><span class="sxs-lookup"><span data-stu-id="dacbc-124">For example, type 1.</span></span> <span data-ttu-id="dacbc-125">Uppsetningartímar eru að öllu jöfnu hluti af verðinu sem reiknað er fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="dacbc-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="dacbc-126">Í reitinn leiðaflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="dacbc-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="dacbc-127">Í þessu dæmi, velja Std.</span><span class="sxs-lookup"><span data-stu-id="dacbc-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="dacbc-128">Smellið á flipann „Setja upp“.</span><span class="sxs-lookup"><span data-stu-id="dacbc-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="dacbc-129">Sláið inn eða veldu gildi í reitnum Setja upp flokkur.</span><span class="sxs-lookup"><span data-stu-id="dacbc-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="dacbc-130">Í þessu dæmi, velja Samsetning.</span><span class="sxs-lookup"><span data-stu-id="dacbc-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="dacbc-131">Smellt er á tímaflipann.</span><span class="sxs-lookup"><span data-stu-id="dacbc-131">Click the Times tab.</span></span>
17. <span data-ttu-id="dacbc-132">Í svæði Uppsetningartími, slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="dacbc-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="dacbc-133">Í þessu dæmi, slá inn 1.</span><span class="sxs-lookup"><span data-stu-id="dacbc-133">For this example, type 1.</span></span> <span data-ttu-id="dacbc-134">Uppsetningartímar eru að öllu jöfnu hluti af verðinu sem reiknað er fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="dacbc-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="dacbc-135">Í aðgerðasvæði, smella á Leiðarútgáfa.</span><span class="sxs-lookup"><span data-stu-id="dacbc-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="dacbc-136">Smellið á Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="dacbc-136">Click Approve.</span></span>
20. <span data-ttu-id="dacbc-137">Velja skal Já í „Á einnig að samþykkja leiðina?“ reit.</span><span class="sxs-lookup"><span data-stu-id="dacbc-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="dacbc-138">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="dacbc-138">Click OK.</span></span>
22. <span data-ttu-id="dacbc-139">Í aðgerðasvæði, smella á Leiðarútgáfa.</span><span class="sxs-lookup"><span data-stu-id="dacbc-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="dacbc-140">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="dacbc-140">Click Activate.</span></span>
24. <span data-ttu-id="dacbc-141">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="dacbc-141">Close the page.</span></span>
25. <span data-ttu-id="dacbc-142">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="dacbc-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="dacbc-143">Búa til leið fyrir fullunnin vara</span><span class="sxs-lookup"><span data-stu-id="dacbc-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="dacbc-144">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="dacbc-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="dacbc-145">Veljið vörunúmer BOM_1.</span><span class="sxs-lookup"><span data-stu-id="dacbc-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="dacbc-146">Smellið á tæknifræðingur á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="dacbc-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="dacbc-147">Smellt er á Leiðinni.</span><span class="sxs-lookup"><span data-stu-id="dacbc-147">Click Route.</span></span>
4. <span data-ttu-id="dacbc-148">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="dacbc-148">Click New.</span></span>
5. <span data-ttu-id="dacbc-149">Smellt er á Leið og leiðarútgáfa.</span><span class="sxs-lookup"><span data-stu-id="dacbc-149">Click Route and route version.</span></span>
6. <span data-ttu-id="dacbc-150">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="dacbc-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="dacbc-151">Í þessu dæmi, slá inn ROUTE_1.</span><span class="sxs-lookup"><span data-stu-id="dacbc-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="dacbc-152">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="dacbc-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="dacbc-153">Í þessu dæmi, slá inn eða velja Svæði 1.</span><span class="sxs-lookup"><span data-stu-id="dacbc-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="dacbc-154">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="dacbc-154">Click OK.</span></span>
9. <span data-ttu-id="dacbc-155">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="dacbc-155">Click New.</span></span>
10. <span data-ttu-id="dacbc-156">Færa inn eða veljið gildi í svæðinu aðgerð.</span><span class="sxs-lookup"><span data-stu-id="dacbc-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="dacbc-157">Í þessu dæmi, velja Umbúðir.</span><span class="sxs-lookup"><span data-stu-id="dacbc-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="dacbc-158">Í reitinn keyrslutími skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="dacbc-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="dacbc-159">Í þessu dæmi, slá inn 1.</span><span class="sxs-lookup"><span data-stu-id="dacbc-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="dacbc-160">Í reitinn leiðaflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="dacbc-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="dacbc-161">Í þessu dæmi, velja Std.</span><span class="sxs-lookup"><span data-stu-id="dacbc-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="dacbc-162">Smellið á flipann „Setja upp“.</span><span class="sxs-lookup"><span data-stu-id="dacbc-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="dacbc-163">Sláið inn eða veldu gildi í reitnum Setja upp flokkur.</span><span class="sxs-lookup"><span data-stu-id="dacbc-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="dacbc-164">Í þessu dæmi, velja Umbúðir.</span><span class="sxs-lookup"><span data-stu-id="dacbc-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="dacbc-165">Smellt er á tímaflipann.</span><span class="sxs-lookup"><span data-stu-id="dacbc-165">Click the Times tab.</span></span>
16. <span data-ttu-id="dacbc-166">Í svæði Uppsetningartími, slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="dacbc-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="dacbc-167">Í þessu dæmi, slá inn 1.</span><span class="sxs-lookup"><span data-stu-id="dacbc-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="dacbc-168">Í aðgerðasvæði, smella á Leiðarútgáfa.</span><span class="sxs-lookup"><span data-stu-id="dacbc-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="dacbc-169">Smellið á Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="dacbc-169">Click Approve.</span></span>
19. <span data-ttu-id="dacbc-170">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="dacbc-170">Click OK.</span></span>
20. <span data-ttu-id="dacbc-171">Í aðgerðasvæði, smella á Leiðarútgáfa.</span><span class="sxs-lookup"><span data-stu-id="dacbc-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="dacbc-172">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="dacbc-172">Click Activate.</span></span>
22. <span data-ttu-id="dacbc-173">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="dacbc-173">Close the page.</span></span>
23. <span data-ttu-id="dacbc-174">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="dacbc-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="dacbc-175">Kveikja á sjálfvirkt notkun á uppsetningartími</span><span class="sxs-lookup"><span data-stu-id="dacbc-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="dacbc-176">Smella skal á Framleiðslustýring > Uppsetningu > Leiðir > Leiðaflokkar.</span><span class="sxs-lookup"><span data-stu-id="dacbc-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="dacbc-177">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="dacbc-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="dacbc-178">Velja Std á listanum.</span><span class="sxs-lookup"><span data-stu-id="dacbc-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="dacbc-179">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="dacbc-179">Click Edit.</span></span>
4. <span data-ttu-id="dacbc-180">Velja Já í svæði Uppsetningartími.</span><span class="sxs-lookup"><span data-stu-id="dacbc-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="dacbc-181">Uppsetningartímar eru að öllu jöfnu hluti af verðinu sem reiknað er fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="dacbc-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="dacbc-182">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="dacbc-182">Click Save.</span></span>
6. <span data-ttu-id="dacbc-183">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="dacbc-183">Close the page.</span></span>

