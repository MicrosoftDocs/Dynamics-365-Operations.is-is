---
title: Bæta við lógói
description: Þetta efni lýsir því hvernig á að bæta merki við á vefsvæði í Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 01/23/2020
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
ms.openlocfilehash: 62b8237fa0c30fa9d901d670de38416cf8615c8d
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686647"
---
# <a name="add-a-logo"></a><span data-ttu-id="2b055-103">Bæta við lógói</span><span class="sxs-lookup"><span data-stu-id="2b055-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2b055-104">Þetta efni lýsir því hvernig á að bæta merki við á vefsvæði í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2b055-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2b055-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="2b055-105">Overview</span></span>

<span data-ttu-id="2b055-106">Þegar þú byggir vefsvæðið er eitt af fyrstu hlutunum sem þú munt líklega gera er að bæta fyrirtækinu þínu eða merki vörumerkis við haus svæðisins.</span><span class="sxs-lookup"><span data-stu-id="2b055-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="2b055-107">Byrjunareining Dynamics 365 Commerce á netinu veitir einingu sem gerir þetta verkefni auðvelt.</span><span class="sxs-lookup"><span data-stu-id="2b055-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="2b055-108">Þú getur bætt merki beint við í sniðmát, skipulag eða síðu.</span><span class="sxs-lookup"><span data-stu-id="2b055-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="2b055-109">Á þennan hátt geturðu auðveldlega breytt merkinu sem birtist á tilteknum síðum eða síðuhópum.</span><span class="sxs-lookup"><span data-stu-id="2b055-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="2b055-110">En þetta efni nær yfir algengustu atburðarásina, þar sem þú bætir merkinu við hausbrot sem hægt er að endurnýta á öllum síðum vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="2b055-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2b055-111">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="2b055-111">Prerequisites</span></span>

<span data-ttu-id="2b055-112">Það verður að ljúka þessum verkefnum áður en þú getur bætt merki við allar síður vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="2b055-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="2b055-113">Hladdu upp lógóinu þínu í fjölmiðlasafnið.</span><span class="sxs-lookup"><span data-stu-id="2b055-113">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="2b055-114">Stofna hausbrot.</span><span class="sxs-lookup"><span data-stu-id="2b055-114">Create a header fragment.</span></span> <span data-ttu-id="2b055-115">Fyrir frekari upplýsingar um hvernig á að búa til og nota brot, sjá [Unnið með brot](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="2b055-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="2b055-116">Láttu hausbrotið fylgja með í sniðmátinu sem vefsíður þínar nota fyrir skipulags- og einingavalkosti.</span><span class="sxs-lookup"><span data-stu-id="2b055-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="2b055-117">Nánari upplýsingar um sniðmát er að finna í [Unnið með sniðmát](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="2b055-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="2b055-118">Bæta merki við hausbrot</span><span class="sxs-lookup"><span data-stu-id="2b055-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="2b055-119">Fylgdu þessum skrefum til að bæta við merki við hausbrotið fyrir vefsvæðið.</span><span class="sxs-lookup"><span data-stu-id="2b055-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="2b055-120">Í stýriglugganum vinstra megin velurðu **Brot**.</span><span class="sxs-lookup"><span data-stu-id="2b055-120">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="2b055-121">Veldu hausbrotið sem þú bjóst til og veldu síðan **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="2b055-121">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="2b055-122">Stækkaðu hausseininguna.</span><span class="sxs-lookup"><span data-stu-id="2b055-122">Expand the header module.</span></span>
1. <span data-ttu-id="2b055-123">Settu upp mynd og tengil fyrir lógóið í eiginleikaglugganum fyrir hausseininguna.</span><span class="sxs-lookup"><span data-stu-id="2b055-123">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="2b055-124">Vistaðu hausbrotið, ljúktu við að breyta því og birtu það.</span><span class="sxs-lookup"><span data-stu-id="2b055-124">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="2b055-125">Eftir að þú hefur birt uppfært hausbrot birta allar vefsíðurnar sem nota sniðmátið sem inniheldur hausbrotið merkið þitt.</span><span class="sxs-lookup"><span data-stu-id="2b055-125">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2b055-126">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="2b055-126">Additional resources</span></span>

[<span data-ttu-id="2b055-127">Velja þema svæðis</span><span class="sxs-lookup"><span data-stu-id="2b055-127">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="2b055-128">Unnið með CSS hnekkiskrám</span><span class="sxs-lookup"><span data-stu-id="2b055-128">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="2b055-129">Bæta við táknmynd</span><span class="sxs-lookup"><span data-stu-id="2b055-129">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="2b055-130">Bæta við opnunarkveðju</span><span class="sxs-lookup"><span data-stu-id="2b055-130">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="2b055-131">Bæta við yfirlýsingu um höfundarrétt</span><span class="sxs-lookup"><span data-stu-id="2b055-131">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="2b055-132">Bæta tungumálum við síðuna</span><span class="sxs-lookup"><span data-stu-id="2b055-132">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="2b055-133">Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar</span><span class="sxs-lookup"><span data-stu-id="2b055-133">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

