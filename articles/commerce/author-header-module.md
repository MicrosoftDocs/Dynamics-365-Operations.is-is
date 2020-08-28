---
title: Fyrirsagnareining
description: Þetta efni fjallar um fyrirsagnareiningar og lýsir því hvernig á að stofna síðuhausa í Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: e7dde3ba1ad375b309ae66cc6d31ccad85615e45
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686623"
---
# <a name="header-module"></a><span data-ttu-id="80a0c-103">Eining síðuhauss</span><span class="sxs-lookup"><span data-stu-id="80a0c-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="80a0c-104">Þetta efni fjallar um fyrirsagnareiningar og lýsir því hvernig á að stofna síðuhausa í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="80a0c-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="80a0c-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="80a0c-105">Overview</span></span>

<span data-ttu-id="80a0c-106">Í Dynamics 365 Commerce samanstendur síðuhaus af mörgum einingum, eins og haus, yfirlitsvalmynd, leit, auglýsingarborða og samþykkiseiningum fyrir smákökur.</span><span class="sxs-lookup"><span data-stu-id="80a0c-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="80a0c-107">Hausseiningin inniheldur merki vefsvæða, tengla á leiðsöguveldi, tengla á aðrar síður á vefnum, körfitákn, óskalistatákn, innskráningarvalkosti og leitarstikuna.</span><span class="sxs-lookup"><span data-stu-id="80a0c-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="80a0c-108">Fyrirsagnareining er sjálfkrafa fínstillt fyrir tækið sem vefurinn er skoðaður á (með öðrum orðum, fyrir skjáborðstæki eða fartæki).</span><span class="sxs-lookup"><span data-stu-id="80a0c-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="80a0c-109">Til dæmis, í fartæki er leiðsagnarstikan smækkuð niður í hnappinn **Valmynd** (sem er stundum kallaður *hamborgaravalmynd*).</span><span class="sxs-lookup"><span data-stu-id="80a0c-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="80a0c-110">Eftirfarandi mynd sýnir dæmi um fyrirsagnareiningu á heimasíðu.</span><span class="sxs-lookup"><span data-stu-id="80a0c-110">The following image shows an example of a header module on a home page.</span></span>

