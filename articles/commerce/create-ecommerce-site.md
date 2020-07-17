---
title: Stofna svæði fyrir rafræn viðskipti
description: Þetta efni lýsir skrefum og upplýsingum sem þarf til að stofna nýja netverslunarsíðu á Dynamics 365 Commerce vefsvæðishönnuðinum.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
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
ms.openlocfilehash: ea3517a4f2b84db8a87a97d2f644bb4436f8693f
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533437"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="7809e-103">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="7809e-103">Create an e-Commerce site</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7809e-104">Þetta efni lýsir skrefum og upplýsingum sem þarf til að stofna nýja netverslunarsíðu á Dynamics 365 Commerce vefsvæðishönnuðinum.</span><span class="sxs-lookup"><span data-stu-id="7809e-104">This topic describes the steps and information required to create a new e-Commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="7809e-105">Þegar veitt er heimild fyrir rafrænum viðskiptamöguleikum, fær vefhönnuður úthlutað upphafssíðu sem hægt er að nota sem grunn fyrir eigin síðu.</span><span class="sxs-lookup"><span data-stu-id="7809e-105">When you license the e-Commerce capabilities, site builder will be provisioned with a starter site that you can use as a basis for your own site.</span></span> <span data-ttu-id="7809e-106">Ef þú vilt hins vegar byrja frá grunni eða ef þú vilt koma á öðru vefsvæði þarftu að koma á fót nýju svæði í hönnunarumhverfi vefsvæðis.</span><span class="sxs-lookup"><span data-stu-id="7809e-106">However, if you want to start from scratch or if you want to establish a second site, you will need to establish a new site in the site authoring environment.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="7809e-107">Setja upp síðuna</span><span class="sxs-lookup"><span data-stu-id="7809e-107">Set up your site</span></span>

<span data-ttu-id="7809e-108">Til að setja upp síðuna þína skaltu gera eftirfarandi.</span><span class="sxs-lookup"><span data-stu-id="7809e-108">To set up your site, do the following.</span></span>

