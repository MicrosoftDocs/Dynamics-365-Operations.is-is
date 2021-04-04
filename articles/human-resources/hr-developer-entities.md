---
title: Dataverse töflur
description: Microsoft Dynamics 365 Human Resources notar Dataverse til að gera mögulegt atburðarás fyrir stækkun og samþættingu.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: caf8b0a5d0b24ef3619f45a6d236acae6d29c8ab
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465223"
---
# <a name="dataverse-tables"></a><span data-ttu-id="26c33-103">Dataverse töflur</span><span class="sxs-lookup"><span data-stu-id="26c33-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="26c33-104">Microsoft Dynamics 365 Human Resources notar Dataverse til að gera mögulegt atburðarás fyrir stækkun og samþættingu.</span><span class="sxs-lookup"><span data-stu-id="26c33-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="26c33-105">Mannauðseiningar samsvara Dataverse töflum.</span><span class="sxs-lookup"><span data-stu-id="26c33-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="26c33-106">Frekari upplýsingar um Dataverse (áður Common Data Service) og uppfærslur á hugtökum er að finna í [Hvað er Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="26c33-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="26c33-107">Eftirfarandi Dataverse-töflur eru í boði sem byggja á einingum Human Resources.</span><span class="sxs-lookup"><span data-stu-id="26c33-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="26c33-108">Fríðindatöflur</span><span class="sxs-lookup"><span data-stu-id="26c33-108">Benefit tables</span></span>

| <span data-ttu-id="26c33-109">Nafn</span><span class="sxs-lookup"><span data-stu-id="26c33-109">Name</span></span> | <span data-ttu-id="26c33-110">Tafla</span><span class="sxs-lookup"><span data-stu-id="26c33-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="26c33-111">Útreikningstíðni fríðinda</span><span class="sxs-lookup"><span data-stu-id="26c33-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="26c33-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="26c33-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="26c33-113">Útreikningsíðni fríðinda á launatímabili</span><span class="sxs-lookup"><span data-stu-id="26c33-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="26c33-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="26c33-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="26c33-115">Hlutfall útreikninga fyrir fríðindi</span><span class="sxs-lookup"><span data-stu-id="26c33-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="26c33-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="26c33-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="26c33-117">Upplýsingar um hlutfall útreikninga fyrir fríðindi</span><span class="sxs-lookup"><span data-stu-id="26c33-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="26c33-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="26c33-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="26c33-119">Fríðindavalkostur</span><span class="sxs-lookup"><span data-stu-id="26c33-119">Benefit Option</span></span> | <span data-ttu-id="26c33-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="26c33-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="26c33-121">Fríðindaáætlun</span><span class="sxs-lookup"><span data-stu-id="26c33-121">Benefit Plan</span></span> | <span data-ttu-id="26c33-122">cdm_benefitplan (Ekki virkjað fyrir sérsniðinn reitastuðning)</span><span class="sxs-lookup"><span data-stu-id="26c33-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="26c33-123">Gerð fríðinda</span><span class="sxs-lookup"><span data-stu-id="26c33-123">Benefit Type</span></span> | <span data-ttu-id="26c33-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="26c33-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="26c33-125">Verkefnatöflur viðskiptaferlis</span><span class="sxs-lookup"><span data-stu-id="26c33-125">Business process tasks tables</span></span>

| <span data-ttu-id="26c33-126">Nafn</span><span class="sxs-lookup"><span data-stu-id="26c33-126">Name</span></span> | <span data-ttu-id="26c33-127">Tafla</span><span class="sxs-lookup"><span data-stu-id="26c33-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="26c33-128">Dagatal viðskiptaferlis</span><span class="sxs-lookup"><span data-stu-id="26c33-128">Business Process Calendar</span></span> | <span data-ttu-id="26c33-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="26c33-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="26c33-130">Hópverkefni viðskiptaferlis</span><span class="sxs-lookup"><span data-stu-id="26c33-130">Business Process Group Assignment</span></span> | <span data-ttu-id="26c33-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="26c33-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="26c33-132">Verkhópur viðskiptaferlissafns</span><span class="sxs-lookup"><span data-stu-id="26c33-132">Business Process Library Task Group</span></span> | <span data-ttu-id="26c33-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="26c33-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="26c33-134">Stig viðskiptaferlis</span><span class="sxs-lookup"><span data-stu-id="26c33-134">Business Process Stage</span></span> | <span data-ttu-id="26c33-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="26c33-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="26c33-136">Haus gátlistasniðmáts</span><span class="sxs-lookup"><span data-stu-id="26c33-136">Checklist Template Header</span></span> | <span data-ttu-id="26c33-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="26c33-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="26c33-138">Verkefni gátlistasniðmáts</span><span class="sxs-lookup"><span data-stu-id="26c33-138">Checklist Template Task</span></span> | <span data-ttu-id="26c33-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="26c33-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="26c33-140">Launatöflur</span><span class="sxs-lookup"><span data-stu-id="26c33-140">Compensation tables</span></span>

