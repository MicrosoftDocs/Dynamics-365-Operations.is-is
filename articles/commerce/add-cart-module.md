---
title: Körfueining
description: Þetta efni fjallar um körfueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.openlocfilehash: 598b35b1bd365e761d8d4c5ef214935e60b971f4
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154018"
---
# <a name="cart-module"></a><span data-ttu-id="844c0-103">Körfueining</span><span class="sxs-lookup"><span data-stu-id="844c0-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="844c0-104">Þetta efni fjallar um körfueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="844c0-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="844c0-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="844c0-105">Overview</span></span>

<span data-ttu-id="844c0-106">Körfueining sýnir hluti sem hafa verið settir í körfuna áður en viðskiptavinurinn heldur áfram að kassa.</span><span class="sxs-lookup"><span data-stu-id="844c0-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="844c0-107">Einingin sýnir einnig samantekt á pöntun og gerir viðskiptavininum kleift að beita eða fjarlægja kynningarkóða.</span><span class="sxs-lookup"><span data-stu-id="844c0-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="844c0-108">Körfueiningin styður innskráð greiðsluferli og greiðslu sem gestur.</span><span class="sxs-lookup"><span data-stu-id="844c0-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="844c0-109">Hún styður einnig tengilinn **Til baka í verslun**.</span><span class="sxs-lookup"><span data-stu-id="844c0-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="844c0-110">Þú getur stillt leiðina fyrir þennan hlekk á **Svæðisstillingar \> Viðbætur \> Leiðir**.</span><span class="sxs-lookup"><span data-stu-id="844c0-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="844c0-111">Í körfueiningunni eru gögn byggð á körfuauðkenninu, sem er vafrakaka sem hægt er að nálgast á vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="844c0-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="844c0-112">Eiginleikar og hólf körfueininga</span><span class="sxs-lookup"><span data-stu-id="844c0-112">Cart module properties and slots</span></span>

