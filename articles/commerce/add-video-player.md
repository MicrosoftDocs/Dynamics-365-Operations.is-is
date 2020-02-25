---
title: Myndspilaraeining
description: Þetta efni fjallar um myndspilaraeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: e94658eed12b12d6666e63d2c06b86646c81a120
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025650"
---
# <a name="video-player-module"></a><span data-ttu-id="32aff-103">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="32aff-103">Video player module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="32aff-104">Þetta efni fjallar um myndspilaraeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="32aff-104">This topic covers video player modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="32aff-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="32aff-105">Overview</span></span>

<span data-ttu-id="32aff-106">Myndspilaraeiningin er notuð til að styðja myndspilun.</span><span class="sxs-lookup"><span data-stu-id="32aff-106">The video player module is used to support video playback.</span></span> <span data-ttu-id="32aff-107">Hægt er að bæta henni við hvaða síðu sem er, að því tilskildu að myndbandsefni sé hlaðið upp á og tiltækt í efnisstjórnunarkerfinu (CMS).</span><span class="sxs-lookup"><span data-stu-id="32aff-107">It can be added to any page, provided that video content is uploaded to and available in the content management system (CMS).</span></span> <span data-ttu-id="32aff-108">Myndbandsspilarann styður .mp4 miðlunargerðina.</span><span class="sxs-lookup"><span data-stu-id="32aff-108">The video player module supports the .mp4 media type.</span></span>

## <a name="video-player-module"></a><span data-ttu-id="32aff-109">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="32aff-109">Video player module</span></span>

<span data-ttu-id="32aff-110">Hægt er að nota myndbandsspilarann til að sýna myndskeið á rafrænni verslunarsíðu.</span><span class="sxs-lookup"><span data-stu-id="32aff-110">The video player module can be used to showcase videos on an e-Commerce site.</span></span> <span data-ttu-id="32aff-111">Það styður alla spilunargetu, eins og spilun, hlé, stillingu í fullri stærð, hljóðlýsingum og lokuðum myndatexta.</span><span class="sxs-lookup"><span data-stu-id="32aff-111">It supports all playback capabilities, such as play, pause, full-size mode, audio descriptions, and closed captions.</span></span> <span data-ttu-id="32aff-112">Myndspilunareiningin styður einnig aðlögun á lokuðum myndatexta til að uppfylla aðgengisstaðla Microsoft.</span><span class="sxs-lookup"><span data-stu-id="32aff-112">The video player module also supports customization of closed captions to meet Microsoft accessibility standards.</span></span> <span data-ttu-id="32aff-113">Til dæmis er hægt að aðlaga leturstærð og bakgrunnslit.</span><span class="sxs-lookup"><span data-stu-id="32aff-113">For example, you can customize the font size and background color.</span></span>

<span data-ttu-id="32aff-114">Myndbandsspilaeiningin styður einnig aðrar hljóðrásir.</span><span class="sxs-lookup"><span data-stu-id="32aff-114">The video player module also supports secondary audio tracks.</span></span> <span data-ttu-id="32aff-115">Þegar myndskeiði er hlaðið upp í CMS er einnig hægt að hlaða upp annari hljóðrás.</span><span class="sxs-lookup"><span data-stu-id="32aff-115">When a video is uploaded to the CMS, a secondary audio track can also be uploaded.</span></span> <span data-ttu-id="32aff-116">Síðan getur myndskeiðsspilarinn spilað seinni hljóðrásina ef notandi velur það.</span><span class="sxs-lookup"><span data-stu-id="32aff-116">The video player module can then play the secondary audio track if a user selects it.</span></span>

### <a name="examples-of-video-player-modules-in-e-commerce"></a><span data-ttu-id="32aff-117">Dæmi um myndspilareiningar í rafrænni verslun</span><span class="sxs-lookup"><span data-stu-id="32aff-117">Examples of video player modules in e-Commerce</span></span>

