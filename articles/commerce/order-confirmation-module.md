---
title: Upplýsingaeining pöntunar
description: Þetta efni fjallar um upplýsingaeiningar pantana og lýsir því hvernig á að nota þær í Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 06/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c2ec629d9fd027be01652351ab1c99001e063e30
ms.sourcegitcommit: 49656661c89c864e8e067259a601c3bbceb8bef4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/18/2020
ms.locfileid: "3464931"
---
# <a name="order-details-module"></a><span data-ttu-id="f1998-103">Upplýsingaeining pöntunar</span><span class="sxs-lookup"><span data-stu-id="f1998-103">Order details module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="f1998-104">Þetta efni fjallar um upplýsingaeiningar pantana og lýsir því hvernig á að nota þær í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f1998-104">This topic covers order details modules and describes how to use them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f1998-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="f1998-105">Overview</span></span>

<span data-ttu-id="f1998-106">Eftir að pöntun hefur verið gerð er hægt að nota staðfestingarhlutann til að sýna staðfestingarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="f1998-106">The order details module is used to show order confirmation details after an order has been placed.</span></span> <span data-ttu-id="f1998-107">Hún sýnir auðkenni pöntunarstaðfestingar, upplýsingar um pöntunarupplýsingar og aðrar pöntunarupplýsingar, svo sem hlutina sem voru keyptir, greiðsluupplýsingar og sendingaraðferð.</span><span class="sxs-lookup"><span data-stu-id="f1998-107">It shows the order confirmation ID, order contact information, and other order details, such as the items that were purchased, payment information, and the shipping method.</span></span>

## <a name="order-details-module-properties"></a><span data-ttu-id="f1998-108">Eiginleikar upplýsingaeiningar pöntunar</span><span class="sxs-lookup"><span data-stu-id="f1998-108">Order details module properties</span></span>

| <span data-ttu-id="f1998-109">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="f1998-109">Property name</span></span>  | <span data-ttu-id="f1998-110">Gildi</span><span class="sxs-lookup"><span data-stu-id="f1998-110">Values</span></span> | <span data-ttu-id="f1998-111">lýsing</span><span class="sxs-lookup"><span data-stu-id="f1998-111">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="f1998-112">Yfirskrift</span><span class="sxs-lookup"><span data-stu-id="f1998-112">Heading</span></span>        | <span data-ttu-id="f1998-113">Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**)</span><span class="sxs-lookup"><span data-stu-id="f1998-113">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="f1998-114">Upplýsingaeining pöntunar getur verið með haus.</span><span class="sxs-lookup"><span data-stu-id="f1998-114">The order details module can have a heading.</span></span> <span data-ttu-id="f1998-115">Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina.</span><span class="sxs-lookup"><span data-stu-id="f1998-115">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="f1998-116">Hins vegar er hægt að breyta merkinu til að uppfylla kröfur um aðgengi.</span><span class="sxs-lookup"><span data-stu-id="f1998-116">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="f1998-117">Númer tengiliðar</span><span class="sxs-lookup"><span data-stu-id="f1998-117">Contact number</span></span> | <span data-ttu-id="f1998-118">Text</span><span class="sxs-lookup"><span data-stu-id="f1998-118">Text</span></span> | <span data-ttu-id="f1998-119">Hægt er að gefa upp tengiliðanúmer fyrir pöntunarskyldar spurningar.</span><span class="sxs-lookup"><span data-stu-id="f1998-119">A contact number can be provided for order-related questions.</span></span> |

## <a name="modules-that-can-be-used-on-an-order-details-page"></a><span data-ttu-id="f1998-120">Einingar sem hægt er að nota á pöntunarupplýsingasíðu</span><span class="sxs-lookup"><span data-stu-id="f1998-120">Modules that can be used on an order details page</span></span>

<span data-ttu-id="f1998-121">Þegar þú býrð til síðu fyrir pöntunarupplýsingar geturðu bætt við öðrum viðeigandi einingum til viðbótar pöntunarupplýsingareiningunni.</span><span class="sxs-lookup"><span data-stu-id="f1998-121">When you create an order details page, you can add other relevant modules in addition to the order details module.</span></span> <span data-ttu-id="f1998-122">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="f1998-122">Here are some examples:</span></span>

