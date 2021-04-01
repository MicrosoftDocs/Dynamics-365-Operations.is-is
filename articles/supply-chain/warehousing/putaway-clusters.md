---
title: Frágangsklasar
description: Frágangsklasar bjóða upp á leið til að tína margar númeraplötur samtímis og ganga síðan frá þeim á mörgum staðsetningum. Þeir geta verið mjög gagnlegir fyrir smásölufyrirtæki þar sem númeraplötur eru yfirleitt ekki heil bretti af birgðum.
author: Mirzaab
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 5552959068d109bffe32b8074666bcd63b57183a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228442"
---
# <a name="putaway-clusters"></a><span data-ttu-id="e4bb0-104">Frágangsklasar</span><span class="sxs-lookup"><span data-stu-id="e4bb0-104">Putaway clusters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e4bb0-105">Frágangsklasar bjóða upp á leið til að tína margar númeraplötur samtímis og ganga síðan frá þeim á mörgum staðsetningum.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-105">Putaway clusters offer a way to pick multiple license plates at the same time and then take them for putaway in different locations.</span></span> <span data-ttu-id="e4bb0-106">Þetta ferli er oft kallað *samflutningur*.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-106">This process is often referred to as a *milk run*.</span></span> <span data-ttu-id="e4bb0-107">Frágangsklasar geta verið mjög gagnlegir fyrir smásölufyrirtæki þar sem númeraplötur eru yfirleitt ekki heil bretti af birgðum.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-107">Putaway clusters can be very useful for retail businesses, where license plates typically aren't full pallets of inventory.</span></span> 

## <a name="turn-on-the-cluster-putaway-feature"></a><span data-ttu-id="e4bb0-108">Kveikja á eiginleika frágangsklasa</span><span class="sxs-lookup"><span data-stu-id="e4bb0-108">Turn on the cluster putaway feature</span></span>

<span data-ttu-id="e4bb0-109">Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-109">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="e4bb0-110">Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="e4bb0-111">Þar er eiginleikinn sýndur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="e4bb0-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e4bb0-112">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="e4bb0-113">**Heiti eiginleika:** *Eiginleiki fyrir frágang klasa*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-113">**Feature name:** *Cluster putaway feature*</span></span>

## <a name="setup-for-the-example-scenario"></a><span data-ttu-id="e4bb0-114">Uppsetning fyrir dæmi um aðstæður</span><span class="sxs-lookup"><span data-stu-id="e4bb0-114">Setup for the example scenario</span></span>

### <a name="cluster-profiles"></a><span data-ttu-id="e4bb0-115">Klasanotandaupplýsingar</span><span class="sxs-lookup"><span data-stu-id="e4bb0-115">Cluster profiles</span></span>

<span data-ttu-id="e4bb0-116">Forstilling frágangsklasa ákvarðar hvert varan fer samkvæmt staðsetningunni sem vörunni er úthlutað þegar hún er móttekin.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-116">The putaway cluster profile determines where an item will go, based on the location that is assigned to the item at the time of receipt.</span></span> <span data-ttu-id="e4bb0-117">Ef krafist er mismunandi klasa skal stofna mismunandi frágangsklasa, einn fyrir hvert valmyndaratriði fartækis.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-117">If different clusters are required, different putaway clusters should be created, one for each mobile device menu item.</span></span>

1. <span data-ttu-id="e4bb0-118">Farðu á **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Klasaforstillingar**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-118">Go to **Warehouse management \> Setup \> Mobile device \> Cluster profiles**.</span></span>
1. <span data-ttu-id="e4bb0-119">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-119">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e4bb0-120">Í **Haus** skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="e4bb0-120">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="e4bb0-121">**Forstillingarkenni frágangsklasa:** *Frágangur klasa*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-121">**Putaway cluster profile ID:** *Cluster putaway*</span></span>
    - <span data-ttu-id="e4bb0-122">**Heiti forstillingarkennis frágangsklasa:** *Frágangur klasa*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-122">**Putaway cluster profile ID Name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="e4bb0-123">**Gerð klasa:** *Frágangur*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-123">**Cluster type:** *Putaway*</span></span>
    - <span data-ttu-id="e4bb0-124">**Raðnúmer:** Samþykkja sjálfgildið.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-124">**Sequence number:** Accept the default value.</span></span>

