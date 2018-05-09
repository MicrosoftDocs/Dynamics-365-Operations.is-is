---
title: "Telja birgðir í vöruhúsi"
description: "Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun birgðatalningabók til að telja tiltekinnar vöru á staðsetningu í vöruhúsinu."
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e7813f9add1c8cf3c2f22aff826daf22f54f348e
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="3209b-103">Telja birgðir í vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="3209b-103">Count inventory in a warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3209b-104">Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun birgðatalningabók til að telja tiltekinnar vöru á staðsetningu í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="3209b-104">This procedure walks you through the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="3209b-105">Ferlið á við "grunn vöruhús" aðgerðir, sem tiltækar eru í kerfinu birgðastjórnun, ekki á vöruhúsaaðgerð sem tiltæk er í kerfiseiningunni vöruhúsakerfi.</span><span class="sxs-lookup"><span data-stu-id="3209b-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="3209b-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="3209b-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="3209b-107">Ef verið er að nota eigin gögn, tryggja þarf afurðir og staðsetningar eru uppsettar og að hefur verið stofnað heiti birgðabókar fyrir talningarbækur.</span><span class="sxs-lookup"><span data-stu-id="3209b-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="3209b-108">Birgðatalning er yfirleitt framkvæmd af starfsmanni í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="3209b-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="3209b-109">Stofna færslubóka fyrir birgðatalningu</span><span class="sxs-lookup"><span data-stu-id="3209b-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="3209b-110">Fara í Birgðastjórnun > Færslubókarfærslur > Vörutalning > Talning.</span><span class="sxs-lookup"><span data-stu-id="3209b-110">Go to Inventory management > Journal entries > Item counting > Counting.</span></span>
2. <span data-ttu-id="3209b-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="3209b-111">Click New.</span></span>
3. <span data-ttu-id="3209b-112">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="3209b-112">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3209b-113">Á listanum, smella á að nota nafn birgðatalningabókar</span><span class="sxs-lookup"><span data-stu-id="3209b-113">In the list, click on the inventory counting journal name you want to use</span></span>
    * <span data-ttu-id="3209b-114">Sum svæði er fyllt út samkvæmt uppsetningu heitis birgðatalningabókar sem er valin.</span><span class="sxs-lookup"><span data-stu-id="3209b-114">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
5. <span data-ttu-id="3209b-115">Í reitnum starfskraftur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="3209b-115">In the Worker field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="3209b-116">Veljið starfsmanninn sem á að nota í listanum.</span><span class="sxs-lookup"><span data-stu-id="3209b-116">In the list, select the worker you want to use.</span></span>
7. <span data-ttu-id="3209b-117">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="3209b-117">Click Select.</span></span>
8. <span data-ttu-id="3209b-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="3209b-118">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="3209b-119">Stofna færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="3209b-119">Create journal lines</span></span>
1. <span data-ttu-id="3209b-120">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="3209b-120">Click New.</span></span>
2. <span data-ttu-id="3209b-121">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="3209b-121">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="3209b-122">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="3209b-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3209b-123">Ef verið er að nota sýnigögn fyrirtækisins USMF velja 'A0001'.</span><span class="sxs-lookup"><span data-stu-id="3209b-123">If you are using demo data company USMF, select 'A0001'.</span></span>  
4. <span data-ttu-id="3209b-124">Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="3209b-124">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="3209b-125">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="3209b-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3209b-126">Ef verið er að nota sýnigögn fyrirtækisins USMF, veljið svæði '2'.</span><span class="sxs-lookup"><span data-stu-id="3209b-126">If you are using demo data company USMF, select site '2'.</span></span>  
6. <span data-ttu-id="3209b-127">Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="3209b-127">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="3209b-128">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="3209b-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3209b-129">Ef verið er að nota sýnigögn fyrirtækisins USMF, skal velja vöruhúsið '24'.</span><span class="sxs-lookup"><span data-stu-id="3209b-129">If you are using demo data company USMF, select warehouse '24'.</span></span>  
8. <span data-ttu-id="3209b-130">Í reitnum staðsetning skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="3209b-130">In the Location field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="3209b-131">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="3209b-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3209b-132">Ef verið er að nota sýnigögn fyrirtækisins USMF, velja staðsetningu ‚BULK-001'</span><span class="sxs-lookup"><span data-stu-id="3209b-132">If you are using demo data company USMF, select location 'BULK-001'</span></span>  
10. <span data-ttu-id="3209b-133">Í reitinn Talið skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="3209b-133">In the Counted field, enter a number.</span></span>
    * <span data-ttu-id="3209b-134">Ef fært er inn talið númer sem er annað númer en er sýnd í svæðinu á lager, er magnsvæðið uppfærð til að sýna misræmið.</span><span class="sxs-lookup"><span data-stu-id="3209b-134">If you enter a counted number that’s different to the number shown in the On-hand field, the Quantity field is updated to show the discrepancy.</span></span>  
11. <span data-ttu-id="3209b-135">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="3209b-135">Click Save.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="3209b-136">Bóka færslubók fyrir birgðatalningu</span><span class="sxs-lookup"><span data-stu-id="3209b-136">Post the inventory counting journal</span></span>
1. <span data-ttu-id="3209b-137">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="3209b-137">Click Post.</span></span>
    * <span data-ttu-id="3209b-138">Þegar bókað er birgðatalningabók, ef talin upphæð er önnur en upphæð sem skráð er í svæðinu á lager er innhreyfing eða úthreyfing birgða bókuð, birgðastigi og birgðagildi breytt og fjárhagsfærslur stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="3209b-138">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the On-hand field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
2. <span data-ttu-id="3209b-139">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="3209b-139">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="3209b-140">Skoða birgðafærslur</span><span class="sxs-lookup"><span data-stu-id="3209b-140">View inventory transactions</span></span>
1. <span data-ttu-id="3209b-141">Smellið á birgðir.</span><span class="sxs-lookup"><span data-stu-id="3209b-141">Click Inventory.</span></span>
2. <span data-ttu-id="3209b-142">Smella á Færslur.</span><span class="sxs-lookup"><span data-stu-id="3209b-142">Click Transactions.</span></span>
    * <span data-ttu-id="3209b-143">Hér er hægt að sjá tengdar færslur sem stofnast þegar talningarbók birgða er bókuð.</span><span class="sxs-lookup"><span data-stu-id="3209b-143">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

