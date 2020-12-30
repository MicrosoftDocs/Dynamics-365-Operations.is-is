---
title: Áætluð dreifing frá dreifingarstöð
description: Þetta efnisatriði lýsir háþróaðri, áætlaðri dreifingu frá dreifingarstöð þar sem birgðamagninu sem þarf til pöntunar er strax við móttöku eða stofnun beint á rétt úthlið eða sviðsetningarsvæði. Öllum eftirstandandi birgðum frá upprunastaðnum á innleið verður beint að réttum geymslustað með hefðbundnu frágangsferli.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCrossDockingTemplate, WHSLoadPostMethod, WHSWorkClass, WHSWorkTemplateTable, WHSLocDirTable, WHSPlannedCrossDocking
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: cc217f21a5fa70feb9ef9161f3ef2e2b6a333f35
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430733"
---
# <a name="planned-cross-docking"></a><span data-ttu-id="22fc9-104">Áætluð dreifing frá dreifingarstöð</span><span class="sxs-lookup"><span data-stu-id="22fc9-104">Planned cross-docking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="22fc9-105">Þetta efnisatriði lýsir háþróaðri, áætlaðri dreifingu frá dreifingarstöð.</span><span class="sxs-lookup"><span data-stu-id="22fc9-105">This topic describes advanced planned cross-docking.</span></span> <span data-ttu-id="22fc9-106">Dreifing frá dreifingarstöð er vöruhúsaferli þar sem birgðamagnið sem þarf til pöntunar er strax við móttöku eða stofnun beint á rétt úthlið eða sviðsetningarsvæði.</span><span class="sxs-lookup"><span data-stu-id="22fc9-106">Cross-docking is a warehouse process where the inventory quantity that is required for an order is directed straight from receipt or creation to the correct outbound dock or staging area.</span></span> <span data-ttu-id="22fc9-107">Öllum eftirstandandi birgðum frá upprunastaðnum á innleið verður beint að réttum geymslustað með hefðbundnu frágangsferli.</span><span class="sxs-lookup"><span data-stu-id="22fc9-107">All remaining inventory from the inbound source is directed to the correct storage location through the regular put-away process.</span></span>

<span data-ttu-id="22fc9-108">Dreifing frá dreifingarstöð gerir starfsmönnum kleift að sleppa frágangi á innleið og tiltekt á útleið á birgðum sem þegar eru merktar fyrir pöntun á útleið.</span><span class="sxs-lookup"><span data-stu-id="22fc9-108">Cross-docking lets workers skip inbound put-away and outbound picking of inventory that is already marked for an outbound order.</span></span> <span data-ttu-id="22fc9-109">Þar af leiðandi er dregið úr fjölda skipta sem hreyft er við birgðum, þegar slíku er við komið.</span><span class="sxs-lookup"><span data-stu-id="22fc9-109">Therefore, the number of times that inventory is touched is minimized, where possible.</span></span> <span data-ttu-id="22fc9-110">Þar að auki, vegna þess að minni samskipti eru við kerfið, eykst sparnaður á tíma og rými í vinnusal vöruhússins til muna.</span><span class="sxs-lookup"><span data-stu-id="22fc9-110">Additionally, because there is less interaction with the system, time and space savings on the warehouse shop floor are increased.</span></span>

<span data-ttu-id="22fc9-111">Áður en hægt er að keyra dreifingu frá dreifingarstöð verður notandinn að grunnstilla nýtt sniðmát fyrir dreifingu frá dreifingarstöð, þar sem birgðauppruni og önnur skilyrði fyrir dreifingu frá dreifingarstöð eru skilgreind.</span><span class="sxs-lookup"><span data-stu-id="22fc9-111">Before cross-docking can be run, the user must configure a new cross-docking template, where the supply source and other sets of requirements for cross-docking are specified.</span></span> <span data-ttu-id="22fc9-112">Þegar pöntunin á útleið er stofnuð verður línan að vera merkt á móti pöntun á innleið sem inniheldur sama atriði.</span><span class="sxs-lookup"><span data-stu-id="22fc9-112">As the outbound order is created, the line must be marked against an inbound order that contains the same item.</span></span>

<span data-ttu-id="22fc9-113">Þegar tekið er á móti pöntun á innleið, auðkennir dreifing frá dreifingarstöð sjálfkrafa þörfina fyrir dreifingu frá dreifingarstöð og býr til birgðahreyfingu fyrir það magn sem krafist er, miðað við uppsetningu staðsetningarleiðbeininga.</span><span class="sxs-lookup"><span data-stu-id="22fc9-113">At the time of inbound order receiving, the cross-docking setup automatically identifies the need for cross-docking and creates the movement work for the required quantity, based on the setup of the location directive.</span></span>

> [!NOTE]
> <span data-ttu-id="22fc9-114">Birgðafærslur eru **ekki** óskráðar þegar hætt er við dreifingu frá dreifingarstöð, jafnvel þó að kveikt sé á stillingunni fyrir þennan eiginleika í færibreytum vöruhúsakerfisins.</span><span class="sxs-lookup"><span data-stu-id="22fc9-114">Inventory transactions are **not** unregistered when crossing-dock work is canceled, even if the setting for this capability is turned on in Warehouse management parameters.</span></span>

## <a name="turn-on-the-planned-cross-docking-feature"></a><span data-ttu-id="22fc9-115">Kveikja á áætlaðri dreifingu frá dreifingarstöð</span><span class="sxs-lookup"><span data-stu-id="22fc9-115">Turn on the Planned cross docking feature</span></span>

<span data-ttu-id="22fc9-116">Áður en þú getur notað háþróaða, áætlaða dreifingu frá dreifingarstöð verður að vera kveikt á eiginleikanum í kerfinu þínu.</span><span class="sxs-lookup"><span data-stu-id="22fc9-116">Before you can use advanced planned cross-docking, the feature must be turned on in your system.</span></span> <span data-ttu-id="22fc9-117">Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="22fc9-117">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="22fc9-118">Þar er eiginleikinn sýndur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="22fc9-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="22fc9-119">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="22fc9-119">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="22fc9-120">**Heiti eiginleika:** *Áætluð dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="22fc9-120">**Feature name:** *Planned cross docking*</span></span>

