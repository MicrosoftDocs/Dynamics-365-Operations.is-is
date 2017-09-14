---
title: "Uppsetning íhluta starfs"
description: "Þetta efnisatriði lýsir þeim hugtakaþáttum sem vinnsla getur haft með og gefur dæmi um hvernig hægt er að nota þessa þætti í fyrirtækinu."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.author: rschloma
ms.reviewer: rschloma
ms.search.scope: Core, Operations, UnifiedOperations, Retail
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: a5fa86bace459d694ab0a2ec289e11b0e4420932
ms.openlocfilehash: c616637922e617661482875d78531ea79fda4407
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---

# <a name="setting-up-the-components-of-a-job"></a><span data-ttu-id="174e2-103">Uppsetning íhluta starfs</span><span class="sxs-lookup"><span data-stu-id="174e2-103">Setting up the components of a job</span></span>

[!include[banner](includes/banner.md)]

[!include[retail name](includes/retail-name.md)]


<span data-ttu-id="174e2-104">Þetta efnisatriði lýsir þeim hugtakaþáttum sem vinnsla getur haft með og gefur dæmi um hvernig hægt er að nota þessa þætti í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="174e2-104">This topic describes the conceptual elements that a job can include and provides examples of how you can use those elements in your organization.</span></span> 

<span data-ttu-id="174e2-105">Áður en hægt er að stofna vinnslur verður þú að setja upp tilvísunarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="174e2-105">Before you can create jobs, you must set up some reference information.</span></span> <span data-ttu-id="174e2-106">Hægt er að stofna vinnslu sem hefur aðeins heiti.</span><span class="sxs-lookup"><span data-stu-id="174e2-106">You can create a job that has only a name.</span></span> <span data-ttu-id="174e2-107">Hins vegar með því að hafa frekari upplýsingar með, t.d. titil vinnslu, veitirðu sjálfgildi fyrir þær stöður sem er úthlutað til vinnslu.</span><span class="sxs-lookup"><span data-stu-id="174e2-107">However, by including additional information, such as a job title, you provide default values for the positions that are assigned to the job.</span></span> <span data-ttu-id="174e2-108">Þar að auki er hægt að nota sumar þeirra upplýsinga sem voru færðar inn til að afmarka launafyrirkomulag við tilgreindar vinnslur.</span><span class="sxs-lookup"><span data-stu-id="174e2-108">Additionally, some of the information that you enter can be used to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="174e2-109">Ef ætlunin er að setja upp hæfni sem hægt er nota til að afmarka launafyrirkomulag við tilgreindar vinnslur ætti að setja upp starfshlutverk og vinnslugerð áður en vinnslur eru setter upp.</span><span class="sxs-lookup"><span data-stu-id="174e2-109">If you want to set up eligibility that you can use to filter compensation plans to a specific job, you should set up job functions and job types before you set up jobs.</span></span> <span data-ttu-id="174e2-110">Með því að hafa þessi sjálfgildi tiltæk spararðu tíma þegar stöðum er bætt við starfið.</span><span class="sxs-lookup"><span data-stu-id="174e2-110">By having these default values available, you will save time when you add positions to the job.</span></span> 

<span data-ttu-id="174e2-111">Sumar starfsupplýsingar, eins og starfsheiti, gerð og aðgerð, eru dagsetningarvirkar.</span><span class="sxs-lookup"><span data-stu-id="174e2-111">Some job details, such as the job title, type, and function, are date-effective.</span></span> <span data-ttu-id="174e2-112">Ef þú stofnar starf í dag en bætir þessum upplýsingum ekki við fyrr en seinna og skoðar síðan starfið frá og með stofndagsetningu munu þessar upplýsingar ekki birtast.</span><span class="sxs-lookup"><span data-stu-id="174e2-112">If you create a job today but don't add these details until later, and you then look at the job as of the creation date, these details won't appear.</span></span> <span data-ttu-id="174e2-113">Þess vegna ættirðu að stofna sumar þessara tilvísunarupplýsinga áður en þú þarft að nota þær.</span><span class="sxs-lookup"><span data-stu-id="174e2-113">Therefore, you should create some of this reference information before you require it.</span></span> <span data-ttu-id="174e2-114">Á þann hátt er hægt að bæta við upplýsingum í ný störf þegar þau eru stofnuð.</span><span class="sxs-lookup"><span data-stu-id="174e2-114">That way, you can add the information to new jobs when you create them.</span></span>

