---
title: Skilgreina einkunnir og umsagnir
description: Þetta efnisatriði lýsir því hvernig á að grunnstilla svæði fyrir rafræn viðskipti til að sýna einkunnir og umsagnir viðskiptavina í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 130c80c1d68c7fb207a4fa073fe2b0476cbdd409
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220535"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="f6029-103">Skilgreina einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="f6029-103">Configure ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f6029-104">Þetta efnisatriði lýsir því hvernig á að grunnstilla svæði fyrir rafræn viðskipti til að sýna einkunnir og umsagnir viðskiptavina í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f6029-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f6029-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="f6029-105">Overview</span></span>

<span data-ttu-id="f6029-106">Mat og umsagnir á vefsíðum um netverslun hjálpa viðskiptavinum að fræðast um vörur áður en þeir taka kaupákvörðun með því að sýna þeim hvað öðrum viðskiptavinum finnst um þessar vörur.</span><span class="sxs-lookup"><span data-stu-id="f6029-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision by showing them what other customers think about those products.</span></span> <span data-ttu-id="f6029-107">Fyrir vefsíður í netverslun eru einkunnir og umsagnir einnig búnaður til að safna endurgjöf viðskiptavina um vörur.</span><span class="sxs-lookup"><span data-stu-id="f6029-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="f6029-108">Skilgreina svæði til að sýna einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="f6029-108">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="f6029-109">Stillingargildi fyrir einkunnir og umsagnir, svo sem auðkenni leigjanda, lengd textatexta og lengd endurskoðunar titils, eru stillt á vefsvæðisstig.</span><span class="sxs-lookup"><span data-stu-id="f6029-109">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="f6029-110">Fylgdu þessum skrefum til að stilla vefsíðu til að sýna einkunnir og umsagnir.</span><span class="sxs-lookup"><span data-stu-id="f6029-110">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="f6029-111">Fara til **Heim \> Svæði**.</span><span class="sxs-lookup"><span data-stu-id="f6029-111">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="f6029-112">Veldu heiti vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="f6029-112">Select the name of your site.</span></span> 
1. <span data-ttu-id="f6029-113">Fara til **Vefstillingar \> Viðbætur**.</span><span class="sxs-lookup"><span data-stu-id="f6029-113">Go to **Site settings \> Extensions**.</span></span> 
1. <span data-ttu-id="f6029-114">Í reitinn **Hámarkstextalengd umsagnar** slærðu inn hámarksfjölda stafa sem umsagnartexti getur haft (t.d. **1000**).</span><span class="sxs-lookup"><span data-stu-id="f6029-114">In the **Review text max length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="f6029-115">Í reitinn **Hámarkstitillengd umsagnar** slærðu inn hámarksfjölda stafa sem umsagnartitill getur haft (t.d. **55**).</span><span class="sxs-lookup"><span data-stu-id="f6029-115">In the **Review title max length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="f6029-116">Veldur **Vista og birta**.</span><span class="sxs-lookup"><span data-stu-id="f6029-116">Select **Save and Publish**.</span></span> 

