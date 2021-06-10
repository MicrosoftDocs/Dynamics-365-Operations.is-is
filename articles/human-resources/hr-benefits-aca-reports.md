---
title: Mynda skýrslur fyrir Affordable Care Act (ACA)
description: Skýrslugerð Affordable Care Act býr til eyðublöð 1095-B og 1095-C til stuðnings þeim hluta af Affordable Care Act sem snýr að **umboði vinnuveitanda**.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 1091460ee1996b944b760f3771007bd2a26666a9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053202"
---
# <a name="generate-aca-reports"></a><span data-ttu-id="d8cba-103">Mynda ACA-skýrslur</span><span class="sxs-lookup"><span data-stu-id="d8cba-103">Generate ACA reports</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d8cba-104">Skýrslugerð Affordable Care Act býr til eyðublöð 1095-B og 1095-C til stuðnings þeim hluta af Affordable Care Act sem snýr að **umboði vinnuveitanda**.</span><span class="sxs-lookup"><span data-stu-id="d8cba-104">Affordable Care Act (ACA) reporting generates forms 1095-B and 1095-C in support of the **Employer Mandate** portion of the Affordable Care Act.</span></span>

> [!NOTE]
> <span data-ttu-id="d8cba-105">ACA-skýrslugerð er aðeins virkjuð fyrir lögaðila í Bandaríkjunum.</span><span class="sxs-lookup"><span data-stu-id="d8cba-105">ACA reporting is only enabled for legal entities in the United States.</span></span>

## <a name="getting-started"></a><span data-ttu-id="d8cba-106">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="d8cba-106">Getting started</span></span>

<span data-ttu-id="d8cba-107">Til að rekja upplýsingar fyrir eyðublöð 1095-B og 1095-C skal fyrst stofna einn eða fleiri Affordable Care-tryggingaflokka.</span><span class="sxs-lookup"><span data-stu-id="d8cba-107">To track information for forms 1095-B and 1095-C, you must first create one or more Affordable care coverage groups.</span></span> <span data-ttu-id="d8cba-108">Affordable Care-tryggingaflokkar tilgreina:</span><span class="sxs-lookup"><span data-stu-id="d8cba-108">Affordable Care coverage groups indicate:</span></span>

- <span data-ttu-id="d8cba-109">Tryggingatilboð handa starfsmanni</span><span class="sxs-lookup"><span data-stu-id="d8cba-109">The offer of coverage for an employee</span></span>
- <span data-ttu-id="d8cba-110">Hlutdeild starfsmanns í lægstu mánaðarlegu greiðslu iðgjalds, ef kostnaðurinn er fyrir ofan fátæktarmörk</span><span class="sxs-lookup"><span data-stu-id="d8cba-110">The employee’s share of the lowest cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="d8cba-111">Örugg höfn sem er notuð af starfsmanni, ef á við</span><span class="sxs-lookup"><span data-stu-id="d8cba-111">Safe Harbor used by the employer, if applicable</span></span>

<span data-ttu-id="d8cba-112">Affordable Care-tryggingaflokkar gera þér kleift að hafa umsjón með þessum reitum án þess að breyta öllum starfsmannafærslum þar sem skilyrðin eru þau sömu.</span><span class="sxs-lookup"><span data-stu-id="d8cba-112">Affordable Care coverage groups allow you to manage the information for these fields without changing every employee record where the conditions are the same.</span></span> <span data-ttu-id="d8cba-113">Það er auðveldlega hægt að úthluta Affordable Care-tryggingaflokkum á einn eða fleiri starfsmenn með valkostinum **Fjöldaúthluta** á síðunni.</span><span class="sxs-lookup"><span data-stu-id="d8cba-113">You can easily assign Affordable Care coverage groups to one or more employees by using the **Mass assign** option on the page.</span></span>

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a><span data-ttu-id="d8cba-114">Umsjón með mörgum útgáfum tryggingahóps</span><span class="sxs-lookup"><span data-stu-id="d8cba-114">Maintaining multiple versions of a coverage group</span></span>

<span data-ttu-id="d8cba-115">Hægt er að viðhalda mörgum útgáfum í hvaða tryggingaflokki sem er.</span><span class="sxs-lookup"><span data-stu-id="d8cba-115">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="d8cba-116">Þessi virkni gerir þér kleift að gera breytingar án þess að þurfa að búa til nýjan flokk og endurúthluta starfsmönnum í hann.</span><span class="sxs-lookup"><span data-stu-id="d8cba-116">This functionality allows you to make changes without having to create a new group and reassign employees to it.</span></span> 

