---
title: Skilgreina og stjórna fríðindaáætlun
description: Mannauður býður upp á verkfæri til að setja upp og viðhalda fríðindi, frádráttur og launafyrirkomulag sem fyrirtæki býður upp á eða vinnur fyrir sína starfsmenn. Þessi skrá veitir upplýsingar um hvernig setja á upp stjórna fríðindum.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a7fe99d4982b8f35871b15e8049c39eb806e315c
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430027"
---
# <a name="define-and-manage-a-benefits-program"></a><span data-ttu-id="9f11d-104">Skilgreina og stjórna fríðindaáætlun</span><span class="sxs-lookup"><span data-stu-id="9f11d-104">Define and manage a benefits program</span></span>

<span data-ttu-id="9f11d-105">Human Resources býður upp á verkfæri til að setja upp og viðhalda fríðindi, frádráttur og launafyrirkomulag sem fyrirtæki býður upp á eða vinnur fyrir sína starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="9f11d-105">Human Resources provides a set of tools that can be used to set up and maintain benefits, deductions, and workers' compensation plans that an organization offers or processes for its workers.</span></span> <span data-ttu-id="9f11d-106">Þessi skrá veitir upplýsingar um hvernig setja á upp og stjórna fríðindum.</span><span class="sxs-lookup"><span data-stu-id="9f11d-106">This article provides information about how to set up and manage benefits.</span></span>

## <a name="benefit-setup"></a><span data-ttu-id="9f11d-107">Uppsetning á fríðindum</span><span class="sxs-lookup"><span data-stu-id="9f11d-107">Benefit setup</span></span>

<span data-ttu-id="9f11d-108">Áður en hægt er að skrá starfsmenn í fríðindi verður að stofna einingar fyrir hverja fríðinda.</span><span class="sxs-lookup"><span data-stu-id="9f11d-108">Before workers can be enrolled in benefits, you must create the elements of each benefit.</span></span> <span data-ttu-id="9f11d-109">Þessar einingar sameina svipuð fríðindaáætlanir og skilgreinið sjálfgefnar stillingar, eins og frádráttuartaxta og bókhaldsupplýsingum.</span><span class="sxs-lookup"><span data-stu-id="9f11d-109">These elements combine similar benefit plans and define default settings, such as deduction rates and accounting details.</span></span> <span data-ttu-id="9f11d-110">Margar af þessum stillingum er hægt að leiðrétta þegar starfsmenn eru skráðir síðar í fríðindi.</span><span class="sxs-lookup"><span data-stu-id="9f11d-110">Many of these settings can be adjusted when workers are later enrolled in the benefit.</span></span> <span data-ttu-id="9f11d-111">Fyrir hverja fríðindaáætlun getur fyrirtæki bjóða nokkrar skráningavalkosti eða starfsmaður fellt niður skráningu í áætlun.</span><span class="sxs-lookup"><span data-stu-id="9f11d-111">For each benefit plan, an organization can offer several enrollment options, or a worker can waive enrollment in the plan.</span></span> 

