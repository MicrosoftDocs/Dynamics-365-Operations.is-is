---
title: Fyrirsagnareining
description: Þetta efni fjallar um fyrirsagnareiningar og lýsir því hvernig á að stofna síðuhausa í Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: cec138ebefbd2beb2f1cf6302ce58d8bbc5c4bbd
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261445"
---
# <a name="header-module"></a><span data-ttu-id="bdd42-103">Eining síðuhauss</span><span class="sxs-lookup"><span data-stu-id="bdd42-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="bdd42-104">Þetta efni fjallar um fyrirsagnareiningar og lýsir því hvernig á að stofna síðuhausa í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bdd42-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bdd42-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="bdd42-105">Overview</span></span>

<span data-ttu-id="bdd42-106">Í Dynamics 365 Commerce samanstendur síðuhaus af mörgum einingum, eins og haus, yfirlitsvalmynd, leit, auglýsingarborða og samþykkiseiningum fyrir smákökur.</span><span class="sxs-lookup"><span data-stu-id="bdd42-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="bdd42-107">Hausseiningin inniheldur merki vefsvæða, tengla á leiðsöguveldi, tengla á aðrar síður á vefnum, körfitákn, óskalistatákn, innskráningarvalkosti og leitarstikuna.</span><span class="sxs-lookup"><span data-stu-id="bdd42-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="bdd42-108">Fyrirsagnareining er sjálfkrafa fínstillt fyrir tækið sem vefurinn er skoðaður á (með öðrum orðum, fyrir skjáborðstæki eða fartæki).</span><span class="sxs-lookup"><span data-stu-id="bdd42-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="bdd42-109">Til dæmis, í fartæki er leiðsagnarstikan smækkuð niður í hnappinn **Valmynd** (sem er stundum kallaður *hamborgaravalmynd*).</span><span class="sxs-lookup"><span data-stu-id="bdd42-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="bdd42-110">Eiginleikar fyrirsagnareiningar</span><span class="sxs-lookup"><span data-stu-id="bdd42-110">Properties of a header module</span></span>

