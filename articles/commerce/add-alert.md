---
title: Auglýsingaborðaeining
description: Þetta efni fjallar um auglysingaborðaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: da5e220e4578d1064eb7b627b441d3f585b3c095
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025621"
---
# <a name="promo-banner-module"></a><span data-ttu-id="12522-103">Auglýsingaborðaeining</span><span class="sxs-lookup"><span data-stu-id="12522-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="12522-104">Þetta efni fjallar um auglysingaborðaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="12522-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="12522-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="12522-105">Overview</span></span>

<span data-ttu-id="12522-106">Auglýsingaborðaeiningar eru notaðar til að sýna upplýsingarskilaboð á síðu.</span><span class="sxs-lookup"><span data-stu-id="12522-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="12522-107">Hægt er að nota þær til að sýna kynningar á öllu svæðinu sem birtast á öllum síðum svæðis rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="12522-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="12522-108">Auglýsingaborðaeiningar styðja textaskilaboð og tengil.</span><span class="sxs-lookup"><span data-stu-id="12522-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="12522-109">Ef mörgum skilaboðum er bætt við auglýsingaborðaeiningar verður til myndaræmuborði sem snýst og gerir viðskiptavinum kleift að fletta í gegnum öll skilaboðin.</span><span class="sxs-lookup"><span data-stu-id="12522-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="12522-110">Auglýsingaborðaeiningar eru knúnar af gögnum frá efnisstýringarkerfinu (CMS) og hægt er að setja þær á hvaða síðu sem er.</span><span class="sxs-lookup"><span data-stu-id="12522-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="12522-111">Dæmi um notkun auglýsingaborða í rafrænum viðskiptum</span><span class="sxs-lookup"><span data-stu-id="12522-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="12522-112">Hægt er að nota auglýsingaborða í haus síðunnar til að sýna kynningar eða skilaboð á vefnum, eins og í eftirfarandi dæmum.</span><span class="sxs-lookup"><span data-stu-id="12522-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="12522-113">„Árlegri útsölu lýkur eftir 10 daga“</span><span class="sxs-lookup"><span data-stu-id="12522-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="12522-114">„Stórsparnaður með útsölu fyrir skólann.</span><span class="sxs-lookup"><span data-stu-id="12522-114">"Save big with back to school sale.</span></span> <span data-ttu-id="12522-115">Verslaðu núna."</span><span class="sxs-lookup"><span data-stu-id="12522-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="12522-116">Eiginleikar auglýsingaborðaeiningar</span><span class="sxs-lookup"><span data-stu-id="12522-116">Promo banner module properties</span></span>