<span data-ttu-id="f6029-117">Eftirfarandi skýringarmynd sýnir hvernig þessi skilgreining lítur út í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f6029-117">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Skilgreining svæðis til að sýna einkunnir og umsagnir](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="f6029-119">Tengja vörueinkunn við umsagnarhlutann í PDP</span><span class="sxs-lookup"><span data-stu-id="f6029-119">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="f6029-120">Afurðaeinkunn er sýnd fyrir neðan afurðaheitið efst á PDP.</span><span class="sxs-lookup"><span data-stu-id="f6029-120">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="f6029-121">Hægt er að stilla afurðaeinkunnina þannig að hún sé tengd við hlutann **Umsagnir** í sama PDP.</span><span class="sxs-lookup"><span data-stu-id="f6029-121">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="f6029-122">Til að tengja vörueinkunn við hlutann **Umsagnir** í PDP fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="f6029-122">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="f6029-123">Opnaðu PDP-sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="f6029-123">Open the PDP template.</span></span> 
1. <span data-ttu-id="f6029-124">Farðu í **Einingastillingar kaupkassagáma**.</span><span class="sxs-lookup"><span data-stu-id="f6029-124">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="f6029-125">Undir **Kaupkassi** velurðu **Afurðaeinkunn** og velur síðan gátreitinn **Tengja smellinn við fulla umsagnaeiningu**.</span><span class="sxs-lookup"><span data-stu-id="f6029-125">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="f6029-126">Eftirfarandi skýringarmynd sýnir hvernig þessi skilgreining lítur út í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f6029-126">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Tenging afurðaeinkunnar við umsagnarhlutann í PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="f6029-128">Stilltu hlekkinn fyrir persónuverndar- og stefnusíðuna</span><span class="sxs-lookup"><span data-stu-id="f6029-128">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="f6029-129">Til að stilla hlekkinn fyrir persónuverndar- og stefnusíðuna skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="f6029-129">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="f6029-130">Fara til **Heim \> Svæði**.</span><span class="sxs-lookup"><span data-stu-id="f6029-130">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="f6029-131">Veldu heiti vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="f6029-131">Select the name of your site.</span></span> 
1. <span data-ttu-id="f6029-132">Fara til **Vefstillingar \> Viðbætur**.</span><span class="sxs-lookup"><span data-stu-id="f6029-132">Go to **Site settings \> Extensions**.</span></span>
1. <span data-ttu-id="f6029-133">Á flipanum **Leiðir**, undir **Persónuvernd og stefna RNR**, velurðu **Bæta við tengli**.</span><span class="sxs-lookup"><span data-stu-id="f6029-133">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="f6029-134">Ef tengill hefur þegar verið sleginn inn og þú vilt skipta um hann skaltu velja hann.</span><span class="sxs-lookup"><span data-stu-id="f6029-134">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="f6029-135">Í valmyndinni **Bæta við tengli** velurðu tengilinn fyrir persónuverndar- og stefnusíðuna og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f6029-135">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="f6029-136">Veldur **Vista og birta**.</span><span class="sxs-lookup"><span data-stu-id="f6029-136">Select **Save and Publish**.</span></span> 

<span data-ttu-id="f6029-137">Eftirfarandi skýringarmynd sýnir hvernig þessi skilgreining lítur út í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f6029-137">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Stilling tengils fyrir persónuverndar- og stefnusíðuna](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a><span data-ttu-id="f6029-139">Stilla einkunnir og endurskoða einingar á upplýsingasíðum</span><span class="sxs-lookup"><span data-stu-id="f6029-139">Configure ratings and reviews modules on product details pages</span></span>

<span data-ttu-id="f6029-140">Sjá upplýsingar um stillingar á einkunna- og umsagnaeiningum á upplýsingasíðum afurða [Einkunna- og umsagnaeiningar](ratings-reviews-modules.md).</span><span class="sxs-lookup"><span data-stu-id="f6029-140">For information on configuring ratings and reviews modules on product details pages, see [Ratings and reviews modules](ratings-reviews-modules.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f6029-141">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f6029-141">Additional resources</span></span>

[<span data-ttu-id="f6029-142">Yfirlit yfir einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="f6029-142">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="f6029-143">Velja að nota einkunnir og umsagnir</span><span class="sxs-lookup"><span data-stu-id="f6029-143">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="f6029-144">Stjórna einkunnum og umsögnum</span><span class="sxs-lookup"><span data-stu-id="f6029-144">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="f6029-145">Stilla einkunnir og endurskoða einingar á upplýsingasíðum</span><span class="sxs-lookup"><span data-stu-id="f6029-145">Configure ratings and reviews modules on product details pages</span></span>](ratings-reviews-modules.md)

[<span data-ttu-id="f6029-146">Samstilla afurðaeinkunnir í Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="f6029-146">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]