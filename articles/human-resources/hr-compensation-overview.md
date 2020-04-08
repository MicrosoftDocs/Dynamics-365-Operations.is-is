---
title: Launafyrirkomulag
description: Stjórnendur launa og fríðinda geta notað launastjórnun til að viðhalda og vinna úr föstum og breytilegum launafyrirkomulögum fyrir starfsmenn fyrirtækisins.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1b2494ac717bc8c0171be49cc39e6aefff4425ab
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009463"
---
# <a name="compensation-plans"></a><span data-ttu-id="35009-103">Launafyrirkomulag</span><span class="sxs-lookup"><span data-stu-id="35009-103">Compensation plans</span></span>

<span data-ttu-id="35009-104">Stjórnendur launa og fríðinda geta notað launastjórnun til að viðhalda og vinna úr föstum og breytilegum launafyrirkomulögum fyrir starfsmenn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="35009-104">Compensation and Benefits Managers can use Compensation management to maintain and process fixed and variable compensation plans for the organization's employees.</span></span>

### <a name="introduction"></a><span data-ttu-id="35009-105">Inngangur</span><span class="sxs-lookup"><span data-stu-id="35009-105">Introduction</span></span>

<span data-ttu-id="35009-106">Lausnastjórnun er notuð til að stýra afhendingu grunnlauna og umbunar.</span><span class="sxs-lookup"><span data-stu-id="35009-106">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="35009-107">Föstum grunnlaunum starfsmanns og verðleikaaukning er stýrt með launafyrirkomulag fastra launa.</span><span class="sxs-lookup"><span data-stu-id="35009-107">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="35009-108">Greiðsla hvatagreiðslu, svo sem kaupauka, afkastaumbun, hlutafjárkaupréttur og styrki, en einnig eins-skiptis umbun, er stýrt með breytilegu launafyrirkomulagi.</span><span class="sxs-lookup"><span data-stu-id="35009-108">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span> 

<span data-ttu-id="35009-109">Hægt er að tengja starfsmenn við eina eða fleiri áætlanir af báðum gerðum.</span><span class="sxs-lookup"><span data-stu-id="35009-109">Employees can be enrolled in one or more plans of both types.</span></span> <span data-ttu-id="35009-110">Starfsmaður verður að uppfylla eftirfarandi skilyrði til að vera hæfur fyrir launafyrirkomulagið.</span><span class="sxs-lookup"><span data-stu-id="35009-110">An employee must meet the following requirements in order to be eligible for enrollment in a compensation plan:</span></span>
-   <span data-ttu-id="35009-111">Starfsmaðurinn verður að hafa virka stöðuverkefni.</span><span class="sxs-lookup"><span data-stu-id="35009-111">The employee must have an active position assignment.</span></span>
-   <span data-ttu-id="35009-112">Starfsmaðurinn verður að uppfylla skilyrðin sem eru skilgreind af hæfnisreglum fyrir launafyrirkomulag.</span><span class="sxs-lookup"><span data-stu-id="35009-112">The employee must meet the criteria that are defined by eligibility rules for a compensation plan.</span></span>

