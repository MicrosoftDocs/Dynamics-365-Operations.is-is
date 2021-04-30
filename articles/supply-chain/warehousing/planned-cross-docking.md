---
title: Áætluð dreifing frá dreifingarstöð
description: Þetta efnisatriði lýsir háþróaðri, áætlaðri dreifingu frá dreifingarstöð þar sem birgðamagninu sem þarf til pöntunar er strax við móttöku eða stofnun beint á rétt úthlið eða sviðsetningarsvæði. Öllum eftirstandandi birgðum frá upprunastaðnum á innleið verður beint að réttum geymslustað með hefðbundnu frágangsferli.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 11e044e04e05c68af676bf97e6085e9975da5c1d
ms.sourcegitcommit: bef7bd2aac00d7eb837fd275d383b7a5c3f1c1ee
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/19/2021
ms.locfileid: "5911249"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="a61f6-104">Áætluð dreifing frá dreifingarstöð</span><span class="sxs-lookup"><span data-stu-id="a61f6-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a61f6-105">Þetta efnisatriði lýsir háþróaðri, áætlaðri dreifingu frá dreifingarstöð.</span><span class="sxs-lookup"><span data-stu-id="a61f6-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="a61f6-106">Dreifing frá dreifingarstöð er vöruhúsaferli þar sem birgðamagnið sem þarf til pöntunar er strax við móttöku eða stofnun beint á rétt úthlið eða sviðsetningarsvæði.</span><span class="sxs-lookup"><span data-stu-id="a61f6-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="a61f6-107">Öllum eftirstandandi birgðum frá upprunastaðnum á innleið verður beint að réttum geymslustað með hefðbundnu frágangsferli.</span><span class="sxs-lookup"><span data-stu-id="a61f6-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="a61f6-108">Dreifing frá dreifingarstöð gerir starfsmönnum kleift að sleppa frágangi á innleið og tiltekt á útleið á birgðum sem þegar eru merktar fyrir pöntun á útleið.</span><span class="sxs-lookup"><span data-stu-id="a61f6-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="a61f6-109">Þar af leiðandi er dregið úr fjölda skipta sem hreyft er við birgðum, þegar slíku er við komið.</span><span class="sxs-lookup"><span data-stu-id="a61f6-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="a61f6-110">Þar að auki, vegna þess að minni samskipti eru við kerfið, eykst sparnaður á tíma og rými í vinnusal vöruhússins til muna.</span><span class="sxs-lookup"><span data-stu-id="a61f6-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="a61f6-111">Áður en hægt er að keyra dreifingu frá dreifingarstöð þarf að grunnstilla nýtt sniðmát fyrir dreifingu frá dreifingarstöð, þar sem birgðauppruni og önnur skilyrði fyrir dreifingu frá dreifingarstöð eru skilgreind.</span><span class="sxs-lookup"><span data-stu-id="a61f6-111">Before you can run cross-docking, you must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="a61f6-112">Þegar pöntunin á útleið er stofnuð verður línan að vera merkt á móti pöntun á innleið sem inniheldur sama atriði.</span><span class="sxs-lookup"><span data-stu-id="a61f6-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span> <span data-ttu-id="a61f6-113">Hægt er að velja reit leiðbeiningarkóða í sniðmáti dreifingar frá dreifingarstöð á svipaðan hátt og áfyllingar og innkaupapantanir eru settar upp.</span><span class="sxs-lookup"><span data-stu-id="a61f6-113">You can select the directive code field on the cross-docking template, similar to the way you set up replenishment and purchase orders.</span></span>

<span data-ttu-id="a61f6-114">Þegar tekið er á móti pöntun á innleið, auðkennir dreifing frá dreifingarstöð sjálfkrafa þörfina fyrir dreifingu frá dreifingarstöð og býr til birgðahreyfingu fyrir það magn sem krafist er, miðað við uppsetningu staðsetningarleiðbeininga.</span><span class="sxs-lookup"><span data-stu-id="a61f6-114">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="a61f6-115">Birgðafærslur eru *ekki* óskráðar þegar hætt er við dreifingu frá dreifingarstöð, jafnvel þó að kveikt sé á stillingunni fyrir þennan eiginleika í færibreytum vöruhúsakerfisins.</span><span class="sxs-lookup"><span data-stu-id="a61f6-115">Inventory transactions are *not* unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-features"></a><span data-ttu-id="a61f6-116">Kveikja á áætlaðri dreifingu frá dreifingarstöð</span><span class="sxs-lookup"><span data-stu-id="a61f6-116">Turn on the planned cross docking features</span></span>

<span data-ttu-id="a61f6-117">Ef kerfið inniheldur ekki eiginleikana sem lýst er í þessu efnisatriði skal fara í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og kveikja á eftirfarandi eiginleikum í eftirfarandi röð:</span><span class="sxs-lookup"><span data-stu-id="a61f6-117">If your system doesn't already include the features described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) and turn on the following features in the following order:</span></span>

