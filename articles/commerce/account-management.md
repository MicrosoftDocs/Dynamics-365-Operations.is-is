---
title: Síður og einingar fyrir stjórnun reikninga
description: Þetta efnisatriði lýsir síðum og einingum fyrir stjórnun reikninga í Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: df4959a61f1b2948c62a558523a848ff8b2fe0a8
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796295"
---
# <a name="account-management-pages-and-modules"></a><span data-ttu-id="b5920-103">Síður og einingar fyrir stjórnun reikninga</span><span class="sxs-lookup"><span data-stu-id="b5920-103">Account management pages and modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b5920-104">Þetta efnisatriði lýsir síðum og einingum fyrir stjórnun reikninga í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b5920-104">This topic covers account management pages and modules in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b5920-105">Með stjórnun reikninga er átt við hóp síðna sem notaðar eru til að stjórna upplýsingum sem tengjast notendareikningi í Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b5920-105">Account management refers to a group of pages that is used to manage user account–related information in Dynamics 365 Commerce.</span></span> <span data-ttu-id="b5920-106">Reikningsstjórnunarsíður innihalda lendingasíðu reikningsstjórnunar, notandaforstillingasíðu, notendasíðu, síðu pöntunarferils, pöntunarupplýsingasíðu, vildarsíðu og óskalistasíðu.</span><span class="sxs-lookup"><span data-stu-id="b5920-106">Account management pages include the account management landing page, user profile page, user address page, order history page, order details page, loyalty page, and wish list page.</span></span>

### <a name="account-management-landing-page"></a><span data-ttu-id="b5920-107">Lendingasíða fyrir stjórnun reikninga</span><span class="sxs-lookup"><span data-stu-id="b5920-107">Account management landing page</span></span>

<span data-ttu-id="b5920-108">Lendingasíða reikningsstjórnunar notar eftirfarandi einingar:</span><span class="sxs-lookup"><span data-stu-id="b5920-108">The account management landing page uses the following modules:</span></span>

- <span data-ttu-id="b5920-109">**Gámur** - Allar lendingarsíðueiningar reikningsstjórnunar skulu settar í gám.</span><span class="sxs-lookup"><span data-stu-id="b5920-109">**Container** - All account management landing page modules should be placed within a container.</span></span> 
- <span data-ttu-id="b5920-110">**Móttökureitur reiknings** - Þessi eining er notuð til að veita móttökuskilaboð á reikningssíðu.</span><span class="sxs-lookup"><span data-stu-id="b5920-110">**Account welcome tile** – This module is used to provide a welcome message on the account management page.</span></span> <span data-ttu-id="b5920-111">Hann felur í sér eiginleika fyrir fyrirsögnina.</span><span class="sxs-lookup"><span data-stu-id="b5920-111">It includes properties for the heading.</span></span>
- <span data-ttu-id="b5920-112">**Almennir reitir reiknings** - Þessa einingu er hægt að nota til að útvega fyrirsagnir og tengla á reikningastjórnarsíður, svo sem „Pöntunarferill“ eða „Prófíllinn minn“.</span><span class="sxs-lookup"><span data-stu-id="b5920-112">**Account generic tile** - This module can be used to provide headings and links to account management pages, such as the "Order history" or "My profile" pages.</span></span> <span data-ttu-id="b5920-113">Hægt er að nota almenna reitaeiningu til að stilla reit fyrir hvaða síðu sem er.</span><span class="sxs-lookup"><span data-stu-id="b5920-113">The generic tile module can be used to configure a tile for any page.</span></span> <span data-ttu-id="b5920-114">Í Fabrikam er þessi eining notuð fyrir tengilinn „Pöntunarferill“ og „Prófíllinn minn“ á lendingasíðu reikningsstjórnunar.</span><span class="sxs-lookup"><span data-stu-id="b5920-114">In Fabrikam, this module is used for "Order history" and "My profile" page links on the account management landing page.</span></span>
- <span data-ttu-id="b5920-115">**Óskalistareitur reiknings** - Þessi eining er notuð til að gefa yfirlit yfir hluti á óskalista viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="b5920-115">**Account wishlist tile** – This module is used to provide a summary of the items on the customer's wish list.</span></span> <span data-ttu-id="b5920-116">Til dæmis gæti hann fullyrt: „Þú ert með 10 atriði á óskalistanum þínum.“</span><span class="sxs-lookup"><span data-stu-id="b5920-116">For example, it might state, "You have 10 items in your wish list."</span></span> <span data-ttu-id="b5920-117">Hún felur í sér eiginleika fyrir fyrirsögnina og tengilinn „Skoða upplýsingar“.</span><span class="sxs-lookup"><span data-stu-id="b5920-117">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="b5920-118">Stilla ætti tengilinn „Skoða upplýsingar“ til að framsenda á óskalistasíðuna.</span><span class="sxs-lookup"><span data-stu-id="b5920-118">The "View details" link should be configured to redirect to the wish list page.</span></span> 
- <span data-ttu-id="b5920-119">**Netfangareitur reiknings** - Þessi eining er notuð til að gefa yfirlit yfir netföng notandans.</span><span class="sxs-lookup"><span data-stu-id="b5920-119">**Account address tile** – This module is used to provide a summary of the user's addresses.</span></span> <span data-ttu-id="b5920-120">Til dæmis gæti hún fullyrt: „Þú ert með 2 netföng bætt við reikninginn þinn.“</span><span class="sxs-lookup"><span data-stu-id="b5920-120">For example, it might state, "You have 2 addresses added to your account."</span></span> <span data-ttu-id="b5920-121">Hún felur í sér eiginleika fyrir fyrirsögnina og tengilinn „Skoða upplýsingar“.</span><span class="sxs-lookup"><span data-stu-id="b5920-121">It includes properties for the heading and the "View details" link.</span></span> <span data-ttu-id="b5920-122">Stilla ætti tengilinn „Skoða upplýsingar“ til að framsenda á notandanetfangasíðuna.</span><span class="sxs-lookup"><span data-stu-id="b5920-122">The "View details" link should be configured to redirect to the user address page.</span></span>
- <span data-ttu-id="b5920-123">**Vildarreitur reiknings** - Þessi eining er notuð til að sýna og tengjast upplýsingum um vildarkerfi.</span><span class="sxs-lookup"><span data-stu-id="b5920-123">**Account loyalty tile** – This module is used to display and link to loyalty program information.</span></span> <span data-ttu-id="b5920-124">Þessi reitur er með tvær stöður: Ein staða sýnir tengla til að taka þátt í vildarkerfi ef notandinn er ekki meðlimur nú þegar.</span><span class="sxs-lookup"><span data-stu-id="b5920-124">This tile has two states: one state shows links to join a loyalty program if the user is not a member already.</span></span> <span data-ttu-id="b5920-125">Hin staðan sýnir tengla til að skoða síðu vildarupplyýsinga þegar notandinn er þegar meðlimur.</span><span class="sxs-lookup"><span data-stu-id="b5920-125">The other state shows links to view the loyalty details page when the user is already a member.</span></span> <span data-ttu-id="b5920-126">Eiginleikar fela í sér fyrirsögnina, tengilinn „Skráning“ og tengilinn „Skoða hollustu“.</span><span class="sxs-lookup"><span data-stu-id="b5920-126">Properties include the heading, the "Sign-up" link, and the "View loyalty" link.</span></span> <span data-ttu-id="b5920-127">Stilla ætti tengilinn „Skoða vildarupplýsingar“ til að framsenda á vildarkerfissíðuna.</span><span class="sxs-lookup"><span data-stu-id="b5920-127">The "View loyalty" link should be configured to redirect to the loyalty page.</span></span> <span data-ttu-id="b5920-128">Stilla ætti tengilinn „Innskráning“ til að framsenda á síðu þar sem notendur geta tekið þátt í vildarkerfinu.</span><span class="sxs-lookup"><span data-stu-id="b5920-128">The "Sign-up" link should be configured to redirect to a page where users can join the loyalty program.</span></span> 

