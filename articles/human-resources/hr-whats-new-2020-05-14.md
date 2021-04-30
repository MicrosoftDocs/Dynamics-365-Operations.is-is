---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources (14. maí 2020)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 14. maí 2020.
author: andreabichsel
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f8244d512c9e1236fc52cd4a91cdc78cc2b9b984
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893102"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a><span data-ttu-id="5670f-103">Hvað er nýtt eða breytt í Dynamics 365 Human Resources (14. maí 2020)</span><span class="sxs-lookup"><span data-stu-id="5670f-103">What's new or changed in Dynamics 365 Human Resources (May 14, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5670f-104">Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5670f-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="5670f-105">Breytingar eiga við um byggingarnúmer 8.1.3244.</span><span class="sxs-lookup"><span data-stu-id="5670f-105">Changes apply to build number 8.1.3244.</span></span> <span data-ttu-id="5670f-106">Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Lifecycle Services (LCS) vegna tilvísunar.</span><span class="sxs-lookup"><span data-stu-id="5670f-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="5670f-107">Verkvangsbreytingar</span><span class="sxs-lookup"><span data-stu-id="5670f-107">Platform changes</span></span>

<span data-ttu-id="5670f-108">Breytingar á verkvangi eru teknar með í útgáfu þessarar viku.</span><span class="sxs-lookup"><span data-stu-id="5670f-108">Platform changes are included in this week's release.</span></span> <span data-ttu-id="5670f-109">Frekari upplýsingar er að finna í [Verkvangsuppfærslur fyrir útgáfu 10.0.10 af Finance and Operations -forritum (maí 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34.md).</span><span class="sxs-lookup"><span data-stu-id="5670f-109">For more information, see [Platform updates for version 10.0.10 of Finance and Operations apps (May 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34.md).</span></span> <span data-ttu-id="5670f-110">Þessi útgáfa inniheldur villuleiðréttingar og breytingar á vistuðum yfirlitum.</span><span class="sxs-lookup"><span data-stu-id="5670f-110">This release includes bug fixes and changes to saved views.</span></span>
 
## <a name="ensure-dataverse-picklists-are-consistent-with-leave-enums-436343"></a><span data-ttu-id="5670f-111">Tryggið að tínslulistar Dataverse séu í samræmi við fasttexta leyfa (436343)</span><span class="sxs-lookup"><span data-stu-id="5670f-111">Ensure Dataverse picklists are consistent with Leave enums (436343)</span></span>

<span data-ttu-id="5670f-112">Tínslulistar Dataverse eru nú í samræmi við fasttexta leyfa.</span><span class="sxs-lookup"><span data-stu-id="5670f-112">Dataverse picklists are now consistent with Leave enums.</span></span>

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a><span data-ttu-id="5670f-113">Leyfa notendum að grunnstilla verkflæði leyfisbeiðna út frá umbeðnu magni (300044)</span><span class="sxs-lookup"><span data-stu-id="5670f-113">Allow users to configure leave request workflow based on the request amount (300044)</span></span>

<span data-ttu-id="5670f-114">Notendur geta skilgreint verkflæði leyfisbeiðna út frá umbeðnu magni.</span><span class="sxs-lookup"><span data-stu-id="5670f-114">Users can configure leave requests workflows based on request amounts.</span></span>
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a><span data-ttu-id="5670f-115">Nýtt eyðublað starfskrafts birtir gögn í gegnum Skoðunarvalmynd þegar Ítarlegar öryggisstillingar eru virkar (403185)</span><span class="sxs-lookup"><span data-stu-id="5670f-115">New worker form exposes data through the View menu when advanced security is enabled (403185)</span></span>

<span data-ttu-id="5670f-116">Þessi útgáfa leiðréttir hvernig skoðun starfsmanna milli lögaðila virkar þegar ítarlegur aðgangur er virkur og starfsmenn í öðrum fyrirtækjum eru aðgengilegir.</span><span class="sxs-lookup"><span data-stu-id="5670f-116">This release corrects how viewing workers across legal entities functions when advanced access is enabled and workers in other companies are accessible.</span></span>

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a><span data-ttu-id="5670f-117">Leyfa keyrslu uppsafnaðra leyfa fyrir eina áætlun eða eitt fyrirtæki (318844)</span><span class="sxs-lookup"><span data-stu-id="5670f-117">Allow running leave accruals for a single plan or a single company (318844)</span></span>

