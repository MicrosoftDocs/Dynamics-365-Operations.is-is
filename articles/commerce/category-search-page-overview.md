---
title: Yfirlit yfir sjálfgefna lendingarsíðu og leitarniðurstöðusíðu
description: Þetta efni veitir yfirlit yfir sjálfgefna áfangasíðu flokks og leitarniðurstöðusíðu í Dynamics 365 Commerce.
author: ashishmsft
ms.date: 06/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f380f3f56727d927d7cd328fef3c9d999afa2873
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794350"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a><span data-ttu-id="7171b-103">Yfirlit yfir sjálfgefna lendingarsíðu og leitarniðurstöðusíðu</span><span class="sxs-lookup"><span data-stu-id="7171b-103">Default category landing page and search results page overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7171b-104">Þetta efni veitir yfirlit yfir sjálfgefna áfangasíðu flokks og leitarniðurstöðusíðu í Microsoft Dynamics 365 Commerce rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="7171b-104">This topic provides an overview of the default category landing page and search results page in Microsoft Dynamics 365 Commerce e-Commerce.</span></span>

## <a name="default-category-landing-page"></a><span data-ttu-id="7171b-105">Sjálfgefin lendingarsíða flokks</span><span class="sxs-lookup"><span data-stu-id="7171b-105">Default category landing page</span></span>

<span data-ttu-id="7171b-106">Sjálfgefin lendingasíða flokks er sú síðu sem notendur vefsíðna eru venjulega færðir til þegar þeir velja flokk í yfirlitsstigveldi.</span><span class="sxs-lookup"><span data-stu-id="7171b-106">The default category landing page is the page that website users typically are taken to when they select a category in the navigation hierarchy.</span></span> <span data-ttu-id="7171b-107">Flokkasíðan gerir þér kleift að fletta og einnig er hægt að flokka og fínstilla flokkaðar vörur.</span><span class="sxs-lookup"><span data-stu-id="7171b-107">The category page lets you browse, and you can also sort and refine the categorized products.</span></span>

![Sjálfgefin lendingarsíða flokks](./media/SimpleCategoryLandingDressCategory.png)

<span data-ttu-id="7171b-109">Efst á síðunni er haus sem sýnir alla vöruflokka og aðrar síður sem vörustjórinn hefur flokkað.</span><span class="sxs-lookup"><span data-stu-id="7171b-109">At the top of the page is a header that shows all the product categories and other pages that the merchandising manager has categorized.</span></span> <span data-ttu-id="7171b-110">Stillingar eru gerðar sem hluti af stillingum yfirlitsstigveldis rásar.</span><span class="sxs-lookup"><span data-stu-id="7171b-110">Configuration is done as part of the configuration of the channel navigation hierarchy.</span></span> <span data-ttu-id="7171b-111">Neðst á síðunni er fótur sem inniheldur fljótlega tengla á ýmis efni sem kaupandi gæti haft áhuga á.</span><span class="sxs-lookup"><span data-stu-id="7171b-111">At the bottom of the page is a footer that includes quick links to various topics that a shopper might be interested in.</span></span>

<span data-ttu-id="7171b-112">Eftirfarandi þættir eru nauðsynlegir fyrir flokk:</span><span class="sxs-lookup"><span data-stu-id="7171b-112">The following components are essential for a category:</span></span>

