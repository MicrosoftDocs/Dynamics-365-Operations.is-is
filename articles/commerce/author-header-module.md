---
title: Fyrirsagnareining
description: Þetta efni fjallar um fyrirsagnareiningar og lýsir því hvernig á að stofna síðuhausa í Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: eb440a8fb67888c9411ad5998fead4d00982b436
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761225"
---
# <a name="header-module"></a><span data-ttu-id="b1ce3-103">Eining síðuhauss</span><span class="sxs-lookup"><span data-stu-id="b1ce3-103">Header module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="b1ce3-104">Þetta efni fjallar um fyrirsagnareiningar og lýsir því hvernig á að stofna síðuhausa í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b1ce3-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="b1ce3-105">Overview</span></span>

<span data-ttu-id="b1ce3-106">Í Dynamics 365 Commerce er síðuhaus stilltur sem síðubrot sem inniheldur haus, tilboðsborða og kökusamþykkiseiningar.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="b1ce3-107">Hausaeiningin inniheldur svæðismerki, tengla á yfirlitsstigveldið, tengla á aðrar síður á svæðinu, tákneiningu körfu, tákn óskalista, innskráningarmöguleika og leitarslána.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="b1ce3-108">Fyrirsagnareining er sjálfkrafa fínstillt fyrir tækið sem vefurinn er skoðaður á (með öðrum orðum, fyrir skjáborðstæki eða fartæki).</span><span class="sxs-lookup"><span data-stu-id="b1ce3-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="b1ce3-109">Til dæmis, í fartæki er leiðsagnarstikan smækkuð niður í hnappinn **Valmynd** (sem er stundum kallaður *hamborgaravalmynd*).</span><span class="sxs-lookup"><span data-stu-id="b1ce3-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="b1ce3-110">Eftirfarandi mynd sýnir dæmi um fyrirsagnareiningu á heimasíðu.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-110">The following image shows an example of a header module on a home page.</span></span>

