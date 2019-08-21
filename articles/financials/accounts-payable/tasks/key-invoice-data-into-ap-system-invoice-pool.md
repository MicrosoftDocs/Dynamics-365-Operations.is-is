---
title: Færa reikningsgögn inn í viðskiptaskuldakerfi með reikningasafni
description: Þessi leiðarvísi fyrir verk sýnir hvernig á að nota komubók til að stofna reikninga.
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b870613512a8f4a5c19a0a05cd72b35ea32861b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843218"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="f4e54-103">Færa reikningsgögn inn í viðskiptaskuldakerfi með reikningasafni</span><span class="sxs-lookup"><span data-stu-id="f4e54-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f4e54-104">Þessi leiðarvísi fyrir verk sýnir hvernig á að nota komubók til að stofna reikninga.</span><span class="sxs-lookup"><span data-stu-id="f4e54-104">This task guide will show you how to use the invoice register to create invoices.</span></span>  <span data-ttu-id="f4e54-105">Nota síðan reikningasafninu til að jafna reikninginn við innkaupapöntun og ljúka kostnað á síðunni reikningur lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="f4e54-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="f4e54-106">Stofna innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="f4e54-106">Create a purchase order</span></span>
1. <span data-ttu-id="f4e54-107">Fara í Viðskiptaskuldir > Innkaupapantanir > Innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="f4e54-107">Go to Accounts payable > Purchase orders > Purchase orders.</span></span>
2. <span data-ttu-id="f4e54-108">Smellið á Nýtt til að stofna innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="f4e54-108">Click New to create a purchase order.</span></span>
3. <span data-ttu-id="f4e54-109">Í reitnum lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f4e54-109">In the Vendor account field, click the drop down button to open the lookup.</span></span>
4. <span data-ttu-id="f4e54-110">Veljið lánardrottinn úr listanum.</span><span class="sxs-lookup"><span data-stu-id="f4e54-110">Select the vendor from the list.</span></span> <span data-ttu-id="f4e54-111">Til dæmis lánardrottins 1001.</span><span class="sxs-lookup"><span data-stu-id="f4e54-111">For example, vendor 1001.</span></span>
5. <span data-ttu-id="f4e54-112">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="f4e54-112">Click OK.</span></span>
6. <span data-ttu-id="f4e54-113">Í reitnum vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f4e54-113">In the Item number field, click the drop down button to open the lookup.</span></span>
7. <span data-ttu-id="f4e54-114">Finna vörunúmer þjónustu af listanum.</span><span class="sxs-lookup"><span data-stu-id="f4e54-114">Find the services item number in the list.</span></span> <span data-ttu-id="f4e54-115">Veljið til dæmis S0001.</span><span class="sxs-lookup"><span data-stu-id="f4e54-115">For example, select S0001.</span></span>
8. <span data-ttu-id="f4e54-116">Smellið á vörunúmer og veljið það.</span><span class="sxs-lookup"><span data-stu-id="f4e54-116">Click on the item number and select it.</span></span>
    * <span data-ttu-id="f4e54-117">Nettóupphæðin er 75,00.</span><span class="sxs-lookup"><span data-stu-id="f4e54-117">The net amount is 75.00.</span></span>  <span data-ttu-id="f4e54-118">Þetta er Upphæð sem við búumst við á reikningnum.</span><span class="sxs-lookup"><span data-stu-id="f4e54-118">That is the amount that we will expect on the invoice.</span></span>  
