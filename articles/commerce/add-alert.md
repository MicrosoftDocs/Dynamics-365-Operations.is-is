---
title: Auglýsingaborðaeining
description: Þetta efni fjallar um auglysingaborðaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.openlocfilehash: d9debd16b18300d090bde1862a16920d8e9185eb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413074"
---
# <a name="promo-banner-module"></a><span data-ttu-id="fa7b3-103">Auglýsingaborðaeining</span><span class="sxs-lookup"><span data-stu-id="fa7b3-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="fa7b3-104">Þetta efni fjallar um auglysingaborðaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fa7b3-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="fa7b3-105">Overview</span></span>

<span data-ttu-id="fa7b3-106">Auglýsingaborðaeiningar eru notaðar til að sýna upplýsingarskilaboð á síðu.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="fa7b3-107">Hægt er að nota þær til að sýna kynningar á öllu svæðinu sem birtast á öllum síðum svæðis rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="fa7b3-108">Auglýsingaborðaeiningar styðja textaskilaboð og tengil.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="fa7b3-109">Ef mörgum skilaboðum er bætt við auglýsingaborðaeiningar verður til myndaræmuborði sem snýst og gerir viðskiptavinum kleift að fletta í gegnum öll skilaboðin.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="fa7b3-110">Auglýsingaborðaeiningar eru knúnar af gögnum frá efnisstýringarkerfinu (CMS) og hægt er að setja þær á hvaða síðu sem er.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="fa7b3-111">Dæmi um notkun auglýsingaborða í rafrænum viðskiptum</span><span class="sxs-lookup"><span data-stu-id="fa7b3-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="fa7b3-112">Hægt er að nota auglýsingaborða í haus síðunnar til að sýna kynningar eða skilaboð á vefnum, eins og í eftirfarandi dæmum.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="fa7b3-113">„Árlegri útsölu lýkur eftir 10 daga“</span><span class="sxs-lookup"><span data-stu-id="fa7b3-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="fa7b3-114">„Stórsparnaður með útsölu fyrir skólann.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-114">"Save big with back to school sale.</span></span> <span data-ttu-id="fa7b3-115">Verslaðu núna."</span><span class="sxs-lookup"><span data-stu-id="fa7b3-115">Shop Now."</span></span>

<span data-ttu-id="fa7b3-116">„Verslaðu á þakkargjörðarútsölunni!“</span><span class="sxs-lookup"><span data-stu-id="fa7b3-116">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="fa7b3-117">Eftirfarandi mynd sýnir dæmi um tilboðsborða.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-117">The following image shows an example of a promo banner.</span></span>

