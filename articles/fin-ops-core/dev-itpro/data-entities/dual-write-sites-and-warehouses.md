---
title: Innbyggð svæði og vöruhús
description: Þetta efni lýsir samþættingu svæðis- og vöruhúsgagna milli Finance and Operations og Common Data Service.
author: t-benebo
manager: AnnBe
ms.date: 10/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: benebotg
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-08-15
ms.openlocfilehash: 093f33e313bfb194ef932dffe9c9b5bcb84ae762
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569226"
---
# <a name="integrated-sites-and-warehouses"></a><span data-ttu-id="4f468-103">Innbyggð svæði og vöruhús</span><span class="sxs-lookup"><span data-stu-id="4f468-103">Integrated sites and warehouses</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="4f468-104">Þetta efni lýsir samþættingu svæðis- og vöruhúsgagna milli Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4f468-104">This topic describes the integration of site and warehouse data between Finance and Operations and Common Data Service.</span></span> <span data-ttu-id="4f468-105">Rekstrarsvæði og vöruhús eru algeng hugtök í forritinu Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="4f468-105">Operational sites and warehouses are common concepts in a Supply Chain Management application.</span></span> <span data-ttu-id="4f468-106">Þau eru notuð til að móta aðfangakeðju fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="4f468-106">They are used to model the supply chain of your company.</span></span>

## <a name="templates"></a><span data-ttu-id="4f468-107">Sniðmát</span><span class="sxs-lookup"><span data-stu-id="4f468-107">Templates</span></span>

<span data-ttu-id="4f468-108">Með samþættingunni við Common Data Service eru þessi hugtök og allar tengdar upplýsingar fáanleg í Common Data Service með því að nota gagnaeiningar svæðanna og vöruhúsanna í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="4f468-108">With the integration with Common Data Service, these concepts and all their related information are available in Common Data Service using the sites and warehouses data entities in the following table.</span></span>

<span data-ttu-id="4f468-109">Forrit Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="4f468-109">Finance and Operations apps</span></span> | <span data-ttu-id="4f468-110">Önnur Dynamics 365 forrit</span><span class="sxs-lookup"><span data-stu-id="4f468-110">Other Dynamics 365 apps</span></span>
--------------------------|---------------------------------
<span data-ttu-id="4f468-111">Svæði</span><span class="sxs-lookup"><span data-stu-id="4f468-111">Sites</span></span>                     | <span data-ttu-id="4f468-112">msdyn_operationalsites</span><span class="sxs-lookup"><span data-stu-id="4f468-112">msdyn_operationalsites</span></span>
<span data-ttu-id="4f468-113">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="4f468-113">Warehouses</span></span>                | <span data-ttu-id="4f468-114">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="4f468-114">warehouses</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="operational-sites"></a><span data-ttu-id="4f468-115">Rekstrarsvæði</span><span class="sxs-lookup"><span data-stu-id="4f468-115">Operational sites</span></span>

<span data-ttu-id="4f468-116">Rekstrarsvæðin eru fáanleg í Common Data Service með eftirfarandi vörpunum.</span><span class="sxs-lookup"><span data-stu-id="4f468-116">The operational sites are available in Common Data Service using the following mappings.</span></span>

