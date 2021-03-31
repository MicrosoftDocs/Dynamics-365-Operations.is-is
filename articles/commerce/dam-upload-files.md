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
ms.openlocfilehash: c065aa961cf5c2d6770ae47c63a75953e6d38e00
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222538"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="4d952-103">Hlaða upp skrám öðrum en myndum og myndböndum</span><span class="sxs-lookup"><span data-stu-id="4d952-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4d952-104">Þetta efni lýsir því hvernig hægt er að hlaða upp skrám en myndum og myndböndum í vefsíðuhönnuði í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4d952-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="4d952-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="4d952-105">Overview</span></span>

<span data-ttu-id="4d952-106">Margmiðlunarsafn vefsvæðishönnuðar Commerce styður upphleðslu tvöfaldra eigna annarra en mynda eða myndskeiða.</span><span class="sxs-lookup"><span data-stu-id="4d952-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="4d952-107">Til dæmis gætirðu viljað hlaða inn Microsoft Excel, Microsoft Word, Microsoft PowerPoint eða PDF-skrám.</span><span class="sxs-lookup"><span data-stu-id="4d952-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="4d952-108">Eftirfarandi gerðir skjala eru studdar:</span><span class="sxs-lookup"><span data-stu-id="4d952-108">The following document types are supported:</span></span>
- <span data-ttu-id="4d952-109">7Z</span><span class="sxs-lookup"><span data-stu-id="4d952-109">7Z</span></span>
- <span data-ttu-id="4d952-110">AVI</span><span class="sxs-lookup"><span data-stu-id="4d952-110">AVI</span></span>
- <span data-ttu-id="4d952-111">CS</span><span class="sxs-lookup"><span data-stu-id="4d952-111">CS</span></span>
- <span data-ttu-id="4d952-112">CSS</span><span class="sxs-lookup"><span data-stu-id="4d952-112">CSS</span></span>
- <span data-ttu-id="4d952-113">DOC</span><span class="sxs-lookup"><span data-stu-id="4d952-113">DOC</span></span>
- <span data-ttu-id="4d952-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="4d952-114">DOCX</span></span>
- <span data-ttu-id="4d952-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="4d952-115">EPUB</span></span>
- <span data-ttu-id="4d952-116">GIF</span><span class="sxs-lookup"><span data-stu-id="4d952-116">GIF</span></span>
- <span data-ttu-id="4d952-117">INDD</span><span class="sxs-lookup"><span data-stu-id="4d952-117">INDD</span></span>
- <span data-ttu-id="4d952-118">JAR</span><span class="sxs-lookup"><span data-stu-id="4d952-118">JAR</span></span>
- <span data-ttu-id="4d952-119">JPG</span><span class="sxs-lookup"><span data-stu-id="4d952-119">JPG</span></span>
- <span data-ttu-id="4d952-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="4d952-120">JPEG</span></span>
- <span data-ttu-id="4d952-121">JS</span><span class="sxs-lookup"><span data-stu-id="4d952-121">JS</span></span>
- <span data-ttu-id="4d952-122">MP3</span><span class="sxs-lookup"><span data-stu-id="4d952-122">MP3</span></span>
- <span data-ttu-id="4d952-123">MP4</span><span class="sxs-lookup"><span data-stu-id="4d952-123">MP4</span></span>
- <span data-ttu-id="4d952-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="4d952-124">MPEG</span></span>
- <span data-ttu-id="4d952-125">MPG</span><span class="sxs-lookup"><span data-stu-id="4d952-125">MPG</span></span>
- <span data-ttu-id="4d952-126">ODP</span><span class="sxs-lookup"><span data-stu-id="4d952-126">ODP</span></span>
- <span data-ttu-id="4d952-127">ODS</span><span class="sxs-lookup"><span data-stu-id="4d952-127">ODS</span></span>
- <span data-ttu-id="4d952-128">ODT</span><span class="sxs-lookup"><span data-stu-id="4d952-128">ODT</span></span>
- <span data-ttu-id="4d952-129">PDF</span><span class="sxs-lookup"><span data-stu-id="4d952-129">PDF</span></span>
- <span data-ttu-id="4d952-130">PNG</span><span class="sxs-lookup"><span data-stu-id="4d952-130">PNG</span></span>
- <span data-ttu-id="4d952-131">PPT</span><span class="sxs-lookup"><span data-stu-id="4d952-131">PPT</span></span>
- <span data-ttu-id="4d952-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="4d952-132">PPTX</span></span>
- <span data-ttu-id="4d952-133">PS</span><span class="sxs-lookup"><span data-stu-id="4d952-133">PS</span></span>
- <span data-ttu-id="4d952-134">QXP</span><span class="sxs-lookup"><span data-stu-id="4d952-134">QXP</span></span>
- <span data-ttu-id="4d952-135">RAR</span><span class="sxs-lookup"><span data-stu-id="4d952-135">RAR</span></span>
- <span data-ttu-id="4d952-136">RTF</span><span class="sxs-lookup"><span data-stu-id="4d952-136">RTF</span></span>
- <span data-ttu-id="4d952-137">SVG</span><span class="sxs-lookup"><span data-stu-id="4d952-137">SVG</span></span>
- <span data-ttu-id="4d952-138">TAR</span><span class="sxs-lookup"><span data-stu-id="4d952-138">TAR</span></span>
- <span data-ttu-id="4d952-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="4d952-139">TGZ</span></span>
- <span data-ttu-id="4d952-140">TXT</span><span class="sxs-lookup"><span data-stu-id="4d952-140">TXT</span></span>
- <span data-ttu-id="4d952-141">WMV</span><span class="sxs-lookup"><span data-stu-id="4d952-141">WMV</span></span>
- <span data-ttu-id="4d952-142">XLS</span><span class="sxs-lookup"><span data-stu-id="4d952-142">XLS</span></span>
- <span data-ttu-id="4d952-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="4d952-143">XLSX</span></span>
- <span data-ttu-id="4d952-144">XML</span><span class="sxs-lookup"><span data-stu-id="4d952-144">XML</span></span>
- <span data-ttu-id="4d952-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="4d952-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="4d952-146">Hlaða upp skrá</span><span class="sxs-lookup"><span data-stu-id="4d952-146">Upload a file</span></span>

