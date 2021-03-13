---
title: Nýjungar eða breytingar í Dynamics 365 Human Resources (11. júní 2020)
description: Í þessu efnisatriði er að finna lýsingu á nýjum eða breyttum eiginleikum í Microsoft Dynamics 365 Human Resources fyrir 11. júní 2020.
author: andreabichsel
manager: tfehr
ms.date: 06/16/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6ff359f65afc03a1b5691fddc078f73682e99e44
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127802"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a><span data-ttu-id="d903d-103">Nýjungar eða breytingar í Dynamics 365 Human Resources (11. júní 2020)</span><span class="sxs-lookup"><span data-stu-id="d903d-103">What's new or changed in Dynamics 365 Human Resources (June 11, 2020)</span></span>

<span data-ttu-id="d903d-104">Í þessari grein er að finna lýsingu á nýjum eða breyttum eiginleikum Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="d903d-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d903d-105">Breytingar eiga við um byggingarnúmer 8.1.3316.</span><span class="sxs-lookup"><span data-stu-id="d903d-105">Changes apply to build number 8.1.3316.</span></span> <span data-ttu-id="d903d-106">Tölurnar í sviga í sumum fyrirsögnum vísa til stuðningsnúmera LCS fyrir tilvísun.</span><span class="sxs-lookup"><span data-stu-id="d903d-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a><span data-ttu-id="d903d-107">Einfölduð skjámynd starfsmanns veldur því stundum að hnappar (X) sem loka undirskjámynd hætti að virka (442369)</span><span class="sxs-lookup"><span data-stu-id="d903d-107">Streamlined employee form sometimes causes child form close (X) buttons to stop working (442369)</span></span>

<span data-ttu-id="d903d-108">Þegar nýja skjámyndin **Starfsmaður** var virkjuð, virkaði stundum ekki hnappurinn (**X**) í undirskjámyndum sem lokar skjámynd.</span><span class="sxs-lookup"><span data-stu-id="d903d-108">When the new **Worker** form was enabled, the close (**X**) button occasionally didn't work on child forms.</span></span> <span data-ttu-id="d903d-109">Þetta vandamál kom upp annað slagið.</span><span class="sxs-lookup"><span data-stu-id="d903d-109">This problem was intermittent.</span></span> <span data-ttu-id="d903d-110">Hægt var að loka skjámyndinni eftir að hafa farið úr henni og komið aftur.</span><span class="sxs-lookup"><span data-stu-id="d903d-110">You could close the form after leaving and coming back to it.</span></span> <span data-ttu-id="d903d-111">Til dæmis var hægt að velja valmyndaratriði vinstra megin og fara aftur í skjámyndina **Starfsmaður** og síðan loka henni.</span><span class="sxs-lookup"><span data-stu-id="d903d-111">For example, you could select a menu item on the left, and navigate back to the **Worker** form, and then close it.</span></span> <span data-ttu-id="d903d-112">Útgáfa vikunnar lagar þetta vandamál.</span><span class="sxs-lookup"><span data-stu-id="d903d-112">This week's release fixes this problem.</span></span> 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a><span data-ttu-id="d903d-113">Einingin fyrir persónulegan tengilið starfsmanns flytur ekki út persónulega tengiliði með gerð yfirtengsla</span><span class="sxs-lookup"><span data-stu-id="d903d-113">The Worker personal contact person entity doesn't export personal contacts with a parent relationship type</span></span>

<span data-ttu-id="d903d-114">Með þessari útgáfu flytur einingin **Persónulegur tengiliður starfskrafts** út allar tengslagerðir.</span><span class="sxs-lookup"><span data-stu-id="d903d-114">With this release, the **Worker personal contact person** entity exports all relationship types.</span></span>

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a><span data-ttu-id="d903d-115">HcmPositionWorkerAssignmentV2Entity ætti að vera sjálfgefið hluti af samþættingarpakka Ceridian-launaskrár (448506)</span><span class="sxs-lookup"><span data-stu-id="d903d-115">The HcmPositionWorkerAssignmentV2Entity should be part of the Ceridian payroll integration package by default (448506)</span></span>

<span data-ttu-id="d903d-116">Með þessari breytingu er **HcmPositionWorkerAssignmentV2Entity** hluti af samþættingarpakka Ceridian-launaskrár.</span><span class="sxs-lookup"><span data-stu-id="d903d-116">With this change, the **HcmPositionWorkerAssignmentV2Entity** is included in the Ceridian payroll integration package.</span></span>

## <a name="in-preview"></a><span data-ttu-id="d903d-117">Í kynningarútgáfu</span><span class="sxs-lookup"><span data-stu-id="d903d-117">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="d903d-118">Gagnagrunnsskráning</span><span class="sxs-lookup"><span data-stu-id="d903d-118">Database logging</span></span>

