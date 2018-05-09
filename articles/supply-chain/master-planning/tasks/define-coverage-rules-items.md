--- 
title: "Skilgreina þekjureglur fyrir vörur"
description: "Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF."
author: YuyuScheller
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3205fe6a10ce714073334c7ccd25acb755e0aebf
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="d98e2-103">Skilgreina þekjureglur fyrir vörur</span><span class="sxs-lookup"><span data-stu-id="d98e2-103">Define coverage rules for items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d98e2-104">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="d98e2-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d98e2-105">Þetta ferli sýnir hvernig á að stofna þekjureglur og hnekkja þekjustillingum fyrir tiltekna vöru.</span><span class="sxs-lookup"><span data-stu-id="d98e2-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="d98e2-106">Hún sýnir einnig hvernig á að tilgreina sjálfgefnar birgðastillingar.</span><span class="sxs-lookup"><span data-stu-id="d98e2-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="d98e2-107">Stofna þekjuflokk</span><span class="sxs-lookup"><span data-stu-id="d98e2-107">Create a coverage group</span></span>
1. <span data-ttu-id="d98e2-108">Fara í þekjuflokka.</span><span class="sxs-lookup"><span data-stu-id="d98e2-108">Go to Coverage groups.</span></span>
2. <span data-ttu-id="d98e2-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d98e2-109">Click New.</span></span>
3. <span data-ttu-id="d98e2-110">Færa inn gildi í svæðinu Þekjuflokkur.</span><span class="sxs-lookup"><span data-stu-id="d98e2-110">In the Coverage group field, type a value.</span></span>
4. <span data-ttu-id="d98e2-111">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d98e2-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d98e2-112">Í reitinn Dagatal skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d98e2-112">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="d98e2-113">Velja dagatalið sem aðaláætlanagerð notar til að stofna tillögur um áfyllingu fyrir vörur í þessum flokki.</span><span class="sxs-lookup"><span data-stu-id="d98e2-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="d98e2-114">Veljið valkost í svæðinu Þekjukóði.</span><span class="sxs-lookup"><span data-stu-id="d98e2-114">In the Coverage code field, select an option.</span></span>
    * <span data-ttu-id="d98e2-115">Veljið Þarfir fyrir þessa færslu.</span><span class="sxs-lookup"><span data-stu-id="d98e2-115">Select Requirement for this procedure.</span></span>  
7. <span data-ttu-id="d98e2-116">Í reitnum Tímamörk tryggingar (dagar) skal slá inn ‚90‘.</span><span class="sxs-lookup"><span data-stu-id="d98e2-116">In the Coverage time fence (days) field, enter '90'.</span></span>
    * <span data-ttu-id="d98e2-117">Fyrir vörur í þessum flokki, mun aðaláætlanagerð stofna tillögur að áfyllingu fyrir upp að 90 daga til framtíðar.</span><span class="sxs-lookup"><span data-stu-id="d98e2-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="d98e2-118">Fært er inn 1 í reitinn Neikvætt Dagar.</span><span class="sxs-lookup"><span data-stu-id="d98e2-118">In the Negative days field, enter '1'.</span></span>
