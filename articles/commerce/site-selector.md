---
title: Svæðisvalseining
description: Þetta efnisatriði fjallar um svæðisvalseininguna og útskýrir hvernig á að bæta henni við síður á vefsvæði Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.openlocfilehash: bd54695f54b501631f916328c05bfd47e538d50d
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055831"
---
# <a name="site-selector-module"></a><span data-ttu-id="bbeea-103">Svæðisvalseining</span><span class="sxs-lookup"><span data-stu-id="bbeea-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="bbeea-104">Þetta efnisatriði fjallar um svæðisvalseininguna og útskýrir hvernig á að bæta henni við síður á vefsvæði Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bbeea-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bbeea-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="bbeea-105">Overview</span></span>

<span data-ttu-id="bbeea-106">Þegar fyrirtæki er með ólík svæði á mörkuðum, svæði og staðhætti þurfa notendur svæðis að skipta á milli svæða og velja æskilegt verslunarsvæði á einfaldan hátt.</span><span class="sxs-lookup"><span data-stu-id="bbeea-106">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="bbeea-107">Til að mæta þessari atburðarás gerir svæðarvaleiningin kleift að fletta á mörgum svæðum.</span><span class="sxs-lookup"><span data-stu-id="bbeea-107">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="bbeea-108">Grunnkerfi svæðisins verður að skilgreina með lista yfir svæði (markaði, svæði eða svæði) sem notendur svæðisins geta flett í.</span><span class="sxs-lookup"><span data-stu-id="bbeea-108">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="bbeea-109">Svæðisvalseiningin er tiltæk í Dynamics 365 Commerce útgáfu 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="bbeea-109">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="bbeea-110">Eftirfarandi mynd sýnir dæmi um færibreytueiningu sem er valin í haus vefsíðu.</span><span class="sxs-lookup"><span data-stu-id="bbeea-110">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![Dæmi um val á svæðiseiningu í haus vefsíðu](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="bbeea-112">Eiginleikar svæðisvalseiningar</span><span class="sxs-lookup"><span data-stu-id="bbeea-112">Site selector module properties</span></span>

| <span data-ttu-id="bbeea-113">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="bbeea-113">Property name</span></span> | <span data-ttu-id="bbeea-114">Virði</span><span class="sxs-lookup"><span data-stu-id="bbeea-114">Value</span></span>                 | <span data-ttu-id="bbeea-115">lýsing</span><span class="sxs-lookup"><span data-stu-id="bbeea-115">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="bbeea-116">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="bbeea-116">Heading</span></span>       | <span data-ttu-id="bbeea-117">Texti</span><span class="sxs-lookup"><span data-stu-id="bbeea-117">Text</span></span>                  | <span data-ttu-id="bbeea-118">Fyrirsögn einingarinnar.</span><span class="sxs-lookup"><span data-stu-id="bbeea-118">The heading for the module.</span></span> |
| <span data-ttu-id="bbeea-119">Vefsvæðakostir</span><span class="sxs-lookup"><span data-stu-id="bbeea-119">Site options</span></span>  | <span data-ttu-id="bbeea-120">Nafn, mynd, URL</span><span class="sxs-lookup"><span data-stu-id="bbeea-120">Name, Image, URL</span></span>      | <span data-ttu-id="bbeea-121">Þessi eiginleiki tilgreinir heiti, tengil á heimasíðu svæðisins og valfrjálsa mynd til að sýna fyrir hvert svæði sem er tekið með í einingunni.</span><span class="sxs-lookup"><span data-stu-id="bbeea-121">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="bbeea-122">Myndin getur verið flagg eða einhver framsetning á markaði, svæði eða staðháttum.</span><span class="sxs-lookup"><span data-stu-id="bbeea-122">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="bbeea-123">Bæta svæðisvalseiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="bbeea-123">Add a site selector module to a page</span></span>

<span data-ttu-id="bbeea-124">Hægt er að bæta við svæðisvalseiningu í [Hauseiningu](author-header-module.md) undir vali á svæði.</span><span class="sxs-lookup"><span data-stu-id="bbeea-124">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="bbeea-125">Eftir að því er bætt við er hægt að skilgreina fyrirsögn einingar og svæði.</span><span class="sxs-lookup"><span data-stu-id="bbeea-125">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bbeea-126">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="bbeea-126">Additional resources</span></span>

[<span data-ttu-id="bbeea-127">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="bbeea-127">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bbeea-128">Eining síðuhauss</span><span class="sxs-lookup"><span data-stu-id="bbeea-128">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="bbeea-129">Brauðmylsnueining</span><span class="sxs-lookup"><span data-stu-id="bbeea-129">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="bbeea-130">Eining yfirlitsvalmyndar</span><span class="sxs-lookup"><span data-stu-id="bbeea-130">Navigation menu module</span></span>](nav-menu-module.md)
