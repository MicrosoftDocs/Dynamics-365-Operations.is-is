---
title: Vsk-greiðslur og sléttunarreglur
description: Þessi grein útskýrir hvernig uppsetning sléttunarreglu á Skattyfirvöld gengur fyrir sig og hvernig á að slétta virðisaukaskatt í ferlinu Jafna og bóka virðisaukaskatt.
author: ShylaThompson
manager: AnnBe
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adc48d1841903670577684b1c3d773d323c19ea1
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275675"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="41dfe-103">Vsk-greiðslur og sléttunarreglur</span><span class="sxs-lookup"><span data-stu-id="41dfe-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41dfe-104">Þessi grein útskýrir hvernig uppsetning sléttunarreglu á Skattyfirvöld gengur fyrir sig og hvernig á að slétta virðisaukaskatt í ferlinu Jafna og bóka virðisaukaskatt.</span><span class="sxs-lookup"><span data-stu-id="41dfe-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="41dfe-105">Reglulega þarf að tilkynna vsk og greiða hann til skattayfirvalda.</span><span class="sxs-lookup"><span data-stu-id="41dfe-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="41dfe-106">Þetta er gert með því að keyra í jafna og bóka vsk-ferlið á síðunni Virðisaukaskattur.</span><span class="sxs-lookup"><span data-stu-id="41dfe-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="41dfe-107">Virðisaukaskattur fyrir tímabilið verða jafnaðar á móti lyklum virðisaukaskatts og staða virðisaukaskatts verður bókuð í lykilinn fyrir jöfnun vsk.</span><span class="sxs-lookup"><span data-stu-id="41dfe-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="41dfe-108">Stöðu virðisaukaskatts sem er bókuð í VSK-lykilinn er hægt slétta eins og krafist er á af skattayfirvöldum með því að setja upp sléttunarreglu á síðunni Virðisaukaskattur.</span><span class="sxs-lookup"><span data-stu-id="41dfe-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="41dfe-109">Sléttunarmismunur er bókaður á VSK-sléttunarlykil sem er valinn í lyklum fyrir sjálfvirkar færslur í reitnum Fjárhagur.</span><span class="sxs-lookup"><span data-stu-id="41dfe-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="41dfe-110">Dæmið hér að neðan sýnir hvernig sléttunarreglan á virðisaukaskattsyfirvöld virkar.</span><span class="sxs-lookup"><span data-stu-id="41dfe-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="41dfe-111">Dæmi</span><span class="sxs-lookup"><span data-stu-id="41dfe-111">Examples</span></span>

<span data-ttu-id="41dfe-112">Heildarupphæð VSK fyrir tímabil sýnir kreditstöðu-98,765.43.</span><span class="sxs-lookup"><span data-stu-id="41dfe-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="41dfe-113">Lögaðili innheimti hærri virðisaukaskattsupphæð en hann greiddi.</span><span class="sxs-lookup"><span data-stu-id="41dfe-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="41dfe-114">Þess vegna skuldar lögaðili peninga til skattyfirvalda.</span><span class="sxs-lookup"><span data-stu-id="41dfe-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="41dfe-115">Fyrirtækið vill nota sléttunaraðferð sem sléttar stöðuna í næstu 1,00 EUR.</span><span class="sxs-lookup"><span data-stu-id="41dfe-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="41dfe-116">Starfsmaðurinn sem ber ábyrgð á VSK-bókhaldi framkvæmir eftirfarandi skref.</span><span class="sxs-lookup"><span data-stu-id="41dfe-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1. <span data-ttu-id="41dfe-117">Fara á **Skattur** > **Óbeinir skattar** > **Virðisaukaskattur** > **Virðisaukaskattsyfirvöld**.</span><span class="sxs-lookup"><span data-stu-id="41dfe-117">Click **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax authorities**.</span></span>
2. <span data-ttu-id="41dfe-118">Í flýtiflipanum **Almennt**, í reitnum **Sléttunarregla** skal velja **Eðlilegt**.</span><span class="sxs-lookup"><span data-stu-id="41dfe-118">On the **General** FastTab, in the **Rounding form** field, select **Normal**.</span></span>
3. <span data-ttu-id="41dfe-119">Í reitinn **Sléttun** skal slá inn 1,00.</span><span class="sxs-lookup"><span data-stu-id="41dfe-119">In the **Round-off** field, enter 1.00.</span></span>
4. <span data-ttu-id="41dfe-120">Þegar tími er kominn til að greiða skattyfirvöldum VSK-skattinn skal opna **Skattur** > **Skattframtöl** > **Virðisaukaskattur** > **Jafna og bóka virðisaukaskatt**.</span><span class="sxs-lookup"><span data-stu-id="41dfe-120">When it is time to pay the sales taxes to the tax authority, go to **Tax** > **Declarations** > **Sales tax** > **Settle and post sale tax**.</span></span> <span data-ttu-id="41dfe-121">Í vsk-jöfnunarlykli má sjá að upphæð skattskuldar upp á **98.765,43** er sléttuð í **98.765**.</span><span class="sxs-lookup"><span data-stu-id="41dfe-121">On the sales tax settlement account, you can see that the tax liability amount of **98,765.43** is rounded to **98,765**.</span></span>

