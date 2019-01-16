---
title: "Hugtök leyfis og fjarvista"
description: "Þetta efnisatriði lýsir hugtökum leyfis og fjarvista og hvernig stöður frítíma eru ákvarðaðar."
author: jcart
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: a388e0efe6c19a3aabe04e7fff039ce11ae023c4
ms.openlocfilehash: 563593d6c93b0488c681f5b43004f5c0d22cc004
ms.contentlocale: is-is
ms.lasthandoff: 01/07/2019

---

# <a name="leave-and-absence-concepts"></a><span data-ttu-id="98112-103">Hugtök leyfis og fjarvista</span><span class="sxs-lookup"><span data-stu-id="98112-103">Leave and absence concepts</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="98112-104">Hugtökum sem er lýst í þessu efnisatriði geta auðveldað þér að ákvarða hvernig starfsmanni er veittur frítími og hvernig tímastöður starfsmannsins eru reiknaðar út.</span><span class="sxs-lookup"><span data-stu-id="98112-104">The concepts and terms that are described in this topic can help you determine how an employee is awarded time off, and how that employee's time balances are calculated.</span></span> <span data-ttu-id="98112-105">Frekari upplýsingar um stjórnun leyfa og fjarvista er að finna í [Stjórnun leyfis og fjarvista](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span><span class="sxs-lookup"><span data-stu-id="98112-105">For more information about leave and absence management, see [Leave and absence management](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).</span></span>

## <a name="leave-plan-details"></a><span data-ttu-id="98112-106">Upplýsingar um leyfisáætlanir</span><span class="sxs-lookup"><span data-stu-id="98112-106">Leave plan details</span></span>

### <a name="start-date"></a><span data-ttu-id="98112-107">Upphafsdagur</span><span class="sxs-lookup"><span data-stu-id="98112-107">Start date</span></span>

<span data-ttu-id="98112-108">Upphafsdagsetningin er dagurinn þegar uppsöfnunarferli byrjar.</span><span class="sxs-lookup"><span data-stu-id="98112-108">The start date is the date when accrual processing begins.</span></span> <span data-ttu-id="98112-109">Upphafsdagurinn þjónar einnig sem árleg dagsetning sem er notuð til að reikna út yfirfærðar upphæðir.</span><span class="sxs-lookup"><span data-stu-id="98112-109">The start date also serves as the anniversary date that is used to calculate carry-forward amounts.</span></span>

## <a name="accruals"></a><span data-ttu-id="98112-110">Uppsafnanir</span><span class="sxs-lookup"><span data-stu-id="98112-110">Accruals</span></span>

<span data-ttu-id="98112-111">Uppsafnanir ákvarða hvenær og hversu oft starfsmanni er veittur frítími.</span><span class="sxs-lookup"><span data-stu-id="98112-111">Accruals determine when and how often an employee is awarded time off.</span></span> <span data-ttu-id="98112-112">Reglur um það hvenær eigi að úthluta uppsöfnunum og reglur um hlutfallsskipti eru skilgreind í hlutanum **Uppsafnanir** við uppsetningu á áætlun leyfis og fjarvista.</span><span class="sxs-lookup"><span data-stu-id="98112-112">Policies about when accruals should be awarded and policies about proration are defined in the **Accruals** section when setting up the leave and absence plan.</span></span>

### <a name="accrual-frequency"></a><span data-ttu-id="98112-113">Uppsöfnunartíðni</span><span class="sxs-lookup"><span data-stu-id="98112-113">Accrual frequency</span></span>

<span data-ttu-id="98112-114">Uppsöfnunartíðnin skilgreinir hversu oft leyfi er safnað upp eða úthlutað.</span><span class="sxs-lookup"><span data-stu-id="98112-114">The accrual frequency defines how often leave is accrued or awarded.</span></span> <span data-ttu-id="98112-115">Eftirtaldir valkostir eru í boði:</span><span class="sxs-lookup"><span data-stu-id="98112-115">The following options are available:</span></span>

- <span data-ttu-id="98112-116">Daglega</span><span class="sxs-lookup"><span data-stu-id="98112-116">Daily</span></span>
- <span data-ttu-id="98112-117">Vikulega</span><span class="sxs-lookup"><span data-stu-id="98112-117">Weekly</span></span>
- <span data-ttu-id="98112-118">Aðra hverja viku</span><span class="sxs-lookup"><span data-stu-id="98112-118">Biweekly</span></span>
- <span data-ttu-id="98112-119">Annan hvern mánuð</span><span class="sxs-lookup"><span data-stu-id="98112-119">Semimonthly</span></span>
- <span data-ttu-id="98112-120">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="98112-120">Monthly</span></span>
- <span data-ttu-id="98112-121">Ársfjórðungslega</span><span class="sxs-lookup"><span data-stu-id="98112-121">Quarterly</span></span>
- <span data-ttu-id="98112-122">Annað hvert ár</span><span class="sxs-lookup"><span data-stu-id="98112-122">Semiannually</span></span>
- <span data-ttu-id="98112-123">Árlega</span><span class="sxs-lookup"><span data-stu-id="98112-123">Annually</span></span>
- <span data-ttu-id="98112-124">Enginn</span><span class="sxs-lookup"><span data-stu-id="98112-124">None</span></span>

### <a name="accrual-period-basis"></a><span data-ttu-id="98112-125">Tímabilsgrunnur uppsöfnunar</span><span class="sxs-lookup"><span data-stu-id="98112-125">Accrual period basis</span></span>

<span data-ttu-id="98112-126">Tímabilsgrunnur uppsöfnunar ákvarðar dagsetninguna sem er notuð til að reikna út uppsöfnunartímabil.</span><span class="sxs-lookup"><span data-stu-id="98112-126">The accrual period basis determines the date that is used to calculate accrual periods.</span></span> <span data-ttu-id="98112-127">Eftirtaldir valkostir eru í boði:</span><span class="sxs-lookup"><span data-stu-id="98112-127">The following options are available:</span></span>

- <span data-ttu-id="98112-128">**Upphafsdagsetning áætlunar**</span><span class="sxs-lookup"><span data-stu-id="98112-128">**Plan start date**</span></span>
- <span data-ttu-id="98112-129">**Tiltekin dagsetning starfsmanns** - Þegar þessi valkostur er valinn ákvarðar gildið uppruna gildisins fyrir upphaflegu dagsetninguna sem er notuð til að reikna út uppsöfnunartímabil.</span><span class="sxs-lookup"><span data-stu-id="98112-129">**Employee specific date** – When this option is selected, the value determines the source of the initial date value that is used to calculate accrual periods.</span></span> <span data-ttu-id="98112-130">Eftirtaldir valkostir eru í boði:</span><span class="sxs-lookup"><span data-stu-id="98112-130">The following options are available:</span></span>

    - <span data-ttu-id="98112-131">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="98112-131">Custom</span></span>
    - <span data-ttu-id="98112-132">Árleg dagsetning</span><span class="sxs-lookup"><span data-stu-id="98112-132">Anniversary date</span></span>
    - <span data-ttu-id="98112-133">Upprunaleg ráðningardagsetning</span><span class="sxs-lookup"><span data-stu-id="98112-133">Original hire date</span></span>
    - <span data-ttu-id="98112-134">Starfsaldursdagsetning</span><span class="sxs-lookup"><span data-stu-id="98112-134">Seniority date</span></span>
    - <span data-ttu-id="98112-135">Breyttur fyrsti starfsdagur starfskrafts</span><span class="sxs-lookup"><span data-stu-id="98112-135">Worker's adjusted start date</span></span>
    - <span data-ttu-id="98112-136">Fyrsti starfsdagur starfskrafts</span><span class="sxs-lookup"><span data-stu-id="98112-136">Worker's start date</span></span>

