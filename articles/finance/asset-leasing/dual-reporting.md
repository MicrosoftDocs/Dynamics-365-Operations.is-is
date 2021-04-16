---
title: Tvískipt skýrslugjöf
description: Þetta efnisatriði leiðir notandann í gegnum dæmi sem sýnir hvernig hægt er að uppfylla skilyrði bæði um skýrslugerð samkvæmt alþjóðlegum reikningsskilastaðli (IFRS) og lögboðinnar skýrslugerðar um eignaleigu.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c9f2bae330e688e1e941277d46ddcbd38916f8c8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815981"
---
# <a name="dual-reporting"></a><span data-ttu-id="91349-103">Tvískipt skýrslugjöf</span><span class="sxs-lookup"><span data-stu-id="91349-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91349-104">Þetta efnisatriði leiðir notandann í gegnum dæmi sem sýnir hvernig hægt er að uppfylla skilyrði bæði um skýrslugerð samkvæmt alþjóðlegum reikningsskilastaðli (IFRS) og lögboðinnar skýrslugerðar um eignaleigu.</span><span class="sxs-lookup"><span data-stu-id="91349-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="91349-105">Þekking á bókunarlögum í Microsoft Dynamics 365 Finance er áskilin og auðveldar skilning á dæminu.</span><span class="sxs-lookup"><span data-stu-id="91349-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="91349-106">Dæmi</span><span class="sxs-lookup"><span data-stu-id="91349-106">Example</span></span>

<span data-ttu-id="91349-107">Eftirfarandi dæmi sýnir leigusamning sem fellur undir ítalska lögboðna skýrslugerð með því að nota bæði aðferð reiðufjáraðferðar og IFRS-skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="91349-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="91349-108">Fyrirtækið verður að stofna þrjár bækur til að uppfylla skilyrði ítalskra laga og skilyrði IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="91349-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="91349-109">Ein bók er áskilin fyrir IFRS 16, ein bók er áskilin fyrir lögboðnar kröfur og ein bók er áskilin til að bakfæra lögboðnar bókanir sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="91349-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="91349-110">Bækurnar eru settar upp eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="91349-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="91349-111">**IFRS 16 bók**</span><span class="sxs-lookup"><span data-stu-id="91349-111">**IFRS 16 book**</span></span>

<span data-ttu-id="91349-112">IFRS 16 bókin er sett upp þannig að hún samræmist IFRS 16 bókhaldsstaðli.</span><span class="sxs-lookup"><span data-stu-id="91349-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="91349-113">Allar færslur sem eru bókaðar í þessari bók verða bókaðar í sérsniðið lag.</span><span class="sxs-lookup"><span data-stu-id="91349-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="91349-114">Nafn</span><span class="sxs-lookup"><span data-stu-id="91349-114">Name</span></span>                                    | <span data-ttu-id="91349-115">lýsing</span><span class="sxs-lookup"><span data-stu-id="91349-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="91349-116">Gerð bókar</span><span class="sxs-lookup"><span data-stu-id="91349-116">Book type</span></span>                               | <span data-ttu-id="91349-117">Alþjóðlegur reikningsskilastaðall 16</span><span class="sxs-lookup"><span data-stu-id="91349-117">IFRS 16</span></span>        |
| <span data-ttu-id="91349-118">Bókarlýsing</span><span class="sxs-lookup"><span data-stu-id="91349-118">Book description</span></span>                        | <span data-ttu-id="91349-119">Alþjóðlegur reikningsskilastaðall 16</span><span class="sxs-lookup"><span data-stu-id="91349-119">IFRS 16</span></span>        |
| <span data-ttu-id="91349-120">Bókunarlag</span><span class="sxs-lookup"><span data-stu-id="91349-120">Posting Layer</span></span>                           | <span data-ttu-id="91349-121">Sérsniðið lag 1</span><span class="sxs-lookup"><span data-stu-id="91349-121">Custom layer 1</span></span> |
| <span data-ttu-id="91349-122">Gerð leigu</span><span class="sxs-lookup"><span data-stu-id="91349-122">Lease Type</span></span>                              | <span data-ttu-id="91349-123">Finance</span><span class="sxs-lookup"><span data-stu-id="91349-123">Finance</span></span>        |
| <span data-ttu-id="91349-124">Bókhaldsrammi</span><span class="sxs-lookup"><span data-stu-id="91349-124">Accounting Framework</span></span>                    | <span data-ttu-id="91349-125">Alþjóðlegur reikningsskilastaðall 16</span><span class="sxs-lookup"><span data-stu-id="91349-125">IFRS 16</span></span>        |
| <span data-ttu-id="91349-126">Uppsetning leigutíma / nýtingartíma</span><span class="sxs-lookup"><span data-stu-id="91349-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="91349-127">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-127">0.00</span></span>           |
| <span data-ttu-id="91349-128">Uppsetning á núvirði / Gangvirði eignar</span><span class="sxs-lookup"><span data-stu-id="91349-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="91349-129">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-129">0.00</span></span>           |
| <span data-ttu-id="91349-130">Skammtímaþröskuldur</span><span class="sxs-lookup"><span data-stu-id="91349-130">Short-term threshold</span></span>                    | <span data-ttu-id="91349-131">12</span><span class="sxs-lookup"><span data-stu-id="91349-131">12</span></span>             |
| <span data-ttu-id="91349-132">Mörk verðlítillar eignar</span><span class="sxs-lookup"><span data-stu-id="91349-132">Low Value Threshold</span></span>                     | <span data-ttu-id="91349-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="91349-133">5,000.00</span></span>       |
| <span data-ttu-id="91349-134">Greiða lánardrottni</span><span class="sxs-lookup"><span data-stu-id="91349-134">Pay to Vendor</span></span>                           | <span data-ttu-id="91349-135">Ekkert</span><span class="sxs-lookup"><span data-stu-id="91349-135">No</span></span>             |

<span data-ttu-id="91349-136">**Lögboðin bók**</span><span class="sxs-lookup"><span data-stu-id="91349-136">**Statutory book**</span></span>

