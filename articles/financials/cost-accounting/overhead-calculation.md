---
title: "Útreikningur fastakostnaður"
description: "Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði."
author: AndersGirke
manager: AnnBe
ms.date: 10/04/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 12ae99c15bafcd9cc08b30903fe3f251f446b17d
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---

# <a name="overhead-calculation"></a><span data-ttu-id="531b1-103">Útreikningur fastakostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="531b1-104">Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði.</span><span class="sxs-lookup"><span data-stu-id="531b1-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="531b1-105">Skýrsluskilgreining</span><span class="sxs-lookup"><span data-stu-id="531b1-105">Term definition</span></span>
---------------

<span data-ttu-id="531b1-106">Stjórnunarkostnaður er sá kostnaður sem stofnað er til fyrir rekstur fyrirtækis, en sem ekki er hægt að rekja beint til neinna sérstakrar starfsemi, vöru eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="531b1-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="531b1-107">Stjórnunarkostnaður veitir mikilvægan stuðning við myndun hagnaðarmyndandi verkþátta.</span><span class="sxs-lookup"><span data-stu-id="531b1-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="531b1-108">Hér eru nokkur dæmi um skilyrði:</span><span class="sxs-lookup"><span data-stu-id="531b1-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="531b1-109">Leiga</span><span class="sxs-lookup"><span data-stu-id="531b1-109">Rent</span></span>
-   <span data-ttu-id="531b1-110">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-110">Electricity</span></span>
-   <span data-ttu-id="531b1-111">Stjórnunarkostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="531b1-112">Yfirlit yfir útreikning fastakostnaðar</span><span class="sxs-lookup"><span data-stu-id="531b1-112">Overhead calculation overview</span></span>
<span data-ttu-id="531b1-113">Útreikningur fastakostnaðar keyrir reglur kostnaðarbókhalds í réttri röð.</span><span class="sxs-lookup"><span data-stu-id="531b1-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="531b1-114">Hægt er að keyra útreikning fastakostnaðar margsinnis fyrir sama fjárhagstímabil ef reglum kostnaðarbókhalds hefur verið breytt eða ákveðnar villur hafa fundist.</span><span class="sxs-lookup"><span data-stu-id="531b1-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="531b1-115">Hver keyrsla á útreikningi fastakostnaðar er geymd og fær einkvæmt útgáfukenni sem gerir kleift að bera saman útreikning í mismunandi útgáfum.</span><span class="sxs-lookup"><span data-stu-id="531b1-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="531b1-116">Kostnaðarfærslur sem útreikningur fastakostnaðar mynda fá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="531b1-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="531b1-117">Dagsetningin bókhald samsvarar lokadagsetning fjárhagstímabilsins sem er dagsetning reikningsskiladagsetning reikningsskila notað í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="531b1-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="531b1-118">Einkvæmt útgáfukenni samanstendur af eftirfarandi þáttum:</span><span class="sxs-lookup"><span data-stu-id="531b1-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="531b1-119">Gerð útgáfu</span><span class="sxs-lookup"><span data-stu-id="531b1-119">Version type</span></span>
-   <span data-ttu-id="531b1-120">Dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="531b1-120">Date and time</span></span>
-   <span data-ttu-id="531b1-121">Fjárhagur kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="531b1-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="531b1-122">Fjárhagsár</span><span class="sxs-lookup"><span data-stu-id="531b1-122">Fiscal year</span></span>
-   <span data-ttu-id="531b1-123">Reikningstímabil</span><span class="sxs-lookup"><span data-stu-id="531b1-123">Fiscal period</span></span>

<span data-ttu-id="531b1-124">Útreikningur fastakostnaðar er keyrður óháð því hver útgáfan er.</span><span class="sxs-lookup"><span data-stu-id="531b1-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="531b1-125">Þess vegna er hægt að reikna út áætlaða útgáfu á undan raunútgáfu.</span><span class="sxs-lookup"><span data-stu-id="531b1-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="531b1-126">Útreikningur fastakostnaðar samanstendur af fjórum skrefum, eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="531b1-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="531b1-127">Í hverju skrefi er færslubókarhaus stofnaður með bókarfærslum.</span><span class="sxs-lookup"><span data-stu-id="531b1-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="531b1-128">Þessi færslubókarhaus geymir inntaksgögn fyrir hvert útreikningsþrep.</span><span class="sxs-lookup"><span data-stu-id="531b1-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="531b1-129">Stefnur og reglur eru notaðar í hverri færslulínu og kostnaðarfærslur eru myndaðar sem úttak.</span><span class="sxs-lookup"><span data-stu-id="531b1-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="531b1-130">Þess vegna hefurðu ávallt fullan rekjanleika.</span><span class="sxs-lookup"><span data-stu-id="531b1-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="531b1-131">[![Útreikningur fastakostnaðar](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="531b1-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="531b1-132">Reikna og úthluta sameiginlegur kostnaði vegna rafmagns</span><span class="sxs-lookup"><span data-stu-id="531b1-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="531b1-133">Í Fjárhagsbókhaldi er ákveðinn kostnaður, eins og rafmagn, skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="531b1-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="531b1-134">Þar af leiðandi er nákvæmar innsýn rekstrarfélags ekki veitt fyrir kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="531b1-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="531b1-135">Í kostnaðarbókhaldi verður kostnaður að flæða í gegnum fyrirtækiseiningar til að veita rétta innsýn rekstrarfélags þvert á allar fyrirtækiseiningar og stig.</span><span class="sxs-lookup"><span data-stu-id="531b1-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="531b1-136">Þetta flæði verður að byggja á annaðhvort nákvæmri færslu notkunar eða sanngjarnri matsreglu.</span><span class="sxs-lookup"><span data-stu-id="531b1-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="531b1-137">Í fjárhagnum er hægt að bóka rafmagnskostnað eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="531b1-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="531b1-138">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="531b1-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="531b1-139">Kostnaðarstaður</span><span class="sxs-lookup"><span data-stu-id="531b1-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="531b1-140">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="531b1-140">Main account</span></span></th>
<th><span data-ttu-id="531b1-141">Upphæð í bókhaldsgjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="531b1-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-142">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="531b1-143">CC099</span><span class="sxs-lookup"><span data-stu-id="531b1-143">CC099</span></span></td>
<td><span data-ttu-id="531b1-144">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="531b1-144">Default cost center</span></span></td>
<td><span data-ttu-id="531b1-145">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-145">10001</span></span></td>
<td><span data-ttu-id="531b1-146">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-146">Electricity</span></span></td>
<td><span data-ttu-id="531b1-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="531b1-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="531b1-148">Skref 1: Keyra útreikning kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="531b1-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="531b1-149">Sjálfvirkt er að þegar kostnaðarfærslur eru fluttar úr grunngögnum fái þær flokkun kostnaðarhegðunar **Óflokkað** í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="531b1-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="531b1-150">Með því að nota stefnureglur kostnaðarhegðunar er hægt að endurflokka kostnaðarfærslur sem annaðhvort **Fastan kostnað** eða **Breytilegan kostnað**.</span><span class="sxs-lookup"><span data-stu-id="531b1-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="531b1-151">Tilgreinið reglu kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="531b1-151">Define the cost behavior rule</span></span>

