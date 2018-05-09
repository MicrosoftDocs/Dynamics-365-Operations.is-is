--- 
title: "Setja upp handvirka pökkun (aðeins febrúar og maí 2016)"
description: "Pökkunarferli gerir kleift að sannprófa og pakka afurðir í gáma."
author: BibiSp
manager: AnnBe
ms.date: 11/04/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 714fd4762ae54f8f6638e81dd19fdd636091b88e
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-manual-packing-february--may-2016-only"></a><span data-ttu-id="384f7-103">Setja upp handvirka pökkun (aðeins febrúar og maí 2016)</span><span class="sxs-lookup"><span data-stu-id="384f7-103">Set up manual packing (February & May 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="384f7-104">Pökkunarferli gerir kleift að sannprófa og pakka afurðir í gáma.</span><span class="sxs-lookup"><span data-stu-id="384f7-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="384f7-105">Í þessu ferli starfsmenn vöruhússins taka vörur frá staðsetningum geymslu og flytja þær í pökkunarstöð þar sem þær athuga vörumagn og gerðir og úthluta þeim til viðeigandi gáma.</span><span class="sxs-lookup"><span data-stu-id="384f7-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="384f7-106">Þegar gámur er alveg fullur, geta þeir loka honum og færa hana til úthliða, og vörurnar eru tilbúnar til sendingar.</span><span class="sxs-lookup"><span data-stu-id="384f7-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="384f7-107">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="384f7-107">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="384f7-108">Setja upp forstillingar staðsetningar</span><span class="sxs-lookup"><span data-stu-id="384f7-108">Set up location profiles</span></span>
1. <span data-ttu-id="384f7-109">Fara í vöruhúsakerfi > Uppsetning > Vöruhús > Forstillingar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="384f7-109">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="384f7-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="384f7-110">Click New.</span></span>
    * <span data-ttu-id="384f7-111">Forstilling staðsetningar er notað fyrir pökkunarstöðvar og inniheldur upplýsingar um og reglur fyrir staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="384f7-111">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="384f7-112">Færa inn gildi í reitnum Kenni forstillingar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="384f7-112">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="384f7-113">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="384f7-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="384f7-114">Sláðu inn eða veldu gildi í reitnum Staðsetningarsnið</span><span class="sxs-lookup"><span data-stu-id="384f7-114">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="384f7-115">Færa inn eða veljið gildi í svæðinu gerð staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="384f7-115">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="384f7-116">Velja skal Já í svæðinu Leyfa blandaðar vörur.</span><span class="sxs-lookup"><span data-stu-id="384f7-116">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="384f7-117">Velja skal Já í svæðinu Leyfa blandað birgðastaða.</span><span class="sxs-lookup"><span data-stu-id="384f7-117">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="384f7-118">Velja skal Já í Hnekkja reglum fyrir runudaga svæði.</span><span class="sxs-lookup"><span data-stu-id="384f7-118">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="384f7-119">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="384f7-119">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="384f7-120">Setja upp færibreytur vöruhúsastjórnunar</span><span class="sxs-lookup"><span data-stu-id="384f7-120">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="384f7-121">Fara í vöruhúsakerfi > Uppsetning > Færibreytur vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="384f7-121">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="384f7-122">Smella á pökkunarflipann</span><span class="sxs-lookup"><span data-stu-id="384f7-122">Click the Packing tab.</span></span>
3. <span data-ttu-id="384f7-123">Veldu eða settu inn gildi í reitinn kenni forstillingar fyrir pökkunarstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="384f7-123">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="384f7-124">Velja forstillingu staðsetningar sem á að nota fyrir pökkun.</span><span class="sxs-lookup"><span data-stu-id="384f7-124">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="384f7-125">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="384f7-125">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="384f7-126">Setja upp gámagerðir</span><span class="sxs-lookup"><span data-stu-id="384f7-126">Set up container types</span></span>
1. <span data-ttu-id="384f7-127">Fara í vöruhúsakerfi  > Uppsetningu  > Gáma  > gámagerðir.</span><span class="sxs-lookup"><span data-stu-id="384f7-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="384f7-128">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="384f7-128">Click New.</span></span>
    * <span data-ttu-id="384f7-129">Hægt er að skilgreina gerðir gáma til að nota.</span><span class="sxs-lookup"><span data-stu-id="384f7-129">You can define the types of containers to use.</span></span> <span data-ttu-id="384f7-130">Þú getur tilgreint efnisleg vídd ílátsins, þar á meðal töruþungi, hámarks þyngd, hámarksrúmmál, lengd, breidd og þyngd.</span><span class="sxs-lookup"><span data-stu-id="384f7-130">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="384f7-131">Eigindirnar eru sérsniðnir reitir sem leyfa þér að bæta fleiri víddum við gámagerð.</span><span class="sxs-lookup"><span data-stu-id="384f7-131">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="384f7-132">Færa inn gildi í svæðinu kóði gámagerðar.</span><span class="sxs-lookup"><span data-stu-id="384f7-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="384f7-133">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="384f7-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="384f7-134">Í reitinn Umbúðaþyngd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="384f7-134">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="384f7-135">Í reitinn hámarksþyngd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="384f7-135">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="384f7-136">Í reitinn Magn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="384f7-136">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="384f7-137">Í reitinn Lengd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="384f7-137">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="384f7-138">Færið númer inn í svæðið breidd.</span><span class="sxs-lookup"><span data-stu-id="384f7-138">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="384f7-139">Færið númer inn í svæðið hæð.</span><span class="sxs-lookup"><span data-stu-id="384f7-139">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="384f7-140">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="384f7-140">Click Save.</span></span>
