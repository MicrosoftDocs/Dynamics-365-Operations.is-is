---
title: Vsk-greiðslur og sléttunarreglur
description: Þessi grein útskýrir hvernig uppsetning sléttunarreglu á Skattyfirvöld gengur fyrir sig og hvernig á að slétta virðisaukaskatt í ferlinu Jafna og bóka virðisaukaskatt.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
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
ms.openlocfilehash: 4e66a62007025964b3d58ff0620ebecd6d9769f9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771753"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="2af7f-103">Vsk-greiðslur og sléttunarreglur</span><span class="sxs-lookup"><span data-stu-id="2af7f-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2af7f-104">Þessi grein útskýrir hvernig uppsetning sléttunarreglu á Skattyfirvöld gengur fyrir sig og hvernig á að slétta virðisaukaskatt í ferlinu Jafna og bóka virðisaukaskatt.</span><span class="sxs-lookup"><span data-stu-id="2af7f-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="2af7f-105">Reglulega þarf að tilkynna vsk og greiða hann til skattayfirvalda.</span><span class="sxs-lookup"><span data-stu-id="2af7f-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="2af7f-106">Þetta er gert með því að keyra í jafna og bóka vsk-ferlið á síðunni Virðisaukaskattur.</span><span class="sxs-lookup"><span data-stu-id="2af7f-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="2af7f-107">Virðisaukaskattur fyrir tímabilið verða jafnaðar á móti lyklum virðisaukaskatts og staða virðisaukaskatts verður bókuð í lykilinn fyrir jöfnun vsk.</span><span class="sxs-lookup"><span data-stu-id="2af7f-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="2af7f-108">Stöðu virðisaukaskatts sem er bókuð í VSK-lykilinn er hægt slétta eins og krafist er á af skattayfirvöldum með því að setja upp sléttunarreglu á síðunni Virðisaukaskattur.</span><span class="sxs-lookup"><span data-stu-id="2af7f-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="2af7f-109">Sléttunarmismunur er bókaður á VSK-sléttunarlykil sem er valinn í lyklum fyrir sjálfvirkar færslur í reitnum Fjárhagur.</span><span class="sxs-lookup"><span data-stu-id="2af7f-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="2af7f-110">Dæmið hér að neðan sýnir hvernig sléttunarreglan á virðisaukaskattsyfirvöld virkar.</span><span class="sxs-lookup"><span data-stu-id="2af7f-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="2af7f-111">Dæmi</span><span class="sxs-lookup"><span data-stu-id="2af7f-111">Examples</span></span>

