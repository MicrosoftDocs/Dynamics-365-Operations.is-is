---
title: Færa reikningsgögn inn í viðskiptaskuldakerfi með reikningasafni
description: Þetta efni lýsir því hvernig nota á komubókina til að búa til reikninga.
author: abruer
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 670dd2ec15aa26791758ec4bea2b431482499436
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227161"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a><span data-ttu-id="ec190-103">Færa reikningsgögn inn í viðskiptaskuldakerfi með reikningasafni</span><span class="sxs-lookup"><span data-stu-id="ec190-103">Key invoice data into the AP system using invoice pool</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ec190-104">Þetta efni lýsir því hvernig nota á komubókina til að búa til reikninga.</span><span class="sxs-lookup"><span data-stu-id="ec190-104">This topic describes how to use the invoice register to create invoices.</span></span> <span data-ttu-id="ec190-105">Nota síðan reikningasafninu til að jafna reikninginn við innkaupapöntun og ljúka kostnað á síðunni reikningur lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="ec190-105">Then use the invoice pool to match the invoice to a purchase order and finalize the expense in the vendor invoice page.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="ec190-106">Stofna innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="ec190-106">Create a purchase order</span></span>
1. <span data-ttu-id="ec190-107">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Viðskiptaskuldir > Innkaupapantanir > Innkaupapantanir**.</span><span class="sxs-lookup"><span data-stu-id="ec190-107">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > Purchase orders**.</span></span>
2. <span data-ttu-id="ec190-108">Smellið á **Nýtt** til að stofna nýja innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="ec190-108">Select **New** to create a purchase order.</span></span>
3. <span data-ttu-id="ec190-109">Í reitnum **Lánardrottnalykill** skal velja lánardrottinn fyrir fellilistann.</span><span class="sxs-lookup"><span data-stu-id="ec190-109">In the **Vendor account** field, select a vendor for the drop-down list.</span></span> <span data-ttu-id="ec190-110">Til dæmis, veljið lánardrottinn **1001**.</span><span class="sxs-lookup"><span data-stu-id="ec190-110">For example, select vendor **1001**.</span></span>
4. <span data-ttu-id="ec190-111">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ec190-111">Select **OK**.</span></span>
5. <span data-ttu-id="ec190-112">Í reitnum **Vörunúmer** velurðu vörnúmer þjónustu af fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="ec190-112">In the **Item number** field, select the services item number in the drop-down list.</span></span> <span data-ttu-id="ec190-113">Veljið til dæmis **S0001**.</span><span class="sxs-lookup"><span data-stu-id="ec190-113">For example, select **S0001**.</span></span> <span data-ttu-id="ec190-114">Nettóupphæðin er 75,00.</span><span class="sxs-lookup"><span data-stu-id="ec190-114">The net amount is 75.00.</span></span>  <span data-ttu-id="ec190-115">Þetta er Upphæð sem við búumst við á reikningnum.</span><span class="sxs-lookup"><span data-stu-id="ec190-115">That is the amount that we will expect on the invoice.</span></span>  
6. <span data-ttu-id="ec190-116">Í aðgerðasvæðinu velurðu **Innkaup**.</span><span class="sxs-lookup"><span data-stu-id="ec190-116">On the action pane, select **Purchase**.</span></span>
7. <span data-ttu-id="ec190-117">Veldu **Staðfesta**.</span><span class="sxs-lookup"><span data-stu-id="ec190-117">Select **Confirm**.</span></span>