<span data-ttu-id="91349-137">Lögboðna bókin er reiðufjársbók þar sem fyrirtækið bókar leigukostnaðinn sem reiðufjárupphæðina sem er greidd mánaðarlega fyrir leigu.</span><span class="sxs-lookup"><span data-stu-id="91349-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="91349-138">Þessi bók myndar hvorki afnotarétt af eign né leiguskuldbindingu.</span><span class="sxs-lookup"><span data-stu-id="91349-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="91349-139">Nafn</span><span class="sxs-lookup"><span data-stu-id="91349-139">Name</span></span>                                    | <span data-ttu-id="91349-140">lýsing</span><span class="sxs-lookup"><span data-stu-id="91349-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="91349-141">Gerð bókar</span><span class="sxs-lookup"><span data-stu-id="91349-141">Book type</span></span>                               | <span data-ttu-id="91349-142">Lögboðið</span><span class="sxs-lookup"><span data-stu-id="91349-142">Statutory</span></span>   |
| <span data-ttu-id="91349-143">Bókarlýsing</span><span class="sxs-lookup"><span data-stu-id="91349-143">Book description</span></span>                        | <span data-ttu-id="91349-144">Staðbundið GAAP</span><span class="sxs-lookup"><span data-stu-id="91349-144">Local GAAP</span></span>  |
| <span data-ttu-id="91349-145">Bókunarlag</span><span class="sxs-lookup"><span data-stu-id="91349-145">Posting Layer</span></span>                           | <span data-ttu-id="91349-146">Núverandi</span><span class="sxs-lookup"><span data-stu-id="91349-146">Current</span></span>     |
| <span data-ttu-id="91349-147">Gerð leigu</span><span class="sxs-lookup"><span data-stu-id="91349-147">Lease Type</span></span>                              | <span data-ttu-id="91349-148">Sjálfvirk</span><span class="sxs-lookup"><span data-stu-id="91349-148">Automatic</span></span>   |
| <span data-ttu-id="91349-149">Bókhaldsrammi</span><span class="sxs-lookup"><span data-stu-id="91349-149">Accounting Framework</span></span>                    | <span data-ttu-id="91349-150">Grundvöllur reiðufjár</span><span class="sxs-lookup"><span data-stu-id="91349-150">Cash basis</span></span>  |
| <span data-ttu-id="91349-151">Uppsetning leigutíma / nýtingartíma</span><span class="sxs-lookup"><span data-stu-id="91349-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="91349-152">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-152">0.00</span></span>        |
| <span data-ttu-id="91349-153">Uppsetning á núvirði / Gangvirði eignar</span><span class="sxs-lookup"><span data-stu-id="91349-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="91349-154">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-154">0.00</span></span>        |
| <span data-ttu-id="91349-155">Skammtímaþröskuldur</span><span class="sxs-lookup"><span data-stu-id="91349-155">Short-term threshold</span></span>                    | <span data-ttu-id="91349-156">0</span><span class="sxs-lookup"><span data-stu-id="91349-156">0</span></span>           |
| <span data-ttu-id="91349-157">Mörk verðlítillar eignar</span><span class="sxs-lookup"><span data-stu-id="91349-157">Low Value Threshold</span></span>                     | <span data-ttu-id="91349-158">0</span><span class="sxs-lookup"><span data-stu-id="91349-158">0</span></span>           |
| <span data-ttu-id="91349-159">Greiða lánardrottni</span><span class="sxs-lookup"><span data-stu-id="91349-159">Pay to Vendor</span></span>                           | <span data-ttu-id="91349-160">Ekkert</span><span class="sxs-lookup"><span data-stu-id="91349-160">No</span></span>          |

<span data-ttu-id="91349-161">**Lögboðin bakfærslubók**</span><span class="sxs-lookup"><span data-stu-id="91349-161">**Statutory reversal book**</span></span>

<span data-ttu-id="91349-162">Lögboðin bakfærslubók er sett upp á sama hátt og lögboðna bókin.</span><span class="sxs-lookup"><span data-stu-id="91349-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="91349-163">Nafn</span><span class="sxs-lookup"><span data-stu-id="91349-163">Name</span></span>                                    | <span data-ttu-id="91349-164">lýsing</span><span class="sxs-lookup"><span data-stu-id="91349-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="91349-165">Gerð bókar</span><span class="sxs-lookup"><span data-stu-id="91349-165">Book type</span></span>                               | <span data-ttu-id="91349-166">Lögboðin - Bakfærsla</span><span class="sxs-lookup"><span data-stu-id="91349-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="91349-167">Bókarlýsing</span><span class="sxs-lookup"><span data-stu-id="91349-167">Book description</span></span>                        | <span data-ttu-id="91349-168">Bók til að bakfæra lögboðna bók</span><span class="sxs-lookup"><span data-stu-id="91349-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="91349-169">Bókunarlag</span><span class="sxs-lookup"><span data-stu-id="91349-169">Posting Layer</span></span>                           | <span data-ttu-id="91349-170">Sérsniðið lag 1</span><span class="sxs-lookup"><span data-stu-id="91349-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="91349-171">Gerð leigu</span><span class="sxs-lookup"><span data-stu-id="91349-171">Lease Type</span></span>                              | <span data-ttu-id="91349-172">Sjálfvirk</span><span class="sxs-lookup"><span data-stu-id="91349-172">Automatic</span></span>                      |
| <span data-ttu-id="91349-173">Bókhaldsrammi</span><span class="sxs-lookup"><span data-stu-id="91349-173">Accounting Framework</span></span>                    | <span data-ttu-id="91349-174">Grundvöllur reiðufjár</span><span class="sxs-lookup"><span data-stu-id="91349-174">Cash basis</span></span>                     |
| <span data-ttu-id="91349-175">Uppsetning leigutíma / nýtingartíma</span><span class="sxs-lookup"><span data-stu-id="91349-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="91349-176">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-176">0.00</span></span>                           |
| <span data-ttu-id="91349-177">Uppsetning á núvirði / Gangvirði eignar</span><span class="sxs-lookup"><span data-stu-id="91349-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="91349-178">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-178">0.00</span></span>                           |
| <span data-ttu-id="91349-179">Skammtímaþröskuldur</span><span class="sxs-lookup"><span data-stu-id="91349-179">Short-term threshold</span></span>                    | <span data-ttu-id="91349-180">0</span><span class="sxs-lookup"><span data-stu-id="91349-180">0</span></span>                              |
| <span data-ttu-id="91349-181">Mörk verðlítillar eignar</span><span class="sxs-lookup"><span data-stu-id="91349-181">Low Value Threshold</span></span>                     | <span data-ttu-id="91349-182">0</span><span class="sxs-lookup"><span data-stu-id="91349-182">0</span></span>                              |
| <span data-ttu-id="91349-183">Greiða lánardrottni</span><span class="sxs-lookup"><span data-stu-id="91349-183">Pay to Vendor</span></span>                           | <span data-ttu-id="91349-184">Ekkert</span><span class="sxs-lookup"><span data-stu-id="91349-184">No</span></span>                             |

<span data-ttu-id="91349-185">Í þessu dæmi er búið að stofna leigusamning með eftirfarandi stillingar á flipunum **Almennt** og **Greiðsluáætlunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="91349-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="91349-186">**Almennt**</span><span class="sxs-lookup"><span data-stu-id="91349-186">**General tab**</span></span>

| <span data-ttu-id="91349-187">Svæði</span><span class="sxs-lookup"><span data-stu-id="91349-187">Field</span></span>                      | <span data-ttu-id="91349-188">Virði</span><span class="sxs-lookup"><span data-stu-id="91349-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="91349-189">Vextir á nýju lánsfé</span><span class="sxs-lookup"><span data-stu-id="91349-189">Incremental borrowing rate</span></span> | <span data-ttu-id="91349-190">5%</span><span class="sxs-lookup"><span data-stu-id="91349-190">5%</span></span>               |
| <span data-ttu-id="91349-191">Upphafsdagsetning</span><span class="sxs-lookup"><span data-stu-id="91349-191">Commencement date</span></span>          | <span data-ttu-id="91349-192">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="91349-192">1/1/2020</span></span>         |
| <span data-ttu-id="91349-193">Leigusamningsflokkur</span><span class="sxs-lookup"><span data-stu-id="91349-193">Lease group</span></span>                | <span data-ttu-id="91349-194">Byggingar</span><span class="sxs-lookup"><span data-stu-id="91349-194">Buildings</span></span>        |
| <span data-ttu-id="91349-195">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="91349-195">Vendor</span></span>                     | <span data-ttu-id="91349-196">1001</span><span class="sxs-lookup"><span data-stu-id="91349-196">1001</span></span>             |
| <span data-ttu-id="91349-197">Gangvirði eignarinnar</span><span class="sxs-lookup"><span data-stu-id="91349-197">Fair value of the asset</span></span>    | <span data-ttu-id="91349-198">245,000</span><span class="sxs-lookup"><span data-stu-id="91349-198">245,000</span></span>          |
| <span data-ttu-id="91349-199">Nýtingartími eignar</span><span class="sxs-lookup"><span data-stu-id="91349-199">Asset useful life</span></span>          | <span data-ttu-id="91349-200">120</span><span class="sxs-lookup"><span data-stu-id="91349-200">120</span></span>              |
| <span data-ttu-id="91349-201">Tegund afborgunar</span><span class="sxs-lookup"><span data-stu-id="91349-201">Annuity type</span></span>               | <span data-ttu-id="91349-202">Venjulegar afborganir</span><span class="sxs-lookup"><span data-stu-id="91349-202">Ordinary annuity</span></span> |
| <span data-ttu-id="91349-203">Samsett tímabil</span><span class="sxs-lookup"><span data-stu-id="91349-203">Compounding interval</span></span>       | <span data-ttu-id="91349-204">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="91349-204">Monthly</span></span>          |

