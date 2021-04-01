---
title: Eining yfirlitsvalmyndar
description: Þetta efnisatriði fjallar um einingar yfirlitsvalmyndar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
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
ms.openlocfilehash: f3461993e2bd59d66be1640331e4ef315a078469
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251212"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="7c032-103">Eining yfirlitsvalmyndar</span><span class="sxs-lookup"><span data-stu-id="7c032-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="7c032-104">Þetta efnisatriði fjallar um einingar yfirlitsvalmyndar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7c032-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7c032-105">Aðaltilgangurinn einingar yfirlitsvalmyndar er að leyfa notendum vefsvæða að skoða vörur og síður samkvæmt yfirlitsstigveldi rásar sem er skilgreint í Dynamics 365 Commerce höfuðstöðvum.</span><span class="sxs-lookup"><span data-stu-id="7c032-105">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="7c032-106">Vörur sem eru skilgreindar í einingu yfirlitsvalmyndar birtast sem yfirlit síðuhauss.</span><span class="sxs-lookup"><span data-stu-id="7c032-106">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="7c032-107">Einingar yfirlitsvalmyndar styðja einnig föst valmyndaratriði sem tengjast öðrum síðum á e-Commerce svæði.</span><span class="sxs-lookup"><span data-stu-id="7c032-107">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="7c032-108">Hægt er að bæta einingu yfirlitsvalmyndar í hauseiningu síðu.</span><span class="sxs-lookup"><span data-stu-id="7c032-108">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="7c032-109">Í Fabrikam-þema sýnir yfirlitsvalmynd sjálfgefið tvö stig.</span><span class="sxs-lookup"><span data-stu-id="7c032-109">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="7c032-110">Í Upphafsþema sýnir yfirlitsvalmynd sjálfgefið tvö stig.</span><span class="sxs-lookup"><span data-stu-id="7c032-110">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="7c032-111">Til að breyta fjölda stiga er skoðunarviðbót nauðsynleg við þemað.</span><span class="sxs-lookup"><span data-stu-id="7c032-111">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="7c032-112">Eftirfarandi mynd sýnir dæmi um yfirlitsvalmynd fyrir Fabrikam-svæðið með tveimur stigum tegundastigveldis og nokkrum föstum valmyndaratriðum.</span><span class="sxs-lookup"><span data-stu-id="7c032-112">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="7c032-113">![Dæmi um einingu yfirlitsvalmyndar](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="7c032-113">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="7c032-114">Eiginleikar einingar yfirlitsvalmyndar</span><span class="sxs-lookup"><span data-stu-id="7c032-114">Navigation menu module properties</span></span>

