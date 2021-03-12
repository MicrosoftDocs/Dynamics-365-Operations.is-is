---
title: Velja þema svæðis
description: Þetta efni lýsir því hvernig á að stilla eða breyta þema vefsvæðis þíns í Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 66fcff9fa18d3c98e022ef91d15903fbba8b6b61
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982405"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="0e8eb-103">Velja þema svæðis</span><span class="sxs-lookup"><span data-stu-id="0e8eb-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0e8eb-104">Þetta efni lýsir því hvernig á að stilla eða breyta þema vefsvæðis þíns í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0e8eb-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0e8eb-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="0e8eb-105">Overview</span></span>

<span data-ttu-id="0e8eb-106">Útlit og stíll vefsvæðis (til dæmis leturgerðir, stærðir og litir) eru skilgreind af þema sem þú velur og beitir á síðuna.</span><span class="sxs-lookup"><span data-stu-id="0e8eb-106">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="0e8eb-107">Þema er búið til og sent af þróunaraðila hjá fyrirtækinu þínu.</span><span class="sxs-lookup"><span data-stu-id="0e8eb-107">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="0e8eb-108">Fyrir yfirlit yfir þemu skal sjá [Yfirlit yfir þemu](e-commerce-extensibility/theming.md).</span><span class="sxs-lookup"><span data-stu-id="0e8eb-108">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="0e8eb-109">Nánari upplýsingar um hvernig á að stofna og nota þeum eru í [Stofna nýtt þema](e-commerce-extensibility/create-theme.md).</span><span class="sxs-lookup"><span data-stu-id="0e8eb-109">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="0e8eb-110">Þegar þú stofnar vefsíðu notar hún sjálfgefið þema sem heitir **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="0e8eb-110">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="0e8eb-111">Þetta sjálfgefna þema er veitt sem hluti af einingasafni Commerce.</span><span class="sxs-lookup"><span data-stu-id="0e8eb-111">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="0e8eb-112">Eftir að þú hefur notað fleiri þemu fyrir síðuna þína geturðu stillt vefsvæðið þannig að hann noti eitt af þeim í staðinn.</span><span class="sxs-lookup"><span data-stu-id="0e8eb-112">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="0e8eb-113">Veldu þema svæðis</span><span class="sxs-lookup"><span data-stu-id="0e8eb-113">Select the site theme</span></span>

<span data-ttu-id="0e8eb-114">Fylgdu þessum skrefum til að velja þemað sem er notað á síðuna þína.</span><span class="sxs-lookup"><span data-stu-id="0e8eb-114">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="0e8eb-115">Í höfundaumhverfi svæðisins ferðu á vefsvæðið.</span><span class="sxs-lookup"><span data-stu-id="0e8eb-115">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="0e8eb-116">Farðu á **Svæðisstjórnun** \> **Stækkunarhæfni**.</span><span class="sxs-lookup"><span data-stu-id="0e8eb-116">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="0e8eb-117">Undir **Þema** velurðu þema á fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="0e8eb-117">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="0e8eb-118">Til að nota valið þema á vefsvæðið velurðu **Vista og birta**.</span><span class="sxs-lookup"><span data-stu-id="0e8eb-118">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="0e8eb-119">Þemað sem þú velur er birt á vefsvæðið um leið og þú velur **Vista og birta** á síðunni **Stækkanleiki**.</span><span class="sxs-lookup"><span data-stu-id="0e8eb-119">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="0e8eb-120">Til að forskoða þema á vefsvæðinu áður en þú notar það geturðu notað þróunar- eða sandkassaumhverfi.</span><span class="sxs-lookup"><span data-stu-id="0e8eb-120">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e8eb-121">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="0e8eb-121">Additional resources</span></span>

[<span data-ttu-id="0e8eb-122">Bæta við lógói</span><span class="sxs-lookup"><span data-stu-id="0e8eb-122">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="0e8eb-123">Unnið með CSS hnekkiskrám</span><span class="sxs-lookup"><span data-stu-id="0e8eb-123">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="0e8eb-124">Bæta við táknmynd</span><span class="sxs-lookup"><span data-stu-id="0e8eb-124">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="0e8eb-125">Bæta við opnunarkveðju</span><span class="sxs-lookup"><span data-stu-id="0e8eb-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="0e8eb-126">Bæta við yfirlýsingu um höfundarrétt</span><span class="sxs-lookup"><span data-stu-id="0e8eb-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="0e8eb-127">Bæta tungumálum við síðuna</span><span class="sxs-lookup"><span data-stu-id="0e8eb-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="0e8eb-128">Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar</span><span class="sxs-lookup"><span data-stu-id="0e8eb-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="0e8eb-129">Yfirlit yfir þemu</span><span class="sxs-lookup"><span data-stu-id="0e8eb-129">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="0e8eb-130">Búa til nýtt þema</span><span class="sxs-lookup"><span data-stu-id="0e8eb-130">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)

