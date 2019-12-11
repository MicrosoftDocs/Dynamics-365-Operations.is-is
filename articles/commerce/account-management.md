---
title: Reikningsstjórnunarsíður og -einingar
description: Þetta efni fjallar um reikningsstjórnunarsíður og -einingar í Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3986505a7e0e8d33d5b8ff2c06f493335731a8d9
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785382"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="c799c-103">Reikningsstjórnunarsíður og -einingar</span><span class="sxs-lookup"><span data-stu-id="c799c-103">Account management pages and modules</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c799c-104">Þetta efni fjallar um reikningsstjórnunarsíður og -einingar í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c799c-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c799c-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="c799c-105">Overview</span></span>

<span data-ttu-id="c799c-106">Með stjórnun reikninga er átt við hóp síðna sem notaðar eru til að stjórna upplýsingum sem tengjast notendareikningi í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c799c-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="c799c-107">Reikningsstjórnunarsíður innihalda lendingasíðu reikningsstjórnunar, notandaforstillingasíðu, notendasíðu, síðu pöntunarferils, pöntunarupplýsingasíðu, vildarsíðu og óskalistasíðu.</span><span class="sxs-lookup"><span data-stu-id="c799c-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="c799c-108">Lendingasíða fyrir stjórnun reikninga</span><span class="sxs-lookup"><span data-stu-id="c799c-108">Account management landing page</span></span>

