--- 
title: "Skilgreina staðsetningar í vöruhúsi með vöruhúsakerfi"
description: "Þessi handbók sýnir hvernig á að grunnstilla uppsetningu á staðsetningu fyrir nýtt vöruhúsakerfisvirkjað vöruhús (vöruhús sem notar ítarleg vöruhúsaferli)."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: fb48914491597f2eb7cc08db99ed548764213709
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="configure-locations-in-a-wms-enabled-warehouse"></a><span data-ttu-id="f1178-103">Skilgreina staðsetningar í vöruhúsi með vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="f1178-103">Configure locations in a WMS-enabled warehouse</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1178-104">Þessi handbók sýnir hvernig á að grunnstilla uppsetningu á staðsetningu fyrir nýtt vöruhúsakerfisvirkjað vöruhús (vöruhús sem notar ítarleg vöruhúsaferli).</span><span class="sxs-lookup"><span data-stu-id="f1178-104">This guide shows you how to configure the location setup for a new WMS-enabled warehouse (a warehouse that uses advanced warehouse management processes).</span></span> <span data-ttu-id="f1178-105">Ferlið er yfirleitt gert af stjórnanda vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="f1178-105">The process is typically done by a warehouse manager.</span></span> <span data-ttu-id="f1178-106">Hægt er að keyra þessa handbók í sýnifyrirtækinu USMF eða í eigin gögnum.</span><span class="sxs-lookup"><span data-stu-id="f1178-106">You can run this guide in demo data company USMF or on your own data.</span></span> <span data-ttu-id="f1178-107">Forkröfur eru að minnsta kosti eitt svæði sé grunnstillt.</span><span class="sxs-lookup"><span data-stu-id="f1178-107">A precondition is that you have at least one site configured.</span></span>


## <a name="create-a-new-warehouse"></a><span data-ttu-id="f1178-108">Stofna nýtt vöruhús</span><span class="sxs-lookup"><span data-stu-id="f1178-108">Create a new warehouse</span></span>
1. <span data-ttu-id="f1178-109">Fara í Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="f1178-109">Go to Warehouses.</span></span>
2. <span data-ttu-id="f1178-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f1178-110">Click New.</span></span>
3. <span data-ttu-id="f1178-111">Í reitinn vöruhús skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-111">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="f1178-112">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f1178-113">Í reitinn Svæði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-113">In the Site field, type a value.</span></span>
6. <span data-ttu-id="f1178-114">Stækka eða fella saman hlutann Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="f1178-114">Expand or collapse the Warehouse section.</span></span>
7. <span data-ttu-id="f1178-115">Stilltu valkostinn Nota ferli vöruhúsastjórnunar á Já.</span><span class="sxs-lookup"><span data-stu-id="f1178-115">Set the Use warehouse management processes option to Yes.</span></span>
    * <span data-ttu-id="f1178-116">Þessi stilling leyfir þér að keyra ítarleg vöruhúsaferli með því að nota vöruhúsavinnu og fartæki.</span><span class="sxs-lookup"><span data-stu-id="f1178-116">This setting allows you to  run advanced warehousing processes using warehouse work and mobile devices.</span></span>  
8. <span data-ttu-id="f1178-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f1178-117">Close the page.</span></span>

## <a name="define-a-location-format"></a><span data-ttu-id="f1178-118">Skilgreina snið staðsetningar</span><span class="sxs-lookup"><span data-stu-id="f1178-118">Define a location format</span></span>
1. <span data-ttu-id="f1178-119">Fara á staðsetningarsnið.</span><span class="sxs-lookup"><span data-stu-id="f1178-119">Go to Location formats.</span></span>
    * <span data-ttu-id="f1178-120">Staðsetningarsnið eru nafngiftarkerfi sem eru notuð til að stofna einkvæm og samræmd heiti fyrir aðrar staðsetningu karfa stöður notað innan vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="f1178-120">Location formats are a naming-system used to create unique and consistent names for the different location bin positions used within a warehouse.</span></span> <span data-ttu-id="f1178-121">Það getur verið gagnlegt að nota skiltákn sem hluta af staðsetningarsniði til að auðvelda auðkenningu íhluta staðsetningar eins og númer gangs.</span><span class="sxs-lookup"><span data-stu-id="f1178-121">It can be useful to use separators as part of the location format to make it easier to identify components of the location such as the aisle number.</span></span> <span data-ttu-id="f1178-122">Í þessu dæmi stofnum við heiti með fjórum íhlutum.</span><span class="sxs-lookup"><span data-stu-id="f1178-122">In this example, we’ll create a name with four components.</span></span> <span data-ttu-id="f1178-123">Til dæmis, þetta gæti verið gangur, rekki, hilla og karfa.</span><span class="sxs-lookup"><span data-stu-id="f1178-123">For example, these could be aisle, rack, shelf, and bin.</span></span>  
