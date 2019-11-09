---
title: Þróa uppbyggingu launa og launafyrirkomulag
description: Þessi leiðarvísir fyrir verk fer í gegnum ferlið við stofnun launafyrirkomulags fastra launa og virkjun starfsmönnum að vera skráðir í launafyrirkomulag með hæfnisreglum.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3f0732736736fdc87f3367f24b1d20b9fa6efc59
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178389"
---
# <a name="develop-salarycompensation-structure-and-plan"></a><span data-ttu-id="7ea47-103">Þróa uppbyggingu launa og launafyrirkomulag</span><span class="sxs-lookup"><span data-stu-id="7ea47-103">Develop salary/compensation structure and plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7ea47-104">Þessi leiðarvísir fyrir verk fer í gegnum ferlið við stofnun launafyrirkomulags fastra launa og virkjun starfsmönnum að vera skráðir í launafyrirkomulag með hæfnisreglum.</span><span class="sxs-lookup"><span data-stu-id="7ea47-104">This task guide walks though the process of creating a Fixed compensation plan and enabling employees to be enrolled in the plan through eligibility rules.</span></span> <span data-ttu-id="7ea47-105">Sýnigagnafyrirtækisins til að stofna verkið er USMF og verkið er ætluð fyrir Launa- og Fríðindastjórnendur.</span><span class="sxs-lookup"><span data-stu-id="7ea47-105">The demo data company used to create this task is USMF and the task is intended for Compensation and Benefits Managers.</span></span>


