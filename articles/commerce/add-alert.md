---
title: Auglýsingaborðaeining
description: Þetta efni fjallar um tilboðsborðaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: be3cc9729b58fce9ebc9885d8cb20b63114362a0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796247"
---
# <a name="promo-banner-module"></a><span data-ttu-id="aaf9a-103">Tilboðsborðaeining</span><span class="sxs-lookup"><span data-stu-id="aaf9a-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="aaf9a-104">Þetta efni fjallar um tilboðsborðaeiningar og lýsir því hvernig á að bæta þeim við vefsíður hjá Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="aaf9a-105">Auglýsingaborðaeiningar eru notaðar til að sýna upplýsingarskilaboð á síðu.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-105">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="aaf9a-106">Hægt er að nota þær til að sýna kynningar á öllu svæðinu sem birtast á öllum síðum svæðis rafrænna viðskipta.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-106">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="aaf9a-107">Auglýsingaborðaeiningar styðja textaskilaboð og tengil.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-107">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="aaf9a-108">Ef mörgum skilaboðum er bætt við auglýsingaborðaeiningar verður til myndaræmuborði sem snýst og gerir viðskiptavinum kleift að fletta í gegnum öll skilaboðin.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-108">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="aaf9a-109">Auglýsingaborðaeiningar eru knúnar af gögnum frá efnisstýringarkerfinu (CMS) og hægt er að setja þær á hvaða síðu sem er.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-109">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="aaf9a-110">Dæmi um notkun auglýsingaborða í rafrænum viðskiptum</span><span class="sxs-lookup"><span data-stu-id="aaf9a-110">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="aaf9a-111">Hægt er að nota auglýsingaborða í haus síðunnar til að sýna kynningar eða skilaboð á vefnum, eins og í eftirfarandi dæmum.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-111">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="aaf9a-112">„Árlegri útsölu lýkur eftir 10 daga“</span><span class="sxs-lookup"><span data-stu-id="aaf9a-112">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="aaf9a-113">„Stórsparnaður með útsölu fyrir skólann.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-113">"Save big with back to school sale.</span></span> <span data-ttu-id="aaf9a-114">Verslaðu núna."</span><span class="sxs-lookup"><span data-stu-id="aaf9a-114">Shop Now."</span></span>

<span data-ttu-id="aaf9a-115">„Verslaðu á þakkargjörðarútsölunni!“</span><span class="sxs-lookup"><span data-stu-id="aaf9a-115">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="aaf9a-116">Eftirfarandi mynd sýnir dæmi um tilboðsborða.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-116">The following image shows an example of a promo banner.</span></span>

