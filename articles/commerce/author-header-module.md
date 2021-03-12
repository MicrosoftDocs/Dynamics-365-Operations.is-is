---
title: Fyrirsagnareining
description: Þetta efni fjallar um fyrirsagnareiningar og lýsir því hvernig á að stofna síðuhausa í Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1373397c4499ed65835bcc71c6fc628ff356e4e7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991516"
---
# <a name="header-module"></a><span data-ttu-id="76e7e-103">Eining síðuhauss</span><span class="sxs-lookup"><span data-stu-id="76e7e-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="76e7e-104">Þetta efni fjallar um fyrirsagnareiningar og lýsir því hvernig á að stofna síðuhausa í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="76e7e-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="76e7e-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="76e7e-105">Overview</span></span>

<span data-ttu-id="76e7e-106">Í Dynamics 365 Commerce er síðuhaus stilltur sem síðubrot sem inniheldur haus, tilboðsborða og kökusamþykkiseiningar.</span><span class="sxs-lookup"><span data-stu-id="76e7e-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="76e7e-107">Hausaeiningin inniheldur svæðismerki, tengla á yfirlitsstigveldið, tengla á aðrar síður á svæðinu, tákneiningu körfu, tákn óskalista, innskráningarmöguleika og leitarslána.</span><span class="sxs-lookup"><span data-stu-id="76e7e-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="76e7e-108">Fyrirsagnareining er sjálfkrafa fínstillt fyrir tækið sem vefurinn er skoðaður á (með öðrum orðum, fyrir skjáborðstæki eða fartæki).</span><span class="sxs-lookup"><span data-stu-id="76e7e-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="76e7e-109">Til dæmis, í fartæki er leiðsagnarstikan smækkuð niður í hnappinn **Valmynd** (sem er stundum kallaður *hamborgaravalmynd*).</span><span class="sxs-lookup"><span data-stu-id="76e7e-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="76e7e-110">Eftirfarandi mynd sýnir dæmi um fyrirsagnareiningu á heimasíðu.</span><span class="sxs-lookup"><span data-stu-id="76e7e-110">The following image shows an example of a header module on a home page.</span></span>

