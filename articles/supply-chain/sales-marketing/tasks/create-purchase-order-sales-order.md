--- 
title: "Stofna innkaupapöntun úr sölupöntun"
description: "Þessi verklýsing sýnir hvernig á að stofna innkaupapöntun sem byggist á sölupöntun."
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 3774943e7147df88be0133c6fc983df54ca70f35
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="18c9d-103">Stofna innkaupapöntun úr sölupöntun</span><span class="sxs-lookup"><span data-stu-id="18c9d-103">Create a purchase order from a sales order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="18c9d-104">Þessi verklýsing sýnir hvernig á að stofna innkaupapöntun sem byggist á sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="18c9d-104">This procedure shows you how to create a purchase order that is based on a sales order.</span></span> <span data-ttu-id="18c9d-105">Magn afurðarinnar á innkaupapöntuninni eru síðan hannaðir til að uppfylla eftirspurn upphaflegrar sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="18c9d-105">The product's quantities on the purchase order are then designated to fulfill the demand of the originating sales order.</span></span> <span data-ttu-id="18c9d-106">Uppfylling þannig að sölueftirspurn er annar valkostur við yfirgripsmeiri og bestuð aðferð við Dreifingu Kröfum Áætlanagerðar.</span><span class="sxs-lookup"><span data-stu-id="18c9d-106">Fulfilling sales demand this way is an alternative to a more comprehensive and optimized method of Distribution Requirements Planning.</span></span> <span data-ttu-id="18c9d-107">Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.</span><span class="sxs-lookup"><span data-stu-id="18c9d-107">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="18c9d-108">Stofna innkaupapöntun úr sölupöntun</span><span class="sxs-lookup"><span data-stu-id="18c9d-108">Create a purchase order from a sales order</span></span>
1. <span data-ttu-id="18c9d-109">Fara í Sölu og markaðssetningu > sölupöntun > Allar sölupantanir</span><span class="sxs-lookup"><span data-stu-id="18c9d-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="18c9d-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="18c9d-110">Click New.</span></span>
3. <span data-ttu-id="18c9d-111">Í reitnum Reikningur viðskiptavina skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="18c9d-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="18c9d-112">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="18c9d-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="18c9d-113">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="18c9d-113">Click OK.</span></span>
6. <span data-ttu-id="18c9d-114">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="18c9d-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="18c9d-115">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="18c9d-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="18c9d-116">Ef verið er að nota USMF, var hægt að velja D0001.</span><span class="sxs-lookup"><span data-stu-id="18c9d-116">If you're using USMF, you could select D0001.</span></span>  
8. <span data-ttu-id="18c9d-117">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="18c9d-117">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="18c9d-118">Smellið á „Bæta við línu“.</span><span class="sxs-lookup"><span data-stu-id="18c9d-118">Click Add line.</span></span>
10. <span data-ttu-id="18c9d-119">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="18c9d-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="18c9d-120">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="18c9d-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="18c9d-121">Ef verið er að nota USMF, var hægt að velja T0020.</span><span class="sxs-lookup"><span data-stu-id="18c9d-121">If you're using USMF, you could select T0020.</span></span>  
12. <span data-ttu-id="18c9d-122">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="18c9d-122">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="18c9d-123">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="18c9d-123">In the Quantity field, enter a number.</span></span>
14. <span data-ttu-id="18c9d-124">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="18c9d-124">Click Save.</span></span>
15. <span data-ttu-id="18c9d-125">Smellið á „Sölupöntun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="18c9d-125">On the Action Pane, click Sales order.</span></span>
16. <span data-ttu-id="18c9d-126">Smellt er á Innkaupapöntunarlína.</span><span class="sxs-lookup"><span data-stu-id="18c9d-126">Click Purchase order.</span></span>
    * <span data-ttu-id="18c9d-127">Stofna innkaupapöntunarsíðu sýnir allar opnar sölupöntunarlínurnar sem afritað er úr sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="18c9d-127">The Create purchase order page lists all the open sales order lines which have been copied from the sales order.</span></span> <span data-ttu-id="18c9d-128">Hægt er að skoða upplýsingar um pöntun, og ef þörf krefur, er hægt að breyta völdum upplýsingum um slíkar innkaupamagn og verðskilmálar áður en hægt er að stofna innkaup .</span><span class="sxs-lookup"><span data-stu-id="18c9d-128">You can review the order details, and if required, you can modify selected details such purchase quantity and pricing terms, before you create the purchases.</span></span>  
17. <span data-ttu-id="18c9d-129">Veljið valkostinn er Taka allar með</span><span class="sxs-lookup"><span data-stu-id="18c9d-129">Select the Include all option.</span></span>
    * <span data-ttu-id="18c9d-130">Ef mynda á innkaupapöntun fyrir aðeins hlutmengi sölupöntunarlínur, veljið þær sérstaklega.</span><span class="sxs-lookup"><span data-stu-id="18c9d-130">If you want to generate purchase orders for only a subset of the sales order lines, select these individually.</span></span>  
    * <span data-ttu-id="18c9d-131">Svæðið fyrir reikninga Lánardrottins getur eða ekki þegar vera með númer lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="18c9d-131">The Vendor account field may or may not already be populated with a vendor number.</span></span> <span data-ttu-id="18c9d-132">Ef sjálfgefinn lánardrottinn er sett upp fyrir afurðina (á tengda vöruþekju) þessi lánardrottinn verða afritaðar í línuna.</span><span class="sxs-lookup"><span data-stu-id="18c9d-132">If the default vendor is set up for the product (on the associated Item coverage) then this vendor will be copied  to the line.</span></span> <span data-ttu-id="18c9d-133">Annars þarf að færa lánardrottinn handvirkt.</span><span class="sxs-lookup"><span data-stu-id="18c9d-133">Otherwise, you must enter a vendor manually.</span></span>  <span data-ttu-id="18c9d-134">Í þessari handbók, óháð því hvort svæðið Lánardrottins þegar inniheldur gildi eða ekki, eftirfarandi skref sýna hvernig á að velja nýja lánardrottins sem eru mismunandi fyrir hverja línu.</span><span class="sxs-lookup"><span data-stu-id="18c9d-134">In this guide, regardless of whether the Vendor account field already contains a value or not, the following steps instruct you to select a new vendor which is different for each line.</span></span>  
