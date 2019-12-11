---
title: Eining með fjölbreyttu efni
description: Þetta efni fjallar um einingar með fjölbreyttu efni og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785422"
---
# <a name="content-rich-block-module"></a><span data-ttu-id="339a2-103">Eining með fjölbreyttu efni</span><span class="sxs-lookup"><span data-stu-id="339a2-103">Content rich block module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="339a2-104">Þetta efni fjallar um einingar með fjölbreyttu efni og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="339a2-104">This topic covers content rich block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="339a2-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="339a2-105">Overview</span></span>

<span data-ttu-id="339a2-106">Eining með fjölbreyttu efni er sérstakur gámur sem hægt er að setja eina eða fleiri einingar með fjölbreyttu efni í.</span><span class="sxs-lookup"><span data-stu-id="339a2-106">A content rich block module is a special container that one or more content rich block items can be put inside.</span></span> <span data-ttu-id="339a2-107">Einingar með fjölbreyttu efni eru notaðar fyrir textaefni á síðu.</span><span class="sxs-lookup"><span data-stu-id="339a2-107">Content rich block modules are used for textual content on a page.</span></span> <span data-ttu-id="339a2-108">Þetta efni getur verið annaðhvort upplýsandi eða kynningar.</span><span class="sxs-lookup"><span data-stu-id="339a2-108">This content can be either informational or promotional.</span></span>

<span data-ttu-id="339a2-109">Einingar með fjölbreyttu efni eru knúnar af gögnum frá efnisstýringarkerfinu (CMS) og hægt er að setja þær á hvaða síðu sem er.</span><span class="sxs-lookup"><span data-stu-id="339a2-109">Content rich block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="339a2-110">Þær eru sjálfstæðar einingar sem eru ekki háðar síðusamhengi eða neinum öðrum einingum.</span><span class="sxs-lookup"><span data-stu-id="339a2-110">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a><span data-ttu-id="339a2-111">Dæmi um einingar með fjölbreyttu efni í rafrænum viðskiptum</span><span class="sxs-lookup"><span data-stu-id="339a2-111">Examples of content rich block modules in e-Commerce</span></span>

<span data-ttu-id="339a2-112">Hægt er að nota einingar með fjölbreyttu efni á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="339a2-112">Content rich block modules can be used in the following ways:</span></span>

* <span data-ttu-id="339a2-113">Til að sýna fram á eiginleika vöru á vöruupplýsingasíðu.</span><span class="sxs-lookup"><span data-stu-id="339a2-113">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="339a2-114">Til upplýsinga á hvaða síðu sem er.</span><span class="sxs-lookup"><span data-stu-id="339a2-114">For informational purposes on any page.</span></span> <span data-ttu-id="339a2-115">Til dæmis geta þeir útskýrt ávinninginn af vildarkerfum, lýst stefnumótun um sendingu og til baka, svarað algengum spurningum eða gefið „um okkur“ efni.</span><span class="sxs-lookup"><span data-stu-id="339a2-115">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="339a2-116">Til að bæta við sérsniðnum skilaboðum á upplýsingasíðu.</span><span class="sxs-lookup"><span data-stu-id="339a2-116">To add custom messages on a product details page.</span></span> <span data-ttu-id="339a2-117">(til dæmis „Ókeypis sending fyrir pantanir yfir $50“).</span><span class="sxs-lookup"><span data-stu-id="339a2-117">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="339a2-118">Fyrir fyrirvara og samskiptaupplýsingar á vöruupplýsingasíðum, körfusíðum, kassasíðum og öðrum síðum (til dæmis „Sendingar og skil falla undir verslunarstefnu“).</span><span class="sxs-lookup"><span data-stu-id="339a2-118">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="content-rich-block-module-properties"></a><span data-ttu-id="339a2-119">Eiginleikar einingar með fjölbreyttu efni</span><span class="sxs-lookup"><span data-stu-id="339a2-119">Content rich block module properties</span></span>

