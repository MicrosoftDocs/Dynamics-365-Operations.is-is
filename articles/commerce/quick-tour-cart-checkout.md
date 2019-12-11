---
title: Yfirlit yfir síður körfu og greiðsluferlis
description: Þetta efnisatriði veitir yfirlit yfir körfu- og greiðslusíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 347db3af36521e11dc70d5188dcc54b07efa1fbe
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697843"
---
# <a name="overview-of-cart-and-checkout-pages"></a><span data-ttu-id="dad01-103">Yfirlit yfir síður körfu og greiðsluferlis</span><span class="sxs-lookup"><span data-stu-id="dad01-103">Overview of cart and checkout pages</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="dad01-104">Þetta efnisatriði veitir yfirlit yfir körfu- og greiðslusíður í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dad01-104">This topic provides an overview of the cart and checkout pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="dad01-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="dad01-105">Overview</span></span>

<span data-ttu-id="dad01-106">Körfusíðan á vef netverslunar sýnir alla hluti sem viðskiptavinur hefur bætt við körfuna.</span><span class="sxs-lookup"><span data-stu-id="dad01-106">The cart page of an e-Commerce website shows all items that a customer has added to the cart.</span></span> <span data-ttu-id="dad01-107">Körfusíðan er smíðuð með því að nota körfueininguna.</span><span class="sxs-lookup"><span data-stu-id="dad01-107">The cart page is built by using the cart module.</span></span> <span data-ttu-id="dad01-108">Körfueiningin er gámur sem er hýsir allar einingar sem þarf til að sýna hluti sem eru í körfunni.</span><span class="sxs-lookup"><span data-stu-id="dad01-108">The cart module is a container that hosts all the modules that are required to showcase items in the cart.</span></span> <span data-ttu-id="dad01-109">Körfueiningin getur einnig notað aðrar einingar til að sýna pöntunaryfirlitið og alla kynningarkóða sem hefur verið beitt á pöntun viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="dad01-109">The cart module can also use other modules to show the order summary and any promotional codes that have been applied to the customer order.</span></span>

<span data-ttu-id="dad01-110">Greiðslusíðan á vefsíðu netverslunar sýnir skref fyrir skref sem viðskiptavinir fylgja til að færa inn allar upplýsingar sem þarf til að setja inn pöntun.</span><span class="sxs-lookup"><span data-stu-id="dad01-110">The checkout page of an e-Commerce website presents a step-by-step flow that customers follow to enter all the information that is required to place an order.</span></span> <span data-ttu-id="dad01-111">Greiðsluferliseining getur innihaldið einingar sem sjá um póstfang, sendingaraðferðir, innheimtuupplýsingar, pöntunaryfirlit og aðrar upplýsingar sem tengjast pantanir viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="dad01-111">A checkout module can include modules that handle the shipping address, shipping methods, billing information, order summary, and other information that is related to customer orders.</span></span>

## <a name="cart-page"></a><span data-ttu-id="dad01-112">Körfusíða</span><span class="sxs-lookup"><span data-stu-id="dad01-112">Cart page</span></span>

<span data-ttu-id="dad01-113">Körfusíðan virkar sem innkaupapokinn og inniheldur alla hluti sem hafa verið settir í körfuna.</span><span class="sxs-lookup"><span data-stu-id="dad01-113">The cart page serves as the shopping bag and includes all the items that have been added to the cart.</span></span>

<span data-ttu-id="dad01-114">Eftirfarandi mynd sýnir dæmi um körfusíðu sem var smíðuð með því að nota byrjunarbúnaðinn á netinu og „Fabrikam“ þemað.</span><span class="sxs-lookup"><span data-stu-id="dad01-114">The following illustration show an example of a cart page that was built by using the online starter kit and the "Fabrikam" theme.</span></span>

![Dæmi um körfusíðu](./media/cart2.PNG)

