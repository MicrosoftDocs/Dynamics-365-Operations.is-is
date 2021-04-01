---
title: Kortaeining
description: Þetta efnisatriði fjallar um kortaeiningar og lýsir því hvernig á að skilgreina þær í Microsoft Dynamics 365 Commerce.
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 74991a2979540dab344f39976005250637fab29c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5252583"
---
# <a name="map-module"></a><span data-ttu-id="6d3b7-103">Kortaeining</span><span class="sxs-lookup"><span data-stu-id="6d3b7-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="6d3b7-104">Þetta efnisatriði fjallar um kortaeiningar og lýsir því hvernig á að skilgreina þær í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6d3b7-105">Kortaeining sýnir staðsetningar verslana á gagnvirku korti sem er sett fram með því að nota [Bing Maps V8 vefstýringu](https://docs.microsoft.com/bingmaps/v8-web-control/).</span><span class="sxs-lookup"><span data-stu-id="6d3b7-105">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="6d3b7-106">API-lykill Bing-korta er nauðsynlegur og verður að bæta honum við samnýtta færibreytusíðu í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-106">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="6d3b7-107">Kortaeiningar bjóða upp á mismunandi sjónarhorn, t.d. af vegi, úr lofti og af götunni, sem notendur geta valið til að skoða kortastaðsetningar.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-107">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="6d3b7-108">Þær leyfa einnig aðgerðir eins og aðdrátt og nota staðsetningu notanda.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-108">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="6d3b7-109">Kortaeining vinnur með verslunarvalseiningunni til að ákvarða landfræðilegar staðsetningar á verslunum sem sýna þarf á korti.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-109">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="6d3b7-110">Verslunarvals- og kortaeiningar vinna saman þegar notandi velur verslun í annarri hvorri einingunni á svæði síðu.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-110">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="6d3b7-111">Hægt er að nota kortaeiningar í öðrum aðstæðum, sem tengjast ekki verslunarvalseiningum.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-111">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="6d3b7-112">Hins vegar er sérstilling einingar nauðsynleg.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-112">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="6d3b7-113">Kortaeiningin er tiltæk í Dynamics 365 Commerce útgáfu 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-113">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="6d3b7-114">Eftirfarandi mynd sýnir dæmi um kortaeiningu sem er notuð á staðsetningarsíðu verslunar.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-114">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Dæmi um verslunarvalseiningu](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="6d3b7-116">Eiginleikar einingar</span><span class="sxs-lookup"><span data-stu-id="6d3b7-116">Module properties</span></span>

