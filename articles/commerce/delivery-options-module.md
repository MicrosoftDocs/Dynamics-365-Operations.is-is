---
title: Eining afhendingarvalkosta
description: Þetta efnisatriði fjallar um einingar afhendingarvalkosta og lýsir því hvernig á að skilgreina þær í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 1e55ce327e2c8ab714eb5e2fa14b3830b9171688
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020680"
---
# <a name="delivery-options-module"></a><span data-ttu-id="7c75e-103">Afhendingarkostaeining</span><span class="sxs-lookup"><span data-stu-id="7c75e-103">Delivery options module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="7c75e-104">Þetta efnisatriði fjallar um einingar afhendingarvalkosta og lýsir því hvernig á að skilgreina þær í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7c75e-104">This topic covers delivery options modules and explains how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7c75e-105">Einingar afhendingarvalkosta leyfir viðskiptavinum að velja afhendingarmáta á borð við senda eða sækja fyrir pöntun á netinu.</span><span class="sxs-lookup"><span data-stu-id="7c75e-105">Delivery options modules let customers select a mode of delivery such as shipping or pickup for their online order.</span></span> <span data-ttu-id="7c75e-106">Heimilisfang viðtakanda er nauðsynlegt til að ákvarða afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="7c75e-106">A shipping address is required to determine the mode of delivery.</span></span> <span data-ttu-id="7c75e-107">Ef heimilisfang viðtakanda breytist, þarf að sækja afhendingarvalkostina aftur.</span><span class="sxs-lookup"><span data-stu-id="7c75e-107">If the shipping address changes, the delivery options must be retrieved again.</span></span> <span data-ttu-id="7c75e-108">Ef pöntun inniheldur aðeins vörur sem verða sóttar í verslun, verður þessi eining sjálfkrafa falin.</span><span class="sxs-lookup"><span data-stu-id="7c75e-108">If an order includes only items that will be picked up in a store, this module is automatically hidden.</span></span>

