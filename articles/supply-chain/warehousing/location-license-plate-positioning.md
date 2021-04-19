---
title: Númeraplötustaða staðsetningar
description: Númeraplötustaða staðsetningar gerir þér kleift að sjá hvar tiltekin númeraplata er á staðsetningu með mörgum vörubrettum, eins og staðsetningu þar sem vörubrettum er raðað ofan á hvort annað.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: e5fd7a9a9703f9ab6802def0aac096e29aa04f1a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831387"
---
# <a name="location-license-plate-positioning"></a><span data-ttu-id="ea47c-103">Númeraplötustaða staðsetningar</span><span class="sxs-lookup"><span data-stu-id="ea47c-103">Location license plate positioning</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea47c-104">Númeraplötustaða staðsetningar gerir þér kleift að sjá hvar tiltekin númeraplata er á staðsetningu með mörgum vörubrettum, eins og staðsetningu þar sem vörubrettum er raðað ofan á hvort annað.</span><span class="sxs-lookup"><span data-stu-id="ea47c-104">License plate location positioning lets you see where a license plate is located in a multi-pallet location, such as a location that uses double-deep pallet racking.</span></span>

<span data-ttu-id="ea47c-105">Eiginleikinn bætir raðnúmeri við hverja númeraplötu sem er sett á geymslustað.</span><span class="sxs-lookup"><span data-stu-id="ea47c-105">The feature adds a sequence number to each license plate that is put into a storage location.</span></span> <span data-ttu-id="ea47c-106">Þetta raðnúmer er notað til að raða númeraplötunum á geymslustaðnum.</span><span class="sxs-lookup"><span data-stu-id="ea47c-106">This sequence number is used to order the license plates in the storage location.</span></span> <span data-ttu-id="ea47c-107">Þar af leiðandir styður eiginleikinn á snjallan hátt aðstæður þar sem viðskiptavinir nota hallandi hillukerfi og þurfa að vita hvaða númeraplata snýr fram við tiltekt.</span><span class="sxs-lookup"><span data-stu-id="ea47c-107">Therefore, the feature intelligently supports scenarios where customers are using a gravity racking system and must know, for picking purposes, which license plate is front-facing.</span></span>

<span data-ttu-id="ea47c-108">Þetta efnisatriði kynnir aðstæður sem sýna hvernig á að setja upp og nota eiginleikann.</span><span class="sxs-lookup"><span data-stu-id="ea47c-108">This topic presents a scenario that shows how to set up and use the feature.</span></span>

## <a name="turn-on-the-location-license-plate-positioning-feature"></a><span data-ttu-id="ea47c-109">Kveikið á eiginleikanum Númeraplötustaða staðsetningar</span><span class="sxs-lookup"><span data-stu-id="ea47c-109">Turn on the Location license plate positioning feature</span></span>

<span data-ttu-id="ea47c-110">Áður en hægt er að nota númeraplötustöðu staðsetningar verður að kveikja á eiginleikanum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="ea47c-110">Before you can use license plate location positioning, the feature must be turned on in your system.</span></span> <span data-ttu-id="ea47c-111">Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="ea47c-111">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="ea47c-112">Þar er eiginleikinn sýndur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="ea47c-112">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="ea47c-113">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="ea47c-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="ea47c-114">**Heiti eiginleika:** *Númeraplötustaða staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="ea47c-114">**Feature name:** *Location license plate positioning*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="ea47c-115">Dæmi</span><span class="sxs-lookup"><span data-stu-id="ea47c-115">Example scenario</span></span>

### <a name="make-sample-data-available"></a><span data-ttu-id="ea47c-116">Gera sýnigögn tiltæk</span><span class="sxs-lookup"><span data-stu-id="ea47c-116">Make sample data available</span></span>

<span data-ttu-id="ea47c-117">Til að vinna í gegnum þessar aðstæður með því að nota gildin sem hér koma fram, verður þú að nota kerfi þar sem sýnigögn eru sett upp.</span><span class="sxs-lookup"><span data-stu-id="ea47c-117">To work through this scenario by using the values that are suggested here, you must work on a system where sample data is installed.</span></span> <span data-ttu-id="ea47c-118">Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.</span><span class="sxs-lookup"><span data-stu-id="ea47c-118">Additionally, you must select the **USMF** legal entity before you start.</span></span>

### <a name="set-up-the-feature-for-this-scenario"></a><span data-ttu-id="ea47c-119">Setja upp eiginleikann fyrir þessar aðstæður</span><span class="sxs-lookup"><span data-stu-id="ea47c-119">Set up the feature for this scenario</span></span>

<span data-ttu-id="ea47c-120">Ljúktu eftirfarandi aðferðum til að setja upp eiginleikann *Númeraplötustaða staðsetningar* fyrir aðstæðurnar sem eru kynntar í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="ea47c-120">Complete the following procedures to set up the *Location license plate positioning* feature for the scenario that is presented in this topic.</span></span>

#### <a name="location-profiles"></a><span data-ttu-id="ea47c-121">Forstillingar staðsetningar</span><span class="sxs-lookup"><span data-stu-id="ea47c-121">Location profiles</span></span>

<span data-ttu-id="ea47c-122">Kveikja verður á eiginleikanum í staðsetningarforstillingunni fyrir allar staðsetningar þar sem hann verður notaður.</span><span class="sxs-lookup"><span data-stu-id="ea47c-122">The feature must be turned on in the location profile for every location where it will be used.</span></span>

