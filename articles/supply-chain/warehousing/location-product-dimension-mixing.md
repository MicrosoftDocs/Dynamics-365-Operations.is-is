---
title: Blöndun á afurðarvídd staðsetningar
description: Þetta efnisatriði inniheldur upplýsingar um blöndun á afurðarvídd staðsetningar. Þessi virkni staðsetningarforstillingar hjálpar til við að bæta staðsetningarstjórnun þegar afurðarafbrigði eða afurðir með víddir eru notaðar, svo sem í tískuiðnaðinum. Það gerir þér kleift að ákveða hvort hægt sé að blanda stillingum, litum, stílum og stærðum fyrir tiltekna staðsetningarforstillingu, eða hvort hægt sé að setja eina af þessum víddum eða samsetningu þeirra á sömu staðsetninguna.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: c4e42864bfde9ed0650a88961b5a71b33b34c89d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004603"
---
# <a name="location-product-dimension-mixing"></a><span data-ttu-id="16273-105">Blöndun á afurðarvídd staðsetningar</span><span class="sxs-lookup"><span data-stu-id="16273-105">Location product dimension mixing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="16273-106">Blöndun á afurðarvídd staðsetningar er staðsetningarforstilling sem hjálpar til við að bæta staðsetningarstjórnun þegar afurðarafbrigði eða afurðir með víddir eru notaðar, svo sem í tískuiðnaðinum.</span><span class="sxs-lookup"><span data-stu-id="16273-106">Location product dimension mixing is location profile functionality that helps improve location management when product variants or products that have dimensions are used, such as in the fashion industry.</span></span> <span data-ttu-id="16273-107">Það gerir þér kleift að ákveða hvort hægt sé að blanda stillingum, litum, stílum og stærðum fyrir tiltekna staðsetningarforstillingu, eða hvort hægt sé að setja eina af þessum víddum eða samsetningu þeirra á sömu staðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="16273-107">It lets you decide whether configurations, colors, styles, and sizes can be mixed for a specific location profile, or whether just one of these dimensions or a combination of them can be put to the same location.</span></span>

## <a name="turn-on-the-location-product-dimension-mixing-feature"></a><span data-ttu-id="16273-108">Kveikja á eiginleika blöndunar á afurðarvídd staðsetningar</span><span class="sxs-lookup"><span data-stu-id="16273-108">Turn on the Location product dimension mixing feature</span></span>

<span data-ttu-id="16273-109">Áður en þú getur notað blöndun á afurðarvídd staðsetningar verður að kveikja á eiginleikanum í kerfinu þínu.</span><span class="sxs-lookup"><span data-stu-id="16273-109">Before you can use location product dimension mixing, the feature must be turned on in your system.</span></span> <span data-ttu-id="16273-110">Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="16273-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="16273-111">Þar er eiginleikinn sýndur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="16273-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="16273-112">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="16273-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="16273-113">**Heiti eiginleika:** *Blöndun á afurðarvídd staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="16273-113">**Feature name:** *Location product dimension mixing*</span></span>

## <a name="setup"></a><span data-ttu-id="16273-114">Setja upp</span><span class="sxs-lookup"><span data-stu-id="16273-114">Setup</span></span>

<span data-ttu-id="16273-115">Hver staðsetning í vöruhúsi verður að hafa staðsetningarforstillingu tengda sem lýsir eiginleikum staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="16273-115">Every location in the warehouse needs to have a location profile associated with it that describes the properties of the location.</span></span> <span data-ttu-id="16273-116">Þess vegna verður hægt að blanda vöruvídd allra staðsetningar sem nota sömu staðsetningarforstillingu eftir að hún hefur verið sett upp.</span><span class="sxs-lookup"><span data-stu-id="16273-116">Therefore, all locations that use the same location profile will be able to allow product dimension mixing after it has been set up.</span></span>

### <a name="configure-location-profiles-to-allow-product-dimension-mixing"></a><span data-ttu-id="16273-117">Stilla staðsetningarforstillingar til að leyfa blöndun á afurðarvídd</span><span class="sxs-lookup"><span data-stu-id="16273-117">Configure location profiles to allow product dimension mixing</span></span>

1. <span data-ttu-id="16273-118">Fara í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Forstillingar staðsetningar**.</span><span class="sxs-lookup"><span data-stu-id="16273-118">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="16273-119">Smelltu á **MAGN** á lista staðsetningarforstillinga.</span><span class="sxs-lookup"><span data-stu-id="16273-119">In the list of location profiles, select **BULK**.</span></span>
1. <span data-ttu-id="16273-120">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="16273-120">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="16273-121">Á flýtiflipanum **Almennt** skaltu stilla valkostinn **Virkja tiltekna blöndun á afurðarvídd staðsetningar** á *Já*.</span><span class="sxs-lookup"><span data-stu-id="16273-121">On the **General** FastTab, set the **Enable location product dimension specific mixing** option to *Yes*.</span></span>

    > [!NOTE]
    > <span data-ttu-id="16273-122">Þú getur aðeins stillt valkostinn á *Já* ef valkosturinn **Leyfa blandaðar afurðir** er stilltur á *Nei*.</span><span class="sxs-lookup"><span data-stu-id="16273-122">You can set this option to *Yes* only if the **Allow mixed items** option is set to *No*.</span></span>