## <a name="compensation-setup"></a><span data-ttu-id="35009-113"> Uppsetning launa.</span><span class="sxs-lookup"><span data-stu-id="35009-113">Compensation setup</span></span>
<span data-ttu-id="35009-114">Í eftirfarandi töflu er listi yfir þætti launaferlis sem geta verið sambyggt uppsetningu launafyrirkomulags fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="35009-114">The following table lists components of the compensation process that can be integral in setting up your company's compensation plans.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="35009-115">Íhlutur</span><span class="sxs-lookup"><span data-stu-id="35009-115">Component</span></span></th>
<th><span data-ttu-id="35009-116">Meiri upplýsingar…</span><span class="sxs-lookup"><span data-stu-id="35009-116">More information…</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="35009-117">Aðgerðir fastra launa</span><span class="sxs-lookup"><span data-stu-id="35009-117">Fixed compensation actions</span></span></td>
<td><span data-ttu-id="35009-118">Aðgerðir fastra launa hafa tvennan tilgang:</span><span class="sxs-lookup"><span data-stu-id="35009-118">Fixed compensation actions accomplish two purposes:</span></span>
<ul>
<li><span data-ttu-id="35009-119">Aðgerðir getur tilgreint gerðir upplýsingar sem verður að skrá þegar laun starfsmanns breytist.</span><span class="sxs-lookup"><span data-stu-id="35009-119">Actions can specify the kind of information that must be recorded when an employee’s compensation changes.</span></span> <span data-ttu-id="35009-120">Til dæmis er hægt að krefjast ástæðu breytinga, eins og stöðuhækkun eða stöðulækkun verður skráð.</span><span class="sxs-lookup"><span data-stu-id="35009-120">For example, you can require that the reason a change, such as a promotion or a demotion be recorded.</span></span></li>
<li><span data-ttu-id="35009-121">Aðgerðir geta tryggt að útreikningur er notað þegar launafyrirkomulag fastra launa eru unnið.</span><span class="sxs-lookup"><span data-stu-id="35009-121">Actions can ensure that a calculation is applied when fixed compensation plans are processed.</span></span>  <span data-ttu-id="35009-122">Til dæmis, aðgerðir af gerðinni eigið fé bera saman laun fyrir starfsmenn við lágmarks tilvísunarpunkt fyrir stig starfsmanns og tryggja að starfsmaðurinn fái greidd að minnsta kosti lágmarkið.&#39;</span><span class="sxs-lookup"><span data-stu-id="35009-122">For example, actions of type Equity will compare the employees pay to the minimum reference point for the level on the employee&#39;s and ensure the employee is getting paid at least the minimum.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35009-123">Stig</span><span class="sxs-lookup"><span data-stu-id="35009-123">Levels</span></span></td>
<td><span data-ttu-id="35009-124">Stigum er úthlutað á störf, og allar stöður sem eru tengdar við starfstilvísun.</span><span class="sxs-lookup"><span data-stu-id="35009-124">Levels are associated with jobs and any positions that are related to a job reference.</span></span> <span data-ttu-id="35009-125">Hægt er að stofna afmarkaðar gerðir launafyrirkomulaga: Gráða, braut og skref.</span><span class="sxs-lookup"><span data-stu-id="35009-125">You can create discrete levels for the three types of compensation plans: Grade, Band, and Step.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35009-126">Fylki nýtingar launabils</span><span class="sxs-lookup"><span data-stu-id="35009-126">Range utilization matrix</span></span></td>
<td><span data-ttu-id="35009-127">Nýtingarfylki sviðs hjálpar þér að flytja starfsmenn í stýripunktinn fyrir starf þeirra.</span><span class="sxs-lookup"><span data-stu-id="35009-127">A range utilization matrix helps you transition employees to the control point for their jobs.</span></span> <span data-ttu-id="35009-128">Einnig er hægt að nota nýtingarmörk til að stýra launataxta eigin fjár innan fyrirtækisins óháð frammistöðu starfsmanns eða heildarframmistöðu fyrirtækisins.&#39;</span><span class="sxs-lookup"><span data-stu-id="35009-128">You can also use range utilization to control pay rate equity in the company without regard to an individual employee&#39;s performance or the overall performance of the company.</span></span> <span data-ttu-id="35009-129">Til dæmis Starfsmenn sem fá minna greitt í sínu sviði fá hærri prósentuaukning en þeir starfsmenn sem eru fá greitt meira innan sviðsins.</span><span class="sxs-lookup"><span data-stu-id="35009-129">For example, employees who are paid lower in their range get higher percentage increases than employees who are paid higher in the range.</span></span> <span data-ttu-id="35009-130">Á þennan hátt er hægt kerfisbundið hægt að mótbóka muninn á eigin fé.</span><span class="sxs-lookup"><span data-stu-id="35009-130">In this manner, you can systematically offset equity differences.</span></span> <span data-ttu-id="35009-131">Notkunarmörkin eru reiknuð út á eftirfarandi hátt: (Fastur launataxti - Lágmark sviðs) / (Hámark sviðs - Lágmark sviðs).</span><span class="sxs-lookup"><span data-stu-id="35009-131">The range utilization is calculated as follows: (Fixed Pay Rate - Range Minimum) ÷ (Range Maximum - Range Minimum).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35009-132">Uppsetning tilvísunarpunkta</span><span class="sxs-lookup"><span data-stu-id="35009-132">Reference point setups</span></span></td>
<td><span data-ttu-id="35009-133">Uppsetningar tilvísunarpunkta innihalda hóp tilvísunarpunkta sem sýna svið í fylki.</span><span class="sxs-lookup"><span data-stu-id="35009-133">A reference point setup includes a set of reference points that represent ranges in a matrix.</span></span> <span data-ttu-id="35009-134">Hverju sviði má tengja launataxta.</span><span class="sxs-lookup"><span data-stu-id="35009-134">Each range can be associated with a pay rate.</span></span> <span data-ttu-id="35009-135">Til dæmis hafa gráðuáætlanir oft tilvísunarpunkta fyrir Lágmark, Miðpunktur og Hámark.</span><span class="sxs-lookup"><span data-stu-id="35009-135">For example, grade plans will often have reference points of Minimum, Midpoint, and Maximum.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35009-136">Launafylki</span><span class="sxs-lookup"><span data-stu-id="35009-136">Compensation matrix</span></span></td>
<td><span data-ttu-id="35009-137">Launafylki er safn tilvísunarpunkta og stiga sem þú notar til að stofna launafyrirkomulag.</span><span class="sxs-lookup"><span data-stu-id="35009-137">A compensation matrix is the set of reference points and levels that you use to create a compensation structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35009-138">Launaskipulag</span><span class="sxs-lookup"><span data-stu-id="35009-138">Compensation structure</span></span></td>
<td><span data-ttu-id="35009-139">Launaskipulag er launafylki sem er með launataxta sem tengist tilvísunarpunkta fyrir hvert stig.</span><span class="sxs-lookup"><span data-stu-id="35009-139">A compensation structure is a compensation matrix that has pay rates associated with the reference points for each level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35009-140">Hæfnisreglur</span><span class="sxs-lookup"><span data-stu-id="35009-140">Eligibility rules</span></span></td>
<td><span data-ttu-id="35009-141">Hægt er að nota hæfnisreglur til að bera kennsl á starfsmenn í tilteknum vinnslur, vinnsluaðgerðir, vinnslugerðir, deildum, verkalýðsfélögum, eða launasvæðum sem tilteknar launafyrirkomulag eiga við um.</span><span class="sxs-lookup"><span data-stu-id="35009-141">Eligibility rules are used to identify employees in specific jobs, job functions, job types, departments, labor unions, or compensation regions that are covered by specific compensation plans.</span></span> <span data-ttu-id="35009-142">Stofna verður hæfnireglur fyrir bæði launafyrirkomulag fastra og breytilegra launa til að skrá starfsmenn í áætlun.</span><span class="sxs-lookup"><span data-stu-id="35009-142">You must create eligibility rules for both variable and fixed compensation plans in order to enroll employees in the plan.</span></span> <span data-ttu-id="35009-143">Eftir að hafa tilgreint hæfnisreglur fyrir greiðsluáætlun, skal skilgreina stiga munu eiga við vinnslur sem áætlunin á við um.</span><span class="sxs-lookup"><span data-stu-id="35009-143">After eligibility rules are specified for a compensation plan, you can define the levels that should apply to the jobs that are covered by the plan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35009-144">Greiðslutíðni</span><span class="sxs-lookup"><span data-stu-id="35009-144">Pay frequencies</span></span></td>
<td><span data-ttu-id="35009-145">Greiðslutíðni er notuð til að skilgreina tímabilið sem laun eru greidd fyrir. </span><span class="sxs-lookup"><span data-stu-id="35009-145">Pay frequencies are used to define the time period for which the compensation is specified.</span></span>  <span data-ttu-id="35009-146">Til dæmis auðveldar greiðslutíðni að skilja hvort launaupphæðin er tilgreindur sem árleg laun eða launataxti á klukkustund.</span><span class="sxs-lookup"><span data-stu-id="35009-146">For example, the pay frequency helps you understand if the compensation amount is specified as an annual salary versus an hourly pay rate.</span></span> <span data-ttu-id="35009-147">Greiðslutíðni eru einnig notaðar til að setja upp umreiknistuðla til að umbreyta upphæðir launa úr  greiðslutíðni fyrir mánaðarlega, vikulega, hálfsmánaðarlegrar og tímakaups yfir í árleg greiðslutíðni.</span><span class="sxs-lookup"><span data-stu-id="35009-147">Pay frequencies are also used to set up conversion factors to convert compensation amounts from monthly, weekly, biweekly and hourly pay frequencies to an annual pay frequency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35009-148">Launasvæði</span><span class="sxs-lookup"><span data-stu-id="35009-148">Compensation regions</span></span></td>
<td><span data-ttu-id="35009-149">Launasvæði eru notuð til þess að tilgreina laun starfsmanns samkvæmt staðsetningu vinnustaðar.</span><span class="sxs-lookup"><span data-stu-id="35009-149">Compensation regions are used to specify employee compensation based on the location of the workplace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35009-150">Stýripunktur</span><span class="sxs-lookup"><span data-stu-id="35009-150">Control point</span></span></td>
<td><span data-ttu-id="35009-151">Stýripunkturinn skilgreinir hvað þú telur vera besta launataxta fyrir alla starfsmenn í launastigi.</span><span class="sxs-lookup"><span data-stu-id="35009-151">The control point defines what you consider to be the ideal pay rate for all employees at a compensation level.</span></span> <span data-ttu-id="35009-152">Fyrir áætlunarskipulag gráðu eru stýripunktar yfirleitt miðpunktur sviðsins.</span><span class="sxs-lookup"><span data-stu-id="35009-152">For grade plan structures, control points are typically the midpoint of the ranges.</span></span> <span data-ttu-id="35009-153">Brautarskipulag notast sjaldan við stýripunkta.</span><span class="sxs-lookup"><span data-stu-id="35009-153">Band structures rarely use control points.</span></span> <span data-ttu-id="35009-154">Hægt er að tilgreina stýripunktur fyrir launafyrirkomulag fastra launa í skjámynd launafyrirkomulags Fastra launa.</span><span class="sxs-lookup"><span data-stu-id="35009-154">You can specify the control point for a fixed compensation plan in the Fixed compensation plans form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35009-155">Starfshlutverk</span><span class="sxs-lookup"><span data-stu-id="35009-155">Job functions</span></span></td>
<td><span data-ttu-id="35009-156">Starfshlutverk eru notaðar til að flokka og sía launafyrirkomulag fyrir tiltekin störf.</span><span class="sxs-lookup"><span data-stu-id="35009-156">Job functions are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35009-157">Vinnslugerðir</span><span class="sxs-lookup"><span data-stu-id="35009-157">Job types</span></span></td>
<td><span data-ttu-id="35009-158">Vinnslugerðir eru notaðar til að flokka og sía launafyrirkomulag fyrir tiltekin störf.</span><span class="sxs-lookup"><span data-stu-id="35009-158">Job types are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35009-159">Gerðir breytilegra uppbóta</span><span class="sxs-lookup"><span data-stu-id="35009-159">Variable compensation types</span></span></td>
<td><span data-ttu-id="35009-160">Breytileg launagerð, eins og hlutabréfaumbun eða umbun í reiðufé, er sett upp í breytilegu launafyrirkomulagi.</span><span class="sxs-lookup"><span data-stu-id="35009-160">Variable compensation types, such as stock awards or cash award bonuses, are set up in variable compensation plans.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35009-161">Launanet</span><span class="sxs-lookup"><span data-stu-id="35009-161">Compensation grids</span></span></td>
<td><span data-ttu-id="35009-162">Launanet innihalda launaskipulagið.</span><span class="sxs-lookup"><span data-stu-id="35009-162">Compensation grids contain the compensation structure.</span></span>  <span data-ttu-id="35009-163">Eitt eða fleiri launafyrirkomulag geta notað hnitanet launa.</span><span class="sxs-lookup"><span data-stu-id="35009-163">Compensation grids can be used by one or more compensation plans.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="35009-164">Afkastaáætlanir</span><span class="sxs-lookup"><span data-stu-id="35009-164">Performance plans</span></span></td>
<td><span data-ttu-id="35009-165">Afkastaáætlanir eru notaðar til að tengja afköst við úthlutunarfylki, til að nota áætlun fyrir árangurstengingu launa.</span><span class="sxs-lookup"><span data-stu-id="35009-165">Performance plans are used to associate performance with an allocation matrix, so that you can use the plan in a pay-for-performance strategy.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="35009-166">Afkastaeinkunnir</span><span class="sxs-lookup"><span data-stu-id="35009-166">Performance ratings</span></span></td>
<td><span data-ttu-id="35009-167">Afkastaeinkunnir eru notaðar í afkastaáætlunum til að ákvarða upphæð umbunar vegna verðleika eða afkasta.</span><span class="sxs-lookup"><span data-stu-id="35009-167">Performance ratings are used in performance plans to determine the amount of a merit award or performance award.</span></span></td>
</tr>
</tbody>
</table>

