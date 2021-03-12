---
title: Eining pöntunarstaðfestingar
description: Þetta efnisatriði fjallar um staðfestingareiningar og lýsir því hvernig á að notar þær í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/06/2020
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
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9d916d2687777403f2b0df7c35171948ad2fb7db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4972745"
---
# <a name="order-confirmation-module"></a><span data-ttu-id="95ece-103">Eining pöntunarstaðfestingar</span><span class="sxs-lookup"><span data-stu-id="95ece-103">Order confirmation module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="95ece-104">Þetta efnisatriði fjallar um staðfestingareiningar og lýsir því hvernig á að notar þær í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="95ece-104">This topic covers order confirmation modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="95ece-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="95ece-105">Overview</span></span>

<span data-ttu-id="95ece-106">Pöntunarstaðfestingareiningin er notuð til að sýna upplýsingar pöntunarstaðfestinga eftir að pöntun hefur verið gerð.</span><span class="sxs-lookup"><span data-stu-id="95ece-106">The order confirmation module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="95ece-107">Hún sýnir staðfestingarkenni pöntunar, tengslaupplýsingar pöntunar og aðrar upplýsingar um pöntun, svo sem vörur sem voru keyptar, greiðsluupplýsingar, afhendingarmáta og sendingaraðferð.</span><span class="sxs-lookup"><span data-stu-id="95ece-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, pickup options, and the shipping method.</span></span>

## <a name="order-confirmation-module-properties"></a><span data-ttu-id="95ece-108">Eiginleikar staðfestingareiningar pöntunar</span><span class="sxs-lookup"><span data-stu-id="95ece-108">Order confirmation module properties</span></span>

| <span data-ttu-id="95ece-109">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="95ece-109">Property name</span></span>  | <span data-ttu-id="95ece-110">Gildi</span><span class="sxs-lookup"><span data-stu-id="95ece-110">Values</span></span> | <span data-ttu-id="95ece-111">Lýsing</span><span class="sxs-lookup"><span data-stu-id="95ece-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="95ece-112">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="95ece-112">Heading</span></span>        | <span data-ttu-id="95ece-113">Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**)</span><span class="sxs-lookup"><span data-stu-id="95ece-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="95ece-114">Pöntunarstaðfestingareiningin getur haft fyrirsögn.</span><span class="sxs-lookup"><span data-stu-id="95ece-114">The order confirmation module can have a heading.</span></span> <span data-ttu-id="95ece-115">Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina.</span><span class="sxs-lookup"><span data-stu-id="95ece-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="95ece-116">Hins vegar er hægt að breyta merkinu til að uppfylla kröfur um aðgengi.</span><span class="sxs-lookup"><span data-stu-id="95ece-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="95ece-117">Númer tengiliðar</span><span class="sxs-lookup"><span data-stu-id="95ece-117">Contact number</span></span> | <span data-ttu-id="95ece-118">Text</span><span class="sxs-lookup"><span data-stu-id="95ece-118">Text</span></span> | <span data-ttu-id="95ece-119">Hægt er að gefa upp tengiliðanúmer fyrir pöntunarskyldar spurningar.</span><span class="sxs-lookup"><span data-stu-id="95ece-119">A contact number can be provided for order-related questions.</span></span> |
| <span data-ttu-id="95ece-120">Sýna upplýsingar um tímahólf afhendingar</span><span class="sxs-lookup"><span data-stu-id="95ece-120">Show pickup timeslot information</span></span> | <span data-ttu-id="95ece-121">Satt eða ósatt</span><span class="sxs-lookup"><span data-stu-id="95ece-121">True or False</span></span> | <span data-ttu-id="95ece-122">Þessi eiginleiki er í boði í Dynamics 365 Commerce 10.0.15 og ´nýrri.</span><span class="sxs-lookup"><span data-stu-id="95ece-122">This property is available in Dynamics 365 Commerce 10.0.15 and higher.</span></span> <span data-ttu-id="95ece-123">Þegar eiginleikinn er sannur birtir hann upplýsingar um tímahólf afhendingar ef slíkt er í boði fyrir vöru til afhendingar</span><span class="sxs-lookup"><span data-stu-id="95ece-123">When true, it displays the pickup timeslot information if provided for a pickup item</span></span>|

## <a name="modules-that-can-be-used-on-an-order-confirmation-page"></a><span data-ttu-id="95ece-124">Einingar sem hægt er að nota á staðfestingarsíðu pöntunar</span><span class="sxs-lookup"><span data-stu-id="95ece-124">Modules that can be used on an order confirmation page</span></span>

<span data-ttu-id="95ece-125">Þegar stofnuð er síða pöntunarstaðfestingar er hægt að bæta við öðrum tengdum einingum til viðbótar við einingu pöntunarstaðfestingar.</span><span class="sxs-lookup"><span data-stu-id="95ece-125">When you create an order confirmation page, you can add other relevant modules in addition to the order confirmation module.</span></span> <span data-ttu-id="95ece-126">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="95ece-126">Here are some examples:</span></span>

