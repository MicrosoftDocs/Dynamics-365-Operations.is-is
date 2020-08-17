---
title: Fellingareining
description: Þetta efnisatriði fjallar um fellingareiningar og útskýrir hvernig á að bæta þeim við síður svæða í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 1097289d339b84aa477752934afe8192e56c5ce5
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621085"
---
# <a name="accordion-module"></a><span data-ttu-id="170eb-103">Fellingareining</span><span class="sxs-lookup"><span data-stu-id="170eb-103">Accordion module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="170eb-104">Þetta efnisatriði fjallar um fellingareiningar og útskýrir hvernig á að bæta þeim við síður svæða í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="170eb-104">This topic covers accordion modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="170eb-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="170eb-105">Overview</span></span>

<span data-ttu-id="170eb-106">Fellingareiningar líta út eins og hólfaeiningar sem eru notaðar við skipulagningu upplýsinga eða eininga á síðu með því að bjóða upp á möguleika sem lítur út eins og skúffa sem hægt er að draga út.</span><span class="sxs-lookup"><span data-stu-id="170eb-106">Accordion modules are container-like modules that are used to organize the information or modules on a page by providing a collapsible drawer-like capability.</span></span> <span data-ttu-id="170eb-107">Fellingareiningar er hægt að nota á öllu síðum.</span><span class="sxs-lookup"><span data-stu-id="170eb-107">An accordion module can be used on any page.</span></span>

<span data-ttu-id="170eb-108">Innan hverrar fellingareiningar er hægt að bæta við einu eða fleiri fellingareiningaratriðum.</span><span class="sxs-lookup"><span data-stu-id="170eb-108">Inside every accordion module, one or more accordion item modules can be added.</span></span> <span data-ttu-id="170eb-109">Sérhvert atriði fellingareiningar felur í sér opnanlega skúffu.</span><span class="sxs-lookup"><span data-stu-id="170eb-109">Each accordion item module represents a collapsible drawer.</span></span> <span data-ttu-id="170eb-110">Innan hvers fellingareiningaratriðis er hægt að bæta við einni eða fleiri einingum.</span><span class="sxs-lookup"><span data-stu-id="170eb-110">Inside every accordion item module, one or more modules can be added.</span></span> <span data-ttu-id="170eb-111">Engar takmarkanir eru á þeim gerðum eininga sem hægt er að bæta við fellingareiningaratriði.</span><span class="sxs-lookup"><span data-stu-id="170eb-111">There are no restrictions on the types of modules that can be added to an accordion item module.</span></span>

<span data-ttu-id="170eb-112">Eftirfarandi mynd sýnir dæmi um fellingareiningu sem er notuð til að halda skipulagi á upplýsingum á síðu verslunar með algengum spurningum.</span><span class="sxs-lookup"><span data-stu-id="170eb-112">The following image shows an example of an accordion module that is used to organize information on a store's frequently asked questions (FAQ) page.</span></span>

![Dæmi um fellingareiningu](./media/ecommerce-accordion.PNG)

## <a name="accordion-module-properties"></a><span data-ttu-id="170eb-114">Eiginleikar fellingareiningar</span><span class="sxs-lookup"><span data-stu-id="170eb-114">Accordion module properties</span></span>

