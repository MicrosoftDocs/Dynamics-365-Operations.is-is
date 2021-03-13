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
ms.openlocfilehash: d60248f2bd6774b2e9afdb3632b6eb31d67349ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5009519"
---
# <a name="overhead-calculation"></a><span data-ttu-id="27464-103">Útreikningur fastakostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27464-104">Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði.</span><span class="sxs-lookup"><span data-stu-id="27464-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="27464-105">Skýrsluskilgreining</span><span class="sxs-lookup"><span data-stu-id="27464-105">Term definition</span></span>
---------------

<span data-ttu-id="27464-106">Stjórnunarkostnaður er sá kostnaður sem stofnað er til fyrir rekstur fyrirtækis, en sem ekki er hægt að rekja beint til neinna sérstakrar starfsemi, vöru eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="27464-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="27464-107">Stjórnunarkostnaður veitir mikilvægan stuðning við myndun hagnaðarmyndandi verkþátta.</span><span class="sxs-lookup"><span data-stu-id="27464-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="27464-108">Hér eru nokkur dæmi um skilyrði:</span><span class="sxs-lookup"><span data-stu-id="27464-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="27464-109">Leiga</span><span class="sxs-lookup"><span data-stu-id="27464-109">Rent</span></span>
-   <span data-ttu-id="27464-110">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-110">Electricity</span></span>
-   <span data-ttu-id="27464-111">Stjórnunarkostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="27464-112">Yfirlit yfir útreikning fastakostnaðar</span><span class="sxs-lookup"><span data-stu-id="27464-112">Overhead calculation overview</span></span>
<span data-ttu-id="27464-113">Útreikningur fastakostnaðar keyrir reglur kostnaðarbókhalds í réttri röð.</span><span class="sxs-lookup"><span data-stu-id="27464-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="27464-114">Hægt er að keyra útreikning fastakostnaðar margsinnis fyrir sama fjárhagstímabil ef reglum kostnaðarbókhalds hefur verið breytt eða ákveðnar villur hafa fundist.</span><span class="sxs-lookup"><span data-stu-id="27464-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="27464-115">Hver keyrsla á útreikningi fastakostnaðar er geymd og fær einkvæmt útgáfukenni sem gerir kleift að bera saman útreikning í mismunandi útgáfum.</span><span class="sxs-lookup"><span data-stu-id="27464-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="27464-116">Kostnaðarfærslur sem útreikningur fastakostnaðar mynda fá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="27464-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="27464-117">Dagsetningin bókhald samsvarar lokadagsetning fjárhagstímabilsins sem er dagsetning reikningsskiladagsetning reikningsskila notað í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="27464-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="27464-118">Einkvæmt útgáfukenni samanstendur af eftirfarandi þáttum:</span><span class="sxs-lookup"><span data-stu-id="27464-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="27464-119">Gerð útgáfu</span><span class="sxs-lookup"><span data-stu-id="27464-119">Version type</span></span>
-   <span data-ttu-id="27464-120">Dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="27464-120">Date and time</span></span>
-   <span data-ttu-id="27464-121">Fjárhagur kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="27464-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="27464-122">Fjárhagsár</span><span class="sxs-lookup"><span data-stu-id="27464-122">Fiscal year</span></span>
-   <span data-ttu-id="27464-123">Reikningstímabil</span><span class="sxs-lookup"><span data-stu-id="27464-123">Fiscal period</span></span>

<span data-ttu-id="27464-124">Útreikningur fastakostnaðar er keyrður óháð því hver útgáfan er.</span><span class="sxs-lookup"><span data-stu-id="27464-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="27464-125">Þess vegna er hægt að reikna út áætlaða útgáfu á undan raunútgáfu.</span><span class="sxs-lookup"><span data-stu-id="27464-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="27464-126">Útreikningur fastakostnaðar samanstendur af fjórum skrefum, eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="27464-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="27464-127">Í hverju skrefi er færslubókarhaus stofnaður með bókarfærslum.</span><span class="sxs-lookup"><span data-stu-id="27464-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="27464-128">Þessi færslubókarhaus geymir inntaksgögn fyrir hvert útreikningsþrep.</span><span class="sxs-lookup"><span data-stu-id="27464-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="27464-129">Stefnur og reglur eru notaðar í hverri færslulínu og kostnaðarfærslur eru myndaðar sem úttak.</span><span class="sxs-lookup"><span data-stu-id="27464-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="27464-130">Þess vegna hefurðu ávallt fullan rekjanleika.</span><span class="sxs-lookup"><span data-stu-id="27464-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="27464-131">[![Útreikningur fastakostnaðar](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="27464-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="27464-132">Reikna og úthluta sameiginlegur kostnaði vegna rafmagns</span><span class="sxs-lookup"><span data-stu-id="27464-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="27464-133">Í Fjárhagsbókhaldi er ákveðinn kostnaður, eins og rafmagn, skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="27464-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="27464-134">Þar af leiðandi er nákvæmar innsýn rekstrarfélags ekki veitt fyrir kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="27464-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="27464-135">Í kostnaðarbókhaldi verður kostnaður að flæða í gegnum fyrirtækiseiningar til að veita rétta innsýn rekstrarfélags þvert á allar fyrirtækiseiningar og stig.</span><span class="sxs-lookup"><span data-stu-id="27464-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="27464-136">Þetta flæði verður að byggja á annaðhvort nákvæmri færslu notkunar eða sanngjarnri matsreglu.</span><span class="sxs-lookup"><span data-stu-id="27464-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="27464-137">Í fjárhagnum er hægt að bóka rafmagnskostnað eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="27464-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="27464-138">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="27464-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="27464-139">Kostnaðarstaður</span><span class="sxs-lookup"><span data-stu-id="27464-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="27464-140">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="27464-140">Main account</span></span></th>
<th><span data-ttu-id="27464-141">Upphæð í bókhaldsgjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="27464-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-142">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="27464-143">CC099</span><span class="sxs-lookup"><span data-stu-id="27464-143">CC099</span></span></td>
<td><span data-ttu-id="27464-144">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="27464-144">Default cost center</span></span></td>
<td><span data-ttu-id="27464-145">10001</span><span class="sxs-lookup"><span data-stu-id="27464-145">10001</span></span></td>
<td><span data-ttu-id="27464-146">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-146">Electricity</span></span></td>
<td><span data-ttu-id="27464-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="27464-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="27464-148">Skref 1: Keyra útreikning kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="27464-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="27464-149">Sjálfvirkt er að þegar kostnaðarfærslur eru fluttar úr grunngögnum fái þær flokkun kostnaðarhegðunar **Óflokkað** í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="27464-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="27464-150">Með því að nota stefnureglur kostnaðarhegðunar er hægt að endurflokka kostnaðarfærslur sem annaðhvort **Fastan kostnað** eða **Breytilegan kostnað**.</span><span class="sxs-lookup"><span data-stu-id="27464-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="27464-151">Tilgreinið reglu kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="27464-151">Define the cost behavior rule</span></span>

<span data-ttu-id="27464-152">Í sumum tilfellum er hluti af kostnaði föst þóknun og eftirstandandi kostnaður byggist á notkun.</span><span class="sxs-lookup"><span data-stu-id="27464-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="27464-153">Rafmagnsreikningar stemma oft við þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="27464-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="27464-154">Þegar tiltekin föst þóknun hefur verið greidd, er greitt fyrir notkun á kílóvattklukkustund (Kwh).</span><span class="sxs-lookup"><span data-stu-id="27464-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="27464-155">Til dæmis ef föst kostnaðarþóknun er 1000.00 sýnir þetta hvernig regla kostnaðarhegðunar er skilgreind:</span><span class="sxs-lookup"><span data-stu-id="27464-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="27464-156">Föst upphæð 1.000,00</span><span class="sxs-lookup"><span data-stu-id="27464-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="27464-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="27464-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="27464-158">1000.01 &lt; N = Breyta</span><span class="sxs-lookup"><span data-stu-id="27464-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="27464-159">Færslubók</span><span class="sxs-lookup"><span data-stu-id="27464-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="27464-160">Færslubók</span><span class="sxs-lookup"><span data-stu-id="27464-160">Journal</span></span></th>
<th><span data-ttu-id="27464-161">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="27464-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="27464-162">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="27464-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="27464-163">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="27464-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-164">00001</span><span class="sxs-lookup"><span data-stu-id="27464-164">00001</span></span></td>
<td><span data-ttu-id="27464-165">Færslubók útreiknings fyrir kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="27464-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="27464-166">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="27464-166">Fiscal</span></span></td>
<td><span data-ttu-id="27464-167">2017</span><span class="sxs-lookup"><span data-stu-id="27464-167">2017</span></span></td>
<td><span data-ttu-id="27464-168">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="27464-168">Period 1</span></span></td>
<td><span data-ttu-id="27464-169">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="27464-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="27464-170">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="27464-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="27464-171">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="27464-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="27464-172">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="27464-173">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="27464-173">Cost element</span></span></th>
<th><span data-ttu-id="27464-174">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="27464-174">Cost behavior</span></span></th>
<th><span data-ttu-id="27464-175">Upphæð</span><span class="sxs-lookup"><span data-stu-id="27464-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-176">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="27464-177">CC099</span><span class="sxs-lookup"><span data-stu-id="27464-177">CC099</span></span></td>
<td><span data-ttu-id="27464-178">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="27464-178">Default cost center</span></span></td>
<td><span data-ttu-id="27464-179">10001</span><span class="sxs-lookup"><span data-stu-id="27464-179">10001</span></span></td>
<td><span data-ttu-id="27464-180">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-180">Electricity</span></span></td>
<td><span data-ttu-id="27464-181">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="27464-181">Unclassified</span></span></td>
<td><span data-ttu-id="27464-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="27464-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="27464-183">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="27464-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="27464-184">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="27464-185">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="27464-185">Cost element</span></span></th>
<th><span data-ttu-id="27464-186">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="27464-186">Cost behavior</span></span></th>
<th><span data-ttu-id="27464-187">Upphæð</span><span class="sxs-lookup"><span data-stu-id="27464-187">Amount</span></span></th>
<th><span data-ttu-id="27464-188">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="27464-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-189">CC099</span><span class="sxs-lookup"><span data-stu-id="27464-189">CC099</span></span></td>
<td><span data-ttu-id="27464-190">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="27464-190">Default cost center</span></span></td>
<td><span data-ttu-id="27464-191">10001</span><span class="sxs-lookup"><span data-stu-id="27464-191">10001</span></span></td>
<td><span data-ttu-id="27464-192">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-192">Electricity</span></span></td>
<td><span data-ttu-id="27464-193">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="27464-193">Unclassified</span></span></td>
<td><span data-ttu-id="27464-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="27464-194">10,000.00</span></span></td>
<td><span data-ttu-id="27464-195">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-196">CC099</span><span class="sxs-lookup"><span data-stu-id="27464-196">CC099</span></span></td>
<td><span data-ttu-id="27464-197">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="27464-197">Default cost center</span></span></td>
<td><span data-ttu-id="27464-198">10001</span><span class="sxs-lookup"><span data-stu-id="27464-198">10001</span></span></td>
<td><span data-ttu-id="27464-199">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-199">Electricity</span></span></td>
<td><span data-ttu-id="27464-200">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="27464-200">Unclassified</span></span></td>
<td><span data-ttu-id="27464-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="27464-201">-10,000.00</span></span></td>
<td><span data-ttu-id="27464-202">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-203">CC099</span><span class="sxs-lookup"><span data-stu-id="27464-203">CC099</span></span></td>
<td><span data-ttu-id="27464-204">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="27464-204">Default cost center</span></span></td>
<td><span data-ttu-id="27464-205">10001</span><span class="sxs-lookup"><span data-stu-id="27464-205">10001</span></span></td>
<td><span data-ttu-id="27464-206">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-206">Electricity</span></span></td>
<td><span data-ttu-id="27464-207">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-207">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="27464-208">1,000.00</span></span></td>
<td><span data-ttu-id="27464-209">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-210">CC099</span><span class="sxs-lookup"><span data-stu-id="27464-210">CC099</span></span></td>
<td><span data-ttu-id="27464-211">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="27464-211">Default cost center</span></span></td>
<td><span data-ttu-id="27464-212">10001</span><span class="sxs-lookup"><span data-stu-id="27464-212">10001</span></span></td>
<td><span data-ttu-id="27464-213">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-213">Electricity</span></span></td>
<td><span data-ttu-id="27464-214">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-214">Variable cost</span></span></td>
<td><span data-ttu-id="27464-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="27464-215">9,000.00</span></span></td>
<td><span data-ttu-id="27464-216">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="27464-217">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðarhegðunarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="27464-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="27464-218">Skref 2: Keyra útreikning kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="27464-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="27464-219">Kostnaðardreifing er notuð til að endurúthluta kostnaði frá einum kostnaðarhlut til annars eða fleiri kostnaðarhluta með því að nota viðeigandi úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="27464-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="27464-220">Kostnaðardreifing og kostnaðarúthlutun eru ólíkar að því leyti að kostnaðardreifing kemur alltaf upp á stigi aðalkostnaðareiningar upphaflegs verðs.</span><span class="sxs-lookup"><span data-stu-id="27464-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="27464-221">Tilgreinið kostnaðardreifingarreglu</span><span class="sxs-lookup"><span data-stu-id="27464-221">Define the cost distribution rule</span></span>

