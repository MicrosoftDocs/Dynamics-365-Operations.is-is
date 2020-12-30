---
title: Setja upp eldsneytisvísi flutningsaðila
description: Þessari handbók sýnir hvernig stofna á eldsneytisvísasvæði, eldsneytisvísi og eldsneytisvísi flutningsaðila.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFuelIndexRegion,TMSCarrierFuelIndexTable,TMSFuelIndex
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 12ade30b63454dfd997aa47a62cde21b066140fa
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/29/2020
ms.locfileid: "4430799"
---
# <a name="set-up-a-carrier-fuel-index"></a><span data-ttu-id="5ee41-103">Setja upp eldsneytisvísi flutningsaðila</span><span class="sxs-lookup"><span data-stu-id="5ee41-103">Set up a carrier fuel index</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5ee41-104">Þessari handbók sýnir hvernig stofna á eldsneytisvísasvæði, eldsneytisvísi og eldsneytisvísi flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="5ee41-104">This guide shows how to create a fuel index region, a fuel index and a carrier fuel index.</span></span> <span data-ttu-id="5ee41-105">Eldsneytisvísasvæði tilgreinir á hvaða svæðum eldsneytisvísi gilda, og eldsneytisvísir tilgreinir eldsneytisverð á tilteknu tímabili.</span><span class="sxs-lookup"><span data-stu-id="5ee41-105">The fuel index region specifies which region the fuel index should apply to, and the fuel index specifies a fuel price for a particular period of time.</span></span> <span data-ttu-id="5ee41-106">Til að endurspegla breytingarnar í verði eldsneytis yfir tíma, er hægt að tengja marga eldsneytisvísa við flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="5ee41-106">To reflect the change in fuel prices over time, you can associate multiple fuel indexes with a carrier.</span></span>  <span data-ttu-id="5ee41-107">Þessi verk eru yfirleitt gert með af samræmingaraðila flutninga.</span><span class="sxs-lookup"><span data-stu-id="5ee41-107">These tasks are normally done by a transportation coordinator.</span></span> <span data-ttu-id="5ee41-108">Hægt er að nota þessa aðgerð í fyrirtæki gögn sýnigögn USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="5ee41-108">You can use this procedure in demo data company USMF or using your own data.</span></span>


## <a name="create-a-fuel-index-region"></a><span data-ttu-id="5ee41-109">Stofna svæði eldsneytisvísis.</span><span class="sxs-lookup"><span data-stu-id="5ee41-109">Create a fuel index region</span></span>
1. <span data-ttu-id="5ee41-110">Fara í flutningsstjórnun > Uppsetning >Eldsneytisvísa > Svæði eldsneytisvísis.</span><span class="sxs-lookup"><span data-stu-id="5ee41-110">Go to Transportation management > Setup > Fuel indexes > Fuel index regions.</span></span>
    * <span data-ttu-id="5ee41-111">Fyrst þarf að stofna mismunandi svæðum, þar sem starfa og reikna út mismunandi eldsneytisálag.</span><span class="sxs-lookup"><span data-stu-id="5ee41-111">First you have to create the different regions, where you operate and calculate different fuel surcharges.</span></span>  
2. <span data-ttu-id="5ee41-112">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5ee41-112">Click New.</span></span>
3. <span data-ttu-id="5ee41-113">Í reitnum Svæði skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5ee41-113">In the Region field, type a value.</span></span>
4. <span data-ttu-id="5ee41-114">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5ee41-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="5ee41-115">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="5ee41-115">Click Save.</span></span>

## <a name="create-a-fuel-index"></a><span data-ttu-id="5ee41-116">Búa til eldsneytisvísi</span><span class="sxs-lookup"><span data-stu-id="5ee41-116">Create a fuel index</span></span>
1. <span data-ttu-id="5ee41-117">Fara í flutningsstjórnun > Uppsetning >Eldsneytisvísa > Eldsneytisvísa.</span><span class="sxs-lookup"><span data-stu-id="5ee41-117">Go to Transportation management > Setup > Fuel indexes > Fuel indexes.</span></span>
    * <span data-ttu-id="5ee41-118">Fyrir svæði sem hefur verið sett upp þarf að færa núgildandi verð fyrir eldsneytisálag á.</span><span class="sxs-lookup"><span data-stu-id="5ee41-118">For the regions you have set up you need to enter the current prices for the fuel.</span></span>  
