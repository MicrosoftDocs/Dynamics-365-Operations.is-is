---
title: Myndaræmueining
description: Þetta efni fjallar um myndaræmueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: f399e4c5618b65b781fdd3ec835e841614579313
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269729"
---
# <a name="carousel-module"></a><span data-ttu-id="36bb6-103">Myndaræmueining</span><span class="sxs-lookup"><span data-stu-id="36bb6-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="36bb6-104">Þetta efni fjallar um myndaræmueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="36bb6-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="36bb6-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="36bb6-105">Overview</span></span>

<span data-ttu-id="36bb6-106">Myndaræmueining er notuð til að setja margar kynningarvörur (þar með talið rtf-myndir) í myndaræmuborða sem snýst og viðskiptavinir geta skoðað.</span><span class="sxs-lookup"><span data-stu-id="36bb6-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="36bb6-107">Til dæmis getur smásali notað myndræmueiningu á heimasíðu til að sýna margar nýjar vörur eða kynningar.</span><span class="sxs-lookup"><span data-stu-id="36bb6-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="36bb6-108">Þú getur bætt innihaldsbálkaeiningum í myndaræmueiningu.</span><span class="sxs-lookup"><span data-stu-id="36bb6-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="36bb6-109">Eiginleikar myndaræmueiningarinnar skilgreina síðan hvernig þessar einingar eru birtar.</span><span class="sxs-lookup"><span data-stu-id="36bb6-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="36bb6-110">Dæmi um myndaræmueiningar í rafrænum viðskiptum</span><span class="sxs-lookup"><span data-stu-id="36bb6-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="36bb6-111">Hægt er að nota myndaræmu með mörgum kynningareiningum á heimasíðunni.</span><span class="sxs-lookup"><span data-stu-id="36bb6-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="36bb6-112">Hægt er að nota myndaræmu með mörgum kynningareiningum á vöruupplýsingasíðunni.</span><span class="sxs-lookup"><span data-stu-id="36bb6-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="36bb6-113">Hægt er að nota myndaræmu á hvaða markaðssíðu sem er til að auglýsa margar kynningar eða vörur.</span><span class="sxs-lookup"><span data-stu-id="36bb6-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="36bb6-114">Eiginleikar myndaræmueiningar</span><span class="sxs-lookup"><span data-stu-id="36bb6-114">Carousel module properties</span></span>

| <span data-ttu-id="36bb6-115">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="36bb6-115">Property name</span></span>             | <span data-ttu-id="36bb6-116">Virði</span><span class="sxs-lookup"><span data-stu-id="36bb6-116">Value</span></span>                 | <span data-ttu-id="36bb6-117">Lýsing</span><span class="sxs-lookup"><span data-stu-id="36bb6-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="36bb6-118">Sjálfvirk spilun</span><span class="sxs-lookup"><span data-stu-id="36bb6-118">Autoplay</span></span>                  | <span data-ttu-id="36bb6-119">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="36bb6-119">**True** or **False**</span></span> | <span data-ttu-id="36bb6-120">Ef gildi er stillt á **Satt** á breytingin á milli hluta í myndaræmunni sér stað sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="36bb6-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="36bb6-121">Ef gildi er stillt á **Rangt** eiga engin umskipti sér stað nema viðskiptavinurinn noti lyklaborðið eða músina til að fara frá einum hlut til næsta hlutar.</span><span class="sxs-lookup"><span data-stu-id="36bb6-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="36bb6-122">Tími á milli skyggna</span><span class="sxs-lookup"><span data-stu-id="36bb6-122">Slide transition interval</span></span> | <span data-ttu-id="36bb6-123">Gildi í sekúndum</span><span class="sxs-lookup"><span data-stu-id="36bb6-123">A value in seconds</span></span>    | <span data-ttu-id="36bb6-124">Bilið fyrir umbreytingar milli atriða.</span><span class="sxs-lookup"><span data-stu-id="36bb6-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="36bb6-125">Umbreytingargerð</span><span class="sxs-lookup"><span data-stu-id="36bb6-125">Transition type</span></span>           | <span data-ttu-id="36bb6-126">**Renna** eða **Hverfa**</span><span class="sxs-lookup"><span data-stu-id="36bb6-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="36bb6-127">Umskiptaáhrif milli liða.</span><span class="sxs-lookup"><span data-stu-id="36bb6-127">The transition effect between items.</span></span> |
| <span data-ttu-id="36bb6-128">Fela flettingu myndaræmu</span><span class="sxs-lookup"><span data-stu-id="36bb6-128">Hide carousel flipper</span></span>     | <span data-ttu-id="36bb6-129">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="36bb6-129">**True** or **False**</span></span> | <span data-ttu-id="36bb6-130">Ef gildi er stillt á **Satt** eru myndaræmuflipinn og raðvísirinn faldir.</span><span class="sxs-lookup"><span data-stu-id="36bb6-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="36bb6-131">Leyfa að myndaræmu sé hafnað</span><span class="sxs-lookup"><span data-stu-id="36bb6-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="36bb6-132">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="36bb6-132">**True** or **False**</span></span> | <span data-ttu-id="36bb6-133">Ef gildið er stillt á **Satt** geta notendur hafnað myndaræmunni.</span><span class="sxs-lookup"><span data-stu-id="36bb6-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="36bb6-134">Bæta myndaræmueiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="36bb6-134">Add a carousel module to a page</span></span>

