--- 
title: "Lykilgögn reiknings í AP kerfið með því að nota reikning lánardrottins"
description: "Þessar verkefnaleiðbeiningar hjálpa notandanum að stofna reikning lánardrottins og skoða niðurstöður jöfnunar á innkaupapöntun, kvittun og reikningi (þríhliða jöfnun)."
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e1d2e31a5de7cefd20996c18bf4771296a587997
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---
# <a name="key-invoice-data-in-ap-system-using-vendor-invoice"></a><span data-ttu-id="bcbeb-103">Lykilgögn reiknings í AP kerfið með því að nota reikning lánardrottins</span><span class="sxs-lookup"><span data-stu-id="bcbeb-103">Key invoice data in AP system using vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bcbeb-104">Þessar verkefnaleiðbeiningar hjálpa notandanum að stofna reikning lánardrottins og skoða niðurstöður jöfnunar á innkaupapöntun, kvittun og reikningi (þríhliða jöfnun).</span><span class="sxs-lookup"><span data-stu-id="bcbeb-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="bcbeb-105">Stofna innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="bcbeb-105">Create a purchase order</span></span>
1. <span data-ttu-id="bcbeb-106">Fara í Viðskiptaskuldir > Innkaupapantanir > Allar innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-106">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="bcbeb-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-107">Click New.</span></span>
3. <span data-ttu-id="bcbeb-108">Í reitnum Lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-108">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bcbeb-109">Finna lánardrottin til að velja.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-109">Find a vendor to select.</span></span> <span data-ttu-id="bcbeb-110">Til dæmis fletta niður að US-104.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="bcbeb-111">Velja lánardrottin US-104</span><span class="sxs-lookup"><span data-stu-id="bcbeb-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="bcbeb-112">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-112">Click OK.</span></span>
7. <span data-ttu-id="bcbeb-113">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-113">In the Item number field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="bcbeb-114">Velja birgðavöru.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-114">Select an inventory item.</span></span> <span data-ttu-id="bcbeb-115">Til dæmis, veljið vörunúmerið 1000.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="bcbeb-116">Útvíkka eða draga saman hluta upplýsingar Línu.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-116">Expand or collapse the Line details section.</span></span>
10. <span data-ttu-id="bcbeb-117">Smellið á flipann „Setja upp“.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-117">Click the Setup tab.</span></span>
    * <span data-ttu-id="bcbeb-118">Hægt er að hnekkja jöfnunarreglunni til að nota enga jöfnun, tvíhliða jöfnun eða þríhliða jöfnun.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-118">You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="bcbeb-119">Útvíkka eða draga saman hluta upplýsingar Línu.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-119">Expand or collapse the Line details section.</span></span>