2. <span data-ttu-id="f1178-124">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f1178-124">Click New.</span></span>
3. <span data-ttu-id="f1178-125">Í reitinn staðsetningarsnið skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-125">In the Location format field, type a value.</span></span>
4. <span data-ttu-id="f1178-126">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-126">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f1178-127">Í reitinn Lýsing hluta skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-127">In the Segment description field, type a value.</span></span>
    * <span data-ttu-id="f1178-128">Það lýsir því fyrir hvað fyrsti íhluti heitis staðsetningar stendur.</span><span class="sxs-lookup"><span data-stu-id="f1178-128">This describes what the first component of the location name represents.</span></span> <span data-ttu-id="f1178-129">Til dæmis, gæti það verið Gangur.</span><span class="sxs-lookup"><span data-stu-id="f1178-129">For example, it could be Aisle.</span></span>  
6. <span data-ttu-id="f1178-130">Í reitinn Lengd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f1178-130">In the Length field, enter a number.</span></span>
    * <span data-ttu-id="f1178-131">Þetta ákvarðar hversu margir stafir verða að vera í þessum hluta af nafni staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="f1178-131">This determines how many characters this part of the location name must have.</span></span> <span data-ttu-id="f1178-132">Athugið að samtala allra íhluta í heiti, þar á meðal skiltákn, má ekki fara yfir 10 staftákn.</span><span class="sxs-lookup"><span data-stu-id="f1178-132">Note that the total of all components in the name, including the separators, cannot exceed 10 characters.</span></span>  
7. <span data-ttu-id="f1178-133">Í reitinn Skiltákn skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-133">In the Separator field, type a value.</span></span>
    * <span data-ttu-id="f1178-134">Þetta ákveður hvaða stafur eða tákn er notað á milli fyrsta og annars íhluta í heiti.</span><span class="sxs-lookup"><span data-stu-id="f1178-134">This determines which character or symbol is used between the first and second component of the name.</span></span>  
8. <span data-ttu-id="f1178-135">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f1178-135">Click New.</span></span>
9. <span data-ttu-id="f1178-136">Í reitinn Lýsing hluta skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-136">In the Segment description field, type a value.</span></span>
10. <span data-ttu-id="f1178-137">Í reitinn Lengd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f1178-137">In the Length field, enter a number.</span></span>
11. <span data-ttu-id="f1178-138">Í reitinn Skiltákn skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-138">In the Separator field, type a value.</span></span>
12. <span data-ttu-id="f1178-139">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="f1178-139">Click New.</span></span>
13. <span data-ttu-id="f1178-140">Í reitinn Lýsing hluta skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-140">In the Segment description field, type a value.</span></span>
14. <span data-ttu-id="f1178-141">Í reitinn Lengd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f1178-141">In the Length field, enter a number.</span></span>
15. <span data-ttu-id="f1178-142">Í reitinn Skiltákn skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-142">In the Separator field, type a value.</span></span>
16. <span data-ttu-id="f1178-143">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="f1178-143">Click New.</span></span>
17. <span data-ttu-id="f1178-144">Í reitinn Lýsing hluta skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-144">In the Segment description field, type a value.</span></span>
18. <span data-ttu-id="f1178-145">Í reitinn Lengd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f1178-145">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="f1178-146">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f1178-146">Click Save.</span></span>
20. <span data-ttu-id="f1178-147">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f1178-147">Close the page.</span></span>

