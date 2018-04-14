--- 
title: "Setja upp sniðmát fyrir taxta"
description: "Þessi verklýsing sýnir hvernig á að setja upp taxtasniðmát."
author: BibiSp
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a3ba01bc05d130991e8a744d9026d53edf93ee20
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="set-up-rate-masters"></a><span data-ttu-id="71554-103">Setja upp sniðmát fyrir taxta</span><span class="sxs-lookup"><span data-stu-id="71554-103">Set up rate masters</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="71554-104">Þessi verklýsing sýnir hvernig á að setja upp taxtasniðmát.</span><span class="sxs-lookup"><span data-stu-id="71554-104">This procedure shows you how to set up a rate master.</span></span> <span data-ttu-id="71554-105">stjórnandi vörustjórnunar setur yfirleitt upp taxtasniðmát, allt eftir samningum sem voru undirritað með í flutningsaðila.</span><span class="sxs-lookup"><span data-stu-id="71554-105">The logistic manager usually sets up rate masters, depending on the contracts signed with the carriers.</span></span> <span data-ttu-id="71554-106">Í þessu tilfelli verður að setja upp taxtasniðmát fyrir flutningsaðila í lofti.</span><span class="sxs-lookup"><span data-stu-id="71554-106">In this scenario you will set up a rate master for an air carrier.</span></span> <span data-ttu-id="71554-107">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="71554-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-rate-master"></a><span data-ttu-id="71554-108">Setja upp taxtasniðmát</span><span class="sxs-lookup"><span data-stu-id="71554-108">Set up rate master</span></span>
1. <span data-ttu-id="71554-109">Fara í flutningsstjórnun > Uppsetning >Einkunn > Taxtasniðmát.</span><span class="sxs-lookup"><span data-stu-id="71554-109">Go to Transportation management > Setup > Rating > Rate master.</span></span>
2. <span data-ttu-id="71554-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="71554-110">Click New.</span></span>
3. <span data-ttu-id="71554-111">Í reitinn Taxtasniðmát skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="71554-111">In the Rate master field, type a value.</span></span>
4. <span data-ttu-id="71554-112">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="71554-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="71554-113">Í reitnum Lýsigagnakenni fyrir taxta skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="71554-113">In the Rating metadata ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="71554-114">Lýsigagnakenni fyrir taxta ákvarða gögn sem þarf fyrir taxtasniðmátið, þar sem það skilgreinir lýsigögn sem TMS vél býst við með þessu taxtasniðmát.</span><span class="sxs-lookup"><span data-stu-id="71554-114">The rating metadata ID will determine the data needed for the rate master, as it defines the metadata expected by the TMS engine using this rate master.</span></span>  
6. <span data-ttu-id="71554-115">Í þessu dæmi skal velja valkostinn P2P</span><span class="sxs-lookup"><span data-stu-id="71554-115">For this example, select the P2P option</span></span>
7. <span data-ttu-id="71554-116">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="71554-116">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="71554-117">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="71554-117">Click Save.</span></span>

## <a name="set-up-rate-base"></a><span data-ttu-id="71554-118">Setja upp taxtagrunn</span><span class="sxs-lookup"><span data-stu-id="71554-118">Set up rate base</span></span>
1. <span data-ttu-id="71554-119">Smellt er á taxtagrunn.</span><span class="sxs-lookup"><span data-stu-id="71554-119">Click Rate base.</span></span>
    * <span data-ttu-id="71554-120">Taxtagrunn ákvarðar gengi farmflytjanda og hægt er að nota til að setja upp uppbyggingu taxta þar sem það byggir upp taxta á rofstöðum sem skilgreint í aðalgögnum skila.</span><span class="sxs-lookup"><span data-stu-id="71554-120">The rate base determines the rate of the carrier, and can be used to set up a tariff structure as it structures the rates in the breakpoints defined in the break master.</span></span>  
