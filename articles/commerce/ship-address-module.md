---
title: Eining sendingaraðseturs
description: Þetta efnisatriði fjallar um einingu sendingaraðseturs og útskýrir hvernig á að skilgreina hana í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e590c966ca6bd8111df5f91cbac0485afaa45c78
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234414"
---
# <a name="shipping-address-module"></a><span data-ttu-id="1dc40-103">Sendingaraðseturseining</span><span class="sxs-lookup"><span data-stu-id="1dc40-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1dc40-104">Þetta efnisatriði lýsir einingu sendingaraðseturs og útskýrir hvernig á að skilgreina hana í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1dc40-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1dc40-105">Einingin fyrir sendingaraðsetur gerir viðskiptavinum kleift að bæta við eða velja sendingaraðsetur fyrir pöntun meðan á greiðsluferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="1dc40-105">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="1dc40-106">Ef viðskiptavinur er skráður inn eru öll aðsetur sem áður voru vistuð fyrir þennan viðskiptavin sýnd og viðskiptavinurinn getur valið á milli þeirra.</span><span class="sxs-lookup"><span data-stu-id="1dc40-106">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="1dc40-107">Viðskiptavinurinn getur einnig bætt við nýju heimilisfangi.</span><span class="sxs-lookup"><span data-stu-id="1dc40-107">The customer can also add a new address.</span></span> <span data-ttu-id="1dc40-108">Einingin fyrir sendingaraðsetur er notuð fyrir allar vörur í pöntun sem krefjast sendingar.</span><span class="sxs-lookup"><span data-stu-id="1dc40-108">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="1dc40-109">Hægt er að skilgreina snið sendingaraðseturs í Commerce Headquarters fyrir hvert land eða svæði og eining sendingaraðseturs framfylgir þá reglum fyrir tiltekið land/svæði.</span><span class="sxs-lookup"><span data-stu-id="1dc40-109">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="1dc40-110">Þegar viðskiptavinir færa inn sendingaraðsetur í greiðsluferlinu, hafa þeir val um að vista aðsetrið sem aðalaðsetur.</span><span class="sxs-lookup"><span data-stu-id="1dc40-110">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="1dc40-111">Þessi valkostur er aðeins sýndur ef viðskiptavinur er skráður inn.</span><span class="sxs-lookup"><span data-stu-id="1dc40-111">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="1dc40-112">Þótt einingin fyrir sendingaraðsetur veiti ekki staðfestingu á aðsetri, er hægt að innleiða þessa virkni í gegnum sérstillingu.</span><span class="sxs-lookup"><span data-stu-id="1dc40-112">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="1dc40-113">Eftirfarandi mynd sýnir dæmi um nýja einingu sendingaraðseturs á greiðsluferlissíðu.</span><span class="sxs-lookup"><span data-stu-id="1dc40-113">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Dæmi um einingu sendingaraðseturs á greiðsluferlissíðu](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="1dc40-115">Eiginleikar einingar</span><span class="sxs-lookup"><span data-stu-id="1dc40-115">Module properties</span></span>