### <a name="accrual-award-date"></a><span data-ttu-id="98112-137">Úthlutunardagsetning uppsöfunar</span><span class="sxs-lookup"><span data-stu-id="98112-137">Accrual award date</span></span>

<span data-ttu-id="98112-138">Úthlutunardagsetning uppsöfnunar ákvarðar hvenær starfsmanni er úthlutaður frítími.</span><span class="sxs-lookup"><span data-stu-id="98112-138">The accrual award date determines when an employee is awarded time off.</span></span> <span data-ttu-id="98112-139">Eftirtaldir valkostir eru í boði:</span><span class="sxs-lookup"><span data-stu-id="98112-139">The following options are available:</span></span>

- <span data-ttu-id="98112-140">**Lokadagsetning uppsöfnunartímabils** - Starfsmanni verður úthlutaður frítími á síðasta degi úthlutunartímabilsins.</span><span class="sxs-lookup"><span data-stu-id="98112-140">**Accrual period end date** – The employee will be awarded time off on the last day of the award period.</span></span>

    <span data-ttu-id="98112-141">Til að safna upp réttri upphæð verður uppsöfnunarferlið að fela í sér allt tímabilið.</span><span class="sxs-lookup"><span data-stu-id="98112-141">To accrue the correct amount, the accrual process must include the whole period.</span></span> <span data-ttu-id="98112-142">Til dæmis er uppsöfnunartímabilið frá 1. janúar til og með 31. janúar 2018.</span><span class="sxs-lookup"><span data-stu-id="98112-142">For example, the accrual period is January 1, 2018, through January 31, 2018.</span></span> <span data-ttu-id="98112-143">Í þessu tilfelli, svo janúar verði tekin með, verður uppsöfnunin að keyra fyrir 1. febrúar 2018.</span><span class="sxs-lookup"><span data-stu-id="98112-143">In this case, for January to be included, the accrual must be run for February 1, 2018.</span></span>

- <span data-ttu-id="98112-144">**Upphafsdagur uppsöfnunartímabils** - Starfsmanni verður úthlutaður frítími á fyrsta degi úthlutunartímabilsins.</span><span class="sxs-lookup"><span data-stu-id="98112-144">**Accrual period start date** – The employee will be awarded time off on the first day of the award period.</span></span>

### <a name="accrual-policy-on-enrollment"></a><span data-ttu-id="98112-145">Uppsöfnunarregla við skráningu</span><span class="sxs-lookup"><span data-stu-id="98112-145">Accrual policy on enrollment</span></span>

<span data-ttu-id="98112-146">Þessi uppsöfnunarregla fyrir skráningu skilgreinir hvernig uppsöfnun er reiknuð út þegar starfsmaður er skráður á miðju uppsöfnunartímabili.</span><span class="sxs-lookup"><span data-stu-id="98112-146">The accrual policy on enrollment defines how accrual is calculated when an employee is enrolled in the middle of an accrual period.</span></span> <span data-ttu-id="98112-147">Eftirtaldir valkostir eru í boði:</span><span class="sxs-lookup"><span data-stu-id="98112-147">The following options are available:</span></span>

- <span data-ttu-id="98112-148">**Hlutfallslega skipt** - Dagsetningabilið milli skráningardags og upphafsdags er notað til að ákvarða dagamuninn.</span><span class="sxs-lookup"><span data-stu-id="98112-148">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="98112-149">Þessi mismunur er notaður þegar unnið er úr uppsöfnunum.</span><span class="sxs-lookup"><span data-stu-id="98112-149">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="98112-150">**Full uppsöfnun** - Upphæð fullrar uppsöfnunar, sem byggist á laginu, er úthlutað við fyrstu úrvinnslu uppsöfnunar.</span><span class="sxs-lookup"><span data-stu-id="98112-150">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="98112-151">**Engin uppsöfnun** - Engri uppsöfnun er úthlutað fyrr en við næsta uppsöfnunartímabil.</span><span class="sxs-lookup"><span data-stu-id="98112-151">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

### <a name="accrual-policy-on-unenrollment"></a><span data-ttu-id="98112-152">Uppsöfnunarregla við afskráningu</span><span class="sxs-lookup"><span data-stu-id="98112-152">Accrual policy on unenrollment</span></span>

<span data-ttu-id="98112-153">Þessi uppsöfnunarregla fyrir afskráningu skilgreinir hvernig uppsöfnun er reiknuð út þegar starfsmaður er afskráður á miðju uppsöfnunartímabili.</span><span class="sxs-lookup"><span data-stu-id="98112-153">The accrual policy on unenrollment defines how accrual is calculated when an employee is unenrolled in the middle of an accrual period.</span></span> <span data-ttu-id="98112-154">Eftirtaldir valkostir eru í boði:</span><span class="sxs-lookup"><span data-stu-id="98112-154">The following options are available:</span></span>

- <span data-ttu-id="98112-155">**Hlutfallslega skipt** - Dagsetningabilið milli skráningardags og upphafsdags er notað til að ákvarða dagamuninn.</span><span class="sxs-lookup"><span data-stu-id="98112-155">**Prorated** – The date range between the enrollment date and the start date is used to determine the difference in days.</span></span> <span data-ttu-id="98112-156">Þessi mismunur er notaður þegar unnið er úr uppsöfnunum.</span><span class="sxs-lookup"><span data-stu-id="98112-156">That difference is applied when accruals are processed.</span></span>
- <span data-ttu-id="98112-157">**Full uppsöfnun** - Upphæð fullrar uppsöfnunar, sem byggist á laginu, er úthlutað við fyrstu úrvinnslu uppsöfnunar.</span><span class="sxs-lookup"><span data-stu-id="98112-157">**Full accrual** – The full accrual amount, based on the tier, is awarded during the first accrual processing.</span></span>
- <span data-ttu-id="98112-158">**Engin uppsöfnun** - Engri uppsöfnun er úthlutað fyrr en við næsta uppsöfnunartímabil.</span><span class="sxs-lookup"><span data-stu-id="98112-158">**No accrual** – No accrual is awarded until the next accrual period.</span></span>

## <a name="accrual-schedule"></a><span data-ttu-id="98112-159">Uppsöfnunaráætlun</span><span class="sxs-lookup"><span data-stu-id="98112-159">Accrual schedule</span></span>

<span data-ttu-id="98112-160">Uppsöfnunaráætlun ákvarðar hvernig starfsmaður safnar upp frítíma og hvaða upphæðum þessi starfsmaður safnar upp og yfirfærir.</span><span class="sxs-lookup"><span data-stu-id="98112-160">The accrual schedule determines how an employee will accrue time off, and what amounts that employee will accrue and carry forward.</span></span> <span data-ttu-id="98112-161">Hægt er að búa til lög þannig að frítíma sé úthlutað á grunni mismunandi stiga.</span><span class="sxs-lookup"><span data-stu-id="98112-161">Tiers can be created so that time off is awarded based on different levels.</span></span>