| <span data-ttu-id="12522-117">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="12522-117">Property name</span></span>             | <span data-ttu-id="12522-118">Value</span><span class="sxs-lookup"><span data-stu-id="12522-118">Value</span></span>                              | <span data-ttu-id="12522-119">Lýsing</span><span class="sxs-lookup"><span data-stu-id="12522-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="12522-120">Skilaboð vefborða</span><span class="sxs-lookup"><span data-stu-id="12522-120">Banner messages</span></span>           | <span data-ttu-id="12522-121">Texti og tenglar</span><span class="sxs-lookup"><span data-stu-id="12522-121">Text and links</span></span>                     | <span data-ttu-id="12522-122">Úrval texta og tengla.</span><span class="sxs-lookup"><span data-stu-id="12522-122">An array of text and links.</span></span> |
| <span data-ttu-id="12522-123">Sjálfvirk spilun</span><span class="sxs-lookup"><span data-stu-id="12522-123">Autoplay</span></span>                  | <span data-ttu-id="12522-124">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="12522-124">**True** or **False**</span></span>              | <span data-ttu-id="12522-125">Gildi sem gefur til kynna hvort skilaboðum sé sjálfkrafa hleypt í gegn, ef mörg skilaboð eru stillt.</span><span class="sxs-lookup"><span data-stu-id="12522-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="12522-126">Tími á milli skyggna</span><span class="sxs-lookup"><span data-stu-id="12522-126">Slide transition interval</span></span> | <span data-ttu-id="12522-127">Fjöldi millisekúnda (ms)</span><span class="sxs-lookup"><span data-stu-id="12522-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="12522-128">Bilið sem er notað til að fletta í gegnum skilaboð.</span><span class="sxs-lookup"><span data-stu-id="12522-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="12522-129">Leyfa höfnun</span><span class="sxs-lookup"><span data-stu-id="12522-129">Allow dismiss</span></span>             | <span data-ttu-id="12522-130">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="12522-130">**True** or **False**</span></span>              | <span data-ttu-id="12522-131">Ef gildi er stillt á **Satt** geta viðskiptavinir hafnað viðvöruninni.</span><span class="sxs-lookup"><span data-stu-id="12522-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="12522-132">Sýna myndaræmuflipa</span><span class="sxs-lookup"><span data-stu-id="12522-132">Show carousel flipper</span></span>     | <span data-ttu-id="12522-133">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="12522-133">**True** or **False**</span></span>              | <span data-ttu-id="12522-134">Gildi sem gefur til kynna hvort sýna ætti myndaræmuflipana svo viðskiptavinir geti flett handvirkt í gegnum marga borðahluti.</span><span class="sxs-lookup"><span data-stu-id="12522-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="12522-135">Textajöfnun</span><span class="sxs-lookup"><span data-stu-id="12522-135">Text alignment</span></span>            | <span data-ttu-id="12522-136">**Hægri**, **Vinstri** eða **Miðja**</span><span class="sxs-lookup"><span data-stu-id="12522-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="12522-137">Textajöfnunin í auglýsingaborðaeiningunni.</span><span class="sxs-lookup"><span data-stu-id="12522-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="12522-138">Tengill</span><span class="sxs-lookup"><span data-stu-id="12522-138">Link</span></span>                      | <span data-ttu-id="12522-139">Slóð</span><span class="sxs-lookup"><span data-stu-id="12522-139">A URL</span></span>                              | <span data-ttu-id="12522-140">Slóðin fyrir valfrjálsan tengil.</span><span class="sxs-lookup"><span data-stu-id="12522-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="12522-141">Bæta auglýsingaborðaeiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="12522-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="12522-142">Fylgdu þessum skrefum til að bæta auglýsingaborðaeiningu við síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="12522-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="12522-143">Búðu til síðusniðmát sem heitir **Auglýsingaborðasniðmát**.</span><span class="sxs-lookup"><span data-stu-id="12522-143">Create a page template that is named **Promo banner template**.</span></span>
1. <span data-ttu-id="12522-144">Undir **Útlínur síðu** bætirðu við einingunni **Sjálfgefin síða** við hólfið **Meginmál**.</span><span class="sxs-lookup"><span data-stu-id="12522-144">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="12522-145">Skráðu brotið út í sniðmátinu og birtu það.</span><span class="sxs-lookup"><span data-stu-id="12522-145">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="12522-146">Notaðu sniðmátið sem þú bjóst til til að búa til síðu sem heitir **Auglýsingaborðasíða**.</span><span class="sxs-lookup"><span data-stu-id="12522-146">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="12522-147">Í hólfinu **Aðal** á nýju síðunni bætirðu við gámaeiningu.</span><span class="sxs-lookup"><span data-stu-id="12522-147">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="12522-148">Í glugganum til hægri stillirðu gildið **Breidd** á **Fylla gám**.</span><span class="sxs-lookup"><span data-stu-id="12522-148">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="12522-149">Undir **Útlínur síðu** bæirðu auglýsingaborðaeiningu við gámaeininguna.</span><span class="sxs-lookup"><span data-stu-id="12522-149">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="12522-150">Bættu við einum eða fleiri borðaskilaboðum í stillingunum fyrir borðaeininguna.</span><span class="sxs-lookup"><span data-stu-id="12522-150">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="12522-151">Hver skilaboð geta verið með texta ásamt tengli.</span><span class="sxs-lookup"><span data-stu-id="12522-151">Each message can have text together with a link.</span></span> <span data-ttu-id="12522-152">Þú getur breytt öðrum eiginleikum til að sérsníða eininguna frekar.</span><span class="sxs-lookup"><span data-stu-id="12522-152">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="12522-153">Vistaðu og forskoðaðu síðuna.</span><span class="sxs-lookup"><span data-stu-id="12522-153">Save and preview the page.</span></span> <span data-ttu-id="12522-154">Efst á síðunni ættirðu að sjá viðvörun sem sýnir textann sem þú bættir við.</span><span class="sxs-lookup"><span data-stu-id="12522-154">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="12522-155">Ljúktu við að breyta síðunni, vistaðu hana og birtu.</span><span class="sxs-lookup"><span data-stu-id="12522-155">Finish editing the page, and publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="12522-156">Auglýsingaborði er venjulega notaður í hólfi síðuhausa eða hólfi undirhauss.</span><span class="sxs-lookup"><span data-stu-id="12522-156">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="12522-157">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="12522-157">Additional resources</span></span>

[<span data-ttu-id="12522-158">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="12522-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="12522-159">Myndaræmueining</span><span class="sxs-lookup"><span data-stu-id="12522-159">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="12522-160">Textabálkseining</span><span class="sxs-lookup"><span data-stu-id="12522-160">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="12522-161">Innihaldsbálkseining</span><span class="sxs-lookup"><span data-stu-id="12522-161">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="12522-162">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="12522-162">Video player module</span></span>](add-video-player.md)
