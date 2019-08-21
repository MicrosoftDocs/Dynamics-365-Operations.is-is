---
title: Setja greiðsluskilmála fyrir viðskiptavin
description: Þetta ferli skilgreinir staðgreiðsluafslátt og uppsetning gjalddaga.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cddccbeb60e3eb9e498affcaa547fddb145a2bb2
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846420"
---
# <a name="establish-customer-payment-terms"></a><span data-ttu-id="4a049-103">Setja greiðsluskilmála fyrir viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="4a049-103">Establish customer payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4a049-104">Þetta ferli skilgreinir staðgreiðsluafslátt og uppsetning gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="4a049-104">This procedure defines a cash discount and due date setup.</span></span> <span data-ttu-id="4a049-105">Þessi leiðarvísi fyrir verk notar sýnigögn USMF fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="4a049-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="4a049-106">Fara í Viðskiptakröfur > Uppsetningar greiðslu > Greiðsludagar.</span><span class="sxs-lookup"><span data-stu-id="4a049-106">Go to Accounts receivable > Payments setup > Payment days.</span></span>
    * <span data-ttu-id="4a049-107">Uppsetning Greiðsluskilmála er samnýtt fyrir Viðskiptakröfur og Viðskiptaskuldir.</span><span class="sxs-lookup"><span data-stu-id="4a049-107">The setup for the Terms of payment is shared for Accounts receivable and Accounts payable.</span></span> <span data-ttu-id="4a049-108">Ef verið er að skilgreina það í kerfinu, hún verður tiltæk í hinu kerfi einnig.</span><span class="sxs-lookup"><span data-stu-id="4a049-108">If you define it in module, it will be available in the other module also.</span></span> <span data-ttu-id="4a049-109">Fyrir þessa leiðarvísi fyrir verk, ég að setja upp allar greiðsluskilmála undir viðskiptakröfur.</span><span class="sxs-lookup"><span data-stu-id="4a049-109">For this task guide, I set up all the terms of payment under Accounts receivable.</span></span>  
2. <span data-ttu-id="4a049-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="4a049-110">Click New.</span></span>
    * <span data-ttu-id="4a049-111">Stofna greiðsludag þarfnist skal greiðsluskilmála þínir tiltekinn dag vikunnar (Mánudegi, Þriðjudegi, o. s. frv) eða á tilteknum degi hvers mánaðar (5., 10., o. s. frv).</span><span class="sxs-lookup"><span data-stu-id="4a049-111">Create a payment day if your terms of payment require a specific day of the week (Monday, Tuesday, etc) or a specific date of the month (5th, 10th, etc).</span></span>  
3. <span data-ttu-id="4a049-112">Í svæðið dagur Greiðslu er að færa inn Kenni fyrir greiðsludaginn í svæðið dagur greiðslu.</span><span class="sxs-lookup"><span data-stu-id="4a049-112">In the Payment day field, enter an ID for the Payment day in the payment day field.</span></span>
4. <span data-ttu-id="4a049-113">Færið inn lýsingu á greiðsludegi í svæðinu Lýsing..</span><span class="sxs-lookup"><span data-stu-id="4a049-113">In the Description field, enter a description of the payment day.</span></span>
5. <span data-ttu-id="4a049-114">Í svæðinu Viku/Mánuður velja Viku eða Mánuð.</span><span class="sxs-lookup"><span data-stu-id="4a049-114">In the Week/Month field, select either Week or Month.</span></span>
    * <span data-ttu-id="4a049-115">Ef óskað er að færa inn dag vikunnar, eins og Mánudegi, veljið Viku.</span><span class="sxs-lookup"><span data-stu-id="4a049-115">If you want to enter a day of the week, such as Monday, select Week.</span></span> <span data-ttu-id="4a049-116">Ef óskað er að færa inn dagsetningu í mánuði, svo sem 10, veljið Mánuð.</span><span class="sxs-lookup"><span data-stu-id="4a049-116">If you want to enter a date in the month, such as the 10th, select Month.</span></span> <span data-ttu-id="4a049-117">Velja Mánuð fyrir þetta dæmi.</span><span class="sxs-lookup"><span data-stu-id="4a049-117">Select Month for this example.</span></span>  
6. <span data-ttu-id="4a049-118">Í mánaðardagur svæðinu, færið inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="4a049-118">In the Day of month field, enter a date.</span></span>
    * <span data-ttu-id="4a049-119">Ætti að færa inn dagsetninguna sem tölu, til dæmis "10" og ekki sem ‚10.'.</span><span class="sxs-lookup"><span data-stu-id="4a049-119">The date should be entered as a number, such as '10', and not as '10th'.</span></span>  
