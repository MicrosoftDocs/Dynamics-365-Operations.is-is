---
title: Skilgreina hæfni
description: Hægt er að rekja hæfni starfsmanns í Dynamics 365 Human Resources. Einnig er hægt að tilgreina hæfni sem krafist er fyrir tiltekna vinnslu.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076560"
---
# <a name="configure-skills"></a><span data-ttu-id="466d7-104">Skilgreina hæfni</span><span class="sxs-lookup"><span data-stu-id="466d7-104">Configure skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="466d7-105">Hægt er að rekja hæfni starfsmanns í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="466d7-105">You can track your worker's skills in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="466d7-106">Einnig er hægt að tilgreina hæfni sem krafist er fyrir tiltekna vinnslu.</span><span class="sxs-lookup"><span data-stu-id="466d7-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="466d7-107">Dæmi um hæfni sem hægt er að rekja eru:</span><span class="sxs-lookup"><span data-stu-id="466d7-107">Examples of skills you can track include:</span></span>

- <span data-ttu-id="466d7-108">Eftirlitsyfirvald - getan til að hafa umsjón með vinnu annarra.</span><span class="sxs-lookup"><span data-stu-id="466d7-108">Supervisory – Ability to supervise the work of others.</span></span>
- <span data-ttu-id="466d7-109">Forysta - Geta til að leiða starfsmenn og fyriristækjasvið.</span><span class="sxs-lookup"><span data-stu-id="466d7-109">Leadership – Ability to lead employees and business domains.</span></span>
- <span data-ttu-id="466d7-110">Áætlanagerð – Geta til að horfa fram á við, til að búa til yfirlýst markmið og fylgja þeim eftir.</span><span class="sxs-lookup"><span data-stu-id="466d7-110">Planning – Ability to look ahead, to form vision statements, and to see them through.</span></span>
- <span data-ttu-id="466d7-111">HTML-Möguleika á að skrifa html-kóða.</span><span class="sxs-lookup"><span data-stu-id="466d7-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="466d7-112">Ef þú hefur ekki þegar sett upp hæfnisgerðir og matslíkön þarftu að bæta einhverjum við áður en hæfni er búin til.</span><span class="sxs-lookup"><span data-stu-id="466d7-112">If you haven't already set up skill types and rating models, you'll need to add some before creating skills.</span></span>

<span data-ttu-id="466d7-113">Eftirfarandi aðilar geta fært inn hæfni fyrir starfsmann:</span><span class="sxs-lookup"><span data-stu-id="466d7-113">The following people can enter skills for a worker:</span></span>

- <span data-ttu-id="466d7-114">Starfskraftar geta sjálfir skráð hæfni sína í sjálfsafgreiðslu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="466d7-114">Workers can enter skills for themselves in Employee self-service.</span></span> <span data-ttu-id="466d7-115">Þessi hæfni krefst samþykkis stjórnanda.</span><span class="sxs-lookup"><span data-stu-id="466d7-115">These skills require manager approval.</span></span>
- <span data-ttu-id="466d7-116">Stjórnendur geta fært inn hæfni fyrir starfsmenn sína.</span><span class="sxs-lookup"><span data-stu-id="466d7-116">Managers can enter skills for their workers.</span></span> <span data-ttu-id="466d7-117">Hægt er að stofna vinnuflæði sem samþykkir þessa hæfni sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="466d7-117">You can create a workflow that auto-approves these skills.</span></span>

## <a name="create-a-skill-type"></a><span data-ttu-id="466d7-118">Stofna hæfnisgerð</span><span class="sxs-lookup"><span data-stu-id="466d7-118">Create a skill type</span></span>

<span data-ttu-id="466d7-119">Hæfnisgerðir eru flokkar sem einstaka hæfni fellur undir, t.d. stjórnun eða sölu.</span><span class="sxs-lookup"><span data-stu-id="466d7-119">Skill types are categories that individual skills fall under, such as Administration or Sales.</span></span>

1. <span data-ttu-id="466d7-120">Á vinnusvæðinu **Þróun starfsmanns** skal velja **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="466d7-120">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="466d7-121">Undir **Uppsetning á hæfni** skal velja **Hæfnisgerðir**.</span><span class="sxs-lookup"><span data-stu-id="466d7-121">Under **Competency setup**, select **Skill types**.</span></span>

