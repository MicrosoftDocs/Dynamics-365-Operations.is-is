---
title: Setja upp launanet
description: Launahnitanet eru notaðar til að skilgreina og viðhalda skipan launa fyrir launafyrirkomulög fastra launa.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b7e68ec4d172ced7ac66837e9580971d22b23b5f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465751"
---
# <a name="set-up-compensation-grids"></a><span data-ttu-id="6a794-103">Setja upp launanet</span><span class="sxs-lookup"><span data-stu-id="6a794-103">Set up compensation grids</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6a794-104">Launahnitanet eru notaðar til að skilgreina og viðhalda skipan launa fyrir launafyrirkomulög fastra launa.</span><span class="sxs-lookup"><span data-stu-id="6a794-104">Compensation grids are used to define and maintain the pay structures for fixed compensation plans.</span></span> <span data-ttu-id="6a794-105">Hægt er að deila hnitanet launa milli margra áætlanir eða afrituð þegar ný launafyrirkomulag er stofnað.</span><span class="sxs-lookup"><span data-stu-id="6a794-105">Compensation grids can be shared between multiple plans or copied when creating a new compensation plan.</span></span>  <span data-ttu-id="6a794-106">Áður en launanet er stofnað, setja verður upp Stig og tilvísunarpunkta.</span><span class="sxs-lookup"><span data-stu-id="6a794-106">Before creating a compensation grid, Levels and Reference points must be set up.</span></span> <span data-ttu-id="6a794-107">Þessu dæmi mun búa til nýja Launaþrep gerð launanet með sýnigögn fyrir Stig- og Tilvísuninarpunkta.</span><span class="sxs-lookup"><span data-stu-id="6a794-107">This example will create a new Grade type of compensation grid using demo data for the Levels and Reference points.</span></span> <span data-ttu-id="6a794-108">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="6a794-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-information-about-the-compensation-grid"></a><span data-ttu-id="6a794-109">Setja upp upplýsingar um hnitanet launa</span><span class="sxs-lookup"><span data-stu-id="6a794-109">Set up information about the compensation grid</span></span>
1. <span data-ttu-id="6a794-110">Farið í Mannauður > Bætur > Föst laun >Launanet.</span><span class="sxs-lookup"><span data-stu-id="6a794-110">Go to Human resources > Compensation > Fixed compensation > Compensation grids.</span></span>
2. <span data-ttu-id="6a794-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="6a794-111">Click New.</span></span>
3. <span data-ttu-id="6a794-112">Í reitinn hnitanet skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="6a794-112">In the Grid field, type a value.</span></span>
4. <span data-ttu-id="6a794-113">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="6a794-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6a794-114">Veljið valkost í svæðinu tegund.</span><span class="sxs-lookup"><span data-stu-id="6a794-114">In the Type field, select an option.</span></span>
6. <span data-ttu-id="6a794-115">Færa inn eða velja gildi í svæðinu uppsetningu Tilvísunar.</span><span class="sxs-lookup"><span data-stu-id="6a794-115">In the Reference setup field, enter or select a value.</span></span>
7. <span data-ttu-id="6a794-116">Í reitinn gjaldmiðill skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="6a794-116">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="6a794-117">Í reitinn Gjaldmiðill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="6a794-117">In the Currency field, type a value.</span></span>
9. <span data-ttu-id="6a794-118">Í reitnum Gildisdagsetning skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="6a794-118">In the Effective date field, enter a date.</span></span>

