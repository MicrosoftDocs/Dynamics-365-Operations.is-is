--- 
title: 'Skilgreina reglulega talningu '
description: "Reglulega talningu er vöruhúsið ferli sem hægt er að nota til að endurskoða vörur á lager."
author: MarkusFogelberg
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f9cdb0a7de0199363279c53e817c98085b31fe6b
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="define-cycle-counting"></a><span data-ttu-id="dd746-103">Skilgreina reglulega talningu </span><span class="sxs-lookup"><span data-stu-id="dd746-103">Define cycle counting</span></span> 

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dd746-104">Reglulega talningu er vöruhúsið ferli sem hægt er að nota til að endurskoða vörur á lager.</span><span class="sxs-lookup"><span data-stu-id="dd746-104">Cycle counting is a warehouse process that you can use to audit on-hand inventory items.</span></span> <span data-ttu-id="dd746-105">Þetta verk sýnir hvernig á að: setja upp sjálfgefinn verkforgang talningar; virkja valmyndaratriði fartækis til að keyra bæði tínslu- og talningaraðgerðir; virkja kveikju þröskulds talningar þegar staðsetning tæmist; virkja áætlun um reglulega talningu fyrir tiltekna vöru innan tiltekins vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="dd746-105">This task recording shows how to set up the default counting work priority, enable a mobile device menu item to process both picking and counting operations, enable a counting threshold trigger when a location becomes empty, and enable a cycle counting plan for a specific item in a specific warehouse.</span></span> <span data-ttu-id="dd746-106">Þessi verk eru yfirleitt unnin af stjórnanda vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="dd746-106">Typically, these tasks are performed by a warehouse manager.</span></span> <span data-ttu-id="dd746-107">Hægt er að fara í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða þín eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="dd746-107">You can go through this procedure in the USMF demo data company or in your own data.</span></span>


## <a name="set-the-priority-of-counting-work"></a><span data-ttu-id="dd746-108">Stilla forgang talningar</span><span class="sxs-lookup"><span data-stu-id="dd746-108">Set the priority of counting work</span></span>
1. <span data-ttu-id="dd746-109">Fara í vöruhúsakerfi > Uppsetning > Færibreytur vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="dd746-109">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="dd746-110">Smellt er á flipann Regluleg talningu.</span><span class="sxs-lookup"><span data-stu-id="dd746-110">Click the Cycle counting tab.</span></span>
3. <span data-ttu-id="dd746-111">Í reitnum Sjálfgefinn forgangur verkforgangs reglulegrar talningar skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="dd746-111">In the Default cycle count work priority field, enter a number.</span></span>
    * <span data-ttu-id="dd746-112">Þetta skref mun breyta forgangi reglulegrar talningarvinnu samanborið við aðrar gerðir vinnu í vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="dd746-112">This step changes the priority of cycle counting work compared to other types of work in the warehouse.</span></span> <span data-ttu-id="dd746-113">Ef þú setur inn lægri tölu fyrir reglulega talningu en fyrir aðrar gerðir vinnu hækkar það forgang vinnu reglulegrar talningar.</span><span class="sxs-lookup"><span data-stu-id="dd746-113">By entering a number that is lower than the number for other types of work, you raise the priority of the cycle counting work.</span></span>  
4. <span data-ttu-id="dd746-114">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="dd746-114">Click Save.</span></span>
5. <span data-ttu-id="dd746-115">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="dd746-115">Close the page.</span></span>

## <a name="enable-the-mobile-device"></a><span data-ttu-id="dd746-116">Virkja fartækið</span><span class="sxs-lookup"><span data-stu-id="dd746-116">Enable the mobile device</span></span>
1. <span data-ttu-id="dd746-117">Fara í vöruhúsakerfi > Uppsetning > fartækis > Valmyndaratriði fartækis</span><span class="sxs-lookup"><span data-stu-id="dd746-117">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="dd746-118">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="dd746-118">Click New.</span></span>
3. <span data-ttu-id="dd746-119">Í svæðið heiti valmyndaratriðis, færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="dd746-119">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="dd746-120">Í reitinn Titill skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="dd746-120">In the Title field, type a value.</span></span>
5. <span data-ttu-id="dd746-121">Í reitnum Stilling velurðu „Vinna“.</span><span class="sxs-lookup"><span data-stu-id="dd746-121">In the Mode field, select 'Work'.</span></span>
6. <span data-ttu-id="dd746-122">Stilltu valkostinn Nota fyrirliggjandi verk á Já.</span><span class="sxs-lookup"><span data-stu-id="dd746-122">Set the Use existing work option to Yes.</span></span>
    * <span data-ttu-id="dd746-123">Þegar þessi valkostur er settur á Já leitar kerfið að fyrirliggjandi vinnu þegar valmyndaratriði fartækis er notað.</span><span class="sxs-lookup"><span data-stu-id="dd746-123">When you set this option to Yes, the system will look for existing work when the mobile device menu item is used.</span></span>  