1. <span data-ttu-id="e4bb0-125">Veljið **Vista** til að gera áskilda reiti í flýtiflipanum **Almennt** tiltæka.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-125">Select **Save** to make the required fields on the **General** FastTab available.</span></span>
1. <span data-ttu-id="e4bb0-126">Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:</span><span class="sxs-lookup"><span data-stu-id="e4bb0-126">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e4bb0-127">**Tímasetning á úthlutun klasa:** *Við móttöku*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-127">**Cluster assignment timing:** *At receipt*</span></span>

        <span data-ttu-id="e4bb0-128">Þessir reitir skilgreina hvort eigi að úthluta frágangsklasa strax þegar tekið er á móti birgðum eða hvort eigi að flokka þá seinna.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-128">This field defines whether the putaway cluster should be assigned immediately when the inventory is received, or whether it should be sorted later.</span></span>

    - <span data-ttu-id="e4bb0-129">**Úthlutunarregla klasa:** *Handvirkt*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-129">**Cluster assignment rule:** *Manual*</span></span>

        <span data-ttu-id="e4bb0-130">Þessi reitur skilgreinir hvort ákveða eigi úthlutun klasans sjálfkrafa af kerfinu eða handvirkt af notanda.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-130">This field defines whether the cluster assignment should be determined automatically by the system or manually by the user.</span></span>

    - <span data-ttu-id="e4bb0-131">**Leiðbeiningarkóði:** Hafðu þetta svæði autt.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-131">**Directive code:** Leave this field blank.</span></span>
    - <span data-ttu-id="e4bb0-132">**Staður frágangsklasa:** *Kvittun*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-132">**Putaway cluster locate:** *Receipt*</span></span>

        <span data-ttu-id="e4bb0-133">Eftirtalin gildi eru tiltæk:</span><span class="sxs-lookup"><span data-stu-id="e4bb0-133">The following values are available:</span></span>

        - <span data-ttu-id="e4bb0-134">**Kvittun** – Staðsetning finnst strax við móttöku.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-134">**Receipt** – A location is found immediately during receipt.</span></span>
        - <span data-ttu-id="e4bb0-135">**Klasalokun** – Staðsetning finnst þegar klasanum er lokað.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-135">**Cluster close** – A location is found when the cluster is closed.</span></span>
        - <span data-ttu-id="e4bb0-136">**Stýrt af notanda** - Staðsetning er fundin þegar númeraplatan er tínd úr klasanum fyrir frágang.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-136">**User directed** – A location is found when the license plate is picked from the cluster for putaway.</span></span> <span data-ttu-id="e4bb0-137">Í þessu tilvikum er engin staðsetning tilgreind þegar frágangsvinna er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-137">In this case, no location is specified when the putaway work is created.</span></span> <span data-ttu-id="e4bb0-138">Við sjálfan fráganginn verður notandinn að skanna númeraplötuna eða verkkennið til að hefja frágangsskrefið.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-138">During the putaway itself, the user must scan the license plate or work ID to initiate the put step.</span></span> <span data-ttu-id="e4bb0-139">Kerfið finnur síðan frágangsstaðsetninguna aftur og segir notandanum hvar á að ganga frá tiltektarmagninu.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-139">The system then finds the put location again and tells the user where to put the picked quantity.</span></span>

    - <span data-ttu-id="e4bb0-140">**Frágangsklasi á hvern notanda:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-140">**Putaway cluster per user:** *No*</span></span>

        <span data-ttu-id="e4bb0-141">Þessi reitur skilgreinir hvort hver klasi eigi að vera einkvæmur fyrir notanda þegar klösum er úthlutað sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-141">This field defines whether each cluster should be unique per user when clusters are automatically assigned.</span></span> <span data-ttu-id="e4bb0-142">Hann er aðeins í boði þegar reiturinn **Úthlutunarregla klasa** er stilltur á *Sjálfvirkur*.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-142">It's available only when the **Cluster assignment rule** field is set to *Automatic*.</span></span>

    - <span data-ttu-id="e4bb0-143">**Takmörkun einingar:** Hafðu reitinn auðan.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-143">**Unit restriction:** Leave this field blank.</span></span>

        <span data-ttu-id="e4bb0-144">Þessi svæði skilgreinir eininguna sem verður að vera móttekin til að forstillingin sé gild.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-144">This field defines the unit that must be received for the profile to be valid.</span></span> <span data-ttu-id="e4bb0-145">Ef þetta er skilið eftir autt eru allar einingar gildar.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-145">If it's left blank, all units are valid.</span></span>

    - <span data-ttu-id="e4bb0-146">**Skipting verkeiningar:** *Út af fyrir sig*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-146">**Work unit break:** *Individual*</span></span>

        <span data-ttu-id="e4bb0-147">Þessi reitur skilgreinir hvort allar birgðir eigi að vera sameinaðar (með því að nota klasakenni og númeraplötu) í eina númeraplötu þegar klasi er lokaður og hvort eigi að ganga frá þeim á einni númeraplötu eða aðskildar á númeraplötum sem tekið var á móti.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-147">This field defines whether all inventory should be consolidated (by using the cluster ID and the license plate) onto one license plate when a cluster is closed, and whether it should be put away as a single license plate or separately on the license plates that were received.</span></span> <span data-ttu-id="e4bb0-148">Þessi reitur er ekki í boði þegar reiturinn **Staður frágangsklasa** er stilltur á *Móttaka*.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-148">This field is unavailable when the **Putaway cluster locate** field is set to *Receipt*.</span></span>

    - <span data-ttu-id="e4bb0-149">**heldur yfireiningu númeraplötu:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-149">**Cluster persists as Parent License Plate:** *No*</span></span>

        <span data-ttu-id="e4bb0-150">Ef þessi valkostur er stilltur á *Já*, þegar frágangsskrefinu er lokið, verður klasakennið að yfireiningu númeraplötu og allar vörur í klasakenninu verða tengdar við þessa yfireiningu númeraplötunnar.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-150">If this option is set to *Yes*, when the put step is completed, the cluster ID will become a parent license plate, and all items on the cluster ID will be linked to that parent license plate.</span></span>