## <a name="setup"></a><span data-ttu-id="22fc9-121">Setja upp</span><span class="sxs-lookup"><span data-stu-id="22fc9-121">Setup</span></span>

### <a name="regenerate-load-posting-methods"></a><span data-ttu-id="22fc9-122">Endurgera bókunaraðferðir farms</span><span class="sxs-lookup"><span data-stu-id="22fc9-122">Regenerate load posting methods</span></span>

<span data-ttu-id="22fc9-123">Áætluð dreifing frá dreifingarstöð er útfærð sem bókunaraðferð farms.</span><span class="sxs-lookup"><span data-stu-id="22fc9-123">Planned cross-docking is implemented as a load posting method.</span></span> <span data-ttu-id="22fc9-124">Eftir að þú hefur kveikt á eiginleikanum verður þú að endurgera aðferðirnar.</span><span class="sxs-lookup"><span data-stu-id="22fc9-124">After you turn on the feature, you must regenerate the methods.</span></span>

1. <span data-ttu-id="22fc9-125">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Bókunaraðferðir farms**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-125">Go to **Warehouse management \> Setup \> Load posting methods**.</span></span>
1. <span data-ttu-id="22fc9-126">Veldu **Endurgera aðferðir** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="22fc9-126">On the Action Pane, select **Regenerate methods**.</span></span>

    <span data-ttu-id="22fc9-127">Þegar endurgerð er lokið ætti að birtast aðferð sem hefur **Aðferðarheitisgildið** *planCrossDocking*.</span><span class="sxs-lookup"><span data-stu-id="22fc9-127">When regeneration is completed, you should see a method that has a **Method name** value of *planCrossDocking*.</span></span>

1. <span data-ttu-id="22fc9-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="22fc9-128">Close the page.</span></span>

### <a name="create-a-cross-docking-template"></a><span data-ttu-id="22fc9-129">Búa til sniðmát fyrir dreifingu frá dreifingarstöð</span><span class="sxs-lookup"><span data-stu-id="22fc9-129">Create a cross-docking template</span></span>

