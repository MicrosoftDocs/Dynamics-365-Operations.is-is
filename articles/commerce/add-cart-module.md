---
title: Körfueining
description: Þetta efni fjallar um körfueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.openlocfilehash: 33db06ecfa2a8fa93cde3c4f1b31d6b30bfd0c34
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/07/2020
ms.locfileid: "4413316"
---
# <a name="cart-module"></a><span data-ttu-id="222f1-103">Körfueining</span><span class="sxs-lookup"><span data-stu-id="222f1-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="222f1-104">Þetta efni fjallar um körfueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="222f1-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="222f1-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="222f1-105">Overview</span></span>

<span data-ttu-id="222f1-106">Körfueining sýnir hluti sem hafa verið settir í körfuna áður en viðskiptavinurinn heldur áfram að kassa.</span><span class="sxs-lookup"><span data-stu-id="222f1-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="222f1-107">Einingin sýnir einnig samantekt á pöntun og gerir viðskiptavininum kleift að beita eða fjarlægja kynningarkóða.</span><span class="sxs-lookup"><span data-stu-id="222f1-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="222f1-108">Körfueiningin styður innskráð greiðsluferli og greiðslu sem gestur.</span><span class="sxs-lookup"><span data-stu-id="222f1-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="222f1-109">Hún styður einnig tengilinn **Til baka í verslun**.</span><span class="sxs-lookup"><span data-stu-id="222f1-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="222f1-110">Þú getur stillt leiðina fyrir þennan hlekk á **Svæðisstillingar \> Viðbætur \> Leiðir**.</span><span class="sxs-lookup"><span data-stu-id="222f1-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="222f1-111">Í körfueiningunni eru gögn byggð á körfuauðkenninu, sem er vafrakaka sem hægt er að nálgast á vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="222f1-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="222f1-112">Eftirfarandi mynd sýnir dæmi um körfusíðu á Fabrikam-svæðinu.</span><span class="sxs-lookup"><span data-stu-id="222f1-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Dæmi um körfueiningu á Fabrikam-síðu](./media/cart2.PNG)

<span data-ttu-id="222f1-114">Eftirfarandi mynd sýnir dæmi um körfusíðu á Fabrikam-svæðinu.</span><span class="sxs-lookup"><span data-stu-id="222f1-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="222f1-115">Í þessu dæmi er afgreiðslugjald fyrir línuatriði.</span><span class="sxs-lookup"><span data-stu-id="222f1-115">In this example, there is a handling fee for a line item.</span></span>

