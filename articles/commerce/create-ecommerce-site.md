---
title: Stofna svæði fyrir rafræn viðskipti
description: Þetta efni lýsir skrefum og upplýsingum sem þarf til að stofna nýja netverslunarsíðu á Dynamics 365 Commerce vefsvæðishönnuðinum.
author: bicyclingfool
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
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7177bae911dfa91a645b40581bf23b3ed76562a3
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096775"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="dce2b-103">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="dce2b-103">Create an e-Commerce site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="dce2b-104">Þetta efni lýsir skrefum og upplýsingum sem þarf til að stofna nýja netverslunarsíðu á Dynamics 365 Commerce vefsvæðishönnuðinum.</span><span class="sxs-lookup"><span data-stu-id="dce2b-104">This topic describes the steps and information required to create a new e-Commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="dce2b-105">Áður en hægt er að hefja þróun á netverslunarsíðunni verðurðu fyrst að stofna nýja síðu í vefsvæðishönnuðinum.</span><span class="sxs-lookup"><span data-stu-id="dce2b-105">Before you can start developing your e-Commerce site, you must first establish a new site in site builder.</span></span> 


<span data-ttu-id="dce2b-106">Til að byrja að þróa netverslunarsíðuna þína verðurðu fyrst að stofna nýja síðu í umhverfi höfundaréttarins.</span><span class="sxs-lookup"><span data-stu-id="dce2b-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="dce2b-107">Áður en þú getur búið til nýja síðu verður að búa til að minnsta kosti eina netverslun í Commerce.</span><span class="sxs-lookup"><span data-stu-id="dce2b-107">Before you can create a new site, at least one online store must be created in Commerce.</span></span> 


## <a name="set-up-your-site"></a><span data-ttu-id="dce2b-108">Setja upp síðuna</span><span class="sxs-lookup"><span data-stu-id="dce2b-108">Set up your site</span></span>