- <span data-ttu-id="f1998-123">**Tillögueining** - Hægt er að bæta tillögueiningunni við á upplýsingasíðu pöntunar til að benda viðskiptavinum á aðrar vörur.</span><span class="sxs-lookup"><span data-stu-id="f1998-123">**Recommendations module** – The recommendations module can be added to the order details page to suggest other products to the customer.</span></span>
- <span data-ttu-id="f1998-124">**Markaðseiningar** - Hægt er að bæta hvaða markaðsseining sem er við pöntunarsíðuna til að sýna markaðsefni.</span><span class="sxs-lookup"><span data-stu-id="f1998-124">**Marketing modules** – Any marketing module can be added to the order details page to show marketing content.</span></span>

## <a name="add-an-order-details-module-to-a-page"></a><span data-ttu-id="f1998-125">Bæta upplýsingaeiningu pöntunar við síðu</span><span class="sxs-lookup"><span data-stu-id="f1998-125">Add an order details module to a page</span></span>

<span data-ttu-id="f1998-126">Til að bæta upplýsingaeiningu pöntunar við nýja síðu og stilla nauðsynlega eiginleika skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="f1998-126">To add an order details module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f1998-127">Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="f1998-127">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="f1998-128">Í svarglugganum **Nýtt sniðmát**, undir **Heiti sniðmáts**, skal slá inn heitið **Sniðmát pöntunarupplýsinga** og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f1998-128">In the **New Template** dialog box, under **Template name**, enter the name **Order details template**, and then select **OK**.</span></span>
1. <span data-ttu-id="f1998-129">Í hólfinu **Meginmál**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="f1998-129">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f1998-130">Í glugganum **Bæta við einingu** skal velja eininguna **Sjálfgefin síða** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f1998-130">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f1998-131">Í hólfinu **Aðalsvæði** í einingunni **Sjálfgefin síða** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="f1998-131">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f1998-132">Í svarglugganum **Bæta við einingu** skal velja eininguna **Upplýsingar um pöntun** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f1998-132">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f1998-133">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="f1998-133">Select **Save**, and then select **Preview** to preview the template.</span></span> <span data-ttu-id="f1998-134">Pöntunarupplýsingaeiningin verður ekki látin af hendi sem hún þarf samhengi við pöntunarstaðfestingarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="f1998-134">The order details module won't be rendered, because it requires the context of the order confirmation number.</span></span>
1. <span data-ttu-id="f1998-135">Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="f1998-135">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="f1998-136">Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.</span><span class="sxs-lookup"><span data-stu-id="f1998-136">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="f1998-137">Í svarglugganum **Velja sniðmát** skal velja **Sniðmát pöntunarupplýsinga**.</span><span class="sxs-lookup"><span data-stu-id="f1998-137">In the **Choose a template** dialog box, select **Order details template**.</span></span> <span data-ttu-id="f1998-138">Undir **Síðuheiti** skal færa inn **Upplýsingasíða pöntunar** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f1998-138">Under **Page name**, enter **Order details page**, and then select **OK**.</span></span>
1. <span data-ttu-id="f1998-139">Í hólfinu **Aðalsvæði** í einingunni **Sjálfgefin síða** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="f1998-139">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f1998-140">Í svarglugganum **Bæta við einingu** skal velja eininguna **Upplýsingar um pöntun** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f1998-140">In the **Add Module** dialog box, select the **Order details** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f1998-141">Á eiginleikasvæðinu fyrir upplýsingaeiningu pöntunar skal velja **Fyrirsögn** við hliðina á blýantstákninu.</span><span class="sxs-lookup"><span data-stu-id="f1998-141">In the properties pane for the order details module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="f1998-142">Í reitinn **Fyrirsagnartexti** í svarglugganum **Fyrirsögn** skal slá inn fyrirsagnartextanum **Upplýsingar pöntunar** og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f1998-142">In the **Heading Text** field of the **Heading** dialog box, enter the heading text **Order details**, and then select **OK**.</span></span>
1. <span data-ttu-id="f1998-143">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="f1998-143">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="f1998-144">Veldu**Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="f1998-144">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f1998-145">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f1998-145">Additional resources</span></span>

[<span data-ttu-id="f1998-146">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="f1998-146">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f1998-147">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="f1998-147">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f1998-148">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="f1998-148">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f1998-149">Körfueining</span><span class="sxs-lookup"><span data-stu-id="f1998-149">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f1998-150">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="f1998-150">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f1998-151">Eining síðuhauss</span><span class="sxs-lookup"><span data-stu-id="f1998-151">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f1998-152">Eining síðufótar</span><span class="sxs-lookup"><span data-stu-id="f1998-152">Footer module</span></span>](author-footer-module.md)
