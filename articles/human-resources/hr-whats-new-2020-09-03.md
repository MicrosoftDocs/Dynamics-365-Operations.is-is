---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources (03. september 2020)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 3. september 2020.
author: andreabichsel
ms.date: 09/03/2020
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
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 10978d8843e7bce2800d62b63e58152569be9631
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891770"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a><span data-ttu-id="bccfa-103">Nýjungar eða breytingar í Dynamics 365 Human Resources (3. september 2020)</span><span class="sxs-lookup"><span data-stu-id="bccfa-103">What's new or changed in Dynamics 365 Human Resources (September 3, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="bccfa-104">Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bccfa-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="bccfa-105">Breytingar eiga við um byggingarnúmer 8.1.3504.</span><span class="sxs-lookup"><span data-stu-id="bccfa-105">Changes apply to build number 8.1.3504.</span></span> <span data-ttu-id="bccfa-106">Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera í Lifecycle Services (LCS) vegna tilvísunar.</span><span class="sxs-lookup"><span data-stu-id="bccfa-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

<span data-ttu-id="bccfa-107">Frekari upplýsingar um væntanlegu eiginleikana í Human Resources er að finna í [Yfirlit yfir Dynamics 365 Human Resources 2019 útgáfutímabil 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).</span><span class="sxs-lookup"><span data-stu-id="bccfa-107">For more information about upcoming features in Human Resources, see [Overview of Dynamics 365 Human Resources 2019 release wave 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).</span></span> <span data-ttu-id="bccfa-108">Nánari upplýsingar um uppfærsluferlið fyrir Human Resources er að finna í [Uppfærsluferli](hr-admin-setup-update-process.md).</span><span class="sxs-lookup"><span data-stu-id="bccfa-108">For more information about the update process for Human Resources, see [Update process](hr-admin-setup-update-process.md).</span></span>

## <a name="in-this-release"></a><span data-ttu-id="bccfa-109">Í þessari útgáfu</span><span class="sxs-lookup"><span data-stu-id="bccfa-109">In this release</span></span>

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a><span data-ttu-id="bccfa-110">Ný sjálfgefin hnitanet fjárhagsvídda og svarmynstur í Human Resources (469495)</span><span class="sxs-lookup"><span data-stu-id="bccfa-110">New default financial dimensions grid and dialog pattern throughout Human Resources (469495)</span></span>

<span data-ttu-id="bccfa-111">Nýja mynstrið fyrir fjárhagsvíddir er nú aðgengilegt á eftirtöldum svæðum:</span><span class="sxs-lookup"><span data-stu-id="bccfa-111">The new pattern for financial dimensions is now available in the following areas:</span></span>

- <span data-ttu-id="bccfa-112">Stöðuaðgerðir (Snið: **HcmPositionActionDetail**)</span><span class="sxs-lookup"><span data-stu-id="bccfa-112">Position actions  (Form: **HcmPositionActionDetail**)</span></span>
- <span data-ttu-id="bccfa-113">Tekjukóðar launa (Snið: **PayrollEarningCode**)</span><span class="sxs-lookup"><span data-stu-id="bccfa-113">Payroll earning codes  (Form: **PayrollEarningCode**)</span></span>

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a><span data-ttu-id="bccfa-114">Færslur birtast ekki í frídagatali fyrirtækis ef ekki er kveikt á Viðbætur dagatals yfir leyfi og fjarvistir (484406)</span><span class="sxs-lookup"><span data-stu-id="bccfa-114">Entries don't appear in company leave calendar if Leave and absence calendar enhancements aren't enabled (484406)</span></span>

<span data-ttu-id="bccfa-115">Þessi útgáfa leiðréttir vandamál þar sem frífærslur eru ekki birtar í frídagatali fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="bccfa-115">This release corrects an issue where leave entries aren't displayed in the company leave calendar.</span></span> <span data-ttu-id="bccfa-116">Þetta vandamál kemur aðeins upp þegar valkostur Eiginleikastjórnunar **Viðbætur dagatals yfir leyfi og fjarvistir** er ekki virkur.</span><span class="sxs-lookup"><span data-stu-id="bccfa-116">This issue only occurs when the Feature management option **Leave and absence calendar enhancements** isn't enabled.</span></span>

### <a name="benefitplanemployeeentity-issue-467597"></a><span data-ttu-id="bccfa-117">BenefitPlanEmployeeEntity vandamál (467597)</span><span class="sxs-lookup"><span data-stu-id="bccfa-117">BenefitPlanEmployeeEntity issue (467597)</span></span>

