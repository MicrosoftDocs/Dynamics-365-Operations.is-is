---
title: Reikna út tillögur um kanban-magn
description: Þetta ferli leggur áherslu á besta kanban-stærð og magn fyrir tiltekna kanban-reglu með því að nota útreikning kanban-magns.
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 540dd32c5da5859ef5e69f55d6806eada90bc840
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "348987"
---
# <a name="calculate-kanban-quantity-suggestions"></a><span data-ttu-id="3d1be-103">Reikna út tillögur um kanban-magn</span><span class="sxs-lookup"><span data-stu-id="3d1be-103">Calculate kanban quantity suggestions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3d1be-104">Þetta ferli leggur áherslu á besta kanban-stærð og magn fyrir tiltekna kanban-reglu með því að nota útreikning kanban-magns.</span><span class="sxs-lookup"><span data-stu-id="3d1be-104">This procedure focuses on optimizing the kanban size and quantities for a specific kanban rule by using the kanban quantity calculation.</span></span> <span data-ttu-id="3d1be-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="3d1be-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3d1be-106">Þetta ferli er ætlað fyrir virðisstraumsstjóra.</span><span class="sxs-lookup"><span data-stu-id="3d1be-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="3d1be-107">Það er frumskilyrði að þú hafir lokið ferli Bæta nýja útreikningsstefnu kanban-magns á kanban-reglu.</span><span class="sxs-lookup"><span data-stu-id="3d1be-107">It is a prerequisite that you have completed the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span>


## <a name="create-a-kanban-quantity-calculation"></a><span data-ttu-id="3d1be-108">Stofna útreikning fyrir kanban-magn</span><span class="sxs-lookup"><span data-stu-id="3d1be-108">Create a kanban quantity calculation</span></span>
1. <span data-ttu-id="3d1be-109">Fara í Framleiðslustýringar > Reglubundin verkefni > Útreikningur kanban-magns > Útreikningsreglur kanban-magns.</span><span class="sxs-lookup"><span data-stu-id="3d1be-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Calculate kanban quantity.</span></span>
2. <span data-ttu-id="3d1be-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="3d1be-110">Click New.</span></span>
3. <span data-ttu-id="3d1be-111">Í svæðið Heiti, færðu inn 'Speaker2016'.</span><span class="sxs-lookup"><span data-stu-id="3d1be-111">In the Name field, type 'Speaker2016'.</span></span>
4. <span data-ttu-id="3d1be-112">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="3d1be-112">In the Name field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3d1be-113">Veljið regluna sem þú hefur stofnað í ferlinu Bæta til nýja útreikningsstefnu kanban-magns á kanban-reglu.</span><span class="sxs-lookup"><span data-stu-id="3d1be-113">Select the policy that you have created in the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span> <span data-ttu-id="3d1be-114">Til dæmis Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="3d1be-114">For example, Speaker2016.</span></span>  
5. <span data-ttu-id="3d1be-115">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="3d1be-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="3d1be-116">Í svæðið Regla virk frá og með dagsetningu, setja dagsetningu og tíma í '2012-12-17T08:00:00'.</span><span class="sxs-lookup"><span data-stu-id="3d1be-116">In the Rule active as of date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="3d1be-117">Þessi dagsetning virkar sem grundvöllur fyrir því að ákvarða hvaða fasta kanban-reglur eru hafðar með í útreikningur kanban-magns.</span><span class="sxs-lookup"><span data-stu-id="3d1be-117">This date serves as the basis for determining which fixed kanban rules are included in the kanban quantity calculation.</span></span>  
7. <span data-ttu-id="3d1be-118">Í upphafsdagsetningarsvæðið Uppfyllt eftirspurn tímabils, setja dagsetningu og tíma í ' 2012-11-17T09:00:00'.</span><span class="sxs-lookup"><span data-stu-id="3d1be-118">In the Fulfilled demand period start date field, set the date and time to '2012-11-17T09:00:00'.</span></span>
    * <span data-ttu-id="3d1be-119">Frá og með þessari dagsetningu eru liðnar eftirspurnarfærslur hafðar með í útreikningi kanban-magns.</span><span class="sxs-lookup"><span data-stu-id="3d1be-119">The date from when past demand transactions are included to calculate the kanban quantity.</span></span>  
