---
title: Myndaræmueining
description: Þetta efni fjallar um myndaræmueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785238"
---
# <a name="carousel-module"></a><span data-ttu-id="47385-103">Myndaræmueining</span><span class="sxs-lookup"><span data-stu-id="47385-103">Carousel module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="47385-104">Þetta efni fjallar um myndaræmueiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="47385-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="47385-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="47385-105">Overview</span></span>

<span data-ttu-id="47385-106">Myndaræmueining er notuð til að setja margar kynningarvörur í myndaræmu sem viðskiptavinir geta skoðað.</span><span class="sxs-lookup"><span data-stu-id="47385-106">A carousel module is used to put multiple promotional items in a carousel that customers can browse.</span></span> <span data-ttu-id="47385-107">Hún er sérstök gámaeining sem hýsir aðrar einingar.</span><span class="sxs-lookup"><span data-stu-id="47385-107">It's a special container module that hosts other modules.</span></span> <span data-ttu-id="47385-108">Til dæmis getur smásali notað myndræmueiningu á heimasíðu til að sýna margar nýjar vörur eða kynningar.</span><span class="sxs-lookup"><span data-stu-id="47385-108">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="47385-109">Þú getur bætt hetju- og eiginleikaeiningum í myndaræmueiningu.</span><span class="sxs-lookup"><span data-stu-id="47385-109">You can add hero and feature modules inside a carousel module.</span></span> <span data-ttu-id="47385-110">Eiginleikar myndaræmueiningarinnar skilgreina síðan hvernig þessar einingar eru birtar.</span><span class="sxs-lookup"><span data-stu-id="47385-110">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="47385-111">Dæmi um myndaræmueiningar í rafrænum viðskiptum</span><span class="sxs-lookup"><span data-stu-id="47385-111">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="47385-112">Hægt er að nota myndaræmu með mörgum kynningareiningum á heimasíðunni.</span><span class="sxs-lookup"><span data-stu-id="47385-112">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="47385-113">Hægt er að nota myndaræmu með mörgum kynningareiningum á vöruupplýsingasíðunni.</span><span class="sxs-lookup"><span data-stu-id="47385-113">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="47385-114">Hægt er að nota myndaræmu á hvaða markaðssíðu sem er til að auglýsa margar kynningar eða vörur.</span><span class="sxs-lookup"><span data-stu-id="47385-114">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="47385-115">Eiginleikar myndaræmueiningar</span><span class="sxs-lookup"><span data-stu-id="47385-115">Carousel module properties</span></span>

| <span data-ttu-id="47385-116">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="47385-116">Property name</span></span>             | <span data-ttu-id="47385-117">Virði</span><span class="sxs-lookup"><span data-stu-id="47385-117">Value</span></span>                                | <span data-ttu-id="47385-118">Lýsing</span><span class="sxs-lookup"><span data-stu-id="47385-118">Description</span></span> |
|---------------------------|--------------------------------------|-------------|
| <span data-ttu-id="47385-119">Sjálfvirk spilun</span><span class="sxs-lookup"><span data-stu-id="47385-119">Autoplay</span></span>                  | <span data-ttu-id="47385-120">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="47385-120">**True** or **False**</span></span>                | <span data-ttu-id="47385-121">Ef gildi er stillt á **Satt** á breytingin á milli hluta í myndaræmunni sér stað sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="47385-121">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="47385-122">Ef gildi er stillt á **Rangt** eiga engin umskipti sér stað nema viðskiptavinurinn noti lyklaborðið eða músina til að fara frá einum hlut til næsta hlutar.</span><span class="sxs-lookup"><span data-stu-id="47385-122">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="47385-123">Tími á milli skyggna</span><span class="sxs-lookup"><span data-stu-id="47385-123">Slide transition interval</span></span> | <span data-ttu-id="47385-124">Gildi í sekúndum</span><span class="sxs-lookup"><span data-stu-id="47385-124">A value in seconds</span></span>                   | <span data-ttu-id="47385-125">Bilið fyrir umbreytingar milli atriða.</span><span class="sxs-lookup"><span data-stu-id="47385-125">The interval for transitions between items.</span></span> |
| <span data-ttu-id="47385-126">Skiptimynd</span><span class="sxs-lookup"><span data-stu-id="47385-126">Transition animation</span></span>      | <span data-ttu-id="47385-127">**Renna** eða **Hverfa**</span><span class="sxs-lookup"><span data-stu-id="47385-127">**Slide** or **Fade**</span></span>                | <span data-ttu-id="47385-128">Umskiptaáhrifin.</span><span class="sxs-lookup"><span data-stu-id="47385-128">The transition effect.</span></span> |
| <span data-ttu-id="47385-129">Breidd</span><span class="sxs-lookup"><span data-stu-id="47385-129">Width</span></span>                     | <span data-ttu-id="47385-130">**Passa í gám** eða **Fylla skjáinn**</span><span class="sxs-lookup"><span data-stu-id="47385-130">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="47385-131">Ef gildi er stillt á **Passa í gám** eru hlutirnir í hringekjunni takmarkaðir við breidd myndaræmunnar.</span><span class="sxs-lookup"><span data-stu-id="47385-131">If the value is set to **Fit container**, the items inside the carousel are restricted to the width of the carousel.</span></span> <span data-ttu-id="47385-132">Ef gildi er stillt á **Fylla skjáinn** eru atriðin takmörkuð við breidd myndaræmunnar en geta farið í stillingar fyrir allan skjáinn.</span><span class="sxs-lookup"><span data-stu-id="47385-132">If the value is set to **Fill screen**, the items aren't restricted to the carousel width but can go into full-screen mode.</span></span> <span data-ttu-id="47385-133">Þú getur breytt gildi til að ná tilætluðu útliti.</span><span class="sxs-lookup"><span data-stu-id="47385-133">You can change the value to achieve the desired layout.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="47385-134">Bæta myndaræmueiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="47385-134">Add a carousel module to a page</span></span>

