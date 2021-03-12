---
title: Iframe-eining
description: Þetta efnisatriði fjallar um iframe-eininguna og útskýrir hvernig á að bæta henni við síður á vefsvæði Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b7b5935a81377e0cb6acfc497eece6148bf1eeee
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993370"
---
# <a name="iframe-module"></a><span data-ttu-id="f1428-103">Iframe-eining</span><span class="sxs-lookup"><span data-stu-id="f1428-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f1428-104">Þetta efnisatriði fjallar um iframe-eininguna og útskýrir hvernig á að bæta henni við síður á vefsvæði Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f1428-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f1428-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="f1428-105">Overview</span></span>

<span data-ttu-id="f1428-106">Iframe-eining býður upp á iframe (ramma innan línu) sem hýsir ytra efni á vefsvæði.</span><span class="sxs-lookup"><span data-stu-id="f1428-106">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="f1428-107">Til dæmis er hægt að nota hana til að hýsa YouTube-myndband eða PDF-skráaskoðun á hvaða síðu sem er.</span><span class="sxs-lookup"><span data-stu-id="f1428-107">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="f1428-108">Iframe-eining krefst markvefsslóðar.</span><span class="sxs-lookup"><span data-stu-id="f1428-108">An iframe module requires a target URL.</span></span> <span data-ttu-id="f1428-109">Hún hýsir svo efni marksíðunnar innan HTML einingar **iframe**.</span><span class="sxs-lookup"><span data-stu-id="f1428-109">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="f1428-110">Ytri vefslóðir verða að vera á heimildarlistanum samkvæmt leiðbeiningum fyrir öryggisreglu um efni vefsvæðis.</span><span class="sxs-lookup"><span data-stu-id="f1428-110">External URLs must be on the allow list per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="f1428-111">Fyrir iframe-efni ættu vefslóðir að vera leyfðar með því að nota leiðbeininguna **frame-ancestor**.</span><span class="sxs-lookup"><span data-stu-id="f1428-111">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="f1428-112">Frekari upplýsingar er að finna í [Stjórna öryggisreglu fyrir efni (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="f1428-112">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

> [!NOTE]
> <span data-ttu-id="f1428-113">iframe-einingin er tiltæk í Dynamics 365 Commerce útgáfu 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="f1428-113">The iframe module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="f1428-114">Eftirfarandi mynd sýnir dæmi um iframe-einingar sem sýna ytri myndbönd á síðum vefsvæðis.</span><span class="sxs-lookup"><span data-stu-id="f1428-114">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![Dæmi um iframe-einingar sem sýna ytri myndbönd](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="f1428-116">Eiginleikar Iframe-einingar</span><span class="sxs-lookup"><span data-stu-id="f1428-116">Iframe module properties</span></span>

| <span data-ttu-id="f1428-117">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="f1428-117">Property name</span></span>             | <span data-ttu-id="f1428-118">Virði</span><span class="sxs-lookup"><span data-stu-id="f1428-118">Value</span></span>                 | <span data-ttu-id="f1428-119">lýsing</span><span class="sxs-lookup"><span data-stu-id="f1428-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="f1428-120">Yfirskrift</span><span class="sxs-lookup"><span data-stu-id="f1428-120">Heading</span></span> | <span data-ttu-id="f1428-121">Texti</span><span class="sxs-lookup"><span data-stu-id="f1428-121">Text</span></span> | <span data-ttu-id="f1428-122">Fyrirsögn einingarinnar.</span><span class="sxs-lookup"><span data-stu-id="f1428-122">The heading for the module.</span></span> |
| <span data-ttu-id="f1428-123">Viðtökuslóð</span><span class="sxs-lookup"><span data-stu-id="f1428-123">Target URL</span></span> | <span data-ttu-id="f1428-124">URL</span><span class="sxs-lookup"><span data-stu-id="f1428-124">URL</span></span> | <span data-ttu-id="f1428-125">Vefslóðin sem er hýst í einingunni.</span><span class="sxs-lookup"><span data-stu-id="f1428-125">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="f1428-126">Hæð</span><span class="sxs-lookup"><span data-stu-id="f1428-126">Height</span></span> | <span data-ttu-id="f1428-127">Númer eða prósentuhlutfall</span><span class="sxs-lookup"><span data-stu-id="f1428-127">Number or percentage</span></span> | <span data-ttu-id="f1428-128">Hæð einingarinnar, í pixlum eða sem prósenta.</span><span class="sxs-lookup"><span data-stu-id="f1428-128">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="f1428-129">Til dæmis verður gildið **100** meðhöndlað sem fjöldi pixla og gildið **100%** verður meðhöndlað sem prósenta.</span><span class="sxs-lookup"><span data-stu-id="f1428-129">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="f1428-130">Aria merki</span><span class="sxs-lookup"><span data-stu-id="f1428-130">Aria label</span></span> | <span data-ttu-id="f1428-131">Texti</span><span class="sxs-lookup"><span data-stu-id="f1428-131">Text</span></span> | <span data-ttu-id="f1428-132">Hægt er að skilgreina ARIA-merki (Accessible Rich Internet Applications) fyrir aðgengi.</span><span class="sxs-lookup"><span data-stu-id="f1428-132">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="f1428-133">Bæta iframe-einingu við síðu</span><span class="sxs-lookup"><span data-stu-id="f1428-133">Add an iframe module to a page</span></span>

<span data-ttu-id="f1428-134">Til að bæta iframe-einingu við síðu til að sýna ytra myndband skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="f1428-134">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="f1428-135">Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="f1428-135">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="f1428-136">Í svarglugganum **Nýtt sniðmát**, undir **Heiti sniðmáts**, skal slá inn **Markaðssniðmát** og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f1428-136">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="f1428-137">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="f1428-137">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="f1428-138">Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.</span><span class="sxs-lookup"><span data-stu-id="f1428-138">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="f1428-139">Í svarglugganum **Velja sniðmát** skal velja sniðmátið **Markaðssniðmát**.</span><span class="sxs-lookup"><span data-stu-id="f1428-139">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="f1428-140">Undir **Síðuheiti** skal færa inn **Síða markaðssetningar** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f1428-140">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="f1428-141">Í hólfinu **Aðalsvæði** á nýju síðunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="f1428-141">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f1428-142">Í glugganum **Bæta við einingu** skal velja eininguna **Hólf** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f1428-142">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f1428-143">Á eiginleikasvæði einingarinnar skal stilla gildið **Breidd** á **Fylla hólf**.</span><span class="sxs-lookup"><span data-stu-id="f1428-143">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="f1428-144">Í hólfinu **Hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="f1428-144">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="f1428-145">Í glugganum **Bæta við einingu** skal velja eininguna **iframe** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f1428-145">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="f1428-146">Á eiginleikasvæði einingarinnar skal stilla gildið **Markvefslóð** á ytri vefslóð fyrir myndband.</span><span class="sxs-lookup"><span data-stu-id="f1428-146">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="f1428-147">Stillið aðra eiginleika, t.d. **Fyrirsögn** og **Hæð**, eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="f1428-147">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="f1428-148">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="f1428-148">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="f1428-149">Opnaðu markaðssíðuna á vefsvæðinu þinni.</span><span class="sxs-lookup"><span data-stu-id="f1428-149">Go to the marketing page on your site.</span></span> <span data-ttu-id="f1428-150">Þú ættir að sjá að myndbandið er sýnt í iframe-einingunni.</span><span class="sxs-lookup"><span data-stu-id="f1428-150">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="f1428-151">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f1428-151">Additional resources</span></span>

[<span data-ttu-id="f1428-152">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="f1428-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f1428-153">Stjórna öryggisreglu fyrir efni (CSP)</span><span class="sxs-lookup"><span data-stu-id="f1428-153">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
