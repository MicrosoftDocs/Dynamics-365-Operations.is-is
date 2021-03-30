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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: d0e5fa731d4b808cda9863074d17d1917410f399
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213675"
---
# <a name="delivery-options-module"></a><span data-ttu-id="b50ec-103">Afhendingarkostaeining</span><span class="sxs-lookup"><span data-stu-id="b50ec-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b50ec-104">Þetta efnisatriði fjallar um einingar afhendingarvalkosta og lýsir því hvernig á að skilgreina þær í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b50ec-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b50ec-105">Einingar afhendingarvalkosta leyfir viðskiptavinum að velja afhendingarmáta á borð við senda eða sækja fyrir pöntun á netinu.</span><span class="sxs-lookup"><span data-stu-id="b50ec-105">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="b50ec-106">Heimilisfang viðtakanda er nauðsynlegt til að ákvarða afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="b50ec-106">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="b50ec-107">Ef heimilisfang viðtakanda breytist, þarf að sækja afhendingarvalkostina aftur.</span><span class="sxs-lookup"><span data-stu-id="b50ec-107">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="b50ec-108">Ef pöntun inniheldur aðeins vörur sem verða sóttar í verslun, verður þessi eining sjálfkrafa falin.</span><span class="sxs-lookup"><span data-stu-id="b50ec-108">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="b50ec-109">Frekari upplýsingar um hvernig skilgreina á afhendingarmáta er að finna í [Uppsetning netrásar](channel-setup-online.md) og [Setja upp afhendingarmáta](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="b50ec-109">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="b50ec-110">Hver afhendingarmáti getur verið með gjald tengt við.</span><span class="sxs-lookup"><span data-stu-id="b50ec-110">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="b50ec-111">Frekari upplýsingar um hvernig á að skilgreina gjöld fyrir netverslun er að finna í [Ítarleg sjálfvirk gjöld fyrir omni-rás](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="b50ec-111">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="b50ec-112">Í Commerce-útgáfu 10.0.13 hefur eining afhendingarvalkosta verið uppfærð til að styðja eiginleikana **Gjöld í haus án skiptingar** og **Senda sem línugjald**.</span><span class="sxs-lookup"><span data-stu-id="b50ec-112">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="b50ec-113">Ef slökkt er á skiptingu má búast við því að verkflæði rafrænna viðskipta leyfi ekki blandaðan afhendingarmáta fyrir vörurnar í körfunni (þ.e. sumar vörur eru valdar fyrir sendingu, en aðrar eru valdar til að sækja).</span><span class="sxs-lookup"><span data-stu-id="b50ec-113">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="b50ec-114">Eiginleikinn **Gjöld í haus án skiptingar** krefst þess að kveikt sé á flagginu **Virkja samræmda meðhöndlun afhendingar í rás** í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="b50ec-114">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag be turned on in Commerce headquarters.</span></span> <span data-ttu-id="b50ec-115">Þegar kveikt er á flagginu verða sendingargjöld sett á annaðhvort á hausstigi eða línustigi, fer eftir skilgreiningunni í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="b50ec-115">When that flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="b50ec-116">Fabrikam-þemað styður við blandaða afhendingarmáta, þar sem sumar vörur eru valdar fyrir sendingu en aðrar eru valdar til að vera sóttar.</span><span class="sxs-lookup"><span data-stu-id="b50ec-116">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="b50ec-117">Í þessari stillingu verður sendingargjöldum skipt niður fyrir allar vörur sem eru valdar fyrir afhendingarmáta sendingar.</span><span class="sxs-lookup"><span data-stu-id="b50ec-117">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="b50ec-118">Til að blandaður afhendingarmáti virki þarf fyrst að skilgreina eiginleikann **Gjöld í haus með skiptingu** í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="b50ec-118">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="b50ec-119">Frekari upplýsingar um þessa skilgreiningu er að finna í [Skipta gjöldum í haus til að stemma við sölulínur](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="b50ec-119">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="b50ec-120">Ef sendingargjöld eiga við um línuatriði er hægt að sýna þau í körfulínunni fyrir hverja vöru.</span><span class="sxs-lookup"><span data-stu-id="b50ec-120">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="b50ec-121">Þessi virkni krefst þess að kveikt sé á eiginleikanum **Sýna sendingargjöld í línuatriði** fyrir bæði körfueininguna og greiðsluferliseininguna.</span><span class="sxs-lookup"><span data-stu-id="b50ec-121">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="b50ec-122">Frekari upplýsingar er að finna í [Körfueining](add-cart-module.md) og [Greiðsluferliseining](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="b50ec-122">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="b50ec-123">Eftirfarandi mynd sýnir dæmi um einingu afhendingarvalkosts á greiðsluferlissíðu.</span><span class="sxs-lookup"><span data-stu-id="b50ec-123">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Dæmi um einingu afhendingarvalkosts á greiðsluferlissíðu](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="b50ec-125">Eiginleikar einingar afhendingarvalkosta</span><span class="sxs-lookup"><span data-stu-id="b50ec-125">Delivery options module properties</span></span>

