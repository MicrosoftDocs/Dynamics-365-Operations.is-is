---
title: Common Data Service einingar
description: Microsoft Dynamics 365 Human Resources notar Common Data Service til að gera mögulegt atburðarás fyrir stækkun og samþættingu.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: c8e0288da16829c04a9b97c0a52caa8bd27cddf8
ms.sourcegitcommit: fde8045ea49d0cf26d5e7ac5a0da5c0d3d69d5bc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/26/2020
ms.locfileid: "3166499"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="4d673-103">Common Data Service einingar</span><span class="sxs-lookup"><span data-stu-id="4d673-103">Common Data Service entities</span></span>

<span data-ttu-id="4d673-104">Microsoft Dynamics 365 Human Resources notar Common Data Service til að gera mögulegt atburðarás fyrir stækkun og samþættingu.</span><span class="sxs-lookup"><span data-stu-id="4d673-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="4d673-105">Nánari upplýsingar um Common Data Service er að finna í [Hvað er Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span><span class="sxs-lookup"><span data-stu-id="4d673-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="4d673-106">Eftirfarandi einingar Human Resources eru í boði í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4d673-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="4d673-107">Fríðindaeiningar</span><span class="sxs-lookup"><span data-stu-id="4d673-107">Benefit entities</span></span>

| <span data-ttu-id="4d673-108">Nafn</span><span class="sxs-lookup"><span data-stu-id="4d673-108">Name</span></span> | <span data-ttu-id="4d673-109">Eining</span><span class="sxs-lookup"><span data-stu-id="4d673-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4d673-110">Útreikningstíðni fríðinda</span><span class="sxs-lookup"><span data-stu-id="4d673-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="4d673-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="4d673-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="4d673-112">Útreikningsíðni fríðinda á launatímabili</span><span class="sxs-lookup"><span data-stu-id="4d673-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="4d673-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="4d673-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="4d673-114">Hlutfall útreikninga fyrir fríðindi</span><span class="sxs-lookup"><span data-stu-id="4d673-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="4d673-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="4d673-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="4d673-116">Upplýsingar um hlutfall útreikninga fyrir fríðindi</span><span class="sxs-lookup"><span data-stu-id="4d673-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="4d673-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="4d673-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="4d673-118">Fríðindavalkostur</span><span class="sxs-lookup"><span data-stu-id="4d673-118">Benefit Option</span></span> | <span data-ttu-id="4d673-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="4d673-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="4d673-120">Fríðindaáætlun</span><span class="sxs-lookup"><span data-stu-id="4d673-120">Benefit Plan</span></span> | <span data-ttu-id="4d673-121">cdm_benefitplan (Ekki virkjað fyrir sérsniðinn reitastuðning)</span><span class="sxs-lookup"><span data-stu-id="4d673-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="4d673-122">Gerð fríðinda</span><span class="sxs-lookup"><span data-stu-id="4d673-122">Benefit Type</span></span> | <span data-ttu-id="4d673-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="4d673-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="4d673-124">Einingar viðskiptaferlaverka</span><span class="sxs-lookup"><span data-stu-id="4d673-124">Business process tasks entities</span></span>

| <span data-ttu-id="4d673-125">Nafn</span><span class="sxs-lookup"><span data-stu-id="4d673-125">Name</span></span> | <span data-ttu-id="4d673-126">Eining</span><span class="sxs-lookup"><span data-stu-id="4d673-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4d673-127">Dagatal viðskiptaferlis</span><span class="sxs-lookup"><span data-stu-id="4d673-127">Business Process Calendar</span></span> | <span data-ttu-id="4d673-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="4d673-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="4d673-129">Hópverkefni viðskiptaferlis</span><span class="sxs-lookup"><span data-stu-id="4d673-129">Business Process Group Assignment</span></span> | <span data-ttu-id="4d673-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="4d673-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="4d673-131">Verkhópur viðskiptaferlissafns</span><span class="sxs-lookup"><span data-stu-id="4d673-131">Business Process Library Task Group</span></span> | <span data-ttu-id="4d673-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="4d673-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="4d673-133">Stig viðskiptaferlis</span><span class="sxs-lookup"><span data-stu-id="4d673-133">Business Process Stage</span></span> | <span data-ttu-id="4d673-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="4d673-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="4d673-135">Haus gátlistasniðmáts</span><span class="sxs-lookup"><span data-stu-id="4d673-135">Checklist Template Header</span></span> | <span data-ttu-id="4d673-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="4d673-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="4d673-137">Verkefni gátlistasniðmáts</span><span class="sxs-lookup"><span data-stu-id="4d673-137">Checklist Template Task</span></span> | <span data-ttu-id="4d673-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="4d673-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="4d673-139">Bótaeiningar</span><span class="sxs-lookup"><span data-stu-id="4d673-139">Compensation entities</span></span>