<span data-ttu-id="2af7f-112">Heildarupphæð VSK fyrir tímabil sýnir kreditstöðu-98,765.43.</span><span class="sxs-lookup"><span data-stu-id="2af7f-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="2af7f-113">Lögaðili innheimti hærri virðisaukaskattsupphæð en hann greiddi.</span><span class="sxs-lookup"><span data-stu-id="2af7f-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="2af7f-114">Þess vegna skuldar lögaðili peninga til skattyfirvalda.</span><span class="sxs-lookup"><span data-stu-id="2af7f-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="2af7f-115">Fyrirtækið vill nota sléttunaraðferð sem sléttar stöðuna í næstu 1,00 EUR.</span><span class="sxs-lookup"><span data-stu-id="2af7f-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="2af7f-116">Starfsmaðurinn sem ber ábyrgð á VSK-bókhaldi framkvæmir eftirfarandi skref.</span><span class="sxs-lookup"><span data-stu-id="2af7f-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="2af7f-117">Fara á Skattur &gt; Óbeinir skattar &gt; Virðisaukaskattur &gt; Virðisaukaskattsyfirvöld</span><span class="sxs-lookup"><span data-stu-id="2af7f-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="2af7f-118">Veljið Venjulegt í reitnum Sléttunarregla í Flýtiflipanum Almennt.</span><span class="sxs-lookup"><span data-stu-id="2af7f-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="2af7f-119">Í reitinn sléttun skal slá inn 1,00.</span><span class="sxs-lookup"><span data-stu-id="2af7f-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="2af7f-120">Þegar tími er kominn til að greiða skattyfirvöldum VSK-skattinn skal opna síðuna Jafna og bóka virðisaukaskatt.</span><span class="sxs-lookup"><span data-stu-id="2af7f-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="2af7f-121">(Fara á Skattur &gt; Skattframtöl &gt; Virðisaukaskattur &gt; Jafna og bóka vsk.)</span><span class="sxs-lookup"><span data-stu-id="2af7f-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="2af7f-122">Í vsk-jöfnunarlykli er upphæð skattskuldar upp á 98,765.43 sléttuð í 98,765.</span><span class="sxs-lookup"><span data-stu-id="2af7f-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="2af7f-123">Eftirfarandi tafla sýnir hvernig upphæðin 98,765.43 er sléttuð með því að nota hverja sléttunaraðferð sem tiltæk er í svæðið Sléttunarregla á síðunni Skattayfirvöld.</span><span class="sxs-lookup"><span data-stu-id="2af7f-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="2af7f-124">Skjámyndavalkostur fyrir sléttun</span><span class="sxs-lookup"><span data-stu-id="2af7f-124">Rounding form option</span></span>                | <span data-ttu-id="2af7f-125">Námunda markaðsvirði = 0,01</span><span class="sxs-lookup"><span data-stu-id="2af7f-125">Round-off value = 0.01</span></span> | <span data-ttu-id="2af7f-126">Námunda markaðsvirði = 0,10</span><span class="sxs-lookup"><span data-stu-id="2af7f-126">Round-off value = 0.10</span></span> | <span data-ttu-id="2af7f-127">Námunda markaðsvirði = 1,00</span><span class="sxs-lookup"><span data-stu-id="2af7f-127">Round-off value = 1.00</span></span> | <span data-ttu-id="2af7f-128">Námunda markaðsvirði = 100,00</span><span class="sxs-lookup"><span data-stu-id="2af7f-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="2af7f-129">Venjulegt</span><span class="sxs-lookup"><span data-stu-id="2af7f-129">Normal</span></span>                              | <span data-ttu-id="2af7f-130">98,765.43</span><span class="sxs-lookup"><span data-stu-id="2af7f-130">98,765.43</span></span>              | <span data-ttu-id="2af7f-131">98,765.40</span><span class="sxs-lookup"><span data-stu-id="2af7f-131">98,765.40</span></span>              | <span data-ttu-id="2af7f-132">98,765.00</span><span class="sxs-lookup"><span data-stu-id="2af7f-132">98,765.00</span></span>              | <span data-ttu-id="2af7f-133">98,800.00</span><span class="sxs-lookup"><span data-stu-id="2af7f-133">98,800.00</span></span>                |
| <span data-ttu-id="2af7f-134">Slétta niður</span><span class="sxs-lookup"><span data-stu-id="2af7f-134">Downward</span></span>                            | <span data-ttu-id="2af7f-135">98,765.43</span><span class="sxs-lookup"><span data-stu-id="2af7f-135">98,765.43</span></span>              | <span data-ttu-id="2af7f-136">98,765.40</span><span class="sxs-lookup"><span data-stu-id="2af7f-136">98,765.40</span></span>              | <span data-ttu-id="2af7f-137">98,765.00</span><span class="sxs-lookup"><span data-stu-id="2af7f-137">98,765.00</span></span>              | <span data-ttu-id="2af7f-138">98,700.00</span><span class="sxs-lookup"><span data-stu-id="2af7f-138">98,700.00</span></span>                |
| <span data-ttu-id="2af7f-139">Slétta upp</span><span class="sxs-lookup"><span data-stu-id="2af7f-139">Rounding-up</span></span>                         | <span data-ttu-id="2af7f-140">98,765.43</span><span class="sxs-lookup"><span data-stu-id="2af7f-140">98,765.43</span></span>              | <span data-ttu-id="2af7f-141">98,765.50</span><span class="sxs-lookup"><span data-stu-id="2af7f-141">98,765.50</span></span>              | <span data-ttu-id="2af7f-142">98,766.00</span><span class="sxs-lookup"><span data-stu-id="2af7f-142">98,766.00</span></span>              | <span data-ttu-id="2af7f-143">98,800.00</span><span class="sxs-lookup"><span data-stu-id="2af7f-143">98,800.00</span></span>                |
| <span data-ttu-id="2af7f-144">Eigin hagur fyrir kreditstöðu</span><span class="sxs-lookup"><span data-stu-id="2af7f-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="2af7f-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="2af7f-145">98,765.43</span></span>              | <span data-ttu-id="2af7f-146">98,765.40</span><span class="sxs-lookup"><span data-stu-id="2af7f-146">98,765.40</span></span>              | <span data-ttu-id="2af7f-147">98,765.00</span><span class="sxs-lookup"><span data-stu-id="2af7f-147">98,765.00</span></span>              | <span data-ttu-id="2af7f-148">98,700.00</span><span class="sxs-lookup"><span data-stu-id="2af7f-148">98,700.00</span></span>                |
| <span data-ttu-id="2af7f-149">Eigin hagur fyrir debetstöðu</span><span class="sxs-lookup"><span data-stu-id="2af7f-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="2af7f-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="2af7f-150">98,765.43</span></span>              | <span data-ttu-id="2af7f-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="2af7f-151">98,765.50</span></span>              | <span data-ttu-id="2af7f-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="2af7f-152">98,766.00</span></span>              | <span data-ttu-id="2af7f-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="2af7f-153">98,800.00</span></span>                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a><span data-ttu-id="2af7f-154">Engin sléttun vegna þess að sléttunin er 0,00</span><span class="sxs-lookup"><span data-stu-id="2af7f-154">No rounding at all, since the round-off is 0.00</span></span>

