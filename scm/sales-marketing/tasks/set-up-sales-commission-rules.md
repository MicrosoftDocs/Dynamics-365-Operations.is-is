--- 
title: "Setja upp reglur söluþóknunar"
description: "Þessi verklýsing sýnir hvernig á að setja upp og virkja útreikning á sölulaunum og rakningu."
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
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 0ab5b3b5447e56eb8ed012a67454400cb2357af4
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="set-up-sales-commission-rules"></a><span data-ttu-id="800bf-103">Setja upp reglur söluþóknunar</span><span class="sxs-lookup"><span data-stu-id="800bf-103">Set up sales commission rules</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="800bf-104">Þessi verklýsing sýnir hvernig á að setja upp og virkja útreikning á sölulaunum og rakningu.</span><span class="sxs-lookup"><span data-stu-id="800bf-104">This procedure shows you how to set up and enable sales commission calculation and tracking.</span></span> <span data-ttu-id="800bf-105">Ferlið sýnir hvernig á að stofna bæði sölulaunaflokka viðskiptavina og vöru og svo hvernig á að tengja við valinn viðskiptavin og afurð viðkomandi flokka.</span><span class="sxs-lookup"><span data-stu-id="800bf-105">The procedure shows how to create both customer and item commission groups, and then how to link a selected customer and product to the respective groups.</span></span> <span data-ttu-id="800bf-106">Þessir flokkar eru síðan notaðir í uppsetningu á útreikningi þóknunar til að stofna samsetningu viðskiptavinar, vöru og sölufulltrúa sem jafna verður við sölupöntun til að heimila sölufulltrúum að fá þóknun.</span><span class="sxs-lookup"><span data-stu-id="800bf-106">Those groups are then used in the commission calculation setup to create a customer, item, and sales representatives combination that must be matched by the sales order to entitle the sales people to a commission.</span></span> <span data-ttu-id="800bf-107">Valfrjálst er að stofna sölulaunaflokk viðskiptavinar og vöru, þar sem einnig er hægt að reikna þóknun fyrir stakan viðskiptavin og/eða vöru.</span><span class="sxs-lookup"><span data-stu-id="800bf-107">Creating customer and item commission groups are optional, as the calculation of commission can also be done for an individual customer and/or item.</span></span> <span data-ttu-id="800bf-108">Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.</span><span class="sxs-lookup"><span data-stu-id="800bf-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-commission-groups-and-commission-rates"></a><span data-ttu-id="800bf-109">Setja upp þóknunarflokka og umboðslaunataxta</span><span class="sxs-lookup"><span data-stu-id="800bf-109">Set up commission groups and commission rates</span></span>
1. <span data-ttu-id="800bf-110">Fara í Sölu og markaðssetningu > Þóknanir > Viðskiptavinaflokkar þóknunar.</span><span class="sxs-lookup"><span data-stu-id="800bf-110">Go to Sales and marketing > Commissions > Customer groups for commission.</span></span>
2. <span data-ttu-id="800bf-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="800bf-111">Click New.</span></span>
3. <span data-ttu-id="800bf-112">Í reitinn Hópur skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="800bf-112">In the Group field, type a value.</span></span>
4. <span data-ttu-id="800bf-113">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="800bf-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="800bf-114">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="800bf-114">Click Save.</span></span>
6. <span data-ttu-id="800bf-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="800bf-115">Close the page.</span></span>
7. <span data-ttu-id="800bf-116">Fara í Sölu og markaðssetningu > Þóknanir > Vöruflokkar.</span><span class="sxs-lookup"><span data-stu-id="800bf-116">Go to Sales and marketing > Commissions > Item groups.</span></span>
8. <span data-ttu-id="800bf-117">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="800bf-117">Click New.</span></span>
9. <span data-ttu-id="800bf-118">Í reitinn Hópur skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="800bf-118">In the Group field, type a value.</span></span>
10. <span data-ttu-id="800bf-119">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="800bf-119">In the Name field, type a value.</span></span>
11. <span data-ttu-id="800bf-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="800bf-120">Close the page.</span></span>
12. <span data-ttu-id="800bf-121">Fara í Sölu og markaðssetningu > Þóknanir > Söluflokkar.</span><span class="sxs-lookup"><span data-stu-id="800bf-121">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="800bf-122">Söluflokkur Þóknunar tilgreinir starfsmenn í hlutverki sölufulltrúa sem eru hæfir til að fá þóknun þegar viðskiptavinur tengdur viðeigandi söluflokk kaupir tilteknar vörur.</span><span class="sxs-lookup"><span data-stu-id="800bf-122">A Commission sales group specifies the employees in sales representative roles who are eligible to receive a commission when a customer associated with the relevant sales group buys certain items.</span></span>  
    * <span data-ttu-id="800bf-123">Í sýnifyrirtækinu USMF er söluflokkur sem heitir „Sölufulltrúar US“.</span><span class="sxs-lookup"><span data-stu-id="800bf-123">In the USMF demo data company, there is a sales group called "Sales reps US."</span></span>  
