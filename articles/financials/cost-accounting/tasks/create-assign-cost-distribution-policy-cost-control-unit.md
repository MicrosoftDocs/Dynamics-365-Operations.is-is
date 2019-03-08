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
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 46ba6322f2cea7828033c214502accdf73f073be
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "308461"
---
# <a name="create-and-assign-a-cost-distribution-policy-to-a-cost-control-unit"></a><span data-ttu-id="90eaa-103">Stofna og úthluta kostnaðardreifingarreglu fyrir kostnaðarstýringareiningu</span><span class="sxs-lookup"><span data-stu-id="90eaa-103">Create and assign a cost distribution policy to a cost control unit</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="90eaa-104">Kostnaðardreifingarreglur eru notaðar til að dreifa kostnaði sem hefur verið fjárhagslega talinn á sameiginlegum kostnaðarstað.</span><span class="sxs-lookup"><span data-stu-id="90eaa-104">Cost distribution rules are used to distribute costs that have been financially counted on a collective cost center.</span></span> <span data-ttu-id="90eaa-105">Endurskoðandi kostnaðar gengur úr skugga um að kostnaði sé dreift til kostnaðarstaða, út frá völdum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="90eaa-105">The cost accountant makes sure that the cost is distributed to the cost centers, based on the selected allocation base.</span></span> <span data-ttu-id="90eaa-106">Stefna og samsvarandi reglur er úthlutað til kostnaðarstýringareiningar.</span><span class="sxs-lookup"><span data-stu-id="90eaa-106">A policy and the corresponding rules are assigned to a cost control unit.</span></span> <span data-ttu-id="90eaa-107">Þessar verkefnaleiðbeiningar nota dæmi til að sýna hvernig skal stofna kostnaðardreifingarstefnu og samsvarandi reglur.</span><span class="sxs-lookup"><span data-stu-id="90eaa-107">This task guide uses an example to show how to create a cost distribution policy and the corresponding rules.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="90eaa-108">Stofna Stefnu</span><span class="sxs-lookup"><span data-stu-id="90eaa-108">Create a policy</span></span>
1. <span data-ttu-id="90eaa-109">Fara í Kostnaðarbókhald > Stefnur > Stefnur fyrir kostnaðardreifingu.</span><span class="sxs-lookup"><span data-stu-id="90eaa-109">Go to Cost accounting > Policies > Cost distribution policies.</span></span>
2. <span data-ttu-id="90eaa-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="90eaa-110">Click New.</span></span>
3. <span data-ttu-id="90eaa-111">Sláið inn gildi í reitinn Stefnuheiti.</span><span class="sxs-lookup"><span data-stu-id="90eaa-111">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="90eaa-112">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="90eaa-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="90eaa-113">Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="90eaa-113">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="90eaa-114">Velja Fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="90eaa-114">Select Organization.</span></span>  
6. <span data-ttu-id="90eaa-115">Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="90eaa-115">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="90eaa-116">Velja CDS P/L.</span><span class="sxs-lookup"><span data-stu-id="90eaa-116">Select CDS P/L.</span></span>  
7. <span data-ttu-id="90eaa-117">Sláið inn eða veljið gildi í reitnum Tölfræðileg vídd.</span><span class="sxs-lookup"><span data-stu-id="90eaa-117">In the Statistical dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="90eaa-118">Velja skal Tölfræðilegar einingar.</span><span class="sxs-lookup"><span data-stu-id="90eaa-118">Select Statistical elements.</span></span>  
8. <span data-ttu-id="90eaa-119">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="90eaa-119">Click Save.</span></span>

