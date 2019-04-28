---
title: Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (14. desember 2018)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c2d209cac52665053b664a93bfb6c35e171b0948
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/12/2019
ms.locfileid: "949852"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-14-2018"></a><span data-ttu-id="e1e68-103">Nýjungar eða breytingar í Dynamics 365 for Talent Core HR (14. desember 2018)</span><span class="sxs-lookup"><span data-stu-id="e1e68-103">What's new or changed in Dynamics 365 for Talent Core HR (December 14, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e1e68-104">**Smíði 8.1.2085**</span><span class="sxs-lookup"><span data-stu-id="e1e68-104">**Build 8.1.2085**</span></span>

<span data-ttu-id="e1e68-105">Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Core HR.</span><span class="sxs-lookup"><span data-stu-id="e1e68-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="e1e68-106">Breytingar</span><span class="sxs-lookup"><span data-stu-id="e1e68-106">Changes</span></span>

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a><span data-ttu-id="e1e68-107">US - ACA (Affordable Care Act) stuðningur fyrir skattár 2018 eyðublöð 1095-B og 1095-C</span><span class="sxs-lookup"><span data-stu-id="e1e68-107">US - ACA (Affordable Care Act) support for tax year 2018 1095-B and 1095-C forms</span></span>

<span data-ttu-id="e1e68-108">Á hverju ári skulu Viðeigandi stórir vinnuveitendur (ALE) veita öllum starfsmönnum í fullu starfi 1095-C.</span><span class="sxs-lookup"><span data-stu-id="e1e68-108">Each year, Applicable Large Employers (ALEs) must provide each full-time employees with a 1095-C.</span></span> <span data-ttu-id="e1e68-109">Að auki, ef vinnuveitandinn veitir sjálfsábyrgðartryggingu skal hann útvega 1095-C (ef hann er ALE) og 1095-B (ef hann er lítill vinnuveitandi) til allra starfsmanna, í fullu starfi eða hlutastarfi, sem falla undir eina af sjúkratryggingum þeirra sem boðið er upp á.</span><span class="sxs-lookup"><span data-stu-id="e1e68-109">In addition, if the employer provides self-insured coverage they must provide the 1095-C (if they are an ALE) and a 1095-B (if they are a small employer) to any employee, full-time or part-time, covered under one of their offered health plans.</span></span> <span data-ttu-id="e1e68-110">Þessi eiginleiki veitir prenthæf eyðublöð fyrir bæði 1095-C og 1095-B.</span><span class="sxs-lookup"><span data-stu-id="e1e68-110">This feature provides printable forms for both the 1095-C and 1095-B.</span></span>

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a><span data-ttu-id="e1e68-111">Við innflutning er reiturinn SubmittedByPersonId í HcmPerfJournalEntity hunsaður</span><span class="sxs-lookup"><span data-stu-id="e1e68-111">During import SubmittedByPersonId field on HcmPerfJournalEntity is ignored</span></span>

<span data-ttu-id="e1e68-112">Við innflutning/útflutning á færslum frammistöðubókar er reiturinn **Sent inn af** hunsaður.</span><span class="sxs-lookup"><span data-stu-id="e1e68-112">When importing/exporting performance journal entries, the **Submitted by** field is ignored.</span></span> <span data-ttu-id="e1e68-113">Með þessari breytingu endurspeglar gildið **innflutt/útflutt** gildið í töflunni við útflutninginn, við innflutning verður kerfið uppfært með gildinu sem gefið er upp í innflutningsskránni.</span><span class="sxs-lookup"><span data-stu-id="e1e68-113">With this change, the value **imported/exported** will reflect the value in the table during the export, when importing the system will be updated with the value supplied in the import file.</span></span>

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a><span data-ttu-id="e1e68-114">Greiningarflipi á vinnusvæðinu „Leyfi og fjarvistir“ sýnir villuna „OpenConnectionError“ fyrir hlutverk sem heyrir ekki undir kerfisstjóra</span><span class="sxs-lookup"><span data-stu-id="e1e68-114">Analytics tab on 'Leave and absence' workspace displays "OpenConnectionError" error for non-system Admin roles</span></span>

