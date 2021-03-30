---
title: Tvöfaldur gjaldeyrisstuðningur fyrir skatta
description: Þetta efni útskýrir hvernig á að framlengja tvískiptan gjaldeyrisbókhald á skattalénum og áhrifin á útreikning skatta og bókun
author: EricWang
manager: Ann Beebe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 3f7ca56fef636431e152b2db424f1f972a507721
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212206"
---
# <a name="dual-currency-support-for-sales-tax"></a><span data-ttu-id="d4336-103">Tvöfaldur gjaldeyrisstuðningur fyrir virðisaukaskatt</span><span class="sxs-lookup"><span data-stu-id="d4336-103">Dual currency support for sales tax</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4336-104">Þetta efni útskýrir hvernig á að framlengja tvískipt gjaldeyrisbókhald fyrir virðisaukaskatt og áhrifin á útreikning virðisaukaskatts, bókun og uppgjör.</span><span class="sxs-lookup"><span data-stu-id="d4336-104">This topic explains how to extend dual currency accounting for sales taxes and the impact for sales tax calculations, posting and settlements.</span></span>

<span data-ttu-id="d4336-105">Eiginleikinn Tvískiptur gjaldmiðill fyrir Dynamics 365 Finance var kynntur í útgáfu 8.1 (október 2018).</span><span class="sxs-lookup"><span data-stu-id="d4336-105">The Dual currency feature for Dynamics 365 Finance was introduced in version 8.1 (October 2018).</span></span> <span data-ttu-id="d4336-106">Hann breytir því hvernig bókhaldsskýrslur í skýrslugjaldmiðlinum eru reiknaðar.</span><span class="sxs-lookup"><span data-stu-id="d4336-106">It changes the way that accounting entries in the reporting currency are calculated.</span></span>

<span data-ttu-id="d4336-107">Í fyrri útgáfum var færslum breytt í skýrslugjaldmiðilinn í eftirfarandi röð:</span><span class="sxs-lookup"><span data-stu-id="d4336-107">In earlier versions, transactions were converted to the reporting currency in the following sequence:</span></span> 

- <span data-ttu-id="d4336-108">Heildarfjárhæð færslna var reiknuð í færslugjaldmiðlinum > Færsluupphæðin var umreiknuð í bókhaldsgjaldmiðil > Upphæð bókhaldsgjaldmiðils var umreiknuð í skýrslugjaldmiðilinn</span><span class="sxs-lookup"><span data-stu-id="d4336-108">Transaction total was calculated in the transaction currency > Transaction amount was converted to the accounting currency > Accounting currency amount was converted to the Reporting currency</span></span>

<span data-ttu-id="d4336-109">Eftir að kveikt var á tvískiptum gjaldeyriseiginleika voru færslur umreiknaðar í skýrslugjaldmiðilinn í eftirfarandi röð:</span><span class="sxs-lookup"><span data-stu-id="d4336-109">After enabling the dual currency feature, transactions were converted to the reporting currency in the following sequence:</span></span>

- <span data-ttu-id="d4336-110">Færslugjaldmiðilsupphæð > skýrslugjaldmiðilsupphæð</span><span class="sxs-lookup"><span data-stu-id="d4336-110">Transaction currency amount > Reporting currency amount</span></span>

<span data-ttu-id="d4336-111">Nánari upplýsingar um tvískiptan gjaldmiðil er að finna í [Tvöfaldur gjaldmiðill](dual-currency.md).</span><span class="sxs-lookup"><span data-stu-id="d4336-111">For more information about dual currency, please refer to [Dual currency](dual-currency.md).</span></span>

<span data-ttu-id="d4336-112">Sem afleiðing af stuðningi við tvískipta gjaldmiðla eru tveir nýir möguleikar fáanlegir í eiginleikastjórnun:</span><span class="sxs-lookup"><span data-stu-id="d4336-112">As a consequence of support for dual currencies, two new features are available in feature management:</span></span> 

- <span data-ttu-id="d4336-113">Umreikningur virðisaukaskatts (nýtt í útgáfu 10.0.13)</span><span class="sxs-lookup"><span data-stu-id="d4336-113">Sales tax conversion (new in version 10.0.13)</span></span>