| <span data-ttu-id="6d3b7-117">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="6d3b7-117">Property name</span></span>             | <span data-ttu-id="6d3b7-118">Virði</span><span class="sxs-lookup"><span data-stu-id="6d3b7-118">Value</span></span>                 | <span data-ttu-id="6d3b7-119">lýsing</span><span class="sxs-lookup"><span data-stu-id="6d3b7-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="6d3b7-120">Yfirskrift</span><span class="sxs-lookup"><span data-stu-id="6d3b7-120">Heading</span></span> | <span data-ttu-id="6d3b7-121">Texti</span><span class="sxs-lookup"><span data-stu-id="6d3b7-121">Text</span></span> | <span data-ttu-id="6d3b7-122">Fyrirsögn einingarinnar.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-122">The heading for the module.</span></span> |
| <span data-ttu-id="6d3b7-123">Valkostir teiknibólu: Sjálfgefið tákn</span><span class="sxs-lookup"><span data-stu-id="6d3b7-123">Pushpin options: Default icon</span></span> | <span data-ttu-id="6d3b7-124">Mynd</span><span class="sxs-lookup"><span data-stu-id="6d3b7-124">Image</span></span> | <span data-ttu-id="6d3b7-125">Myndatákn teiknibólunnar sem er notaðfyrir verslanir sem sjást á korti.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-125">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="6d3b7-126">Valkostir teiknibólu: Virkt tákn</span><span class="sxs-lookup"><span data-stu-id="6d3b7-126">Pushpin options: Active icon</span></span> | <span data-ttu-id="6d3b7-127">Mynd</span><span class="sxs-lookup"><span data-stu-id="6d3b7-127">Image</span></span> | <span data-ttu-id="6d3b7-128">Myndatákn teiknibólunnar sem er notað fyrir verslun sem er valin á korti.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-128">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="6d3b7-129">Valkostir teiknibólu: Sjálfgefinn litur tákns</span><span class="sxs-lookup"><span data-stu-id="6d3b7-129">Pushpin options: Default icon color</span></span> | <span data-ttu-id="6d3b7-130">Stafastrengur</span><span class="sxs-lookup"><span data-stu-id="6d3b7-130">Character string</span></span> | <span data-ttu-id="6d3b7-131">Textinn eða sextándakerfisgildið fyrir litinn á teiknibólutákni á korti.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-131">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="6d3b7-132">Valkostir teiknibólu: Litur virks tákns</span><span class="sxs-lookup"><span data-stu-id="6d3b7-132">Pushpin options: Active icon color</span></span> | <span data-ttu-id="6d3b7-133">Stafastrengur</span><span class="sxs-lookup"><span data-stu-id="6d3b7-133">Character string</span></span> | <span data-ttu-id="6d3b7-134">Textinn eða sextándakerfisgildið fyrir litinn á völdu teiknibólutákni á korti.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-134">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="6d3b7-135">Sýna atriðaskrá</span><span class="sxs-lookup"><span data-stu-id="6d3b7-135">Show index</span></span> | <span data-ttu-id="6d3b7-136">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="6d3b7-136">**True** or **False**</span></span> | <span data-ttu-id="6d3b7-137">Ef þessi eiginleiki er stilltur á **Satt**, sýna öll teiknibólutákn sem standa fyrir verslun atriðaskrá.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-137">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="6d3b7-138">Þessi atriðaskrá samsvarar atriðaskránni í listayfirlitinu sem verslunarvalseiningin sýnir.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-138">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="6d3b7-139">Bæta leyfðum kortavefslóðum við öryggisleiðbeiningar um innihald vefsvæðis</span><span class="sxs-lookup"><span data-stu-id="6d3b7-139">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="6d3b7-140">Til þess að kortaeining geti unnið með Bing-korti, þarf að ganga úr skugga um að eftirfarandi kortavefslóðir séu leyfðar í öryggisreglum vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-140">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="6d3b7-141">Þessi uppsetning er gerð í Commerce-vefsmiðnum með því að bæta leyfðum vefslóðum við ýmsar öryggisleiðbeiningar vefsvæðis (t.d. **img-src**).</span><span class="sxs-lookup"><span data-stu-id="6d3b7-141">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="6d3b7-142">Nánari upplýsingar er að finna í [Öryggisregla um innihald](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="6d3b7-142">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="6d3b7-143">Í leiðbeininguna **connect-src** skal bæta við **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-143">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="6d3b7-144">Í leiðbeininguna **img-src** skal bæta við **&#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-144">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="6d3b7-145">Í leiðbeininguna **script-src** skal bæta við **&#42;.bing.com, &#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-145">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="6d3b7-146">Í leiðbeininguna **script style-src** skal bæta við **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="6d3b7-146">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="6d3b7-147">Bæta kortaeiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="6d3b7-147">Add a map module to a page</span></span>

<span data-ttu-id="6d3b7-148">Ítarlegar upplýsingar um hvernig á að skilgreina kortaeiningu á síðu er að finna í [Eining til að velja verslun](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="6d3b7-148">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="6d3b7-149">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="6d3b7-149">Additional resources</span></span>

[<span data-ttu-id="6d3b7-150">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="6d3b7-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6d3b7-151">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="6d3b7-151">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="6d3b7-152">Körfueining</span><span class="sxs-lookup"><span data-stu-id="6d3b7-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="6d3b7-153">Eining til að velja verslun</span><span class="sxs-lookup"><span data-stu-id="6d3b7-153">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="6d3b7-154">Stjórna Bing-kortum fyrir þitt fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="6d3b7-154">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="6d3b7-155">Bing-kort V8 Vefstýringar</span><span class="sxs-lookup"><span data-stu-id="6d3b7-155">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]