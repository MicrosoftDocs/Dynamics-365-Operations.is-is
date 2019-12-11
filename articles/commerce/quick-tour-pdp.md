---
title: Yfirlit yfir upplýsingasíður afurða
description: Þetta efni veitir yfirlit yfir afurðaupplýsingasíður (PDP) í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697866"
---
# <a name="overview-of-product-details-pages"></a><span data-ttu-id="005c0-103">Yfirlit yfir upplýsingasíður afurða</span><span class="sxs-lookup"><span data-stu-id="005c0-103">Overview of product details pages</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="005c0-104">Þetta efni veitir yfirlit yfir afurðaupplýsingasíður (PDP) í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="005c0-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="005c0-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="005c0-105">Overview</span></span>

<span data-ttu-id="005c0-106">PDP veitir nákvæmar upplýsingar um afurð og gerir viðskiptavinum kleift að velja afurðakosti eins og stærð, stíl og lit.</span><span class="sxs-lookup"><span data-stu-id="005c0-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="005c0-107">PDP ætti að sýna allar vöruupplýsingar sem viðskiptavinur þarfnast til að taka ákvörðun um kaup.</span><span class="sxs-lookup"><span data-stu-id="005c0-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="005c0-108">Eftirfarandi skýringarmynd sýnir dæmi um PDP.</span><span class="sxs-lookup"><span data-stu-id="005c0-108">The following illustration shows an example of a PDP.</span></span>

