---
title: Körfueining
description: Þetta efni fjallar um körfueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 3ba46fd90507a9cf8da92598c8449a2e553da352
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411274"
---
# <a name="cart-module"></a><span data-ttu-id="a6029-103">Körfueining</span><span class="sxs-lookup"><span data-stu-id="a6029-103">Cart module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a6029-104">Þetta efni fjallar um körfueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a6029-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a6029-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="a6029-105">Overview</span></span>

<span data-ttu-id="a6029-106">Körfueining sýnir hluti sem hafa verið settir í körfuna áður en viðskiptavinurinn heldur áfram að kassa.</span><span class="sxs-lookup"><span data-stu-id="a6029-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="a6029-107">Einingin sýnir einnig samantekt á pöntun og gerir viðskiptavininum kleift að beita eða fjarlægja kynningarkóða.</span><span class="sxs-lookup"><span data-stu-id="a6029-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="a6029-108">Körfueiningin styður innskráð greiðsluferli og greiðslu sem gestur.</span><span class="sxs-lookup"><span data-stu-id="a6029-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="a6029-109">Hún styður einnig tengilinn **Til baka í verslun**.</span><span class="sxs-lookup"><span data-stu-id="a6029-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="a6029-110">Þú getur stillt leiðina fyrir þennan hlekk á **Svæðisstillingar \> Viðbætur \> Leiðir**.</span><span class="sxs-lookup"><span data-stu-id="a6029-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="a6029-111">Í körfueiningunni eru gögn byggð á körfuauðkenninu, sem er vafrakaka sem hægt er að nálgast á vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="a6029-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="a6029-112">Eftirfarandi mynd sýnir dæmi um körfusíðu á Fabrikam-svæðinu.</span><span class="sxs-lookup"><span data-stu-id="a6029-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Dæmi um körfueiningu](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="a6029-114">Eiginleikar og hólf körfueininga</span><span class="sxs-lookup"><span data-stu-id="a6029-114">Cart module properties and slots</span></span>

<span data-ttu-id="a6029-115">Körfueiningin er með eiginleikann **Fyrirsögn** sem hægt er að stilla á gildi eins og **Innkaupapoki** og **Vörur í körfunni þinni**.</span><span class="sxs-lookup"><span data-stu-id="a6029-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="a6029-116">Einingar sem hægt er að nota í körfueiningu</span><span class="sxs-lookup"><span data-stu-id="a6029-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="a6029-117">**Textabálkur** – Þessi eining styður sérsniðin skilaboð í körfueiningunni.</span><span class="sxs-lookup"><span data-stu-id="a6029-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="a6029-118">Skilaboðin eru keyrð af efnisstjórnunarkerfinu (CMS).</span><span class="sxs-lookup"><span data-stu-id="a6029-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="a6029-119">Hægt er að bæta við hvaða skilaboðum sem er, eins og „Vegna vandamála með pöntunina, hafið samband við 1-800-Fabrikam.“</span><span class="sxs-lookup"><span data-stu-id="a6029-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="a6029-120">**Verslunarval** – Þessi eining sýnir lista yfir nærliggjandi verslanir þar sem hægt er að sækja vöru.</span><span class="sxs-lookup"><span data-stu-id="a6029-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="a6029-121">Það gerir notendum kleift að slá inn staðsetningu til að finna verslanir í nágrenninu.</span><span class="sxs-lookup"><span data-stu-id="a6029-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="a6029-122">Fyrir frekari upplýsingar um þessa einingu, sjá [Verslunarvalseiningu](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="a6029-122">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="a6029-123">Eiginleikar einingar</span><span class="sxs-lookup"><span data-stu-id="a6029-123">Module properties</span></span>