1. <span data-ttu-id="7809e-109">Opnaðu umhverfi vefsvæðishönnuðar.</span><span class="sxs-lookup"><span data-stu-id="7809e-109">Open the site builder environment.</span></span> <span data-ttu-id="7809e-110">Þú getur fundið tengil á vefsvæði byggingaraðila í Microsoft Lifecycle Services (LCS) á umhverfisaðgerðarsíðunni fyrir Commerce.</span><span class="sxs-lookup"><span data-stu-id="7809e-110">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="7809e-111">Á heimasíðunni fyrir höfundarumhverfi svæðisins velurðu **Ný síða**.</span><span class="sxs-lookup"><span data-stu-id="7809e-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="7809e-112">Í svarglugganum **Nýtt svæði** gefurðu upp eftirfarandi upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="7809e-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="7809e-113">Svæði</span><span class="sxs-lookup"><span data-stu-id="7809e-113">Field</span></span>                               | <span data-ttu-id="7809e-114">Lýsing</span><span class="sxs-lookup"><span data-stu-id="7809e-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="7809e-115">Svæðaheiti</span><span class="sxs-lookup"><span data-stu-id="7809e-115">Site name</span></span>                           | <span data-ttu-id="7809e-116">Sláðu inn skjáheitið sem ætti að nota fyrir síðuna þína í umhverfi höfundaréttarins.</span><span class="sxs-lookup"><span data-stu-id="7809e-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="7809e-117">Þetta nafn er aðeins sýnilegt í höfundarumhverfinu og verður ekki sýnt viðskiptavinum.</span><span class="sxs-lookup"><span data-stu-id="7809e-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="7809e-118">Öryggishópur vefstjórans</span><span class="sxs-lookup"><span data-stu-id="7809e-118">Site administrator's security group</span></span> | <span data-ttu-id="7809e-119">Tilgreindu Microsoft Azure Active Directory (Azure AD) öryggishóp sem heldur utan um notendur sem hafa hlutverk stjórnanda vefsins á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="7809e-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="7809e-120">Sjálfgefin rás (númer rekstrareiningar)</span><span class="sxs-lookup"><span data-stu-id="7809e-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="7809e-121">Veldu netverslunina sem þessi síða mun þjóna sem vefverslun fyrir.</span><span class="sxs-lookup"><span data-stu-id="7809e-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="7809e-122">Ef þú vilt að netverslunarsíðan þín styðji margar netverslanir, verður þú að tengja verslanirnar við síðuna þína á **Stillingar svæðis** eftir að svæðið er sett upp.</span><span class="sxs-lookup"><span data-stu-id="7809e-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="7809e-123">Sjálfgefið tungumál</span><span class="sxs-lookup"><span data-stu-id="7809e-123">Default language</span></span>                            | <span data-ttu-id="7809e-124">Tilgreindu sjálfgefið tungumál fyrir þessa netverslun og markað.</span><span class="sxs-lookup"><span data-stu-id="7809e-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="7809e-125">Netverslun getur stutt mörg tungumál.</span><span class="sxs-lookup"><span data-stu-id="7809e-125">An online store can support multiple languages.</span></span> <span data-ttu-id="7809e-126">Ef þú vilt styðja mörg tungumál fyrir þessa netverslun eða aðra netverslun geturðu stillt þann stuðning í **Stillingar svæðis** eftir að svæðið er settur upp.</span><span class="sxs-lookup"><span data-stu-id="7809e-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="7809e-127">Lén</span><span class="sxs-lookup"><span data-stu-id="7809e-127">Domain</span></span>                              | <span data-ttu-id="7809e-128">Veldu heiti léns sem mun þjóna sem lén fyrir þessa vefverslun.</span><span class="sxs-lookup"><span data-stu-id="7809e-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="7809e-129">Ef þú hefur ekki stillt nein lén í LCS geturðu haft þennan reit auðan.</span><span class="sxs-lookup"><span data-stu-id="7809e-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="7809e-130">Eftir að lénið þitt er stillt í LCS verðurðu að bæta því við netverslunina þína í **Stillingar svæðis**.</span><span class="sxs-lookup"><span data-stu-id="7809e-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="7809e-131">Slóð</span><span class="sxs-lookup"><span data-stu-id="7809e-131">Path</span></span>                              | <span data-ttu-id="7809e-132">Þegar vefsvæðið þitt styður fleiri en eitt tungumál fyrir tiltekið lén, notaðu slóðareitinn til að búa til einstaka vefslóð fyrir það lén og tungumálasamsetningu.</span><span class="sxs-lookup"><span data-stu-id="7809e-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="7809e-133">Ef tungumálið sem þú tilgreindir í reitnum **Sjálfgefið tungumál** er eina tungumálið sem þú munt styðja fyrir þetta lén eða heldur áfram að vera sjálfgefið tungumál eftir að þú hefur staðfært síðuna á fleiri tungumál mælum við með að þú hafir þennan reit auðan.</span><span class="sxs-lookup"><span data-stu-id="7809e-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="7809e-134">Eftir að vefsvæðið þitt er búið til geturðu staðfest að það er tengt netversluninni þinni með því að velja flipann **Afurðir**. Þú ættir að sjá úrval af vörum sem hefur verið úthlutað í netverslunina.</span><span class="sxs-lookup"><span data-stu-id="7809e-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="7809e-135">Þú getur líka notað fellivalmyndina efst til vinstri á síðunni til að fá aðgang að úthlutuðum afurðum eftir flokkum.</span><span class="sxs-lookup"><span data-stu-id="7809e-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7809e-136">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7809e-136">Additional resources</span></span>

[<span data-ttu-id="7809e-137">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="7809e-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="7809e-138">Uppsetning á nýju vefsvæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="7809e-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="7809e-139">Tengja netsvæði við rás</span><span class="sxs-lookup"><span data-stu-id="7809e-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="7809e-140">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="7809e-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="7809e-141">Hlaða upp mörgum slóðartilvísunum í einu</span><span class="sxs-lookup"><span data-stu-id="7809e-141">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="7809e-142">Setja upp B2C-leigjanda í Commerce</span><span class="sxs-lookup"><span data-stu-id="7809e-142">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="7809e-143">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="7809e-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="7809e-144">Stilla marga B2C leigjendur í viðskiptaumhverfi</span><span class="sxs-lookup"><span data-stu-id="7809e-144">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="7809e-145">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="7809e-145">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="7809e-146">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="7809e-146">Enable location-based store detection</span></span>](enable-store-detection.md)
