---
title: Útreikningur fastakostnaður
description: Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði.
author: AndersGirke
ms.date: 10/04/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2dddc22128621dc148a253cd568430587f294544
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822904"
---
# <a name="overhead-calculation"></a><span data-ttu-id="7a744-103">Útreikningur fastakostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a744-104">Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði.</span><span class="sxs-lookup"><span data-stu-id="7a744-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="7a744-105">Skýrsluskilgreining</span><span class="sxs-lookup"><span data-stu-id="7a744-105">Term definition</span></span>
---------------

<span data-ttu-id="7a744-106">Stjórnunarkostnaður er sá kostnaður sem stofnað er til fyrir rekstur fyrirtækis, en sem ekki er hægt að rekja beint til neinna sérstakrar starfsemi, vöru eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="7a744-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="7a744-107">Stjórnunarkostnaður veitir mikilvægan stuðning við myndun hagnaðarmyndandi verkþátta.</span><span class="sxs-lookup"><span data-stu-id="7a744-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="7a744-108">Hér eru nokkur dæmi um skilyrði:</span><span class="sxs-lookup"><span data-stu-id="7a744-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="7a744-109">Leiga</span><span class="sxs-lookup"><span data-stu-id="7a744-109">Rent</span></span>
-   <span data-ttu-id="7a744-110">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-110">Electricity</span></span>
-   <span data-ttu-id="7a744-111">Stjórnunarkostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="7a744-112">Yfirlit yfir útreikning fastakostnaðar</span><span class="sxs-lookup"><span data-stu-id="7a744-112">Overhead calculation overview</span></span>
<span data-ttu-id="7a744-113">Útreikningur fastakostnaðar keyrir reglur kostnaðarbókhalds í réttri röð.</span><span class="sxs-lookup"><span data-stu-id="7a744-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="7a744-114">Hægt er að keyra útreikning fastakostnaðar margsinnis fyrir sama fjárhagstímabil ef reglum kostnaðarbókhalds hefur verið breytt eða ákveðnar villur hafa fundist.</span><span class="sxs-lookup"><span data-stu-id="7a744-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="7a744-115">Hver keyrsla á útreikningi fastakostnaðar er geymd og fær einkvæmt útgáfukenni sem gerir kleift að bera saman útreikning í mismunandi útgáfum.</span><span class="sxs-lookup"><span data-stu-id="7a744-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="7a744-116">Kostnaðarfærslur sem útreikningur fastakostnaðar mynda fá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="7a744-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="7a744-117">Dagsetningin bókhald samsvarar lokadagsetning fjárhagstímabilsins sem er dagsetning reikningsskiladagsetning reikningsskila notað í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="7a744-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="7a744-118">Einkvæmt útgáfukenni samanstendur af eftirfarandi þáttum:</span><span class="sxs-lookup"><span data-stu-id="7a744-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="7a744-119">Gerð útgáfu</span><span class="sxs-lookup"><span data-stu-id="7a744-119">Version type</span></span>
-   <span data-ttu-id="7a744-120">Dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="7a744-120">Date and time</span></span>
-   <span data-ttu-id="7a744-121">Fjárhagur kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="7a744-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="7a744-122">Fjárhagsár</span><span class="sxs-lookup"><span data-stu-id="7a744-122">Fiscal year</span></span>
-   <span data-ttu-id="7a744-123">Reikningstímabil</span><span class="sxs-lookup"><span data-stu-id="7a744-123">Fiscal period</span></span>

<span data-ttu-id="7a744-124">Útreikningur fastakostnaðar er keyrður óháð því hver útgáfan er.</span><span class="sxs-lookup"><span data-stu-id="7a744-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="7a744-125">Þess vegna er hægt að reikna út áætlaða útgáfu á undan raunútgáfu.</span><span class="sxs-lookup"><span data-stu-id="7a744-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="7a744-126">Útreikningur fastakostnaðar samanstendur af fjórum skrefum, eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="7a744-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="7a744-127">Í hverju skrefi er færslubókarhaus stofnaður með bókarfærslum.</span><span class="sxs-lookup"><span data-stu-id="7a744-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="7a744-128">Þessi færslubókarhaus geymir inntaksgögn fyrir hvert útreikningsþrep.</span><span class="sxs-lookup"><span data-stu-id="7a744-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="7a744-129">Stefnur og reglur eru notaðar í hverri færslulínu og kostnaðarfærslur eru myndaðar sem úttak.</span><span class="sxs-lookup"><span data-stu-id="7a744-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="7a744-130">Þess vegna hefurðu ávallt fullan rekjanleika.</span><span class="sxs-lookup"><span data-stu-id="7a744-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="7a744-131">[![Útreikningur fastakostnaðar](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="7a744-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="7a744-132">Reikna og úthluta sameiginlegur kostnaði vegna rafmagns</span><span class="sxs-lookup"><span data-stu-id="7a744-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="7a744-133">Í Fjárhagsbókhaldi er ákveðinn kostnaður, eins og rafmagn, skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="7a744-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="7a744-134">Þar af leiðandi er nákvæmar innsýn rekstrarfélags ekki veitt fyrir kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="7a744-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="7a744-135">Í kostnaðarbókhaldi verður kostnaður að flæða í gegnum fyrirtækiseiningar til að veita rétta innsýn rekstrarfélags þvert á allar fyrirtækiseiningar og stig.</span><span class="sxs-lookup"><span data-stu-id="7a744-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="7a744-136">Þetta flæði verður að byggja á annaðhvort nákvæmri færslu notkunar eða sanngjarnri matsreglu.</span><span class="sxs-lookup"><span data-stu-id="7a744-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="7a744-137">Í fjárhagnum er hægt að bóka rafmagnskostnað eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="7a744-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7a744-138">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="7a744-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7a744-139">Kostnaðarstaður</span><span class="sxs-lookup"><span data-stu-id="7a744-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="7a744-140">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="7a744-140">Main account</span></span></th>
<th><span data-ttu-id="7a744-141">Upphæð í bókhaldsgjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="7a744-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-142">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="7a744-143">CC099</span><span class="sxs-lookup"><span data-stu-id="7a744-143">CC099</span></span></td>
<td><span data-ttu-id="7a744-144">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="7a744-144">Default cost center</span></span></td>
<td><span data-ttu-id="7a744-145">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-145">10001</span></span></td>
<td><span data-ttu-id="7a744-146">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-146">Electricity</span></span></td>
<td><span data-ttu-id="7a744-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="7a744-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="7a744-148">Skref 1: Keyra útreikning kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="7a744-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="7a744-149">Sjálfvirkt er að þegar kostnaðarfærslur eru fluttar úr grunngögnum fái þær flokkun kostnaðarhegðunar **Óflokkað** í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="7a744-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="7a744-150">Með því að nota stefnureglur kostnaðarhegðunar er hægt að endurflokka kostnaðarfærslur sem annaðhvort **Fastan kostnað** eða **Breytilegan kostnað**.</span><span class="sxs-lookup"><span data-stu-id="7a744-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="7a744-151">Tilgreinið reglu kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="7a744-151">Define the cost behavior rule</span></span>

