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
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976476"
---
# <a name="overhead-calculation"></a><span data-ttu-id="85b4c-103">Útreikningur fastakostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85b4c-104">Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði.</span><span class="sxs-lookup"><span data-stu-id="85b4c-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="85b4c-105">Skýrsluskilgreining</span><span class="sxs-lookup"><span data-stu-id="85b4c-105">Term definition</span></span>
---------------

<span data-ttu-id="85b4c-106">Stjórnunarkostnaður er sá kostnaður sem stofnað er til fyrir rekstur fyrirtækis, en sem ekki er hægt að rekja beint til neinna sérstakrar starfsemi, vöru eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="85b4c-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="85b4c-107">Stjórnunarkostnaður veitir mikilvægan stuðning við myndun hagnaðarmyndandi verkþátta.</span><span class="sxs-lookup"><span data-stu-id="85b4c-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="85b4c-108">Hér eru nokkur dæmi um skilyrði:</span><span class="sxs-lookup"><span data-stu-id="85b4c-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="85b4c-109">Leiga</span><span class="sxs-lookup"><span data-stu-id="85b4c-109">Rent</span></span>
-   <span data-ttu-id="85b4c-110">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-110">Electricity</span></span>
-   <span data-ttu-id="85b4c-111">Stjórnunarkostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="85b4c-112">Yfirlit yfir útreikning fastakostnaðar</span><span class="sxs-lookup"><span data-stu-id="85b4c-112">Overhead calculation overview</span></span>
<span data-ttu-id="85b4c-113">Útreikningur fastakostnaðar keyrir reglur kostnaðarbókhalds í réttri röð.</span><span class="sxs-lookup"><span data-stu-id="85b4c-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="85b4c-114">Hægt er að keyra útreikning fastakostnaðar margsinnis fyrir sama fjárhagstímabil ef reglum kostnaðarbókhalds hefur verið breytt eða ákveðnar villur hafa fundist.</span><span class="sxs-lookup"><span data-stu-id="85b4c-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="85b4c-115">Hver keyrsla á útreikningi fastakostnaðar er geymd og fær einkvæmt útgáfukenni sem gerir kleift að bera saman útreikning í mismunandi útgáfum.</span><span class="sxs-lookup"><span data-stu-id="85b4c-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="85b4c-116">Kostnaðarfærslur sem útreikningur fastakostnaðar mynda fá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="85b4c-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="85b4c-117">Dagsetningin bókhald samsvarar lokadagsetning fjárhagstímabilsins sem er dagsetning reikningsskiladagsetning reikningsskila notað í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="85b4c-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="85b4c-118">Einkvæmt útgáfukenni samanstendur af eftirfarandi þáttum:</span><span class="sxs-lookup"><span data-stu-id="85b4c-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="85b4c-119">Gerð útgáfu</span><span class="sxs-lookup"><span data-stu-id="85b4c-119">Version type</span></span>
-   <span data-ttu-id="85b4c-120">Dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="85b4c-120">Date and time</span></span>
-   <span data-ttu-id="85b4c-121">Fjárhagur kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="85b4c-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="85b4c-122">Fjárhagsár</span><span class="sxs-lookup"><span data-stu-id="85b4c-122">Fiscal year</span></span>
-   <span data-ttu-id="85b4c-123">Reikningstímabil</span><span class="sxs-lookup"><span data-stu-id="85b4c-123">Fiscal period</span></span>

<span data-ttu-id="85b4c-124">Útreikningur fastakostnaðar er keyrður óháð því hver útgáfan er.</span><span class="sxs-lookup"><span data-stu-id="85b4c-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="85b4c-125">Þess vegna er hægt að reikna út áætlaða útgáfu á undan raunútgáfu.</span><span class="sxs-lookup"><span data-stu-id="85b4c-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="85b4c-126">Útreikningur fastakostnaðar samanstendur af fjórum skrefum, eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="85b4c-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="85b4c-127">Í hverju skrefi er færslubókarhaus stofnaður með bókarfærslum.</span><span class="sxs-lookup"><span data-stu-id="85b4c-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="85b4c-128">Þessi færslubókarhaus geymir inntaksgögn fyrir hvert útreikningsþrep.</span><span class="sxs-lookup"><span data-stu-id="85b4c-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="85b4c-129">Stefnur og reglur eru notaðar í hverri færslulínu og kostnaðarfærslur eru myndaðar sem úttak.</span><span class="sxs-lookup"><span data-stu-id="85b4c-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="85b4c-130">Þess vegna hefurðu ávallt fullan rekjanleika.</span><span class="sxs-lookup"><span data-stu-id="85b4c-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="85b4c-131">[![Útreikningur fastakostnaðar](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="85b4c-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="85b4c-132">Reikna og úthluta sameiginlegur kostnaði vegna rafmagns</span><span class="sxs-lookup"><span data-stu-id="85b4c-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="85b4c-133">Í Fjárhagsbókhaldi er ákveðinn kostnaður, eins og rafmagn, skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="85b4c-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="85b4c-134">Þar af leiðandi er nákvæmar innsýn rekstrarfélags ekki veitt fyrir kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="85b4c-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="85b4c-135">Í kostnaðarbókhaldi verður kostnaður að flæða í gegnum fyrirtækiseiningar til að veita rétta innsýn rekstrarfélags þvert á allar fyrirtækiseiningar og stig.</span><span class="sxs-lookup"><span data-stu-id="85b4c-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="85b4c-136">Þetta flæði verður að byggja á annaðhvort nákvæmri færslu notkunar eða sanngjarnri matsreglu.</span><span class="sxs-lookup"><span data-stu-id="85b4c-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="85b4c-137">Í fjárhagnum er hægt að bóka rafmagnskostnað eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="85b4c-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="85b4c-138">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="85b4c-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="85b4c-139">Kostnaðarstaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="85b4c-140">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="85b4c-140">Main account</span></span></th>
<th><span data-ttu-id="85b4c-141">Upphæð í bókhaldsgjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="85b4c-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-142">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="85b4c-143">CC099</span><span class="sxs-lookup"><span data-stu-id="85b4c-143">CC099</span></span></td>
<td><span data-ttu-id="85b4c-144">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="85b4c-144">Default cost center</span></span></td>
<td><span data-ttu-id="85b4c-145">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-145">10001</span></span></td>
<td><span data-ttu-id="85b4c-146">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-146">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="85b4c-148">Skref 1: Keyra útreikning kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="85b4c-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="85b4c-149">Sjálfvirkt er að þegar kostnaðarfærslur eru fluttar úr grunngögnum fái þær flokkun kostnaðarhegðunar **Óflokkað** í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="85b4c-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="85b4c-150">Með því að nota stefnureglur kostnaðarhegðunar er hægt að endurflokka kostnaðarfærslur sem annaðhvort **Fastan kostnað** eða **Breytilegan kostnað**.</span><span class="sxs-lookup"><span data-stu-id="85b4c-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="85b4c-151">Tilgreinið reglu kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="85b4c-151">Define the cost behavior rule</span></span>