<span data-ttu-id="7c75e-109">Frekari upplýsingar um hvernig skilgreina á afhendingarmáta er að finna í [Uppsetning netrásar](channel-setup-online.md) og [Setja upp afhendingarmáta](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="7c75e-109">For information about how to configure modes of delivery, see [Online channel setup](channel-setup-online.md) and [Set up modes of delivery](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="7c75e-110">Hver afhendingarmáti getur verið með gjald tengt við.</span><span class="sxs-lookup"><span data-stu-id="7c75e-110">Each delivery mode can have an associated charge.</span></span> <span data-ttu-id="7c75e-111">Frekari upplýsingar um hvernig á að skilgreina gjöld fyrir netverslun er að finna í [Ítarleg sjálfvirk gjöld fyrir omni-rás](omni-auto-charges.md).</span><span class="sxs-lookup"><span data-stu-id="7c75e-111">For more information about how to configure charges for an online store, see [Omni-channel Advanced auto-charges](omni-auto-charges.md).</span></span>

<span data-ttu-id="7c75e-112">Í Commerce-útgáfu 10.0.13 hefur eining afhendingarvalkosta verið uppfærð til að styðja eiginleikana **Gjöld í haus án skiptingar** og **Senda sem línugjald**.</span><span class="sxs-lookup"><span data-stu-id="7c75e-112">In Commerce version 10.0.13, the delivery options module has been updated to support the **Header charges without proration** and **Shipping as a line charge** features.</span></span> <span data-ttu-id="7c75e-113">Ef slökkt er á skiptingu má búast við því að verkflæði rafrænna viðskipta leyfi ekki blandaðan afhendingarmáta fyrir vörurnar í körfunni (þ.e. sumar vörur eru valdar fyrir sendingu, en aðrar eru valdar til að sækja).</span><span class="sxs-lookup"><span data-stu-id="7c75e-113">If proration is turned off, the expectation is that the e-Commerce workflow won't allow a mixed mode of delivery for the items in the cart (that is, some items are selected for shipment, but others are selected for pickup).</span></span> <span data-ttu-id="7c75e-114">Eiginleikinn **Gjöld í haus án skiptingar** krefst þess að kveikt sé á flagginu **Virkja samræmda meðhöndlun afhendingar í rás** í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="7c75e-114">The **Header charges without proration** feature requires that the **Enable consistent delivery mode handling in channel** flag is turned on in Commerce headquarters.</span></span> <span data-ttu-id="7c75e-115">Þegar kveikt er á eiginleikaflagginu verða sendingargjöld sett á annaðhvort á hausstigi eða línustigi, fer eftir skilgreiningunni í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="7c75e-115">When the feature flag is turned on, shipping charges will be applied at either the header level or the line level, depending on the configuration in Commerce headquarters.</span></span>

<span data-ttu-id="7c75e-116">Fabrikam-þemað styður við blandaða afhendingarmáta, þar sem sumar vörur eru valdar fyrir sendingu en aðrar eru valdar til að vera sóttar.</span><span class="sxs-lookup"><span data-stu-id="7c75e-116">The Fabrikam theme supports a mixed mode of delivery, where some items are selected for shipment but others are selected for pickup.</span></span> <span data-ttu-id="7c75e-117">Í þessari stillingu verður sendingargjöldum skipt niður fyrir allar vörur sem eru valdar fyrir afhendingarmáta sendingar.</span><span class="sxs-lookup"><span data-stu-id="7c75e-117">In this mode, shipping charges will be prorated for all items that are selected for the shipping mode of delivery.</span></span> <span data-ttu-id="7c75e-118">Til að blandaður afhendingarmáti virki þarf fyrst að skilgreina eiginleikann **Gjöld í haus með skiptingu** í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="7c75e-118">For a mixed mode of delivery to work, you must first configure the **Header charges with proration** feature in Commerce headquarters.</span></span> <span data-ttu-id="7c75e-119">Frekari upplýsingar um þessa skilgreiningu er að finna í [Skipta gjöldum í haus til að stemma við sölulínur](pro-rate-charges-matching-lines.md).</span><span class="sxs-lookup"><span data-stu-id="7c75e-119">For more information about this configuration, see [Prorate header charges to match sales lines](pro-rate-charges-matching-lines.md).</span></span>

<span data-ttu-id="7c75e-120">Ef sendingargjöld eiga við um línuatriði er hægt að sýna þau í körfulínunni fyrir hverja vöru.</span><span class="sxs-lookup"><span data-stu-id="7c75e-120">If shipping charges apply to line items, they can be shown on the cart line for each item.</span></span> <span data-ttu-id="7c75e-121">Þessi virkni krefst þess að kveikt sé á eiginleikanum **Sýna sendingargjöld í línuatriði** fyrir bæði körfueininguna og greiðsluferliseininguna.</span><span class="sxs-lookup"><span data-stu-id="7c75e-121">This functionality requires that the **Show shipping charges on line item** property be turned on for both the cart module and the checkout module.</span></span> <span data-ttu-id="7c75e-122">Frekari upplýsingar er að finna í [Körfueining](add-cart-module.md) og [Greiðsluferliseining](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="7c75e-122">For more information, see [Cart module](add-cart-module.md) and [Checkout module](add-checkout-module.md).</span></span>

<span data-ttu-id="7c75e-123">Eftirfarandi mynd sýnir dæmi um einingu afhendingarvalkosts á greiðsluferlissíðu.</span><span class="sxs-lookup"><span data-stu-id="7c75e-123">The following illustration shows an example of a delivery options module on a checkout page.</span></span>

![Dæmi um einingu afhendingarvalkosts á greiðsluferlissíðu](./media/ecommerce-deliveryoptions.PNG)

## <a name="delivery-options-module-properties"></a><span data-ttu-id="7c75e-125">Eiginleikar einingar afhendingarvalkosta</span><span class="sxs-lookup"><span data-stu-id="7c75e-125">Delivery options module properties</span></span>

| <span data-ttu-id="7c75e-126">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="7c75e-126">Property</span></span> | <span data-ttu-id="7c75e-127">Gildi</span><span class="sxs-lookup"><span data-stu-id="7c75e-127">Values</span></span> | <span data-ttu-id="7c75e-128">lýsing</span><span class="sxs-lookup"><span data-stu-id="7c75e-128">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="7c75e-129">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="7c75e-129">Heading</span></span> | <span data-ttu-id="7c75e-130">Fyrirsagnartexti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**)</span><span class="sxs-lookup"><span data-stu-id="7c75e-130">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="7c75e-131">Valfrjáls fyrirsögn fyrir einingu afhendingarvalkosta.</span><span class="sxs-lookup"><span data-stu-id="7c75e-131">An optional heading for the delivery options module.</span></span> |
| <span data-ttu-id="7c75e-132">Sérsniðið CSS heiti klasa</span><span class="sxs-lookup"><span data-stu-id="7c75e-132">Custom CSS class name</span></span> | <span data-ttu-id="7c75e-133">Texti</span><span class="sxs-lookup"><span data-stu-id="7c75e-133">Text</span></span> | <span data-ttu-id="7c75e-134">Sérsniðið klasaheiti stallaðs stílblaðs (CSS) sem verður notað til að sýna þessa einingu, ef það á við.</span><span class="sxs-lookup"><span data-stu-id="7c75e-134">A custom Cascading Style Sheets (CSS) class name that will be used to render this module, if applicable.</span></span> |
| <span data-ttu-id="7c75e-135">Sía fyrir sendingarstillingu</span><span class="sxs-lookup"><span data-stu-id="7c75e-135">Filter Delivery Mode Option</span></span> | <span data-ttu-id="7c75e-136">**Ekki sía** eða **Afhendingarmátar án sendingar**</span><span class="sxs-lookup"><span data-stu-id="7c75e-136">**Do not filter** or **Non-shipping modes**</span></span> | <span data-ttu-id="7c75e-137">Gildi sem tilgreinir hvort eining afhendingarvalkosta eigi að sía út alla afhendingarmáta án sendingar.</span><span class="sxs-lookup"><span data-stu-id="7c75e-137">A value that specifies whether the delivery options module should filter out all non-shipping delivery modes.</span></span> |
| <span data-ttu-id="7c75e-138">Velja afhendingarvalkost sjálfkrafa</span><span class="sxs-lookup"><span data-stu-id="7c75e-138">Auto select a delivery option</span></span> | <span data-ttu-id="7c75e-139">**Ekki sía**, **Velja afhendingarvalkost sjálfkrafa og sýna samantekt** eða **Velja afhendingarvalkost sjálfkrafa og ekki sýna samantekt**</span><span class="sxs-lookup"><span data-stu-id="7c75e-139">**Do not filter**, **Auto select delivery option and show summary**, or **Auto select delivery option and don't show summary**</span></span> | <span data-ttu-id="7c75e-140">Þessi eiginleiki notar sjálfkrafa fyrsta tiltæka afhendingarvalkostinn til að ljúka kaupum án þess að notandinn þurfi að velja hann.</span><span class="sxs-lookup"><span data-stu-id="7c75e-140">This property automatically applies the first available delivery option to checkout without requiring the user to select it.</span></span> <span data-ttu-id="7c75e-141">Aðeins ætti að nota hann ef einn afhendingarvalkostur er fyrir hendi.</span><span class="sxs-lookup"><span data-stu-id="7c75e-141">It should be used only if there is one available delivery option.</span></span> <span data-ttu-id="7c75e-142">Þessi eiginleiki er studdur frá og með Commerce-útgáfu 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="7c75e-142">This property is supported as of the Commerce version 10.0.19 release.</span></span> |

## <a name="add-a-delivery-options-module-to-a-checkout-page-and-set-the-required-properties"></a><span data-ttu-id="7c75e-143">Bæta einingu afhendingarvalkosta við greiðsluferlissíðu og stilla nauðsynlega eiginleika</span><span class="sxs-lookup"><span data-stu-id="7c75e-143">Add a delivery options module to a checkout page and set the required properties</span></span>

<span data-ttu-id="7c75e-144">Aðeins er hægt að bæta einingu afhendingarvalkosta við greiðsluferliseiningu.</span><span class="sxs-lookup"><span data-stu-id="7c75e-144">A delivery options module can be added only to a checkout module.</span></span> <span data-ttu-id="7c75e-145">Frekari upplýsingar um hvernig skilgreina á einingu afhendingarvalkosta og bæta henni við greiðsluferlissíðu er að finna í [Greiðsluferliseining](add-checkout-module.md).</span><span class="sxs-lookup"><span data-stu-id="7c75e-145">For more information about how to configure the delivery options module and add it to a checkout page, see [Checkout module](add-checkout-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c75e-146">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7c75e-146">Additional resources</span></span>

[<span data-ttu-id="7c75e-147">Körfueining</span><span class="sxs-lookup"><span data-stu-id="7c75e-147">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="7c75e-148">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="7c75e-148">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7c75e-149">Greiðslueining</span><span class="sxs-lookup"><span data-stu-id="7c75e-149">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="7c75e-150">Sendingaraðseturseining</span><span class="sxs-lookup"><span data-stu-id="7c75e-150">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="7c75e-151">Eining fyrir afhendingarupplýsingar</span><span class="sxs-lookup"><span data-stu-id="7c75e-151">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="7c75e-152">Pöntunarupplýsingaeining</span><span class="sxs-lookup"><span data-stu-id="7c75e-152">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="7c75e-153">Gjafakortseining</span><span class="sxs-lookup"><span data-stu-id="7c75e-153">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="7c75e-154">Uppsetning netrásar</span><span class="sxs-lookup"><span data-stu-id="7c75e-154">Online channel setup</span></span>](channel-setup-online.md)

[<span data-ttu-id="7c75e-155">Ítarleg sjálfvirk gjöld fyrir omni-rás</span><span class="sxs-lookup"><span data-stu-id="7c75e-155">Omni-channel Advanced auto-charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="7c75e-156">Skipta gjöldum í haus til að stemma við sölulínur</span><span class="sxs-lookup"><span data-stu-id="7c75e-156">Prorate header charges to match sales lines</span></span>](pro-rate-charges-matching-lines.md)

[<span data-ttu-id="7c75e-157">Setja upp afhendingarmáta</span><span class="sxs-lookup"><span data-stu-id="7c75e-157">Set up modes of delivery</span></span>](/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
