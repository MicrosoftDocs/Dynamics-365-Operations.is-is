---
title: Útreikningur fastakostnaður
description: Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði.
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation, CAMOverheadRateCalculationJournalEntry, CAMFormulaAllocationBase
audience: Application User
ms.reviewer: roschlom
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 882804141a6b520e2420343958c7a6b02a7e09ae
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208848"
---
# <a name="overhead-calculation"></a><span data-ttu-id="cd106-103">Útreikningur fastakostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd106-104">Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði.</span><span class="sxs-lookup"><span data-stu-id="cd106-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="cd106-105">Skýrsluskilgreining</span><span class="sxs-lookup"><span data-stu-id="cd106-105">Term definition</span></span>
---------------

<span data-ttu-id="cd106-106">Stjórnunarkostnaður er sá kostnaður sem stofnað er til fyrir rekstur fyrirtækis, en sem ekki er hægt að rekja beint til neinna sérstakrar starfsemi, vöru eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="cd106-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="cd106-107">Stjórnunarkostnaður veitir mikilvægan stuðning við myndun hagnaðarmyndandi verkþátta.</span><span class="sxs-lookup"><span data-stu-id="cd106-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="cd106-108">Hér eru nokkur dæmi um skilyrði:</span><span class="sxs-lookup"><span data-stu-id="cd106-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="cd106-109">Leiga</span><span class="sxs-lookup"><span data-stu-id="cd106-109">Rent</span></span>
-   <span data-ttu-id="cd106-110">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-110">Electricity</span></span>
-   <span data-ttu-id="cd106-111">Stjórnunarkostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="cd106-112">Yfirlit yfir útreikning fastakostnaðar</span><span class="sxs-lookup"><span data-stu-id="cd106-112">Overhead calculation overview</span></span>
<span data-ttu-id="cd106-113">Útreikningur fastakostnaðar keyrir reglur kostnaðarbókhalds í réttri röð.</span><span class="sxs-lookup"><span data-stu-id="cd106-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="cd106-114">Hægt er að keyra útreikning fastakostnaðar margsinnis fyrir sama fjárhagstímabil ef reglum kostnaðarbókhalds hefur verið breytt eða ákveðnar villur hafa fundist.</span><span class="sxs-lookup"><span data-stu-id="cd106-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="cd106-115">Hver keyrsla á útreikningi fastakostnaðar er geymd og fær einkvæmt útgáfukenni sem gerir kleift að bera saman útreikning í mismunandi útgáfum.</span><span class="sxs-lookup"><span data-stu-id="cd106-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="cd106-116">Kostnaðarfærslur sem útreikningur fastakostnaðar mynda fá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="cd106-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="cd106-117">Dagsetningin bókhald samsvarar lokadagsetning fjárhagstímabilsins sem er dagsetning reikningsskiladagsetning reikningsskila notað í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="cd106-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="cd106-118">Einkvæmt útgáfukenni samanstendur af eftirfarandi þáttum:</span><span class="sxs-lookup"><span data-stu-id="cd106-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="cd106-119">Gerð útgáfu</span><span class="sxs-lookup"><span data-stu-id="cd106-119">Version type</span></span>
-   <span data-ttu-id="cd106-120">Dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="cd106-120">Date and time</span></span>
-   <span data-ttu-id="cd106-121">Fjárhagur kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="cd106-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="cd106-122">Fjárhagsár</span><span class="sxs-lookup"><span data-stu-id="cd106-122">Fiscal year</span></span>
-   <span data-ttu-id="cd106-123">Reikningstímabil</span><span class="sxs-lookup"><span data-stu-id="cd106-123">Fiscal period</span></span>

<span data-ttu-id="cd106-124">Útreikningur fastakostnaðar er keyrður óháð því hver útgáfan er.</span><span class="sxs-lookup"><span data-stu-id="cd106-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="cd106-125">Þess vegna er hægt að reikna út áætlaða útgáfu á undan raunútgáfu.</span><span class="sxs-lookup"><span data-stu-id="cd106-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="cd106-126">Útreikningur fastakostnaðar samanstendur af fjórum skrefum, eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="cd106-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="cd106-127">Í hverju skrefi er færslubókarhaus stofnaður með bókarfærslum.</span><span class="sxs-lookup"><span data-stu-id="cd106-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="cd106-128">Þessi færslubókarhaus geymir inntaksgögn fyrir hvert útreikningsþrep.</span><span class="sxs-lookup"><span data-stu-id="cd106-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="cd106-129">Stefnur og reglur eru notaðar í hverri færslulínu og kostnaðarfærslur eru myndaðar sem úttak.</span><span class="sxs-lookup"><span data-stu-id="cd106-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="cd106-130">Þess vegna hefurðu ávallt fullan rekjanleika.</span><span class="sxs-lookup"><span data-stu-id="cd106-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="cd106-131">[![Útreikningur fastakostnaðar](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="cd106-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="cd106-132">Reikna og úthluta sameiginlegur kostnaði vegna rafmagns</span><span class="sxs-lookup"><span data-stu-id="cd106-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="cd106-133">Í Fjárhagsbókhaldi er ákveðinn kostnaður, eins og rafmagn, skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="cd106-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="cd106-134">Þar af leiðandi er nákvæmar innsýn rekstrarfélags ekki veitt fyrir kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="cd106-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="cd106-135">Í kostnaðarbókhaldi verður kostnaður að flæða í gegnum fyrirtækiseiningar til að veita rétta innsýn rekstrarfélags þvert á allar fyrirtækiseiningar og stig.</span><span class="sxs-lookup"><span data-stu-id="cd106-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="cd106-136">Þetta flæði verður að byggja á annaðhvort nákvæmri færslu notkunar eða sanngjarnri matsreglu.</span><span class="sxs-lookup"><span data-stu-id="cd106-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="cd106-137">Í fjárhagnum er hægt að bóka rafmagnskostnað eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="cd106-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="cd106-138">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="cd106-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="cd106-139">Kostnaðarstaður</span><span class="sxs-lookup"><span data-stu-id="cd106-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="cd106-140">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="cd106-140">Main account</span></span></th>
<th><span data-ttu-id="cd106-141">Upphæð í bókhaldsgjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="cd106-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-142">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="cd106-143">CC099</span><span class="sxs-lookup"><span data-stu-id="cd106-143">CC099</span></span></td>
<td><span data-ttu-id="cd106-144">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="cd106-144">Default cost center</span></span></td>
<td><span data-ttu-id="cd106-145">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-145">10001</span></span></td>
<td><span data-ttu-id="cd106-146">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-146">Electricity</span></span></td>
<td><span data-ttu-id="cd106-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="cd106-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="cd106-148">Skref 1: Keyra útreikning kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="cd106-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="cd106-149">Sjálfvirkt er að þegar kostnaðarfærslur eru fluttar úr grunngögnum fái þær flokkun kostnaðarhegðunar **Óflokkað** í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="cd106-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="cd106-150">Með því að nota stefnureglur kostnaðarhegðunar er hægt að endurflokka kostnaðarfærslur sem annaðhvort **Fastan kostnað** eða **Breytilegan kostnað**.</span><span class="sxs-lookup"><span data-stu-id="cd106-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="cd106-151">Tilgreinið reglu kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="cd106-151">Define the cost behavior rule</span></span>

