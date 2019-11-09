---
title: Jafna hlutagreiðslu viðskiptavinar fyrir afsláttardagsetninguna með lokagreiðslu eftir afsláttardagsetninguna
description: Þessi grein fer yfir áhrif þess að jafna greiðslur á reikninga fyrir viðskiptavini. Aðstæðurnar einblína á áhrifin í undirbókinni, ekki í Fjárhagnum.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14584
ms.assetid: e54936f5-053b-4ed3-b778-42c7e9aeb7cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a71d0931445f3501f1b74f26c5eef583ab598b3c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2188902"
---
# <a name="settle-a-partial-customer-payment-before-the-discount-date-with-a-final-payment-after-the-discount-date"></a><span data-ttu-id="d8fa9-104">Jafna hlutagreiðslu viðskiptavinar fyrir afsláttardagsetninguna með lokagreiðslu eftir afsláttardagsetninguna</span><span class="sxs-lookup"><span data-stu-id="d8fa9-104">Settle a partial customer payment before the discount date with a final payment after the discount date</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8fa9-105">Þessi grein fer yfir áhrif þess að jafna greiðslur á reikninga fyrir viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-105">This article discusses the effect of settling payments to invoices for customers.</span></span> <span data-ttu-id="d8fa9-106">Aðstæðurnar einblína á áhrifin í undirbókinni, ekki í Fjárhagnum.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-106">The scenario focuses on the effects in the subledger, not in General ledger.</span></span>

<span data-ttu-id="d8fa9-107">Fabrikam selur vörurn til 4027 viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-107">Fabrikam sells goods to customer 4027.</span></span> <span data-ttu-id="d8fa9-108">Fabrikam býður 1 prósent afslátt ef reikningurinn er greiddur innan 14 daga.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-108">Fabrikam offers a cash discount of 1 percent if the invoice is paid in 14 days.</span></span> <span data-ttu-id="d8fa9-109">Greiða þarf reikninga eftir 30 daga.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-109">Invoices must be paid in 30 days.</span></span> <span data-ttu-id="d8fa9-110">Fabrikam býður einnig upp á staðgreiðsluafslætti fyrir hlutagreiðslur.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-110">Fabrikam also offers cash discounts on partial payments.</span></span> <span data-ttu-id="d8fa9-111">Uppgjörsfæribreytur eru staðsettar á síðunni **Færibreytur viðskiptakrafna**.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-111">The settlement parameters are located on the **Accounts receivable parameters** page.</span></span>

## <a name="invoice"></a><span data-ttu-id="d8fa9-112">Reikningur</span><span class="sxs-lookup"><span data-stu-id="d8fa9-112">Invoice</span></span>
<span data-ttu-id="d8fa9-113">25. júní færir Apríl inn og bókar reikning uppá 1.000,00 fyrir viðskiptamann 4027.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-113">On June 25, Arnie enters and posts an invoice for 1,000.00 for customer 4027.</span></span> <span data-ttu-id="d8fa9-114">Arnie getur skoðað þennan reikning með því að nota hnappinn **Færslur** á síðunni **Viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-114">Arnie can view this invoice by using the **Transactions** button on the **Customers** page.</span></span>

| <span data-ttu-id="d8fa9-115">Fylgiskjal</span><span class="sxs-lookup"><span data-stu-id="d8fa9-115">Voucher</span></span>   | <span data-ttu-id="d8fa9-116">Færslugerð</span><span class="sxs-lookup"><span data-stu-id="d8fa9-116">Transaction type</span></span> | <span data-ttu-id="d8fa9-117">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="d8fa9-117">Date</span></span>      | <span data-ttu-id="d8fa9-118">Reikningur</span><span class="sxs-lookup"><span data-stu-id="d8fa9-118">Invoice</span></span> | <span data-ttu-id="d8fa9-119">Upphæð í færslugjaldmiðli - debet</span><span class="sxs-lookup"><span data-stu-id="d8fa9-119">Amount in transaction currency debit</span></span> | <span data-ttu-id="d8fa9-120">Upphæð í færslugjaldmiðli - kredit</span><span class="sxs-lookup"><span data-stu-id="d8fa9-120">Amount in transaction currency credit</span></span> | <span data-ttu-id="d8fa9-121">Staða</span><span class="sxs-lookup"><span data-stu-id="d8fa9-121">Balance</span></span>  | <span data-ttu-id="d8fa9-122">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d8fa9-122">Currency</span></span> |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| <span data-ttu-id="d8fa9-123">FTI-10020</span><span class="sxs-lookup"><span data-stu-id="d8fa9-123">FTI-10020</span></span> | <span data-ttu-id="d8fa9-124">Reikningur</span><span class="sxs-lookup"><span data-stu-id="d8fa9-124">Invoice</span></span>          | <span data-ttu-id="d8fa9-125">6/25/2015</span><span class="sxs-lookup"><span data-stu-id="d8fa9-125">6/25/2015</span></span> | <span data-ttu-id="d8fa9-126">10020</span><span class="sxs-lookup"><span data-stu-id="d8fa9-126">10020</span></span>   | <span data-ttu-id="d8fa9-127">1.000,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-127">1,000.00</span></span>                             |                                       | <span data-ttu-id="d8fa9-128">1.000,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-128">1,000.00</span></span> | <span data-ttu-id="d8fa9-129">USD</span><span class="sxs-lookup"><span data-stu-id="d8fa9-129">USD</span></span>      |

