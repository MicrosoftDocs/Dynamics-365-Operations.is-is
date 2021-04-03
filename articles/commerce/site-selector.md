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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e24590d4a8f172809704aab0d761f6db0fb0e11b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234342"
---
# <a name="site-selector-module"></a><span data-ttu-id="7fced-103">Svæðisvalseining</span><span class="sxs-lookup"><span data-stu-id="7fced-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7fced-104">Þetta efnisatriði fjallar um svæðisvalseininguna og útskýrir hvernig á að bæta henni við síður á vefsvæði Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7fced-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="7fced-105">Þegar fyrirtæki er með ólík svæði á mörkuðum, svæði og staðhætti þurfa notendur svæðis að skipta á milli svæða og velja æskilegt verslunarsvæði á einfaldan hátt.</span><span class="sxs-lookup"><span data-stu-id="7fced-105">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="7fced-106">Til að mæta þessari atburðarás gerir svæðarvaleiningin kleift að fletta á mörgum svæðum.</span><span class="sxs-lookup"><span data-stu-id="7fced-106">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="7fced-107">Grunnkerfi svæðisins verður að skilgreina með lista yfir svæði (markaði, svæði eða svæði) sem notendur svæðisins geta flett í.</span><span class="sxs-lookup"><span data-stu-id="7fced-107">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="7fced-108">Svæðisvalseiningin er tiltæk í Dynamics 365 Commerce útgáfu 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="7fced-108">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="7fced-109">Eftirfarandi mynd sýnir dæmi um færibreytueiningu sem er valin í haus vefsíðu.</span><span class="sxs-lookup"><span data-stu-id="7fced-109">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![Dæmi um val á svæðiseiningu í haus vefsíðu](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="7fced-111">Eiginleikar svæðisvalseiningar</span><span class="sxs-lookup"><span data-stu-id="7fced-111">Site selector module properties</span></span>

| <span data-ttu-id="7fced-112">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="7fced-112">Property name</span></span> | <span data-ttu-id="7fced-113">Virði</span><span class="sxs-lookup"><span data-stu-id="7fced-113">Value</span></span>                 | <span data-ttu-id="7fced-114">lýsing</span><span class="sxs-lookup"><span data-stu-id="7fced-114">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="7fced-115">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="7fced-115">Heading</span></span>       | <span data-ttu-id="7fced-116">Texti</span><span class="sxs-lookup"><span data-stu-id="7fced-116">Text</span></span>                  | <span data-ttu-id="7fced-117">Fyrirsögn einingarinnar.</span><span class="sxs-lookup"><span data-stu-id="7fced-117">The heading for the module.</span></span> |
| <span data-ttu-id="7fced-118">Vefsvæðakostir</span><span class="sxs-lookup"><span data-stu-id="7fced-118">Site options</span></span>  | <span data-ttu-id="7fced-119">Nafn, mynd, URL</span><span class="sxs-lookup"><span data-stu-id="7fced-119">Name, Image, URL</span></span>      | <span data-ttu-id="7fced-120">Þessi eiginleiki tilgreinir heiti, tengil á heimasíðu svæðisins og valfrjálsa mynd til að sýna fyrir hvert svæði sem er tekið með í einingunni.</span><span class="sxs-lookup"><span data-stu-id="7fced-120">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="7fced-121">Myndin getur verið flagg eða einhver framsetning á markaði, svæði eða staðháttum.</span><span class="sxs-lookup"><span data-stu-id="7fced-121">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="7fced-122">Bæta svæðisvalseiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="7fced-122">Add a site selector module to a page</span></span>

<span data-ttu-id="7fced-123">Hægt er að bæta við svæðisvalseiningu í [Hauseiningu](author-header-module.md) undir vali á svæði.</span><span class="sxs-lookup"><span data-stu-id="7fced-123">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="7fced-124">Eftir að því er bætt við er hægt að skilgreina fyrirsögn einingar og svæði.</span><span class="sxs-lookup"><span data-stu-id="7fced-124">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7fced-125">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7fced-125">Additional resources</span></span>

[<span data-ttu-id="7fced-126">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="7fced-126">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7fced-127">Eining síðuhauss</span><span class="sxs-lookup"><span data-stu-id="7fced-127">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="7fced-128">Brauðmylsnueining</span><span class="sxs-lookup"><span data-stu-id="7fced-128">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="7fced-129">Eining yfirlitsvalmyndar</span><span class="sxs-lookup"><span data-stu-id="7fced-129">Navigation menu module</span></span>](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]