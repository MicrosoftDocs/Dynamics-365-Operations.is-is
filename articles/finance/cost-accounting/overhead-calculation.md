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
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roschlom
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 923e6e38a664e17ec3349d839c4b77ec903c5dc2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444491"
---
# <a name="overhead-calculation"></a><span data-ttu-id="07518-103">Útreikningur fastakostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07518-104">Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði.</span><span class="sxs-lookup"><span data-stu-id="07518-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="07518-105">Skýrsluskilgreining</span><span class="sxs-lookup"><span data-stu-id="07518-105">Term definition</span></span>
---------------

<span data-ttu-id="07518-106">Stjórnunarkostnaður er sá kostnaður sem stofnað er til fyrir rekstur fyrirtækis, en sem ekki er hægt að rekja beint til neinna sérstakrar starfsemi, vöru eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="07518-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="07518-107">Stjórnunarkostnaður veitir mikilvægan stuðning við myndun hagnaðarmyndandi verkþátta.</span><span class="sxs-lookup"><span data-stu-id="07518-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="07518-108">Hér eru nokkur dæmi um skilyrði:</span><span class="sxs-lookup"><span data-stu-id="07518-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="07518-109">Leiga</span><span class="sxs-lookup"><span data-stu-id="07518-109">Rent</span></span>
-   <span data-ttu-id="07518-110">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-110">Electricity</span></span>
-   <span data-ttu-id="07518-111">Stjórnunarkostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="07518-112">Yfirlit yfir útreikning fastakostnaðar</span><span class="sxs-lookup"><span data-stu-id="07518-112">Overhead calculation overview</span></span>
<span data-ttu-id="07518-113">Útreikningur fastakostnaðar keyrir reglur kostnaðarbókhalds í réttri röð.</span><span class="sxs-lookup"><span data-stu-id="07518-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="07518-114">Hægt er að keyra útreikning fastakostnaðar margsinnis fyrir sama fjárhagstímabil ef reglum kostnaðarbókhalds hefur verið breytt eða ákveðnar villur hafa fundist.</span><span class="sxs-lookup"><span data-stu-id="07518-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="07518-115">Hver keyrsla á útreikningi fastakostnaðar er geymd og fær einkvæmt útgáfukenni sem gerir kleift að bera saman útreikning í mismunandi útgáfum.</span><span class="sxs-lookup"><span data-stu-id="07518-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="07518-116">Kostnaðarfærslur sem útreikningur fastakostnaðar mynda fá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="07518-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="07518-117">Dagsetningin bókhald samsvarar lokadagsetning fjárhagstímabilsins sem er dagsetning reikningsskiladagsetning reikningsskila notað í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="07518-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="07518-118">Einkvæmt útgáfukenni samanstendur af eftirfarandi þáttum:</span><span class="sxs-lookup"><span data-stu-id="07518-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="07518-119">Gerð útgáfu</span><span class="sxs-lookup"><span data-stu-id="07518-119">Version type</span></span>
-   <span data-ttu-id="07518-120">Dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="07518-120">Date and time</span></span>
-   <span data-ttu-id="07518-121">Fjárhagur kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="07518-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="07518-122">Fjárhagsár</span><span class="sxs-lookup"><span data-stu-id="07518-122">Fiscal year</span></span>
-   <span data-ttu-id="07518-123">Reikningstímabil</span><span class="sxs-lookup"><span data-stu-id="07518-123">Fiscal period</span></span>

<span data-ttu-id="07518-124">Útreikningur fastakostnaðar er keyrður óháð því hver útgáfan er.</span><span class="sxs-lookup"><span data-stu-id="07518-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="07518-125">Þess vegna er hægt að reikna út áætlaða útgáfu á undan raunútgáfu.</span><span class="sxs-lookup"><span data-stu-id="07518-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="07518-126">Útreikningur fastakostnaðar samanstendur af fjórum skrefum, eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="07518-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="07518-127">Í hverju skrefi er færslubókarhaus stofnaður með bókarfærslum.</span><span class="sxs-lookup"><span data-stu-id="07518-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="07518-128">Þessi færslubókarhaus geymir inntaksgögn fyrir hvert útreikningsþrep.</span><span class="sxs-lookup"><span data-stu-id="07518-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="07518-129">Stefnur og reglur eru notaðar í hverri færslulínu og kostnaðarfærslur eru myndaðar sem úttak.</span><span class="sxs-lookup"><span data-stu-id="07518-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="07518-130">Þess vegna hefurðu ávallt fullan rekjanleika.</span><span class="sxs-lookup"><span data-stu-id="07518-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="07518-131">[![Útreikningur fastakostnaðar](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="07518-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="07518-132">Reikna og úthluta sameiginlegur kostnaði vegna rafmagns</span><span class="sxs-lookup"><span data-stu-id="07518-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="07518-133">Í Fjárhagsbókhaldi er ákveðinn kostnaður, eins og rafmagn, skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="07518-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="07518-134">Þar af leiðandi er nákvæmar innsýn rekstrarfélags ekki veitt fyrir kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="07518-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="07518-135">Í kostnaðarbókhaldi verður kostnaður að flæða í gegnum fyrirtækiseiningar til að veita rétta innsýn rekstrarfélags þvert á allar fyrirtækiseiningar og stig.</span><span class="sxs-lookup"><span data-stu-id="07518-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="07518-136">Þetta flæði verður að byggja á annaðhvort nákvæmri færslu notkunar eða sanngjarnri matsreglu.</span><span class="sxs-lookup"><span data-stu-id="07518-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="07518-137">Í fjárhagnum er hægt að bóka rafmagnskostnað eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="07518-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07518-138">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="07518-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="07518-139">Kostnaðarstaður</span><span class="sxs-lookup"><span data-stu-id="07518-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="07518-140">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="07518-140">Main account</span></span></th>
<th><span data-ttu-id="07518-141">Upphæð í bókhaldsgjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="07518-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-142">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="07518-143">CC099</span><span class="sxs-lookup"><span data-stu-id="07518-143">CC099</span></span></td>
<td><span data-ttu-id="07518-144">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="07518-144">Default cost center</span></span></td>
<td><span data-ttu-id="07518-145">10001</span><span class="sxs-lookup"><span data-stu-id="07518-145">10001</span></span></td>
<td><span data-ttu-id="07518-146">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-146">Electricity</span></span></td>
<td><span data-ttu-id="07518-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="07518-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="07518-148">Skref 1: Keyra útreikning kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="07518-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="07518-149">Sjálfvirkt er að þegar kostnaðarfærslur eru fluttar úr grunngögnum fái þær flokkun kostnaðarhegðunar **Óflokkað** í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="07518-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="07518-150">Með því að nota stefnureglur kostnaðarhegðunar er hægt að endurflokka kostnaðarfærslur sem annaðhvort **Fastan kostnað** eða **Breytilegan kostnað**.</span><span class="sxs-lookup"><span data-stu-id="07518-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="07518-151">Tilgreinið reglu kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="07518-151">Define the cost behavior rule</span></span>

<span data-ttu-id="07518-152">Í sumum tilfellum er hluti af kostnaði föst þóknun og eftirstandandi kostnaður byggist á notkun.</span><span class="sxs-lookup"><span data-stu-id="07518-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="07518-153">Rafmagnsreikningar stemma oft við þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="07518-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="07518-154">Þegar tiltekin föst þóknun hefur verið greidd, er greitt fyrir notkun á kílóvattklukkustund (Kwh).</span><span class="sxs-lookup"><span data-stu-id="07518-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="07518-155">Til dæmis ef föst kostnaðarþóknun er 1000.00 sýnir þetta hvernig regla kostnaðarhegðunar er skilgreind:</span><span class="sxs-lookup"><span data-stu-id="07518-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="07518-156">Föst upphæð 1.000,00</span><span class="sxs-lookup"><span data-stu-id="07518-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="07518-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="07518-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="07518-158">1000.01 &lt; N = Breyta</span><span class="sxs-lookup"><span data-stu-id="07518-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="07518-159">Færslubók</span><span class="sxs-lookup"><span data-stu-id="07518-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07518-160">Færslubók</span><span class="sxs-lookup"><span data-stu-id="07518-160">Journal</span></span></th>
<th><span data-ttu-id="07518-161">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="07518-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="07518-162">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="07518-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="07518-163">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="07518-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-164">00001</span><span class="sxs-lookup"><span data-stu-id="07518-164">00001</span></span></td>
<td><span data-ttu-id="07518-165">Færslubók útreiknings fyrir kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="07518-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="07518-166">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="07518-166">Fiscal</span></span></td>
<td><span data-ttu-id="07518-167">2017</span><span class="sxs-lookup"><span data-stu-id="07518-167">2017</span></span></td>
<td><span data-ttu-id="07518-168">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="07518-168">Period 1</span></span></td>
<td><span data-ttu-id="07518-169">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="07518-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="07518-170">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="07518-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07518-171">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="07518-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="07518-172">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="07518-173">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="07518-173">Cost element</span></span></th>
<th><span data-ttu-id="07518-174">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="07518-174">Cost behavior</span></span></th>
<th><span data-ttu-id="07518-175">Upphæð</span><span class="sxs-lookup"><span data-stu-id="07518-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-176">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="07518-177">CC099</span><span class="sxs-lookup"><span data-stu-id="07518-177">CC099</span></span></td>
<td><span data-ttu-id="07518-178">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="07518-178">Default cost center</span></span></td>
<td><span data-ttu-id="07518-179">10001</span><span class="sxs-lookup"><span data-stu-id="07518-179">10001</span></span></td>
<td><span data-ttu-id="07518-180">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-180">Electricity</span></span></td>
<td><span data-ttu-id="07518-181">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="07518-181">Unclassified</span></span></td>
<td><span data-ttu-id="07518-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="07518-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="07518-183">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="07518-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07518-184">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="07518-185">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="07518-185">Cost element</span></span></th>
<th><span data-ttu-id="07518-186">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="07518-186">Cost behavior</span></span></th>
<th><span data-ttu-id="07518-187">Upphæð</span><span class="sxs-lookup"><span data-stu-id="07518-187">Amount</span></span></th>
<th><span data-ttu-id="07518-188">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="07518-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-189">CC099</span><span class="sxs-lookup"><span data-stu-id="07518-189">CC099</span></span></td>
<td><span data-ttu-id="07518-190">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="07518-190">Default cost center</span></span></td>
<td><span data-ttu-id="07518-191">10001</span><span class="sxs-lookup"><span data-stu-id="07518-191">10001</span></span></td>
<td><span data-ttu-id="07518-192">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-192">Electricity</span></span></td>
<td><span data-ttu-id="07518-193">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="07518-193">Unclassified</span></span></td>
<td><span data-ttu-id="07518-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="07518-194">10,000.00</span></span></td>
<td><span data-ttu-id="07518-195">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-196">CC099</span><span class="sxs-lookup"><span data-stu-id="07518-196">CC099</span></span></td>
<td><span data-ttu-id="07518-197">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="07518-197">Default cost center</span></span></td>
<td><span data-ttu-id="07518-198">10001</span><span class="sxs-lookup"><span data-stu-id="07518-198">10001</span></span></td>
<td><span data-ttu-id="07518-199">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-199">Electricity</span></span></td>
<td><span data-ttu-id="07518-200">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="07518-200">Unclassified</span></span></td>
<td><span data-ttu-id="07518-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="07518-201">-10,000.00</span></span></td>
<td><span data-ttu-id="07518-202">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-203">CC099</span><span class="sxs-lookup"><span data-stu-id="07518-203">CC099</span></span></td>
<td><span data-ttu-id="07518-204">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="07518-204">Default cost center</span></span></td>
<td><span data-ttu-id="07518-205">10001</span><span class="sxs-lookup"><span data-stu-id="07518-205">10001</span></span></td>
<td><span data-ttu-id="07518-206">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-206">Electricity</span></span></td>
<td><span data-ttu-id="07518-207">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-207">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="07518-208">1,000.00</span></span></td>
<td><span data-ttu-id="07518-209">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-210">CC099</span><span class="sxs-lookup"><span data-stu-id="07518-210">CC099</span></span></td>
<td><span data-ttu-id="07518-211">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="07518-211">Default cost center</span></span></td>
<td><span data-ttu-id="07518-212">10001</span><span class="sxs-lookup"><span data-stu-id="07518-212">10001</span></span></td>
<td><span data-ttu-id="07518-213">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-213">Electricity</span></span></td>
<td><span data-ttu-id="07518-214">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-214">Variable cost</span></span></td>
<td><span data-ttu-id="07518-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="07518-215">9,000.00</span></span></td>
<td><span data-ttu-id="07518-216">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07518-217">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðarhegðunarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="07518-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="07518-218">Skref 2: Keyra útreikning kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="07518-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="07518-219">Kostnaðardreifing er notuð til að endurúthluta kostnaði frá einum kostnaðarhlut til annars eða fleiri kostnaðarhluta með því að nota viðeigandi úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="07518-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="07518-220">Kostnaðardreifing og kostnaðarúthlutun eru ólíkar að því leyti að kostnaðardreifing kemur alltaf upp á stigi aðalkostnaðareiningar upphaflegs verðs.</span><span class="sxs-lookup"><span data-stu-id="07518-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="07518-221">Tilgreinið kostnaðardreifingarreglu</span><span class="sxs-lookup"><span data-stu-id="07518-221">Define the cost distribution rule</span></span>

