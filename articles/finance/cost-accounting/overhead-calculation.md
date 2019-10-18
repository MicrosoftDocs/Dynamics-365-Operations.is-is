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
ms.openlocfilehash: 6c045f82f3288dba193721dd80c90e68750af9a7
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178297"
---
# <a name="overhead-calculation"></a><span data-ttu-id="b7752-103">Útreikningur fastakostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-103">Overhead calculation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7752-104">Þetta efnisatriði lýsir dæmigerðum ferlum til að reikna út og úthluta rekstrarkostnaði.</span><span class="sxs-lookup"><span data-stu-id="b7752-104">This topic describes the typical processes for calculating and allocating overhead costs.</span></span>

<a name="term-definition"></a><span data-ttu-id="b7752-105">Skýrsluskilgreining</span><span class="sxs-lookup"><span data-stu-id="b7752-105">Term definition</span></span>
---------------

<span data-ttu-id="b7752-106">Stjórnunarkostnaður er sá kostnaður sem stofnað er til fyrir rekstur fyrirtækis, en sem ekki er hægt að rekja beint til neinna sérstakrar starfsemi, vöru eða þjónustu.</span><span class="sxs-lookup"><span data-stu-id="b7752-106">Overhead costs are the costs that are incurred in order to run a business, but that can't be directly attributed to any specific business activity, product, or service.</span></span> <span data-ttu-id="b7752-107">Stjórnunarkostnaður veitir mikilvægan stuðning við myndun hagnaðarmyndandi verkþátta.</span><span class="sxs-lookup"><span data-stu-id="b7752-107">Overhead costs provide critical support for the generation of profit-making activities.</span></span> <span data-ttu-id="b7752-108">Hér eru nokkur dæmi um skilyrði:</span><span class="sxs-lookup"><span data-stu-id="b7752-108">Here are some examples of overhead costs:</span></span>

-   <span data-ttu-id="b7752-109">Leiga</span><span class="sxs-lookup"><span data-stu-id="b7752-109">Rent</span></span>
-   <span data-ttu-id="b7752-110">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-110">Electricity</span></span>
-   <span data-ttu-id="b7752-111">Stjórnunarkostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-111">Administrative salaries</span></span>

## <a name="overhead-calculation-overview"></a><span data-ttu-id="b7752-112">Yfirlit yfir útreikning fastakostnaðar</span><span class="sxs-lookup"><span data-stu-id="b7752-112">Overhead calculation overview</span></span>
<span data-ttu-id="b7752-113">Útreikningur fastakostnaðar keyrir reglur kostnaðarbókhalds í réttri röð.</span><span class="sxs-lookup"><span data-stu-id="b7752-113">Overhead calculation runs the cost accounting policies in the correct order.</span></span> <span data-ttu-id="b7752-114">Hægt er að keyra útreikning fastakostnaðar margsinnis fyrir sama fjárhagstímabil ef reglum kostnaðarbókhalds hefur verið breytt eða ákveðnar villur hafa fundist.</span><span class="sxs-lookup"><span data-stu-id="b7752-114">You can run overhead calculation multiple times for the same fiscal period if cost accounting policies have been changed or specific errors have been detected.</span></span> <span data-ttu-id="b7752-115">Hver keyrsla á útreikningi fastakostnaðar er geymd og fær einkvæmt útgáfukenni sem gerir kleift að bera saman útreikning í mismunandi útgáfum.</span><span class="sxs-lookup"><span data-stu-id="b7752-115">Each run of the overhead calculation is stored and receives a unique version ID that lets you compare the calculations in various versions.</span></span> <span data-ttu-id="b7752-116">Kostnaðarfærslur sem útreikningur fastakostnaðar mynda fá dagsetningu reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="b7752-116">The cost entries that the overhead calculation generates receive an accounting date.</span></span> <span data-ttu-id="b7752-117">Dagsetningin bókhald samsvarar lokadagsetning fjárhagstímabilsins sem er dagsetning reikningsskiladagsetning reikningsskila notað í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="b7752-117">This accounting date matches the end date of the fiscal period that is used in the calculation.</span></span> <span data-ttu-id="b7752-118">Einkvæmt útgáfukenni samanstendur af eftirfarandi þáttum:</span><span class="sxs-lookup"><span data-stu-id="b7752-118">The unique version ID consists of the following elements:</span></span>

-   <span data-ttu-id="b7752-119">Gerð útgáfu</span><span class="sxs-lookup"><span data-stu-id="b7752-119">Version type</span></span>
-   <span data-ttu-id="b7752-120">Dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="b7752-120">Date and time</span></span>
-   <span data-ttu-id="b7752-121">Fjárhagur kostnaðarbókhalds</span><span class="sxs-lookup"><span data-stu-id="b7752-121">Cost accounting ledger</span></span>
-   <span data-ttu-id="b7752-122">Fjárhagsár</span><span class="sxs-lookup"><span data-stu-id="b7752-122">Fiscal year</span></span>
-   <span data-ttu-id="b7752-123">Reikningstímabil</span><span class="sxs-lookup"><span data-stu-id="b7752-123">Fiscal period</span></span>

<span data-ttu-id="b7752-124">Útreikningur fastakostnaðar er keyrður óháð því hver útgáfan er.</span><span class="sxs-lookup"><span data-stu-id="b7752-124">Overhead calculation is run independently of the version.</span></span> <span data-ttu-id="b7752-125">Þess vegna er hægt að reikna út áætlaða útgáfu á undan raunútgáfu.</span><span class="sxs-lookup"><span data-stu-id="b7752-125">Therefore, you can calculate the Budget version before the Actual version.</span></span> <span data-ttu-id="b7752-126">Útreikningur fastakostnaðar samanstendur af fjórum skrefum, eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="b7752-126">Overhead calculation consists of four steps, as shown in the following illustration.</span></span> <span data-ttu-id="b7752-127">Í hverju skrefi er færslubókarhaus stofnaður með bókarfærslum.</span><span class="sxs-lookup"><span data-stu-id="b7752-127">In each step, a journal header is created that has journal entries.</span></span> <span data-ttu-id="b7752-128">Þessi færslubókarhaus geymir inntaksgögn fyrir hvert útreikningsþrep.</span><span class="sxs-lookup"><span data-stu-id="b7752-128">This journal header keeps the input data for each calculation step.</span></span> <span data-ttu-id="b7752-129">Stefnur og reglur eru notaðar í hverri færslulínu og kostnaðarfærslur eru myndaðar sem úttak.</span><span class="sxs-lookup"><span data-stu-id="b7752-129">Policies and rules are applied to each journal line, and cost entries are generated as output.</span></span> <span data-ttu-id="b7752-130">Þess vegna hefurðu ávallt fullan rekjanleika.</span><span class="sxs-lookup"><span data-stu-id="b7752-130">Therefore, you always have full traceability.</span></span> 