### <a name="months-of-service"></a><span data-ttu-id="98112-162">Starfsaldur í mánuðum</span><span class="sxs-lookup"><span data-stu-id="98112-162">Months of service</span></span>

<span data-ttu-id="98112-163">Gildið fyrir **Starfsaldur í mánuðum** skilgreinir lágmarksfjölda mánaða sem starfsmaður verður að vinna til að eiga rétt á uppsöfnunum.</span><span class="sxs-lookup"><span data-stu-id="98112-163">The **Months of service** value defines the minimum number of months that employees must work to be entitled to accruals.</span></span> <span data-ttu-id="98112-164">Ef ekki er þörf á lágmarki fyrir starfsmenn skal stilla gildið á **0**.</span><span class="sxs-lookup"><span data-stu-id="98112-164">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="hours-worked"></a><span data-ttu-id="98112-165">Unnar vinnustundir</span><span class="sxs-lookup"><span data-stu-id="98112-165">Hours worked</span></span>

<span data-ttu-id="98112-166">Gildið fyrir **Unnar vinnustundir** skilgreinir lágmarksfjölda vinnustunda sem starfsmaður verður að vinna á hverju uppsöfnunartímabili til að eiga rétt á uppsöfnunum.</span><span class="sxs-lookup"><span data-stu-id="98112-166">The **Hours worked** value defines the minimum number of hours that employees must work per accrual period to be entitled to accruals.</span></span> <span data-ttu-id="98112-167">Ef ekki er þörf á lágmarki fyrir starfsmenn skal stilla gildið á **0**.</span><span class="sxs-lookup"><span data-stu-id="98112-167">If no minimum is required for employees, set the value to **0**.</span></span>

### <a name="accrual-amount"></a><span data-ttu-id="98112-168">Uppsöfnunarupphæð</span><span class="sxs-lookup"><span data-stu-id="98112-168">Accrual amount</span></span>

<span data-ttu-id="98112-169">Uppsöfnunarupphæðin er fjöldi vinnustunda eða daga sem starfsmenn safna upp á hverju tímabili.</span><span class="sxs-lookup"><span data-stu-id="98112-169">The accrual amount is the number of hours or days that employees will accrue per period.</span></span> <span data-ttu-id="98112-170">Tímabilið byggir á uppsöfnunartíðni.</span><span class="sxs-lookup"><span data-stu-id="98112-170">The period is based on the accrual frequency.</span></span>

### <a name="minimum-balance"></a><span data-ttu-id="98112-171">Lágmarksstaða</span><span class="sxs-lookup"><span data-stu-id="98112-171">Minimum balance</span></span>

<span data-ttu-id="98112-172">Hægt er að nota neikvætt gildi fyrir lágmarksstöðu ef starfsmenn geta óskað eftir lengra leyfi en það sem þeir eru með.</span><span class="sxs-lookup"><span data-stu-id="98112-172">A negative value can be used for the minimum balance if employees can request more leave than they have available.</span></span>

### <a name="maximum-carry-forward"></a><span data-ttu-id="98112-173">Hámark yfirfærslu</span><span class="sxs-lookup"><span data-stu-id="98112-173">Maximum carry-forward</span></span>

<span data-ttu-id="98112-174">Uppsöfnunarferlið mun jafna stöðu leyfa sem fara yfir stöðu hámarksyfirfærslu á árlegri upphafsdagsetningu.</span><span class="sxs-lookup"><span data-stu-id="98112-174">The accrual process will adjust leave balances that exceed the maximum carry-forward balance on the anniversary of the start date.</span></span>

### <a name="grant-amount"></a><span data-ttu-id="98112-175">Styrksupphæð</span><span class="sxs-lookup"><span data-stu-id="98112-175">Grant amount</span></span>

<span data-ttu-id="98112-176">Styrksupphæðin er upprunalegur fjöldi vinnustunda eða daga sem starfsmenn fá þegar þeir skrá sig í fyrsta sinn í leyfisáætlunina.</span><span class="sxs-lookup"><span data-stu-id="98112-176">The grant amount is the initial number of hours or days that employees are granted when they first enroll in the leave plan.</span></span> <span data-ttu-id="98112-177">Upphæðin safnast ekki upp fyrir hvert uppsöfnunartímabil.</span><span class="sxs-lookup"><span data-stu-id="98112-177">The amount doesn't accrue for each accrual period.</span></span>

## <a name="enrollments-and-balances"></a><span data-ttu-id="98112-178">Skráningar og stöður</span><span class="sxs-lookup"><span data-stu-id="98112-178">Enrollments and balances</span></span>

### <a name="enrollment-date"></a><span data-ttu-id="98112-179">Skráningardagur</span><span class="sxs-lookup"><span data-stu-id="98112-179">Enrollment date</span></span>

<span data-ttu-id="98112-180">Skráningardagurinn ákvarðar hvenær starfsmaður getur byrjað að safna frítíma.</span><span class="sxs-lookup"><span data-stu-id="98112-180">The enrollment date determines when an employee can start to accrue time off.</span></span> <span data-ttu-id="98112-181">Til dæmis, ef starfsmaður er skráður í frí 15. júní 2018 getur hún safnað upp frítíma fyrir 15. júní 2018.</span><span class="sxs-lookup"><span data-stu-id="98112-181">For example, if an employee is enrolled in a vacation plan on June 15, 2018, she can't accrue any time off before June 15, 2018.</span></span>

### <a name="current-balance"></a><span data-ttu-id="98112-182">Gildandi staða</span><span class="sxs-lookup"><span data-stu-id="98112-182">Current balance</span></span>

<span data-ttu-id="98112-183">Núgildandi staða er upphæð leyfis sem er í boði fyrir frítímabeiðnir.</span><span class="sxs-lookup"><span data-stu-id="98112-183">The current balance is the amount of leave that is available for time off requests.</span></span> <span data-ttu-id="98112-184">Þessi upphæð inniheldur uppsafnanir, samþykktar beiðnir og breytingar á núgildandi degi.</span><span class="sxs-lookup"><span data-stu-id="98112-184">This amount includes accruals, approved requests, and adjustments through the current date.</span></span>

### <a name="current-balance-examples"></a><span data-ttu-id="98112-185">Dæmi um núverandi stöðu</span><span class="sxs-lookup"><span data-stu-id="98112-185">Current balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="98112-186">Árleg áætlun</span><span class="sxs-lookup"><span data-stu-id="98112-186">Annual plan</span></span>

<span data-ttu-id="98112-187">**Uppsetning áætlunar**</span><span class="sxs-lookup"><span data-stu-id="98112-187">**Plan setup**</span></span>