| <span data-ttu-id="170eb-115">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="170eb-115">Property name</span></span> | <span data-ttu-id="170eb-116">Gildi</span><span class="sxs-lookup"><span data-stu-id="170eb-116">Values</span></span> | <span data-ttu-id="170eb-117">lýsing</span><span class="sxs-lookup"><span data-stu-id="170eb-117">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="170eb-118">Yfirskrift</span><span class="sxs-lookup"><span data-stu-id="170eb-118">Heading</span></span> | <span data-ttu-id="170eb-119">Texti</span><span class="sxs-lookup"><span data-stu-id="170eb-119">Text</span></span> | <span data-ttu-id="170eb-120">Þessi eiginleiki sýnir valfrjálsa textafyrirsögn fyrir fellingareininguna.</span><span class="sxs-lookup"><span data-stu-id="170eb-120">This property specifies an optional text heading for the accordion module.</span></span> |
| <span data-ttu-id="170eb-121">Stækka allt</span><span class="sxs-lookup"><span data-stu-id="170eb-121">Expand All</span></span> | <span data-ttu-id="170eb-122">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="170eb-122">**True** or **False**</span></span> | <span data-ttu-id="170eb-123">Ef gildið er stillt á **Satt** er kveikt á víkka/draga saman virkninni þannig að hægt sé að víkka og draga saman öll atriði í fellingareiningunni.</span><span class="sxs-lookup"><span data-stu-id="170eb-123">If the value is set to **True**, expand/collapse functionality is turned on, so that all items in the accordion module can be expanded and collapsed.</span></span> |
| <span data-ttu-id="170eb-124">Samskiptastíll</span><span class="sxs-lookup"><span data-stu-id="170eb-124">Interaction Style</span></span> | <span data-ttu-id="170eb-125">**Óháð** eða **Víkka aðeins eitt atriði**</span><span class="sxs-lookup"><span data-stu-id="170eb-125">**Independent** or **Expand one item only**</span></span> | <span data-ttu-id="170eb-126">Þessi eiginleiki skilgreinir samskiptastíl fellingaratriða.</span><span class="sxs-lookup"><span data-stu-id="170eb-126">This property defines the style of interaction for accordion items.</span></span> <span data-ttu-id="170eb-127">Ef gildið er stillt á **Óháð** er hægt að víkka og draga saman hvert fellingaratriði fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="170eb-127">If the value is set to **Independent**, each accordion item can be expanded or collapsed independently.</span></span> <span data-ttu-id="170eb-128">Ef gildið er stillt á **Víkka aðeins eitt atriði** er aðeins hægt að víkka eitt atriði í einu.</span><span class="sxs-lookup"><span data-stu-id="170eb-128">If the value is set to **Expand one item only**, only one item can be expanded at a time.</span></span> <span data-ttu-id="170eb-129">Þegar atriði eru víkkuð dragast saman þau atriði sem voru víkkuð á undan.</span><span class="sxs-lookup"><span data-stu-id="170eb-129">As items are expanded, previously expanded items are collapsed.</span></span> |

## <a name="accordion-item-module-properties"></a><span data-ttu-id="170eb-130">Eiginleikar fellingareiningaratriða</span><span class="sxs-lookup"><span data-stu-id="170eb-130">Accordion item module properties</span></span>

| <span data-ttu-id="170eb-131">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="170eb-131">Property name</span></span> | <span data-ttu-id="170eb-132">Gildi</span><span class="sxs-lookup"><span data-stu-id="170eb-132">Values</span></span> | <span data-ttu-id="170eb-133">lýsing</span><span class="sxs-lookup"><span data-stu-id="170eb-133">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="170eb-134">Titill</span><span class="sxs-lookup"><span data-stu-id="170eb-134">Title</span></span> | <span data-ttu-id="170eb-135">Texti</span><span class="sxs-lookup"><span data-stu-id="170eb-135">Text</span></span> | <span data-ttu-id="170eb-136">Þessi eiginleiki sýnir titiltexta fyrir atriði fellingareiningar.</span><span class="sxs-lookup"><span data-stu-id="170eb-136">This property specifies the title text for the accordion item module.</span></span> <span data-ttu-id="170eb-137">Með því að velja titilsvæðið geta notendur víkkað eða dregið saman hlutann.</span><span class="sxs-lookup"><span data-stu-id="170eb-137">By selecting the title region, users can expand or collapse the section.</span></span> |
| <span data-ttu-id="170eb-138">Víkka sjálfgefið</span><span class="sxs-lookup"><span data-stu-id="170eb-138">Expand by default</span></span> | <span data-ttu-id="170eb-139">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="170eb-139">**True** or **False**</span></span> | <span data-ttu-id="170eb-140">Ef gildið er stillt á **Satt** víkkar atriði fellingareiningar að sjálfgefnu þegar síðan er hlaðin inn.</span><span class="sxs-lookup"><span data-stu-id="170eb-140">If the value is set to **True**, the accordion item is expanded by default when the page is loaded.</span></span> |

## <a name="add-an-accordion-module-to-a-faq-page"></a><span data-ttu-id="170eb-141">Bæta fellingareiningu við síðu algengra spurninga</span><span class="sxs-lookup"><span data-stu-id="170eb-141">Add an accordion module to a FAQ page</span></span>

<span data-ttu-id="170eb-142">Til að bæta fellingareiningu við síðu algengra spurninga og stilla eiginleika hennar í svæðissmið skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="170eb-142">To add an accordion module to a FAQ page and set its properties in site builder, follow these steps.</span></span>

