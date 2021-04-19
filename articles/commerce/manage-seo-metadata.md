---
title: Stjórna SEO-lýsigögnum
description: Þetta efnisatriði lýsir því hvernig á að stjórna lýsigögnum leitarvélabestunar í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 1e03ef346df92a94b0a403f241d0f7d1f64fd210
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794212"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="4e386-103">Stjórna SEO-lýsigögnum</span><span class="sxs-lookup"><span data-stu-id="4e386-103">Manage SEO metadata</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4e386-104">Þetta efnisatriði lýsir því hvernig á að stjórna lýsigögnum leitarvélabestunar í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4e386-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4e386-105">Hægt er að stjórna SEO lýsigögnum fyrir síðu með því að nota svæðiskort og lýsigögn síðna.</span><span class="sxs-lookup"><span data-stu-id="4e386-105">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="4e386-106">Svæðiskort</span><span class="sxs-lookup"><span data-stu-id="4e386-106">Site maps</span></span>

<span data-ttu-id="4e386-107">Vefkort er vélalæsilegur listi, á XML sniði, af síðunum á vefsíðunni þinni.</span><span class="sxs-lookup"><span data-stu-id="4e386-107">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="4e386-108">Það er ætlað að notkunar leitarvéla, svo að þær geti veitt betri leitarniðurstöður frá vefsvæðinu þínu.</span><span class="sxs-lookup"><span data-stu-id="4e386-108">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="4e386-109">Leitarvélar geta tekið vefkort upp handvirkt eða gefa út í robots.txt skrá.</span><span class="sxs-lookup"><span data-stu-id="4e386-109">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="4e386-110">Dynamics 365 Commerce styður sjálfvirka myndun á vefkortum.</span><span class="sxs-lookup"><span data-stu-id="4e386-110">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="4e386-111">Vefkort eru uppfærð sjálfkrafa þegar síður eru birtar og óbirtar.</span><span class="sxs-lookup"><span data-stu-id="4e386-111">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="4e386-112">Kveiktu á myndun vefkorts</span><span class="sxs-lookup"><span data-stu-id="4e386-112">Turn on site map generation</span></span>

1. <span data-ttu-id="4e386-113">Skráðu þig inn á höfundatólið.</span><span class="sxs-lookup"><span data-stu-id="4e386-113">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="4e386-114">Undir **Svæði** velurðu **Fabrikam** (eða heiti svæðisins).</span><span class="sxs-lookup"><span data-stu-id="4e386-114">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="4e386-115">Í stýriglugganum vinstra megin velurðu **Svæðisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="4e386-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="4e386-116">Gakktu úr skugga um að kveikt sé á valkostinum **Vefkort virkjuð**.</span><span class="sxs-lookup"><span data-stu-id="4e386-116">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="4e386-117">Lýsigögn síðu</span><span class="sxs-lookup"><span data-stu-id="4e386-117">Page metadata</span></span>

