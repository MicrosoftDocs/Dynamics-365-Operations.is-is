---
title: Stofna flutningsverkþætti fyrir lean-framleiðslu
description: Stofna flutningsverkþátt fyrir lean-framleiðslu.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityWizard, LeanWorkCellLookup, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 36f79ef189924b0f3bd38cb764e73c6a0793353e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545383"
---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="19d00-103">Stofna flutningsverkþætti fyrir lean-framleiðslu</span><span class="sxs-lookup"><span data-stu-id="19d00-103">Create transfer activities for lean manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="19d00-104">Stofna flutningsverkþátt fyrir lean-framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="19d00-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="19d00-105">Skilyrði:</span><span class="sxs-lookup"><span data-stu-id="19d00-105">Prerequisites:</span></span> 

1. <span data-ttu-id="19d00-106">Stofna verður framleiðsluflæði og útgáfu sem er ekki virk.</span><span class="sxs-lookup"><span data-stu-id="19d00-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="19d00-107">Stofna verður Úr og í vöruhús og staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="19d00-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="19d00-108">Einnig er hægt að stofna áfyllingu eða áfyllingarvinnuflokk.</span><span class="sxs-lookup"><span data-stu-id="19d00-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="19d00-109">Finndu útgáfu framleiðsluflæðis</span><span class="sxs-lookup"><span data-stu-id="19d00-109">Find the production flow version</span></span>
1. <span data-ttu-id="19d00-110">Fara í Framleiðslustýringar > Uppsetning > Framleiðsluflæði fyrir lean > Framleiðsluflæði.</span><span class="sxs-lookup"><span data-stu-id="19d00-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="19d00-111">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="19d00-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="19d00-112">Athugið að framleiðsluflæði verður að hafa útgáfu stöðuna drög.</span><span class="sxs-lookup"><span data-stu-id="19d00-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="19d00-113">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="19d00-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="19d00-114">Stofnaðu nýja aðgerð</span><span class="sxs-lookup"><span data-stu-id="19d00-114">Create a new activity</span></span>
1. <span data-ttu-id="19d00-115">Smellt er á Verkþætti.</span><span class="sxs-lookup"><span data-stu-id="19d00-115">Click Activities.</span></span>
    * <span data-ttu-id="19d00-116">Tryggja skal að valið framleiðsluflæði hafi útgáfu í drögum og velja þá útgáfu.</span><span class="sxs-lookup"><span data-stu-id="19d00-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="19d00-117">Smellt er á verkþáttinn Stofna nýja áætlun.</span><span class="sxs-lookup"><span data-stu-id="19d00-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="19d00-118">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="19d00-118">Click Next.</span></span>
