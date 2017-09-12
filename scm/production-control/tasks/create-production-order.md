--- 
title: "Stofna framleiðslupöntun"
description: "Þessi verklýsing sýnir hvernig á að stofna framleiðslupöntun."
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: ac2ee418082aa6579424fc9480478587b7c22c6d
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-production-order"></a><span data-ttu-id="09e17-103">Stofna framleiðslupöntun</span><span class="sxs-lookup"><span data-stu-id="09e17-103">Create a production order</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="09e17-104">Þessi verklýsing sýnir hvernig á að stofna framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="09e17-104">This procedure shows how to create a production order.</span></span> <span data-ttu-id="09e17-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="09e17-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="09e17-106">Þetta er fyrsta ferlinu af sjö sem útskýrir lífsferli framleiðslupöntunar.</span><span class="sxs-lookup"><span data-stu-id="09e17-106">This is the first procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="09e17-107">Stofna framleiðslupöntun</span><span class="sxs-lookup"><span data-stu-id="09e17-107">Create a production order</span></span>
1. <span data-ttu-id="09e17-108">Fara í Framleiðslustýringar > Framleiðslupantanir > Allar framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="09e17-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="09e17-109">Smella á Ný framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="09e17-109">Click New production order.</span></span>
3. <span data-ttu-id="09e17-110">Sláið inn „D0001“ á svæðinu „Vörunúmer“.</span><span class="sxs-lookup"><span data-stu-id="09e17-110">In the Item number field, type 'D0001'.</span></span>
4. <span data-ttu-id="09e17-111">Í reitinn Afhending skal færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="09e17-111">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="09e17-112">Dagsetning afhendingar gefur til kynna þegar framleiðslupöntunin ætti að ljúka til að afhenda á réttum tíma.</span><span class="sxs-lookup"><span data-stu-id="09e17-112">The delivery date indicates when the production order should end in order to deliver on time.</span></span> <span data-ttu-id="09e17-113">Þessi dagsetning er hægt að nota í áætlunarferli.</span><span class="sxs-lookup"><span data-stu-id="09e17-113">This date can be used in the scheduling process.</span></span> <span data-ttu-id="09e17-114">Til dæmis er hægt að raða pöntunina afturábak frá afhendingardagsetningu.</span><span class="sxs-lookup"><span data-stu-id="09e17-114">For example, you can schedule the order backward from the delivery date.</span></span>  
5. <span data-ttu-id="09e17-115">Stillið magn á „20“.</span><span class="sxs-lookup"><span data-stu-id="09e17-115">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="09e17-116">Athugasemd: Svæðið Uppskrift birtir sjálfkrafa númer allra virkra uppskrifta fyrir gildandi vöru, en hægt er að breyta Uppskrift fyrir framleiðslupöntunina með því að velja virka Uppskrift af lista yfir samþykktar uppskriftaútgáfur.</span><span class="sxs-lookup"><span data-stu-id="09e17-116">Note: The BOM number field automatically displays the number of any active BOM for the current item, but you can change the BOM for the production order by selecting an active BOM from the list of approved BOM versions.</span></span>    <span data-ttu-id="09e17-117">Svæði fyrir númer leiðar birtir sjálfkrafa númer allra virkra leiða fyrir gildandi vöru, en hægt er að breyta leið fyrir framleiðslupöntunina með því að velja virka leið af lista yfir samþykktar leiðarútgáfur.</span><span class="sxs-lookup"><span data-stu-id="09e17-117">The Route number field automatically displays the number of any active Route for the current item, but you can change the Route for the production order by selecting an active Route from the list of approved Route versions.</span></span>  
6. <span data-ttu-id="09e17-118">Smellið á „Stofna“.</span><span class="sxs-lookup"><span data-stu-id="09e17-118">Click Create.</span></span>

## <a name="validate-the-production-order"></a><span data-ttu-id="09e17-119">Villuleita framleiðslupöntunina</span><span class="sxs-lookup"><span data-stu-id="09e17-119">Validate the production order</span></span>
1. <span data-ttu-id="09e17-120">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="09e17-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="09e17-121">Smelltu á tengil fyrir númer framleiðslupöntunar sem var nýlega stofnuð.</span><span class="sxs-lookup"><span data-stu-id="09e17-121">Click the link for the production order number that you have just created.</span></span> <span data-ttu-id="09e17-122">Þetta opnar upplýsingasíðunni fyrir pöntunina.</span><span class="sxs-lookup"><span data-stu-id="09e17-122">This will open the details page for the order.</span></span>  
2. <span data-ttu-id="09e17-123">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="09e17-123">Click Edit.</span></span>
3. <span data-ttu-id="09e17-124">Í reitinn Afhending skal færa inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="09e17-124">In the Delivery field, enter a date.</span></span>
    * <span data-ttu-id="09e17-125">Til dæmis er hægt að breyta afhendingardagsetningu fyrir framleiðslupöntunina.</span><span class="sxs-lookup"><span data-stu-id="09e17-125">For example, you can change the delivery date for the production order.</span></span>  