13. <span data-ttu-id="800bf-124">Smellið á „Almennt“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="800bf-124">On the Action Pane, click General.</span></span>
14. <span data-ttu-id="800bf-125">Smellt er á Sölufulltrúa...</span><span class="sxs-lookup"><span data-stu-id="800bf-125">Click Sales rep..</span></span>
    * <span data-ttu-id="800bf-126">Sölufulltrúinn</span><span class="sxs-lookup"><span data-stu-id="800bf-126">The Sales rep.</span></span> <span data-ttu-id="800bf-127">síðan birtir lista yfir sölumenn fyrirtækisins sem eru tengdar við tiltekinn þóknunarflokk.</span><span class="sxs-lookup"><span data-stu-id="800bf-127">page displays a list of the company's sales people who are associated with a specific commission group.</span></span> <span data-ttu-id="800bf-128">Hægt er að úthluta mörgum sölufulltrúum á sama flokk og skilgreina viðkomandi hluta þeirra í heildarþóknun sem prósentugildi.</span><span class="sxs-lookup"><span data-stu-id="800bf-128">You can assign multiple sales representatives to the same group and define their respective share of the total commission fee as a percentage value.</span></span> <span data-ttu-id="800bf-129">Heildarþóknunarhluti yfir alla starfsmenn má ekki fara yfir 100.</span><span class="sxs-lookup"><span data-stu-id="800bf-129">The total commission share across all employees must not exceed 100.</span></span>  
15. <span data-ttu-id="800bf-130">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="800bf-130">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="800bf-131">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="800bf-131">Click Edit.</span></span>
17. <span data-ttu-id="800bf-132">Stilla þóknunarhluti á '50'.</span><span class="sxs-lookup"><span data-stu-id="800bf-132">Set Commission share to '50'.</span></span>
18. <span data-ttu-id="800bf-133">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="800bf-133">Click New.</span></span>
19. <span data-ttu-id="800bf-134">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="800bf-134">In the Name field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="800bf-135">Nota Síu á Flýtiræsistikunni til að leita að færslum.</span><span class="sxs-lookup"><span data-stu-id="800bf-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="800bf-136">Til dæmis, sía svæðið Heiti með gildinu 'Susan Burk'.</span><span class="sxs-lookup"><span data-stu-id="800bf-136">For example, filter on the Name field with a value of 'Susan Burk'.</span></span>
21. <span data-ttu-id="800bf-137">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="800bf-137">Click Select.</span></span>
22. <span data-ttu-id="800bf-138">Stilla þóknunarhluti á '50'.</span><span class="sxs-lookup"><span data-stu-id="800bf-138">Set Commission share to '50'.</span></span>
23. <span data-ttu-id="800bf-139">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="800bf-139">Click Save.</span></span>
24. <span data-ttu-id="800bf-140">Fara í Sölu og markaðssetningu > Þóknanir > Útreikningur þóknunar.</span><span class="sxs-lookup"><span data-stu-id="800bf-140">Go to Sales and marketing > Commissions > Commission calculation.</span></span>
    * <span data-ttu-id="800bf-141">Á síðunni Útreikningur á þóknun skilgreinirðu umboðslaunataxta sem starfsmaðurinn á að fá sölufærslu fyrir þegar hún inniheldur fyrirframstillta samsetningu viðskiptavinar og vöru.</span><span class="sxs-lookup"><span data-stu-id="800bf-141">In the Commission calculation page you define the commission rate that the employee is to receive for a sales transaction when it contains the pre-set combination of customer and product.</span></span> <span data-ttu-id="800bf-142">Sem hluti af uppsetningu umboðslaunataxta verður að tilgreina grundvöll fyrir útreikning þóknunar og hvort hún eigi að taka með eða útiloka afslætti.</span><span class="sxs-lookup"><span data-stu-id="800bf-142">As part of the commission rate setup, you must specify the commission calculation basis and whether it should include or exclude discounts.</span></span> <span data-ttu-id="800bf-143">Hægt er að færa inn gildistímabil þegar umboðslaunataxti er virkur.</span><span class="sxs-lookup"><span data-stu-id="800bf-143">You can also enter a validity period for when the commission rate is active.</span></span>  
