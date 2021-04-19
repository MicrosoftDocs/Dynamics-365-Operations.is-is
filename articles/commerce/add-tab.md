---
title: Flipaeining
description: Þetta efnisatriði fjallar um flipaeiningar og útskýrir hvernig á að bæta þeim við síður svæða í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: c865d5e055e3fadf2dda225b49f13a163974768f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797456"
---
# <a name="tab-module"></a><span data-ttu-id="cc7f3-103">Flipaeining</span><span class="sxs-lookup"><span data-stu-id="cc7f3-103">Tab module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cc7f3-104">Þetta efnisatriði fjallar um flipaeiningar og útskýrir hvernig á að bæta þeim við síður svæða í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-104">This topic covers tab modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="cc7f3-105">Flipaeiningar líta út eins og hólfaeiningar og eru notaðar við skipulagningu upplýsinga á síðusvæði í flipum.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-105">Tab modules are container-like modules that are used to organize the information on a site page on tabs.</span></span> <span data-ttu-id="cc7f3-106">Hægt er að nota þær á sérhverri síðu þar sem upplýsingar þurfa að koma fram í flipum.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-106">They can be used on any page where information must be presented on tabs.</span></span>

<span data-ttu-id="cc7f3-107">Í hverri flipaeiningu er hægt að bæta við einu eða fleiri flipaeiningaratriðum.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-107">In every tab module, one or more tab item modules can be added.</span></span> <span data-ttu-id="cc7f3-108">Hvert flipaeiningaratriði stendur fyrir einn flipa. Í hverja einingu flipaatriðis er hægt að bæta við einni eða fleiri einingum.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-108">Each tab item module represents a single tab. In each tab item module, one or more modules can be added.</span></span> <span data-ttu-id="cc7f3-109">Engar takmarkanir eru á þeim gerðum eininga sem hægt er að bæta við flipaeiningaratriði.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-109">There are no restrictions on the types of modules that can be added to a tab item module.</span></span>

<span data-ttu-id="cc7f3-110">Eftirfarandi mynd sýnir dæmi um flipaeiningu á síðusvæði.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-110">The following image shows an example of a tab module on a site page.</span></span> <span data-ttu-id="cc7f3-111">Í þessu dæmi er flipinn **Sending** valinn.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-111">In this example, the **Shipping** tab selected.</span></span>

![Dæmi um flipaeiningu](./media/ecommerce-tab.PNG)

## <a name="tab-module-properties"></a><span data-ttu-id="cc7f3-113">Eiginleikar flipaeiningar</span><span class="sxs-lookup"><span data-stu-id="cc7f3-113">Tab module properties</span></span>

| <span data-ttu-id="cc7f3-114">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="cc7f3-114">Property name</span></span> | <span data-ttu-id="cc7f3-115">Gildi</span><span class="sxs-lookup"><span data-stu-id="cc7f3-115">Values</span></span> | <span data-ttu-id="cc7f3-116">lýsing</span><span class="sxs-lookup"><span data-stu-id="cc7f3-116">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="cc7f3-117">Yfirskrift</span><span class="sxs-lookup"><span data-stu-id="cc7f3-117">Heading</span></span> | <span data-ttu-id="cc7f3-118">Texti</span><span class="sxs-lookup"><span data-stu-id="cc7f3-118">Text</span></span> | <span data-ttu-id="cc7f3-119">Þessi eiginleiki sýnir valfrjálsa textafyrirsögn fyrir flipaeininguna.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-119">This property specifies an optional text heading for the tab module.</span></span> |
| <span data-ttu-id="cc7f3-120">Virkur flipavísir</span><span class="sxs-lookup"><span data-stu-id="cc7f3-120">Active Tab Index</span></span> | <span data-ttu-id="cc7f3-121">Númer</span><span class="sxs-lookup"><span data-stu-id="cc7f3-121">Number</span></span> | <span data-ttu-id="cc7f3-122">Þessi eiginleiki sýnir flipann sem á að vera sjálfgefið virkur þegar síða er hlaðin.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-122">This property specifies the tab that should be active by default when a page is loaded.</span></span> <span data-ttu-id="cc7f3-123">Ef ekkert gildi er gefið upp verður fyrsta flipaatriðið virkt að sjálfgefnu.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-123">If no value is provided, the first tab item is active by default.</span></span> |

## <a name="tab-item-module-properties"></a><span data-ttu-id="cc7f3-124">Eiginleikar flipaeiningaratriða</span><span class="sxs-lookup"><span data-stu-id="cc7f3-124">Tab item module properties</span></span>

