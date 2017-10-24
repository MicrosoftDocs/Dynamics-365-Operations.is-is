--- 
title: "Flytja inn bankaábyrgð"
description: "Þetta ferli fer í gegnum ferlið fyrir innflutning á kreditbréfs."
author: kweekley
manager: AnnBe
ms.date: 02/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 02be2627186a149a05eaccfa3e5906a9fe1d74dd
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="import-a-letter-of-credit"></a><span data-ttu-id="554dc-103">Flytja inn bankaábyrgð</span><span class="sxs-lookup"><span data-stu-id="554dc-103">Import a letter of credit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="554dc-104">Þetta ferli fer í gegnum ferlið fyrir innflutning á kreditbréfs.</span><span class="sxs-lookup"><span data-stu-id="554dc-104">This procedure walks through the process of importing a letter of credit.</span></span> <span data-ttu-id="554dc-105">Setja verður upp eftirfarandi áður en þessi ferli er klárað: banka aðstöðu, forstillingar bókunar , bankaaðstöðusamningnum og upplýsingar um banka lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="554dc-105">The following must be set up before completing this procedure: bank facilities, posting profiles, a bank facility agreement and vendor bank details.</span></span>

<span data-ttu-id="554dc-106">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="554dc-106">This procedure uses the USMF demo company.</span></span>


## <a name="create-a-purchase-order-with-letter-of-credit"></a><span data-ttu-id="554dc-107">Stofna innkaupapöntun með kreditbréfi</span><span class="sxs-lookup"><span data-stu-id="554dc-107">Create a Purchase order with Letter of credit</span></span>
1. <span data-ttu-id="554dc-108">Fara í Viðskiptaskuldir > Innkaupapantanir > Allar innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="554dc-108">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="554dc-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="554dc-109">Click New.</span></span>
3. <span data-ttu-id="554dc-110">Færa inn eða veljið gildi í svæðinu lánardrottnalykill.</span><span class="sxs-lookup"><span data-stu-id="554dc-110">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="554dc-111">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="554dc-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="554dc-112">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="554dc-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="554dc-113">Útvíkka eða draga saman hlutann Almennt.</span><span class="sxs-lookup"><span data-stu-id="554dc-113">Expand the General section.</span></span>
7. <span data-ttu-id="554dc-114">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="554dc-114">In the Site field, enter or select a value.</span></span>
8. <span data-ttu-id="554dc-115">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="554dc-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="554dc-116">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="554dc-116">In the Warehouse field, enter or select a value.</span></span>
10. <span data-ttu-id="554dc-117">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="554dc-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="554dc-118">Dagsetning er rituð í reitinn dagsetning reikningsskila.</span><span class="sxs-lookup"><span data-stu-id="554dc-118">In the Accounting date field, enter a date.</span></span>
12. <span data-ttu-id="554dc-119">Dagsetning er rituð í reitinn afhendingardagur.</span><span class="sxs-lookup"><span data-stu-id="554dc-119">In the Delivery date field, enter a date.</span></span>
    * <span data-ttu-id="554dc-120">Athugasemd: Svæðið 'Gerð bankaskjals' ætti að velja með gildinu "Kreditbréfs".</span><span class="sxs-lookup"><span data-stu-id="554dc-120">Note: The 'Bank document type' field should be selected with the value  'Letter of credit'.</span></span>  
