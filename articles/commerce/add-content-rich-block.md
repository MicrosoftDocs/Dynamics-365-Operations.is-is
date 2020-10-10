---
title: Textabálkseining
description: Þetta efni fjallar um textabálkseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: c6527ad00e74fa105f3873036eb56557b98b05aa
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817379"
---
# <a name="text-block-module"></a><span data-ttu-id="be3c1-103">Textabálkseining</span><span class="sxs-lookup"><span data-stu-id="be3c1-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="be3c1-104">Þetta efni fjallar um textabálkseiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="be3c1-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="be3c1-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="be3c1-105">Overview</span></span>

<span data-ttu-id="be3c1-106">Textabálkseining er eining sem er notuð til að bæta við textainnihaldi.</span><span class="sxs-lookup"><span data-stu-id="be3c1-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="be3c1-107">Þetta efni getur verið upplýsandi eða kynningar.</span><span class="sxs-lookup"><span data-stu-id="be3c1-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="be3c1-108">Textabálkseiningar eru knúnar af gögnum frá efnisstýringarkerfinu (CMS) og hægt er að setja þær á hvaða síðu sem er.</span><span class="sxs-lookup"><span data-stu-id="be3c1-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="be3c1-109">Þær eru sjálfstæðar einingar sem eru ekki háðar síðusamhengi eða neinum öðrum einingum.</span><span class="sxs-lookup"><span data-stu-id="be3c1-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="be3c1-110">Dæmi um textabálkseiningar í rafrænum viðskiptum</span><span class="sxs-lookup"><span data-stu-id="be3c1-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="be3c1-111">Hægt er að nota textabálkseiningar á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="be3c1-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="be3c1-112">Til að sýna fram á eiginleika vöru á vöruupplýsingasíðu.</span><span class="sxs-lookup"><span data-stu-id="be3c1-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="be3c1-113">Til upplýsinga á hvaða síðu sem er.</span><span class="sxs-lookup"><span data-stu-id="be3c1-113">For informational purposes on any page.</span></span> <span data-ttu-id="be3c1-114">Til dæmis geta þeir útskýrt ávinninginn af vildarkerfum, lýst stefnumótun um sendingu og til baka, svarað algengum spurningum eða gefið „um okkur“ efni.</span><span class="sxs-lookup"><span data-stu-id="be3c1-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="be3c1-115">Til að bæta við sérsniðnum skilaboðum á upplýsingasíðu.</span><span class="sxs-lookup"><span data-stu-id="be3c1-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="be3c1-116">(til dæmis „Ókeypis sending fyrir pantanir yfir $50“).</span><span class="sxs-lookup"><span data-stu-id="be3c1-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="be3c1-117">Fyrir fyrirvara og samskiptaupplýsingar á vöruupplýsingasíðum, körfusíðum, kassasíðum og öðrum síðum (til dæmis „Sendingar og skil falla undir verslunarstefnu“).</span><span class="sxs-lookup"><span data-stu-id="be3c1-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="be3c1-118">Eftirfarandi mynd sýnir dæmi um textabálkseiningu sem er notuð á heimasíðu.</span><span class="sxs-lookup"><span data-stu-id="be3c1-118">The following image shows an example of a text block module that is used on a home page.</span></span>