| <span data-ttu-id="4d673-140">Nafn</span><span class="sxs-lookup"><span data-stu-id="4d673-140">Name</span></span> | <span data-ttu-id="4d673-141">Eining</span><span class="sxs-lookup"><span data-stu-id="4d673-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4d673-142">Fyrirkomulag fastra launa</span><span class="sxs-lookup"><span data-stu-id="4d673-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="4d673-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="4d673-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="4d673-144">Launanet</span><span class="sxs-lookup"><span data-stu-id="4d673-144">Compensation Grid</span></span> | <span data-ttu-id="4d673-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="4d673-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="4d673-146">Launastig</span><span class="sxs-lookup"><span data-stu-id="4d673-146">Compensation Level</span></span> | <span data-ttu-id="4d673-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="4d673-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="4d673-148">Greiðslutíðni launa</span><span class="sxs-lookup"><span data-stu-id="4d673-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="4d673-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="4d673-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="4d673-150">Uppsetning á tilvísunarpunkti launa</span><span class="sxs-lookup"><span data-stu-id="4d673-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="4d673-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="4d673-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="4d673-152">Setja upp línu tilvísunarpunkts launa</span><span class="sxs-lookup"><span data-stu-id="4d673-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="4d673-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="4d673-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="4d673-154">Launasvæði</span><span class="sxs-lookup"><span data-stu-id="4d673-154">Compensation Region</span></span> | <span data-ttu-id="4d673-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="4d673-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="4d673-156">Launaskipulag</span><span class="sxs-lookup"><span data-stu-id="4d673-156">Compensation Structure</span></span> | <span data-ttu-id="4d673-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="4d673-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="4d673-158">Fyrirkomulag breytilegra uppbóta</span><span class="sxs-lookup"><span data-stu-id="4d673-158">Compensation Variable Plan</span></span> | <span data-ttu-id="4d673-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="4d673-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="4d673-160">Fyrirkomulagsstig breytilegra uppbóta</span><span class="sxs-lookup"><span data-stu-id="4d673-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="4d673-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="4d673-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="4d673-162">Fyrirkomulagsgerð breytilegra uppbóta</span><span class="sxs-lookup"><span data-stu-id="4d673-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="4d673-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="4d673-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="4d673-164">Fast launatilvik</span><span class="sxs-lookup"><span data-stu-id="4d673-164">Fixed Compensation Event</span></span> | <span data-ttu-id="4d673-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="4d673-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="4d673-166">Veitiregla</span><span class="sxs-lookup"><span data-stu-id="4d673-166">Vesting Rule</span></span> | <span data-ttu-id="4d673-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="4d673-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="4d673-168">Föst laun starfskrafts</span><span class="sxs-lookup"><span data-stu-id="4d673-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="4d673-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="4d673-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="4d673-170">Fyrirtækjaeiningar</span><span class="sxs-lookup"><span data-stu-id="4d673-170">Organization entities</span></span>

