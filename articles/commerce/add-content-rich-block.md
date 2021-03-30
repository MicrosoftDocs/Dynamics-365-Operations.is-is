---
title: Textabálkseining
description: Þetta efni fjallar um textabálkaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
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
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3926f23e4e762a49ef94ef0c8f3291e7e9a4a6a2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206392"
---
# <a name="text-block-module"></a><span data-ttu-id="021d1-103">Textabálkseining</span><span class="sxs-lookup"><span data-stu-id="021d1-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="021d1-104">Þetta efni fjallar um textabálkaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="021d1-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="021d1-105">Textabálkseining er eining sem er notuð til að bæta við textainnihaldi.</span><span class="sxs-lookup"><span data-stu-id="021d1-105">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="021d1-106">Þetta efni getur verið upplýsandi eða kynningar.</span><span class="sxs-lookup"><span data-stu-id="021d1-106">This content can be informational or promotional.</span></span>

<span data-ttu-id="021d1-107">Textabálkseiningar eru knúnar af gögnum frá efnisstýringarkerfinu (CMS) og hægt er að setja þær á hvaða síðu sem er.</span><span class="sxs-lookup"><span data-stu-id="021d1-107">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="021d1-108">Þær eru sjálfstæðar einingar sem eru ekki háðar síðusamhengi eða neinum öðrum einingum.</span><span class="sxs-lookup"><span data-stu-id="021d1-108">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="021d1-109">Dæmi um textabálkseiningar í rafrænum viðskiptum</span><span class="sxs-lookup"><span data-stu-id="021d1-109">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="021d1-110">Hægt er að nota textabálkseiningar á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="021d1-110">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="021d1-111">Til að sýna fram á eiginleika vöru á vöruupplýsingasíðu.</span><span class="sxs-lookup"><span data-stu-id="021d1-111">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="021d1-112">Til upplýsinga á hvaða síðu sem er.</span><span class="sxs-lookup"><span data-stu-id="021d1-112">For informational purposes on any page.</span></span> <span data-ttu-id="021d1-113">Til dæmis geta þeir útskýrt ávinninginn af vildarkerfum, lýst stefnumótun um sendingu og til baka, svarað algengum spurningum eða gefið „um okkur“ efni.</span><span class="sxs-lookup"><span data-stu-id="021d1-113">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="021d1-114">Til að bæta við sérsniðnum skilaboðum á upplýsingasíðu.</span><span class="sxs-lookup"><span data-stu-id="021d1-114">To add custom messages on a product details page.</span></span> <span data-ttu-id="021d1-115">(til dæmis „Ókeypis sending fyrir pantanir yfir $50“).</span><span class="sxs-lookup"><span data-stu-id="021d1-115">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="021d1-116">Fyrir fyrirvara og samskiptaupplýsingar á vöruupplýsingasíðum, körfusíðum, kassasíðum og öðrum síðum (til dæmis „Sendingar og skil falla undir verslunarstefnu“).</span><span class="sxs-lookup"><span data-stu-id="021d1-116">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="021d1-117">Eftirfarandi mynd sýnir dæmi um textabálkseiningu sem er notuð á heimasíðu.</span><span class="sxs-lookup"><span data-stu-id="021d1-117">The following image shows an example of a text block module that is used on a home page.</span></span>

