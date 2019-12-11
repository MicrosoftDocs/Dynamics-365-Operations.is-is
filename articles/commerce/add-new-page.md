---
title: Bæta við nýrri síðu á svæði
description: Þetta efni lýsir því hvernig á að bæta við nýrri síðu svæðis í Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: d5ab90343220e427a80cc4dde17c628ba64ac69e
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696739"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="d8173-103">Bæta við nýrri síðu á svæði</span><span class="sxs-lookup"><span data-stu-id="d8173-103">Add a new site page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="d8173-104">Þetta efni lýsir því hvernig á að bæta við nýrri síðu svæðis í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d8173-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d8173-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="d8173-105">Overview</span></span>

<span data-ttu-id="d8173-106">Eftir að þú hefur búið til sniðmát og brot fyrir síðuna þína er næsta skref að byrja að búa til síður sem nota þau.</span><span class="sxs-lookup"><span data-stu-id="d8173-106">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="d8173-107">Til að byrja verður þú að velja sniðmát eða skipulag, nafn á síðu og slóð síðu.</span><span class="sxs-lookup"><span data-stu-id="d8173-107">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="d8173-108">Sniðmát eða útlit</span><span class="sxs-lookup"><span data-stu-id="d8173-108">Template or layout</span></span>

<span data-ttu-id="d8173-109">Þú getur annaðhvort notað sniðmát eða skipulag fyrir nýju síðuna þína.</span><span class="sxs-lookup"><span data-stu-id="d8173-109">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="d8173-110">Frekari upplýsingar eru í [Yfirlit yfir sniðmát og skipulag](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d8173-110">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="d8173-111">Heiti síðu</span><span class="sxs-lookup"><span data-stu-id="d8173-111">Page name</span></span>

<span data-ttu-id="d8173-112">Síðuheitið verður að vera einkvæmt fyrir síðuna.</span><span class="sxs-lookup"><span data-stu-id="d8173-112">The page name must be unique to your page.</span></span> <span data-ttu-id="d8173-113">Það ætti að vera lýsandi, svo að þú getur auðveldlega fundið það og aðrir vita fyrir hvað síðan stendur.</span><span class="sxs-lookup"><span data-stu-id="d8173-113">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="d8173-114">Veldu síðuheitið vandlega, því ekki er hægt að breyta því seinna.</span><span class="sxs-lookup"><span data-stu-id="d8173-114">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="d8173-115">Vefslóð síðu</span><span class="sxs-lookup"><span data-stu-id="d8173-115">Page URL</span></span>

<span data-ttu-id="d8173-116">Þú getur haft þann kost að slá inn slóð fyrir nýju síðuna.</span><span class="sxs-lookup"><span data-stu-id="d8173-116">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="d8173-117">Þegar þú býrð til síðu geturðu slegið inn streng sem verður notaður til að mynda heila vefslóð.</span><span class="sxs-lookup"><span data-stu-id="d8173-117">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="d8173-118">Þessi strengur er þekktur sem hlutfallsleg slóð eða slóðasnigill.</span><span class="sxs-lookup"><span data-stu-id="d8173-118">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="d8173-119">Síðan er stofnuð heil vefslóð byggt á slóðarsniglinum og nýju síðunni er úthlutað á hana.</span><span class="sxs-lookup"><span data-stu-id="d8173-119">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="d8173-120">Þú getur breytt slóðarsnigli seinna áður en þú birtir síðuna.</span><span class="sxs-lookup"><span data-stu-id="d8173-120">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="d8173-121">Nánari upplýsingar sjá [Stofna vefslóð síðu](create-page-URL.md).</span><span class="sxs-lookup"><span data-stu-id="d8173-121">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="d8173-122">Dynamics 365 Commerce aftengir slóðir og innihald.</span><span class="sxs-lookup"><span data-stu-id="d8173-122">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="d8173-123">Með öðrum orðum er hægt að búa til síðu sem er ekki tengd vefslóð og hægt er að búa til slóð sem er ekki tengd síðu.</span><span class="sxs-lookup"><span data-stu-id="d8173-123">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="d8173-124">Þess vegna er hægt að skipta um innihald fyrir slóð og engan niðritíma þarf og því er auðveldara að stjórna framsendingum.</span><span class="sxs-lookup"><span data-stu-id="d8173-124">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="d8173-125">Bæta við nýrri síðu</span><span class="sxs-lookup"><span data-stu-id="d8173-125">Add a new page</span></span>

<span data-ttu-id="d8173-126">Fylgdu þessum skrefum til að bæta við nýrri síðu á síðuna þína.</span><span class="sxs-lookup"><span data-stu-id="d8173-126">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="d8173-127">Undir **Svæði** velurðu **Fabrikam** (eða heiti svæðisins).</span><span class="sxs-lookup"><span data-stu-id="d8173-127">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="d8173-128">Veljið **Ný síða**.</span><span class="sxs-lookup"><span data-stu-id="d8173-128">Select **New Page**.</span></span>
1. <span data-ttu-id="d8173-129">Í svarglugganum **Ný síða** skal velja sniðmát og síðan smella á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d8173-129">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="d8173-130">Í reitnum **Heiti síðu** slærðu inn heiti síðunnar (til dæmis, **Nýja síða mín**).</span><span class="sxs-lookup"><span data-stu-id="d8173-130">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="d8173-131">Í reitinumm **Vefslóð** slærðu inn streng (slóðarsnigil) til að ljúka slóðinni (t.d. **myndsíða**).</span><span class="sxs-lookup"><span data-stu-id="d8173-131">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="d8173-132">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d8173-132">Select **OK**.</span></span> <span data-ttu-id="d8173-133">Síðuritillinn birtist.</span><span class="sxs-lookup"><span data-stu-id="d8173-133">The page editor appears.</span></span> <span data-ttu-id="d8173-134">Taktu eftir að fyrirsögn og undirmálstexta er sjálfkrafa bætt við síðuna, byggt á sniðmátinu sem þú valdir.</span><span class="sxs-lookup"><span data-stu-id="d8173-134">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="d8173-135">Í síðuútlínunum velurðu hólfið **Aðal**, velur úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="d8173-135">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d8173-136">Veldu **Gámur** og síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d8173-136">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="d8173-137">Veldu **Vökvagámur**, veldu úrfellingarhnappinn og veldu síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="d8173-137">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="d8173-138">Veldu **Bálkur með fjölbreyttu efni** og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d8173-138">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="d8173-139">Veldu **Bálk með fjölbreyttu efni**, veldu úrfellingarhnappinn og veldu síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="d8173-139">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="d8173-140">Veldu **Bálkaliður með fjölbreyttu efni** og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d8173-140">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="d8173-141">Í eiginleikaglugganum til hægri velurðu **Málsgrein** og slærð síðan inn í reitinn **Prufuextinn minn**.</span><span class="sxs-lookup"><span data-stu-id="d8173-141">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="d8173-142">Veldu **Vista** og síðan **Skrá inn**.</span><span class="sxs-lookup"><span data-stu-id="d8173-142">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="d8173-143">Í reitnum **Athugasemdir** slærðu inn **Bætti við nýrri síðu** og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d8173-143">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="d8173-144">Veldu **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="d8173-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="d8173-145">Þegar þú hefur lokið því skaltu loka forskoðunarflipanum til að fara aftur í höfundatólið.</span><span class="sxs-lookup"><span data-stu-id="d8173-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="d8173-146">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="d8173-146">Select **Publish**.</span></span>
1. <span data-ttu-id="d8173-147">Veldu á leiðsöguslóðina (brauðmylsna) **Fabrikam** (eða nafn vefsvæðisins).</span><span class="sxs-lookup"><span data-stu-id="d8173-147">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="d8173-148">Í stýriglugganum vinstra megin velurðu **Vefslóðir**.</span><span class="sxs-lookup"><span data-stu-id="d8173-148">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="d8173-149">Finndu og veldu slóðina (**mynewpage**) af listanum.</span><span class="sxs-lookup"><span data-stu-id="d8173-149">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="d8173-150">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="d8173-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d8173-151">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d8173-151">Additional resources</span></span>

[<span data-ttu-id="d8173-152">Breyta síðu svæðis sem þegar er til</span><span class="sxs-lookup"><span data-stu-id="d8173-152">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="d8173-153">Velja síðuútlit</span><span class="sxs-lookup"><span data-stu-id="d8173-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="d8173-154">Stjórna SEO-lýsigögnum</span><span class="sxs-lookup"><span data-stu-id="d8173-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="d8173-155">Vista, forskoða og birta síðu</span><span class="sxs-lookup"><span data-stu-id="d8173-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="d8173-156">Bæta vörusíðu</span><span class="sxs-lookup"><span data-stu-id="d8173-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="d8173-157">Bæta lendingarsíðu flokks</span><span class="sxs-lookup"><span data-stu-id="d8173-157">Enrich a category landing page</span></span>](enrich-category-page.md)