### <a name="order-history-page"></a><span data-ttu-id="b5920-129">Pöntunarferilssíða</span><span class="sxs-lookup"><span data-stu-id="b5920-129">Order history page</span></span>

<span data-ttu-id="b5920-130">Pöntunarferilsíðan notar pöntunarferilseininguna til að sýna allar nýlegar pantanir sem notandinn hefur sett inn.</span><span class="sxs-lookup"><span data-stu-id="b5920-130">The order history page uses the order history module to show all the recent orders that the user has placed.</span></span>

### <a name="order-details-page"></a><span data-ttu-id="b5920-131">Upplýsingasíða pöntunar</span><span class="sxs-lookup"><span data-stu-id="b5920-131">Order details page</span></span>

<span data-ttu-id="b5920-132">Pöntunarupplýsingasíðan veitir ítarlegar upplýsingar um hverja pöntun og má nálgast af pöntunarferilssíðunni.</span><span class="sxs-lookup"><span data-stu-id="b5920-132">The order details page provides detailed information for each order and is accessed from the order history page.</span></span> <span data-ttu-id="b5920-133">Það notar pöntunarupplýsingaeininguna, sem krefst sölukennis eða færslukennis til að sækja pöntunarupplýsingarnar.</span><span class="sxs-lookup"><span data-stu-id="b5920-133">It uses the order details module, which requires the sales ID or transaction ID to retrieve the order details.</span></span>

### <a name="my-profile-page"></a><span data-ttu-id="b5920-134">Forstillingarsíða mín</span><span class="sxs-lookup"><span data-stu-id="b5920-134">My profile page</span></span>