<span data-ttu-id="4f468-117">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="4f468-117">Source field</span></span> | <span data-ttu-id="4f468-118">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="4f468-118">Map type</span></span> | <span data-ttu-id="4f468-119">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="4f468-119">Destination field</span></span>
---|---|---
<span data-ttu-id="4f468-120">SITENAME</span><span class="sxs-lookup"><span data-stu-id="4f468-120">SITENAME</span></span> | >< | <span data-ttu-id="4f468-121">msdyn_name</span><span class="sxs-lookup"><span data-stu-id="4f468-121">msdyn_name</span></span>
<span data-ttu-id="4f468-122">DEFAULTFINANCIALDIMENSIONVALUE</span><span class="sxs-lookup"><span data-stu-id="4f468-122">DEFAULTFINANCIALDIMENSIONVALUE</span></span> | >< | <span data-ttu-id="4f468-123">msdyn_defaultfinancialdimensionvalue</span><span class="sxs-lookup"><span data-stu-id="4f468-123">msdyn_defaultfinancialdimensionvalue</span></span>
<span data-ttu-id="4f468-124">DEFAULTINVENTORYSTATUSID</span><span class="sxs-lookup"><span data-stu-id="4f468-124">DEFAULTINVENTORYSTATUSID</span></span> | >< | <span data-ttu-id="4f468-125">msdyn_defaultinventorystatusid</span><span class="sxs-lookup"><span data-stu-id="4f468-125">msdyn_defaultinventorystatusid</span></span>
<span data-ttu-id="4f468-126">ISRECEIVINGWAREHOUSEOVERRIDEALLOWED</span><span class="sxs-lookup"><span data-stu-id="4f468-126">ISRECEIVINGWAREHOUSEOVERRIDEALLOWED</span></span> | >< | <span data-ttu-id="4f468-127">msdyn_isreceivingwarehouseoverrideallowed</span><span class="sxs-lookup"><span data-stu-id="4f468-127">msdyn_isreceivingwarehouseoverrideallowed</span></span>
<span data-ttu-id="4f468-128">SITEID</span><span class="sxs-lookup"><span data-stu-id="4f468-128">SITEID</span></span> | >< | <span data-ttu-id="4f468-129">msdyn_siteid</span><span class="sxs-lookup"><span data-stu-id="4f468-129">msdyn_siteid</span></span>
<span data-ttu-id="4f468-130">SITENAME</span><span class="sxs-lookup"><span data-stu-id="4f468-130">SITENAME</span></span> | >< | <span data-ttu-id="4f468-131">msdyn_sitename</span><span class="sxs-lookup"><span data-stu-id="4f468-131">msdyn_sitename</span></span>
<span data-ttu-id="4f468-132">TAXBRANCHCODE</span><span class="sxs-lookup"><span data-stu-id="4f468-132">TAXBRANCHCODE</span></span> | >< | <span data-ttu-id="4f468-133">msdyn_taxbranchcode</span><span class="sxs-lookup"><span data-stu-id="4f468-133">msdyn_taxbranchcode</span></span>
<span data-ttu-id="4f468-134">FISCALESTABLISHMENTID</span><span class="sxs-lookup"><span data-stu-id="4f468-134">FISCALESTABLISHMENTID</span></span> | >< | <span data-ttu-id="4f468-135">msdyn_fiscalestablishmentid</span><span class="sxs-lookup"><span data-stu-id="4f468-135">msdyn_fiscalestablishmentid</span></span>
<span data-ttu-id="4f468-136">ISPRIMARYADDRESSASSIGNED</span><span class="sxs-lookup"><span data-stu-id="4f468-136">ISPRIMARYADDRESSASSIGNED</span></span> | >< | <span data-ttu-id="4f468-137">msdyn_isprimaryaddressassigned</span><span class="sxs-lookup"><span data-stu-id="4f468-137">msdyn_isprimaryaddressassigned</span></span>
<span data-ttu-id="4f468-138">PRIMARYADDRESSCITY</span><span class="sxs-lookup"><span data-stu-id="4f468-138">PRIMARYADDRESSCITY</span></span> | >< | <span data-ttu-id="4f468-139">msdyn_primaryaddresscity</span><span class="sxs-lookup"><span data-stu-id="4f468-139">msdyn_primaryaddresscity</span></span>
<span data-ttu-id="4f468-140">PRIMARYADDRESSCOUNTRYREGIONID</span><span class="sxs-lookup"><span data-stu-id="4f468-140">PRIMARYADDRESSCOUNTRYREGIONID</span></span> | >< | <span data-ttu-id="4f468-141">msdyn_primaryaddresscountryregionid</span><span class="sxs-lookup"><span data-stu-id="4f468-141">msdyn_primaryaddresscountryregionid</span></span>
<span data-ttu-id="4f468-142">PRIMARYADDRESSCOUNTYID</span><span class="sxs-lookup"><span data-stu-id="4f468-142">PRIMARYADDRESSCOUNTYID</span></span> | >< | <span data-ttu-id="4f468-143">msdyn_primaryaddresscountyid</span><span class="sxs-lookup"><span data-stu-id="4f468-143">msdyn_primaryaddresscountyid</span></span>
<span data-ttu-id="4f468-144">PRIMARYADDRESSDISTRICTNAME</span><span class="sxs-lookup"><span data-stu-id="4f468-144">PRIMARYADDRESSDISTRICTNAME</span></span> | >< | <span data-ttu-id="4f468-145">msdyn_primaryaddressdistrictname</span><span class="sxs-lookup"><span data-stu-id="4f468-145">msdyn_primaryaddressdistrictname</span></span>
<span data-ttu-id="4f468-146">PRIMARYADDRESSLATITUDE</span><span class="sxs-lookup"><span data-stu-id="4f468-146">PRIMARYADDRESSLATITUDE</span></span> | >< | <span data-ttu-id="4f468-147">msdyn_primaryaddresslatitude</span><span class="sxs-lookup"><span data-stu-id="4f468-147">msdyn_primaryaddresslatitude</span></span>
<span data-ttu-id="4f468-148">PRIMARYADDRESSLOCATIONROLES</span><span class="sxs-lookup"><span data-stu-id="4f468-148">PRIMARYADDRESSLOCATIONROLES</span></span> | >< | <span data-ttu-id="4f468-149">msdyn_primaryaddresslocationrole</span><span class="sxs-lookup"><span data-stu-id="4f468-149">msdyn_primaryaddresslocationrole</span></span>
<span data-ttu-id="4f468-150">PRIMARYADDRESSLOCATIONSALESTAXGROUPCODE</span><span class="sxs-lookup"><span data-stu-id="4f468-150">PRIMARYADDRESSLOCATIONSALESTAXGROUPCODE</span></span> | >< | <span data-ttu-id="4f468-151">msdyn_primaryaddresslocationsalestaxgroupcode</span><span class="sxs-lookup"><span data-stu-id="4f468-151">msdyn_primaryaddresslocationsalestaxgroupcode</span></span>
<span data-ttu-id="4f468-152">PRIMARYADDRESSLONGITUDE</span><span class="sxs-lookup"><span data-stu-id="4f468-152">PRIMARYADDRESSLONGITUDE</span></span> | >< | <span data-ttu-id="4f468-153">msdyn_primaryaddresslongitude</span><span class="sxs-lookup"><span data-stu-id="4f468-153">msdyn_primaryaddresslongitude</span></span>
<span data-ttu-id="4f468-154">PRIMARYADDRESSSTATEID</span><span class="sxs-lookup"><span data-stu-id="4f468-154">PRIMARYADDRESSSTATEID</span></span> | >< | <span data-ttu-id="4f468-155">msdyn_primaryaddressstateid</span><span class="sxs-lookup"><span data-stu-id="4f468-155">msdyn_primaryaddressstateid</span></span>
<span data-ttu-id="4f468-156">PRIMARYADDRESSSTREET</span><span class="sxs-lookup"><span data-stu-id="4f468-156">PRIMARYADDRESSSTREET</span></span> | >< | <span data-ttu-id="4f468-157">msdyn_primaryaddressstreet</span><span class="sxs-lookup"><span data-stu-id="4f468-157">msdyn_primaryaddressstreet</span></span>
<span data-ttu-id="4f468-158">PRIMARYADDRESSZIPCODE</span><span class="sxs-lookup"><span data-stu-id="4f468-158">PRIMARYADDRESSZIPCODE</span></span> | >< | <span data-ttu-id="4f468-159">msdyn_primaryaddresszipcode</span><span class="sxs-lookup"><span data-stu-id="4f468-159">msdyn_primaryaddresszipcode</span></span>
<span data-ttu-id="4f468-160">PRIMARYADDRESSBUILDINGCOMPLIMENT</span><span class="sxs-lookup"><span data-stu-id="4f468-160">PRIMARYADDRESSBUILDINGCOMPLIMENT</span></span> | >< | <span data-ttu-id="4f468-161">msdyn_primaryaddressbuildingcompliment</span><span class="sxs-lookup"><span data-stu-id="4f468-161">msdyn_primaryaddressbuildingcompliment</span></span>
<span data-ttu-id="4f468-162">PRIMARYADDRESSCITYINKANA</span><span class="sxs-lookup"><span data-stu-id="4f468-162">PRIMARYADDRESSCITYINKANA</span></span> | >< | <span data-ttu-id="4f468-163">msdyn_primaryaddresscityinkana</span><span class="sxs-lookup"><span data-stu-id="4f468-163">msdyn_primaryaddresscityinkana</span></span>
<span data-ttu-id="4f468-164">PRIMARYADDRESSSTREETINKANA</span><span class="sxs-lookup"><span data-stu-id="4f468-164">PRIMARYADDRESSSTREETINKANA</span></span> | >< | <span data-ttu-id="4f468-165">msdyn_primaryaddressstreetinkana</span><span class="sxs-lookup"><span data-stu-id="4f468-165">msdyn_primaryaddressstreetinkana</span></span>
<span data-ttu-id="4f468-166">PRIMARYADDRESSDESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4f468-166">PRIMARYADDRESSDESCRIPTION</span></span> | >< | <span data-ttu-id="4f468-167">msdyn_primaryaddressdescription</span><span class="sxs-lookup"><span data-stu-id="4f468-167">msdyn_primaryaddressdescription</span></span>
<span data-ttu-id="4f468-168">FORMATTEDPRIMARYADDRESS</span><span class="sxs-lookup"><span data-stu-id="4f468-168">FORMATTEDPRIMARYADDRESS</span></span> | >< | <span data-ttu-id="4f468-169">msdyn_formattedprimaryaddress</span><span class="sxs-lookup"><span data-stu-id="4f468-169">msdyn_formattedprimaryaddress</span></span>
<span data-ttu-id="4f468-170">WILLMASTERPLANNEDINTRASITEMOVEMENTSUSETRANSFERJOURNALS</span><span class="sxs-lookup"><span data-stu-id="4f468-170">WILLMASTERPLANNEDINTRASITEMOVEMENTSUSETRANSFERJOURNALS</span></span> | >< | <span data-ttu-id="4f468-171">msdyn_masterplannedusestransferjournal</span><span class="sxs-lookup"><span data-stu-id="4f468-171">msdyn_masterplannedusestransferjournal</span></span>
<span data-ttu-id="4f468-172">PRIMARYADDRESSPOSTBOX</span><span class="sxs-lookup"><span data-stu-id="4f468-172">PRIMARYADDRESSPOSTBOX</span></span> | >< | <span data-ttu-id="4f468-173">msdyn_primaryaddresspostbox</span><span class="sxs-lookup"><span data-stu-id="4f468-173">msdyn_primaryaddresspostbox</span></span>
<span data-ttu-id="4f468-174">PRIMARYADDRESSSTREETNUMBER</span><span class="sxs-lookup"><span data-stu-id="4f468-174">PRIMARYADDRESSSTREETNUMBER</span></span> | >< | <span data-ttu-id="4f468-175">msdyn_primaryaddressstreetnumber</span><span class="sxs-lookup"><span data-stu-id="4f468-175">msdyn_primaryaddressstreetnumber</span></span>


