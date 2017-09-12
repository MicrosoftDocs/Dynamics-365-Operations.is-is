--- 
title: "Flytja út bankaábyrgð"
description: "Þetta ferli fer í gegnum ferlið fyrir Útflutning kreditbréfs."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 07fef304361fa0008f57425ff27596e4e382072a
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="export-a-letter-of-credit"></a><span data-ttu-id="9811d-103">Flytja út bankaábyrgð</span><span class="sxs-lookup"><span data-stu-id="9811d-103">Export a letter of credit</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9811d-104">Þetta ferli fer í gegnum ferlið fyrir Útflutning kreditbréfs.</span><span class="sxs-lookup"><span data-stu-id="9811d-104">This procedure walks through the process of the Export letter of credit.</span></span>

<span data-ttu-id="9811d-105">Skjalaupplýsingar um kreditbréf er samning sem er gefið út af banka, sem bankinn samþykkir til að tryggja að greiðslur fyrir hönd kaupanda, ef skilmálum samningsins milli seljanda og kaupanda eru uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="9811d-105">A letter of credit is an agreement that is issued by a bank, in which the bank agrees to ensure payment on behalf of the buyer, if the terms of the agreement between the buyer and seller are met.</span></span>



<span data-ttu-id="9811d-106">Keyra ferli 'Setja upp bankaaðgerðir og bókunarreglur' og ‚kreditbréf_Stofna bankaaðstöðusamningur' aðferð fyrir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="9811d-106">Run the 'Set up bank facilities and posting profiles' procedure and the 'Letter of Credit_Create a bank facility agreement' procedure prior to this procedure.</span></span> <span data-ttu-id="9811d-107">Verður að velja fyrirtæki USMF sýnigögn til að keyra þetta ferli til enda.</span><span class="sxs-lookup"><span data-stu-id="9811d-107">The USMF demo company must be selected in order to run this procedure successfully.</span></span>




## <a name="create-sales-order-for-export-letter-of-credit"></a><span data-ttu-id="9811d-108">Stofna sölupöntun fyrir Flytja út kreditbréf</span><span class="sxs-lookup"><span data-stu-id="9811d-108">Create Sales Order for Export letter of credit</span></span>
1. <span data-ttu-id="9811d-109">Farið í Viðskiptakröfur > Pantanir > Allar sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="9811d-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="9811d-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="9811d-110">Click New.</span></span>
3. <span data-ttu-id="9811d-111">Í reitnum Reikningur viðskiptavina skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="9811d-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="9811d-112">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="9811d-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="9811d-113">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9811d-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9811d-114">Útvíkka eða draga saman hlutann Almennt.</span><span class="sxs-lookup"><span data-stu-id="9811d-114">Expand or collapse the General section.</span></span>
7. <span data-ttu-id="9811d-115">Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="9811d-115">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9811d-116">Velja Svæðið þar sem varan á að gefa út er í birgðum.</span><span class="sxs-lookup"><span data-stu-id="9811d-116">Select the Site where the item to be issued is stocked.</span></span>  
8. <span data-ttu-id="9811d-117">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9811d-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9811d-118">Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="9811d-118">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9811d-119">Veljið Vöruhús þar sem varan á að gefa út er í birgðum.</span><span class="sxs-lookup"><span data-stu-id="9811d-119">Select the Warehouse where item to be issued is stocked.</span></span>  
10. <span data-ttu-id="9811d-120">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9811d-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9811d-121">Athugasemd: Svæðið "Gerð bankaskjals" ætti að velja með gildinu "Kreditbréfs".</span><span class="sxs-lookup"><span data-stu-id="9811d-121">Note: The Bank document type field should be selected with the value 'Letter of credit'.</span></span>  
11. <span data-ttu-id="9811d-122">Í gerð bankaskjals svæðinu, veljið "Kreditbréfs".</span><span class="sxs-lookup"><span data-stu-id="9811d-122">In the Bank document type field, select 'Letter of credit'.</span></span>
12. <span data-ttu-id="9811d-123">Stækka eða fella saman hlutann Afhending.</span><span class="sxs-lookup"><span data-stu-id="9811d-123">Expand or collapse the Delivery section.</span></span>
    * <span data-ttu-id="9811d-124">Veljið stýringu Afhendingardagsetningar = Ekkert.</span><span class="sxs-lookup"><span data-stu-id="9811d-124">Select Delivery date control = None.</span></span>  
