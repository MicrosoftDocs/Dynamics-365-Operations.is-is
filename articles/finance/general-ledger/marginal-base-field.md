---
title: Virðisaukaskattur byggður á jaðargrunns- og útreikningsaðferðum
description: Þetta efnisatriði útskýrir hvernig gildin í svæðunum jaðargrunnur og útreikningsaðferð ákvarða skatthlutfall í sölu- og innkaupafærslum.
author: ShylaThompson
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34e7e3f37d759953b7b4f70fe9eae78154da44d1
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178235"
---
# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a><span data-ttu-id="b1a5e-103">Virðisaukaskattur byggður á jaðargrunns- og útreikningsaðferðum</span><span class="sxs-lookup"><span data-stu-id="b1a5e-103">Sales tax rates based on the Marginal base and Calculation methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1a5e-104">Þetta efnisatriði útskýrir hvernig gildin í svæðunum jaðargrunnur og útreikningsaðferð ákvarða skatthlutfall í sölu- og innkaupafærslum.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-104">This topic explains how the values in the fields Marginal base and Calculation method determine the tax rate(s) in sales and purchase transactions.</span></span>

<span data-ttu-id="b1a5e-105">Jaðargrunnurinn á flýtiflipanum Útreikningur á síðunni VSK-kóðar ákvarðar hvaða upphæð er notuð til að velja viðeigandi skatthlutfall úr skatthlutfallinu á síðunni Gildi VSK-kóða.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-105">The Marginal base on the Calculation FastTab on the Sales tax codes page determines which amount is used to pick the appropriate tax rate(s) from the rates in the Sales tax code values page.</span></span> <span data-ttu-id="b1a5e-106">Gerð upphæðar í jaðargrunni ásamt aðferðinni í reitnum Útreikningsaðferð ákvarðar rökin til að finna rétt skatthlutfalls fyrir færslu.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-106">The amount type in the Marginal base field in combination with the method in the Calculation method field determines the logic to find the correct tax rate(s) for a transaction.</span></span> 

<span data-ttu-id="b1a5e-107">Mismunandi samsetning gilda í þessum svæðum leiðir til mjög ólíkra VSK-útreikninga, eins og sést í eftirfarandi dæmum.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-107">Various combinations of values in these fields produce very different sales tax calculations, as shown by the following examples.</span></span> <span data-ttu-id="b1a5e-108">Dæmin nota sömu gildi skattatímabila, sem eru sett upp fyrir hvern skattkóða á síðunni Gildi VSK-kóða.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-108">The examples use the same tax interval values, which are set up for each tax code in the Sales tax codes values page.</span></span> <span data-ttu-id="b1a5e-109">Til að opna þessa síðu er smellt á VSK-kóði &gt; Gildi á síðunni VSK-kóði.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-109">To open this page, click Sales tax code &gt; Values in the Sales tax codes page.</span></span>

> [!Important]                                                                                                                  
> <span data-ttu-id="b1a5e-110">Ef jaðargrunnurinn í einum eða fleiri VSK-kóðanna er byggður á línuupphæðum eða einingu, verður gildið í reitnum Útreikningsaðferð í skjámyndinni Færðibreytur fjárhags að vera stillt á Lína.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-110">If the Marginal base on one or more of your sales tax codes is based on line amounts or units, the value of the Calculation method field in the General ledger parameters page must be set to Line.</span></span> |

## <a name="net-amount-per-line"></a><span data-ttu-id="b1a5e-111">Nettóupphæð á línu</span><span class="sxs-lookup"><span data-stu-id="b1a5e-111">Net amount per line</span></span>
<span data-ttu-id="b1a5e-112">Veldu þennan valkost til að ákvarða hlutfall virðisaukaskatts byggðan á nettóupphæð í reikningslínum, án allra annarra skatta.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-112">Select this option to determine sales tax rates based on the net amount for the invoice lines, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="b1a5e-113">Dæmi</span><span class="sxs-lookup"><span data-stu-id="b1a5e-113">Example</span></span>

