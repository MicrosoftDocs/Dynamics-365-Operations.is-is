---
title: Eiginleikaeining
description: Þetta efni fjallar um eiginleikaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785285"
---
# <a name="feature-module"></a><span data-ttu-id="05430-103">Eiginleikaeining</span><span class="sxs-lookup"><span data-stu-id="05430-103">Feature module</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="05430-104">Þetta efni fjallar um eiginleikaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="05430-104">This topic covers feature modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="05430-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="05430-105">Overview</span></span>

<span data-ttu-id="05430-106">Eiginleikaeining er notuð til að markaðssetja vörur eða kynningar með blöndu af myndum og texta.</span><span class="sxs-lookup"><span data-stu-id="05430-106">A feature module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="05430-107">Til dæmis getur smásali bætt eiginleikaeiningunni við upplýsingasíðu vöru til að varpa ljósi á eiginleika vörunnar.</span><span class="sxs-lookup"><span data-stu-id="05430-107">For example, a retailer can add a feature module to a product details page to highlight the features of the product.</span></span>

<span data-ttu-id="05430-108">Eiginleikaeining er knúin áfram af gögnum frá efnisstýringarkerfinu (CMS).</span><span class="sxs-lookup"><span data-stu-id="05430-108">A feature module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="05430-109">Þetta er sjálfstæð eining sem er ekki háð öðrum einingum á síðunni.</span><span class="sxs-lookup"><span data-stu-id="05430-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="05430-110">Hægt er að setja eiginleikaeiningar á hvaða síðu sem er þar sem smásali vill markaðssetja eða auglýsa eitthvað (til dæmis vörur, útsölu eða eiginleika).</span><span class="sxs-lookup"><span data-stu-id="05430-110">A feature module can be put on any site page where a retailer wants to market or promote something (for example products, sales, or features).</span></span>

## <a name="examples-of-feature-modules-in-e-commerce"></a><span data-ttu-id="05430-111">Dæmi um eiginleikaeiningar í rafrænum viðskiptum</span><span class="sxs-lookup"><span data-stu-id="05430-111">Examples of feature modules in e-Commerce</span></span>

<span data-ttu-id="05430-112">Eiginleikaeiningu má nota á eftirfarandi síðum:</span><span class="sxs-lookup"><span data-stu-id="05430-112">A feature module can used on the following pages:</span></span>

- <span data-ttu-id="05430-113">Upplýsingar um vöru til að sýna fram á eiginleika vöru</span><span class="sxs-lookup"><span data-stu-id="05430-113">A product details page, to showcase product features</span></span>
- <span data-ttu-id="05430-114">Heimasíðan, til að kynna vörur</span><span class="sxs-lookup"><span data-stu-id="05430-114">The home page, to promote products</span></span>
- <span data-ttu-id="05430-115">Flokkasíða, til að auðkenna vöruflokk</span><span class="sxs-lookup"><span data-stu-id="05430-115">A category page, to highlight a category of products</span></span>

## <a name="feature-module-properties"></a><span data-ttu-id="05430-116">Eiginleikar eiginleikaeiningar</span><span class="sxs-lookup"><span data-stu-id="05430-116">Feature module properties</span></span>

