---
title: Greina niðurstöður spurningalista
description: Hægt er að nota talnagögn spurningalista til að reikna út meðaltöl, samtölur og prósentur samkvæmt lýðfræðilegum gögn.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9d3b13ef7eda9943af35bbb37e3059dd81aa6365
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009456"
---
# <a name="analyzing-questionnaire-results"></a><span data-ttu-id="afe06-103">Greina niðurstöður spurningalista</span><span class="sxs-lookup"><span data-stu-id="afe06-103">Analyzing questionnaire results</span></span>



<span data-ttu-id="afe06-104">Hægt er að nota talnagögn spurningalista til að reikna út meðaltöl, samtölur og prósentur samkvæmt lýðfræðilegum gögn.</span><span class="sxs-lookup"><span data-stu-id="afe06-104">Questionnaire statistics can be used to calculate averages, totals, and percentages based on a set of demographic data.</span></span> <span data-ttu-id="afe06-105">Til að hefja ferlið, farið í Spurningalist > Skoða og greina niðurstöður > Talnagögn spurningalista.</span><span class="sxs-lookup"><span data-stu-id="afe06-105">To begin this procedure, go to Questionnaire > View and analyze results > Questionnaire statistics.</span></span> <span data-ttu-id="afe06-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="afe06-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-statistics-record"></a><span data-ttu-id="afe06-107">Stofna færslu fyrir talnagögn Spurningalista</span><span class="sxs-lookup"><span data-stu-id="afe06-107">Create a Questionnaire statistics record</span></span>
1. <span data-ttu-id="afe06-108">Fara á talnagögn spurningalista</span><span class="sxs-lookup"><span data-stu-id="afe06-108">Go to Questionnaire statistics.</span></span>
2. <span data-ttu-id="afe06-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="afe06-109">Click New.</span></span>
3. <span data-ttu-id="afe06-110">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="afe06-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="afe06-111">Í reitnum talnagögn skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="afe06-111">In the Statistics field, type a value.</span></span>
5. <span data-ttu-id="afe06-112">Í reitinn Lýsing skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="afe06-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="afe06-113">Í reitnum Spurningalisti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="afe06-113">In the Questionnaire field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="afe06-114">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="afe06-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="afe06-115">Smellið á flipann „Almennt“.</span><span class="sxs-lookup"><span data-stu-id="afe06-115">Click the General tab.</span></span>
    * <span data-ttu-id="afe06-116">Veljið ef óskað er að taka með niðurstöður fyrir ónafngreinda eða niðurstöður úr starfsmönnum, tengiliði og umsækjendur.</span><span class="sxs-lookup"><span data-stu-id="afe06-116">Select if you want to include anonymous results or results from workers, contacts, and applicants.</span></span>  
9. <span data-ttu-id="afe06-117">Veldu eða hreinsaðu gátreitinn starfsmaður.</span><span class="sxs-lookup"><span data-stu-id="afe06-117">Select or clear the Worker check box.</span></span>
    * <span data-ttu-id="afe06-118">Ef þú verður að skoða niðurstöður eftir aldur eða starfsaldur, tilgreina bil sem óskað er að nota til að flokka niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="afe06-118">If you will be viewing the results by seniority or age, specify the intervals that you would like to use for grouping the results.</span></span>  
    * <span data-ttu-id="afe06-119">Innfærsla á 5 fyrir aldursbilið mun flokka niðurstöðurnar samkvæmt fimm ár aldursbila.</span><span class="sxs-lookup"><span data-stu-id="afe06-119">Entering a 5 for the age interval will group the results based on five-year age intervals.</span></span>  
