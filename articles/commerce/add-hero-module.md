---
title: Innihaldsbálkseining
description: Þetta efni fjallar um efnisbálkaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: ad95dc943f075e088f5e13b507fa08f11548282f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206272"
---
# <a name="content-block-module"></a><span data-ttu-id="83657-103">Eining fyrir bálk með efni</span><span class="sxs-lookup"><span data-stu-id="83657-103">Content block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="83657-104">Þetta efni fjallar um efnisbálkaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="83657-104">This topic covers content block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="83657-105">Innihaldsbálkseining er notuð til að markaðssetja vörur eða kynningar með blöndu af myndum og texta.</span><span class="sxs-lookup"><span data-stu-id="83657-105">A content block module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="83657-106">Til dæmis getur smásali bætt innihaldsbálkseiningu á heimasíðu svæðis fyrir rafræn viðskipti til að kynna nýja vöru og vekja athygli viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="83657-106">For example, a retailer can add a content block module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="83657-107">Innihaldsbálkseining er knúin áfram af gögnum frá efnisstýringarkerfinu (CMS).</span><span class="sxs-lookup"><span data-stu-id="83657-107">A content block module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="83657-108">Þetta er sjálfstæð eining sem er ekki háð öðrum einingum á síðunni.</span><span class="sxs-lookup"><span data-stu-id="83657-108">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="83657-109">Hægt er að setja innihaldsbálkseiningar á hvaða síðu sem er þar sem smásali vill markaðssetja eða auglýsa eitthvað (til dæmis vörur, útsölu eða eiginleika).</span><span class="sxs-lookup"><span data-stu-id="83657-109">A content block module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-content-block-module-in-e-commerce"></a><span data-ttu-id="83657-110">Dæmi um innihaldsbálkseiningu í rafrænum viðskiptum</span><span class="sxs-lookup"><span data-stu-id="83657-110">Examples of content block module in e-Commerce</span></span>

- <span data-ttu-id="83657-111">Hægt er að nota innihaldsbálkseiningu á heimasíðu svæðis fyrir rafræn viðskipti til að varpa ljósi á kynningar og nýjar vörur.</span><span class="sxs-lookup"><span data-stu-id="83657-111">A content block module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="83657-112">Hægt er að nota innihaldsbálkseiningu á upplýsingasíðu vöru til að sýna upplýsingar um vöru.</span><span class="sxs-lookup"><span data-stu-id="83657-112">A content block module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="83657-113">Hægt er að setja margar innihaldsbálkseiningar í myndaræmueiningu til að varpa ljósi á margar vörur eða kynningar.</span><span class="sxs-lookup"><span data-stu-id="83657-113">Multiple content block modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="content-block-modules-and-themes"></a><span data-ttu-id="83657-114">Innihaldsbálkseiningar og -þemu</span><span class="sxs-lookup"><span data-stu-id="83657-114">Content block modules and themes</span></span>

<span data-ttu-id="83657-115">Innihaldsbálkseiningar geta stutt ýmis útlit og stíla út frá þema.</span><span class="sxs-lookup"><span data-stu-id="83657-115">Content block modules can support various layouts and styles based on a theme.</span></span> <span data-ttu-id="83657-116">Til dæmis styður Fabrikam þemað þrjú skipulagstilbrigði af innihaldsbálkseiningum: hetja, eiginleiki og reitur.</span><span class="sxs-lookup"><span data-stu-id="83657-116">For example, the Fabrikam theme supports three layout variations of a content block module: hero, feature, and tile.</span></span> <span data-ttu-id="83657-117">Hetjuuppsetningin sýnir mynd á bakgrunni með textayfirlagi.</span><span class="sxs-lookup"><span data-stu-id="83657-117">The hero layout shows an image on the background with text overlay.</span></span> <span data-ttu-id="83657-118">Skipulag eiginleika sýnir mynd og texta hlið við hlið.</span><span class="sxs-lookup"><span data-stu-id="83657-118">The feature layout shows an image and text side by side.</span></span> <span data-ttu-id="83657-119">Uppsetning reitanna gerir kleift að hafa margvíslega efnisbálka á reitasniði.</span><span class="sxs-lookup"><span data-stu-id="83657-119">The tile layout allows multiple content blocks in a tile format.</span></span>

