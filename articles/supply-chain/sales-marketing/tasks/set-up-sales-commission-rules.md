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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8d81765884f741443d1c0f5b0cb8bc545945e1a1
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-sales-commission-rules"></a><span data-ttu-id="0abc2-103">Setja upp reglur söluþóknunar</span><span class="sxs-lookup"><span data-stu-id="0abc2-103">Set up sales commission rules</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0abc2-104">Þessi verklýsing sýnir hvernig á að setja upp og virkja útreikning á sölulaunum og rakningu.</span><span class="sxs-lookup"><span data-stu-id="0abc2-104">This procedure shows you how to set up and enable sales commission calculation and tracking.</span></span> <span data-ttu-id="0abc2-105">Ferlið sýnir hvernig á að stofna bæði sölulaunaflokka viðskiptavina og vöru og svo hvernig á að tengja við valinn viðskiptavin og afurð viðkomandi flokka.</span><span class="sxs-lookup"><span data-stu-id="0abc2-105">The procedure shows how to create both customer and item commission groups, and then how to link a selected customer and product to the respective groups.</span></span> <span data-ttu-id="0abc2-106">Þessir flokkar eru síðan notaðir í uppsetningu á útreikningi þóknunar til að stofna samsetningu viðskiptavinar, vöru og sölufulltrúa sem jafna verður við sölupöntun til að heimila sölufulltrúum að fá þóknun.</span><span class="sxs-lookup"><span data-stu-id="0abc2-106">Those groups are then used in the commission calculation setup to create a customer, item, and sales representatives combination that must be matched by the sales order to entitle the sales people to a commission.</span></span> <span data-ttu-id="0abc2-107">Valfrjálst er að stofna sölulaunaflokk viðskiptavinar og vöru, þar sem einnig er hægt að reikna þóknun fyrir stakan viðskiptavin og/eða vöru.</span><span class="sxs-lookup"><span data-stu-id="0abc2-107">Creating customer and item commission groups are optional, as the calculation of commission can also be done for an individual customer and/or item.</span></span> <span data-ttu-id="0abc2-108">Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.</span><span class="sxs-lookup"><span data-stu-id="0abc2-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-commission-groups-and-commission-rates"></a><span data-ttu-id="0abc2-109">Setja upp þóknunarflokka og umboðslaunataxta</span><span class="sxs-lookup"><span data-stu-id="0abc2-109">Set up commission groups and commission rates</span></span>
1. <span data-ttu-id="0abc2-110">Fara í Sölu og markaðssetningu > Þóknanir > Viðskiptavinaflokkar þóknunar.</span><span class="sxs-lookup"><span data-stu-id="0abc2-110">Go to Sales and marketing > Commissions > Customer groups for commission.</span></span>
2. <span data-ttu-id="0abc2-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="0abc2-111">Click New.</span></span>
3. <span data-ttu-id="0abc2-112">Í reitinn Hópur skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="0abc2-112">In the Group field, type a value.</span></span>
4. <span data-ttu-id="0abc2-113">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="0abc2-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0abc2-114">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="0abc2-114">Click Save.</span></span>
6. <span data-ttu-id="0abc2-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0abc2-115">Close the page.</span></span>
7. <span data-ttu-id="0abc2-116">Fara í Sölu og markaðssetningu > Þóknanir > Vöruflokkar.</span><span class="sxs-lookup"><span data-stu-id="0abc2-116">Go to Sales and marketing > Commissions > Item groups.</span></span>
8. <span data-ttu-id="0abc2-117">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="0abc2-117">Click New.</span></span>
9. <span data-ttu-id="0abc2-118">Í reitinn Hópur skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="0abc2-118">In the Group field, type a value.</span></span>
10. <span data-ttu-id="0abc2-119">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="0abc2-119">In the Name field, type a value.</span></span>
11. <span data-ttu-id="0abc2-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0abc2-120">Close the page.</span></span>
12. <span data-ttu-id="0abc2-121">Fara í Sölu og markaðssetningu > Þóknanir > Söluflokkar.</span><span class="sxs-lookup"><span data-stu-id="0abc2-121">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="0abc2-122">Söluflokkur Þóknunar tilgreinir starfsmenn í hlutverki sölufulltrúa sem eru hæfir til að fá þóknun þegar viðskiptavinur tengdur viðeigandi söluflokk kaupir tilteknar vörur.</span><span class="sxs-lookup"><span data-stu-id="0abc2-122">A Commission sales group specifies the employees in sales representative roles who are eligible to receive a commission when a customer associated with the relevant sales group buys certain items.</span></span>  
    * <span data-ttu-id="0abc2-123">Í sýnifyrirtækinu USMF er söluflokkur sem heitir „Sölufulltrúar US“.</span><span class="sxs-lookup"><span data-stu-id="0abc2-123">In the USMF demo data company, there is a sales group called "Sales reps US."</span></span>  