1. <span data-ttu-id="ea47c-123">Fara í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Forstillingar staðsetningar**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-123">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="ea47c-124">Veldu **MAGN-06** í listanum yfir staðsetningarforstillingar á svæðinu vinstra megin.</span><span class="sxs-lookup"><span data-stu-id="ea47c-124">In the list of location profiles in the left pane, select **BULK-06**.</span></span>
1. <span data-ttu-id="ea47c-125">Tveir nýir valkostir verið bætt við af eiginleikanum á flýtiflipanum **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-125">On the **General** FastTab, two new options have been added by the feature.</span></span> <span data-ttu-id="ea47c-126">Stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="ea47c-126">Set the following values:</span></span>

    - <span data-ttu-id="ea47c-127">**Virkja númeraplötustöðu:** *Já*</span><span class="sxs-lookup"><span data-stu-id="ea47c-127">**Enable license plate position:** *Yes*</span></span>

        <span data-ttu-id="ea47c-128">Þegar aðgerðin er stillt á *Já*, verður númeraplötustöðunni haldið við fyrir númeraplötur í staðsetningunni.</span><span class="sxs-lookup"><span data-stu-id="ea47c-128">When this option is set to *Yes*, the license plate position will be maintained for license plates in the location.</span></span>

    - <span data-ttu-id="ea47c-129">**Birta númeraplötustöðu í fartæki:** *Já*</span><span class="sxs-lookup"><span data-stu-id="ea47c-129">**Display mobile device LP position:** *Yes*</span></span>

        <span data-ttu-id="ea47c-130">Þegar þessi valkostur er stilltur á *Já*, verður fartækjanotendum sýnd númeraplötustaðan við breytingar og talningu.</span><span class="sxs-lookup"><span data-stu-id="ea47c-130">When this option is set to *Yes*, the license plate position will be shown to mobile device users during adjustment and counting.</span></span> <span data-ttu-id="ea47c-131">Þú getur aðeins breytt stillingunni á þessum möguleika þegar kveikt er á eiginleikanum.</span><span class="sxs-lookup"><span data-stu-id="ea47c-131">You can change the setting of this option only when the feature is turned on.</span></span>

1. <span data-ttu-id="ea47c-132">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-132">Select **Save**.</span></span>

#### <a name="location-directives"></a><span data-ttu-id="ea47c-133">Staðsetningarleiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="ea47c-133">Location directives</span></span>

1. <span data-ttu-id="ea47c-134">Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-134">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="ea47c-135">Gakktu úr skugga um að svæðið **Gerð verkbeiðni** sé stillt á *Sölupantanir* í vinstri glugganum.</span><span class="sxs-lookup"><span data-stu-id="ea47c-135">In the left pane, make sure that the **Work order type** field is set to *Sales orders*.</span></span>
1. <span data-ttu-id="ea47c-136">Veldu **61 Tiltektarpöntun sölupöntunar** á listanum yfir staðsetningarleiðbeiningar.</span><span class="sxs-lookup"><span data-stu-id="ea47c-136">In the list of location directives, select **61 SO Pick order**.</span></span>
1. <span data-ttu-id="ea47c-137">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-137">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="ea47c-138">Á flýtiflipanum **Línur** velur þú línuna sem hefur **raðnúmeragildið** *2*.</span><span class="sxs-lookup"><span data-stu-id="ea47c-138">On the **Lines** FastTab, select the line that has a **Sequence number** value of *2*.</span></span>
1. <span data-ttu-id="ea47c-139">Á flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum**, velur þú línuna sem hefur **Nafngildi** *Taka til fyrir minna en bretti* (hún ætti að vera eina lína) og breytir **Raðnúmeragildi** hennar í *2*.</span><span class="sxs-lookup"><span data-stu-id="ea47c-139">On the **Location Directive Actions** FastTab, select the line that has a **Name** value of *Pick for less than pallet* (it should be the only line), and change its **Sequence number** value to *2*.</span></span>
1. <span data-ttu-id="ea47c-140">Veldu **Nýtt** fyrir ofan hnitanetið til að bæta við línu fyrir nýjar aðgerðir í staðsetningarleiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="ea47c-140">Select **New** above the grid to add a line for a new location directive action.</span></span>
1. <span data-ttu-id="ea47c-141">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="ea47c-141">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ea47c-142">**Raðnúmer:** *1*</span><span class="sxs-lookup"><span data-stu-id="ea47c-142">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="ea47c-143">**Heiti:** *Staðsetning tiltektar 1*</span><span class="sxs-lookup"><span data-stu-id="ea47c-143">**Name:** *Pick position 1*</span></span>