![Dæmi um einingu textabálks](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="021d1-119">Eiginleikar textabálkseiningar</span><span class="sxs-lookup"><span data-stu-id="021d1-119">Text block module properties</span></span>

| <span data-ttu-id="021d1-120">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="021d1-120">Property name</span></span>     | <span data-ttu-id="021d1-121">Virði</span><span class="sxs-lookup"><span data-stu-id="021d1-121">Value</span></span>                                            | <span data-ttu-id="021d1-122">lýsing</span><span class="sxs-lookup"><span data-stu-id="021d1-122">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="021d1-123">RTF-snið</span><span class="sxs-lookup"><span data-stu-id="021d1-123">Rich text</span></span>         | <span data-ttu-id="021d1-124">RTF-snið</span><span class="sxs-lookup"><span data-stu-id="021d1-124">Rich text</span></span>                                        | <span data-ttu-id="021d1-125">Texti efnisgreinar.</span><span class="sxs-lookup"><span data-stu-id="021d1-125">Paragraph text.</span></span> <span data-ttu-id="021d1-126">Stuðningur er við nokkra grunntextaeiginleika, eins og feitletrun, undirstrikun og skáletrun texta.</span><span class="sxs-lookup"><span data-stu-id="021d1-126">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="021d1-127">Sérsniðið heiti klasa</span><span class="sxs-lookup"><span data-stu-id="021d1-127">Custom class name</span></span> | <span data-ttu-id="021d1-128">Klasaheiti Cascading Style Sheets (CSS)</span><span class="sxs-lookup"><span data-stu-id="021d1-128">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="021d1-129">Heiti sérsniðins CSS-klasa sem forritari veitir til að forsníða þessa einingu.</span><span class="sxs-lookup"><span data-stu-id="021d1-129">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="021d1-130">Skilgreina ætti klasaheitið í þemapakkanum.</span><span class="sxs-lookup"><span data-stu-id="021d1-130">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="021d1-131">Leturtærð</span><span class="sxs-lookup"><span data-stu-id="021d1-131">Font size</span></span>         | <span data-ttu-id="021d1-132">**Lítil**, **Miðlungs**, **Stór** eða **X-stór**</span><span class="sxs-lookup"><span data-stu-id="021d1-132">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="021d1-133">Leturstærð fyrir innihaldið.</span><span class="sxs-lookup"><span data-stu-id="021d1-133">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="021d1-134">Bæta við textabálkseiningu á síðu</span><span class="sxs-lookup"><span data-stu-id="021d1-134">Add a text block module to a page</span></span>

<span data-ttu-id="021d1-135">Fylgdu þessum skrefum til að bæta textabálkseiningu við nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="021d1-135">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="021d1-136">Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="021d1-136">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="021d1-137">Í svarglugganum **Nýtt sniðmát**, undir **Heiti sniðmáts**, skal slá inn **Efnissniðmát**.</span><span class="sxs-lookup"><span data-stu-id="021d1-137">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="021d1-138">Í hólfinu **Meginmál**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="021d1-138">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="021d1-139">Í glugganum **Bæta við einingu** skal velja eininguna **Sjálfgefin síða** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="021d1-139">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="021d1-140">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="021d1-140">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="021d1-141">Farðu í **Síður** og veldu **Ný** til að búa til nýja síðu.</span><span class="sxs-lookup"><span data-stu-id="021d1-141">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="021d1-142">Í svarglugganum **Velja sniðmát** skal velja **Efnissniðmát**.</span><span class="sxs-lookup"><span data-stu-id="021d1-142">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="021d1-143">Undir **Síðuheiti** skal færa inn **Efnissíða** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="021d1-143">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="021d1-144">Í hólfinu **Aðalsvæði** á nýju síðunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="021d1-144">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="021d1-145">Í glugganum **Bæta við einingu** skal velja eininguna **Hólf** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="021d1-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="021d1-146">Í eiginleikaglugganum fyrir gámaeininguna stillirðu eiginleikann **Breidd** á **Fylla gám**.</span><span class="sxs-lookup"><span data-stu-id="021d1-146">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="021d1-147">Í hólfinu **Hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="021d1-147">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="021d1-148">Í glugganum **Bæta við einingu** skal velja eininguna **Textabálkur** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="021d1-148">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="021d1-149">Í eiginleikaglugga textabálkseiningarinnar bætirðu texta við í reitinn **Mótaður texti**.</span><span class="sxs-lookup"><span data-stu-id="021d1-149">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="021d1-150">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="021d1-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="021d1-151">Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="021d1-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="021d1-152">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="021d1-152">Additional resources</span></span>

[<span data-ttu-id="021d1-153">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="021d1-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="021d1-154">Tilboðsborðaeining</span><span class="sxs-lookup"><span data-stu-id="021d1-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="021d1-155">Myndaræmueining</span><span class="sxs-lookup"><span data-stu-id="021d1-155">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="021d1-156">Eining fyrir bálk með efni</span><span class="sxs-lookup"><span data-stu-id="021d1-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="021d1-157">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="021d1-157">Video player module</span></span>](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]