8. <span data-ttu-id="3d1be-120">Í lokadagsetningarsvæðið Uppfyllt eftirspurn tímabils, setja dagsetningu og tíma í ' 2012-12-17T07:59:59'.</span><span class="sxs-lookup"><span data-stu-id="3d1be-120">In the Fulfilled demand period end date field, set the date and time to '2012-12-17T07:59:59'.</span></span>
    * <span data-ttu-id="3d1be-121">Til og með þessari dagsetningu eru liðnar eftirspurnarfærslur hafðar með í útreikningi kanban-magns.</span><span class="sxs-lookup"><span data-stu-id="3d1be-121">The date until when past demand transactions are included to calculate the kanban quantity.</span></span>  
9. <span data-ttu-id="3d1be-122">Í upphafsdagsetningarsvæðið eftirspurnartímabil, setja dagsetningu og tíma í ' 2012-12-17T08:00:00'.</span><span class="sxs-lookup"><span data-stu-id="3d1be-122">In the Demand period start date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="3d1be-123">Frá og með þessari dagsetningu eru núgildandi eftirspurnarfærslur hafðar með í útreikningi kanban-magns.</span><span class="sxs-lookup"><span data-stu-id="3d1be-123">The date from when current demand transactions are included to calculate the kanban quantity.</span></span>  
10. <span data-ttu-id="3d1be-124">Í lokadagsetningarsvæðið eftirspurnartímabil, setja dagsetningu og tíma í ' 2013-01-16T07:59:59'.</span><span class="sxs-lookup"><span data-stu-id="3d1be-124">In the Demand period end date field, set the date and time to '2013-01-16T07:59:59'.</span></span>
    * <span data-ttu-id="3d1be-125">Til og með þessari dagsetningu eru núgildandi eftirspurnarfærslur hafðar með í útreikningi kanban-magns.</span><span class="sxs-lookup"><span data-stu-id="3d1be-125">The date until when current demand transactions are included to calculate the kanban quantity.</span></span>  

## <a name="generate-kanban-quantity-proposal"></a><span data-ttu-id="3d1be-126">Stofna Tillaga um kanban-magn.</span><span class="sxs-lookup"><span data-stu-id="3d1be-126">Generate kanban quantity proposal</span></span>
1. <span data-ttu-id="3d1be-127">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="3d1be-127">Click Save.</span></span>
2. <span data-ttu-id="3d1be-128">Smellt er á Mynda.</span><span class="sxs-lookup"><span data-stu-id="3d1be-128">Click Generate.</span></span>
    * <span data-ttu-id="3d1be-129">Þetta myndar tillögulína kanban-magns fyrir kanban-reglu 000020.</span><span class="sxs-lookup"><span data-stu-id="3d1be-129">This generates a kanban quantity proposal line for the kanban rule 000020.</span></span>  

## <a name="run-kanban-quantity-calculation"></a><span data-ttu-id="3d1be-130">Keyra útreikning fyrir kanban-magn</span><span class="sxs-lookup"><span data-stu-id="3d1be-130">Run kanban quantity calculation</span></span>
1. <span data-ttu-id="3d1be-131">Smellt er á að reikna Út.</span><span class="sxs-lookup"><span data-stu-id="3d1be-131">Click Calculate.</span></span>
    * <span data-ttu-id="3d1be-132">þetta reiknar Tillaga um kanban-magn.</span><span class="sxs-lookup"><span data-stu-id="3d1be-132">This calculates the kanban quantity proposal.</span></span>  
2. <span data-ttu-id="3d1be-133">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="3d1be-133">Click OK.</span></span>
3. <span data-ttu-id="3d1be-134">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="3d1be-134">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="3d1be-135">Athugið ráðlagt kanban-magn er 2.</span><span class="sxs-lookup"><span data-stu-id="3d1be-135">Notice the suggested kanban quantity is 2.</span></span>  

