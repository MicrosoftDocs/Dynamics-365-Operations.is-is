---
title: Dataverse töflur
description: Microsoft Dynamics 365 Human Resources notar Dataverse til að gera mögulegt atburðarás fyrir stækkun og samþættingu.
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: e316cda9b9c5361c0a2837e7ed6c050e76cc39b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793610"
---
# <a name="dataverse-tables"></a><span data-ttu-id="eab46-103">Dataverse töflur</span><span class="sxs-lookup"><span data-stu-id="eab46-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="eab46-104">Microsoft Dynamics 365 Human Resources notar Dataverse til að gera mögulegt atburðarás fyrir stækkun og samþættingu.</span><span class="sxs-lookup"><span data-stu-id="eab46-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="eab46-105">Mannauðseiningar samsvara Dataverse töflum.</span><span class="sxs-lookup"><span data-stu-id="eab46-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="eab46-106">Frekari upplýsingar um Dataverse (áður Common Data Service) og uppfærslur á hugtökum er að finna í [Hvað er Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="eab46-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="eab46-107">Eftirfarandi Dataverse-töflur eru í boði sem byggja á einingum Human Resources.</span><span class="sxs-lookup"><span data-stu-id="eab46-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="eab46-108">Fríðindatöflur</span><span class="sxs-lookup"><span data-stu-id="eab46-108">Benefit tables</span></span>

| <span data-ttu-id="eab46-109">Nafn</span><span class="sxs-lookup"><span data-stu-id="eab46-109">Name</span></span> | <span data-ttu-id="eab46-110">Tafla</span><span class="sxs-lookup"><span data-stu-id="eab46-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="eab46-111">Útreikningstíðni fríðinda</span><span class="sxs-lookup"><span data-stu-id="eab46-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="eab46-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="eab46-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="eab46-113">Útreikningsíðni fríðinda á launatímabili</span><span class="sxs-lookup"><span data-stu-id="eab46-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="eab46-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="eab46-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="eab46-115">Hlutfall útreikninga fyrir fríðindi</span><span class="sxs-lookup"><span data-stu-id="eab46-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="eab46-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="eab46-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="eab46-117">Upplýsingar um hlutfall útreikninga fyrir fríðindi</span><span class="sxs-lookup"><span data-stu-id="eab46-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="eab46-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="eab46-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="eab46-119">Fríðindavalkostur</span><span class="sxs-lookup"><span data-stu-id="eab46-119">Benefit Option</span></span> | <span data-ttu-id="eab46-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="eab46-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="eab46-121">Fríðindaáætlun</span><span class="sxs-lookup"><span data-stu-id="eab46-121">Benefit Plan</span></span> | <span data-ttu-id="eab46-122">cdm_benefitplan (Ekki virkjað fyrir sérsniðinn reitastuðning)</span><span class="sxs-lookup"><span data-stu-id="eab46-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="eab46-123">Gerð fríðinda</span><span class="sxs-lookup"><span data-stu-id="eab46-123">Benefit Type</span></span> | <span data-ttu-id="eab46-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="eab46-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="eab46-125">Verkefnatöflur viðskiptaferlis</span><span class="sxs-lookup"><span data-stu-id="eab46-125">Business process tasks tables</span></span>

| <span data-ttu-id="eab46-126">Nafn</span><span class="sxs-lookup"><span data-stu-id="eab46-126">Name</span></span> | <span data-ttu-id="eab46-127">Tafla</span><span class="sxs-lookup"><span data-stu-id="eab46-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="eab46-128">Dagatal viðskiptaferlis</span><span class="sxs-lookup"><span data-stu-id="eab46-128">Business Process Calendar</span></span> | <span data-ttu-id="eab46-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="eab46-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="eab46-130">Hópverkefni viðskiptaferlis</span><span class="sxs-lookup"><span data-stu-id="eab46-130">Business Process Group Assignment</span></span> | <span data-ttu-id="eab46-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="eab46-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="eab46-132">Verkhópur viðskiptaferlissafns</span><span class="sxs-lookup"><span data-stu-id="eab46-132">Business Process Library Task Group</span></span> | <span data-ttu-id="eab46-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="eab46-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="eab46-134">Stig viðskiptaferlis</span><span class="sxs-lookup"><span data-stu-id="eab46-134">Business Process Stage</span></span> | <span data-ttu-id="eab46-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="eab46-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="eab46-136">Haus gátlistasniðmáts</span><span class="sxs-lookup"><span data-stu-id="eab46-136">Checklist Template Header</span></span> | <span data-ttu-id="eab46-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="eab46-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="eab46-138">Verkefni gátlistasniðmáts</span><span class="sxs-lookup"><span data-stu-id="eab46-138">Checklist Template Task</span></span> | <span data-ttu-id="eab46-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="eab46-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="eab46-140">Launatöflur</span><span class="sxs-lookup"><span data-stu-id="eab46-140">Compensation tables</span></span>

