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
ms.openlocfilehash: 8dc312e66dc666ac6c23bac6b705ffc7893fd06b
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187998"
---
# <a name="overhead-calculation"></a><span data-ttu-id="f9181-103">Útreikningur fastakostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9181-104">Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði.</span><span class="sxs-lookup"><span data-stu-id="f9181-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

## <a name="term-definition"></a><span data-ttu-id="f9181-105">Skýrsluskilgreining</span><span class="sxs-lookup"><span data-stu-id="f9181-105">Term definition</span></span>

<span data-ttu-id="f9181-106">Stjórnunarkostnaður er sá kostnaður sem stofnað er til fyrir rekstur fyrirtækis, en sem ekki er hægt að rekja beint til neinna sérstakrar starfsemi, vöru eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="f9181-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="f9181-107">Stjórnunarkostnaður veitir mikilvægan stuðning við myndun hagnaðarmyndandi verkþátta.</span><span class="sxs-lookup"><span data-stu-id="f9181-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="f9181-108">Hér eru nokkur dæmi um skilyrði:</span><span class="sxs-lookup"><span data-stu-id="f9181-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="f9181-109">Leiga</span><span class="sxs-lookup"><span data-stu-id="f9181-109">Rent</span></span>
-   <span data-ttu-id="f9181-110">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-110">Electricity</span></span>
-   <span data-ttu-id="f9181-111">Stjórnunarkostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="f9181-112">Yfirlit yfir útreikning fastakostnaðar</span><span class="sxs-lookup"><span data-stu-id="f9181-112">Overhead calculation overview</span></span>
<span data-ttu-id="f9181-113">Útreikningur fastakostnaðar keyrir reglur kostnaðarbókhalds í réttri röð.</span><span class="sxs-lookup"><span data-stu-id="f9181-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="f9181-114">Hægt er að keyra útreikning fastakostnaðar margsinnis fyrir sama fjárhagstímabil ef reglum kostnaðarbókhalds hefur verið breytt eða ákveðnar villur hafa fundist.</span><span class="sxs-lookup"><span data-stu-id="f9181-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="f9181-115">Hver keyrsla á útreikningi fastakostnaðar er geymd og fær einkvæmt útgáfukenni sem gerir kleift að bera saman útreikning í mismunandi útgáfum.</span><span class="sxs-lookup"><span data-stu-id="f9181-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="f9181-116">Kostnaðarfærslur sem útreikningur fastakostnaðar mynda fá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="f9181-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="f9181-117">Dagsetningin bókhald samsvarar lokadagsetning fjárhagstímabilsins sem er dagsetning reikningsskiladagsetning reikningsskila notað í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="f9181-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="f9181-118">Einkvæmt útgáfukenni samanstendur af eftirfarandi þáttum:</span><span class="sxs-lookup"><span data-stu-id="f9181-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="f9181-119">Gerð útgáfu</span><span class="sxs-lookup"><span data-stu-id="f9181-119">Version type</span></span>
-   <span data-ttu-id="f9181-120">Dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="f9181-120">Date and time</span></span>
-   <span data-ttu-id="f9181-121">Fjárhagur kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="f9181-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="f9181-122">Fjárhagsár</span><span class="sxs-lookup"><span data-stu-id="f9181-122">Fiscal year</span></span>
-   <span data-ttu-id="f9181-123">Reikningstímabil</span><span class="sxs-lookup"><span data-stu-id="f9181-123">Fiscal period</span></span>

<span data-ttu-id="f9181-124">Útreikningur fastakostnaðar er keyrður óháð því hver útgáfan er.</span><span class="sxs-lookup"><span data-stu-id="f9181-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="f9181-125">Þess vegna er hægt að reikna út áætlaða útgáfu á undan raunútgáfu.</span><span class="sxs-lookup"><span data-stu-id="f9181-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="f9181-126">Útreikningur fastakostnaðar samanstendur af fjórum skrefum, eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="f9181-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="f9181-127">Í hverju skrefi er færslubókarhaus stofnaður með bókarfærslum.</span><span class="sxs-lookup"><span data-stu-id="f9181-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="f9181-128">Þessi færslubókarhaus geymir inntaksgögn fyrir hvert útreikningsþrep.</span><span class="sxs-lookup"><span data-stu-id="f9181-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="f9181-129">Stefnur og reglur eru notaðar í hverri færslulínu og kostnaðarfærslur eru myndaðar sem úttak.</span><span class="sxs-lookup"><span data-stu-id="f9181-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="f9181-130">Þess vegna hefurðu ávallt fullan rekjanleika.</span><span class="sxs-lookup"><span data-stu-id="f9181-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="f9181-131">[![Útreikningur fastakostnaðar](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="f9181-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="f9181-132">Reikna og úthluta sameiginlegur kostnaði vegna rafmagns</span><span class="sxs-lookup"><span data-stu-id="f9181-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="f9181-133">Í Fjárhagsbókhaldi er ákveðinn kostnaður, eins og rafmagn, skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="f9181-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="f9181-134">Þar af leiðandi er nákvæmar innsýn rekstrarfélags ekki veitt fyrir kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="f9181-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="f9181-135">Í kostnaðarbókhaldi verður kostnaður að flæða í gegnum fyrirtækiseiningar til að veita rétta innsýn rekstrarfélags þvert á allar fyrirtækiseiningar og stig.</span><span class="sxs-lookup"><span data-stu-id="f9181-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="f9181-136">Þetta flæði verður að byggja á annaðhvort nákvæmri færslu notkunar eða sanngjarnri matsreglu.</span><span class="sxs-lookup"><span data-stu-id="f9181-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="f9181-137">Í fjárhagnum er hægt að bóka rafmagnskostnað eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="f9181-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f9181-138">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="f9181-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f9181-139">Kostnaðarstaður</span><span class="sxs-lookup"><span data-stu-id="f9181-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="f9181-140">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="f9181-140">Main account</span></span></th>
<th><span data-ttu-id="f9181-141">Upphæð í bókhaldsgjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="f9181-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-142">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="f9181-143">CC099</span><span class="sxs-lookup"><span data-stu-id="f9181-143">CC099</span></span></td>
<td><span data-ttu-id="f9181-144">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="f9181-144">Default cost center</span></span></td>
<td><span data-ttu-id="f9181-145">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-145">10001</span></span></td>
<td><span data-ttu-id="f9181-146">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-146">Electricity</span></span></td>
<td><span data-ttu-id="f9181-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="f9181-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="f9181-148">Skref 1: Keyra útreikning kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="f9181-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="f9181-149">Sjálfvirkt er að þegar kostnaðarfærslur eru fluttar úr grunngögnum fái þær flokkun kostnaðarhegðunar **Óflokkað** í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="f9181-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="f9181-150">Með því að nota stefnureglur kostnaðarhegðunar er hægt að endurflokka kostnaðarfærslur sem annaðhvort **Fastan kostnað** eða **Breytilegan kostnað**.</span><span class="sxs-lookup"><span data-stu-id="f9181-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="f9181-151">Tilgreinið reglu kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="f9181-151">Define the cost behavior rule</span></span>

