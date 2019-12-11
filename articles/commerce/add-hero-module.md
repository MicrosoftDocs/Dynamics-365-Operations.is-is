---
title: Hetjueining
description: Þetta efni fjallar um hetjueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785393"
---
# <a name="hero-module"></a><span data-ttu-id="b9020-103">Hetjueining</span><span class="sxs-lookup"><span data-stu-id="b9020-103">Hero module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b9020-104">Þetta efni fjallar um hetjueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b9020-104">This topic covers hero modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b9020-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="b9020-105">Overview</span></span>

<span data-ttu-id="b9020-106">Hetjueining er notuð til að markaðssetja vörur eða kynningar með blöndu af myndum og texta.</span><span class="sxs-lookup"><span data-stu-id="b9020-106">A hero module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="b9020-107">Til dæmis getur smásali bætt hetjueiningu á heimasíðu svæðis fyrir rafræn viðskipti til að kynna nýja vöru og vekja athygli viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="b9020-107">For example, a retailer can add a hero module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="b9020-108">Hetjueining er knúin áfram af gögnum frá efnisstýringarkerfinu (CMS).</span><span class="sxs-lookup"><span data-stu-id="b9020-108">A hero module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="b9020-109">Þetta er sjálfstæð eining sem er ekki háð öðrum einingum á síðunni.</span><span class="sxs-lookup"><span data-stu-id="b9020-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="b9020-110">Hægt er að setja hetjueiningar á hvaða síðu sem er þar sem smásali vill markaðssetja eða auglýsa eitthvað (til dæmis vörur, útsölu eða eiginleika).</span><span class="sxs-lookup"><span data-stu-id="b9020-110">A hero module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-hero-module-in-e-commerce"></a><span data-ttu-id="b9020-111">Dæmi um hetjueiningu í rafrænum viðskiptum</span><span class="sxs-lookup"><span data-stu-id="b9020-111">Examples of hero module in e-Commerce</span></span>

- <span data-ttu-id="b9020-112">Hægt er að nota hetjueiningu á heimasíðu svæðis fyrir rafræn viðskipti til að varpa ljósi á kynningar og nýjar vörur.</span><span class="sxs-lookup"><span data-stu-id="b9020-112">A hero module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="b9020-113">Hægt er að nota hetjueiningu á upplýsingasíðu vöru til að sýna upplýsingar um vöru.</span><span class="sxs-lookup"><span data-stu-id="b9020-113">A hero module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="b9020-114">Hægt er að setja margar hetjueiningar í myndaræmueiningu til að varpa ljósi á margar vörur eða kynningar.</span><span class="sxs-lookup"><span data-stu-id="b9020-114">Multiple hero modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="hero-module-properties"></a><span data-ttu-id="b9020-115">Eiginleikar hetjueiningar</span><span class="sxs-lookup"><span data-stu-id="b9020-115">Hero module properties</span></span>