9. <span data-ttu-id="f4e54-119">Í aðgerðasvæðinu er smellt á Innkaup.</span><span class="sxs-lookup"><span data-stu-id="f4e54-119">On the action pane, click Purchase.</span></span>
10. <span data-ttu-id="f4e54-120">Smellið á „Staðfesta“.</span><span class="sxs-lookup"><span data-stu-id="f4e54-120">Click Confirm.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="f4e54-121">Stofna og bóka og reikningsfæra</span><span class="sxs-lookup"><span data-stu-id="f4e54-121">Create and post and invoice</span></span>
1. <span data-ttu-id="f4e54-122">Fara í Viðskiptaskuldir > Reikningar > Komubók.</span><span class="sxs-lookup"><span data-stu-id="f4e54-122">Go to Accounts payable > Invoices > Invoice register.</span></span>
2. <span data-ttu-id="f4e54-123">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f4e54-123">Click New.</span></span>
3. <span data-ttu-id="f4e54-124">Opna uppflettingu til að velja heiti komubókar sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="f4e54-124">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="f4e54-125">Veldu heiti komubókarinnar sem þú vilt nota.</span><span class="sxs-lookup"><span data-stu-id="f4e54-125">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="f4e54-126">Smellið á Línur til að opna afgreiðslukassann og færa inn kostnaðarlínur.</span><span class="sxs-lookup"><span data-stu-id="f4e54-126">Click on Lines to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="f4e54-127">Í Uppfletting skal velja lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="f4e54-127">In the lookup, select a vendor.</span></span> <span data-ttu-id="f4e54-128">Til dæmis má smella á lánardrottni 1001.</span><span class="sxs-lookup"><span data-stu-id="f4e54-128">For example, click on vendor 1001.</span></span>
7. <span data-ttu-id="f4e54-129">Í reitnum Reikningur færirðu inn númer reiknings.</span><span class="sxs-lookup"><span data-stu-id="f4e54-129">In the Invoice field, enter the invoice number.</span></span>
8. <span data-ttu-id="f4e54-130">Í reitinn Lýsing skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f4e54-130">In the Description field, type a value.</span></span>
9. <span data-ttu-id="f4e54-131">Í reitnum Kredit skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="f4e54-131">In the Credit field, enter a number.</span></span>
10. <span data-ttu-id="f4e54-132">Í reitnum innkaupapöntun skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f4e54-132">In the Purchase order field, click the drop down button to open the lookup.</span></span>
11. <span data-ttu-id="f4e54-133">Velja innkaupapöntun sem búið var til áður.</span><span class="sxs-lookup"><span data-stu-id="f4e54-133">Select the purchase order that you created earlier.</span></span>
12. <span data-ttu-id="f4e54-134">Í reitnum Samþykkt af skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f4e54-134">In the Approved by field, click the drop down button to open the lookup.</span></span>
13. <span data-ttu-id="f4e54-135">Merkið samþykkjanda og smelltu á Velja til að velja þann samþykkjanda.</span><span class="sxs-lookup"><span data-stu-id="f4e54-135">Highlight an approver and click Select to select that approver.</span></span>
14. <span data-ttu-id="f4e54-136">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="f4e54-136">Click Post.</span></span>
15. <span data-ttu-id="f4e54-137">Lokaðu skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="f4e54-137">Close the form.</span></span>
16. <span data-ttu-id="f4e54-138">Lokaðu skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="f4e54-138">Close the form.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="f4e54-139">Opna reikning úr safninu og stemma hann við innkaupapöntun til að ljúka reikningsferlinu.</span><span class="sxs-lookup"><span data-stu-id="f4e54-139">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="f4e54-140">Fara í Viðskiptaskuldir > Reikningar > Reikningasafn.</span><span class="sxs-lookup"><span data-stu-id="f4e54-140">Go to Accounts payable > Invoices > Invoice pool.</span></span>
2. <span data-ttu-id="f4e54-141">Smellt er á innkaupapöntun til að búa til reikning lánardrottins úr reikningi í safninu.</span><span class="sxs-lookup"><span data-stu-id="f4e54-141">Click Purchase order to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="f4e54-142">Veljið reikninginn sem á að skoða.</span><span class="sxs-lookup"><span data-stu-id="f4e54-142">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="f4e54-143">Smellið á Uppfæra samsvörunarstöðu til að ljúka við samsvörun.</span><span class="sxs-lookup"><span data-stu-id="f4e54-143">Click Update match status to complete the matching.</span></span>
5. <span data-ttu-id="f4e54-144">Í aðgerðasvæðinu er smellt á valkostir.</span><span class="sxs-lookup"><span data-stu-id="f4e54-144">On the action pane, click Options.</span></span>
6. <span data-ttu-id="f4e54-145">Smellið á skoða Breytingu.</span><span class="sxs-lookup"><span data-stu-id="f4e54-145">Click Change view.</span></span>
7. <span data-ttu-id="f4e54-146">Smellið á skoða Hnitanet.</span><span class="sxs-lookup"><span data-stu-id="f4e54-146">Click Grid view.</span></span>
8. <span data-ttu-id="f4e54-147">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="f4e54-147">Click Post.</span></span>
9. <span data-ttu-id="f4e54-148">Lokaðu skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="f4e54-148">Close the form.</span></span>
10. <span data-ttu-id="f4e54-149">Farið í Viðskiptaskuldir > Lánardrottnar > Lánardrottnar.</span><span class="sxs-lookup"><span data-stu-id="f4e54-149">Go to Accounts payable > Vendors > Vendors.</span></span>
11. <span data-ttu-id="f4e54-150">Veljið þann lánardrottinn sem var á innkaupapöntuninni.</span><span class="sxs-lookup"><span data-stu-id="f4e54-150">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="f4e54-151">Til dæmis, veljið lánardrottinn 1001.</span><span class="sxs-lookup"><span data-stu-id="f4e54-151">For example, select vendor 1001.</span></span>
12. <span data-ttu-id="f4e54-152">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f4e54-152">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="f4e54-153">Í aðgerðasvæðinu er smellt á lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="f4e54-153">On the action pane, click Vendor.</span></span>
14. <span data-ttu-id="f4e54-154">Smella á Færslur.</span><span class="sxs-lookup"><span data-stu-id="f4e54-154">Click Transactions.</span></span>
15. <span data-ttu-id="f4e54-155">Velja reikninginn sem þú stofnaðir.</span><span class="sxs-lookup"><span data-stu-id="f4e54-155">Select the invoice that you created.</span></span>
    * <span data-ttu-id="f4e54-156">uppsöfnun komubókar var bakfærð og bókaðar á viðeigandi kostnaðarlykil.</span><span class="sxs-lookup"><span data-stu-id="f4e54-156">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  

