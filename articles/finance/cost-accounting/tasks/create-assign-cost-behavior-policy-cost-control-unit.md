---
title: Stofna og úthluta kostnaðarhegðunarreglu fyrir kostnaðarstýringareiningu
description: Kostnaður er flokkaður út frá kostnaðarhegðun sem annað hvort fastur eða breytilegur.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cfdff9b1af9183d21e988dd53559e749eed077eb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976236"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a><span data-ttu-id="d3348-103">Stofna og úthluta kostnaðarhegðunarreglu fyrir kostnaðarstýringareiningu</span><span class="sxs-lookup"><span data-stu-id="d3348-103">Create and assign a cost behavior policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d3348-104">Kostnaður er flokkaður út frá kostnaðarhegðun sem annað hvort fastur eða breytilegur.</span><span class="sxs-lookup"><span data-stu-id="d3348-104">Cost behavior is the classification of costs as either fixed or variable.</span></span> <span data-ttu-id="d3348-105">Stefna og samsvarandi reglur er úthlutað til kostnaðarstýringareiningar svo stefnan taki gildi.</span><span class="sxs-lookup"><span data-stu-id="d3348-105">A policy and the corresponding rules have to be assigned to a cost control unit for the policy to become effective.</span></span> <span data-ttu-id="d3348-106">Nota þetta ferli til að stofna stefnu og síðan úthluta stefnunni til kostnaðarstýringareiningar</span><span class="sxs-lookup"><span data-stu-id="d3348-106">Use this procedure to create a policy and then assign the policy to a cost control unit.</span></span>


## <a name="create-a-cost-behavior-hierarchy"></a><span data-ttu-id="d3348-107">Stofna Stigveldi kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="d3348-107">Create a cost behavior hierarchy</span></span>
1. <span data-ttu-id="d3348-108">Fara í kostnaðarbókhald > Víddir > Stigveldi vídda.</span><span class="sxs-lookup"><span data-stu-id="d3348-108">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="d3348-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d3348-109">Click New.</span></span>
3. <span data-ttu-id="d3348-110">Smellið á „Stofna“.</span><span class="sxs-lookup"><span data-stu-id="d3348-110">Click Create.</span></span>
4. <span data-ttu-id="d3348-111">Í reitinn Heiti stigveldi víddar skal slá inn „Stigveldi kostnaðarhegðunar“.</span><span class="sxs-lookup"><span data-stu-id="d3348-111">In the Dimension hierarchy name field, type 'Cost behavior hierarchy'.</span></span>
5. <span data-ttu-id="d3348-112">Sláið inn eða veljið gildi í reitnum Vídd.</span><span class="sxs-lookup"><span data-stu-id="d3348-112">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="d3348-113">Velja kostnaðareiningar</span><span class="sxs-lookup"><span data-stu-id="d3348-113">Select Cost elements.</span></span>  
6. <span data-ttu-id="d3348-114">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d3348-114">Click Save.</span></span>
7. <span data-ttu-id="d3348-115">Smella á Skoða stigveldi</span><span class="sxs-lookup"><span data-stu-id="d3348-115">Click View hierarchy.</span></span>
8. <span data-ttu-id="d3348-116">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d3348-116">Click New.</span></span>
9. <span data-ttu-id="d3348-117">Í svæðið Heiti hnútar, færðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d3348-117">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="d3348-118">Færa inn Fastan kostnað.</span><span class="sxs-lookup"><span data-stu-id="d3348-118">Enter Fixed cost.</span></span>  
10. <span data-ttu-id="d3348-119">Í trénu skal velja „Stigveldi kostnaðarhegðunar“.</span><span class="sxs-lookup"><span data-stu-id="d3348-119">In the tree, select 'Cost behavior hierarchy'.</span></span>
11. <span data-ttu-id="d3348-120">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d3348-120">Click New.</span></span>
12. <span data-ttu-id="d3348-121">Í svæðið Heiti hnútar, færðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d3348-121">In the Node name field, type a value.</span></span>
    * <span data-ttu-id="d3348-122">Færa inn breytilegur kostnaður.</span><span class="sxs-lookup"><span data-stu-id="d3348-122">Enter Variable cost.</span></span>  
