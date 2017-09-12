--- 
title: "Búa til efnisáætlun fyrir aukaafurðir"
description: "Framleiðslustjóri áætlar efnisþarfir fyrir vörur sem eru aukaafurðir formúlu."
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: c8805ca02525ae001fbd5e10ad9405fe60c7473e
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="393e2-103">Búa til efnisáætlun fyrir aukaafurðir</span><span class="sxs-lookup"><span data-stu-id="393e2-103">Create a material plan for co-products</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="393e2-104">Framleiðslustjóri áætlar efnisþarfir fyrir vörur sem eru aukaafurðir formúlu.</span><span class="sxs-lookup"><span data-stu-id="393e2-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="393e2-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USP2.</span><span class="sxs-lookup"><span data-stu-id="393e2-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="393e2-106">Stofna þörf fyrir aukaafurð</span><span class="sxs-lookup"><span data-stu-id="393e2-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="393e2-107">Farðu í Sjálfgefið mælaborð.</span><span class="sxs-lookup"><span data-stu-id="393e2-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="393e2-108">Smellt er á Vinnsla og fyrirspurnir sölupantana.</span><span class="sxs-lookup"><span data-stu-id="393e2-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="393e2-109">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="393e2-109">Click New.</span></span>
4. <span data-ttu-id="393e2-110">Smellt er á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="393e2-110">Click Sales order.</span></span>
5. <span data-ttu-id="393e2-111">Í reitinn Reikningur viðskiptavinar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="393e2-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="393e2-112">Dæmi: US-001</span><span class="sxs-lookup"><span data-stu-id="393e2-112">Example: US-001</span></span>  
6. <span data-ttu-id="393e2-113">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="393e2-113">Click OK.</span></span>
7. <span data-ttu-id="393e2-114">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="393e2-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="393e2-115">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="393e2-115">Example: P6003</span></span>  
8. <span data-ttu-id="393e2-116">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="393e2-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="393e2-117">Til dæmis: 50000.</span><span class="sxs-lookup"><span data-stu-id="393e2-117">Example: 50000</span></span>  
9. <span data-ttu-id="393e2-118">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="393e2-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="393e2-119">Búa til efnisáætlun fyrir aukaafurðir</span><span class="sxs-lookup"><span data-stu-id="393e2-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="393e2-120">Smellt er á aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="393e2-120">Click Master planning.</span></span>
2. <span data-ttu-id="393e2-121">Í reitnum Áætlun skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="393e2-121">In the Plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="393e2-122">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="393e2-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="393e2-123">Dæmi: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="393e2-123">Example: MasterPlan</span></span>  
4. <span data-ttu-id="393e2-124">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="393e2-124">Click Run.</span></span>
5. <span data-ttu-id="393e2-125">Útvíkka eða draga saman Færslur sem á að taka með hluta.</span><span class="sxs-lookup"><span data-stu-id="393e2-125">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="393e2-126">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="393e2-126">Click Filter.</span></span>
7. <span data-ttu-id="393e2-127">Á listanum, Velja línuna fyrir svæðið = vörunúmer</span><span class="sxs-lookup"><span data-stu-id="393e2-127">In the list, select the row for Field = Item number.</span></span>
8. <span data-ttu-id="393e2-128">Í reitinn Skilyrði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="393e2-128">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="393e2-129">Til dæmis: P6003</span><span class="sxs-lookup"><span data-stu-id="393e2-129">Example: P6003</span></span>  
9. <span data-ttu-id="393e2-130">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="393e2-130">Click OK.</span></span>
10. <span data-ttu-id="393e2-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="393e2-131">Click OK.</span></span>
11. <span data-ttu-id="393e2-132">Smellt er á Áætlaðar pantanir.</span><span class="sxs-lookup"><span data-stu-id="393e2-132">Click Planned orders.</span></span>
12. <span data-ttu-id="393e2-133">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="393e2-133">Use the Quick Filter to find records.</span></span> <span data-ttu-id="393e2-134">Til dæmis, sía svæðið vörunúmer með gildið 'P6000'.</span><span class="sxs-lookup"><span data-stu-id="393e2-134">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="393e2-135">Sía eftir formúluvöru sem hefur aukaafurð vöru sem stofnuð var sölupöntun fyrir.</span><span class="sxs-lookup"><span data-stu-id="393e2-135">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
13. <span data-ttu-id="393e2-136">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="393e2-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="393e2-137">Velja allar línur sem sían skilaði.</span><span class="sxs-lookup"><span data-stu-id="393e2-137">Select any of the rows returned by the filter.</span></span>  
14. <span data-ttu-id="393e2-138">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="393e2-138">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="393e2-139">Útvíkka eða draga saman hlutann Þarfarakning.</span><span class="sxs-lookup"><span data-stu-id="393e2-139">Expand or collapse the Pegging section.</span></span>
16. <span data-ttu-id="393e2-140">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="393e2-140">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="393e2-141">Áætluð pöntun er fest við sölupöntun fyrir aukaafurðina.</span><span class="sxs-lookup"><span data-stu-id="393e2-141">The planned order is pegged to the sales order for the co-product.</span></span>  
17. <span data-ttu-id="393e2-142">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="393e2-142">Close the page.</span></span>


