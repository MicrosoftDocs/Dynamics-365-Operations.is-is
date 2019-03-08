---
title: Færa inn og bera saman kauptilboð vegna beiðni um TILBOÐ og veita aðilum samninga.
description: Þessi verklýsing sýnir hvernig á að færa inn svör við Tilboðsbeiðni, gefa stig og bera saman tilboð, og veita síðan einum lánardrottninum kauptilboðið.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchRFQCaseTable, PurchRFQReplyTable, PurchRFQCompare, PurchRFQEditLines, PurchRFQEditLinesParameters, PurchTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7cd4876acfebcc9595abb358cfc9b355e93041d6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "349999"
---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a><span data-ttu-id="463be-103">Færa inn og bera saman kauptilboð vegna beiðni um TILBOÐ og veita aðilum samninga.</span><span class="sxs-lookup"><span data-stu-id="463be-103">Enter and compare RFQ bids, and award contracts</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="463be-104">Þessi verklýsing sýnir hvernig á að færa inn svör við Tilboðsbeiðni, gefa stig og bera saman tilboð, og veita síðan einum lánardrottninum kauptilboðið.</span><span class="sxs-lookup"><span data-stu-id="463be-104">This procedure shows you how to enter replies to an RFQ, score and compare bids, and then award the bid to one of the vendors.</span></span> <span data-ttu-id="463be-105">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="463be-105">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="463be-106">Áður en byrjað er, verður að hafa beiðni um TILBOÐ með tveimur línum sem hefur verið send til a.m.k. tveimur lánardrottnum.</span><span class="sxs-lookup"><span data-stu-id="463be-106">Before you start, you must have an RFQ with two lines that has been sent to at least two vendors.</span></span> <span data-ttu-id="463be-107">Hægt er að keyra ferlinu "Stofna beiðni um tilboð" sem forsendu til að stofna þessi.</span><span class="sxs-lookup"><span data-stu-id="463be-107">You can run the "Create a request for quotation" procedure as a prerequisite to create this.</span></span> <span data-ttu-id="463be-108">Það Þarf að vera uppsettur skilyrði fyrir stigagjöf áður en þessari ferli er keyrð.</span><span class="sxs-lookup"><span data-stu-id="463be-108">You need to have set up scoring criteria before you can run this procedure.</span></span>


## <a name="enter-a-reply-from-a-vendor"></a><span data-ttu-id="463be-109">Færa skal inn svar frá lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="463be-109">Enter a reply from a vendor</span></span>
1. <span data-ttu-id="463be-110">Fara í innkaup og aðföng  > Beiðnir um tilboð  > Allar beiðnir um tilboð.</span><span class="sxs-lookup"><span data-stu-id="463be-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="463be-111">Veljið beiðni um TILBOÐ sem er með stöðuna Sent og smella á tengilinn fyrir málsnúmer Beiðni um tilboð.</span><span class="sxs-lookup"><span data-stu-id="463be-111">Select an RFQ that has a status of Sent and click the link on the Request for quotation case number.</span></span>
    * <span data-ttu-id="463be-112">Beiðni um TILBOÐ hefði átt að senda til í það minnsta 2 lánardrottna .</span><span class="sxs-lookup"><span data-stu-id="463be-112">The RFQ should have been sent to at least 2 vendors.</span></span>  
3. <span data-ttu-id="463be-113">Smellt er á Hausnum til að fara í lista yfir lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="463be-113">Click Header to go to the list of vendors.</span></span>
4. <span data-ttu-id="463be-114">Velja skal lánardrottin til að sem færa á svar inn fyrir á beiðni um tilboð.</span><span class="sxs-lookup"><span data-stu-id="463be-114">Select the vendor for whom you want to enter a response on the RFQ.</span></span>
5. <span data-ttu-id="463be-115">Smella á Færa inn svar</span><span class="sxs-lookup"><span data-stu-id="463be-115">Click Enter reply.</span></span>
6. <span data-ttu-id="463be-116">Smellið á Svara á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="463be-116">On the Action Pane, click Reply.</span></span>
7. <span data-ttu-id="463be-117">Smella á Afrita gögn til að svara.</span><span class="sxs-lookup"><span data-stu-id="463be-117">Click Copy data to reply.</span></span>
    * <span data-ttu-id="463be-118">Þessi aðgerð mun afrita valda gögn, t.d. magnið frá BUT-verki í svar við tilboðsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="463be-118">This action will copy selected data, for example, the quantity from the RFQ case to the RFQ reply.</span></span> <span data-ttu-id="463be-119">Einnig hægt að sleppa þessari aðgerð og fylla inn í öll svæði fyrir svör handvirkt þegar svari er breytt.</span><span class="sxs-lookup"><span data-stu-id="463be-119">Alternatively you can skip this action and fill in all the response fields manually when you edit the reply.</span></span>  