1. <span data-ttu-id="a61f6-118">*Áætluð dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="a61f6-118">*Planned cross docking*</span></span>
1. <span data-ttu-id="a61f6-119">*Sniðmát dreifingar frá dreifingarstöð með staðsetningarleiðbeiningum*</span><span class="sxs-lookup"><span data-stu-id="a61f6-119">*Cross docking templates with location directives*</span></span>
    > [!NOTE]
    > <span data-ttu-id="a61f6-120">Þessi eiginleiki virkjar reitinn **Leiðbeiningarkóði** til að vera tilgreindur í sniðmáti dreifingar frá drefingarstöð á svipaðan hátt og áfyllingarsniðmát eru sett upp.</span><span class="sxs-lookup"><span data-stu-id="a61f6-120">This feature enables the **Directive code** field to be specified on the cross-docking template, similar to the way you set up replenishment templates.</span></span> <span data-ttu-id="a61f6-121">Að virkja þennan eiginleika kemur í veg fyrir að þú bætir við leiðbeiningarkóða í sniðmátslínur dreifingar frá dreifingarstöð fyrir síðustu *Frágangslínuna*.</span><span class="sxs-lookup"><span data-stu-id="a61f6-121">Enabling this feature prevents you from adding a directive code on the cross-docking work template lines for the final *Put* line.</span></span> <span data-ttu-id="a61f6-122">Þetta tryggir að hægt er að ákveða lokastaðsetningu frágangs meðan á stofnun vinnu stendur áður en vinnusniðmát eru tekin til greina.</span><span class="sxs-lookup"><span data-stu-id="a61f6-122">This ensures that the final put location can be determined during work creation before considering work templates.</span></span>

## <a name="setup"></a><span data-ttu-id="a61f6-123">Setja upp</span><span class="sxs-lookup"><span data-stu-id="a61f6-123">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="a61f6-124">Endurgera bókunaraðferðir farms</span><span class="sxs-lookup"><span data-stu-id="a61f6-124">Regenerate load posting methods</span></span>

<span data-ttu-id="a61f6-125">Áætluð dreifing frá dreifingarstöð er útfærð sem bókunaraðferð farms.</span><span class="sxs-lookup"><span data-stu-id="a61f6-125">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="a61f6-126">Eftir að þú hefur kveikt á eiginleikanum verður þú að endurgera aðferðirnar.</span><span class="sxs-lookup"><span data-stu-id="a61f6-126">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="a61f6-127">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Bókunaraðferðir farms**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-127">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="a61f6-128">Veldu **Endurgera aðferðir** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="a61f6-128">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="a61f6-129">Þegar endurgerð er lokið ætti að birtast aðferð sem hefur **Aðferðarheitisgildið** *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="a61f6-129">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="a61f6-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a61f6-130">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="a61f6-131">Búa til sniðmát fyrir dreifingu frá dreifingarstöð</span><span class="sxs-lookup"><span data-stu-id="a61f6-131">Create a cross-docking template</span></span>