- <span data-ttu-id="7171b-113">**Afurðastaðsetningarritir** sýna vörurnar sem verslunarstjórinn hefur skilgreint í flokk sem hluta af stillingum yfirlitsstigveldisins.</span><span class="sxs-lookup"><span data-stu-id="7171b-113">**Product placement tiles** show the products that the merchandising manager has defined in a category as part of the configuration of the navigation hierarchy.</span></span>
- <span data-ttu-id="7171b-114">**Yfirlit yfir hreinsara og val** eru síur sem veita fjölda og sem hægt er að nota til að fínstilla vörur.</span><span class="sxs-lookup"><span data-stu-id="7171b-114">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="7171b-115">Vörustjórinn stillir þá sem hluta af uppsetningu lýsigagnanna sem tengjast rásaflokkum og afurðareigindum.</span><span class="sxs-lookup"><span data-stu-id="7171b-115">The merchandising manager configures them as part of the configuration of the metadata related to channel categories and product attributes.</span></span>
- <span data-ttu-id="7171b-116">**Flokkunarvalkostir** eru notaðir af gestum vefsíðna til að flokka vörurnar.</span><span class="sxs-lookup"><span data-stu-id="7171b-116">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="7171b-117">Sjálfgefið er að eftirfarandi flokkunarvalkostir eru tiltækir:</span><span class="sxs-lookup"><span data-stu-id="7171b-117">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="7171b-118">Verð – lægsta til hæsta</span><span class="sxs-lookup"><span data-stu-id="7171b-118">Price – low to high</span></span>
    - <span data-ttu-id="7171b-119">Verð – hæsta til lægsta</span><span class="sxs-lookup"><span data-stu-id="7171b-119">Price – high to low</span></span>
    - <span data-ttu-id="7171b-120">Afurðaheiti – \[A-Z\]</span><span class="sxs-lookup"><span data-stu-id="7171b-120">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="7171b-121">Afurðaheiti – \[Z-A\]</span><span class="sxs-lookup"><span data-stu-id="7171b-121">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="7171b-122">Einkunnir – lægsta til hæsta</span><span class="sxs-lookup"><span data-stu-id="7171b-122">Ratings – low to high</span></span>
    - <span data-ttu-id="7171b-123">Einkunnir – hæsta til lægsta</span><span class="sxs-lookup"><span data-stu-id="7171b-123">Ratings – high to low</span></span>

- <span data-ttu-id="7171b-124">**Síðuskipting** gerir gestum vefsíðu kleift að fara af einni síðu með flokkaðar vöruniðurstöður á aðra síðu.</span><span class="sxs-lookup"><span data-stu-id="7171b-124">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="7171b-125">**Heildarfjöldi** veitir heildarfjölda vara sem eru skilgreindar í flokk.</span><span class="sxs-lookup"><span data-stu-id="7171b-125">**Total count** provides the total number of products that are defined in a category.</span></span>

## <a name="enrich-a-category-landing-page"></a><span data-ttu-id="7171b-126">Bæta lendingarsíðu flokks</span><span class="sxs-lookup"><span data-stu-id="7171b-126">Enrich a category landing page</span></span>

<span data-ttu-id="7171b-127">Ef þú vilt að lendingasíða flokks hafi sérsniðnari reynslu fyrir ákveðinn flokk geturðu „auðgað“ lendingarsíðuna fyrir þann flokk.</span><span class="sxs-lookup"><span data-stu-id="7171b-127">If you want a category landing page to have a more tailored experience for a specific category, you can "enrich" the category landing page for that category.</span></span> <span data-ttu-id="7171b-128">Til dæmis er hægt að bæta við markaðssetningarmyndbandi og sögufrásögn í flokknum til að ná athygli kaupandans.</span><span class="sxs-lookup"><span data-stu-id="7171b-128">For example, you can add a marketing video and some category storytelling to get the shopper's attention.</span></span> <span data-ttu-id="7171b-129">Sjá frekari upplýsingar [Bæta lendingarsíðu flokks](enrich-category-page.md).</span><span class="sxs-lookup"><span data-stu-id="7171b-129">For more information, see [Enrich a category landing page](enrich-category-page.md).</span></span>

