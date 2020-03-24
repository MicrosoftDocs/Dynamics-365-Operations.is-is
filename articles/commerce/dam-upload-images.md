---
title: Hlaða upp myndum
description: Þetta efni lýsir því hvernig á að hlaða upp myndum í vefsvæðishönnuði í Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8571c52b98a87751400dab9482168ee370834bcc
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/03/2020
ms.locfileid: "3097031"
---
# <a name="upload-images"></a><span data-ttu-id="cf07c-103">Hlaða upp myndum</span><span class="sxs-lookup"><span data-stu-id="cf07c-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cf07c-104">Þetta efni lýsir því hvernig á að hlaða upp myndum í vefsvæðishönnuði í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cf07c-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="cf07c-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="cf07c-105">Overview</span></span>

<span data-ttu-id="cf07c-106">Margmiðlunarsafn vefsvæðishönnuðar Commerce gerir þér kleift að hlaða inn myndum, annaðhvort stökum eða mörgum í einu með því að nota möppur.</span><span class="sxs-lookup"><span data-stu-id="cf07c-106">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="cf07c-107">Þú ættir alltaf að hlaða útgáfuna af myndinni með hæstu upplausn og gæðum, vegna þess að hluti myndbotans bætir sjálfkrafa myndina fyrir mismunandi skoðunargáttir og brotamörk þeirra.</span><span class="sxs-lookup"><span data-stu-id="cf07c-107">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="cf07c-108">Upplýsingar um mynd sem tilgreindar voru við upphleðslu</span><span class="sxs-lookup"><span data-stu-id="cf07c-108">Image information specified during upload</span></span>

<span data-ttu-id="cf07c-109">Þegar mynd er hlaðið inn er hægt að tilgreina eftirfarandi upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="cf07c-109">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="cf07c-110">**Titill, annar texti, lýsing, lykilorð**: Lýsigögn myndarinnar eða myndanna.</span><span class="sxs-lookup"><span data-stu-id="cf07c-110">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="cf07c-111">Titill og annar texti eru nauðsynleg gildi.</span><span class="sxs-lookup"><span data-stu-id="cf07c-111">Title and alt text are required values.</span></span>
- <span data-ttu-id="cf07c-112">**Velja tegund**:</span><span class="sxs-lookup"><span data-stu-id="cf07c-112">**Select category**:</span></span>
    - <span data-ttu-id="cf07c-113">**Enginn**: Notað fyrir sagnamynd eða myndir í e-verslun.</span><span class="sxs-lookup"><span data-stu-id="cf07c-113">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="cf07c-114">**Afurð, flokkur, viðskiptavinur, starfsmaður, vörulisti**: Notað fyrir Dynamics 365 Commerce alhliða mynd eða myndir.</span><span class="sxs-lookup"><span data-stu-id="cf07c-114">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="cf07c-115">**Birta eignir eftir upphleðslu**: Þegar þessi gátreitur er valinn birtast myndin eða myndirnar strax eftir upphleðslu.</span><span class="sxs-lookup"><span data-stu-id="cf07c-115">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="cf07c-116">Myndeignir með útlutaðan flokk eru einnig sjálfkrafa merktar með flokknum sem lykilorð til að hjálpa til að leita að eignum í tilteknum flokki.</span><span class="sxs-lookup"><span data-stu-id="cf07c-116">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="cf07c-117">Nafngiftavenjur fyrir alhliða myndir</span><span class="sxs-lookup"><span data-stu-id="cf07c-117">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="cf07c-118">Ef þú hefur stillt Margmiðlunarsafnið sem alhliða myndabakvinnslu er hægt að nota myndaflokka til að tilgreina hvaða flokk hlaðin mynd tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="cf07c-118">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="cf07c-119">Það er líka til nafngiftarvenja sem ætti að fylgja til að tryggja að myndir séu rétt sóttar af öðrum rásum, svo sem sölustað (POS).</span><span class="sxs-lookup"><span data-stu-id="cf07c-119">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="cf07c-120">Sjálfgefin nafngiftarvenja er breytileg eftir flokknum:</span><span class="sxs-lookup"><span data-stu-id="cf07c-120">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="cf07c-121">Myndir vörulista ættu að heita „**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**”</span><span class="sxs-lookup"><span data-stu-id="cf07c-121">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="cf07c-122">Flokkamyndir ættu að heita „**/Categories/\{CategoryName\}.png**”</span><span class="sxs-lookup"><span data-stu-id="cf07c-122">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="cf07c-123">Viðskiptavinamyndir ættu að heita „**/Customers/\{CustomerNumber\}.jpg**”</span><span class="sxs-lookup"><span data-stu-id="cf07c-123">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="cf07c-124">Starfsmannamyndir ættu að heita „**/Workers/\{WorkerNumber\}.jpg**”</span><span class="sxs-lookup"><span data-stu-id="cf07c-124">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="cf07c-125">Afurðamyndir ættu að heita „**/Products/\{ProductNumber\}_000_001.png**”</span><span class="sxs-lookup"><span data-stu-id="cf07c-125">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="cf07c-126">001 er röð myndarinnar og hún getur verið 001, 002, 003, 004 eða 005</span><span class="sxs-lookup"><span data-stu-id="cf07c-126">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="cf07c-127">Afuðaraðbrigðamyndir ættu að heita „**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**”</span><span class="sxs-lookup"><span data-stu-id="cf07c-127">Product variant images should be named "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="cf07c-128">Hlaða upp mynd</span><span class="sxs-lookup"><span data-stu-id="cf07c-128">Upload an image</span></span>

