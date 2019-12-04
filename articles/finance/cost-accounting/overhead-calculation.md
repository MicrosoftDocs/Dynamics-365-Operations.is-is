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
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 954e0669c3d24bcc20fe667c22b7dcc367aba1e7
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770805"
---
# <a name="overhead-calculation"></a><span data-ttu-id="33657-103">Útreikningur fastakostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33657-104">Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði.</span><span class="sxs-lookup"><span data-stu-id="33657-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="33657-105">Skýrsluskilgreining</span><span class="sxs-lookup"><span data-stu-id="33657-105">Term definition</span></span>
---------------

<span data-ttu-id="33657-106">Stjórnunarkostnaður er sá kostnaður sem stofnað er til fyrir rekstur fyrirtækis, en sem ekki er hægt að rekja beint til neinna sérstakrar starfsemi, vöru eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="33657-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="33657-107">Stjórnunarkostnaður veitir mikilvægan stuðning við myndun hagnaðarmyndandi verkþátta.</span><span class="sxs-lookup"><span data-stu-id="33657-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="33657-108">Hér eru nokkur dæmi um skilyrði:</span><span class="sxs-lookup"><span data-stu-id="33657-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="33657-109">Leiga</span><span class="sxs-lookup"><span data-stu-id="33657-109">Rent</span></span>
-   <span data-ttu-id="33657-110">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-110">Electricity</span></span>
-   <span data-ttu-id="33657-111">Stjórnunarkostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="33657-112">Yfirlit yfir útreikning fastakostnaðar</span><span class="sxs-lookup"><span data-stu-id="33657-112">Overhead calculation overview</span></span>
<span data-ttu-id="33657-113">Útreikningur fastakostnaðar keyrir reglur kostnaðarbókhalds í réttri röð.</span><span class="sxs-lookup"><span data-stu-id="33657-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="33657-114">Hægt er að keyra útreikning fastakostnaðar margsinnis fyrir sama fjárhagstímabil ef reglum kostnaðarbókhalds hefur verið breytt eða ákveðnar villur hafa fundist.</span><span class="sxs-lookup"><span data-stu-id="33657-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="33657-115">Hver keyrsla á útreikningi fastakostnaðar er geymd og fær einkvæmt útgáfukenni sem gerir kleift að bera saman útreikning í mismunandi útgáfum.</span><span class="sxs-lookup"><span data-stu-id="33657-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="33657-116">Kostnaðarfærslur sem útreikningur fastakostnaðar mynda fá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="33657-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="33657-117">Dagsetningin bókhald samsvarar lokadagsetning fjárhagstímabilsins sem er dagsetning reikningsskiladagsetning reikningsskila notað í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="33657-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="33657-118">Einkvæmt útgáfukenni samanstendur af eftirfarandi þáttum:</span><span class="sxs-lookup"><span data-stu-id="33657-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="33657-119">Gerð útgáfu</span><span class="sxs-lookup"><span data-stu-id="33657-119">Version type</span></span>
-   <span data-ttu-id="33657-120">Dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="33657-120">Date and time</span></span>
-   <span data-ttu-id="33657-121">Fjárhagur kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="33657-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="33657-122">Fjárhagsár</span><span class="sxs-lookup"><span data-stu-id="33657-122">Fiscal year</span></span>
-   <span data-ttu-id="33657-123">Reikningstímabil</span><span class="sxs-lookup"><span data-stu-id="33657-123">Fiscal period</span></span>

<span data-ttu-id="33657-124">Útreikningur fastakostnaðar er keyrður óháð því hver útgáfan er.</span><span class="sxs-lookup"><span data-stu-id="33657-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="33657-125">Þess vegna er hægt að reikna út áætlaða útgáfu á undan raunútgáfu.</span><span class="sxs-lookup"><span data-stu-id="33657-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="33657-126">Útreikningur fastakostnaðar samanstendur af fjórum skrefum, eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="33657-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="33657-127">Í hverju skrefi er færslubókarhaus stofnaður með bókarfærslum.</span><span class="sxs-lookup"><span data-stu-id="33657-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="33657-128">Þessi færslubókarhaus geymir inntaksgögn fyrir hvert útreikningsþrep.</span><span class="sxs-lookup"><span data-stu-id="33657-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="33657-129">Stefnur og reglur eru notaðar í hverri færslulínu og kostnaðarfærslur eru myndaðar sem úttak.</span><span class="sxs-lookup"><span data-stu-id="33657-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="33657-130">Þess vegna hefurðu ávallt fullan rekjanleika.</span><span class="sxs-lookup"><span data-stu-id="33657-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="33657-131">[![Útreikningur fastakostnaðar](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="33657-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="33657-132">Reikna og úthluta sameiginlegur kostnaði vegna rafmagns</span><span class="sxs-lookup"><span data-stu-id="33657-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="33657-133">Í Fjárhagsbókhaldi er ákveðinn kostnaður, eins og rafmagn, skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="33657-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="33657-134">Þar af leiðandi er nákvæmar innsýn rekstrarfélags ekki veitt fyrir kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="33657-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="33657-135">Í kostnaðarbókhaldi verður kostnaður að flæða í gegnum fyrirtækiseiningar til að veita rétta innsýn rekstrarfélags þvert á allar fyrirtækiseiningar og stig.</span><span class="sxs-lookup"><span data-stu-id="33657-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="33657-136">Þetta flæði verður að byggja á annaðhvort nákvæmri færslu notkunar eða sanngjarnri matsreglu.</span><span class="sxs-lookup"><span data-stu-id="33657-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="33657-137">Í fjárhagnum er hægt að bóka rafmagnskostnað eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="33657-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="33657-138">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="33657-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="33657-139">Kostnaðarstaður</span><span class="sxs-lookup"><span data-stu-id="33657-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="33657-140">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="33657-140">Main account</span></span></th>
<th><span data-ttu-id="33657-141">Upphæð í bókhaldsgjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="33657-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-142">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="33657-143">CC099</span><span class="sxs-lookup"><span data-stu-id="33657-143">CC099</span></span></td>
<td><span data-ttu-id="33657-144">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="33657-144">Default cost center</span></span></td>
<td><span data-ttu-id="33657-145">10001</span><span class="sxs-lookup"><span data-stu-id="33657-145">10001</span></span></td>
<td><span data-ttu-id="33657-146">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-146">Electricity</span></span></td>
<td><span data-ttu-id="33657-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="33657-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="33657-148">Skref 1: Keyra útreikning kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="33657-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="33657-149">Sjálfvirkt er að þegar kostnaðarfærslur eru fluttar úr grunngögnum fái þær flokkun kostnaðarhegðunar **Óflokkað** í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="33657-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="33657-150">Með því að nota stefnureglur kostnaðarhegðunar er hægt að endurflokka kostnaðarfærslur sem annaðhvort **Fastan kostnað** eða **Breytilegan kostnað**.</span><span class="sxs-lookup"><span data-stu-id="33657-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="33657-151">Tilgreinið reglu kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="33657-151">Define the cost behavior rule</span></span>

<span data-ttu-id="33657-152">Í sumum tilfellum er hluti af kostnaði föst þóknun og eftirstandandi kostnaður byggist á notkun.</span><span class="sxs-lookup"><span data-stu-id="33657-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="33657-153">Rafmagnsreikningar stemma oft við þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="33657-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="33657-154">Þegar tiltekin föst þóknun hefur verið greidd, er greitt fyrir notkun á kílóvattklukkustund (Kwh).</span><span class="sxs-lookup"><span data-stu-id="33657-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="33657-155">Til dæmis ef föst kostnaðarþóknun er 1000.00 sýnir þetta hvernig regla kostnaðarhegðunar er skilgreind:</span><span class="sxs-lookup"><span data-stu-id="33657-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="33657-156">Föst upphæð 1.000,00</span><span class="sxs-lookup"><span data-stu-id="33657-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="33657-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="33657-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="33657-158">1000.01 &lt; N = Breyta</span><span class="sxs-lookup"><span data-stu-id="33657-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="33657-159">Færslubók</span><span class="sxs-lookup"><span data-stu-id="33657-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="33657-160">Færslubók</span><span class="sxs-lookup"><span data-stu-id="33657-160">Journal</span></span></th>
<th><span data-ttu-id="33657-161">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="33657-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="33657-162">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="33657-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="33657-163">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="33657-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-164">00001</span><span class="sxs-lookup"><span data-stu-id="33657-164">00001</span></span></td>
<td><span data-ttu-id="33657-165">Færslubók útreiknings fyrir kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="33657-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="33657-166">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="33657-166">Fiscal</span></span></td>
<td><span data-ttu-id="33657-167">2017</span><span class="sxs-lookup"><span data-stu-id="33657-167">2017</span></span></td>
<td><span data-ttu-id="33657-168">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="33657-168">Period 1</span></span></td>
<td><span data-ttu-id="33657-169">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="33657-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="33657-170">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="33657-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="33657-171">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="33657-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="33657-172">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="33657-173">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="33657-173">Cost element</span></span></th>
<th><span data-ttu-id="33657-174">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="33657-174">Cost behavior</span></span></th>
<th><span data-ttu-id="33657-175">Upphæð</span><span class="sxs-lookup"><span data-stu-id="33657-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-176">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="33657-177">CC099</span><span class="sxs-lookup"><span data-stu-id="33657-177">CC099</span></span></td>
<td><span data-ttu-id="33657-178">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="33657-178">Default cost center</span></span></td>
<td><span data-ttu-id="33657-179">10001</span><span class="sxs-lookup"><span data-stu-id="33657-179">10001</span></span></td>
<td><span data-ttu-id="33657-180">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-180">Electricity</span></span></td>
<td><span data-ttu-id="33657-181">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="33657-181">Unclassified</span></span></td>
<td><span data-ttu-id="33657-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="33657-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="33657-183">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="33657-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="33657-184">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="33657-185">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="33657-185">Cost element</span></span></th>
<th><span data-ttu-id="33657-186">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="33657-186">Cost behavior</span></span></th>
<th><span data-ttu-id="33657-187">Upphæð</span><span class="sxs-lookup"><span data-stu-id="33657-187">Amount</span></span></th>
<th><span data-ttu-id="33657-188">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="33657-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-189">CC099</span><span class="sxs-lookup"><span data-stu-id="33657-189">CC099</span></span></td>
<td><span data-ttu-id="33657-190">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="33657-190">Default cost center</span></span></td>
<td><span data-ttu-id="33657-191">10001</span><span class="sxs-lookup"><span data-stu-id="33657-191">10001</span></span></td>
<td><span data-ttu-id="33657-192">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-192">Electricity</span></span></td>
<td><span data-ttu-id="33657-193">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="33657-193">Unclassified</span></span></td>
<td><span data-ttu-id="33657-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="33657-194">10,000.00</span></span></td>
<td><span data-ttu-id="33657-195">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-196">CC099</span><span class="sxs-lookup"><span data-stu-id="33657-196">CC099</span></span></td>
<td><span data-ttu-id="33657-197">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="33657-197">Default cost center</span></span></td>
<td><span data-ttu-id="33657-198">10001</span><span class="sxs-lookup"><span data-stu-id="33657-198">10001</span></span></td>
<td><span data-ttu-id="33657-199">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-199">Electricity</span></span></td>
<td><span data-ttu-id="33657-200">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="33657-200">Unclassified</span></span></td>
<td><span data-ttu-id="33657-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="33657-201">-10,000.00</span></span></td>
<td><span data-ttu-id="33657-202">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-203">CC099</span><span class="sxs-lookup"><span data-stu-id="33657-203">CC099</span></span></td>
<td><span data-ttu-id="33657-204">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="33657-204">Default cost center</span></span></td>
<td><span data-ttu-id="33657-205">10001</span><span class="sxs-lookup"><span data-stu-id="33657-205">10001</span></span></td>
<td><span data-ttu-id="33657-206">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-206">Electricity</span></span></td>
<td><span data-ttu-id="33657-207">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-207">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="33657-208">1,000.00</span></span></td>
<td><span data-ttu-id="33657-209">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-210">CC099</span><span class="sxs-lookup"><span data-stu-id="33657-210">CC099</span></span></td>
<td><span data-ttu-id="33657-211">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="33657-211">Default cost center</span></span></td>
<td><span data-ttu-id="33657-212">10001</span><span class="sxs-lookup"><span data-stu-id="33657-212">10001</span></span></td>
<td><span data-ttu-id="33657-213">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-213">Electricity</span></span></td>
<td><span data-ttu-id="33657-214">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-214">Variable cost</span></span></td>
<td><span data-ttu-id="33657-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="33657-215">9,000.00</span></span></td>
<td><span data-ttu-id="33657-216">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="33657-217">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðarhegðunarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="33657-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="33657-218">Skref 2: Keyra útreikning kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="33657-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="33657-219">Kostnaðardreifing er notuð til að endurúthluta kostnaði frá einum kostnaðarhlut til annars eða fleiri kostnaðarhluta með því að nota viðeigandi úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="33657-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="33657-220">Kostnaðardreifing og kostnaðarúthlutun eru ólíkar að því leyti að kostnaðardreifing kemur alltaf upp á stigi aðalkostnaðareiningar upphaflegs verðs.</span><span class="sxs-lookup"><span data-stu-id="33657-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="33657-221">Tilgreinið kostnaðardreifingarreglu</span><span class="sxs-lookup"><span data-stu-id="33657-221">Define the cost distribution rule</span></span>

