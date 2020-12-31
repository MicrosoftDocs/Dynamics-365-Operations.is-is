---
title: Tvískipt skýrslugjöf
description: Þetta efnisatriði leiðir notandann í gegnum dæmi sem sýnir hvernig hægt er að uppfylla skilyrði bæði um skýrslugerð samkvæmt alþjóðlegum reikningsskilastaðli (IFRS) og lögboðinnar skýrslugerðar um eignaleigu.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 96e1d4d460aef2f74422d5e4bd4fc68255466455
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4444567"
---
# <a name="dual-reporting"></a><span data-ttu-id="1c306-103">Tvískipt skýrslugjöf</span><span class="sxs-lookup"><span data-stu-id="1c306-103">Dual reporting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c306-104">Þetta efnisatriði leiðir notandann í gegnum dæmi sem sýnir hvernig hægt er að uppfylla skilyrði bæði um skýrslugerð samkvæmt alþjóðlegum reikningsskilastaðli (IFRS) og lögboðinnar skýrslugerðar um eignaleigu.</span><span class="sxs-lookup"><span data-stu-id="1c306-104">This topic guides you through an example that shows how you can fulfill the requirements for both International Financial Reporting Standard (IFRS) reporting and statutory reporting in Asset leasing.</span></span> <span data-ttu-id="1c306-105">Þekking á bókunarlögum í Microsoft Dynamics 365 Finance er áskilin og auðveldar skilning á dæminu.</span><span class="sxs-lookup"><span data-stu-id="1c306-105">Familiarity with posting layers in Microsoft Dynamics 365 Finance is required and will make the example easier to understand.</span></span>

## <a name="example"></a><span data-ttu-id="1c306-106">Dæmi</span><span class="sxs-lookup"><span data-stu-id="1c306-106">Example</span></span>

<span data-ttu-id="1c306-107">Eftirfarandi dæmi sýnir leigusamning sem fellur undir ítalska lögboðna skýrslugerð með því að nota bæði aðferð reiðufjáraðferðar og IFRS-skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="1c306-107">The following example accounts for a lease under Italian statutory reporting by using both the cash-basis method and IFRS reporting methods.</span></span> <span data-ttu-id="1c306-108">Fyrirtækið verður að stofna þrjár bækur til að uppfylla skilyrði ítalskra laga og skilyrði IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="1c306-108">The company must establish three books to account for both the Italian statutory requirements and the IFRS 16 requirements.</span></span> <span data-ttu-id="1c306-109">Ein bók er áskilin fyrir IFRS 16, ein bók er áskilin fyrir lögboðnar kröfur og ein bók er áskilin til að bakfæra lögboðnar bókanir sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="1c306-109">One book is required for IFRS 16, one book is required for statutory requirements, and one book is required to automatically reverse statutory postings.</span></span> <span data-ttu-id="1c306-110">Bækurnar eru settar upp eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="1c306-110">The books are set up as shown in the following tables.</span></span>

<span data-ttu-id="1c306-111">**IFRS 16 bók**</span><span class="sxs-lookup"><span data-stu-id="1c306-111">**IFRS 16 book**</span></span>

<span data-ttu-id="1c306-112">IFRS 16 bókin er sett upp þannig að hún samræmist IFRS 16 bókhaldsstaðli.</span><span class="sxs-lookup"><span data-stu-id="1c306-112">The IFRS 16 book is set up so that it complies with the IFRS 16 accounting standard.</span></span> <span data-ttu-id="1c306-113">Allar færslur sem eru bókaðar í þessari bók verða bókaðar í sérsniðið lag.</span><span class="sxs-lookup"><span data-stu-id="1c306-113">All entries that are posted in this book will be posted to a custom layer.</span></span>

| <span data-ttu-id="1c306-114">Nafn</span><span class="sxs-lookup"><span data-stu-id="1c306-114">Name</span></span>                                    | <span data-ttu-id="1c306-115">lýsing</span><span class="sxs-lookup"><span data-stu-id="1c306-115">Description</span></span>    |
|-----------------------------------------|----------------|
| <span data-ttu-id="1c306-116">Gerð bókar</span><span class="sxs-lookup"><span data-stu-id="1c306-116">Book type</span></span>                               | <span data-ttu-id="1c306-117">Alþjóðlegur reikningsskilastaðall 16</span><span class="sxs-lookup"><span data-stu-id="1c306-117">IFRS 16</span></span>        |
| <span data-ttu-id="1c306-118">Bókarlýsing</span><span class="sxs-lookup"><span data-stu-id="1c306-118">Book description</span></span>                        | <span data-ttu-id="1c306-119">Alþjóðlegur reikningsskilastaðall 16</span><span class="sxs-lookup"><span data-stu-id="1c306-119">IFRS 16</span></span>        |
| <span data-ttu-id="1c306-120">Bókunarlag</span><span class="sxs-lookup"><span data-stu-id="1c306-120">Posting Layer</span></span>                           | <span data-ttu-id="1c306-121">Sérsniðið lag 1</span><span class="sxs-lookup"><span data-stu-id="1c306-121">Custom layer 1</span></span> |
| <span data-ttu-id="1c306-122">Gerð leigu</span><span class="sxs-lookup"><span data-stu-id="1c306-122">Lease Type</span></span>                              | <span data-ttu-id="1c306-123">Finance</span><span class="sxs-lookup"><span data-stu-id="1c306-123">Finance</span></span>        |
| <span data-ttu-id="1c306-124">Bókhaldsrammi</span><span class="sxs-lookup"><span data-stu-id="1c306-124">Accounting Framework</span></span>                    | <span data-ttu-id="1c306-125">Alþjóðlegur reikningsskilastaðall 16</span><span class="sxs-lookup"><span data-stu-id="1c306-125">IFRS 16</span></span>        |
| <span data-ttu-id="1c306-126">Uppsetning leigutíma / nýtingartíma</span><span class="sxs-lookup"><span data-stu-id="1c306-126">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="1c306-127">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-127">0.00</span></span>           |
| <span data-ttu-id="1c306-128">Uppsetning á núvirði / Gangvirði eignar</span><span class="sxs-lookup"><span data-stu-id="1c306-128">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="1c306-129">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-129">0.00</span></span>           |
| <span data-ttu-id="1c306-130">Skammtímaþröskuldur</span><span class="sxs-lookup"><span data-stu-id="1c306-130">Short-term threshold</span></span>                    | <span data-ttu-id="1c306-131">12</span><span class="sxs-lookup"><span data-stu-id="1c306-131">12</span></span>             |
| <span data-ttu-id="1c306-132">Mörk verðlítillar eignar</span><span class="sxs-lookup"><span data-stu-id="1c306-132">Low Value Threshold</span></span>                     | <span data-ttu-id="1c306-133">5,000.00</span><span class="sxs-lookup"><span data-stu-id="1c306-133">5,000.00</span></span>       |
| <span data-ttu-id="1c306-134">Greiða lánardrottni</span><span class="sxs-lookup"><span data-stu-id="1c306-134">Pay to Vendor</span></span>                           | <span data-ttu-id="1c306-135">Ekkert</span><span class="sxs-lookup"><span data-stu-id="1c306-135">No</span></span>             |

<span data-ttu-id="1c306-136">**Lögboðin bók**</span><span class="sxs-lookup"><span data-stu-id="1c306-136">**Statutory book**</span></span>

<span data-ttu-id="1c306-137">Lögboðna bókin er reiðufjársbók þar sem fyrirtækið bókar leigukostnaðinn sem reiðufjárupphæðina sem er greidd mánaðarlega fyrir leigu.</span><span class="sxs-lookup"><span data-stu-id="1c306-137">The statutory book is a cash-basis book where the company will account for the lease expense as the amount of cash that is paid each month for rent.</span></span> <span data-ttu-id="1c306-138">Þessi bók myndar hvorki afnotarétt af eign né leiguskuldbindingu.</span><span class="sxs-lookup"><span data-stu-id="1c306-138">This book won't produce a right-of-use (ROU) asset or lease liability.</span></span>

| <span data-ttu-id="1c306-139">Nafn</span><span class="sxs-lookup"><span data-stu-id="1c306-139">Name</span></span>                                    | <span data-ttu-id="1c306-140">lýsing</span><span class="sxs-lookup"><span data-stu-id="1c306-140">Description</span></span> |
|-----------------------------------------|-------------|
| <span data-ttu-id="1c306-141">Gerð bókar</span><span class="sxs-lookup"><span data-stu-id="1c306-141">Book type</span></span>                               | <span data-ttu-id="1c306-142">Lögboðið</span><span class="sxs-lookup"><span data-stu-id="1c306-142">Statutory</span></span>   |
| <span data-ttu-id="1c306-143">Bókarlýsing</span><span class="sxs-lookup"><span data-stu-id="1c306-143">Book description</span></span>                        | <span data-ttu-id="1c306-144">Staðbundið GAAP</span><span class="sxs-lookup"><span data-stu-id="1c306-144">Local GAAP</span></span>  |
| <span data-ttu-id="1c306-145">Bókunarlag</span><span class="sxs-lookup"><span data-stu-id="1c306-145">Posting Layer</span></span>                           | <span data-ttu-id="1c306-146">Núverandi</span><span class="sxs-lookup"><span data-stu-id="1c306-146">Current</span></span>     |
| <span data-ttu-id="1c306-147">Gerð leigu</span><span class="sxs-lookup"><span data-stu-id="1c306-147">Lease Type</span></span>                              | <span data-ttu-id="1c306-148">Sjálfvirk</span><span class="sxs-lookup"><span data-stu-id="1c306-148">Automatic</span></span>   |
| <span data-ttu-id="1c306-149">Bókhaldsrammi</span><span class="sxs-lookup"><span data-stu-id="1c306-149">Accounting Framework</span></span>                    | <span data-ttu-id="1c306-150">Grundvöllur reiðufjár</span><span class="sxs-lookup"><span data-stu-id="1c306-150">Cash basis</span></span>  |
| <span data-ttu-id="1c306-151">Uppsetning leigutíma / nýtingartíma</span><span class="sxs-lookup"><span data-stu-id="1c306-151">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="1c306-152">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-152">0.00</span></span>        |
| <span data-ttu-id="1c306-153">Uppsetning á núvirði / Gangvirði eignar</span><span class="sxs-lookup"><span data-stu-id="1c306-153">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="1c306-154">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-154">0.00</span></span>        |
| <span data-ttu-id="1c306-155">Skammtímaþröskuldur</span><span class="sxs-lookup"><span data-stu-id="1c306-155">Short-term threshold</span></span>                    | <span data-ttu-id="1c306-156">0</span><span class="sxs-lookup"><span data-stu-id="1c306-156">0</span></span>           |
| <span data-ttu-id="1c306-157">Mörk verðlítillar eignar</span><span class="sxs-lookup"><span data-stu-id="1c306-157">Low Value Threshold</span></span>                     | <span data-ttu-id="1c306-158">0</span><span class="sxs-lookup"><span data-stu-id="1c306-158">0</span></span>           |
| <span data-ttu-id="1c306-159">Greiða lánardrottni</span><span class="sxs-lookup"><span data-stu-id="1c306-159">Pay to Vendor</span></span>                           | <span data-ttu-id="1c306-160">Ekkert</span><span class="sxs-lookup"><span data-stu-id="1c306-160">No</span></span>          |