<span data-ttu-id="531b1-152">Í sumum tilfellum er hluti af kostnaði föst þóknun og eftirstandandi kostnaður byggist á notkun.</span><span class="sxs-lookup"><span data-stu-id="531b1-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="531b1-153">Rafmagnsreikningar stemma oft við þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="531b1-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="531b1-154">Þegar tiltekin föst þóknun hefur verið greidd, er greitt fyrir notkun á kílóvattklukkustund (Kwh).</span><span class="sxs-lookup"><span data-stu-id="531b1-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="531b1-155">Til dæmis ef föst kostnaðarþóknun er 1000.00 sýnir þetta hvernig regla kostnaðarhegðunar er skilgreind:</span><span class="sxs-lookup"><span data-stu-id="531b1-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="531b1-156">Föst upphæð 1.000,00</span><span class="sxs-lookup"><span data-stu-id="531b1-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="531b1-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="531b1-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="531b1-158">1000.01 &lt; N = Breyta</span><span class="sxs-lookup"><span data-stu-id="531b1-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="531b1-159">Færslubók</span><span class="sxs-lookup"><span data-stu-id="531b1-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="531b1-160">Færslubók</span><span class="sxs-lookup"><span data-stu-id="531b1-160">Journal</span></span></th>
<th><span data-ttu-id="531b1-161">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="531b1-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="531b1-162">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="531b1-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="531b1-163">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="531b1-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-164">00001</span><span class="sxs-lookup"><span data-stu-id="531b1-164">00001</span></span></td>
<td><span data-ttu-id="531b1-165">Færslubók útreiknings fyrir kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="531b1-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="531b1-166">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="531b1-166">Fiscal</span></span></td>
<td><span data-ttu-id="531b1-167">2017</span><span class="sxs-lookup"><span data-stu-id="531b1-167">2017</span></span></td>
<td><span data-ttu-id="531b1-168">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="531b1-168">Period 1</span></span></td>
<td><span data-ttu-id="531b1-169">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="531b1-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="531b1-170">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="531b1-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="531b1-171">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="531b1-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="531b1-172">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="531b1-173">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="531b1-173">Cost element</span></span></th>
<th><span data-ttu-id="531b1-174">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="531b1-174">Cost behavior</span></span></th>
<th><span data-ttu-id="531b1-175">Upphæð</span><span class="sxs-lookup"><span data-stu-id="531b1-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-176">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="531b1-177">CC099</span><span class="sxs-lookup"><span data-stu-id="531b1-177">CC099</span></span></td>
<td><span data-ttu-id="531b1-178">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="531b1-178">Default cost center</span></span></td>
<td><span data-ttu-id="531b1-179">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-179">10001</span></span></td>
<td><span data-ttu-id="531b1-180">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-180">Electricity</span></span></td>
<td><span data-ttu-id="531b1-181">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="531b1-181">Unclassified</span></span></td>
<td><span data-ttu-id="531b1-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="531b1-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="531b1-183">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="531b1-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="531b1-184">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="531b1-185">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="531b1-185">Cost element</span></span></th>
<th><span data-ttu-id="531b1-186">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="531b1-186">Cost behavior</span></span></th>
<th><span data-ttu-id="531b1-187">Upphæð</span><span class="sxs-lookup"><span data-stu-id="531b1-187">Amount</span></span></th>
<th><span data-ttu-id="531b1-188">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="531b1-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-189">CC099</span><span class="sxs-lookup"><span data-stu-id="531b1-189">CC099</span></span></td>
<td><span data-ttu-id="531b1-190">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="531b1-190">Default cost center</span></span></td>
<td><span data-ttu-id="531b1-191">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-191">10001</span></span></td>
<td><span data-ttu-id="531b1-192">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-192">Electricity</span></span></td>
<td><span data-ttu-id="531b1-193">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="531b1-193">Unclassified</span></span></td>
<td><span data-ttu-id="531b1-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="531b1-194">10,000.00</span></span></td>
<td><span data-ttu-id="531b1-195">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-196">CC099</span><span class="sxs-lookup"><span data-stu-id="531b1-196">CC099</span></span></td>
<td><span data-ttu-id="531b1-197">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="531b1-197">Default cost center</span></span></td>
<td><span data-ttu-id="531b1-198">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-198">10001</span></span></td>
<td><span data-ttu-id="531b1-199">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-199">Electricity</span></span></td>
<td><span data-ttu-id="531b1-200">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="531b1-200">Unclassified</span></span></td>
<td><span data-ttu-id="531b1-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="531b1-201">-10,000.00</span></span></td>
<td><span data-ttu-id="531b1-202">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-203">CC099</span><span class="sxs-lookup"><span data-stu-id="531b1-203">CC099</span></span></td>
<td><span data-ttu-id="531b1-204">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="531b1-204">Default cost center</span></span></td>
<td><span data-ttu-id="531b1-205">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-205">10001</span></span></td>
<td><span data-ttu-id="531b1-206">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-206">Electricity</span></span></td>
<td><span data-ttu-id="531b1-207">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-207">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="531b1-208">1,000.00</span></span></td>
<td><span data-ttu-id="531b1-209">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-210">CC099</span><span class="sxs-lookup"><span data-stu-id="531b1-210">CC099</span></span></td>
<td><span data-ttu-id="531b1-211">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="531b1-211">Default cost center</span></span></td>
<td><span data-ttu-id="531b1-212">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-212">10001</span></span></td>
<td><span data-ttu-id="531b1-213">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-213">Electricity</span></span></td>
<td><span data-ttu-id="531b1-214">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-214">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="531b1-215">9,000.00</span></span></td>
<td><span data-ttu-id="531b1-216">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="531b1-217">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðarhegðunarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="531b1-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="531b1-218">Skref 2: Keyra útreikning kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="531b1-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="531b1-219">Kostnaðardreifing er notuð til að endurúthluta kostnaði frá einum kostnaðarhlut til annars eða fleiri kostnaðarhluta með því að nota viðeigandi úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="531b1-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="531b1-220">Kostnaðardreifing og kostnaðarúthlutun eru ólíkar að því leyti að kostnaðardreifing kemur alltaf upp á stigi aðalkostnaðareiningar upphaflegs verðs.</span><span class="sxs-lookup"><span data-stu-id="531b1-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="531b1-221">Tilgreinið kostnaðardreifingarreglu</span><span class="sxs-lookup"><span data-stu-id="531b1-221">Define the cost distribution rule</span></span>

