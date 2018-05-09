---
title: "Endurmat á gjaldmiðli í samstæðufyrirtæki"
description: "Þetta efnisatriði lýsir því hvernig á að endurmeta gjaldmiðil í samstæðufyrirtæki."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 2368021864668c2721976e820c74263137c1ee00
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="08838-103">Endurmat á gjaldmiðli í samstæðufyrirtæki</span><span class="sxs-lookup"><span data-stu-id="08838-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08838-104">Þegar gögn frá einum bókhaldsgjaldmiðill til annars eru sameinuð, verður samt að keyra gjaldmiðilsendurmatið ef breyting á gjaldmiðla verður , þannig að lykilsstöður þínar séu rétt endurmetnar.</span><span class="sxs-lookup"><span data-stu-id="08838-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="08838-105">Þegar gögnum eru sameinuð í upphafi, nota á **umreikningur Gjaldmiðils** flipa til að velja fyrstu gengi fyrir þýðingu á meðan á sameiningarferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="08838-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="08838-106">Eftir að nýtt gengi er fært inn (til dæmis í næsta mánuð), verður að endurmeta stöðu lykils.</span><span class="sxs-lookup"><span data-stu-id="08838-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="08838-107">Óinnleystur hagnaður eða tap er síðan uppfærð til samræmis, byggt á nýju gengi og dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="08838-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="08838-108">Eftirfarandi dæmi sýnir bókhaldsfærslur sem eru stofnaðar á meðan vinnslu stendur.</span><span class="sxs-lookup"><span data-stu-id="08838-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="08838-109">Uppsetning fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="08838-109">Company setup</span></span>
-   <span data-ttu-id="08838-110">**Uppruna/rekstrar fyrirtæki (USMF)** – Bandarískum dollurum (USD) eru notaðar sem á bókhalds og skýrslugjaldmiðill.</span><span class="sxs-lookup"><span data-stu-id="08838-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="08838-111">**Sameinað fyrirtæki (CON)** – Evrur (EUR) eru notaðar sem á bókhalds og skýrslugjaldmiðill.</span><span class="sxs-lookup"><span data-stu-id="08838-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="08838-112">**Óinnleystur hagnaður**– Fjárhagslykil 801500</span><span class="sxs-lookup"><span data-stu-id="08838-112">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="08838-113">**Innleystur tap**– fjárhagslykill 801600</span><span class="sxs-lookup"><span data-stu-id="08838-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="08838-114">**Óinnleystur hagnaður**– fjárhagslykill 801600</span><span class="sxs-lookup"><span data-stu-id="08838-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="08838-115">**Óinnleyst tap**– fjárhagslykill 801400</span><span class="sxs-lookup"><span data-stu-id="08838-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="08838-116">Upphaflegar færslur</span><span class="sxs-lookup"><span data-stu-id="08838-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="08838-117">innhreyfingarfærslur Reiðufés í USMF</span><span class="sxs-lookup"><span data-stu-id="08838-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="08838-118">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="08838-118">Date</span></span>       | <span data-ttu-id="08838-119">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="08838-119">Ledger account</span></span>               | <span data-ttu-id="08838-120">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="08838-120">Currency</span></span> | <span data-ttu-id="08838-121">Upphæð</span><span class="sxs-lookup"><span data-stu-id="08838-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="08838-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="08838-122">10/11/2015</span></span> | <span data-ttu-id="08838-123">110110 – Reiðufé</span><span class="sxs-lookup"><span data-stu-id="08838-123">110110 – Cash</span></span>                | <span data-ttu-id="08838-124">USD</span><span class="sxs-lookup"><span data-stu-id="08838-124">USD</span></span>      | <span data-ttu-id="08838-125">500</span><span class="sxs-lookup"><span data-stu-id="08838-125">500</span></span>    |
| <span data-ttu-id="08838-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="08838-126">10/11/2015</span></span> | <span data-ttu-id="08838-127">130100 – Viðskiptakröfur</span><span class="sxs-lookup"><span data-stu-id="08838-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="08838-128">USD</span><span class="sxs-lookup"><span data-stu-id="08838-128">USD</span></span>      | <span data-ttu-id="08838-129">-500</span><span class="sxs-lookup"><span data-stu-id="08838-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="08838-130">Gengi gjaldmiðla</span><span class="sxs-lookup"><span data-stu-id="08838-130">Exchange rates</span></span>

