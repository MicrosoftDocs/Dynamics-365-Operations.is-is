---
title: Stofna vinnsluverkþætti fyrir lean-framleiðslu
description: Stofna ferlisverkþátt fyrir lean-framleiðslu.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 609a7872bd2388291aed88c0eb260b4a64d06391
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838608"
---
# <a name="create-process-activities-for-lean-manufacturing"></a><span data-ttu-id="ad5c5-103">Stofna vinnsluverkþætti fyrir lean-framleiðslu</span><span class="sxs-lookup"><span data-stu-id="ad5c5-103">Create process activities for lean manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ad5c5-104">Stofna ferlisverkþátt fyrir lean-framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-104">Create a process activity for lean manufacturing.</span></span> 

<span data-ttu-id="ad5c5-105">Skilyrði:</span><span class="sxs-lookup"><span data-stu-id="ad5c5-105">Prerequisites:</span></span> 

1. <span data-ttu-id="ad5c5-106">Stofna verður framleiðsluflæði og útgáfu sem er ekki virk.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="ad5c5-107">Stofna verður vinnuflokk.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-107">A work cell must be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="ad5c5-108">Finndu útgáfu framleiðsluflæðis</span><span class="sxs-lookup"><span data-stu-id="ad5c5-108">Find the production flow version</span></span>
1. <span data-ttu-id="ad5c5-109">Fara í Framleiðslustýringar > Uppsetning > Framleiðsluflæði fyrir lean > Framleiðsluflæði.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-109">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="ad5c5-110">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ad5c5-111">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-111">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="ad5c5-112">Stofnaðu nýja aðgerð</span><span class="sxs-lookup"><span data-stu-id="ad5c5-112">Create a new activity</span></span>
1. <span data-ttu-id="ad5c5-113">Smellt er á Verkþætti.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-113">Click Activities.</span></span>
    * <span data-ttu-id="ad5c5-114">Tryggja skal að valið framleiðsluflæði hafi útgáfu í drögum og velja þá útgáfu.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-114">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="ad5c5-115">Smellt er á verkþáttinn Stofna nýja áætlun.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-115">Click Create new plan activity.</span></span>
3. <span data-ttu-id="ad5c5-116">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-116">Click Next.</span></span>
4. <span data-ttu-id="ad5c5-117">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-117">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ad5c5-118">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-118">In the Name field, type a value.</span></span>
    * <span data-ttu-id="ad5c5-119">Athugið að heitið verður að vera einkvæmt fyrir gefið framleiðsluflæði fyrir allar útgáfur.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-119">Note that the name must be unique for a given production flow for all versions.</span></span>  
6. <span data-ttu-id="ad5c5-120">Í reitinn Vinna magn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-120">In the Process quantity field, enter a number.</span></span>
    * <span data-ttu-id="ad5c5-121">Athugið að óháð því hvaða magn vinnslu verður keyrt er þetta lágmarksmagn á hverja vinnslu til að reikna út kostnað við vinnu.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-121">Note that no matter what job quantity will be processed, this is the minimum quantity per job to calculate the labor cost.</span></span> <span data-ttu-id="ad5c5-122">Ef vinnsla á magn víkja frá þessu magni, verða kostnaðarfrávik vinnu stofnuð.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-122">If job quantities deviate from this quantity, labor cost variance will be created.</span></span>  
7. <span data-ttu-id="ad5c5-123">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-123">Click Next.</span></span>

## <a name="select-the-work-cell"></a><span data-ttu-id="ad5c5-124">Veldu vinnuflokk</span><span class="sxs-lookup"><span data-stu-id="ad5c5-124">Select the work cell</span></span>
1. <span data-ttu-id="ad5c5-125">Í reitnum vinnuflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-125">In the Work cell field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="ad5c5-126">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-126">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="ad5c5-127">Skilgreina uppfærslur birgða</span><span class="sxs-lookup"><span data-stu-id="ad5c5-127">Define the inventory updates</span></span>
1. <span data-ttu-id="ad5c5-128">Velja eða hreinsa gátreitinn Uppfærsla á innhreyfingu á lager.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-128">Select or clear the Update on hand receipt check box.</span></span>
    * <span data-ttu-id="ad5c5-129">Ef Uppfæra á lager = Nei, er hægt að skilgreina verkþátt til að taka við hálfkláraðri afurð (verkþátturinn nær ekki næsta stigi í Uppskrift).</span><span class="sxs-lookup"><span data-stu-id="ad5c5-129">If Update On hand = No, you can define the activity to receive a semi-finished product (the activity does not reach the next BOM level).</span></span>    <span data-ttu-id="ad5c5-130">Einnig er hægt að velja að nota hálfkláraðar afurðir.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-130">You can also select to consume semi-finished products.</span></span>  