13. <span data-ttu-id="d3348-123">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d3348-123">Click Save.</span></span>
14. <span data-ttu-id="d3348-124">Í trénu skal velja „stigveldi kostnaðarhegðunar\Fastur kostnaður“.</span><span class="sxs-lookup"><span data-stu-id="d3348-124">In the tree, select 'Cost behavior hierarchy\Fixed cost'.</span></span>
15. <span data-ttu-id="d3348-125">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d3348-125">Click New.</span></span>
16. <span data-ttu-id="d3348-126">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d3348-126">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="d3348-127">Sláið inn eða veldu gildi í reitnum Frá víddarstak.</span><span class="sxs-lookup"><span data-stu-id="d3348-127">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d3348-128">Afmörkun víddarstaks getur innihaldið gloppur, en stökin geta ekki skarast.</span><span class="sxs-lookup"><span data-stu-id="d3348-128">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
18. <span data-ttu-id="d3348-129">Sláið inn eða veldu gildi í reitnum í Til víddarstak.</span><span class="sxs-lookup"><span data-stu-id="d3348-129">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d3348-130">Afmörkun víddarstaks getur innihaldið gloppur, en stökin geta ekki skarast.</span><span class="sxs-lookup"><span data-stu-id="d3348-130">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
19. <span data-ttu-id="d3348-131">Í trénu skal velja „stigveldi kostnaðarhegðunar\Breytilegur kostnaður“.</span><span class="sxs-lookup"><span data-stu-id="d3348-131">In the tree, select 'Cost behavior hierarchy\Variable cost'.</span></span>
20. <span data-ttu-id="d3348-132">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d3348-132">Click New.</span></span>
21. <span data-ttu-id="d3348-133">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d3348-133">In the list, mark the selected row.</span></span>
22. <span data-ttu-id="d3348-134">Sláið inn eða veldu gildi í reitnum Frá víddarstak.</span><span class="sxs-lookup"><span data-stu-id="d3348-134">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d3348-135">Afmörkun víddarstaks getur innihaldið gloppur, en stökin geta ekki skarast.</span><span class="sxs-lookup"><span data-stu-id="d3348-135">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
23. <span data-ttu-id="d3348-136">Sláið inn eða veldu gildi í reitnum í Til víddarstak.</span><span class="sxs-lookup"><span data-stu-id="d3348-136">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="d3348-137">Afmörkun víddarstaks getur innihaldið gloppur, en stökin geta ekki skarast.</span><span class="sxs-lookup"><span data-stu-id="d3348-137">The range of dimension members can contain gaps, but the members cannot overlap.</span></span>  
24. <span data-ttu-id="d3348-138">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d3348-138">Click Save.</span></span>

## <a name="create-the-policy-and-rules"></a><span data-ttu-id="d3348-139">Stofna stefnu og reglur</span><span class="sxs-lookup"><span data-stu-id="d3348-139">Create the policy and rules</span></span>
1. <span data-ttu-id="d3348-140">Fara í Kostnaðarbókhald > Stefnur > Stefnur fyrir kostnaðarhegðun.</span><span class="sxs-lookup"><span data-stu-id="d3348-140">Go to Cost accounting > Policies > Cost behavior policies.</span></span>
2. <span data-ttu-id="d3348-141">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d3348-141">Click New.</span></span>
3. <span data-ttu-id="d3348-142">Sláið inn gildi í reitinn Stefnuheiti.</span><span class="sxs-lookup"><span data-stu-id="d3348-142">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="d3348-143">Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="d3348-143">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="d3348-144">Velja stigveldi stefnunnar sem nýverið var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="d3348-144">Select the policy hierarchy that you just created.</span></span>  
5. <span data-ttu-id="d3348-145">Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="d3348-145">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="d3348-146">Velja Fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="d3348-146">Select Organization.</span></span>  
6. <span data-ttu-id="d3348-147">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d3348-147">Click Save.</span></span>
7. <span data-ttu-id="d3348-148">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d3348-148">Click New.</span></span>
8. <span data-ttu-id="d3348-149">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d3348-149">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="d3348-150">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="d3348-150">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="d3348-151">Útvíkka stigveldið til að velja Breytilegur kostnaður.</span><span class="sxs-lookup"><span data-stu-id="d3348-151">Expand the hierarchy to select Variable cost.</span></span>  
10. <span data-ttu-id="d3348-152">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="d3348-152">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="d3348-153">Að sjálfgefnu er prósentan í breytilegu 100 prósent.</span><span class="sxs-lookup"><span data-stu-id="d3348-153">By default, the variable percentage is 100 percent.</span></span>  
11. <span data-ttu-id="d3348-154">Smella á Regluúthlutanir fyrir kostnaðarstýringareiningu.</span><span class="sxs-lookup"><span data-stu-id="d3348-154">Click Policy assignments for cost control unit.</span></span>
12. <span data-ttu-id="d3348-155">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d3348-155">Click New.</span></span>
13. <span data-ttu-id="d3348-156">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d3348-156">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="d3348-157">Færa skal inn dagsetningu í reitinn Gildir frá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="d3348-157">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="d3348-158">Reglurnar stjórnast af dagsetningum, og getur notandi eða kerfið látið reglurnar renna út ef nýrri útgáfa er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="d3348-158">The rules are date-effective, and a user or the system can expire a rule if a newer version is created.</span></span>  
15. <span data-ttu-id="d3348-159">Í reitinn Kostnaðarstýringareining skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="d3348-159">In the Cost control unit field, enter or select a value.</span></span>
16. <span data-ttu-id="d3348-160">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d3348-160">Click Save.</span></span>

