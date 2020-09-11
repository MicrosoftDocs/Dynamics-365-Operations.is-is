---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources (13. apríl 2020)
description: Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 13. apríl 2020.
author: Darinkramer
manager: AnnBe
ms.date: 4/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 729490e7516d8c7aef7232c9f5c227d3207dcd68
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712425"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a><span data-ttu-id="2c622-103">Hvað er nýtt eða breytt í Dynamics 365 Human Resources (13. apríl 2020)</span><span class="sxs-lookup"><span data-stu-id="2c622-103">What's new or changed in Dynamics 365 Human Resources (April 13, 2020)</span></span>

<span data-ttu-id="2c622-104">Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2c622-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2c622-105">Breytingar eiga við um byggingarnúmer 8.1.3136.</span><span class="sxs-lookup"><span data-stu-id="2c622-105">Changes apply to build number 8.1.3136.</span></span> <span data-ttu-id="2c622-106">Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera LCS fyrir tilvísun.</span><span class="sxs-lookup"><span data-stu-id="2c622-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="2c622-107">Ný tíðni framleiðsluútgáfu</span><span class="sxs-lookup"><span data-stu-id="2c622-107">New production release cadence</span></span>

<span data-ttu-id="2c622-108">Með útgáfu þessarar viku breytist losunarferlið fyrir Human Resources úr vikulegri uppfærslu í hálfsmánaðar uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="2c622-108">With this week's release, the release cadence for Human Resources shifts from a weekly update to a biweekly update.</span></span> <span data-ttu-id="2c622-109">Til að tryggja samræmingu við örugga notkun á vettvangi og viðhalda háum stöðlum um stöðugleika og áreiðanleika í þjónustunni er ferlið við að dreifa þjónustuuppfærslum á öllum svæðum núna í hálfsmánaðar útgáfu.</span><span class="sxs-lookup"><span data-stu-id="2c622-109">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions is now a two-week rollout.</span></span> <span data-ttu-id="2c622-110">Viðbótarprófanir og skjáir eru uppsettir til að staðfesta árangursríka dreifingu á hverju stigi ferlisins.</span><span class="sxs-lookup"><span data-stu-id="2c622-110">Additional testing and monitors are in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="2c622-111">Nánari upplýsingar um losunarrýmið, sjá [Uppfæra ferli](hr-admin-setup-update-process.md).</span><span class="sxs-lookup"><span data-stu-id="2c622-111">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a><span data-ttu-id="2c622-112">Ekki er hægt að breyta reitnum Sléttunarnákvæmni þegar gerð sléttunar hefur verið tilgreind (435616)</span><span class="sxs-lookup"><span data-stu-id="2c622-112">Rounding precision field isn't editable after specifying a Rounding type (435616)</span></span>

<span data-ttu-id="2c622-113">Með þessari breytingu er reiturinn **Sléttunarnákvæmni** nú tiltækur eftir að þú uppfærir reitinn **Gerð sléttunar**.</span><span class="sxs-lookup"><span data-stu-id="2c622-113">With this change, the **Rounding precision** field is now available after you update the **Rounding type** field.</span></span>

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a><span data-ttu-id="2c622-114">Ekki hægt að breyta lokadegi leyfisskráningar þegar leyfistímabilið er ekki með uppsöfnunartímabil (413628)</span><span class="sxs-lookup"><span data-stu-id="2c622-114">Can't edit leave enrollment end date when the leave plan doesn't have accrual periods (413628)</span></span>

<span data-ttu-id="2c622-115">Þú getur nú breytt lokadagsetningu skráningar án þess að fá villuna „Fylla verður út reitinn Grundvöllur uppsöfnunardags”.</span><span class="sxs-lookup"><span data-stu-id="2c622-115">You can now edit the enrollment end date without getting the error "Field Accrual date basis must be filled in."</span></span>

## <a name="employment-entity-doesnt-sync-to-common-data-service-430834"></a><span data-ttu-id="2c622-116">Starfseiningin samstillist ekki við Common Data Service (430834)</span><span class="sxs-lookup"><span data-stu-id="2c622-116">Employment entity doesn't sync to Common Data Service (430834)</span></span>