| <span data-ttu-id="eab46-141">Nafn</span><span class="sxs-lookup"><span data-stu-id="eab46-141">Name</span></span> | <span data-ttu-id="eab46-142">Tafla</span><span class="sxs-lookup"><span data-stu-id="eab46-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="eab46-143">Fyrirkomulag fastra launa</span><span class="sxs-lookup"><span data-stu-id="eab46-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="eab46-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="eab46-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="eab46-145">Launanet</span><span class="sxs-lookup"><span data-stu-id="eab46-145">Compensation Grid</span></span> | <span data-ttu-id="eab46-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="eab46-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="eab46-147">Launastig</span><span class="sxs-lookup"><span data-stu-id="eab46-147">Compensation Level</span></span> | <span data-ttu-id="eab46-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="eab46-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="eab46-149">Greiðslutíðni launa</span><span class="sxs-lookup"><span data-stu-id="eab46-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="eab46-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="eab46-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="eab46-151">Uppsetning á tilvísunarpunkti launa</span><span class="sxs-lookup"><span data-stu-id="eab46-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="eab46-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="eab46-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="eab46-153">Setja upp línu tilvísunarpunkts launa</span><span class="sxs-lookup"><span data-stu-id="eab46-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="eab46-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="eab46-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="eab46-155">Launasvæði</span><span class="sxs-lookup"><span data-stu-id="eab46-155">Compensation Region</span></span> | <span data-ttu-id="eab46-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="eab46-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="eab46-157">Launaskipulag</span><span class="sxs-lookup"><span data-stu-id="eab46-157">Compensation Structure</span></span> | <span data-ttu-id="eab46-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="eab46-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="eab46-159">Fyrirkomulag breytilegra uppbóta</span><span class="sxs-lookup"><span data-stu-id="eab46-159">Compensation Variable Plan</span></span> | <span data-ttu-id="eab46-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="eab46-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="eab46-161">Fyrirkomulagsstig breytilegra uppbóta</span><span class="sxs-lookup"><span data-stu-id="eab46-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="eab46-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="eab46-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="eab46-163">Fyrirkomulagsgerð breytilegra uppbóta</span><span class="sxs-lookup"><span data-stu-id="eab46-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="eab46-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="eab46-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="eab46-165">Fast launatilvik</span><span class="sxs-lookup"><span data-stu-id="eab46-165">Fixed Compensation Event</span></span> | <span data-ttu-id="eab46-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="eab46-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="eab46-167">Veitiregla</span><span class="sxs-lookup"><span data-stu-id="eab46-167">Vesting Rule</span></span> | <span data-ttu-id="eab46-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="eab46-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="eab46-169">Föst laun starfskrafts</span><span class="sxs-lookup"><span data-stu-id="eab46-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="eab46-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="eab46-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="eab46-171">Fyrirtækistöflur</span><span class="sxs-lookup"><span data-stu-id="eab46-171">Organization tables</span></span>

