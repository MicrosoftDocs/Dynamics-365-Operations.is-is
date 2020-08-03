---
title: Hólfaskipting vöruhúss
description: Þetta efni inniheldur upplýsingar um hólfaskiptingu vöruhúss. Hólfaskipting vöruhúss gerir þér kleift að sameina eftirspurn eftir vöru og mælieiningu frá pöntunum með stöðuna Pöntuð, Frátekin eða Sleppt. Slíkt aðstoðar stjórnendur vöruhúsa að skipuleggja betur tiltektarstaðsetningar áður en þeir sleppa pöntunum til vöruhússins og búa til tiltektarvinnu.
author: mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: f6764f8bc082962af37d4775b6fe53d8704658eb
ms.sourcegitcommit: f64fce03ec52f844b05a9e8cac286cb201385002
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/16/2020
ms.locfileid: "3597459"
---
# <a name="warehouse-slotting"></a><span data-ttu-id="d7066-105">Hólfaskipting vöruhúss</span><span class="sxs-lookup"><span data-stu-id="d7066-105">Warehouse slotting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d7066-106">Hólfaskipting vöruhúss gerir þér kleift að sameina eftirspurn eftir vöru og mælieiningu frá pöntunum með stöðuna *Pöntuð*, *Frátekin* eða *Sleppt*.</span><span class="sxs-lookup"><span data-stu-id="d7066-106">Warehouse slotting lets you consolidate demand by item and unit of measure from orders that have a status of *Ordered*, *Reserved*, or *Released*.</span></span> <span data-ttu-id="d7066-107">Tilbúna eftirspurn er síðan hægt að nota á staðsetningar sem verða notaðar fyrir tiltekt miðað við magn, einingu, efnislegar víddir, fastar staðsetningar o.s.frv.</span><span class="sxs-lookup"><span data-stu-id="d7066-107">Generated demand can then be applied to locations that will be used for picking, based on quantity, unit, physical dimensions, fixed locations, and more.</span></span> <span data-ttu-id="d7066-108">Þegar áætlunin um hólfaskiptingu er tilbúin er hægt að stofna áfyllingarvinnu til að færa rétt magn birgða í hverja staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="d7066-108">After the slotting plan has been established, replenishment work can be created to bring the appropriate amount of inventory to each location.</span></span>

<span data-ttu-id="d7066-109">Þessi eiginleiki aðstoðar stjórnendur vöruhúsa að skipuleggja betur tiltektarstaðsetningar áður en þeir sleppa pöntunum til vöruhússins og búa til tiltektarvinnu.</span><span class="sxs-lookup"><span data-stu-id="d7066-109">This functionality helps warehouse managers intelligently plan picking locations before they release orders to the warehouse and create picking work.</span></span>

## <a name="turn-on-the-warehouse-slotting-feature"></a><span data-ttu-id="d7066-110">Kveikja á hólfaskiptingu vöruhúss</span><span class="sxs-lookup"><span data-stu-id="d7066-110">Turn on the warehouse slotting feature</span></span>

<span data-ttu-id="d7066-111">Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="d7066-111">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="d7066-112">Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="d7066-112">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="d7066-113">Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="d7066-113">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="d7066-114">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="d7066-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="d7066-115">**Heiti eiginleika:** *Hólfaskipting vöruhúss*</span><span class="sxs-lookup"><span data-stu-id="d7066-115">**Feature name:** *Warehouse slotting feature*</span></span>

## <a name="set-up-warehouse-slotting"></a><span data-ttu-id="d7066-116">Setja upp hólfaskiptingu vöruhúss</span><span class="sxs-lookup"><span data-stu-id="d7066-116">Set up warehouse slotting</span></span>

<span data-ttu-id="d7066-117">Þú verður að setja upp eftirfarandi færibreytur í kerfinu til að hægt sé að nota hólfaskiptingu vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="d7066-117">To use warehouse slotting, you must set up the following elements in your system.</span></span>

### <a name="create-unit-of-measure-tiers-for-slotting"></a><a name="unit-tiers"></a><span data-ttu-id="d7066-118">Búa til mælieiningarlag fyrir hólfaskiptingu</span><span class="sxs-lookup"><span data-stu-id="d7066-118">Create unit-of-measure tiers for slotting</span></span>

<span data-ttu-id="d7066-119">Mælieiningarlög gera kleift að flokka margar mælieiningar saman í þeim tilgangi að skipta niður í hólf.</span><span class="sxs-lookup"><span data-stu-id="d7066-119">Unit-of-measure tiers enable multiple units of measure to be grouped together for the purposes of slotting.</span></span> <span data-ttu-id="d7066-120">Til dæmis, ef kassar í mörgum stærðum eru teknir af sama tiltektarsvæði kassa, er hægt að búa til eitt lag fyrir allar stærðirnar.</span><span class="sxs-lookup"><span data-stu-id="d7066-120">For example, if multiple sizes of boxes are all picked from the same box picking area, one tier can be created for all the sizes.</span></span> <span data-ttu-id="d7066-121">**Búa verður til línu fyrir hverja mælieiningu sem ætti að vera hluti af stiginu.**</span><span class="sxs-lookup"><span data-stu-id="d7066-121">**A line must be created for each unit of measure that should be part of the tier.**</span></span>

1. <span data-ttu-id="d7066-122">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Áfylling \> Hólfaskiptieining fyrir mælieiningarlög**.</span><span class="sxs-lookup"><span data-stu-id="d7066-122">Go to **Warehouse management \> Setup \> Replenishment \> Slotting unit of measure tiers**.</span></span>
1. <span data-ttu-id="d7066-123">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d7066-123">Select **New**.</span></span>
1. <span data-ttu-id="d7066-124">Stilla eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="d7066-124">In the header, set the following values:</span></span>

    - <span data-ttu-id="d7066-125">**Mælieiningarlag:** *EaBoxPl*</span><span class="sxs-lookup"><span data-stu-id="d7066-125">**Unit of measure tier:** *EaBoxPl*</span></span>
    - <span data-ttu-id="d7066-126">**Lýsing:** *Hvert vörubretti með kössum*</span><span class="sxs-lookup"><span data-stu-id="d7066-126">**Description:** *Each box pallet*</span></span>

1. <span data-ttu-id="d7066-127">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d7066-127">Select **Save**.</span></span>
1. <span data-ttu-id="d7066-128">Á flýtiflipanum **Mælieiningar** velur þú **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="d7066-128">On the **Units of measure** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="d7066-129">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="d7066-129">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d7066-130">**Eining:** *Kassi*</span><span class="sxs-lookup"><span data-stu-id="d7066-130">**Unit:** *Box*</span></span>
    - <span data-ttu-id="d7066-131">**Lýsing:** Hafðu svæðið autt.</span><span class="sxs-lookup"><span data-stu-id="d7066-131">**Description:** Leave this field blank.</span></span> <span data-ttu-id="d7066-132">Þetta svæði er sjálfkrafa fyllt út um leið og breytingarnar eru vistaðar.</span><span class="sxs-lookup"><span data-stu-id="d7066-132">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="d7066-133">**Einingarflokkur:** *Magn*</span><span class="sxs-lookup"><span data-stu-id="d7066-133">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="d7066-134">Veldu **Ný** til að bæta annarri línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="d7066-134">Select **New** to add a second line to the grid.</span></span>
