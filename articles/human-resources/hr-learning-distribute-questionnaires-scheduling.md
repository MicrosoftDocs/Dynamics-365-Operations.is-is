---
title: Dreifa spurningalistum með áætlanagerð
description: Röðun spurningalista er hægt að nota til að áætla og dreifa spurningalistum á marga svarendur.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0448a7ebe802a961c8c1296ef57d12ea22e4ec27
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009435"
---
# <a name="distribute-questionnaires-using-scheduling"></a><span data-ttu-id="e32db-103">Dreifa spurningalistum með áætlanagerð</span><span class="sxs-lookup"><span data-stu-id="e32db-103">Distribute questionnaires using scheduling</span></span>

<span data-ttu-id="e32db-104">Röðun spurningalista er hægt að nota til að áætla og dreifa spurningalistum á marga svarendur.</span><span class="sxs-lookup"><span data-stu-id="e32db-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="e32db-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="e32db-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="e32db-106">Stofna áætlun spurningalista</span><span class="sxs-lookup"><span data-stu-id="e32db-106">Create a questionnaire schedule</span></span>

1. <span data-ttu-id="e32db-107">Fara í Spurningalista > Dreifa > Áætlanir Spurningalista.</span><span class="sxs-lookup"><span data-stu-id="e32db-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>

2. <span data-ttu-id="e32db-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e32db-108">Click New.</span></span>

3. <span data-ttu-id="e32db-109">Í reitinn Áætlun skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e32db-109">In the Scheduling field, type a value.</span></span>

4. <span data-ttu-id="e32db-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="e32db-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="e32db-111">Stilla áætlun á Nafnlaus ef það á að skrá svörin án þess að tengja þau nafni.</span><span class="sxs-lookup"><span data-stu-id="e32db-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="e32db-112">Leyfa nafnlausar niðurstöður verður fyrst að setja upp í færibreytum Mannauður.</span><span class="sxs-lookup"><span data-stu-id="e32db-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  

5. <span data-ttu-id="e32db-113">Í reitnum Tegund er gerð áætlunar valin.</span><span class="sxs-lookup"><span data-stu-id="e32db-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="e32db-114">Í þessu dæmi munum við nota Ánægju-gerð.</span><span class="sxs-lookup"><span data-stu-id="e32db-114">In this example we will use the Satisfaction type.</span></span>

6. <span data-ttu-id="e32db-115">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="e32db-115">In the list, find and select the desired record.</span></span>

7. <span data-ttu-id="e32db-116">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e32db-116">In the list, click the link in the selected row.</span></span>

8. <span data-ttu-id="e32db-117">Dagsetning er rituð í reitinn Dagetning.</span><span class="sxs-lookup"><span data-stu-id="e32db-117">In the Date field, enter a date.</span></span>

9. <span data-ttu-id="e32db-118">Stækka hlutann Tölvupóstur fyrir sjálfsafgreiðslu starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="e32db-118">Expand the Email for employee self service section.</span></span>

10. <span data-ttu-id="e32db-119">Í reitinn Efni skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e32db-119">In the Subject field, type a value.</span></span>

    * <span data-ttu-id="e32db-120">Dæmi: Tiltæka Spurningalista</span><span class="sxs-lookup"><span data-stu-id="e32db-120">Example: Questionnaire available</span></span>  

11. <span data-ttu-id="e32db-121">Meginmál tölvupóstskilaboða skal slá inn í svæðið Texti.</span><span class="sxs-lookup"><span data-stu-id="e32db-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="e32db-122">Athugið að hægt er að neyta breytuna til að skipta út gildum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="e32db-122">Note, the variable can be used to substitue values in the system.</span></span>

    * <span data-ttu-id="e32db-123">Dæmi: Kæri/kæra %P%, vinsamlegast skráðu þig inn í Sjálfsafgreiðsla Starfsmanns til að ljúka spurningalistanum heilbrigði Vinnuafls.</span><span class="sxs-lookup"><span data-stu-id="e32db-123">Example: Dear %P%, Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="e32db-124">Contoso</span><span class="sxs-lookup"><span data-stu-id="e32db-124">Contoso</span></span>  

12. <span data-ttu-id="e32db-125">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e32db-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="e32db-126">Nota upplýsingar um Uppsetningu til að velja spurningalista sem á að svara auk hvaða fyrirspurnir á að nota til að velja svarendur.</span><span class="sxs-lookup"><span data-stu-id="e32db-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>

1. <span data-ttu-id="e32db-127">Smellið á Upplýsingar um uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="e32db-127">Click Setup details.</span></span>

2. <span data-ttu-id="e32db-128">Í listanum skal finna spurningalista til að nota til að finna svarendur fyrir spurningalistann.</span><span class="sxs-lookup"><span data-stu-id="e32db-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>

    * <span data-ttu-id="e32db-129">Dæmi: Starfsmenn</span><span class="sxs-lookup"><span data-stu-id="e32db-129">Example: Workers</span></span>  

