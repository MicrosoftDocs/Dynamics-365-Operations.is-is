---
title: Fjarvistarskráning í Tími og mæting
description: Í þessu efnisatriði er útskýrt hvernig á að meðhöndla fjarvistarskráningu í Tími og mæting.
author: johanhoffmann
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JMGParameters, JmgAbsenceCalendar
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 961b87fb066018f9f6ecc3dcc3cc88e64574bb64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246550"
---
# <a name="absence-registration-in-time-and-attendance"></a><span data-ttu-id="9b117-103">Fjarvistarskráning í Tími og mæting</span><span class="sxs-lookup"><span data-stu-id="9b117-103">Absence registration in Time and attendance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9b117-104">Þetta efni lýsir hugtökunum um fjarveru og útskýrir hvernig á að meðhöndla fjarveru í Tíma og mætingu.</span><span class="sxs-lookup"><span data-stu-id="9b117-104">This topic describes the concepts for absence and explains how to handle absence in Time and attendance.</span></span>

## <a name="absence-that-is-based-on-regular-work-hours"></a><span data-ttu-id="9b117-105">Fjarvist sem er byggður á venjulegum vinnustundum</span><span class="sxs-lookup"><span data-stu-id="9b117-105">Absence that is based on regular work hours</span></span>

<span data-ttu-id="9b117-106">Starfsmenn eru talin fjarverandi allar klukkustundir sem þeir vinna ekki á venjulegum vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="9b117-106">Workers are considered absent for any hours that they don't work during their regular work hours.</span></span> <span data-ttu-id="9b117-107">Venjulegur vinnutími er skilgreindur í forstillingu staðalvinnutíma starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="9b117-107">Regular work hours are defined in a worker's standard time profile.</span></span>

<span data-ttu-id="9b117-108">Til dæmis vinnur starfsmaður á forstillingu dags útfrá innstimplun klukkan 07:00 og útstimplun klukkan 15:00.</span><span class="sxs-lookup"><span data-stu-id="9b117-108">For example, a worker is working on a day profile that has clock-in at 7:00 AM and clock-out at 3:00 PM.</span></span> <span data-ttu-id="9b117-109">Ef starfsmaður stimplar sig inn klukkan 09:00 er hann talinn fjarverandi frá 07:00 til 09:00 á þeim degi.</span><span class="sxs-lookup"><span data-stu-id="9b117-109">If the worker clocks in at 9:00 AM, he is considered absent from 7:00 AM to 9:00 AM on that day.</span></span>

<span data-ttu-id="9b117-110">Í þessu tilviki eru starfsmenn beðnir um að slá inn ástæðu fyrir fjarveru þeirra.</span><span class="sxs-lookup"><span data-stu-id="9b117-110">In this case, workers are prompted to enter a reason for their absence.</span></span> <span data-ttu-id="9b117-111">Þeir geta skilgreint ástæðu með því að velja fjarveru kóða.</span><span class="sxs-lookup"><span data-stu-id="9b117-111">They can specify a reason by selecting an absence code.</span></span>

## <a name="absence-codes"></a><span data-ttu-id="9b117-112">Fjarvistarkóðar</span><span class="sxs-lookup"><span data-stu-id="9b117-112">Absence codes</span></span>

<span data-ttu-id="9b117-113">Gerðir fjarvistarkóða leyfa skilgreina hinar ýmsu gerðir fjarvista.</span><span class="sxs-lookup"><span data-stu-id="9b117-113">Absence codes define the various types of absence.</span></span> <span data-ttu-id="9b117-114">Fyrirtækin skilgreina kóðana.</span><span class="sxs-lookup"><span data-stu-id="9b117-114">Absence codes are defined by the company.</span></span>