1. <span data-ttu-id="d7066-135">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="d7066-135">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d7066-136">**Prófhópur:** *ea*</span><span class="sxs-lookup"><span data-stu-id="d7066-136">**Unit:** *ea*</span></span>
    - <span data-ttu-id="d7066-137">**Lýsing:** Hafðu svæðið autt.</span><span class="sxs-lookup"><span data-stu-id="d7066-137">**Description:** Leave this field blank.</span></span> <span data-ttu-id="d7066-138">Þetta svæði er sjálfkrafa fyllt út um leið og breytingarnar eru vistaðar.</span><span class="sxs-lookup"><span data-stu-id="d7066-138">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="d7066-139">**Einingarflokkur:** *Magn*</span><span class="sxs-lookup"><span data-stu-id="d7066-139">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="d7066-140">Veldu **Ný** til að bæta þriðju línunni við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="d7066-140">Select **New** to add a third line to the grid.</span></span>
1. <span data-ttu-id="d7066-141">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="d7066-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d7066-142">**Eining:** *VÖRUBRETTI*</span><span class="sxs-lookup"><span data-stu-id="d7066-142">**Unit:** *PL*</span></span>
    - <span data-ttu-id="d7066-143">**Lýsing:** Hafðu svæðið autt.</span><span class="sxs-lookup"><span data-stu-id="d7066-143">**Description:** Leave this field blank.</span></span> <span data-ttu-id="d7066-144">Þetta svæði er sjálfkrafa fyllt út um leið og breytingarnar eru vistaðar.</span><span class="sxs-lookup"><span data-stu-id="d7066-144">It will be filled in automatically when you save your changes.</span></span>
    - <span data-ttu-id="d7066-145">**Einingarflokkur:** *Magn*</span><span class="sxs-lookup"><span data-stu-id="d7066-145">**Unit class:** *Quantity*</span></span>

1. <span data-ttu-id="d7066-146">Veljið **Vista** til að vista lagið.</span><span class="sxs-lookup"><span data-stu-id="d7066-146">Select **Save** to save the tier.</span></span>

### <a name="create-a-directive-code-for-slotting"></a><span data-ttu-id="d7066-147">Búa til leiðbeiningarkóða fyrir hólfaskiptingu</span><span class="sxs-lookup"><span data-stu-id="d7066-147">Create a directive code for slotting</span></span>

<span data-ttu-id="d7066-148">Þú verður að velja leiðbeiningarkóða sem ætti að tengjast sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="d7066-148">You must select the directive code that should be associated with a template.</span></span>

1. <span data-ttu-id="d7066-149">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Leiðbeiningarkóðar**.</span><span class="sxs-lookup"><span data-stu-id="d7066-149">Go to **Warehouse management \> Setup \> Directive codes**.</span></span>
1. <span data-ttu-id="d7066-150">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d7066-150">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d7066-151">Í svæðinu **Leiðbeiningarkóði** skaltu slá inn *Hólfaskipting*.</span><span class="sxs-lookup"><span data-stu-id="d7066-151">In the **Directive code** field, enter *Slotting*.</span></span>
1. <span data-ttu-id="d7066-152">Í svæðinu **Lýsing leiðbeiningar** skaltu slá inn *Hólfaskipting*.</span><span class="sxs-lookup"><span data-stu-id="d7066-152">In the **Directive description** field, enter *Slotting*.</span></span>

### <a name="set-up-slotting-templates"></a><span data-ttu-id="d7066-153">Setja upp hólfaskiptingarsniðmát</span><span class="sxs-lookup"><span data-stu-id="d7066-153">Set up slotting templates</span></span>

<span data-ttu-id="d7066-154">Hvert hólfaskiptingarsniðmát stjórnar því hvernig birgðum er úthlutað á staðsetningar í tilteknu vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="d7066-154">Each slotting template controls how inventory is assigned to locations for a specific warehouse.</span></span> <span data-ttu-id="d7066-155">Hvert sniðmát verður að innihalda línu fyrir hverja forskrift hólfaskiptingar.</span><span class="sxs-lookup"><span data-stu-id="d7066-155">Each template must include a line for each slotting specification.</span></span> <span data-ttu-id="d7066-156">Notaðu ferlin í þessum hluta til að setja upp hólfaskiptingarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="d7066-156">Use the procedures in this section to set up slotting templates.</span></span>

1. <span data-ttu-id="d7066-157">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Áfylling \> Hólfaskiptingarsniðmát**.</span><span class="sxs-lookup"><span data-stu-id="d7066-157">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**.</span></span>
1. <span data-ttu-id="d7066-158">Veldu **Nýtt** til að búa til sniðmát.</span><span class="sxs-lookup"><span data-stu-id="d7066-158">Select **New** to create a template.</span></span>

<span data-ttu-id="d7066-159">Því næst verður þú að setja upp sniðmáthaus, forskriftir hólfaskiptingar og staðsetningarleiðbeiningar, eins og útskýrt er í eftirfarandi undirköflum.</span><span class="sxs-lookup"><span data-stu-id="d7066-159">Next, you must set up the template header, slotting specifications, and location directives, as explained in the following subsections.</span></span>

#### <a name="set-up-a-slotting-template-header"></a><span data-ttu-id="d7066-160">Setja upp sniðmátshaus fyrir hólfaskiptingu</span><span class="sxs-lookup"><span data-stu-id="d7066-160">Set up a slotting template header</span></span>

