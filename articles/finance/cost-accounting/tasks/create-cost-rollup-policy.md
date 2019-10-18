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
ms.openlocfilehash: facffeaf8d880bad01877b420197e29b6791ebbf
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187775"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="c9e85-103">Stofna reglu fyrir samantekt kostnaðar</span><span class="sxs-lookup"><span data-stu-id="c9e85-103">Create a cost rollup policy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c9e85-104">Þetta ferli sýnir hvernig skal stofna stefnu fyrir samantekt kostnaðar og stofna reglur fyrir stefnuna.</span><span class="sxs-lookup"><span data-stu-id="c9e85-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="c9e85-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USP2.</span><span class="sxs-lookup"><span data-stu-id="c9e85-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="c9e85-106">Stofna Stefnu</span><span class="sxs-lookup"><span data-stu-id="c9e85-106">Create a policy</span></span>
1. <span data-ttu-id="c9e85-107">Fara í Kostnaðarbókhald > Stefnur > Stefnur fyrir samantekt kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="c9e85-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="c9e85-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="c9e85-108">Click New.</span></span>
3. <span data-ttu-id="c9e85-109">Sláið inn gildi í reitinn Stefnuheiti.</span><span class="sxs-lookup"><span data-stu-id="c9e85-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="c9e85-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="c9e85-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c9e85-111">Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="c9e85-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="c9e85-112">Velja samantekt kostnaðar CC</span><span class="sxs-lookup"><span data-stu-id="c9e85-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="c9e85-113">Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="c9e85-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="c9e85-114">Velja samantekt kostnaðar CC</span><span class="sxs-lookup"><span data-stu-id="c9e85-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="c9e85-115">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="c9e85-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="c9e85-116">Stofna reglur fyrir stefnuna fyrir samantekinn kostnað.</span><span class="sxs-lookup"><span data-stu-id="c9e85-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="c9e85-117">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="c9e85-117">Click New.</span></span>
2. <span data-ttu-id="c9e85-118">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="c9e85-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="c9e85-119">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="c9e85-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c9e85-120">Velja 007</span><span class="sxs-lookup"><span data-stu-id="c9e85-120">Select 007.</span></span>  
4. <span data-ttu-id="c9e85-121">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="c9e85-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c9e85-122">Velja samantekt kostnaðar CE</span><span class="sxs-lookup"><span data-stu-id="c9e85-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="c9e85-123">Sláið inn eða veljið gildi í reitnum Aukakostnaðareining.</span><span class="sxs-lookup"><span data-stu-id="c9e85-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="c9e85-124">Í þessu dæmi skal varpa aukakostnaðareiningunni CC-007 til kostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="c9e85-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="c9e85-125">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="c9e85-125">Click New.</span></span>
7. <span data-ttu-id="c9e85-126">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="c9e85-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="c9e85-127">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="c9e85-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c9e85-128">Velja 008.</span><span class="sxs-lookup"><span data-stu-id="c9e85-128">Select 008.</span></span>  
9. <span data-ttu-id="c9e85-129">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="c9e85-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c9e85-130">Velja samantekt kostnaðar CE</span><span class="sxs-lookup"><span data-stu-id="c9e85-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="c9e85-131">Sláið inn eða veljið gildi í reitnum Aukakostnaðareining.</span><span class="sxs-lookup"><span data-stu-id="c9e85-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="c9e85-132">Í þessu dæmi skal varpa aukakostnaðareiningunni CC-008 til kostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="c9e85-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="c9e85-133">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="c9e85-133">Click New.</span></span>
12. <span data-ttu-id="c9e85-134">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="c9e85-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="c9e85-135">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="c9e85-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c9e85-136">Velja 009.</span><span class="sxs-lookup"><span data-stu-id="c9e85-136">Select 009.</span></span>  
14. <span data-ttu-id="c9e85-137">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="c9e85-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="c9e85-138">Velja samantekt kostnaðar CE</span><span class="sxs-lookup"><span data-stu-id="c9e85-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="c9e85-139">Sláið inn eða veljið gildi í reitnum Aukakostnaðareining.</span><span class="sxs-lookup"><span data-stu-id="c9e85-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="c9e85-140">Í þessu dæmi skal varpa aukakostnaðareiningunni CC-009 til kostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="c9e85-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="c9e85-141">Halda áfram þar til allir kostnaðarstaðir eru varpaðir til samsvarandi aukakostnaðareiningar þeirra.</span><span class="sxs-lookup"><span data-stu-id="c9e85-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="c9e85-142">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="c9e85-142">Click Save.</span></span>

