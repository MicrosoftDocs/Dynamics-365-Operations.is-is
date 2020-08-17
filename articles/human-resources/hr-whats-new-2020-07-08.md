---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources (08. júlí 2020)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 07/08/2020
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
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c4382aa7473e2b67201ac00753ac9abe11b3c646
ms.sourcegitcommit: 81296c49be9953aa01e15527c34d0ef13b4622a9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/22/2020
ms.locfileid: "3614363"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a><span data-ttu-id="87fb5-103">Nýjungar eða breytingar í Dynamics 365 Human Resources (8. júlí 2020)</span><span class="sxs-lookup"><span data-stu-id="87fb5-103">What's new or changed in Dynamics 365 Human Resources (July 8, 2020)</span></span>

<span data-ttu-id="87fb5-104">Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="87fb5-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="87fb5-105">Breytingar eiga við um byggingarnúmer 8.1.3382.</span><span class="sxs-lookup"><span data-stu-id="87fb5-105">Changes apply to build number 8.1.3382.</span></span> <span data-ttu-id="87fb5-106">Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera LCS fyrir tilvísun.</span><span class="sxs-lookup"><span data-stu-id="87fb5-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="database-logging"></a><span data-ttu-id="87fb5-107">Gagnagrunnsskráning</span><span class="sxs-lookup"><span data-stu-id="87fb5-107">Database logging</span></span>

