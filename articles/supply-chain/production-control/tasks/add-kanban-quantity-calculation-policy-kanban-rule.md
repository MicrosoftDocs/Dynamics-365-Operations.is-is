---
title: Bæta útreikningsreglu kanban-magns við kanban-reglu
description: Þetta ferli leggur áherslu á stofnun útreikningsstefnu kanban-magns og henni er bætt við kanban-reglu til að besta stærðar og magn kanban.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fffd623104dc403e230128c9234521ad1e39c7bb
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "352138"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="0a981-103">Bæta útreikningsreglu kanban-magns við kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="0a981-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0a981-104">Þetta ferli leggur áherslu á stofnun útreikningsstefnu kanban-magns og henni er bætt við kanban-reglu til að besta stærðar og magn kanban.</span><span class="sxs-lookup"><span data-stu-id="0a981-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="0a981-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="0a981-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0a981-106">Þetta ferli er ætlað fyrir virðisstraumsstjóra.</span><span class="sxs-lookup"><span data-stu-id="0a981-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="0a981-107">Þetta ferli er skilyrði til að stofna ferlið Reikna tillögur kanban-magns.</span><span class="sxs-lookup"><span data-stu-id="0a981-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="0a981-108">Stofna útreikningsreglu fyrir kanban-magn</span><span class="sxs-lookup"><span data-stu-id="0a981-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="0a981-109">Fara í Framleiðslustýringar > Reglubundin verkefni > Útreikning kanban-magns > Útreikningsreglur kanban-magns.</span><span class="sxs-lookup"><span data-stu-id="0a981-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="0a981-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="0a981-110">Click New.</span></span>
3. <span data-ttu-id="0a981-111">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="0a981-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="0a981-112">Til dæmis, skráið Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="0a981-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="0a981-113">Í aðaláætlunarreitnum skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="0a981-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0a981-114">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="0a981-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0a981-115">Veljið StaticPlan til að reikna út eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="0a981-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="0a981-116">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0a981-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="0a981-117">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="0a981-117">Click Save.</span></span>
8. <span data-ttu-id="0a981-118">Í svæðinu Lágmarks kanban-magn, færið inn '1'.</span><span class="sxs-lookup"><span data-stu-id="0a981-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="0a981-119">Þetta er aukanúmer kanbana sem er innifalið í útreikningi kanban-magns.</span><span class="sxs-lookup"><span data-stu-id="0a981-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="0a981-120">Setja öryggisstuðull á "1".</span><span class="sxs-lookup"><span data-stu-id="0a981-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="0a981-121">Þetta er the stuðull sem er notað í a‘ reikna út aukalegt magn öryggisbirgða.</span><span class="sxs-lookup"><span data-stu-id="0a981-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="0a981-122">Í dagar fram í tímann svæðinu, færið inn '30'.</span><span class="sxs-lookup"><span data-stu-id="0a981-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="0a981-123">Þetta er fjöldi daga fyrir dagsetningu útreiknings fyrir kanban-magn sem er innifalið í útreikningi eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="0a981-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="0a981-124">Færið inn '30' í Dagar aftur í tímann.</span><span class="sxs-lookup"><span data-stu-id="0a981-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="0a981-125">Þetta er fjöldi daga eftir dagsetningu útreiknings fyrir kanban-magn sem er innifalið í útreikningi eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="0a981-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="0a981-126">Formúla notuð við útreikning er sýnd með raungildin.</span><span class="sxs-lookup"><span data-stu-id="0a981-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="0a981-127">Fyrir dæmi, Kanban-magn = ((meðaltals dagleg eftirspurn x afhendingartími x 2,00) / Afurðarmagn per efnismeðhöndlunareining) + 1</span><span class="sxs-lookup"><span data-stu-id="0a981-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="0a981-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0a981-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="0a981-129">Bæta útreikningsreglu kanban-magns við kanban-reglu</span><span class="sxs-lookup"><span data-stu-id="0a981-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="0a981-130">Farið í upplýsingar um afurðarstjórnun > Lean-framleiðsla > Kanban-reglur.</span><span class="sxs-lookup"><span data-stu-id="0a981-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="0a981-131">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="0a981-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0a981-132">Velja kanban-reglu 000020 fyrir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="0a981-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="0a981-133">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0a981-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0a981-134">Víxla útvíkkun á hluta útreikningsreglur um kanban-magn.</span><span class="sxs-lookup"><span data-stu-id="0a981-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="0a981-135">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="0a981-135">Click Add.</span></span>
    * <span data-ttu-id="0a981-136">Bæta við útreikningsstefnu kanban-magns sem stofnuð hefur verið nýlega í fyrra undirverki.</span><span class="sxs-lookup"><span data-stu-id="0a981-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="0a981-137">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="0a981-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="0a981-138">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="0a981-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="0a981-139">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0a981-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0a981-140">Velja reglu fyrir Speaker2016 hafa nýverið var stofnuð í fyrri undirverki.</span><span class="sxs-lookup"><span data-stu-id="0a981-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  