1. <span data-ttu-id="ea47c-144">Meðan nýja línan er enn valin skaltu velja **Breyta fyrirspurn** fyrir ofan hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="ea47c-144">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="ea47c-145">Veldu flipann **Samtengingar** í fyrirspurnarritlinum.</span><span class="sxs-lookup"><span data-stu-id="ea47c-145">In the query editor, select the **Joins** tab.</span></span>
1. <span data-ttu-id="ea47c-146">Stækkaðu töfluna **Staðsetningar** til að birta tenginguna við töfluna **Birgðavíddir**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-146">Expand the **Locations** table join to show the join to the **Inventory dimensions** table.</span></span>
1. <span data-ttu-id="ea47c-147">Stækkaðu töfluna **Birgðavíddir** til að birta tenginguna við töfluna **Lagerbirgðir**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-147">Expand the **Inventory dimensions** table join to show the join to the **On-hand inventory** table.</span></span>
1. <span data-ttu-id="ea47c-148">Veldu **Birgðavíddir** og veldu síðan **Bæta við töflutengingu**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-148">Select **Inventory dimensions**, and then select **Add table join**.</span></span>
1. <span data-ttu-id="ea47c-149">Í listanum yfir töflur sem birtist í dálkinum **Tengsl** skaltu velja **Númeraplata (númeraplata)**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-149">In the list of tables that appears, in the **Relation** column, select **License plate (License plate)**.</span></span> <span data-ttu-id="ea47c-150">Veldu síðan **Velja** til að bæta **Númeraplötu** við töflutenginguna **Birgðavíddir**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-150">Then select **Select** to add **License plate** to the **Inventory dimensions** table join.</span></span>
1. <span data-ttu-id="ea47c-151">Veldu **Númeraplötu** og veldu svo **Bæta við töflutengingu**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-151">While **License plate** is still selected, select **Add table join**.</span></span>
1. <span data-ttu-id="ea47c-152">Í listanum yfir töflur sem birtist velur þú í dálknum **Tengsl** velur þú **Númeraplötustaða staðsetningar (númeraplata)**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-152">In the list of tables that appears, in the **Relation** column, select **Location license plate positioning (License plate)**.</span></span> <span data-ttu-id="ea47c-153">Veldu síðan **Velja** til að bæta **Númeraplötustöðu staðsetningar** við töflutenginguna **Birgðavíddir**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-153">Then select **Select** to add **Location license plate positioning** to the **Inventory dimensions** table join.</span></span>

    <span data-ttu-id="ea47c-154">![Töflutengingar](media/LpTableJoin.png "Töflutengingar")</span><span class="sxs-lookup"><span data-stu-id="ea47c-154">![Table joins](media/LpTableJoin.png "Table joins")</span></span>

1. <span data-ttu-id="ea47c-155">Veldu **Í lagi** til að staðfesta uppfærðar töflutengingar og loka fyrirspurnarritlinum.</span><span class="sxs-lookup"><span data-stu-id="ea47c-155">Select **OK** to confirm the updated joined tables and close the query editor.</span></span>
1. <span data-ttu-id="ea47c-156">Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Breyta fyrirspurn** til að opna fyrirspurnarritilinn að nýju.</span><span class="sxs-lookup"><span data-stu-id="ea47c-156">On the **Location Directive Actions** FastTab, select **Edit query** again to reopen to the query editor.</span></span>
1. <span data-ttu-id="ea47c-157">Á flipanum **Svið** velur þú **Bæta við** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="ea47c-157">On the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="ea47c-158">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="ea47c-158">On the new line, set the following values:</span></span>

    - <span data-ttu-id="ea47c-159">**Tafla:** *Númeraplötustaða staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="ea47c-159">**Table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="ea47c-160">**Afleidd tafla:** *Númeraplötustaða staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="ea47c-160">**Derived table:** *Location license plate positioning*</span></span>
    - <span data-ttu-id="ea47c-161">**Svæði:** *Númeraplötustaða*</span><span class="sxs-lookup"><span data-stu-id="ea47c-161">**Field:** *LP Position*</span></span>
    - <span data-ttu-id="ea47c-162">**Skilyrði:** *1*</span><span class="sxs-lookup"><span data-stu-id="ea47c-162">**Criteria:** *1*</span></span>

    <span data-ttu-id="ea47c-163">![Nýtt svið](media/LpPositionCriteria.png "Nýtt svið")</span><span class="sxs-lookup"><span data-stu-id="ea47c-163">![New range](media/LpPositionCriteria.png "New range")</span></span>

1. <span data-ttu-id="ea47c-164">Smelltu á **Í lagi** til að vista breytingarnar og loka fyrirspurnarritlinum.</span><span class="sxs-lookup"><span data-stu-id="ea47c-164">Select **OK** to confirm your changes and close the query editor.</span></span>

### <a name="set-up-sample-data-for-this-scenario"></a><span data-ttu-id="ea47c-165">Uppsetning sýnigagna fyrir þessar aðstæður</span><span class="sxs-lookup"><span data-stu-id="ea47c-165">Set up sample data for this scenario</span></span>

<span data-ttu-id="ea47c-166">Fyrir þessar aðstæður verður notandinn að skrá sig inn í farsímaforrit vöruhússins með því að nota starfsmann sem er settur upp fyrir vöruhús *61* til að vinna verk.</span><span class="sxs-lookup"><span data-stu-id="ea47c-166">For this scenario, the user must sign in to the warehousing mobile app by using a worker who is set up for warehouse *61* to perform work.</span></span> <span data-ttu-id="ea47c-167">Notandinn verður einnig að ljúka við færslur.</span><span class="sxs-lookup"><span data-stu-id="ea47c-167">The user must also complete transactions.</span></span>

<span data-ttu-id="ea47c-168">Vegna þess að eiginleikinn *Númeraplötustaða staðsetningar* bætir við nýju kennimerki fyrir númeraplötustöðu staðsetningar, verður þú fyrst að búa til einhver gögn til að styðja við aðstæðurnar.</span><span class="sxs-lookup"><span data-stu-id="ea47c-168">Because the *Location license plate positioning* feature adds a new identifier for license plate positions in a location, you must first create some data to support the scenario.</span></span>