<span data-ttu-id="dce2b-109">Til að setja upp síðuna þína skaltu gera eftirfarandi.</span><span class="sxs-lookup"><span data-stu-id="dce2b-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="dce2b-110">Opnaðu umhverfi vefsvæðishönnuðar.</span><span class="sxs-lookup"><span data-stu-id="dce2b-110">Open the site builder environment.</span></span> <span data-ttu-id="dce2b-111">Þú getur fundið tengil á vefsvæði byggingaraðila í Microsoft Lifecycle Services (LCS) á umhverfisaðgerðarsíðunni fyrir Commerce.</span><span class="sxs-lookup"><span data-stu-id="dce2b-111">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="dce2b-112">Á heimasíðunni fyrir höfundarumhverfi svæðisins velurðu **Ný síða**.</span><span class="sxs-lookup"><span data-stu-id="dce2b-112">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="dce2b-113">Í svarglugganum **Nýtt svæði** gefurðu upp eftirfarandi upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="dce2b-113">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="dce2b-114">Svæði</span><span class="sxs-lookup"><span data-stu-id="dce2b-114">Field</span></span>                               | <span data-ttu-id="dce2b-115">Lýsing</span><span class="sxs-lookup"><span data-stu-id="dce2b-115">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="dce2b-116">Svæðaheiti</span><span class="sxs-lookup"><span data-stu-id="dce2b-116">Site name</span></span>                           | <span data-ttu-id="dce2b-117">Sláðu inn skjáheitið sem ætti að nota fyrir síðuna þína í umhverfi höfundaréttarins.</span><span class="sxs-lookup"><span data-stu-id="dce2b-117">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="dce2b-118">Þetta nafn er aðeins sýnilegt í höfundarumhverfinu og verður ekki sýnt viðskiptavinum.</span><span class="sxs-lookup"><span data-stu-id="dce2b-118">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="dce2b-119">Öryggishópur vefstjórans</span><span class="sxs-lookup"><span data-stu-id="dce2b-119">Site administrator's security group</span></span> | <span data-ttu-id="dce2b-120">Tilgreindu Microsoft Azure Active Directory (Azure AD) öryggishóp sem heldur utan um notendur sem hafa hlutverk stjórnanda vefsins á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="dce2b-120">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="dce2b-121">Sjálfgefin rás (númer rekstrareiningar)</span><span class="sxs-lookup"><span data-stu-id="dce2b-121">Default channel (operating unit number)</span></span> | <span data-ttu-id="dce2b-122">Veldu netverslunina sem þessi síða mun þjóna sem vefverslun fyrir.</span><span class="sxs-lookup"><span data-stu-id="dce2b-122">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="dce2b-123">Ef þú vilt að netverslunarsíðan þín styðji margar netverslanir, verður þú að tengja verslanirnar við síðuna þína á **Stillingar svæðis** eftir að svæðið er sett upp.</span><span class="sxs-lookup"><span data-stu-id="dce2b-123">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="dce2b-124">Sjálfgefið tungumál</span><span class="sxs-lookup"><span data-stu-id="dce2b-124">Default language</span></span>                            | <span data-ttu-id="dce2b-125">Tilgreindu sjálfgefið tungumál fyrir þessa netverslun og markað.</span><span class="sxs-lookup"><span data-stu-id="dce2b-125">Specify the default language for this online store and market.</span></span> <span data-ttu-id="dce2b-126">Netverslun getur stutt mörg tungumál.</span><span class="sxs-lookup"><span data-stu-id="dce2b-126">An online store can support multiple languages.</span></span> <span data-ttu-id="dce2b-127">Ef þú vilt styðja mörg tungumál fyrir þessa netverslun eða aðra netverslun geturðu stillt þann stuðning í **Stillingar svæðis** eftir að svæðið er settur upp.</span><span class="sxs-lookup"><span data-stu-id="dce2b-127">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="dce2b-128">Lén</span><span class="sxs-lookup"><span data-stu-id="dce2b-128">Domain</span></span>                              | <span data-ttu-id="dce2b-129">Veldu heiti léns sem mun þjóna sem lén fyrir þessa vefverslun.</span><span class="sxs-lookup"><span data-stu-id="dce2b-129">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="dce2b-130">Ef þú hefur ekki stillt nein lén í LCS geturðu haft þennan reit auðan.</span><span class="sxs-lookup"><span data-stu-id="dce2b-130">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="dce2b-131">Eftir að lénið þitt er stillt í LCS verðurðu að bæta því við netverslunina þína í **Stillingar svæðis**.</span><span class="sxs-lookup"><span data-stu-id="dce2b-131">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="dce2b-132">Slóð</span><span class="sxs-lookup"><span data-stu-id="dce2b-132">Path</span></span>                              | <span data-ttu-id="dce2b-133">Þegar vefsvæðið þitt styður fleiri en eitt tungumál fyrir tiltekið lén, notaðu slóðareitinn til að búa til einstaka vefslóð fyrir það lén og tungumálasamsetningu.</span><span class="sxs-lookup"><span data-stu-id="dce2b-133">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="dce2b-134">Ef tungumálið sem þú tilgreindir í reitnum **Sjálfgefið tungumál** er eina tungumálið sem þú munt styðja fyrir þetta lén eða heldur áfram að vera sjálfgefið tungumál eftir að þú hefur staðfært síðuna á fleiri tungumál mælum við með að þú hafir þennan reit auðan.</span><span class="sxs-lookup"><span data-stu-id="dce2b-134">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="dce2b-135">Eftir að vefsvæðið þitt er búið til geturðu staðfest að það er tengt netversluninni þinni með því að velja flipann **Afurðir**. Þú ættir að sjá úrval af vörum sem hefur verið úthlutað í netverslunina.</span><span class="sxs-lookup"><span data-stu-id="dce2b-135">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="dce2b-136">Þú getur líka notað fellivalmyndina efst til vinstri á síðunni til að fá aðgang að úthlutuðum afurðum eftir flokkum.</span><span class="sxs-lookup"><span data-stu-id="dce2b-136">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dce2b-137">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="dce2b-137">Additional resources</span></span>

[<span data-ttu-id="dce2b-138">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="dce2b-138">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="dce2b-139">Uppsetning á nýju vefsvæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="dce2b-139">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="dce2b-140">Setja upp netverslunarrás</span><span class="sxs-lookup"><span data-stu-id="dce2b-140">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="dce2b-141">Tengja netsvæði við rás</span><span class="sxs-lookup"><span data-stu-id="dce2b-141">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="dce2b-142">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="dce2b-142">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="dce2b-143">Hlaða upp mörgum slóðartilvísunum í einu</span><span class="sxs-lookup"><span data-stu-id="dce2b-143">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="dce2b-144">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="dce2b-144">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="dce2b-145">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="dce2b-145">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="dce2b-146">Stilla marga B2C leigjendur í viðskiptaumhverfi</span><span class="sxs-lookup"><span data-stu-id="dce2b-146">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="dce2b-147">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="dce2b-147">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="dce2b-148">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="dce2b-148">Enable location-based store detection</span></span>](enable-store-detection.md)
