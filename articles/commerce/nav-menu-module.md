---
title: Eining yfirlitsvalmyndar
description: Þetta efnisatriði fjallar um einingar yfirlitsvalmyndar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/01/2020
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
ms.openlocfilehash: b0e8168ca9ec9ca68011650a73cc09983deca645
ms.sourcegitcommit: eee3523be26369aecdb36c0143a6ee3dab4b7966
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/20/2020
ms.locfileid: "4413295"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="b85dd-103">Eining yfirlitsvalmyndar</span><span class="sxs-lookup"><span data-stu-id="b85dd-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b85dd-104">Þetta efnisatriði fjallar um einingar yfirlitsvalmyndar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b85dd-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b85dd-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="b85dd-105">Overview</span></span>

<span data-ttu-id="b85dd-106">Aðaltilgangurinn einingar yfirlitsvalmyndar er að leyfa notendum vefsvæða að skoða vörur og síður samkvæmt yfirlitsstigveldi rásar sem er skilgreint í Dynamics 365 Commerce höfuðstöðvum.</span><span class="sxs-lookup"><span data-stu-id="b85dd-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="b85dd-107">Vörur sem eru skilgreindar í einingu yfirlitsvalmyndar birtast sem yfirlit síðuhauss.</span><span class="sxs-lookup"><span data-stu-id="b85dd-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="b85dd-108">Einingar yfirlitsvalmyndar styðja einnig föst valmyndaratriði sem tengjast öðrum síðum á e-Commerce svæði.</span><span class="sxs-lookup"><span data-stu-id="b85dd-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="b85dd-109">Hægt er að bæta einingu yfirlitsvalmyndar í hauseiningu síðu.</span><span class="sxs-lookup"><span data-stu-id="b85dd-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="b85dd-110">Í Fabrikam-þema sýnir yfirlitsvalmynd sjálfgefið tvö stig.</span><span class="sxs-lookup"><span data-stu-id="b85dd-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="b85dd-111">Í Upphafsþema sýnir yfirlitsvalmynd sjálfgefið tvö stig.</span><span class="sxs-lookup"><span data-stu-id="b85dd-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="b85dd-112">Til að breyta fjölda stiga er skoðunarviðbót nauðsynleg við þemað.</span><span class="sxs-lookup"><span data-stu-id="b85dd-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="b85dd-113">Eftirfarandi mynd sýnir dæmi um yfirlitsvalmynd fyrir Fabrikam-svæðið með tveimur stigum tegundastigveldis og nokkrum föstum valmyndaratriðum.</span><span class="sxs-lookup"><span data-stu-id="b85dd-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="b85dd-114">![Dæmi um einingu yfirlitsvalmyndar](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="b85dd-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="b85dd-115">Eiginleikar einingar yfirlitsvalmyndar</span><span class="sxs-lookup"><span data-stu-id="b85dd-115">Navigation menu module properties</span></span>

| <span data-ttu-id="b85dd-116">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="b85dd-116">Property name</span></span>             | <span data-ttu-id="b85dd-117">Virði</span><span class="sxs-lookup"><span data-stu-id="b85dd-117">Value</span></span>                 | <span data-ttu-id="b85dd-118">lýsing</span><span class="sxs-lookup"><span data-stu-id="b85dd-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="b85dd-119">Uppruni</span><span class="sxs-lookup"><span data-stu-id="b85dd-119">Source</span></span>                  | <span data-ttu-id="b85dd-120">**Retail**, **Handvirk höfundarvinna**, **Retail og handvirk höfundarvinna**</span><span class="sxs-lookup"><span data-stu-id="b85dd-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="b85dd-121">**Retail**-gildið leyfir birtingu yfirlitsstigveldi rásarinnar úr Commerce Headquarters í yfirlitsvalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="b85dd-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="b85dd-122">**Handvirk höfundarvinna**-gildi leyfir umsjón með föstum valmyndaratriðum.</span><span class="sxs-lookup"><span data-stu-id="b85dd-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="b85dd-123">**Retail og handvirk höfundarvinna** leyfir blöndu af hvoru tveggja.</span><span class="sxs-lookup"><span data-stu-id="b85dd-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="b85dd-124">Sýna flokkamyndir</span><span class="sxs-lookup"><span data-stu-id="b85dd-124">Show category images</span></span> | <span data-ttu-id="b85dd-125">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="b85dd-125">**True** or **False**</span></span>    | <span data-ttu-id="b85dd-126">Þegar þetta er virkt birtir þessi eiginleiki flokkamyndir á yfirlitsvalmyndinni eins og skilgreint er í höfuðstöðvum Commerce fyrir hvern flokk.</span><span class="sxs-lookup"><span data-stu-id="b85dd-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="b85dd-127">Bætt við í Commerce Release 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="b85dd-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="b85dd-128">Virkja stigskipta yfirlitsvalmynd</span><span class="sxs-lookup"><span data-stu-id="b85dd-128">Enable multi-level navigation menu</span></span> | <span data-ttu-id="b85dd-129">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="b85dd-129">**True** or **False**</span></span> | <span data-ttu-id="b85dd-130">Þegar þessi eiginleiki er virkur getur yfirlitsvalmynd sýnt mörg stig yfirlitsstigveldis.</span><span class="sxs-lookup"><span data-stu-id="b85dd-130">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="b85dd-131">Þessi eiginleiki er fáanlegur í Dynamics 365 Commerce útgáfu 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="b85dd-131">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="b85dd-132">Stigafjöldi</span><span class="sxs-lookup"><span data-stu-id="b85dd-132">Number of levels</span></span> | <span data-ttu-id="b85dd-133">heiltala</span><span class="sxs-lookup"><span data-stu-id="b85dd-133">integer</span></span> | <span data-ttu-id="b85dd-134">Þessi eiginleiki skilgreinir fjölda stiga sem á að sýna ef **Virkja stigskipta yfirlitsvalmynd** eiginleikinn er stilltur á **Satt**.</span><span class="sxs-lookup"><span data-stu-id="b85dd-134">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="b85dd-135">Fast valmyndaratriði</span><span class="sxs-lookup"><span data-stu-id="b85dd-135">Static menu item</span></span>| <span data-ttu-id="b85dd-136">Fylki gilda</span><span class="sxs-lookup"><span data-stu-id="b85dd-136">Array of values</span></span>| <span data-ttu-id="b85dd-137">Föst valmyndaratriði sem tengja heiti valmyndaratriðis við tengil á fasta síðu vefsvæða.</span><span class="sxs-lookup"><span data-stu-id="b85dd-137">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="b85dd-138">Hægt er að búa til valmyndaratriði fyrir neðan önnur valmyndaratriði.</span><span class="sxs-lookup"><span data-stu-id="b85dd-138">You can create menu items below other menu items.</span></span> <span data-ttu-id="b85dd-139">Fastar valmyndir birtast sjálfkrafa á rótarstigi og þeim verður bætt við yfirlitsstigveldi rásar ef það er til staðar.</span><span class="sxs-lookup"><span data-stu-id="b85dd-139">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="b85dd-140">Sýna rótarvalmynd</span><span class="sxs-lookup"><span data-stu-id="b85dd-140">Show root menu</span></span> | <span data-ttu-id="b85dd-141">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="b85dd-141">**True** or **False**</span></span> | <span data-ttu-id="b85dd-142">Þegar þessi eiginleiki er virkur er hægt að skilgreina yfirlitsvalmynd undir sérstilltri rót (til dæmis **Versla núna**).</span><span class="sxs-lookup"><span data-stu-id="b85dd-142">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now**).</span></span> <span data-ttu-id="b85dd-143">Þessi eiginleiki er fáanlegur í Dynamics 365 Commerce útgáfu 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="b85dd-143">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="b85dd-144">Rótarvalmynd</span><span class="sxs-lookup"><span data-stu-id="b85dd-144">Root menu</span></span> | <span data-ttu-id="b85dd-145">strengur</span><span class="sxs-lookup"><span data-stu-id="b85dd-145">string</span></span> | <span data-ttu-id="b85dd-146">Hægt er að nota þennan eiginleika til að skilgreina texta fyrir sérstillta rót ef **Sýna rótarvalmynd** eiginleikinn er stillt á **Satt**.</span><span class="sxs-lookup"><span data-stu-id="b85dd-146">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="b85dd-147">Eftirfarandi mynd sýnir dæmi um tegund myndar sem birtist á yfirlitsvalmyndinni fyrir Fabrikam-svæðið.</span><span class="sxs-lookup"><span data-stu-id="b85dd-147">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="b85dd-148">![Dæmi um einingu yfirlitsvalmyndar með flokkamyndum](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="b85dd-148">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="b85dd-149">Bæta einingu yfirlitsvalmyndar við hauseiningu</span><span class="sxs-lookup"><span data-stu-id="b85dd-149">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="b85dd-150">Frekari upplýsingar um hvernig á að bæta við einingu yfirlitsvalmyndar í hauseiningu er að finna í [Hauseining](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="b85dd-150">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b85dd-151">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b85dd-151">Additional resources</span></span>

[<span data-ttu-id="b85dd-152">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="b85dd-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b85dd-153">Brauðmylsnueining</span><span class="sxs-lookup"><span data-stu-id="b85dd-153">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="b85dd-154">Svæðisvalseining</span><span class="sxs-lookup"><span data-stu-id="b85dd-154">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="b85dd-155">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="b85dd-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b85dd-156">Reglufylgni köku</span><span class="sxs-lookup"><span data-stu-id="b85dd-156">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="b85dd-157">Eining síðuhauss</span><span class="sxs-lookup"><span data-stu-id="b85dd-157">Header module</span></span>](author-header-module.md)
