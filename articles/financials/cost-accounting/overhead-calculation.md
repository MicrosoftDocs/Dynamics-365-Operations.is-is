---
title: "Útreikningur fastakostnaður"
description: "Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði."
author: AndersGirke
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 936e54c0ef1de449afda2392cd1fbb304eed631b
ms.contentlocale: is-is
ms.lasthandoff: 01/17/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="58049-103">Útreikningur fastakostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="58049-104">Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði.</span><span class="sxs-lookup"><span data-stu-id="58049-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="58049-105">Skýrsluskilgreining</span><span class="sxs-lookup"><span data-stu-id="58049-105">Term definition</span></span>
---------------

<span data-ttu-id="58049-106">Stjórnunarkostnaður er sá kostnaður sem stofnað er til fyrir rekstur fyrirtækis, en sem ekki er hægt að rekja beint til neinna sérstakrar starfsemi, vöru eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="58049-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="58049-107">Stjórnunarkostnaður veitir mikilvægan stuðning við myndun hagnaðarmyndandi verkþátta.</span><span class="sxs-lookup"><span data-stu-id="58049-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="58049-108">Hér eru nokkur dæmi um skilyrði:</span><span class="sxs-lookup"><span data-stu-id="58049-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="58049-109">Leiga</span><span class="sxs-lookup"><span data-stu-id="58049-109">Rent</span></span>
-   <span data-ttu-id="58049-110">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-110">Electricity</span></span>
-   <span data-ttu-id="58049-111">Stjórnunarkostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="58049-112">Yfirlit yfir útreikning fastakostnaðar</span><span class="sxs-lookup"><span data-stu-id="58049-112">Overhead calculation overview</span></span>
<span data-ttu-id="58049-113">Útreikningur fastakostnaðar keyrir reglur kostnaðarbókhalds í réttri röð.</span><span class="sxs-lookup"><span data-stu-id="58049-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="58049-114">Hægt er að keyra útreikning fastakostnaðar margsinnis fyrir sama fjárhagstímabil ef reglum kostnaðarbókhalds hefur verið breytt eða ákveðnar villur hafa fundist.</span><span class="sxs-lookup"><span data-stu-id="58049-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="58049-115">Hver keyrsla á útreikningi fastakostnaðar er geymd og fær einkvæmt útgáfukenni sem gerir kleift að bera saman útreikning í mismunandi útgáfum.</span><span class="sxs-lookup"><span data-stu-id="58049-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="58049-116">Kostnaðarfærslur sem útreikningur fastakostnaðar mynda fá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="58049-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="58049-117">Dagsetningin bókhald samsvarar lokadagsetning fjárhagstímabilsins sem er dagsetning reikningsskiladagsetning reikningsskila notað í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="58049-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="58049-118">Einkvæmt útgáfukenni samanstendur af eftirfarandi þáttum:</span><span class="sxs-lookup"><span data-stu-id="58049-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="58049-119">Gerð útgáfu</span><span class="sxs-lookup"><span data-stu-id="58049-119">Version type</span></span>
-   <span data-ttu-id="58049-120">Dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="58049-120">Date and time</span></span>
-   <span data-ttu-id="58049-121">Fjárhagur kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="58049-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="58049-122">Fjárhagsár</span><span class="sxs-lookup"><span data-stu-id="58049-122">Fiscal year</span></span>
-   <span data-ttu-id="58049-123">Reikningstímabil</span><span class="sxs-lookup"><span data-stu-id="58049-123">Fiscal period</span></span>

<span data-ttu-id="58049-124">Útreikningur fastakostnaðar er keyrður óháð því hver útgáfan er.</span><span class="sxs-lookup"><span data-stu-id="58049-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="58049-125">Þess vegna er hægt að reikna út áætlaða útgáfu á undan raunútgáfu.</span><span class="sxs-lookup"><span data-stu-id="58049-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="58049-126">Útreikningur fastakostnaðar samanstendur af fjórum skrefum, eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="58049-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="58049-127">Í hverju skrefi er færslubókarhaus stofnaður með bókarfærslum.</span><span class="sxs-lookup"><span data-stu-id="58049-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="58049-128">Þessi færslubókarhaus geymir inntaksgögn fyrir hvert útreikningsþrep.</span><span class="sxs-lookup"><span data-stu-id="58049-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="58049-129">Stefnur og reglur eru notaðar í hverri færslulínu og kostnaðarfærslur eru myndaðar sem úttak.</span><span class="sxs-lookup"><span data-stu-id="58049-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="58049-130">Þess vegna hefurðu ávallt fullan rekjanleika.</span><span class="sxs-lookup"><span data-stu-id="58049-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="58049-131">[![Útreikningur fastakostnaðar](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="58049-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="58049-132">Reikna og úthluta sameiginlegur kostnaði vegna rafmagns</span><span class="sxs-lookup"><span data-stu-id="58049-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="58049-133">Í Fjárhagsbókhaldi er ákveðinn kostnaður, eins og rafmagn, skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="58049-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="58049-134">Þar af leiðandi er nákvæmar innsýn rekstrarfélags ekki veitt fyrir kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="58049-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="58049-135">Í kostnaðarbókhaldi verður kostnaður að flæða í gegnum fyrirtækiseiningar til að veita rétta innsýn rekstrarfélags þvert á allar fyrirtækiseiningar og stig.</span><span class="sxs-lookup"><span data-stu-id="58049-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="58049-136">Þetta flæði verður að byggja á annaðhvort nákvæmri færslu notkunar eða sanngjarnri matsreglu.</span><span class="sxs-lookup"><span data-stu-id="58049-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="58049-137">Í fjárhagnum er hægt að bóka rafmagnskostnað eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="58049-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="58049-138">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="58049-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="58049-139">Kostnaðarstaður</span><span class="sxs-lookup"><span data-stu-id="58049-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="58049-140">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="58049-140">Main account</span></span></th>
<th><span data-ttu-id="58049-141">Upphæð í bókhaldsgjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="58049-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-142">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="58049-143">CC099</span><span class="sxs-lookup"><span data-stu-id="58049-143">CC099</span></span></td>
<td><span data-ttu-id="58049-144">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58049-144">Default cost center</span></span></td>
<td><span data-ttu-id="58049-145">10001</span><span class="sxs-lookup"><span data-stu-id="58049-145">10001</span></span></td>
<td><span data-ttu-id="58049-146">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-146">Electricity</span></span></td>
<td><span data-ttu-id="58049-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="58049-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="58049-148">Skref 1: Keyra útreikning kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="58049-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="58049-149">Sjálfvirkt er að þegar kostnaðarfærslur eru fluttar úr grunngögnum fái þær flokkun kostnaðarhegðunar **Óflokkað** í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="58049-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="58049-150">Með því að nota stefnureglur kostnaðarhegðunar er hægt að endurflokka kostnaðarfærslur sem annaðhvort **Fastan kostnað** eða **Breytilegan kostnað**.</span><span class="sxs-lookup"><span data-stu-id="58049-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="58049-151">Tilgreinið reglu kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="58049-151">Define the cost behavior rule</span></span>