1. <span data-ttu-id="d7066-161">Stilltu eftirfarandi gildi í sniðmátshausnum:</span><span class="sxs-lookup"><span data-stu-id="d7066-161">In the header for the template, set the following values:</span></span>

    - <span data-ttu-id="d7066-162">**Hólfaskiptingarsniðmát:** _61_</span><span class="sxs-lookup"><span data-stu-id="d7066-162">**Slotting template:** _61_</span></span>
    - <span data-ttu-id="d7066-163">**Lýsing:** _61_</span><span class="sxs-lookup"><span data-stu-id="d7066-163">**Description:** _61_</span></span>
    - <span data-ttu-id="d7066-164">**Gerð eftirspurnar:** *Sölupöntun*</span><span class="sxs-lookup"><span data-stu-id="d7066-164">**Demand type:** *Sales order*</span></span>

        <span data-ttu-id="d7066-165">Sem stendur er *Sölupöntun* eina eftirspurnargerðin sem er studd.</span><span class="sxs-lookup"><span data-stu-id="d7066-165">Currently, *Sales order* is the only demand type that is supported.</span></span>

    - <span data-ttu-id="d7066-166">**Eftirspurnarstefna:** _Pöntuð_</span><span class="sxs-lookup"><span data-stu-id="d7066-166">**Demand strategy:** _Ordered_</span></span>

        <span data-ttu-id="d7066-167">Eftirtalin gildi eru tiltæk á þessu svæði:</span><span class="sxs-lookup"><span data-stu-id="d7066-167">The following values are available in this field:</span></span>

        - <span data-ttu-id="d7066-168">**Pantað** – Allt pantað magn á sölupöntuninni skal telja sem eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="d7066-168">**Ordered** – The full ordered quantity on the sales order should be considered demand.</span></span>
        - <span data-ttu-id="d7066-169">**Frátekið** – Aðeins magn af sölupöntunarlínu sem er frátekið (efnislega og pantað) ætti að teljast sem eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="d7066-169">**Reserved** – Only the sales order line quantities that are reserved (physical and ordered) should be considered demand.</span></span>

    - <span data-ttu-id="d7066-170">**Vöruhús:** _61_</span><span class="sxs-lookup"><span data-stu-id="d7066-170">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="d7066-171">**Leyfa bylgjueftirspurn að nota magn sem ekki er frátekið:** _Já_</span><span class="sxs-lookup"><span data-stu-id="d7066-171">**Allow wave demand to use unreserved quantities:** _Yes_</span></span>

<span data-ttu-id="d7066-172">Þú getur einnig tilgreint fyrirspurn til að þrengja umfang eftirspurnar sem er metin.</span><span class="sxs-lookup"><span data-stu-id="d7066-172">You can also specify a query to narrow the scope of the demand that is evaluated.</span></span>

#### <a name="set-up-slotting-specifications-for-each-template"></a><span data-ttu-id="d7066-173">Settu upp forskriftir hólfaskiptingar fyrir hvert sniðmát</span><span class="sxs-lookup"><span data-stu-id="d7066-173">Set up slotting specifications for each template</span></span>

<span data-ttu-id="d7066-174">Fylgdu þessum skrefum fyrir hvert sniðmát sem þú býrð til að bæta við línu fyrir hverja forskrift hólfaskiptingar.</span><span class="sxs-lookup"><span data-stu-id="d7066-174">For each template that you create, follow these steps to add a line for each slotting specification.</span></span>

