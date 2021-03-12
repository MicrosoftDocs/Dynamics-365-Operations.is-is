---
title: Nota greiðsluspár viðskiptavinar (forskoðun)
description: Þetta efnisatriði fer með þig í gegnum áskildar forsendur og áskilin skref til að nota prufuútgáfu Fjármálainnsýnar.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-11-16
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: aa4a4975fc2ccdd91d5beb32060d68f7e77dbcb7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645650"
---
# <a name="use-customer-payment-predictions-preview"></a><span data-ttu-id="5e2b4-103">Nota greiðsluspár viðskiptavinar (forskoðun)</span><span class="sxs-lookup"><span data-stu-id="5e2b4-103">Use Customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="5e2b4-104">Þetta efnisatriði útskýrir hverni gá að nota greiðsluspár viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-104">This topic explains how to use the Customer payment predictions.</span></span> <span data-ttu-id="5e2b4-105">Gakktu úr skugga um að ljúka við uppsetningarskrefin áður en þú notar þennan eiginleika.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-105">Before you use this feature, make sure that you've completed the setup steps for it.</span></span> <span data-ttu-id="5e2b4-106">Nánari upplýsingar eru í [Virkja greiðsluspár viðskiptavinar](enable-cust-paymnt-prediction.md).</span><span class="sxs-lookup"><span data-stu-id="5e2b4-106">For more information, see [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

<span data-ttu-id="5e2b4-107">Þú getur skoðað greiðsluspár viðskiptavinar á vinnusvæðinu **Stjórna skuldum og innheimtu viðskiptavinar** og á tveimur nýjum listasíðum **Greiðsluspár fyrir hverja færslu** og **Greiðsluspár fyrir hvern viðskiptavin**.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-107">You can view customer payment predictions in the **Manage customer credit and collections** workspace and on two new list pages, **Payment predictions per transaction** and **Payment prediction per customer**.</span></span>

### <a name="manage-customer-credit-and-collections-workspace"></a><span data-ttu-id="5e2b4-108">Stjórna vinnusvæði skulda og innheimtu viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="5e2b4-108">Manage customer credit and collections workspace</span></span>

<span data-ttu-id="5e2b4-109">Vinnusvæðið **Stjórna skuldum og innheimtu viðskiptavinar** inniheldur tvo nýja reiti, **Greiðsluspár fyrir hverja færslu** og **Viðskiptavinir með stöður sem áætlað er að verði á eftir áætlun**.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-109">The **Manage customer credit and collections** workspace includes two new tiles, **Payment prediction per transaction** and **Customers with predicted high late balances**.</span></span>

- <span data-ttu-id="5e2b4-110">Reiturinn **Greiðsluspár fyrir hverja færslu** sýnir fjölda opinna færslna viðskiptavinar þar sem líkur á að greiðsla sé á réttum tíma eru innan við 50 prósent í rammanum **Á réttum tíma**.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-110">The **Payment prediction per transaction** tile shows the number of open customer transactions that have a probability of payment that is less than 50 percent in the **On time** bucket.</span></span> <span data-ttu-id="5e2b4-111">Þú getur valið þennan reit til að opna listasíðuna **Greiðsluspár fyrir hverja færslu**.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-111">You can select this tile to open the **Payment predictions per transaction** list page.</span></span>
- <span data-ttu-id="5e2b4-112">Reiturinn **Viðskiptavinir með stöður sem áætlað er að verði á eftir áætlun** sýnir fjölda viðskiptavina þar sem áætlað er að helmingur (50 prósent) af heildarstöðunni verði greiddur seint og/eða mjög seint.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-112">The **Customers with predicted high late balances** tile shows the number of customers for which more than half (50 percent) of the total balance is predicted to be paid late and/or very late.</span></span> <span data-ttu-id="5e2b4-113">Þú getur valið þennan reit til að opna listasíðuna **Greiðsluspár fyrir hvern viðskiptavin**.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-113">You can select this tile to open the **Payment prediction per customer** list page.</span></span>

<span data-ttu-id="5e2b4-114">[![Viðskiptavinir með stöður sem áætlað er að verði á eftir áætlun](./media/manage-customer-credit-collections.png)](./media/manage-customer-credit-collections.png)</span><span class="sxs-lookup"><span data-stu-id="5e2b4-114">[![Manage customer credit and collections workspace](./media/manage-customer-credit-collections.png)](./media/manage-customer-credit-collections.png)</span></span>