| <span data-ttu-id="eab46-172">Nafn</span><span class="sxs-lookup"><span data-stu-id="eab46-172">Name</span></span> | <span data-ttu-id="eab46-173">Tafla</span><span class="sxs-lookup"><span data-stu-id="eab46-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="eab46-174">Deild</span><span class="sxs-lookup"><span data-stu-id="eab46-174">Department</span></span> | <span data-ttu-id="eab46-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="eab46-175">cdm_department</span></span> |
| <span data-ttu-id="eab46-176">Ráðning</span><span class="sxs-lookup"><span data-stu-id="eab46-176">Employment</span></span> | <span data-ttu-id="eab46-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="eab46-177">cdm_employment</span></span> |
| <span data-ttu-id="eab46-178">Fyrirt.  </span><span class="sxs-lookup"><span data-stu-id="eab46-178">Company</span></span> | <span data-ttu-id="eab46-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="eab46-179">cdm_company</span></span> |
| <span data-ttu-id="eab46-180">Vinnsla</span><span class="sxs-lookup"><span data-stu-id="eab46-180">Job</span></span> | <span data-ttu-id="eab46-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="eab46-181">cdm_job</span></span> |
| <span data-ttu-id="eab46-182">Starfshlutverk</span><span class="sxs-lookup"><span data-stu-id="eab46-182">Job Function</span></span> | <span data-ttu-id="eab46-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="eab46-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="eab46-184">Staða starfs</span><span class="sxs-lookup"><span data-stu-id="eab46-184">Job Position</span></span> | <span data-ttu-id="eab46-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="eab46-185">cdm_jobposition</span></span> |
| <span data-ttu-id="eab46-186">Gerð stöðu</span><span class="sxs-lookup"><span data-stu-id="eab46-186">Position Type</span></span> | <span data-ttu-id="eab46-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="eab46-187">cdm_positiontype</span></span> |
| <span data-ttu-id="eab46-188">Stöðuúthlutun starfskrafts</span><span class="sxs-lookup"><span data-stu-id="eab46-188">Position Worker Assignment</span></span> | <span data-ttu-id="eab46-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="eab46-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="eab46-190">Vídd stöðu starfs</span><span class="sxs-lookup"><span data-stu-id="eab46-190">Job Position Dimension</span></span> | <span data-ttu-id="eab46-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="eab46-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="eab46-192">Starfsgerð</span><span class="sxs-lookup"><span data-stu-id="eab46-192">Job Type</span></span> | <span data-ttu-id="eab46-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="eab46-193">cdm_jobtype</span></span> |
| <span data-ttu-id="eab46-194">Tungumál</span><span class="sxs-lookup"><span data-stu-id="eab46-194">Language</span></span> | <span data-ttu-id="eab46-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="eab46-195">cdm_language</span></span> |
| <span data-ttu-id="eab46-196">Titill</span><span class="sxs-lookup"><span data-stu-id="eab46-196">Title</span></span> | <span data-ttu-id="eab46-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="eab46-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="eab46-198">Fjárhagslegar víddir fyrir **Gerð stöðu**, **Stöðuúthlutun starfskrafts** og **Starf** veita einnar áttar samþættingu við Dataverse.</span><span class="sxs-lookup"><span data-stu-id="eab46-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="eab46-199">Uppfærslur fjárhagsvídda samstillast ekki eins og stendur úr Dataverse í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="eab46-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="eab46-200">Leyfis- og fjarvistatöflur</span><span class="sxs-lookup"><span data-stu-id="eab46-200">Leave and absence tables</span></span>

| <span data-ttu-id="eab46-201">Nafn</span><span class="sxs-lookup"><span data-stu-id="eab46-201">Name</span></span> | <span data-ttu-id="eab46-202">Tafla</span><span class="sxs-lookup"><span data-stu-id="eab46-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="eab46-203">Orlofsbankafærsla</span><span class="sxs-lookup"><span data-stu-id="eab46-203">Leave Bank Transaction</span></span> | <span data-ttu-id="eab46-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="eab46-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="eab46-205">Orlofsskráning</span><span class="sxs-lookup"><span data-stu-id="eab46-205">Leave Enrollment</span></span> | <span data-ttu-id="eab46-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="eab46-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="eab46-207">Leyfisáætlun</span><span class="sxs-lookup"><span data-stu-id="eab46-207">Leave Plan</span></span> | <span data-ttu-id="eab46-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="eab46-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="eab46-209">Orlofsbeiðni</span><span class="sxs-lookup"><span data-stu-id="eab46-209">Leave Request</span></span> | <span data-ttu-id="eab46-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="eab46-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="eab46-211">Upplýsingar um orlofsbeiðni</span><span class="sxs-lookup"><span data-stu-id="eab46-211">Leave Request Detail</span></span> | <span data-ttu-id="eab46-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="eab46-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="eab46-213">Gerð leyfis</span><span class="sxs-lookup"><span data-stu-id="eab46-213">Leave Type</span></span> | <span data-ttu-id="eab46-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="eab46-214">cdm_leavetype</span></span> |
| <span data-ttu-id="eab46-215">Ástæðukóði orlofsgerðar</span><span class="sxs-lookup"><span data-stu-id="eab46-215">Leave Type Reason Code</span></span> | <span data-ttu-id="eab46-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="eab46-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="eab46-217">Töflur launaskráar</span><span class="sxs-lookup"><span data-stu-id="eab46-217">Payroll tables</span></span>