1. <span data-ttu-id="16273-123">Á flýtiflipanum **Leyfð blöndun á afurðarvídd** skaltu stilla valkostinn **Stærð** á *Já*.</span><span class="sxs-lookup"><span data-stu-id="16273-123">On the **Allowed product dimension mixing** FastTab, set the **Size** option to *Yes*.</span></span> <span data-ttu-id="16273-124">Við aðstæðurnar sem lýst er í þessu efnisatriði er aðeins hægt að blanda afurðum sem hafa mismunandi **Stærðarvíddir**.</span><span class="sxs-lookup"><span data-stu-id="16273-124">In the scenario that is described in this topic, mixing can be done only for products that have different **Size** dimensions.</span></span> <span data-ttu-id="16273-125">Aðrir valkostir eru einnig í boði.</span><span class="sxs-lookup"><span data-stu-id="16273-125">However, other options are also available.</span></span>
1. <span data-ttu-id="16273-126">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="16273-126">Select **Save**.</span></span>

### <a name="create-a-new-product-master-and-product-variants"></a><span data-ttu-id="16273-127">Stofna nýtt afurðarsniðmát og ný afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="16273-127">Create a new product master and product variants</span></span>

1. <span data-ttu-id="16273-128">Opna **upplýsingar um afurðastjórnun \> Afurðir \> Afurðarsniðmát**.</span><span class="sxs-lookup"><span data-stu-id="16273-128">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="16273-129">Á aðgerðasvæðinu skal velja **Nýtt** til að stofna nýtt afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="16273-129">On the Action Pane, select **New** to create a product master.</span></span>
1. <span data-ttu-id="16273-130">Sláið inn eftirfarandi gildi í svarglugganum **Ný afurð**:</span><span class="sxs-lookup"><span data-stu-id="16273-130">In the **New product** dialog box, set the following values:</span></span>

    - <span data-ttu-id="16273-131">**Gerð afurðar:** *Afurð*</span><span class="sxs-lookup"><span data-stu-id="16273-131">**Product type:** *Item*</span></span>
    - <span data-ttu-id="16273-132">**Undirgerð afurðar:** *Afurðarsniðmát*</span><span class="sxs-lookup"><span data-stu-id="16273-132">**Product subtype:** *Product master*</span></span>
    - <span data-ttu-id="16273-133">**Afurðarnúmer:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="16273-133">**Product number:** *B0001*</span></span>
    - <span data-ttu-id="16273-134">**Afurðarheiti:** *B0001 Stærð*</span><span class="sxs-lookup"><span data-stu-id="16273-134">**Product name:** *B0001 Size*</span></span>
    - <span data-ttu-id="16273-135">**Afurðavíddaflokkur:** *Stærð*</span><span class="sxs-lookup"><span data-stu-id="16273-135">**Product dimension group:** *Size*</span></span>
    - <span data-ttu-id="16273-136">**Skilgreiningartækni:** *Forskilgreint afbrigði*</span><span class="sxs-lookup"><span data-stu-id="16273-136">**Configuration technology:** *Predefined variant*</span></span>

1. <span data-ttu-id="16273-137">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="16273-137">Select **OK**.</span></span>
1. <span data-ttu-id="16273-138">Stilltu eftirfarandi gildi á síðunni **Upplýsingar um afurð** á flýtiflipanum **Almennt**:</span><span class="sxs-lookup"><span data-stu-id="16273-138">On the **Product details** page, on the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="16273-139">**Búa til afbrigði sjálfkrafa** *Já*</span><span class="sxs-lookup"><span data-stu-id="16273-139">**Generate variants automatically:** *Yes*</span></span>
    - <span data-ttu-id="16273-140">**Stærðarflokkur:** *CASUALDHIR*</span><span class="sxs-lookup"><span data-stu-id="16273-140">**Size group:** *CASUALDHIR*</span></span>

1. <span data-ttu-id="16273-141">Til að skoða forskilgreind afbrigði skaltu velja **Afurðarafbrigði** á aðgerðarsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="16273-141">To view the predefined variants, on the Action Pane, select **Product variants**.</span></span>

    <span data-ttu-id="16273-142">Síðan **Afurðarafbrigði** opnast og sýnir lista yfir afbrigði grunnstillingar stærðarflokksins.</span><span class="sxs-lookup"><span data-stu-id="16273-142">The **Product variants** page appears and shows a list of variants from the configuration of the size group.</span></span>