<span data-ttu-id="b1a5e-114">Skatthlutfall virðisaukaskatts eru sett upp í eftirfarandi tímabilum:</span><span class="sxs-lookup"><span data-stu-id="b1a5e-114">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="b1a5e-115">Upphæðarbil</span><span class="sxs-lookup"><span data-stu-id="b1a5e-115">Amount interval</span></span>    | <span data-ttu-id="b1a5e-116">Skatthlutfall</span><span class="sxs-lookup"><span data-stu-id="b1a5e-116">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="b1a5e-117">0 - 50</span><span class="sxs-lookup"><span data-stu-id="b1a5e-117">0 - 50</span></span>             | <span data-ttu-id="b1a5e-118">30%</span><span class="sxs-lookup"><span data-stu-id="b1a5e-118">30%</span></span>      |
| <span data-ttu-id="b1a5e-119">50 - 100</span><span class="sxs-lookup"><span data-stu-id="b1a5e-119">50 - 100</span></span>           | <span data-ttu-id="b1a5e-120">20%</span><span class="sxs-lookup"><span data-stu-id="b1a5e-120">20%</span></span>      |
| <span data-ttu-id="b1a5e-121">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="b1a5e-121">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="b1a5e-122">10%</span><span class="sxs-lookup"><span data-stu-id="b1a5e-122">10%</span></span>      |

> [!NOTE]                                                                                                             
> <span data-ttu-id="b1a5e-123">Efri mörkin núll (0) í síðasta tímabili þýðir að allar upphæðir yfir 100 eru hafðar með í bilinu.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-123">The upper limit of zero (0) in the last interval means that all amounts that exceed 100 are included in the interval.</span></span>

<span data-ttu-id="b1a5e-124">Jaðargrunnur: **Nettóupphæð á línu**</span><span class="sxs-lookup"><span data-stu-id="b1a5e-124">Marginal base: **Net amount per line**</span></span> 

<span data-ttu-id="b1a5e-125">Útreikningsaðferð: **Tímabil**</span><span class="sxs-lookup"><span data-stu-id="b1a5e-125">Calculation method: **Interval**</span></span> 

<span data-ttu-id="b1a5e-126">Keyptir eru 8 lampar sem kosta 25,00 hver.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-126">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="b1a5e-127">Nettóupphæðin fyrir reikningslínuna er 200,00.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-127">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="b1a5e-128">Skatturinn er reiknaður sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="b1a5e-128">The tax is calculated as follows:</span></span> 

<span data-ttu-id="b1a5e-129">Heildarsöluskattur = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span><span class="sxs-lookup"><span data-stu-id="b1a5e-129">Total sales tax = 50 x 30% + 50 x 20% + 100 x 10% = 15 + 10 + 10 = 35.00</span></span> 

<span data-ttu-id="b1a5e-130">Heildarupphæð reiknings = 200,00 + 35,00 = 235,00</span><span class="sxs-lookup"><span data-stu-id="b1a5e-130">Total invoice amount = 200.00 + 35.00 = 235.00</span></span> 

<span data-ttu-id="b1a5e-131">**Breytileiki**</span><span class="sxs-lookup"><span data-stu-id="b1a5e-131">**Variation**</span></span> 

<span data-ttu-id="b1a5e-132">Ef reikningur hefur tvær línur með fjórum atriðum í hverri línu er nettóupphæð í hverri línu 100,00 og virðisaukaskattur er reiknaður á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="b1a5e-132">If the invoice has two lines with four items on each line, the net amount on each line is 100.00 and the sales tax is calculated as follows:</span></span> 

<span data-ttu-id="b1a5e-133">Virðisaukaskattslína 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span><span class="sxs-lookup"><span data-stu-id="b1a5e-133">Sales tax line 1 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="b1a5e-134">Virðisaukaskattslína 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span><span class="sxs-lookup"><span data-stu-id="b1a5e-134">Sales tax line 2 = 50 x 30% + 50 x 20% = 15 + 10 = 25.00</span></span> 

<span data-ttu-id="b1a5e-135">Heildarupphæð virðisaukaskatts = 25,00 + 25,00 = 50,00</span><span class="sxs-lookup"><span data-stu-id="b1a5e-135">Total sales tax = 25.00 + 25.00 = 50.00</span></span> 

<span data-ttu-id="b1a5e-136">Heildarupphæð reiknings = 200,00 + 50,00 = 250,00</span><span class="sxs-lookup"><span data-stu-id="b1a5e-136">Total invoice amount = 200.00 + 50.00 = 250.00</span></span>

