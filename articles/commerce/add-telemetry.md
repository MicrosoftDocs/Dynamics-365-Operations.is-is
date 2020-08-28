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
ms.openlocfilehash: 4f26ed5b6674566f579e801f4b7be63c2d0dc38d
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686815"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="c6b77-103">Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar</span><span class="sxs-lookup"><span data-stu-id="c6b77-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c6b77-104">Þetta efnisatriði lýsir því hvernig hægt er að bæta skriftarkóða biðlara við síður svæðisins til að styðja söfnun fjarmælinga biðlara.</span><span class="sxs-lookup"><span data-stu-id="c6b77-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="c6b77-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="c6b77-105">Overview</span></span>

<span data-ttu-id="c6b77-106">Vefgreining er ómissandi tæki þegar þú vilt skilja hvernig viðskiptavinir þínir hafa samskipti við vefsíðuna og taka ákvarðanir sem munu hjálpa til við að hámarka upplifunina fyrir hámarks umreikning.</span><span class="sxs-lookup"><span data-stu-id="c6b77-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="c6b77-107">Margir vefgreiningarpakkar eru í boði til að hjálpa þér að ná þessum markmiðum, eins og Google Analytics, Clicky, Moz Analytics og KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="c6b77-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="c6b77-108">Flestir vefgreiningarpakkar krefjast þess að bætt sé við skriftarkóða biðlaramegin í einingu **\<head\>** í HTML fyrir allar síður á vefsvæðinu þínu.</span><span class="sxs-lookup"><span data-stu-id="c6b77-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="c6b77-109">Leiðbeiningarnar í þessu efni eiga einnig við um aðra sérsniðna virkni biðlara sem Microsoft Dynamics 365 Commerce býður ekki staðbundið.</span><span class="sxs-lookup"><span data-stu-id="c6b77-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-page-fragment-for-your-script-code"></a><span data-ttu-id="c6b77-110">Stofnaðu endurnýtanlegt síðubrot fyrir forskriftarkóðann</span><span class="sxs-lookup"><span data-stu-id="c6b77-110">Create a reusable page fragment for your script code</span></span>

<span data-ttu-id="c6b77-111">Síðubrot gerir þér kleift að endurnýta innbyggðan eða ytri forskriftarkóða á öllum síðum á vefsvæði þínu, óháð sniðmátinu sem þeir nota.</span><span class="sxs-lookup"><span data-stu-id="c6b77-111">A page fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-inline-script-code"></a><span data-ttu-id="c6b77-112">Stofna endurnýtanlegt síðubrot fyrir innbyggðan forskriftarkóðann</span><span class="sxs-lookup"><span data-stu-id="c6b77-112">Create a reusable page fragment for your inline script code</span></span>

<span data-ttu-id="c6b77-113">Fylgdu þessum skrefum til að búa til endurnýtanlegt blaðsíðubrot fyrir innbyggðan forskriftarkóðann.</span><span class="sxs-lookup"><span data-stu-id="c6b77-113">To create a reusable page fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="c6b77-114">Farðu í **Brot** og veldu síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="c6b77-115">Í svarglugganum **Nýtt síðubrot** skal velja **Innfelld forskrift**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-115">In the **New page fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="c6b77-116">Undir **Heiti síðubrots** skal slá inn heiti brotsins og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-116">Under **Page fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="c6b77-117">Undir síðubrotinu sem þú stofnaðir velurðu eininguna **Sjálfgefin innbyggð forskrift**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-117">Under the page fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="c6b77-118">Í eiginleikarrúðunni til hægri, undir **Innbyggð forskrift**, slærðu inn forskrift viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="c6b77-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="c6b77-119">Stilltu síðan aðra valkosti eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="c6b77-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="c6b77-120">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="c6b77-121">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-page-fragment-for-your-external-script-code"></a><span data-ttu-id="c6b77-122">Stofna endurnýtanlegt síðubrot fyrir ytri forskriftarkóðann</span><span class="sxs-lookup"><span data-stu-id="c6b77-122">Create a reusable page fragment for your external script code</span></span>

<span data-ttu-id="c6b77-123">Fylgdu þessum skrefum til að búa til endurnýtanlegt blaðsíðubrot fyrir ytri forskriftarkóðann.</span><span class="sxs-lookup"><span data-stu-id="c6b77-123">To create a reusable page fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="c6b77-124">Farðu í **Brot** og veldu síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="c6b77-125">Í svarglugganum **Nýtt síðubrot** skal velja **Ytri forskrift**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-125">In the **New page fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="c6b77-126">Undir **Heiti síðubrots** skal slá inn heiti brotsins og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-126">Under **Page fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="c6b77-127">Undir síðubrotinu sem þú stofnaðir velurðu eininguna **Sjálfgefin ytri forskrift**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-127">Under the page fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="c6b77-128">Í eiginleikaglugganum til hægri, undir **Uppruni forskriftar**, bætirðu við ytri eða tengdri slóð fyrir ytri uppruna forskriftar.</span><span class="sxs-lookup"><span data-stu-id="c6b77-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="c6b77-129">Stilltu síðan aðra valkosti eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="c6b77-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="c6b77-130">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="c6b77-131">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-131">Select **Publish**.</span></span>

