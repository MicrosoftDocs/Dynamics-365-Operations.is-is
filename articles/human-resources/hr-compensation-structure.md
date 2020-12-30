---
title: Þróa launaskipulag
description: Þessi grein fer í gegnum ferlið við stofnun fyrirkomulags fastra launa og skráningu starfsmanna í launafyrirkomulagið með hæfnisreglum.
author: andreabichsel
manager: AnnBe
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 124d0f7f83feebabf622f00732c25bfa0f6eccdd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419052"
---
# <a name="develop-a-compensation-structure"></a><span data-ttu-id="a7932-103">Þróa launaskipulag</span><span class="sxs-lookup"><span data-stu-id="a7932-103">Develop a compensation structure</span></span>

<span data-ttu-id="a7932-104">Þessi grein fer í gegnum ferlið við stofnun fyrirkomulags fastra launa og skráningu starfsmanna í launafyrirkomulagið með hæfnisreglum.</span><span class="sxs-lookup"><span data-stu-id="a7932-104">This article walks you through creating a fixed compensation plan and enrolling employees in the plan through eligibility rules.</span></span> <span data-ttu-id="a7932-105">Þessi grein notar USMF kynningargögn og gildir um launa- og fríðindastjórnendur.</span><span class="sxs-lookup"><span data-stu-id="a7932-105">This article uses the USMF demo data and applies to Compensation and Benefits Managers.</span></span>

## <a name="create-a-fixed-compensation-plan"></a><span data-ttu-id="a7932-106">Setja upp fasta launaáætlun</span><span class="sxs-lookup"><span data-stu-id="a7932-106">Create a fixed compensation plan</span></span>

1. <span data-ttu-id="a7932-107">Veldu **Launastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="a7932-107">Select **Compensation management**.</span></span>

2. <span data-ttu-id="a7932-108">Veldu **Launafyrirkomulag fastra launa**.</span><span class="sxs-lookup"><span data-stu-id="a7932-108">Select **Fixed compensation plans**.</span></span>

3. <span data-ttu-id="a7932-109">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="a7932-109">Select **New**.</span></span>

4. <span data-ttu-id="a7932-110">Í reitinn **Fyrirkomulag** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a7932-110">In the **Plan** field, enter a value.</span></span>

5. <span data-ttu-id="a7932-111">Sláið inn gildi í reitnum **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="a7932-111">In the **Description** field, enter a value.</span></span>

6. <span data-ttu-id="a7932-112">Í reitnum **Gildisdagsetning** skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="a7932-112">In the **Effective date** field, enter a date.</span></span>

7. <span data-ttu-id="a7932-113">Í reitnum **Gerð** velurðu hvort launafyrirkomulag Fastra launa er **Brautar**, **Stiga** eða **Þrepa** áætlun.</span><span class="sxs-lookup"><span data-stu-id="a7932-113">In the **Type** field, select whether the fixed compensation plan is a **Band**, **Grade**, or **Step** plan.</span></span>

8. <span data-ttu-id="a7932-114">Gátreiturinn **Ráðleggingar leyfðar** virkar sem sjálfgildi fyrir allar aðgerðir sem er bætt við þessa áætlun í vinnslutilviki.</span><span class="sxs-lookup"><span data-stu-id="a7932-114">The **Recommendation allowed** checkbox acts as a default value for any actions added to this plan in a Process event.</span></span> <span data-ttu-id="a7932-115">Með því að heimila ráðleggingar gerir það kleift að hnekkja reiknaðri viðmiðunarupphæð við vinnslu launa.</span><span class="sxs-lookup"><span data-stu-id="a7932-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>