<span data-ttu-id="dad01-116">Meginhlutinn af körfusíðunni sýnir hluti sem viðskiptavinur hefur bætt við körfuna.</span><span class="sxs-lookup"><span data-stu-id="dad01-116">The main body of the cart page shows all the items that the customer has added to the cart.</span></span> <span data-ttu-id="dad01-117">Allur viðeigandi afsláttur er sýndur.</span><span class="sxs-lookup"><span data-stu-id="dad01-117">All applicable discounts are showcased.</span></span> <span data-ttu-id="dad01-118">Þessir afslættir innihalda flókna afslátt.</span><span class="sxs-lookup"><span data-stu-id="dad01-118">These discounts include complex discounts.</span></span> <span data-ttu-id="dad01-119">Sem dæmi má nefna „Kauptu 3 hluti og fáðu 10% afslátt“ eða „Kauptu flösku og bakpoka til að fá 10% afslátt.“</span><span class="sxs-lookup"><span data-stu-id="dad01-119">Examples include "Buy 3 items and get 10% off" or "Buy a bottle and a backpack to get 10% off."</span></span> <span data-ttu-id="dad01-120">Pöntunarsamantektareiningin sýnir upphæðina sem er gjaldfærð eftir að afslætti, flutningum, sköttum og svo framvegis hefur verið beitt.</span><span class="sxs-lookup"><span data-stu-id="dad01-120">The order summary module shows the amount that is due after discounts, shipping, taxes, and so on, have been applied.</span></span> <span data-ttu-id="dad01-121">Það er einnig til kynningarkóðaeining sem gerir viðskiptavininum kleift að beita eða fjarlægja kynningarkóða.</span><span class="sxs-lookup"><span data-stu-id="dad01-121">There is also a promo code module that lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="dad01-122">Viðskiptavinur getur verslað nafnlaust eða sem innskráður notandi.</span><span class="sxs-lookup"><span data-stu-id="dad01-122">A customer can shop anonymously or as a signed-in user.</span></span> <span data-ttu-id="dad01-123">Ef viðskiptavinur er skráður inn eru hlutir í körfunni varðveittir milli seta.</span><span class="sxs-lookup"><span data-stu-id="dad01-123">If a customer is signed in, items in the cart are preserved between sessions.</span></span> <span data-ttu-id="dad01-124">Á þennan hátt getur viðskiptavinurinn haldið áfram að versla úr mörgum tækjum.</span><span class="sxs-lookup"><span data-stu-id="dad01-124">In this way, the customer can continue to shop from multiple devices.</span></span>

<span data-ttu-id="dad01-125">Úr körfunni getur viðskiptavinurinn haldið áfram í greiðsluferli.</span><span class="sxs-lookup"><span data-stu-id="dad01-125">From the cart, the customer can proceed to checkout.</span></span> <span data-ttu-id="dad01-126">Viðskiptavinur getur hafið greiðsluferli sem gestanotandi eða sem innskráður notandi.</span><span class="sxs-lookup"><span data-stu-id="dad01-126">A customer can initiate checkout as a guest user or as a signed-in user.</span></span>

<span data-ttu-id="dad01-127">Sjá upplýsingar um hvernig á að skrifa körfusíðu [Bæta körfueiningu við síðu](add-cart-module.md).</span><span class="sxs-lookup"><span data-stu-id="dad01-127">For information about how to author a cart page, see [Add a cart module to a page](add-cart-module.md).</span></span>

## <a name="checkout-page"></a><span data-ttu-id="dad01-128">Greiðslusíða</span><span class="sxs-lookup"><span data-stu-id="dad01-128">Checkout page</span></span>

<span data-ttu-id="dad01-129">Greiðslusíðan er þar sem viðskiptavinir slá inn upplýsingarnar sem þarf til að setja pöntun.</span><span class="sxs-lookup"><span data-stu-id="dad01-129">The checkout page is where customers enter the information that is required to place an order.</span></span>

<span data-ttu-id="dad01-130">Eftirfarandi mynd sýnir dæmi um greiðslusíðu sem var smíðuð með því að nota byrjunarbúnaðinn á netinu.</span><span class="sxs-lookup"><span data-stu-id="dad01-130">The following illustration show an example of a checkout page that was built by using the online starter kit.</span></span>

![Dæmi um greiðslusíðu](./media/Checkout.PNG)