1. <span data-ttu-id="22fc9-130">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Vinna \> Sniðmát dreifingar frá dreifingarstöð**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-130">Go to **Warehouse management \> Setup \> Work \> Cross docking templates**.</span></span>
1. <span data-ttu-id="22fc9-131">Veldu **Nýtt** á aðgerðasvæðinu til að búa til sniðmát.</span><span class="sxs-lookup"><span data-stu-id="22fc9-131">On the Action Pane, select **New** to create a template.</span></span>
1. <span data-ttu-id="22fc9-132">Stilla eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="22fc9-132">In the header, set the following values:</span></span>

    - <span data-ttu-id="22fc9-133">**Röð:** *1*</span><span class="sxs-lookup"><span data-stu-id="22fc9-133">**Sequence:** *1*</span></span>

        <span data-ttu-id="22fc9-134">Þetta svæði skilgreinir röðina sem sniðmátin eru metin.</span><span class="sxs-lookup"><span data-stu-id="22fc9-134">This field defines the order that templates are evaluated in.</span></span>

    - <span data-ttu-id="22fc9-135">**Auðkenni sniðmáts fyrir dreifingu frá dreifingarmiðstöð:** *51*</span><span class="sxs-lookup"><span data-stu-id="22fc9-135">**Cross docking template ID:** *51*</span></span>
    - <span data-ttu-id="22fc9-136">**Lýsing:** *Vöruhús 51*</span><span class="sxs-lookup"><span data-stu-id="22fc9-136">**Description:** *Warehouse 51*</span></span>
    - <span data-ttu-id="22fc9-137">**Losunarregla eftirspurnar:** *Áður en tekið er við birgðum*</span><span class="sxs-lookup"><span data-stu-id="22fc9-137">**Demand release policy:** *Before supply receipt*</span></span>
    - <span data-ttu-id="22fc9-138">**Vöruhús:** *51*</span><span class="sxs-lookup"><span data-stu-id="22fc9-138">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="22fc9-139">Uppsetningin á flýtiflipanum **Skipulag** stýrir því hvernig sniðmátið virkar.</span><span class="sxs-lookup"><span data-stu-id="22fc9-139">The setup on the **Planning** FastTab controls how the template works.</span></span> <span data-ttu-id="22fc9-140">Stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="22fc9-140">Set the following values:</span></span>

    - <span data-ttu-id="22fc9-141">**Eftirspurnarkröfur:** *Engar*</span><span class="sxs-lookup"><span data-stu-id="22fc9-141">**Demand requirements:** *None*</span></span>

        <span data-ttu-id="22fc9-142">Þetta svæði skilgreinir kröfur birgðaeftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="22fc9-142">This field defines the requirements of the demand inventory.</span></span> <span data-ttu-id="22fc9-143">Ef eftirspurnin verður að vera tengd við birgðir áður en hún er losið skaltu velja *Merking*.</span><span class="sxs-lookup"><span data-stu-id="22fc9-143">If the demand must be linked to the supply before release, select *Marking*.</span></span> <span data-ttu-id="22fc9-144">Ef taka verður eftirspurnina frá birgðum áður en losun á sér stað, skaltu velja *Frátektarpöntun*.</span><span class="sxs-lookup"><span data-stu-id="22fc9-144">If the demand must be order-reserved against the supply before release, select *Order reservation*.</span></span>

    - <span data-ttu-id="22fc9-145">**Gerð staðsetningar:** *Staðsetningar sendinga*</span><span class="sxs-lookup"><span data-stu-id="22fc9-145">**Locating type:** *Shipment locations*</span></span>

        <span data-ttu-id="22fc9-146">Þetta svæði skilgreinir hvort að vinna við dreifingu frá dreifingarstöð ætti að nota sviðsetningar-/hleðslustaðsetningar sendingarinnar, eða hvort hún eigi að nota staðsetningarleiðbeiningar til að leita að eigin sviðsetningar- /hleðslustaðsetningum.</span><span class="sxs-lookup"><span data-stu-id="22fc9-146">This field defines whether the cross-docking work should use the staging/load locations from the shipment, or whether it should use location directives to find its own staging/load locations.</span></span>

    - <span data-ttu-id="22fc9-147">**Vinnusniðmát:** Skildu þetta svæði eftir autt.</span><span class="sxs-lookup"><span data-stu-id="22fc9-147">**Work template:** Leave this field blank.</span></span>

        <span data-ttu-id="22fc9-148">Þetta svæði skilgreinir vinnusniðmátið sem skal nota þegar vinna við dreifingu frá dreifingarstöð er búin til.</span><span class="sxs-lookup"><span data-stu-id="22fc9-148">This field defines the work template that should be used when cross-docking work is created.</span></span>

    - <span data-ttu-id="22fc9-149">**Staðfesta aftur birgðarafhendingu:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="22fc9-149">**Revalidate on supply receipt:** *No*</span></span>

        <span data-ttu-id="22fc9-150">Þessi valkostur skilgreinir hvort staðfest skuli aftur birgðir við afhendingu.</span><span class="sxs-lookup"><span data-stu-id="22fc9-150">This option defines whether the supply should be revalidated during receipt.</span></span> <span data-ttu-id="22fc9-151">Ef þessi valkostur er stilltur á *Já* er bæði hámarkstímagluggi og dagsetningabil lokadaga athugaðir.</span><span class="sxs-lookup"><span data-stu-id="22fc9-151">If this option is set to *Yes*, both the maximum time window and the expiration days range are checked.</span></span>

    - <span data-ttu-id="22fc9-152">**Staðfesta tímaglugga:** *Já*</span><span class="sxs-lookup"><span data-stu-id="22fc9-152">**Validate time window:** *Yes*</span></span>

        <span data-ttu-id="22fc9-153">Þessi valkostur skilgreinir hvort að meta skuli hámarkstímagluga þegar birgðauppruni er valinn.</span><span class="sxs-lookup"><span data-stu-id="22fc9-153">This option defines whether the maximum time window should be evaluated when a supply source is selected.</span></span> <span data-ttu-id="22fc9-154">Ef þessi valkostur er stilltur á *Já* verða svæðin sem tengjast hámarks- og lágmarkstímagluggum tiltækir.</span><span class="sxs-lookup"><span data-stu-id="22fc9-154">If this option is set to *Yes*, the fields that are related to the maximum and minimum time windows become available.</span></span>

    - <span data-ttu-id="22fc9-155">**Hámarkstímagluggi:** *5*</span><span class="sxs-lookup"><span data-stu-id="22fc9-155">**Maximum time window:** *5*</span></span>

        <span data-ttu-id="22fc9-156">Þetta svæði skilgreinir leyfilegt hámarkstímabil á milli komu birgða og loka eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="22fc9-156">This field defines the maximum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="22fc9-157">**Eining fyrir hámarkstímaglugga:** *Dagar*</span><span class="sxs-lookup"><span data-stu-id="22fc9-157">**Maximum time window unit:** *Days*</span></span>
    - <span data-ttu-id="22fc9-158">**Lágmarkstímagluggi:** *0*</span><span class="sxs-lookup"><span data-stu-id="22fc9-158">**Minimum time window:** *0*</span></span>

        <span data-ttu-id="22fc9-159">Þetta svæði skilgreinir leyfilegt lágmarkstímabil á milli komu birgða og loka eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="22fc9-159">This field defines the minimum period that is allowed between supply arrival and demand departure.</span></span>

    - <span data-ttu-id="22fc9-160">**Eining fyrir lágmarkstímaglugga:** *Dagar*</span><span class="sxs-lookup"><span data-stu-id="22fc9-160">**Minimum time window unit:** *Days*</span></span>
    - <span data-ttu-id="22fc9-161">**Dagsetningabil lokadags:** *0*</span><span class="sxs-lookup"><span data-stu-id="22fc9-161">**Expiration days range:** *0*</span></span>

        <span data-ttu-id="22fc9-162">*Viðmið fyrir Fyrsta Lokadag Fyrst út (FEFO):* Þetta svæði skilgreinir hámarksfjölda daga á milli lokadags rununnar sem rennur fyrst út sem er núna í vöruhúsinu og rununnar sem verið er að taka á móti.</span><span class="sxs-lookup"><span data-stu-id="22fc9-162">*First expiry first out (FEFO) criteria:* This field defines the maximum number of days between the expiration date of the first-expiring batch that is currently in the warehouse and the batch that is being received.</span></span>

1. <span data-ttu-id="22fc9-163">Á flýtiflipanum **Birgðaupprunar** skilgreinir þú birgðagerðirnar sem gilda fyrir þetta sniðmát.</span><span class="sxs-lookup"><span data-stu-id="22fc9-163">On the **Supply sources** FastTab, you specify the types of supply that are valid for this template.</span></span> <span data-ttu-id="22fc9-164">Veldu **Nýtt** og stilltu síðan eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="22fc9-164">Select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="22fc9-165">**Raðnúmer:** *1*</span><span class="sxs-lookup"><span data-stu-id="22fc9-165">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="22fc9-166">**Birgðauppruni:** *Innkaupapöntun*</span><span class="sxs-lookup"><span data-stu-id="22fc9-166">**Supply source:** *Purchase order*</span></span>

### <a name="create-a-work-class"></a><span data-ttu-id="22fc9-167">Stofna vinnuklasa</span><span class="sxs-lookup"><span data-stu-id="22fc9-167">Create a work class</span></span>