<span data-ttu-id="91349-205">**Flipi greiðsluáætlunarlína**</span><span class="sxs-lookup"><span data-stu-id="91349-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="91349-206">Svæði</span><span class="sxs-lookup"><span data-stu-id="91349-206">Field</span></span>             | <span data-ttu-id="91349-207">Virði</span><span class="sxs-lookup"><span data-stu-id="91349-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="91349-208">Upphafsdagsetning</span><span class="sxs-lookup"><span data-stu-id="91349-208">Start date</span></span>        | <span data-ttu-id="91349-209">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="91349-209">1/1/2020</span></span>   |
| <span data-ttu-id="91349-210">Tímabil</span><span class="sxs-lookup"><span data-stu-id="91349-210">Period interval</span></span>   | <span data-ttu-id="91349-211">Mánuðir</span><span class="sxs-lookup"><span data-stu-id="91349-211">Months</span></span>     |
| <span data-ttu-id="91349-212">Tímabil</span><span class="sxs-lookup"><span data-stu-id="91349-212">Periods</span></span>           | <span data-ttu-id="91349-213">24</span><span class="sxs-lookup"><span data-stu-id="91349-213">24</span></span>         |
| <span data-ttu-id="91349-214">Lokadagsetning</span><span class="sxs-lookup"><span data-stu-id="91349-214">End date</span></span>          | <span data-ttu-id="91349-215">31/12/2020</span><span class="sxs-lookup"><span data-stu-id="91349-215">12/31/2020</span></span> |
| <span data-ttu-id="91349-216">Greiðslutíðni</span><span class="sxs-lookup"><span data-stu-id="91349-216">Payment frequency</span></span> | <span data-ttu-id="91349-217">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="91349-217">Monthly</span></span>    |
| <span data-ttu-id="91349-218">Upphæð greiðslu</span><span class="sxs-lookup"><span data-stu-id="91349-218">Payment amount</span></span>    | <span data-ttu-id="91349-219">1.000</span><span class="sxs-lookup"><span data-stu-id="91349-219">1,000</span></span>      |

