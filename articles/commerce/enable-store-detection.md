---
title: Virkja greiningu á verslun eftir staðsetningu
description: Þetta efnisatriði lýsir því hvernig á að kveikja á staðsetningarbundinni verslun fyrir þitt Dynamics 365 Commerce svæði.
author: brianshook
manager: annbe
ms.date: 03/02/2020
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 66ffe56f9d969c9d62ed4ff49f0848fab7e58a56
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096870"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="4eefc-103">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="4eefc-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4eefc-104">Þetta efnisatriði lýsir því hvernig á að kveikja á staðsetningarbundinni verslun fyrir þitt Dynamics 365 Commerce svæði.</span><span class="sxs-lookup"><span data-stu-id="4eefc-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="4eefc-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="4eefc-105">Overview</span></span>

<span data-ttu-id="4eefc-106">Staðsetningartengd verslunargreining í Commerce gerir þér kleift að veita viðskiptavinum viðeigandi efni, út frá staðsetningu þeirra.</span><span class="sxs-lookup"><span data-stu-id="4eefc-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="4eefc-107">Þegar kveikt er á staðsetningabundinni verslun finnur viðskiptaþjónustan upplýsingar um landið/svæðið frá IP-tölu vafra viðskiptavinarins til að beina viðskiptavininum að bestu landfræðilegu uppsetningarstað sem til er.</span><span class="sxs-lookup"><span data-stu-id="4eefc-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="4eefc-108">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="4eefc-108">Privacy notice</span></span>

<span data-ttu-id="4eefc-109">Ef þú kveikir á staðsetningarbyggðri greiningaraðgerðar verslunar eru upplýsingar úr vafra viðskiptavinarins sendar til Microsoft staðsetningarþjónustu.</span><span class="sxs-lookup"><span data-stu-id="4eefc-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="4eefc-110">Þessar upplýsingar eru síðan notaðar til að veita viðskiptavininum efni sem skiptir máli fyrir staðsetningu hans.</span><span class="sxs-lookup"><span data-stu-id="4eefc-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="4eefc-111">Bæði upplýsingar sem sendar eru úr vafra viðskiptavinarins og staðsetningarupplýsingum sem skilað er til viðskiptavinarins eru háðar persónuverndarstefnu og reglum um samræmi við fótspor.</span><span class="sxs-lookup"><span data-stu-id="4eefc-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="4eefc-112">Kveiktu á greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="4eefc-112">Turn on location-based store detection</span></span>

<span data-ttu-id="4eefc-113">Fylgdu þessum skrefum til að kveikja á staðsetningarbyggðri greiningu verslunar í Commerce.</span><span class="sxs-lookup"><span data-stu-id="4eefc-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="4eefc-114">Farðu á síðuna þína í höfundatólinu.</span><span class="sxs-lookup"><span data-stu-id="4eefc-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="4eefc-115">Í stýriglugganum vinstra megin velurðu **Svæðisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="4eefc-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="4eefc-116">Veldu **Svæðisstillingar**.</span><span class="sxs-lookup"><span data-stu-id="4eefc-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="4eefc-117">Stilltu valkostinn **Kveikja á staðsetningarbyggðri greiningu** á **Kveikt**.</span><span class="sxs-lookup"><span data-stu-id="4eefc-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4eefc-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4eefc-118">Additional resources</span></span>

[<span data-ttu-id="4eefc-119">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="4eefc-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="4eefc-120">Uppsetning á nýju vefsvæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="4eefc-120">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="4eefc-121">Setja upp netverslunarrás</span><span class="sxs-lookup"><span data-stu-id="4eefc-121">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="4eefc-122">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="4eefc-122">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="4eefc-123">Tengja netsvæði við rás</span><span class="sxs-lookup"><span data-stu-id="4eefc-123">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="4eefc-124">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="4eefc-124">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="4eefc-125">Hlaða upp mörgum slóðartilvísunum í einu</span><span class="sxs-lookup"><span data-stu-id="4eefc-125">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="4eefc-126">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="4eefc-126">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="4eefc-127">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="4eefc-127">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="4eefc-128">Stilla marga B2C leigjendur í viðskiptaumhverfi</span><span class="sxs-lookup"><span data-stu-id="4eefc-128">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="4eefc-129">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="4eefc-129">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