<span data-ttu-id="d8cba-117">Þegar búið er að stofna ACA-tryggingaflokka er hægt að fjöldaúthluta flokkunum á starfsmenn með valkostinum **Fjöldaúthlutun**.</span><span class="sxs-lookup"><span data-stu-id="d8cba-117">After you’ve created ACA coverage groups, you can mass assign the groups to employees with the **Mass assignment** option.</span></span> <span data-ttu-id="d8cba-118">Einnig er hægt að gefa til kynna í hverju tilfelli fyrir sig hvort eigi að rekja og tilkynna ACA-upplýsingar og úthluta starfsmanni á Affordable Care-tryggingaflokk.</span><span class="sxs-lookup"><span data-stu-id="d8cba-118">You can also individually indicate whether to track and report ACA information, and assign an employee to an Affordable Care coverage group.</span></span>

<span data-ttu-id="d8cba-119">Ekki þarf að rekja sumar ACA-tryggingaupplýsingar eins og fyrir starfsmenn í hlutastarfi.</span><span class="sxs-lookup"><span data-stu-id="d8cba-119">You don't need to track some ACA coverage information, such as for part-time employees.</span></span> <span data-ttu-id="d8cba-120">Í þessu tilfelli skal stilla reitinn **Telja tryggingu fram** á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="d8cba-120">In this case, set the **Report coverage** field to **No**.</span></span> <span data-ttu-id="d8cba-121">Þótt þurfi að úthluta hverjum starfsmanni rekjanlegar ACA-upplýsingar í Affordable Care-tryggingaflokk, er enn hægt að breyta eftirfarandi valkostum fyrir mánuði með ólíkum gildum:</span><span class="sxs-lookup"><span data-stu-id="d8cba-121">Although you must assign each employee with trackable ACA information to an Affordable Care coverage group, you can still change the following options for months with different values:</span></span>

- <span data-ttu-id="d8cba-122">**Tryggingatilboð**</span><span class="sxs-lookup"><span data-stu-id="d8cba-122">**Offer of coverage**</span></span>
- <span data-ttu-id="d8cba-123">**Kostnaðarhlutdeild starfsmanns**</span><span class="sxs-lookup"><span data-stu-id="d8cba-123">**Employee share of cost**</span></span>
- <span data-ttu-id="d8cba-124">**Örugg höfn**</span><span class="sxs-lookup"><span data-stu-id="d8cba-124">**Safe Harbor**</span></span>

<span data-ttu-id="d8cba-125">Til að færa inn undantekningar fyrir gildi Affordable Care-tryggingaflokks skal velja tengilinn **Affordable Care-trygging** á síðunni **Upplýsingar um starfsmann** undir hlutanum **Frekari upplýsingar** í flipanum **Starf**.</span><span class="sxs-lookup"><span data-stu-id="d8cba-125">To enter exceptions for Affordable Care coverage group values, select the **Affordable Care Coverage** link on the **Worker detail** page under the **Additional information** section on the **Employment tab**.</span></span>

## <a name="reporting-health-care-coverage"></a><span data-ttu-id="d8cba-126">Skráning sjúkratrygginga</span><span class="sxs-lookup"><span data-stu-id="d8cba-126">Reporting health care coverage</span></span>

<span data-ttu-id="d8cba-127">Auk þess að rekja sjúkratryggingu sem boðin er starfsmönnum í fullu starfi, ef vinnuveitandi býður upp á sjálfstryggða sjúkratryggingu kostaða af vinnuveitanda þar sem starfsmaðurinn er skráður (burtséð frá því hvort þeir eru í fullu starfi eða hlutastarfi), þarf að tilkynna frekari upplýsingar á 1095-C.</span><span class="sxs-lookup"><span data-stu-id="d8cba-127">In addition to tracking health insurance coverage offered to full-time employees, if the employer offers employer-sponsored self-insured health coverage for which the employee is enrolled (regardless of whether their employment status is full-time or part-time), additional information needs to be reported on the 1095-C.</span></span> <span data-ttu-id="d8cba-128">Hver starfsmaður (þ.m.t. skjólstæðingar) sem tryggður er af tryggingum vinnuveitanda verður að vera skráður í skýrslunni fyrir þá mánuði sem hann var tryggður.</span><span class="sxs-lookup"><span data-stu-id="d8cba-128">Each employee (including dependents) covered by the employer-sponsored benefit plans needs to be included on the report for the months they were covered.</span></span> 