1. <span data-ttu-id="170eb-143">Opnið **Síður** og notið markaðssniðmát Fabrikam (eða annað sniðmát sem er með engum takmörkunum) til að búa til nýja síðu sem heitir **Algengar spurningar verslunar**.</span><span class="sxs-lookup"><span data-stu-id="170eb-143">Go to **Pages**, and use the Fabrikam marketing template (or any template that has no restrictions) to create a new page that is named **Store FAQ**.</span></span>
1. <span data-ttu-id="170eb-144">Í hólfinu **Aðalsvæði** á **Sjálfgefin síða** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="170eb-144">In the **Main** slot of the **Default page**, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="170eb-145">Í glugganum **Bæta við einingu** skal velja eininguna **Hólf** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="170eb-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="170eb-146">Í hólfinu **Hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="170eb-146">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="170eb-147">Í glugganum **Bæta við einingu** skal velja eininguna **Felling** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="170eb-147">In the **Add Module** dialog box, select the **Accordion** module, and then select **OK**.</span></span>
1. <span data-ttu-id="170eb-148">Á eiginleikasvæði fellingareiningar skal velja **Fyrirsögn** við hliðina á blýantstákninu.</span><span class="sxs-lookup"><span data-stu-id="170eb-148">In the property pane of the accordion module, select **Heading** next to the pencil symbol.</span></span>
1. <span data-ttu-id="170eb-149">Í glugganum **Fyrirsögn**, undir **Texti fyrirsagnar**, skal færa inn **Algengar spurningar**.</span><span class="sxs-lookup"><span data-stu-id="170eb-149">In the **Heading** dialog box, under **Heading Text**, enter **Frequently asked questions**.</span></span> <span data-ttu-id="170eb-150">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="170eb-150">Then select **OK**.</span></span>
1. <span data-ttu-id="170eb-151">Á eiginleikasvæði fellingareiningar skal velja gátreitinn **Sýna allt víkkað** og síðan, í reitnum **Samskiptastíll**, skal velja **Óháð**.</span><span class="sxs-lookup"><span data-stu-id="170eb-151">In the property pane of the accordion module, select the **Show expand all** check box, and then, in the **Interaction style** field, select **Independent**.</span></span>
1. <span data-ttu-id="170eb-152">Í hólfinu **Felling**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="170eb-152">In the **Accordion** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="170eb-153">Í glugganum **Bæta við einingu** skal velja eininguna **Fellingaratriði** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="170eb-153">In the **Add Module** dialog box, select the **Accordion item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="170eb-154">Á eiginleikasvæði fellingareiningaratriðis, undir **Titill**, skal færa inn titiltexta (til dæmis **Hvernig virka skil?**).</span><span class="sxs-lookup"><span data-stu-id="170eb-154">In the property pane of the accordion item module, under **Title**, enter title text (for example, **How do returns work?**).</span></span>
1. <span data-ttu-id="170eb-155">Í hólfinu **Fellingaratriði**, skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="170eb-155">In the **Accordion item** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="170eb-156">Í glugganum **Bæta við einingu** skal velja eininguna **Textabálkur** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="170eb-156">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span>
1. <span data-ttu-id="170eb-157">Á eiginleikasvæði textabálkseiningar skal slá inn stuttan texta (til dæmis **Skil þurfa að fara fram í gegnum símaver. Hringja skal í 1-800-FABRIKAM fyrir skil. Vörur eru með 30 daga skilareglu. Hefja verður skil innan þess tímaramma.**).</span><span class="sxs-lookup"><span data-stu-id="170eb-157">In the property pane of the text block module, enter a paragraph of text (for example, **Returns must be processed via the call center. Contact 1-800-FABRIKAM for returns. Products have a 30-day return policy. Returns must be initiated within this time frame.**).</span></span>
1. <span data-ttu-id="170eb-158">Í hólfinu **Felling** skal bæta við nokkrum fellingareiningaratriðum í viðbót.</span><span class="sxs-lookup"><span data-stu-id="170eb-158">In the **Accordion** slot, add a few more accordion item modules.</span></span> <span data-ttu-id="170eb-159">Í hverju fellingareiningaratriði skal bæta við textabálkseiningu með innihaldi.</span><span class="sxs-lookup"><span data-stu-id="170eb-159">In each accordion item module, add a text block module that has content.</span></span>
1. <span data-ttu-id="170eb-160">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="170eb-160">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="170eb-161">Síðan mun sýna fellingareiningu með innihaldinu sem var bætt við.</span><span class="sxs-lookup"><span data-stu-id="170eb-161">The page will show an accordion module that has the content that you added.</span></span>
1. <span data-ttu-id="170eb-162">Veldu**Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="170eb-162">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="170eb-163">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="170eb-163">Additional resources</span></span>

[<span data-ttu-id="170eb-164">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="170eb-164">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="170eb-165">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="170eb-165">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="170eb-166">Flipaeining</span><span class="sxs-lookup"><span data-stu-id="170eb-166">Tab module</span></span>](add-tab.md)

[<span data-ttu-id="170eb-167">Textabálkseining</span><span class="sxs-lookup"><span data-stu-id="170eb-167">Text block module</span></span>](add-content-rich-block.md)
