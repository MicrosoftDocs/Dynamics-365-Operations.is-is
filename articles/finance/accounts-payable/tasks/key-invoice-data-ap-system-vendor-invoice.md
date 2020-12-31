---
title: Lykilgögn reiknings í AP með því að nota reikning lánardrottins
description: Þessar verkefnaleiðbeiningar hjálpa notandanum að stofna reikning lánardrottins og skoða niðurstöður jöfnunar á innkaupapöntun, kvittun og reikningi (þríhliða jöfnun).
author: abruer
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines, VendEditInvoice, InventItemIdLookupSimple, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f80c88b7fb3542f624d233f670cd7cd6ccd48b94
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444218"
---
# <a name="key-invoice-data-in-ap-using-a-vendor-invoice"></a><span data-ttu-id="acb27-103">Lykilgögn reiknings í AP með því að nota reikning lánardrottins</span><span class="sxs-lookup"><span data-stu-id="acb27-103">Key invoice data in AP using a vendor invoice</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="acb27-104">Þessar verkefnaleiðbeiningar hjálpa notandanum að stofna reikning lánardrottins og skoða niðurstöður jöfnunar á innkaupapöntun, kvittun og reikningi (þríhliða jöfnun).</span><span class="sxs-lookup"><span data-stu-id="acb27-104">This task guide will help you create a vendor invoice from a purchase order and view the results of matching the purchase order, receipt, and invoice (3 way matching).</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="acb27-105">Stofna innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="acb27-105">Create a purchase order</span></span>
1. <span data-ttu-id="acb27-106">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Viðskiptaskuldir > Innkaupapantanir > Allar innkaupapantanir**.</span><span class="sxs-lookup"><span data-stu-id="acb27-106">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="acb27-107">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="acb27-107">Click **New**.</span></span>
3. <span data-ttu-id="acb27-108">Í reitnum **Lánardrottnalykill** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="acb27-108">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="acb27-109">Finna lánardrottin til að velja.</span><span class="sxs-lookup"><span data-stu-id="acb27-109">Find a vendor to select.</span></span> <span data-ttu-id="acb27-110">Til dæmis fletta niður að US-104.</span><span class="sxs-lookup"><span data-stu-id="acb27-110">For example, scroll down to US-104.</span></span>
5. <span data-ttu-id="acb27-111">Velja lánardrottin US-104</span><span class="sxs-lookup"><span data-stu-id="acb27-111">Select vendor US-104.</span></span>
6. <span data-ttu-id="acb27-112">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="acb27-112">Click **OK**.</span></span>
7. <span data-ttu-id="acb27-113">Í reitnum **Vörunúmer** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="acb27-113">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="acb27-114">Velja birgðavöru.</span><span class="sxs-lookup"><span data-stu-id="acb27-114">Select an inventory item.</span></span> <span data-ttu-id="acb27-115">Til dæmis, veljið vörunúmerið 1000.</span><span class="sxs-lookup"><span data-stu-id="acb27-115">For example, select item number 1000.</span></span>
9. <span data-ttu-id="acb27-116">Útvíkkaðu flýtiflipann **Upplýsingar um línur**.</span><span class="sxs-lookup"><span data-stu-id="acb27-116">Expand the **Line details** fastTab.</span></span>
10. <span data-ttu-id="acb27-117">Smelltu á flipann **Uppsetning**. Hægt er að hnekkja jöfnunarreglunni til að nota enga jöfnun, tvíhliða jöfnun eða þríhliða jöfnun.</span><span class="sxs-lookup"><span data-stu-id="acb27-117">Click the **Setup** tab. You can override the matching policy to use no matching, 2-way matching, or 3-way matching.</span></span>  
11. <span data-ttu-id="acb27-118">Í aðgerðasvæðinu skal smella á **Innkaup**.</span><span class="sxs-lookup"><span data-stu-id="acb27-118">On the Action Pane, click **Purchase**.</span></span>
12. <span data-ttu-id="acb27-119">Smellið á **Staðfesta**.</span><span class="sxs-lookup"><span data-stu-id="acb27-119">Click **Confirm**.</span></span>

## <a name="receive-the-products"></a><span data-ttu-id="acb27-120">Taka við vörunum</span><span class="sxs-lookup"><span data-stu-id="acb27-120">Receive the products</span></span>
1. <span data-ttu-id="acb27-121">Í aðgerðasvæðinu skal smella á **Móttaka**.</span><span class="sxs-lookup"><span data-stu-id="acb27-121">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="acb27-122">Smellið á **Innhreyfingarskjal afurða**.</span><span class="sxs-lookup"><span data-stu-id="acb27-122">Click **Product receipt**.</span></span>
3. <span data-ttu-id="acb27-123">Færið inn innhreyfingarskjalsnúmerið í reitnum **Innhreyfingarskjal**.</span><span class="sxs-lookup"><span data-stu-id="acb27-123">In the **Product receipt** field, enter the product receipt number.</span></span> <span data-ttu-id="acb27-124">Til dæmis er slegið inn „PR123“.</span><span class="sxs-lookup"><span data-stu-id="acb27-124">For example, enter PR123.</span></span>
4. <span data-ttu-id="acb27-125">Smellið á **Í lagi** til að bóka innhreyfingarskjalið.</span><span class="sxs-lookup"><span data-stu-id="acb27-125">Click **OK** to post the product receipt.</span></span>
5. <span data-ttu-id="acb27-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="acb27-126">Close the page.</span></span>

