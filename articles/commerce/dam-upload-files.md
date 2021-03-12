---
title: Hlaða upp öðrum skrám en myndum og myndskeiðum
description: Þetta efni lýsir því hvernig hægt er að hlaða upp tvöföldum skrám en myndum og myndböndum í vefsíðuhönnuði í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 3392f5f36d04e8cb0a9d6e6b7db31ff62c987649
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995771"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="ad99f-103">Hlaða upp öðrum skrám en myndum og myndskeiðum</span><span class="sxs-lookup"><span data-stu-id="ad99f-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ad99f-104">Þetta efni lýsir því hvernig hægt er að hlaða upp skrám en myndum og myndböndum í vefsíðuhönnuði í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ad99f-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="ad99f-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="ad99f-105">Overview</span></span>

<span data-ttu-id="ad99f-106">Margmiðlunarsafn vefsvæðishönnuðar Commerce styður upphleðslu tvöfaldra eigna annarra en mynda eða myndskeiða.</span><span class="sxs-lookup"><span data-stu-id="ad99f-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="ad99f-107">Til dæmis gætirðu viljað hlaða inn Microsoft Excel, Microsoft Word, Microsoft PowerPoint eða PDF-skrám.</span><span class="sxs-lookup"><span data-stu-id="ad99f-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="ad99f-108">Eftirfarandi gerðir skjala eru studdar:</span><span class="sxs-lookup"><span data-stu-id="ad99f-108">The following document types are supported:</span></span>
- <span data-ttu-id="ad99f-109">7Z</span><span class="sxs-lookup"><span data-stu-id="ad99f-109">7Z</span></span>
- <span data-ttu-id="ad99f-110">AVI</span><span class="sxs-lookup"><span data-stu-id="ad99f-110">AVI</span></span>
- <span data-ttu-id="ad99f-111">CS</span><span class="sxs-lookup"><span data-stu-id="ad99f-111">CS</span></span>
- <span data-ttu-id="ad99f-112">CSS</span><span class="sxs-lookup"><span data-stu-id="ad99f-112">CSS</span></span>
- <span data-ttu-id="ad99f-113">DOC</span><span class="sxs-lookup"><span data-stu-id="ad99f-113">DOC</span></span>
- <span data-ttu-id="ad99f-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="ad99f-114">DOCX</span></span>
- <span data-ttu-id="ad99f-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="ad99f-115">EPUB</span></span>
- <span data-ttu-id="ad99f-116">GIF</span><span class="sxs-lookup"><span data-stu-id="ad99f-116">GIF</span></span>
- <span data-ttu-id="ad99f-117">INDD</span><span class="sxs-lookup"><span data-stu-id="ad99f-117">INDD</span></span>
- <span data-ttu-id="ad99f-118">JAR</span><span class="sxs-lookup"><span data-stu-id="ad99f-118">JAR</span></span>
- <span data-ttu-id="ad99f-119">JPG</span><span class="sxs-lookup"><span data-stu-id="ad99f-119">JPG</span></span>
- <span data-ttu-id="ad99f-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="ad99f-120">JPEG</span></span>
- <span data-ttu-id="ad99f-121">JS</span><span class="sxs-lookup"><span data-stu-id="ad99f-121">JS</span></span>
- <span data-ttu-id="ad99f-122">MP3</span><span class="sxs-lookup"><span data-stu-id="ad99f-122">MP3</span></span>
- <span data-ttu-id="ad99f-123">MP4</span><span class="sxs-lookup"><span data-stu-id="ad99f-123">MP4</span></span>
- <span data-ttu-id="ad99f-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="ad99f-124">MPEG</span></span>
- <span data-ttu-id="ad99f-125">MPG</span><span class="sxs-lookup"><span data-stu-id="ad99f-125">MPG</span></span>
- <span data-ttu-id="ad99f-126">ODP</span><span class="sxs-lookup"><span data-stu-id="ad99f-126">ODP</span></span>
- <span data-ttu-id="ad99f-127">ODS</span><span class="sxs-lookup"><span data-stu-id="ad99f-127">ODS</span></span>
- <span data-ttu-id="ad99f-128">ODT</span><span class="sxs-lookup"><span data-stu-id="ad99f-128">ODT</span></span>
- <span data-ttu-id="ad99f-129">PDF</span><span class="sxs-lookup"><span data-stu-id="ad99f-129">PDF</span></span>
- <span data-ttu-id="ad99f-130">PNG</span><span class="sxs-lookup"><span data-stu-id="ad99f-130">PNG</span></span>
- <span data-ttu-id="ad99f-131">PPT</span><span class="sxs-lookup"><span data-stu-id="ad99f-131">PPT</span></span>
- <span data-ttu-id="ad99f-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="ad99f-132">PPTX</span></span>
- <span data-ttu-id="ad99f-133">PS</span><span class="sxs-lookup"><span data-stu-id="ad99f-133">PS</span></span>
- <span data-ttu-id="ad99f-134">QXP</span><span class="sxs-lookup"><span data-stu-id="ad99f-134">QXP</span></span>
- <span data-ttu-id="ad99f-135">RAR</span><span class="sxs-lookup"><span data-stu-id="ad99f-135">RAR</span></span>
- <span data-ttu-id="ad99f-136">RTF</span><span class="sxs-lookup"><span data-stu-id="ad99f-136">RTF</span></span>
- <span data-ttu-id="ad99f-137">SVG</span><span class="sxs-lookup"><span data-stu-id="ad99f-137">SVG</span></span>
- <span data-ttu-id="ad99f-138">TAR</span><span class="sxs-lookup"><span data-stu-id="ad99f-138">TAR</span></span>
- <span data-ttu-id="ad99f-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="ad99f-139">TGZ</span></span>
- <span data-ttu-id="ad99f-140">TXT</span><span class="sxs-lookup"><span data-stu-id="ad99f-140">TXT</span></span>
- <span data-ttu-id="ad99f-141">WMV</span><span class="sxs-lookup"><span data-stu-id="ad99f-141">WMV</span></span>
- <span data-ttu-id="ad99f-142">XLS</span><span class="sxs-lookup"><span data-stu-id="ad99f-142">XLS</span></span>
- <span data-ttu-id="ad99f-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="ad99f-143">XLSX</span></span>
- <span data-ttu-id="ad99f-144">XML</span><span class="sxs-lookup"><span data-stu-id="ad99f-144">XML</span></span>
- <span data-ttu-id="ad99f-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="ad99f-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="ad99f-146">Hlaða upp skrá</span><span class="sxs-lookup"><span data-stu-id="ad99f-146">Upload a file</span></span>