25. <span data-ttu-id="800bf-144">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="800bf-144">Click New.</span></span>
26. <span data-ttu-id="800bf-145">Í reitnum vörukóði er valið 'flokkur'.</span><span class="sxs-lookup"><span data-stu-id="800bf-145">In the Item code field, select 'Group'.</span></span>
27. <span data-ttu-id="800bf-146">Í reitnum Vöruvensl skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="800bf-146">In the Item relation field, click the drop-down button to open the lookup.</span></span>
28. <span data-ttu-id="800bf-147">Í listanum finnurðu og velur flokk sem þú stofnaðir áður.</span><span class="sxs-lookup"><span data-stu-id="800bf-147">In the list, find and select the group that you created earlier.</span></span>
29. <span data-ttu-id="800bf-148">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="800bf-148">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="800bf-149">Í reitnum Viðskiptavinakóði er valið „Flokkur“.</span><span class="sxs-lookup"><span data-stu-id="800bf-149">In the Customer code field, select 'Group'.</span></span>
31. <span data-ttu-id="800bf-150">Í reitnum Tengsl viðskiptavina skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="800bf-150">In the Customer relation field, click the drop-down button to open the lookup.</span></span>
32. <span data-ttu-id="800bf-151">Á listanum velurðu flokkinn sem áður var settur upp.</span><span class="sxs-lookup"><span data-stu-id="800bf-151">In the list, select the group that you set up earlier.</span></span>
33. <span data-ttu-id="800bf-152">Í Sölufulltrúa</span><span class="sxs-lookup"><span data-stu-id="800bf-152">In the Sales rep.</span></span> <span data-ttu-id="800bf-153">í reitnum Tengsl skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="800bf-153">relation field, click the drop-down button to open the lookup.</span></span>
34. <span data-ttu-id="800bf-154">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="800bf-154">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="800bf-155">Halda valkosturinn „Fyrir línuafslátt".</span><span class="sxs-lookup"><span data-stu-id="800bf-155">Keep the "Before line discount" option.</span></span>  
    * <span data-ttu-id="800bf-156">Halda valkosturinn "Tekjur" sem grunni fyrir útreikning á þóknana gildi.</span><span class="sxs-lookup"><span data-stu-id="800bf-156">Keep the "Revenue" option as the basis for commission value calculation.</span></span>    
35. <span data-ttu-id="800bf-157">Færið inn tölu í reitinn þóknunarprósenta.</span><span class="sxs-lookup"><span data-stu-id="800bf-157">In the Commission percentage field, enter a number.</span></span>
36. <span data-ttu-id="800bf-158">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="800bf-158">Click Save.</span></span>