## <a name="job-titles"></a><span data-ttu-id="174e2-115">Starfsheiti</span><span class="sxs-lookup"><span data-stu-id="174e2-115">Job titles</span></span>
<span data-ttu-id="174e2-116">Áður en hægt er að stofna vinnslur verður að setja upp titla fyrir þær vinnslur.</span><span class="sxs-lookup"><span data-stu-id="174e2-116">Before you create jobs, you must set up titles for those jobs.</span></span> <span data-ttu-id="174e2-117">Stöður erfa starfsheiti úr vinnslum sem þær eru tengdar við.</span><span class="sxs-lookup"><span data-stu-id="174e2-117">Positions inherit job titles from the jobs that the positions are associated with.</span></span> 

<span data-ttu-id="174e2-118">Viðhalda starfsheitum með því að nota síðuna **Titlar** sem þú getur opnað með því að nota leitaraðgerð.</span><span class="sxs-lookup"><span data-stu-id="174e2-118">Maintain job titles using the **Titles** page, which you can open by using the Search function.</span></span> <span data-ttu-id="174e2-119">Á **síðunni **Titlar skal færa inn þá titla sem þú ætlar að nota fyrir störfin.</span><span class="sxs-lookup"><span data-stu-id="174e2-119">On the **Titles **page, enter the titles that you plan to use for your jobs.</span></span>

## <a name="job-types"></a><span data-ttu-id="174e2-120">Vinnslugerðir</span><span class="sxs-lookup"><span data-stu-id="174e2-120">Job types</span></span>
<span data-ttu-id="174e2-121">Þú notar vinnslugerð til að flokka svipuð störf í flokka.</span><span class="sxs-lookup"><span data-stu-id="174e2-121">You use job types to group similar jobs into categories.</span></span> <span data-ttu-id="174e2-122">Starfstegundir eru ekki áskildar.</span><span class="sxs-lookup"><span data-stu-id="174e2-122">Job types aren't required.</span></span> <span data-ttu-id="174e2-123">Hins vegar ef ætlunin er að nota vinnslugerðir þegar setja á upp hæfnireglur fyrir greiðsluáætlunarstjórnun ætti að setja upp vinnslugerðir áður en hægt er að setja upp störf.</span><span class="sxs-lookup"><span data-stu-id="174e2-123">However, if you plan to use job types when you set up eligibility rules for compensation management, you should set up job types before you set up jobs.</span></span> <span data-ttu-id="174e2-124">Sum dæmi um starfstegundir eru Fullt starf og Hlutastarf, eða Laun og Tímakaup.</span><span class="sxs-lookup"><span data-stu-id="174e2-124">Some examples of job types are full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="174e2-125">Starfstegundum er viðhaldið með því að nota síðuna **Vinnslugerð**.</span><span class="sxs-lookup"><span data-stu-id="174e2-125">You maintain job types by using the **Job types** page.</span></span> <span data-ttu-id="174e2-126">Á síðunni **Starfsgerðir** skal færa inn heiti og lýsingu á starfsgerðinni.</span><span class="sxs-lookup"><span data-stu-id="174e2-126">On the **Job types** page, enter a name and a brief description for the job type.</span></span> <span data-ttu-id="174e2-127">Í reitnum **Staða undanþágu** velurðu einn af eftirfarandi valkostum til að tilgreina þá stöðu undanþágu Fair Labor Standards Act (FLSA) starfa sem hafa þessa starfsgerð:</span><span class="sxs-lookup"><span data-stu-id="174e2-127">In the **Exempt status** field, select one of the following options to indicate the Fair Labor Standards Act (FLSA) exempt status of jobs that have this job type:</span></span>

-   <span data-ttu-id="174e2-128">**Undanþága** – Störf eru undanþegin yfirvinnu undir FLSA.</span><span class="sxs-lookup"><span data-stu-id="174e2-128">**Exempt** – Jobs are exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="174e2-129">**Ekki undanþága** – Störf eru ekki undanþegin yfirvinnu undir FLSA.</span><span class="sxs-lookup"><span data-stu-id="174e2-129">**Non-exempt** – Jobs aren't exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="174e2-130">**Á ekki við** – FLSA á ekki við.</span><span class="sxs-lookup"><span data-stu-id="174e2-130">**Does not apply** – FLSA coverage isn't applicable.</span></span>