1. <span data-ttu-id="a61f6-132">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Vinna \> Sniðmát dreifingar frá dreifingarstöð**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-132">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="a61f6-133">Veldu **Nýtt** á aðgerðasvæðinu til að búa til sniðmát.</span><span class="sxs-lookup"><span data-stu-id="a61f6-133">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="a61f6-134">Stilla eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="a61f6-134">In the header, set the following values:</span></span>

    - <span data-ttu-id="a61f6-135">**Röð:** *1*</span><span class="sxs-lookup"><span data-stu-id="a61f6-135">**Sequence:** *1*</span></span>

        <span data-ttu-id="a61f6-136">Þetta svæði skilgreinir röðina sem sniðmátin eru metin.</span><span class="sxs-lookup"><span data-stu-id="a61f6-136">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="a61f6-137">**Auðkenni sniðmáts fyrir dreifingu frá dreifingarmiðstöð:** *51*</span><span class="sxs-lookup"><span data-stu-id="a61f6-137">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="a61f6-138">**Lýsing:** *Vöruhús 51*</span><span class="sxs-lookup"><span data-stu-id="a61f6-138">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="a61f6-139">**Losunarregla eftirspurnar:** *Áður en tekið er við birgðum*</span><span class="sxs-lookup"><span data-stu-id="a61f6-139">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="a61f6-140">**Vöruhús:** *51*</span><span class="sxs-lookup"><span data-stu-id="a61f6-140">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="a61f6-141">Uppsetningin á flýtiflipanum **Skipulag** stýrir því hvernig sniðmátið virkar.</span><span class="sxs-lookup"><span data-stu-id="a61f6-141">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="a61f6-142">Stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="a61f6-142">Set the following values:</span></span>

    - <span data-ttu-id="a61f6-143">**Eftirspurnarkröfur:** *Engar*</span><span class="sxs-lookup"><span data-stu-id="a61f6-143">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="a61f6-144">Þetta svæði skilgreinir kröfur birgðaeftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="a61f6-144">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="a61f6-145">Ef eftirspurnin verður að vera tengd við birgðir áður en hún er losið skaltu velja *Merking*.</span><span class="sxs-lookup"><span data-stu-id="a61f6-145">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="a61f6-146">Ef taka verður eftirspurnina frá birgðum áður en losun á sér stað, skaltu velja *Frátektarpöntun*.</span><span class="sxs-lookup"><span data-stu-id="a61f6-146">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="a61f6-147">**Gerð staðsetningar:** *Staðsetningar sendinga*</span><span class="sxs-lookup"><span data-stu-id="a61f6-147">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="a61f6-148">Þetta svæði skilgreinir hvort að vinna við dreifingu frá dreifingarstöð ætti að nota sviðsetningar-/hleðslustaðsetningar sendingarinnar, eða hvort hún eigi að nota staðsetningarleiðbeiningar til að leita að eigin sviðsetningar- /hleðslustaðsetningum.</span><span class="sxs-lookup"><span data-stu-id="a61f6-148">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="a61f6-149">**Vinnusniðmát:** Skildu þetta svæði eftir autt.</span><span class="sxs-lookup"><span data-stu-id="a61f6-149">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="a61f6-150">Þetta svæði skilgreinir vinnusniðmátið sem skal nota þegar vinna við dreifingu frá dreifingarstöð er búin til.</span><span class="sxs-lookup"><span data-stu-id="a61f6-150">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="a61f6-151">**Staðfesta aftur birgðarafhendingu:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="a61f6-151">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="a61f6-152">Þessi valkostur skilgreinir hvort staðfest skuli aftur birgðir við afhendingu.</span><span class="sxs-lookup"><span data-stu-id="a61f6-152">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="a61f6-153">Ef þessi valkostur er stilltur á *Já* er bæði hámarkstímagluggi og dagsetningabil lokadaga athugaðir.</span><span class="sxs-lookup"><span data-stu-id="a61f6-153">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="a61f6-154">**Leiðbeiningarkóði:** Hafðu þetta svæði autt</span><span class="sxs-lookup"><span data-stu-id="a61f6-154">**Directive code:** Leave this field blank</span></span>

        <span data-ttu-id="a61f6-155">Þessi valkostur er virkjaður af eiginleikanum *Sniðmát dreifingar frá dreifingarstöð með staðsetningarleiðbeiningum*.</span><span class="sxs-lookup"><span data-stu-id="a61f6-155">This option is enabled by the *Cross docking templates with location directives* feature.</span></span> <span data-ttu-id="a61f6-156">Kerfið notar staðsetningarleiðbeiningar til að finna út bestu staðsetninguna til að dreifa birgðum frá dreifingarstöð.</span><span class="sxs-lookup"><span data-stu-id="a61f6-156">The system uses location directives to help determine the best location to move cross-docking inventory to.</span></span> <span data-ttu-id="a61f6-157">Hægt er að setja það upp með því að úthluta leiðbeiningarkóða á hvert sniðmát dreifingarstöðvar.</span><span class="sxs-lookup"><span data-stu-id="a61f6-157">You can set it up by assigning a directive code to each relevant cross-docking template.</span></span> <span data-ttu-id="a61f6-158">Ef leiðbeiningarkóði er stilltur leitar kerfið í staðsetningarleiðbeiningum eftir leiðbeiningarkóða þegar vinna er búin til.</span><span class="sxs-lookup"><span data-stu-id="a61f6-158">If a directive code is set, the system will search location directives by directive code when work is generated.</span></span> <span data-ttu-id="a61f6-159">Þannig er hægt að takmarka staðsetningarleiðbeiningar sem eru notaðar fyrir tiltekið sniðmát dreifingar frá dreifingarstöð.</span><span class="sxs-lookup"><span data-stu-id="a61f6-159">In this way, you can limit location directives that are used for a particular cross-docking template.</span></span>

    - <span data-ttu-id="a61f6-160">**Staðfesta tímaglugga:** *Já*</span><span class="sxs-lookup"><span data-stu-id="a61f6-160">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="a61f6-161">Þessi valkostur skilgreinir hvort að meta skuli hámarkstímagluga þegar birgðauppruni er valinn.</span><span class="sxs-lookup"><span data-stu-id="a61f6-161">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="a61f6-162">Ef þessi valkostur er stilltur á *Já* verða svæðin sem tengjast hámarks- og lágmarkstímagluggum tiltækir.</span><span class="sxs-lookup"><span data-stu-id="a61f6-162">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="a61f6-163">**Hámarkstímagluggi:** *5*</span><span class="sxs-lookup"><span data-stu-id="a61f6-163">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="a61f6-164">Þetta svæði skilgreinir leyfilegt hámarkstímabil á milli komu birgða og loka eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="a61f6-164">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="a61f6-165">**Eining fyrir hámarkstímaglugga:** *Dagar*</span><span class="sxs-lookup"><span data-stu-id="a61f6-165">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="a61f6-166">**Lágmarkstímagluggi:** *0*</span><span class="sxs-lookup"><span data-stu-id="a61f6-166">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="a61f6-167">Þetta svæði skilgreinir leyfilegt lágmarkstímabil á milli komu birgða og loka eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="a61f6-167">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="a61f6-168">**Eining fyrir lágmarkstímaglugga:** *Dagar*</span><span class="sxs-lookup"><span data-stu-id="a61f6-168">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="a61f6-169">**Dagsetningabil lokadags:** *0*</span><span class="sxs-lookup"><span data-stu-id="a61f6-169">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="a61f6-170">*Viðmið fyrir Fyrsta Lokadag Fyrst út (FEFO):* Þetta svæði skilgreinir hámarksfjölda daga á milli lokadags rununnar sem rennur fyrst út sem er núna í vöruhúsinu og rununnar sem verið er að taka á móti.</span><span class="sxs-lookup"><span data-stu-id="a61f6-170">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="a61f6-171">Á flýtiflipanum **Birgðaupprunar** skilgreinir þú birgðagerðirnar sem gilda fyrir þetta sniðmát.</span><span class="sxs-lookup"><span data-stu-id="a61f6-171">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="a61f6-172">Veldu **Nýtt** og stilltu síðan eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="a61f6-172">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="a61f6-173">**Raðnúmer:** *1*</span><span class="sxs-lookup"><span data-stu-id="a61f6-173">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="a61f6-174">**Birgðauppruni:** *Innkaupapöntun*</span><span class="sxs-lookup"><span data-stu-id="a61f6-174">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="a61f6-175">Stofna vinnuklasa</span><span class="sxs-lookup"><span data-stu-id="a61f6-175">Create a work class</span></span>

