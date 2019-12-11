---
title: Staðsetningareining efnis
description: Þetta efni fjallar um staðsetningu efnis og staðsetningareiningar efnis og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785301"
---
# <a name="content-placement-module"></a><span data-ttu-id="2d242-103">Staðsetningareining efnis</span><span class="sxs-lookup"><span data-stu-id="2d242-103">Content placement module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2d242-104">Þetta efni fjallar um staðsetningu efnis og staðsetningareiningar efnis og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2d242-104">This topic covers content placement and content placement item modules, and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2d242-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="2d242-105">Overview</span></span>

<span data-ttu-id="2d242-106">Staðsetningareining efnis er sérstakur gámur sem hægt er að setja aðrar einingar inn í í tilteknu skipulagi.</span><span class="sxs-lookup"><span data-stu-id="2d242-106">A content placement module is a special container that other modules can be put inside in a specific layout.</span></span> <span data-ttu-id="2d242-107">Staðsetningareiningar efnis styðja eftirfarandi gerðir af einingum sem undireiningar: staðsetningarlið efnis, móttökulið reiknings, pöntunarlið reiknings, óskalistalið reiknings og forstillingarlið reiknings.</span><span class="sxs-lookup"><span data-stu-id="2d242-107">Content placement modules support the following types of modules as child modules: content placement item, account welcome item, account order item, account wish list item, and account profile item.</span></span>

<span data-ttu-id="2d242-108">Staðsetningareiningar efnis fá gögn úr undireiningunum sem þær styðja.</span><span class="sxs-lookup"><span data-stu-id="2d242-108">Content placement modules derive data from the child modules that they support.</span></span> <span data-ttu-id="2d242-109">Þess vegna er hægt að nota staðsetningareiningar efnis á ýmsa vegu, allt eftir þeim einingum sem bætt er við það.</span><span class="sxs-lookup"><span data-stu-id="2d242-109">Therefore, content placement modules can be used in various ways, depending on the modules that are added to it.</span></span>

<span data-ttu-id="2d242-110">Staðsetningareiningar efnis nota bæði myndir og texta til að sýna kynningar, stefnur og vöruaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="2d242-110">Content placement item modules use both images and text to showcase promotions, policies, and product features.</span></span> <span data-ttu-id="2d242-111">Til dæmis er hægt að nota einingu staðsetningarliðar efnis á heimasíðunni til að sýna stefnu um verslun eða sendingarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="2d242-111">For example, a content placement item module can be used on a home page to show store policies or shipping information.</span></span> <span data-ttu-id="2d242-112">Einingar staðsetningarliðar efnis eru knúnar af gögnum frá efnisstýringarkerfinu (CMS) og hægt er að setja þær á hvaða síðu sem er.</span><span class="sxs-lookup"><span data-stu-id="2d242-112">Content placement item modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="2d242-113">Hins vegar er aðeins hægt að nota þær í staðsetningareiningu efnis.</span><span class="sxs-lookup"><span data-stu-id="2d242-113">However, they can be used only inside a content placement module.</span></span>

## <a name="examples-of-content-placement-modules-in-e-commerce"></a><span data-ttu-id="2d242-114">Dæmi um staðsetningareiningar efnis í rafrænum viðskiptum</span><span class="sxs-lookup"><span data-stu-id="2d242-114">Examples of content placement modules in e-Commerce</span></span>

* <span data-ttu-id="2d242-115">Hægt er að nota staðsetningareiningar efnis sem innihalda einingar staðsetningarliðar efnis á heimasíðu eða markaðssíðum til að sýna vörueiginleika, kynningar, verslunarstefnu, sendingarupplýsingar og aðrar upplýsingar í gegnum bæði myndir og texta.</span><span class="sxs-lookup"><span data-stu-id="2d242-115">Content placement modules that contain content placement item modules can be used on a home page or marketing pages to showcase product features, promotions, store policies, shipping information, and other information through both images and text.</span></span>
* <span data-ttu-id="2d242-116">Hægt er að nota staðsetningareiningar efnis sem innihalda einingar staðsetningarliðar efnis á upplýsingasíðum til að sýna eiginleika vöru.</span><span class="sxs-lookup"><span data-stu-id="2d242-116">Content placement modules that contain content placement item modules can be used on product details pages to showcase product features.</span></span>
* <span data-ttu-id="2d242-117">Hægt er að nota staðsetningareiningar efnis sem innihalda móttökulið reiknings eða pöntunarlið reiknings á síðum reikningastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="2d242-117">Content placement modules that contain account welcome item or account order item modules can be used on account management pages.</span></span>

