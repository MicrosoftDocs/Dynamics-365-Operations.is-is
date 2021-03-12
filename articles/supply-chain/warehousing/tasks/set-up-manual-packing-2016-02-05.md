---
title: Setja upp handvirka pökkun (febrúar 2016 & maí 2016)
description: Pökkunarferli gerir kleift að sannprófa og pakka afurðir í gáma.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSParameters, WHSContainerType, WHSPackProfile, WHSCloseContainerProfile, InventLocationIdLookup, UnitOfMeasureLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 84a405b2a0afa3541fa0d691d751ecea0ad6606a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4976989"
---
# <a name="set-up-manual-packing-february-2016--may-2016"></a><span data-ttu-id="23e1f-103">Setja upp handvirka pökkun (febrúar 2016 & maí 2016)</span><span class="sxs-lookup"><span data-stu-id="23e1f-103">Set up manual packing (February 2016 & May 2016)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="23e1f-104">Pökkunarferli gerir kleift að sannprófa og pakka afurðir í gáma.</span><span class="sxs-lookup"><span data-stu-id="23e1f-104">The packing process allows you to validate and pack products into containers.</span></span> <span data-ttu-id="23e1f-105">Í þessu ferli starfsmenn vöruhússins taka vörur frá staðsetningum geymslu og flytja þær í pökkunarstöð þar sem þær athuga vörumagn og gerðir og úthluta þeim til viðeigandi gáma.</span><span class="sxs-lookup"><span data-stu-id="23e1f-105">In this process, warehouse workers pick products from the storage locations and move them to a packing station where they check the item quantities and types, and assign them to appropriate containers.</span></span> <span data-ttu-id="23e1f-106">Þegar gámur er alveg fullur, geta þeir loka honum og færa hana til úthliða, og vörurnar eru tilbúnar til sendingar.</span><span class="sxs-lookup"><span data-stu-id="23e1f-106">When a container is fully packed, they can close it and move it to the outbound docks, and the products are ready to ship.</span></span> <span data-ttu-id="23e1f-107">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="23e1f-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="23e1f-108">Þetta ferli er fyrir Febrúar 2016 og Maí 2016 útgáfur af Dynamics 365 for Operations eingöngu.</span><span class="sxs-lookup"><span data-stu-id="23e1f-108">This procedure is for the February 2016 & May 2016 versions of Dynamics 365 for Operations only.</span></span>


## <a name="set-up-location-profiles"></a><span data-ttu-id="23e1f-109">Setja upp forstillingar staðsetningar</span><span class="sxs-lookup"><span data-stu-id="23e1f-109">Set up location profiles</span></span>
1. <span data-ttu-id="23e1f-110">Fara í vöruhúsakerfi > Uppsetning > Vöruhús > Forstillingar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="23e1f-110">Go to Warehouse management > Setup > Warehouse > Location profiles.</span></span>
2. <span data-ttu-id="23e1f-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="23e1f-111">Click New.</span></span>
    * <span data-ttu-id="23e1f-112">Forstilling staðsetningar er notað fyrir pökkunarstöðvar og inniheldur upplýsingar um og reglur fyrir staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="23e1f-112">The location profile is used for packing stations and contains information and rules for a location.</span></span>  
3. <span data-ttu-id="23e1f-113">Færa inn gildi í reitnum Kenni forstillingar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="23e1f-113">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="23e1f-114">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="23e1f-114">In the Name field, type a value.</span></span>
5. <span data-ttu-id="23e1f-115">Sláðu inn eða veldu gildi í reitnum Staðsetningarsnið</span><span class="sxs-lookup"><span data-stu-id="23e1f-115">In the Location format field, enter or select a value.</span></span>
6. <span data-ttu-id="23e1f-116">Færa inn eða veljið gildi í svæðinu gerð staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="23e1f-116">In the Location type field, enter or select a value.</span></span>
7. <span data-ttu-id="23e1f-117">Velja skal Já í svæðinu Leyfa blandaðar vörur.</span><span class="sxs-lookup"><span data-stu-id="23e1f-117">Select Yes in the Allow mixed items field.</span></span>
8. <span data-ttu-id="23e1f-118">Velja skal Já í svæðinu Leyfa blandað birgðastaða.</span><span class="sxs-lookup"><span data-stu-id="23e1f-118">Select Yes in the Allow mixed  inventory statuses field.</span></span>
9. <span data-ttu-id="23e1f-119">Velja skal Já í Hnekkja reglum fyrir runudaga svæði.</span><span class="sxs-lookup"><span data-stu-id="23e1f-119">Select Yes in the Override rules for batch days field.</span></span>
10. <span data-ttu-id="23e1f-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="23e1f-120">Close the page.</span></span>

