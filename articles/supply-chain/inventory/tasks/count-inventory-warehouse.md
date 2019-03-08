---
title: Telja birgðir í vöruhúsi
description: Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun birgðatalningabók til að telja tiltekinnar vöru á staðsetningu í vöruhúsinu.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c0bbfe8f86d27f81b0d577ed89dfa34ebcf3f18
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "353472"
---
# <a name="count-inventory-in-a-warehouse"></a><span data-ttu-id="aa406-103">Telja birgðir í vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="aa406-103">Count inventory in a warehouse</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="aa406-104">Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun birgðatalningabók til að telja tiltekinnar vöru á staðsetningu í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="aa406-104">This procedure walks you through the process of creating and posting an inventory counting journal in order to count a specific item at a location in the warehouse.</span></span> <span data-ttu-id="aa406-105">Ferlið á við "grunn vöruhús" aðgerðir, sem tiltækar eru í kerfinu birgðastjórnun, ekki á vöruhúsaaðgerð sem tiltæk er í kerfiseiningunni vöruhúsakerfi.</span><span class="sxs-lookup"><span data-stu-id="aa406-105">The procedure applies to “basic warehousing” functionality, available in the Inventory management module, not to the warehousing functionality that’s available in the Warehouse management module.</span></span> <span data-ttu-id="aa406-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="aa406-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="aa406-107">Ef verið er að nota eigin gögn, tryggja þarf afurðir og staðsetningar eru uppsettar og að hefur verið stofnað heiti birgðabókar fyrir talningarbækur.</span><span class="sxs-lookup"><span data-stu-id="aa406-107">If you’re using your own data, make sure that you have products and locations set up, and that you’ve created an inventory journal name for counting journals.</span></span> <span data-ttu-id="aa406-108">Birgðatalning er yfirleitt framkvæmd af starfsmanni í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="aa406-108">Inventory counting is normally carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-counting-journal"></a><span data-ttu-id="aa406-109">Stofna færslubóka fyrir birgðatalningu</span><span class="sxs-lookup"><span data-stu-id="aa406-109">Create an inventory counting journal</span></span>
1. <span data-ttu-id="aa406-110">Fara í Birgðastjórnun > Færslubókarfærslur > Vörutalning > Talning.</span><span class="sxs-lookup"><span data-stu-id="aa406-110">Go to Inventory management > Journal entries > Item counting > Counting.</span></span>
2. <span data-ttu-id="aa406-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="aa406-111">Click New.</span></span>
3. <span data-ttu-id="aa406-112">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="aa406-112">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="aa406-113">Á listanum, smella á að nota nafn birgðatalningabókar</span><span class="sxs-lookup"><span data-stu-id="aa406-113">In the list, click on the inventory counting journal name you want to use</span></span>
    * <span data-ttu-id="aa406-114">Sum svæði er fyllt út samkvæmt uppsetningu heitis birgðatalningabókar sem er valin.</span><span class="sxs-lookup"><span data-stu-id="aa406-114">Some other fields will be populated based on the setup of the inventory counting journal name that you select.</span></span>  
5. <span data-ttu-id="aa406-115">Í reitnum starfskraftur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="aa406-115">In the Worker field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="aa406-116">Veljið starfsmanninn sem á að nota í listanum.</span><span class="sxs-lookup"><span data-stu-id="aa406-116">In the list, select the worker you want to use.</span></span>
7. <span data-ttu-id="aa406-117">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="aa406-117">Click Select.</span></span>
8. <span data-ttu-id="aa406-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="aa406-118">Click OK.</span></span>

## <a name="create-journal-lines"></a><span data-ttu-id="aa406-119">Stofna færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="aa406-119">Create journal lines</span></span>
1. <span data-ttu-id="aa406-120">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="aa406-120">Click New.</span></span>
2. <span data-ttu-id="aa406-121">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="aa406-121">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="aa406-122">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="aa406-122">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="aa406-123">Ef verið er að nota sýnigögn fyrirtækisins USMF velja 'A0001'.</span><span class="sxs-lookup"><span data-stu-id="aa406-123">If you are using demo data company USMF, select 'A0001'.</span></span>  
4. <span data-ttu-id="aa406-124">Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="aa406-124">In the Site field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="aa406-125">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="aa406-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="aa406-126">Ef verið er að nota sýnigögn fyrirtækisins USMF, veljið svæði '2'.</span><span class="sxs-lookup"><span data-stu-id="aa406-126">If you are using demo data company USMF, select site '2'.</span></span>  
6. <span data-ttu-id="aa406-127">Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="aa406-127">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="aa406-128">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="aa406-128">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="aa406-129">Ef verið er að nota sýnigögn fyrirtækisins USMF, skal velja vöruhúsið '24'.</span><span class="sxs-lookup"><span data-stu-id="aa406-129">If you are using demo data company USMF, select warehouse '24'.</span></span>  
8. <span data-ttu-id="aa406-130">Í reitnum staðsetning skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="aa406-130">In the Location field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="aa406-131">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="aa406-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="aa406-132">Ef verið er að nota sýnigögn fyrirtækisins USMF, velja staðsetningu ‚BULK-001'</span><span class="sxs-lookup"><span data-stu-id="aa406-132">If you are using demo data company USMF, select location 'BULK-001'</span></span>  
10. <span data-ttu-id="aa406-133">Í reitinn Talið skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="aa406-133">In the Counted field, enter a number.</span></span>
    * <span data-ttu-id="aa406-134">Ef fært er inn talið númer sem er annað númer en er sýnd í svæðinu á lager, er magnsvæðið uppfærð til að sýna misræmið.</span><span class="sxs-lookup"><span data-stu-id="aa406-134">If you enter a counted number that’s different to the number shown in the On-hand field, the Quantity field is updated to show the discrepancy.</span></span>  
11. <span data-ttu-id="aa406-135">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="aa406-135">Click Save.</span></span>

## <a name="post-the-inventory-counting-journal"></a><span data-ttu-id="aa406-136">Bóka færslubók fyrir birgðatalningu</span><span class="sxs-lookup"><span data-stu-id="aa406-136">Post the inventory counting journal</span></span>
1. <span data-ttu-id="aa406-137">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="aa406-137">Click Post.</span></span>
    * <span data-ttu-id="aa406-138">Þegar bókað er birgðatalningabók, ef talin upphæð er önnur en upphæð sem skráð er í svæðinu á lager er innhreyfing eða úthreyfing birgða bókuð, birgðastigi og birgðagildi breytt og fjárhagsfærslur stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="aa406-138">When you post an inventory counting journal, if the counted amount differs from amount that’s reported in the On-hand field an inventory receipt or issue is posted, the inventory level and value are changed, and ledger transactions are generated.</span></span>  
2. <span data-ttu-id="aa406-139">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="aa406-139">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="aa406-140">Skoða birgðafærslur</span><span class="sxs-lookup"><span data-stu-id="aa406-140">View inventory transactions</span></span>
1. <span data-ttu-id="aa406-141">Smellið á birgðir.</span><span class="sxs-lookup"><span data-stu-id="aa406-141">Click Inventory.</span></span>
2. <span data-ttu-id="aa406-142">Smella á Færslur.</span><span class="sxs-lookup"><span data-stu-id="aa406-142">Click Transactions.</span></span>
    * <span data-ttu-id="aa406-143">Hér er hægt að sjá tengdar færslur sem stofnast þegar talningarbók birgða er bókuð.</span><span class="sxs-lookup"><span data-stu-id="aa406-143">Here you can see any related transactions that will be created when you post your inventory counting journal.</span></span>   