<span data-ttu-id="d4336-114">Tvöfaldur gjaldmiðilsstuðningur við virðisaukaskatta tryggir að skattar eru reiknaðir nákvæmlega í skattagjaldmiðlinum og að uppgjörsstaða virðisaukaskatts er reiknuð nákvæmlega bæði í bókhaldsgjaldmiðli og skýrslugjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="d4336-114">Dual currency support for sales taxes ensures that taxes are calculated accurately in the tax currency, and that the sales tax settlement balance is calculated accurately in both the accounting currency and reporting currency.</span></span> 

## <a name="sales-tax-conversion"></a><span data-ttu-id="d4336-115">Umskráning virðisaukaskatts</span><span class="sxs-lookup"><span data-stu-id="d4336-115">Sales tax conversion</span></span>

<span data-ttu-id="d4336-116">Færibreytan **Virðisaukaskattsbreyting** býður upp á tvo möguleika til að umreikna skattafjárhæð úr færslugjaldmiðli yfir í skattagjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="d4336-116">The **Sales tax conversion** parameter provides two options to convert tax amount from transaction currency to tax currency.</span></span> 

- <span data-ttu-id="d4336-117">Bókhaldsgjaldmiðill: Slóðin verður „Upphæð í færslugjaldmiðli > Upphæð í bókhaldsgjaldmiðli > Upphæð í skattagjaldmiðli”.</span><span class="sxs-lookup"><span data-stu-id="d4336-117">Accounting currency: The path will be "Amount in transaction currency > Amount in accounting currency > Amount in tax currency".</span></span> <span data-ttu-id="d4336-118">Gengisgerð bókhaldsgjaldmiðilsins (stillt í fjárhagsuppsetningu) verður notuð fyrir umreikning gjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="d4336-118">The accounting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>
- <span data-ttu-id="d4336-119">Skýrslugjaldmiðill: Slóðin verður „Upphæð í færslugjaldmiðli > Upphæð í skýrslugjaldmiðli > Upphæð í skattagjaldmiðli”.</span><span class="sxs-lookup"><span data-stu-id="d4336-119">Reporting currency: The path will be "Amount in transaction currency > Amount in reporting currency > Amount in tax currency".</span></span> <span data-ttu-id="d4336-120">Gengisgerð skýrslugjaldmiðils (stillt í fjárhagsuppsetningu) verður notuð fyrir umreikning gjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="d4336-120">The reporting currency exchange rate type (configured in Ledger setup) will be used for the currency conversion.</span></span>

### <a name="example"></a><span data-ttu-id="d4336-121">Dæmi</span><span class="sxs-lookup"><span data-stu-id="d4336-121">Example</span></span>

<span data-ttu-id="d4336-122">Einfalt dæmi til að sýna fram á þessa virkni er:</span><span class="sxs-lookup"><span data-stu-id="d4336-122">A simple example to demonstrate this functionality is:</span></span>

<span data-ttu-id="d4336-123">Gjaldeyrisuppsetning fyrir fjárhag og skatta</span><span class="sxs-lookup"><span data-stu-id="d4336-123">Currency setup for ledger and tax</span></span>

| <span data-ttu-id="d4336-124">Færslugjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d4336-124">Transaction currency</span></span> | <span data-ttu-id="d4336-125">Bókhaldsgjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d4336-125">Accounting currency</span></span> | <span data-ttu-id="d4336-126">Skýrslugjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d4336-126">Reporting currency</span></span> | <span data-ttu-id="d4336-127">Skattagjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d4336-127">Tax currency</span></span> |
| -------------------- | ------------------- | ------------------ | ------------ |
| <span data-ttu-id="d4336-128">EUR</span><span class="sxs-lookup"><span data-stu-id="d4336-128">EUR</span></span>                  | <span data-ttu-id="d4336-129">USD</span><span class="sxs-lookup"><span data-stu-id="d4336-129">USD</span></span>                 | <span data-ttu-id="d4336-130">GBP</span><span class="sxs-lookup"><span data-stu-id="d4336-130">GBP</span></span>                | <span data-ttu-id="d4336-131">GBP</span><span class="sxs-lookup"><span data-stu-id="d4336-131">GBP</span></span>          |

<span data-ttu-id="d4336-132">Gengi</span><span class="sxs-lookup"><span data-stu-id="d4336-132">Exchange rate</span></span>