## <a name="create-fixed-compensation-plan"></a><span data-ttu-id="7ea47-106">Stofna launafyrirkomulag fastra launa</span><span class="sxs-lookup"><span data-stu-id="7ea47-106">Create fixed compensation plan</span></span>
1. <span data-ttu-id="7ea47-107">Smellt er á Launastjórnun.</span><span class="sxs-lookup"><span data-stu-id="7ea47-107">Click Compensation management.</span></span>
2. <span data-ttu-id="7ea47-108">Smellt er á launafyrirkomulag fastra launa.</span><span class="sxs-lookup"><span data-stu-id="7ea47-108">Click Fixed compensation plans.</span></span>
3. <span data-ttu-id="7ea47-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7ea47-109">Click New.</span></span>
4. <span data-ttu-id="7ea47-110">Í reitinn Áætlun skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7ea47-110">In the Plan field, type a value.</span></span>
5. <span data-ttu-id="7ea47-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="7ea47-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="7ea47-112">Í reitnum Gildisdagsetning skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="7ea47-112">In the Effective date field, enter a date.</span></span>
7. <span data-ttu-id="7ea47-113">Í svæðinu, veljið hvort launafyrirkomulag Fastra launa er Brautar, Stiga eða Þrepa áætlun.</span><span class="sxs-lookup"><span data-stu-id="7ea47-113">In the Type field, select whether the Fixed compensation plan is a Band, Grade, or Step plan.</span></span>
8. <span data-ttu-id="7ea47-114">Gátreiturinn Ráðleggingar leyfðar virkar sem sjálfgildi fyrir allar aðgerðir sem er bætt við þessa áætlun í vinnslutilviki.</span><span class="sxs-lookup"><span data-stu-id="7ea47-114">The Recommendation allowed checkbox acts as a default value for any actions added to this plan in a Process event.</span></span>  <span data-ttu-id="7ea47-115">Með því að heimila ráðleggingar gerir það kleift að hnekkja reiknaðri viðmiðunarupphæð við vinnslu launa.</span><span class="sxs-lookup"><span data-stu-id="7ea47-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>
9. <span data-ttu-id="7ea47-116">Utan marka vikmörk gerir kleift að tilgreina hvernig eigi að meðhöndla upphæðir launa sem falla utan sviðs tilgreinda launafyrirkomulagsins fyrir tiltekið stig.</span><span class="sxs-lookup"><span data-stu-id="7ea47-116">The Out of range tolerance allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span>  <span data-ttu-id="7ea47-117">Ef Vikmörk Utan marka er Ekkert, eru allar upphæðir launa sem á að nota leyfðar.</span><span class="sxs-lookup"><span data-stu-id="7ea47-117">An Out of range tolerance of None will allow any compensation amount to be used.</span></span>  <span data-ttu-id="7ea47-118">Óbundnar vikmörk varar notandann við ef launaupphæðin er minna en lágmarks lágmarksupphæð tilvísunartímapunkts fyrir það stig, eða hærri en hámarksupphæð fyrir það stig.</span><span class="sxs-lookup"><span data-stu-id="7ea47-118">A Soft tolerance will warn the user if the compensation amount is less than the minimum reference point amount for that level, or greater than the maximum amount for that level.</span></span> <span data-ttu-id="7ea47-119">Notandinn getur hunsað viðvörunina og haldið áfram.</span><span class="sxs-lookup"><span data-stu-id="7ea47-119">The user can ignore the warning and continue.</span></span>  <span data-ttu-id="7ea47-120">Bundnar vikmörk mynda villa ef laun starfsmanns eru stillt utan lágmarks og hámarks tilvísunarpunkta fyrir það stig og leiðréttir sjálfkrafa launum starfsmanns til að falla innan sviðsins.</span><span class="sxs-lookup"><span data-stu-id="7ea47-120">A Hard tolerance will generate an error if an employee's compensation is set outside of the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>
10. <span data-ttu-id="7ea47-121">svæðið Ráðningarregla er notað þegar launavinnslutilvik er keyrt til að reikna út laun starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="7ea47-121">The Hire rule field is used when a compensation Process event is run to calculate an employee's compensation.</span></span>  <span data-ttu-id="7ea47-122">Ráðningarreglu með prósentum reiknar hækkun sem er í hlutfalli við lengd þess tíma sem starfsmaður hefur verið í starfi í ferlinu.</span><span class="sxs-lookup"><span data-stu-id="7ea47-122">A Hire rule of Percent will calculate an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>
11. <span data-ttu-id="7ea47-123">Í reitinn Gjaldmiðill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7ea47-123">In the Currency field, type a value.</span></span>
12. <span data-ttu-id="7ea47-124">Sláðu inn eða veldu gildi í reitnum umreikningur launataxta.</span><span class="sxs-lookup"><span data-stu-id="7ea47-124">In the Pay rate conversion field, enter or select a value.</span></span>
13. <span data-ttu-id="7ea47-125">Útvíkka hlutann Nýtingarfylki sviðs.</span><span class="sxs-lookup"><span data-stu-id="7ea47-125">Expand the Range utilization matrix section.</span></span>
    * <span data-ttu-id="7ea47-126">Einnig er hægt að bæta við notkunarmörkum sviða til að koma starfsmenn fyrr til þeirra miðpunktur og hægja á því að þeir nái hámarki síns sviðs.</span><span class="sxs-lookup"><span data-stu-id="7ea47-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>  
14. <span data-ttu-id="7ea47-127">Á þessum tímapunkti, verður að vista launafyrirkomulag Fastra launa að virkja hnappinn Setja upp laun og halda áfram að skilgreina launaskipulag þitt fyrir áætlunina.</span><span class="sxs-lookup"><span data-stu-id="7ea47-127">At this point, you must save the Fixed compensation plan to enable the Set up compensation button and continue defining your compensation structure for the plan.</span></span>  <span data-ttu-id="7ea47-128">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="7ea47-128">Click Save.</span></span>
15. <span data-ttu-id="7ea47-129">Smellt er á Setja upp laun.</span><span class="sxs-lookup"><span data-stu-id="7ea47-129">Click Set up compensation.</span></span>
    * <span data-ttu-id="7ea47-130">Það eru þrjár leiðir til að stofna launaskipulag.</span><span class="sxs-lookup"><span data-stu-id="7ea47-130">There are three ways to create a compensation structure.</span></span> <span data-ttu-id="7ea47-131">1: stofna algerlega nýja skipulag með því að velja safn tilvísunarpunkta og bæta stig við stigum til að stofna þitt eigið skipulag.</span><span class="sxs-lookup"><span data-stu-id="7ea47-131">1: Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span> <span data-ttu-id="7ea47-132">2: afrita launaskipulag úr fyrirliggjandi áætlun sem upphafspunkt og breyta hann fyrir nýja áætlun.</span><span class="sxs-lookup"><span data-stu-id="7ea47-132">2: Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span> <span data-ttu-id="7ea47-133">3: Velja skal núverandi launanet.</span><span class="sxs-lookup"><span data-stu-id="7ea47-133">3: Select an existing compensation grid.</span></span> <span data-ttu-id="7ea47-134">Ef launanetinu er þegar í notkun fyrir aðra áætlun, munu breytingar á töflunni einnig endurspeglast í hinni áætlun.</span><span class="sxs-lookup"><span data-stu-id="7ea47-134">If the compensation grid is already being used by another plan, any changes made to the grid will also be reflected in the other plan.</span></span>  
