---
title: Uppsetning rafrænna undirskrifta
description: Notaðu þetta ferli til að setja upp rafrænar undirskriftir.
author: maertenm
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysConfiguration, SIGParameters, SIGReasonCode, SIGProcSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ad4ef067841511e235dcf538c720b72283d31c3
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178367"
---
# <a name="set-up-electronic-signatures"></a><span data-ttu-id="f5f63-103">Uppsetning rafrænna undirskrifta</span><span class="sxs-lookup"><span data-stu-id="f5f63-103">Set up electronic signatures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f5f63-104">Notaðu þetta ferli til að setja upp rafrænar undirskriftir.</span><span class="sxs-lookup"><span data-stu-id="f5f63-104">Use this procedure to set up electronic signatures.</span></span> <span data-ttu-id="f5f63-105">Rafræn undirskrift staðfestir deili á þeim aðila sem er í þann mund að hefja eða samþykkja ferli.</span><span class="sxs-lookup"><span data-stu-id="f5f63-105">An electronic signature confirms the identity of a person who is about to start or approve a computing process.</span></span> <span data-ttu-id="f5f63-106">Sýnigögn gögn fyrirtækisins til að stofna þetta ferli er DAT.</span><span class="sxs-lookup"><span data-stu-id="f5f63-106">The demo data company used to create this procedure is DAT.</span></span>


## <a name="enable-the-electronic-signature-configuration-key"></a><span data-ttu-id="f5f63-107">Virkja skilgreiningarlykilinn Rafræn undirskrift</span><span class="sxs-lookup"><span data-stu-id="f5f63-107">Enable the Electronic signature configuration key</span></span>
1. <span data-ttu-id="f5f63-108">Fara í Kerfisstjórnun > Uppsetning > Skilgreining leyfis.</span><span class="sxs-lookup"><span data-stu-id="f5f63-108">Go to System administration > Setup > License configuration.</span></span>
2. <span data-ttu-id="f5f63-109">Í trénu skal víkka út „Stjórnun“.</span><span class="sxs-lookup"><span data-stu-id="f5f63-109">In the tree, expand 'Administration'.</span></span>
    * <span data-ttu-id="f5f63-110">Staðfesta að gátreiturinn Rafræn undirskrift sé valinn.</span><span class="sxs-lookup"><span data-stu-id="f5f63-110">Verify that the Electronic signature check box is selected.</span></span>  
    * <span data-ttu-id="f5f63-111">Ef gátreiturinn Rafræn undirskrift er ekki valinn þarf að virkja viðhaldsham.</span><span class="sxs-lookup"><span data-stu-id="f5f63-111">If the Electronic signature check box is not selected, you must enable maintenance mode.</span></span> <span data-ttu-id="f5f63-112">Hægt er að virkja viðhaldsham í þessu umhverfi með því að keyra viðhaldvinnslu frá Lifecycle Services eða með því að nota verkfærið Deployment.Setup staðbundið.</span><span class="sxs-lookup"><span data-stu-id="f5f63-112">Maintenance mode can be enabled in this environment by running a maintenance job from Lifecycle Services, or by using the Deployment.Setup tool locally.</span></span>  
3. <span data-ttu-id="f5f63-113">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f5f63-113">Close the page.</span></span>