## <a name="warehouses"></a><span data-ttu-id="4f468-176">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="4f468-176">Warehouses</span></span>

<span data-ttu-id="4f468-177">Vöruhúsin eru fáanleg í með eftirfarandi vörpunum.</span><span class="sxs-lookup"><span data-stu-id="4f468-177">The warehouses are available using the following mappings.</span></span>

<span data-ttu-id="4f468-178">Upprunasvæði</span><span class="sxs-lookup"><span data-stu-id="4f468-178">Source field</span></span> | <span data-ttu-id="4f468-179">Gerð vörpunar</span><span class="sxs-lookup"><span data-stu-id="4f468-179">Map type</span></span> | <span data-ttu-id="4f468-180">Áfangasvæði</span><span class="sxs-lookup"><span data-stu-id="4f468-180">Destination field</span></span>
---|---|---
<span data-ttu-id="4f468-181">DEFAULTCONTAINERTYPEID</span><span class="sxs-lookup"><span data-stu-id="4f468-181">DEFAULTCONTAINERTYPEID</span></span> | >> | <span data-ttu-id="4f468-182">msdyn_defaultcontainertypeid</span><span class="sxs-lookup"><span data-stu-id="4f468-182">msdyn_defaultcontainertypeid</span></span>
<span data-ttu-id="4f468-183">AREITEMSCOVERAGEPLANNEDMANUALLY</span><span class="sxs-lookup"><span data-stu-id="4f468-183">AREITEMSCOVERAGEPLANNEDMANUALLY</span></span> | >> | <span data-ttu-id="4f468-184">msdyn_areitemscoverageplannedmanually</span><span class="sxs-lookup"><span data-stu-id="4f468-184">msdyn_areitemscoverageplannedmanually</span></span>
<span data-ttu-id="4f468-185">ARELABORSTANDARDSALLOWED</span><span class="sxs-lookup"><span data-stu-id="4f468-185">ARELABORSTANDARDSALLOWED</span></span> | >> | <span data-ttu-id="4f468-186">msdyn_arelaborstandardsallowed</span><span class="sxs-lookup"><span data-stu-id="4f468-186">msdyn_arelaborstandardsallowed</span></span>
<span data-ttu-id="4f468-187">PRIMARYADDRESSBUILDINGCOMPLIMENT</span><span class="sxs-lookup"><span data-stu-id="4f468-187">PRIMARYADDRESSBUILDINGCOMPLIMENT</span></span> | >> | <span data-ttu-id="4f468-188">msdyn_primaryaddressbuildingcompliment</span><span class="sxs-lookup"><span data-stu-id="4f468-188">msdyn_primaryaddressbuildingcompliment</span></span>
<span data-ttu-id="4f468-189">PRIMARYADDRESSPOSTBOX</span><span class="sxs-lookup"><span data-stu-id="4f468-189">PRIMARYADDRESSPOSTBOX</span></span> | >> | <span data-ttu-id="4f468-190">msdyn_primaryaddresspostbox</span><span class="sxs-lookup"><span data-stu-id="4f468-190">msdyn_primaryaddresspostbox</span></span>
<span data-ttu-id="4f468-191">PRIMARYADDRESSSTREETNUMBER</span><span class="sxs-lookup"><span data-stu-id="4f468-191">PRIMARYADDRESSSTREETNUMBER</span></span> | >> | <span data-ttu-id="4f468-192">msdyn_primaryaddressstreetnumber</span><span class="sxs-lookup"><span data-stu-id="4f468-192">msdyn_primaryaddressstreetnumber</span></span>
<span data-ttu-id="4f468-193">AREWAREHOUSELOCATIONCHECKDIGITSUNIQUE</span><span class="sxs-lookup"><span data-stu-id="4f468-193">AREWAREHOUSELOCATIONCHECKDIGITSUNIQUE</span></span> | >> | <span data-ttu-id="4f468-194">msdyn_arewarehouselocationcheckdigitsunique</span><span class="sxs-lookup"><span data-stu-id="4f468-194">msdyn_arewarehouselocationcheckdigitsunique</span></span>
<span data-ttu-id="4f468-195">INVENTORYCOUNTINGREASONCODEPOLICYNAME</span><span class="sxs-lookup"><span data-stu-id="4f468-195">INVENTORYCOUNTINGREASONCODEPOLICYNAME</span></span> | >> | <span data-ttu-id="4f468-196">msdyn_inventorycountingreasoncodepolicyname</span><span class="sxs-lookup"><span data-stu-id="4f468-196">msdyn_inventorycountingreasoncodepolicyname</span></span>
<span data-ttu-id="4f468-197">AUTOUPDATESHIPMENTRULE</span><span class="sxs-lookup"><span data-stu-id="4f468-197">AUTOUPDATESHIPMENTRULE</span></span> | >> | <span data-ttu-id="4f468-198">msdyn_autoupdateshipmentrule</span><span class="sxs-lookup"><span data-stu-id="4f468-198">msdyn_autoupdateshipmentrule</span></span>
<span data-ttu-id="4f468-199">WAREHOUSERELEASERESERVATIONREQUIREMENTRULE</span><span class="sxs-lookup"><span data-stu-id="4f468-199">WAREHOUSERELEASERESERVATIONREQUIREMENTRULE</span></span> | >> | <span data-ttu-id="4f468-200">msdyn_warehousereleasereservationrequirement</span><span class="sxs-lookup"><span data-stu-id="4f468-200">msdyn_warehousereleasereservationrequirement</span></span>
<span data-ttu-id="4f468-201">EXTERNALLYLOCATEDWAREHOUSEVENDORACCOUNTNUMBER</span><span class="sxs-lookup"><span data-stu-id="4f468-201">EXTERNALLYLOCATEDWAREHOUSEVENDORACCOUNTNUMBER</span></span> | >> | <span data-ttu-id="4f468-202">msdyn_externallylocatedwarehousevendoraccountnu</span><span class="sxs-lookup"><span data-stu-id="4f468-202">msdyn_externallylocatedwarehousevendoraccountnu</span></span>
<span data-ttu-id="4f468-203">INVENTORYSTATUSCHANGERESERVATIONREMOVALLEVEL</span><span class="sxs-lookup"><span data-stu-id="4f468-203">INVENTORYSTATUSCHANGERESERVATIONREMOVALLEVEL</span></span> | >> | <span data-ttu-id="4f468-204">msdyn_inventorystatuschangereservationremoval</span><span class="sxs-lookup"><span data-stu-id="4f468-204">msdyn_inventorystatuschangereservationremoval</span></span>
<span data-ttu-id="4f468-205">WAREHOUSEWORKPROCESSINGPOLICYNAME</span><span class="sxs-lookup"><span data-stu-id="4f468-205">WAREHOUSEWORKPROCESSINGPOLICYNAME</span></span> | >> | <span data-ttu-id="4f468-206">msdyn_warehouseworkprocessingpolicyname</span><span class="sxs-lookup"><span data-stu-id="4f468-206">msdyn_warehouseworkprocessingpolicyname</span></span>
<span data-ttu-id="4f468-207">ISFALLBACKWAREHOUSE</span><span class="sxs-lookup"><span data-stu-id="4f468-207">ISFALLBACKWAREHOUSE</span></span> | >> | <span data-ttu-id="4f468-208">msdyn_isfallbackwarehouse</span><span class="sxs-lookup"><span data-stu-id="4f468-208">msdyn_isfallbackwarehouse</span></span>
<span data-ttu-id="4f468-209">ISFINANCIALNEGATIVERETAILSTOREINVENTORYALLOWED</span><span class="sxs-lookup"><span data-stu-id="4f468-209">ISFINANCIALNEGATIVERETAILSTOREINVENTORYALLOWED</span></span> | >> | <span data-ttu-id="4f468-210">msdyn_financialnegativestoreinventoryallowed</span><span class="sxs-lookup"><span data-stu-id="4f468-210">msdyn_financialnegativestoreinventoryallowed</span></span>
<span data-ttu-id="4f468-211">ISPALLETMOVEMENTDURINGCYCLECOUNTINGALLOWED</span><span class="sxs-lookup"><span data-stu-id="4f468-211">ISPALLETMOVEMENTDURINGCYCLECOUNTINGALLOWED</span></span> | >> | <span data-ttu-id="4f468-212">msdyn_palletmovementduringcyclecountingallowed</span><span class="sxs-lookup"><span data-stu-id="4f468-212">msdyn_palletmovementduringcyclecountingallowed</span></span>
<span data-ttu-id="4f468-213">ISPHYSICALNEGATIVERETAILSTOREINVENTORYALLOWED</span><span class="sxs-lookup"><span data-stu-id="4f468-213">ISPHYSICALNEGATIVERETAILSTOREINVENTORYALLOWED</span></span> | >> | <span data-ttu-id="4f468-214">msdyn_physicalnegativestoreinventoryallowed</span><span class="sxs-lookup"><span data-stu-id="4f468-214">msdyn_physicalnegativestoreinventoryallowed</span></span>
<span data-ttu-id="4f468-215">ISREFILLEDFROMMAINWAREHOUSE</span><span class="sxs-lookup"><span data-stu-id="4f468-215">ISREFILLEDFROMMAINWAREHOUSE</span></span> | >> | <span data-ttu-id="4f468-216">msdyn_isrefilledfrommainwarehouse</span><span class="sxs-lookup"><span data-stu-id="4f468-216">msdyn_isrefilledfrommainwarehouse</span></span>
<span data-ttu-id="4f468-217">ISRETAILSTOREWAREHOUSE</span><span class="sxs-lookup"><span data-stu-id="4f468-217">ISRETAILSTOREWAREHOUSE</span></span> | >> | <span data-ttu-id="4f468-218">msdyn_isretailstorewarehouse</span><span class="sxs-lookup"><span data-stu-id="4f468-218">msdyn_isretailstorewarehouse</span></span>
<span data-ttu-id="4f468-219">MAINREFILLINGWAREHOUSEID</span><span class="sxs-lookup"><span data-stu-id="4f468-219">MAINREFILLINGWAREHOUSEID</span></span> | >> | <span data-ttu-id="4f468-220">msdyn_mainrefillingwarehouseid.msdyn_warehouseid</span><span class="sxs-lookup"><span data-stu-id="4f468-220">msdyn_mainrefillingwarehouseid.msdyn_warehouseid</span></span>
<span data-ttu-id="4f468-221">MASTERPLANNINGWORKCALENDARDID</span><span class="sxs-lookup"><span data-stu-id="4f468-221">MASTERPLANNINGWORKCALENDARDID</span></span> | >> | <span data-ttu-id="4f468-222">msdyn_masterplanningworkcalendarid</span><span class="sxs-lookup"><span data-stu-id="4f468-222">msdyn_masterplanningworkcalendarid</span></span>
<span data-ttu-id="4f468-223">MAXIMUMBATCHPICKINGLISTQUANTITY</span><span class="sxs-lookup"><span data-stu-id="4f468-223">MAXIMUMBATCHPICKINGLISTQUANTITY</span></span> | >> | <span data-ttu-id="4f468-224">msdyn_maximumbatchpickinglistquantity</span><span class="sxs-lookup"><span data-stu-id="4f468-224">msdyn_maximumbatchpickinglistquantity</span></span>
<span data-ttu-id="4f468-225">MAXIMUMPICKINGLISTLINEQUANTITY</span><span class="sxs-lookup"><span data-stu-id="4f468-225">MAXIMUMPICKINGLISTLINEQUANTITY</span></span> | >> | <span data-ttu-id="4f468-226">msdyn_maximumpickinglistlinequantity</span><span class="sxs-lookup"><span data-stu-id="4f468-226">msdyn_maximumpickinglistlinequantity</span></span>
<span data-ttu-id="4f468-227">OPERATIONALSITEID</span><span class="sxs-lookup"><span data-stu-id="4f468-227">OPERATIONALSITEID</span></span> | >> | <span data-ttu-id="4f468-228">msdyn_operationalsiteid.msdyn_siteid</span><span class="sxs-lookup"><span data-stu-id="4f468-228">msdyn_operationalsiteid.msdyn_siteid</span></span>
<span data-ttu-id="4f468-229">QUARANTINEWAREHOUSEID</span><span class="sxs-lookup"><span data-stu-id="4f468-229">QUARANTINEWAREHOUSEID</span></span> | >> | <span data-ttu-id="4f468-230">msdyn_quarantinewarehouseid.msdyn_warehouseid</span><span class="sxs-lookup"><span data-stu-id="4f468-230">msdyn_quarantinewarehouseid.msdyn_warehouseid</span></span>
<span data-ttu-id="4f468-231">RETAILSTOREQUANTITYALLOCATIONREPLENISMENTRULEWEIGHT</span><span class="sxs-lookup"><span data-stu-id="4f468-231">RETAILSTOREQUANTITYALLOCATIONREPLENISMENTRULEWEIGHT</span></span> | > | <span data-ttu-id="4f468-232">msdyn_storeqtyallocationreplenishmentweight</span><span class="sxs-lookup"><span data-stu-id="4f468-232">msdyn_storeqtyallocationreplenishmentweight</span></span>
<span data-ttu-id="4f468-233">SHOULDWAREHOUSELOCATIONIDINCLUDEAISLEID</span><span class="sxs-lookup"><span data-stu-id="4f468-233">SHOULDWAREHOUSELOCATIONIDINCLUDEAISLEID</span></span> | >> | <span data-ttu-id="4f468-234">msdyn_shouldwarehouselocationincludeaisleid</span><span class="sxs-lookup"><span data-stu-id="4f468-234">msdyn_shouldwarehouselocationincludeaisleid</span></span>
<span data-ttu-id="4f468-235">TRANSITWAREHOUSEID</span><span class="sxs-lookup"><span data-stu-id="4f468-235">TRANSITWAREHOUSEID</span></span> | >> | <span data-ttu-id="4f468-236">msdyn_transitwarehouseid.msdyn_warehouseid</span><span class="sxs-lookup"><span data-stu-id="4f468-236">msdyn_transitwarehouseid.msdyn_warehouseid</span></span>
<span data-ttu-id="4f468-237">WAREHOUSEID</span><span class="sxs-lookup"><span data-stu-id="4f468-237">WAREHOUSEID</span></span> | >> | <span data-ttu-id="4f468-238">msdyn_warehouseid</span><span class="sxs-lookup"><span data-stu-id="4f468-238">msdyn_warehouseid</span></span>
<span data-ttu-id="4f468-239">WAREHOUSELOCATIONIDBINIDFORMAT</span><span class="sxs-lookup"><span data-stu-id="4f468-239">WAREHOUSELOCATIONIDBINIDFORMAT</span></span> | >> | <span data-ttu-id="4f468-240">msdyn_warehouselocationidbinidformat</span><span class="sxs-lookup"><span data-stu-id="4f468-240">msdyn_warehouselocationidbinidformat</span></span>
<span data-ttu-id="4f468-241">WAREHOUSELOCATIONIDRACKIDFORMAT</span><span class="sxs-lookup"><span data-stu-id="4f468-241">WAREHOUSELOCATIONIDRACKIDFORMAT</span></span> | >> | <span data-ttu-id="4f468-242">msdyn_warehouselocationidrackidformat</span><span class="sxs-lookup"><span data-stu-id="4f468-242">msdyn_warehouselocationidrackidformat</span></span>
<span data-ttu-id="4f468-243">WAREHOUSELOCATIONIDSHELFIDFORMAT</span><span class="sxs-lookup"><span data-stu-id="4f468-243">WAREHOUSELOCATIONIDSHELFIDFORMAT</span></span> | >> | <span data-ttu-id="4f468-244">msdyn_warehouselocationidshelfidformat</span><span class="sxs-lookup"><span data-stu-id="4f468-244">msdyn_warehouselocationidshelfidformat</span></span>
<span data-ttu-id="4f468-245">WAREHOUSENAME</span><span class="sxs-lookup"><span data-stu-id="4f468-245">WAREHOUSENAME</span></span> | >> | <span data-ttu-id="4f468-246">msdyn_name</span><span class="sxs-lookup"><span data-stu-id="4f468-246">msdyn_name</span></span>
<span data-ttu-id="4f468-247">WAREHOUSENAME</span><span class="sxs-lookup"><span data-stu-id="4f468-247">WAREHOUSENAME</span></span> | >> | <span data-ttu-id="4f468-248">msdyn_warehousename</span><span class="sxs-lookup"><span data-stu-id="4f468-248">msdyn_warehousename</span></span>
<span data-ttu-id="4f468-249">WAREHOUSESPECIFICDEFAULTINVENTORYSTATUSID</span><span class="sxs-lookup"><span data-stu-id="4f468-249">WAREHOUSESPECIFICDEFAULTINVENTORYSTATUSID</span></span> | >> | <span data-ttu-id="4f468-250">msdyn_warehousespecificdefaultinventorystatusid</span><span class="sxs-lookup"><span data-stu-id="4f468-250">msdyn_warehousespecificdefaultinventorystatusid</span></span>
<span data-ttu-id="4f468-251">WAREHOUSETYPE</span><span class="sxs-lookup"><span data-stu-id="4f468-251">WAREHOUSETYPE</span></span> | >> | <span data-ttu-id="4f468-252">msdyn_warehousetype</span><span class="sxs-lookup"><span data-stu-id="4f468-252">msdyn_warehousetype</span></span>
<span data-ttu-id="4f468-253">ISPRIMARYADDRESSASSIGNED</span><span class="sxs-lookup"><span data-stu-id="4f468-253">ISPRIMARYADDRESSASSIGNED</span></span> | >> | <span data-ttu-id="4f468-254">msdyn_isprimaryaddressassigned</span><span class="sxs-lookup"><span data-stu-id="4f468-254">msdyn_isprimaryaddressassigned</span></span>
<span data-ttu-id="4f468-255">PRIMARYADDRESSCITY</span><span class="sxs-lookup"><span data-stu-id="4f468-255">PRIMARYADDRESSCITY</span></span> | >> | <span data-ttu-id="4f468-256">msdyn_primaryaddresscity</span><span class="sxs-lookup"><span data-stu-id="4f468-256">msdyn_primaryaddresscity</span></span>
<span data-ttu-id="4f468-257">PRIMARYADDRESSCOUNTRYREGIONID</span><span class="sxs-lookup"><span data-stu-id="4f468-257">PRIMARYADDRESSCOUNTRYREGIONID</span></span> | >> | <span data-ttu-id="4f468-258">msdyn_primaryaddresscountryregionid</span><span class="sxs-lookup"><span data-stu-id="4f468-258">msdyn_primaryaddresscountryregionid</span></span>
<span data-ttu-id="4f468-259">PRIMARYADDRESSCOUNTYID</span><span class="sxs-lookup"><span data-stu-id="4f468-259">PRIMARYADDRESSCOUNTYID</span></span> | >> | <span data-ttu-id="4f468-260">msdyn_primaryaddresscountyid</span><span class="sxs-lookup"><span data-stu-id="4f468-260">msdyn_primaryaddresscountyid</span></span>
<span data-ttu-id="4f468-261">PRIMARYADDRESSDISTRICTNAME</span><span class="sxs-lookup"><span data-stu-id="4f468-261">PRIMARYADDRESSDISTRICTNAME</span></span> | >> | <span data-ttu-id="4f468-262">msdyn_primaryaddressdistrictname</span><span class="sxs-lookup"><span data-stu-id="4f468-262">msdyn_primaryaddressdistrictname</span></span>
<span data-ttu-id="4f468-263">PRIMARYADDRESSLATITUDE</span><span class="sxs-lookup"><span data-stu-id="4f468-263">PRIMARYADDRESSLATITUDE</span></span> | >> | <span data-ttu-id="4f468-264">msdyn_primaryaddresslatitude</span><span class="sxs-lookup"><span data-stu-id="4f468-264">msdyn_primaryaddresslatitude</span></span>
<span data-ttu-id="4f468-265">PRIMARYADDRESSLONGITUDE</span><span class="sxs-lookup"><span data-stu-id="4f468-265">PRIMARYADDRESSLONGITUDE</span></span> | >> | <span data-ttu-id="4f468-266">msdyn_primaryaddresslongitude</span><span class="sxs-lookup"><span data-stu-id="4f468-266">msdyn_primaryaddresslongitude</span></span>
<span data-ttu-id="4f468-267">PRIMARYADDRESSLOCATIONROLES</span><span class="sxs-lookup"><span data-stu-id="4f468-267">PRIMARYADDRESSLOCATIONROLES</span></span> | >> | <span data-ttu-id="4f468-268">msdyn_primaryaddresslocationroles</span><span class="sxs-lookup"><span data-stu-id="4f468-268">msdyn_primaryaddresslocationroles</span></span>
<span data-ttu-id="4f468-269">PRIMARYADDRESSLOCATIONSALESTAXGROUPCODE</span><span class="sxs-lookup"><span data-stu-id="4f468-269">PRIMARYADDRESSLOCATIONSALESTAXGROUPCODE</span></span> | >> | <span data-ttu-id="4f468-270">msdyn_primaryaddresslocationsalestaxgroupcode</span><span class="sxs-lookup"><span data-stu-id="4f468-270">msdyn_primaryaddresslocationsalestaxgroupcode</span></span>
<span data-ttu-id="4f468-271">PRIMARYADDRESSSTATEID</span><span class="sxs-lookup"><span data-stu-id="4f468-271">PRIMARYADDRESSSTATEID</span></span> | >> | <span data-ttu-id="4f468-272">msdyn_primaryaddressstateid</span><span class="sxs-lookup"><span data-stu-id="4f468-272">msdyn_primaryaddressstateid</span></span>
<span data-ttu-id="4f468-273">PRIMARYADDRESSSTREET</span><span class="sxs-lookup"><span data-stu-id="4f468-273">PRIMARYADDRESSSTREET</span></span> | >> | <span data-ttu-id="4f468-274">msdyn_primaryaddressstreet</span><span class="sxs-lookup"><span data-stu-id="4f468-274">msdyn_primaryaddressstreet</span></span>
<span data-ttu-id="4f468-275">PRIMARYADDRESSZIPCODE</span><span class="sxs-lookup"><span data-stu-id="4f468-275">PRIMARYADDRESSZIPCODE</span></span> | >> | <span data-ttu-id="4f468-276">msdyn_primaryaddresszipcode</span><span class="sxs-lookup"><span data-stu-id="4f468-276">msdyn_primaryaddresszipcode</span></span>
<span data-ttu-id="4f468-277">EXTERNALLYLOCATEDWAREHOUSECUSTOMERACCOUNTNUMBER</span><span class="sxs-lookup"><span data-stu-id="4f468-277">EXTERNALLYLOCATEDWAREHOUSECUSTOMERACCOUNTNUMBER</span></span> | >> | <span data-ttu-id="4f468-278">msdyn_externallylocatedwarehousecustomeraccount</span><span class="sxs-lookup"><span data-stu-id="4f468-278">msdyn_externallylocatedwarehousecustomeraccount</span></span>
<span data-ttu-id="4f468-279">PRIMARYADDRESSCITYINKANA</span><span class="sxs-lookup"><span data-stu-id="4f468-279">PRIMARYADDRESSCITYINKANA</span></span> | >> | <span data-ttu-id="4f468-280">msdyn_primaryaddresscityinkana</span><span class="sxs-lookup"><span data-stu-id="4f468-280">msdyn_primaryaddresscityinkana</span></span>
<span data-ttu-id="4f468-281">PRIMARYADDRESSSTREETINKANA</span><span class="sxs-lookup"><span data-stu-id="4f468-281">PRIMARYADDRESSSTREETINKANA</span></span> | >> | <span data-ttu-id="4f468-282">msdyn_primaryaddressstreetinkana</span><span class="sxs-lookup"><span data-stu-id="4f468-282">msdyn_primaryaddressstreetinkana</span></span>
<span data-ttu-id="4f468-283">PRIMARYADDRESSDESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4f468-283">PRIMARYADDRESSDESCRIPTION</span></span> | >> | <span data-ttu-id="4f468-284">msdyn_primaryaddressdescription</span><span class="sxs-lookup"><span data-stu-id="4f468-284">msdyn_primaryaddressdescription</span></span>
<span data-ttu-id="4f468-285">AREADVANCEDWAREHOUSEMANAGEMENTPROCESSESENABLED</span><span class="sxs-lookup"><span data-stu-id="4f468-285">AREADVANCEDWAREHOUSEMANAGEMENTPROCESSESENABLED</span></span> | >> | <span data-ttu-id="4f468-286">msdyn_uesadvancedwarehousemanagementprocesses</span><span class="sxs-lookup"><span data-stu-id="4f468-286">msdyn_uesadvancedwarehousemanagementprocesses</span></span>
<span data-ttu-id="4f468-287">AREPICKINGLISTSDELIVERYMODESPECIFIC</span><span class="sxs-lookup"><span data-stu-id="4f468-287">AREPICKINGLISTSDELIVERYMODESPECIFIC</span></span> | >> | <span data-ttu-id="4f468-288">msdyn_arepickinglistsdeliverymodespecific</span><span class="sxs-lookup"><span data-stu-id="4f468-288">msdyn_arepickinglistsdeliverymodespecific</span></span>
<span data-ttu-id="4f468-289">AREPICKINGLISTSSHIPMENTSPECIFICONLY</span><span class="sxs-lookup"><span data-stu-id="4f468-289">AREPICKINGLISTSSHIPMENTSPECIFICONLY</span></span> | >> | <span data-ttu-id="4f468-290">msdyn_arepickinglistshipmentspecificonly</span><span class="sxs-lookup"><span data-stu-id="4f468-290">msdyn_arepickinglistshipmentspecificonly</span></span>
<span data-ttu-id="4f468-291">FORMATTEDPRIMARYADDRESS</span><span class="sxs-lookup"><span data-stu-id="4f468-291">FORMATTEDPRIMARYADDRESS</span></span> | >> | <span data-ttu-id="4f468-292">msdyn_formattedprimaryaddress</span><span class="sxs-lookup"><span data-stu-id="4f468-292">msdyn_formattedprimaryaddress</span></span>
<span data-ttu-id="4f468-293">ISBILLOFLADINGPRINTINGBEFORESHIPMENTCONFIRMATIONENABLED</span><span class="sxs-lookup"><span data-stu-id="4f468-293">ISBILLOFLADINGPRINTINGBEFORESHIPMENTCONFIRMATIONENABLED</span></span> | >> | <span data-ttu-id="4f468-294">msdyn_printbillofladingbeforeshipconfirmation</span><span class="sxs-lookup"><span data-stu-id="4f468-294">msdyn_printbillofladingbeforeshipconfirmation</span></span>
<span data-ttu-id="4f468-295">RAWMATERIALPICKINGINVENTORYISSUESTATUS</span><span class="sxs-lookup"><span data-stu-id="4f468-295">RAWMATERIALPICKINGINVENTORYISSUESTATUS</span></span> | >> | <span data-ttu-id="4f468-296">msdyn_rawmaterialpickinginventoryissuestatus</span><span class="sxs-lookup"><span data-stu-id="4f468-296">msdyn_rawmaterialpickinginventoryissuestatus</span></span>
<span data-ttu-id="4f468-297">WILLAUTOMATICLOADRELEASERESERVEINVENTORY</span><span class="sxs-lookup"><span data-stu-id="4f468-297">WILLAUTOMATICLOADRELEASERESERVEINVENTORY</span></span> | >> | <span data-ttu-id="4f468-298">msdyn_willautomaticloadreleaseinventory</span><span class="sxs-lookup"><span data-stu-id="4f468-298">msdyn_willautomaticloadreleaseinventory</span></span>
<span data-ttu-id="4f468-299">WILLINVENTORYSTATUSCHANGEREMOVEBLOCKING</span><span class="sxs-lookup"><span data-stu-id="4f468-299">WILLINVENTORYSTATUSCHANGEREMOVEBLOCKING</span></span> | >> | <span data-ttu-id="4f468-300">msdyn_willinventorystatuschangeremoveblocking</span><span class="sxs-lookup"><span data-stu-id="4f468-300">msdyn_willinventorystatuschangeremoveblocking</span></span>
<span data-ttu-id="4f468-301">WILLMANUALLOADRELEASERESERVEINVENTORY</span><span class="sxs-lookup"><span data-stu-id="4f468-301">WILLMANUALLOADRELEASERESERVEINVENTORY</span></span> | >> | <span data-ttu-id="4f468-302">msdyn_willmanualloadreleasereserveinventory</span><span class="sxs-lookup"><span data-stu-id="4f468-302">msdyn_willmanualloadreleasereserveinventory</span></span>
<span data-ttu-id="4f468-303">WILLORDERRELEASINGCONSOLIDATESHIPMENTS</span><span class="sxs-lookup"><span data-stu-id="4f468-303">WILLORDERRELEASINGCONSOLIDATESHIPMENTS</span></span> | >> | <span data-ttu-id="4f468-304">msdyn_willorderreleasingconsolidateshipments</span><span class="sxs-lookup"><span data-stu-id="4f468-304">msdyn_willorderreleasingconsolidateshipments</span></span>
<span data-ttu-id="4f468-305">WILLPRODUCTIONBOMSRESERVEWAREHOUSELEVELONLY</span><span class="sxs-lookup"><span data-stu-id="4f468-305">WILLPRODUCTIONBOMSRESERVEWAREHOUSELEVELONLY</span></span> | >> | <span data-ttu-id="4f468-306">msdyn_productionbomsreservewarehouselevel</span><span class="sxs-lookup"><span data-stu-id="4f468-306">msdyn_productionbomsreservewarehouselevel</span></span>
<span data-ttu-id="4f468-307">WILLSHIPPINGCANCELLATIONDECREMENTLOADQUANITY</span><span class="sxs-lookup"><span data-stu-id="4f468-307">WILLSHIPPINGCANCELLATIONDECREMENTLOADQUANITY</span></span> | >> | <span data-ttu-id="4f468-308">msdyn_shippingcanceldecrementloadquantity</span><span class="sxs-lookup"><span data-stu-id="4f468-308">msdyn_shippingcanceldecrementloadquantity</span></span>
<span data-ttu-id="4f468-309">WILLWAREHOUSELOCATIONIDINCLUDEBINIDBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="4f468-309">WILLWAREHOUSELOCATIONIDINCLUDEBINIDBYDEFAULT</span></span> | >> | <span data-ttu-id="4f468-310">msdyn_warehouselocationidincludeblindid</span><span class="sxs-lookup"><span data-stu-id="4f468-310">msdyn_warehouselocationidincludeblindid</span></span>
<span data-ttu-id="4f468-311">WILLWAREHOUSELOCATIONIDINCLUDERACKIDBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="4f468-311">WILLWAREHOUSELOCATIONIDINCLUDERACKIDBYDEFAULT</span></span> | >> | <span data-ttu-id="4f468-312">msdyn_warehouselocationincluderackidbydefault</span><span class="sxs-lookup"><span data-stu-id="4f468-312">msdyn_warehouselocationincluderackidbydefault</span></span>
<span data-ttu-id="4f468-313">WILLWAREHOUSELOCATIONIDINCLUDESHELFIDBYDEFAULT</span><span class="sxs-lookup"><span data-stu-id="4f468-313">WILLWAREHOUSELOCATIONIDINCLUDESHELFIDBYDEFAULT</span></span> | >> | <span data-ttu-id="4f468-314">msdyn_warehouselocationidincludeshelfid</span><span class="sxs-lookup"><span data-stu-id="4f468-314">msdyn_warehouselocationidincludeshelfid</span></span>