#### <a name="spot-count-the-first-location"></a><span data-ttu-id="ea47c-169">Teljið fyrstu staðsetninguna á staðnum</span><span class="sxs-lookup"><span data-stu-id="ea47c-169">Spot-count the first location</span></span>

1. <span data-ttu-id="ea47c-170">Opnaðu farsímaforritið vöruhússins og skráðu þig inn á vöruhús *61*.</span><span class="sxs-lookup"><span data-stu-id="ea47c-170">Open the warehousing mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="ea47c-171">Opnaðu **Birgðir \> Telja á staðnum**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-171">Go to **Inventory \> Spot Counting**.</span></span>
1. <span data-ttu-id="ea47c-172">Opnaðu síðuna **Telja á staðnum** og stilltu svæðið **Staðsetning** á *01A01R1S1B*.</span><span class="sxs-lookup"><span data-stu-id="ea47c-172">On the **Spot Counting** page, set the **Location** field to *01A01R1S1B*.</span></span>
1. <span data-ttu-id="ea47c-173">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-173">Select **OK**.</span></span>

    <span data-ttu-id="ea47c-174">Síðan birtir staðsetninguna sem þú slóst inn.</span><span class="sxs-lookup"><span data-stu-id="ea47c-174">The page shows the location that you entered.</span></span> <span data-ttu-id="ea47c-175">Einnig birtast eftirfarandi skilaboð: „Staðsetningu lokið, bæta við nýrri númeraplötu eða vöru?“</span><span class="sxs-lookup"><span data-stu-id="ea47c-175">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="ea47c-176">Smelltu á **Uppfæra** til að bæta við talningu á staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="ea47c-176">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="ea47c-177">Á síðunni **Regluleg talning: Bæta við nýrri númeraplötu eða vöru** skaltu velja svæðið **Vara** og síðan slá inn gildið *A0001*.</span><span class="sxs-lookup"><span data-stu-id="ea47c-177">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0001*.</span></span>
1. <span data-ttu-id="ea47c-178">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-178">Select **OK**.</span></span>
1. <span data-ttu-id="ea47c-179">Á síðunni **Regluleg talning: Bæta við nýrri númeraplötu eða vöru** skaltu velja svæðið **Númeraplata** og síðan slá inn gildið *LP1001* (eða annað númeraplötunúmer að eigin vali).</span><span class="sxs-lookup"><span data-stu-id="ea47c-179">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1001* (or any other license plate number of your choice).</span></span>

    <span data-ttu-id="ea47c-180">Síðan **Regluleg talning: Bæta við nýrri númeraplötu eða vöru** sýnir **Númeraplötustöðu 1**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-180">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="ea47c-181">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-181">Select **OK**.</span></span>

    <span data-ttu-id="ea47c-182">Nú verður þú að tilgreina magn vörunnar sem talin er á númeraplötunni.</span><span class="sxs-lookup"><span data-stu-id="ea47c-182">You must now specify the quantity of the item that is counted on the license plate.</span></span>

1. <span data-ttu-id="ea47c-183">Stilltu svæðið **Magn** á *10*.</span><span class="sxs-lookup"><span data-stu-id="ea47c-183">Set the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="ea47c-184">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-184">Select **OK**.</span></span>

    <span data-ttu-id="ea47c-185">Síðan birtir staðsetninguna sem þú slóst inn.</span><span class="sxs-lookup"><span data-stu-id="ea47c-185">The page shows the location that you entered.</span></span> <span data-ttu-id="ea47c-186">Einnig birtast eftirfarandi skilaboð: „Staðsetningu lokið, bæta við nýrri númeraplötu eða vöru?“</span><span class="sxs-lookup"><span data-stu-id="ea47c-186">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="ea47c-187">Smelltu á **Uppfæra** til að bæta við annarri talningu á staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="ea47c-187">Select **Refresh** to add another count in the location.</span></span>
1. <span data-ttu-id="ea47c-188">Á síðunni **Regluleg talning: Bæta við nýrri númeraplötu eða vöru** skaltu velja svæðið **Vara** og síðan slá inn gildið *A0002*.</span><span class="sxs-lookup"><span data-stu-id="ea47c-188">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="ea47c-189">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-189">Select **OK**.</span></span>
1. <span data-ttu-id="ea47c-190">Á síðunni **Regluleg talning: Bæta við nýrri númeraplötu eða vöru** skaltu velja svæðið **Númeraplata** og síðan slá inn gildið *LP1002* (eða annað númeraplötunúmer að eigin vali, að því tilskyldu að númerið sé annað en númeraplötunúmerið sem þú tilgreindir áður).</span><span class="sxs-lookup"><span data-stu-id="ea47c-190">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1002* (or any other license plate number of your choice, provided that it differs from the license plate number that you specified earlier).</span></span>
1. <span data-ttu-id="ea47c-191">Breyttu stöðu númeraplötunnar með því að stilla reitinn **Númeraplötustaða** á *2*.</span><span class="sxs-lookup"><span data-stu-id="ea47c-191">Change the license plate position by setting the **LP Position** field to *2*.</span></span>
1. <span data-ttu-id="ea47c-192">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-192">Select **OK**.</span></span>
1. <span data-ttu-id="ea47c-193">Tilgreindu magn vörunnar sem talin er á númeraplötunni með því að stilla svæðið **Magn** á *10*.</span><span class="sxs-lookup"><span data-stu-id="ea47c-193">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="ea47c-194">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-194">Select **OK**.</span></span>

    <span data-ttu-id="ea47c-195">Síðan birtir staðsetninguna sem þú slóst inn.</span><span class="sxs-lookup"><span data-stu-id="ea47c-195">The page shows the location that you entered.</span></span> <span data-ttu-id="ea47c-196">Einnig birtast eftirfarandi skilaboð: „Staðsetningu lokið, bæta við nýrri númeraplötu eða vöru?“</span><span class="sxs-lookup"><span data-stu-id="ea47c-196">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="ea47c-197">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-197">Select **OK**.</span></span>