## <a name="add-a-page-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="c6b77-132">Bættu síðubroti sem inniheldur forskriftakóða í sniðmát</span><span class="sxs-lookup"><span data-stu-id="c6b77-132">Add a page fragment that includes script code to a template</span></span>

<span data-ttu-id="c6b77-133">Fylgdu þessum skrefum til að bæta við síðubroti sem inniheldur forskriftarkóða í sniðmát í vefsvæðishönnuði.</span><span class="sxs-lookup"><span data-stu-id="c6b77-133">To add a page fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="c6b77-134">Farðu í **Sniðmát** og opnaðu sniðmátið fyrir síðurnar sem þú vilt bæta forskriftakóðanum við.</span><span class="sxs-lookup"><span data-stu-id="c6b77-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="c6b77-135">Stækkaðu sniðmát stigveldisins í vinstri glugganum til að sýna hólfið **HTML-höfuð**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="c6b77-136">Í hólfinu **HTML-haus** velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við síðubroti**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="c6b77-137">Veldu brotið sem þú bjóst til fyrir forskriftakóðann.</span><span class="sxs-lookup"><span data-stu-id="c6b77-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="c6b77-138">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="c6b77-139">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="c6b77-140">Bæta ytri eða innbyggðri forskrift beint við sniðmát</span><span class="sxs-lookup"><span data-stu-id="c6b77-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="c6b77-141">Ef þú vilt setja innbyggðar eða ytri forskriftir beint inn í mengi af síðum sem er stjórnað af einu sniðmáti þarftu ekki að búa til síðubrot fyrst.</span><span class="sxs-lookup"><span data-stu-id="c6b77-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a page fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="c6b77-142">Bæta innbyggðri forskrift beint við sniðmát</span><span class="sxs-lookup"><span data-stu-id="c6b77-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="c6b77-143">Fylgdu þessum skrefum til að bæta innbyggðri forskrift beint við sniðmát í vefsvæðishönnuði.</span><span class="sxs-lookup"><span data-stu-id="c6b77-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="c6b77-144">Farðu í **Sniðmát** og opnaðu sniðmátið fyrir síðurnar sem þú vilt bæta forskriftakóðanum við.</span><span class="sxs-lookup"><span data-stu-id="c6b77-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="c6b77-145">Stækkaðu sniðmát stigveldisins í vinstri glugganum til að sýna hólfið **HTML-höfuð**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="c6b77-146">Í hólfinu **HTML-haus** velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c6b77-147">Í valmyndinni **Bæta við einingu** velurðu **Innbyggð forskrift**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="c6b77-148">Í eiginleikarrúðunni til hægri, undir **Innbyggð forskrift**, slærðu inn forskrift viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="c6b77-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="c6b77-149">Stilltu síðan aðra valkosti eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="c6b77-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="c6b77-150">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="c6b77-151">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="c6b77-152">Bæta ytri forskrift beint við sniðmát</span><span class="sxs-lookup"><span data-stu-id="c6b77-152">Add an external script directly to a template</span></span>

<span data-ttu-id="c6b77-153">Fylgdu þessum skrefum til að bæta ytri forskrift beint við sniðmát í vefsvæðishönnuði.</span><span class="sxs-lookup"><span data-stu-id="c6b77-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="c6b77-154">Farðu í **Sniðmát** og opnaðu sniðmátið fyrir síðurnar sem þú vilt bæta forskriftakóðanum við.</span><span class="sxs-lookup"><span data-stu-id="c6b77-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="c6b77-155">Stækkaðu sniðmát stigveldisins í vinstri glugganum til að sýna hólfið **HTML-höfuð**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="c6b77-156">Í hólfinu **HTML-haus** velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="c6b77-157">Í valmyndinni **Bæta við einingu** velurðu **Ytri forskrift**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="c6b77-158">Í eiginleikaglugganum til hægri, undir **Uppruni forskriftar**, bætirðu við ytri eða tengdri slóð fyrir ytri uppruna forskriftar.</span><span class="sxs-lookup"><span data-stu-id="c6b77-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="c6b77-159">Stilltu síðan aðra valkosti eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="c6b77-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="c6b77-160">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="c6b77-161">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="c6b77-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c6b77-162">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c6b77-162">Additional resources</span></span>

[<span data-ttu-id="c6b77-163">Bæta við lógói</span><span class="sxs-lookup"><span data-stu-id="c6b77-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="c6b77-164">Velja þema svæðis</span><span class="sxs-lookup"><span data-stu-id="c6b77-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="c6b77-165">Unnið með CSS hnekkiskrám</span><span class="sxs-lookup"><span data-stu-id="c6b77-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="c6b77-166">Bæta við táknmynd</span><span class="sxs-lookup"><span data-stu-id="c6b77-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="c6b77-167">Bæta við opnunarkveðju</span><span class="sxs-lookup"><span data-stu-id="c6b77-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="c6b77-168">Bæta við yfirlýsingu um höfundarrétt</span><span class="sxs-lookup"><span data-stu-id="c6b77-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="c6b77-169">Bæta tungumálum við síðuna</span><span class="sxs-lookup"><span data-stu-id="c6b77-169">Add languages to your site</span></span>](add-languages-to-site.md)
