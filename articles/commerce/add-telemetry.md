---
title: Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar
description: Þetta efnisatriði lýsir því hvernig hægt er að bæta skriftarkóða biðlara við síður svæðisins til að styðja söfnun fjarmælinga biðlara.
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fb1773ab10b23a586eb6a8286f145181818585b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797432"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="8f652-103">Bæta skriftarkóða við síður vefsvæðis til að aðstoða við fjarmælingar</span><span class="sxs-lookup"><span data-stu-id="8f652-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8f652-104">Þetta efnisatriði lýsir því hvernig hægt er að bæta skriftarkóða biðlara við síður svæðisins til að styðja söfnun fjarmælinga biðlara.</span><span class="sxs-lookup"><span data-stu-id="8f652-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

<span data-ttu-id="8f652-105">Vefgreining er ómissandi tæki þegar þú vilt skilja hvernig viðskiptavinir þínir hafa samskipti við vefsíðuna og taka ákvarðanir sem munu hjálpa til við að hámarka upplifunina fyrir hámarks umreikning.</span><span class="sxs-lookup"><span data-stu-id="8f652-105">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="8f652-106">Margir vefgreiningarpakkar eru í boði til að hjálpa þér að ná þessum markmiðum, eins og Google Analytics, Clicky, Moz Analytics og KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="8f652-106">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="8f652-107">Flestir vefgreiningarpakkar krefjast þess að bætt sé við skriftarkóða biðlaramegin í einingu **\<head\>** í HTML fyrir allar síður á vefsvæðinu þínu.</span><span class="sxs-lookup"><span data-stu-id="8f652-107">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="8f652-108">Leiðbeiningarnar í þessu efnisatriði eiga einnig við um aðra sérstillta biðlaravirkni sem Microsoft Dynamics 365 Commerce ekki er hægt að veita í öllum löndum.</span><span class="sxs-lookup"><span data-stu-id="8f652-108">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="8f652-109">Stofnaðu endurnýtanlegt brot fyrir skriftarkóðann</span><span class="sxs-lookup"><span data-stu-id="8f652-109">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="8f652-110">Brot gerir þér kleift að endurnýta innfelldan eða ytri skriftarkóða á öllum síðum á svæðinu, óháð sniðmátinu sem er notað.</span><span class="sxs-lookup"><span data-stu-id="8f652-110">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="8f652-111">Búa til endurnýtanlegt brot fyrir innbyggðan skriftarkóða</span><span class="sxs-lookup"><span data-stu-id="8f652-111">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="8f652-112">Til að búa til endurnýtanlegt brot fyrir innbyggðan skriftarkóðann í svæðasmíði skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8f652-112">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="8f652-113">Farðu í **Brot** og veldu síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="8f652-113">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="8f652-114">Í svarglugganum **Nýtt brot** skal velja **Innfelld forskrift**.</span><span class="sxs-lookup"><span data-stu-id="8f652-114">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="8f652-115">Undir **Heiti brots** skal slá inn heiti brotsins og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="8f652-115">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="8f652-116">Undir broti sem þú bjóst til skaltu velja **Sjálfgefin innfelld eining forskriftar**.</span><span class="sxs-lookup"><span data-stu-id="8f652-116">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="8f652-117">Í eiginleikarrúðunni til hægri, undir **Innbyggð forskrift**, slærðu inn forskrift viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="8f652-117">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="8f652-118">Stilltu síðan aðra valkosti eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="8f652-118">Then configure other options as you require.</span></span>
1. <span data-ttu-id="8f652-119">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="8f652-119">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="8f652-120">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="8f652-120">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="8f652-121">Búa til endurnýtanlegt brot fyrir ytri skriftarkóða</span><span class="sxs-lookup"><span data-stu-id="8f652-121">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="8f652-122">Til að búa til endurnýtanlegt brot fyrir ytri skriftarkóða í svæðasmíði skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8f652-122">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="8f652-123">Farðu í **Brot** og veldu síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="8f652-123">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="8f652-124">Í svarglugganum **Nýtt brot** skal velja **Ytri forskrift**.</span><span class="sxs-lookup"><span data-stu-id="8f652-124">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="8f652-125">Undir **Heiti brots** skal slá inn heiti brotsins og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="8f652-125">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="8f652-126">Í brotinu sem þú býrð til skaltu velja **Sjálfgefin ytri eining forskriftar**.</span><span class="sxs-lookup"><span data-stu-id="8f652-126">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="8f652-127">Í eiginleikaglugganum til hægri, undir **Uppruni forskriftar**, bætirðu við ytri eða tengdri slóð fyrir ytri uppruna forskriftar.</span><span class="sxs-lookup"><span data-stu-id="8f652-127">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="8f652-128">Stilltu síðan aðra valkosti eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="8f652-128">Then configure other options as you require.</span></span>
1. <span data-ttu-id="8f652-129">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="8f652-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="8f652-130">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="8f652-130">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="8f652-131">Ef öryggisregla fyrir efni (CSP) er virkjuð fyrir svæðið þitt, skaltu ganga úr skugga um að öllum ytri vefslóðum sé bætt við CSP-leiðbeininguna **script-src** í svæðishönnuð Commerce.</span><span class="sxs-lookup"><span data-stu-id="8f652-131">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="8f652-132">Frekari upplýsingar er að finna í [Stjórna öryggisreglu fyrir efni (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="8f652-132">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="8f652-133">Bæta við broti sem inniheldur skriftarkóða í sniðmát</span><span class="sxs-lookup"><span data-stu-id="8f652-133">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="8f652-134">Til að bæta við hluta sem inniheldur skriftarkóða í sniðmát í svæðasmíði skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="8f652-134">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="8f652-135">Farðu í **Sniðmát** og opnaðu sniðmátið fyrir síðurnar sem þú vilt bæta forskriftakóðanum við.</span><span class="sxs-lookup"><span data-stu-id="8f652-135">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="8f652-136">Stækkaðu sniðmát stigveldisins í vinstri glugganum til að sýna hólfið **HTML-höfuð**.</span><span class="sxs-lookup"><span data-stu-id="8f652-136">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="8f652-137">Í **HTML-haus** skaltu velja hnapp úrfellingarmerkis (**...**) og svo **Bæta við broti**.</span><span class="sxs-lookup"><span data-stu-id="8f652-137">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="8f652-138">Veldu brotið sem þú bjóst til fyrir forskriftakóðann.</span><span class="sxs-lookup"><span data-stu-id="8f652-138">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="8f652-139">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="8f652-139">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="8f652-140">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="8f652-140">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="8f652-141">Bæta ytri eða innbyggðri forskrift beint við sniðmát</span><span class="sxs-lookup"><span data-stu-id="8f652-141">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="8f652-142">Ef ætlunin er að setja innfellda eða ytri forskrift beint inn í safn af síðum sem eru stýrðar með einu sniðmáti þarf ekki að búa fyrst til brotið.</span><span class="sxs-lookup"><span data-stu-id="8f652-142">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="8f652-143">Bæta innbyggðri forskrift beint við sniðmát</span><span class="sxs-lookup"><span data-stu-id="8f652-143">Add an inline script directly to a template</span></span>

