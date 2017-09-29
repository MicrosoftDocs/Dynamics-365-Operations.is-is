--- 
title: Stofna innkaupasamning
description: "Þetta ferli leiðbeinir við stofnun innkaupasamnings."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0d0cc6508071bea3f622bc21f06aa55d2b757b6f
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="3aeec-103">Stofna innkaupasamning</span><span class="sxs-lookup"><span data-stu-id="3aeec-103">Create a purchase agreement</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3aeec-104">Þetta ferli leiðbeinir við stofnun innkaupasamnings.</span><span class="sxs-lookup"><span data-stu-id="3aeec-104">This procedure guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="3aeec-105">Þetta verk myndi yfirleitt gert af innkaupastjóra.</span><span class="sxs-lookup"><span data-stu-id="3aeec-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="3aeec-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="3aeec-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="3aeec-107">Þú Þarft að hafa sett upp flokkanir innkaupasamnings áður en byrjað er.</span><span class="sxs-lookup"><span data-stu-id="3aeec-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="3aeec-108">Þegar Innkaupapöntun er stofnuð og hægt er að nota hana þegar þú stofnar innkaupapöntun, og það afrita skilyrði innkaupasamnings í haus og allar línur í pöntun sem verða fyrir áhrifum af samninginn.</span><span class="sxs-lookup"><span data-stu-id="3aeec-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="3aeec-109">Stofna nýjan innkaupasamning</span><span class="sxs-lookup"><span data-stu-id="3aeec-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="3aeec-110">Fara í Innkaup og uppruni > Innkaupasamningar > Innkaupasamningar.</span><span class="sxs-lookup"><span data-stu-id="3aeec-110">Go to Procurement and sourcing > Purchase agreements > Purchase agreements.</span></span>
2. <span data-ttu-id="3aeec-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="3aeec-111">Click New.</span></span>
3. <span data-ttu-id="3aeec-112">Í reitnum Lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="3aeec-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3aeec-113">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="3aeec-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="3aeec-114">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="3aeec-114">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="3aeec-115">Í reitnum Innkaupasamningur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="3aeec-115">In the Purchase agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="3aeec-116">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="3aeec-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="3aeec-117">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="3aeec-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="3aeec-118">Víkkið út almenna hlutann.</span><span class="sxs-lookup"><span data-stu-id="3aeec-118">Expand the General section.</span></span>
10. <span data-ttu-id="3aeec-119">Dagsetning er rituð í reitinn lokadagur.</span><span class="sxs-lookup"><span data-stu-id="3aeec-119">In the Expiration date field, enter a date.</span></span>
    * <span data-ttu-id="3aeec-120">Þessi lokadagur verður sjálfgefið fyrir allar línur ráðstöfunar og ákvarða hve lengi hver tiltekin ráðstöfun er gild.</span><span class="sxs-lookup"><span data-stu-id="3aeec-120">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  
11. <span data-ttu-id="3aeec-121">Í reitinn Titill skjalsins skal færa inn heiti fyrir innkaupasamninginn.</span><span class="sxs-lookup"><span data-stu-id="3aeec-121">In the Document title field, type a name for your purchase agreement.</span></span>
    * <span data-ttu-id="3aeec-122">Láta svæðið Sjálfgefin ráðstöfun vera stillt til á ráðstöfun afurðarmagns (eða breyta þeim, ef hann er ekki stillt á þetta).</span><span class="sxs-lookup"><span data-stu-id="3aeec-122">Leave the Default commitment field set to Product quantity commitment (or change it if it’s not set to this).</span></span>  
    * <span data-ttu-id="3aeec-123">Sjálfgefin ráðstöfunargildið ákvarðar valkostirnir þínir á samningslínur.</span><span class="sxs-lookup"><span data-stu-id="3aeec-123">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="3aeec-124">Ef ný ráðstöfunargerð er þörf þegar verið er að stofna samningslínur, þarftu að breyta sjálfgefin ráðstöfun í haus.</span><span class="sxs-lookup"><span data-stu-id="3aeec-124">If you need a new commitment type when you’re creating the agreement lines, you need to change the default commitment on the header.</span></span>  <span data-ttu-id="3aeec-125">Til eru 4 Gerðirnar ráðstafana: Ráðstöfun afurðarmagns - fyrir ákveðið magn afurðar; Ráðstöfunarvirði afurðar - fyrir tiltekna gjaldmiðilsupphæð afurðar; Ráðstöfunarvirði vörutegundar - fyrir upphæð í tilteknum gjaldmiðli í innkaupaflokki þar sem upphæðin getur verið fyrir vöru í vörulista eða vöru sem er ekki á vörulista; Ráðstöfunarvirði - fyrir tiltekna gjaldmiðilsupphæð sem getur verið uppfyllt af hvaða vöru eða af hvaða innkaupategund sem er.</span><span class="sxs-lookup"><span data-stu-id="3aeec-125">There are 4 types of commitments: Product quantity commitment - for a specific quantity of a product; Product value commitment - for a specific currency amount of a product; Product category value commitment - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; Value commitment - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  
