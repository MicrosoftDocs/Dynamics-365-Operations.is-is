---
title: Færsla ábyrgðarbréfs
description: Þetta ferli fer í gegnum Fyrir ferli ábyrgðarbréfs.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Reasons, SalesTableListPage, SalesCreateOrder, SalesTable, BankLGRequestForm, BankLGRequestFormRequest, BankLGGuarantee, BankLGFormSubmitToBank, BankDocumentAgreementLineLookup, BankLGFormReceiveFromBank, LedgerJournalTable, LedgerJournalTransDaily, BankLGRequestFormGiveToBeneficiary, BankLGFormGiveToBeneficiary, BankLGRequestFormIncreaseValue, BankLGFormIncreaseValue, BankLGRequestFormLiquidate, BankLGFormLiquidate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05abad6898c2b97cf66abdff21b30407dacd6488
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444475"
---
# <a name="letter-of-guarantee-transaction"></a><span data-ttu-id="8be0c-103">Færsla ábyrgðarbréfs</span><span class="sxs-lookup"><span data-stu-id="8be0c-103">Letter of guarantee transaction</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8be0c-104">Þetta ferli fer í gegnum Fyrir ferli ábyrgðarbréfs.</span><span class="sxs-lookup"><span data-stu-id="8be0c-104">This procedure walks through the Letter of guarantee process.</span></span>



<span data-ttu-id="8be0c-105">Ljúka þarf eftirfarandi verkum áður en þessu ferli er lokið:</span><span class="sxs-lookup"><span data-stu-id="8be0c-105">The following tasks must be complete before completing this procedure:</span></span>

- <span data-ttu-id="8be0c-106">Setja upp bankaaðstöðu og bókunarreglur fyrir ábyrgðaryfirlýsingu.</span><span class="sxs-lookup"><span data-stu-id="8be0c-106">Set up bank facilities and posting profiles for a letter of guarantee.</span></span>

- <span data-ttu-id="8be0c-107">Stofna bankaaðstöðusamningn fyrir kreditbréf.</span><span class="sxs-lookup"><span data-stu-id="8be0c-107">Create a bank facility agreement for a letter of guarantee.</span></span>



<span data-ttu-id="8be0c-108">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="8be0c-108">This procedure uses the USMF demo company.</span></span>


## <a name="create-sales-order-with-letter-of-guarantee"></a><span data-ttu-id="8be0c-109">Stofna Sölupöntun með Ábyrgðarbréf</span><span class="sxs-lookup"><span data-stu-id="8be0c-109">Create Sales Order with Letter of Guarantee</span></span>
1. <span data-ttu-id="8be0c-110">Farið í Viðskiptakröfur > Pantanir > Allar sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="8be0c-110">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="8be0c-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="8be0c-111">Click New.</span></span>
3. <span data-ttu-id="8be0c-112">Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="8be0c-112">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="8be0c-113">Útvíkka eða draga saman hlutann Almennt.</span><span class="sxs-lookup"><span data-stu-id="8be0c-113">Expand the General section.</span></span>
5. <span data-ttu-id="8be0c-114">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="8be0c-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="8be0c-115">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="8be0c-115">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="8be0c-116">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="8be0c-116">In the Warehouse field, enter or select a value.</span></span>
8. <span data-ttu-id="8be0c-117">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="8be0c-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="8be0c-118">Í gerð bankaskjals svæðinu, veljið 'Ábyrgðarbréf'.</span><span class="sxs-lookup"><span data-stu-id="8be0c-118">In the Bank document type field, select 'Letter of guarantee'.</span></span>
10. <span data-ttu-id="8be0c-119">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="8be0c-119">Click OK.</span></span>
11. <span data-ttu-id="8be0c-120">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="8be0c-120">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="8be0c-121">Færið inn númer í reitnum „Einingarverð“.</span><span class="sxs-lookup"><span data-stu-id="8be0c-121">In the Unit price field, enter a number.</span></span>
13. <span data-ttu-id="8be0c-122">Víkkið út hlutann „Upplýsingar um línu“.</span><span class="sxs-lookup"><span data-stu-id="8be0c-122">Expand the Line details section.</span></span>
14. <span data-ttu-id="8be0c-123">Smellið á flipann „Afhending“.</span><span class="sxs-lookup"><span data-stu-id="8be0c-123">Click the Delivery tab.</span></span>
    * <span data-ttu-id="8be0c-124">Athugasemd: Velja stýringu Afhendingardagsetningar = Ekkert</span><span class="sxs-lookup"><span data-stu-id="8be0c-124">Note: Select Delivery date control = None</span></span>  