8. <span data-ttu-id="463be-120">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="463be-120">Click Edit.</span></span>
9. <span data-ttu-id="463be-121">Færið inn númer í reitnum „Einingarverð“.</span><span class="sxs-lookup"><span data-stu-id="463be-121">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="463be-122">Velja hina tilboðslínuna.</span><span class="sxs-lookup"><span data-stu-id="463be-122">Choose the other quotation line.</span></span>
11. <span data-ttu-id="463be-123">Færið inn númer í reitnum „Einingarverð“.</span><span class="sxs-lookup"><span data-stu-id="463be-123">In the Unit price field, enter a number.</span></span>

## <a name="score-the-bid"></a><span data-ttu-id="463be-124">Gefa kauptilboði stig.</span><span class="sxs-lookup"><span data-stu-id="463be-124">Score the bid</span></span>
1. <span data-ttu-id="463be-125">Smellt er á Hausnum til að fara í stigagjöf tilboða.</span><span class="sxs-lookup"><span data-stu-id="463be-125">Click Header to go to the scoring of the bid.</span></span>
2. <span data-ttu-id="463be-126">Útvíkka stigagjöf fyrir Kauptilboðið hluta.</span><span class="sxs-lookup"><span data-stu-id="463be-126">Expand the Bid scoring section.</span></span>
3. <span data-ttu-id="463be-127">Færið inn númer fyrir eitt skilyrði fyrir stigagjöf í svæðinu Stigagjöf.</span><span class="sxs-lookup"><span data-stu-id="463be-127">In the Score field, enter a number for one of the scoring criteria.</span></span>
    * <span data-ttu-id="463be-128">Ef þú hefur músabendil yfir skilyrði fyrir stigagjöf kemur ábending sem sýnir bil sem þarf hafa stig innan.</span><span class="sxs-lookup"><span data-stu-id="463be-128">If you hover over one of the scoring criteria a tooltip shows the range that you have to score within.</span></span> <span data-ttu-id="463be-129">Hægt er að bæta tölu á bilinu 1 til 5 við hvert þessara skilyrða í þessari sýnigögn.</span><span class="sxs-lookup"><span data-stu-id="463be-129">In this demo you can add a number between 1 and 5 to any of the criteria.</span></span>  
4. <span data-ttu-id="463be-130">Veljið annað skilyrði fyrir stigagjöf.</span><span class="sxs-lookup"><span data-stu-id="463be-130">Select another scoring criterion.</span></span>
5. <span data-ttu-id="463be-131">Í reitinn Stigafjöldi skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="463be-131">In the Score field, enter a number.</span></span>
6. <span data-ttu-id="463be-132">Útvikka liðnum Spurningalisti.</span><span class="sxs-lookup"><span data-stu-id="463be-132">Expand the Questionnaires section.</span></span>
    * <span data-ttu-id="463be-133">Ef BUT-verk er með spurningalista sem var send til lánardrottna er hægt að færa inn svör þeirra í hlutanum spurningalisti.</span><span class="sxs-lookup"><span data-stu-id="463be-133">If the RFQ case has a questionnaire that was sent to the vendors, you can enter their responses in the questionnaire section.</span></span>  
7. <span data-ttu-id="463be-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="463be-134">Close the page.</span></span>

