--- 
title: "Keyra snið fyrir talningu og samlagningu í rafrænni skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 60a34e35a376635669b764457617cb997822bdcd
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="run-the-format-to-do-counting-and-summing-for-electronic-reporting-er"></a><span data-ttu-id="a484a-103">Keyra snið fyrir talningu og samlagningu í rafrænni skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="a484a-103">Run the format to do counting and summing for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a484a-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað.</span><span class="sxs-lookup"><span data-stu-id="a484a-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="a484a-105">Hægt er að framkvæma þessum skrefum í DEMF fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="a484a-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="a484a-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á "Rafræn skýrslugerð skilgreingasnið sér um að telja og taka saman (Hluti 3: Nota útreikninga til að búa til úttak)" ferli.</span><span class="sxs-lookup"><span data-stu-id="a484a-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="a484a-107">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="a484a-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="a484a-108">Prófa þetta afbrigði fyrir myndun intrastat-skýrslur</span><span class="sxs-lookup"><span data-stu-id="a484a-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="a484a-109">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="a484a-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a484a-110">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="a484a-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="a484a-111">Í trénu skal víkka út 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="a484a-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="a484a-112">Í trénu skal víkka út 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="a484a-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="a484a-113">Í trénu skal velja „Intrastat model\Intrastat (DE)\Intrastat (DE) með talningu & samlagningu“.</span><span class="sxs-lookup"><span data-stu-id="a484a-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="a484a-114">Í Aðgerðarrúðunni er smellt á skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="a484a-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="a484a-115">Smelltu á Færibreytur notanda</span><span class="sxs-lookup"><span data-stu-id="a484a-115">Click User parameters.</span></span>
8. <span data-ttu-id="a484a-116">Veljið Já í svæðinu Stillingar keyrslu.</span><span class="sxs-lookup"><span data-stu-id="a484a-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="a484a-117">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a484a-117">Click OK.</span></span>
10. <span data-ttu-id="a484a-118">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="a484a-118">Click Edit.</span></span>
11. <span data-ttu-id="a484a-119">Veljið Já í svæðinu drög keyrslu.</span><span class="sxs-lookup"><span data-stu-id="a484a-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="a484a-120">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a484a-120">Click Save.</span></span>
13. <span data-ttu-id="a484a-121">Fara í Skattur > Uppsetning > Erlend viðskipti > Færibreytur erlendra viðskipta.</span><span class="sxs-lookup"><span data-stu-id="a484a-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="a484a-122">Útvíkka hlutann Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="a484a-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="a484a-123">Veljið skilgreininguna „Intrastat (DE) með talningu & samlagningu“.</span><span class="sxs-lookup"><span data-stu-id="a484a-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="a484a-124">Veljið skilgreininguna „Intrastat (DE) með talningu & samlagningu“.</span><span class="sxs-lookup"><span data-stu-id="a484a-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="a484a-125">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a484a-125">Click Save.</span></span>
18. <span data-ttu-id="a484a-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a484a-126">Close the page.</span></span>
19. <span data-ttu-id="a484a-127">Fara í Skattur > Yfirlýsingar > Erlend viðskipti > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="a484a-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="a484a-128">Smellið á úttak</span><span class="sxs-lookup"><span data-stu-id="a484a-128">Click Output.</span></span>
21. <span data-ttu-id="a484a-129">Smellið á Skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="a484a-129">Click Report.</span></span>
    * <span data-ttu-id="a484a-130">Keyra myndunarferli intrastat-skýrslu.</span><span class="sxs-lookup"><span data-stu-id="a484a-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="a484a-131">Í svæði Frá-dagsetningu, stilla á dagsetningu ' 2000-01-01 ".</span><span class="sxs-lookup"><span data-stu-id="a484a-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="a484a-132">Skilgreinið upphafs og lokadagsetningar fyrir skýrslutímabil sem innihalda fyrirliggjandi færslur í skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="a484a-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="a484a-133">Í svæðinu Til dags, setja dagsetningu ' 2022-12-31'.</span><span class="sxs-lookup"><span data-stu-id="a484a-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="a484a-134">Skilgreinið upphafs og lokadagsetningar fyrir skýrslutímabil sem innihalda fyrirliggjandi færslur í skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="a484a-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="a484a-135">Í reitnum stefna skal velja "komur".</span><span class="sxs-lookup"><span data-stu-id="a484a-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="a484a-136">Velja skal Já í svæðinu Mynda skrá.</span><span class="sxs-lookup"><span data-stu-id="a484a-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="a484a-137">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a484a-137">Click OK.</span></span>
    * <span data-ttu-id="a484a-138">Fara yfir stofnað úttak með samantektarlínur í lok.</span><span class="sxs-lookup"><span data-stu-id="a484a-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="a484a-139">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="a484a-139">Click New.</span></span>