18. <span data-ttu-id="18c9d-135">Í reitnum Lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="18c9d-135">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="18c9d-136">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="18c9d-136">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="18c9d-137">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="18c9d-137">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="18c9d-138">Veljið pöntunarlínu númer tvö.</span><span class="sxs-lookup"><span data-stu-id="18c9d-138">Select the second order line.</span></span>
22. <span data-ttu-id="18c9d-139">Í reitnum Lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="18c9d-139">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="18c9d-140">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="18c9d-140">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="18c9d-141">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="18c9d-141">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="18c9d-142">Smella á Villuleita.</span><span class="sxs-lookup"><span data-stu-id="18c9d-142">Click Validate.</span></span>
26. <span data-ttu-id="18c9d-143">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="18c9d-143">Click OK.</span></span>
    * <span data-ttu-id="18c9d-144">Skilaboðin tilkynnir þér að ein eða fleiri innkaupapantanir hafa verið stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="18c9d-144">The message informs you that one or more purchase orders have been created.</span></span> <span data-ttu-id="18c9d-145">Kerfið myndar til aðskilda innkaupapöntun fyrir hvern lánardrottin sem tilgreindur er í sölupöntunarlínum.</span><span class="sxs-lookup"><span data-stu-id="18c9d-145">The system generates a separate purchase order for each vendor that you specified for the sales order lines.</span></span> <span data-ttu-id="18c9d-146">Þetta þýðir að ef margar sölupöntunarlínur eiga að vera frá sama lánardrottni, eina innkaupapöntun fyrir með margar línur eru mynduð.</span><span class="sxs-lookup"><span data-stu-id="18c9d-146">This means that if several sales order lines are to be supplied by the same vendor, a single purchase order with multiple lines will be generated.</span></span>  

## <a name="review-purchase-orders-created-from-sales-orders"></a><span data-ttu-id="18c9d-147">Yfirfara innkaupapantanir stofnaðar úr sölupantana</span><span class="sxs-lookup"><span data-stu-id="18c9d-147">Review purchase orders created from sales orders</span></span>
1. <span data-ttu-id="18c9d-148">Smellið á „Almennt“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="18c9d-148">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="18c9d-149">Smellt er á Tengdar pantanir.</span><span class="sxs-lookup"><span data-stu-id="18c9d-149">Click Related orders.</span></span>
    * <span data-ttu-id="18c9d-150">Tengdar pantanir síða inniheldur lista yfir allar pantanir sem voru stofnaðar úr sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="18c9d-150">The Related orders page lists all the orders that were created from the sales order.</span></span> <span data-ttu-id="18c9d-151">Í þessu dæmi eru tvær innkaupapantanir búnar til fyrir tveimur mismunandi lánardrottnum í þessari röð.</span><span class="sxs-lookup"><span data-stu-id="18c9d-151">In this example, there are two purchase orders generated for two different vendors respectively.</span></span>  
3. <span data-ttu-id="18c9d-152">Smellið til að velja tengilinn í reitnum Innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="18c9d-152">Click to follow the link in the Purchase order field.</span></span>
    * <span data-ttu-id="18c9d-153">Hvert innkaupapöntunarlína er tengd sölupöntunarlína sem leiddi til innkaupanna.</span><span class="sxs-lookup"><span data-stu-id="18c9d-153">Each purchase order line is associated with the sales order line that led to the purchase.</span></span> <span data-ttu-id="18c9d-154">Vensl á sölupöntun er tilgreint á afurðaflipanum í flýtiflipi línuupplýsingar, í svæðunum tilvísunargerð, tilvísunarnúmer og tilvísunarlota.</span><span class="sxs-lookup"><span data-stu-id="18c9d-154">The relation to the sales order is indicated on the Product tab in the Line details FastTab, in the Reference type, Reference number, and Reference lot fields.</span></span>  
4. <span data-ttu-id="18c9d-155">Útvíkka eða draga saman hluta upplýsingar Línu.</span><span class="sxs-lookup"><span data-stu-id="18c9d-155">Expand or collapse the Line details section.</span></span>
5. <span data-ttu-id="18c9d-156">Smellið á flipann Afurðar.</span><span class="sxs-lookup"><span data-stu-id="18c9d-156">Click the Product tab.</span></span>
    * <span data-ttu-id="18c9d-157">Tilvísunarlota tryggir að kostnaður úr núgildandi Innkaup eru gjaldfærð á viðhengda sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="18c9d-157">The Reference lot guarantees that the costs from the current purchase are charged on the attached sales order.</span></span>  
    * <span data-ttu-id="18c9d-158">Hægt er að fara á upprunalegri sölupöntun með því að opna tengil í svæðinu Tilvísunarnúmer.</span><span class="sxs-lookup"><span data-stu-id="18c9d-158">You can navigate to the originating sales order by opening the link in the Reference number field.</span></span>  


