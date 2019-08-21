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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b7f0a18910cbaed382971e47eb688c075e7e6a5
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839426"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a><span data-ttu-id="28b8d-103">Endurmat á gjaldmiðli í samstæðufyrirtæki</span><span class="sxs-lookup"><span data-stu-id="28b8d-103">Currency revaluation in a consolidation company</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28b8d-104">Þegar gögn frá einum bókhaldsgjaldmiðill til annars eru sameinuð, verður samt að keyra gjaldmiðilsendurmatið ef breyting á gjaldmiðla verður , þannig að lykilsstöður þínar séu rétt endurmetnar.</span><span class="sxs-lookup"><span data-stu-id="28b8d-104">When you consolidate data from one accounting currency to another, you must still run currency revaluation if there is a change in exchange rates, so that your account balances  are correctly revalued.</span></span> <span data-ttu-id="28b8d-105">Þegar gögnum eru sameinuð í upphafi, nota á **umreikningur Gjaldmiðils** flipa til að velja fyrstu gengi fyrir þýðingu á meðan á sameiningarferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="28b8d-105">When you originally consolidate the data, use the **Currency translation** tab to select the initial exchange rates to for translation during the consolidation process.</span></span> <span data-ttu-id="28b8d-106">Eftir að nýtt gengi er fært inn (til dæmis í næsta mánuð), verður að endurmeta stöðu lykils.</span><span class="sxs-lookup"><span data-stu-id="28b8d-106">After a new exchange rate is entered (for example, in the next month), you must revalue the account balances.</span></span> <span data-ttu-id="28b8d-107">Óinnleystur hagnaður eða tap er síðan uppfærð til samræmis, byggt á nýju gengi og dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="28b8d-107">The unrealized gains or losses are then updated accordingly, based on the new exchange rate and date.</span></span> <span data-ttu-id="28b8d-108">Eftirfarandi dæmi sýnir bókhaldsfærslur sem eru stofnaðar á meðan vinnslu stendur.</span><span class="sxs-lookup"><span data-stu-id="28b8d-108">The following example illustrates the accounting entries that are created during the process.</span></span>

## <a name="company-setup"></a><span data-ttu-id="28b8d-109">Uppsetning fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="28b8d-109">Company setup</span></span>
-   <span data-ttu-id="28b8d-110">**Uppruna/rekstrar fyrirtæki (USMF)** – Bandarískum dollurum (USD) eru notaðar sem á bókhalds og skýrslugjaldmiðill.</span><span class="sxs-lookup"><span data-stu-id="28b8d-110">**Source/operating company (USMF)** – US dollars (USD) are used as the accounting and reporting currency.</span></span>
-   <span data-ttu-id="28b8d-111">**Sameinað fyrirtæki (CON)** – Evrur (EUR) eru notaðar sem á bókhalds og skýrslugjaldmiðill.</span><span class="sxs-lookup"><span data-stu-id="28b8d-111">**Consolidated company (CON)** – Euros (EUR) are used as the accounting and reporting currency.</span></span>
    -   <span data-ttu-id="28b8d-112">**Innleystur hagnaður** – fjárhagslykill 801500</span><span class="sxs-lookup"><span data-stu-id="28b8d-112">**Realized gain**– Ledger account 801500</span></span>
    -   <span data-ttu-id="28b8d-113">**Innleystur tap** – fjárhagslykill 801600</span><span class="sxs-lookup"><span data-stu-id="28b8d-113">**Realized loss** – Ledger account 801600</span></span>
    -   <span data-ttu-id="28b8d-114">**Óinnleystur hagnaður**– fjárhagslykill 801600</span><span class="sxs-lookup"><span data-stu-id="28b8d-114">**Unrealized gain** – Ledger account 801600</span></span>
    -   <span data-ttu-id="28b8d-115">**Óinnleyst tap**– fjárhagslykill 801400</span><span class="sxs-lookup"><span data-stu-id="28b8d-115">**Unrealized loss** – Ledger account 801400</span></span>

## <a name="original-transactions"></a><span data-ttu-id="28b8d-116">Upphaflegar færslur</span><span class="sxs-lookup"><span data-stu-id="28b8d-116">Original transactions</span></span>
### <a name="cash-receipt-transactions-in-usmf"></a><span data-ttu-id="28b8d-117">innhreyfingarfærslur Reiðufés í USMF</span><span class="sxs-lookup"><span data-stu-id="28b8d-117">Cash receipt transactions in USMF</span></span>