13. <span data-ttu-id="0abc2-124">Smellið á „Almennt“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="0abc2-124">On the Action Pane, click General.</span></span>
14. <span data-ttu-id="0abc2-125">Smellt er á Sölufulltrúa...</span><span class="sxs-lookup"><span data-stu-id="0abc2-125">Click Sales rep..</span></span>
    * <span data-ttu-id="0abc2-126">Síðan Sölufulltrúi sýnir lista yfir sölufulltrúa fyrirtækisins sem tengjast ákveðnum þóknunarflokki.</span><span class="sxs-lookup"><span data-stu-id="0abc2-126">The Sales rep. page displays a list of the company's sales people who are associated with a specific commission group.</span></span> <span data-ttu-id="0abc2-127">Hægt er að úthluta mörgum sölufulltrúum á sama flokk og skilgreina viðkomandi hluta þeirra í heildarþóknun sem prósentugildi.</span><span class="sxs-lookup"><span data-stu-id="0abc2-127">You can assign multiple sales representatives to the same group and define their respective share of the total commission fee as a percentage value.</span></span> <span data-ttu-id="0abc2-128">Heildarþóknunarhluti yfir alla starfsmenn má ekki fara yfir 100.</span><span class="sxs-lookup"><span data-stu-id="0abc2-128">The total commission share across all employees must not exceed 100.</span></span>  
15. <span data-ttu-id="0abc2-129">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="0abc2-129">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="0abc2-130">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="0abc2-130">Click Edit.</span></span>
17. <span data-ttu-id="0abc2-131">Stilla þóknunarhluti á '50'.</span><span class="sxs-lookup"><span data-stu-id="0abc2-131">Set Commission share to '50'.</span></span>
18. <span data-ttu-id="0abc2-132">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="0abc2-132">Click New.</span></span>
19. <span data-ttu-id="0abc2-133">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="0abc2-133">In the Name field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="0abc2-134">Nota Síu á Flýtiræsistikunni til að leita að færslum.</span><span class="sxs-lookup"><span data-stu-id="0abc2-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0abc2-135">Til dæmis, sía svæðið Heiti með gildinu 'Susan Burk'.</span><span class="sxs-lookup"><span data-stu-id="0abc2-135">For example, filter on the Name field with a value of 'Susan Burk'.</span></span>
21. <span data-ttu-id="0abc2-136">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="0abc2-136">Click Select.</span></span>
22. <span data-ttu-id="0abc2-137">Stilla þóknunarhluti á '50'.</span><span class="sxs-lookup"><span data-stu-id="0abc2-137">Set Commission share to '50'.</span></span>
23. <span data-ttu-id="0abc2-138">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="0abc2-138">Click Save.</span></span>
24. <span data-ttu-id="0abc2-139">Fara í Sölu og markaðssetningu > Þóknanir > Útreikningur þóknunar.</span><span class="sxs-lookup"><span data-stu-id="0abc2-139">Go to Sales and marketing > Commissions > Commission calculation.</span></span>
    * <span data-ttu-id="0abc2-140">Á síðunni Útreikningur á þóknun skilgreinirðu umboðslaunataxta sem starfsmaðurinn á að fá sölufærslu fyrir þegar hún inniheldur fyrirframstillta samsetningu viðskiptavinar og vöru.</span><span class="sxs-lookup"><span data-stu-id="0abc2-140">In the Commission calculation page you define the commission rate that the employee is to receive for a sales transaction when it contains the pre-set combination of customer and product.</span></span> <span data-ttu-id="0abc2-141">Sem hluti af uppsetningu umboðslaunataxta verður að tilgreina grundvöll fyrir útreikning þóknunar og hvort hún eigi að taka með eða útiloka afslætti.</span><span class="sxs-lookup"><span data-stu-id="0abc2-141">As part of the commission rate setup, you must specify the commission calculation basis and whether it should include or exclude discounts.</span></span> <span data-ttu-id="0abc2-142">Hægt er að færa inn gildistímabil þegar umboðslaunataxti er virkur.</span><span class="sxs-lookup"><span data-stu-id="0abc2-142">You can also enter a validity period for when the commission rate is active.</span></span>  