13. <span data-ttu-id="554dc-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="554dc-121">Click OK.</span></span>
14. <span data-ttu-id="554dc-122">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="554dc-122">In the Item number field, enter or select a value.</span></span>
15. <span data-ttu-id="554dc-123">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="554dc-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="554dc-124">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="554dc-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="554dc-125">Útvíkka hlutann upplýsingar Línu.</span><span class="sxs-lookup"><span data-stu-id="554dc-125">Expand the Line details section.</span></span>
18. <span data-ttu-id="554dc-126">Smellið á flipann Afhendingar.</span><span class="sxs-lookup"><span data-stu-id="554dc-126">Click the Delivery tab.</span></span>
19. <span data-ttu-id="554dc-127">Dagsetning er rituð í reitinn afhendingardagur.</span><span class="sxs-lookup"><span data-stu-id="554dc-127">In the Delivery date field, enter a date.</span></span>
20. <span data-ttu-id="554dc-128">Dagsetning er rituð í reitinn staðfestur afhendingardagur.</span><span class="sxs-lookup"><span data-stu-id="554dc-128">In the Confirmed delivery date field, enter a date.</span></span>
21. <span data-ttu-id="554dc-129">Færið inn númer í reitnum „Einingarverð“.</span><span class="sxs-lookup"><span data-stu-id="554dc-129">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="554dc-130">Skilgreina upplýsingar kreditbréfs.</span><span class="sxs-lookup"><span data-stu-id="554dc-130">Define the Letter of credit details.</span></span>  
22. <span data-ttu-id="554dc-131">Í Aðgerðarrúðunni er smellt á Stjórna.</span><span class="sxs-lookup"><span data-stu-id="554dc-131">On the Action Pane, click Manage.</span></span>
23. <span data-ttu-id="554dc-132">Smellt er á kreditbréf/innflutningssafn</span><span class="sxs-lookup"><span data-stu-id="554dc-132">Click Letter of credit / import collection.</span></span>
24. <span data-ttu-id="554dc-133">Í svæðinu dagsetningu beitingar, færið inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="554dc-133">In the Application date field, enter a date and time.</span></span>
    * <span data-ttu-id="554dc-134">Staðfesta að svæðið ' bankareikningur' hefur sjálfgefin virkan bankareikninginn, sem er byggð á dagsetningu forrits.</span><span class="sxs-lookup"><span data-stu-id="554dc-134">Verify that the 'Bank account' field has the default active Bank account, which is based on the application date.</span></span>  
25. <span data-ttu-id="554dc-135">Færa inn gildi í reitnum númer bankaskjals.</span><span class="sxs-lookup"><span data-stu-id="554dc-135">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="554dc-136">Í svæðið móttökudagsetning, færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="554dc-136">In the Date of receipt field, enter a date and time.</span></span>
27. <span data-ttu-id="554dc-137">Útvíkka hlutann Bankaskjal.</span><span class="sxs-lookup"><span data-stu-id="554dc-137">Expand the Bank document section.</span></span>
28. <span data-ttu-id="554dc-138">Færa inn dagsetningu og tíma í dagsetningarsvæði Gildistíma.</span><span class="sxs-lookup"><span data-stu-id="554dc-138">In the Expiration date field, enter a date and time.</span></span>
29. <span data-ttu-id="554dc-139">Útvíkka hlutann bankaupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="554dc-139">Expand the Bank details section.</span></span>
30. <span data-ttu-id="554dc-140">Sláið inn eða veldu gildi í reitnum banki sem veitir ráðgjöf.</span><span class="sxs-lookup"><span data-stu-id="554dc-140">In the Advising bank field, enter or select a value.</span></span>
31. <span data-ttu-id="554dc-141">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="554dc-141">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="554dc-142">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="554dc-142">Click Save.</span></span>
33. <span data-ttu-id="554dc-143">Smellt er á Sækja sending innkaupapöntunar.</span><span class="sxs-lookup"><span data-stu-id="554dc-143">Click Fetch purchase order shipments.</span></span>
34. <span data-ttu-id="554dc-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-144">Close the page.</span></span>
35. <span data-ttu-id="554dc-145">Smellið á „Innkaup“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-145">On the Action Pane, click Purchase.</span></span>
36. <span data-ttu-id="554dc-146">Smellið á „Staðfesta“.</span><span class="sxs-lookup"><span data-stu-id="554dc-146">Click Confirm.</span></span>
37. <span data-ttu-id="554dc-147">Í Aðgerðarrúðunni er smellt á Stjórna.</span><span class="sxs-lookup"><span data-stu-id="554dc-147">On the Action Pane, click Manage.</span></span>
38. <span data-ttu-id="554dc-148">Smellt er á kreditbréf/innflutningssafn</span><span class="sxs-lookup"><span data-stu-id="554dc-148">Click Letter of credit / import collection.</span></span>
39. <span data-ttu-id="554dc-149">Smellið á Vinnslu.</span><span class="sxs-lookup"><span data-stu-id="554dc-149">Click Process.</span></span>
40. <span data-ttu-id="554dc-150">Smellið á „Staðfesta“.</span><span class="sxs-lookup"><span data-stu-id="554dc-150">Click Confirm.</span></span>
    * <span data-ttu-id="554dc-151">Staðfesta aðstöðustaða minnkar upphæð innkaupapöntunar.</span><span class="sxs-lookup"><span data-stu-id="554dc-151">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="554dc-152">Í þessu dæmi Innkaupaupphæð = 500,00, aðstöðuhámark = 10000.00, því aðstöðustaða = 9500.00.</span><span class="sxs-lookup"><span data-stu-id="554dc-152">In this example, Purchase amount = 500.00,  Facility limit = 10000.00,  therefore, Facility balance = 9500.00.</span></span>  
