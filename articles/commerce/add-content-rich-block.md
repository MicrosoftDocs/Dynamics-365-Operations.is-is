---
title: Textabálkseining
description: Þetta efni fjallar um textabálkseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025598"
---
# <a name="text-block-module"></a><span data-ttu-id="3447c-103">Textabálkseining</span><span class="sxs-lookup"><span data-stu-id="3447c-103">Text block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3447c-104">Þetta efni fjallar um textabálkseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3447c-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3447c-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="3447c-105">Overview</span></span>

<span data-ttu-id="3447c-106">Textabálkseining er eining sem er notuð til að bæta við textainnihaldi.</span><span class="sxs-lookup"><span data-stu-id="3447c-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="3447c-107">Þetta efni getur verið upplýsandi eða kynningar.</span><span class="sxs-lookup"><span data-stu-id="3447c-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="3447c-108">Textabálkseiningar eru knúnar af gögnum frá efnisstýringarkerfinu (CMS) og hægt er að setja þær á hvaða síðu sem er.</span><span class="sxs-lookup"><span data-stu-id="3447c-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="3447c-109">Þær eru sjálfstæðar einingar sem eru ekki háðar síðusamhengi eða neinum öðrum einingum.</span><span class="sxs-lookup"><span data-stu-id="3447c-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="3447c-110">Dæmi um textabálkseiningar í rafrænum viðskiptum</span><span class="sxs-lookup"><span data-stu-id="3447c-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="3447c-111">Hægt er að nota textabálkseiningar á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="3447c-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="3447c-112">Til að sýna fram á eiginleika vöru á vöruupplýsingasíðu.</span><span class="sxs-lookup"><span data-stu-id="3447c-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="3447c-113">Til upplýsinga á hvaða síðu sem er.</span><span class="sxs-lookup"><span data-stu-id="3447c-113">For informational purposes on any page.</span></span> <span data-ttu-id="3447c-114">Til dæmis geta þeir útskýrt ávinninginn af vildarkerfum, lýst stefnumótun um sendingu og til baka, svarað algengum spurningum eða gefið „um okkur“ efni.</span><span class="sxs-lookup"><span data-stu-id="3447c-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="3447c-115">Til að bæta við sérsniðnum skilaboðum á upplýsingasíðu.</span><span class="sxs-lookup"><span data-stu-id="3447c-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="3447c-116">(til dæmis „Ókeypis sending fyrir pantanir yfir $50“).</span><span class="sxs-lookup"><span data-stu-id="3447c-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="3447c-117">Fyrir fyrirvara og samskiptaupplýsingar á vöruupplýsingasíðum, körfusíðum, kassasíðum og öðrum síðum (til dæmis „Sendingar og skil falla undir verslunarstefnu“).</span><span class="sxs-lookup"><span data-stu-id="3447c-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="text-block-module-properties"></a><span data-ttu-id="3447c-118">Eiginleikar textabálkseiningar</span><span class="sxs-lookup"><span data-stu-id="3447c-118">Text block module properties</span></span>