| <span data-ttu-id="1dc40-116">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="1dc40-116">Property name</span></span> | <span data-ttu-id="1dc40-117">Gildi</span><span class="sxs-lookup"><span data-stu-id="1dc40-117">Values</span></span> | <span data-ttu-id="1dc40-118">lýsing</span><span class="sxs-lookup"><span data-stu-id="1dc40-118">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="1dc40-119">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="1dc40-119">Heading</span></span> | <span data-ttu-id="1dc40-120">Fyrirsagnartexti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**)</span><span class="sxs-lookup"><span data-stu-id="1dc40-120">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="1dc40-121">Valfrjáls fyrirsögn fyrir einingu sendingaraðseturs.</span><span class="sxs-lookup"><span data-stu-id="1dc40-121">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="1dc40-122">Sýna aðsetursgerð</span><span class="sxs-lookup"><span data-stu-id="1dc40-122">Show address type</span></span> | <span data-ttu-id="1dc40-123">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="1dc40-123">**True** or **False**</span></span> | <span data-ttu-id="1dc40-124">Ef þessi valfrjálsi eiginleiki er stilltur á **Satt**, verður gerð aðseturs, t.d. **Heimili** eða **Fyrirtæki** sýnt.</span><span class="sxs-lookup"><span data-stu-id="1dc40-124">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="1dc40-125">Ef engin aðsetursgerð er tilgreind verður aðsetrið sjálfkrafa vistað sem **Gerð**=**Annað**.</span><span class="sxs-lookup"><span data-stu-id="1dc40-125">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |
| <span data-ttu-id="1dc40-126">Kveikja á sjálfvirkum tillögum</span><span class="sxs-lookup"><span data-stu-id="1dc40-126">Enable auto suggestion</span></span>| <span data-ttu-id="1dc40-127">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="1dc40-127">**True** or **False**</span></span> | <span data-ttu-id="1dc40-128">Ef þessi valfrjálsa eiginleiki er stilltur á **Satt** verða tillögur að sjálfvirkum aðsetrum veittar.</span><span class="sxs-lookup"><span data-stu-id="1dc40-128">If this optional property is set to **True**, automatic address suggestions will be provided.</span></span> <span data-ttu-id="1dc40-129">Þessar tillögur eru knúnar af Bing-kortum.</span><span class="sxs-lookup"><span data-stu-id="1dc40-129">These suggestions are powered by Bing Maps.</span></span> <span data-ttu-id="1dc40-130">Frekari upplýsingar um hvernig setja á upp samþættingu Bing-korta á svæðinu er að finna í [Verslunarvalseining](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="1dc40-130">For information about how to set up Bing Maps integration for your site, see [Store selector module](store-selector.md).</span></span> <span data-ttu-id="1dc40-131">Þessi eiginleiki er í boði frá og með Commerce útgáfu 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="1dc40-131">This feature is available as of the Commerce version 10.0.15 release.</span></span>|
|<span data-ttu-id="1dc40-132">Valkostir fyrir sjálfvirkar tillögur</span><span class="sxs-lookup"><span data-stu-id="1dc40-132">Auto suggest options</span></span>| <span data-ttu-id="1dc40-133">Númer</span><span class="sxs-lookup"><span data-stu-id="1dc40-133">A number</span></span>| <span data-ttu-id="1dc40-134">Ef sjálfvirkar aðseturstillögur eru virkar er hægt að tilgreina frekari valmöguleika, svo sem hámarksfjölda tillagna sem ætti að gefa upp.</span><span class="sxs-lookup"><span data-stu-id="1dc40-134">If automatic address suggestions are enabled, you can specify additional options, such as the maximum number of suggestions that should be provided.</span></span>|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="1dc40-135">Bæta einingu sendingaraðseturs við greiðsluferlissíðu og stilla nauðsynlega eiginleika</span><span class="sxs-lookup"><span data-stu-id="1dc40-135">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="1dc40-136">Aðeins er hægt að bæta einingu sendingaraðseturs við greiðsluferliseiningu.</span><span class="sxs-lookup"><span data-stu-id="1dc40-136">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="1dc40-137">Frekari upplýsingar um hvernig skilgreina á einingu sendingaraðseturs og bæta henni við greiðsluferlissíðu er að finna í [Greiðsluferliseining](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="1dc40-137">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1dc40-138">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="1dc40-138">Additional resources</span></span>

[<span data-ttu-id="1dc40-139">Körfueining</span><span class="sxs-lookup"><span data-stu-id="1dc40-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="1dc40-140">Körfutáknseining</span><span class="sxs-lookup"><span data-stu-id="1dc40-140">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="1dc40-141">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="1dc40-141">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="1dc40-142">Greiðslueining</span><span class="sxs-lookup"><span data-stu-id="1dc40-142">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="1dc40-143">Afhendingarkostaeining</span><span class="sxs-lookup"><span data-stu-id="1dc40-143">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="1dc40-144">Eining fyrir afhendingarupplýsingar</span><span class="sxs-lookup"><span data-stu-id="1dc40-144">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="1dc40-145">Pöntunarupplýsingaeining</span><span class="sxs-lookup"><span data-stu-id="1dc40-145">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="1dc40-146">Gjafakortseining</span><span class="sxs-lookup"><span data-stu-id="1dc40-146">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="1dc40-147">Eining til að velja verslun</span><span class="sxs-lookup"><span data-stu-id="1dc40-147">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]