<span data-ttu-id="83657-120">Að auki getur þemað afhjúpað mismunandi eiginleika fyrir hvert skipulag.</span><span class="sxs-lookup"><span data-stu-id="83657-120">In addition, the theme can expose different properties for each layout.</span></span> <span data-ttu-id="83657-121">Þemahönnuður getur smíðað fleiri skipulag með fleiri stílum með því að nota innihaldsbálkaeininguna.</span><span class="sxs-lookup"><span data-stu-id="83657-121">A theme developer can build more layouts with more styles using the content block module.</span></span>

<span data-ttu-id="83657-122">Eftirfarandi mynd sýnir dæmi um innihaldsbálkseiningu með hetjuuppsetningu.</span><span class="sxs-lookup"><span data-stu-id="83657-122">The following image shows an example of a content block module with a hero layout.</span></span>

![Dæmi um hetjueiningu](./media/Hero.PNG)

<span data-ttu-id="83657-124">Eftirfarandi mynd sýnir dæmi um innihaldsbálkseiningu með eiginleikauppsetningu.</span><span class="sxs-lookup"><span data-stu-id="83657-124">The following image shows an example of a content block module with a feature layout.</span></span>

![Dæmi um eiginleikaeiningar](./media/Feature.PNG)

## <a name="content-block-module-properties"></a><span data-ttu-id="83657-126">Eiginleikar innihaldsbálks</span><span class="sxs-lookup"><span data-stu-id="83657-126">Content block module properties</span></span>

| <span data-ttu-id="83657-127">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="83657-127">Property name</span></span>  | <span data-ttu-id="83657-128">Gildi</span><span class="sxs-lookup"><span data-stu-id="83657-128">Values</span></span> | <span data-ttu-id="83657-129">Lýsing</span><span class="sxs-lookup"><span data-stu-id="83657-129">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="83657-130">Mynd</span><span class="sxs-lookup"><span data-stu-id="83657-130">Image</span></span>          | <span data-ttu-id="83657-131">Myndaskrá</span><span class="sxs-lookup"><span data-stu-id="83657-131">Image file</span></span> | <span data-ttu-id="83657-132">Hægt er að nota mynd til að sýna vöruna eða auglýsa.</span><span class="sxs-lookup"><span data-stu-id="83657-132">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="83657-133">Hægt er að hlaða mynd inn í myndasafnið eða nota núverandi mynd.</span><span class="sxs-lookup"><span data-stu-id="83657-133">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="83657-134">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="83657-134">Heading</span></span>        | <span data-ttu-id="83657-135">Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**)</span><span class="sxs-lookup"><span data-stu-id="83657-135">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="83657-136">Sérhver hetjueining getur haft fyrirsögn.</span><span class="sxs-lookup"><span data-stu-id="83657-136">Every hero module can have a heading.</span></span> <span data-ttu-id="83657-137">Sjálfgefið er að fyrirsagnarmerkið **H2** er notað fyrir fyrirsögnina.</span><span class="sxs-lookup"><span data-stu-id="83657-137">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="83657-138">Hins vegar er hægt að breyta merkinu til að uppfylla kröfur um aðgengi.</span><span class="sxs-lookup"><span data-stu-id="83657-138">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="83657-139">Efnisgrein</span><span class="sxs-lookup"><span data-stu-id="83657-139">Paragraph</span></span>      | <span data-ttu-id="83657-140">Texti efnisgreinar</span><span class="sxs-lookup"><span data-stu-id="83657-140">Paragraph text</span></span> | <span data-ttu-id="83657-141">Hetjueiningar styðja málsgreinatexta með ríku textasniði.</span><span class="sxs-lookup"><span data-stu-id="83657-141">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="83657-142">Stuðningur er við nokkra grunntextaeiginleika, eins og feitletrun, undirstrikun og skáletrun texta og tengla.</span><span class="sxs-lookup"><span data-stu-id="83657-142">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="83657-143">Sumum af þessum eiginleikum er hægt að hnekkja með síðuþema sem er beitt á eininguna.</span><span class="sxs-lookup"><span data-stu-id="83657-143">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="83657-144">Tengill</span><span class="sxs-lookup"><span data-stu-id="83657-144">Link</span></span>           | <span data-ttu-id="83657-145">Tenglatexti, vefslóð tengils, ARIA-merki (Accessible Rich Internet Applications) og **Opnaðu hlekk í nýjum flipa**</span><span class="sxs-lookup"><span data-stu-id="83657-145">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="83657-146">Hetjueiningar styðja einn eða fleiri „kalla til aðgerða“ tengla.</span><span class="sxs-lookup"><span data-stu-id="83657-146">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="83657-147">Ef tengli er bætt við þarf tenglatexta, vefslóð og ARIA-merki.</span><span class="sxs-lookup"><span data-stu-id="83657-147">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="83657-148">ARIA-merki ættu að vera lýsandi til að uppfylla kröfur um aðgengi.</span><span class="sxs-lookup"><span data-stu-id="83657-148">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="83657-149">Hægt er að stilla tengla þannig að þeir séu opnaðir á nýjum flipa.</span><span class="sxs-lookup"><span data-stu-id="83657-149">Links can be configured so that they are opened on a new tab.</span></span> |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a><span data-ttu-id="83657-150">Eiginleikar innihaldsbálkseininga útsettir fyrir Fabrikam-þema</span><span class="sxs-lookup"><span data-stu-id="83657-150">Content block module properties exposed by the Fabrikam theme</span></span> 

