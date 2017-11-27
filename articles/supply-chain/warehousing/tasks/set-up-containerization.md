--- 
title: "Setja upp gámun"
description: "Þetta aðferð lýsir því hvernig á að gera sjálfvirka gámun á farm í vöruhúsakerfi"
author: YuyuScheller
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 76334f7ee4efe33df4a86aaa11a59748387cec89
ms.openlocfilehash: c5faf926071dec5d2ddc1c9e921a98ecd0754917
ms.contentlocale: is-is
ms.lasthandoff: 11/02/2017

---
# <a name="set-up-containerization"></a><span data-ttu-id="46264-103">Setja upp gámun</span><span class="sxs-lookup"><span data-stu-id="46264-103">Set up containerization</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="46264-104">Þetta aðferð lýsir því hvernig á að gera sjálfvirka gámun á farm í vöruhúsakerfi</span><span class="sxs-lookup"><span data-stu-id="46264-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="46264-105">Sjálfvirk gámun stofnar gáma og tínsluvinnu fyrir sendingar þegar unnið er úr bylgju og hægt er að skipta upp vinnulínum í magn sem passa við gáma.</span><span class="sxs-lookup"><span data-stu-id="46264-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="46264-106">Þetta hjálpar starfsmenn vöruhúss að taka til vörur beint í gám sem var valið.</span><span class="sxs-lookup"><span data-stu-id="46264-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="46264-107">Borið saman við handvirkt pökkunarferli eru verk eins og stofnun gáma, úthluta vörum og lokunar gáma sjálfvirk af kerfinu.</span><span class="sxs-lookup"><span data-stu-id="46264-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="46264-108">Þetta ferli notar USMF sýnifyrirtækið og er framkvæmt af stjórnanda Vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="46264-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="46264-109">Velja bylgjusniðmát</span><span class="sxs-lookup"><span data-stu-id="46264-109">Set up a wave template</span></span>
1. <span data-ttu-id="46264-110">Fara í vöruhúsakerfi > Uppsetning > Bylgjur > bylgjusniðmát.</span><span class="sxs-lookup"><span data-stu-id="46264-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="46264-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="46264-111">Click New.</span></span>
3. <span data-ttu-id="46264-112">Í reitinn Heiti bylgjusniðmáts skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="46264-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="46264-113">Færa inn gildi í reitnum lýsingu bylgjusniðmáts.</span><span class="sxs-lookup"><span data-stu-id="46264-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="46264-114">Sláið inn eða veldu gildi í reitnum svæði.</span><span class="sxs-lookup"><span data-stu-id="46264-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="46264-115">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="46264-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="46264-116">Víkkið út hlutann aðferðir.</span><span class="sxs-lookup"><span data-stu-id="46264-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="46264-117">Valdar aðferðir svæðið skráir aðferðir fyrir valið bylgjusniðmát tegund.</span><span class="sxs-lookup"><span data-stu-id="46264-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="46264-118">Bylgjusniðmátið verður að hafa með gámunar aðferð.</span><span class="sxs-lookup"><span data-stu-id="46264-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="46264-119">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="46264-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="46264-120">Færa inn gildi í svæðinu bylgjuskrefakóði.</span><span class="sxs-lookup"><span data-stu-id="46264-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="46264-121">Færið inn bylgjuskrefskóða fyrir viðbætta aðferð sem má vera hvaða kóði sem er.</span><span class="sxs-lookup"><span data-stu-id="46264-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="46264-122">Hægt er að bæta við aðferð oftar en einu sinni og úthluta mismunandi kóðum fyrir bylgjuskref.</span><span class="sxs-lookup"><span data-stu-id="46264-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="46264-123">Veljið Endurtekin fyrir þennan aðferð á síðu aðferðir Bylgju ferli til að gera þetta.</span><span class="sxs-lookup"><span data-stu-id="46264-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="46264-124">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="46264-124">Click Save.</span></span>
11. <span data-ttu-id="46264-125">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="46264-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="46264-126">Setja upp gámagerð</span><span class="sxs-lookup"><span data-stu-id="46264-126">Set up a container type</span></span>
1. <span data-ttu-id="46264-127">Fara í vöruhúsakerfi  > Uppsetningu  > Gáma  > gámagerðir.</span><span class="sxs-lookup"><span data-stu-id="46264-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="46264-128">Hægt er að skilgreina gáma á Gáms gerðir síðu.</span><span class="sxs-lookup"><span data-stu-id="46264-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="46264-129">Þú getur stillt efnisleg vídd gámanna, þar á meðal töruþungi, hámarks þyngd, hámarksrúmmál, lengd, breidd og hæð.</span><span class="sxs-lookup"><span data-stu-id="46264-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="46264-130">Í þessu dæmi eru þrjár mismunandi stærðum kassar.</span><span class="sxs-lookup"><span data-stu-id="46264-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="46264-131">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="46264-131">Click New.</span></span>
3. <span data-ttu-id="46264-132">Færa inn gildi í svæðinu kóði gámagerðar.</span><span class="sxs-lookup"><span data-stu-id="46264-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="46264-133">Í reitinn Umbúðaþyngd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="46264-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="46264-134">Í reitinn hámarksþyngd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="46264-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="46264-135">Í reitinn Magn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="46264-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="46264-136">Í reitinn Lengd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="46264-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="46264-137">Færið númer inn í svæðið breidd.</span><span class="sxs-lookup"><span data-stu-id="46264-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="46264-138">Færið númer inn í svæðið hæð.</span><span class="sxs-lookup"><span data-stu-id="46264-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="46264-139">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="46264-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="46264-140">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="46264-140">Click Save.</span></span>
12. <span data-ttu-id="46264-141">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="46264-141">Click New.</span></span>
13. <span data-ttu-id="46264-142">Færa inn gildi í svæðinu kóði gámagerðar.</span><span class="sxs-lookup"><span data-stu-id="46264-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="46264-143">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="46264-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="46264-144">Í reitinn Umbúðaþyngd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="46264-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="46264-145">Í reitinn hámarksþyngd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="46264-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="46264-146">Í reitinn Magn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="46264-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="46264-147">Í reitinn Lengd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="46264-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="46264-148">Færið númer inn í svæðið breidd.</span><span class="sxs-lookup"><span data-stu-id="46264-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="46264-149">Færið númer inn í svæðið hæð.</span><span class="sxs-lookup"><span data-stu-id="46264-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="46264-150">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="46264-150">Click Save.</span></span>
22. <span data-ttu-id="46264-151">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="46264-151">Click New.</span></span>
23. <span data-ttu-id="46264-152">Færa inn gildi í svæðinu kóði gámagerðar.</span><span class="sxs-lookup"><span data-stu-id="46264-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="46264-153">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="46264-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="46264-154">Í reitinn Umbúðaþyngd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="46264-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="46264-155">Í reitinn hámarksþyngd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="46264-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="46264-156">Í reitinn Magn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="46264-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="46264-157">Í reitinn Lengd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="46264-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="46264-158">Færið númer inn í svæðið breidd.</span><span class="sxs-lookup"><span data-stu-id="46264-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="46264-159">Færið númer inn í svæðið hæð.</span><span class="sxs-lookup"><span data-stu-id="46264-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="46264-160">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="46264-160">Click Save.</span></span>
32. <span data-ttu-id="46264-161">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="46264-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="46264-162">Setja upp gámaflokk</span><span class="sxs-lookup"><span data-stu-id="46264-162">Set up a container group</span></span>
1. <span data-ttu-id="46264-163">Fara í vöruhúsakerfi  > Uppsetningu  > Gáma  > gámahópar.</span><span class="sxs-lookup"><span data-stu-id="46264-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="46264-164">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="46264-164">Click New.</span></span>
    * <span data-ttu-id="46264-165">Þú getur sett upp rökrétta flokka af gámagerðum.</span><span class="sxs-lookup"><span data-stu-id="46264-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="46264-166">Fyrir hvern hóp er hægt að tilgreinir röð gámar eru pakkaðar og fyllingarhlutfall hvers gáms.</span><span class="sxs-lookup"><span data-stu-id="46264-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.</span></span> <span data-ttu-id="46264-167">Víddarstærð vörunnar er notuð til að ákvarða hvort hún passi í gám.</span><span class="sxs-lookup"><span data-stu-id="46264-167">The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="46264-168">Geymir sem er næst er afhendingardegi stærð vídda vörunnar er notað.</span><span class="sxs-lookup"><span data-stu-id="46264-168">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="46264-169">Ef margar gámagerðum eru í flokki, er ráðlagt að hagræða röðinni eftir stærð, þannig að stærsta gámurinn er fyrst, númer 1 í röðinni og minnsti gámurinn er síðasta.</span><span class="sxs-lookup"><span data-stu-id="46264-169">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="46264-170">Færa inn gildi í reitnum Auðkenni gámahóps.</span><span class="sxs-lookup"><span data-stu-id="46264-170">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="46264-171">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="46264-171">In the Description field, type a value.</span></span>