<span data-ttu-id="b5920-135">Notandasíða mín sýnir upplýsingar um notandasíðu reikningsins þíns með einingu reikningsstillingar.</span><span class="sxs-lookup"><span data-stu-id="b5920-135">The My profile page shows the user's account profile details using the account profile module.</span></span> <span data-ttu-id="b5920-136">Síðan sýnir netfangið sem er tengt við reikning notanda, auk kjörstillingar sem eru settar upp fyrir reikninginn.</span><span class="sxs-lookup"><span data-stu-id="b5920-136">The page shows the email address associated with the user's account, as well as preferences set up for the account.</span></span> <span data-ttu-id="b5920-137">Ef sérstilltir eiginleika viðskiptavinar eru settir upp birtir eigindin „Viðbótarupplýsingar“ einnig þessa eiginleika.</span><span class="sxs-lookup"><span data-stu-id="b5920-137">If setting up custom customer attributes, an "Additional Information" section will also display those attributes.</span></span> <span data-ttu-id="b5920-138">Notendur geta breytt nafni sínu, kjörstillingum eða viðbótarupplýsingum (ef þær eru til staðar).</span><span class="sxs-lookup"><span data-stu-id="b5920-138">Users can edit their name, preferences, or additional information (if available).</span></span>

### <a name="user-address-page"></a><span data-ttu-id="b5920-139">Netfangssíða notanda</span><span class="sxs-lookup"><span data-stu-id="b5920-139">User address page</span></span>

<span data-ttu-id="b5920-140">Netfangasíða notanda sýnir lista yfir netföng sem tengjast notendareikningnum.</span><span class="sxs-lookup"><span data-stu-id="b5920-140">The user address page shows the list of addresses that are associated with the user account.</span></span> <span data-ttu-id="b5920-141">Notandinn gaf þessi netföng annaðhvort upp í greiðsluferlinu eða bætti þeim beint við á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="b5920-141">The user either provided these addresses during checkout or added them directly on  this page.</span></span> <span data-ttu-id="b5920-142">Notendanetfangareiningin er notuð til að bæta við og breyta netföngum, stilla aðalnetfangið og láta núverandi netföng birtast á síðunni.</span><span class="sxs-lookup"><span data-stu-id="b5920-142">The user address module is used add and edit addresses, set the primary address, and render existing addresses on the page.</span></span>

### <a name="wish-list-page"></a><span data-ttu-id="b5920-143">Óskalistasíða</span><span class="sxs-lookup"><span data-stu-id="b5920-143">Wish list page</span></span>

<span data-ttu-id="b5920-144">Óskalistasíðan sýnir atriðin sem hefur verið bætt við óskalista viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="b5920-144">The wish list page shows the items that have been added to the customer's wish list.</span></span> <span data-ttu-id="b5920-145">Hún notar óskalistaeininguna til að birta atriði óskalista.</span><span class="sxs-lookup"><span data-stu-id="b5920-145">It uses the wish list module to render wish list items.</span></span>

### <a name="loyalty-page"></a><span data-ttu-id="b5920-146">Síða vildarkerfis</span><span class="sxs-lookup"><span data-stu-id="b5920-146">Loyalty page</span></span>

<span data-ttu-id="b5920-147">Vildarkerfissíðan gerir viðskiptavinum kleift að skoða í vildarupplýsingar sínar ef þeir eru nú þegar meðlimir í vildarkerfi.</span><span class="sxs-lookup"><span data-stu-id="b5920-147">The loyalty page lets customers view their loyalty details if they are already loyalty program members.</span></span> <span data-ttu-id="b5920-148">Þeir geta einnig skoðað stigin sem þeir hafa unnið og innleyst í nýlegum færslum.</span><span class="sxs-lookup"><span data-stu-id="b5920-148">They can also view the points that they have earned and redeemed in recent transactions.</span></span> <span data-ttu-id="b5920-149">Síðan notar vildarupplýsingareininguna til að sýna upplýsingar um vildarkerfi.</span><span class="sxs-lookup"><span data-stu-id="b5920-149">The page uses the loyalty details module to showcase the loyalty details.</span></span> 

<span data-ttu-id="b5920-150">Til að taka þátt í vildarkerfi er hægt að búa til markaðssíðu með vildarskráningar og einingar fyrir vildarskilmála.</span><span class="sxs-lookup"><span data-stu-id="b5920-150">To join loyalty program, a marketing page can be created with loyalty sign up and loyalty terms modules.</span></span> <span data-ttu-id="b5920-151">Ef notandinn er ekki meðlimur í vildarkerfi munu þessar einingar gera notandanum kleift að skrá sig.</span><span class="sxs-lookup"><span data-stu-id="b5920-151">If the user is not a member of a loyalty program, these modules will enable the user to sign up.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5920-152">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b5920-152">Additional resources</span></span>

[<span data-ttu-id="b5920-153">Yfirlit einingasafns</span><span class="sxs-lookup"><span data-stu-id="b5920-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b5920-154">Hólfeining</span><span class="sxs-lookup"><span data-stu-id="b5920-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b5920-155">Kaupgluggaeining</span><span class="sxs-lookup"><span data-stu-id="b5920-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b5920-156">Körfueining</span><span class="sxs-lookup"><span data-stu-id="b5920-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b5920-157">Greiðsluferliseining</span><span class="sxs-lookup"><span data-stu-id="b5920-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b5920-158">Pöntunarstaðfestingareining</span><span class="sxs-lookup"><span data-stu-id="b5920-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b5920-159">Fyrirsagnareining</span><span class="sxs-lookup"><span data-stu-id="b5920-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="b5920-160">Neðanmálseining</span><span class="sxs-lookup"><span data-stu-id="b5920-160">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]