<span data-ttu-id="85b4c-152">Í sumum tilfellum er hluti af kostnaði föst þóknun og eftirstandandi kostnaður byggist á notkun.</span><span class="sxs-lookup"><span data-stu-id="85b4c-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="85b4c-153">Rafmagnsreikningar stemma oft við þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="85b4c-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="85b4c-154">Þegar tiltekin föst þóknun hefur verið greidd, er greitt fyrir notkun á kílóvattklukkustund (Kwh).</span><span class="sxs-lookup"><span data-stu-id="85b4c-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="85b4c-155">Til dæmis ef föst kostnaðarþóknun er 1000.00 sýnir þetta hvernig regla kostnaðarhegðunar er skilgreind:</span><span class="sxs-lookup"><span data-stu-id="85b4c-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="85b4c-156">Föst upphæð 1.000,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="85b4c-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="85b4c-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="85b4c-158">1000.01 &lt; N = Breyta</span><span class="sxs-lookup"><span data-stu-id="85b4c-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="85b4c-159">Færslubók</span><span class="sxs-lookup"><span data-stu-id="85b4c-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="85b4c-160">Færslubók</span><span class="sxs-lookup"><span data-stu-id="85b4c-160">Journal</span></span></th>
<th><span data-ttu-id="85b4c-161">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="85b4c-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="85b4c-162">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="85b4c-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="85b4c-163">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="85b4c-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-164">00001</span><span class="sxs-lookup"><span data-stu-id="85b4c-164">00001</span></span></td>
<td><span data-ttu-id="85b4c-165">Færslubók útreiknings fyrir kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="85b4c-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="85b4c-166">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="85b4c-166">Fiscal</span></span></td>
<td><span data-ttu-id="85b4c-167">2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-167">2017</span></span></td>
<td><span data-ttu-id="85b4c-168">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="85b4c-168">Period 1</span></span></td>
<td><span data-ttu-id="85b4c-169">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="85b4c-170">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="85b4c-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="85b4c-171">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="85b4c-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="85b4c-172">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="85b4c-173">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="85b4c-173">Cost element</span></span></th>
<th><span data-ttu-id="85b4c-174">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="85b4c-174">Cost behavior</span></span></th>
<th><span data-ttu-id="85b4c-175">Upphæð</span><span class="sxs-lookup"><span data-stu-id="85b4c-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-176">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="85b4c-177">CC099</span><span class="sxs-lookup"><span data-stu-id="85b4c-177">CC099</span></span></td>
<td><span data-ttu-id="85b4c-178">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="85b4c-178">Default cost center</span></span></td>
<td><span data-ttu-id="85b4c-179">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-179">10001</span></span></td>
<td><span data-ttu-id="85b4c-180">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-180">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-181">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="85b4c-181">Unclassified</span></span></td>
<td><span data-ttu-id="85b4c-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="85b4c-183">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="85b4c-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="85b4c-184">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="85b4c-185">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="85b4c-185">Cost element</span></span></th>
<th><span data-ttu-id="85b4c-186">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="85b4c-186">Cost behavior</span></span></th>
<th><span data-ttu-id="85b4c-187">Upphæð</span><span class="sxs-lookup"><span data-stu-id="85b4c-187">Amount</span></span></th>
<th><span data-ttu-id="85b4c-188">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="85b4c-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-189">CC099</span><span class="sxs-lookup"><span data-stu-id="85b4c-189">CC099</span></span></td>
<td><span data-ttu-id="85b4c-190">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="85b4c-190">Default cost center</span></span></td>
<td><span data-ttu-id="85b4c-191">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-191">10001</span></span></td>
<td><span data-ttu-id="85b4c-192">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-192">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-193">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="85b4c-193">Unclassified</span></span></td>
<td><span data-ttu-id="85b4c-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-194">10,000.00</span></span></td>
<td><span data-ttu-id="85b4c-195">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-196">CC099</span><span class="sxs-lookup"><span data-stu-id="85b4c-196">CC099</span></span></td>
<td><span data-ttu-id="85b4c-197">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="85b4c-197">Default cost center</span></span></td>
<td><span data-ttu-id="85b4c-198">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-198">10001</span></span></td>
<td><span data-ttu-id="85b4c-199">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-199">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-200">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="85b4c-200">Unclassified</span></span></td>
<td><span data-ttu-id="85b4c-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-201">-10,000.00</span></span></td>
<td><span data-ttu-id="85b4c-202">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-203">CC099</span><span class="sxs-lookup"><span data-stu-id="85b4c-203">CC099</span></span></td>
<td><span data-ttu-id="85b4c-204">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="85b4c-204">Default cost center</span></span></td>
<td><span data-ttu-id="85b4c-205">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-205">10001</span></span></td>
<td><span data-ttu-id="85b4c-206">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-206">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-207">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-207">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-208">1,000.00</span></span></td>
<td><span data-ttu-id="85b4c-209">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-210">CC099</span><span class="sxs-lookup"><span data-stu-id="85b4c-210">CC099</span></span></td>
<td><span data-ttu-id="85b4c-211">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="85b4c-211">Default cost center</span></span></td>
<td><span data-ttu-id="85b4c-212">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-212">10001</span></span></td>
<td><span data-ttu-id="85b4c-213">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-213">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-214">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-214">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="85b4c-215">9,000.00</span></span></td>
<td><span data-ttu-id="85b4c-216">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="85b4c-217">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðarhegðunarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="85b4c-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="85b4c-218">Skref 2: Keyra útreikning kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="85b4c-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="85b4c-219">Kostnaðardreifing er notuð til að endurúthluta kostnaði frá einum kostnaðarhlut til annars eða fleiri kostnaðarhluta með því að nota viðeigandi úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="85b4c-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="85b4c-220">Kostnaðardreifing og kostnaðarúthlutun eru ólíkar að því leyti að kostnaðardreifing kemur alltaf upp á stigi aðalkostnaðareiningar upphaflegs verðs.</span><span class="sxs-lookup"><span data-stu-id="85b4c-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="85b4c-221">Tilgreinið kostnaðardreifingarreglu</span><span class="sxs-lookup"><span data-stu-id="85b4c-221">Define the cost distribution rule</span></span>

