---
title: Hlaða upp öðrum skrám en myndum og myndskeiðum
description: Þetta efni lýsir því hvernig hægt er að hlaða upp tvöföldum skrám en myndum og myndböndum í vefsíðuhönnuði í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 380bcccd1053cbcc276e964ce97f16d1d39ea75a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799254"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="0f5a8-103">Hlaða upp skrám öðrum en myndum og myndböndum</span><span class="sxs-lookup"><span data-stu-id="0f5a8-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0f5a8-104">Þetta efni lýsir því hvernig hægt er að hlaða upp skrám en myndum og myndböndum í vefsíðuhönnuði í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0f5a8-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="0f5a8-105">Margmiðlunarsafn vefsvæðishönnuðar Commerce styður upphleðslu tvöfaldra eigna annarra en mynda eða myndskeiða.</span><span class="sxs-lookup"><span data-stu-id="0f5a8-105">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="0f5a8-106">Til dæmis gætirðu viljað hlaða inn Microsoft Excel, Microsoft Word, Microsoft PowerPoint eða PDF-skrám.</span><span class="sxs-lookup"><span data-stu-id="0f5a8-106">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="0f5a8-107">Eftirfarandi gerðir skjala eru studdar:</span><span class="sxs-lookup"><span data-stu-id="0f5a8-107">The following document types are supported:</span></span>
- <span data-ttu-id="0f5a8-108">7Z</span><span class="sxs-lookup"><span data-stu-id="0f5a8-108">7Z</span></span>
- <span data-ttu-id="0f5a8-109">AVI</span><span class="sxs-lookup"><span data-stu-id="0f5a8-109">AVI</span></span>
- <span data-ttu-id="0f5a8-110">CS</span><span class="sxs-lookup"><span data-stu-id="0f5a8-110">CS</span></span>
- <span data-ttu-id="0f5a8-111">CSS</span><span class="sxs-lookup"><span data-stu-id="0f5a8-111">CSS</span></span>
- <span data-ttu-id="0f5a8-112">DOC</span><span class="sxs-lookup"><span data-stu-id="0f5a8-112">DOC</span></span>
- <span data-ttu-id="0f5a8-113">DOCX</span><span class="sxs-lookup"><span data-stu-id="0f5a8-113">DOCX</span></span>
- <span data-ttu-id="0f5a8-114">EPUB</span><span class="sxs-lookup"><span data-stu-id="0f5a8-114">EPUB</span></span>
- <span data-ttu-id="0f5a8-115">GIF</span><span class="sxs-lookup"><span data-stu-id="0f5a8-115">GIF</span></span>
- <span data-ttu-id="0f5a8-116">INDD</span><span class="sxs-lookup"><span data-stu-id="0f5a8-116">INDD</span></span>
- <span data-ttu-id="0f5a8-117">JAR</span><span class="sxs-lookup"><span data-stu-id="0f5a8-117">JAR</span></span>
- <span data-ttu-id="0f5a8-118">JPG</span><span class="sxs-lookup"><span data-stu-id="0f5a8-118">JPG</span></span>
- <span data-ttu-id="0f5a8-119">JPEG</span><span class="sxs-lookup"><span data-stu-id="0f5a8-119">JPEG</span></span>
- <span data-ttu-id="0f5a8-120">JS</span><span class="sxs-lookup"><span data-stu-id="0f5a8-120">JS</span></span>
- <span data-ttu-id="0f5a8-121">MP3</span><span class="sxs-lookup"><span data-stu-id="0f5a8-121">MP3</span></span>
- <span data-ttu-id="0f5a8-122">MP4</span><span class="sxs-lookup"><span data-stu-id="0f5a8-122">MP4</span></span>
- <span data-ttu-id="0f5a8-123">MPEG</span><span class="sxs-lookup"><span data-stu-id="0f5a8-123">MPEG</span></span>
- <span data-ttu-id="0f5a8-124">MPG</span><span class="sxs-lookup"><span data-stu-id="0f5a8-124">MPG</span></span>
- <span data-ttu-id="0f5a8-125">ODP</span><span class="sxs-lookup"><span data-stu-id="0f5a8-125">ODP</span></span>
- <span data-ttu-id="0f5a8-126">ODS</span><span class="sxs-lookup"><span data-stu-id="0f5a8-126">ODS</span></span>
- <span data-ttu-id="0f5a8-127">ODT</span><span class="sxs-lookup"><span data-stu-id="0f5a8-127">ODT</span></span>
- <span data-ttu-id="0f5a8-128">PDF</span><span class="sxs-lookup"><span data-stu-id="0f5a8-128">PDF</span></span>
- <span data-ttu-id="0f5a8-129">PNG</span><span class="sxs-lookup"><span data-stu-id="0f5a8-129">PNG</span></span>
- <span data-ttu-id="0f5a8-130">PPT</span><span class="sxs-lookup"><span data-stu-id="0f5a8-130">PPT</span></span>
- <span data-ttu-id="0f5a8-131">PPTX</span><span class="sxs-lookup"><span data-stu-id="0f5a8-131">PPTX</span></span>
- <span data-ttu-id="0f5a8-132">PS</span><span class="sxs-lookup"><span data-stu-id="0f5a8-132">PS</span></span>
- <span data-ttu-id="0f5a8-133">QXP</span><span class="sxs-lookup"><span data-stu-id="0f5a8-133">QXP</span></span>
- <span data-ttu-id="0f5a8-134">RAR</span><span class="sxs-lookup"><span data-stu-id="0f5a8-134">RAR</span></span>
- <span data-ttu-id="0f5a8-135">RTF</span><span class="sxs-lookup"><span data-stu-id="0f5a8-135">RTF</span></span>
- <span data-ttu-id="0f5a8-136">SVG</span><span class="sxs-lookup"><span data-stu-id="0f5a8-136">SVG</span></span>
- <span data-ttu-id="0f5a8-137">TAR</span><span class="sxs-lookup"><span data-stu-id="0f5a8-137">TAR</span></span>
- <span data-ttu-id="0f5a8-138">TGZ</span><span class="sxs-lookup"><span data-stu-id="0f5a8-138">TGZ</span></span>
- <span data-ttu-id="0f5a8-139">TXT</span><span class="sxs-lookup"><span data-stu-id="0f5a8-139">TXT</span></span>
- <span data-ttu-id="0f5a8-140">WMV</span><span class="sxs-lookup"><span data-stu-id="0f5a8-140">WMV</span></span>
- <span data-ttu-id="0f5a8-141">XLS</span><span class="sxs-lookup"><span data-stu-id="0f5a8-141">XLS</span></span>
- <span data-ttu-id="0f5a8-142">XLSX</span><span class="sxs-lookup"><span data-stu-id="0f5a8-142">XLSX</span></span>
- <span data-ttu-id="0f5a8-143">XML</span><span class="sxs-lookup"><span data-stu-id="0f5a8-143">XML</span></span>
- <span data-ttu-id="0f5a8-144">ZIP</span><span class="sxs-lookup"><span data-stu-id="0f5a8-144">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="0f5a8-145">Hlaða upp skrá</span><span class="sxs-lookup"><span data-stu-id="0f5a8-145">Upload a file</span></span>