<span data-ttu-id="1c306-161">**Lögboðin bakfærslubók**</span><span class="sxs-lookup"><span data-stu-id="1c306-161">**Statutory reversal book**</span></span>

<span data-ttu-id="1c306-162">Lögboðin bakfærslubók er sett upp á sama hátt og lögboðna bókin.</span><span class="sxs-lookup"><span data-stu-id="1c306-162">The statutory reversal book is set up in the same way as the statutory book.</span></span>

| <span data-ttu-id="1c306-163">Nafn</span><span class="sxs-lookup"><span data-stu-id="1c306-163">Name</span></span>                                    | <span data-ttu-id="1c306-164">lýsing</span><span class="sxs-lookup"><span data-stu-id="1c306-164">Description</span></span>                    |
|-----------------------------------------|--------------------------------|
| <span data-ttu-id="1c306-165">Gerð bókar</span><span class="sxs-lookup"><span data-stu-id="1c306-165">Book type</span></span>                               | <span data-ttu-id="1c306-166">Lögboðin - Bakfærsla</span><span class="sxs-lookup"><span data-stu-id="1c306-166">Statutory – Reversal</span></span>           |
| <span data-ttu-id="1c306-167">Bókarlýsing</span><span class="sxs-lookup"><span data-stu-id="1c306-167">Book description</span></span>                        | <span data-ttu-id="1c306-168">Bók til að bakfæra lögboðna bók</span><span class="sxs-lookup"><span data-stu-id="1c306-168">Book to reverse statutory book</span></span> |
| <span data-ttu-id="1c306-169">Bókunarlag</span><span class="sxs-lookup"><span data-stu-id="1c306-169">Posting Layer</span></span>                           | <span data-ttu-id="1c306-170">Sérsniðið lag 1</span><span class="sxs-lookup"><span data-stu-id="1c306-170">Custom layer 1</span></span>                 |
| <span data-ttu-id="1c306-171">Gerð leigu</span><span class="sxs-lookup"><span data-stu-id="1c306-171">Lease Type</span></span>                              | <span data-ttu-id="1c306-172">Sjálfvirk</span><span class="sxs-lookup"><span data-stu-id="1c306-172">Automatic</span></span>                      |
| <span data-ttu-id="1c306-173">Bókhaldsrammi</span><span class="sxs-lookup"><span data-stu-id="1c306-173">Accounting Framework</span></span>                    | <span data-ttu-id="1c306-174">Grundvöllur reiðufjár</span><span class="sxs-lookup"><span data-stu-id="1c306-174">Cash basis</span></span>                     |
| <span data-ttu-id="1c306-175">Uppsetning leigutíma / nýtingartíma</span><span class="sxs-lookup"><span data-stu-id="1c306-175">Lease Term / Useful life Set Up</span></span>         | <span data-ttu-id="1c306-176">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-176">0.00</span></span>                           |
| <span data-ttu-id="1c306-177">Uppsetning á núvirði / Gangvirði eignar</span><span class="sxs-lookup"><span data-stu-id="1c306-177">Present Value / Asset Fair Value Set Up</span></span> | <span data-ttu-id="1c306-178">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-178">0.00</span></span>                           |
| <span data-ttu-id="1c306-179">Skammtímaþröskuldur</span><span class="sxs-lookup"><span data-stu-id="1c306-179">Short-term threshold</span></span>                    | <span data-ttu-id="1c306-180">0</span><span class="sxs-lookup"><span data-stu-id="1c306-180">0</span></span>                              |
| <span data-ttu-id="1c306-181">Mörk verðlítillar eignar</span><span class="sxs-lookup"><span data-stu-id="1c306-181">Low Value Threshold</span></span>                     | <span data-ttu-id="1c306-182">0</span><span class="sxs-lookup"><span data-stu-id="1c306-182">0</span></span>                              |
| <span data-ttu-id="1c306-183">Greiða lánardrottni</span><span class="sxs-lookup"><span data-stu-id="1c306-183">Pay to Vendor</span></span>                           | <span data-ttu-id="1c306-184">Ekkert</span><span class="sxs-lookup"><span data-stu-id="1c306-184">No</span></span>                             |

<span data-ttu-id="1c306-185">Í þessu dæmi er búið að stofna leigusamning með eftirfarandi stillingar á flipunum **Almennt** og **Greiðsluáætlunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="1c306-185">For this example, a lease has been created that has the following settings on the **General** and **Payment schedule lines** tabs.</span></span>

<span data-ttu-id="1c306-186">**Almennt**</span><span class="sxs-lookup"><span data-stu-id="1c306-186">**General tab**</span></span>

| <span data-ttu-id="1c306-187">Svæði</span><span class="sxs-lookup"><span data-stu-id="1c306-187">Field</span></span>                      | <span data-ttu-id="1c306-188">Virði</span><span class="sxs-lookup"><span data-stu-id="1c306-188">Value</span></span>            |
|----------------------------|------------------|
| <span data-ttu-id="1c306-189">Vextir á nýju lánsfé</span><span class="sxs-lookup"><span data-stu-id="1c306-189">Incremental borrowing rate</span></span> | <span data-ttu-id="1c306-190">5%</span><span class="sxs-lookup"><span data-stu-id="1c306-190">5%</span></span>               |
| <span data-ttu-id="1c306-191">Upphafsdagsetning</span><span class="sxs-lookup"><span data-stu-id="1c306-191">Commencement date</span></span>          | <span data-ttu-id="1c306-192">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="1c306-192">1/1/2020</span></span>         |
| <span data-ttu-id="1c306-193">Leigusamningsflokkur</span><span class="sxs-lookup"><span data-stu-id="1c306-193">Lease group</span></span>                | <span data-ttu-id="1c306-194">Byggingar</span><span class="sxs-lookup"><span data-stu-id="1c306-194">Buildings</span></span>        |
| <span data-ttu-id="1c306-195">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="1c306-195">Vendor</span></span>                     | <span data-ttu-id="1c306-196">1001</span><span class="sxs-lookup"><span data-stu-id="1c306-196">1001</span></span>             |
| <span data-ttu-id="1c306-197">Gangvirði eignarinnar</span><span class="sxs-lookup"><span data-stu-id="1c306-197">Fair value of the asset</span></span>    | <span data-ttu-id="1c306-198">245,000</span><span class="sxs-lookup"><span data-stu-id="1c306-198">245,000</span></span>          |
| <span data-ttu-id="1c306-199">Nýtingartími eignar</span><span class="sxs-lookup"><span data-stu-id="1c306-199">Asset useful life</span></span>          | <span data-ttu-id="1c306-200">120</span><span class="sxs-lookup"><span data-stu-id="1c306-200">120</span></span>              |
| <span data-ttu-id="1c306-201">Tegund afborgunar</span><span class="sxs-lookup"><span data-stu-id="1c306-201">Annuity type</span></span>               | <span data-ttu-id="1c306-202">Venjulegar afborganir</span><span class="sxs-lookup"><span data-stu-id="1c306-202">Ordinary annuity</span></span> |
| <span data-ttu-id="1c306-203">Samsett tímabil</span><span class="sxs-lookup"><span data-stu-id="1c306-203">Compounding interval</span></span>       | <span data-ttu-id="1c306-204">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="1c306-204">Monthly</span></span>          |

<span data-ttu-id="1c306-205">**Flipi greiðsluáætlunarlína**</span><span class="sxs-lookup"><span data-stu-id="1c306-205">**Payment schedule lines tab**</span></span>

| <span data-ttu-id="1c306-206">Svæði</span><span class="sxs-lookup"><span data-stu-id="1c306-206">Field</span></span>             | <span data-ttu-id="1c306-207">Virði</span><span class="sxs-lookup"><span data-stu-id="1c306-207">Value</span></span>      |
|-------------------|------------|
| <span data-ttu-id="1c306-208">Upphafsdagsetning</span><span class="sxs-lookup"><span data-stu-id="1c306-208">Start date</span></span>        | <span data-ttu-id="1c306-209">1/1/2020</span><span class="sxs-lookup"><span data-stu-id="1c306-209">1/1/2020</span></span>   |
| <span data-ttu-id="1c306-210">Tímabil</span><span class="sxs-lookup"><span data-stu-id="1c306-210">Period interval</span></span>   | <span data-ttu-id="1c306-211">Mánuðir</span><span class="sxs-lookup"><span data-stu-id="1c306-211">Months</span></span>     |
| <span data-ttu-id="1c306-212">Tímabil</span><span class="sxs-lookup"><span data-stu-id="1c306-212">Periods</span></span>           | <span data-ttu-id="1c306-213">24</span><span class="sxs-lookup"><span data-stu-id="1c306-213">24</span></span>         |
| <span data-ttu-id="1c306-214">Lokadagsetning</span><span class="sxs-lookup"><span data-stu-id="1c306-214">End date</span></span>          | <span data-ttu-id="1c306-215">31/12/2020</span><span class="sxs-lookup"><span data-stu-id="1c306-215">12/31/2020</span></span> |
| <span data-ttu-id="1c306-216">Greiðslutíðni</span><span class="sxs-lookup"><span data-stu-id="1c306-216">Payment frequency</span></span> | <span data-ttu-id="1c306-217">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="1c306-217">Monthly</span></span>    |
| <span data-ttu-id="1c306-218">Upphæð greiðslu</span><span class="sxs-lookup"><span data-stu-id="1c306-218">Payment amount</span></span>    | <span data-ttu-id="1c306-219">1.000</span><span class="sxs-lookup"><span data-stu-id="1c306-219">1,000</span></span>      |

