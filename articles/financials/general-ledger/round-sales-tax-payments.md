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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1c1bb1c792eb79888a1df209f2eebaf14a38dd
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1531858"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="da6a7-103">Vsk-greiðslur og sléttunarreglur</span><span class="sxs-lookup"><span data-stu-id="da6a7-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="da6a7-104">Þessi grein útskýrir hvernig uppsetning sléttunarreglu á Skattyfirvöld gengur fyrir sig og hvernig á að slétta virðisaukaskatt í ferlinu Jafna og bóka virðisaukaskatt.</span><span class="sxs-lookup"><span data-stu-id="da6a7-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="da6a7-105">Reglulega þarf að tilkynna vsk og greiða hann til skattayfirvalda.</span><span class="sxs-lookup"><span data-stu-id="da6a7-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="da6a7-106">Þetta er gert með því að keyra í jafna og bóka vsk-ferlið á síðunni Virðisaukaskattur.</span><span class="sxs-lookup"><span data-stu-id="da6a7-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="da6a7-107">Virðisaukaskattur fyrir tímabilið verða jafnaðar á móti lyklum virðisaukaskatts og staða virðisaukaskatts verður bókuð í lykilinn fyrir jöfnun vsk.</span><span class="sxs-lookup"><span data-stu-id="da6a7-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="da6a7-108">Stöðu virðisaukaskatts sem er bókuð í VSK-lykilinn er hægt slétta eins og krafist er á af skattayfirvöldum með því að setja upp sléttunarreglu á síðunni Virðisaukaskattur.</span><span class="sxs-lookup"><span data-stu-id="da6a7-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="da6a7-109">Sléttunarmismunur er bókaður á VSK-sléttunarlykil sem er valinn í lyklum fyrir sjálfvirkar færslur í reitnum Fjárhagur.</span><span class="sxs-lookup"><span data-stu-id="da6a7-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="da6a7-110">Dæmið hér að neðan sýnir hvernig sléttunarreglan á virðisaukaskattsyfirvöld virkar.</span><span class="sxs-lookup"><span data-stu-id="da6a7-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="da6a7-111">Dæmi</span><span class="sxs-lookup"><span data-stu-id="da6a7-111">Examples</span></span>