<span data-ttu-id="e1e68-115">Með þessari uppfærslu verða engar villur sendar þegar flipinn **Greiningar** er opnaður á vinnusvæðinu **Leyfi og fjarvistir**.</span><span class="sxs-lookup"><span data-stu-id="e1e68-115">With this update, no errors will be issued when opening the **Analytics** tab on the **Leave and Absence** workspace.</span></span>

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="e1e68-116">Sjálfsafgreiðsla starfsmanns, köfun niður í stöðustigveldi úr reit mistekst að sækja yfirhnút</span><span class="sxs-lookup"><span data-stu-id="e1e68-116">Employee self-service, Position Hierarchy drill-down from tile fails to get parent node</span></span>

<span data-ttu-id="e1e68-117">Breyting hefur verið gerð til að leiðrétta villuna „Mistókst að sækja yfirhnútinn“ þegar stöðustigveldið hefur verið sérsniðið til að birtast á fyrirliggjandi vinnusvæði og staða er valin í stigveldinu.</span><span class="sxs-lookup"><span data-stu-id="e1e68-117">A change has been made to correct the error "Getting the parent node failed" when the position hierarchy has been personalized to appear on an existing workspace and a position is selected in the hierarchy.</span></span>  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a><span data-ttu-id="e1e68-118">Verður að vera kerfisstjóri til að sjá launaflipa á stöðusíðunni</span><span class="sxs-lookup"><span data-stu-id="e1e68-118">Must be System Admin to see the Payroll tab in the Position page</span></span>

<span data-ttu-id="e1e68-119">Breyting hefur verið gerð til að hafa með réttar öryggiseiningar í fyrirliggjandi réttindum: „Vinna með upplýsingar um laun starfsmanns og stöðu“.</span><span class="sxs-lookup"><span data-stu-id="e1e68-119">A change has been made to include the correct security elements in the existing privilege: "Maintain payroll worker and position detail".</span></span> <span data-ttu-id="e1e68-120">Með þessari breytingu hefur launastjórinn sjálfgefið aðgang að launasvæðum á stöðusíðunni.</span><span class="sxs-lookup"><span data-stu-id="e1e68-120">With this change, by default, the Payroll Administrator will have access to the Payroll fields on the Position page.</span></span>

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a><span data-ttu-id="e1e68-121">Villa þegar frammistöðumat var sent inn til yfirmanns og staðgengillinn %Reviews.PerfPeriod% er notaður í sendingarleiðbeiningum</span><span class="sxs-lookup"><span data-stu-id="e1e68-121">Error when submitting performance review to manager and the %Reviews.PerfPeriod% placeholder is used in the Submission instructions</span></span>

<span data-ttu-id="e1e68-122">Breyting hefur verið gerð sem leiðréttir villuna „Núlltilvísun“ þegar staðgengillinn %Reviews.PerfPeriod% er notaður í sendingarleiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="e1e68-122">A change has been made that corrects the "Null Reference" error when using the %Reviews.PerfPeriod% placeholder in the Submission instructions.</span></span>

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a><span data-ttu-id="e1e68-123">Skýrsla um vinnuafl Power BI sýnir villu þegar starfsaldursdagsetning starfskrafts er hlaupadagur</span><span class="sxs-lookup"><span data-stu-id="e1e68-123">Workforce Power BI report shows error when worker seniority date is a leap day</span></span>

<span data-ttu-id="e1e68-124">Með þessari breytingu eru hlaupadagar studdir í Power BI.</span><span class="sxs-lookup"><span data-stu-id="e1e68-124">With this change, leap days are now supported in Power BI.</span></span>