![Dæmi um einingu textabálks](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="be3c1-120">Eiginleikar textabálkseiningar</span><span class="sxs-lookup"><span data-stu-id="be3c1-120">Text block module properties</span></span>

| <span data-ttu-id="be3c1-121">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="be3c1-121">Property name</span></span>     | <span data-ttu-id="be3c1-122">Virði</span><span class="sxs-lookup"><span data-stu-id="be3c1-122">Value</span></span>                                            | <span data-ttu-id="be3c1-123">lýsing</span><span class="sxs-lookup"><span data-stu-id="be3c1-123">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="be3c1-124">RTF-snið</span><span class="sxs-lookup"><span data-stu-id="be3c1-124">Rich text</span></span>         | <span data-ttu-id="be3c1-125">RTF-snið</span><span class="sxs-lookup"><span data-stu-id="be3c1-125">Rich text</span></span>                                        | <span data-ttu-id="be3c1-126">Texti efnisgreinar.</span><span class="sxs-lookup"><span data-stu-id="be3c1-126">Paragraph text.</span></span> <span data-ttu-id="be3c1-127">Stuðningur er við nokkra grunntextaeiginleika, eins og feitletrun, undirstrikun og skáletrun texta.</span><span class="sxs-lookup"><span data-stu-id="be3c1-127">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="be3c1-128">Sérsniðið heiti klasa</span><span class="sxs-lookup"><span data-stu-id="be3c1-128">Custom class name</span></span> | <span data-ttu-id="be3c1-129">Klasaheiti Cascading Style Sheets (CSS)</span><span class="sxs-lookup"><span data-stu-id="be3c1-129">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="be3c1-130">Heiti sérsniðins CSS-klasa sem forritari veitir til að forsníða þessa einingu.</span><span class="sxs-lookup"><span data-stu-id="be3c1-130">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="be3c1-131">Skilgreina ætti klasaheitið í þemapakkanum.</span><span class="sxs-lookup"><span data-stu-id="be3c1-131">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="be3c1-132">Leturtærð</span><span class="sxs-lookup"><span data-stu-id="be3c1-132">Font size</span></span>         | <span data-ttu-id="be3c1-133">**Lítil**, **Miðlungs**, **Stór** eða **X-stór**</span><span class="sxs-lookup"><span data-stu-id="be3c1-133">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="be3c1-134">Leturstærð fyrir innihaldið.</span><span class="sxs-lookup"><span data-stu-id="be3c1-134">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="be3c1-135">Bæta við textabálkseiningu á síðu</span><span class="sxs-lookup"><span data-stu-id="be3c1-135">Add a text block module to a page</span></span>

<span data-ttu-id="be3c1-136">Fylgdu þessum skrefum til að bæta textabálkseiningu við nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="be3c1-136">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="be3c1-137">Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="be3c1-137">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="be3c1-138">Í svarglugganum **Nýtt sniðmát**, undir **Heiti sniðmáts**, skal slá inn **Efnissniðmát**.</span><span class="sxs-lookup"><span data-stu-id="be3c1-138">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="be3c1-139">Í hólfinu **Meginmál**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="be3c1-139">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="be3c1-140">Í glugganum **Bæta við einingu** skal velja eininguna **Sjálfgefin síða** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="be3c1-140">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="be3c1-141">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="be3c1-141">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="be3c1-142">Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.</span><span class="sxs-lookup"><span data-stu-id="be3c1-142">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="be3c1-143">Í svarglugganum **Velja sniðmát** skal velja **Efnissniðmát**.</span><span class="sxs-lookup"><span data-stu-id="be3c1-143">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="be3c1-144">Undir **Síðuheiti** skal færa inn **Efnissíða** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="be3c1-144">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="be3c1-145">Í hólfinu **Aðalsvæði** á nýju síðunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="be3c1-145">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="be3c1-146">Í glugganum **Bæta við einingu** skal velja eininguna **Hólf** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="be3c1-146">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="be3c1-147">Í eiginleikaglugganum fyrir gámaeininguna stillirðu eiginleikann **Breidd** á **Fylla gám**.</span><span class="sxs-lookup"><span data-stu-id="be3c1-147">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="be3c1-148">Í hólfinu **Hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="be3c1-148">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="be3c1-149">Í glugganum **Bæta við einingu** skal velja eininguna **Textabálkur** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="be3c1-149">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="be3c1-150">Í eiginleikaglugga textabálkseiningarinnar bætirðu texta við í reitinn **Mótaður texti**.</span><span class="sxs-lookup"><span data-stu-id="be3c1-150">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="be3c1-151">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="be3c1-151">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="be3c1-152">Veldu**Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="be3c1-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be3c1-153">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="be3c1-153">Additional resources</span></span>

[<span data-ttu-id="be3c1-154">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="be3c1-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="be3c1-155">Tilboðsborðaeining</span><span class="sxs-lookup"><span data-stu-id="be3c1-155">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="be3c1-156">Myndaræmueining</span><span class="sxs-lookup"><span data-stu-id="be3c1-156">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="be3c1-157">Eining fyrir bálk með efni</span><span class="sxs-lookup"><span data-stu-id="be3c1-157">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="be3c1-158">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="be3c1-158">Video player module</span></span>](add-video-player.md)

