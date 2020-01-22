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
ms.openlocfilehash: cc98419077f6f563ea2265d4e68ba809971cfbd6
ms.sourcegitcommit: ff93b8f6a11993f2cd00be2da7aa77ef0d950ab8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885479"
---
# <a name="header-module"></a><span data-ttu-id="3fdd4-103">Eining síðuhauss</span><span class="sxs-lookup"><span data-stu-id="3fdd4-103">Header module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="3fdd4-104">Þetta efni fjallar um fyrirsagnareiningar og lýsir því hvernig á að stofna þær í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-104">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3fdd4-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="3fdd4-105">Overview</span></span>

<span data-ttu-id="3fdd4-106">Fyrirsagnareining er sérstakur gámur sem er notaður til að hýsa allar einingar sem verða sýndar í fyrirsögn síðu.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-106">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="3fdd4-107">Til dæmis getur hún falið í sér merki vefsvæðisins, tengla á leiðsögustigveldi, tengla á aðrar síður á vefnum og leitarstikuna.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-107">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="3fdd4-108">Fyrirsagnareining er sjálfkrafa fínstillt fyrir tækið sem vefurinn er skoðaður á (það er skjáborðstæki eða fartæki).</span><span class="sxs-lookup"><span data-stu-id="3fdd4-108">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="3fdd4-109">Til dæmis, í fartæki er leiðsagnarstikan smækkuð niður í hnappinn **Valmynd** (sem er stundum kallaður *hamborgaravalmynd*).</span><span class="sxs-lookup"><span data-stu-id="3fdd4-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="3fdd4-110">Eiginleikar fyrirsagnar</span><span class="sxs-lookup"><span data-stu-id="3fdd4-110">Properties of a header</span></span>

<span data-ttu-id="3fdd4-111">Eins og almennir gámar, styður fyrirsagnareiningin eiginleikana **fyrirsögn** og **breidd**.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-111">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="3fdd4-112">Fyrirsagnareining hefur mörg hólf.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-112">A header module has multiple slots.</span></span> <span data-ttu-id="3fdd4-113">Til dæmis eru til hólf fyrir upplýsingaskilaboð, leiðsagnarvalmynd, lógó, leitarstiku, körfutákn, tákn óskalista og reikningsupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-113">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="3fdd4-114">Hvert hólf styður sérstakt mengi eininga.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-114">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="3fdd4-115">Einingar sem eru fáanlegar í fyrirsagnareiningunni</span><span class="sxs-lookup"><span data-stu-id="3fdd4-115">Modules that are available in a header module</span></span>