![Dæmi um fyrirsagnareiningu](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="b1ce3-112">Eiginleikar fyrirsagnareiningar</span><span class="sxs-lookup"><span data-stu-id="b1ce3-112">Properties of a header module</span></span>

<span data-ttu-id="b1ce3-113">Hauseining styður eiginleikana **Fyrirtækismerki**, **Merkjatengil** og **Mínir reikningstenglar**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="b1ce3-114">Eiginleikarnir **Fyrirtækismerki** og **Merkjatengill** eru notaðir til að skilgreina merki á síðunni.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="b1ce3-115">Frekari upplýsingar er að finna á [Bæta merki við](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="b1ce3-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="b1ce3-116">Hægt er að nota eiginleikann **Mínir reikningstenglar** til að skilgreina reikningssíður sem eigandi vefsins vill sýna flýtitengla fyrir í hausnum.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="b1ce3-117">Einingar sem eru í boði innan hauseiningar</span><span class="sxs-lookup"><span data-stu-id="b1ce3-117">Modules that are available within a header module</span></span>

<span data-ttu-id="b1ce3-118">Eftirfarandi einingar er hægt að nota í fyrirsagnareiningu:</span><span class="sxs-lookup"><span data-stu-id="b1ce3-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="b1ce3-119">**Leiðasagnarvalmynd** - Leiðsagnarvalmyndin táknar leiðsagnarstigveldi rásarinnar og fleiri fasta leiðsagnartengla.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="b1ce3-120">Frekari upplýsingar má finna i [Eining yfirlitsvalmyndar](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="b1ce3-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="b1ce3-121">**Leit** - Leitareiningin gerir notendum kleift að slá inn leitarskilyrði til að leita að vörum.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="b1ce3-122">Vefslóð sjálfgefnu leitarsíðunnar og færibreytur leitarfyrirspurna vera að vera gefnar upp í **Svæðisstillingar \> Viðbætur**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="b1ce3-123">Leitareiningin hefur eiginleika sem gera þér kleift að fela leitarhnappinn eða merkimiðann eins og þú þarfnast.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="b1ce3-124">Leitareiningin styður einnig valkosti með sjálfvirkum tillögum, svo sem leitarniðurstöðum afurðar, leitarorða og flokka.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="b1ce3-125">**Körfutákn** - Körfutákneiningin táknar körfutáknið sem sýnir fjölda af vörum í körfunni á hverjum tíma.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="b1ce3-126">Fyrir frekari upplýsingar, sjá [Körfutáknseining](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="b1ce3-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="b1ce3-127">Búa til hausbrot fyrir síðu</span><span class="sxs-lookup"><span data-stu-id="b1ce3-127">Create a header fragment for a page</span></span>

<span data-ttu-id="b1ce3-128">Fylgdu þessum skrefum til að búa til hausbrot.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-128">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="b1ce3-129">Farðu í **Brot** og veldu **Nýtt** til að búa til nýtt brot.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-129">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="b1ce3-130">Í glugganum **Nýtt brot** skal velja eininguna **Hólf**, slá inn heiti fyrir brotið og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-130">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="b1ce3-131">Velja skal hólfið **Sjálfgefið hólf** og síðan, hægra megin á eiginleikasvæðinu, skal stilla eiginleikann **Breidd** á **Fylla skjáinn**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-131">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="b1ce3-132">Í hólfinu **Sjálfgefið hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-132">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b1ce3-133">Í glugganum **Bæta við einingu** skal velja einingarnar **Kökusamþykki**, **Haus** og **Tilboðsborði** og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-133">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="b1ce3-134">Í eiginleikasvæði í **Tilboðsborðaeining** skal velja **Bæta við skilaboðum** og velja svo **Skilaboð**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-134">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="b1ce3-135">Í svarglugganum **Skilaboða** skal bæta við texta og tenglum fyrir kynningarefnið og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-135">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="b1ce3-136">Í einingunni **Samþykki köku** skaltu bæta við og grunnstilla texta og tengil á persónuverndarsíðu.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-136">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="b1ce3-137">Í hólfinu **Yfirlitsvalmynd** í fyrirsagnareiningunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-137">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b1ce3-138">Í glugganum **Bæta við einingu** skal velja eininguna **Yfirlitsvalmynd** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-138">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b1ce3-139">Á eiginleikasvæðinu fyrir einingu yfirlitsvalmyndar, undir **Uppruni yfirlitsvalmyndar** skal velja **Retail Server**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-139">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="b1ce3-140">Í eignasvæði fyrir einingu yfirlitsvalmyndar, undir **Föst valmyndaratriði** skal velja **Bæta við valmyndaratriði** og velja svo **Valmyndaratriði**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-140">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="b1ce3-141">Í svarglugganum **Valmyndaratriði** undir **Texti valmyndaratriðis** skal slá inn „Tengiliður“.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-141">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="b1ce3-142">Í svarglugganum **Valmyndaratriði**, undir **Tenglamarkmið valmyndaratriðis** skal velja **Bæta við tengli**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-142">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="b1ce3-143">Í svarglugganum **Bæta við tengli** skal velja tengil fyrir „Tengiliður“ síðuna og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-143">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="b1ce3-144">Í svarglugganum **Valmyndaratriði** skal velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-144">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="b1ce3-145">Í hólfinu **Leita** í fyrirsagnareiningunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b1ce3-146">Í glugganum **Bæta við einingu** skal velja eininguna **Leita** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b1ce3-147">Á eiginleikasvæðinu fyrir leitareininguna skal stilla eiginleikana eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="b1ce3-148">Í hólfinu **Körfutákn** í fyrirsagnareiningunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b1ce3-149">Í glugganum **Bæta við einingu** skal velja eininguna **Körfutákn** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b1ce3-150">Á eiginleikasvæðinu fyrir einingu körfutákns skal stilla eiginleikana eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="b1ce3-151">Ef óskað er eftir að körfutáknið sýni samantekt körfu (einnig þekkt sem smákarfa) þegar notendur fara með bendilinn yfir það, skal velja **Sýna smákörfu**.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="b1ce3-152">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="b1ce3-153">Til að hjálpa til við að tryggja að haus birtist á hverri síðu skal fylgja þessum skrefum á hverju síðusniðmáti sem er búið til fyrir vefsvæðið.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-153">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="b1ce3-154">Í hólfinu **Fyrirsögn** í einingunni **Sjálfgefin síða** skal bæta við neðanmálsbrotinu sem var búið til.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="b1ce3-155">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="b1ce3-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1ce3-156">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b1ce3-156">Additional resources</span></span>

[<span data-ttu-id="b1ce3-157">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="b1ce3-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b1ce3-158">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="b1ce3-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b1ce3-159">Körfutáknseining</span><span class="sxs-lookup"><span data-stu-id="b1ce3-159">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="b1ce3-160">Tilboðsborðaeining</span><span class="sxs-lookup"><span data-stu-id="b1ce3-160">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="b1ce3-161">Eining yfirlitsvalmyndar</span><span class="sxs-lookup"><span data-stu-id="b1ce3-161">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="b1ce3-162">Samþykki köku</span><span class="sxs-lookup"><span data-stu-id="b1ce3-162">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="b1ce3-163">Eining síðufótar</span><span class="sxs-lookup"><span data-stu-id="b1ce3-163">Footer module</span></span>](author-footer-module.md)
