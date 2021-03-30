---
title: Hlaða upp myndskeiðum
description: Þetta efnisatriði lýsir því hvernig hægt er að hlaða upp myndböndum í vefsíðuhönnuði í Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 03/03/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d74e7116d68074bfc917784a8f51f85d5682c5d6
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213843"
---
# <a name="upload-videos"></a><span data-ttu-id="a382b-103">Hlaða upp myndskeiðum</span><span class="sxs-lookup"><span data-stu-id="a382b-103">Upload videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a382b-104">Þetta efnisatriði lýsir því hvernig hægt er að hlaða upp myndböndum í vefsíðuhönnuði í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a382b-104">This topic describes how to upload videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="a382b-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="a382b-105">Overview</span></span>

<span data-ttu-id="a382b-106">Margmiðlunarsafn vefsíðuhönnuðar Commerce gerir þér kleift að hlaða upp myndskeiðum.</span><span class="sxs-lookup"><span data-stu-id="a382b-106">The Commerce site builder Media Library allows you to upload videos.</span></span> <span data-ttu-id="a382b-107">Þú ættir alltaf að hlaða útgáfu af vídeói með hæsta bitahraða og upplausn, því vídeóinu verður sjálfkrafa breytt til að henta fyrir mismunandi skoðunargáttir og brotamörk þeirra.</span><span class="sxs-lookup"><span data-stu-id="a382b-107">You should always upload the version of a video with the highest bitrate and resolution, because the video will be automatically converted to be suitable for different viewports and their breakpoints.</span></span>

### <a name="video-information-specified-during-upload"></a><span data-ttu-id="a382b-108">Upplýsingar um myndskeið sem tilgreindar voru við upphleðslu</span><span class="sxs-lookup"><span data-stu-id="a382b-108">Video information specified during upload</span></span>

<span data-ttu-id="a382b-109">Þegar myndskeiði er hlaðið inn er hægt að tilgreina eftirfarandi upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="a382b-109">When uploading a video, the following information can be specified.</span></span>

- <span data-ttu-id="a382b-110">**Titill, lýsing, lykilorð**: Lýsigögn myndbandsins.</span><span class="sxs-lookup"><span data-stu-id="a382b-110">**Title, Description, Keywords**: Metadata of the video.</span></span>
- <span data-ttu-id="a382b-111">**Mynda lokaða myndatexta sjálfvirkt**: Tilgreinir hvort mynda eigi myndatexta sjálfkrafa fyrir myndbandið.</span><span class="sxs-lookup"><span data-stu-id="a382b-111">**Automatically generate closed captions**: Specifies whether closed captions should be automatically generated for the video.</span></span>
- <span data-ttu-id="a382b-112">**Lokaður myndatexti**: Tilgreinir lokaða myndatexta sem nota á.</span><span class="sxs-lookup"><span data-stu-id="a382b-112">**Closed Caption**: Specifies the closed captions to be used.</span></span>
- <span data-ttu-id="a382b-113">**Venjulegt hljóð**: Tilgreinir venjulegt hljóðrás sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="a382b-113">**Regular Audio**: Specifies the regular audio track to be used.</span></span>
- <span data-ttu-id="a382b-114">**Smámynd**: Tilgreinir smámynd fyrir myndbandið.</span><span class="sxs-lookup"><span data-stu-id="a382b-114">**Thumbnail**: Specifies the thumbnail for the video.</span></span> <span data-ttu-id="a382b-115">Ef hún er ekki tilgreind verður hún mynduð sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="a382b-115">If not specified, it will be generated automatically.</span></span>
- <span data-ttu-id="a382b-116">**Lýsandi hljóð**: Tilgreinir lýsandi hljóðrás sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="a382b-116">**Descriptive Audio**: Specifies the descriptive audio track to be used.</span></span>

## <a name="upload-a-video"></a><span data-ttu-id="a382b-117">Hlaða upp myndskeiði</span><span class="sxs-lookup"><span data-stu-id="a382b-117">Upload a video</span></span>

<span data-ttu-id="a382b-118">Fylgdu þessum skrefum til að hlaða upp myndskeiði í vefsvæðishönnuði.</span><span class="sxs-lookup"><span data-stu-id="a382b-118">To upload a video in site builder, follow these steps.</span></span>

1. <span data-ttu-id="a382b-119">Í vinstri stýriglugganum velurðu **Margmiðlunarsafn**.</span><span class="sxs-lookup"><span data-stu-id="a382b-119">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="a382b-120">Veldu á skipanastikunni **Hlaða inn \> Hlaða upp margmiðlun**.</span><span class="sxs-lookup"><span data-stu-id="a382b-120">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="a382b-121">Farðu í File Explorer gluggann og flettu að og veldu eitt eða fleiri myndskeið sem þú vilt hlaða upp og veldu síðan **Opna**.</span><span class="sxs-lookup"><span data-stu-id="a382b-121">In the File Explorer window, navigate to and select one or more video files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="a382b-122">Í valmyndinni **Hlaða upp margmiðlun** slærðu inn nauðsynlegan titil og annan texta.</span><span class="sxs-lookup"><span data-stu-id="a382b-122">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="a382b-123">Sláðu inn valfrjálsa lýsingu og lykilorð og veldu flokk ef þess er óskað.</span><span class="sxs-lookup"><span data-stu-id="a382b-123">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="a382b-124">Ef þú vild birta mynd(ir) beint eftir uppflutning skaltu velja gátreitinn **Birta margmiðlunarefni eftir uppflutning**</span><span class="sxs-lookup"><span data-stu-id="a382b-124">If you want to publish the image(s) after immediately upload, select the **Publish media items after upload** check box</span></span>
1. <span data-ttu-id="a382b-125">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a382b-125">Select **OK**.</span></span>

<span data-ttu-id="a382b-126">Ef þú ert að hlaða inn mörgum tegundum eigna samtímis (til dæmis myndum og myndböndum), í valmyndinni **Hlaða upp margmiðlunarefni** verður aðeins hægt að tilgreina lykilorð, hvort skrárnar skuli gefnar út strax eftir upphleðslu og hvort sjálfkrafa ætti að búa til lokaða myndatexta fyrir myndbandsskrár.</span><span class="sxs-lookup"><span data-stu-id="a382b-126">If you are uploading multiple types of assets simultaneously (for example, images and videos), in the **Upload Media Item** dialog box you will only be able to specify keywords, whether the files should be published immediately after upload, and whether closed captions should be automatically generated for video files.</span></span> <span data-ttu-id="a382b-127">Allar eignir munu deila sömu lykilorðum.</span><span class="sxs-lookup"><span data-stu-id="a382b-127">All the assets will share the same keywords.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a382b-128">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a382b-128">Additional resources</span></span>

[<span data-ttu-id="a382b-129">Yfirlit stafrænnar eignastýringar</span><span class="sxs-lookup"><span data-stu-id="a382b-129">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="a382b-130">Hlaða upp myndum</span><span class="sxs-lookup"><span data-stu-id="a382b-130">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="a382b-131">Hlaða upp skrám</span><span class="sxs-lookup"><span data-stu-id="a382b-131">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="a382b-132">Skera myndir</span><span class="sxs-lookup"><span data-stu-id="a382b-132">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="a382b-133">Sérstilla áherslupunkta myndar</span><span class="sxs-lookup"><span data-stu-id="a382b-133">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="a382b-134">Hlaða upp og þjóna föstum skrám</span><span class="sxs-lookup"><span data-stu-id="a382b-134">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]