## <a name="define-the-picking-activities"></a><span data-ttu-id="ad5c5-131">Skilgreina tiltektarverkþættina</span><span class="sxs-lookup"><span data-stu-id="ad5c5-131">Define the picking activities</span></span>
1. <span data-ttu-id="ad5c5-132">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-132">Click Next.</span></span>
2. <span data-ttu-id="ad5c5-133">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-133">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ad5c5-134">Sjálfgefinn tiltektarverkþáttur er stofnaður fyrir ílagsstaðsetningu valins vinnuflokks.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-134">A default picking activity is created for the input location of the selected work cell.</span></span>  
3. <span data-ttu-id="ad5c5-135">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-135">Click Add.</span></span>
    * <span data-ttu-id="ad5c5-136">Hægt er að stofna viðbótar tiltektarverkþætti fyrir tilteknar vörur sem eru ekki sett í ílagsverkþætti vinnuflokks.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-136">You can create additional picking activities for specific products, that are not staged at the work cell input activity.</span></span>  
4. <span data-ttu-id="ad5c5-137">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="ad5c5-138">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-138">In the Item number field, type a value.</span></span>
6. <span data-ttu-id="ad5c5-139">Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-139">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ad5c5-140">Með þessari skilgreiningu er allt notað efni í verkþættinum tekið úr sjálfgefnu ílagsvöruhúsi og staðsetningu nema vara sem skilgreind er í annarri tiltektaraðgerð.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-140">With this definition, all materials consumed in the activity are picked from the default input warehouse and location except the item that is defined in the second picking activity.</span></span> <span data-ttu-id="ad5c5-141">Þessi vara verður tekið úr öðru vöruhúsi og staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-141">This item will be picked from a different warehouse and location.</span></span>  
7. <span data-ttu-id="ad5c5-142">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-142">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="ad5c5-143">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-143">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="ad5c5-144">Veldu eða hreinsaðu gátreitinn Skrá úrkast.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-144">Select or clear the Register scrap check box.</span></span>
10. <span data-ttu-id="ad5c5-145">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-145">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="ad5c5-146">Skilgreina tíma verkþátta</span><span class="sxs-lookup"><span data-stu-id="ad5c5-146">Define the activity times</span></span>
1. <span data-ttu-id="ad5c5-147">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-147">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ad5c5-148">Skilgreiningar er krafist á Keyrslutíma.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-148">The definition of a Runtime is required.</span></span> <span data-ttu-id="ad5c5-149">Keyrslutími er notaður til að reikna út kostnað og gegnumstreymistíma kanban-vinnslurnar.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-149">The Runtime is used to calculate costs and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="ad5c5-150">Keyrslur eru ekki notaðar til að reikna álag og notkun, það er reiknað út með tíma ferlis úr verkinu útgáfu framleiðsluflæðis framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-150">Runtimes are not used to calculate capacity load and consumption, this is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="ad5c5-151">Í reitinn Tími skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-151">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="ad5c5-152">Í reitnum Eining skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-152">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="ad5c5-153">Velja tímaeiningu.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-153">Select the Time unit.</span></span>
5. <span data-ttu-id="ad5c5-154">Í reitinn Á magn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-154">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="ad5c5-155">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-155">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ad5c5-156">Biðtímar eru valfrjálsir.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-156">Queue times are optional.</span></span>  
7. <span data-ttu-id="ad5c5-157">Í reitinn Tími skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-157">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="ad5c5-158">Í reitnum Eining skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-158">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="ad5c5-159">Velja tímaeiningu.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-159">Select the Time unit.</span></span>
10. <span data-ttu-id="ad5c5-160">Í reitinn Á magn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-160">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="ad5c5-161">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-161">Click Next.</span></span>
12. <span data-ttu-id="ad5c5-162">Smellt er á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-162">Click Finish.</span></span>
13. <span data-ttu-id="ad5c5-163">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ad5c5-163">Close the page.</span></span>