## <a name="partial-payment-before-the-cash-discount-date"></a><span data-ttu-id="d8fa9-130">hlutagreiðsla fyrir dagsetningu staðgreiðsluafsláttar</span><span class="sxs-lookup"><span data-stu-id="d8fa9-130">Partial payment before the cash discount date</span></span>
<span data-ttu-id="d8fa9-131">2. júlí gerir viðskiptavinar 4027 hlutagreiðslu upp á 297.00 fyrir reikninginn.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-131">On July 2, customer 4027 makes a partial payment of 297.00 for the invoice.</span></span> <span data-ttu-id="d8fa9-132">Greiðslan gefur rétt á afslætti, þar sem Fabrikam býður afslátt á hlutagreiðslur og hlutagreiðslan er gerð á undan dagsetningu staðgreiðsluafsláttar.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-132">The payment is eligible for a cash discount, because Fabrikam offers cash discounts on partial payments, and the partial payment is made before the cash discount date.</span></span> <span data-ttu-id="d8fa9-133">Þess vegna fær viðskiptavinar 4027 3,00 í staðgreiðsluafslátt.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-133">Therefore, customer 4027 takes a 3.00 cash discount.</span></span> <span data-ttu-id="d8fa9-134">Arnie skráir greiðslu fyrir viðskiptavin 4027 með því að nota greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-134">Arnie records the payment for customer 4027 by using the Payment journal.</span></span> <span data-ttu-id="d8fa9-135">Síðan opnar Arnie síðuna **Jafna færslur** svo að hann geti merkt reikninginn fyrir jöfnun.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-135">Arnie then opens the **Settle transactions** page, so that he can mark the invoice for settlement.</span></span>

| <span data-ttu-id="d8fa9-136">Merkja</span><span class="sxs-lookup"><span data-stu-id="d8fa9-136">Mark</span></span>     | <span data-ttu-id="d8fa9-137">Nota staðgreiðsluafslátt</span><span class="sxs-lookup"><span data-stu-id="d8fa9-137">Use cash discount</span></span> | <span data-ttu-id="d8fa9-138">Fylgiskjal</span><span class="sxs-lookup"><span data-stu-id="d8fa9-138">Voucher</span></span>   | <span data-ttu-id="d8fa9-139">Reikningur</span><span class="sxs-lookup"><span data-stu-id="d8fa9-139">Account</span></span> | <span data-ttu-id="d8fa9-140">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="d8fa9-140">Date</span></span>      | <span data-ttu-id="d8fa9-141">Gjalddagi</span><span class="sxs-lookup"><span data-stu-id="d8fa9-141">Due date</span></span>  | <span data-ttu-id="d8fa9-142">Reikningur</span><span class="sxs-lookup"><span data-stu-id="d8fa9-142">Invoice</span></span> | <span data-ttu-id="d8fa9-143">Upphæð í færslugjaldmiðli - debet</span><span class="sxs-lookup"><span data-stu-id="d8fa9-143">Amount in transaction currency debit</span></span> | <span data-ttu-id="d8fa9-144">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d8fa9-144">Currency</span></span> | <span data-ttu-id="d8fa9-145">Upphæð til jöfnunar</span><span class="sxs-lookup"><span data-stu-id="d8fa9-145">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| <span data-ttu-id="d8fa9-146">Valið</span><span class="sxs-lookup"><span data-stu-id="d8fa9-146">Selected</span></span> | <span data-ttu-id="d8fa9-147">Venjulegt</span><span class="sxs-lookup"><span data-stu-id="d8fa9-147">Normal</span></span>            | <span data-ttu-id="d8fa9-148">FTI-10020</span><span class="sxs-lookup"><span data-stu-id="d8fa9-148">FTI-10020</span></span> | <span data-ttu-id="d8fa9-149">4027</span><span class="sxs-lookup"><span data-stu-id="d8fa9-149">4027</span></span>    | <span data-ttu-id="d8fa9-150">6/25/2015</span><span class="sxs-lookup"><span data-stu-id="d8fa9-150">6/25/2015</span></span> | <span data-ttu-id="d8fa9-151">7/25/2015</span><span class="sxs-lookup"><span data-stu-id="d8fa9-151">7/25/2015</span></span> | <span data-ttu-id="d8fa9-152">10020</span><span class="sxs-lookup"><span data-stu-id="d8fa9-152">10020</span></span>   | <span data-ttu-id="d8fa9-153">1.000,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-153">1,000.00</span></span>                             | <span data-ttu-id="d8fa9-154">USD</span><span class="sxs-lookup"><span data-stu-id="d8fa9-154">USD</span></span>      | <span data-ttu-id="d8fa9-155">297,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-155">297.00</span></span>           |