<span data-ttu-id="9f11d-112">[![Flæði fríðindaferla](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span><span class="sxs-lookup"><span data-stu-id="9f11d-112">[![Benefit process flow](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span></span>

## <a name="benefit-elements"></a><span data-ttu-id="9f11d-113">Fríðindaeiningar</span><span class="sxs-lookup"><span data-stu-id="9f11d-113">Benefit elements</span></span>

<span data-ttu-id="9f11d-114">Áður en byrjað er stofna fríðindi og skrá starfsmenn í þau verður að skilgreina einingar sem mynda fríðindi: gerð, áætlun, og valkosti.</span><span class="sxs-lookup"><span data-stu-id="9f11d-114">Before you begin to create benefits and enroll workers in them, you must define the elements that make up a benefit: the type, plan, and options.</span></span>

-   <span data-ttu-id="9f11d-115">**Gerð** – Safn áætlana fyrir tiltekin fríðindi, eins og læknisþjónusta eða bílastæði.</span><span class="sxs-lookup"><span data-stu-id="9f11d-115">**Type** – A collection of plans for a specific benefit, such as medical or parking.</span></span>
-   <span data-ttu-id="9f11d-116">**Áætlun** – Tiltekin fríðindi sem er fenginn samkvæmt samningi frá veitanda.</span><span class="sxs-lookup"><span data-stu-id="9f11d-116">**Plan** – A specific benefit that is contracted from a provider.</span></span>
-   <span data-ttu-id="9f11d-117">**Valkostur** – Tryggingarstig, svo sem starfsmaður eingöngu eða starfsmaður og maki.</span><span class="sxs-lookup"><span data-stu-id="9f11d-117">**Option** – The coverage level, such as employee only, or employee and spouse/partner.</span></span>

<span data-ttu-id="9f11d-118">Fyrir hverja fríðindagerð, eins og sjón eða tannlæknaþjónusta, getur fyrirtæki hægt bjóða einum eða fleiri áætlunum starfsmönnum sínum.</span><span class="sxs-lookup"><span data-stu-id="9f11d-118">For each type of benefit, such as vision or dental, an organization can offer one or more plans to its workers.</span></span> <span data-ttu-id="9f11d-119">Fyrir hverja áætlun getur fyrirtækið boðið mismunandi valkostir.</span><span class="sxs-lookup"><span data-stu-id="9f11d-119">For each plan, the organization can offer different options.</span></span> <span data-ttu-id="9f11d-120">Starfsmenn geta til dæmis kaupa viðbótar líftryggingar sem þekja eitt, tvö eða þrisvar sinnum árleg laun þeirra.</span><span class="sxs-lookup"><span data-stu-id="9f11d-120">For example, workers can buy additional term life insurance coverage at one, two, or three times their yearly salary.</span></span> <span data-ttu-id="9f11d-121">Hver samsetning áætlunar og valkosta verða fríðindi sem starfsmenn geta skrá sig í.</span><span class="sxs-lookup"><span data-stu-id="9f11d-121">Each combination of a plan and options becomes a benefit that workers can enroll in.</span></span> 

<span data-ttu-id="9f11d-122">[![fríðindamynd](./media/benefit-pic.png)](./media/benefit-pic.png)</span><span class="sxs-lookup"><span data-stu-id="9f11d-122">[![benefit pic](./media/benefit-pic.png)](./media/benefit-pic.png)</span></span>

## <a name="eligibility"></a><span data-ttu-id="9f11d-123">Hæfni</span><span class="sxs-lookup"><span data-stu-id="9f11d-123">Eligibility</span></span>
<span data-ttu-id="9f11d-124">Mörgum þáttum ákvarða hæfni starfsmanns fyrir mismunandi gerðir af fríðindum sem vinnuveitandi býður uppá.</span><span class="sxs-lookup"><span data-stu-id="9f11d-124">Many factors determine worker eligibility for the various types of benefits that an employer offers.</span></span> <span data-ttu-id="9f11d-125">Þegar fríðindi eru stofnuð í Dynamics 365 Human Resources er hægt að stilla hæfnigerð sem á við um fríðindin.</span><span class="sxs-lookup"><span data-stu-id="9f11d-125">When you create a benefit in Dynamics 365 Human Resources, you can set the type of eligibility that applies to that benefit.</span></span> 

<span data-ttu-id="9f11d-126">Hægt er að gera fríðindi tiltæk til allra starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="9f11d-126">You can make a benefit available to all workers.</span></span> <span data-ttu-id="9f11d-127">Til dæmis bjóða sum fyrirtækjum bílastæðapassa fyrir alla starfsmenn sem er hliðarfríðindi.</span><span class="sxs-lookup"><span data-stu-id="9f11d-127">For example, some companies offer parking passes to all employees as a fringe benefit.</span></span> <span data-ttu-id="9f11d-128">Þegar þú stofna þessi fríðindi, stillirðu hæfniskilyrði á **allt starfsfólk eru uppfyllir hæfniskilyrði**.</span><span class="sxs-lookup"><span data-stu-id="9f11d-128">When you create this benefit, you set the eligibility to **All workers are eligible**.</span></span> 

<span data-ttu-id="9f11d-129">Fyrir önnur fríðindi, svo sem frádráttur frá launum og skattheimtu, á hæfni ekki við.</span><span class="sxs-lookup"><span data-stu-id="9f11d-129">For other benefits, such as garnishments and tax levies, eligibility doesn't apply.</span></span> <span data-ttu-id="9f11d-130">Þegar þú búa til þessar tegundir af fríðindum, stillirðu hæfni til að **fara framhjá hæfniferli**</span><span class="sxs-lookup"><span data-stu-id="9f11d-130">Whey you create these types of benefits, you set the eligibility to **Bypass eligibility process**.</span></span> 

<span data-ttu-id="9f11d-131">Að lokum, fríðindahæfni getur byggt á reglum.</span><span class="sxs-lookup"><span data-stu-id="9f11d-131">Finally, benefit eligibility can be rule-based.</span></span> <span data-ttu-id="9f11d-132">Til dæmis býður fyrirtæki upp á tvær gerðir af fríðindum fyrir líftryggingar til starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="9f11d-132">For example, a company offers two types of life insurance benefit to employees.</span></span> <span data-ttu-id="9f11d-133">Yfirmenn á meðan starfsmanna eru hæfar fyrir eina líftryggingaáætlun á meðan allir aðrir starfsmanna í fullu starfi eru hæfar fyrir aðra líftryggingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="9f11d-133">Executive employees are eligible for one life insurance plan, whereas all other full-time employees are eligible for the other life insurance plan.</span></span> <span data-ttu-id="9f11d-134">Í Human Resources er hægt að stofna hæfnisreglu fríðinda til að finna alla yfirmenn og aðrar reglur til að finna aðra starfsmenn í fullu starfi og svo nota þær reglur fyrir viðeigandi fríðindi.</span><span class="sxs-lookup"><span data-stu-id="9f11d-134">In Human Resources, you can create a benefit eligibility rule to find all executive employees and another rule to find all other full-time employees, and then apply those rules to the appropriate benefit.</span></span>

## <a name="enrollment"></a><span data-ttu-id="9f11d-135">Skráning</span><span class="sxs-lookup"><span data-stu-id="9f11d-135">Enrollment</span></span>
<span data-ttu-id="9f11d-136">Eftir að fríðindi sem fyrirtækið býður upp hafa verið stofnuð og hæfni ákvörðuð, er hægt að skrá starfsmenn í fríðindi.</span><span class="sxs-lookup"><span data-stu-id="9f11d-136">After you've created the benefits that your organization offers and determined eligibility, you can enroll your workers in benefits.</span></span> <span data-ttu-id="9f11d-137">Hægt er að skrá einn starfsmanns í fríðindum, eða hægt er að skrá mörgum starfsmönnum í ein eða fleiri fríðindi í einni vinnslu.</span><span class="sxs-lookup"><span data-stu-id="9f11d-137">You can enroll a single worker in benefits, or you can enroll many workers in one or more benefits during a single process.</span></span> 

<span data-ttu-id="9f11d-138">Stundum hættir fyrirtæki að bjóða ákveðnum fríðindi.</span><span class="sxs-lookup"><span data-stu-id="9f11d-138">Sometimes, an organization stops offering certain benefits.</span></span> <span data-ttu-id="9f11d-139">Í þessu tilfelli þarf að uppfæra fríðindin og starfsmenn sem skráðir eru í þau.</span><span class="sxs-lookup"><span data-stu-id="9f11d-139">In this case, you must update the benefit and the workers who are enrolled in.</span></span> <span data-ttu-id="9f11d-140">Lokadagur fjöldafríðinda leyfir þér að breyta lokadegi fríðindi og innskráningu starfsmanns fyrir þau fríðindi á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="9f11d-140">Mass benefit expiration lets you change the expiration date of both a benefit and the worker enrollments for that benefit at the same time.</span></span> <span data-ttu-id="9f11d-141">Einnig er hægt að velja marga starfsmenn sem eru skráðir í fríðindi og breyta lokadagsetningu þekju þeirra.</span><span class="sxs-lookup"><span data-stu-id="9f11d-141">You can also select multiple workers who are enrolled in a benefit and change the ending date of their coverage.</span></span> 

<span data-ttu-id="9f11d-142">Á sama hátt leyfa fjöldafríðinda þér að breyta lokadegi fríðindi og innskráningu starfsmanns fyrir þau fríðindi á sama tíma ef þú ákveður að bjóta fríðindi lengur ef þú upprunalega áætlaðir.</span><span class="sxs-lookup"><span data-stu-id="9f11d-142">Similarly, mass benefit extension lets you extend the expiration date of both a benefit and the worker enrollments for that benefit if you decide to offer a benefit longer than you originally planned.</span></span>