## <a name="create-rules-for-the-policy"></a><span data-ttu-id="90eaa-120">Stofna reglur fyrir stefnuna</span><span class="sxs-lookup"><span data-stu-id="90eaa-120">Create rules for the policy</span></span>
1. <span data-ttu-id="90eaa-121">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="90eaa-121">Click New.</span></span>
2. <span data-ttu-id="90eaa-122">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="90eaa-122">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="90eaa-123">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="90eaa-123">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="90eaa-124">Útvíkka stigveldið til að velja 094.</span><span class="sxs-lookup"><span data-stu-id="90eaa-124">Expand the hierarchy to select 094.</span></span>  
4. <span data-ttu-id="90eaa-125">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="90eaa-125">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="90eaa-126">Velja Annar rekstrarkostnaður og veljið síðan 605110 Hreinsun.</span><span class="sxs-lookup"><span data-stu-id="90eaa-126">Select Other operating expenses and then select 605110 Cleaning.</span></span>  
5. <span data-ttu-id="90eaa-127">Veljið valkost í svæðinu Kostnaðarhegðun.</span><span class="sxs-lookup"><span data-stu-id="90eaa-127">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="90eaa-128">Velja Fastur kostnaður.</span><span class="sxs-lookup"><span data-stu-id="90eaa-128">Select Fixed cost.</span></span>  
6. <span data-ttu-id="90eaa-129">Sláið inn eða veldu gildi í Úthlutunargrunnur reitnum.</span><span class="sxs-lookup"><span data-stu-id="90eaa-129">In the Allocation base field, enter or select a value.</span></span>
7. <span data-ttu-id="90eaa-130">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="90eaa-130">Click New.</span></span>
8. <span data-ttu-id="90eaa-131">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="90eaa-131">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="90eaa-132">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="90eaa-132">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="90eaa-133">Útvíkka stigveldið til að velja 094.</span><span class="sxs-lookup"><span data-stu-id="90eaa-133">Expand the hierarchy to select 094.</span></span>  
10. <span data-ttu-id="90eaa-134">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="90eaa-134">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="90eaa-135">Velja Annar rekstrarkostnaður og veljið síðan 605150 Leiga.</span><span class="sxs-lookup"><span data-stu-id="90eaa-135">Select Other operating expenses and then select 605150 Rent.</span></span>  
11. <span data-ttu-id="90eaa-136">Veljið valkost í svæðinu Kostnaðarhegðun.</span><span class="sxs-lookup"><span data-stu-id="90eaa-136">In the Cost behavior field, select an option.</span></span>
    * <span data-ttu-id="90eaa-137">Velja Fastur kostnaður.</span><span class="sxs-lookup"><span data-stu-id="90eaa-137">Select Fixed cost.</span></span>  
12. <span data-ttu-id="90eaa-138">Sláið inn eða veldu gildi í Úthlutunargrunnur reitnum.</span><span class="sxs-lookup"><span data-stu-id="90eaa-138">In the Allocation base field, enter or select a value.</span></span>
13. <span data-ttu-id="90eaa-139">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="90eaa-139">Click Save.</span></span>

## <a name="assign-rules-to-a-cost-control-unit"></a><span data-ttu-id="90eaa-140">Úthluta reglum til kostnaðarstýringareiningar</span><span class="sxs-lookup"><span data-stu-id="90eaa-140">Assign rules to a cost control unit</span></span>
1. <span data-ttu-id="90eaa-141">Smella á Regluúthlutanir fyrir kostnaðarstýringareiningu.</span><span class="sxs-lookup"><span data-stu-id="90eaa-141">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="90eaa-142">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="90eaa-142">Click New.</span></span>
3. <span data-ttu-id="90eaa-143">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="90eaa-143">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="90eaa-144">Færa skal inn dagsetningu í reitinn Gildir frá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="90eaa-144">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="90eaa-145">Velja 1. september í gildu fjárhagsárinu.</span><span class="sxs-lookup"><span data-stu-id="90eaa-145">Select September 1 in the valid fiscal year.</span></span>  
5. <span data-ttu-id="90eaa-146">Í reitinn Kostnaðarstýringareining skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="90eaa-146">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="90eaa-147">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="90eaa-147">Click Save.</span></span>