<span data-ttu-id="41dfe-122">Eftirfarandi tafla sýnir hvernig upphæðin 98.765,43 er sléttuð með því að nota hverja sléttunaraðferð sem tiltæk er í svæðið **Sléttunarregla** á síðunni **Skattayfirvöld**.</span><span class="sxs-lookup"><span data-stu-id="41dfe-122">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the **Rounding form** field in the **Sales tax authorities** page.</span></span>

> [!NOTE]                                                                                  
> <span data-ttu-id="41dfe-123">Ef sléttunargildið er stillt á 0,00 verður:</span><span class="sxs-lookup"><span data-stu-id="41dfe-123">If the round-off value is set as 0.00, then:</span></span>
>
> - <span data-ttu-id="41dfe-124">Fyrir eðlilega sléttun verður sléttunin sú sama og fyrir **Sléttun = 0,01**.</span><span class="sxs-lookup"><span data-stu-id="41dfe-124">For normal rounding, the rounding behavior is the same as for **Round-off = 0.01**.</span></span>
> - <span data-ttu-id="41dfe-125">Fyrir **Valkostir sléttunarreglu**, **Niður á við**, **Upp á við** og **Í eigin hag** er hegðunin sú sama og fyrir **Sléttun = 1,00**.</span><span class="sxs-lookup"><span data-stu-id="41dfe-125">For the **Rounding form options**, **Downward**, **Rounding-up**, and **Own advantage**, the behavior is the same as for **Round-off = 1.00**.</span></span>