<span data-ttu-id="27464-222">Í Fjárhagsbókhaldi er rafmagnskostnaður oft skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="27464-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="27464-223">Í kostnaðarbókhaldi er þessi nálgun ekki nógu nákvæm.</span><span class="sxs-lookup"><span data-stu-id="27464-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="27464-224">Breytilegur kostnaði þarf að dreifa á staka kostnaðarhluti á sanngjörnum grunni.</span><span class="sxs-lookup"><span data-stu-id="27464-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="27464-225">Rökréttasti úthlutunargrunnurinn er notkun á rafmagni (Kwh).</span><span class="sxs-lookup"><span data-stu-id="27464-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="27464-226">Stofnað er tölfræðilegt víddarstak sem er nefnt Rafmagn og rafmagnsnotkun er skráð.</span><span class="sxs-lookup"><span data-stu-id="27464-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="27464-227">Sjálfgefið er að öll tölfræðileg víddarstök verða tiltæk sem úthlutunargrunnur.</span><span class="sxs-lookup"><span data-stu-id="27464-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="27464-228">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-228">Cost object</span></span></th>
<th><span data-ttu-id="27464-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="27464-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-230">CC001</span><span class="sxs-lookup"><span data-stu-id="27464-230">CC001</span></span></td>
<td><span data-ttu-id="27464-231">Mannauður</span><span class="sxs-lookup"><span data-stu-id="27464-231">HR</span></span></td>
<td><span data-ttu-id="27464-232">1.000</span><span class="sxs-lookup"><span data-stu-id="27464-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-233">CC002</span><span class="sxs-lookup"><span data-stu-id="27464-233">CC002</span></span></td>
<td><span data-ttu-id="27464-234">Fjármál</span><span class="sxs-lookup"><span data-stu-id="27464-234">Finance</span></span></td>
<td><span data-ttu-id="27464-235">6,000</span><span class="sxs-lookup"><span data-stu-id="27464-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-236">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-236">CC003</span></span></td>
<td><span data-ttu-id="27464-237">Smölun</span><span class="sxs-lookup"><span data-stu-id="27464-237">Assembly</span></span></td>
<td><span data-ttu-id="27464-238">0</span><span class="sxs-lookup"><span data-stu-id="27464-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="27464-239">Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunni fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="27464-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="27464-240">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-240">Cost object</span></span></th>
<th><span data-ttu-id="27464-241">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="27464-241">Magnitude</span></span></th>
<th><span data-ttu-id="27464-242">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="27464-242">Allocation factor</span></span></th>
<th><span data-ttu-id="27464-243">Upphæð</span><span class="sxs-lookup"><span data-stu-id="27464-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-244">CC001</span><span class="sxs-lookup"><span data-stu-id="27464-244">CC001</span></span></td>
<td><span data-ttu-id="27464-245">Mannauður</span><span class="sxs-lookup"><span data-stu-id="27464-245">HR</span></span></td>
<td><span data-ttu-id="27464-246">1.000</span><span class="sxs-lookup"><span data-stu-id="27464-246">1,000</span></span></td>
<td><span data-ttu-id="27464-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="27464-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="27464-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="27464-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-249">CC002</span><span class="sxs-lookup"><span data-stu-id="27464-249">CC002</span></span></td>
<td><span data-ttu-id="27464-250">Fjármál</span><span class="sxs-lookup"><span data-stu-id="27464-250">Finance</span></span></td>
<td><span data-ttu-id="27464-251">6,000</span><span class="sxs-lookup"><span data-stu-id="27464-251">6,000</span></span></td>
<td><span data-ttu-id="27464-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="27464-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="27464-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="27464-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-254">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-254">CC003</span></span></td>
<td><span data-ttu-id="27464-255">Smölun</span><span class="sxs-lookup"><span data-stu-id="27464-255">Assembly</span></span></td>
<td><span data-ttu-id="27464-256">0</span><span class="sxs-lookup"><span data-stu-id="27464-256">0</span></span></td>
<td><span data-ttu-id="27464-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="27464-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="27464-258">0,00</span><span class="sxs-lookup"><span data-stu-id="27464-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="27464-259">Föstum kostnaði þarf að dreifa jafnt á staka kostnaðarhluti sem hafa notað rafmagn.</span><span class="sxs-lookup"><span data-stu-id="27464-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="27464-260">Hægt er að ná þessa niðurstöðu með því að nota tölfræðilegt víddarstakið Rafmagn í úthlutunargrunni reikniformúlu: (Rafmagn &gt; 0,00) Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunn fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="27464-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="27464-261">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-261">Cost object</span></span></th>
<th><span data-ttu-id="27464-262">Formúla</span><span class="sxs-lookup"><span data-stu-id="27464-262">Formula</span></span></th>
<th><span data-ttu-id="27464-263">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="27464-263">Magnitude</span></span></th>
<th><span data-ttu-id="27464-264">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="27464-264">Allocation factor</span></span></th>
<th><span data-ttu-id="27464-265">Upphæð</span><span class="sxs-lookup"><span data-stu-id="27464-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-266">CC001</span><span class="sxs-lookup"><span data-stu-id="27464-266">CC001</span></span></td>
<td><span data-ttu-id="27464-267">Mannauður</span><span class="sxs-lookup"><span data-stu-id="27464-267">HR</span></span></td>
<td><span data-ttu-id="27464-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="27464-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="27464-269">1</span><span class="sxs-lookup"><span data-stu-id="27464-269">1</span></span></td>
<td><span data-ttu-id="27464-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="27464-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="27464-271">500,00</span><span class="sxs-lookup"><span data-stu-id="27464-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-272">CC002</span><span class="sxs-lookup"><span data-stu-id="27464-272">CC002</span></span></td>
<td><span data-ttu-id="27464-273">Fjármál</span><span class="sxs-lookup"><span data-stu-id="27464-273">Finance</span></span></td>
<td><span data-ttu-id="27464-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="27464-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="27464-275">1</span><span class="sxs-lookup"><span data-stu-id="27464-275">1</span></span></td>
<td><span data-ttu-id="27464-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="27464-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="27464-277">500,00</span><span class="sxs-lookup"><span data-stu-id="27464-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-278">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-278">CC003</span></span></td>
<td><span data-ttu-id="27464-279">Smölun</span><span class="sxs-lookup"><span data-stu-id="27464-279">Assembly</span></span></td>
<td><span data-ttu-id="27464-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="27464-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="27464-281">0</span><span class="sxs-lookup"><span data-stu-id="27464-281">0</span></span></td>
<td><span data-ttu-id="27464-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="27464-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="27464-283">0,00</span><span class="sxs-lookup"><span data-stu-id="27464-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="27464-284">Færslubók</span><span class="sxs-lookup"><span data-stu-id="27464-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="27464-285">Færslubók</span><span class="sxs-lookup"><span data-stu-id="27464-285">Journal</span></span></th>
<th><span data-ttu-id="27464-286">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="27464-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="27464-287">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="27464-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="27464-288">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="27464-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-289">00002</span><span class="sxs-lookup"><span data-stu-id="27464-289">00002</span></span></td>
<td><span data-ttu-id="27464-290">Útreikningabók kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="27464-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="27464-291">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="27464-291">Fiscal</span></span></td>
<td><span data-ttu-id="27464-292">2017</span><span class="sxs-lookup"><span data-stu-id="27464-292">2017</span></span></td>
<td><span data-ttu-id="27464-293">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="27464-293">Period 1</span></span></td>
<td><span data-ttu-id="27464-294">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="27464-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="27464-295">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="27464-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="27464-296">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="27464-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="27464-297">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="27464-298">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="27464-298">Cost element</span></span></th>
<th><span data-ttu-id="27464-299">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="27464-299">Cost behavior</span></span></th>
<th><span data-ttu-id="27464-300">Upphæð</span><span class="sxs-lookup"><span data-stu-id="27464-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-301">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="27464-302">CC099</span><span class="sxs-lookup"><span data-stu-id="27464-302">CC099</span></span></td>
<td><span data-ttu-id="27464-303">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="27464-303">Default cost center</span></span></td>
<td><span data-ttu-id="27464-304">10001</span><span class="sxs-lookup"><span data-stu-id="27464-304">10001</span></span></td>
<td><span data-ttu-id="27464-305">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-305">Electricity</span></span></td>
<td><span data-ttu-id="27464-306">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-306">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="27464-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-308">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="27464-309">CC099</span><span class="sxs-lookup"><span data-stu-id="27464-309">CC099</span></span></td>
<td><span data-ttu-id="27464-310">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="27464-310">Default cost center</span></span></td>
<td><span data-ttu-id="27464-311">10001</span><span class="sxs-lookup"><span data-stu-id="27464-311">10001</span></span></td>
<td><span data-ttu-id="27464-312">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-312">Electricity</span></span></td>
<td><span data-ttu-id="27464-313">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-313">Variable cost</span></span></td>
<td><span data-ttu-id="27464-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="27464-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="27464-315">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="27464-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="27464-316">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="27464-317">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="27464-317">Cost element</span></span></th>
<th><span data-ttu-id="27464-318">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="27464-318">Cost behavior</span></span></th>
<th><span data-ttu-id="27464-319">Upphæð</span><span class="sxs-lookup"><span data-stu-id="27464-319">Amount</span></span></th>
<th><span data-ttu-id="27464-320">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="27464-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-321">CC099</span><span class="sxs-lookup"><span data-stu-id="27464-321">CC099</span></span></td>
<td><span data-ttu-id="27464-322">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="27464-322">Default cost center</span></span></td>
<td><span data-ttu-id="27464-323">10001</span><span class="sxs-lookup"><span data-stu-id="27464-323">10001</span></span></td>
<td><span data-ttu-id="27464-324">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-324">Electricity</span></span></td>
<td><span data-ttu-id="27464-325">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-325">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="27464-326">-1,000.00</span></span></td>
<td><span data-ttu-id="27464-327">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-328">CC001</span><span class="sxs-lookup"><span data-stu-id="27464-328">CC001</span></span></td>
<td><span data-ttu-id="27464-329">Mannauður</span><span class="sxs-lookup"><span data-stu-id="27464-329">HR</span></span></td>
<td><span data-ttu-id="27464-330">10001</span><span class="sxs-lookup"><span data-stu-id="27464-330">10001</span></span></td>
<td><span data-ttu-id="27464-331">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-331">Electricity</span></span></td>
<td><span data-ttu-id="27464-332">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-332">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-333">500,00</span><span class="sxs-lookup"><span data-stu-id="27464-333">500.00</span></span></td>
<td><span data-ttu-id="27464-334">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-335">CC002</span><span class="sxs-lookup"><span data-stu-id="27464-335">CC002</span></span></td>
<td><span data-ttu-id="27464-336">Fjármál</span><span class="sxs-lookup"><span data-stu-id="27464-336">Finance</span></span></td>
<td><span data-ttu-id="27464-337">10001</span><span class="sxs-lookup"><span data-stu-id="27464-337">10001</span></span></td>
<td><span data-ttu-id="27464-338">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-338">Electricity</span></span></td>
<td><span data-ttu-id="27464-339">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-339">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-340">500,00</span><span class="sxs-lookup"><span data-stu-id="27464-340">500.00</span></span></td>
<td><span data-ttu-id="27464-341">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-342">CC099</span><span class="sxs-lookup"><span data-stu-id="27464-342">CC099</span></span></td>
<td><span data-ttu-id="27464-343">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="27464-343">Default cost center</span></span></td>
<td><span data-ttu-id="27464-344">10001</span><span class="sxs-lookup"><span data-stu-id="27464-344">10001</span></span></td>
<td><span data-ttu-id="27464-345">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-345">Electricity</span></span></td>
<td><span data-ttu-id="27464-346">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-346">Variable cost</span></span></td>
<td><span data-ttu-id="27464-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="27464-347">-9,000.00</span></span></td>
<td><span data-ttu-id="27464-348">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-349">CC001</span><span class="sxs-lookup"><span data-stu-id="27464-349">CC001</span></span></td>
<td><span data-ttu-id="27464-350">Mannauður</span><span class="sxs-lookup"><span data-stu-id="27464-350">HR</span></span></td>
<td><span data-ttu-id="27464-351">10001</span><span class="sxs-lookup"><span data-stu-id="27464-351">10001</span></span></td>
<td><span data-ttu-id="27464-352">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-352">Electricity</span></span></td>
<td><span data-ttu-id="27464-353">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-353">Variable cost</span></span></td>
<td><span data-ttu-id="27464-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="27464-354">1,285.71</span></span></td>
<td><span data-ttu-id="27464-355">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-356">CC002</span><span class="sxs-lookup"><span data-stu-id="27464-356">CC002</span></span></td>
<td><span data-ttu-id="27464-357">Fjármál</span><span class="sxs-lookup"><span data-stu-id="27464-357">Finance</span></span></td>
<td><span data-ttu-id="27464-358">10001</span><span class="sxs-lookup"><span data-stu-id="27464-358">10001</span></span></td>
<td><span data-ttu-id="27464-359">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-359">Electricity</span></span></td>
<td><span data-ttu-id="27464-360">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-360">Variable cost</span></span></td>
<td><span data-ttu-id="27464-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="27464-361">7,714.29</span></span></td>
<td><span data-ttu-id="27464-362">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="27464-363">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðardreifingarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="27464-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="27464-364">Skref 3: Keyra útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="27464-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="27464-365">Sameiginlegur kostnaður er notaður til að rukka einn eða fleiri tilgreinda kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="27464-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="27464-366">Gjöldin byggjast á fyrirframákveðnu kostnaðarhlutfalli og mæligildi úr úthlutuðum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="27464-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="27464-367">Skilgreina sameiginlegan kostnað</span><span class="sxs-lookup"><span data-stu-id="27464-367">Define the overhead rate</span></span>

