---
title: Vista valeiningu
description: Þetta efni fjallar um verslunarvalseininguna og lýsir því hvernig á að bæta henni við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8efc2345ded52bfaee2d400815795906f326f4fd
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/21/2020
ms.locfileid: "3157341"
---
# <a name="store-selector-module"></a><span data-ttu-id="5926e-103">Vista valeiningu</span><span class="sxs-lookup"><span data-stu-id="5926e-103">Store selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5926e-104">Þetta efni fjallar um verslunarvalseininguna og lýsir því hvernig á að bæta henni við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5926e-104">This topic covers the store selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5926e-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="5926e-105">Overview</span></span>

<span data-ttu-id="5926e-106">Verslunarvalseining er notuð fyrir „kaup á netinu, sækja í verslun“ (BOPIS) viðskiptavinar atburðarás.</span><span class="sxs-lookup"><span data-stu-id="5926e-106">A store selector module is used for the "buy online, pick up in store"" (BOPIS) customer scenario.</span></span> <span data-ttu-id="5926e-107">Það birtir lista yfir verslanir þar sem vara er fáanleg, svo og verslunartími og vörubirgðir fyrir hverja verslun.</span><span class="sxs-lookup"><span data-stu-id="5926e-107">It displays a list of stores where a product is available for pickup, as well as store hours and product inventory for each store.</span></span>

<span data-ttu-id="5926e-108">Verslunarvalseiningin krefst samhengis vöru og leitarstað til að finna verslanir.</span><span class="sxs-lookup"><span data-stu-id="5926e-108">The store selector module requires the context of a product and a search location to find stores.</span></span> <span data-ttu-id="5926e-109">Ef ekki er leitað, skiptir það staðinn að vafra staðsetningu viðskiptavinarins að því tilskildu að viðskiptavinurinn veiti samþykki.</span><span class="sxs-lookup"><span data-stu-id="5926e-109">In the absence of a search location, it defaults to the customer's browser location, provided that the customer gives consent.</span></span> <span data-ttu-id="5926e-110">Einingin er með inntakskassa sem gerir viðskiptavininum kleift að slá inn staðsetningu (póstnúmer, eða borg og ríki) til að finna verslanir sem eru í nágrenninu.</span><span class="sxs-lookup"><span data-stu-id="5926e-110">The module has an input box which allows the customer to enter a location (zipcode, or city and state) to find stores that are nearby.</span></span>

<span data-ttu-id="5926e-111">Verslunarvalseiningin er samþætt við Bing Maps Geocoding forritunarviðmót (API) landskóðunar til að umbreyta staðsetningunni í breiddar- og lengdargráðu.</span><span class="sxs-lookup"><span data-stu-id="5926e-111">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="5926e-112">Bing Maps API lykils er krafist og bæta verður honum við Commerce sameiginlegar færibreytusíðuna í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5926e-112">A Bing Maps API key is required and must be added to the Commerce shared parameters page in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5926e-113">Hægt er að bæta verslunareiningareiningunni við innkaupakassaeiningu á upplýsingasíðu vöru (PDP) til að birta verslanir þar sem vara er fáanleg.</span><span class="sxs-lookup"><span data-stu-id="5926e-113">The store selector module can be added to a buy box module on the product details page (PDP) to display stores where a product is available for pickup.</span></span> <span data-ttu-id="5926e-114">Það er einnig hægt að bæta við körfu mát.</span><span class="sxs-lookup"><span data-stu-id="5926e-114">It can also be added to a cart module.</span></span> <span data-ttu-id="5926e-115">Þegar versluninni er bætt við körfueininguna birtir valkosti verslunarinnar söfnunarkosti fyrir hverja vöruhluta í körfunni.</span><span class="sxs-lookup"><span data-stu-id="5926e-115">When added to a cart module, the store selector module displays pickup options for each cart line item.</span></span> <span data-ttu-id="5926e-116">Að auki, með sérsniðnum kóðun er hægt að bæta þessari einingu við aðrar síður eða einingar í gegnum viðbætur og sérstillingar.</span><span class="sxs-lookup"><span data-stu-id="5926e-116">In addition, with custom coding this module can be added to other pages or modules via extensions and customizations.</span></span>

