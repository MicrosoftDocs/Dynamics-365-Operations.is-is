---
title: Staðfesta aðgengi að efni síðu
description: Þetta efni lýsir því hvernig hægt er að sannreyna aðgengi að síðuinnihaldi í Microsoft Dynamics 365 Commerce.
author: josaw1
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: fc3dca673510e1636f497bb7d5c295bebe025677
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4413285"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="ea50a-103">Staðfesta aðgengi að efni síðu</span><span class="sxs-lookup"><span data-stu-id="ea50a-103">Verify page content accessibility</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ea50a-104">Þetta efni lýsir því hvernig hægt er að sannreyna aðgengi að síðuinnihaldi í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ea50a-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ea50a-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="ea50a-105">Overview</span></span>

<span data-ttu-id="ea50a-106">Þegar þú hefur lokið við að breyta síðu ættirðu að ganga úr skugga um að innihaldið sé aðgengilegt fyrir alla á vefnum.</span><span class="sxs-lookup"><span data-stu-id="ea50a-106">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="ea50a-107">Í höfundatækjum Commerce geturðu auðveldlega sannreynt aðgengi síðuefnisins með því að nota samþættu þjónustuna [Microsoft Accessibility Insights](https://accessibilityinsights.io/).</span><span class="sxs-lookup"><span data-stu-id="ea50a-107">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="ea50a-108">Þessi þjónusta sannreynir innihald síðunnar gagnvart nýjustu viðmiðunarreglunum [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility).</span><span class="sxs-lookup"><span data-stu-id="ea50a-108">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="ea50a-109">Kveikja verður á samþættingu [Microsoft Accessibility Insights](https://accessibilityinsights.io/) á leigjanda- eða vefsvæðisstigi áður en hægt er að nota hana.</span><span class="sxs-lookup"><span data-stu-id="ea50a-109">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="ea50a-110">Kveiktu á Microsoft Accessibility Insights fyrir öll vefsvæði leigjandans</span><span class="sxs-lookup"><span data-stu-id="ea50a-110">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="ea50a-111">Til að kveikja á [Microsoft Accessibility Insights](https://accessibilityinsights.io/) fyrir öll svæði Commerce í leigjandanum skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ea50a-111">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="ea50a-112">Til að fara í leigjandastillingar verður þú að vera skráð/ur inn í Commerce sem kerfisstjóri.</span><span class="sxs-lookup"><span data-stu-id="ea50a-112">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="ea50a-113">Skráðu þig inn í Commerce sem kerfisstjóri.</span><span class="sxs-lookup"><span data-stu-id="ea50a-113">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="ea50a-114">Í vinstri stýriglugganum velurðu **Leigjandastillingar** (við hlið gírstáknsins) til að stækka hann.</span><span class="sxs-lookup"><span data-stu-id="ea50a-114">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="ea50a-115">Undir **Leigjandastillingar** velurðu **Eiginleikar**.</span><span class="sxs-lookup"><span data-stu-id="ea50a-115">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="ea50a-116">Stilltu valkostinn **Aðgengisathugun** **Kveikt**.</span><span class="sxs-lookup"><span data-stu-id="ea50a-116">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="ea50a-117">Kveiktu á Microsoft Accessibility Insights fyrir stakt vefsvæði</span><span class="sxs-lookup"><span data-stu-id="ea50a-117">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="ea50a-118">Til að kveikja á [Microsoft Accessibility Insights](https://accessibilityinsights.io/) fyrir stakt svæði Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ea50a-118">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="ea50a-119">Undir **Svæði** velurðu **Fabrikam** (eða heiti svæðisins).</span><span class="sxs-lookup"><span data-stu-id="ea50a-119">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="ea50a-120">Í vinstri yfirlitsglugganum velurðu **Svæðisstillingar** til að stækka hann.</span><span class="sxs-lookup"><span data-stu-id="ea50a-120">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="ea50a-121">Undir **Svæðisstillingar** velurðu **Eiginleikar**.</span><span class="sxs-lookup"><span data-stu-id="ea50a-121">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="ea50a-122">Stilltu valkostinn **Aðgengisathugun** **Kveikt**.</span><span class="sxs-lookup"><span data-stu-id="ea50a-122">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="ea50a-123">Staðfestu aðgengi efnisins á heimasíðunni</span><span class="sxs-lookup"><span data-stu-id="ea50a-123">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="ea50a-124">Til að nota samþætta þjónustu [Microsoft Accessibility Insights](https://accessibilityinsights.io/) til að skanna og staðfesta innihald heimasíðunnar í Commerce skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ea50a-124">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="ea50a-125">Undir **Svæði** velurðu **Fabrikam** (eða heiti svæðisins).</span><span class="sxs-lookup"><span data-stu-id="ea50a-125">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="ea50a-126">Í vinstri stýriglugganum velurðu **Síður**.</span><span class="sxs-lookup"><span data-stu-id="ea50a-126">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="ea50a-127">Finndu og veldu heimasíðuna til að opna hana í ritlinum.</span><span class="sxs-lookup"><span data-stu-id="ea50a-127">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="ea50a-128">Á skipanastikunni velurðu **Athuga aðgengi**.</span><span class="sxs-lookup"><span data-stu-id="ea50a-128">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="ea50a-129">Síðan **Athuga aðgengi** birtist.</span><span class="sxs-lookup"><span data-stu-id="ea50a-129">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="ea50a-130">Eftir að skönnuninni er lokið skaltu skoða innihald skýrslunnar.</span><span class="sxs-lookup"><span data-stu-id="ea50a-130">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="ea50a-131">Ef einhverjar athuganir misfórust skaltu velja hvert misheppnað athugunaratriði til að stækka það svo hægt sé að skoða frekari upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="ea50a-131">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="ea50a-132">Til að loka skýrslunni eftir að þú hefur lokið við að skoða hana skal fletta neðst á síðuna **Athuga aðgengi** og velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ea50a-132">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea50a-133">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ea50a-133">Additional resources</span></span>

[<span data-ttu-id="ea50a-134">Breyta síðu svæðis sem þegar er til</span><span class="sxs-lookup"><span data-stu-id="ea50a-134">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="ea50a-135">Bæta við nýrri síðu á svæði</span><span class="sxs-lookup"><span data-stu-id="ea50a-135">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="ea50a-136">Velja síðuútlit</span><span class="sxs-lookup"><span data-stu-id="ea50a-136">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="ea50a-137">Stjórna SEO-lýsigögnum</span><span class="sxs-lookup"><span data-stu-id="ea50a-137">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="ea50a-138">Vista, forskoða og birta síðu</span><span class="sxs-lookup"><span data-stu-id="ea50a-138">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="ea50a-139">Bæta vörusíðu</span><span class="sxs-lookup"><span data-stu-id="ea50a-139">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="ea50a-140">Bæta lendingarsíðu flokks</span><span class="sxs-lookup"><span data-stu-id="ea50a-140">Enrich a category landing page</span></span>](enrich-category-page.md)
