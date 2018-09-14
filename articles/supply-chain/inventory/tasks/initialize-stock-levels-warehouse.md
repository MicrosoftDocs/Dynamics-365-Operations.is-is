--- 
title: "Frumstilla birgðastöðu í vöruhúsi"
description: "Þetta ferli sýnir hvernig á að uppfæra lagerbirgðir handvirkt með því að nota færslubók birgðahreyfinga."
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalMovement, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 4bfa40c19e34631edb68b8cff42e7f72eb9ce2ad
ms.contentlocale: is-is
ms.lasthandoff: 09/14/2018

---
# <a name="initialize-stock-levels-in-the-warehouse"></a><span data-ttu-id="f2c6c-103">Frumstilla birgðastöðu í vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="f2c6c-103">Initialize stock levels in the warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f2c6c-104">Þetta ferli sýnir hvernig á að uppfæra lagerbirgðir handvirkt með því að nota færslubók birgðahreyfinga.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-104">This procedure shows you how to get the on-hand inventory updated manually using an Inventory movement journal.</span></span> <span data-ttu-id="f2c6c-105">(Einnig er hægt að uppfæra lagerbirgðir með því að flytja inn færslur í gagnaeigind.) Hægt er að keyra þessa handbók í sýnifyrirtækinu USMF, þar sem öll frumskilyrði eins og heiti færslubókar, uppsetning á vörum, bókunarreglur og lyklar eru í boði.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-105">(It’s also possible to update on-hand inventory by importing transactions in data entities.) You can run this guide in demo data company USMF where all the prerequisites like journal name, item setup, posting profiles, and accounts are available.</span></span> <span data-ttu-id="f2c6c-106">Leiðbeiningarnar stinga upp á ákveðnum gildum fyrir vöruna og víddir sem eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-106">The guide suggests specific values for the item and dimensions that are used.</span></span> <span data-ttu-id="f2c6c-107">Ef þú velur aðra vöru gætirðu þurft að færa inn gildi fyrir aðrar víddir.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-107">If you choose a different item, you may need to enter values for different dimensions.</span></span>

1. <span data-ttu-id="f2c6c-108">Fara í Birgðastjórnun > Færslubókarfærslur > Vörur > Hreyfing.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-108">Go to Inventory management > Journal entries > Items > Movement.</span></span>
2. <span data-ttu-id="f2c6c-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-109">Click New.</span></span>
3. <span data-ttu-id="f2c6c-110">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f2c6c-111">Veldu IMov.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-111">Select IMov.</span></span>
    * <span data-ttu-id="f2c6c-112">Það eru góðar starfsvenjur að nota önnur sniðmát fyrir heiti færslubókar fyrir mismunandi viðskiptatilgang.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-112">It’s a good practise to use different journal name templates for the different business purposes.</span></span>  
5. <span data-ttu-id="f2c6c-113">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="f2c6c-114">Í reitinn Mótlykill skal tilgreina gildin '140200'.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-114">In the Offset account field, specify the values '140200'.</span></span>
    * <span data-ttu-id="f2c6c-115">Þetta er mótlykill sem verður sjálfgefinn lykill í færslubókarlínum.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-115">This is the offset account that will be the default account on the journal lines.</span></span> <span data-ttu-id="f2c6c-116">Það er hægt að hnekkja sjálfgildinu til að úthluta öðrum mótlyklum á hverja línu.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-116">It’s possible to override the default to assign different offset accounts per line.</span></span>  
7. <span data-ttu-id="f2c6c-117">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-117">Click OK.</span></span>
8. <span data-ttu-id="f2c6c-118">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-118">Click New.</span></span>
9. <span data-ttu-id="f2c6c-119">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="f2c6c-120">Velja vöru A0001.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-120">Select item A0001.</span></span>
11. <span data-ttu-id="f2c6c-121">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="f2c6c-122">Smellið á flipann Birgðavíddir.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-122">Click the Inventory dimensions tab.</span></span>
13. <span data-ttu-id="f2c6c-123">Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-123">In the Site field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="f2c6c-124">Velja svæði 1.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-124">Select site 1.</span></span>
15. <span data-ttu-id="f2c6c-125">Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-125">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="f2c6c-126">Velja vöruhús 13.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-126">Select warehouse 13.</span></span>
17. <span data-ttu-id="f2c6c-127">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-127">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="f2c6c-128">Í reitnum staðsetning skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-128">In the Location field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="f2c6c-129">Velja staðsetningu 13.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-129">Select location 13.</span></span>
20. <span data-ttu-id="f2c6c-130">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-130">In the Quantity field, enter a number.</span></span>
21. <span data-ttu-id="f2c6c-131">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-131">Click Save.</span></span>
22. <span data-ttu-id="f2c6c-132">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-132">Click Post.</span></span>
23. <span data-ttu-id="f2c6c-133">Merkja eða afmerkja í gátreitinn Millifæra allar bókunarvillur í nýja færslubók.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-133">Check or uncheck the Transfer all posting errors to a new journal check box.</span></span>
    * <span data-ttu-id="f2c6c-134">Ef þú virkjar þennan valkost verða allar línur sem ekki bókast afritaðar í nýja færslubók.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-134">If you enable this option, any lines that fail to post will be copied to a new journal.</span></span> <span data-ttu-id="f2c6c-135">Hægt er að nota upplýsingarnar í skránni til að leiðrétta vandamál og síðan endurbóka línurnar.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-135">You can use the information in the log to correct the issues and then re-post the lines.</span></span>  
24. <span data-ttu-id="f2c6c-136">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-136">Click OK.</span></span>
25. <span data-ttu-id="f2c6c-137">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-137">Close the page.</span></span>
26. <span data-ttu-id="f2c6c-138">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f2c6c-138">Close the page.</span></span>