<span data-ttu-id="5670f-118">Með þessari breytingu er hægt að keyra uppsöfnun fyrir fyrirtæki eða áætlun.</span><span class="sxs-lookup"><span data-stu-id="5670f-118">With this change, you can run accruals for a company or a plan.</span></span>
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a><span data-ttu-id="5670f-119">Sýna jafngildi stöðunnar í fullu starfi (FTE) á skjámyndinni „skráðir starfsmenn“ (414658)</span><span class="sxs-lookup"><span data-stu-id="5670f-119">Show the position's full-time equivalent (FTE) in the Enrolled workers form (414658)</span></span>

<span data-ttu-id="5670f-120">FTE-gildi fyrir stöðu starfsmanns ákvarðar uppsöfnun réttinda starfsmanns þegar valkosturinn FTE er virkur í leyfisgerðinni.</span><span class="sxs-lookup"><span data-stu-id="5670f-120">The FTE value from a worker's position determines a worker's accrual rate when the FTE option is enabled on the leave type.</span></span> <span data-ttu-id="5670f-121">Þessi reitur er nú hafður með í skjámyndinni **„Skráðir starfsmenn“** og svarglugganum **„Fjöldaskráning“**.</span><span class="sxs-lookup"><span data-stu-id="5670f-121">This field is now included in **Enrolled workers** form and the **Mass enrollment** dialog.</span></span>

## <a name="add-leave-balance-expiration-batch-job-431266"></a><span data-ttu-id="5670f-122">Bæta við lokarunuvinnslu leyfisstöðu (431266)</span><span class="sxs-lookup"><span data-stu-id="5670f-122">Add leave balance expiration batch job (431266)</span></span>

<span data-ttu-id="5670f-123">Ný runuvinnsla er nú tiltæk sem keyrir daglega.</span><span class="sxs-lookup"><span data-stu-id="5670f-123">A new batch job is now available that runs daily.</span></span> <span data-ttu-id="5670f-124">Það styttir eftirstandandi leyfisstöðu þegar lokadagsetningar verða gildandi.</span><span class="sxs-lookup"><span data-stu-id="5670f-124">It decreases the remaining leave balance when expiration dates become current.</span></span>

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a><span data-ttu-id="5670f-125">Við útflutning persónulegs tengiliðs fyrir starfsmann með einingunni Persónulegur tengiliður starfsmanns eru persónulegir tengiliðir af venslagerðinni Yfireining ekki fluttir út (345893)</span><span class="sxs-lookup"><span data-stu-id="5670f-125">Exporting personal contacts for an employee using the Worker personal contact person entity doesn't export personal contacts with the Parent relationship type (345893)</span></span>

<span data-ttu-id="5670f-126">Gagnaeiningin **Persónulegur tengiliður starfsmanns** (**HcmPersonalContactPersonEntity** í DMF og **PersonalContactPerson** í OData) gat ekki flutt út persónulega tengiliði sem er með venslagerðina **Yfireining**.</span><span class="sxs-lookup"><span data-stu-id="5670f-126">The **Worker personal contact person** data entity (**HcmPersonalContactPersonEntity** in DMF and **PersonalContactPerson** in OData) couldn't export personal contacts that have a relationship type of **Parent**.</span></span> <span data-ttu-id="5670f-127">Þetta atriði er fast fyrir persónulega tengiliði sem stofnaðir eru eftir þessa breytingu.</span><span class="sxs-lookup"><span data-stu-id="5670f-127">This issue is fixed for personal contacts that are created after this change.</span></span> <span data-ttu-id="5670f-128">Fyrirliggjandi persónulegir tengiliðir af gerðinni **Yfireining** verða fastir í nýrri útgáfu.</span><span class="sxs-lookup"><span data-stu-id="5670f-128">Existing personal contacts of type **Parent** will be fixed in a later release.</span></span>

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a><span data-ttu-id="5670f-129">Ástæðukóðar birtast í mismunandi aðstæðum þegar þeir eru merktir sem „leyfi og fjarvistir“ og einfölduð skjámynd starfsmanns er virk (434163)</span><span class="sxs-lookup"><span data-stu-id="5670f-129">Reason codes display across different scenarios when they're marked as Leave and absence and the streamlined employee form is enabled (434163)</span></span>