<span data-ttu-id="844c0-113">Körfueiningin er með eiginleikann **Fyrirsögn** sem hægt er að stilla á gildi eins og **Innkaupapoki** og **Vörur í körfunni þinni**.</span><span class="sxs-lookup"><span data-stu-id="844c0-113">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="844c0-114">Einingar sem hægt er að nota í körfueiningu</span><span class="sxs-lookup"><span data-stu-id="844c0-114">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="844c0-115">**Textabálkur** – Þessi eining styður sérsniðin skilaboð í körfueiningunni.</span><span class="sxs-lookup"><span data-stu-id="844c0-115">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="844c0-116">Skilaboðin eru keyrð af efnisstjórnunarkerfinu (CMS).</span><span class="sxs-lookup"><span data-stu-id="844c0-116">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="844c0-117">Hægt er að bæta við hvaða skilaboðum sem er, eins og „Vegna vandamála með pöntunina, hafið samband við 1-800-Fabrikam.“</span><span class="sxs-lookup"><span data-stu-id="844c0-117">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="844c0-118">**Verslunarval** – Þessi eining sýnir lista yfir nærliggjandi verslanir þar sem hægt er að sækja vöru.</span><span class="sxs-lookup"><span data-stu-id="844c0-118">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="844c0-119">Það gerir notendum kleift að slá inn staðsetningu til að finna verslanir í nágrenninu.</span><span class="sxs-lookup"><span data-stu-id="844c0-119">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="844c0-120">Fyrir frekari upplýsingar um þessa einingu, sjá [Verslunarvalseiningu](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="844c0-120">For more information on this module, see [Store Selector module](store-selector.md).</span></span>

## <a name="cart-module-settings"></a><span data-ttu-id="844c0-121">Stillingar körfueiningar</span><span class="sxs-lookup"><span data-stu-id="844c0-121">Cart module settings</span></span>

<span data-ttu-id="844c0-122">Körfueiningar hafa eftirfarandi stillingar sem hægt er að stilla á **Svæðisstillingar \> Viðbætur**:</span><span class="sxs-lookup"><span data-stu-id="844c0-122">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="844c0-123">**Hámarksmagn** - Þessi eiginleiki er notaður til að tilgreina hámarksfjölda hvers hlutar sem hægt er að bæta við körfuna.</span><span class="sxs-lookup"><span data-stu-id="844c0-123">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="844c0-124">Til dæmis gæti smásali ákveðið að aðeins megi selja 10 stykki af hverri afurð í sömu færslunni.</span><span class="sxs-lookup"><span data-stu-id="844c0-124">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="844c0-125">**Birgðakönnun** - Þegar gildi er stillt á **Satt** er vara aðeins sett í körfuna eftir að kaupkassaeiningin tryggir að hún sé til á lager.</span><span class="sxs-lookup"><span data-stu-id="844c0-125">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="844c0-126">Þessi úttekt á birgðum er gerð fyrir atburðarás þar sem hluturinn verður sendur og fyrir atburðarás þar sem hann verður sóttur í verslunina.</span><span class="sxs-lookup"><span data-stu-id="844c0-126">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="844c0-127">Ef gildi er stillt á **Rangt** er engin úttekt á birgðum gerð áður en hlutur er settur í körfuna og pöntunin er gerð.</span><span class="sxs-lookup"><span data-stu-id="844c0-127">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="844c0-128">**Birgðabiðminni** - Þessi eiginleiki er notaður til að tilgreina biðminnisnúmer fyrir birgðir.</span><span class="sxs-lookup"><span data-stu-id="844c0-128">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="844c0-129">Birgðunum er viðhaldið í rauntíma og þegar margir viðskiptavinir leggja inn pantanir getur verið erfitt að viðhalda nákvæmri birgðatalningu.</span><span class="sxs-lookup"><span data-stu-id="844c0-129">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="844c0-130">Þegar úttekt á birgðum er framkvæmd og birgðahaldið er minna en biðmagnið er varan meðhöndluð sem ekki til á lager.</span><span class="sxs-lookup"><span data-stu-id="844c0-130">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="844c0-131">Þess vegna, þegar sala á sér stað hratt í gegnum nokkrar rásir og birgðir eru ekki samstilltar að fullu, er minni hætta á að hlutur sem er ekki á lager verði seldur.</span><span class="sxs-lookup"><span data-stu-id="844c0-131">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="844c0-132">**Til baka í verslun** - Þessi eiginleiki er notaður til að tilgreina leiðina fyrir tengilinn **Til baka í verslun**.</span><span class="sxs-lookup"><span data-stu-id="844c0-132">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="844c0-133">Hægt er að stilla leiðina á vettvangsstigi, sem gerir smásöluaðilum kleift að fara með viðskiptavininn aftur á heimasíðuna eða aðra síðu á síðunni.</span><span class="sxs-lookup"><span data-stu-id="844c0-133">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="844c0-134">Samskipti við Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="844c0-134">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="844c0-135">Körfueiningin sækir upplýsingar um afurðir með API kvörðunareiningu fyrir Commerce.</span><span class="sxs-lookup"><span data-stu-id="844c0-135">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="844c0-136">Auðkenni körfunnar frá vafrakökunni er notað til að sækja allar vöruupplýsingar frá Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="844c0-136">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="844c0-137">Bæta körfueiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="844c0-137">Add a cart module to a page</span></span>

<span data-ttu-id="844c0-138">Fylgdu þessum skrefum til að bæta körfueiningu við nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="844c0-138">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="844c0-139">Búðu til brot sem er nefnt **Körfubrot** og bættu körfueiningunni við nýja brotið.</span><span class="sxs-lookup"><span data-stu-id="844c0-139">Create a fragment named **Cart fragment**, and add a cart module to the new fragment.</span></span>
1. <span data-ttu-id="844c0-140">Bæta fyrirsögn við körfueininguna.</span><span class="sxs-lookup"><span data-stu-id="844c0-140">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="844c0-141">Bættu verslunarvalseiningu við körfueininguna.</span><span class="sxs-lookup"><span data-stu-id="844c0-141">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="844c0-142">Vistaðu brotið, ljúktu við að breyta því og birtu síðan brotið.</span><span class="sxs-lookup"><span data-stu-id="844c0-142">Save the fragment, finish editing, and then publish the fragment.</span></span>
1. <span data-ttu-id="844c0-143">Búðu til sniðmát sem heitir **Körfusniðmát** og bættu við körfubrotinu sem þú bjóst til.</span><span class="sxs-lookup"><span data-stu-id="844c0-143">Create a template named **Cart template**, and add the cart fragment that you just created.</span></span>
1. <span data-ttu-id="844c0-144">Vistaðu sniðmátið, ljúktu við að breyta því og birtu síðan sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="844c0-144">Save the template, finish editing, and then publish the template.</span></span>
1. <span data-ttu-id="844c0-145">Búðu til síðu sem notar nýja sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="844c0-145">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="844c0-146">Vistaðu og forskoðaðu síðuna.</span><span class="sxs-lookup"><span data-stu-id="844c0-146">Save and preview the page.</span></span>
1. <span data-ttu-id="844c0-147">Ljúktu við að breyta síðunni og birtu hana síðan.</span><span class="sxs-lookup"><span data-stu-id="844c0-147">Finish editing the page, and then publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="844c0-148">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="844c0-148">Additional resources</span></span>

[<span data-ttu-id="844c0-149">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="844c0-149">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="844c0-150">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="844c0-150">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="844c0-151">Verslunarvalseining</span><span class="sxs-lookup"><span data-stu-id="844c0-151">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="844c0-152">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="844c0-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="844c0-153">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="844c0-153">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="844c0-154">Eining pöntunarstaðfestingar</span><span class="sxs-lookup"><span data-stu-id="844c0-154">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="844c0-155">Fyrirsagnareining</span><span class="sxs-lookup"><span data-stu-id="844c0-155">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="844c0-156">Neðanmálseining</span><span class="sxs-lookup"><span data-stu-id="844c0-156">Footer module</span></span>](author-footer-module.md)
