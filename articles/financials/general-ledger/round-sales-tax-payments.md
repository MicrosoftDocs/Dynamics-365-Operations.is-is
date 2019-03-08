---
title: Vsk-greiðslur og sléttunarreglur
description: Þessi grein útskýrir hvernig uppsetning sléttunarreglu á Skattyfirvöld gengur fyrir sig og hvernig á að slétta virðisaukaskatt í ferlinu Jafna og bóka virðisaukaskatt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/01/2017
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
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f03336c834e74cd12d039c7b9692874843811746
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "367847"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="facd1-103">Vsk-greiðslur og sléttunarreglur</span><span class="sxs-lookup"><span data-stu-id="facd1-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="facd1-104">Þessi grein útskýrir hvernig uppsetning sléttunarreglu á Skattyfirvöld gengur fyrir sig og hvernig á að slétta virðisaukaskatt í ferlinu Jafna og bóka virðisaukaskatt.</span><span class="sxs-lookup"><span data-stu-id="facd1-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="facd1-105">Reglulega þarf að tilkynna vsk og greiða hann til skattayfirvalda.</span><span class="sxs-lookup"><span data-stu-id="facd1-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="facd1-106">Þetta er gert með því að keyra í jafna og bóka vsk-ferlið á síðunni Virðisaukaskattur.</span><span class="sxs-lookup"><span data-stu-id="facd1-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="facd1-107">Virðisaukaskattur fyrir tímabilið verða jafnaðar á móti lyklum virðisaukaskatts og staða virðisaukaskatts verður bókuð í lykilinn fyrir jöfnun vsk.</span><span class="sxs-lookup"><span data-stu-id="facd1-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="facd1-108">Stöðu virðisaukaskatts sem er bókuð í VSK-lykilinn er hægt slétta eins og krafist er á af skattayfirvöldum með því að setja upp sléttunarreglu á síðunni Virðisaukaskattur.</span><span class="sxs-lookup"><span data-stu-id="facd1-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="facd1-109">Sléttunarmismunur er bókaður á VSK-sléttunarlykil sem er valinn í lyklum fyrir sjálfvirkar færslur í reitnum Fjárhagur.</span><span class="sxs-lookup"><span data-stu-id="facd1-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="facd1-110">Dæmið hér að neðan sýnir hvernig sléttunarreglan á virðisaukaskattsyfirvöld virkar.</span><span class="sxs-lookup"><span data-stu-id="facd1-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

### <a name="example"></a><span data-ttu-id="facd1-111">Dæmi:</span><span class="sxs-lookup"><span data-stu-id="facd1-111">Example:</span></span>

