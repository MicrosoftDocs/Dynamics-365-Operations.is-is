---
title: Pantanir viðskiptavinar í Modern POS (MPOS)
description: Þetta efnisatriði gefur upplýsingar um pantanir viðskiptavinar í Modern POS (MPOS). Pantanir viðskiptavinar eru einnig þekktar sem sérpantanir. Efnisatriðið inniheldur umræðu um tengdar færibreytur og færsluflæði.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b8ea8339c2ad25ceed2415eb5ccf5e2048c612fa
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022869"
---
# <a name="customer-orders-in-modern-pos-mpos"></a><span data-ttu-id="cf0c6-105">Pantanir viðskiptavinar í Modern POS (MPOS)</span><span class="sxs-lookup"><span data-stu-id="cf0c6-105">Customer orders in Modern POS (MPOS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cf0c6-106">Þetta efnisatriði gefur upplýsingar um pantanir viðskiptavinar í Modern POS (MPOS).</span><span class="sxs-lookup"><span data-stu-id="cf0c6-106">This topic provides information about customer orders in Modern POS (MPOS).</span></span> <span data-ttu-id="cf0c6-107">Pantanir viðskiptavinar eru einnig þekktar sem sérpantanir.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="cf0c6-108">Efnisatriðið inniheldur umræðu um tengdar færibreytur og færsluflæði.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="cf0c6-109">Í alhliða samskiptum netverslunar veita margir smásalar valkost pantana viðskiptavina eða sérpantana til að mæta ýmsum þörfum afurða og uppfyllingar.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-109">In an omni-channel commerce world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="cf0c6-110">Hér eru nokkrar dæmigerðar aðstæður.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-110">Here are some typical scenarios:</span></span>

- <span data-ttu-id="cf0c6-111">Viðskiptavinur vill að afurð sé afhent á tilgreint aðsetur á tilgreindum degi.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
- <span data-ttu-id="cf0c6-112">Viðskiptavinur vill taka til afurðir úr verslun eða staðsetningu sem er önnur en verslunin eða staðsetningin þar sem viðskiptamaðurinn keypti þær afurðir.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
- <span data-ttu-id="cf0c6-113">Viðskiptavinur vill að einhver annar taki til afurðir sem viðskiptamaðurinn keypti.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="cf0c6-114">Smásalar nota einnig pantanir viðskiptavinar til að lágmarka tapaða sölu sem birgðastöðvanir gætu annars valdið, þar sem varninginn má afhenda eða taka til á mismunandi tíma eða stað.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="cf0c6-115">Setja upp pantanir viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="cf0c6-115">Set up customer orders</span></span>

<span data-ttu-id="cf0c6-116">Hér eru nokkrar af færibreytur sem hægt er að stilla á síðunni **Commerce-færibreytur** til að skilgreina hvernig pantanir viðskiptavinar eru uppfylltar:</span><span class="sxs-lookup"><span data-stu-id="cf0c6-116">Here are some of the parameters that can be set on the **Commerce parameters** page to define how customer orders are fulfilled:</span></span>