| <span data-ttu-id="26c33-141">Nafn</span><span class="sxs-lookup"><span data-stu-id="26c33-141">Name</span></span> | <span data-ttu-id="26c33-142">Tafla</span><span class="sxs-lookup"><span data-stu-id="26c33-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="26c33-143">Fyrirkomulag fastra launa</span><span class="sxs-lookup"><span data-stu-id="26c33-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="26c33-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="26c33-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="26c33-145">Launanet</span><span class="sxs-lookup"><span data-stu-id="26c33-145">Compensation Grid</span></span> | <span data-ttu-id="26c33-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="26c33-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="26c33-147">Launastig</span><span class="sxs-lookup"><span data-stu-id="26c33-147">Compensation Level</span></span> | <span data-ttu-id="26c33-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="26c33-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="26c33-149">Greiðslutíðni launa</span><span class="sxs-lookup"><span data-stu-id="26c33-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="26c33-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="26c33-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="26c33-151">Uppsetning á tilvísunarpunkti launa</span><span class="sxs-lookup"><span data-stu-id="26c33-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="26c33-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="26c33-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="26c33-153">Setja upp línu tilvísunarpunkts launa</span><span class="sxs-lookup"><span data-stu-id="26c33-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="26c33-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="26c33-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="26c33-155">Launasvæði</span><span class="sxs-lookup"><span data-stu-id="26c33-155">Compensation Region</span></span> | <span data-ttu-id="26c33-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="26c33-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="26c33-157">Launaskipulag</span><span class="sxs-lookup"><span data-stu-id="26c33-157">Compensation Structure</span></span> | <span data-ttu-id="26c33-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="26c33-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="26c33-159">Fyrirkomulag breytilegra uppbóta</span><span class="sxs-lookup"><span data-stu-id="26c33-159">Compensation Variable Plan</span></span> | <span data-ttu-id="26c33-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="26c33-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="26c33-161">Fyrirkomulagsstig breytilegra uppbóta</span><span class="sxs-lookup"><span data-stu-id="26c33-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="26c33-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="26c33-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="26c33-163">Fyrirkomulagsgerð breytilegra uppbóta</span><span class="sxs-lookup"><span data-stu-id="26c33-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="26c33-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="26c33-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="26c33-165">Fast launatilvik</span><span class="sxs-lookup"><span data-stu-id="26c33-165">Fixed Compensation Event</span></span> | <span data-ttu-id="26c33-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="26c33-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="26c33-167">Veitiregla</span><span class="sxs-lookup"><span data-stu-id="26c33-167">Vesting Rule</span></span> | <span data-ttu-id="26c33-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="26c33-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="26c33-169">Föst laun starfskrafts</span><span class="sxs-lookup"><span data-stu-id="26c33-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="26c33-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="26c33-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="26c33-171">Fyrirtækistöflur</span><span class="sxs-lookup"><span data-stu-id="26c33-171">Organization tables</span></span>