<span data-ttu-id="2c622-117">Þessi breyting leiðréttir vandamál þar sem starfsgögn samstilltust ekki við Common Data Service þegar fjárhagsvíddum hefur verið bætt við.</span><span class="sxs-lookup"><span data-stu-id="2c622-117">This change corrects an issue where the employment data wasn't syncing to Common Data Service after adding financial dimensions.</span></span> 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a><span data-ttu-id="2c622-118">Fjarlægja fjölyfireiningar fyrir eininguna Tímabil vinnudagatals (431775)</span><span class="sxs-lookup"><span data-stu-id="2c622-118">Remove multi-parenting for Work Calendar Time Interval entity (431775)</span></span>

<span data-ttu-id="2c622-119">Þessi breyting fjarlægir fjölyfireiningar fyrir eininguna **Tímabil vinnudagatals**.</span><span class="sxs-lookup"><span data-stu-id="2c622-119">This change removes multi-parenting for the **Work Calendar Time Interval** entity.</span></span>

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a><span data-ttu-id="2c622-120">Sía með CAST aðgerð virkar ekki á OData kall einingar Stöðuúthlutun starfskrafts (431699)</span><span class="sxs-lookup"><span data-stu-id="2c622-120">Filter with CAST function doesn't work on OData call Position Worker Assignment entity (431699)</span></span>

<span data-ttu-id="2c622-121">Þessi uppfærsla felur í sér breytingu til að leyfa síu með CAST aðgerð innan OData fyrir eininguna **Stöðuúthlutun starfskrafts**.</span><span class="sxs-lookup"><span data-stu-id="2c622-121">This update includes a change to allow  filter with CAST function within OData for the **Position Worker Assignment** entity.</span></span>

## <a name="in-preview"></a><span data-ttu-id="2c622-122">Í kynningarútgáfu</span><span class="sxs-lookup"><span data-stu-id="2c622-122">In Preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="2c622-123">Frestun leyfis</span><span class="sxs-lookup"><span data-stu-id="2c622-123">Leave suspension</span></span>

