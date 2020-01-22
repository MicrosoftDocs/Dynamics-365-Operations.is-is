---
title: Nýjungar eða breytingar í Dynamics 365 Talent - Core HR (10. september 2018)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: ff5d21a8a71b068a276bedaf6e4b9964adcb4027
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896751"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-10-2018"></a><span data-ttu-id="1208b-103">Nýjungar eða breytingar í Dynamics 365 Talent - Core HR (10. september 2018)</span><span class="sxs-lookup"><span data-stu-id="1208b-103">What's new or changed in Dynamics 365 Talent - Core HR (September 10, 2018)</span></span>

<span data-ttu-id="1208b-104">**Smíði 8.1.138.0**</span><span class="sxs-lookup"><span data-stu-id="1208b-104">**Build 8.1.138.0**</span></span>

<span data-ttu-id="1208b-105">Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Talent: Core HR.</span><span class="sxs-lookup"><span data-stu-id="1208b-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 Talent: Core HR.</span></span>

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a><span data-ttu-id="1208b-106">Leyfa beiðni um frí (hálfir dagar) á ákveðnum tíma dags</span><span class="sxs-lookup"><span data-stu-id="1208b-106">Allow specific time of day on time-off requests (half days)</span></span>

<span data-ttu-id="1208b-107">Ef leyfi og fjarvera er sett upp þannig að frítími sé sendur inn í dögum, geturðu nú einnig virkjað skilgreiningu á hálfum dag.</span><span class="sxs-lookup"><span data-stu-id="1208b-107">If leave and absence is set up so that time off is submitted in days, you can now also enable a half-day definition.</span></span> <span data-ttu-id="1208b-108">Þá, þegar notendur leggja inn beiðni um frítíma, geta þeir tilgreint hvort þeir biðja um frí fyrri eða seinni hluta dags.</span><span class="sxs-lookup"><span data-stu-id="1208b-108">Then, when users submit time-off requests, they can specify whether they are requesting the first half or the second half of the day off.</span></span>

<span data-ttu-id="1208b-109">Sjálfgefið er að slökkt sé á þessum valkosti.</span><span class="sxs-lookup"><span data-stu-id="1208b-109">By default, this option is turned off.</span></span> <span data-ttu-id="1208b-110">Til að starfsmenn geti óskað eftir fríi fyrri eða seinni hluta dags verður þú að kveikja á þessum valkosti á **Leyfi og fjarvera** svæði fyrir færibreytur mannauðs.</span><span class="sxs-lookup"><span data-stu-id="1208b-110">For employees to request the first half or second half of the day off, you must turn on this option in the **Leave and absence** area of Human resources parameters.</span></span>

<span data-ttu-id="1208b-111">Öryggisréttindi fyrir þennan eiginleika er Vinna með færibreytur fyrir mannauð.</span><span class="sxs-lookup"><span data-stu-id="1208b-111">The security privilege for this feature is Maintain Human Resources Parameters.</span></span>

## <a name="validation-of-leave-and-absence-entries"></a><span data-ttu-id="1208b-112">Villuleit á færslum leyfis og fjarvista</span><span class="sxs-lookup"><span data-stu-id="1208b-112">Validation of leave and absence entries</span></span>

<span data-ttu-id="1208b-113">Það fer eftir því hvernig leyfi er stillt, starfsmenn sem reyna að leggja fram beiðni um frítíma sem er lengri en vinnudagur þeirra fá viðvörunarboð.</span><span class="sxs-lookup"><span data-stu-id="1208b-113">Depending on how leave is configured, employees who try to submit a time-off request that is longer than their work day receive a warning message.</span></span> <span data-ttu-id="1208b-114">Með öðrum orðum, þeir eru varaðir við ef þeir reyna að taka meira en heilan dag í frí fyrir sérhvern dag.</span><span class="sxs-lookup"><span data-stu-id="1208b-114">In other words, they are warned if they try to take more than a full day off on any given date.</span></span>