### <a name="release-products-to-the-usmf-company"></a><span data-ttu-id="16273-143">Losa afurðir til USMF-fyrirtækisins</span><span class="sxs-lookup"><span data-stu-id="16273-143">Release products to the USMF company</span></span>

1. <span data-ttu-id="16273-144">Smelltu á **Losa afurðir** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="16273-144">On the Action Pane, select **Release products**.</span></span>
1. <span data-ttu-id="16273-145">Staðfestu á **Velja afurðir til losunar** að afurðarnúmer *B0001* sé á listanum og smelltu síðan á **Áfram**.</span><span class="sxs-lookup"><span data-stu-id="16273-145">On the **Select products to release** page, confirm that product number *B0001* is in the list, and then select **Next**.</span></span>
1. <span data-ttu-id="16273-146">Smelltu á **Áfram** til að staðfesta afurðarafbrigði sem á að losa um.</span><span class="sxs-lookup"><span data-stu-id="16273-146">Select **Next** to confirm the product variants to release.</span></span>
1. <span data-ttu-id="16273-147">Á síðunni **Velja fyrirtæki sem á að losa til** skaltu smella á *USMF* og síðan smella á **Áfram** til að staðfesta valið.</span><span class="sxs-lookup"><span data-stu-id="16273-147">On the **Select companies to release to** page, select *USMF*, and then select **Next** to confirm the selection.</span></span>
1. <span data-ttu-id="16273-148">Á síðunni **Staðfesta val** smellir þú á **Ljúka** til að losa um.</span><span class="sxs-lookup"><span data-stu-id="16273-148">On the **Confirm selection** page, select **Finish** to complete the release.</span></span>

    <span data-ttu-id="16273-149">Þú færð skilaboðin „Aðgerð er lokið“.</span><span class="sxs-lookup"><span data-stu-id="16273-149">You receive an "Operation completed" message.</span></span>

### <a name="update-a-released-product-in-the-usmf-company"></a><span data-ttu-id="16273-150">Uppfæra afurð sem losað var um í USMF-fyrirtækinu</span><span class="sxs-lookup"><span data-stu-id="16273-150">Update a released product in the USMF company</span></span>

1. <span data-ttu-id="16273-151">Gakktu úr skugga um að þú sért skráð(ur) inn á **USMF**-fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="16273-151">Make sure that you're signed in to the **USMF** company.</span></span>
1. <span data-ttu-id="16273-152">Opnaðu **Afurðaupplýsingastjórnun \> Afurðir \> Losaðar afurðir** til að ljúka við að búa til losuðu afurðina.</span><span class="sxs-lookup"><span data-stu-id="16273-152">Go to **Product information management \> Products \> Released products** to finish creating the released product.</span></span>
1. <span data-ttu-id="16273-153">Leitaðu að og veldu vörunúmer *B0001* til að opna síðuna **Upplýsingasíða um losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="16273-153">Find and select item number *B0001* to open the **Released product details** page.</span></span>
1. <span data-ttu-id="16273-154">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="16273-154">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="16273-155">Á flýtiflipanum **Almennt** skal gæta þess að stilla svæðið **Vörulíkanaflokkur** á *FIFO*.</span><span class="sxs-lookup"><span data-stu-id="16273-155">On the **General** FastTab, make sure that the **Item model group** field is set to *FIFO*.</span></span>
1. <span data-ttu-id="16273-156">Á aðgerðasvæðinu, á flipanum **Afurð** í hópnum **Uppsetning** skal velja **Víddaflokka**.</span><span class="sxs-lookup"><span data-stu-id="16273-156">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Dimension groups**.</span></span>
1. <span data-ttu-id="16273-157">Stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="16273-157">Set the following values:</span></span>

    - <span data-ttu-id="16273-158">**Geymsluvíddarflokkur:** *Afurð*</span><span class="sxs-lookup"><span data-stu-id="16273-158">**Storage dimension group:** *Ware*</span></span>
    - <span data-ttu-id="16273-159">**Rakningarvíddarflokkur:** *Enginn*</span><span class="sxs-lookup"><span data-stu-id="16273-159">**Tracking dimension group:** *None*</span></span>