- <span data-ttu-id="cf0c6-117">**Prósenta sjálfgefinnar innborgunar** – Tilgreina upphæð sem viðskiptamaðurinn verður að borga sem innistæða áður en hægt er að staðfesta pöntun.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="cf0c6-118">Sjálfgefin innborgunarupphæð er reiknuð sem prósenta af virði pöntunar.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="cf0c6-119">Það fer eftir réttindum en aðili tengdur verslun gæti hnekkt upphæð með því að nota **Hnekking innborgunar**.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
- <span data-ttu-id="cf0c6-120">**Afpöntunargjald prósenta** – Ef gjald verður jafnað þegar hætt er við pöntun viðskiptavinar, skal skilgreina upphæð þess gjalds.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
- <span data-ttu-id="cf0c6-121">**Kóði afpöntunargjalds** – Ef gjald er sett á þegar pöntun frá viðskiptavini er afturkölluð, er það gjald sýnt með gjaldkóða á sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="cf0c6-122">Notaðu þessa færibreytu til að skilgreina kóða afpöntunargjalds.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-122">Use this parameter to define the cancellation charge code.</span></span>
- <span data-ttu-id="cf0c6-123">**Kóði sendingargjalds** – Smásalar geta rukkað sérstaka þóknun fyrir afhendingu á varningi til viðskiptavinur.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="cf0c6-124">Upphæð þess sendingargjalds er sýnt undir gjaldkóða á sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="cf0c6-125">Notaðu þessa færibreytu til að varpa kóða sendingargjalds í sendingargjöld á pöntun viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
- <span data-ttu-id="cf0c6-126">**Endurgreiðsla sendingargjöld** – Tilgreina hvort sendingargjöld sem eru sem tengist a pöntun viðskiptavinar eru endurgreiðanleg.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
- <span data-ttu-id="cf0c6-127">**Hámarksupphæð án samþykkis** – Ef sendingargjöld eru endurgreiðanleg skal tilgreina hámarksupphæð endurgreiðslu sendingargjalda í skilapöntunum.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="cf0c6-128">Ef farið er upp fyrir þessa upphæð er hnekkingu stjórnanda þörf til að halda áfram með endurgreiðsluna.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="cf0c6-129">Til að koma fyrir eftirfarandi sviðsmyndum getur endurgreiðsla á sendingargjöldum farið yfir upphæðina sem var upphaflega greidd:</span><span class="sxs-lookup"><span data-stu-id="cf0c6-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>

    - <span data-ttu-id="cf0c6-130">Gjöld eru jafnað á stigi sölupöntunarhauss, og þegar sumu magni afurðarlínu er skilað, er ekki hægt að ákvarða hámarksendurgreiðslu sendingargjalda sem er leyfileg fyrir afurðir og magn á þann hátt sem virkar fyrir alla viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all customers.</span></span>
    - <span data-ttu-id="cf0c6-131">Stofnað er til sendingargjalda fyrir hvert tilvik sendingar.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="cf0c6-132">Ef viðskiptavinur skilar afurð mörgum sinnum og stefna smásala tilgreinir að smásalinn beri kostnað af gjöldum skilasendingar, verða sendingargjöld skila meiri en raunveruleg sendingargjöld.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-132">If a customer returns products multiple times, and the retailer's policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="cf0c6-133">Færsluflæði fyrir pantanir viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="cf0c6-133">Transaction flow for customer orders</span></span>

### <a name="create-a-customer-order-in-modern-pos"></a><span data-ttu-id="cf0c6-134">Stofna pöntun viðskiptavinar í Modern POS</span><span class="sxs-lookup"><span data-stu-id="cf0c6-134">Create a customer order in Modern POS</span></span>

1. <span data-ttu-id="cf0c6-135">Bæta skal viðskiptavini við færsluna.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-135">Add a customer to the transaction.</span></span>
2. <span data-ttu-id="cf0c6-136">Bæta afurðum við körfuna.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-136">Add products to the cart.</span></span>
3. <span data-ttu-id="cf0c6-137">Smellið á **Stofna pöntun viðskiptavinar**, og svo velurðu gerð pöntunar.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-137">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="cf0c6-138">Gerð pöntunar getur verið annaðhvort **Pöntun viðskiptavinar** eða **Tilboð**.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-138">The order type can be either **Customer order** or **Quote**.</span></span>
4. <span data-ttu-id="cf0c6-139">Smellt er á **Senda valið** eða **Senda allt** til að senda afurðir á aðsetur á viðskiptavinalykli, skal tilgreina áskilda sendingardagsetningu og sendingargjöld.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-139">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5. <span data-ttu-id="cf0c6-140">Smellt er á **Taka til valið** eða **Taka allt til** til að velja afurðir sem verða teknar til úr núgildandi verslun eða annarri verslun á tilgreindum degi.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-140">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6. <span data-ttu-id="cf0c6-141">Innheimtu innborgunarupphæðina ef innborgunar er þörf.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-141">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="cf0c6-142">Breyta fyrirliggjandi pöntun viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="cf0c6-142">Edit an existing customer order</span></span>

1. <span data-ttu-id="cf0c6-143">Á heimasíðunni smellirðu á **Finna pöntun**.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-143">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="cf0c6-144">Finna og velja pöntunina sem á að breyta.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-144">Find and select the order to edit.</span></span> <span data-ttu-id="cf0c6-145">Í valmyndinni neðst á síðunni er valið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-145">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="cf0c6-146">Taka til pöntun</span><span class="sxs-lookup"><span data-stu-id="cf0c6-146">Pick up an order</span></span>