<span data-ttu-id="c799c-109">Lendingasíða reikningsstjórnunar notar eftirfarandi einingar:</span><span class="sxs-lookup"><span data-stu-id="c799c-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="c799c-110">**Staðsetning efnis** - Þessi eining er gámaeining sem geymir allar einingar á lendingasíðu reikningsstjórnunar.</span><span class="sxs-lookup"><span data-stu-id="c799c-110">**Content placement** – This module is a container module that holds all the modules on the account management landing page.</span></span>
- <span data-ttu-id="c799c-111">**Móttökuskilaboð reiknings** - Þessi eining er notuð til að veita móttökuskilaboð á reikningssíðu.</span><span class="sxs-lookup"><span data-stu-id="c799c-111">**Account welcome item** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="c799c-112">Hún felur í sér eiginleika fyrir fyrirsögnina og reitastærðina.</span><span class="sxs-lookup"><span data-stu-id="c799c-112">It includes properties for the heading and the tile size.</span></span> <span data-ttu-id="c799c-113">Eiginleikinn **Reitastærð** skilgreinir breidd einingarinnar í staðsetningareiningu efnis.</span><span class="sxs-lookup"><span data-stu-id="c799c-113">The **Tile size** property defines the width of the module in the content placement module.</span></span> <span data-ttu-id="c799c-114">Gildin eru frá **1** til **12**, þar sem **12** táknar alla breidd staðsetningargáms efnisins.</span><span class="sxs-lookup"><span data-stu-id="c799c-114">Values range from **1** through **12**, where **12** represents the full width of the content placement container.</span></span>
- <span data-ttu-id="c799c-115">**Staðsetningarliður reikningspöntunar** - Þessi eining er notuð til að gefa yfirlit yfir fjölda pantana sem hafa verið gerðar af notendareikningnum.</span><span class="sxs-lookup"><span data-stu-id="c799c-115">**Account order placement item** – This module is used to provide a summary of the number of orders that have been placed by the user account.</span></span> <span data-ttu-id="c799c-116">Hún felur í sér eiginleika fyrir fyrirsögnina, reitastærðina og tengilinn „Skoða upplýsingar“.</span><span class="sxs-lookup"><span data-stu-id="c799c-116">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="c799c-117">Stilla ætti tengilinn „skoða upplýsingar“ til að framsenda á pöntunarferilsíðuna.</span><span class="sxs-lookup"><span data-stu-id="c799c-117">The "view details" link should be configured to redirect to the order history page.</span></span>
- <span data-ttu-id="c799c-118">**Staðsetningarliður reikningsforstillinga** - Þessi eining er notuð til að gefa yfirlit yfir notandaforstillingarnar.</span><span class="sxs-lookup"><span data-stu-id="c799c-118">**Account profile placement item** – This module is used to provide a summary of the user profile.</span></span> <span data-ttu-id="c799c-119">Hún felur í sér eiginleika fyrir fyrirsögnina, reitastærðina og tengilinn „Skoða upplýsingar“.</span><span class="sxs-lookup"><span data-stu-id="c799c-119">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="c799c-120">Stilla ætti tengilinn „skoða upplýsingar“ til að framsenda á notandaforstillingasíðuna.</span><span class="sxs-lookup"><span data-stu-id="c799c-120">The "view details" link should be configured to redirect to the user profile page.</span></span>
- <span data-ttu-id="c799c-121">**Óskalistaliður reiknings** - Þessi eining er notuð til að gefa yfirlit yfir hluti á óskalista viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="c799c-121">**Account wishlist item** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="c799c-122">Til dæmis gæti hann fullyrt: „Þú ert með 10 atriði á óskalistanum þínum.“</span><span class="sxs-lookup"><span data-stu-id="c799c-122">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="c799c-123">Hún felur í sér eiginleika fyrir fyrirsögnina, reitastærðina og tengilinn „Skoða upplýsingar“.</span><span class="sxs-lookup"><span data-stu-id="c799c-123">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="c799c-124">Stilla ætti tengilinn „skoða upplýsingar“ til að framsenda á óskalistasíðuna.</span><span class="sxs-lookup"><span data-stu-id="c799c-124">The "view details" link should be configured to redirect to the wish list page.</span></span>
- <span data-ttu-id="c799c-125">**Netfangaliður reiknings** - Þessi eining er notuð til að gefa yfirlit yfir netföng notandans.</span><span class="sxs-lookup"><span data-stu-id="c799c-125">**Account address item** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="c799c-126">Til dæmis gæti hún fullyrt: „Þú ert með 2 netföng bætt við reikninginn þinn.“</span><span class="sxs-lookup"><span data-stu-id="c799c-126">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="c799c-127">Hún felur í sér eiginleika fyrir fyrirsögnina, reitastærðina og tengilinn „Skoða upplýsingar“.</span><span class="sxs-lookup"><span data-stu-id="c799c-127">It includes properties for the heading, the tile size, and the "view details" link.</span></span> <span data-ttu-id="c799c-128">Stilla ætti tengilinn „skoða upplýsingar“ til að framsenda á notandanetfangasíðuna.</span><span class="sxs-lookup"><span data-stu-id="c799c-128">The "view details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="c799c-129">**Vildaratriði reiknings** - Þessi eining er notuð til að sýna og tengjast upplýsingum um vildarkerfi.</span><span class="sxs-lookup"><span data-stu-id="c799c-129">**Account loyalty item** – This module is used to show and link to loyalty program information.</span></span> <span data-ttu-id="c799c-130">Hún felur í sér eiginleika fyrir fyrirsögnina, reitastærðina, tengilinn „Skoða upplýsingar“ og tengilinn „Gerast meðlimur“.</span><span class="sxs-lookup"><span data-stu-id="c799c-130">It includes properties for the heading, the tile size, the "view details" link, and the "become a member" link.</span></span> <span data-ttu-id="c799c-131">Stilla ætti tengilinn „skoða upplýsingar“ til að framsenda á vildarkerfissíðuna.</span><span class="sxs-lookup"><span data-stu-id="c799c-131">The "view details" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="c799c-132">Stilla ætti tengilinn „gerast meðlimur“ til að framsenda á síðu þar sem notendur geta tekið þátt í vildarkerfinu.</span><span class="sxs-lookup"><span data-stu-id="c799c-132">The "become a member" link should be configured to redirect to a page where users can join the loyalty program.</span></span>

### <a name="order-history-page"></a><span data-ttu-id="c799c-133">Pöntunarferilssíða</span><span class="sxs-lookup"><span data-stu-id="c799c-133">Order history page</span></span>

<span data-ttu-id="c799c-134">Pöntunarferilsíðan notar pöntunarferilseininguna til að sýna allar nýlegar pantanir sem notandinn hefur sett inn.</span><span class="sxs-lookup"><span data-stu-id="c799c-134">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="c799c-135">Upplýsingasíða pöntunar</span><span class="sxs-lookup"><span data-stu-id="c799c-135">Order details page</span></span>

