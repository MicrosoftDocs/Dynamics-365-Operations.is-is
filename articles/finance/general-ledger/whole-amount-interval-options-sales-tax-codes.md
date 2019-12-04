---
title: Útreikningsaðferð heildarupphæðar og tímabils fyrir vsk-kóða
description: Þessi grein útskýrir hvernig valkostir fyrir svæðið Útreikningsaðferðir hafa áhrif á virðisaukaskattskóða og hvernig virðisaukaskattur er reiknaður fyrir tímabil og fullar upphæðir.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxData, TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 5624
ms.assetid: 96166db4-b7ca-470b-aeb7-0a66fe0554c4
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d452ccc94324a695f0d203486fc5fa8fe9db79f6
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770552"
---
# <a name="whole-amount-and-interval-calculation-options-for-sales-tax-codes"></a><span data-ttu-id="da18f-103">Útreikningsaðferð heildarupphæðar og tímabils fyrir vsk-kóða</span><span class="sxs-lookup"><span data-stu-id="da18f-103">Whole amount and Interval calculation options for sales tax codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da18f-104">Þessi grein útskýrir hvernig valkostir fyrir svæðið Útreikningsaðferðir hafa áhrif á virðisaukaskattskóða og hvernig virðisaukaskattur er reiknaður fyrir tímabil og fullar upphæðir.</span><span class="sxs-lookup"><span data-stu-id="da18f-104">This article explains the options for the Calculation method field on sales tax codes and how sales tax is calculated for intervals and whole amounts.</span></span>

<span data-ttu-id="da18f-105">Hægt er að setja upp vsk-kóða til að reikna út byggt á heildarupphæð eða tímabilsupphæð.</span><span class="sxs-lookup"><span data-stu-id="da18f-105">You can set up a sales tax code to be calculated based on a whole amount or an interval amount.</span></span> <span data-ttu-id="da18f-106">Í síðu vsk kóða, skal nota aðferð Útreiknings svæðið á Flýtiflipanum Útreikningur til að velja hvernig á að reikna vsk-kóða.</span><span class="sxs-lookup"><span data-stu-id="da18f-106">In the Sales tax codes page, use the Calculation method field on the Calculation FastTab to select how to calculate a sales tax code.</span></span>
- <span data-ttu-id="da18f-107">Heildarupphæð – Skatthlutfall er notað fyrir alla skattskyldu upphæðina.</span><span class="sxs-lookup"><span data-stu-id="da18f-107">Whole amount – The tax rate is applied to the whole taxable amount.</span></span>
- <span data-ttu-id="da18f-108">Tímabil – Skattskyldu upphæðinni er skipt í hluta, en hver þeirra fellur undir upphæðarbil með sérstöku skatthlutfalli.</span><span class="sxs-lookup"><span data-stu-id="da18f-108">Interval – The taxable amount is divided into parts, each of which falls in a range that has a specific sales tax rate.</span></span> <span data-ttu-id="da18f-109">Hlutur upphæðarinnar sem fellur undir tiltekið bil er skattlagt í samræmi við skatthlutfallið fyrir það bil.</span><span class="sxs-lookup"><span data-stu-id="da18f-109">The part of the amount that falls in a given interval is taxed according to the tax rate for that interval.</span></span> <span data-ttu-id="da18f-110">Virðisaukaskatturinn er samtala skattupphæðanna sem eru reiknaðar fyrir hvert upphæðarbil.</span><span class="sxs-lookup"><span data-stu-id="da18f-110">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>
  > [!NOTE]                                                                                                                              
  > <span data-ttu-id="da18f-111">valkostur tímabils er aðeins tiltækt þegar Lína er valin í svæðinu Útreikningsaðferð í svæðinu virðisaukaskattur af síðunni færibreytur fjárhags.</span><span class="sxs-lookup"><span data-stu-id="da18f-111">The Interval option is available only when you select Line in the Calculation method field in the Sales tax area of the General ledger parameters page.</span></span> 

