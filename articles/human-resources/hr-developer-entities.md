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
ms.openlocfilehash: 6879a45dd1fcc1ba718747aaaf0d7936c2eac49f
ms.sourcegitcommit: 3cad15f8ecc257d3a45c1bc1fada7c094ff4bcec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087347"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="8a1a3-103">Common Data Service einingar</span><span class="sxs-lookup"><span data-stu-id="8a1a3-103">Common Data Service entities</span></span>

<span data-ttu-id="8a1a3-104">Microsoft Dynamics 365 Human Resources notar Common Data Service til að gera mögulegt atburðarás fyrir stækkun og samþættingu.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="8a1a3-105">Nánari upplýsingar um Common Data Service er að finna í [Hvað er Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span><span class="sxs-lookup"><span data-stu-id="8a1a3-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="8a1a3-106">Eftirfarandi einingar Human Resources eru í boði í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="8a1a3-107">Fríðindaeiningar</span><span class="sxs-lookup"><span data-stu-id="8a1a3-107">Benefit entities</span></span>

| <span data-ttu-id="8a1a3-108">Nafn</span><span class="sxs-lookup"><span data-stu-id="8a1a3-108">Name</span></span> | <span data-ttu-id="8a1a3-109">Eining</span><span class="sxs-lookup"><span data-stu-id="8a1a3-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="8a1a3-110">Útreikningstíðni fríðinda</span><span class="sxs-lookup"><span data-stu-id="8a1a3-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="8a1a3-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="8a1a3-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="8a1a3-112">Útreikningsíðni fríðinda á launatímabili</span><span class="sxs-lookup"><span data-stu-id="8a1a3-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="8a1a3-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="8a1a3-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="8a1a3-114">Hlutfall útreikninga fyrir fríðindi</span><span class="sxs-lookup"><span data-stu-id="8a1a3-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="8a1a3-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="8a1a3-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="8a1a3-116">Upplýsingar um hlutfall útreikninga fyrir fríðindi</span><span class="sxs-lookup"><span data-stu-id="8a1a3-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="8a1a3-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="8a1a3-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="8a1a3-118">Fríðindavalkostur</span><span class="sxs-lookup"><span data-stu-id="8a1a3-118">Benefit Option</span></span> | <span data-ttu-id="8a1a3-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="8a1a3-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="8a1a3-120">Fríðindaáætlun</span><span class="sxs-lookup"><span data-stu-id="8a1a3-120">Benefit Plan</span></span> | <span data-ttu-id="8a1a3-121">cdm_benefitplan (Ekki virkjað fyrir sérsniðinn reitastuðning)</span><span class="sxs-lookup"><span data-stu-id="8a1a3-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="8a1a3-122">Gerð fríðinda</span><span class="sxs-lookup"><span data-stu-id="8a1a3-122">Benefit Type</span></span> | <span data-ttu-id="8a1a3-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="8a1a3-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="8a1a3-124">Einingar viðskiptaferlaverka</span><span class="sxs-lookup"><span data-stu-id="8a1a3-124">Business process tasks entities</span></span>

| <span data-ttu-id="8a1a3-125">Nafn</span><span class="sxs-lookup"><span data-stu-id="8a1a3-125">Name</span></span> | <span data-ttu-id="8a1a3-126">Eining</span><span class="sxs-lookup"><span data-stu-id="8a1a3-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="8a1a3-127">Dagatal viðskiptaferlis</span><span class="sxs-lookup"><span data-stu-id="8a1a3-127">Business Process Calendar</span></span> | <span data-ttu-id="8a1a3-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="8a1a3-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="8a1a3-129">Hópverkefni viðskiptaferlis</span><span class="sxs-lookup"><span data-stu-id="8a1a3-129">Business Process Group Assignment</span></span> | <span data-ttu-id="8a1a3-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="8a1a3-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="8a1a3-131">Verkhópur viðskiptaferlissafns</span><span class="sxs-lookup"><span data-stu-id="8a1a3-131">Business Process Library Task Group</span></span> | <span data-ttu-id="8a1a3-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="8a1a3-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="8a1a3-133">Stig viðskiptaferlis</span><span class="sxs-lookup"><span data-stu-id="8a1a3-133">Business Process Stage</span></span> | <span data-ttu-id="8a1a3-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="8a1a3-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="8a1a3-135">Haus gátlistasniðmáts</span><span class="sxs-lookup"><span data-stu-id="8a1a3-135">Checklist Template Header</span></span> | <span data-ttu-id="8a1a3-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="8a1a3-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="8a1a3-137">Verkefni gátlistasniðmáts</span><span class="sxs-lookup"><span data-stu-id="8a1a3-137">Checklist Template Task</span></span> | <span data-ttu-id="8a1a3-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="8a1a3-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="8a1a3-139">Bótaeiningar</span><span class="sxs-lookup"><span data-stu-id="8a1a3-139">Compensation entities</span></span>

| <span data-ttu-id="8a1a3-140">Nafn</span><span class="sxs-lookup"><span data-stu-id="8a1a3-140">Name</span></span> | <span data-ttu-id="8a1a3-141">Eining</span><span class="sxs-lookup"><span data-stu-id="8a1a3-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="8a1a3-142">Fyrirkomulag fastra launa</span><span class="sxs-lookup"><span data-stu-id="8a1a3-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="8a1a3-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="8a1a3-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="8a1a3-144">Launanet</span><span class="sxs-lookup"><span data-stu-id="8a1a3-144">Compensation Grid</span></span> | <span data-ttu-id="8a1a3-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="8a1a3-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="8a1a3-146">Launastig</span><span class="sxs-lookup"><span data-stu-id="8a1a3-146">Compensation Level</span></span> | <span data-ttu-id="8a1a3-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="8a1a3-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="8a1a3-148">Greiðslutíðni launa</span><span class="sxs-lookup"><span data-stu-id="8a1a3-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="8a1a3-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="8a1a3-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="8a1a3-150">Uppsetning á tilvísunarpunkti launa</span><span class="sxs-lookup"><span data-stu-id="8a1a3-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="8a1a3-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="8a1a3-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="8a1a3-152">Setja upp línu tilvísunarpunkts launa</span><span class="sxs-lookup"><span data-stu-id="8a1a3-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="8a1a3-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="8a1a3-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="8a1a3-154">Launasvæði</span><span class="sxs-lookup"><span data-stu-id="8a1a3-154">Compensation Region</span></span> | <span data-ttu-id="8a1a3-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="8a1a3-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="8a1a3-156">Launaskipulag</span><span class="sxs-lookup"><span data-stu-id="8a1a3-156">Compensation Structure</span></span> | <span data-ttu-id="8a1a3-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="8a1a3-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="8a1a3-158">Fyrirkomulag breytilegra uppbóta</span><span class="sxs-lookup"><span data-stu-id="8a1a3-158">Compensation Variable Plan</span></span> | <span data-ttu-id="8a1a3-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="8a1a3-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="8a1a3-160">Fyrirkomulagsstig breytilegra uppbóta</span><span class="sxs-lookup"><span data-stu-id="8a1a3-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="8a1a3-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="8a1a3-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="8a1a3-162">Fyrirkomulagsgerð breytilegra uppbóta</span><span class="sxs-lookup"><span data-stu-id="8a1a3-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="8a1a3-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="8a1a3-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="8a1a3-164">Fast launatilvik</span><span class="sxs-lookup"><span data-stu-id="8a1a3-164">Fixed Compensation Event</span></span> | <span data-ttu-id="8a1a3-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="8a1a3-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="8a1a3-166">Veitiregla</span><span class="sxs-lookup"><span data-stu-id="8a1a3-166">Vesting Rule</span></span> | <span data-ttu-id="8a1a3-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="8a1a3-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="8a1a3-168">Föst laun starfskrafts</span><span class="sxs-lookup"><span data-stu-id="8a1a3-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="8a1a3-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="8a1a3-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="8a1a3-170">Fyrirtækjaeiningar</span><span class="sxs-lookup"><span data-stu-id="8a1a3-170">Organization entities</span></span>

| <span data-ttu-id="8a1a3-171">Nafn</span><span class="sxs-lookup"><span data-stu-id="8a1a3-171">Name</span></span> | <span data-ttu-id="8a1a3-172">Eining</span><span class="sxs-lookup"><span data-stu-id="8a1a3-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="8a1a3-173">Deild</span><span class="sxs-lookup"><span data-stu-id="8a1a3-173">Department</span></span> | <span data-ttu-id="8a1a3-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="8a1a3-174">cdm_department</span></span> |
| <span data-ttu-id="8a1a3-175">Ráðning</span><span class="sxs-lookup"><span data-stu-id="8a1a3-175">Employment</span></span> | <span data-ttu-id="8a1a3-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="8a1a3-176">cdm_employment</span></span> |
| <span data-ttu-id="8a1a3-177">Fyrirt.</span><span class="sxs-lookup"><span data-stu-id="8a1a3-177">Company</span></span> | <span data-ttu-id="8a1a3-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="8a1a3-178">cdm_company</span></span> |
| <span data-ttu-id="8a1a3-179">Vinnsla</span><span class="sxs-lookup"><span data-stu-id="8a1a3-179">Job</span></span> | <span data-ttu-id="8a1a3-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="8a1a3-180">cdm_job</span></span> |
| <span data-ttu-id="8a1a3-181">Starfshlutverk</span><span class="sxs-lookup"><span data-stu-id="8a1a3-181">Job Function</span></span> | <span data-ttu-id="8a1a3-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="8a1a3-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="8a1a3-183">Staða starfs</span><span class="sxs-lookup"><span data-stu-id="8a1a3-183">Job Position</span></span> | <span data-ttu-id="8a1a3-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="8a1a3-184">cdm_jobposition</span></span> |
| <span data-ttu-id="8a1a3-185">Gerð stöðu</span><span class="sxs-lookup"><span data-stu-id="8a1a3-185">Position Type</span></span> | <span data-ttu-id="8a1a3-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="8a1a3-186">cdm_positiontype</span></span> |
| <span data-ttu-id="8a1a3-187">Stöðuúthlutun starfskrafts</span><span class="sxs-lookup"><span data-stu-id="8a1a3-187">Position Worker Assignment</span></span> | <span data-ttu-id="8a1a3-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="8a1a3-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="8a1a3-189">Starfsgerð</span><span class="sxs-lookup"><span data-stu-id="8a1a3-189">Job Type</span></span> | <span data-ttu-id="8a1a3-190">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="8a1a3-190">cdm_jobtype</span></span> |
| <span data-ttu-id="8a1a3-191">Tungumál</span><span class="sxs-lookup"><span data-stu-id="8a1a3-191">Language</span></span> | <span data-ttu-id="8a1a3-192">cdm_language</span><span class="sxs-lookup"><span data-stu-id="8a1a3-192">cdm_language</span></span> |

## <a name="leave-and-absence-entities"></a><span data-ttu-id="8a1a3-193">Einingar fyrir leyfi og fjarvistir</span><span class="sxs-lookup"><span data-stu-id="8a1a3-193">Leave and absence entities</span></span>

| <span data-ttu-id="8a1a3-194">Nafn</span><span class="sxs-lookup"><span data-stu-id="8a1a3-194">Name</span></span> | <span data-ttu-id="8a1a3-195">Eining</span><span class="sxs-lookup"><span data-stu-id="8a1a3-195">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="8a1a3-196">Orlofsbankafærsla</span><span class="sxs-lookup"><span data-stu-id="8a1a3-196">Leave Bank Transaction</span></span> | <span data-ttu-id="8a1a3-197">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="8a1a3-197">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="8a1a3-198">Orlofsskráning</span><span class="sxs-lookup"><span data-stu-id="8a1a3-198">Leave Enrollment</span></span> | <span data-ttu-id="8a1a3-199">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="8a1a3-199">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="8a1a3-200">Leyfisáætlun</span><span class="sxs-lookup"><span data-stu-id="8a1a3-200">Leave Plan</span></span> | <span data-ttu-id="8a1a3-201">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="8a1a3-201">cdm_leaveplan</span></span> |
| <span data-ttu-id="8a1a3-202">Orlofsbeiðni</span><span class="sxs-lookup"><span data-stu-id="8a1a3-202">Leave Request</span></span> | <span data-ttu-id="8a1a3-203">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="8a1a3-203">cdm_leaverequest</span></span> |
| <span data-ttu-id="8a1a3-204">Upplýsingar um orlofsbeiðni</span><span class="sxs-lookup"><span data-stu-id="8a1a3-204">Leave Request Detail</span></span> | <span data-ttu-id="8a1a3-205">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="8a1a3-205">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="8a1a3-206">Gerð leyfis</span><span class="sxs-lookup"><span data-stu-id="8a1a3-206">Leave Type</span></span> | <span data-ttu-id="8a1a3-207">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="8a1a3-207">cdm_leavetype</span></span> |
| <span data-ttu-id="8a1a3-208">Ástæðukóði orlofsgerðar</span><span class="sxs-lookup"><span data-stu-id="8a1a3-208">Leave Type Reason Code</span></span> | <span data-ttu-id="8a1a3-209">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="8a1a3-209">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="8a1a3-210">Launaeiningar</span><span class="sxs-lookup"><span data-stu-id="8a1a3-210">Payroll entities</span></span>

| <span data-ttu-id="8a1a3-211">Nafn</span><span class="sxs-lookup"><span data-stu-id="8a1a3-211">Name</span></span> | <span data-ttu-id="8a1a3-212">Eining</span><span class="sxs-lookup"><span data-stu-id="8a1a3-212">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="8a1a3-213">Greiðsluferli</span><span class="sxs-lookup"><span data-stu-id="8a1a3-213">Pay Cycle</span></span> | <span data-ttu-id="8a1a3-214">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="8a1a3-214">cdm_paycycle</span></span> |
| <span data-ttu-id="8a1a3-215">Launatímabil</span><span class="sxs-lookup"><span data-stu-id="8a1a3-215">Pay Period</span></span> | <span data-ttu-id="8a1a3-216">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="8a1a3-216">cdm_payperiod</span></span> |
| <span data-ttu-id="8a1a3-217">Tekjukóði launa</span><span class="sxs-lookup"><span data-stu-id="8a1a3-217">Payroll Earning Code</span></span> | <span data-ttu-id="8a1a3-218">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="8a1a3-218">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="8a1a3-219">Bankareikningsgreiðslur</span><span class="sxs-lookup"><span data-stu-id="8a1a3-219">Bank Account Disbursement</span></span> | <span data-ttu-id="8a1a3-220">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="8a1a3-220">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="8a1a3-221">Skattumdæmi</span><span class="sxs-lookup"><span data-stu-id="8a1a3-221">Tax Region</span></span> | <span data-ttu-id="8a1a3-222">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="8a1a3-222">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="8a1a3-223">Starfskraftaeiningar</span><span class="sxs-lookup"><span data-stu-id="8a1a3-223">Worker entities</span></span>

| <span data-ttu-id="8a1a3-224">Nafn</span><span class="sxs-lookup"><span data-stu-id="8a1a3-224">Name</span></span> | <span data-ttu-id="8a1a3-225">Eining</span><span class="sxs-lookup"><span data-stu-id="8a1a3-225">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="8a1a3-226">Starfskraftur</span><span class="sxs-lookup"><span data-stu-id="8a1a3-226">Worker</span></span> | <span data-ttu-id="8a1a3-227">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="8a1a3-227">cdm_worker</span></span> |
| <span data-ttu-id="8a1a3-228">Aðsetur starfskrafts</span><span class="sxs-lookup"><span data-stu-id="8a1a3-228">Worker Address</span></span> | <span data-ttu-id="8a1a3-229">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="8a1a3-229">cdm_workeraddress</span></span> |
| <span data-ttu-id="8a1a3-230">Persónuupplýsingar starfskrafts</span><span class="sxs-lookup"><span data-stu-id="8a1a3-230">Worker Personal Detail</span></span> | <span data-ttu-id="8a1a3-231">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="8a1a3-231">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="8a1a3-232">Kennitala starfskrafts</span><span class="sxs-lookup"><span data-stu-id="8a1a3-232">Worker Person Identification Number</span></span> | <span data-ttu-id="8a1a3-233">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="8a1a3-233">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="8a1a3-234">Persónukennisgerð starfskrafts</span><span class="sxs-lookup"><span data-stu-id="8a1a3-234">Worker Person Identification Type</span></span> | <span data-ttu-id="8a1a3-235">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="8a1a3-235">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="8a1a3-236">Vinnudagatal</span><span class="sxs-lookup"><span data-stu-id="8a1a3-236">Work Calendar</span></span> | <span data-ttu-id="8a1a3-237">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="8a1a3-237">cdm_workcalendar</span></span> |
| <span data-ttu-id="8a1a3-238">Dagur í vinnudagatali</span><span class="sxs-lookup"><span data-stu-id="8a1a3-238">Work Calendar Day</span></span> | <span data-ttu-id="8a1a3-239">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="8a1a3-239">cdm_workcalendarday</span></span> |
| <span data-ttu-id="8a1a3-240">Frídagur í vinnudagatali</span><span class="sxs-lookup"><span data-stu-id="8a1a3-240">Work Calendar Holiday</span></span> |<span data-ttu-id="8a1a3-241">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="8a1a3-241">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="8a1a3-242">Frídagslína í vinnudagatali</span><span class="sxs-lookup"><span data-stu-id="8a1a3-242">Work Calendar Holiday Line</span></span> | <span data-ttu-id="8a1a3-243">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="8a1a3-243">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="8a1a3-244">Tímabil vinnudagatals</span><span class="sxs-lookup"><span data-stu-id="8a1a3-244">Work Calendar Time Interval</span></span> | <span data-ttu-id="8a1a3-245">cdm_workcalendartimeinterval (Ekki virkjað fyrir sérsniðinn reitastuðning)</span><span class="sxs-lookup"><span data-stu-id="8a1a3-245">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="8a1a3-246">Bankareikningur starfskrafts</span><span class="sxs-lookup"><span data-stu-id="8a1a3-246">Worker Bank Account</span></span> | <span data-ttu-id="8a1a3-247">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="8a1a3-247">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="8a1a3-248">Uppsetningareiningar starfskrafts</span><span class="sxs-lookup"><span data-stu-id="8a1a3-248">Worker setup entities</span></span>

| <span data-ttu-id="8a1a3-249">Nafn</span><span class="sxs-lookup"><span data-stu-id="8a1a3-249">Name</span></span> | <span data-ttu-id="8a1a3-250">Eining</span><span class="sxs-lookup"><span data-stu-id="8a1a3-250">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="8a1a3-251">Uppgjafahermaður</span><span class="sxs-lookup"><span data-stu-id="8a1a3-251">Veteran Status</span></span> | <span data-ttu-id="8a1a3-252">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="8a1a3-252">cdm_veteranstatus</span></span> |
| <span data-ttu-id="8a1a3-253">Þjóðernisuppruni</span><span class="sxs-lookup"><span data-stu-id="8a1a3-253">Ethnic Origin</span></span> | <span data-ttu-id="8a1a3-254">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="8a1a3-254">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="8a1a3-255">Ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="8a1a3-255">Reason Code</span></span> | <span data-ttu-id="8a1a3-256">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="8a1a3-256">cdm_reasoncode</span></span> |
| <span data-ttu-id="8a1a3-257">Útgáfustofnun persónuskilríkja</span><span class="sxs-lookup"><span data-stu-id="8a1a3-257">Person Identification Issuing Agency</span></span> | <span data-ttu-id="8a1a3-258">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="8a1a3-258">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="8a1a3-259">Hæfnieiningar</span><span class="sxs-lookup"><span data-stu-id="8a1a3-259">Competency entities</span></span>

| <span data-ttu-id="8a1a3-260">Nafn</span><span class="sxs-lookup"><span data-stu-id="8a1a3-260">Name</span></span> | <span data-ttu-id="8a1a3-261">Eining</span><span class="sxs-lookup"><span data-stu-id="8a1a3-261">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="8a1a3-262">Gerð hæfni</span><span class="sxs-lookup"><span data-stu-id="8a1a3-262">Skill Type</span></span> | <span data-ttu-id="8a1a3-263">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="8a1a3-263">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="8a1a3-264">Einingaþáttur tengslalíkanseiningar</span><span class="sxs-lookup"><span data-stu-id="8a1a3-264">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="8a1a3-265">Starfskraftur</span><span class="sxs-lookup"><span data-stu-id="8a1a3-265">Worker</span></span>

![Starfskraftur](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="8a1a3-267">Starf og starfstaða</span><span class="sxs-lookup"><span data-stu-id="8a1a3-267">Job and Job Position</span></span>

![Starf og starfstaða](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="8a1a3-269">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="8a1a3-269">Benefits</span></span>

![Fríðindi](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="8a1a3-271">Laun</span><span class="sxs-lookup"><span data-stu-id="8a1a3-271">Compensation</span></span>

![Laun](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="8a1a3-273">Hætta</span><span class="sxs-lookup"><span data-stu-id="8a1a3-273">Leave</span></span>

![Hætta](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="8a1a3-275">Vinnudagatal</span><span class="sxs-lookup"><span data-stu-id="8a1a3-275">Work Calendar</span></span>

![Vinnudagatal](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="8a1a3-277">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="8a1a3-277">See also</span></span>

[<span data-ttu-id="8a1a3-278">Velja tækni við samþættingu gagna</span><span class="sxs-lookup"><span data-stu-id="8a1a3-278">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="8a1a3-279">Skilgreina Common Data Service-samþættingu</span><span class="sxs-lookup"><span data-stu-id="8a1a3-279">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)