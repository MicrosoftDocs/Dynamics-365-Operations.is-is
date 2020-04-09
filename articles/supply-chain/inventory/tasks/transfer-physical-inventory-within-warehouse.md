---
title: Flytja efnislegar birgðir innan vöruhúss
description: Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun á birgðaflutningabók til að skrá hreyfingar vöru úr einni staðsetningu í vöruhúsi í annað.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTransfer, InventJournalCreate, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 899701413814ce38a4367618ed72d1039eca0bf8
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148171"
---
# <a name="transfer-physical-inventory-within-the-warehouse"></a><span data-ttu-id="11015-103">Flytja efnislegar birgðir innan vöruhúss</span><span class="sxs-lookup"><span data-stu-id="11015-103">Transfer physical inventory within the warehouse</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11015-104">Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun á birgðaflutningabók til að skrá hreyfingar vöru úr einni staðsetningu í vöruhúsi í annað.</span><span class="sxs-lookup"><span data-stu-id="11015-104">This procedure walks you through the process of creating and posting an inventory transfer journal in order to register movement of an item from one location in a warehouse to another.</span></span> <span data-ttu-id="11015-105">Þú þarft að hafa með heiti birgðabókarinnar sett upp fyrir birgðaflutning áður en byrjað er að þetta.</span><span class="sxs-lookup"><span data-stu-id="11015-105">You need to have an inventory journal name set up for inventory transfers before you start this.</span></span> <span data-ttu-id="11015-106">Hægt er að fara í gegnum þessu ferli í sýnigögn fyrirtækisins USMF með notkun dæmagilda sem eru sýndar eða með því að nota eigin gögn ef afurðir og staðsetningar eru uppsettar.</span><span class="sxs-lookup"><span data-stu-id="11015-106">You can walk through this procedure in demo data company USMF using the example values that are shown, or using you can use your own data if you have products and locations set up.</span></span> <span data-ttu-id="11015-107">Þessi verkefni eru venjulega framkvæmd af starfsmanni í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="11015-107">These tasks would normally be carried out by a warehouse employee.</span></span>


## <a name="create-an-inventory-transfer-journal"></a><span data-ttu-id="11015-108">Stofna færslubóka fyrir birgðaflutning</span><span class="sxs-lookup"><span data-stu-id="11015-108">Create an inventory transfer journal</span></span>
1. <span data-ttu-id="11015-109">Í **Skoðunarrúðu** ferðu í **Birgðastjórnun > Færslubókarfærslur > Vörur > Flutningur**.</span><span class="sxs-lookup"><span data-stu-id="11015-109">In the **Navigation pane**, go to **Inventory management > Journal entries > Items > Transfer**.</span></span>
2. <span data-ttu-id="11015-110">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="11015-110">Click **New**.</span></span>
3. <span data-ttu-id="11015-111">Sláið inn eða veldu gildi í reitnum **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="11015-111">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="11015-112">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="11015-112">Click **OK**.</span></span> <span data-ttu-id="11015-113">Það er að valkostur um að tilgreina 'Frá' og ''til“ vídda fyrir hverja færslubókarlínu.</span><span class="sxs-lookup"><span data-stu-id="11015-113">There is the option to specify 'From' and 'To' dimensions for each journal line.</span></span> <span data-ttu-id="11015-114">Þetta eru mikilvægar fyrir gerð færslubókar.</span><span class="sxs-lookup"><span data-stu-id="11015-114">These are essential for this journal type.</span></span> <span data-ttu-id="11015-115">Hægt er að flytja vörur á staði með mismunandi reglur.</span><span class="sxs-lookup"><span data-stu-id="11015-115">You can transfer items to locations using different rules.</span></span> <span data-ttu-id="11015-116">Í þessu dæmi munum við flytja vöru innan sama vöruhús, frá númeraplötustýrð staðsetningu á staðsetningu sem ekki er númeraplötustýrð.</span><span class="sxs-lookup"><span data-stu-id="11015-116">In this example we'll transfer an item within the same warehouse, from a license plate controlled location to a location that is not license plate controlled.</span></span>   

