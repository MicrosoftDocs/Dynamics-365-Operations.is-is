---
title: Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi
description: Í þessu Umfjöllunarefni er að finna yfirlit yfir Microsoft Dynamics 365 Commerce matsumhverfi.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8e08c2f327771d7731b836840006d63b6ecb7dfc
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5000951"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="e55ec-103">Dynamics 365 Commerce yfirlit yfir forskoðunarumhverfi</span><span class="sxs-lookup"><span data-stu-id="e55ec-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e55ec-104">Í þessu Umfjöllunarefni er að finna yfirlit yfir Microsoft Dynamics 365 Commerce matsumhverfi.</span><span class="sxs-lookup"><span data-stu-id="e55ec-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="e55ec-105">Commerce matsumhverfi er almennt ekki í boði og er veitt af samstarfsaðilum og viðskiptavinum á grundvelli beiðna.</span><span class="sxs-lookup"><span data-stu-id="e55ec-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="e55ec-106">Þú ættir að hafa samband við Microsoft samstarfsaðila þinn til að fá aðstoð ef þig vantar frekari upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="e55ec-106">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="e55ec-107">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="e55ec-107">Overview</span></span>

<span data-ttu-id="e55ec-108">Commerce matsumhverfi er valfrjálst og tekur til alls ferilsins Dynamics 365 Commerce sem gerir samstarfsaðilum og hugsanlegum viðskiptavinum kleift að prófa Commerce-vöruna.</span><span class="sxs-lookup"><span data-stu-id="e55ec-108">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="e55ec-109">Matsumhverfi er forstillt að hluta til að draga úr nauðsynlegum eftirúthlutunarskrefum.</span><span class="sxs-lookup"><span data-stu-id="e55ec-109">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="e55ec-110">Fyrir utan nokkrar minni háttar takmarkanir sem hafa ekki áhrif á eiginleika eða virkni, býður Commerce matsumhverfið upp á alla Commerce reynslu, og hægt er að nota viðskiptavini og innleiðingaraðila til að meta afurðina, gefa endurgjöf og gera samræmis og gloppugreiningu.</span><span class="sxs-lookup"><span data-stu-id="e55ec-110">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="e55ec-111">Takmarkanir á Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="e55ec-111">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="e55ec-112">Þrátt fyrir að Commerce matsumhverfi fyrir viðskiptaviðskipti veiti alla eiginleika og virkni í Commerce eru smávægilegar takmarkanir:</span><span class="sxs-lookup"><span data-stu-id="e55ec-112">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="e55ec-113">Þrátt fyrir að mat Commerce matsumhverfi er ekki með neinar landfræðilegar takmarkanir, er aðeins hægt að úthluta á Retail Cloud Scale Unit (rcsu) og e-Commerce-forritum í Bandaríkjunum.</span><span class="sxs-lookup"><span data-stu-id="e55ec-113">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="e55ec-114">Notkun á Commerce matsumhverfi takmarkast við 30 daga frá dagsetningunni þegar e-Commerce er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="e55ec-114">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="e55ec-115">Hægt er að setja upp og frumstilla Commerce matsumhverfið í umhverfi sem notar sýnisgrannfræði, þar sem allir þættir umhverfis eru virkjaðir á sýndarvél í einu skýi (VL).</span><span class="sxs-lookup"><span data-stu-id="e55ec-115">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="e55ec-116">Aðaltakmörkunin á þessari grannfræði er fjöldi samhliða notenda sem umhverfið styður.</span><span class="sxs-lookup"><span data-stu-id="e55ec-116">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="e55ec-117">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="e55ec-117">Get started</span></span>

<span data-ttu-id="e55ec-118">Til að ráðstafa viðskiptaumhverfinu í Commerce, sjá [Úthlutun Commerce matsumhverfis](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="e55ec-118">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e55ec-119">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e55ec-119">Additional resources</span></span>

[<span data-ttu-id="e55ec-120">Úthluta Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="e55ec-120">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="e55ec-121">Stilla Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="e55ec-121">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="e55ec-122">Skilgreina BOPIS í Dynamics 365 Commerce í matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="e55ec-122">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="e55ec-123">Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="e55ec-123">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="e55ec-124">algengar spurningar um Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="e55ec-124">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)
