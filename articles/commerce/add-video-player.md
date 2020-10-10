---
title: Myndspilaraeining
description: Þetta efni fjallar um myndspilaraeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3cf7ead9a5340d5db37a87bdf131ba87681d5a82
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817062"
---
# <a name="video-player-module"></a><span data-ttu-id="860ca-103">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="860ca-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="860ca-104">Þetta efni fjallar um myndspilaraeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="860ca-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="860ca-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="860ca-105">Overview</span></span>

<span data-ttu-id="860ca-106">Myndspilaraeiningin er notuð til að styðja myndspilun.</span><span class="sxs-lookup"><span data-stu-id="860ca-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="860ca-107">Hægt er að bæta henni við hvaða síðu sem er, að því tilskildu að myndbandsefni sé hlaðið upp á og tiltækt í efnisstjórnunarkerfinu (CMS).</span><span class="sxs-lookup"><span data-stu-id="860ca-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="860ca-108">Myndbandsspilarann styður .mp4 miðlunargerðina.</span><span class="sxs-lookup"><span data-stu-id="860ca-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="860ca-109">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="860ca-109">Video player module</span></span>

<span data-ttu-id="860ca-110">Hægt er að nota myndbandsspilarann til að sýna myndskeið á rafrænni verslunarsíðu.</span><span class="sxs-lookup"><span data-stu-id="860ca-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="860ca-111">Það styður alla spilunargetu, eins og spilun, hlé, stillingu í fullri stærð, hljóðlýsingum og lokuðum myndatexta.</span><span class="sxs-lookup"><span data-stu-id="860ca-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="860ca-112">Myndspilunareiningin styður einnig aðlögun á lokuðum myndatexta til að uppfylla aðgengisstaðla Microsoft.</span><span class="sxs-lookup"><span data-stu-id="860ca-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="860ca-113">Til dæmis er hægt að aðlaga leturstærð og bakgrunnslit.</span><span class="sxs-lookup"><span data-stu-id="860ca-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="860ca-114">Myndbandsspilaeiningin styður einnig aðrar hljóðrásir.</span><span class="sxs-lookup"><span data-stu-id="860ca-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="860ca-115">Þegar myndskeiði er hlaðið upp í CMS er einnig hægt að hlaða upp annari hljóðrás.</span><span class="sxs-lookup"><span data-stu-id="860ca-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="860ca-116">Síðan getur myndskeiðsspilarinn spilað seinni hljóðrásina ef notandi velur það.</span><span class="sxs-lookup"><span data-stu-id="860ca-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="860ca-117">Dæmi um myndspilareiningar í rafrænni verslun</span><span class="sxs-lookup"><span data-stu-id="860ca-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="860ca-118">Leiðbeinandi myndbönd á vöruupplýsingasíðum eða markaðssíðum</span><span class="sxs-lookup"><span data-stu-id="860ca-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="860ca-119">Kynningarmyndbönd eða myndbönd um stefnu á hvaða markaðssíðu sem er</span><span class="sxs-lookup"><span data-stu-id="860ca-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="860ca-120">Markaðssetningarmyndbönd sem varpa ljósi á vöruaðgerðir á upplýsingasíðum eða markaðssíðum</span><span class="sxs-lookup"><span data-stu-id="860ca-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

<span data-ttu-id="860ca-121">Eftirfarandi mynd sýnir dæmi um myndspilaraeiningu á heimasíðu.</span><span class="sxs-lookup"><span data-stu-id="860ca-121">The following image shows an example of a video player module on a home page.</span></span>