2. <span data-ttu-id="71554-121">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="71554-121">Click New.</span></span>
3. <span data-ttu-id="71554-122">Í reitnum Taxtagrunnur skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="71554-122">In the Rate base field, type a value.</span></span>
4. <span data-ttu-id="71554-123">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="71554-123">In the Name field, type a value.</span></span>
5. <span data-ttu-id="71554-124">Í reitnum Sniðmát hlés skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="71554-124">In the Break master field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="71554-125">Sniðmát hlés eru notuð til að skilgreina uppbyggingu verðlagningar og rofstaði hennar.</span><span class="sxs-lookup"><span data-stu-id="71554-125">Break masters are used to define the pricing structure and its breakpoints.</span></span> <span data-ttu-id="71554-126">Uppbygging verðlagningar notar lagskipt verðlagningu sem byggir á efnislegum víddum.</span><span class="sxs-lookup"><span data-stu-id="71554-126">The pricing structure uses tiered pricing that is based on physical dimensions.</span></span>  
6. <span data-ttu-id="71554-127">Í þessu dæmi notarðu þyngd</span><span class="sxs-lookup"><span data-stu-id="71554-127">For this example, use weight</span></span>
7. <span data-ttu-id="71554-128">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="71554-128">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="71554-129">Víxla útvíkkun á liðnum upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="71554-129">Toggle the expansion of the Details section.</span></span>
9. <span data-ttu-id="71554-130">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="71554-130">Click New.</span></span>
10. <span data-ttu-id="71554-131">Í reitnum Póstnúmer affermingar frá skal slá inn ‚30301‘.</span><span class="sxs-lookup"><span data-stu-id="71554-131">In the Drop-off Postal Code From field, type '30301'.</span></span>
11. <span data-ttu-id="71554-132">Í reitnum Póstnúmer affermingar til skal slá inn ‚30318‘.</span><span class="sxs-lookup"><span data-stu-id="71554-132">In the Drop-off Postal Code To field, type '30318'.</span></span>
12. <span data-ttu-id="71554-133">Í reitnum Landsvæði affermingar skal slá inn ‚USA‘.</span><span class="sxs-lookup"><span data-stu-id="71554-133">In the Drop-off Country Region field, type 'USA'.</span></span>
13. <span data-ttu-id="71554-134">Í reitnum <1,00 pund ritið '100'.</span><span class="sxs-lookup"><span data-stu-id="71554-134">In the <1.00 Lbs field, type '100'.</span></span>
    * <span data-ttu-id="71554-135">Setja inn taxtann fyrir hverja pund ef heildarþyngd hleðslu er minna en 1 pund.</span><span class="sxs-lookup"><span data-stu-id="71554-135">Insert the rate per lbs if the total weight of the load is less than 1 pound.</span></span>  
14. <span data-ttu-id="71554-136">Í reitnum <5.00 pund ritið '300'.</span><span class="sxs-lookup"><span data-stu-id="71554-136">In the <5.00 Lbs field, type '300'.</span></span>
    * <span data-ttu-id="71554-137">Setja inn taxtann fyrir hverja pund ef heildarþyngd hleðslu er minna en 5 pund.</span><span class="sxs-lookup"><span data-stu-id="71554-137">Insert the rate per lbs if the total weight of the load is less than 5 pounds.</span></span>  
15. <span data-ttu-id="71554-138">Í reitnum < 20,00 pund ritið '500'.</span><span class="sxs-lookup"><span data-stu-id="71554-138">In the <20.00 Lbs field, type '500'.</span></span>
    * <span data-ttu-id="71554-139">Setja inn taxtann fyrir hverja pund ef heildarþyngd hleðslu er minna en 20 pund.</span><span class="sxs-lookup"><span data-stu-id="71554-139">Insert the rate per lbs if the total weight of the load is less than 20 pounds.</span></span>  
