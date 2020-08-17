---
title: Myndaræmueining
description: Þetta efni fjallar um myndaræmueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 10ff0cd566a1a8d89ccadce9571dafc5a592520b
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/27/2020
ms.locfileid: "3620987"
---
# <a name="carousel-module"></a><span data-ttu-id="f5a8d-103">Myndaræmueining</span><span class="sxs-lookup"><span data-stu-id="f5a8d-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f5a8d-104">Þetta efni fjallar um myndaræmueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f5a8d-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="f5a8d-105">Overview</span></span>

<span data-ttu-id="f5a8d-106">Myndaræmueining er notuð til að setja margar kynningarvörur (þar með talið rtf-myndir) í myndaræmuborða sem snýst og viðskiptavinir geta skoðað.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="f5a8d-107">Til dæmis getur smásali notað myndræmueiningu á heimasíðu til að sýna margar nýjar vörur eða kynningar.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="f5a8d-108">Þú getur bætt innihaldsbálkaeiningum í myndaræmueiningu.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="f5a8d-109">Eiginleikar myndaræmueiningarinnar skilgreina síðan hvernig þessar einingar eru birtar.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="f5a8d-110">Dæmi um myndaræmueiningar í rafrænum viðskiptum</span><span class="sxs-lookup"><span data-stu-id="f5a8d-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="f5a8d-111">Hægt er að nota myndaræmu með mörgum kynningareiningum á heimasíðunni.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="f5a8d-112">Hægt er að nota myndaræmu með mörgum kynningareiningum á vöruupplýsingasíðunni.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="f5a8d-113">Hægt er að nota myndaræmu á hvaða markaðssíðu sem er til að auglýsa margar kynningar eða vörur.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="f5a8d-114">Eftirfarandi mynd sýnir dæmi um myndaræmueiningu sem er notuð á heimasíðu.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-114">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="f5a8d-115">Þessi myndaræmueining inniheldur mörg efnissvæði.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-115">This carousel module contains multiple content block items.</span></span>

