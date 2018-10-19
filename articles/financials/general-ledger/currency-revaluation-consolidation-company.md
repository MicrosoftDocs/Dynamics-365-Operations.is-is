---
title: "Endurmat á gjaldmiðli í samstæðufyrirtæki"
description: "Þetta efnisatriði lýsir því hvernig á að endurmeta gjaldmiðil í samstæðufyrirtæki."
author: ShylaThompson
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ad0083018d2734cb1e36cbf5f94105376c57cdf9
ms.openlocfilehash: 76290564037ab6f5c7a1cd4508a819bd603e8148
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="0f2e5-103">Endurmat á gjaldmiðli í samstæðufyrirtæki</span><span class="sxs-lookup"><span data-stu-id="0f2e5-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f2e5-104">Þegar gögn frá einum bókhaldsgjaldmiðill til annars eru sameinuð, verður samt að keyra gjaldmiðilsendurmatið ef breyting á gjaldmiðla verður , þannig að lykilsstöður þínar séu rétt endurmetnar.</span><span class="sxs-lookup"><span data-stu-id="0f2e5-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="0f2e5-105">Þegar gögnum eru sameinuð í upphafi, nota á **umreikningur Gjaldmiðils** flipa til að velja fyrstu gengi fyrir þýðingu á meðan á sameiningarferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="0f2e5-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="0f2e5-106">Eftir að nýtt gengi er fært inn (til dæmis í næsta mánuð), verður að endurmeta stöðu lykils.</span><span class="sxs-lookup"><span data-stu-id="0f2e5-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="0f2e5-107">Óinnleystur hagnaður eða tap er síðan uppfærð til samræmis, byggt á nýju gengi og dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="0f2e5-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="0f2e5-108">Eftirfarandi dæmi sýnir bókhaldsfærslur sem eru stofnaðar á meðan vinnslu stendur.</span><span class="sxs-lookup"><span data-stu-id="0f2e5-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="0f2e5-109">Uppsetning fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="0f2e5-109">Company setup</span></span>
-   <span data-ttu-id="0f2e5-110">**Uppruna/rekstrar fyrirtæki (USMF)** – Bandarískum dollurum (USD) eru notaðar sem á bókhalds og skýrslugjaldmiðill.</span><span class="sxs-lookup"><span data-stu-id="0f2e5-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="0f2e5-111">**Sameinað fyrirtæki (CON)** – Evrur (EUR) eru notaðar sem á bókhalds og skýrslugjaldmiðill.</span><span class="sxs-lookup"><span data-stu-id="0f2e5-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="0f2e5-112">**Innleystur hagnaður** – fjárhagslykill 801500</span><span class="sxs-lookup"><span data-stu-id="0f2e5-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="0f2e5-113">**Innleystur tap** – fjárhagslykill 801600</span><span class="sxs-lookup"><span data-stu-id="0f2e5-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="0f2e5-114">**Óinnleystur hagnaður**– fjárhagslykill 801600</span><span class="sxs-lookup"><span data-stu-id="0f2e5-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="0f2e5-115">**Óinnleyst tap**– fjárhagslykill 801400</span><span class="sxs-lookup"><span data-stu-id="0f2e5-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="0f2e5-116">Upphaflegar færslur</span><span class="sxs-lookup"><span data-stu-id="0f2e5-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="0f2e5-117">innhreyfingarfærslur Reiðufés í USMF</span><span class="sxs-lookup"><span data-stu-id="0f2e5-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="0f2e5-118">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="0f2e5-118">Date</span></span>       | <span data-ttu-id="0f2e5-119">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="0f2e5-119">Ledger account</span></span>               | <span data-ttu-id="0f2e5-120">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="0f2e5-120">Currency</span></span> | <span data-ttu-id="0f2e5-121">Upphæð</span><span class="sxs-lookup"><span data-stu-id="0f2e5-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="0f2e5-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="0f2e5-122">10/11/2015</span></span> | <span data-ttu-id="0f2e5-123">110110 – Reiðufé</span><span class="sxs-lookup"><span data-stu-id="0f2e5-123">110110 – Cash</span></span>                | <span data-ttu-id="0f2e5-124">USD</span><span class="sxs-lookup"><span data-stu-id="0f2e5-124">USD</span></span>      | <span data-ttu-id="0f2e5-125">500</span><span class="sxs-lookup"><span data-stu-id="0f2e5-125">500</span></span>    |
| <span data-ttu-id="0f2e5-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="0f2e5-126">10/11/2015</span></span> | <span data-ttu-id="0f2e5-127">130100 – Viðskiptakröfur</span><span class="sxs-lookup"><span data-stu-id="0f2e5-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="0f2e5-128">USD</span><span class="sxs-lookup"><span data-stu-id="0f2e5-128">USD</span></span>      | <span data-ttu-id="0f2e5-129">-500</span><span class="sxs-lookup"><span data-stu-id="0f2e5-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="0f2e5-130">Gengi gjaldmiðla</span><span class="sxs-lookup"><span data-stu-id="0f2e5-130">Exchange rates</span></span>