## <a name="set-up-electronic-signature-parameters"></a><span data-ttu-id="f5f63-114">Uppsetning á færibreytum rafræna undirskrifta</span><span class="sxs-lookup"><span data-stu-id="f5f63-114">Set up electronic signature parameters</span></span>
1. <span data-ttu-id="f5f63-115">Fara í Fyrirtækisstjórnun > Uppsetning > Rafræn undirskrift > Færibreytur rafrænna undirskrifta.</span><span class="sxs-lookup"><span data-stu-id="f5f63-115">Go to Organization administration > Setup > Electronic signature > Electronic signature parameters.</span></span>
2. <span data-ttu-id="f5f63-116">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="f5f63-116">Click Edit.</span></span>
3. <span data-ttu-id="f5f63-117">Í reitinn Tilkynning skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f5f63-117">In the Notice field, type a value.</span></span>
    * <span data-ttu-id="f5f63-118">Færðu inn tilkynningu sem notendur fá þegar beðið er um undirskrift.</span><span class="sxs-lookup"><span data-stu-id="f5f63-118">Enter the notice that signers will receive when a signature is requested.</span></span> <span data-ttu-id="f5f63-119">Hægt er að færa inn hvaða texta sem er.</span><span class="sxs-lookup"><span data-stu-id="f5f63-119">You can enter any text.</span></span> <span data-ttu-id="f5f63-120">Venjulega segir þessi texti notanda frá því hvað rafræn undirskrift felur í sér.</span><span class="sxs-lookup"><span data-stu-id="f5f63-120">Typically, this text tells the user what it means to sign a document electronically.</span></span>  
    * <span data-ttu-id="f5f63-121">Ef óskað er að færa inn texta fyrir Tilkynningar á öðrum tungumálum, smellið á hnappinn Þýðingar.</span><span class="sxs-lookup"><span data-stu-id="f5f63-121">If you want to enter the Notice text in additional languages, click the Translations button.</span></span>  
4. <span data-ttu-id="f5f63-122">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f5f63-122">Click Save.</span></span>
5. <span data-ttu-id="f5f63-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f5f63-123">Close the page.</span></span>

## <a name="set-up-reason-codes-for-electronic-signatures"></a><span data-ttu-id="f5f63-124">Setja upp ástæðukóða fyrir rafrænar undirskriftir</span><span class="sxs-lookup"><span data-stu-id="f5f63-124">Set up reason codes for electronic signatures</span></span>
1. <span data-ttu-id="f5f63-125">Fara í Fyrirtækisstjórnun > Uppsetning > Rafræn undirskrift > Ástæðukóðar rafrænna undirskrifta.</span><span class="sxs-lookup"><span data-stu-id="f5f63-125">Go to Organization administration > Setup > Electronic signature > Electronic signature reason codes.</span></span>
2. <span data-ttu-id="f5f63-126">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f5f63-126">Click New.</span></span>
    * <span data-ttu-id="f5f63-127">Áður en hægt er að nota rafrænar undirskriftir verður að setja upp ástæðukóða.</span><span class="sxs-lookup"><span data-stu-id="f5f63-127">You must set up reason codes before using electronic signatures.</span></span> <span data-ttu-id="f5f63-128">Þegar skjal er undirritað þarf að gefa upp gildan ástæðukóða.</span><span class="sxs-lookup"><span data-stu-id="f5f63-128">A valid reason code is required when signing a document.</span></span>     <span data-ttu-id="f5f63-129">Áritari velur ástæðukóða til að tilgreina tilgang rafrænnar undirskriftar.</span><span class="sxs-lookup"><span data-stu-id="f5f63-129">A signer selects a reason code to indicate the purpose of an electronic signature.</span></span> <span data-ttu-id="f5f63-130">Til dæmis gæti ástæðukóði gefið til kynna lagalegt samþykki.</span><span class="sxs-lookup"><span data-stu-id="f5f63-130">For example, a reason code could be used to indicate legal approval.</span></span>  
3. <span data-ttu-id="f5f63-131">Í reitinn Ástæðukóði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f5f63-131">In the Reason code field, type a value.</span></span>
4. <span data-ttu-id="f5f63-132">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="f5f63-132">In the Description field, type a value.</span></span>
    * <span data-ttu-id="f5f63-133">Færa inn viðbótar ástæðukóða, ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="f5f63-133">Enter additional reason codes, if needed.</span></span>  
5. <span data-ttu-id="f5f63-134">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f5f63-134">Click Save.</span></span>
6. <span data-ttu-id="f5f63-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f5f63-135">Close the page.</span></span>