| <span data-ttu-id="4d673-171">Nafn</span><span class="sxs-lookup"><span data-stu-id="4d673-171">Name</span></span> | <span data-ttu-id="4d673-172">Eining</span><span class="sxs-lookup"><span data-stu-id="4d673-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4d673-173">Deild</span><span class="sxs-lookup"><span data-stu-id="4d673-173">Department</span></span> | <span data-ttu-id="4d673-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="4d673-174">cdm_department</span></span> |
| <span data-ttu-id="4d673-175">Ráðning</span><span class="sxs-lookup"><span data-stu-id="4d673-175">Employment</span></span> | <span data-ttu-id="4d673-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="4d673-176">cdm_employment</span></span> |
| <span data-ttu-id="4d673-177">Fyrirt.</span><span class="sxs-lookup"><span data-stu-id="4d673-177">Company</span></span> | <span data-ttu-id="4d673-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="4d673-178">cdm_company</span></span> |
| <span data-ttu-id="4d673-179">Vinnsla</span><span class="sxs-lookup"><span data-stu-id="4d673-179">Job</span></span> | <span data-ttu-id="4d673-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="4d673-180">cdm_job</span></span> |
| <span data-ttu-id="4d673-181">Starfshlutverk</span><span class="sxs-lookup"><span data-stu-id="4d673-181">Job Function</span></span> | <span data-ttu-id="4d673-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="4d673-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="4d673-183">Staða starfs</span><span class="sxs-lookup"><span data-stu-id="4d673-183">Job Position</span></span> | <span data-ttu-id="4d673-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="4d673-184">cdm_jobposition</span></span> |
| <span data-ttu-id="4d673-185">Gerð stöðu</span><span class="sxs-lookup"><span data-stu-id="4d673-185">Position Type</span></span> | <span data-ttu-id="4d673-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="4d673-186">cdm_positiontype</span></span> |
| <span data-ttu-id="4d673-187">Stöðuúthlutun starfskrafts</span><span class="sxs-lookup"><span data-stu-id="4d673-187">Position Worker Assignment</span></span> | <span data-ttu-id="4d673-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="4d673-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="4d673-189">Vídd stöðu starfs</span><span class="sxs-lookup"><span data-stu-id="4d673-189">Job Position Dimension</span></span> | <span data-ttu-id="4d673-190">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="4d673-190">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="4d673-191">Starfsgerð</span><span class="sxs-lookup"><span data-stu-id="4d673-191">Job Type</span></span> | <span data-ttu-id="4d673-192">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="4d673-192">cdm_jobtype</span></span> |
| <span data-ttu-id="4d673-193">Tungumál</span><span class="sxs-lookup"><span data-stu-id="4d673-193">Language</span></span> | <span data-ttu-id="4d673-194">cdm_language</span><span class="sxs-lookup"><span data-stu-id="4d673-194">cdm_language</span></span> |
| <span data-ttu-id="4d673-195">Titill</span><span class="sxs-lookup"><span data-stu-id="4d673-195">Title</span></span> | <span data-ttu-id="4d673-196">cdm_title</span><span class="sxs-lookup"><span data-stu-id="4d673-196">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="4d673-197">Fjárhagslegar víddir fyrir **Gerð stöðu**, **Stöðuúthlutun starfskrafts** og **Starf** veita einnar áttar samþættingu við Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4d673-197">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Common Data Service.</span></span> <span data-ttu-id="4d673-198">Uppfærslur fjárhagsvídda samstillast ekki eins og stendur úr Common Data Service í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4d673-198">Financial dimensions updates currently can't synchronize from Common Data Service to Human Resources.</span></span> 

## <a name="leave-and-absence-entities"></a><span data-ttu-id="4d673-199">Einingar fyrir leyfi og fjarvistir</span><span class="sxs-lookup"><span data-stu-id="4d673-199">Leave and absence entities</span></span>

| <span data-ttu-id="4d673-200">Nafn</span><span class="sxs-lookup"><span data-stu-id="4d673-200">Name</span></span> | <span data-ttu-id="4d673-201">Eining</span><span class="sxs-lookup"><span data-stu-id="4d673-201">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4d673-202">Orlofsbankafærsla</span><span class="sxs-lookup"><span data-stu-id="4d673-202">Leave Bank Transaction</span></span> | <span data-ttu-id="4d673-203">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="4d673-203">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="4d673-204">Orlofsskráning</span><span class="sxs-lookup"><span data-stu-id="4d673-204">Leave Enrollment</span></span> | <span data-ttu-id="4d673-205">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="4d673-205">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="4d673-206">Leyfisáætlun</span><span class="sxs-lookup"><span data-stu-id="4d673-206">Leave Plan</span></span> | <span data-ttu-id="4d673-207">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="4d673-207">cdm_leaveplan</span></span> |
| <span data-ttu-id="4d673-208">Orlofsbeiðni</span><span class="sxs-lookup"><span data-stu-id="4d673-208">Leave Request</span></span> | <span data-ttu-id="4d673-209">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="4d673-209">cdm_leaverequest</span></span> |
| <span data-ttu-id="4d673-210">Upplýsingar um orlofsbeiðni</span><span class="sxs-lookup"><span data-stu-id="4d673-210">Leave Request Detail</span></span> | <span data-ttu-id="4d673-211">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="4d673-211">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="4d673-212">Gerð leyfis</span><span class="sxs-lookup"><span data-stu-id="4d673-212">Leave Type</span></span> | <span data-ttu-id="4d673-213">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="4d673-213">cdm_leavetype</span></span> |
| <span data-ttu-id="4d673-214">Ástæðukóði orlofsgerðar</span><span class="sxs-lookup"><span data-stu-id="4d673-214">Leave Type Reason Code</span></span> | <span data-ttu-id="4d673-215">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="4d673-215">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="4d673-216">Launaeiningar</span><span class="sxs-lookup"><span data-stu-id="4d673-216">Payroll entities</span></span>

