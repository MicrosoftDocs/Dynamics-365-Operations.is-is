---
title: Innihaldsbálkseining
description: Þetta efni fjallar um innihaldsbálseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: a6359c915d053bb00c969b166325f675c0003ead
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980358"
---
# <a name="content-block-module"></a><span data-ttu-id="e95f8-103">Innihaldsbálkseining</span><span class="sxs-lookup"><span data-stu-id="e95f8-103">Content block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e95f8-104">Þetta efni fjallar um innihaldsbálseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e95f8-104">This topic covers content block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e95f8-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="e95f8-105">Overview</span></span>

<span data-ttu-id="e95f8-106">Innihaldsbálkseining er notuð til að markaðssetja vörur eða kynningar með blöndu af myndum og texta.</span><span class="sxs-lookup"><span data-stu-id="e95f8-106">A content block module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="e95f8-107">Til dæmis getur smásali bætt innihaldsbálkseiningu á heimasíðu svæðis fyrir rafræn viðskipti til að kynna nýja vöru og vekja athygli viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="e95f8-107">For example, a retailer can add a content block module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="e95f8-108">Innihaldsbálkseining er knúin áfram af gögnum frá efnisstýringarkerfinu (CMS).</span><span class="sxs-lookup"><span data-stu-id="e95f8-108">A content block module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="e95f8-109">Þetta er sjálfstæð eining sem er ekki háð öðrum einingum á síðunni.</span><span class="sxs-lookup"><span data-stu-id="e95f8-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="e95f8-110">Hægt er að setja innihaldsbálkseiningar á hvaða síðu sem er þar sem smásali vill markaðssetja eða auglýsa eitthvað (til dæmis vörur, útsölu eða eiginleika).</span><span class="sxs-lookup"><span data-stu-id="e95f8-110">A content block module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-content-block-module-in-e-commerce"></a><span data-ttu-id="e95f8-111">Dæmi um innihaldsbálkseiningu í rafrænum viðskiptum</span><span class="sxs-lookup"><span data-stu-id="e95f8-111">Examples of content block module in e-Commerce</span></span>

- <span data-ttu-id="e95f8-112">Hægt er að nota innihaldsbálkseiningu á heimasíðu svæðis fyrir rafræn viðskipti til að varpa ljósi á kynningar og nýjar vörur.</span><span class="sxs-lookup"><span data-stu-id="e95f8-112">A content block module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="e95f8-113">Hægt er að nota innihaldsbálkseiningu á upplýsingasíðu vöru til að sýna upplýsingar um vöru.</span><span class="sxs-lookup"><span data-stu-id="e95f8-113">A content block module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="e95f8-114">Hægt er að setja margar innihaldsbálkseiningar í myndaræmueiningu til að varpa ljósi á margar vörur eða kynningar.</span><span class="sxs-lookup"><span data-stu-id="e95f8-114">Multiple content block modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="content-block-modules-and-themes"></a><span data-ttu-id="e95f8-115">Innihaldsbálkseiningar og -þemu</span><span class="sxs-lookup"><span data-stu-id="e95f8-115">Content block modules and themes</span></span>

<span data-ttu-id="e95f8-116">Innihaldsbálkseiningar geta stutt ýmis útlit og stíla út frá þema.</span><span class="sxs-lookup"><span data-stu-id="e95f8-116">Content block modules can support various layouts and styles based on a theme.</span></span> <span data-ttu-id="e95f8-117">Til dæmis styður Fabrikam þemað þrjú skipulagstilbrigði af innihaldsbálkseiningum: hetja, eiginleiki og reitur.</span><span class="sxs-lookup"><span data-stu-id="e95f8-117">For example, the Fabrikam theme supports three layout variations of a content block module: hero, feature, and tile.</span></span> <span data-ttu-id="e95f8-118">Hetjuuppsetningin sýnir mynd á bakgrunni með textayfirlagi.</span><span class="sxs-lookup"><span data-stu-id="e95f8-118">The hero layout shows an image on the background with text overlay.</span></span> <span data-ttu-id="e95f8-119">Skipulag eiginleika sýnir mynd og texta hlið við hlið.</span><span class="sxs-lookup"><span data-stu-id="e95f8-119">The feature layout shows an image and text side by side.</span></span> <span data-ttu-id="e95f8-120">Uppsetning reitanna gerir kleift að hafa margvíslega efnisbálka á reitasniði.</span><span class="sxs-lookup"><span data-stu-id="e95f8-120">The tile layout allows multiple content blocks in a tile format.</span></span>

