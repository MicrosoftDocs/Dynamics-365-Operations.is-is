--- 
title: "Skrá vörumóttöku í innkaupapöntun"
description: "Þessi verklýsing sýnir hvernig á að skrá móttöku á vörum beint á innkaupapöntun."
author: FrankDahl
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 14d1d43479f9864d8fd5ed94a98a654e75eeedf0
ms.contentlocale: is-is
ms.lasthandoff: 09/14/2018

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="82950-103">Skrá vörumóttöku í innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="82950-103">Record the receipt of goods on the purchase order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82950-104">Þessi verklýsing sýnir hvernig á að skrá móttöku á vörum beint á innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="82950-104">This procedure shows you how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="82950-105">Einnig er hægt að skrá innhreyfingu afurða í vöruhúsinu og síðan síðar skrá hana í innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="82950-105">It’s also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="82950-106">Þetta verk er yfirleitt gert af innkaupaaðila eða af samræmingaraðila viðskiptaskulda.</span><span class="sxs-lookup"><span data-stu-id="82950-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="82950-107">Dæmi sem eru sýnd í þessari handbók er hægt að nota sýnigögn USMF-fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="82950-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="82950-108">Dæmin inniheldur skref til að stofna einfalda innkaupapöntun, þannig að hægt er að spila ferlið sem leiðarvísi fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="82950-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="82950-109">Ef þú værir að nota ferlið á þín eigin gögn, myndirðu byrgja á undirverkinu Færsla innhreyfingar á vörum.</span><span class="sxs-lookup"><span data-stu-id="82950-109">If you were using the procedure on your own data, you would start at the Record receipt of goods subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="82950-110">Undirbúa nýja innkaupapöntun vegna móttöku afurða.</span><span class="sxs-lookup"><span data-stu-id="82950-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="82950-111">Fara í innkaup og aðföng > innkaupapöntun  > allar innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="82950-111">Go to Procurement and sourcing > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="82950-112">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="82950-112">Click New.</span></span>
3. <span data-ttu-id="82950-113">Í svæðinu Lánardrottnalykill skal slá inn 'US-101'.</span><span class="sxs-lookup"><span data-stu-id="82950-113">In the Vendor account field, enter US-101.</span></span>
4. <span data-ttu-id="82950-114">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="82950-114">Click OK.</span></span>
5. <span data-ttu-id="82950-115">Í svæðið vörunúmer sláið inn M0001.</span><span class="sxs-lookup"><span data-stu-id="82950-115">In the Item number field, enter M0001.</span></span>
6. <span data-ttu-id="82950-116">Í reitinn magn skal slá inn 5.</span><span class="sxs-lookup"><span data-stu-id="82950-116">In the Quantity field, enter 5.</span></span>
7. <span data-ttu-id="82950-117">Smellið á „Innkaup“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="82950-117">On the Action Pane, click Purchase.</span></span>
8. <span data-ttu-id="82950-118">Smellið á „Staðfesta“.</span><span class="sxs-lookup"><span data-stu-id="82950-118">Click Confirm.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="82950-119">Skrásetja viðtöku varnings</span><span class="sxs-lookup"><span data-stu-id="82950-119">Record receipt of goods</span></span>
1. <span data-ttu-id="82950-120">Smellið á „Móttaka“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="82950-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="82950-121">Smellið á „Innhreyfingarskjal“.</span><span class="sxs-lookup"><span data-stu-id="82950-121">Click Product receipt.</span></span>
    * <span data-ttu-id="82950-122">Magnsvæðið leyfir þér að velja mismunandi valkosti fyrir það magn sem á að taka á móti.</span><span class="sxs-lookup"><span data-stu-id="82950-122">The Quantity field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="82950-123">Til dæmis, ef áður hefur verið skráð magn í vöruhúsi, er hægt að velja Skráð magn .</span><span class="sxs-lookup"><span data-stu-id="82950-123">For example, if a quantity has previously been registered in the warehouse, you can select Registered quantity.</span></span>  <span data-ttu-id="82950-124">Í þessu dæmis, notaðu gildið Pantað magn.</span><span class="sxs-lookup"><span data-stu-id="82950-124">For this example, use the value Ordered quantity.</span></span>   
3. <span data-ttu-id="82950-125">Í reitinn móttaka afurða skal slá inn hvaða gildi sem er.</span><span class="sxs-lookup"><span data-stu-id="82950-125">In the Product receipt field, type any value.</span></span>
    * <span data-ttu-id="82950-126">Þetta svæði er notað til að færa inn tilvísun sem verður notað sem fylgiskjal fyrir færslubók innhreyfingarskjala afurða.</span><span class="sxs-lookup"><span data-stu-id="82950-126">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
4. <span data-ttu-id="82950-127">Stækka línuhlutann.</span><span class="sxs-lookup"><span data-stu-id="82950-127">Expand the Lines section.</span></span>
5. <span data-ttu-id="82950-128">Stillið magn á „4“.</span><span class="sxs-lookup"><span data-stu-id="82950-128">Set Quantity to '4'.</span></span>
    * <span data-ttu-id="82950-129">Hér er hægt að tilgreina handvirkt magn sem fæst fyrir hverja línu í pöntun.</span><span class="sxs-lookup"><span data-stu-id="82950-129">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
6. <span data-ttu-id="82950-130">Fella saman hlutann línur.</span><span class="sxs-lookup"><span data-stu-id="82950-130">Collapse the Lines section.</span></span>
7. <span data-ttu-id="82950-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="82950-131">Click OK.</span></span>
    * <span data-ttu-id="82950-132">Vörurnar hafa nú verið skráð sem móttekið á innkaupapöntuninni og búið er að stofna færslubók fyrir innhreyfingarskjal afurða sem endurspegla þetta.</span><span class="sxs-lookup"><span data-stu-id="82950-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="82950-133">Hægt er að nota aðgerðina innhreyfing afurðar til að fara yfir færslubækur sem stofnaðar eru með innkaupapöntuninni og sjá hvað var móttekið og hvenær.</span><span class="sxs-lookup"><span data-stu-id="82950-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  