<span data-ttu-id="da18f-112">Tímabil eru sett upp í síðunni gildi virðisaukaskatts með því að færa inn Lágmarks og Hámarks upphæðir fyrir hvern skatthlutfall.</span><span class="sxs-lookup"><span data-stu-id="da18f-112">Intervals are set up in the Sales tax code values page by entering Minimum and Maximum limit amounts per tax rate.</span></span> <span data-ttu-id="da18f-113">Til þess að geta reiknað skatt af öllum skattskyldum upphæðum, óháð því hvaða útreikningsaðferð er valin, verða bil að vera samkvæmt eftirfarandi reglum:</span><span class="sxs-lookup"><span data-stu-id="da18f-113">For taxes to be calculated on all taxable amounts, regardless of which calculation method is selected, intervals must follow these rules:</span></span>
-   <span data-ttu-id="da18f-114">Fyrsta bilið verður að vera með lágmark núll.</span><span class="sxs-lookup"><span data-stu-id="da18f-114">The first interval must have a Minimum limit of zero.</span></span>
-   <span data-ttu-id="da18f-115">Síðasta bilið verður að hafa hámark núll, sem gefur til kynna óendanleika.</span><span class="sxs-lookup"><span data-stu-id="da18f-115">The last interval must have a Maximum limit of zero, which indicates infinity.</span></span>
-   <span data-ttu-id="da18f-116">Hámark bils verður að vera Lágmark næsta bils.</span><span class="sxs-lookup"><span data-stu-id="da18f-116">The Maximum limit of an interval must be the Minimum limit of the next interval.</span></span>

<span data-ttu-id="da18f-117">Ef upphæð er hámark fyrra bils og lágmark næsta bils, mun söluskattshlutfallið fyrir fyrsta bilið vera beitt á upphæðina.</span><span class="sxs-lookup"><span data-stu-id="da18f-117">If an amount is the Maximum limit of the previous interval and the Minimum limit of the next interval, the sales tax rate of the first interval will be applied to the amount.</span></span> <span data-ttu-id="da18f-118">Ef upphæð fellur utan við bil sem eru skilgreind með efri og neðri mörkum, er söluskatthlutfallið núll notað.</span><span class="sxs-lookup"><span data-stu-id="da18f-118">If an amount falls outside the intervals that are defined by upper and lower limits, a sales tax rate of zero will be applied.</span></span>

## <a name="example-whole-amount-method-of-calculation"></a><span data-ttu-id="da18f-119">Útreikningsaðferð heildarupphæðar: Dæmi</span><span class="sxs-lookup"><span data-stu-id="da18f-119">Example: Whole amount method of calculation</span></span>
<span data-ttu-id="da18f-120">Í síðunni gildi VSK-kóði, eru Skatthlutfall virðisaukaskatts sett upp í eftirfarandi tímabilum:</span><span class="sxs-lookup"><span data-stu-id="da18f-120">In the Sales tax code values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="da18f-121">**Neðri mörk**</span><span class="sxs-lookup"><span data-stu-id="da18f-121">**Minimum limit**</span></span> | <span data-ttu-id="da18f-122">**Hámarksgildi**</span><span class="sxs-lookup"><span data-stu-id="da18f-122">**Maximum limit**</span></span> | <span data-ttu-id="da18f-123">**Skatthlutfall**</span><span class="sxs-lookup"><span data-stu-id="da18f-123">**Tax rate**</span></span> |
| <span data-ttu-id="da18f-124">0,00</span><span class="sxs-lookup"><span data-stu-id="da18f-124">0.00</span></span>              | <span data-ttu-id="da18f-125">50,00</span><span class="sxs-lookup"><span data-stu-id="da18f-125">50.00</span></span>             | <span data-ttu-id="da18f-126">30%</span><span class="sxs-lookup"><span data-stu-id="da18f-126">30%</span></span>          |
| <span data-ttu-id="da18f-127">50,00</span><span class="sxs-lookup"><span data-stu-id="da18f-127">50.00</span></span>             | <span data-ttu-id="da18f-128">100,00</span><span class="sxs-lookup"><span data-stu-id="da18f-128">100.00</span></span>            | <span data-ttu-id="da18f-129">20%</span><span class="sxs-lookup"><span data-stu-id="da18f-129">20%</span></span>          |
| <span data-ttu-id="da18f-130">100,00</span><span class="sxs-lookup"><span data-stu-id="da18f-130">100.00</span></span>            | <span data-ttu-id="da18f-131">0,00</span><span class="sxs-lookup"><span data-stu-id="da18f-131">0.00</span></span>              | <span data-ttu-id="da18f-132">10%</span><span class="sxs-lookup"><span data-stu-id="da18f-132">10%</span></span>          |

