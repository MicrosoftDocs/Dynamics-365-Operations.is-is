---
title: Útreikningur á VSK-skatti í almennum færslubókarlínum
description: Þetta efni útskýrir hvernig VSK-skattur er reiknaður fyrir mismunandi gerðir lykla (lánardrottna, viðskiptavina, fjárhag og verkefni) á almennum dagbókarlínum.
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 51d43c8e6d16201e1f8c392c13ead20287782dcc
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2020
ms.locfileid: "3983598"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="2fa32-103">Útreikningur á VSK-skatti í almennum færslubókarlínum</span><span class="sxs-lookup"><span data-stu-id="2fa32-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="2fa32-104">Þetta efni útskýrir hvernig VSK-skattur er reiknaður fyrir mismunandi gerðir lykla (lánardrottna, viðskiptavina, fjárhag og verkefni) á almennum dagbókarlínum.</span><span class="sxs-lookup"><span data-stu-id="2fa32-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="2fa32-105">Skipta má ferlinu í þrjú skref:</span><span class="sxs-lookup"><span data-stu-id="2fa32-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="2fa32-106">Ákvarðið stefnu VSK-skatts.</span><span class="sxs-lookup"><span data-stu-id="2fa32-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="2fa32-107">Ákvarðið VSK-skattupphæð sem verður geymd í tímabundinni VSK-skattatöflu.</span><span class="sxs-lookup"><span data-stu-id="2fa32-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="2fa32-108">Ákvarðið VSK-skattupphæð og lykil á fylgiskjalið.</span><span class="sxs-lookup"><span data-stu-id="2fa32-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="2fa32-109">Ákvarðið stefnu VSK-skatts</span><span class="sxs-lookup"><span data-stu-id="2fa32-109">Determine the sales tax direction</span></span>

<span data-ttu-id="2fa32-110">Hvernig stefna VSK-skatts er ákvörðuð fer eftir gerð lykils í fylgiskjalinu.</span><span class="sxs-lookup"><span data-stu-id="2fa32-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="2fa32-111">Stefna VSK-skatts ræðst af samsetningu gerð lykils og VSK-kóða.</span><span class="sxs-lookup"><span data-stu-id="2fa32-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="2fa32-112">Eftirfarandi hlutar fjalla nánar um valkostina.</span><span class="sxs-lookup"><span data-stu-id="2fa32-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="2fa32-113">Lykilgerðin er Verk</span><span class="sxs-lookup"><span data-stu-id="2fa32-113">Account type is Project</span></span>

<span data-ttu-id="2fa32-114">Ef fylgiskjalið er með færslubókarlínu þar sem lykilgerðin er **Verk** beita allar færslubókarlínur í fylgiskjalinu sömu skattastefnu.</span><span class="sxs-lookup"><span data-stu-id="2fa32-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="2fa32-115">Eftirfarandi mynd sýnir regluna.</span><span class="sxs-lookup"><span data-stu-id="2fa32-115">The following illustration shows the rule.</span></span> <span data-ttu-id="2fa32-116">Eftirfarandi atriði sýna hugsanlegar skattaleiðbeiningar fyrir verklykla.</span><span class="sxs-lookup"><span data-stu-id="2fa32-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="2fa32-117">•   Ef VSK-skattsnúmerið er neysluskattur, þá er VSK-skattsstefnan Neysluskattur.</span><span class="sxs-lookup"><span data-stu-id="2fa32-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="2fa32-118">•   Ef VSK-skattsnúmerið er undanþegið skatti, þá er VSK-skattsstefnan Innkaup án skatts.</span><span class="sxs-lookup"><span data-stu-id="2fa32-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="2fa32-119">•   Ef VSK-skattsnúmerið er VSK á milli fyrirtækja, þá er VSK-skattsstefnan Útskattur.</span><span class="sxs-lookup"><span data-stu-id="2fa32-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="2fa32-120">•   Ef VSK-skattsnúmerið er bakfært gjald, þá er VSK-skattsstefnan Útskattur.</span><span class="sxs-lookup"><span data-stu-id="2fa32-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="2fa32-121">Annars er stefna VSK-skatts Innskattur.</span><span class="sxs-lookup"><span data-stu-id="2fa32-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="2fa32-122">Eftirfarandi skýringarmynd sýnir regluna myndrænt.</span><span class="sxs-lookup"><span data-stu-id="2fa32-122">The following diagram illustrates the rule graphically.</span></span>