<span data-ttu-id="c799c-136">Pöntunarupplýsingasíðan veitir ítarlegar upplýsingar um hverja pöntun og má nálgast af pöntunarferilssíðunni.</span><span class="sxs-lookup"><span data-stu-id="c799c-136">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="c799c-137">Það notar pöntunarupplýsingaeininguna, sem krefst sölukennis eða færslukennis til að sækja pöntunarupplýsingarnar.</span><span class="sxs-lookup"><span data-stu-id="c799c-137">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="c799c-138">Notandaforstillingasíða</span><span class="sxs-lookup"><span data-stu-id="c799c-138">User profile page</span></span>

<span data-ttu-id="c799c-139">Notandaforstillingasíðan sýnir upplýsingar um notandareikning, svo sem nafn notanda og netfang.</span><span class="sxs-lookup"><span data-stu-id="c799c-139">The user profile page shows user account details, such as user's name and email address.</span></span> <span data-ttu-id="c799c-140">Hún notar notandaforstillingaeininguna.</span><span class="sxs-lookup"><span data-stu-id="c799c-140">It uses the user profile module.</span></span> <span data-ttu-id="c799c-141">Þrátt fyrir að ekki sé hægt að fjarlægja netfangið er hægt að breyta því.</span><span class="sxs-lookup"><span data-stu-id="c799c-141">Although the email address can't be removed, it can be edited.</span></span>

### <a name="user-address-page"></a><span data-ttu-id="c799c-142">Netfangssíða notanda</span><span class="sxs-lookup"><span data-stu-id="c799c-142">User address page</span></span>

<span data-ttu-id="c799c-143">Netfangasíða notanda sýnir lista yfir netföng sem tengjast notendareikningnum.</span><span class="sxs-lookup"><span data-stu-id="c799c-143">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="c799c-144">Notandinn gaf þessi netföng annaðhvort upp í greiðsluferlinu eða bætti þeim beint við á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="c799c-144">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="c799c-145">Notendanetfangareiningin er notuð til að bæta við og breyta netföngum, stilla aðalnetfangið og láta núverandi netföng birtast á síðunni.</span><span class="sxs-lookup"><span data-stu-id="c799c-145">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="c799c-146">Óskalistasíða</span><span class="sxs-lookup"><span data-stu-id="c799c-146">Wish list page</span></span>

<span data-ttu-id="c799c-147">Óskalistasíðan sýnir atriðin sem hefur verið bætt við óskalista viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="c799c-147">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="c799c-148">Hún notar óskalistaeininguna til að birta atriði óskalista.</span><span class="sxs-lookup"><span data-stu-id="c799c-148">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="c799c-149">Síða vildarkerfis</span><span class="sxs-lookup"><span data-stu-id="c799c-149">Loyalty page</span></span>

<span data-ttu-id="c799c-150">Vildarkerfissíðan gerir viðskiptavinum kleift að ganga í vildarkerfi eða, ef þeir eru nú þegar meðlimir í vildarkerfi, skoða upplýsingar um kerfið«».</span><span class="sxs-lookup"><span data-stu-id="c799c-150">The loyalty page lets customers join a loyalty program or, if they are already loyalty program members, view their program details.</span></span> <span data-ttu-id="c799c-151">Þeir geta einnig skoðað stigin sem þeir hafa unnið og innleyst í nýlegum færslum.</span><span class="sxs-lookup"><span data-stu-id="c799c-151">They can also view the points that they have earned and redeemed in recent transactions.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c799c-152">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="c799c-152">Additional resources</span></span>

[<span data-ttu-id="c799c-153">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="c799c-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c799c-154">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="c799c-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="c799c-155">Kaupkassaeining</span><span class="sxs-lookup"><span data-stu-id="c799c-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c799c-156">Körfueining</span><span class="sxs-lookup"><span data-stu-id="c799c-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c799c-157">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="c799c-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c799c-158">Pöntunarstaðfestingareining</span><span class="sxs-lookup"><span data-stu-id="c799c-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="c799c-159">Fyrirsagnareining</span><span class="sxs-lookup"><span data-stu-id="c799c-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="c799c-160">Neðanmálseining</span><span class="sxs-lookup"><span data-stu-id="c799c-160">Footer module</span></span>](author-footer-module.md)