| <span data-ttu-id="28b8d-118">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="28b8d-118">Date</span></span>       | <span data-ttu-id="28b8d-119">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="28b8d-119">Ledger account</span></span>               | <span data-ttu-id="28b8d-120">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="28b8d-120">Currency</span></span> | <span data-ttu-id="28b8d-121">Upphæð</span><span class="sxs-lookup"><span data-stu-id="28b8d-121">Amount</span></span> |
|------------|------------------------------|----------|--------|
| <span data-ttu-id="28b8d-122">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="28b8d-122">10/11/2015</span></span> | <span data-ttu-id="28b8d-123">110110 – Reiðufé</span><span class="sxs-lookup"><span data-stu-id="28b8d-123">110110 – Cash</span></span>                | <span data-ttu-id="28b8d-124">USD</span><span class="sxs-lookup"><span data-stu-id="28b8d-124">USD</span></span>      | <span data-ttu-id="28b8d-125">500</span><span class="sxs-lookup"><span data-stu-id="28b8d-125">500</span></span>    |
| <span data-ttu-id="28b8d-126">10/11/2015</span><span class="sxs-lookup"><span data-stu-id="28b8d-126">10/11/2015</span></span> | <span data-ttu-id="28b8d-127">130100 – Viðskiptakröfur</span><span class="sxs-lookup"><span data-stu-id="28b8d-127">130100 – Accounts Receivable</span></span> | <span data-ttu-id="28b8d-128">USD</span><span class="sxs-lookup"><span data-stu-id="28b8d-128">USD</span></span>      | <span data-ttu-id="28b8d-129">-500</span><span class="sxs-lookup"><span data-stu-id="28b8d-129">-500</span></span>   |

## <a name="exchange-rates"></a><span data-ttu-id="28b8d-130">Gengi gjaldmiðla</span><span class="sxs-lookup"><span data-stu-id="28b8d-130">Exchange rates</span></span>

| <span data-ttu-id="28b8d-131">Úr gjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="28b8d-131">From currency</span></span> | <span data-ttu-id="28b8d-132">Í gjaldmiðil</span><span class="sxs-lookup"><span data-stu-id="28b8d-132">To currency</span></span> | <span data-ttu-id="28b8d-133">Upphafsdagsetning</span><span class="sxs-lookup"><span data-stu-id="28b8d-133">Start date</span></span> | <span data-ttu-id="28b8d-134">Gengi</span><span class="sxs-lookup"><span data-stu-id="28b8d-134">Exchange rate</span></span> |
|---------------|-------------|------------|---------------|
| <span data-ttu-id="28b8d-135">EUR</span><span class="sxs-lookup"><span data-stu-id="28b8d-135">EUR</span></span>           | <span data-ttu-id="28b8d-136">USD</span><span class="sxs-lookup"><span data-stu-id="28b8d-136">USD</span></span>         | <span data-ttu-id="28b8d-137">10/1/2015</span><span class="sxs-lookup"><span data-stu-id="28b8d-137">10/1/2015</span></span>  | <span data-ttu-id="28b8d-138">200</span><span class="sxs-lookup"><span data-stu-id="28b8d-138">200</span></span>           |
| <span data-ttu-id="28b8d-139">EUR</span><span class="sxs-lookup"><span data-stu-id="28b8d-139">EUR</span></span>           | <span data-ttu-id="28b8d-140">USD</span><span class="sxs-lookup"><span data-stu-id="28b8d-140">USD</span></span>         | <span data-ttu-id="28b8d-141">11/1/2015</span><span class="sxs-lookup"><span data-stu-id="28b8d-141">11/1/2015</span></span>  | <span data-ttu-id="28b8d-142">150</span><span class="sxs-lookup"><span data-stu-id="28b8d-142">150</span></span>           |
| <span data-ttu-id="28b8d-143">EUR</span><span class="sxs-lookup"><span data-stu-id="28b8d-143">EUR</span></span>           | <span data-ttu-id="28b8d-144">USD</span><span class="sxs-lookup"><span data-stu-id="28b8d-144">USD</span></span>         | <span data-ttu-id="28b8d-145">12/1/2012</span><span class="sxs-lookup"><span data-stu-id="28b8d-145">12/1/2012</span></span>  | <span data-ttu-id="28b8d-146">100</span><span class="sxs-lookup"><span data-stu-id="28b8d-146">100</span></span>           |

## <a name="perform-the-consolidation-for-october-2015"></a><span data-ttu-id="28b8d-147">Framkvæma sameiningu fyrir Október 2015</span><span class="sxs-lookup"><span data-stu-id="28b8d-147">Perform the consolidation for October 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="28b8d-148">Stöður í samstæðufyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="28b8d-148">Balances in the consolidation company</span></span>

