---
title: Hólfaskipting vöruhúss
description: Þetta efni inniheldur upplýsingar um hólfaskiptingu vöruhúss. Hólfaskipting vöruhúss gerir þér kleift að sameina eftirspurn eftir vöru og mælieiningu frá pöntunum með stöðuna Pöntuð, Frátekin eða Sleppt. Slíkt aðstoðar stjórnendur vöruhúsa að skipuleggja betur tiltektarstaðsetningar áður en þeir sleppa pöntunum til vöruhússins og búa til tiltektarvinnu.
author: mirzaab
manager: tfehr
ms.date: 11/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSInventFixedLocation, WHSSlotDemandLocated, WHSSlotDemand, WHSSlotUOMTier, WHSSlotTemplate, WHSLocDirHint, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: fb39daba393944471ee5d412b1eb61754843926f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993754"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="63106-105">Hólfaskipting vöruhúss</span><span class="sxs-lookup"><span data-stu-id="63106-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="63106-106">Ýmsir eiginleikar fyrir hólfaskiptingu vöruhúss eru í boði til að aðstoða stjórnendur vöruhúsa að skipuleggja betur tiltektarstaðsetningar áður en þeir sleppa pöntunum til vöruhússins og búa til tiltektarvinnu.</span><span class="sxs-lookup"><span data-stu-id="63106-106">Several warehouse slotting features are available to help warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

<span data-ttu-id="63106-107">Eiginleikinn *Hólfaskipting vöruhúss* gerir þér kleift að sameina eftirspurn eftir vöru og mælieiningu frá pöntunum með stöðuna *Pöntuð*, *Frátekin* eða *Sleppt*.</span><span class="sxs-lookup"><span data-stu-id="63106-107">The *Warehouse slotting feature* lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="63106-108">Tilbúna eftirspurn er síðan hægt að nota á staðsetningar sem verða notaðar fyrir tiltekt miðað við magn, einingu, efnislegar víddir, fastar staðsetningar o.s.frv.</span><span class="sxs-lookup"><span data-stu-id="63106-108">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="63106-109">Þegar áætlunin um hólfaskiptingu er tilbúin er hægt að stofna áfyllingarvinnu til að færa rétt magn birgða í hverja staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="63106-109">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="63106-110">Eiginleikinn *Vöruhúsahólf fyrir flutningspantanir* heimilar stjórnendum vöruhúss að fylla á tiltektarstaðsetningar samkvæmt eftirspurn flutningspantana sem ekki er enn búið að losa úr vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="63106-110">The *Warehouse slotting for transfer orders* feature lets warehouse managers replenish picking locations, based on demand from transfer orders that aren't yet released to the warehouse.</span></span> <span data-ttu-id="63106-111">Slíkt tryggir að í tiltektarstaðsetningunum verði allar vörurnar sem þarf fyrir flutningspantanir þegar þær eru losaðar í vöruhús.</span><span class="sxs-lookup"><span data-stu-id="63106-111">It ensures that picking locations will include all the items that are required for the transfer orders after they are released to warehouse.</span></span> <span data-ttu-id="63106-112">Þessi eiginleiki krefst þess að eiginleikinn *Hólfaskipting vöruhúss* sé einnig virkjaður.</span><span class="sxs-lookup"><span data-stu-id="63106-112">This feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span>

<span data-ttu-id="63106-113">Eiginleikinn *Endurbætur á úthlutun hólfaskiptingar í vöruhúsi* bætir við valkosti fyrir sniðmátslínur sem eru notaðar af eiginleikanum *Hólfaskipting vöruhúss*.</span><span class="sxs-lookup"><span data-stu-id="63106-113">The *Warehouse slotting allocation enhancements* feature adds an option for the template lines that are used by the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="63106-114">Valkosturinn gerir kerfinu kleift að íhuga fyrirliggjandi lagerbirgðir á viðtökustað.</span><span class="sxs-lookup"><span data-stu-id="63106-114">The option enables the system to consider existing on-hand inventory at a target location.</span></span> <span data-ttu-id="63106-115">Þar af leiðandi kunna færri áfyllingar að vera búnar til fyrir hólf.</span><span class="sxs-lookup"><span data-stu-id="63106-115">Therefore, fewer replenishments might be generated for slotting.</span></span> <span data-ttu-id="63106-116">Eiginleikinn *Endurbætur á úthlutun hólfaskiptingar í vöruhúsi* krefst þess að eiginleikinn *Hólfaskipting vöruhúss* sé einnig virkjaður.</span><span class="sxs-lookup"><span data-stu-id="63106-116">The *Warehouse slotting allocation enhancements* feature requires that you also turn on the *Warehouse slotting feature* feature.</span></span> <span data-ttu-id="63106-117">Einnig er hægt að nota hann ásamt eiginleikanum *Vöruhúsahólf fyrir flutningspantanir*.</span><span class="sxs-lookup"><span data-stu-id="63106-117">It can optionally be used together with the *Warehouse slotting for transfer orders* feature.</span></span>

## <a name="turn-on-the-warehouse-slotting-features"></a><span data-ttu-id="63106-118">Kveikja á eiginleikum fyrir hólfaskiptingu vöruhúss</span><span class="sxs-lookup"><span data-stu-id="63106-118">Turn on the warehouse slotting features</span></span>

