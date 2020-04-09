---
title: Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar
description: Þetta efnisatriði lýsir því hvernig hægt er að bæta skriftarkóða biðlara við síður svæðisins til að styðja söfnun fjarmælinga biðlara.
author: bicyclingfool
manager: annbe
ms.date: 03/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 81c36685c1eccceb2f1854fe7c866186120c08a3
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154087"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="037f2-103">Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar</span><span class="sxs-lookup"><span data-stu-id="037f2-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="037f2-104">Þetta efnisatriði lýsir því hvernig hægt er að bæta skriftarkóða biðlara við síður svæðisins til að styðja söfnun fjarmælinga biðlara.</span><span class="sxs-lookup"><span data-stu-id="037f2-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="037f2-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="037f2-105">Overview</span></span>

<span data-ttu-id="037f2-106">Vefgreining er ómissandi tæki þegar þú vilt skilja hvernig viðskiptavinir þínir hafa samskipti við vefsíðuna og taka ákvarðanir sem munu hjálpa til við að hámarka upplifunina fyrir hámarks umreikning.</span><span class="sxs-lookup"><span data-stu-id="037f2-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="037f2-107">Margir vefgreiningarpakkar eru í boði til að hjálpa þér að ná þessum markmiðum, eins og Google Analytics, Clicky, Moz Analytics og KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="037f2-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="037f2-108">Flestir vefgreiningarpakkar krefjast þess að þú bætir við skriftarkóða biðlarans í **\<höfuð\>**-þáttinn í HTML fyrir allar síður á vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="037f2-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="037f2-109">Leiðbeiningarnar í þessu efni eiga einnig við um aðra sérsniðna virkni biðlara sem Microsoft Dynamics 365 Commerce býður ekki staðbundið.</span><span class="sxs-lookup"><span data-stu-id="037f2-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a><span data-ttu-id="037f2-110">Stofnaðu endurnýtanlegt síðubrot fyrir forskriftarkóðann</span><span class="sxs-lookup"><span data-stu-id="037f2-110">Create a reusable page fragment for your script code</span></span>

<span data-ttu-id="037f2-111">Síðubrot gerir þér kleift að endurnýta innbyggðan eða ytri forskriftarkóða á öllum síðum á vefsvæði þínu, óháð sniðmátinu sem þeir nota.</span><span class="sxs-lookup"><span data-stu-id="037f2-111">A page fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a><span data-ttu-id="037f2-112">Stofna endurnýtanlegt síðubrot fyrir innbyggðan forskriftarkóðann</span><span class="sxs-lookup"><span data-stu-id="037f2-112">Create a reusable page fragment for your inline script code</span></span>

<span data-ttu-id="037f2-113">Fylgdu þessum skrefum til að búa til endurnýtanlegt blaðsíðubrot fyrir innbyggðan forskriftarkóðann.</span><span class="sxs-lookup"><span data-stu-id="037f2-113">To create a reusable page fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="037f2-114">Farðu í **Síðubrot** og veldu síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="037f2-114">Go to **Page Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="037f2-115">Í valmyndinni **Nýtt síðubrot** velurðu **Innbyggð forskrift**.</span><span class="sxs-lookup"><span data-stu-id="037f2-115">In the **New Page Fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="037f2-116">Undir **Heiti síðubrots** slærðu inn heiti fyrir brotið og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="037f2-116">Under **Page Fragment Name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="037f2-117">Undir síðubrotinu sem þú stofnaðir velurðu eininguna **Sjálfgefin innbyggð forskrift**.</span><span class="sxs-lookup"><span data-stu-id="037f2-117">Under the page fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="037f2-118">Í eiginleikarrúðunni til hægri, undir **Innbyggð forskrift**, slærðu inn forskrift viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="037f2-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="037f2-119">Stilltu síðan aðra valkosti eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="037f2-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="037f2-120">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="037f2-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="037f2-121">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="037f2-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a><span data-ttu-id="037f2-122">Stofna endurnýtanlegt síðubrot fyrir ytri forskriftarkóðann</span><span class="sxs-lookup"><span data-stu-id="037f2-122">Create a reusable page fragment for your external script code</span></span>

<span data-ttu-id="037f2-123">Fylgdu þessum skrefum til að búa til endurnýtanlegt blaðsíðubrot fyrir ytri forskriftarkóðann.</span><span class="sxs-lookup"><span data-stu-id="037f2-123">To create a reusable page fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="037f2-124">Farðu í **Síðubrot** og veldu síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="037f2-124">Go to **Page Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="037f2-125">Í valmyndinni **Nýtt síðubrot** velurðu **Ytri forskrift**.</span><span class="sxs-lookup"><span data-stu-id="037f2-125">In the **New Page Fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="037f2-126">Undir **Heiti síðubrots** slærðu inn heiti fyrir brotið og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="037f2-126">Under **Page Fragment Name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="037f2-127">Undir síðubrotinu sem þú stofnaðir velurðu eininguna **Sjálfgefin ytri forskrift**.</span><span class="sxs-lookup"><span data-stu-id="037f2-127">Under the page fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="037f2-128">Í eiginleikaglugganum til hægri, undir **Uppruni forskriftar**, bætirðu við ytri eða tengdri slóð fyrir ytri uppruna forskriftar.</span><span class="sxs-lookup"><span data-stu-id="037f2-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="037f2-129">Stilltu síðan aðra valkosti eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="037f2-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="037f2-130">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="037f2-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="037f2-131">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="037f2-131">Select **Publish**.</span></span>

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="037f2-132">Bættu síðubroti sem inniheldur forskriftakóða í sniðmát</span><span class="sxs-lookup"><span data-stu-id="037f2-132">Add a page fragment that includes script code to a template</span></span>

