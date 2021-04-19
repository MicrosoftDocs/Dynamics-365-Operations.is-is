---
title: Bæta vörusíðu
description: Þetta efnisatriði lýsir hvernig á að auðga vörusíðu í Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6c1a9474ed514426386b1d7b4a72b62129cdb8a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799046"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="970f7-103">Bæta vörusíðu</span><span class="sxs-lookup"><span data-stu-id="970f7-103">Enrich a product page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="970f7-104">Þetta efnisatriði lýsir hvernig á að auðga vörusíðu í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="970f7-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="970f7-105">Sjálfgefið er að vefsíðan þín noti almenna síðu til að sýna vörugögn.</span><span class="sxs-lookup"><span data-stu-id="970f7-105">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="970f7-106">Þessi síða inniheldur grunnupplýsingar um vöruna og stjórntæki sem þarf til að selja hana.</span><span class="sxs-lookup"><span data-stu-id="970f7-106">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="970f7-107">Hins vegar geturðu bætt við upplýsingarnar sem koma frá Commerce Scale Unit með viðbótarmyndum eða texta fyrir tiltekna afurð.</span><span class="sxs-lookup"><span data-stu-id="970f7-107">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="970f7-108">Þetta ferli er þekkt sem að auðga vörusíðuna.</span><span class="sxs-lookup"><span data-stu-id="970f7-108">This process is known as enriching the product page.</span></span>

<span data-ttu-id="970f7-109">Í mörgum tilvikum viltu nota sérstakt viðbótarefni fyrir vörur þínar.</span><span class="sxs-lookup"><span data-stu-id="970f7-109">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="970f7-110">Þegar þú ferð til **Retail og Commerce** í höfundatólinu sérðu lista yfir afurðir af rásinni sem er úthlutað á svæðið.</span><span class="sxs-lookup"><span data-stu-id="970f7-110">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="970f7-111">Í þessum lista gefur dálkurinn **Auðgað** til kynna hvort vörusíðan fyrir vöru hafi verið auðguð.</span><span class="sxs-lookup"><span data-stu-id="970f7-111">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="970f7-112">Ef gátmerki birtist í dálknum er auðguð vörusíða til staðar fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="970f7-112">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="970f7-113">Ef ekkert hak birtist er sjálfgefna vörusíðan og innihald notað fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="970f7-113">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="970f7-114">Þú getur forskoðað bæði auðgaðar og óauðgaðar vörusíður með því að velja vöruheiti á listanum.</span><span class="sxs-lookup"><span data-stu-id="970f7-114">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="970f7-115">Bæta vörusíðu</span><span class="sxs-lookup"><span data-stu-id="970f7-115">Enrich a product page</span></span>

<span data-ttu-id="970f7-116">Fylgdu þessum skrefum til að auðga vörusíðu.</span><span class="sxs-lookup"><span data-stu-id="970f7-116">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="970f7-117">Undir **Svæði** velurðu **Fabrikam** (eða heiti svæðisins).</span><span class="sxs-lookup"><span data-stu-id="970f7-117">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="970f7-118">Í stýriglugganum vinstra megin velurðu **Afurðir**.</span><span class="sxs-lookup"><span data-stu-id="970f7-118">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="970f7-119">Veldu allar vörur sem eru ekki með auðgaða vörusíðu.</span><span class="sxs-lookup"><span data-stu-id="970f7-119">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="970f7-120">Í aðgerðasvæðinu velurðu **Auðga afurðasíðu**.</span><span class="sxs-lookup"><span data-stu-id="970f7-120">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="970f7-121">Veldu **PDP-sniðmát** og síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="970f7-121">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="970f7-122">Í útlínutré síðunnar til hægri stækkarðu hólfið **Aðal**.</span><span class="sxs-lookup"><span data-stu-id="970f7-122">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="970f7-123">Veldu úrfellingarhnappinn (**...**) fyrir hólfið **Aðal** og veldu síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="970f7-123">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="970f7-124">Veldu **Gámur 2** og síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="970f7-124">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="970f7-125">Veldu úrfellingarhnappinn fyrir **Gámur 2** og veldu síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="970f7-125">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="970f7-126">Veldu **Eiginleiki** og síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="970f7-126">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="970f7-127">Í eiginleikaglugganum til hægri, í reitnum **Sniðinn texti** slærðu inn uppfærða lýsingu vörunnar.</span><span class="sxs-lookup"><span data-stu-id="970f7-127">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="970f7-128">Í reitinn **Fyrirsögn** slærðu inn fyrirsagnartexta og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="970f7-128">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="970f7-129">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="970f7-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="970f7-130">Í reitnum **Athugasemdir** slærðu inn **Afurð auðguð** og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="970f7-130">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="970f7-131">Veldu **Forskoða** til að forskoða auðgaða afurðasíðu.</span><span class="sxs-lookup"><span data-stu-id="970f7-131">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="970f7-132">Þegar þú hefur lokið því skaltu loka forskoðunarflipanum til að fara aftur í höfundatólið.</span><span class="sxs-lookup"><span data-stu-id="970f7-132">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="970f7-133">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="970f7-133">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="970f7-134">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="970f7-134">Additional resources</span></span>

[<span data-ttu-id="970f7-135">Breyta síðu svæðis sem þegar er til</span><span class="sxs-lookup"><span data-stu-id="970f7-135">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="970f7-136">Bæta við nýrri síðu á svæði</span><span class="sxs-lookup"><span data-stu-id="970f7-136">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="970f7-137">Velja síðuútlit</span><span class="sxs-lookup"><span data-stu-id="970f7-137">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="970f7-138">Stjórna SEO-lýsigögnum</span><span class="sxs-lookup"><span data-stu-id="970f7-138">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="970f7-139">Vista, forskoða og birta síðu</span><span class="sxs-lookup"><span data-stu-id="970f7-139">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="970f7-140">Bæta lendingarsíðu flokks</span><span class="sxs-lookup"><span data-stu-id="970f7-140">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="970f7-141">Staðfesta aðgengi að efni síðu</span><span class="sxs-lookup"><span data-stu-id="970f7-141">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="970f7-142">Búa til gagnvirkar síður fyrir rafræn viðskipti sem byggja á færibreytum vefslóða</span><span class="sxs-lookup"><span data-stu-id="970f7-142">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
