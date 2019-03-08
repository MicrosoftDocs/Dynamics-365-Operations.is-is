---
title: Endurmat á gjaldmiðli í samstæðufyrirtæki
description: Þetta efnisatriði lýsir því hvernig á að endurmeta gjaldmiðil í samstæðufyrirtæki.
author: ShylaThompson
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
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
ms.openlocfilehash: 76290564037ab6f5c7a1cd4508a819bd603e8148
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "338752"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="2b39f-103">Endurmat á gjaldmiðli í samstæðufyrirtæki</span><span class="sxs-lookup"><span data-stu-id="2b39f-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2b39f-104">Þegar gögn frá einum bókhaldsgjaldmiðill til annars eru sameinuð, verður samt að keyra gjaldmiðilsendurmatið ef breyting á gjaldmiðla verður , þannig að lykilsstöður þínar séu rétt endurmetnar.</span><span class="sxs-lookup"><span data-stu-id="2b39f-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="2b39f-105">Þegar gögnum eru sameinuð í upphafi, nota á **umreikningur Gjaldmiðils** flipa til að velja fyrstu gengi fyrir þýðingu á meðan á sameiningarferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="2b39f-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="2b39f-106">Eftir að nýtt gengi er fært inn (til dæmis í næsta mánuð), verður að endurmeta stöðu lykils.</span><span class="sxs-lookup"><span data-stu-id="2b39f-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="2b39f-107">Óinnleystur hagnaður eða tap er síðan uppfærð til samræmis, byggt á nýju gengi og dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="2b39f-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="2b39f-108">Eftirfarandi dæmi sýnir bókhaldsfærslur sem eru stofnaðar á meðan vinnslu stendur.</span><span class="sxs-lookup"><span data-stu-id="2b39f-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="2b39f-109">Uppsetning fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="2b39f-109">Company setup</span></span>
-   <span data-ttu-id="2b39f-110">**Uppruna/rekstrar fyrirtæki (USMF)** – Bandarískum dollurum (USD) eru notaðar sem á bókhalds og skýrslugjaldmiðill.</span><span class="sxs-lookup"><span data-stu-id="2b39f-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="2b39f-111">**Sameinað fyrirtæki (CON)** – Evrur (EUR) eru notaðar sem á bókhalds og skýrslugjaldmiðill.</span><span class="sxs-lookup"><span data-stu-id="2b39f-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="2b39f-112">**Innleystur hagnaður** – fjárhagslykill 801500</span><span class="sxs-lookup"><span data-stu-id="2b39f-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="2b39f-113">**Innleystur tap** – fjárhagslykill 801600</span><span class="sxs-lookup"><span data-stu-id="2b39f-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="2b39f-114">**Óinnleystur hagnaður**– fjárhagslykill 801600</span><span class="sxs-lookup"><span data-stu-id="2b39f-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="2b39f-115">**Óinnleyst tap**– fjárhagslykill 801400</span><span class="sxs-lookup"><span data-stu-id="2b39f-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="2b39f-116">Upphaflegar færslur</span><span class="sxs-lookup"><span data-stu-id="2b39f-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="2b39f-117">innhreyfingarfærslur Reiðufés í USMF</span><span class="sxs-lookup"><span data-stu-id="2b39f-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="2b39f-118">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="2b39f-118">Date</span></span>       | <span data-ttu-id="2b39f-119">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="2b39f-119">Ledger account</span></span>               | <span data-ttu-id="2b39f-120">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="2b39f-120">Currency</span></span> | <span data-ttu-id="2b39f-121">Upphæð</span><span class="sxs-lookup"><span data-stu-id="2b39f-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="2b39f-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="2b39f-122">10/11/2015</span></span> | <span data-ttu-id="2b39f-123">110110 – Reiðufé</span><span class="sxs-lookup"><span data-stu-id="2b39f-123">110110 – Cash</span></span>                | <span data-ttu-id="2b39f-124">USD</span><span class="sxs-lookup"><span data-stu-id="2b39f-124">USD</span></span>      | <span data-ttu-id="2b39f-125">500</span><span class="sxs-lookup"><span data-stu-id="2b39f-125">500</span></span>    |
| <span data-ttu-id="2b39f-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="2b39f-126">10/11/2015</span></span> | <span data-ttu-id="2b39f-127">130100 – Viðskiptakröfur</span><span class="sxs-lookup"><span data-stu-id="2b39f-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="2b39f-128">USD</span><span class="sxs-lookup"><span data-stu-id="2b39f-128">USD</span></span>      | <span data-ttu-id="2b39f-129">-500</span><span class="sxs-lookup"><span data-stu-id="2b39f-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="2b39f-130">Gengi gjaldmiðla</span><span class="sxs-lookup"><span data-stu-id="2b39f-130">Exchange rates</span></span>