<span data-ttu-id="a6029-124">Hægt er að skilgreina eftirfarandi stillingar fyrir körfueiningar á **Stillingar svæðis \> viðbætur**:</span><span class="sxs-lookup"><span data-stu-id="a6029-124">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="a6029-125">**Hámarksmagn** - Þessi eiginleiki er notaður til að tilgreina hámarksfjölda hvers hlutar sem hægt er að bæta við körfuna.</span><span class="sxs-lookup"><span data-stu-id="a6029-125">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="a6029-126">Til dæmis gæti smásali ákveðið að aðeins megi selja 10 stykki af hverri afurð í sömu færslunni.</span><span class="sxs-lookup"><span data-stu-id="a6029-126">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="a6029-127">**Birgðir** - Frekari upplýsingar um hvernig á að nota birgðastillingar er að finna í [Nota birgðastillingar](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="a6029-127">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="a6029-128">**Til baka í verslun** - Þessi eiginleiki er notaður til að tilgreina leiðina fyrir tengilinn **Til baka í verslun**.</span><span class="sxs-lookup"><span data-stu-id="a6029-128">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="a6029-129">Hægt er að stilla leiðina á vettvangsstigi, sem gerir smásöluaðilum kleift að fara með viðskiptavininn aftur á heimasíðuna eða aðra síðu á síðunni.</span><span class="sxs-lookup"><span data-stu-id="a6029-129">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="a6029-130">Samskipti við Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="a6029-130">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="a6029-131">Körfueiningin sækir upplýsingar um afurðir með API kvörðunareiningu fyrir Commerce.</span><span class="sxs-lookup"><span data-stu-id="a6029-131">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="a6029-132">Auðkenni körfunnar frá vafrakökunni er notað til að sækja allar vöruupplýsingar frá Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="a6029-132">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="a6029-133">Bæta körfueiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="a6029-133">Add a cart module to a page</span></span>

<span data-ttu-id="a6029-134">Fylgdu þessum skrefum til að bæta körfueiningu við nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="a6029-134">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a6029-135">Farðu í **Síðubrot** og veldu **Nýtt** til að búa til nýtt síðubrot.</span><span class="sxs-lookup"><span data-stu-id="a6029-135">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="a6029-136">Í svarglugganum **Nýtt síðubrot** skal velja eininguna **Karfa**.</span><span class="sxs-lookup"><span data-stu-id="a6029-136">In the **New Page Fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="a6029-137">Undir **Heiti síðubrots** skal slá inn heitið **Körfubrot** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a6029-137">Under **Page Fragment Name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="a6029-138">Veldu hólfið **Karfa**.</span><span class="sxs-lookup"><span data-stu-id="a6029-138">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="a6029-139">Hægra megin á eiginleikasvæðinu skal velja blýantstáknið, slá inn texta fyrirsagnar í reitinn og síðan velja gátmerkistáknið.</span><span class="sxs-lookup"><span data-stu-id="a6029-139">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="a6029-140">Í hólfinu **Karfa**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="a6029-140">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a6029-141">Í glugganum **Bæta við einingu** skal velja eininguna **Verslunarval** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a6029-141">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a6029-142">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="a6029-142">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="a6029-143">Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="a6029-143">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="a6029-144">Í svarglugganum **Nýtt sniðmát**, undir **Heiti sniðmáts**, skal slá inn heiti fyrir sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="a6029-144">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="a6029-145">Í trjáskipulaginu skal velja hólfið **Meginmál**, velja úrfellingarmerkið (**...**), og síðan velja **Bæta við broti**.</span><span class="sxs-lookup"><span data-stu-id="a6029-145">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="a6029-146">Í svarglugganum **Velja síðubrot** skal velja síðubrotið **Körfubrot** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a6029-146">In the **Select Page Fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="a6029-147">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="a6029-147">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="a6029-148">Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.</span><span class="sxs-lookup"><span data-stu-id="a6029-148">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="a6029-149">Í glugganum **Velja sniðmát** skal velja sniðmátið sem var búið til, slá inn síðuheiti og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a6029-149">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="a6029-150">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="a6029-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="a6029-151">Veldu**Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="a6029-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a6029-152">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a6029-152">Additional resources</span></span>

[<span data-ttu-id="a6029-153">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="a6029-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a6029-154">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="a6029-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="a6029-155">Vista valeiningu</span><span class="sxs-lookup"><span data-stu-id="a6029-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="a6029-156">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="a6029-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="a6029-157">Körfutáknseining</span><span class="sxs-lookup"><span data-stu-id="a6029-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="a6029-158">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="a6029-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a6029-159">Eining pöntunarstaðfestingar</span><span class="sxs-lookup"><span data-stu-id="a6029-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="a6029-160">Eining síðuhauss</span><span class="sxs-lookup"><span data-stu-id="a6029-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="a6029-161">Eining síðufótar</span><span class="sxs-lookup"><span data-stu-id="a6029-161">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="a6029-162">Reikna tiltækar birgðir fyrir smásölurásir</span><span class="sxs-lookup"><span data-stu-id="a6029-162">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