| <span data-ttu-id="28b8d-149">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="28b8d-149">Ledger account</span></span> | <span data-ttu-id="28b8d-150">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="28b8d-150">Currency</span></span> | <span data-ttu-id="28b8d-151">Upphæð</span><span class="sxs-lookup"><span data-stu-id="28b8d-151">Amount</span></span> | <span data-ttu-id="28b8d-152">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="28b8d-152">Calculation</span></span>    |
|----------------|----------|--------|----------------|
| <span data-ttu-id="28b8d-153">110110</span><span class="sxs-lookup"><span data-stu-id="28b8d-153">110110</span></span>         | <span data-ttu-id="28b8d-154">EUR</span><span class="sxs-lookup"><span data-stu-id="28b8d-154">EUR</span></span>      | <span data-ttu-id="28b8d-155">250</span><span class="sxs-lookup"><span data-stu-id="28b8d-155">250</span></span>    | <span data-ttu-id="28b8d-156">500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="28b8d-156">500 USD × 50%</span></span>  |
| <span data-ttu-id="28b8d-157">130100</span><span class="sxs-lookup"><span data-stu-id="28b8d-157">130100</span></span>         | <span data-ttu-id="28b8d-158">EUR</span><span class="sxs-lookup"><span data-stu-id="28b8d-158">EUR</span></span>      | <span data-ttu-id="28b8d-159">-250</span><span class="sxs-lookup"><span data-stu-id="28b8d-159">-250</span></span>   | <span data-ttu-id="28b8d-160">-500 USD × 50%</span><span class="sxs-lookup"><span data-stu-id="28b8d-160">-500 USD × 50%</span></span> |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a><span data-ttu-id="28b8d-161">Endurmeta gjaldmiðilinn fyrir lykla frá Október 1, 2015, til og með 30 Nóvember 2015</span><span class="sxs-lookup"><span data-stu-id="28b8d-161">Perform currency revaluation for the accounts from October 1, 2015, through November 30, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="28b8d-162">Stöður í samstæðufyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="28b8d-162">Balances in the consolidation company</span></span>

| <span data-ttu-id="28b8d-163">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="28b8d-163">Ledger account</span></span> | <span data-ttu-id="28b8d-164">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="28b8d-164">Currency</span></span> | <span data-ttu-id="28b8d-165">Upphæð</span><span class="sxs-lookup"><span data-stu-id="28b8d-165">Amount</span></span>  | <span data-ttu-id="28b8d-166">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="28b8d-166">Calculation</span></span>                        |
|----------------|----------|---------|------------------------------------|
| <span data-ttu-id="28b8d-167">110110</span><span class="sxs-lookup"><span data-stu-id="28b8d-167">110110</span></span>         | <span data-ttu-id="28b8d-168">EUR</span><span class="sxs-lookup"><span data-stu-id="28b8d-168">EUR</span></span>      | <span data-ttu-id="28b8d-169">333,33</span><span class="sxs-lookup"><span data-stu-id="28b8d-169">333.33</span></span>  | <span data-ttu-id="28b8d-170">Upprunaleg upphæð uppá 500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="28b8d-170">Original amount of 500 × 66.6667%</span></span>  |
| <span data-ttu-id="28b8d-171">130100</span><span class="sxs-lookup"><span data-stu-id="28b8d-171">130100</span></span>         | <span data-ttu-id="28b8d-172">EUR</span><span class="sxs-lookup"><span data-stu-id="28b8d-172">EUR</span></span>      | <span data-ttu-id="28b8d-173">-333,33</span><span class="sxs-lookup"><span data-stu-id="28b8d-173">-333.33</span></span> | <span data-ttu-id="28b8d-174">Upprunaleg upphæð uppá -500 × 66,6667%</span><span class="sxs-lookup"><span data-stu-id="28b8d-174">Original amount of -500 × 66.6667%</span></span> |
| <span data-ttu-id="28b8d-175">801400</span><span class="sxs-lookup"><span data-stu-id="28b8d-175">801400</span></span>         | <span data-ttu-id="28b8d-176">EUR</span><span class="sxs-lookup"><span data-stu-id="28b8d-176">EUR</span></span>      | <span data-ttu-id="28b8d-177">83,33</span><span class="sxs-lookup"><span data-stu-id="28b8d-177">83.33</span></span>   | <span data-ttu-id="28b8d-178">333,33 – 250</span><span class="sxs-lookup"><span data-stu-id="28b8d-178">333.33 – 250</span></span>                       |
| <span data-ttu-id="28b8d-179">801600</span><span class="sxs-lookup"><span data-stu-id="28b8d-179">801600</span></span>         | <span data-ttu-id="28b8d-180">EUR</span><span class="sxs-lookup"><span data-stu-id="28b8d-180">EUR</span></span>      | <span data-ttu-id="28b8d-181">-83,33</span><span class="sxs-lookup"><span data-stu-id="28b8d-181">-83.33</span></span>  | <span data-ttu-id="28b8d-182">-333,33 – (-250)</span><span class="sxs-lookup"><span data-stu-id="28b8d-182">-333.33 – (-250)</span></span>                   |