| <span data-ttu-id="b50ec-126">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="b50ec-126">Property</span></span> | <span data-ttu-id="b50ec-127">Gildi</span><span class="sxs-lookup"><span data-stu-id="b50ec-127">Values</span></span> | <span data-ttu-id="b50ec-128">lýsing</span><span class="sxs-lookup"><span data-stu-id="b50ec-128">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="b50ec-129">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="b50ec-129">Heading</span></span> | <span data-ttu-id="b50ec-130">Fyrirsagnartexti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**)</span><span class="sxs-lookup"><span data-stu-id="b50ec-130">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="b50ec-131">Valfrjáls fyrirsögn fyrir einingu afhendingarvalkosta.</span><span class="sxs-lookup"><span data-stu-id="b50ec-131">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="b50ec-132">Sérsniðið CSS heiti klasa</span><span class="sxs-lookup"><span data-stu-id="b50ec-132">Custom CSS class name</span></span> | <span data-ttu-id="b50ec-133">Texti</span><span class="sxs-lookup"><span data-stu-id="b50ec-133">Text</span></span> | <span data-ttu-id="b50ec-134">Sérsniðið klasaheiti stallaðs stílblaðs (CSS) sem verður notað til að sýna þessa einingu, ef það á við.</span><span class="sxs-lookup"><span data-stu-id="b50ec-134">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="b50ec-135">Sía fyrir sendingarstillingu</span><span class="sxs-lookup"><span data-stu-id="b50ec-135">Filter Delivery Mode Option</span></span> | <span data-ttu-id="b50ec-136">**Ekki sía** eða **Afhendingarmátar án sendingar**</span><span class="sxs-lookup"><span data-stu-id="b50ec-136">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="b50ec-137">Gildi sem tilgreinir hvort eining afhendingarvalkosta eigi að sía út alla afhendingarmáta án sendingar.</span><span class="sxs-lookup"><span data-stu-id="b50ec-137">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="b50ec-138">Bæta einingu afhendingarvalkosta við greiðsluferlissíðu og stilla nauðsynlega eiginleika</span><span class="sxs-lookup"><span data-stu-id="b50ec-138">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="b50ec-139">Aðeins er hægt að bæta einingu afhendingarvalkosta við greiðsluferliseiningu.</span><span class="sxs-lookup"><span data-stu-id="b50ec-139">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="b50ec-140">Frekari upplýsingar um hvernig skilgreina á einingu afhendingarvalkosta og bæta henni við greiðsluferlissíðu er að finna í [Greiðsluferliseining](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="b50ec-140">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b50ec-141">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b50ec-141">Additional resources</span></span>

[<span data-ttu-id="b50ec-142">Körfueining</span><span class="sxs-lookup"><span data-stu-id="b50ec-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b50ec-143">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="b50ec-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b50ec-144">Greiðslueining</span><span class="sxs-lookup"><span data-stu-id="b50ec-144">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="b50ec-145">Sendingaraðseturseining</span><span class="sxs-lookup"><span data-stu-id="b50ec-145">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="b50ec-146">Eining fyrir afhendingarupplýsingar</span><span class="sxs-lookup"><span data-stu-id="b50ec-146">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="b50ec-147">Pöntunarupplýsingaeining</span><span class="sxs-lookup"><span data-stu-id="b50ec-147">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b50ec-148">Gjafakortseining</span><span class="sxs-lookup"><span data-stu-id="b50ec-148">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="b50ec-149">Uppsetning netrásar</span><span class="sxs-lookup"><span data-stu-id="b50ec-149">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="b50ec-150">Ítarleg sjálfvirk gjöld fyrir omni-rás</span><span class="sxs-lookup"><span data-stu-id="b50ec-150">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="b50ec-151">Skipta gjöldum í haus til að stemma við sölulínur</span><span class="sxs-lookup"><span data-stu-id="b50ec-151">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="b50ec-152">Setja upp afhendingarmáta</span><span class="sxs-lookup"><span data-stu-id="b50ec-152">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]