<span data-ttu-id="33657-222">Í Fjárhagsbókhaldi er rafmagnskostnaður oft skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="33657-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="33657-223">Í kostnaðarbókhaldi er þessi nálgun ekki nógu nákvæm.</span><span class="sxs-lookup"><span data-stu-id="33657-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="33657-224">Breytilegur kostnaði þarf að dreifa á staka kostnaðarhluti á sanngjörnum grunni.</span><span class="sxs-lookup"><span data-stu-id="33657-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="33657-225">Rökréttasti úthlutunargrunnurinn er notkun á rafmagni (Kwh).</span><span class="sxs-lookup"><span data-stu-id="33657-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="33657-226">Stofnað er tölfræðilegt víddarstak sem er nefnt Rafmagn og rafmagnsnotkun er skráð.</span><span class="sxs-lookup"><span data-stu-id="33657-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="33657-227">Sjálfgefið er að öll tölfræðileg víddarstök verða tiltæk sem úthlutunargrunnur.</span><span class="sxs-lookup"><span data-stu-id="33657-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="33657-228">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-228">Cost object</span></span></th>
<th><span data-ttu-id="33657-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="33657-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-230">CC001</span><span class="sxs-lookup"><span data-stu-id="33657-230">CC001</span></span></td>
<td><span data-ttu-id="33657-231">Mannauður</span><span class="sxs-lookup"><span data-stu-id="33657-231">HR</span></span></td>
<td><span data-ttu-id="33657-232">1.000</span><span class="sxs-lookup"><span data-stu-id="33657-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-233">CC002</span><span class="sxs-lookup"><span data-stu-id="33657-233">CC002</span></span></td>
<td><span data-ttu-id="33657-234">Fjármál</span><span class="sxs-lookup"><span data-stu-id="33657-234">Finance</span></span></td>
<td><span data-ttu-id="33657-235">6,000</span><span class="sxs-lookup"><span data-stu-id="33657-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-236">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-236">CC003</span></span></td>
<td><span data-ttu-id="33657-237">Smölun</span><span class="sxs-lookup"><span data-stu-id="33657-237">Assembly</span></span></td>
<td><span data-ttu-id="33657-238">0</span><span class="sxs-lookup"><span data-stu-id="33657-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="33657-239">Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunni fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="33657-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="33657-240">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-240">Cost object</span></span></th>
<th><span data-ttu-id="33657-241">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="33657-241">Magnitude</span></span></th>
<th><span data-ttu-id="33657-242">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="33657-242">Allocation factor</span></span></th>
<th><span data-ttu-id="33657-243">Upphæð</span><span class="sxs-lookup"><span data-stu-id="33657-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-244">CC001</span><span class="sxs-lookup"><span data-stu-id="33657-244">CC001</span></span></td>
<td><span data-ttu-id="33657-245">Mannauður</span><span class="sxs-lookup"><span data-stu-id="33657-245">HR</span></span></td>
<td><span data-ttu-id="33657-246">1.000</span><span class="sxs-lookup"><span data-stu-id="33657-246">1,000</span></span></td>
<td><span data-ttu-id="33657-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="33657-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="33657-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="33657-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-249">CC002</span><span class="sxs-lookup"><span data-stu-id="33657-249">CC002</span></span></td>
<td><span data-ttu-id="33657-250">Fjármál</span><span class="sxs-lookup"><span data-stu-id="33657-250">Finance</span></span></td>
<td><span data-ttu-id="33657-251">6,000</span><span class="sxs-lookup"><span data-stu-id="33657-251">6,000</span></span></td>
<td><span data-ttu-id="33657-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="33657-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="33657-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="33657-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-254">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-254">CC003</span></span></td>
<td><span data-ttu-id="33657-255">Smölun</span><span class="sxs-lookup"><span data-stu-id="33657-255">Assembly</span></span></td>
<td><span data-ttu-id="33657-256">0</span><span class="sxs-lookup"><span data-stu-id="33657-256">0</span></span></td>
<td><span data-ttu-id="33657-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="33657-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="33657-258">0,00</span><span class="sxs-lookup"><span data-stu-id="33657-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="33657-259">Föstum kostnaði þarf að dreifa jafnt á staka kostnaðarhluti sem hafa notað rafmagn.</span><span class="sxs-lookup"><span data-stu-id="33657-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="33657-260">Hægt er að ná þessa niðurstöðu með því að nota tölfræðilegt víddarstakið Rafmagn í úthlutunargrunni reikniformúlu: (Rafmagn &gt; 0,00) Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunn fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="33657-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="33657-261">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-261">Cost object</span></span></th>
<th><span data-ttu-id="33657-262">Formúla</span><span class="sxs-lookup"><span data-stu-id="33657-262">Formula</span></span></th>
<th><span data-ttu-id="33657-263">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="33657-263">Magnitude</span></span></th>
<th><span data-ttu-id="33657-264">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="33657-264">Allocation factor</span></span></th>
<th><span data-ttu-id="33657-265">Upphæð</span><span class="sxs-lookup"><span data-stu-id="33657-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-266">CC001</span><span class="sxs-lookup"><span data-stu-id="33657-266">CC001</span></span></td>
<td><span data-ttu-id="33657-267">Mannauður</span><span class="sxs-lookup"><span data-stu-id="33657-267">HR</span></span></td>
<td><span data-ttu-id="33657-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="33657-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="33657-269">1</span><span class="sxs-lookup"><span data-stu-id="33657-269">1</span></span></td>
<td><span data-ttu-id="33657-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="33657-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="33657-271">500,00</span><span class="sxs-lookup"><span data-stu-id="33657-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-272">CC002</span><span class="sxs-lookup"><span data-stu-id="33657-272">CC002</span></span></td>
<td><span data-ttu-id="33657-273">Fjármál</span><span class="sxs-lookup"><span data-stu-id="33657-273">Finance</span></span></td>
<td><span data-ttu-id="33657-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="33657-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="33657-275">1</span><span class="sxs-lookup"><span data-stu-id="33657-275">1</span></span></td>
<td><span data-ttu-id="33657-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="33657-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="33657-277">500,00</span><span class="sxs-lookup"><span data-stu-id="33657-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-278">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-278">CC003</span></span></td>
<td><span data-ttu-id="33657-279">Smölun</span><span class="sxs-lookup"><span data-stu-id="33657-279">Assembly</span></span></td>
<td><span data-ttu-id="33657-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="33657-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="33657-281">0</span><span class="sxs-lookup"><span data-stu-id="33657-281">0</span></span></td>
<td><span data-ttu-id="33657-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="33657-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="33657-283">0,00</span><span class="sxs-lookup"><span data-stu-id="33657-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="33657-284">Færslubók</span><span class="sxs-lookup"><span data-stu-id="33657-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="33657-285">Færslubók</span><span class="sxs-lookup"><span data-stu-id="33657-285">Journal</span></span></th>
<th><span data-ttu-id="33657-286">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="33657-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="33657-287">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="33657-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="33657-288">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="33657-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-289">00002</span><span class="sxs-lookup"><span data-stu-id="33657-289">00002</span></span></td>
<td><span data-ttu-id="33657-290">Útreikningabók kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="33657-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="33657-291">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="33657-291">Fiscal</span></span></td>
<td><span data-ttu-id="33657-292">2017</span><span class="sxs-lookup"><span data-stu-id="33657-292">2017</span></span></td>
<td><span data-ttu-id="33657-293">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="33657-293">Period 1</span></span></td>
<td><span data-ttu-id="33657-294">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="33657-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="33657-295">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="33657-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="33657-296">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="33657-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="33657-297">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="33657-298">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="33657-298">Cost element</span></span></th>
<th><span data-ttu-id="33657-299">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="33657-299">Cost behavior</span></span></th>
<th><span data-ttu-id="33657-300">Upphæð</span><span class="sxs-lookup"><span data-stu-id="33657-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-301">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="33657-302">CC099</span><span class="sxs-lookup"><span data-stu-id="33657-302">CC099</span></span></td>
<td><span data-ttu-id="33657-303">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="33657-303">Default cost center</span></span></td>
<td><span data-ttu-id="33657-304">10001</span><span class="sxs-lookup"><span data-stu-id="33657-304">10001</span></span></td>
<td><span data-ttu-id="33657-305">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-305">Electricity</span></span></td>
<td><span data-ttu-id="33657-306">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-306">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="33657-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-308">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="33657-309">CC099</span><span class="sxs-lookup"><span data-stu-id="33657-309">CC099</span></span></td>
<td><span data-ttu-id="33657-310">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="33657-310">Default cost center</span></span></td>
<td><span data-ttu-id="33657-311">10001</span><span class="sxs-lookup"><span data-stu-id="33657-311">10001</span></span></td>
<td><span data-ttu-id="33657-312">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-312">Electricity</span></span></td>
<td><span data-ttu-id="33657-313">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-313">Variable cost</span></span></td>
<td><span data-ttu-id="33657-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="33657-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="33657-315">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="33657-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="33657-316">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="33657-317">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="33657-317">Cost element</span></span></th>
<th><span data-ttu-id="33657-318">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="33657-318">Cost behavior</span></span></th>
<th><span data-ttu-id="33657-319">Upphæð</span><span class="sxs-lookup"><span data-stu-id="33657-319">Amount</span></span></th>
<th><span data-ttu-id="33657-320">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="33657-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-321">CC099</span><span class="sxs-lookup"><span data-stu-id="33657-321">CC099</span></span></td>
<td><span data-ttu-id="33657-322">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="33657-322">Default cost center</span></span></td>
<td><span data-ttu-id="33657-323">10001</span><span class="sxs-lookup"><span data-stu-id="33657-323">10001</span></span></td>
<td><span data-ttu-id="33657-324">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-324">Electricity</span></span></td>
<td><span data-ttu-id="33657-325">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-325">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="33657-326">-1,000.00</span></span></td>
<td><span data-ttu-id="33657-327">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-328">CC001</span><span class="sxs-lookup"><span data-stu-id="33657-328">CC001</span></span></td>
<td><span data-ttu-id="33657-329">Mannauður</span><span class="sxs-lookup"><span data-stu-id="33657-329">HR</span></span></td>
<td><span data-ttu-id="33657-330">10001</span><span class="sxs-lookup"><span data-stu-id="33657-330">10001</span></span></td>
<td><span data-ttu-id="33657-331">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-331">Electricity</span></span></td>
<td><span data-ttu-id="33657-332">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-332">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-333">500,00</span><span class="sxs-lookup"><span data-stu-id="33657-333">500.00</span></span></td>
<td><span data-ttu-id="33657-334">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-335">CC002</span><span class="sxs-lookup"><span data-stu-id="33657-335">CC002</span></span></td>
<td><span data-ttu-id="33657-336">Fjármál</span><span class="sxs-lookup"><span data-stu-id="33657-336">Finance</span></span></td>
<td><span data-ttu-id="33657-337">10001</span><span class="sxs-lookup"><span data-stu-id="33657-337">10001</span></span></td>
<td><span data-ttu-id="33657-338">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-338">Electricity</span></span></td>
<td><span data-ttu-id="33657-339">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-339">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-340">500,00</span><span class="sxs-lookup"><span data-stu-id="33657-340">500.00</span></span></td>
<td><span data-ttu-id="33657-341">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-342">CC099</span><span class="sxs-lookup"><span data-stu-id="33657-342">CC099</span></span></td>
<td><span data-ttu-id="33657-343">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="33657-343">Default cost center</span></span></td>
<td><span data-ttu-id="33657-344">10001</span><span class="sxs-lookup"><span data-stu-id="33657-344">10001</span></span></td>
<td><span data-ttu-id="33657-345">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-345">Electricity</span></span></td>
<td><span data-ttu-id="33657-346">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-346">Variable cost</span></span></td>
<td><span data-ttu-id="33657-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="33657-347">-9,000.00</span></span></td>
<td><span data-ttu-id="33657-348">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-349">CC001</span><span class="sxs-lookup"><span data-stu-id="33657-349">CC001</span></span></td>
<td><span data-ttu-id="33657-350">Mannauður</span><span class="sxs-lookup"><span data-stu-id="33657-350">HR</span></span></td>
<td><span data-ttu-id="33657-351">10001</span><span class="sxs-lookup"><span data-stu-id="33657-351">10001</span></span></td>
<td><span data-ttu-id="33657-352">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-352">Electricity</span></span></td>
<td><span data-ttu-id="33657-353">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-353">Variable cost</span></span></td>
<td><span data-ttu-id="33657-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="33657-354">1,285.71</span></span></td>
<td><span data-ttu-id="33657-355">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-356">CC002</span><span class="sxs-lookup"><span data-stu-id="33657-356">CC002</span></span></td>
<td><span data-ttu-id="33657-357">Fjármál</span><span class="sxs-lookup"><span data-stu-id="33657-357">Finance</span></span></td>
<td><span data-ttu-id="33657-358">10001</span><span class="sxs-lookup"><span data-stu-id="33657-358">10001</span></span></td>
<td><span data-ttu-id="33657-359">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-359">Electricity</span></span></td>
<td><span data-ttu-id="33657-360">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-360">Variable cost</span></span></td>
<td><span data-ttu-id="33657-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="33657-361">7,714.29</span></span></td>
<td><span data-ttu-id="33657-362">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="33657-363">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðardreifingarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="33657-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="33657-364">Skref 3: Keyra útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="33657-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="33657-365">Sameiginlegur kostnaður er notaður til að rukka einn eða fleiri tilgreinda kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="33657-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="33657-366">Gjöldin byggjast á fyrirframákveðnu kostnaðarhlutfalli og mæligildi úr úthlutuðum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="33657-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="33657-367">Skilgreina sameiginlegan kostnað</span><span class="sxs-lookup"><span data-stu-id="33657-367">Define the overhead rate</span></span>