![Dæmi um myndspilaraeiningu](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a><span data-ttu-id="860ca-123">Eiginleikar myndspilaraeiningar</span><span class="sxs-lookup"><span data-stu-id="860ca-123">Video player module properties</span></span>

| <span data-ttu-id="860ca-124">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="860ca-124">Property name</span></span>         | <span data-ttu-id="860ca-125">Virði</span><span class="sxs-lookup"><span data-stu-id="860ca-125">Value</span></span>                               | <span data-ttu-id="860ca-126">lýsing</span><span class="sxs-lookup"><span data-stu-id="860ca-126">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="860ca-127">Sjálfvirk spilun</span><span class="sxs-lookup"><span data-stu-id="860ca-127">Auto play</span></span>             | <span data-ttu-id="860ca-128">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="860ca-128">**True** or **False**</span></span>               | <span data-ttu-id="860ca-129">Þegar gildi er stillt á **Satt** er myndskeiðið sjálfkrafa spilað.</span><span class="sxs-lookup"><span data-stu-id="860ca-129">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="860ca-130">Þagga</span><span class="sxs-lookup"><span data-stu-id="860ca-130">Mute</span></span>                  | <span data-ttu-id="860ca-131">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="860ca-131">**True** or **False**</span></span>               | <span data-ttu-id="860ca-132">Þegar gildi er stillt á **Satt** er skrúfað fyrir hljóðið.</span><span class="sxs-lookup"><span data-stu-id="860ca-132">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="860ca-133">Fyrir þennan spilara er sjálfgildið **Ósatt**.</span><span class="sxs-lookup"><span data-stu-id="860ca-133">For this player, the default value is **False**.</span></span> <span data-ttu-id="860ca-134">Í Chrome-vafranum er sjálfvirk spilun myndskeiða sjálfgefið þögguð og hljóðið er aðeins spilað ef notandinn spilar myndbandið handvirkt.</span><span class="sxs-lookup"><span data-stu-id="860ca-134">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="860ca-135">Lykkja</span><span class="sxs-lookup"><span data-stu-id="860ca-135">Loop</span></span>                  | <span data-ttu-id="860ca-136">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="860ca-136">**True** or **False**</span></span>               | <span data-ttu-id="860ca-137">Þegar gildi er stillt á **Satt** er myndskeiðið endurtekið í lúppu.</span><span class="sxs-lookup"><span data-stu-id="860ca-137">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="860ca-138">Miðlar</span><span class="sxs-lookup"><span data-stu-id="860ca-138">Media</span></span>                 | <span data-ttu-id="860ca-139">Skráarslóð og -heiti myndskeiðs</span><span class="sxs-lookup"><span data-stu-id="860ca-139">Video file path and name</span></span> | <span data-ttu-id="860ca-140">Myndskeiðið sem er spilað í myndspilaranum.</span><span class="sxs-lookup"><span data-stu-id="860ca-140">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="860ca-141">Spila á öllum skjánum</span><span class="sxs-lookup"><span data-stu-id="860ca-141">Play fullscreen</span></span>       | <span data-ttu-id="860ca-142">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="860ca-142">**True** or **False**</span></span>               | <span data-ttu-id="860ca-143">Þegar gildi er stillt á **Satt** er myndskeiðið spilað á öllum skjánum.</span><span class="sxs-lookup"><span data-stu-id="860ca-143">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="860ca-144">Spila/hlé</span><span class="sxs-lookup"><span data-stu-id="860ca-144">Play pause trigger</span></span>    | <span data-ttu-id="860ca-145">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="860ca-145">**True** or **False**</span></span>               | <span data-ttu-id="860ca-146">Þegar gildið er stillt á **Satt** sést spilunar-/hléhnappur í myndskeiðinu.</span><span class="sxs-lookup"><span data-stu-id="860ca-146">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="860ca-147">Stýringar myndspilara</span><span class="sxs-lookup"><span data-stu-id="860ca-147">Video player controls</span></span> | <span data-ttu-id="860ca-148">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="860ca-148">**True** or **False**</span></span>               | <span data-ttu-id="860ca-149">Þegar gildið er stillt á **Satt** eru öll stjórntæki myndbandsspilarans sýnd.</span><span class="sxs-lookup"><span data-stu-id="860ca-149">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="860ca-150">Þessar stjórntæki fela í sér spilunar- og hléhnappa, framvinduvísir og valkosti fyir lokaða myndatexta.</span><span class="sxs-lookup"><span data-stu-id="860ca-150">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="860ca-151">Fela forsíðumynd</span><span class="sxs-lookup"><span data-stu-id="860ca-151">Hide poster image</span></span>     | <span data-ttu-id="860ca-152">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="860ca-152">**True** or **False**</span></span>               | <span data-ttu-id="860ca-153">Myndskeið getur verið með plakatramma.</span><span class="sxs-lookup"><span data-stu-id="860ca-153">A video can have a poster frame.</span></span> <span data-ttu-id="860ca-154">Þegar gildið þessa eiginleika er stillt á **Satt** er plakatramminn falinn.</span><span class="sxs-lookup"><span data-stu-id="860ca-154">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="860ca-155">Sniðmátsstig</span><span class="sxs-lookup"><span data-stu-id="860ca-155">Mask level</span></span>            | <span data-ttu-id="860ca-156">Tölugildi frá **0** til og með **100**</span><span class="sxs-lookup"><span data-stu-id="860ca-156">A number from **0** through **100**</span></span> | <span data-ttu-id="860ca-157">Sniðmátið sem er beitt á myndskeiðið til útlitshönnun.</span><span class="sxs-lookup"><span data-stu-id="860ca-157">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="860ca-158">Bæta við myndspilaraeiningu á síðu</span><span class="sxs-lookup"><span data-stu-id="860ca-158">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="860ca-159">Áður en þú býrð til myndspilaraeiningu verðurðu fyrst að hlaða upp myndskeiði á fjölmiðlasafnið.</span><span class="sxs-lookup"><span data-stu-id="860ca-159">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="860ca-160">Fylgdu þessum skrefum til að bæta myndspilaraeiningu við nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="860ca-160">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="860ca-161">Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="860ca-161">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="860ca-162">Í svarglugganum **Nýtt sniðmát**, undir **Heiti sniðmáts**, skal slá inn **Sniðmát myndspilara** og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="860ca-162">In the **New Template** dialog box, under **Template name**, enter **Video player template**, and then select **OK**.</span></span>
1. <span data-ttu-id="860ca-163">Í hólfinu **Meginmál**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="860ca-163">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="860ca-164">Í glugganum **Bæta við einingu** skal velja eininguna **Sjálfgefin síða** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="860ca-164">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="860ca-165">Í hólfinu **Aðalsvæði** í einingunni **Sjálfgefin síða** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="860ca-165">In the **Main** slot of the **Default Page** module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="860ca-166">Í glugganum **Bæta við einingu** skal velja eininguna **Hólf** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="860ca-166">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="860ca-167">Í hólfinu **Hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="860ca-167">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="860ca-168">Í glugganum **Bæta við einingu** skal velja eininguna **Myndspilari** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="860ca-168">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="860ca-169">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="860ca-169">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="860ca-170">Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.</span><span class="sxs-lookup"><span data-stu-id="860ca-170">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="860ca-171">Í svarglugganum **Velja sniðmát** skal velja það sniðmát myndspilara sem var búið til.</span><span class="sxs-lookup"><span data-stu-id="860ca-171">In the **Choose a template** dialog box, select the video player template that you created.</span></span> <span data-ttu-id="860ca-172">Undir **Síðuheiti** skal færa inn **Myndspilarasíða** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="860ca-172">Under **Page name**, enter **Video player page**, and then select **OK**.</span></span>
1. <span data-ttu-id="860ca-173">Í hólfinu **Aðalsvæði** á nýju síðunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="860ca-173">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="860ca-174">Í glugganum **Bæta við einingu** skal velja eininguna **Hólf** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="860ca-174">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="860ca-175">Í hólfinu **Hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="860ca-175">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="860ca-176">Í glugganum **Bæta við einingu** skal velja eininguna **Myndspilari** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="860ca-176">In the **Add Module** dialog box, select the **Video player** module, and then select **OK**.</span></span>
1. <span data-ttu-id="860ca-177">Á eiginleikasvæði myndspilaraeiningar skal velja **Bæta við myndbandi**.</span><span class="sxs-lookup"><span data-stu-id="860ca-177">In the property pane of the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="860ca-178">Í valmyndinni **Miðlaval** velurðu myndskeið og velur síðan **Hlaða upp nýjum miðli**.</span><span class="sxs-lookup"><span data-stu-id="860ca-178">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="860ca-179">Í File Explorer skal velja myndbandsskrá og velja síðan **Opna**.</span><span class="sxs-lookup"><span data-stu-id="860ca-179">In File Explorer, select a video file, and then select **Open**.</span></span>
1. <span data-ttu-id="860ca-180">Í glugganum **Hlaða upp margmiðlunarefni** skal slá inn titil og aðrar upplýsingar eftir þörfum og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="860ca-180">In the **Upload Media Item** dialog box, enter a title and other information as needed, and then select **OK**.</span></span>
1. <span data-ttu-id="860ca-181">Í glugganum **Val á miðli** skal velja **Loka**.</span><span class="sxs-lookup"><span data-stu-id="860ca-181">In the **Media Picker** dialog box, select **Close**.</span></span>
1. <span data-ttu-id="860ca-182">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="860ca-182">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="860ca-183">Þú ættir að sjá myndskeiðseininguna á síðunni.</span><span class="sxs-lookup"><span data-stu-id="860ca-183">You should see the video module on the page.</span></span> <span data-ttu-id="860ca-184">Þú getur breytt viðbótarstillingum til að sérsníða hegðun einingarinnar.</span><span class="sxs-lookup"><span data-stu-id="860ca-184">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="860ca-185">Veldu**Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="860ca-185">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="860ca-186">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="860ca-186">Additional resources</span></span>

[<span data-ttu-id="860ca-187">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="860ca-187">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="860ca-188">Tilboðsborðaeining</span><span class="sxs-lookup"><span data-stu-id="860ca-188">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="860ca-189">Myndaræmueining</span><span class="sxs-lookup"><span data-stu-id="860ca-189">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="860ca-190">Textabálkseining</span><span class="sxs-lookup"><span data-stu-id="860ca-190">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="860ca-191">Innihaldsbálkseining</span><span class="sxs-lookup"><span data-stu-id="860ca-191">Content block module</span></span>](add-hero-module.md)
