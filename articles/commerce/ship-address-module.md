---
title: Eining sendingaraðseturs
description: Þetta efnisatriði fjallar um einingu sendingaraðseturs og útskýrir hvernig á að skilgreina hana í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: aeaa410fde29b285fdbbdd6acac19b0c4e917aa5
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/07/2020
ms.locfileid: "4413320"
---
# <a name="shipping-address-module"></a><span data-ttu-id="c5859-103">Eining sendingaraðseturs</span><span class="sxs-lookup"><span data-stu-id="c5859-103">Shipping address module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c5859-104">Þetta efnisatriði lýsir einingu sendingaraðseturs og útskýrir hvernig á að skilgreina hana í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c5859-104">This topic describes covers the shipping address module and explains how to configure it in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c5859-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="c5859-105">Overview</span></span>

<span data-ttu-id="c5859-106">Einingin fyrir sendingaraðsetur gerir viðskiptavinum kleift að bæta við eða velja sendingaraðsetur fyrir pöntun meðan á greiðsluferlinu stendur.</span><span class="sxs-lookup"><span data-stu-id="c5859-106">The shipping address module lets customers add or select the shipping address for an order during the checkout flow.</span></span> <span data-ttu-id="c5859-107">Ef viðskiptavinur er skráður inn eru öll aðsetur sem áður voru vistuð fyrir þennan viðskiptavin sýnd og viðskiptavinurinn getur valið á milli þeirra.</span><span class="sxs-lookup"><span data-stu-id="c5859-107">If a customer is signed in, any addresses that were previously saved for that customer are shown, and the customer can select among them.</span></span> <span data-ttu-id="c5859-108">Viðskiptavinurinn getur einnig bætt við nýju heimilisfangi.</span><span class="sxs-lookup"><span data-stu-id="c5859-108">The customer can also add a new address.</span></span> <span data-ttu-id="c5859-109">Einingin fyrir sendingaraðsetur er notuð fyrir allar vörur í pöntun sem krefjast sendingar.</span><span class="sxs-lookup"><span data-stu-id="c5859-109">The shipping address module is used for all items on an order that require shipping.</span></span>

<span data-ttu-id="c5859-110">Hægt er að skilgreina snið sendingaraðseturs í Commerce Headquarters fyrir hvert land eða svæði og eining sendingaraðseturs framfylgir þá reglum fyrir tiltekið land/svæði.</span><span class="sxs-lookup"><span data-stu-id="c5859-110">Shipping address formats can be defined in Commerce headquarters for each country or region, and the shipping address module then enforces country/region-specific rules.</span></span>

<span data-ttu-id="c5859-111">Þegar viðskiptavinir færa inn sendingaraðsetur í greiðsluferlinu, hafa þeir val um að vista aðsetrið sem aðalaðsetur.</span><span class="sxs-lookup"><span data-stu-id="c5859-111">When customers enter a shipping address during the checkout flow, they have the option to save the address as a primary address.</span></span> <span data-ttu-id="c5859-112">Þessi valkostur er aðeins sýndur ef viðskiptavinur er skráður inn.</span><span class="sxs-lookup"><span data-stu-id="c5859-112">This option is shown only if a customer is signed in.</span></span>

<span data-ttu-id="c5859-113">Þótt einingin fyrir sendingaraðsetur veiti ekki staðfestingu á aðsetri, er hægt að innleiða þessa virkni í gegnum sérstillingu.</span><span class="sxs-lookup"><span data-stu-id="c5859-113">Although the shipping address module doesn't provide address validation, this functionality can be implemented through customization.</span></span>

<span data-ttu-id="c5859-114">Eftirfarandi mynd sýnir dæmi um nýja einingu sendingaraðseturs á greiðsluferlissíðu.</span><span class="sxs-lookup"><span data-stu-id="c5859-114">The following illustration shows an example of a new shipping address module on a checkout page.</span></span>

![Dæmi um einingu sendingaraðseturs á greiðsluferlissíðu](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a><span data-ttu-id="c5859-116">Eiginleikar einingar</span><span class="sxs-lookup"><span data-stu-id="c5859-116">Module properties</span></span>

| <span data-ttu-id="c5859-117">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="c5859-117">Property name</span></span> | <span data-ttu-id="c5859-118">Gildi</span><span class="sxs-lookup"><span data-stu-id="c5859-118">Values</span></span> | <span data-ttu-id="c5859-119">lýsing</span><span class="sxs-lookup"><span data-stu-id="c5859-119">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="c5859-120">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="c5859-120">Heading</span></span> | <span data-ttu-id="c5859-121">Fyrirsagnartexti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**)</span><span class="sxs-lookup"><span data-stu-id="c5859-121">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="c5859-122">Valfrjáls fyrirsögn fyrir einingu sendingaraðseturs.</span><span class="sxs-lookup"><span data-stu-id="c5859-122">An optional heading for the shipping address module.</span></span> |
| <span data-ttu-id="c5859-123">Sýna aðsetursgerð</span><span class="sxs-lookup"><span data-stu-id="c5859-123">Show address type</span></span> | <span data-ttu-id="c5859-124">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="c5859-124">**True** or **False**</span></span> | <span data-ttu-id="c5859-125">Ef þessi valfrjálsi eiginleiki er stilltur á **Satt**, verður gerð aðseturs, t.d. **Heimili** eða **Fyrirtæki** sýnt.</span><span class="sxs-lookup"><span data-stu-id="c5859-125">If this optional property is set to **True**, an address type, such as **Home** or **Business**, will be shown.</span></span> <span data-ttu-id="c5859-126">Ef engin aðsetursgerð er tilgreind verður aðsetrið sjálfkrafa vistað sem **Gerð**=**Annað**.</span><span class="sxs-lookup"><span data-stu-id="c5859-126">If no address type is specified, the address will automatically be saved as **Type**=**Other**.</span></span> |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="c5859-127">Bæta einingu sendingaraðseturs við greiðsluferlissíðu og stilla nauðsynlega eiginleika</span><span class="sxs-lookup"><span data-stu-id="c5859-127">Add a shipping address module to a checkout page and set the required properties</span></span>

<span data-ttu-id="c5859-128">Aðeins er hægt að bæta einingu sendingaraðseturs við greiðsluferliseiningu.</span><span class="sxs-lookup"><span data-stu-id="c5859-128">A shipping address module can be added only to a checkout module.</span></span> <span data-ttu-id="c5859-129">Frekari upplýsingar um hvernig skilgreina á einingu sendingaraðseturs og bæta henni við greiðsluferlissíðu er að finna í [Greiðsluferliseining](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="c5859-129">For more information about how to configure the shipping address module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c5859-130">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c5859-130">Additional resources</span></span>

[<span data-ttu-id="c5859-131">Körfueining</span><span class="sxs-lookup"><span data-stu-id="c5859-131">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c5859-132">Körfutáknseining</span><span class="sxs-lookup"><span data-stu-id="c5859-132">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="c5859-133">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="c5859-133">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c5859-134">Greiðslueining</span><span class="sxs-lookup"><span data-stu-id="c5859-134">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="c5859-135">Afhendingarkostaeining</span><span class="sxs-lookup"><span data-stu-id="c5859-135">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="c5859-136">Eining fyrir afhendingarupplýsingar</span><span class="sxs-lookup"><span data-stu-id="c5859-136">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="c5859-137">Pöntunarupplýsingaeining</span><span class="sxs-lookup"><span data-stu-id="c5859-137">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="c5859-138">Gjafakortseining</span><span class="sxs-lookup"><span data-stu-id="c5859-138">Gift card module</span></span>](add-giftcard.md)