### <a name="integration-between-core-hr-and-attract"></a><span data-ttu-id="e1e68-125">Samþætting milli Core HR og Attract</span><span class="sxs-lookup"><span data-stu-id="e1e68-125">Integration between Core HR and Attract</span></span>

<span data-ttu-id="e1e68-126">Breyting hefur verið gerð til að uppfæra samþættingu milli Core HR og Attract sem tengist umsækjendum sem á að ráða.</span><span class="sxs-lookup"><span data-stu-id="e1e68-126">A change has been made to update the integration between Core HR and Attract related to candidates to hire.</span></span> <span data-ttu-id="e1e68-127">Til að umsækjendur sem á að ráða séu sýnilegir á vinnusvæðinu **Starfsmannastjórnun** eru eftirfarandi einingar Common Data Service notaðar:</span><span class="sxs-lookup"><span data-stu-id="e1e68-127">For candidates to hire to be visible in the **Personnel Management** workspace, the following Common Data Service entities are used:</span></span>

<span data-ttu-id="e1e68-128">Starfsumsókn</span><span class="sxs-lookup"><span data-stu-id="e1e68-128">Job Application</span></span>
- <span data-ttu-id="e1e68-129">Ástæða stöðu verður að vera stillt á Tilboð samþykkt</span><span class="sxs-lookup"><span data-stu-id="e1e68-129">Status Reason needs to be set to Offer Accepted</span></span>
-   <span data-ttu-id="e1e68-130">Sýnir umsækjanda og laust starf</span><span class="sxs-lookup"><span data-stu-id="e1e68-130">Provides Candidate and Job Opening</span></span>

<span data-ttu-id="e1e68-131">Umsækjandi</span><span class="sxs-lookup"><span data-stu-id="e1e68-131">Candidate</span></span>
-   <span data-ttu-id="e1e68-132">Sýnir upplýsingar um umsækjanda</span><span class="sxs-lookup"><span data-stu-id="e1e68-132">Provides Candidate information</span></span>

<span data-ttu-id="e1e68-133">Laust starf</span><span class="sxs-lookup"><span data-stu-id="e1e68-133">Job Opening</span></span>
-   <span data-ttu-id="e1e68-134">Sýnir auðkenni fyrir laust starf og þátttakendur lausa starfsins</span><span class="sxs-lookup"><span data-stu-id="e1e68-134">Provides Job Opening ID and Job Opening Participants</span></span>

<span data-ttu-id="e1e68-135">Þátttakendur lausa starfsins</span><span class="sxs-lookup"><span data-stu-id="e1e68-135">Job Opening Participants</span></span>
-   <span data-ttu-id="e1e68-136">Sýnir mannauðsstjóra</span><span class="sxs-lookup"><span data-stu-id="e1e68-136">Provides Hiring Manager</span></span>

<span data-ttu-id="e1e68-137">Þegar umsækjanda er bætt við starfsmannastjórnun getur hann nú einnig verið vísað frá með því að nota nýjan valkost sem er tiltækur á spjaldi umsækjanda.</span><span class="sxs-lookup"><span data-stu-id="e1e68-137">When a candidate is added to Personnel Management, the candidate can now also be dismissed using a new option available on the candidate card.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="e1e68-138">Væntanlegt</span><span class="sxs-lookup"><span data-stu-id="e1e68-138">Coming soon</span></span>

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a><span data-ttu-id="e1e68-139">Leyfi og fjarvistir: Stöður á leyfi fram í tímann og spár um leyfi</span><span class="sxs-lookup"><span data-stu-id="e1e68-139">Leave and absence: Future leave and forecasting leave balances</span></span>

<span data-ttu-id="e1e68-140">Með breytinginum sem eru gerðar til að leyfa starfsmönnum að spá fyrir um frítíma og framtíðaróskum um frítíma án þess að það hafi áhrif á núgildandi stöður frítíma, hvernig stöður frítíma eru birtar er einnig að breytast.</span><span class="sxs-lookup"><span data-stu-id="e1e68-140">With the changes being made to allow for employees to forecast time off and request future time off requests without impacting their current time off balances, the way the time off balances are displayed is also changing.</span></span> 

