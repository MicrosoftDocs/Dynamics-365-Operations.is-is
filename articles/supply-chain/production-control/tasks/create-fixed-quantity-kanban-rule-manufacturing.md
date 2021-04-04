---
title: Stofna kanban í föstu magni fyrir framleiðslu
description: Þetta ferli leggur áherslu á uppsetningu sem þarf til að stofna fasta kanban-reglu framleiðslu til að kveikja umbreytingarverkþætti, á vinnuflokk, í lean-umhverfi.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 540df772f132f60c9d8e7e937e72d3f51f6759ab
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255254"
---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a><span data-ttu-id="0e7f8-103">Stofna kanban í föstu magni fyrir framleiðslu</span><span class="sxs-lookup"><span data-stu-id="0e7f8-103">Create a fixed quantity kanban rule for manufacturing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0e7f8-104">Þetta ferli leggur áherslu á uppsetningu sem þarf til að stofna fasta kanban-reglu framleiðslu til að kveikja umbreytingarverkþætti, á vinnuflokk, í lean-umhverfi.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-104">This procedure focuses on the setup needed to create a fixed manufacturing kanban rule for triggering transforming activities, at a work cell, in a lean environment.</span></span> <span data-ttu-id="0e7f8-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0e7f8-106">Þetta ferli er ætlað fyrir Ferlishönnuð eða Virðisstraumsstjóra, þar sem þau undirbúa framleiðslu nýja eða breytta afurðar.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="0e7f8-107">Stofna nýja kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="0e7f8-107">Create new kanban rule</span></span>
1. <span data-ttu-id="0e7f8-108">Fara á kanban-reglur.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="0e7f8-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-109">Click New.</span></span>
    * <span data-ttu-id="0e7f8-110">Athugaðu að sjálfgefin gerð er Framleiðsla og Áfyllingaráætlun er Fast.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-110">Notice that the default Type is Manufacturing and Replenishment strategy is Fixed.</span></span> <span data-ttu-id="0e7f8-111">Ekki þarf að breyta þessum færibreytum.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-111">You do not have to change these parameters.</span></span>  
3. <span data-ttu-id="0e7f8-112">Færa inn eða velja gildi í reitnum Fyrsta áætlun verkþáttarins.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="0e7f8-113">Þetta er verkþátturinn sem verður að framkvæma fyrir kanbön stofnuð byggt á þessari kanban-reglu.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-113">This is the activity that will be performed for kanbans created based on this kanban rule.</span></span>  <span data-ttu-id="0e7f8-114">Veljið 'SpeakerTestAndPackaging'.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-114">Select 'SpeakerTestAndPackaging'.</span></span>  
4. <span data-ttu-id="0e7f8-115">Útvíkka hlutann Upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-115">Expand the Details section.</span></span>
5. <span data-ttu-id="0e7f8-116">Sláðu inn eða veldu gildi í reitnum Afurð.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="0e7f8-117">Veldu L0050.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-117">Select L0050.</span></span>  
6. <span data-ttu-id="0e7f8-118">Færðu inn eða veldu gildi í reitnum Mælieining.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-118">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="0e7f8-119">Veljið mínútur.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-119">Select minutes.</span></span>  
7. <span data-ttu-id="0e7f8-120">Í reitinn Afhendingartími skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-120">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="0e7f8-121">Færðu inn 5.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-121">Enter 5.</span></span>  

## <a name="set-quantities"></a><span data-ttu-id="0e7f8-122">Stilla magn</span><span class="sxs-lookup"><span data-stu-id="0e7f8-122">Set quantities</span></span>
1. <span data-ttu-id="0e7f8-123">Útvíkka hlutann Magn.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-123">Expand the Quantities section.</span></span>
2. <span data-ttu-id="0e7f8-124">Stilla Sjálfgefið magn á '10'.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-124">Set Default quantity to '10'.</span></span>
    * <span data-ttu-id="0e7f8-125">Þetta er magnið sem verður flutt fyrir hverja kanban.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-125">This is the quantity that will be transferred for each kanban.</span></span>  
3. <span data-ttu-id="0e7f8-126">Veldu gátreitinn Frávik afurðarmagns.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-126">Select the Product quantity variance check box.</span></span>
    * <span data-ttu-id="0e7f8-127">Með þessu er hægt að ljúka völdum kanbönum með frávik úr sjálfgefnu magni.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-127">With this, selected kanbans can be completed with a variance from the default quantity.</span></span>  <span data-ttu-id="0e7f8-128">Til að leyfa að kanbönum sé lokið með magn frá 8 til 12 þarf að stilla bæði frávik á 2.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-128">To allow kanbans to be completed with a quantity from 8 to 12, set both variances to 2.</span></span>  