## <a name="net-amount-per-unit"></a><span data-ttu-id="b1a5e-137">Nettóupphæð á einingu</span><span class="sxs-lookup"><span data-stu-id="b1a5e-137">Net amount per unit</span></span>
<span data-ttu-id="b1a5e-138">Veldu þennan valkost til að ákvarða hlutfall virðisaukaskatts byggðan á gildi hverrar einingar, án allra annarra skatta.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-138">Select this option to determine sales tax rates based on the value of each unit, excluding any other taxes.</span></span> <span data-ttu-id="b1a5e-139">Þegar eining út jaðargrunnurinn er valin verður einnig að tilgreina einingu fyrir VSK-kóðann.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-139">When a unit based Marginal base is selected then also a Unit has to be specified for the Sales tax code.</span></span>

### <a name="example"></a><span data-ttu-id="b1a5e-140">Dæmi</span><span class="sxs-lookup"><span data-stu-id="b1a5e-140">Example</span></span>

<span data-ttu-id="b1a5e-141">Skatthlutfall virðisaukaskatts eru sett upp í eftirfarandi tímabilum:</span><span class="sxs-lookup"><span data-stu-id="b1a5e-141">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="b1a5e-142">Upphæð</span><span class="sxs-lookup"><span data-stu-id="b1a5e-142">Amount</span></span>             | <span data-ttu-id="b1a5e-143">Skatthlutfall</span><span class="sxs-lookup"><span data-stu-id="b1a5e-143">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="b1a5e-144">0 - 50</span><span class="sxs-lookup"><span data-stu-id="b1a5e-144">0 - 50</span></span>             | <span data-ttu-id="b1a5e-145">30%</span><span class="sxs-lookup"><span data-stu-id="b1a5e-145">30%</span></span>      |
| <span data-ttu-id="b1a5e-146">50 - 100</span><span class="sxs-lookup"><span data-stu-id="b1a5e-146">50 - 100</span></span>           | <span data-ttu-id="b1a5e-147">20%</span><span class="sxs-lookup"><span data-stu-id="b1a5e-147">20%</span></span>      |
| <span data-ttu-id="b1a5e-148">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="b1a5e-148">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="b1a5e-149">10%</span><span class="sxs-lookup"><span data-stu-id="b1a5e-149">10%</span></span>      |

<span data-ttu-id="b1a5e-150">Jaðargrunnur: **Nettóupphæð á einingu**</span><span class="sxs-lookup"><span data-stu-id="b1a5e-150">Marginal base: **Net amount per unit**</span></span> 

<span data-ttu-id="b1a5e-151">Reikningsaðferð: **Öll upphæðin**</span><span class="sxs-lookup"><span data-stu-id="b1a5e-151">Calculation method: **Whole amount**</span></span> 

<span data-ttu-id="b1a5e-152">Keyptir eru 8 lampar sem kosta 25,00 hver.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-152">You buy 8 lamps that cost 25.00 each.</span></span> 

<span data-ttu-id="b1a5e-153">Nettóupphæðin fyrir reikningslínuna er 200,00.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-153">The net amount for the invoice line is 200.00.</span></span> 

<span data-ttu-id="b1a5e-154">Skatturinn er reiknaður sem hér segir: VSK á einingu = 25,00 x 30% = 7,50 Heildarupphæð vsk = 7,50 x 8 einingar = 60,00 Heildarreikningsupphæð = 200,00 + 60,00 = 260,00</span><span class="sxs-lookup"><span data-stu-id="b1a5e-154">The tax is calculated as follows: Sales tax per unit = 25.00 x 30% = 7.50 Total sales tax = 7.50 x 8 units = 60.00 Total invoice amount = 200.00 + 60.00 = 260.00</span></span>

## <a name="net-amount-of-invoice-balance"></a><span data-ttu-id="b1a5e-155">Nettóupphæð af reikningsstöðu</span><span class="sxs-lookup"><span data-stu-id="b1a5e-155">Net amount of invoice balance</span></span>

<span data-ttu-id="b1a5e-156">Veldu þennan valkost til að ákvarða hlutfall virðisaukaskatts byggt á heildarvirði reikningsins, án allra annarra skatta.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-156">Select this option to determine sales tax rates based on the total value for the invoice, excluding any other taxes.</span></span>