1. <span data-ttu-id="16273-160">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="16273-160">Select **OK**.</span></span>
1. <span data-ttu-id="16273-161">Á aðgerðasvæðinu, á flipanum **Afurð** í hópnum **Uppsetning** skal velja **Frátekningarstigveldi**.</span><span class="sxs-lookup"><span data-stu-id="16273-161">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Reservation hierarchy**.</span></span>
1. <span data-ttu-id="16273-162">Stilltu svæðið **Frátekningarstigveldi** á *Sjálfgefið* og smelltu síðan á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="16273-162">Set the **Reservation hierarchy** field to *Default*, and then select **OK**.</span></span>
1. <span data-ttu-id="16273-163">Athugaðu á flýtiflipanum **Almennt** í hlutanum **Stjórnun** hvort að valkostir þinir hafi verið uppfærðir.</span><span class="sxs-lookup"><span data-stu-id="16273-163">On the **General** FastTab, in the **Administration** section, notice that your selections have been updated.</span></span>
1. <span data-ttu-id="16273-164">Í flýtiflipanum **Kaup** í svæðinu **Verð** slærðu inn *10*.</span><span class="sxs-lookup"><span data-stu-id="16273-164">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="16273-165">Á flýtiflipanum **Stjórna kostnaði**, í reitnum **Vöruflokkur** skal slá inn *Hljóð*.</span><span class="sxs-lookup"><span data-stu-id="16273-165">On the **Manage costs** FastTab, in the **Item group** field, enter *Audio*.</span></span>
1. <span data-ttu-id="16273-166">Í flýtiflipanum **Kaup** í svæðinu **Verð** slærðu inn *10*.</span><span class="sxs-lookup"><span data-stu-id="16273-166">On the **Purchase** FastTab, in the **Price** field, enter *10*.</span></span>
1. <span data-ttu-id="16273-167">Á flýtiflipanum **Vöruhús** á svæðinu **Auðkenni röðunarflokks einingar** skaltu slá inn *ea*.</span><span class="sxs-lookup"><span data-stu-id="16273-167">On the **Warehouse** FastTab, in the **Unit sequence group ID** field, enter *ea*.</span></span>
1. <span data-ttu-id="16273-168">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="16273-168">Select **Save**.</span></span>

### <a name="create-a-location-directive"></a><span data-ttu-id="16273-169">Stofna staðsetningarleiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="16273-169">Create a location directive</span></span>

1. <span data-ttu-id="16273-170">Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.</span><span class="sxs-lookup"><span data-stu-id="16273-170">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="16273-171">Í svæðinu **Gerð verkbeiðni** í vinstri glugganum velur þú *Innkaupapantanir*.</span><span class="sxs-lookup"><span data-stu-id="16273-171">In the left pane, in the **Work order type** field, select *Purchase orders*.</span></span>
1. <span data-ttu-id="16273-172">Veldu staðsetningarleiðbeiningar sem kallast *24 PO Direct* á listanum.</span><span class="sxs-lookup"><span data-stu-id="16273-172">In the list, select the location directive that is named *24 PO Direct*.</span></span>
1. <span data-ttu-id="16273-173">Á flýtiflipanum **Aðgerðir staðsetningarleiðbeininga** velur þú **Ný** til að bæta við nýrri línu í hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="16273-173">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="16273-174">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="16273-174">On the new line, set the following values:</span></span>

    - <span data-ttu-id="16273-175">**Raðnúmer:** *1*</span><span class="sxs-lookup"><span data-stu-id="16273-175">**Sequence number:** *1*</span></span>

        <span data-ttu-id="16273-176">Nýja línan ætti að vera fyrir framan línuna sem fyrir er.</span><span class="sxs-lookup"><span data-stu-id="16273-176">The new line should be in front of the previously existing line.</span></span> <span data-ttu-id="16273-177">Til að gera breytinguna skaltu nota hnappana **Færa upp** og **Færa niður** á tækjastikunni eða breyta **Raðnúmeragildi** núverandi línu í *2*.</span><span class="sxs-lookup"><span data-stu-id="16273-177">To make the change, use the **Move up** and **Move down** buttons on the toolbar, or change the existing line's **Sequence number** value to *2*.</span></span>

    - <span data-ttu-id="16273-178">**Heiti:** *Setja í staðsetningarforstillingu MAGNS*</span><span class="sxs-lookup"><span data-stu-id="16273-178">**Name:** *Put to BULK Location profile*</span></span>
    - <span data-ttu-id="16273-179">**Notkun fastrar staðsetningar:** *Fastar og lausar staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="16273-179">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>
    - <span data-ttu-id="16273-180">**Leyfa neikvæðar birgðir:** *Hreinsa þennan gátreit (=Nei)*</span><span class="sxs-lookup"><span data-stu-id="16273-180">**Allow negative inventory:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="16273-181">**Runa virk:** *Hreinsa þennan gátreit (=Nei)*</span><span class="sxs-lookup"><span data-stu-id="16273-181">**Batch enabled:** *Clear this check box (=No)*</span></span>
    - <span data-ttu-id="16273-182">**Áætlun:** *Engin*</span><span class="sxs-lookup"><span data-stu-id="16273-182">**Strategy:** *None*</span></span>