<span data-ttu-id="e95f8-121">Að auki getur þemað afhjúpað mismunandi eiginleika fyrir hvert skipulag.</span><span class="sxs-lookup"><span data-stu-id="e95f8-121">In addition, the theme can expose different properties for each layout.</span></span> <span data-ttu-id="e95f8-122">Þemahönnuður getur smíðað fleiri skipulag með fleiri stílum með því að nota innihaldsbálkaeininguna.</span><span class="sxs-lookup"><span data-stu-id="e95f8-122">A theme developer can build more layouts with more styles using the content block module.</span></span>

<span data-ttu-id="e95f8-123">Eftirfarandi mynd sýnir dæmi um innihaldsbálkseiningu með hetjuuppsetningu.</span><span class="sxs-lookup"><span data-stu-id="e95f8-123">The following image shows an example of a content block module with a hero layout.</span></span>

![Dæmi um hetjueiningu](./media/Hero.PNG)

<span data-ttu-id="e95f8-125">Eftirfarandi mynd sýnir dæmi um innihaldsbálkseiningu með eiginleikauppsetningu.</span><span class="sxs-lookup"><span data-stu-id="e95f8-125">The following image shows an example of a content block module with a feature layout.</span></span>

![Dæmi um eiginleikaeiningar](./media/Feature.PNG)

## <a name="content-block-module-properties"></a><span data-ttu-id="e95f8-127">Eiginleikar innihaldsbálks</span><span class="sxs-lookup"><span data-stu-id="e95f8-127">Content block module properties</span></span>

| <span data-ttu-id="e95f8-128">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="e95f8-128">Property name</span></span>  | <span data-ttu-id="e95f8-129">Gildi</span><span class="sxs-lookup"><span data-stu-id="e95f8-129">Values</span></span> | <span data-ttu-id="e95f8-130">Lýsing</span><span class="sxs-lookup"><span data-stu-id="e95f8-130">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="e95f8-131">Mynd</span><span class="sxs-lookup"><span data-stu-id="e95f8-131">Image</span></span>          | <span data-ttu-id="e95f8-132">Myndaskrá</span><span class="sxs-lookup"><span data-stu-id="e95f8-132">Image file</span></span> | <span data-ttu-id="e95f8-133">Hægt er að nota mynd til að sýna vöruna eða auglýsa.</span><span class="sxs-lookup"><span data-stu-id="e95f8-133">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="e95f8-134">Hægt er að hlaða mynd inn í myndasafnið eða nota núverandi mynd.</span><span class="sxs-lookup"><span data-stu-id="e95f8-134">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="e95f8-135">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="e95f8-135">Heading</span></span>        | <span data-ttu-id="e95f8-136">Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**)</span><span class="sxs-lookup"><span data-stu-id="e95f8-136">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="e95f8-137">Sérhver hetjueining getur haft fyrirsögn.</span><span class="sxs-lookup"><span data-stu-id="e95f8-137">Every hero module can have a heading.</span></span> <span data-ttu-id="e95f8-138">Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina.</span><span class="sxs-lookup"><span data-stu-id="e95f8-138">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="e95f8-139">Hins vegar er hægt að breyta merkinu til að uppfylla kröfur um aðgengi.</span><span class="sxs-lookup"><span data-stu-id="e95f8-139">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="e95f8-140">Efnisgrein</span><span class="sxs-lookup"><span data-stu-id="e95f8-140">Paragraph</span></span>      | <span data-ttu-id="e95f8-141">Texti efnisgreinar</span><span class="sxs-lookup"><span data-stu-id="e95f8-141">Paragraph text</span></span> | <span data-ttu-id="e95f8-142">Hetjueiningar styðja málsgreinatexta með ríku textasniði.</span><span class="sxs-lookup"><span data-stu-id="e95f8-142">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="e95f8-143">Stuðningur er við nokkra grunntextaeiginleika, eins og feitletrun, undirstrikun og skáletrun texta og tengla.</span><span class="sxs-lookup"><span data-stu-id="e95f8-143">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="e95f8-144">Sumum af þessum eiginleikum er hægt að hnekkja með síðuþema sem er beitt á eininguna.</span><span class="sxs-lookup"><span data-stu-id="e95f8-144">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="e95f8-145">Tengill</span><span class="sxs-lookup"><span data-stu-id="e95f8-145">Link</span></span>           | <span data-ttu-id="e95f8-146">Tenglatexti, vefslóð tengils, ARIA-merki (Accessible Rich Internet Applications) og **Opnaðu hlekk í nýjum flipa**</span><span class="sxs-lookup"><span data-stu-id="e95f8-146">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="e95f8-147">Hetjueiningar styðja einn eða fleiri „kalla til aðgerða“ tengla.</span><span class="sxs-lookup"><span data-stu-id="e95f8-147">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="e95f8-148">Ef tengli er bætt við þarf tenglatexta, vefslóð og ARIA-merki.</span><span class="sxs-lookup"><span data-stu-id="e95f8-148">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="e95f8-149">ARIA-merki ættu að vera lýsandi til að uppfylla kröfur um aðgengi.</span><span class="sxs-lookup"><span data-stu-id="e95f8-149">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="e95f8-150">Hægt er að stilla tengla þannig að þeir séu opnaðir á nýjum flipa.</span><span class="sxs-lookup"><span data-stu-id="e95f8-150">Links can be configured so that they are opened on a new tab.</span></span> |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a><span data-ttu-id="e95f8-151">Eiginleikar innihaldsbálkseininga útsettir fyrir Fabrikam-þema</span><span class="sxs-lookup"><span data-stu-id="e95f8-151">Content block module properties exposed by the Fabrikam theme</span></span> 

