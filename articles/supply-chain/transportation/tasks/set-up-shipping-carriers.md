---
title: Setja upp farmflytjendur
description: Í þessu efnisatriði er lýst hvernig eigi að setja upp flytjanda og skilgreina upplýsingar eins og þjónustu, afhendingarmáta sendingar, flutningstilboð, takmarkanir fyrir flutningsstöðu og flutningstaxta.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c5ac13d17c97f20ee79e7faf57c570f02158424
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "314487"
---
# <a name="set-up-shipping-carriers"></a><span data-ttu-id="01bf6-103">Setja upp farmflytjendur</span><span class="sxs-lookup"><span data-stu-id="01bf6-103">Set up shipping carriers</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="01bf6-104">Í þessu efnisatriði er lýst hvernig eigi að setja upp flytjanda og skilgreina upplýsingar eins og þjónustu, afhendingarmáta sendingar, flutningstilboð, takmarkanir fyrir flutningsstöðu og flutningstaxta.</span><span class="sxs-lookup"><span data-stu-id="01bf6-104">This procedure shows how to set up a shipping carrier and define details such as service, shipment mode, transportation tender, transportation constraints, and shipping rate.</span></span> <span data-ttu-id="01bf6-105">Samræmingaraðili við flutninga getur þá úthluta farmflytjanda á hleðslu á inn eða útleið.</span><span class="sxs-lookup"><span data-stu-id="01bf6-105">A transportation coordinator can then assign a shipping carrier to an inbound or outbound load.</span></span>


## <a name="create-a-new-shipping-carrier"></a><span data-ttu-id="01bf6-106">Stofna nýtt farmflytjandi</span><span class="sxs-lookup"><span data-stu-id="01bf6-106">Create a new shipping carrier</span></span>
1. <span data-ttu-id="01bf6-107">Farið í flutningsstjórnun > Uppsetning > Flutningsaðilar > Farmflytjendur.</span><span class="sxs-lookup"><span data-stu-id="01bf6-107">Go to Transportation management > Setup > Carriers > Shipping carriers.</span></span>
2. <span data-ttu-id="01bf6-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="01bf6-108">Click New.</span></span>
3. <span data-ttu-id="01bf6-109">Í reitnum farmflytjandi skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="01bf6-109">In the Shipping carrier field, type a value.</span></span>
4. <span data-ttu-id="01bf6-110">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="01bf6-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="01bf6-111">Í reitnum Hamur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="01bf6-111">In the Mode field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="01bf6-112">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="01bf6-112">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="01bf6-113">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="01bf6-113">In the list, click the link in the selected row.</span></span>

## <a name="fill-in-the-general-information-for-the-shipping-carrier"></a><span data-ttu-id="01bf6-114">Fyllið inn almennar upplýsingar um farmflytjanda</span><span class="sxs-lookup"><span data-stu-id="01bf6-114">Fill in the general information for the shipping carrier</span></span>
1. <span data-ttu-id="01bf6-115">Víxla útvíkkun á liðnum yfirlit.</span><span class="sxs-lookup"><span data-stu-id="01bf6-115">Toggle the expansion of the Overview section.</span></span>
2. <span data-ttu-id="01bf6-116">Kanna eða afhaka Virkja flutningsaðila sendingu gátreit .</span><span class="sxs-lookup"><span data-stu-id="01bf6-116">Check or uncheck the Activate shipping carrier checkbox.</span></span>
3. <span data-ttu-id="01bf6-117">Í reitnum lánardrottinn skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="01bf6-117">In the Vendor field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="01bf6-118">Veljið lánardrottnalykil sem á að úthluta farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="01bf6-118">Select the vendor account to assign the shipping carrier to.</span></span>  
4. <span data-ttu-id="01bf6-119">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="01bf6-119">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="01bf6-120">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="01bf6-120">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="01bf6-121">Veljið valkost í svæðinu greiðslumátii flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="01bf6-121">In the Transportation tender type field, select an option.</span></span>
    * <span data-ttu-id="01bf6-122">Veljið Handvirkt til að nota Tilboðssíðu flutninga eða velja EDI til að uppfæra tilboð með því að nota Rafræna gagnamillifærslu (EDI).</span><span class="sxs-lookup"><span data-stu-id="01bf6-122">Select Manual to use the Transportation Tender page, or select EDI to update the tender by using Electronic Data Interchange (EDI).</span></span>  
7. <span data-ttu-id="01bf6-123">Merkja eða afmerkja gátreitinn Virkja mat á farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="01bf6-123">Check or uncheck the Activate carrier rating checkbox.</span></span>