## <a name="require-electronic-signatures-for-existing-processes"></a><span data-ttu-id="f5f63-136">Krefjast rafrænna undirskrifta fyrir fyrirliggjandi ferli</span><span class="sxs-lookup"><span data-stu-id="f5f63-136">Require electronic signatures for existing processes</span></span>
1. <span data-ttu-id="f5f63-137">Fara í Fyrirtækisstjórnun > Uppsetning > Rafræn undirskrift > Kröfur um rafrænar undirskriftir.</span><span class="sxs-lookup"><span data-stu-id="f5f63-137">Go to Organization administration > Setup > Electronic signature > Electronic signature requirements.</span></span>
2. <span data-ttu-id="f5f63-138">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f5f63-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f5f63-139">Velja ferli sem krefst rafrænna undirskrifta.</span><span class="sxs-lookup"><span data-stu-id="f5f63-139">Select a process that requires electronic signatures.</span></span>  
3. <span data-ttu-id="f5f63-140">Veldu eða hreinsaðu gátreitinn Undirskriftar krafist.</span><span class="sxs-lookup"><span data-stu-id="f5f63-140">Select or clear the Signature required check box.</span></span>
    * <span data-ttu-id="f5f63-141">Endurtakið þessi skref fyrir hvert ferli sem þarfnast rafrænna undirskrifta.</span><span class="sxs-lookup"><span data-stu-id="f5f63-141">Repeat these steps for each process that requires electronic signatures.</span></span>  
4. <span data-ttu-id="f5f63-142">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f5f63-142">Click Save.</span></span>

## <a name="create-a-custom-requirement-for-electronic-signatures"></a><span data-ttu-id="f5f63-143">Stofna sérstilltar kröfur fyrir rafrænar undirskriftir</span><span class="sxs-lookup"><span data-stu-id="f5f63-143">Create a custom requirement for electronic signatures</span></span>
1. <span data-ttu-id="f5f63-144">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f5f63-144">Click New.</span></span>
2. <span data-ttu-id="f5f63-145">Veldu eða hreinsaðu gátreitinn Undirskriftar krafist.</span><span class="sxs-lookup"><span data-stu-id="f5f63-145">Select or clear the Signature required check box.</span></span>
3. <span data-ttu-id="f5f63-146">Í reitnum Heiti skal færa inn heiti fyrir ferli sem þarfnast rafrænna undirskrifta.</span><span class="sxs-lookup"><span data-stu-id="f5f63-146">In the Name field, enter a name for the process that requires electronic signatures.</span></span>
4. <span data-ttu-id="f5f63-147">Í reitnum Heiti töflu skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f5f63-147">In the Table name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f5f63-148">Í listanum skal finna og velja þá töflu þar sem gögnin sem verður að undirrita eru geymd.</span><span class="sxs-lookup"><span data-stu-id="f5f63-148">In the list, find and select the table where the data that must be signed is stored.</span></span>
6. <span data-ttu-id="f5f63-149">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f5f63-149">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f5f63-150">Í reitnum Heiti reits skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f5f63-150">In the Field name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="f5f63-151">Í reitnum skal finna og velja töflu sem á að bæta fylgjast með.</span><span class="sxs-lookup"><span data-stu-id="f5f63-151">In the list, find and select the field in the table that you want to monitor.</span></span>
9. <span data-ttu-id="f5f63-152">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f5f63-152">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f5f63-153">Tilgreindu hvenær undirskrift er nauðsynleg.</span><span class="sxs-lookup"><span data-stu-id="f5f63-153">Specify when a signature is required.</span></span>     <span data-ttu-id="f5f63-154">Velja Alltaf ef undirskriftar er krafist þegar gögn í reitnum breytast.</span><span class="sxs-lookup"><span data-stu-id="f5f63-154">Select Always if a signature is required when the data in the field changes.</span></span>     <span data-ttu-id="f5f63-155">Velja Aðeins ef undirskriftar er krafist við ákveðin skilyrði.</span><span class="sxs-lookup"><span data-stu-id="f5f63-155">Select Only if a signature is required only under certain conditions.</span></span> <span data-ttu-id="f5f63-156">Ef Aðeins, verður einnig að velja einn af eftirfarandi valkostum: Þegar færsla er færð inn, Þegar færsla er uppfærð eða þegar færslu er eytt.</span><span class="sxs-lookup"><span data-stu-id="f5f63-156">If you select Only, you must also select one of the following options: When a record is inserted, When a record is updated, or When a record is deleted.</span></span>  
10. <span data-ttu-id="f5f63-157">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f5f63-157">Click Save.</span></span>
11. <span data-ttu-id="f5f63-158">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f5f63-158">Close the page.</span></span>