4. <span data-ttu-id="09e17-126">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="09e17-126">Click Save.</span></span>
5. <span data-ttu-id="09e17-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09e17-127">Close the page.</span></span>

## <a name="update-the-bom"></a><span data-ttu-id="09e17-128">Uppfæra Uppskrift</span><span class="sxs-lookup"><span data-stu-id="09e17-128">Update the BOM</span></span>
1. <span data-ttu-id="09e17-129">Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="09e17-129">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="09e17-130">Smellt er á uppskrift.</span><span class="sxs-lookup"><span data-stu-id="09e17-130">Click BOM.</span></span>
    * <span data-ttu-id="09e17-131">Opna síðuna Uppskriftar til að villuleita gögn Uppskriftar sem var afritað úr sjálfgefnum gögnum þegar framleiðslupöntunin var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="09e17-131">Open the BOM page to validate the BOM data that was copied from the default data when the production order was created.</span></span> <span data-ttu-id="09e17-132">Í þessari aðferð þarf að uppfæra magn fyrir Uppskrift.</span><span class="sxs-lookup"><span data-stu-id="09e17-132">In this procedure, you need to update the quantity for a BOM.</span></span>  
3. <span data-ttu-id="09e17-133">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="09e17-133">Click Edit.</span></span>
4. <span data-ttu-id="09e17-134">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="09e17-134">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="09e17-135">Breytingu á magni í uppskriftarlínu hefur áhrif á kostnaðarmat á efnisnotkun fyrir framleiðslupöntunina.</span><span class="sxs-lookup"><span data-stu-id="09e17-135">Changing the quantity on the BOM line affects the cost estimate of material consumption for the production order.</span></span>  
5. <span data-ttu-id="09e17-136">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="09e17-136">Click Save.</span></span>
6. <span data-ttu-id="09e17-137">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09e17-137">Close the page.</span></span>

## <a name="update-the-production-route"></a><span data-ttu-id="09e17-138">Uppfæra „Framleiðsluleið“.</span><span class="sxs-lookup"><span data-stu-id="09e17-138">Update the production route</span></span>
1. <span data-ttu-id="09e17-139">Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="09e17-139">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="09e17-140">Smellt er á Leiðinni.</span><span class="sxs-lookup"><span data-stu-id="09e17-140">Click Route.</span></span>
    * <span data-ttu-id="09e17-141">Opna síðuna Leið til að villuleita gögn í framleiðsluleiðinni sem var afritað úr sjálfgefnum upplýsingum þegar pöntunin var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="09e17-141">Open the Route page to validate the data of the production route that was copied from the default data when the order was created.</span></span> <span data-ttu-id="09e17-142">Í þessari aðferð þarf að uppfæra magn fyrir eina af aðgerðunum í framleiðsluleiðinni.</span><span class="sxs-lookup"><span data-stu-id="09e17-142">In this procedure, you need to update the quantity for one of the operations in the production route.</span></span>  
3. <span data-ttu-id="09e17-143">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="09e17-143">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="09e17-144">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="09e17-144">Click Edit.</span></span>
5. <span data-ttu-id="09e17-145">Í svæðinu framleiðslumagn</span><span class="sxs-lookup"><span data-stu-id="09e17-145">In the Process qty.</span></span> <span data-ttu-id="09e17-146">færðu inn númer</span><span class="sxs-lookup"><span data-stu-id="09e17-146">field, enter a number.</span></span>
    * <span data-ttu-id="09e17-147">Ef Vinnslutími er breytt hefur það áhrif á áætlaður leiðarnotkun og kostnað framleiðslupöntunar.</span><span class="sxs-lookup"><span data-stu-id="09e17-147">Changing the process time affects the estimated route consumption and the cost of the production order.</span></span>  
6. <span data-ttu-id="09e17-148">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="09e17-148">Click Save.</span></span>
7. <span data-ttu-id="09e17-149">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09e17-149">Close the page.</span></span>


