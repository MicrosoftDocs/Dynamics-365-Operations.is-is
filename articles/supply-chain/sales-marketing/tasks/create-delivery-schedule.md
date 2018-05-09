--- 
title: "Stofna afhendingaráætlun"
description: "Þetta ferli sýnir hvernig á að stofna afhendingaráætlun fyrir sölupöntun."
author: omulvad
manager: AnnBe
ms.date: 02/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 407337d31e0aa68217a27a5709da16ddc7d6e4a1
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-delivery-schedule"></a><span data-ttu-id="a6a8a-103">Stofna afhendingaráætlun</span><span class="sxs-lookup"><span data-stu-id="a6a8a-103">Create a delivery schedule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a6a8a-104">Þetta ferli sýnir hvernig á að stofna afhendingaráætlun fyrir sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-104">This procedure demonstrates how to create a delivery schedule for a sales order.</span></span> <span data-ttu-id="a6a8a-105">Afhendingaráætlun er notaður þegar magn í pöntun beðið er um að afhenda í margar sendingar.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-105">A delivery schedule is used when a quantity on an order or a quotation is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="a6a8a-106">Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-delivery-schedule"></a><span data-ttu-id="a6a8a-107">Stofna afhendingaráætlun</span><span class="sxs-lookup"><span data-stu-id="a6a8a-107">Create delivery schedule</span></span>
1. <span data-ttu-id="a6a8a-108">Fara í Allar sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-108">Go to All sales orders.</span></span>
2. <span data-ttu-id="a6a8a-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-109">Click New.</span></span>
3. <span data-ttu-id="a6a8a-110">Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-110">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="a6a8a-111">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-111">Click OK.</span></span>
5. <span data-ttu-id="a6a8a-112">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-112">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="a6a8a-113">Í reitinn magn skal slá inn númer sem er stærra en 1</span><span class="sxs-lookup"><span data-stu-id="a6a8a-113">In the Quantity field, enter a number that is bigger than 1.</span></span>
7. <span data-ttu-id="a6a8a-114">Smellið á „Sölupöntunarlína“.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-114">Click Sales order line.</span></span>
8. <span data-ttu-id="a6a8a-115">Smellið á „Afhendingaráætlun“.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-115">Click Delivery schedule.</span></span>
    * <span data-ttu-id="a6a8a-116">Síðan Afhendingaráætlun er staðurinn þar sem hægt er að tilgreina fjölda sendinga þar sem heildarmagn pöntunarlínu verða afhentar viðskiptavininum.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-116">The Delivery schedule page is the place where you can specify the number of shipments in which the total quantity of the order line will be delivered to the customer.</span></span>    
    * <span data-ttu-id="a6a8a-117">Að sjálfgefnu kerfið afritar heildarmagn og aðrar upplýsingar um afhendingu á upprunalegri sölulínu í fyrstu afhendingaráætlunarlínu.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-117">By default, the system copies the total quantity and other delivery details of the original sales line into the first delivery schedule line.</span></span> <span data-ttu-id="a6a8a-118">Í þessu dæmi stofnum við áætlun fyrir tvær sendingar og sendingardagsetningin er stillt viku eftir þá fyrstu.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-118">In this example, we’ll create a schedule for two shipments, with the second shipment's date offset by a week from the first one.</span></span>  
9. <span data-ttu-id="a6a8a-119">Í reitinn magn skal slá inn númer sem er hluti af heildarmagni</span><span class="sxs-lookup"><span data-stu-id="a6a8a-119">In the Quantity field, enter a number that is part of the total quantity.</span></span>
10. <span data-ttu-id="a6a8a-120">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-120">Click New.</span></span>
11. <span data-ttu-id="a6a8a-121">Í reitnum Magn skal slá inn eftirstandandi magn.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-121">In the Quantity field, enter the remaining quantity.</span></span>
12. <span data-ttu-id="a6a8a-122">Í reitnum Umbeðinni sendingardagsetningu skal færa inn dagsetningu sem er eina viku á undan dagsetningu fyrstu afhendingarlínu.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-122">In the Requested ship date field, enter a date a date that is one week ahead from the date of the first delivery line.</span></span>
    * <span data-ttu-id="a6a8a-123">Tveir valmöguleikar á flýtiflipanum Gjöld fyrir umreikning stýrir hvernig á að dreifa á milli afhendingar á að raða línum þegar þeim hefur verið búið að úthluta upprunalegu pöntunarlínunni.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-123">The two options on the Charges conversion FastTab control how you want the charges to be distributed across the delivery schedule lines, once they’ve been assigned to the original order line.</span></span> <span data-ttu-id="a6a8a-124">Ef valið er Afrita brúttóupphæðir, er sömu upphæð gjalda afritað í hverja línu.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-124">If you select Copy gross amounts, the same charge amount is copied to each line.</span></span> <span data-ttu-id="a6a8a-125">Valkosturinn Úthlutun á afhendingarlínur skiptir gjöld jafnt yfir í afhendingarlínur.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-125">The Allocate to delivery lines option divides the charge equally across the delivery lines.</span></span>  
    * <span data-ttu-id="a6a8a-126">Aðeins föst gjöld hægt er að skipta niður, en enn verða afritaðar breytileg gjöld í línur.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-126">Only fixed charges can be divided, whereas variable charges will still be copied to the lines.</span></span>  
