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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 82a8795360f453cdee19fa6e9e376a42e8276849
ms.sourcegitcommit: 69075e001d1fb4ef69282667052cd8d082273094
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022078"
---
# <a name="social-share-module"></a><span data-ttu-id="10638-103">Samfélagsmiðlaeining</span><span class="sxs-lookup"><span data-stu-id="10638-103">Social share module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="10638-104">Þetta efnisatriði fjallar um samfélagsmiðlaeiningar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="10638-104">This topic covers social share modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="10638-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="10638-105">Overview</span></span>

<span data-ttu-id="10638-106">Samfélagsmiðlaeiningar gera notendum kleift að miðla vefslóðum rafrænna viðskipta á samfélagsmiðla á borð við Facebook, Twitter, Pinterest og LinkedIn.</span><span class="sxs-lookup"><span data-stu-id="10638-106">Social share modules allow users to share e-Commerce site page URLs on social media such as Facebook, Twitter, Pinterest, and LinkedIn.</span></span> <span data-ttu-id="10638-107">Einnig er hægt að samnýta vefslóðið vefsíðna með tölvupósti.</span><span class="sxs-lookup"><span data-stu-id="10638-107">Site page URLs can also be shared via email.</span></span> <span data-ttu-id="10638-108">Samfélagsmiðlaeiningar eru almennt notaðar á upplýsingasíðum vöru (PDPs) til að auðvelda notendum að miðla upplýsingum um vöru.</span><span class="sxs-lookup"><span data-stu-id="10638-108">Social share modules are commonly used on product details pages (PDPs) to help users share product information.</span></span>

<span data-ttu-id="10638-109">Hver samfélagsmiðlaeining er gámur fyrir einingar samfélagsmiðlaatriða.</span><span class="sxs-lookup"><span data-stu-id="10638-109">Each social share module is a container for social share item modules.</span></span> <span data-ttu-id="10638-110">Hægt er að skilgreina hverja einingu þannig að hún beinist á tiltekna samfélagsmiðlasíðu.</span><span class="sxs-lookup"><span data-stu-id="10638-110">Each social share item module can be configured to point to a specific social media site.</span></span> <span data-ttu-id="10638-111">Samþætti við Facebook, Twitter, Pinterest, LinkedIn og tölvupóst er studd.</span><span class="sxs-lookup"><span data-stu-id="10638-111">Integration with Facebook, Twitter, Pinterest, LinkedIn, and email is supported out of the box.</span></span> <span data-ttu-id="10638-112">Þegar vefsvæðisnotandi velur samfélagsmiðlatákn er HTML iframe opnað fyrir viðkomandi samfélagsmiðil.</span><span class="sxs-lookup"><span data-stu-id="10638-112">When a site user selects a social media symbol, an HTML iframe is launched for the respective social media site.</span></span> <span data-ttu-id="10638-113">Innan iframe getur notandinn skráð sig inn og birt efni síðunnar sem hann var að skoða.</span><span class="sxs-lookup"><span data-stu-id="10638-113">Within the iframe, the user can sign in and post the page content that they were viewing.</span></span>