<span data-ttu-id="037f2-133">Fylgdu þessum skrefum til að bæta við síðubroti sem inniheldur forskriftarkóða í sniðmát í vefsvæðishönnuði.</span><span class="sxs-lookup"><span data-stu-id="037f2-133">To add a page fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="037f2-134">Farðu í **Sniðmát** og opnaðu sniðmátið fyrir síðurnar sem þú vilt bæta forskriftakóðanum við.</span><span class="sxs-lookup"><span data-stu-id="037f2-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="037f2-135">Stækkaðu sniðmát stigveldisins í vinstri glugganum til að sýna hólfið **HTML-höfuð**.</span><span class="sxs-lookup"><span data-stu-id="037f2-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="037f2-136">Í hólfinu **HTML-haus** velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við síðubroti**.</span><span class="sxs-lookup"><span data-stu-id="037f2-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="037f2-137">Veldu brotið sem þú bjóst til fyrir forskriftakóðann.</span><span class="sxs-lookup"><span data-stu-id="037f2-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="037f2-138">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="037f2-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="037f2-139">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="037f2-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="037f2-140">Bæta ytri eða innbyggðri forskrift beint við sniðmát</span><span class="sxs-lookup"><span data-stu-id="037f2-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="037f2-141">Ef þú vilt setja innbyggðar eða ytri forskriftir beint inn í mengi af síðum sem er stjórnað af einu sniðmáti þarftu ekki að búa til síðubrot fyrst.</span><span class="sxs-lookup"><span data-stu-id="037f2-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a page fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="037f2-142">Bæta innbyggðri forskrift beint við sniðmát</span><span class="sxs-lookup"><span data-stu-id="037f2-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="037f2-143">Fylgdu þessum skrefum til að bæta innbyggðri forskrift beint við sniðmát í vefsvæðishönnuði.</span><span class="sxs-lookup"><span data-stu-id="037f2-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="037f2-144">Farðu í **Sniðmát** og opnaðu sniðmátið fyrir síðurnar sem þú vilt bæta forskriftakóðanum við.</span><span class="sxs-lookup"><span data-stu-id="037f2-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="037f2-145">Stækkaðu sniðmát stigveldisins í vinstri glugganum til að sýna hólfið **HTML-höfuð**.</span><span class="sxs-lookup"><span data-stu-id="037f2-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="037f2-146">Í hólfinu **HTML-haus** velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="037f2-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="037f2-147">Í valmyndinni **Bæta við einingu** velurðu **Innbyggð forskrift**.</span><span class="sxs-lookup"><span data-stu-id="037f2-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="037f2-148">Í eiginleikarrúðunni til hægri, undir **Innbyggð forskrift**, slærðu inn forskrift viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="037f2-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="037f2-149">Stilltu síðan aðra valkosti eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="037f2-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="037f2-150">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="037f2-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="037f2-151">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="037f2-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="037f2-152">Bæta ytri forskrift beint við sniðmát</span><span class="sxs-lookup"><span data-stu-id="037f2-152">Add an external script directly to a template</span></span>

<span data-ttu-id="037f2-153">Fylgdu þessum skrefum til að bæta ytri forskrift beint við sniðmát í vefsvæðishönnuði.</span><span class="sxs-lookup"><span data-stu-id="037f2-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="037f2-154">Farðu í **Sniðmát** og opnaðu sniðmátið fyrir síðurnar sem þú vilt bæta forskriftakóðanum við.</span><span class="sxs-lookup"><span data-stu-id="037f2-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="037f2-155">Stækkaðu sniðmát stigveldisins í vinstri glugganum til að sýna hólfið **HTML-höfuð**.</span><span class="sxs-lookup"><span data-stu-id="037f2-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="037f2-156">Í hólfinu **HTML-haus** velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="037f2-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="037f2-157">Í valmyndinni **Bæta við einingu** velurðu **Ytri forskrift**.</span><span class="sxs-lookup"><span data-stu-id="037f2-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="037f2-158">Í eiginleikaglugganum til hægri, undir **Uppruni forskriftar**, bætirðu við ytri eða tengdri slóð fyrir ytri uppruna forskriftar.</span><span class="sxs-lookup"><span data-stu-id="037f2-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="037f2-159">Stilltu síðan aðra valkosti eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="037f2-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="037f2-160">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="037f2-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="037f2-161">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="037f2-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="037f2-162">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="037f2-162">Additional resources</span></span>

[<span data-ttu-id="037f2-163">Bæta við lógói</span><span class="sxs-lookup"><span data-stu-id="037f2-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="037f2-164">Velja þema svæðis</span><span class="sxs-lookup"><span data-stu-id="037f2-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="037f2-165">Unnið með CSS hnekkiskrám</span><span class="sxs-lookup"><span data-stu-id="037f2-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="037f2-166">Bæta við táknmynd</span><span class="sxs-lookup"><span data-stu-id="037f2-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="037f2-167">Bæta við opnunarkveðju</span><span class="sxs-lookup"><span data-stu-id="037f2-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="037f2-168">Bæta við yfirlýsingu um höfundarrétt</span><span class="sxs-lookup"><span data-stu-id="037f2-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="037f2-169">Bæta tungumálum við síðuna</span><span class="sxs-lookup"><span data-stu-id="037f2-169">Add languages to your site</span></span>](add-languages-to-site.md)