<span data-ttu-id="9b117-115">Ýmsar reglur er hægt að setja um fjarvistarkóða.</span><span class="sxs-lookup"><span data-stu-id="9b117-115">Various rules can be applied to absence codes.</span></span> <span data-ttu-id="9b117-116">Til dæmis er hægt að stilla fjarvistarkóða til að draga frá eða veita greiðslur.</span><span class="sxs-lookup"><span data-stu-id="9b117-116">For example, an absence code can be configured to deduct or grant pay.</span></span>

<span data-ttu-id="9b117-117">Til dæmis skilgreinir fyrirtæki **Seint** frágangskóði sem starfsmenn nota ef þeir koma seint og hafa ekki góða ástæðu.</span><span class="sxs-lookup"><span data-stu-id="9b117-117">For example, a company defines a **Late** absence code that workers use if they come in late and don't have a good reason.</span></span> <span data-ttu-id="9b117-118">Fyrirtækið skilgreinir einnig **innri námskeið** fjarvistarkóða sem starfsmenn nota fyrir tíma sem þeir eyða að sækja innri námskeið.</span><span class="sxs-lookup"><span data-stu-id="9b117-118">The company also defines an **Internal course** absence code that workers use for time that they spend attending internal courses.</span></span> <span data-ttu-id="9b117-119">Þessar fjarvistarkóðar geta verið settar upp þannig að **Seint** dregur frá launum starfsmanns en **innri námskeið** dregur ekki frá launum starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="9b117-119">These absence codes can be set up so that **Late** deducts from a worker's pay but **Internal course** doesn't deduct from a worker's pay.</span></span>

<span data-ttu-id="9b117-120">Hægt er að setja upp sjálfvirka fjarvistarkóða.</span><span class="sxs-lookup"><span data-stu-id="9b117-120">You can set up automatic absence codes.</span></span> <span data-ttu-id="9b117-121">Þessar fjarverukóðar geta verið notaðir til að reikna tíma starfsmanns þegar engin fjarvist er skráð.</span><span class="sxs-lookup"><span data-stu-id="9b117-121">These absence codes can be used to calculate a worker's time when no absence is registered.</span></span> <span data-ttu-id="9b117-122">Forstilling starfsmanns ákvarðar hvort fjarvistarkóði fyrir staðlaðan tíma eða sveigjanlegan tíma er notuð.</span><span class="sxs-lookup"><span data-stu-id="9b117-122">The worker's time profile determines whether the absence code for standard time or flex time is used.</span></span>

### <a name="set-up-standard-time-and-flex-time"></a><span data-ttu-id="9b117-123">Setja upp staðlaðan og sveigjanlegan tíma</span><span class="sxs-lookup"><span data-stu-id="9b117-123">Set up standard time and flex time</span></span>

- <span data-ttu-id="9b117-124">Stilla færibreytur fyrir staðlaða tíma og sveigjanlegan tíma með því að nota **sjálfvirka innsetning fjarvista** og **sjálfvirk innsetningu sveigjanlegt** valmöguleikar á **tími og mæting færibreytur** síðunni.</span><span class="sxs-lookup"><span data-stu-id="9b117-124">Configure the parameters for standard time and flex time by using the **Auto insert absence** and **Auto insert Flex-** options on the **Time and attendance parameters** page.</span></span>

## <a name="absence-groups"></a><span data-ttu-id="9b117-125">Fjarvistaflokkar</span><span class="sxs-lookup"><span data-stu-id="9b117-125">Absence groups</span></span>

<span data-ttu-id="9b117-126">Fjarvistarkóðar eru flokkaðar í fjarveruhópa.</span><span class="sxs-lookup"><span data-stu-id="9b117-126">Absence codes are grouped into absence groups.</span></span> <span data-ttu-id="9b117-127">Fjarvistarflokkar eru notaðir til að flokka fjarvistarkóða sem hafa svipaða eiginleika í hóp.</span><span class="sxs-lookup"><span data-stu-id="9b117-127">You use absence groups to group absence codes that have common characteristics.</span></span> <span data-ttu-id="9b117-128">Dæmi um það eru fjarvistarkóðar vegna lagalegrar fjarvistar eða fjarveru vegna læknisheimsóknar, kviðdómsskyldu eða barns sem er lasið.</span><span class="sxs-lookup"><span data-stu-id="9b117-128">Examples include absence codes for a legal absence, or absence because of a doctor's appointment, jury duty, or a sick child.</span></span>

