---
title: Grunnstilla færibreytur leyfis og fjarvista
description: Skilgreindu færibreytur Human Resources fyrir leyfi og fjarvistir í Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 11/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c3a3f4a8a1fa0b5dbc4869f81f091cc66437e978
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056853"
---
# <a name="configure-leave-and-absence-parameters"></a><span data-ttu-id="97f09-103">Grunnstilla færibreytur leyfis og fjarvista</span><span class="sxs-lookup"><span data-stu-id="97f09-103">Configure leave and absence parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="97f09-104">Áður en þú setur upp áætlanir um leyfi og fjarvistir í Dynamics 365 Human Resources, það er góð hugmynd að staðfesta stillingar fyrir allar skyldar færibreytur Human Resources, þar á meðal:</span><span class="sxs-lookup"><span data-stu-id="97f09-104">Before you set up leave and absence plans in Dynamics 365 Human Resources, it's a good idea to verify the settings for all related human resources parameters, including:</span></span>

- <span data-ttu-id="97f09-105">Númeraröð fyrir leyfisbeiðnir</span><span class="sxs-lookup"><span data-stu-id="97f09-105">Number sequence for leave requests</span></span>
- <span data-ttu-id="97f09-106">Stillingar á Family and Medical Leave Act (lög um leyfi vegna fjölskyldu eða veikinda)</span><span class="sxs-lookup"><span data-stu-id="97f09-106">Family Medical and Leave Act (FMLA) settings</span></span>
- <span data-ttu-id="97f09-107">Stillingar fyrir sjálfsafgreiðslu starfsmanna vegna orlofs- og fjarverubeiðna</span><span class="sxs-lookup"><span data-stu-id="97f09-107">Employee self service settings for leave and absence requests</span></span>
- <span data-ttu-id="97f09-108">Færibreytur leyfis og fjarvista</span><span class="sxs-lookup"><span data-stu-id="97f09-108">Leave and absence parameters</span></span>

## <a name="view-and-change-human-resources-parameters"></a><span data-ttu-id="97f09-109">Skoða og breyta færibreytum Human Resources</span><span class="sxs-lookup"><span data-stu-id="97f09-109">View and change human resources parameters</span></span>

1. <span data-ttu-id="97f09-110">Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="97f09-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="97f09-111">Undir **Skipulag**, veldu **Færirbreytur Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="97f09-111">Under **Setup**, select **Human resources parameters**.</span></span>

3. <span data-ttu-id="97f09-112">Á **Númeraraðir** flipann, staðfestu **Númeraröð kóða** fyrir **Skildu eftir skilríki** og breyta eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="97f09-112">On the **Number sequences** tab, verify the **Number sequence code** for **Leave request ID** and change as necessary.</span></span> <span data-ttu-id="97f09-113">Þessi stilling ákvarðar röðina sem notuð er til að úthluta sjálfkrafa skilríkjum til að skilja eftir beiðnir.</span><span class="sxs-lookup"><span data-stu-id="97f09-113">This setting determines the sequence used for automatically assigning IDs to leave requests.</span></span>

4. <span data-ttu-id="97f09-114">Á **FMLA** flipanum, staðfestu FMLA stillingarnar og breyttu eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="97f09-114">On the **FMLA** tab, verify the FMLA settings and change as necessary.</span></span>

5. <span data-ttu-id="97f09-115">Á **Sjálfsafgreiðsla starfsmanna** flipann, tilgreinir hvort stjórnendur geti slegið inn leyfi og fjarvistarbeiðnir fyrir hönd starfsmanna sinna.</span><span class="sxs-lookup"><span data-stu-id="97f09-115">On the **Employee self service** tab, indicate whether managers can enter leave and absence requests on behalf of their employees.</span></span>

7. <span data-ttu-id="97f09-116">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="97f09-116">Select **Save**.</span></span>

>[!IMPORTANT]
><span data-ttu-id="97f09-117">Skoðun leyfis og fjarvista milli fyrirtækja er gert í forskoðun eins og er.</span><span class="sxs-lookup"><span data-stu-id="97f09-117">Viewing leave and absence across companies is currently in preview.</span></span> <span data-ttu-id="97f09-118">Þú þarft að virkja þetta í **sandkassaumhverfinu** til að birta valkostinn fyrir leyfi og fjarvistir.</span><span class="sxs-lookup"><span data-stu-id="97f09-118">You'll need to enable it in your **Sandbox** environment to display the option for leave and absence.</span></span> <span data-ttu-id="97f09-119">Frekari upplýsingar um virkjun forútgáfueiginleika er að finna í [Vinna með eiginleika](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="97f09-119">For more information about enabling preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="view-and-change-human-resources-shared-parameters"></a><span data-ttu-id="97f09-120">Skoða og breyta samnýttum færibreytum fyrir mannauð</span><span class="sxs-lookup"><span data-stu-id="97f09-120">View and change Human resources shared parameters</span></span>

1. <span data-ttu-id="97f09-121">Á síðunni **Starfsmannastjórnun** skal velja flipann **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="97f09-121">On the **Personnel management** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="97f09-122">Undir **Uppsetning**, veldu **Samnýttar færibreytur fyrir mannauð**.</span><span class="sxs-lookup"><span data-stu-id="97f09-122">Under **Setup**, select **Human resources shared parameters**.</span></span>

3. <span data-ttu-id="97f09-123">Á flipanum **Ítarlegur aðgangur** skal velja **Já** til að **Virkja yfirlit á milli fyrirtækja** til að heimila skoðun leyfis í öllu fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="97f09-123">On the **Advance access** tab, select **Yes** for **Enable cross company leave view** to allow leave to be viewed across company.</span></span>

