---
title: Hlaða upp myndum
description: Þetta efnisatriði lýsir hvernig á að hlaða upp myndum á Microsoft Dynamics 365 Commerce svæðasmið.
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
ms.openlocfilehash: 2a0a2fdb275cbeb65c06c01128e90ba660f98c9b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799230"
---
# <a name="upload-images"></a><span data-ttu-id="793ea-103">Hlaða upp myndum</span><span class="sxs-lookup"><span data-stu-id="793ea-103">Upload images</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="793ea-104">Þetta efnisatriði lýsir hvernig á að hlaða upp myndum á Microsoft Dynamics 365 Commerce svæðasmið.</span><span class="sxs-lookup"><span data-stu-id="793ea-104">This topic describes how to upload images in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="793ea-105">Margmiðlunarsafn vefsvæðishönnuðar Commerce gerir þér kleift að hlaða inn myndum, annaðhvort stökum eða mörgum í einu með því að nota möppur.</span><span class="sxs-lookup"><span data-stu-id="793ea-105">The Commerce site builder Media Library allows you to upload images, either singly or in bulk using folders.</span></span> <span data-ttu-id="793ea-106">Þú ættir alltaf að hlaða útgáfuna af myndinni með hæstu upplausn og gæðum, vegna þess að hluti myndbotans bætir sjálfkrafa myndina fyrir mismunandi skoðunargáttir og brotamörk þeirra.</span><span class="sxs-lookup"><span data-stu-id="793ea-106">You should always upload the version of the image with highest resolution and quality, because the image resizer component will automatically optimize the image for different viewports and their breakpoints.</span></span>

### <a name="image-information-specified-during-upload"></a><span data-ttu-id="793ea-107">Upplýsingar um mynd sem tilgreindar voru við upphleðslu</span><span class="sxs-lookup"><span data-stu-id="793ea-107">Image information specified during upload</span></span>

<span data-ttu-id="793ea-108">Þegar mynd er hlaðið inn er hægt að tilgreina eftirfarandi upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="793ea-108">When uploading an image, the following information can be specified.</span></span>

- <span data-ttu-id="793ea-109">**Titill, annar texti, lýsing, lykilorð**: Lýsigögn myndarinnar eða myndanna.</span><span class="sxs-lookup"><span data-stu-id="793ea-109">**Title, Alt Text, Description, Keywords**: Metadata of the image or images.</span></span> <span data-ttu-id="793ea-110">Titill og annar texti eru nauðsynleg gildi.</span><span class="sxs-lookup"><span data-stu-id="793ea-110">Title and alt text are required values.</span></span>
- <span data-ttu-id="793ea-111">**Velja tegund**:</span><span class="sxs-lookup"><span data-stu-id="793ea-111">**Select category**:</span></span>
    - <span data-ttu-id="793ea-112">**Enginn**: Notað fyrir sagnamynd eða myndir í e-verslun.</span><span class="sxs-lookup"><span data-stu-id="793ea-112">**None**: Used for an e-Commerce storytelling image or images.</span></span>
    - <span data-ttu-id="793ea-113">**Afurð, flokkur, viðskiptavinur, starfsmaður, vörulisti**: Notað fyrir Dynamics 365 Commerce alhliða mynd eða myndir.</span><span class="sxs-lookup"><span data-stu-id="793ea-113">**Product, Category, Customer, Employee, Catalog**: Used for Dynamics 365 Commerce omni-channel image or images.</span></span>
- <span data-ttu-id="793ea-114">**Birta eignir eftir upphleðslu**: Þegar þessi gátreitur er valinn birtast myndin eða myndirnar strax eftir upphleðslu.</span><span class="sxs-lookup"><span data-stu-id="793ea-114">**Publish assets after upload**: When this check box is selected, the image or images are published immediately after upload.</span></span>

> [!NOTE]
> <span data-ttu-id="793ea-115">Myndeignir með útlutaðan flokk eru einnig sjálfkrafa merktar með flokknum sem lykilorð til að hjálpa til að leita að eignum í tilteknum flokki.</span><span class="sxs-lookup"><span data-stu-id="793ea-115">Image assets with a category assigned are also automatically tagged with the category as a keyword to aid searching for assets of a specific category.</span></span>