<span data-ttu-id="da18f-133">virðisaukaskattur er reiknaður af allri skattskyldri upphæð.</span><span class="sxs-lookup"><span data-stu-id="da18f-133">The sales tax is calculated on the whole taxable amount.</span></span>

| <span data-ttu-id="da18f-134">Skattskyld upphæð (verð)</span><span class="sxs-lookup"><span data-stu-id="da18f-134">Taxable amount (price)</span></span> | <span data-ttu-id="da18f-135">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="da18f-135">Calculation</span></span>    | <span data-ttu-id="da18f-136">Virðisaukaskattur</span><span class="sxs-lookup"><span data-stu-id="da18f-136">Sales tax</span></span> |
|------------------------|----------------|-----------|
| <span data-ttu-id="da18f-137">35,00</span><span class="sxs-lookup"><span data-stu-id="da18f-137">35.00</span></span>                  | <span data-ttu-id="da18f-138">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="da18f-138">35.00 \* 0.30</span></span>  | <span data-ttu-id="da18f-139">10,50</span><span class="sxs-lookup"><span data-stu-id="da18f-139">10.50</span></span>     |
| <span data-ttu-id="da18f-140">50,00</span><span class="sxs-lookup"><span data-stu-id="da18f-140">50.00</span></span>                  | <span data-ttu-id="da18f-141">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="da18f-141">50.00 \* 0.30</span></span>  | <span data-ttu-id="da18f-142">15:00</span><span class="sxs-lookup"><span data-stu-id="da18f-142">15.00</span></span>     |
| <span data-ttu-id="da18f-143">85,00</span><span class="sxs-lookup"><span data-stu-id="da18f-143">85.00</span></span>                  | <span data-ttu-id="da18f-144">85,00 \* 0,20</span><span class="sxs-lookup"><span data-stu-id="da18f-144">85.00 \* 0.20</span></span>  | <span data-ttu-id="da18f-145">17,00</span><span class="sxs-lookup"><span data-stu-id="da18f-145">17.00</span></span>     |
| <span data-ttu-id="da18f-146">305,00</span><span class="sxs-lookup"><span data-stu-id="da18f-146">305.00</span></span>                 | <span data-ttu-id="da18f-147">305,00 \* 0,10</span><span class="sxs-lookup"><span data-stu-id="da18f-147">305.00 \* 0.10</span></span> | <span data-ttu-id="da18f-148">30,50</span><span class="sxs-lookup"><span data-stu-id="da18f-148">30.50</span></span>     |

## <a name="example-interval-method-of-calculation"></a><span data-ttu-id="da18f-149">Útreikningsaðferð tímabila: Dæmi</span><span class="sxs-lookup"><span data-stu-id="da18f-149">Example: Interval method of calculation</span></span>
<span data-ttu-id="da18f-150">Í síðunni gildi, eru Skatthlutfall virðisaukaskatts sett upp í eftirfarandi tímabilum:</span><span class="sxs-lookup"><span data-stu-id="da18f-150">In the Values page, sales tax rates are set up in the following intervals:</span></span>

|                   |                   |              |
|-------------------|-------------------|--------------|
| <span data-ttu-id="da18f-151">**Neðri mörk**</span><span class="sxs-lookup"><span data-stu-id="da18f-151">**Minimum limit**</span></span> | <span data-ttu-id="da18f-152">**Hámarksgildi**</span><span class="sxs-lookup"><span data-stu-id="da18f-152">**Maximum limit**</span></span> | <span data-ttu-id="da18f-153">**Skatthlutfall**</span><span class="sxs-lookup"><span data-stu-id="da18f-153">**Tax rate**</span></span> |
| <span data-ttu-id="da18f-154">0,00</span><span class="sxs-lookup"><span data-stu-id="da18f-154">0.00</span></span>              | <span data-ttu-id="da18f-155">50,00</span><span class="sxs-lookup"><span data-stu-id="da18f-155">50.00</span></span>             | <span data-ttu-id="da18f-156">30%</span><span class="sxs-lookup"><span data-stu-id="da18f-156">30%</span></span>          |
| <span data-ttu-id="da18f-157">50,00</span><span class="sxs-lookup"><span data-stu-id="da18f-157">50.00</span></span>             | <span data-ttu-id="da18f-158">100,00</span><span class="sxs-lookup"><span data-stu-id="da18f-158">100.00</span></span>            | <span data-ttu-id="da18f-159">20%</span><span class="sxs-lookup"><span data-stu-id="da18f-159">20%</span></span>          |
| <span data-ttu-id="da18f-160">100,00</span><span class="sxs-lookup"><span data-stu-id="da18f-160">100.00</span></span>            | <span data-ttu-id="da18f-161">0,00</span><span class="sxs-lookup"><span data-stu-id="da18f-161">0.00</span></span>              | <span data-ttu-id="da18f-162">10%</span><span class="sxs-lookup"><span data-stu-id="da18f-162">10%</span></span>          |

