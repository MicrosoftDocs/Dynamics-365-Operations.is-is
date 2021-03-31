---
title: Búa til gagnvirkar síður fyrir rafræn viðskipti sem byggja á færibreytum vefslóða
description: Þetta efnisatriði lýsir því hvernig setja á upp Microsoft Dynamics 365 Commerce-síðu rafrænna viðskipta sem getur þjónað gagnvirku efni, byggt á færibreytum vefslóða.
author: StuHarg
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8d6b4756fc81dc99786da251d5d9a575a71ccc49
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208016"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a><span data-ttu-id="055dd-103">Búa til gagnvirkar síður fyrir rafræn viðskipti sem byggja á færibreytum vefslóða</span><span class="sxs-lookup"><span data-stu-id="055dd-103">Create dynamic e-commerce pages based on URL parameters</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="055dd-104">Þetta efnisatriði lýsir því hvernig setja á upp Microsoft Dynamics 365 Commerce-síðu rafrænna viðskipta sem getur þjónað gagnvirku efni, byggt á færibreytum vefslóða.</span><span class="sxs-lookup"><span data-stu-id="055dd-104">This topic describes how to set up a Microsoft Dynamics 365 Commerce e-commerce page that can serve dynamic content, based on URL parameters.</span></span>

<span data-ttu-id="055dd-105">Hægt er að stilla síður rafrænna viðskipta til að þjóna mismunandi efni byggt á hluta vefslóðar.</span><span class="sxs-lookup"><span data-stu-id="055dd-105">An e-commerce page can be configured to serve different content, based on a segment in the URL path.</span></span> <span data-ttu-id="055dd-106">Þess vegna er síðan þekkt sem gagnvirk síða.</span><span class="sxs-lookup"><span data-stu-id="055dd-106">Therefore, the page is known as a dynamic page.</span></span> <span data-ttu-id="055dd-107">Hlutinn er notaður sem færibreyta til að sækja efni síðunnar.</span><span class="sxs-lookup"><span data-stu-id="055dd-107">The segment is used as a parameter to retrieve the page content.</span></span> <span data-ttu-id="055dd-108">Til dæmis er síða sem heitir **blogg\_yfirlit** stofnuð og tengd við vefslóðina `https://fabrikam.com/blog`.</span><span class="sxs-lookup"><span data-stu-id="055dd-108">For example, a page that is named **blog\_viewer** is created and associated with the URL `https://fabrikam.com/blog`.</span></span> <span data-ttu-id="055dd-109">Síðan er hægt að nota þessa síðu til að sýna mismunandi efni byggt á síðasta hlutanum vefslóðinni.</span><span class="sxs-lookup"><span data-stu-id="055dd-109">This page can then be used to show different content, based on the last segment in the URL path.</span></span> <span data-ttu-id="055dd-110">Til dæmis er síðasti hlutinn í vefslóð `https://fabrikam.com/blog/article-1` **article-1**.</span><span class="sxs-lookup"><span data-stu-id="055dd-110">For example, the last segment in the URL `https://fabrikam.com/blog/article-1` is **article-1**.</span></span>

<span data-ttu-id="055dd-111">Aðskildar sérsniðnar síður sem hnekkja gagnvirku síðunni geta einnig verið tengdar við hluta í vefslóðinni.</span><span class="sxs-lookup"><span data-stu-id="055dd-111">Separate custom pages that override the dynamic page can also be associated with segments in the URL path.</span></span> <span data-ttu-id="055dd-112">Til dæmis er síða sem heitir **blogg\_samantekt** stofnuð og tengd við vefslóðina `https://fabrikam.com/blog/about-this-blog`.</span><span class="sxs-lookup"><span data-stu-id="055dd-112">For example, a page that is named **blog\_summary** is created and associated with the URL `https://fabrikam.com/blog/about-this-blog`.</span></span> <span data-ttu-id="055dd-113">Þegar beðið er um þessa vefslóð kemur upp síðan **blogg\_samantekt** sem tengist færibreytunni **/about-this-blog** í staðinn fyrir síðuna **blogg\_yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="055dd-113">When this URL is requested, the **blog\_summary** page that is associated with the **/about-this-blog** parameter is returned instead of the **blog\_viewer** page.</span></span>

