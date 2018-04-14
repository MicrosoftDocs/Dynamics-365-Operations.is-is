--- 
title: "Stofna innheimtubréfaröð"
description: "Notið þessa leiðarvísi fyrir verk til að stofna innheimtubréfaröð."
author: mikefalkner
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5905a630addfd850d22d34bdbecf116e83b4933f
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-collection-letter-sequence"></a><span data-ttu-id="ca506-103">Stofna innheimtubréfaröð</span><span class="sxs-lookup"><span data-stu-id="ca506-103">Create a collection letter sequence</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ca506-104">Notið þessa leiðarvísi fyrir verk til að stofna innheimtubréfaröð.</span><span class="sxs-lookup"><span data-stu-id="ca506-104">Use this task guide to create a collection letter sequence.</span></span> <span data-ttu-id="ca506-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="ca506-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="ca506-106">Fara í Skuldir og innheimta > Uppsetning > Setja upp innheimtubréfaröð.</span><span class="sxs-lookup"><span data-stu-id="ca506-106">Go to Credit and collections > Setup > Set up collection letter sequence.</span></span>
2. <span data-ttu-id="ca506-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="ca506-107">Click New.</span></span>
3. <span data-ttu-id="ca506-108">Í svæðinu Kenni númeraraðarinnar skal færa inn kenni raðar sem mun standa fyrir röðina.</span><span class="sxs-lookup"><span data-stu-id="ca506-108">In the Collection letter sequence field, enter a sequence ID that will represent the sequence.</span></span> <span data-ttu-id="ca506-109">Það verður notuð þegar þú setur upp bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="ca506-109">It will be used when you set up a posting profile.</span></span>
4. <span data-ttu-id="ca506-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="ca506-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="ca506-111">Greiðsluskilmálar eru valfrjálsar.</span><span class="sxs-lookup"><span data-stu-id="ca506-111">The terms of payment is optional.</span></span> <span data-ttu-id="ca506-112">Ef fært er inn hér gildi, reikningur þóknunar innheimtubréfs nota þessar greiðsluskilmála í stað greiðsluskilmálar geymd með viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="ca506-112">If you enter a value here, the collection letter fee invoice will use these terms of payment instead of the terms of payment stored with the customer.</span></span>  
5. <span data-ttu-id="ca506-113">Í safn innheimtubréfs svæðinu, skal velja kóða fyrir fyrsta innheimtubréfið sem á að senda.</span><span class="sxs-lookup"><span data-stu-id="ca506-113">In the collection letter code field, select the code for the first collection letter that you want to send.</span></span>
    * <span data-ttu-id="ca506-114">Fyrsta innheimtubréf er stofna samkvæmt gjalddagi á reikningur, gildi sem þú færa inn fyrir biðtími í svæði dagar á þessari línu, og aðrar upplýsingar sem þú færa inn á þessari línu.</span><span class="sxs-lookup"><span data-stu-id="ca506-114">The first collection letter is created according to the due date on the invoice, the value that you enter for the grace period in the Days field on this line, and other information that you enter on this line.</span></span>  
6. <span data-ttu-id="ca506-115">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="ca506-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="ca506-116">Gjaldmiðill fyrir fyrir þóknun fær sjálfgildi í gjaldmiðli viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="ca506-116">The currency for the fee defaults to the customer currency.</span></span> <span data-ttu-id="ca506-117">Þessi gjaldmiðilskóði getur verið annað en gjaldmiðli reikningsins.</span><span class="sxs-lookup"><span data-stu-id="ca506-117">This currency code can be different than the invoice currency.</span></span>  
7. <span data-ttu-id="ca506-118">Smella á bæta Við til að bæta við næsta innheimtubréf sem verða sendar í röðinni</span><span class="sxs-lookup"><span data-stu-id="ca506-118">Click Add to add the next collection letter that will be sent in the sequence</span></span>
    * <span data-ttu-id="ca506-119">Í mörgum tilvikum fyrsta innheimtubréfið er bara viðvörun.</span><span class="sxs-lookup"><span data-stu-id="ca506-119">In many cases, the first collection letter is just a warning.</span></span> <span data-ttu-id="ca506-120">Hægt er að bæta þóknun ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="ca506-120">You can add fees if needed.</span></span>  
