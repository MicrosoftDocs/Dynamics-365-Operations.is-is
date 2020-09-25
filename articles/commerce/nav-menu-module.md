---
title: Eining yfirlitsvalmyndar
description: Þetta efnisatriði fjallar um einingar yfirlitsvalmyndar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 9f66bbe7bf436ab6360dda7d92d6d51e47eedf16
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761397"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="c86df-103">Eining yfirlitsvalmyndar</span><span class="sxs-lookup"><span data-stu-id="c86df-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="c86df-104">Þetta efnisatriði fjallar um einingar yfirlitsvalmyndar og útskýrir hvernig á að bæta þeim við svæðissíður í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c86df-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c86df-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="c86df-105">Overview</span></span>

<span data-ttu-id="c86df-106">Aðaltilgangurinn einingar yfirlitsvalmyndar er að leyfa notendum vefsvæða að skoða vörur og síður samkvæmt yfirlitsstigveldi rásar sem er skilgreint í Dynamics 365 Commerce höfuðstöðvum.</span><span class="sxs-lookup"><span data-stu-id="c86df-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="c86df-107">Vörur sem eru skilgreindar í einingu yfirlitsvalmyndar birtast sem yfirlit síðuhauss.</span><span class="sxs-lookup"><span data-stu-id="c86df-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="c86df-108">Einingar yfirlitsvalmyndar styðja einnig föst valmyndaratriði sem tengjast öðrum síðum á e-Commerce svæði.</span><span class="sxs-lookup"><span data-stu-id="c86df-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="c86df-109">Hægt er að bæta einingu yfirlitsvalmyndar í hauseiningu síðu.</span><span class="sxs-lookup"><span data-stu-id="c86df-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="c86df-110">Í Fabrikam-þema sýnir yfirlitsvalmynd sjálfgefið tvö stig.</span><span class="sxs-lookup"><span data-stu-id="c86df-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="c86df-111">Í Upphafsþema sýnir yfirlitsvalmynd sjálfgefið tvö stig.</span><span class="sxs-lookup"><span data-stu-id="c86df-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="c86df-112">Til að breyta fjölda stiga er skoðunarviðbót nauðsynleg við þemað.</span><span class="sxs-lookup"><span data-stu-id="c86df-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="c86df-113">Eftirfarandi mynd sýnir dæmi um yfirlitsvalmynd fyrir Fabrikam-svæðið með tveimur stigum tegundastigveldis og nokkrum föstum valmyndaratriðum.</span><span class="sxs-lookup"><span data-stu-id="c86df-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="c86df-114">![Dæmi um einingu yfirlitsvalmyndar](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="c86df-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="c86df-115">Eiginleikar einingar yfirlitsvalmyndar</span><span class="sxs-lookup"><span data-stu-id="c86df-115">Navigation menu module properties</span></span>

| <span data-ttu-id="c86df-116">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="c86df-116">Property name</span></span>             | <span data-ttu-id="c86df-117">Virði</span><span class="sxs-lookup"><span data-stu-id="c86df-117">Value</span></span>                 | <span data-ttu-id="c86df-118">lýsing</span><span class="sxs-lookup"><span data-stu-id="c86df-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="c86df-119">Uppruni</span><span class="sxs-lookup"><span data-stu-id="c86df-119">Source</span></span>                  | <span data-ttu-id="c86df-120">**Retail**, **Handvirk höfundarvinna**, **Retail og handvirk höfundarvinna**</span><span class="sxs-lookup"><span data-stu-id="c86df-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="c86df-121">**Retail**-gildið leyfir birtingu yfirlitsstigveldi rásarinnar úr Commerce Headquarters í yfirlitsvalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="c86df-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="c86df-122">**Handvirk höfundarvinna**-gildi leyfir umsjón með föstum valmyndaratriðum.</span><span class="sxs-lookup"><span data-stu-id="c86df-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="c86df-123">**Retail og handvirk höfundarvinna** leyfir blöndu af hvoru tveggja.</span><span class="sxs-lookup"><span data-stu-id="c86df-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="c86df-124">Sýna flokkamyndir</span><span class="sxs-lookup"><span data-stu-id="c86df-124">Show category images</span></span> | <span data-ttu-id="c86df-125">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="c86df-125">**True** or **False**</span></span>    | <span data-ttu-id="c86df-126">Þegar þetta er virkt birtir þessi eiginleiki flokkamyndir á yfirlitsvalmyndinni eins og skilgreint er í höfuðstöðvum Commerce fyrir hvern flokk.</span><span class="sxs-lookup"><span data-stu-id="c86df-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="c86df-127">Bætt við í Commerce Release 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="c86df-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="c86df-128">Fast valmyndaratriði</span><span class="sxs-lookup"><span data-stu-id="c86df-128">Static menu item</span></span>| <span data-ttu-id="c86df-129">Fylki gilda</span><span class="sxs-lookup"><span data-stu-id="c86df-129">Array of values</span></span>| <span data-ttu-id="c86df-130">Föst valmyndaratriði sem tengja heiti valmyndaratriðis við tengil á fasta síðu vefsvæða.</span><span class="sxs-lookup"><span data-stu-id="c86df-130">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="c86df-131">Hægt er að búa til valmyndaratriði fyrir neðan önnur valmyndaratriði.</span><span class="sxs-lookup"><span data-stu-id="c86df-131">You can create menu items below other menu items.</span></span> <span data-ttu-id="c86df-132">Fastar valmyndir birtast sjálfkrafa á rótarstigi og þeim verður bætt við yfirlitsstigveldi rásar ef það er til staðar.</span><span class="sxs-lookup"><span data-stu-id="c86df-132">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |

<span data-ttu-id="c86df-133">Eftirfarandi mynd sýnir dæmi um tegund myndar sem birtist á yfirlitsvalmyndinni fyrir Fabrikam-svæðið.</span><span class="sxs-lookup"><span data-stu-id="c86df-133">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="c86df-134">![Dæmi um einingu yfirlitsvalmyndar með flokkamyndum](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="c86df-134">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="c86df-135">Bæta einingu yfirlitsvalmyndar við hauseiningu</span><span class="sxs-lookup"><span data-stu-id="c86df-135">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="c86df-136">Frekari upplýsingar um hvernig á að bæta við einingu yfirlitsvalmyndar í hauseiningu er að finna í [Hauseining](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="c86df-136">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c86df-137">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c86df-137">Additional resources</span></span>

[<span data-ttu-id="c86df-138">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="c86df-138">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c86df-139">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="c86df-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c86df-140">Reglufylgni köku</span><span class="sxs-lookup"><span data-stu-id="c86df-140">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="c86df-141">Eining síðuhauss</span><span class="sxs-lookup"><span data-stu-id="c86df-141">Header module</span></span>](author-header-module.md)
