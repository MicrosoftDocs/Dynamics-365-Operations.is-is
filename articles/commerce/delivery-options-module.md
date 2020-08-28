---
title: Eining afhendingarvalkosta
description: Þetta efnisatriði fjallar um einingar afhendingarvalkosta og lýsir því hvernig á að skilgreina þær í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 60449e9492c8e831b4ec6b2896f1ab471ef9d499
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661208"
---
# <a name="delivery-options-module"></a><span data-ttu-id="65ee9-103">Eining afhendingarvalkosta</span><span class="sxs-lookup"><span data-stu-id="65ee9-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="65ee9-104">Þetta efnisatriði fjallar um einingar afhendingarvalkosta og lýsir því hvernig á að skilgreina þær í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="65ee9-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="65ee9-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="65ee9-105">Overview</span></span>

<span data-ttu-id="65ee9-106">Einingar afhendingarvalkosta leyfir viðskiptavinum að velja afhendingarmáta á borð við senda eða sækja fyrir pöntun á netinu.</span><span class="sxs-lookup"><span data-stu-id="65ee9-106">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="65ee9-107">Heimilisfang viðtakanda er nauðsynlegt til að ákvarða afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="65ee9-107">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="65ee9-108">Ef heimilisfang viðtakanda breytist, þarf að sækja afhendingarvalkostina aftur.</span><span class="sxs-lookup"><span data-stu-id="65ee9-108">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="65ee9-109">Ef pöntun inniheldur aðeins vörur sem verða sóttar í verslun, verður þessi eining sjálfkrafa falin.</span><span class="sxs-lookup"><span data-stu-id="65ee9-109">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="65ee9-110">Frekari upplýsingar um hvernig skilgreina á afhendingarmáta er að finna í [Uppsetning netrásar](channel-setup-online.md) og [Setja upp afhendingarmáta](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="65ee9-110">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="65ee9-111">Hver afhendingarmáti getur verið með gjald tengt við.</span><span class="sxs-lookup"><span data-stu-id="65ee9-111">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="65ee9-112">Frekari upplýsingar um hvernig á að skilgreina gjöld fyrir netverslun er að finna í [Ítarleg sjálfvirk gjöld fyrir omni-rás](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="65ee9-112">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="65ee9-113">Í Commerce-útgáfu 10.0.13 hefur eining afhendingarvalkosta verið uppfærð til að styðja eiginleikana **Gjöld í haus án skiptingar** og **Senda sem línugjald**.</span><span class="sxs-lookup"><span data-stu-id="65ee9-113">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="65ee9-114">Ef slökkt er á skiptingu má búast við því að verkflæði rafrænna viðskipta leyfi ekki blandaðan afhendingarmáta fyrir vörurnar í körfunni (þ.e. sumar vörur eru valdar fyrir sendingu, en aðrar eru valdar til að sækja).</span><span class="sxs-lookup"><span data-stu-id="65ee9-114">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="65ee9-115">Eiginleikinn **Gjöld í haus án skiptingar** krefst þess að kveikt sé á flagginu **Virkja samræmda meðhöndlun afhendingar í rás** í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="65ee9-115">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag be turned on in Commerce headquarters.</span></span> <span data-ttu-id="65ee9-116">Þegar kveikt er á flagginu verða sendingargjöld sett á annaðhvort á hausstigi eða línustigi, fer eftir skilgreiningunni í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="65ee9-116">When that flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="65ee9-117">Fabrikam-þemað styður við blandaða afhendingarmáta, þar sem sumar vörur eru valdar fyrir sendingu en aðrar eru valdar til að vera sóttar.</span><span class="sxs-lookup"><span data-stu-id="65ee9-117">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="65ee9-118">Í þessari stillingu verður sendingargjöldum skipt niður fyrir allar vörur sem eru valdar fyrir afhendingarmáta sendingar.</span><span class="sxs-lookup"><span data-stu-id="65ee9-118">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="65ee9-119">Til að blandaður afhendingarmáti virki þarf fyrst að skilgreina eiginleikann **Gjöld í haus með skiptingu** í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="65ee9-119">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="65ee9-120">Frekari upplýsingar um þessa skilgreiningu er að finna í [Skipta gjöldum í haus til að stemma við sölulínur](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="65ee9-120">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="65ee9-121">Ef sendingargjöld eiga við um línuatriði er hægt að sýna þau í körfulínunni fyrir hverja vöru.</span><span class="sxs-lookup"><span data-stu-id="65ee9-121">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="65ee9-122">Þessi virkni krefst þess að kveikt sé á eiginleikanum **Sýna sendingargjöld í línuatriði** fyrir bæði körfueininguna og greiðsluferliseininguna.</span><span class="sxs-lookup"><span data-stu-id="65ee9-122">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="65ee9-123">Frekari upplýsingar er að finna í [Körfueining](add-cart-module.md) og [Greiðsluferliseining](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="65ee9-123">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="65ee9-124">Eftirfarandi mynd sýnir dæmi um einingu afhendingarvalkosts á greiðsluferlissíðu.</span><span class="sxs-lookup"><span data-stu-id="65ee9-124">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Dæmi um einingu afhendingarvalkosts á greiðsluferlissíðu](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="65ee9-126">Eiginleikar einingar afhendingarvalkosta</span><span class="sxs-lookup"><span data-stu-id="65ee9-126">Delivery options module properties</span></span>

| <span data-ttu-id="65ee9-127">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="65ee9-127">Property</span></span> | <span data-ttu-id="65ee9-128">Gildi</span><span class="sxs-lookup"><span data-stu-id="65ee9-128">Values</span></span> | <span data-ttu-id="65ee9-129">lýsing</span><span class="sxs-lookup"><span data-stu-id="65ee9-129">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="65ee9-130">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="65ee9-130">Heading</span></span> | <span data-ttu-id="65ee9-131">Fyrirsagnartexti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**)</span><span class="sxs-lookup"><span data-stu-id="65ee9-131">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="65ee9-132">Valfrjáls fyrirsögn fyrir einingu afhendingarvalkosta.</span><span class="sxs-lookup"><span data-stu-id="65ee9-132">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="65ee9-133">Sérsniðið CSS heiti klasa</span><span class="sxs-lookup"><span data-stu-id="65ee9-133">Custom CSS class name</span></span> | <span data-ttu-id="65ee9-134">Texti</span><span class="sxs-lookup"><span data-stu-id="65ee9-134">Text</span></span> | <span data-ttu-id="65ee9-135">Sérsniðið klasaheiti stallaðs stílblaðs (CSS) sem verður notað til að sýna þessa einingu, ef það á við.</span><span class="sxs-lookup"><span data-stu-id="65ee9-135">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="65ee9-136">Sía fyrir sendingarstillingu</span><span class="sxs-lookup"><span data-stu-id="65ee9-136">Filter Delivery Mode Option</span></span> | <span data-ttu-id="65ee9-137">**Ekki sía** eða **Afhendingarmátar án sendingar**</span><span class="sxs-lookup"><span data-stu-id="65ee9-137">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="65ee9-138">Gildi sem tilgreinir hvort eining afhendingarvalkosta eigi að sía út alla afhendingarmáta án sendingar.</span><span class="sxs-lookup"><span data-stu-id="65ee9-138">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="65ee9-139">Bæta einingu afhendingarvalkosta við greiðsluferlissíðu og stilla nauðsynlega eiginleika</span><span class="sxs-lookup"><span data-stu-id="65ee9-139">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="65ee9-140">Aðeins er hægt að bæta einingu afhendingarvalkosta við greiðsluferliseiningu.</span><span class="sxs-lookup"><span data-stu-id="65ee9-140">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="65ee9-141">Frekari upplýsingar um hvernig skilgreina á einingu afhendingarvalkosta og bæta henni við greiðsluferlissíðu er að finna í [Greiðsluferliseining](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="65ee9-141">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65ee9-142">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="65ee9-142">Additional resources</span></span>

[<span data-ttu-id="65ee9-143">Körfueining</span><span class="sxs-lookup"><span data-stu-id="65ee9-143">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="65ee9-144">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="65ee9-144">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="65ee9-145">Greiðslueining</span><span class="sxs-lookup"><span data-stu-id="65ee9-145">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="65ee9-146">Eining sendingaraðseturs</span><span class="sxs-lookup"><span data-stu-id="65ee9-146">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="65ee9-147">Pöntunarupplýsingaeining</span><span class="sxs-lookup"><span data-stu-id="65ee9-147">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="65ee9-148">Gjafakortseining</span><span class="sxs-lookup"><span data-stu-id="65ee9-148">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="65ee9-149">Uppsetning netrásar</span><span class="sxs-lookup"><span data-stu-id="65ee9-149">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="65ee9-150">Ítarleg sjálfvirk gjöld fyrir omni-rás</span><span class="sxs-lookup"><span data-stu-id="65ee9-150">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="65ee9-151">Skipta gjöldum í haus til að stemma við sölulínur</span><span class="sxs-lookup"><span data-stu-id="65ee9-151">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="65ee9-152">Setja upp afhendingarmáta</span><span class="sxs-lookup"><span data-stu-id="65ee9-152">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
