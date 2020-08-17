---
title: Kortaeining
description: Þetta efnisatriði fjallar um kortaeiningar og lýsir því hvernig á að skilgreina þær í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: a0f5d902289c5867095e34a135c50d342f3c4f13
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646960"
---
# <a name="map-module"></a><span data-ttu-id="e7964-103">Kortaeining</span><span class="sxs-lookup"><span data-stu-id="e7964-103">Map module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="e7964-104">Þetta efnisatriði fjallar um kortaeiningar og lýsir því hvernig á að skilgreina þær í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e7964-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e7964-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="e7964-105">Overview</span></span>

<span data-ttu-id="e7964-106">Kortaeining sýnir staðsetningar verslana á gagnvirku korti sem er sett fram með því að nota [Bing Maps V8 vefstýringu](https://docs.microsoft.com/bingmaps/v8-web-control/).</span><span class="sxs-lookup"><span data-stu-id="e7964-106">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="e7964-107">API-lykill Bing-korta er nauðsynlegur og verður að bæta honum við samnýtta færibreytusíðu í Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="e7964-107">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="e7964-108">Kortaeiningar bjóða upp á mismunandi sjónarhorn, t.d. af vegi, úr lofti og af götunni, sem notendur geta valið til að skoða kortastaðsetningar.</span><span class="sxs-lookup"><span data-stu-id="e7964-108">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="e7964-109">Þær leyfa einnig aðgerðir eins og aðdrátt og nota staðsetningu notanda.</span><span class="sxs-lookup"><span data-stu-id="e7964-109">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="e7964-110">Kortaeining vinnur með verslunarvalseiningunni til að ákvarða landfræðilegar staðsetningar á verslunum sem sýna þarf á korti.</span><span class="sxs-lookup"><span data-stu-id="e7964-110">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="e7964-111">Verslunarvals- og kortaeiningar vinna saman þegar notandi velur verslun í annarri hvorri einingunni á svæði síðu.</span><span class="sxs-lookup"><span data-stu-id="e7964-111">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="e7964-112">Hægt er að nota kortaeiningar í öðrum aðstæðum, sem tengjast ekki verslunarvalseiningum.</span><span class="sxs-lookup"><span data-stu-id="e7964-112">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="e7964-113">Hins vegar er sérstilling einingar nauðsynleg.</span><span class="sxs-lookup"><span data-stu-id="e7964-113">However, module customization is required.</span></span>

<span data-ttu-id="e7964-114">Kortaeiningin var kynnt til sögunnar í Commerce, útgáfu 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="e7964-114">The map module was introduced in Commerce version 10.0.13.</span></span>

<span data-ttu-id="e7964-115">Eftirfarandi mynd sýnir dæmi um kortaeiningu sem er notuð á staðsetningarsíðu verslunar.</span><span class="sxs-lookup"><span data-stu-id="e7964-115">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Dæmi um verslunarvalseiningu](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="e7964-117">Eiginleikar einingar</span><span class="sxs-lookup"><span data-stu-id="e7964-117">Module properties</span></span>

| <span data-ttu-id="e7964-118">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="e7964-118">Property name</span></span>             | <span data-ttu-id="e7964-119">Virði</span><span class="sxs-lookup"><span data-stu-id="e7964-119">Value</span></span>                 | <span data-ttu-id="e7964-120">lýsing</span><span class="sxs-lookup"><span data-stu-id="e7964-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="e7964-121">Yfirskrift</span><span class="sxs-lookup"><span data-stu-id="e7964-121">Heading</span></span> | <span data-ttu-id="e7964-122">Texti</span><span class="sxs-lookup"><span data-stu-id="e7964-122">Text</span></span> | <span data-ttu-id="e7964-123">Fyrirsögn einingarinnar.</span><span class="sxs-lookup"><span data-stu-id="e7964-123">The heading for the module.</span></span> |
| <span data-ttu-id="e7964-124">Valkostir teiknibólu: Sjálfgefið tákn</span><span class="sxs-lookup"><span data-stu-id="e7964-124">Pushpin options: Default icon</span></span> | <span data-ttu-id="e7964-125">Mynd</span><span class="sxs-lookup"><span data-stu-id="e7964-125">Image</span></span> | <span data-ttu-id="e7964-126">Myndatákn teiknibólunnar sem er notaðfyrir verslanir sem sjást á korti.</span><span class="sxs-lookup"><span data-stu-id="e7964-126">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="e7964-127">Valkostir teiknibólu: Virkt tákn</span><span class="sxs-lookup"><span data-stu-id="e7964-127">Pushpin options: Active icon</span></span> | <span data-ttu-id="e7964-128">Mynd</span><span class="sxs-lookup"><span data-stu-id="e7964-128">Image</span></span> | <span data-ttu-id="e7964-129">Myndatákn teiknibólunnar sem er notað fyrir verslun sem er valin á korti.</span><span class="sxs-lookup"><span data-stu-id="e7964-129">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="e7964-130">Valkostir teiknibólu: Sjálfgefinn litur tákns</span><span class="sxs-lookup"><span data-stu-id="e7964-130">Pushpin options: Default icon color</span></span> | <span data-ttu-id="e7964-131">Stafastrengur</span><span class="sxs-lookup"><span data-stu-id="e7964-131">Character string</span></span> | <span data-ttu-id="e7964-132">Textinn eða sextándakerfisgildið fyrir litinn á teiknibólutákni á korti.</span><span class="sxs-lookup"><span data-stu-id="e7964-132">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="e7964-133">Valkostir teiknibólu: Litur virks tákns</span><span class="sxs-lookup"><span data-stu-id="e7964-133">Pushpin options: Active icon color</span></span> | <span data-ttu-id="e7964-134">Stafastrengur</span><span class="sxs-lookup"><span data-stu-id="e7964-134">Character string</span></span> | <span data-ttu-id="e7964-135">Textinn eða sextándakerfisgildið fyrir litinn á völdu teiknibólutákni á korti.</span><span class="sxs-lookup"><span data-stu-id="e7964-135">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="e7964-136">Sýna atriðaskrá</span><span class="sxs-lookup"><span data-stu-id="e7964-136">Show index</span></span> | <span data-ttu-id="e7964-137">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="e7964-137">**True** or **False**</span></span> | <span data-ttu-id="e7964-138">Ef þessi eiginleiki er stilltur á **Satt**, sýna öll teiknibólutákn sem standa fyrir verslun atriðaskrá.</span><span class="sxs-lookup"><span data-stu-id="e7964-138">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="e7964-139">Þessi atriðaskrá samsvarar atriðaskránni í listayfirlitinu sem verslunarvalseiningin sýnir.</span><span class="sxs-lookup"><span data-stu-id="e7964-139">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="e7964-140">Bæta leyfðum kortavefslóðum við öryggisleiðbeiningar um innihald vefsvæðis</span><span class="sxs-lookup"><span data-stu-id="e7964-140">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="e7964-141">Til þess að kortaeining geti unnið með Bing-korti, þarf að ganga úr skugga um að eftirfarandi kortavefslóðir séu leyfðar (einnig þekkt sem „undanþágulisti“) í öryggisreglum vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="e7964-141">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed (also known as "whitelisted") per your site's content security policy (CSP).</span></span> <span data-ttu-id="e7964-142">Þessi uppsetning er gerð í Commerce-vefsmiðnum með því að bæta leyfðum vefslóðum við ýmsar öryggisleiðbeiningar vefsvæðis (t.d. **img-src**).</span><span class="sxs-lookup"><span data-stu-id="e7964-142">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="e7964-143">Nánari upplýsingar er að finna í [Öryggisregla um innihald](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="e7964-143">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="e7964-144">Í leiðbeininguna **connect-src** skal bæta við **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="e7964-144">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="e7964-145">Í leiðbeininguna **img-src** skal bæta við **&#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="e7964-145">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="e7964-146">Í leiðbeininguna **script-src** skal bæta við **&#42;.bing.com, &#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="e7964-146">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="e7964-147">Í leiðbeininguna **script style-src** skal bæta við **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="e7964-147">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="e7964-148">Bæta kortaeiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="e7964-148">Add a map module to a page</span></span>

<span data-ttu-id="e7964-149">Ítarlegar upplýsingar um hvernig á að skilgreina kortaeiningu á síðu er að finna í [Eining til að velja verslun](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="e7964-149">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="e7964-150">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e7964-150">Additional resources</span></span>

[<span data-ttu-id="e7964-151">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="e7964-151">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e7964-152">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="e7964-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e7964-153">Körfueining</span><span class="sxs-lookup"><span data-stu-id="e7964-153">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e7964-154">Vista valeiningu</span><span class="sxs-lookup"><span data-stu-id="e7964-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="e7964-155">Stjórna Bing-kortum fyrir þitt fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="e7964-155">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="e7964-156">Bing-kort V8 Vefstýringar</span><span class="sxs-lookup"><span data-stu-id="e7964-156">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)