| <span data-ttu-id="4d673-217">Nafn</span><span class="sxs-lookup"><span data-stu-id="4d673-217">Name</span></span> | <span data-ttu-id="4d673-218">Eining</span><span class="sxs-lookup"><span data-stu-id="4d673-218">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4d673-219">Greiðsluferli</span><span class="sxs-lookup"><span data-stu-id="4d673-219">Pay Cycle</span></span> | <span data-ttu-id="4d673-220">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="4d673-220">cdm_paycycle</span></span> |
| <span data-ttu-id="4d673-221">Launatímabil</span><span class="sxs-lookup"><span data-stu-id="4d673-221">Pay Period</span></span> | <span data-ttu-id="4d673-222">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="4d673-222">cdm_payperiod</span></span> |
| <span data-ttu-id="4d673-223">Tekjukóði launa</span><span class="sxs-lookup"><span data-stu-id="4d673-223">Payroll Earning Code</span></span> | <span data-ttu-id="4d673-224">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="4d673-224">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="4d673-225">Bankareikningsgreiðslur</span><span class="sxs-lookup"><span data-stu-id="4d673-225">Bank Account Disbursement</span></span> | <span data-ttu-id="4d673-226">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="4d673-226">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="4d673-227">Skattumdæmi</span><span class="sxs-lookup"><span data-stu-id="4d673-227">Tax Region</span></span> | <span data-ttu-id="4d673-228">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="4d673-228">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="4d673-229">Starfskraftaeiningar</span><span class="sxs-lookup"><span data-stu-id="4d673-229">Worker entities</span></span>

| <span data-ttu-id="4d673-230">Nafn</span><span class="sxs-lookup"><span data-stu-id="4d673-230">Name</span></span> | <span data-ttu-id="4d673-231">Eining</span><span class="sxs-lookup"><span data-stu-id="4d673-231">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4d673-232">Starfskraftur</span><span class="sxs-lookup"><span data-stu-id="4d673-232">Worker</span></span> | <span data-ttu-id="4d673-233">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="4d673-233">cdm_worker</span></span> |
| <span data-ttu-id="4d673-234">Aðsetur starfskrafts</span><span class="sxs-lookup"><span data-stu-id="4d673-234">Worker Address</span></span> | <span data-ttu-id="4d673-235">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="4d673-235">cdm_workeraddress</span></span> |
| <span data-ttu-id="4d673-236">Persónuupplýsingar starfskrafts</span><span class="sxs-lookup"><span data-stu-id="4d673-236">Worker Personal Detail</span></span> | <span data-ttu-id="4d673-237">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="4d673-237">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="4d673-238">Kennitala starfskrafts</span><span class="sxs-lookup"><span data-stu-id="4d673-238">Worker Person Identification Number</span></span> | <span data-ttu-id="4d673-239">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="4d673-239">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="4d673-240">Persónukennisgerð starfskrafts</span><span class="sxs-lookup"><span data-stu-id="4d673-240">Worker Person Identification Type</span></span> | <span data-ttu-id="4d673-241">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="4d673-241">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="4d673-242">Vinnudagatal</span><span class="sxs-lookup"><span data-stu-id="4d673-242">Work Calendar</span></span> | <span data-ttu-id="4d673-243">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="4d673-243">cdm_workcalendar</span></span> |
| <span data-ttu-id="4d673-244">Dagur í vinnudagatali</span><span class="sxs-lookup"><span data-stu-id="4d673-244">Work Calendar Day</span></span> | <span data-ttu-id="4d673-245">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="4d673-245">cdm_workcalendarday</span></span> |
| <span data-ttu-id="4d673-246">Frídagur í vinnudagatali</span><span class="sxs-lookup"><span data-stu-id="4d673-246">Work Calendar Holiday</span></span> |<span data-ttu-id="4d673-247">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="4d673-247">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="4d673-248">Frídagslína í vinnudagatali</span><span class="sxs-lookup"><span data-stu-id="4d673-248">Work Calendar Holiday Line</span></span> | <span data-ttu-id="4d673-249">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="4d673-249">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="4d673-250">Tímabil vinnudagatals</span><span class="sxs-lookup"><span data-stu-id="4d673-250">Work Calendar Time Interval</span></span> | <span data-ttu-id="4d673-251">cdm_workcalendartimeinterval (Ekki virkjað fyrir sérsniðinn reitastuðning)</span><span class="sxs-lookup"><span data-stu-id="4d673-251">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="4d673-252">Bankareikningur starfskrafts</span><span class="sxs-lookup"><span data-stu-id="4d673-252">Worker Bank Account</span></span> | <span data-ttu-id="4d673-253">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="4d673-253">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="4d673-254">Uppsetningareiningar starfskrafts</span><span class="sxs-lookup"><span data-stu-id="4d673-254">Worker setup entities</span></span>