| <span data-ttu-id="41dfe-126">Skjámyndavalkostur fyrir sléttun</span><span class="sxs-lookup"><span data-stu-id="41dfe-126">Rounding form option</span></span>                | <span data-ttu-id="41dfe-127">Námunda markaðsvirði = 0,01</span><span class="sxs-lookup"><span data-stu-id="41dfe-127">Round-off value = 0.01</span></span> | <span data-ttu-id="41dfe-128">Námunda markaðsvirði = 0,10</span><span class="sxs-lookup"><span data-stu-id="41dfe-128">Round-off value = 0.10</span></span> | <span data-ttu-id="41dfe-129">Námunda markaðsvirði = 1,00</span><span class="sxs-lookup"><span data-stu-id="41dfe-129">Round-off value = 1.00</span></span> | <span data-ttu-id="41dfe-130">Námunda markaðsvirði = 100,00</span><span class="sxs-lookup"><span data-stu-id="41dfe-130">Round-off value = 100.00</span></span> | <span data-ttu-id="41dfe-131">Námunda markaðsvirði = 0,00</span><span class="sxs-lookup"><span data-stu-id="41dfe-131">Round-off value = 0.00</span></span>   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| <span data-ttu-id="41dfe-132">Venjulegt</span><span class="sxs-lookup"><span data-stu-id="41dfe-132">Normal</span></span>                              | <span data-ttu-id="41dfe-133">98,765.43</span><span class="sxs-lookup"><span data-stu-id="41dfe-133">98,765.43</span></span>              | <span data-ttu-id="41dfe-134">98,765.40</span><span class="sxs-lookup"><span data-stu-id="41dfe-134">98,765.40</span></span>              | <span data-ttu-id="41dfe-135">98,765.00</span><span class="sxs-lookup"><span data-stu-id="41dfe-135">98,765.00</span></span>              | <span data-ttu-id="41dfe-136">98,800.00</span><span class="sxs-lookup"><span data-stu-id="41dfe-136">98,800.00</span></span>                | <span data-ttu-id="41dfe-137">98,765.43</span><span class="sxs-lookup"><span data-stu-id="41dfe-137">98,765.43</span></span>                |
| <span data-ttu-id="41dfe-138">Slétta niður</span><span class="sxs-lookup"><span data-stu-id="41dfe-138">Downward</span></span>                            | <span data-ttu-id="41dfe-139">98,765.43</span><span class="sxs-lookup"><span data-stu-id="41dfe-139">98,765.43</span></span>              | <span data-ttu-id="41dfe-140">98,765.40</span><span class="sxs-lookup"><span data-stu-id="41dfe-140">98,765.40</span></span>              | <span data-ttu-id="41dfe-141">98,765.00</span><span class="sxs-lookup"><span data-stu-id="41dfe-141">98,765.00</span></span>              | <span data-ttu-id="41dfe-142">98,700.00</span><span class="sxs-lookup"><span data-stu-id="41dfe-142">98,700.00</span></span>                | <span data-ttu-id="41dfe-143">98,765.00</span><span class="sxs-lookup"><span data-stu-id="41dfe-143">98,765.00</span></span>                |
| <span data-ttu-id="41dfe-144">Slétta upp</span><span class="sxs-lookup"><span data-stu-id="41dfe-144">Rounding-up</span></span>                         | <span data-ttu-id="41dfe-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="41dfe-145">98,765.43</span></span>              | <span data-ttu-id="41dfe-146">98,765.50</span><span class="sxs-lookup"><span data-stu-id="41dfe-146">98,765.50</span></span>              | <span data-ttu-id="41dfe-147">98,766.00</span><span class="sxs-lookup"><span data-stu-id="41dfe-147">98,766.00</span></span>              | <span data-ttu-id="41dfe-148">98,800.00</span><span class="sxs-lookup"><span data-stu-id="41dfe-148">98,800.00</span></span>                | <span data-ttu-id="41dfe-149">98,766.00</span><span class="sxs-lookup"><span data-stu-id="41dfe-149">98,766.00</span></span>                |
| <span data-ttu-id="41dfe-150">Eigin hagur fyrir kreditstöðu</span><span class="sxs-lookup"><span data-stu-id="41dfe-150">Own advantage, for a credit balance</span></span> | <span data-ttu-id="41dfe-151">98,765.43</span><span class="sxs-lookup"><span data-stu-id="41dfe-151">98,765.43</span></span>              | <span data-ttu-id="41dfe-152">98,765.40</span><span class="sxs-lookup"><span data-stu-id="41dfe-152">98,765.40</span></span>              | <span data-ttu-id="41dfe-153">98,765.00</span><span class="sxs-lookup"><span data-stu-id="41dfe-153">98,765.00</span></span>              | <span data-ttu-id="41dfe-154">98,700.00</span><span class="sxs-lookup"><span data-stu-id="41dfe-154">98,700.00</span></span>                | <span data-ttu-id="41dfe-155">98,765.00</span><span class="sxs-lookup"><span data-stu-id="41dfe-155">98,765.00</span></span>                |
| <span data-ttu-id="41dfe-156">Eigin hagur fyrir debetstöðu</span><span class="sxs-lookup"><span data-stu-id="41dfe-156">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="41dfe-157">98,765.43</span><span class="sxs-lookup"><span data-stu-id="41dfe-157">98,765.43</span></span>              | <span data-ttu-id="41dfe-158">98,765.50</span><span class="sxs-lookup"><span data-stu-id="41dfe-158">98,765.50</span></span>              | <span data-ttu-id="41dfe-159">98,766.00</span><span class="sxs-lookup"><span data-stu-id="41dfe-159">98,766.00</span></span>              | <span data-ttu-id="41dfe-160">98,800.00</span><span class="sxs-lookup"><span data-stu-id="41dfe-160">98,800.00</span></span>                | <span data-ttu-id="41dfe-161">98,766.00</span><span class="sxs-lookup"><span data-stu-id="41dfe-161">98,766.00</span></span>                |

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="41dfe-162">Venjuleg sléttun og sléttunarnákvæmni er 0,01</span><span class="sxs-lookup"><span data-stu-id="41dfe-162">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="41dfe-163">Sléttun</span><span class="sxs-lookup"><span data-stu-id="41dfe-163">Rounding</span></span>
    </td>
    <td><span data-ttu-id="41dfe-164">Ferli útreiknings</span><span class="sxs-lookup"><span data-stu-id="41dfe-164">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="41dfe-165">sléttun(1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="41dfe-165">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="41dfe-166">sléttun(1,015 / 0,01, 0) = sléttun(101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="41dfe-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="41dfe-167">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="41dfe-167">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="41dfe-168">sléttun(1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="41dfe-168">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="41dfe-169">sléttun(1,014 / 0,01, 0) = sléttun(101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="41dfe-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="41dfe-170">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="41dfe-170">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="41dfe-171">sléttun(1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="41dfe-171">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="41dfe-172">sléttun(1,011 / 0,02, 0) = sléttun(50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="41dfe-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="41dfe-173">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="41dfe-173">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="41dfe-174">sléttun(1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="41dfe-174">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="41dfe-175">sléttun(1,009 / 0,02, 0) = sléttun(50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="41dfe-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="41dfe-176">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="41dfe-176">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="41dfe-177">Ef þú velur Eigin hagur er sléttun alltaf í hag lögaðila.</span><span class="sxs-lookup"><span data-stu-id="41dfe-177">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="41dfe-178">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="41dfe-178">For more information, see the following topics:</span></span>
- [<span data-ttu-id="41dfe-179">Yfirlit virðisaukaskatts</span><span class="sxs-lookup"><span data-stu-id="41dfe-179">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="41dfe-180">Stofna VSK-greiðslu</span><span class="sxs-lookup"><span data-stu-id="41dfe-180">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="41dfe-181">Stofna VSK-færslur í skjölum</span><span class="sxs-lookup"><span data-stu-id="41dfe-181">Create sales tax transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="41dfe-182">Skoða bókaðar VSK-færslur</span><span class="sxs-lookup"><span data-stu-id="41dfe-182">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="41dfe-183">sléttunarvirkni</span><span class="sxs-lookup"><span data-stu-id="41dfe-183">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