<span data-ttu-id="e1e68-141">Tiltæk staða sem er sýnd eins og er er upphæð frítíma sem er í boði fyrir beiðnir, þ.m.t. uppsafnanir til og með deginum í dag og allar samþykktar leyfisbeiðnir fram til lok tímabils.</span><span class="sxs-lookup"><span data-stu-id="e1e68-141">The available balance currently displayed is the amount of time off available for requests including accruals through today and all approved leave requests to the end of time.</span></span> 

<span data-ttu-id="e1e68-142">Þegar getan til að spá fyrir er gefin út, breytist staðan sem sýnd er í núgildandi stöðu frítíma ásamt uppsöfnunum og beiðnum til og með deginum í dag.</span><span class="sxs-lookup"><span data-stu-id="e1e68-142">When the ability to forecast is released, the balance displayed changes to  be the current balance of time off including accruals through today and requests through today.</span></span> <span data-ttu-id="e1e68-143">Starfsmenn og yfirmenn sjá þessar uppfærðu stöður í sjálfsafgreiðslu starfsmanna og yfirmanna í spjaldinu **Frítími** og í glugganum **Stöður frítíma**.</span><span class="sxs-lookup"><span data-stu-id="e1e68-143">Employees and managers will see these updated balances in employee and manager self-service on the **Time off** card and in the **Time off balances** window.</span></span> <span data-ttu-id="e1e68-144">Mannauðsstjórar munu sjá þessar uppfærðu stöður á vinnusvæðinu **Fólk** og glugganum **Úthlutaðar leyfisáætlanir** fyrir starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="e1e68-144">HR managers will see these updated balances in the **People** workspace and in the employee’s **Assigned leave plans** window.</span></span>

## <a name="known-issue"></a><span data-ttu-id="e1e68-145">Þekkt vandamál</span><span class="sxs-lookup"><span data-stu-id="e1e68-145">Known issue</span></span>

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a><span data-ttu-id="e1e68-146">Vörpunarvillur í samþættingu við Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e1e68-146">Mapping errors in the integration with Finance and Operations</span></span>

<span data-ttu-id="e1e68-147">Eftirfarandi vandamál hafa verið greind í núgildandi sniðmáti fyrir samþættingu Talent við Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e1e68-147">The following issues have been identified in the current template for integrating Talent with Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="e1e68-148">Nýtt sniðmát verður birt fljótlega og verður notað fyrir öll ný samþættingarverk sem eru búin til.</span><span class="sxs-lookup"><span data-stu-id="e1e68-148">A new template will be published soon and will be applied to all new integration projects that are created.</span></span> <span data-ttu-id="e1e68-149">Hægt er að uppfæra vörpunarverkin fyrir núverandi samþættingarverk.</span><span class="sxs-lookup"><span data-stu-id="e1e68-149">For existing integration projects, the task mappings can be updated.</span></span> <span data-ttu-id="e1e68-150">Frekari upplýsingar um uppfærðar varpanir eru í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="e1e68-150">Refer to the following table for updated mappings.</span></span> 

>[!NOTE]
> <span data-ttu-id="e1e68-151">Úthlutunarverk á stöðum starfa til staða yfirstarfa samþættir ekki gögn.</span><span class="sxs-lookup"><span data-stu-id="e1e68-151">The Job Positions to Positions Parent Job Assignment task does not integrate data.</span></span> <span data-ttu-id="e1e68-152">Þetta er mál sem verið er að rannsaka.</span><span class="sxs-lookup"><span data-stu-id="e1e68-152">This is an issue that is currently being researched.</span></span> <span data-ttu-id="e1e68-153">Það er engin hjáleið í núverandi vörpun.</span><span class="sxs-lookup"><span data-stu-id="e1e68-153">There is no workaround in the current mapping.</span></span> 

