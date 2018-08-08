--- 
title: "Bóka tímabilsbækur"
description: "Tímabilsbækur eru stundum kallaðir endurteknar færslubækur þar sem upphæð, texti og aðrar upplýsingar eru endurteknar í hvert sinn sem er sótt í tímabilsbók."
author: aprilolson
manager: AnnBe
ms.date: 02/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 4132f647d8fa225b402a006f0da2347ac9660fa0
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---
# <a name="post-periodic-journals"></a><span data-ttu-id="14e2c-103">Bóka tímabilsbækur</span><span class="sxs-lookup"><span data-stu-id="14e2c-103">Post periodic journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="14e2c-104">Tímabilsbækur eru stundum kallaðir endurteknar færslubækur þar sem upphæð, texti og aðrar upplýsingar eru endurteknar í hvert sinn sem er sótt í tímabilsbók.</span><span class="sxs-lookup"><span data-stu-id="14e2c-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="14e2c-105">Þegar þú stofnar reglulega tímabilsdagbók tilgreinirðu tímabilið sem líður á milli endurkomu, svo sem daga eða mánuði.</span><span class="sxs-lookup"><span data-stu-id="14e2c-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="14e2c-106">Þessar verkefnaleiðbeiningar munu stofna tímabilsbækur með mánaðarlegum endurtekningum.</span><span class="sxs-lookup"><span data-stu-id="14e2c-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>



1. <span data-ttu-id="14e2c-107">Fara í Fjárhag > Reglubundin verkefni > Tímabilsbækur.</span><span class="sxs-lookup"><span data-stu-id="14e2c-107">Go to General ledger > Periodic tasks > Periodic journals.</span></span>
2. <span data-ttu-id="14e2c-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="14e2c-108">Click New.</span></span>
3. <span data-ttu-id="14e2c-109">Sláið inn eða veldu gildi í reitnum heiti.</span><span class="sxs-lookup"><span data-stu-id="14e2c-109">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="14e2c-110">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="14e2c-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="14e2c-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="14e2c-111">In the Description field, type a value.</span></span>
    * <span data-ttu-id="14e2c-112">Lýsing verður nafn tímabilsbókar þegar sótt síðar svo tryggja að veita viðeigandi heiti.</span><span class="sxs-lookup"><span data-stu-id="14e2c-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>  
6. <span data-ttu-id="14e2c-113">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="14e2c-113">Click Lines.</span></span>
    * <span data-ttu-id="14e2c-114">Tímabilsbók hefur yfirleitt færslubókarlínur.</span><span class="sxs-lookup"><span data-stu-id="14e2c-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="14e2c-115">þessi leiðarvísi fyrir verk hins vegar aðeins bæta við einni línu.</span><span class="sxs-lookup"><span data-stu-id="14e2c-115">this task guide will however only add one line.</span></span>  
7. <span data-ttu-id="14e2c-116">Dagsetning er rituð í reitinn Dagetning.</span><span class="sxs-lookup"><span data-stu-id="14e2c-116">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="14e2c-117">Í þessum reit dagsetningar er bókunardagsetning fyrir næstu færslu í daglega færslubók.</span><span class="sxs-lookup"><span data-stu-id="14e2c-117">The Date field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="14e2c-118">Fyrir Færslubækur sem verða sóttar hvern mánuð mælt er með að nota dagsetningu í mánuði þegar verður að bóka hana, yfirleitt fyrsta eða síðasta degi tímabilsins.</span><span class="sxs-lookup"><span data-stu-id="14e2c-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="14e2c-119">Hægt er að hafa Dagsetningu svæðið autt og veita dagsetningu þegar færslubók er sótt með því að nota Auða svæðið dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="14e2c-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span>    <span data-ttu-id="14e2c-120">Svæðið uppfærist sjálfkrafa á næsta endurtekna dagsetningu þegar færslur eru sóttar.</span><span class="sxs-lookup"><span data-stu-id="14e2c-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span>  
8. <span data-ttu-id="14e2c-121">Í reitnum Lykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="14e2c-121">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="14e2c-122">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="14e2c-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="14e2c-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="14e2c-123">Close the page.</span></span>
11. <span data-ttu-id="14e2c-124">Í reitnum Debet skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="14e2c-124">In the Debit field, enter a number.</span></span>
12. <span data-ttu-id="14e2c-125">Í reitnum Mótlykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="14e2c-125">In the Offset account field, specify the desired values.</span></span>
13. <span data-ttu-id="14e2c-126">Í reitnum Eining skal velja ‚Mánuði‘.</span><span class="sxs-lookup"><span data-stu-id="14e2c-126">In the Unit field, select 'Months'.</span></span>
14. <span data-ttu-id="14e2c-127">Í reitnum Fjöldi eininga skal færa inn ‚1‘.</span><span class="sxs-lookup"><span data-stu-id="14e2c-127">In the Number of units field, enter '1'.</span></span>
15. <span data-ttu-id="14e2c-128">Í reitnum Síðasta dagsetning skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="14e2c-128">In the Last date field, enter a date.</span></span>
    * <span data-ttu-id="14e2c-129">Innsláttur síðustu dagsetningu á tímabilinu á undan kemur í veg fyrir að ítrekunarbók er stofnuðá röngu upphafstímabili.</span><span class="sxs-lookup"><span data-stu-id="14e2c-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="14e2c-130">Síðasta dagsetning verður síðar  uppfærð í hvert skipti sem tímabilsbók er sótt.</span><span class="sxs-lookup"><span data-stu-id="14e2c-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span>  