![Dæmi um einingu tilboðsborða](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="aaf9a-118">Eiginleikar auglýsingaborðaeiningar</span><span class="sxs-lookup"><span data-stu-id="aaf9a-118">Promo banner module properties</span></span>

| <span data-ttu-id="aaf9a-119">Nafn eiginleika</span><span class="sxs-lookup"><span data-stu-id="aaf9a-119">Property name</span></span>             | <span data-ttu-id="aaf9a-120">Virði</span><span class="sxs-lookup"><span data-stu-id="aaf9a-120">Value</span></span>                              | <span data-ttu-id="aaf9a-121">lýsing</span><span class="sxs-lookup"><span data-stu-id="aaf9a-121">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="aaf9a-122">Skilaboð vefborða</span><span class="sxs-lookup"><span data-stu-id="aaf9a-122">Banner messages</span></span>           | <span data-ttu-id="aaf9a-123">Texti og tenglar</span><span class="sxs-lookup"><span data-stu-id="aaf9a-123">Text and links</span></span>                     | <span data-ttu-id="aaf9a-124">Úrval texta og tengla.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-124">An array of text and links.</span></span> |
| <span data-ttu-id="aaf9a-125">Sjálfvirk spilun</span><span class="sxs-lookup"><span data-stu-id="aaf9a-125">Autoplay</span></span>                  | <span data-ttu-id="aaf9a-126">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="aaf9a-126">**True** or **False**</span></span>              | <span data-ttu-id="aaf9a-127">Gildi sem gefur til kynna hvort skilaboðum sé sjálfkrafa hleypt í gegn, ef mörg skilaboð eru stillt.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-127">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="aaf9a-128">Tími á milli skyggna</span><span class="sxs-lookup"><span data-stu-id="aaf9a-128">Slide transition interval</span></span> | <span data-ttu-id="aaf9a-129">Fjöldi millisekúnda (ms)</span><span class="sxs-lookup"><span data-stu-id="aaf9a-129">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="aaf9a-130">Bilið sem er notað til að fletta í gegnum skilaboð.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-130">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="aaf9a-131">Leyfa höfnun</span><span class="sxs-lookup"><span data-stu-id="aaf9a-131">Allow dismiss</span></span>             | <span data-ttu-id="aaf9a-132">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="aaf9a-132">**True** or **False**</span></span>              | <span data-ttu-id="aaf9a-133">Ef gildi er stillt á **Satt** geta viðskiptavinir hafnað viðvöruninni.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-133">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="aaf9a-134">Sýna myndaræmuflipa</span><span class="sxs-lookup"><span data-stu-id="aaf9a-134">Show carousel flipper</span></span>     | <span data-ttu-id="aaf9a-135">**Satt** eða **Ósatt**</span><span class="sxs-lookup"><span data-stu-id="aaf9a-135">**True** or **False**</span></span>              | <span data-ttu-id="aaf9a-136">Gildi sem gefur til kynna hvort sýna ætti myndaræmuflipana svo viðskiptavinir geti flett handvirkt í gegnum marga borðahluti.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-136">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="aaf9a-137">Textajöfnun</span><span class="sxs-lookup"><span data-stu-id="aaf9a-137">Text alignment</span></span>            | <span data-ttu-id="aaf9a-138">**Hægri**, **Vinstri** eða **Miðja**</span><span class="sxs-lookup"><span data-stu-id="aaf9a-138">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="aaf9a-139">Textajöfnunin í auglýsingaborðaeiningunni.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-139">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="aaf9a-140">Tengill</span><span class="sxs-lookup"><span data-stu-id="aaf9a-140">Link</span></span>                      | <span data-ttu-id="aaf9a-141">Slóð</span><span class="sxs-lookup"><span data-stu-id="aaf9a-141">A URL</span></span>                              | <span data-ttu-id="aaf9a-142">Slóðin fyrir valfrjálsan tengil.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-142">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="aaf9a-143">Bæta auglýsingaborðaeiningu við síðu</span><span class="sxs-lookup"><span data-stu-id="aaf9a-143">Add a promo banner module to a page</span></span> 

<span data-ttu-id="aaf9a-144">Fylgdu þessum skrefum til að bæta auglýsingaborðaeiningu við síðu og stilla nauðsynlega eiginleika.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-144">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="aaf9a-145">Farðu í **Sniðmát** og veldu **Nýtt** til að búa til nýtt sniðmát.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-145">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="aaf9a-146">Í svarglugganum **Nýtt sniðmát** undir **Heiti sniðmáts** skaltu slá inn **Sniðmát tilboðsborða** og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-146">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="aaf9a-147">Undir **Útlínur síðu** bætirðu við einingunni **Sjálfgefin síða** við hólfið **Meginmál**.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-147">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="aaf9a-148">Veldu **Ljúka við breytingar** til að athuga með sniðmátið og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-148">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="aaf9a-149">Notaðu sniðmátið sem þú bjóst til til að búa til síðu sem heitir **Auglýsingaborðasíða**.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-149">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="aaf9a-150">Í hólfinu **Aðal** á nýju síðunni bætirðu við gámaeiningu.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-150">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="aaf9a-151">Í glugganum til hægri stillirðu gildið **Breidd** á **Fylla gám**.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-151">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="aaf9a-152">Undir **Útlínur síðu** bæirðu auglýsingaborðaeiningu við gámaeininguna.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-152">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="aaf9a-153">Bættu við einum eða fleiri borðaskilaboðum í stillingunum fyrir borðaeininguna.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-153">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="aaf9a-154">Hver skilaboð geta verið með texta ásamt tengli.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-154">Each message can have text together with a link.</span></span> <span data-ttu-id="aaf9a-155">Þú getur breytt öðrum eiginleikum til að sérsníða eininguna frekar.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-155">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="aaf9a-156">Veldu **Vista** og veldu síðan **Forskoðun** til að forskoða síðuna.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="aaf9a-157">Efst á síðunni ættirðu að sjá viðvörun sem sýnir textann sem þú bættir við.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-157">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="aaf9a-158">Veldu **Ljúka við breytingar** til að athuga á síðunni og veldu síðan **Birta** til að birta hana.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="aaf9a-159">Auglýsingaborði er venjulega notaður í hólfi síðuhausa eða hólfi undirhauss.</span><span class="sxs-lookup"><span data-stu-id="aaf9a-159">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="aaf9a-160">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="aaf9a-160">Additional resources</span></span>

[<span data-ttu-id="aaf9a-161">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="aaf9a-161">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="aaf9a-162">Myndaræmueining</span><span class="sxs-lookup"><span data-stu-id="aaf9a-162">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="aaf9a-163">Textabálkseining</span><span class="sxs-lookup"><span data-stu-id="aaf9a-163">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="aaf9a-164">Eining fyrir bálk með efni</span><span class="sxs-lookup"><span data-stu-id="aaf9a-164">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="aaf9a-165">Myndspilaraeining</span><span class="sxs-lookup"><span data-stu-id="aaf9a-165">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]