## <a name="create-the-necessary-services-for-the-shipping-carrier"></a><span data-ttu-id="01bf6-124">Stofna nauðsynlega þjónustuna fyrir farmflytjanda</span><span class="sxs-lookup"><span data-stu-id="01bf6-124">Create the necessary services for the shipping carrier</span></span>
1. <span data-ttu-id="01bf6-125">Víxla útvíkkun á liðnum þjónustur.</span><span class="sxs-lookup"><span data-stu-id="01bf6-125">Toggle the expansion of the Services section.</span></span>
2. <span data-ttu-id="01bf6-126">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="01bf6-126">Click New.</span></span>
3. <span data-ttu-id="01bf6-127">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="01bf6-127">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="01bf6-128">Í reitinn flutningsþjónusta skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="01bf6-128">In the Carrier service field, type a value.</span></span>
5. <span data-ttu-id="01bf6-129">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="01bf6-129">In the Name field, type a value.</span></span>
6. <span data-ttu-id="01bf6-130">Í reitnum flutningsaðferð skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="01bf6-130">In the Transportation method field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="01bf6-131">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="01bf6-131">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="01bf6-132">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="01bf6-132">In the list, click the link in the selected row.</span></span>

## <a name="set-up-the-address-for-the-carrier-optional"></a><span data-ttu-id="01bf6-133">Setja upp aðsetur fyrir flutningsaðila (valfrjálst)</span><span class="sxs-lookup"><span data-stu-id="01bf6-133">Set up the address for the carrier (optional)</span></span>
1. <span data-ttu-id="01bf6-134">Víxla útvíkkun á liðnum heimilisföng.</span><span class="sxs-lookup"><span data-stu-id="01bf6-134">Toggle the expansion of the Addresses section.</span></span>
2. <span data-ttu-id="01bf6-135">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="01bf6-135">Click New.</span></span>
3. <span data-ttu-id="01bf6-136">Færa inn gildi í reitnum Nafn eða lýsing.</span><span class="sxs-lookup"><span data-stu-id="01bf6-136">In the Name or description field, type a value.</span></span>
4. <span data-ttu-id="01bf6-137">Í reitnum land/svæði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="01bf6-137">In the Country/region field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="01bf6-138">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="01bf6-138">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="01bf6-139">Í reitnum Póstnúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="01bf6-139">In the ZIP/postal code field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="01bf6-140">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="01bf6-140">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="01bf6-141">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="01bf6-141">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="01bf6-142">Í reitinn Gata skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="01bf6-142">In the Street field, type a value.</span></span>
10. <span data-ttu-id="01bf6-143">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="01bf6-143">Click OK.</span></span>

## <a name="set-up-the-rating-profile-for-the-shipping-carrier"></a><span data-ttu-id="01bf6-144">Setja upp taxtaforstilling fyrir farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="01bf6-144">Set up the rating profile for the shipping carrier</span></span>
1. <span data-ttu-id="01bf6-145">Víxla útvíkkun á liðnum taxtaforstillingar.</span><span class="sxs-lookup"><span data-stu-id="01bf6-145">Toggle the expansion of the Rating profiles section.</span></span>
2. <span data-ttu-id="01bf6-146">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="01bf6-146">Click New.</span></span>
3. <span data-ttu-id="01bf6-147">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="01bf6-147">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="01bf6-148">Í reitinn taxtaforstilling skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="01bf6-148">In the Rating profile field, type a value.</span></span>
5. <span data-ttu-id="01bf6-149">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="01bf6-149">In the Name field, type a value.</span></span>
6. <span data-ttu-id="01bf6-150">Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="01bf6-150">In the Site field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="01bf6-151">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="01bf6-151">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="01bf6-152">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="01bf6-152">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="01bf6-153">Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="01bf6-153">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="01bf6-154">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="01bf6-154">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="01bf6-155">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="01bf6-155">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="01bf6-156">Í reitnum taxtavél skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="01bf6-156">In the Rate engine field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="01bf6-157">Veljið taxtavél sem er í samræmi við samning sem á að hafa með farmflytjanda.</span><span class="sxs-lookup"><span data-stu-id="01bf6-157">Select the Rate engine that is in accordance with the contract that you have with the carrier.</span></span>  
13. <span data-ttu-id="01bf6-158">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="01bf6-158">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="01bf6-159">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="01bf6-159">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="01bf6-160">Í reitnum taxtasniðmát skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="01bf6-160">In the Rate master field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="01bf6-161">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="01bf6-161">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="01bf6-162">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="01bf6-162">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="01bf6-163">Í reitnum flutningstímavél skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="01bf6-163">In the Transit time engine field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="01bf6-164">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="01bf6-164">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="01bf6-165">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="01bf6-165">Click Save.</span></span>