<span data-ttu-id="2af7f-155">sléttun(1,0151, 0,00) = 1,0151 sléttun(1,0149, 0,00) = 1,0149</span><span class="sxs-lookup"><span data-stu-id="2af7f-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span></span>

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="2af7f-156">Venjuleg sléttun og sléttunarnákvæmni er 0,01</span><span class="sxs-lookup"><span data-stu-id="2af7f-156">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="2af7f-157">Sléttun</span><span class="sxs-lookup"><span data-stu-id="2af7f-157">Rounding</span></span>
    </td>
    <td><span data-ttu-id="2af7f-158">Ferli útreiknings</span><span class="sxs-lookup"><span data-stu-id="2af7f-158">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="2af7f-159">sléttun(1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="2af7f-159">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="2af7f-160">sléttun(1,015 / 0,01, 0) = sléttun(101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="2af7f-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="2af7f-161">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="2af7f-161">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="2af7f-162">sléttun(1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="2af7f-162">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="2af7f-163">sléttun(1,014 / 0,01, 0) = sléttun(101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="2af7f-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="2af7f-164">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="2af7f-164">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="2af7f-165">sléttun(1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="2af7f-165">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="2af7f-166">sléttun(1,011 / 0,02, 0) = sléttun(50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="2af7f-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="2af7f-167">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="2af7f-167">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="2af7f-168">sléttun(1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="2af7f-168">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="2af7f-169">sléttun(1,009 / 0,02, 0) = sléttun(50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="2af7f-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="2af7f-170">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="2af7f-170">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="2af7f-171">Ef þú velur Eigin hagur er sléttun alltaf í hag lögaðila.</span><span class="sxs-lookup"><span data-stu-id="2af7f-171">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="2af7f-172">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="2af7f-172">For more information, see the following topics:</span></span>
- [<span data-ttu-id="2af7f-173">Yfirlit virðisaukaskatts</span><span class="sxs-lookup"><span data-stu-id="2af7f-173">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="2af7f-174">Stofna VSK-greiðslu</span><span class="sxs-lookup"><span data-stu-id="2af7f-174">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="2af7f-175">Stofna VSK-færslur í skjölum</span><span class="sxs-lookup"><span data-stu-id="2af7f-175">Create sales tax transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="2af7f-176">Skoða bókaðar VSK-færslur</span><span class="sxs-lookup"><span data-stu-id="2af7f-176">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="2af7f-177">sléttunarvirkni</span><span class="sxs-lookup"><span data-stu-id="2af7f-177">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


