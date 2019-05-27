---
title: Stjórnun tíma og viðveru í Retail
description: Þessi efnisþáttur lýsir aðstæðum sem styður stjórnun á tíma og mætingu í Microsoft Dynamics 365 for Retail.
author: aamirallaqaband
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: JMGParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 62813
ms.assetid: 821994a6-cd29-45a3-a526-ce204064f080
ms.search.region: global
ms.search.industry: Retail
ms.author: aamiral
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 4c54909a02376a62a72a986e634649fa0ae54284
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567954"
---
# <a name="time-and-attendance-management-in-retail"></a><span data-ttu-id="3f4f4-103">Stjórnun tíma og viðveru í Retail</span><span class="sxs-lookup"><span data-stu-id="3f4f4-103">Time and attendance management in Retail</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3f4f4-104">Þessi efnisþáttur lýsir aðstæðum sem styður stjórnun á tíma og mætingu í Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="3f4f4-104">This topic describes the scenarios that are supported for time and attendance management in Microsoft Dynamics 365 for Retail.</span></span>

## <a name="manage-worker-setup-and-scheduling"></a><span data-ttu-id="3f4f4-105">Stjórna uppsetningu starfsmanns og áætlun</span><span class="sxs-lookup"><span data-stu-id="3f4f4-105">Manage worker setup and scheduling</span></span>

### <a name="initial-configuration"></a><span data-ttu-id="3f4f4-106"> Upphafleg skilgreining</span><span class="sxs-lookup"><span data-stu-id="3f4f4-106">Initial configuration</span></span>

- <span data-ttu-id="3f4f4-107">Keyrið leiðsagnarforrit grunnstillingar</span><span class="sxs-lookup"><span data-stu-id="3f4f4-107">Run the configuration wizard.</span></span>
- <span data-ttu-id="3f4f4-108">Skrá starfsmenn sem starfsmenn tímaskráningar.</span><span class="sxs-lookup"><span data-stu-id="3f4f4-108">Register workers as time registration workers.</span></span>

### <a name="plan-worker-schedules"></a><span data-ttu-id="3f4f4-109">Áætla áætlanir starfsmanns</span><span class="sxs-lookup"><span data-stu-id="3f4f4-109">Plan worker schedules</span></span>

