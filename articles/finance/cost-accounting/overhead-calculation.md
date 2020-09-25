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
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: cc6ad48ef80aa01739129b59cc1133d0a1930f24
ms.sourcegitcommit: cd339f48066b1d0fc740b513cb72ea19015acd16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3759473"
---
# <a name="overhead-calculation"></a><span data-ttu-id="9d35b-103">Útreikningur fastakostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d35b-104">Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði.</span><span class="sxs-lookup"><span data-stu-id="9d35b-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="9d35b-105">Skýrsluskilgreining</span><span class="sxs-lookup"><span data-stu-id="9d35b-105">Term definition</span></span>
---------------

<span data-ttu-id="9d35b-106">Stjórnunarkostnaður er sá kostnaður sem stofnað er til fyrir rekstur fyrirtækis, en sem ekki er hægt að rekja beint til neinna sérstakrar starfsemi, vöru eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="9d35b-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="9d35b-107">Stjórnunarkostnaður veitir mikilvægan stuðning við myndun hagnaðarmyndandi verkþátta.</span><span class="sxs-lookup"><span data-stu-id="9d35b-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="9d35b-108">Hér eru nokkur dæmi um skilyrði:</span><span class="sxs-lookup"><span data-stu-id="9d35b-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="9d35b-109">Leiga</span><span class="sxs-lookup"><span data-stu-id="9d35b-109">Rent</span></span>
-   <span data-ttu-id="9d35b-110">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-110">Electricity</span></span>
-   <span data-ttu-id="9d35b-111">Stjórnunarkostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="9d35b-112">Yfirlit yfir útreikning fastakostnaðar</span><span class="sxs-lookup"><span data-stu-id="9d35b-112">Overhead calculation overview</span></span>
<span data-ttu-id="9d35b-113">Útreikningur fastakostnaðar keyrir reglur kostnaðarbókhalds í réttri röð.</span><span class="sxs-lookup"><span data-stu-id="9d35b-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="9d35b-114">Hægt er að keyra útreikning fastakostnaðar margsinnis fyrir sama fjárhagstímabil ef reglum kostnaðarbókhalds hefur verið breytt eða ákveðnar villur hafa fundist.</span><span class="sxs-lookup"><span data-stu-id="9d35b-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="9d35b-115">Hver keyrsla á útreikningi fastakostnaðar er geymd og fær einkvæmt útgáfukenni sem gerir kleift að bera saman útreikning í mismunandi útgáfum.</span><span class="sxs-lookup"><span data-stu-id="9d35b-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="9d35b-116">Kostnaðarfærslur sem útreikningur fastakostnaðar mynda fá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="9d35b-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="9d35b-117">Dagsetningin bókhald samsvarar lokadagsetning fjárhagstímabilsins sem er dagsetning reikningsskiladagsetning reikningsskila notað í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="9d35b-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="9d35b-118">Einkvæmt útgáfukenni samanstendur af eftirfarandi þáttum:</span><span class="sxs-lookup"><span data-stu-id="9d35b-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="9d35b-119">Gerð útgáfu</span><span class="sxs-lookup"><span data-stu-id="9d35b-119">Version type</span></span>
-   <span data-ttu-id="9d35b-120">Dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="9d35b-120">Date and time</span></span>
-   <span data-ttu-id="9d35b-121">Fjárhagur kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="9d35b-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="9d35b-122">Fjárhagsár</span><span class="sxs-lookup"><span data-stu-id="9d35b-122">Fiscal year</span></span>
-   <span data-ttu-id="9d35b-123">Reikningstímabil</span><span class="sxs-lookup"><span data-stu-id="9d35b-123">Fiscal period</span></span>

<span data-ttu-id="9d35b-124">Útreikningur fastakostnaðar er keyrður óháð því hver útgáfan er.</span><span class="sxs-lookup"><span data-stu-id="9d35b-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="9d35b-125">Þess vegna er hægt að reikna út áætlaða útgáfu á undan raunútgáfu.</span><span class="sxs-lookup"><span data-stu-id="9d35b-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="9d35b-126">Útreikningur fastakostnaðar samanstendur af fjórum skrefum, eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="9d35b-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="9d35b-127">Í hverju skrefi er færslubókarhaus stofnaður með bókarfærslum.</span><span class="sxs-lookup"><span data-stu-id="9d35b-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="9d35b-128">Þessi færslubókarhaus geymir inntaksgögn fyrir hvert útreikningsþrep.</span><span class="sxs-lookup"><span data-stu-id="9d35b-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="9d35b-129">Stefnur og reglur eru notaðar í hverri færslulínu og kostnaðarfærslur eru myndaðar sem úttak.</span><span class="sxs-lookup"><span data-stu-id="9d35b-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="9d35b-130">Þess vegna hefurðu ávallt fullan rekjanleika.</span><span class="sxs-lookup"><span data-stu-id="9d35b-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="9d35b-131">[![Útreikningur fastakostnaðar](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="9d35b-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="9d35b-132">Reikna og úthluta sameiginlegur kostnaði vegna rafmagns</span><span class="sxs-lookup"><span data-stu-id="9d35b-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="9d35b-133">Í Fjárhagsbókhaldi er ákveðinn kostnaður, eins og rafmagn, skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="9d35b-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="9d35b-134">Þar af leiðandi er nákvæmar innsýn rekstrarfélags ekki veitt fyrir kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="9d35b-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="9d35b-135">Í kostnaðarbókhaldi verður kostnaður að flæða í gegnum fyrirtækiseiningar til að veita rétta innsýn rekstrarfélags þvert á allar fyrirtækiseiningar og stig.</span><span class="sxs-lookup"><span data-stu-id="9d35b-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="9d35b-136">Þetta flæði verður að byggja á annaðhvort nákvæmri færslu notkunar eða sanngjarnri matsreglu.</span><span class="sxs-lookup"><span data-stu-id="9d35b-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="9d35b-137">Í fjárhagnum er hægt að bóka rafmagnskostnað eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="9d35b-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9d35b-138">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="9d35b-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9d35b-139">Kostnaðarstaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="9d35b-140">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="9d35b-140">Main account</span></span></th>
<th><span data-ttu-id="9d35b-141">Upphæð í bókhaldsgjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="9d35b-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-142">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="9d35b-143">CC099</span><span class="sxs-lookup"><span data-stu-id="9d35b-143">CC099</span></span></td>
<td><span data-ttu-id="9d35b-144">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9d35b-144">Default cost center</span></span></td>
<td><span data-ttu-id="9d35b-145">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-145">10001</span></span></td>
<td><span data-ttu-id="9d35b-146">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-146">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="9d35b-148">Skref 1: Keyra útreikning kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="9d35b-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="9d35b-149">Sjálfvirkt er að þegar kostnaðarfærslur eru fluttar úr grunngögnum fái þær flokkun kostnaðarhegðunar **Óflokkað** í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="9d35b-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="9d35b-150">Með því að nota stefnureglur kostnaðarhegðunar er hægt að endurflokka kostnaðarfærslur sem annaðhvort **Fastan kostnað** eða **Breytilegan kostnað**.</span><span class="sxs-lookup"><span data-stu-id="9d35b-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="9d35b-151">Tilgreinið reglu kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="9d35b-151">Define the cost behavior rule</span></span>