41. <span data-ttu-id="554dc-153">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-153">Close the page.</span></span>
42. <span data-ttu-id="554dc-154">Færið inn númer í reitnum „Einingarverð“.</span><span class="sxs-lookup"><span data-stu-id="554dc-154">In the Unit price field, enter a number.</span></span>
43. <span data-ttu-id="554dc-155">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="554dc-155">Click Save.</span></span>
44. <span data-ttu-id="554dc-156">Smellið á „Innkaup“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-156">On the Action Pane, click Purchase.</span></span>
45. <span data-ttu-id="554dc-157">Smellið á „Staðfesta“.</span><span class="sxs-lookup"><span data-stu-id="554dc-157">Click Confirm.</span></span>
    * <span data-ttu-id="554dc-158">Lagfæra kreditbréf, vegna breytinga í einingaverði.</span><span class="sxs-lookup"><span data-stu-id="554dc-158">Amend the Letter of credit, due to the change in Unit price.</span></span>  
46. <span data-ttu-id="554dc-159">Í Aðgerðarrúðunni er smellt á Stjórna.</span><span class="sxs-lookup"><span data-stu-id="554dc-159">On the Action Pane, click Manage.</span></span>
47. <span data-ttu-id="554dc-160">Smellt er á kreditbréf/innflutningssafn</span><span class="sxs-lookup"><span data-stu-id="554dc-160">Click Letter of credit / import collection.</span></span>
    * <span data-ttu-id="554dc-161">Lagfæra kreditbréf, vegna breytinga á einingarverð Innkaupapöntunar.</span><span class="sxs-lookup"><span data-stu-id="554dc-161">Amend the letter of credit, due to the change in Purchase unit price.</span></span>  
48. <span data-ttu-id="554dc-162">Smellið á Vinnslu.</span><span class="sxs-lookup"><span data-stu-id="554dc-162">Click Process.</span></span>
49. <span data-ttu-id="554dc-163">Smellt er á Lagfæra.</span><span class="sxs-lookup"><span data-stu-id="554dc-163">Click Amend.</span></span>
50. <span data-ttu-id="554dc-164">Smella á Fjarlægja.</span><span class="sxs-lookup"><span data-stu-id="554dc-164">Click Remove.</span></span>
51. <span data-ttu-id="554dc-165">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="554dc-165">Click Yes.</span></span>
52. <span data-ttu-id="554dc-166">Smellt er á Sækja sending innkaupapöntunar.</span><span class="sxs-lookup"><span data-stu-id="554dc-166">Click Fetch purchase order shipments.</span></span>
53. <span data-ttu-id="554dc-167">Smellið á Vinnslu.</span><span class="sxs-lookup"><span data-stu-id="554dc-167">Click Process.</span></span>
54. <span data-ttu-id="554dc-168">Smellið á „Staðfesta“.</span><span class="sxs-lookup"><span data-stu-id="554dc-168">Click Confirm.</span></span>
    * <span data-ttu-id="554dc-169">Staðfesta aðstöðustaða minnkar upphæð innkaupapöntunar.</span><span class="sxs-lookup"><span data-stu-id="554dc-169">Verify that the Facility balance reduces the purchase order amount.</span></span>  <span data-ttu-id="554dc-170">Í þessu dæmi er hægt að breyta upphæð Innkaupa = 600,00, aðstöðuhámark = 10000.00, því aðstöðustaða = 9400.00.</span><span class="sxs-lookup"><span data-stu-id="554dc-170">In this example, edited Purchase amount = 600.00,  Facility limit = 10000.00,  therefore, Facility balance = 9400.00.</span></span>  
