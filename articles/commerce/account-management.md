---
title: Reikningsstjórnunarsíður og -einingar
description: Þetta efni fjallar um reikningsstjórnunarsíður og -einingar í Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: 8787a7b01ecf15752569d2a3a8d7804fe492e63d
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025697"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="26433-103">Reikningsstjórnunarsíður og -einingar</span><span class="sxs-lookup"><span data-stu-id="26433-103">Account management pages and modules</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="26433-104">Þetta efni fjallar um reikningsstjórnunarsíður og -einingar í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="26433-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="26433-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="26433-105">Overview</span></span>

<span data-ttu-id="26433-106">Með stjórnun reikninga er átt við hóp síðna sem notaðar eru til að stjórna upplýsingum sem tengjast notendareikningi í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="26433-106">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="26433-107">Reikningsstjórnunarsíður innihalda lendingasíðu reikningsstjórnunar, notandaforstillingasíðu, notendasíðu, síðu pöntunarferils, pöntunarupplýsingasíðu, vildarsíðu og óskalistasíðu.</span><span class="sxs-lookup"><span data-stu-id="26433-107">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="26433-108">Lendingasíða fyrir stjórnun reikninga</span><span class="sxs-lookup"><span data-stu-id="26433-108">Account management landing page</span></span>

<span data-ttu-id="26433-109">Lendingasíða reikningsstjórnunar notar eftirfarandi einingar:</span><span class="sxs-lookup"><span data-stu-id="26433-109">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="26433-110">**Gámur** - Allar lendingarsíðueiningar reikningsstjórnunar skulu settar í gám.</span><span class="sxs-lookup"><span data-stu-id="26433-110">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="26433-111">**Móttökureitur reiknings** - Þessi eining er notuð til að veita móttökuskilaboð á reikningssíðu.</span><span class="sxs-lookup"><span data-stu-id="26433-111">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="26433-112">Hann felur í sér eiginleika fyrir fyrirsögnina.</span><span class="sxs-lookup"><span data-stu-id="26433-112">It includes properties for the heading.</span></span>
- <span data-ttu-id="26433-113">**Almennir reitir reiknings** - Þessa einingu er hægt að nota til að útvega fyrirsagnir og tengla á reikningastjórnarsíður, svo sem „Pöntunarferill“ eða „Prófíllinn minn“.</span><span class="sxs-lookup"><span data-stu-id="26433-113">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="26433-114">Hægt er að nota almenna reitaeiningu til að stilla reit fyrir hvaða síðu sem er.</span><span class="sxs-lookup"><span data-stu-id="26433-114">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="26433-115">Í Fabrikam er þessi eining notuð fyrir tengilinn „Pöntunarferill“ og „Prófíllinn minn“ á lendingasíðu reikningsstjórnunar.</span><span class="sxs-lookup"><span data-stu-id="26433-115">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="26433-116">**Óskalistareitur reiknings** - Þessi eining er notuð til að gefa yfirlit yfir hluti á óskalista viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="26433-116">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="26433-117">Til dæmis gæti hann fullyrt: „Þú ert með 10 atriði á óskalistanum þínum.“</span><span class="sxs-lookup"><span data-stu-id="26433-117">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="26433-118">Hún felur í sér eiginleika fyrir fyrirsögnina og tengilinn „Skoða upplýsingar“.</span><span class="sxs-lookup"><span data-stu-id="26433-118">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="26433-119">Stilla ætti tengilinn „Skoða upplýsingar“ til að framsenda á óskalistasíðuna.</span><span class="sxs-lookup"><span data-stu-id="26433-119">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="26433-120">**Netfangareitur reiknings** - Þessi eining er notuð til að gefa yfirlit yfir netföng notandans.</span><span class="sxs-lookup"><span data-stu-id="26433-120">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="26433-121">Til dæmis gæti hún fullyrt: „Þú ert með 2 netföng bætt við reikninginn þinn.“</span><span class="sxs-lookup"><span data-stu-id="26433-121">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="26433-122">Hún felur í sér eiginleika fyrir fyrirsögnina og tengilinn „Skoða upplýsingar“.</span><span class="sxs-lookup"><span data-stu-id="26433-122">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="26433-123">Stilla ætti tengilinn „Skoða upplýsingar“ til að framsenda á notandanetfangasíðuna.</span><span class="sxs-lookup"><span data-stu-id="26433-123">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="26433-124">**Vildarreitur reiknings** - Þessi eining er notuð til að sýna og tengjast upplýsingum um vildarkerfi.</span><span class="sxs-lookup"><span data-stu-id="26433-124">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="26433-125">Þessir reitir eru með tvær stöður: Ein staða sýnir tengla til að taka þátt í vildarkerfi ef notandinn er ekki meðlimur nú þegar.</span><span class="sxs-lookup"><span data-stu-id="26433-125">This tile has two states: one state shows links to join a loyalty progam if the user is not a member already.</span></span> <span data-ttu-id="26433-126">Hin staðan sýnir tengla til að skoða síðu vildarupplyýsinga þegar notandinn er þegar meðlimur.</span><span class="sxs-lookup"><span data-stu-id="26433-126">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="26433-127">Eiginleikar fela í sér fyrirsögnina, tengilinn „Skráning“ og tengilinn „Skoða hollustu“.</span><span class="sxs-lookup"><span data-stu-id="26433-127">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="26433-128">Stilla ætti tengilinn „Skoða vildarupplýsingar“ til að framsenda á vildarkerfissíðuna.</span><span class="sxs-lookup"><span data-stu-id="26433-128">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="26433-129">Stilla ætti tengilinn „Innskráning“ til að framsenda á síðu þar sem notendur geta tekið þátt í vildarkerfinu.</span><span class="sxs-lookup"><span data-stu-id="26433-129">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="26433-130">Pöntunarferilssíða</span><span class="sxs-lookup"><span data-stu-id="26433-130">Order history page</span></span>