12. <span data-ttu-id="384f7-141">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="384f7-141">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="384f7-142">Setja upp pökkunarforstillingar</span><span class="sxs-lookup"><span data-stu-id="384f7-142">Set up packing profiles</span></span>
1. <span data-ttu-id="384f7-143">Fara í vöruhúsakerfi > Uppsetning > Pökkun > Forstillingar umbúða.</span><span class="sxs-lookup"><span data-stu-id="384f7-143">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="384f7-144">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="384f7-144">Click New.</span></span>
3. <span data-ttu-id="384f7-145">Í reitinn auðkenni forstilling umbúða skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="384f7-145">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="384f7-146">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="384f7-146">In the Description field, type a value.</span></span>
5. <span data-ttu-id="384f7-147">Færa inn eða veljið gildi í reit fyrir auðkenni lokunarreglu gáms.</span><span class="sxs-lookup"><span data-stu-id="384f7-147">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="384f7-148">Auðkenni lokunarreglu gáms er valfrjálst og er sjálfgefin forstillingu lokunar gáms fyrir þessa forstillingu umbúða.</span><span class="sxs-lookup"><span data-stu-id="384f7-148">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="384f7-149">Í reitnum auðkennisstilling gáms velurðu valkost.</span><span class="sxs-lookup"><span data-stu-id="384f7-149">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="384f7-150">Þessi valkostur ákvarðar hvort kenni gáms verður sjálfkrafa myndað þegar gámur er stofnaður eða ef kenni gáms verður búið til handvirkt.</span><span class="sxs-lookup"><span data-stu-id="384f7-150">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="384f7-151">Færa inn eða veljið gildi í svæðinu gerð gáms.</span><span class="sxs-lookup"><span data-stu-id="384f7-151">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="384f7-152">Gámagerð er notuð að sjálfgefnu þegar nýjum gámi er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="384f7-152">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="384f7-153">Velja Stofna sjálfkrafa gám við lokun gáms gátreitur.</span><span class="sxs-lookup"><span data-stu-id="384f7-153">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="384f7-154">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="384f7-154">Click Save.</span></span>
10. <span data-ttu-id="384f7-155">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="384f7-155">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="384f7-156">Setja upp lokunarreglu gáms</span><span class="sxs-lookup"><span data-stu-id="384f7-156">Set up container closing profiles</span></span>
1. <span data-ttu-id="384f7-157">Fara í vöruhúsakerfi > Uppsetningu > Gáma > Lokunarregla gáms.</span><span class="sxs-lookup"><span data-stu-id="384f7-157">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="384f7-158">Lokunarreglur gáma skilgreina hvað gerist þegar gámi er lokað.</span><span class="sxs-lookup"><span data-stu-id="384f7-158">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="384f7-159">Þú getur sett upp margar forstillingar fyrir lokun gáms.</span><span class="sxs-lookup"><span data-stu-id="384f7-159">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="384f7-160">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="384f7-160">Click New.</span></span>
3. <span data-ttu-id="384f7-161">Færa inn gildi í reit fyrir auðkenni lokunarreglu gáms.</span><span class="sxs-lookup"><span data-stu-id="384f7-161">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="384f7-162">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="384f7-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="384f7-163">Í reitnum Skrá skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="384f7-163">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="384f7-164">Tilgreina hvort skráning munu eiga sér stað þegar gáma er lokað eða þegar sending er staðfest.</span><span class="sxs-lookup"><span data-stu-id="384f7-164">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="384f7-165">Athugið að skráning krefst flutningsstjórnun.</span><span class="sxs-lookup"><span data-stu-id="384f7-165">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="384f7-166">Verður að innleiða skráningu í flutningsstjórnunarvélar til þess að virka</span><span class="sxs-lookup"><span data-stu-id="384f7-166">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="384f7-167">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="384f7-167">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="384f7-168">Í reitinn sjálfgefin staðsetning lokasendingar skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="384f7-168">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="384f7-169">Þetta verður staðsetning sem vörur verða færð á eftir gámarnir eru lokaðar.</span><span class="sxs-lookup"><span data-stu-id="384f7-169">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="384f7-170">Þessi staðsetningar þarf að hafa forstillingu fyrir staðsetningu skilgreinda í færibreytur vörugeymslu.</span><span class="sxs-lookup"><span data-stu-id="384f7-170">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="384f7-171">Í reitinn þyngdareining skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="384f7-171">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="384f7-172">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="384f7-172">Click Save.</span></span>