| <span data-ttu-id="2b39f-131">Úr gjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="2b39f-131">From currency</span></span> | <span data-ttu-id="2b39f-132">Í gjaldmiðil</span><span class="sxs-lookup"><span data-stu-id="2b39f-132">To currency</span></span> | <span data-ttu-id="2b39f-133">Upphafsdagsetning</span><span class="sxs-lookup"><span data-stu-id="2b39f-133">Start date</span></span> | <span data-ttu-id="2b39f-134">Gengi</span><span class="sxs-lookup"><span data-stu-id="2b39f-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="2b39f-135">EUR</span><span class="sxs-lookup"><span data-stu-id="2b39f-135">EUR</span></span>           | <span data-ttu-id="2b39f-136">USD</span><span class="sxs-lookup"><span data-stu-id="2b39f-136">USD</span></span>         | <span data-ttu-id="2b39f-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="2b39f-137">10/1/2015</span></span>  | <span data-ttu-id="2b39f-138">200</span><span class="sxs-lookup"><span data-stu-id="2b39f-138">200</span></span>           |
| <span data-ttu-id="2b39f-139">EUR</span><span class="sxs-lookup"><span data-stu-id="2b39f-139">EUR</span></span>           | <span data-ttu-id="2b39f-140">USD</span><span class="sxs-lookup"><span data-stu-id="2b39f-140">USD</span></span>         | <span data-ttu-id="2b39f-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="2b39f-141">11/1/2015</span></span>  | <span data-ttu-id="2b39f-142">150</span><span class="sxs-lookup"><span data-stu-id="2b39f-142">150</span></span>           |
| <span data-ttu-id="2b39f-143">EUR</span><span class="sxs-lookup"><span data-stu-id="2b39f-143">EUR</span></span>           | <span data-ttu-id="2b39f-144">USD</span><span class="sxs-lookup"><span data-stu-id="2b39f-144">USD</span></span>         | <span data-ttu-id="2b39f-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="2b39f-145">12/1/2012</span></span>  | <span data-ttu-id="2b39f-146">100</span><span class="sxs-lookup"><span data-stu-id="2b39f-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="2b39f-147">Framkvæma sameiningu fyrir Október 2015</span><span class="sxs-lookup"><span data-stu-id="2b39f-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="2b39f-148">Stöður í samstæðufyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="2b39f-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="2b39f-149">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="2b39f-149">Ledger account</span></span> | <span data-ttu-id="2b39f-150">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="2b39f-150">Currency</span></span> | <span data-ttu-id="2b39f-151">Upphæð</span><span class="sxs-lookup"><span data-stu-id="2b39f-151">Amount</span></span> | <span data-ttu-id="2b39f-152">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="2b39f-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="2b39f-153">110110</span><span class="sxs-lookup"><span data-stu-id="2b39f-153">110110</span></span>         | <span data-ttu-id="2b39f-154">EUR</span><span class="sxs-lookup"><span data-stu-id="2b39f-154">EUR</span></span>      | <span data-ttu-id="2b39f-155">250</span><span class="sxs-lookup"><span data-stu-id="2b39f-155">250</span></span>    | <span data-ttu-id="2b39f-156">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="2b39f-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="2b39f-157">130100</span><span class="sxs-lookup"><span data-stu-id="2b39f-157">130100</span></span>         | <span data-ttu-id="2b39f-158">EUR</span><span class="sxs-lookup"><span data-stu-id="2b39f-158">EUR</span></span>      | <span data-ttu-id="2b39f-159">-250</span><span class="sxs-lookup"><span data-stu-id="2b39f-159">-250</span></span>   | <span data-ttu-id="2b39f-160">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="2b39f-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="2b39f-161">Endurmeta gjaldmiðilinn fyrir lykla frá Október 1, 2015, til og með 30 Nóvember 2015</span><span class="sxs-lookup"><span data-stu-id="2b39f-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="2b39f-162">Stöður í samstæðufyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="2b39f-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="2b39f-163">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="2b39f-163">Ledger account</span></span> | <span data-ttu-id="2b39f-164">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="2b39f-164">Currency</span></span> | <span data-ttu-id="2b39f-165">Upphæð</span><span class="sxs-lookup"><span data-stu-id="2b39f-165">Amount</span></span>  | <span data-ttu-id="2b39f-166">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="2b39f-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="2b39f-167">110110</span><span class="sxs-lookup"><span data-stu-id="2b39f-167">110110</span></span>         | <span data-ttu-id="2b39f-168">EUR</span><span class="sxs-lookup"><span data-stu-id="2b39f-168">EUR</span></span>      | <span data-ttu-id="2b39f-169">333,33</span><span class="sxs-lookup"><span data-stu-id="2b39f-169">333.33</span></span>  | <span data-ttu-id="2b39f-170">Upprunaleg upphæð uppá 500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="2b39f-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="2b39f-171">130100</span><span class="sxs-lookup"><span data-stu-id="2b39f-171">130100</span></span>         | <span data-ttu-id="2b39f-172">EUR</span><span class="sxs-lookup"><span data-stu-id="2b39f-172">EUR</span></span>      | <span data-ttu-id="2b39f-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="2b39f-173">-333.33</span></span> | <span data-ttu-id="2b39f-174">Upprunaleg upphæð uppá -500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="2b39f-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="2b39f-175">801400</span><span class="sxs-lookup"><span data-stu-id="2b39f-175">801400</span></span>         | <span data-ttu-id="2b39f-176">EUR</span><span class="sxs-lookup"><span data-stu-id="2b39f-176">EUR</span></span>      | <span data-ttu-id="2b39f-177">83,33</span><span class="sxs-lookup"><span data-stu-id="2b39f-177">83.33</span></span>   | <span data-ttu-id="2b39f-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="2b39f-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="2b39f-179">801600</span><span class="sxs-lookup"><span data-stu-id="2b39f-179">801600</span></span>         | <span data-ttu-id="2b39f-180">EUR</span><span class="sxs-lookup"><span data-stu-id="2b39f-180">EUR</span></span>      | <span data-ttu-id="2b39f-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="2b39f-181">-83.33</span></span>  | <span data-ttu-id="2b39f-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="2b39f-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="2b39f-183">Þú munst sjá viðbótarfærslur fyrir upphæðir skýrslugjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="2b39f-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="2b39f-184">Endurmeta gjaldmiðilinn fyrir lykla frá Október 1, 2015, til og með 31 desember 2015</span><span class="sxs-lookup"><span data-stu-id="2b39f-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="2b39f-185">Stöður í samstæðufyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="2b39f-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="2b39f-186">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="2b39f-186">Ledger account</span></span> | <span data-ttu-id="2b39f-187">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="2b39f-187">Currency</span></span> | <span data-ttu-id="2b39f-188">Upphæð</span><span class="sxs-lookup"><span data-stu-id="2b39f-188">Amount</span></span>  | <span data-ttu-id="2b39f-189">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="2b39f-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="2b39f-190">110110</span><span class="sxs-lookup"><span data-stu-id="2b39f-190">110110</span></span>         | <span data-ttu-id="2b39f-191">EUR</span><span class="sxs-lookup"><span data-stu-id="2b39f-191">EUR</span></span>      | <span data-ttu-id="2b39f-192">500,00</span><span class="sxs-lookup"><span data-stu-id="2b39f-192">500.00</span></span>  | <span data-ttu-id="2b39f-193">Upprunaleg upphæð uppá 500 × 1</span><span class="sxs-lookup"><span data-stu-id="2b39f-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="2b39f-194">130100</span><span class="sxs-lookup"><span data-stu-id="2b39f-194">130100</span></span>         | <span data-ttu-id="2b39f-195">EUR</span><span class="sxs-lookup"><span data-stu-id="2b39f-195">EUR</span></span>      | <span data-ttu-id="2b39f-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="2b39f-196">-500.00</span></span> | <span data-ttu-id="2b39f-197">Upprunaleg upphæð uppá -500 × 1</span><span class="sxs-lookup"><span data-stu-id="2b39f-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="2b39f-198">801400</span><span class="sxs-lookup"><span data-stu-id="2b39f-198">801400</span></span>         | <span data-ttu-id="2b39f-199">EUR</span><span class="sxs-lookup"><span data-stu-id="2b39f-199">EUR</span></span>      | <span data-ttu-id="2b39f-200">250</span><span class="sxs-lookup"><span data-stu-id="2b39f-200">250</span></span>     | <span data-ttu-id="2b39f-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="2b39f-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="2b39f-202">801600</span><span class="sxs-lookup"><span data-stu-id="2b39f-202">801600</span></span>         | <span data-ttu-id="2b39f-203">EUR</span><span class="sxs-lookup"><span data-stu-id="2b39f-203">EUR</span></span>      | <span data-ttu-id="2b39f-204">-250</span><span class="sxs-lookup"><span data-stu-id="2b39f-204">-250</span></span>    | <span data-ttu-id="2b39f-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="2b39f-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