25. <span data-ttu-id="0abc2-143">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="0abc2-143">Click New.</span></span>
26. <span data-ttu-id="0abc2-144">Í reitnum vörukóði er valið 'flokkur'.</span><span class="sxs-lookup"><span data-stu-id="0abc2-144">In the Item code field, select 'Group'.</span></span>
27. <span data-ttu-id="0abc2-145">Í reitnum Vöruvensl skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="0abc2-145">In the Item relation field, click the drop-down button to open the lookup.</span></span>
28. <span data-ttu-id="0abc2-146">Í listanum finnurðu og velur flokk sem þú stofnaðir áður.</span><span class="sxs-lookup"><span data-stu-id="0abc2-146">In the list, find and select the group that you created earlier.</span></span>
29. <span data-ttu-id="0abc2-147">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0abc2-147">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="0abc2-148">Í reitnum Viðskiptavinakóði er valið „Flokkur“.</span><span class="sxs-lookup"><span data-stu-id="0abc2-148">In the Customer code field, select 'Group'.</span></span>
31. <span data-ttu-id="0abc2-149">Í reitnum Tengsl viðskiptavina skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="0abc2-149">In the Customer relation field, click the drop-down button to open the lookup.</span></span>
32. <span data-ttu-id="0abc2-150">Á listanum velurðu flokkinn sem áður var settur upp.</span><span class="sxs-lookup"><span data-stu-id="0abc2-150">In the list, select the group that you set up earlier.</span></span>
33. <span data-ttu-id="0abc2-151">Í Sölufulltrúa í reitnum Tengsl skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="0abc2-151">In the Sales rep. relation field, click the drop-down button to open the lookup.</span></span>
34. <span data-ttu-id="0abc2-152">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="0abc2-152">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0abc2-153">Halda valkosturinn „Fyrir línuafslátt".</span><span class="sxs-lookup"><span data-stu-id="0abc2-153">Keep the "Before line discount" option.</span></span>  
    * <span data-ttu-id="0abc2-154">Halda valkosturinn "Tekjur" sem grunni fyrir útreikning á þóknana gildi.</span><span class="sxs-lookup"><span data-stu-id="0abc2-154">Keep the "Revenue" option as the basis for commission value calculation.</span></span>    
35. <span data-ttu-id="0abc2-155">Færið inn tölu í reitinn þóknunarprósenta.</span><span class="sxs-lookup"><span data-stu-id="0abc2-155">In the Commission percentage field, enter a number.</span></span>
36. <span data-ttu-id="0abc2-156">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="0abc2-156">Click Save.</span></span>

