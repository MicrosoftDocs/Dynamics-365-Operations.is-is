---
title: Eining pöntunarstaðfestingar
description: Þetta efnisatriði fjallar um staðfestingareiningar og lýsir því hvernig á að notar þær í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 11/06/2020
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1f8742637cc8ed29abcfb9a8061a8d2602762d4f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804578"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="130e2-103">Eining pöntunarstaðfestingar</span><span class="sxs-lookup"><span data-stu-id="130e2-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="130e2-104">Þetta efnisatriði fjallar um staðfestingareiningar og lýsir því hvernig á að notar þær í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="130e2-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="130e2-105">Pöntunarstaðfestingareiningin er notuð til að sýna upplýsingar pöntunarstaðfestinga eftir að pöntun hefur verið gerð.</span><span class="sxs-lookup"><span data-stu-id="130e2-105">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="130e2-106">Hún sýnir staðfestingarkenni pöntunar, tengslaupplýsingar pöntunar og aðrar upplýsingar um pöntun, svo sem vörur sem voru keyptar, greiðsluupplýsingar, afhendingarmáta og sendingaraðferð.</span><span class="sxs-lookup"><span data-stu-id="130e2-106">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="130e2-107">Eiginleikar staðfestingareiningar pöntunar</span><span class="sxs-lookup"><span data-stu-id="130e2-107">Order confirmation module properties</span></span>

| <span data-ttu-id="130e2-108">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="130e2-108">Property name</span></span>  | <span data-ttu-id="130e2-109">Gildi</span><span class="sxs-lookup"><span data-stu-id="130e2-109">Values</span></span> | <span data-ttu-id="130e2-110">Lýsing</span><span class="sxs-lookup"><span data-stu-id="130e2-110">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="130e2-111">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="130e2-111">Heading</span></span>        | <span data-ttu-id="130e2-112">Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**)</span><span class="sxs-lookup"><span data-stu-id="130e2-112">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="130e2-113">Pöntunarstaðfestingareiningin getur haft fyrirsögn.</span><span class="sxs-lookup"><span data-stu-id="130e2-113">The order confirmation module can have a heading.</span></span> <span data-ttu-id="130e2-114">Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina.</span><span class="sxs-lookup"><span data-stu-id="130e2-114">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="130e2-115">Hins vegar er hægt að breyta merkinu til að uppfylla kröfur um aðgengi.</span><span class="sxs-lookup"><span data-stu-id="130e2-115">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="130e2-116">Númer tengiliðar</span><span class="sxs-lookup"><span data-stu-id="130e2-116">Contact number</span></span> | <span data-ttu-id="130e2-117">Text</span><span class="sxs-lookup"><span data-stu-id="130e2-117">Text</span></span> | <span data-ttu-id="130e2-118">Hægt er að gefa upp tengiliðanúmer fyrir pöntunarskyldar spurningar.</span><span class="sxs-lookup"><span data-stu-id="130e2-118">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="130e2-119">Sýna upplýsingar um tímahólf afhendingar</span><span class="sxs-lookup"><span data-stu-id="130e2-119">Show pickup timeslot information</span></span> | <span data-ttu-id="130e2-120">Satt eða ósatt</span><span class="sxs-lookup"><span data-stu-id="130e2-120">True or False</span></span> | <span data-ttu-id="130e2-121">Þessi eiginleiki er í boði í Dynamics 365 Commerce 10.0.15 og ´nýrri.</span><span class="sxs-lookup"><span data-stu-id="130e2-121">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="130e2-122">Þegar eiginleikinn er sannur birtir hann upplýsingar um tímahólf afhendingar ef slíkt er í boði fyrir vöru til afhendingar</span><span class="sxs-lookup"><span data-stu-id="130e2-122">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="130e2-123">Einingar sem hægt er að nota á staðfestingarsíðu pöntunar</span><span class="sxs-lookup"><span data-stu-id="130e2-123">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="130e2-124">Þegar stofnuð er síða pöntunarstaðfestingar er hægt að bæta við öðrum tengdum einingum til viðbótar við einingu pöntunarstaðfestingar.</span><span class="sxs-lookup"><span data-stu-id="130e2-124">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="130e2-125">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="130e2-125">Here are some examples:</span></span>