<span data-ttu-id="91349-220">Til að gera ráð fyrir þessum leigusamningi samkvæmt tveimur römmum er notað núverandi bókunarlag og sérsniðið bókunarlag.</span><span class="sxs-lookup"><span data-stu-id="91349-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="91349-221">Eftirfarandi tafla sýnir dæmi um hverja áskilda bókarfærslu til að birta fjármál á réttan hátt samkvæmt hverjum reikningsskilastaðli fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="91349-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="91349-222">Ítarleg lýsing á hverri bókarfærslu fyrir fyrsta mánuð leigusamningsins er veitt eftir á.</span><span class="sxs-lookup"><span data-stu-id="91349-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="91349-223">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="91349-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="91349-224">lýsing</span><span class="sxs-lookup"><span data-stu-id="91349-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="91349-225">Lögboðin bók (núverandi lag)</span><span class="sxs-lookup"><span data-stu-id="91349-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="91349-226">Núverandi lag samtals</span><span class="sxs-lookup"><span data-stu-id="91349-226">Current layer total</span></span></th>
<th><span data-ttu-id="91349-227">Bakfærslubók (sérsniðið lag)</span><span class="sxs-lookup"><span data-stu-id="91349-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="91349-228">IFRS 16 bók (sérsniðið lag)</span><span class="sxs-lookup"><span data-stu-id="91349-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="91349-229">Núgildandi lag + sérsniðið lag alls</span><span class="sxs-lookup"><span data-stu-id="91349-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="91349-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="91349-230">JE-100</span></span></th>
<th><span data-ttu-id="91349-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="91349-231">JE-110</span></span></th>
<th><span data-ttu-id="91349-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="91349-232">JE-120</span></span></th>
<th><span data-ttu-id="91349-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="91349-233">JE-130</span></span></th>
<th><span data-ttu-id="91349-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="91349-234">JE-140</span></span></th>
<th><span data-ttu-id="91349-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="91349-235">JE-150</span></span></th>
<th><span data-ttu-id="91349-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="91349-236">JE-160</span></span></th>
<th><span data-ttu-id="91349-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="91349-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="91349-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91349-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="91349-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91349-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="91349-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91349-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="91349-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91349-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="91349-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91349-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="91349-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91349-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="91349-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91349-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="91349-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91349-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="91349-246">1</span><span class="sxs-lookup"><span data-stu-id="91349-246">1</span></span></td>
<td><span data-ttu-id="91349-247">Leigukostnaður</span><span class="sxs-lookup"><span data-stu-id="91349-247">Lease expense</span></span></td>
<td><span data-ttu-id="91349-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91349-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91349-249">1,000.00</span></span></td>
<td><span data-ttu-id="91349-250">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="91349-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-251">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-252">2</span><span class="sxs-lookup"><span data-stu-id="91349-252">2</span></span></td>
<td><span data-ttu-id="91349-253">Bankaþóknun</span><span class="sxs-lookup"><span data-stu-id="91349-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="91349-254">3.00</span><span class="sxs-lookup"><span data-stu-id="91349-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="91349-255">3.00</span><span class="sxs-lookup"><span data-stu-id="91349-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-256">3.00</span><span class="sxs-lookup"><span data-stu-id="91349-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-257">3</span><span class="sxs-lookup"><span data-stu-id="91349-257">3</span></span></td>
<td><span data-ttu-id="91349-258">VSK útgjöld</span><span class="sxs-lookup"><span data-stu-id="91349-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="91349-259">5.00</span><span class="sxs-lookup"><span data-stu-id="91349-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="91349-260">5.00</span><span class="sxs-lookup"><span data-stu-id="91349-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-261">5.00</span><span class="sxs-lookup"><span data-stu-id="91349-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-262">4</span><span class="sxs-lookup"><span data-stu-id="91349-262">4</span></span></td>
<td><span data-ttu-id="91349-263">Millireikningur</span><span class="sxs-lookup"><span data-stu-id="91349-263">Clearing account</span></span></td>
<td><span data-ttu-id="91349-264">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="91349-264">-1,000.00</span></span></td>
<td><span data-ttu-id="91349-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91349-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="91349-266">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-266">0.00</span></span></td>
<td><span data-ttu-id="91349-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91349-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="91349-268">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="91349-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-269">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-270">5</span><span class="sxs-lookup"><span data-stu-id="91349-270">5</span></span></td>
<td><span data-ttu-id="91349-271">Viðskiptaskuldir</span><span class="sxs-lookup"><span data-stu-id="91349-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="91349-272">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="91349-272">-1,008.00</span></span></td>
<td><span data-ttu-id="91349-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="91349-273">1,008.00</span></span></td>
<td><span data-ttu-id="91349-274">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-275">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-276">6</span><span class="sxs-lookup"><span data-stu-id="91349-276">6</span></span></td>
<td><span data-ttu-id="91349-277">Afnotaréttur af eign</span><span class="sxs-lookup"><span data-stu-id="91349-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-278">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="91349-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="91349-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="91349-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-281">7</span><span class="sxs-lookup"><span data-stu-id="91349-281">7</span></span></td>
<td><span data-ttu-id="91349-282">Skylda fjármögnunarleigusamnings</span><span class="sxs-lookup"><span data-stu-id="91349-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-283">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="91349-284">-22.794,00</span><span class="sxs-lookup"><span data-stu-id="91349-284">-22,794.00</span></span></td>
<td><span data-ttu-id="91349-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91349-285">1,000.00</span></span></td>
<td><span data-ttu-id="91349-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="91349-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="91349-287">-21.888,87</span><span class="sxs-lookup"><span data-stu-id="91349-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-288">8</span><span class="sxs-lookup"><span data-stu-id="91349-288">8</span></span></td>
<td><span data-ttu-id="91349-289">Vaxtakostnaður</span><span class="sxs-lookup"><span data-stu-id="91349-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-290">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-291">94.97</span><span class="sxs-lookup"><span data-stu-id="91349-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="91349-292">94.97</span><span class="sxs-lookup"><span data-stu-id="91349-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-293">9</span><span class="sxs-lookup"><span data-stu-id="91349-293">9</span></span></td>
<td><span data-ttu-id="91349-294">Innlausn</span><span class="sxs-lookup"><span data-stu-id="91349-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-295">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="91349-295">-1,008.00</span></span></td>
<td><span data-ttu-id="91349-296">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="91349-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-297">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="91349-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-298">10</span><span class="sxs-lookup"><span data-stu-id="91349-298">10</span></span></td>
<td><span data-ttu-id="91349-299">Afskriftakostnaður</span><span class="sxs-lookup"><span data-stu-id="91349-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-300">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-301">949.75</span><span class="sxs-lookup"><span data-stu-id="91349-301">949.75</span></span></td>
<td><span data-ttu-id="91349-302">949.75</span><span class="sxs-lookup"><span data-stu-id="91349-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-303">11</span><span class="sxs-lookup"><span data-stu-id="91349-303">11</span></span></td>
<td><span data-ttu-id="91349-304">Uppsöfnuð afskrift</span><span class="sxs-lookup"><span data-stu-id="91349-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-305">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="91349-306">-949.75</span></span></td>
<td><span data-ttu-id="91349-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="91349-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="91349-308">Eins og taflan hér á undan sýnir eru þrjár bækur áskildar til skráningar bæði samkvæmt lögboðinni skýrslugerð og IFRS-skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="91349-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="91349-309">Lögboðna bókin skráir leigugreiðsluna samkvæmt reglum fyrir reiðufjársbókhald samkvæmt núverandi lagi.</span><span class="sxs-lookup"><span data-stu-id="91349-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="91349-310">Lögboðna bakfærslubókin bakfærir lögboðnu bókarfærslurnar.</span><span class="sxs-lookup"><span data-stu-id="91349-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="91349-311">IFRS 16 bókin stofnar áskildar bókarfærslur samkvæmt IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="91349-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="91349-312">Aðeins þarf að færa inn leigu einu sinni.</span><span class="sxs-lookup"><span data-stu-id="91349-312">You must enter a lease only one time.</span></span> <span data-ttu-id="91349-313">Síðan er hægt að opna síðuna **Bækur** til að skoða allar bækurnar sem eru tengdar leigusamningnum.</span><span class="sxs-lookup"><span data-stu-id="91349-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="91349-314">Þegar búið er að stofna bækurnar verður að tengja allar þrjár við sömu leiguskrána.</span><span class="sxs-lookup"><span data-stu-id="91349-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="91349-315">Fyrsta bókarfærslan skráir kostnað leigusamningsins samkvæmt lögboðnu bókinni.</span><span class="sxs-lookup"><span data-stu-id="91349-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="91349-316">Hægt er að stofna greiðslurnar annaðhvort í runu eða með því að velja greiðsluáætlunina í lögboðnu bókinni.</span><span class="sxs-lookup"><span data-stu-id="91349-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="91349-317">Í þessu dæmi er eftirfarandi bókarfærsla gerð fyrir lögboðnu bókina úr greiðsluáætlun.</span><span class="sxs-lookup"><span data-stu-id="91349-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="91349-318">Leigugreiðsla – 31/1/2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="91349-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="91349-319">Lykilgerð</span><span class="sxs-lookup"><span data-stu-id="91349-319">Account type</span></span> | <span data-ttu-id="91349-320">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="91349-320">Account number</span></span> | <span data-ttu-id="91349-321">Lag</span><span class="sxs-lookup"><span data-stu-id="91349-321">Layer</span></span>   | <span data-ttu-id="91349-322">Lýsing á lykli</span><span class="sxs-lookup"><span data-stu-id="91349-322">Account description</span></span> | <span data-ttu-id="91349-323">Debet</span><span class="sxs-lookup"><span data-stu-id="91349-323">Debit</span></span>    | <span data-ttu-id="91349-324">Kredit</span><span class="sxs-lookup"><span data-stu-id="91349-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="91349-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="91349-325">Ledger</span></span>       | <span data-ttu-id="91349-326">1</span><span class="sxs-lookup"><span data-stu-id="91349-326">1</span></span>              | <span data-ttu-id="91349-327">Núverandi</span><span class="sxs-lookup"><span data-stu-id="91349-327">Current</span></span> | <span data-ttu-id="91349-328">Leigukostnaður</span><span class="sxs-lookup"><span data-stu-id="91349-328">Lease expense</span></span>       | <span data-ttu-id="91349-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91349-329">1,000.00</span></span> |          |
| <span data-ttu-id="91349-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="91349-330">Ledger</span></span>       | <span data-ttu-id="91349-331">4</span><span class="sxs-lookup"><span data-stu-id="91349-331">4</span></span>              | <span data-ttu-id="91349-332">Núverandi</span><span class="sxs-lookup"><span data-stu-id="91349-332">Current</span></span> | <span data-ttu-id="91349-333">Millireikningur</span><span class="sxs-lookup"><span data-stu-id="91349-333">Clearing account</span></span>    |          | <span data-ttu-id="91349-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91349-334">1,000.00</span></span> |

