---
title: Greiðslueining
description: Þetta efnisatriði fjallar um greiðslueininguna og útskýrir hvernig á að skilgreina hana í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: f4f6baa3c4a42a2994cab772c98d373996e2648b
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661209"
---
# <a name="payment-module"></a><span data-ttu-id="30550-103">Greiðslueining</span><span class="sxs-lookup"><span data-stu-id="30550-103">Payment module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="30550-104">Þetta efnisatriði fjallar um greiðslueininguna og útskýrir hvernig á að skilgreina hana í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="30550-104">This topic covers the payment module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="30550-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="30550-105">Overview</span></span>

<span data-ttu-id="30550-106">Greiðslueiningin gerir viðskiptavinum kleift að greiða pantanir með kredit- eða debetkortum.</span><span class="sxs-lookup"><span data-stu-id="30550-106">The payment module lets customers pay for orders by using credit or debit cards.</span></span> <span data-ttu-id="30550-107">Greiðslusamþætting fyrir þessa eining er í boði greiðslutengils Dynamics 365 fyrir Adyen.</span><span class="sxs-lookup"><span data-stu-id="30550-107">Payment integration for this module is provided by the Dynamics 365 Payment Connector for Adyen.</span></span> <span data-ttu-id="30550-108">Frekari upplýsingar um hvernig setja á upp og skilgreina greiðslutengil er að finna í [Greiðslutengill Dynamics 365 fyrir Adyen](dev-itpro/adyen-connector.md).</span><span class="sxs-lookup"><span data-stu-id="30550-108">For more information about how to set up and configure the payment connector, see [Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md).</span></span>

<span data-ttu-id="30550-109">Greiðslueiningin hýsir greiðsluupplýsingar sem er miðlað í gegnum Adyen í innfelldum HTML-ramma (iframe).</span><span class="sxs-lookup"><span data-stu-id="30550-109">The payment module hosts the payment information that is served via Adyen in an HTML inline frame (iframe).</span></span> <span data-ttu-id="30550-110">Greiðslueiningin vinnur með Commerce Scale Unit til að sækja Adyen-greiðsluupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="30550-110">The payment module interacts with the Commerce Scale Unit to retrieve the Adyen payment information.</span></span> <span data-ttu-id="30550-111">Sem hluti af samvinnu Commerce Scale Unit, getur greiðslueiningin leyft upplýsingar um reikningsaðsetur að vera sett fram annaðhvort í iframe eða aðskilinni einingu.</span><span class="sxs-lookup"><span data-stu-id="30550-111">As part of the Commerce Scale Unit interaction, the payment module can allow billing address information to be served either in the iframe or as a separate module.</span></span> <span data-ttu-id="30550-112">Í Fabrikam-þemanu er reikningsaðsetrið sýnt í aðskilinni einingu.</span><span class="sxs-lookup"><span data-stu-id="30550-112">In the Fabrikam theme, the billing address is shown in a separate module.</span></span> <span data-ttu-id="30550-113">Þessi nálgun býður upp á meiri sveigjanleika fyrir sniðmótun, því að hægt er að sýna línur aðsetursins þannig að þær líkist línum afhendingaraðsetursins.</span><span class="sxs-lookup"><span data-stu-id="30550-113">This approach allows for more formatting flexibility, because the address lines can be rendered so that they resemble the lines of the shipping address.</span></span>

<span data-ttu-id="30550-114">Greiðslueiningin leyfir einnig innskráðum viðskiptavinum að vista greiðsluupplýsingarnar sínar.</span><span class="sxs-lookup"><span data-stu-id="30550-114">The payment module also lets signed-in customers save their payment information.</span></span> <span data-ttu-id="30550-115">Greiðsluupplýsingar og reikningsaðsetur eru vistuð og stjórnað í gegnum Adyen-greiðslutengilinn.</span><span class="sxs-lookup"><span data-stu-id="30550-115">The payment information and billing address are saved and managed via the Adyen payment connector.</span></span>

<span data-ttu-id="30550-116">Greiðslueiningin nær yfir öll pöntunargjöld sem vildarpunktar eða gjafakort ná ekki þegar yfir.</span><span class="sxs-lookup"><span data-stu-id="30550-116">The payment module covers any order charges that aren't already covered by loyalty points or a gift card.</span></span> <span data-ttu-id="30550-117">Ef samtala fyrir pöntun er að fullu dekkuð af vildarpunktum eða inneign gjafakorts, verður greiðslueiningin falin, og viðskiptavinurinn mun geta lagt inn pöntunina án hennar.</span><span class="sxs-lookup"><span data-stu-id="30550-117">If the total for an order is fully covered by loyalty points or gift card credits, the payment module will be hidden, and the customer will be able to place the order without it.</span></span>