16. <span data-ttu-id="7ea47-135">Velja Stofna nýtt út frá fyrirliggjandi launafylki valkostinn.</span><span class="sxs-lookup"><span data-stu-id="7ea47-135">Select the Create new from existing compensation matrix option.</span></span>
17. <span data-ttu-id="7ea47-136">Í reitinn afrita frá hnitaneti skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7ea47-136">In the Copy from grid field, enter or select a value.</span></span>
    * <span data-ttu-id="7ea47-137">Einnig er hægt að breyta heiti nýs launanets sem verður stofnað sem afrit af valda netinu.</span><span class="sxs-lookup"><span data-stu-id="7ea47-137">Optionally you can change the name of the new compensation grid that will be created as a copy of the selected grid.</span></span>  
18. <span data-ttu-id="7ea47-138">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="7ea47-138">Click OK.</span></span>
19. <span data-ttu-id="7ea47-139">Smellt er á Fjöldabreyting.</span><span class="sxs-lookup"><span data-stu-id="7ea47-139">Click Mass change.</span></span>
    * <span data-ttu-id="7ea47-140">Fjöldabreyting gerir kleift að vinna með upphæðir launafylkis með því að nota prósenta eða flata upphæð fyrir aukningu á eitt eða fleiri stig og/eða tilvísunarpunkta.</span><span class="sxs-lookup"><span data-stu-id="7ea47-140">Mass change allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels and/or reference points.</span></span>  
20. <span data-ttu-id="7ea47-141">Í reitinn Leiðréttingarupphæð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="7ea47-141">In the Adjustment amount field, enter a number.</span></span>
21. <span data-ttu-id="7ea47-142">Merkið eða afmerkið allar línur í listanum.</span><span class="sxs-lookup"><span data-stu-id="7ea47-142">In the list, mark or unmark all rows.</span></span>
22. <span data-ttu-id="7ea47-143">Smellt er á Nota á hnitanet.</span><span class="sxs-lookup"><span data-stu-id="7ea47-143">Click Apply to grid.</span></span>
23. <span data-ttu-id="7ea47-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7ea47-144">Close the page.</span></span>
    * <span data-ttu-id="7ea47-145">Þegar launaskipulag hefur verið stofnuð eða valin, er hægt að velja hvaða tilvísununarpunkta á að nota sem stýripunkt fyrir launafyrirkomulag Fastra launa.</span><span class="sxs-lookup"><span data-stu-id="7ea47-145">Once a compensation structure has been created or selected, you can select which of the reference points should be used as the Control point for the Fixed compensation plan.</span></span>  <span data-ttu-id="7ea47-146">Stýripunkturinn er notuð til að reikna út samanburðarhlutfall starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="7ea47-146">The Control point is used to calculate an employee's Compa Ratio.</span></span>  
