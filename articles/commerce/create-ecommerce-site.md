---
title: Stofna svæði fyrir rafræn viðskipti
description: Þetta efnisatriði lýsir verkum sem tengjast stofnun nýrrar netverslunarsíðu í Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
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
ms.openlocfilehash: 54259d3f5dfd8c8e1ff2caaadfac497cc0e133e0
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945836"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="b75da-103">Stofna svæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="b75da-103">Create an e-Commerce site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b75da-104">Þetta efnisatriði lýsir verkum sem tengjast stofnun nýrrar netverslunarsíðu í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b75da-104">This topic describes the tasks that are associated with the creation of a new e-Commerce site in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b75da-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="b75da-105">Overview</span></span>

<span data-ttu-id="b75da-106">Til að byrja að þróa netverslunarsíðuna þína verðurðu fyrst að stofna nýja síðu í umhverfi höfundaréttarins.</span><span class="sxs-lookup"><span data-stu-id="b75da-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="b75da-107">Áður en þú getur búið til nýja síðu verður að búa til að minnsta kosti eina netverslun í Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="b75da-107">Before you can create a new site, at least one online store must be created in Dynamics 365 Retail.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="b75da-108">Setja upp síðuna</span><span class="sxs-lookup"><span data-stu-id="b75da-108">Set up your site</span></span>