| <span data-ttu-id="98112-188">Upphafsdagsetning áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-188">Plan start date</span></span> | <span data-ttu-id="98112-189">Skráningardagur</span><span class="sxs-lookup"><span data-stu-id="98112-189">Enrollment date</span></span> | <span data-ttu-id="98112-190">Uppsöfnunartíðni</span><span class="sxs-lookup"><span data-stu-id="98112-190">Accrual frequency</span></span> | <span data-ttu-id="98112-191">Tímabilsgrunnur uppsöfnunar</span><span class="sxs-lookup"><span data-stu-id="98112-191">Accrual period basis</span></span> | <span data-ttu-id="98112-192">Úthlutunardagsetning uppsöfunar</span><span class="sxs-lookup"><span data-stu-id="98112-192">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="98112-193">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-193">1/1/2018</span></span>        | <span data-ttu-id="98112-194">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-194">1/1/2018</span></span>        | <span data-ttu-id="98112-195">Árlegur</span><span class="sxs-lookup"><span data-stu-id="98112-195">Annual</span></span>            | <span data-ttu-id="98112-196">Upphafsdagsetning áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-196">Plan start date</span></span>      | <span data-ttu-id="98112-197">Lok uppsöfnunartímabils</span><span class="sxs-lookup"><span data-stu-id="98112-197">End of accrual period</span></span> |

<span data-ttu-id="98112-198">Unnið er úr uppsöfnunum 1. janúar 2019 (1/1/2019) þannig að þetta heildartímabil er tekið með.</span><span class="sxs-lookup"><span data-stu-id="98112-198">Accruals are processed on January 1, 2019 (1/1/2019), so that that whole period is included.</span></span>

<span data-ttu-id="98112-199">**Niðurstöður**</span><span class="sxs-lookup"><span data-stu-id="98112-199">**Results**</span></span>

| <span data-ttu-id="98112-200">Uppsöfnunarupphæð</span><span class="sxs-lookup"><span data-stu-id="98112-200">Accrual amount</span></span> | <span data-ttu-id="98112-201">Lágmarksstaða</span><span class="sxs-lookup"><span data-stu-id="98112-201">Minimum balance</span></span> | <span data-ttu-id="98112-202">Hámark yfirfærslu</span><span class="sxs-lookup"><span data-stu-id="98112-202">Maximum carry-forward</span></span> | <span data-ttu-id="98112-203">Upphæð beiðni</span><span class="sxs-lookup"><span data-stu-id="98112-203">Request amount</span></span> | <span data-ttu-id="98112-204">Núgildandi staða (frá og með 1/1/2019)</span><span class="sxs-lookup"><span data-stu-id="98112-204">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="98112-205">200</span><span class="sxs-lookup"><span data-stu-id="98112-205">200</span></span>            | <span data-ttu-id="98112-206">0</span><span class="sxs-lookup"><span data-stu-id="98112-206">0</span></span>               | <span data-ttu-id="98112-207">120</span><span class="sxs-lookup"><span data-stu-id="98112-207">120</span></span>                   | <span data-ttu-id="98112-208">40</span><span class="sxs-lookup"><span data-stu-id="98112-208">40</span></span>             | <span data-ttu-id="98112-209">160</span><span class="sxs-lookup"><span data-stu-id="98112-209">160</span></span>                              |

<span data-ttu-id="98112-210">Núgildandi staða (160) = Uppsöfnunarupphæð (200) - Upphæð beiðni (40)</span><span class="sxs-lookup"><span data-stu-id="98112-210">Current balance (160) = Accrual amount (200) – Request amount (40)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="98112-211">Áætlun annan hvern mánuð</span><span class="sxs-lookup"><span data-stu-id="98112-211">Semimonthly plan</span></span>

<span data-ttu-id="98112-212">**Uppsetning áætlunar**</span><span class="sxs-lookup"><span data-stu-id="98112-212">**Plan setup**</span></span>

| <span data-ttu-id="98112-213">Upphafsdagsetning áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-213">Plan start date</span></span> | <span data-ttu-id="98112-214">Skráningardagur</span><span class="sxs-lookup"><span data-stu-id="98112-214">Enrollment date</span></span> | <span data-ttu-id="98112-215">Uppsöfnunartíðni</span><span class="sxs-lookup"><span data-stu-id="98112-215">Accrual frequency</span></span> | <span data-ttu-id="98112-216">Tímabilsgrunnur uppsöfnunar</span><span class="sxs-lookup"><span data-stu-id="98112-216">Accrual period basis</span></span> | <span data-ttu-id="98112-217">Úthlutunardagsetning uppsöfunar</span><span class="sxs-lookup"><span data-stu-id="98112-217">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="98112-218">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-218">1/1/2018</span></span>        | <span data-ttu-id="98112-219">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-219">2/1/2018</span></span>        | <span data-ttu-id="98112-220">Annan hvern mánuð</span><span class="sxs-lookup"><span data-stu-id="98112-220">Semimonthly</span></span>       | <span data-ttu-id="98112-221">Upphafsdagsetning áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-221">Plan start date</span></span>      | <span data-ttu-id="98112-222">Lok uppsöfnunartímabils</span><span class="sxs-lookup"><span data-stu-id="98112-222">End of accrual period</span></span> |

<span data-ttu-id="98112-223">Unnið er úr uppsöfnunum 1. maí 2018 (1/5/2018) þannig að þetta heildartímabil er tekið með.</span><span class="sxs-lookup"><span data-stu-id="98112-223">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="98112-224">**Niðurstöður**</span><span class="sxs-lookup"><span data-stu-id="98112-224">**Results**</span></span>

| <span data-ttu-id="98112-225">Uppsöfnunarupphæð</span><span class="sxs-lookup"><span data-stu-id="98112-225">Accrual amount</span></span> | <span data-ttu-id="98112-226">Lágmarksstaða</span><span class="sxs-lookup"><span data-stu-id="98112-226">Minimum balance</span></span> | <span data-ttu-id="98112-227">Hámark yfirfærslu</span><span class="sxs-lookup"><span data-stu-id="98112-227">Maximum carry-forward</span></span> | <span data-ttu-id="98112-228">Upphæð beiðni</span><span class="sxs-lookup"><span data-stu-id="98112-228">Request amount</span></span> | <span data-ttu-id="98112-229">Núgildandi staða (frá og með 1/1/2019)</span><span class="sxs-lookup"><span data-stu-id="98112-229">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="98112-230">5</span><span class="sxs-lookup"><span data-stu-id="98112-230">5</span></span>              | <span data-ttu-id="98112-231">0</span><span class="sxs-lookup"><span data-stu-id="98112-231">0</span></span>               | <span data-ttu-id="98112-232">120</span><span class="sxs-lookup"><span data-stu-id="98112-232">120</span></span>                   | <span data-ttu-id="98112-233">8</span><span class="sxs-lookup"><span data-stu-id="98112-233">8</span></span>              | <span data-ttu-id="98112-234">22</span><span class="sxs-lookup"><span data-stu-id="98112-234">22</span></span>                               |

<span data-ttu-id="98112-235">Núgildandi staða (22) = Uppsöfnunarupphæð (5 x 6) - Upphæð beiðni (8)</span><span class="sxs-lookup"><span data-stu-id="98112-235">Current balance (22) = Accrual amount (5 × 6) – Request amount (8)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="98112-236">Mánaðarleg áætlun</span><span class="sxs-lookup"><span data-stu-id="98112-236">Monthly plan</span></span>

<span data-ttu-id="98112-237">**Uppsetning áætlunar**</span><span class="sxs-lookup"><span data-stu-id="98112-237">**Plan setup**</span></span>

