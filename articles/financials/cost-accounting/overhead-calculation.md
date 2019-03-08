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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272163
ms.assetid: 93119afb-47ed-4786-ba44-ba93576d3e28
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: 4de705324ac497cfb11fae3dadc6f57d038fd0b5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "335118"
---
# <a name="overhead-calculation"></a><span data-ttu-id="9fe8e-103">Útreikningur fastakostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9fe8e-104">Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="9fe8e-105">Skýrsluskilgreining</span><span class="sxs-lookup"><span data-stu-id="9fe8e-105">Term definition</span></span>
---------------

<span data-ttu-id="9fe8e-106">Stjórnunarkostnaður er sá kostnaður sem stofnað er til fyrir rekstur fyrirtækis, en sem ekki er hægt að rekja beint til neinna sérstakrar starfsemi, vöru eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="9fe8e-107">Stjórnunarkostnaður veitir mikilvægan stuðning við myndun hagnaðarmyndandi verkþátta.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="9fe8e-108">Hér eru nokkur dæmi um skilyrði:</span><span class="sxs-lookup"><span data-stu-id="9fe8e-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="9fe8e-109">Leiga</span><span class="sxs-lookup"><span data-stu-id="9fe8e-109">Rent</span></span>
-   <span data-ttu-id="9fe8e-110">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-110">Electricity</span></span>
-   <span data-ttu-id="9fe8e-111">Stjórnunarkostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="9fe8e-112">Yfirlit yfir útreikning fastakostnaðar</span><span class="sxs-lookup"><span data-stu-id="9fe8e-112">Overhead calculation overview</span></span>
<span data-ttu-id="9fe8e-113">Útreikningur fastakostnaðar keyrir reglur kostnaðarbókhalds í réttri röð.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="9fe8e-114">Hægt er að keyra útreikning fastakostnaðar margsinnis fyrir sama fjárhagstímabil ef reglum kostnaðarbókhalds hefur verið breytt eða ákveðnar villur hafa fundist.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="9fe8e-115">Hver keyrsla á útreikningi fastakostnaðar er geymd og fær einkvæmt útgáfukenni sem gerir kleift að bera saman útreikning í mismunandi útgáfum.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="9fe8e-116">Kostnaðarfærslur sem útreikningur fastakostnaðar mynda fá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="9fe8e-117">Dagsetningin bókhald samsvarar lokadagsetning fjárhagstímabilsins sem er dagsetning reikningsskiladagsetning reikningsskila notað í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="9fe8e-118">Einkvæmt útgáfukenni samanstendur af eftirfarandi þáttum:</span><span class="sxs-lookup"><span data-stu-id="9fe8e-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="9fe8e-119">Gerð útgáfu</span><span class="sxs-lookup"><span data-stu-id="9fe8e-119">Version type</span></span>
-   <span data-ttu-id="9fe8e-120">Dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="9fe8e-120">Date and time</span></span>
-   <span data-ttu-id="9fe8e-121">Fjárhagur kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="9fe8e-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="9fe8e-122">Fjárhagsár</span><span class="sxs-lookup"><span data-stu-id="9fe8e-122">Fiscal year</span></span>
-   <span data-ttu-id="9fe8e-123">Reikningstímabil</span><span class="sxs-lookup"><span data-stu-id="9fe8e-123">Fiscal period</span></span>

