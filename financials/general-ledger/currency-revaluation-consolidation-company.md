---
title: "Endurmat á gjaldmiðli í samstæðufyrirtæki"
description: 
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 643af8d771685fe8fd652b353d41f2679e0bef8b
ms.contentlocale: is-is
ms.lasthandoff: 07/18/2017

---

# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="73b29-102">Endurmat á gjaldmiðli í samstæðufyrirtæki</span><span class="sxs-lookup"><span data-stu-id="73b29-102">Currency revaluation in a consolidation company</span></span>

[!include[banner](../includes/banner.md)]




<span data-ttu-id="73b29-103">Þegar gögn frá einum bókhaldsgjaldmiðill til annars eru sameinuð, verður samt að keyra gjaldmiðilsendurmatið ef breyting á gjaldmiðla verður , þannig að lykilsstöður þínar séu rétt endurmetnar.</span><span class="sxs-lookup"><span data-stu-id="73b29-103">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="73b29-104">Þegar gögnum eru sameinuð í upphafi, nota á **umreikningur Gjaldmiðils** flipa til að velja fyrstu gengi fyrir þýðingu á meðan á sameiningarferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="73b29-104">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="73b29-105">Eftir að nýtt gengi er fært inn (til dæmis í næsta mánuð), verður að endurmeta stöðu lykils.</span><span class="sxs-lookup"><span data-stu-id="73b29-105">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="73b29-106">Óinnleystur hagnaður eða tap er síðan uppfærð til samræmis, byggt á nýju gengi og dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="73b29-106">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="73b29-107">Eftirfarandi dæmi sýnir bókhaldsfærslur sem eru stofnaðar á meðan vinnslu stendur.</span><span class="sxs-lookup"><span data-stu-id="73b29-107">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="73b29-108">Uppsetning fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="73b29-108">Company setup</span></span>
-   <span data-ttu-id="73b29-109">**Uppruna/rekstrar fyrirtæki (USMF)** – Bandarískum dollurum (USD) eru notaðar sem á bókhalds og skýrslugjaldmiðill.</span><span class="sxs-lookup"><span data-stu-id="73b29-109">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="73b29-110">**Sameinað fyrirtæki (CON)** – Evrur (EUR) eru notaðar sem á bókhalds og skýrslugjaldmiðill.</span><span class="sxs-lookup"><span data-stu-id="73b29-110">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="73b29-111">**Óinnleystur hagnaður**– Fjárhagslykil 801500</span><span class="sxs-lookup"><span data-stu-id="73b29-111">**Realized gain **– Ledger account 801500</span></span>
    -   <span data-ttu-id="73b29-112">**Innleystur tap**– fjárhagslykill 801600</span><span class="sxs-lookup"><span data-stu-id="73b29-112">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="73b29-113">**Óinnleystur hagnaður**– fjárhagslykill 801600</span><span class="sxs-lookup"><span data-stu-id="73b29-113">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="73b29-114">**Óinnleyst tap**– fjárhagslykill 801400</span><span class="sxs-lookup"><span data-stu-id="73b29-114">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="73b29-115">Upphaflegar færslur</span><span class="sxs-lookup"><span data-stu-id="73b29-115">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="73b29-116">innhreyfingarfærslur Reiðufés í USMF</span><span class="sxs-lookup"><span data-stu-id="73b29-116">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="73b29-117">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="73b29-117">Date</span></span>       | <span data-ttu-id="73b29-118">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="73b29-118">Ledger account</span></span>               | <span data-ttu-id="73b29-119">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="73b29-119">Currency</span></span> | <span data-ttu-id="73b29-120">Upphæð</span><span class="sxs-lookup"><span data-stu-id="73b29-120">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="73b29-121">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="73b29-121">10/11/2015</span></span> | <span data-ttu-id="73b29-122">110110 – Reiðufé</span><span class="sxs-lookup"><span data-stu-id="73b29-122">110110 – Cash</span></span>                | <span data-ttu-id="73b29-123">USD</span><span class="sxs-lookup"><span data-stu-id="73b29-123">USD</span></span>      | <span data-ttu-id="73b29-124">500</span><span class="sxs-lookup"><span data-stu-id="73b29-124">500</span></span>    |