<span data-ttu-id="91349-335">Afgreiðslumaður viðskiptaskulda notar staðlaða Dynamics 365-virkni til að stofna reikning til að greiða fyrir leigusamning utan eignarleigu.</span><span class="sxs-lookup"><span data-stu-id="91349-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="91349-336">Hins vegar, í stað þess að velja **Leigukostnað** sem debetlykil velur afgreiðslumaður viðskiptaskulda millireikning til að mynda eftirfarandi færslu.</span><span class="sxs-lookup"><span data-stu-id="91349-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="91349-337">AP-ferli – 31/1/2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="91349-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="91349-338">Lykilgerð</span><span class="sxs-lookup"><span data-stu-id="91349-338">Account type</span></span> | <span data-ttu-id="91349-339">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="91349-339">Account number</span></span> | <span data-ttu-id="91349-340">Lag</span><span class="sxs-lookup"><span data-stu-id="91349-340">Layer</span></span>   | <span data-ttu-id="91349-341">Lýsing á lykli</span><span class="sxs-lookup"><span data-stu-id="91349-341">Account description</span></span> | <span data-ttu-id="91349-342">Debet</span><span class="sxs-lookup"><span data-stu-id="91349-342">Debit</span></span>    | <span data-ttu-id="91349-343">Kredit</span><span class="sxs-lookup"><span data-stu-id="91349-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="91349-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="91349-344">Ledger</span></span>       | <span data-ttu-id="91349-345">4</span><span class="sxs-lookup"><span data-stu-id="91349-345">4</span></span>              | <span data-ttu-id="91349-346">Núverandi</span><span class="sxs-lookup"><span data-stu-id="91349-346">Current</span></span> | <span data-ttu-id="91349-347">Millireikningur</span><span class="sxs-lookup"><span data-stu-id="91349-347">Clearing account</span></span>    | <span data-ttu-id="91349-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91349-348">1,000.00</span></span> |          |
| <span data-ttu-id="91349-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="91349-349">Ledger</span></span>       | <span data-ttu-id="91349-350">2</span><span class="sxs-lookup"><span data-stu-id="91349-350">2</span></span>              | <span data-ttu-id="91349-351">Núverandi</span><span class="sxs-lookup"><span data-stu-id="91349-351">Current</span></span> | <span data-ttu-id="91349-352">Bankaþóknun</span><span class="sxs-lookup"><span data-stu-id="91349-352">Bank fee</span></span>            | <span data-ttu-id="91349-353">3.00</span><span class="sxs-lookup"><span data-stu-id="91349-353">3.00</span></span>     |          |
| <span data-ttu-id="91349-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="91349-354">Ledger</span></span>       | <span data-ttu-id="91349-355">3</span><span class="sxs-lookup"><span data-stu-id="91349-355">3</span></span>              | <span data-ttu-id="91349-356">Núverandi</span><span class="sxs-lookup"><span data-stu-id="91349-356">Current</span></span> | <span data-ttu-id="91349-357">VSK útgjöld</span><span class="sxs-lookup"><span data-stu-id="91349-357">VAT expense</span></span>         | <span data-ttu-id="91349-358">5.00</span><span class="sxs-lookup"><span data-stu-id="91349-358">5.00</span></span>     |          |
| <span data-ttu-id="91349-359">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="91349-359">Vendor</span></span>       | <span data-ttu-id="91349-360">5</span><span class="sxs-lookup"><span data-stu-id="91349-360">5</span></span>              | <span data-ttu-id="91349-361">Núverandi</span><span class="sxs-lookup"><span data-stu-id="91349-361">Current</span></span> | <span data-ttu-id="91349-362">Viðskiptaskuldir</span><span class="sxs-lookup"><span data-stu-id="91349-362">Accounts payable</span></span>    |          | <span data-ttu-id="91349-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="91349-363">1,008.00</span></span> |

<span data-ttu-id="91349-364">Þegar yfirlitið er gefið út til lánardrottins er reglubundna greiðsluferlinu fylgt eftir.</span><span class="sxs-lookup"><span data-stu-id="91349-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="91349-365">Eftirfarandi bókarfærsla er mynduð við þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="91349-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="91349-366">Reiðufjárgreiðsla – 31/1/2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="91349-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="91349-367">Lykilgerð</span><span class="sxs-lookup"><span data-stu-id="91349-367">Account type</span></span> | <span data-ttu-id="91349-368">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="91349-368">Account number</span></span> | <span data-ttu-id="91349-369">Lag</span><span class="sxs-lookup"><span data-stu-id="91349-369">Layer</span></span>   | <span data-ttu-id="91349-370">Lýsing á lykli</span><span class="sxs-lookup"><span data-stu-id="91349-370">Account description</span></span> | <span data-ttu-id="91349-371">Debet</span><span class="sxs-lookup"><span data-stu-id="91349-371">Debit</span></span>    | <span data-ttu-id="91349-372">Kredit</span><span class="sxs-lookup"><span data-stu-id="91349-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="91349-373">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="91349-373">Vendor</span></span>       | <span data-ttu-id="91349-374">5</span><span class="sxs-lookup"><span data-stu-id="91349-374">5</span></span>              | <span data-ttu-id="91349-375">Núverandi</span><span class="sxs-lookup"><span data-stu-id="91349-375">Current</span></span> | <span data-ttu-id="91349-376">Viðskiptaskuldir</span><span class="sxs-lookup"><span data-stu-id="91349-376">Accounts Payable</span></span>    | <span data-ttu-id="91349-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="91349-377">1,008.00</span></span> |          |
| <span data-ttu-id="91349-378">Banki</span><span class="sxs-lookup"><span data-stu-id="91349-378">Bank</span></span>         | <span data-ttu-id="91349-379">9</span><span class="sxs-lookup"><span data-stu-id="91349-379">9</span></span>              | <span data-ttu-id="91349-380">Núverandi</span><span class="sxs-lookup"><span data-stu-id="91349-380">Current</span></span> | <span data-ttu-id="91349-381">Innlausn</span><span class="sxs-lookup"><span data-stu-id="91349-381">Cash</span></span>                |          | <span data-ttu-id="91349-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="91349-382">1,008.00</span></span> |