## <a name="process-events"></a><span data-ttu-id="35009-168">Vinnslutilvik</span><span class="sxs-lookup"><span data-stu-id="35009-168">Process events</span></span>
<span data-ttu-id="35009-169">Vinnslutilvik reiknar út launaupplýsingar fyrir tilgreint tímabil handa öllum starfsmönnum sem eru skráðir í eina eða fleiri fastar eða breytilegar launafyrirkomulag.</span><span class="sxs-lookup"><span data-stu-id="35009-169">A process event calculates compensation information for a specific period for all employees who are enrolled in one or more fixed or variable compensation plans.</span></span> <span data-ttu-id="35009-170">Hægt er að keyra vinnslutilvik endurtekið, til að prófa eða uppfæra útreiknaðar launaniðurstöður.</span><span class="sxs-lookup"><span data-stu-id="35009-170">You can run a process event repeatedly to test or update calculated compensation results.</span></span>

<a name="compensation-events"></a><span data-ttu-id="35009-171">Launatilvik</span><span class="sxs-lookup"><span data-stu-id="35009-171">Compensation events</span></span>
-------------------

<span data-ttu-id="35009-172">Í hvert sinn vinnslutilvik er keyrt er launatilvik stofnað.</span><span class="sxs-lookup"><span data-stu-id="35009-172">Each time a process event is run, a compensation event is created.</span></span>  <span data-ttu-id="35009-173">Launatilvik innihalda niðurstöðu launavinnslu fyrir hvern starfsmann sem hafður var með í vinnslutilvikinu.</span><span class="sxs-lookup"><span data-stu-id="35009-173">Compensation events contain the results of the compensation process for each employee included in that process event.</span></span>  <span data-ttu-id="35009-174">Þegar útreikningar eru réttir er hægt að hlaða launatilvikinu til að uppfæra launafærslur fyrir starfsmenn sem verða fyrir áhrifum af vinnslutilvikið.</span><span class="sxs-lookup"><span data-stu-id="35009-174">When the calculations are correct, you can load the compensation event to update the compensation records for the employees who are affected by the process event.</span></span>

## <a name="recommendations"></a><span data-ttu-id="35009-175"> Ráðleggingar</span><span class="sxs-lookup"><span data-stu-id="35009-175">Recommendations</span></span>
<span data-ttu-id="35009-176">Þegar vinnslutilvik hefur verið keyrt, geturðu stungið uppá leiðréttingar á verðleikahækkun starfsmanns eða umbunarupphæð út frá reiknuðum leiðbeiningar á vinnslutilvikinu.</span><span class="sxs-lookup"><span data-stu-id="35009-176">After you run a process event, you can recommend adjustments to an employee’s merit increase or award amount, based on the calculated guidelines of the process event.</span></span> <span data-ttu-id="35009-177">Til að gera tillögur fyrir starfsmenn, verður að virkja tillögur þegar launafyrirkomulag eru sett upp eða þegar sett er upp vinnslutilvikið.</span><span class="sxs-lookup"><span data-stu-id="35009-177">To make recommendations for employees, you must enable recommendations when you set up compensation plans or when you set up the process event.</span></span>


