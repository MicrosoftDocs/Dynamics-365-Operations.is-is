---
title: Fyrirframgreiðslur viðskiptavinar
description: Í þessu efnisatriði er því lýst hvernig á að setja upp og vinna úr fyrirframgreiðslum viðskiptavina (einnig þekkt sem innborganir viðskiptavina).
author: roschlom
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3314803b994aed40e5b04d8546a45bd305d48b6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019421"
---
# <a name="customer-prepayments"></a><span data-ttu-id="202f4-103">Fyrirframgreiðslur viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="202f4-103">Customer prepayments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="202f4-104">Fyrirframgreiðslur viðskiptavina eru notaðar þegar greiðsla frá viðskiptavini er móttekin en enginn reikningur er til staðar sem hægt er að jafna greiðsluna við.</span><span class="sxs-lookup"><span data-stu-id="202f4-104">Customer prepayments are used when you receive a payment from a customer, but there is no invoice that the payment can be settled against.</span></span> <span data-ttu-id="202f4-105">Þessar greiðslutegundir eru einnig kallaðar innborganir viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="202f4-105">These types of payments are also referred to as customer deposits.</span></span>

<span data-ttu-id="202f4-106">Ferlið við að setja upp og vinna með fyrirframgreiðslur viðskiptavina samanstendur af eftirfarandi grunnskrefum.</span><span class="sxs-lookup"><span data-stu-id="202f4-106">The process of setting up and working with customer prepayments consists of the following basic steps.</span></span>

1. <span data-ttu-id="202f4-107">Búðu til bókunarreglu viðskiptavinar fyrir fyrirframgreiðslur.</span><span class="sxs-lookup"><span data-stu-id="202f4-107">Create a customer posting profile for prepayments.</span></span>
2. <span data-ttu-id="202f4-108">Stillið færibreytuna **Bókunarregla með fylgiskjali fyrirframgreiðslubókar**.</span><span class="sxs-lookup"><span data-stu-id="202f4-108">Set the **Posting profile with prepayment journal voucher** parameter.</span></span>
3. <span data-ttu-id="202f4-109">Stofnið fyrirframgreiðslubók og veljið gátreitinn **Fylgiskjal fyrirframgreiðslubókar** í hverri línu.</span><span class="sxs-lookup"><span data-stu-id="202f4-109">Create a customer payment journal, and select the **Prepayment journal voucher** check box on each line.</span></span>
4. <span data-ttu-id="202f4-110">Bóka greiðslubók viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="202f4-110">Post the customer payment journal.</span></span>
5. <span data-ttu-id="202f4-111">Þegar búið er að búa til reikning skal jafna fyrirframgreiðsluna við hann með því að nota síðuna **Jafna opnar færslur**.</span><span class="sxs-lookup"><span data-stu-id="202f4-111">After an invoice is generated, settle the prepayment with it by using the **Settle open transactions** page.</span></span>

## <a name="create-a-customer-posting-profile-for-prepayments"></a><span data-ttu-id="202f4-112">Búðu til bókunarreglu viðskiptavinar fyrir fyrirframgreiðslur</span><span class="sxs-lookup"><span data-stu-id="202f4-112">Create a customer posting profile for prepayments</span></span>

<span data-ttu-id="202f4-113">Þegar fyrirframgreiðslur eða innborganir frá viðskiptavinum eru samþykktar áður en vörur eða þjónusta er afhent, eða áður en reikningur verður til í kerfinu, vill notandinn yfirleitt skrá reiðuféð sem skuld í stað eignar í bókhaldslyklinum.</span><span class="sxs-lookup"><span data-stu-id="202f4-113">Typically, when you accept prepayments or deposits from your customers before goods or services are delivered, or before an invoice exists in your system, you will want to record the cash as a liability instead of an asset in your chart of accounts.</span></span> <span data-ttu-id="202f4-114">Hins vegar geta kröfur vegna skráningar á þessum upphæðum í fjárhagnum verið mismunandi eftir landi eða svæði.</span><span class="sxs-lookup"><span data-stu-id="202f4-114">However, the requirements for recording these amounts in your general ledger might differ, depending on your country or region.</span></span> <span data-ttu-id="202f4-115">Því skal ráðfæra sig við bókarana varðandi staðbundnar reglugerðir sem eiga við.</span><span class="sxs-lookup"><span data-stu-id="202f4-115">Therefore, be sure to consult your accountants about any local regulations that apply.</span></span>

