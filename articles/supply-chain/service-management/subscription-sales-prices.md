---
title: Áskriftarsöluverð
description: Þegar þú stofnar áskrift er söluverðið byggt á uppsetningu söluverðs sem var stofnað í skjámyndinni „Söluverð (áskrift)“.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASalespriceSubscription
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2ed8329e9da08fbe24d9b3982eee562974f0fb3b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5242302"
---
# <a name="subscription-sales-prices"></a><span data-ttu-id="d1c14-103">Áskriftarsöluverð</span><span class="sxs-lookup"><span data-stu-id="d1c14-103">Subscription sales prices</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="d1c14-104">Þegar þú stofnar áskrift er söluverðið byggt á uppsetningu söluverðs sem var stofnað í skjámyndinni **Söluverð (áskrift)**.</span><span class="sxs-lookup"><span data-stu-id="d1c14-104">When you create a subscription, the sales price is derived from the sales price setup that was created in the **Sales price (subscription)** form.</span></span>

<span data-ttu-id="d1c14-105">Í skjámyndinni **Söluverði (áskrift)** getur þú stofnað söluverð fyrir tiltekna áskrift eða þú getur stofnað söluverð sem gilda í víðara samhengi.</span><span class="sxs-lookup"><span data-stu-id="d1c14-105">In the **Sales price (subscription)** form, you can create sales prices for a specific subscription or you can create sales prices that apply more broadly.</span></span> <span data-ttu-id="d1c14-106">Til þess að söluverð verði notað á áskrift skal tímabilskóðinn og gjaldmiðill áskriftarinnar vera eins og tímabilskóði og gjaldmiðill söluverðsins.</span><span class="sxs-lookup"><span data-stu-id="d1c14-106">For a sales price to be applied to a subscription, the period code and the currency of the subscription must be identical to the period code and the currency of the sales price.</span></span>