## <a name="define-location-types"></a><span data-ttu-id="f1178-148">Skilgreina staðsetningagerðir</span><span class="sxs-lookup"><span data-stu-id="f1178-148">Define location types</span></span>
1. <span data-ttu-id="f1178-149">Fara í Gerðir staðsetninga.</span><span class="sxs-lookup"><span data-stu-id="f1178-149">Go to Location types.</span></span>
    * <span data-ttu-id="f1178-150">Hægt er að nota gerðir staðsetninga sem síunarvalkosti til að stýra mismunandi vöruhúsakerfisferlum.</span><span class="sxs-lookup"><span data-stu-id="f1178-150">Location types can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="f1178-151">Sem lágmark þarf að stofna staðsetningagerðir sviðsetninga og endanlegra sendinga til að skilgreina stjórnunarferli á útleið í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="f1178-151">As a minimum, you need to create staging and final shipping location types in order to define the outbound warehouse management process.</span></span>  
2. <span data-ttu-id="f1178-152">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f1178-152">Click New.</span></span>
3. <span data-ttu-id="f1178-153">Í reitinn Gerð staðsetningar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-153">In the Location type field, type a value.</span></span>
4. <span data-ttu-id="f1178-154">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="f1178-154">In the Description field, type a value.</span></span>
5. <span data-ttu-id="f1178-155">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f1178-155">Close the page.</span></span>

## <a name="define-location-profile"></a><span data-ttu-id="f1178-156">Skilgreina forstillingu staðsetningar</span><span class="sxs-lookup"><span data-stu-id="f1178-156">Define location profile</span></span>
1. <span data-ttu-id="f1178-157">Fara í Forstillingar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="f1178-157">Go to Location profiles.</span></span>
    * <span data-ttu-id="f1178-158">Skilgreining á forstillingum staðsetningar er mjög mikilvæg.</span><span class="sxs-lookup"><span data-stu-id="f1178-158">The definition of location profiles is very important.</span></span> <span data-ttu-id="f1178-159">Hægt er að stýra afkastagetu flokkaðra staðsetninga hér, ásamt reglum sem tengjast hvaða birgðir eru vistaðar og hvernig þær eru vistaðar.</span><span class="sxs-lookup"><span data-stu-id="f1178-159">Grouped locations capacity can be controlled here, as well as the policies related to what inventory gets stored, and how it is stored.</span></span> <span data-ttu-id="f1178-160">Hægt er að nota forstillingar staðsetninga sem síunarvalkosti til að stýra mismunandi vöruhúsakerfisferlum.</span><span class="sxs-lookup"><span data-stu-id="f1178-160">Location profiles can be used as filtering options to control the different warehouse management processes.</span></span> <span data-ttu-id="f1178-161">Sem lágmark verður að stofna forstillingu fyrir staðsetningu notanda til að virkja ferli vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="f1178-161">As a minimum, you must create a user location profile in order to enable the warehouse management processes.</span></span>  
2. <span data-ttu-id="f1178-162">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f1178-162">Click New.</span></span>
3. <span data-ttu-id="f1178-163">Færa inn gildi í reitnum Kenni forstillingar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="f1178-163">In the Location profile ID field, type a value.</span></span>
4. <span data-ttu-id="f1178-164">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-164">In the Name field, type a value.</span></span>
5. <span data-ttu-id="f1178-165">Í reitnum Staðsetningarsnið skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f1178-165">In the Location format field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f1178-166">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f1178-166">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f1178-167">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f1178-167">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f1178-168">Í reitnum Gerð staðsetningar skal smella a fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f1178-168">In the Location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="f1178-169">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f1178-169">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="f1178-170">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f1178-170">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="f1178-171">Merkja eða afmerkja gátreitinn Heimila blandaða birgðastöðu.</span><span class="sxs-lookup"><span data-stu-id="f1178-171">Select or clear the Allow mixed  inventory statuses check box.</span></span>
    * <span data-ttu-id="f1178-172">Virkja þennan valkost ef óskað er að heimila stöðugildi blandaðra birgða í staðsetningum sem eru flokkaðar eftir þessa forstillingu staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="f1178-172">Enable this option if you want to allow mixed inventory status values in the locations that are going to be grouped by this location profile.</span></span>  