<span data-ttu-id="1c306-220">Til að gera ráð fyrir þessum leigusamningi samkvæmt tveimur römmum er notað núverandi bókunarlag og sérsniðið bókunarlag.</span><span class="sxs-lookup"><span data-stu-id="1c306-220">To account for this lease under two frameworks, you use a current posting layer and a custom posting layer.</span></span> <span data-ttu-id="1c306-221">Eftirfarandi tafla sýnir dæmi um hverja áskilda bókarfærslu til að birta fjármál á réttan hátt samkvæmt hverjum reikningsskilastaðli fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="1c306-221">The following table shows an example of every journal entry that required to fairly represent the financials under each reporting standard.</span></span> <span data-ttu-id="1c306-222">Ítarleg lýsing á hverri bókarfærslu fyrir fyrsta mánuð leigusamningsins er veitt eftir á.</span><span class="sxs-lookup"><span data-stu-id="1c306-222">A detailed description of each journal entry for the first month of the lease is provided afterward.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="1c306-223">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="1c306-223">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="1c306-224">lýsing</span><span class="sxs-lookup"><span data-stu-id="1c306-224">Description</span></span></th>
<th colspan='3'><span data-ttu-id="1c306-225">Lögboðin bók (núverandi lag)</span><span class="sxs-lookup"><span data-stu-id="1c306-225">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="1c306-226">Núverandi lag samtals</span><span class="sxs-lookup"><span data-stu-id="1c306-226">Current layer total</span></span></th>
<th><span data-ttu-id="1c306-227">Bakfærslubók (sérsniðið lag)</span><span class="sxs-lookup"><span data-stu-id="1c306-227">Reversal book (custom layer)</span></span></th>
<th colspan='4'><span data-ttu-id="1c306-228">IFRS 16 bók (sérsniðið lag)</span><span class="sxs-lookup"><span data-stu-id="1c306-228">IFRS 16 book (custom layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="1c306-229">Núgildandi lag + sérsniðið lag alls</span><span class="sxs-lookup"><span data-stu-id="1c306-229">Current layer + custom layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1c306-230">JE-100</span><span class="sxs-lookup"><span data-stu-id="1c306-230">JE-100</span></span></th>
<th><span data-ttu-id="1c306-231">JE-110</span><span class="sxs-lookup"><span data-stu-id="1c306-231">JE-110</span></span></th>
<th><span data-ttu-id="1c306-232">JE-120</span><span class="sxs-lookup"><span data-stu-id="1c306-232">JE-120</span></span></th>
<th><span data-ttu-id="1c306-233">JE-130</span><span class="sxs-lookup"><span data-stu-id="1c306-233">JE-130</span></span></th>
<th><span data-ttu-id="1c306-234">JE-140</span><span class="sxs-lookup"><span data-stu-id="1c306-234">JE-140</span></span></th>
<th><span data-ttu-id="1c306-235">JE-150</span><span class="sxs-lookup"><span data-stu-id="1c306-235">JE-150</span></span></th>
<th><span data-ttu-id="1c306-236">JE-160</span><span class="sxs-lookup"><span data-stu-id="1c306-236">JE-160</span></span></th>
<th><span data-ttu-id="1c306-237">JE-170</span><span class="sxs-lookup"><span data-stu-id="1c306-237">JE-170</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1c306-238">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="1c306-238">Dr (Cr)</span></span></th>
<th><span data-ttu-id="1c306-239">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="1c306-239">Dr (Cr)</span></span></th>
<th><span data-ttu-id="1c306-240">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="1c306-240">Dr (Cr)</span></span></th>
<th><span data-ttu-id="1c306-241">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="1c306-241">Dr (Cr)</span></span></th>
<th><span data-ttu-id="1c306-242">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="1c306-242">Dr (Cr)</span></span></th>
<th><span data-ttu-id="1c306-243">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="1c306-243">Dr (Cr)</span></span></th>
<th><span data-ttu-id="1c306-244">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="1c306-244">Dr (Cr)</span></span></th>
<th><span data-ttu-id="1c306-245">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="1c306-245">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1c306-246">1</span><span class="sxs-lookup"><span data-stu-id="1c306-246">1</span></span></td>
<td><span data-ttu-id="1c306-247">Leigukostnaður</span><span class="sxs-lookup"><span data-stu-id="1c306-247">Lease expense</span></span></td>
<td><span data-ttu-id="1c306-248">1,000.00</span><span class="sxs-lookup"><span data-stu-id="1c306-248">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-249">1,000.00</span><span class="sxs-lookup"><span data-stu-id="1c306-249">1,000.00</span></span></td>
<td><span data-ttu-id="1c306-250">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="1c306-250">-1,000.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-251">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-251">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-252">2</span><span class="sxs-lookup"><span data-stu-id="1c306-252">2</span></span></td>
<td><span data-ttu-id="1c306-253">Bankaþóknun</span><span class="sxs-lookup"><span data-stu-id="1c306-253">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="1c306-254">3.00</span><span class="sxs-lookup"><span data-stu-id="1c306-254">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="1c306-255">3.00</span><span class="sxs-lookup"><span data-stu-id="1c306-255">3.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-256">3.00</span><span class="sxs-lookup"><span data-stu-id="1c306-256">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-257">3</span><span class="sxs-lookup"><span data-stu-id="1c306-257">3</span></span></td>
<td><span data-ttu-id="1c306-258">VSK útgjöld</span><span class="sxs-lookup"><span data-stu-id="1c306-258">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="1c306-259">5.00</span><span class="sxs-lookup"><span data-stu-id="1c306-259">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="1c306-260">5.00</span><span class="sxs-lookup"><span data-stu-id="1c306-260">5.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-261">5.00</span><span class="sxs-lookup"><span data-stu-id="1c306-261">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-262">4</span><span class="sxs-lookup"><span data-stu-id="1c306-262">4</span></span></td>
<td><span data-ttu-id="1c306-263">Millireikningur</span><span class="sxs-lookup"><span data-stu-id="1c306-263">Clearing account</span></span></td>
<td><span data-ttu-id="1c306-264">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="1c306-264">-1,000.00</span></span></td>
<td><span data-ttu-id="1c306-265">1,000.00</span><span class="sxs-lookup"><span data-stu-id="1c306-265">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="1c306-266">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-266">0.00</span></span></td>
<td><span data-ttu-id="1c306-267">1,000.00</span><span class="sxs-lookup"><span data-stu-id="1c306-267">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="1c306-268">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="1c306-268">-1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-269">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-269">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-270">5</span><span class="sxs-lookup"><span data-stu-id="1c306-270">5</span></span></td>
<td><span data-ttu-id="1c306-271">Viðskiptaskuldir</span><span class="sxs-lookup"><span data-stu-id="1c306-271">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="1c306-272">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="1c306-272">-1,008.00</span></span></td>
<td><span data-ttu-id="1c306-273">1,008.00</span><span class="sxs-lookup"><span data-stu-id="1c306-273">1,008.00</span></span></td>
<td><span data-ttu-id="1c306-274">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-274">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-275">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-275">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-276">6</span><span class="sxs-lookup"><span data-stu-id="1c306-276">6</span></span></td>
<td><span data-ttu-id="1c306-277">Afnotaréttur af eign</span><span class="sxs-lookup"><span data-stu-id="1c306-277">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-278">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-278">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="1c306-279">22,794.00</span><span class="sxs-lookup"><span data-stu-id="1c306-279">22,794.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-280">22,793.90</span><span class="sxs-lookup"><span data-stu-id="1c306-280">22,793.90</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-281">7</span><span class="sxs-lookup"><span data-stu-id="1c306-281">7</span></span></td>
<td><span data-ttu-id="1c306-282">Skylda fjármögnunarleigusamnings</span><span class="sxs-lookup"><span data-stu-id="1c306-282">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-283">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-283">0.00</span></span></td>
<td></td>
<td><span data-ttu-id="1c306-284">-22.794,00</span><span class="sxs-lookup"><span data-stu-id="1c306-284">-22,794.00</span></span></td>
<td><span data-ttu-id="1c306-285">1,000.00</span><span class="sxs-lookup"><span data-stu-id="1c306-285">1,000.00</span></span></td>
<td><span data-ttu-id="1c306-286">-94,97</span><span class="sxs-lookup"><span data-stu-id="1c306-286">-94.97</span></span></td>
<td></td>
<td><span data-ttu-id="1c306-287">-21.888,87</span><span class="sxs-lookup"><span data-stu-id="1c306-287">-21,888.87</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-288">8</span><span class="sxs-lookup"><span data-stu-id="1c306-288">8</span></span></td>
<td><span data-ttu-id="1c306-289">Vaxtakostnaður</span><span class="sxs-lookup"><span data-stu-id="1c306-289">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-290">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-290">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-291">94.97</span><span class="sxs-lookup"><span data-stu-id="1c306-291">94.97</span></span></td>
<td></td>
<td><span data-ttu-id="1c306-292">94.97</span><span class="sxs-lookup"><span data-stu-id="1c306-292">94.97</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-293">9</span><span class="sxs-lookup"><span data-stu-id="1c306-293">9</span></span></td>
<td><span data-ttu-id="1c306-294">Innlausn</span><span class="sxs-lookup"><span data-stu-id="1c306-294">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-295">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="1c306-295">-1,008.00</span></span></td>
<td><span data-ttu-id="1c306-296">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="1c306-296">-1,008.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-297">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="1c306-297">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-298">10</span><span class="sxs-lookup"><span data-stu-id="1c306-298">10</span></span></td>
<td><span data-ttu-id="1c306-299">Afskriftakostnaður</span><span class="sxs-lookup"><span data-stu-id="1c306-299">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-300">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-300">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-301">949.75</span><span class="sxs-lookup"><span data-stu-id="1c306-301">949.75</span></span></td>
<td><span data-ttu-id="1c306-302">949.75</span><span class="sxs-lookup"><span data-stu-id="1c306-302">949.75</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-303">11</span><span class="sxs-lookup"><span data-stu-id="1c306-303">11</span></span></td>
<td><span data-ttu-id="1c306-304">Uppsöfnuð afskrift</span><span class="sxs-lookup"><span data-stu-id="1c306-304">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-305">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-305">0.00</span></span></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-306">-949,75</span><span class="sxs-lookup"><span data-stu-id="1c306-306">-949.75</span></span></td>
<td><span data-ttu-id="1c306-307">-949,75</span><span class="sxs-lookup"><span data-stu-id="1c306-307">-949.75</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1c306-308">Eins og taflan hér á undan sýnir eru þrjár bækur áskildar til skráningar bæði samkvæmt lögboðinni skýrslugerð og IFRS-skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="1c306-308">As the preceding table shows, three books are required to report under both statutory reporting and IFRS reporting.</span></span>

- <span data-ttu-id="1c306-309">Lögboðna bókin skráir leigugreiðsluna samkvæmt reglum fyrir reiðufjársbókhald samkvæmt núverandi lagi.</span><span class="sxs-lookup"><span data-stu-id="1c306-309">The statutory book records the lease payment according to the rules for cash-basis accounting under the current layer.</span></span>
- <span data-ttu-id="1c306-310">Lögboðna bakfærslubókin bakfærir lögboðnu bókarfærslurnar.</span><span class="sxs-lookup"><span data-stu-id="1c306-310">The statutory reversal book reverses the statutory journal entries.</span></span>
- <span data-ttu-id="1c306-311">IFRS 16 bókin stofnar áskildar bókarfærslur samkvæmt IFRS 16.</span><span class="sxs-lookup"><span data-stu-id="1c306-311">The IFRS 16 book creates the journal entries that are required under IFRS 16.</span></span>

<span data-ttu-id="1c306-312">Aðeins þarf að færa inn leigu einu sinni.</span><span class="sxs-lookup"><span data-stu-id="1c306-312">You must enter a lease only one time.</span></span> <span data-ttu-id="1c306-313">Síðan er hægt að opna síðuna **Bækur** til að skoða allar bækurnar sem eru tengdar leigusamningnum.</span><span class="sxs-lookup"><span data-stu-id="1c306-313">You can then open the **Books** page to see all the books that are associated with the lease.</span></span>

> [!NOTE]
> <span data-ttu-id="1c306-314">Þegar búið er að stofna bækurnar verður að tengja allar þrjár við sömu leiguskrána.</span><span class="sxs-lookup"><span data-stu-id="1c306-314">When you create the books, all three of them must be associated with the same lease record.</span></span>

<span data-ttu-id="1c306-315">Fyrsta bókarfærslan skráir kostnað leigusamningsins samkvæmt lögboðnu bókinni.</span><span class="sxs-lookup"><span data-stu-id="1c306-315">The first journal entry records the lease expense under the statutory book.</span></span> <span data-ttu-id="1c306-316">Hægt er að stofna greiðslurnar annaðhvort í runu eða með því að velja greiðsluáætlunina í lögboðnu bókinni.</span><span class="sxs-lookup"><span data-stu-id="1c306-316">You can create the payments either in a batch or by selecting the payment schedule in the statutory book.</span></span>

<span data-ttu-id="1c306-317">Í þessu dæmi er eftirfarandi bókarfærsla gerð fyrir lögboðnu bókina úr greiðsluáætlun.</span><span class="sxs-lookup"><span data-stu-id="1c306-317">For this example, the following journal entry is produced for the statutory book from the payment schedule.</span></span>

### <a name="lease-payment--1312020--je-100"></a><span data-ttu-id="1c306-318">Leigugreiðsla – 31/1/2020 – JE 100</span><span class="sxs-lookup"><span data-stu-id="1c306-318">Lease payment – 1/31/2020 – JE 100</span></span>

| <span data-ttu-id="1c306-319">Lykilgerð</span><span class="sxs-lookup"><span data-stu-id="1c306-319">Account type</span></span> | <span data-ttu-id="1c306-320">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="1c306-320">Account number</span></span> | <span data-ttu-id="1c306-321">Lag</span><span class="sxs-lookup"><span data-stu-id="1c306-321">Layer</span></span>   | <span data-ttu-id="1c306-322">Lýsing á lykli</span><span class="sxs-lookup"><span data-stu-id="1c306-322">Account description</span></span> | <span data-ttu-id="1c306-323">Debet</span><span class="sxs-lookup"><span data-stu-id="1c306-323">Debit</span></span>    | <span data-ttu-id="1c306-324">Kredit</span><span class="sxs-lookup"><span data-stu-id="1c306-324">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="1c306-325">Ledger</span><span class="sxs-lookup"><span data-stu-id="1c306-325">Ledger</span></span>       | <span data-ttu-id="1c306-326">1</span><span class="sxs-lookup"><span data-stu-id="1c306-326">1</span></span>              | <span data-ttu-id="1c306-327">Núverandi</span><span class="sxs-lookup"><span data-stu-id="1c306-327">Current</span></span> | <span data-ttu-id="1c306-328">Leigukostnaður</span><span class="sxs-lookup"><span data-stu-id="1c306-328">Lease expense</span></span>       | <span data-ttu-id="1c306-329">1,000.00</span><span class="sxs-lookup"><span data-stu-id="1c306-329">1,000.00</span></span> |          |
| <span data-ttu-id="1c306-330">Ledger</span><span class="sxs-lookup"><span data-stu-id="1c306-330">Ledger</span></span>       | <span data-ttu-id="1c306-331">4</span><span class="sxs-lookup"><span data-stu-id="1c306-331">4</span></span>              | <span data-ttu-id="1c306-332">Núverandi</span><span class="sxs-lookup"><span data-stu-id="1c306-332">Current</span></span> | <span data-ttu-id="1c306-333">Millireikningur</span><span class="sxs-lookup"><span data-stu-id="1c306-333">Clearing account</span></span>    |          | <span data-ttu-id="1c306-334">1,000.00</span><span class="sxs-lookup"><span data-stu-id="1c306-334">1,000.00</span></span> |

<span data-ttu-id="1c306-335">Afgreiðslumaður viðskiptaskulda notar staðlaða Dynamics 365-virkni til að stofna reikning til að greiða fyrir leigusamning utan eignarleigu.</span><span class="sxs-lookup"><span data-stu-id="1c306-335">An Accounts payable clerk uses standard Dynamics 365 functionality to create an invoice to pay for the lease outside Asset leasing.</span></span> <span data-ttu-id="1c306-336">Hins vegar, í stað þess að velja **Leigukostnað** sem debetlykil velur afgreiðslumaður viðskiptaskulda millireikning til að mynda eftirfarandi færslu.</span><span class="sxs-lookup"><span data-stu-id="1c306-336">However, instead of selecting **Lease expense** as the debit account, the Accounts payable clerk selects a clearing account to generate the following entry.</span></span>

### <a name="ap-process--1312020--je-110"></a><span data-ttu-id="1c306-337">AP-ferli – 31/1/2020 – JE 110</span><span class="sxs-lookup"><span data-stu-id="1c306-337">AP process – 1/31/2020 – JE 110</span></span>

| <span data-ttu-id="1c306-338">Lykilgerð</span><span class="sxs-lookup"><span data-stu-id="1c306-338">Account type</span></span> | <span data-ttu-id="1c306-339">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="1c306-339">Account number</span></span> | <span data-ttu-id="1c306-340">Lag</span><span class="sxs-lookup"><span data-stu-id="1c306-340">Layer</span></span>   | <span data-ttu-id="1c306-341">Lýsing á lykli</span><span class="sxs-lookup"><span data-stu-id="1c306-341">Account description</span></span> | <span data-ttu-id="1c306-342">Debet</span><span class="sxs-lookup"><span data-stu-id="1c306-342">Debit</span></span>    | <span data-ttu-id="1c306-343">Kredit</span><span class="sxs-lookup"><span data-stu-id="1c306-343">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="1c306-344">Ledger</span><span class="sxs-lookup"><span data-stu-id="1c306-344">Ledger</span></span>       | <span data-ttu-id="1c306-345">4</span><span class="sxs-lookup"><span data-stu-id="1c306-345">4</span></span>              | <span data-ttu-id="1c306-346">Núverandi</span><span class="sxs-lookup"><span data-stu-id="1c306-346">Current</span></span> | <span data-ttu-id="1c306-347">Millireikningur</span><span class="sxs-lookup"><span data-stu-id="1c306-347">Clearing account</span></span>    | <span data-ttu-id="1c306-348">1,000.00</span><span class="sxs-lookup"><span data-stu-id="1c306-348">1,000.00</span></span> |          |
| <span data-ttu-id="1c306-349">Ledger</span><span class="sxs-lookup"><span data-stu-id="1c306-349">Ledger</span></span>       | <span data-ttu-id="1c306-350">2</span><span class="sxs-lookup"><span data-stu-id="1c306-350">2</span></span>              | <span data-ttu-id="1c306-351">Núverandi</span><span class="sxs-lookup"><span data-stu-id="1c306-351">Current</span></span> | <span data-ttu-id="1c306-352">Bankaþóknun</span><span class="sxs-lookup"><span data-stu-id="1c306-352">Bank fee</span></span>            | <span data-ttu-id="1c306-353">3.00</span><span class="sxs-lookup"><span data-stu-id="1c306-353">3.00</span></span>     |          |
| <span data-ttu-id="1c306-354">Ledger</span><span class="sxs-lookup"><span data-stu-id="1c306-354">Ledger</span></span>       | <span data-ttu-id="1c306-355">3</span><span class="sxs-lookup"><span data-stu-id="1c306-355">3</span></span>              | <span data-ttu-id="1c306-356">Núverandi</span><span class="sxs-lookup"><span data-stu-id="1c306-356">Current</span></span> | <span data-ttu-id="1c306-357">VSK útgjöld</span><span class="sxs-lookup"><span data-stu-id="1c306-357">VAT expense</span></span>         | <span data-ttu-id="1c306-358">5.00</span><span class="sxs-lookup"><span data-stu-id="1c306-358">5.00</span></span>     |          |
| <span data-ttu-id="1c306-359">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="1c306-359">Vendor</span></span>       | <span data-ttu-id="1c306-360">5</span><span class="sxs-lookup"><span data-stu-id="1c306-360">5</span></span>              | <span data-ttu-id="1c306-361">Núverandi</span><span class="sxs-lookup"><span data-stu-id="1c306-361">Current</span></span> | <span data-ttu-id="1c306-362">Viðskiptaskuldir</span><span class="sxs-lookup"><span data-stu-id="1c306-362">Accounts payable</span></span>    |          | <span data-ttu-id="1c306-363">1,008.00</span><span class="sxs-lookup"><span data-stu-id="1c306-363">1,008.00</span></span> |

<span data-ttu-id="1c306-364">Þegar yfirlitið er gefið út til lánardrottins er reglubundna greiðsluferlinu fylgt eftir.</span><span class="sxs-lookup"><span data-stu-id="1c306-364">When the statement is issued to the vendor, you follow the regular payment process.</span></span> <span data-ttu-id="1c306-365">Eftirfarandi bókarfærsla er mynduð við þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="1c306-365">During this process, the following journal entry is generated.</span></span>

### <a name="cash-payment--1312020--je-120"></a><span data-ttu-id="1c306-366">Reiðufjárgreiðsla – 31/1/2020 – JE 120</span><span class="sxs-lookup"><span data-stu-id="1c306-366">Cash payment – 1/31/2020 – JE 120</span></span>

| <span data-ttu-id="1c306-367">Lykilgerð</span><span class="sxs-lookup"><span data-stu-id="1c306-367">Account type</span></span> | <span data-ttu-id="1c306-368">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="1c306-368">Account number</span></span> | <span data-ttu-id="1c306-369">Lag</span><span class="sxs-lookup"><span data-stu-id="1c306-369">Layer</span></span>   | <span data-ttu-id="1c306-370">Lýsing á lykli</span><span class="sxs-lookup"><span data-stu-id="1c306-370">Account description</span></span> | <span data-ttu-id="1c306-371">Debet</span><span class="sxs-lookup"><span data-stu-id="1c306-371">Debit</span></span>    | <span data-ttu-id="1c306-372">Kredit</span><span class="sxs-lookup"><span data-stu-id="1c306-372">Credit</span></span>   |
|--------------|----------------|---------|---------------------|----------|----------|
| <span data-ttu-id="1c306-373">Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="1c306-373">Vendor</span></span>       | <span data-ttu-id="1c306-374">5</span><span class="sxs-lookup"><span data-stu-id="1c306-374">5</span></span>              | <span data-ttu-id="1c306-375">Núverandi</span><span class="sxs-lookup"><span data-stu-id="1c306-375">Current</span></span> | <span data-ttu-id="1c306-376">Viðskiptaskuldir</span><span class="sxs-lookup"><span data-stu-id="1c306-376">Accounts Payable</span></span>    | <span data-ttu-id="1c306-377">1,008.00</span><span class="sxs-lookup"><span data-stu-id="1c306-377">1,008.00</span></span> |          |
| <span data-ttu-id="1c306-378">Banki</span><span class="sxs-lookup"><span data-stu-id="1c306-378">Bank</span></span>         | <span data-ttu-id="1c306-379">9</span><span class="sxs-lookup"><span data-stu-id="1c306-379">9</span></span>              | <span data-ttu-id="1c306-380">Núverandi</span><span class="sxs-lookup"><span data-stu-id="1c306-380">Current</span></span> | <span data-ttu-id="1c306-381">Innlausn</span><span class="sxs-lookup"><span data-stu-id="1c306-381">Cash</span></span>                |          | <span data-ttu-id="1c306-382">1,008.00</span><span class="sxs-lookup"><span data-stu-id="1c306-382">1,008.00</span></span> |

<span data-ttu-id="1c306-383">Á þessu stigi er búið að reikna þetta út samkvæmt lögboðnum skýrslukröfum og hægt er að búa til prófjöfnuð með því að nota núgildandi lag.</span><span class="sxs-lookup"><span data-stu-id="1c306-383">At this point, you've fully accounted for this lease under statutory reporting requirements and can generate a trial balance by using the current layer.</span></span> <span data-ttu-id="1c306-384">Kerfið skilar prófjöfnuði sem inniheldur eftirfarandi tölur.</span><span class="sxs-lookup"><span data-stu-id="1c306-384">The system returns a trial balance that has the following figures.</span></span>

<table>
<thead>
<tr>
<th rowspan='3'><span data-ttu-id="1c306-385">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="1c306-385">Account number</span></span></th>
<th rowspan='3'><span data-ttu-id="1c306-386">lýsing</span><span class="sxs-lookup"><span data-stu-id="1c306-386">Description</span></span></th>
<th colspan='3'><span data-ttu-id="1c306-387">Lögboðin bók (núverandi lag)</span><span class="sxs-lookup"><span data-stu-id="1c306-387">Statutory book (current layer)</span></span></th>
<th rowspan='3'><span data-ttu-id="1c306-388">Núverandi lag samtals</span><span class="sxs-lookup"><span data-stu-id="1c306-388">Current layer total</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1c306-389">JE-100</span><span class="sxs-lookup"><span data-stu-id="1c306-389">JE-100</span></span></th>
<th><span data-ttu-id="1c306-390">JE-110</span><span class="sxs-lookup"><span data-stu-id="1c306-390">JE-110</span></span></th>
<th><span data-ttu-id="1c306-391">JE-120</span><span class="sxs-lookup"><span data-stu-id="1c306-391">JE-120</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="1c306-392">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="1c306-392">Dr (Cr)</span></span></th>
<th><span data-ttu-id="1c306-393">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="1c306-393">Dr (Cr)</span></span></th>
<th><span data-ttu-id="1c306-394">Dr (Cr)</span><span class="sxs-lookup"><span data-stu-id="1c306-394">Dr (Cr)</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="1c306-395">1</span><span class="sxs-lookup"><span data-stu-id="1c306-395">1</span></span></td>
<td><span data-ttu-id="1c306-396">Leigukostnaður</span><span class="sxs-lookup"><span data-stu-id="1c306-396">Lease expense</span></span></td>
<td><span data-ttu-id="1c306-397">1,000.00</span><span class="sxs-lookup"><span data-stu-id="1c306-397">1,000.00</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-398">1,000.00</span><span class="sxs-lookup"><span data-stu-id="1c306-398">1,000.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-399">2</span><span class="sxs-lookup"><span data-stu-id="1c306-399">2</span></span></td>
<td><span data-ttu-id="1c306-400">Bankaþóknun</span><span class="sxs-lookup"><span data-stu-id="1c306-400">Bank fee</span></span></td>
<td></td>
<td><span data-ttu-id="1c306-401">3.00</span><span class="sxs-lookup"><span data-stu-id="1c306-401">3.00</span></span></td>
<td></td>
<td><span data-ttu-id="1c306-402">3.00</span><span class="sxs-lookup"><span data-stu-id="1c306-402">3.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-403">3</span><span class="sxs-lookup"><span data-stu-id="1c306-403">3</span></span></td>
<td><span data-ttu-id="1c306-404">VSK útgjöld</span><span class="sxs-lookup"><span data-stu-id="1c306-404">VAT expense</span></span></td>
<td></td>
<td><span data-ttu-id="1c306-405">5.00</span><span class="sxs-lookup"><span data-stu-id="1c306-405">5.00</span></span></td>
<td></td>
<td><span data-ttu-id="1c306-406">5.00</span><span class="sxs-lookup"><span data-stu-id="1c306-406">5.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-407">4</span><span class="sxs-lookup"><span data-stu-id="1c306-407">4</span></span></td>
<td><span data-ttu-id="1c306-408">Millireikningur</span><span class="sxs-lookup"><span data-stu-id="1c306-408">Clearing account</span></span></td>
<td><span data-ttu-id="1c306-409">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="1c306-409">-1,000.00</span></span></td>
<td><span data-ttu-id="1c306-410">1,000.00</span><span class="sxs-lookup"><span data-stu-id="1c306-410">1,000.00</span></span></td>
<td></td>
<td><span data-ttu-id="1c306-411">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-411">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-412">5</span><span class="sxs-lookup"><span data-stu-id="1c306-412">5</span></span></td>
<td><span data-ttu-id="1c306-413">Viðskiptaskuldir</span><span class="sxs-lookup"><span data-stu-id="1c306-413">Accounts payable</span></span></td>
<td></td>
<td><span data-ttu-id="1c306-414">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="1c306-414">-1,008.00</span></span></td>
<td><span data-ttu-id="1c306-415">1,008.00</span><span class="sxs-lookup"><span data-stu-id="1c306-415">1,008.00</span></span></td>
<td><span data-ttu-id="1c306-416">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-416">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-417">6</span><span class="sxs-lookup"><span data-stu-id="1c306-417">6</span></span></td>
<td><span data-ttu-id="1c306-418">Afnotaréttur af eign</span><span class="sxs-lookup"><span data-stu-id="1c306-418">ROU asset</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-419">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-419">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-420">7</span><span class="sxs-lookup"><span data-stu-id="1c306-420">7</span></span></td>
<td><span data-ttu-id="1c306-421">Skylda fjármögnunarleigusamnings</span><span class="sxs-lookup"><span data-stu-id="1c306-421">Finance lease obligation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-422">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-422">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-423">8</span><span class="sxs-lookup"><span data-stu-id="1c306-423">8</span></span></td>
<td><span data-ttu-id="1c306-424">Vaxtakostnaður</span><span class="sxs-lookup"><span data-stu-id="1c306-424">Interest expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-425">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-425">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-426">9</span><span class="sxs-lookup"><span data-stu-id="1c306-426">9</span></span></td>
<td><span data-ttu-id="1c306-427">Innlausn</span><span class="sxs-lookup"><span data-stu-id="1c306-427">Cash</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-428">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="1c306-428">-1,008.00</span></span></td>
<td><span data-ttu-id="1c306-429">-1.008,00</span><span class="sxs-lookup"><span data-stu-id="1c306-429">-1,008.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-430">10</span><span class="sxs-lookup"><span data-stu-id="1c306-430">10</span></span></td>
<td><span data-ttu-id="1c306-431">Afskriftakostnaður</span><span class="sxs-lookup"><span data-stu-id="1c306-431">Depreciation expense</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-432">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-432">0.00</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c306-433">11</span><span class="sxs-lookup"><span data-stu-id="1c306-433">11</span></span></td>
<td><span data-ttu-id="1c306-434">Uppsöfnuð afskrift</span><span class="sxs-lookup"><span data-stu-id="1c306-434">Accumulated depreciation</span></span></td>
<td></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c306-435">0,00</span><span class="sxs-lookup"><span data-stu-id="1c306-435">0.00</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1c306-436">Ef ætlunin er að nota tölur IFRS 16 til að keyra sama prófjöfnuð verður að bakfæra færslur lögboðinnar færslubókar og bóka IFRS 16-færslurnar.</span><span class="sxs-lookup"><span data-stu-id="1c306-436">If you want to use the IFRS 16 figures to run the same trial balance, the statutory accounting journal entries must be reversed, and the IFRS 16 journal entries must be posted.</span></span> <span data-ttu-id="1c306-437">Til að bakfæra lögboðnu færslubókarfærslur, inniheldur þetta dæmi lögboðna bakfærslubók með sömu uppsetningu og lögboðin færslubók en með gagnstæða bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="1c306-437">To reverse the statutory journal entries, this example includes a statutory reversal book that has the same setup as the statutory book but an opposite posting profile.</span></span> <span data-ttu-id="1c306-438">Lögboðna bókin er t.d. *skuldfærð* kostnaðarlykill leigusamnings en bakfærslubókin *kreditfærir* slíkan lykil.</span><span class="sxs-lookup"><span data-stu-id="1c306-438">For example, the statutory book *debited* a lease expense account, but the reversal book will *credit* this account.</span></span> <span data-ttu-id="1c306-439">Þessi vensl eru skilgreind á auðveldan hátt í bókunarlyklum eignarleigu á síðunni **Færibreytur fyrir eignarleigu** (**Eignarleiga \> Uppsetning \> Færibreytur fyrir eignarleigu**).</span><span class="sxs-lookup"><span data-stu-id="1c306-439">These relationships are easily defined in the Asset leasing posting accounts on the **Asset leasing parameters** page (**Asset leasing \> Setup \> Asset leasing parameters**).</span></span>

<span data-ttu-id="1c306-440">Þegar sama ferlið sem notað var fyrir lögboðnu bókina er notað fyrir bakfærslubókina er eftirfarandi bókarfærsla mynduð.</span><span class="sxs-lookup"><span data-stu-id="1c306-440">When the same process that was used for the statutory book is used for the reversal book, the following journal entry is produced.</span></span> <span data-ttu-id="1c306-441">Munurinn er sá að bakfærslubókin bókar bakfærslurnar úr lögboðnu bókinni.</span><span class="sxs-lookup"><span data-stu-id="1c306-441">The difference is that the reversal book books the reversing entries from the statutory book.</span></span> <span data-ttu-id="1c306-442">Bakfærslurnar eru einnig gerðar í sérstillta laginu.</span><span class="sxs-lookup"><span data-stu-id="1c306-442">The reversing entries are also made to the custom layer.</span></span> <span data-ttu-id="1c306-443">Þegar verið er að keyra prófjöfnuð á núverandi lagi eru færslur bakfærslubókarinnar ekki teknar með.</span><span class="sxs-lookup"><span data-stu-id="1c306-443">When a trial balance is run at the current layer, the reversing journal entries aren't included.</span></span>

### <a name="lease-payment--1312020--je-130"></a><span data-ttu-id="1c306-444">Leigugreiðsla – 31/1/2020 – JE 130</span><span class="sxs-lookup"><span data-stu-id="1c306-444">Lease payment – 1/31/2020 – JE 130</span></span>

| <span data-ttu-id="1c306-445">Lykilgerð</span><span class="sxs-lookup"><span data-stu-id="1c306-445">Account type</span></span> | <span data-ttu-id="1c306-446">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="1c306-446">Account number</span></span> | <span data-ttu-id="1c306-447">Lag</span><span class="sxs-lookup"><span data-stu-id="1c306-447">Layer</span></span>  | <span data-ttu-id="1c306-448">Lýsing á lykli</span><span class="sxs-lookup"><span data-stu-id="1c306-448">Account description</span></span> | <span data-ttu-id="1c306-449">Debet</span><span class="sxs-lookup"><span data-stu-id="1c306-449">Debit</span></span>    | <span data-ttu-id="1c306-450">Kredit</span><span class="sxs-lookup"><span data-stu-id="1c306-450">Credit</span></span>   |
|--------------|----------------|--------|---------------------|----------|----------|
| <span data-ttu-id="1c306-451">Ledger</span><span class="sxs-lookup"><span data-stu-id="1c306-451">Ledger</span></span>       | <span data-ttu-id="1c306-452">4</span><span class="sxs-lookup"><span data-stu-id="1c306-452">4</span></span>              | <span data-ttu-id="1c306-453">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="1c306-453">Custom</span></span> | <span data-ttu-id="1c306-454">Millireikningur</span><span class="sxs-lookup"><span data-stu-id="1c306-454">Clearing account</span></span>    | <span data-ttu-id="1c306-455">1,000.00</span><span class="sxs-lookup"><span data-stu-id="1c306-455">1,000.00</span></span> |          |
| <span data-ttu-id="1c306-456">Ledger</span><span class="sxs-lookup"><span data-stu-id="1c306-456">Ledger</span></span>       | <span data-ttu-id="1c306-457">1</span><span class="sxs-lookup"><span data-stu-id="1c306-457">1</span></span>              | <span data-ttu-id="1c306-458">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="1c306-458">Custom</span></span> | <span data-ttu-id="1c306-459">Leigukostnaður</span><span class="sxs-lookup"><span data-stu-id="1c306-459">Lease expense</span></span>       |          | <span data-ttu-id="1c306-460">1,000.00</span><span class="sxs-lookup"><span data-stu-id="1c306-460">1,000.00</span></span> |

<span data-ttu-id="1c306-461">Nú þegar búið er að útiloka færslur lögboðnu bókarinnar verður að bóka allar áskildar bókarfærslur samkvæmt IFRS 16 í IFRS 16-bókinni.</span><span class="sxs-lookup"><span data-stu-id="1c306-461">Now that you've eliminated the statutory journal entries, you will book all the journal entries that IFRS 16 requires in the IFRS 16 book.</span></span> <span data-ttu-id="1c306-462">Þessar færslur fela í sér fyrstu viðurkenningu á afnotarétt af eign og ábyrgðina og færslu vaxta og afskrifta.</span><span class="sxs-lookup"><span data-stu-id="1c306-462">These entries include the initial recognition of the ROU asset and the liability, and the record of interest and depreciation.</span></span>

### <a name="initial-recognition--112020--je-140"></a><span data-ttu-id="1c306-463">Upphafleg viðurkenning – 1/1/2020 – JE 140</span><span class="sxs-lookup"><span data-stu-id="1c306-463">Initial recognition – 1/1/2020 – JE 140</span></span>

| <span data-ttu-id="1c306-464">Lykilgerð</span><span class="sxs-lookup"><span data-stu-id="1c306-464">Account type</span></span> | <span data-ttu-id="1c306-465">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="1c306-465">Account number</span></span> | <span data-ttu-id="1c306-466">Lag</span><span class="sxs-lookup"><span data-stu-id="1c306-466">Layer</span></span>  | <span data-ttu-id="1c306-467">Lýsing á lykli</span><span class="sxs-lookup"><span data-stu-id="1c306-467">Account description</span></span>      | <span data-ttu-id="1c306-468">Debet</span><span class="sxs-lookup"><span data-stu-id="1c306-468">Debit</span></span>     | <span data-ttu-id="1c306-469">Kredit</span><span class="sxs-lookup"><span data-stu-id="1c306-469">Credit</span></span>    |
|--------------|----------------|--------|--------------------------|-----------|-----------|
| <span data-ttu-id="1c306-470">Ledger</span><span class="sxs-lookup"><span data-stu-id="1c306-470">Ledger</span></span>       | <span data-ttu-id="1c306-471">6</span><span class="sxs-lookup"><span data-stu-id="1c306-471">6</span></span>              | <span data-ttu-id="1c306-472">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="1c306-472">Custom</span></span> | <span data-ttu-id="1c306-473">Afnotaréttur af eign</span><span class="sxs-lookup"><span data-stu-id="1c306-473">ROU Asset</span></span>                | <span data-ttu-id="1c306-474">22,793.90</span><span class="sxs-lookup"><span data-stu-id="1c306-474">22,793.90</span></span> |           |
| <span data-ttu-id="1c306-475">Ledger</span><span class="sxs-lookup"><span data-stu-id="1c306-475">Ledger</span></span>       | <span data-ttu-id="1c306-476">7</span><span class="sxs-lookup"><span data-stu-id="1c306-476">7</span></span>              | <span data-ttu-id="1c306-477">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="1c306-477">Custom</span></span> | <span data-ttu-id="1c306-478">Skylda fjármögnunarleigusamnings</span><span class="sxs-lookup"><span data-stu-id="1c306-478">Finance lease obligation</span></span> |           | <span data-ttu-id="1c306-479">22,793.90</span><span class="sxs-lookup"><span data-stu-id="1c306-479">22,793.90</span></span> |

<span data-ttu-id="1c306-480">Leigugreiðslan er bókuð á sama hátt og aðrar leigugreiðslur.</span><span class="sxs-lookup"><span data-stu-id="1c306-480">The lease payment is posted like the other lease payments.</span></span> <span data-ttu-id="1c306-481">Ástæðan fyrir því að nota millireikning er að tryggja að reiðufé sé aðeins kreditfært í eitt skipti.</span><span class="sxs-lookup"><span data-stu-id="1c306-481">The reason for using the clearing account is to ensure that cash is credited only one time.</span></span>

### <a name="lease-payment--1312020--je-150"></a><span data-ttu-id="1c306-482">Leigugreiðsla – 31/1/2020 – JE 150</span><span class="sxs-lookup"><span data-stu-id="1c306-482">Lease payment – 1/31/2020 – JE 150</span></span>

| <span data-ttu-id="1c306-483">Lykilgerð</span><span class="sxs-lookup"><span data-stu-id="1c306-483">Account type</span></span> | <span data-ttu-id="1c306-484">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="1c306-484">Account number</span></span> | <span data-ttu-id="1c306-485">Lag</span><span class="sxs-lookup"><span data-stu-id="1c306-485">Layer</span></span>  | <span data-ttu-id="1c306-486">Lýsing á lykli</span><span class="sxs-lookup"><span data-stu-id="1c306-486">Account description</span></span>      | <span data-ttu-id="1c306-487">Debet</span><span class="sxs-lookup"><span data-stu-id="1c306-487">Debit</span></span>    | <span data-ttu-id="1c306-488">Kredit</span><span class="sxs-lookup"><span data-stu-id="1c306-488">Credit</span></span>   |
|--------------|----------------|--------|--------------------------|----------|----------|
| <span data-ttu-id="1c306-489">Ledger</span><span class="sxs-lookup"><span data-stu-id="1c306-489">Ledger</span></span>       | <span data-ttu-id="1c306-490">7</span><span class="sxs-lookup"><span data-stu-id="1c306-490">7</span></span>              | <span data-ttu-id="1c306-491">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="1c306-491">Custom</span></span> | <span data-ttu-id="1c306-492">Skylda fjármögnunarleigusamnings</span><span class="sxs-lookup"><span data-stu-id="1c306-492">Finance lease obligation</span></span> | <span data-ttu-id="1c306-493">1,000.00</span><span class="sxs-lookup"><span data-stu-id="1c306-493">1,000.00</span></span> |          |
| <span data-ttu-id="1c306-494">Ledger</span><span class="sxs-lookup"><span data-stu-id="1c306-494">Ledger</span></span>       | <span data-ttu-id="1c306-495">4</span><span class="sxs-lookup"><span data-stu-id="1c306-495">4</span></span>              | <span data-ttu-id="1c306-496">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="1c306-496">Custom</span></span> | <span data-ttu-id="1c306-497">Millireikningur</span><span class="sxs-lookup"><span data-stu-id="1c306-497">Clearing account</span></span>         |          | <span data-ttu-id="1c306-498">1,000.00</span><span class="sxs-lookup"><span data-stu-id="1c306-498">1,000.00</span></span> |

<span data-ttu-id="1c306-499">Bókarfærsla vaxtakostnaðar er mynduð úr afskriftaráætlun leiguskuldbindingar.</span><span class="sxs-lookup"><span data-stu-id="1c306-499">The interest expense journal entry is generated from the liability amortization schedule.</span></span>

### <a name="interest-expense--1312020--je-160"></a><span data-ttu-id="1c306-500">Vaxtakostnaður – 31/1/2020 – JE 160</span><span class="sxs-lookup"><span data-stu-id="1c306-500">Interest expense – 1/31/2020 – JE 160</span></span>

| <span data-ttu-id="1c306-501">Lykilgerð</span><span class="sxs-lookup"><span data-stu-id="1c306-501">Account type</span></span> | <span data-ttu-id="1c306-502">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="1c306-502">Account number</span></span> | <span data-ttu-id="1c306-503">Lag</span><span class="sxs-lookup"><span data-stu-id="1c306-503">Layer</span></span>  | <span data-ttu-id="1c306-504">Lýsing á lykli</span><span class="sxs-lookup"><span data-stu-id="1c306-504">Account description</span></span>      | <span data-ttu-id="1c306-505">Debet</span><span class="sxs-lookup"><span data-stu-id="1c306-505">Debit</span></span> | <span data-ttu-id="1c306-506">Kredit</span><span class="sxs-lookup"><span data-stu-id="1c306-506">Credit</span></span> |
|--------------|----------------|--------|--------------------------|-------|--------|
| <span data-ttu-id="1c306-507">Ledger</span><span class="sxs-lookup"><span data-stu-id="1c306-507">Ledger</span></span>       | <span data-ttu-id="1c306-508">8</span><span class="sxs-lookup"><span data-stu-id="1c306-508">8</span></span>              | <span data-ttu-id="1c306-509">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="1c306-509">Custom</span></span> | <span data-ttu-id="1c306-510">Vaxtakostnaður</span><span class="sxs-lookup"><span data-stu-id="1c306-510">Interest expense</span></span>         | <span data-ttu-id="1c306-511">94.97</span><span class="sxs-lookup"><span data-stu-id="1c306-511">94.97</span></span> |        |
| <span data-ttu-id="1c306-512">Ledger</span><span class="sxs-lookup"><span data-stu-id="1c306-512">Ledger</span></span>       | <span data-ttu-id="1c306-513">7</span><span class="sxs-lookup"><span data-stu-id="1c306-513">7</span></span>              | <span data-ttu-id="1c306-514">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="1c306-514">Custom</span></span> | <span data-ttu-id="1c306-515">Skylda fjármögnunarleigusamnings</span><span class="sxs-lookup"><span data-stu-id="1c306-515">Finance lease obligation</span></span> |       | <span data-ttu-id="1c306-516">94.97</span><span class="sxs-lookup"><span data-stu-id="1c306-516">94.97</span></span>  |

<span data-ttu-id="1c306-517">Bókarfærsla afskriftakostnaðar er mynduð úr afskriftaráætlun eignar.</span><span class="sxs-lookup"><span data-stu-id="1c306-517">The depreciation expense journal entry is generated from the asset depreciation schedule.</span></span>

### <a name="depreciation-expense--1312020--je-170"></a><span data-ttu-id="1c306-518">Afskriftarkostnaður – 1/31/2020 – JE 170</span><span class="sxs-lookup"><span data-stu-id="1c306-518">Depreciation expense – 1/31/2020 – JE 170</span></span>

| <span data-ttu-id="1c306-519">Lykilgerð</span><span class="sxs-lookup"><span data-stu-id="1c306-519">Account type</span></span> | <span data-ttu-id="1c306-520">Reikningsnúmer</span><span class="sxs-lookup"><span data-stu-id="1c306-520">Account number</span></span> | <span data-ttu-id="1c306-521">Lag</span><span class="sxs-lookup"><span data-stu-id="1c306-521">Layer</span></span>  | <span data-ttu-id="1c306-522">Lýsing á lykli</span><span class="sxs-lookup"><span data-stu-id="1c306-522">Account description</span></span>      | <span data-ttu-id="1c306-523">Debet</span><span class="sxs-lookup"><span data-stu-id="1c306-523">Debit</span></span>  | <span data-ttu-id="1c306-524">Kredit</span><span class="sxs-lookup"><span data-stu-id="1c306-524">Credit</span></span> |
|--------------|----------------|--------|--------------------------|--------|--------|
| <span data-ttu-id="1c306-525">Ledger</span><span class="sxs-lookup"><span data-stu-id="1c306-525">Ledger</span></span>       | <span data-ttu-id="1c306-526">10</span><span class="sxs-lookup"><span data-stu-id="1c306-526">10</span></span>             | <span data-ttu-id="1c306-527">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="1c306-527">Custom</span></span> | <span data-ttu-id="1c306-528">Afskriftakostnaður</span><span class="sxs-lookup"><span data-stu-id="1c306-528">Depreciation expense</span></span>     | <span data-ttu-id="1c306-529">949.75</span><span class="sxs-lookup"><span data-stu-id="1c306-529">949.75</span></span> |        |
| <span data-ttu-id="1c306-530">Ledger</span><span class="sxs-lookup"><span data-stu-id="1c306-530">Ledger</span></span>       | <span data-ttu-id="1c306-531">11</span><span class="sxs-lookup"><span data-stu-id="1c306-531">11</span></span>             | <span data-ttu-id="1c306-532">Sérsniðinn</span><span class="sxs-lookup"><span data-stu-id="1c306-532">Custom</span></span> | <span data-ttu-id="1c306-533">Uppsöfnuð afskrift</span><span class="sxs-lookup"><span data-stu-id="1c306-533">Accumulated depreciation</span></span> |        | <span data-ttu-id="1c306-534">949.75</span><span class="sxs-lookup"><span data-stu-id="1c306-534">949.75</span></span> |

<span data-ttu-id="1c306-535">Eftir að allar þessar bókarfærslur hafa verið stofnaðar og bókaðar birtast eftirfarandi gildi „Sérsniðins lags 1“.</span><span class="sxs-lookup"><span data-stu-id="1c306-535">After all these journal entries are created and posted, you will see the following "custom layer 1" values.</span></span> <span data-ttu-id="1c306-536">Athugaðu að í síðasta dálkinum er innifalið bankagjald, virðisaukaskattur (VSK), útgjöld og minnkun reiðufjár frá fyrra lagi, en bókarfærslur lögboðinnar skýrslugerðar eru ekki innifaldar.</span><span class="sxs-lookup"><span data-stu-id="1c306-536">Note that the last column includes the bank fee, the value-added tax (VAT) expense, and the reduction of cash from the previous layer, but it doesn't include the statutory reporting journal entries.</span></span> <span data-ttu-id="1c306-537">Þar af leiðir áttu kost á tvískiptri skýrslugjöf.</span><span class="sxs-lookup"><span data-stu-id="1c306-537">Therefore, you achieve true dual-reporting capabilities.</span></span> <span data-ttu-id="1c306-538">Á þessu stigi þarf fyrirtækið aðeins að keyra prófjöfnuð sinn og sameina núverandi lag og sérsniðna lagið til að búa til IFRS-prófjöfnuð.</span><span class="sxs-lookup"><span data-stu-id="1c306-538">At this point, the company just has to run its trial balance, and combine the current layer and the custom layer to create an IFRS trial balance.</span></span>

| <span data-ttu-id="1c306-539">Lykill nr.</span><span class="sxs-lookup"><span data-stu-id="1c306-539">Account No</span></span> | <span data-ttu-id="1c306-540">lýsing</span><span class="sxs-lookup"><span data-stu-id="1c306-540">Description</span></span>              | <span data-ttu-id="1c306-541">Lögboðin bók\-Núverandi lag\-JE\-100\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="1c306-541">Statutory Book\-Current Layer\-JE\-100\-Dr \(Cr\)</span></span> | <span data-ttu-id="1c306-542">Lögboðin bók\-Núverandi lag\-JE\-110\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="1c306-542">Statutory Book\-Current Layer\-JE\-110\-Dr \(Cr\)</span></span> | <span data-ttu-id="1c306-543">Lögboðin bók\-Núverandi lag\-JE\-120\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="1c306-543">Statutory Book\-Current Layer\-JE\-120\-Dr \(Cr\)</span></span> | <span data-ttu-id="1c306-544">Núverandi lag \- Samtals</span><span class="sxs-lookup"><span data-stu-id="1c306-544">Current Layer \- Totals</span></span> | - | <span data-ttu-id="1c306-545">Bakfærslubók\-Sérsniðið lag\-JE\-130\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="1c306-545">Reversal Book\-Custom layer\-JE\-130\-Dr \(Cr\)</span></span> | <span data-ttu-id="1c306-546">IFRS 16 bók\-Sérsniðið lag\-JE\-140\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="1c306-546">IFRS 16 Book\-Custom layer\-JE\-140\-Dr \(Cr\)</span></span> | <span data-ttu-id="1c306-547">IFRS 16 bók\-Sérsniðið lag\-JE\-150\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="1c306-547">IFRS 16 Book\-Custom layer\-JE\-150\-Dr \(Cr\)</span></span> | <span data-ttu-id="1c306-548">IFRS 16 bók\-Sérsniðið lag\-JE\-160\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="1c306-548">IFRS 16 Book\-Custom layer\-JE\-160\-Dr \(Cr\)</span></span> | <span data-ttu-id="1c306-549">IFRS 16 bók\-Sérsniðið lag\-JE\-170\-Dr \(Cr\)</span><span class="sxs-lookup"><span data-stu-id="1c306-549">IFRS 16 Book\-Custom layer\-JE\-170\-Dr \(Cr\)</span></span> | <span data-ttu-id="1c306-550">Sérsniðið lag \+ Núgildandi lag \- Samtals</span><span class="sxs-lookup"><span data-stu-id="1c306-550">Custom Layer \+ Current Layer \- Totals</span></span> |
|------------|--------------------------|---------------------------------------------------|---------------------------------------------------|---------------------------------------------------|-------------------------|---|-------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|------------------------------------------------|-----------------------------------------|
| <span data-ttu-id="1c306-551">1</span><span class="sxs-lookup"><span data-stu-id="1c306-551">1</span></span>          | <span data-ttu-id="1c306-552">Leigukostnaður</span><span class="sxs-lookup"><span data-stu-id="1c306-552">Lease expense</span></span>            | <span data-ttu-id="1c306-553">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-553">1,000\.00</span></span>                                         |                                                   |                                                   | <span data-ttu-id="1c306-554">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-554">1,000\.00</span></span>               |   | <span data-ttu-id="1c306-555">\-1.000</span><span class="sxs-lookup"><span data-stu-id="1c306-555">\-1,000</span></span>                                         |                                                |                                                |                                                |                                                | <span data-ttu-id="1c306-556">0\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-556">0\.00</span></span>                                   |
| <span data-ttu-id="1c306-557">2</span><span class="sxs-lookup"><span data-stu-id="1c306-557">2</span></span>          | <span data-ttu-id="1c306-558">Bankaþóknun</span><span class="sxs-lookup"><span data-stu-id="1c306-558">Bank fee</span></span>                 |                                                   | <span data-ttu-id="1c306-559">3\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-559">3\.00</span></span>                                             |                                                   | <span data-ttu-id="1c306-560">3\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-560">3\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="1c306-561">3\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-561">3\.00</span></span>                                   |
| <span data-ttu-id="1c306-562">3</span><span class="sxs-lookup"><span data-stu-id="1c306-562">3</span></span>          | <span data-ttu-id="1c306-563">VSK útgjöld</span><span class="sxs-lookup"><span data-stu-id="1c306-563">VAT expense</span></span>              |                                                   | <span data-ttu-id="1c306-564">5\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-564">5\.00</span></span>                                             |                                                   | <span data-ttu-id="1c306-565">5\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-565">5\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="1c306-566">5\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-566">5\.00</span></span>                                   |
| <span data-ttu-id="1c306-567">4</span><span class="sxs-lookup"><span data-stu-id="1c306-567">4</span></span>          | <span data-ttu-id="1c306-568">Millireikningur</span><span class="sxs-lookup"><span data-stu-id="1c306-568">Clearing account</span></span>         | <span data-ttu-id="1c306-569">\-1.000\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-569">\-1,000\.00</span></span>                                       | <span data-ttu-id="1c306-570">1,000\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-570">1,000\.00</span></span>                                         |                                                   | <span data-ttu-id="1c306-571">0\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-571">0\.00</span></span>                   |   | <span data-ttu-id="1c306-572">1.000</span><span class="sxs-lookup"><span data-stu-id="1c306-572">1,000</span></span>                                           |                                                | <span data-ttu-id="1c306-573">\-1.000</span><span class="sxs-lookup"><span data-stu-id="1c306-573">\-1,000</span></span>                                        |                                                |                                                | <span data-ttu-id="1c306-574">0\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-574">0\.00</span></span>                                   |
| <span data-ttu-id="1c306-575">5</span><span class="sxs-lookup"><span data-stu-id="1c306-575">5</span></span>          | <span data-ttu-id="1c306-576">Viðskiptaskuldir</span><span class="sxs-lookup"><span data-stu-id="1c306-576">Accounts payable</span></span>         |                                                   | <span data-ttu-id="1c306-577">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-577">\-1,008\.00</span></span>                                       | <span data-ttu-id="1c306-578">1,008\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-578">1,008\.00</span></span>                                         | <span data-ttu-id="1c306-579">0\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-579">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="1c306-580">0\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-580">0\.00</span></span>                                   |
| <span data-ttu-id="1c306-581">6</span><span class="sxs-lookup"><span data-stu-id="1c306-581">6</span></span>          | <span data-ttu-id="1c306-582">Afnotaréttur af eign</span><span class="sxs-lookup"><span data-stu-id="1c306-582">ROU asset</span></span>                |                                                   |                                                   |                                                   | <span data-ttu-id="1c306-583">0\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-583">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="1c306-584">22,794</span><span class="sxs-lookup"><span data-stu-id="1c306-584">22,794</span></span>                                         |                                                |                                                |                                                | <span data-ttu-id="1c306-585">22,793\.90</span><span class="sxs-lookup"><span data-stu-id="1c306-585">22,793\.90</span></span>                              |
| <span data-ttu-id="1c306-586">7</span><span class="sxs-lookup"><span data-stu-id="1c306-586">7</span></span>          | <span data-ttu-id="1c306-587">Skylda fjármögnunarleigusamnings</span><span class="sxs-lookup"><span data-stu-id="1c306-587">Finance lease obligation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="1c306-588">0\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-588">0\.00</span></span>                   |   |                                                 | <span data-ttu-id="1c306-589">\-22.794</span><span class="sxs-lookup"><span data-stu-id="1c306-589">\-22,794</span></span>                                       | <span data-ttu-id="1c306-590">1.000</span><span class="sxs-lookup"><span data-stu-id="1c306-590">1,000</span></span>                                          | <span data-ttu-id="1c306-591">\-94\.97</span><span class="sxs-lookup"><span data-stu-id="1c306-591">\-94\.97</span></span>                                       |                                                | <span data-ttu-id="1c306-592">\-21.888\.87</span><span class="sxs-lookup"><span data-stu-id="1c306-592">\-21,888\.87</span></span>                            |
| <span data-ttu-id="1c306-593">8</span><span class="sxs-lookup"><span data-stu-id="1c306-593">8</span></span>          | <span data-ttu-id="1c306-594">Vaxtakostnaður</span><span class="sxs-lookup"><span data-stu-id="1c306-594">Interest expense</span></span>         |                                                   |                                                   |                                                   | <span data-ttu-id="1c306-595">0\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-595">0\.00</span></span>                   |   |                                                 |                                                |                                                | <span data-ttu-id="1c306-596">94\.97</span><span class="sxs-lookup"><span data-stu-id="1c306-596">94\.97</span></span>                                         |                                                | <span data-ttu-id="1c306-597">94\.97</span><span class="sxs-lookup"><span data-stu-id="1c306-597">94\.97</span></span>                                  |
| <span data-ttu-id="1c306-598">9</span><span class="sxs-lookup"><span data-stu-id="1c306-598">9</span></span>          | <span data-ttu-id="1c306-599">Innlausn</span><span class="sxs-lookup"><span data-stu-id="1c306-599">Cash</span></span>                     |                                                   |                                                   | <span data-ttu-id="1c306-600">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-600">\-1,008\.00</span></span>                                       | <span data-ttu-id="1c306-601">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-601">\-1,008\.00</span></span>             |   |                                                 |                                                |                                                |                                                |                                                | <span data-ttu-id="1c306-602">\-1.008\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-602">\-1,008\.00</span></span>                             |
| <span data-ttu-id="1c306-603">10</span><span class="sxs-lookup"><span data-stu-id="1c306-603">10</span></span>         | <span data-ttu-id="1c306-604">Afskriftakostnaður</span><span class="sxs-lookup"><span data-stu-id="1c306-604">Depreciation expense</span></span>     |                                                   |                                                   |                                                   | <span data-ttu-id="1c306-605">0\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-605">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="1c306-606">949\.75</span><span class="sxs-lookup"><span data-stu-id="1c306-606">949\.75</span></span>                                        | <span data-ttu-id="1c306-607">949\.75</span><span class="sxs-lookup"><span data-stu-id="1c306-607">949\.75</span></span>                                 |
| <span data-ttu-id="1c306-608">11</span><span class="sxs-lookup"><span data-stu-id="1c306-608">11</span></span>         | <span data-ttu-id="1c306-609">Uppsöfnuð afskrift</span><span class="sxs-lookup"><span data-stu-id="1c306-609">Accumulated depreciation</span></span> |                                                   |                                                   |                                                   | <span data-ttu-id="1c306-610">0\.00</span><span class="sxs-lookup"><span data-stu-id="1c306-610">0\.00</span></span>                   |   |                                                 |                                                |                                                |                                                | <span data-ttu-id="1c306-611">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="1c306-611">\-949\.75</span></span>                                      | <span data-ttu-id="1c306-612">\-949\.75</span><span class="sxs-lookup"><span data-stu-id="1c306-612">\-949\.75</span></span>                               |