15. <span data-ttu-id="8be0c-125">Færa inn dagsetningu í reitnum Umbeðinni sendingardagsetningu .</span><span class="sxs-lookup"><span data-stu-id="8be0c-125">In the Requested ship date field, enter a date.</span></span>
16. <span data-ttu-id="8be0c-126">Færa inn dagsetningu í reitnum staðfest sendingardagsetning</span><span class="sxs-lookup"><span data-stu-id="8be0c-126">In the Confirmed ship date field, enter a date.</span></span>

## <a name="process-letter-of-guarantee_request"></a><span data-ttu-id="8be0c-127">Ferli ábyrgðaryfirlýsing_beiðni</span><span class="sxs-lookup"><span data-stu-id="8be0c-127">Process letter of guarantee_Request</span></span>
1. <span data-ttu-id="8be0c-128">Í Aðgerðarrúðunni er smellt á Stjórna.</span><span class="sxs-lookup"><span data-stu-id="8be0c-128">On the Action Pane, click Manage.</span></span>
2. <span data-ttu-id="8be0c-129">Smellt er á Ábyrgðaryfirlýsingar.</span><span class="sxs-lookup"><span data-stu-id="8be0c-129">Click Letter of guarantee.</span></span>
3. <span data-ttu-id="8be0c-130">Á Aðgerðarúðu, smellið á ábyrgðaryfirlýsing.</span><span class="sxs-lookup"><span data-stu-id="8be0c-130">On the Action Pane, click Letter of guarantee.</span></span>
4. <span data-ttu-id="8be0c-131">Smelltu á Beiðni til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8be0c-131">Click Request to open the drop dialog.</span></span>
5. <span data-ttu-id="8be0c-132">Færa inn eða veljið gildi í svæðinu gerð.</span><span class="sxs-lookup"><span data-stu-id="8be0c-132">In the Type field, enter or select a value.</span></span>
6. <span data-ttu-id="8be0c-133">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="8be0c-133">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="8be0c-134">Í reitinn Gildi skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="8be0c-134">In the Value field, enter a number.</span></span>
8. <span data-ttu-id="8be0c-135">Færa inn dagsetningu og tíma í dagsetningarsvæði Gildistíma.</span><span class="sxs-lookup"><span data-stu-id="8be0c-135">In the Expiration date field, enter a date and time.</span></span>
9. <span data-ttu-id="8be0c-136">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8be0c-136">Click OK.</span></span>
10. <span data-ttu-id="8be0c-137">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8be0c-137">Close the page.</span></span>

## <a name="process-letter-of-guarantee_submit-to-bank"></a><span data-ttu-id="8be0c-138">Ferli ábyrgðaryfirlýsing_senda í banka</span><span class="sxs-lookup"><span data-stu-id="8be0c-138">Process letter of guarantee_Submit to bank</span></span>
1. <span data-ttu-id="8be0c-139">Fara í Reiðufé og bankastjórnun > Ábyrgðaryfirlýsingar > Ábyrgðaryfirlýsingar.</span><span class="sxs-lookup"><span data-stu-id="8be0c-139">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
2. <span data-ttu-id="8be0c-140">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="8be0c-140">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8be0c-141">Smellt er á Senda til banka til að opna felligluggi.</span><span class="sxs-lookup"><span data-stu-id="8be0c-141">Click Submit to bank to open the drop dialog.</span></span>
4. <span data-ttu-id="8be0c-142">Færa inn eða veljið gildi í svæðinu bankareikning.</span><span class="sxs-lookup"><span data-stu-id="8be0c-142">In the Bank account field, enter or select a value.</span></span>
5. <span data-ttu-id="8be0c-143">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="8be0c-143">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="8be0c-144">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8be0c-144">Click OK.</span></span>

## <a name="process-letter-of-guarantee_receive-from-bank"></a><span data-ttu-id="8be0c-145">Ferli ábyrgðaryfirlýsing_móttekið frá banka</span><span class="sxs-lookup"><span data-stu-id="8be0c-145">Process letter of guarantee_Receive from bank</span></span>
1. <span data-ttu-id="8be0c-146">Smellt er á Móttekið frá banka til að opna felligluggi</span><span class="sxs-lookup"><span data-stu-id="8be0c-146">Click Receive from bank to open the drop dialog.</span></span>
2. <span data-ttu-id="8be0c-147">Færa inn gildi í reitnum númer banka.</span><span class="sxs-lookup"><span data-stu-id="8be0c-147">In the Bank number field, type a value.</span></span>
    * <span data-ttu-id="8be0c-148">Staðfestið gildin í reiknuðum svæðum Framlegð og Kostnað.</span><span class="sxs-lookup"><span data-stu-id="8be0c-148">Verify the values in the calculated Margin and Expense fields.</span></span>  