## <a name="job-functions"></a><span data-ttu-id="174e2-131">Starfshlutverk</span><span class="sxs-lookup"><span data-stu-id="174e2-131">Job functions</span></span>
<span data-ttu-id="174e2-132">Starfshlutverk lýsa hástigs virkt flokkar og tengdum hástigs skyldur.</span><span class="sxs-lookup"><span data-stu-id="174e2-132">Job junctions describe high-level functional categories and relate high-level duties.</span></span> <span data-ttu-id="174e2-133">Starfshlutverk eru ekki áskilin.</span><span class="sxs-lookup"><span data-stu-id="174e2-133">Job functions aren't required.</span></span> <span data-ttu-id="174e2-134">Þú getur notað starfshlutverk ásamt vinnslugerð til að afmarka launafyrirkomulag við tilteknar vinnslur.</span><span class="sxs-lookup"><span data-stu-id="174e2-134">You can use job functions, together with job types, to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="174e2-135">Þú tengir starfshlutverk og vinnslugerð við launafyrirkomulag með því að setja upp hæfnisreglur á síðunni **Hæfnisreglur**.</span><span class="sxs-lookup"><span data-stu-id="174e2-135">You associate job functions and job types with compensation plans by setting up eligibility rules on the **Eligibility rules** page.</span></span> <span data-ttu-id="174e2-136">Síðan er hægt að festa hóp stiga við launafyrirkomulag sem eiga við um tilgreinda samsetningu vinnslugerðar og starfshlutverka sem þú hefur skilgreint til og með hæfniregla.</span><span class="sxs-lookup"><span data-stu-id="174e2-136">You can then attach a set of levels to a compensation plan that apply to the specific combination of a job type and job function that you've defined through an eligibility rule.</span></span> <span data-ttu-id="174e2-137">(Þessir eiginleikar eiga við um bæði launafyrirkomulagi fastra launa og breytileg uppbót áætlun.) Hins vegar ef þú ætlar að nota starfshlutverk þegar hæfnisreglur eru settar upp fyrir launafyrirkomulag þarf að setja upp starfshlutverk áður en þú setur upp störf.</span><span class="sxs-lookup"><span data-stu-id="174e2-137">(These features apply to both fixed compensation plans and variable compensation plans.) However, if you plan to use job functions when you set up eligibility rules for compensation management, you should set up job functions before you set up jobs.</span></span> <span data-ttu-id="174e2-138">Eftirfarandi tafla sýnir dæmi um starfshlutverk.</span><span class="sxs-lookup"><span data-stu-id="174e2-138">The following table shows some examples of job functions.</span></span>

| <span data-ttu-id="174e2-139">Starf</span><span class="sxs-lookup"><span data-stu-id="174e2-139">Job</span></span>           | <span data-ttu-id="174e2-140">Starfshlutverk</span><span class="sxs-lookup"><span data-stu-id="174e2-140">Job function</span></span>         |
|---------------|----------------------|
| <span data-ttu-id="174e2-141">Sölustjóri</span><span class="sxs-lookup"><span data-stu-id="174e2-141">Sales manager</span></span> | <span data-ttu-id="174e2-142">Stjórnandi á miðsstigi</span><span class="sxs-lookup"><span data-stu-id="174e2-142">Mid-level Manager</span></span>    |
| <span data-ttu-id="174e2-143">Bókhaldari</span><span class="sxs-lookup"><span data-stu-id="174e2-143">Accountant</span></span>    | <span data-ttu-id="174e2-144">Sérfræðingar</span><span class="sxs-lookup"><span data-stu-id="174e2-144">Professionals</span></span>        |

<span data-ttu-id="174e2-145">Starfstegundum er viðhaldið með því að nota síðuna **Starfshlutverk**.</span><span class="sxs-lookup"><span data-stu-id="174e2-145">You maintain job functions by using the **Job functions** page.</span></span> <span data-ttu-id="174e2-146">Á síðunni **Starfshlutverk** skal færa inn staðfestingarkóða og stutta lýsingu á starfshlutverk.</span><span class="sxs-lookup"><span data-stu-id="174e2-146">On the **Job functions** page, enter an identification code and a brief description for the job function.</span></span>