9. <span data-ttu-id="a7932-116">Reiturinn **Vikmörk utan marka** gerir kleift að tilgreina hvernig eigi að meðhöndla upphæðir launa sem falla utan sviðs tilgreinda launafyrirkomulagsins fyrir tiltekið stig.</span><span class="sxs-lookup"><span data-stu-id="a7932-116">The **Out of range tolerance** field allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span> <span data-ttu-id="a7932-117">Ef reiturinn **Vikmörk utan marka** er stilltur á **Ekkert** gerir þér kleift að nota hvaða launaupphæð sem er.</span><span class="sxs-lookup"><span data-stu-id="a7932-117">Setting the **Out of range tolerance** field to **None** allows you to use any compensation amount.</span></span> <span data-ttu-id="a7932-118">**Óbundin vikmörk** vara notendur við ef launaupphæðin er lægri en lágmarkið eða hærri en hámark tilvísunartímapunkts fyrir það stig.</span><span class="sxs-lookup"><span data-stu-id="a7932-118">**Soft tolerance** warns users if the compensation amount is less than the minimum or greater than the maximum reference point amounts for that level.</span></span> <span data-ttu-id="a7932-119">Notendur geta hunsað viðvörunina og haldið áfram.</span><span class="sxs-lookup"><span data-stu-id="a7932-119">Users can ignore the warning and continue.</span></span> <span data-ttu-id="a7932-120">**Bundin vikmörk** mynda villu ef laun starfsmanns eru stillt utan lágmarks og hámarks tilvísunarpunkta fyrir það stig og leiðréttir sjálfkrafa launum starfsmanns til að falla innan sviðsins.</span><span class="sxs-lookup"><span data-stu-id="a7932-120">**Hard tolerance** generates an error if an employee's compensation is outside the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>

10. <span data-ttu-id="a7932-121">Reiturinn **Ráðningarregla** reiknar laun starfsmanns í vinnslutilviki.</span><span class="sxs-lookup"><span data-stu-id="a7932-121">The **Hire rule** field calculates an employee's compensation during a process event.</span></span> <span data-ttu-id="a7932-122">**Ráðningarreglan** **Prósenta** reiknar hækkun sem er í hlutfalli við lengd þess tíma sem starfsmaður hefur verið í starfi í ferlinu.</span><span class="sxs-lookup"><span data-stu-id="a7932-122">A **Hire rule** of **Percent** calculates an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>

11. <span data-ttu-id="a7932-123">Í reitinn **Gjaldmiðill** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a7932-123">In the **Currency** field, type a value.</span></span>

12. <span data-ttu-id="a7932-124">Í reitnum **Umreikningur launataxta** slærðu inn eða velur gildi.</span><span class="sxs-lookup"><span data-stu-id="a7932-124">In the **Pay rate conversion** field, enter or select a value.</span></span>

13. <span data-ttu-id="a7932-125">Útvíkkaðu hlutann **Fylki nýtingar launabils**.</span><span class="sxs-lookup"><span data-stu-id="a7932-125">Expand the **Range utilization matrix** section.</span></span> <span data-ttu-id="a7932-126">Einnig er hægt að bæta við notkunarmörkum sviða til að koma starfsmenn fyrr til þeirra miðpunktur og hægja á því að þeir nái hámarki síns sviðs.</span><span class="sxs-lookup"><span data-stu-id="a7932-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>

14. <span data-ttu-id="a7932-127">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a7932-127">Select **Save**.</span></span> <span data-ttu-id="a7932-128">Þetta virkjar hnappinn **Setja upp laun** og heldur áfram að skilgreina launaskipan fyrir áætlunina.</span><span class="sxs-lookup"><span data-stu-id="a7932-128">This enables the **Set up compensation** button and continue defining your compensation structure for the plan.</span></span>

15. <span data-ttu-id="a7932-129">Veldu **Setja upp laun**.</span><span class="sxs-lookup"><span data-stu-id="a7932-129">Select **Set up compensation**.</span></span> <span data-ttu-id="a7932-130">Þú getur búið til launafyrirkomulag með því að nota eina af þessum þremur aðferðum:</span><span class="sxs-lookup"><span data-stu-id="a7932-130">You can create a compensation structure by using one of these three methods:</span></span>

    - <span data-ttu-id="a7932-131">Stofna alveg nýtt fyrirkomulag með því að velja safn tilvísunarpunkta og bæta stig við stigum til að stofna þitt eigið skipulag.</span><span class="sxs-lookup"><span data-stu-id="a7932-131">Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span>
    - <span data-ttu-id="a7932-132">Afrita launafyrirkomulag úr fyrirliggjandi áætlun sem upphafspunkt og breyta því fyrir nýja áætlun.</span><span class="sxs-lookup"><span data-stu-id="a7932-132">Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span>
    - <span data-ttu-id="a7932-133">Velja fyrirliggjandi launanet.</span><span class="sxs-lookup"><span data-stu-id="a7932-133">Select an existing compensation grid.</span></span> <span data-ttu-id="a7932-134">Ef önnur áætlun er þegar að nota launanetið endurspeglar hin áætlunin einnig allar breytingar sem eru gerðar á netinu.</span><span class="sxs-lookup"><span data-stu-id="a7932-134">If another plan already uses the compensation grid, the other plan also reflects any changes you make to the grid.</span></span>