![Möguleikar á skattastefnu vegna verklykla](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="2fa32-124">Lykilgerðin er Lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="2fa32-124">Account type is Vendor</span></span>

<span data-ttu-id="2fa32-125">Ef fylgiskjalið er með færslubókarlínu þar sem lykilgerðin er **Lánardrottinn** beita allar færslubókarlínur í fylgiskjalinu sömu skattastefnu.</span><span class="sxs-lookup"><span data-stu-id="2fa32-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="2fa32-126">Eftirfarandi atriði sýna hugsanlegar skattaleiðbeiningar fyrir lánardrottnalykla.</span><span class="sxs-lookup"><span data-stu-id="2fa32-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="2fa32-127">•   Ef VSK-skattsnúmerið er neysluskattur, þá er VSK-skattsstefnan Neysluskattur.</span><span class="sxs-lookup"><span data-stu-id="2fa32-127">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="2fa32-128">•   Ef VSK-skattsnúmerið er undanþegið skatti, þá er VSK-skattsstefnan Innkaup án skatts.</span><span class="sxs-lookup"><span data-stu-id="2fa32-128">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="2fa32-129">•   Ef VSK-skattsnúmerið er VSK á milli fyrirtækja, þá er VSK-skattsstefnan Útskattur.</span><span class="sxs-lookup"><span data-stu-id="2fa32-129">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="2fa32-130">•   Ef VSK-skattsnúmerið er bakfært gjald, þá er VSK-skattsstefnan Útskattur.</span><span class="sxs-lookup"><span data-stu-id="2fa32-130">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="2fa32-131">Annars er stefna VSK-skatts Innskattur.</span><span class="sxs-lookup"><span data-stu-id="2fa32-131">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="2fa32-132">Eftirfarandi skýringarmynd sýnir regluna myndrænt.</span><span class="sxs-lookup"><span data-stu-id="2fa32-132">The following diagram illustrates the rule graphically.</span></span>

![Möguleikar á skattastefnu vegna lánardrottnalykla](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="2fa32-134">Lykilgerðin er Viðskiptavinur</span><span class="sxs-lookup"><span data-stu-id="2fa32-134">Account type is Customer</span></span>

<span data-ttu-id="2fa32-135">Ef fylgiskjalið er með færslubókarlínu þar sem lykilgerðin er **Viðskiptavinur** beita allar færslubókarlínur í fylgiskjalinu sömu skattastefnu.</span><span class="sxs-lookup"><span data-stu-id="2fa32-135">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="2fa32-136">Eftirfarandi atriði sýna hugsanlegar skattaleiðbeiningar fyrir viðskiptavinalykla.</span><span class="sxs-lookup"><span data-stu-id="2fa32-136">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="2fa32-137">•   Ef VSK-skattsnúmerið er undanþegið skatti, þá er VSK-skattsstefnan Innkaup án skatts.</span><span class="sxs-lookup"><span data-stu-id="2fa32-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="2fa32-138">•   Ef VSK-skattsnúmerið er VSK á milli fyrirtækja, þá er VSK-skattsstefnan Innskattur.</span><span class="sxs-lookup"><span data-stu-id="2fa32-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="2fa32-139">•   Ef VSK-skattsnúmerið er bakfært gjald, þá er VSK-skattsstefnan Innskattur.</span><span class="sxs-lookup"><span data-stu-id="2fa32-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="2fa32-140">Annars er stefna VSK-skatts Útskattur.</span><span class="sxs-lookup"><span data-stu-id="2fa32-140">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="2fa32-141">Eftirfarandi skýringarmynd sýnir regluna myndrænt.</span><span class="sxs-lookup"><span data-stu-id="2fa32-141">The following diagram illustrates the rule graphically.</span></span>

![Möguleikar á skattastefnu vegna viðskiptavinalykla](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="2fa32-143">Lykilgerðin er Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="2fa32-143">Account type is Ledger</span></span>

<span data-ttu-id="2fa32-144">Eftirfarandi mynd sýnir regluna sem gildir þegar fylgiskjalið hefur aðeins dagbókarlínur þar sem gerð lykilsins er **Fjárhagur**.</span><span class="sxs-lookup"><span data-stu-id="2fa32-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="2fa32-145">Eftirfarandi atriði sýna hugsanlegar skattaleiðbeiningar fyrir fjárhagslykla.</span><span class="sxs-lookup"><span data-stu-id="2fa32-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="2fa32-146">•   Ef VSK-skattsnúmerið er neysluskattur, þá er VSK-skattsstefnan Neysluskattur.</span><span class="sxs-lookup"><span data-stu-id="2fa32-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="2fa32-147">•   Ef VSK-skattsnúmerið er undanþegið skatti, þá er VSK-skattsstefnan Innkaup án skatts.</span><span class="sxs-lookup"><span data-stu-id="2fa32-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="2fa32-148">Annars, ef dagbókarupphæðin er debet (jákvæð), er VSK-skattsstefna Innskattur; ef dagbókarupphæðin er kredit (neikvæð), þá er VSK-skattsstefna Útskattur.</span><span class="sxs-lookup"><span data-stu-id="2fa32-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="2fa32-149">Eftirfarandi skýringarmynd sýnir regluna myndrænt.</span><span class="sxs-lookup"><span data-stu-id="2fa32-149">The following diagram illustrates the rule graphically.</span></span>

![Möguleikar á skattastefnu vegna fjárhagslykla](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="2fa32-151">Hnekkið stefnu VSK-skatts</span><span class="sxs-lookup"><span data-stu-id="2fa32-151">Override the sales tax direction</span></span>

<span data-ttu-id="2fa32-152">Þú getur hnekkt stefnu VSK-skatts þegar fylgiskjalið inniheldur aðeins línur þar sem gerð reikningsins er **Fjárhagur**.</span><span class="sxs-lookup"><span data-stu-id="2fa32-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="2fa32-153">Farðu í **Fjárhag \> Bókhaldslykil \> Lyklar \> Aðallyklar** og veldu flýtiflipann **Lögaðili hnekkir**.</span><span class="sxs-lookup"><span data-stu-id="2fa32-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="2fa32-154">Ákvarðið upphæð VSK-skatts</span><span class="sxs-lookup"><span data-stu-id="2fa32-154">Determine the sales tax amount</span></span>

<span data-ttu-id="2fa32-155">Í þessum kafla er lýst hvernig VSK-skattsupphæðartákn er reiknað.</span><span class="sxs-lookup"><span data-stu-id="2fa32-155">This section describes how the sales tax amount sign is calculated.</span></span>

![Síða virðisaukaskattsfærslna](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="2fa32-157">Eftirfarandi tafla sýnir almenna regluna til að ákvarða merki um VSK-skattsupphæðir í tímabundinni VSK-skattatöflu.</span><span class="sxs-lookup"><span data-stu-id="2fa32-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="2fa32-158">Upphæð færslubókarlínu</span><span class="sxs-lookup"><span data-stu-id="2fa32-158">Journal line amount</span></span> | <span data-ttu-id="2fa32-159">Stefna VSK</span><span class="sxs-lookup"><span data-stu-id="2fa32-159">Sales tax direction</span></span>  | <span data-ttu-id="2fa32-160">Merki VSK-skattupphæðar</span><span class="sxs-lookup"><span data-stu-id="2fa32-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="2fa32-161">Jákvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-161">Positive</span></span>            | <span data-ttu-id="2fa32-162">Innskattur</span><span class="sxs-lookup"><span data-stu-id="2fa32-162">Sales Tax Receivable</span></span> | <span data-ttu-id="2fa32-163">Jákvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-163">Positive</span></span>              |
| <span data-ttu-id="2fa32-164">Jákvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-164">Positive</span></span>            | <span data-ttu-id="2fa32-165">Útskattur</span><span class="sxs-lookup"><span data-stu-id="2fa32-165">Sales Tax Payable</span></span>    | <span data-ttu-id="2fa32-166">Neikvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-166">Negative</span></span>              |
| <span data-ttu-id="2fa32-167">Neikvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-167">Negative</span></span>            | <span data-ttu-id="2fa32-168">Innskattur</span><span class="sxs-lookup"><span data-stu-id="2fa32-168">Sales Tax Receivable</span></span> | <span data-ttu-id="2fa32-169">Neikvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-169">Negative</span></span>              |
| <span data-ttu-id="2fa32-170">Neikvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-170">Negative</span></span>            | <span data-ttu-id="2fa32-171">Útskattur</span><span class="sxs-lookup"><span data-stu-id="2fa32-171">Sales Tax Payable</span></span>    | <span data-ttu-id="2fa32-172">Jákvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-172">Positive</span></span>              |

<span data-ttu-id="2fa32-173">Það er sérstök regla fyrir fylgiskjöl sem hafa aðeins línurnar **Verk** eða **Fjárhagur**, þegar VSK-skattshópur eða VSK-skattshópur vöru er valinn á línunni **Fjárhagur**.</span><span class="sxs-lookup"><span data-stu-id="2fa32-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="2fa32-174">Þessari reglu er stjórnað af eiginleikanum Virkja sjálfstæðan útreikning á VSK-skatti fyrir almennar færslubækur.</span><span class="sxs-lookup"><span data-stu-id="2fa32-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="2fa32-175">Þegar slökkt er á þessari aðgerð notar skattafjárhæðin í línunni **Fjárhagur** stefnuna debet/kredit í línunni **Verk**.</span><span class="sxs-lookup"><span data-stu-id="2fa32-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="2fa32-176">Þegar kveikt er á þessari aðgerð notar skattafjárhæðin í línunni **Fjárhagur** sína eigin debet-/kreditstefnu.</span><span class="sxs-lookup"><span data-stu-id="2fa32-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="2fa32-177">Eftirfarandi töflur sýna regluna fyrir hverja atburðarás.</span><span class="sxs-lookup"><span data-stu-id="2fa32-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="2fa32-178">**Regla þegar kveikt er á eiginleikanum**</span><span class="sxs-lookup"><span data-stu-id="2fa32-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="2fa32-179">Færslubókarlínuupphæð verks</span><span class="sxs-lookup"><span data-stu-id="2fa32-179">Journal line amount of project</span></span> | <span data-ttu-id="2fa32-180">Stefna VSK</span><span class="sxs-lookup"><span data-stu-id="2fa32-180">Sales tax direction</span></span>  | <span data-ttu-id="2fa32-181">Merki VSK-skattupphæðar</span><span class="sxs-lookup"><span data-stu-id="2fa32-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="2fa32-182">Jákvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-182">Positive</span></span>                       | <span data-ttu-id="2fa32-183">Innskattur</span><span class="sxs-lookup"><span data-stu-id="2fa32-183">Sales Tax Receivable</span></span> | <span data-ttu-id="2fa32-184">Jákvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-184">Positive</span></span>              |
| <span data-ttu-id="2fa32-185">Neikvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-185">Negative</span></span>                       | <span data-ttu-id="2fa32-186">Innskattur</span><span class="sxs-lookup"><span data-stu-id="2fa32-186">Sales Tax Receivable</span></span> | <span data-ttu-id="2fa32-187">Neikvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-187">Negative</span></span>              |

<span data-ttu-id="2fa32-188">**Regla þegar slökkt er á eiginleikanum**</span><span class="sxs-lookup"><span data-stu-id="2fa32-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="2fa32-189">Færslubókarlínuupphæð fjárhags</span><span class="sxs-lookup"><span data-stu-id="2fa32-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="2fa32-190">Stefna VSK</span><span class="sxs-lookup"><span data-stu-id="2fa32-190">Sales tax direction</span></span>  | <span data-ttu-id="2fa32-191">Merki VSK-skattupphæðar</span><span class="sxs-lookup"><span data-stu-id="2fa32-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="2fa32-192">Jákvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-192">Positive</span></span>                       | <span data-ttu-id="2fa32-193">Innskattur</span><span class="sxs-lookup"><span data-stu-id="2fa32-193">Sales Tax Receivable</span></span> | <span data-ttu-id="2fa32-194">Jákvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-194">Positive</span></span>              |
| <span data-ttu-id="2fa32-195">Neikvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-195">Negative</span></span>                       | <span data-ttu-id="2fa32-196">Innskattur</span><span class="sxs-lookup"><span data-stu-id="2fa32-196">Sales Tax Receivable</span></span> | <span data-ttu-id="2fa32-197">Neikvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="2fa32-198">Ákvarðið VSK-skattupphæð og lykil á fylgiskjalið</span><span class="sxs-lookup"><span data-stu-id="2fa32-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="2fa32-199">Þegar þú bókar VSK-skatt er aðallykillinn sóttur úr forstillingum fjárhagsbókunarflokks.</span><span class="sxs-lookup"><span data-stu-id="2fa32-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="2fa32-200">Þegar VSK-skattar eru innskattur notar kerfið innskattslykil sem er tilgreindur í forstillingunum.</span><span class="sxs-lookup"><span data-stu-id="2fa32-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="2fa32-201">Fyrir VSK-skatt sem er útskattur notar kerfið útskattslykil sem er tilgreindur í forstillingunum.</span><span class="sxs-lookup"><span data-stu-id="2fa32-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="2fa32-202">Eftirfarandi tafla sýnir almennu regluna.</span><span class="sxs-lookup"><span data-stu-id="2fa32-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="2fa32-203">Stefna VSK</span><span class="sxs-lookup"><span data-stu-id="2fa32-203">Sales tax direction</span></span>  | <span data-ttu-id="2fa32-204">Merki VSK-skattupphæðar</span><span class="sxs-lookup"><span data-stu-id="2fa32-204">Sales tax amount sign</span></span> | <span data-ttu-id="2fa32-205">VSK-lykill</span><span class="sxs-lookup"><span data-stu-id="2fa32-205">Sales tax account</span></span>      | <span data-ttu-id="2fa32-206">Upphæð á fylgiskjali</span><span class="sxs-lookup"><span data-stu-id="2fa32-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="2fa32-207">Innskattur</span><span class="sxs-lookup"><span data-stu-id="2fa32-207">Sales Tax Receivable</span></span> | <span data-ttu-id="2fa32-208">Jákvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-208">Positive</span></span>              | <span data-ttu-id="2fa32-209">Viðskiptakröfulykill</span><span class="sxs-lookup"><span data-stu-id="2fa32-209">Tax Receivable Account</span></span> | <span data-ttu-id="2fa32-210">Jákvætt (debet)</span><span class="sxs-lookup"><span data-stu-id="2fa32-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="2fa32-211">Innskattur</span><span class="sxs-lookup"><span data-stu-id="2fa32-211">Sales Tax Receivable</span></span> | <span data-ttu-id="2fa32-212">Neikvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-212">Negative</span></span>              | <span data-ttu-id="2fa32-213">Viðskiptakröfulykill</span><span class="sxs-lookup"><span data-stu-id="2fa32-213">Tax Receivable Account</span></span> | <span data-ttu-id="2fa32-214">Neikvætt (kredit)</span><span class="sxs-lookup"><span data-stu-id="2fa32-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="2fa32-215">Útskattur</span><span class="sxs-lookup"><span data-stu-id="2fa32-215">Sales Tax Payable</span></span>    | <span data-ttu-id="2fa32-216">Jákvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-216">Positive</span></span>              | <span data-ttu-id="2fa32-217">Viðskiptaskuldalykill</span><span class="sxs-lookup"><span data-stu-id="2fa32-217">Tax Payable Account</span></span>    | <span data-ttu-id="2fa32-218">Neikvætt (kredit)</span><span class="sxs-lookup"><span data-stu-id="2fa32-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="2fa32-219">Útskattur</span><span class="sxs-lookup"><span data-stu-id="2fa32-219">Sales Tax Payable</span></span>    | <span data-ttu-id="2fa32-220">Neikvætt</span><span class="sxs-lookup"><span data-stu-id="2fa32-220">Negative</span></span>              | <span data-ttu-id="2fa32-221">Viðskiptaskuldalykill</span><span class="sxs-lookup"><span data-stu-id="2fa32-221">Tax Payable Account</span></span>    | <span data-ttu-id="2fa32-222">Jákvætt (debet)</span><span class="sxs-lookup"><span data-stu-id="2fa32-222">Positive (Debit)</span></span>  |