8. <span data-ttu-id="ca506-121">Í svæðinu kóði innheimtubréfs , veljið næsta innheimtubréf sem verða sendar í röðinni.</span><span class="sxs-lookup"><span data-stu-id="ca506-121">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
9. <span data-ttu-id="ca506-122">Í reitinn Lýsing skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ca506-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="ca506-123">Velja tekjurreiknings se, verður notaður fyrir þóknanir í svæðinu aðallykill.</span><span class="sxs-lookup"><span data-stu-id="ca506-123">In the main account field, select the revenue account that will be used for fees.</span></span>
11. <span data-ttu-id="ca506-124">Færið inn gjöld sem verður krafinn þegar þessu innheimtubréfi er bókuð.</span><span class="sxs-lookup"><span data-stu-id="ca506-124">Enter the fee that will be charged when this collection letter is posted.</span></span>
12. <span data-ttu-id="ca506-125">Í reitnum VSK-flokkur vöru skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="ca506-125">In the Item sales tax group field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="ca506-126">Veljið vsk-flokkur vöru ef þarf að reikna út vsk á þóknunina.</span><span class="sxs-lookup"><span data-stu-id="ca506-126">Select an item sales tax group if sales taxes must be calculated on the fee.</span></span>  
13. <span data-ttu-id="ca506-127">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="ca506-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="ca506-128">Færðu inn lágmarks gjaldfallna stöðu sem krafist er áður en innheimtubréf er sent.</span><span class="sxs-lookup"><span data-stu-id="ca506-128">Enter the minimum overdue balance required before a collection letter is sent.</span></span>
15. <span data-ttu-id="ca506-129">Færið inn fjölda biðdaga sem verður leyft.</span><span class="sxs-lookup"><span data-stu-id="ca506-129">Enter the number of grace days that you will allow.</span></span>
    * <span data-ttu-id="ca506-130">Þetta er fjöldi daga eftir gjalddag sem hægt er að mynda innheimtubréf.</span><span class="sxs-lookup"><span data-stu-id="ca506-130">This is the number of days after the due date that a collection letter can be generated.</span></span> <span data-ttu-id="ca506-131">Gjalddagi sem er notað fyrir útreikning fer eftir stöðu innheimtubréfs í innheimtubréfaröðinni: ⦁ Biðtími fyrir innheimtubréf 1 stendur í samhengi við gjalddaga á reikningnum.</span><span class="sxs-lookup"><span data-stu-id="ca506-131">The due date that is used for the calculation depends on the position of the collection letter in the collection letter sequence:   ⦁    The grace period for collection letter 1 is relative to the due date on the invoice.</span></span>  <span data-ttu-id="ca506-132">⦁ Biðtími fyrir innheimtubréf 2 og hærri er miðaður við þá dagsetningu sem fyrri innheimtubréfið er bókað eða prentað, eftir því hvað var valið í svæðinu Uppfærslu kóða innheimtubréfs á síðunni Færibreytur viðskiptakrafna.</span><span class="sxs-lookup"><span data-stu-id="ca506-132">⦁ The grace period for collection letters 2 and higher is relative to the date that the previous collection letter is posted or printed, depending on the selection in the Update collection letter code field in the Accounts receivable parameters page.</span></span>  
16. <span data-ttu-id="ca506-133">Smella á bæta Við til að bæta við síðasta innheimtubréfs í röðinni.</span><span class="sxs-lookup"><span data-stu-id="ca506-133">Click Add to add the last collection letter in the sequence.</span></span>
    * <span data-ttu-id="ca506-134">Hægt er að bæta við allt að fimm kóðum innheimtubréfs fyrir röð innheimtubréfs.</span><span class="sxs-lookup"><span data-stu-id="ca506-134">You can add up to five collection letter codes for a collection letter sequence.</span></span>  
17. <span data-ttu-id="ca506-135">Í svæðinu kóði innheimtubréfs , veljið næsta innheimtubréf sem verða sendar í röðinni.</span><span class="sxs-lookup"><span data-stu-id="ca506-135">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
18. <span data-ttu-id="ca506-136">Í reitinn Lýsing skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ca506-136">In the Description field, type a value.</span></span>
19. <span data-ttu-id="ca506-137">Í reitnum aðallykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ca506-137">In the Main account field, specify the desired values.</span></span>
20. <span data-ttu-id="ca506-138">Færið inn tölu í svæðinu Þóknun í gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="ca506-138">In the Fee in currency field, enter a number.</span></span>
21. <span data-ttu-id="ca506-139">Í reitnum VSK-flokkur vöru skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="ca506-139">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="ca506-140">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="ca506-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="ca506-141">Færið inn tölu í svæðinu Lágmarks gjaldfallna stöðu.</span><span class="sxs-lookup"><span data-stu-id="ca506-141">In the Minimum overdue balance field, enter a number.</span></span>
24. <span data-ttu-id="ca506-142">Í reitinn dagar skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="ca506-142">In the Days field, enter a number.</span></span>
25. <span data-ttu-id="ca506-143">Skal velja þennan gátreitur í stöðva viðskiptamaðurinn frá frekari afhendingum og reikningsfærsla.</span><span class="sxs-lookup"><span data-stu-id="ca506-143">Select this check box to stop the customer from additional deliveries and invoicing.</span></span>
    * <span data-ttu-id="ca506-144">Veljið Nei í Reikningsfærsla og afhending í bið svæðið á síðunni Viðskiptavinir til að opna fyrir lykilinn.</span><span class="sxs-lookup"><span data-stu-id="ca506-144">To unblock the account, select No in the Invoicing and delivery on hold field in the Customers page.</span></span>  
26. <span data-ttu-id="ca506-145">Útvíkka hlutann Athugasemd.</span><span class="sxs-lookup"><span data-stu-id="ca506-145">Expand the Note fasttab.</span></span>
27. <span data-ttu-id="ca506-146">Færið inn textann sem birtist innheimtubréfinu fyrir valda innheimtubréfakóða.</span><span class="sxs-lookup"><span data-stu-id="ca506-146">Enter the text to appear on the collection letter for the selected collection letter code.</span></span>
    * <span data-ttu-id="ca506-147">Hægt er að þýða þennan texta í á mörgum tungumálum með því að nota valmyndina Þýðingar yfir víxilkassanum.</span><span class="sxs-lookup"><span data-stu-id="ca506-147">You can translate this text in to multiple languages using the Translations menu above the note box.</span></span>  