<span data-ttu-id="63106-119">Áður en hægt er að nota slíka eiginleika verður að vera kveikt á þeim í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="63106-119">Before you can use these features, they must be turned on in your system.</span></span> <span data-ttu-id="63106-120">Stjórnendur geta notað stillingar [eiginleikastjórnunar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikanna og kveikja á þeim ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="63106-120">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="63106-121">Kveikja skal á eftirfarandi eiginleikum eftir því sem þörf krefur:</span><span class="sxs-lookup"><span data-stu-id="63106-121">Turn on the following features as required:</span></span>

- <span data-ttu-id="63106-122">Hólfaröðunareiginleiki vöruhúss</span><span class="sxs-lookup"><span data-stu-id="63106-122">Warehouse slotting feature</span></span>
- <span data-ttu-id="63106-123">Vöruhúsahólf fyrir flutningspantanir</span><span class="sxs-lookup"><span data-stu-id="63106-123">Warehouse slotting for transfer orders</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="63106-124">Kveikja verður á eiginleikanum *Vöruhúsahólf fyrir flutningspantanir* áður en kveikt er á þessum eiginleika.</span><span class="sxs-lookup"><span data-stu-id="63106-124">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

- <span data-ttu-id="63106-125">Endurbætur á úthlutun hólfaskiptingar í vöruhúsi</span><span class="sxs-lookup"><span data-stu-id="63106-125">Warehouse slotting allocation enhancements</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="63106-126">Kveikja verður á eiginleikanum *Vöruhúsahólf fyrir flutningspantanir* áður en kveikt er á þessum eiginleika.</span><span class="sxs-lookup"><span data-stu-id="63106-126">The *Warehouse slotting feature* feature must be turned on before this feature.</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="63106-127">Setja upp hólfaskiptingu vöruhúss</span><span class="sxs-lookup"><span data-stu-id="63106-127">Set up warehouse slotting</span></span>

<span data-ttu-id="63106-128">Þú verður að setja upp eftirfarandi eiginleika í kerfinu til að hægt sé að nota hólfaskiptingu vöruhúss:</span><span class="sxs-lookup"><span data-stu-id="63106-128">To use warehouse slotting, you must set up the following elements in your system:</span></span>

- <span data-ttu-id="63106-129">Mælieiningarlög hólfaskiptingar</span><span class="sxs-lookup"><span data-stu-id="63106-129">Slotting unit of measure tiers</span></span>
- <span data-ttu-id="63106-130">Leiðbeiningarkóðar</span><span class="sxs-lookup"><span data-stu-id="63106-130">Directive codes</span></span>
- <span data-ttu-id="63106-131">Hólfaskiptingarsniðmát</span><span class="sxs-lookup"><span data-stu-id="63106-131">Slotting templates</span></span>
- <span data-ttu-id="63106-132">Staðsetningarleiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="63106-132">Location directives</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="63106-133">Búa til mælieiningarlag fyrir hólfaskiptingu</span><span class="sxs-lookup"><span data-stu-id="63106-133">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="63106-134">Mælieiningarlög gera kleift að flokka margar mælieiningar saman í þeim tilgangi að skipta niður í hólf.</span><span class="sxs-lookup"><span data-stu-id="63106-134">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="63106-135">Til dæmis, ef kassar í mörgum stærðum eru teknir af sama tiltektarsvæði kassa, er hægt að búa til eitt lag fyrir allar stærðirnar.</span><span class="sxs-lookup"><span data-stu-id="63106-135">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="63106-136">**Búa verður til línu fyrir hverja mælieiningu sem ætti að vera hluti af stiginu.**</span><span class="sxs-lookup"><span data-stu-id="63106-136">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="63106-137">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Áfylling \> Hólfaskiptieining fyrir mælieiningarlög**.</span><span class="sxs-lookup"><span data-stu-id="63106-137">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="63106-138">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="63106-138">Select **New**.</span></span>
1. <span data-ttu-id="63106-139">Stilla eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="63106-139">In the header, set the following values:</span></span>

    - <span data-ttu-id="63106-140">**Mælieiningarlag:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="63106-140">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="63106-141">**Lýsing:** *Hvert vörubretti með kössum*</span><span class="sxs-lookup"><span data-stu-id="63106-141">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="63106-142">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="63106-142">Select **Save**.</span></span>
1. <span data-ttu-id="63106-143">Á flýtiflipanum **Mælieiningar** velur þú **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="63106-143">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="63106-144">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="63106-144">On the new line, set the following values:</span></span>

    - <span data-ttu-id="63106-145">**Eining:** *Kassi*</span><span class="sxs-lookup"><span data-stu-id="63106-145">**Unit:** *Box*</span></span>
    - <span data-ttu-id="63106-146">**Lýsing:** Hafðu svæðið autt.</span><span class="sxs-lookup"><span data-stu-id="63106-146">**Description:** Leave this field blank.</span></span> <span data-ttu-id="63106-147">Þetta svæði er sjálfkrafa fyllt út um leið og breytingarnar eru vistaðar.</span><span class="sxs-lookup"><span data-stu-id="63106-147">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="63106-148">**Einingarflokkur:** *Magn*</span><span class="sxs-lookup"><span data-stu-id="63106-148">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="63106-149">Veldu **Ný** til að bæta annarri línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="63106-149">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="63106-150">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="63106-150">On the new line, set the following values:</span></span>

    - <span data-ttu-id="63106-151">**Prófhópur:** *ea*</span><span class="sxs-lookup"><span data-stu-id="63106-151">**Unit:** *ea*</span></span>
    - <span data-ttu-id="63106-152">**Lýsing:** Hafðu svæðið autt.</span><span class="sxs-lookup"><span data-stu-id="63106-152">**Description:** Leave this field blank.</span></span> <span data-ttu-id="63106-153">Þetta svæði er sjálfkrafa fyllt út um leið og breytingarnar eru vistaðar.</span><span class="sxs-lookup"><span data-stu-id="63106-153">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="63106-154">**Einingarflokkur:** *Magn*</span><span class="sxs-lookup"><span data-stu-id="63106-154">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="63106-155">Veldu **Ný** til að bæta þriðju línunni við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="63106-155">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="63106-156">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="63106-156">On the new line, set the following values:</span></span>

    - <span data-ttu-id="63106-157">**Eining:** *VÖRUBRETTI*</span><span class="sxs-lookup"><span data-stu-id="63106-157">**Unit:** *PL*</span></span>
    - <span data-ttu-id="63106-158">**Lýsing:** Hafðu svæðið autt.</span><span class="sxs-lookup"><span data-stu-id="63106-158">**Description:** Leave this field blank.</span></span> <span data-ttu-id="63106-159">Þetta svæði er sjálfkrafa fyllt út um leið og breytingarnar eru vistaðar.</span><span class="sxs-lookup"><span data-stu-id="63106-159">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="63106-160">**Einingarflokkur:** *Magn*</span><span class="sxs-lookup"><span data-stu-id="63106-160">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="63106-161">Veljið **Vista** til að vista lagið.</span><span class="sxs-lookup"><span data-stu-id="63106-161">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="63106-162">Búa til leiðbeiningarkóða fyrir hólfaskiptingu</span><span class="sxs-lookup"><span data-stu-id="63106-162">Create a directive code for slotting</span></span>

<span data-ttu-id="63106-163">Þú verður að velja leiðbeiningarkóða sem ætti að tengjast sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="63106-163">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="63106-164">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Leiðbeiningarkóðar**.</span><span class="sxs-lookup"><span data-stu-id="63106-164">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="63106-165">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="63106-165">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="63106-166">Í svæðinu **Leiðbeiningarkóði** skaltu slá inn *Hólfaskipting*.</span><span class="sxs-lookup"><span data-stu-id="63106-166">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="63106-167">Í svæðinu **Lýsing leiðbeiningar** skaltu slá inn *Hólfaskipting*.</span><span class="sxs-lookup"><span data-stu-id="63106-167">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="63106-168">Setja upp hólfaskiptingarsniðmát</span><span class="sxs-lookup"><span data-stu-id="63106-168">Set up slotting templates</span></span>

<span data-ttu-id="63106-169">Hvert hólfaskiptingarsniðmát stjórnar því hvernig birgðum er úthlutað á staðsetningar í tilteknu vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="63106-169">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="63106-170">Hvert sniðmát verður að innihalda línu fyrir hverja forskrift hólfaskiptingar.</span><span class="sxs-lookup"><span data-stu-id="63106-170">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="63106-171">Notaðu ferlin í þessum hluta til að setja upp hólfaskiptingarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="63106-171">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="63106-172">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Áfylling \> Hólfaskiptingarsniðmát**.</span><span class="sxs-lookup"><span data-stu-id="63106-172">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="63106-173">Veldu **Nýtt** til að búa til sniðmát.</span><span class="sxs-lookup"><span data-stu-id="63106-173">Select **New** to create a template.</span></span>

<span data-ttu-id="63106-174">Því næst verður þú að setja upp sniðmáthaus, forskriftir hólfaskiptingar og staðsetningarleiðbeiningar, eins og útskýrt er í eftirfarandi undirköflum.</span><span class="sxs-lookup"><span data-stu-id="63106-174">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span> <span data-ttu-id="63106-175">Uppsetning fyrir flutningspantanir líkist uppsetningu fyrir sölupantanir, en svæðið **Gerð eftirspurnar** er stillt á *Flutningspantanir* í staðinn fyrir *Sölupantanir*.</span><span class="sxs-lookup"><span data-stu-id="63106-175">The setup for slotting for transfer orders resembles the setup for slotting for sales orders, but the **Demand type** field is set *Transfer orders* instead of *Sales order*.</span></span>

#### <a name="set-up-the-header-for-a-sales-order-slotting-template"></a><span data-ttu-id="63106-176">Setja upp haus fyrir hólfasniðmát sölupöntunar</span><span class="sxs-lookup"><span data-stu-id="63106-176">Set up the header for a sales order slotting template</span></span>

1. <span data-ttu-id="63106-177">Stilltu eftirfarandi gildi í sniðmátshausnum:</span><span class="sxs-lookup"><span data-stu-id="63106-177">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="63106-178">**Hólfaskiptingarsniðmát:** _61_</span><span class="sxs-lookup"><span data-stu-id="63106-178">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="63106-179">**Lýsing:** _61_</span><span class="sxs-lookup"><span data-stu-id="63106-179">**Description:** _61_</span></span>
    - <span data-ttu-id="63106-180">**Gerð eftirspurnar:** *Sölupöntun*</span><span class="sxs-lookup"><span data-stu-id="63106-180">**Demand type:** *Sales order*</span></span>

        > [!NOTE]
        > <span data-ttu-id="63106-181">Eins og stendur eru *Sölupantanir* og *Flutningspantanir* einu gerðir eftirspurnar sem eru studdar.</span><span class="sxs-lookup"><span data-stu-id="63106-181">Currently, *Sales orders* and *Transfer orders* are the only demand types that are supported.</span></span> <span data-ttu-id="63106-182">Þú getur einungis valið *Flutningspantanir* ef kveikt er á eiginleikanum *Vöruhúsahólf fyrir flutningspantanir*.</span><span class="sxs-lookup"><span data-stu-id="63106-182">You can select *Transfer orders* only if the *Warehouse Slotting for transfer orders* feature is turned on.</span></span>

    - <span data-ttu-id="63106-183">**Eftirspurnarstefna:** _Pöntuð_</span><span class="sxs-lookup"><span data-stu-id="63106-183">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="63106-184">Eftirtalin gildi eru tiltæk á þessu svæði:</span><span class="sxs-lookup"><span data-stu-id="63106-184">The following values are available in this field:</span></span>

        - <span data-ttu-id="63106-185">**Pantað** – Allt pantað magn á sölupöntuninni skal telja sem eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="63106-185">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="63106-186">**Frátekið** – Aðeins magn af sölupöntunarlínu sem er frátekið (efnislega og pantað) ætti að teljast sem eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="63106-186">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>
        - <span data-ttu-id="63106-187">**Losað** – Losað magn skal flokka sem eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="63106-187">**Released** – The released quantity should be considered demand.</span></span>

    - <span data-ttu-id="63106-188">**Vöruhús:** _61_</span><span class="sxs-lookup"><span data-stu-id="63106-188">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="63106-189">**Leyfa bylgjueftirspurn að nota magn sem ekki er frátekið:** _Já_</span><span class="sxs-lookup"><span data-stu-id="63106-189">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="63106-190">Þú getur einnig tilgreint fyrirspurn til að þrengja umfang eftirspurnar sem er metin.</span><span class="sxs-lookup"><span data-stu-id="63106-190">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="63106-191">Settu upp forskriftir hólfaskiptingar fyrir hvert sniðmát</span><span class="sxs-lookup"><span data-stu-id="63106-191">Set up slotting specifications for each template</span></span>

<span data-ttu-id="63106-192">Fylgdu þessum skrefum fyrir hvert pöntunarsniðmát sem þú býrð til að bæta við línu fyrir hverja forskrift hólfaskiptingar.</span><span class="sxs-lookup"><span data-stu-id="63106-192">For each sales order template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="63106-193">Á flýtiflipanum **Upplýsingar um hólfaskiptingarsniðmát** velur þú **Nýtt** til að búa til nýja sniðmátslínu.</span><span class="sxs-lookup"><span data-stu-id="63106-193">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="63106-194">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="63106-194">On the new line, set the following values:</span></span>

    - <span data-ttu-id="63106-195">**Röð:** _1_</span><span class="sxs-lookup"><span data-stu-id="63106-195">**Sequence:** _1_</span></span>
    - <span data-ttu-id="63106-196">**Lýsing:** _Föst staðsetning_</span><span class="sxs-lookup"><span data-stu-id="63106-196">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="63106-197">**Lágmarksmagn:** _1_</span><span class="sxs-lookup"><span data-stu-id="63106-197">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="63106-198">Þetta svæði skilgreinir áskilið lágmarksmagn eftirspurnar fyrir línuna.</span><span class="sxs-lookup"><span data-stu-id="63106-198">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="63106-199">**Hámarksmagn:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="63106-199">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="63106-200">Þetta svæði skilgreinir áskilið hámarksmagn eftirspurnar sem er gilt fyrir línuna.</span><span class="sxs-lookup"><span data-stu-id="63106-200">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="63106-201">**Eining:** Hafðu þetta svæði autt.</span><span class="sxs-lookup"><span data-stu-id="63106-201">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="63106-202">Þetta svæði skilgreinir mælieininguna sem lágmarks- og hámarksmagnið vísa til.</span><span class="sxs-lookup"><span data-stu-id="63106-202">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="63106-203">**Mælieiningarlag:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="63106-203">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="63106-204">Þetta svæði skilgreinir mælieiningar eftirspurnar sem gilda fyrir línuna.</span><span class="sxs-lookup"><span data-stu-id="63106-204">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="63106-205">(Frekari upplýsingar er að finna í hlutanum [Uppsetning á mælieiningarlögum fyrir hólfaskiptingu](#unit-tiers) fyrr í þessu efnisatriði).</span><span class="sxs-lookup"><span data-stu-id="63106-205">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="63106-206">**Skilyrði úthlutunar hólfa:** _Taka mið af magni_</span><span class="sxs-lookup"><span data-stu-id="63106-206">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="63106-207">Eftirtalin gildi eru tiltæk á þessu svæði:</span><span class="sxs-lookup"><span data-stu-id="63106-207">The following values are available in this field:</span></span>

        - <span data-ttu-id="63106-208">**Gera ráð fyrir að staðsetning sé tóm** – Þetta kerfi ætti að gera ráð fyrir að allar staðsetningar á tiltektarsvæðinu séu tómar og ætti ekki að athuga áðurnefndar staðsetningar fyrir birgðir.</span><span class="sxs-lookup"><span data-stu-id="63106-208">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="63106-209">**Gera ráð fyrir magni á staðsetningu** – Kerfið ætti að athuga staðsetningu á tiltektarsvæðinu fyrir birgðir og ætti að sleppa öllum staðsetningum sem eru ekki tómar.</span><span class="sxs-lookup"><span data-stu-id="63106-209">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>
        - <span data-ttu-id="63106-210">**Íhuga magn í birgðum** – kerfið ætti að athuga hvort einhver viðtökustaður innihaldi magn sem er ekki frátekið fyrir vöruna í eftirspurnarlínunni.</span><span class="sxs-lookup"><span data-stu-id="63106-210">**Consider on-hand** – The system should check whether any target location contains unreserved quantities for the item on the demand line.</span></span> <span data-ttu-id="63106-211">Þegar magnið er nægilega mikið til að uppfylla að minnsta kosti eina einingu eftirspurnarlínunnar, er færsla áætlunar fyrir hólfaskiptingu færð niður í tiltækt magn.</span><span class="sxs-lookup"><span data-stu-id="63106-211">If the quantity is large enough to satisfy at least one unit of the demand line, the generated slotting plan record is reduced by the available amount.</span></span> <span data-ttu-id="63106-212">Þegar eftirspurn er t.d. 10 tilvik og eitt tilvik er á lager verður fundin eftirspurn í níu tilvikum.</span><span class="sxs-lookup"><span data-stu-id="63106-212">For example, if the demand is 10 cases, and one case is on hand, the located demand will be nine cases.</span></span> <span data-ttu-id="63106-213">Þegar eftirspurn er 10 tilvik og hvert þeirra er á lager verður fundin eftirspurn í 10 tilvikum.</span><span class="sxs-lookup"><span data-stu-id="63106-213">If the demand is 10 cases, and one each is on hand, the located demand will be 10 cases.</span></span> <span data-ttu-id="63106-214">Þetta gildi er aðeins tiltækt þegar kveikt er á eiginleikanum *Endurbætur á úthlutun hólfaskiptingar í vöruhúsi*.</span><span class="sxs-lookup"><span data-stu-id="63106-214">This value is available only when the *Warehouse slotting allocation enhancements* feature is turned on.</span></span>

    - <span data-ttu-id="63106-215">**Leiðbeiningarkóði:** _Hólfaskipting_</span><span class="sxs-lookup"><span data-stu-id="63106-215">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="63106-216">Þetta svæði skilgreinir staðsetningarleiðbeiningarnar sem eru notaðar til að finna tiltektarstaðsetningu áfyllingarvinnunnar.</span><span class="sxs-lookup"><span data-stu-id="63106-216">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="63106-217">**Yfirflæði á staðsetningu:** Hafðu þetta svæði autt.</span><span class="sxs-lookup"><span data-stu-id="63106-217">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="63106-218">Þetta svæði skilgreinir staðsetningu sem birgðir eru settar ef staðsetning finnst ekki fyrir magnið við vinnslu línunnar.</span><span class="sxs-lookup"><span data-stu-id="63106-218">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="63106-219">**Leyfa stöðvun:** _já_</span><span class="sxs-lookup"><span data-stu-id="63106-219">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="63106-220">Þegar þessi valkostur er stilltur á *Já*, ef ekki er hægt að skipta einhverri eftirspurn í hólf, verður búin til birgðahreyfing til að taka birgðum úr staðsetningum þar sem engar birgðir eru, en engu var skipt niður í hólf.</span><span class="sxs-lookup"><span data-stu-id="63106-220">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="63106-221">Sniðmátið er síðan keyrt aftur.</span><span class="sxs-lookup"><span data-stu-id="63106-221">The template is then run again.</span></span> <span data-ttu-id="63106-222">Í þetta sinn hunsar það birgðir í staðsetningum.</span><span class="sxs-lookup"><span data-stu-id="63106-222">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="63106-223">Þessi eiginleiki virkar best þegar svæðið **Úthluta skilyrðum fyrir hólf** er stillt á _Taka mið af magni_.</span><span class="sxs-lookup"><span data-stu-id="63106-223">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="63106-224">**Notkun fastrar staðsetningar:** _Aðeins fastar staðsetningar fyrir afurðina_</span><span class="sxs-lookup"><span data-stu-id="63106-224">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="63106-225">Eftirtalin gildi eru tiltæk á þessu svæði:</span><span class="sxs-lookup"><span data-stu-id="63106-225">The following values are available in this field:</span></span>

        - <span data-ttu-id="63106-226">**Fastar og lausar staðsetningar** – Ekki ætti að takmarka kerfið við að nota aðeins fastar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="63106-226">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="63106-227">**Aðeins fastar staðsetningar fyrir afurðina** – Kerfið ætti aðeins að skipta niður í hólf á staðsetningar sem eru fastar staðsetningar fyrir afurðina.</span><span class="sxs-lookup"><span data-stu-id="63106-227">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="63106-228">**Aðeins fastar staðsetningar fyrir afurðarafbrigðið** – Kerfið ætti aðeins að skipta niður í hólf á staðsetningar sem eru fastar staðsetningar fyrir afurðarafbrigðið.</span><span class="sxs-lookup"><span data-stu-id="63106-228">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

> [!NOTE]
> <span data-ttu-id="63106-229">Ef hólfasniðmátið inniheldur að minnsta kosti eina línu þar sem svæðið **Úthluta skilyrðum fyrir hólf** er stillt á *Íhuga magn í birgðum* er yfirflæði ekki lengur leyft fyrir neina línu í sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="63106-229">If the slotting template contains at least one line where the **Assign slot criteria** field is set to *Consider on-hand*, let-ups are no longer allowed for any line in the template.</span></span>

1. <span data-ttu-id="63106-230">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="63106-230">Select **Save**.</span></span>
1. <span data-ttu-id="63106-231">Veldu **Ný** til að búa til aðra sniðmátslínu.</span><span class="sxs-lookup"><span data-stu-id="63106-231">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="63106-232">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="63106-232">On the new line, set the following values:</span></span>

    - <span data-ttu-id="63106-233">**Röð:** _2_</span><span class="sxs-lookup"><span data-stu-id="63106-233">**Sequence:** _2_</span></span>
    - <span data-ttu-id="63106-234">**Lýsing:** _Annað_</span><span class="sxs-lookup"><span data-stu-id="63106-234">**Description:** _Other_</span></span>
    - <span data-ttu-id="63106-235">**Lágmarksmagn:** _1_</span><span class="sxs-lookup"><span data-stu-id="63106-235">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="63106-236">**Hámarksmagn:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="63106-236">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="63106-237">**Eining:** Hafðu þetta svæði autt.</span><span class="sxs-lookup"><span data-stu-id="63106-237">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="63106-238">**Mælieiningarlag:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="63106-238">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="63106-239">**Skilyrði úthlutunar hólfa:** _Taka mið af magni_</span><span class="sxs-lookup"><span data-stu-id="63106-239">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="63106-240">**Leiðbeiningarkóði:** _Hólfaskipting_</span><span class="sxs-lookup"><span data-stu-id="63106-240">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="63106-241">**Yfirflæði á staðsetningu:** Hafðu þetta svæði autt.</span><span class="sxs-lookup"><span data-stu-id="63106-241">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="63106-242">**Leyfa stöðvun:** _já_</span><span class="sxs-lookup"><span data-stu-id="63106-242">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="63106-243">**Nota fastar staðsetningar:** _Fastar og lausar staðsetningar_</span><span class="sxs-lookup"><span data-stu-id="63106-243">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="63106-244">Í fyrirspurninni fyrir aðra línuna tilgreinir þú skilyrðin sem eru notuð til að ákvarða hvaða staðsetningar eftirspurnar fyrir umrædda línu er hægt að skipa í hólf.</span><span class="sxs-lookup"><span data-stu-id="63106-244">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="63106-245">Veldu línuna þar sem svæðið **Runa** er stillt á *2*.</span><span class="sxs-lookup"><span data-stu-id="63106-245">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="63106-246">Veldu **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="63106-246">Select **Edit query**.</span></span>
1. <span data-ttu-id="63106-247">Á flipanum **Svið** velur þú **Bæta við** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="63106-247">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="63106-248">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="63106-248">On the new line, set the following values:</span></span>

    - <span data-ttu-id="63106-249">**Tafla:** *Staðir*</span><span class="sxs-lookup"><span data-stu-id="63106-249">**Table:** *Locations*</span></span>
    - <span data-ttu-id="63106-250">**Afleidd tafla:** *Staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="63106-250">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="63106-251">**Reitur:** *Auðkenni forstillingar staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="63106-251">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="63106-252">**Skilyrði:** *Tiltekt-06* (Veldu tvöfalt plúsmerki \[**++**\] á svæðinu til að stækka listann, og veldu síðan *Tiltekt-06* - *Tiltektarsvæði 6*.)</span><span class="sxs-lookup"><span data-stu-id="63106-252">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="63106-253">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="63106-253">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="63106-254">Setja upp staðsetningarleiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="63106-254">Set up location directives</span></span>

<span data-ttu-id="63106-255">Setja þarf upp að minnsta kosti eina staðsetningarleiðbeiningar til að styðja tiltekt við hólfaskiptingu.</span><span class="sxs-lookup"><span data-stu-id="63106-255">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="63106-256">Notaðu verklagsreglurnar í þessum kafla til að setja upp nýjar *staðsetningarleiðbeiningar fyrir áfyllingu* fyrir tiltekt við hólfaskiptingu.</span><span class="sxs-lookup"><span data-stu-id="63106-256">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="63106-257">Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.</span><span class="sxs-lookup"><span data-stu-id="63106-257">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="63106-258">Í svæðinu **Gerð verkbeiðni** í vinstri glugganum velur þú *Áfylling*.</span><span class="sxs-lookup"><span data-stu-id="63106-258">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="63106-259">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="63106-259">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="63106-260">Í haus nýju staðsetningarleiðbeininganna á svæðinu **Heiti** slærðu inn *61 Tiltekt við hólfaskiptingu*.</span><span class="sxs-lookup"><span data-stu-id="63106-260">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>
1. <span data-ttu-id="63106-261">Samþykktu sjálfgildið í svæðinu **Raðnúmer**.</span><span class="sxs-lookup"><span data-stu-id="63106-261">In the **Sequence number** field, accept the default value.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="63106-262">Grunnstilling flýtiflipans Staðsetningarleiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="63106-262">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="63106-263">Stilltu eftirfarandi gildi á flýtiflipanum **staðsetningarleiðbeiningar**.</span><span class="sxs-lookup"><span data-stu-id="63106-263">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="63106-264">Samþykktu sjálfgildin fyrir öll önnur svæði.</span><span class="sxs-lookup"><span data-stu-id="63106-264">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="63106-265">**Tegund vinnu:** _Tínsla_</span><span class="sxs-lookup"><span data-stu-id="63106-265">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="63106-266">**Svæði:** _6_</span><span class="sxs-lookup"><span data-stu-id="63106-266">**Site:** _6_</span></span>
    - <span data-ttu-id="63106-267">**Vöruhús:** _61_</span><span class="sxs-lookup"><span data-stu-id="63106-267">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="63106-268">**Leiðbeiningarkóði:** _Hólfaskipting_</span><span class="sxs-lookup"><span data-stu-id="63106-268">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="63106-269">Veldu **Vista** til að gera flýtiflipann **Línur** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="63106-269">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="63106-270">Grunnstilling flýtiflipans Línur</span><span class="sxs-lookup"><span data-stu-id="63106-270">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="63106-271">Á flýtiflipanum **Línur** velur þú **Ný** til að búa til línu.</span><span class="sxs-lookup"><span data-stu-id="63106-271">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="63106-272">Stilltu eftirfarandi gildi á nýju línunni.</span><span class="sxs-lookup"><span data-stu-id="63106-272">On the new line, set the following values.</span></span>

    - <span data-ttu-id="63106-273">**Frá-magn:** _0_</span><span class="sxs-lookup"><span data-stu-id="63106-273">**From quantity:** _0_</span></span>
    - <span data-ttu-id="63106-274">**Til magn:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="63106-274">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="63106-275">Samþykkið sjálfgefin gildi fyrir reitina sem eftir eru.</span><span class="sxs-lookup"><span data-stu-id="63106-275">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="63106-276">Veldu **Vista** til að gera flýtiflipann **Aðgerðir í staðsetningarleiðbeiningum** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="63106-276">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="63106-277">Grunnstilling flýtiflipans Aðgerðir í staðsetningarleiðbeiningum</span><span class="sxs-lookup"><span data-stu-id="63106-277">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="63106-278">Á flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** velur þú **Ný** til að búa til línu.</span><span class="sxs-lookup"><span data-stu-id="63106-278">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="63106-279">Stilltu eftirfarandi gildi á nýju línunni.</span><span class="sxs-lookup"><span data-stu-id="63106-279">On the new line, set the following values.</span></span> <span data-ttu-id="63106-280">Samþykktu sjálfgildin fyrir öll önnur svæði.</span><span class="sxs-lookup"><span data-stu-id="63106-280">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="63106-281">**Raðnúmer:** Samþykkja sjálfgildið.</span><span class="sxs-lookup"><span data-stu-id="63106-281">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="63106-282">**Heiti:** _Magn_</span><span class="sxs-lookup"><span data-stu-id="63106-282">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="63106-283">**Áætlun:** _Engin_</span><span class="sxs-lookup"><span data-stu-id="63106-283">**Strategy:** _None_</span></span>

1. <span data-ttu-id="63106-284">Samþykkið sjálfgefin gildi fyrir reitina sem eftir eru.</span><span class="sxs-lookup"><span data-stu-id="63106-284">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="63106-285">Veldu **Vista** til að gera hnappinn **Breyta fyrirspurn** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="63106-285">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="63106-286">Breyta fyrirspurn</span><span class="sxs-lookup"><span data-stu-id="63106-286">Edit the query</span></span>

1. <span data-ttu-id="63106-287">Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="63106-287">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="63106-288">Á flipanum **Svið** velur þú **Bæta við** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="63106-288">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="63106-289">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="63106-289">On the new line, set the following values:</span></span>

    - <span data-ttu-id="63106-290">**Tafla:** *Staðir*</span><span class="sxs-lookup"><span data-stu-id="63106-290">**Table:** *Locations*</span></span>
    - <span data-ttu-id="63106-291">**Afleidd tafla:** *Staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="63106-291">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="63106-292">**Reitur::** *Auðkenni svæðis*</span><span class="sxs-lookup"><span data-stu-id="63106-292">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="63106-293">**Skilyrði:** *Magn* (Veldu tvöfalt plúsmerki \[**++**\] á svæðinu til að stækka listann, og veldu síðan *Magn*).</span><span class="sxs-lookup"><span data-stu-id="63106-293">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="63106-294">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="63106-294">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="63106-295">Aðstæður</span><span class="sxs-lookup"><span data-stu-id="63106-295">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="63106-296">Setja upp aðstæður</span><span class="sxs-lookup"><span data-stu-id="63106-296">Set up the scenario</span></span>

<span data-ttu-id="63106-297">Notaðu innbyggðu sýnigögnin fyrir þessar aðstæður og búðu til skrárnar sem lýst er í þessum hluta.</span><span class="sxs-lookup"><span data-stu-id="63106-297">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="63106-298">Nota USMF-sýnigögn</span><span class="sxs-lookup"><span data-stu-id="63106-298">Use the USMF sample data</span></span>

<span data-ttu-id="63106-299">Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind hér verður þú að vera á kerfi þar sem venjuleg [sýnigögn](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er sett upp.</span><span class="sxs-lookup"><span data-stu-id="63106-299">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="63106-300">Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.</span><span class="sxs-lookup"><span data-stu-id="63106-300">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="63106-301">Búa til eftirspurn</span><span class="sxs-lookup"><span data-stu-id="63106-301">Create demand</span></span>

<span data-ttu-id="63106-302">Fylgdu eftirfarandi skrefum til að búa til eftirspurn sem verður notuð við hólfaskiptingu.</span><span class="sxs-lookup"><span data-stu-id="63106-302">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="63106-303">Opnið **Sala og markaðssetning \> Sölupantanir \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="63106-303">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="63106-304">Smellið á **Nýtt** til að stofna nýja sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="63106-304">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="63106-305">IÍ svarglugganum **Búa til sölupöntun** í svæðinu **Viðskiptavinalykill** skaltu velja _US-007_.</span><span class="sxs-lookup"><span data-stu-id="63106-305">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="63106-306">Í reitnum **Vöruhús** skal velja _61_.</span><span class="sxs-lookup"><span data-stu-id="63106-306">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="63106-307">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="63106-307">Select **OK**.</span></span>
1. <span data-ttu-id="63106-308">Ný sölupöntun opnast.</span><span class="sxs-lookup"><span data-stu-id="63106-308">The new sales order is opened.</span></span> <span data-ttu-id="63106-309">Hún inniheldur tóma línu á flýtiflipanum **Sölupöntunarlína**.</span><span class="sxs-lookup"><span data-stu-id="63106-309">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="63106-310">Stilltu eftirfarandi gildi á þessari línu:</span><span class="sxs-lookup"><span data-stu-id="63106-310">On this line, set the following values:</span></span>

    - <span data-ttu-id="63106-311">**Vara:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="63106-311">**Item:** _L0101_</span></span>
    - <span data-ttu-id="63106-312">**Magn:** _20_</span><span class="sxs-lookup"><span data-stu-id="63106-312">**Quantity:** _20_</span></span>

1. <span data-ttu-id="63106-313">Veldu **Bæta við línu** til að bæta við nýrri línu og stilltu eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="63106-313">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="63106-314">**Vara:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="63106-314">**Item:** _T0100_</span></span>
    - <span data-ttu-id="63106-315">**Magn:** _8_</span><span class="sxs-lookup"><span data-stu-id="63106-315">**Quantity:** _8_</span></span>

1. <span data-ttu-id="63106-316">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="63106-316">Select **Save**.</span></span>
1. <span data-ttu-id="63106-317">Veldu **Nýtt** til að búa til aðra sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="63106-317">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="63106-318">IÍ svarglugganum **Búa til sölupöntun** í svæðinu **Viðskiptavinalykill** skaltu velja _US-008_.</span><span class="sxs-lookup"><span data-stu-id="63106-318">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="63106-319">Í reitnum **Vöruhús** skal velja _61_.</span><span class="sxs-lookup"><span data-stu-id="63106-319">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="63106-320">Ný sölupöntun opnast.</span><span class="sxs-lookup"><span data-stu-id="63106-320">The new sales order is opened.</span></span> <span data-ttu-id="63106-321">Hún inniheldur tóma línu á flýtiflipanum **Sölupöntunarlína**.</span><span class="sxs-lookup"><span data-stu-id="63106-321">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="63106-322">Stilltu eftirfarandi gildi á þessari línu:</span><span class="sxs-lookup"><span data-stu-id="63106-322">On this line, set the following values:</span></span>

    - <span data-ttu-id="63106-323">**Vara:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="63106-323">**Item:** _T0100_</span></span>
    - <span data-ttu-id="63106-324">**Magn:** _1_</span><span class="sxs-lookup"><span data-stu-id="63106-324">**Quantity:** _1_</span></span>

1. <span data-ttu-id="63106-325">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="63106-325">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="63106-326">Handleiðsla í gegnum hefðbundnar aðstæður við hólfaskiptingu</span><span class="sxs-lookup"><span data-stu-id="63106-326">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="63106-327">Þegar öll skilyrði eru uppfyllt, eins og lýst er í fyrri hlutanum, ertu tilbúinn að prófa eiginleikann með því að vinna í gegnum hverja æfingu í þessum kafla.</span><span class="sxs-lookup"><span data-stu-id="63106-327">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="63106-328">Búa til eftirspurn</span><span class="sxs-lookup"><span data-stu-id="63106-328">Generate demand</span></span>

1. <span data-ttu-id="63106-329">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Áfylling \> Hólfaskiptingarsniðmát** og veldu hólfaskiptingarsniðmátið sem þú bjóst til áður.</span><span class="sxs-lookup"><span data-stu-id="63106-329">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="63106-330">Á aðgerðasvæðinu skal velja **Búa til eftirspurn**.</span><span class="sxs-lookup"><span data-stu-id="63106-330">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="63106-331">Þessi skipun metur alla eftirspurn sem er í kerfinu og samsvarar fyrirspurninni um hólfaskiptingarsniðmátið.</span><span class="sxs-lookup"><span data-stu-id="63106-331">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="63106-332">Heildareftirspurn yfir allar pantanir er síðan sameinaður í eina línu fyrir hvert magn/mælieining.</span><span class="sxs-lookup"><span data-stu-id="63106-332">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="63106-333">Upplýsingaboð birtast þegar ferlið er fullklárað.</span><span class="sxs-lookup"><span data-stu-id="63106-333">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="63106-334">Eftirspurn eftir hólfaskiptingu</span><span class="sxs-lookup"><span data-stu-id="63106-334">Slotting demand</span></span>

<span data-ttu-id="63106-335">*Eftirspurn eftir hólfaskiptingu* sýnir niðurstöður myndunar eftirspurnar miðað við uppsetningu hólfaskiptingarsniðmátsins.</span><span class="sxs-lookup"><span data-stu-id="63106-335">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="63106-336">Á aðgerðarsvæðinu velur þú **Eftirspurn eftir hólfaskiptingu** til að skoða niðurstöður skipunarinnar **Búa til eftirspurn**.</span><span class="sxs-lookup"><span data-stu-id="63106-336">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="63106-337">Hægt er að breyta línunum í eftirspurn eftir hólfaskiptingu.</span><span class="sxs-lookup"><span data-stu-id="63106-337">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="63106-338">Þú getur eytt línu, bætt við nýrri línu eða breytt upplýsingum um línuna.</span><span class="sxs-lookup"><span data-stu-id="63106-338">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="63106-339">Þú getur breytt eftirspurn handvirkt, eða þú getur flutt hana inn frá utanaðkomandi kerfi með gagnastjórnun.</span><span class="sxs-lookup"><span data-stu-id="63106-339">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="63106-340">Allt efni í eftirspurn eftir hólfaskiptingu er notað í næsta skrefi, óháð því hvaðan hún kom.</span><span class="sxs-lookup"><span data-stu-id="63106-340">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="63106-341">Finna eftirspurn</span><span class="sxs-lookup"><span data-stu-id="63106-341">Locate demand</span></span>

<span data-ttu-id="63106-342">Eftir að eftirspurn hefur verið mynduð verður þú að nota skipunina **Finna eftirspurn** til að búa til *áætlunina um hólfaskiptingu*.</span><span class="sxs-lookup"><span data-stu-id="63106-342">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="63106-343">Á aðgerðasvæðinu skal velja **Finna eftirspurn**.</span><span class="sxs-lookup"><span data-stu-id="63106-343">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="63106-344">Hólfaskiptingarferlið er keyrt.</span><span class="sxs-lookup"><span data-stu-id="63106-344">The slotting process runs.</span></span> <span data-ttu-id="63106-345">Upplýsingaboð birtast þegar ferlið er fullklárað.</span><span class="sxs-lookup"><span data-stu-id="63106-345">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="63106-346">Hólfaskiptingaráætlun</span><span class="sxs-lookup"><span data-stu-id="63106-346">Slotting plan</span></span>

<span data-ttu-id="63106-347">Áætlunin fyrir hólfaskiptingu sýnir staðsetningu sem hverri vöru/magni var úthlutað, hvort yfirflæði var notað, hvort vinnustöðvun var búin til og sniðmátalínan sem var notuð.</span><span class="sxs-lookup"><span data-stu-id="63106-347">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="63106-348">*Eftirspurn sem ekki var hægt að skipa í hólf er auðkennd með rauðu.*</span><span class="sxs-lookup"><span data-stu-id="63106-348">*Any demand that could not be slotted is highlighted in red.*</span></span>

- <span data-ttu-id="63106-349">Á aðgerðarsvæðinu velur þú **Áætlun fyrir hólfaskiptingu** til að skoða niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="63106-349">On the Action Pane, select **Slotting plan** to view the results.</span></span>

> [!NOTE]
> - <span data-ttu-id="63106-350">Ferlin **Búa til eftirspurn**, **Finna eftirspurn** og **Keyra áfyllingu** ferli eru nú keyrð í sandkassa.</span><span class="sxs-lookup"><span data-stu-id="63106-350">The **Generate demand**, **Locate demand**, and **Run replenishment** processes are now run in a sandbox.</span></span> <span data-ttu-id="63106-351">(Þessir ferlar eru tiltækir á aðgerðasvæðinu á síðunni **Hólfasniðmát**.)</span><span class="sxs-lookup"><span data-stu-id="63106-351">(These processes are available from the Action Pane on the **Slotting templates** page.)</span></span>
> - <span data-ttu-id="63106-352">Ferlin **Búa til eftirspurn**, **Finna eftirspurn** og **Keyra áfyllingu** ferli eru læst til að tryggja að ekki sé hægt að virkja þau samtímis.</span><span class="sxs-lookup"><span data-stu-id="63106-352">The **Generate demand**, **Locate demand**, and **Run replenishment** processes have a lock to ensure that they can't be triggered at the same time.</span></span> <span data-ttu-id="63106-353">Að öðrum kosti kann gögnunum sem eru notuð að vera eytt.</span><span class="sxs-lookup"><span data-stu-id="63106-353">Otherwise, the data that is used could be deleted.</span></span>
> - <span data-ttu-id="63106-354">Ferlin **Búa til eftirspurn** og **Finna eftirspurn** sýna viðvörun ef keyrslan myndar ekki færslur eða ef upplýsingar vantar um færslurnar.</span><span class="sxs-lookup"><span data-stu-id="63106-354">The **Generate demand** and **Locate demand** processes show a warning if the run didn't generate records, or if the records are missing information.</span></span>
> - <span data-ttu-id="63106-355">Þegar þú velur **Hólfaáætlun** birtast hnapparnir **Nýtt**, **Breyta** eða **Eyða** á aðgerðasvæðinu vegna þess að ekki er hægt að gera breytingar á gagnagjafanum.</span><span class="sxs-lookup"><span data-stu-id="63106-355">When you select **Slotting plan**, the page doesn't have **New**, **Edit**, or **Delete** buttons on the Action Pane, because the data source can't be edited.</span></span>
> - <span data-ttu-id="63106-356">Þegar þú smellir á **Keyra áfyllingu** villuleitar kerfið í völdum hólfasniðmátum og ferlum.</span><span class="sxs-lookup"><span data-stu-id="63106-356">When you select **Run replenishment**, the system validates the selected slot template and processes.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="63106-357">Stofna áfyllingu</span><span class="sxs-lookup"><span data-stu-id="63106-357">Create replenishment</span></span>

<span data-ttu-id="63106-358">Þegar áætlun fyrir hólfaskiptingu hefur verið búin til verður þú að búa til *áfyllingarvinnu* miðað við áætlunina.</span><span class="sxs-lookup"><span data-stu-id="63106-358">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="63106-359">Á aðgerðasvæðinu skal velja **Keyra áfyllingu**.</span><span class="sxs-lookup"><span data-stu-id="63106-359">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="63106-360">Upplýsingaboð birtast þegar ferlið er fullklárað.</span><span class="sxs-lookup"><span data-stu-id="63106-360">An informational message appears when the process is completed.</span></span> <span data-ttu-id="63106-361">Þessi skilaboð gefa til kynna fjölda hausa sem voru búnir til fyrir smíðakenni vinnu.</span><span class="sxs-lookup"><span data-stu-id="63106-361">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="63106-362">Staðsetningarleiðbeiningar sem notaðar verða eru auðkenndar út frá leiðbeiningarkóðanum sem er tilgreindur á hverri sniðmátslínu.</span><span class="sxs-lookup"><span data-stu-id="63106-362">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="63106-363">Ábendingar</span><span class="sxs-lookup"><span data-stu-id="63106-363">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="63106-364">Setja upp sjálfvirka hólfaskiptingu</span><span class="sxs-lookup"><span data-stu-id="63106-364">Set up automatic slotting</span></span>

<span data-ttu-id="63106-365">Eftir að allir nauðsynlegir þættir eru til staðar geturðu sett upp hólfaskiptingu til að keyra sjálfkrafa með því að fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="63106-365">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="63106-366">Opnaðu **Vöruhúsakerfi \> Áfylling \> Keyra hólfaskiptingu**.</span><span class="sxs-lookup"><span data-stu-id="63106-366">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="63106-367">Tilgreindu skref hólfaskiptingar sem á að keyra.</span><span class="sxs-lookup"><span data-stu-id="63106-367">Specify the slotting steps to run.</span></span> <span data-ttu-id="63106-368">Veldu eitt eða fleiri af eftirfarandi skrefum hólfaskiptingar:</span><span class="sxs-lookup"><span data-stu-id="63106-368">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="63106-369">Búa til eftirspurn</span><span class="sxs-lookup"><span data-stu-id="63106-369">Generate demand</span></span>
    - <span data-ttu-id="63106-370">Finna eftirspurn</span><span class="sxs-lookup"><span data-stu-id="63106-370">Locate demand</span></span>
    - <span data-ttu-id="63106-371">Stofna áfyllingarvinnu</span><span class="sxs-lookup"><span data-stu-id="63106-371">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="63106-372">Skrefin við hólfaskiptingu eru samfelld.</span><span class="sxs-lookup"><span data-stu-id="63106-372">The slotting steps are progressive.</span></span> <span data-ttu-id="63106-373">Ef þú vilt velja *Finna eftirspurn* verður þú fyrst að velja *Búa til eftirspurn*.</span><span class="sxs-lookup"><span data-stu-id="63106-373">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="63106-374">Tilgreindu hólfaskiptingarsniðmátið sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="63106-374">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="63106-375">Stilltu endurtekninguna til að keyra sjálfkrafa ef þú vilt.</span><span class="sxs-lookup"><span data-stu-id="63106-375">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="63106-376">Þegar aðstæður eru æfðar skal **ekki** setja upp sjálfvirka hólfaskiptingu.</span><span class="sxs-lookup"><span data-stu-id="63106-376">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