1. <span data-ttu-id="e4bb0-151">Í flýtiflipanum **Klasaröðun** er hægt að skilgreina skilyrði frágangsröðunar.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-151">On the **Cluster sorting** FastTab, you can define putaway sorting criteria.</span></span> <span data-ttu-id="e4bb0-152">Veljið **Ný** í tækjastikunni til að bæta við línu og stillið síðan eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="e4bb0-152">Select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="e4bb0-153">**Raðnúmer:** Samþykkja sjálfgildið.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-153">**Sequence number:** Accept the default value.</span></span>
    - <span data-ttu-id="e4bb0-154">**Heiti reits:** *WMSLocationId*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-154">**Field name:** *WMSLocationId*</span></span>

        <span data-ttu-id="e4bb0-155">Þessi reitur skilgreinir reitinn sem þessi lína á að nota sem röðunarskilyrði.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-155">This field defines the field that this line should use as a sorting criterion.</span></span>

    - <span data-ttu-id="e4bb0-156">**Röðun:** - Veljið *Hækkandi*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-156">**Sorting:** *Ascending*</span></span>

        <span data-ttu-id="e4bb0-157">Þessi reitur skilgreinir hvort á að framkvæma röðun í hækkandi eða lækkandi röð.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-157">This field defines whether sorting should be done in ascending or descending order.</span></span>

1. <span data-ttu-id="e4bb0-158">Í flýtiflipanum **Vinnusniðmát klasa** skal velja **Ný** í tækjastikunni til að bæta við línu og stillið síðan eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="e4bb0-158">On the **Cluster work template** FastTab, select **New** on the toolbar to add a line, and then set the following values:</span></span>

    - <span data-ttu-id="e4bb0-159">**Gerð verkbeiðni:** *Innkaupapantanir*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-159">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="e4bb0-160">**Vinnusniðmát:** *61 PO Direct*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-160">**Work template:** *61 PO Direct*</span></span>

1. <span data-ttu-id="e4bb0-161">Á aðgerðasvæðinu skal velja **Vista** og síðan velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-161">On the Action Pane, select **Save**, and then select **Edit query**.</span></span>
1. <span data-ttu-id="e4bb0-162">Í **Frágangur klasa** svarglugganum á flipanum **Svið** velur þú **Bæta við** til að bæta annari línu við fyrirspurnina.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-162">In the **Cluster putaway** dialog box, on the **Range** tab, select **Add** to add a second line to the query.</span></span> <span data-ttu-id="e4bb0-163">Uppfærið síðan fyrirspurnarlínurnar eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-163">Then update the query lines as shown in the following table.</span></span>

    | <span data-ttu-id="e4bb0-164">Tafla</span><span class="sxs-lookup"><span data-stu-id="e4bb0-164">Table</span></span> | <span data-ttu-id="e4bb0-165">Afleidd tafla</span><span class="sxs-lookup"><span data-stu-id="e4bb0-165">Derived table</span></span> | <span data-ttu-id="e4bb0-166">Svæði</span><span class="sxs-lookup"><span data-stu-id="e4bb0-166">Field</span></span> | <span data-ttu-id="e4bb0-167">Skilyrði</span><span class="sxs-lookup"><span data-stu-id="e4bb0-167">Criteria</span></span> |
    |---|---|---|---|
    | <span data-ttu-id="e4bb0-168">Starf</span><span class="sxs-lookup"><span data-stu-id="e4bb0-168">Work</span></span> | <span data-ttu-id="e4bb0-169">Starf</span><span class="sxs-lookup"><span data-stu-id="e4bb0-169">Work</span></span> | <span data-ttu-id="e4bb0-170">Vöruhús</span><span class="sxs-lookup"><span data-stu-id="e4bb0-170">Warehouse</span></span> | <span data-ttu-id="e4bb0-171">*61*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-171">*61*</span></span> |
    | <span data-ttu-id="e4bb0-172">Starf</span><span class="sxs-lookup"><span data-stu-id="e4bb0-172">Work</span></span> | <span data-ttu-id="e4bb0-173">Starf</span><span class="sxs-lookup"><span data-stu-id="e4bb0-173">Work</span></span> | <span data-ttu-id="e4bb0-174">Auðkenni vinnu</span><span class="sxs-lookup"><span data-stu-id="e4bb0-174">Work ID</span></span> | <span data-ttu-id="e4bb0-175">Hafa reitinn auðann.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-175">Leave this field blank.</span></span> |