<span data-ttu-id="b7752-131">[![Útreikningur fastakostnaðar](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span><span class="sxs-lookup"><span data-stu-id="b7752-131">[![Overhead calculation](./media/period-cost-calculation.png)](./media/period-cost-calculation.png)</span></span>

## <a name="calculate-and-allocate-the-electricity-overhead-cost"></a><span data-ttu-id="b7752-132">Reikna og úthluta sameiginlegur kostnaði vegna rafmagns</span><span class="sxs-lookup"><span data-stu-id="b7752-132">Calculate and allocate the Electricity overhead cost</span></span>
<span data-ttu-id="b7752-133">Í Fjárhagsbókhaldi er ákveðinn kostnaður, eins og rafmagn, skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="b7752-133">In Financial accounting, some costs, such as electricity, are registered as a lump sum.</span></span> <span data-ttu-id="b7752-134">Þar af leiðandi er nákvæmar innsýn rekstrarfélags ekki veitt fyrir kostnaðarbókhald.</span><span class="sxs-lookup"><span data-stu-id="b7752-134">Therefore, detailed managerial insight isn't provided for Cost accounting.</span></span> <span data-ttu-id="b7752-135">Í kostnaðarbókhaldi verður kostnaður að flæða í gegnum fyrirtækiseiningar til að veita rétta innsýn rekstrarfélags þvert á allar fyrirtækiseiningar og stig.</span><span class="sxs-lookup"><span data-stu-id="b7752-135">In Cost accounting, to provide correct managerial insight across all organizational units and levels, costs must flow through the organizational units.</span></span> <span data-ttu-id="b7752-136">Þetta flæði verður að byggja á annaðhvort nákvæmri færslu notkunar eða sanngjarnri matsreglu.</span><span class="sxs-lookup"><span data-stu-id="b7752-136">This flow must be based on either an accurate record of the consumption or a fair assessment.</span></span> <span data-ttu-id="b7752-137">Í fjárhagnum er hægt að bóka rafmagnskostnað eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="b7752-137">In the general ledger, an electricity cost can be posted as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b7752-138">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="b7752-138">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b7752-139">Kostnaðarstaður</span><span class="sxs-lookup"><span data-stu-id="b7752-139">Cost center</span></span></th>
<th colspan="2"><span data-ttu-id="b7752-140">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="b7752-140">Main account</span></span></th>
<th><span data-ttu-id="b7752-141">Upphæð í bókhaldsgjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="b7752-141">Amount in the accounting currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-142">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-142">January 3, 2017</span></span></td>
<td><span data-ttu-id="b7752-143">CC099</span><span class="sxs-lookup"><span data-stu-id="b7752-143">CC099</span></span></td>
<td><span data-ttu-id="b7752-144">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="b7752-144">Default cost center</span></span></td>
<td><span data-ttu-id="b7752-145">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-145">10001</span></span></td>
<td><span data-ttu-id="b7752-146">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-146">Electricity</span></span></td>
<td><span data-ttu-id="b7752-147">10.000,00</span><span class="sxs-lookup"><span data-stu-id="b7752-147">10,000.00</span></span></td>
</tr>
</tbody>
</table>

### <a name="step-1-process-the-cost-behavior-calculation"></a><span data-ttu-id="b7752-148">Skref 1: Keyra útreikning kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="b7752-148">Step 1: Process the cost behavior calculation</span></span>

<span data-ttu-id="b7752-149">Sjálfvirkt er að þegar kostnaðarfærslur eru fluttar úr grunngögnum fái þær flokkun kostnaðarhegðunar **Óflokkað** í kostnaðarbókhaldi.</span><span class="sxs-lookup"><span data-stu-id="b7752-149">By default, when cost entries are imported from the source data, they receive the **Unclassified** cost behavior classification in Cost accounting.</span></span> <span data-ttu-id="b7752-150">Með því að nota stefnureglur kostnaðarhegðunar er hægt að endurflokka kostnaðarfærslur sem annaðhvort **Fastan kostnað** eða **Breytilegan kostnað**.</span><span class="sxs-lookup"><span data-stu-id="b7752-150">By applying cost behavior policy rules, you can reclassify cost entries as either **Fixed cost** or **Variable cost**.</span></span>

#### <a name="define-the-cost-behavior-rule"></a><span data-ttu-id="b7752-151">Tilgreinið reglu kostnaðarhegðunar</span><span class="sxs-lookup"><span data-stu-id="b7752-151">Define the cost behavior rule</span></span>

<span data-ttu-id="b7752-152">Í sumum tilfellum er hluti af kostnaði föst þóknun og eftirstandandi kostnaður byggist á notkun.</span><span class="sxs-lookup"><span data-stu-id="b7752-152">In some cases, part of the cost is a fixed fee, and the remaining cost is based on consumption.</span></span> <span data-ttu-id="b7752-153">Rafmagnsreikningar stemma oft við þessa skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="b7752-153">Electricity bills often match this definition.</span></span> <span data-ttu-id="b7752-154">Þegar tiltekin föst þóknun hefur verið greidd, er greitt fyrir notkun á kílóvattklukkustund (Kwh).</span><span class="sxs-lookup"><span data-stu-id="b7752-154">After you pay a specific fixed fee, you pay for consumption per kilowatt hour (Kwh).</span></span> <span data-ttu-id="b7752-155">Til dæmis ef föst kostnaðarþóknun er 1000.00 sýnir þetta hvernig regla kostnaðarhegðunar er skilgreind:</span><span class="sxs-lookup"><span data-stu-id="b7752-155">For example, if the fixed cost fee is 1,000.00, here is how the cost behavior rule is defined:</span></span>

-   <span data-ttu-id="b7752-156">Föst upphæð 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b7752-156">Fixed amount 1,000.00</span></span>
    -   <span data-ttu-id="b7752-157">0 &lt;= 1.000,00 = Fast</span><span class="sxs-lookup"><span data-stu-id="b7752-157">0 &lt;= 1,000.00 = Fixed</span></span>
    -   <span data-ttu-id="b7752-158">1000.01 &lt; N = Breyta</span><span class="sxs-lookup"><span data-stu-id="b7752-158">1000,01 &lt; N = Variable</span></span>

##### <a name="journal"></a><span data-ttu-id="b7752-159">Færslubók</span><span class="sxs-lookup"><span data-stu-id="b7752-159">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b7752-160">Færslubók</span><span class="sxs-lookup"><span data-stu-id="b7752-160">Journal</span></span></th>
<th><span data-ttu-id="b7752-161">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="b7752-161">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b7752-162">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="b7752-162">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b7752-163">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="b7752-163">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-164">00001</span><span class="sxs-lookup"><span data-stu-id="b7752-164">00001</span></span></td>
<td><span data-ttu-id="b7752-165">Færslubók útreiknings fyrir kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="b7752-165">Cost behavior calculation journal</span></span></td>
<td><span data-ttu-id="b7752-166">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="b7752-166">Fiscal</span></span></td>
<td><span data-ttu-id="b7752-167">2017</span><span class="sxs-lookup"><span data-stu-id="b7752-167">2017</span></span></td>
<td><span data-ttu-id="b7752-168">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="b7752-168">Period 1</span></span></td>
<td><span data-ttu-id="b7752-169">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="b7752-169">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b7752-170">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="b7752-170">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b7752-171">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="b7752-171">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b7752-172">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-172">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b7752-173">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="b7752-173">Cost element</span></span></th>
<th><span data-ttu-id="b7752-174">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="b7752-174">Cost behavior</span></span></th>
<th><span data-ttu-id="b7752-175">Upphæð</span><span class="sxs-lookup"><span data-stu-id="b7752-175">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-176">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-176">January 3, 2017</span></span></td>
<td><span data-ttu-id="b7752-177">CC099</span><span class="sxs-lookup"><span data-stu-id="b7752-177">CC099</span></span></td>
<td><span data-ttu-id="b7752-178">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="b7752-178">Default cost center</span></span></td>
<td><span data-ttu-id="b7752-179">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-179">10001</span></span></td>
<td><span data-ttu-id="b7752-180">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-180">Electricity</span></span></td>
<td><span data-ttu-id="b7752-181">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="b7752-181">Unclassified</span></span></td>
<td><span data-ttu-id="b7752-182">10.000,00</span><span class="sxs-lookup"><span data-stu-id="b7752-182">10,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b7752-183">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="b7752-183">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7752-184">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-184">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b7752-185">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="b7752-185">Cost element</span></span></th>
<th><span data-ttu-id="b7752-186">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="b7752-186">Cost behavior</span></span></th>
<th><span data-ttu-id="b7752-187">Upphæð</span><span class="sxs-lookup"><span data-stu-id="b7752-187">Amount</span></span></th>
<th><span data-ttu-id="b7752-188">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="b7752-188">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-189">CC099</span><span class="sxs-lookup"><span data-stu-id="b7752-189">CC099</span></span></td>
<td><span data-ttu-id="b7752-190">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="b7752-190">Default cost center</span></span></td>
<td><span data-ttu-id="b7752-191">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-191">10001</span></span></td>
<td><span data-ttu-id="b7752-192">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-192">Electricity</span></span></td>
<td><span data-ttu-id="b7752-193">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="b7752-193">Unclassified</span></span></td>
<td><span data-ttu-id="b7752-194">10.000,00</span><span class="sxs-lookup"><span data-stu-id="b7752-194">10,000.00</span></span></td>
<td><span data-ttu-id="b7752-195">3. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-195">January 3, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-196">CC099</span><span class="sxs-lookup"><span data-stu-id="b7752-196">CC099</span></span></td>
<td><span data-ttu-id="b7752-197">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="b7752-197">Default cost center</span></span></td>
<td><span data-ttu-id="b7752-198">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-198">10001</span></span></td>
<td><span data-ttu-id="b7752-199">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-199">Electricity</span></span></td>
<td><span data-ttu-id="b7752-200">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="b7752-200">Unclassified</span></span></td>
<td><span data-ttu-id="b7752-201">-10.000,00</span><span class="sxs-lookup"><span data-stu-id="b7752-201">-10,000.00</span></span></td>
<td><span data-ttu-id="b7752-202">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-202">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-203">CC099</span><span class="sxs-lookup"><span data-stu-id="b7752-203">CC099</span></span></td>
<td><span data-ttu-id="b7752-204">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="b7752-204">Default cost center</span></span></td>
<td><span data-ttu-id="b7752-205">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-205">10001</span></span></td>
<td><span data-ttu-id="b7752-206">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-206">Electricity</span></span></td>
<td><span data-ttu-id="b7752-207">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-207">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-208">1.000,00</span><span class="sxs-lookup"><span data-stu-id="b7752-208">1,000.00</span></span></td>
<td><span data-ttu-id="b7752-209">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-209">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-210">CC099</span><span class="sxs-lookup"><span data-stu-id="b7752-210">CC099</span></span></td>
<td><span data-ttu-id="b7752-211">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="b7752-211">Default cost center</span></span></td>
<td><span data-ttu-id="b7752-212">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-212">10001</span></span></td>
<td><span data-ttu-id="b7752-213">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-213">Electricity</span></span></td>
<td><span data-ttu-id="b7752-214">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-214">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-215">9,000.00</span><span class="sxs-lookup"><span data-stu-id="b7752-215">9,000.00</span></span></td>
<td><span data-ttu-id="b7752-216">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-216">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7752-217">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðarhegðunarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="b7752-217">For more information, see [Create and assign a cost behavior policy to a cost control unit](tasks/create-assign-cost-behavior-policy-cost-control-unit.md).</span></span>
### <a name="step-2-process-the-cost-distribution-calculation"></a><span data-ttu-id="b7752-218">Skref 2: Keyra útreikning kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="b7752-218">Step 2: Process the cost distribution calculation</span></span>

<span data-ttu-id="b7752-219">Kostnaðardreifing er notuð til að endurúthluta kostnaði frá einum kostnaðarhlut til annars eða fleiri kostnaðarhluta með því að nota viðeigandi úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="b7752-219">Cost distribution is used to redistribute cost from one cost object to one or more other cost objects by applying a relevant allocation base.</span></span> <span data-ttu-id="b7752-220">Kostnaðardreifing og kostnaðarúthlutun eru ólíkar að því leyti að kostnaðardreifing kemur alltaf upp á stigi aðalkostnaðareiningar upphaflegs verðs.</span><span class="sxs-lookup"><span data-stu-id="b7752-220">Cost distribution and cost allocation differ in that cost distribution always occurs at the level of the primary cost element of the original cost.</span></span>

#### <a name="define-the-cost-distribution-rule"></a><span data-ttu-id="b7752-221">Tilgreinið kostnaðardreifingarreglu</span><span class="sxs-lookup"><span data-stu-id="b7752-221">Define the cost distribution rule</span></span>

<span data-ttu-id="b7752-222">Í Fjárhagsbókhaldi er rafmagnskostnaður oft skráður sem eingreiðsla.</span><span class="sxs-lookup"><span data-stu-id="b7752-222">In Financial accounting, electricity costs are often registered as a lump sum.</span></span> <span data-ttu-id="b7752-223">Í kostnaðarbókhaldi er þessi nálgun ekki nógu nákvæm.</span><span class="sxs-lookup"><span data-stu-id="b7752-223">In Cost accounting, this approach isn't detailed enough.</span></span> <span data-ttu-id="b7752-224">Breytilegur kostnaði þarf að dreifa á staka kostnaðarhluti á sanngjörnum grunni.</span><span class="sxs-lookup"><span data-stu-id="b7752-224">The variable cost should be distributed to the individual cost objects on a fair basis.</span></span> <span data-ttu-id="b7752-225">Rökréttasti úthlutunargrunnurinn er notkun á rafmagni (Kwh).</span><span class="sxs-lookup"><span data-stu-id="b7752-225">The most logical allocation basis is the consumption of electricity (Kwh).</span></span> <span data-ttu-id="b7752-226">Stofnað er tölfræðilegt víddarstak sem er nefnt Rafmagn og rafmagnsnotkun er skráð.</span><span class="sxs-lookup"><span data-stu-id="b7752-226">A statistical dimension member that is named Electricity is created, and electricity consumption is recorded.</span></span> <span data-ttu-id="b7752-227">Sjálfgefið er að öll tölfræðileg víddarstök verða tiltæk sem úthlutunargrunnur.</span><span class="sxs-lookup"><span data-stu-id="b7752-227">By default, all statistical dimension members become available as allocation bases.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7752-228">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-228">Cost object</span></span></th>
<th><span data-ttu-id="b7752-229">Kwh</span><span class="sxs-lookup"><span data-stu-id="b7752-229">Kwh</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-230">CC001</span><span class="sxs-lookup"><span data-stu-id="b7752-230">CC001</span></span></td>
<td><span data-ttu-id="b7752-231">Mannauður</span><span class="sxs-lookup"><span data-stu-id="b7752-231">HR</span></span></td>
<td><span data-ttu-id="b7752-232">1.000</span><span class="sxs-lookup"><span data-stu-id="b7752-232">1,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-233">CC002</span><span class="sxs-lookup"><span data-stu-id="b7752-233">CC002</span></span></td>
<td><span data-ttu-id="b7752-234">Fjármál</span><span class="sxs-lookup"><span data-stu-id="b7752-234">Finance</span></span></td>
<td><span data-ttu-id="b7752-235">6,000</span><span class="sxs-lookup"><span data-stu-id="b7752-235">6,000</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-236">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-236">CC003</span></span></td>
<td><span data-ttu-id="b7752-237">Smölun</span><span class="sxs-lookup"><span data-stu-id="b7752-237">Assembly</span></span></td>
<td><span data-ttu-id="b7752-238">0</span><span class="sxs-lookup"><span data-stu-id="b7752-238">0</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7752-239">Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunni fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="b7752-239">The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7752-240">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-240">Cost object</span></span></th>
<th><span data-ttu-id="b7752-241">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="b7752-241">Magnitude</span></span></th>
<th><span data-ttu-id="b7752-242">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="b7752-242">Allocation factor</span></span></th>
<th><span data-ttu-id="b7752-243">Upphæð</span><span class="sxs-lookup"><span data-stu-id="b7752-243">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-244">CC001</span><span class="sxs-lookup"><span data-stu-id="b7752-244">CC001</span></span></td>
<td><span data-ttu-id="b7752-245">Mannauður</span><span class="sxs-lookup"><span data-stu-id="b7752-245">HR</span></span></td>
<td><span data-ttu-id="b7752-246">1.000</span><span class="sxs-lookup"><span data-stu-id="b7752-246">1,000</span></span></td>
<td><span data-ttu-id="b7752-247">(1.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="b7752-247">(1,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b7752-248">1,285.71</span><span class="sxs-lookup"><span data-stu-id="b7752-248">1,285.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-249">CC002</span><span class="sxs-lookup"><span data-stu-id="b7752-249">CC002</span></span></td>
<td><span data-ttu-id="b7752-250">Fjármál</span><span class="sxs-lookup"><span data-stu-id="b7752-250">Finance</span></span></td>
<td><span data-ttu-id="b7752-251">6,000</span><span class="sxs-lookup"><span data-stu-id="b7752-251">6,000</span></span></td>
<td><span data-ttu-id="b7752-252">(6.000 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="b7752-252">(6,000 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b7752-253">7,714.29</span><span class="sxs-lookup"><span data-stu-id="b7752-253">7,714.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-254">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-254">CC003</span></span></td>
<td><span data-ttu-id="b7752-255">Smölun</span><span class="sxs-lookup"><span data-stu-id="b7752-255">Assembly</span></span></td>
<td><span data-ttu-id="b7752-256">0</span><span class="sxs-lookup"><span data-stu-id="b7752-256">0</span></span></td>
<td><span data-ttu-id="b7752-257">(0 ÷ 7.000) × 9.000,00</span><span class="sxs-lookup"><span data-stu-id="b7752-257">(0 ÷ 7,000) × 9,000.00</span></span></td>
<td><span data-ttu-id="b7752-258">0,00</span><span class="sxs-lookup"><span data-stu-id="b7752-258">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7752-259">Föstum kostnaði þarf að dreifa jafnt á staka kostnaðarhluti sem hafa notað rafmagn.</span><span class="sxs-lookup"><span data-stu-id="b7752-259">The fixed cost should be distributed evenly to the individual cost objects that have consumed electricity.</span></span> <span data-ttu-id="b7752-260">Hægt er að ná þessa niðurstöðu með því að nota tölfræðilegt víddarstakið Rafmagn í úthlutunargrunni reikniformúlu: (Rafmagn &gt; 0,00) Eftirfarandi tafla sýnir niðurstöður þegar rafmagnsnotkun er beitt sem úthlutunargrunn fyrir breytilegan kostnað.</span><span class="sxs-lookup"><span data-stu-id="b7752-260">You can achieve this result by using the Electricity statistical dimension member in a formula allocation base: (Electricity &gt; 0.00) The following table shows the result when electricity consumption is applied as an allocation base for variable costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7752-261">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-261">Cost object</span></span></th>
<th><span data-ttu-id="b7752-262">Formúla</span><span class="sxs-lookup"><span data-stu-id="b7752-262">Formula</span></span></th>
<th><span data-ttu-id="b7752-263">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="b7752-263">Magnitude</span></span></th>
<th><span data-ttu-id="b7752-264">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="b7752-264">Allocation factor</span></span></th>
<th><span data-ttu-id="b7752-265">Upphæð</span><span class="sxs-lookup"><span data-stu-id="b7752-265">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-266">CC001</span><span class="sxs-lookup"><span data-stu-id="b7752-266">CC001</span></span></td>
<td><span data-ttu-id="b7752-267">Mannauður</span><span class="sxs-lookup"><span data-stu-id="b7752-267">HR</span></span></td>
<td><span data-ttu-id="b7752-268">(1.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b7752-268">(1,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b7752-269">1</span><span class="sxs-lookup"><span data-stu-id="b7752-269">1</span></span></td>
<td><span data-ttu-id="b7752-270">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b7752-270">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b7752-271">500,00</span><span class="sxs-lookup"><span data-stu-id="b7752-271">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-272">CC002</span><span class="sxs-lookup"><span data-stu-id="b7752-272">CC002</span></span></td>
<td><span data-ttu-id="b7752-273">Fjármál</span><span class="sxs-lookup"><span data-stu-id="b7752-273">Finance</span></span></td>
<td><span data-ttu-id="b7752-274">(6.000 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b7752-274">(6,000 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b7752-275">1</span><span class="sxs-lookup"><span data-stu-id="b7752-275">1</span></span></td>
<td><span data-ttu-id="b7752-276">(1 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b7752-276">(1 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b7752-277">500,00</span><span class="sxs-lookup"><span data-stu-id="b7752-277">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-278">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-278">CC003</span></span></td>
<td><span data-ttu-id="b7752-279">Smölun</span><span class="sxs-lookup"><span data-stu-id="b7752-279">Assembly</span></span></td>
<td><span data-ttu-id="b7752-280">(0 &gt; 0,00)</span><span class="sxs-lookup"><span data-stu-id="b7752-280">(0 &gt; 0.00)</span></span></td>
<td><span data-ttu-id="b7752-281">0</span><span class="sxs-lookup"><span data-stu-id="b7752-281">0</span></span></td>
<td><span data-ttu-id="b7752-282">(0 ÷ 2) × 1.000,00</span><span class="sxs-lookup"><span data-stu-id="b7752-282">(0 ÷ 2) × 1,000.00</span></span></td>
<td><span data-ttu-id="b7752-283">0,00</span><span class="sxs-lookup"><span data-stu-id="b7752-283">0.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="b7752-284">Færslubók</span><span class="sxs-lookup"><span data-stu-id="b7752-284">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b7752-285">Færslubók</span><span class="sxs-lookup"><span data-stu-id="b7752-285">Journal</span></span></th>
<th><span data-ttu-id="b7752-286">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="b7752-286">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b7752-287">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="b7752-287">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b7752-288">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="b7752-288">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-289">00002</span><span class="sxs-lookup"><span data-stu-id="b7752-289">00002</span></span></td>
<td><span data-ttu-id="b7752-290">Útreikningabók kostnaðardreifingar</span><span class="sxs-lookup"><span data-stu-id="b7752-290">Cost distribution calculation journal</span></span></td>
<td><span data-ttu-id="b7752-291">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="b7752-291">Fiscal</span></span></td>
<td><span data-ttu-id="b7752-292">2017</span><span class="sxs-lookup"><span data-stu-id="b7752-292">2017</span></span></td>
<td><span data-ttu-id="b7752-293">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="b7752-293">Period 1</span></span></td>
<td><span data-ttu-id="b7752-294">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="b7752-294">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b7752-295">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="b7752-295">Journal entries (Cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b7752-296">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="b7752-296">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b7752-297">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-297">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b7752-298">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="b7752-298">Cost element</span></span></th>
<th><span data-ttu-id="b7752-299">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="b7752-299">Cost behavior</span></span></th>
<th><span data-ttu-id="b7752-300">Upphæð</span><span class="sxs-lookup"><span data-stu-id="b7752-300">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-301">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-301">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7752-302">CC099</span><span class="sxs-lookup"><span data-stu-id="b7752-302">CC099</span></span></td>
<td><span data-ttu-id="b7752-303">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="b7752-303">Default cost center</span></span></td>
<td><span data-ttu-id="b7752-304">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-304">10001</span></span></td>
<td><span data-ttu-id="b7752-305">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-305">Electricity</span></span></td>
<td><span data-ttu-id="b7752-306">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-306">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-307">1.000,00</span><span class="sxs-lookup"><span data-stu-id="b7752-307">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-308">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-308">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7752-309">CC099</span><span class="sxs-lookup"><span data-stu-id="b7752-309">CC099</span></span></td>
<td><span data-ttu-id="b7752-310">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="b7752-310">Default cost center</span></span></td>
<td><span data-ttu-id="b7752-311">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-311">10001</span></span></td>
<td><span data-ttu-id="b7752-312">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-312">Electricity</span></span></td>
<td><span data-ttu-id="b7752-313">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-313">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-314">9,000.00</span><span class="sxs-lookup"><span data-stu-id="b7752-314">9,000.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b7752-315">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="b7752-315">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7752-316">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-316">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b7752-317">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="b7752-317">Cost element</span></span></th>
<th><span data-ttu-id="b7752-318">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="b7752-318">Cost behavior</span></span></th>
<th><span data-ttu-id="b7752-319">Upphæð</span><span class="sxs-lookup"><span data-stu-id="b7752-319">Amount</span></span></th>
<th><span data-ttu-id="b7752-320">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="b7752-320">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-321">CC099</span><span class="sxs-lookup"><span data-stu-id="b7752-321">CC099</span></span></td>
<td><span data-ttu-id="b7752-322">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="b7752-322">Default cost center</span></span></td>
<td><span data-ttu-id="b7752-323">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-323">10001</span></span></td>
<td><span data-ttu-id="b7752-324">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-324">Electricity</span></span></td>
<td><span data-ttu-id="b7752-325">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-325">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-326">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="b7752-326">-1,000.00</span></span></td>
<td><span data-ttu-id="b7752-327">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-327">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-328">CC001</span><span class="sxs-lookup"><span data-stu-id="b7752-328">CC001</span></span></td>
<td><span data-ttu-id="b7752-329">Mannauður</span><span class="sxs-lookup"><span data-stu-id="b7752-329">HR</span></span></td>
<td><span data-ttu-id="b7752-330">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-330">10001</span></span></td>
<td><span data-ttu-id="b7752-331">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-331">Electricity</span></span></td>
<td><span data-ttu-id="b7752-332">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-332">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-333">500,00</span><span class="sxs-lookup"><span data-stu-id="b7752-333">500.00</span></span></td>
<td><span data-ttu-id="b7752-334">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-334">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-335">CC002</span><span class="sxs-lookup"><span data-stu-id="b7752-335">CC002</span></span></td>
<td><span data-ttu-id="b7752-336">Fjármál</span><span class="sxs-lookup"><span data-stu-id="b7752-336">Finance</span></span></td>
<td><span data-ttu-id="b7752-337">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-337">10001</span></span></td>
<td><span data-ttu-id="b7752-338">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-338">Electricity</span></span></td>
<td><span data-ttu-id="b7752-339">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-339">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-340">500,00</span><span class="sxs-lookup"><span data-stu-id="b7752-340">500.00</span></span></td>
<td><span data-ttu-id="b7752-341">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-341">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-342">CC099</span><span class="sxs-lookup"><span data-stu-id="b7752-342">CC099</span></span></td>
<td><span data-ttu-id="b7752-343">Sjálfgefin hlutverkamiðstöð</span><span class="sxs-lookup"><span data-stu-id="b7752-343">Default cost center</span></span></td>
<td><span data-ttu-id="b7752-344">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-344">10001</span></span></td>
<td><span data-ttu-id="b7752-345">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-345">Electricity</span></span></td>
<td><span data-ttu-id="b7752-346">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-346">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-347">-9.000,00</span><span class="sxs-lookup"><span data-stu-id="b7752-347">-9,000.00</span></span></td>
<td><span data-ttu-id="b7752-348">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-348">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-349">CC001</span><span class="sxs-lookup"><span data-stu-id="b7752-349">CC001</span></span></td>
<td><span data-ttu-id="b7752-350">Mannauður</span><span class="sxs-lookup"><span data-stu-id="b7752-350">HR</span></span></td>
<td><span data-ttu-id="b7752-351">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-351">10001</span></span></td>
<td><span data-ttu-id="b7752-352">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-352">Electricity</span></span></td>
<td><span data-ttu-id="b7752-353">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-353">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-354">1,285.71</span><span class="sxs-lookup"><span data-stu-id="b7752-354">1,285.71</span></span></td>
<td><span data-ttu-id="b7752-355">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-355">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-356">CC002</span><span class="sxs-lookup"><span data-stu-id="b7752-356">CC002</span></span></td>
<td><span data-ttu-id="b7752-357">Fjármál</span><span class="sxs-lookup"><span data-stu-id="b7752-357">Finance</span></span></td>
<td><span data-ttu-id="b7752-358">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-358">10001</span></span></td>
<td><span data-ttu-id="b7752-359">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-359">Electricity</span></span></td>
<td><span data-ttu-id="b7752-360">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-360">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-361">7,714.29</span><span class="sxs-lookup"><span data-stu-id="b7752-361">7,714.29</span></span></td>
<td><span data-ttu-id="b7752-362">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-362">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7752-363">Nánari upplýsingar er að finna í [Stofna og úthluta kostnaðardreifingarreglu fyrir kostnaðarstýringareiningu](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span><span class="sxs-lookup"><span data-stu-id="b7752-363">For more information, see [Create and assign a cost distribution policy to a cost control unit](tasks/create-assign-cost-distribution-policy-cost-control-unit.md).</span></span> 

### <a name="step-3-process-the-overhead-rate-calculation"></a><span data-ttu-id="b7752-364">Skref 3: Keyra útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="b7752-364">Step 3: Process the overhead rate calculation</span></span>

<span data-ttu-id="b7752-365">Sameiginlegur kostnaður er notaður til að rukka einn eða fleiri tilgreinda kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="b7752-365">The overhead rate is used to charge one or more specific cost objects.</span></span> <span data-ttu-id="b7752-366">Gjöldin byggjast á fyrirframákveðnu kostnaðarhlutfalli og mæligildi úr úthlutuðum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="b7752-366">The charge is based on a predetermined cost rate and the magnitude from the assigned allocation base.</span></span> 

#### <a name="define-the-overhead-rate"></a><span data-ttu-id="b7752-367">Skilgreina sameiginlegan kostnað</span><span class="sxs-lookup"><span data-stu-id="b7752-367">Define the overhead rate</span></span>

<span data-ttu-id="b7752-368">Kostnaðarhlutur CC001 Mannauður stuðlar að safni innri verka.</span><span class="sxs-lookup"><span data-stu-id="b7752-368">Cost object CC001 HR contributes to a set of internal projects.</span></span> <span data-ttu-id="b7752-369">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsverk til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="b7752-369">A statistical dimension member that is named HR projects is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7752-370">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-370">Cost object</span></span></th>
<th><span data-ttu-id="b7752-371">Tímar</span><span class="sxs-lookup"><span data-stu-id="b7752-371">Hours</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-372">Verk 1</span><span class="sxs-lookup"><span data-stu-id="b7752-372">Proj 1</span></span></td>
<td><span data-ttu-id="b7752-373">Verk 1</span><span class="sxs-lookup"><span data-stu-id="b7752-373">Project 1</span></span></td>
<td><span data-ttu-id="b7752-374">3</span><span class="sxs-lookup"><span data-stu-id="b7752-374">3</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-375">Verk 2</span><span class="sxs-lookup"><span data-stu-id="b7752-375">Proj 2</span></span></td>
<td><span data-ttu-id="b7752-376">Verk 2</span><span class="sxs-lookup"><span data-stu-id="b7752-376">Project 2</span></span></td>
<td><span data-ttu-id="b7752-377">1</span><span class="sxs-lookup"><span data-stu-id="b7752-377">1</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7752-378">Fyrirframákveðið kostnaðarhlutfall fyrir kostnaðarframlag verk hefur verið skilgreint.</span><span class="sxs-lookup"><span data-stu-id="b7752-378">A predetermined cost rate for the cost projects contribution has been defined.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7752-379">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-379">Cost object</span></span></th>
<th><span data-ttu-id="b7752-380">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="b7752-380">Cost element</span></span></th>
<th><span data-ttu-id="b7752-381">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="b7752-381">Cost behavior</span></span></th>
<th><span data-ttu-id="b7752-382">Einingar</span><span class="sxs-lookup"><span data-stu-id="b7752-382">Units</span></span></th>
<th><span data-ttu-id="b7752-383">Taxti</span><span class="sxs-lookup"><span data-stu-id="b7752-383">Rate</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-384">CC001</span><span class="sxs-lookup"><span data-stu-id="b7752-384">CC001</span></span></td>
<td><span data-ttu-id="b7752-385">Mannauður</span><span class="sxs-lookup"><span data-stu-id="b7752-385">HR</span></span></td>
<td><span data-ttu-id="b7752-386">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-386">10001</span></span></td>
<td><span data-ttu-id="b7752-387">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-387">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-388">1</span><span class="sxs-lookup"><span data-stu-id="b7752-388">1</span></span></td>
<td><span data-ttu-id="b7752-389">10</span><span class="sxs-lookup"><span data-stu-id="b7752-389">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7752-390">Eftirfarandi tafla sýnir niðurstöður þegar Mannauðsverk eru notuð sem grunnur við úthlutun.</span><span class="sxs-lookup"><span data-stu-id="b7752-390">The following table shows the result when the HR projects are applied as an allocation base.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7752-391">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-391">Cost object</span></span></th>
<th><span data-ttu-id="b7752-392">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="b7752-392">Magnitude</span></span></th>
<th><span data-ttu-id="b7752-393">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="b7752-393">Cost element</span></span></th>
<th><span data-ttu-id="b7752-394">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="b7752-394">Allocation factor</span></span></th>
<th><span data-ttu-id="b7752-395">Upphæð</span><span class="sxs-lookup"><span data-stu-id="b7752-395">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-396">Verk 1</span><span class="sxs-lookup"><span data-stu-id="b7752-396">Proj 1</span></span></td>
<td><span data-ttu-id="b7752-397">Verk 1</span><span class="sxs-lookup"><span data-stu-id="b7752-397">Project 1</span></span></td>
<td><span data-ttu-id="b7752-398">3</span><span class="sxs-lookup"><span data-stu-id="b7752-398">3</span></span></td>
<td><span data-ttu-id="b7752-399">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-399">10001</span></span></td>
<td><span data-ttu-id="b7752-400">(3 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="b7752-400">(3 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="b7752-401">30,00</span><span class="sxs-lookup"><span data-stu-id="b7752-401">30.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-402">Verk 2</span><span class="sxs-lookup"><span data-stu-id="b7752-402">Proj 2</span></span></td>
<td><span data-ttu-id="b7752-403">Verk 2</span><span class="sxs-lookup"><span data-stu-id="b7752-403">Project 2</span></span></td>
<td><span data-ttu-id="b7752-404">1</span><span class="sxs-lookup"><span data-stu-id="b7752-404">1</span></span></td>
<td><span data-ttu-id="b7752-405">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-405">10001</span></span></td>
<td><span data-ttu-id="b7752-406">(1 ÷ 1) × 10,00</span><span class="sxs-lookup"><span data-stu-id="b7752-406">(1 ÷ 1) × 10.00</span></span></td>
<td><span data-ttu-id="b7752-407">10,00</span><span class="sxs-lookup"><span data-stu-id="b7752-407">10.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal"></a><span data-ttu-id="b7752-408">Færslubók</span><span class="sxs-lookup"><span data-stu-id="b7752-408">Journal</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b7752-409">Færslubók</span><span class="sxs-lookup"><span data-stu-id="b7752-409">Journal</span></span></th>
<th><span data-ttu-id="b7752-410">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="b7752-410">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b7752-411">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="b7752-411">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b7752-412">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="b7752-412">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-413">00003</span><span class="sxs-lookup"><span data-stu-id="b7752-413">00003</span></span></td>
<td><span data-ttu-id="b7752-414">Færslubók fyrir útreikning sameiginlegs kostnaðar</span><span class="sxs-lookup"><span data-stu-id="b7752-414">Overhead rate calculation journal</span></span></td>
<td><span data-ttu-id="b7752-415">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="b7752-415">Fiscal</span></span></td>
<td><span data-ttu-id="b7752-416">2017</span><span class="sxs-lookup"><span data-stu-id="b7752-416">2017</span></span></td>
<td><span data-ttu-id="b7752-417">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="b7752-417">Period 1</span></span></td>
<td><span data-ttu-id="b7752-418">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="b7752-418">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-journal-entries-for-overhead-rate-calculation"></a><span data-ttu-id="b7752-419">Bókarfærslur (Bókarfærslur fyrir útreikning sameiginlegs kostnaðar)</span><span class="sxs-lookup"><span data-stu-id="b7752-419">Journal entries (Journal entries for overhead rate calculation)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b7752-420">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="b7752-420">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b7752-421">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-421">Cost object</span></span></th>
<th><span data-ttu-id="b7752-422">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="b7752-422">Magnitude</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-423">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-423">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7752-424">Verk 1</span><span class="sxs-lookup"><span data-stu-id="b7752-424">Proj 1</span></span></td>
<td><span data-ttu-id="b7752-425">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="b7752-425">Internal Proj 1</span></span></td>
<td><span data-ttu-id="b7752-426">3,00</span><span class="sxs-lookup"><span data-stu-id="b7752-426">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-427">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-427">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7752-428">Verk 2</span><span class="sxs-lookup"><span data-stu-id="b7752-428">Proj 2</span></span></td>
<td><span data-ttu-id="b7752-429">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="b7752-429">Internal Proj 2</span></span></td>
<td><span data-ttu-id="b7752-430">1,00</span><span class="sxs-lookup"><span data-stu-id="b7752-430">1.00</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b7752-431">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="b7752-431">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7752-432">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-432">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b7752-433">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="b7752-433">Cost element</span></span></th>
<th><span data-ttu-id="b7752-434">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="b7752-434">Cost behavior</span></span></th>
<th><span data-ttu-id="b7752-435">Upphæð</span><span class="sxs-lookup"><span data-stu-id="b7752-435">Amount</span></span></th>
<th><span data-ttu-id="b7752-436">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="b7752-436">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-437">CC0001</span><span class="sxs-lookup"><span data-stu-id="b7752-437">CC0001</span></span></td>
<td><span data-ttu-id="b7752-438">Mannauður</span><span class="sxs-lookup"><span data-stu-id="b7752-438">HR</span></span></td>
<td><span data-ttu-id="b7752-439">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-439">10001</span></span></td>
<td><span data-ttu-id="b7752-440">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-440">Electricity</span></span></td>
<td><span data-ttu-id="b7752-441">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-441">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-442">-30,00</span><span class="sxs-lookup"><span data-stu-id="b7752-442">-30.00</span></span></td>
<td><span data-ttu-id="b7752-443">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-443">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-444">Verk 1</span><span class="sxs-lookup"><span data-stu-id="b7752-444">Proj 1</span></span></td>
<td><span data-ttu-id="b7752-445">Innanhúsverk 1</span><span class="sxs-lookup"><span data-stu-id="b7752-445">Internal Proj 1</span></span></td>
<td><span data-ttu-id="b7752-446">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-446">10001</span></span></td>
<td><span data-ttu-id="b7752-447">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-447">Electricity</span></span></td>
<td><span data-ttu-id="b7752-448">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-448">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-449">30,00</span><span class="sxs-lookup"><span data-stu-id="b7752-449">30.00</span></span></td>
<td><span data-ttu-id="b7752-450">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-450">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-451">CC001</span><span class="sxs-lookup"><span data-stu-id="b7752-451">CC001</span></span></td>
<td><span data-ttu-id="b7752-452">Mannauður</span><span class="sxs-lookup"><span data-stu-id="b7752-452">HR</span></span></td>
<td><span data-ttu-id="b7752-453">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-453">10001</span></span></td>
<td><span data-ttu-id="b7752-454">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-454">Electricity</span></span></td>
<td><span data-ttu-id="b7752-455">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-455">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-456">-10,00</span><span class="sxs-lookup"><span data-stu-id="b7752-456">-10.00</span></span></td>
<td><span data-ttu-id="b7752-457">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-457">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-458">Verk 2</span><span class="sxs-lookup"><span data-stu-id="b7752-458">Proj 2</span></span></td>
<td><span data-ttu-id="b7752-459">Innanhúsverk 2</span><span class="sxs-lookup"><span data-stu-id="b7752-459">Internal Proj 2</span></span></td>
<td><span data-ttu-id="b7752-460">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-460">10001</span></span></td>
<td><span data-ttu-id="b7752-461">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-461">Electricity</span></span></td>
<td><span data-ttu-id="b7752-462">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-462">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-463">10,00</span><span class="sxs-lookup"><span data-stu-id="b7752-463">10.00</span></span></td>
<td><span data-ttu-id="b7752-464">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-464">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7752-465">Nánari upplýsingar er að finna í [Framkvæma útreikning fastakostnaðar](cost-rollup.md#perform-overhead-calculation).</span><span class="sxs-lookup"><span data-stu-id="b7752-465">For more information, see [Perform overhead calculation](cost-rollup.md#perform-overhead-calculation).</span></span>

### <a name="step-4-process-the-cost-allocation-calculation"></a><span data-ttu-id="b7752-466">Skref 4: Keyra útreikning kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="b7752-466">Step 4: Process the cost allocation calculation</span></span>

<span data-ttu-id="b7752-467">Úthlutun er notuð til að úthluta stöðu kostnaðarhlutar í öðrum kostnaðarhlutum með því að nota úthlutunargrunn.</span><span class="sxs-lookup"><span data-stu-id="b7752-467">Allocation is used to allocate the balance of a cost object to other cost objects by applying an allocation base.</span></span> <span data-ttu-id="b7752-468">Finance styður gagnvirka úthlutunaraðferð.</span><span class="sxs-lookup"><span data-stu-id="b7752-468">Finance supports the reciprocal allocation method.</span></span> <span data-ttu-id="b7752-469">Í gagnvirkri úthlutunaraðferð er sú sameiginlega þjónusta sem hjálparkostnaðarhlutir skiptast á viðurkennd að fullu.</span><span class="sxs-lookup"><span data-stu-id="b7752-469">In the reciprocal allocation method, the mutual services that auxiliary cost objects exchange are fully recognized.</span></span> <span data-ttu-id="b7752-470">Kerfið ákvarðar sjálfkrafa rétta röð til að framkvæma úthlutun eftir.</span><span class="sxs-lookup"><span data-stu-id="b7752-470">The system automatically determines the correct order to perform the allocations in.</span></span> <span data-ttu-id="b7752-471">Stöðu kostnaðarhluta er úthlutað með einum úthlutunargrunni.</span><span class="sxs-lookup"><span data-stu-id="b7752-471">The balance of a cost object is allocated by a single allocation base.</span></span> <span data-ttu-id="b7752-472">Úthlutanir þvert á víddir kostnaðarhluta og viðkomandi stök þeirra eru studdar.</span><span class="sxs-lookup"><span data-stu-id="b7752-472">Allocations across cost objects dimensions and their respective members are supported.</span></span> <span data-ttu-id="b7752-473">Úthlutun pöntunarinnar er stjórnað af stýrieiningu kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="b7752-473">The allocation order is controlled by the cost control unit.</span></span> 

<span data-ttu-id="b7752-474">[![Gagnkvæm aðferð](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span><span class="sxs-lookup"><span data-stu-id="b7752-474">[![Reciprocal method](./media/reciprocal-method.png)](./media/reciprocal-method.png)</span></span>

#### <a name="define-the-cost-allocation"></a><span data-ttu-id="b7752-475">Tilgreinið kostnaðarúthlutun</span><span class="sxs-lookup"><span data-stu-id="b7752-475">Define the cost allocation</span></span>

<span data-ttu-id="b7752-476">Hér er einfalt dæmi sem útskýrir hvernig hægt er að rekja flæði kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="b7752-476">Here is a simple example that explains how you can trace the flow of cost.</span></span> <span data-ttu-id="b7752-477">Kostnaðarhlutir CC001 Mannauður leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="b7752-477">Cost object CC001 HR contributes to several cost objects.</span></span> <span data-ttu-id="b7752-478">Stofnað er tölfræðilegt víddarstak sem kallast Mannauðsþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="b7752-478">A statistical dimension member that is named HR services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7752-479">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-479">Cost object</span></span></th>
<th><span data-ttu-id="b7752-480">Mannauðsþjónusta</span><span class="sxs-lookup"><span data-stu-id="b7752-480">HR services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-481">CC002</span><span class="sxs-lookup"><span data-stu-id="b7752-481">CC002</span></span></td>
<td><span data-ttu-id="b7752-482">Fjármál</span><span class="sxs-lookup"><span data-stu-id="b7752-482">Finance</span></span></td>
<td><span data-ttu-id="b7752-483">35</span><span class="sxs-lookup"><span data-stu-id="b7752-483">35</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-484">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-484">CC003</span></span></td>
<td><span data-ttu-id="b7752-485">Smölun</span><span class="sxs-lookup"><span data-stu-id="b7752-485">Assembly</span></span></td>
<td><span data-ttu-id="b7752-486">55</span><span class="sxs-lookup"><span data-stu-id="b7752-486">55</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-487">CC004</span><span class="sxs-lookup"><span data-stu-id="b7752-487">CC004</span></span></td>
<td><span data-ttu-id="b7752-488">Pakkning</span><span class="sxs-lookup"><span data-stu-id="b7752-488">Packaging</span></span></td>
<td><span data-ttu-id="b7752-489">10</span><span class="sxs-lookup"><span data-stu-id="b7752-489">10</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7752-490">Kostnaðarhlutir CC002 Fjármál leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="b7752-490">Cost object CC002 Finance contributes to several cost objects.</span></span> <span data-ttu-id="b7752-491">Stofnað er tölfræðilegt víddarstak sem kallast Fjármálaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="b7752-491">A statistical dimension member that is named Finance services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7752-492">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-492">Cost object</span></span></th>
<th><span data-ttu-id="b7752-493">Fjármálaþjónusta</span><span class="sxs-lookup"><span data-stu-id="b7752-493">Finance services</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-494">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-494">CC003</span></span></td>
<td><span data-ttu-id="b7752-495">Smölun</span><span class="sxs-lookup"><span data-stu-id="b7752-495">Assembly</span></span></td>
<td><span data-ttu-id="b7752-496">65</span><span class="sxs-lookup"><span data-stu-id="b7752-496">65</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-497">CC004</span><span class="sxs-lookup"><span data-stu-id="b7752-497">CC004</span></span></td>
<td><span data-ttu-id="b7752-498">Pakkning</span><span class="sxs-lookup"><span data-stu-id="b7752-498">Packaging</span></span></td>
<td><span data-ttu-id="b7752-499">35</span><span class="sxs-lookup"><span data-stu-id="b7752-499">35</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7752-500">Kostnaðarhlutir CC003 Samsetning leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="b7752-500">Cost object CC003 Assembly contributes to several cost objects.</span></span> <span data-ttu-id="b7752-501">Meðlimur tölfræðilega víddar sem kallast Mannauður verk er stofnað til að mælvíddarstaka notuðum magnitude.</span><span class="sxs-lookup"><span data-stu-id="b7752-501">A statistical dimension member that is named Assembly services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7752-502">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-502">Cost object</span></span></th>
<th><span data-ttu-id="b7752-503">Samsetningarþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="b7752-503">Assembly services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-504">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-504">Prod 1</span></span></td>
<td><span data-ttu-id="b7752-505">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-505">Product 1</span></span></td>
<td><span data-ttu-id="b7752-506">60</span><span class="sxs-lookup"><span data-stu-id="b7752-506">60</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-507">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-507">Prod 2</span></span></td>
<td><span data-ttu-id="b7752-508">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-508">Product 2</span></span></td>
<td><span data-ttu-id="b7752-509">20</span><span class="sxs-lookup"><span data-stu-id="b7752-509">20</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7752-510">Kostnaðarhlutir CC004 Umbúðir leggur til nokkra kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="b7752-510">Cost object CC004 Packaging contributes to several cost objects.</span></span> <span data-ttu-id="b7752-511">Stofnað er tölfræðilegt víddarstak sem kallast Umbúðaþjónusta til að mæla notkun mæligilda.</span><span class="sxs-lookup"><span data-stu-id="b7752-511">A statistical dimension member that is named Packaging services is created to measure the consumed magnitude.</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7752-512">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-512">Cost object</span></span></th>
<th><span data-ttu-id="b7752-513">Umbúðaþjónusta (tímar)</span><span class="sxs-lookup"><span data-stu-id="b7752-513">Packaging services (hours)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-514">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-514">Prod 1</span></span></td>
<td><span data-ttu-id="b7752-515">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-515">Product 1</span></span></td>
<td><span data-ttu-id="b7752-516">80</span><span class="sxs-lookup"><span data-stu-id="b7752-516">80</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-517">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-517">Prod 2</span></span></td>
<td><span data-ttu-id="b7752-518">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-518">Product 2</span></span></td>
<td><span data-ttu-id="b7752-519">15</span><span class="sxs-lookup"><span data-stu-id="b7752-519">15</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="b7752-520">Hægt er að afleiða tölfræðiaðgerðir eins og framleiðslutíma sem vara notar frá upprunagögnum.</span><span class="sxs-lookup"><span data-stu-id="b7752-520">Statistical measures such as the production hours that a product consumes can be derived from source data.</span></span> <span data-ttu-id="b7752-521">Nánari upplýsingar er að finna í [Veitusniðmát tölfræðiaðgerðar](statistical-measure-provider-template.md#statistical-measure-provider-template).</span><span class="sxs-lookup"><span data-stu-id="b7752-521">For more information, see [Statistical measure provider template](statistical-measure-provider-template.md#statistical-measure-provider-template).</span></span> <span data-ttu-id="b7752-522">Eftirfarandi tafla sýnir niðurstöður þegar mannauðsþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="b7752-522">The following table shows the result when the HR services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7752-523">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-523">Cost object</span></span></th>
<th><span data-ttu-id="b7752-524">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="b7752-524">Magnitude</span></span></th>
<th><span data-ttu-id="b7752-525">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="b7752-525">Allocation factor</span></span></th>
<th><span data-ttu-id="b7752-526">Upphæð</span><span class="sxs-lookup"><span data-stu-id="b7752-526">Amount</span></span></th>
<th><span data-ttu-id="b7752-527">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="b7752-527">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-528">CC002</span><span class="sxs-lookup"><span data-stu-id="b7752-528">CC002</span></span></td>
<td><span data-ttu-id="b7752-529">Fjármál</span><span class="sxs-lookup"><span data-stu-id="b7752-529">Finance</span></span></td>
<td><span data-ttu-id="b7752-530">35</span><span class="sxs-lookup"><span data-stu-id="b7752-530">35</span></span></td>
<td><span data-ttu-id="b7752-531">(35 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b7752-531">(35 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b7752-532">175.00</span><span class="sxs-lookup"><span data-stu-id="b7752-532">175.00</span></span></td>
<td><span data-ttu-id="b7752-533">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-533">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-534">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-534">CC003</span></span></td>
<td><span data-ttu-id="b7752-535">Smölun</span><span class="sxs-lookup"><span data-stu-id="b7752-535">Assembly</span></span></td>
<td><span data-ttu-id="b7752-536">55</span><span class="sxs-lookup"><span data-stu-id="b7752-536">55</span></span></td>
<td><span data-ttu-id="b7752-537">(55 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b7752-537">(55 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b7752-538">275.00</span><span class="sxs-lookup"><span data-stu-id="b7752-538">275.00</span></span></td>
<td><span data-ttu-id="b7752-539">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-539">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-540">CC004</span><span class="sxs-lookup"><span data-stu-id="b7752-540">CC004</span></span></td>
<td><span data-ttu-id="b7752-541">Pakkning</span><span class="sxs-lookup"><span data-stu-id="b7752-541">Packaging</span></span></td>
<td><span data-ttu-id="b7752-542">10</span><span class="sxs-lookup"><span data-stu-id="b7752-542">10</span></span></td>
<td><span data-ttu-id="b7752-543">(10 ÷ 100) × 500,00</span><span class="sxs-lookup"><span data-stu-id="b7752-543">(10 ÷ 100) × 500.00</span></span></td>
<td><span data-ttu-id="b7752-544">50,00</span><span class="sxs-lookup"><span data-stu-id="b7752-544">50.00</span></span></td>
<td><span data-ttu-id="b7752-545">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-545">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-546">CC002</span><span class="sxs-lookup"><span data-stu-id="b7752-546">CC002</span></span></td>
<td><span data-ttu-id="b7752-547">Fjármál</span><span class="sxs-lookup"><span data-stu-id="b7752-547">Finance</span></span></td>
<td><span data-ttu-id="b7752-548">35</span><span class="sxs-lookup"><span data-stu-id="b7752-548">35</span></span></td>
<td><span data-ttu-id="b7752-549">(35 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="b7752-549">(35 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b7752-550">436.00</span><span class="sxs-lookup"><span data-stu-id="b7752-550">436.00</span></span></td>
<td><span data-ttu-id="b7752-551">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-551">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-552">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-552">CC003</span></span></td>
<td><span data-ttu-id="b7752-553">Smölun</span><span class="sxs-lookup"><span data-stu-id="b7752-553">Assembly</span></span></td>
<td><span data-ttu-id="b7752-554">55</span><span class="sxs-lookup"><span data-stu-id="b7752-554">55</span></span></td>
<td><span data-ttu-id="b7752-555">(55 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="b7752-555">(55 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b7752-556">685.14</span><span class="sxs-lookup"><span data-stu-id="b7752-556">685.14</span></span></td>
<td><span data-ttu-id="b7752-557">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-557">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-558">CC004</span><span class="sxs-lookup"><span data-stu-id="b7752-558">CC004</span></span></td>
<td><span data-ttu-id="b7752-559">Pakkning</span><span class="sxs-lookup"><span data-stu-id="b7752-559">Packaging</span></span></td>
<td><span data-ttu-id="b7752-560">10</span><span class="sxs-lookup"><span data-stu-id="b7752-560">10</span></span></td>
<td><span data-ttu-id="b7752-561">(10 ÷ 100) × 1.245,71</span><span class="sxs-lookup"><span data-stu-id="b7752-561">(10 ÷ 100) × 1,245.71</span></span></td>
<td><span data-ttu-id="b7752-562">124.57</span><span class="sxs-lookup"><span data-stu-id="b7752-562">124.57</span></span></td>
<td><span data-ttu-id="b7752-563">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-563">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7752-564">Eftirfarandi tafla sýnir niðurstöður þegar Fjármálaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="b7752-564">The following table shows the result when the Finance services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7752-565">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-565">Cost object</span></span></th>
<th><span data-ttu-id="b7752-566">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="b7752-566">Magnitude</span></span></th>
<th><span data-ttu-id="b7752-567">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="b7752-567">Allocation factor</span></span></th>
<th><span data-ttu-id="b7752-568">Upphæð</span><span class="sxs-lookup"><span data-stu-id="b7752-568">Amount</span></span></th>
<th><span data-ttu-id="b7752-569">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="b7752-569">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-570">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-570">CC003</span></span></td>
<td><span data-ttu-id="b7752-571">Smölun</span><span class="sxs-lookup"><span data-stu-id="b7752-571">Assembly</span></span></td>
<td><span data-ttu-id="b7752-572">65</span><span class="sxs-lookup"><span data-stu-id="b7752-572">65</span></span></td>
<td><span data-ttu-id="b7752-573">(65 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="b7752-573">(65 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="b7752-574">438.75</span><span class="sxs-lookup"><span data-stu-id="b7752-574">438.75</span></span></td>
<td><span data-ttu-id="b7752-575">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-575">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-576">CC004</span><span class="sxs-lookup"><span data-stu-id="b7752-576">CC004</span></span></td>
<td><span data-ttu-id="b7752-577">Pakkning</span><span class="sxs-lookup"><span data-stu-id="b7752-577">Packaging</span></span></td>
<td><span data-ttu-id="b7752-578">35</span><span class="sxs-lookup"><span data-stu-id="b7752-578">35</span></span></td>
<td><span data-ttu-id="b7752-579">(35 ÷ 100) × (500,00 + 175,00)</span><span class="sxs-lookup"><span data-stu-id="b7752-579">(35 ÷ 100) × (500.00 + 175.00)</span></span></td>
<td><span data-ttu-id="b7752-580">236.25</span><span class="sxs-lookup"><span data-stu-id="b7752-580">236.25</span></span></td>
<td><span data-ttu-id="b7752-581">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-581">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-582">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-582">CC003</span></span></td>
<td><span data-ttu-id="b7752-583">Smölun</span><span class="sxs-lookup"><span data-stu-id="b7752-583">Assembly</span></span></td>
<td><span data-ttu-id="b7752-584">65</span><span class="sxs-lookup"><span data-stu-id="b7752-584">65</span></span></td>
<td><span data-ttu-id="b7752-585">(65 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="b7752-585">(65 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="b7752-586">5,297.69</span><span class="sxs-lookup"><span data-stu-id="b7752-586">5,297.69</span></span></td>
<td><span data-ttu-id="b7752-587">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-587">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-588">CC004</span><span class="sxs-lookup"><span data-stu-id="b7752-588">CC004</span></span></td>
<td><span data-ttu-id="b7752-589">Pakkning</span><span class="sxs-lookup"><span data-stu-id="b7752-589">Packaging</span></span></td>
<td><span data-ttu-id="b7752-590">35</span><span class="sxs-lookup"><span data-stu-id="b7752-590">35</span></span></td>
<td><span data-ttu-id="b7752-591">(35 ÷ 100) × (7.714,29 + 436,00)</span><span class="sxs-lookup"><span data-stu-id="b7752-591">(35 ÷ 100) × (7,714.29 + 436.00)</span></span></td>
<td><span data-ttu-id="b7752-592">2,852.60</span><span class="sxs-lookup"><span data-stu-id="b7752-592">2,852.60</span></span></td>
<td><span data-ttu-id="b7752-593">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-593">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7752-594">Eftirfarandi tafla sýnir niðurstöður þegar Samsetningarþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="b7752-594">The following table shows the result when the Assembly services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7752-595">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-595">Cost object</span></span></th>
<th><span data-ttu-id="b7752-596">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="b7752-596">Magnitude</span></span></th>
<th><span data-ttu-id="b7752-597">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="b7752-597">Allocation factor</span></span></th>
<th><span data-ttu-id="b7752-598">Upphæð</span><span class="sxs-lookup"><span data-stu-id="b7752-598">Amount</span></span></th>
<th><span data-ttu-id="b7752-599">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="b7752-599">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-600">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-600">Prod 1</span></span></td>
<td><span data-ttu-id="b7752-601">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-601">Product 1</span></span></td>
<td><span data-ttu-id="b7752-602">60</span><span class="sxs-lookup"><span data-stu-id="b7752-602">60</span></span></td>
<td><span data-ttu-id="b7752-603">(60 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="b7752-603">(60 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="b7752-604">535.31</span><span class="sxs-lookup"><span data-stu-id="b7752-604">535.31</span></span></td>
<td><span data-ttu-id="b7752-605">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-605">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-606">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-606">Prod 2</span></span></td>
<td><span data-ttu-id="b7752-607">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-607">Product 2</span></span></td>
<td><span data-ttu-id="b7752-608">20</span><span class="sxs-lookup"><span data-stu-id="b7752-608">20</span></span></td>
<td><span data-ttu-id="b7752-609">(20 ÷ 80) × (275,00 + 438,75)</span><span class="sxs-lookup"><span data-stu-id="b7752-609">(20 ÷ 80) × (275.00 + 438.75)</span></span></td>
<td><span data-ttu-id="b7752-610">178.44</span><span class="sxs-lookup"><span data-stu-id="b7752-610">178.44</span></span></td>
<td><span data-ttu-id="b7752-611">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-611">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-612">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-612">Prod 1</span></span></td>
<td><span data-ttu-id="b7752-613">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-613">Product 1</span></span></td>
<td><span data-ttu-id="b7752-614">60</span><span class="sxs-lookup"><span data-stu-id="b7752-614">60</span></span></td>
<td><span data-ttu-id="b7752-615">(60 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="b7752-615">(60 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="b7752-616">4,487.12</span><span class="sxs-lookup"><span data-stu-id="b7752-616">4,487.12</span></span></td>
<td><span data-ttu-id="b7752-617">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-617">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-618">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-618">Prod 2</span></span></td>
<td><span data-ttu-id="b7752-619">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-619">Product 2</span></span></td>
<td><span data-ttu-id="b7752-620">20</span><span class="sxs-lookup"><span data-stu-id="b7752-620">20</span></span></td>
<td><span data-ttu-id="b7752-621">(20 ÷ 80) × (5.297,69 + 685,14)</span><span class="sxs-lookup"><span data-stu-id="b7752-621">(20 ÷ 80) × (5,297.69 + 685.14)</span></span></td>
<td><span data-ttu-id="b7752-622">1,495.71</span><span class="sxs-lookup"><span data-stu-id="b7752-622">1,495.71</span></span></td>
<td><span data-ttu-id="b7752-623">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-623">Variable cost</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b7752-624">Eftirfarandi tafla sýnir niðurstöður þegar Umbúðaþjónusta er notuð sem úthlutunargrunnur fyrir heildarkostnað (fastan kostnað og breytilegan kostnað).</span><span class="sxs-lookup"><span data-stu-id="b7752-624">The following table shows the result when the Packaging services are applied as an allocation base for total cost (fixed cost and variable cost).</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7752-625">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-625">Cost object</span></span></th>
<th><span data-ttu-id="b7752-626">Mæligildi</span><span class="sxs-lookup"><span data-stu-id="b7752-626">Magnitude</span></span></th>
<th><span data-ttu-id="b7752-627">Úthlutunarþáttur</span><span class="sxs-lookup"><span data-stu-id="b7752-627">Allocation factor</span></span></th>
<th><span data-ttu-id="b7752-628">Upphæð</span><span class="sxs-lookup"><span data-stu-id="b7752-628">Amount</span></span></th>
<th><span data-ttu-id="b7752-629">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="b7752-629">Cost behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-630">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-630">Prod 1</span></span></td>
<td><span data-ttu-id="b7752-631">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-631">Product 1</span></span></td>
<td><span data-ttu-id="b7752-632">80</span><span class="sxs-lookup"><span data-stu-id="b7752-632">80</span></span></td>
<td><span data-ttu-id="b7752-633">(80 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="b7752-633">(80 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="b7752-634">241.05</span><span class="sxs-lookup"><span data-stu-id="b7752-634">241.05</span></span></td>
<td><span data-ttu-id="b7752-635">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-635">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-636">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-636">Prod 2</span></span></td>
<td><span data-ttu-id="b7752-637">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-637">Product 2</span></span></td>
<td><span data-ttu-id="b7752-638">15</span><span class="sxs-lookup"><span data-stu-id="b7752-638">15</span></span></td>
<td><span data-ttu-id="b7752-639">(15 ÷ 95) × (50,00 + 236,25)</span><span class="sxs-lookup"><span data-stu-id="b7752-639">(15 ÷ 95) × (50.00 + 236.25)</span></span></td>
<td><span data-ttu-id="b7752-640">45.20</span><span class="sxs-lookup"><span data-stu-id="b7752-640">45.20</span></span></td>
<td><span data-ttu-id="b7752-641">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-641">Fixed cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-642">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-642">Prod 1</span></span></td>
<td><span data-ttu-id="b7752-643">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-643">Product 1</span></span></td>
<td><span data-ttu-id="b7752-644">80</span><span class="sxs-lookup"><span data-stu-id="b7752-644">80</span></span></td>
<td><span data-ttu-id="b7752-645">(80 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="b7752-645">(80 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="b7752-646">2,507.09</span><span class="sxs-lookup"><span data-stu-id="b7752-646">2,507.09</span></span></td>
<td><span data-ttu-id="b7752-647">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-647">Variable cost</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-648">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-648">Prod 2</span></span></td>
<td><span data-ttu-id="b7752-649">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-649">Product 2</span></span></td>
<td><span data-ttu-id="b7752-650">15</span><span class="sxs-lookup"><span data-stu-id="b7752-650">15</span></span></td>
<td><span data-ttu-id="b7752-651">(15 ÷ 95) × (2.852,60 + 124,57)</span><span class="sxs-lookup"><span data-stu-id="b7752-651">(15 ÷ 95) × (2,852.60 + 124.57)</span></span></td>
<td><span data-ttu-id="b7752-652">470.08</span><span class="sxs-lookup"><span data-stu-id="b7752-652">470.08</span></span></td>
<td><span data-ttu-id="b7752-653">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-653">Variable cost</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-entries-cost-object-balance-journal-entries"></a><span data-ttu-id="b7752-654">Færslubókarfærslur (Færslubókarfærslur stöðu kostnaðarhlutar)</span><span class="sxs-lookup"><span data-stu-id="b7752-654">Journal entries (cost object balance journal entries)</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b7752-655">Færslubók</span><span class="sxs-lookup"><span data-stu-id="b7752-655">Journal</span></span></th>
<th><span data-ttu-id="b7752-656">Færslubókargerð</span><span class="sxs-lookup"><span data-stu-id="b7752-656">Journal type</span></span></th>
<th colspan="3"><span data-ttu-id="b7752-657">Fjárhagsdagatalstímabil</span><span class="sxs-lookup"><span data-stu-id="b7752-657">Fiscal calendar period</span></span></th>
<th><span data-ttu-id="b7752-658">Útgáfa</span><span class="sxs-lookup"><span data-stu-id="b7752-658">Version</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-659">00004</span><span class="sxs-lookup"><span data-stu-id="b7752-659">00004</span></span></td>
<td><span data-ttu-id="b7752-660">Færslubók kostnaðarúthlutunar</span><span class="sxs-lookup"><span data-stu-id="b7752-660">Cost allocation journal</span></span></td>
<td><span data-ttu-id="b7752-661">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="b7752-661">Fiscal</span></span></td>
<td><span data-ttu-id="b7752-662">2017</span><span class="sxs-lookup"><span data-stu-id="b7752-662">2017</span></span></td>
<td><span data-ttu-id="b7752-663">1. tímabil</span><span class="sxs-lookup"><span data-stu-id="b7752-663">Period 1</span></span></td>
<td><span data-ttu-id="b7752-664">Útreikningur fastakostnaðar / 01-02-2017 11:51:00 PM / Fjárhagur /2017 / Tímabil 1</span><span class="sxs-lookup"><span data-stu-id="b7752-664">Overhead calculation / 01-02-2017 11:51:00 PM / Ledger /2017 / Period 1</span></span></td>
</tr>
</tbody>
</table>

##### <a name="journal-lines"></a><span data-ttu-id="b7752-665">Færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="b7752-665">Journal lines</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="b7752-666">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="b7752-666">Accounting date</span></span></th>
<th colspan="2"><span data-ttu-id="b7752-667">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-667">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b7752-668">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="b7752-668">Cost element</span></span></th>
<th><span data-ttu-id="b7752-669">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="b7752-669">Cost behavior</span></span></th>
<th><span data-ttu-id="b7752-670">Upphæð</span><span class="sxs-lookup"><span data-stu-id="b7752-670">Amount</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-671">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-671">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7752-672">CC001</span><span class="sxs-lookup"><span data-stu-id="b7752-672">CC001</span></span></td>
<td><span data-ttu-id="b7752-673">Mannauður</span><span class="sxs-lookup"><span data-stu-id="b7752-673">HR</span></span></td>
<td><span data-ttu-id="b7752-674">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-674">10001</span></span></td>
<td><span data-ttu-id="b7752-675">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-675">Electricity</span></span></td>
<td><span data-ttu-id="b7752-676">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-676">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-677">500,00</span><span class="sxs-lookup"><span data-stu-id="b7752-677">500.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-678">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-678">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7752-679">CC001</span><span class="sxs-lookup"><span data-stu-id="b7752-679">CC001</span></span></td>
<td><span data-ttu-id="b7752-680">Mannauður</span><span class="sxs-lookup"><span data-stu-id="b7752-680">HR</span></span></td>
<td><span data-ttu-id="b7752-681">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-681">10001</span></span></td>
<td><span data-ttu-id="b7752-682">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-682">Electricity</span></span></td>
<td><span data-ttu-id="b7752-683">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-683">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-684">1,245.71</span><span class="sxs-lookup"><span data-stu-id="b7752-684">1,245.71</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-685">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-685">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7752-686">CC002</span><span class="sxs-lookup"><span data-stu-id="b7752-686">CC002</span></span></td>
<td><span data-ttu-id="b7752-687">Fjármál</span><span class="sxs-lookup"><span data-stu-id="b7752-687">Finance</span></span></td>
<td><span data-ttu-id="b7752-688">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-688">10001</span></span></td>
<td><span data-ttu-id="b7752-689">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-689">Electricity</span></span></td>
<td><span data-ttu-id="b7752-690">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-690">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-691">675.00</span><span class="sxs-lookup"><span data-stu-id="b7752-691">675.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-692">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-692">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7752-693">CC002</span><span class="sxs-lookup"><span data-stu-id="b7752-693">CC002</span></span></td>
<td><span data-ttu-id="b7752-694">Fjármál</span><span class="sxs-lookup"><span data-stu-id="b7752-694">Finance</span></span></td>
<td><span data-ttu-id="b7752-695">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-695">10001</span></span></td>
<td><span data-ttu-id="b7752-696">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-696">Electricity</span></span></td>
<td><span data-ttu-id="b7752-697">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-697">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-698">8,150.29</span><span class="sxs-lookup"><span data-stu-id="b7752-698">8,150.29</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-699">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-699">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7752-700">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-700">CC003</span></span></td>
<td><span data-ttu-id="b7752-701">Smölun</span><span class="sxs-lookup"><span data-stu-id="b7752-701">Assembly</span></span></td>
<td><span data-ttu-id="b7752-702">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-702">10001</span></span></td>
<td><span data-ttu-id="b7752-703">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-703">Electricity</span></span></td>
<td><span data-ttu-id="b7752-704">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-704">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-705">713.75</span><span class="sxs-lookup"><span data-stu-id="b7752-705">713.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-706">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-706">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7752-707">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-707">CC003</span></span></td>
<td><span data-ttu-id="b7752-708">Smölun</span><span class="sxs-lookup"><span data-stu-id="b7752-708">Assembly</span></span></td>
<td><span data-ttu-id="b7752-709">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-709">10001</span></span></td>
<td><span data-ttu-id="b7752-710">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-710">Electricity</span></span></td>
<td><span data-ttu-id="b7752-711">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-711">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-712">5,982.83</span><span class="sxs-lookup"><span data-stu-id="b7752-712">5,982.83</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-713">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-713">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7752-714">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-714">CC003</span></span></td>
<td><span data-ttu-id="b7752-715">Pakkning</span><span class="sxs-lookup"><span data-stu-id="b7752-715">Packaging</span></span></td>
<td><span data-ttu-id="b7752-716">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-716">10001</span></span></td>
<td><span data-ttu-id="b7752-717">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-717">Electricity</span></span></td>
<td><span data-ttu-id="b7752-718">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-718">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-719">286.25</span><span class="sxs-lookup"><span data-stu-id="b7752-719">286.25</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-720">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-720">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7752-721">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-721">CC003</span></span></td>
<td><span data-ttu-id="b7752-722">Pakkning</span><span class="sxs-lookup"><span data-stu-id="b7752-722">Packaging</span></span></td>
<td><span data-ttu-id="b7752-723">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-723">10001</span></span></td>
<td><span data-ttu-id="b7752-724">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-724">Electricity</span></span></td>
<td><span data-ttu-id="b7752-725">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-725">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-726">2,977.17</span><span class="sxs-lookup"><span data-stu-id="b7752-726">2,977.17</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-727">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-727">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7752-728">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-728">Prod 1</span></span></td>
<td><span data-ttu-id="b7752-729">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-729">Product 1</span></span></td>
<td><span data-ttu-id="b7752-730">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-730">10001</span></span></td>
<td><span data-ttu-id="b7752-731">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-731">Electricity</span></span></td>
<td><span data-ttu-id="b7752-732">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-732">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-733">776.36</span><span class="sxs-lookup"><span data-stu-id="b7752-733">776.36</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-734">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-734">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7752-735">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-735">Prod 1</span></span></td>
<td><span data-ttu-id="b7752-736">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-736">Product 1</span></span></td>
<td><span data-ttu-id="b7752-737">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-737">10001</span></span></td>
<td><span data-ttu-id="b7752-738">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-738">Electricity</span></span></td>
<td><span data-ttu-id="b7752-739">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-739">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-740">6,994.21</span><span class="sxs-lookup"><span data-stu-id="b7752-740">6,994.21</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-741">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-741">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7752-742">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-742">Prod 2</span></span></td>
<td><span data-ttu-id="b7752-743">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-743">Product 1</span></span></td>
<td><span data-ttu-id="b7752-744">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-744">10001</span></span></td>
<td><span data-ttu-id="b7752-745">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-745">Electricity</span></span></td>
<td><span data-ttu-id="b7752-746">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-746">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-747">223.64</span><span class="sxs-lookup"><span data-stu-id="b7752-747">223.64</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-748">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-748">January 31, 2017</span></span></td>
<td><span data-ttu-id="b7752-749">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-749">Prod 2</span></span></td>
<td><span data-ttu-id="b7752-750">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-750">Product 1</span></span></td>
<td><span data-ttu-id="b7752-751">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-751">10001</span></span></td>
<td><span data-ttu-id="b7752-752">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-752">Electricity</span></span></td>
<td><span data-ttu-id="b7752-753">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-753">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-754">1,965.79</span><span class="sxs-lookup"><span data-stu-id="b7752-754">1,965.79</span></span></td>
</tr>
</tbody>
</table>

##### <a name="cost-entries"></a><span data-ttu-id="b7752-755">Kostnaðarfærslur</span><span class="sxs-lookup"><span data-stu-id="b7752-755">Cost entries</span></span>

<table>
<thead>
<tr>
<th colspan="2"><span data-ttu-id="b7752-756">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-756">Cost object</span></span></th>
<th colspan="2"><span data-ttu-id="b7752-757">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="b7752-757">Cost element</span></span></th>
<th><span data-ttu-id="b7752-758">Kostnaðarhegðun</span><span class="sxs-lookup"><span data-stu-id="b7752-758">Cost behavior</span></span></th>
<th><span data-ttu-id="b7752-759">Upphæð</span><span class="sxs-lookup"><span data-stu-id="b7752-759">Amount</span></span></th>
<th><span data-ttu-id="b7752-760">Dagsetning reikningsskila</span><span class="sxs-lookup"><span data-stu-id="b7752-760">Accounting date</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b7752-761">CC001</span><span class="sxs-lookup"><span data-stu-id="b7752-761">CC001</span></span></td>
<td><span data-ttu-id="b7752-762">Mannauður</span><span class="sxs-lookup"><span data-stu-id="b7752-762">HR</span></span></td>
<td><span data-ttu-id="b7752-763">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-763">10001</span></span></td>
<td><span data-ttu-id="b7752-764">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-764">Electricity</span></span></td>
<td><span data-ttu-id="b7752-765">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-765">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-766">-500,00</span><span class="sxs-lookup"><span data-stu-id="b7752-766">-500.00</span></span></td>
<td><span data-ttu-id="b7752-767">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-767">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-768">CC002</span><span class="sxs-lookup"><span data-stu-id="b7752-768">CC002</span></span></td>
<td><span data-ttu-id="b7752-769">Fjármál</span><span class="sxs-lookup"><span data-stu-id="b7752-769">Finance</span></span></td>
<td><span data-ttu-id="b7752-770">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-770">10001</span></span></td>
<td><span data-ttu-id="b7752-771">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-771">Electricity</span></span></td>
<td><span data-ttu-id="b7752-772">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-772">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-773">175.00</span><span class="sxs-lookup"><span data-stu-id="b7752-773">175.00</span></span></td>
<td><span data-ttu-id="b7752-774">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-774">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-775">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-775">CC003</span></span></td>
<td><span data-ttu-id="b7752-776">Smölun</span><span class="sxs-lookup"><span data-stu-id="b7752-776">Assembly</span></span></td>
<td><span data-ttu-id="b7752-777">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-777">10001</span></span></td>
<td><span data-ttu-id="b7752-778">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-778">Electricity</span></span></td>
<td><span data-ttu-id="b7752-779">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-779">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-780">275.00</span><span class="sxs-lookup"><span data-stu-id="b7752-780">275.00</span></span></td>
<td><span data-ttu-id="b7752-781">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-781">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-782">CC004</span><span class="sxs-lookup"><span data-stu-id="b7752-782">CC004</span></span></td>
<td><span data-ttu-id="b7752-783">Pakkning</span><span class="sxs-lookup"><span data-stu-id="b7752-783">Packaging</span></span></td>
<td><span data-ttu-id="b7752-784">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-784">10001</span></span></td>
<td><span data-ttu-id="b7752-785">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-785">Electricity</span></span></td>
<td><span data-ttu-id="b7752-786">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-786">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-787">50,00</span><span class="sxs-lookup"><span data-stu-id="b7752-787">50,00</span></span></td>
<td><span data-ttu-id="b7752-788">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-788">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-789">CC001</span><span class="sxs-lookup"><span data-stu-id="b7752-789">CC001</span></span></td>
<td><span data-ttu-id="b7752-790">Mannauður</span><span class="sxs-lookup"><span data-stu-id="b7752-790">HR</span></span></td>
<td><span data-ttu-id="b7752-791">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-791">10001</span></span></td>
<td><span data-ttu-id="b7752-792">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-792">Electricity</span></span></td>
<td><span data-ttu-id="b7752-793">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-793">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-794">-1.245,71</span><span class="sxs-lookup"><span data-stu-id="b7752-794">-1,245.71</span></span></td>
<td><span data-ttu-id="b7752-795">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-795">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-796">CC002</span><span class="sxs-lookup"><span data-stu-id="b7752-796">CC002</span></span></td>
<td><span data-ttu-id="b7752-797">Fjármál</span><span class="sxs-lookup"><span data-stu-id="b7752-797">Finance</span></span></td>
<td><span data-ttu-id="b7752-798">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-798">10001</span></span></td>
<td><span data-ttu-id="b7752-799">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-799">Electricity</span></span></td>
<td><span data-ttu-id="b7752-800">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-800">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-801">436.00</span><span class="sxs-lookup"><span data-stu-id="b7752-801">436.00</span></span></td>
<td><span data-ttu-id="b7752-802">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-802">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-803">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-803">CC003</span></span></td>
<td><span data-ttu-id="b7752-804">Smölun</span><span class="sxs-lookup"><span data-stu-id="b7752-804">Assembly</span></span></td>
<td><span data-ttu-id="b7752-805">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-805">10001</span></span></td>
<td><span data-ttu-id="b7752-806">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-806">Electricity</span></span></td>
<td><span data-ttu-id="b7752-807">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-807">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-808">685.14</span><span class="sxs-lookup"><span data-stu-id="b7752-808">685.14</span></span></td>
<td><span data-ttu-id="b7752-809">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-809">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-810">CC004</span><span class="sxs-lookup"><span data-stu-id="b7752-810">CC004</span></span></td>
<td><span data-ttu-id="b7752-811">Pakkning</span><span class="sxs-lookup"><span data-stu-id="b7752-811">Packaging</span></span></td>
<td><span data-ttu-id="b7752-812">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-812">10001</span></span></td>
<td><span data-ttu-id="b7752-813">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-813">Electricity</span></span></td>
<td><span data-ttu-id="b7752-814">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-814">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-815">124.57</span><span class="sxs-lookup"><span data-stu-id="b7752-815">124.57</span></span></td>
<td><span data-ttu-id="b7752-816">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-816">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-817">CC002</span><span class="sxs-lookup"><span data-stu-id="b7752-817">CC002</span></span></td>
<td><span data-ttu-id="b7752-818">Fjármál</span><span class="sxs-lookup"><span data-stu-id="b7752-818">Finance</span></span></td>
<td><span data-ttu-id="b7752-819">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-819">10001</span></span></td>
<td><span data-ttu-id="b7752-820">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-820">Electricity</span></span></td>
<td><span data-ttu-id="b7752-821">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-821">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-822">-675,00</span><span class="sxs-lookup"><span data-stu-id="b7752-822">-675.00</span></span></td>
<td><span data-ttu-id="b7752-823">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-823">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-824">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-824">CC003</span></span></td>
<td><span data-ttu-id="b7752-825">Smölun</span><span class="sxs-lookup"><span data-stu-id="b7752-825">Assembly</span></span></td>
<td><span data-ttu-id="b7752-826">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-826">10001</span></span></td>
<td><span data-ttu-id="b7752-827">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-827">Electricity</span></span></td>
<td><span data-ttu-id="b7752-828">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-828">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-829">438.75</span><span class="sxs-lookup"><span data-stu-id="b7752-829">438.75</span></span></td>
<td><span data-ttu-id="b7752-830">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-830">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-831">CC004</span><span class="sxs-lookup"><span data-stu-id="b7752-831">CC004</span></span></td>
<td><span data-ttu-id="b7752-832">Pakkning</span><span class="sxs-lookup"><span data-stu-id="b7752-832">Packaging</span></span></td>
<td><span data-ttu-id="b7752-833">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-833">10001</span></span></td>
<td><span data-ttu-id="b7752-834">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-834">Electricity</span></span></td>
<td><span data-ttu-id="b7752-835">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-835">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-836">236.25</span><span class="sxs-lookup"><span data-stu-id="b7752-836">236.25</span></span></td>
<td><span data-ttu-id="b7752-837">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-837">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-838">CC002</span><span class="sxs-lookup"><span data-stu-id="b7752-838">CC002</span></span></td>
<td><span data-ttu-id="b7752-839">Fjármál</span><span class="sxs-lookup"><span data-stu-id="b7752-839">Finance</span></span></td>
<td><span data-ttu-id="b7752-840">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-840">10001</span></span></td>
<td><span data-ttu-id="b7752-841">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-841">Electricity</span></span></td>
<td><span data-ttu-id="b7752-842">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-842">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-843">-8.150,29</span><span class="sxs-lookup"><span data-stu-id="b7752-843">-8,150.29</span></span></td>
<td><span data-ttu-id="b7752-844">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-844">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-845">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-845">CC003</span></span></td>
<td><span data-ttu-id="b7752-846">Smölun</span><span class="sxs-lookup"><span data-stu-id="b7752-846">Assembly</span></span></td>
<td><span data-ttu-id="b7752-847">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-847">10001</span></span></td>
<td><span data-ttu-id="b7752-848">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-848">Electricity</span></span></td>
<td><span data-ttu-id="b7752-849">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-849">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-850">5,297.69</span><span class="sxs-lookup"><span data-stu-id="b7752-850">5,297.69</span></span></td>
<td><span data-ttu-id="b7752-851">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-851">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-852">CC004</span><span class="sxs-lookup"><span data-stu-id="b7752-852">CC004</span></span></td>
<td><span data-ttu-id="b7752-853">Pakkning</span><span class="sxs-lookup"><span data-stu-id="b7752-853">Packaging</span></span></td>
<td><span data-ttu-id="b7752-854">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-854">10001</span></span></td>
<td><span data-ttu-id="b7752-855">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-855">Electricity</span></span></td>
<td><span data-ttu-id="b7752-856">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-856">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-857">2,852.60</span><span class="sxs-lookup"><span data-stu-id="b7752-857">2,852.60</span></span></td>
<td><span data-ttu-id="b7752-858">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-858">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-859">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-859">CC003</span></span></td>
<td><span data-ttu-id="b7752-860">Smölun</span><span class="sxs-lookup"><span data-stu-id="b7752-860">Assembly</span></span></td>
<td><span data-ttu-id="b7752-861">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-861">10001</span></span></td>
<td><span data-ttu-id="b7752-862">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-862">Electricity</span></span></td>
<td><span data-ttu-id="b7752-863">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-863">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-864">-713,75</span><span class="sxs-lookup"><span data-stu-id="b7752-864">-713.75</span></span></td>
<td><span data-ttu-id="b7752-865">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-865">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-866">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-866">Prod 1</span></span></td>
<td><span data-ttu-id="b7752-867">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-867">Product 1</span></span></td>
<td><span data-ttu-id="b7752-868">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-868">10001</span></span></td>
<td><span data-ttu-id="b7752-869">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-869">Electricity</span></span></td>
<td><span data-ttu-id="b7752-870">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-870">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-871">535.31</span><span class="sxs-lookup"><span data-stu-id="b7752-871">535.31</span></span></td>
<td><span data-ttu-id="b7752-872">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-872">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-873">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-873">Prod 2</span></span></td>
<td><span data-ttu-id="b7752-874">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-874">Product 2</span></span></td>
<td><span data-ttu-id="b7752-875">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-875">10001</span></span></td>
<td><span data-ttu-id="b7752-876">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-876">Electricity</span></span></td>
<td><span data-ttu-id="b7752-877">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-877">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-878">178.44</span><span class="sxs-lookup"><span data-stu-id="b7752-878">178.44</span></span></td>
<td><span data-ttu-id="b7752-879">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-879">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-880">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-880">CC003</span></span></td>
<td><span data-ttu-id="b7752-881">Smölun</span><span class="sxs-lookup"><span data-stu-id="b7752-881">Assembly</span></span></td>
<td><span data-ttu-id="b7752-882">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-882">10001</span></span></td>
<td><span data-ttu-id="b7752-883">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-883">Electricity</span></span></td>
<td><span data-ttu-id="b7752-884">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-884">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-885">-5.982,83</span><span class="sxs-lookup"><span data-stu-id="b7752-885">-5,982.83</span></span></td>
<td><span data-ttu-id="b7752-886">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-886">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-887">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-887">Prod 1</span></span></td>
<td><span data-ttu-id="b7752-888">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-888">Product 1</span></span></td>
<td><span data-ttu-id="b7752-889">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-889">10001</span></span></td>
<td><span data-ttu-id="b7752-890">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-890">Electricity</span></span></td>
<td><span data-ttu-id="b7752-891">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-891">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-892">4,487.12</span><span class="sxs-lookup"><span data-stu-id="b7752-892">4,487.12</span></span></td>
<td><span data-ttu-id="b7752-893">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-893">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-894">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-894">Prod 2</span></span></td>
<td><span data-ttu-id="b7752-895">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-895">Product 2</span></span></td>
<td><span data-ttu-id="b7752-896">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-896">10001</span></span></td>
<td><span data-ttu-id="b7752-897">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-897">Electricity</span></span></td>
<td><span data-ttu-id="b7752-898">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-898">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-899">1,495.71</span><span class="sxs-lookup"><span data-stu-id="b7752-899">1,495.71</span></span></td>
<td><span data-ttu-id="b7752-900">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-900">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-901">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-901">CC003</span></span></td>
<td><span data-ttu-id="b7752-902">Smölun</span><span class="sxs-lookup"><span data-stu-id="b7752-902">Assembly</span></span></td>
<td><span data-ttu-id="b7752-903">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-903">10001</span></span></td>
<td><span data-ttu-id="b7752-904">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-904">Electricity</span></span></td>
<td><span data-ttu-id="b7752-905">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-905">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-906">-286,25</span><span class="sxs-lookup"><span data-stu-id="b7752-906">-286.25</span></span></td>
<td><span data-ttu-id="b7752-907">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-907">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-908">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-908">Prod 1</span></span></td>
<td><span data-ttu-id="b7752-909">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-909">Product 1</span></span></td>
<td><span data-ttu-id="b7752-910">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-910">10001</span></span></td>
<td><span data-ttu-id="b7752-911">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-911">Electricity</span></span></td>
<td><span data-ttu-id="b7752-912">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-912">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-913">241.05</span><span class="sxs-lookup"><span data-stu-id="b7752-913">241.05</span></span></td>
<td><span data-ttu-id="b7752-914">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-914">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-915">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-915">Prod 2</span></span></td>
<td><span data-ttu-id="b7752-916">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-916">Product 2</span></span></td>
<td><span data-ttu-id="b7752-917">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-917">10001</span></span></td>
<td><span data-ttu-id="b7752-918">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-918">Electricity</span></span></td>
<td><span data-ttu-id="b7752-919">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-919">Fixed cost</span></span></td>
<td><span data-ttu-id="b7752-920">45.20</span><span class="sxs-lookup"><span data-stu-id="b7752-920">45.20</span></span></td>
<td><span data-ttu-id="b7752-921">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-921">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-922">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-922">CC003</span></span></td>
<td><span data-ttu-id="b7752-923">Smölun</span><span class="sxs-lookup"><span data-stu-id="b7752-923">Assembly</span></span></td>
<td><span data-ttu-id="b7752-924">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-924">10001</span></span></td>
<td><span data-ttu-id="b7752-925">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-925">Electricity</span></span></td>
<td><span data-ttu-id="b7752-926">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-926">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-927">-2.977,17</span><span class="sxs-lookup"><span data-stu-id="b7752-927">-2,977.17</span></span></td>
<td><span data-ttu-id="b7752-928">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-928">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-929">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-929">Prod 1</span></span></td>
<td><span data-ttu-id="b7752-930">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-930">Product 1</span></span></td>
<td><span data-ttu-id="b7752-931">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-931">10001</span></span></td>
<td><span data-ttu-id="b7752-932">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-932">Electricity</span></span></td>
<td><span data-ttu-id="b7752-933">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-933">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-934">2,507.09</span><span class="sxs-lookup"><span data-stu-id="b7752-934">2,507.09</span></span></td>
<td><span data-ttu-id="b7752-935">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-935">January 31, 2017</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b7752-936">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-936">Prod 2</span></span></td>
<td><span data-ttu-id="b7752-937">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-937">Product 2</span></span></td>
<td><span data-ttu-id="b7752-938">10001</span><span class="sxs-lookup"><span data-stu-id="b7752-938">10001</span></span></td>
<td><span data-ttu-id="b7752-939">Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-939">Electricity</span></span></td>
<td><span data-ttu-id="b7752-940">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-940">Variable cost</span></span></td>
<td><span data-ttu-id="b7752-941">470.08</span><span class="sxs-lookup"><span data-stu-id="b7752-941">470.08</span></span></td>
<td><span data-ttu-id="b7752-942">31. janúar 2017</span><span class="sxs-lookup"><span data-stu-id="b7752-942">January 31, 2017</span></span></td>
</tr>
</tbody>
</table>

## <a name="conclusion"></a><span data-ttu-id="b7752-943">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="b7752-943">Conclusion</span></span>
<span data-ttu-id="b7752-944">Í Fjárhagsbókhaldi er kostnaður upp á 10.000,00 fyrir rafmagn bókaður á kenni leppkostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="b7752-944">In Financial accounting, a cost of 10,000.00 for Electricity is posted to a dummy cost center ID.</span></span> <span data-ttu-id="b7752-945">Þar af leiðandi munu kostnaðarbókarar vita að það þarf að úthluta þessum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="b7752-945">Therefore, cost accountants will know that this cost must be allocated.</span></span> <span data-ttu-id="b7752-946">Í kostnaðarbókhaldi streymir kostnaður þvert á fyrirtækiseiningar og stig, samkvæmt þeim stefnum og reglum sem eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="b7752-946">In Cost accounting, the costs flow across organizational units and levels, based on the policies and rules that are applied.</span></span> <span data-ttu-id="b7752-947">Hver kostnaður hefur verið tengdur úthlutunargrunni sem veitir besta mat á úthlutun á kostnaði.</span><span class="sxs-lookup"><span data-stu-id="b7752-947">Each cost has been associated with an allocation base that provides the best assessment for the allocation of costs.</span></span>

<table>
<thead>
<tr>
<th colspan="2" rowspan="2"><span data-ttu-id="b7752-948">Kostnaðareining</span><span class="sxs-lookup"><span data-stu-id="b7752-948">Cost element</span></span></th>
<th colspan="9"><span data-ttu-id="b7752-949">Kostnaðarhlutur</span><span class="sxs-lookup"><span data-stu-id="b7752-949">Cost object</span></span></th>
<th rowspan="2"><span data-ttu-id="b7752-950">Samtala</span><span class="sxs-lookup"><span data-stu-id="b7752-950">Total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b7752-951">CC099</span><span class="sxs-lookup"><span data-stu-id="b7752-951">CC099</span></span></th>
<th><span data-ttu-id="b7752-952">CC001</span><span class="sxs-lookup"><span data-stu-id="b7752-952">CC001</span></span></th>
<th><span data-ttu-id="b7752-953">CC002</span><span class="sxs-lookup"><span data-stu-id="b7752-953">CC002</span></span></th>
<th><span data-ttu-id="b7752-954">CC003</span><span class="sxs-lookup"><span data-stu-id="b7752-954">CC003</span></span></th>
<th><span data-ttu-id="b7752-955">CC004</span><span class="sxs-lookup"><span data-stu-id="b7752-955">CC004</span></span></th>
<th><span data-ttu-id="b7752-956">Verk 1</span><span class="sxs-lookup"><span data-stu-id="b7752-956">Proj 1</span></span></th>
<th><span data-ttu-id="b7752-957">Verk 2</span><span class="sxs-lookup"><span data-stu-id="b7752-957">Proj 2</span></span></th>
<th><span data-ttu-id="b7752-958">Afurð 1</span><span class="sxs-lookup"><span data-stu-id="b7752-958">Prod 1</span></span></th>
<th><span data-ttu-id="b7752-959">Afurð 2</span><span class="sxs-lookup"><span data-stu-id="b7752-959">Prod 2</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="2"><span data-ttu-id="b7752-960">10001 Rafmagn</span><span class="sxs-lookup"><span data-stu-id="b7752-960">10001 Electricity</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-961"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b7752-961"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-962"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b7752-962"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-963"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b7752-963"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-964"><strong>0.00</strong></span><span class="sxs-lookup"><span data-stu-id="b7752-964"><strong>0.00</strong></span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="b7752-965"><strong>30.00</strong></span><span class="sxs-lookup"><span data-stu-id="b7752-965"><strong>30.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-966"><strong>10.00</strong></span><span class="sxs-lookup"><span data-stu-id="b7752-966"><strong>10.00</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-967"><strong>7,770.57</strong></span><span class="sxs-lookup"><span data-stu-id="b7752-967"><strong>7,770.57</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-968"><strong>2,189.43</strong></span><span class="sxs-lookup"><span data-stu-id="b7752-968"><strong>2,189.43</strong></span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-969"><strong>10,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="b7752-969"><strong>10,000.00</strong></span></span></td>
</tr>
<tr>
<td></td>
<td style="text-align: left;"><span data-ttu-id="b7752-970">Óflokkað</span><span class="sxs-lookup"><span data-stu-id="b7752-970">Unclassified</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-971">0,00</span><span class="sxs-lookup"><span data-stu-id="b7752-971">0.00</span></span></td>
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
<td style="text-align: left;"><span data-ttu-id="b7752-972">Fastur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-972">Fixed cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-973">0,00</span><span class="sxs-lookup"><span data-stu-id="b7752-973">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-974">0,00</span><span class="sxs-lookup"><span data-stu-id="b7752-974">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-975">0,00</span><span class="sxs-lookup"><span data-stu-id="b7752-975">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-976">0,00</span><span class="sxs-lookup"><span data-stu-id="b7752-976">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-977">0,00</span><span class="sxs-lookup"><span data-stu-id="b7752-977">0.00</span></span></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"></td>
<td style="text-align: right;"><span data-ttu-id="b7752-978">776.36</span><span class="sxs-lookup"><span data-stu-id="b7752-978">776.36</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-979">223.64</span><span class="sxs-lookup"><span data-stu-id="b7752-979">223.64</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-980"><strong>1,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="b7752-980"><strong>1,000.00</strong></span></span></td>
</tr>
<tr>
<td style="text-align: right;"></td>
<td style="text-align: left;"><span data-ttu-id="b7752-981">Breytilegur kostnaður</span><span class="sxs-lookup"><span data-stu-id="b7752-981">Variable cost</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-982">000</span><span class="sxs-lookup"><span data-stu-id="b7752-982">000</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-983">0,00</span><span class="sxs-lookup"><span data-stu-id="b7752-983">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-984">0,00</span><span class="sxs-lookup"><span data-stu-id="b7752-984">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-985">0,00</span><span class="sxs-lookup"><span data-stu-id="b7752-985">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-986">0,00</span><span class="sxs-lookup"><span data-stu-id="b7752-986">0.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-987">30,00</span><span class="sxs-lookup"><span data-stu-id="b7752-987">30.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-988">10,00</span><span class="sxs-lookup"><span data-stu-id="b7752-988">10.00</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-989">6,994.21</span><span class="sxs-lookup"><span data-stu-id="b7752-989">6,994.21</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-990">1,965.79</span><span class="sxs-lookup"><span data-stu-id="b7752-990">1,965.79</span></span></td>
<td style="text-align: right;"><span data-ttu-id="b7752-991"><strong>9,000.00</strong></span><span class="sxs-lookup"><span data-stu-id="b7752-991"><strong>9,000.00</strong></span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="b7752-992">Þetta efnisatriði sýnir hvernig fyrir aðalkostnaðareiningin 10001 Rafmagn flæðir í gegnum kostnaðarhluti.</span><span class="sxs-lookup"><span data-stu-id="b7752-992">This topic shows how a primary cost element, 10001 Electricity, flows through the cost objects.</span></span> <span data-ttu-id="b7752-993">Þar af leiðandi er þessum sameiginlega kostnaði úthlutað á lægsta stigið í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="b7752-993">Therefore, this overhead cost is allocated to the lowest level in the organization.</span></span> <span data-ttu-id="b7752-994">Með öðrum orðum bera kostnaðarhlutir á lægsta stiginu kostnaðinn.</span><span class="sxs-lookup"><span data-stu-id="b7752-994">In other words, the cost objects at the lowest level bear the cost.</span></span> <span data-ttu-id="b7752-995">Ef þú þarft sjónrænt flæði kostnaðar á milli kostnaðarhluta er hægt að nota stefnureglur samantekins kostnaðar til að gera kostnaðarflæðið sýnilegt.</span><span class="sxs-lookup"><span data-stu-id="b7752-995">If you require a visual flow of the cost between the cost objects, you can use the cost roll-up policy rules to visualize the flow of the cost.</span></span> <span data-ttu-id="b7752-996">Nánari upplýsingar er að finna í [Samantekt kostnaðar](cost-rollup.md).</span><span class="sxs-lookup"><span data-stu-id="b7752-996">For more information, see [Cost roll-up](cost-rollup.md).</span></span>