<span data-ttu-id="91349-383">Á þessu stigi er búið að reikna þetta út samkvæmt lögboðnum skýrslukröfum og hægt er að búa til prófjöfnuð með því að nota núgildandi lag.</span><span class="sxs-lookup"><span data-stu-id="91349-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="91349-384">Kerfið skilar prófjöfnuði sem inniheldur eftirfarandi tölur.</span><span class="sxs-lookup"><span data-stu-id="91349-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="91349-385">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="91349-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="91349-386">lýsing</span><span class="sxs-lookup"><span data-stu-id="91349-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="91349-387">Lögboðin bók (núverandi lag)</span><span class="sxs-lookup"><span data-stu-id="91349-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="91349-388">Núverandi lag samtals</span><span class="sxs-lookup"><span data-stu-id="91349-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="91349-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="91349-389">JE-100</span></span></th>
<th><span data-ttu-id="91349-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="91349-390">JE-110</span></span></th>
<th><span data-ttu-id="91349-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="91349-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="91349-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91349-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="91349-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91349-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="91349-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="91349-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="91349-395">1</span><span class="sxs-lookup"><span data-stu-id="91349-395">1</span></span></td>
<td><span data-ttu-id="91349-396">Leigukostnaður</span><span class="sxs-lookup"><span data-stu-id="91349-396">Lease expense</span></span></td>
<td><span data-ttu-id="91349-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91349-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91349-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-399">2</span><span class="sxs-lookup"><span data-stu-id="91349-399">2</span></span></td>
<td><span data-ttu-id="91349-400">Bankaþóknun</span><span class="sxs-lookup"><span data-stu-id="91349-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="91349-401">3.00</span><span class="sxs-lookup"><span data-stu-id="91349-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="91349-402">3.00</span><span class="sxs-lookup"><span data-stu-id="91349-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-403">3</span><span class="sxs-lookup"><span data-stu-id="91349-403">3</span></span></td>
<td><span data-ttu-id="91349-404">VSK útgjöld</span><span class="sxs-lookup"><span data-stu-id="91349-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="91349-405">5.00</span><span class="sxs-lookup"><span data-stu-id="91349-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="91349-406">5.00</span><span class="sxs-lookup"><span data-stu-id="91349-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-407">4</span><span class="sxs-lookup"><span data-stu-id="91349-407">4</span></span></td>
<td><span data-ttu-id="91349-408">Millireikningur</span><span class="sxs-lookup"><span data-stu-id="91349-408">Clearing account</span></span></td>
<td><span data-ttu-id="91349-409">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="91349-409">-1,000.00</span></span></td>
<td><span data-ttu-id="91349-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91349-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="91349-411">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-412">5</span><span class="sxs-lookup"><span data-stu-id="91349-412">5</span></span></td>
<td><span data-ttu-id="91349-413">Viðskiptaskuldir</span><span class="sxs-lookup"><span data-stu-id="91349-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="91349-414">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="91349-414">-1,008.00</span></span></td>
<td><span data-ttu-id="91349-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="91349-415">1,008.00</span></span></td>
<td><span data-ttu-id="91349-416">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-417">6</span><span class="sxs-lookup"><span data-stu-id="91349-417">6</span></span></td>
<td><span data-ttu-id="91349-418">Afnotaréttur af eign</span><span class="sxs-lookup"><span data-stu-id="91349-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-419">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-420">7</span><span class="sxs-lookup"><span data-stu-id="91349-420">7</span></span></td>
<td><span data-ttu-id="91349-421">Skylda fjármögnunarleigusamnings</span><span class="sxs-lookup"><span data-stu-id="91349-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-422">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-423">8</span><span class="sxs-lookup"><span data-stu-id="91349-423">8</span></span></td>
<td><span data-ttu-id="91349-424">Vaxtakostnaður</span><span class="sxs-lookup"><span data-stu-id="91349-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-425">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-426">9</span><span class="sxs-lookup"><span data-stu-id="91349-426">9</span></span></td>
<td><span data-ttu-id="91349-427">Innlausn</span><span class="sxs-lookup"><span data-stu-id="91349-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-428">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="91349-428">-1,008.00</span></span></td>
<td><span data-ttu-id="91349-429">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="91349-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-430">10</span><span class="sxs-lookup"><span data-stu-id="91349-430">10</span></span></td>
<td><span data-ttu-id="91349-431">Afskriftakostnaður</span><span class="sxs-lookup"><span data-stu-id="91349-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-432">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="91349-433">11</span><span class="sxs-lookup"><span data-stu-id="91349-433">11</span></span></td>
<td><span data-ttu-id="91349-434">Uppsöfnuð afskrift</span><span class="sxs-lookup"><span data-stu-id="91349-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="91349-435">0,00</span><span class="sxs-lookup"><span data-stu-id="91349-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="91349-436">Ef ætlunin er að nota tölur IFRS 16 til að keyra sama prófjöfnuð verður að bakfæra færslur lögboðinnar færslubókar og bóka IFRS 16-færslurnar.</span><span class="sxs-lookup"><span data-stu-id="91349-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="91349-437">Til að bakfæra lögboðnu færslubókarfærslur, inniheldur þetta dæmi lögboðna bakfærslubók með sömu uppsetningu og lögboðin færslubók en með gagnstæða bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="91349-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="91349-438">Lögboðna bókin er t.d. *skuldfærð* kostnaðarlykill leigusamnings en bakfærslubókin *kreditfærir* slíkan lykil.</span><span class="sxs-lookup"><span data-stu-id="91349-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="91349-439">Þessi vensl eru skilgreind á auðveldan hátt í bókunarlyklum eignarleigu á síðunni **Færibreytur fyrir eignarleigu** (**Eignarleiga \> Uppsetning \> Færibreytur fyrir eignarleigu**).</span><span class="sxs-lookup"><span data-stu-id="91349-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="91349-440">Þegar sama ferlið sem notað var fyrir lögboðnu bókina er notað fyrir bakfærslubókina er eftirfarandi bókarfærsla mynduð.</span><span class="sxs-lookup"><span data-stu-id="91349-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="91349-441">Munurinn er sá að bakfærslubókin bókar bakfærslurnar úr lögboðnu bókinni.</span><span class="sxs-lookup"><span data-stu-id="91349-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="91349-442">Bakfærslurnar eru einnig gerðar í sérstillta laginu.</span><span class="sxs-lookup"><span data-stu-id="91349-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="91349-443">Þegar verið er að keyra prófjöfnuð á núverandi lagi eru færslur bakfærslubókarinnar ekki teknar með.</span><span class="sxs-lookup"><span data-stu-id="91349-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="91349-444">Leigugreiðsla – 31/1/2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="91349-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="91349-445">Lykilgerð</span><span class="sxs-lookup"><span data-stu-id="91349-445">Account type</span></span> | <span data-ttu-id="91349-446">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="91349-446">Account number</span></span> | <span data-ttu-id="91349-447">Lag</span><span class="sxs-lookup"><span data-stu-id="91349-447">Layer</span></span>  | <span data-ttu-id="91349-448">Lýsing á lykli</span><span class="sxs-lookup"><span data-stu-id="91349-448">Account description</span></span> | <span data-ttu-id="91349-449">Debet</span><span class="sxs-lookup"><span data-stu-id="91349-449">Debit</span></span>    | <span data-ttu-id="91349-450">Kredit</span><span class="sxs-lookup"><span data-stu-id="91349-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="91349-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="91349-451">Ledger</span></span>       | <span data-ttu-id="91349-452">4</span><span class="sxs-lookup"><span data-stu-id="91349-452">4</span></span>              | <span data-ttu-id="91349-453">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="91349-453">Custom</span></span> | <span data-ttu-id="91349-454">Millireikningur</span><span class="sxs-lookup"><span data-stu-id="91349-454">Clearing account</span></span>    | <span data-ttu-id="91349-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91349-455">1,000.00</span></span> |          |
| <span data-ttu-id="91349-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="91349-456">Ledger</span></span>       | <span data-ttu-id="91349-457">1</span><span class="sxs-lookup"><span data-stu-id="91349-457">1</span></span>              | <span data-ttu-id="91349-458">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="91349-458">Custom</span></span> | <span data-ttu-id="91349-459">Leigukostnaður</span><span class="sxs-lookup"><span data-stu-id="91349-459">Lease expense</span></span>       |          | <span data-ttu-id="91349-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91349-460">1,000.00</span></span> |

<span data-ttu-id="91349-461">Nú þegar búið er að útiloka færslur lögboðnu bókarinnar verður að bóka allar áskildar bókarfærslur samkvæmt IFRS 16 í IFRS 16-bókinni.</span><span class="sxs-lookup"><span data-stu-id="91349-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="91349-462">Þessar færslur fela í sér fyrstu viðurkenningu á afnotarétt af eign og ábyrgðina og færslu vaxta og afskrifta.</span><span class="sxs-lookup"><span data-stu-id="91349-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="91349-463">Upphafleg viðurkenning – 1/1/2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="91349-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="91349-464">Lykilgerð</span><span class="sxs-lookup"><span data-stu-id="91349-464">Account type</span></span> | <span data-ttu-id="91349-465">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="91349-465">Account number</span></span> | <span data-ttu-id="91349-466">Lag</span><span class="sxs-lookup"><span data-stu-id="91349-466">Layer</span></span>  | <span data-ttu-id="91349-467">Lýsing á lykli</span><span class="sxs-lookup"><span data-stu-id="91349-467">Account description</span></span>      | <span data-ttu-id="91349-468">Debet</span><span class="sxs-lookup"><span data-stu-id="91349-468">Debit</span></span>     | <span data-ttu-id="91349-469">Kredit</span><span class="sxs-lookup"><span data-stu-id="91349-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="91349-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="91349-470">Ledger</span></span>       | <span data-ttu-id="91349-471">6</span><span class="sxs-lookup"><span data-stu-id="91349-471">6</span></span>              | <span data-ttu-id="91349-472">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="91349-472">Custom</span></span> | <span data-ttu-id="91349-473">Afnotaréttur af eign</span><span class="sxs-lookup"><span data-stu-id="91349-473">ROU Asset</span></span>                | <span data-ttu-id="91349-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="91349-474">22,793.90</span></span> |           |
| <span data-ttu-id="91349-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="91349-475">Ledger</span></span>       | <span data-ttu-id="91349-476">7</span><span class="sxs-lookup"><span data-stu-id="91349-476">7</span></span>              | <span data-ttu-id="91349-477">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="91349-477">Custom</span></span> | <span data-ttu-id="91349-478">Skylda fjármögnunarleigusamnings</span><span class="sxs-lookup"><span data-stu-id="91349-478">Finance lease obligation</span></span> |           | <span data-ttu-id="91349-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="91349-479">22,793.90</span></span> |