55. <span data-ttu-id="554dc-171">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-171">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="554dc-172">Bóka fylgiseðil</span><span class="sxs-lookup"><span data-stu-id="554dc-172">Post Packing slip</span></span>
1. <span data-ttu-id="554dc-173">Smellið á „Móttaka“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-173">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="554dc-174">Smellið á „Innhreyfingarskjal“.</span><span class="sxs-lookup"><span data-stu-id="554dc-174">Click Product receipt.</span></span>
3. <span data-ttu-id="554dc-175">Í reitinn PurchParmTable_Num skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="554dc-175">In the PurchParmTable_Num field, type a value.</span></span>
    * <span data-ttu-id="554dc-176">Veljið númer Sendingar stofnaðar með tilvísan í kreditbréfi.</span><span class="sxs-lookup"><span data-stu-id="554dc-176">Select the Shipment number created with reference to the Letter of credit.</span></span>  
4. <span data-ttu-id="554dc-177">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="554dc-177">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="554dc-178">Færa inn dagsetningu í reitnum móttökudagsetning afurðar.</span><span class="sxs-lookup"><span data-stu-id="554dc-178">In the Product receipt date field, enter a date.</span></span>
6. <span data-ttu-id="554dc-179">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="554dc-179">Click OK.</span></span>
7. <span data-ttu-id="554dc-180">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-180">Close the page.</span></span>
8. <span data-ttu-id="554dc-181">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-181">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="554dc-182">Staðfesta skal stöðu Innflutnings kreditbréfs</span><span class="sxs-lookup"><span data-stu-id="554dc-182">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="554dc-183">Fara í Reiðufé og bankastjórnun > Kreditbréf > Flytja inn kreditbréf og innflutningssafn.</span><span class="sxs-lookup"><span data-stu-id="554dc-183">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="554dc-184">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="554dc-184">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="554dc-185">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="554dc-185">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="554dc-186">Sannprófa innflutt bréf stöðu lánsfés</span><span class="sxs-lookup"><span data-stu-id="554dc-186">Verify the Import letter of credit status.</span></span>  
4. <span data-ttu-id="554dc-187">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-187">Close the page.</span></span>
5. <span data-ttu-id="554dc-188">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-188">Close the page.</span></span>

## <a name="post-purchase-invoice"></a><span data-ttu-id="554dc-189">Bóka innkaupareikninga</span><span class="sxs-lookup"><span data-stu-id="554dc-189">Post purchase invoice</span></span>
1. <span data-ttu-id="554dc-190">Fara í Viðskiptaskuldir > Innkaupapantanir > Allar innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="554dc-190">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
    * <span data-ttu-id="554dc-191">Velja innkaupapöntun sem var stofnuð með kreditbréfs.</span><span class="sxs-lookup"><span data-stu-id="554dc-191">Select the purchase order that was created with letter of credit.</span></span>  
2. <span data-ttu-id="554dc-192">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="554dc-192">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="554dc-193">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="554dc-193">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="554dc-194">Smellið á „Reikningur“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-194">On the Action Pane, click Invoice.</span></span>
5. <span data-ttu-id="554dc-195">Smellt er á Reikningnum.</span><span class="sxs-lookup"><span data-stu-id="554dc-195">Click Invoice.</span></span>
6. <span data-ttu-id="554dc-196">Í reitnum Númer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="554dc-196">In the Number field, type a value.</span></span>
7. <span data-ttu-id="554dc-197">Í reitinn sendingarnúmer skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="554dc-197">In the Shipment number field, enter or select a value.</span></span>
8. <span data-ttu-id="554dc-198">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="554dc-198">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="554dc-199">Færið inn dagsetningu á svæðinu „Reikningsdagsetning“.</span><span class="sxs-lookup"><span data-stu-id="554dc-199">In the Invoice date field, enter a date.</span></span>
10. <span data-ttu-id="554dc-200">Smellið á „Uppfæra samsvörunarstöðu“.</span><span class="sxs-lookup"><span data-stu-id="554dc-200">Click Update match status.</span></span>
11. <span data-ttu-id="554dc-201">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="554dc-201">Click Post.</span></span>
12. <span data-ttu-id="554dc-202">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-202">Close the page.</span></span>
13. <span data-ttu-id="554dc-203">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-203">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status"></a><span data-ttu-id="554dc-204">Staðfesta skal stöðu Innflutnings kreditbréfs</span><span class="sxs-lookup"><span data-stu-id="554dc-204">Verify Import letter of credit status</span></span>
1. <span data-ttu-id="554dc-205">Fara í Reiðufé og bankastjórnun > Kreditbréf > Flytja inn kreditbréf og innflutningssafn.</span><span class="sxs-lookup"><span data-stu-id="554dc-205">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="554dc-206">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="554dc-206">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="554dc-207">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="554dc-207">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="554dc-208">Staðfesta Innflutning kreditbréfs credit2.</span><span class="sxs-lookup"><span data-stu-id="554dc-208">Verify the Import letter of credit2.</span></span>  
    * <span data-ttu-id="554dc-209">Villuleita: Sendingarstaða = Reikningsfært upplýsingar um bankaaðstaða</span><span class="sxs-lookup"><span data-stu-id="554dc-209">Validate :  Shipment status = Invoiced  Bank facility details</span></span>  
