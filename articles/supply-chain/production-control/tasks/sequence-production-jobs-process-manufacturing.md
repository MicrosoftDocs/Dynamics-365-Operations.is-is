---
title: Raða framleiðsluvinnslum fyrir framleiðsluferli
description: Þessi ferli notar málningu afurðir sem dæmi til að sýna hvernig raða á áætlaðar pantanir eftir forgang lit og stærð pakka.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage, PMFSeqReqRoute, PMFSeqReqRouteChanges, PMFSeqReqSchedDetailsFactBox, PMFSequenceGroup, PMFSequenceItemTable, PMFSequenceTable, PmfSeqWrkCtrCapRes
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e22c767a3de8fd937d9032a5bf285dfb4ced3d55
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981058"
---
# <a name="sequence-production-jobs-for-process-manufacturing"></a><span data-ttu-id="9e3b9-103">Raða framleiðsluvinnslum fyrir framleiðsluferli</span><span class="sxs-lookup"><span data-stu-id="9e3b9-103">Sequence production jobs for process manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9e3b9-104">Þessi ferli notar málningu afurðir sem dæmi til að sýna hvernig raða á áætlaðar pantanir eftir forgang lit og stærð pakka.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-104">This procedure uses paint products as an example to show how to sequence planned orders according to the priority of color and package size.</span></span> <span data-ttu-id="9e3b9-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USPI.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-105">The demo data company used to create this procedure is USPI.</span></span> <span data-ttu-id="9e3b9-106">Þetta ferli er ætluð fyrir framleiðslustjóri</span><span class="sxs-lookup"><span data-stu-id="9e3b9-106">This procedure is intended for the production planner.</span></span>


## <a name="run-master-planning-for-uspi"></a><span data-ttu-id="9e3b9-107">Keyra áætlanagerð fyrir USPI</span><span class="sxs-lookup"><span data-stu-id="9e3b9-107">Run master planning for USPI</span></span>
1. <span data-ttu-id="9e3b9-108">Fara í Áætlanagerð > Áætlunargerðar > Keyra > áætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-108">Go to Master planning > Master planning > Run > Master planning.</span></span>
2. <span data-ttu-id="9e3b9-109">Í aðaláætlunarreitnum skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-109">In the Master plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="9e3b9-110">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9e3b9-111">Veljið MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-111">Select MasterPlan.</span></span>  
4. <span data-ttu-id="9e3b9-112">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-112">Click OK.</span></span>
    * <span data-ttu-id="9e3b9-113">Þetta hefur Áætlanagerð, þar á meðal ferli röð.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-113">This starts Master Planning, including the sequence process.</span></span> <span data-ttu-id="9e3b9-114">Þetta ferli getur tekið nokkrar mínútur.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-114">This process can take a few minutes.</span></span>  

## <a name="view-planned-orders-for-the-paint-products"></a><span data-ttu-id="9e3b9-115">Skoða áætlaðar pantanir fyrir málningu afurðir</span><span class="sxs-lookup"><span data-stu-id="9e3b9-115">View planned orders for the paint products</span></span>
1. <span data-ttu-id="9e3b9-116">Fara í Áætlanagerð > Áætlunargerðar > Áætluð pöntun.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-116">Go to Master planning > Master planning > Planned orders.</span></span>
2. <span data-ttu-id="9e3b9-117">Útvíkka upplýsingareit vöruupplýsinga</span><span class="sxs-lookup"><span data-stu-id="9e3b9-117">Expand the Item details FactBox.</span></span>
3. <span data-ttu-id="9e3b9-118">Útvíkka upplýsingareit upplýsingar um áætlun</span><span class="sxs-lookup"><span data-stu-id="9e3b9-118">Expand the Schedule details FactBox.</span></span>
4. <span data-ttu-id="9e3b9-119">Í reitnum Áætlun skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-119">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="9e3b9-120">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9e3b9-121">Veljið MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-121">Select MasterPlan.</span></span>  
6. <span data-ttu-id="9e3b9-122">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="9e3b9-123">Notið flýtiafmörkun til að sía á vörunúmerasvæðinu með gildinu „P300“.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-123">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="9e3b9-124">Aflæstu til að skruna til hægri til að sjá pöntunardagsetningu og afhendingardagur.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-124">Unlock to scroll to the right to see the order date and delivery date.</span></span> <span data-ttu-id="9e3b9-125">Athugaðu að þessar vörur eru með pöntunardagsetningu dagsins í dag og afhendingardagar fyrir áætlaðar pantanir eru ekki raðaðar samkvæmt forgangi litar og pakkningastærðar, eins og sýnt er í vöruheiti.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-125">Notice that these items have an order date of Today and the delivery dates for the planned orders are not sequenced after the priority of color and package size, as shown in the product name.</span></span> <span data-ttu-id="9e3b9-126">Hægt er að halda bendlinum yfir vörunúmeri til að sjá afurðarheiti og forgang.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-126">You can hover over an item number to see the product name and priority.</span></span>  

