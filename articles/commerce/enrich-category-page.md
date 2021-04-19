---
title: Bæta lendingarsíðu flokks
description: Þetta efni fjallar um auðgun flokksíðna í Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
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
ms.openlocfilehash: 5e18439fc0e91619cade33b83b87be0d5c4d1040
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799012"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="7186f-103">Bæta lendingarsíðu flokks</span><span class="sxs-lookup"><span data-stu-id="7186f-103">Enrich a category landing page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7186f-104">Þetta efni fjallar um auðgun flokksíðna í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7186f-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7186f-105">Commerce býður upp á sjálfgefna áfangasíðu flokks sem er notuð þegar flokkagögn eru sýnd.</span><span class="sxs-lookup"><span data-stu-id="7186f-105">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="7186f-106">Sjálfgefin flokksíða inniheldur nauðsynlega þætti, svo sem hreinsara, flokkaða afurðastaðsetningu, flokkunarvalkosti, yfirlit yfir val og síðuskiptingarstýringar.</span><span class="sxs-lookup"><span data-stu-id="7186f-106">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="7186f-107">Í staðinn fyrir að nota sjálfgefna flokkasíðuna gætirðu viljað nota „auðgað“ áfangasíðu flokks sem hefur meira efni og sértækari þætti.</span><span class="sxs-lookup"><span data-stu-id="7186f-107">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="7186f-108">Dæmigert auðgun gæti falið í sér að bæta flokkasértæku markaðsefni á flokksíðuna.</span><span class="sxs-lookup"><span data-stu-id="7186f-108">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="7186f-109">Þetta efni gæti falið í sér vöruflokka þvert á flokka fyrir krosssölu, ritstjórnarlista, myndir, myndskeið og annan texta.</span><span class="sxs-lookup"><span data-stu-id="7186f-109">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="7186f-110">Þú getur annaðhvort breytt sjálfgefnu flokkasíðunni eða skilgreint aðra flokkasíðu fyrir ákveðinn flokk.</span><span class="sxs-lookup"><span data-stu-id="7186f-110">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Bætt lendingarsíða flokks](./media/CategoryLandingPages.png)

<span data-ttu-id="7186f-112">Í svæðissmið Commerce inniheldur síðan **Vörur** lista yfir flokka frá rásinni sem er úthlutað á svæðið.</span><span class="sxs-lookup"><span data-stu-id="7186f-112">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="7186f-113">Ef staðan **Auðgað** er valin fyrir flokksíðu hefur sú flokksíða verið auðguð.</span><span class="sxs-lookup"><span data-stu-id="7186f-113">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="7186f-114">Að öðrum kosti er sjálfgefna flokkasíðan og innihaldið notað fyrir flokkinn.</span><span class="sxs-lookup"><span data-stu-id="7186f-114">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="7186f-115">Þú getur forskoðað bæði auðgaðar og óauðgaðar flokkasíður fyrir flokk með því að velja flokksheitið.</span><span class="sxs-lookup"><span data-stu-id="7186f-115">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="7186f-116">Til að auðga flokkasíðu skaltu gera eftirfarandi.</span><span class="sxs-lookup"><span data-stu-id="7186f-116">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="7186f-117">Á síðunni **Vörur** velur þú heiti flokksins sem þú vilt bæta við flokkasíðuna.</span><span class="sxs-lookup"><span data-stu-id="7186f-117">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="7186f-118">Sjálfgefin flokksíða fyrir valinn flokk er opnuð í ritlinum.</span><span class="sxs-lookup"><span data-stu-id="7186f-118">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="7186f-119">Veldu **Auðga flokkasíðu**.</span><span class="sxs-lookup"><span data-stu-id="7186f-119">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="7186f-120">Veldu sniðmát fyrir auðgaða flokkasíðu.</span><span class="sxs-lookup"><span data-stu-id="7186f-120">Select a template for the enriched category page.</span></span> <span data-ttu-id="7186f-121">Ef þú ert að gera aðeins smávægilegar breytingar geturðu valið sjálfgefna flokkasíðuna.</span><span class="sxs-lookup"><span data-stu-id="7186f-121">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="7186f-122">Þú getur einnig valið ákveðið sniðmát fyrir flokksíðu.</span><span class="sxs-lookup"><span data-stu-id="7186f-122">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="7186f-123">Þegar þú velur sniðmátið opnast ritstjórinn og valda sniðmátið er notað til að búa til nýja flokksíðu fyrir valinn flokk.</span><span class="sxs-lookup"><span data-stu-id="7186f-123">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="7186f-124">Síðan er skráð út til þín og þú getur nú gert breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="7186f-124">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="7186f-125">Einingar sem nota flokkagerðargögn nota gögnin úr völdum flokknum.</span><span class="sxs-lookup"><span data-stu-id="7186f-125">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="7186f-126">Stillingar sniðmátsins sem þú velur ákvarða breytingar sem þú getur gert.</span><span class="sxs-lookup"><span data-stu-id="7186f-126">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7186f-127">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7186f-127">Additional resources</span></span>

[<span data-ttu-id="7186f-128">Breyta síðu svæðis sem þegar er til</span><span class="sxs-lookup"><span data-stu-id="7186f-128">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="7186f-129">Bæta við nýrri síðu á svæði</span><span class="sxs-lookup"><span data-stu-id="7186f-129">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="7186f-130">Velja síðuútlit</span><span class="sxs-lookup"><span data-stu-id="7186f-130">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="7186f-131">Stjórna SEO-lýsigögnum</span><span class="sxs-lookup"><span data-stu-id="7186f-131">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="7186f-132">Vista, forskoða og birta síðu</span><span class="sxs-lookup"><span data-stu-id="7186f-132">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="7186f-133">Bæta vörusíðu</span><span class="sxs-lookup"><span data-stu-id="7186f-133">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="7186f-134">Staðfesta aðgengi að efni síðu</span><span class="sxs-lookup"><span data-stu-id="7186f-134">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="7186f-135">Búa til gagnvirkar síður fyrir rafræn viðskipti sem byggja á færibreytum vefslóða</span><span class="sxs-lookup"><span data-stu-id="7186f-135">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