<span data-ttu-id="07518-222">Í Fjárhagsbókhaldi er rafmagnskostnaður oft skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="07518-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="07518-223">Í kostnaðarbókhaldi er þessi nálgun ekki nógu nákvæm.</span><span class="sxs-lookup"><span data-stu-id="07518-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="07518-224">Breytilegur kostnaði þarf að dreifa á staka kostnaðarhluti á sanngjörnum grunni.</span><span class="sxs-lookup"><span data-stu-id="07518-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="07518-225">Rökréttasti úthlutunargrunnurinn er notkun á rafmagni (Kwh).</span><span class="sxs-lookup"><span data-stu-id="07518-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="07518-226">Stofnað er tölfræðilegt víddarstak sem er nefnt Rafmagn og rafmagnsnotkun er skráð.</span><span class="sxs-lookup"><span data-stu-id="07518-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="07518-227">Sjálfgefið er að öll tölfræðileg víddarstök verða tiltæk sem úthlutunargrunnur.</span><span class="sxs-lookup"><span data-stu-id="07518-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07518-228">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-228">Cost object</span></span></th>
<th><span data-ttu-id="07518-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="07518-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-230">CC001</span><span class="sxs-lookup"><span data-stu-id="07518-230">CC001</span></span></td>
<td><span data-ttu-id="07518-231">Mannauður</span><span class="sxs-lookup"><span data-stu-id="07518-231">HR</span></span></td>
<td><span data-ttu-id="07518-232">1.000</span><span class="sxs-lookup"><span data-stu-id="07518-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-233">CC002</span><span class="sxs-lookup"><span data-stu-id="07518-233">CC002</span></span></td>
<td><span data-ttu-id="07518-234">Fjármál</span><span class="sxs-lookup"><span data-stu-id="07518-234">Finance</span></span></td>
<td><span data-ttu-id="07518-235">6,000</span><span class="sxs-lookup"><span data-stu-id="07518-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-236">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-236">CC003</span></span></td>
<td><span data-ttu-id="07518-237">Smölun</span><span class="sxs-lookup"><span data-stu-id="07518-237">Assembly</span></span></td>
<td><span data-ttu-id="07518-238">0</span><span class="sxs-lookup"><span data-stu-id="07518-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07518-239">Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunni fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="07518-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07518-240">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-240">Cost object</span></span></th>
<th><span data-ttu-id="07518-241">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="07518-241">Magnitude</span></span></th>
<th><span data-ttu-id="07518-242">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="07518-242">Allocation factor</span></span></th>
<th><span data-ttu-id="07518-243">Upphæð</span><span class="sxs-lookup"><span data-stu-id="07518-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-244">CC001</span><span class="sxs-lookup"><span data-stu-id="07518-244">CC001</span></span></td>
<td><span data-ttu-id="07518-245">Mannauður</span><span class="sxs-lookup"><span data-stu-id="07518-245">HR</span></span></td>
<td><span data-ttu-id="07518-246">1.000</span><span class="sxs-lookup"><span data-stu-id="07518-246">1,000</span></span></td>
<td><span data-ttu-id="07518-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="07518-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="07518-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="07518-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-249">CC002</span><span class="sxs-lookup"><span data-stu-id="07518-249">CC002</span></span></td>
<td><span data-ttu-id="07518-250">Fjármál</span><span class="sxs-lookup"><span data-stu-id="07518-250">Finance</span></span></td>
<td><span data-ttu-id="07518-251">6,000</span><span class="sxs-lookup"><span data-stu-id="07518-251">6,000</span></span></td>
<td><span data-ttu-id="07518-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="07518-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="07518-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="07518-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-254">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-254">CC003</span></span></td>
<td><span data-ttu-id="07518-255">Smölun</span><span class="sxs-lookup"><span data-stu-id="07518-255">Assembly</span></span></td>
<td><span data-ttu-id="07518-256">0</span><span class="sxs-lookup"><span data-stu-id="07518-256">0</span></span></td>
<td><span data-ttu-id="07518-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="07518-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="07518-258">0,00</span><span class="sxs-lookup"><span data-stu-id="07518-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07518-259">Föstum kostnaði þarf að dreifa jafnt á staka kostnaðarhluti sem hafa notað rafmagn.</span><span class="sxs-lookup"><span data-stu-id="07518-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="07518-260">Hægt er að ná þessa niðurstöðu með því að nota tölfræðilegt víddarstakið Rafmagn í úthlutunargrunni reikniformúlu: (Rafmagn &gt; 0,00) Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunn fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="07518-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07518-261">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-261">Cost object</span></span></th>
<th><span data-ttu-id="07518-262">Formúla</span><span class="sxs-lookup"><span data-stu-id="07518-262">Formula</span></span></th>
<th><span data-ttu-id="07518-263">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="07518-263">Magnitude</span></span></th>
<th><span data-ttu-id="07518-264">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="07518-264">Allocation factor</span></span></th>
<th><span data-ttu-id="07518-265">Upphæð</span><span class="sxs-lookup"><span data-stu-id="07518-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-266">CC001</span><span class="sxs-lookup"><span data-stu-id="07518-266">CC001</span></span></td>
<td><span data-ttu-id="07518-267">Mannauður</span><span class="sxs-lookup"><span data-stu-id="07518-267">HR</span></span></td>
<td><span data-ttu-id="07518-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="07518-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="07518-269">1</span><span class="sxs-lookup"><span data-stu-id="07518-269">1</span></span></td>
<td><span data-ttu-id="07518-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="07518-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="07518-271">500,00</span><span class="sxs-lookup"><span data-stu-id="07518-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-272">CC002</span><span class="sxs-lookup"><span data-stu-id="07518-272">CC002</span></span></td>
<td><span data-ttu-id="07518-273">Fjármál</span><span class="sxs-lookup"><span data-stu-id="07518-273">Finance</span></span></td>
<td><span data-ttu-id="07518-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="07518-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="07518-275">1</span><span class="sxs-lookup"><span data-stu-id="07518-275">1</span></span></td>
<td><span data-ttu-id="07518-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="07518-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="07518-277">500,00</span><span class="sxs-lookup"><span data-stu-id="07518-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-278">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-278">CC003</span></span></td>
<td><span data-ttu-id="07518-279">Smölun</span><span class="sxs-lookup"><span data-stu-id="07518-279">Assembly</span></span></td>
<td><span data-ttu-id="07518-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="07518-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="07518-281">0</span><span class="sxs-lookup"><span data-stu-id="07518-281">0</span></span></td>
<td><span data-ttu-id="07518-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="07518-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="07518-283">0,00</span><span class="sxs-lookup"><span data-stu-id="07518-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="07518-284">Færslubók</span><span class="sxs-lookup"><span data-stu-id="07518-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07518-285">Færslubók</span><span class="sxs-lookup"><span data-stu-id="07518-285">Journal</span></span></th>
<th><span data-ttu-id="07518-286">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="07518-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="07518-287">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="07518-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="07518-288">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="07518-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-289">00002</span><span class="sxs-lookup"><span data-stu-id="07518-289">00002</span></span></td>
<td><span data-ttu-id="07518-290">Útreikningabók kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="07518-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="07518-291">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="07518-291">Fiscal</span></span></td>
<td><span data-ttu-id="07518-292">2017</span><span class="sxs-lookup"><span data-stu-id="07518-292">2017</span></span></td>
<td><span data-ttu-id="07518-293">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="07518-293">Period 1</span></span></td>
<td><span data-ttu-id="07518-294">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="07518-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="07518-295">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="07518-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07518-296">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="07518-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="07518-297">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="07518-298">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="07518-298">Cost element</span></span></th>
<th><span data-ttu-id="07518-299">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="07518-299">Cost behavior</span></span></th>
<th><span data-ttu-id="07518-300">Upphæð</span><span class="sxs-lookup"><span data-stu-id="07518-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-301">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="07518-302">CC099</span><span class="sxs-lookup"><span data-stu-id="07518-302">CC099</span></span></td>
<td><span data-ttu-id="07518-303">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="07518-303">Default cost center</span></span></td>
<td><span data-ttu-id="07518-304">10001</span><span class="sxs-lookup"><span data-stu-id="07518-304">10001</span></span></td>
<td><span data-ttu-id="07518-305">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-305">Electricity</span></span></td>
<td><span data-ttu-id="07518-306">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-306">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="07518-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-308">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="07518-309">CC099</span><span class="sxs-lookup"><span data-stu-id="07518-309">CC099</span></span></td>
<td><span data-ttu-id="07518-310">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="07518-310">Default cost center</span></span></td>
<td><span data-ttu-id="07518-311">10001</span><span class="sxs-lookup"><span data-stu-id="07518-311">10001</span></span></td>
<td><span data-ttu-id="07518-312">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-312">Electricity</span></span></td>
<td><span data-ttu-id="07518-313">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-313">Variable cost</span></span></td>
<td><span data-ttu-id="07518-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="07518-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="07518-315">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="07518-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07518-316">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="07518-317">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="07518-317">Cost element</span></span></th>
<th><span data-ttu-id="07518-318">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="07518-318">Cost behavior</span></span></th>
<th><span data-ttu-id="07518-319">Upphæð</span><span class="sxs-lookup"><span data-stu-id="07518-319">Amount</span></span></th>
<th><span data-ttu-id="07518-320">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="07518-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-321">CC099</span><span class="sxs-lookup"><span data-stu-id="07518-321">CC099</span></span></td>
<td><span data-ttu-id="07518-322">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="07518-322">Default cost center</span></span></td>
<td><span data-ttu-id="07518-323">10001</span><span class="sxs-lookup"><span data-stu-id="07518-323">10001</span></span></td>
<td><span data-ttu-id="07518-324">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-324">Electricity</span></span></td>
<td><span data-ttu-id="07518-325">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-325">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="07518-326">-1,000.00</span></span></td>
<td><span data-ttu-id="07518-327">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-328">CC001</span><span class="sxs-lookup"><span data-stu-id="07518-328">CC001</span></span></td>
<td><span data-ttu-id="07518-329">Mannauður</span><span class="sxs-lookup"><span data-stu-id="07518-329">HR</span></span></td>
<td><span data-ttu-id="07518-330">10001</span><span class="sxs-lookup"><span data-stu-id="07518-330">10001</span></span></td>
<td><span data-ttu-id="07518-331">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-331">Electricity</span></span></td>
<td><span data-ttu-id="07518-332">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-332">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-333">500,00</span><span class="sxs-lookup"><span data-stu-id="07518-333">500.00</span></span></td>
<td><span data-ttu-id="07518-334">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-335">CC002</span><span class="sxs-lookup"><span data-stu-id="07518-335">CC002</span></span></td>
<td><span data-ttu-id="07518-336">Fjármál</span><span class="sxs-lookup"><span data-stu-id="07518-336">Finance</span></span></td>
<td><span data-ttu-id="07518-337">10001</span><span class="sxs-lookup"><span data-stu-id="07518-337">10001</span></span></td>
<td><span data-ttu-id="07518-338">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-338">Electricity</span></span></td>
<td><span data-ttu-id="07518-339">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-339">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-340">500,00</span><span class="sxs-lookup"><span data-stu-id="07518-340">500.00</span></span></td>
<td><span data-ttu-id="07518-341">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-342">CC099</span><span class="sxs-lookup"><span data-stu-id="07518-342">CC099</span></span></td>
<td><span data-ttu-id="07518-343">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="07518-343">Default cost center</span></span></td>
<td><span data-ttu-id="07518-344">10001</span><span class="sxs-lookup"><span data-stu-id="07518-344">10001</span></span></td>
<td><span data-ttu-id="07518-345">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-345">Electricity</span></span></td>
<td><span data-ttu-id="07518-346">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-346">Variable cost</span></span></td>
<td><span data-ttu-id="07518-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="07518-347">-9,000.00</span></span></td>
<td><span data-ttu-id="07518-348">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-349">CC001</span><span class="sxs-lookup"><span data-stu-id="07518-349">CC001</span></span></td>
<td><span data-ttu-id="07518-350">Mannauður</span><span class="sxs-lookup"><span data-stu-id="07518-350">HR</span></span></td>
<td><span data-ttu-id="07518-351">10001</span><span class="sxs-lookup"><span data-stu-id="07518-351">10001</span></span></td>
<td><span data-ttu-id="07518-352">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-352">Electricity</span></span></td>
<td><span data-ttu-id="07518-353">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-353">Variable cost</span></span></td>
<td><span data-ttu-id="07518-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="07518-354">1,285.71</span></span></td>
<td><span data-ttu-id="07518-355">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-356">CC002</span><span class="sxs-lookup"><span data-stu-id="07518-356">CC002</span></span></td>
<td><span data-ttu-id="07518-357">Fjármál</span><span class="sxs-lookup"><span data-stu-id="07518-357">Finance</span></span></td>
<td><span data-ttu-id="07518-358">10001</span><span class="sxs-lookup"><span data-stu-id="07518-358">10001</span></span></td>
<td><span data-ttu-id="07518-359">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-359">Electricity</span></span></td>
<td><span data-ttu-id="07518-360">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-360">Variable cost</span></span></td>
<td><span data-ttu-id="07518-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="07518-361">7,714.29</span></span></td>
<td><span data-ttu-id="07518-362">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07518-363">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðardreifingarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="07518-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="07518-364">Skref 3: Keyra útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="07518-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="07518-365">Sameiginlegur kostnaður er notaður til að rukka einn eða fleiri tilgreinda kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="07518-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="07518-366">Gjöldin byggjast á fyrirframákveðnu kostnaðarhlutfalli og mæligildi úr úthlutuðum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="07518-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="07518-367">Skilgreina sameiginlegan kostnað</span><span class="sxs-lookup"><span data-stu-id="07518-367">Define the overhead rate</span></span>