<span data-ttu-id="ea47c-198">Vinnu er nú lokið.</span><span class="sxs-lookup"><span data-stu-id="ea47c-198">Work is now completed.</span></span>

#### <a name="spot-count-the-second-location"></a><span data-ttu-id="ea47c-199">Telja aðra staðsetningu á staðnum</span><span class="sxs-lookup"><span data-stu-id="ea47c-199">Spot-count the second location</span></span>

1. <span data-ttu-id="ea47c-200">Opnaðu síðuna **Telja á staðnum** og stilltu svæðið **Staðsetning** á *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="ea47c-200">On the **Spot Counting** page, set the **Location** field to *01A01R1S2B*.</span></span>
1. <span data-ttu-id="ea47c-201">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-201">Select **OK**.</span></span>

    <span data-ttu-id="ea47c-202">Síðan birtir staðsetninguna sem þú slóst inn.</span><span class="sxs-lookup"><span data-stu-id="ea47c-202">The page shows the location that you entered.</span></span> <span data-ttu-id="ea47c-203">Einnig birtast eftirfarandi skilaboð: „Staðsetningu lokið, bæta við nýrri númeraplötu eða vöru?“</span><span class="sxs-lookup"><span data-stu-id="ea47c-203">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="ea47c-204">Smelltu á **Uppfæra** til að bæta við talningu á staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="ea47c-204">Select **Refresh** to add a count in the location.</span></span>
1. <span data-ttu-id="ea47c-205">Á síðunni **Regluleg talning: Bæta við nýrri númeraplötu eða vöru** skaltu velja svæðið **Vara** og síðan slá inn gildið *A0002*.</span><span class="sxs-lookup"><span data-stu-id="ea47c-205">On the **Cycle Count: Add New LP or Item** page, select the **Item** field, and then enter the value *A0002*.</span></span>
1. <span data-ttu-id="ea47c-206">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-206">Select **OK**.</span></span>
1. <span data-ttu-id="ea47c-207">Á síðunni **Regluleg talning: Bæta við nýrri númeraplötu eða vöru** skaltu velja svæðið **Númeraplata** og síðan slá inn gildið *LP1003* (eða annað númeraplötunúmer að eigin vali, að því tilskyldu að númerið sé annað en bæði númeraplötunúmerin sem þú tilgreindir í ferlinu hér á undan).</span><span class="sxs-lookup"><span data-stu-id="ea47c-207">On the **Cycle Count: Add New LP or Item** page, select the **LP** field, and then enter the value *LP1003* (or any other license plate number of your choice, provided that it differs from the both the license plate numbers that you specified in the previous procedure).</span></span>

    <span data-ttu-id="ea47c-208">Síðan **Regluleg talning: Bæta við nýrri númeraplötu eða vöru** sýnir **Númeraplötustöðu 1**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-208">The **Cycle Count: Add New LP or Item** page shows **License Plate Position 1**.</span></span>

1. <span data-ttu-id="ea47c-209">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-209">Select **OK**.</span></span>
1. <span data-ttu-id="ea47c-210">Tilgreindu magn vörunnar sem talin er á númeraplötunni með því að stilla svæðið **Magn** á *10*.</span><span class="sxs-lookup"><span data-stu-id="ea47c-210">Specify the quantity of the item that is counted on the license plate by setting the **Qty** field to *10*.</span></span>
1. <span data-ttu-id="ea47c-211">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-211">Select **OK**.</span></span>

    <span data-ttu-id="ea47c-212">Síðan birtir staðsetninguna sem þú slóst inn.</span><span class="sxs-lookup"><span data-stu-id="ea47c-212">The page shows the location that you entered.</span></span> <span data-ttu-id="ea47c-213">Einnig birtast eftirfarandi skilaboð: „Staðsetningu lokið, bæta við nýrri númeraplötu eða vöru?“</span><span class="sxs-lookup"><span data-stu-id="ea47c-213">It also shows the following message: "Location complete, add new LP or Item?"</span></span>

1. <span data-ttu-id="ea47c-214">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-214">Select **OK**.</span></span>

<span data-ttu-id="ea47c-215">Vinnu er nú lokið.</span><span class="sxs-lookup"><span data-stu-id="ea47c-215">Work is now completed.</span></span>

#### <a name="work-details"></a><span data-ttu-id="ea47c-216">Upplýsingar um vinnu</span><span class="sxs-lookup"><span data-stu-id="ea47c-216">Work details</span></span>