<span data-ttu-id="5670f-130">Þessi breyting takmarkar ástæðukóðana við leyfis-og fjarvistakóða þegar einfaldaður innsláttur starfsmanns er virkur.</span><span class="sxs-lookup"><span data-stu-id="5670f-130">This change restricts the reason codes to only Leave and absence codes when you enable streamlined employee entry.</span></span>

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a><span data-ttu-id="5670f-131">Forskoðunareiginleikinn „Úthluta leyfisáætlun til starfsmanna í framtíðinni“ sýnir villu (433555)</span><span class="sxs-lookup"><span data-stu-id="5670f-131">The preview feature Assign a leave plan to employees in the future displays error (433555)</span></span>

<span data-ttu-id="5670f-132">Þessi breyting leiðréttir villu þegar tveimur leyfisgerðum hefur verið úthlutað á leyfisáætlun og reynt er að úthluta starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="5670f-132">This change corrects an error when a leave plan has two leave types assigned and you attempt to assign an employee.</span></span>

## <a name="getting-started-banner-appears-for-all-users-441731"></a><span data-ttu-id="5670f-133">Borðarnir „Hafist handa“ birtast fyrir alla notendur (441731)</span><span class="sxs-lookup"><span data-stu-id="5670f-133">Getting started banner appears for all users (441731)</span></span>

<span data-ttu-id="5670f-134">Með þessari breytingu er borðinn „Hafist handa“ falinn fyrir notendum sem eru ekki kerfisstjórar eða stjórnendur gagnastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="5670f-134">With this change, the Getting started banner is hidden for users that aren't System administrators or Data management administrators.</span></span> 

## <a name="the-dataverse-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a><span data-ttu-id="5670f-135">Einingin Dataverse póstfang starfsmanns vinnur á annan hátt að því er varðar dagsetningar gildisdagsetninga í Mannauði (425071)</span><span class="sxs-lookup"><span data-stu-id="5670f-135">The Dataverse Worker Address entity works differently in terms of date time effective dates in Human Resources (425071)</span></span>

<span data-ttu-id="5670f-136">Þessi breyting heldur upplýsingum um aðsetur jöfnuðum í vissum aðstæðum, með hliðsjón af dagsetningum aðseturs.</span><span class="sxs-lookup"><span data-stu-id="5670f-136">This change keeps address information aligned in certain scenarios, based on the dates of the address.</span></span>

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a><span data-ttu-id="5670f-137">Ekki er hægt að bæta viðhengi við samþykkta beiðni um leyfi (425407)</span><span class="sxs-lookup"><span data-stu-id="5670f-137">Unable to add an attachment to an approved leave request (425407)</span></span>

<span data-ttu-id="5670f-138">Í útgáfu þessarar viku er hægt að bæta viðhengjum við samþykktar beiðnir um leyfi án þess að breyta leyfisbeiðninni.</span><span class="sxs-lookup"><span data-stu-id="5670f-138">With this week's release, you can add attachments to approved leave requests without changing the leave request.</span></span>

## <a name="in-preview"></a><span data-ttu-id="5670f-139">Í kynningarútgáfu</span><span class="sxs-lookup"><span data-stu-id="5670f-139">In preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="5670f-140">Frestun leyfis</span><span class="sxs-lookup"><span data-stu-id="5670f-140">Leave suspension</span></span>