<span data-ttu-id="531b1-222">Í Fjárhagsbókhaldi er rafmagnskostnaður oft skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="531b1-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="531b1-223">Í kostnaðarbókhaldi er þessi nálgun ekki nógu nákvæm.</span><span class="sxs-lookup"><span data-stu-id="531b1-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="531b1-224">Breytilegur kostnaði þarf að dreifa á staka kostnaðarhluti á sanngjörnum grunni.</span><span class="sxs-lookup"><span data-stu-id="531b1-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="531b1-225">Rökréttasti úthlutunargrunnurinn er notkun á rafmagni (Kwh).</span><span class="sxs-lookup"><span data-stu-id="531b1-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="531b1-226">Stofnað er tölfræðilegt víddarstak sem er nefnt Rafmagn og rafmagnsnotkun er skráð.</span><span class="sxs-lookup"><span data-stu-id="531b1-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="531b1-227">Sjálfgefið er að öll tölfræðileg víddarstök verða tiltæk sem úthlutunargrunnur.</span><span class="sxs-lookup"><span data-stu-id="531b1-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="531b1-228">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-228">Cost object</span></span></th>
<th><span data-ttu-id="531b1-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="531b1-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-230">CC001</span><span class="sxs-lookup"><span data-stu-id="531b1-230">CC001</span></span></td>
<td><span data-ttu-id="531b1-231">Mannauður</span><span class="sxs-lookup"><span data-stu-id="531b1-231">HR</span></span></td>
<td><span data-ttu-id="531b1-232">1.000</span><span class="sxs-lookup"><span data-stu-id="531b1-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-233">CC002</span><span class="sxs-lookup"><span data-stu-id="531b1-233">CC002</span></span></td>
<td><span data-ttu-id="531b1-234">Fjármál</span><span class="sxs-lookup"><span data-stu-id="531b1-234">Finance</span></span></td>
<td><span data-ttu-id="531b1-235">6,000</span><span class="sxs-lookup"><span data-stu-id="531b1-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-236">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-236">CC003</span></span></td>
<td><span data-ttu-id="531b1-237">Smölun</span><span class="sxs-lookup"><span data-stu-id="531b1-237">Assembly</span></span></td>
<td><span data-ttu-id="531b1-238">0</span><span class="sxs-lookup"><span data-stu-id="531b1-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="531b1-239">Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunni fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="531b1-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="531b1-240">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-240">Cost object</span></span></th>
<th><span data-ttu-id="531b1-241">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="531b1-241">Magnitude</span></span></th>
<th><span data-ttu-id="531b1-242">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="531b1-242">Allocation factor</span></span></th>
<th><span data-ttu-id="531b1-243">Upphæð</span><span class="sxs-lookup"><span data-stu-id="531b1-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-244">CC001</span><span class="sxs-lookup"><span data-stu-id="531b1-244">CC001</span></span></td>
<td><span data-ttu-id="531b1-245">Mannauður</span><span class="sxs-lookup"><span data-stu-id="531b1-245">HR</span></span></td>
<td><span data-ttu-id="531b1-246">1.000</span><span class="sxs-lookup"><span data-stu-id="531b1-246">1,000</span></span></td>
<td><span data-ttu-id="531b1-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="531b1-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="531b1-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="531b1-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-249">CC002</span><span class="sxs-lookup"><span data-stu-id="531b1-249">CC002</span></span></td>
<td><span data-ttu-id="531b1-250">Fjármál</span><span class="sxs-lookup"><span data-stu-id="531b1-250">Finance</span></span></td>
<td><span data-ttu-id="531b1-251">6,000</span><span class="sxs-lookup"><span data-stu-id="531b1-251">6,000</span></span></td>
<td><span data-ttu-id="531b1-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="531b1-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="531b1-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="531b1-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-254">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-254">CC003</span></span></td>
<td><span data-ttu-id="531b1-255">Smölun</span><span class="sxs-lookup"><span data-stu-id="531b1-255">Assembly</span></span></td>
<td><span data-ttu-id="531b1-256">0</span><span class="sxs-lookup"><span data-stu-id="531b1-256">0</span></span></td>
<td><span data-ttu-id="531b1-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="531b1-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="531b1-258">0,00</span><span class="sxs-lookup"><span data-stu-id="531b1-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="531b1-259">Föstum kostnaði þarf að dreifa jafnt á staka kostnaðarhluti sem hafa notað rafmagn.</span><span class="sxs-lookup"><span data-stu-id="531b1-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="531b1-260">Hægt er að ná þessa niðurstöðu með því að nota tölfræðilegt víddarstakið Rafmagn í úthlutunargrunni reikniformúlu: (Rafmagn &gt; 0,00) Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunn fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="531b1-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="531b1-261">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-261">Cost object</span></span></th>
<th><span data-ttu-id="531b1-262">Formúla</span><span class="sxs-lookup"><span data-stu-id="531b1-262">Formula</span></span></th>
<th><span data-ttu-id="531b1-263">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="531b1-263">Magnitude</span></span></th>
<th><span data-ttu-id="531b1-264">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="531b1-264">Allocation factor</span></span></th>
<th><span data-ttu-id="531b1-265">Upphæð</span><span class="sxs-lookup"><span data-stu-id="531b1-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-266">CC001</span><span class="sxs-lookup"><span data-stu-id="531b1-266">CC001</span></span></td>
<td><span data-ttu-id="531b1-267">Mannauður</span><span class="sxs-lookup"><span data-stu-id="531b1-267">HR</span></span></td>
<td><span data-ttu-id="531b1-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="531b1-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="531b1-269">1</span><span class="sxs-lookup"><span data-stu-id="531b1-269">1</span></span></td>
<td><span data-ttu-id="531b1-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="531b1-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="531b1-271">500,00</span><span class="sxs-lookup"><span data-stu-id="531b1-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-272">CC002</span><span class="sxs-lookup"><span data-stu-id="531b1-272">CC002</span></span></td>
<td><span data-ttu-id="531b1-273">Fjármál</span><span class="sxs-lookup"><span data-stu-id="531b1-273">Finance</span></span></td>
<td><span data-ttu-id="531b1-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="531b1-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="531b1-275">1</span><span class="sxs-lookup"><span data-stu-id="531b1-275">1</span></span></td>
<td><span data-ttu-id="531b1-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="531b1-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="531b1-277">500,00</span><span class="sxs-lookup"><span data-stu-id="531b1-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-278">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-278">CC003</span></span></td>
<td><span data-ttu-id="531b1-279">Smölun</span><span class="sxs-lookup"><span data-stu-id="531b1-279">Assembly</span></span></td>
<td><span data-ttu-id="531b1-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="531b1-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="531b1-281">0</span><span class="sxs-lookup"><span data-stu-id="531b1-281">0</span></span></td>
<td><span data-ttu-id="531b1-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="531b1-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="531b1-283">0,00</span><span class="sxs-lookup"><span data-stu-id="531b1-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="531b1-284">Færslubók</span><span class="sxs-lookup"><span data-stu-id="531b1-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="531b1-285">Færslubók</span><span class="sxs-lookup"><span data-stu-id="531b1-285">Journal</span></span></th>
<th><span data-ttu-id="531b1-286">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="531b1-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="531b1-287">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="531b1-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="531b1-288">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="531b1-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-289">00002</span><span class="sxs-lookup"><span data-stu-id="531b1-289">00002</span></span></td>
<td><span data-ttu-id="531b1-290">Útreikningabók kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="531b1-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="531b1-291">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="531b1-291">Fiscal</span></span></td>
<td><span data-ttu-id="531b1-292">2017</span><span class="sxs-lookup"><span data-stu-id="531b1-292">2017</span></span></td>
<td><span data-ttu-id="531b1-293">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="531b1-293">Period 1</span></span></td>
<td><span data-ttu-id="531b1-294">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="531b1-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="531b1-295">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="531b1-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="531b1-296">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="531b1-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="531b1-297">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="531b1-298">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="531b1-298">Cost element</span></span></th>
<th><span data-ttu-id="531b1-299">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="531b1-299">Cost behavior</span></span></th>
<th><span data-ttu-id="531b1-300">Upphæð</span><span class="sxs-lookup"><span data-stu-id="531b1-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-301">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="531b1-302">CC099</span><span class="sxs-lookup"><span data-stu-id="531b1-302">CC099</span></span></td>
<td><span data-ttu-id="531b1-303">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="531b1-303">Default cost center</span></span></td>
<td><span data-ttu-id="531b1-304">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-304">10001</span></span></td>
<td><span data-ttu-id="531b1-305">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-305">Electricity</span></span></td>
<td><span data-ttu-id="531b1-306">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-306">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="531b1-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-308">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="531b1-309">CC099</span><span class="sxs-lookup"><span data-stu-id="531b1-309">CC099</span></span></td>
<td><span data-ttu-id="531b1-310">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="531b1-310">Default cost center</span></span></td>
<td><span data-ttu-id="531b1-311">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-311">10001</span></span></td>
<td><span data-ttu-id="531b1-312">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-312">Electricity</span></span></td>
<td><span data-ttu-id="531b1-313">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-313">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="531b1-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="531b1-315">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="531b1-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="531b1-316">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="531b1-317">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="531b1-317">Cost element</span></span></th>
<th><span data-ttu-id="531b1-318">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="531b1-318">Cost behavior</span></span></th>
<th><span data-ttu-id="531b1-319">Upphæð</span><span class="sxs-lookup"><span data-stu-id="531b1-319">Amount</span></span></th>
<th><span data-ttu-id="531b1-320">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="531b1-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-321">CC099</span><span class="sxs-lookup"><span data-stu-id="531b1-321">CC099</span></span></td>
<td><span data-ttu-id="531b1-322">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="531b1-322">Default cost center</span></span></td>
<td><span data-ttu-id="531b1-323">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-323">10001</span></span></td>
<td><span data-ttu-id="531b1-324">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-324">Electricity</span></span></td>
<td><span data-ttu-id="531b1-325">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-325">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="531b1-326">-1,000.00</span></span></td>
<td><span data-ttu-id="531b1-327">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-328">CC001</span><span class="sxs-lookup"><span data-stu-id="531b1-328">CC001</span></span></td>
<td><span data-ttu-id="531b1-329">Mannauður</span><span class="sxs-lookup"><span data-stu-id="531b1-329">HR</span></span></td>
<td><span data-ttu-id="531b1-330">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-330">10001</span></span></td>
<td><span data-ttu-id="531b1-331">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-331">Electricity</span></span></td>
<td><span data-ttu-id="531b1-332">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-332">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-333">500,00</span><span class="sxs-lookup"><span data-stu-id="531b1-333">500.00</span></span></td>
<td><span data-ttu-id="531b1-334">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-335">CC002</span><span class="sxs-lookup"><span data-stu-id="531b1-335">CC002</span></span></td>
<td><span data-ttu-id="531b1-336">Fjármál</span><span class="sxs-lookup"><span data-stu-id="531b1-336">Finance</span></span></td>
<td><span data-ttu-id="531b1-337">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-337">10001</span></span></td>
<td><span data-ttu-id="531b1-338">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-338">Electricity</span></span></td>
<td><span data-ttu-id="531b1-339">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-339">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-340">500,00</span><span class="sxs-lookup"><span data-stu-id="531b1-340">500.00</span></span></td>
<td><span data-ttu-id="531b1-341">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-342">CC099</span><span class="sxs-lookup"><span data-stu-id="531b1-342">CC099</span></span></td>
<td><span data-ttu-id="531b1-343">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="531b1-343">Default cost center</span></span></td>
<td><span data-ttu-id="531b1-344">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-344">10001</span></span></td>
<td><span data-ttu-id="531b1-345">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-345">Electricity</span></span></td>
<td><span data-ttu-id="531b1-346">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-346">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="531b1-347">-9,000.00</span></span></td>
<td><span data-ttu-id="531b1-348">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-349">CC001</span><span class="sxs-lookup"><span data-stu-id="531b1-349">CC001</span></span></td>
<td><span data-ttu-id="531b1-350">Mannauður</span><span class="sxs-lookup"><span data-stu-id="531b1-350">HR</span></span></td>
<td><span data-ttu-id="531b1-351">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-351">10001</span></span></td>
<td><span data-ttu-id="531b1-352">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-352">Electricity</span></span></td>
<td><span data-ttu-id="531b1-353">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-353">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="531b1-354">1,285.71</span></span></td>
<td><span data-ttu-id="531b1-355">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-356">CC002</span><span class="sxs-lookup"><span data-stu-id="531b1-356">CC002</span></span></td>
<td><span data-ttu-id="531b1-357">Fjármál</span><span class="sxs-lookup"><span data-stu-id="531b1-357">Finance</span></span></td>
<td><span data-ttu-id="531b1-358">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-358">10001</span></span></td>
<td><span data-ttu-id="531b1-359">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-359">Electricity</span></span></td>
<td><span data-ttu-id="531b1-360">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-360">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="531b1-361">7,714.29</span></span></td>
<td><span data-ttu-id="531b1-362">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="531b1-363">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðardreifingarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="531b1-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="531b1-364">Skref 3: Keyra útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="531b1-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="531b1-365">Sameiginlegur kostnaður er notaður til að rukka einn eða fleiri tilgreinda kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="531b1-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="531b1-366">Gjöldin byggjast á fyrirframákveðnu kostnaðarhlutfalli og mæligildi úr úthlutuðum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="531b1-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="531b1-367">Skilgreina sameiginlegan kostnað</span><span class="sxs-lookup"><span data-stu-id="531b1-367">Define the overhead rate</span></span>