1. <span data-ttu-id="a61f6-176">Fara í **Vöruhúsastjórnun \> Uppsetning \> Vinna \> Vinnuklasar**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-176">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="a61f6-177">Veldu **Nýtt** á aðgerðasvæðinu til að búa til vinnuklasa.</span><span class="sxs-lookup"><span data-stu-id="a61f6-177">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="a61f6-178">Stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="a61f6-178">Set the following values:</span></span>

    - <span data-ttu-id="a61f6-179">**Auðkenni vinnuklasa:** *Dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="a61f6-179">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="a61f6-180">**Lýsing:** *Dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="a61f6-180">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="a61f6-181">**Gerð verkpöntunar:** *Dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="a61f6-181">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="a61f6-182">Stofna sniðmát verks</span><span class="sxs-lookup"><span data-stu-id="a61f6-182">Create a work template</span></span>

1. <span data-ttu-id="a61f6-183">Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-183">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="a61f6-184">Stilltu svæðið **Gerð verkpöntunar** á *Dreifing frá dreifingarstöð*.</span><span class="sxs-lookup"><span data-stu-id="a61f6-184">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="a61f6-185">Veldu **Ný** á aðgerðasvæðinu til að bæta línu við flipann **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-185">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="a61f6-186">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="a61f6-186">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a61f6-187">**Raðnúmer:** *1*</span><span class="sxs-lookup"><span data-stu-id="a61f6-187">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="a61f6-188">**Vinnusniðmát:** *51 Dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="a61f6-188">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="a61f6-189">**Lýsing á vinnusniðmáti:** *51 Dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="a61f6-189">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="a61f6-190">Veldu **Vista** til að gera flýtiflipann **Upplýsingar um vinnusniðmát** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="a61f6-190">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="a61f6-191">Á flýtiflipanum **Upplýsingar um vinnusniðmát** velur þú **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="a61f6-191">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="a61f6-192">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="a61f6-192">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a61f6-193">**Verkgerð:** *Tiltekt*</span><span class="sxs-lookup"><span data-stu-id="a61f6-193">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="a61f6-194">**Auðkenni vinnuklasa:** *Dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="a61f6-194">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="a61f6-195">Veldu **Ný** til að bæta við annarri línu og stilltu eftirfarandi gildi fyrir hana:</span><span class="sxs-lookup"><span data-stu-id="a61f6-195">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="a61f6-196">**Tegund vinnu:** *Frágangur*</span><span class="sxs-lookup"><span data-stu-id="a61f6-196">**Work type:** *Put*</span></span>
    - <span data-ttu-id="a61f6-197">**Auðkenni vinnuklasa:** *Dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="a61f6-197">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="a61f6-198">Veldu **Vista** og staðfestu að hakað sé í gátreitinn **Gilt** fyrir sniðmát *51 dreifingar frá dreifingarstöð*.</span><span class="sxs-lookup"><span data-stu-id="a61f6-198">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="a61f6-199">Vinnuklasakenni fyrir vinnugerðir *Tiltektar* og *Frágangs* verða að vera eins.</span><span class="sxs-lookup"><span data-stu-id="a61f6-199">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="a61f6-200">Búa til staðsetningarleiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="a61f6-200">Create location directives</span></span>

