---
title: Endurmat á gjaldmiðli í samstæðufyrirtæki
description: Þetta efnisatriði lýsir því hvernig á að endurmeta gjaldmiðil í samstæðufyrirtæki.
author: roschlom
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33db12388c969b8dadb38bfacf4d9df333b78bd4
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4444549"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="82f99-103">Endurmat á gjaldmiðli í samstæðufyrirtæki</span><span class="sxs-lookup"><span data-stu-id="82f99-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82f99-104">Þegar gögn frá einum bókhaldsgjaldmiðill til annars eru sameinuð, verður samt að keyra gjaldmiðilsendurmatið ef breyting á gjaldmiðla verður , þannig að lykilsstöður þínar séu rétt endurmetnar.</span><span class="sxs-lookup"><span data-stu-id="82f99-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="82f99-105">Þegar gögnum eru sameinuð í upphafi, nota á **umreikningur Gjaldmiðils** flipa til að velja fyrstu gengi fyrir þýðingu á meðan á sameiningarferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="82f99-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="82f99-106">Eftir að nýtt gengi er fært inn (til dæmis í næsta mánuð), verður að endurmeta stöðu lykils.</span><span class="sxs-lookup"><span data-stu-id="82f99-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="82f99-107">Óinnleystur hagnaður eða tap er síðan uppfærð til samræmis, byggt á nýju gengi og dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="82f99-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="82f99-108">Eftirfarandi dæmi sýnir bókhaldsfærslur sem eru stofnaðar á meðan vinnslu stendur.</span><span class="sxs-lookup"><span data-stu-id="82f99-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="82f99-109">Uppsetning fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="82f99-109">Company setup</span></span>
-   <span data-ttu-id="82f99-110">**Uppruna/rekstrar fyrirtæki (USMF)** – Bandarískum dollurum (USD) eru notaðar sem á bókhalds og skýrslugjaldmiðill.</span><span class="sxs-lookup"><span data-stu-id="82f99-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="82f99-111">**Sameinað fyrirtæki (CON)** – Evrur (EUR) eru notaðar sem á bókhalds og skýrslugjaldmiðill.</span><span class="sxs-lookup"><span data-stu-id="82f99-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="82f99-112">**Innleystur hagnaður** – fjárhagslykill 801500</span><span class="sxs-lookup"><span data-stu-id="82f99-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="82f99-113">**Innleystur tap** – fjárhagslykill 801600</span><span class="sxs-lookup"><span data-stu-id="82f99-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="82f99-114">**Óinnleystur hagnaður**– fjárhagslykill 801600</span><span class="sxs-lookup"><span data-stu-id="82f99-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="82f99-115">**Óinnleyst tap**– fjárhagslykill 801400</span><span class="sxs-lookup"><span data-stu-id="82f99-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="82f99-116">Upphaflegar færslur</span><span class="sxs-lookup"><span data-stu-id="82f99-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="82f99-117">innhreyfingarfærslur Reiðufés í USMF</span><span class="sxs-lookup"><span data-stu-id="82f99-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="82f99-118">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="82f99-118">Date</span></span>       | <span data-ttu-id="82f99-119">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="82f99-119">Ledger account</span></span>               | <span data-ttu-id="82f99-120">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="82f99-120">Currency</span></span> | <span data-ttu-id="82f99-121">Upphæð</span><span class="sxs-lookup"><span data-stu-id="82f99-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="82f99-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="82f99-122">10/11/2015</span></span> | <span data-ttu-id="82f99-123">110110 – Reiðufé</span><span class="sxs-lookup"><span data-stu-id="82f99-123">110110 – Cash</span></span>                | <span data-ttu-id="82f99-124">USD</span><span class="sxs-lookup"><span data-stu-id="82f99-124">USD</span></span>      | <span data-ttu-id="82f99-125">500</span><span class="sxs-lookup"><span data-stu-id="82f99-125">500</span></span>    |
| <span data-ttu-id="82f99-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="82f99-126">10/11/2015</span></span> | <span data-ttu-id="82f99-127">130100 – Viðskiptakröfur</span><span class="sxs-lookup"><span data-stu-id="82f99-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="82f99-128">USD</span><span class="sxs-lookup"><span data-stu-id="82f99-128">USD</span></span>      | <span data-ttu-id="82f99-129">-500</span><span class="sxs-lookup"><span data-stu-id="82f99-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="82f99-130">Gengi gjaldmiðla</span><span class="sxs-lookup"><span data-stu-id="82f99-130">Exchange rates</span></span>