<span data-ttu-id="9d35b-152">Í sumum tilfellum er hluti af kostnaði föst þóknun og eftirstandandi kostnaður byggist á notkun.</span><span class="sxs-lookup"><span data-stu-id="9d35b-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="9d35b-153">Rafmagnsreikningar stemma oft við þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="9d35b-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="9d35b-154">Þegar tiltekin föst þóknun hefur verið greidd, er greitt fyrir notkun á kílóvattklukkustund (Kwh).</span><span class="sxs-lookup"><span data-stu-id="9d35b-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="9d35b-155">Til dæmis ef föst kostnaðarþóknun er 1000.00 sýnir þetta hvernig regla kostnaðarhegðunar er skilgreind:</span><span class="sxs-lookup"><span data-stu-id="9d35b-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="9d35b-156">Föst upphæð 1.000,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="9d35b-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="9d35b-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="9d35b-158">1000.01 &lt; N = Breyta</span><span class="sxs-lookup"><span data-stu-id="9d35b-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="9d35b-159">Færslubók</span><span class="sxs-lookup"><span data-stu-id="9d35b-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9d35b-160">Færslubók</span><span class="sxs-lookup"><span data-stu-id="9d35b-160">Journal</span></span></th>
<th><span data-ttu-id="9d35b-161">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="9d35b-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="9d35b-162">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="9d35b-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="9d35b-163">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="9d35b-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-164">00001</span><span class="sxs-lookup"><span data-stu-id="9d35b-164">00001</span></span></td>
<td><span data-ttu-id="9d35b-165">Færslubók útreiknings fyrir kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9d35b-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="9d35b-166">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="9d35b-166">Fiscal</span></span></td>
<td><span data-ttu-id="9d35b-167">2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-167">2017</span></span></td>
<td><span data-ttu-id="9d35b-168">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="9d35b-168">Period 1</span></span></td>
<td><span data-ttu-id="9d35b-169">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="9d35b-170">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="9d35b-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9d35b-171">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="9d35b-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9d35b-172">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9d35b-173">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9d35b-173">Cost element</span></span></th>
<th><span data-ttu-id="9d35b-174">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9d35b-174">Cost behavior</span></span></th>
<th><span data-ttu-id="9d35b-175">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9d35b-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-176">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="9d35b-177">CC099</span><span class="sxs-lookup"><span data-stu-id="9d35b-177">CC099</span></span></td>
<td><span data-ttu-id="9d35b-178">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9d35b-178">Default cost center</span></span></td>
<td><span data-ttu-id="9d35b-179">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-179">10001</span></span></td>
<td><span data-ttu-id="9d35b-180">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-180">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-181">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="9d35b-181">Unclassified</span></span></td>
<td><span data-ttu-id="9d35b-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="9d35b-183">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="9d35b-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9d35b-184">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9d35b-185">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9d35b-185">Cost element</span></span></th>
<th><span data-ttu-id="9d35b-186">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9d35b-186">Cost behavior</span></span></th>
<th><span data-ttu-id="9d35b-187">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9d35b-187">Amount</span></span></th>
<th><span data-ttu-id="9d35b-188">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="9d35b-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-189">CC099</span><span class="sxs-lookup"><span data-stu-id="9d35b-189">CC099</span></span></td>
<td><span data-ttu-id="9d35b-190">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9d35b-190">Default cost center</span></span></td>
<td><span data-ttu-id="9d35b-191">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-191">10001</span></span></td>
<td><span data-ttu-id="9d35b-192">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-192">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-193">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="9d35b-193">Unclassified</span></span></td>
<td><span data-ttu-id="9d35b-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-194">10,000.00</span></span></td>
<td><span data-ttu-id="9d35b-195">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-196">CC099</span><span class="sxs-lookup"><span data-stu-id="9d35b-196">CC099</span></span></td>
<td><span data-ttu-id="9d35b-197">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9d35b-197">Default cost center</span></span></td>
<td><span data-ttu-id="9d35b-198">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-198">10001</span></span></td>
<td><span data-ttu-id="9d35b-199">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-199">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-200">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="9d35b-200">Unclassified</span></span></td>
<td><span data-ttu-id="9d35b-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-201">-10,000.00</span></span></td>
<td><span data-ttu-id="9d35b-202">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-203">CC099</span><span class="sxs-lookup"><span data-stu-id="9d35b-203">CC099</span></span></td>
<td><span data-ttu-id="9d35b-204">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9d35b-204">Default cost center</span></span></td>
<td><span data-ttu-id="9d35b-205">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-205">10001</span></span></td>
<td><span data-ttu-id="9d35b-206">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-206">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-207">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-207">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-208">1,000.00</span></span></td>
<td><span data-ttu-id="9d35b-209">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-210">CC099</span><span class="sxs-lookup"><span data-stu-id="9d35b-210">CC099</span></span></td>
<td><span data-ttu-id="9d35b-211">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9d35b-211">Default cost center</span></span></td>
<td><span data-ttu-id="9d35b-212">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-212">10001</span></span></td>
<td><span data-ttu-id="9d35b-213">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-213">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-214">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-214">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="9d35b-215">9,000.00</span></span></td>
<td><span data-ttu-id="9d35b-216">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9d35b-217">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðarhegðunarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="9d35b-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="9d35b-218">Skref 2: Keyra útreikning kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="9d35b-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="9d35b-219">Kostnaðardreifing er notuð til að endurúthluta kostnaði frá einum kostnaðarhlut til annars eða fleiri kostnaðarhluta með því að nota viðeigandi úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="9d35b-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="9d35b-220">Kostnaðardreifing og kostnaðarúthlutun eru ólíkar að því leyti að kostnaðardreifing kemur alltaf upp á stigi aðalkostnaðareiningar upphaflegs verðs.</span><span class="sxs-lookup"><span data-stu-id="9d35b-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="9d35b-221">Tilgreinið kostnaðardreifingarreglu</span><span class="sxs-lookup"><span data-stu-id="9d35b-221">Define the cost distribution rule</span></span>