13. <span data-ttu-id="9811d-125">Færa inn dagsetningu í reitnum umbeðin móttökudagsetning</span><span class="sxs-lookup"><span data-stu-id="9811d-125">In the Requested receipt date field, enter a date.</span></span>
14. <span data-ttu-id="9811d-126">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9811d-126">Click OK.</span></span>
15. <span data-ttu-id="9811d-127">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="9811d-127">In the Item number field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9811d-128">Veljið vöruna sem þarf að vera Útgefið/Selt.</span><span class="sxs-lookup"><span data-stu-id="9811d-128">Select the required item to be Issued/Sold.</span></span>  
16. <span data-ttu-id="9811d-129">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="9811d-129">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="9811d-130">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9811d-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="9811d-131">Í reitnum Einingarverð skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="9811d-131">In the Unit price field, enter a number.</span></span>
19. <span data-ttu-id="9811d-132">Útvíkka eða draga saman hluta upplýsingar Línu.</span><span class="sxs-lookup"><span data-stu-id="9811d-132">Expand or collapse the Line details section.</span></span>
20. <span data-ttu-id="9811d-133">Smellið á flipann Afhendingar.</span><span class="sxs-lookup"><span data-stu-id="9811d-133">Click the Delivery tab.</span></span>
21. <span data-ttu-id="9811d-134">Færa inn dagsetningu í reitnum Umbeðinni sendingardagsetningu .</span><span class="sxs-lookup"><span data-stu-id="9811d-134">In the Requested ship date field, enter a date.</span></span>
22. <span data-ttu-id="9811d-135">Færa inn dagsetningu í reitnum staðfest sendingardagsetning</span><span class="sxs-lookup"><span data-stu-id="9811d-135">In the Confirmed ship date field, enter a date.</span></span>
23. <span data-ttu-id="9811d-136">Í Aðgerðarrúðunni er smellt á Stjórna.</span><span class="sxs-lookup"><span data-stu-id="9811d-136">On the Action Pane, click Manage.</span></span>
24. <span data-ttu-id="9811d-137">Smellt er á kreditbréf</span><span class="sxs-lookup"><span data-stu-id="9811d-137">Click Letter of credit.</span></span>
25. <span data-ttu-id="9811d-138">Færa inn gildi í reitnum númer bankaskjals.</span><span class="sxs-lookup"><span data-stu-id="9811d-138">In the Bank document number field, type a value.</span></span>
26. <span data-ttu-id="9811d-139">Færa inn dagsetningu og tíma í dagsetningarsvæði Gildistíma.</span><span class="sxs-lookup"><span data-stu-id="9811d-139">In the Expiration date field, enter a date and time.</span></span>
27. <span data-ttu-id="9811d-140">Útvíkka eða draga saman hlutanum bankaupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="9811d-140">Expand or collapse the Bank details section.</span></span>
28. <span data-ttu-id="9811d-141">Í reitnum Útgáfubanki skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="9811d-141">In the Issuing bank field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="9811d-142">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9811d-142">In the list, click the link in the selected row.</span></span>
30. <span data-ttu-id="9811d-143">Í reitnum banki sem veitir ráðgjöf skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="9811d-143">In the Advising bank field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="9811d-144">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="9811d-144">In the list, find and select the desired record.</span></span>
32. <span data-ttu-id="9811d-145">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9811d-145">In the list, click the link in the selected row.</span></span>
33. <span data-ttu-id="9811d-146">Smellt er á Sækja sending sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="9811d-146">Click Fetch sales order shipments.</span></span>
34. <span data-ttu-id="9811d-147">Smelltu á gefa út bankaskjal</span><span class="sxs-lookup"><span data-stu-id="9811d-147">Click Issue bank document.</span></span>
35. <span data-ttu-id="9811d-148">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9811d-148">Close the page.</span></span>