1. <span data-ttu-id="a61f6-201">Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-201">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="a61f6-202">Stilltu svæðið **Gerð verkpöntunar** á *Dreifing frá dreifingarstöð* í vinstri glugganum.</span><span class="sxs-lookup"><span data-stu-id="a61f6-202">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="a61f6-203">Veldu **Nýtt** á aðgerðasvæðinu og stilltu eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="a61f6-203">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="a61f6-204">**Raðnúmer:** *1*</span><span class="sxs-lookup"><span data-stu-id="a61f6-204">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="a61f6-205">**Heiti:** *51 Frágangur dreifingar frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="a61f6-205">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="a61f6-206">**Tegund vinnu:** *Frágangur*</span><span class="sxs-lookup"><span data-stu-id="a61f6-206">**Work type:** *Put*</span></span>
    - <span data-ttu-id="a61f6-207">**Svæði:** *5*</span><span class="sxs-lookup"><span data-stu-id="a61f6-207">**Site:** *5*</span></span>
    - <span data-ttu-id="a61f6-208">**Vöruhús:** *51*</span><span class="sxs-lookup"><span data-stu-id="a61f6-208">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="a61f6-209">Veldu **Vista** til að gera flýtiflipann **Línur** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="a61f6-209">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="a61f6-210">Á flýtiflipanum **Línur** velur þú **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="a61f6-210">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="a61f6-211">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="a61f6-211">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a61f6-212">**Frá-magn:** *1*</span><span class="sxs-lookup"><span data-stu-id="a61f6-212">**From quantity:** *1*</span></span>
    - <span data-ttu-id="a61f6-213">**Til magn:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="a61f6-213">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="a61f6-214">Veldu **Vista** til að gera flýtiflipann **Aðgerðir í staðsetningarleiðbeiningum** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="a61f6-214">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="a61f6-215">Á flýtiflipanum **Aðgerðir staðsetningarleiðbeininga** velur þú **Ný** til að bæta við nýrri línu í hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="a61f6-215">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="a61f6-216">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="a61f6-216">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a61f6-217">**Heiti:** *Útskot*</span><span class="sxs-lookup"><span data-stu-id="a61f6-217">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="a61f6-218">**Notkun fastrar staðsetningar:** *Fastar og lausar staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="a61f6-218">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="a61f6-219">Veldu **Vista** til að gera hnappinn **Breyta fyrirspurn** á **Aðgerðir í staðsetningarleiðbeiningum** tækjastikunni aðgengilegan.</span><span class="sxs-lookup"><span data-stu-id="a61f6-219">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="a61f6-220">Veldu **Breyta fyrirspurn** til að opna fyrirspurnarritilinn.</span><span class="sxs-lookup"><span data-stu-id="a61f6-220">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="a61f6-221">Gakktu úr skugga um að eftirfarandi tvær línur séu stilltar á flipanum **Svið**:</span><span class="sxs-lookup"><span data-stu-id="a61f6-221">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="a61f6-222">Lína 1:</span><span class="sxs-lookup"><span data-stu-id="a61f6-222">Line 1:</span></span>

        - <span data-ttu-id="a61f6-223">**Tafla:** *Staðir*</span><span class="sxs-lookup"><span data-stu-id="a61f6-223">**Table:** *Locations*</span></span>
        - <span data-ttu-id="a61f6-224">**Afleidd tafla:** *Staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="a61f6-224">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="a61f6-225">**Svæði:** *Vöruhús*</span><span class="sxs-lookup"><span data-stu-id="a61f6-225">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="a61f6-226">**Skilyrði:** *51*</span><span class="sxs-lookup"><span data-stu-id="a61f6-226">**Criteria:** *51*</span></span>

    - <span data-ttu-id="a61f6-227">Lína 2:</span><span class="sxs-lookup"><span data-stu-id="a61f6-227">Line 2:</span></span>

        - <span data-ttu-id="a61f6-228">**Tafla:** *Staðir*</span><span class="sxs-lookup"><span data-stu-id="a61f6-228">**Table:** *Locations*</span></span>
        - <span data-ttu-id="a61f6-229">**Afleidd tafla:** *Staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="a61f6-229">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="a61f6-230">**Svæði:** *Staðsetning*</span><span class="sxs-lookup"><span data-stu-id="a61f6-230">**Field:** *Location*</span></span>
        - <span data-ttu-id="a61f6-231">**Skilyrði:** *Útskot*</span><span class="sxs-lookup"><span data-stu-id="a61f6-231">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="a61f6-232">Veldu **Í lagi** til að loka fyrirspurnarritlinum.</span><span class="sxs-lookup"><span data-stu-id="a61f6-232">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="a61f6-233">Stofna valmyndaratriði fartækis</span><span class="sxs-lookup"><span data-stu-id="a61f6-233">Create a mobile device menu item</span></span>