<span data-ttu-id="87fb5-108">Gagnagrunnsskráning gerir notendum kleift að ákvarða hvaða töflum og reitum á að fylgjast með.</span><span class="sxs-lookup"><span data-stu-id="87fb5-108">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="87fb5-109">Hann gerir einnig kleift að ákvarða tilvikin sem eiga að kveikja á breytingarakningu.</span><span class="sxs-lookup"><span data-stu-id="87fb5-109">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="87fb5-110">Notið möguleika gagnagrunnsskráningar til að sjá þessar breytingar yfir tíma.</span><span class="sxs-lookup"><span data-stu-id="87fb5-110">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="87fb5-111">Frekari upplýsingar er að finna í [Skilgreina og stjórna gagnagrunnsskráningu](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="87fb5-111">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="87fb5-112">Grunnstilla heiti á sjálfsafgreiðslu starfsmanns</span><span class="sxs-lookup"><span data-stu-id="87fb5-112">Configure the name of Employee self service</span></span>

<span data-ttu-id="87fb5-113">Í **færibreytum mannauðs** er nú hægt að breyta heiti vinnusvæði fyrir **Sjálfsafgreiðslu starfsmanns** í **Sjálfsafgreiðsla**.</span><span class="sxs-lookup"><span data-stu-id="87fb5-113">In **Human Resources parameters**, you can now change the name of the **Employee self service** workspace to **Self service**.</span></span> <span data-ttu-id="87fb5-114">Frekari upplýsingar er að finna á [Breyta heiti á sjálfsafgreiðsluvinnusvæði starfsmanns](hr-employee-self-service-workspace-name.md)</span><span class="sxs-lookup"><span data-stu-id="87fb5-114">For more information, see [Change Employee self service workspace name](hr-employee-self-service-workspace-name.md)</span></span>

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a><span data-ttu-id="87fb5-115">Aðgangur að opinni skráningu fríðindastjórnunar utan tímabils</span><span class="sxs-lookup"><span data-stu-id="87fb5-115">Benefits management open enrollment access outside of period</span></span>

<span data-ttu-id="87fb5-116">Þessi útgáfa lagar villu þar sem starfsmenn gátu fengið aðgang að opinni skráningu fríðinda utan skráningartímans eða án fríðindaviðburðar.</span><span class="sxs-lookup"><span data-stu-id="87fb5-116">This release fixes a bug where employees could access benefits open enrollment outside of the enrollment period or without a life event.</span></span> <span data-ttu-id="87fb5-117">Þar af leiðandi, ef þú þarft að prufukeyra opna skráningu í sjálfsafgreiðslu starfsmanns, þarftu að breyta dagsetningum opinnar skráningar yfir í daginn í dag (eða fyrr) til að gera hana aðgengilega.</span><span class="sxs-lookup"><span data-stu-id="87fb5-117">As a result, if you need to demo open enrollment in Employee self service, you must adjust the open enrollment dates to today (or earlier) to make it accessible.</span></span> <span data-ttu-id="87fb5-118">Hægt er að breyta þessari stillingu undir **Fríðindastjórnun > Reglur og valkostir tímabila**.</span><span class="sxs-lookup"><span data-stu-id="87fb5-118">You can change this setting under **Benefits management > Rules and options periods**.</span></span>

## <a name="email-employee-enrollment-confirmation"></a><span data-ttu-id="87fb5-119">Senda starfsmanni staðfestingu á skráningu í tölvupósti</span><span class="sxs-lookup"><span data-stu-id="87fb5-119">Email employee enrollment confirmation</span></span>

<span data-ttu-id="87fb5-120">Nú er hægt að senda tölvupóst til starfsmanna eftir að hann lýkur fríðindavali sínu.</span><span class="sxs-lookup"><span data-stu-id="87fb5-120">You can now send emails to employees after they complete their benefits selection.</span></span> <span data-ttu-id="87fb5-121">Annaðhvort er hægt að senda sjálfgefin skilaboð eða nota tölvupóstssniðmát fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="87fb5-121">You can either send a default message or use an organization email template.</span></span> <span data-ttu-id="87fb5-122">Þessar stillingar eru undir **Færibreytur í mannauðsstjórnun > Fríðindastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="87fb5-122">These settings are under **Human resource parameters > Benefits management**.</span></span>

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a><span data-ttu-id="87fb5-123">Ógilt leyfi birtist enn í væntanlegu fríi á vinnusvæði starfsfólks (441358)</span><span class="sxs-lookup"><span data-stu-id="87fb5-123">Canceled leave still appears in upcoming time off on People workspace (441358)</span></span>

<span data-ttu-id="87fb5-124">Afturkallað leyfi birtist ekki lengur sem væntanlegt frí á leyfisspjaldinu á vinnusvæðinu **Starfsfólk**.</span><span class="sxs-lookup"><span data-stu-id="87fb5-124">Canceled leave no longer displays as upcoming time off on the leave cards in the **People** workspace.</span></span>

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a><span data-ttu-id="87fb5-125">Ekki er hægt að nota eiginleika deildareiningar í PositionV2-einingunni (456486)</span><span class="sxs-lookup"><span data-stu-id="87fb5-125">Unable to use the department entity property in the PositionV2 entity (456486)</span></span>

<span data-ttu-id="87fb5-126">Nú er hægt að bæta deild við án þess að stofna tvítekin tengsl.</span><span class="sxs-lookup"><span data-stu-id="87fb5-126">You can now add a department without creating a duplicate relation.</span></span>

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a><span data-ttu-id="87fb5-127">PayrollWorkerEnrolledBenefitDetailEntity ætti aðeins að nota reiknaðan reit fyrir starfslokaáætlanir (459779)</span><span class="sxs-lookup"><span data-stu-id="87fb5-127">PayrollWorkerEnrolledBenefitDetailEntity should only use calculated field for retirement plans (459779)</span></span>

<span data-ttu-id="87fb5-128">Þegar einingin **PayrollWorkerEnrolledBenefitDetailEntity** er flutt út, ákvarðar útflutningurinn hvort nota eigi reiknaðan reit samkvæmt gengistöflu eða nota reitinn **ContributionAmountCur** á stuðningstöflunni.</span><span class="sxs-lookup"><span data-stu-id="87fb5-128">When exporting the **PayrollWorkerEnrolledBenefitDetailEntity** entity, the export determines whether it should use a calculated field based on a rate table or use the **ContributionAmountCur** field on the backing table.</span></span> <span data-ttu-id="87fb5-129">Rökin sem gagnaeiningin notar nýtir sér gengistöfluna í kringumstæðum þar sem forritið virkar yfirleitt ekki.</span><span class="sxs-lookup"><span data-stu-id="87fb5-129">The logic used by the data entity uses the rate table in situations where the application normally doesn't.</span></span> <span data-ttu-id="87fb5-130">Þessi rök valda því að útflutningar gagna skilar núllgildi fyrir þennan dálk, því að engin gengistafla útreiknings er til staðar og afurðin leyfir ekki viðskiptavininum að tilgreina slíka.</span><span class="sxs-lookup"><span data-stu-id="87fb5-130">This logic causes the entity exports to return a zero value for this column, because there's no calculation rate table and the product doesn't allow the customer to specify one.</span></span>
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a><span data-ttu-id="87fb5-131">Ruglingslegar þýðingar á tékknesku í Starfsmannastjórnun og sjálfsafgreiðslu starfsmanna (400276)</span><span class="sxs-lookup"><span data-stu-id="87fb5-131">Confusing translations in Czech language in Personnel management and Employee self service (400276)</span></span>

<span data-ttu-id="87fb5-132">Þessi útgáfa leiðréttir þýðingarnar fyrir **Skráasafn fyrirtækis**, **Næsta skráða námskeið**, **Verk** og **Staða**.</span><span class="sxs-lookup"><span data-stu-id="87fb5-132">This release corrects the translations for **Company directory**, **Next registered course**, **Job**, and **Position**.</span></span>
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a><span data-ttu-id="87fb5-133">Taflan WorkCalendarEmployment er ekki með stofnaða og breytta kerfisreiti virka (460171)</span><span class="sxs-lookup"><span data-stu-id="87fb5-133">The WorkCalendarEmployment table doesn't have the created and modified system fields enabled (460171)</span></span>

<span data-ttu-id="87fb5-134">Stofnaðir og breyttir reitir kerfisins eru nú virkir í töflunni **WorkCalendarEmployment** í Mannauð.</span><span class="sxs-lookup"><span data-stu-id="87fb5-134">Created and modified system fields are now enabled on the **WorkCalendarEmployment** table in Human Resources.</span></span>
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a><span data-ttu-id="87fb5-135">Undantekning núlltilvísunar fyrir Ráða og bæta við upplýsingum fyrir framtíðarstarfsmenn (455475)</span><span class="sxs-lookup"><span data-stu-id="87fb5-135">Null reference exception for Hire and add details for future employee (455475)</span></span>

<span data-ttu-id="87fb5-136">Þessi útgáfa leiðréttir villu (núlltilvísun) í einfaldaðri starfsmannafærslu þegar starfsmaður er ráðinn með því að nota valmöguleikann **Ráða og bæta við upplýsingum**.</span><span class="sxs-lookup"><span data-stu-id="87fb5-136">This release corrects an error (null reference) in streamlined employee entry when you hire an employee using the option to **Hire and add details**.</span></span>

## <a name="changes-made-in-the-common-data-service-worker-entity-dont-reflect-in-human-resources-455652"></a><span data-ttu-id="87fb5-137">Breytingar sem gerðar eru í Common Data Service starfsmannaeiningunni koma ekki fram í Mannauðnum (455652)</span><span class="sxs-lookup"><span data-stu-id="87fb5-137">Changes made in the Common Data Service Worker entity don't reflect in Human Resources (455652)</span></span>

<span data-ttu-id="87fb5-138">Breytingar sem gerðar eru á eftirfarandi reitum í einingunni **Starfsmaður** í Common Data Service birtast nú í Mannauð:</span><span class="sxs-lookup"><span data-stu-id="87fb5-138">Changes made to the following fields in the **Worker** entity in Common Data Service will now show up in Human Resources:</span></span>

- <span data-ttu-id="87fb5-139">**Vinnur heima**</span><span class="sxs-lookup"><span data-stu-id="87fb5-139">**Works from home**</span></span>
- <span data-ttu-id="87fb5-140">**Starfsaldursdagsetning**</span><span class="sxs-lookup"><span data-stu-id="87fb5-140">**Seniority date**</span></span>
- <span data-ttu-id="87fb5-141">**Árleg dagsetning**</span><span class="sxs-lookup"><span data-stu-id="87fb5-141">**Anniversary date**</span></span>
- <span data-ttu-id="87fb5-142">**Upprunaleg ráðningardagsetning**</span><span class="sxs-lookup"><span data-stu-id="87fb5-142">**Original hire date**</span></span>

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a><span data-ttu-id="87fb5-143">Rétt launastig er ekki sjálfgefið samkvæmt starfi sem úthlutað er á stöðuna (394136)</span><span class="sxs-lookup"><span data-stu-id="87fb5-143">Correct compensation level doesn't default based on the job assigned to the position (394136)</span></span>

<span data-ttu-id="87fb5-144">Með þessari breytingu verður rétt launastig sjálfgefið samkvæmt færslunum **Gildisdagur** fyrir **Upplýsingar um stöðu** og **Upphafsdagur** í **Úthlutun launafyrirkomulags**.</span><span class="sxs-lookup"><span data-stu-id="87fb5-144">With this change, the correct compensation level defaults based on the **Date effective** records for the **Position details** and the **Start date** of the **Compensation plan assignment**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="87fb5-145">Í kynningarútgáfu</span><span class="sxs-lookup"><span data-stu-id="87fb5-145">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="87fb5-146">Áskildir reitir</span><span class="sxs-lookup"><span data-stu-id="87fb5-146">Mandatory fields</span></span> 

<span data-ttu-id="87fb5-147">Nú er hægt að gera reiti áskilda með því að nota sérstillingarmöguleika Human Resources.</span><span class="sxs-lookup"><span data-stu-id="87fb5-147">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="87fb5-148">Þessi eiginleiki krefst **Vistuð yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="87fb5-148">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="87fb5-149">Forrit „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="87fb5-149">Human Resources application in Teams</span></span>

<span data-ttu-id="87fb5-150">Starfsmenn geta skoðað og beðið um tíma frá vinnu innan Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="87fb5-150">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="87fb5-151">Hægt er að hafa umsjón með þjark til að búa til beiðnir um leyfi.</span><span class="sxs-lookup"><span data-stu-id="87fb5-151">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="87fb5-152">Frekari upplýsingar er að finna í [Forrit Human Resources í Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="87fb5-152">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="87fb5-153">Einingar gagnastjórnunarramma (DMF) fyrir fríðindastjórnun</span><span class="sxs-lookup"><span data-stu-id="87fb5-153">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="87fb5-154">Einingar fríðindastjórnunar eru að gefa út.</span><span class="sxs-lookup"><span data-stu-id="87fb5-154">Benefits management entities are releasing.</span></span> <span data-ttu-id="87fb5-155">DMF-einingar leyfa innflutning og útflutning gagna til að skilgreina fríðindastjórnun á auðveldan hátt.</span><span class="sxs-lookup"><span data-stu-id="87fb5-155">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="87fb5-156">Sniðmát fríðindastjórnunar verður í boði til að flytja gögn.</span><span class="sxs-lookup"><span data-stu-id="87fb5-156">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="87fb5-157">Sniðmátið flytur út og flytur inn gögnin í ákveðinni röð til að virða gagnatengsl.</span><span class="sxs-lookup"><span data-stu-id="87fb5-157">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="87fb5-158">Kaupa og selja leyfisdaga</span><span class="sxs-lookup"><span data-stu-id="87fb5-158">Buy and sell leave</span></span> 

<span data-ttu-id="87fb5-159">Sum fyrirtæki bjóða upp á fríðindi sem gera starfsmönnum kleift að kaupa eða selja leyfisdaga.</span><span class="sxs-lookup"><span data-stu-id="87fb5-159">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="87fb5-160">Þessu ferli er oft stjórnað handvirkt.</span><span class="sxs-lookup"><span data-stu-id="87fb5-160">This process is often managed manually.</span></span> <span data-ttu-id="87fb5-161">Þessi eiginleiki gerir umsjón með stefnum og beiðnum sjálfvirka fyrir mannauðsdeildina.</span><span class="sxs-lookup"><span data-stu-id="87fb5-161">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="87fb5-162">Hann einfaldar ferli leyfisstjórnunar og hjálpar til við að koma í veg fyrir mistök.</span><span class="sxs-lookup"><span data-stu-id="87fb5-162">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="87fb5-163">Frekari upplýsingar má finna á</span><span class="sxs-lookup"><span data-stu-id="87fb5-163">For more information, see:</span></span>

- [<span data-ttu-id="87fb5-164">Stjórna reglum fyrir kaup og sölu á leyfisdögum</span><span class="sxs-lookup"><span data-stu-id="87fb5-164">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="87fb5-165">Kaupa og selja leyfisdaga</span><span class="sxs-lookup"><span data-stu-id="87fb5-165">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="87fb5-166">Uppsafnað leyfi fyrir eitt fyrirtæki eða eina áætlun</span><span class="sxs-lookup"><span data-stu-id="87fb5-166">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="87fb5-167">Viðskiptavinir geta unnið úr uppsöfnunum fyrir eitt fyrirtæki eða eina áætlun leyfis og fjarveru.</span><span class="sxs-lookup"><span data-stu-id="87fb5-167">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="87fb5-168">Þessi möguleiki varpar betra ljósi á uppsöfnunarferlið yfir viðskiptavini með mismunandi reglur fyrir leyfisár eða leyfisuppsöfnun.</span><span class="sxs-lookup"><span data-stu-id="87fb5-168">This ability provides clarity for the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="87fb5-169">Frekari upplýsingar er að finna í [Uppsafnað leyfi á fyrirtæki eða leyfisáætlun](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span><span class="sxs-lookup"><span data-stu-id="87fb5-169">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="87fb5-170">Bæta viðhengjum við frítímabeiðnir</span><span class="sxs-lookup"><span data-stu-id="87fb5-170">Add attachments to time-off requests</span></span>

<span data-ttu-id="87fb5-171">Möguleikinn á því að bæta viðhengjum við samþykktar leyfisbeiðnir er mikilvægur á þessum COVID 19-tímum.</span><span class="sxs-lookup"><span data-stu-id="87fb5-171">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="87fb5-172">Starfsmenn geta nú bætt við þessum viðhengjum.</span><span class="sxs-lookup"><span data-stu-id="87fb5-172">Employees can now add these attachments.</span></span> <span data-ttu-id="87fb5-173">Þeir hafa einnig meiri innsýn í hvernig uppfærslur á leyfisbeiðnum eru gerðar.</span><span class="sxs-lookup"><span data-stu-id="87fb5-173">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="87fb5-174">Frekari upplýsingar er að finna í [Bæta viðhengi við fyrirliggjandi beiðni](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="87fb5-174">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="87fb5-175">Bæta ástæðukóða við frestun uppsöfnunar</span><span class="sxs-lookup"><span data-stu-id="87fb5-175">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="87fb5-176">Ástæðukóðum hefur verið bætt við uppsöfnun í bið.</span><span class="sxs-lookup"><span data-stu-id="87fb5-176">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="87fb5-177">Yfirfærslureglur</span><span class="sxs-lookup"><span data-stu-id="87fb5-177">Carry forward rules</span></span> 

<span data-ttu-id="87fb5-178">Hægt er að tilgreina yfirfærsluorlofsgerð fyrir yfirfærslustöður þar sem yfirfærsluleiðréttingar eru fluttar.</span><span class="sxs-lookup"><span data-stu-id="87fb5-178">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="87fb5-179">Til dæmis, ef starfsmaður yfirfærir 10 daga getur þú valið aðra leyfisgerð fyrir þessa 10 daga.</span><span class="sxs-lookup"><span data-stu-id="87fb5-179">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="87fb5-180">Fyrir frekari upplýsingar, sjá [Grunnstilla gerðir leyfis og fjarvista](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="87fb5-180">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="87fb5-181">Uppsafnað leyfi í bið fyrir tilteknar leyfisgerðir</span><span class="sxs-lookup"><span data-stu-id="87fb5-181">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="87fb5-182">Hægt er að búa til reglu til að fresta uppsöfnun leyfis fyrir starfsmenn með beiðnum um leyfi sem færðar eru inn fyrir ógreitt leyfi.</span><span class="sxs-lookup"><span data-stu-id="87fb5-182">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="87fb5-183">Ógreit leyfi getur verið gerð, en þarf ekki að vera það.</span><span class="sxs-lookup"><span data-stu-id="87fb5-183">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="87fb5-184">Hægt er að fresta öllu leyfi út frá gerð annarrar leyfisgerðar.</span><span class="sxs-lookup"><span data-stu-id="87fb5-184">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="87fb5-185">DMF-eining er í boði fyrir frestun uppsöfnunar</span><span class="sxs-lookup"><span data-stu-id="87fb5-185">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="87fb5-186">DMF-eining er ekki til staðar fyrir uppsöfnun í bið.</span><span class="sxs-lookup"><span data-stu-id="87fb5-186">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="87fb5-187">Væntanlegt</span><span class="sxs-lookup"><span data-stu-id="87fb5-187">Coming soon</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="87fb5-188">Einingar gátlista innifaldar í Common Data Service</span><span class="sxs-lookup"><span data-stu-id="87fb5-188">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="87fb5-189">Gátlistaeiningar fyrir Ráðstafanir vegna nýrra starfsmanna, Ráðstafanir vegna starfsloka og viðskiptaferla verða bráðum tiltækar í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="87fb5-189">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="87fb5-190">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="87fb5-190">See also</span></span>

[<span data-ttu-id="87fb5-191">Nýjungar í Human Resources</span><span class="sxs-lookup"><span data-stu-id="87fb5-191">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="87fb5-192">Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019</span><span class="sxs-lookup"><span data-stu-id="87fb5-192">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="87fb5-193">Uppfærsluferli</span><span class="sxs-lookup"><span data-stu-id="87fb5-193">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="87fb5-194">Vinna með eiginleika</span><span class="sxs-lookup"><span data-stu-id="87fb5-194">Manage features</span></span>](hr-admin-manage-features.md)