## <a name="setting-up-commission-posting"></a><span data-ttu-id="800bf-159">Uppsetning á þóknunarbókun</span><span class="sxs-lookup"><span data-stu-id="800bf-159">Setting up commission posting</span></span>
1. <span data-ttu-id="800bf-160">Fara í Sölu og markaðssetningu > Þóknanir > Bókun þóknunar.</span><span class="sxs-lookup"><span data-stu-id="800bf-160">Go to Sales and marketing > Commissions > Commission posting.</span></span>
    * <span data-ttu-id="800bf-161">Þóknun er greiðsla til starfsmanna og hana verður því að setja upp til að tryggja rétta fjárhagsbókun á viðeigandi lykla í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="800bf-161">Commission fees are payable to the employees and must therefore be set up to ensure correct financial posting to the appropriate accounts in the General ledger.</span></span> <span data-ttu-id="800bf-162">Þetta er gert á bókunarsíðu Þóknunar.</span><span class="sxs-lookup"><span data-stu-id="800bf-162">This is done in the Commission posting page.</span></span> <span data-ttu-id="800bf-163">Endurskoða uppsetningu sem er tiltæk fyrir gildandi fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="800bf-163">Review the setup that is available for the current company.</span></span> <span data-ttu-id="800bf-164">Yfirleitt eru upphæðir þóknunar bókaðar á sérstakan kostnaðarlykil og jafnaðar við sérstakan reikning lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="800bf-164">Typically, the commission amounts are posted to a dedicated expense account and are offset to a dedicated payable account.</span></span> <span data-ttu-id="800bf-165">Ef ekki er búið að setja upp bókunarreglur þóknunar mun kerfinu ekki takast að ljúka reikningsfærslu sölupöntunarinnar sem er með hæfar þóknanir.</span><span class="sxs-lookup"><span data-stu-id="800bf-165">If you don't have the commission posting rules set up, the system will fail to complete invoicing of a sales order which has eligible commissions.</span></span>  
2. <span data-ttu-id="800bf-166">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="800bf-166">Close the page.</span></span>

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a><span data-ttu-id="800bf-167">Úthluta þóknunarflokki á viðskiptavin og afurð</span><span class="sxs-lookup"><span data-stu-id="800bf-167">Assign a commission group to a customer and a product</span></span>
1. <span data-ttu-id="800bf-168">Fara í Sölu og markaðssetningu > Viðskiptavinir > Allir viðskiptavinir.</span><span class="sxs-lookup"><span data-stu-id="800bf-168">Go to Sales and marketing > Customers > All customers.</span></span>
2. <span data-ttu-id="800bf-169">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="800bf-169">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="800bf-170">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="800bf-170">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="800bf-171">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="800bf-171">Click Edit.</span></span>
5. <span data-ttu-id="800bf-172">Útvíkka hlutann Sjálfgildi sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="800bf-172">Expand the Sales order defaults section.</span></span>
6. <span data-ttu-id="800bf-173">Í reitnum Sölulaunaflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="800bf-173">In the Commission group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="800bf-174">Á listanum velurðu flokkinn sem þú stofnaðir áður.</span><span class="sxs-lookup"><span data-stu-id="800bf-174">In the list, select the group that you created earlier.</span></span>
8. <span data-ttu-id="800bf-175">Í reitnum Söluflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="800bf-175">In the Sales group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="800bf-176">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="800bf-176">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="800bf-177">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="800bf-177">Click Save.</span></span>
11. <span data-ttu-id="800bf-178">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="800bf-178">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="800bf-179">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="800bf-179">Use the Quick Filter to find records.</span></span> <span data-ttu-id="800bf-180">Til dæmis, sía svæðið Vara með gildinu 'T0020'.</span><span class="sxs-lookup"><span data-stu-id="800bf-180">For example, filter on the Item number field with a value of 'T0020 '.</span></span>
13. <span data-ttu-id="800bf-181">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="800bf-181">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="800bf-182">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="800bf-182">Click Edit.</span></span>
15. <span data-ttu-id="800bf-183">Útvíkka hlutann Selja.</span><span class="sxs-lookup"><span data-stu-id="800bf-183">Expand the Sell section.</span></span>
16. <span data-ttu-id="800bf-184">Í reitnum Sölulaunaflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="800bf-184">In the Commission group field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="800bf-185">Á listanum velurðu þóknunarflokk sem þú stofnaðir áður.</span><span class="sxs-lookup"><span data-stu-id="800bf-185">In the list, select the commission group that you created earlier.</span></span>