| <span data-ttu-id="eab46-218">Nafn</span><span class="sxs-lookup"><span data-stu-id="eab46-218">Name</span></span> | <span data-ttu-id="eab46-219">Tafla</span><span class="sxs-lookup"><span data-stu-id="eab46-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="eab46-220">Greiðsluferli</span><span class="sxs-lookup"><span data-stu-id="eab46-220">Pay Cycle</span></span> | <span data-ttu-id="eab46-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="eab46-221">cdm_paycycle</span></span> |
| <span data-ttu-id="eab46-222">Launatímabil</span><span class="sxs-lookup"><span data-stu-id="eab46-222">Pay Period</span></span> | <span data-ttu-id="eab46-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="eab46-223">cdm_payperiod</span></span> |
| <span data-ttu-id="eab46-224">Tekjukóði launa</span><span class="sxs-lookup"><span data-stu-id="eab46-224">Payroll Earning Code</span></span> | <span data-ttu-id="eab46-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="eab46-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="eab46-226">Bankareikningsgreiðslur</span><span class="sxs-lookup"><span data-stu-id="eab46-226">Bank Account Disbursement</span></span> | <span data-ttu-id="eab46-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="eab46-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="eab46-228">Skattumdæmi</span><span class="sxs-lookup"><span data-stu-id="eab46-228">Tax Region</span></span> | <span data-ttu-id="eab46-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="eab46-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="eab46-230">Starfsmannatöflur</span><span class="sxs-lookup"><span data-stu-id="eab46-230">Worker tables</span></span>

| <span data-ttu-id="eab46-231">Nafn</span><span class="sxs-lookup"><span data-stu-id="eab46-231">Name</span></span> | <span data-ttu-id="eab46-232">Tafla</span><span class="sxs-lookup"><span data-stu-id="eab46-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="eab46-233">Starfsmaður</span><span class="sxs-lookup"><span data-stu-id="eab46-233">Worker</span></span> | <span data-ttu-id="eab46-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="eab46-234">cdm_worker</span></span> |
| <span data-ttu-id="eab46-235">Aðsetur starfskrafts</span><span class="sxs-lookup"><span data-stu-id="eab46-235">Worker Address</span></span> | <span data-ttu-id="eab46-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="eab46-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="eab46-237">Persónuupplýsingar starfskrafts</span><span class="sxs-lookup"><span data-stu-id="eab46-237">Worker Personal Detail</span></span> | <span data-ttu-id="eab46-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="eab46-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="eab46-239">Kennitala starfskrafts</span><span class="sxs-lookup"><span data-stu-id="eab46-239">Worker Person Identification Number</span></span> | <span data-ttu-id="eab46-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="eab46-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="eab46-241">Persónukennisgerð starfskrafts</span><span class="sxs-lookup"><span data-stu-id="eab46-241">Worker Person Identification Type</span></span> | <span data-ttu-id="eab46-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="eab46-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="eab46-243">Vinnudagatal</span><span class="sxs-lookup"><span data-stu-id="eab46-243">Work Calendar</span></span> | <span data-ttu-id="eab46-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="eab46-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="eab46-245">Dagur í vinnudagatali</span><span class="sxs-lookup"><span data-stu-id="eab46-245">Work Calendar Day</span></span> | <span data-ttu-id="eab46-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="eab46-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="eab46-247">Frídagur í vinnudagatali</span><span class="sxs-lookup"><span data-stu-id="eab46-247">Work Calendar Holiday</span></span> |<span data-ttu-id="eab46-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="eab46-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="eab46-249">Frídagslína í vinnudagatali</span><span class="sxs-lookup"><span data-stu-id="eab46-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="eab46-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="eab46-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="eab46-251">Tímabil vinnudagatals</span><span class="sxs-lookup"><span data-stu-id="eab46-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="eab46-252">cdm_workcalendartimeinterval (Ekki virkjað fyrir sérsniðinn reitastuðning)</span><span class="sxs-lookup"><span data-stu-id="eab46-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="eab46-253">Bankareikningur starfskrafts</span><span class="sxs-lookup"><span data-stu-id="eab46-253">Worker Bank Account</span></span> | <span data-ttu-id="eab46-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="eab46-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="eab46-255">Uppsetningartöflur starfsmanns</span><span class="sxs-lookup"><span data-stu-id="eab46-255">Worker setup tables</span></span>