| <span data-ttu-id="d4336-133">Úr gjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="d4336-133">From currency</span></span> | <span data-ttu-id="d4336-134">Í gjaldmiðil</span><span class="sxs-lookup"><span data-stu-id="d4336-134">To currency</span></span> | <span data-ttu-id="d4336-135">Stuðull</span><span class="sxs-lookup"><span data-stu-id="d4336-135">Factor</span></span> | <span data-ttu-id="d4336-136">Gengi</span><span class="sxs-lookup"><span data-stu-id="d4336-136">Exchange rate</span></span> |
| ------------- | ----------- | ------ | ------------- |
| <span data-ttu-id="d4336-137">EUR</span><span class="sxs-lookup"><span data-stu-id="d4336-137">EUR</span></span>           | <span data-ttu-id="d4336-138">USD</span><span class="sxs-lookup"><span data-stu-id="d4336-138">USD</span></span>         | <span data-ttu-id="d4336-139">1</span><span class="sxs-lookup"><span data-stu-id="d4336-139">1</span></span>      | <span data-ttu-id="d4336-140">1.11</span><span class="sxs-lookup"><span data-stu-id="d4336-140">1.11</span></span>          |
| <span data-ttu-id="d4336-141">EUR</span><span class="sxs-lookup"><span data-stu-id="d4336-141">EUR</span></span>           | <span data-ttu-id="d4336-142">GBP</span><span class="sxs-lookup"><span data-stu-id="d4336-142">GBP</span></span>         | <span data-ttu-id="d4336-143">1</span><span class="sxs-lookup"><span data-stu-id="d4336-143">1</span></span>      | <span data-ttu-id="d4336-144">0.83</span><span class="sxs-lookup"><span data-stu-id="d4336-144">0.83</span></span>          |
| <span data-ttu-id="d4336-145">USD</span><span class="sxs-lookup"><span data-stu-id="d4336-145">USD</span></span>           | <span data-ttu-id="d4336-146">GBP</span><span class="sxs-lookup"><span data-stu-id="d4336-146">GBP</span></span>         | <span data-ttu-id="d4336-147">1</span><span class="sxs-lookup"><span data-stu-id="d4336-147">1</span></span>      | <span data-ttu-id="d4336-148">0.75</span><span class="sxs-lookup"><span data-stu-id="d4336-148">0.75</span></span>          |

<span data-ttu-id="d4336-149">Útreikningur skattaupphæðar í mismunandi færibreytuvalkostum</span><span class="sxs-lookup"><span data-stu-id="d4336-149">Tax amount calculation in different parameter options</span></span>

<span data-ttu-id="d4336-150">Skattaupphæð = 100 EUR</span><span class="sxs-lookup"><span data-stu-id="d4336-150">Tax amount = 100 EUR</span></span>

| <span data-ttu-id="d4336-151">Færibreytur umreiknings á virðisaukaskatti</span><span class="sxs-lookup"><span data-stu-id="d4336-151">Sales tax conversion parameters</span></span> | <span data-ttu-id="d4336-152">Færslugjaldmiðill (EUR)</span><span class="sxs-lookup"><span data-stu-id="d4336-152">Transaction currency (EUR)</span></span> | <span data-ttu-id="d4336-153">Bókhaldsgjaldmiðill (USD)</span><span class="sxs-lookup"><span data-stu-id="d4336-153">Accounting currency (USD)</span></span> | <span data-ttu-id="d4336-154">Skýrslugjaldmiðill (GBP)</span><span class="sxs-lookup"><span data-stu-id="d4336-154">Reporting currency (GBP)</span></span> | <span data-ttu-id="d4336-155">Skattagjaldmiðill (GBP)</span><span class="sxs-lookup"><span data-stu-id="d4336-155">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="d4336-156">Bókhaldsgjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d4336-156">Accounting currency</span></span>             | <span data-ttu-id="d4336-157">100</span><span class="sxs-lookup"><span data-stu-id="d4336-157">100</span></span>                        | <span data-ttu-id="d4336-158">111</span><span class="sxs-lookup"><span data-stu-id="d4336-158">111</span></span>                       | <span data-ttu-id="d4336-159">83</span><span class="sxs-lookup"><span data-stu-id="d4336-159">83</span></span>                       | <span data-ttu-id="d4336-160">**83.25**</span><span class="sxs-lookup"><span data-stu-id="d4336-160">**83.25**</span></span>          |
| <span data-ttu-id="d4336-161">Skýrslugjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d4336-161">Reporting currency</span></span>              | <span data-ttu-id="d4336-162">100</span><span class="sxs-lookup"><span data-stu-id="d4336-162">100</span></span>                        | <span data-ttu-id="d4336-163">111</span><span class="sxs-lookup"><span data-stu-id="d4336-163">111</span></span>                       | <span data-ttu-id="d4336-164">83</span><span class="sxs-lookup"><span data-stu-id="d4336-164">83</span></span>                       | <span data-ttu-id="d4336-165">**83**</span><span class="sxs-lookup"><span data-stu-id="d4336-165">**83**</span></span>             |

