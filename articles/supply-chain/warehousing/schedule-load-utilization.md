---
title: Tímasetja álagsnýtingu
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp og tímasetja álag fyrir vöruhús.
author: MarkusFogelberg
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSSpaceUtilSetup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 15f3735f79671ac41789d39a5473722a5f35fde0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564833"
---
# <a name="schedule-load-utilization"></a><span data-ttu-id="baaff-103">Tímasetja álagsnýtingu</span><span class="sxs-lookup"><span data-stu-id="baaff-103">Schedule load utilization</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="baaff-104">Þú getur tímasett álagsnýtingu fyrir valdar gerðir staðsetninga og þú getur einnig gert ráð fyrir núverandi og framtíðarálagsnýtingu.</span><span class="sxs-lookup"><span data-stu-id="baaff-104">You can schedule load utilization for selected location types, and you can also project the current and future load utilization.</span></span> <span data-ttu-id="baaff-105">Þú getur áætlað álagið fyrir eitt eða fleiri svæði, fyrir álagseiningarnar (svæði eða vöruhús) eða fyrir samsetningu af svæði og vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="baaff-105">You can project the load for one or more sites, for the load units (zone or warehouse), or for a combination of a zone and a warehouse.</span></span>

## <a name="schedule-and-view-the-load-for-a-warehouse-or-site"></a><span data-ttu-id="baaff-106">Raða og skoða álag fyrir vöruhús eða staðsetningu</span><span class="sxs-lookup"><span data-stu-id="baaff-106">Schedule and view the load for a warehouse or site</span></span>

<span data-ttu-id="baaff-107">Til að raða álaginu fyrir svæði, vöruhús, eða staði er búin til uppsetning plássnotkunar og hún tengd aðaláætlun.</span><span class="sxs-lookup"><span data-stu-id="baaff-107">To schedule the load for sites, warehouses, or zones, you create a space utilization setup and associate it with a master plan.</span></span>

<span data-ttu-id="baaff-108">Í uppsetningu plássnotkunar notarðu gerðir staðsetninga, t.d. **Magnstaðsetning** og **Tínslustaður** til að tilgreina hvernig eigi að áætla plássnotkun.</span><span class="sxs-lookup"><span data-stu-id="baaff-108">In the space utilization setup, you use location types, such as **Bulk location** and **Picking location**, to specify how space utilization should be projected.</span></span> <span data-ttu-id="baaff-109">Þú tilgreinir einnig geymsluálagsstillingu, eins og **Svæði**.</span><span class="sxs-lookup"><span data-stu-id="baaff-109">You also specify a storage load mode, such as **Zone**.</span></span>

<span data-ttu-id="baaff-110">Vörpun framvirkrar plássnotkunar er grundvöllum á upplýsingum sem eru reiknaðar samkvæmt tengdri aðaláætlun.</span><span class="sxs-lookup"><span data-stu-id="baaff-110">The projection of future space utilization is based on information that is calculated on the associated master plan.</span></span> <span data-ttu-id="baaff-111">Aðaláætlanir spá fyrir forðaáætlun fyrir pantanir á innleið og útleið fyrir framleiðslu og aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="baaff-111">Master plans forecast the resource planning for incoming and outgoing orders for production and operations.</span></span> <span data-ttu-id="baaff-112">Vörpun tiltæks pláss er grundvölluð á sambandinu á milli uppsetningar plássnotkunar og valinnar aðaláætlunar.</span><span class="sxs-lookup"><span data-stu-id="baaff-112">The projection of available space is based on the relation between the space utilization setup and the selected master plan.</span></span>

<span data-ttu-id="baaff-113">Með því að nota geymsluálagsstillinguna sem þú valdir í uppsetningu plássnotkunar, getur þú tilgreint hvort álagið skuli áætlað fyrir hvert vöruhús eða svæði, eða hvort áætlanirnar ætti að innihalda upplýsingar um bæði vöruhús og svæði.</span><span class="sxs-lookup"><span data-stu-id="baaff-113">By using the storage load mode that you selected in the space utilization setup, you can specify whether the load should be projected for each warehouse or zone, or whether the projections should include information about both warehouses and zones.</span></span> <span data-ttu-id="baaff-114">Þú tilgreinir einnig hvort staðsetningar sem lokað hefur verið á verði ekki teknar með í útreikningi á álagsnýtingu.</span><span class="sxs-lookup"><span data-stu-id="baaff-114">You also specify whether blocked locations should be excluded from the calculation of load utilization.</span></span>

