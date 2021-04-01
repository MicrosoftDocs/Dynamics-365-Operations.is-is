---
title: Áætla framleiðslupöntun með rekstrar- og vinnuröðun
description: Þetta efni leggur áherslu á röðun á framleiðslupöntun með aðgerðaröðun og vinnsluröðun.
author: ChristianRytt
manager: tfehr
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 32ace204f1ec79cc8f9ce10ebfdc3606879e40d4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215842"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="4422d-103">Áætla framleiðslupöntun með rekstrar- og vinnuröðun</span><span class="sxs-lookup"><span data-stu-id="4422d-103">Schedule a production order with operations and job scheduling</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4422d-104">Þetta efni leggur áherslu á röðun á framleiðslupöntun með aðgerðaröðun og vinnsluröðun.</span><span class="sxs-lookup"><span data-stu-id="4422d-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="4422d-105">Engar vinnslur eru stofnaðar með aðgerðaröðun meðan störf eru stofnuð með vinnsluröðun.</span><span class="sxs-lookup"><span data-stu-id="4422d-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="4422d-106">Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.</span><span class="sxs-lookup"><span data-stu-id="4422d-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="4422d-107">Þetta ferli er ætluð fyrir framleiðslustjóri skipuleggjandi framleiðslu eða vinnusalarstjórnun yfirmaður sem unnið er í framleiðsluumhverfi afmörkuð.</span><span class="sxs-lookup"><span data-stu-id="4422d-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="4422d-108">Stofna framleiðslupöntun</span><span class="sxs-lookup"><span data-stu-id="4422d-108">Create a production order</span></span>
1. <span data-ttu-id="4422d-109">Í skoðunarsíðunni ferðu í **Kerfiseiningar > Framleiðslustýring > Framleiðslupantanir > Allar framleiðslupantanir**.</span><span class="sxs-lookup"><span data-stu-id="4422d-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="4422d-110">Veldu **Ný framleiðslupöntun**.</span><span class="sxs-lookup"><span data-stu-id="4422d-110">Select **New production order**.</span></span>
3. <span data-ttu-id="4422d-111">Í reitinn **Vörunúmer** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="4422d-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="4422d-112">Veldu vörunúmerið **D0001**.</span><span class="sxs-lookup"><span data-stu-id="4422d-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="4422d-113">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="4422d-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="4422d-114">Ef framkvæma á aðgerðaröðun fyrir framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="4422d-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="4422d-115">Merktu nýstofnaða röð.</span><span class="sxs-lookup"><span data-stu-id="4422d-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="4422d-116">Í aðgerðasvæðinu velurðu **Tímasetja**.</span><span class="sxs-lookup"><span data-stu-id="4422d-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="4422d-117">Veldu **Raða aðgerðum**.</span><span class="sxs-lookup"><span data-stu-id="4422d-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="4422d-118">Í reitnum **Röðunarstefna** er valið **Áfram frá röðunardagsetningu**.</span><span class="sxs-lookup"><span data-stu-id="4422d-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="4422d-119">Dagsetning er rituð í reitinn **Röðunardagsetning**.</span><span class="sxs-lookup"><span data-stu-id="4422d-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="4422d-120">Velja dagsetningu í framtíðinni, til dæmis í dag plús ein vika.</span><span class="sxs-lookup"><span data-stu-id="4422d-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="4422d-121">Með valda Röðun stefnu framleiðslupöntun verður raðað áfram frá þessari dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="4422d-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="4422d-122">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4422d-122">Select **OK**.</span></span>
7. <span data-ttu-id="4422d-123">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="4422d-123">In the list, mark the selected row.</span></span> <span data-ttu-id="4422d-124">Athugið að stöðu framleiðslu er breytt í **Tímasett**.</span><span class="sxs-lookup"><span data-stu-id="4422d-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="4422d-125">Veldu **Allar vinnslur**.</span><span class="sxs-lookup"><span data-stu-id="4422d-125">Select **All jobs**.</span></span> <span data-ttu-id="4422d-126">Athugið að engar vinnslur eru stofnaðar með aðgerðaröðun.</span><span class="sxs-lookup"><span data-stu-id="4422d-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="4422d-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="4422d-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="4422d-128">Ef framkvæma á aðgerðaröðun fyrir framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="4422d-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="4422d-129">Í aðgerðasvæðinu velurðu **Tímasetja**.</span><span class="sxs-lookup"><span data-stu-id="4422d-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="4422d-130">Veldu **Röðunarverk**.</span><span class="sxs-lookup"><span data-stu-id="4422d-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="4422d-131">Í reitnum **Röðunarstefna** er valið **Áfram frá röðunardagsetningu**.</span><span class="sxs-lookup"><span data-stu-id="4422d-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="4422d-132">Dagsetning er rituð í reitinn **Röðunardagsetning**.</span><span class="sxs-lookup"><span data-stu-id="4422d-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="4422d-133">Velja dagsetningu í framtíðinni, til dæmis í dag plús ein vika.</span><span class="sxs-lookup"><span data-stu-id="4422d-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="4422d-134">Með valda Röðun stefnu framleiðslupöntun verður raðað áfram frá þessari dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="4422d-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="4422d-135">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4422d-135">Select **OK**.</span></span>
6. <span data-ttu-id="4422d-136">Á aðgerðasvæðinu skal velja **Framleiðslupöntun**.</span><span class="sxs-lookup"><span data-stu-id="4422d-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="4422d-137">Veldu **Allar vinnslur**.</span><span class="sxs-lookup"><span data-stu-id="4422d-137">Select **All jobs**.</span></span> <span data-ttu-id="4422d-138">Athugið samkvæmt virk leið 5 störf eru stofnuð með vinnsluröðun.</span><span class="sxs-lookup"><span data-stu-id="4422d-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]