| <span data-ttu-id="98112-238">Upphafsdagsetning áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-238">Plan start date</span></span> | <span data-ttu-id="98112-239">Skráningardagur</span><span class="sxs-lookup"><span data-stu-id="98112-239">Enrollment date</span></span> | <span data-ttu-id="98112-240">Uppsöfnunartíðni</span><span class="sxs-lookup"><span data-stu-id="98112-240">Accrual frequency</span></span> | <span data-ttu-id="98112-241">Tímabilsgrunnur uppsöfnunar</span><span class="sxs-lookup"><span data-stu-id="98112-241">Accrual period basis</span></span> | <span data-ttu-id="98112-242">Úthlutunardagsetning uppsöfunar</span><span class="sxs-lookup"><span data-stu-id="98112-242">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="98112-243">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-243">1/1/2018</span></span>        | <span data-ttu-id="98112-244">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-244">2/1/2018</span></span>        | <span data-ttu-id="98112-245">Annan hvern mánuð</span><span class="sxs-lookup"><span data-stu-id="98112-245">Semimonthly</span></span>       | <span data-ttu-id="98112-246">Upphafsdagsetning áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-246">Plan start date</span></span>      | <span data-ttu-id="98112-247">Lok uppsöfnunartímabils</span><span class="sxs-lookup"><span data-stu-id="98112-247">End of accrual period</span></span> |

<span data-ttu-id="98112-248">Unnið er úr uppsöfnunum 1. maí 2018 (1/5/2018) þannig að þetta heildartímabil er tekið með.</span><span class="sxs-lookup"><span data-stu-id="98112-248">Accruals are processed on May 1, 2018 (5/1/2018), so that that whole period is included.</span></span>

<span data-ttu-id="98112-249">**Niðurstöður**</span><span class="sxs-lookup"><span data-stu-id="98112-249">**Results**</span></span>

| <span data-ttu-id="98112-250">Uppsöfnunarupphæð</span><span class="sxs-lookup"><span data-stu-id="98112-250">Accrual amount</span></span> | <span data-ttu-id="98112-251">Lágmarksstaða</span><span class="sxs-lookup"><span data-stu-id="98112-251">Minimum balance</span></span> | <span data-ttu-id="98112-252">Hámark yfirfærslu</span><span class="sxs-lookup"><span data-stu-id="98112-252">Maximum carry-forward</span></span> | <span data-ttu-id="98112-253">Upphæð beiðni</span><span class="sxs-lookup"><span data-stu-id="98112-253">Request amount</span></span> | <span data-ttu-id="98112-254">Núgildandi staða (frá og með 1/1/2019)</span><span class="sxs-lookup"><span data-stu-id="98112-254">Current balance (as of 1/1/2019)</span></span> |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| <span data-ttu-id="98112-255">5</span><span class="sxs-lookup"><span data-stu-id="98112-255">5</span></span>              | <span data-ttu-id="98112-256">0</span><span class="sxs-lookup"><span data-stu-id="98112-256">0</span></span>               | <span data-ttu-id="98112-257">120</span><span class="sxs-lookup"><span data-stu-id="98112-257">120</span></span>                   | <span data-ttu-id="98112-258">8</span><span class="sxs-lookup"><span data-stu-id="98112-258">8</span></span>              | <span data-ttu-id="98112-259">7</span><span class="sxs-lookup"><span data-stu-id="98112-259">7</span></span>                                |

<span data-ttu-id="98112-260">Núgildandi staða (7) = Uppsöfnunarupphæð (5 x 3) - Upphæð beiðni (8)</span><span class="sxs-lookup"><span data-stu-id="98112-260">Current balance (7) = Accrual amount (5 × 3) – Request amount (8)</span></span>

### <a name="forecasted-balance"></a><span data-ttu-id="98112-261">Spáð staða</span><span class="sxs-lookup"><span data-stu-id="98112-261">Forecasted balance</span></span>

<span data-ttu-id="98112-262">*Spáð staða* er upphæð leyfis sem er í boði fyrir ókomna dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="98112-262">The *forecasted balance* is the amount of leave that is available on a future date.</span></span> <span data-ttu-id="98112-263">Spáð er fyrir um breytingar á uppsöfnunum og yfirfærslum upp að þeim degi.</span><span class="sxs-lookup"><span data-stu-id="98112-263">Accruals and carry-forward adjustments are forecasted up to that date.</span></span>

<span data-ttu-id="98112-264">Eftirfarandi formúla er notuð:</span><span class="sxs-lookup"><span data-stu-id="98112-264">The following formula is used:</span></span>

<span data-ttu-id="98112-265">Spáð staða mánudags = Núgildandi staða – Beiðnir + Uppsafnanir – breytingar á yfirfærslu</span><span class="sxs-lookup"><span data-stu-id="98112-265">Monday forecasted balance = Current balance – Requests + Accruals – Carry-forward adjustment</span></span>

### <a name="forecasted-balance-examples"></a><span data-ttu-id="98112-266">Dæmi um spáða stöðu</span><span class="sxs-lookup"><span data-stu-id="98112-266">Forecasted balance examples</span></span>

#### <a name="annual-plan"></a><span data-ttu-id="98112-267">Árleg áætlun</span><span class="sxs-lookup"><span data-stu-id="98112-267">Annual plan</span></span>

<span data-ttu-id="98112-268">**Uppsetning áætlunar**</span><span class="sxs-lookup"><span data-stu-id="98112-268">**Plan setup**</span></span>

| <span data-ttu-id="98112-269">Upphafsdagsetning áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-269">Plan start date</span></span> | <span data-ttu-id="98112-270">Skráningardagur</span><span class="sxs-lookup"><span data-stu-id="98112-270">Enrollment date</span></span> | <span data-ttu-id="98112-271">Uppsöfnunartíðni</span><span class="sxs-lookup"><span data-stu-id="98112-271">Accrual frequency</span></span> | <span data-ttu-id="98112-272">Tímabilsgrunnur uppsöfnunar</span><span class="sxs-lookup"><span data-stu-id="98112-272">Accrual period basis</span></span> | <span data-ttu-id="98112-273">Úthlutunardagsetning uppsöfunar</span><span class="sxs-lookup"><span data-stu-id="98112-273">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="98112-274">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-274">1/1/2018</span></span>        | <span data-ttu-id="98112-275">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-275">1/1/2018</span></span>        | <span data-ttu-id="98112-276">Árlegur</span><span class="sxs-lookup"><span data-stu-id="98112-276">Annual</span></span>            | <span data-ttu-id="98112-277">Upphafsdagsetning áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-277">Plan start date</span></span>      | <span data-ttu-id="98112-278">Lok uppsöfnunartímabils</span><span class="sxs-lookup"><span data-stu-id="98112-278">End of accrual period</span></span> |

<span data-ttu-id="98112-279">Unnið er úr uppsöfnunum 15. febrúar 2019 (15/2/2019) þannig að þetta heildartímabil er tekið með.</span><span class="sxs-lookup"><span data-stu-id="98112-279">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="98112-280">**Niðurstöður**</span><span class="sxs-lookup"><span data-stu-id="98112-280">**Results**</span></span>

