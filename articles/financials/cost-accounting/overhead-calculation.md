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
ms.openlocfilehash: cef4a80aa12927fdbffea4bb6bcb108ad81494a6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841490"
---
# <a name="overhead-calculation"></a><span data-ttu-id="58676-103">Útreikningur fastakostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="58676-104">Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði.</span><span class="sxs-lookup"><span data-stu-id="58676-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="58676-105">Skýrsluskilgreining</span><span class="sxs-lookup"><span data-stu-id="58676-105">Term definition</span></span>
---------------

<span data-ttu-id="58676-106">Stjórnunarkostnaður er sá kostnaður sem stofnað er til fyrir rekstur fyrirtækis, en sem ekki er hægt að rekja beint til neinna sérstakrar starfsemi, vöru eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="58676-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="58676-107">Stjórnunarkostnaður veitir mikilvægan stuðning við myndun hagnaðarmyndandi verkþátta.</span><span class="sxs-lookup"><span data-stu-id="58676-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="58676-108">Hér eru nokkur dæmi um skilyrði:</span><span class="sxs-lookup"><span data-stu-id="58676-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="58676-109">Leiga</span><span class="sxs-lookup"><span data-stu-id="58676-109">Rent</span></span>
-   <span data-ttu-id="58676-110">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-110">Electricity</span></span>
-   <span data-ttu-id="58676-111">Stjórnunarkostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="58676-112">Yfirlit yfir útreikning fastakostnaðar</span><span class="sxs-lookup"><span data-stu-id="58676-112">Overhead calculation overview</span></span>
<span data-ttu-id="58676-113">Útreikningur fastakostnaðar keyrir reglur kostnaðarbókhalds í réttri röð.</span><span class="sxs-lookup"><span data-stu-id="58676-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="58676-114">Hægt er að keyra útreikning fastakostnaðar margsinnis fyrir sama fjárhagstímabil ef reglum kostnaðarbókhalds hefur verið breytt eða ákveðnar villur hafa fundist.</span><span class="sxs-lookup"><span data-stu-id="58676-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="58676-115">Hver keyrsla á útreikningi fastakostnaðar er geymd og fær einkvæmt útgáfukenni sem gerir kleift að bera saman útreikning í mismunandi útgáfum.</span><span class="sxs-lookup"><span data-stu-id="58676-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="58676-116">Kostnaðarfærslur sem útreikningur fastakostnaðar mynda fá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="58676-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="58676-117">Dagsetningin bókhald samsvarar lokadagsetning fjárhagstímabilsins sem er dagsetning reikningsskiladagsetning reikningsskila notað í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="58676-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="58676-118">Einkvæmt útgáfukenni samanstendur af eftirfarandi þáttum:</span><span class="sxs-lookup"><span data-stu-id="58676-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="58676-119">Gerð útgáfu</span><span class="sxs-lookup"><span data-stu-id="58676-119">Version type</span></span>
-   <span data-ttu-id="58676-120">Dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="58676-120">Date and time</span></span>
-   <span data-ttu-id="58676-121">Fjárhagur kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="58676-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="58676-122">Fjárhagsár</span><span class="sxs-lookup"><span data-stu-id="58676-122">Fiscal year</span></span>
-   <span data-ttu-id="58676-123">Reikningstímabil</span><span class="sxs-lookup"><span data-stu-id="58676-123">Fiscal period</span></span>

<span data-ttu-id="58676-124">Útreikningur fastakostnaðar er keyrður óháð því hver útgáfan er.</span><span class="sxs-lookup"><span data-stu-id="58676-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="58676-125">Þess vegna er hægt að reikna út áætlaða útgáfu á undan raunútgáfu.</span><span class="sxs-lookup"><span data-stu-id="58676-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="58676-126">Útreikningur fastakostnaðar samanstendur af fjórum skrefum, eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="58676-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="58676-127">Í hverju skrefi er færslubókarhaus stofnaður með bókarfærslum.</span><span class="sxs-lookup"><span data-stu-id="58676-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="58676-128">Þessi færslubókarhaus geymir inntaksgögn fyrir hvert útreikningsþrep.</span><span class="sxs-lookup"><span data-stu-id="58676-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="58676-129">Stefnur og reglur eru notaðar í hverri færslulínu og kostnaðarfærslur eru myndaðar sem úttak.</span><span class="sxs-lookup"><span data-stu-id="58676-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="58676-130">Þess vegna hefurðu ávallt fullan rekjanleika.</span><span class="sxs-lookup"><span data-stu-id="58676-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="58676-131">[![Útreikningur fastakostnaðar](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="58676-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="58676-132">Reikna og úthluta sameiginlegur kostnaði vegna rafmagns</span><span class="sxs-lookup"><span data-stu-id="58676-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="58676-133">Í Fjárhagsbókhaldi er ákveðinn kostnaður, eins og rafmagn, skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="58676-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="58676-134">Þar af leiðandi er nákvæmar innsýn rekstrarfélags ekki veitt fyrir kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="58676-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="58676-135">Í kostnaðarbókhaldi verður kostnaður að flæða í gegnum fyrirtækiseiningar til að veita rétta innsýn rekstrarfélags þvert á allar fyrirtækiseiningar og stig.</span><span class="sxs-lookup"><span data-stu-id="58676-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="58676-136">Þetta flæði verður að byggja á annaðhvort nákvæmri færslu notkunar eða sanngjarnri matsreglu.</span><span class="sxs-lookup"><span data-stu-id="58676-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="58676-137">Í fjárhagnum er hægt að bóka rafmagnskostnað eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="58676-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="58676-138">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="58676-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="58676-139">Kostnaðarstaður</span><span class="sxs-lookup"><span data-stu-id="58676-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="58676-140">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="58676-140">Main account</span></span></th>
<th><span data-ttu-id="58676-141">Upphæð í bókhaldsgjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="58676-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-142">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="58676-143">CC099</span><span class="sxs-lookup"><span data-stu-id="58676-143">CC099</span></span></td>
<td><span data-ttu-id="58676-144">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58676-144">Default cost center</span></span></td>
<td><span data-ttu-id="58676-145">10001</span><span class="sxs-lookup"><span data-stu-id="58676-145">10001</span></span></td>
<td><span data-ttu-id="58676-146">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-146">Electricity</span></span></td>
<td><span data-ttu-id="58676-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="58676-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="58676-148">Skref 1: Keyra útreikning kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="58676-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="58676-149">Sjálfvirkt er að þegar kostnaðarfærslur eru fluttar úr grunngögnum fái þær flokkun kostnaðarhegðunar **Óflokkað** í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="58676-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="58676-150">Með því að nota stefnureglur kostnaðarhegðunar er hægt að endurflokka kostnaðarfærslur sem annaðhvort **Fastan kostnað** eða **Breytilegan kostnað**.</span><span class="sxs-lookup"><span data-stu-id="58676-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="58676-151">Tilgreinið reglu kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="58676-151">Define the cost behavior rule</span></span>