## <a name="add-levels-to-the-compensation-structure"></a><span data-ttu-id="6a794-119">Bæta við stigum í launaskipulag</span><span class="sxs-lookup"><span data-stu-id="6a794-119">Add levels to the compensation structure</span></span>
1. <span data-ttu-id="6a794-120">Smellt er á „Launaskipulag“.</span><span class="sxs-lookup"><span data-stu-id="6a794-120">Click Compensation structure.</span></span>
2. <span data-ttu-id="6a794-121">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="6a794-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="6a794-122">Sláðu inn eða veldu gildi í reitnum stig.</span><span class="sxs-lookup"><span data-stu-id="6a794-122">In the Level field, enter or select a value.</span></span>
4. <span data-ttu-id="6a794-123">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="6a794-123">Click New.</span></span>
5. <span data-ttu-id="6a794-124">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="6a794-124">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="6a794-125">Sláðu inn eða veldu gildi í reitnum stig.</span><span class="sxs-lookup"><span data-stu-id="6a794-125">In the Level field, enter or select a value.</span></span>
7. <span data-ttu-id="6a794-126">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="6a794-126">Click New.</span></span>
8. <span data-ttu-id="6a794-127">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="6a794-127">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="6a794-128">Sláðu inn eða veldu gildi í reitnum stig.</span><span class="sxs-lookup"><span data-stu-id="6a794-128">In the Level field, enter or select a value.</span></span>
10. <span data-ttu-id="6a794-129">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="6a794-129">Click New.</span></span>
11. <span data-ttu-id="6a794-130">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="6a794-130">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="6a794-131">Sláðu inn eða veldu gildi í reitnum stig.</span><span class="sxs-lookup"><span data-stu-id="6a794-131">In the Level field, enter or select a value.</span></span>
13. <span data-ttu-id="6a794-132">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="6a794-132">Click New.</span></span>
14. <span data-ttu-id="6a794-133">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="6a794-133">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="6a794-134">Sláðu inn eða veldu gildi í reitnum stig.</span><span class="sxs-lookup"><span data-stu-id="6a794-134">In the Level field, enter or select a value.</span></span>

## <a name="fill-in-the-compensation-structure-with-values"></a><span data-ttu-id="6a794-135">Fyllið inn í launaskipulag með gildum</span><span class="sxs-lookup"><span data-stu-id="6a794-135">Fill in the compensation structure with values</span></span>
1. <span data-ttu-id="6a794-136">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="6a794-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6a794-137">Á þessum tímapunkti handvirkt er hægt að færa inn gildi launa í hverju svæði í töflu eða breyta Margar aðgerðir sem hægt er að nota auðveldlega mörg svæði eru fyllt út og framkvæma grunnútreikninga.</span><span class="sxs-lookup"><span data-stu-id="6a794-137">At this point, compensation values can manually be entered into each field in the table, or the Mass change functionality can be used to easily fill in multiple fields and perform basic calculations.</span></span>  
2. <span data-ttu-id="6a794-138">Smellt er á Fjöldabreyting.</span><span class="sxs-lookup"><span data-stu-id="6a794-138">Click Mass change.</span></span>
    * <span data-ttu-id="6a794-139">Fyrir þetta hnitanet notum við fyrst gildi miðpunkts á fyrsta stigi á öll svæði í töflunni.</span><span class="sxs-lookup"><span data-stu-id="6a794-139">For this grid, we'll first apply the value for the midpoint of the first level's to all the fields in the table.</span></span> <span data-ttu-id="6a794-140">Þetta verður sem grunnur fyrir launafylki.</span><span class="sxs-lookup"><span data-stu-id="6a794-140">This will be the basis for the compensation matrix.</span></span>  
3. <span data-ttu-id="6a794-141">Veljið valkost í svæðinu gerð leiðréttingar.</span><span class="sxs-lookup"><span data-stu-id="6a794-141">In the Adjustment type field, select an option.</span></span>
4. <span data-ttu-id="6a794-142">Í reitinn Leiðréttingarupphæð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="6a794-142">In the Adjustment amount field, enter a number.</span></span>
5. <span data-ttu-id="6a794-143">Merkið eða afmerkið allar línur í listanum.</span><span class="sxs-lookup"><span data-stu-id="6a794-143">In the list, mark or unmark all rows.</span></span>
6. <span data-ttu-id="6a794-144">Smellt er á Nota á hnitanet.</span><span class="sxs-lookup"><span data-stu-id="6a794-144">Click Apply to grid.</span></span>
    * <span data-ttu-id="6a794-145">Nú munum við nota fjöldabreytingu til að stighækka upphæðir í hverri síðari stig með ákveðnum prósentu eða upphæð.</span><span class="sxs-lookup"><span data-stu-id="6a794-145">Now we'll use the mass change function to increment the amounts in each subsequent level by a certain percentage or amount.</span></span> <span data-ttu-id="6a794-146">Í þessu dæmi, hver launaþrep hafa er % 12,5 mun milli þeirra miðpunkta.</span><span class="sxs-lookup"><span data-stu-id="6a794-146">In this example, each grade will have a 12.5% spread between their midpoints.</span></span>  
