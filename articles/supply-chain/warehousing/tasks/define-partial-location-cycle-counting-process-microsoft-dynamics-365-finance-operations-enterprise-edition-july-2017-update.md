--- 
title: "Skilgreina hlutastaðsetning reglulegrar talningar "
description: "Þegar þú notar áætlun um reglulega talningu til að stofna talningarvinnu, geturðu stýrt hinum raunverulegu talningaraðgerðum með því að fara fram á að aðeins sérstakar vörur og vöruafbrigði verði talin í staðinn fyrir allar lagerbirgðir á staðsetningunni."
author: YuyuScheller
manager: AnnBe
ms.date: 06/23/2017
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: da8b6c4ec7643ffd84713b4098b4ff35ab95a6b4
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="define-partial-location-cycle-counting-process"></a><span data-ttu-id="86a6c-103">Skilgreina hlutastaðsetning reglulegrar talningar </span><span class="sxs-lookup"><span data-stu-id="86a6c-103">Define partial location cycle counting process</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="86a6c-104">Þegar þú notar áætlun um reglulega talningu til að stofna talningarvinnu, geturðu stýrt hinum raunverulegu talningaraðgerðum með því að fara fram á að aðeins sérstakar vörur og vöruafbrigði verði talin í staðinn fyrir allar lagerbirgðir á staðsetningunni.</span><span class="sxs-lookup"><span data-stu-id="86a6c-104">When you use cycle count plans to create counting work, you can guide the actual counting operations by requesting that only specific products and product variants be counted instead of all on-hand inventory at the location.</span></span> <span data-ttu-id="86a6c-105">Með því að afmarka sérstakar vörur, getur stjórnandi vöruhússins minnkað fastan kostnað við endurmat, minnkað líkur á samstæðumistökum og sparað tíma.</span><span class="sxs-lookup"><span data-stu-id="86a6c-105">By filtering on specific products, the warehouse manager can reduce review overhead, help prevent consolidation mistakes, and save time.</span></span> <span data-ttu-id="86a6c-106">Stjórnandi vöruhúss framkvæmir yfirleitt verkin sem tengjast uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="86a6c-106">Typically, a warehouse manager performs the setup tasks.</span></span> <span data-ttu-id="86a6c-107">Hægt er að fara í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða þín eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="86a6c-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="create-a-cycle-counting-work-template"></a><span data-ttu-id="86a6c-108">Stofna Vinnusniðmát reglulegrar talningar</span><span class="sxs-lookup"><span data-stu-id="86a6c-108">Create a cycle counting work template</span></span>
1. <span data-ttu-id="86a6c-109">Fara í vöruhúsakerfi  > Uppsetning  > Vinna  > Vinnusniðmát.</span><span class="sxs-lookup"><span data-stu-id="86a6c-109">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="86a6c-110">Í svæðinu gerð vinnupöntunar, skal velja „Regluleg talning“.</span><span class="sxs-lookup"><span data-stu-id="86a6c-110">In the Work order type field, select 'Cycle counting'.</span></span>
3. <span data-ttu-id="86a6c-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="86a6c-111">Click New.</span></span>
4. <span data-ttu-id="86a6c-112">Í reitinn raðnúmer skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="86a6c-112">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="86a6c-113">Röðunarpöntunin er frá lægsta númerinu til hæsta númersins.</span><span class="sxs-lookup"><span data-stu-id="86a6c-113">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="86a6c-114">Gildið verður að vera meira en 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="86a6c-114">The value must be more than 0 (zero).</span></span>  
5. <span data-ttu-id="86a6c-115">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="86a6c-115">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="86a6c-116">Færa inn gildi í reitnum Vinnusniðmát.</span><span class="sxs-lookup"><span data-stu-id="86a6c-116">In the Work template field, type a value.</span></span>
7. <span data-ttu-id="86a6c-117">Færa inn gildi í reitnum lýsingu Vinnusniðmáts.</span><span class="sxs-lookup"><span data-stu-id="86a6c-117">In the Work template description field, type a value.</span></span>
8. <span data-ttu-id="86a6c-118">Færa inn eða velja gildi í reitnum Kenni Vinnuklasa.</span><span class="sxs-lookup"><span data-stu-id="86a6c-118">In the Work pool ID field, enter or select a value.</span></span>
9. <span data-ttu-id="86a6c-119">Í reitinn Vinnuforgangur skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="86a6c-119">In the Work priority field, enter a number.</span></span>
10. <span data-ttu-id="86a6c-120">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="86a6c-120">Click Save.</span></span>
11. <span data-ttu-id="86a6c-121">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="86a6c-121">Click New.</span></span>
12. <span data-ttu-id="86a6c-122">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="86a6c-122">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="86a6c-123">Veljið „Talning“ í svæðinu vinnutegund.</span><span class="sxs-lookup"><span data-stu-id="86a6c-123">In the Work type field, select 'Counting'.</span></span>
14. <span data-ttu-id="86a6c-124">Færa inn eða velja gildi í reitnum Kenni Vinnuklasa.</span><span class="sxs-lookup"><span data-stu-id="86a6c-124">In the Work class ID field, enter or select a value.</span></span>
15. <span data-ttu-id="86a6c-125">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="86a6c-125">Click Save.</span></span>
16. <span data-ttu-id="86a6c-126">Smella á Vinnulínuskil.</span><span class="sxs-lookup"><span data-stu-id="86a6c-126">Click Work line breaks.</span></span>
17. <span data-ttu-id="86a6c-127">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="86a6c-127">Click New.</span></span>
18. <span data-ttu-id="86a6c-128">Í reitinn raðnúmer skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="86a6c-128">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="86a6c-129">Röðunarpöntunin er frá lægsta númerinu til hæsta númersins.</span><span class="sxs-lookup"><span data-stu-id="86a6c-129">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="86a6c-130">Gildið verður að vera meira en 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="86a6c-130">The value must be more than 0 (zero).</span></span>  
19. <span data-ttu-id="86a6c-131">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="86a6c-131">Click Save.</span></span>
20. <span data-ttu-id="86a6c-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="86a6c-132">Close the page.</span></span>
21. <span data-ttu-id="86a6c-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="86a6c-133">Close the page.</span></span>