<span data-ttu-id="30550-118">Adyen-greiðslutengillinn styður einnig öfluga sannvottun viðskiptavinar (SCA).</span><span class="sxs-lookup"><span data-stu-id="30550-118">The Adyen payment connector also supports strong customer authentication (SCA).</span></span> <span data-ttu-id="30550-119">Hluti af greiðsluþjónustutilskipun 2.0 (PSD2.0) Evrópusambandsins krefst þess að kaupendur á netinu verði auðkenndir utan umhverfis netverslunarinnar þegar þeir nota rafrænan greiðslumáta.</span><span class="sxs-lookup"><span data-stu-id="30550-119">Part of the European Union (EU) Payment Services Directive 2.0 (PSD2.0) requires that online shoppers be authenticated outside their online shopping experience when they use an electronic payment method.</span></span> <span data-ttu-id="30550-120">Meðan á greiðsluferlinu stendur, er viðskiptavinum vísað á bankaþjónustusvæðið þeirra.</span><span class="sxs-lookup"><span data-stu-id="30550-120">During the checkout flow,  customers are redirected to their banking site.</span></span> <span data-ttu-id="30550-121">Eftir sannvottun er þeim beint aftur í greiðsluferli Commerce.</span><span class="sxs-lookup"><span data-stu-id="30550-121">Then, after authentication, they are redirected back to the Commerce checkout flow.</span></span> <span data-ttu-id="30550-122">Á meðan á þessari framsendingu stendur verða upplýsingar sem viðskiptavinur færði inn í greiðsluferlið (til dæmis sendingaraðsetur, afhendingarvalkostir, upplýsingar um gjafakort og vildarupplýsingar) haldið við.</span><span class="sxs-lookup"><span data-stu-id="30550-122">During this redirection, the information that a customer entered in the checkout flow (for example, the shipping address, delivery options, gift card information, and loyalty information) will persist.</span></span> <span data-ttu-id="30550-123">Áður en hægt er að kveikja á þessum eiginleika verður að skilgreina greiðslutengilinn fyrir öfluga sannvottun viðskiptavinar í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="30550-123">Before you can turn on this feature, the payment connector must be configured for SCA in Commerce headquarters.</span></span> <span data-ttu-id="30550-124">Frekari upplýsingar er að finna í [Öflug sannvottun viðskiptavinar með Adyen](adyen_redirect.md).</span><span class="sxs-lookup"><span data-stu-id="30550-124">For more information, see [Strong Customer Authentication using Adyen](adyen_redirect.md).</span></span>

<span data-ttu-id="30550-125">Eftirfarandi skýringarmynd sýnir dæmi um einingar gjafakorts, vildarpunkta og greiðslu á greiðsluferlissíðu.</span><span class="sxs-lookup"><span data-stu-id="30550-125">The following illustration shows an example of gift card, loyalty, and payment modules on a checkout page.</span></span>