| <span data-ttu-id="98112-281">Uppsöfnunarupphæð</span><span class="sxs-lookup"><span data-stu-id="98112-281">Accrual amount</span></span> | <span data-ttu-id="98112-282">Lágmarksstaða</span><span class="sxs-lookup"><span data-stu-id="98112-282">Minimum balance</span></span> | <span data-ttu-id="98112-283">Hámark yfirfærslu</span><span class="sxs-lookup"><span data-stu-id="98112-283">Maximum carry-forward</span></span> | <span data-ttu-id="98112-284">Gildandi staða</span><span class="sxs-lookup"><span data-stu-id="98112-284">Current balance</span></span> | <span data-ttu-id="98112-285">Spáð staða (frá og með 15/2/2019)</span><span class="sxs-lookup"><span data-stu-id="98112-285">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="98112-286">20</span><span class="sxs-lookup"><span data-stu-id="98112-286">20</span></span>             | <span data-ttu-id="98112-287">0</span><span class="sxs-lookup"><span data-stu-id="98112-287">0</span></span>               | <span data-ttu-id="98112-288">20</span><span class="sxs-lookup"><span data-stu-id="98112-288">20</span></span>                    | <span data-ttu-id="98112-289">40</span><span class="sxs-lookup"><span data-stu-id="98112-289">40</span></span>              | <span data-ttu-id="98112-290">40</span><span class="sxs-lookup"><span data-stu-id="98112-290">40</span></span>                                   |

<span data-ttu-id="98112-291">Spáð staða (40) = Uppsöfnunarupphæð (20) + Núgildandi staða (40) – breytingar á yfirfærslu (20)</span><span class="sxs-lookup"><span data-stu-id="98112-291">Forecasted balance (40) = Accrual amount (20) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="semimonthly-plan"></a><span data-ttu-id="98112-292">Áætlun annan hvern mánuð</span><span class="sxs-lookup"><span data-stu-id="98112-292">Semimonthly plan</span></span>

<span data-ttu-id="98112-293">**Uppsetning áætlunar**</span><span class="sxs-lookup"><span data-stu-id="98112-293">**Plan setup**</span></span>

| <span data-ttu-id="98112-294">Upphafsdagsetning áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-294">Plan start date</span></span> | <span data-ttu-id="98112-295">Skráningardagur</span><span class="sxs-lookup"><span data-stu-id="98112-295">Enrollment date</span></span> | <span data-ttu-id="98112-296">Uppsöfnunartíðni</span><span class="sxs-lookup"><span data-stu-id="98112-296">Accrual frequency</span></span> | <span data-ttu-id="98112-297">Tímabilsgrunnur uppsöfnunar</span><span class="sxs-lookup"><span data-stu-id="98112-297">Accrual period basis</span></span> | <span data-ttu-id="98112-298">Úthlutunardagsetning uppsöfunar</span><span class="sxs-lookup"><span data-stu-id="98112-298">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="98112-299">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-299">1/1/2018</span></span>        | <span data-ttu-id="98112-300">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-300">2/1/2018</span></span>        | <span data-ttu-id="98112-301">Annan hvern mánuð</span><span class="sxs-lookup"><span data-stu-id="98112-301">Semimonthly</span></span>       | <span data-ttu-id="98112-302">Upphafsdagsetning áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-302">Plan start date</span></span>      | <span data-ttu-id="98112-303">Lok uppsöfnunartímabils</span><span class="sxs-lookup"><span data-stu-id="98112-303">End of accrual period</span></span> |

<span data-ttu-id="98112-304">Unnið er úr uppsöfnunum 15. febrúar 2019 (15/2/2019) þannig að þetta heildartímabil er tekið með.</span><span class="sxs-lookup"><span data-stu-id="98112-304">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="98112-305">**Niðurstöður**</span><span class="sxs-lookup"><span data-stu-id="98112-305">**Results**</span></span>

| <span data-ttu-id="98112-306">Uppsöfnunarupphæð</span><span class="sxs-lookup"><span data-stu-id="98112-306">Accrual amount</span></span> | <span data-ttu-id="98112-307">Lágmarksstaða</span><span class="sxs-lookup"><span data-stu-id="98112-307">Minimum balance</span></span> | <span data-ttu-id="98112-308">Hámark yfirfærslu</span><span class="sxs-lookup"><span data-stu-id="98112-308">Maximum carry-forward</span></span> | <span data-ttu-id="98112-309">Gildandi staða</span><span class="sxs-lookup"><span data-stu-id="98112-309">Current balance</span></span> | <span data-ttu-id="98112-310">Spáð staða (frá og með 15/2/2019)</span><span class="sxs-lookup"><span data-stu-id="98112-310">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="98112-311">5</span><span class="sxs-lookup"><span data-stu-id="98112-311">5</span></span>              | <span data-ttu-id="98112-312">0</span><span class="sxs-lookup"><span data-stu-id="98112-312">0</span></span>               | <span data-ttu-id="98112-313">20</span><span class="sxs-lookup"><span data-stu-id="98112-313">20</span></span>                    | <span data-ttu-id="98112-314">40</span><span class="sxs-lookup"><span data-stu-id="98112-314">40</span></span>              | <span data-ttu-id="98112-315">35</span><span class="sxs-lookup"><span data-stu-id="98112-315">35</span></span>                                   |

<span data-ttu-id="98112-316">Spáð staða (35) = Uppsöfnunarupphæð (5 x 3) + Núgildandi staða (40) – breytingar á yfirfærslu (20)</span><span class="sxs-lookup"><span data-stu-id="98112-316">Forecasted balance (35) = Accrual amount (5 × 3) + Current balance (40) – Carry-forward adjustment (20)</span></span>

#### <a name="monthly-plan"></a><span data-ttu-id="98112-317">Mánaðarleg áætlun</span><span class="sxs-lookup"><span data-stu-id="98112-317">Monthly plan</span></span>

<span data-ttu-id="98112-318">**Uppsetning áætlunar**</span><span class="sxs-lookup"><span data-stu-id="98112-318">**Plan setup**</span></span>

| <span data-ttu-id="98112-319">Upphafsdagsetning áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-319">Plan start date</span></span> | <span data-ttu-id="98112-320">Skráningardagur</span><span class="sxs-lookup"><span data-stu-id="98112-320">Enrollment date</span></span> | <span data-ttu-id="98112-321">Uppsöfnunartíðni</span><span class="sxs-lookup"><span data-stu-id="98112-321">Accrual frequency</span></span> | <span data-ttu-id="98112-322">Tímabilsgrunnur uppsöfnunar</span><span class="sxs-lookup"><span data-stu-id="98112-322">Accrual period basis</span></span> | <span data-ttu-id="98112-323">Úthlutunardagsetning uppsöfunar</span><span class="sxs-lookup"><span data-stu-id="98112-323">Accrual award date</span></span>    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| <span data-ttu-id="98112-324">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-324">1/1/2018</span></span>        | <span data-ttu-id="98112-325">2/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-325">2/1/2018</span></span>        | <span data-ttu-id="98112-326">Annan hvern mánuð</span><span class="sxs-lookup"><span data-stu-id="98112-326">Semimonthly</span></span>       | <span data-ttu-id="98112-327">Upphafsdagsetning áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-327">Plan start date</span></span>      | <span data-ttu-id="98112-328">Lok uppsöfnunartímabils</span><span class="sxs-lookup"><span data-stu-id="98112-328">End of accrual period</span></span> |