| <span data-ttu-id="7c032-115">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="7c032-115">Property name</span></span>             | <span data-ttu-id="7c032-116">Virði</span><span class="sxs-lookup"><span data-stu-id="7c032-116">Value</span></span>                 | <span data-ttu-id="7c032-117">lýsing</span><span class="sxs-lookup"><span data-stu-id="7c032-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="7c032-118">Uppruni</span><span class="sxs-lookup"><span data-stu-id="7c032-118">Source</span></span>                  | <span data-ttu-id="7c032-119">**Retail**, **Handvirk höfundarvinna**, **Retail og handvirk höfundarvinna**</span><span class="sxs-lookup"><span data-stu-id="7c032-119">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="7c032-120">**Retail**-gildið leyfir birtingu yfirlitsstigveldi rásarinnar úr Commerce Headquarters í yfirlitsvalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="7c032-120">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="7c032-121">**Handvirk höfundarvinna**-gildi leyfir umsjón með föstum valmyndaratriðum.</span><span class="sxs-lookup"><span data-stu-id="7c032-121">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="7c032-122">**Retail og handvirk höfundarvinna** leyfir blöndu af hvoru tveggja.</span><span class="sxs-lookup"><span data-stu-id="7c032-122">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="7c032-123">Sýna flokkamyndir</span><span class="sxs-lookup"><span data-stu-id="7c032-123">Show category images</span></span> | <span data-ttu-id="7c032-124">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="7c032-124">**True** or **False**</span></span>    | <span data-ttu-id="7c032-125">Þegar þetta er virkt birtir þessi eiginleiki flokkamyndir á yfirlitsvalmyndinni eins og skilgreint er í höfuðstöðvum Commerce fyrir hvern flokk.</span><span class="sxs-lookup"><span data-stu-id="7c032-125">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="7c032-126">Bætt við í Commerce Release 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="7c032-126">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="7c032-127">Sýna kynningartilboð</span><span class="sxs-lookup"><span data-stu-id="7c032-127">Show promotions</span></span> | <span data-ttu-id="7c032-128">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="7c032-128">**True** or **False**</span></span> | <span data-ttu-id="7c032-129">Þegar þessi eiginleiki er virkur er hægt að grunnstilla kynningartilboð með því að nota myndir, tengla og texta.</span><span class="sxs-lookup"><span data-stu-id="7c032-129">When this property is enabled, promotions can be configured by using images, links, and text.</span></span> <span data-ttu-id="7c032-130">Þessum eiginleika var bætt við í Commerce útgáfu 10.0.17.</span><span class="sxs-lookup"><span data-stu-id="7c032-130">This property was added in the Commerce version 10.0.17 release.</span></span> |
| <span data-ttu-id="7c032-131">Bæta við stöðuhækkunum</span><span class="sxs-lookup"><span data-stu-id="7c032-131">Add promotions</span></span> | <span data-ttu-id="7c032-132">Texti, mynd eða tengill</span><span class="sxs-lookup"><span data-stu-id="7c032-132">Text, image, or link</span></span> | <span data-ttu-id="7c032-133">Þegar **Sýna kynningartilboð** er virkur er hægt að bæta við texta, mynd eða tengli sem kynningarefni á yfirlitsvalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="7c032-133">When the **Show promotions** property is enabled, you can add text, an image, or a link as promotional content on the navigation menu.</span></span> |
| <span data-ttu-id="7c032-134">Virkja stigskipta yfirlitsvalmynd</span><span class="sxs-lookup"><span data-stu-id="7c032-134">Enable multi-level navigation menu</span></span> | <span data-ttu-id="7c032-135">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="7c032-135">**True** or **False**</span></span> | <span data-ttu-id="7c032-136">Þegar þessi eiginleiki er virkur getur yfirlitsvalmynd sýnt mörg stig yfirlitsstigveldis.</span><span class="sxs-lookup"><span data-stu-id="7c032-136">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="7c032-137">Þessi eiginleiki er í boði í Commerce útgáfu 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="7c032-137">This feature is available in the Commerce version 10.0.15 release.</span></span> |
| <span data-ttu-id="7c032-138">Stigafjöldi</span><span class="sxs-lookup"><span data-stu-id="7c032-138">Number of levels</span></span> | <span data-ttu-id="7c032-139">heiltala</span><span class="sxs-lookup"><span data-stu-id="7c032-139">integer</span></span> | <span data-ttu-id="7c032-140">Þessi eiginleiki skilgreinir fjölda stiga sem á að sýna ef **Virkja stigskipta yfirlitsvalmynd** eiginleikinn er stilltur á **Satt**.</span><span class="sxs-lookup"><span data-stu-id="7c032-140">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="7c032-141">Fast valmyndaratriði</span><span class="sxs-lookup"><span data-stu-id="7c032-141">Static menu item</span></span>| <span data-ttu-id="7c032-142">Fylki gilda</span><span class="sxs-lookup"><span data-stu-id="7c032-142">Array of values</span></span>| <span data-ttu-id="7c032-143">Föst valmyndaratriði sem tengja heiti valmyndaratriðis við tengil á fasta síðu vefsvæða.</span><span class="sxs-lookup"><span data-stu-id="7c032-143">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="7c032-144">Hægt er að búa til valmyndaratriði fyrir neðan önnur valmyndaratriði.</span><span class="sxs-lookup"><span data-stu-id="7c032-144">You can create menu items below other menu items.</span></span> <span data-ttu-id="7c032-145">Fastar valmyndir birtast sjálfkrafa á rótarstigi og þeim verður bætt við yfirlitsstigveldi rásar ef það er til staðar.</span><span class="sxs-lookup"><span data-stu-id="7c032-145">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="7c032-146">Sýna rótarvalmynd</span><span class="sxs-lookup"><span data-stu-id="7c032-146">Show root menu</span></span> | <span data-ttu-id="7c032-147">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="7c032-147">**True** or **False**</span></span> | <span data-ttu-id="7c032-148">Þegar þessi eiginleiki er virkur er hægt að skilgreina yfirlitsvalmynd undir sérstilltri rót (til dæmis **Versla núna**).</span><span class="sxs-lookup"><span data-stu-id="7c032-148">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now**).</span></span> <span data-ttu-id="7c032-149">Þessi eiginleiki er fáanlegur í Dynamics 365 Commerce útgáfu 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="7c032-149">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="7c032-150">Rótarvalmynd</span><span class="sxs-lookup"><span data-stu-id="7c032-150">Root menu</span></span> | <span data-ttu-id="7c032-151">strengur</span><span class="sxs-lookup"><span data-stu-id="7c032-151">string</span></span> | <span data-ttu-id="7c032-152">Hægt er að nota þennan eiginleika til að skilgreina texta fyrir sérstillta rót ef **Sýna rótarvalmynd** eiginleikinn er stillt á **Satt**.</span><span class="sxs-lookup"><span data-stu-id="7c032-152">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="7c032-153">Eftirfarandi mynd sýnir dæmi um tegund myndar sem birtist á yfirlitsvalmyndinni fyrir Fabrikam-svæðið.</span><span class="sxs-lookup"><span data-stu-id="7c032-153">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="7c032-154">![Dæmi um einingu yfirlitsvalmyndar með flokkamyndum](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="7c032-154">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="7c032-155">Bæta einingu yfirlitsvalmyndar við hauseiningu</span><span class="sxs-lookup"><span data-stu-id="7c032-155">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="7c032-156">Frekari upplýsingar um hvernig á að bæta við einingu yfirlitsvalmyndar í hauseiningu er að finna í [Hauseining](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="7c032-156">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7c032-157">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7c032-157">Additional resources</span></span>

[<span data-ttu-id="7c032-158">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="7c032-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7c032-159">Brauðmylsnueining</span><span class="sxs-lookup"><span data-stu-id="7c032-159">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="7c032-160">Svæðisvalseining</span><span class="sxs-lookup"><span data-stu-id="7c032-160">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="7c032-161">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="7c032-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="7c032-162">Reglufylgni köku</span><span class="sxs-lookup"><span data-stu-id="7c032-162">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="7c032-163">Eining síðuhauss</span><span class="sxs-lookup"><span data-stu-id="7c032-163">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]