### <a name="naming-conventions-for-omni-channel-images"></a><span data-ttu-id="793ea-116">Nafngiftavenjur fyrir alhliða myndir</span><span class="sxs-lookup"><span data-stu-id="793ea-116">Naming conventions for omni-channel images</span></span> 

<span data-ttu-id="793ea-117">Ef þú hefur stillt Margmiðlunarsafnið sem alhliða myndabakvinnslu er hægt að nota myndaflokka til að tilgreina hvaða flokk hlaðin mynd tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="793ea-117">If you have configured the Media Library as the omni-channel image backend, you can use image categories to indicate which category the uploaded image belongs to.</span></span> <span data-ttu-id="793ea-118">Það er líka til nafngiftarvenja sem ætti að fylgja til að tryggja að myndir séu rétt sóttar af öðrum rásum, svo sem sölustað (POS).</span><span class="sxs-lookup"><span data-stu-id="793ea-118">There is also a naming convention that should be followed to ensure that images are retrieved correctly by other channels, such as point of sale (POS).</span></span>

<span data-ttu-id="793ea-119">Sjálfgefin nafngiftarvenja er breytileg eftir flokknum:</span><span class="sxs-lookup"><span data-stu-id="793ea-119">The default naming convention varies based on the category:</span></span>
- <span data-ttu-id="793ea-120">Myndir vörulista ættu að heita „**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**”</span><span class="sxs-lookup"><span data-stu-id="793ea-120">Catalog images should be named "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"</span></span>
- <span data-ttu-id="793ea-121">Flokkamyndir ættu að heita „**/Categories/\{CategoryName\}.png**”</span><span class="sxs-lookup"><span data-stu-id="793ea-121">Category images should be named "**/Categories/\{CategoryName\}.png**"</span></span>
- <span data-ttu-id="793ea-122">Viðskiptavinamyndir ættu að heita „**/Customers/\{CustomerNumber\}.jpg**”</span><span class="sxs-lookup"><span data-stu-id="793ea-122">Customer images should be named "**/Customers/\{CustomerNumber\}.jpg**"</span></span>
- <span data-ttu-id="793ea-123">Starfsmannamyndir ættu að heita „**/Workers/\{WorkerNumber\}.jpg**”</span><span class="sxs-lookup"><span data-stu-id="793ea-123">Employee images should be named "**/Workers/\{WorkerNumber\}.jpg**"</span></span>
- <span data-ttu-id="793ea-124">Afurðamyndir ættu að heita „**/Products/\{ProductNumber\}_000_001.png**”</span><span class="sxs-lookup"><span data-stu-id="793ea-124">Product images should be named "**/Products/\{ProductNumber\}_000_001.png**"</span></span>
    - <span data-ttu-id="793ea-125">001 er röð myndarinnar og hún getur verið 001, 002, 003, 004 eða 005</span><span class="sxs-lookup"><span data-stu-id="793ea-125">001 is the sequence of the image and it can be 001, 002, 003, 004 or 005</span></span>
- <span data-ttu-id="793ea-126">Afuðaraðbrigðamyndir ættu að heita „**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**“</span><span class="sxs-lookup"><span data-stu-id="793ea-126">Product variant images should be named "**/Products/\{ProductNumber\} \^ \{Style\} \^ \{Size\} \^ \{Color\} \^\_000_001.png**"</span></span>
    - <span data-ttu-id="793ea-127">Til dæmis: 93039 \^ \^ 2 \^ Svart \^_000_001.png</span><span class="sxs-lookup"><span data-stu-id="793ea-127">For example: 93039 \^ \^ 2 \^ Black \^_000_001.png</span></span>

## <a name="upload-an-image"></a><span data-ttu-id="793ea-128">Hlaða upp mynd</span><span class="sxs-lookup"><span data-stu-id="793ea-128">Upload an image</span></span>

<span data-ttu-id="793ea-129">Fylgdu þessum skrefum til að hlaða upp mynd í vefsvæðishönnuði.</span><span class="sxs-lookup"><span data-stu-id="793ea-129">To upload an image in site builder, follow these steps.</span></span>

