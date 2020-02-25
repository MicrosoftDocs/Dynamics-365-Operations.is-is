---
title: Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar
description: Þetta efnisatriði lýsir því hvernig hægt er að bæta skriftarkóða biðlara við síður svæðisins til að styðja söfnun fjarmælinga biðlara.
author: bicyclingfool
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 674d00faf1b30f87a0b0062129e1b9fbff955dd4
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001278"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="66037-103">Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar</span><span class="sxs-lookup"><span data-stu-id="66037-103">Add script code to site pages to support telemetry</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="66037-104">Þetta efnisatriði lýsir því hvernig hægt er að bæta skriftarkóða biðlara við síður svæðisins til að styðja söfnun fjarmælinga biðlara.</span><span class="sxs-lookup"><span data-stu-id="66037-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="66037-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="66037-105">Overview</span></span>

<span data-ttu-id="66037-106">Vefgreining er ómissandi tæki þegar þú vilt skilja hvernig viðskiptavinir þínir hafa samskipti við vefsíðuna og taka ákvarðanir sem munu hjálpa til við að hámarka upplifunina fyrir hámarks umreikning.</span><span class="sxs-lookup"><span data-stu-id="66037-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="66037-107">Margir vefgreiningarpakkar eru í boði til að hjálpa þér að ná þessum markmiðum, eins og Google Analytics, Clicky, Moz Analytics og KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="66037-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="66037-108">Flestir vefgreiningarpakkar krefjast þess að þú bætir við skriftarkóða biðlarans í **\<höfuð\>**-þáttinn í HTML fyrir allar síður á vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="66037-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="66037-109">Leiðbeiningarnar í þessu efni eiga einnig við um aðra sérsniðna virkni biðlara sem Microsoft Dynamics 365 Commerce býður ekki staðbundið.</span><span class="sxs-lookup"><span data-stu-id="66037-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="66037-110">Stofnaðu endurnýtanlegt brot fyrir skriftarkóðann</span><span class="sxs-lookup"><span data-stu-id="66037-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="66037-111">Eftir að þú hefur stofnað brot fyrir skriftarkóðann er hægt að nota það á allar síður á vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="66037-111">After you create a fragment for your script code, it can be reused across all pages on your site.</span></span>

1. <span data-ttu-id="66037-112">Farðu í **Brot \> Ný síðubrot**.</span><span class="sxs-lookup"><span data-stu-id="66037-112">Go to **Fragments \> New page fragment**.</span></span>
2. <span data-ttu-id="66037-113">Veldu **Ytri forskrift**, sláðu inn heiti fyrir brotið og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="66037-113">Select **External Script**, enter a name for the fragment, and then select **OK**.</span></span>
3. <span data-ttu-id="66037-114">Í brotastigveldinu velurðu undireininguna **innsetning forskriftar** brotsins sem þú varst að búa til.</span><span class="sxs-lookup"><span data-stu-id="66037-114">In the fragment hierarchy, select the **script injector** module child of the fragment that you just created.</span></span>
4. <span data-ttu-id="66037-115">Í eiginleikaglugganum til hægri bætirðu við forskrift biðlara og stillir aðra stillingarvalkosti eins og þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="66037-115">In the property pane on the right, add your client-side script, and set other configuration options as you require.</span></span>

## <a name="add-the-fragment-to-templates"></a><span data-ttu-id="66037-116">Bættu brotunum við sniðmát</span><span class="sxs-lookup"><span data-stu-id="66037-116">Add the fragment to templates</span></span>

1. <span data-ttu-id="66037-117">Farðu í **Sniðmát** og opnaðu sniðmátið fyrir síðurnar sem þú vilt bæta forskriftakóðanum við.</span><span class="sxs-lookup"><span data-stu-id="66037-117">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
2. <span data-ttu-id="66037-118">Stækkaðu sniðmát stigveldisins í vinstri glugganum til að sýna hólfið **HTML-höfuð**.</span><span class="sxs-lookup"><span data-stu-id="66037-118">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
3. <span data-ttu-id="66037-119">Veldu úrfellingarhnappinn (**...**) fyrir hólfið **HTML-haus** og veldu síðan **Bæta við broti**.</span><span class="sxs-lookup"><span data-stu-id="66037-119">Select the ellipsis button (**...**) for the **HTML Head** slot, and then select **Add fragment**.</span></span>
4. <span data-ttu-id="66037-120">Veldu brotið sem þú bjóst til fyrir forskriftakóðann.</span><span class="sxs-lookup"><span data-stu-id="66037-120">Select the fragment that you created for your script code.</span></span>
5. <span data-ttu-id="66037-121">Vista sniðmáti og skráðu það inn.</span><span class="sxs-lookup"><span data-stu-id="66037-121">Save the template, and check it in.</span></span>

> [!NOTE]
> <span data-ttu-id="66037-122">Eftir að því er lokið verður að birta brotið og sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="66037-122">After you've finished, you must publish the fragment and the master template.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="66037-123">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="66037-123">Additional resources</span></span>

[<span data-ttu-id="66037-124">Bæta við lógói</span><span class="sxs-lookup"><span data-stu-id="66037-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="66037-125">Velja þema svæðis</span><span class="sxs-lookup"><span data-stu-id="66037-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="66037-126">Unnið með CSS hnekkiskrám</span><span class="sxs-lookup"><span data-stu-id="66037-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="66037-127">Bæta við táknmynd</span><span class="sxs-lookup"><span data-stu-id="66037-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="66037-128">Bæta við opnunarkveðju</span><span class="sxs-lookup"><span data-stu-id="66037-128">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="66037-129">Bæta við yfirlýsingu um höfundarrétt</span><span class="sxs-lookup"><span data-stu-id="66037-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="66037-130">Bæta tungumálum við síðuna</span><span class="sxs-lookup"><span data-stu-id="66037-130">Add languages to your site</span></span>](add-languages-to-site.md)

