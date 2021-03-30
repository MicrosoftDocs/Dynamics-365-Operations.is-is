---
title: Myndaræmueining
description: Þetta efni fjallar um myndræmueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 5333ecd7a1fe4f60684fa5f5bb3ac9f98efde6d7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206512"
---
# <a name="carousel-module"></a><span data-ttu-id="46200-103">Myndaræmueining</span><span class="sxs-lookup"><span data-stu-id="46200-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="46200-104">Þetta efni fjallar um myndræmueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="46200-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="46200-105">Myndaræmueining er notuð til að setja margar kynningarvörur (þar með talið rtf-myndir) í myndaræmuborða sem snýst og viðskiptavinir geta skoðað.</span><span class="sxs-lookup"><span data-stu-id="46200-105">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="46200-106">Til dæmis getur smásali notað myndræmueiningu á heimasíðu til að sýna margar nýjar vörur eða kynningar.</span><span class="sxs-lookup"><span data-stu-id="46200-106">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="46200-107">Þú getur bætt innihaldsbálkaeiningum í myndaræmueiningu.</span><span class="sxs-lookup"><span data-stu-id="46200-107">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="46200-108">Eiginleikar myndaræmueiningarinnar skilgreina síðan hvernig þessar einingar eru birtar.</span><span class="sxs-lookup"><span data-stu-id="46200-108">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="46200-109">Dæmi um myndaræmueiningar í rafrænum viðskiptum</span><span class="sxs-lookup"><span data-stu-id="46200-109">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="46200-110">Hægt er að nota myndaræmu með mörgum kynningareiningum á heimasíðunni.</span><span class="sxs-lookup"><span data-stu-id="46200-110">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="46200-111">Hægt er að nota myndaræmu með mörgum kynningareiningum á vöruupplýsingasíðunni.</span><span class="sxs-lookup"><span data-stu-id="46200-111">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="46200-112">Hægt er að nota myndaræmu á hvaða markaðssíðu sem er til að auglýsa margar kynningar eða vörur.</span><span class="sxs-lookup"><span data-stu-id="46200-112">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="46200-113">Eftirfarandi mynd sýnir dæmi um myndaræmueiningu sem er notuð á heimasíðu.</span><span class="sxs-lookup"><span data-stu-id="46200-113">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="46200-114">Þessi myndaræmueining inniheldur mörg efnissvæði.</span><span class="sxs-lookup"><span data-stu-id="46200-114">This carousel module contains multiple content block items.</span></span>