## <a name="create-journal-lines"></a><span data-ttu-id="11015-117">Stofna færslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="11015-117">Create journal lines</span></span>
1. <span data-ttu-id="11015-118">Í flýtiflipanum **Færslubókarlínur** smellirðu á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="11015-118">Int the **Journal lines fastTab**, click **New**.</span></span>
2. <span data-ttu-id="11015-119">Í reitinn **Vörunúmer** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="11015-119">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="11015-120">Ef verið er að nota USMF er hægt að velja 'A0001'.</span><span class="sxs-lookup"><span data-stu-id="11015-120">If you are using USMF, you can select 'A0001'.</span></span>  
3. <span data-ttu-id="11015-121">Í reitinn **Frá svæði** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="11015-121">In the **From site** field, enter or select a value.</span></span> <span data-ttu-id="11015-122">Ef verið er að nota USMF er hægt að velja '2'.</span><span class="sxs-lookup"><span data-stu-id="11015-122">If you are using USMF, you can select '2'.</span></span>  
4. <span data-ttu-id="11015-123">í reitinn **Til svæðis** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="11015-123">In the **To site** field, enter or select a value.</span></span> <span data-ttu-id="11015-124">Ef verið er að nota USMF er hægt að velja '2'.</span><span class="sxs-lookup"><span data-stu-id="11015-124">If you are using USMF, you can select '2'.</span></span>  
5. <span data-ttu-id="11015-125">Í reitinn **Úr vöruhúsi** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="11015-125">In the **From warehouse** field, enter or select a value.</span></span> <span data-ttu-id="11015-126">Ef verið er að nota USMF er hægt að velja '24'.</span><span class="sxs-lookup"><span data-stu-id="11015-126">If you are using USMF, you can select '24'.</span></span>  
6. <span data-ttu-id="11015-127">Í reitinn **Í vöruhús** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="11015-127">In the **To warehouse** field, enter or select a value.</span></span> <span data-ttu-id="11015-128">Ef verið er að nota USMF er hægt að velja '24'.</span><span class="sxs-lookup"><span data-stu-id="11015-128">If you are using USMF, you can select '24'.</span></span>  
7. <span data-ttu-id="11015-129">Í reitinn **Frá staðsetningu** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="11015-129">In the **From location** field, enter or select a value.</span></span> <span data-ttu-id="11015-130">Ef verið er að nota USMF er hægt að velja 'FL-001'.</span><span class="sxs-lookup"><span data-stu-id="11015-130">If you are using USMF, you can select 'FL-001'.</span></span>  
8. <span data-ttu-id="11015-131">Í reitinn **Til staðsetningar** skaltu færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="11015-131">In the **To location** field, enter or select a value.</span></span> <span data-ttu-id="11015-132">Ef verið er að nota USMF er hægt að velja ‚BULK-001'.</span><span class="sxs-lookup"><span data-stu-id="11015-132">If you are using USMF, you can select 'BULK-001'.</span></span>  
9. <span data-ttu-id="11015-133">Í reitnum **Magn** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="11015-133">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="11015-134">Í flýtiflipanum **Línulýsing** smellirðu á flipann **Birgðavíddir**.</span><span class="sxs-lookup"><span data-stu-id="11015-134">In the **Line details** fastTab, click the **Inventory dimensions** tab.</span></span>
11. <span data-ttu-id="11015-135">Í **Frá birgðavíddum**, í reitnum **Númeraplata** skaltu slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="11015-135">In **From inventory dimensions**, in the **License plate** field, enter or select a value.</span></span> <span data-ttu-id="11015-136">Ef verið er að nota USMF er hægt að velja '24'.</span><span class="sxs-lookup"><span data-stu-id="11015-136">If you are using USMF, you can select '24'.</span></span>  
12. <span data-ttu-id="11015-137">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="11015-137">Click **Save**.</span></span>

## <a name="post-the-inventory-transfer-journal"></a><span data-ttu-id="11015-138">Bóka færslubóka fyrir birgðaflutning</span><span class="sxs-lookup"><span data-stu-id="11015-138">Post the inventory transfer journal</span></span>
1. <span data-ttu-id="11015-139">Í **Aðgerðasvæðinu** skaltu smella á **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="11015-139">On the **Action pane**, click **Post**.</span></span>
2. <span data-ttu-id="11015-140">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="11015-140">Click **OK**.</span></span>

## <a name="view-inventory-transactions"></a><span data-ttu-id="11015-141">Skoða birgðafærslur</span><span class="sxs-lookup"><span data-stu-id="11015-141">View inventory transactions</span></span>
1. <span data-ttu-id="11015-142">Smelltu á **Birgðir**.</span><span class="sxs-lookup"><span data-stu-id="11015-142">Click **Inventory**.</span></span>
2. <span data-ttu-id="11015-143">Smelltu á **Færslur**.</span><span class="sxs-lookup"><span data-stu-id="11015-143">Click **Transactions**.</span></span> <span data-ttu-id="11015-144">Hér er hægt að sjá færslurnar sem voru stofnaðar þegar þitt færslubók var bókuð.</span><span class="sxs-lookup"><span data-stu-id="11015-144">Here you can see the transactions that were created when you posted your journal.</span></span>  

