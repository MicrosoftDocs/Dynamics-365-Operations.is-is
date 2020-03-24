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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: fc0490e3532dcbb9c1e91101009b2d4605315416
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/03/2020
ms.locfileid: "3097030"
---
# <a name="upload-files-other-than-images-and-videos"></a><span data-ttu-id="c3fd8-103">Hlaða upp öðrum skrám en myndum og myndskeiðum</span><span class="sxs-lookup"><span data-stu-id="c3fd8-103">Upload files other than images and videos</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c3fd8-104">Þetta efni lýsir því hvernig hægt er að hlaða upp skrám en myndum og myndböndum í vefsíðuhönnuði í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c3fd8-104">This topic describes how to upload files other than images and videos in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="c3fd8-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="c3fd8-105">Overview</span></span>

<span data-ttu-id="c3fd8-106">Margmiðlunarsafn vefsvæðishönnuðar Commerce styður upphleðslu tvöfaldra eigna annarra en mynda eða myndskeiða.</span><span class="sxs-lookup"><span data-stu-id="c3fd8-106">The Commerce site builder Media Library supports the uploading of binary assets other than images or videos.</span></span> <span data-ttu-id="c3fd8-107">Til dæmis gætirðu viljað hlaða inn Microsoft Excel, Microsoft Word, Microsoft PowerPoint eða PDF-skrám.</span><span class="sxs-lookup"><span data-stu-id="c3fd8-107">For example, you might want to upload Microsoft Excel, Microsoft Word, Microsoft PowerPoint, or PDF files.</span></span>

<span data-ttu-id="c3fd8-108">Eftirfarandi gerðir skjala eru studdar:</span><span class="sxs-lookup"><span data-stu-id="c3fd8-108">The following document types are supported:</span></span>
- <span data-ttu-id="c3fd8-109">7Z</span><span class="sxs-lookup"><span data-stu-id="c3fd8-109">7Z</span></span>
- <span data-ttu-id="c3fd8-110">AVI</span><span class="sxs-lookup"><span data-stu-id="c3fd8-110">AVI</span></span>
- <span data-ttu-id="c3fd8-111">CS</span><span class="sxs-lookup"><span data-stu-id="c3fd8-111">CS</span></span>
- <span data-ttu-id="c3fd8-112">CSS</span><span class="sxs-lookup"><span data-stu-id="c3fd8-112">CSS</span></span>
- <span data-ttu-id="c3fd8-113">DOC</span><span class="sxs-lookup"><span data-stu-id="c3fd8-113">DOC</span></span>
- <span data-ttu-id="c3fd8-114">DOCX</span><span class="sxs-lookup"><span data-stu-id="c3fd8-114">DOCX</span></span>
- <span data-ttu-id="c3fd8-115">EPUB</span><span class="sxs-lookup"><span data-stu-id="c3fd8-115">EPUB</span></span>
- <span data-ttu-id="c3fd8-116">GIF</span><span class="sxs-lookup"><span data-stu-id="c3fd8-116">GIF</span></span>
- <span data-ttu-id="c3fd8-117">INDD</span><span class="sxs-lookup"><span data-stu-id="c3fd8-117">INDD</span></span>
- <span data-ttu-id="c3fd8-118">JAR</span><span class="sxs-lookup"><span data-stu-id="c3fd8-118">JAR</span></span>
- <span data-ttu-id="c3fd8-119">JPG</span><span class="sxs-lookup"><span data-stu-id="c3fd8-119">JPG</span></span>
- <span data-ttu-id="c3fd8-120">JPEG</span><span class="sxs-lookup"><span data-stu-id="c3fd8-120">JPEG</span></span>
- <span data-ttu-id="c3fd8-121">JS</span><span class="sxs-lookup"><span data-stu-id="c3fd8-121">JS</span></span>
- <span data-ttu-id="c3fd8-122">MP3</span><span class="sxs-lookup"><span data-stu-id="c3fd8-122">MP3</span></span>
- <span data-ttu-id="c3fd8-123">MP4</span><span class="sxs-lookup"><span data-stu-id="c3fd8-123">MP4</span></span>
- <span data-ttu-id="c3fd8-124">MPEG</span><span class="sxs-lookup"><span data-stu-id="c3fd8-124">MPEG</span></span>
- <span data-ttu-id="c3fd8-125">MPG</span><span class="sxs-lookup"><span data-stu-id="c3fd8-125">MPG</span></span>
- <span data-ttu-id="c3fd8-126">ODP</span><span class="sxs-lookup"><span data-stu-id="c3fd8-126">ODP</span></span>
- <span data-ttu-id="c3fd8-127">ODS</span><span class="sxs-lookup"><span data-stu-id="c3fd8-127">ODS</span></span>
- <span data-ttu-id="c3fd8-128">ODT</span><span class="sxs-lookup"><span data-stu-id="c3fd8-128">ODT</span></span>
- <span data-ttu-id="c3fd8-129">PDF</span><span class="sxs-lookup"><span data-stu-id="c3fd8-129">PDF</span></span>
- <span data-ttu-id="c3fd8-130">PNG</span><span class="sxs-lookup"><span data-stu-id="c3fd8-130">PNG</span></span>
- <span data-ttu-id="c3fd8-131">PPT</span><span class="sxs-lookup"><span data-stu-id="c3fd8-131">PPT</span></span>
- <span data-ttu-id="c3fd8-132">PPTX</span><span class="sxs-lookup"><span data-stu-id="c3fd8-132">PPTX</span></span>
- <span data-ttu-id="c3fd8-133">PS</span><span class="sxs-lookup"><span data-stu-id="c3fd8-133">PS</span></span>
- <span data-ttu-id="c3fd8-134">QXP</span><span class="sxs-lookup"><span data-stu-id="c3fd8-134">QXP</span></span>
- <span data-ttu-id="c3fd8-135">RAR</span><span class="sxs-lookup"><span data-stu-id="c3fd8-135">RAR</span></span>
- <span data-ttu-id="c3fd8-136">RTF</span><span class="sxs-lookup"><span data-stu-id="c3fd8-136">RTF</span></span>
- <span data-ttu-id="c3fd8-137">SVG</span><span class="sxs-lookup"><span data-stu-id="c3fd8-137">SVG</span></span>
- <span data-ttu-id="c3fd8-138">TAR</span><span class="sxs-lookup"><span data-stu-id="c3fd8-138">TAR</span></span>
- <span data-ttu-id="c3fd8-139">TGZ</span><span class="sxs-lookup"><span data-stu-id="c3fd8-139">TGZ</span></span>
- <span data-ttu-id="c3fd8-140">TXT</span><span class="sxs-lookup"><span data-stu-id="c3fd8-140">TXT</span></span>
- <span data-ttu-id="c3fd8-141">WMV</span><span class="sxs-lookup"><span data-stu-id="c3fd8-141">WMV</span></span>
- <span data-ttu-id="c3fd8-142">XLS</span><span class="sxs-lookup"><span data-stu-id="c3fd8-142">XLS</span></span>
- <span data-ttu-id="c3fd8-143">XLSX</span><span class="sxs-lookup"><span data-stu-id="c3fd8-143">XLSX</span></span>
- <span data-ttu-id="c3fd8-144">XML</span><span class="sxs-lookup"><span data-stu-id="c3fd8-144">XML</span></span>
- <span data-ttu-id="c3fd8-145">ZIP</span><span class="sxs-lookup"><span data-stu-id="c3fd8-145">ZIP</span></span>