- <span data-ttu-id="3f4f4-110">Nota forstillingar með vinnuáætlun</span><span class="sxs-lookup"><span data-stu-id="3f4f4-110">Apply profiles by using the work planner.</span></span> <span data-ttu-id="3f4f4-111">Nánari upplýsingar er að finna í [Nota forstillingar með vinnuáætlun](https://technet.microsoft.com/library/aa551234.aspx).</span><span class="sxs-lookup"><span data-stu-id="3f4f4-111">For more information, see [Apply profiles using work planner](https://technet.microsoft.com/library/aa551234.aspx).</span></span>

<span data-ttu-id="3f4f4-112">Nánari upplýsingar um skilgreiningarskref er að finna í [Uppsetning á tíma og viðveru](https://technet.microsoft.com/library/aa496971.aspx).</span><span class="sxs-lookup"><span data-stu-id="3f4f4-112">For information about the configuration steps, see [Setting up time and attendance](https://technet.microsoft.com/library/aa496971.aspx).</span></span>

### <a name="retail-specific-configuration"></a><span data-ttu-id="3f4f4-113">Skilgreining fyrir smásölu</span><span class="sxs-lookup"><span data-stu-id="3f4f4-113">Retail-specific configuration</span></span>

- <span data-ttu-id="3f4f4-114">Virkja virknireglu Stimpilklukku, fyrir starfsmenn sem á að virkja tímaskráningar fyrir.</span><span class="sxs-lookup"><span data-stu-id="3f4f4-114">Enable a functionality profile for Time Clock, for workers that you want to enable time registrations for.</span></span> <span data-ttu-id="3f4f4-115">Smellið á **Virkniforstilling sölustaðar** &gt; **Aðgerðir** &gt; **POS tímaskráning** &gt; **Virkja tímaskráningar**.</span><span class="sxs-lookup"><span data-stu-id="3f4f4-115">Click **POS functionality profiles** &gt; **Functions** &gt; **POS time registrations** &gt; **Enable time registrations**.</span></span>
- <span data-ttu-id="3f4f4-116">Skilgreina heimildaflokka sölustaðs (POS) til að virkja heimild fyrir Skoða færslur stimpilklukku.</span><span class="sxs-lookup"><span data-stu-id="3f4f4-116">Configure point of sale (POS) permissions groups to enable the View timeclock entries permission.</span></span> <span data-ttu-id="3f4f4-117">Þessi heimild gerir notanda kleift að skoða skráningar stimpilklukku annarra starfsmanna í versluninni (og úr öllum öðrum verslunum sem notandinn er tengdur, með aðsetursbókinni).</span><span class="sxs-lookup"><span data-stu-id="3f4f4-117">This permission lets a user view the time clock registrations of other workers in the store (and from any other store that the user is associated with, via the address book).</span></span> <span data-ttu-id="3f4f4-118">Þú gætir viljað virkja þessar heimildir fyrir hlutverk stjórnanda en ekki fyrir hlutverk gjaldkera .</span><span class="sxs-lookup"><span data-stu-id="3f4f4-118">You might want to enable this permission for a manager role but not for a cashier role.</span></span> <span data-ttu-id="3f4f4-119">Smellið á **Heimildaflokka sölustaðar** &gt; **Skoða færslur stimpilklukku**.</span><span class="sxs-lookup"><span data-stu-id="3f4f4-119">Click **POS permission groups** &gt; **View time clock entries**.</span></span>

## <a name="register-time"></a><span data-ttu-id="3f4f4-120">Tími á afgreiðslukassa</span><span class="sxs-lookup"><span data-stu-id="3f4f4-120">Register time</span></span>

### <a name="cashier-and-non-cashier-time-registrations"></a><span data-ttu-id="3f4f4-121">tímaskráningar Gjaldkera og þess sem er ekki gjaldkeri</span><span class="sxs-lookup"><span data-stu-id="3f4f4-121">Cashier and non-cashier time registrations</span></span>

- <span data-ttu-id="3f4f4-122">Á sölustað</span><span class="sxs-lookup"><span data-stu-id="3f4f4-122">On POS:</span></span>

    - <span data-ttu-id="3f4f4-123">Innstimplunaraðgerðir:</span><span class="sxs-lookup"><span data-stu-id="3f4f4-123">Clock-in operations:</span></span>

        - <span data-ttu-id="3f4f4-124">Skráið inn með aðgerð utan skúffu eða nýrri vakt.</span><span class="sxs-lookup"><span data-stu-id="3f4f4-124">Log on with a non-drawer operation or New shift.</span></span>
        - <span data-ttu-id="3f4f4-125">Velja aðgerð stimpilklukku</span><span class="sxs-lookup"><span data-stu-id="3f4f4-125">Select a Time Clock operation.</span></span>
        - <span data-ttu-id="3f4f4-126">Velja aðgerð sem óskað er:</span><span class="sxs-lookup"><span data-stu-id="3f4f4-126">Select a desired operation:</span></span>

            - <span data-ttu-id="3f4f4-127">Innstimplun</span><span class="sxs-lookup"><span data-stu-id="3f4f4-127">Clock-in</span></span>
            - <span data-ttu-id="3f4f4-128">Hlé fyrir vinnu</span><span class="sxs-lookup"><span data-stu-id="3f4f4-128">Break for Work</span></span>
            - <span data-ttu-id="3f4f4-129">Hádegishlé</span><span class="sxs-lookup"><span data-stu-id="3f4f4-129">Break for Lunch</span></span>
            - <span data-ttu-id="3f4f4-130">Útstimplun</span><span class="sxs-lookup"><span data-stu-id="3f4f4-130">Clock-out</span></span>

        <table>
        <thead>
        <tr>
        <th><span data-ttu-id="3f4f4-131">Núgildandi staða</span><span class="sxs-lookup"><span data-stu-id="3f4f4-131">Current state</span></span></th>
        <th><span data-ttu-id="3f4f4-132">Tiltækir valkostir</span><span class="sxs-lookup"><span data-stu-id="3f4f4-132">Available operations</span></span></th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td><span data-ttu-id="3f4f4-133">Innstimplun</span><span class="sxs-lookup"><span data-stu-id="3f4f4-133">Clock-in</span></span></td>
        <td>
        <ul>
        <li><span data-ttu-id="3f4f4-134">Hlé fyrir vinnu</span><span class="sxs-lookup"><span data-stu-id="3f4f4-134">Break for Work</span></span></li>
        <li><span data-ttu-id="3f4f4-135">Hádegishlé</span><span class="sxs-lookup"><span data-stu-id="3f4f4-135">Break for Lunch</span></span></li>
        <li><span data-ttu-id="3f4f4-136">Útstimplun</span><span class="sxs-lookup"><span data-stu-id="3f4f4-136">Clock-out</span></span></li>
        </ul>
        </td>
        </tr>
        <tr>
        <td><span data-ttu-id="3f4f4-137">Hlé fyrir vinnu</span><span class="sxs-lookup"><span data-stu-id="3f4f4-137">Break for Work</span></span></td>
        <td><span data-ttu-id="3f4f4-138">Innstimplun</span><span class="sxs-lookup"><span data-stu-id="3f4f4-138">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="3f4f4-139">Hádegishlé</span><span class="sxs-lookup"><span data-stu-id="3f4f4-139">Break for Lunch</span></span></td>
        <td><span data-ttu-id="3f4f4-140">Innstimplun</span><span class="sxs-lookup"><span data-stu-id="3f4f4-140">Clock-in</span></span></td>
        </tr>
        <tr>
        <td><span data-ttu-id="3f4f4-141">Útstimplun</span><span class="sxs-lookup"><span data-stu-id="3f4f4-141">Clock-out</span></span></td>
        <td><span data-ttu-id="3f4f4-142">Innstimplun</span><span class="sxs-lookup"><span data-stu-id="3f4f4-142">Clock-in</span></span></td>
        </tr>
        </tbody>
        </table>

        <span data-ttu-id="3f4f4-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span><span class="sxs-lookup"><span data-stu-id="3f4f4-143">[![TimeClockStates](./media/timeclockstates.png)](./media/timeclockstates.png)</span></span>

- <span data-ttu-id="3f4f4-144">Skoða staðfestingarskilaboðin og votta að núverandi tími verkþáttar sé réttur.</span><span class="sxs-lookup"><span data-stu-id="3f4f4-144">View the confirmation message, and validate that the current activity time is correct.</span></span>
- <span data-ttu-id="3f4f4-145">Færslubók:</span><span class="sxs-lookup"><span data-stu-id="3f4f4-145">Logbook:</span></span>

    - <span data-ttu-id="3f4f4-146">Smellið á **Kladdabók** til að skoða verkþátt stimpilklukku .</span><span class="sxs-lookup"><span data-stu-id="3f4f4-146">Click **Logbook** to view time clock activity.</span></span>
    - <span data-ttu-id="3f4f4-147">nota tímasíur til að velja mismunandi tímaglugga.</span><span class="sxs-lookup"><span data-stu-id="3f4f4-147">Use time filters to select different time windows.</span></span>
    - <span data-ttu-id="3f4f4-148">Ef þú vinnur á mörgum stöðum, sérð þú tímaskráningar þínum frá öllum verslunum þar sem þú skráðir tíma.</span><span class="sxs-lookup"><span data-stu-id="3f4f4-148">If you work at multiple store locations, you see your time registrations from all the stores where you recorded time.</span></span> <span data-ttu-id="3f4f4-149">Hægt er að nota síu verslunar til að skoða tímaskráningar úr valinni verslun.</span><span class="sxs-lookup"><span data-stu-id="3f4f4-149">You can use the store filter to view time registrations from a selected store.</span></span>

- <span data-ttu-id="3f4f4-150">Mismunandi tímabelti:</span><span class="sxs-lookup"><span data-stu-id="3f4f4-150">Different time zones:</span></span>

    - <span data-ttu-id="3f4f4-151">Ef þú skoðar tíma frá öðrum staðsetningum (fyrir færslubók gjaldkera , eða með því að nota **skoða færslur stimpilklukku** fyrir aðstæður stjórnanda ), og að staðsetning er í öðru tímabelti, eru tímafærslur sem þú sérð umbreytt í þinn staðartíma.</span><span class="sxs-lookup"><span data-stu-id="3f4f4-151">If you view time from a different location (for the cashier logbook, or by using **View timeclock entries** for a manager scenario), and that location is in a different time zone, the time records that you see are converted to your local time zone.</span></span> <span data-ttu-id="3f4f4-152">Til dæmis er stjórnandi fyrir tvær verslanir, ein í Arizona og önnur Nevada.</span><span class="sxs-lookup"><span data-stu-id="3f4f4-152">For example, you are a manager for two stores, one in Arizona and the other in Nevada.</span></span> <span data-ttu-id="3f4f4-153">Gjaldkeri skráir innstimplun við 9:00 F.HÁD</span><span class="sxs-lookup"><span data-stu-id="3f4f4-153">A cashier registers a clock-in at 9:00 A.M.</span></span> <span data-ttu-id="3f4f4-154">í Arizona.</span><span class="sxs-lookup"><span data-stu-id="3f4f4-154">in Arizona.</span></span> <span data-ttu-id="3f4f4-155">Á þeirri stundu er tími í Nevada 8:00 F.HÁD</span><span class="sxs-lookup"><span data-stu-id="3f4f4-155">At that moment, the time in Nevada is 8:00 A.M.</span></span> <span data-ttu-id="3f4f4-156">Þess vegna ef þú ert í versluninni í Nevada og skoðar færslur tímaskráningar, eru  tímaskráningarnar merktar sem F.HÁD 8</span><span class="sxs-lookup"><span data-stu-id="3f4f4-156">Therefore, if you are in the Nevada store and look at time registration records, the time registration is marked as 8 A.M.</span></span>

## <a name="view-worker-time-registrations"></a><span data-ttu-id="3f4f4-157">Stjórna tímaskráningu starfskrafts</span><span class="sxs-lookup"><span data-stu-id="3f4f4-157">View worker time registrations</span></span>

### <a name="view-worker-time-registrations-and-filter-by-store-or-activity-type"></a><span data-ttu-id="3f4f4-158">Skoða tímaskráningar starfsmanna og sía eftir verslun eða gerð verkþáttar</span><span class="sxs-lookup"><span data-stu-id="3f4f4-158">View worker time registrations, and filter by store or activity type</span></span>

<span data-ttu-id="3f4f4-159">Á sölustað</span><span class="sxs-lookup"><span data-stu-id="3f4f4-159">On POS:</span></span>

- <span data-ttu-id="3f4f4-160">Velja **skoða færslur stimpilklukku**</span><span class="sxs-lookup"><span data-stu-id="3f4f4-160">Select **View timeclock entries**.</span></span>
- <span data-ttu-id="3f4f4-161">Þú sérð skráningar tímaklukku fyrir aðgerðir fyrir  alla starfsmenn sem úthlutaðir eru á verslunum sem þú ert úthlutað til.</span><span class="sxs-lookup"><span data-stu-id="3f4f4-161">You see time clock registration activities from all workers that are assigned to the same stores that you're assigned to.</span></span>
- <span data-ttu-id="3f4f4-162">Hægt er að nota verkþáttargerð og síur verslunar til að sía tímaskráningar.</span><span class="sxs-lookup"><span data-stu-id="3f4f4-162">You can use the activity type and store filters to filter on time registrations.</span></span>

## <a name="process-and-manage-time-registrations"></a><span data-ttu-id="3f4f4-163">Vinna með og stjórna tímaskráningum</span><span class="sxs-lookup"><span data-stu-id="3f4f4-163">Process and manage time registrations</span></span>

<span data-ttu-id="3f4f4-164">Dynamics 365 for Retail notandi fylgist með verkflæðið til að reikna, samþykkja og flytja tímaskráningar í laun.</span><span class="sxs-lookup"><span data-stu-id="3f4f4-164">A Dynamics 365 for Retail user follows the workflow to calculate, approve, and transfer time registrations to payroll.</span></span>

### <a name="primary-operations"></a><span data-ttu-id="3f4f4-165">Aðalaðgerðir</span><span class="sxs-lookup"><span data-stu-id="3f4f4-165">Primary operations</span></span>

- <span data-ttu-id="3f4f4-166">Reikna</span><span class="sxs-lookup"><span data-stu-id="3f4f4-166">Calculate</span></span>
- <span data-ttu-id="3f4f4-167">Samþykkja</span><span class="sxs-lookup"><span data-stu-id="3f4f4-167">Approve</span></span>
- <span data-ttu-id="3f4f4-168">Senda í laun</span><span class="sxs-lookup"><span data-stu-id="3f4f4-168">Submit to payroll</span></span>

### <a name="other-common-operations"></a><span data-ttu-id="3f4f4-169">Aðrar algengar aðgerðir</span><span class="sxs-lookup"><span data-stu-id="3f4f4-169">Other common operations</span></span>

- <span data-ttu-id="3f4f4-170">Fjöldaútstimplun</span><span class="sxs-lookup"><span data-stu-id="3f4f4-170">Bulk Clock-out</span></span>
- <span data-ttu-id="3f4f4-171">Skrá Fjarvist</span><span class="sxs-lookup"><span data-stu-id="3f4f4-171">Register Absence</span></span>

<span data-ttu-id="3f4f4-172">Nánari upplýsingar um hvernig skal vinna með skráningu tíma og viðveru er að finna í [Vinna með skráningu tíma og viðveru](https://technet.microsoft.com/library/aa573180.aspx).</span><span class="sxs-lookup"><span data-stu-id="3f4f4-172">For more information about how to process time and attendance registrations, see [Process time and attendance registrations](https://technet.microsoft.com/library/aa573180.aspx).</span></span>