<span data-ttu-id="58676-152">Í sumum tilfellum er hluti af kostnaði föst þóknun og eftirstandandi kostnaður byggist á notkun.</span><span class="sxs-lookup"><span data-stu-id="58676-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="58676-153">Rafmagnsreikningar stemma oft við þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="58676-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="58676-154">Þegar tiltekin föst þóknun hefur verið greidd, er greitt fyrir notkun á kílóvattklukkustund (Kwh).</span><span class="sxs-lookup"><span data-stu-id="58676-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="58676-155">Til dæmis ef föst kostnaðarþóknun er 1000.00 sýnir þetta hvernig regla kostnaðarhegðunar er skilgreind:</span><span class="sxs-lookup"><span data-stu-id="58676-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="58676-156">Föst upphæð 1.000,00</span><span class="sxs-lookup"><span data-stu-id="58676-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="58676-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="58676-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="58676-158">1000.01 &lt; N = Breyta</span><span class="sxs-lookup"><span data-stu-id="58676-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="58676-159">Færslubók</span><span class="sxs-lookup"><span data-stu-id="58676-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="58676-160">Færslubók</span><span class="sxs-lookup"><span data-stu-id="58676-160">Journal</span></span></th>
<th><span data-ttu-id="58676-161">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="58676-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="58676-162">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="58676-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="58676-163">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="58676-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-164">00001</span><span class="sxs-lookup"><span data-stu-id="58676-164">00001</span></span></td>
<td><span data-ttu-id="58676-165">Færslubók útreiknings fyrir kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58676-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="58676-166">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="58676-166">Fiscal</span></span></td>
<td><span data-ttu-id="58676-167">2017</span><span class="sxs-lookup"><span data-stu-id="58676-167">2017</span></span></td>
<td><span data-ttu-id="58676-168">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="58676-168">Period 1</span></span></td>
<td><span data-ttu-id="58676-169">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="58676-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="58676-170">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="58676-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="58676-171">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="58676-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="58676-172">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="58676-173">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58676-173">Cost element</span></span></th>
<th><span data-ttu-id="58676-174">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58676-174">Cost behavior</span></span></th>
<th><span data-ttu-id="58676-175">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58676-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-176">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="58676-177">CC099</span><span class="sxs-lookup"><span data-stu-id="58676-177">CC099</span></span></td>
<td><span data-ttu-id="58676-178">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58676-178">Default cost center</span></span></td>
<td><span data-ttu-id="58676-179">10001</span><span class="sxs-lookup"><span data-stu-id="58676-179">10001</span></span></td>
<td><span data-ttu-id="58676-180">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-180">Electricity</span></span></td>
<td><span data-ttu-id="58676-181">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="58676-181">Unclassified</span></span></td>
<td><span data-ttu-id="58676-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="58676-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="58676-183">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="58676-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58676-184">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="58676-185">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58676-185">Cost element</span></span></th>
<th><span data-ttu-id="58676-186">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58676-186">Cost behavior</span></span></th>
<th><span data-ttu-id="58676-187">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58676-187">Amount</span></span></th>
<th><span data-ttu-id="58676-188">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="58676-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-189">CC099</span><span class="sxs-lookup"><span data-stu-id="58676-189">CC099</span></span></td>
<td><span data-ttu-id="58676-190">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58676-190">Default cost center</span></span></td>
<td><span data-ttu-id="58676-191">10001</span><span class="sxs-lookup"><span data-stu-id="58676-191">10001</span></span></td>
<td><span data-ttu-id="58676-192">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-192">Electricity</span></span></td>
<td><span data-ttu-id="58676-193">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="58676-193">Unclassified</span></span></td>
<td><span data-ttu-id="58676-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="58676-194">10,000.00</span></span></td>
<td><span data-ttu-id="58676-195">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-196">CC099</span><span class="sxs-lookup"><span data-stu-id="58676-196">CC099</span></span></td>
<td><span data-ttu-id="58676-197">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58676-197">Default cost center</span></span></td>
<td><span data-ttu-id="58676-198">10001</span><span class="sxs-lookup"><span data-stu-id="58676-198">10001</span></span></td>
<td><span data-ttu-id="58676-199">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-199">Electricity</span></span></td>
<td><span data-ttu-id="58676-200">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="58676-200">Unclassified</span></span></td>
<td><span data-ttu-id="58676-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="58676-201">-10,000.00</span></span></td>
<td><span data-ttu-id="58676-202">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-203">CC099</span><span class="sxs-lookup"><span data-stu-id="58676-203">CC099</span></span></td>
<td><span data-ttu-id="58676-204">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58676-204">Default cost center</span></span></td>
<td><span data-ttu-id="58676-205">10001</span><span class="sxs-lookup"><span data-stu-id="58676-205">10001</span></span></td>
<td><span data-ttu-id="58676-206">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-206">Electricity</span></span></td>
<td><span data-ttu-id="58676-207">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-207">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="58676-208">1,000.00</span></span></td>
<td><span data-ttu-id="58676-209">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-210">CC099</span><span class="sxs-lookup"><span data-stu-id="58676-210">CC099</span></span></td>
<td><span data-ttu-id="58676-211">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58676-211">Default cost center</span></span></td>
<td><span data-ttu-id="58676-212">10001</span><span class="sxs-lookup"><span data-stu-id="58676-212">10001</span></span></td>
<td><span data-ttu-id="58676-213">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-213">Electricity</span></span></td>
<td><span data-ttu-id="58676-214">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-214">Variable cost</span></span></td>
<td><span data-ttu-id="58676-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="58676-215">9,000.00</span></span></td>
<td><span data-ttu-id="58676-216">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58676-217">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðarhegðunarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="58676-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="58676-218">Skref 2: Keyra útreikning kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="58676-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="58676-219">Kostnaðardreifing er notuð til að endurúthluta kostnaði frá einum kostnaðarhlut til annars eða fleiri kostnaðarhluta með því að nota viðeigandi úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="58676-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="58676-220">Kostnaðardreifing og kostnaðarúthlutun eru ólíkar að því leyti að kostnaðardreifing kemur alltaf upp á stigi aðalkostnaðareiningar upphaflegs verðs.</span><span class="sxs-lookup"><span data-stu-id="58676-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="58676-221">Tilgreinið kostnaðardreifingarreglu</span><span class="sxs-lookup"><span data-stu-id="58676-221">Define the cost distribution rule</span></span>

<span data-ttu-id="58676-222">Í Fjárhagsbókhaldi er rafmagnskostnaður oft skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="58676-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="58676-223">Í kostnaðarbókhaldi er þessi nálgun ekki nógu nákvæm.</span><span class="sxs-lookup"><span data-stu-id="58676-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="58676-224">Breytilegur kostnaði þarf að dreifa á staka kostnaðarhluti á sanngjörnum grunni.</span><span class="sxs-lookup"><span data-stu-id="58676-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="58676-225">Rökréttasti úthlutunargrunnurinn er notkun á rafmagni (Kwh).</span><span class="sxs-lookup"><span data-stu-id="58676-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="58676-226">Stofnað er tölfræðilegt víddarstak sem er nefnt Rafmagn og rafmagnsnotkun er skráð.</span><span class="sxs-lookup"><span data-stu-id="58676-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="58676-227">Sjálfgefið er að öll tölfræðileg víddarstök verða tiltæk sem úthlutunargrunnur.</span><span class="sxs-lookup"><span data-stu-id="58676-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58676-228">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-228">Cost object</span></span></th>
<th><span data-ttu-id="58676-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="58676-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-230">CC001</span><span class="sxs-lookup"><span data-stu-id="58676-230">CC001</span></span></td>
<td><span data-ttu-id="58676-231">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58676-231">HR</span></span></td>
<td><span data-ttu-id="58676-232">1.000</span><span class="sxs-lookup"><span data-stu-id="58676-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-233">CC002</span><span class="sxs-lookup"><span data-stu-id="58676-233">CC002</span></span></td>
<td><span data-ttu-id="58676-234">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58676-234">Finance</span></span></td>
<td><span data-ttu-id="58676-235">6,000</span><span class="sxs-lookup"><span data-stu-id="58676-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-236">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-236">CC003</span></span></td>
<td><span data-ttu-id="58676-237">Smölun</span><span class="sxs-lookup"><span data-stu-id="58676-237">Assembly</span></span></td>
<td><span data-ttu-id="58676-238">0</span><span class="sxs-lookup"><span data-stu-id="58676-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58676-239">Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunni fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="58676-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58676-240">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-240">Cost object</span></span></th>
<th><span data-ttu-id="58676-241">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="58676-241">Magnitude</span></span></th>
<th><span data-ttu-id="58676-242">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="58676-242">Allocation factor</span></span></th>
<th><span data-ttu-id="58676-243">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58676-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-244">CC001</span><span class="sxs-lookup"><span data-stu-id="58676-244">CC001</span></span></td>
<td><span data-ttu-id="58676-245">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58676-245">HR</span></span></td>
<td><span data-ttu-id="58676-246">1.000</span><span class="sxs-lookup"><span data-stu-id="58676-246">1,000</span></span></td>
<td><span data-ttu-id="58676-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="58676-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="58676-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="58676-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-249">CC002</span><span class="sxs-lookup"><span data-stu-id="58676-249">CC002</span></span></td>
<td><span data-ttu-id="58676-250">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58676-250">Finance</span></span></td>
<td><span data-ttu-id="58676-251">6,000</span><span class="sxs-lookup"><span data-stu-id="58676-251">6,000</span></span></td>
<td><span data-ttu-id="58676-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="58676-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="58676-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="58676-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-254">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-254">CC003</span></span></td>
<td><span data-ttu-id="58676-255">Smölun</span><span class="sxs-lookup"><span data-stu-id="58676-255">Assembly</span></span></td>
<td><span data-ttu-id="58676-256">0</span><span class="sxs-lookup"><span data-stu-id="58676-256">0</span></span></td>
<td><span data-ttu-id="58676-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="58676-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="58676-258">0,00</span><span class="sxs-lookup"><span data-stu-id="58676-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58676-259">Föstum kostnaði þarf að dreifa jafnt á staka kostnaðarhluti sem hafa notað rafmagn.</span><span class="sxs-lookup"><span data-stu-id="58676-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="58676-260">Hægt er að ná þessa niðurstöðu með því að nota tölfræðilegt víddarstakið Rafmagn í úthlutunargrunni reikniformúlu: (Rafmagn &gt; 0,00) Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunn fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="58676-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58676-261">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-261">Cost object</span></span></th>
<th><span data-ttu-id="58676-262">Formúla</span><span class="sxs-lookup"><span data-stu-id="58676-262">Formula</span></span></th>
<th><span data-ttu-id="58676-263">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="58676-263">Magnitude</span></span></th>
<th><span data-ttu-id="58676-264">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="58676-264">Allocation factor</span></span></th>
<th><span data-ttu-id="58676-265">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58676-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-266">CC001</span><span class="sxs-lookup"><span data-stu-id="58676-266">CC001</span></span></td>
<td><span data-ttu-id="58676-267">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58676-267">HR</span></span></td>
<td><span data-ttu-id="58676-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="58676-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="58676-269">1</span><span class="sxs-lookup"><span data-stu-id="58676-269">1</span></span></td>
<td><span data-ttu-id="58676-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="58676-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="58676-271">500,00</span><span class="sxs-lookup"><span data-stu-id="58676-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-272">CC002</span><span class="sxs-lookup"><span data-stu-id="58676-272">CC002</span></span></td>
<td><span data-ttu-id="58676-273">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58676-273">Finance</span></span></td>
<td><span data-ttu-id="58676-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="58676-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="58676-275">1</span><span class="sxs-lookup"><span data-stu-id="58676-275">1</span></span></td>
<td><span data-ttu-id="58676-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="58676-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="58676-277">500,00</span><span class="sxs-lookup"><span data-stu-id="58676-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-278">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-278">CC003</span></span></td>
<td><span data-ttu-id="58676-279">Smölun</span><span class="sxs-lookup"><span data-stu-id="58676-279">Assembly</span></span></td>
<td><span data-ttu-id="58676-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="58676-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="58676-281">0</span><span class="sxs-lookup"><span data-stu-id="58676-281">0</span></span></td>
<td><span data-ttu-id="58676-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="58676-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="58676-283">0,00</span><span class="sxs-lookup"><span data-stu-id="58676-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="58676-284">Færslubók</span><span class="sxs-lookup"><span data-stu-id="58676-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="58676-285">Færslubók</span><span class="sxs-lookup"><span data-stu-id="58676-285">Journal</span></span></th>
<th><span data-ttu-id="58676-286">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="58676-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="58676-287">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="58676-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="58676-288">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="58676-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-289">00002</span><span class="sxs-lookup"><span data-stu-id="58676-289">00002</span></span></td>
<td><span data-ttu-id="58676-290">Útreikningabók kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="58676-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="58676-291">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="58676-291">Fiscal</span></span></td>
<td><span data-ttu-id="58676-292">2017</span><span class="sxs-lookup"><span data-stu-id="58676-292">2017</span></span></td>
<td><span data-ttu-id="58676-293">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="58676-293">Period 1</span></span></td>
<td><span data-ttu-id="58676-294">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="58676-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="58676-295">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="58676-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="58676-296">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="58676-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="58676-297">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="58676-298">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58676-298">Cost element</span></span></th>
<th><span data-ttu-id="58676-299">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58676-299">Cost behavior</span></span></th>
<th><span data-ttu-id="58676-300">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58676-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-301">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="58676-302">CC099</span><span class="sxs-lookup"><span data-stu-id="58676-302">CC099</span></span></td>
<td><span data-ttu-id="58676-303">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58676-303">Default cost center</span></span></td>
<td><span data-ttu-id="58676-304">10001</span><span class="sxs-lookup"><span data-stu-id="58676-304">10001</span></span></td>
<td><span data-ttu-id="58676-305">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-305">Electricity</span></span></td>
<td><span data-ttu-id="58676-306">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-306">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="58676-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-308">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="58676-309">CC099</span><span class="sxs-lookup"><span data-stu-id="58676-309">CC099</span></span></td>
<td><span data-ttu-id="58676-310">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58676-310">Default cost center</span></span></td>
<td><span data-ttu-id="58676-311">10001</span><span class="sxs-lookup"><span data-stu-id="58676-311">10001</span></span></td>
<td><span data-ttu-id="58676-312">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-312">Electricity</span></span></td>
<td><span data-ttu-id="58676-313">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-313">Variable cost</span></span></td>
<td><span data-ttu-id="58676-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="58676-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="58676-315">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="58676-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58676-316">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="58676-317">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58676-317">Cost element</span></span></th>
<th><span data-ttu-id="58676-318">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58676-318">Cost behavior</span></span></th>
<th><span data-ttu-id="58676-319">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58676-319">Amount</span></span></th>
<th><span data-ttu-id="58676-320">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="58676-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-321">CC099</span><span class="sxs-lookup"><span data-stu-id="58676-321">CC099</span></span></td>
<td><span data-ttu-id="58676-322">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58676-322">Default cost center</span></span></td>
<td><span data-ttu-id="58676-323">10001</span><span class="sxs-lookup"><span data-stu-id="58676-323">10001</span></span></td>
<td><span data-ttu-id="58676-324">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-324">Electricity</span></span></td>
<td><span data-ttu-id="58676-325">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-325">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="58676-326">-1,000.00</span></span></td>
<td><span data-ttu-id="58676-327">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-328">CC001</span><span class="sxs-lookup"><span data-stu-id="58676-328">CC001</span></span></td>
<td><span data-ttu-id="58676-329">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58676-329">HR</span></span></td>
<td><span data-ttu-id="58676-330">10001</span><span class="sxs-lookup"><span data-stu-id="58676-330">10001</span></span></td>
<td><span data-ttu-id="58676-331">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-331">Electricity</span></span></td>
<td><span data-ttu-id="58676-332">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-332">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-333">500,00</span><span class="sxs-lookup"><span data-stu-id="58676-333">500.00</span></span></td>
<td><span data-ttu-id="58676-334">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-335">CC002</span><span class="sxs-lookup"><span data-stu-id="58676-335">CC002</span></span></td>
<td><span data-ttu-id="58676-336">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58676-336">Finance</span></span></td>
<td><span data-ttu-id="58676-337">10001</span><span class="sxs-lookup"><span data-stu-id="58676-337">10001</span></span></td>
<td><span data-ttu-id="58676-338">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-338">Electricity</span></span></td>
<td><span data-ttu-id="58676-339">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-339">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-340">500,00</span><span class="sxs-lookup"><span data-stu-id="58676-340">500.00</span></span></td>
<td><span data-ttu-id="58676-341">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-342">CC099</span><span class="sxs-lookup"><span data-stu-id="58676-342">CC099</span></span></td>
<td><span data-ttu-id="58676-343">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="58676-343">Default cost center</span></span></td>
<td><span data-ttu-id="58676-344">10001</span><span class="sxs-lookup"><span data-stu-id="58676-344">10001</span></span></td>
<td><span data-ttu-id="58676-345">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-345">Electricity</span></span></td>
<td><span data-ttu-id="58676-346">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-346">Variable cost</span></span></td>
<td><span data-ttu-id="58676-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="58676-347">-9,000.00</span></span></td>
<td><span data-ttu-id="58676-348">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-349">CC001</span><span class="sxs-lookup"><span data-stu-id="58676-349">CC001</span></span></td>
<td><span data-ttu-id="58676-350">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58676-350">HR</span></span></td>
<td><span data-ttu-id="58676-351">10001</span><span class="sxs-lookup"><span data-stu-id="58676-351">10001</span></span></td>
<td><span data-ttu-id="58676-352">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-352">Electricity</span></span></td>
<td><span data-ttu-id="58676-353">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-353">Variable cost</span></span></td>
<td><span data-ttu-id="58676-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="58676-354">1,285.71</span></span></td>
<td><span data-ttu-id="58676-355">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-356">CC002</span><span class="sxs-lookup"><span data-stu-id="58676-356">CC002</span></span></td>
<td><span data-ttu-id="58676-357">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58676-357">Finance</span></span></td>
<td><span data-ttu-id="58676-358">10001</span><span class="sxs-lookup"><span data-stu-id="58676-358">10001</span></span></td>
<td><span data-ttu-id="58676-359">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-359">Electricity</span></span></td>
<td><span data-ttu-id="58676-360">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-360">Variable cost</span></span></td>
<td><span data-ttu-id="58676-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="58676-361">7,714.29</span></span></td>
<td><span data-ttu-id="58676-362">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58676-363">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðardreifingarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="58676-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="58676-364">Skref 3: Keyra útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="58676-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="58676-365">Sameiginlegur kostnaður er notaður til að rukka einn eða fleiri tilgreinda kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="58676-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="58676-366">Gjöldin byggjast á fyrirframákveðnu kostnaðarhlutfalli og mæligildi úr úthlutuðum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="58676-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="58676-367">Skilgreina sameiginlegan kostnað</span><span class="sxs-lookup"><span data-stu-id="58676-367">Define the overhead rate</span></span>