<span data-ttu-id="58049-152">Í sumum tilfellum er hluti af kostnaði föst þóknun og eftirstandandi kostnaður byggist á notkun.</span><span class="sxs-lookup"><span data-stu-id="58049-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="58049-153">Rafmagnsreikningar stemma oft við þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="58049-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="58049-154">Þegar tiltekin föst þóknun hefur verið greidd, er greitt fyrir notkun á kílóvattklukkustund (Kwh).</span><span class="sxs-lookup"><span data-stu-id="58049-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="58049-155">Til dæmis ef föst kostnaðarþóknun er 1000.00 sýnir þetta hvernig regla kostnaðarhegðunar er skilgreind:</span><span class="sxs-lookup"><span data-stu-id="58049-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="58049-156">Föst upphæð 1.000,00</span><span class="sxs-lookup"><span data-stu-id="58049-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="58049-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="58049-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="58049-158">1000.01 &lt; N = Breyta</span><span class="sxs-lookup"><span data-stu-id="58049-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="58049-159">Færslubók</span><span class="sxs-lookup"><span data-stu-id="58049-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="58049-160">Færslubók</span><span class="sxs-lookup"><span data-stu-id="58049-160">Journal</span></span></th>
<th><span data-ttu-id="58049-161">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="58049-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="58049-162">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="58049-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="58049-163">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="58049-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-164">00001</span><span class="sxs-lookup"><span data-stu-id="58049-164">00001</span></span></td>
<td><span data-ttu-id="58049-165">Færslubók útreiknings fyrir kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58049-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="58049-166">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="58049-166">Fiscal</span></span></td>
<td><span data-ttu-id="58049-167">2017</span><span class="sxs-lookup"><span data-stu-id="58049-167">2017</span></span></td>
<td><span data-ttu-id="58049-168">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="58049-168">Period 1</span></span></td>
<td><span data-ttu-id="58049-169">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="58049-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="58049-170">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="58049-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="58049-171">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="58049-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="58049-172">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="58049-173">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58049-173">Cost element</span></span></th>
<th><span data-ttu-id="58049-174">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58049-174">Cost behavior</span></span></th>
<th><span data-ttu-id="58049-175">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58049-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-176">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="58049-177">CC099</span><span class="sxs-lookup"><span data-stu-id="58049-177">CC099</span></span></td>
<td><span data-ttu-id="58049-178">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58049-178">Default cost center</span></span></td>
<td><span data-ttu-id="58049-179">10001</span><span class="sxs-lookup"><span data-stu-id="58049-179">10001</span></span></td>
<td><span data-ttu-id="58049-180">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-180">Electricity</span></span></td>
<td><span data-ttu-id="58049-181">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="58049-181">Unclassified</span></span></td>
<td><span data-ttu-id="58049-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="58049-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="58049-183">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="58049-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58049-184">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="58049-185">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58049-185">Cost element</span></span></th>
<th><span data-ttu-id="58049-186">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58049-186">Cost behavior</span></span></th>
<th><span data-ttu-id="58049-187">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58049-187">Amount</span></span></th>
<th><span data-ttu-id="58049-188">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="58049-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-189">CC099</span><span class="sxs-lookup"><span data-stu-id="58049-189">CC099</span></span></td>
<td><span data-ttu-id="58049-190">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58049-190">Default cost center</span></span></td>
<td><span data-ttu-id="58049-191">10001</span><span class="sxs-lookup"><span data-stu-id="58049-191">10001</span></span></td>
<td><span data-ttu-id="58049-192">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-192">Electricity</span></span></td>
<td><span data-ttu-id="58049-193">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="58049-193">Unclassified</span></span></td>
<td><span data-ttu-id="58049-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="58049-194">10,000.00</span></span></td>
<td><span data-ttu-id="58049-195">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-196">CC099</span><span class="sxs-lookup"><span data-stu-id="58049-196">CC099</span></span></td>
<td><span data-ttu-id="58049-197">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58049-197">Default cost center</span></span></td>
<td><span data-ttu-id="58049-198">10001</span><span class="sxs-lookup"><span data-stu-id="58049-198">10001</span></span></td>
<td><span data-ttu-id="58049-199">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-199">Electricity</span></span></td>
<td><span data-ttu-id="58049-200">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="58049-200">Unclassified</span></span></td>
<td><span data-ttu-id="58049-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="58049-201">-10,000.00</span></span></td>
<td><span data-ttu-id="58049-202">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-203">CC099</span><span class="sxs-lookup"><span data-stu-id="58049-203">CC099</span></span></td>
<td><span data-ttu-id="58049-204">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58049-204">Default cost center</span></span></td>
<td><span data-ttu-id="58049-205">10001</span><span class="sxs-lookup"><span data-stu-id="58049-205">10001</span></span></td>
<td><span data-ttu-id="58049-206">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-206">Electricity</span></span></td>
<td><span data-ttu-id="58049-207">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-207">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="58049-208">1,000.00</span></span></td>
<td><span data-ttu-id="58049-209">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-210">CC099</span><span class="sxs-lookup"><span data-stu-id="58049-210">CC099</span></span></td>
<td><span data-ttu-id="58049-211">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58049-211">Default cost center</span></span></td>
<td><span data-ttu-id="58049-212">10001</span><span class="sxs-lookup"><span data-stu-id="58049-212">10001</span></span></td>
<td><span data-ttu-id="58049-213">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-213">Electricity</span></span></td>
<td><span data-ttu-id="58049-214">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-214">Variable cost</span></span></td>
<td><span data-ttu-id="58049-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="58049-215">9,000.00</span></span></td>
<td><span data-ttu-id="58049-216">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58049-217">Nákvæmar upplýsingar um kostnaðarhegðun er að finna í Reglu kostnaðarhegðunar.</span><span class="sxs-lookup"><span data-stu-id="58049-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="58049-218">(Athugaðu að þetta efnisatriði hefur ekki enn verið fullklárað en er væntanlegt.)</span><span class="sxs-lookup"><span data-stu-id="58049-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="58049-219">Skref 2: Keyra útreikning kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="58049-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="58049-220">Kostnaðardreifing er notuð til að endurúthluta kostnaði frá einum kostnaðarhlut til annars eða fleiri kostnaðarhluta með því að nota viðeigandi úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="58049-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="58049-221">Kostnaðardreifing og kostnaðarúthlutun eru ólíkar að því leyti að kostnaðardreifing kemur alltaf upp á stigi aðalkostnaðareiningar upphaflegs verðs.</span><span class="sxs-lookup"><span data-stu-id="58049-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="58049-222">Tilgreinið kostnaðardreifingarreglu</span><span class="sxs-lookup"><span data-stu-id="58049-222">Define the cost distribution rule</span></span>

<span data-ttu-id="58049-223">Í Fjárhagsbókhaldi er rafmagnskostnaður oft skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="58049-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="58049-224">Í kostnaðarbókhaldi er þessi nálgun ekki nógu nákvæm.</span><span class="sxs-lookup"><span data-stu-id="58049-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="58049-225">Breytilegur kostnaði þarf að dreifa á staka kostnaðarhluti á sanngjörnum grunni.</span><span class="sxs-lookup"><span data-stu-id="58049-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="58049-226">Rökréttasti úthlutunargrunnurinn er notkun á rafmagni (Kwh).</span><span class="sxs-lookup"><span data-stu-id="58049-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="58049-227">Stofnað er tölfræðilegt víddarstak sem er nefnt Rafmagn og rafmagnsnotkun er skráð.</span><span class="sxs-lookup"><span data-stu-id="58049-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="58049-228">Sjálfgefið er að öll tölfræðileg víddarstök verða tiltæk sem úthlutunargrunnur.</span><span class="sxs-lookup"><span data-stu-id="58049-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58049-229">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-229">Cost object</span></span></th>
<th><span data-ttu-id="58049-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="58049-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-231">CC001</span><span class="sxs-lookup"><span data-stu-id="58049-231">CC001</span></span></td>
<td><span data-ttu-id="58049-232">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58049-232">HR</span></span></td>
<td><span data-ttu-id="58049-233">1.000</span><span class="sxs-lookup"><span data-stu-id="58049-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-234">CC002</span><span class="sxs-lookup"><span data-stu-id="58049-234">CC002</span></span></td>
<td><span data-ttu-id="58049-235">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58049-235">Finance</span></span></td>
<td><span data-ttu-id="58049-236">6,000</span><span class="sxs-lookup"><span data-stu-id="58049-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-237">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-237">CC003</span></span></td>
<td><span data-ttu-id="58049-238">Smölun</span><span class="sxs-lookup"><span data-stu-id="58049-238">Assembly</span></span></td>
<td><span data-ttu-id="58049-239">0</span><span class="sxs-lookup"><span data-stu-id="58049-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58049-240">Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunni fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="58049-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58049-241">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-241">Cost object</span></span></th>
<th><span data-ttu-id="58049-242">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="58049-242">Magnitude</span></span></th>
<th><span data-ttu-id="58049-243">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="58049-243">Allocation factor</span></span></th>
<th><span data-ttu-id="58049-244">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58049-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-245">CC001</span><span class="sxs-lookup"><span data-stu-id="58049-245">CC001</span></span></td>
<td><span data-ttu-id="58049-246">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58049-246">HR</span></span></td>
<td><span data-ttu-id="58049-247">1.000</span><span class="sxs-lookup"><span data-stu-id="58049-247">1,000</span></span></td>
<td><span data-ttu-id="58049-248">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="58049-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="58049-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="58049-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-250">CC002</span><span class="sxs-lookup"><span data-stu-id="58049-250">CC002</span></span></td>
<td><span data-ttu-id="58049-251">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58049-251">Finance</span></span></td>
<td><span data-ttu-id="58049-252">6,000</span><span class="sxs-lookup"><span data-stu-id="58049-252">6,000</span></span></td>
<td><span data-ttu-id="58049-253">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="58049-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="58049-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="58049-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-255">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-255">CC003</span></span></td>
<td><span data-ttu-id="58049-256">Smölun</span><span class="sxs-lookup"><span data-stu-id="58049-256">Assembly</span></span></td>
<td><span data-ttu-id="58049-257">0</span><span class="sxs-lookup"><span data-stu-id="58049-257">0</span></span></td>
<td><span data-ttu-id="58049-258">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="58049-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="58049-259">0,00</span><span class="sxs-lookup"><span data-stu-id="58049-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58049-260">Föstum kostnaði þarf að dreifa jafnt á staka kostnaðarhluti sem hafa notað rafmagn.</span><span class="sxs-lookup"><span data-stu-id="58049-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="58049-261">Hægt er að ná þessa niðurstöðu með því að nota tölfræðilegt víddarstakið Rafmagn í úthlutunargrunni reikniformúlu: (Rafmagn &gt; 0,00) Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunn fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="58049-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58049-262">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-262">Cost object</span></span></th>
<th><span data-ttu-id="58049-263">Formúla</span><span class="sxs-lookup"><span data-stu-id="58049-263">Formula</span></span></th>
<th><span data-ttu-id="58049-264">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="58049-264">Magnitude</span></span></th>
<th><span data-ttu-id="58049-265">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="58049-265">Allocation factor</span></span></th>
<th><span data-ttu-id="58049-266">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58049-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-267">CC001</span><span class="sxs-lookup"><span data-stu-id="58049-267">CC001</span></span></td>
<td><span data-ttu-id="58049-268">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58049-268">HR</span></span></td>
<td><span data-ttu-id="58049-269">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="58049-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="58049-270">1</span><span class="sxs-lookup"><span data-stu-id="58049-270">1</span></span></td>
<td><span data-ttu-id="58049-271">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="58049-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="58049-272">500,00</span><span class="sxs-lookup"><span data-stu-id="58049-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-273">CC002</span><span class="sxs-lookup"><span data-stu-id="58049-273">CC002</span></span></td>
<td><span data-ttu-id="58049-274">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58049-274">Finance</span></span></td>
<td><span data-ttu-id="58049-275">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="58049-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="58049-276">1</span><span class="sxs-lookup"><span data-stu-id="58049-276">1</span></span></td>
<td><span data-ttu-id="58049-277">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="58049-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="58049-278">500,00</span><span class="sxs-lookup"><span data-stu-id="58049-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-279">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-279">CC003</span></span></td>
<td><span data-ttu-id="58049-280">Smölun</span><span class="sxs-lookup"><span data-stu-id="58049-280">Assembly</span></span></td>
<td><span data-ttu-id="58049-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="58049-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="58049-282">0</span><span class="sxs-lookup"><span data-stu-id="58049-282">0</span></span></td>
<td><span data-ttu-id="58049-283">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="58049-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="58049-284">0,00</span><span class="sxs-lookup"><span data-stu-id="58049-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="58049-285">Færslubók</span><span class="sxs-lookup"><span data-stu-id="58049-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="58049-286">Færslubók</span><span class="sxs-lookup"><span data-stu-id="58049-286">Journal</span></span></th>
<th><span data-ttu-id="58049-287">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="58049-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="58049-288">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="58049-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="58049-289">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="58049-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-290">00002</span><span class="sxs-lookup"><span data-stu-id="58049-290">00002</span></span></td>
<td><span data-ttu-id="58049-291">Útreikningabók kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="58049-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="58049-292">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="58049-292">Fiscal</span></span></td>
<td><span data-ttu-id="58049-293">2017</span><span class="sxs-lookup"><span data-stu-id="58049-293">2017</span></span></td>
<td><span data-ttu-id="58049-294">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="58049-294">Period 1</span></span></td>
<td><span data-ttu-id="58049-295">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="58049-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="58049-296">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="58049-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="58049-297">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="58049-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="58049-298">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="58049-299">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58049-299">Cost element</span></span></th>
<th><span data-ttu-id="58049-300">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58049-300">Cost behavior</span></span></th>
<th><span data-ttu-id="58049-301">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58049-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-302">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="58049-303">CC099</span><span class="sxs-lookup"><span data-stu-id="58049-303">CC099</span></span></td>
<td><span data-ttu-id="58049-304">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58049-304">Default cost center</span></span></td>
<td><span data-ttu-id="58049-305">10001</span><span class="sxs-lookup"><span data-stu-id="58049-305">10001</span></span></td>
<td><span data-ttu-id="58049-306">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-306">Electricity</span></span></td>
<td><span data-ttu-id="58049-307">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-307">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-308">1.000,00</span><span class="sxs-lookup"><span data-stu-id="58049-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-309">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="58049-310">CC099</span><span class="sxs-lookup"><span data-stu-id="58049-310">CC099</span></span></td>
<td><span data-ttu-id="58049-311">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58049-311">Default cost center</span></span></td>
<td><span data-ttu-id="58049-312">10001</span><span class="sxs-lookup"><span data-stu-id="58049-312">10001</span></span></td>
<td><span data-ttu-id="58049-313">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-313">Electricity</span></span></td>
<td><span data-ttu-id="58049-314">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-314">Variable cost</span></span></td>
<td><span data-ttu-id="58049-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="58049-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="58049-316">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="58049-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58049-317">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="58049-318">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58049-318">Cost element</span></span></th>
<th><span data-ttu-id="58049-319">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58049-319">Cost behavior</span></span></th>
<th><span data-ttu-id="58049-320">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58049-320">Amount</span></span></th>
<th><span data-ttu-id="58049-321">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="58049-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-322">CC099</span><span class="sxs-lookup"><span data-stu-id="58049-322">CC099</span></span></td>
<td><span data-ttu-id="58049-323">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58049-323">Default cost center</span></span></td>
<td><span data-ttu-id="58049-324">10001</span><span class="sxs-lookup"><span data-stu-id="58049-324">10001</span></span></td>
<td><span data-ttu-id="58049-325">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-325">Electricity</span></span></td>
<td><span data-ttu-id="58049-326">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-326">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-327">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="58049-327">-1,000.00</span></span></td>
<td><span data-ttu-id="58049-328">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-329">CC001</span><span class="sxs-lookup"><span data-stu-id="58049-329">CC001</span></span></td>
<td><span data-ttu-id="58049-330">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58049-330">HR</span></span></td>
<td><span data-ttu-id="58049-331">10001</span><span class="sxs-lookup"><span data-stu-id="58049-331">10001</span></span></td>
<td><span data-ttu-id="58049-332">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-332">Electricity</span></span></td>
<td><span data-ttu-id="58049-333">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-333">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-334">500,00</span><span class="sxs-lookup"><span data-stu-id="58049-334">500.00</span></span></td>
<td><span data-ttu-id="58049-335">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-336">CC002</span><span class="sxs-lookup"><span data-stu-id="58049-336">CC002</span></span></td>
<td><span data-ttu-id="58049-337">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58049-337">Finance</span></span></td>
<td><span data-ttu-id="58049-338">10001</span><span class="sxs-lookup"><span data-stu-id="58049-338">10001</span></span></td>
<td><span data-ttu-id="58049-339">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-339">Electricity</span></span></td>
<td><span data-ttu-id="58049-340">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-340">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-341">500,00</span><span class="sxs-lookup"><span data-stu-id="58049-341">500.00</span></span></td>
<td><span data-ttu-id="58049-342">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-343">CC099</span><span class="sxs-lookup"><span data-stu-id="58049-343">CC099</span></span></td>
<td><span data-ttu-id="58049-344">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58049-344">Default cost center</span></span></td>
<td><span data-ttu-id="58049-345">10001</span><span class="sxs-lookup"><span data-stu-id="58049-345">10001</span></span></td>
<td><span data-ttu-id="58049-346">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-346">Electricity</span></span></td>
<td><span data-ttu-id="58049-347">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-347">Variable cost</span></span></td>
<td><span data-ttu-id="58049-348">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="58049-348">-9,000.00</span></span></td>
<td><span data-ttu-id="58049-349">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-350">CC001</span><span class="sxs-lookup"><span data-stu-id="58049-350">CC001</span></span></td>
<td><span data-ttu-id="58049-351">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58049-351">HR</span></span></td>
<td><span data-ttu-id="58049-352">10001</span><span class="sxs-lookup"><span data-stu-id="58049-352">10001</span></span></td>
<td><span data-ttu-id="58049-353">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-353">Electricity</span></span></td>
<td><span data-ttu-id="58049-354">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-354">Variable cost</span></span></td>
<td><span data-ttu-id="58049-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="58049-355">1,285.71</span></span></td>
<td><span data-ttu-id="58049-356">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-357">CC002</span><span class="sxs-lookup"><span data-stu-id="58049-357">CC002</span></span></td>
<td><span data-ttu-id="58049-358">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58049-358">Finance</span></span></td>
<td><span data-ttu-id="58049-359">10001</span><span class="sxs-lookup"><span data-stu-id="58049-359">10001</span></span></td>
<td><span data-ttu-id="58049-360">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-360">Electricity</span></span></td>
<td><span data-ttu-id="58049-361">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-361">Variable cost</span></span></td>
<td><span data-ttu-id="58049-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="58049-362">7,714.29</span></span></td>
<td><span data-ttu-id="58049-363">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58049-364">Nákvæmar upplýsingar um kostnaðardreifingu og úthlutunargrunna er að finna í Kostnaðardreifingarreglu og úthlutunargrunnum.</span><span class="sxs-lookup"><span data-stu-id="58049-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="58049-365">(Athugaðu að þetta efnisatriði hefur ekki enn verið fullklárað en er væntanlegt.)</span><span class="sxs-lookup"><span data-stu-id="58049-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="58049-366">Skref 3: Keyra útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="58049-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="58049-367">Sameiginlegur kostnaður er notaður til að rukka einn eða fleiri tilgreinda kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="58049-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="58049-368">Gjöldin byggjast á fyrirframákveðnu kostnaðarhlutfalli og mæligildi úr úthlutuðum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="58049-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="58049-369">Skilgreina sameiginlegan kostnað</span><span class="sxs-lookup"><span data-stu-id="58049-369">Define the overhead rate</span></span>