<span data-ttu-id="27464-368">Kostnaðarhlutur CC001 Mannauður stuðlar að safni innri verka.</span><span class="sxs-lookup"><span data-stu-id="27464-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="27464-369">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsverk til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="27464-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="27464-370">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-370">Cost object</span></span></th>
<th><span data-ttu-id="27464-371">Tímar</span><span class="sxs-lookup"><span data-stu-id="27464-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-372">Verk 1</span><span class="sxs-lookup"><span data-stu-id="27464-372">Proj 1</span></span></td>
<td><span data-ttu-id="27464-373">Verk 1</span><span class="sxs-lookup"><span data-stu-id="27464-373">Project 1</span></span></td>
<td><span data-ttu-id="27464-374">3</span><span class="sxs-lookup"><span data-stu-id="27464-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-375">Verk 2</span><span class="sxs-lookup"><span data-stu-id="27464-375">Proj 2</span></span></td>
<td><span data-ttu-id="27464-376">Verk 2</span><span class="sxs-lookup"><span data-stu-id="27464-376">Project 2</span></span></td>
<td><span data-ttu-id="27464-377">1</span><span class="sxs-lookup"><span data-stu-id="27464-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="27464-378">Fyrirframákveðið kostnaðarhlutfall fyrir kostnaðarframlag verk hefur verið skilgreint.</span><span class="sxs-lookup"><span data-stu-id="27464-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="27464-379">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-379">Cost object</span></span></th>
<th><span data-ttu-id="27464-380">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="27464-380">Cost element</span></span></th>
<th><span data-ttu-id="27464-381">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="27464-381">Cost behavior</span></span></th>
<th><span data-ttu-id="27464-382">Einingar</span><span class="sxs-lookup"><span data-stu-id="27464-382">Units</span></span></th>
<th><span data-ttu-id="27464-383">Taxti</span><span class="sxs-lookup"><span data-stu-id="27464-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-384">CC001</span><span class="sxs-lookup"><span data-stu-id="27464-384">CC001</span></span></td>
<td><span data-ttu-id="27464-385">Mannauður</span><span class="sxs-lookup"><span data-stu-id="27464-385">HR</span></span></td>
<td><span data-ttu-id="27464-386">10001</span><span class="sxs-lookup"><span data-stu-id="27464-386">10001</span></span></td>
<td><span data-ttu-id="27464-387">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-387">Variable cost</span></span></td>
<td><span data-ttu-id="27464-388">1</span><span class="sxs-lookup"><span data-stu-id="27464-388">1</span></span></td>
<td><span data-ttu-id="27464-389">10</span><span class="sxs-lookup"><span data-stu-id="27464-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="27464-390">Eftirfarandi tafla sýnir niðurstöður þegar Mannauðsverk eru notuð sem grunnur við úthlutun.</span><span class="sxs-lookup"><span data-stu-id="27464-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="27464-391">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-391">Cost object</span></span></th>
<th><span data-ttu-id="27464-392">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="27464-392">Magnitude</span></span></th>
<th><span data-ttu-id="27464-393">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="27464-393">Cost element</span></span></th>
<th><span data-ttu-id="27464-394">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="27464-394">Allocation factor</span></span></th>
<th><span data-ttu-id="27464-395">Upphæð</span><span class="sxs-lookup"><span data-stu-id="27464-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-396">Verk 1</span><span class="sxs-lookup"><span data-stu-id="27464-396">Proj 1</span></span></td>
<td><span data-ttu-id="27464-397">Verk 1</span><span class="sxs-lookup"><span data-stu-id="27464-397">Project 1</span></span></td>
<td><span data-ttu-id="27464-398">3</span><span class="sxs-lookup"><span data-stu-id="27464-398">3</span></span></td>
<td><span data-ttu-id="27464-399">10001</span><span class="sxs-lookup"><span data-stu-id="27464-399">10001</span></span></td>
<td><span data-ttu-id="27464-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="27464-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="27464-401">30,00</span><span class="sxs-lookup"><span data-stu-id="27464-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-402">Verk 2</span><span class="sxs-lookup"><span data-stu-id="27464-402">Proj 2</span></span></td>
<td><span data-ttu-id="27464-403">Verk 2</span><span class="sxs-lookup"><span data-stu-id="27464-403">Project 2</span></span></td>
<td><span data-ttu-id="27464-404">1</span><span class="sxs-lookup"><span data-stu-id="27464-404">1</span></span></td>
<td><span data-ttu-id="27464-405">10001</span><span class="sxs-lookup"><span data-stu-id="27464-405">10001</span></span></td>
<td><span data-ttu-id="27464-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="27464-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="27464-407">10,00</span><span class="sxs-lookup"><span data-stu-id="27464-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="27464-408">Færslubók</span><span class="sxs-lookup"><span data-stu-id="27464-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="27464-409">Færslubók</span><span class="sxs-lookup"><span data-stu-id="27464-409">Journal</span></span></th>
<th><span data-ttu-id="27464-410">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="27464-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="27464-411">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="27464-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="27464-412">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="27464-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-413">00003</span><span class="sxs-lookup"><span data-stu-id="27464-413">00003</span></span></td>
<td><span data-ttu-id="27464-414">Færslubók fyrir útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="27464-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="27464-415">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="27464-415">Fiscal</span></span></td>
<td><span data-ttu-id="27464-416">2017</span><span class="sxs-lookup"><span data-stu-id="27464-416">2017</span></span></td>
<td><span data-ttu-id="27464-417">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="27464-417">Period 1</span></span></td>
<td><span data-ttu-id="27464-418">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="27464-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="27464-419">Bókarfærslur (Bókarfærslur fyrir útreikning sameiginlegs kostnaðar)</span><span class="sxs-lookup"><span data-stu-id="27464-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="27464-420">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="27464-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="27464-421">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-421">Cost object</span></span></th>
<th><span data-ttu-id="27464-422">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="27464-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-423">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="27464-424">Verk 1</span><span class="sxs-lookup"><span data-stu-id="27464-424">Proj 1</span></span></td>
<td><span data-ttu-id="27464-425">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="27464-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="27464-426">3,00</span><span class="sxs-lookup"><span data-stu-id="27464-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-427">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="27464-428">Verk 2</span><span class="sxs-lookup"><span data-stu-id="27464-428">Proj 2</span></span></td>
<td><span data-ttu-id="27464-429">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="27464-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="27464-430">1,00</span><span class="sxs-lookup"><span data-stu-id="27464-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="27464-431">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="27464-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="27464-432">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="27464-433">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="27464-433">Cost element</span></span></th>
<th><span data-ttu-id="27464-434">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="27464-434">Cost behavior</span></span></th>
<th><span data-ttu-id="27464-435">Upphæð</span><span class="sxs-lookup"><span data-stu-id="27464-435">Amount</span></span></th>
<th><span data-ttu-id="27464-436">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="27464-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="27464-437">CC0001</span></span></td>
<td><span data-ttu-id="27464-438">Mannauður</span><span class="sxs-lookup"><span data-stu-id="27464-438">HR</span></span></td>
<td><span data-ttu-id="27464-439">10001</span><span class="sxs-lookup"><span data-stu-id="27464-439">10001</span></span></td>
<td><span data-ttu-id="27464-440">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-440">Electricity</span></span></td>
<td><span data-ttu-id="27464-441">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-441">Variable cost</span></span></td>
<td><span data-ttu-id="27464-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="27464-442">-30.00</span></span></td>
<td><span data-ttu-id="27464-443">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-444">Verk 1</span><span class="sxs-lookup"><span data-stu-id="27464-444">Proj 1</span></span></td>
<td><span data-ttu-id="27464-445">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="27464-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="27464-446">10001</span><span class="sxs-lookup"><span data-stu-id="27464-446">10001</span></span></td>
<td><span data-ttu-id="27464-447">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-447">Electricity</span></span></td>
<td><span data-ttu-id="27464-448">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-448">Variable cost</span></span></td>
<td><span data-ttu-id="27464-449">30,00</span><span class="sxs-lookup"><span data-stu-id="27464-449">30.00</span></span></td>
<td><span data-ttu-id="27464-450">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-451">CC001</span><span class="sxs-lookup"><span data-stu-id="27464-451">CC001</span></span></td>
<td><span data-ttu-id="27464-452">Mannauður</span><span class="sxs-lookup"><span data-stu-id="27464-452">HR</span></span></td>
<td><span data-ttu-id="27464-453">10001</span><span class="sxs-lookup"><span data-stu-id="27464-453">10001</span></span></td>
<td><span data-ttu-id="27464-454">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-454">Electricity</span></span></td>
<td><span data-ttu-id="27464-455">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-455">Variable cost</span></span></td>
<td><span data-ttu-id="27464-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="27464-456">-10.00</span></span></td>
<td><span data-ttu-id="27464-457">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-458">Verk 2</span><span class="sxs-lookup"><span data-stu-id="27464-458">Proj 2</span></span></td>
<td><span data-ttu-id="27464-459">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="27464-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="27464-460">10001</span><span class="sxs-lookup"><span data-stu-id="27464-460">10001</span></span></td>
<td><span data-ttu-id="27464-461">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-461">Electricity</span></span></td>
<td><span data-ttu-id="27464-462">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-462">Variable cost</span></span></td>
<td><span data-ttu-id="27464-463">10,00</span><span class="sxs-lookup"><span data-stu-id="27464-463">10.00</span></span></td>
<td><span data-ttu-id="27464-464">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="27464-465">Nánari upplýsingar er að finna í [Framkvæma útreikning fastakostnaðar](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="27464-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="27464-466">Skref 4: Keyra útreikning kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="27464-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="27464-467">Úthlutun er notuð til að úthluta stöðu kostnaðarhlutar í öðrum kostnaðarhlutum með því að nota úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="27464-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="27464-468">Finance styður gagnvirka úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="27464-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="27464-469">Í gagnvirkri úthlutunaraðferð er sú sameiginlega þjónusta sem hjálparkostnaðarhlutir skiptast á viðurkennd að fullu.</span><span class="sxs-lookup"><span data-stu-id="27464-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="27464-470">Kerfið ákvarðar sjálfkrafa rétta röð til að framkvæma úthlutun eftir.</span><span class="sxs-lookup"><span data-stu-id="27464-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="27464-471">Stöðu kostnaðarhluta er úthlutað með einum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="27464-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="27464-472">Úthlutanir þvert á víddir kostnaðarhluta og viðkomandi stök þeirra eru studdar.</span><span class="sxs-lookup"><span data-stu-id="27464-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="27464-473">Úthlutun pöntunarinnar er stjórnað af stýrieiningu kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="27464-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="27464-474">[![Gagnkvæm aðferð](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="27464-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="27464-475">Tilgreinið kostnaðarúthlutun</span><span class="sxs-lookup"><span data-stu-id="27464-475">Define the cost allocation</span></span>

<span data-ttu-id="27464-476">Hér er einfalt dæmi sem útskýrir hvernig hægt er að rekja flæði kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="27464-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="27464-477">Kostnaðarhlutir CC001 Mannauður leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="27464-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="27464-478">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="27464-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="27464-479">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-479">Cost object</span></span></th>
<th><span data-ttu-id="27464-480">Mannauðsþjónusta</span><span class="sxs-lookup"><span data-stu-id="27464-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-481">CC002</span><span class="sxs-lookup"><span data-stu-id="27464-481">CC002</span></span></td>
<td><span data-ttu-id="27464-482">Fjármál</span><span class="sxs-lookup"><span data-stu-id="27464-482">Finance</span></span></td>
<td><span data-ttu-id="27464-483">35</span><span class="sxs-lookup"><span data-stu-id="27464-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-484">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-484">CC003</span></span></td>
<td><span data-ttu-id="27464-485">Smölun</span><span class="sxs-lookup"><span data-stu-id="27464-485">Assembly</span></span></td>
<td><span data-ttu-id="27464-486">55</span><span class="sxs-lookup"><span data-stu-id="27464-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-487">CC004</span><span class="sxs-lookup"><span data-stu-id="27464-487">CC004</span></span></td>
<td><span data-ttu-id="27464-488">Pakkning</span><span class="sxs-lookup"><span data-stu-id="27464-488">Packaging</span></span></td>
<td><span data-ttu-id="27464-489">10</span><span class="sxs-lookup"><span data-stu-id="27464-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="27464-490">Kostnaðarhlutir CC002 Fjármál leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="27464-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="27464-491">Stofnað er tölfræðilegt víddarstak sem kallast Fjármálaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="27464-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="27464-492">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-492">Cost object</span></span></th>
<th><span data-ttu-id="27464-493">Fjármálaþjónusta</span><span class="sxs-lookup"><span data-stu-id="27464-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-494">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-494">CC003</span></span></td>
<td><span data-ttu-id="27464-495">Smölun</span><span class="sxs-lookup"><span data-stu-id="27464-495">Assembly</span></span></td>
<td><span data-ttu-id="27464-496">65</span><span class="sxs-lookup"><span data-stu-id="27464-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-497">CC004</span><span class="sxs-lookup"><span data-stu-id="27464-497">CC004</span></span></td>
<td><span data-ttu-id="27464-498">Pakkning</span><span class="sxs-lookup"><span data-stu-id="27464-498">Packaging</span></span></td>
<td><span data-ttu-id="27464-499">35</span><span class="sxs-lookup"><span data-stu-id="27464-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="27464-500">Kostnaðarhlutir CC003 Samsetning leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="27464-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="27464-501">Meðlimur tölfræðilega víddar sem kallast Mannauður verk er stofnað til að mælvíddarstaka notuðum magnitude.</span><span class="sxs-lookup"><span data-stu-id="27464-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="27464-502">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-502">Cost object</span></span></th>
<th><span data-ttu-id="27464-503">Samsetningarþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="27464-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-504">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-504">Prod 1</span></span></td>
<td><span data-ttu-id="27464-505">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-505">Product 1</span></span></td>
<td><span data-ttu-id="27464-506">60</span><span class="sxs-lookup"><span data-stu-id="27464-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-507">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-507">Prod 2</span></span></td>
<td><span data-ttu-id="27464-508">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-508">Product 2</span></span></td>
<td><span data-ttu-id="27464-509">20</span><span class="sxs-lookup"><span data-stu-id="27464-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="27464-510">Kostnaðarhlutir CC004 Umbúðir leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="27464-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="27464-511">Stofnað er tölfræðilegt víddarstak sem kallast Umbúðaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="27464-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="27464-512">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-512">Cost object</span></span></th>
<th><span data-ttu-id="27464-513">Umbúðaþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="27464-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-514">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-514">Prod 1</span></span></td>
<td><span data-ttu-id="27464-515">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-515">Product 1</span></span></td>
<td><span data-ttu-id="27464-516">80</span><span class="sxs-lookup"><span data-stu-id="27464-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-517">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-517">Prod 2</span></span></td>
<td><span data-ttu-id="27464-518">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-518">Product 2</span></span></td>
<td><span data-ttu-id="27464-519">15</span><span class="sxs-lookup"><span data-stu-id="27464-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="27464-520">Hægt er að afleiða tölfræðiaðgerðir eins og framleiðslutíma sem vara notar frá upprunagögnum.</span><span class="sxs-lookup"><span data-stu-id="27464-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="27464-521">Nánari upplýsingar er að finna í [Veitusniðmát tölfræðiaðgerðar](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="27464-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="27464-522">Eftirfarandi tafla sýnir niðurstöður þegar mannauðsþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="27464-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="27464-523">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-523">Cost object</span></span></th>
<th><span data-ttu-id="27464-524">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="27464-524">Magnitude</span></span></th>
<th><span data-ttu-id="27464-525">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="27464-525">Allocation factor</span></span></th>
<th><span data-ttu-id="27464-526">Upphæð</span><span class="sxs-lookup"><span data-stu-id="27464-526">Amount</span></span></th>
<th><span data-ttu-id="27464-527">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="27464-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-528">CC002</span><span class="sxs-lookup"><span data-stu-id="27464-528">CC002</span></span></td>
<td><span data-ttu-id="27464-529">Fjármál</span><span class="sxs-lookup"><span data-stu-id="27464-529">Finance</span></span></td>
<td><span data-ttu-id="27464-530">35</span><span class="sxs-lookup"><span data-stu-id="27464-530">35</span></span></td>
<td><span data-ttu-id="27464-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="27464-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="27464-532">175.00</span><span class="sxs-lookup"><span data-stu-id="27464-532">175.00</span></span></td>
<td><span data-ttu-id="27464-533">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-534">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-534">CC003</span></span></td>
<td><span data-ttu-id="27464-535">Smölun</span><span class="sxs-lookup"><span data-stu-id="27464-535">Assembly</span></span></td>
<td><span data-ttu-id="27464-536">55</span><span class="sxs-lookup"><span data-stu-id="27464-536">55</span></span></td>
<td><span data-ttu-id="27464-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="27464-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="27464-538">275.00</span><span class="sxs-lookup"><span data-stu-id="27464-538">275.00</span></span></td>
<td><span data-ttu-id="27464-539">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-540">CC004</span><span class="sxs-lookup"><span data-stu-id="27464-540">CC004</span></span></td>
<td><span data-ttu-id="27464-541">Pakkning</span><span class="sxs-lookup"><span data-stu-id="27464-541">Packaging</span></span></td>
<td><span data-ttu-id="27464-542">10</span><span class="sxs-lookup"><span data-stu-id="27464-542">10</span></span></td>
<td><span data-ttu-id="27464-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="27464-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="27464-544">50,00</span><span class="sxs-lookup"><span data-stu-id="27464-544">50.00</span></span></td>
<td><span data-ttu-id="27464-545">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-546">CC002</span><span class="sxs-lookup"><span data-stu-id="27464-546">CC002</span></span></td>
<td><span data-ttu-id="27464-547">Fjármál</span><span class="sxs-lookup"><span data-stu-id="27464-547">Finance</span></span></td>
<td><span data-ttu-id="27464-548">35</span><span class="sxs-lookup"><span data-stu-id="27464-548">35</span></span></td>
<td><span data-ttu-id="27464-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="27464-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="27464-550">436.00</span><span class="sxs-lookup"><span data-stu-id="27464-550">436.00</span></span></td>
<td><span data-ttu-id="27464-551">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-552">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-552">CC003</span></span></td>
<td><span data-ttu-id="27464-553">Smölun</span><span class="sxs-lookup"><span data-stu-id="27464-553">Assembly</span></span></td>
<td><span data-ttu-id="27464-554">55</span><span class="sxs-lookup"><span data-stu-id="27464-554">55</span></span></td>
<td><span data-ttu-id="27464-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="27464-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="27464-556">685.14</span><span class="sxs-lookup"><span data-stu-id="27464-556">685.14</span></span></td>
<td><span data-ttu-id="27464-557">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-558">CC004</span><span class="sxs-lookup"><span data-stu-id="27464-558">CC004</span></span></td>
<td><span data-ttu-id="27464-559">Pakkning</span><span class="sxs-lookup"><span data-stu-id="27464-559">Packaging</span></span></td>
<td><span data-ttu-id="27464-560">10</span><span class="sxs-lookup"><span data-stu-id="27464-560">10</span></span></td>
<td><span data-ttu-id="27464-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="27464-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="27464-562">124.57</span><span class="sxs-lookup"><span data-stu-id="27464-562">124.57</span></span></td>
<td><span data-ttu-id="27464-563">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="27464-564">Eftirfarandi tafla sýnir niðurstöður þegar Fjármálaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="27464-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="27464-565">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-565">Cost object</span></span></th>
<th><span data-ttu-id="27464-566">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="27464-566">Magnitude</span></span></th>
<th><span data-ttu-id="27464-567">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="27464-567">Allocation factor</span></span></th>
<th><span data-ttu-id="27464-568">Upphæð</span><span class="sxs-lookup"><span data-stu-id="27464-568">Amount</span></span></th>
<th><span data-ttu-id="27464-569">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="27464-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-570">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-570">CC003</span></span></td>
<td><span data-ttu-id="27464-571">Smölun</span><span class="sxs-lookup"><span data-stu-id="27464-571">Assembly</span></span></td>
<td><span data-ttu-id="27464-572">65</span><span class="sxs-lookup"><span data-stu-id="27464-572">65</span></span></td>
<td><span data-ttu-id="27464-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="27464-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="27464-574">438.75</span><span class="sxs-lookup"><span data-stu-id="27464-574">438.75</span></span></td>
<td><span data-ttu-id="27464-575">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-576">CC004</span><span class="sxs-lookup"><span data-stu-id="27464-576">CC004</span></span></td>
<td><span data-ttu-id="27464-577">Pakkning</span><span class="sxs-lookup"><span data-stu-id="27464-577">Packaging</span></span></td>
<td><span data-ttu-id="27464-578">35</span><span class="sxs-lookup"><span data-stu-id="27464-578">35</span></span></td>
<td><span data-ttu-id="27464-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="27464-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="27464-580">236.25</span><span class="sxs-lookup"><span data-stu-id="27464-580">236.25</span></span></td>
<td><span data-ttu-id="27464-581">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-582">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-582">CC003</span></span></td>
<td><span data-ttu-id="27464-583">Smölun</span><span class="sxs-lookup"><span data-stu-id="27464-583">Assembly</span></span></td>
<td><span data-ttu-id="27464-584">65</span><span class="sxs-lookup"><span data-stu-id="27464-584">65</span></span></td>
<td><span data-ttu-id="27464-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="27464-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="27464-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="27464-586">5,297.69</span></span></td>
<td><span data-ttu-id="27464-587">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-588">CC004</span><span class="sxs-lookup"><span data-stu-id="27464-588">CC004</span></span></td>
<td><span data-ttu-id="27464-589">Pakkning</span><span class="sxs-lookup"><span data-stu-id="27464-589">Packaging</span></span></td>
<td><span data-ttu-id="27464-590">35</span><span class="sxs-lookup"><span data-stu-id="27464-590">35</span></span></td>
<td><span data-ttu-id="27464-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="27464-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="27464-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="27464-592">2,852.60</span></span></td>
<td><span data-ttu-id="27464-593">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="27464-594">Eftirfarandi tafla sýnir niðurstöður þegar Samsetningarþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="27464-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="27464-595">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-595">Cost object</span></span></th>
<th><span data-ttu-id="27464-596">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="27464-596">Magnitude</span></span></th>
<th><span data-ttu-id="27464-597">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="27464-597">Allocation factor</span></span></th>
<th><span data-ttu-id="27464-598">Upphæð</span><span class="sxs-lookup"><span data-stu-id="27464-598">Amount</span></span></th>
<th><span data-ttu-id="27464-599">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="27464-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-600">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-600">Prod 1</span></span></td>
<td><span data-ttu-id="27464-601">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-601">Product 1</span></span></td>
<td><span data-ttu-id="27464-602">60</span><span class="sxs-lookup"><span data-stu-id="27464-602">60</span></span></td>
<td><span data-ttu-id="27464-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="27464-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="27464-604">535.31</span><span class="sxs-lookup"><span data-stu-id="27464-604">535.31</span></span></td>
<td><span data-ttu-id="27464-605">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-606">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-606">Prod 2</span></span></td>
<td><span data-ttu-id="27464-607">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-607">Product 2</span></span></td>
<td><span data-ttu-id="27464-608">20</span><span class="sxs-lookup"><span data-stu-id="27464-608">20</span></span></td>
<td><span data-ttu-id="27464-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="27464-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="27464-610">178.44</span><span class="sxs-lookup"><span data-stu-id="27464-610">178.44</span></span></td>
<td><span data-ttu-id="27464-611">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-612">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-612">Prod 1</span></span></td>
<td><span data-ttu-id="27464-613">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-613">Product 1</span></span></td>
<td><span data-ttu-id="27464-614">60</span><span class="sxs-lookup"><span data-stu-id="27464-614">60</span></span></td>
<td><span data-ttu-id="27464-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="27464-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="27464-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="27464-616">4,487.12</span></span></td>
<td><span data-ttu-id="27464-617">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-618">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-618">Prod 2</span></span></td>
<td><span data-ttu-id="27464-619">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-619">Product 2</span></span></td>
<td><span data-ttu-id="27464-620">20</span><span class="sxs-lookup"><span data-stu-id="27464-620">20</span></span></td>
<td><span data-ttu-id="27464-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="27464-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="27464-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="27464-622">1,495.71</span></span></td>
<td><span data-ttu-id="27464-623">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="27464-624">Eftirfarandi tafla sýnir niðurstöður þegar Umbúðaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="27464-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="27464-625">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-625">Cost object</span></span></th>
<th><span data-ttu-id="27464-626">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="27464-626">Magnitude</span></span></th>
<th><span data-ttu-id="27464-627">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="27464-627">Allocation factor</span></span></th>
<th><span data-ttu-id="27464-628">Upphæð</span><span class="sxs-lookup"><span data-stu-id="27464-628">Amount</span></span></th>
<th><span data-ttu-id="27464-629">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="27464-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-630">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-630">Prod 1</span></span></td>
<td><span data-ttu-id="27464-631">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-631">Product 1</span></span></td>
<td><span data-ttu-id="27464-632">80</span><span class="sxs-lookup"><span data-stu-id="27464-632">80</span></span></td>
<td><span data-ttu-id="27464-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="27464-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="27464-634">241.05</span><span class="sxs-lookup"><span data-stu-id="27464-634">241.05</span></span></td>
<td><span data-ttu-id="27464-635">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-636">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-636">Prod 2</span></span></td>
<td><span data-ttu-id="27464-637">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-637">Product 2</span></span></td>
<td><span data-ttu-id="27464-638">15</span><span class="sxs-lookup"><span data-stu-id="27464-638">15</span></span></td>
<td><span data-ttu-id="27464-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="27464-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="27464-640">45.20</span><span class="sxs-lookup"><span data-stu-id="27464-640">45.20</span></span></td>
<td><span data-ttu-id="27464-641">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-642">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-642">Prod 1</span></span></td>
<td><span data-ttu-id="27464-643">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-643">Product 1</span></span></td>
<td><span data-ttu-id="27464-644">80</span><span class="sxs-lookup"><span data-stu-id="27464-644">80</span></span></td>
<td><span data-ttu-id="27464-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="27464-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="27464-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="27464-646">2,507.09</span></span></td>
<td><span data-ttu-id="27464-647">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-648">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-648">Prod 2</span></span></td>
<td><span data-ttu-id="27464-649">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-649">Product 2</span></span></td>
<td><span data-ttu-id="27464-650">15</span><span class="sxs-lookup"><span data-stu-id="27464-650">15</span></span></td>
<td><span data-ttu-id="27464-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="27464-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="27464-652">470.08</span><span class="sxs-lookup"><span data-stu-id="27464-652">470.08</span></span></td>
<td><span data-ttu-id="27464-653">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="27464-654">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="27464-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="27464-655">Færslubók</span><span class="sxs-lookup"><span data-stu-id="27464-655">Journal</span></span></th>
<th><span data-ttu-id="27464-656">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="27464-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="27464-657">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="27464-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="27464-658">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="27464-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-659">00004</span><span class="sxs-lookup"><span data-stu-id="27464-659">00004</span></span></td>
<td><span data-ttu-id="27464-660">Færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="27464-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="27464-661">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="27464-661">Fiscal</span></span></td>
<td><span data-ttu-id="27464-662">2017</span><span class="sxs-lookup"><span data-stu-id="27464-662">2017</span></span></td>
<td><span data-ttu-id="27464-663">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="27464-663">Period 1</span></span></td>
<td><span data-ttu-id="27464-664">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="27464-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="27464-665">Færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="27464-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="27464-666">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="27464-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="27464-667">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="27464-668">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="27464-668">Cost element</span></span></th>
<th><span data-ttu-id="27464-669">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="27464-669">Cost behavior</span></span></th>
<th><span data-ttu-id="27464-670">Upphæð</span><span class="sxs-lookup"><span data-stu-id="27464-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-671">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="27464-672">CC001</span><span class="sxs-lookup"><span data-stu-id="27464-672">CC001</span></span></td>
<td><span data-ttu-id="27464-673">Mannauður</span><span class="sxs-lookup"><span data-stu-id="27464-673">HR</span></span></td>
<td><span data-ttu-id="27464-674">10001</span><span class="sxs-lookup"><span data-stu-id="27464-674">10001</span></span></td>
<td><span data-ttu-id="27464-675">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-675">Electricity</span></span></td>
<td><span data-ttu-id="27464-676">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-676">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-677">500,00</span><span class="sxs-lookup"><span data-stu-id="27464-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-678">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="27464-679">CC001</span><span class="sxs-lookup"><span data-stu-id="27464-679">CC001</span></span></td>
<td><span data-ttu-id="27464-680">Mannauður</span><span class="sxs-lookup"><span data-stu-id="27464-680">HR</span></span></td>
<td><span data-ttu-id="27464-681">10001</span><span class="sxs-lookup"><span data-stu-id="27464-681">10001</span></span></td>
<td><span data-ttu-id="27464-682">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-682">Electricity</span></span></td>
<td><span data-ttu-id="27464-683">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-683">Variable cost</span></span></td>
<td><span data-ttu-id="27464-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="27464-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-685">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="27464-686">CC002</span><span class="sxs-lookup"><span data-stu-id="27464-686">CC002</span></span></td>
<td><span data-ttu-id="27464-687">Fjármál</span><span class="sxs-lookup"><span data-stu-id="27464-687">Finance</span></span></td>
<td><span data-ttu-id="27464-688">10001</span><span class="sxs-lookup"><span data-stu-id="27464-688">10001</span></span></td>
<td><span data-ttu-id="27464-689">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-689">Electricity</span></span></td>
<td><span data-ttu-id="27464-690">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-690">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-691">675.00</span><span class="sxs-lookup"><span data-stu-id="27464-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-692">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="27464-693">CC002</span><span class="sxs-lookup"><span data-stu-id="27464-693">CC002</span></span></td>
<td><span data-ttu-id="27464-694">Fjármál</span><span class="sxs-lookup"><span data-stu-id="27464-694">Finance</span></span></td>
<td><span data-ttu-id="27464-695">10001</span><span class="sxs-lookup"><span data-stu-id="27464-695">10001</span></span></td>
<td><span data-ttu-id="27464-696">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-696">Electricity</span></span></td>
<td><span data-ttu-id="27464-697">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-697">Variable cost</span></span></td>
<td><span data-ttu-id="27464-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="27464-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-699">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="27464-700">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-700">CC003</span></span></td>
<td><span data-ttu-id="27464-701">Smölun</span><span class="sxs-lookup"><span data-stu-id="27464-701">Assembly</span></span></td>
<td><span data-ttu-id="27464-702">10001</span><span class="sxs-lookup"><span data-stu-id="27464-702">10001</span></span></td>
<td><span data-ttu-id="27464-703">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-703">Electricity</span></span></td>
<td><span data-ttu-id="27464-704">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-704">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-705">713.75</span><span class="sxs-lookup"><span data-stu-id="27464-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-706">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="27464-707">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-707">CC003</span></span></td>
<td><span data-ttu-id="27464-708">Smölun</span><span class="sxs-lookup"><span data-stu-id="27464-708">Assembly</span></span></td>
<td><span data-ttu-id="27464-709">10001</span><span class="sxs-lookup"><span data-stu-id="27464-709">10001</span></span></td>
<td><span data-ttu-id="27464-710">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-710">Electricity</span></span></td>
<td><span data-ttu-id="27464-711">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-711">Variable cost</span></span></td>
<td><span data-ttu-id="27464-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="27464-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-713">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="27464-714">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-714">CC003</span></span></td>
<td><span data-ttu-id="27464-715">Pakkning</span><span class="sxs-lookup"><span data-stu-id="27464-715">Packaging</span></span></td>
<td><span data-ttu-id="27464-716">10001</span><span class="sxs-lookup"><span data-stu-id="27464-716">10001</span></span></td>
<td><span data-ttu-id="27464-717">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-717">Electricity</span></span></td>
<td><span data-ttu-id="27464-718">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-718">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-719">286.25</span><span class="sxs-lookup"><span data-stu-id="27464-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-720">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="27464-721">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-721">CC003</span></span></td>
<td><span data-ttu-id="27464-722">Pakkning</span><span class="sxs-lookup"><span data-stu-id="27464-722">Packaging</span></span></td>
<td><span data-ttu-id="27464-723">10001</span><span class="sxs-lookup"><span data-stu-id="27464-723">10001</span></span></td>
<td><span data-ttu-id="27464-724">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-724">Electricity</span></span></td>
<td><span data-ttu-id="27464-725">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-725">Variable cost</span></span></td>
<td><span data-ttu-id="27464-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="27464-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-727">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="27464-728">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-728">Prod 1</span></span></td>
<td><span data-ttu-id="27464-729">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-729">Product 1</span></span></td>
<td><span data-ttu-id="27464-730">10001</span><span class="sxs-lookup"><span data-stu-id="27464-730">10001</span></span></td>
<td><span data-ttu-id="27464-731">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-731">Electricity</span></span></td>
<td><span data-ttu-id="27464-732">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-732">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-733">776.36</span><span class="sxs-lookup"><span data-stu-id="27464-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-734">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="27464-735">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-735">Prod 1</span></span></td>
<td><span data-ttu-id="27464-736">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-736">Product 1</span></span></td>
<td><span data-ttu-id="27464-737">10001</span><span class="sxs-lookup"><span data-stu-id="27464-737">10001</span></span></td>
<td><span data-ttu-id="27464-738">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-738">Electricity</span></span></td>
<td><span data-ttu-id="27464-739">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-739">Variable cost</span></span></td>
<td><span data-ttu-id="27464-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="27464-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-741">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="27464-742">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-742">Prod 2</span></span></td>
<td><span data-ttu-id="27464-743">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-743">Product 1</span></span></td>
<td><span data-ttu-id="27464-744">10001</span><span class="sxs-lookup"><span data-stu-id="27464-744">10001</span></span></td>
<td><span data-ttu-id="27464-745">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-745">Electricity</span></span></td>
<td><span data-ttu-id="27464-746">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-746">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-747">223.64</span><span class="sxs-lookup"><span data-stu-id="27464-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-748">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="27464-749">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-749">Prod 2</span></span></td>
<td><span data-ttu-id="27464-750">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-750">Product 1</span></span></td>
<td><span data-ttu-id="27464-751">10001</span><span class="sxs-lookup"><span data-stu-id="27464-751">10001</span></span></td>
<td><span data-ttu-id="27464-752">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-752">Electricity</span></span></td>
<td><span data-ttu-id="27464-753">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-753">Variable cost</span></span></td>
<td><span data-ttu-id="27464-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="27464-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="27464-755">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="27464-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="27464-756">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="27464-757">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="27464-757">Cost element</span></span></th>
<th><span data-ttu-id="27464-758">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="27464-758">Cost behavior</span></span></th>
<th><span data-ttu-id="27464-759">Upphæð</span><span class="sxs-lookup"><span data-stu-id="27464-759">Amount</span></span></th>
<th><span data-ttu-id="27464-760">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="27464-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="27464-761">CC001</span><span class="sxs-lookup"><span data-stu-id="27464-761">CC001</span></span></td>
<td><span data-ttu-id="27464-762">Mannauður</span><span class="sxs-lookup"><span data-stu-id="27464-762">HR</span></span></td>
<td><span data-ttu-id="27464-763">10001</span><span class="sxs-lookup"><span data-stu-id="27464-763">10001</span></span></td>
<td><span data-ttu-id="27464-764">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-764">Electricity</span></span></td>
<td><span data-ttu-id="27464-765">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-765">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="27464-766">-500.00</span></span></td>
<td><span data-ttu-id="27464-767">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-768">CC002</span><span class="sxs-lookup"><span data-stu-id="27464-768">CC002</span></span></td>
<td><span data-ttu-id="27464-769">Fjármál</span><span class="sxs-lookup"><span data-stu-id="27464-769">Finance</span></span></td>
<td><span data-ttu-id="27464-770">10001</span><span class="sxs-lookup"><span data-stu-id="27464-770">10001</span></span></td>
<td><span data-ttu-id="27464-771">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-771">Electricity</span></span></td>
<td><span data-ttu-id="27464-772">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-772">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-773">175.00</span><span class="sxs-lookup"><span data-stu-id="27464-773">175.00</span></span></td>
<td><span data-ttu-id="27464-774">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-775">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-775">CC003</span></span></td>
<td><span data-ttu-id="27464-776">Smölun</span><span class="sxs-lookup"><span data-stu-id="27464-776">Assembly</span></span></td>
<td><span data-ttu-id="27464-777">10001</span><span class="sxs-lookup"><span data-stu-id="27464-777">10001</span></span></td>
<td><span data-ttu-id="27464-778">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-778">Electricity</span></span></td>
<td><span data-ttu-id="27464-779">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-779">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-780">275.00</span><span class="sxs-lookup"><span data-stu-id="27464-780">275.00</span></span></td>
<td><span data-ttu-id="27464-781">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-782">CC004</span><span class="sxs-lookup"><span data-stu-id="27464-782">CC004</span></span></td>
<td><span data-ttu-id="27464-783">Pakkning</span><span class="sxs-lookup"><span data-stu-id="27464-783">Packaging</span></span></td>
<td><span data-ttu-id="27464-784">10001</span><span class="sxs-lookup"><span data-stu-id="27464-784">10001</span></span></td>
<td><span data-ttu-id="27464-785">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-785">Electricity</span></span></td>
<td><span data-ttu-id="27464-786">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-786">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-787">50,00</span><span class="sxs-lookup"><span data-stu-id="27464-787">50,00</span></span></td>
<td><span data-ttu-id="27464-788">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-789">CC001</span><span class="sxs-lookup"><span data-stu-id="27464-789">CC001</span></span></td>
<td><span data-ttu-id="27464-790">Mannauður</span><span class="sxs-lookup"><span data-stu-id="27464-790">HR</span></span></td>
<td><span data-ttu-id="27464-791">10001</span><span class="sxs-lookup"><span data-stu-id="27464-791">10001</span></span></td>
<td><span data-ttu-id="27464-792">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-792">Electricity</span></span></td>
<td><span data-ttu-id="27464-793">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-793">Variable cost</span></span></td>
<td><span data-ttu-id="27464-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="27464-794">-1,245.71</span></span></td>
<td><span data-ttu-id="27464-795">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-796">CC002</span><span class="sxs-lookup"><span data-stu-id="27464-796">CC002</span></span></td>
<td><span data-ttu-id="27464-797">Fjármál</span><span class="sxs-lookup"><span data-stu-id="27464-797">Finance</span></span></td>
<td><span data-ttu-id="27464-798">10001</span><span class="sxs-lookup"><span data-stu-id="27464-798">10001</span></span></td>
<td><span data-ttu-id="27464-799">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-799">Electricity</span></span></td>
<td><span data-ttu-id="27464-800">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-800">Variable cost</span></span></td>
<td><span data-ttu-id="27464-801">436.00</span><span class="sxs-lookup"><span data-stu-id="27464-801">436.00</span></span></td>
<td><span data-ttu-id="27464-802">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-803">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-803">CC003</span></span></td>
<td><span data-ttu-id="27464-804">Smölun</span><span class="sxs-lookup"><span data-stu-id="27464-804">Assembly</span></span></td>
<td><span data-ttu-id="27464-805">10001</span><span class="sxs-lookup"><span data-stu-id="27464-805">10001</span></span></td>
<td><span data-ttu-id="27464-806">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-806">Electricity</span></span></td>
<td><span data-ttu-id="27464-807">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-807">Variable cost</span></span></td>
<td><span data-ttu-id="27464-808">685.14</span><span class="sxs-lookup"><span data-stu-id="27464-808">685.14</span></span></td>
<td><span data-ttu-id="27464-809">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-810">CC004</span><span class="sxs-lookup"><span data-stu-id="27464-810">CC004</span></span></td>
<td><span data-ttu-id="27464-811">Pakkning</span><span class="sxs-lookup"><span data-stu-id="27464-811">Packaging</span></span></td>
<td><span data-ttu-id="27464-812">10001</span><span class="sxs-lookup"><span data-stu-id="27464-812">10001</span></span></td>
<td><span data-ttu-id="27464-813">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-813">Electricity</span></span></td>
<td><span data-ttu-id="27464-814">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-814">Variable cost</span></span></td>
<td><span data-ttu-id="27464-815">124.57</span><span class="sxs-lookup"><span data-stu-id="27464-815">124.57</span></span></td>
<td><span data-ttu-id="27464-816">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-817">CC002</span><span class="sxs-lookup"><span data-stu-id="27464-817">CC002</span></span></td>
<td><span data-ttu-id="27464-818">Fjármál</span><span class="sxs-lookup"><span data-stu-id="27464-818">Finance</span></span></td>
<td><span data-ttu-id="27464-819">10001</span><span class="sxs-lookup"><span data-stu-id="27464-819">10001</span></span></td>
<td><span data-ttu-id="27464-820">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-820">Electricity</span></span></td>
<td><span data-ttu-id="27464-821">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-821">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="27464-822">-675.00</span></span></td>
<td><span data-ttu-id="27464-823">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-824">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-824">CC003</span></span></td>
<td><span data-ttu-id="27464-825">Smölun</span><span class="sxs-lookup"><span data-stu-id="27464-825">Assembly</span></span></td>
<td><span data-ttu-id="27464-826">10001</span><span class="sxs-lookup"><span data-stu-id="27464-826">10001</span></span></td>
<td><span data-ttu-id="27464-827">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-827">Electricity</span></span></td>
<td><span data-ttu-id="27464-828">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-828">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-829">438.75</span><span class="sxs-lookup"><span data-stu-id="27464-829">438.75</span></span></td>
<td><span data-ttu-id="27464-830">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-831">CC004</span><span class="sxs-lookup"><span data-stu-id="27464-831">CC004</span></span></td>
<td><span data-ttu-id="27464-832">Pakkning</span><span class="sxs-lookup"><span data-stu-id="27464-832">Packaging</span></span></td>
<td><span data-ttu-id="27464-833">10001</span><span class="sxs-lookup"><span data-stu-id="27464-833">10001</span></span></td>
<td><span data-ttu-id="27464-834">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-834">Electricity</span></span></td>
<td><span data-ttu-id="27464-835">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-835">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-836">236.25</span><span class="sxs-lookup"><span data-stu-id="27464-836">236.25</span></span></td>
<td><span data-ttu-id="27464-837">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-838">CC002</span><span class="sxs-lookup"><span data-stu-id="27464-838">CC002</span></span></td>
<td><span data-ttu-id="27464-839">Fjármál</span><span class="sxs-lookup"><span data-stu-id="27464-839">Finance</span></span></td>
<td><span data-ttu-id="27464-840">10001</span><span class="sxs-lookup"><span data-stu-id="27464-840">10001</span></span></td>
<td><span data-ttu-id="27464-841">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-841">Electricity</span></span></td>
<td><span data-ttu-id="27464-842">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-842">Variable cost</span></span></td>
<td><span data-ttu-id="27464-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="27464-843">-8,150.29</span></span></td>
<td><span data-ttu-id="27464-844">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-845">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-845">CC003</span></span></td>
<td><span data-ttu-id="27464-846">Smölun</span><span class="sxs-lookup"><span data-stu-id="27464-846">Assembly</span></span></td>
<td><span data-ttu-id="27464-847">10001</span><span class="sxs-lookup"><span data-stu-id="27464-847">10001</span></span></td>
<td><span data-ttu-id="27464-848">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-848">Electricity</span></span></td>
<td><span data-ttu-id="27464-849">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-849">Variable cost</span></span></td>
<td><span data-ttu-id="27464-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="27464-850">5,297.69</span></span></td>
<td><span data-ttu-id="27464-851">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-852">CC004</span><span class="sxs-lookup"><span data-stu-id="27464-852">CC004</span></span></td>
<td><span data-ttu-id="27464-853">Pakkning</span><span class="sxs-lookup"><span data-stu-id="27464-853">Packaging</span></span></td>
<td><span data-ttu-id="27464-854">10001</span><span class="sxs-lookup"><span data-stu-id="27464-854">10001</span></span></td>
<td><span data-ttu-id="27464-855">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-855">Electricity</span></span></td>
<td><span data-ttu-id="27464-856">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-856">Variable cost</span></span></td>
<td><span data-ttu-id="27464-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="27464-857">2,852.60</span></span></td>
<td><span data-ttu-id="27464-858">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-859">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-859">CC003</span></span></td>
<td><span data-ttu-id="27464-860">Smölun</span><span class="sxs-lookup"><span data-stu-id="27464-860">Assembly</span></span></td>
<td><span data-ttu-id="27464-861">10001</span><span class="sxs-lookup"><span data-stu-id="27464-861">10001</span></span></td>
<td><span data-ttu-id="27464-862">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-862">Electricity</span></span></td>
<td><span data-ttu-id="27464-863">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-863">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="27464-864">-713.75</span></span></td>
<td><span data-ttu-id="27464-865">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-866">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-866">Prod 1</span></span></td>
<td><span data-ttu-id="27464-867">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-867">Product 1</span></span></td>
<td><span data-ttu-id="27464-868">10001</span><span class="sxs-lookup"><span data-stu-id="27464-868">10001</span></span></td>
<td><span data-ttu-id="27464-869">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-869">Electricity</span></span></td>
<td><span data-ttu-id="27464-870">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-870">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-871">535.31</span><span class="sxs-lookup"><span data-stu-id="27464-871">535.31</span></span></td>
<td><span data-ttu-id="27464-872">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-873">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-873">Prod 2</span></span></td>
<td><span data-ttu-id="27464-874">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-874">Product 2</span></span></td>
<td><span data-ttu-id="27464-875">10001</span><span class="sxs-lookup"><span data-stu-id="27464-875">10001</span></span></td>
<td><span data-ttu-id="27464-876">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-876">Electricity</span></span></td>
<td><span data-ttu-id="27464-877">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-877">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-878">178.44</span><span class="sxs-lookup"><span data-stu-id="27464-878">178.44</span></span></td>
<td><span data-ttu-id="27464-879">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-880">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-880">CC003</span></span></td>
<td><span data-ttu-id="27464-881">Smölun</span><span class="sxs-lookup"><span data-stu-id="27464-881">Assembly</span></span></td>
<td><span data-ttu-id="27464-882">10001</span><span class="sxs-lookup"><span data-stu-id="27464-882">10001</span></span></td>
<td><span data-ttu-id="27464-883">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-883">Electricity</span></span></td>
<td><span data-ttu-id="27464-884">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-884">Variable cost</span></span></td>
<td><span data-ttu-id="27464-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="27464-885">-5,982.83</span></span></td>
<td><span data-ttu-id="27464-886">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-887">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-887">Prod 1</span></span></td>
<td><span data-ttu-id="27464-888">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-888">Product 1</span></span></td>
<td><span data-ttu-id="27464-889">10001</span><span class="sxs-lookup"><span data-stu-id="27464-889">10001</span></span></td>
<td><span data-ttu-id="27464-890">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-890">Electricity</span></span></td>
<td><span data-ttu-id="27464-891">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-891">Variable cost</span></span></td>
<td><span data-ttu-id="27464-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="27464-892">4,487.12</span></span></td>
<td><span data-ttu-id="27464-893">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-894">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-894">Prod 2</span></span></td>
<td><span data-ttu-id="27464-895">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-895">Product 2</span></span></td>
<td><span data-ttu-id="27464-896">10001</span><span class="sxs-lookup"><span data-stu-id="27464-896">10001</span></span></td>
<td><span data-ttu-id="27464-897">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-897">Electricity</span></span></td>
<td><span data-ttu-id="27464-898">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-898">Variable cost</span></span></td>
<td><span data-ttu-id="27464-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="27464-899">1,495.71</span></span></td>
<td><span data-ttu-id="27464-900">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-901">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-901">CC003</span></span></td>
<td><span data-ttu-id="27464-902">Smölun</span><span class="sxs-lookup"><span data-stu-id="27464-902">Assembly</span></span></td>
<td><span data-ttu-id="27464-903">10001</span><span class="sxs-lookup"><span data-stu-id="27464-903">10001</span></span></td>
<td><span data-ttu-id="27464-904">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-904">Electricity</span></span></td>
<td><span data-ttu-id="27464-905">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-905">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="27464-906">-286.25</span></span></td>
<td><span data-ttu-id="27464-907">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-908">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-908">Prod 1</span></span></td>
<td><span data-ttu-id="27464-909">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-909">Product 1</span></span></td>
<td><span data-ttu-id="27464-910">10001</span><span class="sxs-lookup"><span data-stu-id="27464-910">10001</span></span></td>
<td><span data-ttu-id="27464-911">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-911">Electricity</span></span></td>
<td><span data-ttu-id="27464-912">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-912">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-913">241.05</span><span class="sxs-lookup"><span data-stu-id="27464-913">241.05</span></span></td>
<td><span data-ttu-id="27464-914">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-915">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-915">Prod 2</span></span></td>
<td><span data-ttu-id="27464-916">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-916">Product 2</span></span></td>
<td><span data-ttu-id="27464-917">10001</span><span class="sxs-lookup"><span data-stu-id="27464-917">10001</span></span></td>
<td><span data-ttu-id="27464-918">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-918">Electricity</span></span></td>
<td><span data-ttu-id="27464-919">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-919">Fixed cost</span></span></td>
<td><span data-ttu-id="27464-920">45.20</span><span class="sxs-lookup"><span data-stu-id="27464-920">45.20</span></span></td>
<td><span data-ttu-id="27464-921">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-922">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-922">CC003</span></span></td>
<td><span data-ttu-id="27464-923">Smölun</span><span class="sxs-lookup"><span data-stu-id="27464-923">Assembly</span></span></td>
<td><span data-ttu-id="27464-924">10001</span><span class="sxs-lookup"><span data-stu-id="27464-924">10001</span></span></td>
<td><span data-ttu-id="27464-925">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-925">Electricity</span></span></td>
<td><span data-ttu-id="27464-926">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-926">Variable cost</span></span></td>
<td><span data-ttu-id="27464-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="27464-927">-2,977.17</span></span></td>
<td><span data-ttu-id="27464-928">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-929">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-929">Prod 1</span></span></td>
<td><span data-ttu-id="27464-930">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-930">Product 1</span></span></td>
<td><span data-ttu-id="27464-931">10001</span><span class="sxs-lookup"><span data-stu-id="27464-931">10001</span></span></td>
<td><span data-ttu-id="27464-932">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-932">Electricity</span></span></td>
<td><span data-ttu-id="27464-933">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-933">Variable cost</span></span></td>
<td><span data-ttu-id="27464-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="27464-934">2,507.09</span></span></td>
<td><span data-ttu-id="27464-935">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="27464-936">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-936">Prod 2</span></span></td>
<td><span data-ttu-id="27464-937">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-937">Product 2</span></span></td>
<td><span data-ttu-id="27464-938">10001</span><span class="sxs-lookup"><span data-stu-id="27464-938">10001</span></span></td>
<td><span data-ttu-id="27464-939">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-939">Electricity</span></span></td>
<td><span data-ttu-id="27464-940">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-940">Variable cost</span></span></td>
<td><span data-ttu-id="27464-941">470.08</span><span class="sxs-lookup"><span data-stu-id="27464-941">470.08</span></span></td>
<td><span data-ttu-id="27464-942">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="27464-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="27464-943">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="27464-943">Conclusion</span></span>
<span data-ttu-id="27464-944">Í Fjárhagsbókhaldi er kostnaður upp á 10.000,00 fyrir rafmagn bókaður á kenni leppkostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="27464-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="27464-945">Þar af leiðandi munu kostnaðarbókarar vita að það þarf að úthluta þessum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="27464-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="27464-946">Í kostnaðarbókhaldi streymir kostnaður þvert á fyrirtækiseiningar og stig, samkvæmt þeim stefnum og reglum sem eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="27464-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="27464-947">Hver kostnaður hefur verið tengdur úthlutunargrunni sem veitir besta mat á úthlutun á kostnaði.</span><span class="sxs-lookup"><span data-stu-id="27464-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="27464-948">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="27464-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="27464-949">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="27464-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="27464-950">Samtala</span><span class="sxs-lookup"><span data-stu-id="27464-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="27464-951">CC099</span><span class="sxs-lookup"><span data-stu-id="27464-951">CC099</span></span></th>
<th><span data-ttu-id="27464-952">CC001</span><span class="sxs-lookup"><span data-stu-id="27464-952">CC001</span></span></th>
<th><span data-ttu-id="27464-953">CC002</span><span class="sxs-lookup"><span data-stu-id="27464-953">CC002</span></span></th>
<th><span data-ttu-id="27464-954">CC003</span><span class="sxs-lookup"><span data-stu-id="27464-954">CC003</span></span></th>
<th><span data-ttu-id="27464-955">CC004</span><span class="sxs-lookup"><span data-stu-id="27464-955">CC004</span></span></th>
<th><span data-ttu-id="27464-956">Verk 1</span><span class="sxs-lookup"><span data-stu-id="27464-956">Proj 1</span></span></th>
<th><span data-ttu-id="27464-957">Verk 2</span><span class="sxs-lookup"><span data-stu-id="27464-957">Proj 2</span></span></th>
<th><span data-ttu-id="27464-958">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="27464-958">Prod 1</span></span></th>
<th><span data-ttu-id="27464-959">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="27464-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="27464-960">10001 Rafmagn</span><span class="sxs-lookup"><span data-stu-id="27464-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="27464-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="27464-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="27464-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="27464-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="27464-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="27464-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="27464-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="27464-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="27464-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="27464-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="27464-970">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="27464-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-971">0,00</span><span class="sxs-lookup"><span data-stu-id="27464-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="27464-972">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-973">0,00</span><span class="sxs-lookup"><span data-stu-id="27464-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-974">0,00</span><span class="sxs-lookup"><span data-stu-id="27464-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-975">0,00</span><span class="sxs-lookup"><span data-stu-id="27464-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-976">0,00</span><span class="sxs-lookup"><span data-stu-id="27464-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-977">0,00</span><span class="sxs-lookup"><span data-stu-id="27464-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="27464-978">776.36</span><span class="sxs-lookup"><span data-stu-id="27464-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-979">223.64</span><span class="sxs-lookup"><span data-stu-id="27464-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="27464-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="27464-981">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="27464-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-982">000</span><span class="sxs-lookup"><span data-stu-id="27464-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-983">0,00</span><span class="sxs-lookup"><span data-stu-id="27464-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-984">0,00</span><span class="sxs-lookup"><span data-stu-id="27464-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-985">0,00</span><span class="sxs-lookup"><span data-stu-id="27464-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-986">0,00</span><span class="sxs-lookup"><span data-stu-id="27464-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-987">30,00</span><span class="sxs-lookup"><span data-stu-id="27464-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-988">10,00</span><span class="sxs-lookup"><span data-stu-id="27464-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="27464-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="27464-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="27464-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="27464-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="27464-992">Þetta efnisatriði sýnir hvernig fyrir aðalkostnaðareiningin 10001 Rafmagn flæðir í gegnum kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="27464-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="27464-993">Þar af leiðandi er þessum sameiginlega kostnaði úthlutað á lægsta stigið í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="27464-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="27464-994">Með öðrum orðum bera kostnaðarhlutir á lægsta stiginu kostnaðinn.</span><span class="sxs-lookup"><span data-stu-id="27464-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="27464-995">Ef þú þarft sjónrænt flæði kostnaðar á milli kostnaðarhluta er hægt að nota stefnureglur samantekins kostnaðar til að gera kostnaðarflæðið sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="27464-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="27464-996">Fyrir frekari upplýsingar skal sjá [Stefna fyrir samantekt kostnaðar og útreikning sameiginlegs kostnaðar](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="27464-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



