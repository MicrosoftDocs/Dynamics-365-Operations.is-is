---
title: Bæta við lógói
description: Þetta efni lýsir því hvernig á að bæta merki við á vefsvæði í Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
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
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914623"
---
# <a name="add-a-logo"></a><span data-ttu-id="57f84-103">Bæta við lógói</span><span class="sxs-lookup"><span data-stu-id="57f84-103">Add a logo</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="57f84-104">Þetta efni lýsir því hvernig á að bæta merki við á vefsvæði í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="57f84-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="57f84-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="57f84-105">Overview</span></span>

<span data-ttu-id="57f84-106">Þegar þú byggir vefsvæðið er eitt af fyrstu hlutunum sem þú munt líklega gera er að bæta fyrirtækinu þínu eða merki vörumerkis við haus svæðisins.</span><span class="sxs-lookup"><span data-stu-id="57f84-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="57f84-107">Byrjunareining Dynamics 365 Commerce á netinu veitir einingu sem gerir þetta verkefni auðvelt.</span><span class="sxs-lookup"><span data-stu-id="57f84-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="57f84-108">Þú getur bætt merki beint við í sniðmát, skipulag eða síðu.</span><span class="sxs-lookup"><span data-stu-id="57f84-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="57f84-109">Á þennan hátt geturðu auðveldlega breytt merkinu sem birtist á tilteknum síðum eða síðuhópum.</span><span class="sxs-lookup"><span data-stu-id="57f84-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="57f84-110">En þetta efni nær yfir algengustu atburðarásina, þar sem þú bætir merkinu við hausbrot sem hægt er að endurnýta á öllum síðum vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="57f84-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="57f84-111">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="57f84-111">Prerequisites</span></span>

<span data-ttu-id="57f84-112">Það verður að ljúka þessum verkefnum áður en þú getur bætt merki við allar síður vefsvæðisins.</span><span class="sxs-lookup"><span data-stu-id="57f84-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="57f84-113">Flyttu merkið þitt upp á stafræna eignastjórann sem þú getur fengið aðgang að af síðunni **Eignir**.</span><span class="sxs-lookup"><span data-stu-id="57f84-113">Upload your logo to the digital assets manager, which you can access from the **Assets** page.</span></span>
1. <span data-ttu-id="57f84-114">Stofna hausbrot.</span><span class="sxs-lookup"><span data-stu-id="57f84-114">Create a header fragment.</span></span> <span data-ttu-id="57f84-115">Fyrir frekari upplýsingar um hvernig á að búa til og nota brot, sjá [Unnið með brot](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="57f84-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="57f84-116">Láttu hausbrotið fylgja með í sniðmátinu sem vefsíður þínar nota fyrir skipulags- og einingavalkosti.</span><span class="sxs-lookup"><span data-stu-id="57f84-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="57f84-117">Nánari upplýsingar um sniðmát er að finna í [Unnið með sniðmát](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="57f84-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="57f84-118">Bæta merki við hausbrot</span><span class="sxs-lookup"><span data-stu-id="57f84-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="57f84-119">Fylgdu þessum skrefum til að bæta við merki við hausbrotið fyrir vefsvæðið.</span><span class="sxs-lookup"><span data-stu-id="57f84-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="57f84-120">Í yfirlitssvæðinu til vinstri velurðu **Brot** og velur síðan hausbrotið sem var stofnað.</span><span class="sxs-lookup"><span data-stu-id="57f84-120">In the navigation pane on the left, select **Fragments**, and then select the header fragment that you created.</span></span>
2. <span data-ttu-id="57f84-121">Velja **Skrá út**.</span><span class="sxs-lookup"><span data-stu-id="57f84-121">Select **Check out**.</span></span>
3. <span data-ttu-id="57f84-122">Stækkaðu hólfið **Haus** og hólfið **Merki**.</span><span class="sxs-lookup"><span data-stu-id="57f84-122">Expand the **Header** slot and the **Logo** slot.</span></span>
4. <span data-ttu-id="57f84-123">Veldu úrfellingarhnappinn (**...**) fyrir hólfið **Merki** og veldu síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="57f84-123">Select the ellipsis button (**...**) for the **Logo** slot, and then select **Add module**.</span></span>
5. <span data-ttu-id="57f84-124">Veldu merkiseininguna.</span><span class="sxs-lookup"><span data-stu-id="57f84-124">Select the logo module.</span></span>
6. <span data-ttu-id="57f84-125">Í eiginleikaglugganum til hægri stillirðu merkjaeininguna þannig að hún sýni merkið þitt.</span><span class="sxs-lookup"><span data-stu-id="57f84-125">In the properties pane on the right, configure the logo module so that it shows your logo.</span></span>
7. <span data-ttu-id="57f84-126">Vistaðu fyrirsagnarbrotið, skráðu það inn og gefðu það út.</span><span class="sxs-lookup"><span data-stu-id="57f84-126">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="57f84-127">Eftir að þú hefur birt uppfært hausbrot birta allar vefsíðurnar sem nota sniðmátið sem inniheldur hausbrotið merkið þitt.</span><span class="sxs-lookup"><span data-stu-id="57f84-127">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="57f84-128">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="57f84-128">Additional resources</span></span>

[<span data-ttu-id="57f84-129">Velja þema svæðis</span><span class="sxs-lookup"><span data-stu-id="57f84-129">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="57f84-130">Unnið með CSS hnekkiskrám</span><span class="sxs-lookup"><span data-stu-id="57f84-130">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="57f84-131">Bæta við táknmynd</span><span class="sxs-lookup"><span data-stu-id="57f84-131">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="57f84-132">Bæta við opnunarkveðju</span><span class="sxs-lookup"><span data-stu-id="57f84-132">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="57f84-133">Bæta við yfirlýsingu um höfundarrétt</span><span class="sxs-lookup"><span data-stu-id="57f84-133">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="57f84-134">Bæta tungumálum við síðuna</span><span class="sxs-lookup"><span data-stu-id="57f84-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="57f84-135">Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar</span><span class="sxs-lookup"><span data-stu-id="57f84-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