### <a name="payment-predictions-per-transaction-list-page"></a><span data-ttu-id="5e2b4-115">Listasíða greiðsluspár fyrir hverja færslu</span><span class="sxs-lookup"><span data-stu-id="5e2b4-115">Payment predictions per transaction list page</span></span>

<span data-ttu-id="5e2b4-116">Á listasíðunni **Greiðsluspár fyrir hverja færslu** getur þú skoðað líkurnar á greiðslu fyrir opnar færslur í römmunum **Á réttum tíma**, **Seint**, og **Mjög seint**.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-116">On the **Payment predictions per transaction** list page, you can view the probability of payment for open transactions in the **On time**, **Late**, and **Very late** buckets.</span></span> <span data-ttu-id="5e2b4-117">Fyrir hverja færslu á hnitanetinu sýnir dálkurinn **Líkur á réttum tíma** líkurnar á því að reikningurinn verði greiddur á eða fyrir gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-117">For each transaction in the grid, the **On time probability** column shows the probability that the invoice will be paid on or before the due date.</span></span> <span data-ttu-id="5e2b4-118">Þegar líkurnar á greiðslu á réttum tíma eru minni en 50 prósent birtist rauður hringur við hliðina á prósentuhlutfallinu í dálkinum **Líkur á réttum tíma** til að tilgreina hættuna á greiðsludrætti.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-118">If the probability of an on-time payment is less than 50 percent, a red circle appears next to the percentage in the **On time probability** column to indicate the risk of late payment.</span></span>

