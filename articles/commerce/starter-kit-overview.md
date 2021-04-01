---
title: Yfirlit einingasafns
description: Þetta efnisatriði sýnir yfirlit yfir Microsoft Dynamics 365 Commerce einingasafnið.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: fcb0c2317315308de51d8247d23a930f10c3de6f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234294"
---
# <a name="module-library-overview"></a><span data-ttu-id="29007-103">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="29007-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="29007-104">Þetta efnisatriði sýnir yfirlit yfir Microsoft Dynamics 365 Commerce einingasafnið.</span><span class="sxs-lookup"><span data-stu-id="29007-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

<span data-ttu-id="29007-105">Dynamics 365 Commerce einingasafnið er safn eininga sem hægt er að nota til að búa til vefsvæði í e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="29007-105">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="29007-106">Einingar eru bæði með notendaviðmótaþætti og þætti virkrar hegðunar.</span><span class="sxs-lookup"><span data-stu-id="29007-106">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="29007-107">Hægt er að nota þemu í einingunni í einingasafninu til að breyta útliti og yfirbragði.</span><span class="sxs-lookup"><span data-stu-id="29007-107">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="29007-108">Í þemunum eru töflureiknaðir (CSS).</span><span class="sxs-lookup"><span data-stu-id="29007-108">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="29007-109">Þema fyrir tilbúið e-Commerce-sýnisvæði sem er nefnt „Fabrikam“ er aðgengilegt sem hluti af einingasafninu og hægt er að nota það sem tilvísun.</span><span class="sxs-lookup"><span data-stu-id="29007-109">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="29007-110">Einingar einingasafns</span><span class="sxs-lookup"><span data-stu-id="29007-110">Module library modules</span></span>

<span data-ttu-id="29007-111">Eftirfarandi gerðir eininga eru veittar í einingasafni:</span><span class="sxs-lookup"><span data-stu-id="29007-111">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="29007-112">**Gámaeining** – Gámaeining er einföld eining sem virkar sem hýsill fyrir aðrar einingar.</span><span class="sxs-lookup"><span data-stu-id="29007-112">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="29007-113">Hún stjórnar skipulag eininganna sem eru inni í henni.</span><span class="sxs-lookup"><span data-stu-id="29007-113">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="29007-114">**Markaðseiningar** – Markaðseiningar eru meðal annars innihaldsbálkur, textabálkur, myndspilari og myndræmueiningar.</span><span class="sxs-lookup"><span data-stu-id="29007-114">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="29007-115">Hægt er að nota allar þessar einingar til að sýna efni.</span><span class="sxs-lookup"><span data-stu-id="29007-115">All these modules can be used to showcase content.</span></span> <span data-ttu-id="29007-116">Hægt er að setja þær á allar síður og þær eru knúnar af gögnum frá efnisstýringarkerfinu (CMS).</span><span class="sxs-lookup"><span data-stu-id="29007-116">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="29007-117">**Fyrirsagnar- og síðufótareiningar** – Fyrirsagna- og síðufótareiningar birtast í fyrirsögn og síðufæti á öllum vefsíðum.</span><span class="sxs-lookup"><span data-stu-id="29007-117">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="29007-118">Hægt er að stilla þessar einingar eftir þörfum með eiginleikum.</span><span class="sxs-lookup"><span data-stu-id="29007-118">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="29007-119">**Leitareiningar** – Hægt er að uppgötva vörur með því að nota leitareininguna í fyrirsögninni.</span><span class="sxs-lookup"><span data-stu-id="29007-119">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="29007-120">Leitarniðurstöður birtast á leitarniðurstöðusíðunni.</span><span class="sxs-lookup"><span data-stu-id="29007-120">Search results appear on the search results page.</span></span> <span data-ttu-id="29007-121">Einnig er hægt að uppgötva afurðir á flokksíðum sem eru sérstakar síður fyrir hvern flokk sem er studdur í stigveldi rásarinnar.</span><span class="sxs-lookup"><span data-stu-id="29007-121">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="29007-122">Að auki er hægt að nota hreinsieiningar til að sía enn frekar niðurstöður í leitarniðurstöðum og flokksíðum.</span><span class="sxs-lookup"><span data-stu-id="29007-122">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="29007-123">**Einingar afurðaupplýsingasíðu** – Afurðaupplýsingasíður nota nokkrar einingar til að sýna vöruupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="29007-123">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="29007-124">Kaupgluggaeiningin gerir viðskiptavinum kleift að skoða afurðir og bæta þeim í körfuna.</span><span class="sxs-lookup"><span data-stu-id="29007-124">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="29007-125">Aðrar einingar, eins og tækniforskriftareiningin, sýna upplýsingar um afurðina.</span><span class="sxs-lookup"><span data-stu-id="29007-125">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="29007-126">Hægt er að nota einkunna- og umsagnaeininguna til að skoða og veita umsagnir.</span><span class="sxs-lookup"><span data-stu-id="29007-126">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="29007-127">**Einingin Kaupa á netinu, sækja í verslun** – Eininign Kaupa á netinu, sækja í verslun er samþætt við Bing Maps.</span><span class="sxs-lookup"><span data-stu-id="29007-127">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="29007-128">Hægt er að nota hana til að finna nálægar verslanir þar sem viðskiptavinir geta sótt vörur sem þeir hafa keypt.</span><span class="sxs-lookup"><span data-stu-id="29007-128">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="29007-129">**Innkaupaeiningar** – Innkaupaeiningar innihalda körfueininguna, sem er hægt að nota til að bæta vörum í körfuna.</span><span class="sxs-lookup"><span data-stu-id="29007-129">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="29007-130">Greiðslueiningin tekur upp sendingarfang, afhendingarmöguleika og gjafakort, vildarkerfi og upplýsingar um kreditkort, svo hægt sé að vinna úr pöntun.</span><span class="sxs-lookup"><span data-stu-id="29007-130">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="29007-131">Eftir að pöntun hefur verið gerð er hægt að nota staðfestingarhlutann til að sýna staðfestingarupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="29007-131">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="29007-132">**Einingar reikningsstjórnunar** – Innskráningareiningin gerir viðskiptavinum kleift að skrá sig inn á fyrirliggjandi reikning og með skráningareiningunni geta þeir stofnað nýjan reikning.</span><span class="sxs-lookup"><span data-stu-id="29007-132">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="29007-133">Eftir að reikningur er búinn til er hægt að nota pöntunarferilseininguna til að skoða nýlegar pantanir og nota pöntunarupplýsingareininguna til að skoða upplýsingar um pöntunina.</span><span class="sxs-lookup"><span data-stu-id="29007-133">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="29007-134">**Tillagnaeining** – Tillögur eru sýndar með því að nota staðsetningareiningu afurðar.</span><span class="sxs-lookup"><span data-stu-id="29007-134">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="29007-135">Þessi eining styður reiknirit og ritstjóralista sem hægt er að sýna á hvaða síðu sem er.</span><span class="sxs-lookup"><span data-stu-id="29007-135">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="29007-136">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="29007-136">Additional resources</span></span>

[<span data-ttu-id="29007-137">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="29007-137">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="29007-138">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="29007-138">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="29007-139">Körfueining</span><span class="sxs-lookup"><span data-stu-id="29007-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="29007-140">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="29007-140">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="29007-141">Pöntunarstaðfestingareining</span><span class="sxs-lookup"><span data-stu-id="29007-141">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="29007-142">Fyrirsagnareining</span><span class="sxs-lookup"><span data-stu-id="29007-142">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="29007-143">Neðanmálseining</span><span class="sxs-lookup"><span data-stu-id="29007-143">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]