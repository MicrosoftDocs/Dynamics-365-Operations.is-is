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
ms.openlocfilehash: dee9a6a7e2a5278f069958ce00689b1beb9b1bd7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792148"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="5a135-103">Einkunna- og umsagnaeiningar</span><span class="sxs-lookup"><span data-stu-id="5a135-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5a135-104">Þetta efnisatriði nær yfir stillingu einkunna og endurskoðun einingar á upplýsingasíðum í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5a135-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5a135-105">Mat og umsagnir á vefsíðum um netverslun hjálpa viðskiptavinum að fræðast um vörur áður en þeir taka kaupákvörðun og eru einnig búnaður til að safna endurgjöf viðskiptavina um afurðir.</span><span class="sxs-lookup"><span data-stu-id="5a135-105">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="5a135-106">Einkunnir eru sýndar á vörulistasíðum, flokkalistasíðum, leitarniðurstöðusíðum og öðrum vefsíðum.</span><span class="sxs-lookup"><span data-stu-id="5a135-106">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="5a135-107">Stuðlarit einkunna og afurðaumsagnir eru sýndar á upplýsingasíðum afurða.</span><span class="sxs-lookup"><span data-stu-id="5a135-107">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="5a135-108">Hnappurinn **Skrifa umsögn** gerir viðskiptavinum kleift að senda inn einkunnir og umsagnir um afurð.</span><span class="sxs-lookup"><span data-stu-id="5a135-108">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="5a135-109">Þessum eiginleikum upplýsingasíða afurða er stjórnað af mats- og umsagnareiningum.</span><span class="sxs-lookup"><span data-stu-id="5a135-109">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="5a135-110">Einkunna- og umsagnaeiningar á PDP</span><span class="sxs-lookup"><span data-stu-id="5a135-110">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="5a135-111">Þrjár einingar sýna yfirlit yfir mat og yfirlit yfir PDP:</span><span class="sxs-lookup"><span data-stu-id="5a135-111">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="5a135-112">Skrifa umsagnareiningu</span><span class="sxs-lookup"><span data-stu-id="5a135-112">Write review module</span></span>
- <span data-ttu-id="5a135-113">Eining umsagnalista afurðar</span><span class="sxs-lookup"><span data-stu-id="5a135-113">Product reviews list module</span></span>
- <span data-ttu-id="5a135-114">Stuðlaritseining einkunna</span><span class="sxs-lookup"><span data-stu-id="5a135-114">Ratings histogram module</span></span>
 