## <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="23e1f-121">Setja upp færibreytur vöruhúsastjórnunar</span><span class="sxs-lookup"><span data-stu-id="23e1f-121">Set up warehouse management parameters</span></span> 
1. <span data-ttu-id="23e1f-122">Fara í vöruhúsakerfi > Uppsetning > Færibreytur vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="23e1f-122">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="23e1f-123">Smella á pökkunarflipann</span><span class="sxs-lookup"><span data-stu-id="23e1f-123">Click the Packing tab.</span></span>
3. <span data-ttu-id="23e1f-124">Veldu eða settu inn gildi í reitinn kenni forstillingar fyrir pökkunarstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="23e1f-124">In the Profile ID for packing location field, enter or select a value.</span></span>
    * <span data-ttu-id="23e1f-125">Velja forstillingu staðsetningar sem á að nota fyrir pökkun.</span><span class="sxs-lookup"><span data-stu-id="23e1f-125">Select the location profile that you want to use for packing.</span></span>  
4. <span data-ttu-id="23e1f-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="23e1f-126">Close the page.</span></span>

## <a name="set-up-container-types"></a><span data-ttu-id="23e1f-127">Setja upp gámagerðir</span><span class="sxs-lookup"><span data-stu-id="23e1f-127">Set up container types</span></span>
1. <span data-ttu-id="23e1f-128">Fara í vöruhúsakerfi > Uppsetningu > Gáma > gámagerðir.</span><span class="sxs-lookup"><span data-stu-id="23e1f-128">Go to Warehouse management > Setup > Containers > Container types.</span></span>
2. <span data-ttu-id="23e1f-129">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="23e1f-129">Click New.</span></span>
    * <span data-ttu-id="23e1f-130">Hægt er að skilgreina gerðir gáma til að nota.</span><span class="sxs-lookup"><span data-stu-id="23e1f-130">You can define the types of containers to use.</span></span> <span data-ttu-id="23e1f-131">Þú getur tilgreint efnisleg vídd ílátsins, þar á meðal töruþungi, hámarks þyngd, hámarksrúmmál, lengd, breidd og þyngd.</span><span class="sxs-lookup"><span data-stu-id="23e1f-131">You can specify the physical dimensions of the container, including tare weight, maximum weight, maximum volume, length, width, and weight.</span></span>  <span data-ttu-id="23e1f-132">Eigindirnar eru sérsniðnir reitir sem leyfa þér að bæta fleiri víddum við gámagerð.</span><span class="sxs-lookup"><span data-stu-id="23e1f-132">The Attributes are customized fields that allow you to add extra dimensions on the container type.</span></span>     
3. <span data-ttu-id="23e1f-133">Færa inn gildi í svæðinu kóði gámagerðar.</span><span class="sxs-lookup"><span data-stu-id="23e1f-133">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="23e1f-134">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="23e1f-134">In the Description field, type a value.</span></span>
5. <span data-ttu-id="23e1f-135">Í reitinn Umbúðaþyngd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="23e1f-135">In the Tare weight field, enter a number.</span></span>
6. <span data-ttu-id="23e1f-136">Í reitinn hámarksþyngd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="23e1f-136">In the Maximum weight field, enter a number.</span></span>
7. <span data-ttu-id="23e1f-137">Í reitinn Magn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="23e1f-137">In the Volume field, enter a number.</span></span>
8. <span data-ttu-id="23e1f-138">Í reitinn Lengd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="23e1f-138">In the Length field, enter a number.</span></span>
9. <span data-ttu-id="23e1f-139">Færið númer inn í svæðið breidd.</span><span class="sxs-lookup"><span data-stu-id="23e1f-139">In the Width field, enter a number.</span></span>
10. <span data-ttu-id="23e1f-140">Færið númer inn í svæðið hæð.</span><span class="sxs-lookup"><span data-stu-id="23e1f-140">In the Height field, enter a number.</span></span>
11. <span data-ttu-id="23e1f-141">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="23e1f-141">Click Save.</span></span>
12. <span data-ttu-id="23e1f-142">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="23e1f-142">Close the page.</span></span>

## <a name="set-up-packing-profiles"></a><span data-ttu-id="23e1f-143">Setja upp pökkunarforstillingar</span><span class="sxs-lookup"><span data-stu-id="23e1f-143">Set up packing profiles</span></span>
1. <span data-ttu-id="23e1f-144">Fara í vöruhúsakerfi > Uppsetning > Pökkun > Forstillingar umbúða.</span><span class="sxs-lookup"><span data-stu-id="23e1f-144">Go to Warehouse management > Setup > Packing > Packing profiles.</span></span>
2. <span data-ttu-id="23e1f-145">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="23e1f-145">Click New.</span></span>
3. <span data-ttu-id="23e1f-146">Í reitinn auðkenni forstilling umbúða skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="23e1f-146">In the Packing profile ID field, type a value.</span></span>
4. <span data-ttu-id="23e1f-147">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="23e1f-147">In the Description field, type a value.</span></span>
5. <span data-ttu-id="23e1f-148">Færa inn eða veljið gildi í reit fyrir auðkenni lokunarreglu gáms.</span><span class="sxs-lookup"><span data-stu-id="23e1f-148">In the Container closing profile ID field, enter or select a value.</span></span>
    * <span data-ttu-id="23e1f-149">Auðkenni lokunarreglu gáms er valfrjálst og er sjálfgefin forstillingu lokunar gáms fyrir þessa forstillingu umbúða.</span><span class="sxs-lookup"><span data-stu-id="23e1f-149">A container closing profile ID is optional and is the default close container profile for this packing profile.</span></span>  