![Dæmi um körfueiningu með umsýslugjaldi fyrir línuatriði](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="222f1-117">Eiginleikar og hólf körfueininga</span><span class="sxs-lookup"><span data-stu-id="222f1-117">Cart module properties and slots</span></span>

| <span data-ttu-id="222f1-118">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="222f1-118">Property</span></span> | <span data-ttu-id="222f1-119">Gildi</span><span class="sxs-lookup"><span data-stu-id="222f1-119">Values</span></span> | <span data-ttu-id="222f1-120">lýsing</span><span class="sxs-lookup"><span data-stu-id="222f1-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="222f1-121">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="222f1-121">Heading</span></span> | <span data-ttu-id="222f1-122">Fyrirsagnartexti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**)</span><span class="sxs-lookup"><span data-stu-id="222f1-122">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="222f1-123">Fyrirsögn fyrir körfuna, t.d. „Innkaupakarfa“ eða „Vörur í körfunni þinni“.</span><span class="sxs-lookup"><span data-stu-id="222f1-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="222f1-124">Sýna villuboðin Ekki til á lager</span><span class="sxs-lookup"><span data-stu-id="222f1-124">Show out of stock errors</span></span> | <span data-ttu-id="222f1-125">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="222f1-125">**True** or **False**</span></span> | <span data-ttu-id="222f1-126">Ef þessi eiginleiki er stilltur á **Sat** sýnir körfusíðan villur sem tengjast birgðum.</span><span class="sxs-lookup"><span data-stu-id="222f1-126">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="222f1-127">Mælt er með því að þessi eiginleiki sé stilltur á **Satt** ef birgðaathuganir eru notaðar á svæðinu.</span><span class="sxs-lookup"><span data-stu-id="222f1-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="222f1-128">Sýna sendingargjöld fyrir línuatriði</span><span class="sxs-lookup"><span data-stu-id="222f1-128">Show shipping charges for line items</span></span> | <span data-ttu-id="222f1-129">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="222f1-129">**True** or **False**</span></span> | <span data-ttu-id="222f1-130">Ef þessi eiginleiki er stilltur á **Satt** sýna línuatriði körfu sendingargjöld, ef þessar upplýsingar eru í boði.</span><span class="sxs-lookup"><span data-stu-id="222f1-130">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="222f1-131">Þessi eiginleiki er ekki studdur í Fabrikam-skemanu því að notendur velja sendingu eingöngu í greiðsluferlinu.</span><span class="sxs-lookup"><span data-stu-id="222f1-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="222f1-132">Hins vegar er hægt að kveikja á þessum eiginleika í öðrum verkflæðum ef það á við.</span><span class="sxs-lookup"><span data-stu-id="222f1-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="222f1-133">Einingar sem hægt er að nota í körfueiningu</span><span class="sxs-lookup"><span data-stu-id="222f1-133">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="222f1-134">**Textabálkur** – Þessi eining styður sérsniðin skilaboð í körfueiningunni.</span><span class="sxs-lookup"><span data-stu-id="222f1-134">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="222f1-135">Skilaboðin eru keyrð af efnisstjórnunarkerfinu (CMS).</span><span class="sxs-lookup"><span data-stu-id="222f1-135">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="222f1-136">Hægt er að bæta við hvaða skilaboðum sem er, eins og „Vegna vandamála með pöntunina, hafið samband við 1-800-Fabrikam.“</span><span class="sxs-lookup"><span data-stu-id="222f1-136">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="222f1-137">**Verslunarval** – Þessi eining sýnir lista yfir nærliggjandi verslanir þar sem hægt er að sækja vöru.</span><span class="sxs-lookup"><span data-stu-id="222f1-137">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="222f1-138">Það gerir notendum kleift að slá inn staðsetningu til að finna verslanir í nágrenninu.</span><span class="sxs-lookup"><span data-stu-id="222f1-138">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="222f1-139">Fyrir frekari upplýsingar um þessa einingu, sjá [Verslunarvalseiningu](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="222f1-139">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="222f1-140">Eiginleikar einingar</span><span class="sxs-lookup"><span data-stu-id="222f1-140">Module properties</span></span>

<span data-ttu-id="222f1-141">Hægt er að skilgreina eftirfarandi stillingar fyrir körfueiningar á **Stillingar svæðis \> viðbætur**:</span><span class="sxs-lookup"><span data-stu-id="222f1-141">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="222f1-142">**Hámarksmagn** - Þessi eiginleiki er notaður til að tilgreina hámarksfjölda hvers hlutar sem hægt er að bæta við körfuna.</span><span class="sxs-lookup"><span data-stu-id="222f1-142">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="222f1-143">Til dæmis gæti smásali ákveðið að aðeins megi selja 10 stykki af hverri afurð í sömu færslunni.</span><span class="sxs-lookup"><span data-stu-id="222f1-143">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="222f1-144">**Birgðir** - Frekari upplýsingar um hvernig á að nota birgðastillingar er að finna í [Nota birgðastillingar](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="222f1-144">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="222f1-145">**Til baka í verslun** - Þessi eiginleiki er notaður til að tilgreina leiðina fyrir tengilinn **Til baka í verslun**.</span><span class="sxs-lookup"><span data-stu-id="222f1-145">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="222f1-146">Hægt er að stilla leiðina á vettvangsstigi, sem gerir smásöluaðilum kleift að fara með viðskiptavininn aftur á heimasíðuna eða aðra síðu á síðunni.</span><span class="sxs-lookup"><span data-stu-id="222f1-146">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="222f1-147">Í Dynamics 365 Commerce 10.0.14 útgáfu og síðar eru vörur í körfunni uppsafnaðar á grundvelli stillinga sem eru skilgreindar í virkniforstillingu á netinu fyrir netverslunina í höfuðstöðvum Commerce.</span><span class="sxs-lookup"><span data-stu-id="222f1-147">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="222f1-148">Frekari upplýsingar um hvernig á að stofna virkniforstillingu á netinu og stilla eiginleikana sem þarf fyrir uppsöfnun er að finna í [Búa til virkniforstillingu á netinu](online-functionality-profile.md).</span><span class="sxs-lookup"><span data-stu-id="222f1-148">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="222f1-149">Samskipti við Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="222f1-149">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="222f1-150">Körfueiningin sækir upplýsingar um afurðir með API kvörðunareiningu fyrir Commerce.</span><span class="sxs-lookup"><span data-stu-id="222f1-150">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="222f1-151">Auðkenni körfunnar frá vafrakökunni er notað til að sækja allar vöruupplýsingar frá Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="222f1-151">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="222f1-152">Bæta körfueiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="222f1-152">Add a cart module to a page</span></span>

<span data-ttu-id="222f1-153">Fylgdu þessum skrefum til að bæta körfueiningu við nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="222f1-153">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="222f1-154">Farðu í **Brot** og veldu **Nýtt** til að búa til nýtt brot.</span><span class="sxs-lookup"><span data-stu-id="222f1-154">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="222f1-155">Í svarglugganum **Nýtt brot** skal velja eininguna **Karfa**.</span><span class="sxs-lookup"><span data-stu-id="222f1-155">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="222f1-156">Undir **Heiti brots** skal slá inn heitið **Körfubrot** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="222f1-156">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="222f1-157">Veldu hólfið **Karfa**.</span><span class="sxs-lookup"><span data-stu-id="222f1-157">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="222f1-158">Hægra megin á eiginleikasvæðinu skal velja blýantstáknið, slá inn texta fyrirsagnar í reitinn og síðan velja gátmerkistáknið.</span><span class="sxs-lookup"><span data-stu-id="222f1-158">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="222f1-159">Í hólfinu **Karfa**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="222f1-159">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="222f1-160">Í glugganum **Bæta við einingu** skal velja eininguna **Verslunarval** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="222f1-160">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="222f1-161">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="222f1-161">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="222f1-162">Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="222f1-162">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="222f1-163">Í svarglugganum **Nýtt sniðmát**, undir **Heiti sniðmáts**, skal slá inn heiti fyrir sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="222f1-163">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="222f1-164">Í trjáskipulaginu skal velja hólfið **Meginmál**, velja úrfellingarmerkið (**...**), og síðan velja **Bæta við broti**.</span><span class="sxs-lookup"><span data-stu-id="222f1-164">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="222f1-165">Í svarglugganum **Velja brot** skal velja síðubrotið **Körfubrot** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="222f1-165">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="222f1-166">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="222f1-166">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="222f1-167">Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.</span><span class="sxs-lookup"><span data-stu-id="222f1-167">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="222f1-168">Í glugganum **Velja sniðmát** skal velja sniðmátið sem var búið til, slá inn síðuheiti og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="222f1-168">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="222f1-169">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="222f1-169">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="222f1-170">Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="222f1-170">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="222f1-171">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="222f1-171">Additional resources</span></span>

[<span data-ttu-id="222f1-172">Körfutáknseining</span><span class="sxs-lookup"><span data-stu-id="222f1-172">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="222f1-173">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="222f1-173">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="222f1-174">Greiðslueining</span><span class="sxs-lookup"><span data-stu-id="222f1-174">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="222f1-175">Sendingaraðseturseining</span><span class="sxs-lookup"><span data-stu-id="222f1-175">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="222f1-176">Afhendingarkostaeining</span><span class="sxs-lookup"><span data-stu-id="222f1-176">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="222f1-177">Eining fyrir afhendingarupplýsingar</span><span class="sxs-lookup"><span data-stu-id="222f1-177">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="222f1-178">Pöntunarupplýsingaeining</span><span class="sxs-lookup"><span data-stu-id="222f1-178">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="222f1-179">Gjafakortseining</span><span class="sxs-lookup"><span data-stu-id="222f1-179">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="222f1-180">Reikna tiltækar birgðir fyrir smásölurásir</span><span class="sxs-lookup"><span data-stu-id="222f1-180">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="222f1-181">Búa til virkniforstillingu á netinu</span><span class="sxs-lookup"><span data-stu-id="222f1-181">Create an online functionality profile</span></span>](online-functionality-profile.md)