1. <span data-ttu-id="e4bb0-176">Veldu **Í lagi** til að vista fyrirspurnina og lokaðu glugganum.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-176">Select **OK** to save the query and close the dialog box.</span></span>
1. <span data-ttu-id="e4bb0-177">Í aðgerðarúðunni skal velja **Vista** og loka síðunni.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-177">On the Action Pane, select **Save**, and close the page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e4bb0-178">Reitir í klasaforstillingunni sem eru skyggðir þegar **Mynda klasaauðkenni** er stillt á *Já* eru ekki tiltækir og verða ekki notaðir þegar þessi eiginleiki er notaður.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-178">Fields in the cluster profile that appear dimmed when **Generate cluster ID** is set to *Yes* are unavailable and won't be considered when this feature is used.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="e4bb0-179">Valmyndaratriði fartækis</span><span class="sxs-lookup"><span data-stu-id="e4bb0-179">Mobile device menu items</span></span>

<span data-ttu-id="e4bb0-180">Tvö valmyndaratriði í fartæki eru tiltæk fyrir þennan eiginleika.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-180">Two new mobile device menu items are available for this feature.</span></span> <span data-ttu-id="e4bb0-181">Valmyndaratriðið **Taka á móti og raða klasa** er notað til að raða mótteknum birgðum í frágangsklasa við móttöku.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-181">The **Receive and sort cluster** menu item is used to sort the received inventory into a putaway cluster upon receipt.</span></span> <span data-ttu-id="e4bb0-182">Valmyndaratriðið **Frágangur klasa** er notað til að setja klasann í gang eftir að honum hefur verið úthlutað.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-182">The **Cluster putaway** menu item is used to put the cluster away after it has been assigned.</span></span>

#### <a name="receive-and-sort-cluster"></a><span data-ttu-id="e4bb0-183">Taka á móti og raða klasa</span><span class="sxs-lookup"><span data-stu-id="e4bb0-183">Receive and sort cluster</span></span>

<span data-ttu-id="e4bb0-184">Stofnið nýtt valmyndaratriði fartækis til að taka á móti birgðum og raða þeim í klasa.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-184">Create a new mobile device menu item for receiving inventory and sorting into a cluster.</span></span> <span data-ttu-id="e4bb0-185">Þetta valmyndaratriði stofnar vinnu á innleið eftir að birgðir hafa verið mótteknar, en það gefur til kynna að valmyndaratriðið móttöku verður notað fyrir frágangsklasa.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-185">This menu item will create inbound work after inventory is received, which indicates that the receiving menu item will be used for putaway clusters.</span></span>

> [!NOTE]
> <span data-ttu-id="e4bb0-186">Hægt er að nota valmyndaratriðið **Taka á móti og raða klasa** með eftirfarandi valmyndaratriðum móttöku:</span><span class="sxs-lookup"><span data-stu-id="e4bb0-186">The **Receive and sort cluster** menu item can be used with the following receiving menu items:</span></span>
>
> - <span data-ttu-id="e4bb0-187">Móttaka innkaupapöntunarlínu</span><span class="sxs-lookup"><span data-stu-id="e4bb0-187">Purchase order line receiving</span></span>
> - <span data-ttu-id="e4bb0-188">Móttaka innkaupapöntunarvöru</span><span class="sxs-lookup"><span data-stu-id="e4bb0-188">Purchase order item receiving</span></span>
> - <span data-ttu-id="e4bb0-189">Móttaka farmvöru</span><span class="sxs-lookup"><span data-stu-id="e4bb0-189">Load item receiving</span></span>

1. <span data-ttu-id="e4bb0-190">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-190">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="e4bb0-191">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-191">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e4bb0-192">Í **Haus** skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="e4bb0-192">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="e4bb0-193">**Heiti valmyndaratriðis:** *Taka á móti og raða klasa*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-193">**Menu item name:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="e4bb0-194">**Titill:** *Taka á móti og raða klasa*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-194">**Title:** *Receive and sort cluster*</span></span>
    - <span data-ttu-id="e4bb0-195">**Máti:** *Vinna*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-195">**Mode:** *Work*</span></span>
    - <span data-ttu-id="e4bb0-196">**Nota fyrirliggjandi vinnu:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-196">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="e4bb0-197">Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:</span><span class="sxs-lookup"><span data-stu-id="e4bb0-197">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="e4bb0-198">**Ferli verkstofnunar:** *Móttaka innkaupapöntunarvöru*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-198">**Work creation process:** *Purchase order item receiving*</span></span>
    - <span data-ttu-id="e4bb0-199">**Mynda númeraplötu:** *Já*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-199">**Generate license plate:** *Yes*</span></span>
    - <span data-ttu-id="e4bb0-200">**Úthluta frágangsklasa:** *Já*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-200">**Assign putaway cluster:** *Yes*</span></span>

        > [!NOTE]
        > <span data-ttu-id="e4bb0-201">Valkosturinn **Úthluta frágangsklasa** er aðeins í boði fyrir eins skrefs aðgerðina *Ferli verkstofnunar* fyrir móttöku.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-201">The **Assign putaway cluster** option is available only for the one-step *Work creation process* activity for receiving.</span></span>

    <span data-ttu-id="e4bb0-202">Samþykkið sjálfgefin gildi fyrir reitina sem eftir eru.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-202">Accept the default values for the remaining fields.</span></span>

