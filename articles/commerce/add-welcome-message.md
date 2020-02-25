---
title: Bæta við opnunarkveðju
description: Þetta efnisatriði lýsir því hvernig á að bæta móttökuskilaboðum við Microsoft Dynamics 365 Commerce vefsvæði.
author: psimolin
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: ca10b01268b5dcd4c6fe448d90cd0ebd65a2673b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001255"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="b9e03-103">Bæta við opnunarkveðju</span><span class="sxs-lookup"><span data-stu-id="b9e03-103">Add a welcome message</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b9e03-104">Þetta efnisatriði lýsir því hvernig á að bæta móttökuskilaboðum við Microsoft Dynamics 365 Commerce vefsvæði.</span><span class="sxs-lookup"><span data-stu-id="b9e03-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="b9e03-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="b9e03-105">Overview</span></span>

<span data-ttu-id="b9e03-106">Móttökuskilaboð á vefsíðu rafrænna viðskipta geta tilkynnt gestum um áframhaldandi útsölu, uppfærslur á vefnum eða framboð á árstíðabundnum línum.</span><span class="sxs-lookup"><span data-stu-id="b9e03-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="b9e03-107">Móttökuskilaboðin eru stillt með því að nota viðvörunareininguna.</span><span class="sxs-lookup"><span data-stu-id="b9e03-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="b9e03-108">Viðvörunareiningunni ætti að bæta við hólfið **Villu-/upplýsingaskilaboð** í fyrirsagnarbrotinu.</span><span class="sxs-lookup"><span data-stu-id="b9e03-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="b9e03-109">Viðvörunareiningin gerir þér kleift að tilgreina textann sem er sýndur, textalitinn og jöfnunina.</span><span class="sxs-lookup"><span data-stu-id="b9e03-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="b9e03-110">Það gerir þér einnig kleift að tilgreina hvort gestir á vefnum geti hafnað skilaboðunum.</span><span class="sxs-lookup"><span data-stu-id="b9e03-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="b9e03-111">Þegar móttökuskilaboðum er bætt við samnýtt fyrirsagnarbrot verða þau sýnd á hverri síðu sem notar sniðmátið þar sem það samnýtta fyrirsagnarbrot er notað.</span><span class="sxs-lookup"><span data-stu-id="b9e03-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="b9e03-112">Fylgdu þessum skrefum til að bæta við móttökuskilaboðum á svæðið.</span><span class="sxs-lookup"><span data-stu-id="b9e03-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="b9e03-113">Í Dynamics 365 Commerce, farðu á vefsíðuna.</span><span class="sxs-lookup"><span data-stu-id="b9e03-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="b9e03-114">Veldu **Brot**.</span><span class="sxs-lookup"><span data-stu-id="b9e03-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="b9e03-115">Veldu fyrirsagnarbrot til að bæta skilaboðunum við.</span><span class="sxs-lookup"><span data-stu-id="b9e03-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="b9e03-116">Stækkaðu í útlínutrénu **Villu-/upplýsingaskilaboð**.</span><span class="sxs-lookup"><span data-stu-id="b9e03-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="b9e03-117">Veldu viðvörunareininguna.</span><span class="sxs-lookup"><span data-stu-id="b9e03-117">Select the alert module.</span></span>

    <span data-ttu-id="b9e03-118">Ef viðvörunareining er ekki ennþá til skaltu velja úrfellingarhnappinn (**...**) við hliðina á **Villu-/upplýsingaskilaboð** og velja síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="b9e03-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="b9e03-119">Veldu viðvörunareininguna og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b9e03-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="b9e03-120">Í eiginleikaglugganum til hægri, á flipanum **Gögn** velurðu **Bæta við gagnagjafa** og velur síðan **Innihald**.</span><span class="sxs-lookup"><span data-stu-id="b9e03-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="b9e03-121">Í reitinn **Inntakstexti** slærðu inn texta móttökuskilaboðanna.</span><span class="sxs-lookup"><span data-stu-id="b9e03-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="b9e03-122">Vistaðu fyrirsagnarbrotið, skráðu það inn og gefðu það út.</span><span class="sxs-lookup"><span data-stu-id="b9e03-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="b9e03-123">Móttökuskilaboðin birtast nú efst á hverri síðu svæðis sem notar valið fyrirsagnarbrot.</span><span class="sxs-lookup"><span data-stu-id="b9e03-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9e03-124">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b9e03-124">Additional resources</span></span>

[<span data-ttu-id="b9e03-125">Bæta við lógói</span><span class="sxs-lookup"><span data-stu-id="b9e03-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="b9e03-126">Velja þema svæðis</span><span class="sxs-lookup"><span data-stu-id="b9e03-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="b9e03-127">Unnið með CSS hnekkiskrám</span><span class="sxs-lookup"><span data-stu-id="b9e03-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="b9e03-128">Bæta við táknmynd</span><span class="sxs-lookup"><span data-stu-id="b9e03-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="b9e03-129">Bæta við yfirlýsingu um höfundarrétt</span><span class="sxs-lookup"><span data-stu-id="b9e03-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="b9e03-130">Bæta tungumálum við síðuna</span><span class="sxs-lookup"><span data-stu-id="b9e03-130">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="b9e03-131">Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar</span><span class="sxs-lookup"><span data-stu-id="b9e03-131">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