<span data-ttu-id="4e386-118">Dynamics 365 Commerce gerir þér kleift að stjórna lýsigögnum SEO fyrir einstakar síður.</span><span class="sxs-lookup"><span data-stu-id="4e386-118">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="4e386-119">Þú getur skoðað og breytt þessum upplýsingum í hlutanum **SEO eiginleikar** í síðugámi.</span><span class="sxs-lookup"><span data-stu-id="4e386-119">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="4e386-120">Eftirfarandi lýsigagnaeiginleikar SEO eru studdir:</span><span class="sxs-lookup"><span data-stu-id="4e386-120">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="4e386-121">Titill</span><span class="sxs-lookup"><span data-stu-id="4e386-121">Title</span></span>
- <span data-ttu-id="4e386-122">Lýsing</span><span class="sxs-lookup"><span data-stu-id="4e386-122">Description</span></span>
- <span data-ttu-id="4e386-123">SEO lykilorð</span><span class="sxs-lookup"><span data-stu-id="4e386-123">SEO keywords</span></span>
- <span data-ttu-id="4e386-124">Aria merki</span><span class="sxs-lookup"><span data-stu-id="4e386-124">Aria labels</span></span>
- <span data-ttu-id="4e386-125">noindex</span><span class="sxs-lookup"><span data-stu-id="4e386-125">noindex</span></span>
- <span data-ttu-id="4e386-126">nofollow</span><span class="sxs-lookup"><span data-stu-id="4e386-126">nofollow</span></span>
- <span data-ttu-id="4e386-127">noarchive</span><span class="sxs-lookup"><span data-stu-id="4e386-127">noarchive</span></span>
- <span data-ttu-id="4e386-128">nocache</span><span class="sxs-lookup"><span data-stu-id="4e386-128">nocache</span></span>
- <span data-ttu-id="4e386-129">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="4e386-129">noOpenDirectoryProject</span></span>
- <span data-ttu-id="4e386-130">nosnippet</span><span class="sxs-lookup"><span data-stu-id="4e386-130">nosnippet</span></span>
- <span data-ttu-id="4e386-131">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="4e386-131">noImageIndex</span></span>
- <span data-ttu-id="4e386-132">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="4e386-132">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="4e386-133">Breyta lýsigögnum síðna</span><span class="sxs-lookup"><span data-stu-id="4e386-133">Modify page metadata</span></span>

<span data-ttu-id="4e386-134">Til að breyta lýsigögnum síðu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="4e386-134">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="4e386-135">Undir **Svæði** velurðu **Fabrikam** (eða heiti svæðisins).</span><span class="sxs-lookup"><span data-stu-id="4e386-135">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="4e386-136">Í stýriglugganum vinstra megin velurðu **Síður**.</span><span class="sxs-lookup"><span data-stu-id="4e386-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="4e386-137">Veldu heimasíðuna til að opna hana í ritlinum.</span><span class="sxs-lookup"><span data-stu-id="4e386-137">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="4e386-138">Á skipanastikunni velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="4e386-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="4e386-139">Í eiginleikaglugganum til hægri stækkarðu **Sjálfgild lýsimerki**.</span><span class="sxs-lookup"><span data-stu-id="4e386-139">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="4e386-140">Til að bæta við nýju lýsimerki **Bæta við** og sláðu síðan inn merkið í reitinn.</span><span class="sxs-lookup"><span data-stu-id="4e386-140">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="4e386-141">Til að fjarlægja fyrirliggjandi lýsimerki velurðu ruslatunnutáknið hægra megin við það.</span><span class="sxs-lookup"><span data-stu-id="4e386-141">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="4e386-142">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="4e386-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="4e386-143">Í reitnum **Athugasemdir** slærðu inn **Uppfærð lýsimerki** og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4e386-143">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="4e386-144">Veldu **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="4e386-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="4e386-145">Þegar þú hefur lokið því skaltu loka forskoðunarflipanum til að fara aftur í höfundatólið.</span><span class="sxs-lookup"><span data-stu-id="4e386-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="4e386-146">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="4e386-146">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e386-147">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4e386-147">Additional resources</span></span>

[<span data-ttu-id="4e386-148">Breyta síðu svæðis sem þegar er til</span><span class="sxs-lookup"><span data-stu-id="4e386-148">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="4e386-149">Bæta við nýrri síðu á svæði</span><span class="sxs-lookup"><span data-stu-id="4e386-149">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="4e386-150">Velja síðuútlit</span><span class="sxs-lookup"><span data-stu-id="4e386-150">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="4e386-151">Vista, forskoða og birta síðu</span><span class="sxs-lookup"><span data-stu-id="4e386-151">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="4e386-152">Bæta vörusíðu</span><span class="sxs-lookup"><span data-stu-id="4e386-152">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="4e386-153">Bæta lendingarsíðu flokks</span><span class="sxs-lookup"><span data-stu-id="4e386-153">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="4e386-154">Staðfesta aðgengi að efni síðu</span><span class="sxs-lookup"><span data-stu-id="4e386-154">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="4e386-155">Búa til gagnvirkar síður fyrir rafræn viðskipti sem byggja á færibreytum vefslóða</span><span class="sxs-lookup"><span data-stu-id="4e386-155">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