7. <span data-ttu-id="4a049-120">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="4a049-120">Click Save.</span></span>
8. <span data-ttu-id="4a049-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="4a049-121">Close the page.</span></span>
9. <span data-ttu-id="4a049-122">Fara í Viðskiptakröfur > Uppsetning greiðslu > Greiðsluskilmálar.</span><span class="sxs-lookup"><span data-stu-id="4a049-122">Go to Accounts receivable > Payments setup > Terms of payment.</span></span>
10. <span data-ttu-id="4a049-123">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="4a049-123">Click New.</span></span>
    * <span data-ttu-id="4a049-124">Greiðsluskilmálar er notuð til að skilgreina hvernig gjalddagar verður reiknuð.</span><span class="sxs-lookup"><span data-stu-id="4a049-124">Terms of payment is used to define how the due dates will be calculated.</span></span> <span data-ttu-id="4a049-125">Uppsetning dagsetning staðgreiðsluafsláttar er skilgreind á sérstakri síðu.</span><span class="sxs-lookup"><span data-stu-id="4a049-125">The cash discount date setup is defined in a separate page.</span></span>  
11. <span data-ttu-id="4a049-126">Færið inn Kenni í reitnum greiðsluskilmálar í reitnum greiðsluskilmálar.</span><span class="sxs-lookup"><span data-stu-id="4a049-126">In the Terms of payment field, enter an ID in the Terms of payment field.</span></span>
12. <span data-ttu-id="4a049-127">Færið inn lýsingu í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="4a049-127">In the Description field, enter a description.</span></span>
13. <span data-ttu-id="4a049-128">Veljið greiðslumáta eins og Greiðslukröfu, Nettó, Gildandi mánuður, o.s.frv.</span><span class="sxs-lookup"><span data-stu-id="4a049-128">Select a Payment method such as COD, Net, Current month, etc.</span></span>
    * <span data-ttu-id="4a049-129">Greiðsluskilmálar eru notaðir til að skilgreina upphaf fyrir útreikning gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="4a049-129">The Payment method is used to define the start of how the due will be calculated.</span></span>  <span data-ttu-id="4a049-130">Til dæmis, Nettó er notað ef gjalddagi er alltaf ákveðnum fjölda mánaða eða daga eftir gjalddaga reiknings.</span><span class="sxs-lookup"><span data-stu-id="4a049-130">For example, Net is used if the due date is always a set number of months or days after the invoice date.</span></span> <span data-ttu-id="4a049-131">Hægt er að nota Greiðslukröfu þegar greiðslu er krafist við reikninginn, svo ekki sé reiknaður út gjalddagi.</span><span class="sxs-lookup"><span data-stu-id="4a049-131">COD can be used to when payment is required upon invoice, so a due date wouldn't be calculated.</span></span> <span data-ttu-id="4a049-132">Veljið Gildandi mánuð fyrir þennan leiðarvísi fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="4a049-132">Select Current month for this task guide.</span></span>  
14. <span data-ttu-id="4a049-133">Veljið greiðsludag ef tiltekinn dag, viku eða dagsetningu eru teknar með í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="4a049-133">Select a Payment day if a specific day of the  week or date are included in the calculation.</span></span>
    * <span data-ttu-id="4a049-134">Eftir greiðsluskilmála, má færa inn magn í Mánuðum eða Dögum.</span><span class="sxs-lookup"><span data-stu-id="4a049-134">Depending on your terms of payment, you may enter a quantity in Months or Days.</span></span> <span data-ttu-id="4a049-135">Eða hægt er að nota greiðsluáætlun eða greiðsludag til að ' bæta ' við lok greiðsluaðferðar.</span><span class="sxs-lookup"><span data-stu-id="4a049-135">Or you can use the Payment schedule or Payment day to 'add' to the end of the Payment method.</span></span> <span data-ttu-id="4a049-136">Gjalddagi verður alltaf að vera 10 næsta mánuð, veljið greiðsludag sem á 10.</span><span class="sxs-lookup"><span data-stu-id="4a049-136">If the due date will always be the 10th of the next month, select a Payment day of the 10th.</span></span>  
