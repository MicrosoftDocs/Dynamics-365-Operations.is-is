---
title: "Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (10. september 2018)"
description: "Í þessu efnisatriði er lýst nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent Core HR."
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 7d4a049a44374276655dce696b5bbbe2e6f9fba9
ms.openlocfilehash: b41ce93c8ae93054d2b0d71340b99e0910d4510f
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---

# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-10-2018"></a><span data-ttu-id="ae363-103">Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (10. september 2018)</span><span class="sxs-lookup"><span data-stu-id="ae363-103">What's new or changed in Dynamics 365 for Talent Core HR (September 10, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ae363-104">**Smíði 8.1.138.0**</span><span class="sxs-lookup"><span data-stu-id="ae363-104">**Build 8.1.138.0**</span></span>

<span data-ttu-id="ae363-105">Í þessu efnisatriði er lýst nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent Core HR.</span><span class="sxs-lookup"><span data-stu-id="ae363-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 for Talent Core HR.</span></span>

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a><span data-ttu-id="ae363-106">Leyfa beiðni um frí (hálfir dagar) á ákveðnum tíma dags</span><span class="sxs-lookup"><span data-stu-id="ae363-106">Allow specific time of day on time-off requests (half days)</span></span>

<span data-ttu-id="ae363-107">Ef leyfi og fjarvera er sett upp þannig að frítími sé sendur inn í dögum, geturðu nú einnig virkjað skilgreiningu á hálfum dag.</span><span class="sxs-lookup"><span data-stu-id="ae363-107">If leave and absence is set up so that time off is submitted in days, you can now also enable a half-day definition.</span></span> <span data-ttu-id="ae363-108">Þá, þegar notendur leggja inn beiðni um frítíma, geta þeir tilgreint hvort þeir biðja um frí fyrri eða seinni hluta dags.</span><span class="sxs-lookup"><span data-stu-id="ae363-108">Then, when users submit time-off requests, they can specify whether they are requesting the first half or the second half of the day off.</span></span>

<span data-ttu-id="ae363-109">Sjálfgefið er að slökkt sé á þessum valkosti.</span><span class="sxs-lookup"><span data-stu-id="ae363-109">By default, this option is turned off.</span></span> <span data-ttu-id="ae363-110">Til að starfsmenn geti óskað eftir fríi fyrri eða seinni hluta dags verður þú að kveikja á þessum valkosti á **Leyfi og fjarvera** svæði fyrir færibreytur mannauðs.</span><span class="sxs-lookup"><span data-stu-id="ae363-110">For employees to request the first half or second half of the day off, you must turn on this option in the **Leave and absence** area of Human resources parameters.</span></span>

<span data-ttu-id="ae363-111">Öryggisréttindi fyrir þennan eiginleika er Vinna með færibreytur fyrir mannauð.</span><span class="sxs-lookup"><span data-stu-id="ae363-111">The security privilege for this feature is Maintain Human Resources Parameters.</span></span>

## <a name="validation-of-leave-and-absence-entries"></a><span data-ttu-id="ae363-112">Villuleit á færslum leyfis og fjarvista</span><span class="sxs-lookup"><span data-stu-id="ae363-112">Validation of leave and absence entries</span></span>

<span data-ttu-id="ae363-113">Það fer eftir því hvernig leyfi er stillt, starfsmenn sem reyna að leggja fram beiðni um frítíma sem er lengri en vinnudagur þeirra fá viðvörunarboð.</span><span class="sxs-lookup"><span data-stu-id="ae363-113">Depending on how leave is configured, employees who try to submit a time-off request that is longer than their work day receive a warning message.</span></span> <span data-ttu-id="ae363-114">Með öðrum orðum, þeir eru varaðir við ef þeir reyna að taka meira en heilan dag í frí fyrir sérhvern dag.</span><span class="sxs-lookup"><span data-stu-id="ae363-114">In other words, they are warned if they try to take more than a full day off on any given date.</span></span>

