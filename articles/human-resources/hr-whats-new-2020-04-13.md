---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources (13. apríl 2020)
description: Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 13. apríl 2020.
author: andreabichsel
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2a43b55c075102056ed7c752b72a85f2c9012d46
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051042"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a><span data-ttu-id="2efee-103">Hvað er nýtt eða breytt í Dynamics 365 Human Resources (13. apríl 2020)</span><span class="sxs-lookup"><span data-stu-id="2efee-103">What's new or changed in Dynamics 365 Human Resources (April 13, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2efee-104">Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2efee-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2efee-105">Breytingar eiga við um byggingarnúmer 8.1.3136.</span><span class="sxs-lookup"><span data-stu-id="2efee-105">Changes apply to build number 8.1.3136.</span></span> <span data-ttu-id="2efee-106">Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera LCS fyrir tilvísun.</span><span class="sxs-lookup"><span data-stu-id="2efee-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="new-production-release-cadence"></a><span data-ttu-id="2efee-107">Ný tíðni framleiðsluútgáfu</span><span class="sxs-lookup"><span data-stu-id="2efee-107">New production release cadence</span></span>

<span data-ttu-id="2efee-108">Með útgáfu þessarar viku breytist losunarferlið fyrir Human Resources úr vikulegri uppfærslu í hálfsmánaðar uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="2efee-108">With this week's release, the release cadence for Human Resources shifts from a weekly update to a biweekly update.</span></span> <span data-ttu-id="2efee-109">Til að tryggja samræmingu við örugga notkun á vettvangi og viðhalda háum stöðlum um stöðugleika og áreiðanleika í þjónustunni er ferlið við að dreifa þjónustuuppfærslum á öllum svæðum núna í hálfsmánaðar útgáfu.</span><span class="sxs-lookup"><span data-stu-id="2efee-109">To ensure alignment with safe deployment practices, and maintain high standards of stability and reliability in the service, the process of deploying service updates to all regions is now a two-week rollout.</span></span> <span data-ttu-id="2efee-110">Viðbótarprófanir og skjáir eru uppsettir til að staðfesta árangursríka dreifingu á hverju stigi ferlisins.</span><span class="sxs-lookup"><span data-stu-id="2efee-110">Additional testing and monitors are in place to verify successful deployment at each stage of the process.</span></span> <span data-ttu-id="2efee-111">Nánari upplýsingar um losunarrýmið, sjá [Uppfæra ferli](hr-admin-setup-update-process.md).</span><span class="sxs-lookup"><span data-stu-id="2efee-111">For more information on the release cadence, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a><span data-ttu-id="2efee-112">Ekki er hægt að breyta reitnum Sléttunarnákvæmni þegar gerð sléttunar hefur verið tilgreind (435616)</span><span class="sxs-lookup"><span data-stu-id="2efee-112">Rounding precision field isn't editable after specifying a Rounding type (435616)</span></span>

<span data-ttu-id="2efee-113">Með þessari breytingu er reiturinn **Sléttunarnákvæmni** nú tiltækur eftir að þú uppfærir reitinn **Gerð sléttunar**.</span><span class="sxs-lookup"><span data-stu-id="2efee-113">With this change, the **Rounding precision** field is now available after you update the **Rounding type** field.</span></span>

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a><span data-ttu-id="2efee-114">Ekki hægt að breyta lokadegi leyfisskráningar þegar leyfistímabilið er ekki með uppsöfnunartímabil (413628)</span><span class="sxs-lookup"><span data-stu-id="2efee-114">Can't edit leave enrollment end date when the leave plan doesn't have accrual periods (413628)</span></span>

<span data-ttu-id="2efee-115">Þú getur nú breytt lokadagsetningu skráningar án þess að fá villuna „Fylla verður út reitinn Grundvöllur uppsöfnunardags”.</span><span class="sxs-lookup"><span data-stu-id="2efee-115">You can now edit the enrollment end date without getting the error "Field Accrual date basis must be filled in."</span></span>

## <a name="employment-entity-doesnt-sync-to-dataverse-430834"></a><span data-ttu-id="2efee-116">Starfseiningin samstillist ekki við Dataverse (430834)</span><span class="sxs-lookup"><span data-stu-id="2efee-116">Employment entity doesn't sync to Dataverse (430834)</span></span>