1. <span data-ttu-id="e4bb0-203">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-203">On the Action Pane, select **Save**.</span></span>

#### <a name="cluster-putaway"></a><span data-ttu-id="e4bb0-204">Frágangur klasa</span><span class="sxs-lookup"><span data-stu-id="e4bb0-204">Cluster putaway</span></span>

<span data-ttu-id="e4bb0-205">Stofnið nýtt valmyndaratriði fartækis fyrir frágang klasans eftir að honum hefur verið úthlutað.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-205">Create a new mobile device menu item for putting the cluster away after it has been assigned.</span></span>

1. <span data-ttu-id="e4bb0-206">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-206">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="e4bb0-207">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-207">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e4bb0-208">Í **Haus** skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="e4bb0-208">In the **Header** view, set the following values:</span></span>

    - <span data-ttu-id="e4bb0-209">**Nafn valmyndaratriðis:** *Frágangsklasi*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-209">**Menu item name:** *Cluster putaway*</span></span>
    - <span data-ttu-id="e4bb0-210">**Titill:** *Frágangur klasa*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-210">**Title:** *Cluster putaway*</span></span>
    - <span data-ttu-id="e4bb0-211">**Máti:** *Vinna*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-211">**Mode:** *Work*</span></span>
    - <span data-ttu-id="e4bb0-212">**Nota fyrirliggjandi vinnu:** *Já*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-212">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="e4bb0-213">Í flýtiflipanum **Almennt** skal stilla reitinn **Stjórnað af** á *Frágangur klasa*.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-213">On the **General** FastTab, set the **Directed by** field to *Cluster putaway*.</span></span> <span data-ttu-id="e4bb0-214">Samþykkið sjálfgefin gildi fyrir reitina sem eftir eru.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-214">Accept the default values for the remaining fields.</span></span>
1. <span data-ttu-id="e4bb0-215">Í flýtiflipanum **Vinnuklasar** skal setja upp gildan vinnuklasa fyrir þetta valmyndaratriði fartækis:</span><span class="sxs-lookup"><span data-stu-id="e4bb0-215">On the **Work classes** FastTab, set up the valid work class for this mobile device menu item:</span></span>

    - <span data-ttu-id="e4bb0-216">**Auðkenni vinnuklasa:** *Innkaup*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-216">**Work class ID:** *Purchase*</span></span>
    - <span data-ttu-id="e4bb0-217">**Gerð verkbeiðni:** *Innkaupapantanir*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-217">**Work order type:** *Purchase orders*</span></span>

1. <span data-ttu-id="e4bb0-218">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-218">On the Action Pane, select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="e4bb0-219">Valmynd fartækis</span><span class="sxs-lookup"><span data-stu-id="e4bb0-219">Mobile device menu</span></span>

<span data-ttu-id="e4bb0-220">Bætið valmyndaratriðunum sem voru stofnuð við valmynd fyrir á innleið í farsímaforritinu.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-220">Add the menu items that you just created to the inbound menu of the mobile app.</span></span>

1. <span data-ttu-id="e4bb0-221">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-221">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="e4bb0-222">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-222">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="e4bb0-223">Í valmyndarlistanum skal velja **Á innleið**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-223">In the menu list, select **Inbound**.</span></span>
1. <span data-ttu-id="e4bb0-224">Í listanum **Tiltækar valmyndir og valmyndaratriði** skal finna og velja **Taka á móti og raða klasa**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-224">In the **Available menus and menu items** list, find and select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="e4bb0-225">Veldu hægri örvarhnappinn til að færa valda valmyndaratriðið á listann **Valmyndarskipan**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-225">Select the right arrow button to move the selected menu item to the **Menu structure** list.</span></span>
1. <span data-ttu-id="e4bb0-226">Notið örvarhnappana upp/niður til að færa valmyndaratriðið á æskilegan stað í valmyndinni.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-226">Use the up arrow or down arrow button to move the menu item into the desired position in the menu.</span></span>
1. <span data-ttu-id="e4bb0-227">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-227">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4bb0-228">Endurtakið skref 4 til 7 til að bæta við eftirstandandi valmyndaratriðum:</span><span class="sxs-lookup"><span data-stu-id="e4bb0-228">Repeat steps 4 through 7 to add the remaining menu items:</span></span>

    - <span data-ttu-id="e4bb0-229">Úthluta klasa</span><span class="sxs-lookup"><span data-stu-id="e4bb0-229">Assign cluster</span></span>
    - <span data-ttu-id="e4bb0-230">Frágangur klasa</span><span class="sxs-lookup"><span data-stu-id="e4bb0-230">Cluster putaway</span></span>

## <a name="example-scenario"></a><span data-ttu-id="e4bb0-231">Dæmi</span><span class="sxs-lookup"><span data-stu-id="e4bb0-231">Example scenario</span></span>