9. <span data-ttu-id="d98e2-119">Fært er inn 1 í reitinn Jákvætt Dagar.</span><span class="sxs-lookup"><span data-stu-id="d98e2-119">In the Positive days field, enter '1'.</span></span>
10. <span data-ttu-id="d98e2-120">Stækka eða fella saman hlutann Annað.</span><span class="sxs-lookup"><span data-stu-id="d98e2-120">Expand or collapse the Other section.</span></span>
11. <span data-ttu-id="d98e2-121">Í svæðinu Mörk innhreyfinga bætt við dagsetningu þarfa, færðu inn 1.</span><span class="sxs-lookup"><span data-stu-id="d98e2-121">In the Receipt margin added to requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="d98e2-122">Til dæmis, ef mörk innhreyfinga eru stillt á 1 dag og innkaupapöntunarlína er áætluð til móttöku þann 15. maí reikna mörk innhreyfinga móttökudagsetningu sem 16. maí.</span><span class="sxs-lookup"><span data-stu-id="d98e2-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="d98e2-123">Í svæðinu Mörk úthreyfinga dregin af dagsetningu þarfa skal færa inn 1.</span><span class="sxs-lookup"><span data-stu-id="d98e2-123">In the Issue margin deducted from requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="d98e2-124">Til dæmis, ef öryggismörk eru stillt á 1 dag og sölupöntunarlína er áætluð til afhendingar þann 15. maí reiknar röðun leiðrétta móttökudagsetningu sem 14. maí.</span><span class="sxs-lookup"><span data-stu-id="d98e2-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="d98e2-125">Í svæðinu Endurpöntunarmagni bætt við afhendingartíma vöru skal færa inn 1.</span><span class="sxs-lookup"><span data-stu-id="d98e2-125">In the Reorder margin added to item lead time field, enter '1'.</span></span>
14. <span data-ttu-id="d98e2-126">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d98e2-126">Click Save.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="d98e2-127">Stofna nýja afurð</span><span class="sxs-lookup"><span data-stu-id="d98e2-127">Create a new product</span></span>
1. <span data-ttu-id="d98e2-128">Farðu í Losaðar afurðir.</span><span class="sxs-lookup"><span data-stu-id="d98e2-128">Go to Released products.</span></span>
2. <span data-ttu-id="d98e2-129">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d98e2-129">Click New.</span></span>
3. <span data-ttu-id="d98e2-130">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d98e2-130">In the Product number field, type a value.</span></span>
4. <span data-ttu-id="d98e2-131">Sláið inn gildi í reitinn Afurðarheiti.</span><span class="sxs-lookup"><span data-stu-id="d98e2-131">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="d98e2-132">Í reitnum Vörulíkanaflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="d98e2-132">In the Item model group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="d98e2-133">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d98e2-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="d98e2-134">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d98e2-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="d98e2-135">Í reitnum Vöruflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="d98e2-135">In the Item group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="d98e2-136">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d98e2-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="d98e2-137">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d98e2-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="d98e2-138">Í reitnum Geymsluvíddarflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="d98e2-138">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="d98e2-139">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d98e2-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="d98e2-140">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d98e2-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="d98e2-141">Í reitnum Rakningarvíddarflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="d98e2-141">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="d98e2-142">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="d98e2-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="d98e2-143">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d98e2-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="d98e2-144">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d98e2-144">Click OK.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="d98e2-145">Setja upp sjálfgefnar pöntunarstillingar</span><span class="sxs-lookup"><span data-stu-id="d98e2-145">Setup default order settings</span></span>
1. <span data-ttu-id="d98e2-146">Smellið á „Áætlun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="d98e2-146">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="d98e2-147">Smellt er á sjálfgefnar pöntunarstillingar.</span><span class="sxs-lookup"><span data-stu-id="d98e2-147">Click Default order settings.</span></span>
3. <span data-ttu-id="d98e2-148">Í svæðinu innkaupasvæði, færðu inn svæðið sem er notað sem sjálfgefið þegar innkaupapantanir eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="d98e2-148">In the Purchase site field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="d98e2-149">Í reitnum Birgðasvæði skal slá inn staðinn þar sem varan er geymd.</span><span class="sxs-lookup"><span data-stu-id="d98e2-149">In the Inventory site field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="d98e2-150">Stækka eða fella saman hlutann Birgðir.</span><span class="sxs-lookup"><span data-stu-id="d98e2-150">Expand or collapse the Inventory section.</span></span>
6. <span data-ttu-id="d98e2-151">Margir er stillt á '10'.</span><span class="sxs-lookup"><span data-stu-id="d98e2-151">Set Multiple to '10'.</span></span>
7. <span data-ttu-id="d98e2-152">Setja lágm.</span><span class="sxs-lookup"><span data-stu-id="d98e2-152">Set Min.</span></span> <span data-ttu-id="d98e2-153">pöntunarmagn á ‚10‘.</span><span class="sxs-lookup"><span data-stu-id="d98e2-153">order quantity to '10'.</span></span>
8. <span data-ttu-id="d98e2-154">Setja Hám.</span><span class="sxs-lookup"><span data-stu-id="d98e2-154">Set Max.</span></span> <span data-ttu-id="d98e2-155">pöntunarmagn á ‚100‘.</span><span class="sxs-lookup"><span data-stu-id="d98e2-155">order quantity to '100'.</span></span>
9. <span data-ttu-id="d98e2-156">Stilltu staðlað pöntunarmagn á ‚10‘.</span><span class="sxs-lookup"><span data-stu-id="d98e2-156">Set Standard order quantity to '10'.</span></span>
10. <span data-ttu-id="d98e2-157">Í reitinn Afhendingartími innkaupa skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="d98e2-157">In the Purchase lead time field, enter a number.</span></span>
11. <span data-ttu-id="d98e2-158">Velja skal eða hreinsa gátreitinn Vinnudagar.</span><span class="sxs-lookup"><span data-stu-id="d98e2-158">Select or clear the Working days check box.</span></span>
12. <span data-ttu-id="d98e2-159">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d98e2-159">Click Save.</span></span>
13. <span data-ttu-id="d98e2-160">Í reitnum sjálfgefin gerð pöntunar velurðu „Innkaupapantanir“.</span><span class="sxs-lookup"><span data-stu-id="d98e2-160">In the Default order type field select 'Purchase order'.</span></span>
14. <span data-ttu-id="d98e2-161">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d98e2-161">Click Save.</span></span>
15. <span data-ttu-id="d98e2-162">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d98e2-162">Close the page.</span></span>
    * <span data-ttu-id="d98e2-163">Lokaðu skjámyndinni Sjálfgefnar pöntunarstillingar.</span><span class="sxs-lookup"><span data-stu-id="d98e2-163">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="d98e2-164">Bæta vöru við þekjuflokk</span><span class="sxs-lookup"><span data-stu-id="d98e2-164">Add an item to a coverage group</span></span>
