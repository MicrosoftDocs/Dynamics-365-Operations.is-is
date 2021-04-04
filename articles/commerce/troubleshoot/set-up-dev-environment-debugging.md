---
title: Setja upp þróunarumhverfi rafrænna viðskipta til að kemba lag 1 af sýndarvél Retail Server
description: Þetta efnisatriði útskýrir hvernig á að setja upp þróunarumhverfi rafrænna viðskipta til að kemba lag 1 af sýndarvél Retail Server.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 35380a559a4f1b22bdf04ff25cb2bbfc51aff45b
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585366"
---
# <a name="set-up-an-e-commerce-development-environment-to-debug-against-a-tier-1-retail-server-virtual-machine"></a><span data-ttu-id="8179f-103">Setja upp þróunarumhverfi rafrænna viðskipta til að kemba lag 1 af sýndarvél Retail Server</span><span class="sxs-lookup"><span data-stu-id="8179f-103">Set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8179f-104">Þetta efnisatriði útskýrir hvernig á að setja upp þróunarumhverfi rafrænna viðskipta til að kemba lag 1 af sýndarvél Retail Server.</span><span class="sxs-lookup"><span data-stu-id="8179f-104">This topic explains how to set up an e-commerce development environment to debug against a Tier 1 Retail Server virtual machine (VM).</span></span>

## <a name="description"></a><span data-ttu-id="8179f-105">lýsing</span><span class="sxs-lookup"><span data-stu-id="8179f-105">Description</span></span>

<span data-ttu-id="8179f-106">Lag 1 umhverfi Microsoft Dynamics 365 Commerce eru yfirleitt notuð fyrir Commerce Runtime (CRT) og þróun á viðbót sölustaðar (POS).</span><span class="sxs-lookup"><span data-stu-id="8179f-106">Microsoft Dynamics 365 Commerce Tier 1 environments are typically deployed for Commerce runtime (CRT) and point of sale (POS) extension development.</span></span> <span data-ttu-id="8179f-107">Þetta eru sjálfstæð umhverfi.</span><span class="sxs-lookup"><span data-stu-id="8179f-107">They are standalone environments.</span></span> <span data-ttu-id="8179f-108">Vegna þess að hönnunin er af eðli SaaS-þjónustu inniheldur hún ekki þætti rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="8179f-108">Because of the software as a service (SaaS) nature of the architecture, they don't include e-commerce components.</span></span>

<span data-ttu-id="8179f-109">Í sumum aðstæðum gæti verið sniðugt að prófa köll á viðbætur á umhverfislag 1 svo hægt sé að kemba viðbætur úr þáttum rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="8179f-109">In some scenarios, you might want to test calls to extensions in a Tier 1 environment, so that you can debug extensions from e-commerce components.</span></span> <span data-ttu-id="8179f-110">Almennar leiðbeiningar er að finna í [Kemba með hliðsjón af þróunarumhverfislag 1 í Commerce](../e-commerce-extensibility/debug-tier-1.md).</span><span class="sxs-lookup"><span data-stu-id="8179f-110">For general instructions, see [Debug against a Tier 1 Commerce development environment](../e-commerce-extensibility/debug-tier-1.md).</span></span>

<span data-ttu-id="8179f-111">Þegar umhverfislag 1 er kembt, vegna þess að svæðið kallar nú á annað Retail Server, gætu köll milli þjóna valdið ýmsum villum sem tengjast öryggisreglu efnisins.</span><span class="sxs-lookup"><span data-stu-id="8179f-111">When you debug against a Tier 1 environment, because the site is now calling a different Retail Server, cross-server calls might cause various errors that are related to the content security policy.</span></span>

<span data-ttu-id="8179f-112">Eftirfarandi mynd sýnir dæmi um villu sem gæti komið upp þegar afbrigði er valið á upplýsingasíðu afurðar.</span><span class="sxs-lookup"><span data-stu-id="8179f-112">The following illustration shows an example of an error that might occur when a variant is selected on a product details page.</span></span>

![Villa þegar afbrigði er valið á upplýsingasíðu afurðar](media/unhandled-rejection-error.jpg)

<span data-ttu-id="8179f-114">Eftirfarandi mynd sýnir dæmi um svipaða villu í verkfærum kembiforrits í vafra (F12 forritunarverkfæri).</span><span class="sxs-lookup"><span data-stu-id="8179f-114">The following illustration shows an example of a similar error in a browser's debugger tools (F12 Developer Tools).</span></span> <span data-ttu-id="8179f-115">Villuboðin minnast á brot á öryggisleiðbeiningu efnisins.</span><span class="sxs-lookup"><span data-stu-id="8179f-115">The error message mentions violation of the content security policy directive.</span></span>

![Villa í verkfærum kembiforrits](media/debugger-tools-error.JPG)

## <a name="resolution"></a><span data-ttu-id="8179f-117">Upplausn</span><span class="sxs-lookup"><span data-stu-id="8179f-117">Resolution</span></span>

### <a name="disable-the-content-security-policy-for-the-site-in-commerce-site-builder"></a><span data-ttu-id="8179f-118">Gera öryggisreglu efnis óvirka fyrir svæðið í vefsmið Commerce</span><span class="sxs-lookup"><span data-stu-id="8179f-118">Disable the content security policy for the site in Commerce site builder</span></span>

1. <span data-ttu-id="8179f-119">Veljið svæðið sem unnið er á.</span><span class="sxs-lookup"><span data-stu-id="8179f-119">Select the site that you're working on.</span></span>
1. <span data-ttu-id="8179f-120">Veljið **Stillingar** og veljið síðan **Viðbætur**.</span><span class="sxs-lookup"><span data-stu-id="8179f-120">Select **Settings**, and then select **Extensions**.</span></span>
1. <span data-ttu-id="8179f-121">Í flipanum **Öryggisregla efnis** skal velja **Gera öryggisreglu efnis óvirka**.</span><span class="sxs-lookup"><span data-stu-id="8179f-121">On the **Content security policy** tab, select **Disable content security policy**.</span></span>
1. <span data-ttu-id="8179f-122">Veljið **Vista og birta**.</span><span class="sxs-lookup"><span data-stu-id="8179f-122">Select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="8179f-123">B2C-innskráning virkar ekki í staðbundnu þróunarumhverfi.</span><span class="sxs-lookup"><span data-stu-id="8179f-123">Business-to-consumer (B2C) sign-in won't work in a local development environment.</span></span> <span data-ttu-id="8179f-124">Hins vegar er hægt að nota greiðsluferli gesta eða smíða gervisíður til að hvetja til innskráningar notanda eins og þörf er á.</span><span class="sxs-lookup"><span data-stu-id="8179f-124">However, you can use guest checkouts or build page mocks to simulate a user sign-in as required.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8179f-125">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8179f-125">Additional resources</span></span>

[<span data-ttu-id="8179f-126">Hafist handa með stækkunarhæfni rafrænna viðskipta á netinu</span><span class="sxs-lookup"><span data-stu-id="8179f-126">Get started with e-commerce online extensibility development</span></span>](../e-commerce-extensibility/sdk-getting-started.md)

[<span data-ttu-id="8179f-127">Stjórna öryggisreglu fyrir efni (CSP) á svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="8179f-127">Manage content security policy (CSP) on e-commerce site</span></span>](../manage-csp.md)
