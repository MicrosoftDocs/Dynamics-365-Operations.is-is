---
title: Bæta við opnunarkveðju
description: Þetta efnisatriði lýsir því hvernig á að bæta móttökuskilaboðum við Microsoft Dynamics 365 Commerce vefsvæði.
author: psimolin
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d2a125b4e71016ad620f128af2e3c9f29aa04f4c
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269614"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="cf1a8-103">Bæta við opnunarkveðju</span><span class="sxs-lookup"><span data-stu-id="cf1a8-103">Add a welcome message</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cf1a8-104">Þetta efnisatriði lýsir því hvernig á að bæta móttökuskilaboðum við Microsoft Dynamics 365 Commerce vefsvæði.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="cf1a8-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="cf1a8-105">Overview</span></span>

<span data-ttu-id="cf1a8-106">Móttökuskilaboð á vefsíðu rafrænna viðskipta geta tilkynnt gestum um áframhaldandi útsölu, uppfærslur á vefnum eða framboð á árstíðabundnum línum.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="cf1a8-107">Móttökuskilaboðin eru stillt með því að nota viðvörunareininguna.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="cf1a8-108">Viðvörunareiningunni ætti að bæta við hólfið **Villu-/upplýsingaskilaboð** í fyrirsagnarbrotinu.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="cf1a8-109">Viðvörunareiningin gerir þér kleift að tilgreina textann sem er sýndur, textalitinn og jöfnunina.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="cf1a8-110">Það gerir þér einnig kleift að tilgreina hvort gestir á vefnum geti hafnað skilaboðunum.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="cf1a8-111">Þegar móttökuskilaboðum er bætt við samnýtt fyrirsagnarbrot verða þau sýnd á hverri síðu sem notar sniðmátið þar sem það samnýtta fyrirsagnarbrot er notað.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="cf1a8-112">Fylgdu þessum skrefum til að bæta við móttökuskilaboðum á svæðið.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="cf1a8-113">Opnaðu síðuna þína á svæðissmið Commerce.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-113">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="cf1a8-114">Veldu **Brot**.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="cf1a8-115">Veldu fyrirsagnarbrot til að bæta skilaboðunum við.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="cf1a8-116">Stækkaðu í útlínutrénu **Villu-/upplýsingaskilaboð**.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="cf1a8-117">Veldu viðvörunareininguna og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-117">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="cf1a8-118">Ef viðvörunareining er ekki enn til, veldu fyrst hnappinn fyrir úrfellingarmerki (**...**) **Villu-/upplýsingaboð** og veldu síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-118">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="cf1a8-119">Í eiginleikaglugganum til hægri, á flipanum **Gögn** velurðu **Bæta við gagnagjafa** og velur síðan **Innihald**.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-119">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="cf1a8-120">Í reitinn **Inntakstexti** slærðu inn texta móttökuskilaboðanna.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-120">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="cf1a8-121">Smelltu á **Vista**, veldu **Ljúka við breytingar** til að athuga hausbrotið og smelltu síðan á **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-121">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="cf1a8-122">Móttökuskilaboðin birtast nú efst á hverri síðu svæðis sem notar valið fyrirsagnarbrot.</span><span class="sxs-lookup"><span data-stu-id="cf1a8-122">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf1a8-123">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="cf1a8-123">Additional resources</span></span>

[<span data-ttu-id="cf1a8-124">Bæta við lógói</span><span class="sxs-lookup"><span data-stu-id="cf1a8-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="cf1a8-125">Velja þema svæðis</span><span class="sxs-lookup"><span data-stu-id="cf1a8-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="cf1a8-126">Unnið með CSS hnekkiskrám</span><span class="sxs-lookup"><span data-stu-id="cf1a8-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="cf1a8-127">Bæta við táknmynd</span><span class="sxs-lookup"><span data-stu-id="cf1a8-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="cf1a8-128">Bæta við yfirlýsingu um höfundarrétt</span><span class="sxs-lookup"><span data-stu-id="cf1a8-128">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="cf1a8-129">Bæta tungumálum við síðuna</span><span class="sxs-lookup"><span data-stu-id="cf1a8-129">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="cf1a8-130">Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar</span><span class="sxs-lookup"><span data-stu-id="cf1a8-130">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