| <span data-ttu-id="339a2-120">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="339a2-120">Property name</span></span>     | <span data-ttu-id="339a2-121">Virði</span><span class="sxs-lookup"><span data-stu-id="339a2-121">Value</span></span>                                 | <span data-ttu-id="339a2-122">Eiginleiki</span><span class="sxs-lookup"><span data-stu-id="339a2-122">Property</span></span> |
|-------------------|---------------------------------------|----------|
| <span data-ttu-id="339a2-123">Fjöldi dálka</span><span class="sxs-lookup"><span data-stu-id="339a2-123">Number of columns</span></span> | <span data-ttu-id="339a2-124">Tölugildi frá **1** til og með **4**</span><span class="sxs-lookup"><span data-stu-id="339a2-124">A number from **1** through **4**</span></span>     | <span data-ttu-id="339a2-125">Fjöldi dálka í bálki með fjölbreyttu efni.</span><span class="sxs-lookup"><span data-stu-id="339a2-125">The number of columns in the content rich block.</span></span> <span data-ttu-id="339a2-126">Það geta verið allt að fjórir dálkar.</span><span class="sxs-lookup"><span data-stu-id="339a2-126">There can be up to four columns.</span></span> |
| <span data-ttu-id="339a2-127">Breidd</span><span class="sxs-lookup"><span data-stu-id="339a2-127">Width</span></span>             | <span data-ttu-id="339a2-128">**Fylla gám** eða **Fylla skjáinn**</span><span class="sxs-lookup"><span data-stu-id="339a2-128">**Fill container** or **Fill screen**</span></span> | <span data-ttu-id="339a2-129">Ef gildi er stillt á **Fylla gám** eru hlutirnir í gámnum takmarkaðir við breidd gámsins.</span><span class="sxs-lookup"><span data-stu-id="339a2-129">If the value is set to **Fill container**, the items inside the container are restricted to the width of the container.</span></span> <span data-ttu-id="339a2-130">Ef gildi er stillt á **Fylla skjáinn** eru atriðin takmörkuð við breidd gámsins en geta farið í stillingar fyrir allan skjáinn.</span><span class="sxs-lookup"><span data-stu-id="339a2-130">If the value is set to **Fill screen**, the items aren't restricted to the container width but can go into full-screen mode.</span></span> <span data-ttu-id="339a2-131">Þú getur breytt gildi til að ná tilætluðu útliti.</span><span class="sxs-lookup"><span data-stu-id="339a2-131">You can change the value to achieve the desired layout.</span></span> |

## <a name="content-rich-block-item-module-properties"></a><span data-ttu-id="339a2-132">Eiginleikar einingar bálkaliðar með fjölbreyttu efni</span><span class="sxs-lookup"><span data-stu-id="339a2-132">Content rich block item module properties</span></span>

| <span data-ttu-id="339a2-133">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="339a2-133">Property name</span></span> | <span data-ttu-id="339a2-134">Virði</span><span class="sxs-lookup"><span data-stu-id="339a2-134">Value</span></span>          | <span data-ttu-id="339a2-135">Lýsing</span><span class="sxs-lookup"><span data-stu-id="339a2-135">Description</span></span> |
|---------------|----------------|-------------|
| <span data-ttu-id="339a2-136">Efnisgrein</span><span class="sxs-lookup"><span data-stu-id="339a2-136">Paragraph</span></span>     | <span data-ttu-id="339a2-137">Texti efnisgreinar</span><span class="sxs-lookup"><span data-stu-id="339a2-137">Paragraph text</span></span> | <span data-ttu-id="339a2-138">Textinn sem fylgir sérhverjum dálkalið með fjölbreyttu efni.</span><span class="sxs-lookup"><span data-stu-id="339a2-138">The text that accompanies each content rich block item.</span></span> <span data-ttu-id="339a2-139">Stuðningur er við nokkra grunntextaeiginleika, eins og feitletrun, undirstrikun og skáletrun texta.</span><span class="sxs-lookup"><span data-stu-id="339a2-139">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |

## <a name="add-a-content-rich-block-module-to-a-page"></a><span data-ttu-id="339a2-140">Bæta við einingu með fjölbreyttu efni á síðu</span><span class="sxs-lookup"><span data-stu-id="339a2-140">Add a content rich block module to a page</span></span>