| <span data-ttu-id="e95f8-152">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="e95f8-152">Property name</span></span>  | <span data-ttu-id="e95f8-153">Gildi</span><span class="sxs-lookup"><span data-stu-id="e95f8-153">Values</span></span> | <span data-ttu-id="e95f8-154">Lýsing</span><span class="sxs-lookup"><span data-stu-id="e95f8-154">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="e95f8-155">Staðsetning texta</span><span class="sxs-lookup"><span data-stu-id="e95f8-155">Text placement</span></span> | <span data-ttu-id="e95f8-156">**Hægri**, **vinstri**, **miðja**</span><span class="sxs-lookup"><span data-stu-id="e95f8-156">**Left**, **Right**, **Center**</span></span> | <span data-ttu-id="e95f8-157">Þessi eiginleiki skilgreinir staðsetningu textans á myndinni.</span><span class="sxs-lookup"><span data-stu-id="e95f8-157">This property defines the position of the text on the image.</span></span> <span data-ttu-id="e95f8-158">Hann á aðeins við um hetjuuppsetninguna.</span><span class="sxs-lookup"><span data-stu-id="e95f8-158">It only applies to the hero layout.</span></span> |
| <span data-ttu-id="e95f8-159">Aðalefni texta</span><span class="sxs-lookup"><span data-stu-id="e95f8-159">Text theme</span></span>     | <span data-ttu-id="e95f8-160">**Ljóst** eða **Dökkt**</span><span class="sxs-lookup"><span data-stu-id="e95f8-160">**Light** or **Dark**</span></span> | <span data-ttu-id="e95f8-161">Hægt er að skilgreina litasamsetningu fyrir textann, byggt á bakgrunnsmyndinni.</span><span class="sxs-lookup"><span data-stu-id="e95f8-161">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="e95f8-162">Til dæmis, ef myndin er með dökkan bakgrunn, er hægt að beita léttu þema til að gera textann sýnilegri og til að mæta andstæða litastigshlutfalla í aðgengisskyni.</span><span class="sxs-lookup"><span data-stu-id="e95f8-162">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> <span data-ttu-id="e95f8-163">Hann á aðeins við um hetjuuppsetninguna.</span><span class="sxs-lookup"><span data-stu-id="e95f8-163">It only applies to the hero layout.</span></span>|
| <span data-ttu-id="e95f8-164">Staðsetning myndar</span><span class="sxs-lookup"><span data-stu-id="e95f8-164">Image placement</span></span>       | <span data-ttu-id="e95f8-165">**Vintri**,  **hægri**</span><span class="sxs-lookup"><span data-stu-id="e95f8-165">**Left**,  **Right**</span></span> | <span data-ttu-id="e95f8-166">Þessi eiginleiki tilgreinir hvort myndin skuli vera til vinstri eða hægri í textanum.</span><span class="sxs-lookup"><span data-stu-id="e95f8-166">This property specifies if the image should be to the left or right of the text.</span></span> <span data-ttu-id="e95f8-167">Hann á aðeins við um eiginleikauppsetninguna.</span><span class="sxs-lookup"><span data-stu-id="e95f8-167">It only applies to the feature layout.</span></span>  |