<span data-ttu-id="58049-370">Kostnaðarhlutur CC001 Mannauður stuðlar að safni innri verka.</span><span class="sxs-lookup"><span data-stu-id="58049-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="58049-371">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsverk til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="58049-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58049-372">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-372">Cost object</span></span></th>
<th><span data-ttu-id="58049-373">Tímar</span><span class="sxs-lookup"><span data-stu-id="58049-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-374">Verk 1</span><span class="sxs-lookup"><span data-stu-id="58049-374">Proj 1</span></span></td>
<td><span data-ttu-id="58049-375">Verk 1</span><span class="sxs-lookup"><span data-stu-id="58049-375">Project 1</span></span></td>
<td><span data-ttu-id="58049-376">3</span><span class="sxs-lookup"><span data-stu-id="58049-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-377">Verk 2</span><span class="sxs-lookup"><span data-stu-id="58049-377">Proj 2</span></span></td>
<td><span data-ttu-id="58049-378">Verk 2</span><span class="sxs-lookup"><span data-stu-id="58049-378">Project 2</span></span></td>
<td><span data-ttu-id="58049-379">1</span><span class="sxs-lookup"><span data-stu-id="58049-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58049-380">Fyrirframákveðið kostnaðarhlutfall fyrir kostnaðarframlag verk hefur verið skilgreint.</span><span class="sxs-lookup"><span data-stu-id="58049-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58049-381">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-381">Cost object</span></span></th>
<th><span data-ttu-id="58049-382">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58049-382">Cost element</span></span></th>
<th><span data-ttu-id="58049-383">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58049-383">Cost behavior</span></span></th>
<th><span data-ttu-id="58049-384">Einingar</span><span class="sxs-lookup"><span data-stu-id="58049-384">Units</span></span></th>
<th><span data-ttu-id="58049-385">Taxti</span><span class="sxs-lookup"><span data-stu-id="58049-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-386">CC001</span><span class="sxs-lookup"><span data-stu-id="58049-386">CC001</span></span></td>
<td><span data-ttu-id="58049-387">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58049-387">HR</span></span></td>
<td><span data-ttu-id="58049-388">10001</span><span class="sxs-lookup"><span data-stu-id="58049-388">10001</span></span></td>
<td><span data-ttu-id="58049-389">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-389">Variable cost</span></span></td>
<td><span data-ttu-id="58049-390">1</span><span class="sxs-lookup"><span data-stu-id="58049-390">1</span></span></td>
<td><span data-ttu-id="58049-391">10</span><span class="sxs-lookup"><span data-stu-id="58049-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58049-392">Eftirfarandi tafla sýnir niðurstöður þegar Mannauðsverk eru notuð sem grunnur við úthlutun.</span><span class="sxs-lookup"><span data-stu-id="58049-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58049-393">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-393">Cost object</span></span></th>
<th><span data-ttu-id="58049-394">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="58049-394">Magnitude</span></span></th>
<th><span data-ttu-id="58049-395">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58049-395">Cost element</span></span></th>
<th><span data-ttu-id="58049-396">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="58049-396">Allocation factor</span></span></th>
<th><span data-ttu-id="58049-397">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58049-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-398">Verk 1</span><span class="sxs-lookup"><span data-stu-id="58049-398">Proj 1</span></span></td>
<td><span data-ttu-id="58049-399">Verk 1</span><span class="sxs-lookup"><span data-stu-id="58049-399">Project 1</span></span></td>
<td><span data-ttu-id="58049-400">3</span><span class="sxs-lookup"><span data-stu-id="58049-400">3</span></span></td>
<td><span data-ttu-id="58049-401">10001</span><span class="sxs-lookup"><span data-stu-id="58049-401">10001</span></span></td>
<td><span data-ttu-id="58049-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="58049-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="58049-403">30,00</span><span class="sxs-lookup"><span data-stu-id="58049-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-404">Verk 2</span><span class="sxs-lookup"><span data-stu-id="58049-404">Proj 2</span></span></td>
<td><span data-ttu-id="58049-405">Verk 2</span><span class="sxs-lookup"><span data-stu-id="58049-405">Project 2</span></span></td>
<td><span data-ttu-id="58049-406">1</span><span class="sxs-lookup"><span data-stu-id="58049-406">1</span></span></td>
<td><span data-ttu-id="58049-407">10001</span><span class="sxs-lookup"><span data-stu-id="58049-407">10001</span></span></td>
<td><span data-ttu-id="58049-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="58049-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="58049-409">10,00</span><span class="sxs-lookup"><span data-stu-id="58049-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="58049-410">Færslubók</span><span class="sxs-lookup"><span data-stu-id="58049-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="58049-411">Færslubók</span><span class="sxs-lookup"><span data-stu-id="58049-411">Journal</span></span></th>
<th><span data-ttu-id="58049-412">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="58049-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="58049-413">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="58049-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="58049-414">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="58049-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-415">00003</span><span class="sxs-lookup"><span data-stu-id="58049-415">00003</span></span></td>
<td><span data-ttu-id="58049-416">Færslubók fyrir útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="58049-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="58049-417">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="58049-417">Fiscal</span></span></td>
<td><span data-ttu-id="58049-418">2017</span><span class="sxs-lookup"><span data-stu-id="58049-418">2017</span></span></td>
<td><span data-ttu-id="58049-419">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="58049-419">Period 1</span></span></td>
<td><span data-ttu-id="58049-420">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="58049-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="58049-421">Bókarfærslur (Bókarfærslur fyrir útreikning sameiginlegs kostnaðar)</span><span class="sxs-lookup"><span data-stu-id="58049-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="58049-422">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="58049-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="58049-423">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-423">Cost object</span></span></th>
<th><span data-ttu-id="58049-424">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="58049-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-425">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="58049-426">Verk 1</span><span class="sxs-lookup"><span data-stu-id="58049-426">Proj 1</span></span></td>
<td><span data-ttu-id="58049-427">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="58049-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="58049-428">3,00</span><span class="sxs-lookup"><span data-stu-id="58049-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-429">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="58049-430">Verk 2</span><span class="sxs-lookup"><span data-stu-id="58049-430">Proj 2</span></span></td>
<td><span data-ttu-id="58049-431">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="58049-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="58049-432">1,00</span><span class="sxs-lookup"><span data-stu-id="58049-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="58049-433">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="58049-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58049-434">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="58049-435">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58049-435">Cost element</span></span></th>
<th><span data-ttu-id="58049-436">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58049-436">Cost behavior</span></span></th>
<th><span data-ttu-id="58049-437">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58049-437">Amount</span></span></th>
<th><span data-ttu-id="58049-438">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="58049-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="58049-439">CC0001</span></span></td>
<td><span data-ttu-id="58049-440">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58049-440">HR</span></span></td>
<td><span data-ttu-id="58049-441">10001</span><span class="sxs-lookup"><span data-stu-id="58049-441">10001</span></span></td>
<td><span data-ttu-id="58049-442">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-442">Electricity</span></span></td>
<td><span data-ttu-id="58049-443">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-443">Variable cost</span></span></td>
<td><span data-ttu-id="58049-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="58049-444">-30.00</span></span></td>
<td><span data-ttu-id="58049-445">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-446">Verk 1</span><span class="sxs-lookup"><span data-stu-id="58049-446">Proj 1</span></span></td>
<td><span data-ttu-id="58049-447">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="58049-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="58049-448">10001</span><span class="sxs-lookup"><span data-stu-id="58049-448">10001</span></span></td>
<td><span data-ttu-id="58049-449">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-449">Electricity</span></span></td>
<td><span data-ttu-id="58049-450">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-450">Variable cost</span></span></td>
<td><span data-ttu-id="58049-451">30,00</span><span class="sxs-lookup"><span data-stu-id="58049-451">30.00</span></span></td>
<td><span data-ttu-id="58049-452">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-453">CC001</span><span class="sxs-lookup"><span data-stu-id="58049-453">CC001</span></span></td>
<td><span data-ttu-id="58049-454">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58049-454">HR</span></span></td>
<td><span data-ttu-id="58049-455">10001</span><span class="sxs-lookup"><span data-stu-id="58049-455">10001</span></span></td>
<td><span data-ttu-id="58049-456">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-456">Electricity</span></span></td>
<td><span data-ttu-id="58049-457">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-457">Variable cost</span></span></td>
<td><span data-ttu-id="58049-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="58049-458">-10.00</span></span></td>
<td><span data-ttu-id="58049-459">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-460">Verk 2</span><span class="sxs-lookup"><span data-stu-id="58049-460">Proj 2</span></span></td>
<td><span data-ttu-id="58049-461">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="58049-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="58049-462">10001</span><span class="sxs-lookup"><span data-stu-id="58049-462">10001</span></span></td>
<td><span data-ttu-id="58049-463">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-463">Electricity</span></span></td>
<td><span data-ttu-id="58049-464">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-464">Variable cost</span></span></td>
<td><span data-ttu-id="58049-465">10,00</span><span class="sxs-lookup"><span data-stu-id="58049-465">10.00</span></span></td>
<td><span data-ttu-id="58049-466">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58049-467">Nákvæmar upplýsingar um reglu sameiginlegs kostnaðar er að finna í Reglu fyrir sameiginlegan kostnað og úthlutunargrunnum.</span><span class="sxs-lookup"><span data-stu-id="58049-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="58049-468">(Athugaðu að þetta efnisatriði hefur ekki enn verið fullklárað en er væntanlegt.)</span><span class="sxs-lookup"><span data-stu-id="58049-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="58049-469">Skref 4: Keyra útreikning kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="58049-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="58049-470">Úthlutun er notuð til að úthluta stöðu kostnaðarhlutar í öðrum kostnaðarhlutum með því að nota úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="58049-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="58049-471">Finance and Operations styður gagnvirka úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="58049-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="58049-472">Í gagnvirkri úthlutunaraðferð er sú sameiginlega þjónusta sem hjálparkostnaðarhlutir skiptast á viðurkennd að fullu.</span><span class="sxs-lookup"><span data-stu-id="58049-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="58049-473">Kerfið ákvarðar sjálfkrafa rétta röð til að framkvæma úthlutun eftir.</span><span class="sxs-lookup"><span data-stu-id="58049-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="58049-474">Stöðu kostnaðarhluta er úthlutað með einum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="58049-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="58049-475">Úthlutanir þvert á víddir kostnaðarhluta og viðkomandi stök þeirra eru studdar.</span><span class="sxs-lookup"><span data-stu-id="58049-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="58049-476">Úthlutun pöntunarinnar er stjórnað af stýrieiningu kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="58049-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="58049-477">[![Gagnkvæm aðferð](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="58049-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="58049-478">Tilgreinið kostnaðarúthlutun</span><span class="sxs-lookup"><span data-stu-id="58049-478">Define the cost allocation</span></span>