<span data-ttu-id="5a135-115">Eftirfarandi mynd sýnir hvernig einkunnirnar og umsagnirnar líta út á PDP.</span><span class="sxs-lookup"><span data-stu-id="5a135-115">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Einkunna- og umsagnaeiningar á PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="5a135-117">Fyrir upplýsingar um hvernig á að fínstilla PDP sniðmát og útlit svo að þú getir deilt stillingum fyrir einingar einkunna og umsagna meðal margra PDP á netverslunarvefsvæðinu, sjá [Yfirlit yfir sniðmát og útlit](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5a135-117">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="5a135-118">Eftirfarandi mynd sýnir hvernig glugginn **Bæta við einingu** birtir einingar einkunna og umsagna í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5a135-118">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="5a135-119">![Bættu við einingaglugga](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="5a135-119">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="5a135-120">Skrifa umsagnareiningu</span><span class="sxs-lookup"><span data-stu-id="5a135-120">Write review module</span></span>

<span data-ttu-id="5a135-121">Í einingunni skrifa umsögn inniheldur hnappurinn **Skrifa umsögn** sem gerir notendum kleift að skrá sig inn, úthluta mati og skrifa umsögn um vöru.</span><span class="sxs-lookup"><span data-stu-id="5a135-121">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="5a135-122">Þessi eining gerir notendum einnig kleift að breyta einkunn eða umsögn sem þeir sendu inn áður.</span><span class="sxs-lookup"><span data-stu-id="5a135-122">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="5a135-123">Þessi eining birtist venjulega fyrir ofan einingarnar stuðlarit einkunna og lista yfir afurðaumsagnir á PDP.</span><span class="sxs-lookup"><span data-stu-id="5a135-123">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="5a135-124">Eftirfarandi mynd sýnir valmyndina **Skrifa umsögn** sem birtist þegar viðskiptavinur velur **Skrifa umsögn**.</span><span class="sxs-lookup"><span data-stu-id="5a135-124">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="5a135-125">Viðskiptavinurinn getur notað þennan glugga til að leggja fram mat og umsögn.</span><span class="sxs-lookup"><span data-stu-id="5a135-125">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="5a135-126">![Skrifaðu umsagnarglugga](media/rnr-eCommerce-write-review-module.png) Eftirfarandi tafla sýnir eiginleikann fyrir eininguna skrifa umsögn sem þarf að stilla í höfundatólinu.</span><span class="sxs-lookup"><span data-stu-id="5a135-126">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="5a135-127">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="5a135-127">Property name</span></span> | <span data-ttu-id="5a135-128">Virði</span><span class="sxs-lookup"><span data-stu-id="5a135-128">Value</span></span>        | <span data-ttu-id="5a135-129">Lýsing á eiginleika</span><span class="sxs-lookup"><span data-stu-id="5a135-129">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="5a135-130">Nafn</span><span class="sxs-lookup"><span data-stu-id="5a135-130">Name</span></span>          | <span data-ttu-id="5a135-131">Skrifa umsögn</span><span class="sxs-lookup"><span data-stu-id="5a135-131">Write review</span></span> | <span data-ttu-id="5a135-132">Heiti einingarinnar skrifa umsögn.</span><span class="sxs-lookup"><span data-stu-id="5a135-132">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="5a135-133">Stuðlaritseining einkunna</span><span class="sxs-lookup"><span data-stu-id="5a135-133">Ratings histogram module</span></span>

<span data-ttu-id="5a135-134">Stuðlaritseining einkunna sýnir stuðlarit með einkunnum.</span><span class="sxs-lookup"><span data-stu-id="5a135-134">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="5a135-135">Þessi eining birtist venjulega á milli eininga skrifa umsagna og afurðaumsagnalistaeiningarinnar á PDP.</span><span class="sxs-lookup"><span data-stu-id="5a135-135">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="5a135-136">Stuðlaritseining einkunna þarf enga skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="5a135-136">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="5a135-137">Þú þarft bara að bæta einingunni við í PDP sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="5a135-137">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="5a135-138">Eftirfarandi myndir sýna hvernig PDP sniðmát lítur út í Dynamics 365 Commerce þegar einkunnir og umsagnaeiningar eru stilltar til birtingar á PDP.</span><span class="sxs-lookup"><span data-stu-id="5a135-138">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="5a135-139">![PDP sniðmát þegar einkunnir og umsagnir eru stilltar til birtingar á PDP](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="5a135-139">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="5a135-140">Eining umsagnalista afurðar</span><span class="sxs-lookup"><span data-stu-id="5a135-140">Product reviews list module</span></span>

<span data-ttu-id="5a135-141">Einingin yfir vöruúttektarlista sýnir lista yfir afurðaumsagnir ásamt flokkunar-, síunar- og síðuskiptingarvalkostum.</span><span class="sxs-lookup"><span data-stu-id="5a135-141">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="5a135-142">Þessi eining birtist venjulega eftir stuðlaritseining einkunna á PDP.</span><span class="sxs-lookup"><span data-stu-id="5a135-142">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="5a135-143">Eftirfarandi tafla sýnir eiginleika fyrir einingu yfir umsagnalista afurða sem þarf að stilla í höfundatólinu.</span><span class="sxs-lookup"><span data-stu-id="5a135-143">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="5a135-144">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="5a135-144">Property name</span></span>              | <span data-ttu-id="5a135-145">Virði</span><span class="sxs-lookup"><span data-stu-id="5a135-145">Value</span></span> | <span data-ttu-id="5a135-146">Lýsing á eiginleika</span><span class="sxs-lookup"><span data-stu-id="5a135-146">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="5a135-147">Umsagnir sýndar á síðu</span><span class="sxs-lookup"><span data-stu-id="5a135-147">Reviews shown on each page</span></span> | <span data-ttu-id="5a135-148">10</span><span class="sxs-lookup"><span data-stu-id="5a135-148">10</span></span>    | <span data-ttu-id="5a135-149">Fjöldi umsagna sem ætti að birtast í einu á PDP.</span><span class="sxs-lookup"><span data-stu-id="5a135-149">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="5a135-150">Hnapparnir **Næst** og **Fyrri** eru með, svo að notendur geti farið í gegnum umsagnasíðurnar.</span><span class="sxs-lookup"><span data-stu-id="5a135-150">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="5a135-151">Stuðlarit einkunna - Samantektaryfirlit</span><span class="sxs-lookup"><span data-stu-id="5a135-151">Ratings histogram – Summary view</span></span>

<span data-ttu-id="5a135-152">Einingin yfir afurðaumsagnalista inniheldur hólf þar sem þú getur bætt við stuðlaritseiningu einkunna.</span><span class="sxs-lookup"><span data-stu-id="5a135-152">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="5a135-153">Eftirfarandi mynd sýnir hvernig þú getur bætt við stuðlaritseiningu einkunna fyrir afurðaumsagnalista í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5a135-153">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Bætir við stuðlaritseiningu einkunna í einingu afurðaumsagnalista](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="5a135-155">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="5a135-155">Additional resources</span></span>

[<span data-ttu-id="5a135-156">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="5a135-156">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5a135-157">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="5a135-157">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="5a135-158">Körfueining</span><span class="sxs-lookup"><span data-stu-id="5a135-158">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="5a135-159">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="5a135-159">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="5a135-160">Eining pöntunarstaðfestingar</span><span class="sxs-lookup"><span data-stu-id="5a135-160">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="5a135-161">Fyrirsagnareining</span><span class="sxs-lookup"><span data-stu-id="5a135-161">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="5a135-162">Neðanmálseining</span><span class="sxs-lookup"><span data-stu-id="5a135-162">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]