---
title: Yfirlit yfir upplýsingasíður afurða
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
ms.openlocfilehash: dbf8f4c1ea479a508f4a0294020b7201b32fe228
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025926"
---
# <a name="overview-of-product-details-pages"></a><span data-ttu-id="12ca7-103">Yfirlit yfir upplýsingasíður afurða</span><span class="sxs-lookup"><span data-stu-id="12ca7-103">Overview of product details pages</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="12ca7-104">Þetta efni veitir yfirlit yfir afurðaupplýsingasíður (PDP) í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="12ca7-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="12ca7-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="12ca7-105">Overview</span></span>

<span data-ttu-id="12ca7-106">PDP veitir nákvæmar upplýsingar um afurð og gerir viðskiptavinum kleift að velja afurðakosti eins og stærð, stíl og lit.</span><span class="sxs-lookup"><span data-stu-id="12ca7-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="12ca7-107">PDP ætti að sýna allar vöruupplýsingar sem viðskiptavinur þarfnast til að taka ákvörðun um kaup.</span><span class="sxs-lookup"><span data-stu-id="12ca7-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="12ca7-108">Eftirfarandi skýringarmynd sýnir dæmi um PDP.</span><span class="sxs-lookup"><span data-stu-id="12ca7-108">The following illustration shows an example of a PDP.</span></span>