## <a name="post-packing-slip"></a><span data-ttu-id="9811d-149">Bóka fylgiseðil</span><span class="sxs-lookup"><span data-stu-id="9811d-149">Post Packing slip</span></span>
1. <span data-ttu-id="9811d-150">Smellið á „Tiltekt og pökkun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="9811d-150">On the Action Pane, click Pick and pack.</span></span>
2. <span data-ttu-id="9811d-151">Smellið á „Bóka fylgiseðil“.</span><span class="sxs-lookup"><span data-stu-id="9811d-151">Click Post packing slip.</span></span>
3. <span data-ttu-id="9811d-152">Útvíkka eða draga saman hlutann Færibreytur.</span><span class="sxs-lookup"><span data-stu-id="9811d-152">Expand or collapse the Parameters section.</span></span>
4. <span data-ttu-id="9811d-153">Í svæðinu magn, veljið 'Allt'.</span><span class="sxs-lookup"><span data-stu-id="9811d-153">In the Quantity field, select 'All'.</span></span>
5. <span data-ttu-id="9811d-154">Útvíkka eða draga saman hlutann Setja upp.</span><span class="sxs-lookup"><span data-stu-id="9811d-154">Expand or collapse the Setup section.</span></span>
6. <span data-ttu-id="9811d-155">Færa inn dagsetningu í reitnum dagsetning fylgiseðils.</span><span class="sxs-lookup"><span data-stu-id="9811d-155">In the Packing slip date field, enter a date.</span></span>
7. <span data-ttu-id="9811d-156">Veljið númer fyrir Sendingu.</span><span class="sxs-lookup"><span data-stu-id="9811d-156">Select the Shipment number.</span></span>
8. <span data-ttu-id="9811d-157">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9811d-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9811d-158">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9811d-158">Click OK.</span></span>
10. <span data-ttu-id="9811d-159">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9811d-159">Click OK.</span></span>

## <a name="post-sales-invoice"></a><span data-ttu-id="9811d-160">Bókar sölureikninga.</span><span class="sxs-lookup"><span data-stu-id="9811d-160">Post sales invoice</span></span>
1. <span data-ttu-id="9811d-161">Smellið á „Reikningur“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="9811d-161">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="9811d-162">Smellið á „Reikningur“.</span><span class="sxs-lookup"><span data-stu-id="9811d-162">Click Invoice.</span></span>
3. <span data-ttu-id="9811d-163">Útvíkka eða draga saman hlutann yfirlit.</span><span class="sxs-lookup"><span data-stu-id="9811d-163">Expand or collapse the Overview section.</span></span>
4. <span data-ttu-id="9811d-164">Veljið númer fyrir Sendingu.</span><span class="sxs-lookup"><span data-stu-id="9811d-164">Select the Shipment number.</span></span>
5. <span data-ttu-id="9811d-165">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9811d-165">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9811d-166">Útvíkka eða draga saman hlutann Setja upp.</span><span class="sxs-lookup"><span data-stu-id="9811d-166">Expand or collapse the Setup section.</span></span>
7. <span data-ttu-id="9811d-167">Færið inn dagsetningu á svæðinu „Reikningsdagsetning“.</span><span class="sxs-lookup"><span data-stu-id="9811d-167">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="9811d-168">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9811d-168">Click OK.</span></span>
9. <span data-ttu-id="9811d-169">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9811d-169">Click OK.</span></span>

## <a name="shipment-document-submitted-status"></a><span data-ttu-id="9811d-170">Staða fyrir sent Flutningsskjal </span><span class="sxs-lookup"><span data-stu-id="9811d-170">Shipment document submitted status</span></span>
1. <span data-ttu-id="9811d-171">Í Aðgerðarrúðunni er smellt á Stjórna.</span><span class="sxs-lookup"><span data-stu-id="9811d-171">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="9811d-172">Smellt er á kreditbréf</span><span class="sxs-lookup"><span data-stu-id="9811d-172">Click Letter of credit.</span></span>
3. <span data-ttu-id="9811d-173">Útvíkka eða draga saman hlutann línur.</span><span class="sxs-lookup"><span data-stu-id="9811d-173">Expand or collapse the Lines section.</span></span>
    * <span data-ttu-id="9811d-174">Athugasemd: Svæðið 'Skjal er sent' ætti að stilla 'Já'.</span><span class="sxs-lookup"><span data-stu-id="9811d-174">Note: The 'Document submitted' field should be set to 'Yes'.</span></span>  