<span data-ttu-id="9d35b-222">Í Fjárhagsbókhaldi er rafmagnskostnaður oft skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="9d35b-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="9d35b-223">Í kostnaðarbókhaldi er þessi nálgun ekki nógu nákvæm.</span><span class="sxs-lookup"><span data-stu-id="9d35b-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="9d35b-224">Breytilegur kostnaði þarf að dreifa á staka kostnaðarhluti á sanngjörnum grunni.</span><span class="sxs-lookup"><span data-stu-id="9d35b-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="9d35b-225">Rökréttasti úthlutunargrunnurinn er notkun á rafmagni (Kwh).</span><span class="sxs-lookup"><span data-stu-id="9d35b-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="9d35b-226">Stofnað er tölfræðilegt víddarstak sem er nefnt Rafmagn og rafmagnsnotkun er skráð.</span><span class="sxs-lookup"><span data-stu-id="9d35b-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="9d35b-227">Sjálfgefið er að öll tölfræðileg víddarstök verða tiltæk sem úthlutunargrunnur.</span><span class="sxs-lookup"><span data-stu-id="9d35b-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9d35b-228">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-228">Cost object</span></span></th>
<th><span data-ttu-id="9d35b-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="9d35b-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-230">CC001</span><span class="sxs-lookup"><span data-stu-id="9d35b-230">CC001</span></span></td>
<td><span data-ttu-id="9d35b-231">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9d35b-231">HR</span></span></td>
<td><span data-ttu-id="9d35b-232">1.000</span><span class="sxs-lookup"><span data-stu-id="9d35b-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-233">CC002</span><span class="sxs-lookup"><span data-stu-id="9d35b-233">CC002</span></span></td>
<td><span data-ttu-id="9d35b-234">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9d35b-234">Finance</span></span></td>
<td><span data-ttu-id="9d35b-235">6,000</span><span class="sxs-lookup"><span data-stu-id="9d35b-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-236">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-236">CC003</span></span></td>
<td><span data-ttu-id="9d35b-237">Smölun</span><span class="sxs-lookup"><span data-stu-id="9d35b-237">Assembly</span></span></td>
<td><span data-ttu-id="9d35b-238">0</span><span class="sxs-lookup"><span data-stu-id="9d35b-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9d35b-239">Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunni fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="9d35b-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9d35b-240">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-240">Cost object</span></span></th>
<th><span data-ttu-id="9d35b-241">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="9d35b-241">Magnitude</span></span></th>
<th><span data-ttu-id="9d35b-242">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="9d35b-242">Allocation factor</span></span></th>
<th><span data-ttu-id="9d35b-243">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9d35b-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-244">CC001</span><span class="sxs-lookup"><span data-stu-id="9d35b-244">CC001</span></span></td>
<td><span data-ttu-id="9d35b-245">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9d35b-245">HR</span></span></td>
<td><span data-ttu-id="9d35b-246">1.000</span><span class="sxs-lookup"><span data-stu-id="9d35b-246">1,000</span></span></td>
<td><span data-ttu-id="9d35b-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="9d35b-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="9d35b-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-249">CC002</span><span class="sxs-lookup"><span data-stu-id="9d35b-249">CC002</span></span></td>
<td><span data-ttu-id="9d35b-250">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9d35b-250">Finance</span></span></td>
<td><span data-ttu-id="9d35b-251">6,000</span><span class="sxs-lookup"><span data-stu-id="9d35b-251">6,000</span></span></td>
<td><span data-ttu-id="9d35b-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="9d35b-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="9d35b-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-254">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-254">CC003</span></span></td>
<td><span data-ttu-id="9d35b-255">Smölun</span><span class="sxs-lookup"><span data-stu-id="9d35b-255">Assembly</span></span></td>
<td><span data-ttu-id="9d35b-256">0</span><span class="sxs-lookup"><span data-stu-id="9d35b-256">0</span></span></td>
<td><span data-ttu-id="9d35b-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="9d35b-258">0,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9d35b-259">Föstum kostnaði þarf að dreifa jafnt á staka kostnaðarhluti sem hafa notað rafmagn.</span><span class="sxs-lookup"><span data-stu-id="9d35b-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="9d35b-260">Hægt er að ná þessa niðurstöðu með því að nota tölfræðilegt víddarstakið Rafmagn í úthlutunargrunni reikniformúlu: (Rafmagn &gt; 0,00) Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunn fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="9d35b-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9d35b-261">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-261">Cost object</span></span></th>
<th><span data-ttu-id="9d35b-262">Formúla</span><span class="sxs-lookup"><span data-stu-id="9d35b-262">Formula</span></span></th>
<th><span data-ttu-id="9d35b-263">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="9d35b-263">Magnitude</span></span></th>
<th><span data-ttu-id="9d35b-264">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="9d35b-264">Allocation factor</span></span></th>
<th><span data-ttu-id="9d35b-265">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9d35b-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-266">CC001</span><span class="sxs-lookup"><span data-stu-id="9d35b-266">CC001</span></span></td>
<td><span data-ttu-id="9d35b-267">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9d35b-267">HR</span></span></td>
<td><span data-ttu-id="9d35b-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="9d35b-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="9d35b-269">1</span><span class="sxs-lookup"><span data-stu-id="9d35b-269">1</span></span></td>
<td><span data-ttu-id="9d35b-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="9d35b-271">500,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-272">CC002</span><span class="sxs-lookup"><span data-stu-id="9d35b-272">CC002</span></span></td>
<td><span data-ttu-id="9d35b-273">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9d35b-273">Finance</span></span></td>
<td><span data-ttu-id="9d35b-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="9d35b-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="9d35b-275">1</span><span class="sxs-lookup"><span data-stu-id="9d35b-275">1</span></span></td>
<td><span data-ttu-id="9d35b-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="9d35b-277">500,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-278">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-278">CC003</span></span></td>
<td><span data-ttu-id="9d35b-279">Smölun</span><span class="sxs-lookup"><span data-stu-id="9d35b-279">Assembly</span></span></td>
<td><span data-ttu-id="9d35b-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="9d35b-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="9d35b-281">0</span><span class="sxs-lookup"><span data-stu-id="9d35b-281">0</span></span></td>
<td><span data-ttu-id="9d35b-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="9d35b-283">0,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="9d35b-284">Færslubók</span><span class="sxs-lookup"><span data-stu-id="9d35b-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9d35b-285">Færslubók</span><span class="sxs-lookup"><span data-stu-id="9d35b-285">Journal</span></span></th>
<th><span data-ttu-id="9d35b-286">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="9d35b-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="9d35b-287">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="9d35b-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="9d35b-288">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="9d35b-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-289">00002</span><span class="sxs-lookup"><span data-stu-id="9d35b-289">00002</span></span></td>
<td><span data-ttu-id="9d35b-290">Útreikningabók kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="9d35b-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="9d35b-291">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="9d35b-291">Fiscal</span></span></td>
<td><span data-ttu-id="9d35b-292">2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-292">2017</span></span></td>
<td><span data-ttu-id="9d35b-293">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="9d35b-293">Period 1</span></span></td>
<td><span data-ttu-id="9d35b-294">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="9d35b-295">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="9d35b-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9d35b-296">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="9d35b-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9d35b-297">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9d35b-298">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9d35b-298">Cost element</span></span></th>
<th><span data-ttu-id="9d35b-299">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9d35b-299">Cost behavior</span></span></th>
<th><span data-ttu-id="9d35b-300">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9d35b-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-301">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="9d35b-302">CC099</span><span class="sxs-lookup"><span data-stu-id="9d35b-302">CC099</span></span></td>
<td><span data-ttu-id="9d35b-303">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9d35b-303">Default cost center</span></span></td>
<td><span data-ttu-id="9d35b-304">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-304">10001</span></span></td>
<td><span data-ttu-id="9d35b-305">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-305">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-306">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-306">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-308">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="9d35b-309">CC099</span><span class="sxs-lookup"><span data-stu-id="9d35b-309">CC099</span></span></td>
<td><span data-ttu-id="9d35b-310">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9d35b-310">Default cost center</span></span></td>
<td><span data-ttu-id="9d35b-311">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-311">10001</span></span></td>
<td><span data-ttu-id="9d35b-312">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-312">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-313">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-313">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="9d35b-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="9d35b-315">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="9d35b-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9d35b-316">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9d35b-317">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9d35b-317">Cost element</span></span></th>
<th><span data-ttu-id="9d35b-318">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9d35b-318">Cost behavior</span></span></th>
<th><span data-ttu-id="9d35b-319">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9d35b-319">Amount</span></span></th>
<th><span data-ttu-id="9d35b-320">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="9d35b-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-321">CC099</span><span class="sxs-lookup"><span data-stu-id="9d35b-321">CC099</span></span></td>
<td><span data-ttu-id="9d35b-322">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9d35b-322">Default cost center</span></span></td>
<td><span data-ttu-id="9d35b-323">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-323">10001</span></span></td>
<td><span data-ttu-id="9d35b-324">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-324">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-325">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-325">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-326">-1,000.00</span></span></td>
<td><span data-ttu-id="9d35b-327">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-328">CC001</span><span class="sxs-lookup"><span data-stu-id="9d35b-328">CC001</span></span></td>
<td><span data-ttu-id="9d35b-329">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9d35b-329">HR</span></span></td>
<td><span data-ttu-id="9d35b-330">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-330">10001</span></span></td>
<td><span data-ttu-id="9d35b-331">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-331">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-332">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-332">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-333">500,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-333">500.00</span></span></td>
<td><span data-ttu-id="9d35b-334">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-335">CC002</span><span class="sxs-lookup"><span data-stu-id="9d35b-335">CC002</span></span></td>
<td><span data-ttu-id="9d35b-336">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9d35b-336">Finance</span></span></td>
<td><span data-ttu-id="9d35b-337">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-337">10001</span></span></td>
<td><span data-ttu-id="9d35b-338">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-338">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-339">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-339">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-340">500,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-340">500.00</span></span></td>
<td><span data-ttu-id="9d35b-341">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-342">CC099</span><span class="sxs-lookup"><span data-stu-id="9d35b-342">CC099</span></span></td>
<td><span data-ttu-id="9d35b-343">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9d35b-343">Default cost center</span></span></td>
<td><span data-ttu-id="9d35b-344">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-344">10001</span></span></td>
<td><span data-ttu-id="9d35b-345">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-345">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-346">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-346">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-347">-9,000.00</span></span></td>
<td><span data-ttu-id="9d35b-348">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-349">CC001</span><span class="sxs-lookup"><span data-stu-id="9d35b-349">CC001</span></span></td>
<td><span data-ttu-id="9d35b-350">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9d35b-350">HR</span></span></td>
<td><span data-ttu-id="9d35b-351">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-351">10001</span></span></td>
<td><span data-ttu-id="9d35b-352">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-352">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-353">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-353">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="9d35b-354">1,285.71</span></span></td>
<td><span data-ttu-id="9d35b-355">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-356">CC002</span><span class="sxs-lookup"><span data-stu-id="9d35b-356">CC002</span></span></td>
<td><span data-ttu-id="9d35b-357">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9d35b-357">Finance</span></span></td>
<td><span data-ttu-id="9d35b-358">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-358">10001</span></span></td>
<td><span data-ttu-id="9d35b-359">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-359">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-360">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-360">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="9d35b-361">7,714.29</span></span></td>
<td><span data-ttu-id="9d35b-362">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9d35b-363">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðardreifingarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="9d35b-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="9d35b-364">Skref 3: Keyra útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="9d35b-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="9d35b-365">Sameiginlegur kostnaður er notaður til að rukka einn eða fleiri tilgreinda kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="9d35b-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="9d35b-366">Gjöldin byggjast á fyrirframákveðnu kostnaðarhlutfalli og mæligildi úr úthlutuðum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="9d35b-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="9d35b-367">Skilgreina sameiginlegan kostnað</span><span class="sxs-lookup"><span data-stu-id="9d35b-367">Define the overhead rate</span></span>