3. <span data-ttu-id="466d7-122">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="466d7-122">Select **New**.</span></span>

4. <span data-ttu-id="466d7-123">Ljúktu við eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="466d7-123">Complete the following fields:</span></span>

   - <span data-ttu-id="466d7-124">**Hæfnisgerð**: Færið inn heiti fyrir hæfnisgerðina.</span><span class="sxs-lookup"><span data-stu-id="466d7-124">**Skill type**: Enter a name for the skill type.</span></span>
   - <span data-ttu-id="466d7-125">**Lýsing**: Færið inn lýsingu á hæfnisgerðinni.</span><span class="sxs-lookup"><span data-stu-id="466d7-125">**Description**: Enter a description for the skill type.</span></span>

5. <span data-ttu-id="466d7-126">Veldu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="466d7-126">Select **Save**.</span></span>

## <a name="create-a-rating-model"></a><span data-ttu-id="466d7-127">Búa til einkunnalíkan</span><span class="sxs-lookup"><span data-stu-id="466d7-127">Create a rating model</span></span>

<span data-ttu-id="466d7-128">Matslíkön hjálpa til við að meta raunverulegt stig einstaklings af hæfni, stig sem þeir eiga að vinna að ná, eða þá hæfni sem krafist er fyrir vinnslu.</span><span class="sxs-lookup"><span data-stu-id="466d7-128">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill required for a job.</span></span> <span data-ttu-id="466d7-129">Hvert stig í einkunnalíkani fær úthlutað stuðli.</span><span class="sxs-lookup"><span data-stu-id="466d7-129">Each level in a rating model is assigned a factor.</span></span>

1. <span data-ttu-id="466d7-130">Á vinnusvæðinu **Þróun starfsmanns** skal velja **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="466d7-130">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="466d7-131">Undir **Uppsetning á hæfni** skal velja **Matslíkön**.</span><span class="sxs-lookup"><span data-stu-id="466d7-131">Under **Competency setup**, select **Rating models**.</span></span>

3. <span data-ttu-id="466d7-132">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="466d7-132">Select **New**.</span></span>

4. <span data-ttu-id="466d7-133">Ljúktu við eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="466d7-133">Complete the following fields:</span></span>

   - <span data-ttu-id="466d7-134">**Mat**: Færið inn heiti fyrir matslíkanið, t.d. **Hæfni**.</span><span class="sxs-lookup"><span data-stu-id="466d7-134">**Rating**: Enter a name for the rating model, such as **Skills**.</span></span>
   - <span data-ttu-id="466d7-135">**Lýsing**: Færið inn lýsingu á matslíkaninu, t.d. **Hæfnismat**.</span><span class="sxs-lookup"><span data-stu-id="466d7-135">**Description**: Enter a description for the rating model, such as **Skill ratings**.</span></span>

5. <span data-ttu-id="466d7-136">Í hlutanum **Stig** skal velja **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="466d7-136">In the **Levels** section, select **New**.</span></span> <span data-ttu-id="466d7-137">Fyrir hvert stig sem bæta á við þarf að ljúka eftirfarandi reitum:</span><span class="sxs-lookup"><span data-stu-id="466d7-137">For each level you want to add, complete the following fields:</span></span>

   - <span data-ttu-id="466d7-138">**Stig**: Færið inn heiti fyrir stigið.</span><span class="sxs-lookup"><span data-stu-id="466d7-138">**Level**: Enter a name for the level.</span></span>
   - <span data-ttu-id="466d7-139">**Lýsing**: Færið inn lýsingu fyrir stigið.</span><span class="sxs-lookup"><span data-stu-id="466d7-139">**Description**: Enter a description for the level.</span></span>
   - <span data-ttu-id="466d7-140">**Stuðull**: Færið inn gildi stuðuls frá 0-9.</span><span class="sxs-lookup"><span data-stu-id="466d7-140">**Factor**: Enter a factor value from 0-9.</span></span> <span data-ttu-id="466d7-141">Stuðlar hjálpa til við að staðla einkunnir vegna hæfni sem notast við mismunandi matslíkön.</span><span class="sxs-lookup"><span data-stu-id="466d7-141">Factors help normalize the scores of skills that use different rating models.</span></span> <span data-ttu-id="466d7-142">Hvert stig verður að hafa einkvæman stuðul.</span><span class="sxs-lookup"><span data-stu-id="466d7-142">Each level must have a unique factor.</span></span> <span data-ttu-id="466d7-143">Stig með hærri stuðul hafa meira vægi í einkunnalíkani.</span><span class="sxs-lookup"><span data-stu-id="466d7-143">Levels with higher factor values carry more weight in a rating model.</span></span>

   <span data-ttu-id="466d7-144">Haldið áfram að bæta stigum við eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="466d7-144">Continue adding levels as necessary.</span></span> <span data-ttu-id="466d7-145">Færa má inn allt að 10 stig fyrir hvert matslíkan.</span><span class="sxs-lookup"><span data-stu-id="466d7-145">You can enter up to 10 levels for each rating model.</span></span>