12. <span data-ttu-id="f1178-173">Merkja eða afmerkja gátreitinn Hnekkja reglum fyrir runudaga.</span><span class="sxs-lookup"><span data-stu-id="f1178-173">Select or clear the Override rules for batch days check box.</span></span>
    * <span data-ttu-id="f1178-174">Virkja þennan valkost til að hnekkja reglu fyrir hversu marga daga lokadaga birgðir runuvinnslu getur verið önnur, til að leyfa blöndun birgðaruna sem hlýðir þessari reglu ekki.</span><span class="sxs-lookup"><span data-stu-id="f1178-174">Enable this option to override the rule for how many days the inventory batch expiration dates can differ, to allow mixing of inventory batches that don’t obeying this rule.</span></span>  
13. <span data-ttu-id="f1178-175">Merkja eða afmerkja gátreitinn Leyfa reglulega talningu.</span><span class="sxs-lookup"><span data-stu-id="f1178-175">Select or clear the Allow cycle counting check box.</span></span>
    * <span data-ttu-id="f1178-176">Virkja þennan valkost til að leyfa vinnslu reglulegrar talningar í öllum staðsetningum sem verða flokkaðar eftir þessar staðsetningarforstillingu.</span><span class="sxs-lookup"><span data-stu-id="f1178-176">Enable this option to allow cycle counting processing in all the locations that are going to be grouped by this location profile.</span></span>  
14. <span data-ttu-id="f1178-177">Stækka eða fella saman hlutann Víddir.</span><span class="sxs-lookup"><span data-stu-id="f1178-177">Expand or collapse the Dimensions section.</span></span>
    * <span data-ttu-id="f1178-178">Flipinn Víddir gerir kleift að skilgreina færibreytur og aðferðir til að virkja nákvæmari útreikninga á afkastagetu innan hverrar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="f1178-178">The Dimensions tab allows you to define parameters and methods to enable precise calculations of the load capacity within each of the locations.</span></span>  
15. <span data-ttu-id="f1178-179">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f1178-179">Close the page.</span></span>

## <a name="enable-warehouse-management-parameters"></a><span data-ttu-id="f1178-180">Virkja færibreytur vöruhúsakerfis</span><span class="sxs-lookup"><span data-stu-id="f1178-180">Enable warehouse management parameters</span></span>
1. <span data-ttu-id="f1178-181">Færibreytur fyrir Fara í vöruhúsakerfi.</span><span class="sxs-lookup"><span data-stu-id="f1178-181">Go to Warehouse management parameters.</span></span>
    * <span data-ttu-id="f1178-182">Til að geta keyrt vöruhúsavinnu þarf að setja upp færibreytur fyrir forstillingu notandastaðsetningar af staðsetningu sviðsetningar og endanlegri gerð sendingarstaðsetningar Um leið og færslum á útleið lýkur á endanlegum sendingarstað sem þú skilgreinir eru tengdar færslur á útleið uppfærðar í ‚Tekið til‘.</span><span class="sxs-lookup"><span data-stu-id="f1178-182">To be able to process warehouse work, you need to set parameters for the user location profile the staging location type, and the final shipping location type  As soon as the outbound process ends at the final shipping location type that you define, the related outbound transactions will be updated to ‘Picked’.</span></span>  
2. <span data-ttu-id="f1178-183">Stækka eða fella saman hlutann Forstillingar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="f1178-183">Expand or collapse the Location profiles section.</span></span>
3. <span data-ttu-id="f1178-184">Í reitnum Staðsetning notanda skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f1178-184">In the User location field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f1178-185">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f1178-185">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f1178-186">Stækka eða fella saman hlutann Gerð staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="f1178-186">Expand or collapse the Location types section.</span></span>
6. <span data-ttu-id="f1178-187">Í reitnum Gerð sviðsetningarstaðsetningar skal smella a fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f1178-187">In the Staging location type field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="f1178-188">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f1178-188">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f1178-189">Í reitnum Gerð endanlegs sendingarstaðar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f1178-189">In the Final shipping location type field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="f1178-190">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f1178-190">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="f1178-191">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f1178-191">Close the page.</span></span>

