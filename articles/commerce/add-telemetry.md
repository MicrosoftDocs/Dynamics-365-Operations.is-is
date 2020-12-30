---
title: Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar
description: Þetta efnisatriði lýsir því hvernig hægt er að bæta skriftarkóða biðlara við síður svæðisins til að styðja söfnun fjarmælinga biðlara.
author: bicyclingfool
manager: annbe
ms.date: 09/29/2020
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
ms.openlocfilehash: e15ba6a0d624bd97c25936aa6d3bfafb844b66c0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413102"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="db055-103">Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar</span><span class="sxs-lookup"><span data-stu-id="db055-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="db055-104">Þetta efnisatriði lýsir því hvernig hægt er að bæta skriftarkóða biðlara við síður svæðisins til að styðja söfnun fjarmælinga biðlara.</span><span class="sxs-lookup"><span data-stu-id="db055-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="db055-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="db055-105">Overview</span></span>

<span data-ttu-id="db055-106">Vefgreining er ómissandi tæki þegar þú vilt skilja hvernig viðskiptavinir þínir hafa samskipti við vefsíðuna og taka ákvarðanir sem munu hjálpa til við að hámarka upplifunina fyrir hámarks umreikning.</span><span class="sxs-lookup"><span data-stu-id="db055-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="db055-107">Margir vefgreiningarpakkar eru í boði til að hjálpa þér að ná þessum markmiðum, eins og Google Analytics, Clicky, Moz Analytics og KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="db055-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="db055-108">Flestir vefgreiningarpakkar krefjast þess að bætt sé við skriftarkóða biðlaramegin í einingu **\<head\>** í HTML fyrir allar síður á vefsvæðinu þínu.</span><span class="sxs-lookup"><span data-stu-id="db055-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="db055-109">Leiðbeiningarnar í þessu efni eiga einnig við um aðra sérsniðna virkni biðlara sem Microsoft Dynamics 365 Commerce býður ekki staðbundið.</span><span class="sxs-lookup"><span data-stu-id="db055-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="db055-110">Stofnaðu endurnýtanlegt brot fyrir skriftarkóðann</span><span class="sxs-lookup"><span data-stu-id="db055-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="db055-111">Brot gerir þér kleift að endurnýta innfelldan eða ytri skriftarkóða á öllum síðum á svæðinu, óháð sniðmátinu sem er notað.</span><span class="sxs-lookup"><span data-stu-id="db055-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="db055-112">Búa til endurnýtanlegt brot fyrir innbyggðan skriftarkóða</span><span class="sxs-lookup"><span data-stu-id="db055-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="db055-113">Til að búa til endurnýtanlegt brot fyrir innbyggðan skriftarkóðann í svæðasmíði skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="db055-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="db055-114">Farðu í **Brot** og veldu síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="db055-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="db055-115">Í svarglugganum **Nýtt brot** skal velja **Innfelld forskrift**.</span><span class="sxs-lookup"><span data-stu-id="db055-115">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="db055-116">Undir **Heiti brots** skal slá inn heiti brotsins og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="db055-116">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="db055-117">Undir broti sem þú bjóst til skaltu velja **Sjálfgefin innfelld eining forskriftar**.</span><span class="sxs-lookup"><span data-stu-id="db055-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="db055-118">Í eiginleikarrúðunni til hægri, undir **Innbyggð forskrift**, slærðu inn forskrift viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="db055-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="db055-119">Stilltu síðan aðra valkosti eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="db055-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="db055-120">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="db055-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="db055-121">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="db055-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="db055-122">Búa til endurnýtanlegt brot fyrir ytri skriftarkóða</span><span class="sxs-lookup"><span data-stu-id="db055-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="db055-123">Til að búa til endurnýtanlegt brot fyrir ytri skriftarkóða í svæðasmíði skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="db055-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="db055-124">Farðu í **Brot** og veldu síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="db055-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="db055-125">Í svarglugganum **Nýtt brot** skal velja **Ytri forskrift**.</span><span class="sxs-lookup"><span data-stu-id="db055-125">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="db055-126">Undir **Heiti brots** skal slá inn heiti brotsins og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="db055-126">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="db055-127">Í brotinu sem þú býrð til skaltu velja **Sjálfgefin ytri eining forskriftar**.</span><span class="sxs-lookup"><span data-stu-id="db055-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="db055-128">Í eiginleikaglugganum til hægri, undir **Uppruni forskriftar**, bætirðu við ytri eða tengdri slóð fyrir ytri uppruna forskriftar.</span><span class="sxs-lookup"><span data-stu-id="db055-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="db055-129">Stilltu síðan aðra valkosti eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="db055-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="db055-130">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="db055-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="db055-131">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="db055-131">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="db055-132">Ef öryggisregla fyrir efni (CSP) er virkjuð fyrir svæðið þitt, skaltu ganga úr skugga um að öllum ytri vefslóðum sé bætt við CSP-leiðbeininguna **script-src** í svæðishönnuð Commerce.</span><span class="sxs-lookup"><span data-stu-id="db055-132">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="db055-133">Frekari upplýsingar er að finna í [Stjórna öryggisreglu fyrir efni (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="db055-133">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="db055-134">Bæta við broti sem inniheldur skriftarkóða í sniðmát</span><span class="sxs-lookup"><span data-stu-id="db055-134">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="db055-135">Til að bæta við hluta sem inniheldur skriftarkóða í sniðmát í svæðasmíði skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="db055-135">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="db055-136">Farðu í **Sniðmát** og opnaðu sniðmátið fyrir síðurnar sem þú vilt bæta forskriftakóðanum við.</span><span class="sxs-lookup"><span data-stu-id="db055-136">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="db055-137">Stækkaðu sniðmát stigveldisins í vinstri glugganum til að sýna hólfið **HTML-höfuð**.</span><span class="sxs-lookup"><span data-stu-id="db055-137">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="db055-138">Í **HTML-haus** skaltu velja hnapp úrfellingarmerkis (**...**) og svo **Bæta við broti**.</span><span class="sxs-lookup"><span data-stu-id="db055-138">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="db055-139">Veldu brotið sem þú bjóst til fyrir forskriftakóðann.</span><span class="sxs-lookup"><span data-stu-id="db055-139">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="db055-140">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="db055-140">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="db055-141">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="db055-141">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="db055-142">Bæta ytri eða innbyggðri forskrift beint við sniðmát</span><span class="sxs-lookup"><span data-stu-id="db055-142">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="db055-143">Ef ætlunin er að setja innfellda eða ytri forskrift beint inn í safn af síðum sem eru stýrðar með einu sniðmáti þarf ekki að búa fyrst til brotið.</span><span class="sxs-lookup"><span data-stu-id="db055-143">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="db055-144">Bæta innbyggðri forskrift beint við sniðmát</span><span class="sxs-lookup"><span data-stu-id="db055-144">Add an inline script directly to a template</span></span>