<span data-ttu-id="26433-131">Pöntunarferilsíðan notar pöntunarferilseininguna til að sýna allar nýlegar pantanir sem notandinn hefur sett inn.</span><span class="sxs-lookup"><span data-stu-id="26433-131">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="26433-132">Upplýsingasíða pöntunar</span><span class="sxs-lookup"><span data-stu-id="26433-132">Order details page</span></span>

<span data-ttu-id="26433-133">Pöntunarupplýsingasíðan veitir ítarlegar upplýsingar um hverja pöntun og má nálgast af pöntunarferilssíðunni.</span><span class="sxs-lookup"><span data-stu-id="26433-133">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="26433-134">Það notar pöntunarupplýsingaeininguna, sem krefst sölukennis eða færslukennis til að sækja pöntunarupplýsingarnar.</span><span class="sxs-lookup"><span data-stu-id="26433-134">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="user-profile-page"></a><span data-ttu-id="26433-135">Notandaforstillingasíða</span><span class="sxs-lookup"><span data-stu-id="26433-135">User profile page</span></span>

<span data-ttu-id="26433-136">Notandaforstillingasíðan sýnir upplýsingar um notandareikning, svo sem nafn notanda og netfang.</span><span class="sxs-lookup"><span data-stu-id="26433-136">The user profile page shows user account details, such as a user's name and email address.</span></span> <span data-ttu-id="26433-137">Það notar upplýsingar um notandasnið og notendasnið til að breyta.</span><span class="sxs-lookup"><span data-stu-id="26433-137">It uses the user profile details and user profile edit modules.</span></span> <span data-ttu-id="26433-138">Þrátt fyrir að ekki sé hægt að fjarlægja netfangið er hægt að breyta því.</span><span class="sxs-lookup"><span data-stu-id="26433-138">Although the email address can't be removed, it can be edited.</span></span> <span data-ttu-id="26433-139">Notandasniðssíðan sýnir einnig óskir notenda sem gera notanda kleift að velja eða afþakka ákveðna eiginleika eins og að sérsníða meðmælalista.</span><span class="sxs-lookup"><span data-stu-id="26433-139">The user profile page also shows user preferences that enable a user to opt in or opt out from certain features, such as personalization of recommendation lists.</span></span> 

### <a name="user-address-page"></a><span data-ttu-id="26433-140">Netfangssíða notanda</span><span class="sxs-lookup"><span data-stu-id="26433-140">User address page</span></span>

<span data-ttu-id="26433-141">Netfangasíða notanda sýnir lista yfir netföng sem tengjast notendareikningnum.</span><span class="sxs-lookup"><span data-stu-id="26433-141">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="26433-142">Notandinn gaf þessi netföng annaðhvort upp í greiðsluferlinu eða bætti þeim beint við á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="26433-142">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="26433-143">Notendanetfangareiningin er notuð til að bæta við og breyta netföngum, stilla aðalnetfangið og láta núverandi netföng birtast á síðunni.</span><span class="sxs-lookup"><span data-stu-id="26433-143">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="26433-144">Óskalistasíða</span><span class="sxs-lookup"><span data-stu-id="26433-144">Wish list page</span></span>

<span data-ttu-id="26433-145">Óskalistasíðan sýnir atriðin sem hefur verið bætt við óskalista viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="26433-145">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="26433-146">Hún notar óskalistaeininguna til að birta atriði óskalista.</span><span class="sxs-lookup"><span data-stu-id="26433-146">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="26433-147">Síða vildarkerfis</span><span class="sxs-lookup"><span data-stu-id="26433-147">Loyalty page</span></span>

<span data-ttu-id="26433-148">Vildarkerfissíðan gerir viðskiptavinum kleift að skoða í vildarupplýsingar sínar ef þeir eru nú þegar meðlimir í vildarkerfi.</span><span class="sxs-lookup"><span data-stu-id="26433-148">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="26433-149">Þeir geta einnig skoðað stigin sem þeir hafa unnið og innleyst í nýlegum færslum.</span><span class="sxs-lookup"><span data-stu-id="26433-149">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="26433-150">Síðan notar vildarupplýsingareininguna til að sýna upplýsingar um vildarkerfi.</span><span class="sxs-lookup"><span data-stu-id="26433-150">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="26433-151">Til að taka þátt í vildarkerfi er hægt að búa til markaðssíðu með vildarskráningar og einingar fyrir vildarskilmála.</span><span class="sxs-lookup"><span data-stu-id="26433-151">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="26433-152">Ef notandinn er ekki meðlimur í vildarkerfi munu þessar einingar gera notandanum kleift að skrá sig.</span><span class="sxs-lookup"><span data-stu-id="26433-152">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="26433-153">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="26433-153">Additional resources</span></span>

[<span data-ttu-id="26433-154">Yfirlit byrjendaeiningar</span><span class="sxs-lookup"><span data-stu-id="26433-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="26433-155">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="26433-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="26433-156">Kaupkassaeining</span><span class="sxs-lookup"><span data-stu-id="26433-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="26433-157">Körfueining</span><span class="sxs-lookup"><span data-stu-id="26433-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="26433-158">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="26433-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="26433-159">Pöntunarstaðfestingareining</span><span class="sxs-lookup"><span data-stu-id="26433-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="26433-160">Fyrirsagnareining</span><span class="sxs-lookup"><span data-stu-id="26433-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="26433-161">Neðanmálseining</span><span class="sxs-lookup"><span data-stu-id="26433-161">Footer module</span></span>](author-footer-module.md)