<span data-ttu-id="531b1-368">Kostnaðarhlutur CC001 Mannauður stuðlar að safni innri verka.</span><span class="sxs-lookup"><span data-stu-id="531b1-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="531b1-369">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsverk til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="531b1-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="531b1-370">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-370">Cost object</span></span></th>
<th><span data-ttu-id="531b1-371">Tímar</span><span class="sxs-lookup"><span data-stu-id="531b1-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-372">Verk 1</span><span class="sxs-lookup"><span data-stu-id="531b1-372">Proj 1</span></span></td>
<td><span data-ttu-id="531b1-373">Verk 1</span><span class="sxs-lookup"><span data-stu-id="531b1-373">Project 1</span></span></td>
<td><span data-ttu-id="531b1-374">3</span><span class="sxs-lookup"><span data-stu-id="531b1-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-375">Verk 2</span><span class="sxs-lookup"><span data-stu-id="531b1-375">Proj 2</span></span></td>
<td><span data-ttu-id="531b1-376">Verk 2</span><span class="sxs-lookup"><span data-stu-id="531b1-376">Project 2</span></span></td>
<td><span data-ttu-id="531b1-377">1</span><span class="sxs-lookup"><span data-stu-id="531b1-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="531b1-378">Fyrirframákveðið kostnaðarhlutfall fyrir kostnaðarframlag verk hefur verið skilgreint.</span><span class="sxs-lookup"><span data-stu-id="531b1-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="531b1-379">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-379">Cost object</span></span></th>
<th><span data-ttu-id="531b1-380">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="531b1-380">Cost element</span></span></th>
<th><span data-ttu-id="531b1-381">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="531b1-381">Cost behavior</span></span></th>
<th><span data-ttu-id="531b1-382">Einingar</span><span class="sxs-lookup"><span data-stu-id="531b1-382">Units</span></span></th>
<th><span data-ttu-id="531b1-383">Taxti</span><span class="sxs-lookup"><span data-stu-id="531b1-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-384">CC001</span><span class="sxs-lookup"><span data-stu-id="531b1-384">CC001</span></span></td>
<td><span data-ttu-id="531b1-385">Mannauður</span><span class="sxs-lookup"><span data-stu-id="531b1-385">HR</span></span></td>
<td><span data-ttu-id="531b1-386">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-386">10001</span></span></td>
<td><span data-ttu-id="531b1-387">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-387">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-388">1</span><span class="sxs-lookup"><span data-stu-id="531b1-388">1</span></span></td>
<td><span data-ttu-id="531b1-389">10</span><span class="sxs-lookup"><span data-stu-id="531b1-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="531b1-390">Eftirfarandi tafla sýnir niðurstöður þegar Mannauðsverk eru notuð sem grunnur við úthlutun.</span><span class="sxs-lookup"><span data-stu-id="531b1-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="531b1-391">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-391">Cost object</span></span></th>
<th><span data-ttu-id="531b1-392">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="531b1-392">Magnitude</span></span></th>
<th><span data-ttu-id="531b1-393">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="531b1-393">Cost element</span></span></th>
<th><span data-ttu-id="531b1-394">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="531b1-394">Allocation factor</span></span></th>
<th><span data-ttu-id="531b1-395">Upphæð</span><span class="sxs-lookup"><span data-stu-id="531b1-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-396">Verk 1</span><span class="sxs-lookup"><span data-stu-id="531b1-396">Proj 1</span></span></td>
<td><span data-ttu-id="531b1-397">Verk 1</span><span class="sxs-lookup"><span data-stu-id="531b1-397">Project 1</span></span></td>
<td><span data-ttu-id="531b1-398">3</span><span class="sxs-lookup"><span data-stu-id="531b1-398">3</span></span></td>
<td><span data-ttu-id="531b1-399">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-399">10001</span></span></td>
<td><span data-ttu-id="531b1-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="531b1-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="531b1-401">30,00</span><span class="sxs-lookup"><span data-stu-id="531b1-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-402">Verk 2</span><span class="sxs-lookup"><span data-stu-id="531b1-402">Proj 2</span></span></td>
<td><span data-ttu-id="531b1-403">Verk 2</span><span class="sxs-lookup"><span data-stu-id="531b1-403">Project 2</span></span></td>
<td><span data-ttu-id="531b1-404">1</span><span class="sxs-lookup"><span data-stu-id="531b1-404">1</span></span></td>
<td><span data-ttu-id="531b1-405">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-405">10001</span></span></td>
<td><span data-ttu-id="531b1-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="531b1-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="531b1-407">10,00</span><span class="sxs-lookup"><span data-stu-id="531b1-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="531b1-408">Færslubók</span><span class="sxs-lookup"><span data-stu-id="531b1-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="531b1-409">Færslubók</span><span class="sxs-lookup"><span data-stu-id="531b1-409">Journal</span></span></th>
<th><span data-ttu-id="531b1-410">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="531b1-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="531b1-411">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="531b1-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="531b1-412">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="531b1-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-413">00003</span><span class="sxs-lookup"><span data-stu-id="531b1-413">00003</span></span></td>
<td><span data-ttu-id="531b1-414">Færslubók fyrir útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="531b1-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="531b1-415">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="531b1-415">Fiscal</span></span></td>
<td><span data-ttu-id="531b1-416">2017</span><span class="sxs-lookup"><span data-stu-id="531b1-416">2017</span></span></td>
<td><span data-ttu-id="531b1-417">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="531b1-417">Period 1</span></span></td>
<td><span data-ttu-id="531b1-418">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="531b1-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="531b1-419">Bókarfærslur (Bókarfærslur fyrir útreikning sameiginlegs kostnaðar)</span><span class="sxs-lookup"><span data-stu-id="531b1-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="531b1-420">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="531b1-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="531b1-421">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-421">Cost object</span></span></th>
<th><span data-ttu-id="531b1-422">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="531b1-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-423">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="531b1-424">Verk 1</span><span class="sxs-lookup"><span data-stu-id="531b1-424">Proj 1</span></span></td>
<td><span data-ttu-id="531b1-425">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="531b1-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="531b1-426">3,00</span><span class="sxs-lookup"><span data-stu-id="531b1-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-427">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="531b1-428">Verk 2</span><span class="sxs-lookup"><span data-stu-id="531b1-428">Proj 2</span></span></td>
<td><span data-ttu-id="531b1-429">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="531b1-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="531b1-430">1,00</span><span class="sxs-lookup"><span data-stu-id="531b1-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="531b1-431">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="531b1-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="531b1-432">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="531b1-433">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="531b1-433">Cost element</span></span></th>
<th><span data-ttu-id="531b1-434">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="531b1-434">Cost behavior</span></span></th>
<th><span data-ttu-id="531b1-435">Upphæð</span><span class="sxs-lookup"><span data-stu-id="531b1-435">Amount</span></span></th>
<th><span data-ttu-id="531b1-436">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="531b1-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="531b1-437">CC0001</span></span></td>
<td><span data-ttu-id="531b1-438">Mannauður</span><span class="sxs-lookup"><span data-stu-id="531b1-438">HR</span></span></td>
<td><span data-ttu-id="531b1-439">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-439">10001</span></span></td>
<td><span data-ttu-id="531b1-440">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-440">Electricity</span></span></td>
<td><span data-ttu-id="531b1-441">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-441">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="531b1-442">-30.00</span></span></td>
<td><span data-ttu-id="531b1-443">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-444">Verk 1</span><span class="sxs-lookup"><span data-stu-id="531b1-444">Proj 1</span></span></td>
<td><span data-ttu-id="531b1-445">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="531b1-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="531b1-446">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-446">10001</span></span></td>
<td><span data-ttu-id="531b1-447">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-447">Electricity</span></span></td>
<td><span data-ttu-id="531b1-448">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-448">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-449">30,00</span><span class="sxs-lookup"><span data-stu-id="531b1-449">30.00</span></span></td>
<td><span data-ttu-id="531b1-450">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-451">CC001</span><span class="sxs-lookup"><span data-stu-id="531b1-451">CC001</span></span></td>
<td><span data-ttu-id="531b1-452">Mannauður</span><span class="sxs-lookup"><span data-stu-id="531b1-452">HR</span></span></td>
<td><span data-ttu-id="531b1-453">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-453">10001</span></span></td>
<td><span data-ttu-id="531b1-454">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-454">Electricity</span></span></td>
<td><span data-ttu-id="531b1-455">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-455">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="531b1-456">-10.00</span></span></td>
<td><span data-ttu-id="531b1-457">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-458">Verk 2</span><span class="sxs-lookup"><span data-stu-id="531b1-458">Proj 2</span></span></td>
<td><span data-ttu-id="531b1-459">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="531b1-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="531b1-460">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-460">10001</span></span></td>
<td><span data-ttu-id="531b1-461">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-461">Electricity</span></span></td>
<td><span data-ttu-id="531b1-462">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-462">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-463">10,00</span><span class="sxs-lookup"><span data-stu-id="531b1-463">10.00</span></span></td>
<td><span data-ttu-id="531b1-464">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="531b1-465">Nánari upplýsingar er að finna í [Framkvæma útreikning fastakostnaðar](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="531b1-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="531b1-466">Skref 4: Keyra útreikning kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="531b1-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="531b1-467">Úthlutun er notuð til að úthluta stöðu kostnaðarhlutar í öðrum kostnaðarhlutum með því að nota úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="531b1-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="531b1-468">Finance and Operations styður gagnvirka úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="531b1-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="531b1-469">Í gagnvirkri úthlutunaraðferð er sú sameiginlega þjónusta sem hjálparkostnaðarhlutir skiptast á viðurkennd að fullu.</span><span class="sxs-lookup"><span data-stu-id="531b1-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="531b1-470">Kerfið ákvarðar sjálfkrafa rétta röð til að framkvæma úthlutun eftir.</span><span class="sxs-lookup"><span data-stu-id="531b1-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="531b1-471">Stöðu kostnaðarhluta er úthlutað með einum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="531b1-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="531b1-472">Úthlutanir þvert á víddir kostnaðarhluta og viðkomandi stök þeirra eru studdar.</span><span class="sxs-lookup"><span data-stu-id="531b1-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="531b1-473">Úthlutun pöntunarinnar er stjórnað af stýrieiningu kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="531b1-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="531b1-474">[![Gagnkvæm aðferð](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="531b1-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="531b1-475">Tilgreinið kostnaðarúthlutun</span><span class="sxs-lookup"><span data-stu-id="531b1-475">Define the cost allocation</span></span>

<span data-ttu-id="531b1-476">Hér er einfalt dæmi sem útskýrir hvernig hægt er að rekja flæði kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="531b1-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="531b1-477">Kostnaðarhlutir CC001 Mannauður leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="531b1-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="531b1-478">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="531b1-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="531b1-479">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-479">Cost object</span></span></th>
<th><span data-ttu-id="531b1-480">Mannauðsþjónusta</span><span class="sxs-lookup"><span data-stu-id="531b1-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-481">CC002</span><span class="sxs-lookup"><span data-stu-id="531b1-481">CC002</span></span></td>
<td><span data-ttu-id="531b1-482">Fjármál</span><span class="sxs-lookup"><span data-stu-id="531b1-482">Finance</span></span></td>
<td><span data-ttu-id="531b1-483">35</span><span class="sxs-lookup"><span data-stu-id="531b1-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-484">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-484">CC003</span></span></td>
<td><span data-ttu-id="531b1-485">Smölun</span><span class="sxs-lookup"><span data-stu-id="531b1-485">Assembly</span></span></td>
<td><span data-ttu-id="531b1-486">55</span><span class="sxs-lookup"><span data-stu-id="531b1-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-487">CC004</span><span class="sxs-lookup"><span data-stu-id="531b1-487">CC004</span></span></td>
<td><span data-ttu-id="531b1-488">Pakkning</span><span class="sxs-lookup"><span data-stu-id="531b1-488">Packaging</span></span></td>
<td><span data-ttu-id="531b1-489">10</span><span class="sxs-lookup"><span data-stu-id="531b1-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="531b1-490">Kostnaðarhlutir CC002 Fjármál leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="531b1-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="531b1-491">Stofnað er tölfræðilegt víddarstak sem kallast Fjármálaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="531b1-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="531b1-492">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-492">Cost object</span></span></th>
<th><span data-ttu-id="531b1-493">Fjármálaþjónusta</span><span class="sxs-lookup"><span data-stu-id="531b1-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-494">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-494">CC003</span></span></td>
<td><span data-ttu-id="531b1-495">Smölun</span><span class="sxs-lookup"><span data-stu-id="531b1-495">Assembly</span></span></td>
<td><span data-ttu-id="531b1-496">65</span><span class="sxs-lookup"><span data-stu-id="531b1-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-497">CC004</span><span class="sxs-lookup"><span data-stu-id="531b1-497">CC004</span></span></td>
<td><span data-ttu-id="531b1-498">Pakkning</span><span class="sxs-lookup"><span data-stu-id="531b1-498">Packaging</span></span></td>
<td><span data-ttu-id="531b1-499">35</span><span class="sxs-lookup"><span data-stu-id="531b1-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="531b1-500">Kostnaðarhlutir CC003 Samsetning leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="531b1-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="531b1-501">Meðlimur tölfræðilega víddar sem kallast Mannauður verk er stofnað til að mælvíddarstaka notuðum magnitude.</span><span class="sxs-lookup"><span data-stu-id="531b1-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="531b1-502">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-502">Cost object</span></span></th>
<th><span data-ttu-id="531b1-503">Samsetningarþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="531b1-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-504">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-504">Prod 1</span></span></td>
<td><span data-ttu-id="531b1-505">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-505">Product 1</span></span></td>
<td><span data-ttu-id="531b1-506">60</span><span class="sxs-lookup"><span data-stu-id="531b1-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-507">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-507">Prod 2</span></span></td>
<td><span data-ttu-id="531b1-508">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-508">Product 2</span></span></td>
<td><span data-ttu-id="531b1-509">20</span><span class="sxs-lookup"><span data-stu-id="531b1-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="531b1-510">Kostnaðarhlutir CC004 Umbúðir leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="531b1-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="531b1-511">Stofnað er tölfræðilegt víddarstak sem kallast Umbúðaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="531b1-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="531b1-512">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-512">Cost object</span></span></th>
<th><span data-ttu-id="531b1-513">Umbúðaþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="531b1-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-514">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-514">Prod 1</span></span></td>
<td><span data-ttu-id="531b1-515">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-515">Product 1</span></span></td>
<td><span data-ttu-id="531b1-516">80</span><span class="sxs-lookup"><span data-stu-id="531b1-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-517">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-517">Prod 2</span></span></td>
<td><span data-ttu-id="531b1-518">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-518">Product 2</span></span></td>
<td><span data-ttu-id="531b1-519">sept</span><span class="sxs-lookup"><span data-stu-id="531b1-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="531b1-520">Í Finance and Operations er hægt að afleiða tölfræðiaðgerðir eins og framleiðslutíma sem vara notar frá upprunagögnum.</span><span class="sxs-lookup"><span data-stu-id="531b1-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="531b1-521">Nánari upplýsingar er að finna í [Veitusniðmát tölfræðiaðgerðar](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="531b1-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="531b1-522">Eftirfarandi tafla sýnir niðurstöður þegar mannauðsþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="531b1-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="531b1-523">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-523">Cost object</span></span></th>
<th><span data-ttu-id="531b1-524">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="531b1-524">Magnitude</span></span></th>
<th><span data-ttu-id="531b1-525">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="531b1-525">Allocation factor</span></span></th>
<th><span data-ttu-id="531b1-526">Upphæð</span><span class="sxs-lookup"><span data-stu-id="531b1-526">Amount</span></span></th>
<th><span data-ttu-id="531b1-527">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="531b1-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-528">CC002</span><span class="sxs-lookup"><span data-stu-id="531b1-528">CC002</span></span></td>
<td><span data-ttu-id="531b1-529">Fjármál</span><span class="sxs-lookup"><span data-stu-id="531b1-529">Finance</span></span></td>
<td><span data-ttu-id="531b1-530">35</span><span class="sxs-lookup"><span data-stu-id="531b1-530">35</span></span></td>
<td><span data-ttu-id="531b1-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="531b1-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="531b1-532">175.00</span><span class="sxs-lookup"><span data-stu-id="531b1-532">175.00</span></span></td>
<td><span data-ttu-id="531b1-533">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-534">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-534">CC003</span></span></td>
<td><span data-ttu-id="531b1-535">Smölun</span><span class="sxs-lookup"><span data-stu-id="531b1-535">Assembly</span></span></td>
<td><span data-ttu-id="531b1-536">55</span><span class="sxs-lookup"><span data-stu-id="531b1-536">55</span></span></td>
<td><span data-ttu-id="531b1-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="531b1-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="531b1-538">275.00</span><span class="sxs-lookup"><span data-stu-id="531b1-538">275.00</span></span></td>
<td><span data-ttu-id="531b1-539">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-540">CC004</span><span class="sxs-lookup"><span data-stu-id="531b1-540">CC004</span></span></td>
<td><span data-ttu-id="531b1-541">Pakkning</span><span class="sxs-lookup"><span data-stu-id="531b1-541">Packaging</span></span></td>
<td><span data-ttu-id="531b1-542">10</span><span class="sxs-lookup"><span data-stu-id="531b1-542">10</span></span></td>
<td><span data-ttu-id="531b1-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="531b1-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="531b1-544">50,00</span><span class="sxs-lookup"><span data-stu-id="531b1-544">50.00</span></span></td>
<td><span data-ttu-id="531b1-545">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-546">CC002</span><span class="sxs-lookup"><span data-stu-id="531b1-546">CC002</span></span></td>
<td><span data-ttu-id="531b1-547">Fjármál</span><span class="sxs-lookup"><span data-stu-id="531b1-547">Finance</span></span></td>
<td><span data-ttu-id="531b1-548">35</span><span class="sxs-lookup"><span data-stu-id="531b1-548">35</span></span></td>
<td><span data-ttu-id="531b1-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="531b1-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="531b1-550">436.00</span><span class="sxs-lookup"><span data-stu-id="531b1-550">436.00</span></span></td>
<td><span data-ttu-id="531b1-551">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-552">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-552">CC003</span></span></td>
<td><span data-ttu-id="531b1-553">Smölun</span><span class="sxs-lookup"><span data-stu-id="531b1-553">Assembly</span></span></td>
<td><span data-ttu-id="531b1-554">55</span><span class="sxs-lookup"><span data-stu-id="531b1-554">55</span></span></td>
<td><span data-ttu-id="531b1-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="531b1-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="531b1-556">685.14</span><span class="sxs-lookup"><span data-stu-id="531b1-556">685.14</span></span></td>
<td><span data-ttu-id="531b1-557">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-558">CC004</span><span class="sxs-lookup"><span data-stu-id="531b1-558">CC004</span></span></td>
<td><span data-ttu-id="531b1-559">Pakkning</span><span class="sxs-lookup"><span data-stu-id="531b1-559">Packaging</span></span></td>
<td><span data-ttu-id="531b1-560">10</span><span class="sxs-lookup"><span data-stu-id="531b1-560">10</span></span></td>
<td><span data-ttu-id="531b1-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="531b1-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="531b1-562">124.57</span><span class="sxs-lookup"><span data-stu-id="531b1-562">124.57</span></span></td>
<td><span data-ttu-id="531b1-563">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="531b1-564">Eftirfarandi tafla sýnir niðurstöður þegar Fjármálaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="531b1-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="531b1-565">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-565">Cost object</span></span></th>
<th><span data-ttu-id="531b1-566">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="531b1-566">Magnitude</span></span></th>
<th><span data-ttu-id="531b1-567">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="531b1-567">Allocation factor</span></span></th>
<th><span data-ttu-id="531b1-568">Upphæð</span><span class="sxs-lookup"><span data-stu-id="531b1-568">Amount</span></span></th>
<th><span data-ttu-id="531b1-569">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="531b1-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-570">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-570">CC003</span></span></td>
<td><span data-ttu-id="531b1-571">Smölun</span><span class="sxs-lookup"><span data-stu-id="531b1-571">Assembly</span></span></td>
<td><span data-ttu-id="531b1-572">65</span><span class="sxs-lookup"><span data-stu-id="531b1-572">65</span></span></td>
<td><span data-ttu-id="531b1-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="531b1-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="531b1-574">438.75</span><span class="sxs-lookup"><span data-stu-id="531b1-574">438.75</span></span></td>
<td><span data-ttu-id="531b1-575">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-576">CC004</span><span class="sxs-lookup"><span data-stu-id="531b1-576">CC004</span></span></td>
<td><span data-ttu-id="531b1-577">Pakkning</span><span class="sxs-lookup"><span data-stu-id="531b1-577">Packaging</span></span></td>
<td><span data-ttu-id="531b1-578">35</span><span class="sxs-lookup"><span data-stu-id="531b1-578">35</span></span></td>
<td><span data-ttu-id="531b1-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="531b1-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="531b1-580">236.25</span><span class="sxs-lookup"><span data-stu-id="531b1-580">236.25</span></span></td>
<td><span data-ttu-id="531b1-581">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-582">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-582">CC003</span></span></td>
<td><span data-ttu-id="531b1-583">Smölun</span><span class="sxs-lookup"><span data-stu-id="531b1-583">Assembly</span></span></td>
<td><span data-ttu-id="531b1-584">65</span><span class="sxs-lookup"><span data-stu-id="531b1-584">65</span></span></td>
<td><span data-ttu-id="531b1-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="531b1-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="531b1-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="531b1-586">5,297.69</span></span></td>
<td><span data-ttu-id="531b1-587">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-588">CC004</span><span class="sxs-lookup"><span data-stu-id="531b1-588">CC004</span></span></td>
<td><span data-ttu-id="531b1-589">Pakkning</span><span class="sxs-lookup"><span data-stu-id="531b1-589">Packaging</span></span></td>
<td><span data-ttu-id="531b1-590">35</span><span class="sxs-lookup"><span data-stu-id="531b1-590">35</span></span></td>
<td><span data-ttu-id="531b1-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="531b1-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="531b1-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="531b1-592">2,852.60</span></span></td>
<td><span data-ttu-id="531b1-593">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="531b1-594">Eftirfarandi tafla sýnir niðurstöður þegar Samsetningarþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="531b1-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="531b1-595">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-595">Cost object</span></span></th>
<th><span data-ttu-id="531b1-596">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="531b1-596">Magnitude</span></span></th>
<th><span data-ttu-id="531b1-597">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="531b1-597">Allocation factor</span></span></th>
<th><span data-ttu-id="531b1-598">Upphæð</span><span class="sxs-lookup"><span data-stu-id="531b1-598">Amount</span></span></th>
<th><span data-ttu-id="531b1-599">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="531b1-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-600">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-600">Prod 1</span></span></td>
<td><span data-ttu-id="531b1-601">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-601">Product 1</span></span></td>
<td><span data-ttu-id="531b1-602">60</span><span class="sxs-lookup"><span data-stu-id="531b1-602">60</span></span></td>
<td><span data-ttu-id="531b1-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="531b1-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="531b1-604">535.31</span><span class="sxs-lookup"><span data-stu-id="531b1-604">535.31</span></span></td>
<td><span data-ttu-id="531b1-605">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-606">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-606">Prod 2</span></span></td>
<td><span data-ttu-id="531b1-607">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-607">Product 2</span></span></td>
<td><span data-ttu-id="531b1-608">20</span><span class="sxs-lookup"><span data-stu-id="531b1-608">20</span></span></td>
<td><span data-ttu-id="531b1-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="531b1-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="531b1-610">178.44</span><span class="sxs-lookup"><span data-stu-id="531b1-610">178.44</span></span></td>
<td><span data-ttu-id="531b1-611">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-612">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-612">Prod 1</span></span></td>
<td><span data-ttu-id="531b1-613">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-613">Product 1</span></span></td>
<td><span data-ttu-id="531b1-614">60</span><span class="sxs-lookup"><span data-stu-id="531b1-614">60</span></span></td>
<td><span data-ttu-id="531b1-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="531b1-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="531b1-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="531b1-616">4,487.12</span></span></td>
<td><span data-ttu-id="531b1-617">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-618">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-618">Prod 2</span></span></td>
<td><span data-ttu-id="531b1-619">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-619">Product 2</span></span></td>
<td><span data-ttu-id="531b1-620">20</span><span class="sxs-lookup"><span data-stu-id="531b1-620">20</span></span></td>
<td><span data-ttu-id="531b1-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="531b1-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="531b1-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="531b1-622">1,495.71</span></span></td>
<td><span data-ttu-id="531b1-623">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="531b1-624">Eftirfarandi tafla sýnir niðurstöður þegar Umbúðaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="531b1-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="531b1-625">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-625">Cost object</span></span></th>
<th><span data-ttu-id="531b1-626">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="531b1-626">Magnitude</span></span></th>
<th><span data-ttu-id="531b1-627">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="531b1-627">Allocation factor</span></span></th>
<th><span data-ttu-id="531b1-628">Upphæð</span><span class="sxs-lookup"><span data-stu-id="531b1-628">Amount</span></span></th>
<th><span data-ttu-id="531b1-629">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="531b1-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-630">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-630">Prod 1</span></span></td>
<td><span data-ttu-id="531b1-631">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-631">Product 1</span></span></td>
<td><span data-ttu-id="531b1-632">80</span><span class="sxs-lookup"><span data-stu-id="531b1-632">80</span></span></td>
<td><span data-ttu-id="531b1-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="531b1-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="531b1-634">241.05</span><span class="sxs-lookup"><span data-stu-id="531b1-634">241.05</span></span></td>
<td><span data-ttu-id="531b1-635">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-636">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-636">Prod 2</span></span></td>
<td><span data-ttu-id="531b1-637">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-637">Product 2</span></span></td>
<td><span data-ttu-id="531b1-638">15</span><span class="sxs-lookup"><span data-stu-id="531b1-638">15</span></span></td>
<td><span data-ttu-id="531b1-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="531b1-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="531b1-640">45.20</span><span class="sxs-lookup"><span data-stu-id="531b1-640">45.20</span></span></td>
<td><span data-ttu-id="531b1-641">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-642">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-642">Prod 1</span></span></td>
<td><span data-ttu-id="531b1-643">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-643">Product 1</span></span></td>
<td><span data-ttu-id="531b1-644">80</span><span class="sxs-lookup"><span data-stu-id="531b1-644">80</span></span></td>
<td><span data-ttu-id="531b1-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="531b1-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="531b1-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="531b1-646">2,507.09</span></span></td>
<td><span data-ttu-id="531b1-647">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-648">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-648">Prod 2</span></span></td>
<td><span data-ttu-id="531b1-649">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-649">Product 2</span></span></td>
<td><span data-ttu-id="531b1-650">15</span><span class="sxs-lookup"><span data-stu-id="531b1-650">15</span></span></td>
<td><span data-ttu-id="531b1-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="531b1-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="531b1-652">470.08</span><span class="sxs-lookup"><span data-stu-id="531b1-652">470.08</span></span></td>
<td><span data-ttu-id="531b1-653">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="531b1-654">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="531b1-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="531b1-655">Færslubók</span><span class="sxs-lookup"><span data-stu-id="531b1-655">Journal</span></span></th>
<th><span data-ttu-id="531b1-656">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="531b1-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="531b1-657">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="531b1-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="531b1-658">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="531b1-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-659">00004</span><span class="sxs-lookup"><span data-stu-id="531b1-659">00004</span></span></td>
<td><span data-ttu-id="531b1-660">Færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="531b1-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="531b1-661">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="531b1-661">Fiscal</span></span></td>
<td><span data-ttu-id="531b1-662">2017</span><span class="sxs-lookup"><span data-stu-id="531b1-662">2017</span></span></td>
<td><span data-ttu-id="531b1-663">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="531b1-663">Period 1</span></span></td>
<td><span data-ttu-id="531b1-664">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="531b1-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="531b1-665">Færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="531b1-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="531b1-666">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="531b1-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="531b1-667">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="531b1-668">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="531b1-668">Cost element</span></span></th>
<th><span data-ttu-id="531b1-669">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="531b1-669">Cost behavior</span></span></th>
<th><span data-ttu-id="531b1-670">Upphæð</span><span class="sxs-lookup"><span data-stu-id="531b1-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-671">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="531b1-672">CC001</span><span class="sxs-lookup"><span data-stu-id="531b1-672">CC001</span></span></td>
<td><span data-ttu-id="531b1-673">Mannauður</span><span class="sxs-lookup"><span data-stu-id="531b1-673">HR</span></span></td>
<td><span data-ttu-id="531b1-674">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-674">10001</span></span></td>
<td><span data-ttu-id="531b1-675">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-675">Electricity</span></span></td>
<td><span data-ttu-id="531b1-676">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-676">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-677">500,00</span><span class="sxs-lookup"><span data-stu-id="531b1-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-678">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="531b1-679">CC001</span><span class="sxs-lookup"><span data-stu-id="531b1-679">CC001</span></span></td>
<td><span data-ttu-id="531b1-680">Mannauður</span><span class="sxs-lookup"><span data-stu-id="531b1-680">HR</span></span></td>
<td><span data-ttu-id="531b1-681">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-681">10001</span></span></td>
<td><span data-ttu-id="531b1-682">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-682">Electricity</span></span></td>
<td><span data-ttu-id="531b1-683">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-683">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="531b1-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-685">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="531b1-686">CC002</span><span class="sxs-lookup"><span data-stu-id="531b1-686">CC002</span></span></td>
<td><span data-ttu-id="531b1-687">Fjármál</span><span class="sxs-lookup"><span data-stu-id="531b1-687">Finance</span></span></td>
<td><span data-ttu-id="531b1-688">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-688">10001</span></span></td>
<td><span data-ttu-id="531b1-689">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-689">Electricity</span></span></td>
<td><span data-ttu-id="531b1-690">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-690">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-691">675.00</span><span class="sxs-lookup"><span data-stu-id="531b1-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-692">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="531b1-693">CC002</span><span class="sxs-lookup"><span data-stu-id="531b1-693">CC002</span></span></td>
<td><span data-ttu-id="531b1-694">Fjármál</span><span class="sxs-lookup"><span data-stu-id="531b1-694">Finance</span></span></td>
<td><span data-ttu-id="531b1-695">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-695">10001</span></span></td>
<td><span data-ttu-id="531b1-696">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-696">Electricity</span></span></td>
<td><span data-ttu-id="531b1-697">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-697">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="531b1-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-699">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="531b1-700">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-700">CC003</span></span></td>
<td><span data-ttu-id="531b1-701">Smölun</span><span class="sxs-lookup"><span data-stu-id="531b1-701">Assembly</span></span></td>
<td><span data-ttu-id="531b1-702">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-702">10001</span></span></td>
<td><span data-ttu-id="531b1-703">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-703">Electricity</span></span></td>
<td><span data-ttu-id="531b1-704">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-704">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-705">713.75</span><span class="sxs-lookup"><span data-stu-id="531b1-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-706">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="531b1-707">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-707">CC003</span></span></td>
<td><span data-ttu-id="531b1-708">Smölun</span><span class="sxs-lookup"><span data-stu-id="531b1-708">Assembly</span></span></td>
<td><span data-ttu-id="531b1-709">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-709">10001</span></span></td>
<td><span data-ttu-id="531b1-710">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-710">Electricity</span></span></td>
<td><span data-ttu-id="531b1-711">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-711">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="531b1-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-713">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="531b1-714">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-714">CC003</span></span></td>
<td><span data-ttu-id="531b1-715">Pakkning</span><span class="sxs-lookup"><span data-stu-id="531b1-715">Packaging</span></span></td>
<td><span data-ttu-id="531b1-716">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-716">10001</span></span></td>
<td><span data-ttu-id="531b1-717">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-717">Electricity</span></span></td>
<td><span data-ttu-id="531b1-718">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-718">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-719">286.25</span><span class="sxs-lookup"><span data-stu-id="531b1-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-720">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="531b1-721">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-721">CC003</span></span></td>
<td><span data-ttu-id="531b1-722">Pakkning</span><span class="sxs-lookup"><span data-stu-id="531b1-722">Packaging</span></span></td>
<td><span data-ttu-id="531b1-723">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-723">10001</span></span></td>
<td><span data-ttu-id="531b1-724">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-724">Electricity</span></span></td>
<td><span data-ttu-id="531b1-725">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-725">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="531b1-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-727">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="531b1-728">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-728">Prod 1</span></span></td>
<td><span data-ttu-id="531b1-729">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-729">Product 1</span></span></td>
<td><span data-ttu-id="531b1-730">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-730">10001</span></span></td>
<td><span data-ttu-id="531b1-731">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-731">Electricity</span></span></td>
<td><span data-ttu-id="531b1-732">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-732">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-733">776.36</span><span class="sxs-lookup"><span data-stu-id="531b1-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-734">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="531b1-735">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-735">Prod 1</span></span></td>
<td><span data-ttu-id="531b1-736">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-736">Product 1</span></span></td>
<td><span data-ttu-id="531b1-737">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-737">10001</span></span></td>
<td><span data-ttu-id="531b1-738">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-738">Electricity</span></span></td>
<td><span data-ttu-id="531b1-739">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-739">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="531b1-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-741">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="531b1-742">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-742">Prod 2</span></span></td>
<td><span data-ttu-id="531b1-743">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-743">Product 1</span></span></td>
<td><span data-ttu-id="531b1-744">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-744">10001</span></span></td>
<td><span data-ttu-id="531b1-745">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-745">Electricity</span></span></td>
<td><span data-ttu-id="531b1-746">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-746">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-747">223.64</span><span class="sxs-lookup"><span data-stu-id="531b1-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-748">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="531b1-749">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-749">Prod 2</span></span></td>
<td><span data-ttu-id="531b1-750">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-750">Product 1</span></span></td>
<td><span data-ttu-id="531b1-751">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-751">10001</span></span></td>
<td><span data-ttu-id="531b1-752">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-752">Electricity</span></span></td>
<td><span data-ttu-id="531b1-753">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-753">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="531b1-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="531b1-755">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="531b1-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="531b1-756">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="531b1-757">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="531b1-757">Cost element</span></span></th>
<th><span data-ttu-id="531b1-758">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="531b1-758">Cost behavior</span></span></th>
<th><span data-ttu-id="531b1-759">Upphæð</span><span class="sxs-lookup"><span data-stu-id="531b1-759">Amount</span></span></th>
<th><span data-ttu-id="531b1-760">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="531b1-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="531b1-761">CC001</span><span class="sxs-lookup"><span data-stu-id="531b1-761">CC001</span></span></td>
<td><span data-ttu-id="531b1-762">Mannauður</span><span class="sxs-lookup"><span data-stu-id="531b1-762">HR</span></span></td>
<td><span data-ttu-id="531b1-763">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-763">10001</span></span></td>
<td><span data-ttu-id="531b1-764">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-764">Electricity</span></span></td>
<td><span data-ttu-id="531b1-765">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-765">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="531b1-766">-500.00</span></span></td>
<td><span data-ttu-id="531b1-767">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-768">CC002</span><span class="sxs-lookup"><span data-stu-id="531b1-768">CC002</span></span></td>
<td><span data-ttu-id="531b1-769">Fjármál</span><span class="sxs-lookup"><span data-stu-id="531b1-769">Finance</span></span></td>
<td><span data-ttu-id="531b1-770">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-770">10001</span></span></td>
<td><span data-ttu-id="531b1-771">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-771">Electricity</span></span></td>
<td><span data-ttu-id="531b1-772">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-772">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-773">175.00</span><span class="sxs-lookup"><span data-stu-id="531b1-773">175.00</span></span></td>
<td><span data-ttu-id="531b1-774">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-775">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-775">CC003</span></span></td>
<td><span data-ttu-id="531b1-776">Smölun</span><span class="sxs-lookup"><span data-stu-id="531b1-776">Assembly</span></span></td>
<td><span data-ttu-id="531b1-777">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-777">10001</span></span></td>
<td><span data-ttu-id="531b1-778">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-778">Electricity</span></span></td>
<td><span data-ttu-id="531b1-779">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-779">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-780">275.00</span><span class="sxs-lookup"><span data-stu-id="531b1-780">275.00</span></span></td>
<td><span data-ttu-id="531b1-781">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-782">CC004</span><span class="sxs-lookup"><span data-stu-id="531b1-782">CC004</span></span></td>
<td><span data-ttu-id="531b1-783">Pakkning</span><span class="sxs-lookup"><span data-stu-id="531b1-783">Packaging</span></span></td>
<td><span data-ttu-id="531b1-784">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-784">10001</span></span></td>
<td><span data-ttu-id="531b1-785">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-785">Electricity</span></span></td>
<td><span data-ttu-id="531b1-786">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-786">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-787">50,00</span><span class="sxs-lookup"><span data-stu-id="531b1-787">50,00</span></span></td>
<td><span data-ttu-id="531b1-788">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-789">CC001</span><span class="sxs-lookup"><span data-stu-id="531b1-789">CC001</span></span></td>
<td><span data-ttu-id="531b1-790">Mannauður</span><span class="sxs-lookup"><span data-stu-id="531b1-790">HR</span></span></td>
<td><span data-ttu-id="531b1-791">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-791">10001</span></span></td>
<td><span data-ttu-id="531b1-792">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-792">Electricity</span></span></td>
<td><span data-ttu-id="531b1-793">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-793">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="531b1-794">-1,245.71</span></span></td>
<td><span data-ttu-id="531b1-795">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-796">CC002</span><span class="sxs-lookup"><span data-stu-id="531b1-796">CC002</span></span></td>
<td><span data-ttu-id="531b1-797">Fjármál</span><span class="sxs-lookup"><span data-stu-id="531b1-797">Finance</span></span></td>
<td><span data-ttu-id="531b1-798">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-798">10001</span></span></td>
<td><span data-ttu-id="531b1-799">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-799">Electricity</span></span></td>
<td><span data-ttu-id="531b1-800">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-800">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-801">436.00</span><span class="sxs-lookup"><span data-stu-id="531b1-801">436.00</span></span></td>
<td><span data-ttu-id="531b1-802">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-803">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-803">CC003</span></span></td>
<td><span data-ttu-id="531b1-804">Smölun</span><span class="sxs-lookup"><span data-stu-id="531b1-804">Assembly</span></span></td>
<td><span data-ttu-id="531b1-805">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-805">10001</span></span></td>
<td><span data-ttu-id="531b1-806">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-806">Electricity</span></span></td>
<td><span data-ttu-id="531b1-807">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-807">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-808">685.14</span><span class="sxs-lookup"><span data-stu-id="531b1-808">685.14</span></span></td>
<td><span data-ttu-id="531b1-809">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-810">CC004</span><span class="sxs-lookup"><span data-stu-id="531b1-810">CC004</span></span></td>
<td><span data-ttu-id="531b1-811">Pakkning</span><span class="sxs-lookup"><span data-stu-id="531b1-811">Packaging</span></span></td>
<td><span data-ttu-id="531b1-812">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-812">10001</span></span></td>
<td><span data-ttu-id="531b1-813">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-813">Electricity</span></span></td>
<td><span data-ttu-id="531b1-814">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-814">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-815">124.57</span><span class="sxs-lookup"><span data-stu-id="531b1-815">124.57</span></span></td>
<td><span data-ttu-id="531b1-816">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-817">CC002</span><span class="sxs-lookup"><span data-stu-id="531b1-817">CC002</span></span></td>
<td><span data-ttu-id="531b1-818">Fjármál</span><span class="sxs-lookup"><span data-stu-id="531b1-818">Finance</span></span></td>
<td><span data-ttu-id="531b1-819">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-819">10001</span></span></td>
<td><span data-ttu-id="531b1-820">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-820">Electricity</span></span></td>
<td><span data-ttu-id="531b1-821">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-821">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="531b1-822">-675.00</span></span></td>
<td><span data-ttu-id="531b1-823">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-824">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-824">CC003</span></span></td>
<td><span data-ttu-id="531b1-825">Smölun</span><span class="sxs-lookup"><span data-stu-id="531b1-825">Assembly</span></span></td>
<td><span data-ttu-id="531b1-826">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-826">10001</span></span></td>
<td><span data-ttu-id="531b1-827">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-827">Electricity</span></span></td>
<td><span data-ttu-id="531b1-828">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-828">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-829">438.75</span><span class="sxs-lookup"><span data-stu-id="531b1-829">438.75</span></span></td>
<td><span data-ttu-id="531b1-830">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-831">CC004</span><span class="sxs-lookup"><span data-stu-id="531b1-831">CC004</span></span></td>
<td><span data-ttu-id="531b1-832">Pakkning</span><span class="sxs-lookup"><span data-stu-id="531b1-832">Packaging</span></span></td>
<td><span data-ttu-id="531b1-833">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-833">10001</span></span></td>
<td><span data-ttu-id="531b1-834">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-834">Electricity</span></span></td>
<td><span data-ttu-id="531b1-835">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-835">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-836">236.25</span><span class="sxs-lookup"><span data-stu-id="531b1-836">236.25</span></span></td>
<td><span data-ttu-id="531b1-837">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-838">CC002</span><span class="sxs-lookup"><span data-stu-id="531b1-838">CC002</span></span></td>
<td><span data-ttu-id="531b1-839">Fjármál</span><span class="sxs-lookup"><span data-stu-id="531b1-839">Finance</span></span></td>
<td><span data-ttu-id="531b1-840">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-840">10001</span></span></td>
<td><span data-ttu-id="531b1-841">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-841">Electricity</span></span></td>
<td><span data-ttu-id="531b1-842">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-842">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="531b1-843">-8,150.29</span></span></td>
<td><span data-ttu-id="531b1-844">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-845">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-845">CC003</span></span></td>
<td><span data-ttu-id="531b1-846">Smölun</span><span class="sxs-lookup"><span data-stu-id="531b1-846">Assembly</span></span></td>
<td><span data-ttu-id="531b1-847">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-847">10001</span></span></td>
<td><span data-ttu-id="531b1-848">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-848">Electricity</span></span></td>
<td><span data-ttu-id="531b1-849">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-849">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="531b1-850">5,297.69</span></span></td>
<td><span data-ttu-id="531b1-851">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-852">CC004</span><span class="sxs-lookup"><span data-stu-id="531b1-852">CC004</span></span></td>
<td><span data-ttu-id="531b1-853">Pakkning</span><span class="sxs-lookup"><span data-stu-id="531b1-853">Packaging</span></span></td>
<td><span data-ttu-id="531b1-854">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-854">10001</span></span></td>
<td><span data-ttu-id="531b1-855">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-855">Electricity</span></span></td>
<td><span data-ttu-id="531b1-856">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-856">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="531b1-857">2,852.60</span></span></td>
<td><span data-ttu-id="531b1-858">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-859">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-859">CC003</span></span></td>
<td><span data-ttu-id="531b1-860">Smölun</span><span class="sxs-lookup"><span data-stu-id="531b1-860">Assembly</span></span></td>
<td><span data-ttu-id="531b1-861">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-861">10001</span></span></td>
<td><span data-ttu-id="531b1-862">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-862">Electricity</span></span></td>
<td><span data-ttu-id="531b1-863">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-863">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="531b1-864">-713.75</span></span></td>
<td><span data-ttu-id="531b1-865">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-866">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-866">Prod 1</span></span></td>
<td><span data-ttu-id="531b1-867">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-867">Product 1</span></span></td>
<td><span data-ttu-id="531b1-868">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-868">10001</span></span></td>
<td><span data-ttu-id="531b1-869">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-869">Electricity</span></span></td>
<td><span data-ttu-id="531b1-870">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-870">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-871">535.31</span><span class="sxs-lookup"><span data-stu-id="531b1-871">535.31</span></span></td>
<td><span data-ttu-id="531b1-872">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-873">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-873">Prod 2</span></span></td>
<td><span data-ttu-id="531b1-874">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-874">Product 2</span></span></td>
<td><span data-ttu-id="531b1-875">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-875">10001</span></span></td>
<td><span data-ttu-id="531b1-876">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-876">Electricity</span></span></td>
<td><span data-ttu-id="531b1-877">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-877">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-878">178.44</span><span class="sxs-lookup"><span data-stu-id="531b1-878">178.44</span></span></td>
<td><span data-ttu-id="531b1-879">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-880">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-880">CC003</span></span></td>
<td><span data-ttu-id="531b1-881">Smölun</span><span class="sxs-lookup"><span data-stu-id="531b1-881">Assembly</span></span></td>
<td><span data-ttu-id="531b1-882">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-882">10001</span></span></td>
<td><span data-ttu-id="531b1-883">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-883">Electricity</span></span></td>
<td><span data-ttu-id="531b1-884">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-884">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="531b1-885">-5,982.83</span></span></td>
<td><span data-ttu-id="531b1-886">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-887">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-887">Prod 1</span></span></td>
<td><span data-ttu-id="531b1-888">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-888">Product 1</span></span></td>
<td><span data-ttu-id="531b1-889">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-889">10001</span></span></td>
<td><span data-ttu-id="531b1-890">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-890">Electricity</span></span></td>
<td><span data-ttu-id="531b1-891">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-891">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="531b1-892">4,487.12</span></span></td>
<td><span data-ttu-id="531b1-893">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-894">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-894">Prod 2</span></span></td>
<td><span data-ttu-id="531b1-895">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-895">Product 2</span></span></td>
<td><span data-ttu-id="531b1-896">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-896">10001</span></span></td>
<td><span data-ttu-id="531b1-897">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-897">Electricity</span></span></td>
<td><span data-ttu-id="531b1-898">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-898">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="531b1-899">1,495.71</span></span></td>
<td><span data-ttu-id="531b1-900">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-901">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-901">CC003</span></span></td>
<td><span data-ttu-id="531b1-902">Smölun</span><span class="sxs-lookup"><span data-stu-id="531b1-902">Assembly</span></span></td>
<td><span data-ttu-id="531b1-903">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-903">10001</span></span></td>
<td><span data-ttu-id="531b1-904">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-904">Electricity</span></span></td>
<td><span data-ttu-id="531b1-905">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-905">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="531b1-906">-286.25</span></span></td>
<td><span data-ttu-id="531b1-907">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-908">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-908">Prod 1</span></span></td>
<td><span data-ttu-id="531b1-909">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-909">Product 1</span></span></td>
<td><span data-ttu-id="531b1-910">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-910">10001</span></span></td>
<td><span data-ttu-id="531b1-911">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-911">Electricity</span></span></td>
<td><span data-ttu-id="531b1-912">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-912">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-913">241.05</span><span class="sxs-lookup"><span data-stu-id="531b1-913">241.05</span></span></td>
<td><span data-ttu-id="531b1-914">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-915">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-915">Prod 2</span></span></td>
<td><span data-ttu-id="531b1-916">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-916">Product 2</span></span></td>
<td><span data-ttu-id="531b1-917">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-917">10001</span></span></td>
<td><span data-ttu-id="531b1-918">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-918">Electricity</span></span></td>
<td><span data-ttu-id="531b1-919">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-919">Fixed cost</span></span></td>
<td><span data-ttu-id="531b1-920">45.20</span><span class="sxs-lookup"><span data-stu-id="531b1-920">45.20</span></span></td>
<td><span data-ttu-id="531b1-921">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-922">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-922">CC003</span></span></td>
<td><span data-ttu-id="531b1-923">Smölun</span><span class="sxs-lookup"><span data-stu-id="531b1-923">Assembly</span></span></td>
<td><span data-ttu-id="531b1-924">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-924">10001</span></span></td>
<td><span data-ttu-id="531b1-925">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-925">Electricity</span></span></td>
<td><span data-ttu-id="531b1-926">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-926">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="531b1-927">-2,977.17</span></span></td>
<td><span data-ttu-id="531b1-928">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-929">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-929">Prod 1</span></span></td>
<td><span data-ttu-id="531b1-930">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-930">Product 1</span></span></td>
<td><span data-ttu-id="531b1-931">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-931">10001</span></span></td>
<td><span data-ttu-id="531b1-932">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-932">Electricity</span></span></td>
<td><span data-ttu-id="531b1-933">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-933">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="531b1-934">2,507.09</span></span></td>
<td><span data-ttu-id="531b1-935">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="531b1-936">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-936">Prod 2</span></span></td>
<td><span data-ttu-id="531b1-937">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-937">Product 2</span></span></td>
<td><span data-ttu-id="531b1-938">10001</span><span class="sxs-lookup"><span data-stu-id="531b1-938">10001</span></span></td>
<td><span data-ttu-id="531b1-939">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-939">Electricity</span></span></td>
<td><span data-ttu-id="531b1-940">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-940">Variable cost</span></span></td>
<td><span data-ttu-id="531b1-941">470.08</span><span class="sxs-lookup"><span data-stu-id="531b1-941">470.08</span></span></td>
<td><span data-ttu-id="531b1-942">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="531b1-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="531b1-943">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="531b1-943">Conclusion</span></span>
<span data-ttu-id="531b1-944">Í Fjárhagsbókhaldi er kostnaður upp á 10.000,00 fyrir rafmagn bókaður á kenni leppkostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="531b1-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="531b1-945">Þar af leiðandi munu kostnaðarbókarar vita að það þarf að úthluta þessum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="531b1-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="531b1-946">Í kostnaðarbókhaldi streymir kostnaður þvert á fyrirtækiseiningar og stig, samkvæmt þeim stefnum og reglum sem eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="531b1-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="531b1-947">Hver kostnaður hefur verið tengdur úthlutunargrunni sem veitir besta mat á úthlutun á kostnaði.</span><span class="sxs-lookup"><span data-stu-id="531b1-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="531b1-948">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="531b1-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="531b1-949">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="531b1-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="531b1-950">Samtala</span><span class="sxs-lookup"><span data-stu-id="531b1-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="531b1-951">CC099</span><span class="sxs-lookup"><span data-stu-id="531b1-951">CC099</span></span></th>
<th><span data-ttu-id="531b1-952">CC001</span><span class="sxs-lookup"><span data-stu-id="531b1-952">CC001</span></span></th>
<th><span data-ttu-id="531b1-953">CC002</span><span class="sxs-lookup"><span data-stu-id="531b1-953">CC002</span></span></th>
<th><span data-ttu-id="531b1-954">CC003</span><span class="sxs-lookup"><span data-stu-id="531b1-954">CC003</span></span></th>
<th><span data-ttu-id="531b1-955">CC004</span><span class="sxs-lookup"><span data-stu-id="531b1-955">CC004</span></span></th>
<th><span data-ttu-id="531b1-956">Verk 1</span><span class="sxs-lookup"><span data-stu-id="531b1-956">Proj 1</span></span></th>
<th><span data-ttu-id="531b1-957">Verk 2</span><span class="sxs-lookup"><span data-stu-id="531b1-957">Proj 2</span></span></th>
<th><span data-ttu-id="531b1-958">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="531b1-958">Prod 1</span></span></th>
<th><span data-ttu-id="531b1-959">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="531b1-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="531b1-960">10001 Rafmagn</span><span class="sxs-lookup"><span data-stu-id="531b1-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="531b1-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="531b1-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="531b1-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="531b1-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="531b1-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="531b1-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="531b1-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="531b1-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="531b1-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="531b1-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="531b1-970">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="531b1-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-971">0,00</span><span class="sxs-lookup"><span data-stu-id="531b1-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="531b1-972">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-973">0,00</span><span class="sxs-lookup"><span data-stu-id="531b1-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-974">0,00</span><span class="sxs-lookup"><span data-stu-id="531b1-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-975">0,00</span><span class="sxs-lookup"><span data-stu-id="531b1-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-976">0,00</span><span class="sxs-lookup"><span data-stu-id="531b1-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-977">0,00</span><span class="sxs-lookup"><span data-stu-id="531b1-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="531b1-978">776.36</span><span class="sxs-lookup"><span data-stu-id="531b1-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-979">223.64</span><span class="sxs-lookup"><span data-stu-id="531b1-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="531b1-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="531b1-981">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="531b1-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-982">000</span><span class="sxs-lookup"><span data-stu-id="531b1-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-983">0,00</span><span class="sxs-lookup"><span data-stu-id="531b1-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-984">0,00</span><span class="sxs-lookup"><span data-stu-id="531b1-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-985">0,00</span><span class="sxs-lookup"><span data-stu-id="531b1-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-986">0,00</span><span class="sxs-lookup"><span data-stu-id="531b1-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-987">30,00</span><span class="sxs-lookup"><span data-stu-id="531b1-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-988">10,00</span><span class="sxs-lookup"><span data-stu-id="531b1-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="531b1-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="531b1-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="531b1-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="531b1-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="531b1-992">Þetta efnisatriði sýnir hvernig fyrir aðalkostnaðareiningin 10001 Rafmagn flæðir í gegnum kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="531b1-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="531b1-993">Þar af leiðandi er þessum sameiginlega kostnaði úthlutað á lægsta stigið í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="531b1-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="531b1-994">Með öðrum orðum bera kostnaðarhlutir á lægsta stiginu kostnaðinn.</span><span class="sxs-lookup"><span data-stu-id="531b1-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="531b1-995">Ef þú þarft sjónrænt flæði kostnaðar á milli kostnaðarhluta er hægt að nota stefnureglur samantekins kostnaðar til að gera kostnaðarflæðið sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="531b1-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="531b1-996">Nánari upplýsingar er að finna í [Samantekt kostnaðar](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="531b1-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>