<span data-ttu-id="db055-145">Fylgdu þessum skrefum til að bæta innbyggðri forskrift beint við sniðmát í vefsvæðishönnuði.</span><span class="sxs-lookup"><span data-stu-id="db055-145">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="db055-146">Farðu í **Sniðmát** og opnaðu sniðmátið fyrir síðurnar sem þú vilt bæta forskriftakóðanum við.</span><span class="sxs-lookup"><span data-stu-id="db055-146">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="db055-147">Stækkaðu sniðmát stigveldisins í vinstri glugganum til að sýna hólfið **HTML-höfuð**.</span><span class="sxs-lookup"><span data-stu-id="db055-147">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="db055-148">Í hólfinu **HTML-haus** velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="db055-148">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="db055-149">Í valmyndinni **Bæta við einingu** velurðu **Innbyggð forskrift**.</span><span class="sxs-lookup"><span data-stu-id="db055-149">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="db055-150">Í eiginleikarrúðunni til hægri, undir **Innbyggð forskrift**, slærðu inn forskrift viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="db055-150">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="db055-151">Stilltu síðan aðra valkosti eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="db055-151">Then configure other options as you require.</span></span>
1. <span data-ttu-id="db055-152">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="db055-152">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="db055-153">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="db055-153">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="db055-154">Bæta ytri forskrift beint við sniðmát</span><span class="sxs-lookup"><span data-stu-id="db055-154">Add an external script directly to a template</span></span>

<span data-ttu-id="db055-155">Fylgdu þessum skrefum til að bæta ytri forskrift beint við sniðmát í vefsvæðishönnuði.</span><span class="sxs-lookup"><span data-stu-id="db055-155">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="db055-156">Farðu í **Sniðmát** og opnaðu sniðmátið fyrir síðurnar sem þú vilt bæta forskriftakóðanum við.</span><span class="sxs-lookup"><span data-stu-id="db055-156">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="db055-157">Stækkaðu sniðmát stigveldisins í vinstri glugganum til að sýna hólfið **HTML-höfuð**.</span><span class="sxs-lookup"><span data-stu-id="db055-157">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="db055-158">Í hólfinu **HTML-haus** velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="db055-158">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="db055-159">Í valmyndinni **Bæta við einingu** velurðu **Ytri forskrift**.</span><span class="sxs-lookup"><span data-stu-id="db055-159">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="db055-160">Í eiginleikaglugganum til hægri, undir **Uppruni forskriftar**, bætirðu við ytri eða tengdri slóð fyrir ytri uppruna forskriftar.</span><span class="sxs-lookup"><span data-stu-id="db055-160">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="db055-161">Stilltu síðan aðra valkosti eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="db055-161">Then configure other options as you require.</span></span>
1. <span data-ttu-id="db055-162">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="db055-162">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="db055-163">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="db055-163">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db055-164">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="db055-164">Additional resources</span></span>

[<span data-ttu-id="db055-165">Bæta við lógói</span><span class="sxs-lookup"><span data-stu-id="db055-165">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="db055-166">Velja þema svæðis</span><span class="sxs-lookup"><span data-stu-id="db055-166">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="db055-167">Unnið með CSS hnekkiskrám</span><span class="sxs-lookup"><span data-stu-id="db055-167">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="db055-168">Bæta við táknmynd</span><span class="sxs-lookup"><span data-stu-id="db055-168">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="db055-169">Bæta við opnunarkveðju</span><span class="sxs-lookup"><span data-stu-id="db055-169">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="db055-170">Bæta við yfirlýsingu um höfundarrétt</span><span class="sxs-lookup"><span data-stu-id="db055-170">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="db055-171">Bæta tungumálum við síðuna</span><span class="sxs-lookup"><span data-stu-id="db055-171">Add languages to your site</span></span>](add-languages-to-site.md)