1. <span data-ttu-id="16273-183">Meðan nýja línan er enn valin skaltu velja **Breyta fyrirspurn** fyrir ofan hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="16273-183">While the new line is still selected, select **Edit query** above the grid.</span></span>
1. <span data-ttu-id="16273-184">Í svarglugga ritilsins á flipanum **Svið** velur þú **Bæta við** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="16273-184">In the query dialog box, on the **Range** tab, select **Add** to add a line to the grid.</span></span>
1. <span data-ttu-id="16273-185">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="16273-185">On the new line, set the following values:</span></span>

    - <span data-ttu-id="16273-186">**Tafla:** *Staðir*</span><span class="sxs-lookup"><span data-stu-id="16273-186">**Table:** *Locations*</span></span>
    - <span data-ttu-id="16273-187">**Afleidd tafla:** *Staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="16273-187">**Derived table:** *Locations*</span></span>
    - <span data-ttu-id="16273-188">**Reitur:** *Auðkenni forstillingar staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="16273-188">**Field:** *Location profile ID*</span></span>
    - <span data-ttu-id="16273-189">**Skilyrði:** *BULK*</span><span class="sxs-lookup"><span data-stu-id="16273-189">**Criteria:** *BULK*</span></span>

1. <span data-ttu-id="16273-190">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="16273-190">Select **OK**.</span></span>
1. <span data-ttu-id="16273-191">Á síðunni **Staðsetningarleiðbeiningar** á aðgerðasvæðinu velur þú **Vista**.</span><span class="sxs-lookup"><span data-stu-id="16273-191">On the **Location directives** page, on the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="16273-192">Á flýtiflipanum **Aðgerðir staðsetningarleiðbeiningar** á svæðinu **Áætlun** ef notuð er staðsetningarleiðbeiningarnar *Sameina* er uppsetning á flýtiflipanum **Leyfðar blandanir afurðarvíddar** á **Staðsetningarforstillingum** hunsuð og afurðir settar í sömu staðsetningu, þó að uppsetning leyfi ekki slíka aðgerð.</span><span class="sxs-lookup"><span data-stu-id="16273-192">On the **Location Directive Actions** FastTab **Strategy** field, if you use the *Consolidate* location strategy, the setup of the **Allowed product dimension mixing** FastTab on the **Location profiles** will be overridden, and items will be put to the same location even if this behavior isn't allowed by the setup.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="16273-193">Stofna valmyndaratriði fartækis</span><span class="sxs-lookup"><span data-stu-id="16273-193">Create a mobile device menu item</span></span>

1. <span data-ttu-id="16273-194">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="16273-194">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="16273-195">Á aðgerðasvæðinu skal velja **Nýtt** til að stofna nýtt valmyndaratriði til að nota við flokkun.</span><span class="sxs-lookup"><span data-stu-id="16273-195">On the Action Pane, select **New** to create a menu item to use for sorting.</span></span>
1. <span data-ttu-id="16273-196">Stilla eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="16273-196">In the header, set the following values:</span></span>

    - <span data-ttu-id="16273-197">**Heiti valmyndaratriðis:** *Móttaka innkaupapöntunarlínu*</span><span class="sxs-lookup"><span data-stu-id="16273-197">**Menu item name:** *PO line receiving*</span></span>
    - <span data-ttu-id="16273-198">**Titill:** *Móttaka innkaupapöntunarlínu*</span><span class="sxs-lookup"><span data-stu-id="16273-198">**Title:** *PO line receiving*</span></span>
    - <span data-ttu-id="16273-199">**Máti:** *Vinna*</span><span class="sxs-lookup"><span data-stu-id="16273-199">**Mode:** *Work*</span></span>
    - <span data-ttu-id="16273-200">**Nota fyrirliggjandi vinnu:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="16273-200">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="16273-201">Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:</span><span class="sxs-lookup"><span data-stu-id="16273-201">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="16273-202">**Stofnunarferli vinnu:** *Móttaka og frátekning innkaupapöntunarlínu*</span><span class="sxs-lookup"><span data-stu-id="16273-202">**Work creation process:** *Purchase order line receiving and putaway*</span></span>
    - <span data-ttu-id="16273-203">**Mynda númeraplötu:** *Já*</span><span class="sxs-lookup"><span data-stu-id="16273-203">**Generate license plate:** *Yes*</span></span>

1. <span data-ttu-id="16273-204">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="16273-204">Select **Save**.</span></span>

### <a name="configure-the-mobile-device-menu"></a><span data-ttu-id="16273-205">Grunnstilling valmyndar fartækisins</span><span class="sxs-lookup"><span data-stu-id="16273-205">Configure the mobile device menu</span></span>

1. <span data-ttu-id="16273-206">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.</span><span class="sxs-lookup"><span data-stu-id="16273-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="16273-207">Veldu **Á innleið** á valmyndinni.</span><span class="sxs-lookup"><span data-stu-id="16273-207">In the list of menus, select **Inbound**.</span></span>
1. <span data-ttu-id="16273-208">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="16273-208">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="16273-209">Á listanum **Tiltækar valmyndir og valmyndaratriði** skaltu finna og velja valmyndaratriðið **Móttaka innkaupapöntunarlínu**.</span><span class="sxs-lookup"><span data-stu-id="16273-209">In the **Available Menus And Menu Items** list, find and select the **PO line receiving** menu item.</span></span>
1. <span data-ttu-id="16273-210">Smelltu á hægri örvarhnappinn til að færa valmyndaratriðið **Móttaka innkaupapöntunarlínu** yfir á listann **Valmyndarskipan**.</span><span class="sxs-lookup"><span data-stu-id="16273-210">Select the right arrow button to move the **PO line receiving** menu item to the **Menu Structure** list.</span></span> <span data-ttu-id="16273-211">Á þennan hátt bætirðu nýjum valmyndaratriðum við valda valmynd.</span><span class="sxs-lookup"><span data-stu-id="16273-211">In this way, you add your new menu item to the selected menu.</span></span>
1. <span data-ttu-id="16273-212">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="16273-212">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="16273-213">Aðstæður</span><span class="sxs-lookup"><span data-stu-id="16273-213">Scenario</span></span>