<span data-ttu-id="2efee-117">Þessi breyting leiðréttir vandamál þar sem starfsgögn samstilltust ekki við Dataverse þegar fjárhagsvíddum hefur verið bætt við.</span><span class="sxs-lookup"><span data-stu-id="2efee-117">This change corrects an issue where the employment data wasn't syncing to Dataverse after adding financial dimensions.</span></span> 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a><span data-ttu-id="2efee-118">Fjarlægja fjölyfireiningar fyrir eininguna Tímabil vinnudagatals (431775)</span><span class="sxs-lookup"><span data-stu-id="2efee-118">Remove multi-parenting for Work Calendar Time Interval entity (431775)</span></span>

<span data-ttu-id="2efee-119">Þessi breyting fjarlægir fjölyfireiningar fyrir eininguna **Tímabil vinnudagatals**.</span><span class="sxs-lookup"><span data-stu-id="2efee-119">This change removes multi-parenting for the **Work Calendar Time Interval** entity.</span></span>

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a><span data-ttu-id="2efee-120">Sía með CAST aðgerð virkar ekki á OData kall einingar Stöðuúthlutun starfskrafts (431699)</span><span class="sxs-lookup"><span data-stu-id="2efee-120">Filter with CAST function doesn't work on OData call Position Worker Assignment entity (431699)</span></span>

<span data-ttu-id="2efee-121">Þessi uppfærsla felur í sér breytingu til að leyfa síu með CAST aðgerð innan OData fyrir eininguna **Stöðuúthlutun starfskrafts**.</span><span class="sxs-lookup"><span data-stu-id="2efee-121">This update includes a change to allow  filter with CAST function within OData for the **Position Worker Assignment** entity.</span></span>

## <a name="in-preview"></a><span data-ttu-id="2efee-122">Í kynningarútgáfu</span><span class="sxs-lookup"><span data-stu-id="2efee-122">In Preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="2efee-123">Frestun leyfis</span><span class="sxs-lookup"><span data-stu-id="2efee-123">Leave suspension</span></span>