3. <span data-ttu-id="e32db-130">Smellið á Skoða eða breyta fyrirspurn til að velja ákveðna einstaklinga eða lagfæra fyrirspurnina til að finna einstaklinga sem passa við sérstök skilyrði.</span><span class="sxs-lookup"><span data-stu-id="e32db-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>

    * <span data-ttu-id="e32db-131">Athugið að allir svarendur verður einnig að vera notendur kerfisins.</span><span class="sxs-lookup"><span data-stu-id="e32db-131">Note that all respondents must also be users in the system.</span></span>  

4. <span data-ttu-id="e32db-132">Í listanum skal merkja línu fyrir einstakling</span><span class="sxs-lookup"><span data-stu-id="e32db-132">In the list, mark the row for Person</span></span>

5. <span data-ttu-id="e32db-133">Í reitinn Skilyrði skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="e32db-133">In the Criteria field, enter or select a value.</span></span>

    * <span data-ttu-id="e32db-134">Velja Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="e32db-134">Select Julia Funderburk</span></span>  

6. <span data-ttu-id="e32db-135">Veldu Julia Funderburk í listanum.</span><span class="sxs-lookup"><span data-stu-id="e32db-135">In the list, select Julia Funderburk</span></span>

7. <span data-ttu-id="e32db-136">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e32db-136">Click OK.</span></span>

8. <span data-ttu-id="e32db-137">Smellið á flipann Spurningalisti.</span><span class="sxs-lookup"><span data-stu-id="e32db-137">Click the Questionnaires tab.</span></span>

9. <span data-ttu-id="e32db-138">Í trénu, útvíkkið hnútinn fyrir gerð spurningalista af gerðini ánægjukönnun.</span><span class="sxs-lookup"><span data-stu-id="e32db-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>

10. <span data-ttu-id="e32db-139">Í trénu skal mekja við "heilbrigðisskoðun vinnuafls".</span><span class="sxs-lookup"><span data-stu-id="e32db-139">In the tree, check 'Workforce Health Assessment'.</span></span>

11. <span data-ttu-id="e32db-140">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e32db-140">Click OK.</span></span>

12. <span data-ttu-id="e32db-141">Smellið á Áætluð svarseta.</span><span class="sxs-lookup"><span data-stu-id="e32db-141">Click Planned answer session.</span></span>

    * <span data-ttu-id="e32db-142">Athugið að Áætlaðar svarsetur hafa verið stofnaðar fyrir hvern notanda sem hefur verið valinn eða fengið fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="e32db-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  

13. <span data-ttu-id="e32db-143">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e32db-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="e32db-144">Hefja áætlun spurningalista til að gera spurningalista tiltæka fyrir svarendur til að ljúka.</span><span class="sxs-lookup"><span data-stu-id="e32db-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>

1. <span data-ttu-id="e32db-145">Smellið á Aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="e32db-145">Click Functions.</span></span>

2. <span data-ttu-id="e32db-146">Smellið á „Byrja“.</span><span class="sxs-lookup"><span data-stu-id="e32db-146">Click Start.</span></span>

3. <span data-ttu-id="e32db-147">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e32db-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="e32db-148">Senda tölvupóst til að tilkynna svarendum um tiltæka spurningalista.</span><span class="sxs-lookup"><span data-stu-id="e32db-148">Send the email to inform respondents of the available questionnaire.</span></span>

1. <span data-ttu-id="e32db-149">Smellið á Aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="e32db-149">Click Functions.</span></span>

2. <span data-ttu-id="e32db-150">Smellið á Senda tölvupóst.</span><span class="sxs-lookup"><span data-stu-id="e32db-150">Click Send email.</span></span>

3. <span data-ttu-id="e32db-151">Smellið á Hætta við.</span><span class="sxs-lookup"><span data-stu-id="e32db-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="e32db-152">Notið Áætlaðar svarsetur til að fylgjast með hver þarf að ljúka spurningalistanum.</span><span class="sxs-lookup"><span data-stu-id="e32db-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>

1. <span data-ttu-id="e32db-153">Smellið á Áætluð svarseta.</span><span class="sxs-lookup"><span data-stu-id="e32db-153">Click Planned answer session.</span></span>

    * <span data-ttu-id="e32db-154">Eyðið öllum eftirstandandi áætluðum svarsetum þegar er verið að ljúka áætlaðri svarsetu.</span><span class="sxs-lookup"><span data-stu-id="e32db-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  

2. <span data-ttu-id="e32db-155">Smellið á Eyða.</span><span class="sxs-lookup"><span data-stu-id="e32db-155">Click Delete.</span></span>

3. <span data-ttu-id="e32db-156">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="e32db-156">Click Yes.</span></span>

4. <span data-ttu-id="e32db-157">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e32db-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="e32db-158">Þegar tekið hefur verið á móti öllum svörunum er hægt að ljúka áætlun og/eða þegar búið er að eyða öllum eftirstandandi svarsetum.</span><span class="sxs-lookup"><span data-stu-id="e32db-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>

1. <span data-ttu-id="e32db-159">Smellið á Aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="e32db-159">Click Functions.</span></span>
2. <span data-ttu-id="e32db-160">Smellt er á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="e32db-160">Click End.</span></span>
3. <span data-ttu-id="e32db-161">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e32db-161">Click OK.</span></span>