12. <span data-ttu-id="bcbeb-120">Smellið á „Innkaup“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-120">On the Action Pane, click Purchase.</span></span>
13. <span data-ttu-id="bcbeb-121">Smellið á „Staðfesta“.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-121">Click Confirm.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="bcbeb-122">Taka við vörunum</span><span class="sxs-lookup"><span data-stu-id="bcbeb-122">Receive the products</span></span>
1. <span data-ttu-id="bcbeb-123">Smellið á „Móttaka“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-123">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="bcbeb-124">Smellið á „Innhreyfingarskjal“.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-124">Click Product receipt.</span></span>
3. <span data-ttu-id="bcbeb-125">Færið inn innhreyfingarskjalsnúmerið á svæðinu „Innhreyfingarskjal“.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-125">In the Product receipt field, enter the product receipt number.</span></span> <span data-ttu-id="bcbeb-126">Til dæmis er slegið inn „PR123“.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-126">For example, enter PR123.</span></span>
4. <span data-ttu-id="bcbeb-127">Smellið á „Í lagi“ til að bóka innhreyfingarskjalið.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-127">Click OK to post the product receipt.</span></span>
5. <span data-ttu-id="bcbeb-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-128">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="bcbeb-129">Stofna reikning lánardrottins</span><span class="sxs-lookup"><span data-stu-id="bcbeb-129">Create a vendor invoice</span></span>
1. <span data-ttu-id="bcbeb-130">Farið í Viðskiptaskuldir > Innkaupapantanir > Mótteknar óreikningsfærðar innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-130">Go to Accounts payable > Purchase orders > Purchase orders received but not invoiced.</span></span>
2. <span data-ttu-id="bcbeb-131">Velja innkaupapöntun sem var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-131">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="bcbeb-132">Í aðgerðasvæðinu er smellt á reikningur.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-132">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="bcbeb-133">Smellt er á Reikningnum.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-133">Click Invoice.</span></span>
5. <span data-ttu-id="bcbeb-134">Færið inn númer reiknings á númerasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-134">In the Number field, enter the invoice number.</span></span>
6. <span data-ttu-id="bcbeb-135">Sláið inn gildi á svæðinu „Reikningslýsing“.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-135">In the Invoice description field, type a value.</span></span>
7. <span data-ttu-id="bcbeb-136">Færið inn dagsetningu á svæðinu „Reikningsdagsetning“.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-136">In the Invoice date field, enter a date.</span></span>
8. <span data-ttu-id="bcbeb-137">Í reitnum einingarverð er fært inn 1200.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-137">In the Unit price field, enter 1200.</span></span>
9. <span data-ttu-id="bcbeb-138">Smella á bæta Við línu.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-138">Click Add line.</span></span>
10. <span data-ttu-id="bcbeb-139">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-139">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="bcbeb-140">Finna vörunúmer uppsetningargjalda á listanum.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-140">In the list, find the installation charge item number.</span></span> <span data-ttu-id="bcbeb-141">Til dæmis S0001</span><span class="sxs-lookup"><span data-stu-id="bcbeb-141">For example, S0001</span></span>
12. <span data-ttu-id="bcbeb-142">Veljið vörunúmer uppsetningargjalda.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-142">Select the installation charge item number.</span></span>
    * <span data-ttu-id="bcbeb-143">Athugið að jöfnun hefur ekki verið framkvæmd síðan breytingarnar voru gerðar.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-143">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="bcbeb-144">Smellið á „Uppfæra samsvörunarstöðu“.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-144">Click Update match status.</span></span>
14. <span data-ttu-id="bcbeb-145">Smellið á „Yfirfara“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-145">On the Action Pane, click Review.</span></span>
15. <span data-ttu-id="bcbeb-146">Smellið á „Samsvörunarupplýsingar“.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-146">Click Matching details.</span></span>
    * <span data-ttu-id="bcbeb-147">Ný lína með þjónustu þarf ekki að vera jafnað svo staðan segi "Ekki framkvæmt".</span><span class="sxs-lookup"><span data-stu-id="bcbeb-147">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="bcbeb-148">Velja innhreyfingarskjal afurða fyrir birgðavöruna sem er móttekin.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-148">Select the product receipt for the inventory item that you received.</span></span>
    * <span data-ttu-id="bcbeb-149">Línan með innhreyfingarskjalinu var jöfnuð en ósamræmi er í magni eða verði svo það mistókst.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-149">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="bcbeb-150">Færið inn númer í reitnum „Einingarverð“.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-150">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="bcbeb-151">Þegar einingaverðið hefur verið jafnað uppfærist staðan í „Stóðst“.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-151">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="bcbeb-152">Ef reglan leyfir misræmi eða ef jöfnun er aðeins viðvörun er samt hægt að bóka reikninginn.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-152">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="bcbeb-153">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-153">Close the page.</span></span>
19. <span data-ttu-id="bcbeb-154">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-154">Click Post.</span></span>
20. <span data-ttu-id="bcbeb-155">Lokaðu skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-155">Close the form.</span></span>
    * <span data-ttu-id="bcbeb-156">Athugið að innkaupapöntunin er ekki lengur skráð sem móttekin en ekki reikningsfærð.</span><span class="sxs-lookup"><span data-stu-id="bcbeb-156">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  


