---
title: Frumstilla birgðastöðu í vöruhúsi
description: Þetta ferli sýnir hvernig á að uppfæra lagerbirgðir handvirkt með því að nota færslubók birgðahreyfinga.
author: perlynne
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6934fc8142a589532cbd9d360ca0f8276456b20e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011549"
---
# <a name="initialize-stock-levels-in-the-warehouse"></a><span data-ttu-id="e487b-103">Frumstilla birgðastöðu í vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="e487b-103">Initialize stock levels in the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e487b-104">Þetta ferli sýnir hvernig á að uppfæra lagerbirgðir handvirkt með því að nota færslubók birgðahreyfinga.</span><span class="sxs-lookup"><span data-stu-id="e487b-104">This procedure shows you how to get the on-hand inventory updated manually using an Inventory movement journal.</span></span> <span data-ttu-id="e487b-105">(Einnig er hægt að uppfæra lagerbirgðir með því að flytja inn færslur í gagnaeigind.) Hægt er að keyra þessa handbók í sýnifyrirtækinu USMF, þar sem öll frumskilyrði eins og heiti færslubókar, uppsetning á vörum, bókunarreglur og lyklar eru í boði.</span><span class="sxs-lookup"><span data-stu-id="e487b-105">(It's also possible to update on-hand inventory by importing transactions in data entities.) You can run this guide in demo data company USMF where all the prerequisites like journal name, item setup, posting profiles, and accounts are available.</span></span> <span data-ttu-id="e487b-106">Leiðbeiningarnar stinga upp á ákveðnum gildum fyrir vöruna og víddir sem eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="e487b-106">The guide suggests specific values for the item and dimensions that are used.</span></span> <span data-ttu-id="e487b-107">Ef þú velur aðra vöru gætirðu þurft að færa inn gildi fyrir aðrar víddir.</span><span class="sxs-lookup"><span data-stu-id="e487b-107">If you choose a different item, you may need to enter values for different dimensions.</span></span>

1. <span data-ttu-id="e487b-108">Fara í Birgðastjórnun > Færslubókarfærslur > Vörur > Hreyfing.</span><span class="sxs-lookup"><span data-stu-id="e487b-108">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="e487b-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e487b-109">Click New.</span></span>
3. <span data-ttu-id="e487b-110">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="e487b-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e487b-111">Veldu IMov.</span><span class="sxs-lookup"><span data-stu-id="e487b-111">Select IMov.</span></span>
    * <span data-ttu-id="e487b-112">Það eru góðar starfsvenjur að nota önnur sniðmát fyrir heiti færslubókar fyrir mismunandi viðskiptatilgang.</span><span class="sxs-lookup"><span data-stu-id="e487b-112">It's a good practice to use different journal name templates for the different business purposes.</span></span>  
5. <span data-ttu-id="e487b-113">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e487b-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="e487b-114">Í reitinn Mótlykill skal tilgreina gildin '140200'.</span><span class="sxs-lookup"><span data-stu-id="e487b-114">In the Offset account field, specify the values '140200'.</span></span>
    * <span data-ttu-id="e487b-115">Þetta er mótlykill sem verður sjálfgefinn lykill í færslubókarlínum.</span><span class="sxs-lookup"><span data-stu-id="e487b-115">This is the offset account that will be the default account on the journal lines.</span></span> <span data-ttu-id="e487b-116">Það er hægt að hnekkja sjálfgildinu til að úthluta öðrum mótlyklum á hverja línu.</span><span class="sxs-lookup"><span data-stu-id="e487b-116">It's possible to override the default to assign different offset accounts per line.</span></span>  
7. <span data-ttu-id="e487b-117">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e487b-117">Click OK.</span></span>
8. <span data-ttu-id="e487b-118">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e487b-118">Click New.</span></span>
9. <span data-ttu-id="e487b-119">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="e487b-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="e487b-120">Velja vöru A0001.</span><span class="sxs-lookup"><span data-stu-id="e487b-120">Select item A0001.</span></span>
11. <span data-ttu-id="e487b-121">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e487b-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="e487b-122">Smellið á flipann Birgðavíddir.</span><span class="sxs-lookup"><span data-stu-id="e487b-122">Click the Inventory dimensions tab.</span></span>
13. <span data-ttu-id="e487b-123">Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="e487b-123">In the Site field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="e487b-124">Velja svæði 1.</span><span class="sxs-lookup"><span data-stu-id="e487b-124">Select site 1.</span></span>
15. <span data-ttu-id="e487b-125">Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="e487b-125">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="e487b-126">Velja vöruhús 13.</span><span class="sxs-lookup"><span data-stu-id="e487b-126">Select warehouse 13.</span></span>
17. <span data-ttu-id="e487b-127">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="e487b-127">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="e487b-128">Í reitnum staðsetning skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="e487b-128">In the Location field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="e487b-129">Velja staðsetningu 13.</span><span class="sxs-lookup"><span data-stu-id="e487b-129">Select location 13.</span></span>
20. <span data-ttu-id="e487b-130">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="e487b-130">In the Quantity field, enter a number.</span></span>
21. <span data-ttu-id="e487b-131">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e487b-131">Click Save.</span></span>
22. <span data-ttu-id="e487b-132">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="e487b-132">Click Post.</span></span>
23. <span data-ttu-id="e487b-133">Merkja eða afmerkja í gátreitinn Millifæra allar bókunarvillur í nýja færslubók.</span><span class="sxs-lookup"><span data-stu-id="e487b-133">Check or uncheck the Transfer all posting errors to a new journal check box.</span></span>
    * <span data-ttu-id="e487b-134">Ef þú virkjar þennan valkost verða allar línur sem ekki bókast afritaðar í nýja færslubók.</span><span class="sxs-lookup"><span data-stu-id="e487b-134">If you enable this option, any lines that fail to post will be copied to a new journal.</span></span> <span data-ttu-id="e487b-135">Hægt er að nota upplýsingarnar í skránni til að leiðrétta vandamál og síðan endurbóka línurnar.</span><span class="sxs-lookup"><span data-stu-id="e487b-135">You can use the information in the log to correct the issues and then re-post the lines.</span></span>  
24. <span data-ttu-id="e487b-136">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e487b-136">Click OK.</span></span>
25. <span data-ttu-id="e487b-137">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e487b-137">Close the page.</span></span>
26. <span data-ttu-id="e487b-138">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e487b-138">Close the page.</span></span>