<span data-ttu-id="5926e-117">Til að BOPIS atburðarásinn virki, ættu vörur að vera stilltar með afhendingarstillingu „viðskiptavinur sækir“.</span><span class="sxs-lookup"><span data-stu-id="5926e-117">For the BOPIS scenario to work, products should be configured with the "customer pickup" delivery mode.</span></span> <span data-ttu-id="5926e-118">Annars verður einingin ekki sýnd á viðkomandi síðum.</span><span class="sxs-lookup"><span data-stu-id="5926e-118">Otherwise, the module will not be shown on the respective pages.</span></span> <span data-ttu-id="5926e-119">Nánari upplýsingar um hvernig á að stilla afhendingarstillingu, sjá [Settu upp afhendingaraðferðir](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="5926e-119">For details on how to configure the delivery mode, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="5926e-120">Eftirfarandi mynd sýnir dæmi um verslunarvalseiningu sem er notuð á PDP.</span><span class="sxs-lookup"><span data-stu-id="5926e-120">The following image shows an example of a store selector module used on a PDP.</span></span>

![Dæmi um verslunarvalseiningu](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a><span data-ttu-id="5926e-122">Notkun verslunarvalseiningar í e-Commerce</span><span class="sxs-lookup"><span data-stu-id="5926e-122">Store selector module usage in e-Commerce</span></span>

- <span data-ttu-id="5926e-123">Hægt er að nota verslunareiningareiningu á upplýsingasíðu vöru (PDP) til að finna nálægar verslanir þar sem vara er fáanleg.</span><span class="sxs-lookup"><span data-stu-id="5926e-123">A store selector module can be used on a product details page (PDP) to find nearby stores where a product is available for pickup.</span></span>
- <span data-ttu-id="5926e-124">Hægt er að nota verslunarvalseiningu á körfusíðu til að finna nálægar verslanir þar sem vara í körfunni er fáanleg.</span><span class="sxs-lookup"><span data-stu-id="5926e-124">A store selector module can be used on a cart page to find nearby stores where a product in the cart is available for pickup.</span></span>

## <a name="store-selector-module-properties"></a><span data-ttu-id="5926e-125">Eiginleikar verslunarvalseiningar</span><span class="sxs-lookup"><span data-stu-id="5926e-125">Store selector module properties</span></span>

| <span data-ttu-id="5926e-126">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="5926e-126">Property name</span></span>             | <span data-ttu-id="5926e-127">Virði</span><span class="sxs-lookup"><span data-stu-id="5926e-127">Value</span></span>                 | <span data-ttu-id="5926e-128">lýsing</span><span class="sxs-lookup"><span data-stu-id="5926e-128">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="5926e-129">Leitarradíus</span><span class="sxs-lookup"><span data-stu-id="5926e-129">Search radius</span></span> | <span data-ttu-id="5926e-130">Númer</span><span class="sxs-lookup"><span data-stu-id="5926e-130">Number</span></span> | <span data-ttu-id="5926e-131">Skilgreinir leitarradíus fyrir verslanir, í mílum.</span><span class="sxs-lookup"><span data-stu-id="5926e-131">Defines the search radius for stores, in miles.</span></span> <span data-ttu-id="5926e-132">Ef ekkert gildi er tilgreint er sjálfgefinn leitarradíus upp á 50 mílur notaður.</span><span class="sxs-lookup"><span data-stu-id="5926e-132">If no value is specified, the default search radius of 50 miles is used.</span></span>|
|<span data-ttu-id="5926e-133">Þjónustuskilmálar</span><span class="sxs-lookup"><span data-stu-id="5926e-133">Terms of Service</span></span> | <span data-ttu-id="5926e-134">URL</span><span class="sxs-lookup"><span data-stu-id="5926e-134">URL</span></span>    |  <span data-ttu-id="5926e-135">Skilmálar þjónustuslóðarinnar sem er krafist fyrir þjónustuna Bing Maps.</span><span class="sxs-lookup"><span data-stu-id="5926e-135">The terms of service URL that is required for the Bing Maps service.</span></span> |

## <a name="add-a-store-selector-module-to-a-page"></a><span data-ttu-id="5926e-136">Bæta við verslunarvalseiningu á síðu</span><span class="sxs-lookup"><span data-stu-id="5926e-136">Add a store selector module to a page</span></span>

<span data-ttu-id="5926e-137">Verslunarvalseining þarf samhengi vöru, þannig að það er aðeins hægt að nota það innan kaupabox og körfueiningar.</span><span class="sxs-lookup"><span data-stu-id="5926e-137">A store selector module needs the context of a product, so it can only be used within buy box and cart modules.</span></span> <span data-ttu-id="5926e-138">Verslunarvalseiningar virka ekki utan þessara eininga.</span><span class="sxs-lookup"><span data-stu-id="5926e-138">Store selector modules do not function outside these modules.</span></span>

- <span data-ttu-id="5926e-139">Nánari upplýsingar um hvernig á að bæta verslunareiningareiningunni við innkaupakassaeiningar, sjá [Kaupkassaeiningu](add-buy-box.md).</span><span class="sxs-lookup"><span data-stu-id="5926e-139">For information on how to add a store selector module to a buy box module, see [Buy box module](add-buy-box.md).</span></span> 
- <span data-ttu-id="5926e-140">Nánari upplýsingar um hvernig á að bæta verslunareiningareiningunni við körfueiningar, sjá [Körfueiningu](add-cart-module.md).</span><span class="sxs-lookup"><span data-stu-id="5926e-140">For information on how to add a store selector module to a cart module, see [Cart module](add-cart-module.md)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5926e-141">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="5926e-141">Additional resources</span></span>

[<span data-ttu-id="5926e-142">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="5926e-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5926e-143">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="5926e-143">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="5926e-144">Körfueining</span><span class="sxs-lookup"><span data-stu-id="5926e-144">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="5926e-145">Stutt kynning um PDP</span><span class="sxs-lookup"><span data-stu-id="5926e-145">Quick tour of PDP</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="5926e-146">Stutt kynning á Körfu og greiðsluferli</span><span class="sxs-lookup"><span data-stu-id="5926e-146">Quick tour of Cart and checkout</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="5926e-147">Setja upp afhendingarmáta</span><span class="sxs-lookup"><span data-stu-id="5926e-147">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