7. <span data-ttu-id="dd746-124">Í reitnum Stýrt af velurðu 'Stýrt af Kerfi'.</span><span class="sxs-lookup"><span data-stu-id="dd746-124">In the Directed by field, select 'System directed'.</span></span>
    * <span data-ttu-id="dd746-125">Þegar „Stýrt af kerfi“ er valið, verður vöruhúsastarfsmanni stýrt í átt að opinni vinnu sem er í skilgreindum vinnuklösum.</span><span class="sxs-lookup"><span data-stu-id="dd746-125">When "System directed" is selected, the warehouse worker will be directed to open work that is in defined work classes.</span></span> <span data-ttu-id="dd746-126">(Við munum stofna þessa vinnuklasa næst.)</span><span class="sxs-lookup"><span data-stu-id="dd746-126">(We will create these work classes next.)</span></span>  
8. <span data-ttu-id="dd746-127">Stækka eða fella saman hlutann vinnuklasar.</span><span class="sxs-lookup"><span data-stu-id="dd746-127">Expand or collapse the Work classes section.</span></span>
    * <span data-ttu-id="dd746-128">Næst munum við stofna tvo vinnuklasa sem verða notaðir með þessu valmyndaratriði fartækis.</span><span class="sxs-lookup"><span data-stu-id="dd746-128">Next, we will create two work classes that will be used with this mobile device menu item.</span></span> <span data-ttu-id="dd746-129">Þegar valmyndaratriðið er notað, verður sett fram fyrirspurn um þessa vinnuklasa, og vinnan sem er efst í forgangsröðinni verður sýnd notandanum.</span><span class="sxs-lookup"><span data-stu-id="dd746-129">When the menu item is used, these work classes will be queried, and the work that has the highest priority will be shown to the user.</span></span>  
9. <span data-ttu-id="dd746-130">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="dd746-130">Click New.</span></span>
10. <span data-ttu-id="dd746-131">Í reitnum Kenni vinnuklasa skal velja gildi.</span><span class="sxs-lookup"><span data-stu-id="dd746-131">In the Work class ID field, select a value.</span></span>
11. <span data-ttu-id="dd746-132">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="dd746-132">Click New.</span></span>
12. <span data-ttu-id="dd746-133">Í reitnum Kenni vinnuklasa skal velja gildi.</span><span class="sxs-lookup"><span data-stu-id="dd746-133">In the Work class ID field, select a value.</span></span>
13. <span data-ttu-id="dd746-134">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="dd746-134">Click Save.</span></span>
14. <span data-ttu-id="dd746-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="dd746-135">Close the page.</span></span>
15. <span data-ttu-id="dd746-136">Fara í vöruhúsakerfi > Uppsetning > fartækis > Valmynd fartækis</span><span class="sxs-lookup"><span data-stu-id="dd746-136">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
16. <span data-ttu-id="dd746-137">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="dd746-137">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="dd746-138">Í trénu, skal velja þau valmyndaratriði sem þú varst að stofna.</span><span class="sxs-lookup"><span data-stu-id="dd746-138">In the tree, select 'the menu item that you just created'.</span></span>
18. <span data-ttu-id="dd746-139">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="dd746-139">Click Edit.</span></span>
19. <span data-ttu-id="dd746-140">Smellt er á örina til að bæta við valmyndaratriði við valmyndina.</span><span class="sxs-lookup"><span data-stu-id="dd746-140">Click the arrow to add the menu item to the menu.</span></span>
20. <span data-ttu-id="dd746-141">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="dd746-141">Click Save.</span></span>

## <a name="create-a-counting-threshold"></a><span data-ttu-id="dd746-142">Stofna þröskuld fyrir talningu</span><span class="sxs-lookup"><span data-stu-id="dd746-142">Create a counting threshold</span></span>
1. <span data-ttu-id="dd746-143">Fara í vöruhúsakerfi > Uppsetning >Reglulega talningu > Þröskulda fyrir reglulega talningu.</span><span class="sxs-lookup"><span data-stu-id="dd746-143">Go to Warehouse management > Setup > Cycle counting > Cycle count thresholds.</span></span>
2. <span data-ttu-id="dd746-144">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="dd746-144">Click New.</span></span>
3. <span data-ttu-id="dd746-145">Í reitnum Auðkenni þröskulds fyrir reglulega talningu skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="dd746-145">In the Cycle counting threshold ID field, type a value.</span></span>
4. <span data-ttu-id="dd746-146">Stilltu valkostinn Vinna reglulegrar talningar strax á Já.</span><span class="sxs-lookup"><span data-stu-id="dd746-146">Set the Process cycle counting immediately option to Yes.</span></span>
5. <span data-ttu-id="dd746-147">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="dd746-147">In the Description field, type a value.</span></span>
6. <span data-ttu-id="dd746-148">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="dd746-148">Click Save.</span></span>
7. <span data-ttu-id="dd746-149">Smellt er á Velja staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="dd746-149">Click Select locations.</span></span>
8. <span data-ttu-id="dd746-150">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="dd746-150">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="dd746-151">Veljið gildi í reitnum Skilyrði.</span><span class="sxs-lookup"><span data-stu-id="dd746-151">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="dd746-152">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="dd746-152">Click OK.</span></span>
11. <span data-ttu-id="dd746-153">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="dd746-153">Close the page.</span></span>

