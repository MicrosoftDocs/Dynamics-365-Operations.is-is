---
title: Skilgreina lénsheiti
description: Þetta efni útskýrir hvernig á að stilla lén fyrir Microsoft Dynamics 365 netverslunarsíðu.
author: psimolin
manager: AnnBe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2ad9ca3aee21301ef6d830d7b29982a45cd53f60
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096821"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="c4009-103">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="c4009-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c4009-104">Þetta efni útskýrir hvernig á að stilla lén fyrir Microsoft Dynamics 365 netverslunarsíðu.</span><span class="sxs-lookup"><span data-stu-id="c4009-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="c4009-105">Bættu við lénum við frumstillingu netverslunar</span><span class="sxs-lookup"><span data-stu-id="c4009-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="c4009-106">Til að tengja lén við netverslunarumhverfi þitt skaltu frumstilla netverslun eins og lýst er í [Uppsetning á nýju vefsvæði fyrir netverslun](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="c4009-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="c4009-107">Við frumstilling er beðið um að upplýsingar séu látnar í té sem notaðar verða til að bjóða upp á netverslunarumhverfi þitt.</span><span class="sxs-lookup"><span data-stu-id="c4009-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="c4009-108">Í reitnum **Studd hýsilnöfn** bætirðu við öllum lénum sem þú ætlar að nota með þessu umhverfi.</span><span class="sxs-lookup"><span data-stu-id="c4009-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="c4009-109">Margfeldi lén ætti að aðgreina með semi-kommu.</span><span class="sxs-lookup"><span data-stu-id="c4009-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="c4009-110">Með þessum hætti eru lénin skilgreind í öllum nauðsynlegum íhlutum netverslunar og þau eru tilbún til notkunar þegar þú skiptir úr umferð frá efnisbirtingarnetinu (CDN) eða netþjóninum og beinir henni á framvinnslu netverslunar.</span><span class="sxs-lookup"><span data-stu-id="c4009-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="c4009-111">Bættu við lénum eftir frumstillingu netverslunar</span><span class="sxs-lookup"><span data-stu-id="c4009-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="c4009-112">Til að tengja ný lén við netverslunarumhverfi þitt eftir frumstillingu á netverslun verður þú að leggja fram þjónustubeiðni.</span><span class="sxs-lookup"><span data-stu-id="c4009-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c4009-113">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c4009-113">Additional resources</span></span>

[<span data-ttu-id="c4009-114">Uppsetning á nýju vefsvæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="c4009-114">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="c4009-115">Setja upp netverslunarrás</span><span class="sxs-lookup"><span data-stu-id="c4009-115">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="c4009-116">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="c4009-116">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="c4009-117">Tengja netsvæði við rás</span><span class="sxs-lookup"><span data-stu-id="c4009-117">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="c4009-118">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="c4009-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="c4009-119">Hlaða upp mörgum slóðartilvísunum í einu</span><span class="sxs-lookup"><span data-stu-id="c4009-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="c4009-120">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="c4009-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="c4009-121">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="c4009-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="c4009-122">Stilla marga B2C leigjendur í viðskiptaumhverfi</span><span class="sxs-lookup"><span data-stu-id="c4009-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="c4009-123">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="c4009-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="c4009-124">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="c4009-124">Enable location-based store detection</span></span>](enable-store-detection.md)
