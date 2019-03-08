---
title: Áskriftarsöluverð
description: Þegar þú stofnar áskrift er söluverðið byggt á uppsetningu söluverðs sem var stofnað í skjámyndinni „Söluverð (áskrift)“.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e18690f7e9b790ecbd0ac0de1955fc95ab1f082
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2019
ms.locfileid: "352161"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="c5625-103">Áskriftarsöluverð</span><span class="sxs-lookup"><span data-stu-id="c5625-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="c5625-104">Þegar þú stofnar áskrift er söluverðið byggt á uppsetningu söluverðs sem var stofnað í skjámyndinni **Söluverð (áskrift)**.</span><span class="sxs-lookup"><span data-stu-id="c5625-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="c5625-105">Í skjámyndinni **Söluverði (áskrift)** getur þú stofnað söluverð fyrir tiltekna áskrift eða þú getur stofnað söluverð sem gilda í víðara samhengi.</span><span class="sxs-lookup"><span data-stu-id="c5625-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="c5625-106">Til þess að söluverð verði notað á áskrift skal tímabilskóðinn og gjaldmiðill áskriftarinnar vera eins og tímabilskóði og gjaldmiðill söluverðsins.</span><span class="sxs-lookup"><span data-stu-id="c5625-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="c5625-107">Ef tímabilskóði og gjaldmiðill eru eins fyrir áskrift og söluverð eru áskriftarsöluverð valin á grundvelli forgangsröðunar sem er að finna í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="c5625-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="c5625-108">Autt hólf í töflunni gefur til kynna tóman reit og X gefur til kynna gildi sem er jafnt gildinu í áskriftinni þar sem færslan er mynduð.</span><span class="sxs-lookup"><span data-stu-id="c5625-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5625-109">Forgangur </span><span class="sxs-lookup"><span data-stu-id="c5625-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="c5625-110"><strong>Tegund</strong></span><span class="sxs-lookup"><span data-stu-id="c5625-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="c5625-111"><strong>Kenni verks</strong></span><span class="sxs-lookup"><span data-stu-id="c5625-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="c5625-112"><strong>Áskrift</strong></span><span class="sxs-lookup"><span data-stu-id="c5625-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="c5625-113"><strong>Sölugjaldmiðill</strong></span><span class="sxs-lookup"><span data-stu-id="c5625-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="c5625-114"><strong>Tímabilskóði</strong></span><span class="sxs-lookup"><span data-stu-id="c5625-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5625-115">1</span><span class="sxs-lookup"><span data-stu-id="c5625-115">1</span></span></p></td>
<td><p><span data-ttu-id="c5625-116">X</span><span class="sxs-lookup"><span data-stu-id="c5625-116">X</span></span></p></td>
<td><p><span data-ttu-id="c5625-117">X</span><span class="sxs-lookup"><span data-stu-id="c5625-117">X</span></span></p></td>
<td><p><span data-ttu-id="c5625-118">X</span><span class="sxs-lookup"><span data-stu-id="c5625-118">X</span></span></p></td>
<td><p><span data-ttu-id="c5625-119">X</span><span class="sxs-lookup"><span data-stu-id="c5625-119">X</span></span></p></td>
<td><p><span data-ttu-id="c5625-120">X</span><span class="sxs-lookup"><span data-stu-id="c5625-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5625-121">2</span><span class="sxs-lookup"><span data-stu-id="c5625-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="c5625-122">X</span><span class="sxs-lookup"><span data-stu-id="c5625-122">X</span></span></p></td>
<td><p><span data-ttu-id="c5625-123">X</span><span class="sxs-lookup"><span data-stu-id="c5625-123">X</span></span></p></td>
<td><p><span data-ttu-id="c5625-124">X</span><span class="sxs-lookup"><span data-stu-id="c5625-124">X</span></span></p></td>
<td><p><span data-ttu-id="c5625-125">X</span><span class="sxs-lookup"><span data-stu-id="c5625-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5625-126">3</span><span class="sxs-lookup"><span data-stu-id="c5625-126">3</span></span></p></td>
<td><p><span data-ttu-id="c5625-127">X</span><span class="sxs-lookup"><span data-stu-id="c5625-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="c5625-128">X</span><span class="sxs-lookup"><span data-stu-id="c5625-128">X</span></span></p></td>
<td><p><span data-ttu-id="c5625-129">X</span><span class="sxs-lookup"><span data-stu-id="c5625-129">X</span></span></p></td>
<td><p><span data-ttu-id="c5625-130">X</span><span class="sxs-lookup"><span data-stu-id="c5625-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5625-131">4</span><span class="sxs-lookup"><span data-stu-id="c5625-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="c5625-132">X</span><span class="sxs-lookup"><span data-stu-id="c5625-132">X</span></span></p></td>
<td><p><span data-ttu-id="c5625-133">X</span><span class="sxs-lookup"><span data-stu-id="c5625-133">X</span></span></p></td>
<td><p><span data-ttu-id="c5625-134">X</span><span class="sxs-lookup"><span data-stu-id="c5625-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5625-135">5</span><span class="sxs-lookup"><span data-stu-id="c5625-135">5</span></span></p></td>
<td><p><span data-ttu-id="c5625-136">X</span><span class="sxs-lookup"><span data-stu-id="c5625-136">X</span></span></p></td>
<td><p><span data-ttu-id="c5625-137">X</span><span class="sxs-lookup"><span data-stu-id="c5625-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="c5625-138">X</span><span class="sxs-lookup"><span data-stu-id="c5625-138">X</span></span></p></td>
<td><p><span data-ttu-id="c5625-139">X</span><span class="sxs-lookup"><span data-stu-id="c5625-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5625-140">6</span><span class="sxs-lookup"><span data-stu-id="c5625-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="c5625-141">X</span><span class="sxs-lookup"><span data-stu-id="c5625-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="c5625-142">X</span><span class="sxs-lookup"><span data-stu-id="c5625-142">X</span></span></p></td>
<td><p><span data-ttu-id="c5625-143">X</span><span class="sxs-lookup"><span data-stu-id="c5625-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c5625-144">7</span><span class="sxs-lookup"><span data-stu-id="c5625-144">7</span></span></p></td>
<td><p><span data-ttu-id="c5625-145">X</span><span class="sxs-lookup"><span data-stu-id="c5625-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="c5625-146">X</span><span class="sxs-lookup"><span data-stu-id="c5625-146">X</span></span></p></td>
<td><p><span data-ttu-id="c5625-147">X</span><span class="sxs-lookup"><span data-stu-id="c5625-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5625-148">8</span><span class="sxs-lookup"><span data-stu-id="c5625-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="c5625-149">X</span><span class="sxs-lookup"><span data-stu-id="c5625-149">X</span></span></p></td>
<td><p><span data-ttu-id="c5625-150">X</span><span class="sxs-lookup"><span data-stu-id="c5625-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c5625-151">Þegar áskriftarþóknun er búin til er ítarlegasta söluverðið, eins og fram kemur í töflunni hér fyrir ofan, valið sem áskriftarsöluverð.</span><span class="sxs-lookup"><span data-stu-id="c5625-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="c5625-152">Uppfæra og vísitölubinda söluverð áskrifta</span><span class="sxs-lookup"><span data-stu-id="c5625-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="c5625-153">Hægt er að uppfæra söluverð áskriftarinnar með því að uppfæra grundvallarverðið eða vísinn.</span><span class="sxs-lookup"><span data-stu-id="c5625-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="c5625-154">Þú getur uppfært með prósentu eða nýju gildi.</span><span class="sxs-lookup"><span data-stu-id="c5625-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="c5625-155">Söluverð áskriftarþóknunar</span><span class="sxs-lookup"><span data-stu-id="c5625-155">Subscription fee sales prices</span></span>