<span data-ttu-id="ae363-115">Það er alltaf kveikt á þessari villuleit.</span><span class="sxs-lookup"><span data-stu-id="ae363-115">This validation is always turned on.</span></span> <span data-ttu-id="ae363-116">Hvenær sem starfsmenn fara yfir dagsmörkin sem eru skilgreind, fá þeir viðvörun þegar þeir leggja fram beiðni um frí.</span><span class="sxs-lookup"><span data-stu-id="ae363-116">Any time that employees exceed the day threshold that is defined, they receive a warning in their time-off request.</span></span>

## <a name="additional-fields-for-conditional-statements-in-workflows"></a><span data-ttu-id="ae363-117">Viðbótarsvæði fyrir skilyrtar yfirlýsingar í verkflæði</span><span class="sxs-lookup"><span data-stu-id="ae363-117">Additional fields for conditional statements in workflows</span></span>

<span data-ttu-id="ae363-118">Viðbótarsvæðum hefur verið bætt við skilyrtar yfirlýsingar og staðgengla fyrir nokkur verkflæði í Core HR.</span><span class="sxs-lookup"><span data-stu-id="ae363-118">Additional fields have been added to conditional statements and placeholders for several workflows in Core HR.</span></span>

<span data-ttu-id="ae363-119">Eftirfarandi svæðum hefur verið bætt við verkflæði launa, starfsloka og flutninga:</span><span class="sxs-lookup"><span data-stu-id="ae363-119">The following fields have been added to the compensation, termination, and transfer workflows:</span></span>

- <span data-ttu-id="ae363-120">EmploymentType</span><span class="sxs-lookup"><span data-stu-id="ae363-120">EmploymentType</span></span>
- <span data-ttu-id="ae363-121">LegalEntity</span><span class="sxs-lookup"><span data-stu-id="ae363-121">LegalEntity</span></span>
- <span data-ttu-id="ae363-122">AdjustedWorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="ae363-122">AdjustedWorkerStartDate</span></span>
- <span data-ttu-id="ae363-123">EmployerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="ae363-123">EmployerNoticeAmount</span></span>
- <span data-ttu-id="ae363-124">EmployerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="ae363-124">EmployerUnitOfNotice</span></span>
- <span data-ttu-id="ae363-125">TransitionDate</span><span class="sxs-lookup"><span data-stu-id="ae363-125">TransitionDate</span></span>
- <span data-ttu-id="ae363-126">WorkerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="ae363-126">WorkerNoticeAmount</span></span>
- <span data-ttu-id="ae363-127">WorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="ae363-127">WorkerStartDate</span></span>
- <span data-ttu-id="ae363-128">WorkerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="ae363-128">WorkerUnitOfNotice</span></span>
- <span data-ttu-id="ae363-129">ProbationEndDate</span><span class="sxs-lookup"><span data-stu-id="ae363-129">ProbationEndDate</span></span>
- <span data-ttu-id="ae363-130">Staða</span><span class="sxs-lookup"><span data-stu-id="ae363-130">Position</span></span>
- <span data-ttu-id="ae363-131">Félag</span><span class="sxs-lookup"><span data-stu-id="ae363-131">Union</span></span>
- <span data-ttu-id="ae363-132">Deild</span><span class="sxs-lookup"><span data-stu-id="ae363-132">Department</span></span>
- <span data-ttu-id="ae363-133">PositionType</span><span class="sxs-lookup"><span data-stu-id="ae363-133">PositionType</span></span>
- <span data-ttu-id="ae363-134">CompLocation</span><span class="sxs-lookup"><span data-stu-id="ae363-134">CompLocation</span></span>
- <span data-ttu-id="ae363-135">Starfsheiti</span><span class="sxs-lookup"><span data-stu-id="ae363-135">Title</span></span>
- <span data-ttu-id="ae363-136">Starf</span><span class="sxs-lookup"><span data-stu-id="ae363-136">Job</span></span>
- <span data-ttu-id="ae363-137">JobType</span><span class="sxs-lookup"><span data-stu-id="ae363-137">JobType</span></span>
- <span data-ttu-id="ae363-138">JobFamily</span><span class="sxs-lookup"><span data-stu-id="ae363-138">JobFamily</span></span>
- <span data-ttu-id="ae363-139">JobFunction</span><span class="sxs-lookup"><span data-stu-id="ae363-139">JobFunction</span></span>

