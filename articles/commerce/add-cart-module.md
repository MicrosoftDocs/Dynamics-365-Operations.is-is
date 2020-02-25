---
title: Körfueining
description: Þetta efni fjallar um körfueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025437"
---
# <a name="cart-module"></a><span data-ttu-id="c9355-103">Körfueining</span><span class="sxs-lookup"><span data-stu-id="c9355-103">Cart module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c9355-104">Þetta efni fjallar um körfueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c9355-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c9355-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="c9355-105">Overview</span></span>

<span data-ttu-id="c9355-106">Körfueining er notuð til að sýna hluti sem hafa verið settir í körfuna áður en viðskiptavinurinn heldur áfram að kassa.</span><span class="sxs-lookup"><span data-stu-id="c9355-106">A cart module is used to show the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="c9355-107">Til dæmis felur hún í sér alla hluti sem hafa verið settir í körfuna og samantekt pöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="c9355-107">For example, it includes all the items that have been added to the cart and an order summary.</span></span> <span data-ttu-id="c9355-108">Það gerir viðskiptavininum einnig kleift að beita eða fjarlægja kynningarkóða.</span><span class="sxs-lookup"><span data-stu-id="c9355-108">It also lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="c9355-109">Körfueiningin styður innskráð greiðsluferli og greiðslu sem gestur.</span><span class="sxs-lookup"><span data-stu-id="c9355-109">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="c9355-110">Hún styður einnig tengilinn **Til baka í verslun**.</span><span class="sxs-lookup"><span data-stu-id="c9355-110">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="c9355-111">Þú getur stillt leiðina fyrir þennan hlekk á **Svæðisstillingar \> Viðbætur \> Leiðir**.</span><span class="sxs-lookup"><span data-stu-id="c9355-111">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="c9355-112">Í körfueiningunni eru gögn byggð á auðkenni körfunnar.</span><span class="sxs-lookup"><span data-stu-id="c9355-112">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="c9355-113">Auðkenni körfunnar er vafrakaka sem er fáanleg á þessu svæði.</span><span class="sxs-lookup"><span data-stu-id="c9355-113">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="c9355-114">Eiginleikar og hólf körfueininga</span><span class="sxs-lookup"><span data-stu-id="c9355-114">Cart module properties and slots</span></span>