| <span data-ttu-id="05430-117">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="05430-117">Property name</span></span>     | <span data-ttu-id="05430-118">Gildi</span><span class="sxs-lookup"><span data-stu-id="05430-118">Values</span></span> | <span data-ttu-id="05430-119">Lýsing</span><span class="sxs-lookup"><span data-stu-id="05430-119">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="05430-120">Mynd</span><span class="sxs-lookup"><span data-stu-id="05430-120">Image</span></span>             | <span data-ttu-id="05430-121">Myndaskrá</span><span class="sxs-lookup"><span data-stu-id="05430-121">Image file</span></span> | <span data-ttu-id="05430-122">Hægt er að nota mynd til að markaðssetja vöruna eða auglýsa.</span><span class="sxs-lookup"><span data-stu-id="05430-122">An image can be used to market the product or promotion.</span></span> <span data-ttu-id="05430-123">Hægt er að hlaða mynd inn í myndasafnið eða nota núverandi mynd.</span><span class="sxs-lookup"><span data-stu-id="05430-123">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="05430-124">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="05430-124">Heading</span></span>           | <span data-ttu-id="05430-125">Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**)</span><span class="sxs-lookup"><span data-stu-id="05430-125">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="05430-126">Sérhver eiginleikaeining getur haft fyrirsögn.</span><span class="sxs-lookup"><span data-stu-id="05430-126">Every feature module can have a heading.</span></span> <span data-ttu-id="05430-127">Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina.</span><span class="sxs-lookup"><span data-stu-id="05430-127">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="05430-128">Hins vegar er hægt að breyta merkinu til að uppfylla kröfur um aðgengi.</span><span class="sxs-lookup"><span data-stu-id="05430-128">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="05430-129">Efnisgrein</span><span class="sxs-lookup"><span data-stu-id="05430-129">Paragraph</span></span>         | <span data-ttu-id="05430-130">Texti efnisgreinar</span><span class="sxs-lookup"><span data-stu-id="05430-130">Paragraph text</span></span> | <span data-ttu-id="05430-131">Eiginleikaeiningar styðja málsgreinatexta með ríku textasniði.</span><span class="sxs-lookup"><span data-stu-id="05430-131">Feature modules support paragraph text in rich text format.</span></span> <span data-ttu-id="05430-132">Stuðningur er við nokkra grunntextaeiginleika, eins og feitletrun, undirstrikun og skáletrun texta og tengla.</span><span class="sxs-lookup"><span data-stu-id="05430-132">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="05430-133">Sumum af þessum eiginleikum er hægt að hnekkja með síðuþema sem er beitt á eininguna.</span><span class="sxs-lookup"><span data-stu-id="05430-133">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="05430-134">Tengill</span><span class="sxs-lookup"><span data-stu-id="05430-134">Link</span></span>              | <span data-ttu-id="05430-135">Tenglatexti, vefslóð tengils, ARIA-merki (Accessible Rich Internet Applications) og **Opnaðu hlekk í nýjum flipa**</span><span class="sxs-lookup"><span data-stu-id="05430-135">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="05430-136">Eiginleikaeiningar styðja einn eða fleiri „kalla til aðgerða“ tengla.</span><span class="sxs-lookup"><span data-stu-id="05430-136">Feature modules support one or more "call to action" links.</span></span> <span data-ttu-id="05430-137">Ef tengli er bætt við þarf tenglatexta, vefslóð og ARIA-merki.</span><span class="sxs-lookup"><span data-stu-id="05430-137">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="05430-138">ARIA-merki ættu að vera lýsandi til að uppfylla kröfur um aðgengi.</span><span class="sxs-lookup"><span data-stu-id="05430-138">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="05430-139">Hægt er að stilla tengla þannig að þeir séu opnaðir á nýjum flipa.</span><span class="sxs-lookup"><span data-stu-id="05430-139">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="05430-140">Staðsetning myndar</span><span class="sxs-lookup"><span data-stu-id="05430-140">Image placement</span></span>   | <span data-ttu-id="05430-141">**Hægri**, **Vinstri**, **Efst** eða **Neðst**</span><span class="sxs-lookup"><span data-stu-id="05430-141">**Right**, **Left**, **Top**, or **Bottom**</span></span> | <span data-ttu-id="05430-142">Þessi eiginleiki skilgreinir staðsetningu myndarinnar miðað við textann.</span><span class="sxs-lookup"><span data-stu-id="05430-142">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="05430-143">Til dæmis, ef **hægri** er valið birtist myndin hægra megin við textann.</span><span class="sxs-lookup"><span data-stu-id="05430-143">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="05430-144">Dálkstærð myndar</span><span class="sxs-lookup"><span data-stu-id="05430-144">Image column size</span></span> | <span data-ttu-id="05430-145">Gildi frá **1** til og með **12**</span><span class="sxs-lookup"><span data-stu-id="05430-145">A value from **1** through **12**</span></span> | <span data-ttu-id="05430-146">Þessi eiginleiki skilgreinir stærð myndarinnar miðað við textann.</span><span class="sxs-lookup"><span data-stu-id="05430-146">This property defines the size of the image relative to the text.</span></span> <span data-ttu-id="05430-147">Stærð er gefin upp sem fjöldi dálka á síðunni.</span><span class="sxs-lookup"><span data-stu-id="05430-147">Size is expressed as a number of columns on the page.</span></span> <span data-ttu-id="05430-148">Það eru 12 dálkar á síðunni.</span><span class="sxs-lookup"><span data-stu-id="05430-148">There are 12 columns on a page.</span></span> <span data-ttu-id="05430-149">Sjálfgefið er að myndin og textinn hafi sömu stærð (sex dálkar hver).</span><span class="sxs-lookup"><span data-stu-id="05430-149">By default, the image and text have equal size (six columns each).</span></span> <span data-ttu-id="05430-150">Hins vegar er hægt að breyta stærðinni eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="05430-150">However, the size can be adjusted as required.</span></span> |