<span data-ttu-id="e1e68-154">Verk deilda til rekstrareiningar þarf eftirfarandi varpanir uppfærðar.</span><span class="sxs-lookup"><span data-stu-id="e1e68-154">The Departments to Operating unit task needs the following mappings updated.</span></span>

| <span data-ttu-id="e1e68-155">Fyrirliggjandi upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="e1e68-155">Existing source field</span></span>          | <span data-ttu-id="e1e68-156">Nýtt upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="e1e68-156">New source field</span></span> |
| -------------------------------|------------------|
| <span data-ttu-id="e1e68-157">cdm_description (lýsing)</span><span class="sxs-lookup"><span data-stu-id="e1e68-157">cdm_description (Description)</span></span>  | <span data-ttu-id="e1e68-158">cdm_name (heiti)</span><span class="sxs-lookup"><span data-stu-id="e1e68-158">cdm_name (Name)</span></span>  |

<span data-ttu-id="e1e68-159">Einnig þarf að bæta við aukalegri vörpun.</span><span class="sxs-lookup"><span data-stu-id="e1e68-159">An additional mapping also needs to be added.</span></span> <span data-ttu-id="e1e68-160">Veldu síðasta **Ekkert** svæðið til að bæta við eftirfarandi vörpun.</span><span class="sxs-lookup"><span data-stu-id="e1e68-160">Select the last **None** field to add the following mapping.</span></span>

| <span data-ttu-id="e1e68-161">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="e1e68-161">Source field</span></span>                   | <span data-ttu-id="e1e68-162">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="e1e68-162">Destination field</span></span>    |
| -------------------------------|----------------------|
| <span data-ttu-id="e1e68-163">cdm_description (lýsing)</span><span class="sxs-lookup"><span data-stu-id="e1e68-163">cdm_description (Description)</span></span>  | <span data-ttu-id="e1e68-164">NAMEALIAS (NAMEALIAS)</span><span class="sxs-lookup"><span data-stu-id="e1e68-164">NAMEALIAS (NAMEALIAS)</span></span>|

<span data-ttu-id="e1e68-165">Uppfærðu varpanirnar ættu að líta út eins og eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="e1e68-165">The updated mappings should look like the following image.</span></span>

![Deildir til rekstrareiningar verk](./media/DepartmentMapping.png)


<span data-ttu-id="e1e68-167">Verkið störf til upplýsingar um starf þarf eftirfarandi varpanir uppfærðar.</span><span class="sxs-lookup"><span data-stu-id="e1e68-167">The Jobs to Job Detail task needs the following mappings updated.</span></span>

| <span data-ttu-id="e1e68-168">Fyrirliggjandi upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="e1e68-168">Existing source field</span></span>          | <span data-ttu-id="e1e68-169">Nýtt upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="e1e68-169">New source field</span></span>                   |
| -------------------------------|------------------------------------|
| <span data-ttu-id="e1e68-170">cdm_name (heiti)</span><span class="sxs-lookup"><span data-stu-id="e1e68-170">cdm_name (Name)</span></span>                | <span data-ttu-id="e1e68-171">cdm_description (lýsing)</span><span class="sxs-lookup"><span data-stu-id="e1e68-171">cdm_description (Description)</span></span>      |
| <span data-ttu-id="e1e68-172">cdm_name (lýsing)</span><span class="sxs-lookup"><span data-stu-id="e1e68-172">cdm_name (Description)</span></span>         | <span data-ttu-id="e1e68-173">cdm_jobdescription (starfslýsing)</span><span class="sxs-lookup"><span data-stu-id="e1e68-173">cdm_jobdescription(Job Description)</span></span>|


<span data-ttu-id="e1e68-174">Uppfærðu varpanirnar ættu að líta út eins og myndin hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="e1e68-174">The updated mappings should look like the image below.</span></span>

![Störf til upplýsinga um starf verk](./media/JobMapping.png)