## <a name="enter-a-reply-for-another-vendor"></a><span data-ttu-id="463be-135">Færa inn svar fyrir aðra lánardrottins</span><span class="sxs-lookup"><span data-stu-id="463be-135">Enter a reply for another vendor</span></span>
1. <span data-ttu-id="463be-136">Veljið næsta lánardrottins með því að hreinsa lánardrottin sem verið var að færa inn svar fyrir og velja svo línu fyrir næsta lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="463be-136">Select the next vendor by clearing the vendor you have just entered the reply for and then selecting the row for the next vendor.</span></span>
2. <span data-ttu-id="463be-137">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="463be-137">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="463be-138">Smella á Færa inn svar</span><span class="sxs-lookup"><span data-stu-id="463be-138">Click Enter reply.</span></span>
4. <span data-ttu-id="463be-139">Smella á Afrita gögn til að svara.</span><span class="sxs-lookup"><span data-stu-id="463be-139">Click Copy data to reply.</span></span>
5. <span data-ttu-id="463be-140">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="463be-140">Click Edit.</span></span>
6. <span data-ttu-id="463be-141">Færið inn númer í reitnum „Einingarverð“.</span><span class="sxs-lookup"><span data-stu-id="463be-141">In the Unit price field, enter a number.</span></span>
7. <span data-ttu-id="463be-142">Velja hina tilboðslínuna.</span><span class="sxs-lookup"><span data-stu-id="463be-142">Choose the other quotation line.</span></span>
8. <span data-ttu-id="463be-143">Færið inn númer í reitnum „Einingarverð“.</span><span class="sxs-lookup"><span data-stu-id="463be-143">In the Unit price field, enter a number.</span></span>

## <a name="score-the-second-bid"></a><span data-ttu-id="463be-144">Gefa öðru kauptilboði stig.</span><span class="sxs-lookup"><span data-stu-id="463be-144">Score the second bid</span></span>
1. <span data-ttu-id="463be-145">Smellt er á Hausnum til að fara í stigagjöf tilboða.</span><span class="sxs-lookup"><span data-stu-id="463be-145">Click Header to go to scoring of the bid.</span></span>
2. <span data-ttu-id="463be-146">Í reitinn Stigafjöldi skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="463be-146">In the Score field, enter a number.</span></span>
3. <span data-ttu-id="463be-147">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="463be-147">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="463be-148">Í reitinn Stigafjöldi skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="463be-148">In the Score field, enter a number.</span></span>

## <a name="compare-the-replies"></a><span data-ttu-id="463be-149">Bera saman svör</span><span class="sxs-lookup"><span data-stu-id="463be-149">Compare the replies</span></span>
1. <span data-ttu-id="463be-150">Smellið á „Almennt“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="463be-150">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="463be-151">Smella á Bera saman svör</span><span class="sxs-lookup"><span data-stu-id="463be-151">Click Compare replies.</span></span>
3. <span data-ttu-id="463be-152"> - Færið númer inn í svæðið stigagjöf.</span><span class="sxs-lookup"><span data-stu-id="463be-152">In the Rank field, enter a number.</span></span>
    * <span data-ttu-id="463be-153">Þessi síða sýnir tilboð með haus og línur, og heildarstigafjölda á hausstigi.</span><span class="sxs-lookup"><span data-stu-id="463be-153">This page shows the bids with the header and lines, and the total score on the header level.</span></span> <span data-ttu-id="463be-154">Hægt er að bera saman línum með því að raða í hnitanetinu þannig samanburðarhæfar línur eru hlið við hlið.</span><span class="sxs-lookup"><span data-stu-id="463be-154">You can compare the lines by sorting in the grid so that comparable lines are next to each other.</span></span> <span data-ttu-id="463be-155">Upplýsingar innihalda einnig: Magn: magn sem uppgefið er af lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="463be-155">The information also includes:   Quantity: The quantity quoted by the vendor.</span></span> <span data-ttu-id="463be-156">Þetta gæti ekki verið það sama og magnið í beiðninni um tilboð.</span><span class="sxs-lookup"><span data-stu-id="463be-156">This might not equal the quantity specified in the RFQ.</span></span>   <span data-ttu-id="463be-157">Nettóupphæð – Verð gefið upp af lánardrottni, að frádregnum öllum afsláttum, fyrir vörurnar á línunni.</span><span class="sxs-lookup"><span data-stu-id="463be-157">Net amount: The price quoted by a vendor, after subtracting any discounts, for the items on the line.</span></span>   <span data-ttu-id="463be-158">Frávik – Fjöldi daga sem munar á afhendingardagsetningu í tilboðshaus eða tilboðslínu og umbeðnum afhendingardegi í RFQ-haus eða RFQ-línu.</span><span class="sxs-lookup"><span data-stu-id="463be-158">Deviation: The number of days that the delivery date in the bid header or line deviates from the requested delivery date in the RFQ header or RFQ line.</span></span>   <span data-ttu-id="463be-159">Fyrir hvert tilboð er hægt að færa inn forgangsröðun:</span><span class="sxs-lookup"><span data-stu-id="463be-159">You can enter a rank for each bid.</span></span>  
