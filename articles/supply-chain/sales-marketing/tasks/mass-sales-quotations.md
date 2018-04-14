--- 
title: "Stofna fjölda sölutilboða"
description: "Þetta ferli sýnir hvernig stofna á hagkvæman hátt tilboð og bjóða úrval af vörum eða þjónustu sem á að senda mörg viðskiptavinum."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 35b5f4078d3204c73048a3315b4aae9109d11251
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="9b81f-103">Stofna fjölda sölutilboða</span><span class="sxs-lookup"><span data-stu-id="9b81f-103">Mass create sales quotations</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9b81f-104">Þetta ferli sýnir hvernig stofna á hagkvæman hátt tilboð og bjóða úrval af vörum eða þjónustu sem á að senda mörg viðskiptavinum.</span><span class="sxs-lookup"><span data-stu-id="9b81f-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="9b81f-105">Stofnun margra tilboða er byggt á tilboðssniðmát.</span><span class="sxs-lookup"><span data-stu-id="9b81f-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="9b81f-106">Hægt er að keyra þetta ferli á eigin gögn eða í sýnigögn USMF fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="9b81f-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="9b81f-107">Stofna a sniðmát tilboðs</span><span class="sxs-lookup"><span data-stu-id="9b81f-107">Create a quotation template</span></span>
1. <span data-ttu-id="9b81f-108">Fara í Sölu og markaðssetningu > Uppsetning > Tilboð > Sniðmátsflokka.</span><span class="sxs-lookup"><span data-stu-id="9b81f-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="9b81f-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="9b81f-109">Click New.</span></span>
3. <span data-ttu-id="9b81f-110">Rita Kenni að eigin vali í svæðinu Flokkskenni.</span><span class="sxs-lookup"><span data-stu-id="9b81f-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="9b81f-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="9b81f-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9b81f-112">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9b81f-112">Click Save.</span></span>
6. <span data-ttu-id="9b81f-113">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9b81f-113">Close the page.</span></span>
7. <span data-ttu-id="9b81f-114">Fara í Sölu og markaðssetningu > Sölutilboð > Öll tilboð.</span><span class="sxs-lookup"><span data-stu-id="9b81f-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="9b81f-115">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="9b81f-115">Click New.</span></span>
9. <span data-ttu-id="9b81f-116">Veljið „Viðskiptavinur“ á svæðinu „Gerð lykils“.</span><span class="sxs-lookup"><span data-stu-id="9b81f-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="9b81f-117">Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="9b81f-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="9b81f-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9b81f-118">Click OK.</span></span>
    * <span data-ttu-id="9b81f-119">Fyrir tilboð að verða sniðmát verður að framkvæma uppsetningu skref í tilboðshausnum.</span><span class="sxs-lookup"><span data-stu-id="9b81f-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="9b81f-120">Það verður gert áður en línum er bætt við tilboðið.</span><span class="sxs-lookup"><span data-stu-id="9b81f-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="9b81f-121">Í aðgerðasvæðinu er smellt á valkostir.</span><span class="sxs-lookup"><span data-stu-id="9b81f-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="9b81f-122">Smellið á skoða Breytingu.</span><span class="sxs-lookup"><span data-stu-id="9b81f-122">Click Change view.</span></span>