<span data-ttu-id="d903d-119">Eiginleiki gagnagrunnskladda gerir notendum kleift að ákvarða hvaða töflum og reitum á að fylgjast með.</span><span class="sxs-lookup"><span data-stu-id="d903d-119">The database logging feature allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="d903d-120">Hann gerir einnig kleift að ákvarða tilvikin sem eiga að kveikja á breytingarakningu.</span><span class="sxs-lookup"><span data-stu-id="d903d-120">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="d903d-121">Notið möguleika gagnagrunnsskráningar til að sjá þessar breytingar yfir tíma.</span><span class="sxs-lookup"><span data-stu-id="d903d-121">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="d903d-122">Frekari upplýsingar er að finna í [Skilgreina og stjórna gagnagrunnsskráningu](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="d903d-122">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="d903d-123">Forrit „Human Resources“ í Teams</span><span class="sxs-lookup"><span data-stu-id="d903d-123">Human Resources application in Teams</span></span>

<span data-ttu-id="d903d-124">Starfsmenn geta skoðað og beðið um tíma frá vinnu innan Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="d903d-124">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="d903d-125">Hægt er að hafa umsjón með þjark til að búa til beiðnir um leyfi.</span><span class="sxs-lookup"><span data-stu-id="d903d-125">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="d903d-126">Frekari upplýsingar er að finna í [Forrit Human Resources í Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="d903d-126">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="d903d-127">Einingar gagnastjórnunarramma (DMF) fyrir fríðindastjórnun</span><span class="sxs-lookup"><span data-stu-id="d903d-127">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="d903d-128">Einingar fríðindastjórnunar eru að gefa út.</span><span class="sxs-lookup"><span data-stu-id="d903d-128">Benefits management entities are releasing.</span></span> <span data-ttu-id="d903d-129">DMF-einingar leyfa innflutning og útflutning gagna til að skilgreina fríðindastjórnun á auðveldan hátt.</span><span class="sxs-lookup"><span data-stu-id="d903d-129">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="d903d-130">Sniðmát fríðindastjórnunar verður í boði til að flytja gögn.</span><span class="sxs-lookup"><span data-stu-id="d903d-130">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="d903d-131">Sniðmátið flytur út og flytur inn gögnin í ákveðinni röð til að virða gagnatengsl.</span><span class="sxs-lookup"><span data-stu-id="d903d-131">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="d903d-132">Kaupa og selja leyfisdaga</span><span class="sxs-lookup"><span data-stu-id="d903d-132">Buy and sell leave</span></span> 

<span data-ttu-id="d903d-133">Sum fyrirtæki bjóða upp á fríðindi sem gera starfsmönnum kleift að kaupa eða selja leyfisdaga.</span><span class="sxs-lookup"><span data-stu-id="d903d-133">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="d903d-134">Þessu ferli er oft stjórnað handvirkt.</span><span class="sxs-lookup"><span data-stu-id="d903d-134">This process is often managed manually.</span></span> <span data-ttu-id="d903d-135">Þessi eiginleiki gerir umsjón með stefnum og beiðnum sjálfvirka fyrir mannauðsdeildina.</span><span class="sxs-lookup"><span data-stu-id="d903d-135">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="d903d-136">Hann einfaldar ferli leyfisstjórnunar og hjálpar til við að koma í veg fyrir mistök.</span><span class="sxs-lookup"><span data-stu-id="d903d-136">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="d903d-137">Frekari upplýsingar má finna á</span><span class="sxs-lookup"><span data-stu-id="d903d-137">For more information, see:</span></span>

- [<span data-ttu-id="d903d-138">Stjórna reglum fyrir kaup og sölu á leyfisdögum</span><span class="sxs-lookup"><span data-stu-id="d903d-138">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="d903d-139">Kaupa og selja leyfisdaga</span><span class="sxs-lookup"><span data-stu-id="d903d-139">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="d903d-140">Uppsafnað leyfi fyrir eitt fyrirtæki eða eina áætlun</span><span class="sxs-lookup"><span data-stu-id="d903d-140">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="d903d-141">Viðskiptavinir geta unnið úr uppsöfnunum fyrir eitt fyrirtæki eða eina áætlun leyfis og fjarveru.</span><span class="sxs-lookup"><span data-stu-id="d903d-141">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="d903d-142">Þessi möguleiki varpar betra ljósi á uppsöfnunarferlið yfir viðskiptavini með mismunandi reglur fyrir leyfisár eða leyfisuppsöfnun.</span><span class="sxs-lookup"><span data-stu-id="d903d-142">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="d903d-143">Frekari upplýsingar er að finna í [Uppsafnað leyfi á fyrirtæki eða leyfisáætlun](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="d903d-143">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="d903d-144">Bæta viðhengjum við fríbeiðnir</span><span class="sxs-lookup"><span data-stu-id="d903d-144">Add attachments to time off requests</span></span>

<span data-ttu-id="d903d-145">Möguleikinn á því að bæta viðhengjum við samþykktar leyfisbeiðnir er mikilvægur á þessum COVID 19-tímum.</span><span class="sxs-lookup"><span data-stu-id="d903d-145">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="d903d-146">Starfsmenn geta nú bætt við þessum viðhengjum.</span><span class="sxs-lookup"><span data-stu-id="d903d-146">Employees can now add these attachments.</span></span> <span data-ttu-id="d903d-147">Þeir hafa einnig meiri innsýn í hvernig uppfærslur á leyfisbeiðnum eru gerðar.</span><span class="sxs-lookup"><span data-stu-id="d903d-147">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="d903d-148">Frekari upplýsingar er að finna í [Bæta viðhengi við fyrirliggjandi beiðni](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="d903d-148">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="d903d-149">Bæta ástæðukóða við frestun uppsöfnunar</span><span class="sxs-lookup"><span data-stu-id="d903d-149">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="d903d-150">Ástæðukóðum hefur verið bætt við uppsöfnun í bið.</span><span class="sxs-lookup"><span data-stu-id="d903d-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="d903d-151">Yfirfærslureglur</span><span class="sxs-lookup"><span data-stu-id="d903d-151">Carry forward rules</span></span> 

<span data-ttu-id="d903d-152">Hægt er að tilgreina yfirfærsluorlofsgerð fyrir yfirfærslustöður þar sem yfirfærsluleiðréttingar eru fluttar.</span><span class="sxs-lookup"><span data-stu-id="d903d-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="d903d-153">Til dæmis, ef starfsmaður yfirfærir 10 daga getur þú valið aðra leyfisgerð fyrir þessa 10 daga.</span><span class="sxs-lookup"><span data-stu-id="d903d-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="d903d-154">Fyrir frekari upplýsingar, sjá [Grunnstilla gerðir leyfis og fjarvista](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="d903d-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="d903d-155">Uppsafnað leyfi í bið fyrir tilteknar leyfisgerðir</span><span class="sxs-lookup"><span data-stu-id="d903d-155">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="d903d-156">Hægt er að búa til reglu til að fresta uppsöfnun leyfis fyrir starfsmenn með beiðnum um leyfi sem færðar eru inn fyrir ógreitt leyfi.</span><span class="sxs-lookup"><span data-stu-id="d903d-156">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="d903d-157">Ógreit leyfi getur verið gerð, en þarf ekki að vera það.</span><span class="sxs-lookup"><span data-stu-id="d903d-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="d903d-158">Hægt er að fresta öllu leyfi út frá gerð annarrar leyfisgerðar.</span><span class="sxs-lookup"><span data-stu-id="d903d-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="d903d-159">DMF-eining er í boði fyrir frestun uppsöfnunar</span><span class="sxs-lookup"><span data-stu-id="d903d-159">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="d903d-160">DMF-eining er ekki til staðar fyrir uppsöfnun í bið.</span><span class="sxs-lookup"><span data-stu-id="d903d-160">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="d903d-161">Væntanlegt</span><span class="sxs-lookup"><span data-stu-id="d903d-161">Coming soon</span></span>

## <a name="new-platform-capabilities"></a><span data-ttu-id="d903d-162">Nýir verkvangsmöguleikar</span><span class="sxs-lookup"><span data-stu-id="d903d-162">New platform capabilities</span></span> 

<span data-ttu-id="d903d-163">Hægt verður að gera reiti áskilda með því að nota sérstillingu.</span><span class="sxs-lookup"><span data-stu-id="d903d-163">You'll be able to make fields mandatory by using personalization.</span></span> <span data-ttu-id="d903d-164">Þessi eiginleiki gerir þér kleift að virkja **Vistuð yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="d903d-164">This feature will require you to enable **Saved views**.</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="d903d-165">Stilla heiti á sjálfsafgreiðslu starfsmanns</span><span class="sxs-lookup"><span data-stu-id="d903d-165">Configure the name of Employee self-service</span></span>

<span data-ttu-id="d903d-166">Nýr valkostur verður í boði í færibreytum mannauðs til að uppfæra heiti á vinnusvæði fyrir sjálfsafgreiðslu starfsmanns í Sjálfsafgreiðsla.</span><span class="sxs-lookup"><span data-stu-id="d903d-166">A new option will be available in Human Resources parameters to update the name of the Employee self service workspace to Self service.</span></span> 

## <a name="see-also"></a><span data-ttu-id="d903d-167">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d903d-167">See also</span></span>

[<span data-ttu-id="d903d-168">Nýjungar í Human Resources</span><span class="sxs-lookup"><span data-stu-id="d903d-168">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="d903d-169">Yfirlit yfir Dynamics 365 Human Resources Losunarbylgja 2019</span><span class="sxs-lookup"><span data-stu-id="d903d-169">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="d903d-170">Uppfærsluferli</span><span class="sxs-lookup"><span data-stu-id="d903d-170">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="d903d-171">Vinna með eiginleika</span><span class="sxs-lookup"><span data-stu-id="d903d-171">Manage features</span></span>](hr-admin-manage-features.md)