4. <span data-ttu-id="19d00-119">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="19d00-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="19d00-120">Í reitnum Gerð verkþáttar skal velja ‚Flytja‘.</span><span class="sxs-lookup"><span data-stu-id="19d00-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="19d00-121">Í reitinn Vinna magn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="19d00-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="19d00-122">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="19d00-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="19d00-123">Velja vinnuflokkana</span><span class="sxs-lookup"><span data-stu-id="19d00-123">Select the Work cells</span></span>
1. <span data-ttu-id="19d00-124">Í reitnum Áfylling skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="19d00-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="19d00-125">Til að nota frálagsstaðsetningar vinnuflokksins sem frá staðsetningu í flutningsverkþætti skal velja vinnuflokk.</span><span class="sxs-lookup"><span data-stu-id="19d00-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="19d00-126">Hægt er að gera sama við áfylltan vinnuflokk, sem setur markstaðsetningu fyrir flutning verkþáttar.</span><span class="sxs-lookup"><span data-stu-id="19d00-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="19d00-127">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="19d00-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="19d00-128">Skilgreina uppfærslur birgða</span><span class="sxs-lookup"><span data-stu-id="19d00-128">Define the inventory updates</span></span>
1. <span data-ttu-id="19d00-129">Í reitnum Gerð afurðar skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="19d00-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="19d00-130">Athugið að flutningur breytir ekki gerð afurðar.</span><span class="sxs-lookup"><span data-stu-id="19d00-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="19d00-131">Hægt er að flytja hálfkláraðar vörur eða tilbúnar afurðir (flutning á milli tveggja verkþátta framleiðsluflæðis og mögulega kanban-flæði).</span><span class="sxs-lookup"><span data-stu-id="19d00-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="19d00-132">Þegar tilbúnar afurðir eru fluttar er hægt að velja hvort tiltekt eða móttaka skili af sér birgðafærslu.</span><span class="sxs-lookup"><span data-stu-id="19d00-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="19d00-133">Skilgreina flutningsstaðsetningar</span><span class="sxs-lookup"><span data-stu-id="19d00-133">Define the transfer locations</span></span>
1. <span data-ttu-id="19d00-134">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="19d00-134">Click Next.</span></span>
2. <span data-ttu-id="19d00-135">Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="19d00-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="19d00-136">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="19d00-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="19d00-137">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="19d00-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="19d00-138">Í reitnum staðsetning skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="19d00-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="19d00-139">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="19d00-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="19d00-140">Í reitnum Frakt eftir reit skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="19d00-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="19d00-141">Meðal valkosta eru: Farmsendanda - fyrirtækið vöruhús til sendingar í gangi, Viðtakanda - fyrirtækið rekstrareiningar í móttöku vöruhúss, Farmflytjanda - lánardrottinn þriðja aðila.</span><span class="sxs-lookup"><span data-stu-id="19d00-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="19d00-142">Ef fyrirtækið rekstrareiningar er lánardrottinn krefst flutningsverkþátturinn undirverktakasamnings.</span><span class="sxs-lookup"><span data-stu-id="19d00-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="19d00-143">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="19d00-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="19d00-144">Skilgreina tíma verkþátta</span><span class="sxs-lookup"><span data-stu-id="19d00-144">Define the activity times</span></span>
1. <span data-ttu-id="19d00-145">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="19d00-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="19d00-146">Skilgreiningar er krafist á Keyrslutíma.</span><span class="sxs-lookup"><span data-stu-id="19d00-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="19d00-147">Keyrslutími er notaður til að reikna út kostnað og gegnumstreymi tímum kanban-vinnslurnar.</span><span class="sxs-lookup"><span data-stu-id="19d00-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="19d00-148">Keyrslutímar eru ekki notaðir til að reikna álag og notkun sem er reiknað með tíma ferlis úr verkinu útgáfu framleiðsluflæðis framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="19d00-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="19d00-149">Í reitinn Tími skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="19d00-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="19d00-150">Í reitnum Eining skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="19d00-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="19d00-151">Velja tímaeiningu.</span><span class="sxs-lookup"><span data-stu-id="19d00-151">Select the Time unit.</span></span>
5. <span data-ttu-id="19d00-152">Í reitinn Á magn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="19d00-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="19d00-153">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="19d00-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="19d00-154">Biðtímar eru valfrjálsir.</span><span class="sxs-lookup"><span data-stu-id="19d00-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="19d00-155">Í reitinn Tími skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="19d00-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="19d00-156">Í reitnum Eining skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="19d00-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="19d00-157">Velja tímaeiningu.</span><span class="sxs-lookup"><span data-stu-id="19d00-157">Select the Time unit.</span></span>
10. <span data-ttu-id="19d00-158">Í reitinn Á magn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="19d00-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="19d00-159">Smelltu á Næsta.</span><span class="sxs-lookup"><span data-stu-id="19d00-159">Click Next.</span></span>
12. <span data-ttu-id="19d00-160">Smellt er á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="19d00-160">Click Finish.</span></span>
13. <span data-ttu-id="19d00-161">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="19d00-161">Close the page.</span></span>