<span data-ttu-id="5e2b4-119">[![Síða greiðsluspár fyrir hverja færslu](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)</span><span class="sxs-lookup"><span data-stu-id="5e2b4-119">[![Payment prediction per transaction page](./media/payment-predictions-per-transaction.png)](./media/payment-predictions-per-transaction.png)</span></span>

<span data-ttu-id="5e2b4-120">Í glugganum **Tengdar upplýsingar** hægra megin á síðunni birtast frekari upplýsingar um spárnar:</span><span class="sxs-lookup"><span data-stu-id="5e2b4-120">The **Related information** pane on the right side of the page shows more details about the predictions:</span></span>

- <span data-ttu-id="5e2b4-121">Fyrir færsluna sem er valin á hnitanetinu sýnir flýtiflipinn **Greiðsluspá** frekari upplýsingar um greiðsluspár í römmunum **Á réttum tíma**, **Seint** og **Mjög seint**.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-121">For the transaction that is selected in the grid, the **Payment prediction** FastTab shows the details of the payment predictions in the **On time**, **Late**, and **Very late** buckets.</span></span> <span data-ttu-id="5e2b4-122">Hlutinn **Helstu þættir** sýnir helstu þættina sem hafa áhrif á spárnar.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-122">The **Top factors** section shows the top factors that influenced the predictions.</span></span> <span data-ttu-id="5e2b4-123">Helstu þættir eru eiginleikar valinnar færslu og/eða viðskiptavinurinn fyrir umrædda færslu.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-123">The top factors are attributes of the selected transaction and/or the customer for that transaction.</span></span>
- <span data-ttu-id="5e2b4-124">Flýtiflipinn **Innsýn í viðskiptavini** sýnir núverandi reikning, greiðslu og tölfræði innheimtu fyrir valda færslu.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-124">The **Customer insights** FastTab shows the current invoice, payment, and collections statistics for the customer for the selected transaction.</span></span>
- <span data-ttu-id="5e2b4-125">Flýtiflipinn **Ferill viðskiptavinar** sýnir greiðsluferil viðskiptavinarins í römmunum **Á réttum tíma**, **Seint** og **Mjög seint**.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-125">The **Customer history** FastTab shows the customer's payment history in the **On time**, **Late**, and **Very late** buckets.</span></span>

<span data-ttu-id="5e2b4-126">Gögnin í hlutanum **Helstu þættir** og á flýtiflipunum **Innsýn í viðskiptavini** og **Ferill viðskiptavinar** hjálpa til við að útskýra greiðsluspárnar.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-126">The data in the **Top factors** section, and on the **Customer insights** and **Customer history** FastTabs, helps explain the payment predictions.</span></span> <span data-ttu-id="5e2b4-127">Slíkt getur aukið traust þitt á áreiðanleika slíkra spáa.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-127">It can help increase your confidence in the efficacy of the predictions.</span></span>

<span data-ttu-id="5e2b4-128">[![Myndrænir vísar fyrir greiðsluspár í glugganum tengdar upplýsingar](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)</span><span class="sxs-lookup"><span data-stu-id="5e2b4-128">[![Graphical indicators for payment predictions in the Related information pane](./media/payment-prediction-gauges.png)](./media/payment-prediction-gauges.png)</span></span>

### <a name="payment-prediction-per-customer-list-page"></a><span data-ttu-id="5e2b4-129">Listasíða greiðsluspár fyrir hvern viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="5e2b4-129">Payment prediction per customer list page</span></span>

<span data-ttu-id="5e2b4-130">Listasíðan **Greiðsluspár fyrir hvern viðskiptavin** sýnir opnunarstöðu samtals og upphæðina sem spáð er að greidd verði í römmunum **Á réttum tíma**, **Seint** og **Mjög seint**.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-130">The **Payment prediction per customer** list page shows the total open balance, and the amount that is predicted to be paid in the **On time**, **Late** and **Very late** buckets.</span></span>

<span data-ttu-id="5e2b4-131">[![Síða greiðsluspár fyrir hvern viðskiptavin](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)</span><span class="sxs-lookup"><span data-stu-id="5e2b4-131">[![Payment predictions per customer page](./media/payment-predictions-per-transaction-02.png)](./media/payment-predictions-per-transaction-02.png)</span></span>

<span data-ttu-id="5e2b4-132">Greiðsluupphæðin í hverjum ramma er reiknuð út sem summa af vegnu meðaltali færsluupphæðarinnar.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-132">The payment amount in each bucket is calculated as the sum of the weighted average of the transaction balance.</span></span> <span data-ttu-id="5e2b4-133">Þessi upphæð er reiknuð út miðað við greiðslulíkur fyrir hvern ramma fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-133">This amount is calculated based on the payment probabilities in each bucket.</span></span>

<span data-ttu-id="5e2b4-134">Viðskiptavinur er t.d. með þrjár opnar færslur sem hafa eftirfarandi greiðslulíkur í hverjum ramma fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-134">For example, a customer has three open transactions that have the following payment probabilities in each bucket.</span></span>

| <span data-ttu-id="5e2b4-135">Færsla</span><span class="sxs-lookup"><span data-stu-id="5e2b4-135">Transaction</span></span> | <span data-ttu-id="5e2b4-136">Upphæð</span><span class="sxs-lookup"><span data-stu-id="5e2b4-136">Amount</span></span> | <span data-ttu-id="5e2b4-137">Líkur á greiðslu á réttum tíma</span><span class="sxs-lookup"><span data-stu-id="5e2b4-137">On-time payment probability</span></span> | <span data-ttu-id="5e2b4-138">Líkur á greiðslu seint</span><span class="sxs-lookup"><span data-stu-id="5e2b4-138">Late payment probability</span></span> | <span data-ttu-id="5e2b4-139">Líkur að greiðslu mjög seint</span><span class="sxs-lookup"><span data-stu-id="5e2b4-139">Very late payment probability</span></span> |
|-------------|--------|-----------------------------|--------------------------|-------------------------------|
| <span data-ttu-id="5e2b4-140">T1</span><span class="sxs-lookup"><span data-stu-id="5e2b4-140">T1</span></span>          | <span data-ttu-id="5e2b4-141">100</span><span class="sxs-lookup"><span data-stu-id="5e2b4-141">100</span></span>    | <span data-ttu-id="5e2b4-142">10 prósent</span><span class="sxs-lookup"><span data-stu-id="5e2b4-142">10 percent</span></span>                  | <span data-ttu-id="5e2b4-143">50 prósent</span><span class="sxs-lookup"><span data-stu-id="5e2b4-143">50 percent</span></span>               | <span data-ttu-id="5e2b4-144">40 prósent</span><span class="sxs-lookup"><span data-stu-id="5e2b4-144">40 percent</span></span>                    |
| <span data-ttu-id="5e2b4-145">T2</span><span class="sxs-lookup"><span data-stu-id="5e2b4-145">T2</span></span>          | <span data-ttu-id="5e2b4-146">1.000</span><span class="sxs-lookup"><span data-stu-id="5e2b4-146">1,000</span></span>  | <span data-ttu-id="5e2b4-147">50 prósent</span><span class="sxs-lookup"><span data-stu-id="5e2b4-147">50 percent</span></span>                  | <span data-ttu-id="5e2b4-148">30 prósent</span><span class="sxs-lookup"><span data-stu-id="5e2b4-148">30 percent</span></span>               | <span data-ttu-id="5e2b4-149">20 prósent</span><span class="sxs-lookup"><span data-stu-id="5e2b4-149">20 percent</span></span>                    |
| <span data-ttu-id="5e2b4-150">T3</span><span class="sxs-lookup"><span data-stu-id="5e2b4-150">T3</span></span>          | <span data-ttu-id="5e2b4-151">10,000</span><span class="sxs-lookup"><span data-stu-id="5e2b4-151">10,000</span></span> | <span data-ttu-id="5e2b4-152">1 prósent</span><span class="sxs-lookup"><span data-stu-id="5e2b4-152">1 percent</span></span>                   | <span data-ttu-id="5e2b4-153">4 prósent</span><span class="sxs-lookup"><span data-stu-id="5e2b4-153">4 percent</span></span>                | <span data-ttu-id="5e2b4-154">95 prósent</span><span class="sxs-lookup"><span data-stu-id="5e2b4-154">95 percent</span></span>                    |

<span data-ttu-id="5e2b4-155">Í slíku tilviki eru greiðslur áætlaðar fyrir hvern ramma á eftirfarandi hátt.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-155">In this case, payments are projected for each bucket in the following way.</span></span>

| <span data-ttu-id="5e2b4-156">Rammar</span><span class="sxs-lookup"><span data-stu-id="5e2b4-156">Buckets</span></span>   | <span data-ttu-id="5e2b4-157">Færsla T1</span><span class="sxs-lookup"><span data-stu-id="5e2b4-157">Transaction T1</span></span>      | <span data-ttu-id="5e2b4-158">Færsla T2</span><span class="sxs-lookup"><span data-stu-id="5e2b4-158">Transaction T2</span></span>         | <span data-ttu-id="5e2b4-159">Færsla T3</span><span class="sxs-lookup"><span data-stu-id="5e2b4-159">Transaction T3</span></span>            | <span data-ttu-id="5e2b4-160">Alls</span><span class="sxs-lookup"><span data-stu-id="5e2b4-160">Total</span></span> |
|-----------|---------------------|------------------------|---------------------------|-------|
| <span data-ttu-id="5e2b4-161">Á réttum tíma</span><span class="sxs-lookup"><span data-stu-id="5e2b4-161">On time</span></span>   | <span data-ttu-id="5e2b4-162">100 × 10 ÷ 100 = 10</span><span class="sxs-lookup"><span data-stu-id="5e2b4-162">100 × 10 ÷ 100 = 10</span></span> | <span data-ttu-id="5e2b4-163">1.000 × 50 ÷ 100 = 500</span><span class="sxs-lookup"><span data-stu-id="5e2b4-163">1,000 × 50 ÷ 100 = 500</span></span> | <span data-ttu-id="5e2b4-164">10.000 × 1 ÷ 100 = 100</span><span class="sxs-lookup"><span data-stu-id="5e2b4-164">10,000 × 1 ÷ 100 = 100</span></span>    | <span data-ttu-id="5e2b4-165">610</span><span class="sxs-lookup"><span data-stu-id="5e2b4-165">610</span></span>   |
| <span data-ttu-id="5e2b4-166">Á eftir áætlun</span><span class="sxs-lookup"><span data-stu-id="5e2b4-166">Late</span></span>      | <span data-ttu-id="5e2b4-167">100 × 50 ÷ 100 = 50</span><span class="sxs-lookup"><span data-stu-id="5e2b4-167">100 × 50 ÷ 100 = 50</span></span> | <span data-ttu-id="5e2b4-168">1.000 × 30 ÷ 100 = 300</span><span class="sxs-lookup"><span data-stu-id="5e2b4-168">1,000 × 30 ÷ 100 = 300</span></span> | <span data-ttu-id="5e2b4-169">10.000 × 4 ÷ 100 = 400</span><span class="sxs-lookup"><span data-stu-id="5e2b4-169">10,000 × 4 ÷ 100 = 400</span></span>    | <span data-ttu-id="5e2b4-170">750</span><span class="sxs-lookup"><span data-stu-id="5e2b4-170">750</span></span>   |
| <span data-ttu-id="5e2b4-171">Mjög seint</span><span class="sxs-lookup"><span data-stu-id="5e2b4-171">Very late</span></span> | <span data-ttu-id="5e2b4-172">100 × 40 ÷ 100 = 40</span><span class="sxs-lookup"><span data-stu-id="5e2b4-172">100 × 40 ÷ 100 = 40</span></span> | <span data-ttu-id="5e2b4-173">1.000 × 20 ÷ 100 = 200</span><span class="sxs-lookup"><span data-stu-id="5e2b4-173">1,000 × 20 ÷ 100 = 200</span></span> | <span data-ttu-id="5e2b4-174">10.000 × 95 ÷ 100 = 9.500</span><span class="sxs-lookup"><span data-stu-id="5e2b4-174">10,000 × 95 ÷ 100 = 9,500</span></span> | <span data-ttu-id="5e2b4-175">9,740</span><span class="sxs-lookup"><span data-stu-id="5e2b4-175">9,740</span></span> |

<span data-ttu-id="5e2b4-176">Í hlutanum **Tengdar upplýsingar** hægra megin á síðunni birtast frekari upplýsingar um spárnar:</span><span class="sxs-lookup"><span data-stu-id="5e2b4-176">The **Related information** section on the right side of the page shows more details about the predictions:</span></span>

- <span data-ttu-id="5e2b4-177">Fyrir færsluna sem er valin á hnitanetinu sýnir flýtiflipinn **Greiðsluspár** frekari upplýsingar um greiðsluspár í römmunum **Á réttum tíma**, **Seint** og **Mjög seint**.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-177">For the transaction that is selected in the grid, the **Payment predictions** FastTab shows the details of the payment predictions in the **On time**, **Late**, and **Very Late** buckets.</span></span> <span data-ttu-id="5e2b4-178">Hlutinn **Helstu þættir** sýnir helstu þættina sem hafa áhrif á greiðslurnar.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-178">The **Top factors** section shows the top factors that influenced the payments.</span></span> <span data-ttu-id="5e2b4-179">Helstu þættir eru eiginleikar valinnar færslu og/eða viðskiptavinurinn fyrir umrædda færslu.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-179">The top factors are attributes of the selected transaction and/or the customer for that transaction.</span></span>
- <span data-ttu-id="5e2b4-180">Flýtiflipinn **Innsýn í viðskiptavini** sýnir núverandi reikning, greiðslu og tölfræði innheimtu fyrir valda færslu.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-180">The **Customer insights** FastTab shows the current invoice, payment, and collections statistics for the customer for the selected transaction.</span></span>
- <span data-ttu-id="5e2b4-181">Flýtiflipinn **Ferill viðskiptavinar** sýnir greiðsluferil viðskiptavinarins í römmunum **Á réttum tíma**, **Seint** og **Mjög seint**.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-181">The **Customer history** FastTab shows the customer's payment history in the **On time**, **Late**, and **Very late** buckets.</span></span>

<span data-ttu-id="5e2b4-182">Gögnin í hlutanum **Helstu þættir** og á flýtiflipunum **Innsýn í viðskiptavini** og **Ferill viðskiptavinar** hjálpa til við að útskýra greiðsluspárnar.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-182">The data in the **Top factors** section, and on the **Customer insights** and **Customer history** FastTabs, helps explain the payment predictions.</span></span> <span data-ttu-id="5e2b4-183">Slíkt getur aukið traust þitt á áreiðanleika slíkra spáa.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-183">It can help increase your confidence in the efficacy of the predictions.</span></span>

## <a name="improving-the-accuracy-of-payment-predictions"></a><span data-ttu-id="5e2b4-184">Auka nákvæmni greiðsluspáa</span><span class="sxs-lookup"><span data-stu-id="5e2b4-184">Improving the accuracy of payment predictions</span></span>

<span data-ttu-id="5e2b4-185">Þú getur skoðað nákvæmni greiðsluspáa með því að opna **Skuldir og innheimta \> Uppsetning \> Fjármálainnsýn \> Færibreytur fjármálainnsýnar**.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-185">You can view the accuracy of payment predictions by going to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span> <span data-ttu-id="5e2b4-186">Á flipanum **Innsýn í greiðslu viðskiptavinar** sýnir hlutinn **Spálíkan** nákvæmni spálíkansins sem prósentuhlutfall.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-186">On the **Customer payment insights** tab, the **Prediction model** section shows the accuracy of the prediction model as a percentage.</span></span>

<span data-ttu-id="5e2b4-187">[![Nákvæmni greiðsluspáa](./media/finance-insights-parameters-accuracy-2nd.png)](./media/finance-insights-parameters-accuracy-2nd.png)</span><span class="sxs-lookup"><span data-stu-id="5e2b4-187">[![Accuracy of payment predictions](./media/finance-insights-parameters-accuracy-2nd.png)](./media/finance-insights-parameters-accuracy-2nd.png)</span></span>

<span data-ttu-id="5e2b4-188">Ef nákvæmnin telst ekki vera fullnægjandi skaltu velja tengilinn **Auka nákvæmni líkans** til að opna upplifun AI Builder-viðbótarinnar.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-188">If you aren't satisfied with the accuracy, select the **Improve model accuracy** link to open the AI Builder extension experience.</span></span> <span data-ttu-id="5e2b4-189">Í upplifun AI Builder-viðbótarinnar getur þú valið að hætta við val á svæðum þar til þú hefur valið reitina sem þú telur vera mikilvægasta til að spá fyrir um greiðslulíkur á nákvæman hátt.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-189">In the AI Builder extension experience, you can select or cancel the selection of fields until you've selected the fields that you believe are most important for accurately predicting payment probabilities.</span></span> <span data-ttu-id="5e2b4-190">Þegar því er lokið getur þú auðveldlega endurþjálfað spálíkanið og birt breytingarnar þínar.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-190">When you've finished, you can easily retrain the prediction model and publish your changes.</span></span> <span data-ttu-id="5e2b4-191">Nýþjálfaða spálíkanið verður sjálfkrafa valið fyrir spár í Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-191">The newly trained prediction model will automatically be picked up for predictions in Dynamics 365 Finance.</span></span>

<span data-ttu-id="5e2b4-192">[![Upplifun AI Builder-viðbótar](./media/ai-builder.png)](./media/ai-builder.png)</span><span class="sxs-lookup"><span data-stu-id="5e2b4-192">[![AI Builder extension experience](./media/ai-builder.png)](./media/ai-builder.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="5e2b4-193">Upplýsingar um losun</span><span class="sxs-lookup"><span data-stu-id="5e2b4-193">Release details</span></span>

<span data-ttu-id="5e2b4-194">Almenn forskoðun Fjármálainnsýnar er í boði til uppsetningar í Bandaríkjunum, Evrópu og Bretlandi.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-194">Finance insights public preview is available to try for deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="5e2b4-195">Microsoft bætir smátt og smátt við stuðningi fyrir fleiri svæði.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-195">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="5e2b4-196">Aðeins er hægt og aðeins skal kveikja á eiginleikum almennrar forskoðunar í tveggja laga sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-196">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="5e2b4-197">Uppsetningar- og gervigreindarlíkön sem eru stofnuð í sandkassaumhverfi eru ekki hægt að flytja yfir í vinnsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-197">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="5e2b4-198">Frekari upplýsingar er að finna í [Viðbótarnotkunarskilmálum fyrir Microsoft Dynamics 365 forskoðanir](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span><span class="sxs-lookup"><span data-stu-id="5e2b4-198">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/public-preview-terms).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="5e2b4-199">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="5e2b4-199">Privacy notice</span></span>

<span data-ttu-id="5e2b4-200">Forútgáfur (1) kunna að nota minni persónuverndar- og öryggisráðstafanir og þjónusta Dynamics 365 Finance and Operations, (2) eru ekki hluti af þjónustustigssamningi fyrir þessa þjónustu, (3) ættu ekki að vera notaðar til að vinna úr persónulegum gögnum eða öðrum gögnum sem falla undir lögboðnar kröfur eða reglur um samræmi og (4) hafa takmarkaðan stuðning.</span><span class="sxs-lookup"><span data-stu-id="5e2b4-200">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>