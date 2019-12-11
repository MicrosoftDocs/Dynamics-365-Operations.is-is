---
title: Stjórna SEO-lýsigögnum
description: Þetta efnisatriði lýsir því hvernig hægt er að stjórna lýsigögnum um SEO (SEO) í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: b69d9d2769023967e2b94fef1b8fcf6b5b3357c5
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698350"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="26641-103">Stjórna SEO-lýsigögnum</span><span class="sxs-lookup"><span data-stu-id="26641-103">Manage SEO metadata</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="26641-104">Þetta efnisatriði lýsir því hvernig hægt er að stjórna lýsigögnum um SEO (SEO) í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="26641-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="26641-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="26641-105">Overview</span></span>

<span data-ttu-id="26641-106">Hægt er að stjórna SEO lýsigögnum fyrir síðu með því að nota svæðiskort og lýsigögn síðna.</span><span class="sxs-lookup"><span data-stu-id="26641-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="26641-107">Svæðiskort</span><span class="sxs-lookup"><span data-stu-id="26641-107">Site maps</span></span>

<span data-ttu-id="26641-108">Vefkort er vélalæsilegur listi, á XML sniði, af síðunum á vefsíðunni þinni.</span><span class="sxs-lookup"><span data-stu-id="26641-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="26641-109">Það er ætlað að notkunar leitarvéla, svo að þær geti veitt betri leitarniðurstöður frá vefsvæðinu þínu.</span><span class="sxs-lookup"><span data-stu-id="26641-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="26641-110">Leitarvélar geta tekið vefkort upp handvirkt eða gefa út í robots.txt skrá.</span><span class="sxs-lookup"><span data-stu-id="26641-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="26641-111">Dynamics 365 Commerce styður sjálfvirka myndun á vefkortum.</span><span class="sxs-lookup"><span data-stu-id="26641-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="26641-112">Vefkort eru uppfærð sjálfkrafa þegar síður eru birtar og óbirtar.</span><span class="sxs-lookup"><span data-stu-id="26641-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="26641-113">Kveiktu á myndun vefkorts</span><span class="sxs-lookup"><span data-stu-id="26641-113">Turn on site map generation</span></span>

1. <span data-ttu-id="26641-114">Skráðu þig inn á höfundatólið.</span><span class="sxs-lookup"><span data-stu-id="26641-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="26641-115">Undir **Svæði** velurðu **Fabrikam** (eða heiti svæðisins).</span><span class="sxs-lookup"><span data-stu-id="26641-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="26641-116">Í stýriglugganum vinstra megin velurðu **Svæðisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="26641-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="26641-117">Gakktu úr skugga um að kveikt sé á valkostinum **Vefkort virkjuð**.</span><span class="sxs-lookup"><span data-stu-id="26641-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="26641-118">Lýsigögn síðu</span><span class="sxs-lookup"><span data-stu-id="26641-118">Page metadata</span></span>

<span data-ttu-id="26641-119">Dynamics 365 Commerce gerir þér kleift að stjórna lýsigögnum SEO fyrir einstakar síður.</span><span class="sxs-lookup"><span data-stu-id="26641-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="26641-120">Þú getur skoðað og breytt þessum upplýsingum í hlutanum **SEO eiginleikar** í síðugámi.</span><span class="sxs-lookup"><span data-stu-id="26641-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="26641-121">Eftirfarandi lýsigagnaeiginleikar SEO eru studdir:</span><span class="sxs-lookup"><span data-stu-id="26641-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="26641-122">Titill</span><span class="sxs-lookup"><span data-stu-id="26641-122">Title</span></span>
- <span data-ttu-id="26641-123">Lýsing</span><span class="sxs-lookup"><span data-stu-id="26641-123">Description</span></span>
- <span data-ttu-id="26641-124">SEO lykilorð</span><span class="sxs-lookup"><span data-stu-id="26641-124">SEO keywords</span></span>
- <span data-ttu-id="26641-125">Aria merki</span><span class="sxs-lookup"><span data-stu-id="26641-125">Aria labels</span></span>
- <span data-ttu-id="26641-126">noindex</span><span class="sxs-lookup"><span data-stu-id="26641-126">noindex</span></span>
- <span data-ttu-id="26641-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="26641-127">nofollow</span></span>
- <span data-ttu-id="26641-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="26641-128">noarchive</span></span>
- <span data-ttu-id="26641-129">nocache</span><span class="sxs-lookup"><span data-stu-id="26641-129">nocache</span></span>
- <span data-ttu-id="26641-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="26641-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="26641-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="26641-131">nosnippet</span></span>
- <span data-ttu-id="26641-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="26641-132">noImageIndex</span></span>
- <span data-ttu-id="26641-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="26641-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="26641-134">Breyta lýsigögnum síðna</span><span class="sxs-lookup"><span data-stu-id="26641-134">Modify page metadata</span></span>

<span data-ttu-id="26641-135">Til að breyta lýsigögnum síðu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="26641-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="26641-136">Undir **Svæði** velurðu **Fabrikam** (eða heiti svæðisins).</span><span class="sxs-lookup"><span data-stu-id="26641-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="26641-137">Í stýriglugganum vinstra megin velurðu **Síður**.</span><span class="sxs-lookup"><span data-stu-id="26641-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="26641-138">Veldu heimasíðuna til að opna hana í ritlinum.</span><span class="sxs-lookup"><span data-stu-id="26641-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="26641-139">Í aðgerðasvæðinu velurðu **Skrá út**.</span><span class="sxs-lookup"><span data-stu-id="26641-139">On the Action Pane, select **Check Out**.</span></span>
1. <span data-ttu-id="26641-140">Í eiginleikaglugganum til hægri stækkarðu **Sjálfgild lýsimerki**.</span><span class="sxs-lookup"><span data-stu-id="26641-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="26641-141">Til að bæta við nýju lýsimerki **Bæta við** og sláðu síðan inn merkið í reitinn.</span><span class="sxs-lookup"><span data-stu-id="26641-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span>

    <span data-ttu-id="26641-142">Til að fjarlægja fyrirliggjandi lýsimerki velurðu ruslatunnutáknið hægra megin við það.</span><span class="sxs-lookup"><span data-stu-id="26641-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>

1. <span data-ttu-id="26641-143">Veldu **Vista** og síðan **Skrá inn**.</span><span class="sxs-lookup"><span data-stu-id="26641-143">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="26641-144">Í reitnum **Athugasemdir** slærðu inn **Uppfærð lýsimerki** og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="26641-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="26641-145">Veldu **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="26641-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="26641-146">Þegar þú hefur lokið því skaltu loka forskoðunarflipanum til að fara aftur í höfundatólið.</span><span class="sxs-lookup"><span data-stu-id="26641-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="26641-147">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="26641-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26641-148">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="26641-148">Additional resources</span></span>

[<span data-ttu-id="26641-149">Breyta síðu svæðis sem þegar er til</span><span class="sxs-lookup"><span data-stu-id="26641-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="26641-150">Bæta við nýrri síðu á svæði</span><span class="sxs-lookup"><span data-stu-id="26641-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="26641-151">Velja síðuútlit</span><span class="sxs-lookup"><span data-stu-id="26641-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="26641-152">Vista, forskoða og birta síðu</span><span class="sxs-lookup"><span data-stu-id="26641-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="26641-153">Bæta vörusíðu</span><span class="sxs-lookup"><span data-stu-id="26641-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="26641-154">Bæta lendingarsíðu flokks</span><span class="sxs-lookup"><span data-stu-id="26641-154">Enrich a category landing page</span></span>](enrich-category-page.md)