<span data-ttu-id="dad01-132">Meginhluti greiðslusíðunnar er þar sem öllum pöntunarupplýsingum er safnað.</span><span class="sxs-lookup"><span data-stu-id="dad01-132">The main body of the checkout page is where all the order information is collected.</span></span> <span data-ttu-id="dad01-133">Þessar upplýsingar fela í sér póstfang, afhendingarmöguleika og greiðsluupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="dad01-133">This information includes the shipping address, delivery options, and payment information.</span></span> <span data-ttu-id="dad01-134">Kassi hefur skref fyrir skref flæði, vegna þess að upplýsingarnar verða að vera færðar í ákveðna röð til að vinna úr.</span><span class="sxs-lookup"><span data-stu-id="dad01-134">Checkout has a step-by-step flow, because the information must be entered in a specific order to be processed.</span></span> <span data-ttu-id="dad01-135">Til dæmis verður að færa inn flutningsfangið áður en hægt er að reikna út flutningskostnaðinn og heimila greiðsluna.</span><span class="sxs-lookup"><span data-stu-id="dad01-135">For example, the shipping address must be entered before the shipping costs can be calculated and the payment can be authorized.</span></span>

### <a name="shipping-address"></a><span data-ttu-id="dad01-136">Aðsetur sendingar</span><span class="sxs-lookup"><span data-stu-id="dad01-136">Shipping address</span></span>

<span data-ttu-id="dad01-137">Sendingar heimilisfang er krafist ef hlutir verða að vera sendir.</span><span class="sxs-lookup"><span data-stu-id="dad01-137">A shipping address is required if items must be shipped.</span></span> <span data-ttu-id="dad01-138">Hægt er að stilla snið sendingarföngs fyrir hvert land í Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="dad01-138">The format of shipping addresses for each locale can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="dad01-139">Til dæmis, ef hlutirnir verða fluttir til Bandaríkjanna, verður flutningsfangið að innihalda götuheiti, ástand og póstnúmer.</span><span class="sxs-lookup"><span data-stu-id="dad01-139">For example, if the items will be shipped to the United States, the shipping address must include a street address, state, and ZIP Code.</span></span> <span data-ttu-id="dad01-140">Nokkur grunninntaksprófun er gerð fyrir sendingarfangareiti, svo sem staðfestingu á stafrófsröddum, hámarkslengd og tölur.</span><span class="sxs-lookup"><span data-stu-id="dad01-140">Some basic input validation is done for shipping address fields, such as validation for alphanumeric characters, maximum length, and numbers.</span></span> <span data-ttu-id="dad01-141">Þótt réttmæti heimilisfangsins sjálfs sé ekki staðfest, er hægt að gera þessa staðfestingu með því að nota sérsniðna þjónustu þriðja aðila.</span><span class="sxs-lookup"><span data-stu-id="dad01-141">Although the validity of the address itself isn't verified, this verification can be done by using customized third-party services.</span></span>

<span data-ttu-id="dad01-142">Póstfangið er notað á alla hluti í körfunni sem „skipið“ er valinn fyrir.</span><span class="sxs-lookup"><span data-stu-id="dad01-142">The shipping address is applied to all items in the cart that the "ship" option is selected for.</span></span> <span data-ttu-id="dad01-143">Ef þú notar stöðvunarrennslið sem er að finna í byrjunarbúnaðinum á netinu er ekki hægt að senda einstaka körfuhluti á mismunandi netföng.</span><span class="sxs-lookup"><span data-stu-id="dad01-143">If you use the checkout flow that is provided in the online starter kit, individual cart items can't be shipped to different addresses.</span></span> <span data-ttu-id="dad01-144">Ef þú þarft þessa hæfileika er hægt að útfæra hana með því að aðlaga kassaeiningarnar.</span><span class="sxs-lookup"><span data-stu-id="dad01-144">If you require this capability, it can be implemented through customization of the checkout modules.</span></span>

<span data-ttu-id="dad01-145">Eftir að sendingarfangið hefur verið gefið upp eru sendingaraðferðir sem fáanlegar eru frá Dynamics 365 Commerce netverslun er sýnd.</span><span class="sxs-lookup"><span data-stu-id="dad01-145">After the shipping address is provided, the shipping methods that are available from the Dynamics 365 Commerce online store are shown.</span></span> <span data-ttu-id="dad01-146">Hægt er að stilla sendingaraðferðirnar og netföngin sem þeir styðja í smásölu.</span><span class="sxs-lookup"><span data-stu-id="dad01-146">The shipping methods and the addresses that they support can be configured in Retail.</span></span>

### <a name="payment"></a><span data-ttu-id="dad01-147">Greiðsla</span><span class="sxs-lookup"><span data-stu-id="dad01-147">Payment</span></span>

