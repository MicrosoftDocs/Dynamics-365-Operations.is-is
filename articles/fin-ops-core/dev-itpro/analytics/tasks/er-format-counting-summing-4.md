---
title: Rafræn skýrslugerð Skilgreina snið til að gera talningu og samlagningu (Hluti 4 - keyra snið)
description: Í þessu efni er útskýrt hvernig á að skilgreina snið rafrænnar skýrslugerðar til að telja og gera samantekt sem byggist á gögnum fyrir þegar myndað úttak texta. (Hluti 4)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5576229e8b81824dff6d0b38b8ab5483e04ade8
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092948"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="302da-104">Rafræn skýrslugerð Skilgreina snið til að gera talningu og samlagningu (Hluti 4 - keyra snið)</span><span class="sxs-lookup"><span data-stu-id="302da-104">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="302da-105">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt snið rafrænnar skýrslugerðar (ER) til að telja og taka saman á grundvelli gagna textaúttaks sem þegar var myndað.</span><span class="sxs-lookup"><span data-stu-id="302da-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="302da-106">Hægt er að framkvæma þessum skrefum í DEMF fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="302da-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="302da-107">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð skilgreingasnið sér um að telja og taka saman (Hluti 3: Nota útreikninga til að búa til úttak)”.</span><span class="sxs-lookup"><span data-stu-id="302da-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="302da-108">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="302da-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="302da-109">Prófa þetta afbrigði fyrir myndun intrastat-skýrslur</span><span class="sxs-lookup"><span data-stu-id="302da-109">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="302da-110">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="302da-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="302da-111">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="302da-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="302da-112">Í trénu skal víkka út 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="302da-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="302da-113">Í trénu skal víkka út 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="302da-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="302da-114">Í trénu skal velja „Intrastat model\Intrastat (DE)\Intrastat (DE) með talningu & samlagningu“.</span><span class="sxs-lookup"><span data-stu-id="302da-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="302da-115">Í Aðgerðarrúðunni er smellt á skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="302da-115">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="302da-116">Smelltu á Færibreytur notanda</span><span class="sxs-lookup"><span data-stu-id="302da-116">Click User parameters.</span></span>
8. <span data-ttu-id="302da-117">Veljið Já í svæðinu Stillingar keyrslu.</span><span class="sxs-lookup"><span data-stu-id="302da-117">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="302da-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="302da-118">Click OK.</span></span>
10. <span data-ttu-id="302da-119">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="302da-119">Click Edit.</span></span>
11. <span data-ttu-id="302da-120">Veljið Já í svæðinu drög keyrslu.</span><span class="sxs-lookup"><span data-stu-id="302da-120">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="302da-121">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="302da-121">Click Save.</span></span>
13. <span data-ttu-id="302da-122">Fara í Skattur > Uppsetning > Erlend viðskipti > Færibreytur erlendra viðskipta.</span><span class="sxs-lookup"><span data-stu-id="302da-122">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="302da-123">Útvíkka hlutann Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="302da-123">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="302da-124">Veljið skilgreininguna „Intrastat (DE) með talningu og samlagningu“.</span><span class="sxs-lookup"><span data-stu-id="302da-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="302da-125">Veljið skilgreininguna „Intrastat (DE) með talningu og samlagningu“.</span><span class="sxs-lookup"><span data-stu-id="302da-125">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="302da-126">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="302da-126">Click Save.</span></span>
18. <span data-ttu-id="302da-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="302da-127">Close the page.</span></span>
19. <span data-ttu-id="302da-128">Fara í Skattur > Yfirlýsingar > Erlend viðskipti > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="302da-128">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="302da-129">Smellið á úttak</span><span class="sxs-lookup"><span data-stu-id="302da-129">Click Output.</span></span>
21. <span data-ttu-id="302da-130">Smellið á Skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="302da-130">Click Report.</span></span>
    * <span data-ttu-id="302da-131">Keyra myndunarferli intrastat-skýrslu.</span><span class="sxs-lookup"><span data-stu-id="302da-131">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="302da-132">Í svæði Frá-dagsetningu, stilla á dagsetningu ' 2000-01-01 ".</span><span class="sxs-lookup"><span data-stu-id="302da-132">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="302da-133">Skilgreinið upphafs og lokadagsetningar fyrir skýrslutímabil sem innihalda fyrirliggjandi færslur í skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="302da-133">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="302da-134">Í svæðinu Til dags, setja dagsetningu ' 2022-12-31'.</span><span class="sxs-lookup"><span data-stu-id="302da-134">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="302da-135">Skilgreinið upphafs og lokadagsetningar fyrir skýrslutímabil sem innihalda fyrirliggjandi færslur í skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="302da-135">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="302da-136">Í reitnum stefna skal velja "komur".</span><span class="sxs-lookup"><span data-stu-id="302da-136">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="302da-137">Velja skal Já í svæðinu Mynda skrá.</span><span class="sxs-lookup"><span data-stu-id="302da-137">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="302da-138">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="302da-138">Click OK.</span></span>
    * <span data-ttu-id="302da-139">Fara yfir stofnað úttak með samantektarlínur í lok.</span><span class="sxs-lookup"><span data-stu-id="302da-139">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="302da-140">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="302da-140">Click New.</span></span>