## <a name="sequence-planned-orders-for-paint"></a><span data-ttu-id="9e3b9-127">Raða áætluðum pöntunum fyrir málningu</span><span class="sxs-lookup"><span data-stu-id="9e3b9-127">Sequence planned orders for paint</span></span>
1. <span data-ttu-id="9e3b9-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-128">Close the page.</span></span>
2. <span data-ttu-id="9e3b9-129">Fara í Áætlanagerð > Áætlunargerð > Raðaðar áætlaðar pantanir.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-129">Go to Master planning > Master planning > Sequenced planned orders.</span></span>
3. <span data-ttu-id="9e3b9-130">Útvíkka upplýsingareit vöruupplýsinga</span><span class="sxs-lookup"><span data-stu-id="9e3b9-130">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="9e3b9-131">Útvíkka upplýsingareit upplýsingar um áætlun</span><span class="sxs-lookup"><span data-stu-id="9e3b9-131">Expand the Schedule details FactBox.</span></span>
    * <span data-ttu-id="9e3b9-132">Athugasemd: Hér sést Upphafsdagsetning /-tími fyrir áætlaðar pantanir eru raðaðar eftir lit og pakka stærð innan tímarramma 28 daga.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-132">Note: Here you see that the Start date/time for the planned orders are sequenced according to color and package size within a bucket period of 28 days.</span></span> <span data-ttu-id="9e3b9-133">Þessar tímabil eru skilgreindar með númeri á svæði Herferðar.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-133">These periods are defined by a number in the field Campaign.</span></span> <span data-ttu-id="9e3b9-134">Röðuð áætluð pöntun skjámynd hagar eins og skjámynd dæmigert áætlaða pöntun og framleiðslustjórinn getur staðfesta áætlaðar pantanir hér.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-134">The sequenced planned order form acts like the typical planned order form, and the production planner can firm the planned orders here.</span></span>  
5. <span data-ttu-id="9e3b9-135">Merkja allar línur</span><span class="sxs-lookup"><span data-stu-id="9e3b9-135">Mark all rows.</span></span>
6. <span data-ttu-id="9e3b9-136">Smellið á Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-136">Click Accept.</span></span>
    * <span data-ttu-id="9e3b9-137">Þannig verður unnt að uppfærsla áætluð pöntun með valinni röðunaraðgerð sem er annað hvort Fresta eða Flýta.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-137">This will update the planned orders with the selected sequence action of either Postpone or Advance.</span></span>  

## <a name="verify-the-sequence-of-the-planned-orders"></a><span data-ttu-id="9e3b9-138">Staðfesta röð áætlaðar pantanir</span><span class="sxs-lookup"><span data-stu-id="9e3b9-138">Verify the sequence of the planned orders</span></span>
1. <span data-ttu-id="9e3b9-139">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-139">Close the page.</span></span>
2. <span data-ttu-id="9e3b9-140">Fara í Áætlanagerð > Áætlunargerðar > Áætluð pöntun.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-140">Go to Master planning > Master planning > Planned orders.</span></span>
3. <span data-ttu-id="9e3b9-141">Útvíkka upplýsingareit vöruupplýsinga</span><span class="sxs-lookup"><span data-stu-id="9e3b9-141">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="9e3b9-142">Útvíkka upplýsingareit upplýsingar um áætlun</span><span class="sxs-lookup"><span data-stu-id="9e3b9-142">Expand the Schedule details FactBox.</span></span>
5. <span data-ttu-id="9e3b9-143">Í reitnum Áætlun skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-143">In the Plan field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9e3b9-144">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9e3b9-145">Veljið MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-145">Select MasterPlan.</span></span>  
7. <span data-ttu-id="9e3b9-146">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9e3b9-147">Notið flýtiafmörkun til að sía á vörunúmerasvæðinu með gildinu „P300“.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-147">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="9e3b9-148">Athugið pantanirnar eru nú raðað eftir forgangi lit og stærð og áætlaðar pantanir byrja á fyrstu pöntunardagsetningu og afhendingardagsetningu.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-148">Notice that the orders now are sequenced according to the priority of color and size and the planned orders start at the earliest order date and delivery date.</span></span> <span data-ttu-id="9e3b9-149">Villuleita dálknum pöntunardagsetningu eða upphafsdagsetning upplýsingum um Áætlun upplýsingareit.</span><span class="sxs-lookup"><span data-stu-id="9e3b9-149">Validate the Order date column or the Start date in the Schedule details FactBbox.</span></span>  