24. <span data-ttu-id="7ea47-147">Sláið inn eða veldu gildi í reitnum stýripunktur.</span><span class="sxs-lookup"><span data-stu-id="7ea47-147">In the Control point field, enter or select a value.</span></span>
25. <span data-ttu-id="7ea47-148">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7ea47-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-new-fixed-compensation-plan"></a><span data-ttu-id="7ea47-149">Stofna hæfnisreglur fyrir nýtt launafyrirkomulag fastra launa</span><span class="sxs-lookup"><span data-stu-id="7ea47-149">Create an eligibility rule for the new Fixed compensation plan</span></span>
    * <span data-ttu-id="7ea47-150">Nýja launafyrirkomulag Fastra launa er ekki hægt að úthlutað til starfsmanns fyrr en hæfnisreglur hafa verið skilgreindar fyrir áætlunina.</span><span class="sxs-lookup"><span data-stu-id="7ea47-150">The new Fixed compensation plan cannot be assigned to an employee until Eligibility rules have been defined for the plan.</span></span>  
1. <span data-ttu-id="7ea47-151">Smellið á hæfnisreglur</span><span class="sxs-lookup"><span data-stu-id="7ea47-151">Click Eligibility rules.</span></span>
2. <span data-ttu-id="7ea47-152">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7ea47-152">Click New.</span></span>
3. <span data-ttu-id="7ea47-153">Í reitinn Hæfni skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7ea47-153">In the Eligibility field, type a value.</span></span>
4. <span data-ttu-id="7ea47-154">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="7ea47-154">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7ea47-155">Í reitnum Gildisdagsetning skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="7ea47-155">In the Effective date field, enter a date.</span></span>
    * <span data-ttu-id="7ea47-156">Hæfnisreglur eru notaðar fyrir bæði launafyrirkomulög með fastri og breytilegri uppbót.</span><span class="sxs-lookup"><span data-stu-id="7ea47-156">Eligibility rules are used for both Fixed and Variable compensation plans.</span></span>  <span data-ttu-id="7ea47-157">Í svæðinu gerð, veljið hvaða gerð áætlunar sem þetta safn hæfnisregla er fyrir.</span><span class="sxs-lookup"><span data-stu-id="7ea47-157">In the Type field, select which type of plan this set of eligibility rules is for.</span></span>  
6. <span data-ttu-id="7ea47-158">Í reitinn áætlun skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="7ea47-158">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="7ea47-159">Veljið skilyrði sem starfsmanns verður að uppfylla til að vera hæfur fyrir launafyrirkomulagið.</span><span class="sxs-lookup"><span data-stu-id="7ea47-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="7ea47-160">Skilyrði geta verið Deild, verkalýðsfélag, Staðsetningar (launasvæði), starfshlutverk, vinnslugerð, eða launastig.</span><span class="sxs-lookup"><span data-stu-id="7ea47-160">Criteria can include a Department, Labor union, Location (Compensation region), Job, Function, Job type, or Compensation level.</span></span> <span data-ttu-id="7ea47-161">Starfsmaðurinn verður að uppfylla öll tilgreind skilyrði til að teljast hæfur fyrir launafyrirkomulagið.</span><span class="sxs-lookup"><span data-stu-id="7ea47-161">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="7ea47-162">Ef engin skilyrði eru tilgreind eru allir starfsmenn sem koma til greina fyrir launafyrirkomulagið.</span><span class="sxs-lookup"><span data-stu-id="7ea47-162">If no criteria are specified, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="7ea47-163">Ef starfsmaður uppfyllir skilyrði sem tilgreind er í hæfnisreglu eða hæfnisregla hefur ekki verið tilgreind fyrir launafyrirkomulag, mun launafyrirkomulagið ekki birtast í leitarniðurstöðum þegar stofna á færsla Fastra launa fyrir starfsmann.</span><span class="sxs-lookup"><span data-stu-id="7ea47-163">If an employee does not meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan will not appear in the lookup when creating a Fixed compensation record for an employee.</span></span>  
7. <span data-ttu-id="7ea47-164">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7ea47-164">Close the page.</span></span>
8. <span data-ttu-id="7ea47-165">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7ea47-165">Close the page.</span></span>