<span data-ttu-id="3fdd4-116">Eftirfarandi einingar er hægt að nota í fyrirsagnareiningu:</span><span class="sxs-lookup"><span data-stu-id="3fdd4-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="3fdd4-117">**Leiðasagnarvalmynd** - Leiðsagnarvalmyndin táknar leiðsagnarstigveldi rásarinnar og fleiri fasta leiðsagnartengla.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="3fdd4-118">Hægt er að stilla leiðsagnarstigveldi rásar í Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-118">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="3fdd4-119">Stilltir hlutir birtast síðan sem fyrirsagnarleiðsögn.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-119">Configured items then appear as header navigation.</span></span> <span data-ttu-id="3fdd4-120">Að auki er hægt að stilla fasta leiðsögutengla og hægt er að veita hlutfallslega tengla á aðrar síður á svæði fyrir rafræn viðskipti.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-120">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="3fdd4-121">Hægt er að stilla fyrirsögnina sjálfn til vinstri, hægri eða miðju.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-121">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="3fdd4-122">**Körfutákn** - Körfutáknið er sérstakt tákn sem stendur fyrir körfuna.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-122">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="3fdd4-123">Það er sýnt í fyrirsögninni og sýnir fjölda atriða í körfunni.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-123">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="3fdd4-124">Hlekkur á körfusíðuna ætti að fylgja körfutákninu, svo að hægt sé að vísa viðskiptavinum á körfusíðuna þegar þeir hafa samskipti við táknið.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-124">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="3fdd4-125">**Tákn óskalista** - Tákn óskalistans er sýnt í hausnum og sýnir fjölda atriða sem hefur verið bætt við óskalista viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-125">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="3fdd4-126">Hlekkur á óskalistasíðuna ætti að fylgja þessu tákni, svo að hægt sé að framsenda viðskiptavini á óskalistasíðuna þegar þeir hafa samskipti við táknið.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-126">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="3fdd4-127">**Innskráningareining** - Eining innskráningar er sýnd í hausnum.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-127">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="3fdd4-128">Hún gerir viðskiptavinum kleift að annaðhvort skrá sig inn á reikninginn sinn eða skrá sig fyrir reikning.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-128">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="3fdd4-129">Ef viðskiptavinurinn er þegar skráður inn er hægt að stilla eininguna til að sýna tengla á reikningssíðuna, síðu pöntunarferilsins eða aðra síðu.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-129">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="3fdd4-130">**Merkiseining** - Þessi eining sýnir merkið sem stendur fyrir söluaðila og vörumerki.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-130">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="3fdd4-131">Það er mynd sem hefur tengil.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-131">It's an image that has a link.</span></span> <span data-ttu-id="3fdd4-132">Tengillinn er venjulega stilltur þannig að hann hefur tilvísun á heimasíðuna. Þess vegna geta viðskiptavinir fljótt farið aftur á heimasíðuna af hvaða síðu sem er á svæðinu.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-132">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="3fdd4-133">**Viðvörun** - Viðvörun birtist í hausnum og er notuð til að sýna innbyggð skilaboð sem eiga við um allar síður á svæðinu.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-133">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="3fdd4-134">Til dæmis gæti viðvörun sýnt skilaboð eins og „Árlegri útsölu lýkur eftir tvo daga.“</span><span class="sxs-lookup"><span data-stu-id="3fdd4-134">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="3fdd4-135">**Leitarstika** - Leitarstikan gerir notendum kleift að slá inn leitarskilyrði svo að þeir geti leitað að vörum.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-135">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="3fdd4-136">Einingin verður að vera stillt með vefslóð á leitarniðurstöðusíðunni.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-136">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="3fdd4-137">Hægt er að stilla fyrirspurn strengjasniðsins (sjálfgefið gildi er **"q"**).</span><span class="sxs-lookup"><span data-stu-id="3fdd4-137">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="3fdd4-138">Leitarstikan er með sjálfvirkt hólf þar sem bæta skal sjálfvirkri einingu við.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-138">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="3fdd4-139">**Sjálfvirkni** - Sjálfvirka einingin sýnir niðurstöður sem sjálfkrafa eru lagðar til.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-139">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="3fdd4-140">Þessar niðurstöður geta verið lykilorð, vörur eða flokkar þar sem leitarorð er að finna.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-140">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="3fdd4-141">Búa til hauseiningu</span><span class="sxs-lookup"><span data-stu-id="3fdd4-141">Create a header module</span></span>

<span data-ttu-id="3fdd4-142">Til að stofna fyrirsagnareiningu skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-142">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="3fdd4-143">Stofnaðu síðubrot sem inniheldur hausaeiningu.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-143">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="3fdd4-144">Bættu einingum við hólfin í hausseiningunni.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-144">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="3fdd4-145">Uppfærðu stillingar fyrir hverja einingu.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-145">Update the settings for each module.</span></span>
1. <span data-ttu-id="3fdd4-146">Vistaðu síðubrotið.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-146">Save the page fragment.</span></span> 
1. <span data-ttu-id="3fdd4-147">Athuga á síðunni og birtu hana.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-147">Check in the page, and publish it.</span></span>

<span data-ttu-id="3fdd4-148">Til að tryggja að haus birtist á hverri síðu, fylgdu þessum skrefum á hverju síðusniðmáti sem er búið til fyrir svæðið.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-148">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="3fdd4-149">Á sjálfgefnu síðunni bætirðu við síðubrotinu sem inniheldur hauseininguna á hausinn í aðalhólfinu.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-149">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="3fdd4-150">Vistaðu sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-150">Save the template.</span></span> 
1. <span data-ttu-id="3fdd4-151">Skráðu brotið út í sniðmátinu og birtu það.</span><span class="sxs-lookup"><span data-stu-id="3fdd4-151">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3fdd4-152">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="3fdd4-152">Additional resources</span></span>

[<span data-ttu-id="3fdd4-153">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="3fdd4-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3fdd4-154">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="3fdd4-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="3fdd4-155">Kaupkassaeining</span><span class="sxs-lookup"><span data-stu-id="3fdd4-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="3fdd4-156">Körfueining</span><span class="sxs-lookup"><span data-stu-id="3fdd4-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="3fdd4-157">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="3fdd4-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="3fdd4-158">Pöntunarstaðfestingareining</span><span class="sxs-lookup"><span data-stu-id="3fdd4-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="3fdd4-159">Fyrirsagnareining</span><span class="sxs-lookup"><span data-stu-id="3fdd4-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="3fdd4-160">Neðanmálseining</span><span class="sxs-lookup"><span data-stu-id="3fdd4-160">Footer module</span></span>](author-footer-module.md)