### <a name="example"></a><span data-ttu-id="b1a5e-157">Dæmi</span><span class="sxs-lookup"><span data-stu-id="b1a5e-157">Example</span></span>

<span data-ttu-id="b1a5e-158">Skatthlutfall virðisaukaskatts eru sett upp í eftirfarandi tímabilum:</span><span class="sxs-lookup"><span data-stu-id="b1a5e-158">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="b1a5e-159">Upphæð</span><span class="sxs-lookup"><span data-stu-id="b1a5e-159">Amount</span></span>            | <span data-ttu-id="b1a5e-160">Skatthlutfall</span><span class="sxs-lookup"><span data-stu-id="b1a5e-160">Tax rate</span></span> |
|-------------------|----------|
| <span data-ttu-id="b1a5e-161">0 - 50</span><span class="sxs-lookup"><span data-stu-id="b1a5e-161">0 - 50</span></span>            | <span data-ttu-id="b1a5e-162">30%</span><span class="sxs-lookup"><span data-stu-id="b1a5e-162">30%</span></span>      |
| <span data-ttu-id="b1a5e-163">50 - 100</span><span class="sxs-lookup"><span data-stu-id="b1a5e-163">50 - 100</span></span>          | <span data-ttu-id="b1a5e-164">20%</span><span class="sxs-lookup"><span data-stu-id="b1a5e-164">20%</span></span>      |
| <span data-ttu-id="b1a5e-165">100 -0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="b1a5e-165">100 -0 (&gt; 100)</span></span> | <span data-ttu-id="b1a5e-166">10%</span><span class="sxs-lookup"><span data-stu-id="b1a5e-166">10%</span></span>      |

<span data-ttu-id="b1a5e-167">Jaðargrunnur: **Nettóupphæð af reikningsstöðu**</span><span class="sxs-lookup"><span data-stu-id="b1a5e-167">Marginal base: **Net amount of invoice balance**</span></span> 

<span data-ttu-id="b1a5e-168">Útreikningsaðferð: **Bil** Sölureikningur með 2 línur með 4 lampa hverja línur fyrir 25,00 hver.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-168">Calculation method: **Interval** A sales invoice has 2 lines with 4 lamps on each lines for 25.00 each.</span></span> <span data-ttu-id="b1a5e-169">Nettóupphæð af reikningsstöðu er 4 x 25,00 + 4 x 25,00 = 200,00.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-169">The net amount of invoice balance is 4 x 25.00 + 4 x 25.00 = 200.00.</span></span> <span data-ttu-id="b1a5e-170">Skatturinn er reiknaður sem hér segir: Heildarsöluskattur = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 +10 = 35,00 Heildarreikningsupphæð = 200,00 + 35,00 = 235,00</span><span class="sxs-lookup"><span data-stu-id="b1a5e-170">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 100 x 0.10 = 15 + 10 + 10 = 35.00 Total invoice amount = 200.00 + 35.00 = 235.00</span></span>

## <a name="gross-amount-per-line"></a><span data-ttu-id="b1a5e-171">Brúttó upphæð eftir línu</span><span class="sxs-lookup"><span data-stu-id="b1a5e-171">Gross amount per line</span></span>

<span data-ttu-id="b1a5e-172">Veldu þennan valkost til að ákvarða hlutfall virðisaukaskatts byggt á línunni, ásamt öllum öðrum sköttum fyrir línuna.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-172">Select this option to determine sales tax rates based on the value of the line including all other taxes for that line.</span></span>

> [!NOTE]
> <span data-ttu-id="b1a5e-173">Í VSK-flokki er aðeins hægt að hafa einn VSK-kóða með þessu vali í reitnum Jaðargrunnur.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-173">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="b1a5e-174">Dæmi</span><span class="sxs-lookup"><span data-stu-id="b1a5e-174">Example</span></span>

