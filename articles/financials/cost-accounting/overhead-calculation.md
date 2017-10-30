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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: e57db8f4b692aa9c27916625897e268f63031782
ms.openlocfilehash: 285799d70a945c2dae1e3c65296282d5c432a243
ms.contentlocale: is-is
ms.lasthandoff: 10/30/2017

---

# <a name="overhead-calculation"></a><span data-ttu-id="951ae-103">Útreikningur fastakostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="951ae-104">Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði.</span><span class="sxs-lookup"><span data-stu-id="951ae-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="951ae-105">Skýrsluskilgreining</span><span class="sxs-lookup"><span data-stu-id="951ae-105">Term definition</span></span>
---------------

<span data-ttu-id="951ae-106">Stjórnunarkostnaður er sá kostnaður sem stofnað er til fyrir rekstur fyrirtækis, en sem ekki er hægt að rekja beint til neinna sérstakrar starfsemi, vöru eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="951ae-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="951ae-107">Stjórnunarkostnaður veitir mikilvægan stuðning við myndun hagnaðarmyndandi verkþátta.</span><span class="sxs-lookup"><span data-stu-id="951ae-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="951ae-108">Hér eru nokkur dæmi um skilyrði:</span><span class="sxs-lookup"><span data-stu-id="951ae-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="951ae-109">Leiga</span><span class="sxs-lookup"><span data-stu-id="951ae-109">Rent</span></span>
-   <span data-ttu-id="951ae-110">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-110">Electricity</span></span>
-   <span data-ttu-id="951ae-111">Stjórnunarkostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="951ae-112">Yfirlit yfir útreikning fastakostnaðar</span><span class="sxs-lookup"><span data-stu-id="951ae-112">Overhead calculation overview</span></span>
<span data-ttu-id="951ae-113">Útreikningur fastakostnaðar keyrir reglur kostnaðarbókhalds í réttri röð.</span><span class="sxs-lookup"><span data-stu-id="951ae-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="951ae-114">Hægt er að keyra útreikning fastakostnaðar margsinnis fyrir sama fjárhagstímabil ef reglum kostnaðarbókhalds hefur verið breytt eða ákveðnar villur hafa fundist.</span><span class="sxs-lookup"><span data-stu-id="951ae-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="951ae-115">Hver keyrsla á útreikningi fastakostnaðar er geymd og fær einkvæmt útgáfukenni sem gerir kleift að bera saman útreikning í mismunandi útgáfum.</span><span class="sxs-lookup"><span data-stu-id="951ae-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="951ae-116">Kostnaðarfærslur sem útreikningur fastakostnaðar mynda fá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="951ae-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="951ae-117">Dagsetningin bókhald samsvarar lokadagsetning fjárhagstímabilsins sem er dagsetning reikningsskiladagsetning reikningsskila notað í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="951ae-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="951ae-118">Einkvæmt útgáfukenni samanstendur af eftirfarandi þáttum:</span><span class="sxs-lookup"><span data-stu-id="951ae-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="951ae-119">Gerð útgáfu</span><span class="sxs-lookup"><span data-stu-id="951ae-119">Version type</span></span>
-   <span data-ttu-id="951ae-120">Dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="951ae-120">Date and time</span></span>
-   <span data-ttu-id="951ae-121">Fjárhagur kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="951ae-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="951ae-122">Fjárhagsár</span><span class="sxs-lookup"><span data-stu-id="951ae-122">Fiscal year</span></span>
-   <span data-ttu-id="951ae-123">Reikningstímabil</span><span class="sxs-lookup"><span data-stu-id="951ae-123">Fiscal period</span></span>

<span data-ttu-id="951ae-124">Útreikningur fastakostnaðar er keyrður óháð því hver útgáfan er.</span><span class="sxs-lookup"><span data-stu-id="951ae-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="951ae-125">Þess vegna er hægt að reikna út áætlaða útgáfu á undan raunútgáfu.</span><span class="sxs-lookup"><span data-stu-id="951ae-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="951ae-126">Útreikningur fastakostnaðar samanstendur af fjórum skrefum, eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="951ae-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="951ae-127">Í hverju skrefi er færslubókarhaus stofnaður með bókarfærslum.</span><span class="sxs-lookup"><span data-stu-id="951ae-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="951ae-128">Þessi færslubókarhaus geymir inntaksgögn fyrir hvert útreikningsþrep.</span><span class="sxs-lookup"><span data-stu-id="951ae-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="951ae-129">Stefnur og reglur eru notaðar í hverri færslulínu og kostnaðarfærslur eru myndaðar sem úttak.</span><span class="sxs-lookup"><span data-stu-id="951ae-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="951ae-130">Þess vegna hefurðu ávallt fullan rekjanleika.</span><span class="sxs-lookup"><span data-stu-id="951ae-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="951ae-131">[![Útreikningur fastakostnaðar](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="951ae-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="951ae-132">Reikna og úthluta sameiginlegur kostnaði vegna rafmagns</span><span class="sxs-lookup"><span data-stu-id="951ae-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="951ae-133">Í Fjárhagsbókhaldi er ákveðinn kostnaður, eins og rafmagn, skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="951ae-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="951ae-134">Þar af leiðandi er nákvæmar innsýn rekstrarfélags ekki veitt fyrir kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="951ae-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="951ae-135">Í kostnaðarbókhaldi verður kostnaður að flæða í gegnum fyrirtækiseiningar til að veita rétta innsýn rekstrarfélags þvert á allar fyrirtækiseiningar og stig.</span><span class="sxs-lookup"><span data-stu-id="951ae-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="951ae-136">Þetta flæði verður að byggja á annaðhvort nákvæmri færslu notkunar eða sanngjarnri matsreglu.</span><span class="sxs-lookup"><span data-stu-id="951ae-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="951ae-137">Í fjárhagnum er hægt að bóka rafmagnskostnað eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="951ae-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="951ae-138">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="951ae-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="951ae-139">Kostnaðarstaður</span><span class="sxs-lookup"><span data-stu-id="951ae-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="951ae-140">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="951ae-140">Main account</span></span></th>
<th><span data-ttu-id="951ae-141">Upphæð í bókhaldsgjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="951ae-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-142">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="951ae-143">CC099</span><span class="sxs-lookup"><span data-stu-id="951ae-143">CC099</span></span></td>
<td><span data-ttu-id="951ae-144">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="951ae-144">Default cost center</span></span></td>
<td><span data-ttu-id="951ae-145">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-145">10001</span></span></td>
<td><span data-ttu-id="951ae-146">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-146">Electricity</span></span></td>
<td><span data-ttu-id="951ae-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="951ae-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="951ae-148">Skref 1: Keyra útreikning kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="951ae-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="951ae-149">Sjálfvirkt er að þegar kostnaðarfærslur eru fluttar úr grunngögnum fái þær flokkun kostnaðarhegðunar **Óflokkað** í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="951ae-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="951ae-150">Með því að nota stefnureglur kostnaðarhegðunar er hægt að endurflokka kostnaðarfærslur sem annaðhvort **Fastan kostnað** eða **Breytilegan kostnað**.</span><span class="sxs-lookup"><span data-stu-id="951ae-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="951ae-151">Tilgreinið reglu kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="951ae-151">Define the cost behavior rule</span></span>