<span data-ttu-id="58676-368">Kostnaðarhlutur CC001 Mannauður stuðlar að safni innri verka.</span><span class="sxs-lookup"><span data-stu-id="58676-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="58676-369">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsverk til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="58676-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58676-370">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-370">Cost object</span></span></th>
<th><span data-ttu-id="58676-371">Tímar</span><span class="sxs-lookup"><span data-stu-id="58676-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-372">Verk 1</span><span class="sxs-lookup"><span data-stu-id="58676-372">Proj 1</span></span></td>
<td><span data-ttu-id="58676-373">Verk 1</span><span class="sxs-lookup"><span data-stu-id="58676-373">Project 1</span></span></td>
<td><span data-ttu-id="58676-374">3</span><span class="sxs-lookup"><span data-stu-id="58676-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-375">Verk 2</span><span class="sxs-lookup"><span data-stu-id="58676-375">Proj 2</span></span></td>
<td><span data-ttu-id="58676-376">Verk 2</span><span class="sxs-lookup"><span data-stu-id="58676-376">Project 2</span></span></td>
<td><span data-ttu-id="58676-377">1</span><span class="sxs-lookup"><span data-stu-id="58676-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58676-378">Fyrirframákveðið kostnaðarhlutfall fyrir kostnaðarframlag verk hefur verið skilgreint.</span><span class="sxs-lookup"><span data-stu-id="58676-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58676-379">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-379">Cost object</span></span></th>
<th><span data-ttu-id="58676-380">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58676-380">Cost element</span></span></th>
<th><span data-ttu-id="58676-381">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58676-381">Cost behavior</span></span></th>
<th><span data-ttu-id="58676-382">Einingar</span><span class="sxs-lookup"><span data-stu-id="58676-382">Units</span></span></th>
<th><span data-ttu-id="58676-383">Taxti</span><span class="sxs-lookup"><span data-stu-id="58676-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-384">CC001</span><span class="sxs-lookup"><span data-stu-id="58676-384">CC001</span></span></td>
<td><span data-ttu-id="58676-385">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58676-385">HR</span></span></td>
<td><span data-ttu-id="58676-386">10001</span><span class="sxs-lookup"><span data-stu-id="58676-386">10001</span></span></td>
<td><span data-ttu-id="58676-387">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-387">Variable cost</span></span></td>
<td><span data-ttu-id="58676-388">1</span><span class="sxs-lookup"><span data-stu-id="58676-388">1</span></span></td>
<td><span data-ttu-id="58676-389">10</span><span class="sxs-lookup"><span data-stu-id="58676-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58676-390">Eftirfarandi tafla sýnir niðurstöður þegar Mannauðsverk eru notuð sem grunnur við úthlutun.</span><span class="sxs-lookup"><span data-stu-id="58676-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58676-391">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-391">Cost object</span></span></th>
<th><span data-ttu-id="58676-392">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="58676-392">Magnitude</span></span></th>
<th><span data-ttu-id="58676-393">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58676-393">Cost element</span></span></th>
<th><span data-ttu-id="58676-394">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="58676-394">Allocation factor</span></span></th>
<th><span data-ttu-id="58676-395">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58676-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-396">Verk 1</span><span class="sxs-lookup"><span data-stu-id="58676-396">Proj 1</span></span></td>
<td><span data-ttu-id="58676-397">Verk 1</span><span class="sxs-lookup"><span data-stu-id="58676-397">Project 1</span></span></td>
<td><span data-ttu-id="58676-398">3</span><span class="sxs-lookup"><span data-stu-id="58676-398">3</span></span></td>
<td><span data-ttu-id="58676-399">10001</span><span class="sxs-lookup"><span data-stu-id="58676-399">10001</span></span></td>
<td><span data-ttu-id="58676-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="58676-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="58676-401">30,00</span><span class="sxs-lookup"><span data-stu-id="58676-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-402">Verk 2</span><span class="sxs-lookup"><span data-stu-id="58676-402">Proj 2</span></span></td>
<td><span data-ttu-id="58676-403">Verk 2</span><span class="sxs-lookup"><span data-stu-id="58676-403">Project 2</span></span></td>
<td><span data-ttu-id="58676-404">1</span><span class="sxs-lookup"><span data-stu-id="58676-404">1</span></span></td>
<td><span data-ttu-id="58676-405">10001</span><span class="sxs-lookup"><span data-stu-id="58676-405">10001</span></span></td>
<td><span data-ttu-id="58676-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="58676-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="58676-407">10,00</span><span class="sxs-lookup"><span data-stu-id="58676-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="58676-408">Færslubók</span><span class="sxs-lookup"><span data-stu-id="58676-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="58676-409">Færslubók</span><span class="sxs-lookup"><span data-stu-id="58676-409">Journal</span></span></th>
<th><span data-ttu-id="58676-410">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="58676-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="58676-411">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="58676-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="58676-412">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="58676-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-413">00003</span><span class="sxs-lookup"><span data-stu-id="58676-413">00003</span></span></td>
<td><span data-ttu-id="58676-414">Færslubók fyrir útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="58676-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="58676-415">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="58676-415">Fiscal</span></span></td>
<td><span data-ttu-id="58676-416">2017</span><span class="sxs-lookup"><span data-stu-id="58676-416">2017</span></span></td>
<td><span data-ttu-id="58676-417">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="58676-417">Period 1</span></span></td>
<td><span data-ttu-id="58676-418">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="58676-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="58676-419">Bókarfærslur (Bókarfærslur fyrir útreikning sameiginlegs kostnaðar)</span><span class="sxs-lookup"><span data-stu-id="58676-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="58676-420">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="58676-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="58676-421">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-421">Cost object</span></span></th>
<th><span data-ttu-id="58676-422">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="58676-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-423">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="58676-424">Verk 1</span><span class="sxs-lookup"><span data-stu-id="58676-424">Proj 1</span></span></td>
<td><span data-ttu-id="58676-425">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="58676-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="58676-426">3,00</span><span class="sxs-lookup"><span data-stu-id="58676-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-427">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="58676-428">Verk 2</span><span class="sxs-lookup"><span data-stu-id="58676-428">Proj 2</span></span></td>
<td><span data-ttu-id="58676-429">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="58676-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="58676-430">1,00</span><span class="sxs-lookup"><span data-stu-id="58676-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="58676-431">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="58676-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58676-432">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="58676-433">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58676-433">Cost element</span></span></th>
<th><span data-ttu-id="58676-434">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58676-434">Cost behavior</span></span></th>
<th><span data-ttu-id="58676-435">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58676-435">Amount</span></span></th>
<th><span data-ttu-id="58676-436">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="58676-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="58676-437">CC0001</span></span></td>
<td><span data-ttu-id="58676-438">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58676-438">HR</span></span></td>
<td><span data-ttu-id="58676-439">10001</span><span class="sxs-lookup"><span data-stu-id="58676-439">10001</span></span></td>
<td><span data-ttu-id="58676-440">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-440">Electricity</span></span></td>
<td><span data-ttu-id="58676-441">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-441">Variable cost</span></span></td>
<td><span data-ttu-id="58676-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="58676-442">-30.00</span></span></td>
<td><span data-ttu-id="58676-443">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-444">Verk 1</span><span class="sxs-lookup"><span data-stu-id="58676-444">Proj 1</span></span></td>
<td><span data-ttu-id="58676-445">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="58676-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="58676-446">10001</span><span class="sxs-lookup"><span data-stu-id="58676-446">10001</span></span></td>
<td><span data-ttu-id="58676-447">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-447">Electricity</span></span></td>
<td><span data-ttu-id="58676-448">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-448">Variable cost</span></span></td>
<td><span data-ttu-id="58676-449">30,00</span><span class="sxs-lookup"><span data-stu-id="58676-449">30.00</span></span></td>
<td><span data-ttu-id="58676-450">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-451">CC001</span><span class="sxs-lookup"><span data-stu-id="58676-451">CC001</span></span></td>
<td><span data-ttu-id="58676-452">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58676-452">HR</span></span></td>
<td><span data-ttu-id="58676-453">10001</span><span class="sxs-lookup"><span data-stu-id="58676-453">10001</span></span></td>
<td><span data-ttu-id="58676-454">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-454">Electricity</span></span></td>
<td><span data-ttu-id="58676-455">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-455">Variable cost</span></span></td>
<td><span data-ttu-id="58676-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="58676-456">-10.00</span></span></td>
<td><span data-ttu-id="58676-457">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-458">Verk 2</span><span class="sxs-lookup"><span data-stu-id="58676-458">Proj 2</span></span></td>
<td><span data-ttu-id="58676-459">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="58676-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="58676-460">10001</span><span class="sxs-lookup"><span data-stu-id="58676-460">10001</span></span></td>
<td><span data-ttu-id="58676-461">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-461">Electricity</span></span></td>
<td><span data-ttu-id="58676-462">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-462">Variable cost</span></span></td>
<td><span data-ttu-id="58676-463">10,00</span><span class="sxs-lookup"><span data-stu-id="58676-463">10.00</span></span></td>
<td><span data-ttu-id="58676-464">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58676-465">Nánari upplýsingar er að finna í [Framkvæma útreikning fastakostnaðar](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="58676-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="58676-466">Skref 4: Keyra útreikning kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="58676-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="58676-467">Úthlutun er notuð til að úthluta stöðu kostnaðarhlutar í öðrum kostnaðarhlutum með því að nota úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="58676-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="58676-468">Finance and Operations styður gagnvirka úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="58676-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="58676-469">Í gagnvirkri úthlutunaraðferð er sú sameiginlega þjónusta sem hjálparkostnaðarhlutir skiptast á viðurkennd að fullu.</span><span class="sxs-lookup"><span data-stu-id="58676-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="58676-470">Kerfið ákvarðar sjálfkrafa rétta röð til að framkvæma úthlutun eftir.</span><span class="sxs-lookup"><span data-stu-id="58676-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="58676-471">Stöðu kostnaðarhluta er úthlutað með einum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="58676-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="58676-472">Úthlutanir þvert á víddir kostnaðarhluta og viðkomandi stök þeirra eru studdar.</span><span class="sxs-lookup"><span data-stu-id="58676-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="58676-473">Úthlutun pöntunarinnar er stjórnað af stýrieiningu kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="58676-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="58676-474">[![Gagnkvæm aðferð](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="58676-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="58676-475">Tilgreinið kostnaðarúthlutun</span><span class="sxs-lookup"><span data-stu-id="58676-475">Define the cost allocation</span></span>

<span data-ttu-id="58676-476">Hér er einfalt dæmi sem útskýrir hvernig hægt er að rekja flæði kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="58676-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="58676-477">Kostnaðarhlutir CC001 Mannauður leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="58676-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="58676-478">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="58676-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58676-479">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-479">Cost object</span></span></th>
<th><span data-ttu-id="58676-480">Mannauðsþjónusta</span><span class="sxs-lookup"><span data-stu-id="58676-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-481">CC002</span><span class="sxs-lookup"><span data-stu-id="58676-481">CC002</span></span></td>
<td><span data-ttu-id="58676-482">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58676-482">Finance</span></span></td>
<td><span data-ttu-id="58676-483">35</span><span class="sxs-lookup"><span data-stu-id="58676-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-484">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-484">CC003</span></span></td>
<td><span data-ttu-id="58676-485">Smölun</span><span class="sxs-lookup"><span data-stu-id="58676-485">Assembly</span></span></td>
<td><span data-ttu-id="58676-486">55</span><span class="sxs-lookup"><span data-stu-id="58676-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-487">CC004</span><span class="sxs-lookup"><span data-stu-id="58676-487">CC004</span></span></td>
<td><span data-ttu-id="58676-488">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58676-488">Packaging</span></span></td>
<td><span data-ttu-id="58676-489">10</span><span class="sxs-lookup"><span data-stu-id="58676-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58676-490">Kostnaðarhlutir CC002 Fjármál leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="58676-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="58676-491">Stofnað er tölfræðilegt víddarstak sem kallast Fjármálaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="58676-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58676-492">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-492">Cost object</span></span></th>
<th><span data-ttu-id="58676-493">Fjármálaþjónusta</span><span class="sxs-lookup"><span data-stu-id="58676-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-494">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-494">CC003</span></span></td>
<td><span data-ttu-id="58676-495">Smölun</span><span class="sxs-lookup"><span data-stu-id="58676-495">Assembly</span></span></td>
<td><span data-ttu-id="58676-496">65</span><span class="sxs-lookup"><span data-stu-id="58676-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-497">CC004</span><span class="sxs-lookup"><span data-stu-id="58676-497">CC004</span></span></td>
<td><span data-ttu-id="58676-498">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58676-498">Packaging</span></span></td>
<td><span data-ttu-id="58676-499">35</span><span class="sxs-lookup"><span data-stu-id="58676-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58676-500">Kostnaðarhlutir CC003 Samsetning leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="58676-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="58676-501">Meðlimur tölfræðilega víddar sem kallast Mannauður verk er stofnað til að mælvíddarstaka notuðum magnitude.</span><span class="sxs-lookup"><span data-stu-id="58676-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58676-502">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-502">Cost object</span></span></th>
<th><span data-ttu-id="58676-503">Samsetningarþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="58676-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-504">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-504">Prod 1</span></span></td>
<td><span data-ttu-id="58676-505">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-505">Product 1</span></span></td>
<td><span data-ttu-id="58676-506">60</span><span class="sxs-lookup"><span data-stu-id="58676-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-507">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-507">Prod 2</span></span></td>
<td><span data-ttu-id="58676-508">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-508">Product 2</span></span></td>
<td><span data-ttu-id="58676-509">20</span><span class="sxs-lookup"><span data-stu-id="58676-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58676-510">Kostnaðarhlutir CC004 Umbúðir leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="58676-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="58676-511">Stofnað er tölfræðilegt víddarstak sem kallast Umbúðaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="58676-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58676-512">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-512">Cost object</span></span></th>
<th><span data-ttu-id="58676-513">Umbúðaþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="58676-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-514">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-514">Prod 1</span></span></td>
<td><span data-ttu-id="58676-515">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-515">Product 1</span></span></td>
<td><span data-ttu-id="58676-516">80</span><span class="sxs-lookup"><span data-stu-id="58676-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-517">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-517">Prod 2</span></span></td>
<td><span data-ttu-id="58676-518">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-518">Product 2</span></span></td>
<td><span data-ttu-id="58676-519">sept</span><span class="sxs-lookup"><span data-stu-id="58676-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="58676-520">Í Finance and Operations er hægt að afleiða tölfræðiaðgerðir eins og framleiðslutíma sem vara notar frá upprunagögnum.</span><span class="sxs-lookup"><span data-stu-id="58676-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="58676-521">Nánari upplýsingar er að finna í [Veitusniðmát tölfræðiaðgerðar](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="58676-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="58676-522">Eftirfarandi tafla sýnir niðurstöður þegar mannauðsþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="58676-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58676-523">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-523">Cost object</span></span></th>
<th><span data-ttu-id="58676-524">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="58676-524">Magnitude</span></span></th>
<th><span data-ttu-id="58676-525">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="58676-525">Allocation factor</span></span></th>
<th><span data-ttu-id="58676-526">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58676-526">Amount</span></span></th>
<th><span data-ttu-id="58676-527">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58676-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-528">CC002</span><span class="sxs-lookup"><span data-stu-id="58676-528">CC002</span></span></td>
<td><span data-ttu-id="58676-529">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58676-529">Finance</span></span></td>
<td><span data-ttu-id="58676-530">35</span><span class="sxs-lookup"><span data-stu-id="58676-530">35</span></span></td>
<td><span data-ttu-id="58676-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="58676-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="58676-532">175.00</span><span class="sxs-lookup"><span data-stu-id="58676-532">175.00</span></span></td>
<td><span data-ttu-id="58676-533">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-534">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-534">CC003</span></span></td>
<td><span data-ttu-id="58676-535">Smölun</span><span class="sxs-lookup"><span data-stu-id="58676-535">Assembly</span></span></td>
<td><span data-ttu-id="58676-536">55</span><span class="sxs-lookup"><span data-stu-id="58676-536">55</span></span></td>
<td><span data-ttu-id="58676-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="58676-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="58676-538">275.00</span><span class="sxs-lookup"><span data-stu-id="58676-538">275.00</span></span></td>
<td><span data-ttu-id="58676-539">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-540">CC004</span><span class="sxs-lookup"><span data-stu-id="58676-540">CC004</span></span></td>
<td><span data-ttu-id="58676-541">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58676-541">Packaging</span></span></td>
<td><span data-ttu-id="58676-542">10</span><span class="sxs-lookup"><span data-stu-id="58676-542">10</span></span></td>
<td><span data-ttu-id="58676-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="58676-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="58676-544">50,00</span><span class="sxs-lookup"><span data-stu-id="58676-544">50.00</span></span></td>
<td><span data-ttu-id="58676-545">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-546">CC002</span><span class="sxs-lookup"><span data-stu-id="58676-546">CC002</span></span></td>
<td><span data-ttu-id="58676-547">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58676-547">Finance</span></span></td>
<td><span data-ttu-id="58676-548">35</span><span class="sxs-lookup"><span data-stu-id="58676-548">35</span></span></td>
<td><span data-ttu-id="58676-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="58676-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="58676-550">436.00</span><span class="sxs-lookup"><span data-stu-id="58676-550">436.00</span></span></td>
<td><span data-ttu-id="58676-551">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-552">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-552">CC003</span></span></td>
<td><span data-ttu-id="58676-553">Smölun</span><span class="sxs-lookup"><span data-stu-id="58676-553">Assembly</span></span></td>
<td><span data-ttu-id="58676-554">55</span><span class="sxs-lookup"><span data-stu-id="58676-554">55</span></span></td>
<td><span data-ttu-id="58676-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="58676-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="58676-556">685.14</span><span class="sxs-lookup"><span data-stu-id="58676-556">685.14</span></span></td>
<td><span data-ttu-id="58676-557">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-558">CC004</span><span class="sxs-lookup"><span data-stu-id="58676-558">CC004</span></span></td>
<td><span data-ttu-id="58676-559">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58676-559">Packaging</span></span></td>
<td><span data-ttu-id="58676-560">10</span><span class="sxs-lookup"><span data-stu-id="58676-560">10</span></span></td>
<td><span data-ttu-id="58676-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="58676-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="58676-562">124.57</span><span class="sxs-lookup"><span data-stu-id="58676-562">124.57</span></span></td>
<td><span data-ttu-id="58676-563">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58676-564">Eftirfarandi tafla sýnir niðurstöður þegar Fjármálaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="58676-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58676-565">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-565">Cost object</span></span></th>
<th><span data-ttu-id="58676-566">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="58676-566">Magnitude</span></span></th>
<th><span data-ttu-id="58676-567">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="58676-567">Allocation factor</span></span></th>
<th><span data-ttu-id="58676-568">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58676-568">Amount</span></span></th>
<th><span data-ttu-id="58676-569">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58676-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-570">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-570">CC003</span></span></td>
<td><span data-ttu-id="58676-571">Smölun</span><span class="sxs-lookup"><span data-stu-id="58676-571">Assembly</span></span></td>
<td><span data-ttu-id="58676-572">65</span><span class="sxs-lookup"><span data-stu-id="58676-572">65</span></span></td>
<td><span data-ttu-id="58676-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="58676-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="58676-574">438.75</span><span class="sxs-lookup"><span data-stu-id="58676-574">438.75</span></span></td>
<td><span data-ttu-id="58676-575">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-576">CC004</span><span class="sxs-lookup"><span data-stu-id="58676-576">CC004</span></span></td>
<td><span data-ttu-id="58676-577">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58676-577">Packaging</span></span></td>
<td><span data-ttu-id="58676-578">35</span><span class="sxs-lookup"><span data-stu-id="58676-578">35</span></span></td>
<td><span data-ttu-id="58676-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="58676-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="58676-580">236.25</span><span class="sxs-lookup"><span data-stu-id="58676-580">236.25</span></span></td>
<td><span data-ttu-id="58676-581">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-582">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-582">CC003</span></span></td>
<td><span data-ttu-id="58676-583">Smölun</span><span class="sxs-lookup"><span data-stu-id="58676-583">Assembly</span></span></td>
<td><span data-ttu-id="58676-584">65</span><span class="sxs-lookup"><span data-stu-id="58676-584">65</span></span></td>
<td><span data-ttu-id="58676-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="58676-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="58676-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="58676-586">5,297.69</span></span></td>
<td><span data-ttu-id="58676-587">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-588">CC004</span><span class="sxs-lookup"><span data-stu-id="58676-588">CC004</span></span></td>
<td><span data-ttu-id="58676-589">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58676-589">Packaging</span></span></td>
<td><span data-ttu-id="58676-590">35</span><span class="sxs-lookup"><span data-stu-id="58676-590">35</span></span></td>
<td><span data-ttu-id="58676-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="58676-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="58676-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="58676-592">2,852.60</span></span></td>
<td><span data-ttu-id="58676-593">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58676-594">Eftirfarandi tafla sýnir niðurstöður þegar Samsetningarþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="58676-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58676-595">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-595">Cost object</span></span></th>
<th><span data-ttu-id="58676-596">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="58676-596">Magnitude</span></span></th>
<th><span data-ttu-id="58676-597">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="58676-597">Allocation factor</span></span></th>
<th><span data-ttu-id="58676-598">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58676-598">Amount</span></span></th>
<th><span data-ttu-id="58676-599">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58676-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-600">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-600">Prod 1</span></span></td>
<td><span data-ttu-id="58676-601">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-601">Product 1</span></span></td>
<td><span data-ttu-id="58676-602">60</span><span class="sxs-lookup"><span data-stu-id="58676-602">60</span></span></td>
<td><span data-ttu-id="58676-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="58676-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="58676-604">535.31</span><span class="sxs-lookup"><span data-stu-id="58676-604">535.31</span></span></td>
<td><span data-ttu-id="58676-605">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-606">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-606">Prod 2</span></span></td>
<td><span data-ttu-id="58676-607">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-607">Product 2</span></span></td>
<td><span data-ttu-id="58676-608">20</span><span class="sxs-lookup"><span data-stu-id="58676-608">20</span></span></td>
<td><span data-ttu-id="58676-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="58676-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="58676-610">178.44</span><span class="sxs-lookup"><span data-stu-id="58676-610">178.44</span></span></td>
<td><span data-ttu-id="58676-611">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-612">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-612">Prod 1</span></span></td>
<td><span data-ttu-id="58676-613">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-613">Product 1</span></span></td>
<td><span data-ttu-id="58676-614">60</span><span class="sxs-lookup"><span data-stu-id="58676-614">60</span></span></td>
<td><span data-ttu-id="58676-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="58676-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="58676-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="58676-616">4,487.12</span></span></td>
<td><span data-ttu-id="58676-617">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-618">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-618">Prod 2</span></span></td>
<td><span data-ttu-id="58676-619">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-619">Product 2</span></span></td>
<td><span data-ttu-id="58676-620">20</span><span class="sxs-lookup"><span data-stu-id="58676-620">20</span></span></td>
<td><span data-ttu-id="58676-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="58676-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="58676-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="58676-622">1,495.71</span></span></td>
<td><span data-ttu-id="58676-623">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="58676-624">Eftirfarandi tafla sýnir niðurstöður þegar Umbúðaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="58676-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58676-625">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-625">Cost object</span></span></th>
<th><span data-ttu-id="58676-626">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="58676-626">Magnitude</span></span></th>
<th><span data-ttu-id="58676-627">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="58676-627">Allocation factor</span></span></th>
<th><span data-ttu-id="58676-628">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58676-628">Amount</span></span></th>
<th><span data-ttu-id="58676-629">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58676-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-630">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-630">Prod 1</span></span></td>
<td><span data-ttu-id="58676-631">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-631">Product 1</span></span></td>
<td><span data-ttu-id="58676-632">80</span><span class="sxs-lookup"><span data-stu-id="58676-632">80</span></span></td>
<td><span data-ttu-id="58676-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="58676-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="58676-634">241.05</span><span class="sxs-lookup"><span data-stu-id="58676-634">241.05</span></span></td>
<td><span data-ttu-id="58676-635">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-636">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-636">Prod 2</span></span></td>
<td><span data-ttu-id="58676-637">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-637">Product 2</span></span></td>
<td><span data-ttu-id="58676-638">15</span><span class="sxs-lookup"><span data-stu-id="58676-638">15</span></span></td>
<td><span data-ttu-id="58676-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="58676-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="58676-640">45.20</span><span class="sxs-lookup"><span data-stu-id="58676-640">45.20</span></span></td>
<td><span data-ttu-id="58676-641">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-642">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-642">Prod 1</span></span></td>
<td><span data-ttu-id="58676-643">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-643">Product 1</span></span></td>
<td><span data-ttu-id="58676-644">80</span><span class="sxs-lookup"><span data-stu-id="58676-644">80</span></span></td>
<td><span data-ttu-id="58676-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="58676-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="58676-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="58676-646">2,507.09</span></span></td>
<td><span data-ttu-id="58676-647">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-648">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-648">Prod 2</span></span></td>
<td><span data-ttu-id="58676-649">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-649">Product 2</span></span></td>
<td><span data-ttu-id="58676-650">15</span><span class="sxs-lookup"><span data-stu-id="58676-650">15</span></span></td>
<td><span data-ttu-id="58676-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="58676-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="58676-652">470.08</span><span class="sxs-lookup"><span data-stu-id="58676-652">470.08</span></span></td>
<td><span data-ttu-id="58676-653">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="58676-654">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="58676-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="58676-655">Færslubók</span><span class="sxs-lookup"><span data-stu-id="58676-655">Journal</span></span></th>
<th><span data-ttu-id="58676-656">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="58676-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="58676-657">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="58676-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="58676-658">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="58676-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-659">00004</span><span class="sxs-lookup"><span data-stu-id="58676-659">00004</span></span></td>
<td><span data-ttu-id="58676-660">Færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="58676-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="58676-661">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="58676-661">Fiscal</span></span></td>
<td><span data-ttu-id="58676-662">2017</span><span class="sxs-lookup"><span data-stu-id="58676-662">2017</span></span></td>
<td><span data-ttu-id="58676-663">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="58676-663">Period 1</span></span></td>
<td><span data-ttu-id="58676-664">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="58676-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="58676-665">Færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="58676-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="58676-666">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="58676-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="58676-667">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="58676-668">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58676-668">Cost element</span></span></th>
<th><span data-ttu-id="58676-669">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58676-669">Cost behavior</span></span></th>
<th><span data-ttu-id="58676-670">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58676-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-671">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="58676-672">CC001</span><span class="sxs-lookup"><span data-stu-id="58676-672">CC001</span></span></td>
<td><span data-ttu-id="58676-673">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58676-673">HR</span></span></td>
<td><span data-ttu-id="58676-674">10001</span><span class="sxs-lookup"><span data-stu-id="58676-674">10001</span></span></td>
<td><span data-ttu-id="58676-675">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-675">Electricity</span></span></td>
<td><span data-ttu-id="58676-676">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-676">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-677">500,00</span><span class="sxs-lookup"><span data-stu-id="58676-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-678">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="58676-679">CC001</span><span class="sxs-lookup"><span data-stu-id="58676-679">CC001</span></span></td>
<td><span data-ttu-id="58676-680">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58676-680">HR</span></span></td>
<td><span data-ttu-id="58676-681">10001</span><span class="sxs-lookup"><span data-stu-id="58676-681">10001</span></span></td>
<td><span data-ttu-id="58676-682">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-682">Electricity</span></span></td>
<td><span data-ttu-id="58676-683">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-683">Variable cost</span></span></td>
<td><span data-ttu-id="58676-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="58676-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-685">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="58676-686">CC002</span><span class="sxs-lookup"><span data-stu-id="58676-686">CC002</span></span></td>
<td><span data-ttu-id="58676-687">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58676-687">Finance</span></span></td>
<td><span data-ttu-id="58676-688">10001</span><span class="sxs-lookup"><span data-stu-id="58676-688">10001</span></span></td>
<td><span data-ttu-id="58676-689">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-689">Electricity</span></span></td>
<td><span data-ttu-id="58676-690">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-690">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-691">675.00</span><span class="sxs-lookup"><span data-stu-id="58676-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-692">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="58676-693">CC002</span><span class="sxs-lookup"><span data-stu-id="58676-693">CC002</span></span></td>
<td><span data-ttu-id="58676-694">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58676-694">Finance</span></span></td>
<td><span data-ttu-id="58676-695">10001</span><span class="sxs-lookup"><span data-stu-id="58676-695">10001</span></span></td>
<td><span data-ttu-id="58676-696">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-696">Electricity</span></span></td>
<td><span data-ttu-id="58676-697">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-697">Variable cost</span></span></td>
<td><span data-ttu-id="58676-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="58676-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-699">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="58676-700">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-700">CC003</span></span></td>
<td><span data-ttu-id="58676-701">Smölun</span><span class="sxs-lookup"><span data-stu-id="58676-701">Assembly</span></span></td>
<td><span data-ttu-id="58676-702">10001</span><span class="sxs-lookup"><span data-stu-id="58676-702">10001</span></span></td>
<td><span data-ttu-id="58676-703">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-703">Electricity</span></span></td>
<td><span data-ttu-id="58676-704">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-704">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-705">713.75</span><span class="sxs-lookup"><span data-stu-id="58676-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-706">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="58676-707">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-707">CC003</span></span></td>
<td><span data-ttu-id="58676-708">Smölun</span><span class="sxs-lookup"><span data-stu-id="58676-708">Assembly</span></span></td>
<td><span data-ttu-id="58676-709">10001</span><span class="sxs-lookup"><span data-stu-id="58676-709">10001</span></span></td>
<td><span data-ttu-id="58676-710">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-710">Electricity</span></span></td>
<td><span data-ttu-id="58676-711">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-711">Variable cost</span></span></td>
<td><span data-ttu-id="58676-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="58676-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-713">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="58676-714">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-714">CC003</span></span></td>
<td><span data-ttu-id="58676-715">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58676-715">Packaging</span></span></td>
<td><span data-ttu-id="58676-716">10001</span><span class="sxs-lookup"><span data-stu-id="58676-716">10001</span></span></td>
<td><span data-ttu-id="58676-717">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-717">Electricity</span></span></td>
<td><span data-ttu-id="58676-718">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-718">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-719">286.25</span><span class="sxs-lookup"><span data-stu-id="58676-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-720">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="58676-721">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-721">CC003</span></span></td>
<td><span data-ttu-id="58676-722">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58676-722">Packaging</span></span></td>
<td><span data-ttu-id="58676-723">10001</span><span class="sxs-lookup"><span data-stu-id="58676-723">10001</span></span></td>
<td><span data-ttu-id="58676-724">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-724">Electricity</span></span></td>
<td><span data-ttu-id="58676-725">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-725">Variable cost</span></span></td>
<td><span data-ttu-id="58676-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="58676-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-727">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="58676-728">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-728">Prod 1</span></span></td>
<td><span data-ttu-id="58676-729">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-729">Product 1</span></span></td>
<td><span data-ttu-id="58676-730">10001</span><span class="sxs-lookup"><span data-stu-id="58676-730">10001</span></span></td>
<td><span data-ttu-id="58676-731">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-731">Electricity</span></span></td>
<td><span data-ttu-id="58676-732">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-732">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-733">776.36</span><span class="sxs-lookup"><span data-stu-id="58676-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-734">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="58676-735">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-735">Prod 1</span></span></td>
<td><span data-ttu-id="58676-736">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-736">Product 1</span></span></td>
<td><span data-ttu-id="58676-737">10001</span><span class="sxs-lookup"><span data-stu-id="58676-737">10001</span></span></td>
<td><span data-ttu-id="58676-738">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-738">Electricity</span></span></td>
<td><span data-ttu-id="58676-739">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-739">Variable cost</span></span></td>
<td><span data-ttu-id="58676-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="58676-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-741">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="58676-742">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-742">Prod 2</span></span></td>
<td><span data-ttu-id="58676-743">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-743">Product 1</span></span></td>
<td><span data-ttu-id="58676-744">10001</span><span class="sxs-lookup"><span data-stu-id="58676-744">10001</span></span></td>
<td><span data-ttu-id="58676-745">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-745">Electricity</span></span></td>
<td><span data-ttu-id="58676-746">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-746">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-747">223.64</span><span class="sxs-lookup"><span data-stu-id="58676-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-748">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="58676-749">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-749">Prod 2</span></span></td>
<td><span data-ttu-id="58676-750">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-750">Product 1</span></span></td>
<td><span data-ttu-id="58676-751">10001</span><span class="sxs-lookup"><span data-stu-id="58676-751">10001</span></span></td>
<td><span data-ttu-id="58676-752">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-752">Electricity</span></span></td>
<td><span data-ttu-id="58676-753">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-753">Variable cost</span></span></td>
<td><span data-ttu-id="58676-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="58676-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="58676-755">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="58676-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="58676-756">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="58676-757">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58676-757">Cost element</span></span></th>
<th><span data-ttu-id="58676-758">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="58676-758">Cost behavior</span></span></th>
<th><span data-ttu-id="58676-759">Upphæð</span><span class="sxs-lookup"><span data-stu-id="58676-759">Amount</span></span></th>
<th><span data-ttu-id="58676-760">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="58676-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="58676-761">CC001</span><span class="sxs-lookup"><span data-stu-id="58676-761">CC001</span></span></td>
<td><span data-ttu-id="58676-762">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58676-762">HR</span></span></td>
<td><span data-ttu-id="58676-763">10001</span><span class="sxs-lookup"><span data-stu-id="58676-763">10001</span></span></td>
<td><span data-ttu-id="58676-764">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-764">Electricity</span></span></td>
<td><span data-ttu-id="58676-765">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-765">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="58676-766">-500.00</span></span></td>
<td><span data-ttu-id="58676-767">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-768">CC002</span><span class="sxs-lookup"><span data-stu-id="58676-768">CC002</span></span></td>
<td><span data-ttu-id="58676-769">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58676-769">Finance</span></span></td>
<td><span data-ttu-id="58676-770">10001</span><span class="sxs-lookup"><span data-stu-id="58676-770">10001</span></span></td>
<td><span data-ttu-id="58676-771">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-771">Electricity</span></span></td>
<td><span data-ttu-id="58676-772">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-772">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-773">175.00</span><span class="sxs-lookup"><span data-stu-id="58676-773">175.00</span></span></td>
<td><span data-ttu-id="58676-774">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-775">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-775">CC003</span></span></td>
<td><span data-ttu-id="58676-776">Smölun</span><span class="sxs-lookup"><span data-stu-id="58676-776">Assembly</span></span></td>
<td><span data-ttu-id="58676-777">10001</span><span class="sxs-lookup"><span data-stu-id="58676-777">10001</span></span></td>
<td><span data-ttu-id="58676-778">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-778">Electricity</span></span></td>
<td><span data-ttu-id="58676-779">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-779">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-780">275.00</span><span class="sxs-lookup"><span data-stu-id="58676-780">275.00</span></span></td>
<td><span data-ttu-id="58676-781">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-782">CC004</span><span class="sxs-lookup"><span data-stu-id="58676-782">CC004</span></span></td>
<td><span data-ttu-id="58676-783">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58676-783">Packaging</span></span></td>
<td><span data-ttu-id="58676-784">10001</span><span class="sxs-lookup"><span data-stu-id="58676-784">10001</span></span></td>
<td><span data-ttu-id="58676-785">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-785">Electricity</span></span></td>
<td><span data-ttu-id="58676-786">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-786">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-787">50,00</span><span class="sxs-lookup"><span data-stu-id="58676-787">50,00</span></span></td>
<td><span data-ttu-id="58676-788">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-789">CC001</span><span class="sxs-lookup"><span data-stu-id="58676-789">CC001</span></span></td>
<td><span data-ttu-id="58676-790">Mannauður</span><span class="sxs-lookup"><span data-stu-id="58676-790">HR</span></span></td>
<td><span data-ttu-id="58676-791">10001</span><span class="sxs-lookup"><span data-stu-id="58676-791">10001</span></span></td>
<td><span data-ttu-id="58676-792">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-792">Electricity</span></span></td>
<td><span data-ttu-id="58676-793">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-793">Variable cost</span></span></td>
<td><span data-ttu-id="58676-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="58676-794">-1,245.71</span></span></td>
<td><span data-ttu-id="58676-795">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-796">CC002</span><span class="sxs-lookup"><span data-stu-id="58676-796">CC002</span></span></td>
<td><span data-ttu-id="58676-797">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58676-797">Finance</span></span></td>
<td><span data-ttu-id="58676-798">10001</span><span class="sxs-lookup"><span data-stu-id="58676-798">10001</span></span></td>
<td><span data-ttu-id="58676-799">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-799">Electricity</span></span></td>
<td><span data-ttu-id="58676-800">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-800">Variable cost</span></span></td>
<td><span data-ttu-id="58676-801">436.00</span><span class="sxs-lookup"><span data-stu-id="58676-801">436.00</span></span></td>
<td><span data-ttu-id="58676-802">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-803">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-803">CC003</span></span></td>
<td><span data-ttu-id="58676-804">Smölun</span><span class="sxs-lookup"><span data-stu-id="58676-804">Assembly</span></span></td>
<td><span data-ttu-id="58676-805">10001</span><span class="sxs-lookup"><span data-stu-id="58676-805">10001</span></span></td>
<td><span data-ttu-id="58676-806">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-806">Electricity</span></span></td>
<td><span data-ttu-id="58676-807">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-807">Variable cost</span></span></td>
<td><span data-ttu-id="58676-808">685.14</span><span class="sxs-lookup"><span data-stu-id="58676-808">685.14</span></span></td>
<td><span data-ttu-id="58676-809">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-810">CC004</span><span class="sxs-lookup"><span data-stu-id="58676-810">CC004</span></span></td>
<td><span data-ttu-id="58676-811">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58676-811">Packaging</span></span></td>
<td><span data-ttu-id="58676-812">10001</span><span class="sxs-lookup"><span data-stu-id="58676-812">10001</span></span></td>
<td><span data-ttu-id="58676-813">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-813">Electricity</span></span></td>
<td><span data-ttu-id="58676-814">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-814">Variable cost</span></span></td>
<td><span data-ttu-id="58676-815">124.57</span><span class="sxs-lookup"><span data-stu-id="58676-815">124.57</span></span></td>
<td><span data-ttu-id="58676-816">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-817">CC002</span><span class="sxs-lookup"><span data-stu-id="58676-817">CC002</span></span></td>
<td><span data-ttu-id="58676-818">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58676-818">Finance</span></span></td>
<td><span data-ttu-id="58676-819">10001</span><span class="sxs-lookup"><span data-stu-id="58676-819">10001</span></span></td>
<td><span data-ttu-id="58676-820">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-820">Electricity</span></span></td>
<td><span data-ttu-id="58676-821">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-821">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="58676-822">-675.00</span></span></td>
<td><span data-ttu-id="58676-823">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-824">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-824">CC003</span></span></td>
<td><span data-ttu-id="58676-825">Smölun</span><span class="sxs-lookup"><span data-stu-id="58676-825">Assembly</span></span></td>
<td><span data-ttu-id="58676-826">10001</span><span class="sxs-lookup"><span data-stu-id="58676-826">10001</span></span></td>
<td><span data-ttu-id="58676-827">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-827">Electricity</span></span></td>
<td><span data-ttu-id="58676-828">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-828">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-829">438.75</span><span class="sxs-lookup"><span data-stu-id="58676-829">438.75</span></span></td>
<td><span data-ttu-id="58676-830">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-831">CC004</span><span class="sxs-lookup"><span data-stu-id="58676-831">CC004</span></span></td>
<td><span data-ttu-id="58676-832">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58676-832">Packaging</span></span></td>
<td><span data-ttu-id="58676-833">10001</span><span class="sxs-lookup"><span data-stu-id="58676-833">10001</span></span></td>
<td><span data-ttu-id="58676-834">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-834">Electricity</span></span></td>
<td><span data-ttu-id="58676-835">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-835">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-836">236.25</span><span class="sxs-lookup"><span data-stu-id="58676-836">236.25</span></span></td>
<td><span data-ttu-id="58676-837">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-838">CC002</span><span class="sxs-lookup"><span data-stu-id="58676-838">CC002</span></span></td>
<td><span data-ttu-id="58676-839">Fjármál</span><span class="sxs-lookup"><span data-stu-id="58676-839">Finance</span></span></td>
<td><span data-ttu-id="58676-840">10001</span><span class="sxs-lookup"><span data-stu-id="58676-840">10001</span></span></td>
<td><span data-ttu-id="58676-841">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-841">Electricity</span></span></td>
<td><span data-ttu-id="58676-842">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-842">Variable cost</span></span></td>
<td><span data-ttu-id="58676-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="58676-843">-8,150.29</span></span></td>
<td><span data-ttu-id="58676-844">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-845">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-845">CC003</span></span></td>
<td><span data-ttu-id="58676-846">Smölun</span><span class="sxs-lookup"><span data-stu-id="58676-846">Assembly</span></span></td>
<td><span data-ttu-id="58676-847">10001</span><span class="sxs-lookup"><span data-stu-id="58676-847">10001</span></span></td>
<td><span data-ttu-id="58676-848">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-848">Electricity</span></span></td>
<td><span data-ttu-id="58676-849">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-849">Variable cost</span></span></td>
<td><span data-ttu-id="58676-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="58676-850">5,297.69</span></span></td>
<td><span data-ttu-id="58676-851">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-852">CC004</span><span class="sxs-lookup"><span data-stu-id="58676-852">CC004</span></span></td>
<td><span data-ttu-id="58676-853">Pakkning</span><span class="sxs-lookup"><span data-stu-id="58676-853">Packaging</span></span></td>
<td><span data-ttu-id="58676-854">10001</span><span class="sxs-lookup"><span data-stu-id="58676-854">10001</span></span></td>
<td><span data-ttu-id="58676-855">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-855">Electricity</span></span></td>
<td><span data-ttu-id="58676-856">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-856">Variable cost</span></span></td>
<td><span data-ttu-id="58676-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="58676-857">2,852.60</span></span></td>
<td><span data-ttu-id="58676-858">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-859">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-859">CC003</span></span></td>
<td><span data-ttu-id="58676-860">Smölun</span><span class="sxs-lookup"><span data-stu-id="58676-860">Assembly</span></span></td>
<td><span data-ttu-id="58676-861">10001</span><span class="sxs-lookup"><span data-stu-id="58676-861">10001</span></span></td>
<td><span data-ttu-id="58676-862">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-862">Electricity</span></span></td>
<td><span data-ttu-id="58676-863">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-863">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="58676-864">-713.75</span></span></td>
<td><span data-ttu-id="58676-865">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-866">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-866">Prod 1</span></span></td>
<td><span data-ttu-id="58676-867">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-867">Product 1</span></span></td>
<td><span data-ttu-id="58676-868">10001</span><span class="sxs-lookup"><span data-stu-id="58676-868">10001</span></span></td>
<td><span data-ttu-id="58676-869">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-869">Electricity</span></span></td>
<td><span data-ttu-id="58676-870">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-870">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-871">535.31</span><span class="sxs-lookup"><span data-stu-id="58676-871">535.31</span></span></td>
<td><span data-ttu-id="58676-872">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-873">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-873">Prod 2</span></span></td>
<td><span data-ttu-id="58676-874">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-874">Product 2</span></span></td>
<td><span data-ttu-id="58676-875">10001</span><span class="sxs-lookup"><span data-stu-id="58676-875">10001</span></span></td>
<td><span data-ttu-id="58676-876">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-876">Electricity</span></span></td>
<td><span data-ttu-id="58676-877">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-877">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-878">178.44</span><span class="sxs-lookup"><span data-stu-id="58676-878">178.44</span></span></td>
<td><span data-ttu-id="58676-879">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-880">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-880">CC003</span></span></td>
<td><span data-ttu-id="58676-881">Smölun</span><span class="sxs-lookup"><span data-stu-id="58676-881">Assembly</span></span></td>
<td><span data-ttu-id="58676-882">10001</span><span class="sxs-lookup"><span data-stu-id="58676-882">10001</span></span></td>
<td><span data-ttu-id="58676-883">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-883">Electricity</span></span></td>
<td><span data-ttu-id="58676-884">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-884">Variable cost</span></span></td>
<td><span data-ttu-id="58676-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="58676-885">-5,982.83</span></span></td>
<td><span data-ttu-id="58676-886">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-887">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-887">Prod 1</span></span></td>
<td><span data-ttu-id="58676-888">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-888">Product 1</span></span></td>
<td><span data-ttu-id="58676-889">10001</span><span class="sxs-lookup"><span data-stu-id="58676-889">10001</span></span></td>
<td><span data-ttu-id="58676-890">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-890">Electricity</span></span></td>
<td><span data-ttu-id="58676-891">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-891">Variable cost</span></span></td>
<td><span data-ttu-id="58676-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="58676-892">4,487.12</span></span></td>
<td><span data-ttu-id="58676-893">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-894">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-894">Prod 2</span></span></td>
<td><span data-ttu-id="58676-895">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-895">Product 2</span></span></td>
<td><span data-ttu-id="58676-896">10001</span><span class="sxs-lookup"><span data-stu-id="58676-896">10001</span></span></td>
<td><span data-ttu-id="58676-897">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-897">Electricity</span></span></td>
<td><span data-ttu-id="58676-898">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-898">Variable cost</span></span></td>
<td><span data-ttu-id="58676-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="58676-899">1,495.71</span></span></td>
<td><span data-ttu-id="58676-900">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-901">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-901">CC003</span></span></td>
<td><span data-ttu-id="58676-902">Smölun</span><span class="sxs-lookup"><span data-stu-id="58676-902">Assembly</span></span></td>
<td><span data-ttu-id="58676-903">10001</span><span class="sxs-lookup"><span data-stu-id="58676-903">10001</span></span></td>
<td><span data-ttu-id="58676-904">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-904">Electricity</span></span></td>
<td><span data-ttu-id="58676-905">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-905">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="58676-906">-286.25</span></span></td>
<td><span data-ttu-id="58676-907">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-908">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-908">Prod 1</span></span></td>
<td><span data-ttu-id="58676-909">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-909">Product 1</span></span></td>
<td><span data-ttu-id="58676-910">10001</span><span class="sxs-lookup"><span data-stu-id="58676-910">10001</span></span></td>
<td><span data-ttu-id="58676-911">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-911">Electricity</span></span></td>
<td><span data-ttu-id="58676-912">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-912">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-913">241.05</span><span class="sxs-lookup"><span data-stu-id="58676-913">241.05</span></span></td>
<td><span data-ttu-id="58676-914">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-915">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-915">Prod 2</span></span></td>
<td><span data-ttu-id="58676-916">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-916">Product 2</span></span></td>
<td><span data-ttu-id="58676-917">10001</span><span class="sxs-lookup"><span data-stu-id="58676-917">10001</span></span></td>
<td><span data-ttu-id="58676-918">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-918">Electricity</span></span></td>
<td><span data-ttu-id="58676-919">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-919">Fixed cost</span></span></td>
<td><span data-ttu-id="58676-920">45.20</span><span class="sxs-lookup"><span data-stu-id="58676-920">45.20</span></span></td>
<td><span data-ttu-id="58676-921">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-922">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-922">CC003</span></span></td>
<td><span data-ttu-id="58676-923">Smölun</span><span class="sxs-lookup"><span data-stu-id="58676-923">Assembly</span></span></td>
<td><span data-ttu-id="58676-924">10001</span><span class="sxs-lookup"><span data-stu-id="58676-924">10001</span></span></td>
<td><span data-ttu-id="58676-925">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-925">Electricity</span></span></td>
<td><span data-ttu-id="58676-926">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-926">Variable cost</span></span></td>
<td><span data-ttu-id="58676-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="58676-927">-2,977.17</span></span></td>
<td><span data-ttu-id="58676-928">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-929">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-929">Prod 1</span></span></td>
<td><span data-ttu-id="58676-930">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-930">Product 1</span></span></td>
<td><span data-ttu-id="58676-931">10001</span><span class="sxs-lookup"><span data-stu-id="58676-931">10001</span></span></td>
<td><span data-ttu-id="58676-932">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-932">Electricity</span></span></td>
<td><span data-ttu-id="58676-933">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-933">Variable cost</span></span></td>
<td><span data-ttu-id="58676-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="58676-934">2,507.09</span></span></td>
<td><span data-ttu-id="58676-935">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="58676-936">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-936">Prod 2</span></span></td>
<td><span data-ttu-id="58676-937">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-937">Product 2</span></span></td>
<td><span data-ttu-id="58676-938">10001</span><span class="sxs-lookup"><span data-stu-id="58676-938">10001</span></span></td>
<td><span data-ttu-id="58676-939">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-939">Electricity</span></span></td>
<td><span data-ttu-id="58676-940">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-940">Variable cost</span></span></td>
<td><span data-ttu-id="58676-941">470.08</span><span class="sxs-lookup"><span data-stu-id="58676-941">470.08</span></span></td>
<td><span data-ttu-id="58676-942">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="58676-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="58676-943">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="58676-943">Conclusion</span></span>
<span data-ttu-id="58676-944">Í Fjárhagsbókhaldi er kostnaður upp á 10.000,00 fyrir rafmagn bókaður á kenni leppkostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="58676-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="58676-945">Þar af leiðandi munu kostnaðarbókarar vita að það þarf að úthluta þessum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="58676-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="58676-946">Í kostnaðarbókhaldi streymir kostnaður þvert á fyrirtækiseiningar og stig, samkvæmt þeim stefnum og reglum sem eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="58676-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="58676-947">Hver kostnaður hefur verið tengdur úthlutunargrunni sem veitir besta mat á úthlutun á kostnaði.</span><span class="sxs-lookup"><span data-stu-id="58676-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="58676-948">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="58676-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="58676-949">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="58676-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="58676-950">Samtala</span><span class="sxs-lookup"><span data-stu-id="58676-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="58676-951">CC099</span><span class="sxs-lookup"><span data-stu-id="58676-951">CC099</span></span></th>
<th><span data-ttu-id="58676-952">CC001</span><span class="sxs-lookup"><span data-stu-id="58676-952">CC001</span></span></th>
<th><span data-ttu-id="58676-953">CC002</span><span class="sxs-lookup"><span data-stu-id="58676-953">CC002</span></span></th>
<th><span data-ttu-id="58676-954">CC003</span><span class="sxs-lookup"><span data-stu-id="58676-954">CC003</span></span></th>
<th><span data-ttu-id="58676-955">CC004</span><span class="sxs-lookup"><span data-stu-id="58676-955">CC004</span></span></th>
<th><span data-ttu-id="58676-956">Verk 1</span><span class="sxs-lookup"><span data-stu-id="58676-956">Proj 1</span></span></th>
<th><span data-ttu-id="58676-957">Verk 2</span><span class="sxs-lookup"><span data-stu-id="58676-957">Proj 2</span></span></th>
<th><span data-ttu-id="58676-958">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="58676-958">Prod 1</span></span></th>
<th><span data-ttu-id="58676-959">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="58676-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="58676-960">10001 Rafmagn</span><span class="sxs-lookup"><span data-stu-id="58676-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="58676-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="58676-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="58676-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="58676-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="58676-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="58676-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="58676-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="58676-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="58676-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="58676-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="58676-970">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="58676-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-971">0,00</span><span class="sxs-lookup"><span data-stu-id="58676-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="58676-972">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-973">0,00</span><span class="sxs-lookup"><span data-stu-id="58676-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-974">0,00</span><span class="sxs-lookup"><span data-stu-id="58676-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-975">0,00</span><span class="sxs-lookup"><span data-stu-id="58676-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-976">0,00</span><span class="sxs-lookup"><span data-stu-id="58676-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-977">0,00</span><span class="sxs-lookup"><span data-stu-id="58676-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="58676-978">776.36</span><span class="sxs-lookup"><span data-stu-id="58676-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-979">223.64</span><span class="sxs-lookup"><span data-stu-id="58676-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="58676-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="58676-981">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="58676-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-982">000</span><span class="sxs-lookup"><span data-stu-id="58676-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-983">0,00</span><span class="sxs-lookup"><span data-stu-id="58676-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-984">0,00</span><span class="sxs-lookup"><span data-stu-id="58676-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-985">0,00</span><span class="sxs-lookup"><span data-stu-id="58676-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-986">0,00</span><span class="sxs-lookup"><span data-stu-id="58676-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-987">30,00</span><span class="sxs-lookup"><span data-stu-id="58676-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-988">10,00</span><span class="sxs-lookup"><span data-stu-id="58676-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="58676-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="58676-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="58676-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="58676-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="58676-992">Þetta efnisatriði sýnir hvernig fyrir aðalkostnaðareiningin 10001 Rafmagn flæðir í gegnum kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="58676-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="58676-993">Þar af leiðandi er þessum sameiginlega kostnaði úthlutað á lægsta stigið í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="58676-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="58676-994">Með öðrum orðum bera kostnaðarhlutir á lægsta stiginu kostnaðinn.</span><span class="sxs-lookup"><span data-stu-id="58676-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="58676-995">Ef þú þarft sjónrænt flæði kostnaðar á milli kostnaðarhluta er hægt að nota stefnureglur samantekins kostnaðar til að gera kostnaðarflæðið sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="58676-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="58676-996">Nánari upplýsingar er að finna í [Samantekt kostnaðar](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="58676-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