<span data-ttu-id="e4bb0-232">Þessar aðstæður herma eftir ferli frágangsklasa.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-232">This scenario simulates putaway cluster processing.</span></span>

### <a name="create-a-purchase-order"></a><span data-ttu-id="e4bb0-233">Stofna innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="e4bb0-233">Create a purchase order</span></span>

1. <span data-ttu-id="e4bb0-234">Opnið **Viðskiptaskuldir \> Innkaupapantanir \> Allar innkaupapantanir**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-234">Go to **Accounts payable \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="e4bb0-235">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-235">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e4bb0-236">Sláðu inn eftirfarandi gildi í svarglugganum **Búa til innkaupapöntun**:</span><span class="sxs-lookup"><span data-stu-id="e4bb0-236">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="e4bb0-237">**Lánardrottnalykill:** *1001*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-237">**Vendor account:** *1001*</span></span>
    - <span data-ttu-id="e4bb0-238">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-238">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="e4bb0-239">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-239">Select **OK**.</span></span>

    <span data-ttu-id="e4bb0-240">Síðan **Allar innkaupapantanir** birtist.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-240">The **All purchase orders** page appears.</span></span>

1. <span data-ttu-id="e4bb0-241">Á síðunni **Allar innkaupapantanir**, í flýtiflipanum **Innkaupapöntunarlínur**, skal nota hnappinn **Bæta við línu** til að bæta við eftirfarandi línum:</span><span class="sxs-lookup"><span data-stu-id="e4bb0-241">On the **All purchase orders** page, on the **Purchase order lines** FastTab, use the **Add line** button to add the following lines:</span></span>

    - <span data-ttu-id="e4bb0-242">Innkaupapöntunarlína 1:</span><span class="sxs-lookup"><span data-stu-id="e4bb0-242">Purchase order line 1:</span></span>

        - <span data-ttu-id="e4bb0-243">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-243">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="e4bb0-244">**Magn:** *10*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-244">**Quantity:** *10*</span></span>

    - <span data-ttu-id="e4bb0-245">Innkaupapöntunarlína 2:</span><span class="sxs-lookup"><span data-stu-id="e4bb0-245">Purchase order line 2:</span></span>

        - <span data-ttu-id="e4bb0-246">**Vörunúmer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-246">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="e4bb0-247">**Magn:** *20*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-247">**Quantity:** *20*</span></span>

    - <span data-ttu-id="e4bb0-248">Innkaupapöntunarlína 3:</span><span class="sxs-lookup"><span data-stu-id="e4bb0-248">Purchase order line 3:</span></span>

        - <span data-ttu-id="e4bb0-249">**Vörunúmer:** *M9215*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-249">**Item number:** *M9215*</span></span>
        - <span data-ttu-id="e4bb0-250">**Magn:** *30*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-250">**Quantity:** *30*</span></span>

1. <span data-ttu-id="e4bb0-251">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-251">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="e4bb0-252">Skráið niður innkaupapöntunarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-252">Make a note of the purchase order number.</span></span>

### <a name="receive-inventory-and-put-it-away-from-the-mobile-device"></a><span data-ttu-id="e4bb0-253">Taka við birgðum og ganga frá úr fartæki</span><span class="sxs-lookup"><span data-stu-id="e4bb0-253">Receive inventory and put it away from the mobile device</span></span>

#### <a name="receive-and-sort-the-inventory-into-a-cluster"></a><span data-ttu-id="e4bb0-254">Taka við og raða birgðum í klasa</span><span class="sxs-lookup"><span data-stu-id="e4bb0-254">Receive and sort the inventory into a cluster</span></span>

1. <span data-ttu-id="e4bb0-255">Skráðu þig inn í vöruhúsaforritið sem notandi sem er virkjaður fyrir vöruhús *61*.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-255">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="e4bb0-256">Í aðalvalmyndinni skal velja **Á innleið**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-256">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="e4bb0-257">Í valmyndinni **Á innleið** skal velja **Taka á móti og raða klasa**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-257">On the **Inbound** menu, select **Receive and sort cluster**.</span></span>
1. <span data-ttu-id="e4bb0-258">Í reitinn **Ponum** skal slá inn innkaupapöntunarnúmerið.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-258">In the **Ponum** field, enter the purchase order number.</span></span>
1. <span data-ttu-id="e4bb0-259">Veljið **Í lagi** (hnappurinn með gátmerki).</span><span class="sxs-lookup"><span data-stu-id="e4bb0-259">Select **OK** (the check mark button).</span></span>
1. <span data-ttu-id="e4bb0-260">Veljið reitinn **Vara**, færið inn vörunúmer *A0001* og veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-260">Select the **Item** field, enter item number *A0001*, and then select **OK**.</span></span>
1. <span data-ttu-id="e4bb0-261">Veljið reitinn **Magn**, færið inn *10* með því að nota talnaborðið og veljið síðan gátmerkishnappinn.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-261">Select the **Qty** field, enter *10* by using the number pad, and then select the check mark button.</span></span>
1. <span data-ttu-id="e4bb0-262">Á verksíðunni **Magn** skal velja **Í lagi** (gátmerkishnappurinn) til að staðfesta magnið sem slegið var inn.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-262">On the **Qty** task page, select **OK** (the check mark button) to confirm the quantity that you entered.</span></span>
1. <span data-ttu-id="e4bb0-263">Á verksíðunni **Vara** skal velja **Í lagi** til að staðfesta að varan *A0001* hafi verið færð inn.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-263">On the **Item** task page, select **OK** to confirm that item *A0001* was entered.</span></span>
1. <span data-ttu-id="e4bb0-264">Veljið reitinn **Klasakenni** og færið inn gildi til að úthluta kenni fyrir klasann sem er stofnaður.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-264">Select the **Cluster ID** field, and enter a value to assign an ID for the cluster that you're creating.</span></span>

    <span data-ttu-id="e4bb0-265">Kennið sem var fært inn hér verður notað þegar tvær eftirstandandi vörur í innkaupapöntuninni eru mótteknar.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-265">The ID that you enter here will be used when the two remaining items on the purchase order are received.</span></span>