<span data-ttu-id="16273-214">Þessar sýniaðstæður sýna hvernig hægt er að setja tvö mismunandi afurðarafbrigði á sömu staðsetningu þegar staðsetningarforstillingin leyfir ekki blandaða hluti, en eiginleikinn *Blöndun á afurðarvídd staðsetningar* er virkur.</span><span class="sxs-lookup"><span data-stu-id="16273-214">This demo scenario shows how two different product variants can be put to the same location when the location profile doesn't allow for mixed items, but the *Location product dimension mixing* feature is enabled.</span></span> <span data-ttu-id="16273-215">Í þessu tilfelli muntu nota **stærðarafbrigðið** sem viðmiðun.</span><span class="sxs-lookup"><span data-stu-id="16273-215">In this case, you will use the **Size** variant as the criterion.</span></span>

<span data-ttu-id="16273-216">Áður en þú byrjar skaltu ganga úr skugga um að tómar staðsetningar séu til staðar í vöruhúsi *24* sem nota staðsetningarforstillinguna *MAGN*.</span><span class="sxs-lookup"><span data-stu-id="16273-216">Before you begin, make sure that there are empty locations in warehouse *24* that use the *BULK* location profile.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="16273-217">Stofna innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="16273-217">Create a purchase order</span></span>

<span data-ttu-id="16273-218">Þú verður að búa til innkaupapöntun sem hefur þrjár línur: tvær línur fyrir sama afurðarnúmer en mismunandi **stærðarafbrigði** og þriðja lína fyrir aðra afurð sem hefur engin afbrigði.</span><span class="sxs-lookup"><span data-stu-id="16273-218">You will create a purchase order that has three lines: two lines for the same product number but different **Size** variants, and a third line for a different product that has no variants.</span></span>

1. <span data-ttu-id="16273-219">Opnið **Viðskiptaskuldir \> Innkaupapantanir \> Allar innkaupapantanir**.</span><span class="sxs-lookup"><span data-stu-id="16273-219">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="16273-220">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="16273-220">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="16273-221">Sláðu inn eftirfarandi gildi í svarglugganum **Búa til innkaupapöntun**:</span><span class="sxs-lookup"><span data-stu-id="16273-221">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="16273-222">**Lánardrottnalykill:** *1001*</span><span class="sxs-lookup"><span data-stu-id="16273-222">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="16273-223">**Vöruhús:** *24*</span><span class="sxs-lookup"><span data-stu-id="16273-223">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="16273-224">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="16273-224">Select **OK**.</span></span>
1. <span data-ttu-id="16273-225">Innkaupapöntunin er búin til og ný lína er bætt við flýtiflipann **Innkaupapöntunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="16273-225">The purchase order is created, and a new line is added on the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="16273-226">Skráið niður innkaupapöntunarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="16273-226">Make a note of the purchase order number.</span></span>
1. <span data-ttu-id="16273-227">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="16273-227">On the new line, set the following values:</span></span>

    - <span data-ttu-id="16273-228">**Vörunúmer:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="16273-228">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="16273-229">**Stærð** *L*</span><span class="sxs-lookup"><span data-stu-id="16273-229">**Size** *L*</span></span>
    - <span data-ttu-id="16273-230">**Magn:** *2*</span><span class="sxs-lookup"><span data-stu-id="16273-230">**Quantity:** *2*</span></span>

1. <span data-ttu-id="16273-231">Veldu **Bæta við línu** fyrir ofan hnitanetið til að bæta við annarri innkaupapöntunarlínu og stilltu eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="16273-231">Select **Add line** above the grid to add a second purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="16273-232">**Vörunúmer:** *B0001*</span><span class="sxs-lookup"><span data-stu-id="16273-232">**Item number:** *B0001*</span></span>
    - <span data-ttu-id="16273-233">**Stærð** *XL*</span><span class="sxs-lookup"><span data-stu-id="16273-233">**Size** *XL*</span></span>
    - <span data-ttu-id="16273-234">**Magn:** *2*</span><span class="sxs-lookup"><span data-stu-id="16273-234">**Quantity:** *2*</span></span>