## <a name="upload-a-file"></a><span data-ttu-id="c3fd8-146">Hlaða upp skrá</span><span class="sxs-lookup"><span data-stu-id="c3fd8-146">Upload a file</span></span>

<span data-ttu-id="c3fd8-147">Til að hlaða upp skrá í vefsíðuhönnuð í Commerce skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c3fd8-147">To upload a file to Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="c3fd8-148">Í vinstri stýriglugganum velurðu **Margmiðlunarsafn**.</span><span class="sxs-lookup"><span data-stu-id="c3fd8-148">In the left navigation pane, select **Media Library**.</span></span>
1. <span data-ttu-id="c3fd8-149">Veldu á skipanastikunni **Hlaða inn \> Hlaða upp margmiðlun**.</span><span class="sxs-lookup"><span data-stu-id="c3fd8-149">On the command bar, select **Upload \> Upload Media Items**.</span></span>
1. <span data-ttu-id="c3fd8-150">Veldu File Explorer eina eða fleiri skrár og veldu síðan **Opna**.</span><span class="sxs-lookup"><span data-stu-id="c3fd8-150">In File Explorer, select one or more files and then select **Open**.</span></span>
1. <span data-ttu-id="c3fd8-151">Í valmyndinni **Hlaða upp margmiðlun** slærðu inn titil, lýsingu og lýsigögn leitarorðs eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="c3fd8-151">In the **Upload Media Item** dialog box, enter title, description, and keyword metadata as needed.</span></span>
1. <span data-ttu-id="c3fd8-152">Til að birta skár beint eftir uppflutning skaltu velja gátreitinn **Birta margmiðlunarefni eftir uppflutning**.</span><span class="sxs-lookup"><span data-stu-id="c3fd8-152">To publish the file(s) immediately after upload, select the **Publish media items after upload** check box.</span></span>
1. <span data-ttu-id="c3fd8-153">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c3fd8-153">Select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3fd8-154">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c3fd8-154">Additional resources</span></span>

[<span data-ttu-id="c3fd8-155">Yfirlit stafrænnar eignastýringar</span><span class="sxs-lookup"><span data-stu-id="c3fd8-155">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="c3fd8-156">Hlaða upp myndum</span><span class="sxs-lookup"><span data-stu-id="c3fd8-156">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="c3fd8-157">Hlaða upp myndskeiði</span><span class="sxs-lookup"><span data-stu-id="c3fd8-157">Upload video</span></span>](dam-upload-video.md)

[<span data-ttu-id="c3fd8-158">Skera myndir</span><span class="sxs-lookup"><span data-stu-id="c3fd8-158">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="c3fd8-159">Sérsníða þungamiðju myndar</span><span class="sxs-lookup"><span data-stu-id="c3fd8-159">Customize image focal points</span></span>](dam-custom-focal-point.md)