<span data-ttu-id="cd106-152">Í sumum tilfellum er hluti af kostnaði föst þóknun og eftirstandandi kostnaður byggist á notkun.</span><span class="sxs-lookup"><span data-stu-id="cd106-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="cd106-153">Rafmagnsreikningar stemma oft við þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="cd106-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="cd106-154">Þegar tiltekin föst þóknun hefur verið greidd, er greitt fyrir notkun á kílóvattklukkustund (Kwh).</span><span class="sxs-lookup"><span data-stu-id="cd106-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="cd106-155">Til dæmis ef föst kostnaðarþóknun er 1000.00 sýnir þetta hvernig regla kostnaðarhegðunar er skilgreind:</span><span class="sxs-lookup"><span data-stu-id="cd106-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="cd106-156">Föst upphæð 1.000,00</span><span class="sxs-lookup"><span data-stu-id="cd106-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="cd106-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="cd106-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="cd106-158">1000.01 &lt; N = Breyta</span><span class="sxs-lookup"><span data-stu-id="cd106-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="cd106-159">Færslubók</span><span class="sxs-lookup"><span data-stu-id="cd106-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="cd106-160">Færslubók</span><span class="sxs-lookup"><span data-stu-id="cd106-160">Journal</span></span></th>
<th><span data-ttu-id="cd106-161">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="cd106-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="cd106-162">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="cd106-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="cd106-163">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="cd106-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-164">00001</span><span class="sxs-lookup"><span data-stu-id="cd106-164">00001</span></span></td>
<td><span data-ttu-id="cd106-165">Færslubók útreiknings fyrir kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="cd106-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="cd106-166">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="cd106-166">Fiscal</span></span></td>
<td><span data-ttu-id="cd106-167">2017</span><span class="sxs-lookup"><span data-stu-id="cd106-167">2017</span></span></td>
<td><span data-ttu-id="cd106-168">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="cd106-168">Period 1</span></span></td>
<td><span data-ttu-id="cd106-169">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="cd106-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="cd106-170">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="cd106-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="cd106-171">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="cd106-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="cd106-172">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="cd106-173">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="cd106-173">Cost element</span></span></th>
<th><span data-ttu-id="cd106-174">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="cd106-174">Cost behavior</span></span></th>
<th><span data-ttu-id="cd106-175">Upphæð</span><span class="sxs-lookup"><span data-stu-id="cd106-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-176">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="cd106-177">CC099</span><span class="sxs-lookup"><span data-stu-id="cd106-177">CC099</span></span></td>
<td><span data-ttu-id="cd106-178">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="cd106-178">Default cost center</span></span></td>
<td><span data-ttu-id="cd106-179">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-179">10001</span></span></td>
<td><span data-ttu-id="cd106-180">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-180">Electricity</span></span></td>
<td><span data-ttu-id="cd106-181">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="cd106-181">Unclassified</span></span></td>
<td><span data-ttu-id="cd106-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="cd106-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="cd106-183">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="cd106-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="cd106-184">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="cd106-185">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="cd106-185">Cost element</span></span></th>
<th><span data-ttu-id="cd106-186">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="cd106-186">Cost behavior</span></span></th>
<th><span data-ttu-id="cd106-187">Upphæð</span><span class="sxs-lookup"><span data-stu-id="cd106-187">Amount</span></span></th>
<th><span data-ttu-id="cd106-188">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="cd106-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-189">CC099</span><span class="sxs-lookup"><span data-stu-id="cd106-189">CC099</span></span></td>
<td><span data-ttu-id="cd106-190">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="cd106-190">Default cost center</span></span></td>
<td><span data-ttu-id="cd106-191">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-191">10001</span></span></td>
<td><span data-ttu-id="cd106-192">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-192">Electricity</span></span></td>
<td><span data-ttu-id="cd106-193">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="cd106-193">Unclassified</span></span></td>
<td><span data-ttu-id="cd106-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="cd106-194">10,000.00</span></span></td>
<td><span data-ttu-id="cd106-195">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-196">CC099</span><span class="sxs-lookup"><span data-stu-id="cd106-196">CC099</span></span></td>
<td><span data-ttu-id="cd106-197">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="cd106-197">Default cost center</span></span></td>
<td><span data-ttu-id="cd106-198">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-198">10001</span></span></td>
<td><span data-ttu-id="cd106-199">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-199">Electricity</span></span></td>
<td><span data-ttu-id="cd106-200">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="cd106-200">Unclassified</span></span></td>
<td><span data-ttu-id="cd106-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="cd106-201">-10,000.00</span></span></td>
<td><span data-ttu-id="cd106-202">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-203">CC099</span><span class="sxs-lookup"><span data-stu-id="cd106-203">CC099</span></span></td>
<td><span data-ttu-id="cd106-204">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="cd106-204">Default cost center</span></span></td>
<td><span data-ttu-id="cd106-205">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-205">10001</span></span></td>
<td><span data-ttu-id="cd106-206">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-206">Electricity</span></span></td>
<td><span data-ttu-id="cd106-207">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-207">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="cd106-208">1,000.00</span></span></td>
<td><span data-ttu-id="cd106-209">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-210">CC099</span><span class="sxs-lookup"><span data-stu-id="cd106-210">CC099</span></span></td>
<td><span data-ttu-id="cd106-211">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="cd106-211">Default cost center</span></span></td>
<td><span data-ttu-id="cd106-212">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-212">10001</span></span></td>
<td><span data-ttu-id="cd106-213">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-213">Electricity</span></span></td>
<td><span data-ttu-id="cd106-214">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-214">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="cd106-215">9,000.00</span></span></td>
<td><span data-ttu-id="cd106-216">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cd106-217">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðarhegðunarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="cd106-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="cd106-218">Skref 2: Keyra útreikning kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="cd106-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="cd106-219">Kostnaðardreifing er notuð til að endurúthluta kostnaði frá einum kostnaðarhlut til annars eða fleiri kostnaðarhluta með því að nota viðeigandi úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="cd106-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="cd106-220">Kostnaðardreifing og kostnaðarúthlutun eru ólíkar að því leyti að kostnaðardreifing kemur alltaf upp á stigi aðalkostnaðareiningar upphaflegs verðs.</span><span class="sxs-lookup"><span data-stu-id="cd106-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="cd106-221">Tilgreinið kostnaðardreifingarreglu</span><span class="sxs-lookup"><span data-stu-id="cd106-221">Define the cost distribution rule</span></span>

