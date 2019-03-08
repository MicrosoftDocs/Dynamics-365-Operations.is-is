---
title: Stofna forskilgreind afurðarafbrigði
description: Þetta ferli fer í gegnum stofnun afurðarafbrigða fyrir afurðarsniðmát með samsetningum fyrir afurðavíddir.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab4f43957f7c661349714dbb0933ac3c1d19ab0e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "349815"
---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="1d4a5-103">Stofna forskilgreind afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="1d4a5-103">Create predefined product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1d4a5-104">Þetta ferli fer í gegnum stofnun afurðarafbrigða fyrir afurðarsniðmát með samsetningum fyrir afurðavíddir.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="1d4a5-105">Sýnifyrirtækið sem er notað til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="1d4a5-106">Stofna aðalsniðmát</span><span class="sxs-lookup"><span data-stu-id="1d4a5-106">Create a product master</span></span>
1. <span data-ttu-id="1d4a5-107">Fara í Upplýsingastjórnun afurða > Afurðir > Afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="1d4a5-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-108">Click New.</span></span>
3. <span data-ttu-id="1d4a5-109">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="1d4a5-110">Að færa inn afurðarnúmer handvirkt er aðeins áskilið ef engin númeraröð hefur verið sett upp fyrir svæðið afurðarnúmer.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="1d4a5-111">Með öðrum orðum skal sleppa skrefinu ef númeraröð hefur verið valin fyrir reitinn.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="1d4a5-112">Sláið inn gildi í reitinn Afurðarheiti.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="1d4a5-113">Í reitinn afurðarvíddarflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="1d4a5-114">Veldu Afurðavíddaflokkurinn SizeCol (stærð og Litur)</span><span class="sxs-lookup"><span data-stu-id="1d4a5-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="1d4a5-115">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="1d4a5-116">Bæta við afurðarvíddir</span><span class="sxs-lookup"><span data-stu-id="1d4a5-116">Add product dimensions</span></span>
1. <span data-ttu-id="1d4a5-117">Smella á afurðarvíddir</span><span class="sxs-lookup"><span data-stu-id="1d4a5-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="1d4a5-118">Þetta dæmi sýnir hvernig á að færa inn afurðarvíddir handvirkt.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="1d4a5-119">Einnig er hægt að velja stærð, lit eða stílflokk sem inniheldur afurðarvíddargildi sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="1d4a5-120">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-120">Click New.</span></span>
3. <span data-ttu-id="1d4a5-121">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="1d4a5-122">Sláið inn eða veldu gildi í reitnum stærð.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="1d4a5-123">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="1d4a5-124">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-124">Click New.</span></span>
7. <span data-ttu-id="1d4a5-125">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="1d4a5-126">Sláið inn eða veldu gildi í reitnum stærð.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="1d4a5-127">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="1d4a5-128">Smellið á flipann litur.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="1d4a5-129">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-129">Click New.</span></span>
12. <span data-ttu-id="1d4a5-130">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="1d4a5-131">Sláið inn eða veldu gildi í reitnum litur.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="1d4a5-132">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="1d4a5-133">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-133">Click New.</span></span>
16. <span data-ttu-id="1d4a5-134">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="1d4a5-135">Sláið inn eða veldu gildi í reitnum litur.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="1d4a5-136">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="1d4a5-137">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-137">Click Save.</span></span>
20. <span data-ttu-id="1d4a5-138">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="1d4a5-139">Stofna afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="1d4a5-139">Generate product variants</span></span>
1. <span data-ttu-id="1d4a5-140">Smella á afurðaafbrigði</span><span class="sxs-lookup"><span data-stu-id="1d4a5-140">Click Product variants.</span></span>
2. <span data-ttu-id="1d4a5-141">Smella á Tillögur um afbrigði</span><span class="sxs-lookup"><span data-stu-id="1d4a5-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="1d4a5-142">Smelltu á Velja allt.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-142">Click Select all.</span></span>
    * <span data-ttu-id="1d4a5-143">Allar mögulegar afbrigði eru valin í þessu dæmi.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="1d4a5-144">Ef aðeins hlutmengi mögulegar afurðarvíddarsamsetningar verður notuð til að stofna afbrigði, er hægt að velja einstakar færslur.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="1d4a5-145">Smellið á „Stofna“.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-145">Click Create.</span></span>
    * <span data-ttu-id="1d4a5-146">Hægt er að mynda lýsingar fyrir öll afbrigði á grundvelli samsetninga á afurðarvíddargildum.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="1d4a5-147">Lýsing er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="1d4a5-148">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="1d4a5-148">Click Save.</span></span>