<span data-ttu-id="d1c14-107">Ef tímabilskóði og gjaldmiðill eru eins fyrir áskrift og söluverð eru áskriftarsöluverð valin á grundvelli forgangsröðunar sem er að finna í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="d1c14-107">If the period code and currency are identical for the subscription and the sales price, subscription sales prices are selected on the basis of the priorities listed in the following table.</span></span> <span data-ttu-id="d1c14-108">Autt hólf í töflunni gefur til kynna tóman reit og X gefur til kynna gildi sem er jafnt gildinu í áskriftinni þar sem færslan er mynduð.</span><span class="sxs-lookup"><span data-stu-id="d1c14-108">A blank cell in the table indicates an empty field and an X indicates a value that is equal to the value in the subscription from which the transaction is generated.</span></span>

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
<th><p><span data-ttu-id="d1c14-109">Forgangur </span><span class="sxs-lookup"><span data-stu-id="d1c14-109">Priority</span></span></p></th>
<th><p><span data-ttu-id="d1c14-110"><strong>Tegund</strong></span><span class="sxs-lookup"><span data-stu-id="d1c14-110"><strong>Category</strong></span></span></p></th>
<th><p><span data-ttu-id="d1c14-111"><strong>Kenni verks</strong></span><span class="sxs-lookup"><span data-stu-id="d1c14-111"><strong>Project ID</strong></span></span></p></th>
<th><p><span data-ttu-id="d1c14-112"><strong>Áskrift</strong></span><span class="sxs-lookup"><span data-stu-id="d1c14-112"><strong>Subscription</strong></span></span></p></th>
<th><p><span data-ttu-id="d1c14-113"><strong>Sölugjaldmiðill</strong></span><span class="sxs-lookup"><span data-stu-id="d1c14-113"><strong>Sales currency</strong></span></span></p></th>
<th><p><span data-ttu-id="d1c14-114"><strong>Tímabilskóði</strong></span><span class="sxs-lookup"><span data-stu-id="d1c14-114"><strong>Period code</strong></span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1c14-115">1</span><span class="sxs-lookup"><span data-stu-id="d1c14-115">1</span></span></p></td>
<td><p><span data-ttu-id="d1c14-116">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-116">X</span></span></p></td>
<td><p><span data-ttu-id="d1c14-117">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-117">X</span></span></p></td>
<td><p><span data-ttu-id="d1c14-118">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-118">X</span></span></p></td>
<td><p><span data-ttu-id="d1c14-119">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-119">X</span></span></p></td>
<td><p><span data-ttu-id="d1c14-120">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-120">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1c14-121">2</span><span class="sxs-lookup"><span data-stu-id="d1c14-121">2</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d1c14-122">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-122">X</span></span></p></td>
<td><p><span data-ttu-id="d1c14-123">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-123">X</span></span></p></td>
<td><p><span data-ttu-id="d1c14-124">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-124">X</span></span></p></td>
<td><p><span data-ttu-id="d1c14-125">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-125">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1c14-126">3</span><span class="sxs-lookup"><span data-stu-id="d1c14-126">3</span></span></p></td>
<td><p><span data-ttu-id="d1c14-127">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-127">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d1c14-128">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-128">X</span></span></p></td>
<td><p><span data-ttu-id="d1c14-129">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-129">X</span></span></p></td>
<td><p><span data-ttu-id="d1c14-130">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-130">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1c14-131">4</span><span class="sxs-lookup"><span data-stu-id="d1c14-131">4</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d1c14-132">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-132">X</span></span></p></td>
<td><p><span data-ttu-id="d1c14-133">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-133">X</span></span></p></td>
<td><p><span data-ttu-id="d1c14-134">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-134">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1c14-135">5</span><span class="sxs-lookup"><span data-stu-id="d1c14-135">5</span></span></p></td>
<td><p><span data-ttu-id="d1c14-136">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-136">X</span></span></p></td>
<td><p><span data-ttu-id="d1c14-137">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-137">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d1c14-138">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-138">X</span></span></p></td>
<td><p><span data-ttu-id="d1c14-139">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-139">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1c14-140">6</span><span class="sxs-lookup"><span data-stu-id="d1c14-140">6</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d1c14-141">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-141">X</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d1c14-142">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-142">X</span></span></p></td>
<td><p><span data-ttu-id="d1c14-143">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-143">X</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1c14-144">7</span><span class="sxs-lookup"><span data-stu-id="d1c14-144">7</span></span></p></td>
<td><p><span data-ttu-id="d1c14-145">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-145">X</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d1c14-146">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-146">X</span></span></p></td>
<td><p><span data-ttu-id="d1c14-147">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-147">X</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1c14-148">8</span><span class="sxs-lookup"><span data-stu-id="d1c14-148">8</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="d1c14-149">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-149">X</span></span></p></td>
<td><p><span data-ttu-id="d1c14-150">X</span><span class="sxs-lookup"><span data-stu-id="d1c14-150">X</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d1c14-151">Þegar áskriftarþóknun er búin til er ítarlegasta söluverðið, eins og fram kemur í töflunni hér fyrir ofan, valið sem áskriftarsöluverð.</span><span class="sxs-lookup"><span data-stu-id="d1c14-151">When a subscription fee is created, the sales price with the greatest level of detail, as noted in the table above, is selected as the subscription sales price.</span></span>

## <a name="update-and-index-subscription-sales-prices"></a><span data-ttu-id="d1c14-152">Uppfæra og vísitölubinda söluverð áskrifta</span><span class="sxs-lookup"><span data-stu-id="d1c14-152">Update and index subscription sales prices</span></span>

<span data-ttu-id="d1c14-153">Hægt er að uppfæra söluverð áskriftarinnar með því að uppfæra grundvallarverðið eða vísinn.</span><span class="sxs-lookup"><span data-stu-id="d1c14-153">You can update the subscription sales price by updating the base price or the index.</span></span> <span data-ttu-id="d1c14-154">Þú getur uppfært með prósentu eða nýju gildi.</span><span class="sxs-lookup"><span data-stu-id="d1c14-154">You can update by a percentage or to a new value.</span></span>

## <a name="subscription-fee-sales-prices"></a><span data-ttu-id="d1c14-155">Söluverð áskriftarþóknunar</span><span class="sxs-lookup"><span data-stu-id="d1c14-155">Subscription fee sales prices</span></span>

