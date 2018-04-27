---
title: "Greiðslur lánardrottna fyrir hlutaupphæð"
description: "Stundum þarf að framkvæma greiðslu til lánardrottins sem er minni en upphæð reiknings. Þessi grein lýsir mismunandi valkostum til að meðhöndla þær aðstæður. Valkostirnir sem eru tiltækir fyrir þig fara eftir viðskiptaþörfum og skilgreiningum fyrirtækisins."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: aeef806980665c523f10b373f7662ecf509a8172
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="vendor-payments-for-a-partial-amount"></a><span data-ttu-id="855eb-105">Greiðslur lánardrottna fyrir hlutaupphæð</span><span class="sxs-lookup"><span data-stu-id="855eb-105">Vendor payments for a partial amount</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="855eb-106">Stundum þarf að framkvæma greiðslu til lánardrottins sem er minni en upphæð reiknings.</span><span class="sxs-lookup"><span data-stu-id="855eb-106">Sometimes, you might make a payment to a vendor that is less than the amount of an invoice.</span></span> <span data-ttu-id="855eb-107">Þessi grein lýsir mismunandi valkostum til að meðhöndla þær aðstæður.</span><span class="sxs-lookup"><span data-stu-id="855eb-107">This article describes the various options for handling this situation.</span></span> <span data-ttu-id="855eb-108">Valkostirnir sem eru tiltækir fyrir þig fara eftir viðskiptaþörfum og skilgreiningum fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="855eb-108">The options that are available to you depend on your business requirements and configuration.</span></span> 

<a name="cash-discount-amounts"></a><span data-ttu-id="855eb-109">Upphæðir staðgreiðsluafsláttar</span><span class="sxs-lookup"><span data-stu-id="855eb-109">Cash discount amounts</span></span>
---------------------

<span data-ttu-id="855eb-110">Lánardrottinn getur boðið þér staðgreiðsluafslátt fyrir greiðslu á reikning fyrir gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="855eb-110">A vendor can offer you a cash discount for paying an invoice before the due date.</span></span> <span data-ttu-id="855eb-111">Til dæmis færður er inn reikningur fyrir 100,00 sem tilgreinir 2 prósent staðgreiðsluafslátt ef reikningurinn er greiddur innan 10 daga.</span><span class="sxs-lookup"><span data-stu-id="855eb-111">For example, you enter an invoice for 100.00 that specifies a 2-percent cash discount if the invoice is paid within 10 days.</span></span> <span data-ttu-id="855eb-112">Skilmálar gjalddaga eru 30 dagar.</span><span class="sxs-lookup"><span data-stu-id="855eb-112">The due date terms are 30 days.</span></span> <span data-ttu-id="855eb-113">Ef greiðslutillaga notar staðgreiðsluafslátt sem skilyrði fyrir því að velja reikning og ef tillagan er keyrð á eða á undan dagsetningu staðgreiðsluafsláttar er reikningurinn valinn til greiðslu og greiðsla er stofnuð fyrir 98,00.</span><span class="sxs-lookup"><span data-stu-id="855eb-113">If a payment proposal uses the cash discount as a criterion for selecting an invoice, and if the proposal is run on or before the cash discount date, the invoice is selected for payment, and the payment is created for 98.00.</span></span> <span data-ttu-id="855eb-114">Einnig er hægt að taka staðgreiðsluafslátt fyrir eingreiðslu sem var stofnuð handvirkt.</span><span class="sxs-lookup"><span data-stu-id="855eb-114">A cash discount can also be taken for a one-off payment that was created manually.</span></span>

## <a name="partial-payments-with-cash-discounts"></a><span data-ttu-id="855eb-115">hlutagreiðslur með staðgreiðsluafslætti</span><span class="sxs-lookup"><span data-stu-id="855eb-115">Partial payments with cash discounts</span></span>
<span data-ttu-id="855eb-116">Þegar þú reiðir fram hlutagreiðslu gætiðu gert áætlun um að gera frekari hlutagreiðslu til að jafna reikninginn að fullu.</span><span class="sxs-lookup"><span data-stu-id="855eb-116">When you make a partial payment, you might plan to make an additional partial payment to fully settle the invoice.</span></span> <span data-ttu-id="855eb-117">Til að taka staðgreiðsluafslátt fyrir hlutagreiðslu, verður að stilla <strong>**valkostinn Reikna staðgreiðsluafslætti fyrir hlutagreiðslur á **Já</strong> á síðunni <strong>Færibreytur viðskiptaskulda</strong>.</span><span class="sxs-lookup"><span data-stu-id="855eb-117">To take a cash discount for a partial payment, you must set the <strong>Calculate cash discounts for partial payments **option to **Yes</strong> on the <strong>Account payable parameters</strong> page.</span></span> 

<span data-ttu-id="855eb-118">Til dæmis færðu 2 prósent staðgreiðsluafslátt ef reikningurinn er greiddur innan 10 daga eftir það hann er gefinn út.</span><span class="sxs-lookup"><span data-stu-id="855eb-118">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="855eb-119">Bókaður er reikningur fyrir 100,00.</span><span class="sxs-lookup"><span data-stu-id="855eb-119">An invoice is posted for 100.00.</span></span> <span data-ttu-id="855eb-120">Ef greitt er 49,00 innan 10 daga er fært inn debet uppá 49,00 í greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="855eb-120">If you make a payment of 49.00 within 10 days, you enter a debit of 49.00 in a payment journal.</span></span> <span data-ttu-id="855eb-121">Þegar hlutagreiðsla er jöfnuð á síðunni **Jafna opnar færslur** birtist **1,00** í svæðinu **upphæð staðgreiðsluafsláttar sem á að taka**.</span><span class="sxs-lookup"><span data-stu-id="855eb-121">When you settle the partial payment on the **Settle open transactions** page, **1.00** appears in the **Cash discount amount to take** field.</span></span> 

