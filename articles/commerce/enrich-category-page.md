---
title: Bæta lendingarsíðu flokks
description: Þetta efni fjallar um auðgun flokksíðna í Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fbcf6ec60723b726e022b4e17bbde4c903e5cb57
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238779"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="c2230-103">Bæta lendingarsíðu flokks</span><span class="sxs-lookup"><span data-stu-id="c2230-103">Enrich a category landing page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c2230-104">Þetta efni fjallar um auðgun flokksíðna í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c2230-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c2230-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="c2230-105">Overview</span></span>

<span data-ttu-id="c2230-106">Commerce býður upp á sjálfgefna áfangasíðu flokks sem er notuð þegar flokkagögn eru sýnd.</span><span class="sxs-lookup"><span data-stu-id="c2230-106">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="c2230-107">Sjálfgefin flokksíða inniheldur nauðsynlega þætti, svo sem hreinsara, flokkaða afurðastaðsetningu, flokkunarvalkosti, yfirlit yfir val og síðuskiptingarstýringar.</span><span class="sxs-lookup"><span data-stu-id="c2230-107">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="c2230-108">Í staðinn fyrir að nota sjálfgefna flokkasíðuna gætirðu viljað nota „auðgað“ áfangasíðu flokks sem hefur meira efni og sértækari þætti.</span><span class="sxs-lookup"><span data-stu-id="c2230-108">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="c2230-109">Dæmigert auðgun gæti falið í sér að bæta flokkasértæku markaðsefni á flokksíðuna.</span><span class="sxs-lookup"><span data-stu-id="c2230-109">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="c2230-110">Þetta efni gæti falið í sér vöruflokka þvert á flokka fyrir krosssölu, ritstjórnarlista, myndir, myndskeið og annan texta.</span><span class="sxs-lookup"><span data-stu-id="c2230-110">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="c2230-111">Þú getur annaðhvort breytt sjálfgefnu flokkasíðunni eða skilgreint aðra flokkasíðu fyrir ákveðinn flokk.</span><span class="sxs-lookup"><span data-stu-id="c2230-111">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Bætt lendingarsíða flokks](./media/CategoryLandingPages.png)

<span data-ttu-id="c2230-113">Í svæðissmið Commerce inniheldur síðan **Vörur** lista yfir flokka frá rásinni sem er úthlutað á svæðið.</span><span class="sxs-lookup"><span data-stu-id="c2230-113">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="c2230-114">Ef staðan **Auðgað** er valin fyrir flokksíðu hefur sú flokksíða verið auðguð.</span><span class="sxs-lookup"><span data-stu-id="c2230-114">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="c2230-115">Að öðrum kosti er sjálfgefna flokkasíðan og innihaldið notað fyrir flokkinn.</span><span class="sxs-lookup"><span data-stu-id="c2230-115">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="c2230-116">Þú getur forskoðað bæði auðgaðar og óauðgaðar flokkasíður fyrir flokk með því að velja flokksheitið.</span><span class="sxs-lookup"><span data-stu-id="c2230-116">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="c2230-117">Til að auðga flokkasíðu skaltu gera eftirfarandi.</span><span class="sxs-lookup"><span data-stu-id="c2230-117">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="c2230-118">Á síðunni **Vörur** velur þú heiti flokksins sem þú vilt bæta við flokkasíðuna.</span><span class="sxs-lookup"><span data-stu-id="c2230-118">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="c2230-119">Sjálfgefin flokksíða fyrir valinn flokk er opnuð í ritlinum.</span><span class="sxs-lookup"><span data-stu-id="c2230-119">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="c2230-120">Veldu **Auðga flokkasíðu**.</span><span class="sxs-lookup"><span data-stu-id="c2230-120">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="c2230-121">Veldu sniðmát fyrir auðgaða flokkasíðu.</span><span class="sxs-lookup"><span data-stu-id="c2230-121">Select a template for the enriched category page.</span></span> <span data-ttu-id="c2230-122">Ef þú ert að gera aðeins smávægilegar breytingar geturðu valið sjálfgefna flokkasíðuna.</span><span class="sxs-lookup"><span data-stu-id="c2230-122">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="c2230-123">Þú getur einnig valið ákveðið sniðmát fyrir flokksíðu.</span><span class="sxs-lookup"><span data-stu-id="c2230-123">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="c2230-124">Þegar þú velur sniðmátið opnast ritstjórinn og valda sniðmátið er notað til að búa til nýja flokksíðu fyrir valinn flokk.</span><span class="sxs-lookup"><span data-stu-id="c2230-124">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="c2230-125">Síðan er skráð út til þín og þú getur nú gert breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="c2230-125">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="c2230-126">Einingar sem nota flokkagerðargögn nota gögnin úr völdum flokknum.</span><span class="sxs-lookup"><span data-stu-id="c2230-126">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="c2230-127">Stillingar sniðmátsins sem þú velur ákvarða breytingar sem þú getur gert.</span><span class="sxs-lookup"><span data-stu-id="c2230-127">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2230-128">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c2230-128">Additional resources</span></span>

[<span data-ttu-id="c2230-129">Breyta síðu svæðis sem þegar er til</span><span class="sxs-lookup"><span data-stu-id="c2230-129">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="c2230-130">Bæta við nýrri síðu á svæði</span><span class="sxs-lookup"><span data-stu-id="c2230-130">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="c2230-131">Velja síðuútlit</span><span class="sxs-lookup"><span data-stu-id="c2230-131">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="c2230-132">Stjórna SEO-lýsigögnum</span><span class="sxs-lookup"><span data-stu-id="c2230-132">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="c2230-133">Vista, forskoða og birta síðu</span><span class="sxs-lookup"><span data-stu-id="c2230-133">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="c2230-134">Bæta vörusíðu</span><span class="sxs-lookup"><span data-stu-id="c2230-134">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="c2230-135">Staðfesta aðgengi að efni síðu</span><span class="sxs-lookup"><span data-stu-id="c2230-135">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="c2230-136">Búa til gagnvirkar síður fyrir rafræn viðskipti sem byggja á færibreytum vefslóða</span><span class="sxs-lookup"><span data-stu-id="c2230-136">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]