## <a name="change-product-quantity-and-calculate-again"></a><span data-ttu-id="3d1be-136">Breyta magni afurðar og reikna aftur</span><span class="sxs-lookup"><span data-stu-id="3d1be-136">Change product quantity and calculate again</span></span>
1. <span data-ttu-id="3d1be-137">Setja afurðarmagn á "5".</span><span class="sxs-lookup"><span data-stu-id="3d1be-137">Set Product quantity to '5'.</span></span>
2. <span data-ttu-id="3d1be-138">Smellt er á að reikna Út.</span><span class="sxs-lookup"><span data-stu-id="3d1be-138">Click Calculate.</span></span>
3. <span data-ttu-id="3d1be-139">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="3d1be-139">Click OK.</span></span>
    * <span data-ttu-id="3d1be-140">Athugið með kanban-magn 5 er tillaga breytt í kanban-magn 4.</span><span class="sxs-lookup"><span data-stu-id="3d1be-140">Notice that with a kanban quantity of 5, the suggestion is changed to a kanban quantity of 4.</span></span>  
    * <span data-ttu-id="3d1be-141">Þetta er vegna þeirrar staðreyndar að með lægra magn afurðar þurfum við fleiri kanban til að uppfylla eftirspurnina.</span><span class="sxs-lookup"><span data-stu-id="3d1be-141">This is caused by the fact that with a lower product quantity, we need more kanbans to fulfill the demand.</span></span>  

## <a name="update-kanban-rule"></a><span data-ttu-id="3d1be-142">Uppfæra kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="3d1be-142">Update kanban rule</span></span>
1. <span data-ttu-id="3d1be-143">Í reitnum dagsetning regluvirkni skal færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="3d1be-143">In the Rule effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="3d1be-144">Stilltu ‚Regla er virk frá og með dagsetningu' á dagsetningu í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="3d1be-144">Set the 'Rule active as of date' to a date in the future.</span></span> <span data-ttu-id="3d1be-145">Til dæmis í dag + eitt ár.</span><span class="sxs-lookup"><span data-stu-id="3d1be-145">For example, today + one year.</span></span>  
2. <span data-ttu-id="3d1be-146">Smelltu á Uppfæra.</span><span class="sxs-lookup"><span data-stu-id="3d1be-146">Click Update.</span></span>
3. <span data-ttu-id="3d1be-147">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="3d1be-147">Click OK.</span></span>
4. <span data-ttu-id="3d1be-148">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3d1be-148">Close the page.</span></span>

## <a name="validate-change-on-kanban-rule"></a><span data-ttu-id="3d1be-149">Villuleita breytingu á kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="3d1be-149">Validate change on kanban rule</span></span>
1. <span data-ttu-id="3d1be-150">Farið í upplýsingar um afurðarstjórnun > Lean-framleiðsla > Kanban-reglur.</span><span class="sxs-lookup"><span data-stu-id="3d1be-150">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="3d1be-151">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="3d1be-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3d1be-152">Velja kanban-reglu sem var stofnuð í fyrri undirverki.</span><span class="sxs-lookup"><span data-stu-id="3d1be-152">Select the kanban rule that was created in the previous sub-task.</span></span> <span data-ttu-id="3d1be-153">Þetta ætti að vera fyrsta kanban-reglu af listanum er raðað eftir númeri.</span><span class="sxs-lookup"><span data-stu-id="3d1be-153">This should be the first kanban rule in the list sorted by number.</span></span>  
3. <span data-ttu-id="3d1be-154">Víxla útvíkkun á liðnum upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="3d1be-154">Toggle the expansion of the Details section.</span></span>
    * <span data-ttu-id="3d1be-155">Athugið gildisdagsetning, sem þýðir að þessi regla er ekki virk til þessarar dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="3d1be-155">Notice the effective date, which means that this rule is not activated until this date.</span></span>  
4. <span data-ttu-id="3d1be-156">Víxla útvíkkun á liðnum magn.</span><span class="sxs-lookup"><span data-stu-id="3d1be-156">Toggle the expansion of the Quantities section.</span></span>
    * <span data-ttu-id="3d1be-157">Athugið að þetta er sjálfgefið magn sem fært var inn í útreikningi kanban-magns.</span><span class="sxs-lookup"><span data-stu-id="3d1be-157">Notice this is the default quantity that you entered on the kanban quantity calculation.</span></span>  
    * <span data-ttu-id="3d1be-158">Athugið að þetta er fast kanban-magn 4 úr útreikningi kanban-magns.</span><span class="sxs-lookup"><span data-stu-id="3d1be-158">Notice this is the fixed kanban quantity of 4 from the kanban quantity calculation.</span></span>  
5. <span data-ttu-id="3d1be-159">Smellt er á flipann ListPanel.</span><span class="sxs-lookup"><span data-stu-id="3d1be-159">Click the ListPanel tab.</span></span>