| <span data-ttu-id="83657-151">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="83657-151">Property name</span></span>  | <span data-ttu-id="83657-152">Gildi</span><span class="sxs-lookup"><span data-stu-id="83657-152">Values</span></span> | <span data-ttu-id="83657-153">Lýsing</span><span class="sxs-lookup"><span data-stu-id="83657-153">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="83657-154">Staðsetning texta</span><span class="sxs-lookup"><span data-stu-id="83657-154">Text placement</span></span> | <span data-ttu-id="83657-155">**Hægri**, **vinstri**, **miðja**</span><span class="sxs-lookup"><span data-stu-id="83657-155">**Left**, **Right**, **Center**</span></span> | <span data-ttu-id="83657-156">Þessi eiginleiki skilgreinir staðsetningu textans á myndinni.</span><span class="sxs-lookup"><span data-stu-id="83657-156">This property defines the position of the text on the image.</span></span> <span data-ttu-id="83657-157">Hann á aðeins við um hetjuuppsetninguna.</span><span class="sxs-lookup"><span data-stu-id="83657-157">It only applies to the hero layout.</span></span> |
| <span data-ttu-id="83657-158">Aðalefni texta</span><span class="sxs-lookup"><span data-stu-id="83657-158">Text theme</span></span>     | <span data-ttu-id="83657-159">**Ljóst** eða **Dökkt**</span><span class="sxs-lookup"><span data-stu-id="83657-159">**Light** or **Dark**</span></span> | <span data-ttu-id="83657-160">Hægt er að skilgreina litasamsetningu fyrir textann, byggt á bakgrunnsmyndinni.</span><span class="sxs-lookup"><span data-stu-id="83657-160">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="83657-161">Til dæmis, ef myndin er með dökkan bakgrunn, er hægt að beita léttu þema til að gera textann sýnilegri og til að mæta andstæða litastigshlutfalla í aðgengisskyni.</span><span class="sxs-lookup"><span data-stu-id="83657-161">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> <span data-ttu-id="83657-162">Hann á aðeins við um hetjuuppsetninguna.</span><span class="sxs-lookup"><span data-stu-id="83657-162">It only applies to the hero layout.</span></span>|
| <span data-ttu-id="83657-163">Staðsetning myndar</span><span class="sxs-lookup"><span data-stu-id="83657-163">Image placement</span></span>       | <span data-ttu-id="83657-164">**Vintri**,  **hægri**</span><span class="sxs-lookup"><span data-stu-id="83657-164">**Left**,  **Right**</span></span> | <span data-ttu-id="83657-165">Þessi eiginleiki tilgreinir hvort myndin skuli vera til vinstri eða hægri í textanum.</span><span class="sxs-lookup"><span data-stu-id="83657-165">This property specifies if the image should be to the left or right of the text.</span></span> <span data-ttu-id="83657-166">Hann á aðeins við um eiginleikauppsetninguna.</span><span class="sxs-lookup"><span data-stu-id="83657-166">It only applies to the feature layout.</span></span>  |

