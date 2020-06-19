---
title: Hvað er nýtt eða breytt í Dynamics 365 Human Resources (28. maí 2020)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2020
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
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c386025843edef83d229a42d3f2314678fadae20
ms.sourcegitcommit: beddfba095c23b3265f0004f5124c4e9dc6404cc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411931"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a><span data-ttu-id="956b1-103">Hvað er nýtt eða breytt í Dynamics 365 Human Resources (28. maí 2020)</span><span class="sxs-lookup"><span data-stu-id="956b1-103">What's new or changed in Dynamics 365 Human Resources (May 28, 2020)</span></span>

<span data-ttu-id="956b1-104">Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="956b1-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="956b1-105">Breytingar eiga við um byggingarnúmer 8.1.3287.</span><span class="sxs-lookup"><span data-stu-id="956b1-105">Changes apply to build number 8.1.3287.</span></span> <span data-ttu-id="956b1-106">Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera LCS fyrir tilvísun.</span><span class="sxs-lookup"><span data-stu-id="956b1-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a><span data-ttu-id="956b1-107">LeaveRequest virkar ekki þegar margar gerðir eru gerðar fyrir hverja leyfisáætlun (447498)</span><span class="sxs-lookup"><span data-stu-id="956b1-107">LeaveRequest entity doesn't work when you enable multiple types per leave plan (447498)</span></span>

<span data-ttu-id="956b1-108">Með þessari breytingu er **LeaveEnrollmentV2Entity** nú tiltæk til að leiðrétta villuna sem kemur upp þegar margar leyfisgerðir eru gerðar virkar.</span><span class="sxs-lookup"><span data-stu-id="956b1-108">With this change, the **LeaveEnrollmentV2Entity** is now available to correct the error that occurs when you enable multiple leave types.</span></span>

## <a name="batch-contention-reduction-feature-preview-446619"></a><span data-ttu-id="956b1-109">Minnkunareiginleiki runusteytingar (forútgáfa) (446619)</span><span class="sxs-lookup"><span data-stu-id="956b1-109">Batch contention reduction feature (preview) (446619)</span></span>

<span data-ttu-id="956b1-110">Þegar þessi eiginleiki er gerður virkur má búast við fækkun á lokunum á rammatöflum runu við verkval og verklok.</span><span class="sxs-lookup"><span data-stu-id="956b1-110">When you enable this feature, you can expect a reduction in blocking on batch framework tables while selecting tasks and finishing jobs.</span></span>

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a><span data-ttu-id="956b1-111">UppdateConflict þegar starfsmenn eru vistaðir kemur í veg fyrir breytingu á færslu í Einstaklingar (427915)</span><span class="sxs-lookup"><span data-stu-id="956b1-111">UpdateConflict while saving worker prevents editing a record in People (427915)</span></span>

<span data-ttu-id="956b1-112">Þessi breyting leiðréttir villu þegar nýjum starfsmanni er bætt við, upplýsingum um aðsetur er breytt og kjörstillingum tungumáls er breytt.</span><span class="sxs-lookup"><span data-stu-id="956b1-112">This change corrects an error when adding a new worker, updating address information, and changing language preference.</span></span> <span data-ttu-id="956b1-113">Í þessari sérstöku atburðarás birtist villa sem gefur til kynna að ekki hafi verið hægt að uppfæra færsluna.</span><span class="sxs-lookup"><span data-stu-id="956b1-113">In this unique scenario, an error displayed indicating the record couldn't be updated.</span></span> 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a><span data-ttu-id="956b1-114">Ekki er hægt að bæta viðhengi við samþykkta beiðni um leyfi til að endursenda (425407)</span><span class="sxs-lookup"><span data-stu-id="956b1-114">Unable to add an attachment to an approved leave request to resubmit (425407)</span></span>

<span data-ttu-id="956b1-115">Þessi breyting leyfir nú viðhengi við samþykktar leyfisbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="956b1-115">This change now allows attachments to approved leave requests.</span></span>

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a><span data-ttu-id="956b1-116">Notandi getur fært inn laun fyrir starfsmann í skjámynd annars lögaðila (409529)</span><span class="sxs-lookup"><span data-stu-id="956b1-116">User can enter compensation for an employee in a different legal entity form (409529)</span></span>

<span data-ttu-id="956b1-117">Þessi breyting slekkur á launavalkostum til að koma í veg fyrir að launafærslur séu óvart færðar inn í rangan lögaðila.</span><span class="sxs-lookup"><span data-stu-id="956b1-117">This change disables compensation options to prevent inadvertent entry of compensation records for the wrong legal entity.</span></span>

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a><span data-ttu-id="956b1-118">Villa þegar starfsmaður er fluttur og úthlutunardagur stöðu starfsmanns er á undan tímalengd stöðu (429402)</span><span class="sxs-lookup"><span data-stu-id="956b1-118">Error when you transfer an employee and the Worker position assignment date is before the position duration (429402)</span></span>