1. <span data-ttu-id="e4bb0-266">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-266">Select **OK**.</span></span>

    <span data-ttu-id="e4bb0-267">Verksíðan **Ponum** birtist og sýnir skilaboðin „Vinnu lokið“.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-267">The **Ponum** task page appears and shows a "Work completed" message.</span></span>

    <span data-ttu-id="e4bb0-268">Vara *A0001* hefur nú verið móttekin á staðsetningu *RECV* og úthlutað á klasakenni sem fært var inn í skrefi 10.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-268">Item *A0001* has now been received into the *RECV* location and assigned to the cluster ID that you entered in step 10.</span></span>

1. <span data-ttu-id="e4bb0-269">Endurtakið skref 4 til 11 til að fá eftirstandandi tvær vörur úr innkaupapöntuninni og úthluta þeim á klasakennið:</span><span class="sxs-lookup"><span data-stu-id="e4bb0-269">Repeat steps 4 through 11 to receive the remaining two items from the purchase order and assign them to the cluster ID:</span></span>

    - <span data-ttu-id="e4bb0-270">Magn upp á *20* fyrir atriði *A0002*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-270">A quantity of *20* for item *A0002*</span></span>
    - <span data-ttu-id="e4bb0-271">Magn upp á *30* fyrir atriði *M9215*</span><span class="sxs-lookup"><span data-stu-id="e4bb0-271">A quantity of *30* for item *M9215*</span></span>

#### <a name="close-the-cluster"></a><span data-ttu-id="e4bb0-272">Loka klasa</span><span class="sxs-lookup"><span data-stu-id="e4bb0-272">Close the cluster</span></span>

<span data-ttu-id="e4bb0-273">Áður en hægt verður að ganga frá vörunum, verður að loka klasanum.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-273">Before the items in the cluster can be put away, the cluster must be closed.</span></span>