<span data-ttu-id="36bb6-135">Fylgdu þessum skrefum til að bæta myndaræmueiningu við nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="36bb6-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="36bb6-136">Veljið **Ný** til að stofna nýtt síðusniðmát.</span><span class="sxs-lookup"><span data-stu-id="36bb6-136">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="36bb6-137">Í svarglugganum **Nýtt sniðmát** fyrir neðan undir **Heiti sniðmáts**, slærðu inn **Sniðmát myndaræmu** og smellir síðan á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="36bb6-137">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="36bb6-138">Í hólfinu **Meginmál** bætirðu við einingunni **Sjálfgefin síða**.</span><span class="sxs-lookup"><span data-stu-id="36bb6-138">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="36bb6-139">Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="36bb6-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="36bb6-140">Notaðu sniðmát myndaræmu sem þú varst að búa til til að búa til síðu sem heitir **Myndaræmusíða**.</span><span class="sxs-lookup"><span data-stu-id="36bb6-140">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="36bb6-141">Í hólfinu **Aðal** á nýju síðunni bætirðu við gámaeiningu.</span><span class="sxs-lookup"><span data-stu-id="36bb6-141">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="36bb6-142">Í glugganum til hægri stillirðu gildið **Breidd** á **Fylla skjá**.</span><span class="sxs-lookup"><span data-stu-id="36bb6-142">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="36bb6-143">Undir **Útlínur síðu** bæirðu myndaræmueiningu við gámaeininguna.</span><span class="sxs-lookup"><span data-stu-id="36bb6-143">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="36bb6-144">Bættu innihaldsbálkseiningu við myndaræmueininguna.</span><span class="sxs-lookup"><span data-stu-id="36bb6-144">Add a content block module to the carousel module.</span></span> <span data-ttu-id="36bb6-145">Stilltu eiginleika innihaldsbálkseiningar með því að veita **Fyrirsögn**, **Tengil**, **Skipulag** og aðra eiginleika.</span><span class="sxs-lookup"><span data-stu-id="36bb6-145">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="36bb6-146">Bæta við og stilla aðra innihaldsbálkseiningu.</span><span class="sxs-lookup"><span data-stu-id="36bb6-146">Add and configure another content block module.</span></span>
1. <span data-ttu-id="36bb6-147">Stilltu viðbótareiginleika fyrir myndaræmueininguna eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="36bb6-147">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="36bb6-148">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="36bb6-148">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="36bb6-149">Síðan ætti að sýna myndaræmu sem hefur tvær einingar í sér (hetjueining og eiginleikaeining).</span><span class="sxs-lookup"><span data-stu-id="36bb6-149">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="36bb6-150">Þú getur breytt viðbótareiginleikum fyrir myndaræmu-, hetju- og eiginleikaeiningarnar til að ná tilætluðum áhrifum.</span><span class="sxs-lookup"><span data-stu-id="36bb6-150">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="36bb6-151">Veldu**Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="36bb6-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="36bb6-152">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="36bb6-152">Additional resources</span></span>

[<span data-ttu-id="36bb6-153">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="36bb6-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="36bb6-154">Tilboðsborðaeining</span><span class="sxs-lookup"><span data-stu-id="36bb6-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="36bb6-155">Textabálkseining</span><span class="sxs-lookup"><span data-stu-id="36bb6-155">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="36bb6-156">Innihaldsbálkseining</span><span class="sxs-lookup"><span data-stu-id="36bb6-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="36bb6-157">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="36bb6-157">Video player module</span></span>](add-video-player.md)