<span data-ttu-id="facd1-112">Heildarupphæð VSK fyrir tímabil sýnir kreditstöðu-98,765.43.</span><span class="sxs-lookup"><span data-stu-id="facd1-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="facd1-113">Lögaðili innheimti hærri virðisaukaskattsupphæð en hann greiddi.</span><span class="sxs-lookup"><span data-stu-id="facd1-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="facd1-114">Þess vegna skuldar lögaðili peninga til skattyfirvalda.</span><span class="sxs-lookup"><span data-stu-id="facd1-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="facd1-115">Fyrirtækið vill nota sléttunaraðferð sem sléttar stöðuna í næstu 1,00 EUR.</span><span class="sxs-lookup"><span data-stu-id="facd1-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="facd1-116">Starfsmaðurinn sem ber ábyrgð á VSK-bókhaldi framkvæmir eftirfarandi skref.</span><span class="sxs-lookup"><span data-stu-id="facd1-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="facd1-117">Fara á Skattur &gt; Óbeinir skattar &gt; Virðisaukaskattur &gt; Virðisaukaskattsyfirvöld</span><span class="sxs-lookup"><span data-stu-id="facd1-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="facd1-118">Veljið Venjulegt í reitnum Sléttunarregla í Flýtiflipanum Almennt.</span><span class="sxs-lookup"><span data-stu-id="facd1-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="facd1-119">Í reitinn sléttun skal slá inn 1,00.</span><span class="sxs-lookup"><span data-stu-id="facd1-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="facd1-120">Þegar tími er kominn til að greiða skattyfirvöldum VSK-skattinn skal opna síðuna Jafna og bóka virðisaukaskatt.</span><span class="sxs-lookup"><span data-stu-id="facd1-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="facd1-121">(Fara á Skattur &gt; Skattframtöl &gt; Virðisaukaskattur &gt; Jafna og bóka vsk.)</span><span class="sxs-lookup"><span data-stu-id="facd1-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="facd1-122">Í vsk-jöfnunarlykli er upphæð skattskuldar upp á 98,765.43 sléttuð í 98,765.</span><span class="sxs-lookup"><span data-stu-id="facd1-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="facd1-123">Eftirfarandi tafla sýnir hvernig upphæðin 98,765.43 er sléttuð með því að nota hverja sléttunaraðferð sem tiltæk er í svæðið Sléttunarregla á síðunni Skattayfirvöld.</span><span class="sxs-lookup"><span data-stu-id="facd1-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="facd1-124">Skjámyndavalkostur fyrir sléttun</span><span class="sxs-lookup"><span data-stu-id="facd1-124">Rounding form option</span></span>                | <span data-ttu-id="facd1-125">Námunda markaðsvirði = 0,01</span><span class="sxs-lookup"><span data-stu-id="facd1-125">Round-off value = 0.01</span></span> | <span data-ttu-id="facd1-126">Námunda markaðsvirði = 0,10</span><span class="sxs-lookup"><span data-stu-id="facd1-126">Round-off value = 0.10</span></span> | <span data-ttu-id="facd1-127">Námunda markaðsvirði = 1,00</span><span class="sxs-lookup"><span data-stu-id="facd1-127">Round-off value = 1.00</span></span> | <span data-ttu-id="facd1-128">Námunda markaðsvirði = 100,00</span><span class="sxs-lookup"><span data-stu-id="facd1-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="facd1-129">Venjulegt</span><span class="sxs-lookup"><span data-stu-id="facd1-129">Normal</span></span>                              | <span data-ttu-id="facd1-130">98,765.43</span><span class="sxs-lookup"><span data-stu-id="facd1-130">98,765.43</span></span>              | <span data-ttu-id="facd1-131">98,765.40</span><span class="sxs-lookup"><span data-stu-id="facd1-131">98,765.40</span></span>              | <span data-ttu-id="facd1-132">98,765.00</span><span class="sxs-lookup"><span data-stu-id="facd1-132">98,765.00</span></span>              | <span data-ttu-id="facd1-133">98,800.00</span><span class="sxs-lookup"><span data-stu-id="facd1-133">98,800.00</span></span>                |
| <span data-ttu-id="facd1-134">Slétta niður</span><span class="sxs-lookup"><span data-stu-id="facd1-134">Downward</span></span>                            | <span data-ttu-id="facd1-135">98,765.43</span><span class="sxs-lookup"><span data-stu-id="facd1-135">98,765.43</span></span>              | <span data-ttu-id="facd1-136">98,765.40</span><span class="sxs-lookup"><span data-stu-id="facd1-136">98,765.40</span></span>              | <span data-ttu-id="facd1-137">98,765.00</span><span class="sxs-lookup"><span data-stu-id="facd1-137">98,765.00</span></span>              | <span data-ttu-id="facd1-138">98,700.00</span><span class="sxs-lookup"><span data-stu-id="facd1-138">98,700.00</span></span>                |
| <span data-ttu-id="facd1-139">Slétta upp</span><span class="sxs-lookup"><span data-stu-id="facd1-139">Rounding-up</span></span>                         | <span data-ttu-id="facd1-140">98,765.43</span><span class="sxs-lookup"><span data-stu-id="facd1-140">98,765.43</span></span>              | <span data-ttu-id="facd1-141">98,765.50</span><span class="sxs-lookup"><span data-stu-id="facd1-141">98,765.50</span></span>              | <span data-ttu-id="facd1-142">98,766.00</span><span class="sxs-lookup"><span data-stu-id="facd1-142">98,766.00</span></span>              | <span data-ttu-id="facd1-143">98,800.00</span><span class="sxs-lookup"><span data-stu-id="facd1-143">98,800.00</span></span>                |
| <span data-ttu-id="facd1-144">Eigin hagur fyrir kreditstöðu</span><span class="sxs-lookup"><span data-stu-id="facd1-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="facd1-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="facd1-145">98,765.43</span></span>              | <span data-ttu-id="facd1-146">98,765.40</span><span class="sxs-lookup"><span data-stu-id="facd1-146">98,765.40</span></span>              | <span data-ttu-id="facd1-147">98,765.00</span><span class="sxs-lookup"><span data-stu-id="facd1-147">98,765.00</span></span>              | <span data-ttu-id="facd1-148">98,700.00</span><span class="sxs-lookup"><span data-stu-id="facd1-148">98,700.00</span></span>                |
| <span data-ttu-id="facd1-149">Eigin hagur fyrir debetstöðu</span><span class="sxs-lookup"><span data-stu-id="facd1-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="facd1-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="facd1-150">98,765.43</span></span>              | <span data-ttu-id="facd1-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="facd1-151">98,765.50</span></span>              | <span data-ttu-id="facd1-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="facd1-152">98,766.00</span></span>              | <span data-ttu-id="facd1-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="facd1-153">98,800.00</span></span>                |

> [!NOTE]                                                                                  
> <span data-ttu-id="facd1-154">Ef þú velur Eigin hagur er sléttun alltaf í hag lögaðila.</span><span class="sxs-lookup"><span data-stu-id="facd1-154">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="facd1-155">Frekari upplýsingar er hægt að finna í eftirfarandi efni:</span><span class="sxs-lookup"><span data-stu-id="facd1-155">For more information, see the following topics:</span></span>
- [<span data-ttu-id="facd1-156">Yfirlit virðisaukaskatts</span><span class="sxs-lookup"><span data-stu-id="facd1-156">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="facd1-157">Stofna VSK-greiðslu</span><span class="sxs-lookup"><span data-stu-id="facd1-157">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="facd1-158">Stofna sölufærslur á skjölum</span><span class="sxs-lookup"><span data-stu-id="facd1-158">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="facd1-159">Skoða bókaðar VSK-færslur</span><span class="sxs-lookup"><span data-stu-id="facd1-159">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)