<span data-ttu-id="07518-368">Kostnaðarhlutur CC001 Mannauður stuðlar að safni innri verka.</span><span class="sxs-lookup"><span data-stu-id="07518-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="07518-369">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsverk til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="07518-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07518-370">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-370">Cost object</span></span></th>
<th><span data-ttu-id="07518-371">Tímar</span><span class="sxs-lookup"><span data-stu-id="07518-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-372">Verk 1</span><span class="sxs-lookup"><span data-stu-id="07518-372">Proj 1</span></span></td>
<td><span data-ttu-id="07518-373">Verk 1</span><span class="sxs-lookup"><span data-stu-id="07518-373">Project 1</span></span></td>
<td><span data-ttu-id="07518-374">3</span><span class="sxs-lookup"><span data-stu-id="07518-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-375">Verk 2</span><span class="sxs-lookup"><span data-stu-id="07518-375">Proj 2</span></span></td>
<td><span data-ttu-id="07518-376">Verk 2</span><span class="sxs-lookup"><span data-stu-id="07518-376">Project 2</span></span></td>
<td><span data-ttu-id="07518-377">1</span><span class="sxs-lookup"><span data-stu-id="07518-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07518-378">Fyrirframákveðið kostnaðarhlutfall fyrir kostnaðarframlag verk hefur verið skilgreint.</span><span class="sxs-lookup"><span data-stu-id="07518-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07518-379">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-379">Cost object</span></span></th>
<th><span data-ttu-id="07518-380">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="07518-380">Cost element</span></span></th>
<th><span data-ttu-id="07518-381">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="07518-381">Cost behavior</span></span></th>
<th><span data-ttu-id="07518-382">Einingar</span><span class="sxs-lookup"><span data-stu-id="07518-382">Units</span></span></th>
<th><span data-ttu-id="07518-383">Taxti</span><span class="sxs-lookup"><span data-stu-id="07518-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-384">CC001</span><span class="sxs-lookup"><span data-stu-id="07518-384">CC001</span></span></td>
<td><span data-ttu-id="07518-385">Mannauður</span><span class="sxs-lookup"><span data-stu-id="07518-385">HR</span></span></td>
<td><span data-ttu-id="07518-386">10001</span><span class="sxs-lookup"><span data-stu-id="07518-386">10001</span></span></td>
<td><span data-ttu-id="07518-387">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-387">Variable cost</span></span></td>
<td><span data-ttu-id="07518-388">1</span><span class="sxs-lookup"><span data-stu-id="07518-388">1</span></span></td>
<td><span data-ttu-id="07518-389">10</span><span class="sxs-lookup"><span data-stu-id="07518-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07518-390">Eftirfarandi tafla sýnir niðurstöður þegar Mannauðsverk eru notuð sem grunnur við úthlutun.</span><span class="sxs-lookup"><span data-stu-id="07518-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07518-391">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-391">Cost object</span></span></th>
<th><span data-ttu-id="07518-392">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="07518-392">Magnitude</span></span></th>
<th><span data-ttu-id="07518-393">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="07518-393">Cost element</span></span></th>
<th><span data-ttu-id="07518-394">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="07518-394">Allocation factor</span></span></th>
<th><span data-ttu-id="07518-395">Upphæð</span><span class="sxs-lookup"><span data-stu-id="07518-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-396">Verk 1</span><span class="sxs-lookup"><span data-stu-id="07518-396">Proj 1</span></span></td>
<td><span data-ttu-id="07518-397">Verk 1</span><span class="sxs-lookup"><span data-stu-id="07518-397">Project 1</span></span></td>
<td><span data-ttu-id="07518-398">3</span><span class="sxs-lookup"><span data-stu-id="07518-398">3</span></span></td>
<td><span data-ttu-id="07518-399">10001</span><span class="sxs-lookup"><span data-stu-id="07518-399">10001</span></span></td>
<td><span data-ttu-id="07518-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="07518-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="07518-401">30,00</span><span class="sxs-lookup"><span data-stu-id="07518-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-402">Verk 2</span><span class="sxs-lookup"><span data-stu-id="07518-402">Proj 2</span></span></td>
<td><span data-ttu-id="07518-403">Verk 2</span><span class="sxs-lookup"><span data-stu-id="07518-403">Project 2</span></span></td>
<td><span data-ttu-id="07518-404">1</span><span class="sxs-lookup"><span data-stu-id="07518-404">1</span></span></td>
<td><span data-ttu-id="07518-405">10001</span><span class="sxs-lookup"><span data-stu-id="07518-405">10001</span></span></td>
<td><span data-ttu-id="07518-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="07518-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="07518-407">10,00</span><span class="sxs-lookup"><span data-stu-id="07518-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="07518-408">Færslubók</span><span class="sxs-lookup"><span data-stu-id="07518-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07518-409">Færslubók</span><span class="sxs-lookup"><span data-stu-id="07518-409">Journal</span></span></th>
<th><span data-ttu-id="07518-410">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="07518-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="07518-411">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="07518-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="07518-412">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="07518-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-413">00003</span><span class="sxs-lookup"><span data-stu-id="07518-413">00003</span></span></td>
<td><span data-ttu-id="07518-414">Færslubók fyrir útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="07518-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="07518-415">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="07518-415">Fiscal</span></span></td>
<td><span data-ttu-id="07518-416">2017</span><span class="sxs-lookup"><span data-stu-id="07518-416">2017</span></span></td>
<td><span data-ttu-id="07518-417">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="07518-417">Period 1</span></span></td>
<td><span data-ttu-id="07518-418">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="07518-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="07518-419">Bókarfærslur (Bókarfærslur fyrir útreikning sameiginlegs kostnaðar)</span><span class="sxs-lookup"><span data-stu-id="07518-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07518-420">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="07518-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="07518-421">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-421">Cost object</span></span></th>
<th><span data-ttu-id="07518-422">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="07518-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-423">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="07518-424">Verk 1</span><span class="sxs-lookup"><span data-stu-id="07518-424">Proj 1</span></span></td>
<td><span data-ttu-id="07518-425">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="07518-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="07518-426">3,00</span><span class="sxs-lookup"><span data-stu-id="07518-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-427">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="07518-428">Verk 2</span><span class="sxs-lookup"><span data-stu-id="07518-428">Proj 2</span></span></td>
<td><span data-ttu-id="07518-429">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="07518-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="07518-430">1,00</span><span class="sxs-lookup"><span data-stu-id="07518-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="07518-431">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="07518-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07518-432">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="07518-433">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="07518-433">Cost element</span></span></th>
<th><span data-ttu-id="07518-434">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="07518-434">Cost behavior</span></span></th>
<th><span data-ttu-id="07518-435">Upphæð</span><span class="sxs-lookup"><span data-stu-id="07518-435">Amount</span></span></th>
<th><span data-ttu-id="07518-436">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="07518-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="07518-437">CC0001</span></span></td>
<td><span data-ttu-id="07518-438">Mannauður</span><span class="sxs-lookup"><span data-stu-id="07518-438">HR</span></span></td>
<td><span data-ttu-id="07518-439">10001</span><span class="sxs-lookup"><span data-stu-id="07518-439">10001</span></span></td>
<td><span data-ttu-id="07518-440">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-440">Electricity</span></span></td>
<td><span data-ttu-id="07518-441">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-441">Variable cost</span></span></td>
<td><span data-ttu-id="07518-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="07518-442">-30.00</span></span></td>
<td><span data-ttu-id="07518-443">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-444">Verk 1</span><span class="sxs-lookup"><span data-stu-id="07518-444">Proj 1</span></span></td>
<td><span data-ttu-id="07518-445">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="07518-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="07518-446">10001</span><span class="sxs-lookup"><span data-stu-id="07518-446">10001</span></span></td>
<td><span data-ttu-id="07518-447">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-447">Electricity</span></span></td>
<td><span data-ttu-id="07518-448">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-448">Variable cost</span></span></td>
<td><span data-ttu-id="07518-449">30,00</span><span class="sxs-lookup"><span data-stu-id="07518-449">30.00</span></span></td>
<td><span data-ttu-id="07518-450">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-451">CC001</span><span class="sxs-lookup"><span data-stu-id="07518-451">CC001</span></span></td>
<td><span data-ttu-id="07518-452">Mannauður</span><span class="sxs-lookup"><span data-stu-id="07518-452">HR</span></span></td>
<td><span data-ttu-id="07518-453">10001</span><span class="sxs-lookup"><span data-stu-id="07518-453">10001</span></span></td>
<td><span data-ttu-id="07518-454">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-454">Electricity</span></span></td>
<td><span data-ttu-id="07518-455">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-455">Variable cost</span></span></td>
<td><span data-ttu-id="07518-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="07518-456">-10.00</span></span></td>
<td><span data-ttu-id="07518-457">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-458">Verk 2</span><span class="sxs-lookup"><span data-stu-id="07518-458">Proj 2</span></span></td>
<td><span data-ttu-id="07518-459">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="07518-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="07518-460">10001</span><span class="sxs-lookup"><span data-stu-id="07518-460">10001</span></span></td>
<td><span data-ttu-id="07518-461">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-461">Electricity</span></span></td>
<td><span data-ttu-id="07518-462">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-462">Variable cost</span></span></td>
<td><span data-ttu-id="07518-463">10,00</span><span class="sxs-lookup"><span data-stu-id="07518-463">10.00</span></span></td>
<td><span data-ttu-id="07518-464">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07518-465">Nánari upplýsingar er að finna í [Framkvæma útreikning fastakostnaðar](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="07518-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="07518-466">Skref 4: Keyra útreikning kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="07518-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="07518-467">Úthlutun er notuð til að úthluta stöðu kostnaðarhlutar í öðrum kostnaðarhlutum með því að nota úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="07518-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="07518-468">Finance styður gagnvirka úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="07518-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="07518-469">Í gagnvirkri úthlutunaraðferð er sú sameiginlega þjónusta sem hjálparkostnaðarhlutir skiptast á viðurkennd að fullu.</span><span class="sxs-lookup"><span data-stu-id="07518-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="07518-470">Kerfið ákvarðar sjálfkrafa rétta röð til að framkvæma úthlutun eftir.</span><span class="sxs-lookup"><span data-stu-id="07518-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="07518-471">Stöðu kostnaðarhluta er úthlutað með einum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="07518-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="07518-472">Úthlutanir þvert á víddir kostnaðarhluta og viðkomandi stök þeirra eru studdar.</span><span class="sxs-lookup"><span data-stu-id="07518-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="07518-473">Úthlutun pöntunarinnar er stjórnað af stýrieiningu kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="07518-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="07518-474">[![Gagnkvæm aðferð](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="07518-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="07518-475">Tilgreinið kostnaðarúthlutun</span><span class="sxs-lookup"><span data-stu-id="07518-475">Define the cost allocation</span></span>

<span data-ttu-id="07518-476">Hér er einfalt dæmi sem útskýrir hvernig hægt er að rekja flæði kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="07518-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="07518-477">Kostnaðarhlutir CC001 Mannauður leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="07518-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="07518-478">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="07518-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07518-479">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-479">Cost object</span></span></th>
<th><span data-ttu-id="07518-480">Mannauðsþjónusta</span><span class="sxs-lookup"><span data-stu-id="07518-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-481">CC002</span><span class="sxs-lookup"><span data-stu-id="07518-481">CC002</span></span></td>
<td><span data-ttu-id="07518-482">Fjármál</span><span class="sxs-lookup"><span data-stu-id="07518-482">Finance</span></span></td>
<td><span data-ttu-id="07518-483">35</span><span class="sxs-lookup"><span data-stu-id="07518-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-484">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-484">CC003</span></span></td>
<td><span data-ttu-id="07518-485">Smölun</span><span class="sxs-lookup"><span data-stu-id="07518-485">Assembly</span></span></td>
<td><span data-ttu-id="07518-486">55</span><span class="sxs-lookup"><span data-stu-id="07518-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-487">CC004</span><span class="sxs-lookup"><span data-stu-id="07518-487">CC004</span></span></td>
<td><span data-ttu-id="07518-488">Pakkning</span><span class="sxs-lookup"><span data-stu-id="07518-488">Packaging</span></span></td>
<td><span data-ttu-id="07518-489">10</span><span class="sxs-lookup"><span data-stu-id="07518-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07518-490">Kostnaðarhlutir CC002 Fjármál leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="07518-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="07518-491">Stofnað er tölfræðilegt víddarstak sem kallast Fjármálaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="07518-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07518-492">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-492">Cost object</span></span></th>
<th><span data-ttu-id="07518-493">Fjármálaþjónusta</span><span class="sxs-lookup"><span data-stu-id="07518-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-494">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-494">CC003</span></span></td>
<td><span data-ttu-id="07518-495">Smölun</span><span class="sxs-lookup"><span data-stu-id="07518-495">Assembly</span></span></td>
<td><span data-ttu-id="07518-496">65</span><span class="sxs-lookup"><span data-stu-id="07518-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-497">CC004</span><span class="sxs-lookup"><span data-stu-id="07518-497">CC004</span></span></td>
<td><span data-ttu-id="07518-498">Pakkning</span><span class="sxs-lookup"><span data-stu-id="07518-498">Packaging</span></span></td>
<td><span data-ttu-id="07518-499">35</span><span class="sxs-lookup"><span data-stu-id="07518-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07518-500">Kostnaðarhlutir CC003 Samsetning leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="07518-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="07518-501">Meðlimur tölfræðilega víddar sem kallast Mannauður verk er stofnað til að mælvíddarstaka notuðum magnitude.</span><span class="sxs-lookup"><span data-stu-id="07518-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07518-502">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-502">Cost object</span></span></th>
<th><span data-ttu-id="07518-503">Samsetningarþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="07518-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-504">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-504">Prod 1</span></span></td>
<td><span data-ttu-id="07518-505">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-505">Product 1</span></span></td>
<td><span data-ttu-id="07518-506">60</span><span class="sxs-lookup"><span data-stu-id="07518-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-507">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-507">Prod 2</span></span></td>
<td><span data-ttu-id="07518-508">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-508">Product 2</span></span></td>
<td><span data-ttu-id="07518-509">20</span><span class="sxs-lookup"><span data-stu-id="07518-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07518-510">Kostnaðarhlutir CC004 Umbúðir leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="07518-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="07518-511">Stofnað er tölfræðilegt víddarstak sem kallast Umbúðaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="07518-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07518-512">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-512">Cost object</span></span></th>
<th><span data-ttu-id="07518-513">Umbúðaþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="07518-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-514">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-514">Prod 1</span></span></td>
<td><span data-ttu-id="07518-515">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-515">Product 1</span></span></td>
<td><span data-ttu-id="07518-516">80</span><span class="sxs-lookup"><span data-stu-id="07518-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-517">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-517">Prod 2</span></span></td>
<td><span data-ttu-id="07518-518">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-518">Product 2</span></span></td>
<td><span data-ttu-id="07518-519">15</span><span class="sxs-lookup"><span data-stu-id="07518-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="07518-520">Hægt er að afleiða tölfræðiaðgerðir eins og framleiðslutíma sem vara notar frá upprunagögnum.</span><span class="sxs-lookup"><span data-stu-id="07518-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="07518-521">Nánari upplýsingar er að finna í [Veitusniðmát tölfræðiaðgerðar](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="07518-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="07518-522">Eftirfarandi tafla sýnir niðurstöður þegar mannauðsþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="07518-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07518-523">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-523">Cost object</span></span></th>
<th><span data-ttu-id="07518-524">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="07518-524">Magnitude</span></span></th>
<th><span data-ttu-id="07518-525">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="07518-525">Allocation factor</span></span></th>
<th><span data-ttu-id="07518-526">Upphæð</span><span class="sxs-lookup"><span data-stu-id="07518-526">Amount</span></span></th>
<th><span data-ttu-id="07518-527">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="07518-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-528">CC002</span><span class="sxs-lookup"><span data-stu-id="07518-528">CC002</span></span></td>
<td><span data-ttu-id="07518-529">Fjármál</span><span class="sxs-lookup"><span data-stu-id="07518-529">Finance</span></span></td>
<td><span data-ttu-id="07518-530">35</span><span class="sxs-lookup"><span data-stu-id="07518-530">35</span></span></td>
<td><span data-ttu-id="07518-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="07518-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="07518-532">175.00</span><span class="sxs-lookup"><span data-stu-id="07518-532">175.00</span></span></td>
<td><span data-ttu-id="07518-533">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-534">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-534">CC003</span></span></td>
<td><span data-ttu-id="07518-535">Smölun</span><span class="sxs-lookup"><span data-stu-id="07518-535">Assembly</span></span></td>
<td><span data-ttu-id="07518-536">55</span><span class="sxs-lookup"><span data-stu-id="07518-536">55</span></span></td>
<td><span data-ttu-id="07518-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="07518-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="07518-538">275.00</span><span class="sxs-lookup"><span data-stu-id="07518-538">275.00</span></span></td>
<td><span data-ttu-id="07518-539">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-540">CC004</span><span class="sxs-lookup"><span data-stu-id="07518-540">CC004</span></span></td>
<td><span data-ttu-id="07518-541">Pakkning</span><span class="sxs-lookup"><span data-stu-id="07518-541">Packaging</span></span></td>
<td><span data-ttu-id="07518-542">10</span><span class="sxs-lookup"><span data-stu-id="07518-542">10</span></span></td>
<td><span data-ttu-id="07518-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="07518-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="07518-544">50,00</span><span class="sxs-lookup"><span data-stu-id="07518-544">50.00</span></span></td>
<td><span data-ttu-id="07518-545">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-546">CC002</span><span class="sxs-lookup"><span data-stu-id="07518-546">CC002</span></span></td>
<td><span data-ttu-id="07518-547">Fjármál</span><span class="sxs-lookup"><span data-stu-id="07518-547">Finance</span></span></td>
<td><span data-ttu-id="07518-548">35</span><span class="sxs-lookup"><span data-stu-id="07518-548">35</span></span></td>
<td><span data-ttu-id="07518-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="07518-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="07518-550">436.00</span><span class="sxs-lookup"><span data-stu-id="07518-550">436.00</span></span></td>
<td><span data-ttu-id="07518-551">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-552">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-552">CC003</span></span></td>
<td><span data-ttu-id="07518-553">Smölun</span><span class="sxs-lookup"><span data-stu-id="07518-553">Assembly</span></span></td>
<td><span data-ttu-id="07518-554">55</span><span class="sxs-lookup"><span data-stu-id="07518-554">55</span></span></td>
<td><span data-ttu-id="07518-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="07518-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="07518-556">685.14</span><span class="sxs-lookup"><span data-stu-id="07518-556">685.14</span></span></td>
<td><span data-ttu-id="07518-557">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-558">CC004</span><span class="sxs-lookup"><span data-stu-id="07518-558">CC004</span></span></td>
<td><span data-ttu-id="07518-559">Pakkning</span><span class="sxs-lookup"><span data-stu-id="07518-559">Packaging</span></span></td>
<td><span data-ttu-id="07518-560">10</span><span class="sxs-lookup"><span data-stu-id="07518-560">10</span></span></td>
<td><span data-ttu-id="07518-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="07518-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="07518-562">124.57</span><span class="sxs-lookup"><span data-stu-id="07518-562">124.57</span></span></td>
<td><span data-ttu-id="07518-563">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07518-564">Eftirfarandi tafla sýnir niðurstöður þegar Fjármálaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="07518-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07518-565">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-565">Cost object</span></span></th>
<th><span data-ttu-id="07518-566">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="07518-566">Magnitude</span></span></th>
<th><span data-ttu-id="07518-567">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="07518-567">Allocation factor</span></span></th>
<th><span data-ttu-id="07518-568">Upphæð</span><span class="sxs-lookup"><span data-stu-id="07518-568">Amount</span></span></th>
<th><span data-ttu-id="07518-569">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="07518-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-570">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-570">CC003</span></span></td>
<td><span data-ttu-id="07518-571">Smölun</span><span class="sxs-lookup"><span data-stu-id="07518-571">Assembly</span></span></td>
<td><span data-ttu-id="07518-572">65</span><span class="sxs-lookup"><span data-stu-id="07518-572">65</span></span></td>
<td><span data-ttu-id="07518-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="07518-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="07518-574">438.75</span><span class="sxs-lookup"><span data-stu-id="07518-574">438.75</span></span></td>
<td><span data-ttu-id="07518-575">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-576">CC004</span><span class="sxs-lookup"><span data-stu-id="07518-576">CC004</span></span></td>
<td><span data-ttu-id="07518-577">Pakkning</span><span class="sxs-lookup"><span data-stu-id="07518-577">Packaging</span></span></td>
<td><span data-ttu-id="07518-578">35</span><span class="sxs-lookup"><span data-stu-id="07518-578">35</span></span></td>
<td><span data-ttu-id="07518-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="07518-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="07518-580">236.25</span><span class="sxs-lookup"><span data-stu-id="07518-580">236.25</span></span></td>
<td><span data-ttu-id="07518-581">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-582">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-582">CC003</span></span></td>
<td><span data-ttu-id="07518-583">Smölun</span><span class="sxs-lookup"><span data-stu-id="07518-583">Assembly</span></span></td>
<td><span data-ttu-id="07518-584">65</span><span class="sxs-lookup"><span data-stu-id="07518-584">65</span></span></td>
<td><span data-ttu-id="07518-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="07518-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="07518-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="07518-586">5,297.69</span></span></td>
<td><span data-ttu-id="07518-587">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-588">CC004</span><span class="sxs-lookup"><span data-stu-id="07518-588">CC004</span></span></td>
<td><span data-ttu-id="07518-589">Pakkning</span><span class="sxs-lookup"><span data-stu-id="07518-589">Packaging</span></span></td>
<td><span data-ttu-id="07518-590">35</span><span class="sxs-lookup"><span data-stu-id="07518-590">35</span></span></td>
<td><span data-ttu-id="07518-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="07518-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="07518-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="07518-592">2,852.60</span></span></td>
<td><span data-ttu-id="07518-593">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07518-594">Eftirfarandi tafla sýnir niðurstöður þegar Samsetningarþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="07518-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07518-595">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-595">Cost object</span></span></th>
<th><span data-ttu-id="07518-596">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="07518-596">Magnitude</span></span></th>
<th><span data-ttu-id="07518-597">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="07518-597">Allocation factor</span></span></th>
<th><span data-ttu-id="07518-598">Upphæð</span><span class="sxs-lookup"><span data-stu-id="07518-598">Amount</span></span></th>
<th><span data-ttu-id="07518-599">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="07518-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-600">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-600">Prod 1</span></span></td>
<td><span data-ttu-id="07518-601">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-601">Product 1</span></span></td>
<td><span data-ttu-id="07518-602">60</span><span class="sxs-lookup"><span data-stu-id="07518-602">60</span></span></td>
<td><span data-ttu-id="07518-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="07518-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="07518-604">535.31</span><span class="sxs-lookup"><span data-stu-id="07518-604">535.31</span></span></td>
<td><span data-ttu-id="07518-605">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-606">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-606">Prod 2</span></span></td>
<td><span data-ttu-id="07518-607">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-607">Product 2</span></span></td>
<td><span data-ttu-id="07518-608">20</span><span class="sxs-lookup"><span data-stu-id="07518-608">20</span></span></td>
<td><span data-ttu-id="07518-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="07518-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="07518-610">178.44</span><span class="sxs-lookup"><span data-stu-id="07518-610">178.44</span></span></td>
<td><span data-ttu-id="07518-611">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-612">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-612">Prod 1</span></span></td>
<td><span data-ttu-id="07518-613">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-613">Product 1</span></span></td>
<td><span data-ttu-id="07518-614">60</span><span class="sxs-lookup"><span data-stu-id="07518-614">60</span></span></td>
<td><span data-ttu-id="07518-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="07518-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="07518-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="07518-616">4,487.12</span></span></td>
<td><span data-ttu-id="07518-617">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-618">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-618">Prod 2</span></span></td>
<td><span data-ttu-id="07518-619">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-619">Product 2</span></span></td>
<td><span data-ttu-id="07518-620">20</span><span class="sxs-lookup"><span data-stu-id="07518-620">20</span></span></td>
<td><span data-ttu-id="07518-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="07518-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="07518-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="07518-622">1,495.71</span></span></td>
<td><span data-ttu-id="07518-623">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="07518-624">Eftirfarandi tafla sýnir niðurstöður þegar Umbúðaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="07518-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07518-625">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-625">Cost object</span></span></th>
<th><span data-ttu-id="07518-626">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="07518-626">Magnitude</span></span></th>
<th><span data-ttu-id="07518-627">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="07518-627">Allocation factor</span></span></th>
<th><span data-ttu-id="07518-628">Upphæð</span><span class="sxs-lookup"><span data-stu-id="07518-628">Amount</span></span></th>
<th><span data-ttu-id="07518-629">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="07518-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-630">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-630">Prod 1</span></span></td>
<td><span data-ttu-id="07518-631">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-631">Product 1</span></span></td>
<td><span data-ttu-id="07518-632">80</span><span class="sxs-lookup"><span data-stu-id="07518-632">80</span></span></td>
<td><span data-ttu-id="07518-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="07518-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="07518-634">241.05</span><span class="sxs-lookup"><span data-stu-id="07518-634">241.05</span></span></td>
<td><span data-ttu-id="07518-635">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-636">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-636">Prod 2</span></span></td>
<td><span data-ttu-id="07518-637">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-637">Product 2</span></span></td>
<td><span data-ttu-id="07518-638">15</span><span class="sxs-lookup"><span data-stu-id="07518-638">15</span></span></td>
<td><span data-ttu-id="07518-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="07518-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="07518-640">45.20</span><span class="sxs-lookup"><span data-stu-id="07518-640">45.20</span></span></td>
<td><span data-ttu-id="07518-641">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-642">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-642">Prod 1</span></span></td>
<td><span data-ttu-id="07518-643">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-643">Product 1</span></span></td>
<td><span data-ttu-id="07518-644">80</span><span class="sxs-lookup"><span data-stu-id="07518-644">80</span></span></td>
<td><span data-ttu-id="07518-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="07518-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="07518-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="07518-646">2,507.09</span></span></td>
<td><span data-ttu-id="07518-647">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-648">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-648">Prod 2</span></span></td>
<td><span data-ttu-id="07518-649">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-649">Product 2</span></span></td>
<td><span data-ttu-id="07518-650">15</span><span class="sxs-lookup"><span data-stu-id="07518-650">15</span></span></td>
<td><span data-ttu-id="07518-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="07518-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="07518-652">470.08</span><span class="sxs-lookup"><span data-stu-id="07518-652">470.08</span></span></td>
<td><span data-ttu-id="07518-653">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="07518-654">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="07518-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07518-655">Færslubók</span><span class="sxs-lookup"><span data-stu-id="07518-655">Journal</span></span></th>
<th><span data-ttu-id="07518-656">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="07518-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="07518-657">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="07518-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="07518-658">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="07518-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-659">00004</span><span class="sxs-lookup"><span data-stu-id="07518-659">00004</span></span></td>
<td><span data-ttu-id="07518-660">Færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="07518-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="07518-661">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="07518-661">Fiscal</span></span></td>
<td><span data-ttu-id="07518-662">2017</span><span class="sxs-lookup"><span data-stu-id="07518-662">2017</span></span></td>
<td><span data-ttu-id="07518-663">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="07518-663">Period 1</span></span></td>
<td><span data-ttu-id="07518-664">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="07518-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="07518-665">Færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="07518-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="07518-666">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="07518-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="07518-667">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="07518-668">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="07518-668">Cost element</span></span></th>
<th><span data-ttu-id="07518-669">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="07518-669">Cost behavior</span></span></th>
<th><span data-ttu-id="07518-670">Upphæð</span><span class="sxs-lookup"><span data-stu-id="07518-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-671">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="07518-672">CC001</span><span class="sxs-lookup"><span data-stu-id="07518-672">CC001</span></span></td>
<td><span data-ttu-id="07518-673">Mannauður</span><span class="sxs-lookup"><span data-stu-id="07518-673">HR</span></span></td>
<td><span data-ttu-id="07518-674">10001</span><span class="sxs-lookup"><span data-stu-id="07518-674">10001</span></span></td>
<td><span data-ttu-id="07518-675">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-675">Electricity</span></span></td>
<td><span data-ttu-id="07518-676">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-676">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-677">500,00</span><span class="sxs-lookup"><span data-stu-id="07518-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-678">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="07518-679">CC001</span><span class="sxs-lookup"><span data-stu-id="07518-679">CC001</span></span></td>
<td><span data-ttu-id="07518-680">Mannauður</span><span class="sxs-lookup"><span data-stu-id="07518-680">HR</span></span></td>
<td><span data-ttu-id="07518-681">10001</span><span class="sxs-lookup"><span data-stu-id="07518-681">10001</span></span></td>
<td><span data-ttu-id="07518-682">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-682">Electricity</span></span></td>
<td><span data-ttu-id="07518-683">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-683">Variable cost</span></span></td>
<td><span data-ttu-id="07518-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="07518-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-685">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="07518-686">CC002</span><span class="sxs-lookup"><span data-stu-id="07518-686">CC002</span></span></td>
<td><span data-ttu-id="07518-687">Fjármál</span><span class="sxs-lookup"><span data-stu-id="07518-687">Finance</span></span></td>
<td><span data-ttu-id="07518-688">10001</span><span class="sxs-lookup"><span data-stu-id="07518-688">10001</span></span></td>
<td><span data-ttu-id="07518-689">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-689">Electricity</span></span></td>
<td><span data-ttu-id="07518-690">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-690">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-691">675.00</span><span class="sxs-lookup"><span data-stu-id="07518-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-692">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="07518-693">CC002</span><span class="sxs-lookup"><span data-stu-id="07518-693">CC002</span></span></td>
<td><span data-ttu-id="07518-694">Fjármál</span><span class="sxs-lookup"><span data-stu-id="07518-694">Finance</span></span></td>
<td><span data-ttu-id="07518-695">10001</span><span class="sxs-lookup"><span data-stu-id="07518-695">10001</span></span></td>
<td><span data-ttu-id="07518-696">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-696">Electricity</span></span></td>
<td><span data-ttu-id="07518-697">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-697">Variable cost</span></span></td>
<td><span data-ttu-id="07518-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="07518-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-699">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="07518-700">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-700">CC003</span></span></td>
<td><span data-ttu-id="07518-701">Smölun</span><span class="sxs-lookup"><span data-stu-id="07518-701">Assembly</span></span></td>
<td><span data-ttu-id="07518-702">10001</span><span class="sxs-lookup"><span data-stu-id="07518-702">10001</span></span></td>
<td><span data-ttu-id="07518-703">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-703">Electricity</span></span></td>
<td><span data-ttu-id="07518-704">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-704">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-705">713.75</span><span class="sxs-lookup"><span data-stu-id="07518-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-706">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="07518-707">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-707">CC003</span></span></td>
<td><span data-ttu-id="07518-708">Smölun</span><span class="sxs-lookup"><span data-stu-id="07518-708">Assembly</span></span></td>
<td><span data-ttu-id="07518-709">10001</span><span class="sxs-lookup"><span data-stu-id="07518-709">10001</span></span></td>
<td><span data-ttu-id="07518-710">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-710">Electricity</span></span></td>
<td><span data-ttu-id="07518-711">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-711">Variable cost</span></span></td>
<td><span data-ttu-id="07518-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="07518-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-713">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="07518-714">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-714">CC003</span></span></td>
<td><span data-ttu-id="07518-715">Pakkning</span><span class="sxs-lookup"><span data-stu-id="07518-715">Packaging</span></span></td>
<td><span data-ttu-id="07518-716">10001</span><span class="sxs-lookup"><span data-stu-id="07518-716">10001</span></span></td>
<td><span data-ttu-id="07518-717">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-717">Electricity</span></span></td>
<td><span data-ttu-id="07518-718">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-718">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-719">286.25</span><span class="sxs-lookup"><span data-stu-id="07518-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-720">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="07518-721">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-721">CC003</span></span></td>
<td><span data-ttu-id="07518-722">Pakkning</span><span class="sxs-lookup"><span data-stu-id="07518-722">Packaging</span></span></td>
<td><span data-ttu-id="07518-723">10001</span><span class="sxs-lookup"><span data-stu-id="07518-723">10001</span></span></td>
<td><span data-ttu-id="07518-724">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-724">Electricity</span></span></td>
<td><span data-ttu-id="07518-725">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-725">Variable cost</span></span></td>
<td><span data-ttu-id="07518-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="07518-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-727">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="07518-728">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-728">Prod 1</span></span></td>
<td><span data-ttu-id="07518-729">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-729">Product 1</span></span></td>
<td><span data-ttu-id="07518-730">10001</span><span class="sxs-lookup"><span data-stu-id="07518-730">10001</span></span></td>
<td><span data-ttu-id="07518-731">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-731">Electricity</span></span></td>
<td><span data-ttu-id="07518-732">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-732">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-733">776.36</span><span class="sxs-lookup"><span data-stu-id="07518-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-734">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="07518-735">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-735">Prod 1</span></span></td>
<td><span data-ttu-id="07518-736">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-736">Product 1</span></span></td>
<td><span data-ttu-id="07518-737">10001</span><span class="sxs-lookup"><span data-stu-id="07518-737">10001</span></span></td>
<td><span data-ttu-id="07518-738">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-738">Electricity</span></span></td>
<td><span data-ttu-id="07518-739">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-739">Variable cost</span></span></td>
<td><span data-ttu-id="07518-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="07518-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-741">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="07518-742">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-742">Prod 2</span></span></td>
<td><span data-ttu-id="07518-743">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-743">Product 1</span></span></td>
<td><span data-ttu-id="07518-744">10001</span><span class="sxs-lookup"><span data-stu-id="07518-744">10001</span></span></td>
<td><span data-ttu-id="07518-745">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-745">Electricity</span></span></td>
<td><span data-ttu-id="07518-746">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-746">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-747">223.64</span><span class="sxs-lookup"><span data-stu-id="07518-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-748">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="07518-749">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-749">Prod 2</span></span></td>
<td><span data-ttu-id="07518-750">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-750">Product 1</span></span></td>
<td><span data-ttu-id="07518-751">10001</span><span class="sxs-lookup"><span data-stu-id="07518-751">10001</span></span></td>
<td><span data-ttu-id="07518-752">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-752">Electricity</span></span></td>
<td><span data-ttu-id="07518-753">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-753">Variable cost</span></span></td>
<td><span data-ttu-id="07518-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="07518-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="07518-755">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="07518-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="07518-756">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="07518-757">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="07518-757">Cost element</span></span></th>
<th><span data-ttu-id="07518-758">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="07518-758">Cost behavior</span></span></th>
<th><span data-ttu-id="07518-759">Upphæð</span><span class="sxs-lookup"><span data-stu-id="07518-759">Amount</span></span></th>
<th><span data-ttu-id="07518-760">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="07518-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="07518-761">CC001</span><span class="sxs-lookup"><span data-stu-id="07518-761">CC001</span></span></td>
<td><span data-ttu-id="07518-762">Mannauður</span><span class="sxs-lookup"><span data-stu-id="07518-762">HR</span></span></td>
<td><span data-ttu-id="07518-763">10001</span><span class="sxs-lookup"><span data-stu-id="07518-763">10001</span></span></td>
<td><span data-ttu-id="07518-764">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-764">Electricity</span></span></td>
<td><span data-ttu-id="07518-765">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-765">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="07518-766">-500.00</span></span></td>
<td><span data-ttu-id="07518-767">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-768">CC002</span><span class="sxs-lookup"><span data-stu-id="07518-768">CC002</span></span></td>
<td><span data-ttu-id="07518-769">Fjármál</span><span class="sxs-lookup"><span data-stu-id="07518-769">Finance</span></span></td>
<td><span data-ttu-id="07518-770">10001</span><span class="sxs-lookup"><span data-stu-id="07518-770">10001</span></span></td>
<td><span data-ttu-id="07518-771">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-771">Electricity</span></span></td>
<td><span data-ttu-id="07518-772">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-772">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-773">175.00</span><span class="sxs-lookup"><span data-stu-id="07518-773">175.00</span></span></td>
<td><span data-ttu-id="07518-774">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-775">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-775">CC003</span></span></td>
<td><span data-ttu-id="07518-776">Smölun</span><span class="sxs-lookup"><span data-stu-id="07518-776">Assembly</span></span></td>
<td><span data-ttu-id="07518-777">10001</span><span class="sxs-lookup"><span data-stu-id="07518-777">10001</span></span></td>
<td><span data-ttu-id="07518-778">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-778">Electricity</span></span></td>
<td><span data-ttu-id="07518-779">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-779">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-780">275.00</span><span class="sxs-lookup"><span data-stu-id="07518-780">275.00</span></span></td>
<td><span data-ttu-id="07518-781">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-782">CC004</span><span class="sxs-lookup"><span data-stu-id="07518-782">CC004</span></span></td>
<td><span data-ttu-id="07518-783">Pakkning</span><span class="sxs-lookup"><span data-stu-id="07518-783">Packaging</span></span></td>
<td><span data-ttu-id="07518-784">10001</span><span class="sxs-lookup"><span data-stu-id="07518-784">10001</span></span></td>
<td><span data-ttu-id="07518-785">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-785">Electricity</span></span></td>
<td><span data-ttu-id="07518-786">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-786">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-787">50,00</span><span class="sxs-lookup"><span data-stu-id="07518-787">50,00</span></span></td>
<td><span data-ttu-id="07518-788">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-789">CC001</span><span class="sxs-lookup"><span data-stu-id="07518-789">CC001</span></span></td>
<td><span data-ttu-id="07518-790">Mannauður</span><span class="sxs-lookup"><span data-stu-id="07518-790">HR</span></span></td>
<td><span data-ttu-id="07518-791">10001</span><span class="sxs-lookup"><span data-stu-id="07518-791">10001</span></span></td>
<td><span data-ttu-id="07518-792">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-792">Electricity</span></span></td>
<td><span data-ttu-id="07518-793">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-793">Variable cost</span></span></td>
<td><span data-ttu-id="07518-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="07518-794">-1,245.71</span></span></td>
<td><span data-ttu-id="07518-795">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-796">CC002</span><span class="sxs-lookup"><span data-stu-id="07518-796">CC002</span></span></td>
<td><span data-ttu-id="07518-797">Fjármál</span><span class="sxs-lookup"><span data-stu-id="07518-797">Finance</span></span></td>
<td><span data-ttu-id="07518-798">10001</span><span class="sxs-lookup"><span data-stu-id="07518-798">10001</span></span></td>
<td><span data-ttu-id="07518-799">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-799">Electricity</span></span></td>
<td><span data-ttu-id="07518-800">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-800">Variable cost</span></span></td>
<td><span data-ttu-id="07518-801">436.00</span><span class="sxs-lookup"><span data-stu-id="07518-801">436.00</span></span></td>
<td><span data-ttu-id="07518-802">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-803">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-803">CC003</span></span></td>
<td><span data-ttu-id="07518-804">Smölun</span><span class="sxs-lookup"><span data-stu-id="07518-804">Assembly</span></span></td>
<td><span data-ttu-id="07518-805">10001</span><span class="sxs-lookup"><span data-stu-id="07518-805">10001</span></span></td>
<td><span data-ttu-id="07518-806">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-806">Electricity</span></span></td>
<td><span data-ttu-id="07518-807">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-807">Variable cost</span></span></td>
<td><span data-ttu-id="07518-808">685.14</span><span class="sxs-lookup"><span data-stu-id="07518-808">685.14</span></span></td>
<td><span data-ttu-id="07518-809">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-810">CC004</span><span class="sxs-lookup"><span data-stu-id="07518-810">CC004</span></span></td>
<td><span data-ttu-id="07518-811">Pakkning</span><span class="sxs-lookup"><span data-stu-id="07518-811">Packaging</span></span></td>
<td><span data-ttu-id="07518-812">10001</span><span class="sxs-lookup"><span data-stu-id="07518-812">10001</span></span></td>
<td><span data-ttu-id="07518-813">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-813">Electricity</span></span></td>
<td><span data-ttu-id="07518-814">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-814">Variable cost</span></span></td>
<td><span data-ttu-id="07518-815">124.57</span><span class="sxs-lookup"><span data-stu-id="07518-815">124.57</span></span></td>
<td><span data-ttu-id="07518-816">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-817">CC002</span><span class="sxs-lookup"><span data-stu-id="07518-817">CC002</span></span></td>
<td><span data-ttu-id="07518-818">Fjármál</span><span class="sxs-lookup"><span data-stu-id="07518-818">Finance</span></span></td>
<td><span data-ttu-id="07518-819">10001</span><span class="sxs-lookup"><span data-stu-id="07518-819">10001</span></span></td>
<td><span data-ttu-id="07518-820">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-820">Electricity</span></span></td>
<td><span data-ttu-id="07518-821">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-821">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="07518-822">-675.00</span></span></td>
<td><span data-ttu-id="07518-823">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-824">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-824">CC003</span></span></td>
<td><span data-ttu-id="07518-825">Smölun</span><span class="sxs-lookup"><span data-stu-id="07518-825">Assembly</span></span></td>
<td><span data-ttu-id="07518-826">10001</span><span class="sxs-lookup"><span data-stu-id="07518-826">10001</span></span></td>
<td><span data-ttu-id="07518-827">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-827">Electricity</span></span></td>
<td><span data-ttu-id="07518-828">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-828">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-829">438.75</span><span class="sxs-lookup"><span data-stu-id="07518-829">438.75</span></span></td>
<td><span data-ttu-id="07518-830">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-831">CC004</span><span class="sxs-lookup"><span data-stu-id="07518-831">CC004</span></span></td>
<td><span data-ttu-id="07518-832">Pakkning</span><span class="sxs-lookup"><span data-stu-id="07518-832">Packaging</span></span></td>
<td><span data-ttu-id="07518-833">10001</span><span class="sxs-lookup"><span data-stu-id="07518-833">10001</span></span></td>
<td><span data-ttu-id="07518-834">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-834">Electricity</span></span></td>
<td><span data-ttu-id="07518-835">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-835">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-836">236.25</span><span class="sxs-lookup"><span data-stu-id="07518-836">236.25</span></span></td>
<td><span data-ttu-id="07518-837">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-838">CC002</span><span class="sxs-lookup"><span data-stu-id="07518-838">CC002</span></span></td>
<td><span data-ttu-id="07518-839">Fjármál</span><span class="sxs-lookup"><span data-stu-id="07518-839">Finance</span></span></td>
<td><span data-ttu-id="07518-840">10001</span><span class="sxs-lookup"><span data-stu-id="07518-840">10001</span></span></td>
<td><span data-ttu-id="07518-841">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-841">Electricity</span></span></td>
<td><span data-ttu-id="07518-842">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-842">Variable cost</span></span></td>
<td><span data-ttu-id="07518-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="07518-843">-8,150.29</span></span></td>
<td><span data-ttu-id="07518-844">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-845">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-845">CC003</span></span></td>
<td><span data-ttu-id="07518-846">Smölun</span><span class="sxs-lookup"><span data-stu-id="07518-846">Assembly</span></span></td>
<td><span data-ttu-id="07518-847">10001</span><span class="sxs-lookup"><span data-stu-id="07518-847">10001</span></span></td>
<td><span data-ttu-id="07518-848">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-848">Electricity</span></span></td>
<td><span data-ttu-id="07518-849">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-849">Variable cost</span></span></td>
<td><span data-ttu-id="07518-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="07518-850">5,297.69</span></span></td>
<td><span data-ttu-id="07518-851">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-852">CC004</span><span class="sxs-lookup"><span data-stu-id="07518-852">CC004</span></span></td>
<td><span data-ttu-id="07518-853">Pakkning</span><span class="sxs-lookup"><span data-stu-id="07518-853">Packaging</span></span></td>
<td><span data-ttu-id="07518-854">10001</span><span class="sxs-lookup"><span data-stu-id="07518-854">10001</span></span></td>
<td><span data-ttu-id="07518-855">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-855">Electricity</span></span></td>
<td><span data-ttu-id="07518-856">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-856">Variable cost</span></span></td>
<td><span data-ttu-id="07518-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="07518-857">2,852.60</span></span></td>
<td><span data-ttu-id="07518-858">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-859">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-859">CC003</span></span></td>
<td><span data-ttu-id="07518-860">Smölun</span><span class="sxs-lookup"><span data-stu-id="07518-860">Assembly</span></span></td>
<td><span data-ttu-id="07518-861">10001</span><span class="sxs-lookup"><span data-stu-id="07518-861">10001</span></span></td>
<td><span data-ttu-id="07518-862">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-862">Electricity</span></span></td>
<td><span data-ttu-id="07518-863">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-863">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="07518-864">-713.75</span></span></td>
<td><span data-ttu-id="07518-865">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-866">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-866">Prod 1</span></span></td>
<td><span data-ttu-id="07518-867">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-867">Product 1</span></span></td>
<td><span data-ttu-id="07518-868">10001</span><span class="sxs-lookup"><span data-stu-id="07518-868">10001</span></span></td>
<td><span data-ttu-id="07518-869">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-869">Electricity</span></span></td>
<td><span data-ttu-id="07518-870">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-870">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-871">535.31</span><span class="sxs-lookup"><span data-stu-id="07518-871">535.31</span></span></td>
<td><span data-ttu-id="07518-872">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-873">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-873">Prod 2</span></span></td>
<td><span data-ttu-id="07518-874">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-874">Product 2</span></span></td>
<td><span data-ttu-id="07518-875">10001</span><span class="sxs-lookup"><span data-stu-id="07518-875">10001</span></span></td>
<td><span data-ttu-id="07518-876">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-876">Electricity</span></span></td>
<td><span data-ttu-id="07518-877">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-877">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-878">178.44</span><span class="sxs-lookup"><span data-stu-id="07518-878">178.44</span></span></td>
<td><span data-ttu-id="07518-879">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-880">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-880">CC003</span></span></td>
<td><span data-ttu-id="07518-881">Smölun</span><span class="sxs-lookup"><span data-stu-id="07518-881">Assembly</span></span></td>
<td><span data-ttu-id="07518-882">10001</span><span class="sxs-lookup"><span data-stu-id="07518-882">10001</span></span></td>
<td><span data-ttu-id="07518-883">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-883">Electricity</span></span></td>
<td><span data-ttu-id="07518-884">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-884">Variable cost</span></span></td>
<td><span data-ttu-id="07518-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="07518-885">-5,982.83</span></span></td>
<td><span data-ttu-id="07518-886">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-887">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-887">Prod 1</span></span></td>
<td><span data-ttu-id="07518-888">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-888">Product 1</span></span></td>
<td><span data-ttu-id="07518-889">10001</span><span class="sxs-lookup"><span data-stu-id="07518-889">10001</span></span></td>
<td><span data-ttu-id="07518-890">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-890">Electricity</span></span></td>
<td><span data-ttu-id="07518-891">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-891">Variable cost</span></span></td>
<td><span data-ttu-id="07518-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="07518-892">4,487.12</span></span></td>
<td><span data-ttu-id="07518-893">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-894">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-894">Prod 2</span></span></td>
<td><span data-ttu-id="07518-895">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-895">Product 2</span></span></td>
<td><span data-ttu-id="07518-896">10001</span><span class="sxs-lookup"><span data-stu-id="07518-896">10001</span></span></td>
<td><span data-ttu-id="07518-897">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-897">Electricity</span></span></td>
<td><span data-ttu-id="07518-898">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-898">Variable cost</span></span></td>
<td><span data-ttu-id="07518-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="07518-899">1,495.71</span></span></td>
<td><span data-ttu-id="07518-900">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-901">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-901">CC003</span></span></td>
<td><span data-ttu-id="07518-902">Smölun</span><span class="sxs-lookup"><span data-stu-id="07518-902">Assembly</span></span></td>
<td><span data-ttu-id="07518-903">10001</span><span class="sxs-lookup"><span data-stu-id="07518-903">10001</span></span></td>
<td><span data-ttu-id="07518-904">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-904">Electricity</span></span></td>
<td><span data-ttu-id="07518-905">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-905">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="07518-906">-286.25</span></span></td>
<td><span data-ttu-id="07518-907">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-908">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-908">Prod 1</span></span></td>
<td><span data-ttu-id="07518-909">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-909">Product 1</span></span></td>
<td><span data-ttu-id="07518-910">10001</span><span class="sxs-lookup"><span data-stu-id="07518-910">10001</span></span></td>
<td><span data-ttu-id="07518-911">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-911">Electricity</span></span></td>
<td><span data-ttu-id="07518-912">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-912">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-913">241.05</span><span class="sxs-lookup"><span data-stu-id="07518-913">241.05</span></span></td>
<td><span data-ttu-id="07518-914">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-915">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-915">Prod 2</span></span></td>
<td><span data-ttu-id="07518-916">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-916">Product 2</span></span></td>
<td><span data-ttu-id="07518-917">10001</span><span class="sxs-lookup"><span data-stu-id="07518-917">10001</span></span></td>
<td><span data-ttu-id="07518-918">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-918">Electricity</span></span></td>
<td><span data-ttu-id="07518-919">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-919">Fixed cost</span></span></td>
<td><span data-ttu-id="07518-920">45.20</span><span class="sxs-lookup"><span data-stu-id="07518-920">45.20</span></span></td>
<td><span data-ttu-id="07518-921">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-922">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-922">CC003</span></span></td>
<td><span data-ttu-id="07518-923">Smölun</span><span class="sxs-lookup"><span data-stu-id="07518-923">Assembly</span></span></td>
<td><span data-ttu-id="07518-924">10001</span><span class="sxs-lookup"><span data-stu-id="07518-924">10001</span></span></td>
<td><span data-ttu-id="07518-925">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-925">Electricity</span></span></td>
<td><span data-ttu-id="07518-926">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-926">Variable cost</span></span></td>
<td><span data-ttu-id="07518-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="07518-927">-2,977.17</span></span></td>
<td><span data-ttu-id="07518-928">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-929">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-929">Prod 1</span></span></td>
<td><span data-ttu-id="07518-930">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-930">Product 1</span></span></td>
<td><span data-ttu-id="07518-931">10001</span><span class="sxs-lookup"><span data-stu-id="07518-931">10001</span></span></td>
<td><span data-ttu-id="07518-932">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-932">Electricity</span></span></td>
<td><span data-ttu-id="07518-933">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-933">Variable cost</span></span></td>
<td><span data-ttu-id="07518-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="07518-934">2,507.09</span></span></td>
<td><span data-ttu-id="07518-935">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="07518-936">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-936">Prod 2</span></span></td>
<td><span data-ttu-id="07518-937">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-937">Product 2</span></span></td>
<td><span data-ttu-id="07518-938">10001</span><span class="sxs-lookup"><span data-stu-id="07518-938">10001</span></span></td>
<td><span data-ttu-id="07518-939">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-939">Electricity</span></span></td>
<td><span data-ttu-id="07518-940">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-940">Variable cost</span></span></td>
<td><span data-ttu-id="07518-941">470.08</span><span class="sxs-lookup"><span data-stu-id="07518-941">470.08</span></span></td>
<td><span data-ttu-id="07518-942">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="07518-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="07518-943">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="07518-943">Conclusion</span></span>
<span data-ttu-id="07518-944">Í Fjárhagsbókhaldi er kostnaður upp á 10.000,00 fyrir rafmagn bókaður á kenni leppkostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="07518-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="07518-945">Þar af leiðandi munu kostnaðarbókarar vita að það þarf að úthluta þessum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="07518-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="07518-946">Í kostnaðarbókhaldi streymir kostnaður þvert á fyrirtækiseiningar og stig, samkvæmt þeim stefnum og reglum sem eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="07518-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="07518-947">Hver kostnaður hefur verið tengdur úthlutunargrunni sem veitir besta mat á úthlutun á kostnaði.</span><span class="sxs-lookup"><span data-stu-id="07518-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="07518-948">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="07518-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="07518-949">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="07518-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="07518-950">Samtala</span><span class="sxs-lookup"><span data-stu-id="07518-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="07518-951">CC099</span><span class="sxs-lookup"><span data-stu-id="07518-951">CC099</span></span></th>
<th><span data-ttu-id="07518-952">CC001</span><span class="sxs-lookup"><span data-stu-id="07518-952">CC001</span></span></th>
<th><span data-ttu-id="07518-953">CC002</span><span class="sxs-lookup"><span data-stu-id="07518-953">CC002</span></span></th>
<th><span data-ttu-id="07518-954">CC003</span><span class="sxs-lookup"><span data-stu-id="07518-954">CC003</span></span></th>
<th><span data-ttu-id="07518-955">CC004</span><span class="sxs-lookup"><span data-stu-id="07518-955">CC004</span></span></th>
<th><span data-ttu-id="07518-956">Verk 1</span><span class="sxs-lookup"><span data-stu-id="07518-956">Proj 1</span></span></th>
<th><span data-ttu-id="07518-957">Verk 2</span><span class="sxs-lookup"><span data-stu-id="07518-957">Proj 2</span></span></th>
<th><span data-ttu-id="07518-958">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="07518-958">Prod 1</span></span></th>
<th><span data-ttu-id="07518-959">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="07518-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="07518-960">10001 Rafmagn</span><span class="sxs-lookup"><span data-stu-id="07518-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="07518-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="07518-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="07518-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="07518-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="07518-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="07518-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="07518-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="07518-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="07518-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="07518-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="07518-970">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="07518-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-971">0,00</span><span class="sxs-lookup"><span data-stu-id="07518-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="07518-972">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-973">0,00</span><span class="sxs-lookup"><span data-stu-id="07518-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-974">0,00</span><span class="sxs-lookup"><span data-stu-id="07518-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-975">0,00</span><span class="sxs-lookup"><span data-stu-id="07518-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-976">0,00</span><span class="sxs-lookup"><span data-stu-id="07518-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-977">0,00</span><span class="sxs-lookup"><span data-stu-id="07518-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="07518-978">776.36</span><span class="sxs-lookup"><span data-stu-id="07518-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-979">223.64</span><span class="sxs-lookup"><span data-stu-id="07518-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="07518-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="07518-981">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="07518-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-982">000</span><span class="sxs-lookup"><span data-stu-id="07518-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-983">0,00</span><span class="sxs-lookup"><span data-stu-id="07518-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-984">0,00</span><span class="sxs-lookup"><span data-stu-id="07518-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-985">0,00</span><span class="sxs-lookup"><span data-stu-id="07518-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-986">0,00</span><span class="sxs-lookup"><span data-stu-id="07518-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-987">30,00</span><span class="sxs-lookup"><span data-stu-id="07518-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-988">10,00</span><span class="sxs-lookup"><span data-stu-id="07518-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="07518-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="07518-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="07518-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="07518-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="07518-992">Þetta efnisatriði sýnir hvernig fyrir aðalkostnaðareiningin 10001 Rafmagn flæðir í gegnum kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="07518-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="07518-993">Þar af leiðandi er þessum sameiginlega kostnaði úthlutað á lægsta stigið í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="07518-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="07518-994">Með öðrum orðum bera kostnaðarhlutir á lægsta stiginu kostnaðinn.</span><span class="sxs-lookup"><span data-stu-id="07518-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="07518-995">Ef þú þarft sjónrænt flæði kostnaðar á milli kostnaðarhluta er hægt að nota stefnureglur samantekins kostnaðar til að gera kostnaðarflæðið sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="07518-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="07518-996">Fyrir frekari upplýsingar skal sjá [Stefna fyrir samantekt kostnaðar og útreikning sameiginlegs kostnaðar](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="07518-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