## <a name="planned-absence"></a><span data-ttu-id="9b117-129">Áætlaðar fjarvistir</span><span class="sxs-lookup"><span data-stu-id="9b117-129">Planned absence</span></span>

<span data-ttu-id="9b117-130">Ef þú veist að starfsmaður verður fjarverandi um tíma, svo sem komandi frí, getur þú notað áætlaða fjarvist.</span><span class="sxs-lookup"><span data-stu-id="9b117-130">If you know that a worker will be absent for a period, such as an upcoming vacation, you can use planned absence.</span></span> <span data-ttu-id="9b117-131">Þú setur upp áætlaðan fjarvist með því að stilla fjarvistarkóðann þannig að hann geri ráð fyrir áætlaðri fjarvist.</span><span class="sxs-lookup"><span data-stu-id="9b117-131">You set up planned absence by configuring the absence code so that it considers the planned absence.</span></span> <span data-ttu-id="9b117-132">Þegar þú setur upp áætlaða fjarvist ertu ekki beðin(n) um fjarvistarkóða meðan á fjarveru stendur þegar skráningar notandatíma eru reiknuð.</span><span class="sxs-lookup"><span data-stu-id="9b117-132">When you set up a planned absence, you aren't prompted for an absence code during the absence period when user time registrations are calculated.</span></span> <span data-ttu-id="9b117-133">Áætlaða fjarvist er hægt að skilgreina fyrir einn starfsmann, eða þú getur skilgreint runuvinnslu til þess að fjöldauppfæra áætlaðar fjarvistir fyrir starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="9b117-133">Planned absence can be defined for a single worker, or you can define a batch job to bulk update the planned absence for workers.</span></span>

### <a name="set-up-planned-absence"></a><span data-ttu-id="9b117-134">Setja upp áætlaða fjarvist</span><span class="sxs-lookup"><span data-stu-id="9b117-134">Set up planned absence</span></span>

1. <span data-ttu-id="9b117-135">Veldu **Mannauður** &gt; **Starfsfólk** &gt; **Starfsmenn** og veldu starfsmann.</span><span class="sxs-lookup"><span data-stu-id="9b117-135">Select **Human resources** &gt; **Workers** &gt; **Employees**, and select an employee.</span></span>
2. <span data-ttu-id="9b117-136">Veldu **Tími** &gt; **Tími úthlutanir** &gt; **Tími fjarvistarskráning** og setja upp fyrirhugaða fjarvist.</span><span class="sxs-lookup"><span data-stu-id="9b117-136">Select **Time** &gt; **Time assignments** &gt; **Time Absence registration**, and set up the planned absence.</span></span>

## <a name="interrupted-planned-absence"></a><span data-ttu-id="9b117-137">Rof á ætlaðri fjarvist</span><span class="sxs-lookup"><span data-stu-id="9b117-137">Interrupted planned absence</span></span>

<span data-ttu-id="9b117-138">Ef þú notar **Rof** valkostinn þegar þú setur upp áætlaða fjarvist verður áætlaða fjarvistin rofin ef starfsmaðurinn skráir sig á áætlaðan fjarvistartíma.</span><span class="sxs-lookup"><span data-stu-id="9b117-138">If you apply the **Interrupt** option when you set up a planned absence, the planned absence will be interrupted if the worker signs in during the planned absence period.</span></span> <span data-ttu-id="9b117-139">Áætluð fjarvist verður merkt sem **Rofin** og mun ekki hafa nein áhrif á framtíðarútreikninga.</span><span class="sxs-lookup"><span data-stu-id="9b117-139">The planned absence will be marked as **Interrupted** and won't have any effect on future calculations.</span></span>