4. <span data-ttu-id="463be-160">Veljið haus línu fyrir hitt tilboðið sem þú ætlar að gefa stig.</span><span class="sxs-lookup"><span data-stu-id="463be-160">Select the header line for the other bid that you want to rank.</span></span>
5. <span data-ttu-id="463be-161"> - Færið númer inn í svæðið stigagjöf.</span><span class="sxs-lookup"><span data-stu-id="463be-161">In the Rank field, enter a number.</span></span>
6. <span data-ttu-id="463be-162">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="463be-162">Click Save.</span></span>

## <a name="reject-a-bid"></a><span data-ttu-id="463be-163">Hafna tilboði</span><span class="sxs-lookup"><span data-stu-id="463be-163">Reject a bid</span></span>
1. <span data-ttu-id="463be-164">Veljið haus línu fyrir hitt tilboðið sem þú ætlar að hafna.</span><span class="sxs-lookup"><span data-stu-id="463be-164">Select the header line for the bid that you want to reject.</span></span>
    * <span data-ttu-id="463be-165">Aðeins er hægt að samþykkja, hafna eða skila einu tilboði eða línu innan eins kauptilboðs í einu.</span><span class="sxs-lookup"><span data-stu-id="463be-165">You can only accept, reject, or return one bid or lines within one bid at a time.</span></span>  
2. <span data-ttu-id="463be-166">Veldu gátreitinn Merkja.</span><span class="sxs-lookup"><span data-stu-id="463be-166">Select the Mark check box.</span></span>
    * <span data-ttu-id="463be-167">Ef Merkja gátreitur er merktur á hausi kauptilboðs þá verða allar línurnar merktar líka.</span><span class="sxs-lookup"><span data-stu-id="463be-167">If you select the Mark check box on the Header of the bid then all the lines will be marked as well.</span></span> <span data-ttu-id="463be-168">Einnig mætti velja að merkja hlutmengi línanna innan kauptilboðs til að hafna eða samþykkja þær.</span><span class="sxs-lookup"><span data-stu-id="463be-168">You could also choose to mark a subset of the lines within the bid to reject or accept those.</span></span> <span data-ttu-id="463be-169">Hægt er að samþykkja kauptilboð eins lánardrottins í sumar línur í beiðni um tilboð og síðan veita öðrum línum í beiðni um tilboð til annars lánardrottins, hins vegar þarf að gera þetta í 2 skrefum, eitt tilboð í einu.</span><span class="sxs-lookup"><span data-stu-id="463be-169">It’s possible to accept one vendor’s bid for some lines of an RFQ, and then award other RFQ lines to a different vendor, however you need to do this in 2 steps, one bid at a time.</span></span> <span data-ttu-id="463be-170">Ef aðrar línur eru til staðar er aðeins hægt að samþykkja annaðhvort upprunalegu kauptilboðslínunni eða valkostarlínu, en ekki bæði.</span><span class="sxs-lookup"><span data-stu-id="463be-170">If alternate lines are present, you can only accept either the original bid line or its alternate, but not both.</span></span>  
3. <span data-ttu-id="463be-171">Smellt er á Hafna.</span><span class="sxs-lookup"><span data-stu-id="463be-171">Click Reject.</span></span>
4. <span data-ttu-id="463be-172">Smelltu á Færibreytur til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="463be-172">Click Parameters to open the drop dialog.</span></span>
5. <span data-ttu-id="463be-173">Sláið inn eða veldu gildi í reitnum ástæða fyrir höfnun.</span><span class="sxs-lookup"><span data-stu-id="463be-173">In the Reason reject field, enter or select a value.</span></span>
    * <span data-ttu-id="463be-174">Ástæðan fyrir höfnun verður geymd í svarinu.</span><span class="sxs-lookup"><span data-stu-id="463be-174">The reason for rejection will be stored on the reply.</span></span>  
6. <span data-ttu-id="463be-175">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="463be-175">Click OK.</span></span>
7. <span data-ttu-id="463be-176">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="463be-176">Click OK.</span></span>
8. <span data-ttu-id="463be-177">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="463be-177">Close the page.</span></span>
9. <span data-ttu-id="463be-178">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="463be-178">Close the page.</span></span>
10. <span data-ttu-id="463be-179">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="463be-179">Refresh the page.</span></span>