<span data-ttu-id="9fe8e-124">Útreikningur fastakostnaðar er keyrður óháð því hver útgáfan er.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="9fe8e-125">Þess vegna er hægt að reikna út áætlaða útgáfu á undan raunútgáfu.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="9fe8e-126">Útreikningur fastakostnaðar samanstendur af fjórum skrefum, eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="9fe8e-127">Í hverju skrefi er færslubókarhaus stofnaður með bókarfærslum.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="9fe8e-128">Þessi færslubókarhaus geymir inntaksgögn fyrir hvert útreikningsþrep.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="9fe8e-129">Stefnur og reglur eru notaðar í hverri færslulínu og kostnaðarfærslur eru myndaðar sem úttak.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="9fe8e-130">Þess vegna hefurðu ávallt fullan rekjanleika.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="9fe8e-131">[![Útreikningur fastakostnaðar](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="9fe8e-132">Reikna og úthluta sameiginlegur kostnaði vegna rafmagns</span><span class="sxs-lookup"><span data-stu-id="9fe8e-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="9fe8e-133">Í Fjárhagsbókhaldi er ákveðinn kostnaður, eins og rafmagn, skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="9fe8e-134">Þar af leiðandi er nákvæmar innsýn rekstrarfélags ekki veitt fyrir kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="9fe8e-135">Í kostnaðarbókhaldi verður kostnaður að flæða í gegnum fyrirtækiseiningar til að veita rétta innsýn rekstrarfélags þvert á allar fyrirtækiseiningar og stig.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="9fe8e-136">Þetta flæði verður að byggja á annaðhvort nákvæmri færslu notkunar eða sanngjarnri matsreglu.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="9fe8e-137">Í fjárhagnum er hægt að bóka rafmagnskostnað eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9fe8e-138">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="9fe8e-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9fe8e-139">Kostnaðarstaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="9fe8e-140">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="9fe8e-140">Main account</span></span></th>
<th><span data-ttu-id="9fe8e-141">Upphæð í bókhaldsgjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="9fe8e-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-142">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="9fe8e-143">CC099</span><span class="sxs-lookup"><span data-stu-id="9fe8e-143">CC099</span></span></td>
<td><span data-ttu-id="9fe8e-144">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-144">Default cost center</span></span></td>
<td><span data-ttu-id="9fe8e-145">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-145">10001</span></span></td>
<td><span data-ttu-id="9fe8e-146">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-146">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="9fe8e-148">Skref 1: Keyra útreikning kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="9fe8e-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="9fe8e-149">Sjálfvirkt er að þegar kostnaðarfærslur eru fluttar úr grunngögnum fái þær flokkun kostnaðarhegðunar **Óflokkað** í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="9fe8e-150">Með því að nota stefnureglur kostnaðarhegðunar er hægt að endurflokka kostnaðarfærslur sem annaðhvort **Fastan kostnað** eða **Breytilegan kostnað**.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="9fe8e-151">Tilgreinið reglu kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="9fe8e-151">Define the cost behavior rule</span></span>

<span data-ttu-id="9fe8e-152">Í sumum tilfellum er hluti af kostnaði föst þóknun og eftirstandandi kostnaður byggist á notkun.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="9fe8e-153">Rafmagnsreikningar stemma oft við þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="9fe8e-154">Þegar tiltekin föst þóknun hefur verið greidd, er greitt fyrir notkun á kílóvattklukkustund (Kwh).</span><span class="sxs-lookup"><span data-stu-id="9fe8e-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="9fe8e-155">Til dæmis ef föst kostnaðarþóknun er 1000.00 sýnir þetta hvernig regla kostnaðarhegðunar er skilgreind:</span><span class="sxs-lookup"><span data-stu-id="9fe8e-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="9fe8e-156">Föst upphæð 1.000,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="9fe8e-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="9fe8e-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="9fe8e-158">1000.01 &lt; N = Breyta</span><span class="sxs-lookup"><span data-stu-id="9fe8e-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="9fe8e-159">Færslubók</span><span class="sxs-lookup"><span data-stu-id="9fe8e-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9fe8e-160">Færslubók</span><span class="sxs-lookup"><span data-stu-id="9fe8e-160">Journal</span></span></th>
<th><span data-ttu-id="9fe8e-161">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="9fe8e-162">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="9fe8e-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="9fe8e-163">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="9fe8e-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-164">00001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-164">00001</span></span></td>
<td><span data-ttu-id="9fe8e-165">Færslubók útreiknings fyrir kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="9fe8e-166">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-166">Fiscal</span></span></td>
<td><span data-ttu-id="9fe8e-167">2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-167">2017</span></span></td>
<td><span data-ttu-id="9fe8e-168">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="9fe8e-168">Period 1</span></span></td>
<td><span data-ttu-id="9fe8e-169">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="9fe8e-170">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9fe8e-171">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="9fe8e-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9fe8e-172">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9fe8e-173">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9fe8e-173">Cost element</span></span></th>
<th><span data-ttu-id="9fe8e-174">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-174">Cost behavior</span></span></th>
<th><span data-ttu-id="9fe8e-175">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-176">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="9fe8e-177">CC099</span><span class="sxs-lookup"><span data-stu-id="9fe8e-177">CC099</span></span></td>
<td><span data-ttu-id="9fe8e-178">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-178">Default cost center</span></span></td>
<td><span data-ttu-id="9fe8e-179">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-179">10001</span></span></td>
<td><span data-ttu-id="9fe8e-180">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-180">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-181">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="9fe8e-181">Unclassified</span></span></td>
<td><span data-ttu-id="9fe8e-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="9fe8e-183">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9fe8e-184">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9fe8e-185">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9fe8e-185">Cost element</span></span></th>
<th><span data-ttu-id="9fe8e-186">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-186">Cost behavior</span></span></th>
<th><span data-ttu-id="9fe8e-187">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-187">Amount</span></span></th>
<th><span data-ttu-id="9fe8e-188">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="9fe8e-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-189">CC099</span><span class="sxs-lookup"><span data-stu-id="9fe8e-189">CC099</span></span></td>
<td><span data-ttu-id="9fe8e-190">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-190">Default cost center</span></span></td>
<td><span data-ttu-id="9fe8e-191">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-191">10001</span></span></td>
<td><span data-ttu-id="9fe8e-192">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-192">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-193">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="9fe8e-193">Unclassified</span></span></td>
<td><span data-ttu-id="9fe8e-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-194">10,000.00</span></span></td>
<td><span data-ttu-id="9fe8e-195">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-196">CC099</span><span class="sxs-lookup"><span data-stu-id="9fe8e-196">CC099</span></span></td>
<td><span data-ttu-id="9fe8e-197">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-197">Default cost center</span></span></td>
<td><span data-ttu-id="9fe8e-198">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-198">10001</span></span></td>
<td><span data-ttu-id="9fe8e-199">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-199">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-200">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="9fe8e-200">Unclassified</span></span></td>
<td><span data-ttu-id="9fe8e-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-201">-10,000.00</span></span></td>
<td><span data-ttu-id="9fe8e-202">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-203">CC099</span><span class="sxs-lookup"><span data-stu-id="9fe8e-203">CC099</span></span></td>
<td><span data-ttu-id="9fe8e-204">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-204">Default cost center</span></span></td>
<td><span data-ttu-id="9fe8e-205">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-205">10001</span></span></td>
<td><span data-ttu-id="9fe8e-206">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-206">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-207">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-207">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-208">1,000.00</span></span></td>
<td><span data-ttu-id="9fe8e-209">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-210">CC099</span><span class="sxs-lookup"><span data-stu-id="9fe8e-210">CC099</span></span></td>
<td><span data-ttu-id="9fe8e-211">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-211">Default cost center</span></span></td>
<td><span data-ttu-id="9fe8e-212">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-212">10001</span></span></td>
<td><span data-ttu-id="9fe8e-213">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-213">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-214">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-214">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-215">9,000.00</span></span></td>
<td><span data-ttu-id="9fe8e-216">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9fe8e-217">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðarhegðunarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="9fe8e-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="9fe8e-218">Skref 2: Keyra útreikning kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="9fe8e-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="9fe8e-219">Kostnaðardreifing er notuð til að endurúthluta kostnaði frá einum kostnaðarhlut til annars eða fleiri kostnaðarhluta með því að nota viðeigandi úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="9fe8e-220">Kostnaðardreifing og kostnaðarúthlutun eru ólíkar að því leyti að kostnaðardreifing kemur alltaf upp á stigi aðalkostnaðareiningar upphaflegs verðs.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="9fe8e-221">Tilgreinið kostnaðardreifingarreglu</span><span class="sxs-lookup"><span data-stu-id="9fe8e-221">Define the cost distribution rule</span></span>

<span data-ttu-id="9fe8e-222">Í Fjárhagsbókhaldi er rafmagnskostnaður oft skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="9fe8e-223">Í kostnaðarbókhaldi er þessi nálgun ekki nógu nákvæm.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="9fe8e-224">Breytilegur kostnaði þarf að dreifa á staka kostnaðarhluti á sanngjörnum grunni.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="9fe8e-225">Rökréttasti úthlutunargrunnurinn er notkun á rafmagni (Kwh).</span><span class="sxs-lookup"><span data-stu-id="9fe8e-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="9fe8e-226">Stofnað er tölfræðilegt víddarstak sem er nefnt Rafmagn og rafmagnsnotkun er skráð.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="9fe8e-227">Sjálfgefið er að öll tölfræðileg víddarstök verða tiltæk sem úthlutunargrunnur.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9fe8e-228">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-228">Cost object</span></span></th>
<th><span data-ttu-id="9fe8e-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="9fe8e-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-230">CC001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-230">CC001</span></span></td>
<td><span data-ttu-id="9fe8e-231">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-231">HR</span></span></td>
<td><span data-ttu-id="9fe8e-232">1.000</span><span class="sxs-lookup"><span data-stu-id="9fe8e-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-233">CC002</span><span class="sxs-lookup"><span data-stu-id="9fe8e-233">CC002</span></span></td>
<td><span data-ttu-id="9fe8e-234">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9fe8e-234">Finance</span></span></td>
<td><span data-ttu-id="9fe8e-235">6,000</span><span class="sxs-lookup"><span data-stu-id="9fe8e-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-236">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-236">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-237">Smölun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-237">Assembly</span></span></td>
<td><span data-ttu-id="9fe8e-238">0</span><span class="sxs-lookup"><span data-stu-id="9fe8e-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9fe8e-239">Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunni fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9fe8e-240">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-240">Cost object</span></span></th>
<th><span data-ttu-id="9fe8e-241">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="9fe8e-241">Magnitude</span></span></th>
<th><span data-ttu-id="9fe8e-242">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-242">Allocation factor</span></span></th>
<th><span data-ttu-id="9fe8e-243">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-244">CC001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-244">CC001</span></span></td>
<td><span data-ttu-id="9fe8e-245">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-245">HR</span></span></td>
<td><span data-ttu-id="9fe8e-246">1.000</span><span class="sxs-lookup"><span data-stu-id="9fe8e-246">1,000</span></span></td>
<td><span data-ttu-id="9fe8e-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="9fe8e-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="9fe8e-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-249">CC002</span><span class="sxs-lookup"><span data-stu-id="9fe8e-249">CC002</span></span></td>
<td><span data-ttu-id="9fe8e-250">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9fe8e-250">Finance</span></span></td>
<td><span data-ttu-id="9fe8e-251">6,000</span><span class="sxs-lookup"><span data-stu-id="9fe8e-251">6,000</span></span></td>
<td><span data-ttu-id="9fe8e-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="9fe8e-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="9fe8e-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-254">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-254">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-255">Smölun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-255">Assembly</span></span></td>
<td><span data-ttu-id="9fe8e-256">0</span><span class="sxs-lookup"><span data-stu-id="9fe8e-256">0</span></span></td>
<td><span data-ttu-id="9fe8e-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="9fe8e-258">0,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9fe8e-259">Föstum kostnaði þarf að dreifa jafnt á staka kostnaðarhluti sem hafa notað rafmagn.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="9fe8e-260">Hægt er að ná þessa niðurstöðu með því að nota tölfræðilegt víddarstakið Rafmagn í úthlutunargrunni reikniformúlu: (Rafmagn &gt; 0,00) Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunn fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9fe8e-261">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-261">Cost object</span></span></th>
<th><span data-ttu-id="9fe8e-262">Formúla</span><span class="sxs-lookup"><span data-stu-id="9fe8e-262">Formula</span></span></th>
<th><span data-ttu-id="9fe8e-263">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="9fe8e-263">Magnitude</span></span></th>
<th><span data-ttu-id="9fe8e-264">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-264">Allocation factor</span></span></th>
<th><span data-ttu-id="9fe8e-265">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-266">CC001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-266">CC001</span></span></td>
<td><span data-ttu-id="9fe8e-267">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-267">HR</span></span></td>
<td><span data-ttu-id="9fe8e-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="9fe8e-269">1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-269">1</span></span></td>
<td><span data-ttu-id="9fe8e-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="9fe8e-271">500,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-272">CC002</span><span class="sxs-lookup"><span data-stu-id="9fe8e-272">CC002</span></span></td>
<td><span data-ttu-id="9fe8e-273">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9fe8e-273">Finance</span></span></td>
<td><span data-ttu-id="9fe8e-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="9fe8e-275">1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-275">1</span></span></td>
<td><span data-ttu-id="9fe8e-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="9fe8e-277">500,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-278">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-278">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-279">Smölun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-279">Assembly</span></span></td>
<td><span data-ttu-id="9fe8e-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="9fe8e-281">0</span><span class="sxs-lookup"><span data-stu-id="9fe8e-281">0</span></span></td>
<td><span data-ttu-id="9fe8e-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="9fe8e-283">0,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="9fe8e-284">Færslubók</span><span class="sxs-lookup"><span data-stu-id="9fe8e-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9fe8e-285">Færslubók</span><span class="sxs-lookup"><span data-stu-id="9fe8e-285">Journal</span></span></th>
<th><span data-ttu-id="9fe8e-286">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="9fe8e-287">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="9fe8e-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="9fe8e-288">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="9fe8e-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-289">00002</span><span class="sxs-lookup"><span data-stu-id="9fe8e-289">00002</span></span></td>
<td><span data-ttu-id="9fe8e-290">Útreikningabók kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="9fe8e-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="9fe8e-291">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-291">Fiscal</span></span></td>
<td><span data-ttu-id="9fe8e-292">2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-292">2017</span></span></td>
<td><span data-ttu-id="9fe8e-293">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="9fe8e-293">Period 1</span></span></td>
<td><span data-ttu-id="9fe8e-294">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="9fe8e-295">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9fe8e-296">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="9fe8e-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9fe8e-297">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9fe8e-298">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9fe8e-298">Cost element</span></span></th>
<th><span data-ttu-id="9fe8e-299">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-299">Cost behavior</span></span></th>
<th><span data-ttu-id="9fe8e-300">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-301">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="9fe8e-302">CC099</span><span class="sxs-lookup"><span data-stu-id="9fe8e-302">CC099</span></span></td>
<td><span data-ttu-id="9fe8e-303">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-303">Default cost center</span></span></td>
<td><span data-ttu-id="9fe8e-304">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-304">10001</span></span></td>
<td><span data-ttu-id="9fe8e-305">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-305">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-306">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-306">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-308">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="9fe8e-309">CC099</span><span class="sxs-lookup"><span data-stu-id="9fe8e-309">CC099</span></span></td>
<td><span data-ttu-id="9fe8e-310">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-310">Default cost center</span></span></td>
<td><span data-ttu-id="9fe8e-311">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-311">10001</span></span></td>
<td><span data-ttu-id="9fe8e-312">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-312">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-313">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-313">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="9fe8e-315">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9fe8e-316">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9fe8e-317">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9fe8e-317">Cost element</span></span></th>
<th><span data-ttu-id="9fe8e-318">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-318">Cost behavior</span></span></th>
<th><span data-ttu-id="9fe8e-319">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-319">Amount</span></span></th>
<th><span data-ttu-id="9fe8e-320">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="9fe8e-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-321">CC099</span><span class="sxs-lookup"><span data-stu-id="9fe8e-321">CC099</span></span></td>
<td><span data-ttu-id="9fe8e-322">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-322">Default cost center</span></span></td>
<td><span data-ttu-id="9fe8e-323">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-323">10001</span></span></td>
<td><span data-ttu-id="9fe8e-324">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-324">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-325">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-325">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-326">-1,000.00</span></span></td>
<td><span data-ttu-id="9fe8e-327">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-328">CC001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-328">CC001</span></span></td>
<td><span data-ttu-id="9fe8e-329">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-329">HR</span></span></td>
<td><span data-ttu-id="9fe8e-330">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-330">10001</span></span></td>
<td><span data-ttu-id="9fe8e-331">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-331">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-332">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-332">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-333">500,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-333">500.00</span></span></td>
<td><span data-ttu-id="9fe8e-334">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-335">CC002</span><span class="sxs-lookup"><span data-stu-id="9fe8e-335">CC002</span></span></td>
<td><span data-ttu-id="9fe8e-336">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9fe8e-336">Finance</span></span></td>
<td><span data-ttu-id="9fe8e-337">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-337">10001</span></span></td>
<td><span data-ttu-id="9fe8e-338">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-338">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-339">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-339">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-340">500,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-340">500.00</span></span></td>
<td><span data-ttu-id="9fe8e-341">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-342">CC099</span><span class="sxs-lookup"><span data-stu-id="9fe8e-342">CC099</span></span></td>
<td><span data-ttu-id="9fe8e-343">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-343">Default cost center</span></span></td>
<td><span data-ttu-id="9fe8e-344">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-344">10001</span></span></td>
<td><span data-ttu-id="9fe8e-345">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-345">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-346">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-346">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-347">-9,000.00</span></span></td>
<td><span data-ttu-id="9fe8e-348">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-349">CC001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-349">CC001</span></span></td>
<td><span data-ttu-id="9fe8e-350">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-350">HR</span></span></td>
<td><span data-ttu-id="9fe8e-351">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-351">10001</span></span></td>
<td><span data-ttu-id="9fe8e-352">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-352">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-353">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-353">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="9fe8e-354">1,285.71</span></span></td>
<td><span data-ttu-id="9fe8e-355">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-356">CC002</span><span class="sxs-lookup"><span data-stu-id="9fe8e-356">CC002</span></span></td>
<td><span data-ttu-id="9fe8e-357">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9fe8e-357">Finance</span></span></td>
<td><span data-ttu-id="9fe8e-358">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-358">10001</span></span></td>
<td><span data-ttu-id="9fe8e-359">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-359">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-360">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-360">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="9fe8e-361">7,714.29</span></span></td>
<td><span data-ttu-id="9fe8e-362">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9fe8e-363">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðardreifingarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="9fe8e-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="9fe8e-364">Skref 3: Keyra útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="9fe8e-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="9fe8e-365">Sameiginlegur kostnaður er notaður til að rukka einn eða fleiri tilgreinda kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="9fe8e-366">Gjöldin byggjast á fyrirframákveðnu kostnaðarhlutfalli og mæligildi úr úthlutuðum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="9fe8e-367">Skilgreina sameiginlegan kostnað</span><span class="sxs-lookup"><span data-stu-id="9fe8e-367">Define the overhead rate</span></span>

<span data-ttu-id="9fe8e-368">Kostnaðarhlutur CC001 Mannauður stuðlar að safni innri verka.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="9fe8e-369">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsverk til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9fe8e-370">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-370">Cost object</span></span></th>
<th><span data-ttu-id="9fe8e-371">Tímar</span><span class="sxs-lookup"><span data-stu-id="9fe8e-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-372">Verk 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-372">Proj 1</span></span></td>
<td><span data-ttu-id="9fe8e-373">Verk 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-373">Project 1</span></span></td>
<td><span data-ttu-id="9fe8e-374">3</span><span class="sxs-lookup"><span data-stu-id="9fe8e-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-375">Verk 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-375">Proj 2</span></span></td>
<td><span data-ttu-id="9fe8e-376">Verk 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-376">Project 2</span></span></td>
<td><span data-ttu-id="9fe8e-377">1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9fe8e-378">Fyrirframákveðið kostnaðarhlutfall fyrir kostnaðarframlag verk hefur verið skilgreint.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9fe8e-379">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-379">Cost object</span></span></th>
<th><span data-ttu-id="9fe8e-380">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9fe8e-380">Cost element</span></span></th>
<th><span data-ttu-id="9fe8e-381">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-381">Cost behavior</span></span></th>
<th><span data-ttu-id="9fe8e-382">Einingar</span><span class="sxs-lookup"><span data-stu-id="9fe8e-382">Units</span></span></th>
<th><span data-ttu-id="9fe8e-383">Taxti</span><span class="sxs-lookup"><span data-stu-id="9fe8e-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-384">CC001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-384">CC001</span></span></td>
<td><span data-ttu-id="9fe8e-385">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-385">HR</span></span></td>
<td><span data-ttu-id="9fe8e-386">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-386">10001</span></span></td>
<td><span data-ttu-id="9fe8e-387">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-387">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-388">1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-388">1</span></span></td>
<td><span data-ttu-id="9fe8e-389">10</span><span class="sxs-lookup"><span data-stu-id="9fe8e-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9fe8e-390">Eftirfarandi tafla sýnir niðurstöður þegar Mannauðsverk eru notuð sem grunnur við úthlutun.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9fe8e-391">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-391">Cost object</span></span></th>
<th><span data-ttu-id="9fe8e-392">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="9fe8e-392">Magnitude</span></span></th>
<th><span data-ttu-id="9fe8e-393">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9fe8e-393">Cost element</span></span></th>
<th><span data-ttu-id="9fe8e-394">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-394">Allocation factor</span></span></th>
<th><span data-ttu-id="9fe8e-395">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-396">Verk 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-396">Proj 1</span></span></td>
<td><span data-ttu-id="9fe8e-397">Verk 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-397">Project 1</span></span></td>
<td><span data-ttu-id="9fe8e-398">3</span><span class="sxs-lookup"><span data-stu-id="9fe8e-398">3</span></span></td>
<td><span data-ttu-id="9fe8e-399">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-399">10001</span></span></td>
<td><span data-ttu-id="9fe8e-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="9fe8e-401">30,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-402">Verk 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-402">Proj 2</span></span></td>
<td><span data-ttu-id="9fe8e-403">Verk 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-403">Project 2</span></span></td>
<td><span data-ttu-id="9fe8e-404">1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-404">1</span></span></td>
<td><span data-ttu-id="9fe8e-405">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-405">10001</span></span></td>
<td><span data-ttu-id="9fe8e-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="9fe8e-407">10,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="9fe8e-408">Færslubók</span><span class="sxs-lookup"><span data-stu-id="9fe8e-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9fe8e-409">Færslubók</span><span class="sxs-lookup"><span data-stu-id="9fe8e-409">Journal</span></span></th>
<th><span data-ttu-id="9fe8e-410">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="9fe8e-411">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="9fe8e-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="9fe8e-412">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="9fe8e-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-413">00003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-413">00003</span></span></td>
<td><span data-ttu-id="9fe8e-414">Færslubók fyrir útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="9fe8e-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="9fe8e-415">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-415">Fiscal</span></span></td>
<td><span data-ttu-id="9fe8e-416">2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-416">2017</span></span></td>
<td><span data-ttu-id="9fe8e-417">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="9fe8e-417">Period 1</span></span></td>
<td><span data-ttu-id="9fe8e-418">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="9fe8e-419">Bókarfærslur (Bókarfærslur fyrir útreikning sameiginlegs kostnaðar)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9fe8e-420">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="9fe8e-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9fe8e-421">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-421">Cost object</span></span></th>
<th><span data-ttu-id="9fe8e-422">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="9fe8e-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-423">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="9fe8e-424">Verk 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-424">Proj 1</span></span></td>
<td><span data-ttu-id="9fe8e-425">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="9fe8e-426">3,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-427">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="9fe8e-428">Verk 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-428">Proj 2</span></span></td>
<td><span data-ttu-id="9fe8e-429">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="9fe8e-430">1,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="9fe8e-431">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9fe8e-432">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9fe8e-433">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9fe8e-433">Cost element</span></span></th>
<th><span data-ttu-id="9fe8e-434">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-434">Cost behavior</span></span></th>
<th><span data-ttu-id="9fe8e-435">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-435">Amount</span></span></th>
<th><span data-ttu-id="9fe8e-436">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="9fe8e-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-437">CC0001</span></span></td>
<td><span data-ttu-id="9fe8e-438">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-438">HR</span></span></td>
<td><span data-ttu-id="9fe8e-439">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-439">10001</span></span></td>
<td><span data-ttu-id="9fe8e-440">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-440">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-441">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-441">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-442">-30.00</span></span></td>
<td><span data-ttu-id="9fe8e-443">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-444">Verk 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-444">Proj 1</span></span></td>
<td><span data-ttu-id="9fe8e-445">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="9fe8e-446">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-446">10001</span></span></td>
<td><span data-ttu-id="9fe8e-447">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-447">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-448">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-448">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-449">30,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-449">30.00</span></span></td>
<td><span data-ttu-id="9fe8e-450">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-451">CC001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-451">CC001</span></span></td>
<td><span data-ttu-id="9fe8e-452">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-452">HR</span></span></td>
<td><span data-ttu-id="9fe8e-453">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-453">10001</span></span></td>
<td><span data-ttu-id="9fe8e-454">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-454">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-455">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-455">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-456">-10.00</span></span></td>
<td><span data-ttu-id="9fe8e-457">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-458">Verk 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-458">Proj 2</span></span></td>
<td><span data-ttu-id="9fe8e-459">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="9fe8e-460">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-460">10001</span></span></td>
<td><span data-ttu-id="9fe8e-461">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-461">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-462">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-462">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-463">10,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-463">10.00</span></span></td>
<td><span data-ttu-id="9fe8e-464">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9fe8e-465">Nánari upplýsingar er að finna í [Framkvæma útreikning fastakostnaðar](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="9fe8e-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="9fe8e-466">Skref 4: Keyra útreikning kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="9fe8e-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="9fe8e-467">Úthlutun er notuð til að úthluta stöðu kostnaðarhlutar í öðrum kostnaðarhlutum með því að nota úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="9fe8e-468">Finance and Operations styður gagnvirka úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-468">Finance and Operations supports the reciprocal allocation method.</span></span> <span data-ttu-id="9fe8e-469">Í gagnvirkri úthlutunaraðferð er sú sameiginlega þjónusta sem hjálparkostnaðarhlutir skiptast á viðurkennd að fullu.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="9fe8e-470">Kerfið ákvarðar sjálfkrafa rétta röð til að framkvæma úthlutun eftir.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="9fe8e-471">Stöðu kostnaðarhluta er úthlutað með einum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="9fe8e-472">Úthlutanir þvert á víddir kostnaðarhluta og viðkomandi stök þeirra eru studdar.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="9fe8e-473">Úthlutun pöntunarinnar er stjórnað af stýrieiningu kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="9fe8e-474">[![Gagnkvæm aðferð](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="9fe8e-475">Tilgreinið kostnaðarúthlutun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-475">Define the cost allocation</span></span>

<span data-ttu-id="9fe8e-476">Hér er einfalt dæmi sem útskýrir hvernig hægt er að rekja flæði kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="9fe8e-477">Kostnaðarhlutir CC001 Mannauður leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="9fe8e-478">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9fe8e-479">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-479">Cost object</span></span></th>
<th><span data-ttu-id="9fe8e-480">Mannauðsþjónusta</span><span class="sxs-lookup"><span data-stu-id="9fe8e-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-481">CC002</span><span class="sxs-lookup"><span data-stu-id="9fe8e-481">CC002</span></span></td>
<td><span data-ttu-id="9fe8e-482">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9fe8e-482">Finance</span></span></td>
<td><span data-ttu-id="9fe8e-483">35</span><span class="sxs-lookup"><span data-stu-id="9fe8e-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-484">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-484">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-485">Smölun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-485">Assembly</span></span></td>
<td><span data-ttu-id="9fe8e-486">55</span><span class="sxs-lookup"><span data-stu-id="9fe8e-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-487">CC004</span><span class="sxs-lookup"><span data-stu-id="9fe8e-487">CC004</span></span></td>
<td><span data-ttu-id="9fe8e-488">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9fe8e-488">Packaging</span></span></td>
<td><span data-ttu-id="9fe8e-489">10</span><span class="sxs-lookup"><span data-stu-id="9fe8e-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9fe8e-490">Kostnaðarhlutir CC002 Fjármál leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="9fe8e-491">Stofnað er tölfræðilegt víddarstak sem kallast Fjármálaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9fe8e-492">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-492">Cost object</span></span></th>
<th><span data-ttu-id="9fe8e-493">Fjármálaþjónusta</span><span class="sxs-lookup"><span data-stu-id="9fe8e-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-494">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-494">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-495">Smölun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-495">Assembly</span></span></td>
<td><span data-ttu-id="9fe8e-496">65</span><span class="sxs-lookup"><span data-stu-id="9fe8e-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-497">CC004</span><span class="sxs-lookup"><span data-stu-id="9fe8e-497">CC004</span></span></td>
<td><span data-ttu-id="9fe8e-498">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9fe8e-498">Packaging</span></span></td>
<td><span data-ttu-id="9fe8e-499">35</span><span class="sxs-lookup"><span data-stu-id="9fe8e-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9fe8e-500">Kostnaðarhlutir CC003 Samsetning leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="9fe8e-501">Meðlimur tölfræðilega víddar sem kallast Mannauður verk er stofnað til að mælvíddarstaka notuðum magnitude.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9fe8e-502">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-502">Cost object</span></span></th>
<th><span data-ttu-id="9fe8e-503">Samsetningarþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-504">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-504">Prod 1</span></span></td>
<td><span data-ttu-id="9fe8e-505">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-505">Product 1</span></span></td>
<td><span data-ttu-id="9fe8e-506">60</span><span class="sxs-lookup"><span data-stu-id="9fe8e-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-507">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-507">Prod 2</span></span></td>
<td><span data-ttu-id="9fe8e-508">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-508">Product 2</span></span></td>
<td><span data-ttu-id="9fe8e-509">20</span><span class="sxs-lookup"><span data-stu-id="9fe8e-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9fe8e-510">Kostnaðarhlutir CC004 Umbúðir leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="9fe8e-511">Stofnað er tölfræðilegt víddarstak sem kallast Umbúðaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9fe8e-512">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-512">Cost object</span></span></th>
<th><span data-ttu-id="9fe8e-513">Umbúðaþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-514">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-514">Prod 1</span></span></td>
<td><span data-ttu-id="9fe8e-515">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-515">Product 1</span></span></td>
<td><span data-ttu-id="9fe8e-516">80</span><span class="sxs-lookup"><span data-stu-id="9fe8e-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-517">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-517">Prod 2</span></span></td>
<td><span data-ttu-id="9fe8e-518">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-518">Product 2</span></span></td>
<td><span data-ttu-id="9fe8e-519">sept</span><span class="sxs-lookup"><span data-stu-id="9fe8e-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="9fe8e-520">Í Finance and Operations er hægt að afleiða tölfræðiaðgerðir eins og framleiðslutíma sem vara notar frá upprunagögnum.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-520">In Finance and Operations, statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="9fe8e-521">Nánari upplýsingar er að finna í [Veitusniðmát tölfræðiaðgerðar](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="9fe8e-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="9fe8e-522">Eftirfarandi tafla sýnir niðurstöður þegar mannauðsþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="9fe8e-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9fe8e-523">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-523">Cost object</span></span></th>
<th><span data-ttu-id="9fe8e-524">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="9fe8e-524">Magnitude</span></span></th>
<th><span data-ttu-id="9fe8e-525">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-525">Allocation factor</span></span></th>
<th><span data-ttu-id="9fe8e-526">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-526">Amount</span></span></th>
<th><span data-ttu-id="9fe8e-527">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-528">CC002</span><span class="sxs-lookup"><span data-stu-id="9fe8e-528">CC002</span></span></td>
<td><span data-ttu-id="9fe8e-529">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9fe8e-529">Finance</span></span></td>
<td><span data-ttu-id="9fe8e-530">35</span><span class="sxs-lookup"><span data-stu-id="9fe8e-530">35</span></span></td>
<td><span data-ttu-id="9fe8e-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="9fe8e-532">175.00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-532">175.00</span></span></td>
<td><span data-ttu-id="9fe8e-533">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-534">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-534">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-535">Smölun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-535">Assembly</span></span></td>
<td><span data-ttu-id="9fe8e-536">55</span><span class="sxs-lookup"><span data-stu-id="9fe8e-536">55</span></span></td>
<td><span data-ttu-id="9fe8e-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="9fe8e-538">275.00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-538">275.00</span></span></td>
<td><span data-ttu-id="9fe8e-539">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-540">CC004</span><span class="sxs-lookup"><span data-stu-id="9fe8e-540">CC004</span></span></td>
<td><span data-ttu-id="9fe8e-541">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9fe8e-541">Packaging</span></span></td>
<td><span data-ttu-id="9fe8e-542">10</span><span class="sxs-lookup"><span data-stu-id="9fe8e-542">10</span></span></td>
<td><span data-ttu-id="9fe8e-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="9fe8e-544">50,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-544">50.00</span></span></td>
<td><span data-ttu-id="9fe8e-545">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-546">CC002</span><span class="sxs-lookup"><span data-stu-id="9fe8e-546">CC002</span></span></td>
<td><span data-ttu-id="9fe8e-547">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9fe8e-547">Finance</span></span></td>
<td><span data-ttu-id="9fe8e-548">35</span><span class="sxs-lookup"><span data-stu-id="9fe8e-548">35</span></span></td>
<td><span data-ttu-id="9fe8e-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="9fe8e-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="9fe8e-550">436.00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-550">436.00</span></span></td>
<td><span data-ttu-id="9fe8e-551">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-552">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-552">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-553">Smölun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-553">Assembly</span></span></td>
<td><span data-ttu-id="9fe8e-554">55</span><span class="sxs-lookup"><span data-stu-id="9fe8e-554">55</span></span></td>
<td><span data-ttu-id="9fe8e-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="9fe8e-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="9fe8e-556">685.14</span><span class="sxs-lookup"><span data-stu-id="9fe8e-556">685.14</span></span></td>
<td><span data-ttu-id="9fe8e-557">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-558">CC004</span><span class="sxs-lookup"><span data-stu-id="9fe8e-558">CC004</span></span></td>
<td><span data-ttu-id="9fe8e-559">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9fe8e-559">Packaging</span></span></td>
<td><span data-ttu-id="9fe8e-560">10</span><span class="sxs-lookup"><span data-stu-id="9fe8e-560">10</span></span></td>
<td><span data-ttu-id="9fe8e-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="9fe8e-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="9fe8e-562">124.57</span><span class="sxs-lookup"><span data-stu-id="9fe8e-562">124.57</span></span></td>
<td><span data-ttu-id="9fe8e-563">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9fe8e-564">Eftirfarandi tafla sýnir niðurstöður þegar Fjármálaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="9fe8e-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9fe8e-565">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-565">Cost object</span></span></th>
<th><span data-ttu-id="9fe8e-566">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="9fe8e-566">Magnitude</span></span></th>
<th><span data-ttu-id="9fe8e-567">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-567">Allocation factor</span></span></th>
<th><span data-ttu-id="9fe8e-568">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-568">Amount</span></span></th>
<th><span data-ttu-id="9fe8e-569">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-570">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-570">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-571">Smölun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-571">Assembly</span></span></td>
<td><span data-ttu-id="9fe8e-572">65</span><span class="sxs-lookup"><span data-stu-id="9fe8e-572">65</span></span></td>
<td><span data-ttu-id="9fe8e-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="9fe8e-574">438.75</span><span class="sxs-lookup"><span data-stu-id="9fe8e-574">438.75</span></span></td>
<td><span data-ttu-id="9fe8e-575">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-576">CC004</span><span class="sxs-lookup"><span data-stu-id="9fe8e-576">CC004</span></span></td>
<td><span data-ttu-id="9fe8e-577">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9fe8e-577">Packaging</span></span></td>
<td><span data-ttu-id="9fe8e-578">35</span><span class="sxs-lookup"><span data-stu-id="9fe8e-578">35</span></span></td>
<td><span data-ttu-id="9fe8e-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="9fe8e-580">236.25</span><span class="sxs-lookup"><span data-stu-id="9fe8e-580">236.25</span></span></td>
<td><span data-ttu-id="9fe8e-581">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-582">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-582">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-583">Smölun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-583">Assembly</span></span></td>
<td><span data-ttu-id="9fe8e-584">65</span><span class="sxs-lookup"><span data-stu-id="9fe8e-584">65</span></span></td>
<td><span data-ttu-id="9fe8e-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="9fe8e-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="9fe8e-586">5,297.69</span></span></td>
<td><span data-ttu-id="9fe8e-587">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-588">CC004</span><span class="sxs-lookup"><span data-stu-id="9fe8e-588">CC004</span></span></td>
<td><span data-ttu-id="9fe8e-589">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9fe8e-589">Packaging</span></span></td>
<td><span data-ttu-id="9fe8e-590">35</span><span class="sxs-lookup"><span data-stu-id="9fe8e-590">35</span></span></td>
<td><span data-ttu-id="9fe8e-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="9fe8e-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="9fe8e-592">2,852.60</span></span></td>
<td><span data-ttu-id="9fe8e-593">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9fe8e-594">Eftirfarandi tafla sýnir niðurstöður þegar Samsetningarþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="9fe8e-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9fe8e-595">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-595">Cost object</span></span></th>
<th><span data-ttu-id="9fe8e-596">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="9fe8e-596">Magnitude</span></span></th>
<th><span data-ttu-id="9fe8e-597">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-597">Allocation factor</span></span></th>
<th><span data-ttu-id="9fe8e-598">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-598">Amount</span></span></th>
<th><span data-ttu-id="9fe8e-599">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-600">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-600">Prod 1</span></span></td>
<td><span data-ttu-id="9fe8e-601">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-601">Product 1</span></span></td>
<td><span data-ttu-id="9fe8e-602">60</span><span class="sxs-lookup"><span data-stu-id="9fe8e-602">60</span></span></td>
<td><span data-ttu-id="9fe8e-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="9fe8e-604">535.31</span><span class="sxs-lookup"><span data-stu-id="9fe8e-604">535.31</span></span></td>
<td><span data-ttu-id="9fe8e-605">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-606">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-606">Prod 2</span></span></td>
<td><span data-ttu-id="9fe8e-607">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-607">Product 2</span></span></td>
<td><span data-ttu-id="9fe8e-608">20</span><span class="sxs-lookup"><span data-stu-id="9fe8e-608">20</span></span></td>
<td><span data-ttu-id="9fe8e-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="9fe8e-610">178.44</span><span class="sxs-lookup"><span data-stu-id="9fe8e-610">178.44</span></span></td>
<td><span data-ttu-id="9fe8e-611">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-612">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-612">Prod 1</span></span></td>
<td><span data-ttu-id="9fe8e-613">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-613">Product 1</span></span></td>
<td><span data-ttu-id="9fe8e-614">60</span><span class="sxs-lookup"><span data-stu-id="9fe8e-614">60</span></span></td>
<td><span data-ttu-id="9fe8e-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="9fe8e-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="9fe8e-616">4,487.12</span></span></td>
<td><span data-ttu-id="9fe8e-617">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-618">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-618">Prod 2</span></span></td>
<td><span data-ttu-id="9fe8e-619">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-619">Product 2</span></span></td>
<td><span data-ttu-id="9fe8e-620">20</span><span class="sxs-lookup"><span data-stu-id="9fe8e-620">20</span></span></td>
<td><span data-ttu-id="9fe8e-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="9fe8e-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="9fe8e-622">1,495.71</span></span></td>
<td><span data-ttu-id="9fe8e-623">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="9fe8e-624">Eftirfarandi tafla sýnir niðurstöður þegar Umbúðaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="9fe8e-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9fe8e-625">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-625">Cost object</span></span></th>
<th><span data-ttu-id="9fe8e-626">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="9fe8e-626">Magnitude</span></span></th>
<th><span data-ttu-id="9fe8e-627">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-627">Allocation factor</span></span></th>
<th><span data-ttu-id="9fe8e-628">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-628">Amount</span></span></th>
<th><span data-ttu-id="9fe8e-629">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-630">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-630">Prod 1</span></span></td>
<td><span data-ttu-id="9fe8e-631">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-631">Product 1</span></span></td>
<td><span data-ttu-id="9fe8e-632">80</span><span class="sxs-lookup"><span data-stu-id="9fe8e-632">80</span></span></td>
<td><span data-ttu-id="9fe8e-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="9fe8e-634">241.05</span><span class="sxs-lookup"><span data-stu-id="9fe8e-634">241.05</span></span></td>
<td><span data-ttu-id="9fe8e-635">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-636">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-636">Prod 2</span></span></td>
<td><span data-ttu-id="9fe8e-637">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-637">Product 2</span></span></td>
<td><span data-ttu-id="9fe8e-638">15</span><span class="sxs-lookup"><span data-stu-id="9fe8e-638">15</span></span></td>
<td><span data-ttu-id="9fe8e-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="9fe8e-640">45.20</span><span class="sxs-lookup"><span data-stu-id="9fe8e-640">45.20</span></span></td>
<td><span data-ttu-id="9fe8e-641">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-642">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-642">Prod 1</span></span></td>
<td><span data-ttu-id="9fe8e-643">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-643">Product 1</span></span></td>
<td><span data-ttu-id="9fe8e-644">80</span><span class="sxs-lookup"><span data-stu-id="9fe8e-644">80</span></span></td>
<td><span data-ttu-id="9fe8e-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="9fe8e-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="9fe8e-646">2,507.09</span></span></td>
<td><span data-ttu-id="9fe8e-647">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-648">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-648">Prod 2</span></span></td>
<td><span data-ttu-id="9fe8e-649">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-649">Product 2</span></span></td>
<td><span data-ttu-id="9fe8e-650">15</span><span class="sxs-lookup"><span data-stu-id="9fe8e-650">15</span></span></td>
<td><span data-ttu-id="9fe8e-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="9fe8e-652">470.08</span><span class="sxs-lookup"><span data-stu-id="9fe8e-652">470.08</span></span></td>
<td><span data-ttu-id="9fe8e-653">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="9fe8e-654">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="9fe8e-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9fe8e-655">Færslubók</span><span class="sxs-lookup"><span data-stu-id="9fe8e-655">Journal</span></span></th>
<th><span data-ttu-id="9fe8e-656">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="9fe8e-657">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="9fe8e-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="9fe8e-658">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="9fe8e-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-659">00004</span><span class="sxs-lookup"><span data-stu-id="9fe8e-659">00004</span></span></td>
<td><span data-ttu-id="9fe8e-660">Færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="9fe8e-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="9fe8e-661">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-661">Fiscal</span></span></td>
<td><span data-ttu-id="9fe8e-662">2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-662">2017</span></span></td>
<td><span data-ttu-id="9fe8e-663">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="9fe8e-663">Period 1</span></span></td>
<td><span data-ttu-id="9fe8e-664">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="9fe8e-665">Færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9fe8e-666">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="9fe8e-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="9fe8e-667">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9fe8e-668">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9fe8e-668">Cost element</span></span></th>
<th><span data-ttu-id="9fe8e-669">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-669">Cost behavior</span></span></th>
<th><span data-ttu-id="9fe8e-670">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-671">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="9fe8e-672">CC001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-672">CC001</span></span></td>
<td><span data-ttu-id="9fe8e-673">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-673">HR</span></span></td>
<td><span data-ttu-id="9fe8e-674">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-674">10001</span></span></td>
<td><span data-ttu-id="9fe8e-675">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-675">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-676">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-676">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-677">500,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-678">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="9fe8e-679">CC001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-679">CC001</span></span></td>
<td><span data-ttu-id="9fe8e-680">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-680">HR</span></span></td>
<td><span data-ttu-id="9fe8e-681">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-681">10001</span></span></td>
<td><span data-ttu-id="9fe8e-682">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-682">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-683">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-683">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="9fe8e-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-685">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="9fe8e-686">CC002</span><span class="sxs-lookup"><span data-stu-id="9fe8e-686">CC002</span></span></td>
<td><span data-ttu-id="9fe8e-687">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9fe8e-687">Finance</span></span></td>
<td><span data-ttu-id="9fe8e-688">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-688">10001</span></span></td>
<td><span data-ttu-id="9fe8e-689">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-689">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-690">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-690">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-691">675.00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-692">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="9fe8e-693">CC002</span><span class="sxs-lookup"><span data-stu-id="9fe8e-693">CC002</span></span></td>
<td><span data-ttu-id="9fe8e-694">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9fe8e-694">Finance</span></span></td>
<td><span data-ttu-id="9fe8e-695">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-695">10001</span></span></td>
<td><span data-ttu-id="9fe8e-696">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-696">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-697">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-697">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="9fe8e-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-699">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="9fe8e-700">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-700">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-701">Smölun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-701">Assembly</span></span></td>
<td><span data-ttu-id="9fe8e-702">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-702">10001</span></span></td>
<td><span data-ttu-id="9fe8e-703">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-703">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-704">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-704">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-705">713.75</span><span class="sxs-lookup"><span data-stu-id="9fe8e-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-706">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="9fe8e-707">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-707">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-708">Smölun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-708">Assembly</span></span></td>
<td><span data-ttu-id="9fe8e-709">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-709">10001</span></span></td>
<td><span data-ttu-id="9fe8e-710">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-710">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-711">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-711">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="9fe8e-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-713">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="9fe8e-714">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-714">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-715">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9fe8e-715">Packaging</span></span></td>
<td><span data-ttu-id="9fe8e-716">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-716">10001</span></span></td>
<td><span data-ttu-id="9fe8e-717">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-717">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-718">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-718">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-719">286.25</span><span class="sxs-lookup"><span data-stu-id="9fe8e-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-720">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="9fe8e-721">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-721">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-722">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9fe8e-722">Packaging</span></span></td>
<td><span data-ttu-id="9fe8e-723">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-723">10001</span></span></td>
<td><span data-ttu-id="9fe8e-724">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-724">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-725">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-725">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="9fe8e-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-727">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="9fe8e-728">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-728">Prod 1</span></span></td>
<td><span data-ttu-id="9fe8e-729">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-729">Product 1</span></span></td>
<td><span data-ttu-id="9fe8e-730">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-730">10001</span></span></td>
<td><span data-ttu-id="9fe8e-731">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-731">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-732">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-732">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-733">776.36</span><span class="sxs-lookup"><span data-stu-id="9fe8e-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-734">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="9fe8e-735">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-735">Prod 1</span></span></td>
<td><span data-ttu-id="9fe8e-736">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-736">Product 1</span></span></td>
<td><span data-ttu-id="9fe8e-737">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-737">10001</span></span></td>
<td><span data-ttu-id="9fe8e-738">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-738">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-739">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-739">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="9fe8e-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-741">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="9fe8e-742">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-742">Prod 2</span></span></td>
<td><span data-ttu-id="9fe8e-743">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-743">Product 1</span></span></td>
<td><span data-ttu-id="9fe8e-744">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-744">10001</span></span></td>
<td><span data-ttu-id="9fe8e-745">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-745">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-746">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-746">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-747">223.64</span><span class="sxs-lookup"><span data-stu-id="9fe8e-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-748">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="9fe8e-749">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-749">Prod 2</span></span></td>
<td><span data-ttu-id="9fe8e-750">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-750">Product 1</span></span></td>
<td><span data-ttu-id="9fe8e-751">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-751">10001</span></span></td>
<td><span data-ttu-id="9fe8e-752">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-752">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-753">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-753">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="9fe8e-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="9fe8e-755">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="9fe8e-756">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="9fe8e-757">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9fe8e-757">Cost element</span></span></th>
<th><span data-ttu-id="9fe8e-758">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-758">Cost behavior</span></span></th>
<th><span data-ttu-id="9fe8e-759">Upphæð</span><span class="sxs-lookup"><span data-stu-id="9fe8e-759">Amount</span></span></th>
<th><span data-ttu-id="9fe8e-760">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="9fe8e-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9fe8e-761">CC001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-761">CC001</span></span></td>
<td><span data-ttu-id="9fe8e-762">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-762">HR</span></span></td>
<td><span data-ttu-id="9fe8e-763">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-763">10001</span></span></td>
<td><span data-ttu-id="9fe8e-764">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-764">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-765">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-765">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-766">-500.00</span></span></td>
<td><span data-ttu-id="9fe8e-767">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-768">CC002</span><span class="sxs-lookup"><span data-stu-id="9fe8e-768">CC002</span></span></td>
<td><span data-ttu-id="9fe8e-769">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9fe8e-769">Finance</span></span></td>
<td><span data-ttu-id="9fe8e-770">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-770">10001</span></span></td>
<td><span data-ttu-id="9fe8e-771">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-771">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-772">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-772">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-773">175.00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-773">175.00</span></span></td>
<td><span data-ttu-id="9fe8e-774">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-775">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-775">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-776">Smölun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-776">Assembly</span></span></td>
<td><span data-ttu-id="9fe8e-777">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-777">10001</span></span></td>
<td><span data-ttu-id="9fe8e-778">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-778">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-779">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-779">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-780">275.00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-780">275.00</span></span></td>
<td><span data-ttu-id="9fe8e-781">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-782">CC004</span><span class="sxs-lookup"><span data-stu-id="9fe8e-782">CC004</span></span></td>
<td><span data-ttu-id="9fe8e-783">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9fe8e-783">Packaging</span></span></td>
<td><span data-ttu-id="9fe8e-784">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-784">10001</span></span></td>
<td><span data-ttu-id="9fe8e-785">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-785">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-786">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-786">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-787">50,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-787">50,00</span></span></td>
<td><span data-ttu-id="9fe8e-788">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-789">CC001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-789">CC001</span></span></td>
<td><span data-ttu-id="9fe8e-790">Mannauður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-790">HR</span></span></td>
<td><span data-ttu-id="9fe8e-791">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-791">10001</span></span></td>
<td><span data-ttu-id="9fe8e-792">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-792">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-793">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-793">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="9fe8e-794">-1,245.71</span></span></td>
<td><span data-ttu-id="9fe8e-795">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-796">CC002</span><span class="sxs-lookup"><span data-stu-id="9fe8e-796">CC002</span></span></td>
<td><span data-ttu-id="9fe8e-797">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9fe8e-797">Finance</span></span></td>
<td><span data-ttu-id="9fe8e-798">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-798">10001</span></span></td>
<td><span data-ttu-id="9fe8e-799">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-799">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-800">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-800">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-801">436.00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-801">436.00</span></span></td>
<td><span data-ttu-id="9fe8e-802">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-803">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-803">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-804">Smölun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-804">Assembly</span></span></td>
<td><span data-ttu-id="9fe8e-805">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-805">10001</span></span></td>
<td><span data-ttu-id="9fe8e-806">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-806">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-807">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-807">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-808">685.14</span><span class="sxs-lookup"><span data-stu-id="9fe8e-808">685.14</span></span></td>
<td><span data-ttu-id="9fe8e-809">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-810">CC004</span><span class="sxs-lookup"><span data-stu-id="9fe8e-810">CC004</span></span></td>
<td><span data-ttu-id="9fe8e-811">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9fe8e-811">Packaging</span></span></td>
<td><span data-ttu-id="9fe8e-812">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-812">10001</span></span></td>
<td><span data-ttu-id="9fe8e-813">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-813">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-814">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-814">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-815">124.57</span><span class="sxs-lookup"><span data-stu-id="9fe8e-815">124.57</span></span></td>
<td><span data-ttu-id="9fe8e-816">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-817">CC002</span><span class="sxs-lookup"><span data-stu-id="9fe8e-817">CC002</span></span></td>
<td><span data-ttu-id="9fe8e-818">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9fe8e-818">Finance</span></span></td>
<td><span data-ttu-id="9fe8e-819">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-819">10001</span></span></td>
<td><span data-ttu-id="9fe8e-820">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-820">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-821">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-821">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-822">-675.00</span></span></td>
<td><span data-ttu-id="9fe8e-823">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-824">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-824">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-825">Smölun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-825">Assembly</span></span></td>
<td><span data-ttu-id="9fe8e-826">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-826">10001</span></span></td>
<td><span data-ttu-id="9fe8e-827">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-827">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-828">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-828">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-829">438.75</span><span class="sxs-lookup"><span data-stu-id="9fe8e-829">438.75</span></span></td>
<td><span data-ttu-id="9fe8e-830">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-831">CC004</span><span class="sxs-lookup"><span data-stu-id="9fe8e-831">CC004</span></span></td>
<td><span data-ttu-id="9fe8e-832">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9fe8e-832">Packaging</span></span></td>
<td><span data-ttu-id="9fe8e-833">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-833">10001</span></span></td>
<td><span data-ttu-id="9fe8e-834">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-834">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-835">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-835">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-836">236.25</span><span class="sxs-lookup"><span data-stu-id="9fe8e-836">236.25</span></span></td>
<td><span data-ttu-id="9fe8e-837">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-838">CC002</span><span class="sxs-lookup"><span data-stu-id="9fe8e-838">CC002</span></span></td>
<td><span data-ttu-id="9fe8e-839">Fjármál</span><span class="sxs-lookup"><span data-stu-id="9fe8e-839">Finance</span></span></td>
<td><span data-ttu-id="9fe8e-840">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-840">10001</span></span></td>
<td><span data-ttu-id="9fe8e-841">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-841">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-842">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-842">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="9fe8e-843">-8,150.29</span></span></td>
<td><span data-ttu-id="9fe8e-844">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-845">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-845">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-846">Smölun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-846">Assembly</span></span></td>
<td><span data-ttu-id="9fe8e-847">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-847">10001</span></span></td>
<td><span data-ttu-id="9fe8e-848">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-848">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-849">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-849">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="9fe8e-850">5,297.69</span></span></td>
<td><span data-ttu-id="9fe8e-851">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-852">CC004</span><span class="sxs-lookup"><span data-stu-id="9fe8e-852">CC004</span></span></td>
<td><span data-ttu-id="9fe8e-853">Pakkning</span><span class="sxs-lookup"><span data-stu-id="9fe8e-853">Packaging</span></span></td>
<td><span data-ttu-id="9fe8e-854">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-854">10001</span></span></td>
<td><span data-ttu-id="9fe8e-855">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-855">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-856">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-856">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="9fe8e-857">2,852.60</span></span></td>
<td><span data-ttu-id="9fe8e-858">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-859">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-859">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-860">Smölun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-860">Assembly</span></span></td>
<td><span data-ttu-id="9fe8e-861">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-861">10001</span></span></td>
<td><span data-ttu-id="9fe8e-862">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-862">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-863">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-863">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="9fe8e-864">-713.75</span></span></td>
<td><span data-ttu-id="9fe8e-865">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-866">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-866">Prod 1</span></span></td>
<td><span data-ttu-id="9fe8e-867">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-867">Product 1</span></span></td>
<td><span data-ttu-id="9fe8e-868">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-868">10001</span></span></td>
<td><span data-ttu-id="9fe8e-869">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-869">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-870">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-870">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-871">535.31</span><span class="sxs-lookup"><span data-stu-id="9fe8e-871">535.31</span></span></td>
<td><span data-ttu-id="9fe8e-872">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-873">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-873">Prod 2</span></span></td>
<td><span data-ttu-id="9fe8e-874">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-874">Product 2</span></span></td>
<td><span data-ttu-id="9fe8e-875">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-875">10001</span></span></td>
<td><span data-ttu-id="9fe8e-876">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-876">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-877">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-877">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-878">178.44</span><span class="sxs-lookup"><span data-stu-id="9fe8e-878">178.44</span></span></td>
<td><span data-ttu-id="9fe8e-879">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-880">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-880">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-881">Smölun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-881">Assembly</span></span></td>
<td><span data-ttu-id="9fe8e-882">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-882">10001</span></span></td>
<td><span data-ttu-id="9fe8e-883">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-883">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-884">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-884">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="9fe8e-885">-5,982.83</span></span></td>
<td><span data-ttu-id="9fe8e-886">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-887">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-887">Prod 1</span></span></td>
<td><span data-ttu-id="9fe8e-888">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-888">Product 1</span></span></td>
<td><span data-ttu-id="9fe8e-889">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-889">10001</span></span></td>
<td><span data-ttu-id="9fe8e-890">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-890">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-891">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-891">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="9fe8e-892">4,487.12</span></span></td>
<td><span data-ttu-id="9fe8e-893">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-894">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-894">Prod 2</span></span></td>
<td><span data-ttu-id="9fe8e-895">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-895">Product 2</span></span></td>
<td><span data-ttu-id="9fe8e-896">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-896">10001</span></span></td>
<td><span data-ttu-id="9fe8e-897">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-897">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-898">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-898">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="9fe8e-899">1,495.71</span></span></td>
<td><span data-ttu-id="9fe8e-900">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-901">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-901">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-902">Smölun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-902">Assembly</span></span></td>
<td><span data-ttu-id="9fe8e-903">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-903">10001</span></span></td>
<td><span data-ttu-id="9fe8e-904">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-904">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-905">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-905">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="9fe8e-906">-286.25</span></span></td>
<td><span data-ttu-id="9fe8e-907">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-908">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-908">Prod 1</span></span></td>
<td><span data-ttu-id="9fe8e-909">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-909">Product 1</span></span></td>
<td><span data-ttu-id="9fe8e-910">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-910">10001</span></span></td>
<td><span data-ttu-id="9fe8e-911">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-911">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-912">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-912">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-913">241.05</span><span class="sxs-lookup"><span data-stu-id="9fe8e-913">241.05</span></span></td>
<td><span data-ttu-id="9fe8e-914">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-915">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-915">Prod 2</span></span></td>
<td><span data-ttu-id="9fe8e-916">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-916">Product 2</span></span></td>
<td><span data-ttu-id="9fe8e-917">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-917">10001</span></span></td>
<td><span data-ttu-id="9fe8e-918">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-918">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-919">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-919">Fixed cost</span></span></td>
<td><span data-ttu-id="9fe8e-920">45.20</span><span class="sxs-lookup"><span data-stu-id="9fe8e-920">45.20</span></span></td>
<td><span data-ttu-id="9fe8e-921">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-922">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-922">CC003</span></span></td>
<td><span data-ttu-id="9fe8e-923">Smölun</span><span class="sxs-lookup"><span data-stu-id="9fe8e-923">Assembly</span></span></td>
<td><span data-ttu-id="9fe8e-924">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-924">10001</span></span></td>
<td><span data-ttu-id="9fe8e-925">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-925">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-926">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-926">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="9fe8e-927">-2,977.17</span></span></td>
<td><span data-ttu-id="9fe8e-928">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-929">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-929">Prod 1</span></span></td>
<td><span data-ttu-id="9fe8e-930">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-930">Product 1</span></span></td>
<td><span data-ttu-id="9fe8e-931">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-931">10001</span></span></td>
<td><span data-ttu-id="9fe8e-932">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-932">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-933">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-933">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="9fe8e-934">2,507.09</span></span></td>
<td><span data-ttu-id="9fe8e-935">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="9fe8e-936">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-936">Prod 2</span></span></td>
<td><span data-ttu-id="9fe8e-937">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-937">Product 2</span></span></td>
<td><span data-ttu-id="9fe8e-938">10001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-938">10001</span></span></td>
<td><span data-ttu-id="9fe8e-939">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-939">Electricity</span></span></td>
<td><span data-ttu-id="9fe8e-940">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-940">Variable cost</span></span></td>
<td><span data-ttu-id="9fe8e-941">470.08</span><span class="sxs-lookup"><span data-stu-id="9fe8e-941">470.08</span></span></td>
<td><span data-ttu-id="9fe8e-942">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="9fe8e-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="9fe8e-943">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="9fe8e-943">Conclusion</span></span>
<span data-ttu-id="9fe8e-944">Í Fjárhagsbókhaldi er kostnaður upp á 10.000,00 fyrir rafmagn bókaður á kenni leppkostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="9fe8e-945">Þar af leiðandi munu kostnaðarbókarar vita að það þarf að úthluta þessum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="9fe8e-946">Í kostnaðarbókhaldi streymir kostnaður þvert á fyrirtækiseiningar og stig, samkvæmt þeim stefnum og reglum sem eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="9fe8e-947">Hver kostnaður hefur verið tengdur úthlutunargrunni sem veitir besta mat á úthlutun á kostnaði.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="9fe8e-948">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="9fe8e-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="9fe8e-949">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="9fe8e-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="9fe8e-950">Samtala</span><span class="sxs-lookup"><span data-stu-id="9fe8e-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="9fe8e-951">CC099</span><span class="sxs-lookup"><span data-stu-id="9fe8e-951">CC099</span></span></th>
<th><span data-ttu-id="9fe8e-952">CC001</span><span class="sxs-lookup"><span data-stu-id="9fe8e-952">CC001</span></span></th>
<th><span data-ttu-id="9fe8e-953">CC002</span><span class="sxs-lookup"><span data-stu-id="9fe8e-953">CC002</span></span></th>
<th><span data-ttu-id="9fe8e-954">CC003</span><span class="sxs-lookup"><span data-stu-id="9fe8e-954">CC003</span></span></th>
<th><span data-ttu-id="9fe8e-955">CC004</span><span class="sxs-lookup"><span data-stu-id="9fe8e-955">CC004</span></span></th>
<th><span data-ttu-id="9fe8e-956">Verk 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-956">Proj 1</span></span></th>
<th><span data-ttu-id="9fe8e-957">Verk 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-957">Proj 2</span></span></th>
<th><span data-ttu-id="9fe8e-958">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="9fe8e-958">Prod 1</span></span></th>
<th><span data-ttu-id="9fe8e-959">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="9fe8e-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="9fe8e-960">10001 Rafmagn</span><span class="sxs-lookup"><span data-stu-id="9fe8e-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="9fe8e-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="9fe8e-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="9fe8e-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="9fe8e-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="9fe8e-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="9fe8e-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="9fe8e-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="9fe8e-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="9fe8e-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="9fe8e-970">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="9fe8e-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-971">0,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="9fe8e-972">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-973">0,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-974">0,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-975">0,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-976">0,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-977">0,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-978">776.36</span><span class="sxs-lookup"><span data-stu-id="9fe8e-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-979">223.64</span><span class="sxs-lookup"><span data-stu-id="9fe8e-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="9fe8e-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="9fe8e-981">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="9fe8e-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-982">000</span><span class="sxs-lookup"><span data-stu-id="9fe8e-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-983">0,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-984">0,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-985">0,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-986">0,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-987">30,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-988">10,00</span><span class="sxs-lookup"><span data-stu-id="9fe8e-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="9fe8e-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="9fe8e-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="9fe8e-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="9fe8e-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="9fe8e-992">Þetta efnisatriði sýnir hvernig fyrir aðalkostnaðareiningin 10001 Rafmagn flæðir í gegnum kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="9fe8e-993">Þar af leiðandi er þessum sameiginlega kostnaði úthlutað á lægsta stigið í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="9fe8e-994">Með öðrum orðum bera kostnaðarhlutir á lægsta stiginu kostnaðinn.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="9fe8e-995">Ef þú þarft sjónrænt flæði kostnaðar á milli kostnaðarhluta er hægt að nota stefnureglur samantekins kostnaðar til að gera kostnaðarflæðið sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="9fe8e-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="9fe8e-996">Nánari upplýsingar er að finna í [Samantekt kostnaðar](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="9fe8e-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



