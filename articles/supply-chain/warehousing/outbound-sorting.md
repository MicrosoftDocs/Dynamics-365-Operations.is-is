---
title: Flokkun á útleið
description: Þetta efnisatriði gefur upplýsingar um flokkun á útleið. Þessi virkni auðveldar meðhöndlun lítilla gáma og hjálpar starfsmönnum vöruhúss að áætla og skipuleggja betur brettagetu í flutningabílnum.
author: Mirzaab
manager: tfehr
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPack, WHSOutboundSortTemplate, WHSOutboundSortPositionAssignments, WHSLocationType, WHSLoactionProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 84c4ec83ed16762e6c3c1a22425cf60e5b3ae8da
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017691"
---
# <a name="outbound-sorting"></a><span data-ttu-id="5f1a4-104">Flokkun á útleið</span><span class="sxs-lookup"><span data-stu-id="5f1a4-104">Outbound sorting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f1a4-105">Þessi virkni auðveldar meðhöndlun lítilla gáma og hjálpar starfsmönnum vöruhúss að áætla og skipuleggja betur brettagetu í flutningabílnum.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-105">This functionality makes it easier to handle small containers and helps warehouse workers better plan and organize pallet capacity in the truck.</span></span> <span data-ttu-id="5f1a4-106">Þegar flokkun á útleið er notuð er hægt að raða pökkuðum gámum á rétt bretti eftir að þeir hafa verið á pökkunarstöðinni.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-106">When you use outbound sorting, you can sort packed containers to the correct pallet after they have been at a packing station.</span></span> <span data-ttu-id="5f1a4-107">Einnig er hægt að búa til pökkunarstigveldi.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-107">You can also build a packing hierarchy.</span></span>

<span data-ttu-id="5f1a4-108">Þessi virkni gerir þér kleift að búa til bretti úr gámum sem eru pakkaðir í gegnum pökkunaraðgerðina.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-108">This functionality lets you build pallets from containers that are packed through the packing functionality.</span></span> <span data-ttu-id="5f1a4-109">Gámurinn er ekki sendur á endanlegan sendingarstað eins og gerist í upprunalega pökkunarflæðinu.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-109">The container isn't sent to the final shipping location as it is in the original packing flow.</span></span> <span data-ttu-id="5f1a4-110">Í staðinn geta starfsmenn lokað gámnum og fært hann yfir í staðsetningu röðunargerðar.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-110">Instead, workers can close the container and move it to a sort type location.</span></span> <span data-ttu-id="5f1a4-111">Þeir geta síðan raðað gámum á staðsetningar, hver staðsetning er með númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-111">They can then sort containers to positions, each of which has a license plate (LP).</span></span> <span data-ttu-id="5f1a4-112">Eftir að gámunum hefur verið raðað er hægt að búa til vinnu til að senda alla númeraplötuna að lokaafhendingarstað eða biðsvæðum byggt á staðsetningarleiðbeiningum viðskiptavina eða þínum eigin leiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-112">After the containers have been sorted, work can be created to send the whole LP to the final shipping dock or stage locations, based on location directives or your own requirements.</span></span> <span data-ttu-id="5f1a4-113">Að auki getur lokun röðunarstaðsetningar flutt birgðirnar strax til lokaafhendingarstaðs og tínt hana fyrir pöntunina.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-113">Additionally, the action of closing of the sort position can immediately move the inventory to the final shipping location and pick it to the order.</span></span>

## <a name="turn-on-the-outbound-sorting-feature"></a><span data-ttu-id="5f1a4-114">Kveikja á eiginleika flokkunar á útleið</span><span class="sxs-lookup"><span data-stu-id="5f1a4-114">Turn on the Outbound sorting feature</span></span>

<span data-ttu-id="5f1a4-115">Áður en hægt er að nota eiginleikann verður að vera kveikt á honum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-115">Before you can use the feature, it must be turned on in your system.</span></span> <span data-ttu-id="5f1a4-116">Stjórnendur geta notað vinnusvæði [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-116">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="5f1a4-117">Þar er eiginleikinn sýndur á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-117">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="5f1a4-118">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="5f1a4-119">**Heiti eiginleika:** *Flokkun á útleið*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-119">**Feature name:** *Outbound sorting*</span></span>

## <a name="setup"></a><span data-ttu-id="5f1a4-120">Setja upp</span><span class="sxs-lookup"><span data-stu-id="5f1a4-120">Setup</span></span>

<span data-ttu-id="5f1a4-121">Fyrir þessa atburðarás verður þú að nota hefðbundin sýnigögn **USMF** og vöruhús *62*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-121">For this scenario, you must use standard **USMF** demo data and warehouse *62*.</span></span> <span data-ttu-id="5f1a4-122">Einnig þarf að ljúka uppsetningunni sem lýst er í eftirfarandi undirköflum.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-122">You must also complete the setup that is described in the following subsections.</span></span>

### <a name="set-up-a-wave-template"></a><span data-ttu-id="5f1a4-123">Velja bylgjusniðmát</span><span class="sxs-lookup"><span data-stu-id="5f1a4-123">Set up a wave template</span></span>

<span data-ttu-id="5f1a4-124">Þessi uppsetning vinnur sjálfkrafa úr bylgjunni og stofna vinnu þegar lína er losuð í vöruhús.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-124">This setup automatically processes the wave and creates work when a line is released to the warehouse.</span></span>

1. <span data-ttu-id="5f1a4-125">Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-125">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="5f1a4-126">Í sniðmátslistanum velurðu **Vöruhús 62**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-126">In the template list, select **Warehouse 62**.</span></span>
1. <span data-ttu-id="5f1a4-127">Í flýtiflipanum **Almennt** skal ganga úr skugga um að valkosturinn **Vinna úr bylgju við losun í vöruhús** sé stilltur á *Já*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-127">On the **General** FastTab, make sure that the **Process wave at release to warehouse** option is set to *Yes*.</span></span>

### <a name="set-up-a-worker"></a><span data-ttu-id="5f1a4-128">Setja upp starfskraft</span><span class="sxs-lookup"><span data-stu-id="5f1a4-128">Set up a worker</span></span>

<span data-ttu-id="5f1a4-129">Pökkunarstöðin er talin staðsetning.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-129">The packing station is considered a location.</span></span> <span data-ttu-id="5f1a4-130">Starfsmenn vöruhúss sem skrá sig inn á pökkunarstöðinni sjá og vinna aðeins með sendingar og gáma sem áætlaðir eru á þessari tilteknu pökkunarstaðsetningu.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-130">Warehouse workers who sign in at the packing station see and work on only shipments and containers that are planned at that specific packing location.</span></span> <span data-ttu-id="5f1a4-131">Notandi sem skráir sig inn á Microsoft Dynamics 365 verður að vera settur upp sem starfsmaður í vöruhúsakerfi.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-131">A user who signs in to Microsoft Dynamics 365 must be set up as a worker in Warehouse management.</span></span> <span data-ttu-id="5f1a4-132">Ef nafn notandans birtist ekki á listanum yfir vinnunotendur, skal nota eftirfarandi ferli til að bæta því við.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-132">If the user's name doesn't appear in the list of work users, use the following procedure to add it.</span></span>

> [!NOTE]
> <span data-ttu-id="5f1a4-133">Þessi skref gera ráð fyrir að notandinn sé þegar til í kerfinu og hafi verið tengdur starfsmaður eða starfskraftur í einingunni **Mannauður**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-133">These steps assume that the user already exists in the system and has been associated as an employee or worker in the **Human Resources** module.</span></span>

1. <span data-ttu-id="5f1a4-134">Fara í **Vöruhúsakerfi \> Uppsetning \> Starfskraftur**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-134">Go to **Warehouse management \> Setup \> Worker**.</span></span>
1. <span data-ttu-id="5f1a4-135">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-135">Select **New**.</span></span>
1. <span data-ttu-id="5f1a4-136">Í reitnum **Starfskraftur** skal velja notandann í listanum yfir starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-136">In the **Worker** field, select the target user in the list of employees.</span></span>
1. <span data-ttu-id="5f1a4-137">Veljið **Velja**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-137">Select **Select**.</span></span>
1. <span data-ttu-id="5f1a4-138">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-138">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="5f1a4-139">Í flýtiflipanum **Notendur** skal velja **Nýr** til að stofna reikning í fartæki og stilla eftirfarandi gildi fyrir hann:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-139">On the **Users** FastTab, select **New** to create a mobile device account, and set the following values for it:</span></span>

    - <span data-ttu-id="5f1a4-140">**Notandakenni:** Færðu inn einkvæmt kenni.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-140">**User ID:** Enter a unique ID.</span></span>
    - <span data-ttu-id="5f1a4-141">**Notandanafn:** Færið inn heiti fyrir auðkennið.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-141">**User name:** Enter a name for the ID.</span></span>
    - <span data-ttu-id="5f1a4-142">**Sjálfgefið vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-142">**Default warehouse:** *62*</span></span>
    - <span data-ttu-id="5f1a4-143">**Heiti valmyndar:** *Aðalvalmynd*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-143">**Menu name:** *Main*</span></span>

1. <span data-ttu-id="5f1a4-144">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-144">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="5f1a4-145">Glugginn **Setja aðgangsorð** birtist þar sem hægt er að búa til einfalt aðgangsorð sem notandinn getur notað til að skrá sig inn í forrit fartækis.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-145">The **Set password** dialog box appears, where you can create a simple password that the user can use to sign in to the mobile app.</span></span> <span data-ttu-id="5f1a4-146">Stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-146">Set the following values:</span></span>

    - <span data-ttu-id="5f1a4-147">**Aðgangsorð:** Sláið inn einfalt aðgangsorð.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-147">**Password:** Enter a simple password.</span></span>
    - <span data-ttu-id="5f1a4-148">**Staðfesta aðgangsorð:** Sláið inn sama aðgangsorðið aftur.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-148">**Confirm password:** Enter the same password again.</span></span>

1. <span data-ttu-id="5f1a4-149">Veldu **Stilla aðgangsorð**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-149">Select **Set password**.</span></span>

    <span data-ttu-id="5f1a4-150">Tilkynning í Aðgerðarmiðstöðinni upplýsir þig um að aðgangsorðið hafi verið stillt fyrir notandann sem þú bjóst til.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-150">A notification in the Action Center informs you that the password has been set for the user that you created.</span></span>

### <a name="create-a-location-type"></a><span data-ttu-id="5f1a4-151">Stofna gerð staðsetningar</span><span class="sxs-lookup"><span data-stu-id="5f1a4-151">Create a location type</span></span>

1. <span data-ttu-id="5f1a4-152">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Gerðir staðsetninga**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-152">Go to **Warehouse management \> Setup \> Warehouse \> Location types**.</span></span>
1. <span data-ttu-id="5f1a4-153">Veldu **Nýtt** á aðgerðasvæðinu til að búa til staðsetningargerð og stilltu eftirfarandi gildi fyrir hana:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-153">On the Action Pane, select **New** to create a location type, and set the following values for it:</span></span>

    - <span data-ttu-id="5f1a4-154">**Gerð staðsetningar:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-154">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="5f1a4-155">**Lýsing:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-155">**Description:** *Sort*</span></span>

1. <span data-ttu-id="5f1a4-156">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-156">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-warehouse-management-parameters"></a><span data-ttu-id="5f1a4-157">Setja upp færibreytur vöruhúsakerfis</span><span class="sxs-lookup"><span data-stu-id="5f1a4-157">Set up Warehouse management parameters</span></span>