| <span data-ttu-id="26c33-172">Nafn</span><span class="sxs-lookup"><span data-stu-id="26c33-172">Name</span></span> | <span data-ttu-id="26c33-173">Tafla</span><span class="sxs-lookup"><span data-stu-id="26c33-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="26c33-174">Deild</span><span class="sxs-lookup"><span data-stu-id="26c33-174">Department</span></span> | <span data-ttu-id="26c33-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="26c33-175">cdm_department</span></span> |
| <span data-ttu-id="26c33-176">Ráðning</span><span class="sxs-lookup"><span data-stu-id="26c33-176">Employment</span></span> | <span data-ttu-id="26c33-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="26c33-177">cdm_employment</span></span> |
| <span data-ttu-id="26c33-178">Fyrirt.  </span><span class="sxs-lookup"><span data-stu-id="26c33-178">Company</span></span> | <span data-ttu-id="26c33-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="26c33-179">cdm_company</span></span> |
| <span data-ttu-id="26c33-180">Vinnsla</span><span class="sxs-lookup"><span data-stu-id="26c33-180">Job</span></span> | <span data-ttu-id="26c33-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="26c33-181">cdm_job</span></span> |
| <span data-ttu-id="26c33-182">Starfshlutverk</span><span class="sxs-lookup"><span data-stu-id="26c33-182">Job Function</span></span> | <span data-ttu-id="26c33-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="26c33-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="26c33-184">Staða starfs</span><span class="sxs-lookup"><span data-stu-id="26c33-184">Job Position</span></span> | <span data-ttu-id="26c33-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="26c33-185">cdm_jobposition</span></span> |
| <span data-ttu-id="26c33-186">Gerð stöðu</span><span class="sxs-lookup"><span data-stu-id="26c33-186">Position Type</span></span> | <span data-ttu-id="26c33-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="26c33-187">cdm_positiontype</span></span> |
| <span data-ttu-id="26c33-188">Stöðuúthlutun starfskrafts</span><span class="sxs-lookup"><span data-stu-id="26c33-188">Position Worker Assignment</span></span> | <span data-ttu-id="26c33-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="26c33-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="26c33-190">Vídd stöðu starfs</span><span class="sxs-lookup"><span data-stu-id="26c33-190">Job Position Dimension</span></span> | <span data-ttu-id="26c33-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="26c33-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="26c33-192">Starfsgerð</span><span class="sxs-lookup"><span data-stu-id="26c33-192">Job Type</span></span> | <span data-ttu-id="26c33-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="26c33-193">cdm_jobtype</span></span> |
| <span data-ttu-id="26c33-194">Tungumál</span><span class="sxs-lookup"><span data-stu-id="26c33-194">Language</span></span> | <span data-ttu-id="26c33-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="26c33-195">cdm_language</span></span> |
| <span data-ttu-id="26c33-196">Titill</span><span class="sxs-lookup"><span data-stu-id="26c33-196">Title</span></span> | <span data-ttu-id="26c33-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="26c33-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="26c33-198">Fjárhagslegar víddir fyrir **Gerð stöðu**, **Stöðuúthlutun starfskrafts** og **Starf** veita einnar áttar samþættingu við Dataverse.</span><span class="sxs-lookup"><span data-stu-id="26c33-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="26c33-199">Uppfærslur fjárhagsvídda samstillast ekki eins og stendur úr Dataverse í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="26c33-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="26c33-200">Leyfis- og fjarvistatöflur</span><span class="sxs-lookup"><span data-stu-id="26c33-200">Leave and absence tables</span></span>

| <span data-ttu-id="26c33-201">Nafn</span><span class="sxs-lookup"><span data-stu-id="26c33-201">Name</span></span> | <span data-ttu-id="26c33-202">Tafla</span><span class="sxs-lookup"><span data-stu-id="26c33-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="26c33-203">Orlofsbankafærsla</span><span class="sxs-lookup"><span data-stu-id="26c33-203">Leave Bank Transaction</span></span> | <span data-ttu-id="26c33-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="26c33-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="26c33-205">Orlofsskráning</span><span class="sxs-lookup"><span data-stu-id="26c33-205">Leave Enrollment</span></span> | <span data-ttu-id="26c33-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="26c33-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="26c33-207">Leyfisáætlun</span><span class="sxs-lookup"><span data-stu-id="26c33-207">Leave Plan</span></span> | <span data-ttu-id="26c33-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="26c33-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="26c33-209">Orlofsbeiðni</span><span class="sxs-lookup"><span data-stu-id="26c33-209">Leave Request</span></span> | <span data-ttu-id="26c33-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="26c33-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="26c33-211">Upplýsingar um orlofsbeiðni</span><span class="sxs-lookup"><span data-stu-id="26c33-211">Leave Request Detail</span></span> | <span data-ttu-id="26c33-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="26c33-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="26c33-213">Gerð leyfis</span><span class="sxs-lookup"><span data-stu-id="26c33-213">Leave Type</span></span> | <span data-ttu-id="26c33-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="26c33-214">cdm_leavetype</span></span> |
| <span data-ttu-id="26c33-215">Ástæðukóði orlofsgerðar</span><span class="sxs-lookup"><span data-stu-id="26c33-215">Leave Type Reason Code</span></span> | <span data-ttu-id="26c33-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="26c33-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="26c33-217">Töflur launaskráar</span><span class="sxs-lookup"><span data-stu-id="26c33-217">Payroll tables</span></span>