![Dæmi um myndaræmueiningu](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="f5a8d-117">Eiginleikar myndaræmueiningar</span><span class="sxs-lookup"><span data-stu-id="f5a8d-117">Carousel module properties</span></span>

| <span data-ttu-id="f5a8d-118">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="f5a8d-118">Property name</span></span>             | <span data-ttu-id="f5a8d-119">Virði</span><span class="sxs-lookup"><span data-stu-id="f5a8d-119">Value</span></span>                 | <span data-ttu-id="f5a8d-120">lýsing</span><span class="sxs-lookup"><span data-stu-id="f5a8d-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="f5a8d-121">Sjálfvirk spilun</span><span class="sxs-lookup"><span data-stu-id="f5a8d-121">Autoplay</span></span>                  | <span data-ttu-id="f5a8d-122">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="f5a8d-122">**True** or **False**</span></span> | <span data-ttu-id="f5a8d-123">Ef gildi er stillt á **Satt** á breytingin á milli hluta í myndaræmunni sér stað sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-123">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="f5a8d-124">Ef gildi er stillt á **Rangt** eiga engin umskipti sér stað nema viðskiptavinurinn noti lyklaborðið eða músina til að fara frá einum hlut til næsta hlutar.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-124">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="f5a8d-125">Tími á milli skyggna</span><span class="sxs-lookup"><span data-stu-id="f5a8d-125">Slide transition interval</span></span> | <span data-ttu-id="f5a8d-126">Gildi í sekúndum</span><span class="sxs-lookup"><span data-stu-id="f5a8d-126">A value in seconds</span></span>    | <span data-ttu-id="f5a8d-127">Bilið fyrir umbreytingar milli atriða.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-127">The interval for transitions between items.</span></span> |
| <span data-ttu-id="f5a8d-128">Umbreytingargerð</span><span class="sxs-lookup"><span data-stu-id="f5a8d-128">Transition type</span></span>           | <span data-ttu-id="f5a8d-129">**Renna** eða **Hverfa**</span><span class="sxs-lookup"><span data-stu-id="f5a8d-129">**Slide** or **Fade**</span></span> | <span data-ttu-id="f5a8d-130">Umskiptaáhrif milli liða.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-130">The transition effect between items.</span></span> |
| <span data-ttu-id="f5a8d-131">Fela flettingu myndaræmu</span><span class="sxs-lookup"><span data-stu-id="f5a8d-131">Hide carousel flipper</span></span>     | <span data-ttu-id="f5a8d-132">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="f5a8d-132">**True** or **False**</span></span> | <span data-ttu-id="f5a8d-133">Ef gildi er stillt á **Satt** eru myndaræmuflipinn og raðvísirinn faldir.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-133">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="f5a8d-134">Leyfa að myndaræmu sé hafnað</span><span class="sxs-lookup"><span data-stu-id="f5a8d-134">Allow carousel dismiss</span></span>    | <span data-ttu-id="f5a8d-135">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="f5a8d-135">**True** or **False**</span></span> | <span data-ttu-id="f5a8d-136">Ef gildið er stillt á **Satt** geta notendur hafnað myndaræmunni.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-136">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="f5a8d-137">Bæta myndaræmueiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="f5a8d-137">Add a carousel module to a page</span></span>

<span data-ttu-id="f5a8d-138">Fylgdu þessum skrefum til að bæta myndaræmueiningu við nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-138">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="f5a8d-139">Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-139">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="f5a8d-140">Í svarglugganum **Nýtt sniðmát** fyrir neðan undir **Heiti sniðmáts**, slærðu inn **Sniðmát myndaræmu** og smellir síðan á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-140">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="f5a8d-141">Í hólfinu **Meginmál** bætirðu við einingunni **Sjálfgefin síða**.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-141">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="f5a8d-142">Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-142">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="f5a8d-143">Notaðu sniðmát myndaræmu sem þú varst að búa til til að búa til síðu sem heitir **Myndaræmusíða**.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-143">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="f5a8d-144">Í hólfinu **Aðal** á nýju síðunni bætirðu við gámaeiningu.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-144">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="f5a8d-145">Í glugganum til hægri stillirðu gildið **Breidd** á **Fylla skjá**.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-145">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="f5a8d-146">Undir **Útlínur síðu** bæirðu myndaræmueiningu við gámaeininguna.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-146">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="f5a8d-147">Bættu innihaldsbálkseiningu við myndaræmueininguna.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-147">Add a content block module to the carousel module.</span></span> <span data-ttu-id="f5a8d-148">Stilltu eiginleika innihaldsbálkseiningar með því að veita **Fyrirsögn**, **Tengil**, **Skipulag** og aðra eiginleika.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-148">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="f5a8d-149">Bæta við og stilla aðra innihaldsbálkseiningu.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-149">Add and configure another content block module.</span></span>
1. <span data-ttu-id="f5a8d-150">Stilltu viðbótareiginleika fyrir myndaræmueininguna eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-150">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="f5a8d-151">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-151">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="f5a8d-152">Síðan ætti að sýna myndaræmu sem hefur tvær einingar í sér (hetjueining og eiginleikaeining).</span><span class="sxs-lookup"><span data-stu-id="f5a8d-152">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="f5a8d-153">Þú getur breytt viðbótareiginleikum fyrir myndaræmu-, hetju- og eiginleikaeiningarnar til að ná tilætluðum áhrifum.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-153">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="f5a8d-154">Veldu**Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="f5a8d-154">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f5a8d-155">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="f5a8d-155">Additional resources</span></span>

[<span data-ttu-id="f5a8d-156">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="f5a8d-156">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f5a8d-157">Tilboðsborðaeining</span><span class="sxs-lookup"><span data-stu-id="f5a8d-157">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="f5a8d-158">Textabálkseining</span><span class="sxs-lookup"><span data-stu-id="f5a8d-158">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="f5a8d-159">Innihaldsbálkseining</span><span class="sxs-lookup"><span data-stu-id="f5a8d-159">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="f5a8d-160">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="f5a8d-160">Video player module</span></span>](add-video-player.md)