<span data-ttu-id="d1c14-156">Þegar áskriftarþóknun er stofnuð er söluverðið byggt á söluverðsuppsetningu áskriftarinnar.</span><span class="sxs-lookup"><span data-stu-id="d1c14-156">When you create a subscription fee, the sales price is based on the sales price setup of the subscription.</span></span> <span data-ttu-id="d1c14-157">Þú getur annaðhvort notað grunnverð frá uppsetningu áskriftarverðs eða stofnað merkt söluverð.</span><span class="sxs-lookup"><span data-stu-id="d1c14-157">You can either use the base price from the subscription price setup or create indexed sales prices.</span></span>

## <a name="example"></a><span data-ttu-id="d1c14-158">Dæmi</span><span class="sxs-lookup"><span data-stu-id="d1c14-158">Example</span></span>

<span data-ttu-id="d1c14-159">Setja á upp áskriftarsöluverðið 500 evrur fyrir nýtt verk, 9030.</span><span class="sxs-lookup"><span data-stu-id="d1c14-159">You want to set up subscription sales prices of EUR 500 for a new project 9030.</span></span> <span data-ttu-id="d1c14-160">Í skjámyndinni **Söluverð (áskrift)** stofnarðu áskriftarsöluverðslínu eins og fram kemur í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="d1c14-160">In the **Sales price (subscription)** form, you create a subscription sales price line as indicated in the following table.</span></span>

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
<th><p><span data-ttu-id="d1c14-161">Gildir frá</span><span class="sxs-lookup"><span data-stu-id="d1c14-161">Valid from</span></span></p></th>
<th><p><span data-ttu-id="d1c14-162">Tegund</span><span class="sxs-lookup"><span data-stu-id="d1c14-162">Category</span></span></p></th>
<th><p><span data-ttu-id="d1c14-163">Verkefni</span><span class="sxs-lookup"><span data-stu-id="d1c14-163">Project</span></span></p></th>
<th><p><span data-ttu-id="d1c14-164">Áskrift</span><span class="sxs-lookup"><span data-stu-id="d1c14-164">Subscription</span></span></p></th>
<th><p><span data-ttu-id="d1c14-165">Tímabilskóði</span><span class="sxs-lookup"><span data-stu-id="d1c14-165">Period code</span></span></p></th>
<th><p><span data-ttu-id="d1c14-166">Sölugjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d1c14-166">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="d1c14-167">Söluverð</span><span class="sxs-lookup"><span data-stu-id="d1c14-167">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1c14-168">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="d1c14-168">28-08-2006</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d1c14-169">9030</span><span class="sxs-lookup"><span data-stu-id="d1c14-169">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d1c14-170">Mánuður</span><span class="sxs-lookup"><span data-stu-id="d1c14-170">Month</span></span></p></td>
<td><p><span data-ttu-id="d1c14-171">EUR</span><span class="sxs-lookup"><span data-stu-id="d1c14-171">EUR</span></span></p></td>
<td><p><span data-ttu-id="d1c14-172">500</span><span class="sxs-lookup"><span data-stu-id="d1c14-172">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d1c14-173">Athugaðu að reitirnir **Flokkur** og **Áskrift** eru tómir.</span><span class="sxs-lookup"><span data-stu-id="d1c14-173">Note that the **Category** and **Subscription** fields are empty.</span></span>

