---
title: Flokkun tiltektarlínu
description: Þetta efnisatriði veitir yfirlit yfir flokkun tiltektarlínu.
author: Mirzaab
manager: tfehr
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: b3497d43a500898207ed5154721ee0e3a327fb93
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017737"
---
# <a name="pick-line-grouping"></a><span data-ttu-id="7cc5e-103">Flokkun tiltektarlínu</span><span class="sxs-lookup"><span data-stu-id="7cc5e-103">Pick line grouping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7cc5e-104">Við flokkun tiltektarlínu er hægt að sameina margar vinnulínur sem hafa sama hlut og staðsetningu í staka tínslu sem er kynnt notandanum í fartæki.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-104">In pick line grouping, multiple work lines that have the same item and location can be combined into a single pick that is presented to the user on a mobile device.</span></span> <span data-ttu-id="7cc5e-105">Þess vegna geta starfsmenn vörugeymslu fengið skilvirkustu fyrirmælin sem mögulegt er, en nauðsynlegum aðskilnaði vinnulína í kerfinu er einnig haldið (til dæmis fyrir mismunandi gáma og pantanir).</span><span class="sxs-lookup"><span data-stu-id="7cc5e-105">Therefore, warehouse workers can receive the most efficient instructions that are possible, but the required separation of work lines in the system is also maintained (for example, for different containers and orders).</span></span>

## <a name="set-up-pick-line-grouping"></a><span data-ttu-id="7cc5e-106">Setja upp flokkun tiltektarlínu</span><span class="sxs-lookup"><span data-stu-id="7cc5e-106">Set up pick line grouping</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="7cc5e-107">Stofna valmyndaratriði fartækis</span><span class="sxs-lookup"><span data-stu-id="7cc5e-107">Create a mobile device menu item</span></span>

1. <span data-ttu-id="7cc5e-108">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækja** og búðu til nýtt valmyndaratriði sem heitir **Línutiltekt söluhópa - Stýrt af notanda**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-108">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items** , and create a new menu item that is named **Sales group line picking – User directed**.</span></span>
2. <span data-ttu-id="7cc5e-109">Undir **Valmyndaratriði fyrirtækis** stillirðu eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="7cc5e-109">Under **Mobile device menu items** , set the following values:</span></span>

    - <span data-ttu-id="7cc5e-110">Í reitinn **Heiti valmyndaratriðis** slærðu inn **Sölutiltekt - Flokkalína**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-110">In the **Menu item name** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="7cc5e-111">Í reitinn **Titill** slærðu inn **Sölutiltekt - Flokkalína**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-111">In the **Title** field, enter **Sales Pick - Group line**.</span></span>
    - <span data-ttu-id="7cc5e-112">Í reitnum **Stilling** velurðu **Vinna**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-112">In the **Mode** field, select **Work**.</span></span>
    - <span data-ttu-id="7cc5e-113">Stilltu valkostinn **Nota fyrirliggjandi vinnu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-113">Set the **Use existing work** option to **Yes**.</span></span>

3. <span data-ttu-id="7cc5e-114">Á flýtiflipanum **Almennt** geturðu stillt eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="7cc5e-114">On the **General** FastTab, you can set the following values:</span></span>

    - <span data-ttu-id="7cc5e-115">Í reitnum **Stýrt af** velurðu **Stýrt af notanda**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-115">In the **Directed by** field, select **User directed**.</span></span>
    - <span data-ttu-id="7cc5e-116">Stilltu valkostinn **Mynda númeraplötu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-116">Set the **Generate license plate** option to **Yes**.</span></span>
    - <span data-ttu-id="7cc5e-117">Stilltu valkostinn **Flokkatiltekt** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-117">Set the **Group pick** option to **Yes**.</span></span>

4. <span data-ttu-id="7cc5e-118">Á flýtiflipanum **Vinnuklasar** skaltu fylgja þessum skrefum til að stilla gilda vinnuflokka fyrir valmyndaratriðið í fartækinu:</span><span class="sxs-lookup"><span data-stu-id="7cc5e-118">On the **Work classes** FastTab, follow these steps to configure the valid work classes for the mobile device menu item:</span></span>

    1. <span data-ttu-id="7cc5e-119">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-119">Select **New**.</span></span>
    2. <span data-ttu-id="7cc5e-120">Í reitnum **Auðkenni vinnuklasa** velurðu **Sala** eða **Tiltekt sölupöntunar** , eftir því vöruhúsi sem þú ætlar að nota.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-120">In the **Work class ID** field, select **Sales** or **SO Pick** , depending on the warehouse that you will use.</span></span>
    3. <span data-ttu-id="7cc5e-121">Í reitnum **Gerð verkbeiðni** velurðu **Sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-121">In the **Work order type** field, select **Sales orders**.</span></span>