| <span data-ttu-id="73b29-125">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="73b29-125">10/11/2015</span></span> | <span data-ttu-id="73b29-126">130100 – Viðskiptakröfur</span><span class="sxs-lookup"><span data-stu-id="73b29-126">130100 – Accounts Receivable</span></span> | <span data-ttu-id="73b29-127">USD</span><span class="sxs-lookup"><span data-stu-id="73b29-127">USD</span></span>      | <span data-ttu-id="73b29-128">-500</span><span class="sxs-lookup"><span data-stu-id="73b29-128">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="73b29-129">Gengi gjaldmiðla</span><span class="sxs-lookup"><span data-stu-id="73b29-129">Exchange rates</span></span>
| <span data-ttu-id="73b29-130">Úr gjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="73b29-130">From currency</span></span> | <span data-ttu-id="73b29-131">Í gjaldmiðil</span><span class="sxs-lookup"><span data-stu-id="73b29-131">To currency</span></span> | <span data-ttu-id="73b29-132">Upphafsdagsetning</span><span class="sxs-lookup"><span data-stu-id="73b29-132">Start date</span></span> | <span data-ttu-id="73b29-133">Gengi</span><span class="sxs-lookup"><span data-stu-id="73b29-133">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="73b29-134">EUR</span><span class="sxs-lookup"><span data-stu-id="73b29-134">EUR</span></span>           | <span data-ttu-id="73b29-135">USD</span><span class="sxs-lookup"><span data-stu-id="73b29-135">USD</span></span>         | <span data-ttu-id="73b29-136">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="73b29-136">10/1/2015</span></span>  | <span data-ttu-id="73b29-137">200</span><span class="sxs-lookup"><span data-stu-id="73b29-137">200</span></span>           |
| <span data-ttu-id="73b29-138">EUR</span><span class="sxs-lookup"><span data-stu-id="73b29-138">EUR</span></span>           | <span data-ttu-id="73b29-139">USD</span><span class="sxs-lookup"><span data-stu-id="73b29-139">USD</span></span>         | <span data-ttu-id="73b29-140">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="73b29-140">11/1/2015</span></span>  | <span data-ttu-id="73b29-141">150</span><span class="sxs-lookup"><span data-stu-id="73b29-141">150</span></span>           |
| <span data-ttu-id="73b29-142">EUR</span><span class="sxs-lookup"><span data-stu-id="73b29-142">EUR</span></span>           | <span data-ttu-id="73b29-143">USD</span><span class="sxs-lookup"><span data-stu-id="73b29-143">USD</span></span>         | <span data-ttu-id="73b29-144">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="73b29-144">12/1/2012</span></span>  | <span data-ttu-id="73b29-145">100</span><span class="sxs-lookup"><span data-stu-id="73b29-145">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="73b29-146">Framkvæma sameiningu fyrir Október 2015</span><span class="sxs-lookup"><span data-stu-id="73b29-146">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="73b29-147">Stöður í samstæðufyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="73b29-147">Balances in the consolidation company</span></span>

| <span data-ttu-id="73b29-148">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="73b29-148">Ledger account</span></span> | <span data-ttu-id="73b29-149">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="73b29-149">Currency</span></span> | <span data-ttu-id="73b29-150">Upphæð</span><span class="sxs-lookup"><span data-stu-id="73b29-150">Amount</span></span> | <span data-ttu-id="73b29-151">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="73b29-151">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="73b29-152">110110</span><span class="sxs-lookup"><span data-stu-id="73b29-152">110110</span></span>         | <span data-ttu-id="73b29-153">EUR</span><span class="sxs-lookup"><span data-stu-id="73b29-153">EUR</span></span>      | <span data-ttu-id="73b29-154">250</span><span class="sxs-lookup"><span data-stu-id="73b29-154">250</span></span>    | <span data-ttu-id="73b29-155">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="73b29-155">500 USD × 50%</span></span>  |
| <span data-ttu-id="73b29-156">130100</span><span class="sxs-lookup"><span data-stu-id="73b29-156">130100</span></span>         | <span data-ttu-id="73b29-157">EUR</span><span class="sxs-lookup"><span data-stu-id="73b29-157">EUR</span></span>      | <span data-ttu-id="73b29-158">-250</span><span class="sxs-lookup"><span data-stu-id="73b29-158">-250</span></span>   | <span data-ttu-id="73b29-159">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="73b29-159">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="73b29-160">Endurmeta gjaldmiðilinn fyrir lykla frá Október 1, 2015, til og með 30 Nóvember 2015</span><span class="sxs-lookup"><span data-stu-id="73b29-160">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="73b29-161">Stöður í samstæðufyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="73b29-161">Balances in the consolidation company</span></span>

