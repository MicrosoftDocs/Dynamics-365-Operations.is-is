--- 
title: "Stofna flutningsverkþætti fyrir lean-framleiðslu"
description: "Stofna flutningsverkþátt fyrir lean-framleiðslu."
author: cvocph
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: e50b2fc071c3f89b8bf1b118da2b46a0b44d6c25
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2018

---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="7c832-103">Stofna flutningsverkþætti fyrir lean-framleiðslu</span><span class="sxs-lookup"><span data-stu-id="7c832-103">Create transfer activities for lean manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7c832-104">Stofna flutningsverkþátt fyrir lean-framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="7c832-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="7c832-105">Skilyrði:</span><span class="sxs-lookup"><span data-stu-id="7c832-105">Prerequisites:</span></span> 

1. <span data-ttu-id="7c832-106">Stofna verður framleiðsluflæði og útgáfu sem er ekki virk.</span><span class="sxs-lookup"><span data-stu-id="7c832-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="7c832-107">Stofna verður Úr og í vöruhús og staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="7c832-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="7c832-108">Einnig er hægt að stofna áfyllingu eða áfyllingarvinnuflokk.</span><span class="sxs-lookup"><span data-stu-id="7c832-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="7c832-109">Finndu útgáfu framleiðsluflæðis</span><span class="sxs-lookup"><span data-stu-id="7c832-109">Find the production flow version</span></span>
1. <span data-ttu-id="7c832-110">Fara í Framleiðslustýringar > Uppsetning > Framleiðsluflæði fyrir lean > Framleiðsluflæði.</span><span class="sxs-lookup"><span data-stu-id="7c832-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="7c832-111">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="7c832-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7c832-112">Athugið að framleiðsluflæði verður að hafa útgáfu stöðuna drög.</span><span class="sxs-lookup"><span data-stu-id="7c832-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="7c832-113">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7c832-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="7c832-114">Stofnaðu nýja aðgerð</span><span class="sxs-lookup"><span data-stu-id="7c832-114">Create a new activity</span></span>
1. <span data-ttu-id="7c832-115">Smellt er á Verkþætti.</span><span class="sxs-lookup"><span data-stu-id="7c832-115">Click Activities.</span></span>
    * <span data-ttu-id="7c832-116">Tryggja skal að valið framleiðsluflæði hafi útgáfu í drögum og velja þá útgáfu.</span><span class="sxs-lookup"><span data-stu-id="7c832-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="7c832-117">Smellt er á verkþáttinn Stofna nýja áætlun.</span><span class="sxs-lookup"><span data-stu-id="7c832-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="7c832-118">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="7c832-118">Click Next.</span></span>
4. <span data-ttu-id="7c832-119">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7c832-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="7c832-120">Í reitnum Gerð verkþáttar skal velja ‚Flytja‘.</span><span class="sxs-lookup"><span data-stu-id="7c832-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="7c832-121">Í reitinn Vinna magn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="7c832-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="7c832-122">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="7c832-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="7c832-123">Velja vinnuflokkana</span><span class="sxs-lookup"><span data-stu-id="7c832-123">Select the Work cells</span></span>
1. <span data-ttu-id="7c832-124">Í reitnum Áfylling skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="7c832-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="7c832-125">Til að nota frálagsstaðsetningar vinnuflokksins sem frá staðsetningu í flutningsverkþætti skal velja vinnuflokk.</span><span class="sxs-lookup"><span data-stu-id="7c832-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="7c832-126">Hægt er að gera sama við áfylltan vinnuflokk, sem setur markstaðsetningu fyrir flutning verkþáttar.</span><span class="sxs-lookup"><span data-stu-id="7c832-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="7c832-127">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7c832-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="7c832-128">Skilgreina uppfærslur birgða</span><span class="sxs-lookup"><span data-stu-id="7c832-128">Define the inventory updates</span></span>
1. <span data-ttu-id="7c832-129">Í reitnum Gerð afurðar skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="7c832-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="7c832-130">Athugið að flutningur breytir ekki gerð afurðar.</span><span class="sxs-lookup"><span data-stu-id="7c832-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="7c832-131">Hægt er að flytja hálfkláraðar vörur eða tilbúnar afurðir (flutning á milli tveggja verkþátta framleiðsluflæðis og mögulega kanban-flæði).</span><span class="sxs-lookup"><span data-stu-id="7c832-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="7c832-132">Þegar tilbúnar afurðir eru fluttar er hægt að velja hvort tiltekt eða móttaka skili af sér birgðafærslu.</span><span class="sxs-lookup"><span data-stu-id="7c832-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="7c832-133">Skilgreina flutningsstaðsetningar</span><span class="sxs-lookup"><span data-stu-id="7c832-133">Define the transfer locations</span></span>
1. <span data-ttu-id="7c832-134">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="7c832-134">Click Next.</span></span>
2. <span data-ttu-id="7c832-135">Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="7c832-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="7c832-136">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="7c832-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="7c832-137">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7c832-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="7c832-138">Í reitnum staðsetning skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="7c832-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="7c832-139">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7c832-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="7c832-140">Í reitnum Frakt eftir reit skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="7c832-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="7c832-141">Meðal valkosta eru: Farmsendanda - fyrirtækið vöruhús til sendingar í gangi, Viðtakanda - fyrirtækið rekstrareiningar í móttöku vöruhúss, Farmflytjanda - lánardrottinn þriðja aðila.</span><span class="sxs-lookup"><span data-stu-id="7c832-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="7c832-142">Ef fyrirtækið rekstrareiningar er lánardrottinn krefst flutningsverkþátturinn undirverktakasamnings.</span><span class="sxs-lookup"><span data-stu-id="7c832-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="7c832-143">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="7c832-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="7c832-144">Skilgreina tíma verkþátta</span><span class="sxs-lookup"><span data-stu-id="7c832-144">Define the activity times</span></span>
1. <span data-ttu-id="7c832-145">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="7c832-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7c832-146">Skilgreiningar er krafist á Keyrslutíma.</span><span class="sxs-lookup"><span data-stu-id="7c832-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="7c832-147">Keyrslutími er notaður til að reikna út kostnað og gegnumstreymi tímum kanban-vinnslurnar.</span><span class="sxs-lookup"><span data-stu-id="7c832-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="7c832-148">Keyrslutímar eru ekki notaðir til að reikna álag og notkun sem er reiknað með tíma ferlis úr verkinu útgáfu framleiðsluflæðis framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="7c832-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="7c832-149">Í reitinn Tími skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="7c832-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="7c832-150">Í reitnum Eining skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7c832-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="7c832-151">Velja tímaeiningu.</span><span class="sxs-lookup"><span data-stu-id="7c832-151">Select the Time unit.</span></span>
5. <span data-ttu-id="7c832-152">Í reitinn Á magn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="7c832-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="7c832-153">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="7c832-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7c832-154">Biðtímar eru valfrjálsir.</span><span class="sxs-lookup"><span data-stu-id="7c832-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="7c832-155">Í reitinn Tími skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="7c832-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="7c832-156">Í reitnum Eining skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7c832-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="7c832-157">Velja tímaeiningu.</span><span class="sxs-lookup"><span data-stu-id="7c832-157">Select the Time unit.</span></span>
10. <span data-ttu-id="7c832-158">Í reitinn Á magn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="7c832-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="7c832-159">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="7c832-159">Click Next.</span></span>
12. <span data-ttu-id="7c832-160">Smellt er á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="7c832-160">Click Finish.</span></span>
13. <span data-ttu-id="7c832-161">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7c832-161">Close the page.</span></span>