<span data-ttu-id="98112-329">Unnið er úr uppsöfnunum 15. febrúar 2019 (15/2/2019) þannig að þetta heildartímabil er tekið með.</span><span class="sxs-lookup"><span data-stu-id="98112-329">Accruals are processed on February 15, 2019 (2/15/2019), so that that whole period is included.</span></span>

<span data-ttu-id="98112-330">**Niðurstöður**</span><span class="sxs-lookup"><span data-stu-id="98112-330">**Results**</span></span>

| <span data-ttu-id="98112-331">Uppsöfnunarupphæð</span><span class="sxs-lookup"><span data-stu-id="98112-331">Accrual amount</span></span> | <span data-ttu-id="98112-332">Lágmarksstaða</span><span class="sxs-lookup"><span data-stu-id="98112-332">Minimum balance</span></span> | <span data-ttu-id="98112-333">Hámark yfirfærslu</span><span class="sxs-lookup"><span data-stu-id="98112-333">Maximum carry-forward</span></span> | <span data-ttu-id="98112-334">Gildandi staða</span><span class="sxs-lookup"><span data-stu-id="98112-334">Current balance</span></span> | <span data-ttu-id="98112-335">Spáð staða (frá og með 15/2/2019)</span><span class="sxs-lookup"><span data-stu-id="98112-335">Forecasted balance (as of 2/15/2019)</span></span> |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| <span data-ttu-id="98112-336">10</span><span class="sxs-lookup"><span data-stu-id="98112-336">10</span></span>             | <span data-ttu-id="98112-337">0</span><span class="sxs-lookup"><span data-stu-id="98112-337">0</span></span>               | <span data-ttu-id="98112-338">20</span><span class="sxs-lookup"><span data-stu-id="98112-338">20</span></span>                    | <span data-ttu-id="98112-339">40</span><span class="sxs-lookup"><span data-stu-id="98112-339">40</span></span>              | <span data-ttu-id="98112-340">30</span><span class="sxs-lookup"><span data-stu-id="98112-340">30</span></span>                                   |

<span data-ttu-id="98112-341">Spáð staða (30) = Uppsöfnunarupphæð (10 x 1) + Núgildandi staða (40) – breytingar á yfirfærslu (20)</span><span class="sxs-lookup"><span data-stu-id="98112-341">Forecasted balance (30) = Accrual amount (10 × 1) + Current balance (40) – Carry-forward adjustment (20)</span></span>

### <a name="proration-balance-examples"></a><span data-ttu-id="98112-342">Dæmi um hlutfallsskipti stöðu</span><span class="sxs-lookup"><span data-stu-id="98112-342">Proration balance examples</span></span>

#### <a name="prorated-monthly-plan"></a><span data-ttu-id="98112-343">Skipt mánaðarleg áætlun</span><span class="sxs-lookup"><span data-stu-id="98112-343">Prorated monthly plan</span></span>

<span data-ttu-id="98112-344">**Uppsetning áætlunar**</span><span class="sxs-lookup"><span data-stu-id="98112-344">**Plan setup**</span></span>

| <span data-ttu-id="98112-345">Upphafsdagsetning áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-345">Plan start date</span></span> | <span data-ttu-id="98112-346">Uppsöfnunartíðni</span><span class="sxs-lookup"><span data-stu-id="98112-346">Accrual frequency</span></span> | <span data-ttu-id="98112-347">Tímabilsgrunnur uppsöfnunar</span><span class="sxs-lookup"><span data-stu-id="98112-347">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="98112-348">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-348">1/1/2018</span></span>        | <span data-ttu-id="98112-349">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="98112-349">Monthly</span></span>           | <span data-ttu-id="98112-350">Upphafsdagsetning áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-350">Plan start date</span></span>      |

<span data-ttu-id="98112-351">**Niðurstöður**</span><span class="sxs-lookup"><span data-stu-id="98112-351">**Results**</span></span>

| <span data-ttu-id="98112-352">Starfsmaður</span><span class="sxs-lookup"><span data-stu-id="98112-352">Employee</span></span>            | <span data-ttu-id="98112-353">Starfsaldur í mánuðum</span><span class="sxs-lookup"><span data-stu-id="98112-353">Months of service</span></span> | <span data-ttu-id="98112-354">Skráningardagur</span><span class="sxs-lookup"><span data-stu-id="98112-354">Enrollment date</span></span> | <span data-ttu-id="98112-355">Upphafsdagur</span><span class="sxs-lookup"><span data-stu-id="98112-355">Start date</span></span> | <span data-ttu-id="98112-356">Uppsöfnunarupphæð</span><span class="sxs-lookup"><span data-stu-id="98112-356">Accrual amount</span></span> | <span data-ttu-id="98112-357">Vinna úr uppsöfnun</span><span class="sxs-lookup"><span data-stu-id="98112-357">Process accrual</span></span> | <span data-ttu-id="98112-358">Efnahagur</span><span class="sxs-lookup"><span data-stu-id="98112-358">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="98112-359">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="98112-359">Jeannette Nicholson</span></span> | <span data-ttu-id="98112-360">0,00</span><span class="sxs-lookup"><span data-stu-id="98112-360">0.00</span></span>              | <span data-ttu-id="98112-361">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-361">6/1/2018</span></span>        | <span data-ttu-id="98112-362">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-362">6/1/2018</span></span>   | <span data-ttu-id="98112-363">1,00</span><span class="sxs-lookup"><span data-stu-id="98112-363">1.00</span></span>           | <span data-ttu-id="98112-364">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-364">9/1/2018</span></span>        | <span data-ttu-id="98112-365">3,00</span><span class="sxs-lookup"><span data-stu-id="98112-365">3.00</span></span>    |
| <span data-ttu-id="98112-366">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="98112-366">Jay Norman</span></span>          | <span data-ttu-id="98112-367">0,00</span><span class="sxs-lookup"><span data-stu-id="98112-367">0.00</span></span>              | <span data-ttu-id="98112-368">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="98112-368">6/15/2018</span></span>       | <span data-ttu-id="98112-369">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="98112-369">6/15/2018</span></span>  | <span data-ttu-id="98112-370">1,00</span><span class="sxs-lookup"><span data-stu-id="98112-370">1.00</span></span>           | <span data-ttu-id="98112-371">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-371">9/1/2018</span></span>        | <span data-ttu-id="98112-372">2,53</span><span class="sxs-lookup"><span data-stu-id="98112-372">2.53</span></span>    |

#### <a name="full-accrual-monthly-plan"></a><span data-ttu-id="98112-373">Full uppsöfnun mánaðarlegrar áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-373">Full accrual monthly plan</span></span>

<span data-ttu-id="98112-374">**Uppsetning áætlunar**</span><span class="sxs-lookup"><span data-stu-id="98112-374">**Plan setup**</span></span>

| <span data-ttu-id="98112-375">Upphafsdagsetning áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-375">Plan start date</span></span> | <span data-ttu-id="98112-376">Uppsöfnunartíðni</span><span class="sxs-lookup"><span data-stu-id="98112-376">Accrual frequency</span></span> | <span data-ttu-id="98112-377">Tímabilsgrunnur uppsöfnunar</span><span class="sxs-lookup"><span data-stu-id="98112-377">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="98112-378">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-378">1/1/2018</span></span>        | <span data-ttu-id="98112-379">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="98112-379">Monthly</span></span>           | <span data-ttu-id="98112-380">Upphafsdagsetning áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-380">Plan start date</span></span>      |