1. <span data-ttu-id="22fc9-168">Fara í **Vöruhúsastjórnun \> Uppsetning \> Vinna \> Vinnuklasar**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-168">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="22fc9-169">Veldu **Nýtt** á aðgerðasvæðinu til að búa til vinnuklasa.</span><span class="sxs-lookup"><span data-stu-id="22fc9-169">On the Action Pane, select **New** to create a work class.</span></span>
1. <span data-ttu-id="22fc9-170">Stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="22fc9-170">Set the following values:</span></span>

    - <span data-ttu-id="22fc9-171">**Auðkenni vinnuklasa:** *Dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="22fc9-171">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="22fc9-172">**Lýsing:** *Dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="22fc9-172">**Description:** *Cross Dock*</span></span>
    - <span data-ttu-id="22fc9-173">**Gerð verkpöntunar:** *Dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="22fc9-173">**Work order type:** *Cross docking*</span></span>

### <a name="create-a-work-template"></a><span data-ttu-id="22fc9-174">Stofna sniðmát verks</span><span class="sxs-lookup"><span data-stu-id="22fc9-174">Create a work template</span></span>

1. <span data-ttu-id="22fc9-175">Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-175">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="22fc9-176">Stilltu svæðið **Gerð verkpöntunar** á *Dreifing frá dreifingarstöð*.</span><span class="sxs-lookup"><span data-stu-id="22fc9-176">Set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="22fc9-177">Veldu **Ný** á aðgerðasvæðinu til að bæta línu við flipann **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-177">On the Action Pane, select **New** to add a line to the **Overview** tab.</span></span>
1. <span data-ttu-id="22fc9-178">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="22fc9-178">On the new line, set the following values:</span></span>

    - <span data-ttu-id="22fc9-179">**Raðnúmer:** *1*</span><span class="sxs-lookup"><span data-stu-id="22fc9-179">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="22fc9-180">**Vinnusniðmát:** *51 Dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="22fc9-180">**Work template:** *51 Cross Dock*</span></span>
    - <span data-ttu-id="22fc9-181">**Lýsing á vinnusniðmáti:** *51 Dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="22fc9-181">**Work template description:** *51 Cross Dock*</span></span>

1. <span data-ttu-id="22fc9-182">Veldu **Vista** til að gera flýtiflipann **Upplýsingar um vinnusniðmát** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="22fc9-182">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="22fc9-183">Á flýtiflipanum **Upplýsingar um vinnusniðmát** velur þú **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="22fc9-183">On the **Work Template Details** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="22fc9-184">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="22fc9-184">On the new line, set the following values:</span></span>

    - <span data-ttu-id="22fc9-185">**Verkgerð:** *Tiltekt*</span><span class="sxs-lookup"><span data-stu-id="22fc9-185">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="22fc9-186">**Auðkenni vinnuklasa:** *Dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="22fc9-186">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="22fc9-187">Veldu **Ný** til að bæta við annarri línu og stilltu eftirfarandi gildi fyrir hana:</span><span class="sxs-lookup"><span data-stu-id="22fc9-187">Select **New** to add another line, and set the following values on it:</span></span>

    - <span data-ttu-id="22fc9-188">**Tegund vinnu:** *Frágangur*</span><span class="sxs-lookup"><span data-stu-id="22fc9-188">**Work type:** *Put*</span></span>
    - <span data-ttu-id="22fc9-189">**Auðkenni vinnuklasa:** *Dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="22fc9-189">**Work class ID:** *CrossDock*</span></span>

1. <span data-ttu-id="22fc9-190">Veldu **Vista** og staðfestu að hakað sé í gátreitinn **Gilt** fyrir sniðmát *51 dreifingar frá dreifingarstöð*.</span><span class="sxs-lookup"><span data-stu-id="22fc9-190">Select **Save**, and confirm that the **Valid** check box is selected for the *51 Cross Dock* template.</span></span>

> [!NOTE]
> <span data-ttu-id="22fc9-191">Vinnuklasakenni fyrir vinnugerðir *Tiltektar* og *Frágangs* verða að vera eins.</span><span class="sxs-lookup"><span data-stu-id="22fc9-191">The work class IDs for the *Pick* and *Put* work types must be the same.</span></span>

### <a name="create-location-directives"></a><span data-ttu-id="22fc9-192">Búa til staðsetningarleiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="22fc9-192">Create location directives</span></span>

1. <span data-ttu-id="22fc9-193">Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-193">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="22fc9-194">Stilltu svæðið **Gerð verkpöntunar** á *Dreifing frá dreifingarstöð* í vinstri glugganum.</span><span class="sxs-lookup"><span data-stu-id="22fc9-194">In the left pane, set the **Work order type** field to *Cross docking*.</span></span>
1. <span data-ttu-id="22fc9-195">Veldu **Nýtt** á aðgerðasvæðinu og stilltu eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="22fc9-195">On the Action Pane, select **New**, and set the following values:</span></span>

    - <span data-ttu-id="22fc9-196">**Raðnúmer:** *1*</span><span class="sxs-lookup"><span data-stu-id="22fc9-196">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="22fc9-197">**Heiti:** *51 Frágangur dreifingar frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="22fc9-197">**Name:** *51 Cross Dock Put*</span></span>
    - <span data-ttu-id="22fc9-198">**Tegund vinnu:** *Frágangur*</span><span class="sxs-lookup"><span data-stu-id="22fc9-198">**Work type:** *Put*</span></span>
    - <span data-ttu-id="22fc9-199">**Svæði:** *5*</span><span class="sxs-lookup"><span data-stu-id="22fc9-199">**Site:** *5*</span></span>
    - <span data-ttu-id="22fc9-200">**Vöruhús:** *51*</span><span class="sxs-lookup"><span data-stu-id="22fc9-200">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="22fc9-201">Veldu **Vista** til að gera flýtiflipann **Línur** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="22fc9-201">Select **Save** to make the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="22fc9-202">Á flýtiflipanum **Línur** velur þú **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="22fc9-202">On the **Lines** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="22fc9-203">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="22fc9-203">On the new line, set the following values:</span></span>

    - <span data-ttu-id="22fc9-204">**Frá-magn:** *1*</span><span class="sxs-lookup"><span data-stu-id="22fc9-204">**From quantity:** *1*</span></span>
    - <span data-ttu-id="22fc9-205">**Til magn:** *1000000*</span><span class="sxs-lookup"><span data-stu-id="22fc9-205">**To quantity:** *1,000,000*</span></span>