| <span data-ttu-id="73b29-162">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="73b29-162">Ledger account</span></span> | <span data-ttu-id="73b29-163">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="73b29-163">Currency</span></span> | <span data-ttu-id="73b29-164">Upphæð</span><span class="sxs-lookup"><span data-stu-id="73b29-164">Amount</span></span>  | <span data-ttu-id="73b29-165">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="73b29-165">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="73b29-166">110110</span><span class="sxs-lookup"><span data-stu-id="73b29-166">110110</span></span>         | <span data-ttu-id="73b29-167">EUR</span><span class="sxs-lookup"><span data-stu-id="73b29-167">EUR</span></span>      | <span data-ttu-id="73b29-168">333,33</span><span class="sxs-lookup"><span data-stu-id="73b29-168">333.33</span></span>  | <span data-ttu-id="73b29-169">Upprunaleg upphæð uppá 500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="73b29-169">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="73b29-170">130100</span><span class="sxs-lookup"><span data-stu-id="73b29-170">130100</span></span>         | <span data-ttu-id="73b29-171">EUR</span><span class="sxs-lookup"><span data-stu-id="73b29-171">EUR</span></span>      | <span data-ttu-id="73b29-172">-333,33</span><span class="sxs-lookup"><span data-stu-id="73b29-172">-333.33</span></span> | <span data-ttu-id="73b29-173">Upprunaleg upphæð uppá -500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="73b29-173">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="73b29-174">801400</span><span class="sxs-lookup"><span data-stu-id="73b29-174">801400</span></span>         | <span data-ttu-id="73b29-175">EUR</span><span class="sxs-lookup"><span data-stu-id="73b29-175">EUR</span></span>      | <span data-ttu-id="73b29-176">83,33</span><span class="sxs-lookup"><span data-stu-id="73b29-176">83.33</span></span>   | <span data-ttu-id="73b29-177">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="73b29-177">333.33 – 250</span></span>                       |
| <span data-ttu-id="73b29-178">801600</span><span class="sxs-lookup"><span data-stu-id="73b29-178">801600</span></span>         | <span data-ttu-id="73b29-179">EUR</span><span class="sxs-lookup"><span data-stu-id="73b29-179">EUR</span></span>      | <span data-ttu-id="73b29-180">-83,33</span><span class="sxs-lookup"><span data-stu-id="73b29-180">-83.33</span></span>  | <span data-ttu-id="73b29-181">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="73b29-181">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="73b29-182">Þú munst sjá viðbótarfærslur fyrir upphæðir skýrslugjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="73b29-182">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="73b29-183">Endurmeta gjaldmiðilinn fyrir lykla frá Október 1, 2015, til og með 31 desember 2015</span><span class="sxs-lookup"><span data-stu-id="73b29-183">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="73b29-184">Stöður í samstæðufyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="73b29-184">Balances in the consolidation company</span></span>

| <span data-ttu-id="73b29-185">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="73b29-185">Ledger account</span></span> | <span data-ttu-id="73b29-186">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="73b29-186">Currency</span></span> | <span data-ttu-id="73b29-187">Upphæð</span><span class="sxs-lookup"><span data-stu-id="73b29-187">Amount</span></span>  | <span data-ttu-id="73b29-188">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="73b29-188">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="73b29-189">110110</span><span class="sxs-lookup"><span data-stu-id="73b29-189">110110</span></span>         | <span data-ttu-id="73b29-190">EUR</span><span class="sxs-lookup"><span data-stu-id="73b29-190">EUR</span></span>      | <span data-ttu-id="73b29-191">500,00</span><span class="sxs-lookup"><span data-stu-id="73b29-191">500.00</span></span>  | <span data-ttu-id="73b29-192">Upprunaleg upphæð uppá 500 × 1</span><span class="sxs-lookup"><span data-stu-id="73b29-192">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="73b29-193">130100</span><span class="sxs-lookup"><span data-stu-id="73b29-193">130100</span></span>         | <span data-ttu-id="73b29-194">EUR</span><span class="sxs-lookup"><span data-stu-id="73b29-194">EUR</span></span>      | <span data-ttu-id="73b29-195">-500,00</span><span class="sxs-lookup"><span data-stu-id="73b29-195">-500.00</span></span> | <span data-ttu-id="73b29-196">Upprunaleg upphæð uppá -500 × 1</span><span class="sxs-lookup"><span data-stu-id="73b29-196">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="73b29-197">801400</span><span class="sxs-lookup"><span data-stu-id="73b29-197">801400</span></span>         | <span data-ttu-id="73b29-198">EUR</span><span class="sxs-lookup"><span data-stu-id="73b29-198">EUR</span></span>      | <span data-ttu-id="73b29-199">250</span><span class="sxs-lookup"><span data-stu-id="73b29-199">250</span></span>     | <span data-ttu-id="73b29-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="73b29-200">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="73b29-201">801600</span><span class="sxs-lookup"><span data-stu-id="73b29-201">801600</span></span>         | <span data-ttu-id="73b29-202">EUR</span><span class="sxs-lookup"><span data-stu-id="73b29-202">EUR</span></span>      | <span data-ttu-id="73b29-203">-250</span><span class="sxs-lookup"><span data-stu-id="73b29-203">-250</span></span>    | <span data-ttu-id="73b29-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="73b29-204">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |






