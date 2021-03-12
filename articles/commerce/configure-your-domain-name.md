---
title: Skilgreina lénsheiti
description: Þetta efni útskýrir hvernig á að stilla lén fyrir Microsoft Dynamics 365 netverslunarsíðu.
author: psimolin
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d3df563b62b40970509340802a09bb36dda14777
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001001"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="da62b-103">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="da62b-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="da62b-104">Þetta efni útskýrir hvernig á að stilla lén fyrir Microsoft Dynamics 365 netverslunarsíðu.</span><span class="sxs-lookup"><span data-stu-id="da62b-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="da62b-105">Bæta lénum við frumstillingu á e-Commerce</span><span class="sxs-lookup"><span data-stu-id="da62b-105">Add domains during e-commerce initialization</span></span>

<span data-ttu-id="da62b-106">Til að tengja lén við Dynamics 365 Commerce rafrænt viðskiptaumhverfi skal ræsa e-Commerce eins og lýst er í [Uppsetning á nýjum leigjanda rafrænna viðskipta](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="da62b-106">To associate domains with your Dynamics 365 Commerce e-commerce environment, initialize e-commerce as described in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="da62b-107">Í frumstillingu er beðið um upplýsingar sem verða notaðar til að úthluta rafræna viðskiptaumhverfinu.</span><span class="sxs-lookup"><span data-stu-id="da62b-107">During initialization, you're asked to provide information that will be used to provision your e-commerce environment.</span></span> <span data-ttu-id="da62b-108">Í reitnum **Studd hýsilnöfn** bætirðu við öllum lénum sem þú ætlar að nota með þessu umhverfi.</span><span class="sxs-lookup"><span data-stu-id="da62b-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="da62b-109">Margfeldi lén ætti að aðgreina með semi-kommu.</span><span class="sxs-lookup"><span data-stu-id="da62b-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="da62b-110">Á þennan hátt eru lén skilgreind í öllum nauðsynlegum Commerce-íhlutum og þau eru tilbúin til notkunar þegar umferð er færð frá afhendingarneti notanda (CDN) eða vefþjóni og beint í framenda rafrænna e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="da62b-110">In this way, the domains are configured in all the required Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="da62b-111">Bæta við lénum eftir frumstillingu e-Commerce</span><span class="sxs-lookup"><span data-stu-id="da62b-111">Add domains after e-commerce initialization</span></span>

<span data-ttu-id="da62b-112">Þú verður að leggja fram þjónustubeiðni til að tengja ný lén við rafrænt viðskiptaumhverfi eftir ræsingu e-Commerce</span><span class="sxs-lookup"><span data-stu-id="da62b-112">To associate new domains with your e-commerce environment after e-commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="da62b-113">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="da62b-113">Additional resources</span></span>

[<span data-ttu-id="da62b-114">Uppsetning á nýjum leigjanda rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="da62b-114">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="da62b-115">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="da62b-115">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="da62b-116">Tengja svæði Dynamics 365 Commerce við netrás</span><span class="sxs-lookup"><span data-stu-id="da62b-116">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="da62b-117">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="da62b-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="da62b-118">Hlaða upp mörgum URL-framsendingum í einu</span><span class="sxs-lookup"><span data-stu-id="da62b-118">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="da62b-119">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="da62b-119">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="da62b-120">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="da62b-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="da62b-121">Stilla marga B2C leigjendur í viðskiptaumhverfi</span><span class="sxs-lookup"><span data-stu-id="da62b-121">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="da62b-122">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="da62b-122">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="da62b-123">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="da62b-123">Enable location-based store detection</span></span>](enable-store-detection.md)