<span data-ttu-id="8f652-144">Fylgdu þessum skrefum til að bæta innbyggðri forskrift beint við sniðmát í vefsvæðishönnuði.</span><span class="sxs-lookup"><span data-stu-id="8f652-144">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="8f652-145">Farðu í **Sniðmát** og opnaðu sniðmátið fyrir síðurnar sem þú vilt bæta forskriftakóðanum við.</span><span class="sxs-lookup"><span data-stu-id="8f652-145">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="8f652-146">Stækkaðu sniðmát stigveldisins í vinstri glugganum til að sýna hólfið **HTML-höfuð**.</span><span class="sxs-lookup"><span data-stu-id="8f652-146">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="8f652-147">Í hólfinu **HTML-haus** velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="8f652-147">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8f652-148">Í valmyndinni **Bæta við einingu** velurðu **Innbyggð forskrift**.</span><span class="sxs-lookup"><span data-stu-id="8f652-148">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="8f652-149">Í eiginleikarrúðunni til hægri, undir **Innbyggð forskrift**, slærðu inn forskrift viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="8f652-149">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="8f652-150">Stilltu síðan aðra valkosti eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="8f652-150">Then configure other options as you require.</span></span>
1. <span data-ttu-id="8f652-151">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="8f652-151">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="8f652-152">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="8f652-152">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="8f652-153">Bæta ytri forskrift beint við sniðmát</span><span class="sxs-lookup"><span data-stu-id="8f652-153">Add an external script directly to a template</span></span>

<span data-ttu-id="8f652-154">Fylgdu þessum skrefum til að bæta ytri forskrift beint við sniðmát í vefsvæðishönnuði.</span><span class="sxs-lookup"><span data-stu-id="8f652-154">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="8f652-155">Farðu í **Sniðmát** og opnaðu sniðmátið fyrir síðurnar sem þú vilt bæta forskriftakóðanum við.</span><span class="sxs-lookup"><span data-stu-id="8f652-155">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="8f652-156">Stækkaðu sniðmát stigveldisins í vinstri glugganum til að sýna hólfið **HTML-höfuð**.</span><span class="sxs-lookup"><span data-stu-id="8f652-156">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="8f652-157">Í hólfinu **HTML-haus** velurðu úrfellingarhnappinn (**...**) og velur síðan **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="8f652-157">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8f652-158">Í valmyndinni **Bæta við einingu** velurðu **Ytri forskrift**.</span><span class="sxs-lookup"><span data-stu-id="8f652-158">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="8f652-159">Í eiginleikaglugganum til hægri, undir **Uppruni forskriftar**, bætirðu við ytri eða tengdri slóð fyrir ytri uppruna forskriftar.</span><span class="sxs-lookup"><span data-stu-id="8f652-159">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="8f652-160">Stilltu síðan aðra valkosti eins og þú þarft.</span><span class="sxs-lookup"><span data-stu-id="8f652-160">Then configure other options as you require.</span></span>
1. <span data-ttu-id="8f652-161">Veldu **Vista** og síðan **Ljúka við breytingar**.</span><span class="sxs-lookup"><span data-stu-id="8f652-161">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="8f652-162">Velja **Birta**.</span><span class="sxs-lookup"><span data-stu-id="8f652-162">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8f652-163">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8f652-163">Additional resources</span></span>

[<span data-ttu-id="8f652-164">Bæta við lógói</span><span class="sxs-lookup"><span data-stu-id="8f652-164">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="8f652-165">Velja þema svæðis</span><span class="sxs-lookup"><span data-stu-id="8f652-165">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="8f652-166">Unnið með CSS hnekkiskrám</span><span class="sxs-lookup"><span data-stu-id="8f652-166">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="8f652-167">Bæta við táknmynd</span><span class="sxs-lookup"><span data-stu-id="8f652-167">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="8f652-168">Bæta við opnunarkveðju</span><span class="sxs-lookup"><span data-stu-id="8f652-168">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="8f652-169">Bæta við yfirlýsingu um höfundarrétt</span><span class="sxs-lookup"><span data-stu-id="8f652-169">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="8f652-170">Bæta tungumálum við síðuna</span><span class="sxs-lookup"><span data-stu-id="8f652-170">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