<span data-ttu-id="951ae-152">Í sumum tilfellum er hluti af kostnaði föst þóknun og eftirstandandi kostnaður byggist á notkun.</span><span class="sxs-lookup"><span data-stu-id="951ae-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="951ae-153">Rafmagnsreikningar stemma oft við þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="951ae-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="951ae-154">Þegar tiltekin föst þóknun hefur verið greidd, er greitt fyrir notkun á kílóvattklukkustund (Kwh).</span><span class="sxs-lookup"><span data-stu-id="951ae-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="951ae-155">Til dæmis ef föst kostnaðarþóknun er 1000.00 sýnir þetta hvernig regla kostnaðarhegðunar er skilgreind:</span><span class="sxs-lookup"><span data-stu-id="951ae-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="951ae-156">Föst upphæð 1.000,00</span><span class="sxs-lookup"><span data-stu-id="951ae-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="951ae-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="951ae-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="951ae-158">1000.01 &lt; N = Breyta</span><span class="sxs-lookup"><span data-stu-id="951ae-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="951ae-159">Færslubók</span><span class="sxs-lookup"><span data-stu-id="951ae-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="951ae-160">Færslubók</span><span class="sxs-lookup"><span data-stu-id="951ae-160">Journal</span></span></th>
<th><span data-ttu-id="951ae-161">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="951ae-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="951ae-162">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="951ae-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="951ae-163">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="951ae-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-164">00001</span><span class="sxs-lookup"><span data-stu-id="951ae-164">00001</span></span></td>
<td><span data-ttu-id="951ae-165">Færslubók útreiknings fyrir kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="951ae-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="951ae-166">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="951ae-166">Fiscal</span></span></td>
<td><span data-ttu-id="951ae-167">2017</span><span class="sxs-lookup"><span data-stu-id="951ae-167">2017</span></span></td>
<td><span data-ttu-id="951ae-168">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="951ae-168">Period 1</span></span></td>
<td><span data-ttu-id="951ae-169">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="951ae-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="951ae-170">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="951ae-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="951ae-171">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="951ae-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="951ae-172">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="951ae-173">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="951ae-173">Cost element</span></span></th>
<th><span data-ttu-id="951ae-174">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="951ae-174">Cost behavior</span></span></th>
<th><span data-ttu-id="951ae-175">Upphæð</span><span class="sxs-lookup"><span data-stu-id="951ae-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-176">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="951ae-177">CC099</span><span class="sxs-lookup"><span data-stu-id="951ae-177">CC099</span></span></td>
<td><span data-ttu-id="951ae-178">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="951ae-178">Default cost center</span></span></td>
<td><span data-ttu-id="951ae-179">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-179">10001</span></span></td>
<td><span data-ttu-id="951ae-180">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-180">Electricity</span></span></td>
<td><span data-ttu-id="951ae-181">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="951ae-181">Unclassified</span></span></td>
<td><span data-ttu-id="951ae-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="951ae-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="951ae-183">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="951ae-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="951ae-184">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="951ae-185">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="951ae-185">Cost element</span></span></th>
<th><span data-ttu-id="951ae-186">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="951ae-186">Cost behavior</span></span></th>
<th><span data-ttu-id="951ae-187">Upphæð</span><span class="sxs-lookup"><span data-stu-id="951ae-187">Amount</span></span></th>
<th><span data-ttu-id="951ae-188">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="951ae-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-189">CC099</span><span class="sxs-lookup"><span data-stu-id="951ae-189">CC099</span></span></td>
<td><span data-ttu-id="951ae-190">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="951ae-190">Default cost center</span></span></td>
<td><span data-ttu-id="951ae-191">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-191">10001</span></span></td>
<td><span data-ttu-id="951ae-192">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-192">Electricity</span></span></td>
<td><span data-ttu-id="951ae-193">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="951ae-193">Unclassified</span></span></td>
<td><span data-ttu-id="951ae-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="951ae-194">10,000.00</span></span></td>
<td><span data-ttu-id="951ae-195">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-196">CC099</span><span class="sxs-lookup"><span data-stu-id="951ae-196">CC099</span></span></td>
<td><span data-ttu-id="951ae-197">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="951ae-197">Default cost center</span></span></td>
<td><span data-ttu-id="951ae-198">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-198">10001</span></span></td>
<td><span data-ttu-id="951ae-199">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-199">Electricity</span></span></td>
<td><span data-ttu-id="951ae-200">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="951ae-200">Unclassified</span></span></td>
<td><span data-ttu-id="951ae-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="951ae-201">-10,000.00</span></span></td>
<td><span data-ttu-id="951ae-202">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-203">CC099</span><span class="sxs-lookup"><span data-stu-id="951ae-203">CC099</span></span></td>
<td><span data-ttu-id="951ae-204">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="951ae-204">Default cost center</span></span></td>
<td><span data-ttu-id="951ae-205">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-205">10001</span></span></td>
<td><span data-ttu-id="951ae-206">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-206">Electricity</span></span></td>
<td><span data-ttu-id="951ae-207">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-207">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="951ae-208">1,000.00</span></span></td>
<td><span data-ttu-id="951ae-209">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-210">CC099</span><span class="sxs-lookup"><span data-stu-id="951ae-210">CC099</span></span></td>
<td><span data-ttu-id="951ae-211">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="951ae-211">Default cost center</span></span></td>
<td><span data-ttu-id="951ae-212">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-212">10001</span></span></td>
<td><span data-ttu-id="951ae-213">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-213">Electricity</span></span></td>
<td><span data-ttu-id="951ae-214">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-214">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="951ae-215">9,000.00</span></span></td>
<td><span data-ttu-id="951ae-216">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="951ae-217">Nákvæmar upplýsingar um kostnaðarhegðun er að finna í Reglu kostnaðarhegðunar.</span><span class="sxs-lookup"><span data-stu-id="951ae-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="951ae-218">(Athugaðu að þetta efnisatriði hefur ekki enn verið fullklárað en er væntanlegt.)</span><span class="sxs-lookup"><span data-stu-id="951ae-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="951ae-219">Skref 2: Keyra útreikning kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="951ae-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="951ae-220">Kostnaðardreifing er notuð til að endurúthluta kostnaði frá einum kostnaðarhlut til annars eða fleiri kostnaðarhluta með því að nota viðeigandi úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="951ae-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="951ae-221">Kostnaðardreifing og kostnaðarúthlutun eru ólíkar að því leyti að kostnaðardreifing kemur alltaf upp á stigi aðalkostnaðareiningar upphaflegs verðs.</span><span class="sxs-lookup"><span data-stu-id="951ae-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="951ae-222">Tilgreinið kostnaðardreifingarreglu</span><span class="sxs-lookup"><span data-stu-id="951ae-222">Define the cost distribution rule</span></span>