- <span data-ttu-id="32aff-118">Leiðbeinandi myndbönd á vöruupplýsingasíðum eða markaðssíðum</span><span class="sxs-lookup"><span data-stu-id="32aff-118">Instructional videos on product details pages or marketing pages</span></span>
- <span data-ttu-id="32aff-119">Kynningarmyndbönd eða myndbönd um stefnu á hvaða markaðssíðu sem er</span><span class="sxs-lookup"><span data-stu-id="32aff-119">Promotional videos or videos about policies on any marketing page</span></span>
- <span data-ttu-id="32aff-120">Markaðssetningarmyndbönd sem varpa ljósi á vöruaðgerðir á upplýsingasíðum eða markaðssíðum</span><span class="sxs-lookup"><span data-stu-id="32aff-120">Marketing videos that highlight product features on product details pages or marketing pages</span></span>

### <a name="video-player-module-properties"></a><span data-ttu-id="32aff-121">Eiginleikar myndspilaraeiningar</span><span class="sxs-lookup"><span data-stu-id="32aff-121">Video player module properties</span></span>

| <span data-ttu-id="32aff-122">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="32aff-122">Property name</span></span>         | <span data-ttu-id="32aff-123">Virði</span><span class="sxs-lookup"><span data-stu-id="32aff-123">Value</span></span>                               | <span data-ttu-id="32aff-124">Lýsing</span><span class="sxs-lookup"><span data-stu-id="32aff-124">Description</span></span> |
|-----------------------|-------------------------------------|-------------|
| <span data-ttu-id="32aff-125">Sjálfvirk spilun</span><span class="sxs-lookup"><span data-stu-id="32aff-125">Auto play</span></span>             | <span data-ttu-id="32aff-126">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="32aff-126">**True** or **False**</span></span>               | <span data-ttu-id="32aff-127">Þegar gildi er stillt á **Satt** er myndskeiðið sjálfkrafa spilað.</span><span class="sxs-lookup"><span data-stu-id="32aff-127">When the value is set to **True**, the video is automatically played.</span></span> |
| <span data-ttu-id="32aff-128">Þagga</span><span class="sxs-lookup"><span data-stu-id="32aff-128">Mute</span></span>                  | <span data-ttu-id="32aff-129">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="32aff-129">**True** or **False**</span></span>               | <span data-ttu-id="32aff-130">Þegar gildi er stillt á **Satt** er skrúfað fyrir hljóðið.</span><span class="sxs-lookup"><span data-stu-id="32aff-130">When the value is set to **True**, the audio is muted.</span></span> <span data-ttu-id="32aff-131">Fyrir þennan spilara er sjálfgildið **Ósatt**.</span><span class="sxs-lookup"><span data-stu-id="32aff-131">For this player, the default value is **False**.</span></span> <span data-ttu-id="32aff-132">Í Chrome-vafranum er sjálfvirk spilun myndskeiða sjálfgefið þögguð og hljóðið er aðeins spilað ef notandinn spilar myndbandið handvirkt.</span><span class="sxs-lookup"><span data-stu-id="32aff-132">In the Chrome browser, autoplay videos are muted by default, and the audio is played only if the user manually plays the video.</span></span> |
| <span data-ttu-id="32aff-133">Lykkja</span><span class="sxs-lookup"><span data-stu-id="32aff-133">Loop</span></span>                  | <span data-ttu-id="32aff-134">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="32aff-134">**True** or **False**</span></span>               | <span data-ttu-id="32aff-135">Þegar gildi er stillt á **Satt** er myndskeiðið endurtekið í lúppu.</span><span class="sxs-lookup"><span data-stu-id="32aff-135">When the value is set to **True**, the video is repeated in a loop.</span></span> |
| <span data-ttu-id="32aff-136">Miðlar</span><span class="sxs-lookup"><span data-stu-id="32aff-136">Media</span></span>                 | <span data-ttu-id="32aff-137">Skráarslóð og -heiti myndskeiðs</span><span class="sxs-lookup"><span data-stu-id="32aff-137">Video file path and name</span></span> | <span data-ttu-id="32aff-138">Myndskeiðið sem er spilað í myndspilaranum.</span><span class="sxs-lookup"><span data-stu-id="32aff-138">The video file that is played in the video player.</span></span> |
| <span data-ttu-id="32aff-139">Spila á öllum skjánum</span><span class="sxs-lookup"><span data-stu-id="32aff-139">Play fullscreen</span></span>       | <span data-ttu-id="32aff-140">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="32aff-140">**True** or **False**</span></span>               | <span data-ttu-id="32aff-141">Þegar gildi er stillt á **Satt** er myndskeiðið spilað á öllum skjánum.</span><span class="sxs-lookup"><span data-stu-id="32aff-141">When the value is set to **True**, the video is played in full-screen mode.</span></span> |
| <span data-ttu-id="32aff-142">Spila/hlé</span><span class="sxs-lookup"><span data-stu-id="32aff-142">Play pause trigger</span></span>    | <span data-ttu-id="32aff-143">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="32aff-143">**True** or **False**</span></span>               | <span data-ttu-id="32aff-144">Þegar gildið er stillt á **Satt** sést spilunar-/hléhnappur í myndskeiðinu.</span><span class="sxs-lookup"><span data-stu-id="32aff-144">When the value is set to **True**, a play/pause button is shown on the video.</span></span> |
| <span data-ttu-id="32aff-145">Stýringar myndspilara</span><span class="sxs-lookup"><span data-stu-id="32aff-145">Video player controls</span></span> | <span data-ttu-id="32aff-146">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="32aff-146">**True** or **False**</span></span>               | <span data-ttu-id="32aff-147">Þegar gildið er stillt á **Satt** eru öll stjórntæki myndbandsspilarans sýnd.</span><span class="sxs-lookup"><span data-stu-id="32aff-147">When the value is set to **True**, all video player controls are shown.</span></span> <span data-ttu-id="32aff-148">Þessar stjórntæki fela í sér spilunar- og hléhnappa, framvinduvísir og valkosti fyir lokaða myndatexta.</span><span class="sxs-lookup"><span data-stu-id="32aff-148">These controls include play and pause buttons, a progress indicator, and closed caption options.</span></span> |
| <span data-ttu-id="32aff-149">Fela forsíðumynd</span><span class="sxs-lookup"><span data-stu-id="32aff-149">Hide poster image</span></span>     | <span data-ttu-id="32aff-150">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="32aff-150">**True** or **False**</span></span>               | <span data-ttu-id="32aff-151">Myndskeið getur verið með plakatramma.</span><span class="sxs-lookup"><span data-stu-id="32aff-151">A video can have a poster frame.</span></span> <span data-ttu-id="32aff-152">Þegar gildið þessa eiginleika er stillt á **Satt** er plakatramminn falinn.</span><span class="sxs-lookup"><span data-stu-id="32aff-152">When the value of this property is set to **True**, the poster frame is hidden.</span></span> |
| <span data-ttu-id="32aff-153">Sniðmátsstig</span><span class="sxs-lookup"><span data-stu-id="32aff-153">Mask level</span></span>            | <span data-ttu-id="32aff-154">Tölugildi frá **0** til og með **100**</span><span class="sxs-lookup"><span data-stu-id="32aff-154">A number from **0** through **100**</span></span> | <span data-ttu-id="32aff-155">Sniðmátið sem er beitt á myndskeiðið til útlitshönnun.</span><span class="sxs-lookup"><span data-stu-id="32aff-155">The mask that is applied to the video for styling.</span></span> |