<span data-ttu-id="b75da-109">Til að setja upp síðuna þína skaltu gera eftirfarandi.</span><span class="sxs-lookup"><span data-stu-id="b75da-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="b75da-110">Í Microsoft Lifecycle Services (LCS) skaltu velja tengilinn fyrir höfundarumhverfið.</span><span class="sxs-lookup"><span data-stu-id="b75da-110">In Microsoft Lifecycle Services (LCS), select the link for the site authoring environment.</span></span> 
1. <span data-ttu-id="b75da-111">Á heimasíðunni fyrir höfundarumhverfi svæðisins velurðu **Ný síða**.</span><span class="sxs-lookup"><span data-stu-id="b75da-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="b75da-112">Í svarglugganum **Nýtt svæði** gefurðu upp eftirfarandi upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="b75da-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="b75da-113">Svæði</span><span class="sxs-lookup"><span data-stu-id="b75da-113">Field</span></span>                               | <span data-ttu-id="b75da-114">Lýsing</span><span class="sxs-lookup"><span data-stu-id="b75da-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="b75da-115">Svæðaheiti</span><span class="sxs-lookup"><span data-stu-id="b75da-115">Site name</span></span>                           | <span data-ttu-id="b75da-116">Sláðu inn skjáheitið sem ætti að nota fyrir síðuna þína í umhverfi höfundaréttarins.</span><span class="sxs-lookup"><span data-stu-id="b75da-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="b75da-117">Þetta nafn er aðeins sýnilegt í höfundarumhverfinu og verður ekki sýnt viðskiptavinum.</span><span class="sxs-lookup"><span data-stu-id="b75da-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="b75da-118">Öryggishópur vefstjórans</span><span class="sxs-lookup"><span data-stu-id="b75da-118">Site administrator's security group</span></span> | <span data-ttu-id="b75da-119">Tilgreindu Microsoft Azure Active Directory (Azure AD) öryggishóp sem heldur utan um notendur sem hafa hlutverk stjórnanda vefsins á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="b75da-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="b75da-120">Sjálfgefin rás (númer rekstrareiningar)</span><span class="sxs-lookup"><span data-stu-id="b75da-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="b75da-121">Veldu netverslunina sem þessi síða mun þjóna sem vefverslun fyrir.</span><span class="sxs-lookup"><span data-stu-id="b75da-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="b75da-122">Ef þú vilt að netverslunarsíðan þín styðji margar netverslanir, verður þú að tengja verslanirnar við síðuna þína á **Stillingar svæðis** eftir að svæðið er sett upp.</span><span class="sxs-lookup"><span data-stu-id="b75da-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="b75da-123">Sjálfgefið tungumál</span><span class="sxs-lookup"><span data-stu-id="b75da-123">Default language</span></span>                            | <span data-ttu-id="b75da-124">Tilgreindu sjálfgefið tungumál fyrir þessa netverslun og markað.</span><span class="sxs-lookup"><span data-stu-id="b75da-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="b75da-125">Netverslun getur stutt mörg tungumál.</span><span class="sxs-lookup"><span data-stu-id="b75da-125">An online store can support multiple languages.</span></span> <span data-ttu-id="b75da-126">Ef þú vilt styðja mörg tungumál fyrir þessa netverslun eða aðra netverslun geturðu stillt þann stuðning í **Stillingar svæðis** eftir að svæðið er settur upp.</span><span class="sxs-lookup"><span data-stu-id="b75da-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="b75da-127">Lén</span><span class="sxs-lookup"><span data-stu-id="b75da-127">Domain</span></span>                              | <span data-ttu-id="b75da-128">Veldu heiti léns sem mun þjóna sem lén fyrir þessa vefverslun.</span><span class="sxs-lookup"><span data-stu-id="b75da-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="b75da-129">Ef þú hefur ekki stillt nein lén í LCS geturðu haft þennan reit auðan.</span><span class="sxs-lookup"><span data-stu-id="b75da-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="b75da-130">Eftir að lénið þitt er stillt í LCS verðurðu að bæta því við netverslunina þína í **Stillingar svæðis**.</span><span class="sxs-lookup"><span data-stu-id="b75da-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="b75da-131">Slóð</span><span class="sxs-lookup"><span data-stu-id="b75da-131">Path</span></span>                              | <span data-ttu-id="b75da-132">Þegar vefsvæðið þitt styður fleiri en eitt tungumál fyrir tiltekið lén, notaðu slóðareitinn til að búa til einstaka vefslóð fyrir það lén og tungumálasamsetningu.</span><span class="sxs-lookup"><span data-stu-id="b75da-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="b75da-133">Ef tungumálið sem þú tilgreindir í reitnum **Sjálfgefið tungumál** er eina tungumálið sem þú munt styðja fyrir þetta lén eða heldur áfram að vera sjálfgefið tungumál eftir að þú hefur staðfært síðuna á fleiri tungumál mælum við með að þú hafir þennan reit auðan.</span><span class="sxs-lookup"><span data-stu-id="b75da-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="b75da-134">Eftir að vefsvæðið þitt er búið til geturðu staðfest að það er tengt netversluninni þinni með því að velja flipann **Afurðir**. Þú ættir að sjá úrval af vörum sem hefur verið úthlutað í netverslunina.</span><span class="sxs-lookup"><span data-stu-id="b75da-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="b75da-135">Þú getur líka notað fellivalmyndina efst til vinstri á síðunni til að fá aðgang að úthlutuðum afurðum eftir flokkum.</span><span class="sxs-lookup"><span data-stu-id="b75da-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b75da-136">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b75da-136">Additional resources</span></span>

[<span data-ttu-id="b75da-137">Skilgreina lénsheiti</span><span class="sxs-lookup"><span data-stu-id="b75da-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="b75da-138">Uppsetning á nýju vefsvæði fyrir rafræn viðskipti</span><span class="sxs-lookup"><span data-stu-id="b75da-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="b75da-139">Tengja netsvæði við rás</span><span class="sxs-lookup"><span data-stu-id="b75da-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="b75da-140">Vinna með skrárnar robots.txt</span><span class="sxs-lookup"><span data-stu-id="b75da-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="b75da-141">Setja upp sérsniðnar síður fyrir innskráningu notenda</span><span class="sxs-lookup"><span data-stu-id="b75da-141">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="b75da-142">Bæta við stuðningi fyrir efnisbirtingarnet (CDN)</span><span class="sxs-lookup"><span data-stu-id="b75da-142">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="b75da-143">Virkja greiningu á verslun eftir staðsetningu</span><span class="sxs-lookup"><span data-stu-id="b75da-143">Enable location-based store detection</span></span>](enable-store-detection.md)