12. <span data-ttu-id="3aeec-126">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="3aeec-126">Click OK.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="3aeec-127">Bæta við skuldbindingu</span><span class="sxs-lookup"><span data-stu-id="3aeec-127">Add a commitment</span></span>
1. <span data-ttu-id="3aeec-128">Smellið á „Bæta við línu“.</span><span class="sxs-lookup"><span data-stu-id="3aeec-128">Click Add line.</span></span>
2. <span data-ttu-id="3aeec-129">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="3aeec-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="3aeec-130">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="3aeec-130">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3aeec-131">Veljið afurð sem á að bæta ráðstöfun við.</span><span class="sxs-lookup"><span data-stu-id="3aeec-131">Select the product you want to add a commitment for.</span></span>
5. <span data-ttu-id="3aeec-132">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="3aeec-132">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="3aeec-133">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="3aeec-133">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="3aeec-134">Þetta er heildarmagn sem þú hefur samþykkt að kaupa frá lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="3aeec-134">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
7. <span data-ttu-id="3aeec-135">Færið inn númer í reitnum „Einingarverð“.</span><span class="sxs-lookup"><span data-stu-id="3aeec-135">In the Unit price field, enter a number.</span></span>
8. <span data-ttu-id="3aeec-136">Víkkið út hlutann „Upplýsingar um línu“.</span><span class="sxs-lookup"><span data-stu-id="3aeec-136">Expand the Line details section.</span></span>
9. <span data-ttu-id="3aeec-137">Stilla Valkosturinn Hámark er notað á Já.</span><span class="sxs-lookup"><span data-stu-id="3aeec-137">Set the Max is enforced option to Yes.</span></span>
    * <span data-ttu-id="3aeec-138">Valkosturinn Hámark er notað takmarkar notkun á ráðstöfun.</span><span class="sxs-lookup"><span data-stu-id="3aeec-138">The Max is enforced option limits the use of the commitment.</span></span> <span data-ttu-id="3aeec-139">Aðeins er hægt að kaupa upp að því magni sem er tilgreint er í Magnsvæðinu fyrir línuna.</span><span class="sxs-lookup"><span data-stu-id="3aeec-139">You can only purchase up to the quantity that's specified in the Quantity field for the line.</span></span>  
10. <span data-ttu-id="3aeec-140">draga saman hluta upplýsingar Línu.</span><span class="sxs-lookup"><span data-stu-id="3aeec-140">Collapse the Line details section.</span></span>

## <a name="add-header-conditions"></a><span data-ttu-id="3aeec-141">Bæta við fyrirsagnaskilyrði</span><span class="sxs-lookup"><span data-stu-id="3aeec-141">Add header conditions</span></span>
1. <span data-ttu-id="3aeec-142">Í aðgerðasvæðinu er smellt á valkostir.</span><span class="sxs-lookup"><span data-stu-id="3aeec-142">On the Action Pane, click Options.</span></span>
2. <span data-ttu-id="3aeec-143">Smellið á skoða Breytingu.</span><span class="sxs-lookup"><span data-stu-id="3aeec-143">Click Change view.</span></span>
3. <span data-ttu-id="3aeec-144">Smellið á skoða Haus.</span><span class="sxs-lookup"><span data-stu-id="3aeec-144">Click Header view.</span></span>
4. <span data-ttu-id="3aeec-145">Víkka út liðnum skilmálar.</span><span class="sxs-lookup"><span data-stu-id="3aeec-145">Expand the Terms section.</span></span>
5. <span data-ttu-id="3aeec-146">Í reitnum greiðsluaðferð skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="3aeec-146">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="3aeec-147">Greiðsluskilmálar úr lykli lánardrottins eru sýnd hér sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="3aeec-147">The payment terms from the vendor account are shown here by default.</span></span>       
6. <span data-ttu-id="3aeec-148">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="3aeec-148">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="3aeec-149">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="3aeec-149">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="3aeec-150">Í reitnum Afhendingarmáti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="3aeec-150">In the Mode of delivery field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="3aeec-151">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="3aeec-151">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="3aeec-152">Í reitnum Afhendingarskilmálar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="3aeec-152">In the Delivery terms field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="3aeec-153">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="3aeec-153">In the list, click the link in the selected row.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="3aeec-154">Vista og virkja samning</span><span class="sxs-lookup"><span data-stu-id="3aeec-154">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="3aeec-155">Í aðgerðasvæðinu er smellt á innkaupasamningur.</span><span class="sxs-lookup"><span data-stu-id="3aeec-155">On the Action Pane, click Purchase agreement.</span></span>
2. <span data-ttu-id="3aeec-156">Smellt er á Staðfestingu.</span><span class="sxs-lookup"><span data-stu-id="3aeec-156">Click Confirmation.</span></span>
    * <span data-ttu-id="3aeec-157">Stilla valkost Merkja samning sem gildan á Já.</span><span class="sxs-lookup"><span data-stu-id="3aeec-157">Set the Mark agreement as effective option to Yes.</span></span>  
3. <span data-ttu-id="3aeec-158">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="3aeec-158">Click OK.</span></span>
4. <span data-ttu-id="3aeec-159">Í aðgerðasvæðinu er smellt á innkaupasamningur.</span><span class="sxs-lookup"><span data-stu-id="3aeec-159">On the Action Pane, click Purchase agreement.</span></span>
5. <span data-ttu-id="3aeec-160">Smellt er á Staðfestingar innkaupasamnings.</span><span class="sxs-lookup"><span data-stu-id="3aeec-160">Click Purchase agreement confirmations.</span></span>
    * <span data-ttu-id="3aeec-161">valkostur Forskoðun/Prenta gerir kleift að búa til skjal fyrir innkaupasamning sem síðan er hægt að prenta eða senda til lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3aeec-161">The Preview/Print option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="3aeec-162">Ef þú uppfæra samning síðar og staðfesta hann aftur, verða báðar útgáfur sýnd hér.</span><span class="sxs-lookup"><span data-stu-id="3aeec-162">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="3aeec-163">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3aeec-163">Close the page.</span></span>