<span data-ttu-id="d4336-166">Hægt er að stilla þessa færibreytu út frá samræmiþörf skattayfirvalda.</span><span class="sxs-lookup"><span data-stu-id="d4336-166">This parameter can be configured based on the compliance need from tax authority.</span></span>


### <a name="upgrade-consideration"></a><span data-ttu-id="d4336-167">Uppfæra umhugsunarefni</span><span class="sxs-lookup"><span data-stu-id="d4336-167">Upgrade Consideration</span></span>

<span data-ttu-id="d4336-168">Þessi eiginleiki á aðeins við um nýjar færslur.</span><span class="sxs-lookup"><span data-stu-id="d4336-168">This feature will only apply for new transactions.</span></span> <span data-ttu-id="d4336-169">Fyrir skattafærslu sem þegar er vistuð í TAXTRANS-töflunni en ekki enn gerð upp mun kerfið ekki endurútreikna skattaupphæð í skattagjaldmiðli þar sem gengi þegar skattur var bókaður vantar nú þegar.</span><span class="sxs-lookup"><span data-stu-id="d4336-169">For tax transaction already saved in TAXTRANS table but not settled yet, system will not recalculate tax amount in tax currency because the exchange rate at time point of posting tax is already missing.</span></span>

<span data-ttu-id="d4336-170">Til að koma í veg fyrir fyrri atburðarás mælum við með því að breyta þessu færibreytugildi á nýju (hreinu) skattuppgjörstímabili sem ekki inniheldur óuppgerðar skattafærslur.</span><span class="sxs-lookup"><span data-stu-id="d4336-170">To prevent preceding scenario, we recommend changing this parameter value in a new (clean) tax settlement period that doesn't contain any unsettled tax transactions.</span></span> <span data-ttu-id="d4336-171">Til að breyta þessu gildi á miðju skattauppgjörstímabili, vinsamlegast keyrðu forritið „Jafna og bóka virðisaukaskatt” fyrir núverandi skattauppgjörstímabil áður en þú breytir þessu færibreytugildi.</span><span class="sxs-lookup"><span data-stu-id="d4336-171">To change this value in the middle of a tax settlement period, please run "Settle and post sales tax" program for current tax settlement period before changing this parameter value.</span></span>


## <a name="track-reporting-currency-tax-amount"></a><span data-ttu-id="d4336-172">Rekja skattaupphæð skýrslugjaldmiðils</span><span class="sxs-lookup"><span data-stu-id="d4336-172">Track reporting currency tax amount</span></span>

<span data-ttu-id="d4336-173">Þremur nýjum reitum var bætt við skattskyldar töflur til að rekja fjárhæðir í skýrslugjaldmiðlinum.</span><span class="sxs-lookup"><span data-stu-id="d4336-173">Three new fields were added to tax-related tables to track amounts in the reporting currency.</span></span> <span data-ttu-id="d4336-174">Þessir reitir eru í töflunum TAXUNCOMMITTTED og TAXTRANS:</span><span class="sxs-lookup"><span data-stu-id="d4336-174">These fields are within the TAXUNCOMMITTED and TAXTRANS tables:</span></span>

- <span data-ttu-id="d4336-175">TaxAmountRep: skattaupphæð í skýrslugjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="d4336-175">TaxAmountRep: tax amount in reporting currency</span></span>
- <span data-ttu-id="d4336-176">TaxBaseAmountRep: grunnupphæð í skýrslugjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="d4336-176">TaxBaseAmountRep: base amount in reporting currency</span></span>
- <span data-ttu-id="d4336-177">TaxInCostPriceRep: ekki frádráttarbær fjárhæð í skýrslugjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="d4336-177">TaxInCostPriceRep: non-deductible amount in reporting currency</span></span>