| <span data-ttu-id="3447c-119">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="3447c-119">Property name</span></span>     | <span data-ttu-id="3447c-120">Value</span><span class="sxs-lookup"><span data-stu-id="3447c-120">Value</span></span>                                            | <span data-ttu-id="3447c-121">Lýsing</span><span class="sxs-lookup"><span data-stu-id="3447c-121">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="3447c-122">RTF-snið</span><span class="sxs-lookup"><span data-stu-id="3447c-122">Rich text</span></span>         | <span data-ttu-id="3447c-123">RTF-snið</span><span class="sxs-lookup"><span data-stu-id="3447c-123">Rich text</span></span>                                        | <span data-ttu-id="3447c-124">Texti efnisgreinar.</span><span class="sxs-lookup"><span data-stu-id="3447c-124">Paragraph text.</span></span> <span data-ttu-id="3447c-125">Stuðningur er við nokkra grunntextaeiginleika, eins og feitletrun, undirstrikun og skáletrun texta.</span><span class="sxs-lookup"><span data-stu-id="3447c-125">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="3447c-126">Sérsniðið heiti klasa</span><span class="sxs-lookup"><span data-stu-id="3447c-126">Custom class name</span></span> | <span data-ttu-id="3447c-127">Klasaheiti Cascading Style Sheets (CSS)</span><span class="sxs-lookup"><span data-stu-id="3447c-127">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="3447c-128">Heiti sérsniðins CSS-klasa sem forritari veitir til að forsníða þessa einingu.</span><span class="sxs-lookup"><span data-stu-id="3447c-128">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="3447c-129">Skilgreina ætti klasaheitið í þemapakkanum.</span><span class="sxs-lookup"><span data-stu-id="3447c-129">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="3447c-130">Leturtærð</span><span class="sxs-lookup"><span data-stu-id="3447c-130">Font size</span></span>         | <span data-ttu-id="3447c-131">**Lítil**, **Miðlungs**, **Stór** eða **X-stór**</span><span class="sxs-lookup"><span data-stu-id="3447c-131">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="3447c-132">Leturstærð fyrir innihaldið.</span><span class="sxs-lookup"><span data-stu-id="3447c-132">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="3447c-133">Bæta við textabálkseiningu á síðu</span><span class="sxs-lookup"><span data-stu-id="3447c-133">Add a text block module to a page</span></span>

<span data-ttu-id="3447c-134">Fylgdu þessum skrefum til að bæta textabálkseiningu við nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="3447c-134">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="3447c-135">Búðu til síðusniðmát sem heitir **Efnissniðmát**.</span><span class="sxs-lookup"><span data-stu-id="3447c-135">Create a page template that is named **Content template**.</span></span> 
1. <span data-ttu-id="3447c-136">Í hólfinu **Meginmál** bætirðu við einingunni **Sjálfgefin síða**.</span><span class="sxs-lookup"><span data-stu-id="3447c-136">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="3447c-137">Ljúktu við að breyta sniðmátinu, vistaðu það og birtu.</span><span class="sxs-lookup"><span data-stu-id="3447c-137">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="3447c-138">Notaðu efnissniðmátið sem þú bjóst til til að búa til síðu sem heitir **Efnissíða**.</span><span class="sxs-lookup"><span data-stu-id="3447c-138">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="3447c-139">Í hólfinu **Aðal** á nýju síðunni bætirðu við gámaeiningu.</span><span class="sxs-lookup"><span data-stu-id="3447c-139">In the **Main** slot of the new page, add a container module.</span></span>
1. <span data-ttu-id="3447c-140">Í eiginleikaglugganum fyrir gámaeininguna stillirðu eiginleikann **Breidd** á **Fylla gám**.</span><span class="sxs-lookup"><span data-stu-id="3447c-140">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="3447c-141">Bættu textabálkseiningu við gámaeininguna.</span><span class="sxs-lookup"><span data-stu-id="3447c-141">Add a text block module to the container module.</span></span> 
1. <span data-ttu-id="3447c-142">Í eiginleikaglugga textabálkseiningarinnar bætirðu texta við í reitinn **Mótaður texti**.</span><span class="sxs-lookup"><span data-stu-id="3447c-142">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="3447c-143">Ljúktu við að breyta síðunni, vistaðu hana og birtu.</span><span class="sxs-lookup"><span data-stu-id="3447c-143">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3447c-144">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="3447c-144">Additional resources</span></span>

[<span data-ttu-id="3447c-145">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="3447c-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3447c-146">Kynningarborðaeining</span><span class="sxs-lookup"><span data-stu-id="3447c-146">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="3447c-147">Myndaræmueining</span><span class="sxs-lookup"><span data-stu-id="3447c-147">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="3447c-148">Innihaldsbálkseining</span><span class="sxs-lookup"><span data-stu-id="3447c-148">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="3447c-149">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="3447c-149">Video player module</span></span>](add-video-player.md)