![Dæmi um upplýsingasíðu afurðar](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="12ca7-110">Einingar síðuhauss og síðufótar</span><span class="sxs-lookup"><span data-stu-id="12ca7-110">Header and footer modules</span></span>

<span data-ttu-id="12ca7-111">Efst á PDP er haus sem sýnir alla vöruflokka og aðrar síður sem smásalinn vill að viðskiptavinir skoði.</span><span class="sxs-lookup"><span data-stu-id="12ca7-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="12ca7-112">Neðst á síðunni er síðufótur sem inniheldur fljótlega tengla á ýmis efni sem kaupendur gætu haft áhuga á.</span><span class="sxs-lookup"><span data-stu-id="12ca7-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="12ca7-113">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="12ca7-113">Buy box module</span></span>

<span data-ttu-id="12ca7-114">Mikilvægasta einingin á PDP er kaupboxeiningin, sem birtist sem fyrsta atriðið í aðalhluta síðunnar.</span><span class="sxs-lookup"><span data-stu-id="12ca7-114">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="12ca7-115">Eining innkaupakassa sýnir mikilvægar vöruupplýsingar, svo sem vöruheiti, vörulýsingu, vöruverð, afurðamyndir og vörueinkunn.</span><span class="sxs-lookup"><span data-stu-id="12ca7-115">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="12ca7-116">Kaupgluggaeiningin gerir viðskiptavininum kleift að velja vöruvalkosti (til dæmis stærð, stíl og lit) og bæta vörunni í körfuna.</span><span class="sxs-lookup"><span data-stu-id="12ca7-116">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="12ca7-117">Hún gerir viðskiptavininum einnig kleift að kaupa vöruna á netinu og sækja hana í verslun.</span><span class="sxs-lookup"><span data-stu-id="12ca7-117">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="12ca7-118">Kaupið á netinu og sótt í verslunareininguna notar samþættingu við forritunarviðmót Bing Maps forrita (API) til að finna nálægar verslanir eða verslanir á öðrum stað sem viðskiptavinurinn tilgreinir.</span><span class="sxs-lookup"><span data-stu-id="12ca7-118">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="12ca7-119">Kaupgluggaeining þarf afurðakenni.</span><span class="sxs-lookup"><span data-stu-id="12ca7-119">A buy box module requires a product ID.</span></span> <span data-ttu-id="12ca7-120">Þetta auðkenni er dregið af samhengi síðunnar.</span><span class="sxs-lookup"><span data-stu-id="12ca7-120">This ID is derived from the page context.</span></span> <span data-ttu-id="12ca7-121">Ef kaupgluggaeiningu er bætt við síðu þar sem samhengi síðunnar er ekki með afurðakenni, mun hún ekki birta upplýsingarnar rétt.</span><span class="sxs-lookup"><span data-stu-id="12ca7-121">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="12ca7-122">Afurðaskilgreiningaeining</span><span class="sxs-lookup"><span data-stu-id="12ca7-122">Product specifications module</span></span>

<span data-ttu-id="12ca7-123">Hægt er að nota afurðaskilgreiningareininguna til að sýna frekari upplýsingar um vöruna.</span><span class="sxs-lookup"><span data-stu-id="12ca7-123">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="12ca7-124">Þessar upplýsingar eru fengnar frá afurðareigindum í Commerce.</span><span class="sxs-lookup"><span data-stu-id="12ca7-124">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="12ca7-125">Vörulýsingareiningin sýnir alla eiginleika þar sem eiginleikinn **sýnilegt** er stilltur á **satt**.</span><span class="sxs-lookup"><span data-stu-id="12ca7-125">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="12ca7-126">Það þarf afurðakenni til að sækja afurðareigindir.</span><span class="sxs-lookup"><span data-stu-id="12ca7-126">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="12ca7-127">Tillagnaeining</span><span class="sxs-lookup"><span data-stu-id="12ca7-127">Recommendations module</span></span>

<span data-ttu-id="12ca7-128">Tillagnaeiningin er mikilvæg einingin á PDP.</span><span class="sxs-lookup"><span data-stu-id="12ca7-128">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="12ca7-129">Meðan viðskiptavinir leita að vörum ætti að kynna þeim fleiri vöruvalkosti svo þeir geti fundið réttu vöruna og gert kaup.</span><span class="sxs-lookup"><span data-stu-id="12ca7-129">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="12ca7-130">Tilmæli hjálpa viðskiptavinum að uppgötva tengt efni og halda áfram að versla.</span><span class="sxs-lookup"><span data-stu-id="12ca7-130">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="12ca7-131">Mismunandi gerðir tillagna eru tiltækar:</span><span class="sxs-lookup"><span data-stu-id="12ca7-131">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="12ca7-132">Listinn **Fólki líkar einnig** er byggður á vélanámi.</span><span class="sxs-lookup"><span data-stu-id="12ca7-132">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="12ca7-133">Hann notar viðskiptasögu annarra viðskiptavina til að veita ráðleggingar.</span><span class="sxs-lookup"><span data-stu-id="12ca7-133">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="12ca7-134">Þessi listi er búinn til með ráðleggingaþjónustunni og líkist listunum „Viðskiptavinir sem keyptu þetta keyptu líka ...“.</span><span class="sxs-lookup"><span data-stu-id="12ca7-134">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="12ca7-135">Afurðakennis er krafist til að búa til þennan lista.</span><span class="sxs-lookup"><span data-stu-id="12ca7-135">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="12ca7-136">Listann **Tengt** er hægt að stilla lista fyrir vöru í Commerce.</span><span class="sxs-lookup"><span data-stu-id="12ca7-136">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="12ca7-137">Til dæmis, fyrir brúna handtösku úr leðri, er hægt að stilla fleiri handtöskur úr leðri eða hannaðar til að nota í ferðalögum fyrir viðkomandi lista.</span><span class="sxs-lookup"><span data-stu-id="12ca7-137">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="12ca7-138">Aðrar gerðir tengdra lista, svo sem **Aukahlutir** og **Meira eins og þetta** er einnig er hægt að stilla í Commerce.</span><span class="sxs-lookup"><span data-stu-id="12ca7-138">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="12ca7-139">Afurðakennis er krafist til að búa til þennan lista.</span><span class="sxs-lookup"><span data-stu-id="12ca7-139">A product ID is required to generate this list.</span></span> <span data-ttu-id="12ca7-140">Þess vegna, ef því er bætt við heimasíðuna, þar sem samhengi síðunnar inniheldur ekki afurðakenni, verður listinn tómur.</span><span class="sxs-lookup"><span data-stu-id="12ca7-140">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="12ca7-141">Algrímmyndaðir myndaðir tillagnalistar, eins og **Vinsælt**, **Mest selt** og **Nýtt** má nota á PDP.</span><span class="sxs-lookup"><span data-stu-id="12ca7-141">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="12ca7-142">Þó að þessir listar séu kannski ekki í beinum tengslum við vöruna á PDP, eru þeir önnur leið til að hjálpa viðskiptavinum að finna vörur sem gætu haft áhuga á þeim.</span><span class="sxs-lookup"><span data-stu-id="12ca7-142">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="12ca7-143">Þessar gerðir lista þurfa ekki afurðakenni.</span><span class="sxs-lookup"><span data-stu-id="12ca7-143">These types of lists don't require a product ID.</span></span> <span data-ttu-id="12ca7-144">Þetta eru almennir listar sem eru búnir til út frá innkaupamynstrum á vefnum.</span><span class="sxs-lookup"><span data-stu-id="12ca7-144">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="12ca7-145">Ritstjórnarlistar eru handvirkir listar.</span><span class="sxs-lookup"><span data-stu-id="12ca7-145">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="12ca7-146">Til dæmis gæti smásali ákveðið að setja handvirkt saman lista yfir vörur sem hann vill sýna.</span><span class="sxs-lookup"><span data-stu-id="12ca7-146">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="12ca7-147">Einkunna- og umsagnaeiningar</span><span class="sxs-lookup"><span data-stu-id="12ca7-147">Ratings and reviews modules</span></span>

<span data-ttu-id="12ca7-148">Hægt er að nota þrjár einingar til að sýna og bæta við umsögnum:</span><span class="sxs-lookup"><span data-stu-id="12ca7-148">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="12ca7-149">**Umsagnir** - Þessi eining sýnir einkunnir og umsagnir sýnir einkunnir og umsagnir sem aðrir viðskiptavinir hafa gefið.</span><span class="sxs-lookup"><span data-stu-id="12ca7-149">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="12ca7-150">Viðskiptavinir geta flokkað og síað umsagnir.</span><span class="sxs-lookup"><span data-stu-id="12ca7-150">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="12ca7-151">Þessi eining gerir viðskiptavinum kleift að líka eða líkar ekki við umsagnir og tilkynna um vandamál.</span><span class="sxs-lookup"><span data-stu-id="12ca7-151">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="12ca7-152">**Skrifa umsögn** - Í þessari einingu geta viðskiptavinir skrifað eigin umsagnir um vöru.</span><span class="sxs-lookup"><span data-stu-id="12ca7-152">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="12ca7-153">**Einkunnarit** - Þessi eining er með súlurit sem sýnir mat á þróun vöru.</span><span class="sxs-lookup"><span data-stu-id="12ca7-153">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="12ca7-154">Frekari upplýsingar eru í [Yfirlit yfir einkunnir og umsagnir](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="12ca7-154">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="12ca7-155">Markaðssetningareiningar</span><span class="sxs-lookup"><span data-stu-id="12ca7-155">Marketing modules</span></span>

<span data-ttu-id="12ca7-156">Ef markaðsefni er einstakt fyrir ákveðna afurð er hægt að bæta hvaða markaðsseiningu sem er við PDP.</span><span class="sxs-lookup"><span data-stu-id="12ca7-156">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="12ca7-157">Þú getur bætt markaðsseiningum við PDP með því að „auðga“ síðuna.</span><span class="sxs-lookup"><span data-stu-id="12ca7-157">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="12ca7-158">Sjá frekari upplýsingar [Auðga afurðasíðu](enrich-product-page.md).</span><span class="sxs-lookup"><span data-stu-id="12ca7-158">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12ca7-159">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="12ca7-159">Additional resources</span></span>

[<span data-ttu-id="12ca7-160">Yfirlit heimasíðunnar</span><span class="sxs-lookup"><span data-stu-id="12ca7-160">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="12ca7-161">Yfirlit sjálfgefinnar lendingarsíðu flokks og leitarniðurstöðusíðu</span><span class="sxs-lookup"><span data-stu-id="12ca7-161">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="12ca7-162">Yfirlit yfir síður körfu og greiðsluferlis</span><span class="sxs-lookup"><span data-stu-id="12ca7-162">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="12ca7-163">Yfirlit yfir síður reikningastjórnunar</span><span class="sxs-lookup"><span data-stu-id="12ca7-163">Overview of account management pages</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="12ca7-164">Bæta upplýsingasíðu afurða</span><span class="sxs-lookup"><span data-stu-id="12ca7-164">Enrich a product details page</span></span>](enrich-product-page.md)
