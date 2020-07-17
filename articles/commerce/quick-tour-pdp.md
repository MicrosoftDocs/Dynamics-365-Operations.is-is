---
title: Yfirlýt upplýsingasíðu afurða
description: Þetta efni veitir yfirlit yfir afurðaupplýsingasíður (PDP) í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c53e74204fad2960dfba972a38c511df7d6672d8
ms.sourcegitcommit: ce397c2759f642c595e30fef58a770b50360b2bd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/01/2020
ms.locfileid: "3527540"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="da74d-103">Yfirlýt upplýsingasíðu afurða</span><span class="sxs-lookup"><span data-stu-id="da74d-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="da74d-104">Þetta efni veitir yfirlit yfir afurðaupplýsingasíður (PDP) í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="da74d-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="da74d-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="da74d-105">Overview</span></span>

<span data-ttu-id="da74d-106">PDP veitir nákvæmar upplýsingar um afurð og gerir viðskiptavinum kleift að velja afurðakosti eins og stærð, stíl og lit.</span><span class="sxs-lookup"><span data-stu-id="da74d-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="da74d-107">PDP ætti að sýna allar vöruupplýsingar sem viðskiptavinur þarfnast til að taka ákvörðun um kaup.</span><span class="sxs-lookup"><span data-stu-id="da74d-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="da74d-108">Eftirfarandi skýringarmynd sýnir dæmi um PDP.</span><span class="sxs-lookup"><span data-stu-id="da74d-108">The following illustration shows an example of a PDP.</span></span>