<span data-ttu-id="2efee-124">Þú getur frestað leyfi og fjarvistum í Human Resources fyrir starfsmann.</span><span class="sxs-lookup"><span data-stu-id="2efee-124">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="2efee-125">Frestun leyfis stöðvar leyfisuppsöfnun fyrir valdar leyfisgerðir.</span><span class="sxs-lookup"><span data-stu-id="2efee-125">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="2efee-126">Ef frestunin á sér stað eftir að uppsöfnun hefur verið unnin skapar frestun leyfis hlutfallslega leiðréttingu á leyfisstöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="2efee-126">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="2efee-127">Frekari upplýsingar eru í [Fresta leyfi](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="2efee-127">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="2efee-128">Yfirfærslureglur</span><span class="sxs-lookup"><span data-stu-id="2efee-128">Carry forward rules</span></span>

<span data-ttu-id="2efee-129">Hægt er að tilgreina yfirfærsluorlofsgerð fyrir yfirfærslustöður þar sem yfirfærsluleiðréttingar eru fluttar.</span><span class="sxs-lookup"><span data-stu-id="2efee-129">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="2efee-130">Til dæmis, ef starfsmaður yfirfærir 10 daga getur þú valið aðra leyfisgerð fyrir þessa 10 daga.</span><span class="sxs-lookup"><span data-stu-id="2efee-130">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="2efee-131">Fyrir frekari upplýsingar, sjá [Grunnstilla gerðir leyfis og fjarvista](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="2efee-131">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="known-issues"></a><span data-ttu-id="2efee-132">Þekkt vandamál</span><span class="sxs-lookup"><span data-stu-id="2efee-132">Known issues</span></span>

## <a name="employment-details-entity"></a><span data-ttu-id="2efee-133">Atvinnuupplýsingaeining</span><span class="sxs-lookup"><span data-stu-id="2efee-133">Employment Details entity</span></span>

<span data-ttu-id="2efee-134">Einingin **Starfsupplýsingar** hefur verið uppfærð með eftirfarandi reitum:</span><span class="sxs-lookup"><span data-stu-id="2efee-134">The **Employment Detail** entity has been updated with the following fields:</span></span>

- <span data-ttu-id="2efee-135">**Greiðslutíðni**</span><span class="sxs-lookup"><span data-stu-id="2efee-135">**PayFrequency**</span></span>
- <span data-ttu-id="2efee-136">**Kenni starfsgreinar**</span><span class="sxs-lookup"><span data-stu-id="2efee-136">**Employment Category ID**</span></span>
- <span data-ttu-id="2efee-137">**Starfsheiti**</span><span class="sxs-lookup"><span data-stu-id="2efee-137">**Employment Type**</span></span>
- <span data-ttu-id="2efee-138">**Kenni starfsheitis**</span><span class="sxs-lookup"><span data-stu-id="2efee-138">**EmploymentType ID**</span></span>
- <span data-ttu-id="2efee-139">**Staða starfsfríðinda**</span><span class="sxs-lookup"><span data-stu-id="2efee-139">**Benefit Employment Status**</span></span>

<span data-ttu-id="2efee-140">Uppsetningargögnin fyrir þessa reiti treysta á að fríðindastjórnun sé virkjuð á vinnusvæðinu **Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="2efee-140">The setup data for these fields rely on benefits management being enabled in the **Feature management** workspace.</span></span> <span data-ttu-id="2efee-141">Þessa reitir ætti ekki að fylla út eða uppfæra í einingunni **Starfsupplýsingar** þar sem það mun valda villum við innflutning.</span><span class="sxs-lookup"><span data-stu-id="2efee-141">Don't populate or update these fields in the **Employment Detail** entity, because it will result in errors during import.</span></span>

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a><span data-ttu-id="2efee-142">SharePoint forsýning virkar ekki í sumum umhverfum</span><span class="sxs-lookup"><span data-stu-id="2efee-142">SharePoint preview doesn't work in some environments</span></span>

<span data-ttu-id="2efee-143">Ef forskoðun skjals fyrir skjöl sem eru vistuð í SharePoint virkar ekki, prófaðu eftirfarandi aðferð:</span><span class="sxs-lookup"><span data-stu-id="2efee-143">If document preview for documents stored in SharePoint doesn't work, try the following procedure:</span></span>

1. <span data-ttu-id="2efee-144">Staðfestu að notandareikningur stjórnanda sé með tölvupóst sem tengist notendaskránni.</span><span class="sxs-lookup"><span data-stu-id="2efee-144">Verify the Admin user account has an email associated with the user record.</span></span> <span data-ttu-id="2efee-145">Þessar upplýsingar er hægt að skoða á síðunni **Notandi**.</span><span class="sxs-lookup"><span data-stu-id="2efee-145">You can view this information in the **User** page.</span></span> <span data-ttu-id="2efee-146">Ef tölvupóstur er ekki settur upp þarftu að bæta við tölvupóstinum og veitunni með OData Excel viðbótinni.</span><span class="sxs-lookup"><span data-stu-id="2efee-146">If email isn't set up, you need to add the email and provider with the OData Excel add-in.</span></span> <span data-ttu-id="2efee-147">Sjálfgefið er að netfangið er ekki til í Excel-hönnuninni.</span><span class="sxs-lookup"><span data-stu-id="2efee-147">By default, the email address isn't present in the Excel design.</span></span> <span data-ttu-id="2efee-148">Þú þarft að breyta Excel hönnuninni, bæta við öllum reitum, beita og endurnýja.</span><span class="sxs-lookup"><span data-stu-id="2efee-148">You'll need to edit the Excel design, add all fields, apply, and refresh.</span></span> <span data-ttu-id="2efee-149">Þegar þú hefur lokið þessum skrefum geturðu uppfært stjórnandareikninginn.</span><span class="sxs-lookup"><span data-stu-id="2efee-149">Once you've completed those steps, you can update the admin account.</span></span>

2. <span data-ttu-id="2efee-150">Þegar stjórnandareikningurinn er með tilheyrandi tölvupóstreikning skaltu skrá þig inn á Human Resources með stjórnandaskilríkjum.</span><span class="sxs-lookup"><span data-stu-id="2efee-150">After the Admin account has an associated email account, sign in to Human Resources with Admin credentials.</span></span>

3. <span data-ttu-id="2efee-151">Opnaðu viðhengi í SharePoint til að hefja forskoðun skjalsins.</span><span class="sxs-lookup"><span data-stu-id="2efee-151">Access an attachment in SharePoint to start the document preview.</span></span>

4. <span data-ttu-id="2efee-152">Skráðu þig inn með öðrum notendareikningi sem hefur aðgang að viðhengjum og sannreyndu að forsýningin virkar eins og búist var við.</span><span class="sxs-lookup"><span data-stu-id="2efee-152">Sign in with another user account that has access to attachments and verify that the preview works as expected.</span></span>

## <a name="see-also"></a><span data-ttu-id="2efee-153">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="2efee-153">See also</span></span>

[<span data-ttu-id="2efee-154">Nýjungar í Human Resources</span><span class="sxs-lookup"><span data-stu-id="2efee-154">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="2efee-155">Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019</span><span class="sxs-lookup"><span data-stu-id="2efee-155">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="2efee-156">Uppfærsluferli</span><span class="sxs-lookup"><span data-stu-id="2efee-156">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="2efee-157">Vinna með eiginleika</span><span class="sxs-lookup"><span data-stu-id="2efee-157">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]