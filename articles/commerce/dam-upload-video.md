---
title: Hlaða upp myndskeiðum
description: Þetta efnisatriði lýsir því hvernig hægt er að hlaða upp myndböndum í vefsíðuhönnuði í Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5ec20f8caee2f5a62230be05923dfd52600c1e35
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799206"
---
# <a name="upload-videos"></a><span data-ttu-id="1dc64-103">Hlaða upp myndskeiðum</span><span class="sxs-lookup"><span data-stu-id="1dc64-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1dc64-104">Þetta efnisatriði lýsir því hvernig hægt er að hlaða upp myndböndum í vefsíðuhönnuði í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1dc64-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="1dc64-105">Margmiðlunarsafn vefsíðuhönnuðar Commerce gerir þér kleift að hlaða upp myndskeiðum.</span><span class="sxs-lookup"><span data-stu-id="1dc64-105">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="1dc64-106">Þú ættir alltaf að hlaða útgáfu af vídeói með hæsta bitahraða og upplausn, því vídeóinu verður sjálfkrafa breytt til að henta fyrir mismunandi skoðunargáttir og brotamörk þeirra.</span><span class="sxs-lookup"><span data-stu-id="1dc64-106">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="1dc64-107">Upplýsingar um myndskeið sem tilgreindar voru við upphleðslu</span><span class="sxs-lookup"><span data-stu-id="1dc64-107">Video information specified during upload</span></span>

<span data-ttu-id="1dc64-108">Þegar myndskeiði er hlaðið inn er hægt að tilgreina eftirfarandi upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="1dc64-108">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="1dc64-109">**Titill, lýsing, lykilorð**: Lýsigögn myndbandsins.</span><span class="sxs-lookup"><span data-stu-id="1dc64-109">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="1dc64-110">**Mynda lokaða myndatexta sjálfvirkt**: Tilgreinir hvort mynda eigi myndatexta sjálfkrafa fyrir myndbandið.</span><span class="sxs-lookup"><span data-stu-id="1dc64-110">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="1dc64-111">**Lokaður myndatexti**: Tilgreinir lokaða myndatexta sem nota á.</span><span class="sxs-lookup"><span data-stu-id="1dc64-111">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="1dc64-112">**Venjulegt hljóð**: Tilgreinir venjulegt hljóðrás sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="1dc64-112">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="1dc64-113">**Smámynd**: Tilgreinir smámynd fyrir myndbandið.</span><span class="sxs-lookup"><span data-stu-id="1dc64-113">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="1dc64-114">Ef hún er ekki tilgreind verður hún mynduð sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="1dc64-114">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="1dc64-115">**Lýsandi hljóð**: Tilgreinir lýsandi hljóðrás sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="1dc64-115">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="1dc64-116">Hlaða upp myndskeiði</span><span class="sxs-lookup"><span data-stu-id="1dc64-116">Upload a video</span></span>

<span data-ttu-id="1dc64-117">Fylgdu þessum skrefum til að hlaða upp myndskeiði í vefsvæðishönnuði.</span><span class="sxs-lookup"><span data-stu-id="1dc64-117">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="1dc64-118">Í vinstri stýriglugganum velurðu **Margmiðlunarsafn**.</span><span class="sxs-lookup"><span data-stu-id="1dc64-118">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="1dc64-119">Veldu á skipanastikunni **Hlaða inn \> Hlaða upp margmiðlun**.</span><span class="sxs-lookup"><span data-stu-id="1dc64-119">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="1dc64-120">Farðu í File Explorer gluggann og flettu að og veldu eitt eða fleiri myndskeið sem þú vilt hlaða upp og veldu síðan **Opna**.</span><span class="sxs-lookup"><span data-stu-id="1dc64-120">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="1dc64-121">Í valmyndinni **Hlaða upp margmiðlun** slærðu inn nauðsynlegan titil og annan texta.</span><span class="sxs-lookup"><span data-stu-id="1dc64-121">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="1dc64-122">Sláðu inn valfrjálsa lýsingu og lykilorð og veldu flokk ef þess er óskað.</span><span class="sxs-lookup"><span data-stu-id="1dc64-122">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="1dc64-123">Ef þú vild birta mynd(ir) beint eftir uppflutning skaltu velja gátreitinn **Birta margmiðlunarefni eftir uppflutning**</span><span class="sxs-lookup"><span data-stu-id="1dc64-123">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="1dc64-124">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="1dc64-124">Select **OK**.</span></span>

<span data-ttu-id="1dc64-125">Ef þú ert að hlaða inn mörgum tegundum eigna samtímis (til dæmis myndum og myndböndum), í valmyndinni **Hlaða upp margmiðlunarefni** verður aðeins hægt að tilgreina lykilorð, hvort skrárnar skuli gefnar út strax eftir upphleðslu og hvort sjálfkrafa ætti að búa til lokaða myndatexta fyrir myndbandsskrár.</span><span class="sxs-lookup"><span data-stu-id="1dc64-125">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="1dc64-126">Allar eignir munu deila sömu lykilorðum.</span><span class="sxs-lookup"><span data-stu-id="1dc64-126">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1dc64-127">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="1dc64-127">Additional resources</span></span>

[<span data-ttu-id="1dc64-128">Yfirlit stafrænnar eignastýringar</span><span class="sxs-lookup"><span data-stu-id="1dc64-128">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="1dc64-129">Hlaða upp myndum</span><span class="sxs-lookup"><span data-stu-id="1dc64-129">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="1dc64-130">Hlaða upp skrám</span><span class="sxs-lookup"><span data-stu-id="1dc64-130">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="1dc64-131">Skera myndir</span><span class="sxs-lookup"><span data-stu-id="1dc64-131">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="1dc64-132">Sérstilla áherslupunkta myndar</span><span class="sxs-lookup"><span data-stu-id="1dc64-132">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="1dc64-133">Hlaða upp og þjóna föstum skrám</span><span class="sxs-lookup"><span data-stu-id="1dc64-133">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