<span data-ttu-id="2c622-124">Þú getur frestað leyfi og fjarvistum í Human Resources fyrir starfsmann.</span><span class="sxs-lookup"><span data-stu-id="2c622-124">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="2c622-125">Frestun leyfis stöðvar leyfisuppsöfnun fyrir valdar leyfisgerðir.</span><span class="sxs-lookup"><span data-stu-id="2c622-125">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="2c622-126">Ef frestunin á sér stað eftir að uppsöfnun hefur verið unnin skapar frestun leyfis hlutfallslega leiðréttingu á leyfisstöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="2c622-126">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="2c622-127">Frekari upplýsingar eru í [Fresta leyfi](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="2c622-127">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="2c622-128">Yfirfærslureglur</span><span class="sxs-lookup"><span data-stu-id="2c622-128">Carry forward rules</span></span>

<span data-ttu-id="2c622-129">Hægt er að tilgreina yfirfærsluorlofsgerð fyrir yfirfærslustöður þar sem yfirfærsluleiðréttingar eru fluttar.</span><span class="sxs-lookup"><span data-stu-id="2c622-129">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="2c622-130">Til dæmis, ef starfsmaður yfirfærir 10 daga getur þú valið aðra leyfisgerð fyrir þessa 10 daga.</span><span class="sxs-lookup"><span data-stu-id="2c622-130">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="2c622-131">Fyrir frekari upplýsingar, sjá [Grunnstilla gerðir leyfis og fjarvista](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="2c622-131">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="2c622-132">Þekkt vandamál</span><span class="sxs-lookup"><span data-stu-id="2c622-132">Known issues</span></span>

## <a name="employment-details-entity"></a><span data-ttu-id="2c622-133">Atvinnuupplýsingaeining</span><span class="sxs-lookup"><span data-stu-id="2c622-133">Employment Details entity</span></span>

<span data-ttu-id="2c622-134">Einingin **Starfsupplýsingar** hefur verið uppfærð með eftirfarandi reitum:</span><span class="sxs-lookup"><span data-stu-id="2c622-134">The **Employment Detail** entity has been updated with the following fields:</span></span>

- <span data-ttu-id="2c622-135">**Greiðslutíðni**</span><span class="sxs-lookup"><span data-stu-id="2c622-135">**PayFrequency**</span></span>
- <span data-ttu-id="2c622-136">**Kenni starfsgreinar**</span><span class="sxs-lookup"><span data-stu-id="2c622-136">**Employment Category ID**</span></span>
- <span data-ttu-id="2c622-137">**Starfsheiti**</span><span class="sxs-lookup"><span data-stu-id="2c622-137">**Employment Type**</span></span>
- <span data-ttu-id="2c622-138">**Kenni starfsheitis**</span><span class="sxs-lookup"><span data-stu-id="2c622-138">**EmploymentType ID**</span></span>
- <span data-ttu-id="2c622-139">**Staða starfsfríðinda**</span><span class="sxs-lookup"><span data-stu-id="2c622-139">**Benefit Employment Status**</span></span>

<span data-ttu-id="2c622-140">Uppsetningargögnin fyrir þessa reiti treysta á að fríðindastjórnun sé virkjuð á vinnusvæðinu **Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="2c622-140">The setup data for these fields rely on benefits management being enabled in the **Feature management** workspace.</span></span> <span data-ttu-id="2c622-141">Þessa reitir ætti ekki að fylla út eða uppfæra í einingunni **Starfsupplýsingar** þar sem það mun valda villum við innflutning.</span><span class="sxs-lookup"><span data-stu-id="2c622-141">Don't populate or update these fields in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="2c622-142">SharePoint forsýning virkar ekki í sumum umhverfum</span><span class="sxs-lookup"><span data-stu-id="2c622-142">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="2c622-143">Ef forskoðun skjals fyrir skjöl sem eru vistuð í SharePoint virkar ekki, prófaðu eftirfarandi aðferð:</span><span class="sxs-lookup"><span data-stu-id="2c622-143">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="2c622-144">Staðfestu að notandareikningur stjórnanda sé með tölvupóst sem tengist notendaskránni.</span><span class="sxs-lookup"><span data-stu-id="2c622-144">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="2c622-145">Þessar upplýsingar er hægt að skoða á síðunni **Notandi**.</span><span class="sxs-lookup"><span data-stu-id="2c622-145">You can view this information in the **User** page.</span></span> <span data-ttu-id="2c622-146">Ef tölvupóstur er ekki settur upp þarftu að bæta við tölvupóstinum og veitunni með OData Excel viðbótinni.</span><span class="sxs-lookup"><span data-stu-id="2c622-146">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="2c622-147">Sjálfgefið er að netfangið er ekki til í Excel-hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="2c622-147">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="2c622-148">Þú þarft að breyta Excel hönnuninni, bæta við öllum reitum, beita og endurnýja.</span><span class="sxs-lookup"><span data-stu-id="2c622-148">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="2c622-149">Þegar þú hefur lokið þessum skrefum geturðu uppfært stjórnandareikninginn.</span><span class="sxs-lookup"><span data-stu-id="2c622-149">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="2c622-150">Þegar stjórnandareikningurinn er með tilheyrandi tölvupóstreikning skaltu skrá þig inn á Human Resources með stjórnandaskilríkjum.</span><span class="sxs-lookup"><span data-stu-id="2c622-150">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="2c622-151">Opnaðu viðhengi í SharePoint til að hefja forskoðun skjalsins.</span><span class="sxs-lookup"><span data-stu-id="2c622-151">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="2c622-152">Skráðu þig inn með öðrum notendareikningi sem hefur aðgang að viðhengjum og sannreyndu að forsýningin virkar eins og búist var við.</span><span class="sxs-lookup"><span data-stu-id="2c622-152">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="2c622-153">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2c622-153">See also</span></span>

[<span data-ttu-id="2c622-154">Nýjungar í Human Resources</span><span class="sxs-lookup"><span data-stu-id="2c622-154">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="2c622-155">Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019</span><span class="sxs-lookup"><span data-stu-id="2c622-155">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="2c622-156">Uppfærsluferli</span><span class="sxs-lookup"><span data-stu-id="2c622-156">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="2c622-157">Vinna með eiginleika</span><span class="sxs-lookup"><span data-stu-id="2c622-157">Manage features</span></span>](hr-admin-manage-features.md)