16. <span data-ttu-id="a7932-135">Veldu **Stofna nýtt út frá fyrirliggjandi launafylki**.</span><span class="sxs-lookup"><span data-stu-id="a7932-135">Select **Create new from existing compensation matrix**.</span></span>

17. <span data-ttu-id="a7932-136">Í reitinn **Afrita frá hnitaneti** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="a7932-136">In the **Copy from grid** field, enter or select a value.</span></span> <span data-ttu-id="a7932-137">Einnig er hægt að breyta heiti nýs launanets sem þú stofnar með því að afrita valið net.</span><span class="sxs-lookup"><span data-stu-id="a7932-137">Optionally, you can change the name of the new compensation grid that you create by copying the selected grid.</span></span>

18. <span data-ttu-id="a7932-138">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a7932-138">Select **OK**.</span></span>

19. <span data-ttu-id="a7932-139">Veldu **Fjöldabreyting**.</span><span class="sxs-lookup"><span data-stu-id="a7932-139">Select **Mass change**.</span></span> <span data-ttu-id="a7932-140">**Fjöldabreyting** gerir kleift að vinna með upphæðir launafylkis með því að nota prósenta eða flata upphæð fyrir aukningu á eitt eða fleiri stig eða tilvísunarpunkta.</span><span class="sxs-lookup"><span data-stu-id="a7932-140">**Mass change** allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels or reference points.</span></span>

20. <span data-ttu-id="a7932-141">Í reitinn **Leiðréttingarupphæð** skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="a7932-141">In the **Adjustment amount** field, enter a number.</span></span>

21. <span data-ttu-id="a7932-142">Merkið eða afmerkið allar línur í listanum.</span><span class="sxs-lookup"><span data-stu-id="a7932-142">In the list, mark or unmark all rows.</span></span>

22. <span data-ttu-id="a7932-143">Smellt er á **Nota á hnitanet**.</span><span class="sxs-lookup"><span data-stu-id="a7932-143">Click **Apply to grid**.</span></span>

23. <span data-ttu-id="a7932-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a7932-144">Close the page.</span></span> <span data-ttu-id="a7932-145">Eftir að launafyrirkomulag hefur verið stofnað eða valið, er hægt að velja hvaða tilvísunarpunkta á að nota sem stýripunkt fyrir fast launafyrirkomulag.</span><span class="sxs-lookup"><span data-stu-id="a7932-145">After you create the compensation structure, you can select which of the reference points to use as the control point for the fixed compensation plan.</span></span> <span data-ttu-id="a7932-146">Stýripunkturinn er notuð til að reikna út uppbótarhlutfall starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="a7932-146">The control point is used to calculate an employee's Compa Ratio.</span></span>

24. <span data-ttu-id="a7932-147">Sláið inn eða veldu gildi í reitnum **Stýripunktur**.</span><span class="sxs-lookup"><span data-stu-id="a7932-147">In the **Control point** field, enter or select a value.</span></span>

25. <span data-ttu-id="a7932-148">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a7932-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a><span data-ttu-id="a7932-149">Stofna hæfnisreglur fyrir fast launafyrirkomulag</span><span class="sxs-lookup"><span data-stu-id="a7932-149">Create an eligibility rule for the fixed compensation plan</span></span>

<span data-ttu-id="a7932-150">Ekki er hægt að úthluta föstu launafyrirkomulagi til starfsmanns fyrr en hæfnisreglur eru skilgreindar fyrir áætlunina.</span><span class="sxs-lookup"><span data-stu-id="a7932-150">You can't assign a fixed compensation plan to an employee until you define eligibility rules for the plan.</span></span>  