<span data-ttu-id="d8fa9-156">Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-156">Discount information appears at the bottom of the **Settle open transactions** page.</span></span> <span data-ttu-id="d8fa9-157">Ef gildinu í **Upphæðin til jöfnunar** er ekki breytt í 297.00 verða gildin fyrir **Upphæð staðgreiðsluafsláttar** sem birtast vera mismunandi.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-157">If you don't change the **Amount to settle** value to 297.00, the **Cash discount amount** values that appear will differ.</span></span> <span data-ttu-id="d8fa9-158">Hins vegar verður 3,00 notað sem staðgreiðsluafsláttur þegar greiðslan er bókuð, þar sem jöfnun leiðréttir sjálfkrafa gildið **Upphæð til jöfnunar** fyrir þig.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-158">However, 3.00 will be taken as the cash discount when the payment is posted, because settlement automatically adjusts the \*\*Amount to settle \*\*value for you.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="d8fa9-159">Dagsetning staðgreiðsluafsláttar</span><span class="sxs-lookup"><span data-stu-id="d8fa9-159">Cash discount date</span></span>           | <span data-ttu-id="d8fa9-160">7/09/2015</span><span class="sxs-lookup"><span data-stu-id="d8fa9-160">7/09/2015</span></span> |
| <span data-ttu-id="d8fa9-161">Upphæð staðgreiðsluafsláttar</span><span class="sxs-lookup"><span data-stu-id="d8fa9-161">Cash discount amount</span></span>         | <span data-ttu-id="d8fa9-162">10,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-162">10.00</span></span>     |
| <span data-ttu-id="d8fa9-163">Nota staðgreiðsluafslátt</span><span class="sxs-lookup"><span data-stu-id="d8fa9-163">Use cash discount</span></span>            | <span data-ttu-id="d8fa9-164">Venjulegt</span><span class="sxs-lookup"><span data-stu-id="d8fa9-164">Normal</span></span>    |
| <span data-ttu-id="d8fa9-165">Notaður staðgreiðsluafsláttur</span><span class="sxs-lookup"><span data-stu-id="d8fa9-165">Cash discount taken</span></span>          | <span data-ttu-id="d8fa9-166">0,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-166">0.00</span></span>      |
| <span data-ttu-id="d8fa9-167">Upphæð staðgreiðsluafsláttar sem á að veita</span><span class="sxs-lookup"><span data-stu-id="d8fa9-167">Cash discount amount to take</span></span> | <span data-ttu-id="d8fa9-168">3,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-168">3.00</span></span>      |

<span data-ttu-id="d8fa9-169">Arnie bókar þessa greiðslu.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-169">Arnie posts this payment.</span></span> <span data-ttu-id="d8fa9-170">Reikningurinn hefur núna stöðuna 700,00.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-170">The invoice now has a balance of 700.00.</span></span> <span data-ttu-id="d8fa9-171">Hægt er að sjá eftirfarandi færslur fyrir viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-171">The following transactions can be seen for the customer.</span></span>