<span data-ttu-id="d4336-178">Fyrir skatt sem eingöngu er vistaður í töflunni TAXUNCOMMITTTED en ekki enn verið bókaður mun kerfið endurreikna skattaupphæð í skýrslugjaldmiðli við bókun og vista í TAXTRANS töflunni.</span><span class="sxs-lookup"><span data-stu-id="d4336-178">For tax only saved in TAXUNCOMMITTED table but not posted yet, system will recalculate tax amount in reporting currency at the time of posting and save in TAXTRANS table.</span></span>

<span data-ttu-id="d4336-179">Þessi útgáfa mun ekki innihalda breytingar á skýrslum og eyðublöðum sem sýna skattaupphæðina í skýrslugjaldmiðlinum.</span><span class="sxs-lookup"><span data-stu-id="d4336-179">This release will not include changes to reports and forms that show the tax amount in the reporting currency.</span></span> <span data-ttu-id="d4336-180">Breytingar á skýrslum og eyðublöðum verða afhentar í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="d4336-180">Changes to reports and forms will be delivered in the future release.</span></span>



## <a name="tax-settlement-auto-balance-in-reporting-currency"></a><span data-ttu-id="d4336-181">Sjálfvirk staða skattauppgjörs í skýrslugjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="d4336-181">Tax settlement auto-balance in reporting currency</span></span>

<span data-ttu-id="d4336-182">Ef skattauppgjör er ekki jafnað í skýrslugjaldmiðli af einhverri ástæðu, svo sem að slóð umreiknings virðisaukaskatts er „Bókhaldsgjaldmiðill“, eða gengisbreyting er á einu skattjöfnunartímabili, þá myndar kerfið sjálfkrafa bókhaldsfærslur til að leiðrétta frávik skattupphæðar og mótfærir það gegn innleystum gengishagnaði/taplykli, sem er skilgreindur í fjárhagsgrunni.</span><span class="sxs-lookup"><span data-stu-id="d4336-182">If the tax settlement is not balanced in the reporting currency for certain reason such as the sales tax conversion path is "Accounting currency", or the exchange rate change in a single tax settlement period, then the system will automatically generate accounting entries to adjust the tax amount variance and offset it against realized exchange gain/loss account, which is configured in Ledger setup.</span></span>

<span data-ttu-id="d4336-183">Notaðu fyrra dæmið til að sýna fram á þennan eiginleika, gerðu ráð fyrir að gögnin í TAXTRANS töflunni við bókun séu eftirfarandi.</span><span class="sxs-lookup"><span data-stu-id="d4336-183">Using the the previous example to demonstrate this feature, suppose that the data in TAXTRANS table at the time of posting is as follows.</span></span>

| <span data-ttu-id="d4336-184">Færibreytur umreiknings á virðisaukaskatti</span><span class="sxs-lookup"><span data-stu-id="d4336-184">Sales tax conversion parameters</span></span> | <span data-ttu-id="d4336-185">Færslugjaldmiðill (EUR)</span><span class="sxs-lookup"><span data-stu-id="d4336-185">Transaction currency (EUR)</span></span> | <span data-ttu-id="d4336-186">Bókhaldsgjaldmiðill (USD)</span><span class="sxs-lookup"><span data-stu-id="d4336-186">Accounting currency (USD)</span></span> | <span data-ttu-id="d4336-187">Skýrslugjaldmiðill (GBP)</span><span class="sxs-lookup"><span data-stu-id="d4336-187">Reporting currency (GBP)</span></span> | <span data-ttu-id="d4336-188">Skattagjaldmiðill (GBP)</span><span class="sxs-lookup"><span data-stu-id="d4336-188">Tax currency (GBP)</span></span> |
| ------------------------------- | -------------------------- | ------------------------- | ------------------------ | ------------------ |
| <span data-ttu-id="d4336-189">Bókhaldsgjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d4336-189">Accounting currency</span></span>             | <span data-ttu-id="d4336-190">100</span><span class="sxs-lookup"><span data-stu-id="d4336-190">100</span></span>                        | <span data-ttu-id="d4336-191">111</span><span class="sxs-lookup"><span data-stu-id="d4336-191">111</span></span>                       | <span data-ttu-id="d4336-192">83</span><span class="sxs-lookup"><span data-stu-id="d4336-192">83</span></span>                       | <span data-ttu-id="d4336-193">**83.25**</span><span class="sxs-lookup"><span data-stu-id="d4336-193">**83.25**</span></span>          |
| <span data-ttu-id="d4336-194">Skýrslugjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d4336-194">Reporting currency</span></span>              | <span data-ttu-id="d4336-195">100</span><span class="sxs-lookup"><span data-stu-id="d4336-195">100</span></span>                        | <span data-ttu-id="d4336-196">111</span><span class="sxs-lookup"><span data-stu-id="d4336-196">111</span></span>                       | <span data-ttu-id="d4336-197">83</span><span class="sxs-lookup"><span data-stu-id="d4336-197">83</span></span>                       | <span data-ttu-id="d4336-198">**83**</span><span class="sxs-lookup"><span data-stu-id="d4336-198">**83**</span></span>             |