6. <span data-ttu-id="23e1f-150">Í reitnum auðkennisstilling gáms velurðu valkost.</span><span class="sxs-lookup"><span data-stu-id="23e1f-150">In the Container ID mode field, select an option.</span></span>
    * <span data-ttu-id="23e1f-151">Þessi valkostur ákvarðar hvort kenni gáms verður sjálfkrafa myndað þegar gámur er stofnaður eða ef kenni gáms verður búið til handvirkt.</span><span class="sxs-lookup"><span data-stu-id="23e1f-151">This option determines whether a container ID will be automatically generated when a container is created or if a container ID will be created manually.</span></span>  
7. <span data-ttu-id="23e1f-152">Færa inn eða veljið gildi í svæðinu gerð gáms.</span><span class="sxs-lookup"><span data-stu-id="23e1f-152">In the Container type field, enter or select a value.</span></span>
    * <span data-ttu-id="23e1f-153">Gámagerð er notuð að sjálfgefnu þegar nýjum gámi er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="23e1f-153">The container type will be used by default when a new container is created.</span></span>  
8. <span data-ttu-id="23e1f-154">Velja Stofna sjálfkrafa gám við lokun gáms gátreitur.</span><span class="sxs-lookup"><span data-stu-id="23e1f-154">Select the Autocreate container at container close check box.</span></span>
9. <span data-ttu-id="23e1f-155">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="23e1f-155">Click Save.</span></span>
10. <span data-ttu-id="23e1f-156">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="23e1f-156">Close the page.</span></span>

## <a name="set-up-container-closing-profiles"></a><span data-ttu-id="23e1f-157">Setja upp lokunarreglu gáms</span><span class="sxs-lookup"><span data-stu-id="23e1f-157">Set up container closing profiles</span></span>
1. <span data-ttu-id="23e1f-158">Fara í vöruhúsakerfi > Uppsetningu > Gáma > Lokunarregla gáms.</span><span class="sxs-lookup"><span data-stu-id="23e1f-158">Go to Warehouse management > Setup > Containers > Container closing profiles.</span></span>
    * <span data-ttu-id="23e1f-159">Lokunarreglur gáma skilgreina hvað gerist þegar gámi er lokað.</span><span class="sxs-lookup"><span data-stu-id="23e1f-159">Container closing profiles define what happens when a container is closed.</span></span> <span data-ttu-id="23e1f-160">Þú getur sett upp margar forstillingar fyrir lokun gáms.</span><span class="sxs-lookup"><span data-stu-id="23e1f-160">You can set up multiple close container profiles.</span></span>       
2. <span data-ttu-id="23e1f-161">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="23e1f-161">Click New.</span></span>
3. <span data-ttu-id="23e1f-162">Færa inn gildi í reit fyrir auðkenni lokunarreglu gáms.</span><span class="sxs-lookup"><span data-stu-id="23e1f-162">In the Container closing profile ID field, type a value.</span></span>
4. <span data-ttu-id="23e1f-163">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="23e1f-163">In the Description field, type a value.</span></span>
5. <span data-ttu-id="23e1f-164">Í reitnum Skrá skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="23e1f-164">In the Manifest at field, select an option.</span></span>
    * <span data-ttu-id="23e1f-165">Tilgreina hvort skráning munu eiga sér stað þegar gáma er lokað eða þegar sending er staðfest.</span><span class="sxs-lookup"><span data-stu-id="23e1f-165">Specify whether manifesting will occur when closing containers or when confirming the shipment.</span></span> <span data-ttu-id="23e1f-166">Athugið að skráning krefst flutningsstjórnun.</span><span class="sxs-lookup"><span data-stu-id="23e1f-166">Note that manifesting requires Transportation management.</span></span> <span data-ttu-id="23e1f-167">Verður að innleiða skráningu í flutningsstjórnunarvélar til þess að virka</span><span class="sxs-lookup"><span data-stu-id="23e1f-167">Manifesting must be implemented in the transportation engines in order for it work.</span></span>  
6. <span data-ttu-id="23e1f-168">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="23e1f-168">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="23e1f-169">Í reitinn sjálfgefin staðsetning lokasendingar skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="23e1f-169">In the Default location for final shipment field, enter or select a value.</span></span>
    * <span data-ttu-id="23e1f-170">Þetta verður staðsetning sem vörur verða færð á eftir gámarnir eru lokaðar.</span><span class="sxs-lookup"><span data-stu-id="23e1f-170">This will be location to which products will be moved after the containers are closed.</span></span> <span data-ttu-id="23e1f-171">Þessi staðsetningar þarf að hafa forstillingu fyrir staðsetningu skilgreinda í færibreytur vörugeymslu.</span><span class="sxs-lookup"><span data-stu-id="23e1f-171">This location must have a location profile defined on Warehouse parameters.</span></span>  
8. <span data-ttu-id="23e1f-172">Í reitinn þyngdareining skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="23e1f-172">In the Weight unit field, enter or select a value.</span></span>
9. <span data-ttu-id="23e1f-173">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="23e1f-173">Click Save.</span></span>