> [!NOTE]
> <span data-ttu-id="ea47c-217">Talningar á staðnum í farsímaforritinu stofna reglulegar talningar í Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ea47c-217">Spot counts from the mobile app create cycle counting work in Microsoft Dynamics 365.</span></span> <span data-ttu-id="ea47c-218">Vinnan krefst þess að talningar séu samþykktar áður en þær eru bókaðar í birgðir.</span><span class="sxs-lookup"><span data-stu-id="ea47c-218">The work requires that the counts be accepted before they are posted to inventory.</span></span>

1. <span data-ttu-id="ea47c-219">Innskráning í Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ea47c-219">Sign in to Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="ea47c-220">Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnu**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-220">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="ea47c-221">Finndu línur með eftirfarandi gildi á flipanum **Yfirlit**:</span><span class="sxs-lookup"><span data-stu-id="ea47c-221">On the **Overview** tab, look for the lines that have the following values:</span></span>

    - <span data-ttu-id="ea47c-222">**Gerð verkpöntunar:** *Regluleg talning*</span><span class="sxs-lookup"><span data-stu-id="ea47c-222">**Work order type:** *Cycle counting*</span></span>
    - <span data-ttu-id="ea47c-223">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="ea47c-223">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="ea47c-224">**Vinnustaða:** *Bíður yfirferðar*</span><span class="sxs-lookup"><span data-stu-id="ea47c-224">**Work status:** *Pending review*</span></span>

    <span data-ttu-id="ea47c-225">Stofna ætti tvö vinnuauðkenni fyrir þessar línur.</span><span class="sxs-lookup"><span data-stu-id="ea47c-225">Two work IDs should have been created for these lines.</span></span> <span data-ttu-id="ea47c-226">Staðfesta verður talningar fyrir bæði þessi vinnuauðkenni.</span><span class="sxs-lookup"><span data-stu-id="ea47c-226">The counts for both these work IDs must be accepted.</span></span>

1. <span data-ttu-id="ea47c-227">Veldu fyrsta vinnuauðkennið fyrir gerð verkbeiðni *Reglulegrar talningar*.</span><span class="sxs-lookup"><span data-stu-id="ea47c-227">In the grid, select the first work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="ea47c-228">Á Aðgerðasvæðinu á flipanum **Vinna** í hópnum **Vinna** velur þú **Regluleg talning**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-228">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="ea47c-229">Tvær línur birtast, ein fyrir hverja vöru fyrir sig og númeraplata.</span><span class="sxs-lookup"><span data-stu-id="ea47c-229">Two lines are shown, one for each item and license plate.</span></span> <span data-ttu-id="ea47c-230">Gildin í svæðunum **Talið magn**, **Staðsetning**, **Númeraplata** og **Vara** ættu að passa við talningarfærslurnar sem þú bjóst til í fartækinu.</span><span class="sxs-lookup"><span data-stu-id="ea47c-230">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span> <span data-ttu-id="ea47c-231">Ef einhver af þessum reitum er ekki sýnilegur skaltu smella á **Sýna víddir** á aðgerðasvæðinu til að bæta þeim við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="ea47c-231">If any of these fields aren't visible, select **Display dimensions** on the Action Pane to add them to the grid.</span></span>

1. <span data-ttu-id="ea47c-232">Veldu báðar línurnar.</span><span class="sxs-lookup"><span data-stu-id="ea47c-232">Select both lines.</span></span>
1. <span data-ttu-id="ea47c-233">Veldu **Samþykkja talningu** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="ea47c-233">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="ea47c-234">Skilaboðin „Bókar - Færslubók“ birtast.</span><span class="sxs-lookup"><span data-stu-id="ea47c-234">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="ea47c-235">Smelltu á **Upplýsingar um skilaboð** til að skoða færslubókarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="ea47c-235">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="ea47c-236">Lokaðu upplýsingunum um skilaboð.</span><span class="sxs-lookup"><span data-stu-id="ea47c-236">Close the message details.</span></span>
1. <span data-ttu-id="ea47c-237">Endurhladdu síðuna **Vinna**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-237">Refresh the **Work** page.</span></span>

    <span data-ttu-id="ea47c-238">Fyrsta vinnuauðkenninu hefur verið lokað og er ekki lengur sýnt.</span><span class="sxs-lookup"><span data-stu-id="ea47c-238">The first work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="ea47c-239">Smelltu í gátreitinn **Sýna lokna** fyrir ofan hnitanetið til að skoða vinnu sem er lokið.</span><span class="sxs-lookup"><span data-stu-id="ea47c-239">To view closed work, select the **Show closed** check box above the grid.</span></span>

    <span data-ttu-id="ea47c-240">Þú verður nú að samþykkja vinnuna fyrir númeraplötuna í staðsetningu *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="ea47c-240">You will now accept the work for the license plate in the *01A01R1S2B* location.</span></span>

1. <span data-ttu-id="ea47c-241">Smelltu á flipann **Yfirlit** og veldu annað vinnuauðkenni fyrir gerð verkbeiðni *Reglulegrar talningar*.</span><span class="sxs-lookup"><span data-stu-id="ea47c-241">On the **Overview** tab, select the second work ID for the *Cycle counting* work order type.</span></span>
1. <span data-ttu-id="ea47c-242">Á Aðgerðasvæðinu á flipanum **Vinna** í hópnum **Vinna** velur þú **Regluleg talning**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-242">On the Action Pane, on **Work** tab, in the **Work** group, select **Cycle counting**.</span></span>

    <span data-ttu-id="ea47c-243">Ein lína birtist fyrir vöruna og númeraplötuna.</span><span class="sxs-lookup"><span data-stu-id="ea47c-243">One line is shown, for the item and license plate.</span></span> <span data-ttu-id="ea47c-244">Gildin í svæðunum **Talið magn**, **Staðsetning**, **Númeraplata** og **Vara** ættu að passa við talningarfærslurnar sem þú bjóst til í fartækinu.</span><span class="sxs-lookup"><span data-stu-id="ea47c-244">The values in the **Counted quantity**, **Location**, **License plate**, and **Item** fields should match the count entries that you created on the mobile device.</span></span>