<span data-ttu-id="cd106-222">Í Fjárhagsbókhaldi er rafmagnskostnaður oft skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="cd106-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="cd106-223">Í kostnaðarbókhaldi er þessi nálgun ekki nógu nákvæm.</span><span class="sxs-lookup"><span data-stu-id="cd106-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="cd106-224">Breytilegur kostnaði þarf að dreifa á staka kostnaðarhluti á sanngjörnum grunni.</span><span class="sxs-lookup"><span data-stu-id="cd106-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="cd106-225">Rökréttasti úthlutunargrunnurinn er notkun á rafmagni (Kwh).</span><span class="sxs-lookup"><span data-stu-id="cd106-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="cd106-226">Stofnað er tölfræðilegt víddarstak sem er nefnt Rafmagn og rafmagnsnotkun er skráð.</span><span class="sxs-lookup"><span data-stu-id="cd106-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="cd106-227">Sjálfgefið er að öll tölfræðileg víddarstök verða tiltæk sem úthlutunargrunnur.</span><span class="sxs-lookup"><span data-stu-id="cd106-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="cd106-228">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-228">Cost object</span></span></th>
<th><span data-ttu-id="cd106-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="cd106-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-230">CC001</span><span class="sxs-lookup"><span data-stu-id="cd106-230">CC001</span></span></td>
<td><span data-ttu-id="cd106-231">Mannauður</span><span class="sxs-lookup"><span data-stu-id="cd106-231">HR</span></span></td>
<td><span data-ttu-id="cd106-232">1.000</span><span class="sxs-lookup"><span data-stu-id="cd106-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-233">CC002</span><span class="sxs-lookup"><span data-stu-id="cd106-233">CC002</span></span></td>
<td><span data-ttu-id="cd106-234">Fjármál</span><span class="sxs-lookup"><span data-stu-id="cd106-234">Finance</span></span></td>
<td><span data-ttu-id="cd106-235">6,000</span><span class="sxs-lookup"><span data-stu-id="cd106-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-236">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-236">CC003</span></span></td>
<td><span data-ttu-id="cd106-237">Smölun</span><span class="sxs-lookup"><span data-stu-id="cd106-237">Assembly</span></span></td>
<td><span data-ttu-id="cd106-238">0</span><span class="sxs-lookup"><span data-stu-id="cd106-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cd106-239">Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunni fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="cd106-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="cd106-240">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-240">Cost object</span></span></th>
<th><span data-ttu-id="cd106-241">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="cd106-241">Magnitude</span></span></th>
<th><span data-ttu-id="cd106-242">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="cd106-242">Allocation factor</span></span></th>
<th><span data-ttu-id="cd106-243">Upphæð</span><span class="sxs-lookup"><span data-stu-id="cd106-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-244">CC001</span><span class="sxs-lookup"><span data-stu-id="cd106-244">CC001</span></span></td>
<td><span data-ttu-id="cd106-245">Mannauður</span><span class="sxs-lookup"><span data-stu-id="cd106-245">HR</span></span></td>
<td><span data-ttu-id="cd106-246">1.000</span><span class="sxs-lookup"><span data-stu-id="cd106-246">1,000</span></span></td>
<td><span data-ttu-id="cd106-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="cd106-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="cd106-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="cd106-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-249">CC002</span><span class="sxs-lookup"><span data-stu-id="cd106-249">CC002</span></span></td>
<td><span data-ttu-id="cd106-250">Fjármál</span><span class="sxs-lookup"><span data-stu-id="cd106-250">Finance</span></span></td>
<td><span data-ttu-id="cd106-251">6,000</span><span class="sxs-lookup"><span data-stu-id="cd106-251">6,000</span></span></td>
<td><span data-ttu-id="cd106-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="cd106-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="cd106-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="cd106-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-254">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-254">CC003</span></span></td>
<td><span data-ttu-id="cd106-255">Smölun</span><span class="sxs-lookup"><span data-stu-id="cd106-255">Assembly</span></span></td>
<td><span data-ttu-id="cd106-256">0</span><span class="sxs-lookup"><span data-stu-id="cd106-256">0</span></span></td>
<td><span data-ttu-id="cd106-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="cd106-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="cd106-258">0,00</span><span class="sxs-lookup"><span data-stu-id="cd106-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cd106-259">Föstum kostnaði þarf að dreifa jafnt á staka kostnaðarhluti sem hafa notað rafmagn.</span><span class="sxs-lookup"><span data-stu-id="cd106-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="cd106-260">Hægt er að ná þessa niðurstöðu með því að nota tölfræðilegt víddarstakið Rafmagn í úthlutunargrunni reikniformúlu: (Rafmagn &gt; 0,00) Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunn fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="cd106-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="cd106-261">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-261">Cost object</span></span></th>
<th><span data-ttu-id="cd106-262">Formúla</span><span class="sxs-lookup"><span data-stu-id="cd106-262">Formula</span></span></th>
<th><span data-ttu-id="cd106-263">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="cd106-263">Magnitude</span></span></th>
<th><span data-ttu-id="cd106-264">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="cd106-264">Allocation factor</span></span></th>
<th><span data-ttu-id="cd106-265">Upphæð</span><span class="sxs-lookup"><span data-stu-id="cd106-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-266">CC001</span><span class="sxs-lookup"><span data-stu-id="cd106-266">CC001</span></span></td>
<td><span data-ttu-id="cd106-267">Mannauður</span><span class="sxs-lookup"><span data-stu-id="cd106-267">HR</span></span></td>
<td><span data-ttu-id="cd106-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="cd106-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="cd106-269">1</span><span class="sxs-lookup"><span data-stu-id="cd106-269">1</span></span></td>
<td><span data-ttu-id="cd106-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="cd106-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="cd106-271">500,00</span><span class="sxs-lookup"><span data-stu-id="cd106-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-272">CC002</span><span class="sxs-lookup"><span data-stu-id="cd106-272">CC002</span></span></td>
<td><span data-ttu-id="cd106-273">Fjármál</span><span class="sxs-lookup"><span data-stu-id="cd106-273">Finance</span></span></td>
<td><span data-ttu-id="cd106-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="cd106-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="cd106-275">1</span><span class="sxs-lookup"><span data-stu-id="cd106-275">1</span></span></td>
<td><span data-ttu-id="cd106-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="cd106-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="cd106-277">500,00</span><span class="sxs-lookup"><span data-stu-id="cd106-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-278">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-278">CC003</span></span></td>
<td><span data-ttu-id="cd106-279">Smölun</span><span class="sxs-lookup"><span data-stu-id="cd106-279">Assembly</span></span></td>
<td><span data-ttu-id="cd106-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="cd106-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="cd106-281">0</span><span class="sxs-lookup"><span data-stu-id="cd106-281">0</span></span></td>
<td><span data-ttu-id="cd106-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="cd106-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="cd106-283">0,00</span><span class="sxs-lookup"><span data-stu-id="cd106-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="cd106-284">Færslubók</span><span class="sxs-lookup"><span data-stu-id="cd106-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="cd106-285">Færslubók</span><span class="sxs-lookup"><span data-stu-id="cd106-285">Journal</span></span></th>
<th><span data-ttu-id="cd106-286">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="cd106-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="cd106-287">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="cd106-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="cd106-288">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="cd106-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-289">00002</span><span class="sxs-lookup"><span data-stu-id="cd106-289">00002</span></span></td>
<td><span data-ttu-id="cd106-290">Útreikningabók kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="cd106-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="cd106-291">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="cd106-291">Fiscal</span></span></td>
<td><span data-ttu-id="cd106-292">2017</span><span class="sxs-lookup"><span data-stu-id="cd106-292">2017</span></span></td>
<td><span data-ttu-id="cd106-293">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="cd106-293">Period 1</span></span></td>
<td><span data-ttu-id="cd106-294">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="cd106-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="cd106-295">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="cd106-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="cd106-296">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="cd106-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="cd106-297">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="cd106-298">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="cd106-298">Cost element</span></span></th>
<th><span data-ttu-id="cd106-299">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="cd106-299">Cost behavior</span></span></th>
<th><span data-ttu-id="cd106-300">Upphæð</span><span class="sxs-lookup"><span data-stu-id="cd106-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-301">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="cd106-302">CC099</span><span class="sxs-lookup"><span data-stu-id="cd106-302">CC099</span></span></td>
<td><span data-ttu-id="cd106-303">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="cd106-303">Default cost center</span></span></td>
<td><span data-ttu-id="cd106-304">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-304">10001</span></span></td>
<td><span data-ttu-id="cd106-305">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-305">Electricity</span></span></td>
<td><span data-ttu-id="cd106-306">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-306">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="cd106-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-308">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="cd106-309">CC099</span><span class="sxs-lookup"><span data-stu-id="cd106-309">CC099</span></span></td>
<td><span data-ttu-id="cd106-310">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="cd106-310">Default cost center</span></span></td>
<td><span data-ttu-id="cd106-311">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-311">10001</span></span></td>
<td><span data-ttu-id="cd106-312">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-312">Electricity</span></span></td>
<td><span data-ttu-id="cd106-313">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-313">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="cd106-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="cd106-315">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="cd106-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="cd106-316">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="cd106-317">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="cd106-317">Cost element</span></span></th>
<th><span data-ttu-id="cd106-318">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="cd106-318">Cost behavior</span></span></th>
<th><span data-ttu-id="cd106-319">Upphæð</span><span class="sxs-lookup"><span data-stu-id="cd106-319">Amount</span></span></th>
<th><span data-ttu-id="cd106-320">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="cd106-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-321">CC099</span><span class="sxs-lookup"><span data-stu-id="cd106-321">CC099</span></span></td>
<td><span data-ttu-id="cd106-322">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="cd106-322">Default cost center</span></span></td>
<td><span data-ttu-id="cd106-323">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-323">10001</span></span></td>
<td><span data-ttu-id="cd106-324">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-324">Electricity</span></span></td>
<td><span data-ttu-id="cd106-325">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-325">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="cd106-326">-1,000.00</span></span></td>
<td><span data-ttu-id="cd106-327">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-328">CC001</span><span class="sxs-lookup"><span data-stu-id="cd106-328">CC001</span></span></td>
<td><span data-ttu-id="cd106-329">Mannauður</span><span class="sxs-lookup"><span data-stu-id="cd106-329">HR</span></span></td>
<td><span data-ttu-id="cd106-330">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-330">10001</span></span></td>
<td><span data-ttu-id="cd106-331">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-331">Electricity</span></span></td>
<td><span data-ttu-id="cd106-332">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-332">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-333">500,00</span><span class="sxs-lookup"><span data-stu-id="cd106-333">500.00</span></span></td>
<td><span data-ttu-id="cd106-334">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-335">CC002</span><span class="sxs-lookup"><span data-stu-id="cd106-335">CC002</span></span></td>
<td><span data-ttu-id="cd106-336">Fjármál</span><span class="sxs-lookup"><span data-stu-id="cd106-336">Finance</span></span></td>
<td><span data-ttu-id="cd106-337">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-337">10001</span></span></td>
<td><span data-ttu-id="cd106-338">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-338">Electricity</span></span></td>
<td><span data-ttu-id="cd106-339">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-339">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-340">500,00</span><span class="sxs-lookup"><span data-stu-id="cd106-340">500.00</span></span></td>
<td><span data-ttu-id="cd106-341">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-342">CC099</span><span class="sxs-lookup"><span data-stu-id="cd106-342">CC099</span></span></td>
<td><span data-ttu-id="cd106-343">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="cd106-343">Default cost center</span></span></td>
<td><span data-ttu-id="cd106-344">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-344">10001</span></span></td>
<td><span data-ttu-id="cd106-345">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-345">Electricity</span></span></td>
<td><span data-ttu-id="cd106-346">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-346">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="cd106-347">-9,000.00</span></span></td>
<td><span data-ttu-id="cd106-348">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-349">CC001</span><span class="sxs-lookup"><span data-stu-id="cd106-349">CC001</span></span></td>
<td><span data-ttu-id="cd106-350">Mannauður</span><span class="sxs-lookup"><span data-stu-id="cd106-350">HR</span></span></td>
<td><span data-ttu-id="cd106-351">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-351">10001</span></span></td>
<td><span data-ttu-id="cd106-352">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-352">Electricity</span></span></td>
<td><span data-ttu-id="cd106-353">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-353">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="cd106-354">1,285.71</span></span></td>
<td><span data-ttu-id="cd106-355">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-356">CC002</span><span class="sxs-lookup"><span data-stu-id="cd106-356">CC002</span></span></td>
<td><span data-ttu-id="cd106-357">Fjármál</span><span class="sxs-lookup"><span data-stu-id="cd106-357">Finance</span></span></td>
<td><span data-ttu-id="cd106-358">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-358">10001</span></span></td>
<td><span data-ttu-id="cd106-359">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-359">Electricity</span></span></td>
<td><span data-ttu-id="cd106-360">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-360">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="cd106-361">7,714.29</span></span></td>
<td><span data-ttu-id="cd106-362">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cd106-363">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðardreifingarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="cd106-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="cd106-364">Skref 3: Keyra útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="cd106-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="cd106-365">Sameiginlegur kostnaður er notaður til að rukka einn eða fleiri tilgreinda kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="cd106-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="cd106-366">Gjöldin byggjast á fyrirframákveðnu kostnaðarhlutfalli og mæligildi úr úthlutuðum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="cd106-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="cd106-367">Skilgreina sameiginlegan kostnað</span><span class="sxs-lookup"><span data-stu-id="cd106-367">Define the overhead rate</span></span>

