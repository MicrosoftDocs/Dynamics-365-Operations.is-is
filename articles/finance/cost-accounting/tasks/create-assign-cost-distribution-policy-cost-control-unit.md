---
title: Stofna og úthluta kostnaðardreifingarreglu fyrir kostnaðarstýringareiningu
description: Kostnaðardreifingarreglur eru notaðar til að dreifa kostnaði sem hefur verið fjárhagslega talinn á sameiginlegum kostnaðarstað.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMCostDistributionRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 66921d5eddb31ffba0946c41f634719a684e4ad1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444312"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="d32aa-103">Stofna og úthluta kostnaðardreifingarreglu fyrir kostnaðarstýringareiningu</span><span class="sxs-lookup"><span data-stu-id="d32aa-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d32aa-104">Kostnaðardreifingarreglur eru notaðar til að dreifa kostnaði sem hefur verið fjárhagslega talinn á sameiginlegum kostnaðarstað.</span><span class="sxs-lookup"><span data-stu-id="d32aa-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="d32aa-105">Endurskoðandi kostnaðar gengur úr skugga um að kostnaði sé dreift til kostnaðarstaða, út frá völdum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="d32aa-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="d32aa-106">Stefna og samsvarandi reglur er úthlutað til kostnaðarstýringareiningar.</span><span class="sxs-lookup"><span data-stu-id="d32aa-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="d32aa-107">Þessar verkefnaleiðbeiningar nota dæmi til að sýna hvernig skal stofna kostnaðardreifingarstefnu og samsvarandi reglur.</span><span class="sxs-lookup"><span data-stu-id="d32aa-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="d32aa-108">Stofna Stefnu</span><span class="sxs-lookup"><span data-stu-id="d32aa-108">Create a policy</span></span>
1. <span data-ttu-id="d32aa-109">Fara í Kostnaðarbókhald > Stefnur > Stefnur fyrir kostnaðardreifingu.</span><span class="sxs-lookup"><span data-stu-id="d32aa-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="d32aa-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d32aa-110">Click New.</span></span>
3. <span data-ttu-id="d32aa-111">Sláið inn gildi í reitinn Stefnuheiti.</span><span class="sxs-lookup"><span data-stu-id="d32aa-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="d32aa-112">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="d32aa-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d32aa-113">Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="d32aa-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="d32aa-114">Velja Fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="d32aa-114">Select Organization.</span></span>  
6. <span data-ttu-id="d32aa-115">Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="d32aa-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="d32aa-116">Velja CDS P/L.</span><span class="sxs-lookup"><span data-stu-id="d32aa-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="d32aa-117">Sláið inn eða veljið gildi í reitnum Tölfræðileg vídd.</span><span class="sxs-lookup"><span data-stu-id="d32aa-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="d32aa-118">Velja skal Tölfræðilegar einingar.</span><span class="sxs-lookup"><span data-stu-id="d32aa-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="d32aa-119">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d32aa-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="d32aa-120">Stofna reglur fyrir stefnuna</span><span class="sxs-lookup"><span data-stu-id="d32aa-120">Create rules for the policy</span></span>
1. <span data-ttu-id="d32aa-121">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d32aa-121">Click New.</span></span>
2. <span data-ttu-id="d32aa-122">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d32aa-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="d32aa-123">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="d32aa-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="d32aa-124">Útvíkka stigveldið til að velja 094.</span><span class="sxs-lookup"><span data-stu-id="d32aa-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="d32aa-125">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="d32aa-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="d32aa-126">Velja Annar rekstrarkostnaður og veljið síðan 605110 Hreinsun.</span><span class="sxs-lookup"><span data-stu-id="d32aa-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="d32aa-127">Veljið valkost í svæðinu Kostnaðarhegðun.</span><span class="sxs-lookup"><span data-stu-id="d32aa-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="d32aa-128">Velja Fastur kostnaður.</span><span class="sxs-lookup"><span data-stu-id="d32aa-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="d32aa-129">Sláið inn eða veldu gildi í Úthlutunargrunnur reitnum.</span><span class="sxs-lookup"><span data-stu-id="d32aa-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="d32aa-130">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d32aa-130">Click New.</span></span>
8. <span data-ttu-id="d32aa-131">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d32aa-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="d32aa-132">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="d32aa-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="d32aa-133">Útvíkka stigveldið til að velja 094.</span><span class="sxs-lookup"><span data-stu-id="d32aa-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="d32aa-134">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="d32aa-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="d32aa-135">Velja Annar rekstrarkostnaður og veljið síðan 605150 Leiga.</span><span class="sxs-lookup"><span data-stu-id="d32aa-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="d32aa-136">Veljið valkost í svæðinu Kostnaðarhegðun.</span><span class="sxs-lookup"><span data-stu-id="d32aa-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="d32aa-137">Velja Fastur kostnaður.</span><span class="sxs-lookup"><span data-stu-id="d32aa-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="d32aa-138">Sláið inn eða veldu gildi í Úthlutunargrunnur reitnum.</span><span class="sxs-lookup"><span data-stu-id="d32aa-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="d32aa-139">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d32aa-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="d32aa-140">Úthluta reglum til kostnaðarstýringareiningar</span><span class="sxs-lookup"><span data-stu-id="d32aa-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="d32aa-141">Smella á Regluúthlutanir fyrir kostnaðarstýringareiningu.</span><span class="sxs-lookup"><span data-stu-id="d32aa-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="d32aa-142">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d32aa-142">Click New.</span></span>
3. <span data-ttu-id="d32aa-143">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d32aa-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d32aa-144">Færa skal inn dagsetningu í reitinn Gildir frá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="d32aa-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="d32aa-145">Velja 1. september í gildu fjárhagsárinu.</span><span class="sxs-lookup"><span data-stu-id="d32aa-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="d32aa-146">Í reitinn Kostnaðarstýringareining skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="d32aa-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="d32aa-147">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d32aa-147">Click Save.</span></span>