<span data-ttu-id="951ae-223">Í Fjárhagsbókhaldi er rafmagnskostnaður oft skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="951ae-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="951ae-224">Í kostnaðarbókhaldi er þessi nálgun ekki nógu nákvæm.</span><span class="sxs-lookup"><span data-stu-id="951ae-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="951ae-225">Breytilegur kostnaði þarf að dreifa á staka kostnaðarhluti á sanngjörnum grunni.</span><span class="sxs-lookup"><span data-stu-id="951ae-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="951ae-226">Rökréttasti úthlutunargrunnurinn er notkun á rafmagni (Kwh).</span><span class="sxs-lookup"><span data-stu-id="951ae-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="951ae-227">Stofnað er tölfræðilegt víddarstak sem er nefnt Rafmagn og rafmagnsnotkun er skráð.</span><span class="sxs-lookup"><span data-stu-id="951ae-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="951ae-228">Sjálfgefið er að öll tölfræðileg víddarstök verða tiltæk sem úthlutunargrunnur.</span><span class="sxs-lookup"><span data-stu-id="951ae-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="951ae-229">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-229">Cost object</span></span></th>
<th><span data-ttu-id="951ae-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="951ae-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-231">CC001</span><span class="sxs-lookup"><span data-stu-id="951ae-231">CC001</span></span></td>
<td><span data-ttu-id="951ae-232">Mannauður</span><span class="sxs-lookup"><span data-stu-id="951ae-232">HR</span></span></td>
<td><span data-ttu-id="951ae-233">1.000</span><span class="sxs-lookup"><span data-stu-id="951ae-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-234">CC002</span><span class="sxs-lookup"><span data-stu-id="951ae-234">CC002</span></span></td>
<td><span data-ttu-id="951ae-235">Fjármál</span><span class="sxs-lookup"><span data-stu-id="951ae-235">Finance</span></span></td>
<td><span data-ttu-id="951ae-236">6,000</span><span class="sxs-lookup"><span data-stu-id="951ae-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-237">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-237">CC003</span></span></td>
<td><span data-ttu-id="951ae-238">Smölun</span><span class="sxs-lookup"><span data-stu-id="951ae-238">Assembly</span></span></td>
<td><span data-ttu-id="951ae-239">0</span><span class="sxs-lookup"><span data-stu-id="951ae-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="951ae-240">Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunni fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="951ae-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="951ae-241">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-241">Cost object</span></span></th>
<th><span data-ttu-id="951ae-242">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="951ae-242">Magnitude</span></span></th>
<th><span data-ttu-id="951ae-243">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="951ae-243">Allocation factor</span></span></th>
<th><span data-ttu-id="951ae-244">Upphæð</span><span class="sxs-lookup"><span data-stu-id="951ae-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-245">CC001</span><span class="sxs-lookup"><span data-stu-id="951ae-245">CC001</span></span></td>
<td><span data-ttu-id="951ae-246">Mannauður</span><span class="sxs-lookup"><span data-stu-id="951ae-246">HR</span></span></td>
<td><span data-ttu-id="951ae-247">1.000</span><span class="sxs-lookup"><span data-stu-id="951ae-247">1,000</span></span></td>
<td><span data-ttu-id="951ae-248">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="951ae-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="951ae-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="951ae-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-250">CC002</span><span class="sxs-lookup"><span data-stu-id="951ae-250">CC002</span></span></td>
<td><span data-ttu-id="951ae-251">Fjármál</span><span class="sxs-lookup"><span data-stu-id="951ae-251">Finance</span></span></td>
<td><span data-ttu-id="951ae-252">6,000</span><span class="sxs-lookup"><span data-stu-id="951ae-252">6,000</span></span></td>
<td><span data-ttu-id="951ae-253">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="951ae-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="951ae-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="951ae-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-255">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-255">CC003</span></span></td>
<td><span data-ttu-id="951ae-256">Smölun</span><span class="sxs-lookup"><span data-stu-id="951ae-256">Assembly</span></span></td>
<td><span data-ttu-id="951ae-257">0</span><span class="sxs-lookup"><span data-stu-id="951ae-257">0</span></span></td>
<td><span data-ttu-id="951ae-258">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="951ae-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="951ae-259">0,00</span><span class="sxs-lookup"><span data-stu-id="951ae-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="951ae-260">Föstum kostnaði þarf að dreifa jafnt á staka kostnaðarhluti sem hafa notað rafmagn.</span><span class="sxs-lookup"><span data-stu-id="951ae-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="951ae-261">Hægt er að ná þessa niðurstöðu með því að nota tölfræðilegt víddarstakið Rafmagn í úthlutunargrunni reikniformúlu: (Rafmagn &gt; 0,00) Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunn fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="951ae-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="951ae-262">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-262">Cost object</span></span></th>
<th><span data-ttu-id="951ae-263">Formúla</span><span class="sxs-lookup"><span data-stu-id="951ae-263">Formula</span></span></th>
<th><span data-ttu-id="951ae-264">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="951ae-264">Magnitude</span></span></th>
<th><span data-ttu-id="951ae-265">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="951ae-265">Allocation factor</span></span></th>
<th><span data-ttu-id="951ae-266">Upphæð</span><span class="sxs-lookup"><span data-stu-id="951ae-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-267">CC001</span><span class="sxs-lookup"><span data-stu-id="951ae-267">CC001</span></span></td>
<td><span data-ttu-id="951ae-268">Mannauður</span><span class="sxs-lookup"><span data-stu-id="951ae-268">HR</span></span></td>
<td><span data-ttu-id="951ae-269">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="951ae-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="951ae-270">1</span><span class="sxs-lookup"><span data-stu-id="951ae-270">1</span></span></td>
<td><span data-ttu-id="951ae-271">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="951ae-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="951ae-272">500,00</span><span class="sxs-lookup"><span data-stu-id="951ae-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-273">CC002</span><span class="sxs-lookup"><span data-stu-id="951ae-273">CC002</span></span></td>
<td><span data-ttu-id="951ae-274">Fjármál</span><span class="sxs-lookup"><span data-stu-id="951ae-274">Finance</span></span></td>
<td><span data-ttu-id="951ae-275">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="951ae-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="951ae-276">1</span><span class="sxs-lookup"><span data-stu-id="951ae-276">1</span></span></td>
<td><span data-ttu-id="951ae-277">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="951ae-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="951ae-278">500,00</span><span class="sxs-lookup"><span data-stu-id="951ae-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-279">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-279">CC003</span></span></td>
<td><span data-ttu-id="951ae-280">Smölun</span><span class="sxs-lookup"><span data-stu-id="951ae-280">Assembly</span></span></td>
<td><span data-ttu-id="951ae-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="951ae-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="951ae-282">0</span><span class="sxs-lookup"><span data-stu-id="951ae-282">0</span></span></td>
<td><span data-ttu-id="951ae-283">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="951ae-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="951ae-284">0,00</span><span class="sxs-lookup"><span data-stu-id="951ae-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="951ae-285">Færslubók</span><span class="sxs-lookup"><span data-stu-id="951ae-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="951ae-286">Færslubók</span><span class="sxs-lookup"><span data-stu-id="951ae-286">Journal</span></span></th>
<th><span data-ttu-id="951ae-287">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="951ae-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="951ae-288">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="951ae-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="951ae-289">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="951ae-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-290">00002</span><span class="sxs-lookup"><span data-stu-id="951ae-290">00002</span></span></td>
<td><span data-ttu-id="951ae-291">Útreikningabók kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="951ae-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="951ae-292">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="951ae-292">Fiscal</span></span></td>
<td><span data-ttu-id="951ae-293">2017</span><span class="sxs-lookup"><span data-stu-id="951ae-293">2017</span></span></td>
<td><span data-ttu-id="951ae-294">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="951ae-294">Period 1</span></span></td>
<td><span data-ttu-id="951ae-295">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="951ae-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="951ae-296">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="951ae-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="951ae-297">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="951ae-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="951ae-298">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="951ae-299">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="951ae-299">Cost element</span></span></th>
<th><span data-ttu-id="951ae-300">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="951ae-300">Cost behavior</span></span></th>
<th><span data-ttu-id="951ae-301">Upphæð</span><span class="sxs-lookup"><span data-stu-id="951ae-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-302">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="951ae-303">CC099</span><span class="sxs-lookup"><span data-stu-id="951ae-303">CC099</span></span></td>
<td><span data-ttu-id="951ae-304">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="951ae-304">Default cost center</span></span></td>
<td><span data-ttu-id="951ae-305">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-305">10001</span></span></td>
<td><span data-ttu-id="951ae-306">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-306">Electricity</span></span></td>
<td><span data-ttu-id="951ae-307">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-307">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-308">1.000,00</span><span class="sxs-lookup"><span data-stu-id="951ae-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-309">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="951ae-310">CC099</span><span class="sxs-lookup"><span data-stu-id="951ae-310">CC099</span></span></td>
<td><span data-ttu-id="951ae-311">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="951ae-311">Default cost center</span></span></td>
<td><span data-ttu-id="951ae-312">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-312">10001</span></span></td>
<td><span data-ttu-id="951ae-313">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-313">Electricity</span></span></td>
<td><span data-ttu-id="951ae-314">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-314">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="951ae-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="951ae-316">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="951ae-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="951ae-317">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="951ae-318">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="951ae-318">Cost element</span></span></th>
<th><span data-ttu-id="951ae-319">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="951ae-319">Cost behavior</span></span></th>
<th><span data-ttu-id="951ae-320">Upphæð</span><span class="sxs-lookup"><span data-stu-id="951ae-320">Amount</span></span></th>
<th><span data-ttu-id="951ae-321">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="951ae-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-322">CC099</span><span class="sxs-lookup"><span data-stu-id="951ae-322">CC099</span></span></td>
<td><span data-ttu-id="951ae-323">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="951ae-323">Default cost center</span></span></td>
<td><span data-ttu-id="951ae-324">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-324">10001</span></span></td>
<td><span data-ttu-id="951ae-325">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-325">Electricity</span></span></td>
<td><span data-ttu-id="951ae-326">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-326">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-327">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="951ae-327">-1,000.00</span></span></td>
<td><span data-ttu-id="951ae-328">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-329">CC001</span><span class="sxs-lookup"><span data-stu-id="951ae-329">CC001</span></span></td>
<td><span data-ttu-id="951ae-330">Mannauður</span><span class="sxs-lookup"><span data-stu-id="951ae-330">HR</span></span></td>
<td><span data-ttu-id="951ae-331">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-331">10001</span></span></td>
<td><span data-ttu-id="951ae-332">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-332">Electricity</span></span></td>
<td><span data-ttu-id="951ae-333">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-333">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-334">500,00</span><span class="sxs-lookup"><span data-stu-id="951ae-334">500.00</span></span></td>
<td><span data-ttu-id="951ae-335">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-336">CC002</span><span class="sxs-lookup"><span data-stu-id="951ae-336">CC002</span></span></td>
<td><span data-ttu-id="951ae-337">Fjármál</span><span class="sxs-lookup"><span data-stu-id="951ae-337">Finance</span></span></td>
<td><span data-ttu-id="951ae-338">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-338">10001</span></span></td>
<td><span data-ttu-id="951ae-339">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-339">Electricity</span></span></td>
<td><span data-ttu-id="951ae-340">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-340">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-341">500,00</span><span class="sxs-lookup"><span data-stu-id="951ae-341">500.00</span></span></td>
<td><span data-ttu-id="951ae-342">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-343">CC099</span><span class="sxs-lookup"><span data-stu-id="951ae-343">CC099</span></span></td>
<td><span data-ttu-id="951ae-344">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="951ae-344">Default cost center</span></span></td>
<td><span data-ttu-id="951ae-345">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-345">10001</span></span></td>
<td><span data-ttu-id="951ae-346">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-346">Electricity</span></span></td>
<td><span data-ttu-id="951ae-347">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-347">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-348">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="951ae-348">-9,000.00</span></span></td>
<td><span data-ttu-id="951ae-349">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-350">CC001</span><span class="sxs-lookup"><span data-stu-id="951ae-350">CC001</span></span></td>
<td><span data-ttu-id="951ae-351">Mannauður</span><span class="sxs-lookup"><span data-stu-id="951ae-351">HR</span></span></td>
<td><span data-ttu-id="951ae-352">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-352">10001</span></span></td>
<td><span data-ttu-id="951ae-353">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-353">Electricity</span></span></td>
<td><span data-ttu-id="951ae-354">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-354">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="951ae-355">1,285.71</span></span></td>
<td><span data-ttu-id="951ae-356">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-357">CC002</span><span class="sxs-lookup"><span data-stu-id="951ae-357">CC002</span></span></td>
<td><span data-ttu-id="951ae-358">Fjármál</span><span class="sxs-lookup"><span data-stu-id="951ae-358">Finance</span></span></td>
<td><span data-ttu-id="951ae-359">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-359">10001</span></span></td>
<td><span data-ttu-id="951ae-360">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-360">Electricity</span></span></td>
<td><span data-ttu-id="951ae-361">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-361">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="951ae-362">7,714.29</span></span></td>
<td><span data-ttu-id="951ae-363">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="951ae-364">Nákvæmar upplýsingar um kostnaðardreifingu og úthlutunargrunna er að finna í Kostnaðardreifingarreglu og úthlutunargrunnum.</span><span class="sxs-lookup"><span data-stu-id="951ae-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="951ae-365">(Athugaðu að þetta efnisatriði hefur ekki enn verið fullklárað en er væntanlegt.)</span><span class="sxs-lookup"><span data-stu-id="951ae-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="951ae-366">Skref 3: Keyra útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="951ae-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="951ae-367">Sameiginlegur kostnaður er notaður til að rukka einn eða fleiri tilgreinda kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="951ae-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="951ae-368">Gjöldin byggjast á fyrirframákveðnu kostnaðarhlutfalli og mæligildi úr úthlutuðum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="951ae-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="951ae-369">Skilgreina sameiginlegan kostnað</span><span class="sxs-lookup"><span data-stu-id="951ae-369">Define the overhead rate</span></span>

