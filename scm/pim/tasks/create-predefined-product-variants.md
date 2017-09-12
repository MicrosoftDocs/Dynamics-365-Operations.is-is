--- 
title: "Stofna forskilgreind afurðarafbrigði"
description: "Þetta ferli fer í gegnum stofnun afurðarafbrigða fyrir afurðarsniðmát með samsetningum fyrir afurðavíddir."
author: BibiSp
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: fa23f1449e750b4ed1c0f631a98c42b18b7dbb40
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="75b99-103">Stofna forskilgreind afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="75b99-103">Create predefined product variants</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="75b99-104">Þetta ferli fer í gegnum stofnun afurðarafbrigða fyrir afurðarsniðmát með samsetningum fyrir afurðavíddir.</span><span class="sxs-lookup"><span data-stu-id="75b99-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="75b99-105">Sýnifyrirtækið sem er notað til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="75b99-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="75b99-106">Stofna aðalsniðmát</span><span class="sxs-lookup"><span data-stu-id="75b99-106">Create a product master</span></span>
1. <span data-ttu-id="75b99-107">Fara í Upplýsingastjórnun afurða > Afurðir > Afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="75b99-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="75b99-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="75b99-108">Click New.</span></span>
3. <span data-ttu-id="75b99-109">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="75b99-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="75b99-110">Að færa inn afurðarnúmer handvirkt er aðeins áskilið ef engin númeraröð hefur verið sett upp fyrir svæðið afurðarnúmer.</span><span class="sxs-lookup"><span data-stu-id="75b99-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="75b99-111">Með öðrum orðum skal sleppa skrefinu ef númeraröð hefur verið valin fyrir reitinn.</span><span class="sxs-lookup"><span data-stu-id="75b99-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="75b99-112">Sláið inn gildi í reitinn Afurðarheiti.</span><span class="sxs-lookup"><span data-stu-id="75b99-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="75b99-113">Í reitinn afurðarvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="75b99-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="75b99-114">Veldu Afurðavíddaflokkurinn SizeCol (stærð og Litur)</span><span class="sxs-lookup"><span data-stu-id="75b99-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="75b99-115">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="75b99-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="75b99-116">Bæta við afurðarvíddir</span><span class="sxs-lookup"><span data-stu-id="75b99-116">Add product dimensions</span></span>
1. <span data-ttu-id="75b99-117">Smella á afurðarvíddir</span><span class="sxs-lookup"><span data-stu-id="75b99-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="75b99-118">Þetta dæmi sýnir hvernig á að færa inn afurðarvíddir handvirkt.</span><span class="sxs-lookup"><span data-stu-id="75b99-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="75b99-119">Einnig er hægt að velja stærð, lit eða stílflokk sem inniheldur afurðarvíddargildi sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="75b99-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="75b99-120">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="75b99-120">Click New.</span></span>
3. <span data-ttu-id="75b99-121">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="75b99-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="75b99-122">Sláið inn eða veldu gildi í reitnum stærð.</span><span class="sxs-lookup"><span data-stu-id="75b99-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="75b99-123">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="75b99-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="75b99-124">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="75b99-124">Click New.</span></span>
7. <span data-ttu-id="75b99-125">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="75b99-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="75b99-126">Sláið inn eða veldu gildi í reitnum stærð.</span><span class="sxs-lookup"><span data-stu-id="75b99-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="75b99-127">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="75b99-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="75b99-128">Smellið á flipann litur.</span><span class="sxs-lookup"><span data-stu-id="75b99-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="75b99-129">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="75b99-129">Click New.</span></span>
12. <span data-ttu-id="75b99-130">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="75b99-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="75b99-131">Sláið inn eða veldu gildi í reitnum litur.</span><span class="sxs-lookup"><span data-stu-id="75b99-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="75b99-132">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="75b99-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="75b99-133">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="75b99-133">Click New.</span></span>
16. <span data-ttu-id="75b99-134">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="75b99-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="75b99-135">Sláið inn eða veldu gildi í reitnum litur.</span><span class="sxs-lookup"><span data-stu-id="75b99-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="75b99-136">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="75b99-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="75b99-137">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="75b99-137">Click Save.</span></span>
20. <span data-ttu-id="75b99-138">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="75b99-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="75b99-139">Stofna afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="75b99-139">Generate product variants</span></span>
1. <span data-ttu-id="75b99-140">Smella á afurðaafbrigði</span><span class="sxs-lookup"><span data-stu-id="75b99-140">Click Product variants.</span></span>
2. <span data-ttu-id="75b99-141">Smella á Tillögur um afbrigði</span><span class="sxs-lookup"><span data-stu-id="75b99-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="75b99-142">Smelltu á Velja allt.</span><span class="sxs-lookup"><span data-stu-id="75b99-142">Click Select all.</span></span>
    * <span data-ttu-id="75b99-143">Allar mögulegar afbrigði eru valin í þessu dæmi.</span><span class="sxs-lookup"><span data-stu-id="75b99-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="75b99-144">Ef aðeins hlutmengi mögulegar afurðarvíddarsamsetningar verður notuð til að stofna afbrigði, er hægt að velja einstakar færslur.</span><span class="sxs-lookup"><span data-stu-id="75b99-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="75b99-145">Smellið á „Stofna“.</span><span class="sxs-lookup"><span data-stu-id="75b99-145">Click Create.</span></span>
    * <span data-ttu-id="75b99-146">Hægt er að mynda lýsingar fyrir öll afbrigði á grundvelli samsetninga á afurðarvíddargildum.</span><span class="sxs-lookup"><span data-stu-id="75b99-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="75b99-147">Lýsing er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="75b99-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="75b99-148">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="75b99-148">Click Save.</span></span>