| <span data-ttu-id="4d673-255">Nafn</span><span class="sxs-lookup"><span data-stu-id="4d673-255">Name</span></span> | <span data-ttu-id="4d673-256">Eining</span><span class="sxs-lookup"><span data-stu-id="4d673-256">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4d673-257">Uppgjafahermaður</span><span class="sxs-lookup"><span data-stu-id="4d673-257">Veteran Status</span></span> | <span data-ttu-id="4d673-258">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="4d673-258">cdm_veteranstatus</span></span> |
| <span data-ttu-id="4d673-259">Þjóðernisuppruni</span><span class="sxs-lookup"><span data-stu-id="4d673-259">Ethnic Origin</span></span> | <span data-ttu-id="4d673-260">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="4d673-260">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="4d673-261">Ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="4d673-261">Reason Code</span></span> | <span data-ttu-id="4d673-262">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="4d673-262">cdm_reasoncode</span></span> |
| <span data-ttu-id="4d673-263">Útgáfustofnun persónuskilríkja</span><span class="sxs-lookup"><span data-stu-id="4d673-263">Person Identification Issuing Agency</span></span> | <span data-ttu-id="4d673-264">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="4d673-264">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="4d673-265">Hæfnieiningar</span><span class="sxs-lookup"><span data-stu-id="4d673-265">Competency entities</span></span>

| <span data-ttu-id="4d673-266">Nafn</span><span class="sxs-lookup"><span data-stu-id="4d673-266">Name</span></span> | <span data-ttu-id="4d673-267">Eining</span><span class="sxs-lookup"><span data-stu-id="4d673-267">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4d673-268">Gerð hæfni</span><span class="sxs-lookup"><span data-stu-id="4d673-268">Skill Type</span></span> | <span data-ttu-id="4d673-269">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="4d673-269">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="4d673-270">Einingaþáttur tengslalíkanseiningar</span><span class="sxs-lookup"><span data-stu-id="4d673-270">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="4d673-271">Starfskraftur</span><span class="sxs-lookup"><span data-stu-id="4d673-271">Worker</span></span>

![Starfskraftur](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="4d673-273">Starf og starfstaða</span><span class="sxs-lookup"><span data-stu-id="4d673-273">Job and Job Position</span></span>

![Starf og starfstaða](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="4d673-275">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="4d673-275">Benefits</span></span>

![Fríðindi](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="4d673-277">Laun</span><span class="sxs-lookup"><span data-stu-id="4d673-277">Compensation</span></span>

![Laun](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="4d673-279">Hætta</span><span class="sxs-lookup"><span data-stu-id="4d673-279">Leave</span></span>

![Hætta](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="4d673-281">Vinnudagatal</span><span class="sxs-lookup"><span data-stu-id="4d673-281">Work Calendar</span></span>

![Vinnudagatal](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="4d673-283">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4d673-283">See also</span></span>

[<span data-ttu-id="4d673-284">Velja tækni við samþættingu gagna</span><span class="sxs-lookup"><span data-stu-id="4d673-284">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="4d673-285">Skilgreina Common Data Service-samþættingu</span><span class="sxs-lookup"><span data-stu-id="4d673-285">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)