1. <span data-ttu-id="e4bb0-274">Í Supply Chain Management skal fara í **Vöruhúsakerfi \> Verk \> Á útleið \> Verkklasar**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-274">In Supply Chain Management, go to **Warehouse management \> Work \> Outbound \> Work clusters**.</span></span>
1. <span data-ttu-id="e4bb0-275">Á síðunni **Verkklasar**, í hlutanum **Verkklasi**, skal leita í reitnum **Klasakenni** að klasakenninu sem var fært inn hér á undan.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-275">On the **Work clusters** page, in the **Work cluster** section, search the **Cluster ID** field for the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="e4bb0-276">Ef klasinn birtist ekki, gæti þegar verið búið að loka honum.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-276">If the cluster isn't shown, it might already have been closed.</span></span> <span data-ttu-id="e4bb0-277">Til að komast að því hvort klasanum hafi verið lokað skal velja gátreitinn **Sýna lokað verk** og leita að klasakenninu sem fært var inn hér á undan.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-277">To determine whether the cluster was closed, select the **Show closed work** check box, and search for the cluster ID that you entered earlier.</span></span> <span data-ttu-id="e4bb0-278">Fylgið síðan einu af eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="e4bb0-278">Then follow one of these steps:</span></span>

    - <span data-ttu-id="e4bb0-279">Ef klasanum hefur verið lokað skal hoppa yfir skrefin sem eftir eru í ferlinu og fara yfir í næsta ferli, [Ganga frá klasa](#put-the-cluster-away).</span><span class="sxs-lookup"><span data-stu-id="e4bb0-279">If the cluster has been closed, skip the remaining steps of this procedure, and move on to the next procedure, [Put the cluster away](#put-the-cluster-away).</span></span>
    - <span data-ttu-id="e4bb0-280">Ef klasanum hefur ekki verið lokað skal fara í gegnum skrefin sem eftir eru í þessu ferli til að loka klasanum handvirkt.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-280">If the cluster hasn't been closed, follow the remaining steps of this procedure to manually close the cluster.</span></span> <span data-ttu-id="e4bb0-281">Færðu þig svo yfir í næsta ferli.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-281">Then move on to the next procedure.</span></span>

1. <span data-ttu-id="e4bb0-282">Í hlutanum **Verkklasi** skal velja klasakennið sem fært var inn hér á undan.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-282">In the **Work cluster** section, select the cluster ID that you entered earlier.</span></span>
1. <span data-ttu-id="e4bb0-283">Á aðgerðasvæðinu skal velja **Loka klasa**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-283">On the Action Pane, select **Close cluster**.</span></span>

    <span data-ttu-id="e4bb0-284">Þegar klasanum hefur verið lokað, birtist hann ekki lengur í hlutanum **Verkklasi** (nema ef gátreiturinn **Sýna lokað verk** er valinn).</span><span class="sxs-lookup"><span data-stu-id="e4bb0-284">After the cluster has been closed, it's no longer shown in the **Work cluster** section (unless the **Show closed work** check box is selected).</span></span>

#### <a name="put-the-cluster-away"></a><span data-ttu-id="e4bb0-285">Ganga frá klasa</span><span class="sxs-lookup"><span data-stu-id="e4bb0-285">Put the cluster away</span></span>

1. <span data-ttu-id="e4bb0-286">Skráðu þig inn í vöruhúsaforritið sem notandi sem er virkjaður fyrir vöruhús *61*.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-286">Sign in to the warehouse app as a user who is set up for warehouse *61*.</span></span>
1. <span data-ttu-id="e4bb0-287">Í aðalvalmyndinni skal velja **Á innleið**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-287">On the main menu, select **Inbound**.</span></span>
1. <span data-ttu-id="e4bb0-288">Á valmyndinni **Á innleið** skal velja **Frágangur klasa**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-288">On the **Inbound** menu, select **Cluster putaway**.</span></span>
1. <span data-ttu-id="e4bb0-289">Veljið **Klasakenni** og færið inn klasakennið sem var fært inn áður fyrir lokaða klasann.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-289">Select **Cluster ID**, and enter the cluster ID that you entered earlier for the closed cluster.</span></span>
1. <span data-ttu-id="e4bb0-290">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-290">Select **OK**.</span></span>

    <span data-ttu-id="e4bb0-291">Síðan **Klasafrágangur: Tiltekt** opnast.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-291">The **Cluster putaway: Pick** page appears.</span></span> <span data-ttu-id="e4bb0-292">Hún sýnir klasakennið, tiltektarstaðsetninguna, vörurnar (gildið *Margfalt* verður sýnt) og heildarmagnið í klasanum sem verður að tína.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-292">It shows the cluster ID, the picking location, the items (the value *Multiple* will be shown), and the total quantity in the cluster that must be picked.</span></span>

1. <span data-ttu-id="e4bb0-293">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-293">Select **OK**.</span></span>

    <span data-ttu-id="e4bb0-294">Síðan **Klasafrágangur: Frágangur** opnast.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-294">The **Cluster putaway: Put** page appears.</span></span> <span data-ttu-id="e4bb0-295">Leiðbeiningarnar fyrir **Frágang** bera kennsl á klasakennið, frágangsstaðsetninguna, vörurnar, heildarmagnið og númeraplötukennin fyrir vörurnar sem tekið hefur verið á móti í klasanum.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-295">The **Put** instructions identify the cluster ID, the put location, the items, the total quantity, and the license plate IDs for the items that have been received on the cluster.</span></span>

    <span data-ttu-id="e4bb0-296">Þú ert með hefðbundnu valkostina til að hunsa eða hoppa yfir þetta skref.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-296">You have the standard options to override or pass this step.</span></span>

    <span data-ttu-id="e4bb0-297">![Frágangur klasa: Frágangssíða](media/Cluster_putaway-Put.png "Frágangur klasa: setja síðu")</span><span class="sxs-lookup"><span data-stu-id="e4bb0-297">![Cluster putaway: Put page](media/Cluster_putaway-Put.png "Cluster putaway: Put page")</span></span>

1. <span data-ttu-id="e4bb0-298">Veljið **Í lagi** til að staðfesta frágang klasans.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-298">Select **OK** to confirm the putaway of the cluster.</span></span>

    <span data-ttu-id="e4bb0-299">Skilaboðin „Klasa lokið“ birtast.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-299">A "Cluster completed" message is shown.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="e4bb0-300">Athugasemdir og ábendingar</span><span class="sxs-lookup"><span data-stu-id="e4bb0-300">Notes and tips</span></span>

<span data-ttu-id="e4bb0-301">Í tilvikum þar sem klasakennið verður að yfireiningu númeraplötunnar fyrir faldað bretti, verður frágangsstaðurinn sjálfkrafa gefinn þegar klasakennið er skannað.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-301">For cases where the cluster ID becomes the parent license plate for a nested pallet, the put position is automatically given when the cluster ID is scanned.</span></span> <span data-ttu-id="e4bb0-302">Ekki þarf frekari skönnun númeraplötu, jafnvel þótt myndun númeraplötu sé stillt á handvirkt.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-302">No further license plate must be scanned, even if license plate generation is set to manual.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]