---
title: Einkunna- og umsagnaeiningar
description: Þetta efnisatriði fer yfir stillingu einkunna og endurskoðun einingar á upplýsingasíðum í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: a243399536fec3f5361104289c38e550bf8b1144
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193283"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="d5439-103">Einkunna- og umsagnaeiningar</span><span class="sxs-lookup"><span data-stu-id="d5439-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d5439-104">Þetta efnisatriði nær yfir stillingu einkunna og endurskoðun einingar á upplýsingasíðum í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d5439-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d5439-105">Mat og umsagnir á vefsíðum um netverslun hjálpa viðskiptavinum að fræðast um vörur áður en þeir taka kaupákvörðun og eru einnig búnaður til að safna endurgjöf viðskiptavina um afurðir.</span><span class="sxs-lookup"><span data-stu-id="d5439-105">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="d5439-106">Einkunnir eru sýndar á vörulistasíðum, flokkalistasíðum, leitarniðurstöðusíðum og öðrum vefsíðum.</span><span class="sxs-lookup"><span data-stu-id="d5439-106">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="d5439-107">Stuðlarit einkunna og afurðaumsagnir eru sýndar á upplýsingasíðum afurða.</span><span class="sxs-lookup"><span data-stu-id="d5439-107">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="d5439-108">Hnappurinn **Skrifa umsögn** gerir viðskiptavinum kleift að senda inn einkunnir og umsagnir um afurð.</span><span class="sxs-lookup"><span data-stu-id="d5439-108">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="d5439-109">Þessum eiginleikum upplýsingasíða afurða er stjórnað af mats- og umsagnareiningum.</span><span class="sxs-lookup"><span data-stu-id="d5439-109">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="d5439-110">Einkunna- og umsagnaeiningar á PDP</span><span class="sxs-lookup"><span data-stu-id="d5439-110">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="d5439-111">Þrjár einingar sýna yfirlit yfir mat og yfirlit yfir PDP:</span><span class="sxs-lookup"><span data-stu-id="d5439-111">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="d5439-112">Skrifa umsagnareiningu</span><span class="sxs-lookup"><span data-stu-id="d5439-112">Write review module</span></span>
- <span data-ttu-id="d5439-113">Eining umsagnalista afurðar</span><span class="sxs-lookup"><span data-stu-id="d5439-113">Product reviews list module</span></span>
- <span data-ttu-id="d5439-114">Stuðlaritseining einkunna</span><span class="sxs-lookup"><span data-stu-id="d5439-114">Ratings histogram module</span></span>
 