1. <span data-ttu-id="16273-235">Veldu **Bæta við línu** til að bæta við þriðju innkaupapöntunarlínu og stilltu eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="16273-235">Select **Add line** to add a third purchase order line, and set the following values:</span></span>

    - <span data-ttu-id="16273-236">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="16273-236">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="16273-237">**Magn:** *1*</span><span class="sxs-lookup"><span data-stu-id="16273-237">**Quantity:** *1*</span></span>

<span data-ttu-id="16273-238">1. Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="16273-238">1.Select **Save**.</span></span>

### <a name="receive-purchase-order-lines-in-the-warehouse-app"></a><span data-ttu-id="16273-239">Taka á móti innkaupapöntunarlínum í vöruhúsaforritinu</span><span class="sxs-lookup"><span data-stu-id="16273-239">Receive purchase order lines in the warehouse app</span></span>

1. <span data-ttu-id="16273-240">Skráðu þig inn í vöruhúsaforritið sem notandi sem er virkjaður fyrir vöruhús *24*.</span><span class="sxs-lookup"><span data-stu-id="16273-240">Sign in to the warehouse app as a user who is enabled for warehouse *24*.</span></span>
1. <span data-ttu-id="16273-241">Veldu valmyndina **Á innleið**.</span><span class="sxs-lookup"><span data-stu-id="16273-241">Select the **Inbound** menu.</span></span>
1. <span data-ttu-id="16273-242">Veldu **Móttaka innkaupapöntunarlínu**.</span><span class="sxs-lookup"><span data-stu-id="16273-242">Select **PO Line receiving**.</span></span>
1. <span data-ttu-id="16273-243">Veldu svæðið **PONUM** og sláðu síðan inn númer innkaupapöntunar.</span><span class="sxs-lookup"><span data-stu-id="16273-243">Select the **PONUM** field, and then enter the purchase order number.</span></span>
1. <span data-ttu-id="16273-244">Staðfestu innsláttinn með því að smella á staðfestingarhnappinn (✔) neðst á síðunni.</span><span class="sxs-lookup"><span data-stu-id="16273-244">Confirm your entry by selecting the confirm button ( ✔ ) at the bottom of the page.</span></span>
1. <span data-ttu-id="16273-245">Sláðu inn línunúmerið í innkaupapöntuninni sem verið er að taka á móti.</span><span class="sxs-lookup"><span data-stu-id="16273-245">Enter the line number from the purchase order that is being received.</span></span> <span data-ttu-id="16273-246">Veldu svæðið **LINENUM** og sláðu inn *1* með talnaborðinu.</span><span class="sxs-lookup"><span data-stu-id="16273-246">Select the **LINENUM** field, and then use the number pad to enter *1*.</span></span>
1. <span data-ttu-id="16273-247">Staðfestu færsluna.</span><span class="sxs-lookup"><span data-stu-id="16273-247">Confirm your entry.</span></span>
1. <span data-ttu-id="16273-248">Færðu inn magnið sem á að taka við.</span><span class="sxs-lookup"><span data-stu-id="16273-248">Enter the quantity to receive.</span></span> <span data-ttu-id="16273-249">Veldu hnappinn með plúsmerkinu (**+**) tvisvar til að hækka gildið á svæðinu **Magn** í *2*.</span><span class="sxs-lookup"><span data-stu-id="16273-249">Select the plus sign (**+**) button two times to increase the value in the **Qty** field to *2*.</span></span>
1. <span data-ttu-id="16273-250">Skráðu færsluna þína með því að velja hnappinn (✔) neðst á síðunni og staðfestu síðan færsluna með því að velja hnappinn (✔) aftur.</span><span class="sxs-lookup"><span data-stu-id="16273-250">Register your entry by selecting the button ( ✔ ) at the bottom of the page, and then confirm your entry by selecting the button ( ✔ ) again.</span></span>
1. <span data-ttu-id="16273-251">Skoða upplýsingar á síðunni **Innkaupapantanir: Frágangur**.</span><span class="sxs-lookup"><span data-stu-id="16273-251">View the information on the **Purchase orders: Put** page.</span></span> <span data-ttu-id="16273-252">Þessi síða birtir vinnuna sem var stofnuð fyrir fráganginn (Vinna 1).</span><span class="sxs-lookup"><span data-stu-id="16273-252">This page shows the work that has been created for the put-away (Work 1).</span></span>

    <span data-ttu-id="16273-253">Birt er staðsetningin sem gengið er frá móttekinni afurð, númeraplatan, afurðin, stærðin og magn verksins **Móttaka innkaupapöntunarlínu** sem nýlokið var við.</span><span class="sxs-lookup"><span data-stu-id="16273-253">The location where the received item will be put away, the license plate, the item, the size, and the quantity of the **PO Line receiving** task that you just completed are shown.</span></span>

