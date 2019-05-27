---
title: Ferill runupöntunar frá stofnun til upphafs
description: Þetta ferli fer í gegnum fyrsti hluti lífsferlisins runupöntun.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6484c1954ff4cc600938adb07b5384f1edce8bf7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545903"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="f9d90-103">Ferill runupöntunar frá stofnun til upphafs</span><span class="sxs-lookup"><span data-stu-id="f9d90-103">Batch order lifecycle from create to start</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f9d90-104">Þetta ferli fer í gegnum fyrsti hluti lífsferlisins runupöntun.</span><span class="sxs-lookup"><span data-stu-id="f9d90-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="f9d90-105">Frá stofnun, kostnaður mat og yfir framleiðslu vinnsluröðun til raunveruleg upphafsdagsetning fyrir runupöntun.</span><span class="sxs-lookup"><span data-stu-id="f9d90-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="f9d90-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="f9d90-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="f9d90-107">Skilyrði til að keyra ferlið með annarri gagnamengi eru útgefin afurð með virka útgáfu formúlu og leiðarútgáfa.</span><span class="sxs-lookup"><span data-stu-id="f9d90-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="f9d90-108">Stofna runupöntun</span><span class="sxs-lookup"><span data-stu-id="f9d90-108">Create a batch order</span></span>
1. <span data-ttu-id="f9d90-109">Fara í Allar framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="f9d90-109">Go to All production orders.</span></span>
2. <span data-ttu-id="f9d90-110">Smellt er á Ný runupöntun</span><span class="sxs-lookup"><span data-stu-id="f9d90-110">Click New batch order.</span></span>
3. <span data-ttu-id="f9d90-111">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="f9d90-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="f9d90-112">Smellið á Stofna.</span><span class="sxs-lookup"><span data-stu-id="f9d90-112">Click Create.</span></span>
5. <span data-ttu-id="f9d90-113">Nota flýtiafmörkun til að sía í reitnum afurð með gildið „b“.</span><span class="sxs-lookup"><span data-stu-id="f9d90-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="f9d90-114">Skoða framleiðsluformúlu og áætlaða aukaafurðir</span><span class="sxs-lookup"><span data-stu-id="f9d90-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="f9d90-115">Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="f9d90-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="f9d90-116">Smellt er á Formúlu.</span><span class="sxs-lookup"><span data-stu-id="f9d90-116">Click Formula.</span></span>
3. <span data-ttu-id="f9d90-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f9d90-117">Close the page.</span></span>
4. <span data-ttu-id="f9d90-118">Smellt er á aukaafurðir.</span><span class="sxs-lookup"><span data-stu-id="f9d90-118">Click Co-products.</span></span>
5. <span data-ttu-id="f9d90-119">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f9d90-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="f9d90-120">Áætla runupöntunina</span><span class="sxs-lookup"><span data-stu-id="f9d90-120">Estimate the batch order</span></span>
1. <span data-ttu-id="f9d90-121">Smellt er á Mat.</span><span class="sxs-lookup"><span data-stu-id="f9d90-121">Click Estimate.</span></span>
2. <span data-ttu-id="f9d90-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f9d90-122">Click OK.</span></span>
3. <span data-ttu-id="f9d90-123">Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.</span><span class="sxs-lookup"><span data-stu-id="f9d90-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="f9d90-124">Smellt er á Skoða útreikningsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="f9d90-124">Click View calculation details.</span></span>
5. <span data-ttu-id="f9d90-125">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f9d90-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="f9d90-126">Losa runupöntunina</span><span class="sxs-lookup"><span data-stu-id="f9d90-126">Release the batch order</span></span>
1. <span data-ttu-id="f9d90-127">Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="f9d90-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="f9d90-128">Smellið á „Gefa út“.</span><span class="sxs-lookup"><span data-stu-id="f9d90-128">Click Release.</span></span>
3. <span data-ttu-id="f9d90-129">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f9d90-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="f9d90-130">Áætla framleiðsluverk</span><span class="sxs-lookup"><span data-stu-id="f9d90-130">Schedule production jobs</span></span>
1. <span data-ttu-id="f9d90-131">Í Aðgerðarrúðunni er smellt á Áætlun.</span><span class="sxs-lookup"><span data-stu-id="f9d90-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="f9d90-132">Smella á Áætla verk.</span><span class="sxs-lookup"><span data-stu-id="f9d90-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="f9d90-133">Veljið Nei í svæðinu Takmarkaða afkastaveita.</span><span class="sxs-lookup"><span data-stu-id="f9d90-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="f9d90-134">Veljið Nei í svæðinu Takmarkað efni.</span><span class="sxs-lookup"><span data-stu-id="f9d90-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="f9d90-135">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="f9d90-135">Click OK.</span></span>
6. <span data-ttu-id="f9d90-136">Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="f9d90-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="f9d90-137">Smellt er á Allar vinnslur.</span><span class="sxs-lookup"><span data-stu-id="f9d90-137">Click All jobs.</span></span>
8. <span data-ttu-id="f9d90-138">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f9d90-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="f9d90-139">Ræsið runupöntunina</span><span class="sxs-lookup"><span data-stu-id="f9d90-139">Start the batch order</span></span>
1. <span data-ttu-id="f9d90-140">Smellið á „Byrja“.</span><span class="sxs-lookup"><span data-stu-id="f9d90-140">Click Start.</span></span>
2. <span data-ttu-id="f9d90-141">Smellið á flipann „Almennt“.</span><span class="sxs-lookup"><span data-stu-id="f9d90-141">Click the General tab.</span></span>
3. <span data-ttu-id="f9d90-142">Veljið „Nei“ á svæðinu „Bóka tiltektarlista núna“.</span><span class="sxs-lookup"><span data-stu-id="f9d90-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="f9d90-143">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f9d90-143">Click OK.</span></span>
5. <span data-ttu-id="f9d90-144">Smellið á „Skoða“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="f9d90-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="f9d90-145">Smellt er á tiltektarlista.</span><span class="sxs-lookup"><span data-stu-id="f9d90-145">Click Picking list.</span></span>
7. <span data-ttu-id="f9d90-146">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f9d90-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f9d90-147">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f9d90-147">Close the page.</span></span>
9. <span data-ttu-id="f9d90-148">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f9d90-148">Close the page.</span></span>
10. <span data-ttu-id="f9d90-149">Smellt er á Leiðarspjald.</span><span class="sxs-lookup"><span data-stu-id="f9d90-149">Click Route card.</span></span>
11. <span data-ttu-id="f9d90-150">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f9d90-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="f9d90-151">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f9d90-151">Close the page.</span></span>
13. <span data-ttu-id="f9d90-152">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f9d90-152">Close the page.</span></span>