<span data-ttu-id="b1a5e-175">Skatthlutfall virðisaukaskatts eru sett upp í eftirfarandi tímabilum:</span><span class="sxs-lookup"><span data-stu-id="b1a5e-175">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="b1a5e-176">Upphæð</span><span class="sxs-lookup"><span data-stu-id="b1a5e-176">Amount</span></span>             | <span data-ttu-id="b1a5e-177">Skatthlutfall</span><span class="sxs-lookup"><span data-stu-id="b1a5e-177">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="b1a5e-178">0 - 50</span><span class="sxs-lookup"><span data-stu-id="b1a5e-178">0 - 50</span></span>             | <span data-ttu-id="b1a5e-179">30%</span><span class="sxs-lookup"><span data-stu-id="b1a5e-179">30%</span></span>      |
| <span data-ttu-id="b1a5e-180">50 - 100</span><span class="sxs-lookup"><span data-stu-id="b1a5e-180">50 - 100</span></span>           | <span data-ttu-id="b1a5e-181">20%</span><span class="sxs-lookup"><span data-stu-id="b1a5e-181">20%</span></span>      |
| <span data-ttu-id="b1a5e-182">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="b1a5e-182">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="b1a5e-183">10%</span><span class="sxs-lookup"><span data-stu-id="b1a5e-183">10%</span></span>      |

<span data-ttu-id="b1a5e-184">Jaðargrunnurinn: **Brúttóupphæð eftir línu** Útreikningsaðferð: **Bil** Þar að auki er annar VSK-kóði reiknaður fyrir sérstakt gjald upp á 5,00 fyrir hvern lampa.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-184">Marginal base: **Gross amount per line** Calculation method: **Interval** Additionally there is another tax code calculated for a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="b1a5e-185">Gjaldinu er bætt við nettóupphæðina áður en VSK er reiknaður út.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-185">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="b1a5e-186">Keyptir eru 8 lampar sem kosta 25,00 hver.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-186">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="b1a5e-187">Nettóupphæðin fyrir reikningslínuna er 200,00.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-187">The net amount for the invoice line is 200.00.</span></span> <span data-ttu-id="b1a5e-188">Brúttóupphæð fyrir reikningslínuna er 8 x 25,00 + 8 x 5,00 = 240,00.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-188">The gross amount for the invoice line is 8 x 25.00 + 8 x 5.00 = 240.00.</span></span> <span data-ttu-id="b1a5e-189">Skatturinn er reiknaður sem hér segir: Heildarvirðisaukaskattur = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Heildargjöld = 5,00 x 8 = 40,00 Heildarreikningsupphæð = 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="b1a5e-189">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 20 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="b1a5e-190">**Breytileiki**</span><span class="sxs-lookup"><span data-stu-id="b1a5e-190">**Variation**</span></span> 

<span data-ttu-id="b1a5e-191">Ef reikningur er stofnaður með því að nota 2 reikningslínur með 4 vörum í hverri línu er nettóupphæð fyrir línu 100,00.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-191">If the invoice is created by using 2 invoice lines with 4 items on each line, the net amount per invoice line is 100.00.</span></span> <span data-ttu-id="b1a5e-192">Brúttóupphæð (með gjaldi 4 x 5,00) hverrar reikningslínu væri 120,00 og VSK er stofnuður á eftirfarandi hátt: Lína VSK-reiknings 1 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Lína VSK-reiknings 2 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Samtals virðisaukaskattur = 27,00 + 27,00 = 54,00 Heildargjöld = 5,00 x 8 = 40,00 Heildarreikningsupphæð = 200,00 + 54,00 + 40,00 = 294,00</span><span class="sxs-lookup"><span data-stu-id="b1a5e-192">The gross amount (including the duty of 4 x 5.00) per invoice line would be 120.00, and the sales tax is created as follows: Sales tax invoice line 1 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Sales tax invoice line 2 = 50 x 0.30 + 50 x 0.20 + 20 x 0.10 = 15 + 10 + 2 = 27.00 Total sales tax = 27.00 + 27.00 = 54.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 54.00 + 40.00 = 294.00</span></span>

## <a name="gross-amount-per-unit"></a><span data-ttu-id="b1a5e-193">Brúttó upphæð á einingu</span><span class="sxs-lookup"><span data-stu-id="b1a5e-193">Gross amount per unit</span></span>

<span data-ttu-id="b1a5e-194">Veldu þennan valkost til að ákvarða hlutfall virðisaukaskatts byggðan á einingunni, ásamt öllum öðrum sköttum.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-194">Select this option to determine sales tax rates based on the value of the unit including any other taxes.</span></span>