## <a name="content-placement-module-properties"></a><span data-ttu-id="2d242-118">Eiginleikar staðsetningareiningar efnis</span><span class="sxs-lookup"><span data-stu-id="2d242-118">Content placement module properties</span></span>

| <span data-ttu-id="2d242-119">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="2d242-119">Property name</span></span> | <span data-ttu-id="2d242-120">Virði</span><span class="sxs-lookup"><span data-stu-id="2d242-120">Value</span></span> | <span data-ttu-id="2d242-121">Lýsing</span><span class="sxs-lookup"><span data-stu-id="2d242-121">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="2d242-122">Breidd</span><span class="sxs-lookup"><span data-stu-id="2d242-122">Width</span></span>         | <span data-ttu-id="2d242-123">**Passa í gám** eða **Fylla skjáinn**</span><span class="sxs-lookup"><span data-stu-id="2d242-123">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="2d242-124">Ef gildi er stillt á **Passa í gám** eru hlutirnir í staðsetningareiningu efnis takmarkaðir við breidd staðsetningareiningar efnis.</span><span class="sxs-lookup"><span data-stu-id="2d242-124">If the value is set to **Fit container**, the items inside the content placement module are restricted to the width of the content placement module.</span></span> <span data-ttu-id="2d242-125">Ef gildi er stillt á **Fylla skjáinn** eru atriðin takmörkuð við breidd staðsetningareiningar efnis en geta farið í stillingar fyrir allan skjáinn.</span><span class="sxs-lookup"><span data-stu-id="2d242-125">If the value is set to **Fill screen**, the items aren't restricted to the width of the content placement module but can go into full-screen mode.</span></span> |

## <a name="content-placement-item-module-properties"></a><span data-ttu-id="2d242-126">Eiginleikar staðsetningarliðareiningar efnis</span><span class="sxs-lookup"><span data-stu-id="2d242-126">Content placement item module properties</span></span>