| <span data-ttu-id="d8fa9-172">Fylgiskjal</span><span class="sxs-lookup"><span data-stu-id="d8fa9-172">Voucher</span></span>    | <span data-ttu-id="d8fa9-173">Færslugerð</span><span class="sxs-lookup"><span data-stu-id="d8fa9-173">Transaction type</span></span> | <span data-ttu-id="d8fa9-174">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="d8fa9-174">Date</span></span>      | <span data-ttu-id="d8fa9-175">Reikningur</span><span class="sxs-lookup"><span data-stu-id="d8fa9-175">Invoice</span></span> | <span data-ttu-id="d8fa9-176">Upphæð í færslugjaldmiðli - debet</span><span class="sxs-lookup"><span data-stu-id="d8fa9-176">Amount in transaction currency debit</span></span> | <span data-ttu-id="d8fa9-177">Upphæð í færslugjaldmiðli - kredit</span><span class="sxs-lookup"><span data-stu-id="d8fa9-177">Amount in transaction currency credit</span></span> | <span data-ttu-id="d8fa9-178">Staða</span><span class="sxs-lookup"><span data-stu-id="d8fa9-178">Balance</span></span> | <span data-ttu-id="d8fa9-179">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d8fa9-179">Currency</span></span> |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| <span data-ttu-id="d8fa9-180">FTI-10020</span><span class="sxs-lookup"><span data-stu-id="d8fa9-180">FTI-10020</span></span>  | <span data-ttu-id="d8fa9-181">Reikningur</span><span class="sxs-lookup"><span data-stu-id="d8fa9-181">Invoice</span></span>          | <span data-ttu-id="d8fa9-182">6/25/2015</span><span class="sxs-lookup"><span data-stu-id="d8fa9-182">6/25/2015</span></span> | <span data-ttu-id="d8fa9-183">10020</span><span class="sxs-lookup"><span data-stu-id="d8fa9-183">10020</span></span>   | <span data-ttu-id="d8fa9-184">1.000,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-184">1,000.00</span></span>                             |                                       | <span data-ttu-id="d8fa9-185">700.00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-185">700.00</span></span>  | <span data-ttu-id="d8fa9-186">USD</span><span class="sxs-lookup"><span data-stu-id="d8fa9-186">USD</span></span>      |
| <span data-ttu-id="d8fa9-187">ARP-10020</span><span class="sxs-lookup"><span data-stu-id="d8fa9-187">ARP-10020</span></span>  |  <span data-ttu-id="d8fa9-188">Greiðsla</span><span class="sxs-lookup"><span data-stu-id="d8fa9-188">Payment</span></span>         | <span data-ttu-id="d8fa9-189">7/1/2015</span><span class="sxs-lookup"><span data-stu-id="d8fa9-189">7/1/2015</span></span>  |         |                                      | <span data-ttu-id="d8fa9-190">297,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-190">297.00</span></span>                                | <span data-ttu-id="d8fa9-191">0,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-191">0.00</span></span>    | <span data-ttu-id="d8fa9-192">USD</span><span class="sxs-lookup"><span data-stu-id="d8fa9-192">USD</span></span>      |
| <span data-ttu-id="d8fa9-193">DISC-10020</span><span class="sxs-lookup"><span data-stu-id="d8fa9-193">DISC-10020</span></span> |  <span data-ttu-id="d8fa9-194">Staðgreiðsluafsláttur</span><span class="sxs-lookup"><span data-stu-id="d8fa9-194">Cash discount</span></span>   | <span data-ttu-id="d8fa9-195">7/1/2015</span><span class="sxs-lookup"><span data-stu-id="d8fa9-195">7/1/2015</span></span>  |         |                                      | <span data-ttu-id="d8fa9-196">3,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-196">3.00</span></span>                                  | <span data-ttu-id="d8fa9-197">0,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-197">0.00</span></span>    | <span data-ttu-id="d8fa9-198">USD</span><span class="sxs-lookup"><span data-stu-id="d8fa9-198">USD</span></span>      |