1. <span data-ttu-id="22fc9-206">Veldu **Vista** til að gera flýtiflipann **Aðgerðir í staðsetningarleiðbeiningum** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="22fc9-206">Select **Save** to make the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="22fc9-207">Á flýtiflipanum **Aðgerðir staðsetningarleiðbeininga** velur þú **Ný** til að bæta við nýrri línu í hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="22fc9-207">On the **Location Directive Actions** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="22fc9-208">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="22fc9-208">On the new line, set the following values:</span></span>

    - <span data-ttu-id="22fc9-209">**Heiti:** *Útskot*</span><span class="sxs-lookup"><span data-stu-id="22fc9-209">**Name:** *Baydoor*</span></span>
    - <span data-ttu-id="22fc9-210">**Notkun fastrar staðsetningar:** *Fastar og lausar staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="22fc9-210">**Fixed location usage:** *Fixed and non-fixed locations*</span></span>

1. <span data-ttu-id="22fc9-211">Veldu **Vista** til að gera hnappinn **Breyta fyrirspurn** á **Aðgerðir í staðsetningarleiðbeiningum** tækjastikunni aðgengilegan.</span><span class="sxs-lookup"><span data-stu-id="22fc9-211">Select **Save** to make the **Edit query** button on the **Location Directive Actions** toolbar available.</span></span>
1. <span data-ttu-id="22fc9-212">Veldu **Breyta fyrirspurn** til að opna fyrirspurnarritilinn.</span><span class="sxs-lookup"><span data-stu-id="22fc9-212">Select **Edit query** to open the query editor.</span></span>
1. <span data-ttu-id="22fc9-213">Gakktu úr skugga um að eftirfarandi tvær línur séu stilltar á flipanum **Svið**:</span><span class="sxs-lookup"><span data-stu-id="22fc9-213">On the **Range** tab, make sure that the following two lines are configured:</span></span>

    - <span data-ttu-id="22fc9-214">Lína 1:</span><span class="sxs-lookup"><span data-stu-id="22fc9-214">Line 1:</span></span>

        - <span data-ttu-id="22fc9-215">**Tafla:** *Staðir*</span><span class="sxs-lookup"><span data-stu-id="22fc9-215">**Table:** *Locations*</span></span>
        - <span data-ttu-id="22fc9-216">**Afleidd tafla:** *Staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="22fc9-216">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="22fc9-217">**Svæði:** *Vöruhús*</span><span class="sxs-lookup"><span data-stu-id="22fc9-217">**Field:** *Warehouse*</span></span>
        - <span data-ttu-id="22fc9-218">**Skilyrði:** *51*</span><span class="sxs-lookup"><span data-stu-id="22fc9-218">**Criteria:** *51*</span></span>

    - <span data-ttu-id="22fc9-219">Lína 2:</span><span class="sxs-lookup"><span data-stu-id="22fc9-219">Line 2:</span></span>

        - <span data-ttu-id="22fc9-220">**Tafla:** *Staðir*</span><span class="sxs-lookup"><span data-stu-id="22fc9-220">**Table:** *Locations*</span></span>
        - <span data-ttu-id="22fc9-221">**Afleidd tafla:** *Staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="22fc9-221">**Derived Table:** *Locations*</span></span>
        - <span data-ttu-id="22fc9-222">**Svæði:** *Staðsetning*</span><span class="sxs-lookup"><span data-stu-id="22fc9-222">**Field:** *Location*</span></span>
        - <span data-ttu-id="22fc9-223">**Skilyrði:** *Útskot*</span><span class="sxs-lookup"><span data-stu-id="22fc9-223">**Criteria:** *Baydoor*</span></span>

1. <span data-ttu-id="22fc9-224">Veldu **Í lagi** til að loka fyrirspurnarritlinum.</span><span class="sxs-lookup"><span data-stu-id="22fc9-224">Select **OK** to close the query editor.</span></span>

### <a name="create-a-mobile-device-menu-item"></a><span data-ttu-id="22fc9-225">Stofna valmyndaratriði fartækis</span><span class="sxs-lookup"><span data-stu-id="22fc9-225">Create a mobile device menu item</span></span>

1. <span data-ttu-id="22fc9-226">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-226">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="22fc9-227">Veldu **Frágangur kaupa** í listanum yfir valmyndaratriði í glugganum til vinstri.</span><span class="sxs-lookup"><span data-stu-id="22fc9-227">In the list of menu items in the left pane, select **Purchase Put-away**.</span></span>
1. <span data-ttu-id="22fc9-228">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-228">Select **Edit**.</span></span>
1. <span data-ttu-id="22fc9-229">Á flýtiflipanum **Vinnuklasar** velur þú **Ný** til að bæta línu við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="22fc9-229">On the **Work classes** FastTab, select **New** to add a line to the grid.</span></span>
1. <span data-ttu-id="22fc9-230">Stilltu eftirfarandi gildi á nýju línunni:</span><span class="sxs-lookup"><span data-stu-id="22fc9-230">On the new line, set the following values:</span></span>

    - <span data-ttu-id="22fc9-231">**Auðkenni vinnuklasa:** *Dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="22fc9-231">**Work class ID:** *CrossDock*</span></span>
    - <span data-ttu-id="22fc9-232">**Gerð verkpöntunar:** *Dreifing frá dreifingarstöð*</span><span class="sxs-lookup"><span data-stu-id="22fc9-232">**Work order type:** *Cross docking*</span></span>

1. <span data-ttu-id="22fc9-233">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-233">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="22fc9-234">Aðstæður</span><span class="sxs-lookup"><span data-stu-id="22fc9-234">Scenario</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="22fc9-235">Stofna innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="22fc9-235">Create a purchase order</span></span>