<span data-ttu-id="da6a7-112">Heildarupphæð VSK fyrir tímabil sýnir kreditstöðu-98,765.43.</span><span class="sxs-lookup"><span data-stu-id="da6a7-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="da6a7-113">Lögaðili innheimti hærri virðisaukaskattsupphæð en hann greiddi.</span><span class="sxs-lookup"><span data-stu-id="da6a7-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="da6a7-114">Þess vegna skuldar lögaðili peninga til skattyfirvalda.</span><span class="sxs-lookup"><span data-stu-id="da6a7-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="da6a7-115">Fyrirtækið vill nota sléttunaraðferð sem sléttar stöðuna í næstu 1,00 EUR.</span><span class="sxs-lookup"><span data-stu-id="da6a7-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="da6a7-116">Starfsmaðurinn sem ber ábyrgð á VSK-bókhaldi framkvæmir eftirfarandi skref.</span><span class="sxs-lookup"><span data-stu-id="da6a7-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="da6a7-117">Fara á Skattur &gt; Óbeinir skattar &gt; Virðisaukaskattur &gt; Virðisaukaskattsyfirvöld</span><span class="sxs-lookup"><span data-stu-id="da6a7-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="da6a7-118">Veljið Venjulegt í reitnum Sléttunarregla í Flýtiflipanum Almennt.</span><span class="sxs-lookup"><span data-stu-id="da6a7-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="da6a7-119">Í reitinn sléttun skal slá inn 1,00.</span><span class="sxs-lookup"><span data-stu-id="da6a7-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="da6a7-120">Þegar tími er kominn til að greiða skattyfirvöldum VSK-skattinn skal opna síðuna Jafna og bóka virðisaukaskatt.</span><span class="sxs-lookup"><span data-stu-id="da6a7-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="da6a7-121">(Fara á Skattur &gt; Skattframtöl &gt; Virðisaukaskattur &gt; Jafna og bóka vsk.)</span><span class="sxs-lookup"><span data-stu-id="da6a7-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="da6a7-122">Í vsk-jöfnunarlykli er upphæð skattskuldar upp á 98,765.43 sléttuð í 98,765.</span><span class="sxs-lookup"><span data-stu-id="da6a7-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="da6a7-123">Eftirfarandi tafla sýnir hvernig upphæðin 98,765.43 er sléttuð með því að nota hverja sléttunaraðferð sem tiltæk er í svæðið Sléttunarregla á síðunni Skattayfirvöld.</span><span class="sxs-lookup"><span data-stu-id="da6a7-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="da6a7-124">Skjámyndavalkostur fyrir sléttun</span><span class="sxs-lookup"><span data-stu-id="da6a7-124">Rounding form option</span></span>                | <span data-ttu-id="da6a7-125">Námunda markaðsvirði = 0,01</span><span class="sxs-lookup"><span data-stu-id="da6a7-125">Round-off value = 0.01</span></span> | <span data-ttu-id="da6a7-126">Námunda markaðsvirði = 0,10</span><span class="sxs-lookup"><span data-stu-id="da6a7-126">Round-off value = 0.10</span></span> | <span data-ttu-id="da6a7-127">Námunda markaðsvirði = 1,00</span><span class="sxs-lookup"><span data-stu-id="da6a7-127">Round-off value = 1.00</span></span> | <span data-ttu-id="da6a7-128">Námunda markaðsvirði = 100,00</span><span class="sxs-lookup"><span data-stu-id="da6a7-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="da6a7-129">Venjulegt</span><span class="sxs-lookup"><span data-stu-id="da6a7-129">Normal</span></span>                              | <span data-ttu-id="da6a7-130">98,765.43</span><span class="sxs-lookup"><span data-stu-id="da6a7-130">98,765.43</span></span>              | <span data-ttu-id="da6a7-131">98,765.40</span><span class="sxs-lookup"><span data-stu-id="da6a7-131">98,765.40</span></span>              | <span data-ttu-id="da6a7-132">98,765.00</span><span class="sxs-lookup"><span data-stu-id="da6a7-132">98,765.00</span></span>              | <span data-ttu-id="da6a7-133">98,800.00</span><span class="sxs-lookup"><span data-stu-id="da6a7-133">98,800.00</span></span>                |
| <span data-ttu-id="da6a7-134">Slétta niður</span><span class="sxs-lookup"><span data-stu-id="da6a7-134">Downward</span></span>                            | <span data-ttu-id="da6a7-135">98,765.43</span><span class="sxs-lookup"><span data-stu-id="da6a7-135">98,765.43</span></span>              | <span data-ttu-id="da6a7-136">98,765.40</span><span class="sxs-lookup"><span data-stu-id="da6a7-136">98,765.40</span></span>              | <span data-ttu-id="da6a7-137">98,765.00</span><span class="sxs-lookup"><span data-stu-id="da6a7-137">98,765.00</span></span>              | <span data-ttu-id="da6a7-138">98,700.00</span><span class="sxs-lookup"><span data-stu-id="da6a7-138">98,700.00</span></span>                |
| <span data-ttu-id="da6a7-139">Slétta upp</span><span class="sxs-lookup"><span data-stu-id="da6a7-139">Rounding-up</span></span>                         | <span data-ttu-id="da6a7-140">98,765.43</span><span class="sxs-lookup"><span data-stu-id="da6a7-140">98,765.43</span></span>              | <span data-ttu-id="da6a7-141">98,765.50</span><span class="sxs-lookup"><span data-stu-id="da6a7-141">98,765.50</span></span>              | <span data-ttu-id="da6a7-142">98,766.00</span><span class="sxs-lookup"><span data-stu-id="da6a7-142">98,766.00</span></span>              | <span data-ttu-id="da6a7-143">98,800.00</span><span class="sxs-lookup"><span data-stu-id="da6a7-143">98,800.00</span></span>                |
| <span data-ttu-id="da6a7-144">Eigin hagur fyrir kreditstöðu</span><span class="sxs-lookup"><span data-stu-id="da6a7-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="da6a7-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="da6a7-145">98,765.43</span></span>              | <span data-ttu-id="da6a7-146">98,765.40</span><span class="sxs-lookup"><span data-stu-id="da6a7-146">98,765.40</span></span>              | <span data-ttu-id="da6a7-147">98,765.00</span><span class="sxs-lookup"><span data-stu-id="da6a7-147">98,765.00</span></span>              | <span data-ttu-id="da6a7-148">98,700.00</span><span class="sxs-lookup"><span data-stu-id="da6a7-148">98,700.00</span></span>                |
| <span data-ttu-id="da6a7-149">Eigin hagur fyrir debetstöðu</span><span class="sxs-lookup"><span data-stu-id="da6a7-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="da6a7-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="da6a7-150">98,765.43</span></span>              | <span data-ttu-id="da6a7-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="da6a7-151">98,765.50</span></span>              | <span data-ttu-id="da6a7-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="da6a7-152">98,766.00</span></span>              | <span data-ttu-id="da6a7-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="da6a7-153">98,800.00</span></span>                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a><span data-ttu-id="da6a7-154">Engin sléttun vegna þess að sléttunin er 0,00</span><span class="sxs-lookup"><span data-stu-id="da6a7-154">No rounding at all, since the round-off is 0.00</span></span>