- <span data-ttu-id="130e2-126">**Tillögueining** – Bæta má tillögueiningunni við síðu pöntunarstaðfestingar til að veita viðskiptavininum tillögur að öðrum vörum.</span><span class="sxs-lookup"><span data-stu-id="130e2-126">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="130e2-127">**Markaðssetningareiningar** – Hægt er að bæta öllum markaðssetningareiningum á staðfestingarsíðu pöntunar til að sýna markaðsefni.</span><span class="sxs-lookup"><span data-stu-id="130e2-127">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="130e2-128">Bæta upplýsingaeiningu pöntunar við síðu</span><span class="sxs-lookup"><span data-stu-id="130e2-128">Add an order confirmation module to a page</span></span>

<span data-ttu-id="130e2-129">Til að bæta einingu pöntunarstaðfestingar við nýja síðu og stilla nauðsynlega eiginleika skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="130e2-129">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="130e2-130">Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="130e2-130">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="130e2-131">Í svarglugganum **Nýtt sniðmát**, undir **Heiti sniðmáts**, skal slá inn heitið **Sniðmát pöntunarstaðfestingar** og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="130e2-131">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="130e2-132">Í hólfinu **Meginmál**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="130e2-132">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="130e2-133">Í glugganum **Bæta við einingu** skal velja eininguna **Sjálfgefin síða** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="130e2-133">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="130e2-134">Í hólfinu **Aðalsvæði** í einingunni **Sjálfgefin síða** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="130e2-134">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="130e2-135">Í glugganum **Bæta við einingu** skal velja eininguna **Pöntunarstaðfesting** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="130e2-135">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="130e2-136">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="130e2-136">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="130e2-137">Eining pöntunarstaðfestingar verður ekki myndþýdd vegna þess að hún krefst samhengis númers pöntunarstaðfestingarinnar.</span><span class="sxs-lookup"><span data-stu-id="130e2-137">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="130e2-138">Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="130e2-138">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="130e2-139">Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.</span><span class="sxs-lookup"><span data-stu-id="130e2-139">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="130e2-140">Í svarglugganum **Velja sniðmát** skal velja **Sniðmát pöntunarstaðfestingar**.</span><span class="sxs-lookup"><span data-stu-id="130e2-140">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="130e2-141">Undir **Síðuheiti** skal færa inn **Staðfestingarsíða pöntunar** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="130e2-141">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="130e2-142">Í hólfinu **Aðalsvæði** í einingunni **Sjálfgefin síða** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="130e2-142">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="130e2-143">Í glugganum **Bæta við einingu** skal velja eininguna **Pöntunarstaðfesting** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="130e2-143">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="130e2-144">Á eiginleikasvæðinu fyrir einingu pöntunarstaðfestingar skal velja **Fyrirsögn** við hliðina á blýantstákninu.</span><span class="sxs-lookup"><span data-stu-id="130e2-144">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="130e2-145">Í reitinn **Fyrirsagnartexti** í svarglugganum **Fyrirsögn** skal slá inn fyrirsagnartextanum **Staðfesting pöntunar** og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="130e2-145">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="130e2-146">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="130e2-146">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="130e2-147">Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="130e2-147">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="130e2-148">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="130e2-148">Additional resources</span></span>

[<span data-ttu-id="130e2-149">Körfueining</span><span class="sxs-lookup"><span data-stu-id="130e2-149">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="130e2-150">Körfutáknseining</span><span class="sxs-lookup"><span data-stu-id="130e2-150">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="130e2-151">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="130e2-151">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="130e2-152">Greiðslueining</span><span class="sxs-lookup"><span data-stu-id="130e2-152">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="130e2-153">Sendingaraðseturseining</span><span class="sxs-lookup"><span data-stu-id="130e2-153">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="130e2-154">Afhendingarkostaeining</span><span class="sxs-lookup"><span data-stu-id="130e2-154">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="130e2-155">Eining fyrir afhendingarupplýsingar</span><span class="sxs-lookup"><span data-stu-id="130e2-155">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="130e2-156">Gjafakortseining</span><span class="sxs-lookup"><span data-stu-id="130e2-156">Gift card module</span></span>](add-giftcard.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]