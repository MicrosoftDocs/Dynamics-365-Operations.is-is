---
title: Skilgreina þekjureglur fyrir vörur
description: Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.
author: ShylaThompson
manager: tfehr
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9b10aa50c4a89b2642262f624ac3a6d89cd6ebb4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258652"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="299e6-103">Skilgreina þekjureglur fyrir vörur</span><span class="sxs-lookup"><span data-stu-id="299e6-103">Define coverage rules for items</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="299e6-104">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="299e6-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="299e6-105">Þetta ferli sýnir hvernig á að stofna þekjureglur og hnekkja þekjustillingum fyrir tiltekna vöru.</span><span class="sxs-lookup"><span data-stu-id="299e6-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="299e6-106">Hún sýnir einnig hvernig á að tilgreina sjálfgefnar birgðastillingar.</span><span class="sxs-lookup"><span data-stu-id="299e6-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="299e6-107">Stofna þekjuflokk</span><span class="sxs-lookup"><span data-stu-id="299e6-107">Create a coverage group</span></span>
1. <span data-ttu-id="299e6-108">Farðu í **Skoðunarrúðu > Kerfiseiningar > Aðaláætlanagerð > Uppsetning > Þekjuflokkar**.</span><span class="sxs-lookup"><span data-stu-id="299e6-108">Go to **Navigation pane > Modules > Master planning > Setup > Coverage groups**.</span></span>
2. <span data-ttu-id="299e6-109">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="299e6-109">Click **New**.</span></span>
3. <span data-ttu-id="299e6-110">Í reitnum **Þekjuflokkur** slærðu inn gildi.</span><span class="sxs-lookup"><span data-stu-id="299e6-110">In the **Coverage group** field, type a value.</span></span>
4. <span data-ttu-id="299e6-111">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="299e6-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="299e6-112">Í reitinn **Dagatal** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="299e6-112">In the **Calendar** field, type a value.</span></span> <span data-ttu-id="299e6-113">Velja dagatalið sem aðaláætlanagerð notar til að stofna tillögur um áfyllingu fyrir vörur í þessum flokki.</span><span class="sxs-lookup"><span data-stu-id="299e6-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="299e6-114">Í reitnum **Þekjukóði** velurðu valkost.</span><span class="sxs-lookup"><span data-stu-id="299e6-114">In the **Coverage code** field, select an option.</span></span> <span data-ttu-id="299e6-115">Veldu „Þarfir“ fyrir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="299e6-115">Select 'Requirement' for this procedure.</span></span>  
7. <span data-ttu-id="299e6-116">Í reitnum **Tímamörk tryggingar (dagar)** skal slá inn ‚90‘.</span><span class="sxs-lookup"><span data-stu-id="299e6-116">In the **Coverage time fence (days) field**, enter '90'.</span></span> <span data-ttu-id="299e6-117">Fyrir vörur í þessum flokki, mun aðaláætlanagerð stofna tillögur að áfyllingu fyrir upp að 90 daga til framtíðar.</span><span class="sxs-lookup"><span data-stu-id="299e6-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="299e6-118">Í reitinn **Neikvæðir dagar** færirðu inn „1“.</span><span class="sxs-lookup"><span data-stu-id="299e6-118">In the **Negative days** field, enter '1'.</span></span>
9. <span data-ttu-id="299e6-119">Í reitinn **Jákvæðir dagar** færirðu inn „1“.</span><span class="sxs-lookup"><span data-stu-id="299e6-119">In the **Positive days** field, enter '1'.</span></span>
10. <span data-ttu-id="299e6-120">Stækka eða fella saman hlutann **Annað**.</span><span class="sxs-lookup"><span data-stu-id="299e6-120">Expand or collapse the **Other** section.</span></span>
11. <span data-ttu-id="299e6-121">Undir hlutanum **Öryggismörk á dögum**, í reitinn **Mörk innhreyfinga bætt við dagsetningu þarfa**, slærðu inn '1'.</span><span class="sxs-lookup"><span data-stu-id="299e6-121">Under the **Safety margins in days** section, in the **Receipt margin added to requirement date** field, enter '1'.</span></span> <span data-ttu-id="299e6-122">Til dæmis, ef mörk innhreyfinga eru stillt á 1 dag og innkaupapöntunarlína er áætluð til móttöku þann 15. maí reikna mörk innhreyfinga móttökudagsetningu sem 16. maí.</span><span class="sxs-lookup"><span data-stu-id="299e6-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="299e6-123">Í reitnum **Mörk úthreyfinga dregin af dagsetningu þarfa** skal færa inn 1.</span><span class="sxs-lookup"><span data-stu-id="299e6-123">In the **Issue margin deducted from requirement date** field, enter '1'.</span></span> <span data-ttu-id="299e6-124">Til dæmis, ef öryggismörk eru stillt á 1 dag og sölupöntunarlína er áætluð til afhendingar þann 15. maí reiknar röðun leiðrétta móttökudagsetningu sem 14. maí.</span><span class="sxs-lookup"><span data-stu-id="299e6-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="299e6-125">Í svæðinu **Endurpöntunarmagni bætt við afhendingartíma vöru** skal færa inn 1.</span><span class="sxs-lookup"><span data-stu-id="299e6-125">In the **Reorder margin added to item lead time** field, enter '1'.</span></span>
14. <span data-ttu-id="299e6-126">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="299e6-126">Click **Save**.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="299e6-127">Stofna nýja afurð</span><span class="sxs-lookup"><span data-stu-id="299e6-127">Create a new product</span></span>
1. <span data-ttu-id="299e6-128">Farðu í **Skoðunarrúða > Kerfiseiningar > Afurðaupplýsingastjórnun > Afurðir > Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="299e6-128">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="299e6-129">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="299e6-129">Click **New**.</span></span>
3. <span data-ttu-id="299e6-130">Í reitnum **Afurðarnúmer** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="299e6-130">In the **Product number** field, type a value.</span></span>
4. <span data-ttu-id="299e6-131">Í reitinn **Afurðarheiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="299e6-131">In the **Product name** field, type a value.</span></span>
5. <span data-ttu-id="299e6-132">Í reitnum **Vörulíkanaflokkur** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="299e6-132">In the **Item model group** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="299e6-133">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="299e6-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="299e6-134">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="299e6-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="299e6-135">Í reitnum **Vöruflokkur** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="299e6-135">In the **Item group** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="299e6-136">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="299e6-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="299e6-137">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="299e6-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="299e6-138">Í reitnum **Geymsluvíddarflokkur** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="299e6-138">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="299e6-139">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="299e6-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="299e6-140">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="299e6-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="299e6-141">Í reitnum **Rakningarvíddarflokkur** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="299e6-141">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="299e6-142">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="299e6-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="299e6-143">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="299e6-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="299e6-144">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="299e6-144">Click **OK**.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="299e6-145">Setja upp sjálfgefnar pöntunarstillingar</span><span class="sxs-lookup"><span data-stu-id="299e6-145">Setup default order settings</span></span>
1. <span data-ttu-id="299e6-146">Í **Aðgerðarrúðunni** er smellt á **Áætlun**.</span><span class="sxs-lookup"><span data-stu-id="299e6-146">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="299e6-147">Undir **Panta stillingar** smellirðu á **Sjálfgefnar pöntunarstillingar**.</span><span class="sxs-lookup"><span data-stu-id="299e6-147">Under **Order settings**, click **Default order settings**.</span></span>
3. <span data-ttu-id="299e6-148">Undir **Innkaupapöntun**, í reitnum **Sjálfgefið svæði** færirðu inn svæðið sem er notað sem sjálfgefið þegar innkaupapantanir eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="299e6-148">Under **Purchase order**, in the **Default site** field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="299e6-149">Í reitnum **Sjálfgefið vöruhús** skal slá inn staðinn þar sem varan er geymd.</span><span class="sxs-lookup"><span data-stu-id="299e6-149">In the **Default warehouse** field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="299e6-150">Stækka eða fella saman hlutann **Birgðir**.</span><span class="sxs-lookup"><span data-stu-id="299e6-150">Expand or collapse the **Inventory** section.</span></span>
6. <span data-ttu-id="299e6-151">Í reitinn **Margfeldi** skal slá inn „10“.</span><span class="sxs-lookup"><span data-stu-id="299e6-151">In the **Multiple** field, type '10'.</span></span>
7. <span data-ttu-id="299e6-152">Í reitinn **Lágmarksmagn í pöntun** slærðu inn '10'.</span><span class="sxs-lookup"><span data-stu-id="299e6-152">In the **Min. order quantity** field, type '10'.</span></span>
8. <span data-ttu-id="299e6-153">Í reitinn **Hámarksmagn í pöntun** slærðu inn '100'.</span><span class="sxs-lookup"><span data-stu-id="299e6-153">In the **Max. order quantity** field, type '100'.</span></span>
9. <span data-ttu-id="299e6-154">Í reitinn **Staðlað magn í pöntun** slærðu inn '10'.</span><span class="sxs-lookup"><span data-stu-id="299e6-154">In the **Standard order quantity**, type '10'.</span></span>
10. <span data-ttu-id="299e6-155">Í reitinn **Afhendingartími innkaupa** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="299e6-155">In the **Purchase lead time** field, enter a number.</span></span>
11. <span data-ttu-id="299e6-156">Velja skal eða hreinsa gátreitinn **Vinnudagar**.</span><span class="sxs-lookup"><span data-stu-id="299e6-156">Select or clear the **Working days** check box.</span></span>
12. <span data-ttu-id="299e6-157">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="299e6-157">Click **Save**.</span></span>
13. <span data-ttu-id="299e6-158">Í reitnum **Sjálfgefin gerð pöntunar** velurðu „Innkaupapantanir“.</span><span class="sxs-lookup"><span data-stu-id="299e6-158">In the **Default order type** field select 'Purchase order'.</span></span>
14. <span data-ttu-id="299e6-159">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="299e6-159">Click **Save**.</span></span>
15. <span data-ttu-id="299e6-160">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="299e6-160">Close the page.</span></span> <span data-ttu-id="299e6-161">Lokaðu skjámyndinni Sjálfgefnar pöntunarstillingar.</span><span class="sxs-lookup"><span data-stu-id="299e6-161">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="299e6-162">Bæta vöru við þekjuflokk</span><span class="sxs-lookup"><span data-stu-id="299e6-162">Add an item to a coverage group</span></span>
1. <span data-ttu-id="299e6-163">Stækka eða fella saman hlutann **Áætlun**.</span><span class="sxs-lookup"><span data-stu-id="299e6-163">Expand or collapse the **Plan** section.</span></span>
2. <span data-ttu-id="299e6-164">Í reitnum **Þekjuflokkur** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="299e6-164">In the **Coverage group** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="299e6-165">Í listanum finnurðu **Þekjuflokk** sem hefur verið stofnaður.</span><span class="sxs-lookup"><span data-stu-id="299e6-165">In the list, find the **Coverage group** you have created.</span></span>
4. <span data-ttu-id="299e6-166">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="299e6-166">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="299e6-167">Stofna þekjureglur vöru</span><span class="sxs-lookup"><span data-stu-id="299e6-167">Create item coverage rules</span></span>
1. <span data-ttu-id="299e6-168">Í **Aðgerðarrúðunni** er smellt á **Áætlun**.</span><span class="sxs-lookup"><span data-stu-id="299e6-168">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="299e6-169">Undir **Þekja** smellirðu á **Vöruþekju**.</span><span class="sxs-lookup"><span data-stu-id="299e6-169">Under **Coverage**, click **Item coverage**.</span></span>
3. <span data-ttu-id="299e6-170">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="299e6-170">Click **New**.</span></span>
4. <span data-ttu-id="299e6-171">Smelltu á flipann **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="299e6-171">Click the **General** tab.</span></span>
5. <span data-ttu-id="299e6-172">Merkið við gátreitinn í hausnum í stillingunum **Hnekking þekjuflokks**.</span><span class="sxs-lookup"><span data-stu-id="299e6-172">Check the box on the header of **Override coverage group** settings.</span></span>
6. <span data-ttu-id="299e6-173">Í reitnum **Tímamörk tryggingar (dagar)** skal slá inn ‚60‘.</span><span class="sxs-lookup"><span data-stu-id="299e6-173">In the **Coverage time fence (days)** field, enter '60'.</span></span> <span data-ttu-id="299e6-174">Jafnvel þótt vörur í þekjuflokki Þarfir séu áætlaðar 90 daga fram í tímann, verður varan áætluð 60 daga fram í tímann.</span><span class="sxs-lookup"><span data-stu-id="299e6-174">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="299e6-175">Í reitinn **Neikvæðir dagar** færirðu inn „2“.</span><span class="sxs-lookup"><span data-stu-id="299e6-175">In the **Negative days** field, enter '2'.</span></span>
8. <span data-ttu-id="299e6-176">Í reitinn **Jákvæðir dagar** færirðu inn „2“.</span><span class="sxs-lookup"><span data-stu-id="299e6-176">In the **Positive days** field, enter '2'.</span></span>
9. <span data-ttu-id="299e6-177">Smellt er á flipann **Afhendingartími**.</span><span class="sxs-lookup"><span data-stu-id="299e6-177">Click the **Lead time** tab.</span></span>
10. <span data-ttu-id="299e6-178">Merktu í reitinn í haus **Innkaupa**.</span><span class="sxs-lookup"><span data-stu-id="299e6-178">Check the box on the header of **Purchase**.</span></span>
11. <span data-ttu-id="299e6-179">Í reitnum **Innkaupatími** skal slá inn ‚5‘.</span><span class="sxs-lookup"><span data-stu-id="299e6-179">In the **Purchase time** field, enter '5'.</span></span>
12. <span data-ttu-id="299e6-180">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="299e6-180">Click **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]