<span data-ttu-id="d8cba-129">Hægt er að gefa til kynna hvort tilkynna þurfi hverja fríðindaáætlun fyrir sig með því að velja gátreitinn **ACA-tilkynningaskylt**.</span><span class="sxs-lookup"><span data-stu-id="d8cba-129">You can indicate whether or not each benefit plan must be reported by selecting the **ACA reportable** check box.</span></span>

<span data-ttu-id="d8cba-130">Að auki ef starfsmenn hafa valið að einhverjir skjólstæðinga þeirra verði tryggðir undir fríðindum, er hægt að gefa upp dagsetningarnar sem skjólstæðingurinn var tryggður fyrir hvern starfsmann á síðunni **Viðhalda fríðindum**.</span><span class="sxs-lookup"><span data-stu-id="d8cba-130">In addition, if employees have chosen to have any of their dependents covered under a benefit, you can indicate the dates the dependent was covered for each employee on the **Maintain benefits** page.</span></span> <span data-ttu-id="d8cba-131">Til að gefa til kynna að skjólstæðingurinn sé tryggðir undir fríðindum skal velja hnappinn **Breyta** á aðgerðasvæði flýtiflipans **Skjólstæðingar**.</span><span class="sxs-lookup"><span data-stu-id="d8cba-131">To indicate that the dependent is covered under the benefit, select the **Edit** button in the action pane of the **Dependents** fast tab.</span></span>

<span data-ttu-id="d8cba-132">Á síðunni **Tímabilsstjórnun fyrir tryggingar skjólstæðinga** er hægt að tilgreina dagsetningar sem skjólstæðingar voru tryggðir samkvæmt fríðindum.</span><span class="sxs-lookup"><span data-stu-id="d8cba-132">On the **Dependent coverage date manager** page, you can indicate the dates the dependent was covered by the benefit.</span></span> <span data-ttu-id="d8cba-133">Skráning dagsetninga á þessari síðu mun sjálfkrafa velja gátreitinn **Tryggður** á síðunni **Viðhalda fríðindum**.</span><span class="sxs-lookup"><span data-stu-id="d8cba-133">Entering dates on this page will automatically select the **Covered** checkbox on the **Maintain benefits** page.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="d8cba-134">Búa til eyðublöð 1095-B og 1095-C</span><span class="sxs-lookup"><span data-stu-id="d8cba-134">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="d8cba-135">Einnig er hægt að búa til eyðublöðin 1095-B og 1095-C innan afurðar og dreifa þeim til allra starfsmanna þinna.</span><span class="sxs-lookup"><span data-stu-id="d8cba-135">You can also generate 1095-B and 1095-C forms from within the product, and distribute them to each of your employees.</span></span> <span data-ttu-id="d8cba-136">Kerfið getur einnig rafrænt búið til 1095-C eyðublöð og 1094-C skilaskrár til skattyfirvalda Bandaríkjanna.</span><span class="sxs-lookup"><span data-stu-id="d8cba-136">The system can also electronically generate 1095-C forms and the 1094-C IRS transmittal files.</span></span>  

<span data-ttu-id="d8cba-137">Þegar eyðublað 1095-C er búið til skal færa inn viðeigandi skattaár og tilgreina ef hylja á kennitölur.</span><span class="sxs-lookup"><span data-stu-id="d8cba-137">When generating the 1095-C form, enter the appropriate tax year and indicate if social security numbers should be masked.</span></span> <span data-ttu-id="d8cba-138">Ef eyðublað 1095-C er prentað fyrir fleiri en 500 starfsmenn færðu fleiri en eina PDF-skrá afhenta.</span><span class="sxs-lookup"><span data-stu-id="d8cba-138">If you're printing 1095-C forms for more than 500 employees, you'll receive more than one PDF file.</span></span> <span data-ttu-id="d8cba-139">Mælt er með því að auka **Hámarksstærð skráar** í glugganum **Færibreytur skjalastjórnunar** í 150 MB.</span><span class="sxs-lookup"><span data-stu-id="d8cba-139">It’s recommended that you increase the **Maximum file size** in the **Document management parameters** window to 150 MB.</span></span>

## <a name="viewing-information"></a><span data-ttu-id="d8cba-140">Skoðun upplýsinga</span><span class="sxs-lookup"><span data-stu-id="d8cba-140">Viewing information</span></span>

