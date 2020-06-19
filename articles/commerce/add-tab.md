---
title: Flipaeining
description: Þetta efnisatriði fjallar um flipaeiningar og útskýrir hvernig á að bæta þeim við síður svæða í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
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
ms.openlocfilehash: 60af9b74f7e647e83229e352a03c09d63d0c7902
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417370"
---
# <a name="tab-module"></a><span data-ttu-id="a649b-103">Flipaeining</span><span class="sxs-lookup"><span data-stu-id="a649b-103">Tab module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a649b-104">Þetta efnisatriði fjallar um flipaeiningar og útskýrir hvernig á að bæta þeim við síður svæða í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a649b-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a649b-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="a649b-105">Overview</span></span>

<span data-ttu-id="a649b-106">Flipaeiningar líta út eins og hólfaeiningar og eru notaðar við skipulagningu upplýsinga á síðusvæði í flipum.</span><span class="sxs-lookup"><span data-stu-id="a649b-106">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="a649b-107">Hægt er að nota þær á sérhverri síðu þar sem upplýsingar þurfa að koma fram í flipum.</span><span class="sxs-lookup"><span data-stu-id="a649b-107">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="a649b-108">Í hverri flipaeiningu er hægt að bæta við einu eða fleiri flipaeiningaratriðum.</span><span class="sxs-lookup"><span data-stu-id="a649b-108">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="a649b-109">Hvert flipaeiningaratriði stendur fyrir einn flipa. Í hverja einingu flipaatriðis er hægt að bæta við einni eða fleiri einingum.</span><span class="sxs-lookup"><span data-stu-id="a649b-109">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="a649b-110">Engar takmarkanir eru á þeim gerðum eininga sem hægt er að bæta við flipaeiningaratriði.</span><span class="sxs-lookup"><span data-stu-id="a649b-110">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="a649b-111">Eftirfarandi mynd sýnir dæmi um flipaeiningu á síðusvæði.</span><span class="sxs-lookup"><span data-stu-id="a649b-111">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="a649b-112">Í þessu dæmi er flipinn **Sending** valinn.</span><span class="sxs-lookup"><span data-stu-id="a649b-112">In this example, the **Shipping** tab selected.</span></span>