## <a name="define-warehouse-zone-groups"></a><span data-ttu-id="f1178-192">Skilgreina vöruhúsastaðaflokka</span><span class="sxs-lookup"><span data-stu-id="f1178-192">Define warehouse zone groups</span></span>
1. <span data-ttu-id="f1178-193">Fara í Vöruhúsastaðaflokka.</span><span class="sxs-lookup"><span data-stu-id="f1178-193">Go to Warehouse zone groups.</span></span>
    * <span data-ttu-id="f1178-194">Hægt er að nota vöruhúsastaði sem síur til að stýra mismunandi vöruhúsakerfisferlum.</span><span class="sxs-lookup"><span data-stu-id="f1178-194">Warehouse zones can be used as filters for options to control the different warehouse management processes.</span></span> <span data-ttu-id="f1178-195">Það þarf að stofna tímabeltaflokk áður en hægt er að tilgreina svæði.</span><span class="sxs-lookup"><span data-stu-id="f1178-195">You need to create a zone group before you can define a zone.</span></span>  
2. <span data-ttu-id="f1178-196">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f1178-196">Click New.</span></span>
3. <span data-ttu-id="f1178-197">Færa inn gildi í reitnum Auðkenni svæðisflokks.</span><span class="sxs-lookup"><span data-stu-id="f1178-197">In the Zone group ID field, type a value.</span></span>
4. <span data-ttu-id="f1178-198">Færa inn gildi í reitnum Heiti svæðahóps.</span><span class="sxs-lookup"><span data-stu-id="f1178-198">In the Zone group name field, type a value.</span></span>
5. <span data-ttu-id="f1178-199">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f1178-199">Close the page.</span></span>

## <a name="define-warehouse-zones"></a><span data-ttu-id="f1178-200">Skilgreina vöruhúsastaði</span><span class="sxs-lookup"><span data-stu-id="f1178-200">Define Warehouse zones</span></span>
1. <span data-ttu-id="f1178-201">Farið í Svæði.</span><span class="sxs-lookup"><span data-stu-id="f1178-201">Go to Zones.</span></span>
2. <span data-ttu-id="f1178-202">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f1178-202">Click New.</span></span>
3. <span data-ttu-id="f1178-203">Færa inn gildi í reitnum Kenni svæðisauðkennis.</span><span class="sxs-lookup"><span data-stu-id="f1178-203">In the Zone ID field, type a value.</span></span>
4. <span data-ttu-id="f1178-204">Í reitinn Heiti umdæmis skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-204">In the Zone name field, type a value.</span></span>
5. <span data-ttu-id="f1178-205">Í reitnum Auðkenni svæðisflokks skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f1178-205">In the Zone group ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f1178-206">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f1178-206">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f1178-207">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f1178-207">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f1178-208">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f1178-208">Close the page.</span></span>

## <a name="create-locations-using-the-location-setup-wizard"></a><span data-ttu-id="f1178-209">Stofna staðsetningar með því að nota uppsetningarforrit staðsetningar</span><span class="sxs-lookup"><span data-stu-id="f1178-209">Create locations using the Location setup wizard</span></span>
1. <span data-ttu-id="f1178-210">Fara í leiðsagnarforrit uppsetningar Staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="f1178-210">Go to Location setup wizard.</span></span>
2. <span data-ttu-id="f1178-211">Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f1178-211">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f1178-212">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f1178-212">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="f1178-213">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f1178-213">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="f1178-214">Í reitnum Svæðisauðkenni skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f1178-214">In the Zone ID field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f1178-215">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f1178-215">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="f1178-216">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f1178-216">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f1178-217">Í reitnum Kenni lýsingar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f1178-217">In the Location profile ID field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="f1178-218">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f1178-218">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="f1178-219">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f1178-219">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="f1178-220">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="f1178-220">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="f1178-221">Í reitinn Frá númeri skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f1178-221">In the From number field, enter a number.</span></span>
    * <span data-ttu-id="f1178-222">Reitirnir Frá númeri og Til númers skilgreina hversu margar staðsetningar verða stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="f1178-222">The From number and To number fields define how many locations will be created.</span></span> <span data-ttu-id="f1178-223">Til dæmis, ef þú stilltir Frá númer á 1 og Til númers á 3 fyrir allar fjórar línur í staðsetningarsniðinu verða 81 staðsetningar stofnaðar (3x3x3x3).</span><span class="sxs-lookup"><span data-stu-id="f1178-223">For example, if you set From number to 1 and To number to 3 for all four lines in the location format, 81 locations will be created (3x3x3x3).</span></span>  