> [!NOTE]
> <span data-ttu-id="055dd-114">Virknin til að hýsa, sækja og sýna efni gagnvirkrar síðu er innleidd með því að nota sérsniðna einingu.</span><span class="sxs-lookup"><span data-stu-id="055dd-114">The functionality for hosting, retrieving, and showing dynamic page content is implemented by using a custom module.</span></span> <span data-ttu-id="055dd-115">Frekari upplýsingar er að finna í [Stækkunarhæfni rásar á netinu](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="055dd-115">For more information, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="set-up-a-dynamic-e-commerce-page"></a><span data-ttu-id="055dd-116">Setja upp gagnvirka síðu fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="055dd-116">Set up a dynamic e-commerce page</span></span>

<span data-ttu-id="055dd-117">Til að setja upp gagnvirka síðu fyrir rafræn viðskipti þarf að búa til gagnvirku síðuna, búa til grunnvefslóðina og skilgreina leiðina á gagnvirku síðuna.</span><span class="sxs-lookup"><span data-stu-id="055dd-117">To set up a dynamic e-commerce page, you must create the dynamic page, create the base URL, and configure the route to the dynamic page.</span></span>

### <a name="create-the-page-that-will-serve-dynamic-content"></a><span data-ttu-id="055dd-118">Búa til síðu sem þjónar gagnvirku efni</span><span class="sxs-lookup"><span data-stu-id="055dd-118">Create the page that will serve dynamic content</span></span>

<span data-ttu-id="055dd-119">Til að búa til síðu sem mun þjóna gagnvirku efni skal fylgja þessum skrefum í [Bæta við nýrri síðu á svæði](add-new-page.md).</span><span class="sxs-lookup"><span data-stu-id="055dd-119">To create a page that will serve dynamic content, follow the steps in [Add a new site page](add-new-page.md).</span></span> <span data-ttu-id="055dd-120">Síðan sem stofnuð er þarf innleiðingu einingar sem notar síðasta hlutann í vefslóð til að sækja efni frá ytri gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="055dd-120">The page that you create will require implementation of a module that uses the last segment in the URL path to retrieve content from an external data source.</span></span> <span data-ttu-id="055dd-121">Frekari upplýsingar um sérsniðna þróun einingar er að finna í [Stækkunarhæfni rásar á netinu](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="055dd-121">For more information about custom module development, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

### <a name="create-the-base-url-for-the-dynamic-page"></a><span data-ttu-id="055dd-122">Stofna grunnvefslóð fyrir gagnvirka síðu</span><span class="sxs-lookup"><span data-stu-id="055dd-122">Create the base URL for the dynamic page</span></span>

<span data-ttu-id="055dd-123">Til að stofna grunnvefslóð fyrir gagnvirka síðu í Commerce-vefsmið skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="055dd-123">To create the base URL for the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="055dd-124">Farið í **Vefslóðir** og veljið **Ný \> Ný vefslóð**.</span><span class="sxs-lookup"><span data-stu-id="055dd-124">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="055dd-125">Í svarglugganum **Stofna nýja vefslóð** skal velja **Innri síða**.</span><span class="sxs-lookup"><span data-stu-id="055dd-125">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="055dd-126">Undir **Vefslóð** skal færa inn vefslóðina sem mun þjóna hlutverki leiðar fyrir gagnvirku síðuna (í þessu dæmi **/blog**).</span><span class="sxs-lookup"><span data-stu-id="055dd-126">Under **URL path**, enter the path that will serve as the root for the dynamic page (in this example, **/blog**).</span></span> <span data-ttu-id="055dd-127">Veljið síðan **Næst**.</span><span class="sxs-lookup"><span data-stu-id="055dd-127">Then select **Next**.</span></span>
1. <span data-ttu-id="055dd-128">Í svarglugganum **Velja síðu** skal velja síðuna sem var stofnuð til að þjóna hlutverki gagnvirku síðunnar og síðan velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="055dd-128">In the **Select a page** dialog box, select the page that you created to serve as the dynamic page, and then select **Save**.</span></span>
1. <span data-ttu-id="055dd-129">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="055dd-129">Select **Publish**.</span></span>

### <a name="configure-the-route-to-the-dynamic-page"></a><span data-ttu-id="055dd-130">Skilgreina leiðina á gagnvirka síðu</span><span class="sxs-lookup"><span data-stu-id="055dd-130">Configure the route to the dynamic page</span></span>

<span data-ttu-id="055dd-131">Til að skilgreina leiðina á gagnvirka síðu í Commerce-vefsmið skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="055dd-131">To configure the route to the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="055dd-132">Farið í **Svæðisstillingar \> Viðbætur**.</span><span class="sxs-lookup"><span data-stu-id="055dd-132">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="055dd-133">Undir **Færibreytustilltar vefslóðir** skal velja **Bæta við** og síðan færa inn vefslóðina sem slegin var inn þegar vefslóðin var búin til (í þessu dæmi **/blog**).</span><span class="sxs-lookup"><span data-stu-id="055dd-133">Under **Parameterized URL paths**, select **Add**, and then enter the URL path that you entered when you created the URL (in this example, **/blog**).</span></span>
1. <span data-ttu-id="055dd-134">Veljið **Vista og birta**.</span><span class="sxs-lookup"><span data-stu-id="055dd-134">Select **Save and publish**.</span></span>

<span data-ttu-id="055dd-135">Þegar leiðin er skilgreind munu allar beiðnir til færibreytustilltu vefslóðarinnar skila síðunni sem tengist þeirri vefslóð.</span><span class="sxs-lookup"><span data-stu-id="055dd-135">After the route is configured, all requests to the parameterized URL path will return the page that is associated with that URL.</span></span> <span data-ttu-id="055dd-136">Ef einhver beiðni inniheldur viðbótarhluta verður tengdri síðu skilað og efni síðunnar verður sótt með því að nota hlutann sem færibreytu.</span><span class="sxs-lookup"><span data-stu-id="055dd-136">If any requests contain an additional segment, the associated page will be returned, and the page content will be retrieved by using the segment as a parameter.</span></span> <span data-ttu-id="055dd-137">Til dæmis mun `https://fabrikam.com/blog/article-1` skila síðunni **blogg\_samantekt** og efni síðunnar verður sótt með því að nota færibreytuna **/article-1**.</span><span class="sxs-lookup"><span data-stu-id="055dd-137">For example, `https://fabrikam.com/blog/article-1` will return the **blog\_summary** page, and the page content will be retrieved by using the **/article-1** parameter.</span></span>

## <a name="override-a-parameterized-url-with-a-custom-page"></a><span data-ttu-id="055dd-138">Hnekkja færibreytustilltri vefslóð með sérsniðinni síðu</span><span class="sxs-lookup"><span data-stu-id="055dd-138">Override a parameterized URL with a custom page</span></span>

<span data-ttu-id="055dd-139">Til að hnekkja færibreytustilltri vefslóð með sérsniðinni síðu í Commerce-vefsmið skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="055dd-139">To override a parameterized URL with a custom page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="055dd-140">Farið í **Vefslóðir** og veljið **Ný \> Ný vefslóð**.</span><span class="sxs-lookup"><span data-stu-id="055dd-140">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="055dd-141">Í svarglugganum **Stofna nýja vefslóð** skal velja **Innri síða**.</span><span class="sxs-lookup"><span data-stu-id="055dd-141">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="055dd-142">Undir **Vefslóð** skal færa inn vefslóðin sem inniheldur hlutann sem á að hnekkja (í þessu dæmi **/blog/about-this-blog**).</span><span class="sxs-lookup"><span data-stu-id="055dd-142">Under **URL path**, enter the path that includes the segment to override (in this example, **/blog/about-this-blog**).</span></span> <span data-ttu-id="055dd-143">Veljið síðan **Næst**.</span><span class="sxs-lookup"><span data-stu-id="055dd-143">Then select **Next**.</span></span>
1. <span data-ttu-id="055dd-144">Í svarglugganum **Velja síðu** skal velja sérsniðnu síðuna og síðan velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="055dd-144">In the **Select a page** dialog box, select the custom page, and then select **Save**.</span></span>
1. <span data-ttu-id="055dd-145">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="055dd-145">Select **Publish**.</span></span>
1. <span data-ttu-id="055dd-146">Ef sérsniðna síðan hefur ekki enn verið birt skal fara í **Síður**, velja sérsniðna síðu og síðan velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="055dd-146">If the custom page hasn't yet been published, go to **Pages**, select the custom page, and then select **Publish**.</span></span>

<span data-ttu-id="055dd-147">Þegar sérsniðna síðan hefur verið birt verður hún gefin upp í staðinn fyrir gagnvirku síðuna sem er með færibreytustillt efni.</span><span class="sxs-lookup"><span data-stu-id="055dd-147">After the custom page is published, it will be served instead of the dynamic page that has parameterized content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="055dd-148">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="055dd-148">Additional resources</span></span>

[<span data-ttu-id="055dd-149">Breyta síðu svæðis sem þegar er til</span><span class="sxs-lookup"><span data-stu-id="055dd-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="055dd-150">Bæta við nýrri síðu á svæði</span><span class="sxs-lookup"><span data-stu-id="055dd-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="055dd-151">Velja síðuútlit</span><span class="sxs-lookup"><span data-stu-id="055dd-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="055dd-152">Stjórna SEO-lýsigögnum</span><span class="sxs-lookup"><span data-stu-id="055dd-152">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="055dd-153">Vista, forskoða og birta síðu</span><span class="sxs-lookup"><span data-stu-id="055dd-153">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="055dd-154">Bæta vörusíðu</span><span class="sxs-lookup"><span data-stu-id="055dd-154">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="055dd-155">Bæta lendingarsíðu flokks</span><span class="sxs-lookup"><span data-stu-id="055dd-155">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="055dd-156">Staðfesta aðgengi að efni síðu</span><span class="sxs-lookup"><span data-stu-id="055dd-156">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="055dd-157">Stækkunarhæfni netrásar</span><span class="sxs-lookup"><span data-stu-id="055dd-157">Online channel extensibility</span></span>](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]