<span data-ttu-id="d1c14-174">Þú býrð síðan til eftirfarandi áskriftir.</span><span class="sxs-lookup"><span data-stu-id="d1c14-174">You then create the following subscriptions.</span></span>

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
<th><p><span data-ttu-id="d1c14-175">Þjónustuáskrift</span><span class="sxs-lookup"><span data-stu-id="d1c14-175">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="d1c14-176">Verkefni</span><span class="sxs-lookup"><span data-stu-id="d1c14-176">Project</span></span></p></th>
<th><p><span data-ttu-id="d1c14-177">Áskriftarflokkur</span><span class="sxs-lookup"><span data-stu-id="d1c14-177">Subscription group</span></span></p></th>
<th><p><span data-ttu-id="d1c14-178">Tegund</span><span class="sxs-lookup"><span data-stu-id="d1c14-178">Category</span></span></p></th>
<th><p><span data-ttu-id="d1c14-179">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d1c14-179">Currency</span></span></p></th>
<th><p><span data-ttu-id="d1c14-180">Tímabilskóði</span><span class="sxs-lookup"><span data-stu-id="d1c14-180">Period code</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1c14-181">00020_135</span><span class="sxs-lookup"><span data-stu-id="d1c14-181">00020_135</span></span></p></td>
<td><p><span data-ttu-id="d1c14-182">9030</span><span class="sxs-lookup"><span data-stu-id="d1c14-182">9030</span></span></p></td>
<td><p><span data-ttu-id="d1c14-183">Sub1</span><span class="sxs-lookup"><span data-stu-id="d1c14-183">Sub1</span></span></p></td>
<td><p><span data-ttu-id="d1c14-184">SubCat1</span><span class="sxs-lookup"><span data-stu-id="d1c14-184">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="d1c14-185">EUR</span><span class="sxs-lookup"><span data-stu-id="d1c14-185">EUR</span></span></p></td>
<td><p><span data-ttu-id="d1c14-186">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="d1c14-186">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1c14-187">00021_135</span><span class="sxs-lookup"><span data-stu-id="d1c14-187">00021_135</span></span></p></td>
<td><p><span data-ttu-id="d1c14-188">9030</span><span class="sxs-lookup"><span data-stu-id="d1c14-188">9030</span></span></p></td>
<td><p><span data-ttu-id="d1c14-189">Sub1</span><span class="sxs-lookup"><span data-stu-id="d1c14-189">Sub1</span></span></p></td>
<td><p><span data-ttu-id="d1c14-190">Undirteg2</span><span class="sxs-lookup"><span data-stu-id="d1c14-190">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="d1c14-191">EUR</span><span class="sxs-lookup"><span data-stu-id="d1c14-191">EUR</span></span></p></td>
<td><p><span data-ttu-id="d1c14-192">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="d1c14-192">Monthly</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d1c14-193">Nú eru áskriftarþóknanir stofnaðar fyrir báðar áskriftir í áskriftahópnum Sub1:</span><span class="sxs-lookup"><span data-stu-id="d1c14-193">Now you create subscription fees for both subscriptions in the subscription group Sub1:</span></span>

1.  <span data-ttu-id="d1c14-194">Smelltu á **Þjónustustjórnun** \> **Uppsetning** \> **Þjónusta áskrift** \> **Áskriftarflokkar** .</span><span class="sxs-lookup"><span data-stu-id="d1c14-194">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

2.  <span data-ttu-id="d1c14-195">Í skjámyndinni **Áskriftarflokkar** skaltu smella á **Virkni** \> **Stofna áskriftarþóknun**.</span><span class="sxs-lookup"><span data-stu-id="d1c14-195">In the **Subscription groups** form, click **Function** \> **Create subscription fee**.</span></span>

3.  <span data-ttu-id="d1c14-196">Í skjámyndinni **Stofna áskriftarþóknun** skaltu slá inn viðeigandi upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="d1c14-196">In the **Create subscription fee** form, enter the appropriate information.</span></span> <span data-ttu-id="d1c14-197">Frekari upplýsingar eru í [Stofna færslur áskriftarþóknunar](create-subscription-fee-transactions.md).</span><span class="sxs-lookup"><span data-stu-id="d1c14-197">For more information, see [Create subscription fee transactions](create-subscription-fee-transactions.md).</span></span>