### <a name="set-up-a-mobile-device-menu"></a><span data-ttu-id="7cc5e-122">Setja upp valmynd fartækja</span><span class="sxs-lookup"><span data-stu-id="7cc5e-122">Set up a mobile device menu</span></span>

1. <span data-ttu-id="7cc5e-123">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-123">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span> 
1. <span data-ttu-id="7cc5e-124">Bættu valmyndaratriðinu sem þú bjóst til við valmyndina.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-124">Add the menu item that you just created to the desired menu.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="7cc5e-125">Setja upp vinnusniðmát</span><span class="sxs-lookup"><span data-stu-id="7cc5e-125">Set up a work template</span></span>

1. <span data-ttu-id="7cc5e-126">Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-126">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="7cc5e-127">Finndu vinnusniðmátið sem ætti að nota með þessari aðgerð.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-127">Find the work template that should be used with this function.</span></span> <span data-ttu-id="7cc5e-128">Fyrir þetta dæmi skaltu velja staðalinn **51 tiltekt á stig** Contoso-vinnusniðmát.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-128">For this example, select the standard **51 Pick to stage** Contoso work template.</span></span>
1. <span data-ttu-id="7cc5e-129">Í valmyndinni velurðu **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-129">On the menu, select **Edit query**.</span></span>
1. <span data-ttu-id="7cc5e-130">Á flipanum **Röðun** velurðu **Bæta við** og stillir síðan eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="7cc5e-130">On the **Sorting** tab, select **Add** , and then set the following values:</span></span>

    - <span data-ttu-id="7cc5e-131">Í reitnum **Tafla** velurðu **Tímabundnar vinnufærslur**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-131">In the **Table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="7cc5e-132">Í reitnum **Afleidd tafla** velurðu **Tímabundnar vinnufærslur**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-132">In the **Derived table** field, select **Temporary work transactions**.</span></span>
    - <span data-ttu-id="7cc5e-133">Í reitinn **Reitur** velurðu **Vörunúmer**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-133">In the **Field** field, select **Item number**.</span></span>
    - <span data-ttu-id="7cc5e-134">Í reitnum **Leitarstefna** velurðu **Hækkandi**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-134">In the **Search direction** field, select **Ascending**.</span></span>

> [!NOTE]
> <span data-ttu-id="7cc5e-135">Til að flokkunarvirkni tiltektarlínu virki verður að flokka vinnulínurnar eftir auðkenni hlutar.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-135">For the pick line grouping functionality to work, the work lines must be sorted by item ID.</span></span> <span data-ttu-id="7cc5e-136">Ef línum sem eru með sömu hlutina er ekki skipt í röð hver á eftir annarri verða þær ekki flokkaðar.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-136">If lines that have the same items aren't sequenced one after another, they won't be grouped.</span></span>

## <a name="example"></a><span data-ttu-id="7cc5e-137">Dæmi</span><span class="sxs-lookup"><span data-stu-id="7cc5e-137">Example</span></span>

### <a name="create-picking-work"></a><span data-ttu-id="7cc5e-138">Stofna tiltektarvinnu</span><span class="sxs-lookup"><span data-stu-id="7cc5e-138">Create picking work</span></span>

<span data-ttu-id="7cc5e-139">Áður en þú getur sett upp flokkun tiltektarlína verður þú að búa til einhverja hæfa vinnu á útleið.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-139">Before you can set up pick line grouping, you must create some eligible outbound work.</span></span>