2. <span data-ttu-id="5ee41-119">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5ee41-119">Click New.</span></span>
3. <span data-ttu-id="5ee41-120">Í reitnum Svæði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="5ee41-120">In the Region field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5ee41-121">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="5ee41-121">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="5ee41-122">Í svæðinu Verð á gallon , færið inn tölu.</span><span class="sxs-lookup"><span data-stu-id="5ee41-122">In the Price per gallon field, enter a number.</span></span>
6. <span data-ttu-id="5ee41-123">Færa inn dagsetningu og tíma í reitnum Raunveruleg upphafsdagsetning og -tími.</span><span class="sxs-lookup"><span data-stu-id="5ee41-123">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="5ee41-124">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="5ee41-124">Click Save.</span></span>

## <a name="create-a-carrier-fuel-index"></a><span data-ttu-id="5ee41-125">Setja upp Eldsneytisvísi fyrir flutningsaðila</span><span class="sxs-lookup"><span data-stu-id="5ee41-125">Create a Carrier fuel index</span></span>
1. <span data-ttu-id="5ee41-126">Fara í flutningsstjórnun > Uppsetning >Eldsneytisvísa > Eldsneytisvísir flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="5ee41-126">Go to Transportation management > Setup > Fuel indexes > Carrier fuel indexes.</span></span>
2. <span data-ttu-id="5ee41-127">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="5ee41-127">Click New.</span></span>
3. <span data-ttu-id="5ee41-128">Færa inn gildi í reitnum eldsneytisvísir Flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="5ee41-128">In the Carrier fuel index field, type a value.</span></span>
4. <span data-ttu-id="5ee41-129">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="5ee41-129">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5ee41-130">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="5ee41-130">Click New.</span></span>
6. <span data-ttu-id="5ee41-131">Færa inn dagsetningu og tíma í reitnum Raunveruleg upphafsdagsetning og -tími.</span><span class="sxs-lookup"><span data-stu-id="5ee41-131">In the Effective start date and time field, enter a date and time.</span></span>
7. <span data-ttu-id="5ee41-132">Í reitinn PPG Úr skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="5ee41-132">In the PPG From field, enter a number.</span></span>
    * <span data-ttu-id="5ee41-133">Í þessu dæmi er hægt að stilla PPG Frá svæðið sem 1.95.</span><span class="sxs-lookup"><span data-stu-id="5ee41-133">In this example, you can set PPG From field to 1.95.</span></span>  
8. <span data-ttu-id="5ee41-134">Í reitinn PPG í skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="5ee41-134">In the PPG To field, enter a number.</span></span>
    * <span data-ttu-id="5ee41-135">Í þessu dæmi er hægt að stilla svæðið PPG Til á 2.</span><span class="sxs-lookup"><span data-stu-id="5ee41-135">In this example you can set the PPG To field to 2.</span></span>  
9. <span data-ttu-id="5ee41-136">Færið inn tölu í svæðinu prósenta.</span><span class="sxs-lookup"><span data-stu-id="5ee41-136">In the Percentage field, enter a number.</span></span>
    * <span data-ttu-id="5ee41-137">Hægt er að setja prósentu til 3 í þessu dæmi.</span><span class="sxs-lookup"><span data-stu-id="5ee41-137">In this example you can set the percentage to 3.</span></span>  
10. <span data-ttu-id="5ee41-138">Í reitnum gjaldmiðill skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="5ee41-138">In the Currency field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="5ee41-139">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="5ee41-139">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="5ee41-140">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="5ee41-140">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="5ee41-141">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="5ee41-141">Click Save.</span></span>