<span data-ttu-id="956b1-119">Villuboð þegar starfsmaður er fluttur í þessari atburðarás hafa verið uppfærð til að geta lýst betur þeim breytingum sem þarf til að leiðrétta vandamálið.</span><span class="sxs-lookup"><span data-stu-id="956b1-119">Error messages when transferring an employee in this scenario have been updated to better describe the changes needed to correct the problem.</span></span>

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a><span data-ttu-id="956b1-120">Möguleikar viðhengja í sjálfsafgreiðslu fríðindaskráningar starfsmanns</span><span class="sxs-lookup"><span data-stu-id="956b1-120">Attachments capabilities in Employee self service benefits enrollment</span></span>
 
<span data-ttu-id="956b1-121">Nú er hægt að bæta viðhengjum við ferli fríðindaskráningar fyrir hverja áætlun sem starfsmaðurinn skráir sig í.</span><span class="sxs-lookup"><span data-stu-id="956b1-121">Now you can add attachments during the benefits enrollment process for each plan that the employee's enrolling in.</span></span> <span data-ttu-id="956b1-122">Hægt er að skoða viðhengin í skjámyndinni **Skráð fríðindi starfsmanns**.</span><span class="sxs-lookup"><span data-stu-id="956b1-122">You can then view the attachments within the **Worker enrolled benefit** form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="956b1-123">Í kynningarútgáfu</span><span class="sxs-lookup"><span data-stu-id="956b1-123">In preview</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="956b1-124">Forrit „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="956b1-124">Human Resources application in Teams</span></span>