| <span data-ttu-id="26c33-218">Nafn</span><span class="sxs-lookup"><span data-stu-id="26c33-218">Name</span></span> | <span data-ttu-id="26c33-219">Tafla</span><span class="sxs-lookup"><span data-stu-id="26c33-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="26c33-220">Greiðsluferli</span><span class="sxs-lookup"><span data-stu-id="26c33-220">Pay Cycle</span></span> | <span data-ttu-id="26c33-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="26c33-221">cdm_paycycle</span></span> |
| <span data-ttu-id="26c33-222">Launatímabil</span><span class="sxs-lookup"><span data-stu-id="26c33-222">Pay Period</span></span> | <span data-ttu-id="26c33-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="26c33-223">cdm_payperiod</span></span> |
| <span data-ttu-id="26c33-224">Tekjukóði launa</span><span class="sxs-lookup"><span data-stu-id="26c33-224">Payroll Earning Code</span></span> | <span data-ttu-id="26c33-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="26c33-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="26c33-226">Bankareikningsgreiðslur</span><span class="sxs-lookup"><span data-stu-id="26c33-226">Bank Account Disbursement</span></span> | <span data-ttu-id="26c33-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="26c33-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="26c33-228">Skattumdæmi</span><span class="sxs-lookup"><span data-stu-id="26c33-228">Tax Region</span></span> | <span data-ttu-id="26c33-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="26c33-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="26c33-230">Starfsmannatöflur</span><span class="sxs-lookup"><span data-stu-id="26c33-230">Worker tables</span></span>

| <span data-ttu-id="26c33-231">Nafn</span><span class="sxs-lookup"><span data-stu-id="26c33-231">Name</span></span> | <span data-ttu-id="26c33-232">Tafla</span><span class="sxs-lookup"><span data-stu-id="26c33-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="26c33-233">Starfsmaður</span><span class="sxs-lookup"><span data-stu-id="26c33-233">Worker</span></span> | <span data-ttu-id="26c33-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="26c33-234">cdm_worker</span></span> |
| <span data-ttu-id="26c33-235">Aðsetur starfskrafts</span><span class="sxs-lookup"><span data-stu-id="26c33-235">Worker Address</span></span> | <span data-ttu-id="26c33-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="26c33-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="26c33-237">Persónuupplýsingar starfskrafts</span><span class="sxs-lookup"><span data-stu-id="26c33-237">Worker Personal Detail</span></span> | <span data-ttu-id="26c33-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="26c33-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="26c33-239">Kennitala starfskrafts</span><span class="sxs-lookup"><span data-stu-id="26c33-239">Worker Person Identification Number</span></span> | <span data-ttu-id="26c33-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="26c33-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="26c33-241">Persónukennisgerð starfskrafts</span><span class="sxs-lookup"><span data-stu-id="26c33-241">Worker Person Identification Type</span></span> | <span data-ttu-id="26c33-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="26c33-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="26c33-243">Vinnudagatal</span><span class="sxs-lookup"><span data-stu-id="26c33-243">Work Calendar</span></span> | <span data-ttu-id="26c33-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="26c33-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="26c33-245">Dagur í vinnudagatali</span><span class="sxs-lookup"><span data-stu-id="26c33-245">Work Calendar Day</span></span> | <span data-ttu-id="26c33-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="26c33-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="26c33-247">Frídagur í vinnudagatali</span><span class="sxs-lookup"><span data-stu-id="26c33-247">Work Calendar Holiday</span></span> |<span data-ttu-id="26c33-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="26c33-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="26c33-249">Frídagslína í vinnudagatali</span><span class="sxs-lookup"><span data-stu-id="26c33-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="26c33-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="26c33-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="26c33-251">Tímabil vinnudagatals</span><span class="sxs-lookup"><span data-stu-id="26c33-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="26c33-252">cdm_workcalendartimeinterval (Ekki virkjað fyrir sérsniðinn reitastuðning)</span><span class="sxs-lookup"><span data-stu-id="26c33-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="26c33-253">Bankareikningur starfskrafts</span><span class="sxs-lookup"><span data-stu-id="26c33-253">Worker Bank Account</span></span> | <span data-ttu-id="26c33-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="26c33-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="26c33-255">Uppsetningartöflur starfsmanns</span><span class="sxs-lookup"><span data-stu-id="26c33-255">Worker setup tables</span></span>