<span data-ttu-id="22fc9-236">Fylgdu eftirfarandi skrefum til að stofna innkaupapöntun sem birgðauppruna.</span><span class="sxs-lookup"><span data-stu-id="22fc9-236">Follow these steps to create a purchase order as a source of supply.</span></span>

1. <span data-ttu-id="22fc9-237">Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-237">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="22fc9-238">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-238">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="22fc9-239">Sláðu inn eftirfarandi gildi í svarglugganum **Búa til innkaupapöntun**:</span><span class="sxs-lookup"><span data-stu-id="22fc9-239">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="22fc9-240">**Lánardrottnalykill:** *104*</span><span class="sxs-lookup"><span data-stu-id="22fc9-240">**Vendor account:** *104*</span></span>
    - <span data-ttu-id="22fc9-241">**Vöruhús:** *51*</span><span class="sxs-lookup"><span data-stu-id="22fc9-241">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="22fc9-242">Veldu **Í lagi** og skráðu niður pöntunarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="22fc9-242">Select **OK**, and make a note of the order number.</span></span>
1. <span data-ttu-id="22fc9-243">Nýrri línu er bætt við flýtiflipann **Innkaupapöntunarlínurnar**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-243">A new line is added to the **Purchase order lines** FastTab.</span></span> <span data-ttu-id="22fc9-244">Stilltu eftirfarandi gildi á þessari línu:</span><span class="sxs-lookup"><span data-stu-id="22fc9-244">On this line, set the following values:</span></span>

    - <span data-ttu-id="22fc9-245">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="22fc9-245">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="22fc9-246">**Magn:** *5*</span><span class="sxs-lookup"><span data-stu-id="22fc9-246">**Quantity:** *5*</span></span>

### <a name="create-a-sales-order"></a><span data-ttu-id="22fc9-247">Stofna sölupöntun</span><span class="sxs-lookup"><span data-stu-id="22fc9-247">Create a sales order</span></span>

<span data-ttu-id="22fc9-248">Fylgdu eftirfarandi skrefum til að stofna sölupöntun sem uppruna eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="22fc9-248">Follow these steps to create a sales order as a source of demand.</span></span>

1. <span data-ttu-id="22fc9-249">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-249">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="22fc9-250">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-250">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="22fc9-251">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:</span><span class="sxs-lookup"><span data-stu-id="22fc9-251">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="22fc9-252">**Viðskiptavinalykill:** *US-002*</span><span class="sxs-lookup"><span data-stu-id="22fc9-252">**Customer account:** *US-002*</span></span>
    - <span data-ttu-id="22fc9-253">**Vöruhús:** *51*</span><span class="sxs-lookup"><span data-stu-id="22fc9-253">**Warehouse:** *51*</span></span>

1. <span data-ttu-id="22fc9-254">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-254">Select **OK**.</span></span>
1. <span data-ttu-id="22fc9-255">Nýrri línu er bætt við flýtiflipann **Sölupöntunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-255">A new line is added to the **Sales order lines** FastTab.</span></span> <span data-ttu-id="22fc9-256">Stilltu eftirfarandi gildi á þessari línu:</span><span class="sxs-lookup"><span data-stu-id="22fc9-256">On this line, set the following values:</span></span>

    - <span data-ttu-id="22fc9-257">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="22fc9-257">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="22fc9-258">**Magn:** *3*</span><span class="sxs-lookup"><span data-stu-id="22fc9-258">**Quantity:** *3*</span></span>

### <a name="create-planned-cross-docking"></a><span data-ttu-id="22fc9-259">Búa til áætlaða dreifingu frá dreifingarstöð</span><span class="sxs-lookup"><span data-stu-id="22fc9-259">Create planned cross-docking</span></span>

<span data-ttu-id="22fc9-260">Fylgdu eftirfarandi skrefum til að búa til áætlaða dreifingu frá dreifingarstöð úr sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="22fc9-260">Follow these steps to create the planned cross-docking from the sales order.</span></span>

1. <span data-ttu-id="22fc9-261">Á síðunni **Upplýsingar um sölupöntun** fyrir sölupöntunina sem þú varst að búa til, á aðgerðarglugganum, á flipanum **Vöruhús**, í flokknum **Aðgerðir**, velur þú **Losun í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-261">In the **Sales order details** page for the sales order that you just created, on the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>

    <span data-ttu-id="22fc9-262">Aðgerðin við að losa í vöruhús býr til sendingu og farmlínu á sölupöntunarlínunni og gerir tilraun til að úthluta birgðum.</span><span class="sxs-lookup"><span data-stu-id="22fc9-262">The release to warehouse action creates a shipment and load line for the sales order line, and tries to allocate inventory.</span></span>
    
    <span data-ttu-id="22fc9-263">Þú færð upplýsingaboð.</span><span class="sxs-lookup"><span data-stu-id="22fc9-263">You receive an informational message.</span></span> <span data-ttu-id="22fc9-264">Þú færð einnig eftirfarandi viðvörunarboð: „Engin vinna var búin til fyrir bylgju XXXX.</span><span class="sxs-lookup"><span data-stu-id="22fc9-264">You also receive the following warning message: "No work was created for wave XXXX.</span></span> <span data-ttu-id="22fc9-265">Frekari upplýsingar er að finna í erilannál vinnustofnunar“.</span><span class="sxs-lookup"><span data-stu-id="22fc9-265">See the work creation history log for details."</span></span> <span data-ttu-id="22fc9-266">Búist er við slíkri aðgerð vegna þess að engar birgðir eru í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="22fc9-266">This behavior is expected, because there is no inventory in the warehouse.</span></span>

1. <span data-ttu-id="22fc9-267">Á flýtiflipanum **Sölupöntunarlínur** á valmyndinni **Vöruhús** smellir þú á **Upplýsingar um sendingu**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-267">On the **Sales order lines** FastTab, on the **Warehouse** menu, select **Shipment details**.</span></span>

    <span data-ttu-id="22fc9-268">Síðan **Upplýsingar sendingar** opnast og sýnir sendinguna sem stofnuð var fyrir sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="22fc9-268">The **Shipment details** page appears and shows the shipment that was created for the sales order.</span></span>