<span data-ttu-id="7a744-152">Í sumum tilfellum er hluti af kostnaði föst þóknun og eftirstandandi kostnaður byggist á notkun.</span><span class="sxs-lookup"><span data-stu-id="7a744-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="7a744-153">Rafmagnsreikningar stemma oft við þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="7a744-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="7a744-154">Þegar tiltekin föst þóknun hefur verið greidd, er greitt fyrir notkun á kílóvattklukkustund (Kwh).</span><span class="sxs-lookup"><span data-stu-id="7a744-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="7a744-155">Til dæmis ef föst kostnaðarþóknun er 1000.00 sýnir þetta hvernig regla kostnaðarhegðunar er skilgreind:</span><span class="sxs-lookup"><span data-stu-id="7a744-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="7a744-156">Föst upphæð 1.000,00</span><span class="sxs-lookup"><span data-stu-id="7a744-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="7a744-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="7a744-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="7a744-158">1000.01 &lt; N = Breyta</span><span class="sxs-lookup"><span data-stu-id="7a744-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="7a744-159">Færslubók</span><span class="sxs-lookup"><span data-stu-id="7a744-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7a744-160">Færslubók</span><span class="sxs-lookup"><span data-stu-id="7a744-160">Journal</span></span></th>
<th><span data-ttu-id="7a744-161">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="7a744-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7a744-162">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="7a744-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7a744-163">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="7a744-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-164">00001</span><span class="sxs-lookup"><span data-stu-id="7a744-164">00001</span></span></td>
<td><span data-ttu-id="7a744-165">Færslubók útreiknings fyrir kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="7a744-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="7a744-166">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="7a744-166">Fiscal</span></span></td>
<td><span data-ttu-id="7a744-167">2017</span><span class="sxs-lookup"><span data-stu-id="7a744-167">2017</span></span></td>
<td><span data-ttu-id="7a744-168">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="7a744-168">Period 1</span></span></td>
<td><span data-ttu-id="7a744-169">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="7a744-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7a744-170">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="7a744-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7a744-171">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="7a744-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7a744-172">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7a744-173">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="7a744-173">Cost element</span></span></th>
<th><span data-ttu-id="7a744-174">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="7a744-174">Cost behavior</span></span></th>
<th><span data-ttu-id="7a744-175">Upphæð</span><span class="sxs-lookup"><span data-stu-id="7a744-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-176">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="7a744-177">CC099</span><span class="sxs-lookup"><span data-stu-id="7a744-177">CC099</span></span></td>
<td><span data-ttu-id="7a744-178">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="7a744-178">Default cost center</span></span></td>
<td><span data-ttu-id="7a744-179">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-179">10001</span></span></td>
<td><span data-ttu-id="7a744-180">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-180">Electricity</span></span></td>
<td><span data-ttu-id="7a744-181">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="7a744-181">Unclassified</span></span></td>
<td><span data-ttu-id="7a744-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="7a744-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7a744-183">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="7a744-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a744-184">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7a744-185">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="7a744-185">Cost element</span></span></th>
<th><span data-ttu-id="7a744-186">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="7a744-186">Cost behavior</span></span></th>
<th><span data-ttu-id="7a744-187">Upphæð</span><span class="sxs-lookup"><span data-stu-id="7a744-187">Amount</span></span></th>
<th><span data-ttu-id="7a744-188">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="7a744-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-189">CC099</span><span class="sxs-lookup"><span data-stu-id="7a744-189">CC099</span></span></td>
<td><span data-ttu-id="7a744-190">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="7a744-190">Default cost center</span></span></td>
<td><span data-ttu-id="7a744-191">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-191">10001</span></span></td>
<td><span data-ttu-id="7a744-192">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-192">Electricity</span></span></td>
<td><span data-ttu-id="7a744-193">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="7a744-193">Unclassified</span></span></td>
<td><span data-ttu-id="7a744-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="7a744-194">10,000.00</span></span></td>
<td><span data-ttu-id="7a744-195">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-196">CC099</span><span class="sxs-lookup"><span data-stu-id="7a744-196">CC099</span></span></td>
<td><span data-ttu-id="7a744-197">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="7a744-197">Default cost center</span></span></td>
<td><span data-ttu-id="7a744-198">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-198">10001</span></span></td>
<td><span data-ttu-id="7a744-199">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-199">Electricity</span></span></td>
<td><span data-ttu-id="7a744-200">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="7a744-200">Unclassified</span></span></td>
<td><span data-ttu-id="7a744-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="7a744-201">-10,000.00</span></span></td>
<td><span data-ttu-id="7a744-202">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-203">CC099</span><span class="sxs-lookup"><span data-stu-id="7a744-203">CC099</span></span></td>
<td><span data-ttu-id="7a744-204">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="7a744-204">Default cost center</span></span></td>
<td><span data-ttu-id="7a744-205">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-205">10001</span></span></td>
<td><span data-ttu-id="7a744-206">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-206">Electricity</span></span></td>
<td><span data-ttu-id="7a744-207">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-207">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="7a744-208">1,000.00</span></span></td>
<td><span data-ttu-id="7a744-209">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-210">CC099</span><span class="sxs-lookup"><span data-stu-id="7a744-210">CC099</span></span></td>
<td><span data-ttu-id="7a744-211">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="7a744-211">Default cost center</span></span></td>
<td><span data-ttu-id="7a744-212">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-212">10001</span></span></td>
<td><span data-ttu-id="7a744-213">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-213">Electricity</span></span></td>
<td><span data-ttu-id="7a744-214">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-214">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="7a744-215">9,000.00</span></span></td>
<td><span data-ttu-id="7a744-216">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a744-217">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðarhegðunarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="7a744-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="7a744-218">Skref 2: Keyra útreikning kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="7a744-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="7a744-219">Kostnaðardreifing er notuð til að endurúthluta kostnaði frá einum kostnaðarhlut til annars eða fleiri kostnaðarhluta með því að nota viðeigandi úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="7a744-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="7a744-220">Kostnaðardreifing og kostnaðarúthlutun eru ólíkar að því leyti að kostnaðardreifing kemur alltaf upp á stigi aðalkostnaðareiningar upphaflegs verðs.</span><span class="sxs-lookup"><span data-stu-id="7a744-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="7a744-221">Tilgreinið kostnaðardreifingarreglu</span><span class="sxs-lookup"><span data-stu-id="7a744-221">Define the cost distribution rule</span></span>

<span data-ttu-id="7a744-222">Í Fjárhagsbókhaldi er rafmagnskostnaður oft skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="7a744-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="7a744-223">Í kostnaðarbókhaldi er þessi nálgun ekki nógu nákvæm.</span><span class="sxs-lookup"><span data-stu-id="7a744-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="7a744-224">Breytilegur kostnaði þarf að dreifa á staka kostnaðarhluti á sanngjörnum grunni.</span><span class="sxs-lookup"><span data-stu-id="7a744-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="7a744-225">Rökréttasti úthlutunargrunnurinn er notkun á rafmagni (Kwh).</span><span class="sxs-lookup"><span data-stu-id="7a744-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="7a744-226">Stofnað er tölfræðilegt víddarstak sem er nefnt Rafmagn og rafmagnsnotkun er skráð.</span><span class="sxs-lookup"><span data-stu-id="7a744-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="7a744-227">Sjálfgefið er að öll tölfræðileg víddarstök verða tiltæk sem úthlutunargrunnur.</span><span class="sxs-lookup"><span data-stu-id="7a744-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a744-228">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-228">Cost object</span></span></th>
<th><span data-ttu-id="7a744-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="7a744-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-230">CC001</span><span class="sxs-lookup"><span data-stu-id="7a744-230">CC001</span></span></td>
<td><span data-ttu-id="7a744-231">Mannauður</span><span class="sxs-lookup"><span data-stu-id="7a744-231">HR</span></span></td>
<td><span data-ttu-id="7a744-232">1.000</span><span class="sxs-lookup"><span data-stu-id="7a744-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-233">CC002</span><span class="sxs-lookup"><span data-stu-id="7a744-233">CC002</span></span></td>
<td><span data-ttu-id="7a744-234">Fjármál</span><span class="sxs-lookup"><span data-stu-id="7a744-234">Finance</span></span></td>
<td><span data-ttu-id="7a744-235">6,000</span><span class="sxs-lookup"><span data-stu-id="7a744-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-236">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-236">CC003</span></span></td>
<td><span data-ttu-id="7a744-237">Smölun</span><span class="sxs-lookup"><span data-stu-id="7a744-237">Assembly</span></span></td>
<td><span data-ttu-id="7a744-238">0</span><span class="sxs-lookup"><span data-stu-id="7a744-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a744-239">Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunni fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="7a744-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a744-240">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-240">Cost object</span></span></th>
<th><span data-ttu-id="7a744-241">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="7a744-241">Magnitude</span></span></th>
<th><span data-ttu-id="7a744-242">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="7a744-242">Allocation factor</span></span></th>
<th><span data-ttu-id="7a744-243">Upphæð</span><span class="sxs-lookup"><span data-stu-id="7a744-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-244">CC001</span><span class="sxs-lookup"><span data-stu-id="7a744-244">CC001</span></span></td>
<td><span data-ttu-id="7a744-245">Mannauður</span><span class="sxs-lookup"><span data-stu-id="7a744-245">HR</span></span></td>
<td><span data-ttu-id="7a744-246">1.000</span><span class="sxs-lookup"><span data-stu-id="7a744-246">1,000</span></span></td>
<td><span data-ttu-id="7a744-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="7a744-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7a744-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="7a744-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-249">CC002</span><span class="sxs-lookup"><span data-stu-id="7a744-249">CC002</span></span></td>
<td><span data-ttu-id="7a744-250">Fjármál</span><span class="sxs-lookup"><span data-stu-id="7a744-250">Finance</span></span></td>
<td><span data-ttu-id="7a744-251">6,000</span><span class="sxs-lookup"><span data-stu-id="7a744-251">6,000</span></span></td>
<td><span data-ttu-id="7a744-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="7a744-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7a744-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="7a744-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-254">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-254">CC003</span></span></td>
<td><span data-ttu-id="7a744-255">Smölun</span><span class="sxs-lookup"><span data-stu-id="7a744-255">Assembly</span></span></td>
<td><span data-ttu-id="7a744-256">0</span><span class="sxs-lookup"><span data-stu-id="7a744-256">0</span></span></td>
<td><span data-ttu-id="7a744-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="7a744-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="7a744-258">0,00</span><span class="sxs-lookup"><span data-stu-id="7a744-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a744-259">Föstum kostnaði þarf að dreifa jafnt á staka kostnaðarhluti sem hafa notað rafmagn.</span><span class="sxs-lookup"><span data-stu-id="7a744-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="7a744-260">Hægt er að ná þessa niðurstöðu með því að nota tölfræðilegt víddarstakið Rafmagn í úthlutunargrunni reikniformúlu: (Rafmagn &gt; 0,00) Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunn fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="7a744-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a744-261">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-261">Cost object</span></span></th>
<th><span data-ttu-id="7a744-262">Formúla</span><span class="sxs-lookup"><span data-stu-id="7a744-262">Formula</span></span></th>
<th><span data-ttu-id="7a744-263">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="7a744-263">Magnitude</span></span></th>
<th><span data-ttu-id="7a744-264">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="7a744-264">Allocation factor</span></span></th>
<th><span data-ttu-id="7a744-265">Upphæð</span><span class="sxs-lookup"><span data-stu-id="7a744-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-266">CC001</span><span class="sxs-lookup"><span data-stu-id="7a744-266">CC001</span></span></td>
<td><span data-ttu-id="7a744-267">Mannauður</span><span class="sxs-lookup"><span data-stu-id="7a744-267">HR</span></span></td>
<td><span data-ttu-id="7a744-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7a744-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7a744-269">1</span><span class="sxs-lookup"><span data-stu-id="7a744-269">1</span></span></td>
<td><span data-ttu-id="7a744-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="7a744-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7a744-271">500,00</span><span class="sxs-lookup"><span data-stu-id="7a744-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-272">CC002</span><span class="sxs-lookup"><span data-stu-id="7a744-272">CC002</span></span></td>
<td><span data-ttu-id="7a744-273">Fjármál</span><span class="sxs-lookup"><span data-stu-id="7a744-273">Finance</span></span></td>
<td><span data-ttu-id="7a744-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7a744-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7a744-275">1</span><span class="sxs-lookup"><span data-stu-id="7a744-275">1</span></span></td>
<td><span data-ttu-id="7a744-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="7a744-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7a744-277">500,00</span><span class="sxs-lookup"><span data-stu-id="7a744-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-278">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-278">CC003</span></span></td>
<td><span data-ttu-id="7a744-279">Smölun</span><span class="sxs-lookup"><span data-stu-id="7a744-279">Assembly</span></span></td>
<td><span data-ttu-id="7a744-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="7a744-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="7a744-281">0</span><span class="sxs-lookup"><span data-stu-id="7a744-281">0</span></span></td>
<td><span data-ttu-id="7a744-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="7a744-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="7a744-283">0,00</span><span class="sxs-lookup"><span data-stu-id="7a744-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="7a744-284">Færslubók</span><span class="sxs-lookup"><span data-stu-id="7a744-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7a744-285">Færslubók</span><span class="sxs-lookup"><span data-stu-id="7a744-285">Journal</span></span></th>
<th><span data-ttu-id="7a744-286">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="7a744-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7a744-287">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="7a744-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7a744-288">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="7a744-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-289">00002</span><span class="sxs-lookup"><span data-stu-id="7a744-289">00002</span></span></td>
<td><span data-ttu-id="7a744-290">Útreikningabók kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="7a744-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="7a744-291">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="7a744-291">Fiscal</span></span></td>
<td><span data-ttu-id="7a744-292">2017</span><span class="sxs-lookup"><span data-stu-id="7a744-292">2017</span></span></td>
<td><span data-ttu-id="7a744-293">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="7a744-293">Period 1</span></span></td>
<td><span data-ttu-id="7a744-294">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="7a744-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7a744-295">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="7a744-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7a744-296">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="7a744-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7a744-297">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7a744-298">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="7a744-298">Cost element</span></span></th>
<th><span data-ttu-id="7a744-299">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="7a744-299">Cost behavior</span></span></th>
<th><span data-ttu-id="7a744-300">Upphæð</span><span class="sxs-lookup"><span data-stu-id="7a744-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-301">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a744-302">CC099</span><span class="sxs-lookup"><span data-stu-id="7a744-302">CC099</span></span></td>
<td><span data-ttu-id="7a744-303">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="7a744-303">Default cost center</span></span></td>
<td><span data-ttu-id="7a744-304">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-304">10001</span></span></td>
<td><span data-ttu-id="7a744-305">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-305">Electricity</span></span></td>
<td><span data-ttu-id="7a744-306">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-306">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="7a744-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-308">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a744-309">CC099</span><span class="sxs-lookup"><span data-stu-id="7a744-309">CC099</span></span></td>
<td><span data-ttu-id="7a744-310">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="7a744-310">Default cost center</span></span></td>
<td><span data-ttu-id="7a744-311">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-311">10001</span></span></td>
<td><span data-ttu-id="7a744-312">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-312">Electricity</span></span></td>
<td><span data-ttu-id="7a744-313">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-313">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="7a744-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7a744-315">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="7a744-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a744-316">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7a744-317">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="7a744-317">Cost element</span></span></th>
<th><span data-ttu-id="7a744-318">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="7a744-318">Cost behavior</span></span></th>
<th><span data-ttu-id="7a744-319">Upphæð</span><span class="sxs-lookup"><span data-stu-id="7a744-319">Amount</span></span></th>
<th><span data-ttu-id="7a744-320">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="7a744-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-321">CC099</span><span class="sxs-lookup"><span data-stu-id="7a744-321">CC099</span></span></td>
<td><span data-ttu-id="7a744-322">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="7a744-322">Default cost center</span></span></td>
<td><span data-ttu-id="7a744-323">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-323">10001</span></span></td>
<td><span data-ttu-id="7a744-324">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-324">Electricity</span></span></td>
<td><span data-ttu-id="7a744-325">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-325">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="7a744-326">-1,000.00</span></span></td>
<td><span data-ttu-id="7a744-327">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-328">CC001</span><span class="sxs-lookup"><span data-stu-id="7a744-328">CC001</span></span></td>
<td><span data-ttu-id="7a744-329">Mannauður</span><span class="sxs-lookup"><span data-stu-id="7a744-329">HR</span></span></td>
<td><span data-ttu-id="7a744-330">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-330">10001</span></span></td>
<td><span data-ttu-id="7a744-331">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-331">Electricity</span></span></td>
<td><span data-ttu-id="7a744-332">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-332">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-333">500,00</span><span class="sxs-lookup"><span data-stu-id="7a744-333">500.00</span></span></td>
<td><span data-ttu-id="7a744-334">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-335">CC002</span><span class="sxs-lookup"><span data-stu-id="7a744-335">CC002</span></span></td>
<td><span data-ttu-id="7a744-336">Fjármál</span><span class="sxs-lookup"><span data-stu-id="7a744-336">Finance</span></span></td>
<td><span data-ttu-id="7a744-337">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-337">10001</span></span></td>
<td><span data-ttu-id="7a744-338">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-338">Electricity</span></span></td>
<td><span data-ttu-id="7a744-339">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-339">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-340">500,00</span><span class="sxs-lookup"><span data-stu-id="7a744-340">500.00</span></span></td>
<td><span data-ttu-id="7a744-341">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-342">CC099</span><span class="sxs-lookup"><span data-stu-id="7a744-342">CC099</span></span></td>
<td><span data-ttu-id="7a744-343">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="7a744-343">Default cost center</span></span></td>
<td><span data-ttu-id="7a744-344">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-344">10001</span></span></td>
<td><span data-ttu-id="7a744-345">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-345">Electricity</span></span></td>
<td><span data-ttu-id="7a744-346">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-346">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="7a744-347">-9,000.00</span></span></td>
<td><span data-ttu-id="7a744-348">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-349">CC001</span><span class="sxs-lookup"><span data-stu-id="7a744-349">CC001</span></span></td>
<td><span data-ttu-id="7a744-350">Mannauður</span><span class="sxs-lookup"><span data-stu-id="7a744-350">HR</span></span></td>
<td><span data-ttu-id="7a744-351">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-351">10001</span></span></td>
<td><span data-ttu-id="7a744-352">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-352">Electricity</span></span></td>
<td><span data-ttu-id="7a744-353">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-353">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="7a744-354">1,285.71</span></span></td>
<td><span data-ttu-id="7a744-355">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-356">CC002</span><span class="sxs-lookup"><span data-stu-id="7a744-356">CC002</span></span></td>
<td><span data-ttu-id="7a744-357">Fjármál</span><span class="sxs-lookup"><span data-stu-id="7a744-357">Finance</span></span></td>
<td><span data-ttu-id="7a744-358">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-358">10001</span></span></td>
<td><span data-ttu-id="7a744-359">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-359">Electricity</span></span></td>
<td><span data-ttu-id="7a744-360">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-360">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="7a744-361">7,714.29</span></span></td>
<td><span data-ttu-id="7a744-362">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a744-363">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðardreifingarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="7a744-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="7a744-364">Skref 3: Keyra útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="7a744-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="7a744-365">Sameiginlegur kostnaður er notaður til að rukka einn eða fleiri tilgreinda kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="7a744-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="7a744-366">Gjöldin byggjast á fyrirframákveðnu kostnaðarhlutfalli og mæligildi úr úthlutuðum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="7a744-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="7a744-367">Skilgreina sameiginlegan kostnað</span><span class="sxs-lookup"><span data-stu-id="7a744-367">Define the overhead rate</span></span>

