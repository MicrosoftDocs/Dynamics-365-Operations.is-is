---
title: Skilgreina einkunnir og umsagnir
description: Þetta efni lýsir því hvernig á að stilla netverslunarsíðuna þína til að sýna viðskiptavini mat og umsagnir í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
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
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0aac4b680590a95f465d33950f2933c4a4582e54
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002198"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="8f1de-103">Skilgreina einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="8f1de-103">Configure ratings and reviews</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="8f1de-104">Þetta efni lýsir því hvernig á að stilla netverslunarsíðuna þína til að sýna viðskiptavini mat og umsagnir í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8f1de-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8f1de-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="8f1de-105">Overview</span></span>

<span data-ttu-id="8f1de-106">Mat og umsagnir á vefsíðum um netverslun hjálpa viðskiptavinum að fræðast um vörur áður en þeir taka kaupákvörðun með því að sýna þeim hvað öðrum viðskiptavinum finnst um þessar vörur.</span><span class="sxs-lookup"><span data-stu-id="8f1de-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, by showing them what other customers think about those products.</span></span> <span data-ttu-id="8f1de-107">Fyrir vefsíður í netverslun eru einkunnir og umsagnir einnig búnaður til að safna endurgjöf viðskiptavina um vörur.</span><span class="sxs-lookup"><span data-stu-id="8f1de-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="8f1de-108">Einkunnir eru sýndar á vörulistasíðum, flokkalistasíðum, leitarniðurstöðusíðum og öðrum vefsíðum.</span><span class="sxs-lookup"><span data-stu-id="8f1de-108">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> <span data-ttu-id="8f1de-109">Stuðlarit einkunna og afurðaumsagnir eru sýndar á upplýsingasíðum afurða (PDPs).</span><span class="sxs-lookup"><span data-stu-id="8f1de-109">Ratings histograms and product reviews are shown on product details pages (PDPs).</span></span> <span data-ttu-id="8f1de-110">Hnappurinn **Skrifa umsögn** gerir viðskiptavinum kleift að senda inn einkunnir og umsagnir um afurð.</span><span class="sxs-lookup"><span data-stu-id="8f1de-110">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="8f1de-111">Einkunna- og umsagnaeiningar á PDP</span><span class="sxs-lookup"><span data-stu-id="8f1de-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="8f1de-112">Þrjár einingar sýna yfirlit yfir mat og yfirlit yfir PDP:</span><span class="sxs-lookup"><span data-stu-id="8f1de-112">Three modules show the ratings and reviews summary on PDPs:</span></span>

- <span data-ttu-id="8f1de-113">Skrifa umsagnareiningu</span><span class="sxs-lookup"><span data-stu-id="8f1de-113">Write review module</span></span>
- <span data-ttu-id="8f1de-114">Eining umsagnalista afurðar</span><span class="sxs-lookup"><span data-stu-id="8f1de-114">Product reviews list module</span></span>
- <span data-ttu-id="8f1de-115">Stuðlaritseining einkunna</span><span class="sxs-lookup"><span data-stu-id="8f1de-115">Ratings histogram module</span></span>
 
<span data-ttu-id="8f1de-116">Eftirfarandi mynd sýnir hvernig einkunnirnar og umsagnirnar líta út á PDP.</span><span class="sxs-lookup"><span data-stu-id="8f1de-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Einkunna- og umsagnaeiningar á PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="8f1de-118">Fyrir upplýsingar um hvernig á að fínstilla PDP sniðmát og útlit svo að þú getir deilt stillingum fyrir einingar einkunna og umsagna meðal margra PDP á netverslunarvefsvæðinu, sjá [Yfirlit yfir sniðmát og útlit](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8f1de-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="8f1de-119">Eftirfarandi mynd sýnir hvernig glugginn **Bæta við einingu** birtir einingar einkunna og umsagna í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8f1de-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>