- <span data-ttu-id="95ece-127">**Tillögueining** – Bæta má tillögueiningunni við síðu pöntunarstaðfestingar til að veita viðskiptavininum tillögur að öðrum vörum.</span><span class="sxs-lookup"><span data-stu-id="95ece-127">**Recommendations module** – The recommendations module can be added to the order confirmation page to suggest other products to the customer.</span></span>
- <span data-ttu-id="95ece-128">**Markaðssetningareiningar** – Hægt er að bæta öllum markaðssetningareiningum á staðfestingarsíðu pöntunar til að sýna markaðsefni.</span><span class="sxs-lookup"><span data-stu-id="95ece-128">**Marketing modules** – Any marketing module can be added to the order confirmation page to show marketing content.</span></span>

## <a name="add-an-order-confirmation-module-to-a-page"></a><span data-ttu-id="95ece-129">Bæta upplýsingaeiningu pöntunar við síðu</span><span class="sxs-lookup"><span data-stu-id="95ece-129">Add an order confirmation module to a page</span></span>

<span data-ttu-id="95ece-130">Til að bæta einingu pöntunarstaðfestingar við nýja síðu og stilla nauðsynlega eiginleika skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="95ece-130">To add an order confirmation module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="95ece-131">Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="95ece-131">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="95ece-132">Í svarglugganum **Nýtt sniðmát**, undir **Heiti sniðmáts**, skal slá inn heitið **Sniðmát pöntunarstaðfestingar** og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="95ece-132">In the **New Template** dialog box, under **Template name**, enter the name **Order confirmation template**, and then select **OK**.</span></span>
1. <span data-ttu-id="95ece-133">Í hólfinu **Meginmál**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="95ece-133">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="95ece-134">Í glugganum **Bæta við einingu** skal velja eininguna **Sjálfgefin síða** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="95ece-134">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="95ece-135">Í hólfinu **Aðalsvæði** í einingunni **Sjálfgefin síða** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="95ece-135">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="95ece-136">Í glugganum **Bæta við einingu** skal velja eininguna **Pöntunarstaðfesting** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="95ece-136">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="95ece-137">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="95ece-137">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="95ece-138">Eining pöntunarstaðfestingar verður ekki myndþýdd vegna þess að hún krefst samhengis númers pöntunarstaðfestingarinnar.</span><span class="sxs-lookup"><span data-stu-id="95ece-138">The order confirmation module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="95ece-139">Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="95ece-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="95ece-140">Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.</span><span class="sxs-lookup"><span data-stu-id="95ece-140">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="95ece-141">Í svarglugganum **Velja sniðmát** skal velja **Sniðmát pöntunarstaðfestingar**.</span><span class="sxs-lookup"><span data-stu-id="95ece-141">In the **Choose a template** dialog box, select **Order confirmation template**.</span></span> <span data-ttu-id="95ece-142">Undir **Síðuheiti** skal færa inn **Staðfestingarsíða pöntunar** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="95ece-142">Under **Page name**, enter **Order confirmation page**, and then select **OK**.</span></span>
1. <span data-ttu-id="95ece-143">Í hólfinu **Aðalsvæði** í einingunni **Sjálfgefin síða** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="95ece-143">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="95ece-144">Í glugganum **Bæta við einingu** skal velja eininguna **Pöntunarstaðfesting** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="95ece-144">In the **Add Module** dialog box, select the **Order confirmation** module, and then select **OK**.</span></span>
1. <span data-ttu-id="95ece-145">Á eiginleikasvæðinu fyrir einingu pöntunarstaðfestingar skal velja **Fyrirsögn** við hliðina á blýantstákninu.</span><span class="sxs-lookup"><span data-stu-id="95ece-145">In the properties pane for the order confirmation module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="95ece-146">Í reitinn **Fyrirsagnartexti** í svarglugganum **Fyrirsögn** skal slá inn fyrirsagnartextanum **Staðfesting pöntunar** og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="95ece-146">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order confirmation**, and then select **OK**.</span></span>
1. <span data-ttu-id="95ece-147">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="95ece-147">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="95ece-148">Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="95ece-148">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="95ece-149">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="95ece-149">Additional resources</span></span>

[<span data-ttu-id="95ece-150">Körfueining</span><span class="sxs-lookup"><span data-stu-id="95ece-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="95ece-151">Körfutáknseining</span><span class="sxs-lookup"><span data-stu-id="95ece-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="95ece-152">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="95ece-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="95ece-153">Greiðslueining</span><span class="sxs-lookup"><span data-stu-id="95ece-153">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="95ece-154">Sendingaraðseturseining</span><span class="sxs-lookup"><span data-stu-id="95ece-154">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="95ece-155">Afhendingarkostaeining</span><span class="sxs-lookup"><span data-stu-id="95ece-155">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="95ece-156">Eining fyrir afhendingarupplýsingar</span><span class="sxs-lookup"><span data-stu-id="95ece-156">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="95ece-157">Gjafakortseining</span><span class="sxs-lookup"><span data-stu-id="95ece-157">Gift card module</span></span>](add-giftcard.md)