<span data-ttu-id="ad99f-147">Til að hlaða upp skrá í vefsíðuhönnuð í Commerce skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ad99f-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ad99f-148">Í vinstri stýriglugganum velurðu **Margmiðlunarsafn**.</span><span class="sxs-lookup"><span data-stu-id="ad99f-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="ad99f-149">Veldu á skipanastikunni **Hlaða inn \> Hlaða upp margmiðlun**.</span><span class="sxs-lookup"><span data-stu-id="ad99f-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="ad99f-150">Veldu File Explorer eina eða fleiri skrár og veldu síðan **Opna**.</span><span class="sxs-lookup"><span data-stu-id="ad99f-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="ad99f-151">Í valmyndinni **Hlaða upp margmiðlun** slærðu inn titil, lýsingu og lýsigögn leitarorðs eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="ad99f-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="ad99f-152">Til að birta skár beint eftir uppflutning skaltu velja gátreitinn **Birta margmiðlunarefni eftir uppflutning**.</span><span class="sxs-lookup"><span data-stu-id="ad99f-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="ad99f-153">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ad99f-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ad99f-154">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ad99f-154">Additional resources</span></span>

[<span data-ttu-id="ad99f-155">Yfirlit stafrænnar eignastýringar</span><span class="sxs-lookup"><span data-stu-id="ad99f-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="ad99f-156">Hlaða upp myndum</span><span class="sxs-lookup"><span data-stu-id="ad99f-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="ad99f-157">Hlaða upp myndbandi</span><span class="sxs-lookup"><span data-stu-id="ad99f-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="ad99f-158">Skera myndir</span><span class="sxs-lookup"><span data-stu-id="ad99f-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="ad99f-159">Sérstilla áherslupunkta myndar</span><span class="sxs-lookup"><span data-stu-id="ad99f-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="ad99f-160">Hlaða upp og þjóna föstum skrám</span><span class="sxs-lookup"><span data-stu-id="ad99f-160">Upload and serve static files</span></span>](upload-serve-static-files.md)