1. <span data-ttu-id="7cc5e-140">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-140">Go to **Sales and Marketing \> Sales orders \> All sales orders**.</span></span>
2. <span data-ttu-id="7cc5e-141">Smellið á **Nýtt** til að stofna nýja sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-141">Select **New** to create a sales order.</span></span> 
3. <span data-ttu-id="7cc5e-142">Í reitnum **Viðskiptavinalykill** velurðu einhvern viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-142">In the **Customer account** field, select any customer.</span></span> 
4. <span data-ttu-id="7cc5e-143">Á flýtiflipanum **Almennt** , í reitnum **Vöruhús** , er valið **51**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-143">On the **General** FastTab, in the **Warehouse** field, select **51**.</span></span> <span data-ttu-id="7cc5e-144">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-144">Then select **OK**.</span></span>
5. <span data-ttu-id="7cc5e-145">Undir **Sölupöntunarlínur** skaltu bæta við eftirfarandi sex línum:</span><span class="sxs-lookup"><span data-stu-id="7cc5e-145">Under **Sales order lines** , add the following six lines:</span></span>

    - <span data-ttu-id="7cc5e-146">**Lína 1:** Í reitnum **Vörunúmer** velurðu **M9200**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-146">**Line 1:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="7cc5e-147">Í **Magn** reitinn er fært inn **3**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-147">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="7cc5e-148">**Lína 2:** Í reitnum **Vörunúmer** velurðu **M9201**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-148">**Line 2:** In the **Item number** field, select **M9201**.</span></span> <span data-ttu-id="7cc5e-149">Í **Magn** reitinn er fært inn **3**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-149">In the **Quantity** field, enter **3**.</span></span> 
    - <span data-ttu-id="7cc5e-150">**Lína 3:** Í reitnum **Vörunúmer** velurðu **M9202**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-150">**Line 3:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="7cc5e-151">Í **Magn** reitinn er fært inn **2**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-151">In the **Quantity** field, enter **2**.</span></span> 
    - <span data-ttu-id="7cc5e-152">**Lína 4:** Í reitnum **Vörunúmer** velurðu **M9200**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-152">**Line 4:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="7cc5e-153">Í **Magn** reitinn er fært inn **1**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-153">In the **Quantity** field, enter **1**.</span></span> 
    - <span data-ttu-id="7cc5e-154">**Lína 5:** Í reitnum **Vörunúmer** velurðu **M9200**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-154">**Line 5:** In the **Item number** field, select **M9200**.</span></span> <span data-ttu-id="7cc5e-155">Í **Magn** reitinn er fært inn **3**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-155">In the **Quantity** field, enter **3**.</span></span>
    - <span data-ttu-id="7cc5e-156">**Lína 6:** Í reitnum **Vörunúmer** velurðu **M9202**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-156">**Line 6:** In the **Item number** field, select **M9202**.</span></span> <span data-ttu-id="7cc5e-157">Í **Magn** reitinn er fært inn **7**.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-157">In the **Quantity** field, enter **7**.</span></span> 

    <span data-ttu-id="7cc5e-158">Hér er yfirlit yfir heildarmagn fyrir hverja vöru:</span><span class="sxs-lookup"><span data-stu-id="7cc5e-158">Here is a summary of the total quantities for each item:</span></span>

    - <span data-ttu-id="7cc5e-159">**Vara M9200:** 7 stykki</span><span class="sxs-lookup"><span data-stu-id="7cc5e-159">**Item M9200:** 7 each</span></span>
    - <span data-ttu-id="7cc5e-160">**Vara M9201:** 3 stykki</span><span class="sxs-lookup"><span data-stu-id="7cc5e-160">**Item M9201:** 3 each</span></span>
    - <span data-ttu-id="7cc5e-161">**Vara M9202:** 9 stykki</span><span class="sxs-lookup"><span data-stu-id="7cc5e-161">**Item M9202:** 9 each</span></span>

6. <span data-ttu-id="7cc5e-162">Áður en þú losar pantanir í vöruhúsið verður þú að ganga úr skugga um að tiltektarstaðirnir séu með nægar birgðir fyrir allar vörur í öllum pöntunum.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-162">Before you release the orders to the warehouse, you must make sure that the pick locations have enough inventory for all the items on all the orders.</span></span> <span data-ttu-id="7cc5e-163">Farðu yfir stillinguna **Staðsetningartilskipun** til að ákvarða hvaða tínslustaðir eru notaðir við tínslu sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-163">Review the **Location directive** setting to determine which picking locations are used for sales order picking.</span></span>
7. <span data-ttu-id="7cc5e-164">Bókaðu birgðirnar og slepptu þeim í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-164">Reserve the inventory, and release it to the warehouse.</span></span> <span data-ttu-id="7cc5e-165">Vinnukenni sem hefur sex línur er búið til.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-165">A work ID that has six lines is created.</span></span> <span data-ttu-id="7cc5e-166">Línunum er raðað eftir vörunúmeri.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-166">The lines are sorted by item number.</span></span>