<span data-ttu-id="28b8d-183">Þú munst sjá viðbótarfærslur fyrir upphæðir skýrslugjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="28b8d-183">You will see additional transactions for the reporting currency amounts.</span></span>

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a><span data-ttu-id="28b8d-184">Endurmeta gjaldmiðilinn fyrir lykla frá Október 1, 2015, til og með 31 desember 2015</span><span class="sxs-lookup"><span data-stu-id="28b8d-184">Perform currency revaluation for the accounts from October 1, 2015, through December 31, 2015</span></span>
### <a name="balances-in-the-consolidation-company"></a><span data-ttu-id="28b8d-185">Stöður í samstæðufyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="28b8d-185">Balances in the consolidation company</span></span>

| <span data-ttu-id="28b8d-186">Fjárhagslykill</span><span class="sxs-lookup"><span data-stu-id="28b8d-186">Ledger account</span></span> | <span data-ttu-id="28b8d-187">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="28b8d-187">Currency</span></span> | <span data-ttu-id="28b8d-188">Upphæð</span><span class="sxs-lookup"><span data-stu-id="28b8d-188">Amount</span></span>  | <span data-ttu-id="28b8d-189">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="28b8d-189">Calculation</span></span>                                          |
|----------------|----------|---------|------------------------------------------------------|
| <span data-ttu-id="28b8d-190">110110</span><span class="sxs-lookup"><span data-stu-id="28b8d-190">110110</span></span>         | <span data-ttu-id="28b8d-191">EUR</span><span class="sxs-lookup"><span data-stu-id="28b8d-191">EUR</span></span>      | <span data-ttu-id="28b8d-192">500,00</span><span class="sxs-lookup"><span data-stu-id="28b8d-192">500.00</span></span>  | <span data-ttu-id="28b8d-193">Upprunaleg upphæð uppá 500 × 1</span><span class="sxs-lookup"><span data-stu-id="28b8d-193">Original amount of 500 × 1</span></span>                           |
| <span data-ttu-id="28b8d-194">130100</span><span class="sxs-lookup"><span data-stu-id="28b8d-194">130100</span></span>         | <span data-ttu-id="28b8d-195">EUR</span><span class="sxs-lookup"><span data-stu-id="28b8d-195">EUR</span></span>      | <span data-ttu-id="28b8d-196">-500,00</span><span class="sxs-lookup"><span data-stu-id="28b8d-196">-500.00</span></span> | <span data-ttu-id="28b8d-197">Upprunaleg upphæð uppá -500 × 1</span><span class="sxs-lookup"><span data-stu-id="28b8d-197">Original amount of -500 × 1</span></span>                          |
| <span data-ttu-id="28b8d-198">801400</span><span class="sxs-lookup"><span data-stu-id="28b8d-198">801400</span></span>         | <span data-ttu-id="28b8d-199">EUR</span><span class="sxs-lookup"><span data-stu-id="28b8d-199">EUR</span></span>      | <span data-ttu-id="28b8d-200">250</span><span class="sxs-lookup"><span data-stu-id="28b8d-200">250</span></span>     | <span data-ttu-id="28b8d-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span><span class="sxs-lookup"><span data-stu-id="28b8d-201">500 – 333.33 = 166.67 166.67 + 83.33 = 250</span></span>           |
| <span data-ttu-id="28b8d-202">801600</span><span class="sxs-lookup"><span data-stu-id="28b8d-202">801600</span></span>         | <span data-ttu-id="28b8d-203">EUR</span><span class="sxs-lookup"><span data-stu-id="28b8d-203">EUR</span></span>      | <span data-ttu-id="28b8d-204">-250</span><span class="sxs-lookup"><span data-stu-id="28b8d-204">-250</span></span>    | <span data-ttu-id="28b8d-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span><span class="sxs-lookup"><span data-stu-id="28b8d-205">-500 – (-333.33) = -166.67 -166.67 + (-83.33) = -250</span></span> |





