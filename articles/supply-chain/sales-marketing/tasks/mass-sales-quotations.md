---
title: Stofna fjölda sölutilboða
description: Þetta ferli sýnir hvernig stofna á hagkvæman hátt tilboð og bjóða úrval af vörum eða þjónustu sem á að senda mörg viðskiptavinum.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dcf216c65514820dc50486266a79ad1b4d696db3
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835527"
---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="ddaa6-103">Stofna fjölda sölutilboða</span><span class="sxs-lookup"><span data-stu-id="ddaa6-103">Mass create sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ddaa6-104">Þetta ferli sýnir hvernig stofna á hagkvæman hátt tilboð og bjóða úrval af vörum eða þjónustu sem á að senda mörg viðskiptavinum.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="ddaa6-105">Stofnun margra tilboða er byggt á tilboðssniðmát.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="ddaa6-106">Hægt er að keyra þetta ferli á eigin gögn eða í sýnigögn USMF fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="ddaa6-107">Stofna a sniðmát tilboðs</span><span class="sxs-lookup"><span data-stu-id="ddaa6-107">Create a quotation template</span></span>
1. <span data-ttu-id="ddaa6-108">Fara í Sölu og markaðssetningu > Uppsetning > Tilboð > Sniðmátsflokka.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="ddaa6-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-109">Click New.</span></span>
3. <span data-ttu-id="ddaa6-110">Rita Kenni að eigin vali í svæðinu Flokkskenni.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="ddaa6-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ddaa6-112">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-112">Click Save.</span></span>
6. <span data-ttu-id="ddaa6-113">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-113">Close the page.</span></span>
7. <span data-ttu-id="ddaa6-114">Fara í Sölu og markaðssetningu > Sölutilboð > Öll tilboð.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="ddaa6-115">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-115">Click New.</span></span>
9. <span data-ttu-id="ddaa6-116">Veljið „Viðskiptavinur“ á svæðinu „Gerð lykils“.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="ddaa6-117">Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="ddaa6-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-118">Click OK.</span></span>
    * <span data-ttu-id="ddaa6-119">Fyrir tilboð að verða sniðmát verður að framkvæma uppsetningu skref í tilboðshausnum.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="ddaa6-120">Það verður gert áður en línum er bætt við tilboðið.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="ddaa6-121">Í aðgerðasvæðinu er smellt á valkostir.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="ddaa6-122">Smellið á skoða Breytingu.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-122">Click Change view.</span></span>
14. <span data-ttu-id="ddaa6-123">Smellið á skoða Haus.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-123">Click Header view.</span></span>
15. <span data-ttu-id="ddaa6-124">Víkka út hlutann Uppsetning.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="ddaa6-125">Í reitinn kenni hóps skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="ddaa6-126">Í reitinn Heiti sniðmáts skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="ddaa6-127">Velja skal Já í Virka svæðinu.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="ddaa6-128">Hægt er að nota aðeins virk sniðmát þegar sniðmátsuppskrift er beitt í nýja sölutilboðið.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="ddaa6-129">Í aðgerðasvæðinu er smellt á valkostir.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="ddaa6-130">Smellið á skoða Breytingu.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-130">Click Change view.</span></span>
21. <span data-ttu-id="ddaa6-131">Smellið á Línuyfirlit.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-131">Click Line view.</span></span>
22. <span data-ttu-id="ddaa6-132">Í reitinn vara skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="ddaa6-133">Í reitinn vara skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="ddaa6-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-134">Close the page.</span></span>
25. <span data-ttu-id="ddaa6-135">Færið inn tölu í svæðinu afsláttarprósenta.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="ddaa6-136">Smella á bæta Við línu.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-136">Click Add line.</span></span>
27. <span data-ttu-id="ddaa6-137">Í reitinn vara skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="ddaa6-138">Í reitinn vara skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="ddaa6-139">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-139">Close the page.</span></span>
30. <span data-ttu-id="ddaa6-140">Færa inn nýtt verð eða breyta gildandi í svæðinu einingarverð.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="ddaa6-141">Smella á bæta Við línu.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-141">Click Add line.</span></span>
32. <span data-ttu-id="ddaa6-142">Í reitinn vara skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="ddaa6-143">Í reitinn vara skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="ddaa6-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-144">Close the page.</span></span>
35. <span data-ttu-id="ddaa6-145">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="ddaa6-146">Í reitinn afsláttur skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="ddaa6-147">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="ddaa6-148">Nota sniðmát til að stofna eitt tilboð</span><span class="sxs-lookup"><span data-stu-id="ddaa6-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="ddaa6-149">Fara í Sölu og markaðssetningu > Sölutilboð > Öll tilboð.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="ddaa6-150">Athugið að tilboð sem þú varst að stofna er merkt sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="ddaa6-151">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-151">Click New.</span></span>
3. <span data-ttu-id="ddaa6-152">Veljið „Viðskiptavinur“ á svæðinu „Gerð lykils“.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="ddaa6-153">Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="ddaa6-154">Stækkaðu hlutann Sniðmát.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-154">Expand the Template section.</span></span>
6. <span data-ttu-id="ddaa6-155">Í reitinn kenni hóps skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="ddaa6-156">Sláið inn eða veldu gildi í reitnum heiti sniðmáts.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="ddaa6-157">Veljið í svæðinu útreikningsaðferð 'Byggt á sniðmátsgildum'.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="ddaa6-158">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-158">Click OK.</span></span>
    * <span data-ttu-id="ddaa6-159">Nýtt tilboð hefur nú verið stofnað, byggt á gögnum og skilmála sniðmátsins.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="ddaa6-160">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-160">Close the page.</span></span>
11. <span data-ttu-id="ddaa6-161">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="ddaa6-162">Nota sniðmát til að stofna fjölda tilboða</span><span class="sxs-lookup"><span data-stu-id="ddaa6-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="ddaa6-163">Fara í Sölu og markaðssetningu > Sölutilboð > Uppfærsla tilboðs > Stofna fjölda tilboða.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="ddaa6-164">Veljið „Viðskiptavinur“ á svæðinu „Gerð lykils“.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="ddaa6-165">Í reitinn kenni hóps skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="ddaa6-166">Sláið inn eða veldu gildi í reitnum heiti sniðmáts.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="ddaa6-167">Veljið í svæðinu útreikningsaðferð 'Byggt á sniðmátsgildum'.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="ddaa6-168">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="ddaa6-169">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-169">Click Filter.</span></span>
8. <span data-ttu-id="ddaa6-170">í svæðinu Skilyrði, Stilla síu til að ná yfir svið viðskiptavina sem á að taka með í þetta stofnun fjöldatilboðs.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="ddaa6-171">Notaðu eftirfarandi snið „Viðskiptavinur1... ViðskiptavinurN.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="ddaa6-172">Til dæmis væri hægt að setja síu: US-001..US-004</span><span class="sxs-lookup"><span data-stu-id="ddaa6-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="ddaa6-173">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-173">Click OK.</span></span>
10. <span data-ttu-id="ddaa6-174">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-174">Click OK.</span></span>
11. <span data-ttu-id="ddaa6-175">Fara í Sölu og markaðssetningu > Sölutilboð > Öll tilboð.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="ddaa6-176">Staðfestið að tilboð hafa verið stofnaðar fyrir alla viðskiptavini sem eru tilgreind í fjöldauppfærslu, sem byggist á völdu sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="ddaa6-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  

