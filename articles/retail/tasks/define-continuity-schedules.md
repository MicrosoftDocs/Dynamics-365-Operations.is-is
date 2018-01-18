--- 
title: " Skilgreina samfelldniáætlanir"
description: "Þetta efnisatriði fer í gegnum uppsetningu samfelldniáætlanir (einnig þekkt sem endurteknar pantanir)."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: b79c7fb11f73314dc3f4c0bb788435b829d5b410
ms.contentlocale: is-is
ms.lasthandoff: 01/17/2018

---
# <a name="define-continuity-schedules"></a><span data-ttu-id="0c6b0-103"> Skilgreina samfelldniáætlanir</span><span class="sxs-lookup"><span data-stu-id="0c6b0-103">Define continuity schedules</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="0c6b0-104">Þetta efnisatriði fer í gegnum uppsetningu samfelldniáætlanir (einnig þekkt sem endurteknar pantanir).</span><span class="sxs-lookup"><span data-stu-id="0c6b0-104">This topic walks through setting up a continuity program (otherwise known as reoccurring orders).</span></span> <span data-ttu-id="0c6b0-105">Þessi aðferð notar sýnifyrirtækið USRT.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-105">This topic uses company USRT in the demo data.</span></span>


## <a name="create-continuity-program"></a><span data-ttu-id="0c6b0-106">Stofna samfelldniáætlun</span><span class="sxs-lookup"><span data-stu-id="0c6b0-106">Create continuity program</span></span>
1. <span data-ttu-id="0c6b0-107">Fara í Smásölu og viðskipti > Samfelldni > Samfelldniáætlanir.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-107">Go to Retail and commerce > Continuity > Continuity programs.</span></span>
2. <span data-ttu-id="0c6b0-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-108">Click New.</span></span>
3. <span data-ttu-id="0c6b0-109">Í reitinn kenni áætlunar, skal færa inn kenni samfelldniáætlunar.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-109">In the Schedule ID field, type the continuity schedule ID.</span></span>
4. <span data-ttu-id="0c6b0-110">Í reitnum upphaf pöntunar, veljið 'Fyrsta tilvik'.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-110">In the Order start field, select 'First event'.</span></span>
    * <span data-ttu-id="0c6b0-111">Ef viðskiptavinur útbýr nýja pöntun fyrir samfelldniáætlanirnar, eru tveir valmöguleikar sem afurðin verður send fyrir:  1.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-111">If a customer places a new order for the continuity program, there are two options for which product will be shipped:  1.</span></span> <span data-ttu-id="0c6b0-112">Fyrsta tilvik: fyrsta afurð í samfelldniáætlun verður send.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-112">First event: the first product in the continuity program will be shipped.</span></span>  <span data-ttu-id="0c6b0-113">2.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-113">2.</span></span> <span data-ttu-id="0c6b0-114">Núverandi tilvik: núverandi vöru verður send.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-114">Current event: the current product will be shipped.</span></span> <span data-ttu-id="0c6b0-115">Til dæmis:</span><span class="sxs-lookup"><span data-stu-id="0c6b0-115">For example.</span></span> <span data-ttu-id="0c6b0-116">þegar þrír mánuðir eru liðnir á áætlunina, fær viðskiptavinurinn þriðjung áætlunar.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-116">three months into the program, the customer will receive the third in the program.</span></span>  
