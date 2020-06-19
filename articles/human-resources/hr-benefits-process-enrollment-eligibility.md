---
title: Vinna úr fríðindahæfni
description: Þessi grein útskýrir hvernig á að keyra hæfisferlið fyrir innritun.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dfb7f13dce48f33c111af491918702763f7e3b8a
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429290"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="47815-103">Vinna úr fríðindahæfni</span><span class="sxs-lookup"><span data-stu-id="47815-103">Process enrollment eligibility</span></span>

<span data-ttu-id="47815-104">Þessi grein útskýrir hvernig á að keyra hæfisferlið fyrir innritun.</span><span class="sxs-lookup"><span data-stu-id="47815-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="47815-105">Í vinnusvæðinu **Fríðindastjórnun**, undir **Í vinnslu**, veldu **Vinnsla hæfis fyrir innritun**.</span><span class="sxs-lookup"><span data-stu-id="47815-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="47815-106">Í valmyndinni **Keyra hæfisferli við innritun**, tilgreindu gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="47815-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="47815-107">Svæði</span><span class="sxs-lookup"><span data-stu-id="47815-107">Field</span></span> | <span data-ttu-id="47815-108">Lýsing</span><span class="sxs-lookup"><span data-stu-id="47815-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="47815-109">**Skráningartímabil**</span><span class="sxs-lookup"><span data-stu-id="47815-109">**Enrollment period**</span></span> | <span data-ttu-id="47815-110">Innritunartímabilið til að vinna úr hæfi innritunar.</span><span class="sxs-lookup"><span data-stu-id="47815-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="47815-111">**Lögaðili**</span><span class="sxs-lookup"><span data-stu-id="47815-111">**Legal entity**</span></span> | <span data-ttu-id="47815-112">Lögaðilinn til að vinna úr hæfi innritunar fyrir.</span><span class="sxs-lookup"><span data-stu-id="47815-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="47815-113">**Starfskraftur**</span><span class="sxs-lookup"><span data-stu-id="47815-113">**Worker**</span></span> | <span data-ttu-id="47815-114">Starfskrafturinn til að vinna úr hæfi innritunar fyrir.</span><span class="sxs-lookup"><span data-stu-id="47815-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="47815-115">Ef þú skilur þennan reit eftir auðan verður vinnufærni allra starfsmanna afgreidd.</span><span class="sxs-lookup"><span data-stu-id="47815-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="47815-116">**Fríðindaáætlun**</span><span class="sxs-lookup"><span data-stu-id="47815-116">**Benefit plan**</span></span> | <span data-ttu-id="47815-117">Fríðindaáætlun til að vinna úr hæfi innritunar fyrir.</span><span class="sxs-lookup"><span data-stu-id="47815-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="47815-118">Ef þú vilt keyra ferlið í bakgrunni skaltu velja **Keyra í bakgrunni** og framkvæma eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="47815-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="47815-119">Færið inn upplýsingar fyrir ferlið.</span><span class="sxs-lookup"><span data-stu-id="47815-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="47815-120">Veldu til að setja upp endurtekið starf **Endurtekning**, sláðu inn upplýsingar um endurtekningu og veldu **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="47815-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="47815-121">Veldu til að setja upp atvinnuviðvörun **Viðvaranir**, veldu viðvaranir sem berast og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="47815-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="47815-122">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="47815-122">Select **OK**.</span></span> <span data-ttu-id="47815-123">Ferlið keyrir með breytunum sem þú stillir.</span><span class="sxs-lookup"><span data-stu-id="47815-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="47815-124">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="47815-124">Select **OK**.</span></span>

## <a name="view-process-results"></a><span data-ttu-id="47815-125">Skoða niðurstöður vinnslu</span><span class="sxs-lookup"><span data-stu-id="47815-125">View Process Results</span></span>

<span data-ttu-id="47815-126">Þessi grein útskýrir hvernig á að skoða niðurstöður vinnslu.</span><span class="sxs-lookup"><span data-stu-id="47815-126">This article explains how to view eligibility process results.</span></span>

1.  <span data-ttu-id="47815-127">Í vinnusvæðinu **Fríðindastjórnun**, undir **Í vinnslu**, veldu **Niðurstöður vinnslu**.</span><span class="sxs-lookup"><span data-stu-id="47815-127">In the **Benefits management** workspace, under **Processing**, select **Process results**.</span></span>