<span data-ttu-id="98112-381">**Niðurstöður**</span><span class="sxs-lookup"><span data-stu-id="98112-381">**Results**</span></span>

| <span data-ttu-id="98112-382">Starfsmaður</span><span class="sxs-lookup"><span data-stu-id="98112-382">Employee</span></span>            | <span data-ttu-id="98112-383">Starfsaldur í mánuðum</span><span class="sxs-lookup"><span data-stu-id="98112-383">Months of service</span></span> | <span data-ttu-id="98112-384">Skráningardagur</span><span class="sxs-lookup"><span data-stu-id="98112-384">Enrollment date</span></span> | <span data-ttu-id="98112-385">Upphafsdagur</span><span class="sxs-lookup"><span data-stu-id="98112-385">Start date</span></span> | <span data-ttu-id="98112-386">Uppsöfnunarupphæð</span><span class="sxs-lookup"><span data-stu-id="98112-386">Accrual amount</span></span> | <span data-ttu-id="98112-387">Vinna úr uppsöfnun</span><span class="sxs-lookup"><span data-stu-id="98112-387">Process accrual</span></span> | <span data-ttu-id="98112-388">Efnahagur</span><span class="sxs-lookup"><span data-stu-id="98112-388">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="98112-389">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="98112-389">Jeannette Nicholson</span></span> | <span data-ttu-id="98112-390">0,00</span><span class="sxs-lookup"><span data-stu-id="98112-390">0.00</span></span>              | <span data-ttu-id="98112-391">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-391">6/1/2018</span></span>        | <span data-ttu-id="98112-392">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-392">6/1/2018</span></span>   | <span data-ttu-id="98112-393">1,00</span><span class="sxs-lookup"><span data-stu-id="98112-393">1.00</span></span>           | <span data-ttu-id="98112-394">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-394">9/1/2018</span></span>        | <span data-ttu-id="98112-395">3,00</span><span class="sxs-lookup"><span data-stu-id="98112-395">3.00</span></span>    |
| <span data-ttu-id="98112-396">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="98112-396">Jay Norman</span></span>          | <span data-ttu-id="98112-397">0,00</span><span class="sxs-lookup"><span data-stu-id="98112-397">0.00</span></span>              | <span data-ttu-id="98112-398">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="98112-398">6/15/2018</span></span>       | <span data-ttu-id="98112-399">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="98112-399">6/15/2018</span></span>  | <span data-ttu-id="98112-400">1,00</span><span class="sxs-lookup"><span data-stu-id="98112-400">1.00</span></span>           | <span data-ttu-id="98112-401">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-401">9/1/2018</span></span>        | <span data-ttu-id="98112-402">3,00</span><span class="sxs-lookup"><span data-stu-id="98112-402">3.00</span></span>    |

#### <a name="no-accrual-monthly-plan"></a><span data-ttu-id="98112-403">Engin uppsöfnun mánaðarlegrar áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-403">No accrual monthly plan</span></span>

<span data-ttu-id="98112-404">**Uppsetning áætlunar**</span><span class="sxs-lookup"><span data-stu-id="98112-404">**Plan setup**</span></span>

| <span data-ttu-id="98112-405">Upphafsdagsetning áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-405">Plan start date</span></span> | <span data-ttu-id="98112-406">Uppsöfnunartíðni</span><span class="sxs-lookup"><span data-stu-id="98112-406">Accrual frequency</span></span> | <span data-ttu-id="98112-407">Tímabilsgrunnur uppsöfnunar</span><span class="sxs-lookup"><span data-stu-id="98112-407">Accrual period basis</span></span> |
|-----------------|-------------------|----------------------|
| <span data-ttu-id="98112-408">1/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-408">1/1/2018</span></span>        | <span data-ttu-id="98112-409">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="98112-409">Monthly</span></span>           | <span data-ttu-id="98112-410">Upphafsdagsetning áætlunar</span><span class="sxs-lookup"><span data-stu-id="98112-410">Plan start date</span></span>      |

<span data-ttu-id="98112-411">**Niðurstöður**</span><span class="sxs-lookup"><span data-stu-id="98112-411">**Results**</span></span>

| <span data-ttu-id="98112-412">Starfsmaður</span><span class="sxs-lookup"><span data-stu-id="98112-412">Employee</span></span>            | <span data-ttu-id="98112-413">Starfsaldur í mánuðum</span><span class="sxs-lookup"><span data-stu-id="98112-413">Months of service</span></span> | <span data-ttu-id="98112-414">Skráningardagur</span><span class="sxs-lookup"><span data-stu-id="98112-414">Enrollment date</span></span> | <span data-ttu-id="98112-415">Upphafsdagur</span><span class="sxs-lookup"><span data-stu-id="98112-415">Start date</span></span> | <span data-ttu-id="98112-416">Uppsöfnunarupphæð</span><span class="sxs-lookup"><span data-stu-id="98112-416">Accrual amount</span></span> | <span data-ttu-id="98112-417">Vinna úr uppsöfnun</span><span class="sxs-lookup"><span data-stu-id="98112-417">Process accrual</span></span> | <span data-ttu-id="98112-418">Efnahagur</span><span class="sxs-lookup"><span data-stu-id="98112-418">Balance</span></span> |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| <span data-ttu-id="98112-419">Jeannette Nicholson</span><span class="sxs-lookup"><span data-stu-id="98112-419">Jeannette Nicholson</span></span> | <span data-ttu-id="98112-420">0,00</span><span class="sxs-lookup"><span data-stu-id="98112-420">0.00</span></span>              | <span data-ttu-id="98112-421">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-421">6/1/2018</span></span>        | <span data-ttu-id="98112-422">6/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-422">6/1/2018</span></span>   | <span data-ttu-id="98112-423">1,00</span><span class="sxs-lookup"><span data-stu-id="98112-423">1.00</span></span>           | <span data-ttu-id="98112-424">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-424">9/1/2018</span></span>        | <span data-ttu-id="98112-425">3,00</span><span class="sxs-lookup"><span data-stu-id="98112-425">3.00</span></span>    |
| <span data-ttu-id="98112-426">Jay Norman</span><span class="sxs-lookup"><span data-stu-id="98112-426">Jay Norman</span></span>          | <span data-ttu-id="98112-427">0,00</span><span class="sxs-lookup"><span data-stu-id="98112-427">0.00</span></span>              | <span data-ttu-id="98112-428">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="98112-428">6/15/2018</span></span>       | <span data-ttu-id="98112-429">6/15/2018</span><span class="sxs-lookup"><span data-stu-id="98112-429">6/15/2018</span></span>  | <span data-ttu-id="98112-430">1,00</span><span class="sxs-lookup"><span data-stu-id="98112-430">1.00</span></span>           | <span data-ttu-id="98112-431">9/1/2018</span><span class="sxs-lookup"><span data-stu-id="98112-431">9/1/2018</span></span>        | <span data-ttu-id="98112-432">2.00</span><span class="sxs-lookup"><span data-stu-id="98112-432">2.00</span></span>    |

