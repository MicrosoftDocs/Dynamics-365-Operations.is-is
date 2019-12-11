---
title: Fyrirsagnareining
description: Þetta efni fjallar um fyrirsagnareiningar og lýsir því hvernig á að stofna þær í Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697276"
---
# <a name="header-module"></a><span data-ttu-id="e8d6f-103">Fyrirsagnareining</span><span class="sxs-lookup"><span data-stu-id="e8d6f-103">Header module</span></span>

<span data-ttu-id="e8d6f-104">[!include [banner](includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span><span class="sxs-lookup"><span data-stu-id="e8d6f-104">[!include [banner]includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span></span>

<span data-ttu-id="e8d6f-105">Þetta efni fjallar um fyrirsagnareiningar og lýsir því hvernig á að stofna þær í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-105">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e8d6f-106">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="e8d6f-106">Overview</span></span>

<span data-ttu-id="e8d6f-107">Fyrirsagnareining er sérstakur gámur sem er notaður til að hýsa allar einingar sem verða sýndar í fyrirsögn síðu.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-107">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="e8d6f-108">Til dæmis getur hún falið í sér merki vefsvæðisins, tengla á leiðsögustigveldi, tengla á aðrar síður á vefnum og leitarstikuna.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-108">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="e8d6f-109">Fyrirsagnareining er sjálfkrafa fínstillt fyrir tækið sem vefurinn er skoðaður á (það er skjáborðstæki eða fartæki).</span><span class="sxs-lookup"><span data-stu-id="e8d6f-109">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="e8d6f-110">Til dæmis, í fartæki er leiðsagnarstikan smækkuð niður í hnappinn **Valmynd** (sem er stundum kallaður *hamborgaravalmynd*).</span><span class="sxs-lookup"><span data-stu-id="e8d6f-110">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="e8d6f-111">Eiginleikar fyrirsagnar</span><span class="sxs-lookup"><span data-stu-id="e8d6f-111">Properties of a header</span></span>

<span data-ttu-id="e8d6f-112">Eins og almennir gámar, styður fyrirsagnareiningin eiginleikana **fyrirsögn** og **breidd**.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-112">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="e8d6f-113">Fyrirsagnareining hefur mörg hólf.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-113">A header module has multiple slots.</span></span> <span data-ttu-id="e8d6f-114">Til dæmis eru til hólf fyrir upplýsingaskilaboð, leiðsagnarvalmynd, lógó, leitarstiku, körfutákn, tákn óskalista og reikningsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-114">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="e8d6f-115">Hvert hólf styður sérstakt mengi eininga.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-115">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="e8d6f-116">Einingar sem eru fáanlegar í fyrirsagnareiningunni</span><span class="sxs-lookup"><span data-stu-id="e8d6f-116">Modules that are available in a header module</span></span>

<span data-ttu-id="e8d6f-117">Eftirfarandi einingar er hægt að nota í fyrirsagnareiningu:</span><span class="sxs-lookup"><span data-stu-id="e8d6f-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="e8d6f-118">**Leiðasagnarvalmynd** - Leiðsagnarvalmyndin táknar leiðsagnarstigveldi rásarinnar og fleiri fasta leiðsagnartengla.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="e8d6f-119">Hægt er að stilla leiðsagnarstigveldi rásar í Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-119">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="e8d6f-120">Stilltir hlutir birtast síðan sem fyrirsagnarleiðsögn.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-120">Configured items then appear as header navigation.</span></span> <span data-ttu-id="e8d6f-121">Að auki er hægt að stilla fasta leiðsögutengla og hægt er að veita hlutfallslega tengla á aðrar síður á svæði fyrir rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-121">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="e8d6f-122">Hægt er að stilla fyrirsögnina sjálfn til vinstri, hægri eða miðju.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-122">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="e8d6f-123">**Körfutákn** - Körfutáknið er sérstakt tákn sem stendur fyrir körfuna.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-123">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="e8d6f-124">Það er sýnt í fyrirsögninni og sýnir fjölda atriða í körfunni.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-124">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="e8d6f-125">Hlekkur á körfusíðuna ætti að fylgja körfutákninu, svo að hægt sé að vísa viðskiptavinum á körfusíðuna þegar þeir hafa samskipti við táknið.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-125">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="e8d6f-126">**Tákn óskalista** - Tákn óskalistans er sýnt í hausnum og sýnir fjölda atriða sem hefur verið bætt við óskalista viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-126">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="e8d6f-127">Hlekkur á óskalistasíðuna ætti að fylgja þessu tákni, svo að hægt sé að framsenda viðskiptavini á óskalistasíðuna þegar þeir hafa samskipti við táknið.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-127">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="e8d6f-128">**Innskráningareining** - Eining innskráningar er sýnd í hausnum.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-128">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="e8d6f-129">Hún gerir viðskiptavinum kleift að annaðhvort skrá sig inn á reikninginn sinn eða skrá sig fyrir reikning.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-129">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="e8d6f-130">Ef viðskiptavinurinn er þegar skráður inn er hægt að stilla eininguna til að sýna tengla á reikningssíðuna, síðu pöntunarferilsins eða aðra síðu.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-130">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="e8d6f-131">**Merkiseining** - Þessi eining sýnir merkið sem stendur fyrir söluaðila og vörumerki.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-131">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="e8d6f-132">Það er mynd sem hefur tengil.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-132">It's an image that has a link.</span></span> <span data-ttu-id="e8d6f-133">Tengillinn er venjulega stilltur þannig að hann hefur tilvísun á heimasíðuna. Þess vegna geta viðskiptavinir fljótt farið aftur á heimasíðuna af hvaða síðu sem er á svæðinu.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-133">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="e8d6f-134">**Viðvörun** - Viðvörun birtist í hausnum og er notuð til að sýna innbyggð skilaboð sem eiga við um allar síður á svæðinu.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-134">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="e8d6f-135">Til dæmis gæti viðvörun sýnt skilaboð eins og „Árlegri útsölu lýkur eftir tvo daga.“</span><span class="sxs-lookup"><span data-stu-id="e8d6f-135">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="e8d6f-136">**Leitarstika** - Leitarstikan gerir notendum kleift að slá inn leitarskilyrði svo að þeir geti leitað að vörum.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-136">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="e8d6f-137">Einingin verður að vera stillt með vefslóð á leitarniðurstöðusíðunni.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-137">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="e8d6f-138">Hægt er að stilla fyrirspurn strengjasniðsins (sjálfgefið gildi er **"q"**).</span><span class="sxs-lookup"><span data-stu-id="e8d6f-138">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="e8d6f-139">Leitarstikan er með sjálfvirkt hólf þar sem bæta skal sjálfvirkri einingu við.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-139">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="e8d6f-140">**Sjálfvirkni** - Sjálfvirka einingin sýnir niðurstöður sem sjálfkrafa eru lagðar til.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-140">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="e8d6f-141">Þessar niðurstöður geta verið lykilorð, vörur eða flokkar þar sem leitarorð er að finna.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-141">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="e8d6f-142">Búa til hauseiningu</span><span class="sxs-lookup"><span data-stu-id="e8d6f-142">Create a header module</span></span>

<span data-ttu-id="e8d6f-143">Til að stofna fyrirsagnareiningu skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-143">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="e8d6f-144">Stofnaðu síðubrot sem inniheldur hausaeiningu.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-144">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="e8d6f-145">Bættu einingum við hólfin í hausseiningunni.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-145">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="e8d6f-146">Uppfærðu stillingar fyrir hverja einingu.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-146">Update the settings for each module.</span></span>
1. <span data-ttu-id="e8d6f-147">Vistaðu síðubrotið.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-147">Save the page fragment.</span></span> 
1. <span data-ttu-id="e8d6f-148">Athuga á síðunni og birtu hana.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-148">Check in the page, and publish it.</span></span>

<span data-ttu-id="e8d6f-149">Til að tryggja að haus birtist á hverri síðu, fylgdu þessum skrefum á hverju síðusniðmáti sem er búið til fyrir svæðið.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-149">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="e8d6f-150">Á sjálfgefnu síðunni bætirðu við síðubrotinu sem inniheldur hauseininguna á hausinn í aðalhólfinu.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-150">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="e8d6f-151">Vistaðu sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-151">Save the template.</span></span> 
1. <span data-ttu-id="e8d6f-152">Skráðu brotið út í sniðmátinu og birtu það.</span><span class="sxs-lookup"><span data-stu-id="e8d6f-152">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e8d6f-153">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="e8d6f-153">Additional resources</span></span>

[<span data-ttu-id="e8d6f-154">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="e8d6f-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e8d6f-155">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="e8d6f-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="e8d6f-156">Kaupkassaeining</span><span class="sxs-lookup"><span data-stu-id="e8d6f-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="e8d6f-157">Körfueining</span><span class="sxs-lookup"><span data-stu-id="e8d6f-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="e8d6f-158">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="e8d6f-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="e8d6f-159">Pöntunarstaðfestingareining</span><span class="sxs-lookup"><span data-stu-id="e8d6f-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="e8d6f-160">Fyrirsagnareining</span><span class="sxs-lookup"><span data-stu-id="e8d6f-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="e8d6f-161">Neðanmálseining</span><span class="sxs-lookup"><span data-stu-id="e8d6f-161">Footer module</span></span>](author-footer-module.md)
