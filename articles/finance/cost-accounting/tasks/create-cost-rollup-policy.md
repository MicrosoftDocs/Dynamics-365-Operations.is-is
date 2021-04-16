---
title: Stofna reglu fyrir samantekt kostnaðar
description: Þetta ferli sýnir hvernig skal stofna stefnu fyrir samantekt kostnaðar og stofna reglur fyrir stefnuna.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 50a50dc359dc4c2741ac4d280a9f97c6a7f2c259
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810018"
---
# <a name="create-a-cost-rollup-policy"></a><span data-ttu-id="46515-103">Stofna reglu fyrir samantekt kostnaðar</span><span class="sxs-lookup"><span data-stu-id="46515-103">Create a cost rollup policy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="46515-104">Þetta ferli sýnir hvernig skal stofna stefnu fyrir samantekt kostnaðar og stofna reglur fyrir stefnuna.</span><span class="sxs-lookup"><span data-stu-id="46515-104">This procedure shows how to create a cost rollup policy and create rules for the policy.</span></span> <span data-ttu-id="46515-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USP2.</span><span class="sxs-lookup"><span data-stu-id="46515-105">The demo data used to create this procedure is USP2.</span></span>


## <a name="create-a-policy"></a><span data-ttu-id="46515-106">Stofna Stefnu</span><span class="sxs-lookup"><span data-stu-id="46515-106">Create a policy</span></span>
1. <span data-ttu-id="46515-107">Fara í Kostnaðarbókhald > Stefnur > Stefnur fyrir samantekt kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="46515-107">Go to Cost accounting > Policies > Cost rollup policies.</span></span>
2. <span data-ttu-id="46515-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="46515-108">Click New.</span></span>
3. <span data-ttu-id="46515-109">Sláið inn gildi í reitinn Stefnuheiti.</span><span class="sxs-lookup"><span data-stu-id="46515-109">In the Policy name field, type a value.</span></span>
4. <span data-ttu-id="46515-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="46515-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="46515-111">Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="46515-111">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="46515-112">Velja samantekt kostnaðar CC</span><span class="sxs-lookup"><span data-stu-id="46515-112">Select Cost rollup CC.</span></span>  
6. <span data-ttu-id="46515-113">Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="46515-113">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
    * <span data-ttu-id="46515-114">Velja samantekt kostnaðar CC</span><span class="sxs-lookup"><span data-stu-id="46515-114">Select Cost rollup CC.</span></span>  
7. <span data-ttu-id="46515-115">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="46515-115">Click Save.</span></span>

## <a name="create-rules-for-the-cost-rollup-policy"></a><span data-ttu-id="46515-116">Stofna reglur fyrir stefnuna fyrir samantekinn kostnað.</span><span class="sxs-lookup"><span data-stu-id="46515-116">Create rules for the cost rollup policy</span></span>
1. <span data-ttu-id="46515-117">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="46515-117">Click New.</span></span>
2. <span data-ttu-id="46515-118">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="46515-118">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="46515-119">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="46515-119">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="46515-120">Velja 007</span><span class="sxs-lookup"><span data-stu-id="46515-120">Select 007.</span></span>  
4. <span data-ttu-id="46515-121">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="46515-121">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="46515-122">Velja samantekt kostnaðar CE</span><span class="sxs-lookup"><span data-stu-id="46515-122">Select Cost rollup CE.</span></span>  
5. <span data-ttu-id="46515-123">Sláið inn eða veljið gildi í reitnum Aukakostnaðareining.</span><span class="sxs-lookup"><span data-stu-id="46515-123">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="46515-124">Í þessu dæmi skal varpa aukakostnaðareiningunni CC-007 til kostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="46515-124">For this example, map the secondary cost element CC-007 to the cost center.</span></span>  
6. <span data-ttu-id="46515-125">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="46515-125">Click New.</span></span>
7. <span data-ttu-id="46515-126">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="46515-126">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="46515-127">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="46515-127">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="46515-128">Velja 008.</span><span class="sxs-lookup"><span data-stu-id="46515-128">Select 008.</span></span>  
9. <span data-ttu-id="46515-129">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="46515-129">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="46515-130">Velja samantekt kostnaðar CE</span><span class="sxs-lookup"><span data-stu-id="46515-130">Select Cost rollup CE.</span></span>  
10. <span data-ttu-id="46515-131">Sláið inn eða veljið gildi í reitnum Aukakostnaðareining.</span><span class="sxs-lookup"><span data-stu-id="46515-131">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="46515-132">Í þessu dæmi skal varpa aukakostnaðareiningunni CC-008 til kostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="46515-132">For this example, map the secondary cost element CC-008 to the cost center.</span></span>  
11. <span data-ttu-id="46515-133">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="46515-133">Click New.</span></span>
12. <span data-ttu-id="46515-134">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="46515-134">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="46515-135">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="46515-135">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="46515-136">Velja 009.</span><span class="sxs-lookup"><span data-stu-id="46515-136">Select 009.</span></span>  
14. <span data-ttu-id="46515-137">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="46515-137">In the Cost element dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="46515-138">Velja samantekt kostnaðar CE</span><span class="sxs-lookup"><span data-stu-id="46515-138">Select Cost rollup CE.</span></span>  
15. <span data-ttu-id="46515-139">Sláið inn eða veljið gildi í reitnum Aukakostnaðareining.</span><span class="sxs-lookup"><span data-stu-id="46515-139">In the Secondary cost element field, enter or select a value.</span></span>
    * <span data-ttu-id="46515-140">Í þessu dæmi skal varpa aukakostnaðareiningunni CC-009 til kostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="46515-140">For this example, map the secondary cost element CC-009 to the cost center.</span></span>  
    * <span data-ttu-id="46515-141">Halda áfram þar til allir kostnaðarstaðir eru varpaðir til samsvarandi aukakostnaðareiningar þeirra.</span><span class="sxs-lookup"><span data-stu-id="46515-141">Continue until all cost centers are mapped to their corresponding secondary cost elements.</span></span>  
16. <span data-ttu-id="46515-142">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="46515-142">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]