---
title: Dynamics 365 Commerce yfirlit yfir matsumhverfi
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
ms.openlocfilehash: cc6bffba6ee402c6b48d6a3c8f8356eb32b5423b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478021"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="aceb6-103">Dynamics 365 Commerce yfirlit yfir matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="aceb6-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aceb6-104">Í þessu Umfjöllunarefni er að finna yfirlit yfir Microsoft Dynamics 365 Commerce matsumhverfi.</span><span class="sxs-lookup"><span data-stu-id="aceb6-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="aceb6-105">Commerce matsumhverfi er almennt ekki í boði og er veitt af samstarfsaðilum og viðskiptavinum á grundvelli beiðna.</span><span class="sxs-lookup"><span data-stu-id="aceb6-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="aceb6-106">Þú ættir að hafa samband við Microsoft samstarfsaðila þinn til að fá aðstoð ef þig vantar frekari upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="aceb6-106">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="aceb6-107">Commerce matsumhverfi er valfrjálst og tekur til alls ferilsins Dynamics 365 Commerce sem gerir samstarfsaðilum og hugsanlegum viðskiptavinum kleift að prófa Commerce-vöruna.</span><span class="sxs-lookup"><span data-stu-id="aceb6-107">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="aceb6-108">Matsumhverfi er forstillt að hluta til að draga úr nauðsynlegum eftirúthlutunarskrefum.</span><span class="sxs-lookup"><span data-stu-id="aceb6-108">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="aceb6-109">Fyrir utan nokkrar minni háttar takmarkanir sem hafa ekki áhrif á eiginleika eða virkni, býður Commerce matsumhverfið upp á alla Commerce reynslu, og hægt er að nota viðskiptavini og innleiðingaraðila til að meta afurðina, gefa endurgjöf og gera samræmis og gloppugreiningu.</span><span class="sxs-lookup"><span data-stu-id="aceb6-109">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="aceb6-110">Takmarkanir á Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="aceb6-110">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="aceb6-111">Þrátt fyrir að Commerce matsumhverfi fyrir viðskiptaviðskipti veiti alla eiginleika og virkni í Commerce eru smávægilegar takmarkanir:</span><span class="sxs-lookup"><span data-stu-id="aceb6-111">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="aceb6-112">Þrátt fyrir að mat Commerce matsumhverfi er ekki með neinar landfræðilegar takmarkanir, er aðeins hægt að úthluta á Retail Cloud Scale Unit (rcsu) og e-Commerce-forritum í Bandaríkjunum.</span><span class="sxs-lookup"><span data-stu-id="aceb6-112">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="aceb6-113">Notkun á Commerce matsumhverfi takmarkast við 30 daga frá dagsetningunni þegar e-Commerce er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="aceb6-113">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="aceb6-114">Hægt er að setja upp og frumstilla Commerce matsumhverfið í umhverfi sem notar sýnisgrannfræði, þar sem allir þættir umhverfis eru virkjaðir á sýndarvél í einu skýi (VL).</span><span class="sxs-lookup"><span data-stu-id="aceb6-114">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="aceb6-115">Aðaltakmörkunin á þessari grannfræði er fjöldi samhliða notenda sem umhverfið styður.</span><span class="sxs-lookup"><span data-stu-id="aceb6-115">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="aceb6-116">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="aceb6-116">Get started</span></span>

<span data-ttu-id="aceb6-117">Til að ráðstafa viðskiptaumhverfinu í Commerce, sjá [Úthlutun Commerce matsumhverfis](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="aceb6-117">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aceb6-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="aceb6-118">Additional resources</span></span>

[<span data-ttu-id="aceb6-119">Úthluta Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="aceb6-119">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="aceb6-120">Stilla Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="aceb6-120">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="aceb6-121">Skilgreina BOPIS í Dynamics 365 Commerce í matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="aceb6-121">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="aceb6-122">Skilgreina valfrjálsa eiginleika fyrir Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="aceb6-122">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="aceb6-123">algengar spurningar um Dynamics 365 Commerce matsumhverfi</span><span class="sxs-lookup"><span data-stu-id="aceb6-123">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