<span data-ttu-id="c9355-115">Körfueiningin er með eiginleikann **Fyrirsögn** sem hægt er að stilla á gildi eins og **Innkaupapoki** og **Vörur í körfunni þinni**.</span><span class="sxs-lookup"><span data-stu-id="c9355-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="c9355-116">Einingar sem hægt er að nota í körfueiningu</span><span class="sxs-lookup"><span data-stu-id="c9355-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="c9355-117">**Textabálkur** – Þessi eining styður sérsniðin skilaboð í körfueiningunni.</span><span class="sxs-lookup"><span data-stu-id="c9355-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="c9355-118">Skilaboðin eru keyrð af efnisstjórnunarkerfinu (CMS).</span><span class="sxs-lookup"><span data-stu-id="c9355-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="c9355-119">Hægt er að bæta við hvaða skilaboðum sem er, eins og „Vegna vandamála með pöntunina, hafið samband við 1-800-Fabrikam.“</span><span class="sxs-lookup"><span data-stu-id="c9355-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="c9355-120">**Verslunarval** – Þessi eining sýnir lista yfir nærliggjandi verslanir þar sem hægt er að sækja vöru.</span><span class="sxs-lookup"><span data-stu-id="c9355-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="c9355-121">Það gerir notendum kleift að slá inn staðsetningu til að finna verslanir í nágrenninu.</span><span class="sxs-lookup"><span data-stu-id="c9355-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="c9355-122">Verslunarvalseiningin er samþætt við Bing Maps Geocoding forritunarviðmót (API) landskóðunar til að umbreyta staðsetningunni í breiddar- og lengdargráðu.</span><span class="sxs-lookup"><span data-stu-id="c9355-122">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="c9355-123">Bing Maps API lykils er krafist og bæta verður honum við Retail sameiginlegar færibreytusíðuna í Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="c9355-123">A Bing Maps API key is required and must be added to the Retail shared parameters page in Dynamics 365 Retail.</span></span> <span data-ttu-id="c9355-124">Þessi eining styður tvo eiginleika, **Leitarradíus** og **Tengil í þjónustuskilmála**.</span><span class="sxs-lookup"><span data-stu-id="c9355-124">This module supports two properties, **Search radius** and **Terms of service link**.</span></span> <span data-ttu-id="c9355-125">Eiginleikinn **Leitarradíus** skilgreinir leitarradíus fyrir verslanir, í mílum.</span><span class="sxs-lookup"><span data-stu-id="c9355-125">The **Search radius** property defines the search radius for stores, in miles.</span></span> <span data-ttu-id="c9355-126">Ef ekkert gildi er tilgreint er sjálfgefinn leitarradíus notaður, 50 mílur.</span><span class="sxs-lookup"><span data-stu-id="c9355-126">If no value is specified, the default search radius, 50 miles, is used.</span></span> <span data-ttu-id="c9355-127">Ef Bings kort eða utanaðkomandi þjónusta er notuð er hægt að nota eiginleikann **Tengill í þjónustuskilmála** til að veita tengil á þjónustuskilmálana.</span><span class="sxs-lookup"><span data-stu-id="c9355-127">If Bings Maps or any external service is used, the **Terms of service link** property can be used to provide a link to the terms of service.</span></span> <span data-ttu-id="c9355-128">Þjónustuskilmálatengils er krafist fyrir þjónustuna Bing Maps.</span><span class="sxs-lookup"><span data-stu-id="c9355-128">A terms of service link is required for the Bing Maps service.</span></span> 

## <a name="cart-module-settings"></a><span data-ttu-id="c9355-129">Stillingar körfueiningar</span><span class="sxs-lookup"><span data-stu-id="c9355-129">Cart module settings</span></span>

<span data-ttu-id="c9355-130">Körfueiningar hafa eftirfarandi stillingar sem hægt er að stilla á **Svæðisstillingar \> Viðbætur**:</span><span class="sxs-lookup"><span data-stu-id="c9355-130">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="c9355-131">**Hámarksmagn** - Þessi eiginleiki er notaður til að tilgreina hámarksfjölda hvers hlutar sem hægt er að bæta við körfuna.</span><span class="sxs-lookup"><span data-stu-id="c9355-131">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="c9355-132">Til dæmis gæti smásali ákveðið að aðeins megi selja 10 stykki af hverri afurð í sömu færslunni.</span><span class="sxs-lookup"><span data-stu-id="c9355-132">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="c9355-133">**Birgðakönnun** - Þegar gildi er stillt á **Satt** er vara aðeins sett í körfuna eftir að kaupkassaeiningin tryggir að hún sé til á lager.</span><span class="sxs-lookup"><span data-stu-id="c9355-133">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="c9355-134">Þessi úttekt á birgðum er gerð bæði fyrir atburðarás þar sem hluturinn verður sendur og fyrir atburðarás þar sem hann verður sóttur í verslunina.</span><span class="sxs-lookup"><span data-stu-id="c9355-134">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="c9355-135">Ef gildi er stillt á **Rangt** er engin úttekt á birgðum gerð áður en hlutur er settur í körfuna og pöntunin er gerð.</span><span class="sxs-lookup"><span data-stu-id="c9355-135">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="c9355-136">**Birgðabiðminni** - Þessi eiginleiki er notaður til að tilgreina biðminnisnúmer fyrir birgðir.</span><span class="sxs-lookup"><span data-stu-id="c9355-136">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="c9355-137">Birgðunum er viðhaldið í rauntíma og þegar margir viðskiptavinir leggja inn pantanir getur verið erfitt að viðhalda nákvæmri birgðatalningu.</span><span class="sxs-lookup"><span data-stu-id="c9355-137">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="c9355-138">Þegar úttekt á birgðum er framkvæmd og birgðahaldið er minna en biðmagnið er varan meðhöndluð sem ekki til á lager.</span><span class="sxs-lookup"><span data-stu-id="c9355-138">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="c9355-139">Þess vegna, þegar sala á sér stað hratt í gegnum nokkrar rásir og birgðir eru ekki samstilltar að fullu, er minni hætta á að hlutur sem er ekki á lager verði seldur.</span><span class="sxs-lookup"><span data-stu-id="c9355-139">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="c9355-140">**Til baka í verslun** - Þessi eiginleiki er notaður til að tilgreina leiðina fyrir tengilinn **Til baka í verslun**.</span><span class="sxs-lookup"><span data-stu-id="c9355-140">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="c9355-141">Hægt er að stilla þessa leið á vettvangsstigi.</span><span class="sxs-lookup"><span data-stu-id="c9355-141">This route can be configured at the site level.</span></span> <span data-ttu-id="c9355-142">Þessar stillingar gera smásölum færa viðskiptavininn til baka á heimasíðuna eða aðra síðu á vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="c9355-142">This configuration lets retailers take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="c9355-143">Samskipti við Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="c9355-143">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="c9355-144">Körfueiningin sækir upplýsingar um afurðir með API kvörðunareiningu fyrir Commerce.</span><span class="sxs-lookup"><span data-stu-id="c9355-144">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="c9355-145">Auðkenni körfunnar frá vafrakökunni er notað til að sækja allar vöruupplýsingar frá Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="c9355-145">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="c9355-146">Bæta körfueiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="c9355-146">Add a cart module to a page</span></span>

