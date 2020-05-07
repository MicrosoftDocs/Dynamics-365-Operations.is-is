---
title: Bæta vörusíðu
description: Þetta efni lýsir því hvernig á að bæta afurðasíðu í Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 12508a80c440894ec6e2073b5e550846480e6c45
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269821"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="40ed5-103">Bæta vörusíðu</span><span class="sxs-lookup"><span data-stu-id="40ed5-103">Enrich a product page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="40ed5-104">Þetta efni lýsir því hvernig á að bæta afurðasíðu í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="40ed5-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="40ed5-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="40ed5-105">Overview</span></span>

<span data-ttu-id="40ed5-106">Sjálfgefið er að vefsíðan þín noti almenna síðu til að sýna vörugögn.</span><span class="sxs-lookup"><span data-stu-id="40ed5-106">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="40ed5-107">Þessi síða inniheldur grunnupplýsingar um vöruna og stjórntæki sem þarf til að selja hana.</span><span class="sxs-lookup"><span data-stu-id="40ed5-107">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="40ed5-108">Hins vegar geturðu bætt við upplýsingarnar sem koma frá Commerce Scale Unit með viðbótarmyndum eða texta fyrir tiltekna afurð.</span><span class="sxs-lookup"><span data-stu-id="40ed5-108">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="40ed5-109">Þetta ferli er þekkt sem að auðga vörusíðuna.</span><span class="sxs-lookup"><span data-stu-id="40ed5-109">This process is known as enriching the product page.</span></span>

<span data-ttu-id="40ed5-110">Í mörgum tilvikum viltu nota sérstakt viðbótarefni fyrir vörur þínar.</span><span class="sxs-lookup"><span data-stu-id="40ed5-110">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="40ed5-111">Þegar þú ferð til **Retail og Commerce** í höfundatólinu sérðu lista yfir afurðir af rásinni sem er úthlutað á svæðið.</span><span class="sxs-lookup"><span data-stu-id="40ed5-111">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="40ed5-112">Í þessum lista gefur dálkurinn **Auðgað** til kynna hvort vörusíðan fyrir vöru hafi verið auðguð.</span><span class="sxs-lookup"><span data-stu-id="40ed5-112">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="40ed5-113">Ef gátmerki birtist í dálknum er auðguð vörusíða til staðar fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="40ed5-113">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="40ed5-114">Ef ekkert hak birtist er sjálfgefna vörusíðan og innihald notað fyrir vöruna.</span><span class="sxs-lookup"><span data-stu-id="40ed5-114">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="40ed5-115">Þú getur forskoðað bæði auðgaðar og óauðgaðar vörusíður með því að velja vöruheiti á listanum.</span><span class="sxs-lookup"><span data-stu-id="40ed5-115">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="40ed5-116">Bæta vörusíðu</span><span class="sxs-lookup"><span data-stu-id="40ed5-116">Enrich a product page</span></span>

<span data-ttu-id="40ed5-117">Fylgdu þessum skrefum til að auðga vörusíðu.</span><span class="sxs-lookup"><span data-stu-id="40ed5-117">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="40ed5-118">Undir **Svæði** velurðu **Fabrikam** (eða heiti svæðisins).</span><span class="sxs-lookup"><span data-stu-id="40ed5-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="40ed5-119">Í stýriglugganum vinstra megin velurðu **Afurðir**.</span><span class="sxs-lookup"><span data-stu-id="40ed5-119">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="40ed5-120">Veldu allar vörur sem eru ekki með auðgaða vörusíðu.</span><span class="sxs-lookup"><span data-stu-id="40ed5-120">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="40ed5-121">Í aðgerðasvæðinu velurðu **Auðga afurðasíðu**.</span><span class="sxs-lookup"><span data-stu-id="40ed5-121">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="40ed5-122">Veldu **PDP-sniðmát** og síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="40ed5-122">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="40ed5-123">Í útlínutré síðunnar til hægri stækkarðu hólfið **Aðal**.</span><span class="sxs-lookup"><span data-stu-id="40ed5-123">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="40ed5-124">Veldu úrfellingarhnappinn (**...**) fyrir hólfið **Aðal** og veldu síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="40ed5-124">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="40ed5-125">Veldu **Gámur 2** og síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="40ed5-125">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="40ed5-126">Veldu úrfellingarhnappinn fyrir **Gámur 2** og veldu síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="40ed5-126">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="40ed5-127">Veldu **Eiginleiki** og síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="40ed5-127">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="40ed5-128">Í eiginleikaglugganum til hægri, í reitnum **Sniðinn texti** slærðu inn uppfærða lýsingu vörunnar.</span><span class="sxs-lookup"><span data-stu-id="40ed5-128">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="40ed5-129">Í reitinn **Fyrirsögn** slærðu inn fyrirsagnartexta og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="40ed5-129">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="40ed5-130">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="40ed5-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="40ed5-131">Í reitnum **Athugasemdir** slærðu inn **Afurð auðguð** og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="40ed5-131">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="40ed5-132">Veldu **Forskoða** til að forskoða auðgaða afurðasíðu.</span><span class="sxs-lookup"><span data-stu-id="40ed5-132">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="40ed5-133">Þegar þú hefur lokið því skaltu loka forskoðunarflipanum til að fara aftur í höfundatólið.</span><span class="sxs-lookup"><span data-stu-id="40ed5-133">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="40ed5-134">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="40ed5-134">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="40ed5-135">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="40ed5-135">Additional resources</span></span>

[<span data-ttu-id="40ed5-136">Breyta síðu svæðis sem þegar er til</span><span class="sxs-lookup"><span data-stu-id="40ed5-136">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="40ed5-137">Bæta við nýrri síðu á svæði</span><span class="sxs-lookup"><span data-stu-id="40ed5-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="40ed5-138">Velja síðuútlit</span><span class="sxs-lookup"><span data-stu-id="40ed5-138">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="40ed5-139">Stjórna SEO-lýsigögnum</span><span class="sxs-lookup"><span data-stu-id="40ed5-139">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="40ed5-140">Vista, forskoða og birta síðu</span><span class="sxs-lookup"><span data-stu-id="40ed5-140">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="40ed5-141">Bæta lendingarsíðu flokks</span><span class="sxs-lookup"><span data-stu-id="40ed5-141">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="40ed5-142">Staðfesta aðgengi síðuinnihalds</span><span class="sxs-lookup"><span data-stu-id="40ed5-142">Verify page content accessibility</span></span>](verify-accessibility.md)