1. <span data-ttu-id="a61f6-234">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-234">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="a61f6-235">Veldu **Frágangur kaupa** í listanum yfir valmyndaratriði í glugganum til vinstri.</span><span class="sxs-lookup"><span data-stu-id="a61f6-235">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="a61f6-236">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-236">Select **Edit**.</span></span>
1. <span data-ttu-id="a61f6-237">Á flýtiflipanum **Vinnuklasar** velur þú **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="a61f6-237">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="a61f6-238">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="a61f6-238">On the new line, set the following values:</span></span>

    - <span data-ttu-id="a61f6-239">**Auðkenni vinnuklasa:** *Dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="a61f6-239">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="a61f6-240">**Gerð verkpöntunar:** *Dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="a61f6-240">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="a61f6-241">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-241">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="a61f6-242">Aðstæður</span><span class="sxs-lookup"><span data-stu-id="a61f6-242">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="a61f6-243">Stofna innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="a61f6-243">Create a purchase order</span></span>

<span data-ttu-id="a61f6-244">Fylgdu eftirfarandi skrefum til að stofna innkaupapöntun sem birgðauppruna.</span><span class="sxs-lookup"><span data-stu-id="a61f6-244">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="a61f6-245">Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-245">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="a61f6-246">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-246">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a61f6-247">Sláðu inn eftirfarandi gildi í svarglugganum **Búa til innkaupapöntun**:</span><span class="sxs-lookup"><span data-stu-id="a61f6-247">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a61f6-248">**Lánardrottnalykill:** *104*</span><span class="sxs-lookup"><span data-stu-id="a61f6-248">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="a61f6-249">**Vöruhús:** *51*</span><span class="sxs-lookup"><span data-stu-id="a61f6-249">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="a61f6-250">Veldu **Í lagi** og skráðu niður pöntunarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="a61f6-250">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="a61f6-251">Nýrri línu er bætt við flýtiflipann **Innkaupapöntunarlínurnar**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-251">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="a61f6-252">Stilltu eftirfarandi gildi á þessari línu:</span><span class="sxs-lookup"><span data-stu-id="a61f6-252">On this line, set the following values:</span></span>

    - <span data-ttu-id="a61f6-253">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="a61f6-253">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="a61f6-254">**Magn:** *5*</span><span class="sxs-lookup"><span data-stu-id="a61f6-254">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="a61f6-255">Stofna sölupöntun</span><span class="sxs-lookup"><span data-stu-id="a61f6-255">Create a sales order</span></span>

<span data-ttu-id="a61f6-256">Fylgdu eftirfarandi skrefum til að stofna sölupöntun sem uppruna eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="a61f6-256">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="a61f6-257">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-257">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="a61f6-258">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-258">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="a61f6-259">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="a61f6-259">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="a61f6-260">**Viðskiptavinalykill:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="a61f6-260">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="a61f6-261">**Vöruhús:** *51*</span><span class="sxs-lookup"><span data-stu-id="a61f6-261">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="a61f6-262">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-262">Select **OK**.</span></span>
1. <span data-ttu-id="a61f6-263">Nýrri línu er bætt við flýtiflipann **Sölupöntunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-263">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="a61f6-264">Stilltu eftirfarandi gildi á þessari línu:</span><span class="sxs-lookup"><span data-stu-id="a61f6-264">On this line, set the following values:</span></span>

    - <span data-ttu-id="a61f6-265">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="a61f6-265">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="a61f6-266">**Magn:** *3*</span><span class="sxs-lookup"><span data-stu-id="a61f6-266">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="a61f6-267">Búa til áætlaða dreifingu frá dreifingarstöð</span><span class="sxs-lookup"><span data-stu-id="a61f6-267">Create planned cross-docking</span></span>

