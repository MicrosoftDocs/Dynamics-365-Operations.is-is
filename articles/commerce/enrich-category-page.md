---
title: Bæta lendingarsíðu flokks
description: Þetta efni fjallar um auðgun flokksíðna í Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4ab152dff0925f9c816419083577b5272ac813be
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945784"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="27682-103">Bæta lendingarsíðu flokks</span><span class="sxs-lookup"><span data-stu-id="27682-103">Enrich a category landing page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="27682-104">Þetta efni fjallar um auðgun flokksíðna í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="27682-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="27682-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="27682-105">Overview</span></span>

<span data-ttu-id="27682-106">Commerce býður upp á sjálfgefna áfangasíðu flokks sem er notuð þegar flokkagögn eru sýnd.</span><span class="sxs-lookup"><span data-stu-id="27682-106">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="27682-107">Sjálfgefin flokksíða inniheldur nauðsynlega þætti, svo sem hreinsara, flokkaða afurðastaðsetningu, flokkunarvalkosti, yfirlit yfir val og síðuskiptingarstýringar.</span><span class="sxs-lookup"><span data-stu-id="27682-107">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="27682-108">Í staðinn fyrir að nota sjálfgefna flokkasíðuna gætirðu viljað nota „auðgað“ áfangasíðu flokks sem hefur meira efni og sértækari þætti.</span><span class="sxs-lookup"><span data-stu-id="27682-108">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="27682-109">Dæmigert auðgun gæti falið í sér að bæta flokkasértæku markaðsefni á flokksíðuna.</span><span class="sxs-lookup"><span data-stu-id="27682-109">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="27682-110">Þetta efni gæti falið í sér vöruflokka þvert á flokka fyrir krosssölu, ritstjórnarlista, myndir, myndskeið og annan texta.</span><span class="sxs-lookup"><span data-stu-id="27682-110">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="27682-111">Þú getur annaðhvort breytt sjálfgefnu flokkasíðunni eða skilgreint aðra flokkasíðu fyrir ákveðinn flokk.</span><span class="sxs-lookup"><span data-stu-id="27682-111">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Bætt lendingarsíða flokks](./media/CategoryLandingPages.png)

<span data-ttu-id="27682-113">Í höfundatólinu inniheldur síðan **Afurð** lista yfir flokka úr rásinni sem er úthlutað á síðuna.</span><span class="sxs-lookup"><span data-stu-id="27682-113">In the authoring tool, the **Product** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="27682-114">Ef staðan **Auðgað** er valin fyrir flokksíðu hefur sú flokksíða verið auðguð.</span><span class="sxs-lookup"><span data-stu-id="27682-114">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="27682-115">Að öðrum kosti er sjálfgefna flokkasíðan og innihaldið notað fyrir flokkinn.</span><span class="sxs-lookup"><span data-stu-id="27682-115">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="27682-116">Þú getur forskoðað bæði auðgaðar og óauðgaðar flokkasíður fyrir flokk með því að velja flokksheitið.</span><span class="sxs-lookup"><span data-stu-id="27682-116">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="27682-117">Til að auðga flokkasíðu skaltu gera eftirfarandi.</span><span class="sxs-lookup"><span data-stu-id="27682-117">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="27682-118">Á síðunni **Afurðir** velurðu nafn þess flokks sem þú vilt auðga flokkasíðuna fyrir.</span><span class="sxs-lookup"><span data-stu-id="27682-118">On the **Products** page, select the name of the category that you want to enrich the category page for.</span></span> <span data-ttu-id="27682-119">Sjálfgefin flokksíða fyrir valinn flokk er opnuð í ritlinum.</span><span class="sxs-lookup"><span data-stu-id="27682-119">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="27682-120">Veldu **Auðga flokkasíðu**.</span><span class="sxs-lookup"><span data-stu-id="27682-120">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="27682-121">Veldu sniðmát fyrir auðgaða flokkasíðu.</span><span class="sxs-lookup"><span data-stu-id="27682-121">Select a template for the enriched category page.</span></span> <span data-ttu-id="27682-122">Ef þú ert að gera aðeins smávægilegar breytingar geturðu valið sjálfgefna flokkasíðuna.</span><span class="sxs-lookup"><span data-stu-id="27682-122">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="27682-123">Þú getur einnig valið ákveðið sniðmát fyrir flokksíðu.</span><span class="sxs-lookup"><span data-stu-id="27682-123">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="27682-124">Þegar þú velur sniðmátið opnast ritstjórinn og valda sniðmátið er notað til að búa til nýja flokksíðu fyrir valinn flokk.</span><span class="sxs-lookup"><span data-stu-id="27682-124">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="27682-125">Síðan er skráð út til þín og þú getur nú gert breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="27682-125">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="27682-126">Einingar sem nota flokkagerðargögn nota gögnin úr völdum flokknum.</span><span class="sxs-lookup"><span data-stu-id="27682-126">Modules that use category specification data use the data from your selected category.</span></span>
>
> <span data-ttu-id="27682-127">Stillingar sniðmátsins sem þú velur ákvarða breytingar sem þú getur gert.</span><span class="sxs-lookup"><span data-stu-id="27682-127">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="27682-128">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="27682-128">Additional resources</span></span>

[<span data-ttu-id="27682-129">Breyta síðu svæðis sem þegar er til</span><span class="sxs-lookup"><span data-stu-id="27682-129">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="27682-130">Bæta við nýrri síðu á svæði</span><span class="sxs-lookup"><span data-stu-id="27682-130">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="27682-131">Velja síðuútlit</span><span class="sxs-lookup"><span data-stu-id="27682-131">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="27682-132">Stjórna SEO-lýsigögnum</span><span class="sxs-lookup"><span data-stu-id="27682-132">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="27682-133">Vista, forskoða og birta síðu</span><span class="sxs-lookup"><span data-stu-id="27682-133">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="27682-134">Bæta vörusíðu</span><span class="sxs-lookup"><span data-stu-id="27682-134">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="27682-135">Staðfesta aðgengi síðuinnihalds</span><span class="sxs-lookup"><span data-stu-id="27682-135">Verify page content accessibility</span></span>](verify-accessibility.md)
