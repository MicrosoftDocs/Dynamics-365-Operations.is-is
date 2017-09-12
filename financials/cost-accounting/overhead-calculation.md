---
title: "Útreikningur fastakostnaður"
description: "Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði."
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMActualVersion, CAMBudgetVersion, CAMOverheadCalculation
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 1eb5560ba795ab6df61b5af889049810dd00d79e
ms.contentlocale: is-is
ms.lasthandoff: 06/29/2017


---

# <a name="overhead-calculation"></a><span data-ttu-id="5f648-103">Útreikningur fastakostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-103">Overhead calculation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5f648-104">Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði.</span><span class="sxs-lookup"><span data-stu-id="5f648-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="5f648-105">Skýrsluskilgreining</span><span class="sxs-lookup"><span data-stu-id="5f648-105">Term definition</span></span>
---------------

<span data-ttu-id="5f648-106">Stjórnunarkostnaður er sá kostnaður sem stofnað er til fyrir rekstur fyrirtækis, en sem ekki er hægt að rekja beint til neinna sérstakrar starfsemi, vöru eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="5f648-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="5f648-107">Stjórnunarkostnaður veitir mikilvægan stuðning við myndun hagnaðarmyndandi verkþátta.</span><span class="sxs-lookup"><span data-stu-id="5f648-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="5f648-108">Hér eru nokkur dæmi um skilyrði:</span><span class="sxs-lookup"><span data-stu-id="5f648-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="5f648-109">Leiga</span><span class="sxs-lookup"><span data-stu-id="5f648-109">Rent</span></span>
-   <span data-ttu-id="5f648-110">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-110">Electricity</span></span>
-   <span data-ttu-id="5f648-111">Stjórnunarkostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="5f648-112">Yfirlit yfir útreikning fastakostnaðar</span><span class="sxs-lookup"><span data-stu-id="5f648-112">Overhead calculation overview</span></span>
<span data-ttu-id="5f648-113">Útreikningur fastakostnaðar keyrir reglur kostnaðarbókhalds í réttri röð.</span><span class="sxs-lookup"><span data-stu-id="5f648-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="5f648-114">Hægt er að keyra útreikning fastakostnaðar margsinnis fyrir sama fjárhagstímabil ef reglum kostnaðarbókhalds hefur verið breytt eða ákveðnar villur hafa fundist.</span><span class="sxs-lookup"><span data-stu-id="5f648-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="5f648-115">Hver keyrsla á útreikningi fastakostnaðar er geymd og fær einkvæmt útgáfukenni sem gerir kleift að bera saman útreikning í mismunandi útgáfum.</span><span class="sxs-lookup"><span data-stu-id="5f648-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="5f648-116">Kostnaðarfærslur sem útreikningur fastakostnaðar mynda fá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="5f648-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="5f648-117">Dagsetningin bókhald samsvarar lokadagsetning fjárhagstímabilsins sem er dagsetning reikningsskiladagsetning reikningsskila notað í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="5f648-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="5f648-118">Einkvæmt útgáfukenni samanstendur af eftirfarandi þáttum:</span><span class="sxs-lookup"><span data-stu-id="5f648-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="5f648-119">Gerð útgáfu</span><span class="sxs-lookup"><span data-stu-id="5f648-119">Version type</span></span>
-   <span data-ttu-id="5f648-120">Dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="5f648-120">Date and time</span></span>
-   <span data-ttu-id="5f648-121">Fjárhagur kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="5f648-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="5f648-122">Fjárhagsár</span><span class="sxs-lookup"><span data-stu-id="5f648-122">Fiscal year</span></span>
-   <span data-ttu-id="5f648-123">Reikningstímabil</span><span class="sxs-lookup"><span data-stu-id="5f648-123">Fiscal period</span></span>