<span data-ttu-id="dad01-148">Næsta skref í greiðsluflæðinu er greiðsla.</span><span class="sxs-lookup"><span data-stu-id="dad01-148">The next step in the checkout flow is payment.</span></span> <span data-ttu-id="dad01-149">Í rafrænum viðskiptum er hægt að nota margar greiðslumáta til að setja inn pantanir, svo sem kreditkort, gjafakort og vildarpunkta.</span><span class="sxs-lookup"><span data-stu-id="dad01-149">In e-Commerce, multiple methods of payment can be used to place orders, such as credit cards, gift cards, and loyalty points.</span></span> <span data-ttu-id="dad01-150">Einnig er hægt að nota sambland af þessum greiðslumátum.</span><span class="sxs-lookup"><span data-stu-id="dad01-150">A combination of these payment methods can also be used.</span></span> <span data-ttu-id="dad01-151">Það fer eftir greiðslumáta sem notaður er, viðbótarupplýsingar gætu verið nauðsynlegar.</span><span class="sxs-lookup"><span data-stu-id="dad01-151">Depending on the payment methods that are used, additional information might be required.</span></span> <span data-ttu-id="dad01-152">Til dæmis krefst greiðslu með kreditkorti greiðslu heimilisfang.</span><span class="sxs-lookup"><span data-stu-id="dad01-152">For example, a credit card payment requires a billing address.</span></span> <span data-ttu-id="dad01-153">Greiðslur með kreditkortum eru unnar með því að nota Adyen Payment Connector.</span><span class="sxs-lookup"><span data-stu-id="dad01-153">Credit card payments are processed by using the Adyen Payment Connector.</span></span>

#### <a name="loyalty-points"></a><span data-ttu-id="dad01-154">Vildarpunktar</span><span class="sxs-lookup"><span data-stu-id="dad01-154">Loyalty points</span></span>

<span data-ttu-id="dad01-155">Í greiðsluferlisflæðinu getur viðskiptavinur sem er meðlimur í vildarforriti og hefur safnað vildarpunkta innleyst þá vildarpunkta fyrir pöntun.</span><span class="sxs-lookup"><span data-stu-id="dad01-155">During the checkout flow, a customer who is a member of a loyalty program and who has accrued loyalty points can redeem those loyalty points for an order.</span></span> <span data-ttu-id="dad01-156">Vildarpunktaeiningin er aðeins sýnd ef viðskiptavinurinn er með núverandi vildaraðild.</span><span class="sxs-lookup"><span data-stu-id="dad01-156">The loyalty points module is shown only if the customer has an existing loyalty membership.</span></span> <span data-ttu-id="dad01-157">Fyrir notendur sem ekki eru meðlimir og gestir er þessi eining falin.</span><span class="sxs-lookup"><span data-stu-id="dad01-157">For non-members and guest users, this module is hidden.</span></span>

#### <a name="gift-cards"></a><span data-ttu-id="dad01-158">Gjafakort</span><span class="sxs-lookup"><span data-stu-id="dad01-158">Gift cards</span></span>

<span data-ttu-id="dad01-159">Byrjunareiningin á netinu gerir kleift að hægt sé að innleysa alþjóðleg gjafakort fyrir pöntun.</span><span class="sxs-lookup"><span data-stu-id="dad01-159">The online starter kit lets internal gift cards be redeemed for an order.</span></span> <span data-ttu-id="dad01-160">Til að nota innra gjafakort verður viðskiptavinurinn að vera skráður inn.</span><span class="sxs-lookup"><span data-stu-id="dad01-160">To apply an internal gift card, the customer must be signed in.</span></span> <span data-ttu-id="dad01-161">Til að auka öryggi mælum við með því að þú sérsniðir flæðið með því að nota persónuauðkenni fyrir innri gjafakort.</span><span class="sxs-lookup"><span data-stu-id="dad01-161">For additional security, we recommend that you customize the flow by using a personal identification number (PIN) for internal gift cards.</span></span>

### <a name="signed-in-and-guest-users"></a><span data-ttu-id="dad01-162">Innskráðir og gestir notendur</span><span class="sxs-lookup"><span data-stu-id="dad01-162">Signed-in and guest users</span></span>

<span data-ttu-id="dad01-163">Viðskiptavinur getur lokið greiðsluferli sem gestanotandi eða sem innskráður notandi.</span><span class="sxs-lookup"><span data-stu-id="dad01-163">The customer can complete the checkout process as a guest user or a signed-in user.</span></span> <span data-ttu-id="dad01-164">Ef viðskiptavinurinn skráir sig inn eru reikningsupplýsingar eins og vistaðar sendingarföng og vistaðar kreditkortaupplýsingar sjálfkrafa sóttar.</span><span class="sxs-lookup"><span data-stu-id="dad01-164">If the customer signs in, account information such as saved shipping addresses and saved credit card details is automatically retrieved.</span></span>