<span data-ttu-id="58049-479">Hér er einfalt dæmi sem útskýrir hvernig hægt er að rekja flæði kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="58049-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="58049-480">Kostnaðarhlutir CC001 Mannauður leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="58049-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="58049-481">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="58049-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58049-482">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-482">Cost object</span></span></th>
<th><span data-ttu-id="58049-483">Mannauðsþjónusta</span><span class="sxs-lookup"><span data-stu-id="58049-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-484">CC002</span><span class="sxs-lookup"><span data-stu-id="58049-484">CC002</span></span></td>
<td><span data-ttu-id="58049-485">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58049-485">Finance</span></span></td>
<td><span data-ttu-id="58049-486">35</span><span class="sxs-lookup"><span data-stu-id="58049-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-487">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-487">CC003</span></span></td>
<td><span data-ttu-id="58049-488">Smölun</span><span class="sxs-lookup"><span data-stu-id="58049-488">Assembly</span></span></td>
<td><span data-ttu-id="58049-489">55</span><span class="sxs-lookup"><span data-stu-id="58049-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-490">CC004</span><span class="sxs-lookup"><span data-stu-id="58049-490">CC004</span></span></td>
<td><span data-ttu-id="58049-491">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58049-491">Packaging</span></span></td>
<td><span data-ttu-id="58049-492">10</span><span class="sxs-lookup"><span data-stu-id="58049-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58049-493">Kostnaðarhlutir CC002 Fjármál leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="58049-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="58049-494">Stofnað er tölfræðilegt víddarstak sem kallast Fjármálaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="58049-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58049-495">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-495">Cost object</span></span></th>
<th><span data-ttu-id="58049-496">Fjármálaþjónusta</span><span class="sxs-lookup"><span data-stu-id="58049-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-497">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-497">CC003</span></span></td>
<td><span data-ttu-id="58049-498">Smölun</span><span class="sxs-lookup"><span data-stu-id="58049-498">Assembly</span></span></td>
<td><span data-ttu-id="58049-499">65</span><span class="sxs-lookup"><span data-stu-id="58049-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-500">CC004</span><span class="sxs-lookup"><span data-stu-id="58049-500">CC004</span></span></td>
<td><span data-ttu-id="58049-501">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58049-501">Packaging</span></span></td>
<td><span data-ttu-id="58049-502">35</span><span class="sxs-lookup"><span data-stu-id="58049-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58049-503">Kostnaðarhlutir CC003 Samsetning leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="58049-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="58049-504">Meðlimur tölfræðilega víddar sem kallast Mannauður verk er stofnað til að mælvíddarstaka notuðum magnitude.</span><span class="sxs-lookup"><span data-stu-id="58049-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58049-505">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-505">Cost object</span></span></th>
<th><span data-ttu-id="58049-506">Samsetningarþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="58049-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-507">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-507">Prod 1</span></span></td>
<td><span data-ttu-id="58049-508">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-508">Product 1</span></span></td>
<td><span data-ttu-id="58049-509">60</span><span class="sxs-lookup"><span data-stu-id="58049-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-510">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-510">Prod 2</span></span></td>
<td><span data-ttu-id="58049-511">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-511">Product 2</span></span></td>
<td><span data-ttu-id="58049-512">20</span><span class="sxs-lookup"><span data-stu-id="58049-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58049-513">Kostnaðarhlutir CC004 Umbúðir leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="58049-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="58049-514">Stofnað er tölfræðilegt víddarstak sem kallast Umbúðaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="58049-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58049-515">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-515">Cost object</span></span></th>
<th><span data-ttu-id="58049-516">Umbúðaþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="58049-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-517">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-517">Prod 1</span></span></td>
<td><span data-ttu-id="58049-518">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-518">Product 1</span></span></td>
<td><span data-ttu-id="58049-519">80</span><span class="sxs-lookup"><span data-stu-id="58049-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-520">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-520">Prod 2</span></span></td>
<td><span data-ttu-id="58049-521">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-521">Product 2</span></span></td>
<td><span data-ttu-id="58049-522">sept</span><span class="sxs-lookup"><span data-stu-id="58049-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58049-523">**Athugið:** Í Finance and Operations er hægt að afleiða tölfræðiaðgerðir eins og framleiðslutíma sem vara notar frá upprunagögnum.</span><span class="sxs-lookup"><span data-stu-id="58049-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="58049-524">Ítarlegri upplýsingar um veitur tölfræðiaðgerðar er að finna í Veitusniðmáti tölfræðiaðgerðar.</span><span class="sxs-lookup"><span data-stu-id="58049-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="58049-525">(Athugið að þetta efnisatriði er ekki enn fullklárað en er væntanlegt.) Eftirfarandi tafla sýnir niðurstöður þegar Mannauðsþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="58049-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58049-526">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-526">Cost object</span></span></th>
<th><span data-ttu-id="58049-527">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="58049-527">Magnitude</span></span></th>
<th><span data-ttu-id="58049-528">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="58049-528">Allocation factor</span></span></th>
<th><span data-ttu-id="58049-529">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58049-529">Amount</span></span></th>
<th><span data-ttu-id="58049-530">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58049-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-531">CC002</span><span class="sxs-lookup"><span data-stu-id="58049-531">CC002</span></span></td>
<td><span data-ttu-id="58049-532">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58049-532">Finance</span></span></td>
<td><span data-ttu-id="58049-533">35</span><span class="sxs-lookup"><span data-stu-id="58049-533">35</span></span></td>
<td><span data-ttu-id="58049-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="58049-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="58049-535">175.00</span><span class="sxs-lookup"><span data-stu-id="58049-535">175.00</span></span></td>
<td><span data-ttu-id="58049-536">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-537">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-537">CC003</span></span></td>
<td><span data-ttu-id="58049-538">Smölun</span><span class="sxs-lookup"><span data-stu-id="58049-538">Assembly</span></span></td>
<td><span data-ttu-id="58049-539">55</span><span class="sxs-lookup"><span data-stu-id="58049-539">55</span></span></td>
<td><span data-ttu-id="58049-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="58049-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="58049-541">275.00</span><span class="sxs-lookup"><span data-stu-id="58049-541">275.00</span></span></td>
<td><span data-ttu-id="58049-542">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-543">CC004</span><span class="sxs-lookup"><span data-stu-id="58049-543">CC004</span></span></td>
<td><span data-ttu-id="58049-544">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58049-544">Packaging</span></span></td>
<td><span data-ttu-id="58049-545">10</span><span class="sxs-lookup"><span data-stu-id="58049-545">10</span></span></td>
<td><span data-ttu-id="58049-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="58049-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="58049-547">50,00</span><span class="sxs-lookup"><span data-stu-id="58049-547">50.00</span></span></td>
<td><span data-ttu-id="58049-548">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-549">CC002</span><span class="sxs-lookup"><span data-stu-id="58049-549">CC002</span></span></td>
<td><span data-ttu-id="58049-550">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58049-550">Finance</span></span></td>
<td><span data-ttu-id="58049-551">35</span><span class="sxs-lookup"><span data-stu-id="58049-551">35</span></span></td>
<td><span data-ttu-id="58049-552">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="58049-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="58049-553">436.00</span><span class="sxs-lookup"><span data-stu-id="58049-553">436.00</span></span></td>
<td><span data-ttu-id="58049-554">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-555">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-555">CC003</span></span></td>
<td><span data-ttu-id="58049-556">Smölun</span><span class="sxs-lookup"><span data-stu-id="58049-556">Assembly</span></span></td>
<td><span data-ttu-id="58049-557">55</span><span class="sxs-lookup"><span data-stu-id="58049-557">55</span></span></td>
<td><span data-ttu-id="58049-558">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="58049-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="58049-559">685.14</span><span class="sxs-lookup"><span data-stu-id="58049-559">685.14</span></span></td>
<td><span data-ttu-id="58049-560">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-561">CC004</span><span class="sxs-lookup"><span data-stu-id="58049-561">CC004</span></span></td>
<td><span data-ttu-id="58049-562">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58049-562">Packaging</span></span></td>
<td><span data-ttu-id="58049-563">10</span><span class="sxs-lookup"><span data-stu-id="58049-563">10</span></span></td>
<td><span data-ttu-id="58049-564">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="58049-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="58049-565">124.57</span><span class="sxs-lookup"><span data-stu-id="58049-565">124.57</span></span></td>
<td><span data-ttu-id="58049-566">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58049-567">Eftirfarandi tafla sýnir niðurstöður þegar Fjármálaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="58049-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58049-568">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-568">Cost object</span></span></th>
<th><span data-ttu-id="58049-569">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="58049-569">Magnitude</span></span></th>
<th><span data-ttu-id="58049-570">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="58049-570">Allocation factor</span></span></th>
<th><span data-ttu-id="58049-571">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58049-571">Amount</span></span></th>
<th><span data-ttu-id="58049-572">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58049-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-573">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-573">CC003</span></span></td>
<td><span data-ttu-id="58049-574">Smölun</span><span class="sxs-lookup"><span data-stu-id="58049-574">Assembly</span></span></td>
<td><span data-ttu-id="58049-575">65</span><span class="sxs-lookup"><span data-stu-id="58049-575">65</span></span></td>
<td><span data-ttu-id="58049-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="58049-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="58049-577">438.75</span><span class="sxs-lookup"><span data-stu-id="58049-577">438.75</span></span></td>
<td><span data-ttu-id="58049-578">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-579">CC004</span><span class="sxs-lookup"><span data-stu-id="58049-579">CC004</span></span></td>
<td><span data-ttu-id="58049-580">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58049-580">Packaging</span></span></td>
<td><span data-ttu-id="58049-581">35</span><span class="sxs-lookup"><span data-stu-id="58049-581">35</span></span></td>
<td><span data-ttu-id="58049-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="58049-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="58049-583">236.25</span><span class="sxs-lookup"><span data-stu-id="58049-583">236.25</span></span></td>
<td><span data-ttu-id="58049-584">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-585">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-585">CC003</span></span></td>
<td><span data-ttu-id="58049-586">Smölun</span><span class="sxs-lookup"><span data-stu-id="58049-586">Assembly</span></span></td>
<td><span data-ttu-id="58049-587">65</span><span class="sxs-lookup"><span data-stu-id="58049-587">65</span></span></td>
<td><span data-ttu-id="58049-588">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="58049-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="58049-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="58049-589">5,297.69</span></span></td>
<td><span data-ttu-id="58049-590">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-591">CC004</span><span class="sxs-lookup"><span data-stu-id="58049-591">CC004</span></span></td>
<td><span data-ttu-id="58049-592">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58049-592">Packaging</span></span></td>
<td><span data-ttu-id="58049-593">35</span><span class="sxs-lookup"><span data-stu-id="58049-593">35</span></span></td>
<td><span data-ttu-id="58049-594">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="58049-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="58049-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="58049-595">2,852.60</span></span></td>
<td><span data-ttu-id="58049-596">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58049-597">Eftirfarandi tafla sýnir niðurstöður þegar Samsetningarþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="58049-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58049-598">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-598">Cost object</span></span></th>
<th><span data-ttu-id="58049-599">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="58049-599">Magnitude</span></span></th>
<th><span data-ttu-id="58049-600">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="58049-600">Allocation factor</span></span></th>
<th><span data-ttu-id="58049-601">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58049-601">Amount</span></span></th>
<th><span data-ttu-id="58049-602">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58049-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-603">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-603">Prod 1</span></span></td>
<td><span data-ttu-id="58049-604">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-604">Product 1</span></span></td>
<td><span data-ttu-id="58049-605">60</span><span class="sxs-lookup"><span data-stu-id="58049-605">60</span></span></td>
<td><span data-ttu-id="58049-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="58049-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="58049-607">535.31</span><span class="sxs-lookup"><span data-stu-id="58049-607">535.31</span></span></td>
<td><span data-ttu-id="58049-608">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-609">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-609">Prod 2</span></span></td>
<td><span data-ttu-id="58049-610">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-610">Product 2</span></span></td>
<td><span data-ttu-id="58049-611">20</span><span class="sxs-lookup"><span data-stu-id="58049-611">20</span></span></td>
<td><span data-ttu-id="58049-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="58049-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="58049-613">178.44</span><span class="sxs-lookup"><span data-stu-id="58049-613">178.44</span></span></td>
<td><span data-ttu-id="58049-614">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-615">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-615">Prod 1</span></span></td>
<td><span data-ttu-id="58049-616">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-616">Product 1</span></span></td>
<td><span data-ttu-id="58049-617">60</span><span class="sxs-lookup"><span data-stu-id="58049-617">60</span></span></td>
<td><span data-ttu-id="58049-618">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="58049-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="58049-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="58049-619">4,487.12</span></span></td>
<td><span data-ttu-id="58049-620">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-621">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-621">Prod 2</span></span></td>
<td><span data-ttu-id="58049-622">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-622">Product 2</span></span></td>
<td><span data-ttu-id="58049-623">20</span><span class="sxs-lookup"><span data-stu-id="58049-623">20</span></span></td>
<td><span data-ttu-id="58049-624">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="58049-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="58049-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="58049-625">1,495.71</span></span></td>
<td><span data-ttu-id="58049-626">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58049-627">Eftirfarandi tafla sýnir niðurstöður þegar Umbúðaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="58049-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58049-628">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-628">Cost object</span></span></th>
<th><span data-ttu-id="58049-629">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="58049-629">Magnitude</span></span></th>
<th><span data-ttu-id="58049-630">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="58049-630">Allocation factor</span></span></th>
<th><span data-ttu-id="58049-631">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58049-631">Amount</span></span></th>
<th><span data-ttu-id="58049-632">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58049-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-633">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-633">Prod 1</span></span></td>
<td><span data-ttu-id="58049-634">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-634">Product 1</span></span></td>
<td><span data-ttu-id="58049-635">80</span><span class="sxs-lookup"><span data-stu-id="58049-635">80</span></span></td>
<td><span data-ttu-id="58049-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="58049-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="58049-637">241.05</span><span class="sxs-lookup"><span data-stu-id="58049-637">241.05</span></span></td>
<td><span data-ttu-id="58049-638">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-639">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-639">Prod 2</span></span></td>
<td><span data-ttu-id="58049-640">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-640">Product 2</span></span></td>
<td><span data-ttu-id="58049-641">15</span><span class="sxs-lookup"><span data-stu-id="58049-641">15</span></span></td>
<td><span data-ttu-id="58049-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="58049-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="58049-643">45.20</span><span class="sxs-lookup"><span data-stu-id="58049-643">45.20</span></span></td>
<td><span data-ttu-id="58049-644">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-645">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-645">Prod 1</span></span></td>
<td><span data-ttu-id="58049-646">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-646">Product 1</span></span></td>
<td><span data-ttu-id="58049-647">80</span><span class="sxs-lookup"><span data-stu-id="58049-647">80</span></span></td>
<td><span data-ttu-id="58049-648">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="58049-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="58049-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="58049-649">2,507.09</span></span></td>
<td><span data-ttu-id="58049-650">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-651">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-651">Prod 2</span></span></td>
<td><span data-ttu-id="58049-652">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-652">Product 2</span></span></td>
<td><span data-ttu-id="58049-653">15</span><span class="sxs-lookup"><span data-stu-id="58049-653">15</span></span></td>
<td><span data-ttu-id="58049-654">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="58049-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="58049-655">470.08</span><span class="sxs-lookup"><span data-stu-id="58049-655">470.08</span></span></td>
<td><span data-ttu-id="58049-656">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="58049-657">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="58049-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="58049-658">Færslubók</span><span class="sxs-lookup"><span data-stu-id="58049-658">Journal</span></span></th>
<th><span data-ttu-id="58049-659">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="58049-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="58049-660">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="58049-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="58049-661">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="58049-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-662">00004</span><span class="sxs-lookup"><span data-stu-id="58049-662">00004</span></span></td>
<td><span data-ttu-id="58049-663">Færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="58049-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="58049-664">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="58049-664">Fiscal</span></span></td>
<td><span data-ttu-id="58049-665">2017</span><span class="sxs-lookup"><span data-stu-id="58049-665">2017</span></span></td>
<td><span data-ttu-id="58049-666">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="58049-666">Period 1</span></span></td>
<td><span data-ttu-id="58049-667">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="58049-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="58049-668">Færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="58049-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="58049-669">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="58049-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="58049-670">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="58049-671">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58049-671">Cost element</span></span></th>
<th><span data-ttu-id="58049-672">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58049-672">Cost behavior</span></span></th>
<th><span data-ttu-id="58049-673">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58049-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-674">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="58049-675">CC001</span><span class="sxs-lookup"><span data-stu-id="58049-675">CC001</span></span></td>
<td><span data-ttu-id="58049-676">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58049-676">HR</span></span></td>
<td><span data-ttu-id="58049-677">10001</span><span class="sxs-lookup"><span data-stu-id="58049-677">10001</span></span></td>
<td><span data-ttu-id="58049-678">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-678">Electricity</span></span></td>
<td><span data-ttu-id="58049-679">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-679">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-680">500,00</span><span class="sxs-lookup"><span data-stu-id="58049-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-681">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="58049-682">CC001</span><span class="sxs-lookup"><span data-stu-id="58049-682">CC001</span></span></td>
<td><span data-ttu-id="58049-683">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58049-683">HR</span></span></td>
<td><span data-ttu-id="58049-684">10001</span><span class="sxs-lookup"><span data-stu-id="58049-684">10001</span></span></td>
<td><span data-ttu-id="58049-685">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-685">Electricity</span></span></td>
<td><span data-ttu-id="58049-686">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-686">Variable cost</span></span></td>
<td><span data-ttu-id="58049-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="58049-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-688">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="58049-689">CC002</span><span class="sxs-lookup"><span data-stu-id="58049-689">CC002</span></span></td>
<td><span data-ttu-id="58049-690">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58049-690">Finance</span></span></td>
<td><span data-ttu-id="58049-691">10001</span><span class="sxs-lookup"><span data-stu-id="58049-691">10001</span></span></td>
<td><span data-ttu-id="58049-692">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-692">Electricity</span></span></td>
<td><span data-ttu-id="58049-693">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-693">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-694">675.00</span><span class="sxs-lookup"><span data-stu-id="58049-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-695">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="58049-696">CC002</span><span class="sxs-lookup"><span data-stu-id="58049-696">CC002</span></span></td>
<td><span data-ttu-id="58049-697">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58049-697">Finance</span></span></td>
<td><span data-ttu-id="58049-698">10001</span><span class="sxs-lookup"><span data-stu-id="58049-698">10001</span></span></td>
<td><span data-ttu-id="58049-699">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-699">Electricity</span></span></td>
<td><span data-ttu-id="58049-700">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-700">Variable cost</span></span></td>
<td><span data-ttu-id="58049-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="58049-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-702">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="58049-703">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-703">CC003</span></span></td>
<td><span data-ttu-id="58049-704">Smölun</span><span class="sxs-lookup"><span data-stu-id="58049-704">Assembly</span></span></td>
<td><span data-ttu-id="58049-705">10001</span><span class="sxs-lookup"><span data-stu-id="58049-705">10001</span></span></td>
<td><span data-ttu-id="58049-706">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-706">Electricity</span></span></td>
<td><span data-ttu-id="58049-707">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-707">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-708">713.75</span><span class="sxs-lookup"><span data-stu-id="58049-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-709">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="58049-710">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-710">CC003</span></span></td>
<td><span data-ttu-id="58049-711">Smölun</span><span class="sxs-lookup"><span data-stu-id="58049-711">Assembly</span></span></td>
<td><span data-ttu-id="58049-712">10001</span><span class="sxs-lookup"><span data-stu-id="58049-712">10001</span></span></td>
<td><span data-ttu-id="58049-713">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-713">Electricity</span></span></td>
<td><span data-ttu-id="58049-714">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-714">Variable cost</span></span></td>
<td><span data-ttu-id="58049-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="58049-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-716">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="58049-717">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-717">CC003</span></span></td>
<td><span data-ttu-id="58049-718">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58049-718">Packaging</span></span></td>
<td><span data-ttu-id="58049-719">10001</span><span class="sxs-lookup"><span data-stu-id="58049-719">10001</span></span></td>
<td><span data-ttu-id="58049-720">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-720">Electricity</span></span></td>
<td><span data-ttu-id="58049-721">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-721">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-722">286.25</span><span class="sxs-lookup"><span data-stu-id="58049-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-723">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="58049-724">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-724">CC003</span></span></td>
<td><span data-ttu-id="58049-725">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58049-725">Packaging</span></span></td>
<td><span data-ttu-id="58049-726">10001</span><span class="sxs-lookup"><span data-stu-id="58049-726">10001</span></span></td>
<td><span data-ttu-id="58049-727">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-727">Electricity</span></span></td>
<td><span data-ttu-id="58049-728">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-728">Variable cost</span></span></td>
<td><span data-ttu-id="58049-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="58049-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-730">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="58049-731">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-731">Prod 1</span></span></td>
<td><span data-ttu-id="58049-732">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-732">Product 1</span></span></td>
<td><span data-ttu-id="58049-733">10001</span><span class="sxs-lookup"><span data-stu-id="58049-733">10001</span></span></td>
<td><span data-ttu-id="58049-734">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-734">Electricity</span></span></td>
<td><span data-ttu-id="58049-735">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-735">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-736">776.36</span><span class="sxs-lookup"><span data-stu-id="58049-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-737">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="58049-738">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-738">Prod 1</span></span></td>
<td><span data-ttu-id="58049-739">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-739">Product 1</span></span></td>
<td><span data-ttu-id="58049-740">10001</span><span class="sxs-lookup"><span data-stu-id="58049-740">10001</span></span></td>
<td><span data-ttu-id="58049-741">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-741">Electricity</span></span></td>
<td><span data-ttu-id="58049-742">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-742">Variable cost</span></span></td>
<td><span data-ttu-id="58049-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="58049-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-744">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="58049-745">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-745">Prod 2</span></span></td>
<td><span data-ttu-id="58049-746">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-746">Product 1</span></span></td>
<td><span data-ttu-id="58049-747">10001</span><span class="sxs-lookup"><span data-stu-id="58049-747">10001</span></span></td>
<td><span data-ttu-id="58049-748">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-748">Electricity</span></span></td>
<td><span data-ttu-id="58049-749">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-749">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-750">223.64</span><span class="sxs-lookup"><span data-stu-id="58049-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-751">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="58049-752">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-752">Prod 2</span></span></td>
<td><span data-ttu-id="58049-753">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-753">Product 1</span></span></td>
<td><span data-ttu-id="58049-754">10001</span><span class="sxs-lookup"><span data-stu-id="58049-754">10001</span></span></td>
<td><span data-ttu-id="58049-755">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-755">Electricity</span></span></td>
<td><span data-ttu-id="58049-756">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-756">Variable cost</span></span></td>
<td><span data-ttu-id="58049-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="58049-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="58049-758">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="58049-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58049-759">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="58049-760">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58049-760">Cost element</span></span></th>
<th><span data-ttu-id="58049-761">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58049-761">Cost behavior</span></span></th>
<th><span data-ttu-id="58049-762">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58049-762">Amount</span></span></th>
<th><span data-ttu-id="58049-763">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="58049-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58049-764">CC001</span><span class="sxs-lookup"><span data-stu-id="58049-764">CC001</span></span></td>
<td><span data-ttu-id="58049-765">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58049-765">HR</span></span></td>
<td><span data-ttu-id="58049-766">10001</span><span class="sxs-lookup"><span data-stu-id="58049-766">10001</span></span></td>
<td><span data-ttu-id="58049-767">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-767">Electricity</span></span></td>
<td><span data-ttu-id="58049-768">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-768">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="58049-769">-500.00</span></span></td>
<td><span data-ttu-id="58049-770">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-771">CC002</span><span class="sxs-lookup"><span data-stu-id="58049-771">CC002</span></span></td>
<td><span data-ttu-id="58049-772">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58049-772">Finance</span></span></td>
<td><span data-ttu-id="58049-773">10001</span><span class="sxs-lookup"><span data-stu-id="58049-773">10001</span></span></td>
<td><span data-ttu-id="58049-774">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-774">Electricity</span></span></td>
<td><span data-ttu-id="58049-775">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-775">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-776">175.00</span><span class="sxs-lookup"><span data-stu-id="58049-776">175.00</span></span></td>
<td><span data-ttu-id="58049-777">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-778">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-778">CC003</span></span></td>
<td><span data-ttu-id="58049-779">Smölun</span><span class="sxs-lookup"><span data-stu-id="58049-779">Assembly</span></span></td>
<td><span data-ttu-id="58049-780">10001</span><span class="sxs-lookup"><span data-stu-id="58049-780">10001</span></span></td>
<td><span data-ttu-id="58049-781">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-781">Electricity</span></span></td>
<td><span data-ttu-id="58049-782">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-782">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-783">275.00</span><span class="sxs-lookup"><span data-stu-id="58049-783">275.00</span></span></td>
<td><span data-ttu-id="58049-784">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-785">CC004</span><span class="sxs-lookup"><span data-stu-id="58049-785">CC004</span></span></td>
<td><span data-ttu-id="58049-786">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58049-786">Packaging</span></span></td>
<td><span data-ttu-id="58049-787">10001</span><span class="sxs-lookup"><span data-stu-id="58049-787">10001</span></span></td>
<td><span data-ttu-id="58049-788">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-788">Electricity</span></span></td>
<td><span data-ttu-id="58049-789">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-789">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-790">50,00</span><span class="sxs-lookup"><span data-stu-id="58049-790">50,00</span></span></td>
<td><span data-ttu-id="58049-791">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-792">CC001</span><span class="sxs-lookup"><span data-stu-id="58049-792">CC001</span></span></td>
<td><span data-ttu-id="58049-793">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58049-793">HR</span></span></td>
<td><span data-ttu-id="58049-794">10001</span><span class="sxs-lookup"><span data-stu-id="58049-794">10001</span></span></td>
<td><span data-ttu-id="58049-795">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-795">Electricity</span></span></td>
<td><span data-ttu-id="58049-796">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-796">Variable cost</span></span></td>
<td><span data-ttu-id="58049-797">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="58049-797">-1,245.71</span></span></td>
<td><span data-ttu-id="58049-798">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-799">CC002</span><span class="sxs-lookup"><span data-stu-id="58049-799">CC002</span></span></td>
<td><span data-ttu-id="58049-800">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58049-800">Finance</span></span></td>
<td><span data-ttu-id="58049-801">10001</span><span class="sxs-lookup"><span data-stu-id="58049-801">10001</span></span></td>
<td><span data-ttu-id="58049-802">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-802">Electricity</span></span></td>
<td><span data-ttu-id="58049-803">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-803">Variable cost</span></span></td>
<td><span data-ttu-id="58049-804">436.00</span><span class="sxs-lookup"><span data-stu-id="58049-804">436.00</span></span></td>
<td><span data-ttu-id="58049-805">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-806">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-806">CC003</span></span></td>
<td><span data-ttu-id="58049-807">Smölun</span><span class="sxs-lookup"><span data-stu-id="58049-807">Assembly</span></span></td>
<td><span data-ttu-id="58049-808">10001</span><span class="sxs-lookup"><span data-stu-id="58049-808">10001</span></span></td>
<td><span data-ttu-id="58049-809">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-809">Electricity</span></span></td>
<td><span data-ttu-id="58049-810">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-810">Variable cost</span></span></td>
<td><span data-ttu-id="58049-811">685.14</span><span class="sxs-lookup"><span data-stu-id="58049-811">685.14</span></span></td>
<td><span data-ttu-id="58049-812">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-813">CC004</span><span class="sxs-lookup"><span data-stu-id="58049-813">CC004</span></span></td>
<td><span data-ttu-id="58049-814">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58049-814">Packaging</span></span></td>
<td><span data-ttu-id="58049-815">10001</span><span class="sxs-lookup"><span data-stu-id="58049-815">10001</span></span></td>
<td><span data-ttu-id="58049-816">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-816">Electricity</span></span></td>
<td><span data-ttu-id="58049-817">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-817">Variable cost</span></span></td>
<td><span data-ttu-id="58049-818">124.57</span><span class="sxs-lookup"><span data-stu-id="58049-818">124.57</span></span></td>
<td><span data-ttu-id="58049-819">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-820">CC002</span><span class="sxs-lookup"><span data-stu-id="58049-820">CC002</span></span></td>
<td><span data-ttu-id="58049-821">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58049-821">Finance</span></span></td>
<td><span data-ttu-id="58049-822">10001</span><span class="sxs-lookup"><span data-stu-id="58049-822">10001</span></span></td>
<td><span data-ttu-id="58049-823">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-823">Electricity</span></span></td>
<td><span data-ttu-id="58049-824">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-824">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="58049-825">-675.00</span></span></td>
<td><span data-ttu-id="58049-826">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-827">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-827">CC003</span></span></td>
<td><span data-ttu-id="58049-828">Smölun</span><span class="sxs-lookup"><span data-stu-id="58049-828">Assembly</span></span></td>
<td><span data-ttu-id="58049-829">10001</span><span class="sxs-lookup"><span data-stu-id="58049-829">10001</span></span></td>
<td><span data-ttu-id="58049-830">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-830">Electricity</span></span></td>
<td><span data-ttu-id="58049-831">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-831">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-832">438.75</span><span class="sxs-lookup"><span data-stu-id="58049-832">438.75</span></span></td>
<td><span data-ttu-id="58049-833">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-834">CC004</span><span class="sxs-lookup"><span data-stu-id="58049-834">CC004</span></span></td>
<td><span data-ttu-id="58049-835">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58049-835">Packaging</span></span></td>
<td><span data-ttu-id="58049-836">10001</span><span class="sxs-lookup"><span data-stu-id="58049-836">10001</span></span></td>
<td><span data-ttu-id="58049-837">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-837">Electricity</span></span></td>
<td><span data-ttu-id="58049-838">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-838">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-839">236.25</span><span class="sxs-lookup"><span data-stu-id="58049-839">236.25</span></span></td>
<td><span data-ttu-id="58049-840">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-841">CC002</span><span class="sxs-lookup"><span data-stu-id="58049-841">CC002</span></span></td>
<td><span data-ttu-id="58049-842">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58049-842">Finance</span></span></td>
<td><span data-ttu-id="58049-843">10001</span><span class="sxs-lookup"><span data-stu-id="58049-843">10001</span></span></td>
<td><span data-ttu-id="58049-844">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-844">Electricity</span></span></td>
<td><span data-ttu-id="58049-845">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-845">Variable cost</span></span></td>
<td><span data-ttu-id="58049-846">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="58049-846">-8,150.29</span></span></td>
<td><span data-ttu-id="58049-847">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-848">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-848">CC003</span></span></td>
<td><span data-ttu-id="58049-849">Smölun</span><span class="sxs-lookup"><span data-stu-id="58049-849">Assembly</span></span></td>
<td><span data-ttu-id="58049-850">10001</span><span class="sxs-lookup"><span data-stu-id="58049-850">10001</span></span></td>
<td><span data-ttu-id="58049-851">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-851">Electricity</span></span></td>
<td><span data-ttu-id="58049-852">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-852">Variable cost</span></span></td>
<td><span data-ttu-id="58049-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="58049-853">5,297.69</span></span></td>
<td><span data-ttu-id="58049-854">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-855">CC004</span><span class="sxs-lookup"><span data-stu-id="58049-855">CC004</span></span></td>
<td><span data-ttu-id="58049-856">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58049-856">Packaging</span></span></td>
<td><span data-ttu-id="58049-857">10001</span><span class="sxs-lookup"><span data-stu-id="58049-857">10001</span></span></td>
<td><span data-ttu-id="58049-858">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-858">Electricity</span></span></td>
<td><span data-ttu-id="58049-859">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-859">Variable cost</span></span></td>
<td><span data-ttu-id="58049-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="58049-860">2,852.60</span></span></td>
<td><span data-ttu-id="58049-861">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-862">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-862">CC003</span></span></td>
<td><span data-ttu-id="58049-863">Smölun</span><span class="sxs-lookup"><span data-stu-id="58049-863">Assembly</span></span></td>
<td><span data-ttu-id="58049-864">10001</span><span class="sxs-lookup"><span data-stu-id="58049-864">10001</span></span></td>
<td><span data-ttu-id="58049-865">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-865">Electricity</span></span></td>
<td><span data-ttu-id="58049-866">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-866">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="58049-867">-713.75</span></span></td>
<td><span data-ttu-id="58049-868">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-869">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-869">Prod 1</span></span></td>
<td><span data-ttu-id="58049-870">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-870">Product 1</span></span></td>
<td><span data-ttu-id="58049-871">10001</span><span class="sxs-lookup"><span data-stu-id="58049-871">10001</span></span></td>
<td><span data-ttu-id="58049-872">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-872">Electricity</span></span></td>
<td><span data-ttu-id="58049-873">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-873">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-874">535.31</span><span class="sxs-lookup"><span data-stu-id="58049-874">535.31</span></span></td>
<td><span data-ttu-id="58049-875">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-876">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-876">Prod 2</span></span></td>
<td><span data-ttu-id="58049-877">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-877">Product 2</span></span></td>
<td><span data-ttu-id="58049-878">10001</span><span class="sxs-lookup"><span data-stu-id="58049-878">10001</span></span></td>
<td><span data-ttu-id="58049-879">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-879">Electricity</span></span></td>
<td><span data-ttu-id="58049-880">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-880">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-881">178.44</span><span class="sxs-lookup"><span data-stu-id="58049-881">178.44</span></span></td>
<td><span data-ttu-id="58049-882">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-883">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-883">CC003</span></span></td>
<td><span data-ttu-id="58049-884">Smölun</span><span class="sxs-lookup"><span data-stu-id="58049-884">Assembly</span></span></td>
<td><span data-ttu-id="58049-885">10001</span><span class="sxs-lookup"><span data-stu-id="58049-885">10001</span></span></td>
<td><span data-ttu-id="58049-886">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-886">Electricity</span></span></td>
<td><span data-ttu-id="58049-887">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-887">Variable cost</span></span></td>
<td><span data-ttu-id="58049-888">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="58049-888">-5,982.83</span></span></td>
<td><span data-ttu-id="58049-889">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-890">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-890">Prod 1</span></span></td>
<td><span data-ttu-id="58049-891">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-891">Product 1</span></span></td>
<td><span data-ttu-id="58049-892">10001</span><span class="sxs-lookup"><span data-stu-id="58049-892">10001</span></span></td>
<td><span data-ttu-id="58049-893">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-893">Electricity</span></span></td>
<td><span data-ttu-id="58049-894">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-894">Variable cost</span></span></td>
<td><span data-ttu-id="58049-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="58049-895">4,487.12</span></span></td>
<td><span data-ttu-id="58049-896">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-897">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-897">Prod 2</span></span></td>
<td><span data-ttu-id="58049-898">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-898">Product 2</span></span></td>
<td><span data-ttu-id="58049-899">10001</span><span class="sxs-lookup"><span data-stu-id="58049-899">10001</span></span></td>
<td><span data-ttu-id="58049-900">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-900">Electricity</span></span></td>
<td><span data-ttu-id="58049-901">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-901">Variable cost</span></span></td>
<td><span data-ttu-id="58049-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="58049-902">1,495.71</span></span></td>
<td><span data-ttu-id="58049-903">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-904">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-904">CC003</span></span></td>
<td><span data-ttu-id="58049-905">Smölun</span><span class="sxs-lookup"><span data-stu-id="58049-905">Assembly</span></span></td>
<td><span data-ttu-id="58049-906">10001</span><span class="sxs-lookup"><span data-stu-id="58049-906">10001</span></span></td>
<td><span data-ttu-id="58049-907">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-907">Electricity</span></span></td>
<td><span data-ttu-id="58049-908">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-908">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="58049-909">-286.25</span></span></td>
<td><span data-ttu-id="58049-910">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-911">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-911">Prod 1</span></span></td>
<td><span data-ttu-id="58049-912">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-912">Product 1</span></span></td>
<td><span data-ttu-id="58049-913">10001</span><span class="sxs-lookup"><span data-stu-id="58049-913">10001</span></span></td>
<td><span data-ttu-id="58049-914">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-914">Electricity</span></span></td>
<td><span data-ttu-id="58049-915">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-915">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-916">241.05</span><span class="sxs-lookup"><span data-stu-id="58049-916">241.05</span></span></td>
<td><span data-ttu-id="58049-917">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-918">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-918">Prod 2</span></span></td>
<td><span data-ttu-id="58049-919">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-919">Product 2</span></span></td>
<td><span data-ttu-id="58049-920">10001</span><span class="sxs-lookup"><span data-stu-id="58049-920">10001</span></span></td>
<td><span data-ttu-id="58049-921">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-921">Electricity</span></span></td>
<td><span data-ttu-id="58049-922">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-922">Fixed cost</span></span></td>
<td><span data-ttu-id="58049-923">45.20</span><span class="sxs-lookup"><span data-stu-id="58049-923">45.20</span></span></td>
<td><span data-ttu-id="58049-924">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-925">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-925">CC003</span></span></td>
<td><span data-ttu-id="58049-926">Smölun</span><span class="sxs-lookup"><span data-stu-id="58049-926">Assembly</span></span></td>
<td><span data-ttu-id="58049-927">10001</span><span class="sxs-lookup"><span data-stu-id="58049-927">10001</span></span></td>
<td><span data-ttu-id="58049-928">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-928">Electricity</span></span></td>
<td><span data-ttu-id="58049-929">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-929">Variable cost</span></span></td>
<td><span data-ttu-id="58049-930">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="58049-930">-2,977.17</span></span></td>
<td><span data-ttu-id="58049-931">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-932">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-932">Prod 1</span></span></td>
<td><span data-ttu-id="58049-933">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-933">Product 1</span></span></td>
<td><span data-ttu-id="58049-934">10001</span><span class="sxs-lookup"><span data-stu-id="58049-934">10001</span></span></td>
<td><span data-ttu-id="58049-935">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-935">Electricity</span></span></td>
<td><span data-ttu-id="58049-936">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-936">Variable cost</span></span></td>
<td><span data-ttu-id="58049-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="58049-937">2,507.09</span></span></td>
<td><span data-ttu-id="58049-938">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58049-939">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-939">Prod 2</span></span></td>
<td><span data-ttu-id="58049-940">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-940">Product 2</span></span></td>
<td><span data-ttu-id="58049-941">10001</span><span class="sxs-lookup"><span data-stu-id="58049-941">10001</span></span></td>
<td><span data-ttu-id="58049-942">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-942">Electricity</span></span></td>
<td><span data-ttu-id="58049-943">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-943">Variable cost</span></span></td>
<td><span data-ttu-id="58049-944">470.08</span><span class="sxs-lookup"><span data-stu-id="58049-944">470.08</span></span></td>
<td><span data-ttu-id="58049-945">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58049-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="58049-946">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="58049-946">Conclusion</span></span>
<span data-ttu-id="58049-947">Í Fjárhagsbókhaldi er kostnaður upp á 10.000,00 fyrir rafmagn bókaður á kenni leppkostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="58049-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="58049-948">Þar af leiðandi munu kostnaðarbókarar vita að það þarf að úthluta þessum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="58049-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="58049-949">Í kostnaðarbókhaldi streymir kostnaður þvert á fyrirtækiseiningar og stig, samkvæmt þeim stefnum og reglum sem eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="58049-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="58049-950">Hver kostnaður hefur verið tengdur úthlutunargrunni sem veitir besta mat á úthlutun á kostnaði.</span><span class="sxs-lookup"><span data-stu-id="58049-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="58049-951">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58049-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="58049-952">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58049-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="58049-953">Samtala</span><span class="sxs-lookup"><span data-stu-id="58049-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="58049-954">CC099</span><span class="sxs-lookup"><span data-stu-id="58049-954">CC099</span></span></th>
<th><span data-ttu-id="58049-955">CC001</span><span class="sxs-lookup"><span data-stu-id="58049-955">CC001</span></span></th>
<th><span data-ttu-id="58049-956">CC002</span><span class="sxs-lookup"><span data-stu-id="58049-956">CC002</span></span></th>
<th><span data-ttu-id="58049-957">CC003</span><span class="sxs-lookup"><span data-stu-id="58049-957">CC003</span></span></th>
<th><span data-ttu-id="58049-958">CC004</span><span class="sxs-lookup"><span data-stu-id="58049-958">CC004</span></span></th>
<th><span data-ttu-id="58049-959">Verk 1</span><span class="sxs-lookup"><span data-stu-id="58049-959">Proj 1</span></span></th>
<th><span data-ttu-id="58049-960">Verk 2</span><span class="sxs-lookup"><span data-stu-id="58049-960">Proj 2</span></span></th>
<th><span data-ttu-id="58049-961">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58049-961">Prod 1</span></span></th>
<th><span data-ttu-id="58049-962">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58049-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="58049-963">10001 Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58049-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="58049-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="58049-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="58049-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="58049-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="58049-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="58049-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="58049-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="58049-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="58049-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="58049-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="58049-973">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="58049-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-974">0,00</span><span class="sxs-lookup"><span data-stu-id="58049-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="58049-975">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-976">0,00</span><span class="sxs-lookup"><span data-stu-id="58049-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-977">0,00</span><span class="sxs-lookup"><span data-stu-id="58049-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-978">0,00</span><span class="sxs-lookup"><span data-stu-id="58049-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-979">0,00</span><span class="sxs-lookup"><span data-stu-id="58049-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-980">0,00</span><span class="sxs-lookup"><span data-stu-id="58049-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="58049-981">776.36</span><span class="sxs-lookup"><span data-stu-id="58049-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-982">223.64</span><span class="sxs-lookup"><span data-stu-id="58049-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="58049-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="58049-984">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58049-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-985">000</span><span class="sxs-lookup"><span data-stu-id="58049-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-986">0,00</span><span class="sxs-lookup"><span data-stu-id="58049-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-987">0,00</span><span class="sxs-lookup"><span data-stu-id="58049-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-988">0,00</span><span class="sxs-lookup"><span data-stu-id="58049-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-989">0,00</span><span class="sxs-lookup"><span data-stu-id="58049-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-990">30,00</span><span class="sxs-lookup"><span data-stu-id="58049-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-991">10,00</span><span class="sxs-lookup"><span data-stu-id="58049-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="58049-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="58049-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58049-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="58049-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="58049-995">Þetta efnisatriði sýnir hvernig fyrir aðalkostnaðareiningin 10001 Rafmagn flæðir í gegnum kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="58049-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="58049-996">Þar af leiðandi er þessum sameiginlega kostnaði úthlutað á lægsta stigið í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="58049-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="58049-997">Með öðrum orðum bera kostnaðarhlutir á lægsta stiginu kostnaðinn.</span><span class="sxs-lookup"><span data-stu-id="58049-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="58049-998">Ef þú þarft sjónrænt flæði kostnaðar á milli kostnaðarhluta er hægt að nota stefnureglur samantekins kostnaðar til að gera kostnaðarflæðið sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="58049-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="58049-999">Ítarlegri upplýsingar eru í Reglu samantekins kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="58049-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="58049-1000">(Athugaðu að þetta efnisatriði hefur ekki enn verið fullklárað en er væntanlegt.)</span><span class="sxs-lookup"><span data-stu-id="58049-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