10. <span data-ttu-id="afe06-120">Í reitinn aldur skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="afe06-120">In the Age field, enter a number.</span></span>
    * <span data-ttu-id="afe06-121">Veljið ef óskað er að keyra útreikning gagnvart öllum spurningalistanum, fyrir hvern niðurstöðuflokk, fyrir hverja spurningu, eða fyrir hvern spurningaröð.</span><span class="sxs-lookup"><span data-stu-id="afe06-121">Select if you want to run the calculation against the entire questionnaire, for each result group, for each question, or for each question row.</span></span>  
    * <span data-ttu-id="afe06-122">Velja hvernig óskað er að flokka niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="afe06-122">Select how you would like to group the results.</span></span>  
    * <span data-ttu-id="afe06-123">Til dæmis, ef meðaltal punkta fyrir hverja spurningu er reiknað, viltu e.t.v. sjá spurningar flokkuð eftir niðurstöðuflokki.</span><span class="sxs-lookup"><span data-stu-id="afe06-123">For example, if you calculate the average points per question, you may want to see the questions grouped by Result group.</span></span>  
    * <span data-ttu-id="afe06-124">Velja gögn til að byggja útreikning á.</span><span class="sxs-lookup"><span data-stu-id="afe06-124">Select the data to base the calculation on.</span></span>  
    * <span data-ttu-id="afe06-125">Til dæmis, ef óskað er að sjá meðaltalsprósent sem fékkst úr í spurningalista á meðal starfsmenn þinna eða meðaltal stigafjölda sem var náð á meðal starfsmanna þinna.</span><span class="sxs-lookup"><span data-stu-id="afe06-125">For example, if you want to see the average percent received on the questionnaire across your workers versus the average number of points achieved across your workers.</span></span>  
11. <span data-ttu-id="afe06-126">Smellt er á flipann Svið.</span><span class="sxs-lookup"><span data-stu-id="afe06-126">Click the Range tab.</span></span>
    * <span data-ttu-id="afe06-127">Notið afmarkanir til að takmarka niðurstöðum við einungis þá sem uppfylla skilyrði afmörkunar.</span><span class="sxs-lookup"><span data-stu-id="afe06-127">Use ranges to limit your result set to only those meeting the Range criteria.</span></span>  
12. <span data-ttu-id="afe06-128">Smellið á flipann Flokkun .</span><span class="sxs-lookup"><span data-stu-id="afe06-128">Click the Grouping by tab.</span></span>
    * <span data-ttu-id="afe06-129">Flokkanir er notuð til að ákvarða hvernig á að birta niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="afe06-129">Use Groupings to determine how the results should be displayed.</span></span>  
    * <span data-ttu-id="afe06-130">Til dæmis flokka niðurstöðurnar fyrst eftir kyni, síðan eftir aldri.</span><span class="sxs-lookup"><span data-stu-id="afe06-130">For example, group the results first by gender, then by age.</span></span>  
13. <span data-ttu-id="afe06-131">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="afe06-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="afe06-132">Flytja í flokkanir inn á valda hlið og setja þær í viðeigandi röð.</span><span class="sxs-lookup"><span data-stu-id="afe06-132">Move the groupings into the Selected side and place them in the desired order.</span></span>  

## <a name="execute-the-statistics-calculation"></a><span data-ttu-id="afe06-133">Framkvæma útreikningur talnagagna</span><span class="sxs-lookup"><span data-stu-id="afe06-133">Execute the statistics calculation</span></span>
1. <span data-ttu-id="afe06-134">Smelltu á Keyra.</span><span class="sxs-lookup"><span data-stu-id="afe06-134">Click Execute.</span></span>
    * <span data-ttu-id="afe06-135">Velja hvaða aðgerð útreiknings sem óskað er að framkvæma á niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="afe06-135">Select which calculation function you would like to perform on the results.</span></span>  
    * <span data-ttu-id="afe06-136">Til dæmis er hægt að reikna meðaltal prósentur milli spurningalista fyrir valdar flokkanir eða samtala punkta yfir niðurstöðuflokka fyrir valdar flokkanir.</span><span class="sxs-lookup"><span data-stu-id="afe06-136">For example, calculate the average percentages across the questionnaire for the selected groupings or total the points across the result groups for the selected groupings.</span></span>  
2. <span data-ttu-id="afe06-137">Veljið eða hreinsið gátreit Eyða fyrri leit.</span><span class="sxs-lookup"><span data-stu-id="afe06-137">Select or clear the Delete previous searches check box.</span></span>
3. <span data-ttu-id="afe06-138">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="afe06-138">Click OK.</span></span>

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a><span data-ttu-id="afe06-139">Skoða niðurstöður keyrslu talnagögn spurningalista.</span><span class="sxs-lookup"><span data-stu-id="afe06-139">View the results of the questionnaire statistics run.</span></span>
1. <span data-ttu-id="afe06-140">Smelltu á Niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="afe06-140">Click Result.</span></span>
2. <span data-ttu-id="afe06-141">Smelltu á Niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="afe06-141">Click Result.</span></span>
3. <span data-ttu-id="afe06-142">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="afe06-142">Close the page.</span></span>