## <a name="create-and-post-and-invoice"></a><span data-ttu-id="ec190-118">Stofna og bóka og reikningsfæra</span><span class="sxs-lookup"><span data-stu-id="ec190-118">Create and post and invoice</span></span>
1. <span data-ttu-id="ec190-119">Í skoðunarrúðunni ferðu í **Einingar > Viðskiptaskuldir > Reikningar > Komubók**.</span><span class="sxs-lookup"><span data-stu-id="ec190-119">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice register**.</span></span>
2. <span data-ttu-id="ec190-120">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="ec190-120">Select **New**.</span></span>
3. <span data-ttu-id="ec190-121">Opna uppflettingu til að velja heiti komubókar sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="ec190-121">Open the lookup to select the name of the invoice register that you want to use.</span></span>
4. <span data-ttu-id="ec190-122">Veldu heiti komubókarinnar sem þú vilt nota.</span><span class="sxs-lookup"><span data-stu-id="ec190-122">Select the name of the invoice register that you want to use.</span></span>
5. <span data-ttu-id="ec190-123">Veldu **Línur** til að opna skrána og færa inn kostnaðarlínur.</span><span class="sxs-lookup"><span data-stu-id="ec190-123">Select **Lines** to open the register and enter expense lines.</span></span>
6. <span data-ttu-id="ec190-124">Í Uppfletting skal velja lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="ec190-124">In the lookup, select a vendor.</span></span> <span data-ttu-id="ec190-125">Til dæmis, veljið lánardrottinn **1001**.</span><span class="sxs-lookup"><span data-stu-id="ec190-125">For example, select vendor **1001**.</span></span>
7. <span data-ttu-id="ec190-126">Í reitnum **Reikningur** færirðu inn númer reiknings.</span><span class="sxs-lookup"><span data-stu-id="ec190-126">In the **Invoice** field, enter the invoice number.</span></span>
8. <span data-ttu-id="ec190-127">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ec190-127">In the **Description** field, type a value.</span></span>
9. <span data-ttu-id="ec190-128">Í reitnum **Kredit** skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="ec190-128">In the **Credit** field, enter a number.</span></span>
10. <span data-ttu-id="ec190-129">Í reitnum **Innkaupapöntun** opnarðu fellivalmyndina til að velja innkaupapöntunina sem þú bjóst til áður.</span><span class="sxs-lookup"><span data-stu-id="ec190-129">In the **Purchase order** field, open the drop-down list to select the purchase order that you created earlier.</span></span>
11. <span data-ttu-id="ec190-130">Í reitnum **Samþykkt af** skal auðkenna samþykktaraðila á fellilistanum og smella á **Velja** til að velja þann samþykktaraðila.</span><span class="sxs-lookup"><span data-stu-id="ec190-130">In the **Approved by** field, highlight an approver in the drop-down list and click **Select** to select that approver.</span></span>
12. <span data-ttu-id="ec190-131">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="ec190-131">Select **Post**.</span></span>

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a><span data-ttu-id="ec190-132">Opna reikning úr safninu og stemma hann við innkaupapöntun til að ljúka reikningsferlinu.</span><span class="sxs-lookup"><span data-stu-id="ec190-132">Open an invoice from the pool and match it to a purchase order to complete the invoice process</span></span>
1. <span data-ttu-id="ec190-133">Í skoðunarrúðunni ferðu í **Einingar > Viðskiptaskuldir > Reikningar > Reikningasafn**.</span><span class="sxs-lookup"><span data-stu-id="ec190-133">In the navigation pane, go to **Modules > Accounts payable > Invoices > Invoice pool**.</span></span>
2. <span data-ttu-id="ec190-134">Veldu **Innkaupapöntun** til að búa til reikning lánardrottins úr reikningi í safninu.</span><span class="sxs-lookup"><span data-stu-id="ec190-134">Select **Purchase order** to create a vendor invoice from the invoice in the pool.</span></span>
3. <span data-ttu-id="ec190-135">Veljið reikninginn sem á að skoða.</span><span class="sxs-lookup"><span data-stu-id="ec190-135">Select the invoice that you want to review.</span></span>
4. <span data-ttu-id="ec190-136">Veldu **Uppfæra samsvörunarstöðu** til að ljúka við samsvörun.</span><span class="sxs-lookup"><span data-stu-id="ec190-136">Select **Update match status** to complete the matching.</span></span>
5. <span data-ttu-id="ec190-137">Í aðgerðasvæðinu velurðu **Valkostir**.</span><span class="sxs-lookup"><span data-stu-id="ec190-137">On the action pane, select **Options**.</span></span>
6. <span data-ttu-id="ec190-138">Veldu **Breyta skjámynd**.</span><span class="sxs-lookup"><span data-stu-id="ec190-138">Select **Change view**.</span></span>
7. <span data-ttu-id="ec190-139">Veldu **Hnitalínuyfirlit**.</span><span class="sxs-lookup"><span data-stu-id="ec190-139">Select **Grid view**.</span></span>
8. <span data-ttu-id="ec190-140">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="ec190-140">Select **Post**.</span></span>
9. <span data-ttu-id="ec190-141">Lokaðu skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="ec190-141">Close the form.</span></span>
10. <span data-ttu-id="ec190-142">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Viðskiptaskuldir > Lánardrottnar > Lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="ec190-142">In the navigation pane, go to **Modules > Accounts payable > Vendors > Vendors**.</span></span>
11. <span data-ttu-id="ec190-143">Veljið þann lánardrottinn sem var á innkaupapöntuninni.</span><span class="sxs-lookup"><span data-stu-id="ec190-143">Select the vendor that was on the purchase order.</span></span> <span data-ttu-id="ec190-144">Til dæmis, veljið lánardrottinn **1001**.</span><span class="sxs-lookup"><span data-stu-id="ec190-144">For example, select vendor **1001**.</span></span>
12. <span data-ttu-id="ec190-145">Á aðgerðasvæðinu velurðu **Lánardrottinn**.</span><span class="sxs-lookup"><span data-stu-id="ec190-145">On the action pane, select **Vendor**.</span></span>
13. <span data-ttu-id="ec190-146">Veldu **Færslur**.</span><span class="sxs-lookup"><span data-stu-id="ec190-146">Select **Transactions**.</span></span>
14. <span data-ttu-id="ec190-147">Velja reikninginn sem þú stofnaðir.</span><span class="sxs-lookup"><span data-stu-id="ec190-147">Select the invoice that you created.</span></span> <span data-ttu-id="ec190-148">uppsöfnun komubókar var bakfærð og bókaðar á viðeigandi kostnaðarlykil.</span><span class="sxs-lookup"><span data-stu-id="ec190-148">The invoice register accrual was reversed and posted to the appropriate expense account.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]