<span data-ttu-id="91349-480">Leigugreiðslan er bókuð á sama hátt og aðrar leigugreiðslur.</span><span class="sxs-lookup"><span data-stu-id="91349-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="91349-481">Ástæðan fyrir því að nota millireikning er að tryggja að reiðufé sé aðeins kreditfært í eitt skipti.</span><span class="sxs-lookup"><span data-stu-id="91349-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="91349-482">Leigugreiðsla – 31/1/2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="91349-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="91349-483">Lykilgerð</span><span class="sxs-lookup"><span data-stu-id="91349-483">Account type</span></span> | <span data-ttu-id="91349-484">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="91349-484">Account number</span></span> | <span data-ttu-id="91349-485">Lag</span><span class="sxs-lookup"><span data-stu-id="91349-485">Layer</span></span>  | <span data-ttu-id="91349-486">Lýsing á lykli</span><span class="sxs-lookup"><span data-stu-id="91349-486">Account description</span></span>      | <span data-ttu-id="91349-487">Debet</span><span class="sxs-lookup"><span data-stu-id="91349-487">Debit</span></span>    | <span data-ttu-id="91349-488">Kredit</span><span class="sxs-lookup"><span data-stu-id="91349-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="91349-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="91349-489">Ledger</span></span>       | <span data-ttu-id="91349-490">7</span><span class="sxs-lookup"><span data-stu-id="91349-490">7</span></span>              | <span data-ttu-id="91349-491">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="91349-491">Custom</span></span> | <span data-ttu-id="91349-492">Skylda fjármögnunarleigusamnings</span><span class="sxs-lookup"><span data-stu-id="91349-492">Finance lease obligation</span></span> | <span data-ttu-id="91349-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91349-493">1,000.00</span></span> |          |
| <span data-ttu-id="91349-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="91349-494">Ledger</span></span>       | <span data-ttu-id="91349-495">4</span><span class="sxs-lookup"><span data-stu-id="91349-495">4</span></span>              | <span data-ttu-id="91349-496">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="91349-496">Custom</span></span> | <span data-ttu-id="91349-497">Millireikningur</span><span class="sxs-lookup"><span data-stu-id="91349-497">Clearing account</span></span>         |          | <span data-ttu-id="91349-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="91349-498">1,000.00</span></span> |

<span data-ttu-id="91349-499">Bókarfærsla vaxtakostnaðar er mynduð úr afskriftaráætlun leiguskuldbindingar.</span><span class="sxs-lookup"><span data-stu-id="91349-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="91349-500">Vaxtakostnaður – 31/1/2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="91349-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="91349-501">Lykilgerð</span><span class="sxs-lookup"><span data-stu-id="91349-501">Account type</span></span> | <span data-ttu-id="91349-502">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="91349-502">Account number</span></span> | <span data-ttu-id="91349-503">Lag</span><span class="sxs-lookup"><span data-stu-id="91349-503">Layer</span></span>  | <span data-ttu-id="91349-504">Lýsing á lykli</span><span class="sxs-lookup"><span data-stu-id="91349-504">Account description</span></span>      | <span data-ttu-id="91349-505">Debet</span><span class="sxs-lookup"><span data-stu-id="91349-505">Debit</span></span> | <span data-ttu-id="91349-506">Kredit</span><span class="sxs-lookup"><span data-stu-id="91349-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="91349-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="91349-507">Ledger</span></span>       | <span data-ttu-id="91349-508">8</span><span class="sxs-lookup"><span data-stu-id="91349-508">8</span></span>              | <span data-ttu-id="91349-509">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="91349-509">Custom</span></span> | <span data-ttu-id="91349-510">Vaxtakostnaður</span><span class="sxs-lookup"><span data-stu-id="91349-510">Interest expense</span></span>         | <span data-ttu-id="91349-511">94.97</span><span class="sxs-lookup"><span data-stu-id="91349-511">94.97</span></span> |        |
| <span data-ttu-id="91349-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="91349-512">Ledger</span></span>       | <span data-ttu-id="91349-513">7</span><span class="sxs-lookup"><span data-stu-id="91349-513">7</span></span>              | <span data-ttu-id="91349-514">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="91349-514">Custom</span></span> | <span data-ttu-id="91349-515">Skylda fjármögnunarleigusamnings</span><span class="sxs-lookup"><span data-stu-id="91349-515">Finance lease obligation</span></span> |       | <span data-ttu-id="91349-516">94.97</span><span class="sxs-lookup"><span data-stu-id="91349-516">94.97</span></span>  |

<span data-ttu-id="91349-517">Bókarfærsla afskriftakostnaðar er mynduð úr afskriftaráætlun eignar.</span><span class="sxs-lookup"><span data-stu-id="91349-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="91349-518">Afskriftarkostnaður – 1/31/2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="91349-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="91349-519">Lykilgerð</span><span class="sxs-lookup"><span data-stu-id="91349-519">Account type</span></span> | <span data-ttu-id="91349-520">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="91349-520">Account number</span></span> | <span data-ttu-id="91349-521">Lag</span><span class="sxs-lookup"><span data-stu-id="91349-521">Layer</span></span>  | <span data-ttu-id="91349-522">Lýsing á lykli</span><span class="sxs-lookup"><span data-stu-id="91349-522">Account description</span></span>      | <span data-ttu-id="91349-523">Debet</span><span class="sxs-lookup"><span data-stu-id="91349-523">Debit</span></span>  | <span data-ttu-id="91349-524">Kredit</span><span class="sxs-lookup"><span data-stu-id="91349-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="91349-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="91349-525">Ledger</span></span>       | <span data-ttu-id="91349-526">10</span><span class="sxs-lookup"><span data-stu-id="91349-526">10</span></span>             | <span data-ttu-id="91349-527">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="91349-527">Custom</span></span> | <span data-ttu-id="91349-528">Afskriftakostnaður</span><span class="sxs-lookup"><span data-stu-id="91349-528">Depreciation expense</span></span>     | <span data-ttu-id="91349-529">949.75</span><span class="sxs-lookup"><span data-stu-id="91349-529">949.75</span></span> |        |
| <span data-ttu-id="91349-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="91349-530">Ledger</span></span>       | <span data-ttu-id="91349-531">11</span><span class="sxs-lookup"><span data-stu-id="91349-531">11</span></span>             | <span data-ttu-id="91349-532">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="91349-532">Custom</span></span> | <span data-ttu-id="91349-533">Uppsöfnuð afskrift</span><span class="sxs-lookup"><span data-stu-id="91349-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="91349-534">949.75</span><span class="sxs-lookup"><span data-stu-id="91349-534">949.75</span></span> |