4. <span data-ttu-id="554dc-210">Smellið á Skoða.</span><span class="sxs-lookup"><span data-stu-id="554dc-210">Click View.</span></span>
5. <span data-ttu-id="554dc-211">Smellt er á Prenta umsókn.</span><span class="sxs-lookup"><span data-stu-id="554dc-211">Click Print application.</span></span>
6. <span data-ttu-id="554dc-212">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="554dc-212">Click OK.</span></span>
    * <span data-ttu-id="554dc-213">Staðfesta jöfnun kreditbréf er prentuð.</span><span class="sxs-lookup"><span data-stu-id="554dc-213">Verify that the Letter of credit application gets printed.</span></span>  
7. <span data-ttu-id="554dc-214">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-214">Close the page.</span></span>
8. <span data-ttu-id="554dc-215">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-215">Close the page.</span></span>
9. <span data-ttu-id="554dc-216">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-216">Close the page.</span></span>

## <a name="post-vendor-payment-journal-for-the-created-purchase-invoice-with-letter-of-credit"></a><span data-ttu-id="554dc-217">Bóka greiðslubók Lánardrottins fyrir reikninga innkaupapantana sem stofnaðar með kreditbréfs</span><span class="sxs-lookup"><span data-stu-id="554dc-217">Post Vendor payment journal for the created purchase invoice with letter of credit</span></span>
1. <span data-ttu-id="554dc-218">Fara í Viðskiptaskuldir > Greiðslur > Greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="554dc-218">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="554dc-219">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="554dc-219">Click New.</span></span>
3. <span data-ttu-id="554dc-220">Sláið inn eða veldu gildi í reitnum heiti.</span><span class="sxs-lookup"><span data-stu-id="554dc-220">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="554dc-221">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="554dc-221">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="554dc-222">Smellið á Línur.</span><span class="sxs-lookup"><span data-stu-id="554dc-222">Click Lines.</span></span>
6. <span data-ttu-id="554dc-223">Dagsetning er rituð í reitinn Dagetning.</span><span class="sxs-lookup"><span data-stu-id="554dc-223">In the Date field, enter a date.</span></span>
7. <span data-ttu-id="554dc-224">Í reitnum Lykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="554dc-224">In the Account field, specify the desired values.</span></span>
8. <span data-ttu-id="554dc-225">Smellt er á Gera upp færslur.</span><span class="sxs-lookup"><span data-stu-id="554dc-225">Click Settle transactions.</span></span>
9. <span data-ttu-id="554dc-226">Stækka Samtals hluti.</span><span class="sxs-lookup"><span data-stu-id="554dc-226">Expand the Totals section.</span></span>
10. <span data-ttu-id="554dc-227">Í reitnum Sýna skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="554dc-227">In the Show field, select an option.</span></span>
    * <span data-ttu-id="554dc-228">Staðfesta að númer bankaskjals og svæði sendingarnúmers hafa verið uppfærðar.</span><span class="sxs-lookup"><span data-stu-id="554dc-228">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