<span data-ttu-id="7a744-368">Kostnaðarhlutur CC001 Mannauður stuðlar að safni innri verka.</span><span class="sxs-lookup"><span data-stu-id="7a744-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="7a744-369">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsverk til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="7a744-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a744-370">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-370">Cost object</span></span></th>
<th><span data-ttu-id="7a744-371">Tímar</span><span class="sxs-lookup"><span data-stu-id="7a744-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-372">Verk 1</span><span class="sxs-lookup"><span data-stu-id="7a744-372">Proj 1</span></span></td>
<td><span data-ttu-id="7a744-373">Verk 1</span><span class="sxs-lookup"><span data-stu-id="7a744-373">Project 1</span></span></td>
<td><span data-ttu-id="7a744-374">3</span><span class="sxs-lookup"><span data-stu-id="7a744-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-375">Verk 2</span><span class="sxs-lookup"><span data-stu-id="7a744-375">Proj 2</span></span></td>
<td><span data-ttu-id="7a744-376">Verk 2</span><span class="sxs-lookup"><span data-stu-id="7a744-376">Project 2</span></span></td>
<td><span data-ttu-id="7a744-377">1</span><span class="sxs-lookup"><span data-stu-id="7a744-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a744-378">Fyrirframákveðið kostnaðarhlutfall fyrir kostnaðarframlag verk hefur verið skilgreint.</span><span class="sxs-lookup"><span data-stu-id="7a744-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a744-379">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-379">Cost object</span></span></th>
<th><span data-ttu-id="7a744-380">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="7a744-380">Cost element</span></span></th>
<th><span data-ttu-id="7a744-381">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="7a744-381">Cost behavior</span></span></th>
<th><span data-ttu-id="7a744-382">Einingar</span><span class="sxs-lookup"><span data-stu-id="7a744-382">Units</span></span></th>
<th><span data-ttu-id="7a744-383">Taxti</span><span class="sxs-lookup"><span data-stu-id="7a744-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-384">CC001</span><span class="sxs-lookup"><span data-stu-id="7a744-384">CC001</span></span></td>
<td><span data-ttu-id="7a744-385">Mannauður</span><span class="sxs-lookup"><span data-stu-id="7a744-385">HR</span></span></td>
<td><span data-ttu-id="7a744-386">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-386">10001</span></span></td>
<td><span data-ttu-id="7a744-387">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-387">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-388">1</span><span class="sxs-lookup"><span data-stu-id="7a744-388">1</span></span></td>
<td><span data-ttu-id="7a744-389">10</span><span class="sxs-lookup"><span data-stu-id="7a744-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a744-390">Eftirfarandi tafla sýnir niðurstöður þegar Mannauðsverk eru notuð sem grunnur við úthlutun.</span><span class="sxs-lookup"><span data-stu-id="7a744-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a744-391">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-391">Cost object</span></span></th>
<th><span data-ttu-id="7a744-392">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="7a744-392">Magnitude</span></span></th>
<th><span data-ttu-id="7a744-393">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="7a744-393">Cost element</span></span></th>
<th><span data-ttu-id="7a744-394">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="7a744-394">Allocation factor</span></span></th>
<th><span data-ttu-id="7a744-395">Upphæð</span><span class="sxs-lookup"><span data-stu-id="7a744-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-396">Verk 1</span><span class="sxs-lookup"><span data-stu-id="7a744-396">Proj 1</span></span></td>
<td><span data-ttu-id="7a744-397">Verk 1</span><span class="sxs-lookup"><span data-stu-id="7a744-397">Project 1</span></span></td>
<td><span data-ttu-id="7a744-398">3</span><span class="sxs-lookup"><span data-stu-id="7a744-398">3</span></span></td>
<td><span data-ttu-id="7a744-399">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-399">10001</span></span></td>
<td><span data-ttu-id="7a744-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="7a744-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="7a744-401">30,00</span><span class="sxs-lookup"><span data-stu-id="7a744-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-402">Verk 2</span><span class="sxs-lookup"><span data-stu-id="7a744-402">Proj 2</span></span></td>
<td><span data-ttu-id="7a744-403">Verk 2</span><span class="sxs-lookup"><span data-stu-id="7a744-403">Project 2</span></span></td>
<td><span data-ttu-id="7a744-404">1</span><span class="sxs-lookup"><span data-stu-id="7a744-404">1</span></span></td>
<td><span data-ttu-id="7a744-405">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-405">10001</span></span></td>
<td><span data-ttu-id="7a744-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="7a744-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="7a744-407">10,00</span><span class="sxs-lookup"><span data-stu-id="7a744-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="7a744-408">Færslubók</span><span class="sxs-lookup"><span data-stu-id="7a744-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7a744-409">Færslubók</span><span class="sxs-lookup"><span data-stu-id="7a744-409">Journal</span></span></th>
<th><span data-ttu-id="7a744-410">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="7a744-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7a744-411">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="7a744-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7a744-412">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="7a744-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-413">00003</span><span class="sxs-lookup"><span data-stu-id="7a744-413">00003</span></span></td>
<td><span data-ttu-id="7a744-414">Færslubók fyrir útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="7a744-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="7a744-415">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="7a744-415">Fiscal</span></span></td>
<td><span data-ttu-id="7a744-416">2017</span><span class="sxs-lookup"><span data-stu-id="7a744-416">2017</span></span></td>
<td><span data-ttu-id="7a744-417">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="7a744-417">Period 1</span></span></td>
<td><span data-ttu-id="7a744-418">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="7a744-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="7a744-419">Bókarfærslur (Bókarfærslur fyrir útreikning sameiginlegs kostnaðar)</span><span class="sxs-lookup"><span data-stu-id="7a744-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7a744-420">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="7a744-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7a744-421">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-421">Cost object</span></span></th>
<th><span data-ttu-id="7a744-422">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="7a744-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-423">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a744-424">Verk 1</span><span class="sxs-lookup"><span data-stu-id="7a744-424">Proj 1</span></span></td>
<td><span data-ttu-id="7a744-425">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="7a744-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="7a744-426">3,00</span><span class="sxs-lookup"><span data-stu-id="7a744-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-427">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a744-428">Verk 2</span><span class="sxs-lookup"><span data-stu-id="7a744-428">Proj 2</span></span></td>
<td><span data-ttu-id="7a744-429">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="7a744-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="7a744-430">1,00</span><span class="sxs-lookup"><span data-stu-id="7a744-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7a744-431">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="7a744-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a744-432">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7a744-433">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="7a744-433">Cost element</span></span></th>
<th><span data-ttu-id="7a744-434">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="7a744-434">Cost behavior</span></span></th>
<th><span data-ttu-id="7a744-435">Upphæð</span><span class="sxs-lookup"><span data-stu-id="7a744-435">Amount</span></span></th>
<th><span data-ttu-id="7a744-436">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="7a744-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="7a744-437">CC0001</span></span></td>
<td><span data-ttu-id="7a744-438">Mannauður</span><span class="sxs-lookup"><span data-stu-id="7a744-438">HR</span></span></td>
<td><span data-ttu-id="7a744-439">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-439">10001</span></span></td>
<td><span data-ttu-id="7a744-440">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-440">Electricity</span></span></td>
<td><span data-ttu-id="7a744-441">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-441">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="7a744-442">-30.00</span></span></td>
<td><span data-ttu-id="7a744-443">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-444">Verk 1</span><span class="sxs-lookup"><span data-stu-id="7a744-444">Proj 1</span></span></td>
<td><span data-ttu-id="7a744-445">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="7a744-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="7a744-446">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-446">10001</span></span></td>
<td><span data-ttu-id="7a744-447">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-447">Electricity</span></span></td>
<td><span data-ttu-id="7a744-448">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-448">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-449">30,00</span><span class="sxs-lookup"><span data-stu-id="7a744-449">30.00</span></span></td>
<td><span data-ttu-id="7a744-450">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-451">CC001</span><span class="sxs-lookup"><span data-stu-id="7a744-451">CC001</span></span></td>
<td><span data-ttu-id="7a744-452">Mannauður</span><span class="sxs-lookup"><span data-stu-id="7a744-452">HR</span></span></td>
<td><span data-ttu-id="7a744-453">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-453">10001</span></span></td>
<td><span data-ttu-id="7a744-454">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-454">Electricity</span></span></td>
<td><span data-ttu-id="7a744-455">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-455">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="7a744-456">-10.00</span></span></td>
<td><span data-ttu-id="7a744-457">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-458">Verk 2</span><span class="sxs-lookup"><span data-stu-id="7a744-458">Proj 2</span></span></td>
<td><span data-ttu-id="7a744-459">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="7a744-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="7a744-460">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-460">10001</span></span></td>
<td><span data-ttu-id="7a744-461">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-461">Electricity</span></span></td>
<td><span data-ttu-id="7a744-462">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-462">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-463">10,00</span><span class="sxs-lookup"><span data-stu-id="7a744-463">10.00</span></span></td>
<td><span data-ttu-id="7a744-464">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a744-465">Nánari upplýsingar er að finna í [Framkvæma útreikning fastakostnaðar](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="7a744-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="7a744-466">Skref 4: Keyra útreikning kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="7a744-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="7a744-467">Úthlutun er notuð til að úthluta stöðu kostnaðarhlutar í öðrum kostnaðarhlutum með því að nota úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="7a744-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="7a744-468">Finance styður gagnvirka úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="7a744-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="7a744-469">Í gagnvirkri úthlutunaraðferð er sú sameiginlega þjónusta sem hjálparkostnaðarhlutir skiptast á viðurkennd að fullu.</span><span class="sxs-lookup"><span data-stu-id="7a744-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="7a744-470">Kerfið ákvarðar sjálfkrafa rétta röð til að framkvæma úthlutun eftir.</span><span class="sxs-lookup"><span data-stu-id="7a744-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="7a744-471">Stöðu kostnaðarhluta er úthlutað með einum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="7a744-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="7a744-472">Úthlutanir þvert á víddir kostnaðarhluta og viðkomandi stök þeirra eru studdar.</span><span class="sxs-lookup"><span data-stu-id="7a744-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="7a744-473">Úthlutun pöntunarinnar er stjórnað af stýrieiningu kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="7a744-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="7a744-474">[![Gagnkvæm aðferð](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="7a744-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="7a744-475">Tilgreinið kostnaðarúthlutun</span><span class="sxs-lookup"><span data-stu-id="7a744-475">Define the cost allocation</span></span>

<span data-ttu-id="7a744-476">Hér er einfalt dæmi sem útskýrir hvernig hægt er að rekja flæði kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="7a744-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="7a744-477">Kostnaðarhlutir CC001 Mannauður leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="7a744-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="7a744-478">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="7a744-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a744-479">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-479">Cost object</span></span></th>
<th><span data-ttu-id="7a744-480">Mannauðsþjónusta</span><span class="sxs-lookup"><span data-stu-id="7a744-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-481">CC002</span><span class="sxs-lookup"><span data-stu-id="7a744-481">CC002</span></span></td>
<td><span data-ttu-id="7a744-482">Fjármál</span><span class="sxs-lookup"><span data-stu-id="7a744-482">Finance</span></span></td>
<td><span data-ttu-id="7a744-483">35</span><span class="sxs-lookup"><span data-stu-id="7a744-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-484">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-484">CC003</span></span></td>
<td><span data-ttu-id="7a744-485">Smölun</span><span class="sxs-lookup"><span data-stu-id="7a744-485">Assembly</span></span></td>
<td><span data-ttu-id="7a744-486">55</span><span class="sxs-lookup"><span data-stu-id="7a744-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-487">CC004</span><span class="sxs-lookup"><span data-stu-id="7a744-487">CC004</span></span></td>
<td><span data-ttu-id="7a744-488">Pakkning</span><span class="sxs-lookup"><span data-stu-id="7a744-488">Packaging</span></span></td>
<td><span data-ttu-id="7a744-489">10</span><span class="sxs-lookup"><span data-stu-id="7a744-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a744-490">Kostnaðarhlutir CC002 Fjármál leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="7a744-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="7a744-491">Stofnað er tölfræðilegt víddarstak sem kallast Fjármálaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="7a744-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a744-492">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-492">Cost object</span></span></th>
<th><span data-ttu-id="7a744-493">Fjármálaþjónusta</span><span class="sxs-lookup"><span data-stu-id="7a744-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-494">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-494">CC003</span></span></td>
<td><span data-ttu-id="7a744-495">Smölun</span><span class="sxs-lookup"><span data-stu-id="7a744-495">Assembly</span></span></td>
<td><span data-ttu-id="7a744-496">65</span><span class="sxs-lookup"><span data-stu-id="7a744-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-497">CC004</span><span class="sxs-lookup"><span data-stu-id="7a744-497">CC004</span></span></td>
<td><span data-ttu-id="7a744-498">Pakkning</span><span class="sxs-lookup"><span data-stu-id="7a744-498">Packaging</span></span></td>
<td><span data-ttu-id="7a744-499">35</span><span class="sxs-lookup"><span data-stu-id="7a744-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a744-500">Kostnaðarhlutir CC003 Samsetning leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="7a744-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="7a744-501">Meðlimur tölfræðilega víddar sem kallast Mannauður verk er stofnað til að mælvíddarstaka notuðum magnitude.</span><span class="sxs-lookup"><span data-stu-id="7a744-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a744-502">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-502">Cost object</span></span></th>
<th><span data-ttu-id="7a744-503">Samsetningarþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="7a744-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-504">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-504">Prod 1</span></span></td>
<td><span data-ttu-id="7a744-505">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-505">Product 1</span></span></td>
<td><span data-ttu-id="7a744-506">60</span><span class="sxs-lookup"><span data-stu-id="7a744-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-507">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-507">Prod 2</span></span></td>
<td><span data-ttu-id="7a744-508">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-508">Product 2</span></span></td>
<td><span data-ttu-id="7a744-509">20</span><span class="sxs-lookup"><span data-stu-id="7a744-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a744-510">Kostnaðarhlutir CC004 Umbúðir leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="7a744-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="7a744-511">Stofnað er tölfræðilegt víddarstak sem kallast Umbúðaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="7a744-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a744-512">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-512">Cost object</span></span></th>
<th><span data-ttu-id="7a744-513">Umbúðaþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="7a744-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-514">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-514">Prod 1</span></span></td>
<td><span data-ttu-id="7a744-515">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-515">Product 1</span></span></td>
<td><span data-ttu-id="7a744-516">80</span><span class="sxs-lookup"><span data-stu-id="7a744-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-517">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-517">Prod 2</span></span></td>
<td><span data-ttu-id="7a744-518">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-518">Product 2</span></span></td>
<td><span data-ttu-id="7a744-519">15</span><span class="sxs-lookup"><span data-stu-id="7a744-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7a744-520">Hægt er að afleiða tölfræðiaðgerðir eins og framleiðslutíma sem vara notar frá upprunagögnum.</span><span class="sxs-lookup"><span data-stu-id="7a744-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="7a744-521">Nánari upplýsingar er að finna í [Veitusniðmát tölfræðiaðgerðar](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="7a744-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="7a744-522">Eftirfarandi tafla sýnir niðurstöður þegar mannauðsþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="7a744-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a744-523">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-523">Cost object</span></span></th>
<th><span data-ttu-id="7a744-524">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="7a744-524">Magnitude</span></span></th>
<th><span data-ttu-id="7a744-525">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="7a744-525">Allocation factor</span></span></th>
<th><span data-ttu-id="7a744-526">Upphæð</span><span class="sxs-lookup"><span data-stu-id="7a744-526">Amount</span></span></th>
<th><span data-ttu-id="7a744-527">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="7a744-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-528">CC002</span><span class="sxs-lookup"><span data-stu-id="7a744-528">CC002</span></span></td>
<td><span data-ttu-id="7a744-529">Fjármál</span><span class="sxs-lookup"><span data-stu-id="7a744-529">Finance</span></span></td>
<td><span data-ttu-id="7a744-530">35</span><span class="sxs-lookup"><span data-stu-id="7a744-530">35</span></span></td>
<td><span data-ttu-id="7a744-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7a744-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7a744-532">175.00</span><span class="sxs-lookup"><span data-stu-id="7a744-532">175.00</span></span></td>
<td><span data-ttu-id="7a744-533">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-534">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-534">CC003</span></span></td>
<td><span data-ttu-id="7a744-535">Smölun</span><span class="sxs-lookup"><span data-stu-id="7a744-535">Assembly</span></span></td>
<td><span data-ttu-id="7a744-536">55</span><span class="sxs-lookup"><span data-stu-id="7a744-536">55</span></span></td>
<td><span data-ttu-id="7a744-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7a744-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7a744-538">275.00</span><span class="sxs-lookup"><span data-stu-id="7a744-538">275.00</span></span></td>
<td><span data-ttu-id="7a744-539">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-540">CC004</span><span class="sxs-lookup"><span data-stu-id="7a744-540">CC004</span></span></td>
<td><span data-ttu-id="7a744-541">Pakkning</span><span class="sxs-lookup"><span data-stu-id="7a744-541">Packaging</span></span></td>
<td><span data-ttu-id="7a744-542">10</span><span class="sxs-lookup"><span data-stu-id="7a744-542">10</span></span></td>
<td><span data-ttu-id="7a744-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="7a744-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="7a744-544">50,00</span><span class="sxs-lookup"><span data-stu-id="7a744-544">50.00</span></span></td>
<td><span data-ttu-id="7a744-545">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-546">CC002</span><span class="sxs-lookup"><span data-stu-id="7a744-546">CC002</span></span></td>
<td><span data-ttu-id="7a744-547">Fjármál</span><span class="sxs-lookup"><span data-stu-id="7a744-547">Finance</span></span></td>
<td><span data-ttu-id="7a744-548">35</span><span class="sxs-lookup"><span data-stu-id="7a744-548">35</span></span></td>
<td><span data-ttu-id="7a744-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="7a744-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7a744-550">436.00</span><span class="sxs-lookup"><span data-stu-id="7a744-550">436.00</span></span></td>
<td><span data-ttu-id="7a744-551">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-552">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-552">CC003</span></span></td>
<td><span data-ttu-id="7a744-553">Smölun</span><span class="sxs-lookup"><span data-stu-id="7a744-553">Assembly</span></span></td>
<td><span data-ttu-id="7a744-554">55</span><span class="sxs-lookup"><span data-stu-id="7a744-554">55</span></span></td>
<td><span data-ttu-id="7a744-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="7a744-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7a744-556">685.14</span><span class="sxs-lookup"><span data-stu-id="7a744-556">685.14</span></span></td>
<td><span data-ttu-id="7a744-557">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-558">CC004</span><span class="sxs-lookup"><span data-stu-id="7a744-558">CC004</span></span></td>
<td><span data-ttu-id="7a744-559">Pakkning</span><span class="sxs-lookup"><span data-stu-id="7a744-559">Packaging</span></span></td>
<td><span data-ttu-id="7a744-560">10</span><span class="sxs-lookup"><span data-stu-id="7a744-560">10</span></span></td>
<td><span data-ttu-id="7a744-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="7a744-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="7a744-562">124.57</span><span class="sxs-lookup"><span data-stu-id="7a744-562">124.57</span></span></td>
<td><span data-ttu-id="7a744-563">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a744-564">Eftirfarandi tafla sýnir niðurstöður þegar Fjármálaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="7a744-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a744-565">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-565">Cost object</span></span></th>
<th><span data-ttu-id="7a744-566">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="7a744-566">Magnitude</span></span></th>
<th><span data-ttu-id="7a744-567">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="7a744-567">Allocation factor</span></span></th>
<th><span data-ttu-id="7a744-568">Upphæð</span><span class="sxs-lookup"><span data-stu-id="7a744-568">Amount</span></span></th>
<th><span data-ttu-id="7a744-569">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="7a744-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-570">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-570">CC003</span></span></td>
<td><span data-ttu-id="7a744-571">Smölun</span><span class="sxs-lookup"><span data-stu-id="7a744-571">Assembly</span></span></td>
<td><span data-ttu-id="7a744-572">65</span><span class="sxs-lookup"><span data-stu-id="7a744-572">65</span></span></td>
<td><span data-ttu-id="7a744-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="7a744-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="7a744-574">438.75</span><span class="sxs-lookup"><span data-stu-id="7a744-574">438.75</span></span></td>
<td><span data-ttu-id="7a744-575">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-576">CC004</span><span class="sxs-lookup"><span data-stu-id="7a744-576">CC004</span></span></td>
<td><span data-ttu-id="7a744-577">Pakkning</span><span class="sxs-lookup"><span data-stu-id="7a744-577">Packaging</span></span></td>
<td><span data-ttu-id="7a744-578">35</span><span class="sxs-lookup"><span data-stu-id="7a744-578">35</span></span></td>
<td><span data-ttu-id="7a744-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="7a744-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="7a744-580">236.25</span><span class="sxs-lookup"><span data-stu-id="7a744-580">236.25</span></span></td>
<td><span data-ttu-id="7a744-581">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-582">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-582">CC003</span></span></td>
<td><span data-ttu-id="7a744-583">Smölun</span><span class="sxs-lookup"><span data-stu-id="7a744-583">Assembly</span></span></td>
<td><span data-ttu-id="7a744-584">65</span><span class="sxs-lookup"><span data-stu-id="7a744-584">65</span></span></td>
<td><span data-ttu-id="7a744-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="7a744-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="7a744-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="7a744-586">5,297.69</span></span></td>
<td><span data-ttu-id="7a744-587">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-588">CC004</span><span class="sxs-lookup"><span data-stu-id="7a744-588">CC004</span></span></td>
<td><span data-ttu-id="7a744-589">Pakkning</span><span class="sxs-lookup"><span data-stu-id="7a744-589">Packaging</span></span></td>
<td><span data-ttu-id="7a744-590">35</span><span class="sxs-lookup"><span data-stu-id="7a744-590">35</span></span></td>
<td><span data-ttu-id="7a744-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="7a744-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="7a744-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="7a744-592">2,852.60</span></span></td>
<td><span data-ttu-id="7a744-593">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a744-594">Eftirfarandi tafla sýnir niðurstöður þegar Samsetningarþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="7a744-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a744-595">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-595">Cost object</span></span></th>
<th><span data-ttu-id="7a744-596">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="7a744-596">Magnitude</span></span></th>
<th><span data-ttu-id="7a744-597">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="7a744-597">Allocation factor</span></span></th>
<th><span data-ttu-id="7a744-598">Upphæð</span><span class="sxs-lookup"><span data-stu-id="7a744-598">Amount</span></span></th>
<th><span data-ttu-id="7a744-599">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="7a744-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-600">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-600">Prod 1</span></span></td>
<td><span data-ttu-id="7a744-601">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-601">Product 1</span></span></td>
<td><span data-ttu-id="7a744-602">60</span><span class="sxs-lookup"><span data-stu-id="7a744-602">60</span></span></td>
<td><span data-ttu-id="7a744-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="7a744-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="7a744-604">535.31</span><span class="sxs-lookup"><span data-stu-id="7a744-604">535.31</span></span></td>
<td><span data-ttu-id="7a744-605">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-606">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-606">Prod 2</span></span></td>
<td><span data-ttu-id="7a744-607">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-607">Product 2</span></span></td>
<td><span data-ttu-id="7a744-608">20</span><span class="sxs-lookup"><span data-stu-id="7a744-608">20</span></span></td>
<td><span data-ttu-id="7a744-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="7a744-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="7a744-610">178.44</span><span class="sxs-lookup"><span data-stu-id="7a744-610">178.44</span></span></td>
<td><span data-ttu-id="7a744-611">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-612">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-612">Prod 1</span></span></td>
<td><span data-ttu-id="7a744-613">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-613">Product 1</span></span></td>
<td><span data-ttu-id="7a744-614">60</span><span class="sxs-lookup"><span data-stu-id="7a744-614">60</span></span></td>
<td><span data-ttu-id="7a744-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="7a744-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="7a744-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="7a744-616">4,487.12</span></span></td>
<td><span data-ttu-id="7a744-617">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-618">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-618">Prod 2</span></span></td>
<td><span data-ttu-id="7a744-619">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-619">Product 2</span></span></td>
<td><span data-ttu-id="7a744-620">20</span><span class="sxs-lookup"><span data-stu-id="7a744-620">20</span></span></td>
<td><span data-ttu-id="7a744-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="7a744-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="7a744-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="7a744-622">1,495.71</span></span></td>
<td><span data-ttu-id="7a744-623">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="7a744-624">Eftirfarandi tafla sýnir niðurstöður þegar Umbúðaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="7a744-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a744-625">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-625">Cost object</span></span></th>
<th><span data-ttu-id="7a744-626">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="7a744-626">Magnitude</span></span></th>
<th><span data-ttu-id="7a744-627">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="7a744-627">Allocation factor</span></span></th>
<th><span data-ttu-id="7a744-628">Upphæð</span><span class="sxs-lookup"><span data-stu-id="7a744-628">Amount</span></span></th>
<th><span data-ttu-id="7a744-629">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="7a744-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-630">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-630">Prod 1</span></span></td>
<td><span data-ttu-id="7a744-631">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-631">Product 1</span></span></td>
<td><span data-ttu-id="7a744-632">80</span><span class="sxs-lookup"><span data-stu-id="7a744-632">80</span></span></td>
<td><span data-ttu-id="7a744-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="7a744-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="7a744-634">241.05</span><span class="sxs-lookup"><span data-stu-id="7a744-634">241.05</span></span></td>
<td><span data-ttu-id="7a744-635">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-636">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-636">Prod 2</span></span></td>
<td><span data-ttu-id="7a744-637">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-637">Product 2</span></span></td>
<td><span data-ttu-id="7a744-638">15</span><span class="sxs-lookup"><span data-stu-id="7a744-638">15</span></span></td>
<td><span data-ttu-id="7a744-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="7a744-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="7a744-640">45.20</span><span class="sxs-lookup"><span data-stu-id="7a744-640">45.20</span></span></td>
<td><span data-ttu-id="7a744-641">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-642">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-642">Prod 1</span></span></td>
<td><span data-ttu-id="7a744-643">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-643">Product 1</span></span></td>
<td><span data-ttu-id="7a744-644">80</span><span class="sxs-lookup"><span data-stu-id="7a744-644">80</span></span></td>
<td><span data-ttu-id="7a744-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="7a744-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="7a744-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="7a744-646">2,507.09</span></span></td>
<td><span data-ttu-id="7a744-647">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-648">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-648">Prod 2</span></span></td>
<td><span data-ttu-id="7a744-649">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-649">Product 2</span></span></td>
<td><span data-ttu-id="7a744-650">15</span><span class="sxs-lookup"><span data-stu-id="7a744-650">15</span></span></td>
<td><span data-ttu-id="7a744-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="7a744-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="7a744-652">470.08</span><span class="sxs-lookup"><span data-stu-id="7a744-652">470.08</span></span></td>
<td><span data-ttu-id="7a744-653">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="7a744-654">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="7a744-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7a744-655">Færslubók</span><span class="sxs-lookup"><span data-stu-id="7a744-655">Journal</span></span></th>
<th><span data-ttu-id="7a744-656">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="7a744-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="7a744-657">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="7a744-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="7a744-658">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="7a744-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-659">00004</span><span class="sxs-lookup"><span data-stu-id="7a744-659">00004</span></span></td>
<td><span data-ttu-id="7a744-660">Færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="7a744-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="7a744-661">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="7a744-661">Fiscal</span></span></td>
<td><span data-ttu-id="7a744-662">2017</span><span class="sxs-lookup"><span data-stu-id="7a744-662">2017</span></span></td>
<td><span data-ttu-id="7a744-663">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="7a744-663">Period 1</span></span></td>
<td><span data-ttu-id="7a744-664">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="7a744-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="7a744-665">Færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="7a744-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="7a744-666">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="7a744-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="7a744-667">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7a744-668">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="7a744-668">Cost element</span></span></th>
<th><span data-ttu-id="7a744-669">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="7a744-669">Cost behavior</span></span></th>
<th><span data-ttu-id="7a744-670">Upphæð</span><span class="sxs-lookup"><span data-stu-id="7a744-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-671">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a744-672">CC001</span><span class="sxs-lookup"><span data-stu-id="7a744-672">CC001</span></span></td>
<td><span data-ttu-id="7a744-673">Mannauður</span><span class="sxs-lookup"><span data-stu-id="7a744-673">HR</span></span></td>
<td><span data-ttu-id="7a744-674">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-674">10001</span></span></td>
<td><span data-ttu-id="7a744-675">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-675">Electricity</span></span></td>
<td><span data-ttu-id="7a744-676">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-676">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-677">500,00</span><span class="sxs-lookup"><span data-stu-id="7a744-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-678">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a744-679">CC001</span><span class="sxs-lookup"><span data-stu-id="7a744-679">CC001</span></span></td>
<td><span data-ttu-id="7a744-680">Mannauður</span><span class="sxs-lookup"><span data-stu-id="7a744-680">HR</span></span></td>
<td><span data-ttu-id="7a744-681">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-681">10001</span></span></td>
<td><span data-ttu-id="7a744-682">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-682">Electricity</span></span></td>
<td><span data-ttu-id="7a744-683">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-683">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="7a744-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-685">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a744-686">CC002</span><span class="sxs-lookup"><span data-stu-id="7a744-686">CC002</span></span></td>
<td><span data-ttu-id="7a744-687">Fjármál</span><span class="sxs-lookup"><span data-stu-id="7a744-687">Finance</span></span></td>
<td><span data-ttu-id="7a744-688">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-688">10001</span></span></td>
<td><span data-ttu-id="7a744-689">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-689">Electricity</span></span></td>
<td><span data-ttu-id="7a744-690">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-690">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-691">675.00</span><span class="sxs-lookup"><span data-stu-id="7a744-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-692">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a744-693">CC002</span><span class="sxs-lookup"><span data-stu-id="7a744-693">CC002</span></span></td>
<td><span data-ttu-id="7a744-694">Fjármál</span><span class="sxs-lookup"><span data-stu-id="7a744-694">Finance</span></span></td>
<td><span data-ttu-id="7a744-695">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-695">10001</span></span></td>
<td><span data-ttu-id="7a744-696">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-696">Electricity</span></span></td>
<td><span data-ttu-id="7a744-697">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-697">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="7a744-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-699">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a744-700">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-700">CC003</span></span></td>
<td><span data-ttu-id="7a744-701">Smölun</span><span class="sxs-lookup"><span data-stu-id="7a744-701">Assembly</span></span></td>
<td><span data-ttu-id="7a744-702">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-702">10001</span></span></td>
<td><span data-ttu-id="7a744-703">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-703">Electricity</span></span></td>
<td><span data-ttu-id="7a744-704">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-704">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-705">713.75</span><span class="sxs-lookup"><span data-stu-id="7a744-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-706">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a744-707">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-707">CC003</span></span></td>
<td><span data-ttu-id="7a744-708">Smölun</span><span class="sxs-lookup"><span data-stu-id="7a744-708">Assembly</span></span></td>
<td><span data-ttu-id="7a744-709">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-709">10001</span></span></td>
<td><span data-ttu-id="7a744-710">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-710">Electricity</span></span></td>
<td><span data-ttu-id="7a744-711">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-711">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="7a744-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-713">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a744-714">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-714">CC003</span></span></td>
<td><span data-ttu-id="7a744-715">Pakkning</span><span class="sxs-lookup"><span data-stu-id="7a744-715">Packaging</span></span></td>
<td><span data-ttu-id="7a744-716">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-716">10001</span></span></td>
<td><span data-ttu-id="7a744-717">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-717">Electricity</span></span></td>
<td><span data-ttu-id="7a744-718">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-718">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-719">286.25</span><span class="sxs-lookup"><span data-stu-id="7a744-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-720">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a744-721">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-721">CC003</span></span></td>
<td><span data-ttu-id="7a744-722">Pakkning</span><span class="sxs-lookup"><span data-stu-id="7a744-722">Packaging</span></span></td>
<td><span data-ttu-id="7a744-723">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-723">10001</span></span></td>
<td><span data-ttu-id="7a744-724">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-724">Electricity</span></span></td>
<td><span data-ttu-id="7a744-725">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-725">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="7a744-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-727">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a744-728">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-728">Prod 1</span></span></td>
<td><span data-ttu-id="7a744-729">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-729">Product 1</span></span></td>
<td><span data-ttu-id="7a744-730">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-730">10001</span></span></td>
<td><span data-ttu-id="7a744-731">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-731">Electricity</span></span></td>
<td><span data-ttu-id="7a744-732">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-732">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-733">776.36</span><span class="sxs-lookup"><span data-stu-id="7a744-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-734">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a744-735">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-735">Prod 1</span></span></td>
<td><span data-ttu-id="7a744-736">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-736">Product 1</span></span></td>
<td><span data-ttu-id="7a744-737">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-737">10001</span></span></td>
<td><span data-ttu-id="7a744-738">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-738">Electricity</span></span></td>
<td><span data-ttu-id="7a744-739">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-739">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="7a744-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-741">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a744-742">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-742">Prod 2</span></span></td>
<td><span data-ttu-id="7a744-743">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-743">Product 1</span></span></td>
<td><span data-ttu-id="7a744-744">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-744">10001</span></span></td>
<td><span data-ttu-id="7a744-745">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-745">Electricity</span></span></td>
<td><span data-ttu-id="7a744-746">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-746">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-747">223.64</span><span class="sxs-lookup"><span data-stu-id="7a744-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-748">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="7a744-749">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-749">Prod 2</span></span></td>
<td><span data-ttu-id="7a744-750">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-750">Product 1</span></span></td>
<td><span data-ttu-id="7a744-751">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-751">10001</span></span></td>
<td><span data-ttu-id="7a744-752">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-752">Electricity</span></span></td>
<td><span data-ttu-id="7a744-753">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-753">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="7a744-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="7a744-755">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="7a744-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="7a744-756">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="7a744-757">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="7a744-757">Cost element</span></span></th>
<th><span data-ttu-id="7a744-758">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="7a744-758">Cost behavior</span></span></th>
<th><span data-ttu-id="7a744-759">Upphæð</span><span class="sxs-lookup"><span data-stu-id="7a744-759">Amount</span></span></th>
<th><span data-ttu-id="7a744-760">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="7a744-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="7a744-761">CC001</span><span class="sxs-lookup"><span data-stu-id="7a744-761">CC001</span></span></td>
<td><span data-ttu-id="7a744-762">Mannauður</span><span class="sxs-lookup"><span data-stu-id="7a744-762">HR</span></span></td>
<td><span data-ttu-id="7a744-763">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-763">10001</span></span></td>
<td><span data-ttu-id="7a744-764">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-764">Electricity</span></span></td>
<td><span data-ttu-id="7a744-765">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-765">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="7a744-766">-500.00</span></span></td>
<td><span data-ttu-id="7a744-767">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-768">CC002</span><span class="sxs-lookup"><span data-stu-id="7a744-768">CC002</span></span></td>
<td><span data-ttu-id="7a744-769">Fjármál</span><span class="sxs-lookup"><span data-stu-id="7a744-769">Finance</span></span></td>
<td><span data-ttu-id="7a744-770">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-770">10001</span></span></td>
<td><span data-ttu-id="7a744-771">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-771">Electricity</span></span></td>
<td><span data-ttu-id="7a744-772">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-772">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-773">175.00</span><span class="sxs-lookup"><span data-stu-id="7a744-773">175.00</span></span></td>
<td><span data-ttu-id="7a744-774">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-775">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-775">CC003</span></span></td>
<td><span data-ttu-id="7a744-776">Smölun</span><span class="sxs-lookup"><span data-stu-id="7a744-776">Assembly</span></span></td>
<td><span data-ttu-id="7a744-777">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-777">10001</span></span></td>
<td><span data-ttu-id="7a744-778">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-778">Electricity</span></span></td>
<td><span data-ttu-id="7a744-779">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-779">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-780">275.00</span><span class="sxs-lookup"><span data-stu-id="7a744-780">275.00</span></span></td>
<td><span data-ttu-id="7a744-781">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-782">CC004</span><span class="sxs-lookup"><span data-stu-id="7a744-782">CC004</span></span></td>
<td><span data-ttu-id="7a744-783">Pakkning</span><span class="sxs-lookup"><span data-stu-id="7a744-783">Packaging</span></span></td>
<td><span data-ttu-id="7a744-784">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-784">10001</span></span></td>
<td><span data-ttu-id="7a744-785">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-785">Electricity</span></span></td>
<td><span data-ttu-id="7a744-786">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-786">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-787">50,00</span><span class="sxs-lookup"><span data-stu-id="7a744-787">50,00</span></span></td>
<td><span data-ttu-id="7a744-788">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-789">CC001</span><span class="sxs-lookup"><span data-stu-id="7a744-789">CC001</span></span></td>
<td><span data-ttu-id="7a744-790">Mannauður</span><span class="sxs-lookup"><span data-stu-id="7a744-790">HR</span></span></td>
<td><span data-ttu-id="7a744-791">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-791">10001</span></span></td>
<td><span data-ttu-id="7a744-792">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-792">Electricity</span></span></td>
<td><span data-ttu-id="7a744-793">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-793">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="7a744-794">-1,245.71</span></span></td>
<td><span data-ttu-id="7a744-795">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-796">CC002</span><span class="sxs-lookup"><span data-stu-id="7a744-796">CC002</span></span></td>
<td><span data-ttu-id="7a744-797">Fjármál</span><span class="sxs-lookup"><span data-stu-id="7a744-797">Finance</span></span></td>
<td><span data-ttu-id="7a744-798">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-798">10001</span></span></td>
<td><span data-ttu-id="7a744-799">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-799">Electricity</span></span></td>
<td><span data-ttu-id="7a744-800">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-800">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-801">436.00</span><span class="sxs-lookup"><span data-stu-id="7a744-801">436.00</span></span></td>
<td><span data-ttu-id="7a744-802">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-803">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-803">CC003</span></span></td>
<td><span data-ttu-id="7a744-804">Smölun</span><span class="sxs-lookup"><span data-stu-id="7a744-804">Assembly</span></span></td>
<td><span data-ttu-id="7a744-805">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-805">10001</span></span></td>
<td><span data-ttu-id="7a744-806">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-806">Electricity</span></span></td>
<td><span data-ttu-id="7a744-807">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-807">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-808">685.14</span><span class="sxs-lookup"><span data-stu-id="7a744-808">685.14</span></span></td>
<td><span data-ttu-id="7a744-809">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-810">CC004</span><span class="sxs-lookup"><span data-stu-id="7a744-810">CC004</span></span></td>
<td><span data-ttu-id="7a744-811">Pakkning</span><span class="sxs-lookup"><span data-stu-id="7a744-811">Packaging</span></span></td>
<td><span data-ttu-id="7a744-812">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-812">10001</span></span></td>
<td><span data-ttu-id="7a744-813">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-813">Electricity</span></span></td>
<td><span data-ttu-id="7a744-814">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-814">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-815">124.57</span><span class="sxs-lookup"><span data-stu-id="7a744-815">124.57</span></span></td>
<td><span data-ttu-id="7a744-816">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-817">CC002</span><span class="sxs-lookup"><span data-stu-id="7a744-817">CC002</span></span></td>
<td><span data-ttu-id="7a744-818">Fjármál</span><span class="sxs-lookup"><span data-stu-id="7a744-818">Finance</span></span></td>
<td><span data-ttu-id="7a744-819">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-819">10001</span></span></td>
<td><span data-ttu-id="7a744-820">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-820">Electricity</span></span></td>
<td><span data-ttu-id="7a744-821">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-821">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="7a744-822">-675.00</span></span></td>
<td><span data-ttu-id="7a744-823">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-824">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-824">CC003</span></span></td>
<td><span data-ttu-id="7a744-825">Smölun</span><span class="sxs-lookup"><span data-stu-id="7a744-825">Assembly</span></span></td>
<td><span data-ttu-id="7a744-826">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-826">10001</span></span></td>
<td><span data-ttu-id="7a744-827">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-827">Electricity</span></span></td>
<td><span data-ttu-id="7a744-828">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-828">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-829">438.75</span><span class="sxs-lookup"><span data-stu-id="7a744-829">438.75</span></span></td>
<td><span data-ttu-id="7a744-830">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-831">CC004</span><span class="sxs-lookup"><span data-stu-id="7a744-831">CC004</span></span></td>
<td><span data-ttu-id="7a744-832">Pakkning</span><span class="sxs-lookup"><span data-stu-id="7a744-832">Packaging</span></span></td>
<td><span data-ttu-id="7a744-833">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-833">10001</span></span></td>
<td><span data-ttu-id="7a744-834">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-834">Electricity</span></span></td>
<td><span data-ttu-id="7a744-835">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-835">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-836">236.25</span><span class="sxs-lookup"><span data-stu-id="7a744-836">236.25</span></span></td>
<td><span data-ttu-id="7a744-837">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-838">CC002</span><span class="sxs-lookup"><span data-stu-id="7a744-838">CC002</span></span></td>
<td><span data-ttu-id="7a744-839">Fjármál</span><span class="sxs-lookup"><span data-stu-id="7a744-839">Finance</span></span></td>
<td><span data-ttu-id="7a744-840">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-840">10001</span></span></td>
<td><span data-ttu-id="7a744-841">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-841">Electricity</span></span></td>
<td><span data-ttu-id="7a744-842">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-842">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="7a744-843">-8,150.29</span></span></td>
<td><span data-ttu-id="7a744-844">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-845">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-845">CC003</span></span></td>
<td><span data-ttu-id="7a744-846">Smölun</span><span class="sxs-lookup"><span data-stu-id="7a744-846">Assembly</span></span></td>
<td><span data-ttu-id="7a744-847">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-847">10001</span></span></td>
<td><span data-ttu-id="7a744-848">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-848">Electricity</span></span></td>
<td><span data-ttu-id="7a744-849">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-849">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="7a744-850">5,297.69</span></span></td>
<td><span data-ttu-id="7a744-851">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-852">CC004</span><span class="sxs-lookup"><span data-stu-id="7a744-852">CC004</span></span></td>
<td><span data-ttu-id="7a744-853">Pakkning</span><span class="sxs-lookup"><span data-stu-id="7a744-853">Packaging</span></span></td>
<td><span data-ttu-id="7a744-854">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-854">10001</span></span></td>
<td><span data-ttu-id="7a744-855">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-855">Electricity</span></span></td>
<td><span data-ttu-id="7a744-856">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-856">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="7a744-857">2,852.60</span></span></td>
<td><span data-ttu-id="7a744-858">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-859">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-859">CC003</span></span></td>
<td><span data-ttu-id="7a744-860">Smölun</span><span class="sxs-lookup"><span data-stu-id="7a744-860">Assembly</span></span></td>
<td><span data-ttu-id="7a744-861">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-861">10001</span></span></td>
<td><span data-ttu-id="7a744-862">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-862">Electricity</span></span></td>
<td><span data-ttu-id="7a744-863">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-863">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="7a744-864">-713.75</span></span></td>
<td><span data-ttu-id="7a744-865">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-866">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-866">Prod 1</span></span></td>
<td><span data-ttu-id="7a744-867">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-867">Product 1</span></span></td>
<td><span data-ttu-id="7a744-868">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-868">10001</span></span></td>
<td><span data-ttu-id="7a744-869">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-869">Electricity</span></span></td>
<td><span data-ttu-id="7a744-870">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-870">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-871">535.31</span><span class="sxs-lookup"><span data-stu-id="7a744-871">535.31</span></span></td>
<td><span data-ttu-id="7a744-872">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-873">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-873">Prod 2</span></span></td>
<td><span data-ttu-id="7a744-874">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-874">Product 2</span></span></td>
<td><span data-ttu-id="7a744-875">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-875">10001</span></span></td>
<td><span data-ttu-id="7a744-876">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-876">Electricity</span></span></td>
<td><span data-ttu-id="7a744-877">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-877">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-878">178.44</span><span class="sxs-lookup"><span data-stu-id="7a744-878">178.44</span></span></td>
<td><span data-ttu-id="7a744-879">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-880">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-880">CC003</span></span></td>
<td><span data-ttu-id="7a744-881">Smölun</span><span class="sxs-lookup"><span data-stu-id="7a744-881">Assembly</span></span></td>
<td><span data-ttu-id="7a744-882">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-882">10001</span></span></td>
<td><span data-ttu-id="7a744-883">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-883">Electricity</span></span></td>
<td><span data-ttu-id="7a744-884">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-884">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="7a744-885">-5,982.83</span></span></td>
<td><span data-ttu-id="7a744-886">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-887">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-887">Prod 1</span></span></td>
<td><span data-ttu-id="7a744-888">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-888">Product 1</span></span></td>
<td><span data-ttu-id="7a744-889">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-889">10001</span></span></td>
<td><span data-ttu-id="7a744-890">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-890">Electricity</span></span></td>
<td><span data-ttu-id="7a744-891">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-891">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="7a744-892">4,487.12</span></span></td>
<td><span data-ttu-id="7a744-893">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-894">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-894">Prod 2</span></span></td>
<td><span data-ttu-id="7a744-895">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-895">Product 2</span></span></td>
<td><span data-ttu-id="7a744-896">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-896">10001</span></span></td>
<td><span data-ttu-id="7a744-897">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-897">Electricity</span></span></td>
<td><span data-ttu-id="7a744-898">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-898">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="7a744-899">1,495.71</span></span></td>
<td><span data-ttu-id="7a744-900">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-901">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-901">CC003</span></span></td>
<td><span data-ttu-id="7a744-902">Smölun</span><span class="sxs-lookup"><span data-stu-id="7a744-902">Assembly</span></span></td>
<td><span data-ttu-id="7a744-903">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-903">10001</span></span></td>
<td><span data-ttu-id="7a744-904">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-904">Electricity</span></span></td>
<td><span data-ttu-id="7a744-905">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-905">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="7a744-906">-286.25</span></span></td>
<td><span data-ttu-id="7a744-907">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-908">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-908">Prod 1</span></span></td>
<td><span data-ttu-id="7a744-909">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-909">Product 1</span></span></td>
<td><span data-ttu-id="7a744-910">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-910">10001</span></span></td>
<td><span data-ttu-id="7a744-911">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-911">Electricity</span></span></td>
<td><span data-ttu-id="7a744-912">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-912">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-913">241.05</span><span class="sxs-lookup"><span data-stu-id="7a744-913">241.05</span></span></td>
<td><span data-ttu-id="7a744-914">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-915">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-915">Prod 2</span></span></td>
<td><span data-ttu-id="7a744-916">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-916">Product 2</span></span></td>
<td><span data-ttu-id="7a744-917">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-917">10001</span></span></td>
<td><span data-ttu-id="7a744-918">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-918">Electricity</span></span></td>
<td><span data-ttu-id="7a744-919">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-919">Fixed cost</span></span></td>
<td><span data-ttu-id="7a744-920">45.20</span><span class="sxs-lookup"><span data-stu-id="7a744-920">45.20</span></span></td>
<td><span data-ttu-id="7a744-921">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-922">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-922">CC003</span></span></td>
<td><span data-ttu-id="7a744-923">Smölun</span><span class="sxs-lookup"><span data-stu-id="7a744-923">Assembly</span></span></td>
<td><span data-ttu-id="7a744-924">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-924">10001</span></span></td>
<td><span data-ttu-id="7a744-925">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-925">Electricity</span></span></td>
<td><span data-ttu-id="7a744-926">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-926">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="7a744-927">-2,977.17</span></span></td>
<td><span data-ttu-id="7a744-928">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-929">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-929">Prod 1</span></span></td>
<td><span data-ttu-id="7a744-930">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-930">Product 1</span></span></td>
<td><span data-ttu-id="7a744-931">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-931">10001</span></span></td>
<td><span data-ttu-id="7a744-932">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-932">Electricity</span></span></td>
<td><span data-ttu-id="7a744-933">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-933">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="7a744-934">2,507.09</span></span></td>
<td><span data-ttu-id="7a744-935">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="7a744-936">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-936">Prod 2</span></span></td>
<td><span data-ttu-id="7a744-937">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-937">Product 2</span></span></td>
<td><span data-ttu-id="7a744-938">10001</span><span class="sxs-lookup"><span data-stu-id="7a744-938">10001</span></span></td>
<td><span data-ttu-id="7a744-939">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-939">Electricity</span></span></td>
<td><span data-ttu-id="7a744-940">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-940">Variable cost</span></span></td>
<td><span data-ttu-id="7a744-941">470.08</span><span class="sxs-lookup"><span data-stu-id="7a744-941">470.08</span></span></td>
<td><span data-ttu-id="7a744-942">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="7a744-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="7a744-943">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="7a744-943">Conclusion</span></span>
<span data-ttu-id="7a744-944">Í Fjárhagsbókhaldi er kostnaður upp á 10.000,00 fyrir rafmagn bókaður á kenni leppkostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="7a744-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="7a744-945">Þar af leiðandi munu kostnaðarbókarar vita að það þarf að úthluta þessum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="7a744-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="7a744-946">Í kostnaðarbókhaldi streymir kostnaður þvert á fyrirtækiseiningar og stig, samkvæmt þeim stefnum og reglum sem eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="7a744-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="7a744-947">Hver kostnaður hefur verið tengdur úthlutunargrunni sem veitir besta mat á úthlutun á kostnaði.</span><span class="sxs-lookup"><span data-stu-id="7a744-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="7a744-948">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="7a744-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="7a744-949">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="7a744-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="7a744-950">Samtala</span><span class="sxs-lookup"><span data-stu-id="7a744-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="7a744-951">CC099</span><span class="sxs-lookup"><span data-stu-id="7a744-951">CC099</span></span></th>
<th><span data-ttu-id="7a744-952">CC001</span><span class="sxs-lookup"><span data-stu-id="7a744-952">CC001</span></span></th>
<th><span data-ttu-id="7a744-953">CC002</span><span class="sxs-lookup"><span data-stu-id="7a744-953">CC002</span></span></th>
<th><span data-ttu-id="7a744-954">CC003</span><span class="sxs-lookup"><span data-stu-id="7a744-954">CC003</span></span></th>
<th><span data-ttu-id="7a744-955">CC004</span><span class="sxs-lookup"><span data-stu-id="7a744-955">CC004</span></span></th>
<th><span data-ttu-id="7a744-956">Verk 1</span><span class="sxs-lookup"><span data-stu-id="7a744-956">Proj 1</span></span></th>
<th><span data-ttu-id="7a744-957">Verk 2</span><span class="sxs-lookup"><span data-stu-id="7a744-957">Proj 2</span></span></th>
<th><span data-ttu-id="7a744-958">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="7a744-958">Prod 1</span></span></th>
<th><span data-ttu-id="7a744-959">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="7a744-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="7a744-960">10001 Rafmagn</span><span class="sxs-lookup"><span data-stu-id="7a744-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7a744-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7a744-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7a744-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="7a744-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="7a744-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="7a744-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="7a744-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="7a744-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="7a744-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="7a744-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="7a744-970">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="7a744-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-971">0,00</span><span class="sxs-lookup"><span data-stu-id="7a744-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="7a744-972">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-973">0,00</span><span class="sxs-lookup"><span data-stu-id="7a744-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-974">0,00</span><span class="sxs-lookup"><span data-stu-id="7a744-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-975">0,00</span><span class="sxs-lookup"><span data-stu-id="7a744-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-976">0,00</span><span class="sxs-lookup"><span data-stu-id="7a744-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-977">0,00</span><span class="sxs-lookup"><span data-stu-id="7a744-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="7a744-978">776.36</span><span class="sxs-lookup"><span data-stu-id="7a744-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-979">223.64</span><span class="sxs-lookup"><span data-stu-id="7a744-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="7a744-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="7a744-981">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="7a744-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-982">000</span><span class="sxs-lookup"><span data-stu-id="7a744-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-983">0,00</span><span class="sxs-lookup"><span data-stu-id="7a744-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-984">0,00</span><span class="sxs-lookup"><span data-stu-id="7a744-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-985">0,00</span><span class="sxs-lookup"><span data-stu-id="7a744-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-986">0,00</span><span class="sxs-lookup"><span data-stu-id="7a744-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-987">30,00</span><span class="sxs-lookup"><span data-stu-id="7a744-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-988">10,00</span><span class="sxs-lookup"><span data-stu-id="7a744-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="7a744-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="7a744-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="7a744-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="7a744-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="7a744-992">Þetta efnisatriði sýnir hvernig fyrir aðalkostnaðareiningin 10001 Rafmagn flæðir í gegnum kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="7a744-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="7a744-993">Þar af leiðandi er þessum sameiginlega kostnaði úthlutað á lægsta stigið í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="7a744-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="7a744-994">Með öðrum orðum bera kostnaðarhlutir á lægsta stiginu kostnaðinn.</span><span class="sxs-lookup"><span data-stu-id="7a744-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="7a744-995">Ef þú þarft sjónrænt flæði kostnaðar á milli kostnaðarhluta er hægt að nota stefnureglur samantekins kostnaðar til að gera kostnaðarflæðið sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="7a744-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="7a744-996">Fyrir frekari upplýsingar skal sjá [Stefna fyrir samantekt kostnaðar og útreikning sameiginlegs kostnaðar](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="7a744-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]