<span data-ttu-id="5670f-141">Þú getur frestað leyfi og fjarvistum í Human Resources fyrir starfsmann.</span><span class="sxs-lookup"><span data-stu-id="5670f-141">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="5670f-142">Frestun leyfis stöðvar leyfisuppsöfnun fyrir valdar leyfisgerðir.</span><span class="sxs-lookup"><span data-stu-id="5670f-142">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="5670f-143">Ef frestunin á sér stað eftir að uppsöfnun hefur verið unnin skapar frestun leyfis hlutfallslega leiðréttingu á leyfisstöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="5670f-143">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="5670f-144">Frekari upplýsingar eru í [Fresta leyfi](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="5670f-144">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="5670f-145">Uppfæra notendaupplifun til að sýna að uppsöfnun sé frestað (429550)</span><span class="sxs-lookup"><span data-stu-id="5670f-145">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="5670f-146">Notandaupplifunin sýnir nú að uppsöfnun hafi verið frestað fyrir áætlun.</span><span class="sxs-lookup"><span data-stu-id="5670f-146">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a><span data-ttu-id="5670f-147">Uppsafnað leyfi í bið fyrir tilteknar leyfisgerðir (272447)</span><span class="sxs-lookup"><span data-stu-id="5670f-147">Suspend leave accrual for specified leave types (272447)</span></span>

<span data-ttu-id="5670f-148">Í þessari útgáfu getur mannauður búið til reglu til að fresta uppsöfnun leyfis fyrir starfsmenn með beiðnum um leyfi sem færðar eru inn fyrir ógreitt leyfi.</span><span class="sxs-lookup"><span data-stu-id="5670f-148">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="5670f-149">Ógreit leyfi getur verið gerð, en þarf ekki að vera það.</span><span class="sxs-lookup"><span data-stu-id="5670f-149">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="5670f-150">Hægt er að fresta öllu leyfi út frá gerð annarrar leyfisgerðar.</span><span class="sxs-lookup"><span data-stu-id="5670f-150">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a><span data-ttu-id="5670f-151">DMF-eining er í boði fyrir frestun uppsöfnunar (429549)</span><span class="sxs-lookup"><span data-stu-id="5670f-151">DMF entity available for accrual suspensions (429549)</span></span>

<span data-ttu-id="5670f-152">DMF-eining er ekki til staðar fyrir uppsöfnun í bið.</span><span class="sxs-lookup"><span data-stu-id="5670f-152">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-429547"></a><span data-ttu-id="5670f-153">Bæta ástæðukóða við frestun uppsöfnunar (429547)</span><span class="sxs-lookup"><span data-stu-id="5670f-153">Add reason code to accrual suspensions (429547)</span></span>

<span data-ttu-id="5670f-154">Ástæðukóðum hefur verið bætt við uppsöfnun í bið.</span><span class="sxs-lookup"><span data-stu-id="5670f-154">Reason codes have been added to the accrual suspension.</span></span>

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a><span data-ttu-id="5670f-155">Hefja flutning úr færibreytum Human Resources í færibreytur leyfis og fjarvista</span><span class="sxs-lookup"><span data-stu-id="5670f-155">Begin transitioning from Human Resources parameters to leave and absence parameters</span></span>

<span data-ttu-id="5670f-156">Þessi útgáfa byrjar á að sameina færibreytur mannauðsstjórnunar með færibreytum leyfis og fjarvista.</span><span class="sxs-lookup"><span data-stu-id="5670f-156">This release starts to combine Human Resources parameters with Leave and absence parameters.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="5670f-157">Yfirfærslureglur</span><span class="sxs-lookup"><span data-stu-id="5670f-157">Carry forward rules</span></span>

<span data-ttu-id="5670f-158">Hægt er að tilgreina yfirfærsluorlofsgerð fyrir yfirfærslustöður þar sem yfirfærsluleiðréttingar eru fluttar.</span><span class="sxs-lookup"><span data-stu-id="5670f-158">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="5670f-159">Til dæmis, ef starfsmaður yfirfærir 10 daga getur þú valið aðra leyfisgerð fyrir þessa 10 daga.</span><span class="sxs-lookup"><span data-stu-id="5670f-159">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="5670f-160">Fyrir frekari upplýsingar, sjá [Grunnstilla gerðir leyfis og fjarvista](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="5670f-160">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="5670f-161">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="5670f-161">See also</span></span>

[<span data-ttu-id="5670f-162">Nýjungar í Human Resources</span><span class="sxs-lookup"><span data-stu-id="5670f-162">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="5670f-163">Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019</span><span class="sxs-lookup"><span data-stu-id="5670f-163">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="5670f-164">Uppfærsluferli</span><span class="sxs-lookup"><span data-stu-id="5670f-164">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="5670f-165">Vinna með eiginleika</span><span class="sxs-lookup"><span data-stu-id="5670f-165">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]