![Dæmi um einingu tilboðsborða](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="fa7b3-119">Eiginleikar auglýsingaborðaeiningar</span><span class="sxs-lookup"><span data-stu-id="fa7b3-119">Promo banner module properties</span></span>

| <span data-ttu-id="fa7b3-120">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="fa7b3-120">Property name</span></span>             | <span data-ttu-id="fa7b3-121">Virði</span><span class="sxs-lookup"><span data-stu-id="fa7b3-121">Value</span></span>                              | <span data-ttu-id="fa7b3-122">lýsing</span><span class="sxs-lookup"><span data-stu-id="fa7b3-122">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="fa7b3-123">Skilaboð vefborða</span><span class="sxs-lookup"><span data-stu-id="fa7b3-123">Banner messages</span></span>           | <span data-ttu-id="fa7b3-124">Texti og tenglar</span><span class="sxs-lookup"><span data-stu-id="fa7b3-124">Text and links</span></span>                     | <span data-ttu-id="fa7b3-125">Úrval texta og tengla.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-125">An array of text and links.</span></span> |
| <span data-ttu-id="fa7b3-126">Sjálfvirk spilun</span><span class="sxs-lookup"><span data-stu-id="fa7b3-126">Autoplay</span></span>                  | <span data-ttu-id="fa7b3-127">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="fa7b3-127">**True** or **False**</span></span>              | <span data-ttu-id="fa7b3-128">Gildi sem gefur til kynna hvort skilaboðum sé sjálfkrafa hleypt í gegn, ef mörg skilaboð eru stillt.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-128">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="fa7b3-129">Tími á milli skyggna</span><span class="sxs-lookup"><span data-stu-id="fa7b3-129">Slide transition interval</span></span> | <span data-ttu-id="fa7b3-130">Fjöldi millisekúnda (ms)</span><span class="sxs-lookup"><span data-stu-id="fa7b3-130">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="fa7b3-131">Bilið sem er notað til að fletta í gegnum skilaboð.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-131">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="fa7b3-132">Leyfa höfnun</span><span class="sxs-lookup"><span data-stu-id="fa7b3-132">Allow dismiss</span></span>             | <span data-ttu-id="fa7b3-133">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="fa7b3-133">**True** or **False**</span></span>              | <span data-ttu-id="fa7b3-134">Ef gildi er stillt á **Satt** geta viðskiptavinir hafnað viðvöruninni.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-134">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="fa7b3-135">Sýna myndaræmuflipa</span><span class="sxs-lookup"><span data-stu-id="fa7b3-135">Show carousel flipper</span></span>     | <span data-ttu-id="fa7b3-136">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="fa7b3-136">**True** or **False**</span></span>              | <span data-ttu-id="fa7b3-137">Gildi sem gefur til kynna hvort sýna ætti myndaræmuflipana svo viðskiptavinir geti flett handvirkt í gegnum marga borðahluti.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-137">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="fa7b3-138">Textajöfnun</span><span class="sxs-lookup"><span data-stu-id="fa7b3-138">Text alignment</span></span>            | <span data-ttu-id="fa7b3-139">**Hægri**, **Vinstri** eða **Miðja**</span><span class="sxs-lookup"><span data-stu-id="fa7b3-139">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="fa7b3-140">Textajöfnunin í auglýsingaborðaeiningunni.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-140">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="fa7b3-141">Tengill</span><span class="sxs-lookup"><span data-stu-id="fa7b3-141">Link</span></span>                      | <span data-ttu-id="fa7b3-142">Slóð</span><span class="sxs-lookup"><span data-stu-id="fa7b3-142">A URL</span></span>                              | <span data-ttu-id="fa7b3-143">Slóðin fyrir valfrjálsan tengil.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-143">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="fa7b3-144">Bæta auglýsingaborðaeiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="fa7b3-144">Add a promo banner module to a page</span></span> 

<span data-ttu-id="fa7b3-145">Fylgdu þessum skrefum til að bæta auglýsingaborðaeiningu við síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-145">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="fa7b3-146">Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-146">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="fa7b3-147">Í svarglugganum **Nýtt sniðmát** undir **Heiti sniðmáts** skaltu slá inn **Sniðmát tilboðsborða** og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-147">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="fa7b3-148">Undir **Útlínur síðu** bætirðu við einingunni **Sjálfgefin síða** við hólfið **Meginmál**.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-148">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="fa7b3-149">Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-149">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="fa7b3-150">Notaðu sniðmátið sem þú bjóst til til að búa til síðu sem heitir **Auglýsingaborðasíða**.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-150">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="fa7b3-151">Í hólfinu **Aðal** á nýju síðunni bætirðu við gámaeiningu.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-151">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="fa7b3-152">Í glugganum til hægri stillirðu gildið **Breidd** á **Fylla gám**.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-152">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="fa7b3-153">Undir **Útlínur síðu** bæirðu auglýsingaborðaeiningu við gámaeininguna.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-153">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="fa7b3-154">Bættu við einum eða fleiri borðaskilaboðum í stillingunum fyrir borðaeininguna.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-154">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="fa7b3-155">Hver skilaboð geta verið með texta ásamt tengli.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-155">Each message can have text together with a link.</span></span> <span data-ttu-id="fa7b3-156">Þú getur breytt öðrum eiginleikum til að sérsníða eininguna frekar.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-156">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="fa7b3-157">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-157">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="fa7b3-158">Efst á síðunni ættirðu að sjá viðvörun sem sýnir textann sem þú bættir við.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-158">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="fa7b3-159">Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-159">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="fa7b3-160">Auglýsingaborði er venjulega notaður í hólfi síðuhausa eða hólfi undirhauss.</span><span class="sxs-lookup"><span data-stu-id="fa7b3-160">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="fa7b3-161">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="fa7b3-161">Additional resources</span></span>

[<span data-ttu-id="fa7b3-162">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="fa7b3-162">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="fa7b3-163">Myndaræmueining</span><span class="sxs-lookup"><span data-stu-id="fa7b3-163">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="fa7b3-164">Textabálkseining</span><span class="sxs-lookup"><span data-stu-id="fa7b3-164">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="fa7b3-165">Eining fyrir bálk með efni</span><span class="sxs-lookup"><span data-stu-id="fa7b3-165">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="fa7b3-166">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="fa7b3-166">Video player module</span></span>](add-video-player.md)
