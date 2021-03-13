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
ms.openlocfilehash: 2f075a8e96af55b1363d2d51db377c5b25c38775
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113002"
---
# <a name="dataverse-tables"></a><span data-ttu-id="9f7b4-103">Dataverse töflur</span><span class="sxs-lookup"><span data-stu-id="9f7b4-103">Dataverse tables</span></span>

<span data-ttu-id="9f7b4-104">Microsoft Dynamics 365 Human Resources notar Dataverse til að gera mögulegt atburðarás fyrir stækkun og samþættingu.</span><span class="sxs-lookup"><span data-stu-id="9f7b4-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="9f7b4-105">Mannauðseiningar samsvara Dataverse töflum.</span><span class="sxs-lookup"><span data-stu-id="9f7b4-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="9f7b4-106">Frekari upplýsingar um Dataverse (áður Common Data Service) og uppfærslur á hugtökum er að finna í [Hvað er Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span><span class="sxs-lookup"><span data-stu-id="9f7b4-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="9f7b4-107">Eftirfarandi Dataverse-töflur eru í boði sem byggja á einingum Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9f7b4-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="9f7b4-108">Fríðindatöflur</span><span class="sxs-lookup"><span data-stu-id="9f7b4-108">Benefit tables</span></span>

| <span data-ttu-id="9f7b4-109">Nafn</span><span class="sxs-lookup"><span data-stu-id="9f7b4-109">Name</span></span> | <span data-ttu-id="9f7b4-110">Tafla</span><span class="sxs-lookup"><span data-stu-id="9f7b4-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9f7b4-111">Útreikningstíðni fríðinda</span><span class="sxs-lookup"><span data-stu-id="9f7b4-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="9f7b4-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="9f7b4-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="9f7b4-113">Útreikningsíðni fríðinda á launatímabili</span><span class="sxs-lookup"><span data-stu-id="9f7b4-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="9f7b4-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="9f7b4-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="9f7b4-115">Hlutfall útreikninga fyrir fríðindi</span><span class="sxs-lookup"><span data-stu-id="9f7b4-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="9f7b4-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="9f7b4-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="9f7b4-117">Upplýsingar um hlutfall útreikninga fyrir fríðindi</span><span class="sxs-lookup"><span data-stu-id="9f7b4-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="9f7b4-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="9f7b4-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="9f7b4-119">Fríðindavalkostur</span><span class="sxs-lookup"><span data-stu-id="9f7b4-119">Benefit Option</span></span> | <span data-ttu-id="9f7b4-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="9f7b4-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="9f7b4-121">Fríðindaáætlun</span><span class="sxs-lookup"><span data-stu-id="9f7b4-121">Benefit Plan</span></span> | <span data-ttu-id="9f7b4-122">cdm_benefitplan (Ekki virkjað fyrir sérsniðinn reitastuðning)</span><span class="sxs-lookup"><span data-stu-id="9f7b4-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="9f7b4-123">Gerð fríðinda</span><span class="sxs-lookup"><span data-stu-id="9f7b4-123">Benefit Type</span></span> | <span data-ttu-id="9f7b4-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="9f7b4-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="9f7b4-125">Verkefnatöflur viðskiptaferlis</span><span class="sxs-lookup"><span data-stu-id="9f7b4-125">Business process tasks tables</span></span>

| <span data-ttu-id="9f7b4-126">Nafn</span><span class="sxs-lookup"><span data-stu-id="9f7b4-126">Name</span></span> | <span data-ttu-id="9f7b4-127">Tafla</span><span class="sxs-lookup"><span data-stu-id="9f7b4-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9f7b4-128">Dagatal viðskiptaferlis</span><span class="sxs-lookup"><span data-stu-id="9f7b4-128">Business Process Calendar</span></span> | <span data-ttu-id="9f7b4-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="9f7b4-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="9f7b4-130">Hópverkefni viðskiptaferlis</span><span class="sxs-lookup"><span data-stu-id="9f7b4-130">Business Process Group Assignment</span></span> | <span data-ttu-id="9f7b4-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="9f7b4-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="9f7b4-132">Verkhópur viðskiptaferlissafns</span><span class="sxs-lookup"><span data-stu-id="9f7b4-132">Business Process Library Task Group</span></span> | <span data-ttu-id="9f7b4-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="9f7b4-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="9f7b4-134">Stig viðskiptaferlis</span><span class="sxs-lookup"><span data-stu-id="9f7b4-134">Business Process Stage</span></span> | <span data-ttu-id="9f7b4-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="9f7b4-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="9f7b4-136">Haus gátlistasniðmáts</span><span class="sxs-lookup"><span data-stu-id="9f7b4-136">Checklist Template Header</span></span> | <span data-ttu-id="9f7b4-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="9f7b4-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="9f7b4-138">Verkefni gátlistasniðmáts</span><span class="sxs-lookup"><span data-stu-id="9f7b4-138">Checklist Template Task</span></span> | <span data-ttu-id="9f7b4-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="9f7b4-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="9f7b4-140">Launatöflur</span><span class="sxs-lookup"><span data-stu-id="9f7b4-140">Compensation tables</span></span>

| <span data-ttu-id="9f7b4-141">Nafn</span><span class="sxs-lookup"><span data-stu-id="9f7b4-141">Name</span></span> | <span data-ttu-id="9f7b4-142">Tafla</span><span class="sxs-lookup"><span data-stu-id="9f7b4-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9f7b4-143">Fyrirkomulag fastra launa</span><span class="sxs-lookup"><span data-stu-id="9f7b4-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="9f7b4-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="9f7b4-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="9f7b4-145">Launanet</span><span class="sxs-lookup"><span data-stu-id="9f7b4-145">Compensation Grid</span></span> | <span data-ttu-id="9f7b4-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="9f7b4-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="9f7b4-147">Launastig</span><span class="sxs-lookup"><span data-stu-id="9f7b4-147">Compensation Level</span></span> | <span data-ttu-id="9f7b4-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="9f7b4-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="9f7b4-149">Greiðslutíðni launa</span><span class="sxs-lookup"><span data-stu-id="9f7b4-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="9f7b4-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="9f7b4-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="9f7b4-151">Uppsetning á tilvísunarpunkti launa</span><span class="sxs-lookup"><span data-stu-id="9f7b4-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="9f7b4-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="9f7b4-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="9f7b4-153">Setja upp línu tilvísunarpunkts launa</span><span class="sxs-lookup"><span data-stu-id="9f7b4-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="9f7b4-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="9f7b4-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="9f7b4-155">Launasvæði</span><span class="sxs-lookup"><span data-stu-id="9f7b4-155">Compensation Region</span></span> | <span data-ttu-id="9f7b4-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="9f7b4-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="9f7b4-157">Launaskipulag</span><span class="sxs-lookup"><span data-stu-id="9f7b4-157">Compensation Structure</span></span> | <span data-ttu-id="9f7b4-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="9f7b4-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="9f7b4-159">Fyrirkomulag breytilegra uppbóta</span><span class="sxs-lookup"><span data-stu-id="9f7b4-159">Compensation Variable Plan</span></span> | <span data-ttu-id="9f7b4-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="9f7b4-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="9f7b4-161">Fyrirkomulagsstig breytilegra uppbóta</span><span class="sxs-lookup"><span data-stu-id="9f7b4-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="9f7b4-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="9f7b4-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="9f7b4-163">Fyrirkomulagsgerð breytilegra uppbóta</span><span class="sxs-lookup"><span data-stu-id="9f7b4-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="9f7b4-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="9f7b4-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="9f7b4-165">Fast launatilvik</span><span class="sxs-lookup"><span data-stu-id="9f7b4-165">Fixed Compensation Event</span></span> | <span data-ttu-id="9f7b4-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="9f7b4-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="9f7b4-167">Veitiregla</span><span class="sxs-lookup"><span data-stu-id="9f7b4-167">Vesting Rule</span></span> | <span data-ttu-id="9f7b4-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="9f7b4-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="9f7b4-169">Föst laun starfskrafts</span><span class="sxs-lookup"><span data-stu-id="9f7b4-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="9f7b4-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="9f7b4-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="9f7b4-171">Fyrirtækistöflur</span><span class="sxs-lookup"><span data-stu-id="9f7b4-171">Organization tables</span></span>

| <span data-ttu-id="9f7b4-172">Nafn</span><span class="sxs-lookup"><span data-stu-id="9f7b4-172">Name</span></span> | <span data-ttu-id="9f7b4-173">Tafla</span><span class="sxs-lookup"><span data-stu-id="9f7b4-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9f7b4-174">Deild</span><span class="sxs-lookup"><span data-stu-id="9f7b4-174">Department</span></span> | <span data-ttu-id="9f7b4-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="9f7b4-175">cdm_department</span></span> |
| <span data-ttu-id="9f7b4-176">Ráðning</span><span class="sxs-lookup"><span data-stu-id="9f7b4-176">Employment</span></span> | <span data-ttu-id="9f7b4-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="9f7b4-177">cdm_employment</span></span> |
| <span data-ttu-id="9f7b4-178">Fyrirt.  </span><span class="sxs-lookup"><span data-stu-id="9f7b4-178">Company</span></span> | <span data-ttu-id="9f7b4-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="9f7b4-179">cdm_company</span></span> |
| <span data-ttu-id="9f7b4-180">Vinnsla</span><span class="sxs-lookup"><span data-stu-id="9f7b4-180">Job</span></span> | <span data-ttu-id="9f7b4-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="9f7b4-181">cdm_job</span></span> |
| <span data-ttu-id="9f7b4-182">Starfshlutverk</span><span class="sxs-lookup"><span data-stu-id="9f7b4-182">Job Function</span></span> | <span data-ttu-id="9f7b4-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="9f7b4-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="9f7b4-184">Staða starfs</span><span class="sxs-lookup"><span data-stu-id="9f7b4-184">Job Position</span></span> | <span data-ttu-id="9f7b4-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="9f7b4-185">cdm_jobposition</span></span> |
| <span data-ttu-id="9f7b4-186">Gerð stöðu</span><span class="sxs-lookup"><span data-stu-id="9f7b4-186">Position Type</span></span> | <span data-ttu-id="9f7b4-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="9f7b4-187">cdm_positiontype</span></span> |
| <span data-ttu-id="9f7b4-188">Stöðuúthlutun starfskrafts</span><span class="sxs-lookup"><span data-stu-id="9f7b4-188">Position Worker Assignment</span></span> | <span data-ttu-id="9f7b4-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="9f7b4-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="9f7b4-190">Vídd stöðu starfs</span><span class="sxs-lookup"><span data-stu-id="9f7b4-190">Job Position Dimension</span></span> | <span data-ttu-id="9f7b4-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="9f7b4-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="9f7b4-192">Starfsgerð</span><span class="sxs-lookup"><span data-stu-id="9f7b4-192">Job Type</span></span> | <span data-ttu-id="9f7b4-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="9f7b4-193">cdm_jobtype</span></span> |
| <span data-ttu-id="9f7b4-194">Tungumál</span><span class="sxs-lookup"><span data-stu-id="9f7b4-194">Language</span></span> | <span data-ttu-id="9f7b4-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="9f7b4-195">cdm_language</span></span> |
| <span data-ttu-id="9f7b4-196">Titill</span><span class="sxs-lookup"><span data-stu-id="9f7b4-196">Title</span></span> | <span data-ttu-id="9f7b4-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="9f7b4-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="9f7b4-198">Fjárhagslegar víddir fyrir **Gerð stöðu**, **Stöðuúthlutun starfskrafts** og **Starf** veita einnar áttar samþættingu við Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9f7b4-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="9f7b4-199">Uppfærslur fjárhagsvídda samstillast ekki eins og stendur úr Dataverse í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9f7b4-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="9f7b4-200">Leyfis- og fjarvistatöflur</span><span class="sxs-lookup"><span data-stu-id="9f7b4-200">Leave and absence tables</span></span>

| <span data-ttu-id="9f7b4-201">Nafn</span><span class="sxs-lookup"><span data-stu-id="9f7b4-201">Name</span></span> | <span data-ttu-id="9f7b4-202">Tafla</span><span class="sxs-lookup"><span data-stu-id="9f7b4-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9f7b4-203">Orlofsbankafærsla</span><span class="sxs-lookup"><span data-stu-id="9f7b4-203">Leave Bank Transaction</span></span> | <span data-ttu-id="9f7b4-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="9f7b4-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="9f7b4-205">Orlofsskráning</span><span class="sxs-lookup"><span data-stu-id="9f7b4-205">Leave Enrollment</span></span> | <span data-ttu-id="9f7b4-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="9f7b4-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="9f7b4-207">Leyfisáætlun</span><span class="sxs-lookup"><span data-stu-id="9f7b4-207">Leave Plan</span></span> | <span data-ttu-id="9f7b4-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="9f7b4-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="9f7b4-209">Orlofsbeiðni</span><span class="sxs-lookup"><span data-stu-id="9f7b4-209">Leave Request</span></span> | <span data-ttu-id="9f7b4-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="9f7b4-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="9f7b4-211">Upplýsingar um orlofsbeiðni</span><span class="sxs-lookup"><span data-stu-id="9f7b4-211">Leave Request Detail</span></span> | <span data-ttu-id="9f7b4-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="9f7b4-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="9f7b4-213">Gerð leyfis</span><span class="sxs-lookup"><span data-stu-id="9f7b4-213">Leave Type</span></span> | <span data-ttu-id="9f7b4-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="9f7b4-214">cdm_leavetype</span></span> |
| <span data-ttu-id="9f7b4-215">Ástæðukóði orlofsgerðar</span><span class="sxs-lookup"><span data-stu-id="9f7b4-215">Leave Type Reason Code</span></span> | <span data-ttu-id="9f7b4-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="9f7b4-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="9f7b4-217">Töflur launaskráar</span><span class="sxs-lookup"><span data-stu-id="9f7b4-217">Payroll tables</span></span>

| <span data-ttu-id="9f7b4-218">Nafn</span><span class="sxs-lookup"><span data-stu-id="9f7b4-218">Name</span></span> | <span data-ttu-id="9f7b4-219">Tafla</span><span class="sxs-lookup"><span data-stu-id="9f7b4-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9f7b4-220">Greiðsluferli</span><span class="sxs-lookup"><span data-stu-id="9f7b4-220">Pay Cycle</span></span> | <span data-ttu-id="9f7b4-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="9f7b4-221">cdm_paycycle</span></span> |
| <span data-ttu-id="9f7b4-222">Launatímabil</span><span class="sxs-lookup"><span data-stu-id="9f7b4-222">Pay Period</span></span> | <span data-ttu-id="9f7b4-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="9f7b4-223">cdm_payperiod</span></span> |
| <span data-ttu-id="9f7b4-224">Tekjukóði launa</span><span class="sxs-lookup"><span data-stu-id="9f7b4-224">Payroll Earning Code</span></span> | <span data-ttu-id="9f7b4-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="9f7b4-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="9f7b4-226">Bankareikningsgreiðslur</span><span class="sxs-lookup"><span data-stu-id="9f7b4-226">Bank Account Disbursement</span></span> | <span data-ttu-id="9f7b4-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="9f7b4-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="9f7b4-228">Skattumdæmi</span><span class="sxs-lookup"><span data-stu-id="9f7b4-228">Tax Region</span></span> | <span data-ttu-id="9f7b4-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="9f7b4-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="9f7b4-230">Starfsmannatöflur</span><span class="sxs-lookup"><span data-stu-id="9f7b4-230">Worker tables</span></span>

| <span data-ttu-id="9f7b4-231">Nafn</span><span class="sxs-lookup"><span data-stu-id="9f7b4-231">Name</span></span> | <span data-ttu-id="9f7b4-232">Tafla</span><span class="sxs-lookup"><span data-stu-id="9f7b4-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9f7b4-233">Starfsmaður</span><span class="sxs-lookup"><span data-stu-id="9f7b4-233">Worker</span></span> | <span data-ttu-id="9f7b4-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="9f7b4-234">cdm_worker</span></span> |
| <span data-ttu-id="9f7b4-235">Aðsetur starfskrafts</span><span class="sxs-lookup"><span data-stu-id="9f7b4-235">Worker Address</span></span> | <span data-ttu-id="9f7b4-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="9f7b4-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="9f7b4-237">Persónuupplýsingar starfskrafts</span><span class="sxs-lookup"><span data-stu-id="9f7b4-237">Worker Personal Detail</span></span> | <span data-ttu-id="9f7b4-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="9f7b4-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="9f7b4-239">Kennitala starfskrafts</span><span class="sxs-lookup"><span data-stu-id="9f7b4-239">Worker Person Identification Number</span></span> | <span data-ttu-id="9f7b4-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="9f7b4-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="9f7b4-241">Persónukennisgerð starfskrafts</span><span class="sxs-lookup"><span data-stu-id="9f7b4-241">Worker Person Identification Type</span></span> | <span data-ttu-id="9f7b4-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="9f7b4-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="9f7b4-243">Vinnudagatal</span><span class="sxs-lookup"><span data-stu-id="9f7b4-243">Work Calendar</span></span> | <span data-ttu-id="9f7b4-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="9f7b4-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="9f7b4-245">Dagur í vinnudagatali</span><span class="sxs-lookup"><span data-stu-id="9f7b4-245">Work Calendar Day</span></span> | <span data-ttu-id="9f7b4-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="9f7b4-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="9f7b4-247">Frídagur í vinnudagatali</span><span class="sxs-lookup"><span data-stu-id="9f7b4-247">Work Calendar Holiday</span></span> |<span data-ttu-id="9f7b4-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="9f7b4-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="9f7b4-249">Frídagslína í vinnudagatali</span><span class="sxs-lookup"><span data-stu-id="9f7b4-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="9f7b4-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="9f7b4-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="9f7b4-251">Tímabil vinnudagatals</span><span class="sxs-lookup"><span data-stu-id="9f7b4-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="9f7b4-252">cdm_workcalendartimeinterval (Ekki virkjað fyrir sérsniðinn reitastuðning)</span><span class="sxs-lookup"><span data-stu-id="9f7b4-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="9f7b4-253">Bankareikningur starfskrafts</span><span class="sxs-lookup"><span data-stu-id="9f7b4-253">Worker Bank Account</span></span> | <span data-ttu-id="9f7b4-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="9f7b4-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="9f7b4-255">Uppsetningartöflur starfsmanns</span><span class="sxs-lookup"><span data-stu-id="9f7b4-255">Worker setup tables</span></span>

| <span data-ttu-id="9f7b4-256">Nafn</span><span class="sxs-lookup"><span data-stu-id="9f7b4-256">Name</span></span> | <span data-ttu-id="9f7b4-257">Tafla</span><span class="sxs-lookup"><span data-stu-id="9f7b4-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9f7b4-258">Uppgjafahermaður</span><span class="sxs-lookup"><span data-stu-id="9f7b4-258">Veteran Status</span></span> | <span data-ttu-id="9f7b4-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="9f7b4-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="9f7b4-260">Þjóðernisuppruni</span><span class="sxs-lookup"><span data-stu-id="9f7b4-260">Ethnic Origin</span></span> | <span data-ttu-id="9f7b4-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="9f7b4-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="9f7b4-262">Ástæðukóði</span><span class="sxs-lookup"><span data-stu-id="9f7b4-262">Reason Code</span></span> | <span data-ttu-id="9f7b4-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="9f7b4-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="9f7b4-264">Útgáfustofnun persónuskilríkja</span><span class="sxs-lookup"><span data-stu-id="9f7b4-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="9f7b4-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="9f7b4-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="9f7b4-266">Hæfnistöflur</span><span class="sxs-lookup"><span data-stu-id="9f7b4-266">Competency tables</span></span>

| <span data-ttu-id="9f7b4-267">Nafn</span><span class="sxs-lookup"><span data-stu-id="9f7b4-267">Name</span></span> | <span data-ttu-id="9f7b4-268">Tafla</span><span class="sxs-lookup"><span data-stu-id="9f7b4-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="9f7b4-269">Gerð hæfni</span><span class="sxs-lookup"><span data-stu-id="9f7b4-269">Skill Type</span></span> | <span data-ttu-id="9f7b4-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="9f7b4-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="9f7b4-271">Líkön töfluvensla</span><span class="sxs-lookup"><span data-stu-id="9f7b4-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="9f7b4-272">Starfsmaður</span><span class="sxs-lookup"><span data-stu-id="9f7b4-272">Worker</span></span>

![Starfsmaður](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="9f7b4-274">Starf og starfstaða</span><span class="sxs-lookup"><span data-stu-id="9f7b4-274">Job and Job Position</span></span>

![Starf og starfstaða](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="9f7b4-276">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="9f7b4-276">Benefits</span></span>

![Fríðindi](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="9f7b4-278">Laun</span><span class="sxs-lookup"><span data-stu-id="9f7b4-278">Compensation</span></span>

![Laun](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="9f7b4-280">Hætta</span><span class="sxs-lookup"><span data-stu-id="9f7b4-280">Leave</span></span>

![Hætta](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="9f7b4-282">Vinnudagatal</span><span class="sxs-lookup"><span data-stu-id="9f7b4-282">Work Calendar</span></span>

![Vinnudagatal](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="9f7b4-284">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="9f7b4-284">See also</span></span>

[<span data-ttu-id="9f7b4-285">Velja tækni við samþættingu gagna</span><span class="sxs-lookup"><span data-stu-id="9f7b4-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="9f7b4-286">Skilgreina Dataverse-samþættingu</span><span class="sxs-lookup"><span data-stu-id="9f7b4-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="9f7b4-287">Skilgreina Dataverse-sýndartöflur</span><span class="sxs-lookup"><span data-stu-id="9f7b4-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="9f7b4-288">Algengar spurningar um sýndartöflur Human Resources</span><span class="sxs-lookup"><span data-stu-id="9f7b4-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="9f7b4-289">Hvað er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="9f7b4-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="9f7b4-290">Hugtakauppfærslur</span><span class="sxs-lookup"><span data-stu-id="9f7b4-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)