<span data-ttu-id="bccfa-118">Þessi útgáfa leiðréttir vandamál með **BenefitsPlanEmployee** eininguna.</span><span class="sxs-lookup"><span data-stu-id="bccfa-118">This release corrects an issue with the **BenefitsPlanEmployee** entity.</span></span> <span data-ttu-id="bccfa-119">Þegar verið er að flytja inn innskráningar starfsmanns eru **Tryggingarkóði** og **Kóði áætlunargerðar** nú rangt stilltir.</span><span class="sxs-lookup"><span data-stu-id="bccfa-119">When importing worker enrollments, the **Coverage code** and the **Plan type code** are now set correctly.</span></span> <span data-ttu-id="bccfa-120">Þetta vandamál veldur því að fríðindaáætlanir starfsmanna birtast á rangan hátt í **Fríðindaáætlun starfsmanns** og í **Opnar innskráningar** skjámyndum í sjálfsafgreiðslu starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="bccfa-120">This issue caused employee benefit plans to display incorrectly in the **Worker benefits plan** and **Open enrollment** forms in Employee self service.</span></span>

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a><span data-ttu-id="bccfa-121">Rafræn skrá 1094-C úttakstaf vantar í XML (435190)</span><span class="sxs-lookup"><span data-stu-id="bccfa-121">Electronic file 1094-C output missing letter in XML (435190)</span></span>

<span data-ttu-id="bccfa-122">Þessi breyting leiðréttir vandamál með 1094-C úttaksskrána þar sem staf vantar þegar verið er að senda inn til IRS.</span><span class="sxs-lookup"><span data-stu-id="bccfa-122">This change corrects an issue with the 1094-C output file missing a character needed when submitting to the IRS.</span></span>

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a><span data-ttu-id="bccfa-123">Tafla breytilegra launa starfsmanns varpað á eyðublað fastra launa (476117)</span><span class="sxs-lookup"><span data-stu-id="bccfa-123">Employee variable compensation table mapped to fixed compensation form (476117)</span></span>

<span data-ttu-id="bccfa-124">Þessi breyting samstillir reiti fastra launa við föst laun.</span><span class="sxs-lookup"><span data-stu-id="bccfa-124">This change aligns the fixed compensation fields with the fixed compensation form.</span></span> <span data-ttu-id="bccfa-125">Reitir breytilegra launa eru nú aðeins í boði í skjámyndinni breytileg laun.</span><span class="sxs-lookup"><span data-stu-id="bccfa-125">Variable compensation fields are now only available with the variable compensation form.</span></span>

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a><span data-ttu-id="bccfa-126">Leyfisbeiðnir leyfðar fyrir skráningu ef gerð leyfis er með neikvæða lágmarksstöðu (469917)</span><span class="sxs-lookup"><span data-stu-id="bccfa-126">Leave requests allowed before enrollment if that leave type has a negative minimum balance (469917)</span></span>

<span data-ttu-id="bccfa-127">Þessi breyting bannar innslátt leyfisbeiðna fyrir skráningu í áætlunina, jafnvel þótt skráning sé með neikvæða lágmarksstöðu.</span><span class="sxs-lookup"><span data-stu-id="bccfa-127">This change prohibits entering leave requests before being enrolled in the plan, even if the enrollment has a negative minimum balance.</span></span> <span data-ttu-id="bccfa-128">Aðeins er hægt að færa inn eða senda beiðnir þegar áætlunin er virk.</span><span class="sxs-lookup"><span data-stu-id="bccfa-128">You can only enter or submit requests when the plan is active.</span></span>

### <a name="document-templates-dont-download-457279"></a><span data-ttu-id="bccfa-129">Skjalasniðmát sækja ekki (457279)</span><span class="sxs-lookup"><span data-stu-id="bccfa-129">Document templates don't download (457279)</span></span>

<span data-ttu-id="bccfa-130">Með þessari breytingu er nú hægt að sækja öll skjalasniðmát.</span><span class="sxs-lookup"><span data-stu-id="bccfa-130">With this change, you can now download all document templates.</span></span> 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a><span data-ttu-id="bccfa-131">Gögn birt sem dálkhausar í stað lína fyrir reitinn Launataxti í skýrslu launafyrirkomulags (476077)</span><span class="sxs-lookup"><span data-stu-id="bccfa-131">Data displays as column headers instead of rows for the Pay rate field in the compensation plan report (476077)</span></span>

<span data-ttu-id="bccfa-132">Greiningarskýrslan birtir nú réttar upplýsingar fyrir **Launataxta**.</span><span class="sxs-lookup"><span data-stu-id="bccfa-132">The analytics report now displays the correct information for **Pay rate**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="bccfa-133">Í kynningarútgáfu</span><span class="sxs-lookup"><span data-stu-id="bccfa-133">In preview</span></span>

### <a name="human-resources-application-in-teams"></a><span data-ttu-id="bccfa-134">Forrit „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="bccfa-134">Human Resources application in Teams</span></span>