<span data-ttu-id="91349-535">Eftir að allar þessar bókarfærslur hafa verið stofnaðar og bókaðar birtast eftirfarandi gildi „Sérsniðins lags 1“.</span><span class="sxs-lookup"><span data-stu-id="91349-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="91349-536">Athugaðu að í síðasta dálkinum er innifalið bankagjald, virðisaukaskattur (VSK), útgjöld og minnkun reiðufjár frá fyrra lagi, en bókarfærslur lögboðinnar skýrslugerðar eru ekki innifaldar.</span><span class="sxs-lookup"><span data-stu-id="91349-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="91349-537">Þar af leiðir áttu kost á tvískiptri skýrslugjöf.</span><span class="sxs-lookup"><span data-stu-id="91349-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="91349-538">Á þessu stigi þarf fyrirtækið aðeins að keyra prófjöfnuð sinn og sameina núverandi lag og sérsniðna lagið til að búa til IFRS-prófjöfnuð.</span><span class="sxs-lookup"><span data-stu-id="91349-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="91349-539">Lykill nr.</span><span class="sxs-lookup"><span data-stu-id="91349-539">Account No</span></span> | <span data-ttu-id="91349-540">lýsing</span><span class="sxs-lookup"><span data-stu-id="91349-540">Description</span></span>              | <span data-ttu-id="91349-541">Lögboðin bók\-Núverandi lag\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="91349-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="91349-542">Lögboðin bók\-Núverandi lag\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="91349-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="91349-543">Lögboðin bók\-Núverandi lag\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="91349-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="91349-544">Núverandi lag \- Samtals</span><span class="sxs-lookup"><span data-stu-id="91349-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="91349-545">Bakfærslubók\-Sérsniðið lag\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="91349-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="91349-546">IFRS 16 bók\-Sérsniðið lag\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="91349-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="91349-547">IFRS 16 bók\-Sérsniðið lag\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="91349-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="91349-548">IFRS 16 bók\-Sérsniðið lag\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="91349-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="91349-549">IFRS 16 bók\-Sérsniðið lag\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="91349-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="91349-550">Sérsniðið lag \+ Núgildandi lag \- Samtals</span><span class="sxs-lookup"><span data-stu-id="91349-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="91349-551">1</span><span class="sxs-lookup"><span data-stu-id="91349-551">1</span></span>          | <span data-ttu-id="91349-552">Leigukostnaður</span><span class="sxs-lookup"><span data-stu-id="91349-552">Lease expense</span></span>            | <span data-ttu-id="91349-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="91349-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="91349-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="91349-554">1,000\.00</span></span>               |   | <span data-ttu-id="91349-555">\-1.000</span><span class="sxs-lookup"><span data-stu-id="91349-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="91349-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="91349-556">0\.00</span></span>                                   |
| <span data-ttu-id="91349-557">2</span><span class="sxs-lookup"><span data-stu-id="91349-557">2</span></span>          | <span data-ttu-id="91349-558">Bankaþóknun</span><span class="sxs-lookup"><span data-stu-id="91349-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="91349-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="91349-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="91349-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="91349-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="91349-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="91349-561">3\.00</span></span>                                   |
| <span data-ttu-id="91349-562">3</span><span class="sxs-lookup"><span data-stu-id="91349-562">3</span></span>          | <span data-ttu-id="91349-563">VSK útgjöld</span><span class="sxs-lookup"><span data-stu-id="91349-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="91349-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="91349-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="91349-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="91349-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="91349-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="91349-566">5\.00</span></span>                                   |
| <span data-ttu-id="91349-567">4</span><span class="sxs-lookup"><span data-stu-id="91349-567">4</span></span>          | <span data-ttu-id="91349-568">Millireikningur</span><span class="sxs-lookup"><span data-stu-id="91349-568">Clearing account</span></span>         | <span data-ttu-id="91349-569">\-1.000\.00</span><span class="sxs-lookup"><span data-stu-id="91349-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="91349-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="91349-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="91349-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="91349-571">0\.00</span></span>                   |   | <span data-ttu-id="91349-572">1.000</span><span class="sxs-lookup"><span data-stu-id="91349-572">1,000</span></span>                                           |                                                | <span data-ttu-id="91349-573">\-1.000</span><span class="sxs-lookup"><span data-stu-id="91349-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="91349-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="91349-574">0\.00</span></span>                                   |
| <span data-ttu-id="91349-575">5</span><span class="sxs-lookup"><span data-stu-id="91349-575">5</span></span>          | <span data-ttu-id="91349-576">Viðskiptaskuldir</span><span class="sxs-lookup"><span data-stu-id="91349-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="91349-577">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="91349-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="91349-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="91349-578">1,008\.00</span></span>                                         | <span data-ttu-id="91349-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="91349-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="91349-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="91349-580">0\.00</span></span>                                   |
| <span data-ttu-id="91349-581">6</span><span class="sxs-lookup"><span data-stu-id="91349-581">6</span></span>          | <span data-ttu-id="91349-582">Afnotaréttur af eign</span><span class="sxs-lookup"><span data-stu-id="91349-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="91349-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="91349-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="91349-584">22,794</span><span class="sxs-lookup"><span data-stu-id="91349-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="91349-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="91349-585">22,793\.90</span></span>                              |
| <span data-ttu-id="91349-586">7</span><span class="sxs-lookup"><span data-stu-id="91349-586">7</span></span>          | <span data-ttu-id="91349-587">Skylda fjármögnunarleigusamnings</span><span class="sxs-lookup"><span data-stu-id="91349-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="91349-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="91349-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="91349-589">\-22.794</span><span class="sxs-lookup"><span data-stu-id="91349-589">\-22,794</span></span>                                       | <span data-ttu-id="91349-590">1.000</span><span class="sxs-lookup"><span data-stu-id="91349-590">1,000</span></span>                                          | <span data-ttu-id="91349-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="91349-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="91349-592">\-21.888\.87</span><span class="sxs-lookup"><span data-stu-id="91349-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="91349-593">8</span><span class="sxs-lookup"><span data-stu-id="91349-593">8</span></span>          | <span data-ttu-id="91349-594">Vaxtakostnaður</span><span class="sxs-lookup"><span data-stu-id="91349-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="91349-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="91349-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="91349-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="91349-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="91349-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="91349-597">94\.97</span></span>                                  |
| <span data-ttu-id="91349-598">9</span><span class="sxs-lookup"><span data-stu-id="91349-598">9</span></span>          | <span data-ttu-id="91349-599">Innlausn</span><span class="sxs-lookup"><span data-stu-id="91349-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="91349-600">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="91349-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="91349-601">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="91349-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="91349-602">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="91349-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="91349-603">10</span><span class="sxs-lookup"><span data-stu-id="91349-603">10</span></span>         | <span data-ttu-id="91349-604">Afskriftakostnaður</span><span class="sxs-lookup"><span data-stu-id="91349-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="91349-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="91349-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="91349-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="91349-606">949\.75</span></span>                                        | <span data-ttu-id="91349-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="91349-607">949\.75</span></span>                                 |
| <span data-ttu-id="91349-608">11</span><span class="sxs-lookup"><span data-stu-id="91349-608">11</span></span>         | <span data-ttu-id="91349-609">Uppsöfnuð afskrift</span><span class="sxs-lookup"><span data-stu-id="91349-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="91349-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="91349-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="91349-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="91349-611">\-949\.75</span></span>                                      | <span data-ttu-id="91349-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="91349-612">\-949\.75</span></span>                               |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]