### <a name="run-the-mobile-device-flow"></a><span data-ttu-id="7cc5e-167">Keyrðu fartækjaflæðið</span><span class="sxs-lookup"><span data-stu-id="7cc5e-167">Run the mobile device flow</span></span>

1. <span data-ttu-id="7cc5e-168">Í fartækinu velurðu valmynd sem inniheldur nýtt valmyndaratriði fartækis.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-168">On the mobile device, select the menu that includes the new mobile device menu item.</span></span>
1. <span data-ttu-id="7cc5e-169">Veldu valmyndaratriðið **Sölutiltekt - Flokkalína** og hefðu tiltektina.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-169">Select the **Sales Pick – Group line** menu item, and initiate the pick.</span></span>

    <span data-ttu-id="7cc5e-170">Eftir að þú hefur valið valmyndina og slegið inn vinnukenið sérðu tiltektarskrefið þar sem allar tiltektarlínur fyrir vöruna M9200 eru flokkaðar.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-170">After you select the menu and enter the work ID, you see the pick step where all pick lines for item M9200 are grouped.</span></span> <span data-ttu-id="7cc5e-171">Þú færð leiðbeiningar um að velja 7 stykki af vöru M9200.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-171">You receive an instruction to pick 7 each of item M9200.</span></span>

1. <span data-ttu-id="7cc5e-172">Staðfestu tiltektarskrefið.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-172">Confirm the pick step.</span></span> 
1. <span data-ttu-id="7cc5e-173">Farðu á biðlaraskjáinn í vinnunni sem er í gangi og taktu eftir því að öllum þremur tiltektarlínum fyrir vöruna M9200 var lokað samtímis.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-173">Go to the client screen of the work in process, and notice that all three pick lines for item M9200 were closed simultaneously.</span></span>

    <span data-ttu-id="7cc5e-174">Vinnulína 4 er kynnt.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-174">Work line 4 is presented.</span></span>

1. <span data-ttu-id="7cc5e-175">Staðfestu tiltektarskrefið.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-175">Confirm the pick step.</span></span>

    <span data-ttu-id="7cc5e-176">Síðasta tiltektarstigið í fartækinu safnar saman síðustu tveimur tiltektarlínunum úr vinnupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-176">The last pick step on the mobile device aggregates the last two pick lines from the work order.</span></span>

1. <span data-ttu-id="7cc5e-177">Ljúktu við tiltektarskrefið fyrir 9 stykki af vöru M9202.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-177">Complete the pick step for 9 each of item M9202.</span></span>
1. <span data-ttu-id="7cc5e-178">Staðfestu frágangsskrefið og öll viðbótartiltektar-/frágangspör til að klára vinnuna.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-178">Confirm the put step and any additional pick/put pairs to complete the work.</span></span>

> [!NOTE]
> - <span data-ttu-id="7cc5e-179">Aðeins er hægt að flokka vinnu línur ef þær eru í röð.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-179">Work lines can be grouped only if they are in sequence.</span></span>
> - <span data-ttu-id="7cc5e-180">Eftirfarandi aðgerðir eru ekki studdar:</span><span class="sxs-lookup"><span data-stu-id="7cc5e-180">The following functionality isn't supported:</span></span>
>
>    - <span data-ttu-id="7cc5e-181">Vörur framleiðsluþyngdar.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-181">Catch-weight items.</span></span> <span data-ttu-id="7cc5e-182">Ef það eru einhverjar framleiðsluþyngdir í vvinnunni færðu villuboð áður en þú byrjar tiltekt.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-182">If there are any catch-weight items on the work, you receive an error message before you start to pick.</span></span>
>    - <span data-ttu-id="7cc5e-183">Einingatiltekt.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-183">Piece picking.</span></span>
>    - <span data-ttu-id="7cc5e-184">Vinnulínur sem hafa óunna endurnýjunarvinnu.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-184">Work lines that have unfinished replenishment work.</span></span>
>    - <span data-ttu-id="7cc5e-185">Umframtiltekt.</span><span class="sxs-lookup"><span data-stu-id="7cc5e-185">Over-picking.</span></span>
>    - <span data-ttu-id="7cc5e-186">Endurúthlutun með fyrir vöru</span><span class="sxs-lookup"><span data-stu-id="7cc5e-186">Short picking with item reallocation</span></span>