![Dæmi um myndaræmueiningu](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="46200-116">Eiginleikar myndaræmueiningar</span><span class="sxs-lookup"><span data-stu-id="46200-116">Carousel module properties</span></span>

| <span data-ttu-id="46200-117">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="46200-117">Property name</span></span>             | <span data-ttu-id="46200-118">Virði</span><span class="sxs-lookup"><span data-stu-id="46200-118">Value</span></span>                 | <span data-ttu-id="46200-119">lýsing</span><span class="sxs-lookup"><span data-stu-id="46200-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="46200-120">Sjálfvirk spilun</span><span class="sxs-lookup"><span data-stu-id="46200-120">Autoplay</span></span>                  | <span data-ttu-id="46200-121">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="46200-121">**True** or **False**</span></span> | <span data-ttu-id="46200-122">Ef gildi er stillt á **Satt** á breytingin á milli hluta í myndaræmunni sér stað sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="46200-122">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="46200-123">Ef gildi er stillt á **Rangt** eiga engin umskipti sér stað nema viðskiptavinurinn noti lyklaborðið eða músina til að fara frá einum hlut til næsta hlutar.</span><span class="sxs-lookup"><span data-stu-id="46200-123">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="46200-124">Tími á milli skyggna</span><span class="sxs-lookup"><span data-stu-id="46200-124">Slide transition interval</span></span> | <span data-ttu-id="46200-125">Gildi í sekúndum</span><span class="sxs-lookup"><span data-stu-id="46200-125">A value in seconds</span></span>    | <span data-ttu-id="46200-126">Bilið fyrir umbreytingar milli atriða.</span><span class="sxs-lookup"><span data-stu-id="46200-126">The interval for transitions between items.</span></span> |
| <span data-ttu-id="46200-127">Umbreytingargerð</span><span class="sxs-lookup"><span data-stu-id="46200-127">Transition type</span></span>           | <span data-ttu-id="46200-128">**Renna** eða **Hverfa**</span><span class="sxs-lookup"><span data-stu-id="46200-128">**Slide** or **Fade**</span></span> | <span data-ttu-id="46200-129">Umskiptaáhrif milli liða.</span><span class="sxs-lookup"><span data-stu-id="46200-129">The transition effect between items.</span></span> |
| <span data-ttu-id="46200-130">Fela flettingu myndaræmu</span><span class="sxs-lookup"><span data-stu-id="46200-130">Hide carousel flipper</span></span>     | <span data-ttu-id="46200-131">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="46200-131">**True** or **False**</span></span> | <span data-ttu-id="46200-132">Ef gildi er stillt á **Satt** eru myndaræmuflipinn og raðvísirinn faldir.</span><span class="sxs-lookup"><span data-stu-id="46200-132">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="46200-133">Leyfa að myndaræmu sé hafnað</span><span class="sxs-lookup"><span data-stu-id="46200-133">Allow carousel dismiss</span></span>    | <span data-ttu-id="46200-134">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="46200-134">**True** or **False**</span></span> | <span data-ttu-id="46200-135">Ef gildið er stillt á **Satt** geta notendur hafnað myndaræmunni.</span><span class="sxs-lookup"><span data-stu-id="46200-135">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="46200-136">Bæta myndaræmueiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="46200-136">Add a carousel module to a page</span></span>

<span data-ttu-id="46200-137">Fylgdu þessum skrefum til að bæta myndaræmueiningu við nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="46200-137">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="46200-138">Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="46200-138">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="46200-139">Í svarglugganum **Nýtt sniðmát** fyrir neðan undir **Heiti sniðmáts**, slærðu inn **Sniðmát myndaræmu** og smellir síðan á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="46200-139">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="46200-140">Í hólfinu **Meginmál** bætirðu við einingunni **Sjálfgefin síða**.</span><span class="sxs-lookup"><span data-stu-id="46200-140">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="46200-141">Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="46200-141">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="46200-142">Notaðu sniðmát myndaræmu sem þú varst að búa til til að búa til síðu sem heitir **Myndaræmusíða**.</span><span class="sxs-lookup"><span data-stu-id="46200-142">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="46200-143">Í hólfinu **Aðal** á nýju síðunni bætirðu við gámaeiningu.</span><span class="sxs-lookup"><span data-stu-id="46200-143">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="46200-144">Í glugganum til hægri stillirðu gildið **Breidd** á **Fylla skjá**.</span><span class="sxs-lookup"><span data-stu-id="46200-144">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="46200-145">Undir **Útlínur síðu** bæirðu myndaræmueiningu við gámaeininguna.</span><span class="sxs-lookup"><span data-stu-id="46200-145">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="46200-146">Bættu innihaldsbálkseiningu við myndaræmueininguna.</span><span class="sxs-lookup"><span data-stu-id="46200-146">Add a content block module to the carousel module.</span></span> <span data-ttu-id="46200-147">Stilltu eiginleika innihaldsbálkseiningar með því að veita **Fyrirsögn**, **Tengil**, **Skipulag** og aðra eiginleika.</span><span class="sxs-lookup"><span data-stu-id="46200-147">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="46200-148">Bæta við og stilla aðra innihaldsbálkseiningu.</span><span class="sxs-lookup"><span data-stu-id="46200-148">Add and configure another content block module.</span></span>
1. <span data-ttu-id="46200-149">Stilltu viðbótareiginleika fyrir myndaræmueininguna eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="46200-149">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="46200-150">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="46200-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="46200-151">Síðan ætti að sýna myndaræmu sem hefur tvær einingar í sér (hetjueining og eiginleikaeining).</span><span class="sxs-lookup"><span data-stu-id="46200-151">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="46200-152">Þú getur breytt viðbótareiginleikum fyrir myndaræmu-, hetju- og eiginleikaeiningarnar til að ná tilætluðum áhrifum.</span><span class="sxs-lookup"><span data-stu-id="46200-152">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="46200-153">Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="46200-153">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="46200-154">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="46200-154">Additional resources</span></span>

[<span data-ttu-id="46200-155">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="46200-155">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="46200-156">Tilboðsborðaeining</span><span class="sxs-lookup"><span data-stu-id="46200-156">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="46200-157">Textabálkseining</span><span class="sxs-lookup"><span data-stu-id="46200-157">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="46200-158">Eining fyrir bálk með efni</span><span class="sxs-lookup"><span data-stu-id="46200-158">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="46200-159">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="46200-159">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]