14. <span data-ttu-id="9b81f-123">Smellið á skoða Haus.</span><span class="sxs-lookup"><span data-stu-id="9b81f-123">Click Header view.</span></span>
15. <span data-ttu-id="9b81f-124">Víkka út hlutann Uppsetning.</span><span class="sxs-lookup"><span data-stu-id="9b81f-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="9b81f-125">Í reitinn kenni hóps skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="9b81f-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="9b81f-126">Í reitinn Heiti sniðmáts skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9b81f-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="9b81f-127">Velja skal Já í Virka svæðinu.</span><span class="sxs-lookup"><span data-stu-id="9b81f-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="9b81f-128">Hægt er að nota aðeins virk sniðmát þegar sniðmátsuppskrift er beitt í nýja sölutilboðið.</span><span class="sxs-lookup"><span data-stu-id="9b81f-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="9b81f-129">Í aðgerðasvæðinu er smellt á valkostir.</span><span class="sxs-lookup"><span data-stu-id="9b81f-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="9b81f-130">Smellið á skoða Breytingu.</span><span class="sxs-lookup"><span data-stu-id="9b81f-130">Click Change view.</span></span>
21. <span data-ttu-id="9b81f-131">Smellið á Línuyfirlit.</span><span class="sxs-lookup"><span data-stu-id="9b81f-131">Click Line view.</span></span>
22. <span data-ttu-id="9b81f-132">Í reitinn vara skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="9b81f-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="9b81f-133">Í reitinn vara skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9b81f-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="9b81f-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9b81f-134">Close the page.</span></span>
25. <span data-ttu-id="9b81f-135">Færið inn tölu í svæðinu afsláttarprósenta.</span><span class="sxs-lookup"><span data-stu-id="9b81f-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="9b81f-136">Smella á bæta Við línu.</span><span class="sxs-lookup"><span data-stu-id="9b81f-136">Click Add line.</span></span>
27. <span data-ttu-id="9b81f-137">Í reitinn vara skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="9b81f-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="9b81f-138">Í reitinn vara skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9b81f-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="9b81f-139">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9b81f-139">Close the page.</span></span>
30. <span data-ttu-id="9b81f-140">Færa inn nýtt verð eða breyta gildandi í svæðinu einingarverð.</span><span class="sxs-lookup"><span data-stu-id="9b81f-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="9b81f-141">Smella á bæta Við línu.</span><span class="sxs-lookup"><span data-stu-id="9b81f-141">Click Add line.</span></span>
32. <span data-ttu-id="9b81f-142">Í reitinn vara skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="9b81f-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="9b81f-143">Í reitinn vara skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9b81f-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="9b81f-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9b81f-144">Close the page.</span></span>
35. <span data-ttu-id="9b81f-145">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="9b81f-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="9b81f-146">Í reitinn afsláttur skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="9b81f-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="9b81f-147">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9b81f-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="9b81f-148">Nota sniðmát til að stofna eitt tilboð</span><span class="sxs-lookup"><span data-stu-id="9b81f-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="9b81f-149">Fara í Sölu og markaðssetningu > Sölutilboð > Öll tilboð.</span><span class="sxs-lookup"><span data-stu-id="9b81f-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="9b81f-150">Athugið að tilboð sem þú varst að stofna er merkt sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="9b81f-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="9b81f-151">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="9b81f-151">Click New.</span></span>
3. <span data-ttu-id="9b81f-152">Veljið „Viðskiptavinur“ á svæðinu „Gerð lykils“.</span><span class="sxs-lookup"><span data-stu-id="9b81f-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="9b81f-153">Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="9b81f-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="9b81f-154">Stækkaðu hlutann Sniðmát.</span><span class="sxs-lookup"><span data-stu-id="9b81f-154">Expand the Template section.</span></span>
6. <span data-ttu-id="9b81f-155">Í reitinn kenni hóps skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="9b81f-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="9b81f-156">Sláið inn eða veldu gildi í reitnum heiti sniðmáts.</span><span class="sxs-lookup"><span data-stu-id="9b81f-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="9b81f-157">Veljið í svæðinu útreikningsaðferð 'Byggt á sniðmátsgildum'.</span><span class="sxs-lookup"><span data-stu-id="9b81f-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="9b81f-158">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9b81f-158">Click OK.</span></span>
    * <span data-ttu-id="9b81f-159">Nýtt tilboð hefur nú verið stofnað, byggt á gögnum og skilmála sniðmátsins.</span><span class="sxs-lookup"><span data-stu-id="9b81f-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="9b81f-160">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9b81f-160">Close the page.</span></span>
11. <span data-ttu-id="9b81f-161">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9b81f-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="9b81f-162">Nota sniðmát til að stofna fjölda tilboða</span><span class="sxs-lookup"><span data-stu-id="9b81f-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="9b81f-163">Fara í Sölu og markaðssetningu > Sölutilboð > Uppfærsla tilboðs > Stofna fjölda tilboða.</span><span class="sxs-lookup"><span data-stu-id="9b81f-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="9b81f-164">Veljið „Viðskiptavinur“ á svæðinu „Gerð lykils“.</span><span class="sxs-lookup"><span data-stu-id="9b81f-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="9b81f-165">Í reitinn kenni hóps skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="9b81f-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="9b81f-166">Sláið inn eða veldu gildi í reitnum heiti sniðmáts.</span><span class="sxs-lookup"><span data-stu-id="9b81f-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="9b81f-167">Veljið í svæðinu útreikningsaðferð 'Byggt á sniðmátsgildum'.</span><span class="sxs-lookup"><span data-stu-id="9b81f-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="9b81f-168">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="9b81f-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="9b81f-169">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="9b81f-169">Click Filter.</span></span>
8. <span data-ttu-id="9b81f-170">í svæðinu Skilyrði, Stilla síu til að ná yfir svið viðskiptavina sem á að taka með í þetta stofnun fjöldatilboðs.</span><span class="sxs-lookup"><span data-stu-id="9b81f-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="9b81f-171">Notaðu eftirfarandi snið „Viðskiptavinur1... ViðskiptavinurN.</span><span class="sxs-lookup"><span data-stu-id="9b81f-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="9b81f-172">Til dæmis væri hægt að setja síu: US-001..US-004</span><span class="sxs-lookup"><span data-stu-id="9b81f-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="9b81f-173">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9b81f-173">Click OK.</span></span>
10. <span data-ttu-id="9b81f-174">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9b81f-174">Click OK.</span></span>
11. <span data-ttu-id="9b81f-175">Fara í Sölu og markaðssetningu > Sölutilboð > Öll tilboð.</span><span class="sxs-lookup"><span data-stu-id="9b81f-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="9b81f-176">Staðfestið að tilboð hafa verið stofnaðar fyrir alla viðskiptavini sem eru tilgreind í fjöldauppfærslu, sem byggist á völdu sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="9b81f-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  