| <span data-ttu-id="2d242-127">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="2d242-127">Property name</span></span> | <span data-ttu-id="2d242-128">Virði</span><span class="sxs-lookup"><span data-stu-id="2d242-128">Value</span></span> | <span data-ttu-id="2d242-129">Lýsing</span><span class="sxs-lookup"><span data-stu-id="2d242-129">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="2d242-130">Fyrirsögn</span><span class="sxs-lookup"><span data-stu-id="2d242-130">Heading</span></span>       | <span data-ttu-id="2d242-131">Texti og merki fyrirsagnar (**H1**, **H2**, **H3**, **H4**, **H5** eða **H6**)</span><span class="sxs-lookup"><span data-stu-id="2d242-131">Heading text and heading tags (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="2d242-132">Sérhver staðsetningarliðareiningar efnis getur haft fyrirsögn.</span><span class="sxs-lookup"><span data-stu-id="2d242-132">Every content placement item module can have a heading.</span></span> <span data-ttu-id="2d242-133">Eiginleikinn **Fyrirsögn** styður fyrirsagnamerki.</span><span class="sxs-lookup"><span data-stu-id="2d242-133">The **Heading** property supports heading tags.</span></span> <span data-ttu-id="2d242-134">Sjálfgefið er að fyrirsagnarmerkið **H2** sé notað, en hægt er að breyta fyrirsagnarmerkinu svo að það uppfylli kröfur um aðgengi.</span><span class="sxs-lookup"><span data-stu-id="2d242-134">By default, the **H2** heading tag is used, but the heading tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="2d242-135">Efnisgrein</span><span class="sxs-lookup"><span data-stu-id="2d242-135">Paragraph</span></span>     | <span data-ttu-id="2d242-136">Texti efnisgreinar</span><span class="sxs-lookup"><span data-stu-id="2d242-136">Paragraph text</span></span> | <span data-ttu-id="2d242-137">Staðsetningarliðareiningar efnis styðja málsgreinatexta með ríku textasniði.</span><span class="sxs-lookup"><span data-stu-id="2d242-137">Content placement item modules support paragraph text in rich text format.</span></span> <span data-ttu-id="2d242-138">Stuðningur er við nokkra grunntextaeiginleika, eins og feitletrun, undirstrikun og skáletrun texta og tengla.</span><span class="sxs-lookup"><span data-stu-id="2d242-138">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="2d242-139">Sumum af þessum eiginleikum er hægt að hnekkja með síðuþema sem er beitt á eininguna.</span><span class="sxs-lookup"><span data-stu-id="2d242-139">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="2d242-140">Mynd</span><span class="sxs-lookup"><span data-stu-id="2d242-140">Image</span></span>         | <span data-ttu-id="2d242-141">Myndaskrá</span><span class="sxs-lookup"><span data-stu-id="2d242-141">Image file</span></span> | <span data-ttu-id="2d242-142">Hægt er að tengja mynd við textann.</span><span class="sxs-lookup"><span data-stu-id="2d242-142">An image can be associated with the text.</span></span> |
| <span data-ttu-id="2d242-143">Tengill</span><span class="sxs-lookup"><span data-stu-id="2d242-143">Link</span></span>          | <span data-ttu-id="2d242-144">Slóð og texti tengils</span><span class="sxs-lookup"><span data-stu-id="2d242-144">Link URL and link text</span></span> | <span data-ttu-id="2d242-145">Hægt er að bæta við tengli í textann til að beina notendum á ákveðna síðu.</span><span class="sxs-lookup"><span data-stu-id="2d242-145">A link can be added to the text to redirect users to a specific page.</span></span> |
| <span data-ttu-id="2d242-146">Stærð reits</span><span class="sxs-lookup"><span data-stu-id="2d242-146">Tile size</span></span>     | <span data-ttu-id="2d242-147">Tölugildi frá **1** til og með **12**</span><span class="sxs-lookup"><span data-stu-id="2d242-147">A number from **1** through **12**</span></span> | <span data-ttu-id="2d242-148">Fyrir hvern efnisstaðsetningarlið skilgreinir þessi eiginleiki fjölda hólfa sem hluturinn ætti að fylla út í staðsetningareiningu efnis.</span><span class="sxs-lookup"><span data-stu-id="2d242-148">For each content placement item, this property defines the number of slots that the item should fill in the content placement module.</span></span> <span data-ttu-id="2d242-149">Hámarksstærð staðsetningareiningar efnis er 12 hólf.</span><span class="sxs-lookup"><span data-stu-id="2d242-149">The maximum size of the content placement module is 12 slots.</span></span> <span data-ttu-id="2d242-150">Ef heildarreitastærðin fyrir fyrstu *n* hlutina í staðsetningraeiningu efnis fer yfir 12 hólf er hlutirnir eru pakkaðir í næstu röð.</span><span class="sxs-lookup"><span data-stu-id="2d242-150">If the total tile size for the first *n* items in the content placement module exceeds 12 slots, the items are wrapped to the next row.</span></span> |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a><span data-ttu-id="2d242-151">Bæta við staðsetningareiningu efnis sem inniheldur staðsetningarliðareiningu efnis á síðu</span><span class="sxs-lookup"><span data-stu-id="2d242-151">Add a content placement module that contains a content placement item module to a page</span></span>

<span data-ttu-id="2d242-152">Fylgdu þessum skrefum til að bæta við staðsetningareiningu efnis sem inniheldur staðsetningarliðareiginleika efnis á nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="2d242-152">To add a content placement module that contains a content placement item module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="2d242-153">Búðu til sniðmát sem heitir **sniðmát efnisstaðsetningar**.</span><span class="sxs-lookup"><span data-stu-id="2d242-153">Create a template that is named **content placement template**.</span></span>
1. <span data-ttu-id="2d242-154">Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við staðsetningareiningu efnis.</span><span class="sxs-lookup"><span data-stu-id="2d242-154">In the **Main** slot of the default page, add a content placement module.</span></span>
1. <span data-ttu-id="2d242-155">Í staðsetningareiningu efnis bætirðu við staðsetningarliðareiningu efnis.</span><span class="sxs-lookup"><span data-stu-id="2d242-155">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="2d242-156">Skráðu brotið út í sniðmátinu og birtu það.</span><span class="sxs-lookup"><span data-stu-id="2d242-156">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="2d242-157">Notaðu efnisstaðsetningarsniðmátið sem þú bjóst til til að búa til síðu sem heitir **Efnisstaðsetningarsíða**.</span><span class="sxs-lookup"><span data-stu-id="2d242-157">Use the content placement template that you just created to create a page that is named **Content placement page**.</span></span>
1. <span data-ttu-id="2d242-158">Í hólfinu **Aðal** á nýju síðunni bætirðu við staðsetningareiningu efnis.</span><span class="sxs-lookup"><span data-stu-id="2d242-158">In the **Main** slot of the new page, add a content placement module.</span></span>
1. <span data-ttu-id="2d242-159">Í staðsetningareiningu efnis bætirðu við staðsetningarliðareiningu efnis.</span><span class="sxs-lookup"><span data-stu-id="2d242-159">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="2d242-160">Í eiginleikaglugganum fyrir einingu staðsetningarliðar efnis velurðu mynd, bætir við fyrirsögn, bætir við málsgrein, bætir við tengli, setur slóð fyrir tengilinn og stillir stærð reitar á **6**.</span><span class="sxs-lookup"><span data-stu-id="2d242-160">In the property pane for the content placement item module, select an image, add a heading, add a paragraph, add a link, set the link URL, and set the tile size to **6**.</span></span>
1. <span data-ttu-id="2d242-161">Endurtaktu skref 7 og 8 til að bæta við annarri einingu fyrir vistun efnis sem hefur sömu reitastærð.</span><span class="sxs-lookup"><span data-stu-id="2d242-161">Repeat steps 7 and 8 to add another content placement item module that has the same tile size.</span></span>
1. <span data-ttu-id="2d242-162">Vistaðu og forskoðaðu síðuna.</span><span class="sxs-lookup"><span data-stu-id="2d242-162">Save and preview the page.</span></span> <span data-ttu-id="2d242-163">Þú ættir að sjá tvo efnisstaðsetningarliði sem birtast hlið við hlið.</span><span class="sxs-lookup"><span data-stu-id="2d242-163">You should see two content placement items that appear side by side.</span></span> <span data-ttu-id="2d242-164">Þú getur breytt eiginleikanum **Reitastærð** fyrir hverja staðsetningareiningu efnis eða bætt við fleiri einingum til að ná tilætluðu skipulagi.</span><span class="sxs-lookup"><span data-stu-id="2d242-164">You can adjust the **Tile size** property of each content placement item module or add more modules to achieve the desired layout.</span></span>
1. <span data-ttu-id="2d242-165">Athuga á síðunni og birtu hana.</span><span class="sxs-lookup"><span data-stu-id="2d242-165">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2d242-166">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="2d242-166">Additional resources</span></span>

[<span data-ttu-id="2d242-167">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="2d242-167">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2d242-168">Viðvörunareining</span><span class="sxs-lookup"><span data-stu-id="2d242-168">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="2d242-169">Myndaræmueining</span><span class="sxs-lookup"><span data-stu-id="2d242-169">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="2d242-170">Eining með fjölbreyttu efni</span><span class="sxs-lookup"><span data-stu-id="2d242-170">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="2d242-171">Eiginleikaeining</span><span class="sxs-lookup"><span data-stu-id="2d242-171">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="2d242-172">Hetjueining</span><span class="sxs-lookup"><span data-stu-id="2d242-172">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="2d242-173">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="2d242-173">Video player module</span></span>](add-video-player.md)