13. <span data-ttu-id="f1178-224">Í reitinn Til númers skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f1178-224">In the To number field, enter a number.</span></span>
14. <span data-ttu-id="f1178-225">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f1178-225">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="f1178-226">Í reitinn Frá númeri skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f1178-226">In the From number field, enter a number.</span></span>
16. <span data-ttu-id="f1178-227">Í reitinn Til númers skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f1178-227">In the To number field, enter a number.</span></span>
17. <span data-ttu-id="f1178-228">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f1178-228">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="f1178-229">Í reitinn Frá númeri skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f1178-229">In the From number field, enter a number.</span></span>
19. <span data-ttu-id="f1178-230">Í reitinn Til númers skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f1178-230">In the To number field, enter a number.</span></span>
20. <span data-ttu-id="f1178-231">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f1178-231">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="f1178-232">Í reitinn Frá númeri skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f1178-232">In the From number field, enter a number.</span></span>
22. <span data-ttu-id="f1178-233">Í reitinn Til númers skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f1178-233">In the To number field, enter a number.</span></span>
23. <span data-ttu-id="f1178-234">Smellið á „Stofna“.</span><span class="sxs-lookup"><span data-stu-id="f1178-234">Click Create.</span></span>

## <a name="create-locations-manually"></a><span data-ttu-id="f1178-235">Stofna staðsetningar handvirkt</span><span class="sxs-lookup"><span data-stu-id="f1178-235">Create locations manually</span></span>
1. <span data-ttu-id="f1178-236">Fara í Staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="f1178-236">Go to Locations.</span></span>
    * <span data-ttu-id="f1178-237">Auðvelt er að stofna staðsetningar í vöruhúsi á handvirkan hátt.</span><span class="sxs-lookup"><span data-stu-id="f1178-237">Manually creation of locations within a warehouse can easily be done.</span></span> <span data-ttu-id="f1178-238">Heiti staðsetningar og Auðkenni forstillingar staðsetningar eru áskilin gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-238">The location name and the Location profile ID are mandatory values.</span></span>  
2. <span data-ttu-id="f1178-239">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f1178-239">Click New.</span></span>
3. <span data-ttu-id="f1178-240">Í reitinn vöruhús skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-240">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="f1178-241">Í reitinn staðsetning skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-241">In the Location field, type a value.</span></span>
    * <span data-ttu-id="f1178-242">Athugaðu að þú ert að stofna nýja staðsetningu hér, svo að nauðsynlegt er að slá inn nýtt einkvæmt heiti frekar en að velja gamalt.</span><span class="sxs-lookup"><span data-stu-id="f1178-242">Note that you're creating a new location here, so you need to type a new unique name, rather than selecting an existing one.</span></span>  
5. <span data-ttu-id="f1178-243">Færa inn gildi í reitnum Kenni forstillingar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="f1178-243">In the Location profile ID field, type a value.</span></span>
6. <span data-ttu-id="f1178-244">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f1178-244">Close the page.</span></span>

## <a name="define-pack-size-categories"></a><span data-ttu-id="f1178-245">Skilgreina stærðarflokka umbúða</span><span class="sxs-lookup"><span data-stu-id="f1178-245">Define Pack size categories</span></span>
1. <span data-ttu-id="f1178-246">Fara í Stærðarflokka umbúða.</span><span class="sxs-lookup"><span data-stu-id="f1178-246">Go to Pack size categories.</span></span>
    * <span data-ttu-id="f1178-247">Stærðarflokka er hægt að nota til að flokka vörur sem hafa svipaðar efnislegar pökkunarstærðir.</span><span class="sxs-lookup"><span data-stu-id="f1178-247">Pack size categories can be used to group items that have similar physical packing sizes.</span></span> <span data-ttu-id="f1178-248">Í þessu dæmi verður flokkur pökkunarstærða notaður til að stjórna afköstum á tiltektarstaðsetningum innan tiltekin svæðis vöruhússins.</span><span class="sxs-lookup"><span data-stu-id="f1178-248">In this example the pack size category will be used to control the capacity at the picking locations within a specific zone of the warehouse.</span></span> <span data-ttu-id="f1178-249">Vinsamlegast athugið að úthluta verður auðkenni pökkunarstærðarflokks á útgefna afurð einingar til að nota sem hluta af vinnslu birgðamarka.</span><span class="sxs-lookup"><span data-stu-id="f1178-249">Please note that the pack size category ID must be assigned to the released product entity in order to be used as part of the stocking limits processing.</span></span>  