## <a name="add-a-content-block-module-to-a-new-page"></a><span data-ttu-id="e95f8-168">Bæta við innihaldsbálkseiningu á nýja síðu</span><span class="sxs-lookup"><span data-stu-id="e95f8-168">Add a content block module to a new page</span></span>

<span data-ttu-id="e95f8-169">Fylgdu þessum skrefum til að bæta hetjueiningu við nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="e95f8-169">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="e95f8-170">Farðu í **Sniðmát** og búðu til síðusniðmát sem heitir **Sniðmát útilokunar á efni**.</span><span class="sxs-lookup"><span data-stu-id="e95f8-170">Go to **Templates**, and create a page template that is named **Content block template**.</span></span>
1. <span data-ttu-id="e95f8-171">Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við hetjueiningu.</span><span class="sxs-lookup"><span data-stu-id="e95f8-171">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="e95f8-172">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="e95f8-172">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="e95f8-173">Notaðu sniðmátið fyrir aðalsíðuna sem þú varst að búa til, til að búa til síðu sem heitir **Síða útilokunar á efni**.</span><span class="sxs-lookup"><span data-stu-id="e95f8-173">Use the hero template that you just created to create a page that is named **Content block page**.</span></span>
1. <span data-ttu-id="e95f8-174">Í hólfinu **Aðal** á sjálfgefnu síðunni velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="e95f8-174">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e95f8-175">Í valmyndinni **Bæta við einingu** undir **Velja einingar** velurðu hetjueiningu og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e95f8-175">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="e95f8-176">Veldu innihaldsbálkseininguna í útlínutrénu til vinstri.</span><span class="sxs-lookup"><span data-stu-id="e95f8-176">In the outline tree on the left, select the content block module.</span></span>
1. <span data-ttu-id="e95f8-177">Í eiginleikaglugganum til hægri velurðu **Bæta við mynd**.</span><span class="sxs-lookup"><span data-stu-id="e95f8-177">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="e95f8-178">Veldu þá annaðhvort núverandi mynd eða hladdu upp nýrri mynd.</span><span class="sxs-lookup"><span data-stu-id="e95f8-178">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="e95f8-179">Veldu **Fyrirsögn**.</span><span class="sxs-lookup"><span data-stu-id="e95f8-179">Select **Heading**.</span></span>
1. <span data-ttu-id="e95f8-180">Í valmyndinni **Fyrirsögn** bætirðu við fyrirsagnartexta, velur hausstig og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e95f8-180">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="e95f8-181">Undir **Sniðinn texti** bætirðu við texta eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e95f8-181">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="e95f8-182">Veldu **Bæta við tengli**.</span><span class="sxs-lookup"><span data-stu-id="e95f8-182">Select **Add Link**.</span></span>
1. <span data-ttu-id="e95f8-183">Í valmyndinni **Tengill** bætirðu við texta, slóð og ARIA-merki fyrir tengilinn og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e95f8-183">In the **Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="e95f8-184">Veldu skipulagið **Hetja**.</span><span class="sxs-lookup"><span data-stu-id="e95f8-184">Select the **Hero** layout.</span></span>
1. <span data-ttu-id="e95f8-185">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="e95f8-185">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="e95f8-186">Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="e95f8-186">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="e95f8-187">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e95f8-187">Additional resources</span></span>

[<span data-ttu-id="e95f8-188">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="e95f8-188">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e95f8-189">Tilboðsborðaeining</span><span class="sxs-lookup"><span data-stu-id="e95f8-189">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="e95f8-190">Myndaræmueining</span><span class="sxs-lookup"><span data-stu-id="e95f8-190">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="e95f8-191">Textabálkseining</span><span class="sxs-lookup"><span data-stu-id="e95f8-191">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="e95f8-192">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="e95f8-192">Video player module</span></span>](add-video-player.md)