> [!NOTE] 
> <span data-ttu-id="855eb-122">Ef hlutagreiðsla er færð inn og full reikningsupphæð er látin vera í reitnum **Upphæðin til jöfnunar** er **upphæð staðgreiðsluafsláttar sem á að taka** svæði sjálfkrafa endurreiknað þegar þú bókar færslur.</span><span class="sxs-lookup"><span data-stu-id="855eb-122">If you enter a partial payment and leave the full invoice amount in the **Amount to settle** field, the **Cash discount amount to take** field is automatically recalculated when you post the transactions.</span></span>

## <a name="credit-notes-with-cash-discounts"></a><span data-ttu-id="855eb-123">Kreditnótur með staðgreiðsluafslætti</span><span class="sxs-lookup"><span data-stu-id="855eb-123">Credit notes with cash discounts</span></span>
<span data-ttu-id="855eb-124">Þú gætir skilað sumum af vörunum á reikningi og fengið kreditnótu.</span><span class="sxs-lookup"><span data-stu-id="855eb-124">You might return some of the items on an invoice and receive a credit note.</span></span> <span data-ttu-id="855eb-125">Ef staðgreiðsluafsláttur var tekinn á upphaflega reikningnum er hægt að draga virði afsláttar og fá endurgreiðslu fyrir rétta upphæð.</span><span class="sxs-lookup"><span data-stu-id="855eb-125">If a cash discount was taken on the original invoice, you can subtract the value of the discount and receive a refund for the correct amount.</span></span> <span data-ttu-id="855eb-126">Ef <strong>**valkosturinn Reikna staðgreiðsluafslátt fyrir kreditnótur er stilltur á **Já</strong> á síðunni <strong>Færibreytur viðskiptaskulda</strong>, er afslátturinn sjálfkrafa reiknaður út fyrir kreditnótu.</span><span class="sxs-lookup"><span data-stu-id="855eb-126">If the <strong>Calculate cash discounts for credit notes **option is set to **Yes</strong> on the <strong>Accounts payable parameters</strong> page, the discount is automatically calculated for the credit note.</span></span> 

<span data-ttu-id="855eb-127">Til dæmis færðu 2 prósent staðgreiðsluafslátt ef reikningurinn er greiddur innan 10 daga eftir það hann er gefinn út.</span><span class="sxs-lookup"><span data-stu-id="855eb-127">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="855eb-128">Bókaður er reikningur fyrir 100,00.</span><span class="sxs-lookup"><span data-stu-id="855eb-128">An invoice for 100.00 is posted.</span></span> <span data-ttu-id="855eb-129">Ef þú skilar vörunum og færð kreditnótu geturðu fært inn kreditnótu fyrir fulla upphæð upprunalegs reiknings, 100,00, ásamt 2 prósent staðgreiðsluafslætti sem er einnig skilgreindur í kreditnótunni.</span><span class="sxs-lookup"><span data-stu-id="855eb-129">If you return the goods and receive a credit note, you can enter the credit note for the full amount of the original invoice, 100.00, together with the 2-percent cash discount that is also defined on the credit memo.</span></span>  <span data-ttu-id="855eb-130">Þegar kreditnótan er skoðuð á **Jafna færslur** síðu birtist **98.00** í svæðinu **Upphæðin til jöfnunar** og **-2,00** birtist í á **upphæð staðgreiðsluafsláttar** svæði.</span><span class="sxs-lookup"><span data-stu-id="855eb-130">When you view the credit note on the **Settle transactions** page, **98.00** appears in the **Amount to settle** field, and **-2.00** appears in the **Cash discount amount** field.</span></span> <span data-ttu-id="855eb-131">Afsláttarupphæðin er bókuð á lykil fyrir staðgreiðsluafslátt.</span><span class="sxs-lookup"><span data-stu-id="855eb-131">The discount amount is posted to a cash discount account.</span></span>

## <a name="overpaymentunderpayment-amounts"></a><span data-ttu-id="855eb-132">Upphæðir ofgreiðslu eða vangreiðslu</span><span class="sxs-lookup"><span data-stu-id="855eb-132">Overpayment/underpayment amounts</span></span>
<span data-ttu-id="855eb-133">Þú getur reitt fram hlutagreiðslu þar sem upphæðin sem þarf að jafna er mjög lág.</span><span class="sxs-lookup"><span data-stu-id="855eb-133">You might make a partial payment where the amount that must still be settled is very small.</span></span> <span data-ttu-id="855eb-134">Til dæmis, reikningur lánardrottins er upp á 1.000,00 og þú greiðir 999,90.</span><span class="sxs-lookup"><span data-stu-id="855eb-134">For example, the vendor invoice is for 1,000.00, and you pay 999.90.</span></span> <span data-ttu-id="855eb-135">Ef eftirstandandi upphæð er lægri en upphæðin sem er tilgreind fyrir ofgreiðslu eða vangreiðslu á síðunni **Færibreytur viðskiptaskulda** er mismunur sjálfkrafa bókaður í fjárhagslykil ofgreiðslu/vangreiðslu.</span><span class="sxs-lookup"><span data-stu-id="855eb-135">If the remaining amount is less than the amount that is specified for overpayments or underpayments on the **Accounts payable parameters** page, the difference is automatically posted to an overpayment/underpayment ledger account.</span></span>


<span data-ttu-id="855eb-136">Frekari upplýsingar eru í [Yfirlit greiðslur lánardrottins](../cash-bank-management/tasks/vendor-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="855eb-136">For more information, see [Vendor payment overview](../cash-bank-management/tasks/vendor-payment-overview.md).</span></span>

