---
title: Vinna úr fríðindahæfni
description: Þessi grein útskýrir hvernig á að keyra hæfisferlið fyrir innritun.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0344c48460a7d1540481e09ba106526e119de72b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009357"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="6ed2e-103">Vinna úr fríðindahæfni</span><span class="sxs-lookup"><span data-stu-id="6ed2e-103">Process enrollment eligibility</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="6ed2e-104">Þessi grein útskýrir hvernig á að keyra hæfisferlið fyrir innritun.</span><span class="sxs-lookup"><span data-stu-id="6ed2e-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="6ed2e-105">Í vinnusvæðinu **Fríðindastjórnun**, undir **Í vinnslu**, veldu **Vinnsla hæfis fyrir innritun**.</span><span class="sxs-lookup"><span data-stu-id="6ed2e-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="6ed2e-106">Í valmyndinni **Keyra hæfisferli við innritun**, tilgreindu gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="6ed2e-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="6ed2e-107">Svæði</span><span class="sxs-lookup"><span data-stu-id="6ed2e-107">Field</span></span> | <span data-ttu-id="6ed2e-108">Lýsing</span><span class="sxs-lookup"><span data-stu-id="6ed2e-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="6ed2e-109">Skráningartímabil</span><span class="sxs-lookup"><span data-stu-id="6ed2e-109">Enrollment period</span></span> | <span data-ttu-id="6ed2e-110">Innritunartímabilið til að vinna úr hæfi innritunar.</span><span class="sxs-lookup"><span data-stu-id="6ed2e-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="6ed2e-111">Lögaðili</span><span class="sxs-lookup"><span data-stu-id="6ed2e-111">Legal entity</span></span> | <span data-ttu-id="6ed2e-112">Lögaðilinn til að vinna úr hæfi innritunar fyrir.</span><span class="sxs-lookup"><span data-stu-id="6ed2e-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="6ed2e-113">Starfskraftur</span><span class="sxs-lookup"><span data-stu-id="6ed2e-113">Worker</span></span> | <span data-ttu-id="6ed2e-114">Starfskrafturinn til að vinna úr hæfi innritunar fyrir.</span><span class="sxs-lookup"><span data-stu-id="6ed2e-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="6ed2e-115">Ef þú skilur þennan reit eftir auðan verður vinnufærni allra starfsmanna afgreidd.</span><span class="sxs-lookup"><span data-stu-id="6ed2e-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="6ed2e-116">Fríðindaáætlun</span><span class="sxs-lookup"><span data-stu-id="6ed2e-116">Benefit plan</span></span> | <span data-ttu-id="6ed2e-117">Fríðindaáætlun til að vinna úr hæfi innritunar fyrir.</span><span class="sxs-lookup"><span data-stu-id="6ed2e-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="6ed2e-118">Ef þú vilt keyra ferlið í bakgrunni skaltu velja **Keyra í bakgrunni** og framkvæma eftirfarandi verk:</span><span class="sxs-lookup"><span data-stu-id="6ed2e-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="6ed2e-119">Færið inn upplýsingar fyrir ferlið.</span><span class="sxs-lookup"><span data-stu-id="6ed2e-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="6ed2e-120">Veldu til að setja upp endurtekið starf **Endurtekning**, sláðu inn upplýsingar um endurtekningu og veldu **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6ed2e-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="6ed2e-121">Veldu til að setja upp atvinnuviðvörun **Viðvaranir**, veldu viðvaranir sem berast og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6ed2e-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="6ed2e-122">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6ed2e-122">Select **OK**.</span></span> <span data-ttu-id="6ed2e-123">Ferlið keyrir með breytunum sem þú stillir.</span><span class="sxs-lookup"><span data-stu-id="6ed2e-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="6ed2e-124">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="6ed2e-124">Select **OK**.</span></span>