<span data-ttu-id="da6a7-155">sléttun(1,0151, 0,00) = 1,0151 sléttun(1,0149, 0,00) = 1,0149</span><span class="sxs-lookup"><span data-stu-id="da6a7-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span></span>

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="da6a7-156">Venjuleg sléttun og sléttunarnákvæmni er 0,01</span><span class="sxs-lookup"><span data-stu-id="da6a7-156">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="da6a7-157">Sléttun</span><span class="sxs-lookup"><span data-stu-id="da6a7-157">Rounding</span></span>
    </td>
    <td><span data-ttu-id="da6a7-158">Ferli útreiknings</span><span class="sxs-lookup"><span data-stu-id="da6a7-158">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="da6a7-159">sléttun(1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="da6a7-159">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="da6a7-160">sléttun(1,015 / 0,01, 0) = sléttun(101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="da6a7-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="da6a7-161">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="da6a7-161">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="da6a7-162">sléttun(1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="da6a7-162">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="da6a7-163">sléttun(1,014 / 0,01, 0) = sléttun(101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="da6a7-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="da6a7-164">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="da6a7-164">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="da6a7-165">sléttun(1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="da6a7-165">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="da6a7-166">sléttun(1,011 / 0,02, 0) = sléttun(50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="da6a7-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="da6a7-167">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="da6a7-167">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="da6a7-168">sléttun(1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="da6a7-168">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="da6a7-169">sléttun(1,009 / 0,02, 0) = sléttun(50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="da6a7-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="da6a7-170">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="da6a7-170">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="da6a7-171">Ef þú velur Eigin hagur er sléttun alltaf í hag lögaðila.</span><span class="sxs-lookup"><span data-stu-id="da6a7-171">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="da6a7-172">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="da6a7-172">For more information, see the following topics:</span></span>
- [<span data-ttu-id="da6a7-173">Yfirlit virðisaukaskatts</span><span class="sxs-lookup"><span data-stu-id="da6a7-173">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="da6a7-174">Stofna VSK-greiðslu</span><span class="sxs-lookup"><span data-stu-id="da6a7-174">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="da6a7-175">Stofna sölufærslur á skjölum</span><span class="sxs-lookup"><span data-stu-id="da6a7-175">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="da6a7-176">Skoða bókaðar VSK-færslur</span><span class="sxs-lookup"><span data-stu-id="da6a7-176">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="da6a7-177">sléttunarvirkni</span><span class="sxs-lookup"><span data-stu-id="da6a7-177">round Function</span></span>](https://msdn.microsoft.com/en-us/library/aa850656.aspx)