![Dæmi um upplýsingasíðu afurðar](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="da74d-110">Einingar síðuhauss og síðufótar</span><span class="sxs-lookup"><span data-stu-id="da74d-110">Header and footer modules</span></span>

<span data-ttu-id="da74d-111">Efst á PDP er haus sem sýnir alla vöruflokka og aðrar síður sem smásalinn vill að viðskiptavinir skoði.</span><span class="sxs-lookup"><span data-stu-id="da74d-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="da74d-112">Neðst á síðunni er síðufótur sem inniheldur fljótlega tengla á ýmis efni sem kaupendur gætu haft áhuga á.</span><span class="sxs-lookup"><span data-stu-id="da74d-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="da74d-113">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="da74d-113">Buy box module</span></span>

<span data-ttu-id="da74d-114">Mikilvægasta einingin á PDP er kaupboxeiningin, sem birtist sem fyrsta atriðið í aðalhluta síðunnar.</span><span class="sxs-lookup"><span data-stu-id="da74d-114">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="da74d-115">Eining innkaupakassa sýnir mikilvægar vöruupplýsingar, svo sem vöruheiti, vörulýsingu, vöruverð, afurðamyndir og vörueinkunn.</span><span class="sxs-lookup"><span data-stu-id="da74d-115">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="da74d-116">Kaupgluggaeiningin gerir viðskiptavininum kleift að velja vöruvalkosti (til dæmis stærð, stíl og lit) og bæta vörunni í körfuna.</span><span class="sxs-lookup"><span data-stu-id="da74d-116">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="da74d-117">Hún gerir viðskiptavininum einnig kleift að kaupa vöruna á netinu og sækja hana í verslun.</span><span class="sxs-lookup"><span data-stu-id="da74d-117">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="da74d-118">Kaupið á netinu og sótt í verslunareininguna notar samþættingu við forritunarviðmót Bing Maps forrita (API) til að finna nálægar verslanir eða verslanir á öðrum stað sem viðskiptavinurinn tilgreinir.</span><span class="sxs-lookup"><span data-stu-id="da74d-118">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="da74d-119">Kaupgluggaeining þarf afurðakenni.</span><span class="sxs-lookup"><span data-stu-id="da74d-119">A buy box module requires a product ID.</span></span> <span data-ttu-id="da74d-120">Þetta auðkenni er dregið af samhengi síðunnar.</span><span class="sxs-lookup"><span data-stu-id="da74d-120">This ID is derived from the page context.</span></span> <span data-ttu-id="da74d-121">Ef kaupgluggaeiningu er bætt við síðu þar sem samhengi síðunnar er ekki með afurðakenni, mun hún ekki birta upplýsingarnar rétt.</span><span class="sxs-lookup"><span data-stu-id="da74d-121">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="da74d-122">Afurðaskilgreiningaeining</span><span class="sxs-lookup"><span data-stu-id="da74d-122">Product specifications module</span></span>

<span data-ttu-id="da74d-123">Hægt er að nota afurðaskilgreiningareininguna til að sýna frekari upplýsingar um vöruna.</span><span class="sxs-lookup"><span data-stu-id="da74d-123">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="da74d-124">Þessar upplýsingar eru fengnar frá afurðareigindum í Commerce.</span><span class="sxs-lookup"><span data-stu-id="da74d-124">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="da74d-125">Vörulýsingareiningin sýnir alla eiginleika þar sem eiginleikinn **sýnilegt** er stilltur á **satt**.</span><span class="sxs-lookup"><span data-stu-id="da74d-125">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="da74d-126">Það þarf afurðakenni til að sækja afurðareigindir.</span><span class="sxs-lookup"><span data-stu-id="da74d-126">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="da74d-127">Tillagnaeining</span><span class="sxs-lookup"><span data-stu-id="da74d-127">Recommendations module</span></span>

<span data-ttu-id="da74d-128">Tillagnaeiningin er mikilvæg einingin á PDP.</span><span class="sxs-lookup"><span data-stu-id="da74d-128">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="da74d-129">Meðan viðskiptavinir leita að vörum ætti að kynna þeim fleiri vöruvalkosti svo þeir geti fundið réttu vöruna og gert kaup.</span><span class="sxs-lookup"><span data-stu-id="da74d-129">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="da74d-130">Tilmæli hjálpa viðskiptavinum að uppgötva tengt efni og halda áfram að versla.</span><span class="sxs-lookup"><span data-stu-id="da74d-130">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="da74d-131">Mismunandi gerðir tillagna eru tiltækar:</span><span class="sxs-lookup"><span data-stu-id="da74d-131">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="da74d-132">Listinn **Fólki líkar einnig** er byggður á vélanámi.</span><span class="sxs-lookup"><span data-stu-id="da74d-132">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="da74d-133">Hann notar viðskiptasögu annarra viðskiptavina til að veita ráðleggingar.</span><span class="sxs-lookup"><span data-stu-id="da74d-133">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="da74d-134">Þessi listi er búinn til með ráðleggingaþjónustunni og líkist listunum „Viðskiptavinir sem keyptu þetta keyptu líka ...“.</span><span class="sxs-lookup"><span data-stu-id="da74d-134">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="da74d-135">Afurðakennis er krafist til að búa til þennan lista.</span><span class="sxs-lookup"><span data-stu-id="da74d-135">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="da74d-136">Listann **Tengt** er hægt að stilla lista fyrir vöru í Commerce.</span><span class="sxs-lookup"><span data-stu-id="da74d-136">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="da74d-137">Til dæmis, fyrir brúna handtösku úr leðri, er hægt að stilla fleiri handtöskur úr leðri eða hannaðar til að nota í ferðalögum fyrir viðkomandi lista.</span><span class="sxs-lookup"><span data-stu-id="da74d-137">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="da74d-138">Aðrar gerðir tengdra lista, svo sem **Aukahlutir** og **Meira eins og þetta** er einnig er hægt að stilla í Commerce.</span><span class="sxs-lookup"><span data-stu-id="da74d-138">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="da74d-139">Afurðakennis er krafist til að búa til þennan lista.</span><span class="sxs-lookup"><span data-stu-id="da74d-139">A product ID is required to generate this list.</span></span> <span data-ttu-id="da74d-140">Þess vegna, ef því er bætt við heimasíðuna, þar sem samhengi síðunnar inniheldur ekki afurðakenni, verður listinn tómur.</span><span class="sxs-lookup"><span data-stu-id="da74d-140">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="da74d-141">Algrímmyndaðir myndaðir tillagnalistar, eins og **Vinsælt**, **Mest selt** og **Nýtt** má nota á PDP.</span><span class="sxs-lookup"><span data-stu-id="da74d-141">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="da74d-142">Þó að þessir listar séu kannski ekki í beinum tengslum við vöruna á PDP, eru þeir önnur leið til að hjálpa viðskiptavinum að finna vörur sem gætu haft áhuga á þeim.</span><span class="sxs-lookup"><span data-stu-id="da74d-142">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="da74d-143">Þessar gerðir lista þurfa ekki afurðakenni.</span><span class="sxs-lookup"><span data-stu-id="da74d-143">These types of lists don't require a product ID.</span></span> <span data-ttu-id="da74d-144">Þetta eru almennir listar sem eru búnir til út frá innkaupamynstrum á vefnum.</span><span class="sxs-lookup"><span data-stu-id="da74d-144">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="da74d-145">Ritstjórnarlistar eru handvirkir listar.</span><span class="sxs-lookup"><span data-stu-id="da74d-145">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="da74d-146">Til dæmis gæti smásali ákveðið að setja handvirkt saman lista yfir vörur sem hann vill sýna.</span><span class="sxs-lookup"><span data-stu-id="da74d-146">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="da74d-147">Einkunna- og umsagnaeiningar</span><span class="sxs-lookup"><span data-stu-id="da74d-147">Ratings and reviews modules</span></span>

<span data-ttu-id="da74d-148">Hægt er að nota þrjár einingar til að sýna og bæta við umsögnum:</span><span class="sxs-lookup"><span data-stu-id="da74d-148">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="da74d-149">**Umsagnir** - Þessi eining sýnir einkunnir og umsagnir sýnir einkunnir og umsagnir sem aðrir viðskiptavinir hafa gefið.</span><span class="sxs-lookup"><span data-stu-id="da74d-149">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="da74d-150">Viðskiptavinir geta flokkað og síað umsagnir.</span><span class="sxs-lookup"><span data-stu-id="da74d-150">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="da74d-151">Þessi eining gerir viðskiptavinum kleift að líka eða líkar ekki við umsagnir og tilkynna um vandamál.</span><span class="sxs-lookup"><span data-stu-id="da74d-151">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="da74d-152">**Skrifa umsögn** - Í þessari einingu geta viðskiptavinir skrifað eigin umsagnir um vöru.</span><span class="sxs-lookup"><span data-stu-id="da74d-152">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="da74d-153">**Einkunnarit** - Þessi eining er með súlurit sem sýnir mat á þróun vöru.</span><span class="sxs-lookup"><span data-stu-id="da74d-153">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="da74d-154">Frekari upplýsingar eru í [Yfirlit yfir einkunnir og umsagnir](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="da74d-154">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="da74d-155">Markaðssetningareiningar</span><span class="sxs-lookup"><span data-stu-id="da74d-155">Marketing modules</span></span>

<span data-ttu-id="da74d-156">Ef markaðsefni er einstakt fyrir ákveðna afurð er hægt að bæta hvaða markaðsseiningu sem er við PDP.</span><span class="sxs-lookup"><span data-stu-id="da74d-156">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="da74d-157">Þú getur bætt markaðsseiningum við PDP með því að „auðga“ síðuna.</span><span class="sxs-lookup"><span data-stu-id="da74d-157">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="da74d-158">Sjá frekari upplýsingar [Auðga afurðasíðu](enrich-product-page.md).</span><span class="sxs-lookup"><span data-stu-id="da74d-158">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da74d-159">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="da74d-159">Additional resources</span></span>

[<span data-ttu-id="da74d-160">Yfirlit heimasíðu</span><span class="sxs-lookup"><span data-stu-id="da74d-160">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="da74d-161">Yfirlit yfir síður körfu og greiðsluferlis</span><span class="sxs-lookup"><span data-stu-id="da74d-161">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="da74d-162">Yfirlit yfir síður fyrir stjórnun reikninga</span><span class="sxs-lookup"><span data-stu-id="da74d-162">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="da74d-163">Bæta upplýsingasíðu afurða</span><span class="sxs-lookup"><span data-stu-id="da74d-163">Enrich a product details page</span></span>](enrich-product-page.md)