6. <span data-ttu-id="466d7-146">Veldu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="466d7-146">Select **Save**.</span></span>

## <a name="create-a-skill"></a><span data-ttu-id="466d7-147">Stofna hæfni</span><span class="sxs-lookup"><span data-stu-id="466d7-147">Create a skill</span></span>

<span data-ttu-id="466d7-148">Áður en hægt er að úthluta hæfni eða stofna leit að hæfnisskrá eða stofna hæfnisprófíl þarf að færa inn upplýsingar um hæfni á síðunni **Hæfni**.</span><span class="sxs-lookup"><span data-stu-id="466d7-148">Before you can assign a skill, or create a skill-mapping search or skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="466d7-149">Fyrir hverja hæfni er hægt að velja gerð hæfni og einkunnalíkan.</span><span class="sxs-lookup"><span data-stu-id="466d7-149">For each skill, you can select a skill type and a rating model.</span></span>

1. <span data-ttu-id="466d7-150">Á vinnusvæðinu **Þróun starfsmanns** skal velja **Tenglar**.</span><span class="sxs-lookup"><span data-stu-id="466d7-150">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="466d7-151">Undir **Uppsetning á hæfni** skal velja **Hæfni**.</span><span class="sxs-lookup"><span data-stu-id="466d7-151">Under **Competency setup**, select **Skills**.</span></span>

3. <span data-ttu-id="466d7-152">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="466d7-152">Select **New**.</span></span>

4. <span data-ttu-id="466d7-153">Ljúktu við eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="466d7-153">Complete the following fields:</span></span>

   - <span data-ttu-id="466d7-154">**Hæfni**: Færið inn heiti fyrir hæfnina.</span><span class="sxs-lookup"><span data-stu-id="466d7-154">**Skill**: Enter a name for the skill.</span></span>
   - <span data-ttu-id="466d7-155">**Lýsin**: Færið inn lýsingu á hæfninni.</span><span class="sxs-lookup"><span data-stu-id="466d7-155">**Description**: Enter a description for the skill.</span></span>
   - <span data-ttu-id="466d7-156">**Mat**: Veljið matslíkanið sem á að nota fyrir þessa hæfni.</span><span class="sxs-lookup"><span data-stu-id="466d7-156">**Rating**: Select the rating model you want to use for this skill.</span></span>
   - <span data-ttu-id="466d7-157">**Hæfnisgerð**: Veljið af listanum yfir hæfnisgerðir.</span><span class="sxs-lookup"><span data-stu-id="466d7-157">**Skill type**: Select from the list of skill types.</span></span>

5. <span data-ttu-id="466d7-158">Veldu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="466d7-158">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="466d7-159">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="466d7-159">See also</span></span>

[<span data-ttu-id="466d7-160">Slá inn hæfni</span><span class="sxs-lookup"><span data-stu-id="466d7-160">Enter skills</span></span>](hr-develop-enter-skills.md)<br>
[<span data-ttu-id="466d7-161">Kortleggja hæfni</span><span class="sxs-lookup"><span data-stu-id="466d7-161">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]