## <a name="verify-export-letter-of-credit"></a><span data-ttu-id="9811d-175">Sannprófa flytja út kreditbréf</span><span class="sxs-lookup"><span data-stu-id="9811d-175">Verify Export letter of credit</span></span>
1. <span data-ttu-id="9811d-176">Fara í Reiðufé og bankastjórnun > Kreditbréf > Flytja út kreditbréf og innflutningssafn.</span><span class="sxs-lookup"><span data-stu-id="9811d-176">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="9811d-177">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="9811d-177">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9811d-178">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9811d-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9811d-179">Staðfestið að ábyrgðarbréf útflutnings hefur sendingarstaða 'Reikningsfært'.</span><span class="sxs-lookup"><span data-stu-id="9811d-179">Verify that the Export letter of credit has a Shipment status of 'Invoiced'.</span></span>  

## <a name="customer-payment"></a><span data-ttu-id="9811d-180">Greiðsla viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="9811d-180">Customer payment</span></span>
1. <span data-ttu-id="9811d-181">Fara í Viðskiptakröfur > Greiðslur > Greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="9811d-181">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="9811d-182">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="9811d-182">Click New.</span></span>
3. <span data-ttu-id="9811d-183">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="9811d-183">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="9811d-184">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="9811d-184">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="9811d-185">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9811d-185">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="9811d-186">Smellið á Línur.</span><span class="sxs-lookup"><span data-stu-id="9811d-186">Click Lines.</span></span>
7. <span data-ttu-id="9811d-187">Dagsetning er rituð í reitinn Dagetning.</span><span class="sxs-lookup"><span data-stu-id="9811d-187">In the Date field, enter a date.</span></span>
8. <span data-ttu-id="9811d-188">Í reitnum Lykill skal tilgreina gildi sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="9811d-188">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="9811d-189">Smellt er á Jöfnun.</span><span class="sxs-lookup"><span data-stu-id="9811d-189">Click Settlement.</span></span>
10. <span data-ttu-id="9811d-190">Velja skal gátreitinn í hausnum fyrir samtala.</span><span class="sxs-lookup"><span data-stu-id="9811d-190">Select the check box on the header of Totals.</span></span>
    * <span data-ttu-id="9811d-191">Athugasemd: Stilla svæðið Sýna á "Kreditbréfs" .</span><span class="sxs-lookup"><span data-stu-id="9811d-191">Note: Set the Show field to 'Letter of credit'.</span></span>  
11. <span data-ttu-id="9811d-192">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="9811d-192">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="9811d-193">Veldu eða hreinsaðu gátreitinn Merkið við.</span><span class="sxs-lookup"><span data-stu-id="9811d-193">Select or clear the Mark check box.</span></span>
13. <span data-ttu-id="9811d-194">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9811d-194">Click OK.</span></span>
14. <span data-ttu-id="9811d-195">Smellið á flipann Greiðslu.</span><span class="sxs-lookup"><span data-stu-id="9811d-195">Click the Payment tab.</span></span>
    * <span data-ttu-id="9811d-196">Staðfesta númer bankaskjals og upplýsingar sendingarnúmers</span><span class="sxs-lookup"><span data-stu-id="9811d-196">Verify Bank document number and Shipment number details</span></span>  
15. <span data-ttu-id="9811d-197">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="9811d-197">Click Post.</span></span>

## <a name="verify-export-letter-of-credit-after-payment"></a><span data-ttu-id="9811d-198">Staðfesta flytja út kreditbréf eftir greiðslu</span><span class="sxs-lookup"><span data-stu-id="9811d-198">Verify Export letter of credit after payment</span></span>
1. <span data-ttu-id="9811d-199">Fara í Reiðufé og bankastjórnun > Kreditbréf > Flytja út kreditbréf og innflutningssafn.</span><span class="sxs-lookup"><span data-stu-id="9811d-199">Go to Cash and bank management > Letters of credit > Export letter of credit and import collection.</span></span>
2. <span data-ttu-id="9811d-200">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="9811d-200">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9811d-201">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9811d-201">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9811d-202">Staðfesta sendingarstaða = Greiðsla móttekin og staða upphæð = 0,00.</span><span class="sxs-lookup"><span data-stu-id="9811d-202">Verify Shipment status = Payment received and balance amount = 0.00.</span></span>  