13. <span data-ttu-id="a6a8a-127">Færðu Bendillinn frá önnur afhendingarlína til að uppfæra síðu.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-127">Move the cursor away from the second delivery line to update the page.</span></span>
    * <span data-ttu-id="a6a8a-128">Þú getur fylgst með heildarmagn sem úthlutað er til í línur afhendingaráætlunar með því að líta á svæðin Samtölu og Eftirstandandi.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-128">You can keep track of the total quantity that’s allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="a6a8a-129">Þegar eftirstöðvar magns eru núll, allt magnið í upphaflegu línunni hefur verið úthlutað á áætlun.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-129">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>   
14. <span data-ttu-id="a6a8a-130">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-130">Click OK.</span></span>
    * <span data-ttu-id="a6a8a-131">Afhendingaráætlunin hefur nú verið afrituð í pöntunarlínurnar.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-131">The delivery schedule has now been copied to the order lines.</span></span>   
    * <span data-ttu-id="a6a8a-132">Upprunalegri pöntunarlínunni, nefnt Heildarsöluverðmæti línu, hefur verið breytt í pöntunarlínu með margar afhendingar.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-132">The original order line, referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="a6a8a-133">Hún er merkt með áberandi tákni og þjónar sem haus fyrir afhendingarlínur.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-133">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
    * <span data-ttu-id="a6a8a-134">Hinar tvær nýju línurnar, sem nefndar eru afhendingarlínur, mynda í sameiningu eina afhendingaráætlun.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-134">The two new lines, referred to as delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="a6a8a-135">pöntunina verður unnin gegn þessum línum og ekki gagnvart upphaflegu línunni.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-135">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="a6a8a-136">Ef skjöl eins og staðfestingarseðlar, tiltektarlista, fylgiseðla eða reikninga eru prentaðar, eru eingöngu afhendingarlínur sýndar.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-136">If documents such as confirmation slips, picking lists, packing slips, or invoices are printed, only the delivery lines are shown.</span></span>   
    * <span data-ttu-id="a6a8a-137">Afhendingarlínur getur haft mismunandi afhendingardagsetningar, magn, afhendingarmáti og geymsluvíddir, eins og svæði og vöruhús.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-137">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span> <span data-ttu-id="a6a8a-138">Hins vegar afurðarvíddum alltaf verður að samsvara þeim sem eru á viðskiptalínu og ekki er hægt að breyta.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-138">However, the product dimensions must always match the ones on the commercial line and can't be changed.</span></span>  
15. <span data-ttu-id="a6a8a-139">Í reitinn magn skal slá inn númer sem er stærra en núverandi tala.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-139">In the Quantity field, enter a number that's bigger than the current one.</span></span>
16. <span data-ttu-id="a6a8a-140">Veljið viðskiptalínu til að sjá áhrifin endurútreiknings magns.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-140">Select the commercial line to see the effect of the quantity recalculation.</span></span>
17. <span data-ttu-id="a6a8a-141">Smellið á „Tiltekt og pökkun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-141">On the Action Pane, click Pick and pack.</span></span>
18. <span data-ttu-id="a6a8a-142">Smellt er á Bóka fylgiseðil.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-142">Click Post packing slip.</span></span>
19. <span data-ttu-id="a6a8a-143">Víkkið út færibreytuhlutann.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-143">Expand the Parameters section.</span></span>
20. <span data-ttu-id="a6a8a-144">Veljið „Allt“ á svæðinu „Magn“.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-144">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="a6a8a-145">Athugið að fylgiseðill verður stofnuð fyrir tvær línur afhendingaráætlunar og ekki upprunalegu pöntunarlínunni.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-145">Note that the packing slip will be created for the two delivery schedule lines and not the original order line.</span></span>  
21. <span data-ttu-id="a6a8a-146">Velja skal Já í svæðinu Prenta fylgiseðill.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-146">Select Yes in the Print packing slip field.</span></span>
22. <span data-ttu-id="a6a8a-147">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-147">Click OK.</span></span>
23. <span data-ttu-id="a6a8a-148">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-148">Click Yes.</span></span>
24. <span data-ttu-id="a6a8a-149">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a6a8a-149">Close the page.</span></span>