<span data-ttu-id="9d35b-368">Kostnaðarhlutur CC001 Mannauður stuðlar að safni innri verka.</span><span class="sxs-lookup"><span data-stu-id="9d35b-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="9d35b-369">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsverk til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="9d35b-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9d35b-370">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-370">Cost object</span></span></th>
<th><span data-ttu-id="9d35b-371">Tímar</span><span class="sxs-lookup"><span data-stu-id="9d35b-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-372">Verk 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-372">Proj 1</span></span></td>
<td><span data-ttu-id="9d35b-373">Verk 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-373">Project 1</span></span></td>
<td><span data-ttu-id="9d35b-374">3</span><span class="sxs-lookup"><span data-stu-id="9d35b-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-375">Verk 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-375">Proj 2</span></span></td>
<td><span data-ttu-id="9d35b-376">Verk 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-376">Project 2</span></span></td>
<td><span data-ttu-id="9d35b-377">1</span><span class="sxs-lookup"><span data-stu-id="9d35b-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9d35b-378">Fyrirframákveðið kostnaðarhlutfall fyrir kostnaðarframlag verk hefur verið skilgreint.</span><span class="sxs-lookup"><span data-stu-id="9d35b-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9d35b-379">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-379">Cost object</span></span></th>
<th><span data-ttu-id="9d35b-380">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9d35b-380">Cost element</span></span></th>
<th><span data-ttu-id="9d35b-381">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9d35b-381">Cost behavior</span></span></th>
<th><span data-ttu-id="9d35b-382">Einingar</span><span class="sxs-lookup"><span data-stu-id="9d35b-382">Units</span></span></th>
<th><span data-ttu-id="9d35b-383">Taxti</span><span class="sxs-lookup"><span data-stu-id="9d35b-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-384">CC001</span><span class="sxs-lookup"><span data-stu-id="9d35b-384">CC001</span></span></td>
<td><span data-ttu-id="9d35b-385">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9d35b-385">HR</span></span></td>
<td><span data-ttu-id="9d35b-386">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-386">10001</span></span></td>
<td><span data-ttu-id="9d35b-387">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-387">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-388">1</span><span class="sxs-lookup"><span data-stu-id="9d35b-388">1</span></span></td>
<td><span data-ttu-id="9d35b-389">10</span><span class="sxs-lookup"><span data-stu-id="9d35b-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9d35b-390">Eftirfarandi tafla sýnir niðurstöður þegar Mannauðsverk eru notuð sem grunnur við úthlutun.</span><span class="sxs-lookup"><span data-stu-id="9d35b-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9d35b-391">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-391">Cost object</span></span></th>
<th><span data-ttu-id="9d35b-392">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="9d35b-392">Magnitude</span></span></th>
<th><span data-ttu-id="9d35b-393">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9d35b-393">Cost element</span></span></th>
<th><span data-ttu-id="9d35b-394">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="9d35b-394">Allocation factor</span></span></th>
<th><span data-ttu-id="9d35b-395">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9d35b-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-396">Verk 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-396">Proj 1</span></span></td>
<td><span data-ttu-id="9d35b-397">Verk 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-397">Project 1</span></span></td>
<td><span data-ttu-id="9d35b-398">3</span><span class="sxs-lookup"><span data-stu-id="9d35b-398">3</span></span></td>
<td><span data-ttu-id="9d35b-399">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-399">10001</span></span></td>
<td><span data-ttu-id="9d35b-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="9d35b-401">30,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-402">Verk 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-402">Proj 2</span></span></td>
<td><span data-ttu-id="9d35b-403">Verk 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-403">Project 2</span></span></td>
<td><span data-ttu-id="9d35b-404">1</span><span class="sxs-lookup"><span data-stu-id="9d35b-404">1</span></span></td>
<td><span data-ttu-id="9d35b-405">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-405">10001</span></span></td>
<td><span data-ttu-id="9d35b-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="9d35b-407">10,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="9d35b-408">Færslubók</span><span class="sxs-lookup"><span data-stu-id="9d35b-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9d35b-409">Færslubók</span><span class="sxs-lookup"><span data-stu-id="9d35b-409">Journal</span></span></th>
<th><span data-ttu-id="9d35b-410">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="9d35b-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="9d35b-411">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="9d35b-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="9d35b-412">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="9d35b-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-413">00003</span><span class="sxs-lookup"><span data-stu-id="9d35b-413">00003</span></span></td>
<td><span data-ttu-id="9d35b-414">Færslubók fyrir útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="9d35b-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="9d35b-415">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="9d35b-415">Fiscal</span></span></td>
<td><span data-ttu-id="9d35b-416">2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-416">2017</span></span></td>
<td><span data-ttu-id="9d35b-417">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="9d35b-417">Period 1</span></span></td>
<td><span data-ttu-id="9d35b-418">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="9d35b-419">Bókarfærslur (Bókarfærslur fyrir útreikning sameiginlegs kostnaðar)</span><span class="sxs-lookup"><span data-stu-id="9d35b-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9d35b-420">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="9d35b-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9d35b-421">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-421">Cost object</span></span></th>
<th><span data-ttu-id="9d35b-422">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="9d35b-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-423">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="9d35b-424">Verk 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-424">Proj 1</span></span></td>
<td><span data-ttu-id="9d35b-425">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="9d35b-426">3,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-427">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="9d35b-428">Verk 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-428">Proj 2</span></span></td>
<td><span data-ttu-id="9d35b-429">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="9d35b-430">1,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="9d35b-431">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="9d35b-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9d35b-432">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9d35b-433">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9d35b-433">Cost element</span></span></th>
<th><span data-ttu-id="9d35b-434">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9d35b-434">Cost behavior</span></span></th>
<th><span data-ttu-id="9d35b-435">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9d35b-435">Amount</span></span></th>
<th><span data-ttu-id="9d35b-436">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="9d35b-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="9d35b-437">CC0001</span></span></td>
<td><span data-ttu-id="9d35b-438">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9d35b-438">HR</span></span></td>
<td><span data-ttu-id="9d35b-439">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-439">10001</span></span></td>
<td><span data-ttu-id="9d35b-440">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-440">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-441">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-441">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-442">-30.00</span></span></td>
<td><span data-ttu-id="9d35b-443">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-444">Verk 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-444">Proj 1</span></span></td>
<td><span data-ttu-id="9d35b-445">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="9d35b-446">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-446">10001</span></span></td>
<td><span data-ttu-id="9d35b-447">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-447">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-448">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-448">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-449">30,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-449">30.00</span></span></td>
<td><span data-ttu-id="9d35b-450">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-451">CC001</span><span class="sxs-lookup"><span data-stu-id="9d35b-451">CC001</span></span></td>
<td><span data-ttu-id="9d35b-452">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9d35b-452">HR</span></span></td>
<td><span data-ttu-id="9d35b-453">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-453">10001</span></span></td>
<td><span data-ttu-id="9d35b-454">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-454">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-455">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-455">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-456">-10.00</span></span></td>
<td><span data-ttu-id="9d35b-457">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-458">Verk 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-458">Proj 2</span></span></td>
<td><span data-ttu-id="9d35b-459">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="9d35b-460">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-460">10001</span></span></td>
<td><span data-ttu-id="9d35b-461">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-461">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-462">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-462">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-463">10,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-463">10.00</span></span></td>
<td><span data-ttu-id="9d35b-464">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9d35b-465">Nánari upplýsingar er að finna í [Framkvæma útreikning fastakostnaðar](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="9d35b-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="9d35b-466">Skref 4: Keyra útreikning kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="9d35b-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="9d35b-467">Úthlutun er notuð til að úthluta stöðu kostnaðarhlutar í öðrum kostnaðarhlutum með því að nota úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="9d35b-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="9d35b-468">Finance styður gagnvirka úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="9d35b-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="9d35b-469">Í gagnvirkri úthlutunaraðferð er sú sameiginlega þjónusta sem hjálparkostnaðarhlutir skiptast á viðurkennd að fullu.</span><span class="sxs-lookup"><span data-stu-id="9d35b-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="9d35b-470">Kerfið ákvarðar sjálfkrafa rétta röð til að framkvæma úthlutun eftir.</span><span class="sxs-lookup"><span data-stu-id="9d35b-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="9d35b-471">Stöðu kostnaðarhluta er úthlutað með einum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="9d35b-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="9d35b-472">Úthlutanir þvert á víddir kostnaðarhluta og viðkomandi stök þeirra eru studdar.</span><span class="sxs-lookup"><span data-stu-id="9d35b-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="9d35b-473">Úthlutun pöntunarinnar er stjórnað af stýrieiningu kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="9d35b-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="9d35b-474">[![Gagnkvæm aðferð](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="9d35b-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="9d35b-475">Tilgreinið kostnaðarúthlutun</span><span class="sxs-lookup"><span data-stu-id="9d35b-475">Define the cost allocation</span></span>

<span data-ttu-id="9d35b-476">Hér er einfalt dæmi sem útskýrir hvernig hægt er að rekja flæði kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="9d35b-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="9d35b-477">Kostnaðarhlutir CC001 Mannauður leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="9d35b-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="9d35b-478">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="9d35b-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9d35b-479">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-479">Cost object</span></span></th>
<th><span data-ttu-id="9d35b-480">Mannauðsþjónusta</span><span class="sxs-lookup"><span data-stu-id="9d35b-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-481">CC002</span><span class="sxs-lookup"><span data-stu-id="9d35b-481">CC002</span></span></td>
<td><span data-ttu-id="9d35b-482">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9d35b-482">Finance</span></span></td>
<td><span data-ttu-id="9d35b-483">35</span><span class="sxs-lookup"><span data-stu-id="9d35b-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-484">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-484">CC003</span></span></td>
<td><span data-ttu-id="9d35b-485">Smölun</span><span class="sxs-lookup"><span data-stu-id="9d35b-485">Assembly</span></span></td>
<td><span data-ttu-id="9d35b-486">55</span><span class="sxs-lookup"><span data-stu-id="9d35b-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-487">CC004</span><span class="sxs-lookup"><span data-stu-id="9d35b-487">CC004</span></span></td>
<td><span data-ttu-id="9d35b-488">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9d35b-488">Packaging</span></span></td>
<td><span data-ttu-id="9d35b-489">10</span><span class="sxs-lookup"><span data-stu-id="9d35b-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9d35b-490">Kostnaðarhlutir CC002 Fjármál leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="9d35b-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="9d35b-491">Stofnað er tölfræðilegt víddarstak sem kallast Fjármálaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="9d35b-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9d35b-492">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-492">Cost object</span></span></th>
<th><span data-ttu-id="9d35b-493">Fjármálaþjónusta</span><span class="sxs-lookup"><span data-stu-id="9d35b-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-494">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-494">CC003</span></span></td>
<td><span data-ttu-id="9d35b-495">Smölun</span><span class="sxs-lookup"><span data-stu-id="9d35b-495">Assembly</span></span></td>
<td><span data-ttu-id="9d35b-496">65</span><span class="sxs-lookup"><span data-stu-id="9d35b-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-497">CC004</span><span class="sxs-lookup"><span data-stu-id="9d35b-497">CC004</span></span></td>
<td><span data-ttu-id="9d35b-498">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9d35b-498">Packaging</span></span></td>
<td><span data-ttu-id="9d35b-499">35</span><span class="sxs-lookup"><span data-stu-id="9d35b-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9d35b-500">Kostnaðarhlutir CC003 Samsetning leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="9d35b-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="9d35b-501">Meðlimur tölfræðilega víddar sem kallast Mannauður verk er stofnað til að mælvíddarstaka notuðum magnitude.</span><span class="sxs-lookup"><span data-stu-id="9d35b-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9d35b-502">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-502">Cost object</span></span></th>
<th><span data-ttu-id="9d35b-503">Samsetningarþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="9d35b-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-504">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-504">Prod 1</span></span></td>
<td><span data-ttu-id="9d35b-505">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-505">Product 1</span></span></td>
<td><span data-ttu-id="9d35b-506">60</span><span class="sxs-lookup"><span data-stu-id="9d35b-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-507">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-507">Prod 2</span></span></td>
<td><span data-ttu-id="9d35b-508">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-508">Product 2</span></span></td>
<td><span data-ttu-id="9d35b-509">20</span><span class="sxs-lookup"><span data-stu-id="9d35b-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9d35b-510">Kostnaðarhlutir CC004 Umbúðir leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="9d35b-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="9d35b-511">Stofnað er tölfræðilegt víddarstak sem kallast Umbúðaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="9d35b-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9d35b-512">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-512">Cost object</span></span></th>
<th><span data-ttu-id="9d35b-513">Umbúðaþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="9d35b-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-514">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-514">Prod 1</span></span></td>
<td><span data-ttu-id="9d35b-515">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-515">Product 1</span></span></td>
<td><span data-ttu-id="9d35b-516">80</span><span class="sxs-lookup"><span data-stu-id="9d35b-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-517">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-517">Prod 2</span></span></td>
<td><span data-ttu-id="9d35b-518">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-518">Product 2</span></span></td>
<td><span data-ttu-id="9d35b-519">15</span><span class="sxs-lookup"><span data-stu-id="9d35b-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="9d35b-520">Hægt er að afleiða tölfræðiaðgerðir eins og framleiðslutíma sem vara notar frá upprunagögnum.</span><span class="sxs-lookup"><span data-stu-id="9d35b-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="9d35b-521">Nánari upplýsingar er að finna í [Veitusniðmát tölfræðiaðgerðar](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="9d35b-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="9d35b-522">Eftirfarandi tafla sýnir niðurstöður þegar mannauðsþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="9d35b-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9d35b-523">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-523">Cost object</span></span></th>
<th><span data-ttu-id="9d35b-524">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="9d35b-524">Magnitude</span></span></th>
<th><span data-ttu-id="9d35b-525">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="9d35b-525">Allocation factor</span></span></th>
<th><span data-ttu-id="9d35b-526">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9d35b-526">Amount</span></span></th>
<th><span data-ttu-id="9d35b-527">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9d35b-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-528">CC002</span><span class="sxs-lookup"><span data-stu-id="9d35b-528">CC002</span></span></td>
<td><span data-ttu-id="9d35b-529">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9d35b-529">Finance</span></span></td>
<td><span data-ttu-id="9d35b-530">35</span><span class="sxs-lookup"><span data-stu-id="9d35b-530">35</span></span></td>
<td><span data-ttu-id="9d35b-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="9d35b-532">175.00</span><span class="sxs-lookup"><span data-stu-id="9d35b-532">175.00</span></span></td>
<td><span data-ttu-id="9d35b-533">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-534">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-534">CC003</span></span></td>
<td><span data-ttu-id="9d35b-535">Smölun</span><span class="sxs-lookup"><span data-stu-id="9d35b-535">Assembly</span></span></td>
<td><span data-ttu-id="9d35b-536">55</span><span class="sxs-lookup"><span data-stu-id="9d35b-536">55</span></span></td>
<td><span data-ttu-id="9d35b-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="9d35b-538">275.00</span><span class="sxs-lookup"><span data-stu-id="9d35b-538">275.00</span></span></td>
<td><span data-ttu-id="9d35b-539">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-540">CC004</span><span class="sxs-lookup"><span data-stu-id="9d35b-540">CC004</span></span></td>
<td><span data-ttu-id="9d35b-541">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9d35b-541">Packaging</span></span></td>
<td><span data-ttu-id="9d35b-542">10</span><span class="sxs-lookup"><span data-stu-id="9d35b-542">10</span></span></td>
<td><span data-ttu-id="9d35b-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="9d35b-544">50,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-544">50.00</span></span></td>
<td><span data-ttu-id="9d35b-545">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-546">CC002</span><span class="sxs-lookup"><span data-stu-id="9d35b-546">CC002</span></span></td>
<td><span data-ttu-id="9d35b-547">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9d35b-547">Finance</span></span></td>
<td><span data-ttu-id="9d35b-548">35</span><span class="sxs-lookup"><span data-stu-id="9d35b-548">35</span></span></td>
<td><span data-ttu-id="9d35b-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="9d35b-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="9d35b-550">436.00</span><span class="sxs-lookup"><span data-stu-id="9d35b-550">436.00</span></span></td>
<td><span data-ttu-id="9d35b-551">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-552">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-552">CC003</span></span></td>
<td><span data-ttu-id="9d35b-553">Smölun</span><span class="sxs-lookup"><span data-stu-id="9d35b-553">Assembly</span></span></td>
<td><span data-ttu-id="9d35b-554">55</span><span class="sxs-lookup"><span data-stu-id="9d35b-554">55</span></span></td>
<td><span data-ttu-id="9d35b-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="9d35b-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="9d35b-556">685.14</span><span class="sxs-lookup"><span data-stu-id="9d35b-556">685.14</span></span></td>
<td><span data-ttu-id="9d35b-557">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-558">CC004</span><span class="sxs-lookup"><span data-stu-id="9d35b-558">CC004</span></span></td>
<td><span data-ttu-id="9d35b-559">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9d35b-559">Packaging</span></span></td>
<td><span data-ttu-id="9d35b-560">10</span><span class="sxs-lookup"><span data-stu-id="9d35b-560">10</span></span></td>
<td><span data-ttu-id="9d35b-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="9d35b-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="9d35b-562">124.57</span><span class="sxs-lookup"><span data-stu-id="9d35b-562">124.57</span></span></td>
<td><span data-ttu-id="9d35b-563">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9d35b-564">Eftirfarandi tafla sýnir niðurstöður þegar Fjármálaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="9d35b-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9d35b-565">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-565">Cost object</span></span></th>
<th><span data-ttu-id="9d35b-566">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="9d35b-566">Magnitude</span></span></th>
<th><span data-ttu-id="9d35b-567">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="9d35b-567">Allocation factor</span></span></th>
<th><span data-ttu-id="9d35b-568">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9d35b-568">Amount</span></span></th>
<th><span data-ttu-id="9d35b-569">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9d35b-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-570">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-570">CC003</span></span></td>
<td><span data-ttu-id="9d35b-571">Smölun</span><span class="sxs-lookup"><span data-stu-id="9d35b-571">Assembly</span></span></td>
<td><span data-ttu-id="9d35b-572">65</span><span class="sxs-lookup"><span data-stu-id="9d35b-572">65</span></span></td>
<td><span data-ttu-id="9d35b-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="9d35b-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="9d35b-574">438.75</span><span class="sxs-lookup"><span data-stu-id="9d35b-574">438.75</span></span></td>
<td><span data-ttu-id="9d35b-575">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-576">CC004</span><span class="sxs-lookup"><span data-stu-id="9d35b-576">CC004</span></span></td>
<td><span data-ttu-id="9d35b-577">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9d35b-577">Packaging</span></span></td>
<td><span data-ttu-id="9d35b-578">35</span><span class="sxs-lookup"><span data-stu-id="9d35b-578">35</span></span></td>
<td><span data-ttu-id="9d35b-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="9d35b-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="9d35b-580">236.25</span><span class="sxs-lookup"><span data-stu-id="9d35b-580">236.25</span></span></td>
<td><span data-ttu-id="9d35b-581">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-582">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-582">CC003</span></span></td>
<td><span data-ttu-id="9d35b-583">Smölun</span><span class="sxs-lookup"><span data-stu-id="9d35b-583">Assembly</span></span></td>
<td><span data-ttu-id="9d35b-584">65</span><span class="sxs-lookup"><span data-stu-id="9d35b-584">65</span></span></td>
<td><span data-ttu-id="9d35b-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="9d35b-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="9d35b-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="9d35b-586">5,297.69</span></span></td>
<td><span data-ttu-id="9d35b-587">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-588">CC004</span><span class="sxs-lookup"><span data-stu-id="9d35b-588">CC004</span></span></td>
<td><span data-ttu-id="9d35b-589">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9d35b-589">Packaging</span></span></td>
<td><span data-ttu-id="9d35b-590">35</span><span class="sxs-lookup"><span data-stu-id="9d35b-590">35</span></span></td>
<td><span data-ttu-id="9d35b-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="9d35b-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="9d35b-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="9d35b-592">2,852.60</span></span></td>
<td><span data-ttu-id="9d35b-593">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9d35b-594">Eftirfarandi tafla sýnir niðurstöður þegar Samsetningarþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="9d35b-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9d35b-595">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-595">Cost object</span></span></th>
<th><span data-ttu-id="9d35b-596">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="9d35b-596">Magnitude</span></span></th>
<th><span data-ttu-id="9d35b-597">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="9d35b-597">Allocation factor</span></span></th>
<th><span data-ttu-id="9d35b-598">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9d35b-598">Amount</span></span></th>
<th><span data-ttu-id="9d35b-599">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9d35b-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-600">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-600">Prod 1</span></span></td>
<td><span data-ttu-id="9d35b-601">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-601">Product 1</span></span></td>
<td><span data-ttu-id="9d35b-602">60</span><span class="sxs-lookup"><span data-stu-id="9d35b-602">60</span></span></td>
<td><span data-ttu-id="9d35b-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="9d35b-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="9d35b-604">535.31</span><span class="sxs-lookup"><span data-stu-id="9d35b-604">535.31</span></span></td>
<td><span data-ttu-id="9d35b-605">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-606">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-606">Prod 2</span></span></td>
<td><span data-ttu-id="9d35b-607">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-607">Product 2</span></span></td>
<td><span data-ttu-id="9d35b-608">20</span><span class="sxs-lookup"><span data-stu-id="9d35b-608">20</span></span></td>
<td><span data-ttu-id="9d35b-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="9d35b-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="9d35b-610">178.44</span><span class="sxs-lookup"><span data-stu-id="9d35b-610">178.44</span></span></td>
<td><span data-ttu-id="9d35b-611">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-612">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-612">Prod 1</span></span></td>
<td><span data-ttu-id="9d35b-613">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-613">Product 1</span></span></td>
<td><span data-ttu-id="9d35b-614">60</span><span class="sxs-lookup"><span data-stu-id="9d35b-614">60</span></span></td>
<td><span data-ttu-id="9d35b-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="9d35b-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="9d35b-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="9d35b-616">4,487.12</span></span></td>
<td><span data-ttu-id="9d35b-617">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-618">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-618">Prod 2</span></span></td>
<td><span data-ttu-id="9d35b-619">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-619">Product 2</span></span></td>
<td><span data-ttu-id="9d35b-620">20</span><span class="sxs-lookup"><span data-stu-id="9d35b-620">20</span></span></td>
<td><span data-ttu-id="9d35b-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="9d35b-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="9d35b-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="9d35b-622">1,495.71</span></span></td>
<td><span data-ttu-id="9d35b-623">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9d35b-624">Eftirfarandi tafla sýnir niðurstöður þegar Umbúðaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="9d35b-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9d35b-625">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-625">Cost object</span></span></th>
<th><span data-ttu-id="9d35b-626">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="9d35b-626">Magnitude</span></span></th>
<th><span data-ttu-id="9d35b-627">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="9d35b-627">Allocation factor</span></span></th>
<th><span data-ttu-id="9d35b-628">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9d35b-628">Amount</span></span></th>
<th><span data-ttu-id="9d35b-629">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9d35b-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-630">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-630">Prod 1</span></span></td>
<td><span data-ttu-id="9d35b-631">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-631">Product 1</span></span></td>
<td><span data-ttu-id="9d35b-632">80</span><span class="sxs-lookup"><span data-stu-id="9d35b-632">80</span></span></td>
<td><span data-ttu-id="9d35b-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="9d35b-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="9d35b-634">241.05</span><span class="sxs-lookup"><span data-stu-id="9d35b-634">241.05</span></span></td>
<td><span data-ttu-id="9d35b-635">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-636">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-636">Prod 2</span></span></td>
<td><span data-ttu-id="9d35b-637">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-637">Product 2</span></span></td>
<td><span data-ttu-id="9d35b-638">15</span><span class="sxs-lookup"><span data-stu-id="9d35b-638">15</span></span></td>
<td><span data-ttu-id="9d35b-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="9d35b-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="9d35b-640">45.20</span><span class="sxs-lookup"><span data-stu-id="9d35b-640">45.20</span></span></td>
<td><span data-ttu-id="9d35b-641">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-642">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-642">Prod 1</span></span></td>
<td><span data-ttu-id="9d35b-643">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-643">Product 1</span></span></td>
<td><span data-ttu-id="9d35b-644">80</span><span class="sxs-lookup"><span data-stu-id="9d35b-644">80</span></span></td>
<td><span data-ttu-id="9d35b-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="9d35b-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="9d35b-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="9d35b-646">2,507.09</span></span></td>
<td><span data-ttu-id="9d35b-647">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-648">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-648">Prod 2</span></span></td>
<td><span data-ttu-id="9d35b-649">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-649">Product 2</span></span></td>
<td><span data-ttu-id="9d35b-650">15</span><span class="sxs-lookup"><span data-stu-id="9d35b-650">15</span></span></td>
<td><span data-ttu-id="9d35b-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="9d35b-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="9d35b-652">470.08</span><span class="sxs-lookup"><span data-stu-id="9d35b-652">470.08</span></span></td>
<td><span data-ttu-id="9d35b-653">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="9d35b-654">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="9d35b-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9d35b-655">Færslubók</span><span class="sxs-lookup"><span data-stu-id="9d35b-655">Journal</span></span></th>
<th><span data-ttu-id="9d35b-656">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="9d35b-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="9d35b-657">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="9d35b-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="9d35b-658">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="9d35b-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-659">00004</span><span class="sxs-lookup"><span data-stu-id="9d35b-659">00004</span></span></td>
<td><span data-ttu-id="9d35b-660">Færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="9d35b-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="9d35b-661">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="9d35b-661">Fiscal</span></span></td>
<td><span data-ttu-id="9d35b-662">2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-662">2017</span></span></td>
<td><span data-ttu-id="9d35b-663">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="9d35b-663">Period 1</span></span></td>
<td><span data-ttu-id="9d35b-664">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="9d35b-665">Færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="9d35b-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9d35b-666">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="9d35b-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9d35b-667">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9d35b-668">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9d35b-668">Cost element</span></span></th>
<th><span data-ttu-id="9d35b-669">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9d35b-669">Cost behavior</span></span></th>
<th><span data-ttu-id="9d35b-670">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9d35b-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-671">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="9d35b-672">CC001</span><span class="sxs-lookup"><span data-stu-id="9d35b-672">CC001</span></span></td>
<td><span data-ttu-id="9d35b-673">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9d35b-673">HR</span></span></td>
<td><span data-ttu-id="9d35b-674">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-674">10001</span></span></td>
<td><span data-ttu-id="9d35b-675">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-675">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-676">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-676">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-677">500,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-678">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="9d35b-679">CC001</span><span class="sxs-lookup"><span data-stu-id="9d35b-679">CC001</span></span></td>
<td><span data-ttu-id="9d35b-680">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9d35b-680">HR</span></span></td>
<td><span data-ttu-id="9d35b-681">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-681">10001</span></span></td>
<td><span data-ttu-id="9d35b-682">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-682">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-683">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-683">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="9d35b-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-685">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="9d35b-686">CC002</span><span class="sxs-lookup"><span data-stu-id="9d35b-686">CC002</span></span></td>
<td><span data-ttu-id="9d35b-687">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9d35b-687">Finance</span></span></td>
<td><span data-ttu-id="9d35b-688">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-688">10001</span></span></td>
<td><span data-ttu-id="9d35b-689">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-689">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-690">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-690">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-691">675.00</span><span class="sxs-lookup"><span data-stu-id="9d35b-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-692">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="9d35b-693">CC002</span><span class="sxs-lookup"><span data-stu-id="9d35b-693">CC002</span></span></td>
<td><span data-ttu-id="9d35b-694">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9d35b-694">Finance</span></span></td>
<td><span data-ttu-id="9d35b-695">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-695">10001</span></span></td>
<td><span data-ttu-id="9d35b-696">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-696">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-697">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-697">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="9d35b-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-699">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="9d35b-700">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-700">CC003</span></span></td>
<td><span data-ttu-id="9d35b-701">Smölun</span><span class="sxs-lookup"><span data-stu-id="9d35b-701">Assembly</span></span></td>
<td><span data-ttu-id="9d35b-702">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-702">10001</span></span></td>
<td><span data-ttu-id="9d35b-703">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-703">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-704">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-704">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-705">713.75</span><span class="sxs-lookup"><span data-stu-id="9d35b-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-706">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="9d35b-707">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-707">CC003</span></span></td>
<td><span data-ttu-id="9d35b-708">Smölun</span><span class="sxs-lookup"><span data-stu-id="9d35b-708">Assembly</span></span></td>
<td><span data-ttu-id="9d35b-709">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-709">10001</span></span></td>
<td><span data-ttu-id="9d35b-710">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-710">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-711">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-711">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="9d35b-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-713">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="9d35b-714">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-714">CC003</span></span></td>
<td><span data-ttu-id="9d35b-715">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9d35b-715">Packaging</span></span></td>
<td><span data-ttu-id="9d35b-716">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-716">10001</span></span></td>
<td><span data-ttu-id="9d35b-717">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-717">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-718">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-718">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-719">286.25</span><span class="sxs-lookup"><span data-stu-id="9d35b-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-720">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="9d35b-721">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-721">CC003</span></span></td>
<td><span data-ttu-id="9d35b-722">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9d35b-722">Packaging</span></span></td>
<td><span data-ttu-id="9d35b-723">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-723">10001</span></span></td>
<td><span data-ttu-id="9d35b-724">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-724">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-725">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-725">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="9d35b-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-727">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="9d35b-728">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-728">Prod 1</span></span></td>
<td><span data-ttu-id="9d35b-729">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-729">Product 1</span></span></td>
<td><span data-ttu-id="9d35b-730">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-730">10001</span></span></td>
<td><span data-ttu-id="9d35b-731">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-731">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-732">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-732">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-733">776.36</span><span class="sxs-lookup"><span data-stu-id="9d35b-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-734">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="9d35b-735">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-735">Prod 1</span></span></td>
<td><span data-ttu-id="9d35b-736">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-736">Product 1</span></span></td>
<td><span data-ttu-id="9d35b-737">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-737">10001</span></span></td>
<td><span data-ttu-id="9d35b-738">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-738">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-739">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-739">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="9d35b-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-741">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="9d35b-742">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-742">Prod 2</span></span></td>
<td><span data-ttu-id="9d35b-743">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-743">Product 1</span></span></td>
<td><span data-ttu-id="9d35b-744">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-744">10001</span></span></td>
<td><span data-ttu-id="9d35b-745">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-745">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-746">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-746">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-747">223.64</span><span class="sxs-lookup"><span data-stu-id="9d35b-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-748">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="9d35b-749">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-749">Prod 2</span></span></td>
<td><span data-ttu-id="9d35b-750">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-750">Product 1</span></span></td>
<td><span data-ttu-id="9d35b-751">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-751">10001</span></span></td>
<td><span data-ttu-id="9d35b-752">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-752">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-753">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-753">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="9d35b-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="9d35b-755">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="9d35b-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9d35b-756">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9d35b-757">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9d35b-757">Cost element</span></span></th>
<th><span data-ttu-id="9d35b-758">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9d35b-758">Cost behavior</span></span></th>
<th><span data-ttu-id="9d35b-759">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9d35b-759">Amount</span></span></th>
<th><span data-ttu-id="9d35b-760">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="9d35b-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9d35b-761">CC001</span><span class="sxs-lookup"><span data-stu-id="9d35b-761">CC001</span></span></td>
<td><span data-ttu-id="9d35b-762">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9d35b-762">HR</span></span></td>
<td><span data-ttu-id="9d35b-763">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-763">10001</span></span></td>
<td><span data-ttu-id="9d35b-764">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-764">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-765">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-765">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-766">-500.00</span></span></td>
<td><span data-ttu-id="9d35b-767">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-768">CC002</span><span class="sxs-lookup"><span data-stu-id="9d35b-768">CC002</span></span></td>
<td><span data-ttu-id="9d35b-769">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9d35b-769">Finance</span></span></td>
<td><span data-ttu-id="9d35b-770">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-770">10001</span></span></td>
<td><span data-ttu-id="9d35b-771">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-771">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-772">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-772">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-773">175.00</span><span class="sxs-lookup"><span data-stu-id="9d35b-773">175.00</span></span></td>
<td><span data-ttu-id="9d35b-774">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-775">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-775">CC003</span></span></td>
<td><span data-ttu-id="9d35b-776">Smölun</span><span class="sxs-lookup"><span data-stu-id="9d35b-776">Assembly</span></span></td>
<td><span data-ttu-id="9d35b-777">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-777">10001</span></span></td>
<td><span data-ttu-id="9d35b-778">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-778">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-779">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-779">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-780">275.00</span><span class="sxs-lookup"><span data-stu-id="9d35b-780">275.00</span></span></td>
<td><span data-ttu-id="9d35b-781">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-782">CC004</span><span class="sxs-lookup"><span data-stu-id="9d35b-782">CC004</span></span></td>
<td><span data-ttu-id="9d35b-783">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9d35b-783">Packaging</span></span></td>
<td><span data-ttu-id="9d35b-784">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-784">10001</span></span></td>
<td><span data-ttu-id="9d35b-785">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-785">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-786">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-786">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-787">50,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-787">50,00</span></span></td>
<td><span data-ttu-id="9d35b-788">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-789">CC001</span><span class="sxs-lookup"><span data-stu-id="9d35b-789">CC001</span></span></td>
<td><span data-ttu-id="9d35b-790">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9d35b-790">HR</span></span></td>
<td><span data-ttu-id="9d35b-791">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-791">10001</span></span></td>
<td><span data-ttu-id="9d35b-792">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-792">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-793">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-793">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="9d35b-794">-1,245.71</span></span></td>
<td><span data-ttu-id="9d35b-795">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-796">CC002</span><span class="sxs-lookup"><span data-stu-id="9d35b-796">CC002</span></span></td>
<td><span data-ttu-id="9d35b-797">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9d35b-797">Finance</span></span></td>
<td><span data-ttu-id="9d35b-798">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-798">10001</span></span></td>
<td><span data-ttu-id="9d35b-799">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-799">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-800">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-800">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-801">436.00</span><span class="sxs-lookup"><span data-stu-id="9d35b-801">436.00</span></span></td>
<td><span data-ttu-id="9d35b-802">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-803">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-803">CC003</span></span></td>
<td><span data-ttu-id="9d35b-804">Smölun</span><span class="sxs-lookup"><span data-stu-id="9d35b-804">Assembly</span></span></td>
<td><span data-ttu-id="9d35b-805">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-805">10001</span></span></td>
<td><span data-ttu-id="9d35b-806">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-806">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-807">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-807">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-808">685.14</span><span class="sxs-lookup"><span data-stu-id="9d35b-808">685.14</span></span></td>
<td><span data-ttu-id="9d35b-809">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-810">CC004</span><span class="sxs-lookup"><span data-stu-id="9d35b-810">CC004</span></span></td>
<td><span data-ttu-id="9d35b-811">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9d35b-811">Packaging</span></span></td>
<td><span data-ttu-id="9d35b-812">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-812">10001</span></span></td>
<td><span data-ttu-id="9d35b-813">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-813">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-814">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-814">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-815">124.57</span><span class="sxs-lookup"><span data-stu-id="9d35b-815">124.57</span></span></td>
<td><span data-ttu-id="9d35b-816">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-817">CC002</span><span class="sxs-lookup"><span data-stu-id="9d35b-817">CC002</span></span></td>
<td><span data-ttu-id="9d35b-818">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9d35b-818">Finance</span></span></td>
<td><span data-ttu-id="9d35b-819">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-819">10001</span></span></td>
<td><span data-ttu-id="9d35b-820">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-820">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-821">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-821">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-822">-675.00</span></span></td>
<td><span data-ttu-id="9d35b-823">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-824">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-824">CC003</span></span></td>
<td><span data-ttu-id="9d35b-825">Smölun</span><span class="sxs-lookup"><span data-stu-id="9d35b-825">Assembly</span></span></td>
<td><span data-ttu-id="9d35b-826">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-826">10001</span></span></td>
<td><span data-ttu-id="9d35b-827">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-827">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-828">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-828">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-829">438.75</span><span class="sxs-lookup"><span data-stu-id="9d35b-829">438.75</span></span></td>
<td><span data-ttu-id="9d35b-830">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-831">CC004</span><span class="sxs-lookup"><span data-stu-id="9d35b-831">CC004</span></span></td>
<td><span data-ttu-id="9d35b-832">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9d35b-832">Packaging</span></span></td>
<td><span data-ttu-id="9d35b-833">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-833">10001</span></span></td>
<td><span data-ttu-id="9d35b-834">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-834">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-835">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-835">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-836">236.25</span><span class="sxs-lookup"><span data-stu-id="9d35b-836">236.25</span></span></td>
<td><span data-ttu-id="9d35b-837">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-838">CC002</span><span class="sxs-lookup"><span data-stu-id="9d35b-838">CC002</span></span></td>
<td><span data-ttu-id="9d35b-839">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9d35b-839">Finance</span></span></td>
<td><span data-ttu-id="9d35b-840">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-840">10001</span></span></td>
<td><span data-ttu-id="9d35b-841">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-841">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-842">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-842">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="9d35b-843">-8,150.29</span></span></td>
<td><span data-ttu-id="9d35b-844">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-845">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-845">CC003</span></span></td>
<td><span data-ttu-id="9d35b-846">Smölun</span><span class="sxs-lookup"><span data-stu-id="9d35b-846">Assembly</span></span></td>
<td><span data-ttu-id="9d35b-847">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-847">10001</span></span></td>
<td><span data-ttu-id="9d35b-848">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-848">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-849">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-849">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="9d35b-850">5,297.69</span></span></td>
<td><span data-ttu-id="9d35b-851">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-852">CC004</span><span class="sxs-lookup"><span data-stu-id="9d35b-852">CC004</span></span></td>
<td><span data-ttu-id="9d35b-853">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9d35b-853">Packaging</span></span></td>
<td><span data-ttu-id="9d35b-854">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-854">10001</span></span></td>
<td><span data-ttu-id="9d35b-855">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-855">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-856">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-856">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="9d35b-857">2,852.60</span></span></td>
<td><span data-ttu-id="9d35b-858">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-859">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-859">CC003</span></span></td>
<td><span data-ttu-id="9d35b-860">Smölun</span><span class="sxs-lookup"><span data-stu-id="9d35b-860">Assembly</span></span></td>
<td><span data-ttu-id="9d35b-861">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-861">10001</span></span></td>
<td><span data-ttu-id="9d35b-862">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-862">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-863">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-863">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="9d35b-864">-713.75</span></span></td>
<td><span data-ttu-id="9d35b-865">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-866">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-866">Prod 1</span></span></td>
<td><span data-ttu-id="9d35b-867">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-867">Product 1</span></span></td>
<td><span data-ttu-id="9d35b-868">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-868">10001</span></span></td>
<td><span data-ttu-id="9d35b-869">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-869">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-870">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-870">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-871">535.31</span><span class="sxs-lookup"><span data-stu-id="9d35b-871">535.31</span></span></td>
<td><span data-ttu-id="9d35b-872">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-873">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-873">Prod 2</span></span></td>
<td><span data-ttu-id="9d35b-874">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-874">Product 2</span></span></td>
<td><span data-ttu-id="9d35b-875">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-875">10001</span></span></td>
<td><span data-ttu-id="9d35b-876">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-876">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-877">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-877">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-878">178.44</span><span class="sxs-lookup"><span data-stu-id="9d35b-878">178.44</span></span></td>
<td><span data-ttu-id="9d35b-879">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-880">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-880">CC003</span></span></td>
<td><span data-ttu-id="9d35b-881">Smölun</span><span class="sxs-lookup"><span data-stu-id="9d35b-881">Assembly</span></span></td>
<td><span data-ttu-id="9d35b-882">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-882">10001</span></span></td>
<td><span data-ttu-id="9d35b-883">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-883">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-884">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-884">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="9d35b-885">-5,982.83</span></span></td>
<td><span data-ttu-id="9d35b-886">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-887">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-887">Prod 1</span></span></td>
<td><span data-ttu-id="9d35b-888">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-888">Product 1</span></span></td>
<td><span data-ttu-id="9d35b-889">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-889">10001</span></span></td>
<td><span data-ttu-id="9d35b-890">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-890">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-891">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-891">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="9d35b-892">4,487.12</span></span></td>
<td><span data-ttu-id="9d35b-893">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-894">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-894">Prod 2</span></span></td>
<td><span data-ttu-id="9d35b-895">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-895">Product 2</span></span></td>
<td><span data-ttu-id="9d35b-896">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-896">10001</span></span></td>
<td><span data-ttu-id="9d35b-897">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-897">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-898">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-898">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="9d35b-899">1,495.71</span></span></td>
<td><span data-ttu-id="9d35b-900">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-901">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-901">CC003</span></span></td>
<td><span data-ttu-id="9d35b-902">Smölun</span><span class="sxs-lookup"><span data-stu-id="9d35b-902">Assembly</span></span></td>
<td><span data-ttu-id="9d35b-903">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-903">10001</span></span></td>
<td><span data-ttu-id="9d35b-904">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-904">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-905">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-905">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="9d35b-906">-286.25</span></span></td>
<td><span data-ttu-id="9d35b-907">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-908">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-908">Prod 1</span></span></td>
<td><span data-ttu-id="9d35b-909">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-909">Product 1</span></span></td>
<td><span data-ttu-id="9d35b-910">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-910">10001</span></span></td>
<td><span data-ttu-id="9d35b-911">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-911">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-912">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-912">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-913">241.05</span><span class="sxs-lookup"><span data-stu-id="9d35b-913">241.05</span></span></td>
<td><span data-ttu-id="9d35b-914">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-915">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-915">Prod 2</span></span></td>
<td><span data-ttu-id="9d35b-916">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-916">Product 2</span></span></td>
<td><span data-ttu-id="9d35b-917">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-917">10001</span></span></td>
<td><span data-ttu-id="9d35b-918">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-918">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-919">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-919">Fixed cost</span></span></td>
<td><span data-ttu-id="9d35b-920">45.20</span><span class="sxs-lookup"><span data-stu-id="9d35b-920">45.20</span></span></td>
<td><span data-ttu-id="9d35b-921">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-922">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-922">CC003</span></span></td>
<td><span data-ttu-id="9d35b-923">Smölun</span><span class="sxs-lookup"><span data-stu-id="9d35b-923">Assembly</span></span></td>
<td><span data-ttu-id="9d35b-924">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-924">10001</span></span></td>
<td><span data-ttu-id="9d35b-925">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-925">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-926">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-926">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="9d35b-927">-2,977.17</span></span></td>
<td><span data-ttu-id="9d35b-928">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-929">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-929">Prod 1</span></span></td>
<td><span data-ttu-id="9d35b-930">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-930">Product 1</span></span></td>
<td><span data-ttu-id="9d35b-931">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-931">10001</span></span></td>
<td><span data-ttu-id="9d35b-932">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-932">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-933">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-933">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="9d35b-934">2,507.09</span></span></td>
<td><span data-ttu-id="9d35b-935">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9d35b-936">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-936">Prod 2</span></span></td>
<td><span data-ttu-id="9d35b-937">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-937">Product 2</span></span></td>
<td><span data-ttu-id="9d35b-938">10001</span><span class="sxs-lookup"><span data-stu-id="9d35b-938">10001</span></span></td>
<td><span data-ttu-id="9d35b-939">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-939">Electricity</span></span></td>
<td><span data-ttu-id="9d35b-940">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-940">Variable cost</span></span></td>
<td><span data-ttu-id="9d35b-941">470.08</span><span class="sxs-lookup"><span data-stu-id="9d35b-941">470.08</span></span></td>
<td><span data-ttu-id="9d35b-942">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9d35b-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="9d35b-943">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="9d35b-943">Conclusion</span></span>
<span data-ttu-id="9d35b-944">Í Fjárhagsbókhaldi er kostnaður upp á 10.000,00 fyrir rafmagn bókaður á kenni leppkostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="9d35b-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="9d35b-945">Þar af leiðandi munu kostnaðarbókarar vita að það þarf að úthluta þessum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="9d35b-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="9d35b-946">Í kostnaðarbókhaldi streymir kostnaður þvert á fyrirtækiseiningar og stig, samkvæmt þeim stefnum og reglum sem eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="9d35b-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="9d35b-947">Hver kostnaður hefur verið tengdur úthlutunargrunni sem veitir besta mat á úthlutun á kostnaði.</span><span class="sxs-lookup"><span data-stu-id="9d35b-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="9d35b-948">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9d35b-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="9d35b-949">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9d35b-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="9d35b-950">Samtala</span><span class="sxs-lookup"><span data-stu-id="9d35b-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="9d35b-951">CC099</span><span class="sxs-lookup"><span data-stu-id="9d35b-951">CC099</span></span></th>
<th><span data-ttu-id="9d35b-952">CC001</span><span class="sxs-lookup"><span data-stu-id="9d35b-952">CC001</span></span></th>
<th><span data-ttu-id="9d35b-953">CC002</span><span class="sxs-lookup"><span data-stu-id="9d35b-953">CC002</span></span></th>
<th><span data-ttu-id="9d35b-954">CC003</span><span class="sxs-lookup"><span data-stu-id="9d35b-954">CC003</span></span></th>
<th><span data-ttu-id="9d35b-955">CC004</span><span class="sxs-lookup"><span data-stu-id="9d35b-955">CC004</span></span></th>
<th><span data-ttu-id="9d35b-956">Verk 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-956">Proj 1</span></span></th>
<th><span data-ttu-id="9d35b-957">Verk 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-957">Proj 2</span></span></th>
<th><span data-ttu-id="9d35b-958">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9d35b-958">Prod 1</span></span></th>
<th><span data-ttu-id="9d35b-959">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9d35b-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="9d35b-960">10001 Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9d35b-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="9d35b-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="9d35b-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="9d35b-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="9d35b-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="9d35b-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="9d35b-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="9d35b-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="9d35b-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="9d35b-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="9d35b-970">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="9d35b-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-971">0,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="9d35b-972">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-973">0,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-974">0,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-975">0,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-976">0,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-977">0,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-978">776.36</span><span class="sxs-lookup"><span data-stu-id="9d35b-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-979">223.64</span><span class="sxs-lookup"><span data-stu-id="9d35b-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="9d35b-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="9d35b-981">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9d35b-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-982">000</span><span class="sxs-lookup"><span data-stu-id="9d35b-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-983">0,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-984">0,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-985">0,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-986">0,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-987">30,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-988">10,00</span><span class="sxs-lookup"><span data-stu-id="9d35b-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="9d35b-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="9d35b-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9d35b-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="9d35b-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="9d35b-992">Þetta efnisatriði sýnir hvernig fyrir aðalkostnaðareiningin 10001 Rafmagn flæðir í gegnum kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="9d35b-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="9d35b-993">Þar af leiðandi er þessum sameiginlega kostnaði úthlutað á lægsta stigið í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="9d35b-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="9d35b-994">Með öðrum orðum bera kostnaðarhlutir á lægsta stiginu kostnaðinn.</span><span class="sxs-lookup"><span data-stu-id="9d35b-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="9d35b-995">Ef þú þarft sjónrænt flæði kostnaðar á milli kostnaðarhluta er hægt að nota stefnureglur samantekins kostnaðar til að gera kostnaðarflæðið sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="9d35b-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="9d35b-996">Fyrir frekari upplýsingar skal sjá [Stefna fyrir samantekt kostnaðar og útreikning sameiginlegs kostnaðar](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="9d35b-996">For more information, see [Cost rollup policy and overhead calculation](cost-rollup.md).</span></span>