16. <span data-ttu-id="71554-140">Í reitnum < 100,00 pund ritið '1000'.</span><span class="sxs-lookup"><span data-stu-id="71554-140">In the <100.00 Lbs field, type '1000'.</span></span>
    * <span data-ttu-id="71554-141">Setja inn taxtann fyrir hverja pund ef heildarþyngd hleðslu er minna en 100 pund.</span><span class="sxs-lookup"><span data-stu-id="71554-141">Insert the rate per lbs if the total weight of the load is less than 100 pounds.</span></span>  
17. <span data-ttu-id="71554-142">Í reitnum < 1000,00 pund ritið '3000'.</span><span class="sxs-lookup"><span data-stu-id="71554-142">In the <1,000.00 Lbs field, type '3000'.</span></span>
    * <span data-ttu-id="71554-143">Setja inn taxtann fyrir hverja pund ef heildarþyngd hleðslu er minni en 1000 pund.</span><span class="sxs-lookup"><span data-stu-id="71554-143">Insert the rate per lbs if the total weight of the load is less than 1000 pounds.</span></span>  
18. <span data-ttu-id="71554-144">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="71554-144">Click Save.</span></span>
19. <span data-ttu-id="71554-145">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="71554-145">Close the page.</span></span>

## <a name="assign-rate-base"></a><span data-ttu-id="71554-146">Úthluta taxtagrunn</span><span class="sxs-lookup"><span data-stu-id="71554-146">Assign rate base</span></span>
1. <span data-ttu-id="71554-147">Víxla útvíkkun á hluta úthlutana úr taxtagrunnum .</span><span class="sxs-lookup"><span data-stu-id="71554-147">Toggle the expansion of the Rate base assignments section.</span></span>
2. <span data-ttu-id="71554-148">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="71554-148">Click New.</span></span>
    * <span data-ttu-id="71554-149">Hægt er að hafa nokkrar úthlutanir taxtagrunns fyrir hverja taxtasniðmát.</span><span class="sxs-lookup"><span data-stu-id="71554-149">You can have several rate base assignments for each rate master.</span></span> <span data-ttu-id="71554-150">Þetta gerir mögulegt að stofna nokkra mismunandi verðpunkta fyrir hvern farmflytjanda eftir áfangastaði, þjónustu eða mismunandi taxtagrunnum.</span><span class="sxs-lookup"><span data-stu-id="71554-150">This makes it possible to create several different price points for each carrier depending on destinations, services, or different rate bases.</span></span> <span data-ttu-id="71554-151">Í þessu ferli verður aðeins að stofna eina úthlutun taxtagrunns.</span><span class="sxs-lookup"><span data-stu-id="71554-151">In this procedure you will only create one rate base assignment.</span></span>  
3. <span data-ttu-id="71554-152">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="71554-152">In the Name field, type a value.</span></span>
4. <span data-ttu-id="71554-153">Í reitnum Taxtagrunnur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="71554-153">In the Rate base field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="71554-154">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="71554-154">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="71554-155">Í reitnum Þjónusta skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="71554-155">In the Service field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="71554-156">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="71554-156">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="71554-157">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="71554-157">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="71554-158">Í Svæðið Póstnúmer þar sem sótt er, skal færa inn '98052'.</span><span class="sxs-lookup"><span data-stu-id="71554-158">In the Pick-up Postal Code field, type '98052'.</span></span>
    * <span data-ttu-id="71554-159">Tilgreina hvaða póstnúmer þessa úthlutun taxtagrunns á að gilda frá.</span><span class="sxs-lookup"><span data-stu-id="71554-159">Specify which postal code this rate base assignment should be valid from.</span></span>    
10. <span data-ttu-id="71554-160">Í reitnum Landsvæði þar sem sótt er, skal slá inn ‚USA‘.</span><span class="sxs-lookup"><span data-stu-id="71554-160">In the Pick-up Country Region field, type 'USA'.</span></span>
11. <span data-ttu-id="71554-161">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="71554-161">Click Save.</span></span>


