---
title: Samfélagsmiðlaeining
description: Þetta efnisatriði fjallar um samfélagsmiðlaeiningar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 0e7f30686894f9cf92257e99d95cc8b00f76f899
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234318"
---
# <a name="social-share-module"></a><span data-ttu-id="09893-103">Samfélagsmiðlaeining</span><span class="sxs-lookup"><span data-stu-id="09893-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="09893-104">Þetta efnisatriði fjallar um samfélagsmiðlaeiningar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="09893-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="09893-105">Samfélagsmiðlaeiningar gera notendum kleift að miðla vefslóðum rafrænna viðskipta á samfélagsmiðla á borð við Facebook, Twitter, Pinterest og LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="09893-105">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="09893-106">Einnig er hægt að samnýta vefslóðið vefsíðna með tölvupósti.</span><span class="sxs-lookup"><span data-stu-id="09893-106">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="09893-107">Samfélagsmiðlaeiningar eru almennt notaðar á upplýsingasíðum vöru (PDPs) til að auðvelda notendum að miðla upplýsingum um vöru.</span><span class="sxs-lookup"><span data-stu-id="09893-107">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="09893-108">Hver samfélagsmiðlaeining er gámur fyrir einingar samfélagsmiðlaatriða.</span><span class="sxs-lookup"><span data-stu-id="09893-108">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="09893-109">Hægt er að skilgreina hverja einingu þannig að hún beinist á tiltekna samfélagsmiðlasíðu.</span><span class="sxs-lookup"><span data-stu-id="09893-109">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="09893-110">Samþætti við Facebook, Twitter, Pinterest, LinkedIn og tölvupóst er studd.</span><span class="sxs-lookup"><span data-stu-id="09893-110">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="09893-111">Þegar vefsvæðisnotandi velur samfélagsmiðlatákn er HTML iframe opnað fyrir viðkomandi samfélagsmiðil.</span><span class="sxs-lookup"><span data-stu-id="09893-111">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="09893-112">Innan iframe getur notandinn skráð sig inn og birt efni síðunnar sem hann var að skoða.</span><span class="sxs-lookup"><span data-stu-id="09893-112">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="09893-113">Sérhver verkvangur samfélagsmiðla kann að rekja kökur og því þurfa svæðanotendur að staðfesta samþykkisboð fyrir kökur.</span><span class="sxs-lookup"><span data-stu-id="09893-113">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="09893-114">Þegar kökur eru ekki samþykktar er einingin falin á síðunni.</span><span class="sxs-lookup"><span data-stu-id="09893-114">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="09893-115">Nánari upplýsingar eru í [Reglufylgni köku](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="09893-115">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="09893-116">Eftirfarandi mynd sýnir dæmi um samfélagsmiðlaeiningu sem er notuð á upplýsingasíðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="09893-116">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![Dæmi um samfélagsmiðlaeiningu](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="09893-118">Eiginleikar samfélagsmiðlaeiningar</span><span class="sxs-lookup"><span data-stu-id="09893-118">Social share module properties</span></span>

| <span data-ttu-id="09893-119">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="09893-119">Property name</span></span>             | <span data-ttu-id="09893-120">Virði</span><span class="sxs-lookup"><span data-stu-id="09893-120">Value</span></span>                 | <span data-ttu-id="09893-121">lýsing</span><span class="sxs-lookup"><span data-stu-id="09893-121">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="09893-122">Myndatexti</span><span class="sxs-lookup"><span data-stu-id="09893-122">Caption</span></span>                  | <span data-ttu-id="09893-123">Texti</span><span class="sxs-lookup"><span data-stu-id="09893-123">Text</span></span> | <span data-ttu-id="09893-124">Þessi eiginleiki tilgreinir fyrirsögn einingarinnar.</span><span class="sxs-lookup"><span data-stu-id="09893-124">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="09893-125">Stefna</span><span class="sxs-lookup"><span data-stu-id="09893-125">Orientation</span></span> | <span data-ttu-id="09893-126">**Lárétt** eða **Lóðrétt**</span><span class="sxs-lookup"><span data-stu-id="09893-126">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="09893-127">Þessi eiginleiki skilgreinir útlitsátt fyrir atriði á samfélagsmiðlum.</span><span class="sxs-lookup"><span data-stu-id="09893-127">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="09893-128">Eiginleikaeiningar samfélagsmiðlaeiningar</span><span class="sxs-lookup"><span data-stu-id="09893-128">Social share item module properties</span></span>
| <span data-ttu-id="09893-129">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="09893-129">Property name</span></span>             | <span data-ttu-id="09893-130">Virði</span><span class="sxs-lookup"><span data-stu-id="09893-130">Value</span></span>                 | <span data-ttu-id="09893-131">lýsing</span><span class="sxs-lookup"><span data-stu-id="09893-131">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="09893-132">Netsamfélög</span><span class="sxs-lookup"><span data-stu-id="09893-132">Social media</span></span>              | <span data-ttu-id="09893-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span><span class="sxs-lookup"><span data-stu-id="09893-133">**Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail**</span></span> | <span data-ttu-id="09893-134">Fellivalmynd með lista yfir samfélagsmiðla.</span><span class="sxs-lookup"><span data-stu-id="09893-134">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="09893-135">Tákn</span><span class="sxs-lookup"><span data-stu-id="09893-135">Icon</span></span> |<span data-ttu-id="09893-136">Mynd</span><span class="sxs-lookup"><span data-stu-id="09893-136">Image</span></span>    | <span data-ttu-id="09893-137">Þetta verður myndin sem birtist fyrir viðkomandi samfélagsmiðil.</span><span class="sxs-lookup"><span data-stu-id="09893-137">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="09893-138">Bestu starfsvenju um notkun mynda fyrir verkvanga er að finna í SDK fyrir verkvang samfélagsmiðilsins.</span><span class="sxs-lookup"><span data-stu-id="09893-138">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="09893-139">Bæta samfélagsmiðlaeiningu við kaupgluggaeiningu</span><span class="sxs-lookup"><span data-stu-id="09893-139">Add a social share module to a buy box module</span></span>