<span data-ttu-id="85b4c-222">Í Fjárhagsbókhaldi er rafmagnskostnaður oft skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="85b4c-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="85b4c-223">Í kostnaðarbókhaldi er þessi nálgun ekki nógu nákvæm.</span><span class="sxs-lookup"><span data-stu-id="85b4c-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="85b4c-224">Breytilegur kostnaði þarf að dreifa á staka kostnaðarhluti á sanngjörnum grunni.</span><span class="sxs-lookup"><span data-stu-id="85b4c-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="85b4c-225">Rökréttasti úthlutunargrunnurinn er notkun á rafmagni (Kwh).</span><span class="sxs-lookup"><span data-stu-id="85b4c-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="85b4c-226">Stofnað er tölfræðilegt víddarstak sem er nefnt Rafmagn og rafmagnsnotkun er skráð.</span><span class="sxs-lookup"><span data-stu-id="85b4c-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="85b4c-227">Sjálfgefið er að öll tölfræðileg víddarstök verða tiltæk sem úthlutunargrunnur.</span><span class="sxs-lookup"><span data-stu-id="85b4c-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="85b4c-228">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-228">Cost object</span></span></th>
<th><span data-ttu-id="85b4c-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="85b4c-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-230">CC001</span><span class="sxs-lookup"><span data-stu-id="85b4c-230">CC001</span></span></td>
<td><span data-ttu-id="85b4c-231">Mannauður</span><span class="sxs-lookup"><span data-stu-id="85b4c-231">HR</span></span></td>
<td><span data-ttu-id="85b4c-232">1.000</span><span class="sxs-lookup"><span data-stu-id="85b4c-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-233">CC002</span><span class="sxs-lookup"><span data-stu-id="85b4c-233">CC002</span></span></td>
<td><span data-ttu-id="85b4c-234">Fjármál</span><span class="sxs-lookup"><span data-stu-id="85b4c-234">Finance</span></span></td>
<td><span data-ttu-id="85b4c-235">6,000</span><span class="sxs-lookup"><span data-stu-id="85b4c-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-236">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-236">CC003</span></span></td>
<td><span data-ttu-id="85b4c-237">Smölun</span><span class="sxs-lookup"><span data-stu-id="85b4c-237">Assembly</span></span></td>
<td><span data-ttu-id="85b4c-238">0</span><span class="sxs-lookup"><span data-stu-id="85b4c-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="85b4c-239">Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunni fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="85b4c-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="85b4c-240">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-240">Cost object</span></span></th>
<th><span data-ttu-id="85b4c-241">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="85b4c-241">Magnitude</span></span></th>
<th><span data-ttu-id="85b4c-242">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="85b4c-242">Allocation factor</span></span></th>
<th><span data-ttu-id="85b4c-243">Upphæð</span><span class="sxs-lookup"><span data-stu-id="85b4c-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-244">CC001</span><span class="sxs-lookup"><span data-stu-id="85b4c-244">CC001</span></span></td>
<td><span data-ttu-id="85b4c-245">Mannauður</span><span class="sxs-lookup"><span data-stu-id="85b4c-245">HR</span></span></td>
<td><span data-ttu-id="85b4c-246">1.000</span><span class="sxs-lookup"><span data-stu-id="85b4c-246">1,000</span></span></td>
<td><span data-ttu-id="85b4c-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="85b4c-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="85b4c-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-249">CC002</span><span class="sxs-lookup"><span data-stu-id="85b4c-249">CC002</span></span></td>
<td><span data-ttu-id="85b4c-250">Fjármál</span><span class="sxs-lookup"><span data-stu-id="85b4c-250">Finance</span></span></td>
<td><span data-ttu-id="85b4c-251">6,000</span><span class="sxs-lookup"><span data-stu-id="85b4c-251">6,000</span></span></td>
<td><span data-ttu-id="85b4c-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="85b4c-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="85b4c-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-254">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-254">CC003</span></span></td>
<td><span data-ttu-id="85b4c-255">Smölun</span><span class="sxs-lookup"><span data-stu-id="85b4c-255">Assembly</span></span></td>
<td><span data-ttu-id="85b4c-256">0</span><span class="sxs-lookup"><span data-stu-id="85b4c-256">0</span></span></td>
<td><span data-ttu-id="85b4c-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="85b4c-258">0,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="85b4c-259">Föstum kostnaði þarf að dreifa jafnt á staka kostnaðarhluti sem hafa notað rafmagn.</span><span class="sxs-lookup"><span data-stu-id="85b4c-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="85b4c-260">Hægt er að ná þessa niðurstöðu með því að nota tölfræðilegt víddarstakið Rafmagn í úthlutunargrunni reikniformúlu: (Rafmagn &gt; 0,00) Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunn fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="85b4c-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="85b4c-261">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-261">Cost object</span></span></th>
<th><span data-ttu-id="85b4c-262">Formúla</span><span class="sxs-lookup"><span data-stu-id="85b4c-262">Formula</span></span></th>
<th><span data-ttu-id="85b4c-263">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="85b4c-263">Magnitude</span></span></th>
<th><span data-ttu-id="85b4c-264">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="85b4c-264">Allocation factor</span></span></th>
<th><span data-ttu-id="85b4c-265">Upphæð</span><span class="sxs-lookup"><span data-stu-id="85b4c-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-266">CC001</span><span class="sxs-lookup"><span data-stu-id="85b4c-266">CC001</span></span></td>
<td><span data-ttu-id="85b4c-267">Mannauður</span><span class="sxs-lookup"><span data-stu-id="85b4c-267">HR</span></span></td>
<td><span data-ttu-id="85b4c-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="85b4c-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="85b4c-269">1</span><span class="sxs-lookup"><span data-stu-id="85b4c-269">1</span></span></td>
<td><span data-ttu-id="85b4c-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="85b4c-271">500,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-272">CC002</span><span class="sxs-lookup"><span data-stu-id="85b4c-272">CC002</span></span></td>
<td><span data-ttu-id="85b4c-273">Fjármál</span><span class="sxs-lookup"><span data-stu-id="85b4c-273">Finance</span></span></td>
<td><span data-ttu-id="85b4c-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="85b4c-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="85b4c-275">1</span><span class="sxs-lookup"><span data-stu-id="85b4c-275">1</span></span></td>
<td><span data-ttu-id="85b4c-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="85b4c-277">500,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-278">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-278">CC003</span></span></td>
<td><span data-ttu-id="85b4c-279">Smölun</span><span class="sxs-lookup"><span data-stu-id="85b4c-279">Assembly</span></span></td>
<td><span data-ttu-id="85b4c-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="85b4c-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="85b4c-281">0</span><span class="sxs-lookup"><span data-stu-id="85b4c-281">0</span></span></td>
<td><span data-ttu-id="85b4c-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="85b4c-283">0,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="85b4c-284">Færslubók</span><span class="sxs-lookup"><span data-stu-id="85b4c-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="85b4c-285">Færslubók</span><span class="sxs-lookup"><span data-stu-id="85b4c-285">Journal</span></span></th>
<th><span data-ttu-id="85b4c-286">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="85b4c-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="85b4c-287">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="85b4c-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="85b4c-288">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="85b4c-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-289">00002</span><span class="sxs-lookup"><span data-stu-id="85b4c-289">00002</span></span></td>
<td><span data-ttu-id="85b4c-290">Útreikningabók kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="85b4c-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="85b4c-291">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="85b4c-291">Fiscal</span></span></td>
<td><span data-ttu-id="85b4c-292">2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-292">2017</span></span></td>
<td><span data-ttu-id="85b4c-293">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="85b4c-293">Period 1</span></span></td>
<td><span data-ttu-id="85b4c-294">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="85b4c-295">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="85b4c-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="85b4c-296">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="85b4c-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="85b4c-297">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="85b4c-298">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="85b4c-298">Cost element</span></span></th>
<th><span data-ttu-id="85b4c-299">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="85b4c-299">Cost behavior</span></span></th>
<th><span data-ttu-id="85b4c-300">Upphæð</span><span class="sxs-lookup"><span data-stu-id="85b4c-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-301">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="85b4c-302">CC099</span><span class="sxs-lookup"><span data-stu-id="85b4c-302">CC099</span></span></td>
<td><span data-ttu-id="85b4c-303">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="85b4c-303">Default cost center</span></span></td>
<td><span data-ttu-id="85b4c-304">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-304">10001</span></span></td>
<td><span data-ttu-id="85b4c-305">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-305">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-306">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-306">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-308">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="85b4c-309">CC099</span><span class="sxs-lookup"><span data-stu-id="85b4c-309">CC099</span></span></td>
<td><span data-ttu-id="85b4c-310">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="85b4c-310">Default cost center</span></span></td>
<td><span data-ttu-id="85b4c-311">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-311">10001</span></span></td>
<td><span data-ttu-id="85b4c-312">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-312">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-313">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-313">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="85b4c-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="85b4c-315">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="85b4c-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="85b4c-316">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="85b4c-317">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="85b4c-317">Cost element</span></span></th>
<th><span data-ttu-id="85b4c-318">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="85b4c-318">Cost behavior</span></span></th>
<th><span data-ttu-id="85b4c-319">Upphæð</span><span class="sxs-lookup"><span data-stu-id="85b4c-319">Amount</span></span></th>
<th><span data-ttu-id="85b4c-320">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="85b4c-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-321">CC099</span><span class="sxs-lookup"><span data-stu-id="85b4c-321">CC099</span></span></td>
<td><span data-ttu-id="85b4c-322">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="85b4c-322">Default cost center</span></span></td>
<td><span data-ttu-id="85b4c-323">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-323">10001</span></span></td>
<td><span data-ttu-id="85b4c-324">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-324">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-325">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-325">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-326">-1,000.00</span></span></td>
<td><span data-ttu-id="85b4c-327">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-328">CC001</span><span class="sxs-lookup"><span data-stu-id="85b4c-328">CC001</span></span></td>
<td><span data-ttu-id="85b4c-329">Mannauður</span><span class="sxs-lookup"><span data-stu-id="85b4c-329">HR</span></span></td>
<td><span data-ttu-id="85b4c-330">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-330">10001</span></span></td>
<td><span data-ttu-id="85b4c-331">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-331">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-332">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-332">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-333">500,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-333">500.00</span></span></td>
<td><span data-ttu-id="85b4c-334">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-335">CC002</span><span class="sxs-lookup"><span data-stu-id="85b4c-335">CC002</span></span></td>
<td><span data-ttu-id="85b4c-336">Fjármál</span><span class="sxs-lookup"><span data-stu-id="85b4c-336">Finance</span></span></td>
<td><span data-ttu-id="85b4c-337">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-337">10001</span></span></td>
<td><span data-ttu-id="85b4c-338">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-338">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-339">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-339">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-340">500,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-340">500.00</span></span></td>
<td><span data-ttu-id="85b4c-341">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-342">CC099</span><span class="sxs-lookup"><span data-stu-id="85b4c-342">CC099</span></span></td>
<td><span data-ttu-id="85b4c-343">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="85b4c-343">Default cost center</span></span></td>
<td><span data-ttu-id="85b4c-344">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-344">10001</span></span></td>
<td><span data-ttu-id="85b4c-345">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-345">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-346">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-346">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-347">-9,000.00</span></span></td>
<td><span data-ttu-id="85b4c-348">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-349">CC001</span><span class="sxs-lookup"><span data-stu-id="85b4c-349">CC001</span></span></td>
<td><span data-ttu-id="85b4c-350">Mannauður</span><span class="sxs-lookup"><span data-stu-id="85b4c-350">HR</span></span></td>
<td><span data-ttu-id="85b4c-351">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-351">10001</span></span></td>
<td><span data-ttu-id="85b4c-352">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-352">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-353">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-353">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="85b4c-354">1,285.71</span></span></td>
<td><span data-ttu-id="85b4c-355">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-356">CC002</span><span class="sxs-lookup"><span data-stu-id="85b4c-356">CC002</span></span></td>
<td><span data-ttu-id="85b4c-357">Fjármál</span><span class="sxs-lookup"><span data-stu-id="85b4c-357">Finance</span></span></td>
<td><span data-ttu-id="85b4c-358">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-358">10001</span></span></td>
<td><span data-ttu-id="85b4c-359">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-359">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-360">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-360">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="85b4c-361">7,714.29</span></span></td>
<td><span data-ttu-id="85b4c-362">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="85b4c-363">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðardreifingarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="85b4c-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="85b4c-364">Skref 3: Keyra útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="85b4c-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="85b4c-365">Sameiginlegur kostnaður er notaður til að rukka einn eða fleiri tilgreinda kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="85b4c-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="85b4c-366">Gjöldin byggjast á fyrirframákveðnu kostnaðarhlutfalli og mæligildi úr úthlutuðum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="85b4c-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="85b4c-367">Skilgreina sameiginlegan kostnað</span><span class="sxs-lookup"><span data-stu-id="85b4c-367">Define the overhead rate</span></span>