<span data-ttu-id="c5625-156">Þegar áskriftarþóknun er stofnuð er söluverðið byggt á söluverðsuppsetningu áskriftarinnar.</span><span class="sxs-lookup"><span data-stu-id="c5625-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="c5625-157">Þú getur annaðhvort notað grunnverð frá uppsetningu áskriftarverðs eða stofnað merkt söluverð.</span><span class="sxs-lookup"><span data-stu-id="c5625-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="c5625-158">Dæmi</span><span class="sxs-lookup"><span data-stu-id="c5625-158">Example</span></span>

<span data-ttu-id="c5625-159">Setja á upp áskriftarsöluverðið 500 evrur fyrir nýtt verk, 9030.</span><span class="sxs-lookup"><span data-stu-id="c5625-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="c5625-160">Í skjámyndinni **Söluverð (áskrift)** stofnarðu áskriftarsöluverðslínu eins og fram kemur í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="c5625-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5625-161">Gildir frá</span><span class="sxs-lookup"><span data-stu-id="c5625-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="c5625-162">Tegund</span><span class="sxs-lookup"><span data-stu-id="c5625-162">Category</span></span></p></th>
<th><p><span data-ttu-id="c5625-163">Verkefni</span><span class="sxs-lookup"><span data-stu-id="c5625-163">Project</span></span></p></th>
<th><p><span data-ttu-id="c5625-164">Áskrift</span><span class="sxs-lookup"><span data-stu-id="c5625-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="c5625-165">Tímabilskóði</span><span class="sxs-lookup"><span data-stu-id="c5625-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="c5625-166">Sölugjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="c5625-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="c5625-167">Söluverð</span><span class="sxs-lookup"><span data-stu-id="c5625-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5625-168">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="c5625-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c5625-169">9030</span><span class="sxs-lookup"><span data-stu-id="c5625-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c5625-170">Mánuður</span><span class="sxs-lookup"><span data-stu-id="c5625-170">Month</span></span></p></td>
<td><p><span data-ttu-id="c5625-171">EUR</span><span class="sxs-lookup"><span data-stu-id="c5625-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="c5625-172">500</span><span class="sxs-lookup"><span data-stu-id="c5625-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c5625-173">Athugaðu að reitirnir **Flokkur** og **Áskrift** eru tómir.</span><span class="sxs-lookup"><span data-stu-id="c5625-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="c5625-174">Þú býrð síðan til eftirfarandi áskriftir.</span><span class="sxs-lookup"><span data-stu-id="c5625-174">You then create the following subscriptions.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5625-175">Þjónustuáskrift</span><span class="sxs-lookup"><span data-stu-id="c5625-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="c5625-176">Verkefni</span><span class="sxs-lookup"><span data-stu-id="c5625-176">Project</span></span></p></th>
<th><p><span data-ttu-id="c5625-177">Áskriftarflokkur</span><span class="sxs-lookup"><span data-stu-id="c5625-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="c5625-178">Tegund</span><span class="sxs-lookup"><span data-stu-id="c5625-178">Category</span></span></p></th>
<th><p><span data-ttu-id="c5625-179">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="c5625-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="c5625-180">Tímabilskóði</span><span class="sxs-lookup"><span data-stu-id="c5625-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5625-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="c5625-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="c5625-182">9030</span><span class="sxs-lookup"><span data-stu-id="c5625-182">9030</span></span></p></td>
<td><p><span data-ttu-id="c5625-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="c5625-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="c5625-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="c5625-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="c5625-185">EUR</span><span class="sxs-lookup"><span data-stu-id="c5625-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="c5625-186">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="c5625-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5625-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="c5625-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="c5625-188">9030</span><span class="sxs-lookup"><span data-stu-id="c5625-188">9030</span></span></p></td>
<td><p><span data-ttu-id="c5625-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="c5625-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="c5625-190">Undirteg2</span><span class="sxs-lookup"><span data-stu-id="c5625-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="c5625-191">EUR</span><span class="sxs-lookup"><span data-stu-id="c5625-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="c5625-192">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="c5625-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c5625-193">Nú eru áskriftarþóknanir stofnaðar fyrir báðar áskriftir í áskriftahópnum Sub1:</span><span class="sxs-lookup"><span data-stu-id="c5625-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="c5625-194">Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Þjónusta áskrift** \> **Áskriftarflokkar** .</span><span class="sxs-lookup"><span data-stu-id="c5625-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="c5625-195">Í skjámyndinni **Áskriftarflokkar** skaltu smella á **Virkni** \> **Stofna áskriftarþóknun**.</span><span class="sxs-lookup"><span data-stu-id="c5625-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="c5625-196">Í skjámyndinni **Stofna áskriftarþóknun** skaltu slá inn viðeigandi upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="c5625-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="c5625-197">Frekari upplýsingar eru í [Stofna færslur áskriftarþóknunar](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="c5625-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="c5625-198">Áskriftarþóknanir sem eru með söluverð 500 evrur eru búnar til fyrir bæði áskriftirnar, eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="c5625-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5625-199">Verkdagsetning</span><span class="sxs-lookup"><span data-stu-id="c5625-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="c5625-200">Þjónustuáskrift</span><span class="sxs-lookup"><span data-stu-id="c5625-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="c5625-201">Verkefni</span><span class="sxs-lookup"><span data-stu-id="c5625-201">Project</span></span></p></th>
<th><p><span data-ttu-id="c5625-202">Tegund</span><span class="sxs-lookup"><span data-stu-id="c5625-202">Category</span></span></p></th>
<th><p><span data-ttu-id="c5625-203">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="c5625-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="c5625-204">Lokadagur</span><span class="sxs-lookup"><span data-stu-id="c5625-204">End date</span></span></p></th>
<th><p><span data-ttu-id="c5625-205">Sölugjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="c5625-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="c5625-206">Söluverð</span><span class="sxs-lookup"><span data-stu-id="c5625-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5625-207">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="c5625-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="c5625-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="c5625-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="c5625-209">9030</span><span class="sxs-lookup"><span data-stu-id="c5625-209">9030</span></span></p></td>
<td><p><span data-ttu-id="c5625-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="c5625-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="c5625-211">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="c5625-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="c5625-212">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="c5625-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="c5625-213">EUR</span><span class="sxs-lookup"><span data-stu-id="c5625-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="c5625-214">500</span><span class="sxs-lookup"><span data-stu-id="c5625-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5625-215">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="c5625-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="c5625-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="c5625-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="c5625-217">9030</span><span class="sxs-lookup"><span data-stu-id="c5625-217">9030</span></span></p></td>
<td><p><span data-ttu-id="c5625-218">Undirteg2</span><span class="sxs-lookup"><span data-stu-id="c5625-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="c5625-219">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="c5625-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="c5625-220">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="c5625-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="c5625-221">EUR</span><span class="sxs-lookup"><span data-stu-id="c5625-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="c5625-222">500</span><span class="sxs-lookup"><span data-stu-id="c5625-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c5625-223">Seinna gæti átt að tilgreina söluverð fyrir flokkinn SubCat1 fyrir verk 9030.</span><span class="sxs-lookup"><span data-stu-id="c5625-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="c5625-224">Þess vegna stofnar þú nýja söluverðslínu sem hefur söluverð upp á EUR 550 fyrir samsetningu verkefnis 9030 og gjaldflokkinn SubCat1.</span><span class="sxs-lookup"><span data-stu-id="c5625-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="c5625-225">Nú eru tvær áskriftarsöluverðslínur fyrir verkefni 9030, eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="c5625-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5625-226">Gildir frá</span><span class="sxs-lookup"><span data-stu-id="c5625-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="c5625-227">Tegund</span><span class="sxs-lookup"><span data-stu-id="c5625-227">Category</span></span></p></th>
<th><p><span data-ttu-id="c5625-228">Verkefni</span><span class="sxs-lookup"><span data-stu-id="c5625-228">Project</span></span></p></th>
<th><p><span data-ttu-id="c5625-229">Áskrift</span><span class="sxs-lookup"><span data-stu-id="c5625-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="c5625-230">Tímabilskóði</span><span class="sxs-lookup"><span data-stu-id="c5625-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="c5625-231">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="c5625-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="c5625-232">Söluverð</span><span class="sxs-lookup"><span data-stu-id="c5625-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5625-233">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="c5625-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c5625-234">9030</span><span class="sxs-lookup"><span data-stu-id="c5625-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c5625-235">Mánuður</span><span class="sxs-lookup"><span data-stu-id="c5625-235">Month</span></span></p></td>
<td><p><span data-ttu-id="c5625-236">EUR</span><span class="sxs-lookup"><span data-stu-id="c5625-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="c5625-237">500</span><span class="sxs-lookup"><span data-stu-id="c5625-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5625-238">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="c5625-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="c5625-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="c5625-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="c5625-240">9030</span><span class="sxs-lookup"><span data-stu-id="c5625-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c5625-241">Mánuður</span><span class="sxs-lookup"><span data-stu-id="c5625-241">Month</span></span></p></td>
<td><p><span data-ttu-id="c5625-242">EUR</span><span class="sxs-lookup"><span data-stu-id="c5625-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="c5625-243">550</span><span class="sxs-lookup"><span data-stu-id="c5625-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c5625-244">Ferlið sem lýst er fyrir ofan er endurtekið til að stofna áskriftarþóknanir fyrir báðar áskriftir í áskriftaflokknum Sub1.</span><span class="sxs-lookup"><span data-stu-id="c5625-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="c5625-245">Eftirfarandi tafla sýnir færslur sem eru búnar til fyrir hverja áskrift sem fylgir áskriftarflokknum.</span><span class="sxs-lookup"><span data-stu-id="c5625-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c5625-246">Verkdagsetning</span><span class="sxs-lookup"><span data-stu-id="c5625-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="c5625-247">Áskrift</span><span class="sxs-lookup"><span data-stu-id="c5625-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="c5625-248">Verkefni</span><span class="sxs-lookup"><span data-stu-id="c5625-248">Project</span></span></p></th>
<th><p><span data-ttu-id="c5625-249">Tegund</span><span class="sxs-lookup"><span data-stu-id="c5625-249">Category</span></span></p></th>
<th><p><span data-ttu-id="c5625-250">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="c5625-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="c5625-251">Lokadagur</span><span class="sxs-lookup"><span data-stu-id="c5625-251">End date</span></span></p></th>
<th><p><span data-ttu-id="c5625-252">Sölugjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="c5625-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="c5625-253">Söluverð</span><span class="sxs-lookup"><span data-stu-id="c5625-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c5625-254">28-07-2007</span><span class="sxs-lookup"><span data-stu-id="c5625-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="c5625-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="c5625-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="c5625-256">9030</span><span class="sxs-lookup"><span data-stu-id="c5625-256">9030</span></span></p></td>
<td><p><span data-ttu-id="c5625-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="c5625-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="c5625-258">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="c5625-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="c5625-259">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="c5625-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="c5625-260">EUR</span><span class="sxs-lookup"><span data-stu-id="c5625-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="c5625-261">550</span><span class="sxs-lookup"><span data-stu-id="c5625-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c5625-262">28-07-2008</span><span class="sxs-lookup"><span data-stu-id="c5625-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="c5625-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="c5625-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="c5625-264">9030</span><span class="sxs-lookup"><span data-stu-id="c5625-264">9030</span></span></p></td>
<td><p><span data-ttu-id="c5625-265">Undirteg2</span><span class="sxs-lookup"><span data-stu-id="c5625-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="c5625-266">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="c5625-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="c5625-267">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="c5625-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="c5625-268">EUR</span><span class="sxs-lookup"><span data-stu-id="c5625-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="c5625-269">500</span><span class="sxs-lookup"><span data-stu-id="c5625-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c5625-270">Í fyrstu færslunni fyrir áskrift 00020\_135 er söluverðið 550 EUR komið frá áskriftarsöluverðinu sem er sett upp fyrir samsetningu tiltekins verkefnis og flokks.</span><span class="sxs-lookup"><span data-stu-id="c5625-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="c5625-271">Í seinni færslunni fyrir áskrift 00021\_135 er söluverðið 500 EUR notað sem áskriftarsöluverð verkefnis vegna þess að ekkert verð er sett upp fyrir samsetningu verkefnis 9030 og flokki SubCat2.</span><span class="sxs-lookup"><span data-stu-id="c5625-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="c5625-272">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="c5625-272">See also</span></span>

[<span data-ttu-id="c5625-273">Uppfæra og vísitölubinda söluverð áskrifta</span><span class="sxs-lookup"><span data-stu-id="c5625-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  