## <a name="setting-up-commission-posting"></a><span data-ttu-id="0abc2-157">Uppsetning á þóknunarbókun</span><span class="sxs-lookup"><span data-stu-id="0abc2-157">Setting up commission posting</span></span>
1. <span data-ttu-id="0abc2-158">Fara í Sölu og markaðssetningu > Þóknanir > Bókun þóknunar.</span><span class="sxs-lookup"><span data-stu-id="0abc2-158">Go to Sales and marketing > Commissions > Commission posting.</span></span>
    * <span data-ttu-id="0abc2-159">Þóknun er greiðsla til starfsmanna og hana verður því að setja upp til að tryggja rétta fjárhagsbókun á viðeigandi lykla í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="0abc2-159">Commission fees are payable to the employees and must therefore be set up to ensure correct financial posting to the appropriate accounts in the General ledger.</span></span> <span data-ttu-id="0abc2-160">Þetta er gert á bókunarsíðu Þóknunar.</span><span class="sxs-lookup"><span data-stu-id="0abc2-160">This is done in the Commission posting page.</span></span> <span data-ttu-id="0abc2-161">Endurskoða uppsetningu sem er tiltæk fyrir gildandi fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="0abc2-161">Review the setup that is available for the current company.</span></span> <span data-ttu-id="0abc2-162">Yfirleitt eru upphæðir þóknunar bókaðar á sérstakan kostnaðarlykil og jafnaðar við sérstakan reikning lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="0abc2-162">Typically, the commission amounts are posted to a dedicated expense account and are offset to a dedicated payable account.</span></span> <span data-ttu-id="0abc2-163">Ef ekki er búið að setja upp bókunarreglur þóknunar mun kerfinu ekki takast að ljúka reikningsfærslu sölupöntunarinnar sem er með hæfar þóknanir.</span><span class="sxs-lookup"><span data-stu-id="0abc2-163">If you don't have the commission posting rules set up, the system will fail to complete invoicing of a sales order which has eligible commissions.</span></span>  
2. <span data-ttu-id="0abc2-164">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0abc2-164">Close the page.</span></span>

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a><span data-ttu-id="0abc2-165">Úthluta þóknunarflokki á viðskiptavin og afurð</span><span class="sxs-lookup"><span data-stu-id="0abc2-165">Assign a commission group to a customer and a product</span></span>
1. <span data-ttu-id="0abc2-166">Fara í Sölu og markaðssetningu > Viðskiptavinir > Allir viðskiptavinir.</span><span class="sxs-lookup"><span data-stu-id="0abc2-166">Go to Sales and marketing > Customers > All customers.</span></span>
2. <span data-ttu-id="0abc2-167">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="0abc2-167">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0abc2-168">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0abc2-168">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0abc2-169">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="0abc2-169">Click Edit.</span></span>
5. <span data-ttu-id="0abc2-170">Útvíkka hlutann Sjálfgildi sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="0abc2-170">Expand the Sales order defaults section.</span></span>
6. <span data-ttu-id="0abc2-171">Í reitnum Sölulaunaflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="0abc2-171">In the Commission group field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="0abc2-172">Á listanum velurðu flokkinn sem þú stofnaðir áður.</span><span class="sxs-lookup"><span data-stu-id="0abc2-172">In the list, select the group that you created earlier.</span></span>
8. <span data-ttu-id="0abc2-173">Í reitnum Söluflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="0abc2-173">In the Sales group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="0abc2-174">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="0abc2-174">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="0abc2-175">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="0abc2-175">Click Save.</span></span>
11. <span data-ttu-id="0abc2-176">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="0abc2-176">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="0abc2-177">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="0abc2-177">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0abc2-178">Til dæmis, sía svæðið Vara með gildinu 'T0020'.</span><span class="sxs-lookup"><span data-stu-id="0abc2-178">For example, filter on the Item number field with a value of 'T0020 '.</span></span>
13. <span data-ttu-id="0abc2-179">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0abc2-179">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="0abc2-180">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="0abc2-180">Click Edit.</span></span>
15. <span data-ttu-id="0abc2-181">Útvíkka hlutann Selja.</span><span class="sxs-lookup"><span data-stu-id="0abc2-181">Expand the Sell section.</span></span>
16. <span data-ttu-id="0abc2-182">Í reitnum Sölulaunaflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="0abc2-182">In the Commission group field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="0abc2-183">Á listanum velurðu þóknunarflokk sem þú stofnaðir áður.</span><span class="sxs-lookup"><span data-stu-id="0abc2-183">In the list, select the commission group that you created earlier.</span></span>