28. <span data-ttu-id="a484a-140">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="a484a-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="a484a-141">Í reitnum stefna skal velja "sendingar".</span><span class="sxs-lookup"><span data-stu-id="a484a-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="a484a-142">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="a484a-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="a484a-143">Sláið inn eða veldu gildi í vörur reitnum.</span><span class="sxs-lookup"><span data-stu-id="a484a-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="a484a-144">Stilla á þyngd á "10".</span><span class="sxs-lookup"><span data-stu-id="a484a-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="a484a-145">Stilla upphæð reiknings á "10000".</span><span class="sxs-lookup"><span data-stu-id="a484a-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="a484a-146">Stilla Tölfræðileg upphæð á "10000".</span><span class="sxs-lookup"><span data-stu-id="a484a-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="a484a-147">Smellið á úttak</span><span class="sxs-lookup"><span data-stu-id="a484a-147">Click Output.</span></span>
36. <span data-ttu-id="a484a-148">Smellið á Skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="a484a-148">Click Report.</span></span>
37. <span data-ttu-id="a484a-149">Í reitnum stefna skal velja "sendingar".</span><span class="sxs-lookup"><span data-stu-id="a484a-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="a484a-150">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a484a-150">Click OK.</span></span>
    * <span data-ttu-id="a484a-151">Fara yfir stofnað úttak með samantektarlínur í lok.</span><span class="sxs-lookup"><span data-stu-id="a484a-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="a484a-152">Athugið að það hefur verið breytt miðað við fyrstu keyrsluna.</span><span class="sxs-lookup"><span data-stu-id="a484a-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="a484a-153">Keyra þetta afbrigði er í kembiham til að endurskoða uppsöfnuð gögn talningar & samlagningar</span><span class="sxs-lookup"><span data-stu-id="a484a-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="a484a-154">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="a484a-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a484a-155">Í trénu skal víkka út 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="a484a-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="a484a-156">Í trénu skal víkka út 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="a484a-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="a484a-157">Í trénu skal velja „Intrastat model\Intrastat (DE)\Intrastat (DE) með talningu & samlagningu“.</span><span class="sxs-lookup"><span data-stu-id="a484a-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="a484a-158">Í Aðgerðarrúðunni er smellt á skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="a484a-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="a484a-159">Smelltu á Færibreytur notanda</span><span class="sxs-lookup"><span data-stu-id="a484a-159">Click User parameters.</span></span>
7. <span data-ttu-id="a484a-160">Velja skal Já í reitinn keyra í kembingarhami.</span><span class="sxs-lookup"><span data-stu-id="a484a-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="a484a-161">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a484a-161">Click OK.</span></span>
9. <span data-ttu-id="a484a-162">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a484a-162">Close the page.</span></span>
10. <span data-ttu-id="a484a-163">Fara í Skattur > Yfirlýsingar > Erlend viðskipti > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="a484a-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="a484a-164">Smellið á úttak</span><span class="sxs-lookup"><span data-stu-id="a484a-164">Click Output.</span></span>
12. <span data-ttu-id="a484a-165">Smellið á Skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="a484a-165">Click Report.</span></span>
13. <span data-ttu-id="a484a-166">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a484a-166">Click OK.</span></span>
14. <span data-ttu-id="a484a-167">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a484a-167">Close the page.</span></span>
15. <span data-ttu-id="a484a-168">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="a484a-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="a484a-169">Í trénu skal víkka út 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="a484a-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="a484a-170">Í trénu skal víkka út 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="a484a-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="a484a-171">Í trénu skal velja „Intrastat model\Intrastat (DE)\Intrastat (DE) með talningu & samlagningu“.</span><span class="sxs-lookup"><span data-stu-id="a484a-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="a484a-172">Smelltu á kembingarkladda.</span><span class="sxs-lookup"><span data-stu-id="a484a-172">Click Debug logs.</span></span>
    * <span data-ttu-id="a484a-173">Athugið að kladdfærsla kembingar hefur verið stofnuð fyrir framkvæmd vinnslu á valinni skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="a484a-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="a484a-174">Smellt er á Hengja við.</span><span class="sxs-lookup"><span data-stu-id="a484a-174">Click Attach.</span></span>
21. <span data-ttu-id="a484a-175">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="a484a-175">Click Open.</span></span>
    * <span data-ttu-id="a484a-176">Fara yfir stofnaða xml-skrána sem inniheldur upplýsingar um talningu og samlagningu sem safnað var við keyrslu á valinni skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="a484a-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  