<span data-ttu-id="339a2-141">Fylgdu þessum skrefum til að bæta einingu bálks með fjölbreyttu efni við nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="339a2-141">To add a content rich block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="339a2-142">Búðu til síðusniðmát sem heitir **Efnissniðmát**.</span><span class="sxs-lookup"><span data-stu-id="339a2-142">Create a page template that is named **Content template**.</span></span>
1. <span data-ttu-id="339a2-143">Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við einingu bálks með fjölbreyttu efni.</span><span class="sxs-lookup"><span data-stu-id="339a2-143">In the **Main** slot of the default page, add a content rich block module.</span></span>
1. <span data-ttu-id="339a2-144">Skráðu brotið út í sniðmátinu og birtu það.</span><span class="sxs-lookup"><span data-stu-id="339a2-144">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="339a2-145">Notaðu efnissniðmátið sem þú bjóst til til að búa til síðu sem heitir **Efnissíða**.</span><span class="sxs-lookup"><span data-stu-id="339a2-145">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="339a2-146">Í hólfinu **Aðal** á nýju síðunni bætirðu við einingu bálks með fjölbreyttu efni.</span><span class="sxs-lookup"><span data-stu-id="339a2-146">In the **Main** slot of the new page, add a content rich block module.</span></span>
1. <span data-ttu-id="339a2-147">Í eiginleikum einingar bálks með fjölbreyttu efni skaltu stilla fjölda dálka á **2**.</span><span class="sxs-lookup"><span data-stu-id="339a2-147">In the properties of the content rich block module, set number of columns to **2**.</span></span>
1. <span data-ttu-id="339a2-148">Í einingu bálks með fjölbreyttu efni velurðu **Bæta við einingu** og bætir við dálkalið með fjölbreyttu efni (til dæmis, **item1**).</span><span class="sxs-lookup"><span data-stu-id="339a2-148">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item1**).</span></span>
1. <span data-ttu-id="339a2-149">Bættu við efnisgreinatexta í nýja bálkalið með fjölbreyttu efni.</span><span class="sxs-lookup"><span data-stu-id="339a2-149">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="339a2-150">Í einingu bálks með fjölbreyttu efni velurðu **Bæta við einingu** og bætir við dálkalið með fjölbreyttu efni (til dæmis, **item2**).</span><span class="sxs-lookup"><span data-stu-id="339a2-150">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item2**).</span></span>
1. <span data-ttu-id="339a2-151">Bættu við efnisgreinatexta í nýja bálkalið með fjölbreyttu efni.</span><span class="sxs-lookup"><span data-stu-id="339a2-151">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="339a2-152">Vistaðu síðuna og forskoðaðu breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="339a2-152">Save the page, and preview the changes.</span></span> <span data-ttu-id="339a2-153">Þú ættir að sjá tvær sniðnar textablokkir í tveggja dálka mynd.</span><span class="sxs-lookup"><span data-stu-id="339a2-153">You should see two rich text blocks in a two-column view.</span></span>
1. <span data-ttu-id="339a2-154">Athuga á síðunni og birtu hana.</span><span class="sxs-lookup"><span data-stu-id="339a2-154">Check in the page, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="339a2-155">Ef þú bætir við þriðja sniðna reitnum fyrir efnið verður það staflað fyrir neðan þá tvo hluti sem þú bætir við áður.</span><span class="sxs-lookup"><span data-stu-id="339a2-155">If you add a third content rich block item, it will be stacked below the two items that you previously added.</span></span> <span data-ttu-id="339a2-156">Með því að breyta fjölda dálka og atriða í gámnum geturðu náð mismunandi skipulagi fyrir textaefni.</span><span class="sxs-lookup"><span data-stu-id="339a2-156">By changing the number of columns and items in the container, you can achieve different layouts for textual content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="339a2-157">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="339a2-157">Additional resources</span></span>

[<span data-ttu-id="339a2-158">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="339a2-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="339a2-159">Viðvörunareining</span><span class="sxs-lookup"><span data-stu-id="339a2-159">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="339a2-160">Myndaræmueining</span><span class="sxs-lookup"><span data-stu-id="339a2-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="339a2-161">Staðsetningareining efnis</span><span class="sxs-lookup"><span data-stu-id="339a2-161">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="339a2-162">Eiginleikaeining</span><span class="sxs-lookup"><span data-stu-id="339a2-162">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="339a2-163">Hetjueining</span><span class="sxs-lookup"><span data-stu-id="339a2-163">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="339a2-164">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="339a2-164">Video player module</span></span>](add-video-player.md)