<span data-ttu-id="47385-135">Fylgdu þessum skrefum til að bæta myndaræmueiningu við nýja síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="47385-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="47385-136">Búðu til síðusniðmát sem heitir **myndaræmusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="47385-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="47385-137">Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við myndaræmueiningu.</span><span class="sxs-lookup"><span data-stu-id="47385-137">In the **Main** slot of the default page, add a carousel module.</span></span>
1. <span data-ttu-id="47385-138">Bættu hetjueiningu við myndaræmueininguna.</span><span class="sxs-lookup"><span data-stu-id="47385-138">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="47385-139">Bættu eiginleikaeiningu við myndaræmueininguna.</span><span class="sxs-lookup"><span data-stu-id="47385-139">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="47385-140">Skráðu brotið út í sniðmátinu og birtu það.</span><span class="sxs-lookup"><span data-stu-id="47385-140">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="47385-141">Notaðu myndaræmusniðmátið sem þú bjóst til til að búa til síðu sem heitir **myndaræmusíða**.</span><span class="sxs-lookup"><span data-stu-id="47385-141">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="47385-142">Í hólfinu **Aðal** á nýju síðunni bætirðu við myndaræmueiningu.</span><span class="sxs-lookup"><span data-stu-id="47385-142">In the **Main** slot of the new page, add a carousel module.</span></span>
1. <span data-ttu-id="47385-143">Stilltu eiginleikann **Breidd** í myndaræmueiningunni á **Fylla skjáinn**.</span><span class="sxs-lookup"><span data-stu-id="47385-143">Set the **Width** property of the carousel module to **Fill screen**.</span></span> 
1. <span data-ttu-id="47385-144">Stilltu eiginleikann **Skiptimynd** á **Renna**.</span><span class="sxs-lookup"><span data-stu-id="47385-144">Set the **Transition animation** property to **Slide**.</span></span>
1. <span data-ttu-id="47385-145">Bættu hetjueiningu við myndaræmueininguna.</span><span class="sxs-lookup"><span data-stu-id="47385-145">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="47385-146">Bættu við mynd og fyrirsögn í hetjueiningunni og veldu síðan **Vista**.</span><span class="sxs-lookup"><span data-stu-id="47385-146">In the hero module, add an image and a heading, and then select **Save**.</span></span>
1. <span data-ttu-id="47385-147">Bættu eiginleikaeiningu við myndaræmueininguna.</span><span class="sxs-lookup"><span data-stu-id="47385-147">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="47385-148">Bættu við mynd, fyrirsögn og efnisgrein í eiginleikaeiningunni.</span><span class="sxs-lookup"><span data-stu-id="47385-148">In the feature module, add an image, a heading, and a paragraph of text.</span></span>
1. <span data-ttu-id="47385-149">Vistaðu og forskoðaðu síðuna.</span><span class="sxs-lookup"><span data-stu-id="47385-149">Save and preview the page.</span></span> <span data-ttu-id="47385-150">Síðan ætti að sýna myndaræmu sem hefur tvær einingar í sér (hetjueining og eiginleikaeining).</span><span class="sxs-lookup"><span data-stu-id="47385-150">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="47385-151">Þú getur breytt viðbótareiginleikum fyrir myndaræmu-, hetju- og eiginleikaeiningarnar til að ná tilætluðum áhrifum.</span><span class="sxs-lookup"><span data-stu-id="47385-151">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="47385-152">Athuga á síðunni og birtu hana.</span><span class="sxs-lookup"><span data-stu-id="47385-152">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="47385-153">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="47385-153">Additional resources</span></span>

[<span data-ttu-id="47385-154">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="47385-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="47385-155">Viðvörunareining</span><span class="sxs-lookup"><span data-stu-id="47385-155">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="47385-156">Eining með fjölbreyttu efni</span><span class="sxs-lookup"><span data-stu-id="47385-156">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="47385-157">Staðsetningareining efnis</span><span class="sxs-lookup"><span data-stu-id="47385-157">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="47385-158">Eiginleikaeining</span><span class="sxs-lookup"><span data-stu-id="47385-158">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="47385-159">Hetjueining</span><span class="sxs-lookup"><span data-stu-id="47385-159">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="47385-160">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="47385-160">Video player module</span></span>](add-video-player.md)