15. <span data-ttu-id="4a049-137">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="4a049-137">Click Save.</span></span>
16. <span data-ttu-id="4a049-138">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="4a049-138">Close the page.</span></span>
17. <span data-ttu-id="4a049-139">Fara í Viðskiptakröfur> Greiðsluuppsetning > Staðgreiðsluafsláttur.</span><span class="sxs-lookup"><span data-stu-id="4a049-139">Go to Accounts receivable > Payments setup > Cash discounts.</span></span>
18. <span data-ttu-id="4a049-140">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="4a049-140">Click New.</span></span>
    * <span data-ttu-id="4a049-141">Þessi síða er notuð til að skilgreina hvernig dagsetning staðgreiðsluafsláttar reiknaðar.</span><span class="sxs-lookup"><span data-stu-id="4a049-141">This page is used to define how the cash discount date will be calculated.</span></span>  
19. <span data-ttu-id="4a049-142">Færið inn Kenni í svæðinu staðgreiðsluafslátt í svæðinu staðgreiðsluafslátt.</span><span class="sxs-lookup"><span data-stu-id="4a049-142">In the Cash discount field, enter an ID in the Cash discount field.</span></span>
20. <span data-ttu-id="4a049-143">Færið inn lýsingu í svæðinu Lýsingu.</span><span class="sxs-lookup"><span data-stu-id="4a049-143">In the Description field, enter a description.</span></span>
21. <span data-ttu-id="4a049-144">Ef lagskipt staðgreiðsluafsláttar er tiltækur skal velja Næsta afsláttarkóða sem á við eftir þennan nýja staðgreiðsluafslátt.</span><span class="sxs-lookup"><span data-stu-id="4a049-144">If a tiered cash discount is available, select the Next discount code that is relevant after this new cash discount.</span></span>
22. <span data-ttu-id="4a049-145">Færið inn fjölda daga sem er notað til að reikna út dagsetningu staðgreiðsluafsláttar</span><span class="sxs-lookup"><span data-stu-id="4a049-145">Enter the number of days used to calculate the cash dicount date.</span></span>
    * <span data-ttu-id="4a049-146">Ef Nettó reglu er valinn er fjöldi daga bætt við dagsetningu reiknings til að reikna út dagsetningu staðgreiðsluafsláttar.</span><span class="sxs-lookup"><span data-stu-id="4a049-146">If Net principle is selected, the number of days will be added to the invoice date to calculate the cash discount date.</span></span>  
23. <span data-ttu-id="4a049-147">Færið inn prósentutala staðgreiðsluafsláttar.</span><span class="sxs-lookup"><span data-stu-id="4a049-147">Enter the percentage of the cash discount.</span></span>
24. <span data-ttu-id="4a049-148">Færið inn aðallykilinn sem staðgreiðsluafsláttur eru bókuð fyrir reikninga viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="4a049-148">Enter the main account to which the cash discount will post for customer invoices.</span></span>
25. <span data-ttu-id="4a049-149">Veljið valkost í svæðinu Afsláttur mótlykla.</span><span class="sxs-lookup"><span data-stu-id="4a049-149">In the Discount offset accounts field, select an option.</span></span>
    * <span data-ttu-id="4a049-150">Ef valið er ‚Lyklar í línum reiknings' valið staðgreiðsluafsláttur verður bókaður á sama aðallykil eignar/kostnað í línum reiknings lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="4a049-150">If you select 'Accounts on the invoice lines', the cash discount will post to the same asset/expense main account on the lines of the vendor invoice.</span></span> <span data-ttu-id="4a049-151">Ef valið er 'Nota aðallykil fyrir reikninga lánardrottins' verður staðgreiðsluafsláttar bókuð í aðallykil sem er skilgreindur á 'aðallykils fyrir reikninga lánardrottins'.</span><span class="sxs-lookup"><span data-stu-id="4a049-151">If you select 'Use main account for vendor invoices', the cash discount will post to the main account you define in the 'Main account for vendor invoices'.</span></span> <span data-ttu-id="4a049-152">Í þessu dæmi, veljið 'Nota aðallykil fyrir reikninga lánardrottins.'</span><span class="sxs-lookup"><span data-stu-id="4a049-152">For this example, select 'Use main account for vendor invoices.'</span></span>  
26. <span data-ttu-id="4a049-153">Færið inn aðallykilinn sem staðgreiðsluafsláttur eru bókuð fyrir reikninga lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="4a049-153">Enter the main account to which the cash discount will post for vendor invoices.</span></span>
27. <span data-ttu-id="4a049-154">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="4a049-154">Click Save.</span></span>