## <a name="remaining-payment-after-the-cash-discount-date"></a><span data-ttu-id="d8fa9-199">Eftirstandandi greiðsla eftir dagsetningu staðgreiðsluafsláttar</span><span class="sxs-lookup"><span data-stu-id="d8fa9-199">Remaining payment after the cash discount date</span></span>
<span data-ttu-id="d8fa9-200">Þann 11. júlí, sem er eftir afsláttartímabilið, greiðir viðskiptavinur 4027 afganginn af reikningnum.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-200">On July 11, which is after the discount period, customer 4027 pays the rest of this invoice.</span></span> <span data-ttu-id="d8fa9-201">Á síðunni **Jafna opnar færslur** birtist afsláttarupphæð ekki í reitnum **Áætlaður staðgreiðsluafsláttur** og gildið í reitnum **Upphæð staðgreiðsluafsláttar** er **0,00**.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-201">On the **Settle transactions** page, a discount amount doesn't appear in the **Estimated cash discount** field, and the value in the **Cash discount amount** field is **0.00**.</span></span> <span data-ttu-id="d8fa9-202">Þegar viðskiptavinur 4027 greiðir eftirstandandi 700,00 verður ekki veittur frekari afsláttur.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-202">When customer 4027 pays the remaining 700.00, no additional discount is taken.</span></span>

| <span data-ttu-id="d8fa9-203">Merkja</span><span class="sxs-lookup"><span data-stu-id="d8fa9-203">Mark</span></span>     | <span data-ttu-id="d8fa9-204">Nota staðgreiðsluafslátt</span><span class="sxs-lookup"><span data-stu-id="d8fa9-204">Use cash discount</span></span> | <span data-ttu-id="d8fa9-205">Fylgiskjal</span><span class="sxs-lookup"><span data-stu-id="d8fa9-205">Voucher</span></span>   | <span data-ttu-id="d8fa9-206">Reikningur</span><span class="sxs-lookup"><span data-stu-id="d8fa9-206">Account</span></span> | <span data-ttu-id="d8fa9-207">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="d8fa9-207">Date</span></span>      | <span data-ttu-id="d8fa9-208">Gjalddagi</span><span class="sxs-lookup"><span data-stu-id="d8fa9-208">Due date</span></span>  | <span data-ttu-id="d8fa9-209">Reikningur</span><span class="sxs-lookup"><span data-stu-id="d8fa9-209">Invoice</span></span> | <span data-ttu-id="d8fa9-210">Upphæð í færslugjaldmiðli - debet</span><span class="sxs-lookup"><span data-stu-id="d8fa9-210">Amount in transaction currency debit</span></span> | <span data-ttu-id="d8fa9-211">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d8fa9-211">Currency</span></span> | <span data-ttu-id="d8fa9-212">Upphæð til jöfnunar</span><span class="sxs-lookup"><span data-stu-id="d8fa9-212">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| <span data-ttu-id="d8fa9-213">Valið</span><span class="sxs-lookup"><span data-stu-id="d8fa9-213">Selected</span></span> | <span data-ttu-id="d8fa9-214">Venjulegt</span><span class="sxs-lookup"><span data-stu-id="d8fa9-214">Normal</span></span>            | <span data-ttu-id="d8fa9-215">FTI-10020</span><span class="sxs-lookup"><span data-stu-id="d8fa9-215">FTI-10020</span></span> | <span data-ttu-id="d8fa9-216">4027</span><span class="sxs-lookup"><span data-stu-id="d8fa9-216">4027</span></span>    | <span data-ttu-id="d8fa9-217">6/25/2015</span><span class="sxs-lookup"><span data-stu-id="d8fa9-217">6/25/2015</span></span> | <span data-ttu-id="d8fa9-218">7/25/2015</span><span class="sxs-lookup"><span data-stu-id="d8fa9-218">7/25/2015</span></span> | <span data-ttu-id="d8fa9-219">10020</span><span class="sxs-lookup"><span data-stu-id="d8fa9-219">10020</span></span>   | <span data-ttu-id="d8fa9-220">700.00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-220">700.00</span></span>                               | <span data-ttu-id="d8fa9-221">USD</span><span class="sxs-lookup"><span data-stu-id="d8fa9-221">USD</span></span>      | <span data-ttu-id="d8fa9-222">700.00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-222">700.00</span></span>           |