5. <span data-ttu-id="46264-172">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="46264-172">Click New.</span></span>
6. <span data-ttu-id="46264-173">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="46264-173">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="46264-174">Færa inn eða veljið gildi í svæðinu gerð gáms.</span><span class="sxs-lookup"><span data-stu-id="46264-174">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="46264-175">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="46264-175">Click New.</span></span>
9. <span data-ttu-id="46264-176">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="46264-176">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="46264-177">Færa inn eða veljið gildi í svæðinu gerð gáms.</span><span class="sxs-lookup"><span data-stu-id="46264-177">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="46264-178">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="46264-178">Click New.</span></span>
12. <span data-ttu-id="46264-179">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="46264-179">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="46264-180">Færa inn eða veljið gildi í svæðinu gerð gáms.</span><span class="sxs-lookup"><span data-stu-id="46264-180">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="46264-181">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="46264-181">Click Save.</span></span>
15. <span data-ttu-id="46264-182">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="46264-182">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="46264-183">Setja upp gámaröðunarsniðmát</span><span class="sxs-lookup"><span data-stu-id="46264-183">Set up a container build template</span></span>
1. <span data-ttu-id="46264-184">Fara í vöruhúsakerfi  > Uppsetningu  > Gáma  > gámaröðunarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="46264-184">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="46264-185">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="46264-185">Click New.</span></span>
    * <span data-ttu-id="46264-186">Gámaröðunarsniðmát byggist á hvaða gámunarferli eru framkvæmdar.</span><span class="sxs-lookup"><span data-stu-id="46264-186">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="46264-187">Hver gámaröðunarsniðmát skilgreinir eina gámunarferli sem verða notuð af bylgjusniðmáti.</span><span class="sxs-lookup"><span data-stu-id="46264-187">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="46264-188">Breyta fyrirspurn valkostur gerir kleift að skilgreina skilyrðin sem völdu sniðmáti er unnið úr.</span><span class="sxs-lookup"><span data-stu-id="46264-188">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="46264-189">Til dæmis kannt þú að vilja keyra aðeins gámunarferli fyrir tiltekna viðskiptavini, vörur eða vöruhús eða þá að þú getur bætt viðkomandi fyrirspurn við sniðmátið.</span><span class="sxs-lookup"><span data-stu-id="46264-189">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="46264-190">Svæðið Bylgju skref kóði er hvernig gámaröðunarsniðmát er tengd við skrefin í bylgjusniðmáti.</span><span class="sxs-lookup"><span data-stu-id="46264-190">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="46264-191">Þegar framkvæmt er bylgju ákvarðar hún hvaða gámaröðunarsniðmát eru notaðar til að hefja gámun.</span><span class="sxs-lookup"><span data-stu-id="46264-191">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="46264-192">Reitur grunngerð fyrirspurnar ákvarða hverju á að pakka og hvað á að miða síufyrirspurnina á.</span><span class="sxs-lookup"><span data-stu-id="46264-192">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="46264-193">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="46264-193">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="46264-194">Færa inn gildi í reitnum Kenni gámasniðmáts.</span><span class="sxs-lookup"><span data-stu-id="46264-194">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="46264-195">Í reitinn auðkenni gámahóps skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="46264-195">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="46264-196">Færa inn gildi í svæðinu bylgjuskrefakóði.</span><span class="sxs-lookup"><span data-stu-id="46264-196">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="46264-197">Veljið gátreitinn leyfa að skipta tiltekt.</span><span class="sxs-lookup"><span data-stu-id="46264-197">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="46264-198">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="46264-198">Click Save.</span></span>
9. <span data-ttu-id="46264-199">Smella á Blöndunartakmarkanir gáma.</span><span class="sxs-lookup"><span data-stu-id="46264-199">Click Container mixing constraints.</span></span>
    * <span data-ttu-id="46264-200">Skipti í blöndunarrökum gerir kleift að setja upp reglur fyrir úthlutunarlínur í gáma.</span><span class="sxs-lookup"><span data-stu-id="46264-200">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="46264-201">Til dæmis ef bætt er við svæðið vörunúmer þegar vara er úthlutuð á gáma, er nýjum gámi stofnað þar sem er nýtt vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="46264-201">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="46264-202">Þetta mun koma í veg fyrir að starfsmenn pakki úthlutunarlínum fyrir tvær mismunandi viðskiptavini í sama gám.</span><span class="sxs-lookup"><span data-stu-id="46264-202">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="46264-203">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="46264-203">Click New.</span></span>
11. <span data-ttu-id="46264-204">Í reitnum tafla skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="46264-204">In the Table field, select an option.</span></span>
12. <span data-ttu-id="46264-205">Í reitinn velja Svæði skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="46264-205">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="46264-206">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="46264-206">Click OK.</span></span>