### <a name="set-up-a-planned-absence-for-interruption"></a><span data-ttu-id="9b117-140">Setja upp áætlaða fjarvist fyrir rof</span><span class="sxs-lookup"><span data-stu-id="9b117-140">Set up a planned absence for interruption</span></span>

1. <span data-ttu-id="9b117-141">Opnaðu **Skráningar tíma fjarvista** síðuna eins og lýst er í ferlinu til að setja upp áætlaða fjarvist.</span><span class="sxs-lookup"><span data-stu-id="9b117-141">Open the **Time Absence registration** page as described in the procedure for setting up planned absence.</span></span>
2. <span data-ttu-id="9b117-142">Velja **Rof**.</span><span class="sxs-lookup"><span data-stu-id="9b117-142">Select **Interrupt**.</span></span>

<span data-ttu-id="9b117-143">**Rof** valkosturinn á við þegar tími er skráður í gegnum vinnusal afgreiðslustöðvar eða tæki vinnusals.</span><span class="sxs-lookup"><span data-stu-id="9b117-143">The **Interrupt** option applies when time is registered through the shop floor terminal or the shop floor device.</span></span> <span data-ttu-id="9b117-144">Valkosturinn gildir ekki ef skráningar eru færðar inn á útreikninga- og samþykktarsíðunum, eða á **rafrænt tímaspjald** síðunni.</span><span class="sxs-lookup"><span data-stu-id="9b117-144">The option doesn't apply if the registrations are entered on the calculation and approval pages, or on the **Electronic timecard** page.</span></span>

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a><span data-ttu-id="9b117-145">Dæmi um notkun á fjarvist í sveigjanlegri forstillingu</span><span class="sxs-lookup"><span data-stu-id="9b117-145">Examples of the use of absence in a flex profile</span></span>

<span data-ttu-id="9b117-146">Eftirfarandi þrjú dæmi sýna hvernig fjarvistir eru reiknaður út í forstillingu sem hefur sveigjanlegan tíma.</span><span class="sxs-lookup"><span data-stu-id="9b117-146">The following three examples show how absence is calculated in a profile that has flex periods.</span></span>

<span data-ttu-id="9b117-147">Í dæmunum er notuð eftirfarandi forstilling.</span><span class="sxs-lookup"><span data-stu-id="9b117-147">The examples use the following profile.</span></span>

| <span data-ttu-id="9b117-148">Innstimplun</span><span class="sxs-lookup"><span data-stu-id="9b117-148">Clock-in</span></span> | <span data-ttu-id="9b117-149">Staðaltími</span><span class="sxs-lookup"><span data-stu-id="9b117-149">Standard time</span></span>    | <span data-ttu-id="9b117-150">Hlé</span><span class="sxs-lookup"><span data-stu-id="9b117-150">Break</span></span>             | <span data-ttu-id="9b117-151">Staðaltími</span><span class="sxs-lookup"><span data-stu-id="9b117-151">Standard time</span></span> | <span data-ttu-id="9b117-152">Sveigjanlegt-</span><span class="sxs-lookup"><span data-stu-id="9b117-152">Flex-</span></span>        | <span data-ttu-id="9b117-153">Útstimplun</span><span class="sxs-lookup"><span data-stu-id="9b117-153">Clock-out</span></span> | <span data-ttu-id="9b117-154">Sveigjanlegt+</span><span class="sxs-lookup"><span data-stu-id="9b117-154">Flex+</span></span>        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| <span data-ttu-id="9b117-155">08:00</span><span class="sxs-lookup"><span data-stu-id="9b117-155">8 AM</span></span>     | <span data-ttu-id="9b117-156">09:30 til 11:30</span><span class="sxs-lookup"><span data-stu-id="9b117-156">9 AM to 11:30 AM</span></span> | <span data-ttu-id="9b117-157">11:30 til 12:00</span><span class="sxs-lookup"><span data-stu-id="9b117-157">11:30 AM to 12 PM</span></span> | <span data-ttu-id="9b117-158">12:00 til 15:00</span><span class="sxs-lookup"><span data-stu-id="9b117-158">12 PM to 3 PM</span></span> | <span data-ttu-id="9b117-159">15:00 til 16:00</span><span class="sxs-lookup"><span data-stu-id="9b117-159">3 PM to 4 PM</span></span> | <span data-ttu-id="9b117-160">16:00</span><span class="sxs-lookup"><span data-stu-id="9b117-160">4 PM</span></span>      | <span data-ttu-id="9b117-161">16: 00 til 18: 00</span><span class="sxs-lookup"><span data-stu-id="9b117-161">4 PM to 6 PM</span></span> |