<span data-ttu-id="ae363-140">Eftirfarandi svæðum hefur verið bætt við verkflæðisstöðuna:</span><span class="sxs-lookup"><span data-stu-id="ae363-140">The following fields have been added to the position workflow:</span></span>

- <span data-ttu-id="ae363-141">Staða</span><span class="sxs-lookup"><span data-stu-id="ae363-141">Position</span></span>
- <span data-ttu-id="ae363-142">Félag</span><span class="sxs-lookup"><span data-stu-id="ae363-142">Union</span></span>
- <span data-ttu-id="ae363-143">Deild</span><span class="sxs-lookup"><span data-stu-id="ae363-143">Department</span></span>
- <span data-ttu-id="ae363-144">PositionType</span><span class="sxs-lookup"><span data-stu-id="ae363-144">PositionType</span></span>
- <span data-ttu-id="ae363-145">CompLocation</span><span class="sxs-lookup"><span data-stu-id="ae363-145">CompLocation</span></span>
- <span data-ttu-id="ae363-146">Starfsheiti</span><span class="sxs-lookup"><span data-stu-id="ae363-146">Title</span></span>
- <span data-ttu-id="ae363-147">Starf</span><span class="sxs-lookup"><span data-stu-id="ae363-147">Job</span></span>
- <span data-ttu-id="ae363-148">JobType</span><span class="sxs-lookup"><span data-stu-id="ae363-148">JobType</span></span>
- <span data-ttu-id="ae363-149">JobFamily</span><span class="sxs-lookup"><span data-stu-id="ae363-149">JobFamily</span></span>
- <span data-ttu-id="ae363-150">JobFunction</span><span class="sxs-lookup"><span data-stu-id="ae363-150">JobFunction</span></span>

<span data-ttu-id="ae363-151">Svæði í skilyrtum yfirlýsingum og staðgenglum eru tiltæk öllum notendum sem hafa aðgang til að stilla áðurnefnd verkflæði.</span><span class="sxs-lookup"><span data-stu-id="ae363-151">Fields in conditional statements and placeholders are available to all users who have access to configure the previously mentioned workflows.</span></span>

## <a name="navigation-to-attract-from-personnel-management"></a><span data-ttu-id="ae363-152">Farið í Attract frá starfsmannastjórnun</span><span class="sxs-lookup"><span data-stu-id="ae363-152">Navigation to Attract from personnel management</span></span>

<span data-ttu-id="ae363-153">Í starfsmannastjórnun, ef Attract hefur ekki verið sett upp, þá beinir kaflinn **Umsækjendur til að ráða** notendum að því að byrja með Attract í stað þess að sýna skilaboðin: „Við fundum ekkert til að sýna hér.“</span><span class="sxs-lookup"><span data-stu-id="ae363-153">In personnel management, if Attract hasn't been set up, the **Candidates to hire** section directs users to get started with Attract instead of showing the message, "We didn't find anything to show here."</span></span>

## <a name="other-changes"></a><span data-ttu-id="ae363-154">Aðrar breytingar</span><span class="sxs-lookup"><span data-stu-id="ae363-154">Other changes</span></span>

<span data-ttu-id="ae363-155">Þessi útgáfa inniheldur nokkrar villuleiðréttingar í viðbót:</span><span class="sxs-lookup"><span data-stu-id="ae363-155">This release includes several additional bug fixes:</span></span>

- <span data-ttu-id="ae363-156">Þegar verktaki er ráðinn ætti flipinn **Laun** ekki að vera tiltækur á beiðni/aðgerðasíðunni.</span><span class="sxs-lookup"><span data-stu-id="ae363-156">When a contractor is hired, the **Compensation** tab should not be available on the request/action page.</span></span>
- <span data-ttu-id="ae363-157">Á meðan uppsagnarbeiðni er í ferli er ekki hægt að halda áfram fyrr en allir áskildir reitir innihalda gögn.</span><span class="sxs-lookup"><span data-stu-id="ae363-157">During the request termination process, you can't continue until all required fields contain data.</span></span>
- <span data-ttu-id="ae363-158">Tekið hefur verið á vandamálum vegna birtingar á röðun og dagsetningu í greiningu starfsmannastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="ae363-158">Sort order and date display issues on the Personnel management analytics have been addressed.</span></span>