![Dæmi um fyrirsagnareiningu](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="76e7e-112">Eiginleikar fyrirsagnareiningar</span><span class="sxs-lookup"><span data-stu-id="76e7e-112">Properties of a header module</span></span>

<span data-ttu-id="76e7e-113">Hauseining styður eiginleikana **Fyrirtækismerki**, **Merkjatengil** og **Mínir reikningstenglar**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="76e7e-114">Eiginleikarnir **Fyrirtækismerki** og **Merkjatengill** eru notaðir til að skilgreina merki á síðunni.</span><span class="sxs-lookup"><span data-stu-id="76e7e-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="76e7e-115">Frekari upplýsingar er að finna á [Bæta merki við](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="76e7e-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="76e7e-116">Hægt er að nota eiginleikann **Mínir reikningstenglar** til að skilgreina reikningssíður sem eigandi vefsins vill sýna flýtitengla fyrir í hausnum.</span><span class="sxs-lookup"><span data-stu-id="76e7e-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="76e7e-117">Einingar sem eru í boði innan hauseiningar</span><span class="sxs-lookup"><span data-stu-id="76e7e-117">Modules that are available within a header module</span></span>

<span data-ttu-id="76e7e-118">Eftirfarandi einingar er hægt að nota í fyrirsagnareiningu:</span><span class="sxs-lookup"><span data-stu-id="76e7e-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="76e7e-119">**Leiðasagnarvalmynd** - Leiðsagnarvalmyndin táknar leiðsagnarstigveldi rásarinnar og fleiri fasta leiðsagnartengla.</span><span class="sxs-lookup"><span data-stu-id="76e7e-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="76e7e-120">Frekari upplýsingar má finna i [Eining yfirlitsvalmyndar](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="76e7e-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="76e7e-121">**Leit** - Leitareiningin gerir notendum kleift að slá inn leitarskilyrði til að leita að vörum.</span><span class="sxs-lookup"><span data-stu-id="76e7e-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="76e7e-122">Vefslóð sjálfgefnu leitarsíðunnar og færibreytur leitarfyrirspurna vera að vera gefnar upp í **Svæðisstillingar \> Viðbætur**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="76e7e-123">Leitareiningin hefur eiginleika sem gera þér kleift að fela leitarhnappinn eða merkimiðann eins og þú þarfnast.</span><span class="sxs-lookup"><span data-stu-id="76e7e-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="76e7e-124">Leitareiningin styður einnig valkosti með sjálfvirkum tillögum, svo sem leitarniðurstöðum afurðar, leitarorða og flokka.</span><span class="sxs-lookup"><span data-stu-id="76e7e-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="76e7e-125">**Körfutákn** - Körfutákneiningin táknar körfutáknið sem sýnir fjölda af vörum í körfunni á hverjum tíma.</span><span class="sxs-lookup"><span data-stu-id="76e7e-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="76e7e-126">Fyrir frekari upplýsingar, sjá [Körfutáknseining](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="76e7e-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

- <span data-ttu-id="76e7e-127">**Svæðisval** - Svæðisnotkunareiningin leyfir notendum að fletta upp á mismunandi fyrirframskilgreindum svæðum, byggt á markaði, svæðum og staðarháttum.</span><span class="sxs-lookup"><span data-stu-id="76e7e-127">**Site selector** - The site selector module lets users browse across different predefined sites, based on market, regions, and locales.</span></span> <span data-ttu-id="76e7e-128">Frekari upplýsingar má finna á [Svæðisvalseining](site-selector.md).</span><span class="sxs-lookup"><span data-stu-id="76e7e-128">For more information, see [Site selector module](site-selector.md).</span></span>

- <span data-ttu-id="76e7e-129">**Verslunarval** - Hægt er að taka verslunarvaleininguna með í verslunarvali í haus.</span><span class="sxs-lookup"><span data-stu-id="76e7e-129">**Store selector** - The store selector module can be included in a header module's store selector slot.</span></span> <span data-ttu-id="76e7e-130">Það gerir notendum kleift að fletta og finna nærliggjandi verslanir.</span><span class="sxs-lookup"><span data-stu-id="76e7e-130">It lets users browse and find nearby stores.</span></span> <span data-ttu-id="76e7e-131">Einnig er hægt að tilgreina forgangsverslun.</span><span class="sxs-lookup"><span data-stu-id="76e7e-131">Users can also specify a preferred store.</span></span> <span data-ttu-id="76e7e-132">Þessi verslun verður síðan sýnd í hausnum.</span><span class="sxs-lookup"><span data-stu-id="76e7e-132">That store will then be shown in the header.</span></span> <span data-ttu-id="76e7e-133">Þegar verslunarvalseiningin er tekin með í haus einingar verður **Stillingar** eiginleiki hennarað vera stilltur á **Finna verslanir**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-133">When the store selector module is included in the header module, its **Mode** property must be set to **Find stores**.</span></span> <span data-ttu-id="76e7e-134">Frekari upplýsingar er að finna í [Verslunarvalseining](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="76e7e-134">For more information, see [Store selector module](store-selector.md).</span></span>

> [!NOTE]
> - <span data-ttu-id="76e7e-135">Stuðningur við notkun körfueiningar í hauseiningum er tiltækur í Dynamics 365 Commerce útgáfu 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="76e7e-135">Support for using the cart icon module in header modules is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>
> - <span data-ttu-id="76e7e-136">Stuðningur við notkun svæðisvalseiningar í hauseiningum er tiltækur í Dynamics 365 Commerce útgáfu 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="76e7e-136">Support for using the site selector module in header modules is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>
> - <span data-ttu-id="76e7e-137">Stuðningur við notkun verslunarvalseiningar í hauseiningum er tiltækur í Dynamics 365 Commerce útgáfu 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="76e7e-137">Support for using the store selector module in header modules is available in the Dynamics 365 Commerce 10.0.15 release.</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="76e7e-138">Búa til hausbrot fyrir síðu</span><span class="sxs-lookup"><span data-stu-id="76e7e-138">Create a header fragment for a page</span></span>

<span data-ttu-id="76e7e-139">Fylgdu þessum skrefum til að búa til hausbrot.</span><span class="sxs-lookup"><span data-stu-id="76e7e-139">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="76e7e-140">Farðu í **Brot** og veldu **Nýtt** til að búa til nýtt brot.</span><span class="sxs-lookup"><span data-stu-id="76e7e-140">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="76e7e-141">Í glugganum **Nýtt brot** skal velja eininguna **Hólf**, slá inn heiti fyrir brotið og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-141">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="76e7e-142">Velja skal hólfið **Sjálfgefið hólf** og síðan, hægra megin á eiginleikasvæðinu, skal stilla eiginleikann **Breidd** á **Fylla skjáinn**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-142">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="76e7e-143">Í hólfinu **Sjálfgefið hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-143">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="76e7e-144">Í glugganum **Bæta við einingu** skal velja einingarnar **Kökusamþykki**, **Haus** og **Tilboðsborði** og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-144">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="76e7e-145">Í eiginleikasvæði í **Tilboðsborðaeining** skal velja **Bæta við skilaboðum** og velja svo **Skilaboð**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-145">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="76e7e-146">Í svarglugganum **Skilaboða** skal bæta við texta og tenglum fyrir kynningarefnið og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-146">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="76e7e-147">Í einingunni **Samþykki köku** skaltu bæta við og grunnstilla texta og tengil á persónuverndarsíðu.</span><span class="sxs-lookup"><span data-stu-id="76e7e-147">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="76e7e-148">Í hólfinu **Yfirlitsvalmynd** í fyrirsagnareiningunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-148">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="76e7e-149">Í glugganum **Bæta við einingu** skal velja eininguna **Yfirlitsvalmynd** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-149">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="76e7e-150">Á eiginleikasvæðinu fyrir einingu yfirlitsvalmyndar, undir **Uppruni yfirlitsvalmyndar** skal velja **Retail Server**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-150">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="76e7e-151">Í eignasvæði fyrir einingu yfirlitsvalmyndar, undir **Föst valmyndaratriði** skal velja **Bæta við valmyndaratriði** og velja svo **Valmyndaratriði**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-151">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="76e7e-152">Í svarglugganum **Valmyndaratriði** undir **Texti valmyndaratriðis** skal slá inn „Tengiliður“.</span><span class="sxs-lookup"><span data-stu-id="76e7e-152">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="76e7e-153">Í svarglugganum **Valmyndaratriði**, undir **Tenglamarkmið valmyndaratriðis** skal velja **Bæta við tengli**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-153">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="76e7e-154">Í svarglugganum **Bæta við tengli** skal velja tengil fyrir „Tengiliður“ síðuna og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-154">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="76e7e-155">Í svarglugganum **Valmyndaratriði** skal velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-155">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="76e7e-156">Í hólfinu **Leita** í fyrirsagnareiningunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-156">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="76e7e-157">Í glugganum **Bæta við einingu** skal velja eininguna **Leita** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-157">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="76e7e-158">Á eiginleikasvæðinu fyrir leitareininguna skal stilla eiginleikana eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="76e7e-158">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="76e7e-159">Í hólfinu **Körfutákn** í fyrirsagnareiningunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-159">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="76e7e-160">Í glugganum **Bæta við einingu** skal velja eininguna **Körfutákn** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-160">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="76e7e-161">Á eiginleikasvæðinu fyrir einingu körfutákns skal stilla eiginleikana eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="76e7e-161">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="76e7e-162">Ef óskað er eftir að körfutáknið sýni samantekt körfu (einnig þekkt sem smákarfa) þegar notendur fara með bendilinn yfir það, skal velja **Sýna smákörfu**.</span><span class="sxs-lookup"><span data-stu-id="76e7e-162">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="76e7e-163">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="76e7e-163">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="76e7e-164">Til að hjálpa til við að tryggja að haus birtist á hverri síðu skal fylgja þessum skrefum á hverju síðusniðmáti sem er búið til fyrir vefsvæðið.</span><span class="sxs-lookup"><span data-stu-id="76e7e-164">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="76e7e-165">Í hólfinu **Fyrirsögn** í einingunni **Sjálfgefin síða** skal bæta við neðanmálsbrotinu sem var búið til.</span><span class="sxs-lookup"><span data-stu-id="76e7e-165">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="76e7e-166">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="76e7e-166">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="76e7e-167">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="76e7e-167">Additional resources</span></span>

[<span data-ttu-id="76e7e-168">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="76e7e-168">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="76e7e-169">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="76e7e-169">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="76e7e-170">Körfutáknseining</span><span class="sxs-lookup"><span data-stu-id="76e7e-170">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="76e7e-171">Tilboðsborðaeining</span><span class="sxs-lookup"><span data-stu-id="76e7e-171">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="76e7e-172">Eining yfirlitsvalmyndar</span><span class="sxs-lookup"><span data-stu-id="76e7e-172">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="76e7e-173">Samþykki köku</span><span class="sxs-lookup"><span data-stu-id="76e7e-173">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="76e7e-174">Eining síðufótar</span><span class="sxs-lookup"><span data-stu-id="76e7e-174">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="76e7e-175">Svæðisvalseining</span><span class="sxs-lookup"><span data-stu-id="76e7e-175">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="76e7e-176">Eining til að velja verslun</span><span class="sxs-lookup"><span data-stu-id="76e7e-176">Store selector module</span></span>](store-selector.md)