1. <span data-ttu-id="a7932-151">Veldu **Hæfnisreglur**.</span><span class="sxs-lookup"><span data-stu-id="a7932-151">Select **Eligibility rules**.</span></span>

2. <span data-ttu-id="a7932-152">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="a7932-152">Select **New**.</span></span>

3. <span data-ttu-id="a7932-153">Í reitnum **Hæfnisreglur** slærðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a7932-153">In the **Eligibility** field, enter a value.</span></span>

4. <span data-ttu-id="a7932-154">Sláið inn gildi í reitnum **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="a7932-154">In the **Description** field, enter a value.</span></span>

5. <span data-ttu-id="a7932-155">Í reitnum **Gildisdagsetning** skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="a7932-155">In the **Effective date** field, enter a date.</span></span> <span data-ttu-id="a7932-156">Bæði föst og breytileg launafyrirkomulög nota hæfnisreglur.</span><span class="sxs-lookup"><span data-stu-id="a7932-156">Both fixed and variable compensation plans use eligibility rules.</span></span> <span data-ttu-id="a7932-157">Í reitnum **Gerð** velurðu gerð áætlunar.</span><span class="sxs-lookup"><span data-stu-id="a7932-157">In the **Type** field, select the type of plan.</span></span>

6. <span data-ttu-id="a7932-158">Í reitinn **Áætlun** slærðu inn eða velur gildi.</span><span class="sxs-lookup"><span data-stu-id="a7932-158">In the **Plan** field, enter or select a value.</span></span> <span data-ttu-id="a7932-159">Veljið skilyrði sem starfsmanns verður að uppfylla til að vera hæfur fyrir launafyrirkomulagið.</span><span class="sxs-lookup"><span data-stu-id="a7932-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="a7932-160">Viðmið geta verið:</span><span class="sxs-lookup"><span data-stu-id="a7932-160">Criteria can include:</span></span>

    - <span data-ttu-id="a7932-161">**Deild**</span><span class="sxs-lookup"><span data-stu-id="a7932-161">**Department**</span></span>
    - <span data-ttu-id="a7932-162">**Verkalýðsfélag**</span><span class="sxs-lookup"><span data-stu-id="a7932-162">**Labor union**</span></span>
    - <span data-ttu-id="a7932-163">**Staðsetning** (**Launasvæði**)</span><span class="sxs-lookup"><span data-stu-id="a7932-163">**Location** (**Compensation region**)</span></span>
    - <span data-ttu-id="a7932-164">**Vinnsla**</span><span class="sxs-lookup"><span data-stu-id="a7932-164">**Job**</span></span>
    - <span data-ttu-id="a7932-165">**Aðgerð**</span><span class="sxs-lookup"><span data-stu-id="a7932-165">**Function**</span></span>
    - <span data-ttu-id="a7932-166">**Vinnslugerð**</span><span class="sxs-lookup"><span data-stu-id="a7932-166">**Job type**</span></span>
    - <span data-ttu-id="a7932-167">**Launastig**</span><span class="sxs-lookup"><span data-stu-id="a7932-167">**Compensation level**</span></span>
    
    <span data-ttu-id="a7932-168">Starfsmaðurinn verður að uppfylla öll tilgreind skilyrði til að teljast hæfur fyrir launafyrirkomulagið.</span><span class="sxs-lookup"><span data-stu-id="a7932-168">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="a7932-169">Ef þú skilgreinir engin skilyrði koma allir starfsmenn til greina fyrir launafyrirkomulagið.</span><span class="sxs-lookup"><span data-stu-id="a7932-169">If you don't specify any criteria, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="a7932-170">Ef starfsmaður uppfyllir skilyrði sem tilgreind er í hæfnisreglu eða hæfnisregla hefur ekki verið tilgreind fyrir launafyrirkomulag, mun launafyrirkomulagið ekki birtast í leitarniðurstöðum við stofnun fastrar launaskráar fyrir starfsmann.</span><span class="sxs-lookup"><span data-stu-id="a7932-170">If an employee doesn't meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan won't appear in the lookup when you create a fixed compensation record for an employee.</span></span>

7. <span data-ttu-id="a7932-171">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a7932-171">Close the page.</span></span>

8. <span data-ttu-id="a7932-172">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a7932-172">Close the page.</span></span>