## <a name="job-tasks"></a><span data-ttu-id="174e2-147">Verkefni starfs</span><span class="sxs-lookup"><span data-stu-id="174e2-147">Job tasks</span></span>
<span data-ttu-id="174e2-148">Verkhlutar sem lýsa grunnatriðum verkefnis sem starfskraftur sem er í stöðu fyrir vinnsla verður að ljúka.</span><span class="sxs-lookup"><span data-stu-id="174e2-148">Job tasks describe the basic tasks that a worker who is in a position for a job must complete.</span></span> <span data-ttu-id="174e2-149">Sama verkefni starfs er hægt að bæta við mörg störf og í stöður fyrir þau störf sem nota þau verkefni.</span><span class="sxs-lookup"><span data-stu-id="174e2-149">The same job task can be added to multiple jobs, and to positions for the jobs that use those job tasks.</span></span> <span data-ttu-id="174e2-150">Eftirfarandi tafla sýnir dæmi um verkefni starfs.</span><span class="sxs-lookup"><span data-stu-id="174e2-150">The following table shows some examples of job tasks.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="174e2-151">Starf</span><span class="sxs-lookup"><span data-stu-id="174e2-151">Job</span></span></th>
<th><span data-ttu-id="174e2-152">Verkefni starfs</span><span class="sxs-lookup"><span data-stu-id="174e2-152">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="174e2-153">Sölustjóri</span><span class="sxs-lookup"><span data-stu-id="174e2-153">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="174e2-154"><strong>Perf yfirferð</strong> – fara Yfir afköst hverja sölumanns.</span><span class="sxs-lookup"><span data-stu-id="174e2-154"><strong>Perf-review</strong> – Review each salesperson's job performance.</span></span></li>
<li><span data-ttu-id="174e2-155"><strong>Abs yfirferð</strong> – Samþykkja eða hafna fjarvistabeiðnir hvers sölumanns eða skráningar.</span><span class="sxs-lookup"><span data-stu-id="174e2-155"><strong>Abs-review</strong> – Approve or reject each salesperson's absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="174e2-156">Bókhaldari</span><span class="sxs-lookup"><span data-stu-id="174e2-156">Accountant</span></span></td>
<td><span data-ttu-id="174e2-157"><strong>FIN Skýrslu</strong> – Birta vikulegt fjárhagsskýrslur til fjármálastjórnanda.</span><span class="sxs-lookup"><span data-stu-id="174e2-157"><strong>FIN-Report</strong> – Present weekly financial reports to the chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="174e2-158">Verkefnum starfs er viðhaldið með því að nota síðuna **Verkefni starfs**.</span><span class="sxs-lookup"><span data-stu-id="174e2-158">You maintain job tasks by using the **Job tasks** page.</span></span> <span data-ttu-id="174e2-159">Á síðunni **Verkefni starfs** skal færa inn heiti og lýsingu á verkefni starfs.</span><span class="sxs-lookup"><span data-stu-id="174e2-159">On the **Job tasks** page, enter a name and description for the job task.</span></span> <span data-ttu-id="174e2-160">Í svæðinu **athugasemd** er valfrjálst hægt að færa inn viðbótarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="174e2-160">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="174e2-161">Hægt er að uppfæra athugasemdirnar fyrir tilgreint starf án þess að breyta athugasemdunum sem voru færðar inn hérna.</span><span class="sxs-lookup"><span data-stu-id="174e2-161">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>

## <a name="areas-of-responsibility"></a><span data-ttu-id="174e2-162">Ábyrgðarsvið</span><span class="sxs-lookup"><span data-stu-id="174e2-162">Areas of responsibility</span></span>
<span data-ttu-id="174e2-163">Þú notar Ábyrgðarsvið til að gefa til kynna starfshlutverk, ferli, afurðir og aðgerðir sem starfsmaður sem er í stöðu er ábyrgur fyrir í vinnslu.</span><span class="sxs-lookup"><span data-stu-id="174e2-163">You use areas of responsibility to indicate the work roles, processes, and products that a worker who is in a position for a job is responsible for.</span></span> <span data-ttu-id="174e2-164">Til dæmis fyrir starf sem heitir "Bókari" gæti eitt svæði ábyrgðar verið "Fjárhagsleg skýrslugerð fyrir Afurð A".</span><span class="sxs-lookup"><span data-stu-id="174e2-164">For example, for a job that is named "Accountant," one area of responsibility might be "Financial reporting for product A."</span></span> <span data-ttu-id="174e2-165">Ábyrgðarsviði er viðhaldið með því að nota síðuna **Ábyrgðarsvið** sem þú getur opnað með því að nota leitaraðgerð.</span><span class="sxs-lookup"><span data-stu-id="174e2-165">You maintain areas of responsibility by using the **Areas of responsibility** page, which you can find by using the Search function.</span></span> <span data-ttu-id="174e2-166">Á síðunni **Ábyrgðarsvið** skal færa inn heiti og lýsingu á ábyrgðinni.</span><span class="sxs-lookup"><span data-stu-id="174e2-166">On the **Areas of responsibility** page, enter a name and description for the responsibility.</span></span> <span data-ttu-id="174e2-167">Í svæðinu **athugasemd** er valfrjálst hægt að færa inn viðbótarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="174e2-167">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="174e2-168">Hægt er að uppfæra athugasemdirnar fyrir tilgreint starf án þess að breyta athugasemdunum sem voru færðar inn hérna.</span><span class="sxs-lookup"><span data-stu-id="174e2-168">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>