<span data-ttu-id="951ae-370">Kostnaðarhlutur CC001 Mannauður stuðlar að safni innri verka.</span><span class="sxs-lookup"><span data-stu-id="951ae-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="951ae-371">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsverk til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="951ae-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="951ae-372">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-372">Cost object</span></span></th>
<th><span data-ttu-id="951ae-373">Tímar</span><span class="sxs-lookup"><span data-stu-id="951ae-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-374">Verk 1</span><span class="sxs-lookup"><span data-stu-id="951ae-374">Proj 1</span></span></td>
<td><span data-ttu-id="951ae-375">Verk 1</span><span class="sxs-lookup"><span data-stu-id="951ae-375">Project 1</span></span></td>
<td><span data-ttu-id="951ae-376">3</span><span class="sxs-lookup"><span data-stu-id="951ae-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-377">Verk 2</span><span class="sxs-lookup"><span data-stu-id="951ae-377">Proj 2</span></span></td>
<td><span data-ttu-id="951ae-378">Verk 2</span><span class="sxs-lookup"><span data-stu-id="951ae-378">Project 2</span></span></td>
<td><span data-ttu-id="951ae-379">1</span><span class="sxs-lookup"><span data-stu-id="951ae-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="951ae-380">Fyrirframákveðið kostnaðarhlutfall fyrir kostnaðarframlag verk hefur verið skilgreint.</span><span class="sxs-lookup"><span data-stu-id="951ae-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="951ae-381">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-381">Cost object</span></span></th>
<th><span data-ttu-id="951ae-382">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="951ae-382">Cost element</span></span></th>
<th><span data-ttu-id="951ae-383">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="951ae-383">Cost behavior</span></span></th>
<th><span data-ttu-id="951ae-384">Einingar</span><span class="sxs-lookup"><span data-stu-id="951ae-384">Units</span></span></th>
<th><span data-ttu-id="951ae-385">Taxti</span><span class="sxs-lookup"><span data-stu-id="951ae-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-386">CC001</span><span class="sxs-lookup"><span data-stu-id="951ae-386">CC001</span></span></td>
<td><span data-ttu-id="951ae-387">Mannauður</span><span class="sxs-lookup"><span data-stu-id="951ae-387">HR</span></span></td>
<td><span data-ttu-id="951ae-388">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-388">10001</span></span></td>
<td><span data-ttu-id="951ae-389">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-389">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-390">1</span><span class="sxs-lookup"><span data-stu-id="951ae-390">1</span></span></td>
<td><span data-ttu-id="951ae-391">10</span><span class="sxs-lookup"><span data-stu-id="951ae-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="951ae-392">Eftirfarandi tafla sýnir niðurstöður þegar Mannauðsverk eru notuð sem grunnur við úthlutun.</span><span class="sxs-lookup"><span data-stu-id="951ae-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="951ae-393">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-393">Cost object</span></span></th>
<th><span data-ttu-id="951ae-394">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="951ae-394">Magnitude</span></span></th>
<th><span data-ttu-id="951ae-395">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="951ae-395">Cost element</span></span></th>
<th><span data-ttu-id="951ae-396">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="951ae-396">Allocation factor</span></span></th>
<th><span data-ttu-id="951ae-397">Upphæð</span><span class="sxs-lookup"><span data-stu-id="951ae-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-398">Verk 1</span><span class="sxs-lookup"><span data-stu-id="951ae-398">Proj 1</span></span></td>
<td><span data-ttu-id="951ae-399">Verk 1</span><span class="sxs-lookup"><span data-stu-id="951ae-399">Project 1</span></span></td>
<td><span data-ttu-id="951ae-400">3</span><span class="sxs-lookup"><span data-stu-id="951ae-400">3</span></span></td>
<td><span data-ttu-id="951ae-401">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-401">10001</span></span></td>
<td><span data-ttu-id="951ae-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="951ae-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="951ae-403">30,00</span><span class="sxs-lookup"><span data-stu-id="951ae-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-404">Verk 2</span><span class="sxs-lookup"><span data-stu-id="951ae-404">Proj 2</span></span></td>
<td><span data-ttu-id="951ae-405">Verk 2</span><span class="sxs-lookup"><span data-stu-id="951ae-405">Project 2</span></span></td>
<td><span data-ttu-id="951ae-406">1</span><span class="sxs-lookup"><span data-stu-id="951ae-406">1</span></span></td>
<td><span data-ttu-id="951ae-407">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-407">10001</span></span></td>
<td><span data-ttu-id="951ae-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="951ae-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="951ae-409">10,00</span><span class="sxs-lookup"><span data-stu-id="951ae-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="951ae-410">Færslubók</span><span class="sxs-lookup"><span data-stu-id="951ae-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="951ae-411">Færslubók</span><span class="sxs-lookup"><span data-stu-id="951ae-411">Journal</span></span></th>
<th><span data-ttu-id="951ae-412">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="951ae-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="951ae-413">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="951ae-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="951ae-414">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="951ae-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-415">00003</span><span class="sxs-lookup"><span data-stu-id="951ae-415">00003</span></span></td>
<td><span data-ttu-id="951ae-416">Færslubók fyrir útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="951ae-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="951ae-417">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="951ae-417">Fiscal</span></span></td>
<td><span data-ttu-id="951ae-418">2017</span><span class="sxs-lookup"><span data-stu-id="951ae-418">2017</span></span></td>
<td><span data-ttu-id="951ae-419">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="951ae-419">Period 1</span></span></td>
<td><span data-ttu-id="951ae-420">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="951ae-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="951ae-421">Bókarfærslur (Bókarfærslur fyrir útreikning sameiginlegs kostnaðar)</span><span class="sxs-lookup"><span data-stu-id="951ae-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="951ae-422">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="951ae-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="951ae-423">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-423">Cost object</span></span></th>
<th><span data-ttu-id="951ae-424">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="951ae-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-425">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="951ae-426">Verk 1</span><span class="sxs-lookup"><span data-stu-id="951ae-426">Proj 1</span></span></td>
<td><span data-ttu-id="951ae-427">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="951ae-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="951ae-428">3,00</span><span class="sxs-lookup"><span data-stu-id="951ae-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-429">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="951ae-430">Verk 2</span><span class="sxs-lookup"><span data-stu-id="951ae-430">Proj 2</span></span></td>
<td><span data-ttu-id="951ae-431">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="951ae-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="951ae-432">1,00</span><span class="sxs-lookup"><span data-stu-id="951ae-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="951ae-433">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="951ae-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="951ae-434">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="951ae-435">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="951ae-435">Cost element</span></span></th>
<th><span data-ttu-id="951ae-436">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="951ae-436">Cost behavior</span></span></th>
<th><span data-ttu-id="951ae-437">Upphæð</span><span class="sxs-lookup"><span data-stu-id="951ae-437">Amount</span></span></th>
<th><span data-ttu-id="951ae-438">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="951ae-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="951ae-439">CC0001</span></span></td>
<td><span data-ttu-id="951ae-440">Mannauður</span><span class="sxs-lookup"><span data-stu-id="951ae-440">HR</span></span></td>
<td><span data-ttu-id="951ae-441">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-441">10001</span></span></td>
<td><span data-ttu-id="951ae-442">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-442">Electricity</span></span></td>
<td><span data-ttu-id="951ae-443">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-443">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="951ae-444">-30.00</span></span></td>
<td><span data-ttu-id="951ae-445">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-446">Verk 1</span><span class="sxs-lookup"><span data-stu-id="951ae-446">Proj 1</span></span></td>
<td><span data-ttu-id="951ae-447">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="951ae-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="951ae-448">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-448">10001</span></span></td>
<td><span data-ttu-id="951ae-449">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-449">Electricity</span></span></td>
<td><span data-ttu-id="951ae-450">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-450">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-451">30,00</span><span class="sxs-lookup"><span data-stu-id="951ae-451">30.00</span></span></td>
<td><span data-ttu-id="951ae-452">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-453">CC001</span><span class="sxs-lookup"><span data-stu-id="951ae-453">CC001</span></span></td>
<td><span data-ttu-id="951ae-454">Mannauður</span><span class="sxs-lookup"><span data-stu-id="951ae-454">HR</span></span></td>
<td><span data-ttu-id="951ae-455">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-455">10001</span></span></td>
<td><span data-ttu-id="951ae-456">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-456">Electricity</span></span></td>
<td><span data-ttu-id="951ae-457">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-457">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="951ae-458">-10.00</span></span></td>
<td><span data-ttu-id="951ae-459">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-460">Verk 2</span><span class="sxs-lookup"><span data-stu-id="951ae-460">Proj 2</span></span></td>
<td><span data-ttu-id="951ae-461">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="951ae-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="951ae-462">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-462">10001</span></span></td>
<td><span data-ttu-id="951ae-463">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-463">Electricity</span></span></td>
<td><span data-ttu-id="951ae-464">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-464">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-465">10,00</span><span class="sxs-lookup"><span data-stu-id="951ae-465">10.00</span></span></td>
<td><span data-ttu-id="951ae-466">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="951ae-467">Nákvæmar upplýsingar um reglu sameiginlegs kostnaðar er að finna í Reglu fyrir sameiginlegan kostnað og úthlutunargrunnum.</span><span class="sxs-lookup"><span data-stu-id="951ae-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="951ae-468">(Athugaðu að þetta efnisatriði hefur ekki enn verið fullklárað en er væntanlegt.)</span><span class="sxs-lookup"><span data-stu-id="951ae-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="951ae-469">Skref 4: Keyra útreikning kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="951ae-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="951ae-470">Úthlutun er notuð til að úthluta stöðu kostnaðarhlutar í öðrum kostnaðarhlutum með því að nota úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="951ae-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="951ae-471">Finance and Operations styður gagnvirka úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="951ae-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="951ae-472">Í gagnvirkri úthlutunaraðferð er sú sameiginlega þjónusta sem hjálparkostnaðarhlutir skiptast á viðurkennd að fullu.</span><span class="sxs-lookup"><span data-stu-id="951ae-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="951ae-473">Kerfið ákvarðar sjálfkrafa rétta röð til að framkvæma úthlutun eftir.</span><span class="sxs-lookup"><span data-stu-id="951ae-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="951ae-474">Stöðu kostnaðarhluta er úthlutað með einum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="951ae-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="951ae-475">Úthlutanir þvert á víddir kostnaðarhluta og viðkomandi stök þeirra eru studdar.</span><span class="sxs-lookup"><span data-stu-id="951ae-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="951ae-476">Úthlutun pöntunarinnar er stjórnað af stýrieiningu kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="951ae-476">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="951ae-477">[![Gagnkvæm aðferð](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="951ae-477">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="951ae-478">Tilgreinið kostnaðarúthlutun</span><span class="sxs-lookup"><span data-stu-id="951ae-478">Define the cost allocation</span></span>

