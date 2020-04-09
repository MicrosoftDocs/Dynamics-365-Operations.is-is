---
title: Stofna og úthluta kostnaðarúthlutunarreglu fyrir kostnaðarstýringareiningu
description: Nota þetta ferli til að stofna og úthluta stefnu kostnaðarúthlutunar og samsvarandir reglum til kostnaðarstýringareiningar.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a4ba39b5dbba20a58066054da2e24613381cfaa
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3144437"
---
# <a name="create-and-assign-a-cost-allocation-policy-to-a-cost-control-unit"></a><span data-ttu-id="dbdbb-103">Stofna og úthluta kostnaðarúthlutunarreglu fyrir kostnaðarstýringareiningu</span><span class="sxs-lookup"><span data-stu-id="dbdbb-103">Create and assign a cost allocation policy to a cost control unit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dbdbb-104">Nota þetta ferli til að stofna og úthluta stefnu kostnaðarúthlutunar og samsvarandir reglum til kostnaðarstýringareiningar.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-104">Use this procedure to create and assign a cost allocation policy and the corresponding rules to a cost control unit.</span></span> <span data-ttu-id="dbdbb-105">Þessi skráning notar USP2-sýnigagnafyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-105">This recording uses the USP2 demo data company.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="dbdbb-106">Stofna Stefnu</span><span class="sxs-lookup"><span data-stu-id="dbdbb-106">Create a policy</span></span>
1. <span data-ttu-id="dbdbb-107">Fara í Kostnaðarbókhald > Stefnur > Stefnur fyrir kostnaðarúthlutun.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-107">Go to Cost accounting > Policies > Cost allocation policies.</span></span>
2. <span data-ttu-id="dbdbb-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-108">Click New.</span></span>
3. <span data-ttu-id="dbdbb-109">Sláið inn gildi í reitinn Stefnuheiti.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="dbdbb-110">Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-110">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="dbdbb-111">Velja Fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="dbdbb-111">Select Organization.</span></span>  
5. <span data-ttu-id="dbdbb-112">Sláið inn eða veljið gildi í reitnum Tölfræðileg vídd.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-112">In the Statistical dimension field, enter or select a value.</span></span>
6. <span data-ttu-id="dbdbb-113">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-113">Click Save.</span></span>

## <a name="create-allocation-rules"></a><span data-ttu-id="dbdbb-114">Stofna úthlutunarreglur</span><span class="sxs-lookup"><span data-stu-id="dbdbb-114">Create allocation rules</span></span>
1. <span data-ttu-id="dbdbb-115">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-115">Click New.</span></span>
2. <span data-ttu-id="dbdbb-116">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-116">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="dbdbb-117">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-117">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
4. <span data-ttu-id="dbdbb-118">Veljið „Samtals“ í svæðinu Kostnaðarhegðun.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-118">In the Cost behavior field, select 'Total'.</span></span>
5. <span data-ttu-id="dbdbb-119">Sláið inn eða veldu gildi í Úthlutunargrunnur reitnum.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-119">In the Allocation base field, enter or select a value.</span></span>
6. <span data-ttu-id="dbdbb-120">Smellið á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-120">Click New.</span></span>
7. <span data-ttu-id="dbdbb-121">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-121">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="dbdbb-122">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-122">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
9. <span data-ttu-id="dbdbb-123">Veljið „Samtals“ í svæðinu Kostnaðarhegðun.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-123">In the Cost behavior field, select 'Total'.</span></span>
10. <span data-ttu-id="dbdbb-124">Sláið inn eða veldu gildi í Úthlutunargrunnur reitnum.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-124">In the Allocation base field, enter or select a value.</span></span>
11. <span data-ttu-id="dbdbb-125">Smellið á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-125">Click New.</span></span>
12. <span data-ttu-id="dbdbb-126">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-126">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="dbdbb-127">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
14. <span data-ttu-id="dbdbb-128">Veljið „Samtals“ í svæðinu Kostnaðarhegðun.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-128">In the Cost behavior field, select 'Total'.</span></span>
15. <span data-ttu-id="dbdbb-129">Sláið inn eða veldu gildi í Úthlutunargrunnur reitnum.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-129">In the Allocation base field, enter or select a value.</span></span>
    * <span data-ttu-id="dbdbb-130">Halda áfram þar til þú hefur stofnað allar reglurnar.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-130">Continue until you've created all the rules.</span></span>  
16. <span data-ttu-id="dbdbb-131">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-131">Click Save.</span></span>

## <a name="assign-the-policy-to-a-cost-control-unit"></a><span data-ttu-id="dbdbb-132">Úthluta stefnunni til kostnaðarstýringareiningar</span><span class="sxs-lookup"><span data-stu-id="dbdbb-132">Assign the policy to a cost control unit</span></span>
1. <span data-ttu-id="dbdbb-133">Smella á Regluúthlutanir fyrir kostnaðarstýringareiningu.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-133">Click Policy assignments for cost control unit.</span></span>
2. <span data-ttu-id="dbdbb-134">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-134">Click New.</span></span>
3. <span data-ttu-id="dbdbb-135">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-135">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="dbdbb-136">Færa skal inn dagsetningu í reitinn Gildir frá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-136">In the Valid from accounting date field, enter a date.</span></span>
    * <span data-ttu-id="dbdbb-137">Reglurnar stjórnast af dagsetningum.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-137">The rules are date-effective.</span></span> <span data-ttu-id="dbdbb-138">Notandi eða kerfið getur látið reglurnar renna út ef nýrri útgáfa er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-138">A user or the system can expire the rules if a newer version is created.</span></span>  
5. <span data-ttu-id="dbdbb-139">Í reitinn Kostnaðarstýringareining skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-139">In the Cost control unit field, enter or select a value.</span></span>
6. <span data-ttu-id="dbdbb-140">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="dbdbb-140">Click Save.</span></span>

