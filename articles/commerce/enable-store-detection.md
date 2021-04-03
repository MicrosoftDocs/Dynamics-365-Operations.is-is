---
title: Virkja greiningu á verslun eftir staðsetningu
description: Þetta efnisatriði lýsir því hvernig á að kveikja á staðsetningarbundinni verslun fyrir þitt Dynamics 365 Commerce svæði.
author: brianshook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: b34f156642b23f7b9754dac1ee81c7d0004872d8
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478189"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="631df-103">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="631df-103">Enable location-based store detection</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="631df-104">Þetta efnisatriði lýsir því hvernig á að kveikja á staðsetningarbundinni verslun fyrir þitt Dynamics 365 Commerce svæði.</span><span class="sxs-lookup"><span data-stu-id="631df-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

<span data-ttu-id="631df-105">Staðsetningartengd verslunargreining í Commerce gerir þér kleift að veita viðskiptavinum viðeigandi efni, út frá staðsetningu þeirra.</span><span class="sxs-lookup"><span data-stu-id="631df-105">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="631df-106">Þegar kveikt er á staðsetningabundinni verslun finnur viðskiptaþjónustan upplýsingar um landið/svæðið frá IP-tölu vafra viðskiptavinarins til að beina viðskiptavininum að bestu landfræðilegu uppsetningarstað sem til er.</span><span class="sxs-lookup"><span data-stu-id="631df-106">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="631df-107">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="631df-107">Privacy notice</span></span>

<span data-ttu-id="631df-108">Ef þú kveikir á staðsetningarbyggðri greiningaraðgerðar verslunar eru upplýsingar úr vafra viðskiptavinarins sendar til Microsoft staðsetningarþjónustu.</span><span class="sxs-lookup"><span data-stu-id="631df-108">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="631df-109">Þessar upplýsingar eru síðan notaðar til að veita viðskiptavininum efni sem skiptir máli fyrir staðsetningu hans.</span><span class="sxs-lookup"><span data-stu-id="631df-109">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="631df-110">Bæði upplýsingar sem sendar eru úr vafra viðskiptavinarins og staðsetningarupplýsingum sem skilað er til viðskiptavinarins eru háðar persónuverndarstefnu og reglum um samræmi við fótspor.</span><span class="sxs-lookup"><span data-stu-id="631df-110">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="631df-111">Kveiktu á greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="631df-111">Turn on location-based store detection</span></span>

<span data-ttu-id="631df-112">Fylgdu þessum skrefum til að kveikja á staðsetningarbyggðri greiningu verslunar í Commerce.</span><span class="sxs-lookup"><span data-stu-id="631df-112">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="631df-113">Farðu á síðuna þína í höfundatólinu.</span><span class="sxs-lookup"><span data-stu-id="631df-113">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="631df-114">Í stýriglugganum vinstra megin velurðu **Svæðisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="631df-114">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="631df-115">Veldu **Svæðisstillingar**.</span><span class="sxs-lookup"><span data-stu-id="631df-115">Select **Site Settings**.</span></span>
1. <span data-ttu-id="631df-116">Stilltu valkostinn **Kveikja á staðsetningarbyggðri greiningu** á **Kveikt**.</span><span class="sxs-lookup"><span data-stu-id="631df-116">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="631df-117">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="631df-117">Additional resources</span></span>

[<span data-ttu-id="631df-118">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="631df-118">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="631df-119">Uppsetning á nýjum leigjanda rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="631df-119">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="631df-120">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="631df-120">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="631df-121">Tengja svæði Dynamics 365 Commerce við netrás</span><span class="sxs-lookup"><span data-stu-id="631df-121">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="631df-122">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="631df-122">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="631df-123">Hlaða upp mörgum URL-framsendingum í einu</span><span class="sxs-lookup"><span data-stu-id="631df-123">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="631df-124">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="631df-124">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="631df-125">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="631df-125">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="631df-126">Stilla marga B2C leigjendur í viðskiptaumhverfi</span><span class="sxs-lookup"><span data-stu-id="631df-126">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="631df-127">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="631df-127">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