4. <span data-ttu-id="0e7f8-129">Stilla frávik fyrir neðan á ‚2‘.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-129">Set Variance below to '2'.</span></span>
    * <span data-ttu-id="0e7f8-130">Þetta leyfir að lokið sé niður að 10 - 2 = 8</span><span class="sxs-lookup"><span data-stu-id="0e7f8-130">This will allow completing down to 10 - 2 = 8</span></span>  
5. <span data-ttu-id="0e7f8-131">Stilla frávik að ofan á ‚2‘.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-131">Set Variance above to '2'.</span></span>
    * <span data-ttu-id="0e7f8-132">Þetta leyfir að lokið sé allt að 10 + 2 = 12</span><span class="sxs-lookup"><span data-stu-id="0e7f8-132">This will allow completing up to 10 + 2 = 12</span></span>  
6. <span data-ttu-id="0e7f8-133">Færið inn tölu í reitnum Kanban í Föstu magni.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-133">In the Fixed kanban quantity field, enter a number.</span></span>
    * <span data-ttu-id="0e7f8-134">Þetta er upphæð kanbana sem á að vera virk.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-134">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="0e7f8-135">Í þessu tilfelli vinna 5 kanban 10 hvert um sig.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-135">In this case, 5 kanbans processing 10 each.</span></span>  
7. <span data-ttu-id="0e7f8-136">Í reitnum Lágmark viðvörunarmarka skal færa inn ‚2‘.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-136">In the Alert boundary minimum field, enter '2'.</span></span>
    * <span data-ttu-id="0e7f8-137">Notað til að fylgjast með lágmarksupphæð fullra kanbana sem eiga að vera á ákvörðunarstað.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-137">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="0e7f8-138">Þetta er til dæmis notað á yfirlit yfir magn kanbans.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-138">For example, this is used on the kanban quantity overview.</span></span>  
8. <span data-ttu-id="0e7f8-139">Í reitnum Hámark viðvörunarmarka skal færa inn ‚4‘.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-139">In the Alert boundary maximum field, enter '4'.</span></span>
    * <span data-ttu-id="0e7f8-140">Notað til að fylgjast með hámarksupphæð fullra kanbana sem eiga að vera á ákvörðunarstað.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-140">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="0e7f8-141">Þetta er til dæmis notað á yfirlit yfir magn kanbans.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-141">For example, this is used on the kanban quantity overview.</span></span>  
9. <span data-ttu-id="0e7f8-142">Í reitnum Sjálfvirkt áætlunarmagn skal færa inn ‚1‘.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-142">In the Automatic planning quantity field, enter '1'.</span></span>
    * <span data-ttu-id="0e7f8-143">Ef þetta er stillt á 1 þýðir það að hvert kanban verður sjálfkrafa áætlað.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-143">Setting this to 1 means that every kanban will be automatically planned.</span></span>   <span data-ttu-id="0e7f8-144">Ef 3 var fært inn verða kanban ekki áætluð fyrr en 3 tóm kanban eru tilbúin til áætlunar.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-144">If we entered 3, the kanbans would not be planned until 3 empty kanbans are ready for planning.</span></span> <span data-ttu-id="0e7f8-145">Þetta er gagnlegt fyrir flokkunarvinnu og til að forðast of mikla uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-145">This is useful for grouping work and avoiding too much setup.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="0e7f8-146">Stofna kanban</span><span class="sxs-lookup"><span data-stu-id="0e7f8-146">Create Kanbans</span></span>
1. <span data-ttu-id="0e7f8-147">Útvíkkar kanban-hlutann.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-147">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="0e7f8-148">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-148">Click Save.</span></span>
    * <span data-ttu-id="0e7f8-149">Vista þarf kanban-regluna vista áður en hægt er að stofna kanban.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-149">The kanban rule needs to be saved before kanbans can be created.</span></span>  
3. <span data-ttu-id="0e7f8-150">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-150">Click Add.</span></span>
    * <span data-ttu-id="0e7f8-151">Athugaðu að það eru engin virk kanban, þess vegna er ráðlagður „Fjöldi nýrra kanbana“ 5.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-151">Note that there are no active kanbans, due to this the suggested 'Number of new kanbans' are 5.</span></span> <span data-ttu-id="0e7f8-152">Þetta er jafnt og „Fast kanban-magn“.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-152">This is equal to the 'Fixed kanban quantity'.</span></span>  
4. <span data-ttu-id="0e7f8-153">Smellið á „Stofna“.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-153">Click Create.</span></span>
    * <span data-ttu-id="0e7f8-154">Þetta stofnar 5 kanbana.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-154">This will create 5 kanbans.</span></span>  
    * <span data-ttu-id="0e7f8-155">Athugið að 5 kanbön, fyrir hver 10, voru stofnuð fyrir þessa kanban-reglu framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-155">Note that 5 kanbans, for 10 each, was created for this manufacturing kanban rule.</span></span> <span data-ttu-id="0e7f8-156">Þetta er síðasta skrefið í þessu ferli.</span><span class="sxs-lookup"><span data-stu-id="0e7f8-156">This is the last step in this procedure.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]