<span data-ttu-id="4d952-147">Til að hlaða upp skrá í vefsíðuhönnuð í Commerce skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="4d952-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="4d952-148">Í vinstri stýriglugganum velurðu **Margmiðlunarsafn**.</span><span class="sxs-lookup"><span data-stu-id="4d952-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="4d952-149">Veldu á skipanastikunni **Hlaða inn \> Hlaða upp margmiðlun**.</span><span class="sxs-lookup"><span data-stu-id="4d952-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="4d952-150">Veldu File Explorer eina eða fleiri skrár og veldu síðan **Opna**.</span><span class="sxs-lookup"><span data-stu-id="4d952-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="4d952-151">Í valmyndinni **Hlaða upp margmiðlun** slærðu inn titil, lýsingu og lýsigögn leitarorðs eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="4d952-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="4d952-152">Til að birta skár beint eftir uppflutning skaltu velja gátreitinn **Birta margmiðlunarefni eftir uppflutning**.</span><span class="sxs-lookup"><span data-stu-id="4d952-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="4d952-153">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="4d952-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d952-154">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4d952-154">Additional resources</span></span>

[<span data-ttu-id="4d952-155">Yfirlit stafrænnar eignastýringar</span><span class="sxs-lookup"><span data-stu-id="4d952-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="4d952-156">Hlaða upp myndum</span><span class="sxs-lookup"><span data-stu-id="4d952-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="4d952-157">Hlaða upp myndbandi</span><span class="sxs-lookup"><span data-stu-id="4d952-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="4d952-158">Skera myndir</span><span class="sxs-lookup"><span data-stu-id="4d952-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="4d952-159">Sérstilla áherslupunkta myndar</span><span class="sxs-lookup"><span data-stu-id="4d952-159">Customize image focal points</span></span>](dam-custom-focal-point.md)

[<span data-ttu-id="4d952-160">Hlaða upp og þjóna föstum skrám</span><span class="sxs-lookup"><span data-stu-id="4d952-160">Upload and serve static files</span></span>](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]