| <span data-ttu-id="eab46-256">Nafn</span><span class="sxs-lookup"><span data-stu-id="eab46-256">Name</span></span> | <span data-ttu-id="eab46-257">Tafla</span><span class="sxs-lookup"><span data-stu-id="eab46-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="eab46-258">Uppgjafahermaður</span><span class="sxs-lookup"><span data-stu-id="eab46-258">Veteran Status</span></span> | <span data-ttu-id="eab46-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="eab46-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="eab46-260">Þjóðernisuppruni</span><span class="sxs-lookup"><span data-stu-id="eab46-260">Ethnic Origin</span></span> | <span data-ttu-id="eab46-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="eab46-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="eab46-262">Ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="eab46-262">Reason Code</span></span> | <span data-ttu-id="eab46-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="eab46-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="eab46-264">Útgáfustofnun persónuskilríkja</span><span class="sxs-lookup"><span data-stu-id="eab46-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="eab46-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="eab46-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="eab46-266">Hæfnistöflur</span><span class="sxs-lookup"><span data-stu-id="eab46-266">Competency tables</span></span>

| <span data-ttu-id="eab46-267">Nafn</span><span class="sxs-lookup"><span data-stu-id="eab46-267">Name</span></span> | <span data-ttu-id="eab46-268">Tafla</span><span class="sxs-lookup"><span data-stu-id="eab46-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="eab46-269">Gerð hæfni</span><span class="sxs-lookup"><span data-stu-id="eab46-269">Skill Type</span></span> | <span data-ttu-id="eab46-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="eab46-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="eab46-271">Líkön töfluvensla</span><span class="sxs-lookup"><span data-stu-id="eab46-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="eab46-272">Starfsmaður</span><span class="sxs-lookup"><span data-stu-id="eab46-272">Worker</span></span>

![Starfsmaður](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="eab46-274">Starf og starfstaða</span><span class="sxs-lookup"><span data-stu-id="eab46-274">Job and Job Position</span></span>

![Starf og starfstaða](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="eab46-276">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="eab46-276">Benefits</span></span>

![Fríðindi](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="eab46-278">Laun</span><span class="sxs-lookup"><span data-stu-id="eab46-278">Compensation</span></span>

![Laun](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="eab46-280">Hætta</span><span class="sxs-lookup"><span data-stu-id="eab46-280">Leave</span></span>

![Hætta](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="eab46-282">Vinnudagatal</span><span class="sxs-lookup"><span data-stu-id="eab46-282">Work Calendar</span></span>

![Vinnudagatal](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="eab46-284">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="eab46-284">See also</span></span>

[<span data-ttu-id="eab46-285">Velja tækni við samþættingu gagna</span><span class="sxs-lookup"><span data-stu-id="eab46-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="eab46-286">Skilgreina Dataverse-samþættingu</span><span class="sxs-lookup"><span data-stu-id="eab46-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="eab46-287">Skilgreina Dataverse-sýndartöflur</span><span class="sxs-lookup"><span data-stu-id="eab46-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="eab46-288">Algengar spurningar um sýndartöflur Human Resources</span><span class="sxs-lookup"><span data-stu-id="eab46-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="eab46-289">Hvað er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="eab46-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="eab46-290">Hugtakauppfærslur</span><span class="sxs-lookup"><span data-stu-id="eab46-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]