<span data-ttu-id="0f5a8-146">Til að hlaða upp skrá í vefsíðuhönnuð í Commerce skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="0f5a8-146">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="0f5a8-147">Í vinstri stýriglugganum velurðu **Margmiðlunarsafn**.</span><span class="sxs-lookup"><span data-stu-id="0f5a8-147">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="0f5a8-148">Veldu á skipanastikunni **Hlaða inn \> Hlaða upp margmiðlun**.</span><span class="sxs-lookup"><span data-stu-id="0f5a8-148">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="0f5a8-149">Veldu File Explorer eina eða fleiri skrár og veldu síðan **Opna**.</span><span class="sxs-lookup"><span data-stu-id="0f5a8-149">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="0f5a8-150">Í valmyndinni **Hlaða upp margmiðlun** slærðu inn titil, lýsingu og lýsigögn leitarorðs eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="0f5a8-150">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="0f5a8-151">Til að birta skár beint eftir uppflutning skaltu velja gátreitinn **Birta margmiðlunarefni eftir uppflutning**.</span><span class="sxs-lookup"><span data-stu-id="0f5a8-151">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="0f5a8-152">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0f5a8-152">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f5a8-153">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="0f5a8-153">Additional resources</span></span>

[<span data-ttu-id="0f5a8-154">Yfirlit stafrænnar eignastýringar</span><span class="sxs-lookup"><span data-stu-id="0f5a8-154">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="0f5a8-155">Hlaða upp myndum</span><span class="sxs-lookup"><span data-stu-id="0f5a8-155">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="0f5a8-156">Hlaða upp myndbandi</span><span class="sxs-lookup"><span data-stu-id="0f5a8-156">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="0f5a8-157">Skera myndir</span><span class="sxs-lookup"><span data-stu-id="0f5a8-157">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="0f5a8-158">Sérstilla áherslupunkta myndar</span><span class="sxs-lookup"><span data-stu-id="0f5a8-158">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="0f5a8-159">Hlaða upp og þjóna föstum skrám</span><span class="sxs-lookup"><span data-stu-id="0f5a8-159">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