5. <span data-ttu-id="0c6b0-117">Velja 'Já' til að spyrja um upphafsdagsetning pöntunar.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-117">Select 'Yes' to prompt for the order start date.</span></span>
6. <span data-ttu-id="0c6b0-118">Smellið á „Bæta við línu“.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-118">Click Add line.</span></span>
7. <span data-ttu-id="0c6b0-119">Í svæðið númer sláið inn vörunúmerið fyrir fyrstu afurðarinnar ('0013').</span><span class="sxs-lookup"><span data-stu-id="0c6b0-119">In the Item number field, type the item number for the first product ('0013').</span></span>
8. <span data-ttu-id="0c6b0-120">Sláðu inn 'CP'.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-120">Type 'CP'.</span></span>
9. <span data-ttu-id="0c6b0-121">Sláið inn dagsetningu þegar fyrstu afurð verða tiltækar til pöntunar.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-121">Enter the date when the first product will be available for order.</span></span>
10. <span data-ttu-id="0c6b0-122">Smella á bæta Við línu.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-122">Click Add line.</span></span>
11. <span data-ttu-id="0c6b0-123">Í svæðið númers, færðu inn  '0014'.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-123">In the Item number field, type '0014'.</span></span>
12. <span data-ttu-id="0c6b0-124">Í reitnum kóði dagsetningabils, hreinsa gildi þannig að svæðið er autt.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-124">In the Date interval code field, clear the value so the field is empty.</span></span>
    * <span data-ttu-id="0c6b0-125">Hreinsa dagsetningarbil fyrir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-125">For this procedure, clear the date interval.</span></span> <span data-ttu-id="0c6b0-126">Stilla verður dagsetningin sem stigvaxandi frá upphafsdagsetningu fyrstu vörunnar.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-126">You'll set the date as incremental from the start date of the first item.</span></span>  
13. <span data-ttu-id="0c6b0-127">Hér er fært inn millibilið sem vörur eru sendar á.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-127">Here you'll enter the interval at which the products are shipped.</span></span> <span data-ttu-id="0c6b0-128">Sláðu inn '30'.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-128">Type '30'.</span></span>
    * <span data-ttu-id="0c6b0-129">Fyrir mánaðarlega áætlun, verður að færa inn 30 dagar fyrir bilið.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-129">For a monthly program, you'll enter 30 days for the interval.</span></span>  
14. <span data-ttu-id="0c6b0-130">Smellið á „Bæta við línu“.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-130">Click Add line.</span></span>
15. <span data-ttu-id="0c6b0-131">Í svæðið númers, færðu inn  '0015'.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-131">In the Item number field, type '0015'.</span></span>
16. <span data-ttu-id="0c6b0-132">Sláðu inn "Síðast".</span><span class="sxs-lookup"><span data-stu-id="0c6b0-132">Type 'End'.</span></span>
17. <span data-ttu-id="0c6b0-133">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-133">Click Save.</span></span>

## <a name="assign-to-continuity-item"></a><span data-ttu-id="0c6b0-134">Úthlutið samfelldnivöru</span><span class="sxs-lookup"><span data-stu-id="0c6b0-134">Assign to continuity item</span></span>
1. <span data-ttu-id="0c6b0-135">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-135">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="0c6b0-136">Veldu afurð '0016'.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-136">Select item '0016'.</span></span>
    * <span data-ttu-id="0c6b0-137">Fyrir þetta ferli, veljið vörunúmerið 0016.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-137">For this procedure, you'll select item number 0016.</span></span> <span data-ttu-id="0c6b0-138">Yfirleitt hefurðu stofnað útgefna afurð sem notar aukalega samfelldni viðskiptagrunns þegar hún er sett í sölupöntun í símaveri.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-138">Normally, you'll have created a released product that has additional continuity business logic applied when it's placed on a sales order in call center.</span></span>  
3. <span data-ttu-id="0c6b0-139">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-139">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0c6b0-140">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-140">Click Edit.</span></span>
5. <span data-ttu-id="0c6b0-141">Stækka eða fella saman  hlutann Selja</span><span class="sxs-lookup"><span data-stu-id="0c6b0-141">Expand or collapse the Sell section.</span></span>
6. <span data-ttu-id="0c6b0-142">Hér færirðu inn samfelldniáætlanirnar sem þessi afurð stendur fyrir.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-142">Here you'll enter the continuity program that this item represents.</span></span> <span data-ttu-id="0c6b0-143">Færa inn Kenni áætlunar sem búið var til áður.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-143">Type the Schedule ID you created earlier.</span></span>
    * <span data-ttu-id="0c6b0-144">Þegar varan er seld í þjónustumiðstöð, er notuð viðbótar viðskiptagrunnur af hendi hins valda samfelldniáætlanirnar.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-144">When this item is sold in a call center, additional business logic is applied from the selected continuity program.</span></span>  
7. <span data-ttu-id="0c6b0-145">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="0c6b0-145">Click Save.</span></span>