<span data-ttu-id="d8fa9-223">Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-223">Discount information appears at the bottom of the **Settle open transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="d8fa9-224">Dagsetning staðgreiðsluafsláttar</span><span class="sxs-lookup"><span data-stu-id="d8fa9-224">Cash discount date</span></span>           | <span data-ttu-id="d8fa9-225">7/09/2015</span><span class="sxs-lookup"><span data-stu-id="d8fa9-225">7/09/2015</span></span> |
| <span data-ttu-id="d8fa9-226">Upphæð staðgreiðsluafsláttar</span><span class="sxs-lookup"><span data-stu-id="d8fa9-226">Cash discount amount</span></span>         | <span data-ttu-id="d8fa9-227">0,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-227">0.00</span></span>      |
| <span data-ttu-id="d8fa9-228">Nota staðgreiðsluafslátt</span><span class="sxs-lookup"><span data-stu-id="d8fa9-228">Use cash discount</span></span>            | <span data-ttu-id="d8fa9-229">Venjulegt</span><span class="sxs-lookup"><span data-stu-id="d8fa9-229">Normal</span></span>    |
| <span data-ttu-id="d8fa9-230">Notaður staðgreiðsluafsláttur</span><span class="sxs-lookup"><span data-stu-id="d8fa9-230">Cash discount taken</span></span>          | <span data-ttu-id="d8fa9-231">3,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-231">3.00</span></span>      |
| <span data-ttu-id="d8fa9-232">Upphæð staðgreiðsluafsláttar sem á að veita</span><span class="sxs-lookup"><span data-stu-id="d8fa9-232">Cash discount amount to take</span></span> | <span data-ttu-id="d8fa9-233">0,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-233">0.00</span></span>      |

<span data-ttu-id="d8fa9-234">Ef Arnie breytir gildi í reitnum **Nota staðgreiðsluafslátt** í **Alltaf** er stillingunni **Reikna staðgreiðsluafslátt fyrir hlutagreiðslur** er hnekkt og staðgreiðsluafsláttur er veittur.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-234">If Arnie changes the value in the **Use cash discount** field to **Always**, the **Calculate cash discounts for partial payments** setting is overridden, and the cash discount is taken.</span></span> <span data-ttu-id="d8fa9-235">Greiðsluupphæðin breytist í 693,00 og staðgreiðsluafslátturinn er 7,00.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-235">The payment amount changes to 693.00, and the cash discount is the remaining 7.00.</span></span>

| <span data-ttu-id="d8fa9-236">Merkja</span><span class="sxs-lookup"><span data-stu-id="d8fa9-236">Mark</span></span>     | <span data-ttu-id="d8fa9-237">Nota staðgreiðsluafslátt</span><span class="sxs-lookup"><span data-stu-id="d8fa9-237">Use cash discount</span></span> | <span data-ttu-id="d8fa9-238">Fylgiskjal</span><span class="sxs-lookup"><span data-stu-id="d8fa9-238">Voucher</span></span>   | <span data-ttu-id="d8fa9-239">Reikningur</span><span class="sxs-lookup"><span data-stu-id="d8fa9-239">Account</span></span> | <span data-ttu-id="d8fa9-240">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="d8fa9-240">Date</span></span>      | <span data-ttu-id="d8fa9-241">Gjalddagi</span><span class="sxs-lookup"><span data-stu-id="d8fa9-241">Due date</span></span>  | <span data-ttu-id="d8fa9-242">Reikningur</span><span class="sxs-lookup"><span data-stu-id="d8fa9-242">Invoice</span></span> | <span data-ttu-id="d8fa9-243">Upphæð í færslugjaldmiðli - debet</span><span class="sxs-lookup"><span data-stu-id="d8fa9-243">Amount in transaction currency debit</span></span> | <span data-ttu-id="d8fa9-244">Upphæð í færslugjaldmiðli - kredit</span><span class="sxs-lookup"><span data-stu-id="d8fa9-244">Amount in transaction currency credit</span></span> | <span data-ttu-id="d8fa9-245">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d8fa9-245">Currency</span></span> | <span data-ttu-id="d8fa9-246">Upphæð til jöfnunar</span><span class="sxs-lookup"><span data-stu-id="d8fa9-246">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| <span data-ttu-id="d8fa9-247">Valið</span><span class="sxs-lookup"><span data-stu-id="d8fa9-247">Selected</span></span> | <span data-ttu-id="d8fa9-248">Alltaf</span><span class="sxs-lookup"><span data-stu-id="d8fa9-248">Always</span></span>            | <span data-ttu-id="d8fa9-249">FTI-10020</span><span class="sxs-lookup"><span data-stu-id="d8fa9-249">FTI-10020</span></span> | <span data-ttu-id="d8fa9-250">4027</span><span class="sxs-lookup"><span data-stu-id="d8fa9-250">4027</span></span>    | <span data-ttu-id="d8fa9-251">6/25/2015</span><span class="sxs-lookup"><span data-stu-id="d8fa9-251">6/25/2015</span></span> | <span data-ttu-id="d8fa9-252">7/25/2015</span><span class="sxs-lookup"><span data-stu-id="d8fa9-252">7/25/2015</span></span> | <span data-ttu-id="d8fa9-253">10020</span><span class="sxs-lookup"><span data-stu-id="d8fa9-253">10020</span></span>   | <span data-ttu-id="d8fa9-254">700.00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-254">700.00</span></span>                               |                                       | <span data-ttu-id="d8fa9-255">USD</span><span class="sxs-lookup"><span data-stu-id="d8fa9-255">USD</span></span>      | <span data-ttu-id="d8fa9-256">693,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-256">693.00</span></span>           |