## <a name="add-a-feature-module-to-a-new-page"></a><span data-ttu-id="05430-151">Bæta eiginleikaeiningu við nýja síðu</span><span class="sxs-lookup"><span data-stu-id="05430-151">Add a feature module to a new page</span></span> 

<span data-ttu-id="05430-152">Fylgdu þessum skrefum til að bæta eiginleikaeiningu við nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="05430-152">To add a feature module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="05430-153">Farðu í **Sniðmát** og búðu til síðusniðmát sem heitir **eiginleikasniðmát**.</span><span class="sxs-lookup"><span data-stu-id="05430-153">Go to **Templates**, and create a page template that is named **feature template**.</span></span>
1. <span data-ttu-id="05430-154">Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við eiginleikaeiningu.</span><span class="sxs-lookup"><span data-stu-id="05430-154">In the **Main** slot of the default page, add a feature module.</span></span>
1. <span data-ttu-id="05430-155">Skráðu brotið út í sniðmátinu og birtu það.</span><span class="sxs-lookup"><span data-stu-id="05430-155">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="05430-156">Notaðu eiginleikasniðmátið sem þú bjóst til til að búa til síðu sem heitir **eiginleikasíða**.</span><span class="sxs-lookup"><span data-stu-id="05430-156">Use the feature template that you just created to create a page that is named **feature page**.</span></span>
1. <span data-ttu-id="05430-157">Í hólfinu **Aðal** á sjálfgefnu síðunni velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="05430-157">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="05430-158">Í vlmyndinni **Bæta við einingu** undir **Velja einingar** velurðu eiginleikaeiningu og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="05430-158">In the **Add Module** dialog box, under **Select Modules**, select a feature module, and then select **OK**.</span></span>
1. <span data-ttu-id="05430-159">Veldu eiginleikaeininguna í útlínutrénu til vinstri.</span><span class="sxs-lookup"><span data-stu-id="05430-159">In the outline tree on the left, select the feature module.</span></span>
1. <span data-ttu-id="05430-160">Í eiginleikaglugganum til hægri velurðu **Bæta við mynd**.</span><span class="sxs-lookup"><span data-stu-id="05430-160">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="05430-161">Veldu þá annaðhvort núverandi mynd eða hladdu upp nýrri mynd.</span><span class="sxs-lookup"><span data-stu-id="05430-161">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="05430-162">Veldu **Fyrirsögn**.</span><span class="sxs-lookup"><span data-stu-id="05430-162">Select **Heading**.</span></span>
1. <span data-ttu-id="05430-163">Í valmyndinni **Fyrirsögn** bætirðu við fyrirsagnartexta, velur hausstig og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="05430-163">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="05430-164">Undir **Sniðinn texti** bætirðu við texta eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="05430-164">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="05430-165">Veldu **Bæta við aðgerðartengli**.</span><span class="sxs-lookup"><span data-stu-id="05430-165">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="05430-166">Í valmyndinni **Aðgerðartengill** bætirðu við texta, slóð og ARIA-merki fyrir tengilinn og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="05430-166">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="05430-167">Vistaðu síðuna og forskoðaðu breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="05430-167">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="05430-168">Athuga á síðunni og birtu hana.</span><span class="sxs-lookup"><span data-stu-id="05430-168">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="05430-169">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="05430-169">Additional resources</span></span>

[<span data-ttu-id="05430-170">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="05430-170">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="05430-171">Viðvörunareining</span><span class="sxs-lookup"><span data-stu-id="05430-171">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="05430-172">Myndaræmueining</span><span class="sxs-lookup"><span data-stu-id="05430-172">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="05430-173">Eining með fjölbreyttu efni</span><span class="sxs-lookup"><span data-stu-id="05430-173">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="05430-174">Staðsetningareining efnis</span><span class="sxs-lookup"><span data-stu-id="05430-174">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="05430-175">Hetjueining</span><span class="sxs-lookup"><span data-stu-id="05430-175">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="05430-176">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="05430-176">Video player module</span></span>](add-video-player.md)