1. <span data-ttu-id="5f1a4-158">Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-158">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="5f1a4-159">Í flipanum **Almennt** , í flýtiflipanum **Gerðir staðsetninga** , skal stilla reitinn **Flokkun á gerð staðsetningar** á *SORT*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-159">On the **General** tab, on the **Location types** FastTab, set the **Sorting location type** field to *SORT*.</span></span>
1. <span data-ttu-id="5f1a4-160">Í aðgerðarúðunni skal velja **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-160">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-a-location-profile"></a><span data-ttu-id="5f1a4-161">Setja upp staðsetningarforstillingu</span><span class="sxs-lookup"><span data-stu-id="5f1a4-161">Set up a location profile</span></span>

1. <span data-ttu-id="5f1a4-162">Fara í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Forstillingar staðsetningar**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-162">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="5f1a4-163">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-163">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5f1a4-164">Stilla eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-164">In the header, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-165">**Kenni staðsetningarforstillingar:** *Röðun*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-165">**Location profile ID:** *Sorting*</span></span>
    - <span data-ttu-id="5f1a4-166">**Heiti:** *Röðun*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-166">**Name:** *Sorting*</span></span>

1. <span data-ttu-id="5f1a4-167">Stilltu eftirfarandi gildi á flýtiflipanum **Almennt** :</span><span class="sxs-lookup"><span data-stu-id="5f1a4-167">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-168">**Staðsetningarsnið:** *ASRB* (Aisle-Rack-Shelf-Bin)</span><span class="sxs-lookup"><span data-stu-id="5f1a4-168">**Location format:** *ASRB* (Aisle-Rack-Shelf-Bin)</span></span>
    - <span data-ttu-id="5f1a4-169">**Gerð staðsetningar:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-169">**Location type:** *SORT*</span></span>
    - <span data-ttu-id="5f1a4-170">**Nota rakningu númeraplötu:** *Já*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-170">**Use license plate tracking:** *Yes*</span></span>
    - <span data-ttu-id="5f1a4-171">**Heimila blandaðar vörur:** *Já* (Þegar þessi valkostur er settur á *Já* , verður valkosturinn **Heimila blandaðar birgðastöðurunur** sjálfkrafa stilltur á *Já* og er ekki hægt að breyta út af fyrir sig.)</span><span class="sxs-lookup"><span data-stu-id="5f1a4-171">**Allow mixed items:** *Yes* (When you set this option to *Yes* , the **Allow mixed inventory batches** option is automatically set to *Yes* and can't be changed independently.)</span></span>

1. <span data-ttu-id="5f1a4-172">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-172">Select **Save**.</span></span>

### <a name="set-up-a-location"></a><span data-ttu-id="5f1a4-173">Setja upp staðsetningu</span><span class="sxs-lookup"><span data-stu-id="5f1a4-173">Set up a location</span></span>

1. <span data-ttu-id="5f1a4-174">Opnaðu **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Staðsetningar**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-174">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span>
1. <span data-ttu-id="5f1a4-175">Í hausnum skal hreinsa gátreitinn **Mynda vartölur fyrir staðsetningu**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-175">In the header, clear the **Generate check digits for location** check box.</span></span>
1. <span data-ttu-id="5f1a4-176">Veldu **Nýtt** á aðgerðasvæðinu til að búa til staðsetningargerð og stilltu eftirfarandi gildi fyrir hana:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-176">On the Action Pane, select **New** to create a location, and set the following values for it:</span></span>

    - <span data-ttu-id="5f1a4-177">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-177">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="5f1a4-178">**Staðsetning:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-178">**Location:** *SORT*</span></span>
    - <span data-ttu-id="5f1a4-179">**Kenni staðsetningarforstillingar:** *SORTING*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-179">**Location profile ID:** *SORTING*</span></span>

1. <span data-ttu-id="5f1a4-180">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-180">Select **Save**.</span></span>

### <a name="set-up-an-outbound-sorting-template"></a><span data-ttu-id="5f1a4-181">Setja upp flokkunarsniðmát á útleið</span><span class="sxs-lookup"><span data-stu-id="5f1a4-181">Set up an outbound sorting template</span></span>

<span data-ttu-id="5f1a4-182">Flokkunarsniðmát á útleið ákvarðar hvort vinna er stofnuð út frá röðunarstaðsetningu og hvort röðun er gerð handvirkt eða sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-182">The outbound sorting template determines whether work is created out of the sort location, and whether sorting is done manually or automatically.</span></span>

<span data-ttu-id="5f1a4-183">Fyrir þessa atburðarás stofnarðu flokkunarsniðmát á útleið til að búa til bretti eftir pökkunarstöðina.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-183">For this scenario, you will create an outbound sorting template to build pallets after the packing station.</span></span>

1. <span data-ttu-id="5f1a4-184">Farið í **Vöruhúsakerfi \> Uppsetning \> Pökkun \> Flokkunarsniðmát á útleið**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-184">Go to **Warehouse Management \> Setup \> Packing \> Outbound sorting template**.</span></span>
1. <span data-ttu-id="5f1a4-185">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-185">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5f1a4-186">Stilltu eftirfarandi gildi í haus nýja sniðmátsins:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-186">In the header of the new template, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-187">**Kenni fyrir flokkunarsniðmát á útleið:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-187">**Outbound sorting template ID:** *AutoWork*</span></span>
    - <span data-ttu-id="5f1a4-188">**Lýsing:** *Sjálfvirk stofnun vinnu*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-188">**Description:** *Auto Work Creation*</span></span>
    - <span data-ttu-id="5f1a4-189">**Sniðmátsgerð flokkunar á útleið:** *Gámur*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-189">**Outbound sorting template type:** *Container*</span></span>
    - <span data-ttu-id="5f1a4-190">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-190">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="5f1a4-191">**Staðsetning:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-191">**Location:** *SORT*</span></span>

1. <span data-ttu-id="5f1a4-192">Stilltu eftirfarandi gildi á flýtiflipanum **Almennt** :</span><span class="sxs-lookup"><span data-stu-id="5f1a4-192">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-193">**Sannprófun röðunar:** *Skönnun stöðu*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-193">**Sort verification:** *Position scan*</span></span>
    - <span data-ttu-id="5f1a4-194">**Stofna vinnu á lokun stöðu:** *Já*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-194">**Create work on position close:** *Yes*</span></span>

        <span data-ttu-id="5f1a4-195">Ef þessi valkostur er stilltur á *Já* , þegar staðan er lokuð, verður vinna stofnuð til að færa birgðir á lokasendingarstaðinn.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-195">If this option is set to *Yes* , when the position is closed, work will be created to move inventory to the final shipping location.</span></span> <span data-ttu-id="5f1a4-196">Ef hann er stilltur á *Nei* verða birgðir strax tíndar fyrir pöntunina þegar staðan er lokuð.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-196">If it's set to *No* , inventory will immediately be picked to the order when the position is closed.</span></span>

    - <span data-ttu-id="5f1a4-197">**Stöðuverkefni:** *Sjálfvirkt*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-197">**Position assignment:** *Automatic*</span></span>

        <span data-ttu-id="5f1a4-198">Ef þessi reitur er stilltu rá *Handvirkt* verður notandi alltaf að tilgreina hvaða stöðu birgðir eiga að vera flokkaðar í.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-198">If this field is set to *Manual* , the user must always indicate which position the inventory should be sorted to.</span></span> <span data-ttu-id="5f1a4-199">Ef hann er stilltur á *Sjálfvirkt* beinir kerfið birgðum sjálfkrafa að stöðu þegar það er í boði, á grunni sundurliðana sniðmátsflokkunar.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-199">If it's set to *Automatic* , the system will automatically guide the inventory to a position whenever it can, based on the sort template breaks.</span></span>

1. <span data-ttu-id="5f1a4-200">Veldu **Vista** til að bjóða upp á valkostinn **Breyta fyrirspurn** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-200">Select **Save** to make the **Edit query** button on the Action Pane available.</span></span>
1. <span data-ttu-id="5f1a4-201">Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-201">On the Action Pane, select **Edit Query**.</span></span>
1. <span data-ttu-id="5f1a4-202">Í fyrirspurnarritlinum, í flipanum **Röðun** , skal bæta við línu sem er með eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-202">In the query editor, on the **Sorting** tab, add a line that has the following values:</span></span>

    - <span data-ttu-id="5f1a4-203">**Tafla:** *Sendingar*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-203">**Table:** *Shipments*</span></span>
    - <span data-ttu-id="5f1a4-204">**Afleidd tafla:** *Sendingar*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-204">**Derived table:** *Shipments*</span></span>
    - <span data-ttu-id="5f1a4-205">**Reitur:** *Flutningsþjónusta*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-205">**Field:** *Carrier service*</span></span>

        <span data-ttu-id="5f1a4-206">Þegar þetta gildi er valið gætu komið upp eftirfarandi skilaboð: „Reiturinn Flutningsþjónusta er ekki vísisreitur.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-206">When you select this value, you might receive the following message: "Field Carrier service is not an index field.</span></span> <span data-ttu-id="5f1a4-207">Á að bæta við röðun á þetta?“</span><span class="sxs-lookup"><span data-stu-id="5f1a4-207">Do you want to add sorting on this?"</span></span> <span data-ttu-id="5f1a4-208">Velja skal **Já**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-208">Select **Yes**.</span></span>

    - <span data-ttu-id="5f1a4-209">**Leitarstefna:** *Hækkandi*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-209">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="5f1a4-210">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-210">Select **OK**.</span></span>
1. <span data-ttu-id="5f1a4-211">Þú gætir fengið eftirfarandi skilaboð: „Flokkun verður endurstillt, á að halda áfram?"</span><span class="sxs-lookup"><span data-stu-id="5f1a4-211">You might receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="5f1a4-212">Velja skal **Já**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-212">Select **Yes**.</span></span>

    <span data-ttu-id="5f1a4-213">Hnappur **Sundurliðanir flokkunarsniðmáts á útleið** á aðgerðasvæðinu verður tiltækur.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-213">The **Outbound sorting template breaks** button on the Action Pane becomes available.</span></span>

1. <span data-ttu-id="5f1a4-214">Á aðgerðasvæðinu skal velja **Sundurliðanir flokkunarsniðmáts á útleið**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-214">On the Action Pane, select **Outbound sorting template breaks**.</span></span>
1. <span data-ttu-id="5f1a4-215">Í glugganum **Skilyrði fyrir flokkun á útleið** skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-215">In the **Outbound sorting criteria** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-216">**Tilvísunartöflunafn:** *Sendingar*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-216">**Reference table name:** *Shipments*</span></span>
    - <span data-ttu-id="5f1a4-217">**Heiti tilvísunarreits:** *Flutningsþjónusta*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-217">**Reference field name:** *Carrier service*</span></span>
    - <span data-ttu-id="5f1a4-218">**Flokka eftir reit:** Veljið þennan gátreit til að flokka sendingar eftir flutningsþjónustu.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-218">**Group by field:** Select this check box to group shipments by carrier service.</span></span>

1. <span data-ttu-id="5f1a4-219">Veldu **Í lagi** til að vista stillingarnar þínar og loka glugganum.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-219">Select **OK** to save your settings and close the dialog box.</span></span>

### <a name="set-up-container-packing-policies"></a><span data-ttu-id="5f1a4-220">Setja upp pökkunarreglur geymis</span><span class="sxs-lookup"><span data-stu-id="5f1a4-220">Set up container packing policies</span></span>

1. <span data-ttu-id="5f1a4-221">Fara í **Vöruhúsakerfi \> Uppsetning \> Gámar \> Pökkunarreglur gáms**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-221">Go to **Warehouse management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="5f1a4-222">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-222">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5f1a4-223">Stilla eftirfarandi gildi í hausnum á nýju reglunni:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-223">In the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-224">**Pökkunarregla geymis:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-224">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="5f1a4-225">**Lýsing:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-225">**Description:** *Sort*</span></span>

1. <span data-ttu-id="5f1a4-226">Stilltu eftirfarandi gildi á **Yfirlit** flipanum:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-226">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-227">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-227">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="5f1a4-228">**Sjálfgefin staðsetning fyrir flokkun:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-228">**Default location for sorting:** *SORT*</span></span>
    - <span data-ttu-id="5f1a4-229">**Þyngdareining:** *kg*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-229">**Weight unit:** *kg*</span></span>
    - <span data-ttu-id="5f1a4-230">**Lokunarregla geymis:** *Sjálfvirk losun*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-230">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="5f1a4-231">**Losunarregla geymis:** *Úthluta gámi flokkaðri staðsetningu á útleið*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-231">**Container release policy:** *Assign container to outbound sorting position*</span></span>

1. <span data-ttu-id="5f1a4-232">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-232">Select **Save**.</span></span>

### <a name="set-up-packing-profiles"></a><span data-ttu-id="5f1a4-233">Setja upp pökkunarforstillingar</span><span class="sxs-lookup"><span data-stu-id="5f1a4-233">Set up packing profiles</span></span>

<span data-ttu-id="5f1a4-234">Stofnið nýja pökkunarforstillingu sem verður notuð ásamt röðunarvirkninni.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-234">Create a new packing profile that will be used together with the sorting functionality.</span></span>

1. <span data-ttu-id="5f1a4-235">Fara í **Vöruhúsakerfi \> Uppsetning \> Pökkun \> Forstillingar umbúða**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-235">Go to **Warehouse management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="5f1a4-236">Veljið **Nýtt** á aðgerðasvæðinu til að búa til línu og stillið eftirfarandi gildi fyrir hana:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-236">On the Action Pane, select **New** to create a line, and set the following values for it:</span></span>

    - <span data-ttu-id="5f1a4-237">**Forstillingarkenni pökkunar:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-237">**Packing profile ID:** *Sort*</span></span>
    - <span data-ttu-id="5f1a4-238">**Lýsing:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-238">**Description:** *Sort*</span></span>
    - <span data-ttu-id="5f1a4-239">**Pökkunarregla geymis:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-239">**Container packing policy:** *Sort*</span></span>
    - <span data-ttu-id="5f1a4-240">**Auðkennisstilling gáms:** *Sjálfvirkt*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-240">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="5f1a4-241">**Gámagerð:** *Kassi-stór*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-241">**Container type:** *Box-Large*</span></span>
    - <span data-ttu-id="5f1a4-242">**Stofna sjálfvirkt gám þegar gámi er lokað:** Hreinsað (= *Nei* )</span><span class="sxs-lookup"><span data-stu-id="5f1a4-242">**Auto create container at container close:** Cleared (= *No* )</span></span>

1. <span data-ttu-id="5f1a4-243">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-243">Select **Save**.</span></span>

### <a name="set-up-work-classes"></a><span data-ttu-id="5f1a4-244">Setja upp vinnuklasa</span><span class="sxs-lookup"><span data-stu-id="5f1a4-244">Set up work classes</span></span>

<span data-ttu-id="5f1a4-245">Setjið upp vinnuklasa sem notaður verður ásamt röðun.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-245">Set up a work class that will be used together with sorting.</span></span>

1. <span data-ttu-id="5f1a4-246">Fara í **Vöruhúsastjórnun \> Uppsetning \> Vinna \> Vinnuklasar**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-246">Go to **Warehouse management \> Setup \> Work \> Work classes**.</span></span>
1. <span data-ttu-id="5f1a4-247">Veljið **Nýtt** á aðgerðasvæðinu til að búa til vinnuklasa fyrir röðun og stillið eftirfarandi gildi fyrir hann:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-247">On the Action Pane, select **New** to create a work class for sorting, and set the following values for it:</span></span>

    - <span data-ttu-id="5f1a4-248">**Auðkenni vinnuklasa:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-248">**Work class ID:** *Sort*</span></span>
    - <span data-ttu-id="5f1a4-249">**Lýsing:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-249">**Description:** *Sort*</span></span>
    - <span data-ttu-id="5f1a4-250">**Gerð verkbeiðni:** *Röðuð birgðatínsla*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-250">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="5f1a4-251">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-251">Select **Save**.</span></span>

### <a name="set-up-mobile-device-menu-items"></a><span data-ttu-id="5f1a4-252">Setja upp valmyndaratriði fartækis</span><span class="sxs-lookup"><span data-stu-id="5f1a4-252">Set up mobile device menu items</span></span>

#### <a name="set-up-a-new-pallet-menu-item"></a><span data-ttu-id="5f1a4-253">Setja upp nýtt valmyndaratriði brettis</span><span class="sxs-lookup"><span data-stu-id="5f1a4-253">Set up a new pallet menu item</span></span>

<span data-ttu-id="5f1a4-254">Búa til valmyndaratriði fartækis til að búa til bretti við röðun.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-254">Create a mobile device menu item to build pallets during sorting.</span></span>

1. <span data-ttu-id="5f1a4-255">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-255">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="5f1a4-256">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-256">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5f1a4-257">Stilla eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-257">In the header, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-258">**Heiti valmyndaratriðis:** *Röðun á bretti*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-258">**Menu item name:** *Pallet build*</span></span>
    - <span data-ttu-id="5f1a4-259">**Titill:** *Röðun á bretti*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-259">**Title:** *Pallet build*</span></span>
    - <span data-ttu-id="5f1a4-260">**Stilling:** *Óbein*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-260">**Mode:** *Indirect*</span></span>
    - <span data-ttu-id="5f1a4-261">**Nota fyrirliggjandi vinnu:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-261">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="5f1a4-262">Stilltu eftirfarandi gildi á flýtiflipanum **Almennt** :</span><span class="sxs-lookup"><span data-stu-id="5f1a4-262">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-263">**Verkþáttarkóði:** *Röðun á útleið*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-263">**Activity code:** *Outbound sorting*</span></span>

        <span data-ttu-id="5f1a4-264">Þegar þessi reitur er stilltur á *Röðun á útleið* birtist reiturinn **Auðkenni flokkunarsniðmáts á útleið**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-264">When this field is set to *Outbound sorting* , the **Outbound sorting template ID** field is shown.</span></span>

    - <span data-ttu-id="5f1a4-265">**Nota leiðbeiningar fyrir ferli:** *Já*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-265">**Use process guide:** *Yes*</span></span>

        <span data-ttu-id="5f1a4-266">Þegar reiturinn **Verkþáttarkóði** er stilltur á *Röðun á útleið* verður þessi valkostur sjálfkrafa stilltur á *Já*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-266">When the **Activity code** field is set to *Outbound sorting* , this option is automatically set to *Yes*.</span></span>

    - <span data-ttu-id="5f1a4-267">**Kenni fyrir flokkunarsniðmát á útleið:** *AutoWork*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-267">**Outbound sorting template ID:** *AutoWork*</span></span>

1. <span data-ttu-id="5f1a4-268">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-268">Select **Save**.</span></span>

#### <a name="set-up-a-new-loading-menu-item"></a><span data-ttu-id="5f1a4-269">Setja upp nýtt valmyndaratriði hleðslu</span><span class="sxs-lookup"><span data-stu-id="5f1a4-269">Set up a new loading menu item</span></span>

<span data-ttu-id="5f1a4-270">Næst skal búa til valmyndaratriði sem gerir notendum kleift að flytja raðaðar birgðavörur á sendingarstaðinn.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-270">Next, create a menu item that lets users move the sorted inventory items to the shipping location.</span></span>

1. <span data-ttu-id="5f1a4-271">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-271">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="5f1a4-272">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-272">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5f1a4-273">Stilla eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-273">In the header, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-274">**Heiti valmyndaratriðis:** *Hleðsla frá röðun*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-274">**Menu item name:** *Load from Sorting*</span></span>
    - <span data-ttu-id="5f1a4-275">**Titill:** *Hleðsla frá röðun*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-275">**Title:** *Load from Sorting*</span></span>
    - <span data-ttu-id="5f1a4-276">**Máti:** *Vinna*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-276">**Mode:** *Work*</span></span>
    - <span data-ttu-id="5f1a4-277">**Nota fyrirliggjandi vinnu:** *Já*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-277">**Use existing work:** *Yes*</span></span>

1. <span data-ttu-id="5f1a4-278">Í flýtiflipanum **Almennt** skal stilla reitinn **Stjórnað af** á *Stýrt af notanda*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-278">On the **General** FastTab, set the **Directed by** field to *User directed*.</span></span>
1. <span data-ttu-id="5f1a4-279">Í flýtiflipanum **Vinnuklasar** skal velja **Nýr** og síðan stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-279">On the **Work classes** FastTab, select **New** , and then set the following values:</span></span>

    - <span data-ttu-id="5f1a4-280">**Auðkenni vinnuklasa:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-280">**Work class ID:** *SORT*</span></span>
    - <span data-ttu-id="5f1a4-281">**Gerð verkbeiðni:** *Röðuð birgðatínsla*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-281">**Work order type:** *Sorted inventory picking*</span></span>

1. <span data-ttu-id="5f1a4-282">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-282">Select **Save**.</span></span>

### <a name="set-up-the-mobile-device-menu"></a><span data-ttu-id="5f1a4-283">Uppsetning á valmynd fartækis</span><span class="sxs-lookup"><span data-stu-id="5f1a4-283">Set up the mobile device menu</span></span>

<span data-ttu-id="5f1a4-284">Þú verður nú að bæta nýju valmyndaratriðunum við valmynd fartækis.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-284">You must now add the new menu items to the mobile device menu.</span></span>

1. <span data-ttu-id="5f1a4-285">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-285">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="5f1a4-286">Veljið valmyndina **Á útleið**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-286">Select the **Outbound** menu.</span></span>
1. <span data-ttu-id="5f1a4-287">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-287">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="5f1a4-288">Í dálknum **Tiltækar valmyndir og valmyndaratriði** skal finna og velja **Röðun á bretti**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-288">In the **Available menus and menu items** column, find and select **Pallet build**.</span></span>
1. <span data-ttu-id="5f1a4-289">Smellið á hægri örvarhnappinn til að færa **Röðun á bretti** yfir í dálkinn **Valmyndarskipan**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-289">Select the right arrow button to move **Pallet build** to the **Menu structure** column.</span></span>
1. <span data-ttu-id="5f1a4-290">Notið hnappana fyrir upp- og niðurörina til að setja valmyndaratriðið **Röðun á bretti** í æskilega stöðu á valmyndaratriði fartækis.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-290">Use the up arrow and down arrow buttons to put the **Pallet build** menu item in the desired position on the mobile device menu.</span></span>
1. <span data-ttu-id="5f1a4-291">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-291">Select **Save**.</span></span>
1. <span data-ttu-id="5f1a4-292">Endurtakið þetta ferli til að valmyndaratriðinu **Hleðsla frá röðun** við valmyndina **Á útleið**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-292">Repeat this procedure to add the **Load from Sorting** menu item to the **Outbound** menu.</span></span>

### <a name="set-up-location-directives"></a><span data-ttu-id="5f1a4-293">Setja upp staðsetningarleiðbeiningar</span><span class="sxs-lookup"><span data-stu-id="5f1a4-293">Set up location directives</span></span>

<span data-ttu-id="5f1a4-294">*Staðsetningarleiðbeiningar* eru reglur sem hjálpa við auðkenningu tiltektar- og frágangsstaðsetninga fyrir birgðahreyfingar.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-294">*Location directives* are rules that help identify pick and put locations for inventory movement.</span></span> <span data-ttu-id="5f1a4-295">Nú þarf að búa til reglu til að stjórna röðunarvinnunni.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-295">You must now create a rule to manage the sorting work.</span></span>

#### <a name="set-up-a-single-sku-directive"></a><span data-ttu-id="5f1a4-296">Setja upp leiðbeiningu fyrir eina birgðahaldseiningu</span><span class="sxs-lookup"><span data-stu-id="5f1a4-296">Set up a single-SKU directive</span></span>

1. <span data-ttu-id="5f1a4-297">Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-297">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="5f1a4-298">Á vinstra svæðinu skal breyta gildinu á reitnum **Gerð verkbeiðni** í *Röðuð birgðatínsla*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-298">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="5f1a4-299">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-299">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5f1a4-300">Stilla eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-300">In the header, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-301">**Röð:** *1*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-301">**Sequence:** *1*</span></span>
    - <span data-ttu-id="5f1a4-302">**Heiti:** *Útskot*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-302">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="5f1a4-303">Stilltu eftirfarandi gildi á flýtiflipanum **staðsetningarleiðbeiningar** :</span><span class="sxs-lookup"><span data-stu-id="5f1a4-303">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-304">**Tegund vinnu:** *Frágangur*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-304">**Work type:** *Put*</span></span>
    - <span data-ttu-id="5f1a4-305">**Svæði:** *6*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-305">**Site:** *6*</span></span>
    - <span data-ttu-id="5f1a4-306">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-306">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="5f1a4-307">**Margar birgðahaldseiningar:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-307">**Multiple SKU:** *No*</span></span>

1. <span data-ttu-id="5f1a4-308">Veldu **Vista** til að gera tækjastikuna á flýtiflipanum **Línur** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-308">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="5f1a4-309">Á flipanum **Línur** veldu **Nýtt** og stilltu síðan eftirfarandi gildi á nýju línunni.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-309">On the **Lines** FastTab, select **New** , and then set the following values on the new line.</span></span> <span data-ttu-id="5f1a4-310">Samþykktu sjálfgildin fyrir öll önnur svæði.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-310">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="5f1a4-311">**Röð:** *1*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-311">**Sequence:** *1*</span></span>
    - <span data-ttu-id="5f1a4-312">**Frá:** *0*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-312">**From:** *0*</span></span>
    - <span data-ttu-id="5f1a4-313">**Til:** *1.000.000*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-313">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="5f1a4-314">Veldu **Vista** til að gera tækjastikuna á flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-314">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="5f1a4-315">Í flipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Ný** og stilla síðan eftirfarandi gildi í nýju línunni.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-315">On the **Location Directive Actions** FastTab, select **New** , and then set the following values on the new line.</span></span> <span data-ttu-id="5f1a4-316">Samþykktu sjálfgildin fyrir öll önnur svæði.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-316">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="5f1a4-317">**Röð:** *1*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-317">**Sequence:** *1*</span></span>
    - <span data-ttu-id="5f1a4-318">**Heiti:** *Útskot*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-318">**Name:** *Baydoor*</span></span>

1. <span data-ttu-id="5f1a4-319">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-319">Select **Save**.</span></span>
1. <span data-ttu-id="5f1a4-320">Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-320">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="5f1a4-321">Í fyrirspurnarritlinum, í flipanum **Svið** , skal finna línuna þar sem reiturinn **Svæði** er stilltur á *Staðsetning*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-321">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="5f1a4-322">Stillið reitinn **Skilyrði** fyrir þessa línu á *Útskot*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-322">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="5f1a4-323">Veldu **Í lagi** til að vista stillingarnar þínar og loka fyrirspurnarritilinum.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-323">Select **OK** to save your settings and close the query editor.</span></span>

#### <a name="set-up-a-multiple-sku-directive"></a><span data-ttu-id="5f1a4-324">Setja upp leiðbeiningu fyrir margar birgðahaldseiningar</span><span class="sxs-lookup"><span data-stu-id="5f1a4-324">Set up a multiple-SKU directive</span></span>

1. <span data-ttu-id="5f1a4-325">Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-325">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="5f1a4-326">Á vinstra svæðinu skal breyta gildinu á reitnum **Gerð verkbeiðni** í *Röðuð birgðatínsla*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-326">In the left pane, change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="5f1a4-327">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-327">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5f1a4-328">Stilla eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-328">In the header, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-329">**Röð:** *2*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-329">**Sequence:** *2*</span></span>
    - <span data-ttu-id="5f1a4-330">**Heiti:** *Mörg útskot*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-330">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="5f1a4-331">Stilltu eftirfarandi gildi á flýtiflipanum **staðsetningarleiðbeiningar** :</span><span class="sxs-lookup"><span data-stu-id="5f1a4-331">On the **Location directives** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-332">**Tegund vinnu:** *Frágangur*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-332">**Work type:** *Put*</span></span>
    - <span data-ttu-id="5f1a4-333">**Svæði:** *6*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-333">**Site:** *6*</span></span>
    - <span data-ttu-id="5f1a4-334">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-334">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="5f1a4-335">**Margar birgðahaldseiningar:** *Já*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-335">**Multiple SKU:** *Yes*</span></span>

1. <span data-ttu-id="5f1a4-336">Veldu **Vista** til að gera tækjastikuna á flýtiflipanum **Línur** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-336">Select **Save** to make the toolbar on the **Lines** FastTab available.</span></span>
1. <span data-ttu-id="5f1a4-337">Á flipanum **Línur** veldu **Nýtt** og stilltu síðan eftirfarandi gildi á nýju línunni.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-337">On the **Lines** FastTab, select **New** , and then set the following values on the new line.</span></span> <span data-ttu-id="5f1a4-338">Samþykktu sjálfgildin fyrir öll önnur svæði.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-338">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="5f1a4-339">**Röð:** *1*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-339">**Sequence:** *1*</span></span>
    - <span data-ttu-id="5f1a4-340">**Frá:** *0*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-340">**From:** *0*</span></span>
    - <span data-ttu-id="5f1a4-341">**Til:** *1.000.000*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-341">**To:** *1,000,000*</span></span>

1. <span data-ttu-id="5f1a4-342">Veldu **Vista** til að gera tækjastikuna á flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-342">Select **Save** to make the toolbar on the **Location Directive Actions** FastTab available.</span></span>
1. <span data-ttu-id="5f1a4-343">Í flipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Ný** og stilla síðan eftirfarandi gildi í nýju línunni.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-343">On the **Location Directive Actions** FastTab, select **New** , and then set the following values on the new line.</span></span> <span data-ttu-id="5f1a4-344">Samþykktu sjálfgildin fyrir öll önnur svæði.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-344">Accept the default values for all the other fields.</span></span>

    - <span data-ttu-id="5f1a4-345">**Röð:** *1*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-345">**Sequence:** *1*</span></span>
    - <span data-ttu-id="5f1a4-346">**Heiti:** *Mörg útskot*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-346">**Name:** *Baydoor Multi*</span></span>

1. <span data-ttu-id="5f1a4-347">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-347">Select **Save**.</span></span>
1. <span data-ttu-id="5f1a4-348">Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Breyta fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-348">On the **Location Directive Actions** FastTab, select **Edit query**.</span></span>
1. <span data-ttu-id="5f1a4-349">Í fyrirspurnarritlinum, í flipanum **Svið** , skal finna línuna þar sem reiturinn **Svæði** er stilltur á *Staðsetning*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-349">In the query editor, on the **Range** tab, find the row where the **Field** field is set to *Location*.</span></span> <span data-ttu-id="5f1a4-350">Stillið reitinn **Skilyrði** fyrir þessa línu á *Útskot*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-350">Set the **Criteria** field for this row to *Baydoor*.</span></span>
1. <span data-ttu-id="5f1a4-351">Veldu **Í lagi** til að vista stillingarnar þínar og loka fyrirspurnarritilinum.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-351">Select **OK** to save your settings and close the query editor.</span></span>

### <a name="set-up-work-templates"></a><span data-ttu-id="5f1a4-352">Setja upp vinnusniðmát</span><span class="sxs-lookup"><span data-stu-id="5f1a4-352">Set up work templates</span></span>

1. <span data-ttu-id="5f1a4-353">Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-353">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="5f1a4-354">Breytið gildinu í reitnum **Gerð verkbeiðni** í *Röðuð birgðatínsla*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-354">Change the value of the **Work order type** field to *Sorted inventory picking*.</span></span>
1. <span data-ttu-id="5f1a4-355">Veldu **Nýtt** á aðgerðasvæðinu til að búa til vinnusnið.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-355">On the Action Pane, select **New** to create a work template.</span></span>
1. <span data-ttu-id="5f1a4-356">Í flipanum **Yfirlit** skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-356">On the **Overview** tab, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-357">**Röð:** *1*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-357">**Sequence:** *1*</span></span>
    - <span data-ttu-id="5f1a4-358">**Vinnusniðmát:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-358">**Work template:** *Sort*</span></span>
    - <span data-ttu-id="5f1a4-359">**Lýsing á vinnusniðmáti:** *Flokka*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-359">**Work template description:** *Sort*</span></span>

1. <span data-ttu-id="5f1a4-360">Veldu **Vista** til að gera flýtiflipann **Upplýsingar um vinnusniðmát** tiltækan.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-360">Select **Save** to make the **Work Template Details** FastTab available.</span></span>
1. <span data-ttu-id="5f1a4-361">Á flýtiflipanum **Upplýsingar um vinnusniðmát** velur þú **Ný** til að bæta við línu og stillir svo eftirfarandi gildi fyrir hana:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-361">On the **Work Template Details** FastTab, select **New** to add a line, and then set the following values for it:</span></span>

    - <span data-ttu-id="5f1a4-362">**Verkgerð:** *Tiltekt*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-362">**Work type:** *Pick*</span></span>
    - <span data-ttu-id="5f1a4-363">**Auðkenni vinnuklasa:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-363">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="5f1a4-364">Veldu **Nýtt** til að bæta við annarri línu og stilltu eftirfarandi gildi fyrir hana:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-364">Select **New** again to add a second line, and then set the following values for it:</span></span>

    - <span data-ttu-id="5f1a4-365">**Tegund vinnu:** *Frágangur*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-365">**Work type:** *Put*</span></span>
    - <span data-ttu-id="5f1a4-366">**Auðkenni vinnuklasa:** *SORT*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-366">**Work class ID:** *SORT*</span></span>

1. <span data-ttu-id="5f1a4-367">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-367">Select **Save**.</span></span>

## <a name="scenario"></a><span data-ttu-id="5f1a4-368">Aðstæður</span><span class="sxs-lookup"><span data-stu-id="5f1a4-368">Scenario</span></span>

<span data-ttu-id="5f1a4-369">Þessi atburðarás líkir eftir aðstæðum þar sem raða ætti pökkuðum gámum sjálfkrafa á mismunandi staði (bretti) á eftir pökkunarstöðinni, samkvæmt því hver flutningsþjónustan er.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-369">This scenario simulates a situation where packed containers should automatically be sorted to different positions (pallets) after the packing station, depending on the shipping carrier service.</span></span> <span data-ttu-id="5f1a4-370">Þegar öllum vörum hleðslunnar hefur verið pakkað og raðað eftir heimilisfangi, verða brettin færð yfir í útskotið.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-370">After all items from the load are packed and sorted by address, the pallets will be moved to the bay door.</span></span>

### <a name="create-sales-orders-and-picking-work"></a><span data-ttu-id="5f1a4-371">Búa til sölupöntun og tiltekt</span><span class="sxs-lookup"><span data-stu-id="5f1a4-371">Create sales orders and picking work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="5f1a4-372">Stofna sölupöntun 1</span><span class="sxs-lookup"><span data-stu-id="5f1a4-372">Create sales order 1</span></span>

1. <span data-ttu-id="5f1a4-373">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-373">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="5f1a4-374">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-374">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5f1a4-375">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun** :</span><span class="sxs-lookup"><span data-stu-id="5f1a4-375">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-376">**Viðskiptavinalykill:** *US-005*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-376">**Customer account:** *US-005*</span></span>
    - <span data-ttu-id="5f1a4-377">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-377">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="5f1a4-378">Veldu **Í lagi** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-378">Select **OK** to close the dialog box.</span></span>

    <span data-ttu-id="5f1a4-379">Ný sölupöntun opnast.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-379">The new sales order is opened.</span></span>

1. <span data-ttu-id="5f1a4-380">Skiptið yfir í **Hausa** yfirlitið.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-380">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="5f1a4-381">Í flýtiflipanum **Afhending** , í hlutanum **Flutningur** , skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-381">On the **Delivery** FastTab, in the **Transportation** section, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-382">**Farmflytjandi:** *Flugfarmur*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-382">**Shipping carrier:** *Air cargo*</span></span>
    - <span data-ttu-id="5f1a4-383">**Flutningsþjónusta:** *flug*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-383">**Carrier service:** *Air*</span></span>

1. <span data-ttu-id="5f1a4-384">Skiptið yfir í yfirlitið **Línur**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-384">Switch to the **Lines** view.</span></span>
1. <span data-ttu-id="5f1a4-385">Ef nýrri, tómri línu er ekki sjálfkrafa bætt við hnitanetið í flýtiflipanum **Sölupöntunarlínur** , skal velja **Bæta við línu** til að bæta einni við.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-385">If a new, empty line isn't automatically added to the grid on the **Sales order lines** FastTab, select **Add line** to add one.</span></span>
1. <span data-ttu-id="5f1a4-386">Stilltu eftirfarandi gildi á nýju pöntunarlínunni.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-386">On the new order line, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-387">**Vörunúmer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-387">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="5f1a4-388">**Magn:** *2*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-388">**Quantity:** *2*</span></span>

1. <span data-ttu-id="5f1a4-389">Með nýju pöntunarlínuna enn valda í flýtiflipanum **Sölupöntunarlínur** , í valmyndinni **Birgðir** fyrir ofan hnitanetið, skal velja **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-389">While the new order line is still selected on the **Sales order lines** FastTab, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="5f1a4-390">Í síðunni **Frátekning** skal velja **Frátektarlota** til að taka frá fullt magn af völdum línum í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-390">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="5f1a4-391">Lokið síðunni **Frátekning** til að fara aftur í sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-391">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="5f1a4-392">Á aðgerðarrúðunni, á flipanum **Vöruhús** , í hópnum **Aðgerðir** , velurðu **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-392">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="5f1a4-393">Þú færð upplýsingaboð sem sýna sendinguna og bylgjuna fyrir þessa pöntun.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-393">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="5f1a4-394">Skráið niður bylgjuauðkenni og sendingarnúmer.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-394">Make a note of the wave ID and shipment ID numbers.</span></span>

#### <a name="sales-order-2"></a><span data-ttu-id="5f1a4-395">Sölupöntun 2</span><span class="sxs-lookup"><span data-stu-id="5f1a4-395">Sales order 2</span></span>

1. <span data-ttu-id="5f1a4-396">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-396">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="5f1a4-397">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-397">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="5f1a4-398">Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun** :</span><span class="sxs-lookup"><span data-stu-id="5f1a4-398">In the **Create sales order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-399">**Viðskiptavinalykill:** *US-006*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-399">**Customer account:** *US-006*</span></span>
    - <span data-ttu-id="5f1a4-400">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-400">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="5f1a4-401">Veldu **Í lagi** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-401">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="5f1a4-402">Ný sölupöntun opnast.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-402">The new sales order is opened.</span></span> <span data-ttu-id="5f1a4-403">Hún ætti að innihalda nýja, auða línu í hnitanetinu í flýtiflipanum **Sölupöntunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-403">It should include a new, empty line in the grid on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="5f1a4-404">Í þessari pöntunarlínu skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-404">Set the following values on this order line:</span></span>

    - <span data-ttu-id="5f1a4-405">**Vara:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-405">**Item:** *A0001*</span></span>
    - <span data-ttu-id="5f1a4-406">**Magn:** *1*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-406">**Quantity:** *1*</span></span>

1. <span data-ttu-id="5f1a4-407">Í flýtiflipanum **Upplýsingar um línu** , í flipanum **Afhending** , skal stilla reitinn **Flutningsmáti** á *Flowe-STD*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-407">On the **Line details** FastTab, on the **Delivery** tab, set the **Mode of delivery** field to *Flowe-STD*.</span></span>
1. <span data-ttu-id="5f1a4-408">Í flýtiflipanum **Sölupöntunarlínur** skal velja **Bæta við línu** og síðan stilla eftirfarandi gildi í næstu pöntunarlínu:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-408">On the **Sales order lines** FastTab, select **Add line** , and then set the following values on the second order line:</span></span>

    - <span data-ttu-id="5f1a4-409">**Vara:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-409">**Item:** *A0002*</span></span>
    - <span data-ttu-id="5f1a4-410">**Magn:** *1*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-410">**Quantity:** *1*</span></span>

1. <span data-ttu-id="5f1a4-411">Í flýtiflipanum **Upplýsingar um línu** , í flipanum **Afhending** , skal breyta gildinu í reitnum **Flutningsmáti** í *Air C-Air*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-411">On the **Line details** FastTab, on the **Delivery** tab, change the value of the **Mode of delivery** field to *Air C-Air*.</span></span>
1. <span data-ttu-id="5f1a4-412">Á flýtiflipanum **Sölupöntunarlínur** skal velja fyrstu pöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-412">On the **Sales order lines** FastTab, select the first order line.</span></span> <span data-ttu-id="5f1a4-413">Á valmyndinni **Birgðir** fyrir ofan hnitanetið velur þú svo **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-413">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="5f1a4-414">Í síðunni **Frátekning** skal velja **Frátektarlota** til að taka frá fullt magn af völdum línum í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-414">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="5f1a4-415">Lokið síðunni **Frátekning** til að fara aftur í sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-415">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="5f1a4-416">Á flýtiflipanum **Sölupöntunarlínur** skal velja aðra pöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-416">On the **Sales order lines** FastTab, select the second order line.</span></span> <span data-ttu-id="5f1a4-417">Á valmyndinni **Birgðir** fyrir ofan hnitanetið velur þú svo **Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-417">Then, on the **Inventory** menu above the grid, select **Reservation**.</span></span>
1. <span data-ttu-id="5f1a4-418">Í síðunni **Frátekning** skal velja **Frátektarlota** til að taka frá fullt magn af völdum línum í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-418">On the **Reservation** page, select **Reserve lot** to reserve the full quantity of the selected line in the warehouse.</span></span>
1. <span data-ttu-id="5f1a4-419">Lokið síðunni **Frátekning** til að fara aftur í sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-419">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="5f1a4-420">Á aðgerðarrúðunni, á flipanum **Vöruhús** , í hópnum **Aðgerðir** , velurðu **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-420">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="5f1a4-421">Þú færð upplýsingaboð sem sýna sendinguna og bylgjuna fyrir þessa pöntun.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-421">You receive an informational message that shows the shipment and wave for this order.</span></span> <span data-ttu-id="5f1a4-422">Takið eftir því að tvö auðkennisnúmer bylgju og tvö auðkennisnúmer sendingar hafa verið búin til, eitt fyrir hvorn flutningsmáta sölupöntunarlínanna.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-422">Notice that two wave ID numbers and two shipment ID numbers have been created, one for each mode of delivery for the sales order lines.</span></span>

#### <a name="get-the-work-ids-from-the-work-details"></a><span data-ttu-id="5f1a4-423">Ná í vinnukenni úr upplýsingum um vinnu</span><span class="sxs-lookup"><span data-stu-id="5f1a4-423">Get the work IDs from the work details</span></span>

1. <span data-ttu-id="5f1a4-424">Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnu**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-424">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="5f1a4-425">Síðan sýnir vinnukenni sem hafa verið búin til úr sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-425">The page shows the work IDs that have been created from sales orders.</span></span> <span data-ttu-id="5f1a4-426">Notið bylgjukennin og sendingarkennin úr stofnuðum sölupöntunum til að finna vinnukenni hvorrar bylgju og sendingar.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-426">Use the wave IDs and shipment IDs from the sales orders that you created to find the work ID for each wave and shipment.</span></span> <span data-ttu-id="5f1a4-427">Punktið hjá ykkur þessi vinnukenni því að nota þarf þau í næsta skrefi.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-427">Make a note of those work IDs, because you will need them in the next steps.</span></span> <span data-ttu-id="5f1a4-428">Takið eftir því að tvö vinnukenni voru búin til fyrir seinni sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-428">Notice that two work IDs were created for the second sales order.</span></span> <span data-ttu-id="5f1a4-429">Ef mismunandi vörur eru tíndar úr mismunandi staðsetningum, verða búin til aðskilin vinnukenni.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-429">If different items are picked from different locations, separate word IDs are generated.</span></span>

### <a name="pick-items-for-the-sales-orders"></a><span data-ttu-id="5f1a4-430">Tína atriði í sölupantanir</span><span class="sxs-lookup"><span data-stu-id="5f1a4-430">Pick items for the sales orders</span></span>

<span data-ttu-id="5f1a4-431">Ljúkið stofnaðri vinnu með því að nota fartækið til að færa vörurnar yfir í pökkunarstöðina.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-431">Complete the created work by using the mobile device to move the items to the pack station.</span></span>

1. <span data-ttu-id="5f1a4-432">Í fartækinu skal skrá sig inn í vöruhús *62* með því að nota notandakennið sem var stofnað fyrir þessa atburðarás (eða notandakennið fyrir notanda fyrirliggjandi sýnigagna).</span><span class="sxs-lookup"><span data-stu-id="5f1a4-432">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="5f1a4-433">Í aðalvalmyndinni skal velja **Á útleið**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-433">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="5f1a4-434">Í valmyndinni **Á útleið** skal velja **Sölutiltekt**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-434">On the **Outbound** menu, select **Sales Picking**.</span></span>
1. <span data-ttu-id="5f1a4-435">Í reitinn **Auðkenni** skal slá inn vinnukennið sem búið var til fyrir sölupöntun 1.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-435">In the **ID** field, enter the work ID that was created for sales order 1.</span></span>
1. <span data-ttu-id="5f1a4-436">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-436">Select **OK**.</span></span>
1. <span data-ttu-id="5f1a4-437">Á síðuna **Sölupantanir: Tiltekt** skal slá inn marknúmeraplötu sem var búin til fyrir sölupöntun 1.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-437">On the **Sales orders - Pick** page, enter a target LP that was created for sales order 1.</span></span> <span data-ttu-id="5f1a4-438">Takið eftir því að tiltektarstaðsetningin ( *bulk-001* ), vara ( *A0001* ) og magn ( *2 stk* ) eru sýnd.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-438">Notice that the picking location ( *bulk-001* ), item ( *A0001* ), and quantity ( *2 pcs* ) are shown.</span></span>
1. <span data-ttu-id="5f1a4-439">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-439">Select **OK**.</span></span>
1. <span data-ttu-id="5f1a4-440">Skoðið upplýsingarnar á síðunni **Sölupantanir: Frágangur**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-440">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="5f1a4-441">Reiturinn **Loc** á að sýna að tíndar vörur eru að fara á staðsetninguna *Pakka*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-441">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="5f1a4-442">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-442">Select **OK**.</span></span>

    <span data-ttu-id="5f1a4-443">Á síðunni **Skanna vinnukenni / kenni númeraplötu** birtast skilaboðin „Vinnu lokið“, sem gefur til kynna að vinnukennið fyrir sölupöntun 1 sé lokið.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-443">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message, which indicates that the work ID from sales order 1 has been completed.</span></span>

    <span data-ttu-id="5f1a4-444">Þú velur nú sölupöntun 2.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-444">You will now pick sales order 2.</span></span>

1. <span data-ttu-id="5f1a4-445">Í reitinn **Auðkenni** skal slá inn vinnukennið sem búið var til fyrir sölupöntun 2, þar sem lína 1 er með vöru *A0001*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-445">In the **ID** field, enter the work ID that was created for sales order 2, where line 1 has item *A0001*.</span></span>
1. <span data-ttu-id="5f1a4-446">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-446">Select **OK**.</span></span>
1. <span data-ttu-id="5f1a4-447">Á síðuna **Sölupantanir: Tiltekt** skal slá inn marknúmeraplötu.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-447">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="5f1a4-448">Takið eftir því að tiltektarstaðsetningin ( *bulk-001* ), vara ( *A0001* ) og magn ( *1 stk* ) eru sýnd.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-448">Notice that the picking location ( *bulk-001* ), item ( *A0001* ), and quantity ( *1 pcs* ) are shown.</span></span>
1. <span data-ttu-id="5f1a4-449">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-449">Select **OK**.</span></span>
1. <span data-ttu-id="5f1a4-450">Skoðið upplýsingarnar á síðunni **Sölupantanir: Frágangur**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-450">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="5f1a4-451">Reiturinn **Loc** á að sýna að tíndar vörur eru að fara á staðsetninguna *Pakka*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-451">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="5f1a4-452">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-452">Select **OK**.</span></span>

    <span data-ttu-id="5f1a4-453">Á síðunni **Skanna vinnukenni / kenni númeraplötu** birtast skilaboðin „Vinnu lokið“.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-453">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="5f1a4-454">Þessi skilaboð gefa til kynna að vinnukennið úr línu 1 fyrir sölupöntun 2 sé lokið.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-454">This message indicates that the work ID from line 1 of sales order 2 has been completed.</span></span>

1. <span data-ttu-id="5f1a4-455">Í reitinn **Auðkenni** skal slá inn vinnukennið sem búið var til fyrir sölupöntun 2, þar sem lína 2 er með vöru *A0002*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-455">In the **ID** field, enter the work ID that was created for sales order 2, where line 2 has item *A0002*.</span></span>
1. <span data-ttu-id="5f1a4-456">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-456">Select **OK**.</span></span>
1. <span data-ttu-id="5f1a4-457">Á síðuna **Sölupantanir: Tiltekt** skal slá inn marknúmeraplötu.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-457">On the **Sales orders - Pick** page, enter a target LP.</span></span> <span data-ttu-id="5f1a4-458">Takið eftir því að tiltektarstaðsetningin ( *bulk-002* ), vara ( *A0001* ) og magn ( *1 stk* ) eru sýnd.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-458">Notice that the picking location ( *bulk-002* ), item ( *A0001* ), and quantity ( *1 pcs* ) are shown.</span></span>
1. <span data-ttu-id="5f1a4-459">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-459">Select **OK**.</span></span>
1. <span data-ttu-id="5f1a4-460">Skoðið upplýsingarnar á síðunni **Sölupantanir: Frágangur**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-460">Review the information on the **Sales orders - Put** page.</span></span> <span data-ttu-id="5f1a4-461">Reiturinn **Loc** á að sýna að tíndar vörur eru að fara á staðsetninguna *Pakka*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-461">The **Loc** field should indicate that the picked items are going to the *Pack* location.</span></span>
1. <span data-ttu-id="5f1a4-462">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-462">Select **OK**.</span></span>

    <span data-ttu-id="5f1a4-463">Á síðunni **Skanna vinnukenni / kenni númeraplötu** birtast skilaboðin „Vinnu lokið“.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-463">On the **Scan a work ID / license plate ID** page, you receive a "Work Completed" message.</span></span> <span data-ttu-id="5f1a4-464">Þessi skilaboð gefa til kynna að vinnukennið úr línu 2 fyrir sölupöntun 2 sé lokið.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-464">This message indicates that the work ID from line 2 of sales order 2 has been completed.</span></span>

### <a name="pack-sales-orders-into-containers"></a><span data-ttu-id="5f1a4-465">Pakka sölupöntunum í gáma</span><span class="sxs-lookup"><span data-stu-id="5f1a4-465">Pack sales orders into containers</span></span>

#### <a name="pack-sales-order-1-into-containers"></a><span data-ttu-id="5f1a4-466">Pakka sölupöntun 1 í gáma</span><span class="sxs-lookup"><span data-stu-id="5f1a4-466">Pack sales order 1 into containers</span></span>

1. <span data-ttu-id="5f1a4-467">Fara skal í **Vöruhúsakerfi \> Pökkun og gámun \> Pakka**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-467">Go to **Warehouse management \> Packing and containerization \> Pack**.</span></span>

    <span data-ttu-id="5f1a4-468">Svarglugginn **Velja pökkunarstöð** birtist.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-468">The **Select packing station** dialog box appears.</span></span> <span data-ttu-id="5f1a4-469">Sjálfgefið er að reiturinn **Starfskraftur** verði stilltur á heiti starfskrafts sem var settur upp hér áður.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-469">By default, the **Worker** field should be set to the name of the worker that you set up earlier.</span></span>

1. <span data-ttu-id="5f1a4-470">Stilltu eftirfarandi gildi til að skoða og vinna við sendingar og gáma sem eru fyrirhugaðar á tilteknum pökkunarstað:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-470">Set the following values to view and work on shipments and containers that are planned at the specific packing location:</span></span>

    - <span data-ttu-id="5f1a4-471">**Svæði:** *6*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-471">**Site:** *6*</span></span>
    - <span data-ttu-id="5f1a4-472">**Vöruhús:** *62*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-472">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="5f1a4-473">**Staðsetning:** *Pakka*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-473">**Location:** *Pack*</span></span>
    - <span data-ttu-id="5f1a4-474">**Forstillingarkenni pökkunar:** *Raða*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-474">**Packing profile ID:** *Sort*</span></span>

1. <span data-ttu-id="5f1a4-475">Veldu **Í lagi** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-475">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="5f1a4-476">Á síðuna **Pakka** , í reitinn **Númeraplata eða sending** , skal slá inn marknúmeraplötuna fyrir sölupöntun 1.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-476">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for sales order 1.</span></span> <span data-ttu-id="5f1a4-477">Ýtið síðan á **Tab** eða **Enter** á lyklaborðinu til að fara úr reitnum.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-477">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="5f1a4-478">Á aðgerðasvæðinu skal velja **Nýr gámur**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-478">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="5f1a4-479">Samþykkið allar sjálfgefnar stillingar og veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-479">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="5f1a4-480">Punktið niður gámakennið.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-480">Make a note of the container ID.</span></span>
1. <span data-ttu-id="5f1a4-481">Í flýtiflipanum **Vörupökkun** skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-481">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-482">**Magn:** *1*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-482">**Quantity:** *1*</span></span>
    - <span data-ttu-id="5f1a4-483">**Kennimerki:** Atriði *A0001*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-483">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="5f1a4-484">Á aðgerðasvæðinu skal velja **Loka gámi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-484">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="5f1a4-485">Í svarglugganum **Loka gámi** skal velja **Fá þyngd kerfis** til að fá kerfið til að uppfæra reitinn **Brúttóþyngd**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-485">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="5f1a4-486">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-486">Select **OK**.</span></span> <span data-ttu-id="5f1a4-487">Gámurinn er fluttur á staðsetninguna *SORT* og er tilbúinn til röðunar.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-487">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="5f1a4-488">Búðu til annan gám til að bæta öðrum hlut frá númeraplötu fyrir sölupöntun 1 í nýjan gám.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-488">Create a second container to add the second item from the LP for sales order 1 to a new container.</span></span>
1. <span data-ttu-id="5f1a4-489">Á aðgerðasvæðinu skal velja **Nýr gámur**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-489">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="5f1a4-490">Samþykkið allar sjálfgefnar stillingar og veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-490">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="5f1a4-491">Punktið niður gámakennið.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-491">Make a note of the container ID.</span></span>
1. <span data-ttu-id="5f1a4-492">Í flýtiflipanum **Vörupökkun** skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-492">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-493">**Magn:** *1*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-493">**Quantity:** *1*</span></span>
    - <span data-ttu-id="5f1a4-494">**Kennimerki:** Atriði *A0001*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-494">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="5f1a4-495">Á aðgerðasvæðinu skal velja **Loka gámi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-495">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="5f1a4-496">Í svarglugganum **Loka gámi** skal velja **Fá þyngd kerfis** til að fá kerfið til að uppfæra reitinn **Brúttóþyngd**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-496">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="5f1a4-497">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-497">Select **OK**.</span></span> <span data-ttu-id="5f1a4-498">Gámurinn er fluttur á staðsetninguna *SORT* og er tilbúinn til röðunar.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-498">The container is moved to the *SORT* location and is ready for sorting.</span></span>

#### <a name="pack-sales-order-2-into-containers"></a><span data-ttu-id="5f1a4-499">Pakka sölupöntun 2 í gáma</span><span class="sxs-lookup"><span data-stu-id="5f1a4-499">Pack sales order 2 into containers</span></span>

1. <span data-ttu-id="5f1a4-500">Á síðuna **Pakka** , í reitinn **Númeraplata eða sending** , skal slá inn marknúmeraplötuna fyrir línu 1 í sölupöntun 2.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-500">On the **Pack** page, in the **License plate or shipment** field, enter the target LP for line 1 of sales order 2.</span></span> <span data-ttu-id="5f1a4-501">Ýtið síðan á **Tab** eða **Enter** á lyklaborðinu til að fara úr reitnum.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-501">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="5f1a4-502">Á aðgerðasvæðinu skal velja **Nýr gámur**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-502">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="5f1a4-503">Samþykkið allar sjálfgefnar stillingar og veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-503">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="5f1a4-504">Punktið niður gámakennið.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-504">Make a note of the container ID.</span></span>
1. <span data-ttu-id="5f1a4-505">Í flýtiflipanum **Vörupökkun** skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-505">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-506">**Magn:** *1*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-506">**Quantity:** *1*</span></span>
    - <span data-ttu-id="5f1a4-507">**Kennimerki:** Atriði *A0001*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-507">**Identifier:** Item *A0001*</span></span>

1. <span data-ttu-id="5f1a4-508">Á aðgerðasvæðinu skal velja **Loka gámi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-508">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="5f1a4-509">Í svarglugganum **Loka gámi** skal velja **Fá þyngd kerfis** til að fá kerfið til að uppfæra reitinn **Brúttóþyngd**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-509">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="5f1a4-510">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-510">Select **OK**.</span></span> <span data-ttu-id="5f1a4-511">Gámurinn er fluttur á staðsetninguna *SORT* og er tilbúinn til röðunar.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-511">The container is moved to the *SORT* location and is ready for sorting.</span></span>
1. <span data-ttu-id="5f1a4-512">Í reitinn **Númeraplata eða sending** skal slá inn marknúmeraplötuna fyrir línu 2 í sölupöntun 2.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-512">In the **License plate or shipment** field, enter the target LP for line 2 of the sales order 2.</span></span> <span data-ttu-id="5f1a4-513">Ýtið síðan á **Tab** eða **Enter** á lyklaborðinu til að fara úr reitnum.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-513">Then select the **Tab** or **Enter** key on your keyboard to move out of the field.</span></span>
1. <span data-ttu-id="5f1a4-514">Á aðgerðasvæðinu skal velja **Nýr gámur**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-514">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="5f1a4-515">Samþykkið allar sjálfgefnar stillingar og veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-515">Accept all the default settings, and select **OK**.</span></span> <span data-ttu-id="5f1a4-516">Punktið niður gámakennið.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-516">Make a note of the container ID.</span></span>
1. <span data-ttu-id="5f1a4-517">Í flýtiflipanum **Vörupökkun** skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="5f1a4-517">On the **Item packing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="5f1a4-518">**Magn:** *1*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-518">**Quantity:** *1*</span></span>
    - <span data-ttu-id="5f1a4-519">**Auðkennireitur:** Atriði *A0002*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-519">**Identifier field:** Item *A0002*</span></span>

1. <span data-ttu-id="5f1a4-520">Á aðgerðasvæðinu skal velja **Loka gámi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-520">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="5f1a4-521">Í svarglugganum **Loka gámi** skal velja **Fá þyngd kerfis** til að fá kerfið til að uppfæra reitinn **Brúttóþyngd**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-521">In the **Close container** dialog box, select **Get system weight** to have the system update the **Gross weight** field.</span></span>
1. <span data-ttu-id="5f1a4-522">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-522">Select **OK**.</span></span> <span data-ttu-id="5f1a4-523">Gámurinn er fluttur á staðsetninguna *SORT* og er tilbúinn til röðunar.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-523">The container is moved to the *SORT* location and is ready for sorting.</span></span>

<span data-ttu-id="5f1a4-524">Til að skoða upplýsingar um gáminn skal fara í **Vöruhúsakerfi \> Pökkun og gámun \> Gámar** og leita að gámakennum sem búin voru til við pökkun.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-524">To view the container details, go to **Warehouse management \> Packing and containerization \> Containers** , and search for the container IDs that were created during packing.</span></span>

### <a name="sort-the-containers"></a><span data-ttu-id="5f1a4-525">Raða gámum</span><span class="sxs-lookup"><span data-stu-id="5f1a4-525">Sort the containers</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5f1a4-526">Þegar farið er í valmyndaratriðið **Röðun á bretti** í fartækjaforritinu til að gera röðun á útleið, sést hnappur sem merktur er **Fullhlaðið**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-526">When you access the **Pallet build** menu item on the mobile app to do outbound sorting, you will see a button that is labeled **Full**.</span></span> <span data-ttu-id="5f1a4-527">*Ekki nota hnappinn **Fullhlaðið** til að raða eða loka stöðunni.*</span><span class="sxs-lookup"><span data-stu-id="5f1a4-527">*Don't use the **Full** button to sort or close the position.*</span></span>
>
> <span data-ttu-id="5f1a4-528">Hnappurinn **Fullhlaðið** kemur sjálfgefið fram og er ekki hægt að óvirkja eða fjarlægja af síðunni.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-528">The **Full** button is provided by default and can't be disabled or removed from the page.</span></span> <span data-ttu-id="5f1a4-529">Hann er ekki notaður fyrir eiginleikann *Röðun á útleið*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-529">It isn't used for the *Outbound sorting* feature.</span></span>

#### <a name="sort-the-first-container"></a><span data-ttu-id="5f1a4-530">Raða fyrsta gámnum</span><span class="sxs-lookup"><span data-stu-id="5f1a4-530">Sort the first container</span></span>

1. <span data-ttu-id="5f1a4-531">Í fartækinu skal skrá sig inn í vöruhús *62* með því að nota notandakennið sem var stofnað fyrir þessa atburðarás (eða notandakennið fyrir notanda fyrirliggjandi sýnigagna).</span><span class="sxs-lookup"><span data-stu-id="5f1a4-531">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="5f1a4-532">Í aðalvalmyndinni skal velja **Á útleið**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-532">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="5f1a4-533">Í valmyndinni **Á útleið** skal velja **Röðun á bretti**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-533">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="5f1a4-534">Í reitinn **NP/Gám** skal slá inn fyrsta gámakennið sem tengist sölupöntun 1.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-534">In the **LP/Con** field, enter the first container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="5f1a4-535">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-535">Select **OK**.</span></span>
1. <span data-ttu-id="5f1a4-536">Fyrst að engir röðunarstaðir eru til sem stendur, þarf að tilgreina einn.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-536">Because no sort positions currently exist, you must specify one.</span></span> <span data-ttu-id="5f1a4-537">Í reitinn **Staðsetningarkenni röðunar** skal slá inn *SP01*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-537">In the **Sort position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="5f1a4-538">Fyrst að engin númeraplata sem tengist röðunarstað *SP01* er til sem stendur, þarf að tilgreina einn.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-538">Because no LP is currently associated with sort position *SP01* , you must specify one.</span></span> <span data-ttu-id="5f1a4-539">Í reitinn **NP** skal slá inn *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-539">In the **LP** field, enter *PLP01*.</span></span>
1. <span data-ttu-id="5f1a4-540">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-540">Select **OK**.</span></span>
1. <span data-ttu-id="5f1a4-541">Kveikt er á sannprófun röðunarstaðs og því þarf að slá inn staðsetningarkenni röðunar aftur.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-541">Because sort position validation is turned on, you must enter the sort position ID again.</span></span> <span data-ttu-id="5f1a4-542">Í reitinn **Staðsetningarkenni röðunar** skal slá inn *SP01*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-542">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="5f1a4-543">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-543">Select **OK**.</span></span>

    <span data-ttu-id="5f1a4-544">Skilaboðin „Vinnu er lokið“ birtast.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-544">You receive a "Work completed" message.</span></span>

> [!TIP]
> <span data-ttu-id="5f1a4-545">Til að skoða röðunarstaðinn og númeraplötuna í henni skal fara í **Vöruhúsakerfi \> Pökkun og gámun \> Úthlutanir á staðsetningum röðunar á útleið**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-545">To view the sort position and the LP in it, go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
>
> <span data-ttu-id="5f1a4-546">Síðan **Úthlutanir á staðsetningum röðunar á útleið** sýnir alla röðunarstaði sem eru virkir sem stendur.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-546">The **Outbound sorting position assignments** page shows all the sort positions that are currently active.</span></span> <span data-ttu-id="5f1a4-547">Reiturinn **Færslur röðunarstaðs** sýnir númeraplötuna sem tengist hverri röðunarstöðu og gámana sem eru í röðunarstöðunni.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-547">The **Sort position transactions** field shows the LP that is associated with each sort position, and the containers that are in the sort position.</span></span> <span data-ttu-id="5f1a4-548">Takið eftir því að ein röðunarstaðan er til og að flýtiflipinn **Skilyrði röðunarstaðs** sýnir skilyrði **Sending - Flutningsþjónusta - Flug**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-548">Notice that one sort position currently exists, and that the **Sort position criteria** FastTab shows a criterion of **Shipment – Carrier service - Air**.</span></span>

#### <a name="sort-the-remaining-containers"></a><span data-ttu-id="5f1a4-549">Raða gámunum sem eftir eru</span><span class="sxs-lookup"><span data-stu-id="5f1a4-549">Sort the remaining containers</span></span>

1. <span data-ttu-id="5f1a4-550">Í fartækinu skal skrá sig inn í vöruhús *62* með því að nota notandakennið sem var stofnað fyrir þessa atburðarás (eða notandakennið fyrir notanda fyrirliggjandi sýnigagna).</span><span class="sxs-lookup"><span data-stu-id="5f1a4-550">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="5f1a4-551">Í aðalvalmyndinni skal velja **Á útleið**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-551">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="5f1a4-552">Í valmyndinni **Á útleið** skal velja **Röðun á bretti**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-552">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="5f1a4-553">Í reitinn **NP/Gám** skal slá inn næsta gámakennið sem tengist sölupöntun 1.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-553">In the **LP/Con** field, enter the second container ID that is associated with sales order 1.</span></span>
1. <span data-ttu-id="5f1a4-554">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-554">Select **OK**.</span></span> <span data-ttu-id="5f1a4-555">Fyrst að flokkunarsniðmát er uppsett til að raða sjálfkrafa, og röðunarstaður sem er með samsvarandi skilyrði er þegar til, verður þér sjálfkrafa vísað á réttan röðunarstað.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-555">Because the sorting template is set up to sort automatically, and a sort position that has matching criteria already exists, you're automatically directed to the correct sort position.</span></span>
1. <span data-ttu-id="5f1a4-556">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-556">Select **OK**.</span></span>
1. <span data-ttu-id="5f1a4-557">Staðfestið staðsetningarkenni röðunar til að gefa til kynna að birgðirnar séu á réttum stað.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-557">Confirm the sort position ID to indicate that the inventory is in the correct place.</span></span> <span data-ttu-id="5f1a4-558">Í reitinn **Staðsetningarkenni röðunar** skal slá inn *SP01*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-558">In the **Sort Position ID** field, enter *SP01*.</span></span>
1. <span data-ttu-id="5f1a4-559">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-559">Select **OK**.</span></span>

    <span data-ttu-id="5f1a4-560">Vinnu er lokið við annan gáminn úr sölupöntun 1.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-560">Work is completed on the second container from sales order 1.</span></span> <span data-ttu-id="5f1a4-561">Þú munt nú raða gámunum sem eftir eru úr sölupöntun 2.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-561">You will now sort the remaining containers from sales order 2.</span></span>

1. <span data-ttu-id="5f1a4-562">Í reitinn **NP/Gám** skal slá inn gámakenni gámsins í sölupöntun 2 sem er með vöruna *A0001*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-562">In the **LP/Con** field, enter the container ID of the container from sales order 2 that holds item *A0001*.</span></span> <span data-ttu-id="5f1a4-563">Fyrst að flutningsþjónustan er ekki sú sama er beðið um að færa inn nýjan röðunarstað og úthluta númeraplötu á þá staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-563">Because the carrier service differs, you're prompted to enter a new sort position and assign an LP to that position.</span></span> <span data-ttu-id="5f1a4-564">Notið röðunarstað *SP02* og númeraplötu *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-564">Use sort position *SP02* and LP *PLP02*.</span></span>
1. <span data-ttu-id="5f1a4-565">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-565">Select **OK**.</span></span>
1. <span data-ttu-id="5f1a4-566">Staðfestið röðunarstaðinn með því að slá inn *SP02* í reitinn **Staðsetningarkenni röðunar**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-566">Confirm the sort position by entering *SP02* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="5f1a4-567">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-567">Select **OK**.</span></span>

    <span data-ttu-id="5f1a4-568">Vinnu er lokið við gáminn.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-568">Work is completed on the container.</span></span>

1. <span data-ttu-id="5f1a4-569">Í reitinn **NP/Gám** skal slá inn gámakenni fyrir eftirstandandi gám í sölupöntun 2 sem er með vöruna *A0002*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-569">In the **LP/Con** field, enter the container ID for the remaining container from sales order 2 that holds item *A0002*.</span></span> <span data-ttu-id="5f1a4-570">Fyrst að flutningsþjónustan er sú sama og flutningsþjónusta sölupöntunar 1, sýnir kerfið fyrirliggjandi röðunarstað sem er með samsvarandi skilyrði.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-570">Because the carrier service is the same as the carrier service for sales order 1, the system shows the existing sort position that has matching criteria.</span></span>
1. <span data-ttu-id="5f1a4-571">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-571">Select **OK**.</span></span>
1. <span data-ttu-id="5f1a4-572">Staðfestið röðunarstaðinn með því að slá inn *SP01* í reitinn **Staðsetningarkenni röðunar**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-572">Confirm the sort position by entering *SP01* in the **Sort Position ID** field.</span></span>
1. <span data-ttu-id="5f1a4-573">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-573">Select **OK**.</span></span>

    <span data-ttu-id="5f1a4-574">Vinnu er lokið við gáminn.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-574">Work is completed on the container.</span></span>

### <a name="close-the-outbound-sorting-positions"></a><span data-ttu-id="5f1a4-575">Loka röðunarstöðum á útleið</span><span class="sxs-lookup"><span data-stu-id="5f1a4-575">Close the outbound sorting positions</span></span>

<span data-ttu-id="5f1a4-576">Þegar búið er að raða öllum birgðum verður að loka staðnum áður en hægt er að búa til vinnu.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-576">When all inventory has been sorted, the position must be closed before work can be created.</span></span> <span data-ttu-id="5f1a4-577">Röðuð birgðatínsluvinna verður búin til að fara með birgðirnar í útskotið.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-577">Sorted inventory picking work will be created to take the inventory to the bay door.</span></span>

#### <a name="close-a-position-from-the-mobile-device"></a><span data-ttu-id="5f1a4-578">Loka staðsetningu úr fartækinu</span><span class="sxs-lookup"><span data-stu-id="5f1a4-578">Close a position from the mobile device</span></span>

1. <span data-ttu-id="5f1a4-579">Í fartækinu skal skrá sig inn í vöruhús *62* með því að nota notandakennið sem var stofnað fyrir þessa atburðarás (eða notandakennið fyrir notanda fyrirliggjandi sýnigagna).</span><span class="sxs-lookup"><span data-stu-id="5f1a4-579">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="5f1a4-580">Í aðalvalmyndinni skal velja **Á útleið**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-580">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="5f1a4-581">Í valmyndinni **Á útleið** skal velja **Röðun á bretti**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-581">On the **Outbound** menu, select **Pallet build**.</span></span>
1. <span data-ttu-id="5f1a4-582">Í reitinn **NP/Gám** skal slá inn gámakenni sem var raðað fyrir röðunarstaðinn *SP01*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-582">In the **LP/Con** field, enter a container ID that was sorted to sort position *SP01*.</span></span>
1. <span data-ttu-id="5f1a4-583">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-583">Select **OK**.</span></span>
1. <span data-ttu-id="5f1a4-584">Eftirfarandi skilaboð birtast: „Gámnum hefur þegar verið raðað á staðsetninguna SP01.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-584">You receive the following message: "The container is already sorted to position SP01.</span></span> <span data-ttu-id="5f1a4-585">Loka staðsetningunni?</span><span class="sxs-lookup"><span data-stu-id="5f1a4-585">Close the position?"</span></span> <span data-ttu-id="5f1a4-586">Veljið **Loka**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-586">Select **Close**.</span></span>

    <span data-ttu-id="5f1a4-587">Vinnu er lokið.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-587">Work is completed.</span></span>

#### <a name="close-a-position-from-outbound-sorting-position-assignments"></a><span data-ttu-id="5f1a4-588">Loka staðsetningu í úthlutunum á röðunarstað á útleið</span><span class="sxs-lookup"><span data-stu-id="5f1a4-588">Close a position from outbound sorting position assignments</span></span>

1. <span data-ttu-id="5f1a4-589">Fara skal í **Vöruhúsakerfi \> Pökkun og gámun \> Úthlutanir á röðunarstað á útleið**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-589">Go to **Warehouse management \> Packing and containerization \> Outbound sorting position assignments**.</span></span>
1. <span data-ttu-id="5f1a4-590">Í vinstri dálknum skal velja **SP02**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-590">In the left column, select **SP02**.</span></span> <span data-ttu-id="5f1a4-591">Þessi lína röðunarstaðs á útleið er sú sem á að loka.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-591">This outbound sorting position row is the one that you will close.</span></span>
1. <span data-ttu-id="5f1a4-592">Á aðgerðasvæðinu skal velja **Loka staðsetningu**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-592">On the Action Pane, select **Close position**.</span></span> <span data-ttu-id="5f1a4-593">Færsla röðunarstaðs er lokað og hún ekki lengur sýnd.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-593">The sorting position record is closed and is no longer shown.</span></span>

    > [!TIP]
    > <span data-ttu-id="5f1a4-594">Til að sýna allar færslur lokaðra staðsetninga skal velja gátreitinn **Sýna lokaðar**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-594">To show all closed position records, select the **Show closed** check box.</span></span>

### <a name="sorted-inventory-picking"></a><span data-ttu-id="5f1a4-595">Tiltekt í flokkuðum birgðum</span><span class="sxs-lookup"><span data-stu-id="5f1a4-595">Sorted inventory picking</span></span>

<span data-ttu-id="5f1a4-596">Ljúka þarf tiltekt flokkaðra birgða.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-596">You must complete the sorted inventory picking work.</span></span> <span data-ttu-id="5f1a4-597">Þegar henni er lokið verða birgðir tíndar fyrir sölupöntunina.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-597">When it's completed, the inventory will be picked to the sales order.</span></span> <span data-ttu-id="5f1a4-598">Á þeim tímapunkti eiga öll önnur vöruhúsaferli við.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-598">At that point, all other warehouse processes apply.</span></span>

1. <span data-ttu-id="5f1a4-599">Í fartækinu skal skrá sig inn í vöruhús *62* með því að nota notandakennið sem var stofnað fyrir þessa atburðarás (eða notandakennið fyrir notanda fyrirliggjandi sýnigagna).</span><span class="sxs-lookup"><span data-stu-id="5f1a4-599">On the mobile device, sign in to warehouse *62* by using the user ID that you created for this scenario (or the user ID of an existing demo data user).</span></span>
1. <span data-ttu-id="5f1a4-600">Í aðalvalmyndinni skal velja **Á útleið**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-600">On the main menu, select **Outbound**.</span></span>
1. <span data-ttu-id="5f1a4-601">Í valmyndinni **Á útleið** skal velja **Hleðsla frá röðun**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-601">On the **Outbound** menu, select **Load from Sorting**.</span></span>
1. <span data-ttu-id="5f1a4-602">Sláið inn auðkenni marknúmeraplötu úr fyrsta röðunarstaðnum, *SP01*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-602">Enter the target LP ID from the first sort position, *SP01*.</span></span> <span data-ttu-id="5f1a4-603">Stilltu reitinn **Kenni** á *PLP01*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-603">Set the **ID** field to *PLP01*.</span></span>
1. <span data-ttu-id="5f1a4-604">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-604">Select **OK**.</span></span>
1. <span data-ttu-id="5f1a4-605">Síðan **Tiltekt í flokkuðum birgðum** sýnir tiltektarvinnuna sem þarf að gera.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-605">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="5f1a4-606">Veljið úr staðsetningunni *SORT* og marknúmeraplötunni *PLP01* , sem er með margar vörur og magn upp á *3*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-606">Pick from the *SORT* location and target LP *PLP01* , which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="5f1a4-607">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-607">Select **OK**.</span></span>
1. <span data-ttu-id="5f1a4-608">Síðan **Tiltekt í flokkuðum birgðum** sýnir frágangsvinnuna sem þarf að gera.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-608">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="5f1a4-609">Gangið frá í staðsetninguna *Útskot* og marknúmeraplötuna *PLP01* , sem er með margar vörur og magn upp á *3*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-609">Put to the *Baydoor* location and target LP *PLP01* , which has multiple items and a quantity of *3*.</span></span>
1. <span data-ttu-id="5f1a4-610">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-610">Select **OK**.</span></span>

    <span data-ttu-id="5f1a4-611">Vinnu er lokið.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-611">Work is completed.</span></span>

1. <span data-ttu-id="5f1a4-612">Sláið inn kenni marknúmeraplötu úr seinni röðunarstaðnum *SP02*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-612">Enter the target license plate ID from the second sort position, *SP02*.</span></span> <span data-ttu-id="5f1a4-613">Stilltu reitinn **Kenni** á *PLP02*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-613">Set the **ID** field to *PLP02*.</span></span>
1. <span data-ttu-id="5f1a4-614">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-614">Select **OK**.</span></span>
1. <span data-ttu-id="5f1a4-615">Síðan **Tiltekt í flokkuðum birgðum** sýnir tiltektarvinnuna sem þarf að gera.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-615">The **Sorted inventory picking: Pick** page shows the pick work that must be done.</span></span> <span data-ttu-id="5f1a4-616">Tínið úr staðsetningunni *SORT* og marknúmeraplötunni *PLP02* , sem er með margar vörur og magn upp á *1*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-616">Pick from the *SORT* location and target LP *PLP02* , which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="5f1a4-617">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-617">Select **OK**.</span></span>
1. <span data-ttu-id="5f1a4-618">Síðan **Tiltekt í flokkuðum birgðum** sýnir frágangsvinnuna sem þarf að gera.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-618">The **Sorted inventory picking: Put** page shows the put work that must be done.</span></span> <span data-ttu-id="5f1a4-619">Gangið frá í staðsetninguna *Útskot* og marknúmeraplötuna *PLP02* , sem er með margar vörur og magn upp á *1*.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-619">Put to the *Baydoor* location and target LP *PLP02* , which has multiple items and a quantity of *1*.</span></span>
1. <span data-ttu-id="5f1a4-620">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-620">Select **OK**.</span></span>

    <span data-ttu-id="5f1a4-621">Vinnu er lokið.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-621">Work is completed.</span></span>

<span data-ttu-id="5f1a4-622">Héðan í frá eiga öll önnur vöruhúsaferli við.</span><span class="sxs-lookup"><span data-stu-id="5f1a4-622">From this point forward, all other warehouse processes apply.</span></span>