## <a name="add-a-content-block-module-to-a-new-page"></a><span data-ttu-id="83657-167">Bæta við innihaldsbálkseiningu á nýja síðu</span><span class="sxs-lookup"><span data-stu-id="83657-167">Add a content block module to a new page</span></span>

<span data-ttu-id="83657-168">Fylgdu þessum skrefum til að bæta hetjueiningu við nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="83657-168">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="83657-169">Farðu í **Sniðmát** og búðu til síðusniðmát sem heitir **Sniðmát útilokunar á efni**.</span><span class="sxs-lookup"><span data-stu-id="83657-169">Go to **Templates**, and create a page template that is named **Content block template**.</span></span>
1. <span data-ttu-id="83657-170">Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við hetjueiningu.</span><span class="sxs-lookup"><span data-stu-id="83657-170">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="83657-171">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="83657-171">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="83657-172">Notaðu sniðmátið fyrir aðalsíðuna sem þú varst að búa til, til að búa til síðu sem heitir **Síða útilokunar á efni**.</span><span class="sxs-lookup"><span data-stu-id="83657-172">Use the hero template that you just created to create a page that is named **Content block page**.</span></span>
1. <span data-ttu-id="83657-173">Í hólfinu **Aðal** á sjálfgefnu síðunni velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="83657-173">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="83657-174">Í valmyndinni **Bæta við einingu** undir **Velja einingar** velurðu hetjueiningu og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="83657-174">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="83657-175">Veldu innihaldsbálkseininguna í útlínutrénu til vinstri.</span><span class="sxs-lookup"><span data-stu-id="83657-175">In the outline tree on the left, select the content block module.</span></span>
1. <span data-ttu-id="83657-176">Í eiginleikaglugganum til hægri velurðu **Bæta við mynd**.</span><span class="sxs-lookup"><span data-stu-id="83657-176">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="83657-177">Veldu þá annaðhvort núverandi mynd eða hladdu upp nýrri mynd.</span><span class="sxs-lookup"><span data-stu-id="83657-177">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="83657-178">Veldu **Fyrirsögn**.</span><span class="sxs-lookup"><span data-stu-id="83657-178">Select **Heading**.</span></span>
1. <span data-ttu-id="83657-179">Í valmyndinni **Fyrirsögn** bætirðu við fyrirsagnartexta, velur hausstig og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="83657-179">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="83657-180">Undir **Sniðinn texti** bætirðu við texta eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="83657-180">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="83657-181">Veldu **Bæta við tengli**.</span><span class="sxs-lookup"><span data-stu-id="83657-181">Select **Add Link**.</span></span>
1. <span data-ttu-id="83657-182">Í valmyndinni **Tengill** bætirðu við texta, slóð og ARIA-merki fyrir tengilinn og velur síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="83657-182">In the **Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="83657-183">Veldu skipulagið **Hetja**.</span><span class="sxs-lookup"><span data-stu-id="83657-183">Select the **Hero** layout.</span></span>
1. <span data-ttu-id="83657-184">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="83657-184">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="83657-185">Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="83657-185">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="83657-186">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="83657-186">Additional resources</span></span>

[<span data-ttu-id="83657-187">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="83657-187">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="83657-188">Tilboðsborðaeining</span><span class="sxs-lookup"><span data-stu-id="83657-188">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="83657-189">Myndaræmueining</span><span class="sxs-lookup"><span data-stu-id="83657-189">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="83657-190">Textabálkseining</span><span class="sxs-lookup"><span data-stu-id="83657-190">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="83657-191">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="83657-191">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]