![Dæmi um fyrirsagnareiningu](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="80a0c-112">Eiginleikar fyrirsagnareiningar</span><span class="sxs-lookup"><span data-stu-id="80a0c-112">Properties of a header module</span></span>

<span data-ttu-id="80a0c-113">Hauseining styður eiginleikana **Fyrirtækismerki**, **Merkjatengil** og **Mínir reikningstenglar**.</span><span class="sxs-lookup"><span data-stu-id="80a0c-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="80a0c-114">Eiginleikarnir **Fyrirtækismerki** og **Merkjatengill** eru notaðir til að skilgreina merki á síðunni.</span><span class="sxs-lookup"><span data-stu-id="80a0c-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="80a0c-115">Frekari upplýsingar er að finna á [Bæta merki við](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="80a0c-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="80a0c-116">Hægt er að nota eiginleikann **Mínir reikningstenglar** til að skilgreina reikningssíður sem eigandi vefsins vill sýna flýtitengla fyrir í hausnum.</span><span class="sxs-lookup"><span data-stu-id="80a0c-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="80a0c-117">Einingar sem eru fáanlegar í fyrirsagnareiningunni</span><span class="sxs-lookup"><span data-stu-id="80a0c-117">Modules that are available in a header module</span></span>

<span data-ttu-id="80a0c-118">Eftirfarandi einingar er hægt að nota í fyrirsagnareiningu:</span><span class="sxs-lookup"><span data-stu-id="80a0c-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="80a0c-119">**Leiðasagnarvalmynd** - Leiðsagnarvalmyndin táknar leiðsagnarstigveldi rásarinnar og fleiri fasta leiðsagnartengla.</span><span class="sxs-lookup"><span data-stu-id="80a0c-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="80a0c-120">Hægt er að stilla leiðsagnarstigveldi rásar í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="80a0c-120">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="80a0c-121">Yfirlitsvalmyndin er með eiginleikann **Uppruni yfirlits** sem er notaður til að tilgreina valmyndaratriðin í Retail Server og grunnvalmyndaratriði sem uppsprettu.</span><span class="sxs-lookup"><span data-stu-id="80a0c-121">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="80a0c-122">Ef grunnvalmyndaratriði eru tilgreind sem uppspretta er hægt að veita tengda tengla við aðrar síður á vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="80a0c-122">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="80a0c-123">Stilltir hlutir birtast síðan sem fyrirsagnarleiðsögn.</span><span class="sxs-lookup"><span data-stu-id="80a0c-123">Configured items then appear as header navigation.</span></span> 

- <span data-ttu-id="80a0c-124">**Leit** - Leitareiningin gerir notendum kleift að slá inn leitarskilyrði til að leita að vörum.</span><span class="sxs-lookup"><span data-stu-id="80a0c-124">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="80a0c-125">Vefslóð sjálfgefnu leitarsíðunnar og færibreytur leitarfyrirspurna vera að vera gefnar upp í **Svæðisstillingar \> Viðbætur**.</span><span class="sxs-lookup"><span data-stu-id="80a0c-125">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="80a0c-126">Leitareiningin hefur eiginleika sem gera þér kleift að fela leitarhnappinn eða merkimiðann eins og þú þarfnast.</span><span class="sxs-lookup"><span data-stu-id="80a0c-126">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="80a0c-127">Leitareiningin styður einnig valkosti með sjálfvirkum tillögum, svo sem leitarniðurstöðum afurðar, leitarorða og flokka.</span><span class="sxs-lookup"><span data-stu-id="80a0c-127">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="80a0c-128">**Körfutákn** - Körfutákneiningin táknar körfutáknið sem sýnir fjölda af vörum í körfunni á hverjum tíma.</span><span class="sxs-lookup"><span data-stu-id="80a0c-128">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="80a0c-129">Fyrir frekari upplýsingar, sjá [Körfutáknseining](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="80a0c-129">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="80a0c-130">Stofna hauseiningu fyrir síðu</span><span class="sxs-lookup"><span data-stu-id="80a0c-130">Create a header module for a page</span></span>

<span data-ttu-id="80a0c-131">Til að stofna fyrirsagnareiningu skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="80a0c-131">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="80a0c-132">Farðu í **Brot** og veldu **Nýtt** til að búa til nýtt brot.</span><span class="sxs-lookup"><span data-stu-id="80a0c-132">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="80a0c-133">Í glugganum **Nýtt síðubrot** skal velja eininguna **Hólf**, slá inn heiti fyrir síðubrotið og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="80a0c-133">In the **New page fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="80a0c-134">Velja skal hólfið **Sjálfgefið hólf** og síðan, hægra megin á eiginleikasvæðinu, skal stilla eiginleikann **Breidd** á **Fylla hólf**.</span><span class="sxs-lookup"><span data-stu-id="80a0c-134">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="80a0c-135">Í hólfinu **Sjálfgefið hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="80a0c-135">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="80a0c-136">Í glugganum **Bæta við einingu** skal velja einingarnar **Tilboðsborði** og **Samþykki á kökum** og velja síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="80a0c-136">In the **Add Module** dialog box, select the **Promo banner** and **Cookie consent** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="80a0c-137">Í hólfinu **Sjálfgefið hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="80a0c-137">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="80a0c-138">Í glugganum **Bæta við einingu** skal velja eininguna **Hólf** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="80a0c-138">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="80a0c-139">Velja skal hólfið **Hólf** og síðan, hægra megin á eiginleikasvæðinu, skal stilla eiginleikann **Breidd** á **Fylla hólf**.</span><span class="sxs-lookup"><span data-stu-id="80a0c-139">Select the **Container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="80a0c-140">Í hólfinu **Hólf** skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="80a0c-140">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="80a0c-141">Í glugganum **Bæta við einingu** skal velja eininguna **Fyrirsögn** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="80a0c-141">In the **Add Module** dialog box, select the **Header** module, and then select **OK**.</span></span>
1. <span data-ttu-id="80a0c-142">Í hólfinu **Yfirlitsvalmynd** í fyrirsagnareiningunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="80a0c-142">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="80a0c-143">Í glugganum **Bæta við einingu** skal velja eininguna **Yfirlitsvalmynd** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="80a0c-143">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="80a0c-144">Á eiginleikasvæðinu fyrir einingu yfirlitsvalmyndar skal stilla eiginleikana eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="80a0c-144">In the property pane for the navigation menu module, configure the properties as needed.</span></span>
1. <span data-ttu-id="80a0c-145">Í hólfinu **Leita** í fyrirsagnareiningunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="80a0c-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="80a0c-146">Í glugganum **Bæta við einingu** skal velja eininguna **Leita** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="80a0c-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="80a0c-147">Á eiginleikasvæðinu fyrir leitareininguna skal stilla eiginleikana eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="80a0c-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="80a0c-148">Í hólfinu **Körfutákn** í fyrirsagnareiningunni skal velja úrfellingarmerkið (**...**) og síðan velja **Bæta við einingu**.</span><span class="sxs-lookup"><span data-stu-id="80a0c-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="80a0c-149">Í glugganum **Bæta við einingu** skal velja eininguna **Körfutákn** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="80a0c-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="80a0c-150">Á eiginleikasvæðinu fyrir einingu körfutákns skal stilla eiginleikana eftir því sem þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="80a0c-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="80a0c-151">Ef óskað er eftir að körfutáknið sýni samantekt körfu (einnig þekkt sem smákarfa) þegar notendur fara með bendilinn yfir það, skal velja **Sýna smákörfu**.</span><span class="sxs-lookup"><span data-stu-id="80a0c-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="80a0c-152">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila brotinu og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="80a0c-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="80a0c-153">Til að tryggja að haus birtist á hverri síðu, fylgdu þessum skrefum á hverju síðusniðmáti sem er búið til fyrir svæðið.</span><span class="sxs-lookup"><span data-stu-id="80a0c-153">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="80a0c-154">Í hólfinu **Fyrirsögn** í einingunni **Sjálfgefin síða** skal bæta við neðanmálsbrotinu sem var búið til.</span><span class="sxs-lookup"><span data-stu-id="80a0c-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="80a0c-155">Veldu **Vista**, síðan **Ljúka við breytingar** til að skila sniðmáti og veldu síðan **Birta** til að birta það.</span><span class="sxs-lookup"><span data-stu-id="80a0c-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="80a0c-156">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="80a0c-156">Additional resources</span></span>

[<span data-ttu-id="80a0c-157">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="80a0c-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="80a0c-158">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="80a0c-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="80a0c-159">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="80a0c-159">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="80a0c-160">Körfueining</span><span class="sxs-lookup"><span data-stu-id="80a0c-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="80a0c-161">Körfutáknseining</span><span class="sxs-lookup"><span data-stu-id="80a0c-161">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="80a0c-162">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="80a0c-162">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="80a0c-163">Eining pöntunarstaðfestingar</span><span class="sxs-lookup"><span data-stu-id="80a0c-163">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="80a0c-164">Eining síðuhauss</span><span class="sxs-lookup"><span data-stu-id="80a0c-164">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="80a0c-165">Neðanmálseining</span><span class="sxs-lookup"><span data-stu-id="80a0c-165">Footer module</span></span>](author-footer-module.md)