| <span data-ttu-id="cc7f3-125">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="cc7f3-125">Property name</span></span> | <span data-ttu-id="cc7f3-126">Gildi</span><span class="sxs-lookup"><span data-stu-id="cc7f3-126">Values</span></span> | <span data-ttu-id="cc7f3-127">lýsing</span><span class="sxs-lookup"><span data-stu-id="cc7f3-127">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="cc7f3-128">Titill</span><span class="sxs-lookup"><span data-stu-id="cc7f3-128">Title</span></span> | <span data-ttu-id="cc7f3-129">Texti</span><span class="sxs-lookup"><span data-stu-id="cc7f3-129">Text</span></span> | <span data-ttu-id="cc7f3-130">Þessi eiginleiki sýnir titiltexta fyrir atriði flipaeiningar.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-130">This property specifies the title text for the tab item module.</span></span> |

## <a name="add-a-tab-module-to-a-page"></a><span data-ttu-id="cc7f3-131">Bæta flipaeiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="cc7f3-131">Add a tab module to a page</span></span>

<span data-ttu-id="cc7f3-132">Til að bæta flipaeiningu við síðu og stilla eiginleikana skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-132">To add a tab module to a page and set the properties, follow these steps.</span></span>

1. <span data-ttu-id="cc7f3-133">Notið markaðssniðmát Fabrikam (eða annað sniðmát sem er með engum takmörkunum) til að búa til nýja síðu sem heitir **Reglusíða verslunar**.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-133">Use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store policies page**.</span></span>
1. <span data-ttu-id="cc7f3-134">Í hólfinu **Aðalsvæði** á **Sjálfgefin síða** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-134">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cc7f3-135">Í glugganum **Bæta við einingu** skal velja eininguna **Hólf** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-135">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cc7f3-136">Í hólfinu **Hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-136">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cc7f3-137">Í glugganum **Bæta við einingu** skal velja eininguna **Flipi** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-137">In the **Add Module** dialog box, select the **Tab** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cc7f3-138">Á eiginleikasvæði flipaeiningar skal velja **Fyrirsögn** við hliðina á blýantstákninu.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-138">In the property pane of the tab module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="cc7f3-139">Í glugganum **Fyrirsögn**, undir **Texti fyrirsagnar**, skal færa inn texta fyrirsagnar (til dæmis **Reglur**).</span><span class="sxs-lookup"><span data-stu-id="cc7f3-139">In the **Heading** dialog box, under **Heading Text**, enter heading text (for example, **Policies**).</span></span> <span data-ttu-id="cc7f3-140">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-140">Then select **OK**.</span></span>
1. <span data-ttu-id="cc7f3-141">Í hólfinu **Flipi**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-141">In the **Tab** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cc7f3-142">Í glugganum **Bæta við einingu** skal velja eininguna **Flipaatriði** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-142">In the **Add Module** dialog box, select the **Tab item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cc7f3-143">Á eiginleikasvæði flipaeiningaratriðis, undir **Titill**, skal færa inn titiltexta (til dæmis **Afhending**).</span><span class="sxs-lookup"><span data-stu-id="cc7f3-143">In the property pane of the tab item module, under **Title**, enter title text (for example, **Delivery**).</span></span>
1. <span data-ttu-id="cc7f3-144">Í hólfinu **Flipaatriði**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-144">In the **Tab item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cc7f3-145">Í glugganum **Bæta við einingu** skal velja eininguna **Textabálkur** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-145">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cc7f3-146">Á eiginleikasvæði textabálkseiningar, undir **Sniðinn texti**, skal slá inn stuttan texta.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-146">In the property pane of the text block module, under **Rich text**, enter a paragraph of text.</span></span>
1. <span data-ttu-id="cc7f3-147">Í hólfinu **Flipi** skal bæta við nokkrum flipaeiningaratriðum til viðbótar sem eru með titlum.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-147">In the **Tab** slot, add a few more tab item modules that have titles.</span></span> <span data-ttu-id="cc7f3-148">Í hverju flipaeiningaratriði skal bæta við textabálkseiningu með innihaldi.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-148">In each tab item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="cc7f3-149">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-149">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="cc7f3-150">Síðan birtir flipaeningu sem inniheldur flipaeiningaratriði með innihaldinu sem var bætt við.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-150">The page will show a tab module that contains tab item modules have the content that you added.</span></span>
1. <span data-ttu-id="cc7f3-151">Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="cc7f3-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cc7f3-152">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="cc7f3-152">Additional resources</span></span>

[<span data-ttu-id="cc7f3-153">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="cc7f3-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="cc7f3-154">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="cc7f3-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="cc7f3-155">Fellingareining</span><span class="sxs-lookup"><span data-stu-id="cc7f3-155">Accordion module</span></span>](add-accordion.md)

[<span data-ttu-id="cc7f3-156">Textabálkseining</span><span class="sxs-lookup"><span data-stu-id="cc7f3-156">Text block module</span></span>](add-content-rich-block.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]