1. <span data-ttu-id="16273-254">Staðfestu vinnuna við frágang.</span><span class="sxs-lookup"><span data-stu-id="16273-254">Confirm the put-away work.</span></span>
1. <span data-ttu-id="16273-255">Endurtakið skref 4 til 11 fyrir innkaupapöntunarlínu 2.</span><span class="sxs-lookup"><span data-stu-id="16273-255">Repeat the steps 4 through 11 for the purchase order line 2.</span></span> <span data-ttu-id="16273-256">Hins vegar tilgreinir þú magn *1* í skrefi 8.</span><span class="sxs-lookup"><span data-stu-id="16273-256">However, in step 8, specify a quantity of *1*.</span></span>

    <span data-ttu-id="16273-257">Ný vinna við frágang (Vinna 2) er búin til fyrir sömu staðsetningu og Vinna 1.</span><span class="sxs-lookup"><span data-stu-id="16273-257">New put-away work (Work 2) is created for the same location as Work 1.</span></span>

1. <span data-ttu-id="16273-258">Endurtakið skref 4 til 11 aftur fyrir innkaupapöntunarlínu 2.</span><span class="sxs-lookup"><span data-stu-id="16273-258">Repeat the steps 4 through 11 again for purchase order line 2.</span></span> <span data-ttu-id="16273-259">Í þrepi 8, tilgreindu magnið sem eftir er af *1*.</span><span class="sxs-lookup"><span data-stu-id="16273-259">In step 8, specify the remaining quantity of *1*.</span></span>

    <span data-ttu-id="16273-260">Ný vinna við frágang (Vinna 3) er búin til fyrir sömu staðsetningu og Vinna 1 og Vinna 2.</span><span class="sxs-lookup"><span data-stu-id="16273-260">New put-away work (Work 3) is created for the same location as Work 1 and Work 2.</span></span> <span data-ttu-id="16273-261">Þessi aðgerð verður vegna þess að staðsetningarleiðbeiningar um *Sameiningu* eru notaðar og uppsetningin á flýtiflipanum **Leyfð blöndun á afurðarvídd** á *staðsetningarforstillingum* **Magns** leyfir blöndun á afbrigðinu **Stærð** á staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="16273-261">This behavior occurs because the *Consolidate* location directive strategy is used, and the **Allowed product dimension mixing** FastTab on the *Bulk* **Location profiles** setup allows the **Size** variant to be mixed on a location.</span></span>

1. <span data-ttu-id="16273-262">Endurtakið skref 4 til 11 fyrir innkaupapöntunarlínu 3.</span><span class="sxs-lookup"><span data-stu-id="16273-262">Repeat the steps 4 through 11 for purchase order line 3.</span></span> <span data-ttu-id="16273-263">Í þrepi 8, tilgreindu magn *1* fyrir afurðarnúmer *A0001*.</span><span class="sxs-lookup"><span data-stu-id="16273-263">In step 8, specify a quantity of *1* for item number *A0001*.</span></span>

    <span data-ttu-id="16273-264">Ný vinna við frágang (Vinna 4) er búin til fyrir aðra staðsetningu en staðsetningin sem er notuð fyrir innkaupapöntunarlínur 1 og 2.</span><span class="sxs-lookup"><span data-stu-id="16273-264">New put-away work (Work 4) is created for a different location than the location that is used for purchase order lines 1 and 2.</span></span> <span data-ttu-id="16273-265">Þessi aðgerð verður vegna þess að staðsetningarforstillingin leyfir ekki blandaðar afurðir, en það gerir ráð fyrir blönduðum víddum sama afurðarsniðmáts.</span><span class="sxs-lookup"><span data-stu-id="16273-265">This behavior occurs because the location profile doesn't allow for mixed products, but it does allow for mixed dimensions of the same product master.</span></span>

1. <span data-ttu-id="16273-266">Veldu valmyndarhnappinn efst á síðunni (stundum kallaður hamborgari eða hamborgarahnappur) og veldu síðan **Hætta við** til að loka **Móttöku innkaupapöntunarlínu**.</span><span class="sxs-lookup"><span data-stu-id="16273-266">Select the Menu button at the top of the page (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit **PO Line receiving**.</span></span>

> [!TIP]
> <span data-ttu-id="16273-267">Þú getur endurtekið þessar aðstæður, en í þetta sinn skaltu stilla **Stærð** - *Nei* fyrir neðan **Leyfa blöndun á afurðarvídd** flýtiflipann á *Staðsetningarforstillingar* **Magns**, þannig að ekki sé hægt að blanda saman afurðarvíddum.</span><span class="sxs-lookup"><span data-stu-id="16273-267">You can repeat this scenario, but this time, set **Size** - *No* under the **Allow product dimension mixing** FastTab on the *BULK* **Location profiles**, so that none of the product dimensions can be mixed.</span></span> <span data-ttu-id="16273-268">Í þessu tilfelli, þegar þú færð innkaupapöntunina, verður hvert afurðarafbrigði sett á nýja staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="16273-268">In this case, when you receive the purchase order, each product variant will be put to a new location.</span></span>