<span data-ttu-id="951ae-479">Hér er einfalt dæmi sem útskýrir hvernig hægt er að rekja flæði kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="951ae-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="951ae-480">Kostnaðarhlutir CC001 Mannauður leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="951ae-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="951ae-481">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="951ae-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="951ae-482">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-482">Cost object</span></span></th>
<th><span data-ttu-id="951ae-483">Mannauðsþjónusta</span><span class="sxs-lookup"><span data-stu-id="951ae-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-484">CC002</span><span class="sxs-lookup"><span data-stu-id="951ae-484">CC002</span></span></td>
<td><span data-ttu-id="951ae-485">Fjármál</span><span class="sxs-lookup"><span data-stu-id="951ae-485">Finance</span></span></td>
<td><span data-ttu-id="951ae-486">35</span><span class="sxs-lookup"><span data-stu-id="951ae-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-487">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-487">CC003</span></span></td>
<td><span data-ttu-id="951ae-488">Smölun</span><span class="sxs-lookup"><span data-stu-id="951ae-488">Assembly</span></span></td>
<td><span data-ttu-id="951ae-489">55</span><span class="sxs-lookup"><span data-stu-id="951ae-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-490">CC004</span><span class="sxs-lookup"><span data-stu-id="951ae-490">CC004</span></span></td>
<td><span data-ttu-id="951ae-491">Pakkning</span><span class="sxs-lookup"><span data-stu-id="951ae-491">Packaging</span></span></td>
<td><span data-ttu-id="951ae-492">10</span><span class="sxs-lookup"><span data-stu-id="951ae-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="951ae-493">Kostnaðarhlutir CC002 Fjármál leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="951ae-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="951ae-494">Stofnað er tölfræðilegt víddarstak sem kallast Fjármálaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="951ae-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="951ae-495">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-495">Cost object</span></span></th>
<th><span data-ttu-id="951ae-496">Fjármálaþjónusta</span><span class="sxs-lookup"><span data-stu-id="951ae-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-497">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-497">CC003</span></span></td>
<td><span data-ttu-id="951ae-498">Smölun</span><span class="sxs-lookup"><span data-stu-id="951ae-498">Assembly</span></span></td>
<td><span data-ttu-id="951ae-499">65</span><span class="sxs-lookup"><span data-stu-id="951ae-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-500">CC004</span><span class="sxs-lookup"><span data-stu-id="951ae-500">CC004</span></span></td>
<td><span data-ttu-id="951ae-501">Pakkning</span><span class="sxs-lookup"><span data-stu-id="951ae-501">Packaging</span></span></td>
<td><span data-ttu-id="951ae-502">35</span><span class="sxs-lookup"><span data-stu-id="951ae-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="951ae-503">Kostnaðarhlutir CC003 Samsetning leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="951ae-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="951ae-504">Meðlimur tölfræðilega víddar sem kallast Mannauður verk er stofnað til að mælvíddarstaka notuðum magnitude.</span><span class="sxs-lookup"><span data-stu-id="951ae-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="951ae-505">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-505">Cost object</span></span></th>
<th><span data-ttu-id="951ae-506">Samsetningarþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="951ae-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-507">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-507">Prod 1</span></span></td>
<td><span data-ttu-id="951ae-508">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-508">Product 1</span></span></td>
<td><span data-ttu-id="951ae-509">60</span><span class="sxs-lookup"><span data-stu-id="951ae-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-510">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-510">Prod 2</span></span></td>
<td><span data-ttu-id="951ae-511">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-511">Product 2</span></span></td>
<td><span data-ttu-id="951ae-512">20</span><span class="sxs-lookup"><span data-stu-id="951ae-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="951ae-513">Kostnaðarhlutir CC004 Umbúðir leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="951ae-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="951ae-514">Stofnað er tölfræðilegt víddarstak sem kallast Umbúðaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="951ae-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="951ae-515">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-515">Cost object</span></span></th>
<th><span data-ttu-id="951ae-516">Umbúðaþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="951ae-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-517">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-517">Prod 1</span></span></td>
<td><span data-ttu-id="951ae-518">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-518">Product 1</span></span></td>
<td><span data-ttu-id="951ae-519">80</span><span class="sxs-lookup"><span data-stu-id="951ae-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-520">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-520">Prod 2</span></span></td>
<td><span data-ttu-id="951ae-521">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-521">Product 2</span></span></td>
<td><span data-ttu-id="951ae-522">sept</span><span class="sxs-lookup"><span data-stu-id="951ae-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="951ae-523">**Athugið:** Í Finance and Operations er hægt að afleiða tölfræðiaðgerðir eins og framleiðslutíma sem vara notar frá upprunagögnum.</span><span class="sxs-lookup"><span data-stu-id="951ae-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="951ae-524">Ítarlegri upplýsingar um veitur tölfræðiaðgerðar er að finna í Veitusniðmáti tölfræðiaðgerðar.</span><span class="sxs-lookup"><span data-stu-id="951ae-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="951ae-525">(Athugið að þetta efnisatriði er ekki enn fullklárað en er væntanlegt.) Eftirfarandi tafla sýnir niðurstöður þegar Mannauðsþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="951ae-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="951ae-526">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-526">Cost object</span></span></th>
<th><span data-ttu-id="951ae-527">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="951ae-527">Magnitude</span></span></th>
<th><span data-ttu-id="951ae-528">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="951ae-528">Allocation factor</span></span></th>
<th><span data-ttu-id="951ae-529">Upphæð</span><span class="sxs-lookup"><span data-stu-id="951ae-529">Amount</span></span></th>
<th><span data-ttu-id="951ae-530">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="951ae-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-531">CC002</span><span class="sxs-lookup"><span data-stu-id="951ae-531">CC002</span></span></td>
<td><span data-ttu-id="951ae-532">Fjármál</span><span class="sxs-lookup"><span data-stu-id="951ae-532">Finance</span></span></td>
<td><span data-ttu-id="951ae-533">35</span><span class="sxs-lookup"><span data-stu-id="951ae-533">35</span></span></td>
<td><span data-ttu-id="951ae-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="951ae-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="951ae-535">175.00</span><span class="sxs-lookup"><span data-stu-id="951ae-535">175.00</span></span></td>
<td><span data-ttu-id="951ae-536">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-537">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-537">CC003</span></span></td>
<td><span data-ttu-id="951ae-538">Smölun</span><span class="sxs-lookup"><span data-stu-id="951ae-538">Assembly</span></span></td>
<td><span data-ttu-id="951ae-539">55</span><span class="sxs-lookup"><span data-stu-id="951ae-539">55</span></span></td>
<td><span data-ttu-id="951ae-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="951ae-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="951ae-541">275.00</span><span class="sxs-lookup"><span data-stu-id="951ae-541">275.00</span></span></td>
<td><span data-ttu-id="951ae-542">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-543">CC004</span><span class="sxs-lookup"><span data-stu-id="951ae-543">CC004</span></span></td>
<td><span data-ttu-id="951ae-544">Pakkning</span><span class="sxs-lookup"><span data-stu-id="951ae-544">Packaging</span></span></td>
<td><span data-ttu-id="951ae-545">10</span><span class="sxs-lookup"><span data-stu-id="951ae-545">10</span></span></td>
<td><span data-ttu-id="951ae-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="951ae-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="951ae-547">50,00</span><span class="sxs-lookup"><span data-stu-id="951ae-547">50.00</span></span></td>
<td><span data-ttu-id="951ae-548">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-549">CC002</span><span class="sxs-lookup"><span data-stu-id="951ae-549">CC002</span></span></td>
<td><span data-ttu-id="951ae-550">Fjármál</span><span class="sxs-lookup"><span data-stu-id="951ae-550">Finance</span></span></td>
<td><span data-ttu-id="951ae-551">35</span><span class="sxs-lookup"><span data-stu-id="951ae-551">35</span></span></td>
<td><span data-ttu-id="951ae-552">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="951ae-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="951ae-553">436.00</span><span class="sxs-lookup"><span data-stu-id="951ae-553">436.00</span></span></td>
<td><span data-ttu-id="951ae-554">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-555">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-555">CC003</span></span></td>
<td><span data-ttu-id="951ae-556">Smölun</span><span class="sxs-lookup"><span data-stu-id="951ae-556">Assembly</span></span></td>
<td><span data-ttu-id="951ae-557">55</span><span class="sxs-lookup"><span data-stu-id="951ae-557">55</span></span></td>
<td><span data-ttu-id="951ae-558">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="951ae-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="951ae-559">685.14</span><span class="sxs-lookup"><span data-stu-id="951ae-559">685.14</span></span></td>
<td><span data-ttu-id="951ae-560">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-561">CC004</span><span class="sxs-lookup"><span data-stu-id="951ae-561">CC004</span></span></td>
<td><span data-ttu-id="951ae-562">Pakkning</span><span class="sxs-lookup"><span data-stu-id="951ae-562">Packaging</span></span></td>
<td><span data-ttu-id="951ae-563">10</span><span class="sxs-lookup"><span data-stu-id="951ae-563">10</span></span></td>
<td><span data-ttu-id="951ae-564">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="951ae-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="951ae-565">124.57</span><span class="sxs-lookup"><span data-stu-id="951ae-565">124.57</span></span></td>
<td><span data-ttu-id="951ae-566">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="951ae-567">Eftirfarandi tafla sýnir niðurstöður þegar Fjármálaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="951ae-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="951ae-568">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-568">Cost object</span></span></th>
<th><span data-ttu-id="951ae-569">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="951ae-569">Magnitude</span></span></th>
<th><span data-ttu-id="951ae-570">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="951ae-570">Allocation factor</span></span></th>
<th><span data-ttu-id="951ae-571">Upphæð</span><span class="sxs-lookup"><span data-stu-id="951ae-571">Amount</span></span></th>
<th><span data-ttu-id="951ae-572">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="951ae-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-573">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-573">CC003</span></span></td>
<td><span data-ttu-id="951ae-574">Smölun</span><span class="sxs-lookup"><span data-stu-id="951ae-574">Assembly</span></span></td>
<td><span data-ttu-id="951ae-575">65</span><span class="sxs-lookup"><span data-stu-id="951ae-575">65</span></span></td>
<td><span data-ttu-id="951ae-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="951ae-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="951ae-577">438.75</span><span class="sxs-lookup"><span data-stu-id="951ae-577">438.75</span></span></td>
<td><span data-ttu-id="951ae-578">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-579">CC004</span><span class="sxs-lookup"><span data-stu-id="951ae-579">CC004</span></span></td>
<td><span data-ttu-id="951ae-580">Pakkning</span><span class="sxs-lookup"><span data-stu-id="951ae-580">Packaging</span></span></td>
<td><span data-ttu-id="951ae-581">35</span><span class="sxs-lookup"><span data-stu-id="951ae-581">35</span></span></td>
<td><span data-ttu-id="951ae-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="951ae-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="951ae-583">236.25</span><span class="sxs-lookup"><span data-stu-id="951ae-583">236.25</span></span></td>
<td><span data-ttu-id="951ae-584">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-585">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-585">CC003</span></span></td>
<td><span data-ttu-id="951ae-586">Smölun</span><span class="sxs-lookup"><span data-stu-id="951ae-586">Assembly</span></span></td>
<td><span data-ttu-id="951ae-587">65</span><span class="sxs-lookup"><span data-stu-id="951ae-587">65</span></span></td>
<td><span data-ttu-id="951ae-588">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="951ae-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="951ae-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="951ae-589">5,297.69</span></span></td>
<td><span data-ttu-id="951ae-590">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-591">CC004</span><span class="sxs-lookup"><span data-stu-id="951ae-591">CC004</span></span></td>
<td><span data-ttu-id="951ae-592">Pakkning</span><span class="sxs-lookup"><span data-stu-id="951ae-592">Packaging</span></span></td>
<td><span data-ttu-id="951ae-593">35</span><span class="sxs-lookup"><span data-stu-id="951ae-593">35</span></span></td>
<td><span data-ttu-id="951ae-594">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="951ae-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="951ae-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="951ae-595">2,852.60</span></span></td>
<td><span data-ttu-id="951ae-596">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="951ae-597">Eftirfarandi tafla sýnir niðurstöður þegar Samsetningarþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="951ae-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="951ae-598">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-598">Cost object</span></span></th>
<th><span data-ttu-id="951ae-599">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="951ae-599">Magnitude</span></span></th>
<th><span data-ttu-id="951ae-600">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="951ae-600">Allocation factor</span></span></th>
<th><span data-ttu-id="951ae-601">Upphæð</span><span class="sxs-lookup"><span data-stu-id="951ae-601">Amount</span></span></th>
<th><span data-ttu-id="951ae-602">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="951ae-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-603">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-603">Prod 1</span></span></td>
<td><span data-ttu-id="951ae-604">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-604">Product 1</span></span></td>
<td><span data-ttu-id="951ae-605">60</span><span class="sxs-lookup"><span data-stu-id="951ae-605">60</span></span></td>
<td><span data-ttu-id="951ae-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="951ae-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="951ae-607">535.31</span><span class="sxs-lookup"><span data-stu-id="951ae-607">535.31</span></span></td>
<td><span data-ttu-id="951ae-608">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-609">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-609">Prod 2</span></span></td>
<td><span data-ttu-id="951ae-610">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-610">Product 2</span></span></td>
<td><span data-ttu-id="951ae-611">20</span><span class="sxs-lookup"><span data-stu-id="951ae-611">20</span></span></td>
<td><span data-ttu-id="951ae-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="951ae-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="951ae-613">178.44</span><span class="sxs-lookup"><span data-stu-id="951ae-613">178.44</span></span></td>
<td><span data-ttu-id="951ae-614">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-615">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-615">Prod 1</span></span></td>
<td><span data-ttu-id="951ae-616">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-616">Product 1</span></span></td>
<td><span data-ttu-id="951ae-617">60</span><span class="sxs-lookup"><span data-stu-id="951ae-617">60</span></span></td>
<td><span data-ttu-id="951ae-618">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="951ae-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="951ae-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="951ae-619">4,487.12</span></span></td>
<td><span data-ttu-id="951ae-620">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-621">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-621">Prod 2</span></span></td>
<td><span data-ttu-id="951ae-622">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-622">Product 2</span></span></td>
<td><span data-ttu-id="951ae-623">20</span><span class="sxs-lookup"><span data-stu-id="951ae-623">20</span></span></td>
<td><span data-ttu-id="951ae-624">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="951ae-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="951ae-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="951ae-625">1,495.71</span></span></td>
<td><span data-ttu-id="951ae-626">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="951ae-627">Eftirfarandi tafla sýnir niðurstöður þegar Umbúðaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="951ae-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="951ae-628">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-628">Cost object</span></span></th>
<th><span data-ttu-id="951ae-629">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="951ae-629">Magnitude</span></span></th>
<th><span data-ttu-id="951ae-630">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="951ae-630">Allocation factor</span></span></th>
<th><span data-ttu-id="951ae-631">Upphæð</span><span class="sxs-lookup"><span data-stu-id="951ae-631">Amount</span></span></th>
<th><span data-ttu-id="951ae-632">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="951ae-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-633">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-633">Prod 1</span></span></td>
<td><span data-ttu-id="951ae-634">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-634">Product 1</span></span></td>
<td><span data-ttu-id="951ae-635">80</span><span class="sxs-lookup"><span data-stu-id="951ae-635">80</span></span></td>
<td><span data-ttu-id="951ae-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="951ae-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="951ae-637">241.05</span><span class="sxs-lookup"><span data-stu-id="951ae-637">241.05</span></span></td>
<td><span data-ttu-id="951ae-638">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-639">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-639">Prod 2</span></span></td>
<td><span data-ttu-id="951ae-640">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-640">Product 2</span></span></td>
<td><span data-ttu-id="951ae-641">15</span><span class="sxs-lookup"><span data-stu-id="951ae-641">15</span></span></td>
<td><span data-ttu-id="951ae-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="951ae-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="951ae-643">45.20</span><span class="sxs-lookup"><span data-stu-id="951ae-643">45.20</span></span></td>
<td><span data-ttu-id="951ae-644">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-645">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-645">Prod 1</span></span></td>
<td><span data-ttu-id="951ae-646">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-646">Product 1</span></span></td>
<td><span data-ttu-id="951ae-647">80</span><span class="sxs-lookup"><span data-stu-id="951ae-647">80</span></span></td>
<td><span data-ttu-id="951ae-648">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="951ae-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="951ae-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="951ae-649">2,507.09</span></span></td>
<td><span data-ttu-id="951ae-650">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-651">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-651">Prod 2</span></span></td>
<td><span data-ttu-id="951ae-652">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-652">Product 2</span></span></td>
<td><span data-ttu-id="951ae-653">15</span><span class="sxs-lookup"><span data-stu-id="951ae-653">15</span></span></td>
<td><span data-ttu-id="951ae-654">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="951ae-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="951ae-655">470.08</span><span class="sxs-lookup"><span data-stu-id="951ae-655">470.08</span></span></td>
<td><span data-ttu-id="951ae-656">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="951ae-657">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="951ae-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="951ae-658">Færslubók</span><span class="sxs-lookup"><span data-stu-id="951ae-658">Journal</span></span></th>
<th><span data-ttu-id="951ae-659">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="951ae-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="951ae-660">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="951ae-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="951ae-661">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="951ae-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-662">00004</span><span class="sxs-lookup"><span data-stu-id="951ae-662">00004</span></span></td>
<td><span data-ttu-id="951ae-663">Færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="951ae-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="951ae-664">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="951ae-664">Fiscal</span></span></td>
<td><span data-ttu-id="951ae-665">2017</span><span class="sxs-lookup"><span data-stu-id="951ae-665">2017</span></span></td>
<td><span data-ttu-id="951ae-666">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="951ae-666">Period 1</span></span></td>
<td><span data-ttu-id="951ae-667">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="951ae-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="951ae-668">Færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="951ae-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="951ae-669">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="951ae-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="951ae-670">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="951ae-671">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="951ae-671">Cost element</span></span></th>
<th><span data-ttu-id="951ae-672">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="951ae-672">Cost behavior</span></span></th>
<th><span data-ttu-id="951ae-673">Upphæð</span><span class="sxs-lookup"><span data-stu-id="951ae-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-674">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="951ae-675">CC001</span><span class="sxs-lookup"><span data-stu-id="951ae-675">CC001</span></span></td>
<td><span data-ttu-id="951ae-676">Mannauður</span><span class="sxs-lookup"><span data-stu-id="951ae-676">HR</span></span></td>
<td><span data-ttu-id="951ae-677">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-677">10001</span></span></td>
<td><span data-ttu-id="951ae-678">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-678">Electricity</span></span></td>
<td><span data-ttu-id="951ae-679">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-679">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-680">500,00</span><span class="sxs-lookup"><span data-stu-id="951ae-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-681">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="951ae-682">CC001</span><span class="sxs-lookup"><span data-stu-id="951ae-682">CC001</span></span></td>
<td><span data-ttu-id="951ae-683">Mannauður</span><span class="sxs-lookup"><span data-stu-id="951ae-683">HR</span></span></td>
<td><span data-ttu-id="951ae-684">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-684">10001</span></span></td>
<td><span data-ttu-id="951ae-685">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-685">Electricity</span></span></td>
<td><span data-ttu-id="951ae-686">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-686">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="951ae-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-688">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="951ae-689">CC002</span><span class="sxs-lookup"><span data-stu-id="951ae-689">CC002</span></span></td>
<td><span data-ttu-id="951ae-690">Fjármál</span><span class="sxs-lookup"><span data-stu-id="951ae-690">Finance</span></span></td>
<td><span data-ttu-id="951ae-691">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-691">10001</span></span></td>
<td><span data-ttu-id="951ae-692">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-692">Electricity</span></span></td>
<td><span data-ttu-id="951ae-693">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-693">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-694">675.00</span><span class="sxs-lookup"><span data-stu-id="951ae-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-695">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="951ae-696">CC002</span><span class="sxs-lookup"><span data-stu-id="951ae-696">CC002</span></span></td>
<td><span data-ttu-id="951ae-697">Fjármál</span><span class="sxs-lookup"><span data-stu-id="951ae-697">Finance</span></span></td>
<td><span data-ttu-id="951ae-698">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-698">10001</span></span></td>
<td><span data-ttu-id="951ae-699">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-699">Electricity</span></span></td>
<td><span data-ttu-id="951ae-700">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-700">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="951ae-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-702">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="951ae-703">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-703">CC003</span></span></td>
<td><span data-ttu-id="951ae-704">Smölun</span><span class="sxs-lookup"><span data-stu-id="951ae-704">Assembly</span></span></td>
<td><span data-ttu-id="951ae-705">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-705">10001</span></span></td>
<td><span data-ttu-id="951ae-706">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-706">Electricity</span></span></td>
<td><span data-ttu-id="951ae-707">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-707">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-708">713.75</span><span class="sxs-lookup"><span data-stu-id="951ae-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-709">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="951ae-710">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-710">CC003</span></span></td>
<td><span data-ttu-id="951ae-711">Smölun</span><span class="sxs-lookup"><span data-stu-id="951ae-711">Assembly</span></span></td>
<td><span data-ttu-id="951ae-712">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-712">10001</span></span></td>
<td><span data-ttu-id="951ae-713">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-713">Electricity</span></span></td>
<td><span data-ttu-id="951ae-714">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-714">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="951ae-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-716">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="951ae-717">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-717">CC003</span></span></td>
<td><span data-ttu-id="951ae-718">Pakkning</span><span class="sxs-lookup"><span data-stu-id="951ae-718">Packaging</span></span></td>
<td><span data-ttu-id="951ae-719">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-719">10001</span></span></td>
<td><span data-ttu-id="951ae-720">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-720">Electricity</span></span></td>
<td><span data-ttu-id="951ae-721">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-721">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-722">286.25</span><span class="sxs-lookup"><span data-stu-id="951ae-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-723">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="951ae-724">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-724">CC003</span></span></td>
<td><span data-ttu-id="951ae-725">Pakkning</span><span class="sxs-lookup"><span data-stu-id="951ae-725">Packaging</span></span></td>
<td><span data-ttu-id="951ae-726">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-726">10001</span></span></td>
<td><span data-ttu-id="951ae-727">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-727">Electricity</span></span></td>
<td><span data-ttu-id="951ae-728">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-728">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="951ae-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-730">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="951ae-731">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-731">Prod 1</span></span></td>
<td><span data-ttu-id="951ae-732">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-732">Product 1</span></span></td>
<td><span data-ttu-id="951ae-733">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-733">10001</span></span></td>
<td><span data-ttu-id="951ae-734">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-734">Electricity</span></span></td>
<td><span data-ttu-id="951ae-735">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-735">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-736">776.36</span><span class="sxs-lookup"><span data-stu-id="951ae-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-737">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="951ae-738">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-738">Prod 1</span></span></td>
<td><span data-ttu-id="951ae-739">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-739">Product 1</span></span></td>
<td><span data-ttu-id="951ae-740">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-740">10001</span></span></td>
<td><span data-ttu-id="951ae-741">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-741">Electricity</span></span></td>
<td><span data-ttu-id="951ae-742">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-742">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="951ae-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-744">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="951ae-745">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-745">Prod 2</span></span></td>
<td><span data-ttu-id="951ae-746">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-746">Product 1</span></span></td>
<td><span data-ttu-id="951ae-747">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-747">10001</span></span></td>
<td><span data-ttu-id="951ae-748">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-748">Electricity</span></span></td>
<td><span data-ttu-id="951ae-749">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-749">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-750">223.64</span><span class="sxs-lookup"><span data-stu-id="951ae-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-751">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="951ae-752">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-752">Prod 2</span></span></td>
<td><span data-ttu-id="951ae-753">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-753">Product 1</span></span></td>
<td><span data-ttu-id="951ae-754">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-754">10001</span></span></td>
<td><span data-ttu-id="951ae-755">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-755">Electricity</span></span></td>
<td><span data-ttu-id="951ae-756">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-756">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="951ae-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="951ae-758">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="951ae-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="951ae-759">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="951ae-760">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="951ae-760">Cost element</span></span></th>
<th><span data-ttu-id="951ae-761">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="951ae-761">Cost behavior</span></span></th>
<th><span data-ttu-id="951ae-762">Upphæð</span><span class="sxs-lookup"><span data-stu-id="951ae-762">Amount</span></span></th>
<th><span data-ttu-id="951ae-763">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="951ae-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="951ae-764">CC001</span><span class="sxs-lookup"><span data-stu-id="951ae-764">CC001</span></span></td>
<td><span data-ttu-id="951ae-765">Mannauður</span><span class="sxs-lookup"><span data-stu-id="951ae-765">HR</span></span></td>
<td><span data-ttu-id="951ae-766">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-766">10001</span></span></td>
<td><span data-ttu-id="951ae-767">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-767">Electricity</span></span></td>
<td><span data-ttu-id="951ae-768">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-768">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="951ae-769">-500.00</span></span></td>
<td><span data-ttu-id="951ae-770">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-771">CC002</span><span class="sxs-lookup"><span data-stu-id="951ae-771">CC002</span></span></td>
<td><span data-ttu-id="951ae-772">Fjármál</span><span class="sxs-lookup"><span data-stu-id="951ae-772">Finance</span></span></td>
<td><span data-ttu-id="951ae-773">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-773">10001</span></span></td>
<td><span data-ttu-id="951ae-774">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-774">Electricity</span></span></td>
<td><span data-ttu-id="951ae-775">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-775">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-776">175.00</span><span class="sxs-lookup"><span data-stu-id="951ae-776">175.00</span></span></td>
<td><span data-ttu-id="951ae-777">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-778">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-778">CC003</span></span></td>
<td><span data-ttu-id="951ae-779">Smölun</span><span class="sxs-lookup"><span data-stu-id="951ae-779">Assembly</span></span></td>
<td><span data-ttu-id="951ae-780">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-780">10001</span></span></td>
<td><span data-ttu-id="951ae-781">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-781">Electricity</span></span></td>
<td><span data-ttu-id="951ae-782">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-782">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-783">275.00</span><span class="sxs-lookup"><span data-stu-id="951ae-783">275.00</span></span></td>
<td><span data-ttu-id="951ae-784">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-785">CC004</span><span class="sxs-lookup"><span data-stu-id="951ae-785">CC004</span></span></td>
<td><span data-ttu-id="951ae-786">Pakkning</span><span class="sxs-lookup"><span data-stu-id="951ae-786">Packaging</span></span></td>
<td><span data-ttu-id="951ae-787">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-787">10001</span></span></td>
<td><span data-ttu-id="951ae-788">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-788">Electricity</span></span></td>
<td><span data-ttu-id="951ae-789">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-789">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-790">50,00</span><span class="sxs-lookup"><span data-stu-id="951ae-790">50,00</span></span></td>
<td><span data-ttu-id="951ae-791">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-792">CC001</span><span class="sxs-lookup"><span data-stu-id="951ae-792">CC001</span></span></td>
<td><span data-ttu-id="951ae-793">Mannauður</span><span class="sxs-lookup"><span data-stu-id="951ae-793">HR</span></span></td>
<td><span data-ttu-id="951ae-794">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-794">10001</span></span></td>
<td><span data-ttu-id="951ae-795">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-795">Electricity</span></span></td>
<td><span data-ttu-id="951ae-796">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-796">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-797">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="951ae-797">-1,245.71</span></span></td>
<td><span data-ttu-id="951ae-798">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-799">CC002</span><span class="sxs-lookup"><span data-stu-id="951ae-799">CC002</span></span></td>
<td><span data-ttu-id="951ae-800">Fjármál</span><span class="sxs-lookup"><span data-stu-id="951ae-800">Finance</span></span></td>
<td><span data-ttu-id="951ae-801">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-801">10001</span></span></td>
<td><span data-ttu-id="951ae-802">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-802">Electricity</span></span></td>
<td><span data-ttu-id="951ae-803">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-803">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-804">436.00</span><span class="sxs-lookup"><span data-stu-id="951ae-804">436.00</span></span></td>
<td><span data-ttu-id="951ae-805">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-806">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-806">CC003</span></span></td>
<td><span data-ttu-id="951ae-807">Smölun</span><span class="sxs-lookup"><span data-stu-id="951ae-807">Assembly</span></span></td>
<td><span data-ttu-id="951ae-808">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-808">10001</span></span></td>
<td><span data-ttu-id="951ae-809">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-809">Electricity</span></span></td>
<td><span data-ttu-id="951ae-810">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-810">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-811">685.14</span><span class="sxs-lookup"><span data-stu-id="951ae-811">685.14</span></span></td>
<td><span data-ttu-id="951ae-812">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-813">CC004</span><span class="sxs-lookup"><span data-stu-id="951ae-813">CC004</span></span></td>
<td><span data-ttu-id="951ae-814">Pakkning</span><span class="sxs-lookup"><span data-stu-id="951ae-814">Packaging</span></span></td>
<td><span data-ttu-id="951ae-815">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-815">10001</span></span></td>
<td><span data-ttu-id="951ae-816">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-816">Electricity</span></span></td>
<td><span data-ttu-id="951ae-817">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-817">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-818">124.57</span><span class="sxs-lookup"><span data-stu-id="951ae-818">124.57</span></span></td>
<td><span data-ttu-id="951ae-819">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-820">CC002</span><span class="sxs-lookup"><span data-stu-id="951ae-820">CC002</span></span></td>
<td><span data-ttu-id="951ae-821">Fjármál</span><span class="sxs-lookup"><span data-stu-id="951ae-821">Finance</span></span></td>
<td><span data-ttu-id="951ae-822">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-822">10001</span></span></td>
<td><span data-ttu-id="951ae-823">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-823">Electricity</span></span></td>
<td><span data-ttu-id="951ae-824">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-824">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="951ae-825">-675.00</span></span></td>
<td><span data-ttu-id="951ae-826">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-827">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-827">CC003</span></span></td>
<td><span data-ttu-id="951ae-828">Smölun</span><span class="sxs-lookup"><span data-stu-id="951ae-828">Assembly</span></span></td>
<td><span data-ttu-id="951ae-829">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-829">10001</span></span></td>
<td><span data-ttu-id="951ae-830">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-830">Electricity</span></span></td>
<td><span data-ttu-id="951ae-831">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-831">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-832">438.75</span><span class="sxs-lookup"><span data-stu-id="951ae-832">438.75</span></span></td>
<td><span data-ttu-id="951ae-833">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-834">CC004</span><span class="sxs-lookup"><span data-stu-id="951ae-834">CC004</span></span></td>
<td><span data-ttu-id="951ae-835">Pakkning</span><span class="sxs-lookup"><span data-stu-id="951ae-835">Packaging</span></span></td>
<td><span data-ttu-id="951ae-836">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-836">10001</span></span></td>
<td><span data-ttu-id="951ae-837">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-837">Electricity</span></span></td>
<td><span data-ttu-id="951ae-838">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-838">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-839">236.25</span><span class="sxs-lookup"><span data-stu-id="951ae-839">236.25</span></span></td>
<td><span data-ttu-id="951ae-840">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-841">CC002</span><span class="sxs-lookup"><span data-stu-id="951ae-841">CC002</span></span></td>
<td><span data-ttu-id="951ae-842">Fjármál</span><span class="sxs-lookup"><span data-stu-id="951ae-842">Finance</span></span></td>
<td><span data-ttu-id="951ae-843">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-843">10001</span></span></td>
<td><span data-ttu-id="951ae-844">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-844">Electricity</span></span></td>
<td><span data-ttu-id="951ae-845">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-845">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-846">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="951ae-846">-8,150.29</span></span></td>
<td><span data-ttu-id="951ae-847">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-848">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-848">CC003</span></span></td>
<td><span data-ttu-id="951ae-849">Smölun</span><span class="sxs-lookup"><span data-stu-id="951ae-849">Assembly</span></span></td>
<td><span data-ttu-id="951ae-850">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-850">10001</span></span></td>
<td><span data-ttu-id="951ae-851">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-851">Electricity</span></span></td>
<td><span data-ttu-id="951ae-852">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-852">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="951ae-853">5,297.69</span></span></td>
<td><span data-ttu-id="951ae-854">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-855">CC004</span><span class="sxs-lookup"><span data-stu-id="951ae-855">CC004</span></span></td>
<td><span data-ttu-id="951ae-856">Pakkning</span><span class="sxs-lookup"><span data-stu-id="951ae-856">Packaging</span></span></td>
<td><span data-ttu-id="951ae-857">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-857">10001</span></span></td>
<td><span data-ttu-id="951ae-858">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-858">Electricity</span></span></td>
<td><span data-ttu-id="951ae-859">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-859">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="951ae-860">2,852.60</span></span></td>
<td><span data-ttu-id="951ae-861">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-862">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-862">CC003</span></span></td>
<td><span data-ttu-id="951ae-863">Smölun</span><span class="sxs-lookup"><span data-stu-id="951ae-863">Assembly</span></span></td>
<td><span data-ttu-id="951ae-864">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-864">10001</span></span></td>
<td><span data-ttu-id="951ae-865">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-865">Electricity</span></span></td>
<td><span data-ttu-id="951ae-866">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-866">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="951ae-867">-713.75</span></span></td>
<td><span data-ttu-id="951ae-868">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-869">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-869">Prod 1</span></span></td>
<td><span data-ttu-id="951ae-870">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-870">Product 1</span></span></td>
<td><span data-ttu-id="951ae-871">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-871">10001</span></span></td>
<td><span data-ttu-id="951ae-872">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-872">Electricity</span></span></td>
<td><span data-ttu-id="951ae-873">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-873">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-874">535.31</span><span class="sxs-lookup"><span data-stu-id="951ae-874">535.31</span></span></td>
<td><span data-ttu-id="951ae-875">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-876">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-876">Prod 2</span></span></td>
<td><span data-ttu-id="951ae-877">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-877">Product 2</span></span></td>
<td><span data-ttu-id="951ae-878">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-878">10001</span></span></td>
<td><span data-ttu-id="951ae-879">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-879">Electricity</span></span></td>
<td><span data-ttu-id="951ae-880">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-880">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-881">178.44</span><span class="sxs-lookup"><span data-stu-id="951ae-881">178.44</span></span></td>
<td><span data-ttu-id="951ae-882">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-883">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-883">CC003</span></span></td>
<td><span data-ttu-id="951ae-884">Smölun</span><span class="sxs-lookup"><span data-stu-id="951ae-884">Assembly</span></span></td>
<td><span data-ttu-id="951ae-885">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-885">10001</span></span></td>
<td><span data-ttu-id="951ae-886">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-886">Electricity</span></span></td>
<td><span data-ttu-id="951ae-887">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-887">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-888">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="951ae-888">-5,982.83</span></span></td>
<td><span data-ttu-id="951ae-889">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-890">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-890">Prod 1</span></span></td>
<td><span data-ttu-id="951ae-891">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-891">Product 1</span></span></td>
<td><span data-ttu-id="951ae-892">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-892">10001</span></span></td>
<td><span data-ttu-id="951ae-893">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-893">Electricity</span></span></td>
<td><span data-ttu-id="951ae-894">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-894">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="951ae-895">4,487.12</span></span></td>
<td><span data-ttu-id="951ae-896">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-897">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-897">Prod 2</span></span></td>
<td><span data-ttu-id="951ae-898">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-898">Product 2</span></span></td>
<td><span data-ttu-id="951ae-899">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-899">10001</span></span></td>
<td><span data-ttu-id="951ae-900">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-900">Electricity</span></span></td>
<td><span data-ttu-id="951ae-901">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-901">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="951ae-902">1,495.71</span></span></td>
<td><span data-ttu-id="951ae-903">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-904">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-904">CC003</span></span></td>
<td><span data-ttu-id="951ae-905">Smölun</span><span class="sxs-lookup"><span data-stu-id="951ae-905">Assembly</span></span></td>
<td><span data-ttu-id="951ae-906">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-906">10001</span></span></td>
<td><span data-ttu-id="951ae-907">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-907">Electricity</span></span></td>
<td><span data-ttu-id="951ae-908">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-908">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="951ae-909">-286.25</span></span></td>
<td><span data-ttu-id="951ae-910">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-911">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-911">Prod 1</span></span></td>
<td><span data-ttu-id="951ae-912">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-912">Product 1</span></span></td>
<td><span data-ttu-id="951ae-913">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-913">10001</span></span></td>
<td><span data-ttu-id="951ae-914">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-914">Electricity</span></span></td>
<td><span data-ttu-id="951ae-915">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-915">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-916">241.05</span><span class="sxs-lookup"><span data-stu-id="951ae-916">241.05</span></span></td>
<td><span data-ttu-id="951ae-917">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-918">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-918">Prod 2</span></span></td>
<td><span data-ttu-id="951ae-919">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-919">Product 2</span></span></td>
<td><span data-ttu-id="951ae-920">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-920">10001</span></span></td>
<td><span data-ttu-id="951ae-921">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-921">Electricity</span></span></td>
<td><span data-ttu-id="951ae-922">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-922">Fixed cost</span></span></td>
<td><span data-ttu-id="951ae-923">45.20</span><span class="sxs-lookup"><span data-stu-id="951ae-923">45.20</span></span></td>
<td><span data-ttu-id="951ae-924">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-925">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-925">CC003</span></span></td>
<td><span data-ttu-id="951ae-926">Smölun</span><span class="sxs-lookup"><span data-stu-id="951ae-926">Assembly</span></span></td>
<td><span data-ttu-id="951ae-927">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-927">10001</span></span></td>
<td><span data-ttu-id="951ae-928">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-928">Electricity</span></span></td>
<td><span data-ttu-id="951ae-929">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-929">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-930">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="951ae-930">-2,977.17</span></span></td>
<td><span data-ttu-id="951ae-931">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-932">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-932">Prod 1</span></span></td>
<td><span data-ttu-id="951ae-933">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-933">Product 1</span></span></td>
<td><span data-ttu-id="951ae-934">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-934">10001</span></span></td>
<td><span data-ttu-id="951ae-935">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-935">Electricity</span></span></td>
<td><span data-ttu-id="951ae-936">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-936">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="951ae-937">2,507.09</span></span></td>
<td><span data-ttu-id="951ae-938">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="951ae-939">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-939">Prod 2</span></span></td>
<td><span data-ttu-id="951ae-940">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-940">Product 2</span></span></td>
<td><span data-ttu-id="951ae-941">10001</span><span class="sxs-lookup"><span data-stu-id="951ae-941">10001</span></span></td>
<td><span data-ttu-id="951ae-942">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-942">Electricity</span></span></td>
<td><span data-ttu-id="951ae-943">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-943">Variable cost</span></span></td>
<td><span data-ttu-id="951ae-944">470.08</span><span class="sxs-lookup"><span data-stu-id="951ae-944">470.08</span></span></td>
<td><span data-ttu-id="951ae-945">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="951ae-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="951ae-946">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="951ae-946">Conclusion</span></span>
<span data-ttu-id="951ae-947">Í Fjárhagsbókhaldi er kostnaður upp á 10.000,00 fyrir rafmagn bókaður á kenni leppkostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="951ae-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="951ae-948">Þar af leiðandi munu kostnaðarbókarar vita að það þarf að úthluta þessum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="951ae-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="951ae-949">Í kostnaðarbókhaldi streymir kostnaður þvert á fyrirtækiseiningar og stig, samkvæmt þeim stefnum og reglum sem eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="951ae-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="951ae-950">Hver kostnaður hefur verið tengdur úthlutunargrunni sem veitir besta mat á úthlutun á kostnaði.</span><span class="sxs-lookup"><span data-stu-id="951ae-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="951ae-951">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="951ae-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="951ae-952">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="951ae-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="951ae-953">Samtala</span><span class="sxs-lookup"><span data-stu-id="951ae-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="951ae-954">CC099</span><span class="sxs-lookup"><span data-stu-id="951ae-954">CC099</span></span></th>
<th><span data-ttu-id="951ae-955">CC001</span><span class="sxs-lookup"><span data-stu-id="951ae-955">CC001</span></span></th>
<th><span data-ttu-id="951ae-956">CC002</span><span class="sxs-lookup"><span data-stu-id="951ae-956">CC002</span></span></th>
<th><span data-ttu-id="951ae-957">CC003</span><span class="sxs-lookup"><span data-stu-id="951ae-957">CC003</span></span></th>
<th><span data-ttu-id="951ae-958">CC004</span><span class="sxs-lookup"><span data-stu-id="951ae-958">CC004</span></span></th>
<th><span data-ttu-id="951ae-959">Verk 1</span><span class="sxs-lookup"><span data-stu-id="951ae-959">Proj 1</span></span></th>
<th><span data-ttu-id="951ae-960">Verk 2</span><span class="sxs-lookup"><span data-stu-id="951ae-960">Proj 2</span></span></th>
<th><span data-ttu-id="951ae-961">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="951ae-961">Prod 1</span></span></th>
<th><span data-ttu-id="951ae-962">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="951ae-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="951ae-963">10001 Rafmagn</span><span class="sxs-lookup"><span data-stu-id="951ae-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="951ae-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="951ae-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="951ae-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="951ae-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="951ae-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="951ae-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="951ae-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="951ae-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="951ae-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="951ae-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="951ae-973">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="951ae-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-974">0,00</span><span class="sxs-lookup"><span data-stu-id="951ae-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="951ae-975">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-976">0,00</span><span class="sxs-lookup"><span data-stu-id="951ae-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-977">0,00</span><span class="sxs-lookup"><span data-stu-id="951ae-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-978">0,00</span><span class="sxs-lookup"><span data-stu-id="951ae-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-979">0,00</span><span class="sxs-lookup"><span data-stu-id="951ae-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-980">0,00</span><span class="sxs-lookup"><span data-stu-id="951ae-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="951ae-981">776.36</span><span class="sxs-lookup"><span data-stu-id="951ae-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-982">223.64</span><span class="sxs-lookup"><span data-stu-id="951ae-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="951ae-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="951ae-984">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="951ae-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-985">000</span><span class="sxs-lookup"><span data-stu-id="951ae-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-986">0,00</span><span class="sxs-lookup"><span data-stu-id="951ae-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-987">0,00</span><span class="sxs-lookup"><span data-stu-id="951ae-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-988">0,00</span><span class="sxs-lookup"><span data-stu-id="951ae-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-989">0,00</span><span class="sxs-lookup"><span data-stu-id="951ae-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-990">30,00</span><span class="sxs-lookup"><span data-stu-id="951ae-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-991">10,00</span><span class="sxs-lookup"><span data-stu-id="951ae-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="951ae-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="951ae-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="951ae-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="951ae-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="951ae-995">Þetta efnisatriði sýnir hvernig fyrir aðalkostnaðareiningin 10001 Rafmagn flæðir í gegnum kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="951ae-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="951ae-996">Þar af leiðandi er þessum sameiginlega kostnaði úthlutað á lægsta stigið í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="951ae-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="951ae-997">Með öðrum orðum bera kostnaðarhlutir á lægsta stiginu kostnaðinn.</span><span class="sxs-lookup"><span data-stu-id="951ae-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="951ae-998">Ef þú þarft sjónrænt flæði kostnaðar á milli kostnaðarhluta er hægt að nota stefnureglur samantekins kostnaðar til að gera kostnaðarflæðið sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="951ae-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="951ae-999">Ítarlegri upplýsingar eru í Reglu samantekins kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="951ae-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="951ae-1000">(Athugaðu að þetta efnisatriði hefur ekki enn verið fullklárað en er væntanlegt.)</span><span class="sxs-lookup"><span data-stu-id="951ae-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