<span data-ttu-id="e1e68-176">Starfskraftar til vinnu verk þarf eftirfarandi varpanir uppfærðar.</span><span class="sxs-lookup"><span data-stu-id="e1e68-176">The Workers to Work task needs the following mappings updated.</span></span>

| <span data-ttu-id="e1e68-177">Fyrirliggjandi upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="e1e68-177">Existing source field</span></span>                 | <span data-ttu-id="e1e68-178">Nýtt upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="e1e68-178">New source field</span></span>                               |
| --------------------------------------|------------------------------------------------|
| <span data-ttu-id="e1e68-179">cdm_emailaddress1 (netfang 1)</span><span class="sxs-lookup"><span data-stu-id="e1e68-179">cdm_emailaddress1 (Email Address 1)</span></span>   | <span data-ttu-id="e1e68-180">cdm_primaryemailaddress (aðalnetfang</span><span class="sxs-lookup"><span data-stu-id="e1e68-180">cdm_primaryemailaddress (Primary Email Address</span></span> |
| <span data-ttu-id="e1e68-181">cdm_telephone1 (símanúmer 1)</span><span class="sxs-lookup"><span data-stu-id="e1e68-181">cdm_telephone1 (Telephone 1)</span></span>          | <span data-ttu-id="e1e68-182">cdm_primarytelephone (aðalsímanúmer)</span><span class="sxs-lookup"><span data-stu-id="e1e68-182">cdm_primarytelephone (Primary Telephone)</span></span>       |

<span data-ttu-id="e1e68-183">Umbreyting á svæði kyns þarf einnig að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="e1e68-183">The Gender field transform also needs to be updated.</span></span> <span data-ttu-id="e1e68-184">Veldu **fn** (virkni) vörpunargerð fyrir Kyn og uppfærðu eftirfarandi vörpunargildi.</span><span class="sxs-lookup"><span data-stu-id="e1e68-184">Select the **fn** (function) map type for Gender and update the following value mappings.</span></span>

| <span data-ttu-id="e1e68-185">Common Data Service gildi</span><span class="sxs-lookup"><span data-stu-id="e1e68-185">Common Data Service value</span></span>                   | <span data-ttu-id="e1e68-186">Gildi Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e1e68-186">Finance and Operations value</span></span>                     |
| ----------------------------|--------------------------------------------------|
| <span data-ttu-id="e1e68-187">75440000</span><span class="sxs-lookup"><span data-stu-id="e1e68-187">75440000</span></span>                    | <span data-ttu-id="e1e68-188">Karl</span><span class="sxs-lookup"><span data-stu-id="e1e68-188">Male</span></span>                                             |
| <span data-ttu-id="e1e68-189">75440001</span><span class="sxs-lookup"><span data-stu-id="e1e68-189">75440001</span></span>                    | <span data-ttu-id="e1e68-190">Kona</span><span class="sxs-lookup"><span data-stu-id="e1e68-190">Female</span></span>                                           |
| <span data-ttu-id="e1e68-191">75440002</span><span class="sxs-lookup"><span data-stu-id="e1e68-191">75440002</span></span>                    | <span data-ttu-id="e1e68-192">Enginn</span><span class="sxs-lookup"><span data-stu-id="e1e68-192">None</span></span>                                             | 
| <span data-ttu-id="e1e68-193">75440003</span><span class="sxs-lookup"><span data-stu-id="e1e68-193">75440003</span></span>                    | <span data-ttu-id="e1e68-194">Ótilgreint</span><span class="sxs-lookup"><span data-stu-id="e1e68-194">NonSpecific</span></span>                                      |

<span data-ttu-id="e1e68-195">Uppfærðu varpanirnar ættu að líta út eins og eftirfarandi myndir.</span><span class="sxs-lookup"><span data-stu-id="e1e68-195">The updated mappings should look like the following images.</span></span>

![Starfskraftar til starfskrafts verk](./media/WorkerMapping.png)

![Umbreyting á svæði kyns](./media/WorkerTransform.png)