<span data-ttu-id="da18f-163">Virðisaukaskatturinn er samtala skattupphæðanna sem eru reiknaðar fyrir hvert upphæðarbil.</span><span class="sxs-lookup"><span data-stu-id="da18f-163">The sales tax is the sum of the tax amounts that are calculated for each amount interval.</span></span>

| <span data-ttu-id="da18f-164">Skattskyld upphæð (verð)</span><span class="sxs-lookup"><span data-stu-id="da18f-164">Taxable amount (price)</span></span> | <span data-ttu-id="da18f-165">Útreikningur</span><span class="sxs-lookup"><span data-stu-id="da18f-165">Calculation</span></span>                                                               | <span data-ttu-id="da18f-166">Virðisaukaskattur</span><span class="sxs-lookup"><span data-stu-id="da18f-166">Sales tax</span></span> |
|------------------------|---------------------------------------------------------------------------|-----------|
| <span data-ttu-id="da18f-167">35,00</span><span class="sxs-lookup"><span data-stu-id="da18f-167">35.00</span></span>                  | <span data-ttu-id="da18f-168">35,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="da18f-168">35.00 \* 0.30</span></span>                                                             | <span data-ttu-id="da18f-169">10,50</span><span class="sxs-lookup"><span data-stu-id="da18f-169">10.50</span></span>     |
| <span data-ttu-id="da18f-170">50,00</span><span class="sxs-lookup"><span data-stu-id="da18f-170">50.00</span></span>                  | <span data-ttu-id="da18f-171">50,00 \* 0,30</span><span class="sxs-lookup"><span data-stu-id="da18f-171">50.00 \* 0.30</span></span>                                                             | <span data-ttu-id="da18f-172">15:00</span><span class="sxs-lookup"><span data-stu-id="da18f-172">15.00</span></span>     |
| <span data-ttu-id="da18f-173">85,00</span><span class="sxs-lookup"><span data-stu-id="da18f-173">85.00</span></span>                  | <span data-ttu-id="da18f-174">(50,00 \* 0,30 = 15,00) + (35,00 \* 0,20 = 7,00)</span><span class="sxs-lookup"><span data-stu-id="da18f-174">(50.00 \* 0.30 = 15.00) + (35.00 \* 0.20 = 7.00)</span></span>                          | <span data-ttu-id="da18f-175">22,00</span><span class="sxs-lookup"><span data-stu-id="da18f-175">22.00</span></span>     |
| <span data-ttu-id="da18f-176">305,00</span><span class="sxs-lookup"><span data-stu-id="da18f-176">305.00</span></span>                 | <span data-ttu-id="da18f-177">(50,00 \* 0,30 = 15,00) + (50,00 \* 0,20 = 10,00) + (205 \* 0,10 = 20,50)</span><span class="sxs-lookup"><span data-stu-id="da18f-177">(50.00 \* 0.30 = 15.00) + (50.00 \* 0.20 = 10.00) + (205 \* 0.10 = 20.50)</span></span> | <span data-ttu-id="da18f-178">45.50</span><span class="sxs-lookup"><span data-stu-id="da18f-178">45.50</span></span>     |



<span data-ttu-id="da18f-179">Nánari upplýsingar er að finna í [Skatthlutfall virðisaukaskatts á grundvelli Jaðargrunns og Útreikningsaðferðar](marginal-base-field.md)</span><span class="sxs-lookup"><span data-stu-id="da18f-179">For more information, see [Sales tax rates based on the Marginal base and Calculation methods](marginal-base-field.md).</span></span>