<span data-ttu-id="d4336-199">Þegar þú keyrir uppgjörsáætlun virðisaukaskatts í lok mánaðarins verður bókhaldsfærslan eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="d4336-199">When you run the sales tax settlement program at month-end, the accounting entry will be as follows:.</span></span>
#### <a name="scenario-sales-tax-conversion--accounting-currency"></a><span data-ttu-id="d4336-200">Aðstæður: umreikningur virðisaukaskatts = „Bókhaldsgjaldmiðill”</span><span class="sxs-lookup"><span data-stu-id="d4336-200">Scenario: sales tax conversion = "Accounting currency"</span></span>

| <span data-ttu-id="d4336-201">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="d4336-201">Main account</span></span>           | <span data-ttu-id="d4336-202">Færslugjaldmiðill (GBP)</span><span class="sxs-lookup"><span data-stu-id="d4336-202">Transaction currency (GBP)</span></span> | <span data-ttu-id="d4336-203">Bókhaldsgjaldmiðill (USD)</span><span class="sxs-lookup"><span data-stu-id="d4336-203">Accounting currency (USD)</span></span> | <span data-ttu-id="d4336-204">Skýrslugjaldmiðill (GBP)</span><span class="sxs-lookup"><span data-stu-id="d4336-204">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="d4336-205">Inn- og útskattur</span><span class="sxs-lookup"><span data-stu-id="d4336-205">Tax Payable/Receivable</span></span> | <span data-ttu-id="d4336-206">-83.25</span><span class="sxs-lookup"><span data-stu-id="d4336-206">-83.25</span></span>                     | <span data-ttu-id="d4336-207">-111</span><span class="sxs-lookup"><span data-stu-id="d4336-207">-111</span></span>                      | <span data-ttu-id="d4336-208">-83.25</span><span class="sxs-lookup"><span data-stu-id="d4336-208">-83.25</span></span>                   |
| <span data-ttu-id="d4336-209">Skattauppgjör</span><span class="sxs-lookup"><span data-stu-id="d4336-209">Tax Settlement</span></span>         | <span data-ttu-id="d4336-210">83.25</span><span class="sxs-lookup"><span data-stu-id="d4336-210">83.25</span></span>                      | <span data-ttu-id="d4336-211">111</span><span class="sxs-lookup"><span data-stu-id="d4336-211">111</span></span>                       | <span data-ttu-id="d4336-212">83.25</span><span class="sxs-lookup"><span data-stu-id="d4336-212">83.25</span></span>                    |
| <span data-ttu-id="d4336-213">Innleystur hagnaður/tap</span><span class="sxs-lookup"><span data-stu-id="d4336-213">Realized Gain/Loss</span></span>     | <span data-ttu-id="d4336-214">0</span><span class="sxs-lookup"><span data-stu-id="d4336-214">0</span></span>                          | <span data-ttu-id="d4336-215">0</span><span class="sxs-lookup"><span data-stu-id="d4336-215">0</span></span>                         | <span data-ttu-id="d4336-216">-0.25</span><span class="sxs-lookup"><span data-stu-id="d4336-216">-0.25</span></span>                    |
| <span data-ttu-id="d4336-217">Inn- og útskattur</span><span class="sxs-lookup"><span data-stu-id="d4336-217">Tax Payable/Receivable</span></span> | <span data-ttu-id="d4336-218">0</span><span class="sxs-lookup"><span data-stu-id="d4336-218">0</span></span>                          | <span data-ttu-id="d4336-219">0</span><span class="sxs-lookup"><span data-stu-id="d4336-219">0</span></span>                         | <span data-ttu-id="d4336-220">0.25</span><span class="sxs-lookup"><span data-stu-id="d4336-220">0.25</span></span>                     |