<span data-ttu-id="f9181-152">Í sumum tilfellum er hluti af kostnaði föst þóknun og eftirstandandi kostnaður byggist á notkun.</span><span class="sxs-lookup"><span data-stu-id="f9181-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="f9181-153">Rafmagnsreikningar stemma oft við þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="f9181-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="f9181-154">Þegar tiltekin föst þóknun hefur verið greidd, er greitt fyrir notkun á kílóvattklukkustund (Kwh).</span><span class="sxs-lookup"><span data-stu-id="f9181-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="f9181-155">Til dæmis ef föst kostnaðarþóknun er 1000.00 sýnir þetta hvernig regla kostnaðarhegðunar er skilgreind:</span><span class="sxs-lookup"><span data-stu-id="f9181-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="f9181-156">Föst upphæð 1.000,00</span><span class="sxs-lookup"><span data-stu-id="f9181-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="f9181-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="f9181-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="f9181-158">1000.01 &lt; N = Breyta</span><span class="sxs-lookup"><span data-stu-id="f9181-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="f9181-159">Færslubók</span><span class="sxs-lookup"><span data-stu-id="f9181-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f9181-160">Færslubók</span><span class="sxs-lookup"><span data-stu-id="f9181-160">Journal</span></span></th>
<th><span data-ttu-id="f9181-161">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="f9181-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f9181-162">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="f9181-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f9181-163">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="f9181-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-164">00001</span><span class="sxs-lookup"><span data-stu-id="f9181-164">00001</span></span></td>
<td><span data-ttu-id="f9181-165">Færslubók útreiknings fyrir kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="f9181-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="f9181-166">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="f9181-166">Fiscal</span></span></td>
<td><span data-ttu-id="f9181-167">2017</span><span class="sxs-lookup"><span data-stu-id="f9181-167">2017</span></span></td>
<td><span data-ttu-id="f9181-168">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="f9181-168">Period 1</span></span></td>
<td><span data-ttu-id="f9181-169">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="f9181-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="f9181-170">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="f9181-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f9181-171">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="f9181-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f9181-172">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f9181-173">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="f9181-173">Cost element</span></span></th>
<th><span data-ttu-id="f9181-174">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="f9181-174">Cost behavior</span></span></th>
<th><span data-ttu-id="f9181-175">Upphæð</span><span class="sxs-lookup"><span data-stu-id="f9181-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-176">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="f9181-177">CC099</span><span class="sxs-lookup"><span data-stu-id="f9181-177">CC099</span></span></td>
<td><span data-ttu-id="f9181-178">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="f9181-178">Default cost center</span></span></td>
<td><span data-ttu-id="f9181-179">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-179">10001</span></span></td>
<td><span data-ttu-id="f9181-180">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-180">Electricity</span></span></td>
<td><span data-ttu-id="f9181-181">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="f9181-181">Unclassified</span></span></td>
<td><span data-ttu-id="f9181-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="f9181-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f9181-183">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="f9181-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f9181-184">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f9181-185">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="f9181-185">Cost element</span></span></th>
<th><span data-ttu-id="f9181-186">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="f9181-186">Cost behavior</span></span></th>
<th><span data-ttu-id="f9181-187">Upphæð</span><span class="sxs-lookup"><span data-stu-id="f9181-187">Amount</span></span></th>
<th><span data-ttu-id="f9181-188">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="f9181-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-189">CC099</span><span class="sxs-lookup"><span data-stu-id="f9181-189">CC099</span></span></td>
<td><span data-ttu-id="f9181-190">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="f9181-190">Default cost center</span></span></td>
<td><span data-ttu-id="f9181-191">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-191">10001</span></span></td>
<td><span data-ttu-id="f9181-192">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-192">Electricity</span></span></td>
<td><span data-ttu-id="f9181-193">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="f9181-193">Unclassified</span></span></td>
<td><span data-ttu-id="f9181-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="f9181-194">10,000.00</span></span></td>
<td><span data-ttu-id="f9181-195">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-196">CC099</span><span class="sxs-lookup"><span data-stu-id="f9181-196">CC099</span></span></td>
<td><span data-ttu-id="f9181-197">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="f9181-197">Default cost center</span></span></td>
<td><span data-ttu-id="f9181-198">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-198">10001</span></span></td>
<td><span data-ttu-id="f9181-199">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-199">Electricity</span></span></td>
<td><span data-ttu-id="f9181-200">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="f9181-200">Unclassified</span></span></td>
<td><span data-ttu-id="f9181-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="f9181-201">-10,000.00</span></span></td>
<td><span data-ttu-id="f9181-202">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-203">CC099</span><span class="sxs-lookup"><span data-stu-id="f9181-203">CC099</span></span></td>
<td><span data-ttu-id="f9181-204">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="f9181-204">Default cost center</span></span></td>
<td><span data-ttu-id="f9181-205">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-205">10001</span></span></td>
<td><span data-ttu-id="f9181-206">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-206">Electricity</span></span></td>
<td><span data-ttu-id="f9181-207">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-207">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="f9181-208">1,000.00</span></span></td>
<td><span data-ttu-id="f9181-209">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-210">CC099</span><span class="sxs-lookup"><span data-stu-id="f9181-210">CC099</span></span></td>
<td><span data-ttu-id="f9181-211">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="f9181-211">Default cost center</span></span></td>
<td><span data-ttu-id="f9181-212">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-212">10001</span></span></td>
<td><span data-ttu-id="f9181-213">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-213">Electricity</span></span></td>
<td><span data-ttu-id="f9181-214">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-214">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="f9181-215">9,000.00</span></span></td>
<td><span data-ttu-id="f9181-216">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f9181-217">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðarhegðunarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="f9181-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="f9181-218">Skref 2: Keyra útreikning kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="f9181-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="f9181-219">Kostnaðardreifing er notuð til að endurúthluta kostnaði frá einum kostnaðarhlut til annars eða fleiri kostnaðarhluta með því að nota viðeigandi úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="f9181-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="f9181-220">Kostnaðardreifing og kostnaðarúthlutun eru ólíkar að því leyti að kostnaðardreifing kemur alltaf upp á stigi aðalkostnaðareiningar upphaflegs verðs.</span><span class="sxs-lookup"><span data-stu-id="f9181-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="f9181-221">Tilgreinið kostnaðardreifingarreglu</span><span class="sxs-lookup"><span data-stu-id="f9181-221">Define the cost distribution rule</span></span>

<span data-ttu-id="f9181-222">Í Fjárhagsbókhaldi er rafmagnskostnaður oft skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="f9181-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="f9181-223">Í kostnaðarbókhaldi er þessi nálgun ekki nógu nákvæm.</span><span class="sxs-lookup"><span data-stu-id="f9181-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="f9181-224">Breytilegur kostnaði þarf að dreifa á staka kostnaðarhluti á sanngjörnum grunni.</span><span class="sxs-lookup"><span data-stu-id="f9181-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="f9181-225">Rökréttasti úthlutunargrunnurinn er notkun á rafmagni (Kwh).</span><span class="sxs-lookup"><span data-stu-id="f9181-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="f9181-226">Stofnað er tölfræðilegt víddarstak sem er nefnt Rafmagn og rafmagnsnotkun er skráð.</span><span class="sxs-lookup"><span data-stu-id="f9181-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="f9181-227">Sjálfgefið er að öll tölfræðileg víddarstök verða tiltæk sem úthlutunargrunnur.</span><span class="sxs-lookup"><span data-stu-id="f9181-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f9181-228">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-228">Cost object</span></span></th>
<th><span data-ttu-id="f9181-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="f9181-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-230">CC001</span><span class="sxs-lookup"><span data-stu-id="f9181-230">CC001</span></span></td>
<td><span data-ttu-id="f9181-231">Mannauður</span><span class="sxs-lookup"><span data-stu-id="f9181-231">HR</span></span></td>
<td><span data-ttu-id="f9181-232">1.000</span><span class="sxs-lookup"><span data-stu-id="f9181-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-233">CC002</span><span class="sxs-lookup"><span data-stu-id="f9181-233">CC002</span></span></td>
<td><span data-ttu-id="f9181-234">Fjármál</span><span class="sxs-lookup"><span data-stu-id="f9181-234">Finance</span></span></td>
<td><span data-ttu-id="f9181-235">6,000</span><span class="sxs-lookup"><span data-stu-id="f9181-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-236">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-236">CC003</span></span></td>
<td><span data-ttu-id="f9181-237">Smölun</span><span class="sxs-lookup"><span data-stu-id="f9181-237">Assembly</span></span></td>
<td><span data-ttu-id="f9181-238">0</span><span class="sxs-lookup"><span data-stu-id="f9181-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f9181-239">Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunni fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="f9181-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f9181-240">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-240">Cost object</span></span></th>
<th><span data-ttu-id="f9181-241">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="f9181-241">Magnitude</span></span></th>
<th><span data-ttu-id="f9181-242">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="f9181-242">Allocation factor</span></span></th>
<th><span data-ttu-id="f9181-243">Upphæð</span><span class="sxs-lookup"><span data-stu-id="f9181-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-244">CC001</span><span class="sxs-lookup"><span data-stu-id="f9181-244">CC001</span></span></td>
<td><span data-ttu-id="f9181-245">Mannauður</span><span class="sxs-lookup"><span data-stu-id="f9181-245">HR</span></span></td>
<td><span data-ttu-id="f9181-246">1.000</span><span class="sxs-lookup"><span data-stu-id="f9181-246">1,000</span></span></td>
<td><span data-ttu-id="f9181-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="f9181-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="f9181-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="f9181-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-249">CC002</span><span class="sxs-lookup"><span data-stu-id="f9181-249">CC002</span></span></td>
<td><span data-ttu-id="f9181-250">Fjármál</span><span class="sxs-lookup"><span data-stu-id="f9181-250">Finance</span></span></td>
<td><span data-ttu-id="f9181-251">6,000</span><span class="sxs-lookup"><span data-stu-id="f9181-251">6,000</span></span></td>
<td><span data-ttu-id="f9181-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="f9181-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="f9181-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="f9181-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-254">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-254">CC003</span></span></td>
<td><span data-ttu-id="f9181-255">Smölun</span><span class="sxs-lookup"><span data-stu-id="f9181-255">Assembly</span></span></td>
<td><span data-ttu-id="f9181-256">0</span><span class="sxs-lookup"><span data-stu-id="f9181-256">0</span></span></td>
<td><span data-ttu-id="f9181-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="f9181-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="f9181-258">0,00</span><span class="sxs-lookup"><span data-stu-id="f9181-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f9181-259">Föstum kostnaði þarf að dreifa jafnt á staka kostnaðarhluti sem hafa notað rafmagn.</span><span class="sxs-lookup"><span data-stu-id="f9181-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="f9181-260">Hægt er að ná þessa niðurstöðu með því að nota tölfræðilegt víddarstakið Rafmagn í úthlutunargrunni reikniformúlu: (Rafmagn &gt; 0,00) Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunn fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="f9181-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f9181-261">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-261">Cost object</span></span></th>
<th><span data-ttu-id="f9181-262">Formúla</span><span class="sxs-lookup"><span data-stu-id="f9181-262">Formula</span></span></th>
<th><span data-ttu-id="f9181-263">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="f9181-263">Magnitude</span></span></th>
<th><span data-ttu-id="f9181-264">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="f9181-264">Allocation factor</span></span></th>
<th><span data-ttu-id="f9181-265">Upphæð</span><span class="sxs-lookup"><span data-stu-id="f9181-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-266">CC001</span><span class="sxs-lookup"><span data-stu-id="f9181-266">CC001</span></span></td>
<td><span data-ttu-id="f9181-267">Mannauður</span><span class="sxs-lookup"><span data-stu-id="f9181-267">HR</span></span></td>
<td><span data-ttu-id="f9181-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="f9181-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="f9181-269">1</span><span class="sxs-lookup"><span data-stu-id="f9181-269">1</span></span></td>
<td><span data-ttu-id="f9181-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="f9181-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="f9181-271">500,00</span><span class="sxs-lookup"><span data-stu-id="f9181-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-272">CC002</span><span class="sxs-lookup"><span data-stu-id="f9181-272">CC002</span></span></td>
<td><span data-ttu-id="f9181-273">Fjármál</span><span class="sxs-lookup"><span data-stu-id="f9181-273">Finance</span></span></td>
<td><span data-ttu-id="f9181-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="f9181-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="f9181-275">1</span><span class="sxs-lookup"><span data-stu-id="f9181-275">1</span></span></td>
<td><span data-ttu-id="f9181-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="f9181-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="f9181-277">500,00</span><span class="sxs-lookup"><span data-stu-id="f9181-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-278">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-278">CC003</span></span></td>
<td><span data-ttu-id="f9181-279">Smölun</span><span class="sxs-lookup"><span data-stu-id="f9181-279">Assembly</span></span></td>
<td><span data-ttu-id="f9181-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="f9181-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="f9181-281">0</span><span class="sxs-lookup"><span data-stu-id="f9181-281">0</span></span></td>
<td><span data-ttu-id="f9181-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="f9181-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="f9181-283">0,00</span><span class="sxs-lookup"><span data-stu-id="f9181-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="f9181-284">Færslubók</span><span class="sxs-lookup"><span data-stu-id="f9181-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f9181-285">Færslubók</span><span class="sxs-lookup"><span data-stu-id="f9181-285">Journal</span></span></th>
<th><span data-ttu-id="f9181-286">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="f9181-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f9181-287">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="f9181-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f9181-288">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="f9181-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-289">00002</span><span class="sxs-lookup"><span data-stu-id="f9181-289">00002</span></span></td>
<td><span data-ttu-id="f9181-290">Útreikningabók kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="f9181-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="f9181-291">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="f9181-291">Fiscal</span></span></td>
<td><span data-ttu-id="f9181-292">2017</span><span class="sxs-lookup"><span data-stu-id="f9181-292">2017</span></span></td>
<td><span data-ttu-id="f9181-293">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="f9181-293">Period 1</span></span></td>
<td><span data-ttu-id="f9181-294">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="f9181-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="f9181-295">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="f9181-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f9181-296">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="f9181-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f9181-297">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f9181-298">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="f9181-298">Cost element</span></span></th>
<th><span data-ttu-id="f9181-299">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="f9181-299">Cost behavior</span></span></th>
<th><span data-ttu-id="f9181-300">Upphæð</span><span class="sxs-lookup"><span data-stu-id="f9181-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-301">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="f9181-302">CC099</span><span class="sxs-lookup"><span data-stu-id="f9181-302">CC099</span></span></td>
<td><span data-ttu-id="f9181-303">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="f9181-303">Default cost center</span></span></td>
<td><span data-ttu-id="f9181-304">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-304">10001</span></span></td>
<td><span data-ttu-id="f9181-305">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-305">Electricity</span></span></td>
<td><span data-ttu-id="f9181-306">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-306">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="f9181-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-308">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="f9181-309">CC099</span><span class="sxs-lookup"><span data-stu-id="f9181-309">CC099</span></span></td>
<td><span data-ttu-id="f9181-310">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="f9181-310">Default cost center</span></span></td>
<td><span data-ttu-id="f9181-311">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-311">10001</span></span></td>
<td><span data-ttu-id="f9181-312">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-312">Electricity</span></span></td>
<td><span data-ttu-id="f9181-313">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-313">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="f9181-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f9181-315">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="f9181-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f9181-316">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f9181-317">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="f9181-317">Cost element</span></span></th>
<th><span data-ttu-id="f9181-318">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="f9181-318">Cost behavior</span></span></th>
<th><span data-ttu-id="f9181-319">Upphæð</span><span class="sxs-lookup"><span data-stu-id="f9181-319">Amount</span></span></th>
<th><span data-ttu-id="f9181-320">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="f9181-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-321">CC099</span><span class="sxs-lookup"><span data-stu-id="f9181-321">CC099</span></span></td>
<td><span data-ttu-id="f9181-322">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="f9181-322">Default cost center</span></span></td>
<td><span data-ttu-id="f9181-323">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-323">10001</span></span></td>
<td><span data-ttu-id="f9181-324">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-324">Electricity</span></span></td>
<td><span data-ttu-id="f9181-325">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-325">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="f9181-326">-1,000.00</span></span></td>
<td><span data-ttu-id="f9181-327">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-328">CC001</span><span class="sxs-lookup"><span data-stu-id="f9181-328">CC001</span></span></td>
<td><span data-ttu-id="f9181-329">Mannauður</span><span class="sxs-lookup"><span data-stu-id="f9181-329">HR</span></span></td>
<td><span data-ttu-id="f9181-330">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-330">10001</span></span></td>
<td><span data-ttu-id="f9181-331">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-331">Electricity</span></span></td>
<td><span data-ttu-id="f9181-332">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-332">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-333">500,00</span><span class="sxs-lookup"><span data-stu-id="f9181-333">500.00</span></span></td>
<td><span data-ttu-id="f9181-334">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-335">CC002</span><span class="sxs-lookup"><span data-stu-id="f9181-335">CC002</span></span></td>
<td><span data-ttu-id="f9181-336">Fjármál</span><span class="sxs-lookup"><span data-stu-id="f9181-336">Finance</span></span></td>
<td><span data-ttu-id="f9181-337">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-337">10001</span></span></td>
<td><span data-ttu-id="f9181-338">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-338">Electricity</span></span></td>
<td><span data-ttu-id="f9181-339">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-339">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-340">500,00</span><span class="sxs-lookup"><span data-stu-id="f9181-340">500.00</span></span></td>
<td><span data-ttu-id="f9181-341">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-342">CC099</span><span class="sxs-lookup"><span data-stu-id="f9181-342">CC099</span></span></td>
<td><span data-ttu-id="f9181-343">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="f9181-343">Default cost center</span></span></td>
<td><span data-ttu-id="f9181-344">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-344">10001</span></span></td>
<td><span data-ttu-id="f9181-345">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-345">Electricity</span></span></td>
<td><span data-ttu-id="f9181-346">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-346">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="f9181-347">-9,000.00</span></span></td>
<td><span data-ttu-id="f9181-348">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-349">CC001</span><span class="sxs-lookup"><span data-stu-id="f9181-349">CC001</span></span></td>
<td><span data-ttu-id="f9181-350">Mannauður</span><span class="sxs-lookup"><span data-stu-id="f9181-350">HR</span></span></td>
<td><span data-ttu-id="f9181-351">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-351">10001</span></span></td>
<td><span data-ttu-id="f9181-352">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-352">Electricity</span></span></td>
<td><span data-ttu-id="f9181-353">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-353">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="f9181-354">1,285.71</span></span></td>
<td><span data-ttu-id="f9181-355">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-356">CC002</span><span class="sxs-lookup"><span data-stu-id="f9181-356">CC002</span></span></td>
<td><span data-ttu-id="f9181-357">Fjármál</span><span class="sxs-lookup"><span data-stu-id="f9181-357">Finance</span></span></td>
<td><span data-ttu-id="f9181-358">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-358">10001</span></span></td>
<td><span data-ttu-id="f9181-359">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-359">Electricity</span></span></td>
<td><span data-ttu-id="f9181-360">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-360">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="f9181-361">7,714.29</span></span></td>
<td><span data-ttu-id="f9181-362">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f9181-363">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðardreifingarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="f9181-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="f9181-364">Skref 3: Keyra útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="f9181-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="f9181-365">Sameiginlegur kostnaður er notaður til að rukka einn eða fleiri tilgreinda kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="f9181-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="f9181-366">Gjöldin byggjast á fyrirframákveðnu kostnaðarhlutfalli og mæligildi úr úthlutuðum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="f9181-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="f9181-367">Skilgreina sameiginlegan kostnað</span><span class="sxs-lookup"><span data-stu-id="f9181-367">Define the overhead rate</span></span>