<span data-ttu-id="10638-114">Sérhver verkvangur samfélagsmiðla kann að rekja kökur og því þurfa svæðanotendur að staðfesta samþykkisboð fyrir kökur.</span><span class="sxs-lookup"><span data-stu-id="10638-114">Each social media platform may track cookies, so this module requires site users to accept the cookie consent notification message.</span></span> <span data-ttu-id="10638-115">Þegar kökur eru ekki samþykktar er einingin falin á síðunni.</span><span class="sxs-lookup"><span data-stu-id="10638-115">When cookie consent is not accepted, the module will be hidden on the page.</span></span> <span data-ttu-id="10638-116">Nánari upplýsingar eru í [Reglufylgni köku](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="10638-116">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="10638-117">Eftirfarandi mynd sýnir dæmi um samfélagsmiðlaeiningu sem er notuð á upplýsingasíðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="10638-117">The following illustration highlights an example of a social share module used on a product details page.</span></span>

![Dæmi um samfélagsmiðlaeiningu](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a><span data-ttu-id="10638-119">Eiginleikar samfélagsmiðlaeiningar</span><span class="sxs-lookup"><span data-stu-id="10638-119">Social share module properties</span></span>

| <span data-ttu-id="10638-120">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="10638-120">Property name</span></span>             | <span data-ttu-id="10638-121">Virði</span><span class="sxs-lookup"><span data-stu-id="10638-121">Value</span></span>                 | <span data-ttu-id="10638-122">lýsing</span><span class="sxs-lookup"><span data-stu-id="10638-122">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="10638-123">Myndatexti</span><span class="sxs-lookup"><span data-stu-id="10638-123">Caption</span></span>                  | <span data-ttu-id="10638-124">Texti</span><span class="sxs-lookup"><span data-stu-id="10638-124">Text</span></span> | <span data-ttu-id="10638-125">Þessi eiginleiki tilgreinir fyrirsögn einingarinnar.</span><span class="sxs-lookup"><span data-stu-id="10638-125">This property specifies a caption for the module.</span></span> |
| <span data-ttu-id="10638-126">Stefna</span><span class="sxs-lookup"><span data-stu-id="10638-126">Orientation</span></span> | <span data-ttu-id="10638-127">**Lárétt** eða **Lóðrétt**</span><span class="sxs-lookup"><span data-stu-id="10638-127">**Horizontal** or **Vertical**</span></span>  | <span data-ttu-id="10638-128">Þessi eiginleiki skilgreinir útlitsátt fyrir atriði á samfélagsmiðlum.</span><span class="sxs-lookup"><span data-stu-id="10638-128">This property defines the layout orientation for the social media items.</span></span> |

## <a name="social-share-item-module-properties"></a><span data-ttu-id="10638-129">Eiginleikaeiningar samfélagsmiðlaeiningar</span><span class="sxs-lookup"><span data-stu-id="10638-129">Social share item module properties</span></span>
| <span data-ttu-id="10638-130">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="10638-130">Property name</span></span>             | <span data-ttu-id="10638-131">Virði</span><span class="sxs-lookup"><span data-stu-id="10638-131">Value</span></span>                 | <span data-ttu-id="10638-132">lýsing</span><span class="sxs-lookup"><span data-stu-id="10638-132">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="10638-133">Netsamfélög</span><span class="sxs-lookup"><span data-stu-id="10638-133">Social media</span></span>              | <span data-ttu-id="10638-134">**Facebook** , **Twitter** , **Pinterest** , **LinkedIn** , **Mail**</span><span class="sxs-lookup"><span data-stu-id="10638-134">**Facebook** , **Twitter** , **Pinterest** , **LinkedIn** , **Mail**</span></span> | <span data-ttu-id="10638-135">Fellivalmynd með lista yfir samfélagsmiðla.</span><span class="sxs-lookup"><span data-stu-id="10638-135">A drop-down menu with a list of social media platforms.</span></span> |
| <span data-ttu-id="10638-136">Tákn</span><span class="sxs-lookup"><span data-stu-id="10638-136">Icon</span></span> |<span data-ttu-id="10638-137">Mynd</span><span class="sxs-lookup"><span data-stu-id="10638-137">Image</span></span>    | <span data-ttu-id="10638-138">Þetta verður myndin sem birtist fyrir viðkomandi samfélagsmiðil.</span><span class="sxs-lookup"><span data-stu-id="10638-138">This will be the image that will be shown for the respective social media.</span></span> <span data-ttu-id="10638-139">Bestu starfsvenju um notkun mynda fyrir verkvanga er að finna í SDK fyrir verkvang samfélagsmiðilsins.</span><span class="sxs-lookup"><span data-stu-id="10638-139">As a best practice, refer to the social media platform's SDK for the recommended image to use for each platform.</span></span> |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a><span data-ttu-id="10638-140">Bæta samfélagsmiðlaeiningu við kaupgluggaeiningu</span><span class="sxs-lookup"><span data-stu-id="10638-140">Add a social share module to a buy box module</span></span>

<span data-ttu-id="10638-141">Til að bæta við samfélagsmiðlaeiningu við kaupgluggaeiningu skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="10638-141">To add a social share module to a buy box module, follow these steps.</span></span>

1. <span data-ttu-id="10638-142">Á Fabrikam-svæðinu skal velja **Síður** , og síðan velja **DefaulPDP** síðuna til að opna upplýsingasíðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="10638-142">In the Fabrikam site, select **Pages** , and then select the **DefaultPDP** page to open the product details page.</span></span> 
1. <span data-ttu-id="10638-143">Í hólfinu **Kaupgluggi (krafist)** , skal velja úrfellingarmerkið ( **...** ) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="10638-143">In the **Buybox (required)** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="10638-144">Í glugganum **Bæta við einingu** skal velja eininguna **Deila á samfélagsmiðlum** og síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="10638-144">In the **Add Module** dialog box, select the **Social Share** module, and then select **OK**.</span></span>
1. <span data-ttu-id="10638-145">Í hólfinu **Deila á samfélagsmiðlum** , skal velja úrfellingarmerkið ( **...** ) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="10638-145">In the **Social Share** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="10638-146">Í glugganum **Bæta við einingu** skal velja eininguna **SocialShare** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="10638-146">In the **Add Module** dialog box, select the **SocialShare** module, and then select **OK**.</span></span>
1. <span data-ttu-id="10638-147">Á eiginleikasvæðinu í **SocialShare** einingunni, undir **Stefna** , skal velja **Lárétt**.</span><span class="sxs-lookup"><span data-stu-id="10638-147">In the properties pane of the **SocialShare** module, under **Orientation** , select **Horizontal**.</span></span> <span data-ttu-id="10638-148">Bættu við myndatexta eins og nauðsynlegt er.</span><span class="sxs-lookup"><span data-stu-id="10638-148">Add a caption as needed.</span></span>
1. <span data-ttu-id="10638-149">Í hólfinu **SocialShare** , skal velja úrfellingarmerkið ( **...** ) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="10638-149">In the **SocialShare** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="10638-150">Í glugganum **Bæta við einingu** skal velja eininguna **SocialShareItem** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="10638-150">In the **Add Module** dialog box, select the **SocialShareItem** module, and then select **OK**.</span></span>
1. <span data-ttu-id="10638-151">Á eiginleikasvæði **SocialShareItem** einingarinnar, undir **Samfélagsmiðlar** skal velja **Facebook**.</span><span class="sxs-lookup"><span data-stu-id="10638-151">In the properties pane of the **SocialShareItem** module, under **Social Media** , select **Facebook**.</span></span>
1. <span data-ttu-id="10638-152">Á eiginleikasvæði **SocialShareItem** einingarinnar, undir **Tákn** skal velja **+ Bæta við mynd**.</span><span class="sxs-lookup"><span data-stu-id="10638-152">In the properties pane of the **SocialShareItem** module, under **Icon** , select **+ Add an image**.</span></span>
1. <span data-ttu-id="10638-153">Í glugganum **Val á miðli** skal velja Facebook lógómynd og svo **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="10638-153">In the **Media Picker** dialog box, select the Facebook logo image, and then select **OK**.</span></span> <span data-ttu-id="10638-154">Ef engin Facebook-lógómynd er til staðar skal velja **Hlaða upp nýju margmiðlunaratriði** til að hlaða upp einni.</span><span class="sxs-lookup"><span data-stu-id="10638-154">If no Facebook logo image is present, select **Upload new media item** to upload one.</span></span>
1. <span data-ttu-id="10638-155">Bætið við og skilgreinið frekari **SocialShareItem** einingar eins og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="10638-155">Add and configure additional **SocialShareItem** modules as needed.</span></span>
1. <span data-ttu-id="10638-156">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="10638-156">Select **Save** , and then select **Preview** to preview the page.</span></span> <span data-ttu-id="10638-157">Síðan sýnir samfélagsmiðlaeiningu.</span><span class="sxs-lookup"><span data-stu-id="10638-157">The page will show the social share module.</span></span>
1. <span data-ttu-id="10638-158">Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="10638-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="10638-159">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="10638-159">Additional resources</span></span>

[<span data-ttu-id="10638-160">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="10638-160">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="10638-161">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="10638-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="10638-162">Reglufylgni köku</span><span class="sxs-lookup"><span data-stu-id="10638-162">Cookie compliance</span></span>](cookie-compliance.md)