<span data-ttu-id="baaff-115">Þú getur spáð fyrir um plássnotkun með því að búa til skýrsluna **Álagsnýting í vöruhúsi**.</span><span class="sxs-lookup"><span data-stu-id="baaff-115">You can project the space utilization by generating the **Warehouse load utilization** report.</span></span> <span data-ttu-id="baaff-116">Þegar þú býrð til þessa skýrslu er hægt að tilgreina hvort álagsnýtingin eigi að vera áætluð fyrir hvert svæði eða fyrir valda álagseiningu, t.d. svæði eða vöruhús.</span><span class="sxs-lookup"><span data-stu-id="baaff-116">When you generate this report, you can specify whether the load utilization should be projected for each site, across sites, or for the selected load unit, such as zone or warehouse.</span></span>

### <a name="create-a-space-utilization-setup-for-a-warehouse"></a><span data-ttu-id="baaff-117">Búa til uppsetningu plássnotkunar fyrir vöruhús</span><span class="sxs-lookup"><span data-stu-id="baaff-117">Create a space utilization setup for a warehouse</span></span>

1. <span data-ttu-id="baaff-118">Veldu **Birgðastjórnun** \> **Uppsetning** \> **Vöktun vöruhúss** \> **Plássnotkun**.</span><span class="sxs-lookup"><span data-stu-id="baaff-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Space utilization**.</span></span>
2. <span data-ttu-id="baaff-119">Veldu **Nýtt** til að búa til uppsetningu plássnotkunar.</span><span class="sxs-lookup"><span data-stu-id="baaff-119">Select **New** to create a space utilization setup.</span></span> <span data-ttu-id="baaff-120">Tilgreindu auðkenni og heiti fyrir nýju uppsetninguna.</span><span class="sxs-lookup"><span data-stu-id="baaff-120">Specify an ID and a name for the new setup.</span></span>
3. <span data-ttu-id="baaff-121">Í reitnum **Geymsluálagsstilling** skal velja hvort yfirlit plássnotkunar eigi að sýna upplýsingar eftir vöruhúsi, svæði eða vöruhúsi og svæði.</span><span class="sxs-lookup"><span data-stu-id="baaff-121">In the **Storage load mode** field, select whether the overview of space utilization should show information by warehouse, zone, or warehouse and zone.</span></span>
4. <span data-ttu-id="baaff-122">Stilltu valkostinn **Ekki taka með útilokaðar staðsetningar** á **Já** til að taka birgðastaðsetningar sem hefur verið lokað á ekki með í útreikninginn á tiltæku plássi.</span><span class="sxs-lookup"><span data-stu-id="baaff-122">Set the **Exclude blocked locations** option to **Yes** to exclude blocked inventory locations from the calculation of available space.</span></span> <span data-ttu-id="baaff-123">Þú getur lokað á birgðastaðsetningu fyrir inntak og úttak með því að tilgreina ástæðu útilokunar fyrir staðsetninguna í reitunum **Inntak útilokað** eða **Úttak útilokað** á flýtiflipanum **Annað** á síðunni **Birgðastaðsetningar**.</span><span class="sxs-lookup"><span data-stu-id="baaff-123">You can block an inventory location for input and output by specifying a blocking cause for the location in the **Input blocked** or **Output blocked** field on the **Other** FastTab on the **Inventory locations** page.</span></span>
5. <span data-ttu-id="baaff-124">Á flýtiflipanum **Gerð staðsetningar** skaltu velja gerðir staðsetninga sem eru teknar með í útreikningi á plássnotkun.</span><span class="sxs-lookup"><span data-stu-id="baaff-124">On the **Location type** FastTab, select the location types to include in the space utilization calculation.</span></span> <span data-ttu-id="baaff-125">Velja verður í það minnsta eina staðsetningargerð fyrir spána.</span><span class="sxs-lookup"><span data-stu-id="baaff-125">You must select at least one location type for the projection.</span></span>

### <a name="associate-a-space-utilization-setup-with-a-master-plan"></a><span data-ttu-id="baaff-126">Tengja uppsetningu plássnotkunar við aðaláætlun</span><span class="sxs-lookup"><span data-stu-id="baaff-126">Associate a space utilization setup with a master plan</span></span>

1. <span data-ttu-id="baaff-127">Veldu **Birgðastjórnun** \> **Reglubundin verkefni** \> **Tímasetja álagsnýtingu**.</span><span class="sxs-lookup"><span data-stu-id="baaff-127">Select **Inventory management** \> **Periodic tasks** \> **Schedule load utilization**.</span></span>
2. <span data-ttu-id="baaff-128">Í reitnum **Aðaláætlun** skal velja aðaláætlun.</span><span class="sxs-lookup"><span data-stu-id="baaff-128">In the **Master plan** field, select a master plan.</span></span>
3. <span data-ttu-id="baaff-129">Í reitnum **Fjöldi daga** skal tilgreina fjölda daga sem á að hafa með í áætlun á núverandi og framtíðarvinnuálagi.</span><span class="sxs-lookup"><span data-stu-id="baaff-129">In the **Number of days** field, specify the number of days to include in the projection of current and future workloads.</span></span>
4. <span data-ttu-id="baaff-130">Í reitnum **Plássnotkun** skal velja uppsetningu plássnotkunar til að nota fyrir áætlun á núverandi og framtíðarvinnuálagi.</span><span class="sxs-lookup"><span data-stu-id="baaff-130">In the **Space utilization** field, select the space utilization setup to use for the projection of current and future workloads.</span></span>