<span data-ttu-id="33657-368">Kostnaðarhlutur CC001 Mannauður stuðlar að safni innri verka.</span><span class="sxs-lookup"><span data-stu-id="33657-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="33657-369">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsverk til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="33657-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="33657-370">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-370">Cost object</span></span></th>
<th><span data-ttu-id="33657-371">Tímar</span><span class="sxs-lookup"><span data-stu-id="33657-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-372">Verk 1</span><span class="sxs-lookup"><span data-stu-id="33657-372">Proj 1</span></span></td>
<td><span data-ttu-id="33657-373">Verk 1</span><span class="sxs-lookup"><span data-stu-id="33657-373">Project 1</span></span></td>
<td><span data-ttu-id="33657-374">3</span><span class="sxs-lookup"><span data-stu-id="33657-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-375">Verk 2</span><span class="sxs-lookup"><span data-stu-id="33657-375">Proj 2</span></span></td>
<td><span data-ttu-id="33657-376">Verk 2</span><span class="sxs-lookup"><span data-stu-id="33657-376">Project 2</span></span></td>
<td><span data-ttu-id="33657-377">1</span><span class="sxs-lookup"><span data-stu-id="33657-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="33657-378">Fyrirframákveðið kostnaðarhlutfall fyrir kostnaðarframlag verk hefur verið skilgreint.</span><span class="sxs-lookup"><span data-stu-id="33657-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="33657-379">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-379">Cost object</span></span></th>
<th><span data-ttu-id="33657-380">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="33657-380">Cost element</span></span></th>
<th><span data-ttu-id="33657-381">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="33657-381">Cost behavior</span></span></th>
<th><span data-ttu-id="33657-382">Einingar</span><span class="sxs-lookup"><span data-stu-id="33657-382">Units</span></span></th>
<th><span data-ttu-id="33657-383">Taxti</span><span class="sxs-lookup"><span data-stu-id="33657-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-384">CC001</span><span class="sxs-lookup"><span data-stu-id="33657-384">CC001</span></span></td>
<td><span data-ttu-id="33657-385">Mannauður</span><span class="sxs-lookup"><span data-stu-id="33657-385">HR</span></span></td>
<td><span data-ttu-id="33657-386">10001</span><span class="sxs-lookup"><span data-stu-id="33657-386">10001</span></span></td>
<td><span data-ttu-id="33657-387">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-387">Variable cost</span></span></td>
<td><span data-ttu-id="33657-388">1</span><span class="sxs-lookup"><span data-stu-id="33657-388">1</span></span></td>
<td><span data-ttu-id="33657-389">10</span><span class="sxs-lookup"><span data-stu-id="33657-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="33657-390">Eftirfarandi tafla sýnir niðurstöður þegar Mannauðsverk eru notuð sem grunnur við úthlutun.</span><span class="sxs-lookup"><span data-stu-id="33657-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="33657-391">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-391">Cost object</span></span></th>
<th><span data-ttu-id="33657-392">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="33657-392">Magnitude</span></span></th>
<th><span data-ttu-id="33657-393">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="33657-393">Cost element</span></span></th>
<th><span data-ttu-id="33657-394">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="33657-394">Allocation factor</span></span></th>
<th><span data-ttu-id="33657-395">Upphæð</span><span class="sxs-lookup"><span data-stu-id="33657-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-396">Verk 1</span><span class="sxs-lookup"><span data-stu-id="33657-396">Proj 1</span></span></td>
<td><span data-ttu-id="33657-397">Verk 1</span><span class="sxs-lookup"><span data-stu-id="33657-397">Project 1</span></span></td>
<td><span data-ttu-id="33657-398">3</span><span class="sxs-lookup"><span data-stu-id="33657-398">3</span></span></td>
<td><span data-ttu-id="33657-399">10001</span><span class="sxs-lookup"><span data-stu-id="33657-399">10001</span></span></td>
<td><span data-ttu-id="33657-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="33657-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="33657-401">30,00</span><span class="sxs-lookup"><span data-stu-id="33657-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-402">Verk 2</span><span class="sxs-lookup"><span data-stu-id="33657-402">Proj 2</span></span></td>
<td><span data-ttu-id="33657-403">Verk 2</span><span class="sxs-lookup"><span data-stu-id="33657-403">Project 2</span></span></td>
<td><span data-ttu-id="33657-404">1</span><span class="sxs-lookup"><span data-stu-id="33657-404">1</span></span></td>
<td><span data-ttu-id="33657-405">10001</span><span class="sxs-lookup"><span data-stu-id="33657-405">10001</span></span></td>
<td><span data-ttu-id="33657-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="33657-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="33657-407">10,00</span><span class="sxs-lookup"><span data-stu-id="33657-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="33657-408">Færslubók</span><span class="sxs-lookup"><span data-stu-id="33657-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="33657-409">Færslubók</span><span class="sxs-lookup"><span data-stu-id="33657-409">Journal</span></span></th>
<th><span data-ttu-id="33657-410">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="33657-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="33657-411">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="33657-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="33657-412">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="33657-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-413">00003</span><span class="sxs-lookup"><span data-stu-id="33657-413">00003</span></span></td>
<td><span data-ttu-id="33657-414">Færslubók fyrir útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="33657-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="33657-415">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="33657-415">Fiscal</span></span></td>
<td><span data-ttu-id="33657-416">2017</span><span class="sxs-lookup"><span data-stu-id="33657-416">2017</span></span></td>
<td><span data-ttu-id="33657-417">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="33657-417">Period 1</span></span></td>
<td><span data-ttu-id="33657-418">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="33657-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="33657-419">Bókarfærslur (Bókarfærslur fyrir útreikning sameiginlegs kostnaðar)</span><span class="sxs-lookup"><span data-stu-id="33657-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="33657-420">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="33657-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="33657-421">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-421">Cost object</span></span></th>
<th><span data-ttu-id="33657-422">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="33657-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-423">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="33657-424">Verk 1</span><span class="sxs-lookup"><span data-stu-id="33657-424">Proj 1</span></span></td>
<td><span data-ttu-id="33657-425">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="33657-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="33657-426">3,00</span><span class="sxs-lookup"><span data-stu-id="33657-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-427">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="33657-428">Verk 2</span><span class="sxs-lookup"><span data-stu-id="33657-428">Proj 2</span></span></td>
<td><span data-ttu-id="33657-429">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="33657-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="33657-430">1,00</span><span class="sxs-lookup"><span data-stu-id="33657-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="33657-431">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="33657-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="33657-432">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="33657-433">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="33657-433">Cost element</span></span></th>
<th><span data-ttu-id="33657-434">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="33657-434">Cost behavior</span></span></th>
<th><span data-ttu-id="33657-435">Upphæð</span><span class="sxs-lookup"><span data-stu-id="33657-435">Amount</span></span></th>
<th><span data-ttu-id="33657-436">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="33657-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="33657-437">CC0001</span></span></td>
<td><span data-ttu-id="33657-438">Mannauður</span><span class="sxs-lookup"><span data-stu-id="33657-438">HR</span></span></td>
<td><span data-ttu-id="33657-439">10001</span><span class="sxs-lookup"><span data-stu-id="33657-439">10001</span></span></td>
<td><span data-ttu-id="33657-440">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-440">Electricity</span></span></td>
<td><span data-ttu-id="33657-441">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-441">Variable cost</span></span></td>
<td><span data-ttu-id="33657-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="33657-442">-30.00</span></span></td>
<td><span data-ttu-id="33657-443">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-444">Verk 1</span><span class="sxs-lookup"><span data-stu-id="33657-444">Proj 1</span></span></td>
<td><span data-ttu-id="33657-445">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="33657-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="33657-446">10001</span><span class="sxs-lookup"><span data-stu-id="33657-446">10001</span></span></td>
<td><span data-ttu-id="33657-447">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-447">Electricity</span></span></td>
<td><span data-ttu-id="33657-448">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-448">Variable cost</span></span></td>
<td><span data-ttu-id="33657-449">30,00</span><span class="sxs-lookup"><span data-stu-id="33657-449">30.00</span></span></td>
<td><span data-ttu-id="33657-450">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-451">CC001</span><span class="sxs-lookup"><span data-stu-id="33657-451">CC001</span></span></td>
<td><span data-ttu-id="33657-452">Mannauður</span><span class="sxs-lookup"><span data-stu-id="33657-452">HR</span></span></td>
<td><span data-ttu-id="33657-453">10001</span><span class="sxs-lookup"><span data-stu-id="33657-453">10001</span></span></td>
<td><span data-ttu-id="33657-454">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-454">Electricity</span></span></td>
<td><span data-ttu-id="33657-455">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-455">Variable cost</span></span></td>
<td><span data-ttu-id="33657-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="33657-456">-10.00</span></span></td>
<td><span data-ttu-id="33657-457">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-458">Verk 2</span><span class="sxs-lookup"><span data-stu-id="33657-458">Proj 2</span></span></td>
<td><span data-ttu-id="33657-459">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="33657-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="33657-460">10001</span><span class="sxs-lookup"><span data-stu-id="33657-460">10001</span></span></td>
<td><span data-ttu-id="33657-461">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-461">Electricity</span></span></td>
<td><span data-ttu-id="33657-462">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-462">Variable cost</span></span></td>
<td><span data-ttu-id="33657-463">10,00</span><span class="sxs-lookup"><span data-stu-id="33657-463">10.00</span></span></td>
<td><span data-ttu-id="33657-464">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="33657-465">Nánari upplýsingar er að finna í [Framkvæma útreikning fastakostnaðar](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="33657-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="33657-466">Skref 4: Keyra útreikning kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="33657-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="33657-467">Úthlutun er notuð til að úthluta stöðu kostnaðarhlutar í öðrum kostnaðarhlutum með því að nota úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="33657-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="33657-468">Finance styður gagnvirka úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="33657-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="33657-469">Í gagnvirkri úthlutunaraðferð er sú sameiginlega þjónusta sem hjálparkostnaðarhlutir skiptast á viðurkennd að fullu.</span><span class="sxs-lookup"><span data-stu-id="33657-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="33657-470">Kerfið ákvarðar sjálfkrafa rétta röð til að framkvæma úthlutun eftir.</span><span class="sxs-lookup"><span data-stu-id="33657-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="33657-471">Stöðu kostnaðarhluta er úthlutað með einum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="33657-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="33657-472">Úthlutanir þvert á víddir kostnaðarhluta og viðkomandi stök þeirra eru studdar.</span><span class="sxs-lookup"><span data-stu-id="33657-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="33657-473">Úthlutun pöntunarinnar er stjórnað af stýrieiningu kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="33657-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="33657-474">[![Gagnkvæm aðferð](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="33657-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="33657-475">Tilgreinið kostnaðarúthlutun</span><span class="sxs-lookup"><span data-stu-id="33657-475">Define the cost allocation</span></span>

<span data-ttu-id="33657-476">Hér er einfalt dæmi sem útskýrir hvernig hægt er að rekja flæði kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="33657-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="33657-477">Kostnaðarhlutir CC001 Mannauður leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="33657-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="33657-478">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="33657-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="33657-479">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-479">Cost object</span></span></th>
<th><span data-ttu-id="33657-480">Mannauðsþjónusta</span><span class="sxs-lookup"><span data-stu-id="33657-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-481">CC002</span><span class="sxs-lookup"><span data-stu-id="33657-481">CC002</span></span></td>
<td><span data-ttu-id="33657-482">Fjármál</span><span class="sxs-lookup"><span data-stu-id="33657-482">Finance</span></span></td>
<td><span data-ttu-id="33657-483">35</span><span class="sxs-lookup"><span data-stu-id="33657-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-484">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-484">CC003</span></span></td>
<td><span data-ttu-id="33657-485">Smölun</span><span class="sxs-lookup"><span data-stu-id="33657-485">Assembly</span></span></td>
<td><span data-ttu-id="33657-486">55</span><span class="sxs-lookup"><span data-stu-id="33657-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-487">CC004</span><span class="sxs-lookup"><span data-stu-id="33657-487">CC004</span></span></td>
<td><span data-ttu-id="33657-488">Pakkning</span><span class="sxs-lookup"><span data-stu-id="33657-488">Packaging</span></span></td>
<td><span data-ttu-id="33657-489">10</span><span class="sxs-lookup"><span data-stu-id="33657-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="33657-490">Kostnaðarhlutir CC002 Fjármál leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="33657-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="33657-491">Stofnað er tölfræðilegt víddarstak sem kallast Fjármálaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="33657-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="33657-492">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-492">Cost object</span></span></th>
<th><span data-ttu-id="33657-493">Fjármálaþjónusta</span><span class="sxs-lookup"><span data-stu-id="33657-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-494">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-494">CC003</span></span></td>
<td><span data-ttu-id="33657-495">Smölun</span><span class="sxs-lookup"><span data-stu-id="33657-495">Assembly</span></span></td>
<td><span data-ttu-id="33657-496">65</span><span class="sxs-lookup"><span data-stu-id="33657-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-497">CC004</span><span class="sxs-lookup"><span data-stu-id="33657-497">CC004</span></span></td>
<td><span data-ttu-id="33657-498">Pakkning</span><span class="sxs-lookup"><span data-stu-id="33657-498">Packaging</span></span></td>
<td><span data-ttu-id="33657-499">35</span><span class="sxs-lookup"><span data-stu-id="33657-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="33657-500">Kostnaðarhlutir CC003 Samsetning leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="33657-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="33657-501">Meðlimur tölfræðilega víddar sem kallast Mannauður verk er stofnað til að mælvíddarstaka notuðum magnitude.</span><span class="sxs-lookup"><span data-stu-id="33657-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="33657-502">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-502">Cost object</span></span></th>
<th><span data-ttu-id="33657-503">Samsetningarþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="33657-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-504">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-504">Prod 1</span></span></td>
<td><span data-ttu-id="33657-505">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-505">Product 1</span></span></td>
<td><span data-ttu-id="33657-506">60</span><span class="sxs-lookup"><span data-stu-id="33657-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-507">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-507">Prod 2</span></span></td>
<td><span data-ttu-id="33657-508">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-508">Product 2</span></span></td>
<td><span data-ttu-id="33657-509">20</span><span class="sxs-lookup"><span data-stu-id="33657-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="33657-510">Kostnaðarhlutir CC004 Umbúðir leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="33657-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="33657-511">Stofnað er tölfræðilegt víddarstak sem kallast Umbúðaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="33657-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="33657-512">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-512">Cost object</span></span></th>
<th><span data-ttu-id="33657-513">Umbúðaþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="33657-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-514">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-514">Prod 1</span></span></td>
<td><span data-ttu-id="33657-515">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-515">Product 1</span></span></td>
<td><span data-ttu-id="33657-516">80</span><span class="sxs-lookup"><span data-stu-id="33657-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-517">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-517">Prod 2</span></span></td>
<td><span data-ttu-id="33657-518">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-518">Product 2</span></span></td>
<td><span data-ttu-id="33657-519">15</span><span class="sxs-lookup"><span data-stu-id="33657-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="33657-520">Hægt er að afleiða tölfræðiaðgerðir eins og framleiðslutíma sem vara notar frá upprunagögnum.</span><span class="sxs-lookup"><span data-stu-id="33657-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="33657-521">Nánari upplýsingar er að finna í [Veitusniðmát tölfræðiaðgerðar](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="33657-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="33657-522">Eftirfarandi tafla sýnir niðurstöður þegar mannauðsþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="33657-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="33657-523">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-523">Cost object</span></span></th>
<th><span data-ttu-id="33657-524">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="33657-524">Magnitude</span></span></th>
<th><span data-ttu-id="33657-525">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="33657-525">Allocation factor</span></span></th>
<th><span data-ttu-id="33657-526">Upphæð</span><span class="sxs-lookup"><span data-stu-id="33657-526">Amount</span></span></th>
<th><span data-ttu-id="33657-527">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="33657-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-528">CC002</span><span class="sxs-lookup"><span data-stu-id="33657-528">CC002</span></span></td>
<td><span data-ttu-id="33657-529">Fjármál</span><span class="sxs-lookup"><span data-stu-id="33657-529">Finance</span></span></td>
<td><span data-ttu-id="33657-530">35</span><span class="sxs-lookup"><span data-stu-id="33657-530">35</span></span></td>
<td><span data-ttu-id="33657-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="33657-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="33657-532">175.00</span><span class="sxs-lookup"><span data-stu-id="33657-532">175.00</span></span></td>
<td><span data-ttu-id="33657-533">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-534">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-534">CC003</span></span></td>
<td><span data-ttu-id="33657-535">Smölun</span><span class="sxs-lookup"><span data-stu-id="33657-535">Assembly</span></span></td>
<td><span data-ttu-id="33657-536">55</span><span class="sxs-lookup"><span data-stu-id="33657-536">55</span></span></td>
<td><span data-ttu-id="33657-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="33657-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="33657-538">275.00</span><span class="sxs-lookup"><span data-stu-id="33657-538">275.00</span></span></td>
<td><span data-ttu-id="33657-539">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-540">CC004</span><span class="sxs-lookup"><span data-stu-id="33657-540">CC004</span></span></td>
<td><span data-ttu-id="33657-541">Pakkning</span><span class="sxs-lookup"><span data-stu-id="33657-541">Packaging</span></span></td>
<td><span data-ttu-id="33657-542">10</span><span class="sxs-lookup"><span data-stu-id="33657-542">10</span></span></td>
<td><span data-ttu-id="33657-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="33657-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="33657-544">50,00</span><span class="sxs-lookup"><span data-stu-id="33657-544">50.00</span></span></td>
<td><span data-ttu-id="33657-545">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-546">CC002</span><span class="sxs-lookup"><span data-stu-id="33657-546">CC002</span></span></td>
<td><span data-ttu-id="33657-547">Fjármál</span><span class="sxs-lookup"><span data-stu-id="33657-547">Finance</span></span></td>
<td><span data-ttu-id="33657-548">35</span><span class="sxs-lookup"><span data-stu-id="33657-548">35</span></span></td>
<td><span data-ttu-id="33657-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="33657-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="33657-550">436.00</span><span class="sxs-lookup"><span data-stu-id="33657-550">436.00</span></span></td>
<td><span data-ttu-id="33657-551">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-552">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-552">CC003</span></span></td>
<td><span data-ttu-id="33657-553">Smölun</span><span class="sxs-lookup"><span data-stu-id="33657-553">Assembly</span></span></td>
<td><span data-ttu-id="33657-554">55</span><span class="sxs-lookup"><span data-stu-id="33657-554">55</span></span></td>
<td><span data-ttu-id="33657-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="33657-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="33657-556">685.14</span><span class="sxs-lookup"><span data-stu-id="33657-556">685.14</span></span></td>
<td><span data-ttu-id="33657-557">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-558">CC004</span><span class="sxs-lookup"><span data-stu-id="33657-558">CC004</span></span></td>
<td><span data-ttu-id="33657-559">Pakkning</span><span class="sxs-lookup"><span data-stu-id="33657-559">Packaging</span></span></td>
<td><span data-ttu-id="33657-560">10</span><span class="sxs-lookup"><span data-stu-id="33657-560">10</span></span></td>
<td><span data-ttu-id="33657-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="33657-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="33657-562">124.57</span><span class="sxs-lookup"><span data-stu-id="33657-562">124.57</span></span></td>
<td><span data-ttu-id="33657-563">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="33657-564">Eftirfarandi tafla sýnir niðurstöður þegar Fjármálaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="33657-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="33657-565">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-565">Cost object</span></span></th>
<th><span data-ttu-id="33657-566">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="33657-566">Magnitude</span></span></th>
<th><span data-ttu-id="33657-567">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="33657-567">Allocation factor</span></span></th>
<th><span data-ttu-id="33657-568">Upphæð</span><span class="sxs-lookup"><span data-stu-id="33657-568">Amount</span></span></th>
<th><span data-ttu-id="33657-569">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="33657-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-570">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-570">CC003</span></span></td>
<td><span data-ttu-id="33657-571">Smölun</span><span class="sxs-lookup"><span data-stu-id="33657-571">Assembly</span></span></td>
<td><span data-ttu-id="33657-572">65</span><span class="sxs-lookup"><span data-stu-id="33657-572">65</span></span></td>
<td><span data-ttu-id="33657-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="33657-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="33657-574">438.75</span><span class="sxs-lookup"><span data-stu-id="33657-574">438.75</span></span></td>
<td><span data-ttu-id="33657-575">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-576">CC004</span><span class="sxs-lookup"><span data-stu-id="33657-576">CC004</span></span></td>
<td><span data-ttu-id="33657-577">Pakkning</span><span class="sxs-lookup"><span data-stu-id="33657-577">Packaging</span></span></td>
<td><span data-ttu-id="33657-578">35</span><span class="sxs-lookup"><span data-stu-id="33657-578">35</span></span></td>
<td><span data-ttu-id="33657-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="33657-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="33657-580">236.25</span><span class="sxs-lookup"><span data-stu-id="33657-580">236.25</span></span></td>
<td><span data-ttu-id="33657-581">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-582">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-582">CC003</span></span></td>
<td><span data-ttu-id="33657-583">Smölun</span><span class="sxs-lookup"><span data-stu-id="33657-583">Assembly</span></span></td>
<td><span data-ttu-id="33657-584">65</span><span class="sxs-lookup"><span data-stu-id="33657-584">65</span></span></td>
<td><span data-ttu-id="33657-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="33657-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="33657-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="33657-586">5,297.69</span></span></td>
<td><span data-ttu-id="33657-587">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-588">CC004</span><span class="sxs-lookup"><span data-stu-id="33657-588">CC004</span></span></td>
<td><span data-ttu-id="33657-589">Pakkning</span><span class="sxs-lookup"><span data-stu-id="33657-589">Packaging</span></span></td>
<td><span data-ttu-id="33657-590">35</span><span class="sxs-lookup"><span data-stu-id="33657-590">35</span></span></td>
<td><span data-ttu-id="33657-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="33657-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="33657-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="33657-592">2,852.60</span></span></td>
<td><span data-ttu-id="33657-593">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="33657-594">Eftirfarandi tafla sýnir niðurstöður þegar Samsetningarþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="33657-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="33657-595">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-595">Cost object</span></span></th>
<th><span data-ttu-id="33657-596">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="33657-596">Magnitude</span></span></th>
<th><span data-ttu-id="33657-597">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="33657-597">Allocation factor</span></span></th>
<th><span data-ttu-id="33657-598">Upphæð</span><span class="sxs-lookup"><span data-stu-id="33657-598">Amount</span></span></th>
<th><span data-ttu-id="33657-599">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="33657-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-600">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-600">Prod 1</span></span></td>
<td><span data-ttu-id="33657-601">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-601">Product 1</span></span></td>
<td><span data-ttu-id="33657-602">60</span><span class="sxs-lookup"><span data-stu-id="33657-602">60</span></span></td>
<td><span data-ttu-id="33657-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="33657-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="33657-604">535.31</span><span class="sxs-lookup"><span data-stu-id="33657-604">535.31</span></span></td>
<td><span data-ttu-id="33657-605">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-606">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-606">Prod 2</span></span></td>
<td><span data-ttu-id="33657-607">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-607">Product 2</span></span></td>
<td><span data-ttu-id="33657-608">20</span><span class="sxs-lookup"><span data-stu-id="33657-608">20</span></span></td>
<td><span data-ttu-id="33657-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="33657-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="33657-610">178.44</span><span class="sxs-lookup"><span data-stu-id="33657-610">178.44</span></span></td>
<td><span data-ttu-id="33657-611">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-612">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-612">Prod 1</span></span></td>
<td><span data-ttu-id="33657-613">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-613">Product 1</span></span></td>
<td><span data-ttu-id="33657-614">60</span><span class="sxs-lookup"><span data-stu-id="33657-614">60</span></span></td>
<td><span data-ttu-id="33657-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="33657-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="33657-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="33657-616">4,487.12</span></span></td>
<td><span data-ttu-id="33657-617">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-618">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-618">Prod 2</span></span></td>
<td><span data-ttu-id="33657-619">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-619">Product 2</span></span></td>
<td><span data-ttu-id="33657-620">20</span><span class="sxs-lookup"><span data-stu-id="33657-620">20</span></span></td>
<td><span data-ttu-id="33657-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="33657-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="33657-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="33657-622">1,495.71</span></span></td>
<td><span data-ttu-id="33657-623">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="33657-624">Eftirfarandi tafla sýnir niðurstöður þegar Umbúðaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="33657-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="33657-625">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-625">Cost object</span></span></th>
<th><span data-ttu-id="33657-626">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="33657-626">Magnitude</span></span></th>
<th><span data-ttu-id="33657-627">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="33657-627">Allocation factor</span></span></th>
<th><span data-ttu-id="33657-628">Upphæð</span><span class="sxs-lookup"><span data-stu-id="33657-628">Amount</span></span></th>
<th><span data-ttu-id="33657-629">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="33657-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-630">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-630">Prod 1</span></span></td>
<td><span data-ttu-id="33657-631">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-631">Product 1</span></span></td>
<td><span data-ttu-id="33657-632">80</span><span class="sxs-lookup"><span data-stu-id="33657-632">80</span></span></td>
<td><span data-ttu-id="33657-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="33657-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="33657-634">241.05</span><span class="sxs-lookup"><span data-stu-id="33657-634">241.05</span></span></td>
<td><span data-ttu-id="33657-635">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-636">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-636">Prod 2</span></span></td>
<td><span data-ttu-id="33657-637">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-637">Product 2</span></span></td>
<td><span data-ttu-id="33657-638">15</span><span class="sxs-lookup"><span data-stu-id="33657-638">15</span></span></td>
<td><span data-ttu-id="33657-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="33657-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="33657-640">45.20</span><span class="sxs-lookup"><span data-stu-id="33657-640">45.20</span></span></td>
<td><span data-ttu-id="33657-641">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-642">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-642">Prod 1</span></span></td>
<td><span data-ttu-id="33657-643">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-643">Product 1</span></span></td>
<td><span data-ttu-id="33657-644">80</span><span class="sxs-lookup"><span data-stu-id="33657-644">80</span></span></td>
<td><span data-ttu-id="33657-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="33657-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="33657-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="33657-646">2,507.09</span></span></td>
<td><span data-ttu-id="33657-647">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-648">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-648">Prod 2</span></span></td>
<td><span data-ttu-id="33657-649">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-649">Product 2</span></span></td>
<td><span data-ttu-id="33657-650">15</span><span class="sxs-lookup"><span data-stu-id="33657-650">15</span></span></td>
<td><span data-ttu-id="33657-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="33657-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="33657-652">470.08</span><span class="sxs-lookup"><span data-stu-id="33657-652">470.08</span></span></td>
<td><span data-ttu-id="33657-653">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="33657-654">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="33657-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="33657-655">Færslubók</span><span class="sxs-lookup"><span data-stu-id="33657-655">Journal</span></span></th>
<th><span data-ttu-id="33657-656">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="33657-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="33657-657">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="33657-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="33657-658">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="33657-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-659">00004</span><span class="sxs-lookup"><span data-stu-id="33657-659">00004</span></span></td>
<td><span data-ttu-id="33657-660">Færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="33657-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="33657-661">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="33657-661">Fiscal</span></span></td>
<td><span data-ttu-id="33657-662">2017</span><span class="sxs-lookup"><span data-stu-id="33657-662">2017</span></span></td>
<td><span data-ttu-id="33657-663">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="33657-663">Period 1</span></span></td>
<td><span data-ttu-id="33657-664">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="33657-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="33657-665">Færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="33657-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="33657-666">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="33657-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="33657-667">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="33657-668">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="33657-668">Cost element</span></span></th>
<th><span data-ttu-id="33657-669">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="33657-669">Cost behavior</span></span></th>
<th><span data-ttu-id="33657-670">Upphæð</span><span class="sxs-lookup"><span data-stu-id="33657-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-671">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="33657-672">CC001</span><span class="sxs-lookup"><span data-stu-id="33657-672">CC001</span></span></td>
<td><span data-ttu-id="33657-673">Mannauður</span><span class="sxs-lookup"><span data-stu-id="33657-673">HR</span></span></td>
<td><span data-ttu-id="33657-674">10001</span><span class="sxs-lookup"><span data-stu-id="33657-674">10001</span></span></td>
<td><span data-ttu-id="33657-675">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-675">Electricity</span></span></td>
<td><span data-ttu-id="33657-676">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-676">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-677">500,00</span><span class="sxs-lookup"><span data-stu-id="33657-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-678">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="33657-679">CC001</span><span class="sxs-lookup"><span data-stu-id="33657-679">CC001</span></span></td>
<td><span data-ttu-id="33657-680">Mannauður</span><span class="sxs-lookup"><span data-stu-id="33657-680">HR</span></span></td>
<td><span data-ttu-id="33657-681">10001</span><span class="sxs-lookup"><span data-stu-id="33657-681">10001</span></span></td>
<td><span data-ttu-id="33657-682">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-682">Electricity</span></span></td>
<td><span data-ttu-id="33657-683">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-683">Variable cost</span></span></td>
<td><span data-ttu-id="33657-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="33657-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-685">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="33657-686">CC002</span><span class="sxs-lookup"><span data-stu-id="33657-686">CC002</span></span></td>
<td><span data-ttu-id="33657-687">Fjármál</span><span class="sxs-lookup"><span data-stu-id="33657-687">Finance</span></span></td>
<td><span data-ttu-id="33657-688">10001</span><span class="sxs-lookup"><span data-stu-id="33657-688">10001</span></span></td>
<td><span data-ttu-id="33657-689">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-689">Electricity</span></span></td>
<td><span data-ttu-id="33657-690">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-690">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-691">675.00</span><span class="sxs-lookup"><span data-stu-id="33657-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-692">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="33657-693">CC002</span><span class="sxs-lookup"><span data-stu-id="33657-693">CC002</span></span></td>
<td><span data-ttu-id="33657-694">Fjármál</span><span class="sxs-lookup"><span data-stu-id="33657-694">Finance</span></span></td>
<td><span data-ttu-id="33657-695">10001</span><span class="sxs-lookup"><span data-stu-id="33657-695">10001</span></span></td>
<td><span data-ttu-id="33657-696">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-696">Electricity</span></span></td>
<td><span data-ttu-id="33657-697">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-697">Variable cost</span></span></td>
<td><span data-ttu-id="33657-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="33657-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-699">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="33657-700">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-700">CC003</span></span></td>
<td><span data-ttu-id="33657-701">Smölun</span><span class="sxs-lookup"><span data-stu-id="33657-701">Assembly</span></span></td>
<td><span data-ttu-id="33657-702">10001</span><span class="sxs-lookup"><span data-stu-id="33657-702">10001</span></span></td>
<td><span data-ttu-id="33657-703">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-703">Electricity</span></span></td>
<td><span data-ttu-id="33657-704">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-704">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-705">713.75</span><span class="sxs-lookup"><span data-stu-id="33657-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-706">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="33657-707">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-707">CC003</span></span></td>
<td><span data-ttu-id="33657-708">Smölun</span><span class="sxs-lookup"><span data-stu-id="33657-708">Assembly</span></span></td>
<td><span data-ttu-id="33657-709">10001</span><span class="sxs-lookup"><span data-stu-id="33657-709">10001</span></span></td>
<td><span data-ttu-id="33657-710">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-710">Electricity</span></span></td>
<td><span data-ttu-id="33657-711">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-711">Variable cost</span></span></td>
<td><span data-ttu-id="33657-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="33657-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-713">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="33657-714">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-714">CC003</span></span></td>
<td><span data-ttu-id="33657-715">Pakkning</span><span class="sxs-lookup"><span data-stu-id="33657-715">Packaging</span></span></td>
<td><span data-ttu-id="33657-716">10001</span><span class="sxs-lookup"><span data-stu-id="33657-716">10001</span></span></td>
<td><span data-ttu-id="33657-717">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-717">Electricity</span></span></td>
<td><span data-ttu-id="33657-718">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-718">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-719">286.25</span><span class="sxs-lookup"><span data-stu-id="33657-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-720">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="33657-721">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-721">CC003</span></span></td>
<td><span data-ttu-id="33657-722">Pakkning</span><span class="sxs-lookup"><span data-stu-id="33657-722">Packaging</span></span></td>
<td><span data-ttu-id="33657-723">10001</span><span class="sxs-lookup"><span data-stu-id="33657-723">10001</span></span></td>
<td><span data-ttu-id="33657-724">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-724">Electricity</span></span></td>
<td><span data-ttu-id="33657-725">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-725">Variable cost</span></span></td>
<td><span data-ttu-id="33657-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="33657-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-727">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="33657-728">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-728">Prod 1</span></span></td>
<td><span data-ttu-id="33657-729">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-729">Product 1</span></span></td>
<td><span data-ttu-id="33657-730">10001</span><span class="sxs-lookup"><span data-stu-id="33657-730">10001</span></span></td>
<td><span data-ttu-id="33657-731">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-731">Electricity</span></span></td>
<td><span data-ttu-id="33657-732">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-732">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-733">776.36</span><span class="sxs-lookup"><span data-stu-id="33657-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-734">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="33657-735">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-735">Prod 1</span></span></td>
<td><span data-ttu-id="33657-736">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-736">Product 1</span></span></td>
<td><span data-ttu-id="33657-737">10001</span><span class="sxs-lookup"><span data-stu-id="33657-737">10001</span></span></td>
<td><span data-ttu-id="33657-738">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-738">Electricity</span></span></td>
<td><span data-ttu-id="33657-739">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-739">Variable cost</span></span></td>
<td><span data-ttu-id="33657-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="33657-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-741">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="33657-742">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-742">Prod 2</span></span></td>
<td><span data-ttu-id="33657-743">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-743">Product 1</span></span></td>
<td><span data-ttu-id="33657-744">10001</span><span class="sxs-lookup"><span data-stu-id="33657-744">10001</span></span></td>
<td><span data-ttu-id="33657-745">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-745">Electricity</span></span></td>
<td><span data-ttu-id="33657-746">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-746">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-747">223.64</span><span class="sxs-lookup"><span data-stu-id="33657-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-748">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="33657-749">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-749">Prod 2</span></span></td>
<td><span data-ttu-id="33657-750">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-750">Product 1</span></span></td>
<td><span data-ttu-id="33657-751">10001</span><span class="sxs-lookup"><span data-stu-id="33657-751">10001</span></span></td>
<td><span data-ttu-id="33657-752">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-752">Electricity</span></span></td>
<td><span data-ttu-id="33657-753">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-753">Variable cost</span></span></td>
<td><span data-ttu-id="33657-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="33657-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="33657-755">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="33657-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="33657-756">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="33657-757">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="33657-757">Cost element</span></span></th>
<th><span data-ttu-id="33657-758">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="33657-758">Cost behavior</span></span></th>
<th><span data-ttu-id="33657-759">Upphæð</span><span class="sxs-lookup"><span data-stu-id="33657-759">Amount</span></span></th>
<th><span data-ttu-id="33657-760">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="33657-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="33657-761">CC001</span><span class="sxs-lookup"><span data-stu-id="33657-761">CC001</span></span></td>
<td><span data-ttu-id="33657-762">Mannauður</span><span class="sxs-lookup"><span data-stu-id="33657-762">HR</span></span></td>
<td><span data-ttu-id="33657-763">10001</span><span class="sxs-lookup"><span data-stu-id="33657-763">10001</span></span></td>
<td><span data-ttu-id="33657-764">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-764">Electricity</span></span></td>
<td><span data-ttu-id="33657-765">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-765">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="33657-766">-500.00</span></span></td>
<td><span data-ttu-id="33657-767">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-768">CC002</span><span class="sxs-lookup"><span data-stu-id="33657-768">CC002</span></span></td>
<td><span data-ttu-id="33657-769">Fjármál</span><span class="sxs-lookup"><span data-stu-id="33657-769">Finance</span></span></td>
<td><span data-ttu-id="33657-770">10001</span><span class="sxs-lookup"><span data-stu-id="33657-770">10001</span></span></td>
<td><span data-ttu-id="33657-771">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-771">Electricity</span></span></td>
<td><span data-ttu-id="33657-772">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-772">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-773">175.00</span><span class="sxs-lookup"><span data-stu-id="33657-773">175.00</span></span></td>
<td><span data-ttu-id="33657-774">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-775">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-775">CC003</span></span></td>
<td><span data-ttu-id="33657-776">Smölun</span><span class="sxs-lookup"><span data-stu-id="33657-776">Assembly</span></span></td>
<td><span data-ttu-id="33657-777">10001</span><span class="sxs-lookup"><span data-stu-id="33657-777">10001</span></span></td>
<td><span data-ttu-id="33657-778">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-778">Electricity</span></span></td>
<td><span data-ttu-id="33657-779">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-779">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-780">275.00</span><span class="sxs-lookup"><span data-stu-id="33657-780">275.00</span></span></td>
<td><span data-ttu-id="33657-781">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-782">CC004</span><span class="sxs-lookup"><span data-stu-id="33657-782">CC004</span></span></td>
<td><span data-ttu-id="33657-783">Pakkning</span><span class="sxs-lookup"><span data-stu-id="33657-783">Packaging</span></span></td>
<td><span data-ttu-id="33657-784">10001</span><span class="sxs-lookup"><span data-stu-id="33657-784">10001</span></span></td>
<td><span data-ttu-id="33657-785">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-785">Electricity</span></span></td>
<td><span data-ttu-id="33657-786">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-786">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-787">50,00</span><span class="sxs-lookup"><span data-stu-id="33657-787">50,00</span></span></td>
<td><span data-ttu-id="33657-788">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-789">CC001</span><span class="sxs-lookup"><span data-stu-id="33657-789">CC001</span></span></td>
<td><span data-ttu-id="33657-790">Mannauður</span><span class="sxs-lookup"><span data-stu-id="33657-790">HR</span></span></td>
<td><span data-ttu-id="33657-791">10001</span><span class="sxs-lookup"><span data-stu-id="33657-791">10001</span></span></td>
<td><span data-ttu-id="33657-792">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-792">Electricity</span></span></td>
<td><span data-ttu-id="33657-793">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-793">Variable cost</span></span></td>
<td><span data-ttu-id="33657-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="33657-794">-1,245.71</span></span></td>
<td><span data-ttu-id="33657-795">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-796">CC002</span><span class="sxs-lookup"><span data-stu-id="33657-796">CC002</span></span></td>
<td><span data-ttu-id="33657-797">Fjármál</span><span class="sxs-lookup"><span data-stu-id="33657-797">Finance</span></span></td>
<td><span data-ttu-id="33657-798">10001</span><span class="sxs-lookup"><span data-stu-id="33657-798">10001</span></span></td>
<td><span data-ttu-id="33657-799">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-799">Electricity</span></span></td>
<td><span data-ttu-id="33657-800">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-800">Variable cost</span></span></td>
<td><span data-ttu-id="33657-801">436.00</span><span class="sxs-lookup"><span data-stu-id="33657-801">436.00</span></span></td>
<td><span data-ttu-id="33657-802">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-803">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-803">CC003</span></span></td>
<td><span data-ttu-id="33657-804">Smölun</span><span class="sxs-lookup"><span data-stu-id="33657-804">Assembly</span></span></td>
<td><span data-ttu-id="33657-805">10001</span><span class="sxs-lookup"><span data-stu-id="33657-805">10001</span></span></td>
<td><span data-ttu-id="33657-806">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-806">Electricity</span></span></td>
<td><span data-ttu-id="33657-807">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-807">Variable cost</span></span></td>
<td><span data-ttu-id="33657-808">685.14</span><span class="sxs-lookup"><span data-stu-id="33657-808">685.14</span></span></td>
<td><span data-ttu-id="33657-809">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-810">CC004</span><span class="sxs-lookup"><span data-stu-id="33657-810">CC004</span></span></td>
<td><span data-ttu-id="33657-811">Pakkning</span><span class="sxs-lookup"><span data-stu-id="33657-811">Packaging</span></span></td>
<td><span data-ttu-id="33657-812">10001</span><span class="sxs-lookup"><span data-stu-id="33657-812">10001</span></span></td>
<td><span data-ttu-id="33657-813">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-813">Electricity</span></span></td>
<td><span data-ttu-id="33657-814">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-814">Variable cost</span></span></td>
<td><span data-ttu-id="33657-815">124.57</span><span class="sxs-lookup"><span data-stu-id="33657-815">124.57</span></span></td>
<td><span data-ttu-id="33657-816">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-817">CC002</span><span class="sxs-lookup"><span data-stu-id="33657-817">CC002</span></span></td>
<td><span data-ttu-id="33657-818">Fjármál</span><span class="sxs-lookup"><span data-stu-id="33657-818">Finance</span></span></td>
<td><span data-ttu-id="33657-819">10001</span><span class="sxs-lookup"><span data-stu-id="33657-819">10001</span></span></td>
<td><span data-ttu-id="33657-820">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-820">Electricity</span></span></td>
<td><span data-ttu-id="33657-821">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-821">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="33657-822">-675.00</span></span></td>
<td><span data-ttu-id="33657-823">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-824">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-824">CC003</span></span></td>
<td><span data-ttu-id="33657-825">Smölun</span><span class="sxs-lookup"><span data-stu-id="33657-825">Assembly</span></span></td>
<td><span data-ttu-id="33657-826">10001</span><span class="sxs-lookup"><span data-stu-id="33657-826">10001</span></span></td>
<td><span data-ttu-id="33657-827">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-827">Electricity</span></span></td>
<td><span data-ttu-id="33657-828">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-828">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-829">438.75</span><span class="sxs-lookup"><span data-stu-id="33657-829">438.75</span></span></td>
<td><span data-ttu-id="33657-830">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-831">CC004</span><span class="sxs-lookup"><span data-stu-id="33657-831">CC004</span></span></td>
<td><span data-ttu-id="33657-832">Pakkning</span><span class="sxs-lookup"><span data-stu-id="33657-832">Packaging</span></span></td>
<td><span data-ttu-id="33657-833">10001</span><span class="sxs-lookup"><span data-stu-id="33657-833">10001</span></span></td>
<td><span data-ttu-id="33657-834">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-834">Electricity</span></span></td>
<td><span data-ttu-id="33657-835">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-835">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-836">236.25</span><span class="sxs-lookup"><span data-stu-id="33657-836">236.25</span></span></td>
<td><span data-ttu-id="33657-837">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-838">CC002</span><span class="sxs-lookup"><span data-stu-id="33657-838">CC002</span></span></td>
<td><span data-ttu-id="33657-839">Fjármál</span><span class="sxs-lookup"><span data-stu-id="33657-839">Finance</span></span></td>
<td><span data-ttu-id="33657-840">10001</span><span class="sxs-lookup"><span data-stu-id="33657-840">10001</span></span></td>
<td><span data-ttu-id="33657-841">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-841">Electricity</span></span></td>
<td><span data-ttu-id="33657-842">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-842">Variable cost</span></span></td>
<td><span data-ttu-id="33657-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="33657-843">-8,150.29</span></span></td>
<td><span data-ttu-id="33657-844">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-845">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-845">CC003</span></span></td>
<td><span data-ttu-id="33657-846">Smölun</span><span class="sxs-lookup"><span data-stu-id="33657-846">Assembly</span></span></td>
<td><span data-ttu-id="33657-847">10001</span><span class="sxs-lookup"><span data-stu-id="33657-847">10001</span></span></td>
<td><span data-ttu-id="33657-848">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-848">Electricity</span></span></td>
<td><span data-ttu-id="33657-849">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-849">Variable cost</span></span></td>
<td><span data-ttu-id="33657-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="33657-850">5,297.69</span></span></td>
<td><span data-ttu-id="33657-851">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-852">CC004</span><span class="sxs-lookup"><span data-stu-id="33657-852">CC004</span></span></td>
<td><span data-ttu-id="33657-853">Pakkning</span><span class="sxs-lookup"><span data-stu-id="33657-853">Packaging</span></span></td>
<td><span data-ttu-id="33657-854">10001</span><span class="sxs-lookup"><span data-stu-id="33657-854">10001</span></span></td>
<td><span data-ttu-id="33657-855">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-855">Electricity</span></span></td>
<td><span data-ttu-id="33657-856">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-856">Variable cost</span></span></td>
<td><span data-ttu-id="33657-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="33657-857">2,852.60</span></span></td>
<td><span data-ttu-id="33657-858">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-859">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-859">CC003</span></span></td>
<td><span data-ttu-id="33657-860">Smölun</span><span class="sxs-lookup"><span data-stu-id="33657-860">Assembly</span></span></td>
<td><span data-ttu-id="33657-861">10001</span><span class="sxs-lookup"><span data-stu-id="33657-861">10001</span></span></td>
<td><span data-ttu-id="33657-862">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-862">Electricity</span></span></td>
<td><span data-ttu-id="33657-863">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-863">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="33657-864">-713.75</span></span></td>
<td><span data-ttu-id="33657-865">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-866">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-866">Prod 1</span></span></td>
<td><span data-ttu-id="33657-867">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-867">Product 1</span></span></td>
<td><span data-ttu-id="33657-868">10001</span><span class="sxs-lookup"><span data-stu-id="33657-868">10001</span></span></td>
<td><span data-ttu-id="33657-869">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-869">Electricity</span></span></td>
<td><span data-ttu-id="33657-870">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-870">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-871">535.31</span><span class="sxs-lookup"><span data-stu-id="33657-871">535.31</span></span></td>
<td><span data-ttu-id="33657-872">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-873">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-873">Prod 2</span></span></td>
<td><span data-ttu-id="33657-874">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-874">Product 2</span></span></td>
<td><span data-ttu-id="33657-875">10001</span><span class="sxs-lookup"><span data-stu-id="33657-875">10001</span></span></td>
<td><span data-ttu-id="33657-876">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-876">Electricity</span></span></td>
<td><span data-ttu-id="33657-877">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-877">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-878">178.44</span><span class="sxs-lookup"><span data-stu-id="33657-878">178.44</span></span></td>
<td><span data-ttu-id="33657-879">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-880">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-880">CC003</span></span></td>
<td><span data-ttu-id="33657-881">Smölun</span><span class="sxs-lookup"><span data-stu-id="33657-881">Assembly</span></span></td>
<td><span data-ttu-id="33657-882">10001</span><span class="sxs-lookup"><span data-stu-id="33657-882">10001</span></span></td>
<td><span data-ttu-id="33657-883">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-883">Electricity</span></span></td>
<td><span data-ttu-id="33657-884">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-884">Variable cost</span></span></td>
<td><span data-ttu-id="33657-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="33657-885">-5,982.83</span></span></td>
<td><span data-ttu-id="33657-886">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-887">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-887">Prod 1</span></span></td>
<td><span data-ttu-id="33657-888">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-888">Product 1</span></span></td>
<td><span data-ttu-id="33657-889">10001</span><span class="sxs-lookup"><span data-stu-id="33657-889">10001</span></span></td>
<td><span data-ttu-id="33657-890">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-890">Electricity</span></span></td>
<td><span data-ttu-id="33657-891">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-891">Variable cost</span></span></td>
<td><span data-ttu-id="33657-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="33657-892">4,487.12</span></span></td>
<td><span data-ttu-id="33657-893">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-894">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-894">Prod 2</span></span></td>
<td><span data-ttu-id="33657-895">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-895">Product 2</span></span></td>
<td><span data-ttu-id="33657-896">10001</span><span class="sxs-lookup"><span data-stu-id="33657-896">10001</span></span></td>
<td><span data-ttu-id="33657-897">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-897">Electricity</span></span></td>
<td><span data-ttu-id="33657-898">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-898">Variable cost</span></span></td>
<td><span data-ttu-id="33657-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="33657-899">1,495.71</span></span></td>
<td><span data-ttu-id="33657-900">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-901">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-901">CC003</span></span></td>
<td><span data-ttu-id="33657-902">Smölun</span><span class="sxs-lookup"><span data-stu-id="33657-902">Assembly</span></span></td>
<td><span data-ttu-id="33657-903">10001</span><span class="sxs-lookup"><span data-stu-id="33657-903">10001</span></span></td>
<td><span data-ttu-id="33657-904">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-904">Electricity</span></span></td>
<td><span data-ttu-id="33657-905">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-905">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="33657-906">-286.25</span></span></td>
<td><span data-ttu-id="33657-907">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-908">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-908">Prod 1</span></span></td>
<td><span data-ttu-id="33657-909">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-909">Product 1</span></span></td>
<td><span data-ttu-id="33657-910">10001</span><span class="sxs-lookup"><span data-stu-id="33657-910">10001</span></span></td>
<td><span data-ttu-id="33657-911">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-911">Electricity</span></span></td>
<td><span data-ttu-id="33657-912">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-912">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-913">241.05</span><span class="sxs-lookup"><span data-stu-id="33657-913">241.05</span></span></td>
<td><span data-ttu-id="33657-914">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-915">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-915">Prod 2</span></span></td>
<td><span data-ttu-id="33657-916">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-916">Product 2</span></span></td>
<td><span data-ttu-id="33657-917">10001</span><span class="sxs-lookup"><span data-stu-id="33657-917">10001</span></span></td>
<td><span data-ttu-id="33657-918">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-918">Electricity</span></span></td>
<td><span data-ttu-id="33657-919">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-919">Fixed cost</span></span></td>
<td><span data-ttu-id="33657-920">45.20</span><span class="sxs-lookup"><span data-stu-id="33657-920">45.20</span></span></td>
<td><span data-ttu-id="33657-921">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-922">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-922">CC003</span></span></td>
<td><span data-ttu-id="33657-923">Smölun</span><span class="sxs-lookup"><span data-stu-id="33657-923">Assembly</span></span></td>
<td><span data-ttu-id="33657-924">10001</span><span class="sxs-lookup"><span data-stu-id="33657-924">10001</span></span></td>
<td><span data-ttu-id="33657-925">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-925">Electricity</span></span></td>
<td><span data-ttu-id="33657-926">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-926">Variable cost</span></span></td>
<td><span data-ttu-id="33657-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="33657-927">-2,977.17</span></span></td>
<td><span data-ttu-id="33657-928">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-929">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-929">Prod 1</span></span></td>
<td><span data-ttu-id="33657-930">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-930">Product 1</span></span></td>
<td><span data-ttu-id="33657-931">10001</span><span class="sxs-lookup"><span data-stu-id="33657-931">10001</span></span></td>
<td><span data-ttu-id="33657-932">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-932">Electricity</span></span></td>
<td><span data-ttu-id="33657-933">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-933">Variable cost</span></span></td>
<td><span data-ttu-id="33657-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="33657-934">2,507.09</span></span></td>
<td><span data-ttu-id="33657-935">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="33657-936">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-936">Prod 2</span></span></td>
<td><span data-ttu-id="33657-937">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-937">Product 2</span></span></td>
<td><span data-ttu-id="33657-938">10001</span><span class="sxs-lookup"><span data-stu-id="33657-938">10001</span></span></td>
<td><span data-ttu-id="33657-939">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-939">Electricity</span></span></td>
<td><span data-ttu-id="33657-940">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-940">Variable cost</span></span></td>
<td><span data-ttu-id="33657-941">470.08</span><span class="sxs-lookup"><span data-stu-id="33657-941">470.08</span></span></td>
<td><span data-ttu-id="33657-942">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="33657-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="33657-943">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="33657-943">Conclusion</span></span>
<span data-ttu-id="33657-944">Í Fjárhagsbókhaldi er kostnaður upp á 10.000,00 fyrir rafmagn bókaður á kenni leppkostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="33657-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="33657-945">Þar af leiðandi munu kostnaðarbókarar vita að það þarf að úthluta þessum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="33657-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="33657-946">Í kostnaðarbókhaldi streymir kostnaður þvert á fyrirtækiseiningar og stig, samkvæmt þeim stefnum og reglum sem eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="33657-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="33657-947">Hver kostnaður hefur verið tengdur úthlutunargrunni sem veitir besta mat á úthlutun á kostnaði.</span><span class="sxs-lookup"><span data-stu-id="33657-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="33657-948">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="33657-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="33657-949">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="33657-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="33657-950">Samtala</span><span class="sxs-lookup"><span data-stu-id="33657-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="33657-951">CC099</span><span class="sxs-lookup"><span data-stu-id="33657-951">CC099</span></span></th>
<th><span data-ttu-id="33657-952">CC001</span><span class="sxs-lookup"><span data-stu-id="33657-952">CC001</span></span></th>
<th><span data-ttu-id="33657-953">CC002</span><span class="sxs-lookup"><span data-stu-id="33657-953">CC002</span></span></th>
<th><span data-ttu-id="33657-954">CC003</span><span class="sxs-lookup"><span data-stu-id="33657-954">CC003</span></span></th>
<th><span data-ttu-id="33657-955">CC004</span><span class="sxs-lookup"><span data-stu-id="33657-955">CC004</span></span></th>
<th><span data-ttu-id="33657-956">Verk 1</span><span class="sxs-lookup"><span data-stu-id="33657-956">Proj 1</span></span></th>
<th><span data-ttu-id="33657-957">Verk 2</span><span class="sxs-lookup"><span data-stu-id="33657-957">Proj 2</span></span></th>
<th><span data-ttu-id="33657-958">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="33657-958">Prod 1</span></span></th>
<th><span data-ttu-id="33657-959">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="33657-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="33657-960">10001 Rafmagn</span><span class="sxs-lookup"><span data-stu-id="33657-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="33657-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="33657-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="33657-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="33657-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="33657-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="33657-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="33657-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="33657-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="33657-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="33657-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="33657-970">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="33657-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-971">0,00</span><span class="sxs-lookup"><span data-stu-id="33657-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="33657-972">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-973">0,00</span><span class="sxs-lookup"><span data-stu-id="33657-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-974">0,00</span><span class="sxs-lookup"><span data-stu-id="33657-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-975">0,00</span><span class="sxs-lookup"><span data-stu-id="33657-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-976">0,00</span><span class="sxs-lookup"><span data-stu-id="33657-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-977">0,00</span><span class="sxs-lookup"><span data-stu-id="33657-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="33657-978">776.36</span><span class="sxs-lookup"><span data-stu-id="33657-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-979">223.64</span><span class="sxs-lookup"><span data-stu-id="33657-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="33657-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="33657-981">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="33657-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-982">000</span><span class="sxs-lookup"><span data-stu-id="33657-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-983">0,00</span><span class="sxs-lookup"><span data-stu-id="33657-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-984">0,00</span><span class="sxs-lookup"><span data-stu-id="33657-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-985">0,00</span><span class="sxs-lookup"><span data-stu-id="33657-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-986">0,00</span><span class="sxs-lookup"><span data-stu-id="33657-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-987">30,00</span><span class="sxs-lookup"><span data-stu-id="33657-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-988">10,00</span><span class="sxs-lookup"><span data-stu-id="33657-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="33657-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="33657-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="33657-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="33657-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="33657-992">Þetta efnisatriði sýnir hvernig fyrir aðalkostnaðareiningin 10001 Rafmagn flæðir í gegnum kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="33657-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="33657-993">Þar af leiðandi er þessum sameiginlega kostnaði úthlutað á lægsta stigið í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="33657-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="33657-994">Með öðrum orðum bera kostnaðarhlutir á lægsta stiginu kostnaðinn.</span><span class="sxs-lookup"><span data-stu-id="33657-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="33657-995">Ef þú þarft sjónrænt flæði kostnaðar á milli kostnaðarhluta er hægt að nota stefnureglur samantekins kostnaðar til að gera kostnaðarflæðið sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="33657-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="33657-996">Fyrir frekari upplýsingar skal sjá [Stefna fyrir samantekt kostnaðar og útreikning sameiginlegs kostnaðar](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="33657-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



