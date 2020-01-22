---
title: Yfirlit yfir forskoðunarumhverfi Commerce
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
ms.openlocfilehash: 901583afde4739be5313fa129ff0e52f11326881
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906071"
---
# <a name="commerce-preview-environment-overview"></a><span data-ttu-id="cc8d0-103">Yfirlit yfir forskoðunarumhverfi Commerce</span><span class="sxs-lookup"><span data-stu-id="cc8d0-103">Commerce preview environment overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="cc8d0-104">Þetta efni gefur yfirlit yfir forskoðunarumhverfi Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cc8d0-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="overview"></a><span data-ttu-id="cc8d0-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="cc8d0-105">Overview</span></span>

<span data-ttu-id="cc8d0-106">Forskoðunarumhverfi Commerce er valfrjálst forskoðunarumhverfi sem tekur til alls ferlisins í Dynamics 365 Commerce sem gerir hugsanlegum viðskiptavinum kleift að prófa verslunina áður en hún birtist almenningi.</span><span class="sxs-lookup"><span data-stu-id="cc8d0-106">The Commerce preview environment is an optional end-to-end preview environment of Dynamics 365 Commerce that lets potential customers try out the Commerce product before its general release to the public.</span></span>

<span data-ttu-id="cc8d0-107">Fyrir utan smávægilegar takmarkanir sem hafa ekki áhrif á eiginleika eða virkni veitir forskoðunarumhverfi viðskiptanna fullkomna viðskiptaupplifun og er hægt að nota það af viðskiptavinum og framkvæmdaraðilum til að meta vöruna, veita endurgjöf og gera gloppugreiningu/hæfnigreiningu.</span><span class="sxs-lookup"><span data-stu-id="cc8d0-107">Aside from some minor limitations that don't affect features or functionality, the Commerce preview environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-preview-environment"></a><span data-ttu-id="cc8d0-108">Takmarkanir á forskoðunarumhverfi verslunarinnar</span><span class="sxs-lookup"><span data-stu-id="cc8d0-108">Limitations of the Commerce preview environment</span></span>

<span data-ttu-id="cc8d0-109">Þrátt fyrir að forskoðunarumhverfi Commerce bjóði upp á fullt sett af eiginleikum og virkni í viðskiptum, þá eru nokkrar minniháttar takmarkanir:</span><span class="sxs-lookup"><span data-stu-id="cc8d0-109">Although the Commerce preview environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="cc8d0-110">Þrátt fyrir að forskoðunarumhverfi Commerce hafi engar landfræðilegar takmarkanir, þá er aðeins hægt að úthluta þáttum umhverfisins, eins og Retail Cloud Scale Unit (RCSU) og rafræn viðskiptaforritum, í Bandaríkjunum.</span><span class="sxs-lookup"><span data-stu-id="cc8d0-110">Although the Commerce preview environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, can be provisioned only in the United States.</span></span>
- <span data-ttu-id="cc8d0-111">Notkun forskoðunarumhverfis Commerce er takmörkuð við 30 daga frá þeim degi þegar rafræn viðskipti eru veitt.</span><span class="sxs-lookup"><span data-stu-id="cc8d0-111">Use of the Commerce preview environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="cc8d0-112">Hægt er að nota forskoðunarumhverfið með viðskiptum og frumstilla það aðeins í umhverfi sem notar sýnisgrannfræði, þar sem allir íhlutir umhverfisins eru settir upp í einni sýndarvél (VM).</span><span class="sxs-lookup"><span data-stu-id="cc8d0-112">The Commerce preview environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed in a single virtual machine (VM).</span></span> <span data-ttu-id="cc8d0-113">Helsta takmörkun þessarar OneBox VM grannfræði er fjöldi samtímis notenda sem forskoðunarumhverfið getur stutt.</span><span class="sxs-lookup"><span data-stu-id="cc8d0-113">The main limitation of this OneBox VM topology is the number of concurrent users that the preview environment can support.</span></span>
- <span data-ttu-id="cc8d0-114">Aðeins er hægt að meta forskoðunarumhverfi Commerce þar til almennt framboð (GA) verður á Commerce-afurðinni.</span><span class="sxs-lookup"><span data-stu-id="cc8d0-114">The Commerce preview environment can be evaluated only until the general availability (GA) of the Commerce product.</span></span> <span data-ttu-id="cc8d0-115">Nýtt kynningarumhverfi verður í boði eftir almennt framboð.</span><span class="sxs-lookup"><span data-stu-id="cc8d0-115">New demo environments will be available after GA.</span></span>

## <a name="get-started"></a><span data-ttu-id="cc8d0-116">Leiðsögn</span><span class="sxs-lookup"><span data-stu-id="cc8d0-116">Get started</span></span>

<span data-ttu-id="cc8d0-117">Til að úthluta forskoðunarumhverfi Commerce skal sjá [Veita forskoðunarumhverfi Commerce](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="cc8d0-117">To provision the Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cc8d0-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="cc8d0-118">Additional resources</span></span>

[<span data-ttu-id="cc8d0-119">Úthluta forskoðunarumhverfi Commerce</span><span class="sxs-lookup"><span data-stu-id="cc8d0-119">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="cc8d0-120">Skilgreina forskoðunarumhverfi Commerce</span><span class="sxs-lookup"><span data-stu-id="cc8d0-120">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="cc8d0-121">Stilltu valfrjálsa eiginleika fyrir forsýningarumhverfi Commerce</span><span class="sxs-lookup"><span data-stu-id="cc8d0-121">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="cc8d0-122">Algengar spurningar um forskoðunarumhverfi Commerce</span><span class="sxs-lookup"><span data-stu-id="cc8d0-122">Commerce preview environment FAQ</span></span>](cpe-faq.md)