<span data-ttu-id="bdd42-111">Hauseining styður eiginleikana **Fyrirtækismerki**, **Merkjatengil** og **Mínir reikningstenglar**.</span><span class="sxs-lookup"><span data-stu-id="bdd42-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="bdd42-112">Eiginleikarnir **Fyrirtækismerki** og **Merkjatengill** eru notaðir til að skilgreina merki á síðunni.</span><span class="sxs-lookup"><span data-stu-id="bdd42-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="bdd42-113">Frekari upplýsingar er að finna á [Bæta merki við](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="bdd42-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="bdd42-114">Hægt er að nota eiginleikann **Mínir reikningstenglar** til að skilgreina reikningssíður sem eigandi vefsins vill sýna flýtitengla fyrir í hausnum.</span><span class="sxs-lookup"><span data-stu-id="bdd42-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="bdd42-115">Einingar sem eru fáanlegar í fyrirsagnareiningunni</span><span class="sxs-lookup"><span data-stu-id="bdd42-115">Modules that are available in a header module</span></span>

<span data-ttu-id="bdd42-116">Eftirfarandi einingar er hægt að nota í fyrirsagnareiningu:</span><span class="sxs-lookup"><span data-stu-id="bdd42-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="bdd42-117">**Leiðasagnarvalmynd** - Leiðsagnarvalmyndin táknar leiðsagnarstigveldi rásarinnar og fleiri fasta leiðsagnartengla.</span><span class="sxs-lookup"><span data-stu-id="bdd42-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="bdd42-118">Hægt er að stilla leiðsagnarstigveldi rásar í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bdd42-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="bdd42-119">Yfirlitsvalmyndin er með eiginleikann **Uppruni yfirlits** sem er notaður til að tilgreina valmyndaratriðin í Retail Server og grunnvalmyndaratriði sem uppsprettu.</span><span class="sxs-lookup"><span data-stu-id="bdd42-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="bdd42-120">Ef grunnvalmyndaratriði eru tilgreind sem uppspretta er hægt að veita tengda tengla við aðrar síður á vefsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="bdd42-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="bdd42-121">Stilltir hlutir birtast síðan sem fyrirsagnarleiðsögn.</span><span class="sxs-lookup"><span data-stu-id="bdd42-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="bdd42-122">**Leit** - Leitareiningin gerir notendum kleift að slá inn leitarskilyrði til að leita að vörum.</span><span class="sxs-lookup"><span data-stu-id="bdd42-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="bdd42-123">Vefslóð sjálfgefnu leitarsíðunnar og færibreytur leitarfyrirspurna vera að vera gefnar upp í **Svæðisstillingar \> Viðbætur**.</span><span class="sxs-lookup"><span data-stu-id="bdd42-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="bdd42-124">Leitareiningin hefur eiginleika sem gera þér kleift að fela leitarhnappinn eða merkimiðann eins og þú þarfnast.</span><span class="sxs-lookup"><span data-stu-id="bdd42-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="bdd42-125">Leitareiningin styður einnig valkosti með sjálfvirkum tillögum, svo sem leitarniðurstöðum afurðar, leitarorða og flokka.</span><span class="sxs-lookup"><span data-stu-id="bdd42-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>
- <span data-ttu-id="bdd42-126">**Körfutákn** - Körfutákneiningin táknar körfutáknið sem sýnir fjölda af vörum í körfunni á hverjum tíma.</span><span class="sxs-lookup"><span data-stu-id="bdd42-126">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="bdd42-127">Fyrir frekari upplýsingar, sjá [Körfutáknseining](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="bdd42-127">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="bdd42-128">Stofna hauseiningu fyrir síðu</span><span class="sxs-lookup"><span data-stu-id="bdd42-128">Create a header module for a page</span></span>

<span data-ttu-id="bdd42-129">Til að stofna fyrirsagnareiningu skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="bdd42-129">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="bdd42-130">Búðu til brot sem er nefnt **hausbrot** og bættu gámaeiningunni við það.</span><span class="sxs-lookup"><span data-stu-id="bdd42-130">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="bdd42-131">Í eiginleikaglugganum fyrir gámaeininguna stillirðu eiginleikann **Breidd** á **Fylla gám**.</span><span class="sxs-lookup"><span data-stu-id="bdd42-131">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="bdd42-132">Bættu auglýsingaborða og samþykkiseiningum fyrir smákökur við gámaeininguna.</span><span class="sxs-lookup"><span data-stu-id="bdd42-132">Add a promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="bdd42-133">Bættu annarri gámaeiningu við brotið og stilltu eiginleikann **Breidd** á **Fylla gám**.</span><span class="sxs-lookup"><span data-stu-id="bdd42-133">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="bdd42-134">Bættu hauseiningu við seinni gámaeininguna.</span><span class="sxs-lookup"><span data-stu-id="bdd42-134">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="bdd42-135">Í hólfi **Yfirlitsvalmyndar** í hausseiningunni bætiður við einingu yfirlitsvalmyndar.</span><span class="sxs-lookup"><span data-stu-id="bdd42-135">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="bdd42-136">Stilltu eiginleika aðgerðar einingar yfirlitsvalmyndar í eiginleikaglugganum í yfirlitsvalmyndareiningunni.</span><span class="sxs-lookup"><span data-stu-id="bdd42-136">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="bdd42-137">Í hólfinu **Leita** í hausseiningunni skal bæta leitareiningu við.</span><span class="sxs-lookup"><span data-stu-id="bdd42-137">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="bdd42-138">Í eiginleikaglugga fyrir leitareininguna stillirðu eiginleika leitareiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="bdd42-138">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="bdd42-139">Í raufinni **Körfutákn** í hauseiningunni bætirðu við körfutáknseiningunni.</span><span class="sxs-lookup"><span data-stu-id="bdd42-139">In the **Cart icon** slot of the header module, add a cart icon module.</span></span> 
1. <span data-ttu-id="bdd42-140">Í eiginleikaglugga fyrir körfutáknseininguna stillirðu eiginleika körfutáknseiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="bdd42-140">In the property pane for the cart icon module, configure the properties of the cart icon module.</span></span> <span data-ttu-id="bdd42-141">Ef þú vilt að körfutáknið sýni smákörfu þegar músin sveimar yfir skaltu velja **Satt** fyrir **Sýna smákörfu**.</span><span class="sxs-lookup"><span data-stu-id="bdd42-141">If you want the cart icon to display a mini cart when hovered over, select **True** for **Show mini cart**.</span></span>
1. <span data-ttu-id="bdd42-142">Vistaðu síðubrotið, ljúktu við að breyta því og birtu það.</span><span class="sxs-lookup"><span data-stu-id="bdd42-142">Save the page fragment, finish editing, and publish it.</span></span> 


<span data-ttu-id="bdd42-143">Til að tryggja að haus birtist á hverri síðu, fylgdu þessum skrefum á hverju síðusniðmáti sem er búið til fyrir svæðið.</span><span class="sxs-lookup"><span data-stu-id="bdd42-143">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="bdd42-144">Í hólfinu **Aðal** á sjálfgefnu síðunni bætirðu við haussíðbrotinu sem inniheldur hauseiningunni við hausinn.</span><span class="sxs-lookup"><span data-stu-id="bdd42-144">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="bdd42-145">Vistaðu sniðmátið, ljúktu við að breyta því og birtu það.</span><span class="sxs-lookup"><span data-stu-id="bdd42-145">Save the template, finish editing, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bdd42-146">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="bdd42-146">Additional resources</span></span>

[<span data-ttu-id="bdd42-147">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="bdd42-147">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="bdd42-148">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="bdd42-148">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="bdd42-149">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="bdd42-149">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="bdd42-150">Körfueining</span><span class="sxs-lookup"><span data-stu-id="bdd42-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="bdd42-151">Körfutáknseining</span><span class="sxs-lookup"><span data-stu-id="bdd42-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="bdd42-152">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="bdd42-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="bdd42-153">Eining pöntunarstaðfestingar</span><span class="sxs-lookup"><span data-stu-id="bdd42-153">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="bdd42-154">Eining síðuhauss</span><span class="sxs-lookup"><span data-stu-id="bdd42-154">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="bdd42-155">Neðanmálseining</span><span class="sxs-lookup"><span data-stu-id="bdd42-155">Footer module</span></span>](author-footer-module.md)