1. <span data-ttu-id="d98e2-165">Stækka eða fella saman hlutann Áætlun.</span><span class="sxs-lookup"><span data-stu-id="d98e2-165">Expand or collapse the Plan section.</span></span>
2. <span data-ttu-id="d98e2-166">Í reitnum Þekjuflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="d98e2-166">In the Coverage group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="d98e2-167">Í listanum, Finna þekjuflokk sem hafa verið stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="d98e2-167">In the list, find the Coverage group you have created.</span></span>
4. <span data-ttu-id="d98e2-168">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="d98e2-168">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="d98e2-169">Stofna þekjureglur vöru</span><span class="sxs-lookup"><span data-stu-id="d98e2-169">Create item coverage rules</span></span>
1. <span data-ttu-id="d98e2-170">Smellið á „Áætlun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="d98e2-170">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="d98e2-171">Smellt er á vöruþekju.</span><span class="sxs-lookup"><span data-stu-id="d98e2-171">Click Item coverage.</span></span>
3. <span data-ttu-id="d98e2-172">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d98e2-172">Click New.</span></span>
4. <span data-ttu-id="d98e2-173">Smellið á flipann „Almennt“.</span><span class="sxs-lookup"><span data-stu-id="d98e2-173">Click the General tab.</span></span>
5. <span data-ttu-id="d98e2-174">Merkið við gátreitinn á haus Hnekking þekjuflokks.</span><span class="sxs-lookup"><span data-stu-id="d98e2-174">Check the box on the header of Override coverage group settings.</span></span>
6. <span data-ttu-id="d98e2-175">Í reitnum Tímamörk tryggingar (dagar) skal slá inn ‚60‘.</span><span class="sxs-lookup"><span data-stu-id="d98e2-175">In the Coverage time fence (days) field, enter '60'.</span></span>
    * <span data-ttu-id="d98e2-176">Jafnvel þótt vörur í þekjuflokki Þarfir séu áætlaðar 90 daga fram í tímann, verður varan áætluð 60 daga fram í tímann.</span><span class="sxs-lookup"><span data-stu-id="d98e2-176">Although items in coverage group Requirement are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="d98e2-177">Fært er inn 2 í reitinn Neikvætt Dagar.</span><span class="sxs-lookup"><span data-stu-id="d98e2-177">In the Negative days field, enter '2'.</span></span>
8. <span data-ttu-id="d98e2-178">Fært er inn 2 í reitinn Jákvætt Dagar.</span><span class="sxs-lookup"><span data-stu-id="d98e2-178">In the Positive days field, enter '2'.</span></span>
9. <span data-ttu-id="d98e2-179">Smellt er á flipanum afhendingartími.</span><span class="sxs-lookup"><span data-stu-id="d98e2-179">Click the Lead time tab.</span></span>
10. <span data-ttu-id="d98e2-180">Merktu í reitinn í haus Innkaupa.</span><span class="sxs-lookup"><span data-stu-id="d98e2-180">Check the box on the header of Purchase.</span></span>
11. <span data-ttu-id="d98e2-181">Í reitnum Innkaupatími skal slá inn ‚5‘.</span><span class="sxs-lookup"><span data-stu-id="d98e2-181">In the Purchase time field, enter '5'.</span></span>
12. <span data-ttu-id="d98e2-182">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d98e2-182">Click Save.</span></span>