<span data-ttu-id="09893-140">Til að bæta við samfélagsmiðlaeiningu við kaupgluggaeiningu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="09893-140">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="09893-141">Á Fabrikam-svæðinu skal velja **Síður**, og síðan velja **DefaulPDP** síðuna til að opna upplýsingasíðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="09893-141">In the Fabrikam site, select **Pages**, and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="09893-142">Í hólfinu **Kaupgluggi (krafist)**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="09893-142">In the **Buybox (required)** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="09893-143">Í glugganum **Bæta við einingu** skal velja eininguna **Deila á samfélagsmiðlum** og síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="09893-143">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="09893-144">Í hólfinu **Deila á samfélagsmiðlum**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="09893-144">In the **Social Share** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="09893-145">Í glugganum **Bæta við einingu** skal velja eininguna **SocialShare** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="09893-145">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="09893-146">Á eiginleikasvæðinu í **SocialShare** einingunni, undir **Stefna**, skal velja **Lárétt**.</span><span class="sxs-lookup"><span data-stu-id="09893-146">In the properties pane of the **SocialShare** module, under **Orientation**, select **Horizontal**.</span></span> <span data-ttu-id="09893-147">Bættu við myndatexta eins og nauðsynlegt er.</span><span class="sxs-lookup"><span data-stu-id="09893-147">Add a caption as needed.</span></span>
1. <span data-ttu-id="09893-148">Í hólfinu **SocialShare**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="09893-148">In the **SocialShare** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="09893-149">Í glugganum **Bæta við einingu** skal velja eininguna **SocialShareItem** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="09893-149">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="09893-150">Á eiginleikasvæði **SocialShareItem** einingarinnar, undir **Samfélagsmiðlar** skal velja **Facebook**.</span><span class="sxs-lookup"><span data-stu-id="09893-150">In the properties pane of the **SocialShareItem** module, under **Social Media**, select **Facebook**.</span></span>
1. <span data-ttu-id="09893-151">Á eiginleikasvæði **SocialShareItem** einingarinnar, undir **Tákn** skal velja **+ Bæta við mynd**.</span><span class="sxs-lookup"><span data-stu-id="09893-151">In the properties pane of the **SocialShareItem** module, under **Icon**, select **+ Add an image**.</span></span>
1. <span data-ttu-id="09893-152">Í glugganum **Val á miðli** skal velja Facebook lógómynd og svo **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="09893-152">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="09893-153">Ef engin Facebook-lógómynd er til staðar skal velja **Hlaða upp nýju margmiðlunaratriði** til að hlaða upp einni.</span><span class="sxs-lookup"><span data-stu-id="09893-153">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="09893-154">Bætið við og skilgreinið frekari **SocialShareItem** einingar eins og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="09893-154">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="09893-155">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="09893-155">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="09893-156">Síðan sýnir samfélagsmiðlaeiningu.</span><span class="sxs-lookup"><span data-stu-id="09893-156">The page will show the social share module.</span></span>
1. <span data-ttu-id="09893-157">Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="09893-157">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="09893-158">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="09893-158">Additional resources</span></span>

[<span data-ttu-id="09893-159">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="09893-159">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="09893-160">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="09893-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="09893-161">Reglufylgni köku</span><span class="sxs-lookup"><span data-stu-id="09893-161">Cookie compliance</span></span>](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]