<span data-ttu-id="d8fa9-257">Afsláttarupplýsingarnar birtist neðst á síðunni **Jafna opnar færslur** síðunni.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-257">Discount information appears at the bottom of the **Settle open transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="d8fa9-258">Dagsetning staðgreiðsluafsláttar</span><span class="sxs-lookup"><span data-stu-id="d8fa9-258">Cash discount date</span></span>           | <span data-ttu-id="d8fa9-259">7/09/2015</span><span class="sxs-lookup"><span data-stu-id="d8fa9-259">7/09/2015</span></span> |
| <span data-ttu-id="d8fa9-260">Upphæð staðgreiðsluafsláttar</span><span class="sxs-lookup"><span data-stu-id="d8fa9-260">Cash discount amount</span></span>         | <span data-ttu-id="d8fa9-261">7,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-261">7.00</span></span>      |
| <span data-ttu-id="d8fa9-262">Nota staðgreiðsluafslátt</span><span class="sxs-lookup"><span data-stu-id="d8fa9-262">Use cash discount</span></span>            | <span data-ttu-id="d8fa9-263">Alltaf</span><span class="sxs-lookup"><span data-stu-id="d8fa9-263">Always</span></span>    |
| <span data-ttu-id="d8fa9-264">Notaður staðgreiðsluafsláttur</span><span class="sxs-lookup"><span data-stu-id="d8fa9-264">Cash discount taken</span></span>          | <span data-ttu-id="d8fa9-265">3,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-265">3.00</span></span>      |
| <span data-ttu-id="d8fa9-266">Upphæð staðgreiðsluafsláttar sem á að veita</span><span class="sxs-lookup"><span data-stu-id="d8fa9-266">Cash discount amount to take</span></span> | <span data-ttu-id="d8fa9-267">7,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-267">7.00</span></span>      |

<span data-ttu-id="d8fa9-268">Arnie breytir gildinu í reitnum **Nota staðgreiðsluafslátt** aftur í **Venjulegt**, þar sem hann lætur þennan viðskiptavin ekki fá eftirstandandi staðgreiðsluafslátt upp á 7,00.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-268">Arnie changes the value in the **Use cash discount** field back to **Normal**, because he is not letting this customer take the remaining cash discount of 7.00.</span></span> <span data-ttu-id="d8fa9-269">Síðan bókar Arnie reikninginn.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-269">Arnie then posts the payment.</span></span> <span data-ttu-id="d8fa9-270">Þegar Arnie opnar síðuna **Færslur viðskiptavina** sér hann að reikningurinn hefur stöðuna 0,00.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-270">When Arnie opens the **Customer transactions** page, he sees that the invoice has a balance of 0.00.</span></span> <span data-ttu-id="d8fa9-271">Hann sér einnig að það eru tvær greiðslur.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-271">He also sees that there are two payments.</span></span> <span data-ttu-id="d8fa9-272">Ein greiðsla er upp á 297,00 með 3,00 staðgreiðsluafslætti og önnur greiðsla er upp á 700,00.</span><span class="sxs-lookup"><span data-stu-id="d8fa9-272">One payment is for 297.00 and has a 3.00 cash discount, and the other payment is for 700.00.</span></span>