![Dæmi um gjafakort, vildarpunkta og greiðslueiningar á greiðsluferlissíðu](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a><span data-ttu-id="30550-127">Eiginleikar greiðslueiningar</span><span class="sxs-lookup"><span data-stu-id="30550-127">Payment module properties</span></span>

| <span data-ttu-id="30550-128">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="30550-128">Property name</span></span> | <span data-ttu-id="30550-129">Gildi</span><span class="sxs-lookup"><span data-stu-id="30550-129">Values</span></span> | <span data-ttu-id="30550-130">lýsing</span><span class="sxs-lookup"><span data-stu-id="30550-130">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="30550-131">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="30550-131">Heading</span></span> | <span data-ttu-id="30550-132">Fyrirsagnartexti</span><span class="sxs-lookup"><span data-stu-id="30550-132">Heading text</span></span> | <span data-ttu-id="30550-133">Valfrjáls fyrirsögn fyrir greiðslueininguna.</span><span class="sxs-lookup"><span data-stu-id="30550-133">An optional heading for the payment module.</span></span> |
| <span data-ttu-id="30550-134">Hæð iFrame</span><span class="sxs-lookup"><span data-stu-id="30550-134">Height of the iframe</span></span> | <span data-ttu-id="30550-135">Dílar</span><span class="sxs-lookup"><span data-stu-id="30550-135">Pixels</span></span> | <span data-ttu-id="30550-136">Hæð iframe í dílum.</span><span class="sxs-lookup"><span data-stu-id="30550-136">The iframe height, in pixels.</span></span> <span data-ttu-id="30550-137">Hægt er að stilla hæðina eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="30550-137">The height can be adjusted as required.</span></span> |
| <span data-ttu-id="30550-138">Sýna greiðsluaðsetur</span><span class="sxs-lookup"><span data-stu-id="30550-138">Show billing address</span></span> | <span data-ttu-id="30550-139">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="30550-139">**True** or **False**</span></span> | <span data-ttu-id="30550-140">Ef þessi eiginleiki er stilltur á **Satt** verður reikningsaðsetrið lagt fram af Adyen innan iframe greiðslueiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="30550-140">If this property is set to **True**, the billing address will be served by Adyen inside the payment module iframe.</span></span> <span data-ttu-id="30550-141">Ef hann er stilltur á **Ósatt** verður reikningsaðsetrið ekki lagt fram af Adyen og notandi Commerce verður að skilgreina einingu til að sýna reikningsaðsetrið greiðsluferlissíðunni.</span><span class="sxs-lookup"><span data-stu-id="30550-141">If it's set to **False**, the billing address won't be served by Adyen, and a Commerce user will have to configure a module to show the billing address on the checkout page.</span></span> |
| <span data-ttu-id="30550-142">Hnekkja greiðslustíl</span><span class="sxs-lookup"><span data-stu-id="30550-142">Payment style override</span></span> | <span data-ttu-id="30550-143">Kóði fyrir stölluð stílblöð (CSS)</span><span class="sxs-lookup"><span data-stu-id="30550-143">Cascading Style Sheets (CSS) code</span></span> | <span data-ttu-id="30550-144">Vegna þess að greiðslueiningin er hýst í iframe, er takmarkaður möguleiki á stílmótun.</span><span class="sxs-lookup"><span data-stu-id="30550-144">Because the payment module is hosted in an iframe, there is limited styling capability.</span></span> <span data-ttu-id="30550-145">Hægt er að ná einhverri stílmótun með því að nota þennan eiginleika.</span><span class="sxs-lookup"><span data-stu-id="30550-145">You can achieve some styling by using this property.</span></span> <span data-ttu-id="30550-146">Til að hnekkja stílbrigðum svæðis þarf að líma CSS-kóðann inn sem gildið fyrir þennan eiginleika.</span><span class="sxs-lookup"><span data-stu-id="30550-146">To override site styles, you must paste the CSS code as the value of this property.</span></span> <span data-ttu-id="30550-147">Hnekkingar og stílbrigði CSS-svæðissmiðs eiga ekki við um þessa einingu.</span><span class="sxs-lookup"><span data-stu-id="30550-147">Site builder CSS overrides and styles don't apply to this module.</span></span> |

## <a name="billing-address"></a><span data-ttu-id="30550-148">Póstfang greiðanda</span><span class="sxs-lookup"><span data-stu-id="30550-148">Billing address</span></span>

<span data-ttu-id="30550-149">Greiðslueiningin gerir viðskiptavinum kleift að bjóða upp á reikningsaðsetur vegna greiðsluupplýsinganna.</span><span class="sxs-lookup"><span data-stu-id="30550-149">The payment module lets customers provide a billing address for their payment information.</span></span> <span data-ttu-id="30550-150">Hún gerir þeim einnig kleift að nota sendingaraðsetur sitt sem reikningsaðsetur, til að gera greiðsluferlið auðveldara og fljótlegra.</span><span class="sxs-lookup"><span data-stu-id="30550-150">It also lets them  use their shipping address as the billing address, to make the checkout flow easier and faster.</span></span> <span data-ttu-id="30550-151">Ef eiginleikinn **Sýna reikningsaðsetur** er stilltur á **Ósatt** ætti að skilgreina greiðslueininguna á greiðsluferlissíðunni.</span><span class="sxs-lookup"><span data-stu-id="30550-151">If the **Show billing address** property is set to **False**, the payment module should be configured on the checkout page.</span></span>

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="30550-152">Bæta greiðslueiningu við greiðsluferlissíðu og stilla nauðsynlega eiginleika</span><span class="sxs-lookup"><span data-stu-id="30550-152">Add a payment module to a checkout page and set the required properties</span></span>

<span data-ttu-id="30550-153">Aðeins er hægt að bæta greiðslueiningu við greiðsluferliseiningu.</span><span class="sxs-lookup"><span data-stu-id="30550-153">A payment module can be added only to a checkout module.</span></span> <span data-ttu-id="30550-154">Frekari upplýsingar um hvernig á að skilgreina greiðslueiningu fyrir greiðsluferlissíðu er að finna í [Greiðsluferliseining](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="30550-154">For more information about how to configure a payment module for a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30550-155">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="30550-155">Additional resources</span></span>

[<span data-ttu-id="30550-156">Körfueining</span><span class="sxs-lookup"><span data-stu-id="30550-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="30550-157">Körfutáknseining</span><span class="sxs-lookup"><span data-stu-id="30550-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="30550-158">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="30550-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="30550-159">Eining sendingaraðseturs</span><span class="sxs-lookup"><span data-stu-id="30550-159">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="30550-160">Eining afhendingarvalkosta</span><span class="sxs-lookup"><span data-stu-id="30550-160">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="30550-161">Pöntunarupplýsingaeining</span><span class="sxs-lookup"><span data-stu-id="30550-161">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="30550-162">Gjafakortseining</span><span class="sxs-lookup"><span data-stu-id="30550-162">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="30550-163">Dynamics 365-greiðslutengill fyrir Adyen</span><span class="sxs-lookup"><span data-stu-id="30550-163">Dynamics 365 Payment Connector for Adyen</span></span>](dev-itpro/adyen-connector.md)

[<span data-ttu-id="30550-164">Öflug sannvottun viðskiptavinar með Adyen</span><span class="sxs-lookup"><span data-stu-id="30550-164">Strong Customer Authentication using Adyen</span></span>](adyen_redirect.md)