<span data-ttu-id="956b1-125">Starfsmenn geta skoðað og beðið um tíma frá vinnu innan Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="956b1-125">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="956b1-126">Hægt er að hafa umsjón með þjark til að búa til beiðnir um leyfi.</span><span class="sxs-lookup"><span data-stu-id="956b1-126">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="956b1-127">Frekari upplýsingar er að finna í [Forrit Human Resources í Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="956b1-127">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="leave-suspension"></a><span data-ttu-id="956b1-128">Frestun leyfis</span><span class="sxs-lookup"><span data-stu-id="956b1-128">Leave suspension</span></span>

<span data-ttu-id="956b1-129">Þú getur frestað leyfi og fjarvistum í Human Resources fyrir starfsmann.</span><span class="sxs-lookup"><span data-stu-id="956b1-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="956b1-130">Frestun leyfis stöðvar leyfisuppsöfnun fyrir valdar leyfisgerðir.</span><span class="sxs-lookup"><span data-stu-id="956b1-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="956b1-131">Ef frestunin á sér stað eftir að uppsöfnun hefur verið unnin skapar frestun leyfis hlutfallslega leiðréttingu á leyfisstöðu starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="956b1-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="956b1-132">Frekari upplýsingar eru í [Fresta leyfi](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="956b1-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="956b1-133">Uppfæra notendaupplifun til að sýna að uppsöfnun sé frestað (429550)</span><span class="sxs-lookup"><span data-stu-id="956b1-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="956b1-134">Notandaupplifunin sýnir nú að uppsöfnun hafi verið frestað fyrir áætlun.</span><span class="sxs-lookup"><span data-stu-id="956b1-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="956b1-135">Væntanlegt</span><span class="sxs-lookup"><span data-stu-id="956b1-135">Coming soon</span></span>

## <a name="database-logging-in-preview-in-june"></a><span data-ttu-id="956b1-136">Skráning gagnagrunns (í forútgáfu í júní)</span><span class="sxs-lookup"><span data-stu-id="956b1-136">Database logging (in preview in June)</span></span>

<span data-ttu-id="956b1-137">Eiginleiki gagnagrunnskladda gerir notendum kleift að ákvarða hvaða töflu og reiti á að fylgjast með.</span><span class="sxs-lookup"><span data-stu-id="956b1-137">The database logging feature allows you to determine which table and fields should be monitored.</span></span> <span data-ttu-id="956b1-138">Hann gerir einnig kleift að ákvarða tilvikin sem eiga að kveikja á breytingarakningu.</span><span class="sxs-lookup"><span data-stu-id="956b1-138">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="956b1-139">Fyrirspurnarmöguleikar eru í boði til að sjá þessar breytingar yfir tíma.</span><span class="sxs-lookup"><span data-stu-id="956b1-139">Inquiry capabilities are available to see these changes over time.</span></span>

## <a name="buy-and-sell-leave-in-preview-june-1"></a><span data-ttu-id="956b1-140">Kaupa og selja leyfisdaga (í forútgáfu 1. júní)</span><span class="sxs-lookup"><span data-stu-id="956b1-140">Buy and sell leave (in preview June 1)</span></span>

<span data-ttu-id="956b1-141">Sum fyrirtæki bjóða upp á fríðindi sem gera starfsmönnum kleift að kaupa eða selja leyfisdaga.</span><span class="sxs-lookup"><span data-stu-id="956b1-141">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="956b1-142">Þessu ferli er oft stjórnað handvirkt.</span><span class="sxs-lookup"><span data-stu-id="956b1-142">This process is often managed manually.</span></span> <span data-ttu-id="956b1-143">Þessi eiginleiki býður upp á sjálfvirkari leið til að stjórna stefnum og beiðnum fyrir mannauðsdeildina og auðveldar að koma í veg fyrir mistök við einföldun á ferli leyfisstjórnunar.</span><span class="sxs-lookup"><span data-stu-id="956b1-143">This feature provides a more automated way to manage policies and requests for the HR department, and it helps eliminate mistakes while streamlining the leave management process.</span></span>

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="956b1-144">Einingar gagnastjórnunarramma (DMF) fyrir fríðindastjórnun</span><span class="sxs-lookup"><span data-stu-id="956b1-144">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="956b1-145">Einingar fríðindastjórnunar eru að gefa út.</span><span class="sxs-lookup"><span data-stu-id="956b1-145">Benefits management entities are releasing.</span></span> <span data-ttu-id="956b1-146">DMF-einingar leyfa innflutning og útflutning gagna til að skilgreina fríðindastjórnun á auðveldan hátt.</span><span class="sxs-lookup"><span data-stu-id="956b1-146">DMF entities allow importing and exporting data to easily configure benefits management.</span></span> <span data-ttu-id="956b1-147">Sniðmát fríðindastjórnunar verður einnig í boði til að flytja gögn.</span><span class="sxs-lookup"><span data-stu-id="956b1-147">A Benefits management template will also be available to move data.</span></span> <span data-ttu-id="956b1-148">Sniðmátið flytur út og flytur inn gögnin í ákveðinni röð til að virða gagnatengsl.</span><span class="sxs-lookup"><span data-stu-id="956b1-148">The template exports and imports the data in a sequential manner to respect data dependencies.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a><span data-ttu-id="956b1-149">Bæta ástæðukóða við uppsöfnun í bið (1. júní)</span><span class="sxs-lookup"><span data-stu-id="956b1-149">Add reason code to accrual suspensions (June 1)</span></span>

<span data-ttu-id="956b1-150">Ástæðukóðum hefur verið bætt við uppsöfnun í bið.</span><span class="sxs-lookup"><span data-stu-id="956b1-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules-june-1"></a><span data-ttu-id="956b1-151">Yfirfærslureglur (1. júní)</span><span class="sxs-lookup"><span data-stu-id="956b1-151">Carry forward rules (June 1)</span></span>

<span data-ttu-id="956b1-152">Hægt er að tilgreina yfirfærsluorlofsgerð fyrir yfirfærslustöður þar sem yfirfærsluleiðréttingar eru fluttar.</span><span class="sxs-lookup"><span data-stu-id="956b1-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="956b1-153">Til dæmis, ef starfsmaður yfirfærir 10 daga getur þú valið aðra leyfisgerð fyrir þessa 10 daga.</span><span class="sxs-lookup"><span data-stu-id="956b1-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="956b1-154">Fyrir frekari upplýsingar, sjá [Grunnstilla gerðir leyfis og fjarvista](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="956b1-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a><span data-ttu-id="956b1-155">Uppsafnað leyfi í bið fyrir tilteknar leyfisgerðir (1. júní)</span><span class="sxs-lookup"><span data-stu-id="956b1-155">Suspend leave accrual for specified leave types (June 1)</span></span>

<span data-ttu-id="956b1-156">Í þessari útgáfu getur mannauður búið til reglu til að fresta uppsöfnun leyfis fyrir starfsmenn með beiðnum um leyfi sem færðar eru inn fyrir ógreitt leyfi.</span><span class="sxs-lookup"><span data-stu-id="956b1-156">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="956b1-157">Ógreit leyfi getur verið gerð, en þarf ekki að vera það.</span><span class="sxs-lookup"><span data-stu-id="956b1-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="956b1-158">Hægt er að fresta öllu leyfi út frá gerð annarrar leyfisgerðar.</span><span class="sxs-lookup"><span data-stu-id="956b1-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a><span data-ttu-id="956b1-159">DMF-eining er í boði fyrir frestun uppsöfnunar (1. júní)</span><span class="sxs-lookup"><span data-stu-id="956b1-159">DMF entity available for accrual suspensions (June 1)</span></span>

<span data-ttu-id="956b1-160">DMF-eining er ekki til staðar fyrir uppsöfnun í bið.</span><span class="sxs-lookup"><span data-stu-id="956b1-160">A DMF entity is now available for accrual suspensions.</span></span>