2.  <span data-ttu-id="47815-128">Í forminu **Afgreiða niðurstöður** eru eftirfarandi reitir tilgreindir:</span><span class="sxs-lookup"><span data-stu-id="47815-128">In the **Process results** form, the following fields are specified:</span></span>

   | <span data-ttu-id="47815-129">Svæði</span><span class="sxs-lookup"><span data-stu-id="47815-129">Field</span></span> | <span data-ttu-id="47815-130">lýsing</span><span class="sxs-lookup"><span data-stu-id="47815-130">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="47815-131">**Vinnslukenni**</span><span class="sxs-lookup"><span data-stu-id="47815-131">**Process ID**</span></span> | <span data-ttu-id="47815-132">Einstakt auðkenni fyrir samsetningu starfsmanns, lögaðila og vinnslu keyrslu.</span><span class="sxs-lookup"><span data-stu-id="47815-132">The unique ID for the combination of Worker, Legal entity, and process run.</span></span> |
   | <span data-ttu-id="47815-133">**Gerð ferlis**</span><span class="sxs-lookup"><span data-stu-id="47815-133">**Process type**</span></span> | <span data-ttu-id="47815-134">Þetta greinir ferlið sem var keyrt.</span><span class="sxs-lookup"><span data-stu-id="47815-134">This identifies the process that was run.</span></span> <span data-ttu-id="47815-135">Til dæmis:  Skráning.</span><span class="sxs-lookup"><span data-stu-id="47815-135">For example:  Enrollment.</span></span> |
   | <span data-ttu-id="47815-136">**Tímastilling**</span><span class="sxs-lookup"><span data-stu-id="47815-136">**Time stamp**</span></span> | <span data-ttu-id="47815-137">Tíminn sem hæfisferlið var keyrt.</span><span class="sxs-lookup"><span data-stu-id="47815-137">The time that the eligibility process was run.</span></span> |
   | <span data-ttu-id="47815-138">**Lögaðili**</span><span class="sxs-lookup"><span data-stu-id="47815-138">**Legal entity**</span></span> | <span data-ttu-id="47815-139">Lögaðilinn sem er tilgreindur við innritunarferlið.</span><span class="sxs-lookup"><span data-stu-id="47815-139">The legal entity specified during the enrollment process.</span></span> |
   | <span data-ttu-id="47815-140">**Starfsmaður**</span><span class="sxs-lookup"><span data-stu-id="47815-140">**Worker**</span></span> | <span data-ttu-id="47815-141">Starfsmaðurinn sem var unninn.</span><span class="sxs-lookup"><span data-stu-id="47815-141">The worker who was processed.</span></span> |
   | <span data-ttu-id="47815-142">\*\*Fyrirkomulag</span><span class="sxs-lookup"><span data-stu-id="47815-142">\*\*Plan</span></span> | <span data-ttu-id="47815-143">Fríðindaátlunin sem reynt var að taka þátt í.</span><span class="sxs-lookup"><span data-stu-id="47815-143">The Benefit plan that enrollment was attempted for.</span></span> |
   | <span data-ttu-id="47815-144">**Hæfnisregla**</span><span class="sxs-lookup"><span data-stu-id="47815-144">**Eligibility rule**</span></span> | <span data-ttu-id="47815-145">Hæfisreglan sem var afgreidd.</span><span class="sxs-lookup"><span data-stu-id="47815-145">The eligibility rule that was processed.</span></span> <span data-ttu-id="47815-146">Ef villa kom upp áður en hæfni var keyrð verður þetta tómt.</span><span class="sxs-lookup"><span data-stu-id="47815-146">If an error was encountered before eligibility was run, this will be blank.</span></span> <span data-ttu-id="47815-147">Til dæmis: Ef ekki hafa verið skilgreindar bætur fyrir starfsmann mun hæfisferlið ekki keyra og þessi reitur verður skilinn auður.</span><span class="sxs-lookup"><span data-stu-id="47815-147">For example: If compensation hasn't been defined for a worker, the eligibility process won't run, and this field will be left blank.</span></span> |
   | <span data-ttu-id="47815-148">**Niðurstöður**</span><span class="sxs-lookup"><span data-stu-id="47815-148">**Result status**</span></span> | <span data-ttu-id="47815-149">Þetta verður gjaldgeng eða óhæfur.</span><span class="sxs-lookup"><span data-stu-id="47815-149">This will be Eligible or Ineligible.</span></span> <span data-ttu-id="47815-150">Niðurstaðan verður óhæf ef starfsmaðurinn uppfyllti ekki skilyrði fyrir hæfisreglu, ef starfsmanninn vantar nauðsynlegar upplýsingar, svo sem launatíðni eða fastar bætur, eða ef það vantar upplýsingar í bótakerfið sem kemur í veg fyrir að starfsmenn séu skráðir.</span><span class="sxs-lookup"><span data-stu-id="47815-150">The result status will be Ineligible if the worker didn’t meet the eligibility rule criteria, if the worker is missing required information such as a pay frequency or fixed compensation, or if there is information missing on the benefit plan that prevents workers from being enrolled.</span></span> |
   | <span data-ttu-id="47815-151">**Niðurstöðuskilaboð**</span><span class="sxs-lookup"><span data-stu-id="47815-151">**Result message**</span></span> | <span data-ttu-id="47815-152">Gefur til kynna hvers vegna starfsmaður er óhæfur til fríðindaáætlunar eða ef hæfisreglan var samþykkt.</span><span class="sxs-lookup"><span data-stu-id="47815-152">Indicates why a worker is ineligible for a benefit plan or if the eligibility rule passed.</span></span> |