## <a name="accept-a-bid"></a><span data-ttu-id="463be-180">Samþykkja tilboð</span><span class="sxs-lookup"><span data-stu-id="463be-180">Accept a bid</span></span>
1. <span data-ttu-id="463be-181">Veljið tilboð sem á að samþykkja og smellið síðan á tengilinn í svæðinu Beiðni um tilboð.</span><span class="sxs-lookup"><span data-stu-id="463be-181">Select the bid that you want to accept and then click the link in the Request for quotation field.</span></span>
2. <span data-ttu-id="463be-182">Smellið á Svara á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="463be-182">On the Action Pane, click Reply.</span></span>
3. <span data-ttu-id="463be-183">Smellið á Samþykkja.</span><span class="sxs-lookup"><span data-stu-id="463be-183">Click Accept.</span></span>
    * <span data-ttu-id="463be-184">Ef merkt hefur verið við tilteknar línur en ekki aðrar þá mun samþykktaraðgerðin aðeins innihalda merktar línur.</span><span class="sxs-lookup"><span data-stu-id="463be-184">If you have marked specific lines and not others then the accept action will only include the marked lines.</span></span> <span data-ttu-id="463be-185">Ef óskað er að samþykkja allar línur á kauptilboði þá þarft ekki að merkja línur.</span><span class="sxs-lookup"><span data-stu-id="463be-185">If you want to accept all lines on the bid then you do not have to mark the lines.</span></span>  
4. <span data-ttu-id="463be-186">Smelltu á Færibreytur til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="463be-186">Click Parameters to open the drop dialog.</span></span>
    * <span data-ttu-id="463be-187">Þannig er hægt að skrá ástæðu fyrir samþykkt tilboðsins.</span><span class="sxs-lookup"><span data-stu-id="463be-187">This allows you to record a reason for accepting the bid.</span></span> <span data-ttu-id="463be-188">Ástæðan verður geymd í tilboðinu.</span><span class="sxs-lookup"><span data-stu-id="463be-188">The reason will be stored on the bid.</span></span>  
5. <span data-ttu-id="463be-189">Í reitinn ástæða samþykkis skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="463be-189">In the Reason accept field, enter or select a value.</span></span>
6. <span data-ttu-id="463be-190">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="463be-190">Click OK.</span></span>
7. <span data-ttu-id="463be-191">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="463be-191">Click OK.</span></span>
    * <span data-ttu-id="463be-192">Þegar smellt er á í lagi myndar þetta innkaupapöntun byggða á línum sem eru innifaldar í samþykkt á beiðni um TILBOÐ.</span><span class="sxs-lookup"><span data-stu-id="463be-192">When you click OK this generates a purchase order based on the lines that are included in the RFQ acceptance.</span></span> <span data-ttu-id="463be-193">Ef önnur tilboð sem hafa ekki verið unnar eru til staðar (samþykkt, hafnað eða skilað) mun kerfið biðja notandann um að hafna eftirstandandi tilboðum.</span><span class="sxs-lookup"><span data-stu-id="463be-193">If there are other bids that have not been processed (accepted, rejected, or returned) then the system will prompt you to reject the remaining bids.</span></span>  

## <a name="view-the-purchase-order-thats-been-generated"></a><span data-ttu-id="463be-194">Skoða innkaupapöntun sem hefur verið mynduð.</span><span class="sxs-lookup"><span data-stu-id="463be-194">View the purchase order that's been generated</span></span>
1. <span data-ttu-id="463be-195">Smellið á „Almennt“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="463be-195">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="463be-196">Smellt er á Innkaupapöntunarlína.</span><span class="sxs-lookup"><span data-stu-id="463be-196">Click Purchase order.</span></span>
    * <span data-ttu-id="463be-197">Hér er hægt að sjá innkaupapöntun sem var mynduð þegar tilboðið var samþykkt.</span><span class="sxs-lookup"><span data-stu-id="463be-197">Here you can see the purchase order that was generated when you accepted the bid.</span></span>  
3. <span data-ttu-id="463be-198">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="463be-198">Close the page.</span></span>
4. <span data-ttu-id="463be-199">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="463be-199">Close the page.</span></span>
5. <span data-ttu-id="463be-200">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="463be-200">Close the page.</span></span>
6. <span data-ttu-id="463be-201">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="463be-201">Close the page.</span></span>