<span data-ttu-id="cd106-368">Kostnaðarhlutur CC001 Mannauður stuðlar að safni innri verka.</span><span class="sxs-lookup"><span data-stu-id="cd106-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="cd106-369">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsverk til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="cd106-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="cd106-370">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-370">Cost object</span></span></th>
<th><span data-ttu-id="cd106-371">Tímar</span><span class="sxs-lookup"><span data-stu-id="cd106-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-372">Verk 1</span><span class="sxs-lookup"><span data-stu-id="cd106-372">Proj 1</span></span></td>
<td><span data-ttu-id="cd106-373">Verk 1</span><span class="sxs-lookup"><span data-stu-id="cd106-373">Project 1</span></span></td>
<td><span data-ttu-id="cd106-374">3</span><span class="sxs-lookup"><span data-stu-id="cd106-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-375">Verk 2</span><span class="sxs-lookup"><span data-stu-id="cd106-375">Proj 2</span></span></td>
<td><span data-ttu-id="cd106-376">Verk 2</span><span class="sxs-lookup"><span data-stu-id="cd106-376">Project 2</span></span></td>
<td><span data-ttu-id="cd106-377">1</span><span class="sxs-lookup"><span data-stu-id="cd106-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cd106-378">Fyrirframákveðið kostnaðarhlutfall fyrir kostnaðarframlag verk hefur verið skilgreint.</span><span class="sxs-lookup"><span data-stu-id="cd106-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="cd106-379">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-379">Cost object</span></span></th>
<th><span data-ttu-id="cd106-380">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="cd106-380">Cost element</span></span></th>
<th><span data-ttu-id="cd106-381">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="cd106-381">Cost behavior</span></span></th>
<th><span data-ttu-id="cd106-382">Einingar</span><span class="sxs-lookup"><span data-stu-id="cd106-382">Units</span></span></th>
<th><span data-ttu-id="cd106-383">Taxti</span><span class="sxs-lookup"><span data-stu-id="cd106-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-384">CC001</span><span class="sxs-lookup"><span data-stu-id="cd106-384">CC001</span></span></td>
<td><span data-ttu-id="cd106-385">Mannauður</span><span class="sxs-lookup"><span data-stu-id="cd106-385">HR</span></span></td>
<td><span data-ttu-id="cd106-386">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-386">10001</span></span></td>
<td><span data-ttu-id="cd106-387">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-387">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-388">1</span><span class="sxs-lookup"><span data-stu-id="cd106-388">1</span></span></td>
<td><span data-ttu-id="cd106-389">10</span><span class="sxs-lookup"><span data-stu-id="cd106-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cd106-390">Eftirfarandi tafla sýnir niðurstöður þegar Mannauðsverk eru notuð sem grunnur við úthlutun.</span><span class="sxs-lookup"><span data-stu-id="cd106-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="cd106-391">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-391">Cost object</span></span></th>
<th><span data-ttu-id="cd106-392">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="cd106-392">Magnitude</span></span></th>
<th><span data-ttu-id="cd106-393">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="cd106-393">Cost element</span></span></th>
<th><span data-ttu-id="cd106-394">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="cd106-394">Allocation factor</span></span></th>
<th><span data-ttu-id="cd106-395">Upphæð</span><span class="sxs-lookup"><span data-stu-id="cd106-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-396">Verk 1</span><span class="sxs-lookup"><span data-stu-id="cd106-396">Proj 1</span></span></td>
<td><span data-ttu-id="cd106-397">Verk 1</span><span class="sxs-lookup"><span data-stu-id="cd106-397">Project 1</span></span></td>
<td><span data-ttu-id="cd106-398">3</span><span class="sxs-lookup"><span data-stu-id="cd106-398">3</span></span></td>
<td><span data-ttu-id="cd106-399">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-399">10001</span></span></td>
<td><span data-ttu-id="cd106-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="cd106-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="cd106-401">30,00</span><span class="sxs-lookup"><span data-stu-id="cd106-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-402">Verk 2</span><span class="sxs-lookup"><span data-stu-id="cd106-402">Proj 2</span></span></td>
<td><span data-ttu-id="cd106-403">Verk 2</span><span class="sxs-lookup"><span data-stu-id="cd106-403">Project 2</span></span></td>
<td><span data-ttu-id="cd106-404">1</span><span class="sxs-lookup"><span data-stu-id="cd106-404">1</span></span></td>
<td><span data-ttu-id="cd106-405">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-405">10001</span></span></td>
<td><span data-ttu-id="cd106-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="cd106-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="cd106-407">10,00</span><span class="sxs-lookup"><span data-stu-id="cd106-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="cd106-408">Færslubók</span><span class="sxs-lookup"><span data-stu-id="cd106-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="cd106-409">Færslubók</span><span class="sxs-lookup"><span data-stu-id="cd106-409">Journal</span></span></th>
<th><span data-ttu-id="cd106-410">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="cd106-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="cd106-411">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="cd106-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="cd106-412">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="cd106-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-413">00003</span><span class="sxs-lookup"><span data-stu-id="cd106-413">00003</span></span></td>
<td><span data-ttu-id="cd106-414">Færslubók fyrir útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="cd106-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="cd106-415">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="cd106-415">Fiscal</span></span></td>
<td><span data-ttu-id="cd106-416">2017</span><span class="sxs-lookup"><span data-stu-id="cd106-416">2017</span></span></td>
<td><span data-ttu-id="cd106-417">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="cd106-417">Period 1</span></span></td>
<td><span data-ttu-id="cd106-418">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="cd106-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="cd106-419">Bókarfærslur (Bókarfærslur fyrir útreikning sameiginlegs kostnaðar)</span><span class="sxs-lookup"><span data-stu-id="cd106-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="cd106-420">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="cd106-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="cd106-421">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-421">Cost object</span></span></th>
<th><span data-ttu-id="cd106-422">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="cd106-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-423">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="cd106-424">Verk 1</span><span class="sxs-lookup"><span data-stu-id="cd106-424">Proj 1</span></span></td>
<td><span data-ttu-id="cd106-425">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="cd106-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="cd106-426">3,00</span><span class="sxs-lookup"><span data-stu-id="cd106-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-427">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="cd106-428">Verk 2</span><span class="sxs-lookup"><span data-stu-id="cd106-428">Proj 2</span></span></td>
<td><span data-ttu-id="cd106-429">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="cd106-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="cd106-430">1,00</span><span class="sxs-lookup"><span data-stu-id="cd106-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="cd106-431">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="cd106-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="cd106-432">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="cd106-433">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="cd106-433">Cost element</span></span></th>
<th><span data-ttu-id="cd106-434">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="cd106-434">Cost behavior</span></span></th>
<th><span data-ttu-id="cd106-435">Upphæð</span><span class="sxs-lookup"><span data-stu-id="cd106-435">Amount</span></span></th>
<th><span data-ttu-id="cd106-436">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="cd106-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="cd106-437">CC0001</span></span></td>
<td><span data-ttu-id="cd106-438">Mannauður</span><span class="sxs-lookup"><span data-stu-id="cd106-438">HR</span></span></td>
<td><span data-ttu-id="cd106-439">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-439">10001</span></span></td>
<td><span data-ttu-id="cd106-440">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-440">Electricity</span></span></td>
<td><span data-ttu-id="cd106-441">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-441">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="cd106-442">-30.00</span></span></td>
<td><span data-ttu-id="cd106-443">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-444">Verk 1</span><span class="sxs-lookup"><span data-stu-id="cd106-444">Proj 1</span></span></td>
<td><span data-ttu-id="cd106-445">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="cd106-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="cd106-446">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-446">10001</span></span></td>
<td><span data-ttu-id="cd106-447">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-447">Electricity</span></span></td>
<td><span data-ttu-id="cd106-448">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-448">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-449">30,00</span><span class="sxs-lookup"><span data-stu-id="cd106-449">30.00</span></span></td>
<td><span data-ttu-id="cd106-450">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-451">CC001</span><span class="sxs-lookup"><span data-stu-id="cd106-451">CC001</span></span></td>
<td><span data-ttu-id="cd106-452">Mannauður</span><span class="sxs-lookup"><span data-stu-id="cd106-452">HR</span></span></td>
<td><span data-ttu-id="cd106-453">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-453">10001</span></span></td>
<td><span data-ttu-id="cd106-454">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-454">Electricity</span></span></td>
<td><span data-ttu-id="cd106-455">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-455">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="cd106-456">-10.00</span></span></td>
<td><span data-ttu-id="cd106-457">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-458">Verk 2</span><span class="sxs-lookup"><span data-stu-id="cd106-458">Proj 2</span></span></td>
<td><span data-ttu-id="cd106-459">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="cd106-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="cd106-460">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-460">10001</span></span></td>
<td><span data-ttu-id="cd106-461">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-461">Electricity</span></span></td>
<td><span data-ttu-id="cd106-462">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-462">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-463">10,00</span><span class="sxs-lookup"><span data-stu-id="cd106-463">10.00</span></span></td>
<td><span data-ttu-id="cd106-464">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cd106-465">Nánari upplýsingar er að finna í [Framkvæma útreikning fastakostnaðar](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="cd106-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="cd106-466">Skref 4: Keyra útreikning kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="cd106-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="cd106-467">Úthlutun er notuð til að úthluta stöðu kostnaðarhlutar í öðrum kostnaðarhlutum með því að nota úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="cd106-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="cd106-468">Finance styður gagnvirka úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="cd106-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="cd106-469">Í gagnvirkri úthlutunaraðferð er sú sameiginlega þjónusta sem hjálparkostnaðarhlutir skiptast á viðurkennd að fullu.</span><span class="sxs-lookup"><span data-stu-id="cd106-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="cd106-470">Kerfið ákvarðar sjálfkrafa rétta röð til að framkvæma úthlutun eftir.</span><span class="sxs-lookup"><span data-stu-id="cd106-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="cd106-471">Stöðu kostnaðarhluta er úthlutað með einum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="cd106-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="cd106-472">Úthlutanir þvert á víddir kostnaðarhluta og viðkomandi stök þeirra eru studdar.</span><span class="sxs-lookup"><span data-stu-id="cd106-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="cd106-473">Úthlutun pöntunarinnar er stjórnað af stýrieiningu kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="cd106-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="cd106-474">[![Gagnkvæm aðferð](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="cd106-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="cd106-475">Tilgreinið kostnaðarúthlutun</span><span class="sxs-lookup"><span data-stu-id="cd106-475">Define the cost allocation</span></span>

<span data-ttu-id="cd106-476">Hér er einfalt dæmi sem útskýrir hvernig hægt er að rekja flæði kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="cd106-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="cd106-477">Kostnaðarhlutir CC001 Mannauður leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="cd106-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="cd106-478">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="cd106-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="cd106-479">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-479">Cost object</span></span></th>
<th><span data-ttu-id="cd106-480">Mannauðsþjónusta</span><span class="sxs-lookup"><span data-stu-id="cd106-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-481">CC002</span><span class="sxs-lookup"><span data-stu-id="cd106-481">CC002</span></span></td>
<td><span data-ttu-id="cd106-482">Fjármál</span><span class="sxs-lookup"><span data-stu-id="cd106-482">Finance</span></span></td>
<td><span data-ttu-id="cd106-483">35</span><span class="sxs-lookup"><span data-stu-id="cd106-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-484">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-484">CC003</span></span></td>
<td><span data-ttu-id="cd106-485">Smölun</span><span class="sxs-lookup"><span data-stu-id="cd106-485">Assembly</span></span></td>
<td><span data-ttu-id="cd106-486">55</span><span class="sxs-lookup"><span data-stu-id="cd106-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-487">CC004</span><span class="sxs-lookup"><span data-stu-id="cd106-487">CC004</span></span></td>
<td><span data-ttu-id="cd106-488">Pakkning</span><span class="sxs-lookup"><span data-stu-id="cd106-488">Packaging</span></span></td>
<td><span data-ttu-id="cd106-489">10</span><span class="sxs-lookup"><span data-stu-id="cd106-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cd106-490">Kostnaðarhlutir CC002 Fjármál leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="cd106-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="cd106-491">Stofnað er tölfræðilegt víddarstak sem kallast Fjármálaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="cd106-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="cd106-492">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-492">Cost object</span></span></th>
<th><span data-ttu-id="cd106-493">Fjármálaþjónusta</span><span class="sxs-lookup"><span data-stu-id="cd106-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-494">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-494">CC003</span></span></td>
<td><span data-ttu-id="cd106-495">Smölun</span><span class="sxs-lookup"><span data-stu-id="cd106-495">Assembly</span></span></td>
<td><span data-ttu-id="cd106-496">65</span><span class="sxs-lookup"><span data-stu-id="cd106-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-497">CC004</span><span class="sxs-lookup"><span data-stu-id="cd106-497">CC004</span></span></td>
<td><span data-ttu-id="cd106-498">Pakkning</span><span class="sxs-lookup"><span data-stu-id="cd106-498">Packaging</span></span></td>
<td><span data-ttu-id="cd106-499">35</span><span class="sxs-lookup"><span data-stu-id="cd106-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cd106-500">Kostnaðarhlutir CC003 Samsetning leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="cd106-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="cd106-501">Meðlimur tölfræðilega víddar sem kallast Mannauður verk er stofnað til að mælvíddarstaka notuðum magnitude.</span><span class="sxs-lookup"><span data-stu-id="cd106-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="cd106-502">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-502">Cost object</span></span></th>
<th><span data-ttu-id="cd106-503">Samsetningarþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="cd106-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-504">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-504">Prod 1</span></span></td>
<td><span data-ttu-id="cd106-505">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-505">Product 1</span></span></td>
<td><span data-ttu-id="cd106-506">60</span><span class="sxs-lookup"><span data-stu-id="cd106-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-507">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-507">Prod 2</span></span></td>
<td><span data-ttu-id="cd106-508">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-508">Product 2</span></span></td>
<td><span data-ttu-id="cd106-509">20</span><span class="sxs-lookup"><span data-stu-id="cd106-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cd106-510">Kostnaðarhlutir CC004 Umbúðir leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="cd106-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="cd106-511">Stofnað er tölfræðilegt víddarstak sem kallast Umbúðaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="cd106-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="cd106-512">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-512">Cost object</span></span></th>
<th><span data-ttu-id="cd106-513">Umbúðaþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="cd106-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-514">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-514">Prod 1</span></span></td>
<td><span data-ttu-id="cd106-515">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-515">Product 1</span></span></td>
<td><span data-ttu-id="cd106-516">80</span><span class="sxs-lookup"><span data-stu-id="cd106-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-517">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-517">Prod 2</span></span></td>
<td><span data-ttu-id="cd106-518">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-518">Product 2</span></span></td>
<td><span data-ttu-id="cd106-519">15</span><span class="sxs-lookup"><span data-stu-id="cd106-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="cd106-520">Hægt er að afleiða tölfræðiaðgerðir eins og framleiðslutíma sem vara notar frá upprunagögnum.</span><span class="sxs-lookup"><span data-stu-id="cd106-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="cd106-521">Nánari upplýsingar er að finna í [Veitusniðmát tölfræðiaðgerðar](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="cd106-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="cd106-522">Eftirfarandi tafla sýnir niðurstöður þegar mannauðsþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="cd106-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="cd106-523">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-523">Cost object</span></span></th>
<th><span data-ttu-id="cd106-524">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="cd106-524">Magnitude</span></span></th>
<th><span data-ttu-id="cd106-525">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="cd106-525">Allocation factor</span></span></th>
<th><span data-ttu-id="cd106-526">Upphæð</span><span class="sxs-lookup"><span data-stu-id="cd106-526">Amount</span></span></th>
<th><span data-ttu-id="cd106-527">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="cd106-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-528">CC002</span><span class="sxs-lookup"><span data-stu-id="cd106-528">CC002</span></span></td>
<td><span data-ttu-id="cd106-529">Fjármál</span><span class="sxs-lookup"><span data-stu-id="cd106-529">Finance</span></span></td>
<td><span data-ttu-id="cd106-530">35</span><span class="sxs-lookup"><span data-stu-id="cd106-530">35</span></span></td>
<td><span data-ttu-id="cd106-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="cd106-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="cd106-532">175.00</span><span class="sxs-lookup"><span data-stu-id="cd106-532">175.00</span></span></td>
<td><span data-ttu-id="cd106-533">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-534">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-534">CC003</span></span></td>
<td><span data-ttu-id="cd106-535">Smölun</span><span class="sxs-lookup"><span data-stu-id="cd106-535">Assembly</span></span></td>
<td><span data-ttu-id="cd106-536">55</span><span class="sxs-lookup"><span data-stu-id="cd106-536">55</span></span></td>
<td><span data-ttu-id="cd106-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="cd106-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="cd106-538">275.00</span><span class="sxs-lookup"><span data-stu-id="cd106-538">275.00</span></span></td>
<td><span data-ttu-id="cd106-539">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-540">CC004</span><span class="sxs-lookup"><span data-stu-id="cd106-540">CC004</span></span></td>
<td><span data-ttu-id="cd106-541">Pakkning</span><span class="sxs-lookup"><span data-stu-id="cd106-541">Packaging</span></span></td>
<td><span data-ttu-id="cd106-542">10</span><span class="sxs-lookup"><span data-stu-id="cd106-542">10</span></span></td>
<td><span data-ttu-id="cd106-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="cd106-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="cd106-544">50,00</span><span class="sxs-lookup"><span data-stu-id="cd106-544">50.00</span></span></td>
<td><span data-ttu-id="cd106-545">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-546">CC002</span><span class="sxs-lookup"><span data-stu-id="cd106-546">CC002</span></span></td>
<td><span data-ttu-id="cd106-547">Fjármál</span><span class="sxs-lookup"><span data-stu-id="cd106-547">Finance</span></span></td>
<td><span data-ttu-id="cd106-548">35</span><span class="sxs-lookup"><span data-stu-id="cd106-548">35</span></span></td>
<td><span data-ttu-id="cd106-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="cd106-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="cd106-550">436.00</span><span class="sxs-lookup"><span data-stu-id="cd106-550">436.00</span></span></td>
<td><span data-ttu-id="cd106-551">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-552">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-552">CC003</span></span></td>
<td><span data-ttu-id="cd106-553">Smölun</span><span class="sxs-lookup"><span data-stu-id="cd106-553">Assembly</span></span></td>
<td><span data-ttu-id="cd106-554">55</span><span class="sxs-lookup"><span data-stu-id="cd106-554">55</span></span></td>
<td><span data-ttu-id="cd106-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="cd106-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="cd106-556">685.14</span><span class="sxs-lookup"><span data-stu-id="cd106-556">685.14</span></span></td>
<td><span data-ttu-id="cd106-557">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-558">CC004</span><span class="sxs-lookup"><span data-stu-id="cd106-558">CC004</span></span></td>
<td><span data-ttu-id="cd106-559">Pakkning</span><span class="sxs-lookup"><span data-stu-id="cd106-559">Packaging</span></span></td>
<td><span data-ttu-id="cd106-560">10</span><span class="sxs-lookup"><span data-stu-id="cd106-560">10</span></span></td>
<td><span data-ttu-id="cd106-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="cd106-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="cd106-562">124.57</span><span class="sxs-lookup"><span data-stu-id="cd106-562">124.57</span></span></td>
<td><span data-ttu-id="cd106-563">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cd106-564">Eftirfarandi tafla sýnir niðurstöður þegar Fjármálaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="cd106-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="cd106-565">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-565">Cost object</span></span></th>
<th><span data-ttu-id="cd106-566">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="cd106-566">Magnitude</span></span></th>
<th><span data-ttu-id="cd106-567">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="cd106-567">Allocation factor</span></span></th>
<th><span data-ttu-id="cd106-568">Upphæð</span><span class="sxs-lookup"><span data-stu-id="cd106-568">Amount</span></span></th>
<th><span data-ttu-id="cd106-569">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="cd106-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-570">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-570">CC003</span></span></td>
<td><span data-ttu-id="cd106-571">Smölun</span><span class="sxs-lookup"><span data-stu-id="cd106-571">Assembly</span></span></td>
<td><span data-ttu-id="cd106-572">65</span><span class="sxs-lookup"><span data-stu-id="cd106-572">65</span></span></td>
<td><span data-ttu-id="cd106-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="cd106-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="cd106-574">438.75</span><span class="sxs-lookup"><span data-stu-id="cd106-574">438.75</span></span></td>
<td><span data-ttu-id="cd106-575">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-576">CC004</span><span class="sxs-lookup"><span data-stu-id="cd106-576">CC004</span></span></td>
<td><span data-ttu-id="cd106-577">Pakkning</span><span class="sxs-lookup"><span data-stu-id="cd106-577">Packaging</span></span></td>
<td><span data-ttu-id="cd106-578">35</span><span class="sxs-lookup"><span data-stu-id="cd106-578">35</span></span></td>
<td><span data-ttu-id="cd106-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="cd106-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="cd106-580">236.25</span><span class="sxs-lookup"><span data-stu-id="cd106-580">236.25</span></span></td>
<td><span data-ttu-id="cd106-581">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-582">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-582">CC003</span></span></td>
<td><span data-ttu-id="cd106-583">Smölun</span><span class="sxs-lookup"><span data-stu-id="cd106-583">Assembly</span></span></td>
<td><span data-ttu-id="cd106-584">65</span><span class="sxs-lookup"><span data-stu-id="cd106-584">65</span></span></td>
<td><span data-ttu-id="cd106-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="cd106-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="cd106-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="cd106-586">5,297.69</span></span></td>
<td><span data-ttu-id="cd106-587">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-588">CC004</span><span class="sxs-lookup"><span data-stu-id="cd106-588">CC004</span></span></td>
<td><span data-ttu-id="cd106-589">Pakkning</span><span class="sxs-lookup"><span data-stu-id="cd106-589">Packaging</span></span></td>
<td><span data-ttu-id="cd106-590">35</span><span class="sxs-lookup"><span data-stu-id="cd106-590">35</span></span></td>
<td><span data-ttu-id="cd106-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="cd106-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="cd106-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="cd106-592">2,852.60</span></span></td>
<td><span data-ttu-id="cd106-593">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cd106-594">Eftirfarandi tafla sýnir niðurstöður þegar Samsetningarþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="cd106-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="cd106-595">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-595">Cost object</span></span></th>
<th><span data-ttu-id="cd106-596">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="cd106-596">Magnitude</span></span></th>
<th><span data-ttu-id="cd106-597">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="cd106-597">Allocation factor</span></span></th>
<th><span data-ttu-id="cd106-598">Upphæð</span><span class="sxs-lookup"><span data-stu-id="cd106-598">Amount</span></span></th>
<th><span data-ttu-id="cd106-599">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="cd106-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-600">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-600">Prod 1</span></span></td>
<td><span data-ttu-id="cd106-601">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-601">Product 1</span></span></td>
<td><span data-ttu-id="cd106-602">60</span><span class="sxs-lookup"><span data-stu-id="cd106-602">60</span></span></td>
<td><span data-ttu-id="cd106-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="cd106-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="cd106-604">535.31</span><span class="sxs-lookup"><span data-stu-id="cd106-604">535.31</span></span></td>
<td><span data-ttu-id="cd106-605">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-606">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-606">Prod 2</span></span></td>
<td><span data-ttu-id="cd106-607">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-607">Product 2</span></span></td>
<td><span data-ttu-id="cd106-608">20</span><span class="sxs-lookup"><span data-stu-id="cd106-608">20</span></span></td>
<td><span data-ttu-id="cd106-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="cd106-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="cd106-610">178.44</span><span class="sxs-lookup"><span data-stu-id="cd106-610">178.44</span></span></td>
<td><span data-ttu-id="cd106-611">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-612">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-612">Prod 1</span></span></td>
<td><span data-ttu-id="cd106-613">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-613">Product 1</span></span></td>
<td><span data-ttu-id="cd106-614">60</span><span class="sxs-lookup"><span data-stu-id="cd106-614">60</span></span></td>
<td><span data-ttu-id="cd106-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="cd106-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="cd106-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="cd106-616">4,487.12</span></span></td>
<td><span data-ttu-id="cd106-617">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-618">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-618">Prod 2</span></span></td>
<td><span data-ttu-id="cd106-619">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-619">Product 2</span></span></td>
<td><span data-ttu-id="cd106-620">20</span><span class="sxs-lookup"><span data-stu-id="cd106-620">20</span></span></td>
<td><span data-ttu-id="cd106-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="cd106-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="cd106-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="cd106-622">1,495.71</span></span></td>
<td><span data-ttu-id="cd106-623">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="cd106-624">Eftirfarandi tafla sýnir niðurstöður þegar Umbúðaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="cd106-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="cd106-625">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-625">Cost object</span></span></th>
<th><span data-ttu-id="cd106-626">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="cd106-626">Magnitude</span></span></th>
<th><span data-ttu-id="cd106-627">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="cd106-627">Allocation factor</span></span></th>
<th><span data-ttu-id="cd106-628">Upphæð</span><span class="sxs-lookup"><span data-stu-id="cd106-628">Amount</span></span></th>
<th><span data-ttu-id="cd106-629">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="cd106-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-630">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-630">Prod 1</span></span></td>
<td><span data-ttu-id="cd106-631">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-631">Product 1</span></span></td>
<td><span data-ttu-id="cd106-632">80</span><span class="sxs-lookup"><span data-stu-id="cd106-632">80</span></span></td>
<td><span data-ttu-id="cd106-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="cd106-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="cd106-634">241.05</span><span class="sxs-lookup"><span data-stu-id="cd106-634">241.05</span></span></td>
<td><span data-ttu-id="cd106-635">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-636">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-636">Prod 2</span></span></td>
<td><span data-ttu-id="cd106-637">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-637">Product 2</span></span></td>
<td><span data-ttu-id="cd106-638">15</span><span class="sxs-lookup"><span data-stu-id="cd106-638">15</span></span></td>
<td><span data-ttu-id="cd106-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="cd106-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="cd106-640">45.20</span><span class="sxs-lookup"><span data-stu-id="cd106-640">45.20</span></span></td>
<td><span data-ttu-id="cd106-641">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-642">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-642">Prod 1</span></span></td>
<td><span data-ttu-id="cd106-643">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-643">Product 1</span></span></td>
<td><span data-ttu-id="cd106-644">80</span><span class="sxs-lookup"><span data-stu-id="cd106-644">80</span></span></td>
<td><span data-ttu-id="cd106-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="cd106-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="cd106-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="cd106-646">2,507.09</span></span></td>
<td><span data-ttu-id="cd106-647">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-648">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-648">Prod 2</span></span></td>
<td><span data-ttu-id="cd106-649">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-649">Product 2</span></span></td>
<td><span data-ttu-id="cd106-650">15</span><span class="sxs-lookup"><span data-stu-id="cd106-650">15</span></span></td>
<td><span data-ttu-id="cd106-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="cd106-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="cd106-652">470.08</span><span class="sxs-lookup"><span data-stu-id="cd106-652">470.08</span></span></td>
<td><span data-ttu-id="cd106-653">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="cd106-654">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="cd106-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="cd106-655">Færslubók</span><span class="sxs-lookup"><span data-stu-id="cd106-655">Journal</span></span></th>
<th><span data-ttu-id="cd106-656">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="cd106-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="cd106-657">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="cd106-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="cd106-658">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="cd106-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-659">00004</span><span class="sxs-lookup"><span data-stu-id="cd106-659">00004</span></span></td>
<td><span data-ttu-id="cd106-660">Færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="cd106-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="cd106-661">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="cd106-661">Fiscal</span></span></td>
<td><span data-ttu-id="cd106-662">2017</span><span class="sxs-lookup"><span data-stu-id="cd106-662">2017</span></span></td>
<td><span data-ttu-id="cd106-663">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="cd106-663">Period 1</span></span></td>
<td><span data-ttu-id="cd106-664">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="cd106-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="cd106-665">Færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="cd106-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="cd106-666">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="cd106-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="cd106-667">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="cd106-668">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="cd106-668">Cost element</span></span></th>
<th><span data-ttu-id="cd106-669">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="cd106-669">Cost behavior</span></span></th>
<th><span data-ttu-id="cd106-670">Upphæð</span><span class="sxs-lookup"><span data-stu-id="cd106-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-671">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="cd106-672">CC001</span><span class="sxs-lookup"><span data-stu-id="cd106-672">CC001</span></span></td>
<td><span data-ttu-id="cd106-673">Mannauður</span><span class="sxs-lookup"><span data-stu-id="cd106-673">HR</span></span></td>
<td><span data-ttu-id="cd106-674">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-674">10001</span></span></td>
<td><span data-ttu-id="cd106-675">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-675">Electricity</span></span></td>
<td><span data-ttu-id="cd106-676">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-676">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-677">500,00</span><span class="sxs-lookup"><span data-stu-id="cd106-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-678">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="cd106-679">CC001</span><span class="sxs-lookup"><span data-stu-id="cd106-679">CC001</span></span></td>
<td><span data-ttu-id="cd106-680">Mannauður</span><span class="sxs-lookup"><span data-stu-id="cd106-680">HR</span></span></td>
<td><span data-ttu-id="cd106-681">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-681">10001</span></span></td>
<td><span data-ttu-id="cd106-682">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-682">Electricity</span></span></td>
<td><span data-ttu-id="cd106-683">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-683">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="cd106-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-685">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="cd106-686">CC002</span><span class="sxs-lookup"><span data-stu-id="cd106-686">CC002</span></span></td>
<td><span data-ttu-id="cd106-687">Fjármál</span><span class="sxs-lookup"><span data-stu-id="cd106-687">Finance</span></span></td>
<td><span data-ttu-id="cd106-688">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-688">10001</span></span></td>
<td><span data-ttu-id="cd106-689">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-689">Electricity</span></span></td>
<td><span data-ttu-id="cd106-690">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-690">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-691">675.00</span><span class="sxs-lookup"><span data-stu-id="cd106-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-692">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="cd106-693">CC002</span><span class="sxs-lookup"><span data-stu-id="cd106-693">CC002</span></span></td>
<td><span data-ttu-id="cd106-694">Fjármál</span><span class="sxs-lookup"><span data-stu-id="cd106-694">Finance</span></span></td>
<td><span data-ttu-id="cd106-695">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-695">10001</span></span></td>
<td><span data-ttu-id="cd106-696">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-696">Electricity</span></span></td>
<td><span data-ttu-id="cd106-697">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-697">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="cd106-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-699">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="cd106-700">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-700">CC003</span></span></td>
<td><span data-ttu-id="cd106-701">Smölun</span><span class="sxs-lookup"><span data-stu-id="cd106-701">Assembly</span></span></td>
<td><span data-ttu-id="cd106-702">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-702">10001</span></span></td>
<td><span data-ttu-id="cd106-703">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-703">Electricity</span></span></td>
<td><span data-ttu-id="cd106-704">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-704">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-705">713.75</span><span class="sxs-lookup"><span data-stu-id="cd106-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-706">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="cd106-707">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-707">CC003</span></span></td>
<td><span data-ttu-id="cd106-708">Smölun</span><span class="sxs-lookup"><span data-stu-id="cd106-708">Assembly</span></span></td>
<td><span data-ttu-id="cd106-709">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-709">10001</span></span></td>
<td><span data-ttu-id="cd106-710">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-710">Electricity</span></span></td>
<td><span data-ttu-id="cd106-711">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-711">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="cd106-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-713">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="cd106-714">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-714">CC003</span></span></td>
<td><span data-ttu-id="cd106-715">Pakkning</span><span class="sxs-lookup"><span data-stu-id="cd106-715">Packaging</span></span></td>
<td><span data-ttu-id="cd106-716">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-716">10001</span></span></td>
<td><span data-ttu-id="cd106-717">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-717">Electricity</span></span></td>
<td><span data-ttu-id="cd106-718">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-718">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-719">286.25</span><span class="sxs-lookup"><span data-stu-id="cd106-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-720">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="cd106-721">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-721">CC003</span></span></td>
<td><span data-ttu-id="cd106-722">Pakkning</span><span class="sxs-lookup"><span data-stu-id="cd106-722">Packaging</span></span></td>
<td><span data-ttu-id="cd106-723">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-723">10001</span></span></td>
<td><span data-ttu-id="cd106-724">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-724">Electricity</span></span></td>
<td><span data-ttu-id="cd106-725">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-725">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="cd106-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-727">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="cd106-728">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-728">Prod 1</span></span></td>
<td><span data-ttu-id="cd106-729">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-729">Product 1</span></span></td>
<td><span data-ttu-id="cd106-730">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-730">10001</span></span></td>
<td><span data-ttu-id="cd106-731">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-731">Electricity</span></span></td>
<td><span data-ttu-id="cd106-732">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-732">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-733">776.36</span><span class="sxs-lookup"><span data-stu-id="cd106-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-734">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="cd106-735">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-735">Prod 1</span></span></td>
<td><span data-ttu-id="cd106-736">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-736">Product 1</span></span></td>
<td><span data-ttu-id="cd106-737">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-737">10001</span></span></td>
<td><span data-ttu-id="cd106-738">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-738">Electricity</span></span></td>
<td><span data-ttu-id="cd106-739">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-739">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="cd106-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-741">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="cd106-742">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-742">Prod 2</span></span></td>
<td><span data-ttu-id="cd106-743">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-743">Product 1</span></span></td>
<td><span data-ttu-id="cd106-744">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-744">10001</span></span></td>
<td><span data-ttu-id="cd106-745">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-745">Electricity</span></span></td>
<td><span data-ttu-id="cd106-746">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-746">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-747">223.64</span><span class="sxs-lookup"><span data-stu-id="cd106-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-748">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="cd106-749">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-749">Prod 2</span></span></td>
<td><span data-ttu-id="cd106-750">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-750">Product 1</span></span></td>
<td><span data-ttu-id="cd106-751">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-751">10001</span></span></td>
<td><span data-ttu-id="cd106-752">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-752">Electricity</span></span></td>
<td><span data-ttu-id="cd106-753">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-753">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="cd106-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="cd106-755">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="cd106-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="cd106-756">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="cd106-757">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="cd106-757">Cost element</span></span></th>
<th><span data-ttu-id="cd106-758">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="cd106-758">Cost behavior</span></span></th>
<th><span data-ttu-id="cd106-759">Upphæð</span><span class="sxs-lookup"><span data-stu-id="cd106-759">Amount</span></span></th>
<th><span data-ttu-id="cd106-760">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="cd106-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="cd106-761">CC001</span><span class="sxs-lookup"><span data-stu-id="cd106-761">CC001</span></span></td>
<td><span data-ttu-id="cd106-762">Mannauður</span><span class="sxs-lookup"><span data-stu-id="cd106-762">HR</span></span></td>
<td><span data-ttu-id="cd106-763">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-763">10001</span></span></td>
<td><span data-ttu-id="cd106-764">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-764">Electricity</span></span></td>
<td><span data-ttu-id="cd106-765">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-765">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="cd106-766">-500.00</span></span></td>
<td><span data-ttu-id="cd106-767">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-768">CC002</span><span class="sxs-lookup"><span data-stu-id="cd106-768">CC002</span></span></td>
<td><span data-ttu-id="cd106-769">Fjármál</span><span class="sxs-lookup"><span data-stu-id="cd106-769">Finance</span></span></td>
<td><span data-ttu-id="cd106-770">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-770">10001</span></span></td>
<td><span data-ttu-id="cd106-771">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-771">Electricity</span></span></td>
<td><span data-ttu-id="cd106-772">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-772">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-773">175.00</span><span class="sxs-lookup"><span data-stu-id="cd106-773">175.00</span></span></td>
<td><span data-ttu-id="cd106-774">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-775">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-775">CC003</span></span></td>
<td><span data-ttu-id="cd106-776">Smölun</span><span class="sxs-lookup"><span data-stu-id="cd106-776">Assembly</span></span></td>
<td><span data-ttu-id="cd106-777">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-777">10001</span></span></td>
<td><span data-ttu-id="cd106-778">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-778">Electricity</span></span></td>
<td><span data-ttu-id="cd106-779">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-779">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-780">275.00</span><span class="sxs-lookup"><span data-stu-id="cd106-780">275.00</span></span></td>
<td><span data-ttu-id="cd106-781">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-782">CC004</span><span class="sxs-lookup"><span data-stu-id="cd106-782">CC004</span></span></td>
<td><span data-ttu-id="cd106-783">Pakkning</span><span class="sxs-lookup"><span data-stu-id="cd106-783">Packaging</span></span></td>
<td><span data-ttu-id="cd106-784">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-784">10001</span></span></td>
<td><span data-ttu-id="cd106-785">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-785">Electricity</span></span></td>
<td><span data-ttu-id="cd106-786">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-786">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-787">50,00</span><span class="sxs-lookup"><span data-stu-id="cd106-787">50,00</span></span></td>
<td><span data-ttu-id="cd106-788">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-789">CC001</span><span class="sxs-lookup"><span data-stu-id="cd106-789">CC001</span></span></td>
<td><span data-ttu-id="cd106-790">Mannauður</span><span class="sxs-lookup"><span data-stu-id="cd106-790">HR</span></span></td>
<td><span data-ttu-id="cd106-791">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-791">10001</span></span></td>
<td><span data-ttu-id="cd106-792">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-792">Electricity</span></span></td>
<td><span data-ttu-id="cd106-793">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-793">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="cd106-794">-1,245.71</span></span></td>
<td><span data-ttu-id="cd106-795">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-796">CC002</span><span class="sxs-lookup"><span data-stu-id="cd106-796">CC002</span></span></td>
<td><span data-ttu-id="cd106-797">Fjármál</span><span class="sxs-lookup"><span data-stu-id="cd106-797">Finance</span></span></td>
<td><span data-ttu-id="cd106-798">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-798">10001</span></span></td>
<td><span data-ttu-id="cd106-799">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-799">Electricity</span></span></td>
<td><span data-ttu-id="cd106-800">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-800">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-801">436.00</span><span class="sxs-lookup"><span data-stu-id="cd106-801">436.00</span></span></td>
<td><span data-ttu-id="cd106-802">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-803">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-803">CC003</span></span></td>
<td><span data-ttu-id="cd106-804">Smölun</span><span class="sxs-lookup"><span data-stu-id="cd106-804">Assembly</span></span></td>
<td><span data-ttu-id="cd106-805">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-805">10001</span></span></td>
<td><span data-ttu-id="cd106-806">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-806">Electricity</span></span></td>
<td><span data-ttu-id="cd106-807">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-807">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-808">685.14</span><span class="sxs-lookup"><span data-stu-id="cd106-808">685.14</span></span></td>
<td><span data-ttu-id="cd106-809">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-810">CC004</span><span class="sxs-lookup"><span data-stu-id="cd106-810">CC004</span></span></td>
<td><span data-ttu-id="cd106-811">Pakkning</span><span class="sxs-lookup"><span data-stu-id="cd106-811">Packaging</span></span></td>
<td><span data-ttu-id="cd106-812">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-812">10001</span></span></td>
<td><span data-ttu-id="cd106-813">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-813">Electricity</span></span></td>
<td><span data-ttu-id="cd106-814">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-814">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-815">124.57</span><span class="sxs-lookup"><span data-stu-id="cd106-815">124.57</span></span></td>
<td><span data-ttu-id="cd106-816">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-817">CC002</span><span class="sxs-lookup"><span data-stu-id="cd106-817">CC002</span></span></td>
<td><span data-ttu-id="cd106-818">Fjármál</span><span class="sxs-lookup"><span data-stu-id="cd106-818">Finance</span></span></td>
<td><span data-ttu-id="cd106-819">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-819">10001</span></span></td>
<td><span data-ttu-id="cd106-820">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-820">Electricity</span></span></td>
<td><span data-ttu-id="cd106-821">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-821">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="cd106-822">-675.00</span></span></td>
<td><span data-ttu-id="cd106-823">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-824">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-824">CC003</span></span></td>
<td><span data-ttu-id="cd106-825">Smölun</span><span class="sxs-lookup"><span data-stu-id="cd106-825">Assembly</span></span></td>
<td><span data-ttu-id="cd106-826">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-826">10001</span></span></td>
<td><span data-ttu-id="cd106-827">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-827">Electricity</span></span></td>
<td><span data-ttu-id="cd106-828">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-828">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-829">438.75</span><span class="sxs-lookup"><span data-stu-id="cd106-829">438.75</span></span></td>
<td><span data-ttu-id="cd106-830">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-831">CC004</span><span class="sxs-lookup"><span data-stu-id="cd106-831">CC004</span></span></td>
<td><span data-ttu-id="cd106-832">Pakkning</span><span class="sxs-lookup"><span data-stu-id="cd106-832">Packaging</span></span></td>
<td><span data-ttu-id="cd106-833">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-833">10001</span></span></td>
<td><span data-ttu-id="cd106-834">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-834">Electricity</span></span></td>
<td><span data-ttu-id="cd106-835">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-835">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-836">236.25</span><span class="sxs-lookup"><span data-stu-id="cd106-836">236.25</span></span></td>
<td><span data-ttu-id="cd106-837">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-838">CC002</span><span class="sxs-lookup"><span data-stu-id="cd106-838">CC002</span></span></td>
<td><span data-ttu-id="cd106-839">Fjármál</span><span class="sxs-lookup"><span data-stu-id="cd106-839">Finance</span></span></td>
<td><span data-ttu-id="cd106-840">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-840">10001</span></span></td>
<td><span data-ttu-id="cd106-841">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-841">Electricity</span></span></td>
<td><span data-ttu-id="cd106-842">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-842">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="cd106-843">-8,150.29</span></span></td>
<td><span data-ttu-id="cd106-844">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-845">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-845">CC003</span></span></td>
<td><span data-ttu-id="cd106-846">Smölun</span><span class="sxs-lookup"><span data-stu-id="cd106-846">Assembly</span></span></td>
<td><span data-ttu-id="cd106-847">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-847">10001</span></span></td>
<td><span data-ttu-id="cd106-848">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-848">Electricity</span></span></td>
<td><span data-ttu-id="cd106-849">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-849">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="cd106-850">5,297.69</span></span></td>
<td><span data-ttu-id="cd106-851">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-852">CC004</span><span class="sxs-lookup"><span data-stu-id="cd106-852">CC004</span></span></td>
<td><span data-ttu-id="cd106-853">Pakkning</span><span class="sxs-lookup"><span data-stu-id="cd106-853">Packaging</span></span></td>
<td><span data-ttu-id="cd106-854">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-854">10001</span></span></td>
<td><span data-ttu-id="cd106-855">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-855">Electricity</span></span></td>
<td><span data-ttu-id="cd106-856">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-856">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="cd106-857">2,852.60</span></span></td>
<td><span data-ttu-id="cd106-858">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-859">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-859">CC003</span></span></td>
<td><span data-ttu-id="cd106-860">Smölun</span><span class="sxs-lookup"><span data-stu-id="cd106-860">Assembly</span></span></td>
<td><span data-ttu-id="cd106-861">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-861">10001</span></span></td>
<td><span data-ttu-id="cd106-862">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-862">Electricity</span></span></td>
<td><span data-ttu-id="cd106-863">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-863">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="cd106-864">-713.75</span></span></td>
<td><span data-ttu-id="cd106-865">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-866">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-866">Prod 1</span></span></td>
<td><span data-ttu-id="cd106-867">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-867">Product 1</span></span></td>
<td><span data-ttu-id="cd106-868">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-868">10001</span></span></td>
<td><span data-ttu-id="cd106-869">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-869">Electricity</span></span></td>
<td><span data-ttu-id="cd106-870">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-870">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-871">535.31</span><span class="sxs-lookup"><span data-stu-id="cd106-871">535.31</span></span></td>
<td><span data-ttu-id="cd106-872">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-873">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-873">Prod 2</span></span></td>
<td><span data-ttu-id="cd106-874">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-874">Product 2</span></span></td>
<td><span data-ttu-id="cd106-875">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-875">10001</span></span></td>
<td><span data-ttu-id="cd106-876">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-876">Electricity</span></span></td>
<td><span data-ttu-id="cd106-877">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-877">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-878">178.44</span><span class="sxs-lookup"><span data-stu-id="cd106-878">178.44</span></span></td>
<td><span data-ttu-id="cd106-879">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-880">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-880">CC003</span></span></td>
<td><span data-ttu-id="cd106-881">Smölun</span><span class="sxs-lookup"><span data-stu-id="cd106-881">Assembly</span></span></td>
<td><span data-ttu-id="cd106-882">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-882">10001</span></span></td>
<td><span data-ttu-id="cd106-883">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-883">Electricity</span></span></td>
<td><span data-ttu-id="cd106-884">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-884">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="cd106-885">-5,982.83</span></span></td>
<td><span data-ttu-id="cd106-886">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-887">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-887">Prod 1</span></span></td>
<td><span data-ttu-id="cd106-888">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-888">Product 1</span></span></td>
<td><span data-ttu-id="cd106-889">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-889">10001</span></span></td>
<td><span data-ttu-id="cd106-890">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-890">Electricity</span></span></td>
<td><span data-ttu-id="cd106-891">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-891">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="cd106-892">4,487.12</span></span></td>
<td><span data-ttu-id="cd106-893">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-894">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-894">Prod 2</span></span></td>
<td><span data-ttu-id="cd106-895">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-895">Product 2</span></span></td>
<td><span data-ttu-id="cd106-896">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-896">10001</span></span></td>
<td><span data-ttu-id="cd106-897">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-897">Electricity</span></span></td>
<td><span data-ttu-id="cd106-898">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-898">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="cd106-899">1,495.71</span></span></td>
<td><span data-ttu-id="cd106-900">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-901">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-901">CC003</span></span></td>
<td><span data-ttu-id="cd106-902">Smölun</span><span class="sxs-lookup"><span data-stu-id="cd106-902">Assembly</span></span></td>
<td><span data-ttu-id="cd106-903">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-903">10001</span></span></td>
<td><span data-ttu-id="cd106-904">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-904">Electricity</span></span></td>
<td><span data-ttu-id="cd106-905">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-905">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="cd106-906">-286.25</span></span></td>
<td><span data-ttu-id="cd106-907">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-908">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-908">Prod 1</span></span></td>
<td><span data-ttu-id="cd106-909">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-909">Product 1</span></span></td>
<td><span data-ttu-id="cd106-910">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-910">10001</span></span></td>
<td><span data-ttu-id="cd106-911">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-911">Electricity</span></span></td>
<td><span data-ttu-id="cd106-912">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-912">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-913">241.05</span><span class="sxs-lookup"><span data-stu-id="cd106-913">241.05</span></span></td>
<td><span data-ttu-id="cd106-914">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-915">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-915">Prod 2</span></span></td>
<td><span data-ttu-id="cd106-916">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-916">Product 2</span></span></td>
<td><span data-ttu-id="cd106-917">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-917">10001</span></span></td>
<td><span data-ttu-id="cd106-918">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-918">Electricity</span></span></td>
<td><span data-ttu-id="cd106-919">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-919">Fixed cost</span></span></td>
<td><span data-ttu-id="cd106-920">45.20</span><span class="sxs-lookup"><span data-stu-id="cd106-920">45.20</span></span></td>
<td><span data-ttu-id="cd106-921">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-922">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-922">CC003</span></span></td>
<td><span data-ttu-id="cd106-923">Smölun</span><span class="sxs-lookup"><span data-stu-id="cd106-923">Assembly</span></span></td>
<td><span data-ttu-id="cd106-924">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-924">10001</span></span></td>
<td><span data-ttu-id="cd106-925">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-925">Electricity</span></span></td>
<td><span data-ttu-id="cd106-926">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-926">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="cd106-927">-2,977.17</span></span></td>
<td><span data-ttu-id="cd106-928">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-929">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-929">Prod 1</span></span></td>
<td><span data-ttu-id="cd106-930">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-930">Product 1</span></span></td>
<td><span data-ttu-id="cd106-931">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-931">10001</span></span></td>
<td><span data-ttu-id="cd106-932">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-932">Electricity</span></span></td>
<td><span data-ttu-id="cd106-933">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-933">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="cd106-934">2,507.09</span></span></td>
<td><span data-ttu-id="cd106-935">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="cd106-936">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-936">Prod 2</span></span></td>
<td><span data-ttu-id="cd106-937">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-937">Product 2</span></span></td>
<td><span data-ttu-id="cd106-938">10001</span><span class="sxs-lookup"><span data-stu-id="cd106-938">10001</span></span></td>
<td><span data-ttu-id="cd106-939">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-939">Electricity</span></span></td>
<td><span data-ttu-id="cd106-940">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-940">Variable cost</span></span></td>
<td><span data-ttu-id="cd106-941">470.08</span><span class="sxs-lookup"><span data-stu-id="cd106-941">470.08</span></span></td>
<td><span data-ttu-id="cd106-942">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="cd106-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="cd106-943">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="cd106-943">Conclusion</span></span>
<span data-ttu-id="cd106-944">Í Fjárhagsbókhaldi er kostnaður upp á 10.000,00 fyrir rafmagn bókaður á kenni leppkostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="cd106-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="cd106-945">Þar af leiðandi munu kostnaðarbókarar vita að það þarf að úthluta þessum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="cd106-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="cd106-946">Í kostnaðarbókhaldi streymir kostnaður þvert á fyrirtækiseiningar og stig, samkvæmt þeim stefnum og reglum sem eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="cd106-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="cd106-947">Hver kostnaður hefur verið tengdur úthlutunargrunni sem veitir besta mat á úthlutun á kostnaði.</span><span class="sxs-lookup"><span data-stu-id="cd106-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="cd106-948">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="cd106-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="cd106-949">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="cd106-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="cd106-950">Samtala</span><span class="sxs-lookup"><span data-stu-id="cd106-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="cd106-951">CC099</span><span class="sxs-lookup"><span data-stu-id="cd106-951">CC099</span></span></th>
<th><span data-ttu-id="cd106-952">CC001</span><span class="sxs-lookup"><span data-stu-id="cd106-952">CC001</span></span></th>
<th><span data-ttu-id="cd106-953">CC002</span><span class="sxs-lookup"><span data-stu-id="cd106-953">CC002</span></span></th>
<th><span data-ttu-id="cd106-954">CC003</span><span class="sxs-lookup"><span data-stu-id="cd106-954">CC003</span></span></th>
<th><span data-ttu-id="cd106-955">CC004</span><span class="sxs-lookup"><span data-stu-id="cd106-955">CC004</span></span></th>
<th><span data-ttu-id="cd106-956">Verk 1</span><span class="sxs-lookup"><span data-stu-id="cd106-956">Proj 1</span></span></th>
<th><span data-ttu-id="cd106-957">Verk 2</span><span class="sxs-lookup"><span data-stu-id="cd106-957">Proj 2</span></span></th>
<th><span data-ttu-id="cd106-958">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="cd106-958">Prod 1</span></span></th>
<th><span data-ttu-id="cd106-959">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="cd106-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="cd106-960">10001 Rafmagn</span><span class="sxs-lookup"><span data-stu-id="cd106-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="cd106-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="cd106-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="cd106-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="cd106-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="cd106-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="cd106-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="cd106-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="cd106-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="cd106-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="cd106-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="cd106-970">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="cd106-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-971">0,00</span><span class="sxs-lookup"><span data-stu-id="cd106-971">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="cd106-972">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-973">0,00</span><span class="sxs-lookup"><span data-stu-id="cd106-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-974">0,00</span><span class="sxs-lookup"><span data-stu-id="cd106-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-975">0,00</span><span class="sxs-lookup"><span data-stu-id="cd106-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-976">0,00</span><span class="sxs-lookup"><span data-stu-id="cd106-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-977">0,00</span><span class="sxs-lookup"><span data-stu-id="cd106-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="cd106-978">776.36</span><span class="sxs-lookup"><span data-stu-id="cd106-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-979">223.64</span><span class="sxs-lookup"><span data-stu-id="cd106-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="cd106-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="cd106-981">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="cd106-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-982">000</span><span class="sxs-lookup"><span data-stu-id="cd106-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-983">0,00</span><span class="sxs-lookup"><span data-stu-id="cd106-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-984">0,00</span><span class="sxs-lookup"><span data-stu-id="cd106-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-985">0,00</span><span class="sxs-lookup"><span data-stu-id="cd106-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-986">0,00</span><span class="sxs-lookup"><span data-stu-id="cd106-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-987">30,00</span><span class="sxs-lookup"><span data-stu-id="cd106-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-988">10,00</span><span class="sxs-lookup"><span data-stu-id="cd106-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="cd106-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="cd106-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="cd106-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="cd106-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="cd106-992">Þetta efnisatriði sýnir hvernig fyrir aðalkostnaðareiningin 10001 Rafmagn flæðir í gegnum kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="cd106-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="cd106-993">Þar af leiðandi er þessum sameiginlega kostnaði úthlutað á lægsta stigið í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="cd106-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="cd106-994">Með öðrum orðum bera kostnaðarhlutir á lægsta stiginu kostnaðinn.</span><span class="sxs-lookup"><span data-stu-id="cd106-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="cd106-995">Ef þú þarft sjónrænt flæði kostnaðar á milli kostnaðarhluta er hægt að nota stefnureglur samantekins kostnaðar til að gera kostnaðarflæðið sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="cd106-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="cd106-996">Fyrir frekari upplýsingar skal sjá [Stefna fyrir samantekt kostnaðar og útreikning sameiginlegs kostnaðar](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="cd106-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]