## <a name="create-a-cycle-count-plan"></a><span data-ttu-id="dd746-154">Stofna áætlun um reglulega talningu</span><span class="sxs-lookup"><span data-stu-id="dd746-154">Create a cycle count plan</span></span>
1. <span data-ttu-id="dd746-155">Fara í vöruhúsakerfi > Uppsetning > Reglulega talningu > Áætlanir um reglulega talningu.</span><span class="sxs-lookup"><span data-stu-id="dd746-155">Go to Warehouse management > Setup > Cycle counting > Cycle count plans.</span></span>
2. <span data-ttu-id="dd746-156">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="dd746-156">Click New.</span></span>
3. <span data-ttu-id="dd746-157">Í reitnum Auðkenni fyrir áætlun um reglulega talningu skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="dd746-157">In the Cycle counting plan ID field, type a value.</span></span>
4. <span data-ttu-id="dd746-158">Í reitinn Lýsing skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="dd746-158">In the Description field, type a value.</span></span>
5. <span data-ttu-id="dd746-159">Í reitnum Hámarksfjöldi reglulegrar talningar skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="dd746-159">In the Maximum number of cycle counts field, enter a number.</span></span>
6. <span data-ttu-id="dd746-160">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="dd746-160">Click Save.</span></span>
7. <span data-ttu-id="dd746-161">Smellt er á Velja staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="dd746-161">Click Select locations.</span></span>
8. <span data-ttu-id="dd746-162">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="dd746-162">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="dd746-163">Veljið gildi í reitnum Skilyrði.</span><span class="sxs-lookup"><span data-stu-id="dd746-163">In the Criteria field, select a value.</span></span>
10. <span data-ttu-id="dd746-164">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="dd746-164">Click OK.</span></span>
11. <span data-ttu-id="dd746-165">Færið inn númer í reitinn Dagar á milli reglulegrar talninga.</span><span class="sxs-lookup"><span data-stu-id="dd746-165">In the Days between cycle counting field, enter a number.</span></span>
    * <span data-ttu-id="dd746-166">Til dæmis ef gildið sem er skilgreint í Dagar á milli reglulegrar talninga er 5 verður vinna reglulegrar talningar stofnuð á fimm daga fresti.</span><span class="sxs-lookup"><span data-stu-id="dd746-166">For example, if the Days between cycle counting field is set to 5, cycle counting work will be created every five days.</span></span> <span data-ttu-id="dd746-167">Hins vegar ef unnið er úr vinnu reglulegrar talningar á degi Þrír mun næsta reglulega talning stofnast fimm dögum eftir að síðasta reglulega talning var unnin, á degi 8.</span><span class="sxs-lookup"><span data-stu-id="dd746-167">However, if cycle counting work is processed on day three, the next cycle counting work will be created five days after the last cycle counting was processed, on day 8.</span></span>  
12. <span data-ttu-id="dd746-168">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="dd746-168">Click Save.</span></span>
13. <span data-ttu-id="dd746-169">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="dd746-169">Click New.</span></span>
14. <span data-ttu-id="dd746-170">Í reitinn raðnúmer skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="dd746-170">In the Sequence number field, enter a number.</span></span>
    * <span data-ttu-id="dd746-171">Röðunin er frá lægsta númerinu til hæsta númersins.</span><span class="sxs-lookup"><span data-stu-id="dd746-171">The sort is from the smallest number to the largest number.</span></span> <span data-ttu-id="dd746-172">Gildið verður að vera meira en 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="dd746-172">The value must be more than 0 (zero).</span></span>  
15. <span data-ttu-id="dd746-173">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="dd746-173">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="dd746-174">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="dd746-174">In the Description field, type a value.</span></span>
17. <span data-ttu-id="dd746-175">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="dd746-175">Click Save.</span></span>
18. <span data-ttu-id="dd746-176">Smella á Skilgreina fyrirspurn um afurð</span><span class="sxs-lookup"><span data-stu-id="dd746-176">Click Define product query.</span></span>
19. <span data-ttu-id="dd746-177">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="dd746-177">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="dd746-178">Í reitinn Skilyrði skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="dd746-178">In the Criteria field, enter or select a value.</span></span>
21. <span data-ttu-id="dd746-179">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="dd746-179">Click OK.</span></span>
22. <span data-ttu-id="dd746-180">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="dd746-180">Close the page.</span></span>