2. <span data-ttu-id="f1178-250">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f1178-250">Click New.</span></span>
3. <span data-ttu-id="f1178-251">Færa inn gildi í reitnum Auðkenni stærðarflokks umbúða.</span><span class="sxs-lookup"><span data-stu-id="f1178-251">In the Pack size category ID field, type a value.</span></span>
4. <span data-ttu-id="f1178-252">Færa inn gildi í reitnum Heiti stærðarflokks umbúða.</span><span class="sxs-lookup"><span data-stu-id="f1178-252">In the Pack size category name field, type a value.</span></span>
5. <span data-ttu-id="f1178-253">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f1178-253">Close the page.</span></span>

## <a name="define-location-stocking-limits"></a><span data-ttu-id="f1178-254">Skilgreina birgðamörk staðsetningar</span><span class="sxs-lookup"><span data-stu-id="f1178-254">Define location stocking limits</span></span>
1. <span data-ttu-id="f1178-255">Fara í Birgðamörk staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="f1178-255">Go to Location stocking limits.</span></span>
    * <span data-ttu-id="f1178-256">Birgðamörk staðsetningar hjálpa við að tryggja að vinna sé ekki stofnuð til að biðja um að birgðir séu settar á staðsetningu sem er ekki með efnislega afkastagetu til að taka við birgðunum.</span><span class="sxs-lookup"><span data-stu-id="f1178-256">Location stocking limits help to make sure that work isn't created to request that inventory to be put in a location that doesn't have the physical capacity to carry the inventory.</span></span>  
2. <span data-ttu-id="f1178-257">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f1178-257">Click New.</span></span>
3. <span data-ttu-id="f1178-258">Í reitinn vöruhús skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-258">In the Warehouse field, type a value.</span></span>
4. <span data-ttu-id="f1178-259">Færa inn gildi í reitnum Kenni forstillingar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="f1178-259">In the Location profile ID field, type a value.</span></span>
5. <span data-ttu-id="f1178-260">Færa inn gildi í reitnum Auðkenni stærðarflokks umbúða.</span><span class="sxs-lookup"><span data-stu-id="f1178-260">In the Pack size category ID field, type a value.</span></span>
6. <span data-ttu-id="f1178-261">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="f1178-261">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="f1178-262">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f1178-262">Click Save.</span></span>
8. <span data-ttu-id="f1178-263">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f1178-263">Close the page.</span></span>

## <a name="define-fixed-picking-locations"></a><span data-ttu-id="f1178-264">Skilgreinið fastar tiltektarstaðsetningar</span><span class="sxs-lookup"><span data-stu-id="f1178-264">Define fixed picking locations</span></span>
1. <span data-ttu-id="f1178-265">Farið í Fastar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="f1178-265">Go to Fixed locations.</span></span>
    * <span data-ttu-id="f1178-266">Hægt er að skilgreina staðsetningar sem nota á hverja afurð eða á afurðarafbrigði.</span><span class="sxs-lookup"><span data-stu-id="f1178-266">You can define the locations to be used per product or per product variant.</span></span> <span data-ttu-id="f1178-267">Hægt er að stofna margar fastar staðsetningar fyrir sömu afurð innan sama vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="f1178-267">It is possible to create multiple fixed locations for the same product within the same warehouse.</span></span>  
2. <span data-ttu-id="f1178-268">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f1178-268">Click New.</span></span>
3. <span data-ttu-id="f1178-269">Í reitnum Vörunúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-269">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="f1178-270">Í reitinn vöruhús skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f1178-270">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="f1178-271">Í reitnum staðsetning skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="f1178-271">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f1178-272">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="f1178-272">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f1178-273">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f1178-273">Close the page.</span></span>