16. <span data-ttu-id="14e2c-131">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="14e2c-131">Click Save.</span></span>
17. <span data-ttu-id="14e2c-132">Farðu í Sjálfgefið mælaborð.</span><span class="sxs-lookup"><span data-stu-id="14e2c-132">Go to Default dashboard.</span></span>
18. <span data-ttu-id="14e2c-133">Fara í fjárhag > Færslubókarfærslur > Almennar færslubækur.</span><span class="sxs-lookup"><span data-stu-id="14e2c-133">Go to General ledger > Journal entries > General journals.</span></span>
19. <span data-ttu-id="14e2c-134">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="14e2c-134">Click New.</span></span>
20. <span data-ttu-id="14e2c-135">Sláið inn eða veldu gildi í reitnum heiti.</span><span class="sxs-lookup"><span data-stu-id="14e2c-135">In the Name field, enter or select a value.</span></span>
21. <span data-ttu-id="14e2c-136">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="14e2c-136">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="14e2c-137">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="14e2c-137">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="14e2c-138">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="14e2c-138">In the Description field, type a value.</span></span>
24. <span data-ttu-id="14e2c-139">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="14e2c-139">Click Lines.</span></span>
25. <span data-ttu-id="14e2c-140">Smella er á tímabilsbók.</span><span class="sxs-lookup"><span data-stu-id="14e2c-140">Click Period journal.</span></span>
26. <span data-ttu-id="14e2c-141">Smellt er á sækja færslubók.</span><span class="sxs-lookup"><span data-stu-id="14e2c-141">Click Retrieve journal.</span></span>
27. <span data-ttu-id="14e2c-142">Í reitinn Til dagsetningar skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="14e2c-142">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="14e2c-143">Til Dagsetningin gegnir hlutverki lokadagsetningar fyrir reglubundnar fylgiskjalslínurnar.</span><span class="sxs-lookup"><span data-stu-id="14e2c-143">The To date serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="14e2c-144">Á grundvelli endurtekningastillinga gætu Lokadagsetningin og Til dagsetningin sömu línu verið hafðar með oftar en einu sinni í færslubókinni sem verður til.</span><span class="sxs-lookup"><span data-stu-id="14e2c-144">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="14e2c-145">Til dagsetningar er sjálfvirkt uppfært samkvæmt dagsetningu lotu þegar tímabilslína var síðast millifærð í færslubók.</span><span class="sxs-lookup"><span data-stu-id="14e2c-145">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span>  
28. <span data-ttu-id="14e2c-146">Í reitinn tímabilsbækur skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="14e2c-146">In the Periodic journal number field, enter or select a value.</span></span>
29. <span data-ttu-id="14e2c-147">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="14e2c-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="14e2c-148">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="14e2c-148">Click OK.</span></span>
    * <span data-ttu-id="14e2c-149">Nú er hægt að endurskoða, samþykkja eða bóka tímabilsbók eftir þörf og uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="14e2c-149">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>  