<span data-ttu-id="1208b-115">Það er alltaf kveikt á þessari villuleit.</span><span class="sxs-lookup"><span data-stu-id="1208b-115">This validation is always turned on.</span></span> <span data-ttu-id="1208b-116">Hvenær sem starfsmenn fara yfir dagsmörkin sem eru skilgreind, fá þeir viðvörun þegar þeir leggja fram beiðni um frí.</span><span class="sxs-lookup"><span data-stu-id="1208b-116">Any time that employees exceed the day threshold that is defined, they receive a warning in their time-off request.</span></span>

## <a name="additional-fields-for-conditional-statements-in-workflows"></a><span data-ttu-id="1208b-117">Viðbótarsvæði fyrir skilyrtar yfirlýsingar í verkflæði</span><span class="sxs-lookup"><span data-stu-id="1208b-117">Additional fields for conditional statements in workflows</span></span>

<span data-ttu-id="1208b-118">Viðbótarsvæðum hefur verið bætt við skilyrtar yfirlýsingar og staðgengla fyrir nokkur verkflæði í Core HR.</span><span class="sxs-lookup"><span data-stu-id="1208b-118">Additional fields have been added to conditional statements and placeholders for several workflows in Core HR.</span></span>

<span data-ttu-id="1208b-119">Eftirfarandi svæðum hefur verið bætt við verkflæði launa, starfsloka og flutninga:</span><span class="sxs-lookup"><span data-stu-id="1208b-119">The following fields have been added to the compensation, termination, and transfer workflows:</span></span>

- <span data-ttu-id="1208b-120">EmploymentType</span><span class="sxs-lookup"><span data-stu-id="1208b-120">EmploymentType</span></span>
- <span data-ttu-id="1208b-121">LegalEntity</span><span class="sxs-lookup"><span data-stu-id="1208b-121">LegalEntity</span></span>
- <span data-ttu-id="1208b-122">AdjustedWorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="1208b-122">AdjustedWorkerStartDate</span></span>
- <span data-ttu-id="1208b-123">EmployerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="1208b-123">EmployerNoticeAmount</span></span>
- <span data-ttu-id="1208b-124">EmployerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="1208b-124">EmployerUnitOfNotice</span></span>
- <span data-ttu-id="1208b-125">TransitionDate</span><span class="sxs-lookup"><span data-stu-id="1208b-125">TransitionDate</span></span>
- <span data-ttu-id="1208b-126">WorkerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="1208b-126">WorkerNoticeAmount</span></span>
- <span data-ttu-id="1208b-127">WorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="1208b-127">WorkerStartDate</span></span>
- <span data-ttu-id="1208b-128">WorkerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="1208b-128">WorkerUnitOfNotice</span></span>
- <span data-ttu-id="1208b-129">ProbationEndDate</span><span class="sxs-lookup"><span data-stu-id="1208b-129">ProbationEndDate</span></span>
- <span data-ttu-id="1208b-130">Staða</span><span class="sxs-lookup"><span data-stu-id="1208b-130">Position</span></span>
- <span data-ttu-id="1208b-131">Félag</span><span class="sxs-lookup"><span data-stu-id="1208b-131">Union</span></span>
- <span data-ttu-id="1208b-132">Deild</span><span class="sxs-lookup"><span data-stu-id="1208b-132">Department</span></span>
- <span data-ttu-id="1208b-133">PositionType</span><span class="sxs-lookup"><span data-stu-id="1208b-133">PositionType</span></span>
- <span data-ttu-id="1208b-134">CompLocation</span><span class="sxs-lookup"><span data-stu-id="1208b-134">CompLocation</span></span>
- <span data-ttu-id="1208b-135">Starfsheiti</span><span class="sxs-lookup"><span data-stu-id="1208b-135">Title</span></span>
- <span data-ttu-id="1208b-136">Starf</span><span class="sxs-lookup"><span data-stu-id="1208b-136">Job</span></span>
- <span data-ttu-id="1208b-137">JobType</span><span class="sxs-lookup"><span data-stu-id="1208b-137">JobType</span></span>
- <span data-ttu-id="1208b-138">JobFamily</span><span class="sxs-lookup"><span data-stu-id="1208b-138">JobFamily</span></span>
- <span data-ttu-id="1208b-139">JobFunction</span><span class="sxs-lookup"><span data-stu-id="1208b-139">JobFunction</span></span>