> [!NOTE]
> <span data-ttu-id="b1a5e-195">Í VSK-flokki er aðeins hægt að hafa einn VSK-kóða með þessu vali í reitnum Jaðargrunnur.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-195">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field.</span></span>

### <a name="example"></a><span data-ttu-id="b1a5e-196">Dæmi</span><span class="sxs-lookup"><span data-stu-id="b1a5e-196">Example</span></span>

<span data-ttu-id="b1a5e-197">Skatthlutfall virðisaukaskatts eru sett upp í eftirfarandi tímabilum:</span><span class="sxs-lookup"><span data-stu-id="b1a5e-197">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="b1a5e-198">Upphæð</span><span class="sxs-lookup"><span data-stu-id="b1a5e-198">Amount</span></span>             | <span data-ttu-id="b1a5e-199">Skatthlutfall</span><span class="sxs-lookup"><span data-stu-id="b1a5e-199">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="b1a5e-200">0 - 50</span><span class="sxs-lookup"><span data-stu-id="b1a5e-200">0 - 50</span></span>             | <span data-ttu-id="b1a5e-201">30%</span><span class="sxs-lookup"><span data-stu-id="b1a5e-201">30%</span></span>      |
| <span data-ttu-id="b1a5e-202">50 - 100</span><span class="sxs-lookup"><span data-stu-id="b1a5e-202">50 - 100</span></span>           | <span data-ttu-id="b1a5e-203">20%</span><span class="sxs-lookup"><span data-stu-id="b1a5e-203">20%</span></span>      |
| <span data-ttu-id="b1a5e-204">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="b1a5e-204">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="b1a5e-205">10%</span><span class="sxs-lookup"><span data-stu-id="b1a5e-205">10%</span></span>      |

<span data-ttu-id="b1a5e-206">Jaðargrunnurinn: **Brúttóupphæð á einingu** Það er sérstakt gjald upp á 5,00 fyrir hvern lampa.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-206">Marginal base: **Gross amount per unit** There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="b1a5e-207">Gjaldinu er bætt við nettóupphæðina áður en VSK er reiknaður út.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-207">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="b1a5e-208">Keyptir eru 8 lampar sem kosta 25,00 hver.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-208">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="b1a5e-209">Brúttóupphæð á einingu er 30,00.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-209">The gross amount per unit is 30.00.</span></span> <span data-ttu-id="b1a5e-210">Skatturinn er reiknaður sem hér segir: Virðisaukaskattur á einingu = 30 x 30% = 9,00 Heildarvirðisaukaskattur = 9,00 x 8 = 72,00 Heildargjöld = 5,00 x 8 + 40,00 Heildarreikningsupphæð = 200,00 + 72,00 + 40,00 = 312,00</span><span class="sxs-lookup"><span data-stu-id="b1a5e-210">The tax is calculated as follows: Sales tax per unit = 30 x 30% = 9.00 Total sales tax = 9.00 x 8 = 72.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 72.00 + 40.00 = 312.00</span></span>

## <a name="invoice-total-incl-other-sales-tax-amounts"></a><span data-ttu-id="b1a5e-211">Samtala reiknings að meðtöldum öðrum VSK-upphæðum</span><span class="sxs-lookup"><span data-stu-id="b1a5e-211">Invoice total incl. other sales tax amounts</span></span>

<span data-ttu-id="b1a5e-212">Veldu þennan valkost til að ákvarða hlutfall virðisaukaskatts byggt á heildarvirði reikningsins, ásamt öllum öðrum sköttum.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-212">Select this option to determine sales tax rates based on the total value for the invoice including any other taxes.</span></span>
> [!NOTE]
> <span data-ttu-id="b1a5e-213">Í VSK-flokki er aðeins hægt að hafa einn VSK-kóða með þessu vali í reitnum Jaðargrunnur</span><span class="sxs-lookup"><span data-stu-id="b1a5e-213">In a sales tax group, you can only have one sales tax code with this selection in the Marginal base field</span></span>

### <a name="example"></a><span data-ttu-id="b1a5e-214">Dæmi</span><span class="sxs-lookup"><span data-stu-id="b1a5e-214">Example</span></span>