<span data-ttu-id="cf07c-129">Fylgdu þessum skrefum til að hlaða upp mynd í vefsvæðishönnuði.</span><span class="sxs-lookup"><span data-stu-id="cf07c-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="cf07c-130">Í vinstri stýriglugganum velurðu **Margmiðlunarsafn**.</span><span class="sxs-lookup"><span data-stu-id="cf07c-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="cf07c-131">Veldu á skipanastikunni **Hlaða inn \> Hlaða upp margmiðlun**.</span><span class="sxs-lookup"><span data-stu-id="cf07c-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="cf07c-132">Farðu í File Explorer gluggann og flettu að og veldu eina eða fleiri myndskrár sem þú vilt hlaða upp og veldu síðan **Opna**.</span><span class="sxs-lookup"><span data-stu-id="cf07c-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="cf07c-133">Í valmyndinni **Hlaða upp margmiðlun** slærðu inn nauðsynlegan titil og annan texta.</span><span class="sxs-lookup"><span data-stu-id="cf07c-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="cf07c-134">Sláðu inn valfrjálsa lýsingu og lykilorð og veldu flokk ef þess er óskað.</span><span class="sxs-lookup"><span data-stu-id="cf07c-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="cf07c-135">Ef þú vild birta mynd(ir) beint eftir uppflutning skaltu velja gátreitinn **Birta margmiðlunarefni eftir uppflutning**.</span><span class="sxs-lookup"><span data-stu-id="cf07c-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="cf07c-136">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cf07c-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="cf07c-137">Hlaða upp möppu með myndum</span><span class="sxs-lookup"><span data-stu-id="cf07c-137">Upload a folder of images</span></span>

<span data-ttu-id="cf07c-138">Fylgdu þessum skrefum til að hlaða upp fjölda mynda í myndamöppu í vefsvæðishönnuði.</span><span class="sxs-lookup"><span data-stu-id="cf07c-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="cf07c-139">Í vinstri stýriglugganum velurðu **Margmiðlunarsafn**.</span><span class="sxs-lookup"><span data-stu-id="cf07c-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="cf07c-140">Veldu á skipanastikunni **Hlaða inn \> Hlaða upp möppu**.</span><span class="sxs-lookup"><span data-stu-id="cf07c-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="cf07c-141">Farðu í File Explorer gluggann og flettu að og veldu möppu til að hlaða upp og veldu síðan **Opna**.</span><span class="sxs-lookup"><span data-stu-id="cf07c-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="cf07c-142">Í valmyndinni **Hlaða upp margmiðlunarefni** slærðu inn valkvæð leitarorð og veldu flokk ef þess er óskað.</span><span class="sxs-lookup"><span data-stu-id="cf07c-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="cf07c-143">Ef þú vild birta myndirnar í möppunni beint eftir uppflutning skaltu velja gátreitinn **Birta margmiðlunarefni eftir uppflutning**.</span><span class="sxs-lookup"><span data-stu-id="cf07c-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="cf07c-144">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cf07c-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cf07c-145">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="cf07c-145">Additional resources</span></span>

[<span data-ttu-id="cf07c-146">Yfirlit stafrænnar eignastýringar</span><span class="sxs-lookup"><span data-stu-id="cf07c-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="cf07c-147">Hlaða upp myndskeiði</span><span class="sxs-lookup"><span data-stu-id="cf07c-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="cf07c-148">Hlaða upp skrám</span><span class="sxs-lookup"><span data-stu-id="cf07c-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="cf07c-149">Skera myndir</span><span class="sxs-lookup"><span data-stu-id="cf07c-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="cf07c-150">Sérsníða þungamiðju myndar</span><span class="sxs-lookup"><span data-stu-id="cf07c-150">Customize image focal points</span></span>](dam-custom-focal-point.md)