#### <a name="scenario-sales-tax-conversion--reporting-currency"></a><span data-ttu-id="d4336-221">Aðstæður: umreikningur virðisaukaskatts = „Skýrslugjaldmiðill”</span><span class="sxs-lookup"><span data-stu-id="d4336-221">Scenario: sales tax conversion = "Reporting currency"</span></span>


| <span data-ttu-id="d4336-222">Aðallykill</span><span class="sxs-lookup"><span data-stu-id="d4336-222">Main account</span></span>           | <span data-ttu-id="d4336-223">Færslugjaldmiðill (GBP)</span><span class="sxs-lookup"><span data-stu-id="d4336-223">Transaction currency (GBP)</span></span> | <span data-ttu-id="d4336-224">Bókhaldsgjaldmiðill (USD)</span><span class="sxs-lookup"><span data-stu-id="d4336-224">Accounting currency (USD)</span></span> | <span data-ttu-id="d4336-225">Skýrslugjaldmiðill (GBP)</span><span class="sxs-lookup"><span data-stu-id="d4336-225">Reporting currency (GBP)</span></span> |
| ---------------------- | -------------------------- | ------------------------- | ------------------------ |
| <span data-ttu-id="d4336-226">Inn- og útskattur</span><span class="sxs-lookup"><span data-stu-id="d4336-226">Tax Payable/Receivable</span></span> | <span data-ttu-id="d4336-227">-83</span><span class="sxs-lookup"><span data-stu-id="d4336-227">-83</span></span>                        | <span data-ttu-id="d4336-228">-110.67</span><span class="sxs-lookup"><span data-stu-id="d4336-228">-110.67</span></span>                   | <span data-ttu-id="d4336-229">-83</span><span class="sxs-lookup"><span data-stu-id="d4336-229">-83</span></span>                      |
| <span data-ttu-id="d4336-230">Skattauppgjör</span><span class="sxs-lookup"><span data-stu-id="d4336-230">Tax Settlement</span></span>         | <span data-ttu-id="d4336-231">83</span><span class="sxs-lookup"><span data-stu-id="d4336-231">83</span></span>                         | <span data-ttu-id="d4336-232">110.67</span><span class="sxs-lookup"><span data-stu-id="d4336-232">110.67</span></span>                    | <span data-ttu-id="d4336-233">83</span><span class="sxs-lookup"><span data-stu-id="d4336-233">83</span></span>                       |
| <span data-ttu-id="d4336-234">Innleystur hagnaður/tap</span><span class="sxs-lookup"><span data-stu-id="d4336-234">Realized Gain/Loss</span></span>     | <span data-ttu-id="d4336-235">0</span><span class="sxs-lookup"><span data-stu-id="d4336-235">0</span></span>                          | <span data-ttu-id="d4336-236">0.33</span><span class="sxs-lookup"><span data-stu-id="d4336-236">0.33</span></span>                      | <span data-ttu-id="d4336-237">0</span><span class="sxs-lookup"><span data-stu-id="d4336-237">0</span></span>                        |
| <span data-ttu-id="d4336-238">Inn- og útskattur</span><span class="sxs-lookup"><span data-stu-id="d4336-238">Tax Payable/Receivable</span></span> | <span data-ttu-id="d4336-239">0</span><span class="sxs-lookup"><span data-stu-id="d4336-239">0</span></span>                          | <span data-ttu-id="d4336-240">-0.33</span><span class="sxs-lookup"><span data-stu-id="d4336-240">-0.33</span></span>                     | <span data-ttu-id="d4336-241">0</span><span class="sxs-lookup"><span data-stu-id="d4336-241">0</span></span>                        |



<span data-ttu-id="d4336-242">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="d4336-242">For more information, see the following topics:</span></span>

- [<span data-ttu-id="d4336-243">Tvöfaldur gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d4336-243">Dual currency</span></span>](dual-currency.md)
- [<span data-ttu-id="d4336-244">Yfirlit virðisaukaskatts</span><span class="sxs-lookup"><span data-stu-id="d4336-244">Sales tax overview</span></span>](indirect-taxes-overview.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]