11. <span data-ttu-id="554dc-229">Veldu gátreitinn Merkja.</span><span class="sxs-lookup"><span data-stu-id="554dc-229">Select the Mark check box.</span></span>
12. <span data-ttu-id="554dc-230">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="554dc-230">Click OK.</span></span>
13. <span data-ttu-id="554dc-231">Smellið á flipann Greiðslu.</span><span class="sxs-lookup"><span data-stu-id="554dc-231">Click the Payment tab.</span></span>
    * <span data-ttu-id="554dc-232">Staðfesta að númer bankaskjals og svæði sendingarnúmers hafa verið uppfærðar.</span><span class="sxs-lookup"><span data-stu-id="554dc-232">Verify that the Bank document number and Shipment number fields have been updated.</span></span>  
14. <span data-ttu-id="554dc-233">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="554dc-233">Click Post.</span></span>
15. <span data-ttu-id="554dc-234">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-234">Close the page.</span></span>
16. <span data-ttu-id="554dc-235">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-235">Close the page.</span></span>

## <a name="verify-import-letter-of-credit-status-after-invoice-paid"></a><span data-ttu-id="554dc-236">Staðfesta skal stöðu Innflutnings kreditbréfs eftir að Reikningur greiddur</span><span class="sxs-lookup"><span data-stu-id="554dc-236">Verify Import letter of credit status after Invoice paid</span></span>
1. <span data-ttu-id="554dc-237">Fara í Reiðufé og bankastjórnun > Kreditbréf > Flytja inn kreditbréf og innflutningssafn.</span><span class="sxs-lookup"><span data-stu-id="554dc-237">Go to Cash and bank management > Letters of credit > Import letter of credit and import collection.</span></span>
2. <span data-ttu-id="554dc-238">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="554dc-238">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="554dc-239">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="554dc-239">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="554dc-240">Sannprófa innflutt bréf stöðu lánsfés</span><span class="sxs-lookup"><span data-stu-id="554dc-240">Verify the Import letter of credit status.</span></span>   
4. <span data-ttu-id="554dc-241">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-241">Close the page.</span></span>

## <a name="verify-the-bank-facility-limit-and-utilization-report"></a><span data-ttu-id="554dc-242">Staðfesta aðstöðumörk banka og nýtingarskýrslu</span><span class="sxs-lookup"><span data-stu-id="554dc-242">Verify the Bank facility limit and utilization report</span></span>
1. <span data-ttu-id="554dc-243">Fara í Reiðufé og bankakerfi > Fyrirspurnir og skýrslur > Kreditbréf eða ábyrgðarbréf > Bankaaðgerðir og skýrsla um nýtingu.</span><span class="sxs-lookup"><span data-stu-id="554dc-243">Go to Cash and bank management > Inquiries and reports > Letters of credit or guarantee > Bank facilities and utilization report.</span></span>
2. <span data-ttu-id="554dc-244">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="554dc-244">Expand the Records to include section.</span></span>
3. <span data-ttu-id="554dc-245">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="554dc-245">Click Filter.</span></span>
    * <span data-ttu-id="554dc-246">Skilgreina svæðið Skilyrði með bankareikning sem þarf.</span><span class="sxs-lookup"><span data-stu-id="554dc-246">Define the Criteria field with the required bank account.</span></span>  
4. <span data-ttu-id="554dc-247">Í reitinn Skilyrði skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="554dc-247">In the Criteria field, enter or select a value.</span></span>
5. <span data-ttu-id="554dc-248">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="554dc-248">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="554dc-249">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="554dc-249">Click OK.</span></span>
7. <span data-ttu-id="554dc-250">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="554dc-250">Click OK.</span></span>
    * <span data-ttu-id="554dc-251">Staðfesta skýrsluna sem sýnir færslur.</span><span class="sxs-lookup"><span data-stu-id="554dc-251">Verify the report which lists the transactions.</span></span>  
    * <span data-ttu-id="554dc-252">Staðfesta skýrslunni inniheldur færslur með númer bankaskjals, aðstöðuhámark, nýttar upphæð og stöðuupphæð aðstöðu.</span><span class="sxs-lookup"><span data-stu-id="554dc-252">Verify the report lists the transactions with Bank document number, Facility limit, utilized amount and the facility balance amount.</span></span>  
8. <span data-ttu-id="554dc-253">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="554dc-253">Close the page.</span></span>