### <a name="order-summary"></a><span data-ttu-id="dad01-165">Samantekt pöntunar</span><span class="sxs-lookup"><span data-stu-id="dad01-165">Order summary</span></span>

<span data-ttu-id="dad01-166">Afgreiðsla sýnir yfirlit yfir línuritin í körfunni, svo að viðskiptavinurinn geti staðfest pöntunina áður en hann eða hún leggur hana fram.</span><span class="sxs-lookup"><span data-stu-id="dad01-166">Checkout shows a summary of the line items in the cart, so that the customer can verify the order before he or she places it.</span></span> <span data-ttu-id="dad01-167">Ekki er hægt að breyta línum atriðunum meðan á greiðsluferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="dad01-167">The line items can't be edited during the checkout flow.</span></span> <span data-ttu-id="dad01-168">Hins vegar er tengill á körfuna til staðar ef notandinn vill fara til baka og breyta línuliðum.</span><span class="sxs-lookup"><span data-stu-id="dad01-168">However, a link to the cart is provided in case the user wants to go back and edit line items.</span></span>

<span data-ttu-id="dad01-169">Eftir að viðskiptavinurinn hefur sent frá sér sendingar- og innheimtuupplýsingar endurspeglar pöntunaryfirlitið þá upphæð sem er gjaldfærð eftir að vildarpunkta, gjafakort og aðrar greiðslur hefur verið beitt.</span><span class="sxs-lookup"><span data-stu-id="dad01-169">After the customer provides shipping and billing information, the order summary reflects the amount that is due after loyalty points, gift cards, and other payments have been applied.</span></span>

### <a name="order-confirmation-and-email"></a><span data-ttu-id="dad01-170">Pöntunarstaðfesting og tölvupóstur</span><span class="sxs-lookup"><span data-stu-id="dad01-170">Order confirmation and email</span></span>

<span data-ttu-id="dad01-171">Þegar viðskiptavinurinn leggur inn pöntun er staðfestingarnúmer gefið upp.</span><span class="sxs-lookup"><span data-stu-id="dad01-171">When the customer places an order, a confirmation number is provided.</span></span> <span data-ttu-id="dad01-172">Á þessum tímapunkti hefur greiðslan verið heimiluð en ekki gjaldfærð.</span><span class="sxs-lookup"><span data-stu-id="dad01-172">At this point, the payment has been authorized but not charged.</span></span> <span data-ttu-id="dad01-173">Greiðslan verður aðeins gjaldfærð þegar pöntuninni er fullnægt (það er að segja þegar hún er annaðhvort send eða sótt).</span><span class="sxs-lookup"><span data-stu-id="dad01-173">The payment will be charged only when the order is fulfilled (that is, when it's either shipped or picked up).</span></span>

<span data-ttu-id="dad01-174">Eftir að pöntun er búin til, er tölvupóstur til staðfestingar pöntunar sendur til viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="dad01-174">After an order is created, an order confirmation email is sent to the customer.</span></span>

<span data-ttu-id="dad01-175">Nánari upplýsingar um hvernig á að skrifa greiðsluferlissíðu er að finna á [Bæta greiðsluferliseiningu við síðu](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="dad01-175">For more information about how to author a checkout page, see [Add a checkout module to a page](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dad01-176">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="dad01-176">Additional resources</span></span>

[<span data-ttu-id="dad01-177">Yfirlit yfir heimasíðuna</span><span class="sxs-lookup"><span data-stu-id="dad01-177">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="dad01-178">Yfirlit sjálfgefinnar lendingarsíðu flokks og leitarniðurstöðusíðu</span><span class="sxs-lookup"><span data-stu-id="dad01-178">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="dad01-179">Yfirlit yfir upplýsingasíður afurðar</span><span class="sxs-lookup"><span data-stu-id="dad01-179">Overview of product details pages</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="dad01-180">Yfirlit yfir síður reikningastjórnunar</span><span class="sxs-lookup"><span data-stu-id="dad01-180">Overview of account management pages</span></span>](quick-tour-account-management.md)