1. <span data-ttu-id="22fc9-269">Skoðaðu flýtiflipann **Farmlínur** og athugaðu hvort að svæðið **Áætlað magn til dreifingar frá dreifingarstöð** sé stillt á *3*.</span><span class="sxs-lookup"><span data-stu-id="22fc9-269">On the **Load lines** FastTab, notice that the **Planned cross docking quantity** field is set to *3*.</span></span> <span data-ttu-id="22fc9-270">Þar sem engar birgðir voru tiltækar í vöruhúsinu var magn dreifingar frá dreifingarstöð stofnað, en gildur birgðauppruni berst innan tímagluggans sem er skilgreindur í sniðmáti dreifingar frá dreifingarstöð.</span><span class="sxs-lookup"><span data-stu-id="22fc9-270">Because no inventory was available in the warehouse, but a valid supply source will arrive within the time window that is defined in the cross-docking template, the cross-docking quantity was created.</span></span>
1. <span data-ttu-id="22fc9-271">Á flýtiflipanum **Farmlínur** velur þú **Áætlað til dreifingar frá dreifingarstöð** til að skoða frekari upplýsingar um dreifinguna frá dreifingarstöð sem var stofnuð.</span><span class="sxs-lookup"><span data-stu-id="22fc9-271">On the **Load lines** FastTab, select **Planned cross docking** to view the details of the cross-docking that was created.</span></span>

## <a name="process-the-cross-docking"></a><span data-ttu-id="22fc9-272">Vinna úr dreifingu frá dreifingarstöð</span><span class="sxs-lookup"><span data-stu-id="22fc9-272">Process the cross-docking</span></span>

### <a name="purchase-order-receiving-on-the-warehousing-mobile-app"></a><span data-ttu-id="22fc9-273">Móttaka innkaupapöntunar í farsímaforriti vöruhússins</span><span class="sxs-lookup"><span data-stu-id="22fc9-273">Purchase order receiving on the warehousing mobile app</span></span>

<span data-ttu-id="22fc9-274">Kerfið fær magnið 5 frá innkaupapöntuninni á móttökustaðinn og býr til tvær vinnueiningar.</span><span class="sxs-lookup"><span data-stu-id="22fc9-274">The system will receive the quantity of 5 from the purchase order into the receiving location and create two pieces of work.</span></span>

<span data-ttu-id="22fc9-275">Fyrsta vinnuauðkennið sem er búið til hefur gildi **Gerðar verkpöntunar** af gerð *Dreifingar frá dreifingarstöð* og er tengt sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="22fc9-275">The first work ID that is created has a **Work order type** value of *Cross docking* and is linked to the sales order.</span></span> <span data-ttu-id="22fc9-276">Það hefur magnið 3 og er beint á endanlega flutningsstaðsetningu svo hægt sé að senda hann strax út.</span><span class="sxs-lookup"><span data-stu-id="22fc9-276">It has a quantity of 3 and is directed to the final shipping location so that it can be shipped out immediately.</span></span>

<span data-ttu-id="22fc9-277">Annað vinnuauðkennið sem er búið til hefur gildi **Gerðar verkpöntunar** af gerð *Innkaupapantanir* og er tengt innkaupapöntuninni.</span><span class="sxs-lookup"><span data-stu-id="22fc9-277">The second work ID that is created has a **Work order type** value of *Purchase orders* and is linked to the purchase order.</span></span> <span data-ttu-id="22fc9-278">Það inniheldur magnið 2 sem eftir er sem var ekki í dreifingu úr dreifingarstöð og er beint í frágang í geymslu.</span><span class="sxs-lookup"><span data-stu-id="22fc9-278">It has the remaining quantity of 2 that wasn't cross-docked and is directed to put-away to storage.</span></span>

1. <span data-ttu-id="22fc9-279">Skráðu þig inn í fartækið sem notandi í vöruhúsi *51*.</span><span class="sxs-lookup"><span data-stu-id="22fc9-279">Sign in to the mobile device as a user in warehouse *51*.</span></span>
1. <span data-ttu-id="22fc9-280">Opnaðu **Á innleið \> Móttaka innkaupa**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-280">Go to **Inbound \> Purchase Receive**.</span></span>
1. <span data-ttu-id="22fc9-281">Sláðu inn innkaupapöntunarnúmer þitt á svæðin **PONum**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-281">In the **PONum** field, enter your purchase order number.</span></span>
1. <span data-ttu-id="22fc9-282">Í reitinn **Magn** skaltu slá inn *5*.</span><span class="sxs-lookup"><span data-stu-id="22fc9-282">In the **Qty** field, enter *5*.</span></span>
1. <span data-ttu-id="22fc9-283">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-283">Select **OK**.</span></span>
1. <span data-ttu-id="22fc9-284">Á næstu síðu skaltu stilla svæðið **Atriði** á *A0001*.</span><span class="sxs-lookup"><span data-stu-id="22fc9-284">On the next page, set the **Item** field to *A0001*.</span></span>
1. <span data-ttu-id="22fc9-285">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-285">Select **OK**.</span></span>
1. <span data-ttu-id="22fc9-286">Á næstu síðu staðfestir þú gildi **Sölupöntunarnúmersins**, **Atriðsins** og **Magnsins** með því að velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-286">On the next page, confirm the **PONum**, **Item**, and **Qty** values by selecting **OK**.</span></span>

    <span data-ttu-id="22fc9-287">Skilaboðin „Vinnu er lokið“ birtast.</span><span class="sxs-lookup"><span data-stu-id="22fc9-287">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="22fc9-288">Veldu **Hætta við** til að hætta.</span><span class="sxs-lookup"><span data-stu-id="22fc9-288">Select **Cancel** to exit.</span></span>

### <a name="put-away-to-cross-docking-and-bulk"></a><span data-ttu-id="22fc9-289">Frágangur dreifingar frá dreifingarstöð og magns</span><span class="sxs-lookup"><span data-stu-id="22fc9-289">Put-away to cross-docking and bulk</span></span>