### <a name="specify-the-load-utilization-projection-and-view-information"></a><span data-ttu-id="baaff-131">Tilgreina spá fyrir álagsnýtingu og skoða upplýsingar</span><span class="sxs-lookup"><span data-stu-id="baaff-131">Specify the load utilization projection and view information</span></span>

1. <span data-ttu-id="baaff-132">Veldu **Birgðastjórnun** \> **Fyrirspurnir og skýrslur** \> **Efnislegar birgðarskýrslur** \> **Álagsnýting í vöruhúsi**.</span><span class="sxs-lookup"><span data-stu-id="baaff-132">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Warehouse load utilization**.</span></span>
2. <span data-ttu-id="baaff-133">Í reitnum **Sýna eftir** skaltu velja stig áætlunar á plássnotkun:</span><span class="sxs-lookup"><span data-stu-id="baaff-133">In the **Show by** field, select the level of the space utilization projection:</span></span>

    - <span data-ttu-id="baaff-134">**Svæði** - Spá fyrir um plássnotkun fyrir hvert svæði.</span><span class="sxs-lookup"><span data-stu-id="baaff-134">**Site** – Project the space utilization for each site.</span></span> <span data-ttu-id="baaff-135">Þessi spá er gagnleg, til dæmis ef skoða á öll vöruhús fyrir svæði þannig að hægt sé að jafna plássnotkun á milli vöruhúsa.</span><span class="sxs-lookup"><span data-stu-id="baaff-135">This projection is useful if, for example, you want to view all the warehouses for a site so that you can balance the space utilization between the warehouses.</span></span>
    - <span data-ttu-id="baaff-136">**Álagseining** - Spá fyrir um plássnotkun fyrir svæði eða vöruhús.</span><span class="sxs-lookup"><span data-stu-id="baaff-136">**Load unit** – Project the space utilization for zones or warehouses.</span></span> <span data-ttu-id="baaff-137">Laust pláss er síðan áætlað í samræmi við gildið sem þú valdir í reitnum **Geymsluálagsstilling** á síðunni **Plássnotkun** þegar þú bjóst til uppsetningu plássnotkunar.</span><span class="sxs-lookup"><span data-stu-id="baaff-137">The available space is then projected according to the value that you selected in the **Storage load mode** field on the **Space utilization** page when you created the space utilization setup.</span></span>

3. <span data-ttu-id="baaff-138">Fylgdu einu af þessum skrefum, fer eftir gildinu sem þú valdir í fyrra skrefi:</span><span class="sxs-lookup"><span data-stu-id="baaff-138">Follow one of these steps, depending on the value that you selected in the previous step:</span></span>

    - <span data-ttu-id="baaff-139">Ef þú hefur valið **Svæði** í reitnum **Sýna eftir** er reiturinn **Svæði** tiltækur.</span><span class="sxs-lookup"><span data-stu-id="baaff-139">If you selected **Site** in the **Show by** field, the **Site** field is available.</span></span> <span data-ttu-id="baaff-140">Veldu eitt eða fleiri svæði til að hafa með í spánni.</span><span class="sxs-lookup"><span data-stu-id="baaff-140">Select one or more sites to include in the projection.</span></span>
    - <span data-ttu-id="baaff-141">Ef þú valdir **Álagseining** í reitnum **Sýna eftir** er reiturinn **Álagseining** tiltækur.</span><span class="sxs-lookup"><span data-stu-id="baaff-141">If you selected **Load unit** in the **Show by** field, the **Load unit** field is available.</span></span> <span data-ttu-id="baaff-142">Veldu álagseininguna.</span><span class="sxs-lookup"><span data-stu-id="baaff-142">Select the load unit.</span></span>

4. <span data-ttu-id="baaff-143">Í reitnum **Álagsgerð** skaltu velja **Rúmmál** eða **Þyngd** til að tilgreina rekstrareiningu vöruhússins fyrir áætlun á plássi.</span><span class="sxs-lookup"><span data-stu-id="baaff-143">In the **Load type** field, select **Volume** or **Weight** to specify the warehouse operating unit to project space for.</span></span>
5. <span data-ttu-id="baaff-144">Í reitnum **Uppsetning plássnotkunar** skal velja uppsetningu plássnotkunar sem spáin á að byggjast á.</span><span class="sxs-lookup"><span data-stu-id="baaff-144">In the **Space utilization setup** field, select the space utilization setup that the projection should be based on.</span></span>