| <span data-ttu-id="26c33-256">Nafn</span><span class="sxs-lookup"><span data-stu-id="26c33-256">Name</span></span> | <span data-ttu-id="26c33-257">Tafla</span><span class="sxs-lookup"><span data-stu-id="26c33-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="26c33-258">Uppgjafahermaður</span><span class="sxs-lookup"><span data-stu-id="26c33-258">Veteran Status</span></span> | <span data-ttu-id="26c33-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="26c33-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="26c33-260">Þjóðernisuppruni</span><span class="sxs-lookup"><span data-stu-id="26c33-260">Ethnic Origin</span></span> | <span data-ttu-id="26c33-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="26c33-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="26c33-262">Ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="26c33-262">Reason Code</span></span> | <span data-ttu-id="26c33-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="26c33-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="26c33-264">Útgáfustofnun persónuskilríkja</span><span class="sxs-lookup"><span data-stu-id="26c33-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="26c33-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="26c33-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="26c33-266">Hæfnistöflur</span><span class="sxs-lookup"><span data-stu-id="26c33-266">Competency tables</span></span>

| <span data-ttu-id="26c33-267">Nafn</span><span class="sxs-lookup"><span data-stu-id="26c33-267">Name</span></span> | <span data-ttu-id="26c33-268">Tafla</span><span class="sxs-lookup"><span data-stu-id="26c33-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="26c33-269">Gerð hæfni</span><span class="sxs-lookup"><span data-stu-id="26c33-269">Skill Type</span></span> | <span data-ttu-id="26c33-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="26c33-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="26c33-271">Líkön töfluvensla</span><span class="sxs-lookup"><span data-stu-id="26c33-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="26c33-272">Starfsmaður</span><span class="sxs-lookup"><span data-stu-id="26c33-272">Worker</span></span>

![Starfsmaður](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="26c33-274">Starf og starfstaða</span><span class="sxs-lookup"><span data-stu-id="26c33-274">Job and Job Position</span></span>

![Starf og starfstaða](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="26c33-276">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="26c33-276">Benefits</span></span>

![Fríðindi](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="26c33-278">Laun</span><span class="sxs-lookup"><span data-stu-id="26c33-278">Compensation</span></span>

![Laun](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="26c33-280">Hætta</span><span class="sxs-lookup"><span data-stu-id="26c33-280">Leave</span></span>

![Hætta](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="26c33-282">Vinnudagatal</span><span class="sxs-lookup"><span data-stu-id="26c33-282">Work Calendar</span></span>

![Vinnudagatal](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="26c33-284">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="26c33-284">See also</span></span>

[<span data-ttu-id="26c33-285">Velja tækni við samþættingu gagna</span><span class="sxs-lookup"><span data-stu-id="26c33-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="26c33-286">Skilgreina Dataverse-samþættingu</span><span class="sxs-lookup"><span data-stu-id="26c33-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="26c33-287">Skilgreina Dataverse-sýndartöflur</span><span class="sxs-lookup"><span data-stu-id="26c33-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="26c33-288">Algengar spurningar um sýndartöflur Human Resources</span><span class="sxs-lookup"><span data-stu-id="26c33-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="26c33-289">Hvað er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="26c33-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="26c33-290">Hugtakauppfærslur</span><span class="sxs-lookup"><span data-stu-id="26c33-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]