<span data-ttu-id="d5439-115">Eftirfarandi mynd sýnir hvernig einkunnirnar og umsagnirnar líta út á PDP.</span><span class="sxs-lookup"><span data-stu-id="d5439-115">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Einkunna- og umsagnaeiningar á PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="d5439-117">Fyrir upplýsingar um hvernig á að fínstilla PDP sniðmát og útlit svo að þú getir deilt stillingum fyrir einingar einkunna og umsagna meðal margra PDP á netverslunarvefsvæðinu, sjá [Yfirlit yfir sniðmát og útlit](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d5439-117">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="d5439-118">Eftirfarandi mynd sýnir hvernig glugginn **Bæta við einingu** birtir einingar einkunna og umsagna í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d5439-118">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="d5439-119">![Bættu við einingaglugga](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="d5439-119">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="d5439-120">Skrifa umsagnareiningu</span><span class="sxs-lookup"><span data-stu-id="d5439-120">Write review module</span></span>

<span data-ttu-id="d5439-121">Í einingunni skrifa umsögn inniheldur hnappurinn **Skrifa umsögn** sem gerir notendum kleift að skrá sig inn, úthluta mati og skrifa umsögn um vöru.</span><span class="sxs-lookup"><span data-stu-id="d5439-121">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="d5439-122">Þessi eining gerir notendum einnig kleift að breyta einkunn eða umsögn sem þeir sendu inn áður.</span><span class="sxs-lookup"><span data-stu-id="d5439-122">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="d5439-123">Þessi eining birtist venjulega fyrir ofan einingarnar stuðlarit einkunna og lista yfir afurðaumsagnir á PDP.</span><span class="sxs-lookup"><span data-stu-id="d5439-123">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="d5439-124">Eftirfarandi mynd sýnir valmyndina **Skrifa umsögn** sem birtist þegar viðskiptavinur velur **Skrifa umsögn**.</span><span class="sxs-lookup"><span data-stu-id="d5439-124">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="d5439-125">Viðskiptavinurinn getur notað þennan glugga til að leggja fram mat og umsögn.</span><span class="sxs-lookup"><span data-stu-id="d5439-125">The customer can use this dialog box to submit a rating and a review.</span></span>

![Skrifaðu umsagnarglugga](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="d5439-127">Eftirfarandi tafla sýnir eiginleikann fyrir eininguna skrifa umsögn sem þarf að stilla í höfundatólinu.</span><span class="sxs-lookup"><span data-stu-id="d5439-127">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="d5439-128">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="d5439-128">Property name</span></span> | <span data-ttu-id="d5439-129">Virði</span><span class="sxs-lookup"><span data-stu-id="d5439-129">Value</span></span>        | <span data-ttu-id="d5439-130">Lýsing á eiginleika</span><span class="sxs-lookup"><span data-stu-id="d5439-130">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="d5439-131">Nafn</span><span class="sxs-lookup"><span data-stu-id="d5439-131">Name</span></span>          | <span data-ttu-id="d5439-132">Skrifa umsögn</span><span class="sxs-lookup"><span data-stu-id="d5439-132">Write review</span></span> | <span data-ttu-id="d5439-133">Heiti einingarinnar skrifa umsögn.</span><span class="sxs-lookup"><span data-stu-id="d5439-133">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="d5439-134">Stuðlaritseining einkunna</span><span class="sxs-lookup"><span data-stu-id="d5439-134">Ratings histogram module</span></span>

<span data-ttu-id="d5439-135">Stuðlaritseining einkunna sýnir stuðlarit með einkunnum.</span><span class="sxs-lookup"><span data-stu-id="d5439-135">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="d5439-136">Þessi eining birtist venjulega á milli eininga skrifa umsagna og afurðaumsagnalistaeiningarinnar á PDP.</span><span class="sxs-lookup"><span data-stu-id="d5439-136">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="d5439-137">Stuðlaritseining einkunna þarf enga skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="d5439-137">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="d5439-138">Þú þarft bara að bæta einingunni við í PDP sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="d5439-138">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="d5439-139">Eftirfarandi myndir sýna hvernig PDP sniðmát lítur út í Dynamics 365 Commerce þegar einkunnir og umsagnaeiningar eru stilltar til birtingar á PDP.</span><span class="sxs-lookup"><span data-stu-id="d5439-139">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="d5439-140">![PDP sniðmát þegar einkunnir og umsagnir eru stilltar til birtingar á PDP](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="d5439-140">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="d5439-141">Eining umsagnalista afurðar</span><span class="sxs-lookup"><span data-stu-id="d5439-141">Product reviews list module</span></span>

<span data-ttu-id="d5439-142">Einingin yfir vöruúttektarlista sýnir lista yfir afurðaumsagnir ásamt flokkunar-, síunar- og síðuskiptingarvalkostum.</span><span class="sxs-lookup"><span data-stu-id="d5439-142">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="d5439-143">Þessi eining birtist venjulega eftir stuðlaritseining einkunna á PDP.</span><span class="sxs-lookup"><span data-stu-id="d5439-143">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="d5439-144">Eftirfarandi tafla sýnir eiginleika fyrir einingu yfir umsagnalista afurða sem þarf að stilla í höfundatólinu.</span><span class="sxs-lookup"><span data-stu-id="d5439-144">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="d5439-145">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="d5439-145">Property name</span></span>              | <span data-ttu-id="d5439-146">Virði</span><span class="sxs-lookup"><span data-stu-id="d5439-146">Value</span></span> | <span data-ttu-id="d5439-147">Lýsing á eiginleika</span><span class="sxs-lookup"><span data-stu-id="d5439-147">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="d5439-148">Umsagnir sýndar á síðu</span><span class="sxs-lookup"><span data-stu-id="d5439-148">Reviews shown on each page</span></span> | <span data-ttu-id="d5439-149">10</span><span class="sxs-lookup"><span data-stu-id="d5439-149">10</span></span>    | <span data-ttu-id="d5439-150">Fjöldi umsagna sem ætti að birtast í einu á PDP.</span><span class="sxs-lookup"><span data-stu-id="d5439-150">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="d5439-151">Hnapparnir **Næst** og **Fyrri** eru með, svo að notendur geti farið í gegnum umsagnasíðurnar.</span><span class="sxs-lookup"><span data-stu-id="d5439-151">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="d5439-152">Stuðlarit einkunna - Samantektaryfirlit</span><span class="sxs-lookup"><span data-stu-id="d5439-152">Ratings histogram – Summary view</span></span>

<span data-ttu-id="d5439-153">Einingin yfir afurðaumsagnalista inniheldur hólf þar sem þú getur bætt við stuðlaritseiningu einkunna.</span><span class="sxs-lookup"><span data-stu-id="d5439-153">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="d5439-154">Eftirfarandi mynd sýnir hvernig þú getur bætt við stuðlaritseiningu einkunna fyrir afurðaumsagnalista í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d5439-154">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Bætir við stuðlaritseiningu einkunna í einingu afurðaumsagnalista](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="d5439-156">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d5439-156">Additional resources</span></span>

[<span data-ttu-id="d5439-157">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="d5439-157">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d5439-158">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="d5439-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="d5439-159">Körfueining</span><span class="sxs-lookup"><span data-stu-id="d5439-159">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="d5439-160">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="d5439-160">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d5439-161">Eining pöntunarstaðfestingar</span><span class="sxs-lookup"><span data-stu-id="d5439-161">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="d5439-162">Fyrirsagnareining</span><span class="sxs-lookup"><span data-stu-id="d5439-162">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="d5439-163">Neðanmálseining</span><span class="sxs-lookup"><span data-stu-id="d5439-163">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]