---
title: "Flytja efnislegar birgðir innan vöruhúss"
description: "Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun á birgðaflutningabók til að skrá hreyfingar vöru úr einni staðsetningu í vöruhúsi í annað."
author: MarkusFogelberg
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: bfba69731a4897906d08ff9fb9ce69e79121efeb
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="08544-103">Flytja efnislegar birgðir innan vöruhúss</span><span class="sxs-lookup"><span data-stu-id="08544-103">Transfer physical inventory within the warehouse</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="08544-104">Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun á birgðaflutningabók til að skrá hreyfingar vöru úr einni staðsetningu í vöruhúsi í annað.</span><span class="sxs-lookup"><span data-stu-id="08544-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="08544-105">Þú þarft að hafa með heiti birgðabókarinnar sett upp fyrir birgðaflutning áður en byrjað er að þetta.</span><span class="sxs-lookup"><span data-stu-id="08544-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="08544-106">Hægt er að fara í gegnum þessu ferli í sýnigögn fyrirtækisins USMF með notkun dæmagilda sem eru sýndar eða með því að nota eigin gögn ef afurðir og staðsetningar eru uppsettar.</span><span class="sxs-lookup"><span data-stu-id="08544-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="08544-107">Þessi verkefni eru venjulega framkvæmd af starfsmanni í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="08544-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="08544-108">Stofna færslubóka fyrir birgðaflutning</span><span class="sxs-lookup"><span data-stu-id="08544-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="08544-109">Fara í Flutningi.</span><span class="sxs-lookup"><span data-stu-id="08544-109">Go to Transfer.</span></span>
2. <span data-ttu-id="08544-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="08544-110">Click New.</span></span>
3. <span data-ttu-id="08544-111">Sláið inn eða veldu gildi í reitnum heiti.</span><span class="sxs-lookup"><span data-stu-id="08544-111">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="08544-112">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="08544-112">Click OK.</span></span>
    * <span data-ttu-id="08544-113">Það er að valkostur um að tilgreina 'Frá' og ''til“ vídda fyrir hverja færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="08544-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="08544-114">Þetta eru mikilvægar fyrir gerð færslubókar.</span><span class="sxs-lookup"><span data-stu-id="08544-114">These are essential for this journal type.</span></span> <span data-ttu-id="08544-115">Hægt er að flytja vörur á staði með mismunandi reglur.</span><span class="sxs-lookup"><span data-stu-id="08544-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="08544-116">Í þessu dæmi munum við flytja vöru innan sama vöruhús, frá númeraplötustýrð staðsetningu á staðsetningu sem ekki er númeraplötustýrð.</span><span class="sxs-lookup"><span data-stu-id="08544-116">In this example we’ll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="08544-117">Stofna færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="08544-117">Create journal lines</span></span>
1. <span data-ttu-id="08544-118">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="08544-118">Click New.</span></span>
2. <span data-ttu-id="08544-119">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="08544-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="08544-120">Ef verið er að nota USMF er hægt að velja 'A0001'.</span><span class="sxs-lookup"><span data-stu-id="08544-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="08544-121">Sláið inn eða veldu gildi í reitnum Frá svæði.</span><span class="sxs-lookup"><span data-stu-id="08544-121">In the From site field, enter or select a value.</span></span>
    * <span data-ttu-id="08544-122">Ef verið er að nota USMF er hægt að velja '2'.</span><span class="sxs-lookup"><span data-stu-id="08544-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="08544-123">Sláið inn eða veldu gildi í reitnum í Til svæðis.</span><span class="sxs-lookup"><span data-stu-id="08544-123">In the To site field, enter or select a value.</span></span>
    * <span data-ttu-id="08544-124">Ef verið er að nota USMF er hægt að velja '2'.</span><span class="sxs-lookup"><span data-stu-id="08544-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="08544-125">Sláðu inn eða veldu gildi í reitnum Úr vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="08544-125">In the From warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="08544-126">Ef verið er að nota USMF er hægt að velja '24'.</span><span class="sxs-lookup"><span data-stu-id="08544-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="08544-127">Sláðu inn eða veldu gildi í reitnum Í vöruhús.</span><span class="sxs-lookup"><span data-stu-id="08544-127">In the To warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="08544-128">Ef verið er að nota USMF er hægt að velja '24'.</span><span class="sxs-lookup"><span data-stu-id="08544-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="08544-129">Færa inn eða veljið gildi í svæðinu Frá staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="08544-129">In the From location field, enter or select a value.</span></span>
    * <span data-ttu-id="08544-130">Ef verið er að nota USMF er hægt að velja 'FL-001'.</span><span class="sxs-lookup"><span data-stu-id="08544-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="08544-131">Sláðu inn eða veldu gildi í reitnum Í staðsetning.</span><span class="sxs-lookup"><span data-stu-id="08544-131">In the To location field, enter or select a value.</span></span>
    * <span data-ttu-id="08544-132">Ef verið er að nota USMF er hægt að velja ‚BULK-001'.</span><span class="sxs-lookup"><span data-stu-id="08544-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="08544-133">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="08544-133">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="08544-134">Smellið á flipann Birgðavíddir.</span><span class="sxs-lookup"><span data-stu-id="08544-134">Click the Inventory dimensions tab.</span></span>
11. <span data-ttu-id="08544-135">Færa inn eða veljið gildi í svæðinu númeraplata.</span><span class="sxs-lookup"><span data-stu-id="08544-135">In the License plate field, enter or select a value.</span></span>
    * <span data-ttu-id="08544-136">Ef verið er að nota USMF er hægt að velja '24'.</span><span class="sxs-lookup"><span data-stu-id="08544-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="08544-137">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="08544-137">Click Save.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="08544-138">Bóka færslubóka fyrir birgðaflutning</span><span class="sxs-lookup"><span data-stu-id="08544-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="08544-139">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="08544-139">Click Post.</span></span>
2. <span data-ttu-id="08544-140">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="08544-140">Click OK.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="08544-141">Skoða birgðafærslur</span><span class="sxs-lookup"><span data-stu-id="08544-141">View inventory transactions</span></span>
1. <span data-ttu-id="08544-142">Smellið á birgðir.</span><span class="sxs-lookup"><span data-stu-id="08544-142">Click Inventory.</span></span>
2. <span data-ttu-id="08544-143">Smella á Færslur.</span><span class="sxs-lookup"><span data-stu-id="08544-143">Click Transactions.</span></span>
    * <span data-ttu-id="08544-144">Hér er hægt að sjá færslurnar sem voru stofnaðar þegar þitt færslubók var bókuð.</span><span class="sxs-lookup"><span data-stu-id="08544-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