| <span data-ttu-id="d8fa9-273">Fylgiskjal</span><span class="sxs-lookup"><span data-stu-id="d8fa9-273">Voucher</span></span>    | <span data-ttu-id="d8fa9-274">Færslugerð</span><span class="sxs-lookup"><span data-stu-id="d8fa9-274">Transaction type</span></span> | <span data-ttu-id="d8fa9-275">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="d8fa9-275">Date</span></span>      | <span data-ttu-id="d8fa9-276">Reikningur</span><span class="sxs-lookup"><span data-stu-id="d8fa9-276">Invoice</span></span> | <span data-ttu-id="d8fa9-277">Upphæð í færslugjaldmiðli - debet</span><span class="sxs-lookup"><span data-stu-id="d8fa9-277">Amount in transaction currency debit</span></span> | <span data-ttu-id="d8fa9-278">Upphæð í færslugjaldmiðli - kredit</span><span class="sxs-lookup"><span data-stu-id="d8fa9-278">Amount in transaction currency credit</span></span> | <span data-ttu-id="d8fa9-279">Staða</span><span class="sxs-lookup"><span data-stu-id="d8fa9-279">Balance</span></span> | <span data-ttu-id="d8fa9-280">Gjaldmiðill</span><span class="sxs-lookup"><span data-stu-id="d8fa9-280">Currency</span></span> |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| <span data-ttu-id="d8fa9-281">FTI-10020</span><span class="sxs-lookup"><span data-stu-id="d8fa9-281">FTI-10020</span></span>  | <span data-ttu-id="d8fa9-282">Reikningur</span><span class="sxs-lookup"><span data-stu-id="d8fa9-282">Invoice</span></span>          | <span data-ttu-id="d8fa9-283">6/25/2015</span><span class="sxs-lookup"><span data-stu-id="d8fa9-283">6/25/2015</span></span> | <span data-ttu-id="d8fa9-284">10020</span><span class="sxs-lookup"><span data-stu-id="d8fa9-284">10020</span></span>   | <span data-ttu-id="d8fa9-285">1.000,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-285">1,000.00</span></span>                             |                                       | <span data-ttu-id="d8fa9-286">0,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-286">0.00</span></span>    | <span data-ttu-id="d8fa9-287">USD</span><span class="sxs-lookup"><span data-stu-id="d8fa9-287">USD</span></span>      |
| <span data-ttu-id="d8fa9-288">ARP-10020</span><span class="sxs-lookup"><span data-stu-id="d8fa9-288">ARP-10020</span></span>  |                  | <span data-ttu-id="d8fa9-289">7/1/2015</span><span class="sxs-lookup"><span data-stu-id="d8fa9-289">7/1/2015</span></span>  |         |                                      | <span data-ttu-id="d8fa9-290">297,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-290">297.00</span></span>                                | <span data-ttu-id="d8fa9-291">0,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-291">0.00</span></span>    | <span data-ttu-id="d8fa9-292">USD</span><span class="sxs-lookup"><span data-stu-id="d8fa9-292">USD</span></span>      |
| <span data-ttu-id="d8fa9-293">DISC-10020</span><span class="sxs-lookup"><span data-stu-id="d8fa9-293">DISC-10020</span></span> |                  | <span data-ttu-id="d8fa9-294">7/1/2015</span><span class="sxs-lookup"><span data-stu-id="d8fa9-294">7/1/2015</span></span>  |         |                                      | <span data-ttu-id="d8fa9-295">3,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-295">3.00</span></span>                                  | <span data-ttu-id="d8fa9-296">0,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-296">0.00</span></span>    | <span data-ttu-id="d8fa9-297">USD</span><span class="sxs-lookup"><span data-stu-id="d8fa9-297">USD</span></span>      |
| <span data-ttu-id="d8fa9-298">ARP 10021</span><span class="sxs-lookup"><span data-stu-id="d8fa9-298">ARP-10021</span></span>  |                  | <span data-ttu-id="d8fa9-299">7/11/2015</span><span class="sxs-lookup"><span data-stu-id="d8fa9-299">7/11/2015</span></span> |         |                                      | <span data-ttu-id="d8fa9-300">700.00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-300">700.00</span></span>                                | <span data-ttu-id="d8fa9-301">0,00</span><span class="sxs-lookup"><span data-stu-id="d8fa9-301">0.00</span></span>    | <span data-ttu-id="d8fa9-302">USD</span><span class="sxs-lookup"><span data-stu-id="d8fa9-302">USD</span></span>      |