<span data-ttu-id="202f4-116">Almennt er ferlið við að búa til bókunarreglu sem hægt er að nota fyrir fyrirframgreiðslur það sama og ferlið við að búa til aðrar bókunarreglur.</span><span class="sxs-lookup"><span data-stu-id="202f4-116">In general, the process for creating a posting profile that can be used for prepayments is the same as the process for creating other posting profiles.</span></span> <span data-ttu-id="202f4-117">Helsti munurinn liggur í aðallyklinum sem er valinn í reitnum **Safnlykill**.</span><span class="sxs-lookup"><span data-stu-id="202f4-117">The primary difference is the main account that you select in the **Summary account** field.</span></span> <span data-ttu-id="202f4-118">Frekari upplýsingar eru í [Bókunarreglur viðskiptavina](customer-posting-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="202f4-118">For more information, see [Customer posting profiles](customer-posting-profiles.md).</span></span>

## <a name="define-parameters-for-customer-prepayments"></a><span data-ttu-id="202f4-119">Skilgreina færibreytur fyrir fyrirframgreiðslur viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="202f4-119">Define parameters for customer prepayments</span></span>

<span data-ttu-id="202f4-120">Hafa skal í huga tvær færibreytur aðallykils viðskiptakrafa þegar kerfið er stillt fyrir fyrirframgreiðslur viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="202f4-120">There are two main Accounts receivable parameters that you must consider when you configure the system for customer prepayments.</span></span> <span data-ttu-id="202f4-121">Fylgdu þessum skrefum til að grunnstilla færibreyturnar.</span><span class="sxs-lookup"><span data-stu-id="202f4-121">Follow these steps to configure the parameters.</span></span>

1. <span data-ttu-id="202f4-122">Opnið **Viðskiptakröfur \> Setja upp \> Færibreytur viðskiptakrafna**.</span><span class="sxs-lookup"><span data-stu-id="202f4-122">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="202f4-123">Valfrjálst: Í flipanum **Fjárhagur og virðisaukaskattur**, í flýtiflipanum **Greiðsla**, skal stilla valkostinn **VSK í fylgiskjali fyrirframgreiðslubókar** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="202f4-123">Optional: On the **Ledger and sales tax** tab, on the **Payment** FastTab, set the **Sales tax on prepayment journal voucher** option to **Yes**.</span></span>
3. <span data-ttu-id="202f4-124">Í reitnum **Bókunarregla með fylgiskjali fyrirframgreiðslubókar** skal velja bókunarreglu viðskiptavinar sem á að nota þegar fyrirframgreiðslur viðskiptavinar eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="202f4-124">In the **Posting profile with prepayment journal voucher** field, select the customer posting profile to use when customer prepayments are posted.</span></span>
4. <span data-ttu-id="202f4-125">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="202f4-125">Close the page.</span></span>

## <a name="create-customer-prepayment-vouchers"></a><span data-ttu-id="202f4-126">Stofna fylgiskjal fyrirframgreiðslu viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="202f4-126">Create customer prepayment vouchers</span></span>

<span data-ttu-id="202f4-127">Þegar greiðslubók viðskiptavinar er stofnuð þarf fyrir hverja fyrirframgreiðslu að stilla valkostinn **Fylgiskjal fyrirframgreiðslubókar** á **Já** á síðunni **Greiðslubók viðskiptavinar**.</span><span class="sxs-lookup"><span data-stu-id="202f4-127">When you create the customer payment journal, for every prepayment, you must set the **Prepayment journal voucher** option to **Yes** on the **Customer payment journal** page.</span></span> <span data-ttu-id="202f4-128">Fylgdu þessum skrefum til að búa til fyrirframgreiðslu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="202f4-128">Follow these steps to create a customer prepayment.</span></span>

1. <span data-ttu-id="202f4-129">Farið í **Viðskiptakröfur \> Greiðslur \> Greiðslubók viðskiptavinar**.</span><span class="sxs-lookup"><span data-stu-id="202f4-129">Go to **Accounts receivable \> Payments \> Customer payment journal**.</span></span>
2. <span data-ttu-id="202f4-130">Veljið **Ný** til að stofna færslubók.</span><span class="sxs-lookup"><span data-stu-id="202f4-130">Select **New** to create a journal.</span></span>
3. <span data-ttu-id="202f4-131">Í reitnum **Heiti** skal velja færslubókina sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="202f4-131">In the **Name** field, select the journal name to use.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="202f4-132">Ef valkosturinn **VSK í fylgiskjali fyrirframgreiðslubókar** er stilltur á **Já** í fyrra ferlinu, þarf að velja heiti færslubókar þar sem færibreytan **Upphæð með virðisaukaskatti** er valin.</span><span class="sxs-lookup"><span data-stu-id="202f4-132">If you set the **Sales tax on prepayment journal voucher** option to **Yes** in the previous procedure, you must select a journal name where the **Amount includes sales tax** parameter is selected.</span></span> 

4. <span data-ttu-id="202f4-133">Valfrjálst: Í reitinn **Lýsing** skal færa inn nákvæma lýsingu.</span><span class="sxs-lookup"><span data-stu-id="202f4-133">Optional: In the **Description** field, enter a detailed description.</span></span>
5. <span data-ttu-id="202f4-134">Veldu **Línur**.</span><span class="sxs-lookup"><span data-stu-id="202f4-134">Select **Lines**.</span></span>
6. <span data-ttu-id="202f4-135">Ef auð lína er ekki til skal velja **Ný** til að stofna línu.</span><span class="sxs-lookup"><span data-stu-id="202f4-135">If a blank line doesn't exist, select **New** to create a line.</span></span>
7. <span data-ttu-id="202f4-136">Í reitinn **Dagsetning** skal færa inn dagsetninguna þegar bóka á fyrirframgreiðsluna.</span><span class="sxs-lookup"><span data-stu-id="202f4-136">In the **Date** field, enter the date when the prepayment should be posted.</span></span>
8. <span data-ttu-id="202f4-137">Í reitinn **Lykill** skal velja viðskiptavin fyrirframgreiðslunnar.</span><span class="sxs-lookup"><span data-stu-id="202f4-137">In the **Account** field, select the customer for the prepayment.</span></span>
9. <span data-ttu-id="202f4-138">Valfrjálst: Í reitinn **Lýsing** skal færa inn nákvæma lýsingu á færslunni.</span><span class="sxs-lookup"><span data-stu-id="202f4-138">Optional: In the **Description** field, enter a detailed description of the transaction.</span></span>
10. <span data-ttu-id="202f4-139">Í reitinn **Kredit** skal færa inn upphæð fyrirframgreiðslunnar.</span><span class="sxs-lookup"><span data-stu-id="202f4-139">In the **Credit** field, enter the amount of the prepayment.</span></span>
11. <span data-ttu-id="202f4-140">Í reitnum **Mótlykill** skal velja lykilinn til að jafna við greiðsluna.</span><span class="sxs-lookup"><span data-stu-id="202f4-140">In the **Offset account** field, select the account to offset the payment to.</span></span> <span data-ttu-id="202f4-141">Veljið til að mynda bankann eða aðallykilinn til að bóka greiðsluna á.</span><span class="sxs-lookup"><span data-stu-id="202f4-141">For example, select the bank or main account to post the payment to.</span></span>
12. <span data-ttu-id="202f4-142">Í reitnum **Greiðslumáti** skal velja greiðslumáta viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="202f4-142">In the **Method of payment** field, select the customer's method of payment.</span></span>
13. <span data-ttu-id="202f4-143">Í flipanum **Greiðsla** skal stilla valkostinn **Fylgiskjal fyrirframgreiðslubókar** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="202f4-143">On the **Payment** tab, set the **Prepayment journal voucher** option to **Yes**.</span></span>
14. <span data-ttu-id="202f4-144">Endurtakið skref 7 til 13 fyrir hverja fyrirframgreiðslu til viðbótar sem þarf að bóka.</span><span class="sxs-lookup"><span data-stu-id="202f4-144">Repeat steps 7 through 13 for each additional prepayment that must be posted.</span></span>
15. <span data-ttu-id="202f4-145">Veljið **Bóka** til að ganga frá færslubókinni.</span><span class="sxs-lookup"><span data-stu-id="202f4-145">Select **Post** to finalize the journal.</span></span>

## <a name="settle-prepayments-with-invoices"></a><span data-ttu-id="202f4-146">Jafna fyrirframgreiðslur með reikningum</span><span class="sxs-lookup"><span data-stu-id="202f4-146">Settle prepayments with invoices</span></span>

<span data-ttu-id="202f4-147">Hægt er að nota vinnusvæðið **Greiðslur viðskiptavinar** til að finna og jafna greiðslur sem hafa ekki verið jafnaðar að fullu á auðveldan hátt.</span><span class="sxs-lookup"><span data-stu-id="202f4-147">You can use the **Customer payments** workspace to easily find and settle payments that haven't been fully settled.</span></span>

1. <span data-ttu-id="202f4-148">Í yfirlitinu **Heim** skal velja reitinn **Greiðslur viðskiptavinar**.</span><span class="sxs-lookup"><span data-stu-id="202f4-148">On the **Home** dashboard, select the **Customer payments** tile.</span></span>
2. <span data-ttu-id="202f4-149">Í hlutanum **Færslur viðskiptavinar**, í flipanum **Ójafnaðar greiðslur**, skal leita að og velja greiðslu til að jafna.</span><span class="sxs-lookup"><span data-stu-id="202f4-149">In the **Customer transactions** section, on the **Payments not settled** tab, search for and select the payment to settle.</span></span>
3. <span data-ttu-id="202f4-150">Smellt er á **Jafna færslur**.</span><span class="sxs-lookup"><span data-stu-id="202f4-150">Select **Settle transactions**.</span></span>
4. <span data-ttu-id="202f4-151">Veljið gátreitinn **Merkja** fyrir reikninginn og greiðsluna sem verða jöfnuð.</span><span class="sxs-lookup"><span data-stu-id="202f4-151">Select the **Mark** check box for the invoice and the payment that will be settled.</span></span>
5. <span data-ttu-id="202f4-152">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="202f4-152">Select **Post**.</span></span>

<span data-ttu-id="202f4-153">Frekari upplýsingar um hvernig á að jafna opnar færslur er að finna í [Yfirlit jöfnunar](/cash-bank-management/settlement-overview.md).</span><span class="sxs-lookup"><span data-stu-id="202f4-153">For more information about how to settle open transactions, see [Settlement overview](/cash-bank-management/settlement-overview.md).</span></span>