1. <span data-ttu-id="793ea-130">Í vinstri stýriglugganum velurðu **Margmiðlunarsafn**.</span><span class="sxs-lookup"><span data-stu-id="793ea-130">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="793ea-131">Veldu á skipanastikunni **Hlaða inn \> Hlaða upp margmiðlun**.</span><span class="sxs-lookup"><span data-stu-id="793ea-131">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="793ea-132">Farðu í File Explorer gluggann og flettu að og veldu eina eða fleiri myndskrár sem þú vilt hlaða upp og veldu síðan **Opna**.</span><span class="sxs-lookup"><span data-stu-id="793ea-132">In the File Explorer window, navigate to and select one or more image files to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="793ea-133">Í valmyndinni **Hlaða upp margmiðlun** slærðu inn nauðsynlegan titil og annan texta.</span><span class="sxs-lookup"><span data-stu-id="793ea-133">In the **Upload Media Item** dialog box, enter the required title and alt text.</span></span>
1. <span data-ttu-id="793ea-134">Sláðu inn valfrjálsa lýsingu og lykilorð og veldu flokk ef þess er óskað.</span><span class="sxs-lookup"><span data-stu-id="793ea-134">Enter optional description and keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="793ea-135">Ef þú vild birta mynd(ir) beint eftir uppflutning skaltu velja gátreitinn **Birta margmiðlunarefni eftir uppflutning**.</span><span class="sxs-lookup"><span data-stu-id="793ea-135">If you want to publish the image(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="793ea-136">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="793ea-136">Select **OK**.</span></span>

## <a name="upload-a-folder-of-images"></a><span data-ttu-id="793ea-137">Hlaða upp möppu með myndum</span><span class="sxs-lookup"><span data-stu-id="793ea-137">Upload a folder of images</span></span>

<span data-ttu-id="793ea-138">Fylgdu þessum skrefum til að hlaða upp fjölda mynda í myndamöppu í vefsvæðishönnuði.</span><span class="sxs-lookup"><span data-stu-id="793ea-138">To bulk upload a folder of images in site builder, follow these steps.</span></span>

1. <span data-ttu-id="793ea-139">Í vinstri stýriglugganum velurðu **Margmiðlunarsafn**.</span><span class="sxs-lookup"><span data-stu-id="793ea-139">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="793ea-140">Veldu á skipanastikunni **Hlaða inn \> Hlaða upp möppu**.</span><span class="sxs-lookup"><span data-stu-id="793ea-140">On the command bar, select **Upload \> Upload Folder**.</span></span>
1. <span data-ttu-id="793ea-141">Farðu í File Explorer gluggann og flettu að og veldu möppu til að hlaða upp og veldu síðan **Opna**.</span><span class="sxs-lookup"><span data-stu-id="793ea-141">In the File Explorer window, navigate to and select a folder to upload, and then select **Open**.</span></span>
1. <span data-ttu-id="793ea-142">Í valmyndinni **Hlaða upp margmiðlunarefni** slærðu inn valkvæð leitarorð og veldu flokk ef þess er óskað.</span><span class="sxs-lookup"><span data-stu-id="793ea-142">In the **Upload Media Items** dialog box, enter optional keywords and select a category if desired.</span></span> 
1. <span data-ttu-id="793ea-143">Ef þú vild birta myndirnar í möppunni beint eftir uppflutning skaltu velja gátreitinn **Birta margmiðlunarefni eftir uppflutning**.</span><span class="sxs-lookup"><span data-stu-id="793ea-143">If you want to publish the images in the folder immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="793ea-144">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="793ea-144">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="793ea-145">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="793ea-145">Additional resources</span></span>

[<span data-ttu-id="793ea-146">Yfirlit stafrænnar eignastýringar</span><span class="sxs-lookup"><span data-stu-id="793ea-146">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="793ea-147">Hlaða upp myndbandi</span><span class="sxs-lookup"><span data-stu-id="793ea-147">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="793ea-148">Hlaða upp skrám</span><span class="sxs-lookup"><span data-stu-id="793ea-148">Upload files</span></span>](dam-upload-files.md)

[<span data-ttu-id="793ea-149">Skera myndir</span><span class="sxs-lookup"><span data-stu-id="793ea-149">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="793ea-150">Sérstilla áherslupunkta myndar</span><span class="sxs-lookup"><span data-stu-id="793ea-150">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="793ea-151">Hlaða upp og þjóna föstum skrám</span><span class="sxs-lookup"><span data-stu-id="793ea-151">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