<span data-ttu-id="5f648-124">Útreikningur fastakostnaðar er keyrður óháð því hver útgáfan er.</span><span class="sxs-lookup"><span data-stu-id="5f648-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="5f648-125">Þess vegna er hægt að reikna út áætlaða útgáfu á undan raunútgáfu.</span><span class="sxs-lookup"><span data-stu-id="5f648-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="5f648-126">Útreikningur fastakostnaðar samanstendur af fjórum skrefum, eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="5f648-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="5f648-127">Í hverju skrefi er færslubókarhaus stofnaður með bókarfærslum.</span><span class="sxs-lookup"><span data-stu-id="5f648-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="5f648-128">Þessi færslubókarhaus geymir inntaksgögn fyrir hvert útreikningsþrep.</span><span class="sxs-lookup"><span data-stu-id="5f648-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="5f648-129">Stefnur og reglur eru notaðar í hverri færslulínu og kostnaðarfærslur eru myndaðar sem úttak.</span><span class="sxs-lookup"><span data-stu-id="5f648-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="5f648-130">Þess vegna hefurðu ávallt fullan rekjanleika.</span><span class="sxs-lookup"><span data-stu-id="5f648-130">Therefore, you always have full traceability.</span></span> 
<span data-ttu-id="5f648-131">[![Útreikningur fastakostnaðar](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="5f648-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="5f648-132">Reikna og úthluta sameiginlegur kostnaði vegna rafmagns</span><span class="sxs-lookup"><span data-stu-id="5f648-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="5f648-133">Í Fjárhagsbókhaldi er ákveðinn kostnaður, eins og rafmagn, skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="5f648-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="5f648-134">Þar af leiðandi er nákvæmar innsýn rekstrarfélags ekki veitt fyrir kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="5f648-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="5f648-135">Í kostnaðarbókhaldi verður kostnaður að flæða í gegnum fyrirtækiseiningar til að veita rétta innsýn rekstrarfélags þvert á allar fyrirtækiseiningar og stig.</span><span class="sxs-lookup"><span data-stu-id="5f648-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="5f648-136">Þetta flæði verður að byggja á annaðhvort nákvæmri færslu notkunar eða sanngjarnri matsreglu.</span><span class="sxs-lookup"><span data-stu-id="5f648-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="5f648-137">Í fjárhagnum er hægt að bóka rafmagnskostnað eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="5f648-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5f648-138">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="5f648-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5f648-139">Kostnaðarstaður</span><span class="sxs-lookup"><span data-stu-id="5f648-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="5f648-140">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="5f648-140">Main account</span></span></th>
<th><span data-ttu-id="5f648-141">Upphæð í bókhaldsgjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="5f648-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-142">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="5f648-143">CC099</span><span class="sxs-lookup"><span data-stu-id="5f648-143">CC099</span></span></td>
<td><span data-ttu-id="5f648-144">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="5f648-144">Default cost center</span></span></td>
<td><span data-ttu-id="5f648-145">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-145">10001</span></span></td>
<td><span data-ttu-id="5f648-146">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-146">Electricity</span></span></td>
<td><span data-ttu-id="5f648-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="5f648-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="5f648-148">Skref 1: Keyra útreikning kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="5f648-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="5f648-149">Sjálfvirkt er að þegar kostnaðarfærslur eru fluttar úr grunngögnum fái þær flokkun kostnaðarhegðunar **Óflokkað** í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="5f648-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="5f648-150">Með því að nota stefnureglur kostnaðarhegðunar er hægt að endurflokka kostnaðarfærslur sem annaðhvort **Fastan kostnað** eða **Breytilegan kostnað**.</span><span class="sxs-lookup"><span data-stu-id="5f648-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="5f648-151">Tilgreinið reglu kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="5f648-151">Define the cost behavior rule</span></span>

<span data-ttu-id="5f648-152">Í sumum tilfellum er hluti af kostnaði föst þóknun og eftirstandandi kostnaður byggist á notkun.</span><span class="sxs-lookup"><span data-stu-id="5f648-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="5f648-153">Rafmagnsreikningar stemma oft við þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="5f648-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="5f648-154">Þegar tiltekin föst þóknun hefur verið greidd, er greitt fyrir notkun á kílóvattklukkustund (Kwh).</span><span class="sxs-lookup"><span data-stu-id="5f648-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="5f648-155">Til dæmis ef föst kostnaðarþóknun er 1000.00 sýnir þetta hvernig regla kostnaðarhegðunar er skilgreind:</span><span class="sxs-lookup"><span data-stu-id="5f648-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="5f648-156">Föst upphæð 1.000,00</span><span class="sxs-lookup"><span data-stu-id="5f648-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="5f648-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="5f648-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="5f648-158">1000.01 &lt; N = Breyta</span><span class="sxs-lookup"><span data-stu-id="5f648-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="5f648-159">Færslubók</span><span class="sxs-lookup"><span data-stu-id="5f648-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5f648-160">Færslubók</span><span class="sxs-lookup"><span data-stu-id="5f648-160">Journal</span></span></th>
<th><span data-ttu-id="5f648-161">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="5f648-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5f648-162">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="5f648-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5f648-163">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="5f648-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-164">00001</span><span class="sxs-lookup"><span data-stu-id="5f648-164">00001</span></span></td>
<td><span data-ttu-id="5f648-165">Færslubók útreiknings fyrir kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="5f648-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="5f648-166">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="5f648-166">Fiscal</span></span></td>
<td><span data-ttu-id="5f648-167">2017</span><span class="sxs-lookup"><span data-stu-id="5f648-167">2017</span></span></td>
<td><span data-ttu-id="5f648-168">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="5f648-168">Period 1</span></span></td>
<td><span data-ttu-id="5f648-169">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="5f648-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5f648-170">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="5f648-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5f648-171">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="5f648-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5f648-172">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5f648-173">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="5f648-173">Cost element</span></span></th>
<th><span data-ttu-id="5f648-174">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="5f648-174">Cost behavior</span></span></th>
<th><span data-ttu-id="5f648-175">Upphæð</span><span class="sxs-lookup"><span data-stu-id="5f648-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-176">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="5f648-177">CC099</span><span class="sxs-lookup"><span data-stu-id="5f648-177">CC099</span></span></td>
<td><span data-ttu-id="5f648-178">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="5f648-178">Default cost center</span></span></td>
<td><span data-ttu-id="5f648-179">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-179">10001</span></span></td>
<td><span data-ttu-id="5f648-180">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-180">Electricity</span></span></td>
<td><span data-ttu-id="5f648-181">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="5f648-181">Unclassified</span></span></td>
<td><span data-ttu-id="5f648-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="5f648-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5f648-183">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="5f648-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5f648-184">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5f648-185">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="5f648-185">Cost element</span></span></th>
<th><span data-ttu-id="5f648-186">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="5f648-186">Cost behavior</span></span></th>
<th><span data-ttu-id="5f648-187">Upphæð</span><span class="sxs-lookup"><span data-stu-id="5f648-187">Amount</span></span></th>
<th><span data-ttu-id="5f648-188">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="5f648-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-189">CC099</span><span class="sxs-lookup"><span data-stu-id="5f648-189">CC099</span></span></td>
<td><span data-ttu-id="5f648-190">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="5f648-190">Default cost center</span></span></td>
<td><span data-ttu-id="5f648-191">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-191">10001</span></span></td>
<td><span data-ttu-id="5f648-192">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-192">Electricity</span></span></td>
<td><span data-ttu-id="5f648-193">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="5f648-193">Unclassified</span></span></td>
<td><span data-ttu-id="5f648-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="5f648-194">10,000.00</span></span></td>
<td><span data-ttu-id="5f648-195">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-196">CC099</span><span class="sxs-lookup"><span data-stu-id="5f648-196">CC099</span></span></td>
<td><span data-ttu-id="5f648-197">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="5f648-197">Default cost center</span></span></td>
<td><span data-ttu-id="5f648-198">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-198">10001</span></span></td>
<td><span data-ttu-id="5f648-199">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-199">Electricity</span></span></td>
<td><span data-ttu-id="5f648-200">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="5f648-200">Unclassified</span></span></td>
<td><span data-ttu-id="5f648-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="5f648-201">-10,000.00</span></span></td>
<td><span data-ttu-id="5f648-202">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-203">CC099</span><span class="sxs-lookup"><span data-stu-id="5f648-203">CC099</span></span></td>
<td><span data-ttu-id="5f648-204">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="5f648-204">Default cost center</span></span></td>
<td><span data-ttu-id="5f648-205">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-205">10001</span></span></td>
<td><span data-ttu-id="5f648-206">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-206">Electricity</span></span></td>
<td><span data-ttu-id="5f648-207">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-207">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="5f648-208">1,000.00</span></span></td>
<td><span data-ttu-id="5f648-209">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-210">CC099</span><span class="sxs-lookup"><span data-stu-id="5f648-210">CC099</span></span></td>
<td><span data-ttu-id="5f648-211">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="5f648-211">Default cost center</span></span></td>
<td><span data-ttu-id="5f648-212">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-212">10001</span></span></td>
<td><span data-ttu-id="5f648-213">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-213">Electricity</span></span></td>
<td><span data-ttu-id="5f648-214">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-214">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="5f648-215">9,000.00</span></span></td>
<td><span data-ttu-id="5f648-216">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5f648-217">Nákvæmar upplýsingar um kostnaðarhegðun er að finna í Reglu kostnaðarhegðunar.</span><span class="sxs-lookup"><span data-stu-id="5f648-217">For detailed information about cost behavior, see Cost behavior policy.</span></span> <span data-ttu-id="5f648-218">(Athugaðu að þetta efnisatriði hefur ekki enn verið fullklárað en er væntanlegt.)</span><span class="sxs-lookup"><span data-stu-id="5f648-218">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="5f648-219">Skref 2: Keyra útreikning kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="5f648-219">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="5f648-220">Kostnaðardreifing er notuð til að endurúthluta kostnaði frá einum kostnaðarhlut til annars eða fleiri kostnaðarhluta með því að nota viðeigandi úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="5f648-220">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="5f648-221">Kostnaðardreifing og kostnaðarúthlutun eru ólíkar að því leyti að kostnaðardreifing kemur alltaf upp á stigi aðalkostnaðareiningar upphaflegs verðs.</span><span class="sxs-lookup"><span data-stu-id="5f648-221">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="5f648-222">Tilgreinið kostnaðardreifingarreglu</span><span class="sxs-lookup"><span data-stu-id="5f648-222">Define the cost distribution rule</span></span>

<span data-ttu-id="5f648-223">Í Fjárhagsbókhaldi er rafmagnskostnaður oft skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="5f648-223">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="5f648-224">Í kostnaðarbókhaldi er þessi nálgun ekki nógu nákvæm.</span><span class="sxs-lookup"><span data-stu-id="5f648-224">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="5f648-225">Breytilegur kostnaði þarf að dreifa á staka kostnaðarhluti á sanngjörnum grunni.</span><span class="sxs-lookup"><span data-stu-id="5f648-225">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="5f648-226">Rökréttasti úthlutunargrunnurinn er notkun á rafmagni (Kwh).</span><span class="sxs-lookup"><span data-stu-id="5f648-226">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="5f648-227">Stofnað er tölfræðilegt víddarstak sem er nefnt Rafmagn og rafmagnsnotkun er skráð.</span><span class="sxs-lookup"><span data-stu-id="5f648-227">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="5f648-228">Sjálfgefið er að öll tölfræðileg víddarstök verða tiltæk sem úthlutunargrunnur.</span><span class="sxs-lookup"><span data-stu-id="5f648-228">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5f648-229">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-229">Cost object</span></span></th>
<th><span data-ttu-id="5f648-230">Kwh</span><span class="sxs-lookup"><span data-stu-id="5f648-230">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-231">CC001</span><span class="sxs-lookup"><span data-stu-id="5f648-231">CC001</span></span></td>
<td><span data-ttu-id="5f648-232">Mannauður</span><span class="sxs-lookup"><span data-stu-id="5f648-232">HR</span></span></td>
<td><span data-ttu-id="5f648-233">1.000</span><span class="sxs-lookup"><span data-stu-id="5f648-233">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-234">CC002</span><span class="sxs-lookup"><span data-stu-id="5f648-234">CC002</span></span></td>
<td><span data-ttu-id="5f648-235">Fjármál</span><span class="sxs-lookup"><span data-stu-id="5f648-235">Finance</span></span></td>
<td><span data-ttu-id="5f648-236">6,000</span><span class="sxs-lookup"><span data-stu-id="5f648-236">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-237">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-237">CC003</span></span></td>
<td><span data-ttu-id="5f648-238">Smölun</span><span class="sxs-lookup"><span data-stu-id="5f648-238">Assembly</span></span></td>
<td><span data-ttu-id="5f648-239">0</span><span class="sxs-lookup"><span data-stu-id="5f648-239">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5f648-240">Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunni fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="5f648-240">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5f648-241">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-241">Cost object</span></span></th>
<th><span data-ttu-id="5f648-242">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="5f648-242">Magnitude</span></span></th>
<th><span data-ttu-id="5f648-243">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="5f648-243">Allocation factor</span></span></th>
<th><span data-ttu-id="5f648-244">Upphæð</span><span class="sxs-lookup"><span data-stu-id="5f648-244">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-245">CC001</span><span class="sxs-lookup"><span data-stu-id="5f648-245">CC001</span></span></td>
<td><span data-ttu-id="5f648-246">Mannauður</span><span class="sxs-lookup"><span data-stu-id="5f648-246">HR</span></span></td>
<td><span data-ttu-id="5f648-247">1.000</span><span class="sxs-lookup"><span data-stu-id="5f648-247">1,000</span></span></td>
<td><span data-ttu-id="5f648-248">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="5f648-248">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5f648-249">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5f648-249">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-250">CC002</span><span class="sxs-lookup"><span data-stu-id="5f648-250">CC002</span></span></td>
<td><span data-ttu-id="5f648-251">Fjármál</span><span class="sxs-lookup"><span data-stu-id="5f648-251">Finance</span></span></td>
<td><span data-ttu-id="5f648-252">6,000</span><span class="sxs-lookup"><span data-stu-id="5f648-252">6,000</span></span></td>
<td><span data-ttu-id="5f648-253">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="5f648-253">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5f648-254">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5f648-254">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-255">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-255">CC003</span></span></td>
<td><span data-ttu-id="5f648-256">Smölun</span><span class="sxs-lookup"><span data-stu-id="5f648-256">Assembly</span></span></td>
<td><span data-ttu-id="5f648-257">0</span><span class="sxs-lookup"><span data-stu-id="5f648-257">0</span></span></td>
<td><span data-ttu-id="5f648-258">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="5f648-258">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="5f648-259">0,00</span><span class="sxs-lookup"><span data-stu-id="5f648-259">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5f648-260">Föstum kostnaði þarf að dreifa jafnt á staka kostnaðarhluti sem hafa notað rafmagn.</span><span class="sxs-lookup"><span data-stu-id="5f648-260">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="5f648-261">Hægt er að ná þessa niðurstöðu með því að nota tölfræðilegt víddarstakið Rafmagn í úthlutunargrunni reikniformúlu: (Rafmagn &gt; 0,00) Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunn fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="5f648-261">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5f648-262">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-262">Cost object</span></span></th>
<th><span data-ttu-id="5f648-263">Formúla</span><span class="sxs-lookup"><span data-stu-id="5f648-263">Formula</span></span></th>
<th><span data-ttu-id="5f648-264">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="5f648-264">Magnitude</span></span></th>
<th><span data-ttu-id="5f648-265">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="5f648-265">Allocation factor</span></span></th>
<th><span data-ttu-id="5f648-266">Upphæð</span><span class="sxs-lookup"><span data-stu-id="5f648-266">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-267">CC001</span><span class="sxs-lookup"><span data-stu-id="5f648-267">CC001</span></span></td>
<td><span data-ttu-id="5f648-268">Mannauður</span><span class="sxs-lookup"><span data-stu-id="5f648-268">HR</span></span></td>
<td><span data-ttu-id="5f648-269">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="5f648-269">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5f648-270">1</span><span class="sxs-lookup"><span data-stu-id="5f648-270">1</span></span></td>
<td><span data-ttu-id="5f648-271">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="5f648-271">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5f648-272">500,00</span><span class="sxs-lookup"><span data-stu-id="5f648-272">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-273">CC002</span><span class="sxs-lookup"><span data-stu-id="5f648-273">CC002</span></span></td>
<td><span data-ttu-id="5f648-274">Fjármál</span><span class="sxs-lookup"><span data-stu-id="5f648-274">Finance</span></span></td>
<td><span data-ttu-id="5f648-275">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="5f648-275">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5f648-276">1</span><span class="sxs-lookup"><span data-stu-id="5f648-276">1</span></span></td>
<td><span data-ttu-id="5f648-277">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="5f648-277">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5f648-278">500,00</span><span class="sxs-lookup"><span data-stu-id="5f648-278">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-279">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-279">CC003</span></span></td>
<td><span data-ttu-id="5f648-280">Smölun</span><span class="sxs-lookup"><span data-stu-id="5f648-280">Assembly</span></span></td>
<td><span data-ttu-id="5f648-281">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="5f648-281">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="5f648-282">0</span><span class="sxs-lookup"><span data-stu-id="5f648-282">0</span></span></td>
<td><span data-ttu-id="5f648-283">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="5f648-283">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="5f648-284">0,00</span><span class="sxs-lookup"><span data-stu-id="5f648-284">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5f648-285">Færslubók</span><span class="sxs-lookup"><span data-stu-id="5f648-285">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5f648-286">Færslubók</span><span class="sxs-lookup"><span data-stu-id="5f648-286">Journal</span></span></th>
<th><span data-ttu-id="5f648-287">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="5f648-287">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5f648-288">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="5f648-288">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5f648-289">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="5f648-289">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-290">00002</span><span class="sxs-lookup"><span data-stu-id="5f648-290">00002</span></span></td>
<td><span data-ttu-id="5f648-291">Útreikningabók kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="5f648-291">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="5f648-292">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="5f648-292">Fiscal</span></span></td>
<td><span data-ttu-id="5f648-293">2017</span><span class="sxs-lookup"><span data-stu-id="5f648-293">2017</span></span></td>
<td><span data-ttu-id="5f648-294">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="5f648-294">Period 1</span></span></td>
<td><span data-ttu-id="5f648-295">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="5f648-295">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5f648-296">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="5f648-296">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5f648-297">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="5f648-297">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5f648-298">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-298">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5f648-299">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="5f648-299">Cost element</span></span></th>
<th><span data-ttu-id="5f648-300">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="5f648-300">Cost behavior</span></span></th>
<th><span data-ttu-id="5f648-301">Upphæð</span><span class="sxs-lookup"><span data-stu-id="5f648-301">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-302">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-302">January 31, 2017</span></span></td>
<td><span data-ttu-id="5f648-303">CC099</span><span class="sxs-lookup"><span data-stu-id="5f648-303">CC099</span></span></td>
<td><span data-ttu-id="5f648-304">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="5f648-304">Default cost center</span></span></td>
<td><span data-ttu-id="5f648-305">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-305">10001</span></span></td>
<td><span data-ttu-id="5f648-306">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-306">Electricity</span></span></td>
<td><span data-ttu-id="5f648-307">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-307">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-308">1.000,00</span><span class="sxs-lookup"><span data-stu-id="5f648-308">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-309">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-309">January 31, 2017</span></span></td>
<td><span data-ttu-id="5f648-310">CC099</span><span class="sxs-lookup"><span data-stu-id="5f648-310">CC099</span></span></td>
<td><span data-ttu-id="5f648-311">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="5f648-311">Default cost center</span></span></td>
<td><span data-ttu-id="5f648-312">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-312">10001</span></span></td>
<td><span data-ttu-id="5f648-313">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-313">Electricity</span></span></td>
<td><span data-ttu-id="5f648-314">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-314">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-315">9,000.00</span><span class="sxs-lookup"><span data-stu-id="5f648-315">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5f648-316">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="5f648-316">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5f648-317">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-317">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5f648-318">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="5f648-318">Cost element</span></span></th>
<th><span data-ttu-id="5f648-319">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="5f648-319">Cost behavior</span></span></th>
<th><span data-ttu-id="5f648-320">Upphæð</span><span class="sxs-lookup"><span data-stu-id="5f648-320">Amount</span></span></th>
<th><span data-ttu-id="5f648-321">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="5f648-321">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-322">CC099</span><span class="sxs-lookup"><span data-stu-id="5f648-322">CC099</span></span></td>
<td><span data-ttu-id="5f648-323">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="5f648-323">Default cost center</span></span></td>
<td><span data-ttu-id="5f648-324">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-324">10001</span></span></td>
<td><span data-ttu-id="5f648-325">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-325">Electricity</span></span></td>
<td><span data-ttu-id="5f648-326">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-326">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-327">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="5f648-327">-1,000.00</span></span></td>
<td><span data-ttu-id="5f648-328">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-328">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-329">CC001</span><span class="sxs-lookup"><span data-stu-id="5f648-329">CC001</span></span></td>
<td><span data-ttu-id="5f648-330">Mannauður</span><span class="sxs-lookup"><span data-stu-id="5f648-330">HR</span></span></td>
<td><span data-ttu-id="5f648-331">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-331">10001</span></span></td>
<td><span data-ttu-id="5f648-332">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-332">Electricity</span></span></td>
<td><span data-ttu-id="5f648-333">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-333">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-334">500,00</span><span class="sxs-lookup"><span data-stu-id="5f648-334">500.00</span></span></td>
<td><span data-ttu-id="5f648-335">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-335">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-336">CC002</span><span class="sxs-lookup"><span data-stu-id="5f648-336">CC002</span></span></td>
<td><span data-ttu-id="5f648-337">Fjármál</span><span class="sxs-lookup"><span data-stu-id="5f648-337">Finance</span></span></td>
<td><span data-ttu-id="5f648-338">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-338">10001</span></span></td>
<td><span data-ttu-id="5f648-339">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-339">Electricity</span></span></td>
<td><span data-ttu-id="5f648-340">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-340">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-341">500,00</span><span class="sxs-lookup"><span data-stu-id="5f648-341">500.00</span></span></td>
<td><span data-ttu-id="5f648-342">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-342">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-343">CC099</span><span class="sxs-lookup"><span data-stu-id="5f648-343">CC099</span></span></td>
<td><span data-ttu-id="5f648-344">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="5f648-344">Default cost center</span></span></td>
<td><span data-ttu-id="5f648-345">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-345">10001</span></span></td>
<td><span data-ttu-id="5f648-346">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-346">Electricity</span></span></td>
<td><span data-ttu-id="5f648-347">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-347">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-348">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="5f648-348">-9,000.00</span></span></td>
<td><span data-ttu-id="5f648-349">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-349">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-350">CC001</span><span class="sxs-lookup"><span data-stu-id="5f648-350">CC001</span></span></td>
<td><span data-ttu-id="5f648-351">Mannauður</span><span class="sxs-lookup"><span data-stu-id="5f648-351">HR</span></span></td>
<td><span data-ttu-id="5f648-352">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-352">10001</span></span></td>
<td><span data-ttu-id="5f648-353">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-353">Electricity</span></span></td>
<td><span data-ttu-id="5f648-354">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-354">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-355">1,285.71</span><span class="sxs-lookup"><span data-stu-id="5f648-355">1,285.71</span></span></td>
<td><span data-ttu-id="5f648-356">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-356">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-357">CC002</span><span class="sxs-lookup"><span data-stu-id="5f648-357">CC002</span></span></td>
<td><span data-ttu-id="5f648-358">Fjármál</span><span class="sxs-lookup"><span data-stu-id="5f648-358">Finance</span></span></td>
<td><span data-ttu-id="5f648-359">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-359">10001</span></span></td>
<td><span data-ttu-id="5f648-360">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-360">Electricity</span></span></td>
<td><span data-ttu-id="5f648-361">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-361">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-362">7,714.29</span><span class="sxs-lookup"><span data-stu-id="5f648-362">7,714.29</span></span></td>
<td><span data-ttu-id="5f648-363">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-363">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5f648-364">Nákvæmar upplýsingar um kostnaðardreifingu og úthlutunargrunna er að finna í Kostnaðardreifingarreglu og úthlutunargrunnum.</span><span class="sxs-lookup"><span data-stu-id="5f648-364">For detailed information about cost distribution and allocation bases, see Cost distribution policy and Allocation bases.</span></span> <span data-ttu-id="5f648-365">(Athugaðu að þetta efnisatriði hefur ekki enn verið fullklárað en er væntanlegt.)</span><span class="sxs-lookup"><span data-stu-id="5f648-365">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="5f648-366">Skref 3: Keyra útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="5f648-366">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="5f648-367">Sameiginlegur kostnaður er notaður til að rukka einn eða fleiri tilgreinda kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="5f648-367">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="5f648-368">Gjöldin byggjast á fyrirframákveðnu kostnaðarhlutfalli og mæligildi úr úthlutuðum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="5f648-368">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="5f648-369">Skilgreina sameiginlegan kostnað</span><span class="sxs-lookup"><span data-stu-id="5f648-369">Define the overhead rate</span></span>

<span data-ttu-id="5f648-370">Kostnaðarhlutur CC001 Mannauður stuðlar að safni innri verka.</span><span class="sxs-lookup"><span data-stu-id="5f648-370">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="5f648-371">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsverk til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="5f648-371">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5f648-372">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-372">Cost object</span></span></th>
<th><span data-ttu-id="5f648-373">Tímar</span><span class="sxs-lookup"><span data-stu-id="5f648-373">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-374">Verk 1</span><span class="sxs-lookup"><span data-stu-id="5f648-374">Proj 1</span></span></td>
<td><span data-ttu-id="5f648-375">Verk 1</span><span class="sxs-lookup"><span data-stu-id="5f648-375">Project 1</span></span></td>
<td><span data-ttu-id="5f648-376">3</span><span class="sxs-lookup"><span data-stu-id="5f648-376">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-377">Verk 2</span><span class="sxs-lookup"><span data-stu-id="5f648-377">Proj 2</span></span></td>
<td><span data-ttu-id="5f648-378">Verk 2</span><span class="sxs-lookup"><span data-stu-id="5f648-378">Project 2</span></span></td>
<td><span data-ttu-id="5f648-379">1</span><span class="sxs-lookup"><span data-stu-id="5f648-379">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5f648-380">Fyrirframákveðið kostnaðarhlutfall fyrir kostnaðarframlag verk hefur verið skilgreint.</span><span class="sxs-lookup"><span data-stu-id="5f648-380">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5f648-381">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-381">Cost object</span></span></th>
<th><span data-ttu-id="5f648-382">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="5f648-382">Cost element</span></span></th>
<th><span data-ttu-id="5f648-383">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="5f648-383">Cost behavior</span></span></th>
<th><span data-ttu-id="5f648-384">Einingar</span><span class="sxs-lookup"><span data-stu-id="5f648-384">Units</span></span></th>
<th><span data-ttu-id="5f648-385">Taxti</span><span class="sxs-lookup"><span data-stu-id="5f648-385">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-386">CC001</span><span class="sxs-lookup"><span data-stu-id="5f648-386">CC001</span></span></td>
<td><span data-ttu-id="5f648-387">Mannauður</span><span class="sxs-lookup"><span data-stu-id="5f648-387">HR</span></span></td>
<td><span data-ttu-id="5f648-388">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-388">10001</span></span></td>
<td><span data-ttu-id="5f648-389">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-389">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-390">1</span><span class="sxs-lookup"><span data-stu-id="5f648-390">1</span></span></td>
<td><span data-ttu-id="5f648-391">10</span><span class="sxs-lookup"><span data-stu-id="5f648-391">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5f648-392">Eftirfarandi tafla sýnir niðurstöður þegar Mannauðsverk eru notuð sem grunnur við úthlutun.</span><span class="sxs-lookup"><span data-stu-id="5f648-392">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5f648-393">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-393">Cost object</span></span></th>
<th><span data-ttu-id="5f648-394">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="5f648-394">Magnitude</span></span></th>
<th><span data-ttu-id="5f648-395">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="5f648-395">Cost element</span></span></th>
<th><span data-ttu-id="5f648-396">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="5f648-396">Allocation factor</span></span></th>
<th><span data-ttu-id="5f648-397">Upphæð</span><span class="sxs-lookup"><span data-stu-id="5f648-397">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-398">Verk 1</span><span class="sxs-lookup"><span data-stu-id="5f648-398">Proj 1</span></span></td>
<td><span data-ttu-id="5f648-399">Verk 1</span><span class="sxs-lookup"><span data-stu-id="5f648-399">Project 1</span></span></td>
<td><span data-ttu-id="5f648-400">3</span><span class="sxs-lookup"><span data-stu-id="5f648-400">3</span></span></td>
<td><span data-ttu-id="5f648-401">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-401">10001</span></span></td>
<td><span data-ttu-id="5f648-402">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="5f648-402">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5f648-403">30,00</span><span class="sxs-lookup"><span data-stu-id="5f648-403">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-404">Verk 2</span><span class="sxs-lookup"><span data-stu-id="5f648-404">Proj 2</span></span></td>
<td><span data-ttu-id="5f648-405">Verk 2</span><span class="sxs-lookup"><span data-stu-id="5f648-405">Project 2</span></span></td>
<td><span data-ttu-id="5f648-406">1</span><span class="sxs-lookup"><span data-stu-id="5f648-406">1</span></span></td>
<td><span data-ttu-id="5f648-407">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-407">10001</span></span></td>
<td><span data-ttu-id="5f648-408">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="5f648-408">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="5f648-409">10,00</span><span class="sxs-lookup"><span data-stu-id="5f648-409">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="5f648-410">Færslubók</span><span class="sxs-lookup"><span data-stu-id="5f648-410">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5f648-411">Færslubók</span><span class="sxs-lookup"><span data-stu-id="5f648-411">Journal</span></span></th>
<th><span data-ttu-id="5f648-412">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="5f648-412">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5f648-413">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="5f648-413">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5f648-414">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="5f648-414">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-415">00003</span><span class="sxs-lookup"><span data-stu-id="5f648-415">00003</span></span></td>
<td><span data-ttu-id="5f648-416">Færslubók fyrir útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="5f648-416">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="5f648-417">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="5f648-417">Fiscal</span></span></td>
<td><span data-ttu-id="5f648-418">2017</span><span class="sxs-lookup"><span data-stu-id="5f648-418">2017</span></span></td>
<td><span data-ttu-id="5f648-419">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="5f648-419">Period 1</span></span></td>
<td><span data-ttu-id="5f648-420">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="5f648-420">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="5f648-421">Bókarfærslur (Bókarfærslur fyrir útreikning sameiginlegs kostnaðar)</span><span class="sxs-lookup"><span data-stu-id="5f648-421">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5f648-422">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="5f648-422">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5f648-423">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-423">Cost object</span></span></th>
<th><span data-ttu-id="5f648-424">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="5f648-424">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-425">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-425">January 31, 2017</span></span></td>
<td><span data-ttu-id="5f648-426">Verk 1</span><span class="sxs-lookup"><span data-stu-id="5f648-426">Proj 1</span></span></td>
<td><span data-ttu-id="5f648-427">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="5f648-427">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5f648-428">3,00</span><span class="sxs-lookup"><span data-stu-id="5f648-428">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-429">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-429">January 31, 2017</span></span></td>
<td><span data-ttu-id="5f648-430">Verk 2</span><span class="sxs-lookup"><span data-stu-id="5f648-430">Proj 2</span></span></td>
<td><span data-ttu-id="5f648-431">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="5f648-431">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5f648-432">1,00</span><span class="sxs-lookup"><span data-stu-id="5f648-432">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5f648-433">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="5f648-433">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5f648-434">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-434">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5f648-435">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="5f648-435">Cost element</span></span></th>
<th><span data-ttu-id="5f648-436">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="5f648-436">Cost behavior</span></span></th>
<th><span data-ttu-id="5f648-437">Upphæð</span><span class="sxs-lookup"><span data-stu-id="5f648-437">Amount</span></span></th>
<th><span data-ttu-id="5f648-438">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="5f648-438">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-439">CC0001</span><span class="sxs-lookup"><span data-stu-id="5f648-439">CC0001</span></span></td>
<td><span data-ttu-id="5f648-440">Mannauður</span><span class="sxs-lookup"><span data-stu-id="5f648-440">HR</span></span></td>
<td><span data-ttu-id="5f648-441">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-441">10001</span></span></td>
<td><span data-ttu-id="5f648-442">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-442">Electricity</span></span></td>
<td><span data-ttu-id="5f648-443">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-443">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-444">-30,00</span><span class="sxs-lookup"><span data-stu-id="5f648-444">-30.00</span></span></td>
<td><span data-ttu-id="5f648-445">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-445">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-446">Verk 1</span><span class="sxs-lookup"><span data-stu-id="5f648-446">Proj 1</span></span></td>
<td><span data-ttu-id="5f648-447">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="5f648-447">Internal Proj 1</span></span></td>
<td><span data-ttu-id="5f648-448">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-448">10001</span></span></td>
<td><span data-ttu-id="5f648-449">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-449">Electricity</span></span></td>
<td><span data-ttu-id="5f648-450">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-450">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-451">30,00</span><span class="sxs-lookup"><span data-stu-id="5f648-451">30.00</span></span></td>
<td><span data-ttu-id="5f648-452">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-452">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-453">CC001</span><span class="sxs-lookup"><span data-stu-id="5f648-453">CC001</span></span></td>
<td><span data-ttu-id="5f648-454">Mannauður</span><span class="sxs-lookup"><span data-stu-id="5f648-454">HR</span></span></td>
<td><span data-ttu-id="5f648-455">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-455">10001</span></span></td>
<td><span data-ttu-id="5f648-456">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-456">Electricity</span></span></td>
<td><span data-ttu-id="5f648-457">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-457">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-458">-10,00</span><span class="sxs-lookup"><span data-stu-id="5f648-458">-10.00</span></span></td>
<td><span data-ttu-id="5f648-459">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-459">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-460">Verk 2</span><span class="sxs-lookup"><span data-stu-id="5f648-460">Proj 2</span></span></td>
<td><span data-ttu-id="5f648-461">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="5f648-461">Internal Proj 2</span></span></td>
<td><span data-ttu-id="5f648-462">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-462">10001</span></span></td>
<td><span data-ttu-id="5f648-463">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-463">Electricity</span></span></td>
<td><span data-ttu-id="5f648-464">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-464">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-465">10,00</span><span class="sxs-lookup"><span data-stu-id="5f648-465">10.00</span></span></td>
<td><span data-ttu-id="5f648-466">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-466">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5f648-467">Nákvæmar upplýsingar um reglu sameiginlegs kostnaðar er að finna í Reglu fyrir sameiginlegan kostnað og úthlutunargrunnum.</span><span class="sxs-lookup"><span data-stu-id="5f648-467">For detailed information about overhead rate policy, see Overhead rate policy and Allocation bases.</span></span> <span data-ttu-id="5f648-468">(Athugaðu að þetta efnisatriði hefur ekki enn verið fullklárað en er væntanlegt.)</span><span class="sxs-lookup"><span data-stu-id="5f648-468">(Note that this topic isn't competed yet but is coming soon.)</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="5f648-469">Skref 4: Keyra útreikning kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="5f648-469">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="5f648-470">Úthlutun er notuð til að úthluta stöðu kostnaðarhlutar í öðrum kostnaðarhlutum með því að nota úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="5f648-470">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="5f648-471">Finance and Operations styður gagnvirka úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="5f648-471">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="5f648-472">Í gagnvirkri úthlutunaraðferð er sú sameiginlega þjónusta sem hjálparkostnaðarhlutir skiptast á viðurkennd að fullu.</span><span class="sxs-lookup"><span data-stu-id="5f648-472">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="5f648-473">Kerfið ákvarðar sjálfkrafa rétta röð til að framkvæma úthlutun eftir.</span><span class="sxs-lookup"><span data-stu-id="5f648-473">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="5f648-474">Stöðu kostnaðarhluta er úthlutað með einum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="5f648-474">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="5f648-475">Úthlutanir þvert á víddir kostnaðarhluta og viðkomandi stök þeirra eru studdar.</span><span class="sxs-lookup"><span data-stu-id="5f648-475">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="5f648-476">Úthlutun pöntunarinnar er stjórnað af stýrieiningu kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="5f648-476">The allocation order is controlled by the cost control unit.</span></span> <span data-ttu-id="5f648-477">[![Umhverf aðferð](./media/reciprocal-method.png)]</span><span class="sxs-lookup"><span data-stu-id="5f648-477">[![Reciprocal method](./media/reciprocal-method.png)]</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="5f648-478">Tilgreinið kostnaðarúthlutun</span><span class="sxs-lookup"><span data-stu-id="5f648-478">Define the cost allocation</span></span>

<span data-ttu-id="5f648-479">Hér er einfalt dæmi sem útskýrir hvernig hægt er að rekja flæði kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="5f648-479">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="5f648-480">Kostnaðarhlutir CC001 Mannauður leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="5f648-480">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="5f648-481">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="5f648-481">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5f648-482">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-482">Cost object</span></span></th>
<th><span data-ttu-id="5f648-483">Mannauðsþjónusta</span><span class="sxs-lookup"><span data-stu-id="5f648-483">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-484">CC002</span><span class="sxs-lookup"><span data-stu-id="5f648-484">CC002</span></span></td>
<td><span data-ttu-id="5f648-485">Fjármál</span><span class="sxs-lookup"><span data-stu-id="5f648-485">Finance</span></span></td>
<td><span data-ttu-id="5f648-486">35</span><span class="sxs-lookup"><span data-stu-id="5f648-486">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-487">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-487">CC003</span></span></td>
<td><span data-ttu-id="5f648-488">Smölun</span><span class="sxs-lookup"><span data-stu-id="5f648-488">Assembly</span></span></td>
<td><span data-ttu-id="5f648-489">55</span><span class="sxs-lookup"><span data-stu-id="5f648-489">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-490">CC004</span><span class="sxs-lookup"><span data-stu-id="5f648-490">CC004</span></span></td>
<td><span data-ttu-id="5f648-491">Pakkning</span><span class="sxs-lookup"><span data-stu-id="5f648-491">Packaging</span></span></td>
<td><span data-ttu-id="5f648-492">10</span><span class="sxs-lookup"><span data-stu-id="5f648-492">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5f648-493">Kostnaðarhlutir CC002 Fjármál leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="5f648-493">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="5f648-494">Stofnað er tölfræðilegt víddarstak sem kallast Fjármálaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="5f648-494">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5f648-495">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-495">Cost object</span></span></th>
<th><span data-ttu-id="5f648-496">Fjármálaþjónusta</span><span class="sxs-lookup"><span data-stu-id="5f648-496">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-497">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-497">CC003</span></span></td>
<td><span data-ttu-id="5f648-498">Smölun</span><span class="sxs-lookup"><span data-stu-id="5f648-498">Assembly</span></span></td>
<td><span data-ttu-id="5f648-499">65</span><span class="sxs-lookup"><span data-stu-id="5f648-499">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-500">CC004</span><span class="sxs-lookup"><span data-stu-id="5f648-500">CC004</span></span></td>
<td><span data-ttu-id="5f648-501">Pakkning</span><span class="sxs-lookup"><span data-stu-id="5f648-501">Packaging</span></span></td>
<td><span data-ttu-id="5f648-502">35</span><span class="sxs-lookup"><span data-stu-id="5f648-502">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5f648-503">Kostnaðarhlutir CC003 Samsetning leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="5f648-503">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="5f648-504">Meðlimur tölfræðilega víddar sem kallast Mannauður verk er stofnað til að mælvíddarstaka notuðum magnitude.</span><span class="sxs-lookup"><span data-stu-id="5f648-504">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5f648-505">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-505">Cost object</span></span></th>
<th><span data-ttu-id="5f648-506">Samsetningarþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="5f648-506">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-507">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-507">Prod 1</span></span></td>
<td><span data-ttu-id="5f648-508">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-508">Product 1</span></span></td>
<td><span data-ttu-id="5f648-509">60</span><span class="sxs-lookup"><span data-stu-id="5f648-509">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-510">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-510">Prod 2</span></span></td>
<td><span data-ttu-id="5f648-511">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-511">Product 2</span></span></td>
<td><span data-ttu-id="5f648-512">20</span><span class="sxs-lookup"><span data-stu-id="5f648-512">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5f648-513">Kostnaðarhlutir CC004 Umbúðir leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="5f648-513">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="5f648-514">Stofnað er tölfræðilegt víddarstak sem kallast Umbúðaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="5f648-514">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5f648-515">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-515">Cost object</span></span></th>
<th><span data-ttu-id="5f648-516">Umbúðaþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="5f648-516">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-517">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-517">Prod 1</span></span></td>
<td><span data-ttu-id="5f648-518">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-518">Product 1</span></span></td>
<td><span data-ttu-id="5f648-519">80</span><span class="sxs-lookup"><span data-stu-id="5f648-519">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-520">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-520">Prod 2</span></span></td>
<td><span data-ttu-id="5f648-521">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-521">Product 2</span></span></td>
<td><span data-ttu-id="5f648-522">sept</span><span class="sxs-lookup"><span data-stu-id="5f648-522">15</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5f648-523">**Athugið:** Í Finance and Operations er hægt að afleiða tölfræðiaðgerðir eins og framleiðslutíma sem vara notar frá upprunagögnum.</span><span class="sxs-lookup"><span data-stu-id="5f648-523">**Note:** In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="5f648-524">Ítarlegri upplýsingar um veitur tölfræðiaðgerðar er að finna í Veitusniðmáti tölfræðiaðgerðar.</span><span class="sxs-lookup"><span data-stu-id="5f648-524">For more detailed information about statistical measure providers, see Statistical measure provider template.</span></span> <span data-ttu-id="5f648-525">(Athugið að þetta efnisatriði er ekki enn fullklárað en er væntanlegt.) Eftirfarandi tafla sýnir niðurstöður þegar Mannauðsþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="5f648-525">(Note that this topic isn't completed yet but is coming soon.) The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5f648-526">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-526">Cost object</span></span></th>
<th><span data-ttu-id="5f648-527">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="5f648-527">Magnitude</span></span></th>
<th><span data-ttu-id="5f648-528">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="5f648-528">Allocation factor</span></span></th>
<th><span data-ttu-id="5f648-529">Upphæð</span><span class="sxs-lookup"><span data-stu-id="5f648-529">Amount</span></span></th>
<th><span data-ttu-id="5f648-530">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="5f648-530">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-531">CC002</span><span class="sxs-lookup"><span data-stu-id="5f648-531">CC002</span></span></td>
<td><span data-ttu-id="5f648-532">Fjármál</span><span class="sxs-lookup"><span data-stu-id="5f648-532">Finance</span></span></td>
<td><span data-ttu-id="5f648-533">35</span><span class="sxs-lookup"><span data-stu-id="5f648-533">35</span></span></td>
<td><span data-ttu-id="5f648-534">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="5f648-534">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5f648-535">175.00</span><span class="sxs-lookup"><span data-stu-id="5f648-535">175.00</span></span></td>
<td><span data-ttu-id="5f648-536">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-536">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-537">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-537">CC003</span></span></td>
<td><span data-ttu-id="5f648-538">Smölun</span><span class="sxs-lookup"><span data-stu-id="5f648-538">Assembly</span></span></td>
<td><span data-ttu-id="5f648-539">55</span><span class="sxs-lookup"><span data-stu-id="5f648-539">55</span></span></td>
<td><span data-ttu-id="5f648-540">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="5f648-540">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5f648-541">275.00</span><span class="sxs-lookup"><span data-stu-id="5f648-541">275.00</span></span></td>
<td><span data-ttu-id="5f648-542">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-542">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-543">CC004</span><span class="sxs-lookup"><span data-stu-id="5f648-543">CC004</span></span></td>
<td><span data-ttu-id="5f648-544">Pakkning</span><span class="sxs-lookup"><span data-stu-id="5f648-544">Packaging</span></span></td>
<td><span data-ttu-id="5f648-545">10</span><span class="sxs-lookup"><span data-stu-id="5f648-545">10</span></span></td>
<td><span data-ttu-id="5f648-546">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="5f648-546">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="5f648-547">50,00</span><span class="sxs-lookup"><span data-stu-id="5f648-547">50.00</span></span></td>
<td><span data-ttu-id="5f648-548">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-548">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-549">CC002</span><span class="sxs-lookup"><span data-stu-id="5f648-549">CC002</span></span></td>
<td><span data-ttu-id="5f648-550">Fjármál</span><span class="sxs-lookup"><span data-stu-id="5f648-550">Finance</span></span></td>
<td><span data-ttu-id="5f648-551">35</span><span class="sxs-lookup"><span data-stu-id="5f648-551">35</span></span></td>
<td><span data-ttu-id="5f648-552">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="5f648-552">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5f648-553">436.00</span><span class="sxs-lookup"><span data-stu-id="5f648-553">436.00</span></span></td>
<td><span data-ttu-id="5f648-554">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-554">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-555">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-555">CC003</span></span></td>
<td><span data-ttu-id="5f648-556">Smölun</span><span class="sxs-lookup"><span data-stu-id="5f648-556">Assembly</span></span></td>
<td><span data-ttu-id="5f648-557">55</span><span class="sxs-lookup"><span data-stu-id="5f648-557">55</span></span></td>
<td><span data-ttu-id="5f648-558">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="5f648-558">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5f648-559">685.14</span><span class="sxs-lookup"><span data-stu-id="5f648-559">685.14</span></span></td>
<td><span data-ttu-id="5f648-560">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-560">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-561">CC004</span><span class="sxs-lookup"><span data-stu-id="5f648-561">CC004</span></span></td>
<td><span data-ttu-id="5f648-562">Pakkning</span><span class="sxs-lookup"><span data-stu-id="5f648-562">Packaging</span></span></td>
<td><span data-ttu-id="5f648-563">10</span><span class="sxs-lookup"><span data-stu-id="5f648-563">10</span></span></td>
<td><span data-ttu-id="5f648-564">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="5f648-564">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="5f648-565">124.57</span><span class="sxs-lookup"><span data-stu-id="5f648-565">124.57</span></span></td>
<td><span data-ttu-id="5f648-566">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-566">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5f648-567">Eftirfarandi tafla sýnir niðurstöður þegar Fjármálaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="5f648-567">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5f648-568">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-568">Cost object</span></span></th>
<th><span data-ttu-id="5f648-569">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="5f648-569">Magnitude</span></span></th>
<th><span data-ttu-id="5f648-570">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="5f648-570">Allocation factor</span></span></th>
<th><span data-ttu-id="5f648-571">Upphæð</span><span class="sxs-lookup"><span data-stu-id="5f648-571">Amount</span></span></th>
<th><span data-ttu-id="5f648-572">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="5f648-572">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-573">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-573">CC003</span></span></td>
<td><span data-ttu-id="5f648-574">Smölun</span><span class="sxs-lookup"><span data-stu-id="5f648-574">Assembly</span></span></td>
<td><span data-ttu-id="5f648-575">65</span><span class="sxs-lookup"><span data-stu-id="5f648-575">65</span></span></td>
<td><span data-ttu-id="5f648-576">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="5f648-576">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5f648-577">438.75</span><span class="sxs-lookup"><span data-stu-id="5f648-577">438.75</span></span></td>
<td><span data-ttu-id="5f648-578">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-578">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-579">CC004</span><span class="sxs-lookup"><span data-stu-id="5f648-579">CC004</span></span></td>
<td><span data-ttu-id="5f648-580">Pakkning</span><span class="sxs-lookup"><span data-stu-id="5f648-580">Packaging</span></span></td>
<td><span data-ttu-id="5f648-581">35</span><span class="sxs-lookup"><span data-stu-id="5f648-581">35</span></span></td>
<td><span data-ttu-id="5f648-582">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="5f648-582">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="5f648-583">236.25</span><span class="sxs-lookup"><span data-stu-id="5f648-583">236.25</span></span></td>
<td><span data-ttu-id="5f648-584">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-584">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-585">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-585">CC003</span></span></td>
<td><span data-ttu-id="5f648-586">Smölun</span><span class="sxs-lookup"><span data-stu-id="5f648-586">Assembly</span></span></td>
<td><span data-ttu-id="5f648-587">65</span><span class="sxs-lookup"><span data-stu-id="5f648-587">65</span></span></td>
<td><span data-ttu-id="5f648-588">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="5f648-588">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5f648-589">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5f648-589">5,297.69</span></span></td>
<td><span data-ttu-id="5f648-590">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-590">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-591">CC004</span><span class="sxs-lookup"><span data-stu-id="5f648-591">CC004</span></span></td>
<td><span data-ttu-id="5f648-592">Pakkning</span><span class="sxs-lookup"><span data-stu-id="5f648-592">Packaging</span></span></td>
<td><span data-ttu-id="5f648-593">35</span><span class="sxs-lookup"><span data-stu-id="5f648-593">35</span></span></td>
<td><span data-ttu-id="5f648-594">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="5f648-594">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="5f648-595">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5f648-595">2,852.60</span></span></td>
<td><span data-ttu-id="5f648-596">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-596">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5f648-597">Eftirfarandi tafla sýnir niðurstöður þegar Samsetningarþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="5f648-597">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5f648-598">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-598">Cost object</span></span></th>
<th><span data-ttu-id="5f648-599">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="5f648-599">Magnitude</span></span></th>
<th><span data-ttu-id="5f648-600">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="5f648-600">Allocation factor</span></span></th>
<th><span data-ttu-id="5f648-601">Upphæð</span><span class="sxs-lookup"><span data-stu-id="5f648-601">Amount</span></span></th>
<th><span data-ttu-id="5f648-602">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="5f648-602">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-603">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-603">Prod 1</span></span></td>
<td><span data-ttu-id="5f648-604">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-604">Product 1</span></span></td>
<td><span data-ttu-id="5f648-605">60</span><span class="sxs-lookup"><span data-stu-id="5f648-605">60</span></span></td>
<td><span data-ttu-id="5f648-606">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="5f648-606">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5f648-607">535.31</span><span class="sxs-lookup"><span data-stu-id="5f648-607">535.31</span></span></td>
<td><span data-ttu-id="5f648-608">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-608">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-609">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-609">Prod 2</span></span></td>
<td><span data-ttu-id="5f648-610">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-610">Product 2</span></span></td>
<td><span data-ttu-id="5f648-611">20</span><span class="sxs-lookup"><span data-stu-id="5f648-611">20</span></span></td>
<td><span data-ttu-id="5f648-612">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="5f648-612">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="5f648-613">178.44</span><span class="sxs-lookup"><span data-stu-id="5f648-613">178.44</span></span></td>
<td><span data-ttu-id="5f648-614">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-614">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-615">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-615">Prod 1</span></span></td>
<td><span data-ttu-id="5f648-616">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-616">Product 1</span></span></td>
<td><span data-ttu-id="5f648-617">60</span><span class="sxs-lookup"><span data-stu-id="5f648-617">60</span></span></td>
<td><span data-ttu-id="5f648-618">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="5f648-618">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5f648-619">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5f648-619">4,487.12</span></span></td>
<td><span data-ttu-id="5f648-620">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-620">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-621">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-621">Prod 2</span></span></td>
<td><span data-ttu-id="5f648-622">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-622">Product 2</span></span></td>
<td><span data-ttu-id="5f648-623">20</span><span class="sxs-lookup"><span data-stu-id="5f648-623">20</span></span></td>
<td><span data-ttu-id="5f648-624">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="5f648-624">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="5f648-625">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5f648-625">1,495.71</span></span></td>
<td><span data-ttu-id="5f648-626">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-626">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5f648-627">Eftirfarandi tafla sýnir niðurstöður þegar Umbúðaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="5f648-627">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5f648-628">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-628">Cost object</span></span></th>
<th><span data-ttu-id="5f648-629">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="5f648-629">Magnitude</span></span></th>
<th><span data-ttu-id="5f648-630">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="5f648-630">Allocation factor</span></span></th>
<th><span data-ttu-id="5f648-631">Upphæð</span><span class="sxs-lookup"><span data-stu-id="5f648-631">Amount</span></span></th>
<th><span data-ttu-id="5f648-632">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="5f648-632">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-633">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-633">Prod 1</span></span></td>
<td><span data-ttu-id="5f648-634">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-634">Product 1</span></span></td>
<td><span data-ttu-id="5f648-635">80</span><span class="sxs-lookup"><span data-stu-id="5f648-635">80</span></span></td>
<td><span data-ttu-id="5f648-636">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="5f648-636">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5f648-637">241.05</span><span class="sxs-lookup"><span data-stu-id="5f648-637">241.05</span></span></td>
<td><span data-ttu-id="5f648-638">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-638">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-639">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-639">Prod 2</span></span></td>
<td><span data-ttu-id="5f648-640">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-640">Product 2</span></span></td>
<td><span data-ttu-id="5f648-641">15</span><span class="sxs-lookup"><span data-stu-id="5f648-641">15</span></span></td>
<td><span data-ttu-id="5f648-642">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="5f648-642">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="5f648-643">45.20</span><span class="sxs-lookup"><span data-stu-id="5f648-643">45.20</span></span></td>
<td><span data-ttu-id="5f648-644">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-644">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-645">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-645">Prod 1</span></span></td>
<td><span data-ttu-id="5f648-646">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-646">Product 1</span></span></td>
<td><span data-ttu-id="5f648-647">80</span><span class="sxs-lookup"><span data-stu-id="5f648-647">80</span></span></td>
<td><span data-ttu-id="5f648-648">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="5f648-648">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5f648-649">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5f648-649">2,507.09</span></span></td>
<td><span data-ttu-id="5f648-650">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-650">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-651">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-651">Prod 2</span></span></td>
<td><span data-ttu-id="5f648-652">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-652">Product 2</span></span></td>
<td><span data-ttu-id="5f648-653">15</span><span class="sxs-lookup"><span data-stu-id="5f648-653">15</span></span></td>
<td><span data-ttu-id="5f648-654">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="5f648-654">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="5f648-655">470.08</span><span class="sxs-lookup"><span data-stu-id="5f648-655">470.08</span></span></td>
<td><span data-ttu-id="5f648-656">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-656">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="5f648-657">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="5f648-657">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5f648-658">Færslubók</span><span class="sxs-lookup"><span data-stu-id="5f648-658">Journal</span></span></th>
<th><span data-ttu-id="5f648-659">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="5f648-659">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="5f648-660">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="5f648-660">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="5f648-661">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="5f648-661">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-662">00004</span><span class="sxs-lookup"><span data-stu-id="5f648-662">00004</span></span></td>
<td><span data-ttu-id="5f648-663">Færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="5f648-663">Cost allocation journal</span></span></td>
<td><span data-ttu-id="5f648-664">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="5f648-664">Fiscal</span></span></td>
<td><span data-ttu-id="5f648-665">2017</span><span class="sxs-lookup"><span data-stu-id="5f648-665">2017</span></span></td>
<td><span data-ttu-id="5f648-666">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="5f648-666">Period 1</span></span></td>
<td><span data-ttu-id="5f648-667">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="5f648-667">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="5f648-668">Færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="5f648-668">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="5f648-669">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="5f648-669">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="5f648-670">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-670">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5f648-671">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="5f648-671">Cost element</span></span></th>
<th><span data-ttu-id="5f648-672">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="5f648-672">Cost behavior</span></span></th>
<th><span data-ttu-id="5f648-673">Upphæð</span><span class="sxs-lookup"><span data-stu-id="5f648-673">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-674">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-674">January 31, 2017</span></span></td>
<td><span data-ttu-id="5f648-675">CC001</span><span class="sxs-lookup"><span data-stu-id="5f648-675">CC001</span></span></td>
<td><span data-ttu-id="5f648-676">Mannauður</span><span class="sxs-lookup"><span data-stu-id="5f648-676">HR</span></span></td>
<td><span data-ttu-id="5f648-677">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-677">10001</span></span></td>
<td><span data-ttu-id="5f648-678">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-678">Electricity</span></span></td>
<td><span data-ttu-id="5f648-679">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-679">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-680">500,00</span><span class="sxs-lookup"><span data-stu-id="5f648-680">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-681">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-681">January 31, 2017</span></span></td>
<td><span data-ttu-id="5f648-682">CC001</span><span class="sxs-lookup"><span data-stu-id="5f648-682">CC001</span></span></td>
<td><span data-ttu-id="5f648-683">Mannauður</span><span class="sxs-lookup"><span data-stu-id="5f648-683">HR</span></span></td>
<td><span data-ttu-id="5f648-684">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-684">10001</span></span></td>
<td><span data-ttu-id="5f648-685">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-685">Electricity</span></span></td>
<td><span data-ttu-id="5f648-686">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-686">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-687">1,245.71</span><span class="sxs-lookup"><span data-stu-id="5f648-687">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-688">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-688">January 31, 2017</span></span></td>
<td><span data-ttu-id="5f648-689">CC002</span><span class="sxs-lookup"><span data-stu-id="5f648-689">CC002</span></span></td>
<td><span data-ttu-id="5f648-690">Fjármál</span><span class="sxs-lookup"><span data-stu-id="5f648-690">Finance</span></span></td>
<td><span data-ttu-id="5f648-691">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-691">10001</span></span></td>
<td><span data-ttu-id="5f648-692">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-692">Electricity</span></span></td>
<td><span data-ttu-id="5f648-693">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-693">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-694">675.00</span><span class="sxs-lookup"><span data-stu-id="5f648-694">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-695">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-695">January 31, 2017</span></span></td>
<td><span data-ttu-id="5f648-696">CC002</span><span class="sxs-lookup"><span data-stu-id="5f648-696">CC002</span></span></td>
<td><span data-ttu-id="5f648-697">Fjármál</span><span class="sxs-lookup"><span data-stu-id="5f648-697">Finance</span></span></td>
<td><span data-ttu-id="5f648-698">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-698">10001</span></span></td>
<td><span data-ttu-id="5f648-699">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-699">Electricity</span></span></td>
<td><span data-ttu-id="5f648-700">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-700">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-701">8,150.29</span><span class="sxs-lookup"><span data-stu-id="5f648-701">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-702">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-702">January 31, 2017</span></span></td>
<td><span data-ttu-id="5f648-703">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-703">CC003</span></span></td>
<td><span data-ttu-id="5f648-704">Smölun</span><span class="sxs-lookup"><span data-stu-id="5f648-704">Assembly</span></span></td>
<td><span data-ttu-id="5f648-705">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-705">10001</span></span></td>
<td><span data-ttu-id="5f648-706">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-706">Electricity</span></span></td>
<td><span data-ttu-id="5f648-707">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-707">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-708">713.75</span><span class="sxs-lookup"><span data-stu-id="5f648-708">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-709">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-709">January 31, 2017</span></span></td>
<td><span data-ttu-id="5f648-710">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-710">CC003</span></span></td>
<td><span data-ttu-id="5f648-711">Smölun</span><span class="sxs-lookup"><span data-stu-id="5f648-711">Assembly</span></span></td>
<td><span data-ttu-id="5f648-712">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-712">10001</span></span></td>
<td><span data-ttu-id="5f648-713">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-713">Electricity</span></span></td>
<td><span data-ttu-id="5f648-714">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-714">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-715">5,982.83</span><span class="sxs-lookup"><span data-stu-id="5f648-715">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-716">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-716">January 31, 2017</span></span></td>
<td><span data-ttu-id="5f648-717">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-717">CC003</span></span></td>
<td><span data-ttu-id="5f648-718">Pakkning</span><span class="sxs-lookup"><span data-stu-id="5f648-718">Packaging</span></span></td>
<td><span data-ttu-id="5f648-719">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-719">10001</span></span></td>
<td><span data-ttu-id="5f648-720">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-720">Electricity</span></span></td>
<td><span data-ttu-id="5f648-721">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-721">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-722">286.25</span><span class="sxs-lookup"><span data-stu-id="5f648-722">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-723">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-723">January 31, 2017</span></span></td>
<td><span data-ttu-id="5f648-724">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-724">CC003</span></span></td>
<td><span data-ttu-id="5f648-725">Pakkning</span><span class="sxs-lookup"><span data-stu-id="5f648-725">Packaging</span></span></td>
<td><span data-ttu-id="5f648-726">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-726">10001</span></span></td>
<td><span data-ttu-id="5f648-727">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-727">Electricity</span></span></td>
<td><span data-ttu-id="5f648-728">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-728">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-729">2,977.17</span><span class="sxs-lookup"><span data-stu-id="5f648-729">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-730">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-730">January 31, 2017</span></span></td>
<td><span data-ttu-id="5f648-731">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-731">Prod 1</span></span></td>
<td><span data-ttu-id="5f648-732">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-732">Product 1</span></span></td>
<td><span data-ttu-id="5f648-733">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-733">10001</span></span></td>
<td><span data-ttu-id="5f648-734">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-734">Electricity</span></span></td>
<td><span data-ttu-id="5f648-735">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-735">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-736">776.36</span><span class="sxs-lookup"><span data-stu-id="5f648-736">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-737">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-737">January 31, 2017</span></span></td>
<td><span data-ttu-id="5f648-738">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-738">Prod 1</span></span></td>
<td><span data-ttu-id="5f648-739">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-739">Product 1</span></span></td>
<td><span data-ttu-id="5f648-740">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-740">10001</span></span></td>
<td><span data-ttu-id="5f648-741">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-741">Electricity</span></span></td>
<td><span data-ttu-id="5f648-742">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-742">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-743">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5f648-743">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-744">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-744">January 31, 2017</span></span></td>
<td><span data-ttu-id="5f648-745">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-745">Prod 2</span></span></td>
<td><span data-ttu-id="5f648-746">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-746">Product 1</span></span></td>
<td><span data-ttu-id="5f648-747">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-747">10001</span></span></td>
<td><span data-ttu-id="5f648-748">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-748">Electricity</span></span></td>
<td><span data-ttu-id="5f648-749">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-749">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-750">223.64</span><span class="sxs-lookup"><span data-stu-id="5f648-750">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-751">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-751">January 31, 2017</span></span></td>
<td><span data-ttu-id="5f648-752">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-752">Prod 2</span></span></td>
<td><span data-ttu-id="5f648-753">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-753">Product 1</span></span></td>
<td><span data-ttu-id="5f648-754">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-754">10001</span></span></td>
<td><span data-ttu-id="5f648-755">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-755">Electricity</span></span></td>
<td><span data-ttu-id="5f648-756">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-756">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-757">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5f648-757">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="5f648-758">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="5f648-758">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="5f648-759">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-759">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="5f648-760">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="5f648-760">Cost element</span></span></th>
<th><span data-ttu-id="5f648-761">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="5f648-761">Cost behavior</span></span></th>
<th><span data-ttu-id="5f648-762">Upphæð</span><span class="sxs-lookup"><span data-stu-id="5f648-762">Amount</span></span></th>
<th><span data-ttu-id="5f648-763">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="5f648-763">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5f648-764">CC001</span><span class="sxs-lookup"><span data-stu-id="5f648-764">CC001</span></span></td>
<td><span data-ttu-id="5f648-765">Mannauður</span><span class="sxs-lookup"><span data-stu-id="5f648-765">HR</span></span></td>
<td><span data-ttu-id="5f648-766">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-766">10001</span></span></td>
<td><span data-ttu-id="5f648-767">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-767">Electricity</span></span></td>
<td><span data-ttu-id="5f648-768">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-768">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-769">-500,00</span><span class="sxs-lookup"><span data-stu-id="5f648-769">-500.00</span></span></td>
<td><span data-ttu-id="5f648-770">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-770">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-771">CC002</span><span class="sxs-lookup"><span data-stu-id="5f648-771">CC002</span></span></td>
<td><span data-ttu-id="5f648-772">Fjármál</span><span class="sxs-lookup"><span data-stu-id="5f648-772">Finance</span></span></td>
<td><span data-ttu-id="5f648-773">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-773">10001</span></span></td>
<td><span data-ttu-id="5f648-774">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-774">Electricity</span></span></td>
<td><span data-ttu-id="5f648-775">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-775">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-776">175.00</span><span class="sxs-lookup"><span data-stu-id="5f648-776">175.00</span></span></td>
<td><span data-ttu-id="5f648-777">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-777">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-778">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-778">CC003</span></span></td>
<td><span data-ttu-id="5f648-779">Smölun</span><span class="sxs-lookup"><span data-stu-id="5f648-779">Assembly</span></span></td>
<td><span data-ttu-id="5f648-780">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-780">10001</span></span></td>
<td><span data-ttu-id="5f648-781">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-781">Electricity</span></span></td>
<td><span data-ttu-id="5f648-782">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-782">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-783">275.00</span><span class="sxs-lookup"><span data-stu-id="5f648-783">275.00</span></span></td>
<td><span data-ttu-id="5f648-784">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-784">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-785">CC004</span><span class="sxs-lookup"><span data-stu-id="5f648-785">CC004</span></span></td>
<td><span data-ttu-id="5f648-786">Pakkning</span><span class="sxs-lookup"><span data-stu-id="5f648-786">Packaging</span></span></td>
<td><span data-ttu-id="5f648-787">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-787">10001</span></span></td>
<td><span data-ttu-id="5f648-788">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-788">Electricity</span></span></td>
<td><span data-ttu-id="5f648-789">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-789">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-790">50,00</span><span class="sxs-lookup"><span data-stu-id="5f648-790">50,00</span></span></td>
<td><span data-ttu-id="5f648-791">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-791">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-792">CC001</span><span class="sxs-lookup"><span data-stu-id="5f648-792">CC001</span></span></td>
<td><span data-ttu-id="5f648-793">Mannauður</span><span class="sxs-lookup"><span data-stu-id="5f648-793">HR</span></span></td>
<td><span data-ttu-id="5f648-794">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-794">10001</span></span></td>
<td><span data-ttu-id="5f648-795">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-795">Electricity</span></span></td>
<td><span data-ttu-id="5f648-796">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-796">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-797">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="5f648-797">-1,245.71</span></span></td>
<td><span data-ttu-id="5f648-798">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-798">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-799">CC002</span><span class="sxs-lookup"><span data-stu-id="5f648-799">CC002</span></span></td>
<td><span data-ttu-id="5f648-800">Fjármál</span><span class="sxs-lookup"><span data-stu-id="5f648-800">Finance</span></span></td>
<td><span data-ttu-id="5f648-801">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-801">10001</span></span></td>
<td><span data-ttu-id="5f648-802">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-802">Electricity</span></span></td>
<td><span data-ttu-id="5f648-803">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-803">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-804">436.00</span><span class="sxs-lookup"><span data-stu-id="5f648-804">436.00</span></span></td>
<td><span data-ttu-id="5f648-805">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-805">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-806">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-806">CC003</span></span></td>
<td><span data-ttu-id="5f648-807">Smölun</span><span class="sxs-lookup"><span data-stu-id="5f648-807">Assembly</span></span></td>
<td><span data-ttu-id="5f648-808">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-808">10001</span></span></td>
<td><span data-ttu-id="5f648-809">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-809">Electricity</span></span></td>
<td><span data-ttu-id="5f648-810">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-810">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-811">685.14</span><span class="sxs-lookup"><span data-stu-id="5f648-811">685.14</span></span></td>
<td><span data-ttu-id="5f648-812">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-812">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-813">CC004</span><span class="sxs-lookup"><span data-stu-id="5f648-813">CC004</span></span></td>
<td><span data-ttu-id="5f648-814">Pakkning</span><span class="sxs-lookup"><span data-stu-id="5f648-814">Packaging</span></span></td>
<td><span data-ttu-id="5f648-815">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-815">10001</span></span></td>
<td><span data-ttu-id="5f648-816">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-816">Electricity</span></span></td>
<td><span data-ttu-id="5f648-817">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-817">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-818">124.57</span><span class="sxs-lookup"><span data-stu-id="5f648-818">124.57</span></span></td>
<td><span data-ttu-id="5f648-819">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-819">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-820">CC002</span><span class="sxs-lookup"><span data-stu-id="5f648-820">CC002</span></span></td>
<td><span data-ttu-id="5f648-821">Fjármál</span><span class="sxs-lookup"><span data-stu-id="5f648-821">Finance</span></span></td>
<td><span data-ttu-id="5f648-822">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-822">10001</span></span></td>
<td><span data-ttu-id="5f648-823">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-823">Electricity</span></span></td>
<td><span data-ttu-id="5f648-824">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-824">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-825">-675,00</span><span class="sxs-lookup"><span data-stu-id="5f648-825">-675.00</span></span></td>
<td><span data-ttu-id="5f648-826">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-826">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-827">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-827">CC003</span></span></td>
<td><span data-ttu-id="5f648-828">Smölun</span><span class="sxs-lookup"><span data-stu-id="5f648-828">Assembly</span></span></td>
<td><span data-ttu-id="5f648-829">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-829">10001</span></span></td>
<td><span data-ttu-id="5f648-830">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-830">Electricity</span></span></td>
<td><span data-ttu-id="5f648-831">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-831">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-832">438.75</span><span class="sxs-lookup"><span data-stu-id="5f648-832">438.75</span></span></td>
<td><span data-ttu-id="5f648-833">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-833">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-834">CC004</span><span class="sxs-lookup"><span data-stu-id="5f648-834">CC004</span></span></td>
<td><span data-ttu-id="5f648-835">Pakkning</span><span class="sxs-lookup"><span data-stu-id="5f648-835">Packaging</span></span></td>
<td><span data-ttu-id="5f648-836">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-836">10001</span></span></td>
<td><span data-ttu-id="5f648-837">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-837">Electricity</span></span></td>
<td><span data-ttu-id="5f648-838">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-838">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-839">236.25</span><span class="sxs-lookup"><span data-stu-id="5f648-839">236.25</span></span></td>
<td><span data-ttu-id="5f648-840">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-840">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-841">CC002</span><span class="sxs-lookup"><span data-stu-id="5f648-841">CC002</span></span></td>
<td><span data-ttu-id="5f648-842">Fjármál</span><span class="sxs-lookup"><span data-stu-id="5f648-842">Finance</span></span></td>
<td><span data-ttu-id="5f648-843">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-843">10001</span></span></td>
<td><span data-ttu-id="5f648-844">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-844">Electricity</span></span></td>
<td><span data-ttu-id="5f648-845">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-845">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-846">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="5f648-846">-8,150.29</span></span></td>
<td><span data-ttu-id="5f648-847">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-847">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-848">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-848">CC003</span></span></td>
<td><span data-ttu-id="5f648-849">Smölun</span><span class="sxs-lookup"><span data-stu-id="5f648-849">Assembly</span></span></td>
<td><span data-ttu-id="5f648-850">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-850">10001</span></span></td>
<td><span data-ttu-id="5f648-851">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-851">Electricity</span></span></td>
<td><span data-ttu-id="5f648-852">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-852">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-853">5,297.69</span><span class="sxs-lookup"><span data-stu-id="5f648-853">5,297.69</span></span></td>
<td><span data-ttu-id="5f648-854">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-854">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-855">CC004</span><span class="sxs-lookup"><span data-stu-id="5f648-855">CC004</span></span></td>
<td><span data-ttu-id="5f648-856">Pakkning</span><span class="sxs-lookup"><span data-stu-id="5f648-856">Packaging</span></span></td>
<td><span data-ttu-id="5f648-857">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-857">10001</span></span></td>
<td><span data-ttu-id="5f648-858">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-858">Electricity</span></span></td>
<td><span data-ttu-id="5f648-859">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-859">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-860">2,852.60</span><span class="sxs-lookup"><span data-stu-id="5f648-860">2,852.60</span></span></td>
<td><span data-ttu-id="5f648-861">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-861">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-862">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-862">CC003</span></span></td>
<td><span data-ttu-id="5f648-863">Smölun</span><span class="sxs-lookup"><span data-stu-id="5f648-863">Assembly</span></span></td>
<td><span data-ttu-id="5f648-864">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-864">10001</span></span></td>
<td><span data-ttu-id="5f648-865">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-865">Electricity</span></span></td>
<td><span data-ttu-id="5f648-866">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-866">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-867">-713,75</span><span class="sxs-lookup"><span data-stu-id="5f648-867">-713.75</span></span></td>
<td><span data-ttu-id="5f648-868">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-868">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-869">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-869">Prod 1</span></span></td>
<td><span data-ttu-id="5f648-870">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-870">Product 1</span></span></td>
<td><span data-ttu-id="5f648-871">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-871">10001</span></span></td>
<td><span data-ttu-id="5f648-872">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-872">Electricity</span></span></td>
<td><span data-ttu-id="5f648-873">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-873">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-874">535.31</span><span class="sxs-lookup"><span data-stu-id="5f648-874">535.31</span></span></td>
<td><span data-ttu-id="5f648-875">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-875">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-876">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-876">Prod 2</span></span></td>
<td><span data-ttu-id="5f648-877">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-877">Product 2</span></span></td>
<td><span data-ttu-id="5f648-878">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-878">10001</span></span></td>
<td><span data-ttu-id="5f648-879">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-879">Electricity</span></span></td>
<td><span data-ttu-id="5f648-880">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-880">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-881">178.44</span><span class="sxs-lookup"><span data-stu-id="5f648-881">178.44</span></span></td>
<td><span data-ttu-id="5f648-882">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-882">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-883">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-883">CC003</span></span></td>
<td><span data-ttu-id="5f648-884">Smölun</span><span class="sxs-lookup"><span data-stu-id="5f648-884">Assembly</span></span></td>
<td><span data-ttu-id="5f648-885">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-885">10001</span></span></td>
<td><span data-ttu-id="5f648-886">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-886">Electricity</span></span></td>
<td><span data-ttu-id="5f648-887">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-887">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-888">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="5f648-888">-5,982.83</span></span></td>
<td><span data-ttu-id="5f648-889">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-889">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-890">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-890">Prod 1</span></span></td>
<td><span data-ttu-id="5f648-891">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-891">Product 1</span></span></td>
<td><span data-ttu-id="5f648-892">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-892">10001</span></span></td>
<td><span data-ttu-id="5f648-893">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-893">Electricity</span></span></td>
<td><span data-ttu-id="5f648-894">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-894">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-895">4,487.12</span><span class="sxs-lookup"><span data-stu-id="5f648-895">4,487.12</span></span></td>
<td><span data-ttu-id="5f648-896">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-896">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-897">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-897">Prod 2</span></span></td>
<td><span data-ttu-id="5f648-898">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-898">Product 2</span></span></td>
<td><span data-ttu-id="5f648-899">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-899">10001</span></span></td>
<td><span data-ttu-id="5f648-900">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-900">Electricity</span></span></td>
<td><span data-ttu-id="5f648-901">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-901">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-902">1,495.71</span><span class="sxs-lookup"><span data-stu-id="5f648-902">1,495.71</span></span></td>
<td><span data-ttu-id="5f648-903">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-903">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-904">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-904">CC003</span></span></td>
<td><span data-ttu-id="5f648-905">Smölun</span><span class="sxs-lookup"><span data-stu-id="5f648-905">Assembly</span></span></td>
<td><span data-ttu-id="5f648-906">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-906">10001</span></span></td>
<td><span data-ttu-id="5f648-907">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-907">Electricity</span></span></td>
<td><span data-ttu-id="5f648-908">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-908">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-909">-286,25</span><span class="sxs-lookup"><span data-stu-id="5f648-909">-286.25</span></span></td>
<td><span data-ttu-id="5f648-910">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-910">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-911">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-911">Prod 1</span></span></td>
<td><span data-ttu-id="5f648-912">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-912">Product 1</span></span></td>
<td><span data-ttu-id="5f648-913">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-913">10001</span></span></td>
<td><span data-ttu-id="5f648-914">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-914">Electricity</span></span></td>
<td><span data-ttu-id="5f648-915">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-915">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-916">241.05</span><span class="sxs-lookup"><span data-stu-id="5f648-916">241.05</span></span></td>
<td><span data-ttu-id="5f648-917">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-917">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-918">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-918">Prod 2</span></span></td>
<td><span data-ttu-id="5f648-919">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-919">Product 2</span></span></td>
<td><span data-ttu-id="5f648-920">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-920">10001</span></span></td>
<td><span data-ttu-id="5f648-921">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-921">Electricity</span></span></td>
<td><span data-ttu-id="5f648-922">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-922">Fixed cost</span></span></td>
<td><span data-ttu-id="5f648-923">45.20</span><span class="sxs-lookup"><span data-stu-id="5f648-923">45.20</span></span></td>
<td><span data-ttu-id="5f648-924">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-924">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-925">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-925">CC003</span></span></td>
<td><span data-ttu-id="5f648-926">Smölun</span><span class="sxs-lookup"><span data-stu-id="5f648-926">Assembly</span></span></td>
<td><span data-ttu-id="5f648-927">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-927">10001</span></span></td>
<td><span data-ttu-id="5f648-928">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-928">Electricity</span></span></td>
<td><span data-ttu-id="5f648-929">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-929">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-930">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="5f648-930">-2,977.17</span></span></td>
<td><span data-ttu-id="5f648-931">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-931">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-932">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-932">Prod 1</span></span></td>
<td><span data-ttu-id="5f648-933">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-933">Product 1</span></span></td>
<td><span data-ttu-id="5f648-934">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-934">10001</span></span></td>
<td><span data-ttu-id="5f648-935">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-935">Electricity</span></span></td>
<td><span data-ttu-id="5f648-936">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-936">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-937">2,507.09</span><span class="sxs-lookup"><span data-stu-id="5f648-937">2,507.09</span></span></td>
<td><span data-ttu-id="5f648-938">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-938">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5f648-939">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-939">Prod 2</span></span></td>
<td><span data-ttu-id="5f648-940">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-940">Product 2</span></span></td>
<td><span data-ttu-id="5f648-941">10001</span><span class="sxs-lookup"><span data-stu-id="5f648-941">10001</span></span></td>
<td><span data-ttu-id="5f648-942">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-942">Electricity</span></span></td>
<td><span data-ttu-id="5f648-943">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-943">Variable cost</span></span></td>
<td><span data-ttu-id="5f648-944">470.08</span><span class="sxs-lookup"><span data-stu-id="5f648-944">470.08</span></span></td>
<td><span data-ttu-id="5f648-945">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="5f648-945">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="5f648-946">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="5f648-946">Conclusion</span></span>
<span data-ttu-id="5f648-947">Í Fjárhagsbókhaldi er kostnaður upp á 10.000,00 fyrir rafmagn bókaður á kenni leppkostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="5f648-947">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="5f648-948">Þar af leiðandi munu kostnaðarbókarar vita að það þarf að úthluta þessum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="5f648-948">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="5f648-949">Í kostnaðarbókhaldi streymir kostnaður þvert á fyrirtækiseiningar og stig, samkvæmt þeim stefnum og reglum sem eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="5f648-949">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="5f648-950">Hver kostnaður hefur verið tengdur úthlutunargrunni sem veitir besta mat á úthlutun á kostnaði.</span><span class="sxs-lookup"><span data-stu-id="5f648-950">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="5f648-951">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="5f648-951">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="5f648-952">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="5f648-952">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="5f648-953">Samtala</span><span class="sxs-lookup"><span data-stu-id="5f648-953">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5f648-954">CC099</span><span class="sxs-lookup"><span data-stu-id="5f648-954">CC099</span></span></th>
<th><span data-ttu-id="5f648-955">CC001</span><span class="sxs-lookup"><span data-stu-id="5f648-955">CC001</span></span></th>
<th><span data-ttu-id="5f648-956">CC002</span><span class="sxs-lookup"><span data-stu-id="5f648-956">CC002</span></span></th>
<th><span data-ttu-id="5f648-957">CC003</span><span class="sxs-lookup"><span data-stu-id="5f648-957">CC003</span></span></th>
<th><span data-ttu-id="5f648-958">CC004</span><span class="sxs-lookup"><span data-stu-id="5f648-958">CC004</span></span></th>
<th><span data-ttu-id="5f648-959">Verk 1</span><span class="sxs-lookup"><span data-stu-id="5f648-959">Proj 1</span></span></th>
<th><span data-ttu-id="5f648-960">Verk 2</span><span class="sxs-lookup"><span data-stu-id="5f648-960">Proj 2</span></span></th>
<th><span data-ttu-id="5f648-961">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="5f648-961">Prod 1</span></span></th>
<th><span data-ttu-id="5f648-962">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="5f648-962">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="5f648-963">10001 Rafmagn</span><span class="sxs-lookup"><span data-stu-id="5f648-963">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5f648-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-965"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5f648-965"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-966"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5f648-966"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-967"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="5f648-967"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5f648-968"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="5f648-968"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-969"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="5f648-969"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-970"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="5f648-970"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-971"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="5f648-971"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-972"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5f648-972"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="5f648-973">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="5f648-973">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-974">0,00</span><span class="sxs-lookup"><span data-stu-id="5f648-974">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="5f648-975">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-975">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-976">0,00</span><span class="sxs-lookup"><span data-stu-id="5f648-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-977">0,00</span><span class="sxs-lookup"><span data-stu-id="5f648-977">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-978">0,00</span><span class="sxs-lookup"><span data-stu-id="5f648-978">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-979">0,00</span><span class="sxs-lookup"><span data-stu-id="5f648-979">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-980">0,00</span><span class="sxs-lookup"><span data-stu-id="5f648-980">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="5f648-981">776.36</span><span class="sxs-lookup"><span data-stu-id="5f648-981">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-982">223.64</span><span class="sxs-lookup"><span data-stu-id="5f648-982">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-983"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5f648-983"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="5f648-984">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="5f648-984">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-985">000</span><span class="sxs-lookup"><span data-stu-id="5f648-985">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-986">0,00</span><span class="sxs-lookup"><span data-stu-id="5f648-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-987">0,00</span><span class="sxs-lookup"><span data-stu-id="5f648-987">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-988">0,00</span><span class="sxs-lookup"><span data-stu-id="5f648-988">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-989">0,00</span><span class="sxs-lookup"><span data-stu-id="5f648-989">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-990">30,00</span><span class="sxs-lookup"><span data-stu-id="5f648-990">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-991">10,00</span><span class="sxs-lookup"><span data-stu-id="5f648-991">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-992">6,994.21</span><span class="sxs-lookup"><span data-stu-id="5f648-992">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-993">1,965.79</span><span class="sxs-lookup"><span data-stu-id="5f648-993">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="5f648-994"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="5f648-994"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="5f648-995">Þetta efnisatriði sýnir hvernig fyrir aðalkostnaðareiningin 10001 Rafmagn flæðir í gegnum kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="5f648-995">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="5f648-996">Þar af leiðandi er þessum sameiginlega kostnaði úthlutað á lægsta stigið í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="5f648-996">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="5f648-997">Með öðrum orðum bera kostnaðarhlutir á lægsta stiginu kostnaðinn.</span><span class="sxs-lookup"><span data-stu-id="5f648-997">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="5f648-998">Ef þú þarft sjónrænt flæði kostnaðar á milli kostnaðarhluta er hægt að nota stefnureglur samantekins kostnaðar til að gera kostnaðarflæðið sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="5f648-998">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="5f648-999">Ítarlegri upplýsingar eru í Reglu samantekins kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="5f648-999">For more detailed information, see Cost roll-up policy.</span></span> <span data-ttu-id="5f648-1000">(Athugaðu að þetta efnisatriði hefur ekki enn verið fullklárað en er væntanlegt.)</span><span class="sxs-lookup"><span data-stu-id="5f648-1000">(Note that this topic isn't competed yet but is coming soon.)</span></span>