1. <span data-ttu-id="d7066-175">Á flýtiflipanum **Upplýsingar um hólfaskiptingarsniðmát** velur þú **Nýtt** til að búa til nýja sniðmátslínu.</span><span class="sxs-lookup"><span data-stu-id="d7066-175">On the **Slotting template details** FastTab, select **New** to create a template line.</span></span>
1. <span data-ttu-id="d7066-176">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="d7066-176">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d7066-177">**Röð:** _1_</span><span class="sxs-lookup"><span data-stu-id="d7066-177">**Sequence:** _1_</span></span>
    - <span data-ttu-id="d7066-178">**Lýsing:** _Föst staðsetning_</span><span class="sxs-lookup"><span data-stu-id="d7066-178">**Description:** _Fixed location_</span></span>
    - <span data-ttu-id="d7066-179">**Lágmarksmagn:** _1_</span><span class="sxs-lookup"><span data-stu-id="d7066-179">**Minimum quantity:** _1_</span></span>

        <span data-ttu-id="d7066-180">Þetta svæði skilgreinir áskilið lágmarksmagn eftirspurnar fyrir línuna.</span><span class="sxs-lookup"><span data-stu-id="d7066-180">This field defines the minimum quantity of demand that is required for the line.</span></span>

    - <span data-ttu-id="d7066-181">**Hámarksmagn:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="d7066-181">**Maximum quantity:** _1000000_</span></span>

        <span data-ttu-id="d7066-182">Þetta svæði skilgreinir áskilið hámarksmagn eftirspurnar sem er gilt fyrir línuna.</span><span class="sxs-lookup"><span data-stu-id="d7066-182">This field defines the maximum quantity of demand that is valid for the line.</span></span>

    - <span data-ttu-id="d7066-183">**Eining:** Hafðu þetta svæði autt.</span><span class="sxs-lookup"><span data-stu-id="d7066-183">**Unit:** Leave this field blank.</span></span>

        <span data-ttu-id="d7066-184">Þetta svæði skilgreinir mælieininguna sem lágmarks- og hámarksmagnið vísa til.</span><span class="sxs-lookup"><span data-stu-id="d7066-184">This field defines the unit of measure that the minimum and maximum quantities refer to.</span></span>

    - <span data-ttu-id="d7066-185">**Mælieiningarlag:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="d7066-185">**Unit of Measure Tier:** _EaBoxPl_</span></span>

        <span data-ttu-id="d7066-186">Þetta svæði skilgreinir mælieiningar eftirspurnar sem gilda fyrir línuna.</span><span class="sxs-lookup"><span data-stu-id="d7066-186">This field defines the units of measure of demand that are valid for the line.</span></span> <span data-ttu-id="d7066-187">(Frekari upplýsingar er að finna í hlutanum [Uppsetning á mælieiningarlögum fyrir hólfaskiptingu](#unit-tiers) fyrr í þessu efnisatriði).</span><span class="sxs-lookup"><span data-stu-id="d7066-187">(For more information, see the [Set up unit-of-measure tiers for slotting](#unit-tiers) section earlier in this topic.)</span></span>

    - <span data-ttu-id="d7066-188">**Skilyrði úthlutunar hólfa:** _Taka mið af magni_</span><span class="sxs-lookup"><span data-stu-id="d7066-188">**Assign slot criteria:** _Consider qty_</span></span>

        <span data-ttu-id="d7066-189">Eftirtalin gildi eru tiltæk á þessu svæði:</span><span class="sxs-lookup"><span data-stu-id="d7066-189">The following values are available in this field:</span></span>

        - <span data-ttu-id="d7066-190">**Gera ráð fyrir að staðsetning sé tóm** – Þetta kerfi ætti að gera ráð fyrir að allar staðsetningar á tiltektarsvæðinu séu tómar og ætti ekki að athuga áðurnefndar staðsetningar fyrir birgðir.</span><span class="sxs-lookup"><span data-stu-id="d7066-190">**Assume empty** – This system should assume that all locations in the picking area are empty and should not check those locations for inventory.</span></span>
        - <span data-ttu-id="d7066-191">**Gera ráð fyrir magni á staðsetningu** – Kerfið ætti að athuga staðsetningu á tiltektarsvæðinu fyrir birgðir og ætti að sleppa öllum staðsetningum sem eru ekki tómar.</span><span class="sxs-lookup"><span data-stu-id="d7066-191">**Consider qty** – The system should check the locations in the picking area for inventory and should skip any locations that aren't empty.</span></span>

    - <span data-ttu-id="d7066-192">**Leiðbeiningarkóði:** _Hólfaskipting_</span><span class="sxs-lookup"><span data-stu-id="d7066-192">**Directive code:** _Slotting_</span></span>

        <span data-ttu-id="d7066-193">Þetta svæði skilgreinir staðsetningarleiðbeiningarnar sem eru notaðar til að finna tiltektarstaðsetningu áfyllingarvinnunnar.</span><span class="sxs-lookup"><span data-stu-id="d7066-193">This field defines the location directive that is used to find the picking location of the replenishment work.</span></span>

    - <span data-ttu-id="d7066-194">**Yfirflæði á staðsetningu:** Hafðu þetta svæði autt.</span><span class="sxs-lookup"><span data-stu-id="d7066-194">**Overflow location:** Leave this field blank.</span></span>

        <span data-ttu-id="d7066-195">Þetta svæði skilgreinir staðsetningu sem birgðir eru settar ef staðsetning finnst ekki fyrir magnið við vinnslu línunnar.</span><span class="sxs-lookup"><span data-stu-id="d7066-195">This field defines the location that inventory that is put to if a location can't be found for the quantity when the line is processed.</span></span>

    - <span data-ttu-id="d7066-196">**Leyfa stöðvun:** _já_</span><span class="sxs-lookup"><span data-stu-id="d7066-196">**Allow let up:** _Yes_</span></span>

        <span data-ttu-id="d7066-197">Þegar þessi valkostur er stilltur á *Já*, ef ekki er hægt að skipta einhverri eftirspurn í hólf, verður búin til birgðahreyfing til að taka birgðum úr staðsetningum þar sem engar birgðir eru, en engu var skipt niður í hólf.</span><span class="sxs-lookup"><span data-stu-id="d7066-197">When this option is set to *Yes*, if any demand can't be slotted, movement work will be created to take inventory out of locations where there is inventory, but where nothing was slotted.</span></span> <span data-ttu-id="d7066-198">Sniðmátið er síðan keyrt aftur.</span><span class="sxs-lookup"><span data-stu-id="d7066-198">The template is then run again.</span></span> <span data-ttu-id="d7066-199">Í þetta sinn hunsar það birgðir í staðsetningum.</span><span class="sxs-lookup"><span data-stu-id="d7066-199">This time, it ignores the inventory in the locations.</span></span> <span data-ttu-id="d7066-200">Þessi eiginleiki virkar best þegar svæðið **Úthluta skilyrðum fyrir hólf** er stillt á _Taka mið af magni_.</span><span class="sxs-lookup"><span data-stu-id="d7066-200">This functionality works best when the **Assign slot criteria** field is set to _Consider qty_.</span></span>

    - <span data-ttu-id="d7066-201">**Notkun fastrar staðsetningar:** _Aðeins fastar staðsetningar fyrir afurðina_</span><span class="sxs-lookup"><span data-stu-id="d7066-201">**Fixed location usage:** _Only fixed locations for the product_</span></span>

        <span data-ttu-id="d7066-202">Eftirtalin gildi eru tiltæk á þessu svæði:</span><span class="sxs-lookup"><span data-stu-id="d7066-202">The following values are available in this field:</span></span>

        - <span data-ttu-id="d7066-203">**Fastar og lausar staðsetningar** – Ekki ætti að takmarka kerfið við að nota aðeins fastar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="d7066-203">**Fixed and non-fixed locations** – The system should not be limited to using only fixed locations.</span></span>
        - <span data-ttu-id="d7066-204">**Aðeins fastar staðsetningar fyrir afurðina** – Kerfið ætti aðeins að skipta niður í hólf á staðsetningar sem eru fastar staðsetningar fyrir afurðina.</span><span class="sxs-lookup"><span data-stu-id="d7066-204">**Only fixed locations for the product** – The system should slot only to locations that are fixed locations for the product.</span></span>
        - <span data-ttu-id="d7066-205">**Aðeins fastar staðsetningar fyrir afurðarafbrigðið** – Kerfið ætti aðeins að skipta niður í hólf á staðsetningar sem eru fastar staðsetningar fyrir afurðarafbrigðið.</span><span class="sxs-lookup"><span data-stu-id="d7066-205">**Only fixed locations for the product variant** – The system should slot only to locations that are fixed locations for the product variant.</span></span>

1. <span data-ttu-id="d7066-206">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d7066-206">Select **Save**.</span></span>
1. <span data-ttu-id="d7066-207">Veldu **Ný** til að búa til aðra sniðmátslínu.</span><span class="sxs-lookup"><span data-stu-id="d7066-207">Select **New** to create a second template line.</span></span>
1. <span data-ttu-id="d7066-208">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="d7066-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d7066-209">**Röð:** _2_</span><span class="sxs-lookup"><span data-stu-id="d7066-209">**Sequence:** _2_</span></span>
    - <span data-ttu-id="d7066-210">**Lýsing:** _Annað_</span><span class="sxs-lookup"><span data-stu-id="d7066-210">**Description:** _Other_</span></span>
    - <span data-ttu-id="d7066-211">**Lágmarksmagn:** _1_</span><span class="sxs-lookup"><span data-stu-id="d7066-211">**Minimum Qty:** _1_</span></span>
    - <span data-ttu-id="d7066-212">**Hámarksmagn:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="d7066-212">**Maximum Qty:** _1000000_</span></span>
    - <span data-ttu-id="d7066-213">**Eining:** Hafðu þetta svæði autt.</span><span class="sxs-lookup"><span data-stu-id="d7066-213">**Unit:** Leave this field blank.</span></span>
    - <span data-ttu-id="d7066-214">**Mælieiningarlag:** _EaBoxPl_</span><span class="sxs-lookup"><span data-stu-id="d7066-214">**Unit of measure tier:** _EaBoxPl_</span></span>
    - <span data-ttu-id="d7066-215">**Skilyrði úthlutunar hólfa:** _Taka mið af magni_</span><span class="sxs-lookup"><span data-stu-id="d7066-215">**Assign slot criteria:** _Consider qty_</span></span>
    - <span data-ttu-id="d7066-216">**Leiðbeiningarkóði:** _Hólfaskipting_</span><span class="sxs-lookup"><span data-stu-id="d7066-216">**Directive code:** _Slotting_</span></span>
    - <span data-ttu-id="d7066-217">**Yfirflæði á staðsetningu:** Hafðu þetta svæði autt.</span><span class="sxs-lookup"><span data-stu-id="d7066-217">**Overflow location:** Leave this field blank.</span></span>
    - <span data-ttu-id="d7066-218">**Leyfa stöðvun:** _já_</span><span class="sxs-lookup"><span data-stu-id="d7066-218">**Allow let up:** _Yes_</span></span>
    - <span data-ttu-id="d7066-219">**Nota fastar staðsetningar:** _Fastar og lausar staðsetningar_</span><span class="sxs-lookup"><span data-stu-id="d7066-219">**Use fixed locations:** _Fixed and non-fixed locations_</span></span>

    <span data-ttu-id="d7066-220">Í fyrirspurninni fyrir aðra línuna tilgreinir þú skilyrðin sem eru notuð til að ákvarða hvaða staðsetningar eftirspurnar fyrir umrædda línu er hægt að skipa í hólf.</span><span class="sxs-lookup"><span data-stu-id="d7066-220">In the query for the second line, you will now specify the criteria that are used to determine what locations the demand for that line can be slotted to.</span></span>

1. <span data-ttu-id="d7066-221">Veldu línuna þar sem svæðið **Runa** er stillt á *2*.</span><span class="sxs-lookup"><span data-stu-id="d7066-221">Select the line where the **Sequence** field is set to *2*.</span></span>
1. <span data-ttu-id="d7066-222">Veldu **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="d7066-222">Select **Edit query**.</span></span>
1. <span data-ttu-id="d7066-223">Á flipanum **Svið** velur þú **Bæta við** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="d7066-223">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="d7066-224">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="d7066-224">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d7066-225">**Tafla:** *Staðir*</span><span class="sxs-lookup"><span data-stu-id="d7066-225">**Table:** *Locations*</span></span>
    - <span data-ttu-id="d7066-226">**Afleidd tafla:** *Staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="d7066-226">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="d7066-227">**Reitur:** *Auðkenni forstillingar staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="d7066-227">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="d7066-228">**Skilyrði:** *Tiltekt-06* (Veldu tvöfalt plúsmerki \[**++**\] á svæðinu til að stækka listann, og veldu síðan *Tiltekt-06* - *Tiltektarsvæði 6*.)</span><span class="sxs-lookup"><span data-stu-id="d7066-228">**Criteria:** *Pick-06* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Pick-06* - *Picking Site 6*.)</span></span>

1. <span data-ttu-id="d7066-229">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d7066-229">Select **OK**.</span></span>

#### <a name="set-up-location-directives"></a><span data-ttu-id="d7066-230">Setja upp staðsetningarleiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="d7066-230">Set up location directives</span></span>

<span data-ttu-id="d7066-231">Setja þarf upp að minnsta kosti eina staðsetningarleiðbeiningar til að styðja tiltekt við hólfaskiptingu.</span><span class="sxs-lookup"><span data-stu-id="d7066-231">At least one location directive must be set up to support slotting picks.</span></span> <span data-ttu-id="d7066-232">Notaðu verklagsreglurnar í þessum kafla til að setja upp nýjar *staðsetningarleiðbeiningar fyrir áfyllingu* fyrir tiltekt við hólfaskiptingu.</span><span class="sxs-lookup"><span data-stu-id="d7066-232">Use the procedures in this section to set up a new *replenishment location directive* for slotting picks.</span></span>

1. <span data-ttu-id="d7066-233">Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.</span><span class="sxs-lookup"><span data-stu-id="d7066-233">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="d7066-234">Í svæðinu **Gerð verkbeiðni** í vinstri glugganum velur þú *Áfylling*.</span><span class="sxs-lookup"><span data-stu-id="d7066-234">In the left pane, in the **Work order type** field, select *Replenishment*.</span></span>
1. <span data-ttu-id="d7066-235">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d7066-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="d7066-236">Í haus nýju staðsetningarleiðbeininganna á svæðinu **Heiti** slærðu inn *61 Tiltekt við hólfaskiptingu*.</span><span class="sxs-lookup"><span data-stu-id="d7066-236">In the header for the new location directive, in the **Name** field, enter *61 Slotting pick*.</span></span>

##### <a name="configure-the-location-directives-fasttab"></a><span data-ttu-id="d7066-237">Grunnstilling flýtiflipans Staðsetningarleiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="d7066-237">Configure the Location directives FastTab</span></span>

1. <span data-ttu-id="d7066-238">Stilltu eftirfarandi gildi á flýtiflipanum **staðsetningarleiðbeiningar**.</span><span class="sxs-lookup"><span data-stu-id="d7066-238">On the **Location directives** FastTab, set the following values.</span></span> <span data-ttu-id="d7066-239">Samþykktu sjálfgildin fyrir öll önnur svæði.</span><span class="sxs-lookup"><span data-stu-id="d7066-239">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="d7066-240">**Tegund vinnu:** _Tínsla_</span><span class="sxs-lookup"><span data-stu-id="d7066-240">**Work type:** _Pick_</span></span>
    - <span data-ttu-id="d7066-241">**Svæði:** _6_</span><span class="sxs-lookup"><span data-stu-id="d7066-241">**Site:** _6_</span></span>
    - <span data-ttu-id="d7066-242">**Vöruhús:** _61_</span><span class="sxs-lookup"><span data-stu-id="d7066-242">**Warehouse:** _61_</span></span>
    - <span data-ttu-id="d7066-243">**Leiðbeiningarkóði:** _Hólfaskipting_</span><span class="sxs-lookup"><span data-stu-id="d7066-243">**Directive code:** _Slotting_</span></span>

1. <span data-ttu-id="d7066-244">Veldu **Vista** til að gera flýtiflipann **Línur** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="d7066-244">Select **Save** to make the **Lines** FastTab available.</span></span>

##### <a name="configure-the-lines-fasttab"></a><span data-ttu-id="d7066-245">Grunnstilling flýtiflipans Línur</span><span class="sxs-lookup"><span data-stu-id="d7066-245">Configure the Lines FastTab</span></span>

1. <span data-ttu-id="d7066-246">Á flýtiflipanum **Línur** velur þú **Ný** til að búa til línu.</span><span class="sxs-lookup"><span data-stu-id="d7066-246">On the **Lines** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="d7066-247">Stilltu eftirfarandi gildi á nýju línunni.</span><span class="sxs-lookup"><span data-stu-id="d7066-247">On the new line, set the following values.</span></span> <span data-ttu-id="d7066-248">Samþykktu sjálfgildin fyrir öll önnur svæði.</span><span class="sxs-lookup"><span data-stu-id="d7066-248">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="d7066-249">**Frá-magn:** _0_</span><span class="sxs-lookup"><span data-stu-id="d7066-249">**From quantity:** _0_</span></span>
    - <span data-ttu-id="d7066-250">**Til magn:** _1000000_</span><span class="sxs-lookup"><span data-stu-id="d7066-250">**To quantity:** _1000000_</span></span>

1. <span data-ttu-id="d7066-251">Veldu **Vista** til að gera flýtiflipann **Aðgerðir í staðsetningarleiðbeiningum** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="d7066-251">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>

##### <a name="configure-the-location-directive-actions-fasttab"></a><span data-ttu-id="d7066-252">Grunnstilling flýtiflipans Aðgerðir í staðsetningarleiðbeiningum</span><span class="sxs-lookup"><span data-stu-id="d7066-252">Configure the Location Directive Actions FastTab</span></span>

1. <span data-ttu-id="d7066-253">Á flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** velur þú **Ný** til að búa til línu.</span><span class="sxs-lookup"><span data-stu-id="d7066-253">On the **Location Directive Actions** FastTab, select **New** to create a line.</span></span>
1. <span data-ttu-id="d7066-254">Stilltu eftirfarandi gildi á nýju línunni.</span><span class="sxs-lookup"><span data-stu-id="d7066-254">On the new line, set the following values.</span></span> <span data-ttu-id="d7066-255">Samþykktu sjálfgildin fyrir öll önnur svæði.</span><span class="sxs-lookup"><span data-stu-id="d7066-255">Accept the default values for all other fields.</span></span>

    - <span data-ttu-id="d7066-256">**Heiti:** _Magn_</span><span class="sxs-lookup"><span data-stu-id="d7066-256">**Name:** _Bulk_</span></span>
    - <span data-ttu-id="d7066-257">**Áætlun:** _Engin_</span><span class="sxs-lookup"><span data-stu-id="d7066-257">**Strategy:** _None_</span></span>

1. <span data-ttu-id="d7066-258">Veldu **Vista** til að gera hnappinn **Breyta fyrirspurn** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="d7066-258">Select **Save** to make the **Edit query** button available.</span></span>

##### <a name="edit-the-query"></a><span data-ttu-id="d7066-259">Breyta fyrirspurn</span><span class="sxs-lookup"><span data-stu-id="d7066-259">Edit the query</span></span>

1. <span data-ttu-id="d7066-260">Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="d7066-260">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="d7066-261">Á flipanum **Svið** velur þú **Bæta við** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="d7066-261">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="d7066-262">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="d7066-262">On the new line, set the following values:</span></span>

    - <span data-ttu-id="d7066-263">**Tafla:** *Staðir*</span><span class="sxs-lookup"><span data-stu-id="d7066-263">**Table:** *Locations*</span></span>
    - <span data-ttu-id="d7066-264">**Afleidd tafla:** *Staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="d7066-264">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="d7066-265">**Reitur::** *Auðkenni svæðis*</span><span class="sxs-lookup"><span data-stu-id="d7066-265">**Field:** *Zone ID*</span></span>
    - <span data-ttu-id="d7066-266">**Skilyrði:** *Magn* (Veldu tvöfalt plúsmerki \[**++**\] á svæðinu til að stækka listann, og veldu síðan *Magn*).</span><span class="sxs-lookup"><span data-stu-id="d7066-266">**Criteria:** *Bulk* (Select the double plus sign \[**++**\] in the field to expand the list, and then select *Bulk*.)</span></span>

1. <span data-ttu-id="d7066-267">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d7066-267">Select **OK**.</span></span>

## <a name="scenario"></a><span data-ttu-id="d7066-268">Aðstæður</span><span class="sxs-lookup"><span data-stu-id="d7066-268">Scenario</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="d7066-269">Setja upp aðstæður</span><span class="sxs-lookup"><span data-stu-id="d7066-269">Set up the scenario</span></span>

<span data-ttu-id="d7066-270">Notaðu innbyggðu sýnigögnin fyrir þessar aðstæður og búðu til skrárnar sem lýst er í þessum hluta.</span><span class="sxs-lookup"><span data-stu-id="d7066-270">For this scenario, use the built-in sample data, and create the records that are described in this section.</span></span>

#### <a name="use-the-usmf-sample-data"></a><span data-ttu-id="d7066-271">Nota USMF-sýnigögn</span><span class="sxs-lookup"><span data-stu-id="d7066-271">Use the USMF sample data</span></span>

<span data-ttu-id="d7066-272">Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind hér verður þú að vera á kerfi þar sem venjuleg [sýnigögn](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er sett upp.</span><span class="sxs-lookup"><span data-stu-id="d7066-272">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="d7066-273">Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.</span><span class="sxs-lookup"><span data-stu-id="d7066-273">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

#### <a name="create-demand"></a><span data-ttu-id="d7066-274">Búa til eftirspurn</span><span class="sxs-lookup"><span data-stu-id="d7066-274">Create demand</span></span>

<span data-ttu-id="d7066-275">Fylgdu eftirfarandi skrefum til að búa til eftirspurn sem verður notuð við hólfaskiptingu.</span><span class="sxs-lookup"><span data-stu-id="d7066-275">Follow these steps to create the demand that you will apply slotting to.</span></span>

1. <span data-ttu-id="d7066-276">Opnið **Sala og markaðssetning \> Sölupantanir \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="d7066-276">Go to **Sales and marketing \> Sales orders \> All sales order**.</span></span>
1. <span data-ttu-id="d7066-277">Smellið á **Nýtt** til að stofna nýja sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="d7066-277">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="d7066-278">IÍ svarglugganum **Búa til sölupöntun** í svæðinu **Viðskiptavinalykill** skaltu velja _US-007_.</span><span class="sxs-lookup"><span data-stu-id="d7066-278">In the **Create sales order** dialog box, in the **Customer account** field, select _US-007_.</span></span>
1. <span data-ttu-id="d7066-279">Í reitnum **Vöruhús** skal velja _61_.</span><span class="sxs-lookup"><span data-stu-id="d7066-279">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="d7066-280">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d7066-280">Select **OK**.</span></span>
1. <span data-ttu-id="d7066-281">Ný sölupöntun opnast.</span><span class="sxs-lookup"><span data-stu-id="d7066-281">The new sales order is opened.</span></span> <span data-ttu-id="d7066-282">Hún inniheldur tóma línu á flýtiflipanum **Sölupöntunarlína**.</span><span class="sxs-lookup"><span data-stu-id="d7066-282">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d7066-283">Stilltu eftirfarandi gildi á þessari línu:</span><span class="sxs-lookup"><span data-stu-id="d7066-283">On this line, set the following values:</span></span>

    - <span data-ttu-id="d7066-284">**Vara:** _L0101_</span><span class="sxs-lookup"><span data-stu-id="d7066-284">**Item:** _L0101_</span></span>
    - <span data-ttu-id="d7066-285">**Magn:** _20_</span><span class="sxs-lookup"><span data-stu-id="d7066-285">**Quantity:** _20_</span></span>

1. <span data-ttu-id="d7066-286">Veldu **Bæta við línu** til að bæta við nýrri línu og stilltu eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="d7066-286">Select **Add line** to add a new line, and set the following values:</span></span>

    - <span data-ttu-id="d7066-287">**Vara:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="d7066-287">**Item:** _T0100_</span></span>
    - <span data-ttu-id="d7066-288">**Magn:** _8_</span><span class="sxs-lookup"><span data-stu-id="d7066-288">**Quantity:** _8_</span></span>

1. <span data-ttu-id="d7066-289">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d7066-289">Select **Save**.</span></span>
1. <span data-ttu-id="d7066-290">Veldu **Nýtt** til að búa til aðra sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="d7066-290">Select **New** to create a second sales order.</span></span>
1. <span data-ttu-id="d7066-291">IÍ svarglugganum **Búa til sölupöntun** í svæðinu **Viðskiptavinalykill** skaltu velja _US-008_.</span><span class="sxs-lookup"><span data-stu-id="d7066-291">In the **Create sales order** dialog box, in the **Customer account** field, select _US-008_.</span></span>
1. <span data-ttu-id="d7066-292">Í reitnum **Vöruhús** skal velja _61_.</span><span class="sxs-lookup"><span data-stu-id="d7066-292">In the **Warehouse** field, select _61_.</span></span>
1. <span data-ttu-id="d7066-293">Ný sölupöntun opnast.</span><span class="sxs-lookup"><span data-stu-id="d7066-293">The new sales order is opened.</span></span> <span data-ttu-id="d7066-294">Hún inniheldur tóma línu á flýtiflipanum **Sölupöntunarlína**.</span><span class="sxs-lookup"><span data-stu-id="d7066-294">It includes an empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="d7066-295">Stilltu eftirfarandi gildi á þessari línu:</span><span class="sxs-lookup"><span data-stu-id="d7066-295">On this line, set the following values:</span></span>

    - <span data-ttu-id="d7066-296">**Vara:** _T0100_</span><span class="sxs-lookup"><span data-stu-id="d7066-296">**Item:** _T0100_</span></span>
    - <span data-ttu-id="d7066-297">**Magn:** _1_</span><span class="sxs-lookup"><span data-stu-id="d7066-297">**Quantity:** _1_</span></span>

1. <span data-ttu-id="d7066-298">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d7066-298">Select **Save**.</span></span>

### <a name="walk-through-a-typical-slotting-scenario"></a><span data-ttu-id="d7066-299">Handleiðsla í gegnum hefðbundnar aðstæður við hólfaskiptingu</span><span class="sxs-lookup"><span data-stu-id="d7066-299">Walk through a typical slotting scenario</span></span>

<span data-ttu-id="d7066-300">Þegar öll skilyrði eru uppfyllt, eins og lýst er í fyrri hlutanum, ertu tilbúinn að prófa eiginleikann með því að vinna í gegnum hverja æfingu í þessum kafla.</span><span class="sxs-lookup"><span data-stu-id="d7066-300">After all the prerequisite elements are in place, as described in the previous section, you're ready to try out the feature by working through each exercise in this section.</span></span>

#### <a name="generate-demand"></a><span data-ttu-id="d7066-301">Búa til eftirspurn</span><span class="sxs-lookup"><span data-stu-id="d7066-301">Generate demand</span></span>

1. <span data-ttu-id="d7066-302">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Áfylling \> Hólfaskiptingarsniðmát** og veldu hólfaskiptingarsniðmátið sem þú bjóst til áður.</span><span class="sxs-lookup"><span data-stu-id="d7066-302">Go to **Warehouse management \> Setup \> Replenishment \> Slotting templates**, and select the slotting template that you created earlier.</span></span>
1. <span data-ttu-id="d7066-303">Á aðgerðasvæðinu skal velja **Búa til eftirspurn**.</span><span class="sxs-lookup"><span data-stu-id="d7066-303">On the Action Pane, select **Generate demand**.</span></span> <span data-ttu-id="d7066-304">Þessi skipun metur alla eftirspurn sem er í kerfinu og samsvarar fyrirspurninni um hólfaskiptingarsniðmátið.</span><span class="sxs-lookup"><span data-stu-id="d7066-304">This command evaluates all demand that is in the system, and that matches the slotting template query.</span></span> <span data-ttu-id="d7066-305">Heildareftirspurn yfir allar pantanir er síðan sameinaður í eina línu fyrir hvert magn/mælieining.</span><span class="sxs-lookup"><span data-stu-id="d7066-305">The total demand across all orders is then consolidated onto one line per quantity/unit of measure.</span></span> <span data-ttu-id="d7066-306">Upplýsingaboð birtast þegar ferlið er fullklárað.</span><span class="sxs-lookup"><span data-stu-id="d7066-306">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-demand"></a><span data-ttu-id="d7066-307">Eftirspurn eftir hólfaskiptingu</span><span class="sxs-lookup"><span data-stu-id="d7066-307">Slotting demand</span></span>

<span data-ttu-id="d7066-308">*Eftirspurn eftir hólfaskiptingu* sýnir niðurstöður myndunar eftirspurnar miðað við uppsetningu hólfaskiptingarsniðmátsins.</span><span class="sxs-lookup"><span data-stu-id="d7066-308">The *slotting demand* shows the results of demand generation, based on the setup of the slotting template.</span></span>

- <span data-ttu-id="d7066-309">Á aðgerðarsvæðinu velur þú **Eftirspurn eftir hólfaskiptingu** til að skoða niðurstöður skipunarinnar **Búa til eftirspurn**.</span><span class="sxs-lookup"><span data-stu-id="d7066-309">On the Action Pane, select **Slotting demand** to view the results from the **Generate demand** command.</span></span> <span data-ttu-id="d7066-310">Hægt er að breyta línunum í eftirspurn eftir hólfaskiptingu.</span><span class="sxs-lookup"><span data-stu-id="d7066-310">The lines in the slotting demand can be edited.</span></span> <span data-ttu-id="d7066-311">Þú getur eytt línu, bætt við nýrri línu eða breytt upplýsingum um línuna.</span><span class="sxs-lookup"><span data-stu-id="d7066-311">You can delete a line, add a new line, or edit the line details.</span></span>

> [!NOTE]
> <span data-ttu-id="d7066-312">Þú getur breytt eftirspurn handvirkt, eða þú getur flutt hana inn frá utanaðkomandi kerfi með gagnastjórnun.</span><span class="sxs-lookup"><span data-stu-id="d7066-312">You can edit demand manually, or you can import it from an external system by using data management.</span></span> <span data-ttu-id="d7066-313">Allt efni í eftirspurn eftir hólfaskiptingu er notað í næsta skrefi, óháð því hvaðan hún kom.</span><span class="sxs-lookup"><span data-stu-id="d7066-313">Whatever is in the slotting demand will be used in the next step, regardless of where it came from.</span></span>

#### <a name="locate-demand"></a><span data-ttu-id="d7066-314">Finna eftirspurn</span><span class="sxs-lookup"><span data-stu-id="d7066-314">Locate demand</span></span>

<span data-ttu-id="d7066-315">Eftir að eftirspurn hefur verið mynduð verður þú að nota skipunina **Finna eftirspurn** til að búa til *áætlunina um hólfaskiptingu*.</span><span class="sxs-lookup"><span data-stu-id="d7066-315">After demand has been generated, you must use the **Locate demand** command to generate the *slotting plan*.</span></span>

- <span data-ttu-id="d7066-316">Á aðgerðasvæðinu skal velja **Finna eftirspurn**.</span><span class="sxs-lookup"><span data-stu-id="d7066-316">On the Action Pane, select **Locate demand**.</span></span> <span data-ttu-id="d7066-317">Hólfaskiptingarferlið er keyrt.</span><span class="sxs-lookup"><span data-stu-id="d7066-317">The slotting process runs.</span></span> <span data-ttu-id="d7066-318">Upplýsingaboð birtast þegar ferlið er fullklárað.</span><span class="sxs-lookup"><span data-stu-id="d7066-318">An informational message appears when the process is completed.</span></span>

#### <a name="slotting-plan"></a><span data-ttu-id="d7066-319">Hólfaskiptingaráætlun</span><span class="sxs-lookup"><span data-stu-id="d7066-319">Slotting plan</span></span>

<span data-ttu-id="d7066-320">Áætlunin fyrir hólfaskiptingu sýnir staðsetningu sem hverri vöru/magni var úthlutað, hvort yfirflæði var notað, hvort vinnustöðvun var búin til og sniðmátalínan sem var notuð.</span><span class="sxs-lookup"><span data-stu-id="d7066-320">The slotting plan shows the location that each item/quantity was assigned to, whether overflow was used, whether let-up work was created, and the template line that was used.</span></span> <span data-ttu-id="d7066-321">**Eftirspurn sem ekki var hægt að skipa í hólf er auðkennd með rauðu.**</span><span class="sxs-lookup"><span data-stu-id="d7066-321">**Any demand that could not be slotted is highlighted in red.**</span></span>

- <span data-ttu-id="d7066-322">Á aðgerðarsvæðinu velur þú **Áætlun fyrir hólfaskiptingu** til að skoða niðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="d7066-322">On the Action Pane, select **Slotting plan** to view the results.</span></span>

#### <a name="create-replenishment"></a><span data-ttu-id="d7066-323">Stofna áfyllingu</span><span class="sxs-lookup"><span data-stu-id="d7066-323">Create replenishment</span></span>

<span data-ttu-id="d7066-324">Þegar áætlun fyrir hólfaskiptingu hefur verið búin til verður þú að búa til *áfyllingarvinnu* miðað við áætlunina.</span><span class="sxs-lookup"><span data-stu-id="d7066-324">After the slotting plan has been created, you must create *replenishment work*, based on the plan.</span></span>

- <span data-ttu-id="d7066-325">Á aðgerðasvæðinu skal velja **Keyra áfyllingu**.</span><span class="sxs-lookup"><span data-stu-id="d7066-325">On the Action Pane, select **Run replenishment**.</span></span> <span data-ttu-id="d7066-326">Upplýsingaboð birtast þegar ferlið er fullklárað.</span><span class="sxs-lookup"><span data-stu-id="d7066-326">An informational message appears when the process is completed.</span></span> <span data-ttu-id="d7066-327">Þessi skilaboð gefa til kynna fjölda hausa sem voru búnir til fyrir smíðakenni vinnu.</span><span class="sxs-lookup"><span data-stu-id="d7066-327">This message indicates the number of headers that were created for the work build ID.</span></span>

<span data-ttu-id="d7066-328">Staðsetningarleiðbeiningar sem notaðar verða eru auðkenndar út frá leiðbeiningarkóðanum sem er tilgreindur á hverri sniðmátslínu.</span><span class="sxs-lookup"><span data-stu-id="d7066-328">Location directives that will be used are identified based on the directive code that is specified on each template line.</span></span>

## <a name="tips"></a><span data-ttu-id="d7066-329">Ábendingar</span><span class="sxs-lookup"><span data-stu-id="d7066-329">Tips</span></span>

### <a name="set-up-automatic-slotting"></a><span data-ttu-id="d7066-330">Setja upp sjálfvirka hólfaskiptingu</span><span class="sxs-lookup"><span data-stu-id="d7066-330">Set up automatic slotting</span></span>

<span data-ttu-id="d7066-331">Eftir að allir nauðsynlegir þættir eru til staðar geturðu sett upp hólfaskiptingu til að keyra sjálfkrafa með því að fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="d7066-331">After all the required elements are in place, you can set up slotting to run automatically by following these steps.</span></span>

1. <span data-ttu-id="d7066-332">Opnaðu **Vöruhúsakerfi \> Áfylling \> Keyra hólfaskiptingu**.</span><span class="sxs-lookup"><span data-stu-id="d7066-332">Go to **Warehouse management \> Replenishment \> Run slotting**.</span></span>
1. <span data-ttu-id="d7066-333">Tilgreindu skref hólfaskiptingar sem á að keyra.</span><span class="sxs-lookup"><span data-stu-id="d7066-333">Specify the slotting steps to run.</span></span> <span data-ttu-id="d7066-334">Veldu eitt eða fleiri af eftirfarandi skrefum hólfaskiptingar:</span><span class="sxs-lookup"><span data-stu-id="d7066-334">Select one or more of the following slotting steps:</span></span>

    - <span data-ttu-id="d7066-335">Búa til eftirspurn</span><span class="sxs-lookup"><span data-stu-id="d7066-335">Generate demand</span></span>
    - <span data-ttu-id="d7066-336">Finna eftirspurn</span><span class="sxs-lookup"><span data-stu-id="d7066-336">Locate demand</span></span>
    - <span data-ttu-id="d7066-337">Stofna áfyllingarvinnu</span><span class="sxs-lookup"><span data-stu-id="d7066-337">Create replenishment work</span></span>

    > [!NOTE]
    > <span data-ttu-id="d7066-338">Skrefin við hólfaskiptingu eru samfelld.</span><span class="sxs-lookup"><span data-stu-id="d7066-338">The slotting steps are progressive.</span></span> <span data-ttu-id="d7066-339">Ef þú vilt velja *Finna eftirspurn* verður þú fyrst að velja *Búa til eftirspurn*.</span><span class="sxs-lookup"><span data-stu-id="d7066-339">If you want to select *Locate demand*, you must first select *Generate demand*.</span></span>

1. <span data-ttu-id="d7066-340">Tilgreindu hólfaskiptingarsniðmátið sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="d7066-340">Specify the slotting template to use.</span></span>
1. <span data-ttu-id="d7066-341">Stilltu endurtekninguna til að keyra sjálfkrafa ef þú vilt.</span><span class="sxs-lookup"><span data-stu-id="d7066-341">Set the recurrence to run automatically, if you want.</span></span>

<span data-ttu-id="d7066-342">Þegar aðstæður eru æfðar skal **ekki** setja upp sjálfvirka hólfaskiptingu.</span><span class="sxs-lookup"><span data-stu-id="d7066-342">For the exercises in the scenario, do **not** set up automatic slotting.</span></span>