<span data-ttu-id="c9355-147">Fylgdu þessum skrefum til að bæta körfueiningu við nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="c9355-147">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="c9355-148">Búðu til brot sem er nefnt **Körfubrot** og bættu körfueiningunni við það.</span><span class="sxs-lookup"><span data-stu-id="c9355-148">Create a fragment that is named **Cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="c9355-149">Bæta fyrirsögn við körfueininguna.</span><span class="sxs-lookup"><span data-stu-id="c9355-149">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="c9355-150">Bættu verslunarvalseiningu við körfueininguna.</span><span class="sxs-lookup"><span data-stu-id="c9355-150">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="c9355-151">Vistaðu brotið, ljúktu við að breyta því og birtu það.</span><span class="sxs-lookup"><span data-stu-id="c9355-151">Save the fragment, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="c9355-152">Búðu til sniðmát sem heitir **Körfusniðmát** og bættu körfubrotinu sem þú bjóst til við það.</span><span class="sxs-lookup"><span data-stu-id="c9355-152">Create a template that is named **Cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="c9355-153">Vistaðu sniðmátið, ljúktu við að breyta því og birtu það.</span><span class="sxs-lookup"><span data-stu-id="c9355-153">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="c9355-154">Búðu til síðu sem notar nýja sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="c9355-154">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="c9355-155">Vistaðu og forskoðaðu síðuna.</span><span class="sxs-lookup"><span data-stu-id="c9355-155">Save and preview the page.</span></span>
1. <span data-ttu-id="c9355-156">Ljúktu við að breyta síðunni, vistaðu hana og birtu.</span><span class="sxs-lookup"><span data-stu-id="c9355-156">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c9355-157">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c9355-157">Additional resources</span></span>

[<span data-ttu-id="c9355-158">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="c9355-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c9355-159">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="c9355-159">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="c9355-160">Kaupkassaeining</span><span class="sxs-lookup"><span data-stu-id="c9355-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c9355-161">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="c9355-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c9355-162">Pöntunarstaðfestingareining</span><span class="sxs-lookup"><span data-stu-id="c9355-162">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="c9355-163">Fyrirsagnareining</span><span class="sxs-lookup"><span data-stu-id="c9355-163">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="c9355-164">Neðanmálseining</span><span class="sxs-lookup"><span data-stu-id="c9355-164">Footer module</span></span>](author-footer-module.md)
