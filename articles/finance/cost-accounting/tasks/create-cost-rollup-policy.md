---
title: Stofna reglu fyrir samantekt kostnaðar
description: Þetta ferli sýnir hvernig skal stofna stefnu fyrir samantekt kostnaðar og stofna reglur fyrir stefnuna.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
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
ms.openlocfilehash: ff37655150596a4be8088e20b43f626f97262aba
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3137846"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="0e0cc-103">Stofna reglu fyrir samantekt kostnaðar</span><span class="sxs-lookup"><span data-stu-id="0e0cc-103">Create a cost rollup policy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e0cc-104">Þetta ferli sýnir hvernig skal stofna stefnu fyrir samantekt kostnaðar og stofna reglur fyrir stefnuna.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="0e0cc-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USP2.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="0e0cc-106">Stofna Stefnu</span><span class="sxs-lookup"><span data-stu-id="0e0cc-106">Create a policy</span></span>
1. <span data-ttu-id="0e0cc-107">Fara í Kostnaðarbókhald > Stefnur > Stefnur fyrir samantekt kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="0e0cc-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-108">Click New.</span></span>
3. <span data-ttu-id="0e0cc-109">Sláið inn gildi í reitinn Stefnuheiti.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="0e0cc-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0e0cc-111">Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="0e0cc-112">Velja samantekt kostnaðar CC</span><span class="sxs-lookup"><span data-stu-id="0e0cc-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="0e0cc-113">Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="0e0cc-114">Velja samantekt kostnaðar CC</span><span class="sxs-lookup"><span data-stu-id="0e0cc-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="0e0cc-115">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="0e0cc-116">Stofna reglur fyrir stefnuna fyrir samantekinn kostnað.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="0e0cc-117">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-117">Click New.</span></span>
2. <span data-ttu-id="0e0cc-118">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="0e0cc-119">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="0e0cc-120">Velja 007</span><span class="sxs-lookup"><span data-stu-id="0e0cc-120">Select 007.</span></span>  
4. <span data-ttu-id="0e0cc-121">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="0e0cc-122">Velja samantekt kostnaðar CE</span><span class="sxs-lookup"><span data-stu-id="0e0cc-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="0e0cc-123">Sláið inn eða veljið gildi í reitnum Aukakostnaðareining.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="0e0cc-124">Í þessu dæmi skal varpa aukakostnaðareiningunni CC-007 til kostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="0e0cc-125">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-125">Click New.</span></span>
7. <span data-ttu-id="0e0cc-126">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="0e0cc-127">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="0e0cc-128">Velja 008.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-128">Select 008.</span></span>  
9. <span data-ttu-id="0e0cc-129">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="0e0cc-130">Velja samantekt kostnaðar CE</span><span class="sxs-lookup"><span data-stu-id="0e0cc-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="0e0cc-131">Sláið inn eða veljið gildi í reitnum Aukakostnaðareining.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="0e0cc-132">Í þessu dæmi skal varpa aukakostnaðareiningunni CC-008 til kostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="0e0cc-133">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-133">Click New.</span></span>
12. <span data-ttu-id="0e0cc-134">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="0e0cc-135">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="0e0cc-136">Velja 009.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-136">Select 009.</span></span>  
14. <span data-ttu-id="0e0cc-137">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="0e0cc-138">Velja samantekt kostnaðar CE</span><span class="sxs-lookup"><span data-stu-id="0e0cc-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="0e0cc-139">Sláið inn eða veljið gildi í reitnum Aukakostnaðareining.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="0e0cc-140">Í þessu dæmi skal varpa aukakostnaðareiningunni CC-009 til kostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="0e0cc-141">Halda áfram þar til allir kostnaðarstaðir eru varpaðir til samsvarandi aukakostnaðareiningar þeirra.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="0e0cc-142">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="0e0cc-142">Click Save.</span></span>