| <span data-ttu-id="08838-131">Úr gjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="08838-131">From currency</span></span> | <span data-ttu-id="08838-132">Í gjaldmiðil</span><span class="sxs-lookup"><span data-stu-id="08838-132">To currency</span></span> | <span data-ttu-id="08838-133">Upphafsdagsetning</span><span class="sxs-lookup"><span data-stu-id="08838-133">Start date</span></span> | <span data-ttu-id="08838-134">Gengi</span><span class="sxs-lookup"><span data-stu-id="08838-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="08838-135">EUR</span><span class="sxs-lookup"><span data-stu-id="08838-135">EUR</span></span>           | <span data-ttu-id="08838-136">USD</span><span class="sxs-lookup"><span data-stu-id="08838-136">USD</span></span>         | <span data-ttu-id="08838-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="08838-137">10/1/2015</span></span>  | <span data-ttu-id="08838-138">200</span><span class="sxs-lookup"><span data-stu-id="08838-138">200</span></span>           |
| <span data-ttu-id="08838-139">EUR</span><span class="sxs-lookup"><span data-stu-id="08838-139">EUR</span></span>           | <span data-ttu-id="08838-140">USD</span><span class="sxs-lookup"><span data-stu-id="08838-140">USD</span></span>         | <span data-ttu-id="08838-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="08838-141">11/1/2015</span></span>  | <span data-ttu-id="08838-142">150</span><span class="sxs-lookup"><span data-stu-id="08838-142">150</span></span>           |
| <span data-ttu-id="08838-143">EUR</span><span class="sxs-lookup"><span data-stu-id="08838-143">EUR</span></span>           | <span data-ttu-id="08838-144">USD</span><span class="sxs-lookup"><span data-stu-id="08838-144">USD</span></span>         | <span data-ttu-id="08838-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="08838-145">12/1/2012</span></span>  | <span data-ttu-id="08838-146">100</span><span class="sxs-lookup"><span data-stu-id="08838-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="08838-147">Framkvæma sameiningu fyrir Október 2015</span><span class="sxs-lookup"><span data-stu-id="08838-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="08838-148">Stöður í samstæðufyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="08838-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="08838-149">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="08838-149">Ledger account</span></span> | <span data-ttu-id="08838-150">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="08838-150">Currency</span></span> | <span data-ttu-id="08838-151">Upphæð</span><span class="sxs-lookup"><span data-stu-id="08838-151">Amount</span></span> | <span data-ttu-id="08838-152">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="08838-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="08838-153">110110</span><span class="sxs-lookup"><span data-stu-id="08838-153">110110</span></span>         | <span data-ttu-id="08838-154">EUR</span><span class="sxs-lookup"><span data-stu-id="08838-154">EUR</span></span>      | <span data-ttu-id="08838-155">250</span><span class="sxs-lookup"><span data-stu-id="08838-155">250</span></span>    | <span data-ttu-id="08838-156">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="08838-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="08838-157">130100</span><span class="sxs-lookup"><span data-stu-id="08838-157">130100</span></span>         | <span data-ttu-id="08838-158">EUR</span><span class="sxs-lookup"><span data-stu-id="08838-158">EUR</span></span>      | <span data-ttu-id="08838-159">-250</span><span class="sxs-lookup"><span data-stu-id="08838-159">-250</span></span>   | <span data-ttu-id="08838-160">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="08838-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="08838-161">Endurmeta gjaldmiðilinn fyrir lykla frá Október 1, 2015, til og með 30 Nóvember 2015</span><span class="sxs-lookup"><span data-stu-id="08838-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="08838-162">Stöður í samstæðufyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="08838-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="08838-163">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="08838-163">Ledger account</span></span> | <span data-ttu-id="08838-164">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="08838-164">Currency</span></span> | <span data-ttu-id="08838-165">Upphæð</span><span class="sxs-lookup"><span data-stu-id="08838-165">Amount</span></span>  | <span data-ttu-id="08838-166">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="08838-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="08838-167">110110</span><span class="sxs-lookup"><span data-stu-id="08838-167">110110</span></span>         | <span data-ttu-id="08838-168">EUR</span><span class="sxs-lookup"><span data-stu-id="08838-168">EUR</span></span>      | <span data-ttu-id="08838-169">333,33</span><span class="sxs-lookup"><span data-stu-id="08838-169">333.33</span></span>  | <span data-ttu-id="08838-170">Upprunaleg upphæð uppá 500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="08838-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="08838-171">130100</span><span class="sxs-lookup"><span data-stu-id="08838-171">130100</span></span>         | <span data-ttu-id="08838-172">EUR</span><span class="sxs-lookup"><span data-stu-id="08838-172">EUR</span></span>      | <span data-ttu-id="08838-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="08838-173">-333.33</span></span> | <span data-ttu-id="08838-174">Upprunaleg upphæð uppá -500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="08838-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="08838-175">801400</span><span class="sxs-lookup"><span data-stu-id="08838-175">801400</span></span>         | <span data-ttu-id="08838-176">EUR</span><span class="sxs-lookup"><span data-stu-id="08838-176">EUR</span></span>      | <span data-ttu-id="08838-177">83,33</span><span class="sxs-lookup"><span data-stu-id="08838-177">83.33</span></span>   | <span data-ttu-id="08838-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="08838-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="08838-179">801600</span><span class="sxs-lookup"><span data-stu-id="08838-179">801600</span></span>         | <span data-ttu-id="08838-180">EUR</span><span class="sxs-lookup"><span data-stu-id="08838-180">EUR</span></span>      | <span data-ttu-id="08838-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="08838-181">-83.33</span></span>  | <span data-ttu-id="08838-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="08838-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="08838-183">Þú munst sjá viðbótarfærslur fyrir upphæðir skýrslugjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="08838-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="08838-184">Endurmeta gjaldmiðilinn fyrir lykla frá Október 1, 2015, til og með 31 desember 2015</span><span class="sxs-lookup"><span data-stu-id="08838-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="08838-185">Stöður í samstæðufyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="08838-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="08838-186">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="08838-186">Ledger account</span></span> | <span data-ttu-id="08838-187">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="08838-187">Currency</span></span> | <span data-ttu-id="08838-188">Upphæð</span><span class="sxs-lookup"><span data-stu-id="08838-188">Amount</span></span>  | <span data-ttu-id="08838-189">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="08838-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="08838-190">110110</span><span class="sxs-lookup"><span data-stu-id="08838-190">110110</span></span>         | <span data-ttu-id="08838-191">EUR</span><span class="sxs-lookup"><span data-stu-id="08838-191">EUR</span></span>      | <span data-ttu-id="08838-192">500,00</span><span class="sxs-lookup"><span data-stu-id="08838-192">500.00</span></span>  | <span data-ttu-id="08838-193">Upprunaleg upphæð uppá 500 × 1</span><span class="sxs-lookup"><span data-stu-id="08838-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="08838-194">130100</span><span class="sxs-lookup"><span data-stu-id="08838-194">130100</span></span>         | <span data-ttu-id="08838-195">EUR</span><span class="sxs-lookup"><span data-stu-id="08838-195">EUR</span></span>      | <span data-ttu-id="08838-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="08838-196">-500.00</span></span> | <span data-ttu-id="08838-197">Upprunaleg upphæð uppá -500 × 1</span><span class="sxs-lookup"><span data-stu-id="08838-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="08838-198">801400</span><span class="sxs-lookup"><span data-stu-id="08838-198">801400</span></span>         | <span data-ttu-id="08838-199">EUR</span><span class="sxs-lookup"><span data-stu-id="08838-199">EUR</span></span>      | <span data-ttu-id="08838-200">250</span><span class="sxs-lookup"><span data-stu-id="08838-200">250</span></span>     | <span data-ttu-id="08838-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="08838-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="08838-202">801600</span><span class="sxs-lookup"><span data-stu-id="08838-202">801600</span></span>         | <span data-ttu-id="08838-203">EUR</span><span class="sxs-lookup"><span data-stu-id="08838-203">EUR</span></span>      | <span data-ttu-id="08838-204">-250</span><span class="sxs-lookup"><span data-stu-id="08838-204">-250</span></span>    | <span data-ttu-id="08838-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="08838-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






