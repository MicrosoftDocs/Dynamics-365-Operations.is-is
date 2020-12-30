---
title: Tengja svæði Dynamics 365 Commerce við netrás
description: Þetta efni útskýrir hvernig á að binda Microsoft Dynamics 365 Commerce svæðið við eina eða fleiri netverslanir.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b6ae02d34499275fa303358f7dae4d3835d438e1
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517331"
---
# <a name="associate-a-dynamics-365-commerce-site-with-an-online-channel"></a><span data-ttu-id="1b1e2-103">Tengja svæði Dynamics 365 Commerce við netrás</span><span class="sxs-lookup"><span data-stu-id="1b1e2-103">Associate a Dynamics 365 Commerce site with an online channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1b1e2-104">Þetta efni útskýrir hvernig á að binda Microsoft Dynamics 365 Commerce svæðið við eina eða fleiri netverslanir.</span><span class="sxs-lookup"><span data-stu-id="1b1e2-104">This topic explains how to bind your Microsoft Dynamics 365 Commerce site to one or more online stores.</span></span> 

<span data-ttu-id="1b1e2-105">Eftir að þú hefur úthlutað Dynamics 365 Commerce rafræna viðskiptaumhverfinu þínu með því að nota Microsoft Dynamics Lifecycle Services (LCS) gáttina hefurðu þegar búið til fyrstu rafræna vefsvæðinu þínu.</span><span class="sxs-lookup"><span data-stu-id="1b1e2-105">After you've provisioned your Dynamics 365 Commerce e-commerce environment by using the Microsoft Dynamics Lifecycle Services (LCS) portal, you're ready to establish your first e-commerce website.</span></span> <span data-ttu-id="1b1e2-106">Sem hluta af upphaflegri gerð vefsvæðisins tengir þú vefinn við netverslun sem áður var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="1b1e2-106">As part of the initial site creation, you associate the site with an online store that was previously created.</span></span> <span data-ttu-id="1b1e2-107">Þetta skref bindur vefinn við netrás og lætur vefinn sýna stigveldi, vörur, flokka, verð, flutningsmöguleika og allt annað sem þú skilgreindir í netversluninni.</span><span class="sxs-lookup"><span data-stu-id="1b1e2-107">This step binds the site to an online channel and lets the site show the navigation hierarchy, products, categories, prices, shipping options, and everything else that you defined in the online store.</span></span>

<span data-ttu-id="1b1e2-108">Til að koma á nýrri síðu og tengja netverslun við það, í LCS, veldu tengilinn fyrir höfundarumhverfið.</span><span class="sxs-lookup"><span data-stu-id="1b1e2-108">To establish a new site and associate an online store with it, in LCS, select the link for the site authoring environment.</span></span> <span data-ttu-id="1b1e2-109">Veldu síðan á síðunni fyrir höfundarumhverfi svæðisins **Ný síða**.</span><span class="sxs-lookup"><span data-stu-id="1b1e2-109">Then, on the page for the site authoring environment, select **New site**.</span></span> <span data-ttu-id="1b1e2-110">Í valmyndinni **Nýtt svæði** verður þú að gefa grunnupplýsingar um vefsvæðið.</span><span class="sxs-lookup"><span data-stu-id="1b1e2-110">In the **New site** dialog box, you must provide some basic information about your site.</span></span> <span data-ttu-id="1b1e2-111">Til að fá ítarlegri útskýringar á upplýsingunum sem þarf að gefa upp er að finna á [Búa til nýtt svæði fyrir rafræn viðskipti](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="1b1e2-111">For a complete explanation of the information that you must provide, see [Create a new e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="1b1e2-112">Eftir að vefsvæðið þitt er búið til geturðu staðfest að það sé tengt netversluninni þinni með því að velja flipann **Afurðir**. Þú ættir að sjá úrval af vörum sem hefur verið úthlutað í netverslunina.</span><span class="sxs-lookup"><span data-stu-id="1b1e2-112">After your site is created, you can verify that it's associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="1b1e2-113">Þú getur líka notað fellivalmyndina efst til vinstri á síðunni til að fá aðgang að vörunum eftir flokkum.</span><span class="sxs-lookup"><span data-stu-id="1b1e2-113">You can also use the drop-down field in the upper left of the page to access the products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b1e2-114">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="1b1e2-114">Additional resources</span></span>

[<span data-ttu-id="1b1e2-115">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="1b1e2-115">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="1b1e2-116">Uppsetning á nýjum leigjanda rafrænna viðskipta</span><span class="sxs-lookup"><span data-stu-id="1b1e2-116">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="1b1e2-117">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="1b1e2-117">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="1b1e2-118">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="1b1e2-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="1b1e2-119">Hlaða upp mörgum URL-framsendingum í einu</span><span class="sxs-lookup"><span data-stu-id="1b1e2-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="1b1e2-120">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="1b1e2-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="1b1e2-121">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="1b1e2-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="1b1e2-122">Stilla marga B2C leigjendur í viðskiptaumhverfi</span><span class="sxs-lookup"><span data-stu-id="1b1e2-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="1b1e2-123">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="1b1e2-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="1b1e2-124">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="1b1e2-124">Enable location-based store detection</span></span>](enable-store-detection.md)