## <a name="create-a-cycle-counting-plan"></a><span data-ttu-id="86a6c-134">Stofna áætlun um reglulega talningu</span><span class="sxs-lookup"><span data-stu-id="86a6c-134">Create a cycle counting plan</span></span>
1. <span data-ttu-id="86a6c-135">Fara í vöruhúsakerfi > Uppsetning > Reglulega talningu > Áætlanir um reglulega talningu.</span><span class="sxs-lookup"><span data-stu-id="86a6c-135">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="86a6c-136">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="86a6c-136">Click New.</span></span>
3. <span data-ttu-id="86a6c-137">Í reitnum Auðkenni fyrir áætlun um reglulega talningu skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="86a6c-137">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="86a6c-138">Í reitinn Lýsing skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="86a6c-138">In the Description field, type a value.</span></span>
5. <span data-ttu-id="86a6c-139">Í reitnum Hámarksfjöldi reglulegrar talningar skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="86a6c-139">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="86a6c-140">Sláið inn eða veldu gildi í reitnum vinnusniðmát.</span><span class="sxs-lookup"><span data-stu-id="86a6c-140">In the Work template field, enter or select a value.</span></span>
7. <span data-ttu-id="86a6c-141">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="86a6c-141">Click New.</span></span>
8. <span data-ttu-id="86a6c-142">Í reitinn raðnúmer skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="86a6c-142">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="86a6c-143">Röðunarpöntunin er frá lægsta númerinu til hæsta númersins.</span><span class="sxs-lookup"><span data-stu-id="86a6c-143">The sort order is from the smallest number to the largest number.</span></span> <span data-ttu-id="86a6c-144">Gildið verður að vera meira en 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="86a6c-144">The value must be more than 0 (zero).</span></span>  
9. <span data-ttu-id="86a6c-145">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="86a6c-145">In the Description field, type a value.</span></span>
10. <span data-ttu-id="86a6c-146">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="86a6c-146">Click Save.</span></span>
11. <span data-ttu-id="86a6c-147">Smella á Skilgreina fyrirspurn um afurð</span><span class="sxs-lookup"><span data-stu-id="86a6c-147">Click Define product query.</span></span>
12. <span data-ttu-id="86a6c-148">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="86a6c-148">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="86a6c-149">Í reitinn Skilyrði skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="86a6c-149">In the Criteria field, enter or select a value.</span></span>
14. <span data-ttu-id="86a6c-150">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="86a6c-150">Click OK.</span></span>
15. <span data-ttu-id="86a6c-151">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="86a6c-151">Close the page.</span></span>