### <a name="example-1-signing-out-during-a-flex--period"></a><span data-ttu-id="9b117-162">Dæmi 1: Útskráning á sveigjanlegum tíma</span><span class="sxs-lookup"><span data-stu-id="9b117-162">Example 1: Signing out during a Flex- period</span></span>

<span data-ttu-id="9b117-163">Starfsmaðurinn stimplar sig inn klukkan 08:00 og út klukkan 15:30.</span><span class="sxs-lookup"><span data-stu-id="9b117-163">The worker clocks in at 8:00 AM and clocks out at 3:30 PM.</span></span> <span data-ttu-id="9b117-164">Í þessu tilfelli, vegna þess að starfsmaður stimplar sig út á sveigjanlegum tíma, er engin fjarvera reiknuð og hálftíma er dreginn frá stöðu sveigjanlegs tíma starfsmannsins.</span><span class="sxs-lookup"><span data-stu-id="9b117-164">In this case, because the worker clocks out during a Flex- period, no absence is calculated, and half an hour is deducted from the worker's flex balance.</span></span>

### <a name="example-2-signing-out-in-during-standard-time-period"></a><span data-ttu-id="9b117-165">Dæmi 2: Innskráning á stöðluðum tíma</span><span class="sxs-lookup"><span data-stu-id="9b117-165">Example 2: Signing out in during Standard time period</span></span>

<span data-ttu-id="9b117-166">Starfsmaðurinn stimplar sig inn klukkan 08:00 og út klukkan 14:30.</span><span class="sxs-lookup"><span data-stu-id="9b117-166">The worker clocks in at 8:00 AM and clocks out at 2:30 PM.</span></span> <span data-ttu-id="9b117-167">Í þessu tilviki, vegna þess að starfsmaður klukkur út á stöðluðum tíma, er fjarvera reiknuð frá kl. 14:30 til 16:00 og 1,5 klst. fjarvist er skráð.</span><span class="sxs-lookup"><span data-stu-id="9b117-167">In this case, because the worker clocks out during the Standard time period, absence is calculated from 2:30 PM to 4 PM, and an absence period of 1.5 hours is registered.</span></span> <span data-ttu-id="9b117-168">Krafist er fjarvistarkóða fyrir það tímabil.</span><span class="sxs-lookup"><span data-stu-id="9b117-168">An absence code for that period is required.</span></span>

### <a name="example-3-signing-out-during-a-flex-period"></a><span data-ttu-id="9b117-169">Dæmi 3: Útskráning á sveigjanlegum+ tíma</span><span class="sxs-lookup"><span data-stu-id="9b117-169">Example 3: Signing out during a Flex+ period</span></span>

<span data-ttu-id="9b117-170">Starfsmaðurinn stimplar sig inn klukkan 08:00 og út klukkan 16:30.</span><span class="sxs-lookup"><span data-stu-id="9b117-170">The worker clocks in at 8:00 AM and clocks out at 4:30 PM.</span></span> <span data-ttu-id="9b117-171">Í þessu tilfelli, vegna þess að starfsmaður stimplar sig út á sveigjanlegum+ tíma, er engin fjarvera reiknuð og hálftíma er bætt við stöðu sveigjanlegs tíma starfsmannsins.</span><span class="sxs-lookup"><span data-stu-id="9b117-171">In this case, because the worker clocks out during a Flex+ period, no absence is calculated, and half an hour is added to the worker's flex balance.</span></span>