![Dæmi um upplýsingasíðu afurðar](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="005c0-110">Einingar síðuhauss og síðufótar</span><span class="sxs-lookup"><span data-stu-id="005c0-110">Header and footer modules</span></span>

<span data-ttu-id="005c0-111">Efst á PDP er haus sem sýnir alla vöruflokka og aðrar síður sem smásalinn vill að viðskiptavinir skoði.</span><span class="sxs-lookup"><span data-stu-id="005c0-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="005c0-112">Neðst á síðunni er síðufótur sem inniheldur fljótlega tengla á ýmis efni sem kaupendur gætu haft áhuga á.</span><span class="sxs-lookup"><span data-stu-id="005c0-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="005c0-113">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="005c0-113">Buy box module</span></span>

<span data-ttu-id="005c0-114">Mikilvægasta einingin á PDP er einingin fyrir kaupglugga.</span><span class="sxs-lookup"><span data-stu-id="005c0-114">The most important module on a PDP is the buy box module.</span></span> <span data-ttu-id="005c0-115">Þess vegna er það fyrsta atriðið í aðalhlutanum á síðunni.</span><span class="sxs-lookup"><span data-stu-id="005c0-115">Therefore, it's the first item in the main section of the page.</span></span> <span data-ttu-id="005c0-116">Kaupgluggaeining er gámaeining og hýsir nokkrar einingar sem innihalda mikilvægustu upplýsingar um vöruna.</span><span class="sxs-lookup"><span data-stu-id="005c0-116">A buy box module is a container module and hosts several modules that contain the most important information about the product.</span></span> <span data-ttu-id="005c0-117">Þessar upplýsingar innihalda afurðaheiti, afurðamyndir, lýsingu, verð og afurðaeinkunn.</span><span class="sxs-lookup"><span data-stu-id="005c0-117">This information includes the product name, product images, the description, the price, and product ratings.</span></span>

<span data-ttu-id="005c0-118">Kaupgluggaeiningin gerir viðskiptavininum kleift að velja vöruvalkosti (til dæmis stærð, stíl og lit) og bæta vörunni í körfuna.</span><span class="sxs-lookup"><span data-stu-id="005c0-118">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="005c0-119">Hún gerir viðskiptavininum einnig kleift að kaupa vöruna á netinu og sækja hana í verslun.</span><span class="sxs-lookup"><span data-stu-id="005c0-119">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="005c0-120">Kaupið á netinu og sótt í verslunareininguna notar samþættingu við forritunarviðmót Bing Maps forrita (API) til að finna nálægar verslanir eða verslanir á öðrum stað sem viðskiptavinurinn tilgreinir.</span><span class="sxs-lookup"><span data-stu-id="005c0-120">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="005c0-121">Kaupgluggaeining þarf afurðakenni.</span><span class="sxs-lookup"><span data-stu-id="005c0-121">A buy box module requires a product ID.</span></span> <span data-ttu-id="005c0-122">Þetta auðkenni er dregið af samhengi síðunnar.</span><span class="sxs-lookup"><span data-stu-id="005c0-122">This ID is derived from the page context.</span></span> <span data-ttu-id="005c0-123">Ef kaupgluggaeiningu er bætt við síðu þar sem samhengi síðunnar er ekki með afurðakenni, mun hún ekki birta upplýsingarnar rétt.</span><span class="sxs-lookup"><span data-stu-id="005c0-123">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="005c0-124">Afurðaskilgreiningaeining</span><span class="sxs-lookup"><span data-stu-id="005c0-124">Product specifications module</span></span>

<span data-ttu-id="005c0-125">Hægt er að nota afurðaskilgreiningareininguna til að sýna frekari upplýsingar um vöruna.</span><span class="sxs-lookup"><span data-stu-id="005c0-125">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="005c0-126">Þessar upplýsingar eru fengnar frá afurðareigindum í Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="005c0-126">These details are taken from product attributes in Dynamics 365 Retail.</span></span> <span data-ttu-id="005c0-127">Vörulýsingareiningin sýnir alla eiginleika þar sem eiginleikinn **sýnilegt** er stilltur á **satt**.</span><span class="sxs-lookup"><span data-stu-id="005c0-127">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="005c0-128">Það þarf afurðakenni til að sækja afurðareigindir.</span><span class="sxs-lookup"><span data-stu-id="005c0-128">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="005c0-129">Tillagnaeining</span><span class="sxs-lookup"><span data-stu-id="005c0-129">Recommendations module</span></span>

<span data-ttu-id="005c0-130">Tillagnaeiningin er mikilvæg einingin á PDP.</span><span class="sxs-lookup"><span data-stu-id="005c0-130">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="005c0-131">Meðan viðskiptavinir leita að vörum ætti að kynna þeim fleiri vöruvalkosti svo þeir geti fundið réttu vöruna og gert kaup.</span><span class="sxs-lookup"><span data-stu-id="005c0-131">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="005c0-132">Tilmæli hjálpa viðskiptavinum að uppgötva tengt efni og halda áfram að versla.</span><span class="sxs-lookup"><span data-stu-id="005c0-132">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="005c0-133">Mismunandi gerðir tillagna eru tiltækar:</span><span class="sxs-lookup"><span data-stu-id="005c0-133">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="005c0-134">Listinn **Fólki líkar einnig** er byggður á vélanámi.</span><span class="sxs-lookup"><span data-stu-id="005c0-134">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="005c0-135">Hann notar viðskiptasögu annarra viðskiptavina til að veita ráðleggingar.</span><span class="sxs-lookup"><span data-stu-id="005c0-135">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="005c0-136">Þessi listi er búinn til með ráðleggingaþjónustunni og líkist listunum „Viðskiptavinir sem keyptu þetta keyptu líka ...“.</span><span class="sxs-lookup"><span data-stu-id="005c0-136">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="005c0-137">Afurðakennis er krafist til að búa til þennan lista.</span><span class="sxs-lookup"><span data-stu-id="005c0-137">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="005c0-138">Listann **Tengt** er hægt að stilla lista fyrir vöru í Retail.</span><span class="sxs-lookup"><span data-stu-id="005c0-138">A **Related** list can be configured for a product in Retail.</span></span> <span data-ttu-id="005c0-139">Til dæmis, fyrir brúna handtösku úr leðri, er hægt að stilla fleiri handtöskur úr leðri eða hannaðar til að nota í ferðalögum fyrir viðkomandi lista.</span><span class="sxs-lookup"><span data-stu-id="005c0-139">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="005c0-140">Aðrar gerðir tengdra lista, svo sem **Aukahlutir** og **Meira eins og þetta** er einnig er hægt að stilla í Retail.</span><span class="sxs-lookup"><span data-stu-id="005c0-140">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Retail.</span></span> <span data-ttu-id="005c0-141">Afurðakennis er krafist til að búa til þennan lista.</span><span class="sxs-lookup"><span data-stu-id="005c0-141">A product ID is required to generate this list.</span></span> <span data-ttu-id="005c0-142">Þess vegna, ef því er bætt við heimasíðuna, þar sem samhengi síðunnar inniheldur ekki afurðakenni, verður listinn tómur.</span><span class="sxs-lookup"><span data-stu-id="005c0-142">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="005c0-143">Algrímmyndaðir myndaðir tillagnalistar, eins og **Vinsælt**, **Mest selt** og **Nýtt** má nota á PDP.</span><span class="sxs-lookup"><span data-stu-id="005c0-143">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="005c0-144">Þó að þessir listar séu kannski ekki í beinum tengslum við vöruna á PDP, eru þeir önnur leið til að hjálpa viðskiptavinum að finna vörur sem gætu haft áhuga á þeim.</span><span class="sxs-lookup"><span data-stu-id="005c0-144">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="005c0-145">Þessar gerðir lista þurfa ekki afurðakenni.</span><span class="sxs-lookup"><span data-stu-id="005c0-145">These types of lists don't require a product ID.</span></span> <span data-ttu-id="005c0-146">Þetta eru almennir listar sem eru búnir til út frá innkaupamynstrum á vefnum.</span><span class="sxs-lookup"><span data-stu-id="005c0-146">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="005c0-147">Ritstjórnarlistar eru handvirkir listar.</span><span class="sxs-lookup"><span data-stu-id="005c0-147">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="005c0-148">Til dæmis gæti smásali ákveðið að setja handvirkt saman lista yfir vörur sem hann vill sýna.</span><span class="sxs-lookup"><span data-stu-id="005c0-148">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-module"></a><span data-ttu-id="005c0-149">Einkunna- og umsagnaeining</span><span class="sxs-lookup"><span data-stu-id="005c0-149">Ratings and reviews module</span></span>

<span data-ttu-id="005c0-150">Einingin fyrir einkunnir og umsagnir sýnir einkunnir og umsagnir sem aðrir viðskiptavinir hafa gefið.</span><span class="sxs-lookup"><span data-stu-id="005c0-150">The ratings and reviews module shows ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="005c0-151">Hún gerir viðskiptavinum einnig kleift að skrifa sína eigin umsögn um afurðina.</span><span class="sxs-lookup"><span data-stu-id="005c0-151">It also lets a customer write his or her own review of the product.</span></span> <span data-ttu-id="005c0-152">Að auki inniheldur hún súlurit sem sýnir einkunnagjöf fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="005c0-152">Additionally, it includes a histogram that shows the ratings trend for the product.</span></span> <span data-ttu-id="005c0-153">Frekari upplýsingar eru í [Yfirlit yfir einkunnir og umsagnir](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="005c0-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="005c0-154">Markaðssetningareiningar</span><span class="sxs-lookup"><span data-stu-id="005c0-154">Marketing modules</span></span>

<span data-ttu-id="005c0-155">Ef markaðsefni er einstakt fyrir ákveðna afurð er hægt að bæta hvaða markaðsseiningu sem er við PDP.</span><span class="sxs-lookup"><span data-stu-id="005c0-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="005c0-156">Þú getur bætt markaðsseiningum við PDP með því að „auðga“ síðuna.</span><span class="sxs-lookup"><span data-stu-id="005c0-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="005c0-157">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="005c0-157">Additional resources</span></span>

[<span data-ttu-id="005c0-158">Yfirlit yfir heimasíðuna</span><span class="sxs-lookup"><span data-stu-id="005c0-158">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="005c0-159">Yfirlit sjálfgefinnar lendingarsíðu flokks og leitarniðurstöðusíðu</span><span class="sxs-lookup"><span data-stu-id="005c0-159">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="005c0-160">Yfirlit yfir á körfu- og greiðsluferlissíður</span><span class="sxs-lookup"><span data-stu-id="005c0-160">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="005c0-161">Yfirlit yfir síður reikningastjórnunar</span><span class="sxs-lookup"><span data-stu-id="005c0-161">Overview of account management pages</span></span>](quick-tour-account-management.md)
