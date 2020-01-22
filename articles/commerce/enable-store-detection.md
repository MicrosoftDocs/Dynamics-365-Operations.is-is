---
title: Virkja greiningu á verslun eftir staðsetningu
description: Þetta efnisatriði lýsir því hvernig á að kveikja á staðsetningarbundinni verslun fyrir þitt Dynamics 365 Commerce svæði.
author: brianshook
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: c5fb59a9798e2cddfb75b71235ee7754e54b0e28
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945772"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="e8f75-103">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="e8f75-103">Enable location-based store detection</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e8f75-104">Þetta efnisatriði lýsir því hvernig á að kveikja á staðsetningarbundinni verslun fyrir þitt Dynamics 365 Commerce svæði.</span><span class="sxs-lookup"><span data-stu-id="e8f75-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="e8f75-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="e8f75-105">Overview</span></span>

<span data-ttu-id="e8f75-106">Staðsetningartengd verslunargreining í Commerce gerir þér kleift að veita viðskiptavinum viðeigandi efni, út frá staðsetningu þeirra.</span><span class="sxs-lookup"><span data-stu-id="e8f75-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="e8f75-107">Þegar kveikt er á staðsetningabundinni verslun finnur viðskiptaþjónustan upplýsingar um landið/svæðið frá IP-tölu vafra viðskiptavinarins til að beina viðskiptavininum að bestu landfræðilegu uppsetningarstað sem til er.</span><span class="sxs-lookup"><span data-stu-id="e8f75-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="e8f75-108">Tilkynning um persónuvernd</span><span class="sxs-lookup"><span data-stu-id="e8f75-108">Privacy notice</span></span>

<span data-ttu-id="e8f75-109">Ef þú kveikir á staðsetningarbyggðri greiningaraðgerðar verslunar eru upplýsingar úr vafra viðskiptavinarins sendar til Microsoft staðsetningarþjónustu.</span><span class="sxs-lookup"><span data-stu-id="e8f75-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="e8f75-110">Þessar upplýsingar eru síðan notaðar til að veita viðskiptavininum efni sem skiptir máli fyrir staðsetningu hans.</span><span class="sxs-lookup"><span data-stu-id="e8f75-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="e8f75-111">Bæði upplýsingar sem sendar eru úr vafra viðskiptavinarins og staðsetningarupplýsingum sem skilað er til viðskiptavinarins eru háðar persónuverndarstefnu og reglum um samræmi við fótspor.</span><span class="sxs-lookup"><span data-stu-id="e8f75-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="e8f75-112">Kveiktu á greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="e8f75-112">Turn on location-based store detection</span></span>

<span data-ttu-id="e8f75-113">Fylgdu þessum skrefum til að kveikja á staðsetningarbyggðri greiningu verslunar í Commerce.</span><span class="sxs-lookup"><span data-stu-id="e8f75-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="e8f75-114">Farðu á síðuna þína í höfundatólinu.</span><span class="sxs-lookup"><span data-stu-id="e8f75-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="e8f75-115">Í stýriglugganum vinstra megin velurðu **Svæðisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="e8f75-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="e8f75-116">Veldu **Svæðisstillingar**.</span><span class="sxs-lookup"><span data-stu-id="e8f75-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="e8f75-117">Stilltu valkostinn **Kveikja á staðsetningarbyggðri greiningu** á **Kveikt**.</span><span class="sxs-lookup"><span data-stu-id="e8f75-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8f75-118">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e8f75-118">Additional resources</span></span>

[<span data-ttu-id="e8f75-119">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="e8f75-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="e8f75-120">Uppsetning á nýju vefsvæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="e8f75-120">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="e8f75-121">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="e8f75-121">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="e8f75-122">Tengja netsvæði við rás</span><span class="sxs-lookup"><span data-stu-id="e8f75-122">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="e8f75-123">Stjórna robots.txt-skrám</span><span class="sxs-lookup"><span data-stu-id="e8f75-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="e8f75-124">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="e8f75-124">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="e8f75-125">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="e8f75-125">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