![Dæmi um flipaeiningu](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="a649b-114">Eiginleikar flipaeiningar</span><span class="sxs-lookup"><span data-stu-id="a649b-114">Tab module properties</span></span>

| <span data-ttu-id="a649b-115">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="a649b-115">Property name</span></span> | <span data-ttu-id="a649b-116">Gildi</span><span class="sxs-lookup"><span data-stu-id="a649b-116">Values</span></span> | <span data-ttu-id="a649b-117">lýsing</span><span class="sxs-lookup"><span data-stu-id="a649b-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="a649b-118">Yfirskrift</span><span class="sxs-lookup"><span data-stu-id="a649b-118">Heading</span></span> | <span data-ttu-id="a649b-119">Texti</span><span class="sxs-lookup"><span data-stu-id="a649b-119">Text</span></span> | <span data-ttu-id="a649b-120">Þessi eiginleiki sýnir valfrjálsa textafyrirsögn fyrir flipaeininguna.</span><span class="sxs-lookup"><span data-stu-id="a649b-120">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="a649b-121">Virkur flipavísir</span><span class="sxs-lookup"><span data-stu-id="a649b-121">Active Tab Index</span></span> | <span data-ttu-id="a649b-122">Númer</span><span class="sxs-lookup"><span data-stu-id="a649b-122">Number</span></span> | <span data-ttu-id="a649b-123">Þessi eiginleiki sýnir flipann sem á að vera sjálfgefið virkur þegar síða er hlaðin.</span><span class="sxs-lookup"><span data-stu-id="a649b-123">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="a649b-124">Ef ekkert gildi er gefið upp verður fyrsta flipaatriðið virkt að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="a649b-124">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="a649b-125">Eiginleikar flipaeiningaratriða</span><span class="sxs-lookup"><span data-stu-id="a649b-125">Tab item module properties</span></span>

| <span data-ttu-id="a649b-126">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="a649b-126">Property name</span></span> | <span data-ttu-id="a649b-127">Gildi</span><span class="sxs-lookup"><span data-stu-id="a649b-127">Values</span></span> | <span data-ttu-id="a649b-128">lýsing</span><span class="sxs-lookup"><span data-stu-id="a649b-128">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="a649b-129">Titill</span><span class="sxs-lookup"><span data-stu-id="a649b-129">Title</span></span> | <span data-ttu-id="a649b-130">Texti</span><span class="sxs-lookup"><span data-stu-id="a649b-130">Text</span></span> | <span data-ttu-id="a649b-131">Þessi eiginleiki sýnir titiltexta fyrir atriði flipaeiningar.</span><span class="sxs-lookup"><span data-stu-id="a649b-131">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="a649b-132">Bæta flipaeiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="a649b-132">Add a tab module to a page</span></span>

<span data-ttu-id="a649b-133">Til að bæta flipaeiningu við síðu og stilla eiginleikana skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="a649b-133">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="a649b-134">Notið markaðssniðmát Fabrikam (eða annað sniðmát sem er með engum takmörkunum) til að búa til nýja síðu sem heitir **Reglusíða verslunar**.</span><span class="sxs-lookup"><span data-stu-id="a649b-134">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="a649b-135">Í hólfinu **Aðalsvæði** á **Sjálfgefin síða** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="a649b-135">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a649b-136">Í glugganum **Bæta við einingu** skal velja eininguna **Hólf** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a649b-136">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a649b-137">Í hólfinu **Hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="a649b-137">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a649b-138">Í glugganum **Bæta við einingu** skal velja eininguna **Flipi** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a649b-138">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a649b-139">Á eiginleikasvæði flipaeiningar skal velja **Fyrirsögn** við hliðina á blýantstákninu.</span><span class="sxs-lookup"><span data-stu-id="a649b-139">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="a649b-140">Í glugganum **Fyrirsögn**, undir **Texti fyrirsagnar**, skal færa inn texta fyrirsagnar (til dæmis **Reglur**).</span><span class="sxs-lookup"><span data-stu-id="a649b-140">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="a649b-141">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a649b-141">Then select **OK**.</span></span>
1. <span data-ttu-id="a649b-142">Í hólfinu **Flipi**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="a649b-142">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a649b-143">Í glugganum **Bæta við einingu** skal velja eininguna **Flipaatriði** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a649b-143">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a649b-144">Á eiginleikasvæði flipaeiningaratriðis, undir **Titill**, skal færa inn titiltexta (til dæmis **Afhending**).</span><span class="sxs-lookup"><span data-stu-id="a649b-144">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="a649b-145">Í hólfinu **Flipaatriði**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="a649b-145">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="a649b-146">Í glugganum **Bæta við einingu** skal velja eininguna **Textabálkur** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a649b-146">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="a649b-147">Á eiginleikasvæði textabálkseiningar, undir **Sniðinn texti**, skal slá inn stuttan texta.</span><span class="sxs-lookup"><span data-stu-id="a649b-147">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="a649b-148">Í hólfinu **Flipi** skal bæta við nokkrum flipaeiningaratriðum til viðbótar sem eru með titlum.</span><span class="sxs-lookup"><span data-stu-id="a649b-148">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="a649b-149">Í hverju flipaeiningaratriði skal bæta við textabálkseiningu með innihaldi.</span><span class="sxs-lookup"><span data-stu-id="a649b-149">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="a649b-150">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="a649b-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="a649b-151">Síðan birtir flipaeningu sem inniheldur flipaeiningaratriði með innihaldinu sem var bætt við.</span><span class="sxs-lookup"><span data-stu-id="a649b-151">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="a649b-152">Veldu**Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="a649b-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a649b-153">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a649b-153">Additional resources</span></span>

[<span data-ttu-id="a649b-154">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="a649b-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a649b-155">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="a649b-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="a649b-156">Fellingareining</span><span class="sxs-lookup"><span data-stu-id="a649b-156">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="a649b-157">Textabálkseining</span><span class="sxs-lookup"><span data-stu-id="a649b-157">Text block module</span></span>](add-content-rich-block.md)