3. <span data-ttu-id="8be0c-149">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8be0c-149">Click OK.</span></span>
4. <span data-ttu-id="8be0c-150">Stækka aðgerðasvæðið.</span><span class="sxs-lookup"><span data-stu-id="8be0c-150">Expand the Actions section.</span></span>
    * <span data-ttu-id="8be0c-151">Staðfesta færslu 'Móttekið frá banka'.</span><span class="sxs-lookup"><span data-stu-id="8be0c-151">Verify the 'Receive from bank' record.</span></span>  
5. <span data-ttu-id="8be0c-152">Smellið til að fylgja tenglinum í reitnum Rununúmer færslubókar.</span><span class="sxs-lookup"><span data-stu-id="8be0c-152">Click to follow the link in the Journal batch number field.</span></span>
6. <span data-ttu-id="8be0c-153">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="8be0c-153">Click Lines.</span></span>
    * <span data-ttu-id="8be0c-154">Staðfestið bókun á færslum færslubókar.</span><span class="sxs-lookup"><span data-stu-id="8be0c-154">Verify the posting of journal entries.</span></span>  
7. <span data-ttu-id="8be0c-155">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8be0c-155">Close the page.</span></span>

## <a name="process-letter-of-guarantee_give-to-beneficiary"></a><span data-ttu-id="8be0c-156">Ferli Ábyrgðaryfirlýsingar_veita til rétthafi</span><span class="sxs-lookup"><span data-stu-id="8be0c-156">Process letter of guarantee_Give to beneficiary</span></span>
1. <span data-ttu-id="8be0c-157">Farið í Viðskiptakröfur > Pantanir > Allar sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="8be0c-157">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="8be0c-158">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="8be0c-158">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="8be0c-159">Í Aðgerðarrúðunni er smellt á Stjórna.</span><span class="sxs-lookup"><span data-stu-id="8be0c-159">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="8be0c-160">Smellt er á Ábyrgðaryfirlýsingar.</span><span class="sxs-lookup"><span data-stu-id="8be0c-160">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="8be0c-161">Á Aðgerðarúðu, smellið á ábyrgðaryfirlýsing.</span><span class="sxs-lookup"><span data-stu-id="8be0c-161">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="8be0c-162">Smellt er á Veita rétthafa til að opna felligluggi.</span><span class="sxs-lookup"><span data-stu-id="8be0c-162">Click Give to beneficiary to open the drop dialog.</span></span>
7. <span data-ttu-id="8be0c-163">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8be0c-163">Click OK.</span></span>
8. <span data-ttu-id="8be0c-164">Fara í Reiðufé og bankastjórnun > Ábyrgðaryfirlýsingar > Ábyrgðaryfirlýsingar.</span><span class="sxs-lookup"><span data-stu-id="8be0c-164">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="8be0c-165">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="8be0c-165">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="8be0c-166">Smellt er á Veita rétthafa til að opna felligluggi.</span><span class="sxs-lookup"><span data-stu-id="8be0c-166">Click Give to beneficiary to open the drop dialog.</span></span>
11. <span data-ttu-id="8be0c-167">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8be0c-167">Click OK.</span></span>
12. <span data-ttu-id="8be0c-168">Stækka aðgerðasvæðið.</span><span class="sxs-lookup"><span data-stu-id="8be0c-168">Expand the Actions section.</span></span>
    * <span data-ttu-id="8be0c-169">Villuleita "Gefa rétthafa" færslu.</span><span class="sxs-lookup"><span data-stu-id="8be0c-169">Validate the 'Give to beneficiary' record.</span></span>  

## <a name="process-letter-of-guarantee_increase-value"></a><span data-ttu-id="8be0c-170">Ferli ábyrgðaryfirlýsing_auka gildi</span><span class="sxs-lookup"><span data-stu-id="8be0c-170">Process letter of guarantee_Increase value</span></span>
1. <span data-ttu-id="8be0c-171">Farið í Viðskiptakröfur > Pantanir > Allar sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="8be0c-171">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="8be0c-172">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="8be0c-172">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="8be0c-173">Í Aðgerðarrúðunni er smellt á Stjórna.</span><span class="sxs-lookup"><span data-stu-id="8be0c-173">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="8be0c-174">Smellt er á Ábyrgðaryfirlýsingar.</span><span class="sxs-lookup"><span data-stu-id="8be0c-174">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="8be0c-175">Á Aðgerðarúðu, smellið á ábyrgðaryfirlýsing.</span><span class="sxs-lookup"><span data-stu-id="8be0c-175">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="8be0c-176">Smellt er á auka gildi til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8be0c-176">Click Increase value to open the drop dialog.</span></span>
7. <span data-ttu-id="8be0c-177">Færið inn númer í Gildi til að bæta við svæði.</span><span class="sxs-lookup"><span data-stu-id="8be0c-177">In the Value to add field, enter a number.</span></span>
8. <span data-ttu-id="8be0c-178">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8be0c-178">Click OK.</span></span>
9. <span data-ttu-id="8be0c-179">Fara í Reiðufé og bankastjórnun > Ábyrgðaryfirlýsingar > Ábyrgðaryfirlýsingar.</span><span class="sxs-lookup"><span data-stu-id="8be0c-179">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
10. <span data-ttu-id="8be0c-180">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="8be0c-180">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="8be0c-181">Smellt er á auka gildi til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8be0c-181">Click Increase value to open the drop dialog.</span></span>
12. <span data-ttu-id="8be0c-182">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8be0c-182">Click OK.</span></span>
13. <span data-ttu-id="8be0c-183">Stækka aðgerðasvæðið.</span><span class="sxs-lookup"><span data-stu-id="8be0c-183">Expand the Actions section.</span></span>
    * <span data-ttu-id="8be0c-184">Staðfesta færslu 'Auka gildi'.</span><span class="sxs-lookup"><span data-stu-id="8be0c-184">Verify the 'Increase value' record.</span></span>  