<span data-ttu-id="b1a5e-215">Skatthlutfall virðisaukaskatts eru sett upp í eftirfarandi tímabilum:</span><span class="sxs-lookup"><span data-stu-id="b1a5e-215">The sales tax rates are set up in the following intervals.</span></span>

| <span data-ttu-id="b1a5e-216">Upphæð</span><span class="sxs-lookup"><span data-stu-id="b1a5e-216">Amount</span></span>             | <span data-ttu-id="b1a5e-217">Skatthlutfall</span><span class="sxs-lookup"><span data-stu-id="b1a5e-217">Tax rate</span></span> |
|--------------------|----------|
| <span data-ttu-id="b1a5e-218">0 - 50</span><span class="sxs-lookup"><span data-stu-id="b1a5e-218">0 - 50</span></span>             | <span data-ttu-id="b1a5e-219">30%</span><span class="sxs-lookup"><span data-stu-id="b1a5e-219">30%</span></span>      |
| <span data-ttu-id="b1a5e-220">50 - 100</span><span class="sxs-lookup"><span data-stu-id="b1a5e-220">50 - 100</span></span>           | <span data-ttu-id="b1a5e-221">20%</span><span class="sxs-lookup"><span data-stu-id="b1a5e-221">20%</span></span>      |
| <span data-ttu-id="b1a5e-222">100 - 0 (&gt; 100)</span><span class="sxs-lookup"><span data-stu-id="b1a5e-222">100 - 0 (&gt; 100)</span></span> | <span data-ttu-id="b1a5e-223">10%</span><span class="sxs-lookup"><span data-stu-id="b1a5e-223">10%</span></span>      |

<span data-ttu-id="b1a5e-224">Jaðargrunnur: **Heildarupphæð reiknings að meðtöldum öðrum VSK-upphæðum** Útreikningsaðferð: **Bil** </span><span class="sxs-lookup"><span data-stu-id="b1a5e-224">Marginal base: **Invoice total incl. other sales tax amounts** Calculation method: **Interval** </span></span>  
<span data-ttu-id="b1a5e-225">Það er sérstakt gjald upp á 5,00 fyrir hvern lampa.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-225">There is a special duty of 5.00 on each lamp.</span></span> <span data-ttu-id="b1a5e-226">Gjaldinu er bætt við nettóupphæðina áður en VSK er reiknaður út.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-226">The duty is added to the net amount before the sales tax calculation.</span></span> <span data-ttu-id="b1a5e-227">Keyptir eru 8 lampar sem kosta 25,00 hver.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-227">You buy 8 lamps that cost 25.00 each.</span></span> <span data-ttu-id="b1a5e-228">Nettóupphæðin fyrir reikning er 200,00.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-228">The net amount for the invoice is 200.00.</span></span> <span data-ttu-id="b1a5e-229">Brúttóupphæð fyrir reikningslínuna er 200,00 + (8 x 5,00) = 240,00.</span><span class="sxs-lookup"><span data-stu-id="b1a5e-229">The gross amount for the invoice is 200.00 + (8 x 5.00) = 240.00.</span></span> <span data-ttu-id="b1a5e-230">Skatturinn er reiknaður sem hér segir: Heildarvirðisaukaskattur = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Heildargjöld = 5,00 x 8 = 40,00 Heildarreikningsupphæð = 200,00 + 39,00 + 40,00 = 279,00</span><span class="sxs-lookup"><span data-stu-id="b1a5e-230">The tax is calculated as follows: Total sales tax = 50 x 0.30 + 50 x 0.20 + 140 x 0.10 = 15 + 10 + 14 = 39.00 Total duty = 5.00 x 8 = 40.00 Total invoice amount = 200.00 + 39.00 + 40.00 = 279.00</span></span>

<span data-ttu-id="b1a5e-231">Frekari upplýsingar eru í [Útreikningsaðferð heildarupphæðar og tímabils fyrir VSK-kóða](whole-amount-interval-options-sales-tax-codes.md) og [Aðferðir útreiknings VSK í upprunareitnum](sales-tax-calculation-methods-origin-field.md)</span><span class="sxs-lookup"><span data-stu-id="b1a5e-231">For more information, see [Whole amount and Interval calculation options for sales tax codes](whole-amount-interval-options-sales-tax-codes.md) and [Sales tax calculation methods in the Origin field](sales-tax-calculation-methods-origin-field.md).</span></span>