<span data-ttu-id="f9181-368">Kostnaðarhlutur CC001 Mannauður stuðlar að safni innri verka.</span><span class="sxs-lookup"><span data-stu-id="f9181-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="f9181-369">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsverk til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="f9181-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f9181-370">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-370">Cost object</span></span></th>
<th><span data-ttu-id="f9181-371">Tímar</span><span class="sxs-lookup"><span data-stu-id="f9181-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-372">Verk 1</span><span class="sxs-lookup"><span data-stu-id="f9181-372">Proj 1</span></span></td>
<td><span data-ttu-id="f9181-373">Verk 1</span><span class="sxs-lookup"><span data-stu-id="f9181-373">Project 1</span></span></td>
<td><span data-ttu-id="f9181-374">3</span><span class="sxs-lookup"><span data-stu-id="f9181-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-375">Verk 2</span><span class="sxs-lookup"><span data-stu-id="f9181-375">Proj 2</span></span></td>
<td><span data-ttu-id="f9181-376">Verk 2</span><span class="sxs-lookup"><span data-stu-id="f9181-376">Project 2</span></span></td>
<td><span data-ttu-id="f9181-377">1</span><span class="sxs-lookup"><span data-stu-id="f9181-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f9181-378">Fyrirframákveðið kostnaðarhlutfall fyrir kostnaðarframlag verk hefur verið skilgreint.</span><span class="sxs-lookup"><span data-stu-id="f9181-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f9181-379">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-379">Cost object</span></span></th>
<th><span data-ttu-id="f9181-380">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="f9181-380">Cost element</span></span></th>
<th><span data-ttu-id="f9181-381">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="f9181-381">Cost behavior</span></span></th>
<th><span data-ttu-id="f9181-382">Einingar</span><span class="sxs-lookup"><span data-stu-id="f9181-382">Units</span></span></th>
<th><span data-ttu-id="f9181-383">Taxti</span><span class="sxs-lookup"><span data-stu-id="f9181-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-384">CC001</span><span class="sxs-lookup"><span data-stu-id="f9181-384">CC001</span></span></td>
<td><span data-ttu-id="f9181-385">Mannauður</span><span class="sxs-lookup"><span data-stu-id="f9181-385">HR</span></span></td>
<td><span data-ttu-id="f9181-386">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-386">10001</span></span></td>
<td><span data-ttu-id="f9181-387">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-387">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-388">1</span><span class="sxs-lookup"><span data-stu-id="f9181-388">1</span></span></td>
<td><span data-ttu-id="f9181-389">10</span><span class="sxs-lookup"><span data-stu-id="f9181-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f9181-390">Eftirfarandi tafla sýnir niðurstöður þegar Mannauðsverk eru notuð sem grunnur við úthlutun.</span><span class="sxs-lookup"><span data-stu-id="f9181-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f9181-391">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-391">Cost object</span></span></th>
<th><span data-ttu-id="f9181-392">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="f9181-392">Magnitude</span></span></th>
<th><span data-ttu-id="f9181-393">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="f9181-393">Cost element</span></span></th>
<th><span data-ttu-id="f9181-394">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="f9181-394">Allocation factor</span></span></th>
<th><span data-ttu-id="f9181-395">Upphæð</span><span class="sxs-lookup"><span data-stu-id="f9181-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-396">Verk 1</span><span class="sxs-lookup"><span data-stu-id="f9181-396">Proj 1</span></span></td>
<td><span data-ttu-id="f9181-397">Verk 1</span><span class="sxs-lookup"><span data-stu-id="f9181-397">Project 1</span></span></td>
<td><span data-ttu-id="f9181-398">3</span><span class="sxs-lookup"><span data-stu-id="f9181-398">3</span></span></td>
<td><span data-ttu-id="f9181-399">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-399">10001</span></span></td>
<td><span data-ttu-id="f9181-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="f9181-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="f9181-401">30,00</span><span class="sxs-lookup"><span data-stu-id="f9181-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-402">Verk 2</span><span class="sxs-lookup"><span data-stu-id="f9181-402">Proj 2</span></span></td>
<td><span data-ttu-id="f9181-403">Verk 2</span><span class="sxs-lookup"><span data-stu-id="f9181-403">Project 2</span></span></td>
<td><span data-ttu-id="f9181-404">1</span><span class="sxs-lookup"><span data-stu-id="f9181-404">1</span></span></td>
<td><span data-ttu-id="f9181-405">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-405">10001</span></span></td>
<td><span data-ttu-id="f9181-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="f9181-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="f9181-407">10,00</span><span class="sxs-lookup"><span data-stu-id="f9181-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="f9181-408">Færslubók</span><span class="sxs-lookup"><span data-stu-id="f9181-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f9181-409">Færslubók</span><span class="sxs-lookup"><span data-stu-id="f9181-409">Journal</span></span></th>
<th><span data-ttu-id="f9181-410">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="f9181-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f9181-411">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="f9181-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f9181-412">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="f9181-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-413">00003</span><span class="sxs-lookup"><span data-stu-id="f9181-413">00003</span></span></td>
<td><span data-ttu-id="f9181-414">Færslubók fyrir útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="f9181-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="f9181-415">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="f9181-415">Fiscal</span></span></td>
<td><span data-ttu-id="f9181-416">2017</span><span class="sxs-lookup"><span data-stu-id="f9181-416">2017</span></span></td>
<td><span data-ttu-id="f9181-417">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="f9181-417">Period 1</span></span></td>
<td><span data-ttu-id="f9181-418">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="f9181-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="f9181-419">Bókarfærslur (Bókarfærslur fyrir útreikning sameiginlegs kostnaðar)</span><span class="sxs-lookup"><span data-stu-id="f9181-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f9181-420">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="f9181-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f9181-421">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-421">Cost object</span></span></th>
<th><span data-ttu-id="f9181-422">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="f9181-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-423">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="f9181-424">Verk 1</span><span class="sxs-lookup"><span data-stu-id="f9181-424">Proj 1</span></span></td>
<td><span data-ttu-id="f9181-425">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="f9181-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="f9181-426">3,00</span><span class="sxs-lookup"><span data-stu-id="f9181-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-427">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="f9181-428">Verk 2</span><span class="sxs-lookup"><span data-stu-id="f9181-428">Proj 2</span></span></td>
<td><span data-ttu-id="f9181-429">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="f9181-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="f9181-430">1,00</span><span class="sxs-lookup"><span data-stu-id="f9181-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f9181-431">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="f9181-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f9181-432">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f9181-433">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="f9181-433">Cost element</span></span></th>
<th><span data-ttu-id="f9181-434">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="f9181-434">Cost behavior</span></span></th>
<th><span data-ttu-id="f9181-435">Upphæð</span><span class="sxs-lookup"><span data-stu-id="f9181-435">Amount</span></span></th>
<th><span data-ttu-id="f9181-436">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="f9181-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="f9181-437">CC0001</span></span></td>
<td><span data-ttu-id="f9181-438">Mannauður</span><span class="sxs-lookup"><span data-stu-id="f9181-438">HR</span></span></td>
<td><span data-ttu-id="f9181-439">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-439">10001</span></span></td>
<td><span data-ttu-id="f9181-440">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-440">Electricity</span></span></td>
<td><span data-ttu-id="f9181-441">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-441">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="f9181-442">-30.00</span></span></td>
<td><span data-ttu-id="f9181-443">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-444">Verk 1</span><span class="sxs-lookup"><span data-stu-id="f9181-444">Proj 1</span></span></td>
<td><span data-ttu-id="f9181-445">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="f9181-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="f9181-446">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-446">10001</span></span></td>
<td><span data-ttu-id="f9181-447">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-447">Electricity</span></span></td>
<td><span data-ttu-id="f9181-448">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-448">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-449">30,00</span><span class="sxs-lookup"><span data-stu-id="f9181-449">30.00</span></span></td>
<td><span data-ttu-id="f9181-450">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-451">CC001</span><span class="sxs-lookup"><span data-stu-id="f9181-451">CC001</span></span></td>
<td><span data-ttu-id="f9181-452">Mannauður</span><span class="sxs-lookup"><span data-stu-id="f9181-452">HR</span></span></td>
<td><span data-ttu-id="f9181-453">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-453">10001</span></span></td>
<td><span data-ttu-id="f9181-454">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-454">Electricity</span></span></td>
<td><span data-ttu-id="f9181-455">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-455">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="f9181-456">-10.00</span></span></td>
<td><span data-ttu-id="f9181-457">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-458">Verk 2</span><span class="sxs-lookup"><span data-stu-id="f9181-458">Proj 2</span></span></td>
<td><span data-ttu-id="f9181-459">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="f9181-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="f9181-460">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-460">10001</span></span></td>
<td><span data-ttu-id="f9181-461">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-461">Electricity</span></span></td>
<td><span data-ttu-id="f9181-462">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-462">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-463">10,00</span><span class="sxs-lookup"><span data-stu-id="f9181-463">10.00</span></span></td>
<td><span data-ttu-id="f9181-464">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f9181-465">Nánari upplýsingar er að finna í [Framkvæma útreikning fastakostnaðar](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="f9181-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="f9181-466">Skref 4: Keyra útreikning kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="f9181-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="f9181-467">Úthlutun er notuð til að úthluta stöðu kostnaðarhlutar í öðrum kostnaðarhlutum með því að nota úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="f9181-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="f9181-468">Finance styður gagnvirka úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="f9181-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="f9181-469">Í gagnvirkri úthlutunaraðferð er sú sameiginlega þjónusta sem hjálparkostnaðarhlutir skiptast á viðurkennd að fullu.</span><span class="sxs-lookup"><span data-stu-id="f9181-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="f9181-470">Kerfið ákvarðar sjálfkrafa rétta röð til að framkvæma úthlutun eftir.</span><span class="sxs-lookup"><span data-stu-id="f9181-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="f9181-471">Stöðu kostnaðarhluta er úthlutað með einum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="f9181-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="f9181-472">Úthlutanir þvert á víddir kostnaðarhluta og viðkomandi stök þeirra eru studdar.</span><span class="sxs-lookup"><span data-stu-id="f9181-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="f9181-473">Úthlutun pöntunarinnar er stjórnað af stýrieiningu kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="f9181-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="f9181-474">[![Gagnkvæm aðferð](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="f9181-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="f9181-475">Tilgreinið kostnaðarúthlutun</span><span class="sxs-lookup"><span data-stu-id="f9181-475">Define the cost allocation</span></span>

<span data-ttu-id="f9181-476">Hér er einfalt dæmi sem útskýrir hvernig hægt er að rekja flæði kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="f9181-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="f9181-477">Kostnaðarhlutir CC001 Mannauður leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="f9181-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="f9181-478">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="f9181-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f9181-479">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-479">Cost object</span></span></th>
<th><span data-ttu-id="f9181-480">Mannauðsþjónusta</span><span class="sxs-lookup"><span data-stu-id="f9181-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-481">CC002</span><span class="sxs-lookup"><span data-stu-id="f9181-481">CC002</span></span></td>
<td><span data-ttu-id="f9181-482">Fjármál</span><span class="sxs-lookup"><span data-stu-id="f9181-482">Finance</span></span></td>
<td><span data-ttu-id="f9181-483">35</span><span class="sxs-lookup"><span data-stu-id="f9181-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-484">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-484">CC003</span></span></td>
<td><span data-ttu-id="f9181-485">Smölun</span><span class="sxs-lookup"><span data-stu-id="f9181-485">Assembly</span></span></td>
<td><span data-ttu-id="f9181-486">55</span><span class="sxs-lookup"><span data-stu-id="f9181-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-487">CC004</span><span class="sxs-lookup"><span data-stu-id="f9181-487">CC004</span></span></td>
<td><span data-ttu-id="f9181-488">Pakkning</span><span class="sxs-lookup"><span data-stu-id="f9181-488">Packaging</span></span></td>
<td><span data-ttu-id="f9181-489">10</span><span class="sxs-lookup"><span data-stu-id="f9181-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f9181-490">Kostnaðarhlutir CC002 Fjármál leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="f9181-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="f9181-491">Stofnað er tölfræðilegt víddarstak sem kallast Fjármálaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="f9181-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f9181-492">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-492">Cost object</span></span></th>
<th><span data-ttu-id="f9181-493">Fjármálaþjónusta</span><span class="sxs-lookup"><span data-stu-id="f9181-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-494">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-494">CC003</span></span></td>
<td><span data-ttu-id="f9181-495">Smölun</span><span class="sxs-lookup"><span data-stu-id="f9181-495">Assembly</span></span></td>
<td><span data-ttu-id="f9181-496">65</span><span class="sxs-lookup"><span data-stu-id="f9181-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-497">CC004</span><span class="sxs-lookup"><span data-stu-id="f9181-497">CC004</span></span></td>
<td><span data-ttu-id="f9181-498">Pakkning</span><span class="sxs-lookup"><span data-stu-id="f9181-498">Packaging</span></span></td>
<td><span data-ttu-id="f9181-499">35</span><span class="sxs-lookup"><span data-stu-id="f9181-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f9181-500">Kostnaðarhlutir CC003 Samsetning leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="f9181-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="f9181-501">Meðlimur tölfræðilega víddar sem kallast Mannauður verk er stofnað til að mælvíddarstaka notuðum magnitude.</span><span class="sxs-lookup"><span data-stu-id="f9181-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f9181-502">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-502">Cost object</span></span></th>
<th><span data-ttu-id="f9181-503">Samsetningarþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="f9181-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-504">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-504">Prod 1</span></span></td>
<td><span data-ttu-id="f9181-505">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-505">Product 1</span></span></td>
<td><span data-ttu-id="f9181-506">60</span><span class="sxs-lookup"><span data-stu-id="f9181-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-507">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-507">Prod 2</span></span></td>
<td><span data-ttu-id="f9181-508">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-508">Product 2</span></span></td>
<td><span data-ttu-id="f9181-509">20</span><span class="sxs-lookup"><span data-stu-id="f9181-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f9181-510">Kostnaðarhlutir CC004 Umbúðir leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="f9181-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="f9181-511">Stofnað er tölfræðilegt víddarstak sem kallast Umbúðaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="f9181-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f9181-512">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-512">Cost object</span></span></th>
<th><span data-ttu-id="f9181-513">Umbúðaþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="f9181-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-514">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-514">Prod 1</span></span></td>
<td><span data-ttu-id="f9181-515">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-515">Product 1</span></span></td>
<td><span data-ttu-id="f9181-516">80</span><span class="sxs-lookup"><span data-stu-id="f9181-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-517">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-517">Prod 2</span></span></td>
<td><span data-ttu-id="f9181-518">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-518">Product 2</span></span></td>
<td><span data-ttu-id="f9181-519">15</span><span class="sxs-lookup"><span data-stu-id="f9181-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="f9181-520">Hægt er að afleiða tölfræðiaðgerðir eins og framleiðslutíma sem vara notar frá upprunagögnum.</span><span class="sxs-lookup"><span data-stu-id="f9181-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="f9181-521">Nánari upplýsingar er að finna í [Veitusniðmát tölfræðiaðgerðar](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="f9181-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="f9181-522">Eftirfarandi tafla sýnir niðurstöður þegar mannauðsþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="f9181-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f9181-523">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-523">Cost object</span></span></th>
<th><span data-ttu-id="f9181-524">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="f9181-524">Magnitude</span></span></th>
<th><span data-ttu-id="f9181-525">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="f9181-525">Allocation factor</span></span></th>
<th><span data-ttu-id="f9181-526">Upphæð</span><span class="sxs-lookup"><span data-stu-id="f9181-526">Amount</span></span></th>
<th><span data-ttu-id="f9181-527">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="f9181-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-528">CC002</span><span class="sxs-lookup"><span data-stu-id="f9181-528">CC002</span></span></td>
<td><span data-ttu-id="f9181-529">Fjármál</span><span class="sxs-lookup"><span data-stu-id="f9181-529">Finance</span></span></td>
<td><span data-ttu-id="f9181-530">35</span><span class="sxs-lookup"><span data-stu-id="f9181-530">35</span></span></td>
<td><span data-ttu-id="f9181-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="f9181-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="f9181-532">175.00</span><span class="sxs-lookup"><span data-stu-id="f9181-532">175.00</span></span></td>
<td><span data-ttu-id="f9181-533">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-534">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-534">CC003</span></span></td>
<td><span data-ttu-id="f9181-535">Smölun</span><span class="sxs-lookup"><span data-stu-id="f9181-535">Assembly</span></span></td>
<td><span data-ttu-id="f9181-536">55</span><span class="sxs-lookup"><span data-stu-id="f9181-536">55</span></span></td>
<td><span data-ttu-id="f9181-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="f9181-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="f9181-538">275.00</span><span class="sxs-lookup"><span data-stu-id="f9181-538">275.00</span></span></td>
<td><span data-ttu-id="f9181-539">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-540">CC004</span><span class="sxs-lookup"><span data-stu-id="f9181-540">CC004</span></span></td>
<td><span data-ttu-id="f9181-541">Pakkning</span><span class="sxs-lookup"><span data-stu-id="f9181-541">Packaging</span></span></td>
<td><span data-ttu-id="f9181-542">10</span><span class="sxs-lookup"><span data-stu-id="f9181-542">10</span></span></td>
<td><span data-ttu-id="f9181-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="f9181-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="f9181-544">50,00</span><span class="sxs-lookup"><span data-stu-id="f9181-544">50.00</span></span></td>
<td><span data-ttu-id="f9181-545">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-546">CC002</span><span class="sxs-lookup"><span data-stu-id="f9181-546">CC002</span></span></td>
<td><span data-ttu-id="f9181-547">Fjármál</span><span class="sxs-lookup"><span data-stu-id="f9181-547">Finance</span></span></td>
<td><span data-ttu-id="f9181-548">35</span><span class="sxs-lookup"><span data-stu-id="f9181-548">35</span></span></td>
<td><span data-ttu-id="f9181-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="f9181-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="f9181-550">436.00</span><span class="sxs-lookup"><span data-stu-id="f9181-550">436.00</span></span></td>
<td><span data-ttu-id="f9181-551">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-552">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-552">CC003</span></span></td>
<td><span data-ttu-id="f9181-553">Smölun</span><span class="sxs-lookup"><span data-stu-id="f9181-553">Assembly</span></span></td>
<td><span data-ttu-id="f9181-554">55</span><span class="sxs-lookup"><span data-stu-id="f9181-554">55</span></span></td>
<td><span data-ttu-id="f9181-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="f9181-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="f9181-556">685.14</span><span class="sxs-lookup"><span data-stu-id="f9181-556">685.14</span></span></td>
<td><span data-ttu-id="f9181-557">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-558">CC004</span><span class="sxs-lookup"><span data-stu-id="f9181-558">CC004</span></span></td>
<td><span data-ttu-id="f9181-559">Pakkning</span><span class="sxs-lookup"><span data-stu-id="f9181-559">Packaging</span></span></td>
<td><span data-ttu-id="f9181-560">10</span><span class="sxs-lookup"><span data-stu-id="f9181-560">10</span></span></td>
<td><span data-ttu-id="f9181-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="f9181-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="f9181-562">124.57</span><span class="sxs-lookup"><span data-stu-id="f9181-562">124.57</span></span></td>
<td><span data-ttu-id="f9181-563">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f9181-564">Eftirfarandi tafla sýnir niðurstöður þegar Fjármálaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="f9181-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f9181-565">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-565">Cost object</span></span></th>
<th><span data-ttu-id="f9181-566">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="f9181-566">Magnitude</span></span></th>
<th><span data-ttu-id="f9181-567">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="f9181-567">Allocation factor</span></span></th>
<th><span data-ttu-id="f9181-568">Upphæð</span><span class="sxs-lookup"><span data-stu-id="f9181-568">Amount</span></span></th>
<th><span data-ttu-id="f9181-569">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="f9181-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-570">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-570">CC003</span></span></td>
<td><span data-ttu-id="f9181-571">Smölun</span><span class="sxs-lookup"><span data-stu-id="f9181-571">Assembly</span></span></td>
<td><span data-ttu-id="f9181-572">65</span><span class="sxs-lookup"><span data-stu-id="f9181-572">65</span></span></td>
<td><span data-ttu-id="f9181-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="f9181-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="f9181-574">438.75</span><span class="sxs-lookup"><span data-stu-id="f9181-574">438.75</span></span></td>
<td><span data-ttu-id="f9181-575">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-576">CC004</span><span class="sxs-lookup"><span data-stu-id="f9181-576">CC004</span></span></td>
<td><span data-ttu-id="f9181-577">Pakkning</span><span class="sxs-lookup"><span data-stu-id="f9181-577">Packaging</span></span></td>
<td><span data-ttu-id="f9181-578">35</span><span class="sxs-lookup"><span data-stu-id="f9181-578">35</span></span></td>
<td><span data-ttu-id="f9181-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="f9181-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="f9181-580">236.25</span><span class="sxs-lookup"><span data-stu-id="f9181-580">236.25</span></span></td>
<td><span data-ttu-id="f9181-581">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-582">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-582">CC003</span></span></td>
<td><span data-ttu-id="f9181-583">Smölun</span><span class="sxs-lookup"><span data-stu-id="f9181-583">Assembly</span></span></td>
<td><span data-ttu-id="f9181-584">65</span><span class="sxs-lookup"><span data-stu-id="f9181-584">65</span></span></td>
<td><span data-ttu-id="f9181-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="f9181-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="f9181-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="f9181-586">5,297.69</span></span></td>
<td><span data-ttu-id="f9181-587">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-588">CC004</span><span class="sxs-lookup"><span data-stu-id="f9181-588">CC004</span></span></td>
<td><span data-ttu-id="f9181-589">Pakkning</span><span class="sxs-lookup"><span data-stu-id="f9181-589">Packaging</span></span></td>
<td><span data-ttu-id="f9181-590">35</span><span class="sxs-lookup"><span data-stu-id="f9181-590">35</span></span></td>
<td><span data-ttu-id="f9181-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="f9181-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="f9181-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="f9181-592">2,852.60</span></span></td>
<td><span data-ttu-id="f9181-593">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f9181-594">Eftirfarandi tafla sýnir niðurstöður þegar Samsetningarþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="f9181-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f9181-595">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-595">Cost object</span></span></th>
<th><span data-ttu-id="f9181-596">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="f9181-596">Magnitude</span></span></th>
<th><span data-ttu-id="f9181-597">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="f9181-597">Allocation factor</span></span></th>
<th><span data-ttu-id="f9181-598">Upphæð</span><span class="sxs-lookup"><span data-stu-id="f9181-598">Amount</span></span></th>
<th><span data-ttu-id="f9181-599">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="f9181-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-600">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-600">Prod 1</span></span></td>
<td><span data-ttu-id="f9181-601">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-601">Product 1</span></span></td>
<td><span data-ttu-id="f9181-602">60</span><span class="sxs-lookup"><span data-stu-id="f9181-602">60</span></span></td>
<td><span data-ttu-id="f9181-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="f9181-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="f9181-604">535.31</span><span class="sxs-lookup"><span data-stu-id="f9181-604">535.31</span></span></td>
<td><span data-ttu-id="f9181-605">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-606">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-606">Prod 2</span></span></td>
<td><span data-ttu-id="f9181-607">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-607">Product 2</span></span></td>
<td><span data-ttu-id="f9181-608">20</span><span class="sxs-lookup"><span data-stu-id="f9181-608">20</span></span></td>
<td><span data-ttu-id="f9181-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="f9181-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="f9181-610">178.44</span><span class="sxs-lookup"><span data-stu-id="f9181-610">178.44</span></span></td>
<td><span data-ttu-id="f9181-611">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-612">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-612">Prod 1</span></span></td>
<td><span data-ttu-id="f9181-613">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-613">Product 1</span></span></td>
<td><span data-ttu-id="f9181-614">60</span><span class="sxs-lookup"><span data-stu-id="f9181-614">60</span></span></td>
<td><span data-ttu-id="f9181-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="f9181-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="f9181-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="f9181-616">4,487.12</span></span></td>
<td><span data-ttu-id="f9181-617">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-618">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-618">Prod 2</span></span></td>
<td><span data-ttu-id="f9181-619">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-619">Product 2</span></span></td>
<td><span data-ttu-id="f9181-620">20</span><span class="sxs-lookup"><span data-stu-id="f9181-620">20</span></span></td>
<td><span data-ttu-id="f9181-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="f9181-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="f9181-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="f9181-622">1,495.71</span></span></td>
<td><span data-ttu-id="f9181-623">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f9181-624">Eftirfarandi tafla sýnir niðurstöður þegar Umbúðaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="f9181-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f9181-625">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-625">Cost object</span></span></th>
<th><span data-ttu-id="f9181-626">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="f9181-626">Magnitude</span></span></th>
<th><span data-ttu-id="f9181-627">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="f9181-627">Allocation factor</span></span></th>
<th><span data-ttu-id="f9181-628">Upphæð</span><span class="sxs-lookup"><span data-stu-id="f9181-628">Amount</span></span></th>
<th><span data-ttu-id="f9181-629">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="f9181-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-630">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-630">Prod 1</span></span></td>
<td><span data-ttu-id="f9181-631">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-631">Product 1</span></span></td>
<td><span data-ttu-id="f9181-632">80</span><span class="sxs-lookup"><span data-stu-id="f9181-632">80</span></span></td>
<td><span data-ttu-id="f9181-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="f9181-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="f9181-634">241.05</span><span class="sxs-lookup"><span data-stu-id="f9181-634">241.05</span></span></td>
<td><span data-ttu-id="f9181-635">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-636">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-636">Prod 2</span></span></td>
<td><span data-ttu-id="f9181-637">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-637">Product 2</span></span></td>
<td><span data-ttu-id="f9181-638">15</span><span class="sxs-lookup"><span data-stu-id="f9181-638">15</span></span></td>
<td><span data-ttu-id="f9181-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="f9181-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="f9181-640">45.20</span><span class="sxs-lookup"><span data-stu-id="f9181-640">45.20</span></span></td>
<td><span data-ttu-id="f9181-641">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-642">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-642">Prod 1</span></span></td>
<td><span data-ttu-id="f9181-643">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-643">Product 1</span></span></td>
<td><span data-ttu-id="f9181-644">80</span><span class="sxs-lookup"><span data-stu-id="f9181-644">80</span></span></td>
<td><span data-ttu-id="f9181-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="f9181-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="f9181-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="f9181-646">2,507.09</span></span></td>
<td><span data-ttu-id="f9181-647">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-648">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-648">Prod 2</span></span></td>
<td><span data-ttu-id="f9181-649">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-649">Product 2</span></span></td>
<td><span data-ttu-id="f9181-650">15</span><span class="sxs-lookup"><span data-stu-id="f9181-650">15</span></span></td>
<td><span data-ttu-id="f9181-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="f9181-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="f9181-652">470.08</span><span class="sxs-lookup"><span data-stu-id="f9181-652">470.08</span></span></td>
<td><span data-ttu-id="f9181-653">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="f9181-654">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="f9181-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f9181-655">Færslubók</span><span class="sxs-lookup"><span data-stu-id="f9181-655">Journal</span></span></th>
<th><span data-ttu-id="f9181-656">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="f9181-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="f9181-657">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="f9181-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="f9181-658">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="f9181-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-659">00004</span><span class="sxs-lookup"><span data-stu-id="f9181-659">00004</span></span></td>
<td><span data-ttu-id="f9181-660">Færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="f9181-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="f9181-661">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="f9181-661">Fiscal</span></span></td>
<td><span data-ttu-id="f9181-662">2017</span><span class="sxs-lookup"><span data-stu-id="f9181-662">2017</span></span></td>
<td><span data-ttu-id="f9181-663">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="f9181-663">Period 1</span></span></td>
<td><span data-ttu-id="f9181-664">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="f9181-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="f9181-665">Færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="f9181-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="f9181-666">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="f9181-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="f9181-667">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f9181-668">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="f9181-668">Cost element</span></span></th>
<th><span data-ttu-id="f9181-669">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="f9181-669">Cost behavior</span></span></th>
<th><span data-ttu-id="f9181-670">Upphæð</span><span class="sxs-lookup"><span data-stu-id="f9181-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-671">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="f9181-672">CC001</span><span class="sxs-lookup"><span data-stu-id="f9181-672">CC001</span></span></td>
<td><span data-ttu-id="f9181-673">Mannauður</span><span class="sxs-lookup"><span data-stu-id="f9181-673">HR</span></span></td>
<td><span data-ttu-id="f9181-674">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-674">10001</span></span></td>
<td><span data-ttu-id="f9181-675">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-675">Electricity</span></span></td>
<td><span data-ttu-id="f9181-676">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-676">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-677">500,00</span><span class="sxs-lookup"><span data-stu-id="f9181-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-678">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="f9181-679">CC001</span><span class="sxs-lookup"><span data-stu-id="f9181-679">CC001</span></span></td>
<td><span data-ttu-id="f9181-680">Mannauður</span><span class="sxs-lookup"><span data-stu-id="f9181-680">HR</span></span></td>
<td><span data-ttu-id="f9181-681">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-681">10001</span></span></td>
<td><span data-ttu-id="f9181-682">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-682">Electricity</span></span></td>
<td><span data-ttu-id="f9181-683">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-683">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="f9181-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-685">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="f9181-686">CC002</span><span class="sxs-lookup"><span data-stu-id="f9181-686">CC002</span></span></td>
<td><span data-ttu-id="f9181-687">Fjármál</span><span class="sxs-lookup"><span data-stu-id="f9181-687">Finance</span></span></td>
<td><span data-ttu-id="f9181-688">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-688">10001</span></span></td>
<td><span data-ttu-id="f9181-689">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-689">Electricity</span></span></td>
<td><span data-ttu-id="f9181-690">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-690">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-691">675.00</span><span class="sxs-lookup"><span data-stu-id="f9181-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-692">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="f9181-693">CC002</span><span class="sxs-lookup"><span data-stu-id="f9181-693">CC002</span></span></td>
<td><span data-ttu-id="f9181-694">Fjármál</span><span class="sxs-lookup"><span data-stu-id="f9181-694">Finance</span></span></td>
<td><span data-ttu-id="f9181-695">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-695">10001</span></span></td>
<td><span data-ttu-id="f9181-696">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-696">Electricity</span></span></td>
<td><span data-ttu-id="f9181-697">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-697">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="f9181-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-699">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="f9181-700">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-700">CC003</span></span></td>
<td><span data-ttu-id="f9181-701">Smölun</span><span class="sxs-lookup"><span data-stu-id="f9181-701">Assembly</span></span></td>
<td><span data-ttu-id="f9181-702">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-702">10001</span></span></td>
<td><span data-ttu-id="f9181-703">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-703">Electricity</span></span></td>
<td><span data-ttu-id="f9181-704">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-704">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-705">713.75</span><span class="sxs-lookup"><span data-stu-id="f9181-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-706">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="f9181-707">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-707">CC003</span></span></td>
<td><span data-ttu-id="f9181-708">Smölun</span><span class="sxs-lookup"><span data-stu-id="f9181-708">Assembly</span></span></td>
<td><span data-ttu-id="f9181-709">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-709">10001</span></span></td>
<td><span data-ttu-id="f9181-710">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-710">Electricity</span></span></td>
<td><span data-ttu-id="f9181-711">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-711">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="f9181-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-713">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="f9181-714">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-714">CC003</span></span></td>
<td><span data-ttu-id="f9181-715">Pakkning</span><span class="sxs-lookup"><span data-stu-id="f9181-715">Packaging</span></span></td>
<td><span data-ttu-id="f9181-716">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-716">10001</span></span></td>
<td><span data-ttu-id="f9181-717">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-717">Electricity</span></span></td>
<td><span data-ttu-id="f9181-718">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-718">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-719">286.25</span><span class="sxs-lookup"><span data-stu-id="f9181-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-720">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="f9181-721">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-721">CC003</span></span></td>
<td><span data-ttu-id="f9181-722">Pakkning</span><span class="sxs-lookup"><span data-stu-id="f9181-722">Packaging</span></span></td>
<td><span data-ttu-id="f9181-723">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-723">10001</span></span></td>
<td><span data-ttu-id="f9181-724">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-724">Electricity</span></span></td>
<td><span data-ttu-id="f9181-725">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-725">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="f9181-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-727">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="f9181-728">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-728">Prod 1</span></span></td>
<td><span data-ttu-id="f9181-729">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-729">Product 1</span></span></td>
<td><span data-ttu-id="f9181-730">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-730">10001</span></span></td>
<td><span data-ttu-id="f9181-731">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-731">Electricity</span></span></td>
<td><span data-ttu-id="f9181-732">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-732">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-733">776.36</span><span class="sxs-lookup"><span data-stu-id="f9181-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-734">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="f9181-735">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-735">Prod 1</span></span></td>
<td><span data-ttu-id="f9181-736">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-736">Product 1</span></span></td>
<td><span data-ttu-id="f9181-737">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-737">10001</span></span></td>
<td><span data-ttu-id="f9181-738">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-738">Electricity</span></span></td>
<td><span data-ttu-id="f9181-739">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-739">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="f9181-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-741">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="f9181-742">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-742">Prod 2</span></span></td>
<td><span data-ttu-id="f9181-743">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-743">Product 1</span></span></td>
<td><span data-ttu-id="f9181-744">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-744">10001</span></span></td>
<td><span data-ttu-id="f9181-745">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-745">Electricity</span></span></td>
<td><span data-ttu-id="f9181-746">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-746">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-747">223.64</span><span class="sxs-lookup"><span data-stu-id="f9181-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-748">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="f9181-749">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-749">Prod 2</span></span></td>
<td><span data-ttu-id="f9181-750">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-750">Product 1</span></span></td>
<td><span data-ttu-id="f9181-751">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-751">10001</span></span></td>
<td><span data-ttu-id="f9181-752">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-752">Electricity</span></span></td>
<td><span data-ttu-id="f9181-753">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-753">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="f9181-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="f9181-755">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="f9181-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="f9181-756">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="f9181-757">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="f9181-757">Cost element</span></span></th>
<th><span data-ttu-id="f9181-758">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="f9181-758">Cost behavior</span></span></th>
<th><span data-ttu-id="f9181-759">Upphæð</span><span class="sxs-lookup"><span data-stu-id="f9181-759">Amount</span></span></th>
<th><span data-ttu-id="f9181-760">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="f9181-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f9181-761">CC001</span><span class="sxs-lookup"><span data-stu-id="f9181-761">CC001</span></span></td>
<td><span data-ttu-id="f9181-762">Mannauður</span><span class="sxs-lookup"><span data-stu-id="f9181-762">HR</span></span></td>
<td><span data-ttu-id="f9181-763">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-763">10001</span></span></td>
<td><span data-ttu-id="f9181-764">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-764">Electricity</span></span></td>
<td><span data-ttu-id="f9181-765">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-765">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="f9181-766">-500.00</span></span></td>
<td><span data-ttu-id="f9181-767">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-768">CC002</span><span class="sxs-lookup"><span data-stu-id="f9181-768">CC002</span></span></td>
<td><span data-ttu-id="f9181-769">Fjármál</span><span class="sxs-lookup"><span data-stu-id="f9181-769">Finance</span></span></td>
<td><span data-ttu-id="f9181-770">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-770">10001</span></span></td>
<td><span data-ttu-id="f9181-771">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-771">Electricity</span></span></td>
<td><span data-ttu-id="f9181-772">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-772">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-773">175.00</span><span class="sxs-lookup"><span data-stu-id="f9181-773">175.00</span></span></td>
<td><span data-ttu-id="f9181-774">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-775">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-775">CC003</span></span></td>
<td><span data-ttu-id="f9181-776">Smölun</span><span class="sxs-lookup"><span data-stu-id="f9181-776">Assembly</span></span></td>
<td><span data-ttu-id="f9181-777">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-777">10001</span></span></td>
<td><span data-ttu-id="f9181-778">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-778">Electricity</span></span></td>
<td><span data-ttu-id="f9181-779">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-779">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-780">275.00</span><span class="sxs-lookup"><span data-stu-id="f9181-780">275.00</span></span></td>
<td><span data-ttu-id="f9181-781">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-782">CC004</span><span class="sxs-lookup"><span data-stu-id="f9181-782">CC004</span></span></td>
<td><span data-ttu-id="f9181-783">Pakkning</span><span class="sxs-lookup"><span data-stu-id="f9181-783">Packaging</span></span></td>
<td><span data-ttu-id="f9181-784">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-784">10001</span></span></td>
<td><span data-ttu-id="f9181-785">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-785">Electricity</span></span></td>
<td><span data-ttu-id="f9181-786">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-786">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-787">50,00</span><span class="sxs-lookup"><span data-stu-id="f9181-787">50,00</span></span></td>
<td><span data-ttu-id="f9181-788">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-789">CC001</span><span class="sxs-lookup"><span data-stu-id="f9181-789">CC001</span></span></td>
<td><span data-ttu-id="f9181-790">Mannauður</span><span class="sxs-lookup"><span data-stu-id="f9181-790">HR</span></span></td>
<td><span data-ttu-id="f9181-791">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-791">10001</span></span></td>
<td><span data-ttu-id="f9181-792">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-792">Electricity</span></span></td>
<td><span data-ttu-id="f9181-793">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-793">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="f9181-794">-1,245.71</span></span></td>
<td><span data-ttu-id="f9181-795">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-796">CC002</span><span class="sxs-lookup"><span data-stu-id="f9181-796">CC002</span></span></td>
<td><span data-ttu-id="f9181-797">Fjármál</span><span class="sxs-lookup"><span data-stu-id="f9181-797">Finance</span></span></td>
<td><span data-ttu-id="f9181-798">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-798">10001</span></span></td>
<td><span data-ttu-id="f9181-799">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-799">Electricity</span></span></td>
<td><span data-ttu-id="f9181-800">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-800">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-801">436.00</span><span class="sxs-lookup"><span data-stu-id="f9181-801">436.00</span></span></td>
<td><span data-ttu-id="f9181-802">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-803">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-803">CC003</span></span></td>
<td><span data-ttu-id="f9181-804">Smölun</span><span class="sxs-lookup"><span data-stu-id="f9181-804">Assembly</span></span></td>
<td><span data-ttu-id="f9181-805">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-805">10001</span></span></td>
<td><span data-ttu-id="f9181-806">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-806">Electricity</span></span></td>
<td><span data-ttu-id="f9181-807">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-807">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-808">685.14</span><span class="sxs-lookup"><span data-stu-id="f9181-808">685.14</span></span></td>
<td><span data-ttu-id="f9181-809">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-810">CC004</span><span class="sxs-lookup"><span data-stu-id="f9181-810">CC004</span></span></td>
<td><span data-ttu-id="f9181-811">Pakkning</span><span class="sxs-lookup"><span data-stu-id="f9181-811">Packaging</span></span></td>
<td><span data-ttu-id="f9181-812">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-812">10001</span></span></td>
<td><span data-ttu-id="f9181-813">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-813">Electricity</span></span></td>
<td><span data-ttu-id="f9181-814">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-814">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-815">124.57</span><span class="sxs-lookup"><span data-stu-id="f9181-815">124.57</span></span></td>
<td><span data-ttu-id="f9181-816">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-817">CC002</span><span class="sxs-lookup"><span data-stu-id="f9181-817">CC002</span></span></td>
<td><span data-ttu-id="f9181-818">Fjármál</span><span class="sxs-lookup"><span data-stu-id="f9181-818">Finance</span></span></td>
<td><span data-ttu-id="f9181-819">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-819">10001</span></span></td>
<td><span data-ttu-id="f9181-820">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-820">Electricity</span></span></td>
<td><span data-ttu-id="f9181-821">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-821">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="f9181-822">-675.00</span></span></td>
<td><span data-ttu-id="f9181-823">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-824">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-824">CC003</span></span></td>
<td><span data-ttu-id="f9181-825">Smölun</span><span class="sxs-lookup"><span data-stu-id="f9181-825">Assembly</span></span></td>
<td><span data-ttu-id="f9181-826">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-826">10001</span></span></td>
<td><span data-ttu-id="f9181-827">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-827">Electricity</span></span></td>
<td><span data-ttu-id="f9181-828">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-828">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-829">438.75</span><span class="sxs-lookup"><span data-stu-id="f9181-829">438.75</span></span></td>
<td><span data-ttu-id="f9181-830">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-831">CC004</span><span class="sxs-lookup"><span data-stu-id="f9181-831">CC004</span></span></td>
<td><span data-ttu-id="f9181-832">Pakkning</span><span class="sxs-lookup"><span data-stu-id="f9181-832">Packaging</span></span></td>
<td><span data-ttu-id="f9181-833">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-833">10001</span></span></td>
<td><span data-ttu-id="f9181-834">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-834">Electricity</span></span></td>
<td><span data-ttu-id="f9181-835">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-835">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-836">236.25</span><span class="sxs-lookup"><span data-stu-id="f9181-836">236.25</span></span></td>
<td><span data-ttu-id="f9181-837">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-838">CC002</span><span class="sxs-lookup"><span data-stu-id="f9181-838">CC002</span></span></td>
<td><span data-ttu-id="f9181-839">Fjármál</span><span class="sxs-lookup"><span data-stu-id="f9181-839">Finance</span></span></td>
<td><span data-ttu-id="f9181-840">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-840">10001</span></span></td>
<td><span data-ttu-id="f9181-841">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-841">Electricity</span></span></td>
<td><span data-ttu-id="f9181-842">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-842">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="f9181-843">-8,150.29</span></span></td>
<td><span data-ttu-id="f9181-844">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-845">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-845">CC003</span></span></td>
<td><span data-ttu-id="f9181-846">Smölun</span><span class="sxs-lookup"><span data-stu-id="f9181-846">Assembly</span></span></td>
<td><span data-ttu-id="f9181-847">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-847">10001</span></span></td>
<td><span data-ttu-id="f9181-848">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-848">Electricity</span></span></td>
<td><span data-ttu-id="f9181-849">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-849">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="f9181-850">5,297.69</span></span></td>
<td><span data-ttu-id="f9181-851">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-852">CC004</span><span class="sxs-lookup"><span data-stu-id="f9181-852">CC004</span></span></td>
<td><span data-ttu-id="f9181-853">Pakkning</span><span class="sxs-lookup"><span data-stu-id="f9181-853">Packaging</span></span></td>
<td><span data-ttu-id="f9181-854">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-854">10001</span></span></td>
<td><span data-ttu-id="f9181-855">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-855">Electricity</span></span></td>
<td><span data-ttu-id="f9181-856">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-856">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="f9181-857">2,852.60</span></span></td>
<td><span data-ttu-id="f9181-858">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-859">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-859">CC003</span></span></td>
<td><span data-ttu-id="f9181-860">Smölun</span><span class="sxs-lookup"><span data-stu-id="f9181-860">Assembly</span></span></td>
<td><span data-ttu-id="f9181-861">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-861">10001</span></span></td>
<td><span data-ttu-id="f9181-862">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-862">Electricity</span></span></td>
<td><span data-ttu-id="f9181-863">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-863">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="f9181-864">-713.75</span></span></td>
<td><span data-ttu-id="f9181-865">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-866">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-866">Prod 1</span></span></td>
<td><span data-ttu-id="f9181-867">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-867">Product 1</span></span></td>
<td><span data-ttu-id="f9181-868">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-868">10001</span></span></td>
<td><span data-ttu-id="f9181-869">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-869">Electricity</span></span></td>
<td><span data-ttu-id="f9181-870">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-870">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-871">535.31</span><span class="sxs-lookup"><span data-stu-id="f9181-871">535.31</span></span></td>
<td><span data-ttu-id="f9181-872">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-873">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-873">Prod 2</span></span></td>
<td><span data-ttu-id="f9181-874">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-874">Product 2</span></span></td>
<td><span data-ttu-id="f9181-875">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-875">10001</span></span></td>
<td><span data-ttu-id="f9181-876">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-876">Electricity</span></span></td>
<td><span data-ttu-id="f9181-877">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-877">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-878">178.44</span><span class="sxs-lookup"><span data-stu-id="f9181-878">178.44</span></span></td>
<td><span data-ttu-id="f9181-879">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-880">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-880">CC003</span></span></td>
<td><span data-ttu-id="f9181-881">Smölun</span><span class="sxs-lookup"><span data-stu-id="f9181-881">Assembly</span></span></td>
<td><span data-ttu-id="f9181-882">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-882">10001</span></span></td>
<td><span data-ttu-id="f9181-883">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-883">Electricity</span></span></td>
<td><span data-ttu-id="f9181-884">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-884">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="f9181-885">-5,982.83</span></span></td>
<td><span data-ttu-id="f9181-886">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-887">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-887">Prod 1</span></span></td>
<td><span data-ttu-id="f9181-888">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-888">Product 1</span></span></td>
<td><span data-ttu-id="f9181-889">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-889">10001</span></span></td>
<td><span data-ttu-id="f9181-890">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-890">Electricity</span></span></td>
<td><span data-ttu-id="f9181-891">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-891">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="f9181-892">4,487.12</span></span></td>
<td><span data-ttu-id="f9181-893">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-894">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-894">Prod 2</span></span></td>
<td><span data-ttu-id="f9181-895">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-895">Product 2</span></span></td>
<td><span data-ttu-id="f9181-896">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-896">10001</span></span></td>
<td><span data-ttu-id="f9181-897">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-897">Electricity</span></span></td>
<td><span data-ttu-id="f9181-898">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-898">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="f9181-899">1,495.71</span></span></td>
<td><span data-ttu-id="f9181-900">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-901">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-901">CC003</span></span></td>
<td><span data-ttu-id="f9181-902">Smölun</span><span class="sxs-lookup"><span data-stu-id="f9181-902">Assembly</span></span></td>
<td><span data-ttu-id="f9181-903">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-903">10001</span></span></td>
<td><span data-ttu-id="f9181-904">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-904">Electricity</span></span></td>
<td><span data-ttu-id="f9181-905">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-905">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="f9181-906">-286.25</span></span></td>
<td><span data-ttu-id="f9181-907">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-908">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-908">Prod 1</span></span></td>
<td><span data-ttu-id="f9181-909">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-909">Product 1</span></span></td>
<td><span data-ttu-id="f9181-910">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-910">10001</span></span></td>
<td><span data-ttu-id="f9181-911">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-911">Electricity</span></span></td>
<td><span data-ttu-id="f9181-912">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-912">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-913">241.05</span><span class="sxs-lookup"><span data-stu-id="f9181-913">241.05</span></span></td>
<td><span data-ttu-id="f9181-914">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-915">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-915">Prod 2</span></span></td>
<td><span data-ttu-id="f9181-916">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-916">Product 2</span></span></td>
<td><span data-ttu-id="f9181-917">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-917">10001</span></span></td>
<td><span data-ttu-id="f9181-918">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-918">Electricity</span></span></td>
<td><span data-ttu-id="f9181-919">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-919">Fixed cost</span></span></td>
<td><span data-ttu-id="f9181-920">45.20</span><span class="sxs-lookup"><span data-stu-id="f9181-920">45.20</span></span></td>
<td><span data-ttu-id="f9181-921">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-922">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-922">CC003</span></span></td>
<td><span data-ttu-id="f9181-923">Smölun</span><span class="sxs-lookup"><span data-stu-id="f9181-923">Assembly</span></span></td>
<td><span data-ttu-id="f9181-924">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-924">10001</span></span></td>
<td><span data-ttu-id="f9181-925">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-925">Electricity</span></span></td>
<td><span data-ttu-id="f9181-926">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-926">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="f9181-927">-2,977.17</span></span></td>
<td><span data-ttu-id="f9181-928">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-929">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-929">Prod 1</span></span></td>
<td><span data-ttu-id="f9181-930">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-930">Product 1</span></span></td>
<td><span data-ttu-id="f9181-931">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-931">10001</span></span></td>
<td><span data-ttu-id="f9181-932">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-932">Electricity</span></span></td>
<td><span data-ttu-id="f9181-933">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-933">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="f9181-934">2,507.09</span></span></td>
<td><span data-ttu-id="f9181-935">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f9181-936">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-936">Prod 2</span></span></td>
<td><span data-ttu-id="f9181-937">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-937">Product 2</span></span></td>
<td><span data-ttu-id="f9181-938">10001</span><span class="sxs-lookup"><span data-stu-id="f9181-938">10001</span></span></td>
<td><span data-ttu-id="f9181-939">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-939">Electricity</span></span></td>
<td><span data-ttu-id="f9181-940">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-940">Variable cost</span></span></td>
<td><span data-ttu-id="f9181-941">470.08</span><span class="sxs-lookup"><span data-stu-id="f9181-941">470.08</span></span></td>
<td><span data-ttu-id="f9181-942">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="f9181-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="f9181-943">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="f9181-943">Conclusion</span></span>
<span data-ttu-id="f9181-944">Í Fjárhagsbókhaldi er kostnaður upp á 10.000,00 fyrir rafmagn bókaður á kenni leppkostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="f9181-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="f9181-945">Þar af leiðandi munu kostnaðarbókarar vita að það þarf að úthluta þessum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="f9181-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="f9181-946">Í kostnaðarbókhaldi streymir kostnaður þvert á fyrirtækiseiningar og stig, samkvæmt þeim stefnum og reglum sem eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="f9181-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="f9181-947">Hver kostnaður hefur verið tengdur úthlutunargrunni sem veitir besta mat á úthlutun á kostnaði.</span><span class="sxs-lookup"><span data-stu-id="f9181-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="f9181-948">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="f9181-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="f9181-949">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="f9181-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="f9181-950">Samtala</span><span class="sxs-lookup"><span data-stu-id="f9181-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f9181-951">CC099</span><span class="sxs-lookup"><span data-stu-id="f9181-951">CC099</span></span></th>
<th><span data-ttu-id="f9181-952">CC001</span><span class="sxs-lookup"><span data-stu-id="f9181-952">CC001</span></span></th>
<th><span data-ttu-id="f9181-953">CC002</span><span class="sxs-lookup"><span data-stu-id="f9181-953">CC002</span></span></th>
<th><span data-ttu-id="f9181-954">CC003</span><span class="sxs-lookup"><span data-stu-id="f9181-954">CC003</span></span></th>
<th><span data-ttu-id="f9181-955">CC004</span><span class="sxs-lookup"><span data-stu-id="f9181-955">CC004</span></span></th>
<th><span data-ttu-id="f9181-956">Verk 1</span><span class="sxs-lookup"><span data-stu-id="f9181-956">Proj 1</span></span></th>
<th><span data-ttu-id="f9181-957">Verk 2</span><span class="sxs-lookup"><span data-stu-id="f9181-957">Proj 2</span></span></th>
<th><span data-ttu-id="f9181-958">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="f9181-958">Prod 1</span></span></th>
<th><span data-ttu-id="f9181-959">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="f9181-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="f9181-960">10001 Rafmagn</span><span class="sxs-lookup"><span data-stu-id="f9181-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="f9181-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="f9181-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="f9181-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="f9181-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="f9181-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="f9181-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="f9181-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="f9181-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="f9181-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="f9181-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="f9181-970">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="f9181-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-971">0,00</span><span class="sxs-lookup"><span data-stu-id="f9181-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="f9181-972">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-973">0,00</span><span class="sxs-lookup"><span data-stu-id="f9181-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-974">0,00</span><span class="sxs-lookup"><span data-stu-id="f9181-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-975">0,00</span><span class="sxs-lookup"><span data-stu-id="f9181-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-976">0,00</span><span class="sxs-lookup"><span data-stu-id="f9181-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-977">0,00</span><span class="sxs-lookup"><span data-stu-id="f9181-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="f9181-978">776.36</span><span class="sxs-lookup"><span data-stu-id="f9181-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-979">223.64</span><span class="sxs-lookup"><span data-stu-id="f9181-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="f9181-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="f9181-981">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="f9181-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-982">000</span><span class="sxs-lookup"><span data-stu-id="f9181-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-983">0,00</span><span class="sxs-lookup"><span data-stu-id="f9181-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-984">0,00</span><span class="sxs-lookup"><span data-stu-id="f9181-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-985">0,00</span><span class="sxs-lookup"><span data-stu-id="f9181-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-986">0,00</span><span class="sxs-lookup"><span data-stu-id="f9181-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-987">30,00</span><span class="sxs-lookup"><span data-stu-id="f9181-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-988">10,00</span><span class="sxs-lookup"><span data-stu-id="f9181-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="f9181-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="f9181-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="f9181-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="f9181-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="f9181-992">Þetta efnisatriði sýnir hvernig fyrir aðalkostnaðareiningin 10001 Rafmagn flæðir í gegnum kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="f9181-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="f9181-993">Þar af leiðandi er þessum sameiginlega kostnaði úthlutað á lægsta stigið í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="f9181-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="f9181-994">Með öðrum orðum bera kostnaðarhlutir á lægsta stiginu kostnaðinn.</span><span class="sxs-lookup"><span data-stu-id="f9181-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="f9181-995">Ef þú þarft sjónrænt flæði kostnaðar á milli kostnaðarhluta er hægt að nota stefnureglur samantekins kostnaðar til að gera kostnaðarflæðið sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="f9181-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="f9181-996">Fyrir frekari upplýsingar skal sjá [Stefna fyrir samantekt kostnaðar og útreikning sameiginlegs kostnaðar](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="f9181-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]