1. <span data-ttu-id="cf0c6-147">Á heimasíðunni smellirðu á **Finna pöntun**.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-147">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="cf0c6-148">Velja pöntunina sem á að taka til.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-148">Select the order to pick up.</span></span> <span data-ttu-id="cf0c6-149">Í valmyndinni neðst á síðunni er valið **Tiltekt og pökkun**.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-149">At the bottom of the page, click **Picking and packing**.</span></span>
3. <span data-ttu-id="cf0c6-150">Smelltu á **Taka tiltaka til**.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-150">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="cf0c6-151">Hætta við pöntun</span><span class="sxs-lookup"><span data-stu-id="cf0c6-151">Cancel an order</span></span>

1. <span data-ttu-id="cf0c6-152">Á heimasíðunni smellirðu á **Finna pöntun**.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-152">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="cf0c6-153">Velja pöntunina sem á að hætta við.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-153">Select the order to cancel.</span></span> <span data-ttu-id="cf0c6-154">Í valmyndinni neðst á síðunni er valið **Hætta við**.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-154">At the bottom of the page, click **Cancel**.</span></span>

### <a name="create-a-return-order"></a><span data-ttu-id="cf0c6-155">Stofna skilapöntun</span><span class="sxs-lookup"><span data-stu-id="cf0c6-155">Create a return order</span></span>

1. <span data-ttu-id="cf0c6-156">Á heimasíðunni smellirðu á **Finna pöntun**.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-156">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="cf0c6-157">Velurðu pöntun til að skila, velurðu reikningur fyrir pöntun, og svo velurðu afurðarlínu fyrir varninginn til að skila.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-157">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3. <span data-ttu-id="cf0c6-158">Í valmyndinni neðst á síðunni er valið **Skilapöntun**.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-158">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="cf0c6-159">Ósamstillt færsluflæði fyrir pantanir viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="cf0c6-159">Asynchronous transaction flow for customer orders</span></span>

<span data-ttu-id="cf0c6-160">Hægt er að stofna pantanir viðskiptavinar úr biðlara sölustaðar (POS) í annaðhvort samstilltum eða ósamstilltum ham.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-160">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="cf0c6-161">Gera virkt að pantanir viðskiptavinar séu stofnaðar í ósamstilltum ham</span><span class="sxs-lookup"><span data-stu-id="cf0c6-161">Enable customer orders to be created in asynchronous mode</span></span>

1. <span data-ttu-id="cf0c6-162">Smelltu á **Retail og Commerce** &gt; **Uppsetning rásar** &gt; **Uppsetning sölustaðar** &gt; **Forstilling sölustaðar** &gt; **Virknireglur**.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-162">Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2. <span data-ttu-id="cf0c6-163">Á flipanum **Almennt** stillirðu valkostinn **Stofna viðskiptavinapöntun í ósamstilltri stillingu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-163">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="cf0c6-164">Þegar valkosturinn **Stofna pöntun viðskiptavinar í ósamstilltri stillingu** er stilltur á **Já** verða pantanir viðskiptavinar alltaf stofnaðar í ósamstilltri stillingu, jafnvel þó að Retail Transaction Service (RTS) er tiltækt.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-164">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="cf0c6-165">Ef þessi valkostur er stilltur á **Nei** verða pantanir viðskiptavinar alltaf stofnaðar í samstilltum ham með því að nota RTS.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-165">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="cf0c6-166">Þegar pantanir frá viðskiptavinum eru stofnaðar í ósamstilltum ham eru þær sóttar og settar inn í Commerce með P-vinnslum.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-166">When customer orders are created in asynchronous mode, they are pulled and inserted into Commerce by Pull (P) jobs.</span></span> <span data-ttu-id="cf0c6-167">Samsvarandi sölupantanir eru stofnaðar þegar **Samstilla pantanir** er keyrt annaðhvort handvirkt eða með runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="cf0c6-167">The corresponding sales orders are created when **Synchronize orders** is run either manually or through a batch process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf0c6-168">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="cf0c6-168">Additional resources</span></span>

[<span data-ttu-id="cf0c6-169">Blandaðar pantanir viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="cf0c6-169">Hybrid customer orders</span></span>](hybrid-customer-orders.md)