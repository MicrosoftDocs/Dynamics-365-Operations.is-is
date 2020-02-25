---
title: Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi
description: Þetta efni gefur yfirlit yfir forskoðunarumhverfi Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ff96aeb5963df9ddee56783a089dad129bbb71c
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024684"
---
# <a name="dynamics-365-commerce-preview-environment-overview"></a><span data-ttu-id="b8c10-103">Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi</span><span class="sxs-lookup"><span data-stu-id="b8c10-103">Dynamics 365 Commerce preview environment overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b8c10-104">Þetta efni gefur yfirlit yfir forskoðunarumhverfi Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b8c10-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="overview"></a><span data-ttu-id="b8c10-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="b8c10-105">Overview</span></span>

<span data-ttu-id="b8c10-106">Forskoðunarumhverfi Commerce er valfrjálst forskoðunarumhverfi sem tekur til alls ferlisins í Dynamics 365 Commerce sem gerir hugsanlegum viðskiptavinum kleift að prófa verslunina áður en hún birtist almenningi.</span><span class="sxs-lookup"><span data-stu-id="b8c10-106">The Commerce preview environment is an optional end-to-end preview environment of Dynamics 365 Commerce that lets potential customers try out the Commerce product before its general release to the public.</span></span>

<span data-ttu-id="b8c10-107">Fyrir utan smávægilegar takmarkanir sem hafa ekki áhrif á eiginleika eða virkni veitir forskoðunarumhverfi viðskiptanna fullkomna viðskiptaupplifun og er hægt að nota það af viðskiptavinum og framkvæmdaraðilum til að meta vöruna, veita endurgjöf og gera gloppugreiningu/hæfnigreiningu.</span><span class="sxs-lookup"><span data-stu-id="b8c10-107">Aside from some minor limitations that don't affect features or functionality, the Commerce preview environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-preview-environment"></a><span data-ttu-id="b8c10-108">Takmarkanir á forskoðunarumhverfi verslunarinnar</span><span class="sxs-lookup"><span data-stu-id="b8c10-108">Limitations of the Commerce preview environment</span></span>

<span data-ttu-id="b8c10-109">Þrátt fyrir að forskoðunarumhverfi Commerce bjóði upp á fullt sett af eiginleikum og virkni í viðskiptum, þá eru nokkrar minniháttar takmarkanir:</span><span class="sxs-lookup"><span data-stu-id="b8c10-109">Although the Commerce preview environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="b8c10-110">Þrátt fyrir að forskoðunarumhverfi Commerce hafi engar landfræðilegar takmarkanir, þá er aðeins hægt að úthluta þáttum umhverfisins, eins og Retail Cloud Scale Unit (RCSU) og rafræn viðskiptaforritum, í Bandaríkjunum.</span><span class="sxs-lookup"><span data-stu-id="b8c10-110">Although the Commerce preview environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, can be provisioned only in the United States.</span></span>
- <span data-ttu-id="b8c10-111">Notkun forskoðunarumhverfis Commerce er takmörkuð við 30 daga frá þeim degi þegar rafræn viðskipti eru veitt.</span><span class="sxs-lookup"><span data-stu-id="b8c10-111">Use of the Commerce preview environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="b8c10-112">Hægt er að nota forskoðunarumhverfið með viðskiptum og frumstilla það aðeins í umhverfi sem notar sýnisgrannfræði, þar sem allir íhlutir umhverfisins eru settir upp í einni sýndarvél (VM).</span><span class="sxs-lookup"><span data-stu-id="b8c10-112">The Commerce preview environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed in a single virtual machine (VM).</span></span> <span data-ttu-id="b8c10-113">Helsta takmörkun þessarar OneBox VM grannfræði er fjöldi samtímis notenda sem forskoðunarumhverfið getur stutt.</span><span class="sxs-lookup"><span data-stu-id="b8c10-113">The main limitation of this OneBox VM topology is the number of concurrent users that the preview environment can support.</span></span>
- <span data-ttu-id="b8c10-114">Aðeins er hægt að meta forskoðunarumhverfi Commerce þar til almennt framboð (GA) verður á Commerce-afurðinni.</span><span class="sxs-lookup"><span data-stu-id="b8c10-114">The Commerce preview environment can be evaluated only until the general availability (GA) of the Commerce product.</span></span> <span data-ttu-id="b8c10-115">Nýtt kynningarumhverfi verður í boði eftir almennt framboð.</span><span class="sxs-lookup"><span data-stu-id="b8c10-115">New demo environments will be available after GA.</span></span>

## <a name="get-started"></a><span data-ttu-id="b8c10-116">Leiðsögn</span><span class="sxs-lookup"><span data-stu-id="b8c10-116">Get started</span></span>

<span data-ttu-id="b8c10-117">Til að úthluta forskoðunarumhverfi Commerce skal sjá [Veita forskoðunarumhverfi Commerce](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="b8c10-117">To provision the Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b8c10-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b8c10-118">Additional resources</span></span>

[<span data-ttu-id="b8c10-119">Úthluta Dynamics 365 Commerce forsýningarumhverfi</span><span class="sxs-lookup"><span data-stu-id="b8c10-119">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="b8c10-120">Skilgreina Dynamics 365 Commerce forskoðunarumhverfi</span><span class="sxs-lookup"><span data-stu-id="b8c10-120">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="b8c10-121">Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce forskoðunarumhverfi</span><span class="sxs-lookup"><span data-stu-id="b8c10-121">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="b8c10-122">Dynamics 365 Commerce yfirlitsumhverfi algengra spurninga</span><span class="sxs-lookup"><span data-stu-id="b8c10-122">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)