28. <span data-ttu-id="302da-141">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="302da-141">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="302da-142">Í reitnum stefna skal velja "sendingar".</span><span class="sxs-lookup"><span data-stu-id="302da-142">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="302da-143">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="302da-143">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="302da-144">Sláið inn eða veldu gildi í vörur reitnum.</span><span class="sxs-lookup"><span data-stu-id="302da-144">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="302da-145">Stilla á þyngd á "10".</span><span class="sxs-lookup"><span data-stu-id="302da-145">Set Weight to '10'.</span></span>
33. <span data-ttu-id="302da-146">Stilla upphæð reiknings á "10000".</span><span class="sxs-lookup"><span data-stu-id="302da-146">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="302da-147">Stilla Tölfræðileg upphæð á "10000".</span><span class="sxs-lookup"><span data-stu-id="302da-147">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="302da-148">Smellið á úttak</span><span class="sxs-lookup"><span data-stu-id="302da-148">Click Output.</span></span>
36. <span data-ttu-id="302da-149">Smellið á Skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="302da-149">Click Report.</span></span>
37. <span data-ttu-id="302da-150">Í reitnum stefna skal velja "sendingar".</span><span class="sxs-lookup"><span data-stu-id="302da-150">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="302da-151">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="302da-151">Click OK.</span></span>
    * <span data-ttu-id="302da-152">Fara yfir stofnað úttak með samantektarlínur í lok.</span><span class="sxs-lookup"><span data-stu-id="302da-152">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="302da-153">Athugið að það hefur verið breytt miðað við fyrstu keyrsluna.</span><span class="sxs-lookup"><span data-stu-id="302da-153">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="302da-154">Keyra þetta afbrigði er í kembiham til að endurskoða uppsöfnuð gögn talningar & samlagningar</span><span class="sxs-lookup"><span data-stu-id="302da-154">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="302da-155">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="302da-155">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="302da-156">Í trénu skal víkka út 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="302da-156">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="302da-157">Í trénu skal víkka út 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="302da-157">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="302da-158">Í trénu skal velja „Intrastat model\Intrastat (DE)\Intrastat (DE) með talningu & samlagningu“.</span><span class="sxs-lookup"><span data-stu-id="302da-158">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="302da-159">Í Aðgerðarrúðunni er smellt á skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="302da-159">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="302da-160">Smelltu á Færibreytur notanda</span><span class="sxs-lookup"><span data-stu-id="302da-160">Click User parameters.</span></span>
7. <span data-ttu-id="302da-161">Velja skal Já í reitinn keyra í kembingarhami.</span><span class="sxs-lookup"><span data-stu-id="302da-161">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="302da-162">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="302da-162">Click OK.</span></span>
9. <span data-ttu-id="302da-163">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="302da-163">Close the page.</span></span>
10. <span data-ttu-id="302da-164">Fara í Skattur > Yfirlýsingar > Erlend viðskipti > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="302da-164">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="302da-165">Smellið á úttak</span><span class="sxs-lookup"><span data-stu-id="302da-165">Click Output.</span></span>
12. <span data-ttu-id="302da-166">Smellið á Skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="302da-166">Click Report.</span></span>
13. <span data-ttu-id="302da-167">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="302da-167">Click OK.</span></span>
14. <span data-ttu-id="302da-168">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="302da-168">Close the page.</span></span>
15. <span data-ttu-id="302da-169">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="302da-169">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="302da-170">Í trénu skal víkka út 'Intrastat model'.</span><span class="sxs-lookup"><span data-stu-id="302da-170">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="302da-171">Í trénu skal víkka út 'Intrastat model\Intrastat (DE)'.</span><span class="sxs-lookup"><span data-stu-id="302da-171">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="302da-172">Í trénu skal velja „Intrastat model\Intrastat (DE)\Intrastat (DE) með talningu & samlagningu“.</span><span class="sxs-lookup"><span data-stu-id="302da-172">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="302da-173">Smelltu á kembingarkladda.</span><span class="sxs-lookup"><span data-stu-id="302da-173">Click Debug logs.</span></span>
    * <span data-ttu-id="302da-174">Athugið að kladdfærsla kembingar hefur verið stofnuð fyrir framkvæmd vinnslu á valinni skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="302da-174">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="302da-175">Smellt er á Hengja við.</span><span class="sxs-lookup"><span data-stu-id="302da-175">Click Attach.</span></span>
21. <span data-ttu-id="302da-176">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="302da-176">Click Open.</span></span>
    * <span data-ttu-id="302da-177">Fara yfir stofnaða xml-skrána sem inniheldur upplýsingar um talningu og samlagningu sem safnað var við keyrslu á valinni skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="302da-177">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  