| <span data-ttu-id="b9020-116">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="b9020-116">Property name</span></span>  | <span data-ttu-id="b9020-117">Gildi</span><span class="sxs-lookup"><span data-stu-id="b9020-117">Values</span></span> | <span data-ttu-id="b9020-118">Lýsing</span><span class="sxs-lookup"><span data-stu-id="b9020-118">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="b9020-119">Mynd</span><span class="sxs-lookup"><span data-stu-id="b9020-119">Image</span></span>          | <span data-ttu-id="b9020-120">Myndaskrá</span><span class="sxs-lookup"><span data-stu-id="b9020-120">Image file</span></span> | <span data-ttu-id="b9020-121">Hægt er að nota mynd til að sýna vöruna eða auglýsa.</span><span class="sxs-lookup"><span data-stu-id="b9020-121">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="b9020-122">Hægt er að hlaða mynd inn í myndasafnið eða nota núverandi mynd.</span><span class="sxs-lookup"><span data-stu-id="b9020-122">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="b9020-123">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="b9020-123">Heading</span></span>        | <span data-ttu-id="b9020-124">Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**)</span><span class="sxs-lookup"><span data-stu-id="b9020-124">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="b9020-125">Sérhver hetjueining getur haft fyrirsögn.</span><span class="sxs-lookup"><span data-stu-id="b9020-125">Every hero module can have a heading.</span></span> <span data-ttu-id="b9020-126">Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina.</span><span class="sxs-lookup"><span data-stu-id="b9020-126">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="b9020-127">Hins vegar er hægt að breyta merkinu til að uppfylla kröfur um aðgengi.</span><span class="sxs-lookup"><span data-stu-id="b9020-127">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="b9020-128">Efnisgrein</span><span class="sxs-lookup"><span data-stu-id="b9020-128">Paragraph</span></span>      | <span data-ttu-id="b9020-129">Texti efnisgreinar</span><span class="sxs-lookup"><span data-stu-id="b9020-129">Paragraph text</span></span> | <span data-ttu-id="b9020-130">Hetjueiningar styðja málsgreinatexta með ríku textasniði.</span><span class="sxs-lookup"><span data-stu-id="b9020-130">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="b9020-131">Stuðningur er við nokkra grunntextaeiginleika, eins og feitletrun, undirstrikun og skáletrun texta og tengla.</span><span class="sxs-lookup"><span data-stu-id="b9020-131">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="b9020-132">Sumum af þessum eiginleikum er hægt að hnekkja með síðuþema sem er beitt á eininguna.</span><span class="sxs-lookup"><span data-stu-id="b9020-132">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="b9020-133">Tengill</span><span class="sxs-lookup"><span data-stu-id="b9020-133">Link</span></span>           | <span data-ttu-id="b9020-134">Tenglatexti, vefslóð tengils, ARIA-merki (Accessible Rich Internet Applications) og **Opnaðu hlekk í nýjum flipa**</span><span class="sxs-lookup"><span data-stu-id="b9020-134">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="b9020-135">Hetjueiningar styðja einn eða fleiri „kalla til aðgerða“ tengla.</span><span class="sxs-lookup"><span data-stu-id="b9020-135">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="b9020-136">Ef tengli er bætt við þarf tenglatexta, vefslóð og ARIA-merki.</span><span class="sxs-lookup"><span data-stu-id="b9020-136">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="b9020-137">ARIA-merki ættu að vera lýsandi til að uppfylla kröfur um aðgengi.</span><span class="sxs-lookup"><span data-stu-id="b9020-137">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="b9020-138">Hægt er að stilla tengla þannig að þeir séu opnaðir á nýjum flipa.</span><span class="sxs-lookup"><span data-stu-id="b9020-138">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="b9020-139">Staðsetning texta</span><span class="sxs-lookup"><span data-stu-id="b9020-139">Text placement</span></span> | <span data-ttu-id="b9020-140">**Efst til vinstri**, **Efst til hægri**, **Efsta fyrir miðju**, **Neðst til vinstri**, **Neðst til hægri**, **Neðst fyrir miðju**, **Miðja vinstri**, **Miðja hægri** eða **Miðja fyrir miðju**</span><span class="sxs-lookup"><span data-stu-id="b9020-140">**Top Left**, **Top Right**, **Top Center**, **Bottom Left**, **Bottom Right**, **Bottom Center**, **Center Left**, **Center Right**, or **Center Center**</span></span> | <span data-ttu-id="b9020-141">Þessi eiginleiki skilgreinir staðsetningu myndarinnar miðað við textann.</span><span class="sxs-lookup"><span data-stu-id="b9020-141">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="b9020-142">Til dæmis, ef **hægri** er valið birtist myndin hægra megin við textann.</span><span class="sxs-lookup"><span data-stu-id="b9020-142">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="b9020-143">Aðalefni texta</span><span class="sxs-lookup"><span data-stu-id="b9020-143">Text theme</span></span>     | <span data-ttu-id="b9020-144">**Ljóst** eða **Dökkt**</span><span class="sxs-lookup"><span data-stu-id="b9020-144">**Light** or **Dark**</span></span> | <span data-ttu-id="b9020-145">Hægt er að skilgreina litasamsetningu fyrir textann, byggt á bakgrunnsmyndinni.</span><span class="sxs-lookup"><span data-stu-id="b9020-145">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="b9020-146">Til dæmis, ef myndin er með dökkan bakgrunn, er hægt að beita léttu þema til að gera textann sýnilegri og til að mæta andstæða litastigshlutfalla í aðgengisskyni.</span><span class="sxs-lookup"><span data-stu-id="b9020-146">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> |
| <span data-ttu-id="b9020-147">Stigull</span><span class="sxs-lookup"><span data-stu-id="b9020-147">Gradient</span></span>       | <span data-ttu-id="b9020-148">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="b9020-148">**True** or **False**</span></span> | <span data-ttu-id="b9020-149">Hægt er að beita stigul á myndina til að uppfylla litaréttarhlutföll í aðgengisskyni.</span><span class="sxs-lookup"><span data-stu-id="b9020-149">A gradient can be applied to the image to meet color contrast ratios for accessibility purposes.</span></span> |