<span data-ttu-id="d8cba-141">Hægt er að nota síðuna **Affordable Care-trygging fyrir starfsmann** til að sjá hvaða starfsmenn hafa verið settir í hvaða tryggingahóp, hvaða starfsmenn þurfa að ekki að vera í skýrslu og hvaða starfsmenn hafa ekki verið settir í neinn hóp.</span><span class="sxs-lookup"><span data-stu-id="d8cba-141">You can use the **Worker Affordable Care coverage** page to see which employees have been assigned to each coverage group, which employees don’t need to be included on a report, and which employees are unassigned.</span></span>

<span data-ttu-id="d8cba-142">Ef einhverjum sjálfgefnum gildum úr Affordable Care-tryggingaflokknum hefur verið hnekkt, birtist stjarna við hliðina á gildinu sem var breytt.</span><span class="sxs-lookup"><span data-stu-id="d8cba-142">If any of the default values from the Affordable Care coverage group have been overridden, an asterisk will appear next to the value that was changed.</span></span> <span data-ttu-id="d8cba-143">Ef gildi fyrir alla 12 mánuðina eru þau sömu og þeim hefur ekki verið hnekkt, mun gildið prentast í dálknum **Allir 12 mánuðirnir**.</span><span class="sxs-lookup"><span data-stu-id="d8cba-143">If the values for all 12 months are the same and haven’t been overridden, the value will print in the **All 12 months** column.</span></span>

<span data-ttu-id="d8cba-144">Einnig er hægt að nota fyrirspurnargluggann til að komast að því hvaða starfsmenn hafa verið flaggaðir sem ekki ACA-tilkynningaskyldir.</span><span class="sxs-lookup"><span data-stu-id="d8cba-144">You can also use the inquiry window to understand which employees have been flagged as not ACA reportable.</span></span> <span data-ttu-id="d8cba-145">Ekki þarf að fylgjast með því hvort þeim var boðin trygging og ekki þarf að gefa út 1095-C til þeirra í árslok.</span><span class="sxs-lookup"><span data-stu-id="d8cba-145">You don’t need to track whether coverage was offered to them and won't need to issue a 1095-C to them at the end of the year.</span></span> <span data-ttu-id="d8cba-146">Velja skal **Er ekki ACA-tilkynningaskylt** í reitnum **Sía eftir** til að búa til lista yfir starfsmenn sem fá ekki 1095-C.</span><span class="sxs-lookup"><span data-stu-id="d8cba-146">Select **Not ACA reportable** in the **Filter by** field to generate a list of all employees who won't receive a 1095-C.</span></span>

<span data-ttu-id="d8cba-147">Að auki er hægt að skoða starfsmenn sem ekki úthlutað (reiturinn **Telja ACA-tryggingu fram** er auður) eða hefur verið úthlutað í Affordable Care-tryggingaflokk sem er útrunninn fyrir árið sem er valið í reitnum **Ár**.</span><span class="sxs-lookup"><span data-stu-id="d8cba-147">In addition, you can view any employees who are unassigned (the **ACA Report coverage** field is empty) or who have been assigned to an Affordable Care coverage group that is expired for the year selected in the **Year** field.</span></span>

<span data-ttu-id="d8cba-148">Hægt er að flytja út lista yfir starfsmenn í Excel sem voru myndaðir með einhverjum af síunarkostunum.</span><span class="sxs-lookup"><span data-stu-id="d8cba-148">You can export lists of employees that were generated using any of the filtering options to Excel.</span></span>

<span data-ttu-id="d8cba-149">Ef þarf að tilkynna tryggða einstaklinga vegna þess að þú býður upp á sjálfstryggða tryggingu, er hægt að skoða skjólstæðinga sem eru tryggðir undir fríðindaáætlunum merktar sem **ACA-tilkynningaskylt**.</span><span class="sxs-lookup"><span data-stu-id="d8cba-149">If you need to report covered individuals because you provide self-insured coverage, you can view any dependents covered under benefit plans marked as **ACA reportable**.</span></span> <span data-ttu-id="d8cba-150">Veljið **Skoða tryggingar skjólstæðinga** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="d8cba-150">Select **View Dependent coverage** on the action pane.</span></span>

> [!NOTE]
> <span data-ttu-id="d8cba-151">Aðeins fríðindaáætlanir sem eru merktar **ACA-tilkynningaskylt** birtast í fyrirspurnarglugganum.</span><span class="sxs-lookup"><span data-stu-id="d8cba-151">Only benefit plans marked as **ACA reportable** display in the inquiry window.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]