<span data-ttu-id="a61f6-268">Fylgdu eftirfarandi skrefum til að búa til áætlaða dreifingu frá dreifingarstöð úr sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="a61f6-268">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="a61f6-269">Á síðunni **Upplýsingar um sölupöntun** fyrir sölupöntunina sem þú varst að búa til, á aðgerðarglugganum, á flipanum **Vöruhús**, í flokknum **Aðgerðir**, velur þú **Losun í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-269">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="a61f6-270">Aðgerðin við að losa í vöruhús býr til sendingu og farmlínu á sölupöntunarlínunni og gerir tilraun til að úthluta birgðum.</span><span class="sxs-lookup"><span data-stu-id="a61f6-270">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="a61f6-271">Þú færð upplýsingaboð.</span><span class="sxs-lookup"><span data-stu-id="a61f6-271">You receive an informational message.</span></span> <span data-ttu-id="a61f6-272">Þú færð einnig eftirfarandi viðvörunarboð: „Engin vinna var búin til fyrir bylgju XXXX.</span><span class="sxs-lookup"><span data-stu-id="a61f6-272">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="a61f6-273">Frekari upplýsingar er að finna í erilannál vinnustofnunar“.</span><span class="sxs-lookup"><span data-stu-id="a61f6-273">See the work creation history log for details."</span></span> <span data-ttu-id="a61f6-274">Búist er við slíkri aðgerð vegna þess að engar birgðir eru í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="a61f6-274">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="a61f6-275">Á flýtiflipanum **Sölupöntunarlínur** á valmyndinni **Vöruhús** smellir þú á **Upplýsingar um sendingu**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-275">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="a61f6-276">Síðan **Upplýsingar sendingar** opnast og sýnir sendinguna sem stofnuð var fyrir sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="a61f6-276">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="a61f6-277">Skoðaðu flýtiflipann **Farmlínur** og athugaðu hvort að svæðið **Áætlað magn til dreifingar frá dreifingarstöð** sé stillt á *3*.</span><span class="sxs-lookup"><span data-stu-id="a61f6-277">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="a61f6-278">Þar sem engar birgðir voru tiltækar í vöruhúsinu var magn dreifingar frá dreifingarstöð stofnað, en gildur birgðauppruni berst innan tímagluggans sem er skilgreindur í sniðmáti dreifingar frá dreifingarstöð.</span><span class="sxs-lookup"><span data-stu-id="a61f6-278">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="a61f6-279">Á flýtiflipanum **Farmlínur** velur þú **Áætlað til dreifingar frá dreifingarstöð** til að skoða frekari upplýsingar um dreifinguna frá dreifingarstöð sem var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="a61f6-279">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="a61f6-280">Vinna úr dreifingu frá dreifingarstöð</span><span class="sxs-lookup"><span data-stu-id="a61f6-280">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="a61f6-281">Móttaka innkaupapöntunar í farsímaforriti vöruhússins</span><span class="sxs-lookup"><span data-stu-id="a61f6-281">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="a61f6-282">Kerfið fær magnið 5 frá innkaupapöntuninni á móttökustaðinn og býr til tvær vinnueiningar.</span><span class="sxs-lookup"><span data-stu-id="a61f6-282">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="a61f6-283">Fyrsta vinnuauðkennið sem er búið til hefur gildi **Gerðar verkpöntunar** af gerð *Dreifingar frá dreifingarstöð* og er tengt sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="a61f6-283">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="a61f6-284">Það hefur magnið 3 og er beint á endanlega flutningsstaðsetningu svo hægt sé að senda hann strax út.</span><span class="sxs-lookup"><span data-stu-id="a61f6-284">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="a61f6-285">Annað vinnuauðkennið sem er búið til hefur gildi **Gerðar verkpöntunar** af gerð *Innkaupapantanir* og er tengt innkaupapöntuninni.</span><span class="sxs-lookup"><span data-stu-id="a61f6-285">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="a61f6-286">Það inniheldur magnið 2 sem eftir er sem var ekki í dreifingu úr dreifingarstöð og er beint í frágang í geymslu.</span><span class="sxs-lookup"><span data-stu-id="a61f6-286">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="a61f6-287">Skráðu þig inn í fartækið sem notandi í vöruhúsi *51*.</span><span class="sxs-lookup"><span data-stu-id="a61f6-287">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="a61f6-288">Opnaðu **Á innleið \> Móttaka innkaupa**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-288">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="a61f6-289">Sláðu inn innkaupapöntunarnúmer þitt á svæðin **PONum**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-289">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="a61f6-290">Í reitinn **Magn** skaltu slá inn *5*.</span><span class="sxs-lookup"><span data-stu-id="a61f6-290">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="a61f6-291">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-291">Select **OK**.</span></span>
1. <span data-ttu-id="a61f6-292">Á næstu síðu skaltu stilla svæðið **Atriði** á *A0001*.</span><span class="sxs-lookup"><span data-stu-id="a61f6-292">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="a61f6-293">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-293">Select **OK**.</span></span>
1. <span data-ttu-id="a61f6-294">Á næstu síðu staðfestir þú gildi **Sölupöntunarnúmersins**, **Atriðsins** og **Magnsins** með því að velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-294">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="a61f6-295">Skilaboðin „Vinnu er lokið“ birtast.</span><span class="sxs-lookup"><span data-stu-id="a61f6-295">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="a61f6-296">Veldu **Hætta við** til að hætta.</span><span class="sxs-lookup"><span data-stu-id="a61f6-296">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="a61f6-297">Frágangur dreifingar frá dreifingarstöð og magns</span><span class="sxs-lookup"><span data-stu-id="a61f6-297">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="a61f6-298">Sem stendur hafa bæði vinnuauðkennin sömu marknúmeraplötu.</span><span class="sxs-lookup"><span data-stu-id="a61f6-298">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="a61f6-299">Til að ljúka næstu skrefum verðurðu að fá vinnuauðkenni og marknúmeraplötu.</span><span class="sxs-lookup"><span data-stu-id="a61f6-299">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="a61f6-300">Þú færð þessar upplýsingar úr upplýsingum um innkaupapöntunarlínu og sölupöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="a61f6-300">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="a61f6-301">Að öðrum kosti er hægt að fara í **Vöruhúsakerfi \> Vinna \> Upplýsingar um vinnu** og sía fyrir vinnu þar sem gildi **Vöruhúss** er *51*.</span><span class="sxs-lookup"><span data-stu-id="a61f6-301">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="a61f6-302">Farðu í fatækið og farðu í **Á innleið \> Frágangur innkaupa** og sláðu inn marknúmeraplötu vinnunnar.</span><span class="sxs-lookup"><span data-stu-id="a61f6-302">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="a61f6-303">Í svæðið **Auðkenni** skaltu slá inn auðkenni marknúmeraplötunnar úr upplýsingunum um vinnu.</span><span class="sxs-lookup"><span data-stu-id="a61f6-303">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="a61f6-304">Tiltektarsíða dreifingar frá dreifingarstöð birtir tiltektarstaðsetninguna (*RECV*), marknúmeraplötuna (*númeraplata*), atriði (*A0001*) og magn (*3*).</span><span class="sxs-lookup"><span data-stu-id="a61f6-304">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="a61f6-305">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-305">Select **OK**.</span></span>
1. <span data-ttu-id="a61f6-306">Í reitinn **Marknúmeraplata** skal færa inn kenni marknúmeraplötuna fyrir auðkenni númeraplötunnar sem skal koma fyrir (dreifa frá dreifingarstöð) til sendingarstaðsetningarinnar.</span><span class="sxs-lookup"><span data-stu-id="a61f6-306">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="a61f6-307">Hægt er að velja hvaða auðkenni númeraplötu sem er.</span><span class="sxs-lookup"><span data-stu-id="a61f6-307">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="a61f6-308">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-308">Select **OK**.</span></span>
1. <span data-ttu-id="a61f6-309">Á næstu síðu á svæðinu **Auðkenni** slærðu inn auðkenni marknúmeraplötunnar.</span><span class="sxs-lookup"><span data-stu-id="a61f6-309">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="a61f6-310">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-310">Select **OK**.</span></span>
1. <span data-ttu-id="a61f6-311">Staðfestu vinnuna fyrir tiltektina á magninu sem eftir er 2 og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-311">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="a61f6-312">Veldu **Lokið** á næstu síðu til að ljúka tiltektarferlinu og hefja frágangsferlið.</span><span class="sxs-lookup"><span data-stu-id="a61f6-312">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="a61f6-313">Farsímaforritið birtir staðsetninguna og númeraplötuna til að setja atriðið á.</span><span class="sxs-lookup"><span data-stu-id="a61f6-313">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="a61f6-314">Staðfestu **Frágang** magngeymslu með því að velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-314">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="a61f6-315">Staðfestu **Frágang** dreifingar frá dreifingarstöð á næstu síðu með því að velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="a61f6-315">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="a61f6-316">Skilaboðin „Vinnu er lokið“ birtast.</span><span class="sxs-lookup"><span data-stu-id="a61f6-316">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="a61f6-317">Veldu **Hætta við** til að hætta.</span><span class="sxs-lookup"><span data-stu-id="a61f6-317">Select **Cancel** to exit.</span></span>

<span data-ttu-id="a61f6-318">Eftirfarandi skýringarmynd sýnir hvernig vinna við dreifingu frá dreifingarstöð gæti birst í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="a61f6-318">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="a61f6-319">![Vinnu við dreifingu frá dreifingarstöð er lokið](media/PlannedCrossDockingWork.png "Vinnu við dreifingu frá dreifingarstöð er lokið")</span><span class="sxs-lookup"><span data-stu-id="a61f6-319">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]