## <a name="absence-in-the-calculation-and-approval-process"></a><span data-ttu-id="9b117-172">Fjarvistir í útreiknings- og samþykktarferlinu</span><span class="sxs-lookup"><span data-stu-id="9b117-172">Absence in the calculation and approval process</span></span>

<span data-ttu-id="9b117-173">Skráningar vinnutíma starfsmanns þarf að reikna og samþykkja áður en hægt er að flytja þær í launakerfi sem greiðslur.</span><span class="sxs-lookup"><span data-stu-id="9b117-173">Worker time registrations must be calculated and approved before they can be transferred to a payroll system as pay items.</span></span>

<span data-ttu-id="9b117-174">Samþykkjandi getur breytt tímaskráningum starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="9b117-174">An approver can change a worker's time registrations.</span></span> <span data-ttu-id="9b117-175">Samþykkjandinn getur jafnvel breytt öllum fjarvistarkóðum sem starfsmaðurinn hefur skráð.</span><span class="sxs-lookup"><span data-stu-id="9b117-175">The approver can even change any absence that the worker has registered.</span></span> <span data-ttu-id="9b117-176">Ef samþykkjandinn fer inn í tímabil sem hefur fjarvistarkóða, er fjarvistarkóða þess tímabils ekki hnekkt af sjálfgefnum fjarvistarkóða frá færibreytum Tíma og mætinga.</span><span class="sxs-lookup"><span data-stu-id="9b117-176">If the approver manually enters a time period that has an absence code, the absence code for that period isn't overridden by the default absence code from the Time and attendance parameters.</span></span>

<span data-ttu-id="9b117-177">Starfsmaður stimplar sig t.d. inn klukkan 10:00 og velur fjarvistarkóða sem gefur til kynna að hann sé seinn.</span><span class="sxs-lookup"><span data-stu-id="9b117-177">For example, a worker clocks in at 10 AM and selects an absence code that indicates that she is late.</span></span> <span data-ttu-id="9b117-178">Seinna upplýsir starfsmaður yfirmann sinn um það að hann hafi þurft til læknis frá kl. 8:00 til 10:00.</span><span class="sxs-lookup"><span data-stu-id="9b117-178">Later, the worker informs her supervisor that she had a doctor's appointment from 8 AM to 10 AM.</span></span> <span data-ttu-id="9b117-179">Læknisheimsókn skal ekki leiða til frádráttar af launum starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="9b117-179">A doctor's appointment should not cause a deduction in the worker's pay.</span></span> <span data-ttu-id="9b117-180">Þar af leiðandi getur umsjónarmaðurinn í þessu tilviki leiðrétt tvær klukkustundir frá kl. 8:00 til 10:00 með því að slá handvirkt inn fjarvistarkóða sem gefur til kynna veikindi fyrir þessar tvær klukkustundir.</span><span class="sxs-lookup"><span data-stu-id="9b117-180">Therefore, in this case, the supervisor can adjust the two hours of absence from 8 AM to 10 AM by manually entering an absence code that indicates illness for those two hours.</span></span>

### <a name="calculate-and-approve-absence"></a><span data-ttu-id="9b117-181">Reikna út og samþykkja fjarvistir</span><span class="sxs-lookup"><span data-stu-id="9b117-181">Calculate and approve absence</span></span>

- <span data-ttu-id="9b117-182">Veldu **Tími mæting** &gt; **Skoða og samþykkja** &gt; **Samþykkja eða Reikna**.</span><span class="sxs-lookup"><span data-stu-id="9b117-182">Select **Time attendance** &gt; **Review and approve** &gt; **Approve or Calculate**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]