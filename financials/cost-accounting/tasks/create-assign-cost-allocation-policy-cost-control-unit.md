--- 
title: "Stofna og úthluta kostnaðarúthlutunarreglu fyrir kostnaðarstýringareiningu"
description: "Nota þetta ferli til að stofna og úthluta stefnu kostnaðarúthlutunar og samsvarandir reglum til kostnaðarstýringareiningar."
author: YuyuScheller
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 491d8292b7c951be930d2858362c8107caaa76ff
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="d803f-103">Stofna og úthluta kostnaðarúthlutunarreglu fyrir kostnaðarstýringareiningu</span><span class="sxs-lookup"><span data-stu-id="d803f-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d803f-104">Nota þetta ferli til að stofna og úthluta stefnu kostnaðarúthlutunar og samsvarandir reglum til kostnaðarstýringareiningar.</span><span class="sxs-lookup"><span data-stu-id="d803f-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="d803f-105">Þessi skráning notar USP2-sýnigagnafyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="d803f-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="d803f-106">Stofna Stefnu</span><span class="sxs-lookup"><span data-stu-id="d803f-106">Create a policy</span></span>
1. <span data-ttu-id="d803f-107">Fara í Kostnaðarbókhald > Stefnur > Stefnur fyrir kostnaðarúthlutun.</span><span class="sxs-lookup"><span data-stu-id="d803f-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="d803f-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d803f-108">Click New.</span></span>
3. <span data-ttu-id="d803f-109">Sláið inn gildi í reitinn Stefnuheiti.</span><span class="sxs-lookup"><span data-stu-id="d803f-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="d803f-110">Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="d803f-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="d803f-111">Velja Fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="d803f-111">Select Organization.</span></span>  
5. <span data-ttu-id="d803f-112">Sláið inn eða veljið gildi í reitnum Tölfræðileg vídd.</span><span class="sxs-lookup"><span data-stu-id="d803f-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="d803f-113">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d803f-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="d803f-114">Stofna úthlutunarreglur</span><span class="sxs-lookup"><span data-stu-id="d803f-114">Create allocation rules</span></span>
1. <span data-ttu-id="d803f-115">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d803f-115">Click New.</span></span>
2. <span data-ttu-id="d803f-116">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d803f-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="d803f-117">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="d803f-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="d803f-118">Veljið „Samtals“ í svæðinu Kostnaðarhegðun.</span><span class="sxs-lookup"><span data-stu-id="d803f-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="d803f-119">Sláið inn eða veldu gildi í Úthlutunargrunnur reitnum.</span><span class="sxs-lookup"><span data-stu-id="d803f-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="d803f-120">Smellið á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="d803f-120">Click New.</span></span>
7. <span data-ttu-id="d803f-121">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d803f-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="d803f-122">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="d803f-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="d803f-123">Veljið „Samtals“ í svæðinu Kostnaðarhegðun.</span><span class="sxs-lookup"><span data-stu-id="d803f-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="d803f-124">Sláið inn eða veldu gildi í Úthlutunargrunnur reitnum.</span><span class="sxs-lookup"><span data-stu-id="d803f-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="d803f-125">Smellið á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="d803f-125">Click New.</span></span>
12. <span data-ttu-id="d803f-126">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d803f-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="d803f-127">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="d803f-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="d803f-128">Veljið „Samtals“ í svæðinu Kostnaðarhegðun.</span><span class="sxs-lookup"><span data-stu-id="d803f-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="d803f-129">Sláið inn eða veldu gildi í Úthlutunargrunnur reitnum.</span><span class="sxs-lookup"><span data-stu-id="d803f-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="d803f-130">Halda áfram þar til þú hefur stofnað allar reglurnar.</span><span class="sxs-lookup"><span data-stu-id="d803f-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="d803f-131">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d803f-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="d803f-132">Úthluta stefnunni til kostnaðarstýringareiningar</span><span class="sxs-lookup"><span data-stu-id="d803f-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="d803f-133">Smella á Regluúthlutanir fyrir kostnaðarstýringareiningu.</span><span class="sxs-lookup"><span data-stu-id="d803f-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="d803f-134">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d803f-134">Click New.</span></span>
3. <span data-ttu-id="d803f-135">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d803f-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d803f-136">Færa skal inn dagsetningu í reitinn Gildir frá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="d803f-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="d803f-137">Reglurnar stjórnast af dagsetningum.</span><span class="sxs-lookup"><span data-stu-id="d803f-137">The rules are date-effective.</span></span> <span data-ttu-id="d803f-138">Notandi eða kerfið getur látið reglurnar renna út ef nýrri útgáfa er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="d803f-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="d803f-139">Í reitinn Kostnaðarstýringareining skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="d803f-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="d803f-140">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d803f-140">Click Save.</span></span>