<span data-ttu-id="d1c14-198">Áskriftarþóknanir sem eru með söluverð 500 evrur eru búnar til fyrir bæði áskriftirnar, eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="d1c14-198">Subscription fees that have a sales price of EUR 500 are created for both subscriptions, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="d1c14-199">Verkdagsetning</span><span class="sxs-lookup"><span data-stu-id="d1c14-199">Project date</span></span></p></th>
<th><p><span data-ttu-id="d1c14-200">Þjónustuáskrift</span><span class="sxs-lookup"><span data-stu-id="d1c14-200">Service subscription</span></span></p></th>
<th><p><span data-ttu-id="d1c14-201">Verkefni</span><span class="sxs-lookup"><span data-stu-id="d1c14-201">Project</span></span></p></th>
<th><p><span data-ttu-id="d1c14-202">Tegund</span><span class="sxs-lookup"><span data-stu-id="d1c14-202">Category</span></span></p></th>
<th><p><span data-ttu-id="d1c14-203">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="d1c14-203">Start date</span></span></p></th>
<th><p><span data-ttu-id="d1c14-204">Lokadagur</span><span class="sxs-lookup"><span data-stu-id="d1c14-204">End date</span></span></p></th>
<th><p><span data-ttu-id="d1c14-205">Sölugjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d1c14-205">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="d1c14-206">Söluverð</span><span class="sxs-lookup"><span data-stu-id="d1c14-206">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1c14-207">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="d1c14-207">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="d1c14-208">00020_135</span><span class="sxs-lookup"><span data-stu-id="d1c14-208">00020_135</span></span></p></td>
<td><p><span data-ttu-id="d1c14-209">9030</span><span class="sxs-lookup"><span data-stu-id="d1c14-209">9030</span></span></p></td>
<td><p><span data-ttu-id="d1c14-210">SubCat1</span><span class="sxs-lookup"><span data-stu-id="d1c14-210">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="d1c14-211">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="d1c14-211">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="d1c14-212">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="d1c14-212">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="d1c14-213">EUR</span><span class="sxs-lookup"><span data-stu-id="d1c14-213">EUR</span></span></p></td>
<td><p><span data-ttu-id="d1c14-214">500</span><span class="sxs-lookup"><span data-stu-id="d1c14-214">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1c14-215">28-08-2006</span><span class="sxs-lookup"><span data-stu-id="d1c14-215">28-08-2006</span></span></p></td>
<td><p><span data-ttu-id="d1c14-216">00021_135</span><span class="sxs-lookup"><span data-stu-id="d1c14-216">00021_135</span></span></p></td>
<td><p><span data-ttu-id="d1c14-217">9030</span><span class="sxs-lookup"><span data-stu-id="d1c14-217">9030</span></span></p></td>
<td><p><span data-ttu-id="d1c14-218">Undirteg2</span><span class="sxs-lookup"><span data-stu-id="d1c14-218">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="d1c14-219">01-01-2007</span><span class="sxs-lookup"><span data-stu-id="d1c14-219">01-01-2007</span></span></p></td>
<td><p><span data-ttu-id="d1c14-220">31-03-2007</span><span class="sxs-lookup"><span data-stu-id="d1c14-220">31-03-2007</span></span></p></td>
<td><p><span data-ttu-id="d1c14-221">EUR</span><span class="sxs-lookup"><span data-stu-id="d1c14-221">EUR</span></span></p></td>
<td><p><span data-ttu-id="d1c14-222">500</span><span class="sxs-lookup"><span data-stu-id="d1c14-222">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d1c14-223">Seinna gæti átt að tilgreina söluverð fyrir flokkinn SubCat1 fyrir verk 9030.</span><span class="sxs-lookup"><span data-stu-id="d1c14-223">Later, you decide that you want to specify sales prices for the category SubCat1 for project 9030.</span></span> <span data-ttu-id="d1c14-224">Þess vegna stofnar þú nýja söluverðslínu sem hefur söluverð upp á EUR 550 fyrir samsetningu verkefnis 9030 og gjaldflokkinn SubCat1.</span><span class="sxs-lookup"><span data-stu-id="d1c14-224">Therefore, you create a new sales price line that has a sales price of EUR 550 for the combination of project 9030 and fee category SubCat1.</span></span> <span data-ttu-id="d1c14-225">Nú eru tvær áskriftarsöluverðslínur fyrir verkefni 9030, eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="d1c14-225">There are now two subscription sales price lines for project 9030, as shown in the following table.</span></span>

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
<th><p><span data-ttu-id="d1c14-226">Gildir frá</span><span class="sxs-lookup"><span data-stu-id="d1c14-226">Valid from</span></span></p></th>
<th><p><span data-ttu-id="d1c14-227">Tegund</span><span class="sxs-lookup"><span data-stu-id="d1c14-227">Category</span></span></p></th>
<th><p><span data-ttu-id="d1c14-228">Verkefni</span><span class="sxs-lookup"><span data-stu-id="d1c14-228">Project</span></span></p></th>
<th><p><span data-ttu-id="d1c14-229">Áskrift</span><span class="sxs-lookup"><span data-stu-id="d1c14-229">Subscription</span></span></p></th>
<th><p><span data-ttu-id="d1c14-230">Tímabilskóði</span><span class="sxs-lookup"><span data-stu-id="d1c14-230">Period code</span></span></p></th>
<th><p><span data-ttu-id="d1c14-231">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d1c14-231">Currency</span></span></p></th>
<th><p><span data-ttu-id="d1c14-232">Söluverð</span><span class="sxs-lookup"><span data-stu-id="d1c14-232">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1c14-233">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="d1c14-233">28-08-2007</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d1c14-234">9030</span><span class="sxs-lookup"><span data-stu-id="d1c14-234">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d1c14-235">Mánuður</span><span class="sxs-lookup"><span data-stu-id="d1c14-235">Month</span></span></p></td>
<td><p><span data-ttu-id="d1c14-236">EUR</span><span class="sxs-lookup"><span data-stu-id="d1c14-236">EUR</span></span></p></td>
<td><p><span data-ttu-id="d1c14-237">500</span><span class="sxs-lookup"><span data-stu-id="d1c14-237">500</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1c14-238">28-08-2007</span><span class="sxs-lookup"><span data-stu-id="d1c14-238">28-08-2007</span></span></p></td>
<td><p><span data-ttu-id="d1c14-239">SubCat1</span><span class="sxs-lookup"><span data-stu-id="d1c14-239">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="d1c14-240">9030</span><span class="sxs-lookup"><span data-stu-id="d1c14-240">9030</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d1c14-241">Mánuður</span><span class="sxs-lookup"><span data-stu-id="d1c14-241">Month</span></span></p></td>
<td><p><span data-ttu-id="d1c14-242">EUR</span><span class="sxs-lookup"><span data-stu-id="d1c14-242">EUR</span></span></p></td>
<td><p><span data-ttu-id="d1c14-243">550</span><span class="sxs-lookup"><span data-stu-id="d1c14-243">550</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d1c14-244">Ferlið sem lýst er fyrir ofan er endurtekið til að stofna áskriftarþóknanir fyrir báðar áskriftir í áskriftaflokknum Sub1.</span><span class="sxs-lookup"><span data-stu-id="d1c14-244">You repeat the procedure described above to create subscription fees for both subscriptions in the subscription group Sub1.</span></span> <span data-ttu-id="d1c14-245">Eftirfarandi tafla sýnir færslur sem eru búnar til fyrir hverja áskrift sem fylgir áskriftarflokknum.</span><span class="sxs-lookup"><span data-stu-id="d1c14-245">The following table shows the transactions that are created for each subscription that is attached to the subscription group.</span></span>

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
<th><p><span data-ttu-id="d1c14-246">Verkdagsetning</span><span class="sxs-lookup"><span data-stu-id="d1c14-246">Project date</span></span></p></th>
<th><p><span data-ttu-id="d1c14-247">Áskrift</span><span class="sxs-lookup"><span data-stu-id="d1c14-247">Subscription</span></span></p></th>
<th><p><span data-ttu-id="d1c14-248">Verkefni</span><span class="sxs-lookup"><span data-stu-id="d1c14-248">Project</span></span></p></th>
<th><p><span data-ttu-id="d1c14-249">Tegund</span><span class="sxs-lookup"><span data-stu-id="d1c14-249">Category</span></span></p></th>
<th><p><span data-ttu-id="d1c14-250">Fyrsti vinnudagur</span><span class="sxs-lookup"><span data-stu-id="d1c14-250">Start date</span></span></p></th>
<th><p><span data-ttu-id="d1c14-251">Lokadagur</span><span class="sxs-lookup"><span data-stu-id="d1c14-251">End date</span></span></p></th>
<th><p><span data-ttu-id="d1c14-252">Sölugjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d1c14-252">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="d1c14-253">Söluverð</span><span class="sxs-lookup"><span data-stu-id="d1c14-253">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1c14-254">28-07-2007</span><span class="sxs-lookup"><span data-stu-id="d1c14-254">28-07-2007</span></span></p></td>
<td><p><span data-ttu-id="d1c14-255">00020_135</span><span class="sxs-lookup"><span data-stu-id="d1c14-255">00020_135</span></span></p></td>
<td><p><span data-ttu-id="d1c14-256">9030</span><span class="sxs-lookup"><span data-stu-id="d1c14-256">9030</span></span></p></td>
<td><p><span data-ttu-id="d1c14-257">SubCat1</span><span class="sxs-lookup"><span data-stu-id="d1c14-257">SubCat1</span></span></p></td>
<td><p><span data-ttu-id="d1c14-258">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="d1c14-258">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="d1c14-259">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="d1c14-259">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="d1c14-260">EUR</span><span class="sxs-lookup"><span data-stu-id="d1c14-260">EUR</span></span></p></td>
<td><p><span data-ttu-id="d1c14-261">550</span><span class="sxs-lookup"><span data-stu-id="d1c14-261">550</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1c14-262">28-07-2008</span><span class="sxs-lookup"><span data-stu-id="d1c14-262">28-07-2008</span></span></p></td>
<td><p><span data-ttu-id="d1c14-263">00021_135</span><span class="sxs-lookup"><span data-stu-id="d1c14-263">00021_135</span></span></p></td>
<td><p><span data-ttu-id="d1c14-264">9030</span><span class="sxs-lookup"><span data-stu-id="d1c14-264">9030</span></span></p></td>
<td><p><span data-ttu-id="d1c14-265">Undirteg2</span><span class="sxs-lookup"><span data-stu-id="d1c14-265">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="d1c14-266">01-01-2008</span><span class="sxs-lookup"><span data-stu-id="d1c14-266">01-01-2008</span></span></p></td>
<td><p><span data-ttu-id="d1c14-267">31-03-2008</span><span class="sxs-lookup"><span data-stu-id="d1c14-267">31-03-2008</span></span></p></td>
<td><p><span data-ttu-id="d1c14-268">EUR</span><span class="sxs-lookup"><span data-stu-id="d1c14-268">EUR</span></span></p></td>
<td><p><span data-ttu-id="d1c14-269">500</span><span class="sxs-lookup"><span data-stu-id="d1c14-269">500</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d1c14-270">Í fyrstu færslunni fyrir áskrift 00020\_135 er söluverðið 550 EUR komið frá áskriftarsöluverðinu sem er sett upp fyrir samsetningu tiltekins verkefnis og flokks.</span><span class="sxs-lookup"><span data-stu-id="d1c14-270">In the first transaction for subscription 00020\_135, the sales price of EUR 550 derives from the subscription sales price that is set up for the combination of the specific project and category.</span></span> <span data-ttu-id="d1c14-271">Í seinni færslunni fyrir áskrift 00021\_135 er söluverðið 500 EUR notað sem áskriftarsöluverð verkefnis vegna þess að ekkert verð er sett upp fyrir samsetningu verkefnis 9030 og flokki SubCat2.</span><span class="sxs-lookup"><span data-stu-id="d1c14-271">In the second transaction for subscription 00021\_135, the sales price of EUR 500 is used as the project subscription sales price because there is no price set up for the combination of project 9030 and category SubCat2.</span></span>

## <a name="see-also"></a><span data-ttu-id="d1c14-272">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="d1c14-272">See also</span></span>

[<span data-ttu-id="d1c14-273">Uppfæra og vísitölubinda söluverð áskrifta</span><span class="sxs-lookup"><span data-stu-id="d1c14-273">Update and index subscription sales prices</span></span>](update-and-index-subscription-sales-prices.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]