1. <span data-ttu-id="ea47c-245">Veldu línuna.</span><span class="sxs-lookup"><span data-stu-id="ea47c-245">Select the line.</span></span>
1. <span data-ttu-id="ea47c-246">Veldu **Samþykkja talningu** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="ea47c-246">On the Action Pane, select **Accept count**.</span></span>
1. <span data-ttu-id="ea47c-247">Skilaboðin „Bókar - Færslubók“ birtast.</span><span class="sxs-lookup"><span data-stu-id="ea47c-247">You receive a "Posting - Journal" message.</span></span> <span data-ttu-id="ea47c-248">Smelltu á **Upplýsingar um skilaboð** til að skoða færslubókarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="ea47c-248">Select **Message details** to view the posted journal number.</span></span>
1. <span data-ttu-id="ea47c-249">Lokaðu upplýsingunum um skilaboð.</span><span class="sxs-lookup"><span data-stu-id="ea47c-249">Close the message details.</span></span>
1. <span data-ttu-id="ea47c-250">Endurhladdu síðuna **Vinna**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-250">Refresh the **Work** page.</span></span>

    <span data-ttu-id="ea47c-251">Öðru vinnuauðkenninu hefur verið lokað og er ekki lengur sýnt.</span><span class="sxs-lookup"><span data-stu-id="ea47c-251">The second work ID has been closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="ea47c-252">Smelltu í gátreitinn **Sýna lokna** fyrir ofan hnitanetið til að skoða vinnu sem er lokið.</span><span class="sxs-lookup"><span data-stu-id="ea47c-252">To view closed work, select the **Show closed** check box above the grid.</span></span>

#### <a name="on-hand-by-location"></a><span data-ttu-id="ea47c-253">Á lager eftir birgðageymslu</span><span class="sxs-lookup"><span data-stu-id="ea47c-253">On-hand by location</span></span>

1. <span data-ttu-id="ea47c-254">Opnaðu **Vöruhúsakerfi \> Fyrirpurnir og skýrslur \> Á lager eftir staðsetningu**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-254">Go to **Warehouse management \> Inquiries and reports \> On-hand by location**.</span></span>
1. <span data-ttu-id="ea47c-255">Stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="ea47c-255">Set the following values:</span></span>

    - <span data-ttu-id="ea47c-256">**Svæði:** *6*</span><span class="sxs-lookup"><span data-stu-id="ea47c-256">**Site:** *6*</span></span>
    - <span data-ttu-id="ea47c-257">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="ea47c-257">**Warehouse:** *61*</span></span>
    - <span data-ttu-id="ea47c-258">**Uppfæra á öllum staðsetningum:** *Já*</span><span class="sxs-lookup"><span data-stu-id="ea47c-258">**Refresh across locations:** *Yes*</span></span>

1. <span data-ttu-id="ea47c-259">Taktu eftir að tvær númeraplötur eru fyrir staðsetningu *01A01R1S1B*:</span><span class="sxs-lookup"><span data-stu-id="ea47c-259">Notice that location *01A01R1S1B* has two license plates:</span></span>

    - <span data-ttu-id="ea47c-260">**A0001**, þar sem svæðið **Númeraplötustaður** er stilltur á *1*</span><span class="sxs-lookup"><span data-stu-id="ea47c-260">**A0001**, where the **LP Position** field is set to *1*</span></span>
    - <span data-ttu-id="ea47c-261">**A0002**, þar sem svæðið **Númeraplötustaður** er stilltur á *2*</span><span class="sxs-lookup"><span data-stu-id="ea47c-261">**A0002**, where the **LP Position** field is set to *2*</span></span>

1. <span data-ttu-id="ea47c-262">Taktu eftir því að ein númeraplata er fyrir staðsetningu *01A01R1S2B*:</span><span class="sxs-lookup"><span data-stu-id="ea47c-262">Notice that location *01A01R1S2B* has one license plate:</span></span>

    - <span data-ttu-id="ea47c-263">**A0002**, þar sem svæðið **Númeraplötustaður** er stilltur á *1*</span><span class="sxs-lookup"><span data-stu-id="ea47c-263">**A0002**, where the **LP Position** field is set to *1*</span></span>

### <a name="sales-order-scenario"></a><span data-ttu-id="ea47c-264">Aðstæður sölupöntunar</span><span class="sxs-lookup"><span data-stu-id="ea47c-264">Sales order scenario</span></span>

<span data-ttu-id="ea47c-265">Nú þegar lokið er við að setja upp eiginleikann *Númeraplötustaða staðsetningar* og birgðunum hefur verið sett á svið verður þú að búa til sölupöntun til að búa til tiltekt sem mun beina vöruhússtarfsmanni að taka til vöru *A0002* úr birgðastaðsetningunni þar sem auðkenni vörubrettis er í stöðu *1*.</span><span class="sxs-lookup"><span data-stu-id="ea47c-265">Now that the *Location license plate positioning* feature has been set up, and the inventory has been staged, you must create a sales order to generate picking work that will direct the warehouse worker to pick item *A0002* from the inventory location where the pallet ID is in position *1*.</span></span>