<span data-ttu-id="85b4c-368">Kostnaðarhlutur CC001 Mannauður stuðlar að safni innri verka.</span><span class="sxs-lookup"><span data-stu-id="85b4c-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="85b4c-369">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsverk til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="85b4c-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="85b4c-370">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-370">Cost object</span></span></th>
<th><span data-ttu-id="85b4c-371">Tímar</span><span class="sxs-lookup"><span data-stu-id="85b4c-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-372">Verk 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-372">Proj 1</span></span></td>
<td><span data-ttu-id="85b4c-373">Verk 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-373">Project 1</span></span></td>
<td><span data-ttu-id="85b4c-374">3</span><span class="sxs-lookup"><span data-stu-id="85b4c-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-375">Verk 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-375">Proj 2</span></span></td>
<td><span data-ttu-id="85b4c-376">Verk 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-376">Project 2</span></span></td>
<td><span data-ttu-id="85b4c-377">1</span><span class="sxs-lookup"><span data-stu-id="85b4c-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="85b4c-378">Fyrirframákveðið kostnaðarhlutfall fyrir kostnaðarframlag verk hefur verið skilgreint.</span><span class="sxs-lookup"><span data-stu-id="85b4c-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="85b4c-379">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-379">Cost object</span></span></th>
<th><span data-ttu-id="85b4c-380">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="85b4c-380">Cost element</span></span></th>
<th><span data-ttu-id="85b4c-381">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="85b4c-381">Cost behavior</span></span></th>
<th><span data-ttu-id="85b4c-382">Einingar</span><span class="sxs-lookup"><span data-stu-id="85b4c-382">Units</span></span></th>
<th><span data-ttu-id="85b4c-383">Taxti</span><span class="sxs-lookup"><span data-stu-id="85b4c-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-384">CC001</span><span class="sxs-lookup"><span data-stu-id="85b4c-384">CC001</span></span></td>
<td><span data-ttu-id="85b4c-385">Mannauður</span><span class="sxs-lookup"><span data-stu-id="85b4c-385">HR</span></span></td>
<td><span data-ttu-id="85b4c-386">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-386">10001</span></span></td>
<td><span data-ttu-id="85b4c-387">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-387">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-388">1</span><span class="sxs-lookup"><span data-stu-id="85b4c-388">1</span></span></td>
<td><span data-ttu-id="85b4c-389">10</span><span class="sxs-lookup"><span data-stu-id="85b4c-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="85b4c-390">Eftirfarandi tafla sýnir niðurstöður þegar Mannauðsverk eru notuð sem grunnur við úthlutun.</span><span class="sxs-lookup"><span data-stu-id="85b4c-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="85b4c-391">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-391">Cost object</span></span></th>
<th><span data-ttu-id="85b4c-392">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="85b4c-392">Magnitude</span></span></th>
<th><span data-ttu-id="85b4c-393">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="85b4c-393">Cost element</span></span></th>
<th><span data-ttu-id="85b4c-394">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="85b4c-394">Allocation factor</span></span></th>
<th><span data-ttu-id="85b4c-395">Upphæð</span><span class="sxs-lookup"><span data-stu-id="85b4c-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-396">Verk 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-396">Proj 1</span></span></td>
<td><span data-ttu-id="85b4c-397">Verk 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-397">Project 1</span></span></td>
<td><span data-ttu-id="85b4c-398">3</span><span class="sxs-lookup"><span data-stu-id="85b4c-398">3</span></span></td>
<td><span data-ttu-id="85b4c-399">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-399">10001</span></span></td>
<td><span data-ttu-id="85b4c-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="85b4c-401">30,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-402">Verk 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-402">Proj 2</span></span></td>
<td><span data-ttu-id="85b4c-403">Verk 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-403">Project 2</span></span></td>
<td><span data-ttu-id="85b4c-404">1</span><span class="sxs-lookup"><span data-stu-id="85b4c-404">1</span></span></td>
<td><span data-ttu-id="85b4c-405">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-405">10001</span></span></td>
<td><span data-ttu-id="85b4c-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="85b4c-407">10,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="85b4c-408">Færslubók</span><span class="sxs-lookup"><span data-stu-id="85b4c-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="85b4c-409">Færslubók</span><span class="sxs-lookup"><span data-stu-id="85b4c-409">Journal</span></span></th>
<th><span data-ttu-id="85b4c-410">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="85b4c-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="85b4c-411">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="85b4c-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="85b4c-412">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="85b4c-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-413">00003</span><span class="sxs-lookup"><span data-stu-id="85b4c-413">00003</span></span></td>
<td><span data-ttu-id="85b4c-414">Færslubók fyrir útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="85b4c-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="85b4c-415">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="85b4c-415">Fiscal</span></span></td>
<td><span data-ttu-id="85b4c-416">2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-416">2017</span></span></td>
<td><span data-ttu-id="85b4c-417">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="85b4c-417">Period 1</span></span></td>
<td><span data-ttu-id="85b4c-418">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="85b4c-419">Bókarfærslur (Bókarfærslur fyrir útreikning sameiginlegs kostnaðar)</span><span class="sxs-lookup"><span data-stu-id="85b4c-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="85b4c-420">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="85b4c-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="85b4c-421">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-421">Cost object</span></span></th>
<th><span data-ttu-id="85b4c-422">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="85b4c-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-423">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="85b4c-424">Verk 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-424">Proj 1</span></span></td>
<td><span data-ttu-id="85b4c-425">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="85b4c-426">3,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-427">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="85b4c-428">Verk 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-428">Proj 2</span></span></td>
<td><span data-ttu-id="85b4c-429">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="85b4c-430">1,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="85b4c-431">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="85b4c-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="85b4c-432">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="85b4c-433">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="85b4c-433">Cost element</span></span></th>
<th><span data-ttu-id="85b4c-434">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="85b4c-434">Cost behavior</span></span></th>
<th><span data-ttu-id="85b4c-435">Upphæð</span><span class="sxs-lookup"><span data-stu-id="85b4c-435">Amount</span></span></th>
<th><span data-ttu-id="85b4c-436">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="85b4c-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="85b4c-437">CC0001</span></span></td>
<td><span data-ttu-id="85b4c-438">Mannauður</span><span class="sxs-lookup"><span data-stu-id="85b4c-438">HR</span></span></td>
<td><span data-ttu-id="85b4c-439">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-439">10001</span></span></td>
<td><span data-ttu-id="85b4c-440">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-440">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-441">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-441">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-442">-30.00</span></span></td>
<td><span data-ttu-id="85b4c-443">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-444">Verk 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-444">Proj 1</span></span></td>
<td><span data-ttu-id="85b4c-445">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="85b4c-446">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-446">10001</span></span></td>
<td><span data-ttu-id="85b4c-447">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-447">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-448">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-448">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-449">30,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-449">30.00</span></span></td>
<td><span data-ttu-id="85b4c-450">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-451">CC001</span><span class="sxs-lookup"><span data-stu-id="85b4c-451">CC001</span></span></td>
<td><span data-ttu-id="85b4c-452">Mannauður</span><span class="sxs-lookup"><span data-stu-id="85b4c-452">HR</span></span></td>
<td><span data-ttu-id="85b4c-453">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-453">10001</span></span></td>
<td><span data-ttu-id="85b4c-454">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-454">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-455">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-455">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-456">-10.00</span></span></td>
<td><span data-ttu-id="85b4c-457">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-458">Verk 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-458">Proj 2</span></span></td>
<td><span data-ttu-id="85b4c-459">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="85b4c-460">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-460">10001</span></span></td>
<td><span data-ttu-id="85b4c-461">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-461">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-462">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-462">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-463">10,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-463">10.00</span></span></td>
<td><span data-ttu-id="85b4c-464">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="85b4c-465">Nánari upplýsingar er að finna í [Framkvæma útreikning fastakostnaðar](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="85b4c-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="85b4c-466">Skref 4: Keyra útreikning kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="85b4c-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="85b4c-467">Úthlutun er notuð til að úthluta stöðu kostnaðarhlutar í öðrum kostnaðarhlutum með því að nota úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="85b4c-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="85b4c-468">Finance styður gagnvirka úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="85b4c-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="85b4c-469">Í gagnvirkri úthlutunaraðferð er sú sameiginlega þjónusta sem hjálparkostnaðarhlutir skiptast á viðurkennd að fullu.</span><span class="sxs-lookup"><span data-stu-id="85b4c-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="85b4c-470">Kerfið ákvarðar sjálfkrafa rétta röð til að framkvæma úthlutun eftir.</span><span class="sxs-lookup"><span data-stu-id="85b4c-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="85b4c-471">Stöðu kostnaðarhluta er úthlutað með einum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="85b4c-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="85b4c-472">Úthlutanir þvert á víddir kostnaðarhluta og viðkomandi stök þeirra eru studdar.</span><span class="sxs-lookup"><span data-stu-id="85b4c-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="85b4c-473">Úthlutun pöntunarinnar er stjórnað af stýrieiningu kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="85b4c-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="85b4c-474">[![Gagnkvæm aðferð](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="85b4c-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="85b4c-475">Tilgreinið kostnaðarúthlutun</span><span class="sxs-lookup"><span data-stu-id="85b4c-475">Define the cost allocation</span></span>

<span data-ttu-id="85b4c-476">Hér er einfalt dæmi sem útskýrir hvernig hægt er að rekja flæði kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="85b4c-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="85b4c-477">Kostnaðarhlutir CC001 Mannauður leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="85b4c-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="85b4c-478">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="85b4c-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="85b4c-479">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-479">Cost object</span></span></th>
<th><span data-ttu-id="85b4c-480">Mannauðsþjónusta</span><span class="sxs-lookup"><span data-stu-id="85b4c-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-481">CC002</span><span class="sxs-lookup"><span data-stu-id="85b4c-481">CC002</span></span></td>
<td><span data-ttu-id="85b4c-482">Fjármál</span><span class="sxs-lookup"><span data-stu-id="85b4c-482">Finance</span></span></td>
<td><span data-ttu-id="85b4c-483">35</span><span class="sxs-lookup"><span data-stu-id="85b4c-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-484">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-484">CC003</span></span></td>
<td><span data-ttu-id="85b4c-485">Smölun</span><span class="sxs-lookup"><span data-stu-id="85b4c-485">Assembly</span></span></td>
<td><span data-ttu-id="85b4c-486">55</span><span class="sxs-lookup"><span data-stu-id="85b4c-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-487">CC004</span><span class="sxs-lookup"><span data-stu-id="85b4c-487">CC004</span></span></td>
<td><span data-ttu-id="85b4c-488">Pakkning</span><span class="sxs-lookup"><span data-stu-id="85b4c-488">Packaging</span></span></td>
<td><span data-ttu-id="85b4c-489">10</span><span class="sxs-lookup"><span data-stu-id="85b4c-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="85b4c-490">Kostnaðarhlutir CC002 Fjármál leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="85b4c-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="85b4c-491">Stofnað er tölfræðilegt víddarstak sem kallast Fjármálaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="85b4c-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="85b4c-492">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-492">Cost object</span></span></th>
<th><span data-ttu-id="85b4c-493">Fjármálaþjónusta</span><span class="sxs-lookup"><span data-stu-id="85b4c-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-494">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-494">CC003</span></span></td>
<td><span data-ttu-id="85b4c-495">Smölun</span><span class="sxs-lookup"><span data-stu-id="85b4c-495">Assembly</span></span></td>
<td><span data-ttu-id="85b4c-496">65</span><span class="sxs-lookup"><span data-stu-id="85b4c-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-497">CC004</span><span class="sxs-lookup"><span data-stu-id="85b4c-497">CC004</span></span></td>
<td><span data-ttu-id="85b4c-498">Pakkning</span><span class="sxs-lookup"><span data-stu-id="85b4c-498">Packaging</span></span></td>
<td><span data-ttu-id="85b4c-499">35</span><span class="sxs-lookup"><span data-stu-id="85b4c-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="85b4c-500">Kostnaðarhlutir CC003 Samsetning leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="85b4c-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="85b4c-501">Meðlimur tölfræðilega víddar sem kallast Mannauður verk er stofnað til að mælvíddarstaka notuðum magnitude.</span><span class="sxs-lookup"><span data-stu-id="85b4c-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="85b4c-502">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-502">Cost object</span></span></th>
<th><span data-ttu-id="85b4c-503">Samsetningarþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="85b4c-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-504">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-504">Prod 1</span></span></td>
<td><span data-ttu-id="85b4c-505">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-505">Product 1</span></span></td>
<td><span data-ttu-id="85b4c-506">60</span><span class="sxs-lookup"><span data-stu-id="85b4c-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-507">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-507">Prod 2</span></span></td>
<td><span data-ttu-id="85b4c-508">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-508">Product 2</span></span></td>
<td><span data-ttu-id="85b4c-509">20</span><span class="sxs-lookup"><span data-stu-id="85b4c-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="85b4c-510">Kostnaðarhlutir CC004 Umbúðir leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="85b4c-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="85b4c-511">Stofnað er tölfræðilegt víddarstak sem kallast Umbúðaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="85b4c-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="85b4c-512">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-512">Cost object</span></span></th>
<th><span data-ttu-id="85b4c-513">Umbúðaþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="85b4c-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-514">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-514">Prod 1</span></span></td>
<td><span data-ttu-id="85b4c-515">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-515">Product 1</span></span></td>
<td><span data-ttu-id="85b4c-516">80</span><span class="sxs-lookup"><span data-stu-id="85b4c-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-517">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-517">Prod 2</span></span></td>
<td><span data-ttu-id="85b4c-518">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-518">Product 2</span></span></td>
<td><span data-ttu-id="85b4c-519">15</span><span class="sxs-lookup"><span data-stu-id="85b4c-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="85b4c-520">Hægt er að afleiða tölfræðiaðgerðir eins og framleiðslutíma sem vara notar frá upprunagögnum.</span><span class="sxs-lookup"><span data-stu-id="85b4c-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="85b4c-521">Nánari upplýsingar er að finna í [Veitusniðmát tölfræðiaðgerðar](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="85b4c-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="85b4c-522">Eftirfarandi tafla sýnir niðurstöður þegar mannauðsþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="85b4c-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="85b4c-523">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-523">Cost object</span></span></th>
<th><span data-ttu-id="85b4c-524">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="85b4c-524">Magnitude</span></span></th>
<th><span data-ttu-id="85b4c-525">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="85b4c-525">Allocation factor</span></span></th>
<th><span data-ttu-id="85b4c-526">Upphæð</span><span class="sxs-lookup"><span data-stu-id="85b4c-526">Amount</span></span></th>
<th><span data-ttu-id="85b4c-527">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="85b4c-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-528">CC002</span><span class="sxs-lookup"><span data-stu-id="85b4c-528">CC002</span></span></td>
<td><span data-ttu-id="85b4c-529">Fjármál</span><span class="sxs-lookup"><span data-stu-id="85b4c-529">Finance</span></span></td>
<td><span data-ttu-id="85b4c-530">35</span><span class="sxs-lookup"><span data-stu-id="85b4c-530">35</span></span></td>
<td><span data-ttu-id="85b4c-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="85b4c-532">175.00</span><span class="sxs-lookup"><span data-stu-id="85b4c-532">175.00</span></span></td>
<td><span data-ttu-id="85b4c-533">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-534">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-534">CC003</span></span></td>
<td><span data-ttu-id="85b4c-535">Smölun</span><span class="sxs-lookup"><span data-stu-id="85b4c-535">Assembly</span></span></td>
<td><span data-ttu-id="85b4c-536">55</span><span class="sxs-lookup"><span data-stu-id="85b4c-536">55</span></span></td>
<td><span data-ttu-id="85b4c-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="85b4c-538">275.00</span><span class="sxs-lookup"><span data-stu-id="85b4c-538">275.00</span></span></td>
<td><span data-ttu-id="85b4c-539">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-540">CC004</span><span class="sxs-lookup"><span data-stu-id="85b4c-540">CC004</span></span></td>
<td><span data-ttu-id="85b4c-541">Pakkning</span><span class="sxs-lookup"><span data-stu-id="85b4c-541">Packaging</span></span></td>
<td><span data-ttu-id="85b4c-542">10</span><span class="sxs-lookup"><span data-stu-id="85b4c-542">10</span></span></td>
<td><span data-ttu-id="85b4c-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="85b4c-544">50,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-544">50.00</span></span></td>
<td><span data-ttu-id="85b4c-545">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-546">CC002</span><span class="sxs-lookup"><span data-stu-id="85b4c-546">CC002</span></span></td>
<td><span data-ttu-id="85b4c-547">Fjármál</span><span class="sxs-lookup"><span data-stu-id="85b4c-547">Finance</span></span></td>
<td><span data-ttu-id="85b4c-548">35</span><span class="sxs-lookup"><span data-stu-id="85b4c-548">35</span></span></td>
<td><span data-ttu-id="85b4c-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="85b4c-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="85b4c-550">436.00</span><span class="sxs-lookup"><span data-stu-id="85b4c-550">436.00</span></span></td>
<td><span data-ttu-id="85b4c-551">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-552">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-552">CC003</span></span></td>
<td><span data-ttu-id="85b4c-553">Smölun</span><span class="sxs-lookup"><span data-stu-id="85b4c-553">Assembly</span></span></td>
<td><span data-ttu-id="85b4c-554">55</span><span class="sxs-lookup"><span data-stu-id="85b4c-554">55</span></span></td>
<td><span data-ttu-id="85b4c-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="85b4c-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="85b4c-556">685.14</span><span class="sxs-lookup"><span data-stu-id="85b4c-556">685.14</span></span></td>
<td><span data-ttu-id="85b4c-557">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-558">CC004</span><span class="sxs-lookup"><span data-stu-id="85b4c-558">CC004</span></span></td>
<td><span data-ttu-id="85b4c-559">Pakkning</span><span class="sxs-lookup"><span data-stu-id="85b4c-559">Packaging</span></span></td>
<td><span data-ttu-id="85b4c-560">10</span><span class="sxs-lookup"><span data-stu-id="85b4c-560">10</span></span></td>
<td><span data-ttu-id="85b4c-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="85b4c-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="85b4c-562">124.57</span><span class="sxs-lookup"><span data-stu-id="85b4c-562">124.57</span></span></td>
<td><span data-ttu-id="85b4c-563">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="85b4c-564">Eftirfarandi tafla sýnir niðurstöður þegar Fjármálaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="85b4c-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="85b4c-565">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-565">Cost object</span></span></th>
<th><span data-ttu-id="85b4c-566">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="85b4c-566">Magnitude</span></span></th>
<th><span data-ttu-id="85b4c-567">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="85b4c-567">Allocation factor</span></span></th>
<th><span data-ttu-id="85b4c-568">Upphæð</span><span class="sxs-lookup"><span data-stu-id="85b4c-568">Amount</span></span></th>
<th><span data-ttu-id="85b4c-569">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="85b4c-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-570">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-570">CC003</span></span></td>
<td><span data-ttu-id="85b4c-571">Smölun</span><span class="sxs-lookup"><span data-stu-id="85b4c-571">Assembly</span></span></td>
<td><span data-ttu-id="85b4c-572">65</span><span class="sxs-lookup"><span data-stu-id="85b4c-572">65</span></span></td>
<td><span data-ttu-id="85b4c-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="85b4c-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="85b4c-574">438.75</span><span class="sxs-lookup"><span data-stu-id="85b4c-574">438.75</span></span></td>
<td><span data-ttu-id="85b4c-575">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-576">CC004</span><span class="sxs-lookup"><span data-stu-id="85b4c-576">CC004</span></span></td>
<td><span data-ttu-id="85b4c-577">Pakkning</span><span class="sxs-lookup"><span data-stu-id="85b4c-577">Packaging</span></span></td>
<td><span data-ttu-id="85b4c-578">35</span><span class="sxs-lookup"><span data-stu-id="85b4c-578">35</span></span></td>
<td><span data-ttu-id="85b4c-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="85b4c-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="85b4c-580">236.25</span><span class="sxs-lookup"><span data-stu-id="85b4c-580">236.25</span></span></td>
<td><span data-ttu-id="85b4c-581">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-582">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-582">CC003</span></span></td>
<td><span data-ttu-id="85b4c-583">Smölun</span><span class="sxs-lookup"><span data-stu-id="85b4c-583">Assembly</span></span></td>
<td><span data-ttu-id="85b4c-584">65</span><span class="sxs-lookup"><span data-stu-id="85b4c-584">65</span></span></td>
<td><span data-ttu-id="85b4c-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="85b4c-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="85b4c-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="85b4c-586">5,297.69</span></span></td>
<td><span data-ttu-id="85b4c-587">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-588">CC004</span><span class="sxs-lookup"><span data-stu-id="85b4c-588">CC004</span></span></td>
<td><span data-ttu-id="85b4c-589">Pakkning</span><span class="sxs-lookup"><span data-stu-id="85b4c-589">Packaging</span></span></td>
<td><span data-ttu-id="85b4c-590">35</span><span class="sxs-lookup"><span data-stu-id="85b4c-590">35</span></span></td>
<td><span data-ttu-id="85b4c-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="85b4c-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="85b4c-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="85b4c-592">2,852.60</span></span></td>
<td><span data-ttu-id="85b4c-593">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="85b4c-594">Eftirfarandi tafla sýnir niðurstöður þegar Samsetningarþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="85b4c-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="85b4c-595">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-595">Cost object</span></span></th>
<th><span data-ttu-id="85b4c-596">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="85b4c-596">Magnitude</span></span></th>
<th><span data-ttu-id="85b4c-597">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="85b4c-597">Allocation factor</span></span></th>
<th><span data-ttu-id="85b4c-598">Upphæð</span><span class="sxs-lookup"><span data-stu-id="85b4c-598">Amount</span></span></th>
<th><span data-ttu-id="85b4c-599">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="85b4c-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-600">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-600">Prod 1</span></span></td>
<td><span data-ttu-id="85b4c-601">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-601">Product 1</span></span></td>
<td><span data-ttu-id="85b4c-602">60</span><span class="sxs-lookup"><span data-stu-id="85b4c-602">60</span></span></td>
<td><span data-ttu-id="85b4c-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="85b4c-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="85b4c-604">535.31</span><span class="sxs-lookup"><span data-stu-id="85b4c-604">535.31</span></span></td>
<td><span data-ttu-id="85b4c-605">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-606">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-606">Prod 2</span></span></td>
<td><span data-ttu-id="85b4c-607">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-607">Product 2</span></span></td>
<td><span data-ttu-id="85b4c-608">20</span><span class="sxs-lookup"><span data-stu-id="85b4c-608">20</span></span></td>
<td><span data-ttu-id="85b4c-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="85b4c-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="85b4c-610">178.44</span><span class="sxs-lookup"><span data-stu-id="85b4c-610">178.44</span></span></td>
<td><span data-ttu-id="85b4c-611">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-612">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-612">Prod 1</span></span></td>
<td><span data-ttu-id="85b4c-613">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-613">Product 1</span></span></td>
<td><span data-ttu-id="85b4c-614">60</span><span class="sxs-lookup"><span data-stu-id="85b4c-614">60</span></span></td>
<td><span data-ttu-id="85b4c-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="85b4c-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="85b4c-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="85b4c-616">4,487.12</span></span></td>
<td><span data-ttu-id="85b4c-617">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-618">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-618">Prod 2</span></span></td>
<td><span data-ttu-id="85b4c-619">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-619">Product 2</span></span></td>
<td><span data-ttu-id="85b4c-620">20</span><span class="sxs-lookup"><span data-stu-id="85b4c-620">20</span></span></td>
<td><span data-ttu-id="85b4c-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="85b4c-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="85b4c-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="85b4c-622">1,495.71</span></span></td>
<td><span data-ttu-id="85b4c-623">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="85b4c-624">Eftirfarandi tafla sýnir niðurstöður þegar Umbúðaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="85b4c-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="85b4c-625">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-625">Cost object</span></span></th>
<th><span data-ttu-id="85b4c-626">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="85b4c-626">Magnitude</span></span></th>
<th><span data-ttu-id="85b4c-627">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="85b4c-627">Allocation factor</span></span></th>
<th><span data-ttu-id="85b4c-628">Upphæð</span><span class="sxs-lookup"><span data-stu-id="85b4c-628">Amount</span></span></th>
<th><span data-ttu-id="85b4c-629">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="85b4c-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-630">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-630">Prod 1</span></span></td>
<td><span data-ttu-id="85b4c-631">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-631">Product 1</span></span></td>
<td><span data-ttu-id="85b4c-632">80</span><span class="sxs-lookup"><span data-stu-id="85b4c-632">80</span></span></td>
<td><span data-ttu-id="85b4c-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="85b4c-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="85b4c-634">241.05</span><span class="sxs-lookup"><span data-stu-id="85b4c-634">241.05</span></span></td>
<td><span data-ttu-id="85b4c-635">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-636">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-636">Prod 2</span></span></td>
<td><span data-ttu-id="85b4c-637">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-637">Product 2</span></span></td>
<td><span data-ttu-id="85b4c-638">15</span><span class="sxs-lookup"><span data-stu-id="85b4c-638">15</span></span></td>
<td><span data-ttu-id="85b4c-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="85b4c-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="85b4c-640">45.20</span><span class="sxs-lookup"><span data-stu-id="85b4c-640">45.20</span></span></td>
<td><span data-ttu-id="85b4c-641">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-642">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-642">Prod 1</span></span></td>
<td><span data-ttu-id="85b4c-643">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-643">Product 1</span></span></td>
<td><span data-ttu-id="85b4c-644">80</span><span class="sxs-lookup"><span data-stu-id="85b4c-644">80</span></span></td>
<td><span data-ttu-id="85b4c-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="85b4c-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="85b4c-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="85b4c-646">2,507.09</span></span></td>
<td><span data-ttu-id="85b4c-647">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-648">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-648">Prod 2</span></span></td>
<td><span data-ttu-id="85b4c-649">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-649">Product 2</span></span></td>
<td><span data-ttu-id="85b4c-650">15</span><span class="sxs-lookup"><span data-stu-id="85b4c-650">15</span></span></td>
<td><span data-ttu-id="85b4c-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="85b4c-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="85b4c-652">470.08</span><span class="sxs-lookup"><span data-stu-id="85b4c-652">470.08</span></span></td>
<td><span data-ttu-id="85b4c-653">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="85b4c-654">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="85b4c-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="85b4c-655">Færslubók</span><span class="sxs-lookup"><span data-stu-id="85b4c-655">Journal</span></span></th>
<th><span data-ttu-id="85b4c-656">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="85b4c-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="85b4c-657">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="85b4c-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="85b4c-658">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="85b4c-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-659">00004</span><span class="sxs-lookup"><span data-stu-id="85b4c-659">00004</span></span></td>
<td><span data-ttu-id="85b4c-660">Færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="85b4c-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="85b4c-661">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="85b4c-661">Fiscal</span></span></td>
<td><span data-ttu-id="85b4c-662">2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-662">2017</span></span></td>
<td><span data-ttu-id="85b4c-663">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="85b4c-663">Period 1</span></span></td>
<td><span data-ttu-id="85b4c-664">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="85b4c-665">Færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="85b4c-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="85b4c-666">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="85b4c-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="85b4c-667">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="85b4c-668">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="85b4c-668">Cost element</span></span></th>
<th><span data-ttu-id="85b4c-669">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="85b4c-669">Cost behavior</span></span></th>
<th><span data-ttu-id="85b4c-670">Upphæð</span><span class="sxs-lookup"><span data-stu-id="85b4c-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-671">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="85b4c-672">CC001</span><span class="sxs-lookup"><span data-stu-id="85b4c-672">CC001</span></span></td>
<td><span data-ttu-id="85b4c-673">Mannauður</span><span class="sxs-lookup"><span data-stu-id="85b4c-673">HR</span></span></td>
<td><span data-ttu-id="85b4c-674">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-674">10001</span></span></td>
<td><span data-ttu-id="85b4c-675">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-675">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-676">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-676">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-677">500,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-678">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="85b4c-679">CC001</span><span class="sxs-lookup"><span data-stu-id="85b4c-679">CC001</span></span></td>
<td><span data-ttu-id="85b4c-680">Mannauður</span><span class="sxs-lookup"><span data-stu-id="85b4c-680">HR</span></span></td>
<td><span data-ttu-id="85b4c-681">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-681">10001</span></span></td>
<td><span data-ttu-id="85b4c-682">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-682">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-683">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-683">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="85b4c-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-685">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="85b4c-686">CC002</span><span class="sxs-lookup"><span data-stu-id="85b4c-686">CC002</span></span></td>
<td><span data-ttu-id="85b4c-687">Fjármál</span><span class="sxs-lookup"><span data-stu-id="85b4c-687">Finance</span></span></td>
<td><span data-ttu-id="85b4c-688">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-688">10001</span></span></td>
<td><span data-ttu-id="85b4c-689">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-689">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-690">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-690">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-691">675.00</span><span class="sxs-lookup"><span data-stu-id="85b4c-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-692">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="85b4c-693">CC002</span><span class="sxs-lookup"><span data-stu-id="85b4c-693">CC002</span></span></td>
<td><span data-ttu-id="85b4c-694">Fjármál</span><span class="sxs-lookup"><span data-stu-id="85b4c-694">Finance</span></span></td>
<td><span data-ttu-id="85b4c-695">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-695">10001</span></span></td>
<td><span data-ttu-id="85b4c-696">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-696">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-697">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-697">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="85b4c-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-699">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="85b4c-700">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-700">CC003</span></span></td>
<td><span data-ttu-id="85b4c-701">Smölun</span><span class="sxs-lookup"><span data-stu-id="85b4c-701">Assembly</span></span></td>
<td><span data-ttu-id="85b4c-702">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-702">10001</span></span></td>
<td><span data-ttu-id="85b4c-703">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-703">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-704">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-704">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-705">713.75</span><span class="sxs-lookup"><span data-stu-id="85b4c-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-706">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="85b4c-707">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-707">CC003</span></span></td>
<td><span data-ttu-id="85b4c-708">Smölun</span><span class="sxs-lookup"><span data-stu-id="85b4c-708">Assembly</span></span></td>
<td><span data-ttu-id="85b4c-709">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-709">10001</span></span></td>
<td><span data-ttu-id="85b4c-710">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-710">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-711">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-711">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="85b4c-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-713">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="85b4c-714">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-714">CC003</span></span></td>
<td><span data-ttu-id="85b4c-715">Pakkning</span><span class="sxs-lookup"><span data-stu-id="85b4c-715">Packaging</span></span></td>
<td><span data-ttu-id="85b4c-716">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-716">10001</span></span></td>
<td><span data-ttu-id="85b4c-717">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-717">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-718">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-718">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-719">286.25</span><span class="sxs-lookup"><span data-stu-id="85b4c-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-720">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="85b4c-721">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-721">CC003</span></span></td>
<td><span data-ttu-id="85b4c-722">Pakkning</span><span class="sxs-lookup"><span data-stu-id="85b4c-722">Packaging</span></span></td>
<td><span data-ttu-id="85b4c-723">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-723">10001</span></span></td>
<td><span data-ttu-id="85b4c-724">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-724">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-725">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-725">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="85b4c-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-727">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="85b4c-728">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-728">Prod 1</span></span></td>
<td><span data-ttu-id="85b4c-729">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-729">Product 1</span></span></td>
<td><span data-ttu-id="85b4c-730">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-730">10001</span></span></td>
<td><span data-ttu-id="85b4c-731">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-731">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-732">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-732">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-733">776.36</span><span class="sxs-lookup"><span data-stu-id="85b4c-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-734">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="85b4c-735">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-735">Prod 1</span></span></td>
<td><span data-ttu-id="85b4c-736">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-736">Product 1</span></span></td>
<td><span data-ttu-id="85b4c-737">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-737">10001</span></span></td>
<td><span data-ttu-id="85b4c-738">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-738">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-739">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-739">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="85b4c-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-741">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="85b4c-742">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-742">Prod 2</span></span></td>
<td><span data-ttu-id="85b4c-743">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-743">Product 1</span></span></td>
<td><span data-ttu-id="85b4c-744">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-744">10001</span></span></td>
<td><span data-ttu-id="85b4c-745">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-745">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-746">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-746">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-747">223.64</span><span class="sxs-lookup"><span data-stu-id="85b4c-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-748">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="85b4c-749">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-749">Prod 2</span></span></td>
<td><span data-ttu-id="85b4c-750">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-750">Product 1</span></span></td>
<td><span data-ttu-id="85b4c-751">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-751">10001</span></span></td>
<td><span data-ttu-id="85b4c-752">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-752">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-753">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-753">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="85b4c-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="85b4c-755">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="85b4c-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="85b4c-756">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="85b4c-757">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="85b4c-757">Cost element</span></span></th>
<th><span data-ttu-id="85b4c-758">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="85b4c-758">Cost behavior</span></span></th>
<th><span data-ttu-id="85b4c-759">Upphæð</span><span class="sxs-lookup"><span data-stu-id="85b4c-759">Amount</span></span></th>
<th><span data-ttu-id="85b4c-760">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="85b4c-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="85b4c-761">CC001</span><span class="sxs-lookup"><span data-stu-id="85b4c-761">CC001</span></span></td>
<td><span data-ttu-id="85b4c-762">Mannauður</span><span class="sxs-lookup"><span data-stu-id="85b4c-762">HR</span></span></td>
<td><span data-ttu-id="85b4c-763">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-763">10001</span></span></td>
<td><span data-ttu-id="85b4c-764">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-764">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-765">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-765">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-766">-500.00</span></span></td>
<td><span data-ttu-id="85b4c-767">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-768">CC002</span><span class="sxs-lookup"><span data-stu-id="85b4c-768">CC002</span></span></td>
<td><span data-ttu-id="85b4c-769">Fjármál</span><span class="sxs-lookup"><span data-stu-id="85b4c-769">Finance</span></span></td>
<td><span data-ttu-id="85b4c-770">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-770">10001</span></span></td>
<td><span data-ttu-id="85b4c-771">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-771">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-772">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-772">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-773">175.00</span><span class="sxs-lookup"><span data-stu-id="85b4c-773">175.00</span></span></td>
<td><span data-ttu-id="85b4c-774">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-775">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-775">CC003</span></span></td>
<td><span data-ttu-id="85b4c-776">Smölun</span><span class="sxs-lookup"><span data-stu-id="85b4c-776">Assembly</span></span></td>
<td><span data-ttu-id="85b4c-777">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-777">10001</span></span></td>
<td><span data-ttu-id="85b4c-778">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-778">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-779">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-779">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-780">275.00</span><span class="sxs-lookup"><span data-stu-id="85b4c-780">275.00</span></span></td>
<td><span data-ttu-id="85b4c-781">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-782">CC004</span><span class="sxs-lookup"><span data-stu-id="85b4c-782">CC004</span></span></td>
<td><span data-ttu-id="85b4c-783">Pakkning</span><span class="sxs-lookup"><span data-stu-id="85b4c-783">Packaging</span></span></td>
<td><span data-ttu-id="85b4c-784">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-784">10001</span></span></td>
<td><span data-ttu-id="85b4c-785">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-785">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-786">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-786">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-787">50,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-787">50,00</span></span></td>
<td><span data-ttu-id="85b4c-788">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-789">CC001</span><span class="sxs-lookup"><span data-stu-id="85b4c-789">CC001</span></span></td>
<td><span data-ttu-id="85b4c-790">Mannauður</span><span class="sxs-lookup"><span data-stu-id="85b4c-790">HR</span></span></td>
<td><span data-ttu-id="85b4c-791">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-791">10001</span></span></td>
<td><span data-ttu-id="85b4c-792">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-792">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-793">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-793">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="85b4c-794">-1,245.71</span></span></td>
<td><span data-ttu-id="85b4c-795">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-796">CC002</span><span class="sxs-lookup"><span data-stu-id="85b4c-796">CC002</span></span></td>
<td><span data-ttu-id="85b4c-797">Fjármál</span><span class="sxs-lookup"><span data-stu-id="85b4c-797">Finance</span></span></td>
<td><span data-ttu-id="85b4c-798">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-798">10001</span></span></td>
<td><span data-ttu-id="85b4c-799">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-799">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-800">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-800">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-801">436.00</span><span class="sxs-lookup"><span data-stu-id="85b4c-801">436.00</span></span></td>
<td><span data-ttu-id="85b4c-802">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-803">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-803">CC003</span></span></td>
<td><span data-ttu-id="85b4c-804">Smölun</span><span class="sxs-lookup"><span data-stu-id="85b4c-804">Assembly</span></span></td>
<td><span data-ttu-id="85b4c-805">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-805">10001</span></span></td>
<td><span data-ttu-id="85b4c-806">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-806">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-807">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-807">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-808">685.14</span><span class="sxs-lookup"><span data-stu-id="85b4c-808">685.14</span></span></td>
<td><span data-ttu-id="85b4c-809">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-810">CC004</span><span class="sxs-lookup"><span data-stu-id="85b4c-810">CC004</span></span></td>
<td><span data-ttu-id="85b4c-811">Pakkning</span><span class="sxs-lookup"><span data-stu-id="85b4c-811">Packaging</span></span></td>
<td><span data-ttu-id="85b4c-812">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-812">10001</span></span></td>
<td><span data-ttu-id="85b4c-813">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-813">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-814">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-814">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-815">124.57</span><span class="sxs-lookup"><span data-stu-id="85b4c-815">124.57</span></span></td>
<td><span data-ttu-id="85b4c-816">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-817">CC002</span><span class="sxs-lookup"><span data-stu-id="85b4c-817">CC002</span></span></td>
<td><span data-ttu-id="85b4c-818">Fjármál</span><span class="sxs-lookup"><span data-stu-id="85b4c-818">Finance</span></span></td>
<td><span data-ttu-id="85b4c-819">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-819">10001</span></span></td>
<td><span data-ttu-id="85b4c-820">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-820">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-821">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-821">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-822">-675.00</span></span></td>
<td><span data-ttu-id="85b4c-823">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-824">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-824">CC003</span></span></td>
<td><span data-ttu-id="85b4c-825">Smölun</span><span class="sxs-lookup"><span data-stu-id="85b4c-825">Assembly</span></span></td>
<td><span data-ttu-id="85b4c-826">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-826">10001</span></span></td>
<td><span data-ttu-id="85b4c-827">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-827">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-828">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-828">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-829">438.75</span><span class="sxs-lookup"><span data-stu-id="85b4c-829">438.75</span></span></td>
<td><span data-ttu-id="85b4c-830">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-831">CC004</span><span class="sxs-lookup"><span data-stu-id="85b4c-831">CC004</span></span></td>
<td><span data-ttu-id="85b4c-832">Pakkning</span><span class="sxs-lookup"><span data-stu-id="85b4c-832">Packaging</span></span></td>
<td><span data-ttu-id="85b4c-833">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-833">10001</span></span></td>
<td><span data-ttu-id="85b4c-834">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-834">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-835">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-835">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-836">236.25</span><span class="sxs-lookup"><span data-stu-id="85b4c-836">236.25</span></span></td>
<td><span data-ttu-id="85b4c-837">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-838">CC002</span><span class="sxs-lookup"><span data-stu-id="85b4c-838">CC002</span></span></td>
<td><span data-ttu-id="85b4c-839">Fjármál</span><span class="sxs-lookup"><span data-stu-id="85b4c-839">Finance</span></span></td>
<td><span data-ttu-id="85b4c-840">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-840">10001</span></span></td>
<td><span data-ttu-id="85b4c-841">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-841">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-842">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-842">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="85b4c-843">-8,150.29</span></span></td>
<td><span data-ttu-id="85b4c-844">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-845">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-845">CC003</span></span></td>
<td><span data-ttu-id="85b4c-846">Smölun</span><span class="sxs-lookup"><span data-stu-id="85b4c-846">Assembly</span></span></td>
<td><span data-ttu-id="85b4c-847">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-847">10001</span></span></td>
<td><span data-ttu-id="85b4c-848">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-848">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-849">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-849">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="85b4c-850">5,297.69</span></span></td>
<td><span data-ttu-id="85b4c-851">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-852">CC004</span><span class="sxs-lookup"><span data-stu-id="85b4c-852">CC004</span></span></td>
<td><span data-ttu-id="85b4c-853">Pakkning</span><span class="sxs-lookup"><span data-stu-id="85b4c-853">Packaging</span></span></td>
<td><span data-ttu-id="85b4c-854">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-854">10001</span></span></td>
<td><span data-ttu-id="85b4c-855">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-855">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-856">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-856">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="85b4c-857">2,852.60</span></span></td>
<td><span data-ttu-id="85b4c-858">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-859">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-859">CC003</span></span></td>
<td><span data-ttu-id="85b4c-860">Smölun</span><span class="sxs-lookup"><span data-stu-id="85b4c-860">Assembly</span></span></td>
<td><span data-ttu-id="85b4c-861">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-861">10001</span></span></td>
<td><span data-ttu-id="85b4c-862">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-862">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-863">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-863">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="85b4c-864">-713.75</span></span></td>
<td><span data-ttu-id="85b4c-865">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-866">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-866">Prod 1</span></span></td>
<td><span data-ttu-id="85b4c-867">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-867">Product 1</span></span></td>
<td><span data-ttu-id="85b4c-868">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-868">10001</span></span></td>
<td><span data-ttu-id="85b4c-869">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-869">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-870">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-870">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-871">535.31</span><span class="sxs-lookup"><span data-stu-id="85b4c-871">535.31</span></span></td>
<td><span data-ttu-id="85b4c-872">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-873">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-873">Prod 2</span></span></td>
<td><span data-ttu-id="85b4c-874">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-874">Product 2</span></span></td>
<td><span data-ttu-id="85b4c-875">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-875">10001</span></span></td>
<td><span data-ttu-id="85b4c-876">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-876">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-877">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-877">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-878">178.44</span><span class="sxs-lookup"><span data-stu-id="85b4c-878">178.44</span></span></td>
<td><span data-ttu-id="85b4c-879">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-880">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-880">CC003</span></span></td>
<td><span data-ttu-id="85b4c-881">Smölun</span><span class="sxs-lookup"><span data-stu-id="85b4c-881">Assembly</span></span></td>
<td><span data-ttu-id="85b4c-882">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-882">10001</span></span></td>
<td><span data-ttu-id="85b4c-883">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-883">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-884">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-884">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="85b4c-885">-5,982.83</span></span></td>
<td><span data-ttu-id="85b4c-886">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-887">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-887">Prod 1</span></span></td>
<td><span data-ttu-id="85b4c-888">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-888">Product 1</span></span></td>
<td><span data-ttu-id="85b4c-889">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-889">10001</span></span></td>
<td><span data-ttu-id="85b4c-890">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-890">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-891">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-891">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="85b4c-892">4,487.12</span></span></td>
<td><span data-ttu-id="85b4c-893">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-894">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-894">Prod 2</span></span></td>
<td><span data-ttu-id="85b4c-895">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-895">Product 2</span></span></td>
<td><span data-ttu-id="85b4c-896">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-896">10001</span></span></td>
<td><span data-ttu-id="85b4c-897">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-897">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-898">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-898">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="85b4c-899">1,495.71</span></span></td>
<td><span data-ttu-id="85b4c-900">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-901">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-901">CC003</span></span></td>
<td><span data-ttu-id="85b4c-902">Smölun</span><span class="sxs-lookup"><span data-stu-id="85b4c-902">Assembly</span></span></td>
<td><span data-ttu-id="85b4c-903">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-903">10001</span></span></td>
<td><span data-ttu-id="85b4c-904">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-904">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-905">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-905">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="85b4c-906">-286.25</span></span></td>
<td><span data-ttu-id="85b4c-907">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-908">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-908">Prod 1</span></span></td>
<td><span data-ttu-id="85b4c-909">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-909">Product 1</span></span></td>
<td><span data-ttu-id="85b4c-910">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-910">10001</span></span></td>
<td><span data-ttu-id="85b4c-911">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-911">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-912">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-912">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-913">241.05</span><span class="sxs-lookup"><span data-stu-id="85b4c-913">241.05</span></span></td>
<td><span data-ttu-id="85b4c-914">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-915">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-915">Prod 2</span></span></td>
<td><span data-ttu-id="85b4c-916">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-916">Product 2</span></span></td>
<td><span data-ttu-id="85b4c-917">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-917">10001</span></span></td>
<td><span data-ttu-id="85b4c-918">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-918">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-919">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-919">Fixed cost</span></span></td>
<td><span data-ttu-id="85b4c-920">45.20</span><span class="sxs-lookup"><span data-stu-id="85b4c-920">45.20</span></span></td>
<td><span data-ttu-id="85b4c-921">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-922">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-922">CC003</span></span></td>
<td><span data-ttu-id="85b4c-923">Smölun</span><span class="sxs-lookup"><span data-stu-id="85b4c-923">Assembly</span></span></td>
<td><span data-ttu-id="85b4c-924">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-924">10001</span></span></td>
<td><span data-ttu-id="85b4c-925">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-925">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-926">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-926">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="85b4c-927">-2,977.17</span></span></td>
<td><span data-ttu-id="85b4c-928">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-929">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-929">Prod 1</span></span></td>
<td><span data-ttu-id="85b4c-930">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-930">Product 1</span></span></td>
<td><span data-ttu-id="85b4c-931">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-931">10001</span></span></td>
<td><span data-ttu-id="85b4c-932">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-932">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-933">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-933">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="85b4c-934">2,507.09</span></span></td>
<td><span data-ttu-id="85b4c-935">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="85b4c-936">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-936">Prod 2</span></span></td>
<td><span data-ttu-id="85b4c-937">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-937">Product 2</span></span></td>
<td><span data-ttu-id="85b4c-938">10001</span><span class="sxs-lookup"><span data-stu-id="85b4c-938">10001</span></span></td>
<td><span data-ttu-id="85b4c-939">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-939">Electricity</span></span></td>
<td><span data-ttu-id="85b4c-940">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-940">Variable cost</span></span></td>
<td><span data-ttu-id="85b4c-941">470.08</span><span class="sxs-lookup"><span data-stu-id="85b4c-941">470.08</span></span></td>
<td><span data-ttu-id="85b4c-942">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="85b4c-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="85b4c-943">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="85b4c-943">Conclusion</span></span>
<span data-ttu-id="85b4c-944">Í Fjárhagsbókhaldi er kostnaður upp á 10.000,00 fyrir rafmagn bókaður á kenni leppkostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="85b4c-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="85b4c-945">Þar af leiðandi munu kostnaðarbókarar vita að það þarf að úthluta þessum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="85b4c-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="85b4c-946">Í kostnaðarbókhaldi streymir kostnaður þvert á fyrirtækiseiningar og stig, samkvæmt þeim stefnum og reglum sem eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="85b4c-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="85b4c-947">Hver kostnaður hefur verið tengdur úthlutunargrunni sem veitir besta mat á úthlutun á kostnaði.</span><span class="sxs-lookup"><span data-stu-id="85b4c-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="85b4c-948">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="85b4c-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="85b4c-949">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="85b4c-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="85b4c-950">Samtala</span><span class="sxs-lookup"><span data-stu-id="85b4c-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="85b4c-951">CC099</span><span class="sxs-lookup"><span data-stu-id="85b4c-951">CC099</span></span></th>
<th><span data-ttu-id="85b4c-952">CC001</span><span class="sxs-lookup"><span data-stu-id="85b4c-952">CC001</span></span></th>
<th><span data-ttu-id="85b4c-953">CC002</span><span class="sxs-lookup"><span data-stu-id="85b4c-953">CC002</span></span></th>
<th><span data-ttu-id="85b4c-954">CC003</span><span class="sxs-lookup"><span data-stu-id="85b4c-954">CC003</span></span></th>
<th><span data-ttu-id="85b4c-955">CC004</span><span class="sxs-lookup"><span data-stu-id="85b4c-955">CC004</span></span></th>
<th><span data-ttu-id="85b4c-956">Verk 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-956">Proj 1</span></span></th>
<th><span data-ttu-id="85b4c-957">Verk 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-957">Proj 2</span></span></th>
<th><span data-ttu-id="85b4c-958">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="85b4c-958">Prod 1</span></span></th>
<th><span data-ttu-id="85b4c-959">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="85b4c-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="85b4c-960">10001 Rafmagn</span><span class="sxs-lookup"><span data-stu-id="85b4c-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="85b4c-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="85b4c-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="85b4c-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="85b4c-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="85b4c-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="85b4c-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="85b4c-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="85b4c-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="85b4c-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="85b4c-970">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="85b4c-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-971">0,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="85b4c-972">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-973">0,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-974">0,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-975">0,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-976">0,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-977">0,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-978">776.36</span><span class="sxs-lookup"><span data-stu-id="85b4c-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-979">223.64</span><span class="sxs-lookup"><span data-stu-id="85b4c-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="85b4c-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="85b4c-981">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="85b4c-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-982">000</span><span class="sxs-lookup"><span data-stu-id="85b4c-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-983">0,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-984">0,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-985">0,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-986">0,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-987">30,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-988">10,00</span><span class="sxs-lookup"><span data-stu-id="85b4c-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="85b4c-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="85b4c-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="85b4c-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="85b4c-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="85b4c-992">Þetta efnisatriði sýnir hvernig fyrir aðalkostnaðareiningin 10001 Rafmagn flæðir í gegnum kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="85b4c-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="85b4c-993">Þar af leiðandi er þessum sameiginlega kostnaði úthlutað á lægsta stigið í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="85b4c-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="85b4c-994">Með öðrum orðum bera kostnaðarhlutir á lægsta stiginu kostnaðinn.</span><span class="sxs-lookup"><span data-stu-id="85b4c-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="85b4c-995">Ef þú þarft sjónrænt flæði kostnaðar á milli kostnaðarhluta er hægt að nota stefnureglur samantekins kostnaðar til að gera kostnaðarflæðið sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="85b4c-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="85b4c-996">Fyrir frekari upplýsingar skal sjá [Stefna fyrir samantekt kostnaðar og útreikning sameiginlegs kostnaðar](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="85b4c-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