| <span data-ttu-id="0f2e5-131">Úr gjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="0f2e5-131">From currency</span></span> | <span data-ttu-id="0f2e5-132">Í gjaldmiðil</span><span class="sxs-lookup"><span data-stu-id="0f2e5-132">To currency</span></span> | <span data-ttu-id="0f2e5-133">Upphafsdagsetning</span><span class="sxs-lookup"><span data-stu-id="0f2e5-133">Start date</span></span> | <span data-ttu-id="0f2e5-134">Gengi</span><span class="sxs-lookup"><span data-stu-id="0f2e5-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="0f2e5-135">EUR</span><span class="sxs-lookup"><span data-stu-id="0f2e5-135">EUR</span></span>           | <span data-ttu-id="0f2e5-136">USD</span><span class="sxs-lookup"><span data-stu-id="0f2e5-136">USD</span></span>         | <span data-ttu-id="0f2e5-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="0f2e5-137">10/1/2015</span></span>  | <span data-ttu-id="0f2e5-138">200</span><span class="sxs-lookup"><span data-stu-id="0f2e5-138">200</span></span>           |
| <span data-ttu-id="0f2e5-139">EUR</span><span class="sxs-lookup"><span data-stu-id="0f2e5-139">EUR</span></span>           | <span data-ttu-id="0f2e5-140">USD</span><span class="sxs-lookup"><span data-stu-id="0f2e5-140">USD</span></span>         | <span data-ttu-id="0f2e5-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="0f2e5-141">11/1/2015</span></span>  | <span data-ttu-id="0f2e5-142">150</span><span class="sxs-lookup"><span data-stu-id="0f2e5-142">150</span></span>           |
| <span data-ttu-id="0f2e5-143">EUR</span><span class="sxs-lookup"><span data-stu-id="0f2e5-143">EUR</span></span>           | <span data-ttu-id="0f2e5-144">USD</span><span class="sxs-lookup"><span data-stu-id="0f2e5-144">USD</span></span>         | <span data-ttu-id="0f2e5-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="0f2e5-145">12/1/2012</span></span>  | <span data-ttu-id="0f2e5-146">100</span><span class="sxs-lookup"><span data-stu-id="0f2e5-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="0f2e5-147">Framkvæma sameiningu fyrir Október 2015</span><span class="sxs-lookup"><span data-stu-id="0f2e5-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="0f2e5-148">Stöður í samstæðufyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="0f2e5-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="0f2e5-149">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="0f2e5-149">Ledger account</span></span> | <span data-ttu-id="0f2e5-150">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="0f2e5-150">Currency</span></span> | <span data-ttu-id="0f2e5-151">Upphæð</span><span class="sxs-lookup"><span data-stu-id="0f2e5-151">Amount</span></span> | <span data-ttu-id="0f2e5-152">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="0f2e5-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="0f2e5-153">110110</span><span class="sxs-lookup"><span data-stu-id="0f2e5-153">110110</span></span>         | <span data-ttu-id="0f2e5-154">EUR</span><span class="sxs-lookup"><span data-stu-id="0f2e5-154">EUR</span></span>      | <span data-ttu-id="0f2e5-155">250</span><span class="sxs-lookup"><span data-stu-id="0f2e5-155">250</span></span>    | <span data-ttu-id="0f2e5-156">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="0f2e5-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="0f2e5-157">130100</span><span class="sxs-lookup"><span data-stu-id="0f2e5-157">130100</span></span>         | <span data-ttu-id="0f2e5-158">EUR</span><span class="sxs-lookup"><span data-stu-id="0f2e5-158">EUR</span></span>      | <span data-ttu-id="0f2e5-159">-250</span><span class="sxs-lookup"><span data-stu-id="0f2e5-159">-250</span></span>   | <span data-ttu-id="0f2e5-160">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="0f2e5-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="0f2e5-161">Endurmeta gjaldmiðilinn fyrir lykla frá Október 1, 2015, til og með 30 Nóvember 2015</span><span class="sxs-lookup"><span data-stu-id="0f2e5-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="0f2e5-162">Stöður í samstæðufyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="0f2e5-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="0f2e5-163">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="0f2e5-163">Ledger account</span></span> | <span data-ttu-id="0f2e5-164">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="0f2e5-164">Currency</span></span> | <span data-ttu-id="0f2e5-165">Upphæð</span><span class="sxs-lookup"><span data-stu-id="0f2e5-165">Amount</span></span>  | <span data-ttu-id="0f2e5-166">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="0f2e5-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="0f2e5-167">110110</span><span class="sxs-lookup"><span data-stu-id="0f2e5-167">110110</span></span>         | <span data-ttu-id="0f2e5-168">EUR</span><span class="sxs-lookup"><span data-stu-id="0f2e5-168">EUR</span></span>      | <span data-ttu-id="0f2e5-169">333,33</span><span class="sxs-lookup"><span data-stu-id="0f2e5-169">333.33</span></span>  | <span data-ttu-id="0f2e5-170">Upprunaleg upphæð uppá 500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="0f2e5-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="0f2e5-171">130100</span><span class="sxs-lookup"><span data-stu-id="0f2e5-171">130100</span></span>         | <span data-ttu-id="0f2e5-172">EUR</span><span class="sxs-lookup"><span data-stu-id="0f2e5-172">EUR</span></span>      | <span data-ttu-id="0f2e5-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="0f2e5-173">-333.33</span></span> | <span data-ttu-id="0f2e5-174">Upprunaleg upphæð uppá -500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="0f2e5-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="0f2e5-175">801400</span><span class="sxs-lookup"><span data-stu-id="0f2e5-175">801400</span></span>         | <span data-ttu-id="0f2e5-176">EUR</span><span class="sxs-lookup"><span data-stu-id="0f2e5-176">EUR</span></span>      | <span data-ttu-id="0f2e5-177">83,33</span><span class="sxs-lookup"><span data-stu-id="0f2e5-177">83.33</span></span>   | <span data-ttu-id="0f2e5-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="0f2e5-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="0f2e5-179">801600</span><span class="sxs-lookup"><span data-stu-id="0f2e5-179">801600</span></span>         | <span data-ttu-id="0f2e5-180">EUR</span><span class="sxs-lookup"><span data-stu-id="0f2e5-180">EUR</span></span>      | <span data-ttu-id="0f2e5-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="0f2e5-181">-83.33</span></span>  | <span data-ttu-id="0f2e5-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="0f2e5-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="0f2e5-183">Þú munst sjá viðbótarfærslur fyrir upphæðir skýrslugjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="0f2e5-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="0f2e5-184">Endurmeta gjaldmiðilinn fyrir lykla frá Október 1, 2015, til og með 31 desember 2015</span><span class="sxs-lookup"><span data-stu-id="0f2e5-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="0f2e5-185">Stöður í samstæðufyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="0f2e5-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="0f2e5-186">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="0f2e5-186">Ledger account</span></span> | <span data-ttu-id="0f2e5-187">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="0f2e5-187">Currency</span></span> | <span data-ttu-id="0f2e5-188">Upphæð</span><span class="sxs-lookup"><span data-stu-id="0f2e5-188">Amount</span></span>  | <span data-ttu-id="0f2e5-189">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="0f2e5-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="0f2e5-190">110110</span><span class="sxs-lookup"><span data-stu-id="0f2e5-190">110110</span></span>         | <span data-ttu-id="0f2e5-191">EUR</span><span class="sxs-lookup"><span data-stu-id="0f2e5-191">EUR</span></span>      | <span data-ttu-id="0f2e5-192">500,00</span><span class="sxs-lookup"><span data-stu-id="0f2e5-192">500.00</span></span>  | <span data-ttu-id="0f2e5-193">Upprunaleg upphæð uppá 500 × 1</span><span class="sxs-lookup"><span data-stu-id="0f2e5-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="0f2e5-194">130100</span><span class="sxs-lookup"><span data-stu-id="0f2e5-194">130100</span></span>         | <span data-ttu-id="0f2e5-195">EUR</span><span class="sxs-lookup"><span data-stu-id="0f2e5-195">EUR</span></span>      | <span data-ttu-id="0f2e5-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="0f2e5-196">-500.00</span></span> | <span data-ttu-id="0f2e5-197">Upprunaleg upphæð uppá -500 × 1</span><span class="sxs-lookup"><span data-stu-id="0f2e5-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="0f2e5-198">801400</span><span class="sxs-lookup"><span data-stu-id="0f2e5-198">801400</span></span>         | <span data-ttu-id="0f2e5-199">EUR</span><span class="sxs-lookup"><span data-stu-id="0f2e5-199">EUR</span></span>      | <span data-ttu-id="0f2e5-200">250</span><span class="sxs-lookup"><span data-stu-id="0f2e5-200">250</span></span>     | <span data-ttu-id="0f2e5-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="0f2e5-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="0f2e5-202">801600</span><span class="sxs-lookup"><span data-stu-id="0f2e5-202">801600</span></span>         | <span data-ttu-id="0f2e5-203">EUR</span><span class="sxs-lookup"><span data-stu-id="0f2e5-203">EUR</span></span>      | <span data-ttu-id="0f2e5-204">-250</span><span class="sxs-lookup"><span data-stu-id="0f2e5-204">-250</span></span>    | <span data-ttu-id="0f2e5-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="0f2e5-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