![Bættu við einingaglugga](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a><span data-ttu-id="8f1de-121">Skrifa umsagnareiningu</span><span class="sxs-lookup"><span data-stu-id="8f1de-121">Write review module</span></span>

<span data-ttu-id="8f1de-122">Í einingunni skrifa umsögn inniheldur hnappurinn **Skrifa umsögn** sem gerir notendum kleift að skrá sig inn, úthluta mati og skrifa umsögn um vöru.</span><span class="sxs-lookup"><span data-stu-id="8f1de-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="8f1de-123">Þessi eining gerir notendum einnig kleift að breyta einkunn eða umsögn sem þeir sendu inn áður.</span><span class="sxs-lookup"><span data-stu-id="8f1de-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="8f1de-124">Þessi eining birtist venjulega fyrir ofan einingarnar stuðlarit einkunna og lista yfir afurðaumsagnir á PDP.</span><span class="sxs-lookup"><span data-stu-id="8f1de-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>

<span data-ttu-id="8f1de-125">Eftirfarandi mynd sýnir valmyndina **Skrifa umsögn** sem birtist þegar viðskiptavinur velur **Skrifa umsögn**.</span><span class="sxs-lookup"><span data-stu-id="8f1de-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="8f1de-126">Viðskiptavinurinn getur notað þennan glugga til að leggja fram mat og umsögn.</span><span class="sxs-lookup"><span data-stu-id="8f1de-126">The customer can use this dialog box to submit a rating and a review.</span></span>

![Skrifaðu umsagnarglugga](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="8f1de-128">Eftirfarandi tafla sýnir eiginleikann fyrir eininguna skrifa umsögn sem þarf að stilla í höfundatólinu.</span><span class="sxs-lookup"><span data-stu-id="8f1de-128">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="8f1de-129">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="8f1de-129">Property name</span></span> | <span data-ttu-id="8f1de-130">Virði</span><span class="sxs-lookup"><span data-stu-id="8f1de-130">Value</span></span>        | <span data-ttu-id="8f1de-131">Lýsing á eiginleika</span><span class="sxs-lookup"><span data-stu-id="8f1de-131">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="8f1de-132">Nafn</span><span class="sxs-lookup"><span data-stu-id="8f1de-132">Name</span></span>          | <span data-ttu-id="8f1de-133">Skrifa umsögn</span><span class="sxs-lookup"><span data-stu-id="8f1de-133">Write review</span></span> | <span data-ttu-id="8f1de-134">Heiti einingarinnar skrifa umsögn.</span><span class="sxs-lookup"><span data-stu-id="8f1de-134">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="8f1de-135">Stuðlaritseining einkunna</span><span class="sxs-lookup"><span data-stu-id="8f1de-135">Ratings histogram module</span></span>

<span data-ttu-id="8f1de-136">Stuðlaritseining einkunna sýnir stuðlarit með einkunnum.</span><span class="sxs-lookup"><span data-stu-id="8f1de-136">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="8f1de-137">Þessi eining birtist venjulega á milli eininga skrifa umsagna og afurðaumsagnalistaeiningarinnar á PDP.</span><span class="sxs-lookup"><span data-stu-id="8f1de-137">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>

<span data-ttu-id="8f1de-138">Stuðlaritseining einkunna þarf enga skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="8f1de-138">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="8f1de-139">Þú þarft bara að bæta einingunni við í PDP sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="8f1de-139">You just have to add the module in the PDP template.</span></span> 

<span data-ttu-id="8f1de-140">Eftirfarandi myndir sýna hvernig PDP sniðmát lítur út í Dynamics 365 Commerce þegar einkunnir og umsagnaeiningar eru stilltar til birtingar á PDP.</span><span class="sxs-lookup"><span data-stu-id="8f1de-140">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>

![PDP sniðmát þegar einkunnir og umsagnir eru stilltar til birtingar á PDP](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a><span data-ttu-id="8f1de-142">Eining umsagnalista afurðar</span><span class="sxs-lookup"><span data-stu-id="8f1de-142">Product reviews list module</span></span>

<span data-ttu-id="8f1de-143">Einingin yfir vöruúttektarlista sýnir lista yfir afurðaumsagnir ásamt flokkunar-, síunar- og síðuskiptingarvalkostum.</span><span class="sxs-lookup"><span data-stu-id="8f1de-143">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="8f1de-144">Þessi eining birtist venjulega eftir stuðlaritseining einkunna á PDP.</span><span class="sxs-lookup"><span data-stu-id="8f1de-144">This module typically appears after the ratings histogram module on a PDP.</span></span>

<span data-ttu-id="8f1de-145">Eftirfarandi tafla sýnir eiginleika fyrir einingu yfir umsagnalista afurða sem þarf að stilla í höfundatólinu.</span><span class="sxs-lookup"><span data-stu-id="8f1de-145">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="8f1de-146">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="8f1de-146">Property name</span></span>              | <span data-ttu-id="8f1de-147">Virði</span><span class="sxs-lookup"><span data-stu-id="8f1de-147">Value</span></span> | <span data-ttu-id="8f1de-148">Lýsing á eiginleika</span><span class="sxs-lookup"><span data-stu-id="8f1de-148">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="8f1de-149">Umsagnir sýndar á síðu</span><span class="sxs-lookup"><span data-stu-id="8f1de-149">Reviews shown on each page</span></span> | <span data-ttu-id="8f1de-150">10</span><span class="sxs-lookup"><span data-stu-id="8f1de-150">10</span></span>    | <span data-ttu-id="8f1de-151">Fjöldi umsagna sem ætti að birtast í einu á PDP.</span><span class="sxs-lookup"><span data-stu-id="8f1de-151">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="8f1de-152">Hnapparnir **Næst** og **Fyrri** eru með, svo að notendur geti farið í gegnum umsagnasíðurnar.</span><span class="sxs-lookup"><span data-stu-id="8f1de-152">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="8f1de-153">Stuðlarit einkunna - Samantektaryfirlit</span><span class="sxs-lookup"><span data-stu-id="8f1de-153">Ratings histogram – Summary view</span></span>

<span data-ttu-id="8f1de-154">Einingin yfir afurðaumsagnalista inniheldur hólf þar sem þú getur bætt við stuðlaritseiningu einkunna.</span><span class="sxs-lookup"><span data-stu-id="8f1de-154">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="8f1de-155">Eftirfarandi mynd sýnir hvernig þú getur bætt við stuðlaritseiningu einkunna fyrir afurðaumsagnalista í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8f1de-155">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Bætir við stuðlaritseiningu einkunna í einingu afurðaumsagnalista](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="8f1de-157">Skilgreina svæði til að sýna einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="8f1de-157">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="8f1de-158">Stillingargildi fyrir einkunnir og umsagnir, svo sem auðkenni leigjanda, lengd textatexta og lengd endurskoðunar titils, eru stillt á vefsvæðisstig.</span><span class="sxs-lookup"><span data-stu-id="8f1de-158">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="8f1de-159">Fylgdu þessum skrefum til að stilla vefsíðu til að sýna einkunnir og umsagnir.</span><span class="sxs-lookup"><span data-stu-id="8f1de-159">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="8f1de-160">Fara til **Heim \> Svæði**.</span><span class="sxs-lookup"><span data-stu-id="8f1de-160">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="8f1de-161">Veldu heiti vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="8f1de-161">Select the name of your site.</span></span> 
1. <span data-ttu-id="8f1de-162">Farðu á **Svæðisstjórnun \> Stækkunarhæfni**.</span><span class="sxs-lookup"><span data-stu-id="8f1de-162">Go to **Site management \> Extensibility**.</span></span> 
1. <span data-ttu-id="8f1de-163">Í reitinn **Hámarkstextalengd umsagnar** slærðu inn hámarksfjölda stafa sem umsagnartexti getur haft (t.d. **1000**).</span><span class="sxs-lookup"><span data-stu-id="8f1de-163">In the **Review Text Max Length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="8f1de-164">Í reitinn **Hámarkstitillengd umsagnar** slærðu inn hámarksfjölda stafa sem umsagnartitill getur haft (t.d. **55**).</span><span class="sxs-lookup"><span data-stu-id="8f1de-164">In the **Review Title Max Length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="8f1de-165">Veldur **Vista og birta**.</span><span class="sxs-lookup"><span data-stu-id="8f1de-165">Select **Save and Publish**.</span></span> 

<span data-ttu-id="8f1de-166">Eftirfarandi skýringarmynd sýnir hvernig þessi skilgreining lítur út í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8f1de-166">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Skilgreining svæðis til að sýna einkunnir og umsagnir](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="8f1de-168">Tengja vörueinkunn við umsagnarhlutann í PDP</span><span class="sxs-lookup"><span data-stu-id="8f1de-168">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="8f1de-169">Afurðaeinkunn er sýnd fyrir neðan afurðaheitið efst á PDP.</span><span class="sxs-lookup"><span data-stu-id="8f1de-169">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="8f1de-170">Hægt er að stilla afurðaeinkunnina þannig að hún sé tengd við hlutann **Umsagnir** í sama PDP.</span><span class="sxs-lookup"><span data-stu-id="8f1de-170">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="8f1de-171">Til að tengja vörueinkunn við hlutann **Umsagnir** í PDP fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8f1de-171">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="8f1de-172">Opnaðu PDP-sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="8f1de-172">Open the PDP template.</span></span> 
1. <span data-ttu-id="8f1de-173">Farðu í **Einingastillingar kaupkassagáma**.</span><span class="sxs-lookup"><span data-stu-id="8f1de-173">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="8f1de-174">Undir **Kaupkassi** velurðu **Afurðaeinkunn** og velur síðan gátreitinn **Tengja smellinn við fulla umsagnaeiningu**.</span><span class="sxs-lookup"><span data-stu-id="8f1de-174">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="8f1de-175">Eftirfarandi skýringarmynd sýnir hvernig þessi skilgreining lítur út í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8f1de-175">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Tenging afurðaeinkunnar við umsagnarhlutann í PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="8f1de-177">Stilltu hlekkinn fyrir persónuverndar- og stefnusíðuna</span><span class="sxs-lookup"><span data-stu-id="8f1de-177">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="8f1de-178">Til að stilla hlekkinn fyrir persónuverndar- og stefnusíðuna skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8f1de-178">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="8f1de-179">Fara til **Heim \> Svæði**.</span><span class="sxs-lookup"><span data-stu-id="8f1de-179">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="8f1de-180">Veldu heiti vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="8f1de-180">Select the name of your site.</span></span> 
1. <span data-ttu-id="8f1de-181">Farðu á **Svæðisstjórnun \> Stækkunarhæfni**</span><span class="sxs-lookup"><span data-stu-id="8f1de-181">Go to **Site management \> Extensibility**</span></span>
1. <span data-ttu-id="8f1de-182">Á flipanum **Leiðir**, undir **Persónuvernd og stefna RNR**, velurðu **Bæta við tengli**.</span><span class="sxs-lookup"><span data-stu-id="8f1de-182">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="8f1de-183">Ef tengill hefur þegar verið sleginn inn og þú vilt skipta um hann skaltu velja hann.</span><span class="sxs-lookup"><span data-stu-id="8f1de-183">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="8f1de-184">Í valmyndinni **Bæta við tengli** velurðu tengilinn fyrir persónuverndar- og stefnusíðuna og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="8f1de-184">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="8f1de-185">Veldur **Vista og birta**.</span><span class="sxs-lookup"><span data-stu-id="8f1de-185">Select **Save and Publish**.</span></span> 

<span data-ttu-id="8f1de-186">Eftirfarandi skýringarmynd sýnir hvernig þessi skilgreining lítur út í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8f1de-186">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Stilling tengils fyrir persónuverndar- og stefnusíðuna](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a><span data-ttu-id="8f1de-188">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8f1de-188">Additional resources</span></span>

[<span data-ttu-id="8f1de-189">Yfirlit yfir einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="8f1de-189">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="8f1de-190">Velja að nota einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="8f1de-190">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="8f1de-191">Stjórna einkunnum og umsögnum</span><span class="sxs-lookup"><span data-stu-id="8f1de-191">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="8f1de-192">Samstilla afurðaeinkunnir í Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="8f1de-192">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