<span data-ttu-id="22fc9-290">Sem stendur hafa bæði vinnuauðkennin sömu marknúmeraplötu.</span><span class="sxs-lookup"><span data-stu-id="22fc9-290">Currently, both work IDs have the same target license plate.</span></span> <span data-ttu-id="22fc9-291">Til að ljúka næstu skrefum verðurðu að fá vinnuauðkenni og marknúmeraplötu.</span><span class="sxs-lookup"><span data-stu-id="22fc9-291">To complete the next steps, you must get the work ID and the target license plate ID.</span></span> <span data-ttu-id="22fc9-292">Þú færð þessar upplýsingar úr upplýsingum um innkaupapöntunarlínu og sölupöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="22fc9-292">You can get this information from the work details for the purchase order line and the sales order line.</span></span> <span data-ttu-id="22fc9-293">Að öðrum kosti er hægt að fara í **Vöruhúsakerfi \> Vinna \> Upplýsingar um vinnu** og sía fyrir vinnu þar sem gildi **Vöruhúss** er *51*.</span><span class="sxs-lookup"><span data-stu-id="22fc9-293">Alternately, you can go to **Warehouse management \> Work \> Work details** and filter for work where the **Warehouse** value is *51*.</span></span>

1. <span data-ttu-id="22fc9-294">Farðu í fatækið og farðu í **Á innleið \> Frágangur innkaupa** og sláðu inn marknúmeraplötu vinnunnar.</span><span class="sxs-lookup"><span data-stu-id="22fc9-294">On the mobile device, go to **Inbound \> Purchase put-away**, and enter the target license plate from the work.</span></span>
1. <span data-ttu-id="22fc9-295">Í svæðið **Auðkenni** skaltu slá inn auðkenni marknúmeraplötunnar úr upplýsingunum um vinnu.</span><span class="sxs-lookup"><span data-stu-id="22fc9-295">In the **ID** field, enter the target license plate ID from the work details.</span></span>

    <span data-ttu-id="22fc9-296">Tiltektarsíða dreifingar frá dreifingarstöð birtir tiltektarstaðsetninguna (*RECV*), marknúmeraplötuna (*númeraplata*), atriði (*A0001*) og magn (*3*).</span><span class="sxs-lookup"><span data-stu-id="22fc9-296">The cross-docking pick page shows the picking location (*RECV*), target license plate (*license plate*), item (*A0001*), and quantity (*3*).</span></span>

1. <span data-ttu-id="22fc9-297">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-297">Select **OK**.</span></span>
1. <span data-ttu-id="22fc9-298">Í reitinn **Marknúmeraplata** skal færa inn kenni marknúmeraplötuna fyrir auðkenni númeraplötunnar sem skal koma fyrir (dreifa frá dreifingarstöð) til sendingarstaðsetningarinnar.</span><span class="sxs-lookup"><span data-stu-id="22fc9-298">In the **Target LP** field, enter a target license plate for the license plate ID that should be put (cross-docked) to the shipping location.</span></span> <span data-ttu-id="22fc9-299">Hægt er að velja hvaða auðkenni númeraplötu sem er.</span><span class="sxs-lookup"><span data-stu-id="22fc9-299">You can select any license plate ID of your choice.</span></span>
1. <span data-ttu-id="22fc9-300">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-300">Select **OK**.</span></span>
1. <span data-ttu-id="22fc9-301">Á næstu síðu á svæðinu **Auðkenni** slærðu inn auðkenni marknúmeraplötunnar.</span><span class="sxs-lookup"><span data-stu-id="22fc9-301">On the next page, in the **ID** field, enter the target license plate ID.</span></span>
1. <span data-ttu-id="22fc9-302">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-302">Select **OK**.</span></span>
1. <span data-ttu-id="22fc9-303">Staðfestu vinnuna fyrir tiltektina á magninu sem eftir er 2 og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-303">Confirm the work for picking the remaining quantity of 2, and then select **OK**.</span></span>
1. <span data-ttu-id="22fc9-304">Veldu **Lokið** á næstu síðu til að ljúka tiltektarferlinu og hefja frágangsferlið.</span><span class="sxs-lookup"><span data-stu-id="22fc9-304">On the next page, select **Done** to end the picking process and begin the put-away process.</span></span>

    <span data-ttu-id="22fc9-305">Farsímaforritið birtir staðsetninguna og númeraplötuna til að setja atriðið á.</span><span class="sxs-lookup"><span data-stu-id="22fc9-305">The mobile app presents you with the location and license plate to put the item to.</span></span>

1. <span data-ttu-id="22fc9-306">Staðfestu **Frágang** magngeymslu með því að velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-306">Confirm the bulk storage **Put** by selecting **OK**.</span></span>
1. <span data-ttu-id="22fc9-307">Staðfestu **Frágang** dreifingar frá dreifingarstöð á næstu síðu með því að velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="22fc9-307">On the next page, confirm the cross-docking **Put** by selecting **OK**.</span></span>

    <span data-ttu-id="22fc9-308">Skilaboðin „Vinnu er lokið“ birtast.</span><span class="sxs-lookup"><span data-stu-id="22fc9-308">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="22fc9-309">Veldu **Hætta við** til að hætta.</span><span class="sxs-lookup"><span data-stu-id="22fc9-309">Select **Cancel** to exit.</span></span>

<span data-ttu-id="22fc9-310">Eftirfarandi skýringarmynd sýnir hvernig vinna við dreifingu frá dreifingarstöð gæti birst í Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="22fc9-310">The following illustration shows how the completed cross-docking work might appear in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="22fc9-311">![Vinnu við dreifingu frá dreifingarstöð er lokið](media/PlannedCrossDockingWork.png "Vinnu við dreifingu frá dreifingarstöð er lokið")</span><span class="sxs-lookup"><span data-stu-id="22fc9-311">![Cross-docking work completed](media/PlannedCrossDockingWork.png "Cross-docking work completed")</span></span>