1. <span data-ttu-id="ea47c-266">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-266">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="ea47c-267">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-267">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="ea47c-268">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="ea47c-268">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="ea47c-269">**Viðskiptavinalykill:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="ea47c-269">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="ea47c-270">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="ea47c-270">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="ea47c-271">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-271">Select **OK**.</span></span>
1. <span data-ttu-id="ea47c-272">Nýrri línu er bætt við hnitanetið á flýtiflipanum **Sölupöntunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-272">A new line is added to the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="ea47c-273">Stilltu eftirfarandi gildi á þessari nýju línu:</span><span class="sxs-lookup"><span data-stu-id="ea47c-273">On this new line, set the following values:</span></span>

    - <span data-ttu-id="ea47c-274">**Vörunúmer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="ea47c-274">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="ea47c-275">**Magn:** *1*</span><span class="sxs-lookup"><span data-stu-id="ea47c-275">**Quantity:** *1*</span></span>

1. <span data-ttu-id="ea47c-276">Á valmyndinni **Birgðir** fyrir ofan hnitanetið smellir þú á **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-276">On the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="ea47c-277">Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá birgðir fyrir pöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="ea47c-277">On the **Reservation** page, on the Action Pane, select **Reserve lot** to reserve inventory for the order line.</span></span>
1. <span data-ttu-id="ea47c-278">Lokaðu síðunni **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-278">Close the **Reservation** page.</span></span>
1. <span data-ttu-id="ea47c-279">Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Aðgerðir**, velurðu **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-279">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="ea47c-280">Þú færð upplýsingaboð sem tilgreina bylgjuauðkenni og sendingarkenni sem voru búin til fyrir pöntunina.</span><span class="sxs-lookup"><span data-stu-id="ea47c-280">You receive an informational message that indicates the wave ID and shipment ID that were created for the order.</span></span>

1. <span data-ttu-id="ea47c-281">Á flýtiflipanum **Sölupöntunarlínur** á valmyndinni **Vöruhús** fyrir ofan hnitanetið smellir þú á **Upplýsingar um vinnu**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-281">On the **Sales order lines** FastTab, on the **Warehouse** menu above the grid, select **Work details**.</span></span>
1. <span data-ttu-id="ea47c-282">Síðan opnast síðan **Vinna** og sýnir vinnuna sem stofnuð var fyrir sölulínuna.</span><span class="sxs-lookup"><span data-stu-id="ea47c-282">The **Work** page appears and shows the work that was created for the sales line.</span></span> <span data-ttu-id="ea47c-283">Skráið niður vinnuauðkennið sem birtist.</span><span class="sxs-lookup"><span data-stu-id="ea47c-283">Make a note of the work ID that is shown.</span></span>

### <a name="sales-picking-scenario"></a><span data-ttu-id="ea47c-284">Aðstæður sölutiltektar</span><span class="sxs-lookup"><span data-stu-id="ea47c-284">Sales picking scenario</span></span>

1. <span data-ttu-id="ea47c-285">Opnaðu farsímaforritið og skráðu þig inn á vöruhús *61*.</span><span class="sxs-lookup"><span data-stu-id="ea47c-285">Open the mobile app, and sign in to warehouse *61*.</span></span>
1. <span data-ttu-id="ea47c-286">Opnaðu **Á útleið \> Sölutiltekt**.</span><span class="sxs-lookup"><span data-stu-id="ea47c-286">Go to **Outbound \> Sales picking**.</span></span>
1. <span data-ttu-id="ea47c-287">Á síðunni **Skanna vinnuauðkenni / kenni númeraplötu** skaltu smella á svæðið **Auðkenni** og síðan slá inn auðkenni sölulínunnar.</span><span class="sxs-lookup"><span data-stu-id="ea47c-287">On the **Scan a work ID / license plate ID** page, select the **ID** field, and then enter the work ID from the sales line.</span></span>
1. <span data-ttu-id="ea47c-288">Taktu eftir að tiltektin segir þér til að taka til vöru *A0002* úr staðsetningu *01A01R1S2B*.</span><span class="sxs-lookup"><span data-stu-id="ea47c-288">Notice that the picking work directs you to pick item *A0002* from location *01A01R1S2B*.</span></span> <span data-ttu-id="ea47c-289">Þú færð þessar leiðbeiningar vegna þess að vara *A0002* er á númeraplötunni sem er í stöðu *1* á þeirri staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="ea47c-289">You receive this instruction because item *A0002* is on a license plate that is in position *1* in that location.</span></span>

    <span data-ttu-id="ea47c-290">![Staðsetning stöðu 1](media/LocationLicensePlatePositioning.png "Staðsetning stöðu 1")</span><span class="sxs-lookup"><span data-stu-id="ea47c-290">![Position 1 location](media/LocationLicensePlatePositioning.png "Position 1 location")</span></span>

1. <span data-ttu-id="ea47c-291">Sláðu inn auðkenni númeraplötunnar sem þú bjóst til fyrir staðsetningu og fylgdu síðan leiðbeiningunum til að velja sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="ea47c-291">Enter the license plate ID that you created for the location, and then follow the prompts to pick the sales order.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]