## <a name="add-a-hero-module-to-a-new-page"></a><span data-ttu-id="b9020-150">Bæta hetjueiningu við nýja síðu</span><span class="sxs-lookup"><span data-stu-id="b9020-150">Add a hero module to a new page</span></span>

<span data-ttu-id="b9020-151">Fylgdu þessum skrefum til að bæta hetjueiningu við nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="b9020-151">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="b9020-152">Farðu í **Sniðmát** og búðu til síðusniðmát sem heitir **hetjusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="b9020-152">Go to **Templates**, and create a page template that is named **hero template**.</span></span>
1. <span data-ttu-id="b9020-153">Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við hetjueiningu.</span><span class="sxs-lookup"><span data-stu-id="b9020-153">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="b9020-154">Skráðu brotið út í sniðmátinu og birtu það.</span><span class="sxs-lookup"><span data-stu-id="b9020-154">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="b9020-155">Notaðu hetjusniðmátið sem þú bjóst til að búa til síðu sem heitir **hetjusíða**.</span><span class="sxs-lookup"><span data-stu-id="b9020-155">Use the hero template that you just created to create a page that is named **hero page**.</span></span>
1. <span data-ttu-id="b9020-156">Í hólfinu **Aðal** á sjálfgefnu síðunni velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="b9020-156">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b9020-157">Í valmyndinni **Bæta við einingu** undir **Velja einingar** velurðu hetjueiningu og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b9020-157">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="b9020-158">Veldu hetjueininguna í útlínutrénu til vinstri.</span><span class="sxs-lookup"><span data-stu-id="b9020-158">In the outline tree on the left, select the hero module.</span></span>
1. <span data-ttu-id="b9020-159">Í eiginleikaglugganum til hægri velurðu **Bæta við mynd**.</span><span class="sxs-lookup"><span data-stu-id="b9020-159">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="b9020-160">Veldu þá annaðhvort núverandi mynd eða hladdu upp nýrri mynd.</span><span class="sxs-lookup"><span data-stu-id="b9020-160">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="b9020-161">Veldu **Fyrirsögn**.</span><span class="sxs-lookup"><span data-stu-id="b9020-161">Select **Heading**.</span></span>
1. <span data-ttu-id="b9020-162">Í valmyndinni **Fyrirsögn** bætirðu við fyrirsagnartexta, velur hausstig og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b9020-162">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="b9020-163">Undir **Sniðinn texti** bætirðu við texta eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="b9020-163">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="b9020-164">Veldu **Bæta við aðgerðartengli**.</span><span class="sxs-lookup"><span data-stu-id="b9020-164">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="b9020-165">Í valmyndinni **Aðgerðartengill** bætirðu við texta, slóð og ARIA-merki fyrir tengilinn og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b9020-165">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="b9020-166">Vistaðu síðuna og forskoðaðu breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="b9020-166">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="b9020-167">Athuga á síðunni og birtu hana.</span><span class="sxs-lookup"><span data-stu-id="b9020-167">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9020-168">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b9020-168">Additional resources</span></span>

[<span data-ttu-id="b9020-169">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="b9020-169">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b9020-170">Viðvörunareining</span><span class="sxs-lookup"><span data-stu-id="b9020-170">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="b9020-171">Myndaræmueining</span><span class="sxs-lookup"><span data-stu-id="b9020-171">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="b9020-172">Eining með fjölbreyttu efni</span><span class="sxs-lookup"><span data-stu-id="b9020-172">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="b9020-173">Staðsetningareining efnis</span><span class="sxs-lookup"><span data-stu-id="b9020-173">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="b9020-174">Eiginleikaeining</span><span class="sxs-lookup"><span data-stu-id="b9020-174">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="b9020-175">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="b9020-175">Video player module</span></span>](add-video-player.md)