7. <span data-ttu-id="6a794-147">Veljið valkost í svæðinu gerð leiðréttingar.</span><span class="sxs-lookup"><span data-stu-id="6a794-147">In the Adjustment type field, select an option.</span></span>
8. <span data-ttu-id="6a794-148">Í reitinn Leiðréttingarupphæð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="6a794-148">In the Adjustment amount field, enter a number.</span></span>
9. <span data-ttu-id="6a794-149">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="6a794-149">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="6a794-150">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="6a794-150">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="6a794-151">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="6a794-151">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="6a794-152">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="6a794-152">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="6a794-153">Smellt er á Nota á hnitanet.</span><span class="sxs-lookup"><span data-stu-id="6a794-153">Click Apply to grid.</span></span>
14. <span data-ttu-id="6a794-154">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="6a794-154">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="6a794-155">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="6a794-155">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="6a794-156">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="6a794-156">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="6a794-157">Smellt er á Nota á hnitanet.</span><span class="sxs-lookup"><span data-stu-id="6a794-157">Click Apply to grid.</span></span>
18. <span data-ttu-id="6a794-158">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="6a794-158">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="6a794-159">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="6a794-159">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="6a794-160">Smellt er á Nota á hnitanet.</span><span class="sxs-lookup"><span data-stu-id="6a794-160">Click Apply to grid.</span></span>
21. <span data-ttu-id="6a794-161">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="6a794-161">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="6a794-162">Smellt er á Nota á hnitanet.</span><span class="sxs-lookup"><span data-stu-id="6a794-162">Click Apply to grid.</span></span>
    * <span data-ttu-id="6a794-163">Nú munum við nota fjöldabreytingaraðgerð til að leiðrétta Lágmark og Hámark tilvísunarpunkta fyrir hvert stig.</span><span class="sxs-lookup"><span data-stu-id="6a794-163">Now we'll use the mass change function to adjust the Minimum and Maximum reference points for each level.</span></span> <span data-ttu-id="6a794-164">Þessu dæmi mun nota inn 50% mun svo tilvísunarpunktur Lágmark verður leiðrétt -20% og Hámark verður leiðrétta +20%.</span><span class="sxs-lookup"><span data-stu-id="6a794-164">This example will use a 50% spread so the Minimum reference point will be adjusted -20% and the Maximum will be adjusted +20%.</span></span>  
23. <span data-ttu-id="6a794-165">Í reitinn Leiðréttingarupphæð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="6a794-165">In the Adjustment amount field, enter a number.</span></span>
24. <span data-ttu-id="6a794-166">Færa inn eða veljið gildi í svæðinu tilvísunarpunktur.</span><span class="sxs-lookup"><span data-stu-id="6a794-166">In the Reference point field, enter or select a value.</span></span>
25. <span data-ttu-id="6a794-167">Merkið eða afmerkið allar línur í listanum.</span><span class="sxs-lookup"><span data-stu-id="6a794-167">In the list, mark or unmark all rows.</span></span>
26. <span data-ttu-id="6a794-168">Smellt er á Nota á hnitanet.</span><span class="sxs-lookup"><span data-stu-id="6a794-168">Click Apply to grid.</span></span>
27. <span data-ttu-id="6a794-169">Í reitinn Leiðréttingarupphæð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="6a794-169">In the Adjustment amount field, enter a number.</span></span>
28. <span data-ttu-id="6a794-170">Færa inn eða veljið gildi í svæðinu tilvísunarpunktur.</span><span class="sxs-lookup"><span data-stu-id="6a794-170">In the Reference point field, enter or select a value.</span></span>
29. <span data-ttu-id="6a794-171">Merkið eða afmerkið allar línur í listanum.</span><span class="sxs-lookup"><span data-stu-id="6a794-171">In the list, mark or unmark all rows.</span></span>
30. <span data-ttu-id="6a794-172">Smellt er á Nota á hnitanet.</span><span class="sxs-lookup"><span data-stu-id="6a794-172">Click Apply to grid.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]