| <span data-ttu-id="82f99-131">Úr gjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="82f99-131">From currency</span></span> | <span data-ttu-id="82f99-132">Í gjaldmiðil</span><span class="sxs-lookup"><span data-stu-id="82f99-132">To currency</span></span> | <span data-ttu-id="82f99-133">Upphafsdagsetning</span><span class="sxs-lookup"><span data-stu-id="82f99-133">Start date</span></span> | <span data-ttu-id="82f99-134">Gengi</span><span class="sxs-lookup"><span data-stu-id="82f99-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="82f99-135">EUR</span><span class="sxs-lookup"><span data-stu-id="82f99-135">EUR</span></span>           | <span data-ttu-id="82f99-136">USD</span><span class="sxs-lookup"><span data-stu-id="82f99-136">USD</span></span>         | <span data-ttu-id="82f99-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="82f99-137">10/1/2015</span></span>  | <span data-ttu-id="82f99-138">200</span><span class="sxs-lookup"><span data-stu-id="82f99-138">200</span></span>           |
| <span data-ttu-id="82f99-139">EUR</span><span class="sxs-lookup"><span data-stu-id="82f99-139">EUR</span></span>           | <span data-ttu-id="82f99-140">USD</span><span class="sxs-lookup"><span data-stu-id="82f99-140">USD</span></span>         | <span data-ttu-id="82f99-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="82f99-141">11/1/2015</span></span>  | <span data-ttu-id="82f99-142">150</span><span class="sxs-lookup"><span data-stu-id="82f99-142">150</span></span>           |
| <span data-ttu-id="82f99-143">EUR</span><span class="sxs-lookup"><span data-stu-id="82f99-143">EUR</span></span>           | <span data-ttu-id="82f99-144">USD</span><span class="sxs-lookup"><span data-stu-id="82f99-144">USD</span></span>         | <span data-ttu-id="82f99-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="82f99-145">12/1/2012</span></span>  | <span data-ttu-id="82f99-146">100</span><span class="sxs-lookup"><span data-stu-id="82f99-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="82f99-147">Framkvæma sameiningu fyrir Október 2015</span><span class="sxs-lookup"><span data-stu-id="82f99-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="82f99-148">Stöður í samstæðufyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="82f99-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="82f99-149">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="82f99-149">Ledger account</span></span> | <span data-ttu-id="82f99-150">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="82f99-150">Currency</span></span> | <span data-ttu-id="82f99-151">Upphæð</span><span class="sxs-lookup"><span data-stu-id="82f99-151">Amount</span></span> | <span data-ttu-id="82f99-152">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="82f99-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="82f99-153">110110</span><span class="sxs-lookup"><span data-stu-id="82f99-153">110110</span></span>         | <span data-ttu-id="82f99-154">EUR</span><span class="sxs-lookup"><span data-stu-id="82f99-154">EUR</span></span>      | <span data-ttu-id="82f99-155">250</span><span class="sxs-lookup"><span data-stu-id="82f99-155">250</span></span>    | <span data-ttu-id="82f99-156">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="82f99-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="82f99-157">130100</span><span class="sxs-lookup"><span data-stu-id="82f99-157">130100</span></span>         | <span data-ttu-id="82f99-158">EUR</span><span class="sxs-lookup"><span data-stu-id="82f99-158">EUR</span></span>      | <span data-ttu-id="82f99-159">-250</span><span class="sxs-lookup"><span data-stu-id="82f99-159">-250</span></span>   | <span data-ttu-id="82f99-160">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="82f99-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="82f99-161">Endurmeta gjaldmiðilinn fyrir lykla frá Október 1, 2015, til og með 30 Nóvember 2015</span><span class="sxs-lookup"><span data-stu-id="82f99-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="82f99-162">Stöður í samstæðufyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="82f99-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="82f99-163">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="82f99-163">Ledger account</span></span> | <span data-ttu-id="82f99-164">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="82f99-164">Currency</span></span> | <span data-ttu-id="82f99-165">Upphæð</span><span class="sxs-lookup"><span data-stu-id="82f99-165">Amount</span></span>  | <span data-ttu-id="82f99-166">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="82f99-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="82f99-167">110110</span><span class="sxs-lookup"><span data-stu-id="82f99-167">110110</span></span>         | <span data-ttu-id="82f99-168">EUR</span><span class="sxs-lookup"><span data-stu-id="82f99-168">EUR</span></span>      | <span data-ttu-id="82f99-169">333,33</span><span class="sxs-lookup"><span data-stu-id="82f99-169">333.33</span></span>  | <span data-ttu-id="82f99-170">Upprunaleg upphæð uppá 500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="82f99-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="82f99-171">130100</span><span class="sxs-lookup"><span data-stu-id="82f99-171">130100</span></span>         | <span data-ttu-id="82f99-172">EUR</span><span class="sxs-lookup"><span data-stu-id="82f99-172">EUR</span></span>      | <span data-ttu-id="82f99-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="82f99-173">-333.33</span></span> | <span data-ttu-id="82f99-174">Upprunaleg upphæð uppá -500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="82f99-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="82f99-175">801400</span><span class="sxs-lookup"><span data-stu-id="82f99-175">801400</span></span>         | <span data-ttu-id="82f99-176">EUR</span><span class="sxs-lookup"><span data-stu-id="82f99-176">EUR</span></span>      | <span data-ttu-id="82f99-177">83,33</span><span class="sxs-lookup"><span data-stu-id="82f99-177">83.33</span></span>   | <span data-ttu-id="82f99-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="82f99-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="82f99-179">801600</span><span class="sxs-lookup"><span data-stu-id="82f99-179">801600</span></span>         | <span data-ttu-id="82f99-180">EUR</span><span class="sxs-lookup"><span data-stu-id="82f99-180">EUR</span></span>      | <span data-ttu-id="82f99-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="82f99-181">-83.33</span></span>  | <span data-ttu-id="82f99-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="82f99-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="82f99-183">Þú munst sjá viðbótarfærslur fyrir upphæðir skýrslugjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="82f99-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="82f99-184">Endurmeta gjaldmiðilinn fyrir lykla frá Október 1, 2015, til og með 31 desember 2015</span><span class="sxs-lookup"><span data-stu-id="82f99-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="82f99-185">Stöður í samstæðufyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="82f99-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="82f99-186">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="82f99-186">Ledger account</span></span> | <span data-ttu-id="82f99-187">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="82f99-187">Currency</span></span> | <span data-ttu-id="82f99-188">Upphæð</span><span class="sxs-lookup"><span data-stu-id="82f99-188">Amount</span></span>  | <span data-ttu-id="82f99-189">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="82f99-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="82f99-190">110110</span><span class="sxs-lookup"><span data-stu-id="82f99-190">110110</span></span>         | <span data-ttu-id="82f99-191">EUR</span><span class="sxs-lookup"><span data-stu-id="82f99-191">EUR</span></span>      | <span data-ttu-id="82f99-192">500,00</span><span class="sxs-lookup"><span data-stu-id="82f99-192">500.00</span></span>  | <span data-ttu-id="82f99-193">Upprunaleg upphæð uppá 500 × 1</span><span class="sxs-lookup"><span data-stu-id="82f99-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="82f99-194">130100</span><span class="sxs-lookup"><span data-stu-id="82f99-194">130100</span></span>         | <span data-ttu-id="82f99-195">EUR</span><span class="sxs-lookup"><span data-stu-id="82f99-195">EUR</span></span>      | <span data-ttu-id="82f99-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="82f99-196">-500.00</span></span> | <span data-ttu-id="82f99-197">Upprunaleg upphæð uppá -500 × 1</span><span class="sxs-lookup"><span data-stu-id="82f99-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="82f99-198">801400</span><span class="sxs-lookup"><span data-stu-id="82f99-198">801400</span></span>         | <span data-ttu-id="82f99-199">EUR</span><span class="sxs-lookup"><span data-stu-id="82f99-199">EUR</span></span>      | <span data-ttu-id="82f99-200">250</span><span class="sxs-lookup"><span data-stu-id="82f99-200">250</span></span>     | <span data-ttu-id="82f99-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="82f99-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="82f99-202">801600</span><span class="sxs-lookup"><span data-stu-id="82f99-202">801600</span></span>         | <span data-ttu-id="82f99-203">EUR</span><span class="sxs-lookup"><span data-stu-id="82f99-203">EUR</span></span>      | <span data-ttu-id="82f99-204">-250</span><span class="sxs-lookup"><span data-stu-id="82f99-204">-250</span></span>    | <span data-ttu-id="82f99-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="82f99-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