4. <span data-ttu-id="97f09-124">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="97f09-124">Select **Save**.</span></span>

## <a name="view-and-change-leave-and-absence-parameters"></a><span data-ttu-id="97f09-125">Skoða og breyta færibreytum leyfis og fjarvista</span><span class="sxs-lookup"><span data-stu-id="97f09-125">View and change leave and absence parameters</span></span>

1. <span data-ttu-id="97f09-126">Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="97f09-126">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="97f09-127">Undir **Uppsetning** velurðu **Færibreytur leyfis og fjarvista**.</span><span class="sxs-lookup"><span data-stu-id="97f09-127">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="97f09-128">Á flipanum **Almennt** skal stilla eftirfarandi færibreytur:</span><span class="sxs-lookup"><span data-stu-id="97f09-128">On the **General** tab, set the following parameters:</span></span>
 
    - <span data-ttu-id="97f09-129">Stilltu **Eining fyrir leyfi og fjarvistir** á annaðhvort klukkutíma eða daga.</span><span class="sxs-lookup"><span data-stu-id="97f09-129">Set **Unit for leave and absence** to either hours or days.</span></span> <span data-ttu-id="97f09-130">Ef dagar, getur þú valið **Virkja skilgreining á hálfum degi** til að gera starfsmönnum kleift að velja annaðhvort fyrri eða seinni hluta dags í beiðnum sínum um frí.</span><span class="sxs-lookup"><span data-stu-id="97f09-130">If days, you can select **Enable half day definition** to allow employees to choose either first or second half of day in their time-off requests.</span></span> 

    - <span data-ttu-id="97f09-131">Veldu **Mánuðir gildistíma þjónustu** til að stilla hvenær uppsöfnunarhlutfallið tekur gildi vegna leyfisáætlana sem nota mánaðalega þjónustu.</span><span class="sxs-lookup"><span data-stu-id="97f09-131">Select **Months of service effective date** to set when the accrual rates take effect for leave plans using months of service.</span></span>

    - <span data-ttu-id="97f09-132">Veljið **Útreikningur á stöðu** til að birta stöður frá og með deginum í dag eða á uppsöfnunartímabilinu.</span><span class="sxs-lookup"><span data-stu-id="97f09-132">Select **Balance calculation** to display balances as of today or as of the accrual period.</span></span> <span data-ttu-id="97f09-133">Ef þú velur **Staðan frá deginum í dag** sýnir staðan samtölu allra uppsafnana, leiðréttinga og beiðna frá og með deginum í dag.</span><span class="sxs-lookup"><span data-stu-id="97f09-133">If you select **Balance as of today**, the balance displays the total of all accruals, adjustments, and requests as of today.</span></span> <span data-ttu-id="97f09-134">Ef þú velur **Staða frá og með uppsöfnunartímabili** sýnir staðan samtölu allra uppsafnana, leiðréttinga og beiðna frá og með uppsöfnunartímabilinu sem skilgreint er af tíðni í leyfisáætluninni.</span><span class="sxs-lookup"><span data-stu-id="97f09-134">If you select **Balance as of accrual period**, the balance displays the total of all accruals, adjustments, and requests as of the accrual period defined by the frequency in the leave plan.</span></span> 

    - <span data-ttu-id="97f09-135">Stillið upphafstímann á runuvinnslu gildistíma yfirfærslu.</span><span class="sxs-lookup"><span data-stu-id="97f09-135">Set the start time for the carry forward expiration batch job.</span></span>  
    
    - <span data-ttu-id="97f09-136">Veljið **Já** fyrir **Leyfa starfsmönnum að kaupa leyfisdaga** og **Leyfa starfsmönnum að selja leyfisdaga**.</span><span class="sxs-lookup"><span data-stu-id="97f09-136">Select **Yes** for **Allow employees to buy leave** and **Allow employees to sell leave**.</span></span> <span data-ttu-id="97f09-137">Ef valið er **Já** fyrir þessa valmöguleika er hægt að búa til reglur um kaup og sölu á leyfisdögum og gera starfsmönnum kleift að senda inn beiðnir um kaup og sölu á leyfisdögum.</span><span class="sxs-lookup"><span data-stu-id="97f09-137">If you select **Yes** for these options, you can create buy and sell leave policies and enable employees to submit buy and sell leave requests.</span></span>

## <a name="configure-calendar-parameters"></a><span data-ttu-id="97f09-138">Skilgreina færibreytur dagatals</span><span class="sxs-lookup"><span data-stu-id="97f09-138">Configure calendar parameters</span></span>

1. <span data-ttu-id="97f09-139">Á síðunni **Leyfi og fjarvera** velurðu flipann **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="97f09-139">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="97f09-140">Undir **Uppsetning** velurðu **Færibreytur leyfis og fjarvista**.</span><span class="sxs-lookup"><span data-stu-id="97f09-140">Under **Setup**, select **Leave and absence parameters**.</span></span>

3. <span data-ttu-id="97f09-141">Á **Dagatal** flipanum, skal breyta stillingu dagatals eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="97f09-141">On the **Calendar** tab, change calendar settings as necessary.</span></span>

4. <span data-ttu-id="97f09-142">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="97f09-142">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="97f09-143">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="97f09-143">See also</span></span>

- [<span data-ttu-id="97f09-144">Yfirlit yfir leyfi og fjarvistir</span><span class="sxs-lookup"><span data-stu-id="97f09-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]