<span data-ttu-id="1208b-140">Eftirfarandi svæðum hefur verið bætt við verkflæðisstöðuna:</span><span class="sxs-lookup"><span data-stu-id="1208b-140">The following fields have been added to the position workflow:</span></span>

- <span data-ttu-id="1208b-141">Staða</span><span class="sxs-lookup"><span data-stu-id="1208b-141">Position</span></span>
- <span data-ttu-id="1208b-142">Félag</span><span class="sxs-lookup"><span data-stu-id="1208b-142">Union</span></span>
- <span data-ttu-id="1208b-143">Deild</span><span class="sxs-lookup"><span data-stu-id="1208b-143">Department</span></span>
- <span data-ttu-id="1208b-144">PositionType</span><span class="sxs-lookup"><span data-stu-id="1208b-144">PositionType</span></span>
- <span data-ttu-id="1208b-145">CompLocation</span><span class="sxs-lookup"><span data-stu-id="1208b-145">CompLocation</span></span>
- <span data-ttu-id="1208b-146">Starfsheiti</span><span class="sxs-lookup"><span data-stu-id="1208b-146">Title</span></span>
- <span data-ttu-id="1208b-147">Starf</span><span class="sxs-lookup"><span data-stu-id="1208b-147">Job</span></span>
- <span data-ttu-id="1208b-148">JobType</span><span class="sxs-lookup"><span data-stu-id="1208b-148">JobType</span></span>
- <span data-ttu-id="1208b-149">JobFamily</span><span class="sxs-lookup"><span data-stu-id="1208b-149">JobFamily</span></span>
- <span data-ttu-id="1208b-150">JobFunction</span><span class="sxs-lookup"><span data-stu-id="1208b-150">JobFunction</span></span>

<span data-ttu-id="1208b-151">Svæði í skilyrtum yfirlýsingum og staðgenglum eru tiltæk öllum notendum sem hafa aðgang til að stilla áðurnefnd verkflæði.</span><span class="sxs-lookup"><span data-stu-id="1208b-151">Fields in conditional statements and placeholders are available to all users who have access to configure the previously mentioned workflows.</span></span>

## <a name="navigation-to-attract-from-personnel-management"></a><span data-ttu-id="1208b-152">Farið í Attract frá starfsmannastjórnun</span><span class="sxs-lookup"><span data-stu-id="1208b-152">Navigation to Attract from personnel management</span></span>

<span data-ttu-id="1208b-153">Í starfsmannastjórnun, ef Attract hefur ekki verið sett upp, þá beinir kaflinn **Umsækjendur til að ráða** notendum að því að byrja með Attract í stað þess að sýna skilaboðin: „Við fundum ekkert til að sýna hér.“</span><span class="sxs-lookup"><span data-stu-id="1208b-153">In personnel management, if Attract hasn't been set up, the **Candidates to hire** section directs users to get started with Attract instead of showing the message, "We didn't find anything to show here."</span></span>

## <a name="other-changes"></a><span data-ttu-id="1208b-154">Aðrar breytingar</span><span class="sxs-lookup"><span data-stu-id="1208b-154">Other changes</span></span>

<span data-ttu-id="1208b-155">Þessi útgáfa inniheldur nokkrar villuleiðréttingar í viðbót:</span><span class="sxs-lookup"><span data-stu-id="1208b-155">This release includes several additional bug fixes:</span></span>

- <span data-ttu-id="1208b-156">Þegar verktaki er ráðinn ætti flipinn **Laun** ekki að vera tiltækur á beiðni/aðgerðasíðunni.</span><span class="sxs-lookup"><span data-stu-id="1208b-156">When a contractor is hired, the **Compensation** tab should not be available on the request/action page.</span></span>
- <span data-ttu-id="1208b-157">Á meðan uppsagnarbeiðni er í ferli er ekki hægt að halda áfram fyrr en allir áskildir reitir innihalda gögn.</span><span class="sxs-lookup"><span data-stu-id="1208b-157">During the request termination process, you can't continue until all required fields contain data.</span></span>
- <span data-ttu-id="1208b-158">Tekið hefur verið á vandamálum vegna birtingar á röðun og dagsetningu í greiningu starfsmannastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="1208b-158">Sort order and date display issues on the Personnel management analytics have been addressed.</span></span>