## <a name="create-a-vendor-invoice"></a><span data-ttu-id="acb27-127">Stofna reikning lánardrottins</span><span class="sxs-lookup"><span data-stu-id="acb27-127">Create a vendor invoice</span></span>
1. <span data-ttu-id="acb27-128">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Viðskiptaskuldir > Innkaupapantanir > Mótteknar óreikningsfærðar innkaupapantanir**.</span><span class="sxs-lookup"><span data-stu-id="acb27-128">In the Navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders received but not invoiced**.</span></span>
2. <span data-ttu-id="acb27-129">Velja innkaupapöntun sem var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="acb27-129">Select the purchase order that you created.</span></span>
3. <span data-ttu-id="acb27-130">Í aðgerðasvæðinu smellirðu á **Reikningur.**</span><span class="sxs-lookup"><span data-stu-id="acb27-130">On the Action Pane, click **Invoice**.</span></span>
4. <span data-ttu-id="acb27-131">Smelltu á **Reikningur**.</span><span class="sxs-lookup"><span data-stu-id="acb27-131">Click **Invoice**.</span></span>
5. <span data-ttu-id="acb27-132">Færið inn númer reiknings í **Númer**.</span><span class="sxs-lookup"><span data-stu-id="acb27-132">In the **Number** field, enter the invoice number.</span></span>
6. <span data-ttu-id="acb27-133">Sláið inn gildi í reitinn **Reikningslýsing**.</span><span class="sxs-lookup"><span data-stu-id="acb27-133">In the **Invoice description** field, type a value.</span></span>
7. <span data-ttu-id="acb27-134">Í retinum **Reikningsdagsetning** slærðu inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="acb27-134">In the **Invoice date** field, enter a date.</span></span>
8. <span data-ttu-id="acb27-135">Í reitnum **einingarverð** er fært inn 1200.</span><span class="sxs-lookup"><span data-stu-id="acb27-135">In the **Unit price** field, enter 1200.</span></span>
9. <span data-ttu-id="acb27-136">Smella á **Bæta við línu**.</span><span class="sxs-lookup"><span data-stu-id="acb27-136">Click **Add line**.</span></span>
10. <span data-ttu-id="acb27-137">Í reitnum **Vörunúmer** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="acb27-137">In the **Item number** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="acb27-138">Finna vörunúmer uppsetningargjalda á listanum.</span><span class="sxs-lookup"><span data-stu-id="acb27-138">In the list, find the installation charge item number.</span></span> <span data-ttu-id="acb27-139">Til dæmis S0001</span><span class="sxs-lookup"><span data-stu-id="acb27-139">For example, S0001</span></span>
12. <span data-ttu-id="acb27-140">Veljið vörunúmer uppsetningargjalda.</span><span class="sxs-lookup"><span data-stu-id="acb27-140">Select the installation charge item number.</span></span> <span data-ttu-id="acb27-141">Athugið að jöfnun hefur ekki verið framkvæmd síðan breytingarnar voru gerðar.</span><span class="sxs-lookup"><span data-stu-id="acb27-141">Note that matching has not been performed since you made the changes.</span></span>  
13. <span data-ttu-id="acb27-142">Smelltu á **Uppfæra samsvörunarstöðu**.</span><span class="sxs-lookup"><span data-stu-id="acb27-142">Click **Update match status**.</span></span>
14. <span data-ttu-id="acb27-143">Í aðgerðasvæðinu skal smella á **Yfirfara**.</span><span class="sxs-lookup"><span data-stu-id="acb27-143">On the Action Pane, click **Review**.</span></span>
15. <span data-ttu-id="acb27-144">Smellið á **Samsvörunarupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="acb27-144">Click **Matching details**.</span></span> <span data-ttu-id="acb27-145">Ný lína með þjónustu þarf ekki að vera jafnað svo staðan segi "Ekki framkvæmt".</span><span class="sxs-lookup"><span data-stu-id="acb27-145">The new line with services does not need to be matched so the status stays "Not performed".</span></span>  
16. <span data-ttu-id="acb27-146">Velja innhreyfingarskjal afurða fyrir birgðavöruna sem er móttekin.</span><span class="sxs-lookup"><span data-stu-id="acb27-146">Select the product receipt for the inventory item that you received.</span></span> <span data-ttu-id="acb27-147">Línan með innhreyfingarskjalinu var jöfnuð en ósamræmi er í magni eða verði svo það mistókst.</span><span class="sxs-lookup"><span data-stu-id="acb27-147">The line with the product receipt was matched but there is a mismatch of quantity or price so it fails.</span></span>  
17. <span data-ttu-id="acb27-148">Í reitnum **Einingarverð** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="acb27-148">In the **Unit price** field, enter a number.</span></span> <span data-ttu-id="acb27-149">Þegar einingaverðið hefur verið jafnað uppfærist staðan í „Stóðst“.</span><span class="sxs-lookup"><span data-stu-id="acb27-149">Now that the unit price matches, the status is updated to Passed.</span></span> <span data-ttu-id="acb27-150">Ef reglan leyfir misræmi eða ef jöfnun er aðeins viðvörun er samt hægt að bóka reikninginn.</span><span class="sxs-lookup"><span data-stu-id="acb27-150">If your policy allows discrepancies or if matching is only a warning, you can still post the invoice.</span></span>  
18. <span data-ttu-id="acb27-151">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="acb27-151">Close the page.</span></span>
19. <span data-ttu-id="acb27-152">Smelltu á **Bóka.**</span><span class="sxs-lookup"><span data-stu-id="acb27-152">Click **Post**.</span></span>
20. <span data-ttu-id="acb27-153">Lokaðu skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="acb27-153">Close the form.</span></span> <span data-ttu-id="acb27-154">Athugið að innkaupapöntunin er ekki lengur skráð sem móttekin en ekki reikningsfærð.</span><span class="sxs-lookup"><span data-stu-id="acb27-154">Note that the purchase order is no longer listed as received but not invoiced.</span></span>  