## <a name="add-a-video-player-module-to-a-page"></a><span data-ttu-id="32aff-156">Bæta við myndspilaraeiningu á síðu</span><span class="sxs-lookup"><span data-stu-id="32aff-156">Add a video player module to a page</span></span>

> [!NOTE] 
> <span data-ttu-id="32aff-157">Áður en þú býrð til myndspilaraeiningu verðurðu fyrst að hlaða upp myndskeiði á fjölmiðlasafnið.</span><span class="sxs-lookup"><span data-stu-id="32aff-157">Before you create a video player module, you must first upload a video to the Media Library.</span></span>

<span data-ttu-id="32aff-158">Fylgdu þessum skrefum til að bæta myndspilaraeiningu við nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="32aff-158">To add a video player module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="32aff-159">Búðu til síðusniðmát sem heitir **myndspilarasniðmát**.</span><span class="sxs-lookup"><span data-stu-id="32aff-159">Create a page template that is named **video player template**.</span></span>
1. <span data-ttu-id="32aff-160">Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við gámaeiningu.</span><span class="sxs-lookup"><span data-stu-id="32aff-160">In the **Main** slot of the default page, add a container module.</span></span>
1. <span data-ttu-id="32aff-161">Bætið við myndspilara- og umhverfismyndspilaraeiningunum í gámaeiningunni.</span><span class="sxs-lookup"><span data-stu-id="32aff-161">In the container module, add video player and ambient video player modules.</span></span>
1. <span data-ttu-id="32aff-162">Ljúktu við að breyta sniðmátinu, vistaðu það og birtu.</span><span class="sxs-lookup"><span data-stu-id="32aff-162">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="32aff-163">Notaðu myndspilarasniðmátið sem þú stofnaðir til að búa til síðu sem heitir **myndspilarasíða**.</span><span class="sxs-lookup"><span data-stu-id="32aff-163">Use the video player template that you created to create a page that is named **video player page**.</span></span>
1. <span data-ttu-id="32aff-164">Í hólfinu **Aðal** á nýju síðunni bætirðu við einingu myndspilara.</span><span class="sxs-lookup"><span data-stu-id="32aff-164">In the **Main** slot of the new page, add a video player module.</span></span>
1. <span data-ttu-id="32aff-165">Í eiginleikaglugganum fyrir myndspilaraeininguna velurðu **Bæta við myndskeiði**.</span><span class="sxs-lookup"><span data-stu-id="32aff-165">In the property pane for the video player module, select **Add a video**.</span></span>
1. <span data-ttu-id="32aff-166">Í valmyndinni **Miðlaval** velurðu myndskeið og velur síðan **Hlaða upp nýjum miðli**.</span><span class="sxs-lookup"><span data-stu-id="32aff-166">In the **Media Picker** dialog box, select a video, and then select **Upload new media item**.</span></span>
1. <span data-ttu-id="32aff-167">Vistaðu og forskoðaðu síðuna.</span><span class="sxs-lookup"><span data-stu-id="32aff-167">Save and preview the page.</span></span> <span data-ttu-id="32aff-168">Þú ættir að sjá myndskeiðseininguna á síðunni.</span><span class="sxs-lookup"><span data-stu-id="32aff-168">You should see the video module on the page.</span></span> <span data-ttu-id="32aff-169">Þú getur breytt viðbótarstillingum til að sérsníða hegðun einingarinnar.</span><span class="sxs-lookup"><span data-stu-id="32aff-169">You can change additional settings to customize the behavior of the module.</span></span>
1. <span data-ttu-id="32aff-170">Ljúktu við að breyta síðunni, vistaðu hana og birtu.</span><span class="sxs-lookup"><span data-stu-id="32aff-170">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="32aff-171">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="32aff-171">Additional resources</span></span>

[<span data-ttu-id="32aff-172">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="32aff-172">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="32aff-173">Kynningarborðaeining</span><span class="sxs-lookup"><span data-stu-id="32aff-173">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="32aff-174">Myndaræmueining</span><span class="sxs-lookup"><span data-stu-id="32aff-174">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="32aff-175">Textabálkseining</span><span class="sxs-lookup"><span data-stu-id="32aff-175">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="32aff-176">Innihaldsbálkseining</span><span class="sxs-lookup"><span data-stu-id="32aff-176">Content block module</span></span>](add-hero-module.md)