14. <span data-ttu-id="8be0c-185">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="8be0c-185">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="8be0c-186">Smellið til að fylgja tenglinum í reitnum Rununúmer færslubókar.</span><span class="sxs-lookup"><span data-stu-id="8be0c-186">Click to follow the link in the Journal batch number field.</span></span>
16. <span data-ttu-id="8be0c-187">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="8be0c-187">Click Lines.</span></span>
    * <span data-ttu-id="8be0c-188">Staðfesta bókaðar færslur færslubókar.</span><span class="sxs-lookup"><span data-stu-id="8be0c-188">Verify the posted journal entries.</span></span>  

## <a name="process-letter-of-guarantee_liquidate"></a><span data-ttu-id="8be0c-189">Ferli ábyrgðaryfirlýsing_eyða</span><span class="sxs-lookup"><span data-stu-id="8be0c-189">Process letter of guarantee_Liquidate</span></span>
1. <span data-ttu-id="8be0c-190">Farið í Viðskiptakröfur > Pantanir > Allar sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="8be0c-190">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="8be0c-191">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="8be0c-191">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="8be0c-192">Í Aðgerðarrúðunni er smellt á Stjórna.</span><span class="sxs-lookup"><span data-stu-id="8be0c-192">On the Action Pane, click Manage.</span></span>
4. <span data-ttu-id="8be0c-193">Smellt er á Ábyrgðaryfirlýsingar.</span><span class="sxs-lookup"><span data-stu-id="8be0c-193">Click Letter of guarantee.</span></span>
5. <span data-ttu-id="8be0c-194">Á Aðgerðarúðu, smellið á ábyrgðaryfirlýsing.</span><span class="sxs-lookup"><span data-stu-id="8be0c-194">On the Action Pane, click Letter of guarantee.</span></span>
6. <span data-ttu-id="8be0c-195">Smellt er á eyða til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8be0c-195">Click Liquidate to open the drop dialog.</span></span>
7. <span data-ttu-id="8be0c-196">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8be0c-196">Click OK.</span></span>
8. <span data-ttu-id="8be0c-197">Fara í Reiðufé og bankastjórnun > Ábyrgðaryfirlýsingar > Ábyrgðaryfirlýsingar.</span><span class="sxs-lookup"><span data-stu-id="8be0c-197">Go to Cash and bank management > Letters of guarantee > Letters of guarantee.</span></span>
9. <span data-ttu-id="8be0c-198">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="8be0c-198">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="8be0c-199">Smellt er á eyða til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="8be0c-199">Click Liquidate to open the drop dialog.</span></span>
11. <span data-ttu-id="8be0c-200">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="8be0c-200">Click OK.</span></span>
12. <span data-ttu-id="8be0c-201">Stækka aðgerðasvæðið.</span><span class="sxs-lookup"><span data-stu-id="8be0c-201">Expand the Actions section.</span></span>
    * <span data-ttu-id="8be0c-202">Staðfesta „eyða" færslu.</span><span class="sxs-lookup"><span data-stu-id="8be0c-202">Verify the 'Liquidate' record.</span></span>  
13. <span data-ttu-id="8be0c-203">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="8be0c-203">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="8be0c-204">Smellið til að fylgja tenglinum í reitnum Rununúmer færslubókar.</span><span class="sxs-lookup"><span data-stu-id="8be0c-204">Click to follow the link in the Journal batch number field.</span></span>
15. <span data-ttu-id="8be0c-205">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="8be0c-205">Click Lines.</span></span>
    * <span data-ttu-id="8be0c-206">Staðfesta bókaðar færslur færslubókar.</span><span class="sxs-lookup"><span data-stu-id="8be0c-206">Verify the posted journal entries.</span></span>  
16. <span data-ttu-id="8be0c-207">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="8be0c-207">Close the page.</span></span>