<span data-ttu-id="bccfa-135">Starfsmenn geta skoðað og beðið um tíma frá vinnu innan Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="bccfa-135">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="bccfa-136">Hægt er að hafa umsjón með þjark til að búa til beiðnir um leyfi.</span><span class="sxs-lookup"><span data-stu-id="bccfa-136">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="bccfa-137">Frekari upplýsingar má finna á</span><span class="sxs-lookup"><span data-stu-id="bccfa-137">For more information, see:</span></span>

- <span data-ttu-id="bccfa-138">[Umhverfi starfsmannaleyfis og -fjarvista í Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) í Dynamics 365 2020 útgáfutímabilsáætlun 1</span><span class="sxs-lookup"><span data-stu-id="bccfa-138">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="bccfa-139">[Forritið „Human Resources“ í Teams](./hr-admin-teams-leave-app.md) í Human Resources fylgiskjölum</span><span class="sxs-lookup"><span data-stu-id="bccfa-139">[Human Resources app in Teams](./hr-admin-teams-leave-app.md) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="bccfa-140">Forritið Human Resources í forskoðunareiginleikum Teams</span><span class="sxs-lookup"><span data-stu-id="bccfa-140">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="bccfa-141">**Tilkynningar**: Sendendur og samþykktaraðilar frítímabeiðni verða látnir vita í forriti Human Resources í Teams.</span><span class="sxs-lookup"><span data-stu-id="bccfa-141">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="bccfa-142">Samþykktaraðilar geta samþykkt eða hafnað beiðnum um frí.</span><span class="sxs-lookup"><span data-stu-id="bccfa-142">Approvers will be able to approve or deny time-off requests.</span></span> <span data-ttu-id="bccfa-143">Sendendur verða látnir vita hvort beiðnin hafi verið samþykkt eða henni hafnað.</span><span class="sxs-lookup"><span data-stu-id="bccfa-143">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="bccfa-144">Frekari upplýsingar má finna á</span><span class="sxs-lookup"><span data-stu-id="bccfa-144">For more information, see:</span></span>
   - <span data-ttu-id="bccfa-145">[Umhverfi starfsmannaleyfis og -fjarvista í Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) í Dynamics 365 2020 útgáfutímabilsáætlun 2</span><span class="sxs-lookup"><span data-stu-id="bccfa-145">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="bccfa-146">[Virkja tilkynningar fyrir forritið Human Resources í Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) í Human Resources fylgiskjölum</span><span class="sxs-lookup"><span data-stu-id="bccfa-146">[Enable notifications for the Human Resources app in Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="bccfa-147">[Kveikja eða slökkva á Teams tilkynningum fyrir einstaka notendur](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) í Human Resources fylgiskjölum</span><span class="sxs-lookup"><span data-stu-id="bccfa-147">[Turn Teams notifications on or off for individual users](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="bccfa-148">[Teams-tilkynningarnar](./hr-teams-leave-app.md#respond-to-teams-notifications) í Human Resources fylgiskjölum</span><span class="sxs-lookup"><span data-stu-id="bccfa-148">[Teams notifications](./hr-teams-leave-app.md#respond-to-teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="bccfa-149">[Skoða frídagdagatal teymisins](./hr-teams-leave-app.md#view-your-teams-leave-calendar) í fylgiskjölum Human Resources</span><span class="sxs-lookup"><span data-stu-id="bccfa-149">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="bccfa-150">**Frítímadagatal stjórndanda**: Stjórnendur geta séð samþykkt frí og frí sem bíður ákvörðunar fyrir beina undirmenn í dagatalsyfirliti.</span><span class="sxs-lookup"><span data-stu-id="bccfa-150">**Manager time-off calendar**: Managers will be able to see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="bccfa-151">Þetta yfirlit veitir auðveldan skilning á því hvenær teymismeðlimir þeirra eru fjarri vinnu.</span><span class="sxs-lookup"><span data-stu-id="bccfa-151">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="bccfa-152">Frekari upplýsingar má finna á</span><span class="sxs-lookup"><span data-stu-id="bccfa-152">For more information, see:</span></span>
   - <span data-ttu-id="bccfa-153">[Umhverfi starfsmannaleyfis og -fjarvista í Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) í Dynamics 365 2020 útgáfutímabilsáætlun 2</span><span class="sxs-lookup"><span data-stu-id="bccfa-153">[Employee leave and absence experience in Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="bccfa-154">[Skoða frídagdagatal teymisins](./hr-teams-leave-app.md#view-your-teams-leave-calendar) í fylgiskjölum Human Resources</span><span class="sxs-lookup"><span data-stu-id="bccfa-154">[View your team's leave calendar](./hr-teams-leave-app.md#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="bccfa-155">Skilgreiningarvalkostur fyrir stöðu vinnuliða sem úthlutað er á mig (477004)</span><span class="sxs-lookup"><span data-stu-id="bccfa-155">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="bccfa-156">Nýr valkostur er nú tiltækur til að staðsetja **Vinnuliðum sem úthlutað er á mig** lista í hægri dálknum á stjórnborðinu.</span><span class="sxs-lookup"><span data-stu-id="bccfa-156">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="bccfa-157">Með þessari breytingu eru allir vinnuliðir og verkefnalistar birtir á sama svæði.</span><span class="sxs-lookup"><span data-stu-id="bccfa-157">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="bccfa-158">Virkjaðu þessa virkni með því að kveikja á **(Forskoðun) Endurbætur á upplifun verkflæðis** í eiginleikastjórnun.</span><span class="sxs-lookup"><span data-stu-id="bccfa-158">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="bccfa-159">Frekari upplýsingar um að kveikja á forútgáfueiginleikum er að finna í [Vinna með eiginleika](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="bccfa-159">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="bccfa-160">Þessi eiginleiki er einnig fyrir verkflæðisvalkosti sem birtast í skjámyndunum starfsmannaaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="bccfa-160">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="bccfa-161">Verkflæðisvalkostur birtist einnig fyrir ofan flýtiflipa aðgerðarinnar fyrir flýtiaðgang.</span><span class="sxs-lookup"><span data-stu-id="bccfa-161">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="bccfa-162">Frekari upplýsingar má finna á</span><span class="sxs-lookup"><span data-stu-id="bccfa-162">For more information, see:</span></span> 

- <span data-ttu-id="bccfa-163">[Endurbætur á upplifun verkflæðis fyrir fyrirtæki og starfsfólk](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) í Dynamics 365 2020 útgáfutímabilsáætlun 2</span><span class="sxs-lookup"><span data-stu-id="bccfa-163">[Organization and personnel management workflow experience enhancements](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![Vinnuliðir sem úthlutað er á mig](./media/hr-workflow-work-items-assigned-to-me.png)

![Flýtiaðgangur að verkflæðisatriðum](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a><span data-ttu-id="bccfa-166">Væntanlegt</span><span class="sxs-lookup"><span data-stu-id="bccfa-166">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="bccfa-167">Einingar gátlista innifaldar í Dataverse</span><span class="sxs-lookup"><span data-stu-id="bccfa-167">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="bccfa-168">Gátlistaeiningar fyrir Ráðstafanir vegna nýrra starfsmanna, Ráðstafanir vegna starfsloka og viðskiptaferla verða bráðum tiltækar í Dataverse.</span><span class="sxs-lookup"><span data-stu-id="bccfa-168">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="bccfa-169">Ástæðukóðar fyrir fríðindastjórnun</span><span class="sxs-lookup"><span data-stu-id="bccfa-169">Benefits management reason codes</span></span>

<span data-ttu-id="bccfa-170">Ástæðukóðar fyrir fríðindastjórnun verða brátt sameinaðir við tiltæka ástæðukóða í Human Resources.</span><span class="sxs-lookup"><span data-stu-id="bccfa-170">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="bccfa-171">Ef ástæðukóðar voru stofnaðir í Fríðindastjórnun sem eru yfir 15 stafir að lengd þarf að breyta heiti ástæðukóðans í Fríðindastjórnun **Ástæðukóðar** skjámyndinni þannig að þeir eru 15 stafir eða minna.</span><span class="sxs-lookup"><span data-stu-id="bccfa-171">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="bccfa-172">Þegar búið er að uppfæra heitið mun ástæðukóðinn birtast undir fyrirliggjandi skjámynd ástæðukóða í starfsmannastjórnun.</span><span class="sxs-lookup"><span data-stu-id="bccfa-172">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="bccfa-173">Þessi breyting verður tiltæk í framtíðinni og mun ekki hafa áhrif á fyrirliggjandi virkni.</span><span class="sxs-lookup"><span data-stu-id="bccfa-173">This change will be available in the future and won't affect existing functionally.</span></span>

## <a name="see-also"></a><span data-ttu-id="bccfa-174">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="bccfa-174">See also</span></span>

[<span data-ttu-id="bccfa-175">Nýjungar eða breytingar í Mannauði</span><span class="sxs-lookup"><span data-stu-id="bccfa-175">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="bccfa-176">Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019</span><span class="sxs-lookup"><span data-stu-id="bccfa-176">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="bccfa-177">Uppfærsluferli</span><span class="sxs-lookup"><span data-stu-id="bccfa-177">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="bccfa-178">Vinna með eiginleika</span><span class="sxs-lookup"><span data-stu-id="bccfa-178">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