![Bætt lendingarsíða flokks](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a><span data-ttu-id="7171b-131">Niðurstöðusíður sjálfvirkra uppástungna og leitar</span><span class="sxs-lookup"><span data-stu-id="7171b-131">Auto-suggest and search results pages</span></span>

<span data-ttu-id="7171b-132">Notendur vefsíðna geta kannað síðu annaðhvort með því að fara í flokk úr yfirlitsstigveli eða með því að slá inn leitarorð í leitarreitinn.</span><span class="sxs-lookup"><span data-stu-id="7171b-132">Website users can explore a site either by going to a category from the navigation hierarchy or by entering a search term in the search field.</span></span>

<span data-ttu-id="7171b-133">Um leið og notendur byrja að slá inn í leitarreitinn upplifa þeir þá heildstæðu sjálfvirkni sem stingur upp á leitarskilyrðum.</span><span class="sxs-lookup"><span data-stu-id="7171b-133">As soon as users start to type in the search field, they experience the immersive auto-suggest functionality that suggests search terms.</span></span>

<span data-ttu-id="7171b-134">Hér eru nokkrar af þeim tegundum tillagna sem gætu verið sýndar:</span><span class="sxs-lookup"><span data-stu-id="7171b-134">Here are some of the types of suggestions that might be shown:</span></span>

- <span data-ttu-id="7171b-135">**Lykilorð** eru notuð til að finna vörur í öllum afurðum sem eru flokkaðar í rásina.</span><span class="sxs-lookup"><span data-stu-id="7171b-135">**Keywords** are used to find items across all products that are assorted to the channel.</span></span>
- <span data-ttu-id="7171b-136">**Afurðir** veita beina tengla á upplýsingasíðu afurða.</span><span class="sxs-lookup"><span data-stu-id="7171b-136">**Products** provide direct links to the product details page.</span></span>
- <span data-ttu-id="7171b-137">**Leitartillögur fyrir víðtækan flokk** skráir ýmsa flokka og lætur notendur leita að leitarorðinu í tilteknum flokki.</span><span class="sxs-lookup"><span data-stu-id="7171b-137">**Scoped category search suggestions** list various categories and let users search for the keyword in a specific category.</span></span>

![Heildstæð sjálfvirkni](./media/ImmersiveAutoSuggestUX.png)

<span data-ttu-id="7171b-139">Þegar notendur velja eitt af lykilorðum eða víðtækum leitarflokkum í leitartillögum eða ef það eru engar tillögur að leitarorðinu sem þeir slá inn, er þeim vísað á leitarniðurstöðusíðuna.</span><span class="sxs-lookup"><span data-stu-id="7171b-139">When users select one of the keyword or scoped category search suggestions, or when there are no suggestions for the search term that they enter, they are redirected to a search results page.</span></span> <span data-ttu-id="7171b-140">Notendur geta síðan flett, flokkað og betrumbætt lista yfir leitarniðurstöður til að finna þá vöru sem óskað er.</span><span class="sxs-lookup"><span data-stu-id="7171b-140">The users can then browse, sort, and refine the list of search results to find the desired item.</span></span>

![Leitarlending](./media/SearchLanding.png)

<span data-ttu-id="7171b-142">Eftirfarandi þættir eru nauðsynlegir fyrir leitarniðurstöðusíðu:</span><span class="sxs-lookup"><span data-stu-id="7171b-142">The following components are essential for a search results page:</span></span>

- <span data-ttu-id="7171b-143">**Afurðastaðsetningarreitir** sýna afurðir fyrir notandaleitina.</span><span class="sxs-lookup"><span data-stu-id="7171b-143">**Product placement tiles** show the products for the user's search.</span></span> <span data-ttu-id="7171b-144">Sjálfgefið er að þessir reitir séu flokkaðir eftir skýjadrifnu mikilvægisstigi leitar fyrir notendaleit.</span><span class="sxs-lookup"><span data-stu-id="7171b-144">By default, these tiles are sorted by the cloud-powered search relevancy score for the user search.</span></span>
- <span data-ttu-id="7171b-145">**Yfirlit yfir hreinsara og val** eru síur sem veita fjölda og sem hægt er að nota til að fínstilla vörur.</span><span class="sxs-lookup"><span data-stu-id="7171b-145">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="7171b-146">Vörustjórinn stillir þá sem hluta af uppsetningu lýsigagnanna sem tengjast lýsigögnum „rásaflokka og afurðareiginda“.</span><span class="sxs-lookup"><span data-stu-id="7171b-146">The merchandising manager configures them as part of the configuration of the "channel categories and product attributes" metadata.</span></span>
- <span data-ttu-id="7171b-147">**Flokkunarvalkostir** eru notaðir af gestum vefsíðna til að flokka vörurnar.</span><span class="sxs-lookup"><span data-stu-id="7171b-147">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="7171b-148">Sjálfgefið er að eftirfarandi flokkunarvalkostir eru tiltækir:</span><span class="sxs-lookup"><span data-stu-id="7171b-148">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="7171b-149">Verð – lægsta til hæsta</span><span class="sxs-lookup"><span data-stu-id="7171b-149">Price – low to high</span></span>
    - <span data-ttu-id="7171b-150">Verð – hæsta til lægsta</span><span class="sxs-lookup"><span data-stu-id="7171b-150">Price – high to low</span></span>
    - <span data-ttu-id="7171b-151">Afurðaheiti – \[A-Z\]</span><span class="sxs-lookup"><span data-stu-id="7171b-151">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="7171b-152">Afurðaheiti – \[Z-A\]</span><span class="sxs-lookup"><span data-stu-id="7171b-152">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="7171b-153">Einkunnir – lægsta til hæsta</span><span class="sxs-lookup"><span data-stu-id="7171b-153">Ratings – low to high</span></span>
    - <span data-ttu-id="7171b-154">Einkunnir – hæsta til lægsta</span><span class="sxs-lookup"><span data-stu-id="7171b-154">Ratings – high to low</span></span>
    - <span data-ttu-id="7171b-155">Sjálfgefinn</span><span class="sxs-lookup"><span data-stu-id="7171b-155">Default</span></span>

- <span data-ttu-id="7171b-156">**Síðuskipting** gerir gestum vefsíðu kleift að fara af einni síðu með flokkaðar vöruniðurstöður á aðra síðu.</span><span class="sxs-lookup"><span data-stu-id="7171b-156">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="7171b-157">**Heildarfjöldi** veitir heildarfjölda vara sem eru skilgreindar í flokk og samsvara leitarskilyrðum.</span><span class="sxs-lookup"><span data-stu-id="7171b-157">**Total count** provides the total number of products that are defined in a category and that match the search criteria.</span></span>

>[!NOTE]
><span data-ttu-id="7171b-158">Þessir leitareiginleikar í skýi eru tiltækir frá útgáfu 10.0.8.</span><span class="sxs-lookup"><span data-stu-id="7171b-158">These cloud-powered search capabilities are available starting in version 10.0.8.</span></span> <span data-ttu-id="7171b-159">Gangið úr skugga um að undir **Viðskiptafæribreytur > Skilgreiningarfæribreytur** sé færsla fyrir „ProductSearch.UseAzureSearch stillt á true“.</span><span class="sxs-lookup"><span data-stu-id="7171b-159">Ensure that under **Commerce Parameters > Configuration Parameters** there is an entry for "ProductSearch.UseAzureSearch set to 'true'".</span></span> 
<span data-ttu-id="7171b-160">![Færibreytur skilgreininga fyrir leit í skýinu](./media/CloudPoweredSearchConfigurationParameters.png)</span><span class="sxs-lookup"><span data-stu-id="7171b-160">![Configuration parameters for cloud-powered search](./media/CloudPoweredSearchConfigurationParameters.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7171b-161">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7171b-161">Additional resources</span></span>

[<span data-ttu-id="7171b-162">Leitaryfirlit í skýinu</span><span class="sxs-lookup"><span data-stu-id="7171b-162">Cloud-powered search overview</span></span>](cloud-powered-search-overview.md)

[<span data-ttu-id="7171b-163">Yfirlit heimasíðu</span><span class="sxs-lookup"><span data-stu-id="7171b-163">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="7171b-164">Yfirlýt upplýsingasíðu afurða</span><span class="sxs-lookup"><span data-stu-id="7171b-164">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="7171b-165">Yfirlit yfir síður körfu og greiðsluferlis</span><span class="sxs-lookup"><span data-stu-id="7171b-165">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="7171b-166">Yfirlit yfir síður fyrir stjórnun reikninga</span><span class="sxs-lookup"><span data-stu-id="7171b-166">Account management pages overview</span></span>](quick-tour-account-management.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]