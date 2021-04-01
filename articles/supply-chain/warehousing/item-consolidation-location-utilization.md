---
title: Vörusameining - nýting á staðsetningu
description: Í þessu efnisatriði er að finna upplýsingar um virkni sem auðveldar stjórnendum vöruhúss að skoða og sía rúmmálsnýtingu staðsetninga í öllu vöruhúsinu. Stjórnendur geta valið staðsetningar og búið til birgðahreyfingarvinnu beint úr síðu Vörusameiningar til að sameina vörur og þar af leiðandi nýta betur rými vöruhússins.
author: Mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPhysDimUOM, WHSMovementType, WHSItemConsolidationForm, WHSRFMenu, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 3b20b41d27e5faeac7ea88940c086ae33390dc29
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217006"
---
# <a name="item-consolidation---location-utilization"></a><span data-ttu-id="7d517-104">Vörusameining - nýting á staðsetningu</span><span class="sxs-lookup"><span data-stu-id="7d517-104">Item consolidation - location utilization</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7d517-105">Í þessu efnisatriði er að finna upplýsingar um virkni sem auðveldar stjórnendum vöruhúss að skoða og sía rúmmálsnýtingu staðsetninga í öllu vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="7d517-105">This topic provides information about functionality that makes it easy for warehouse managers to view and filter the volumetric utilization of locations across the warehouse.</span></span> <span data-ttu-id="7d517-106">Stjórnendur geta valið staðsetningar og búið til birgðahreyfingarvinnu beint úr síðunni **Vörusameining** til að sameina vörur og þar af leiðandi nýta betur rými vöruhússins.</span><span class="sxs-lookup"><span data-stu-id="7d517-106">Managers can select locations and create inventory movement work directly from the **Item Consolidation** page to consolidate items and therefore make better use of warehouse space.</span></span>

## <a name="turn-on-the-features"></a><span data-ttu-id="7d517-107">Kveikja á eiginleikum</span><span class="sxs-lookup"><span data-stu-id="7d517-107">Turn on the features</span></span>

<span data-ttu-id="7d517-108">Áður en hægt er að nota eiginleikana sem lýst er í þessu efnisatriði þarf að kveikja á þeim í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="7d517-108">Before you can use the features that are described in this topic, you must turn them on in your system.</span></span> <span data-ttu-id="7d517-109">Stjórnendur geta notað vinnusvæðið [Eiginleikastjórnunar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu þessara eiginleika og kveikja á þeim ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="7d517-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the features and turn them on if they are required.</span></span> <span data-ttu-id="7d517-110">Kveikja á báðum eiginleikum, í þeirri röð sem þeir eru sýndir.</span><span class="sxs-lookup"><span data-stu-id="7d517-110">Turn on both the following features, in the order that they are listed in.</span></span> <span data-ttu-id="7d517-111">(Báðir eiginleikarnir eru fyrir eininguna **Vöruhúsastjórnun**.)</span><span class="sxs-lookup"><span data-stu-id="7d517-111">(Both features are for the **Warehouse management** module.)</span></span>

1. <span data-ttu-id="7d517-112">Staðsetningarstaða vöruhúss</span><span class="sxs-lookup"><span data-stu-id="7d517-112">Warehouse location status</span></span>
2. <span data-ttu-id="7d517-113">Nýting á staðsetningu samstæðuvöru</span><span class="sxs-lookup"><span data-stu-id="7d517-113">Item consolidation location utilization</span></span>

## <a name="warehouse-location-status"></a><span data-ttu-id="7d517-114">Staðsetningarstaða vöruhúss</span><span class="sxs-lookup"><span data-stu-id="7d517-114">Warehouse location status</span></span>

<span data-ttu-id="7d517-115">Eiginleikinn *Staðsetningarstaða vöruhúss* bætir fjórum nýjum reitum við síðuna **Staðsetningar** til að halda utan um viðbótarupplýsingar um núverandi stöðu staðsetningar:</span><span class="sxs-lookup"><span data-stu-id="7d517-115">The *Warehouse location status* feature adds four new fields to the **Locations** page to track additional information about the current state of the location:</span></span>

- <span data-ttu-id="7d517-116">**Vörunúmer** – Varan sem er núna í staðsetningunni.</span><span class="sxs-lookup"><span data-stu-id="7d517-116">**Item number** – The item that is currently in the location.</span></span> <span data-ttu-id="7d517-117">Ef staðsetningin inniheldur margar vörur er þessi reitur auður.</span><span class="sxs-lookup"><span data-stu-id="7d517-117">If the location contains multiple items, this field will be blank.</span></span>
- <span data-ttu-id="7d517-118">**Dagsetning og tími síðustu virkni** – Tímastimpill síðustu færslu vöruhúss sem var framkvæmd á staðsetningunni.</span><span class="sxs-lookup"><span data-stu-id="7d517-118">**Last activity date and time** – The timestamp of the last warehouse transaction that was performed against the location.</span></span>
- <span data-ttu-id="7d517-119">**Aldursdagsetning** –Dagsetningin sem birgðir í staðsetningu voru færðar inn í vöruhúsið.</span><span class="sxs-lookup"><span data-stu-id="7d517-119">**Aging date** – The date when the inventory in the location was brought into the warehouse.</span></span> <span data-ttu-id="7d517-120">Þetta gildi er reiknað út frá aldursdagsetningu númeraplötunnar.</span><span class="sxs-lookup"><span data-stu-id="7d517-120">This date is calculated based on the license plate aging date.</span></span> <span data-ttu-id="7d517-121">Þó þessi dagsetning sé nákvæm fyrir staðsetningar sem er raktar með númeraplötu er hugsanlega ekki nákvæmt fyrir staðsetningar ekki raktar með númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="7d517-121">Although this date is accurate for license plate–tracked locations, it might not be accurate for locations that aren't license plate–tracked.</span></span>
- <span data-ttu-id="7d517-122">**Staðsetningarstaða** – Staða staðsetningarinnar.</span><span class="sxs-lookup"><span data-stu-id="7d517-122">**Location status** – The status of the location.</span></span> <span data-ttu-id="7d517-123">Fjögur gildi eru í boði:</span><span class="sxs-lookup"><span data-stu-id="7d517-123">Four values are available:</span></span>

    - <span data-ttu-id="7d517-124">**Óákveðið** – Staðsetningarforstillingin rekur ekki stöðuna.</span><span class="sxs-lookup"><span data-stu-id="7d517-124">**Undetermined** – The location profile doesn't track status.</span></span> <span data-ttu-id="7d517-125">Þar af leiðandi er núverandi staða óþekkt.</span><span class="sxs-lookup"><span data-stu-id="7d517-125">Therefore, the current status is unknown.</span></span>
    - <span data-ttu-id="7d517-126">**Autt** – Engar birgðir eru á staðsetningunni sem stendur.</span><span class="sxs-lookup"><span data-stu-id="7d517-126">**Empty** – No inventory is currently in the location.</span></span>
    - <span data-ttu-id="7d517-127">**Tiltekt** – Færslur á útleið hafa verið framkvæmdar á staðsetningunni eftir að hún var síðast tóm.</span><span class="sxs-lookup"><span data-stu-id="7d517-127">**Picking** – Outbound transactions have been performed against the location after it was last empty.</span></span>
    - <span data-ttu-id="7d517-128">**Geymsla** – Aðeins færslur á innleið hafa verið framkvæmdar frá því að staðsetningin var síðast tóm.</span><span class="sxs-lookup"><span data-stu-id="7d517-128">**Storage** – Only inbound transactions have been performed since the location was last empty.</span></span>

<span data-ttu-id="7d517-129">Þessi svæði gefa stjórnendum vöruhúsa betri yfirsýn yfir stöðu staðsetninganna í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="7d517-129">These fields let warehouse managers get a better overview of the status of the locations in the warehouse.</span></span> <span data-ttu-id="7d517-130">Þau bjóða einnig upp á háþróaðri skýrslugerð og síun.</span><span class="sxs-lookup"><span data-stu-id="7d517-130">They also allow for more advanced reporting and filtering.</span></span>

## <a name="set-up-item-consolidation-and-location-utilization"></a><span data-ttu-id="7d517-131">Setja upp vörusameiningu og nýtingu staðsetningar</span><span class="sxs-lookup"><span data-stu-id="7d517-131">Set up item consolidation and location utilization</span></span>

<span data-ttu-id="7d517-132">Þessi hluti lýsir því hvernig á að búa kerfið undir að nota vörusameiningu og nýtingu staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="7d517-132">This section describes how to prepare your system to use item consolidation and location utilization.</span></span> <span data-ttu-id="7d517-133">Aðferðirnar nota sýnigildi úr stöðluðu sýnigögnunum.</span><span class="sxs-lookup"><span data-stu-id="7d517-133">The procedures use sample values from the standard demo data.</span></span> <span data-ttu-id="7d517-134">Ef ætlunin er að fara í gegnum dæmið sem boðið er upp á síðar í þessu efnisatriði, skal velja lögaðilann **USMF** (sem inniheldur stöðluðu sýnigögnin) og búa til hverja færslu sem er lýst í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="7d517-134">If you plan to work through the example scenario that is provided later in this topic, select the **USMF** legal entity (which contains the standard demo data), and create each record that is described in this section.</span></span> <span data-ttu-id="7d517-135">Ef ætlunin er ekki að fara í gegnum dæmið, er hægt að líta á gildin sem boðið er upp á hér sem dæmi um gerð uppsetningar sem þarf að ljúka til að geta notað eiginleikana.</span><span class="sxs-lookup"><span data-stu-id="7d517-135">If you don't plan to work through the example scenario, the values that are provided here can be considered examples of the types of setup that you must complete to use the features.</span></span>

### <a name="released-product"></a><span data-ttu-id="7d517-136">Útgefin afurð</span><span class="sxs-lookup"><span data-stu-id="7d517-136">Released product</span></span>

1. <span data-ttu-id="7d517-137">Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="7d517-137">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="7d517-138">Í svæðið **Vörunúmer** skaltu velja *M9201* og opna upplýsingasíðuna.</span><span class="sxs-lookup"><span data-stu-id="7d517-138">In the **Item number** field, select *M9201*, and open the details page.</span></span>
1. <span data-ttu-id="7d517-139">Á Aðgerðasvæði, á flipanum **Stjórna birgðum**, í flokknum **Vöruhús**, velurðu **Efnislegar víddir**.</span><span class="sxs-lookup"><span data-stu-id="7d517-139">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="7d517-140">Á síðunni **Efnisleg vídd**, á aðgerðasvæðinu, skal velja **Nýr**.</span><span class="sxs-lookup"><span data-stu-id="7d517-140">On the **Physical dimension** page, on the Action Pane, select **New**.</span></span>

    <span data-ttu-id="7d517-141">Nýrri línu er bætt við hnitanetið.</span><span class="sxs-lookup"><span data-stu-id="7d517-141">A new line is added to the grid.</span></span> <span data-ttu-id="7d517-142">Reiturinn **Vörunúmeri** er forstilltur.</span><span class="sxs-lookup"><span data-stu-id="7d517-142">The **Item number** field is preset.</span></span>

1. <span data-ttu-id="7d517-143">Í reitnum **Eining** skal velja *ea*.</span><span class="sxs-lookup"><span data-stu-id="7d517-143">In the **Unit** field, select *ea*.</span></span> <span data-ttu-id="7d517-144">Eftirstandandi reitir í línunni eru sjálfkrafa stilltir.</span><span class="sxs-lookup"><span data-stu-id="7d517-144">The remaining fields on the line are automatically set.</span></span>
1. <span data-ttu-id="7d517-145">Veljið **Vista** og lokið skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="7d517-145">Select **Save**, and close the page.</span></span>

### <a name="location-profile"></a><span data-ttu-id="7d517-146">Forstillingar staðsetningar</span><span class="sxs-lookup"><span data-stu-id="7d517-146">Location profile</span></span>

1. <span data-ttu-id="7d517-147">Fara í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Forstillingar staðsetningar**.</span><span class="sxs-lookup"><span data-stu-id="7d517-147">Go to **Warehouse management \> Setup \> Warehouse \> Location profiles**.</span></span>
1. <span data-ttu-id="7d517-148">Veldu **FLOOR-05** á lista staðsetningarforstillinga.</span><span class="sxs-lookup"><span data-stu-id="7d517-148">In the list of location profiles, select **FLOOR-05**.</span></span>
1. <span data-ttu-id="7d517-149">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="7d517-149">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="7d517-150">Í flýtiflipanum **Almennt** skal ganga úr skugga um að báðir eftirfarandi valkostir séu stilltir á *Já*:</span><span class="sxs-lookup"><span data-stu-id="7d517-150">On the **General** FastTab, make sure that both the following options are set to *Yes*:</span></span>

    - <span data-ttu-id="7d517-151">Virkja vöru á staðsetningu</span><span class="sxs-lookup"><span data-stu-id="7d517-151">Enable item in location</span></span>
    - <span data-ttu-id="7d517-152">Virkja staðsetningarstöðu</span><span class="sxs-lookup"><span data-stu-id="7d517-152">Enable location status</span></span>

1. <span data-ttu-id="7d517-153">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="7d517-153">Select **Save**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="7d517-154">Ef valkostirnir **Virkja vöru á staðsetningu** og **Virkja staðsetningarstöðu** voru þegar stilltir á *Já* skal hoppa yfir í leiðbeiningarnar um uppsetningu flýtiflipans **Víddir** í skrefi 10.</span><span class="sxs-lookup"><span data-stu-id="7d517-154">If the **Enable item in location** and **Enable location status** options were already set to *Yes*, skip ahead to the instructions for setting up the **Dimensions** FastTab in step 10.</span></span> <span data-ttu-id="7d517-155">Ef valkostirnir voru ekki þegar stilltir á *Já* þarf að keyra samræmisathugun fyrir eininguna **Vöruhúsastjórnun** þegar búið er að stilla þá handvirkt.</span><span class="sxs-lookup"><span data-stu-id="7d517-155">If the options weren't already set to *Yes*, you must run a consistency check for the **Warehouse management** module after you manually set them.</span></span> <span data-ttu-id="7d517-156">Ef þetta er málið skaltu halda áfram í næsta skref.</span><span class="sxs-lookup"><span data-stu-id="7d517-156">In this case, continue to the next step.</span></span>

1. <span data-ttu-id="7d517-157">Til að keyra samræmisathugunina skal fara í **Kerfisstjórnun \> Reglubundin verkefni \> Gagnagrunnur \> Samræmisathugun**.</span><span class="sxs-lookup"><span data-stu-id="7d517-157">To run the consistency check, go to **System administration \> Periodic tasks \> Database \> Consistency check**.</span></span>
1. <span data-ttu-id="7d517-158">Í svarglugganum **Samræmisathugun** skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="7d517-158">In the **Consistency check** dialog box, set the following values:</span></span>

    - <span data-ttu-id="7d517-159">**Eining:** *Vöruhúsakerfi*</span><span class="sxs-lookup"><span data-stu-id="7d517-159">**Module:** *Warehouse management*</span></span>
    - <span data-ttu-id="7d517-160">**Villuleita/laga:** *Villuleita*</span><span class="sxs-lookup"><span data-stu-id="7d517-160">**Check/Fix:** *Check*</span></span>
    - <span data-ttu-id="7d517-161">**Frá dagsetningu:** Hafðu reitinn auðann.</span><span class="sxs-lookup"><span data-stu-id="7d517-161">**From date:** Leave this field blank.</span></span>
    - <span data-ttu-id="7d517-162">**Samræmisathugun fyrir stöðu vöruhúsastaðsetningar:** Veldu þennan gátreit.</span><span class="sxs-lookup"><span data-stu-id="7d517-162">**Warehouse location status consistency check:** Select this check box.</span></span>

1. <span data-ttu-id="7d517-163">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="7d517-163">Select **OK**.</span></span>

    > [!TIP]
    > <span data-ttu-id="7d517-164">Þegar samræmisathugun er lokið færðu senda tilkynningu.</span><span class="sxs-lookup"><span data-stu-id="7d517-164">When the consistency check is completed, you receive a notification.</span></span> <span data-ttu-id="7d517-165">Opnið [Aðgerðamiðstöð](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) til að skoða skilaboðin.</span><span class="sxs-lookup"><span data-stu-id="7d517-165">Open the [Action Center](../../fin-ops-core/fin-ops/get-started/user-interface-elements.md#notifications) to view the message.</span></span> <span data-ttu-id="7d517-166">Smelltu á **Upplýsingar um skilaboð** til að skoða upplýsingarnar.</span><span class="sxs-lookup"><span data-stu-id="7d517-166">Select **Message details** to view the details.</span></span>
    >
    > <span data-ttu-id="7d517-167">Ef skilaboðin fyrir samræmisathugun segja: „Rangar upplýsingar um stöðu staðsetningar fannst fyrir staðsetningu XXXX í vöruhúsi XX,“ þarf að keyra samræmisathugunina aftur.</span><span class="sxs-lookup"><span data-stu-id="7d517-167">If the message for the consistency check states, "Incorrect location status information found for location XXXX in warehouse XX," you must run the consistency check again.</span></span> <span data-ttu-id="7d517-168">Að þessu sinni skal stilla reitinn **Athuga/Laga** á *Laga villu*.</span><span class="sxs-lookup"><span data-stu-id="7d517-168">This time, set the **Check/Fix** field to *Fix error*.</span></span> <span data-ttu-id="7d517-169">Skoða skilaboðin til að ganga úr skugga um að engar villur hafi fundist.</span><span class="sxs-lookup"><span data-stu-id="7d517-169">View the messages to make sure that no errors were found.</span></span>

1. <span data-ttu-id="7d517-170">Nú þarf að ljúka uppsetningu staðsetningarforstillingar.</span><span class="sxs-lookup"><span data-stu-id="7d517-170">You must now finish setting up the location profile.</span></span> <span data-ttu-id="7d517-171">Farið í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Staðsetningarforstillingar**, veljið staðsetningarforstillingu **FLOOR-05** og síðan, á aðgerðasvæðinu, skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="7d517-171">Go back to **Warehouse management \> Setup \> Warehouse \> Location profiles**, select location profile **FLOOR-05**, and then, on the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="7d517-172">Stilltu eftirfarandi gildi á **Víddir** flipanum:</span><span class="sxs-lookup"><span data-stu-id="7d517-172">On the **Dimensions** FastTab, set the following values:</span></span>

    - <span data-ttu-id="7d517-173">**Hlutfallsleg nýting magns:** *100*</span><span class="sxs-lookup"><span data-stu-id="7d517-173">**Volume utilization percentage:** *100*</span></span>
    - <span data-ttu-id="7d517-174">**Rúmmálsaðferð sem notuð er við birgðastaðsetningu:** *Nota rúmmál staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="7d517-174">**Volumetric method used for inventory location:** *Use location volume*</span></span>
    - <span data-ttu-id="7d517-175">**Raunveruleg hæð staðsetningar:** *10*</span><span class="sxs-lookup"><span data-stu-id="7d517-175">**Actual location height:** *10*</span></span>
    - <span data-ttu-id="7d517-176">**Raunveruleg breidd staðsetningar:** *10*</span><span class="sxs-lookup"><span data-stu-id="7d517-176">**Actual location width:** *10*</span></span>
    - <span data-ttu-id="7d517-177">**Raunveruleg dýpt staðsetningar:** *10*</span><span class="sxs-lookup"><span data-stu-id="7d517-177">**Actual location depth:** *10*</span></span>
    - <span data-ttu-id="7d517-178">**Hámarksþyngd:** *100*</span><span class="sxs-lookup"><span data-stu-id="7d517-178">**Maximum weight:** *100*</span></span>

1. <span data-ttu-id="7d517-179">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="7d517-179">Select **Save**.</span></span>

### <a name="mobile-device-menu-items"></a><span data-ttu-id="7d517-180">Valmyndaratriði fartækis</span><span class="sxs-lookup"><span data-stu-id="7d517-180">Mobile device menu items</span></span>

1. <span data-ttu-id="7d517-181">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="7d517-181">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="7d517-182">Á aðgerðasvæðinu skal velja **Nýtt** til að stofna nýtt valmyndaratriði fyrir flokkun.</span><span class="sxs-lookup"><span data-stu-id="7d517-182">On the Action Pane, select **New** to create a menu item for sorting.</span></span>
1. <span data-ttu-id="7d517-183">Stilla eftirfarandi gildi í hausnum:</span><span class="sxs-lookup"><span data-stu-id="7d517-183">In the header, set the following values:</span></span>

    - <span data-ttu-id="7d517-184">**Nafn valmyndaratriðis:** *Magnleiðréttingar í*</span><span class="sxs-lookup"><span data-stu-id="7d517-184">**Menu item name:** *Adjust In*</span></span>
    - <span data-ttu-id="7d517-185">**Titill:** *Breyta í*</span><span class="sxs-lookup"><span data-stu-id="7d517-185">**Title:** *Adjust In*</span></span>
    - <span data-ttu-id="7d517-186">**Máti:** *Vinna*</span><span class="sxs-lookup"><span data-stu-id="7d517-186">**Mode:** *Work*</span></span>
    - <span data-ttu-id="7d517-187">**Nota fyrirliggjandi vinnu:** *Nei*</span><span class="sxs-lookup"><span data-stu-id="7d517-187">**Use existing work:** *No*</span></span>

1. <span data-ttu-id="7d517-188">Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:</span><span class="sxs-lookup"><span data-stu-id="7d517-188">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="7d517-189">**Ferli verkstofnunar:** *Magnleiðréttingar í*</span><span class="sxs-lookup"><span data-stu-id="7d517-189">**Work creation process:** *Adjustment in*</span></span>
    - <span data-ttu-id="7d517-190">**Gerðir leiðréttinga á birgðaskrá:** *Leiðréttingar í*</span><span class="sxs-lookup"><span data-stu-id="7d517-190">**Inventory adjustment types:** *Adjust in*</span></span>

1. <span data-ttu-id="7d517-191">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="7d517-191">Select **Save**.</span></span>

### <a name="mobile-device-menu"></a><span data-ttu-id="7d517-192">Valmynd fartækis</span><span class="sxs-lookup"><span data-stu-id="7d517-192">Mobile device menu</span></span>

1. <span data-ttu-id="7d517-193">Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.</span><span class="sxs-lookup"><span data-stu-id="7d517-193">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu**.</span></span>
1. <span data-ttu-id="7d517-194">Veldu **Birgðir** á valmyndinni.</span><span class="sxs-lookup"><span data-stu-id="7d517-194">In the list of menus, select **Inventory**.</span></span>
1. <span data-ttu-id="7d517-195">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="7d517-195">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="7d517-196">Á listanum **Tiltækar valmyndir og valmyndaratriði** skaltu finna og velja valmyndaratriðið **Leiðréttingar í**.</span><span class="sxs-lookup"><span data-stu-id="7d517-196">In the **Available Menus And Menu Items** list, find and select the **Adjust In** menu item.</span></span>
1. <span data-ttu-id="7d517-197">Smellið á hægri örvarhnappinn til að færa **Leiðréttingar í** yfir á listann **Valmyndarskipan**.</span><span class="sxs-lookup"><span data-stu-id="7d517-197">Select the right arrow button to move **Adjust In** to the **Menu Structure** list.</span></span> <span data-ttu-id="7d517-198">Á þennan hátt bætirðu nýju valmyndaratriði við valda valmynd.</span><span class="sxs-lookup"><span data-stu-id="7d517-198">In this way, you add the new menu item to the selected menu.</span></span>
1. <span data-ttu-id="7d517-199">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="7d517-199">Select **Save**.</span></span>

### <a name="movement-types"></a><span data-ttu-id="7d517-200">Hreyfingargerðir</span><span class="sxs-lookup"><span data-stu-id="7d517-200">Movement types</span></span>

1. <span data-ttu-id="7d517-201">Fara í **Vöruhúsakerfi \> Uppsetning \> Birgðir \> Hreyfingagerðir**.</span><span class="sxs-lookup"><span data-stu-id="7d517-201">Go to **Warehouse management \> Setup \> Inventory \> Movement types**.</span></span>
1. <span data-ttu-id="7d517-202">Veldu **Nýtt** á aðgerðasvæðinu og stilltu svo eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="7d517-202">On the Action Pane, select **New**, and then set the following values:</span></span>

    - <span data-ttu-id="7d517-203">**Kóði hreyfingargerðar:** *SAMEINA*</span><span class="sxs-lookup"><span data-stu-id="7d517-203">**Movement type code:** *CONSOLIDATE*</span></span>
    - <span data-ttu-id="7d517-204">**Lýsing:** *Sameina staðsetningar*</span><span class="sxs-lookup"><span data-stu-id="7d517-204">**Description:** *Consolidate locations*</span></span>
    - <span data-ttu-id="7d517-205">**Auðkenni vinnuklasa:** *InvMov*</span><span class="sxs-lookup"><span data-stu-id="7d517-205">**Work class ID:** *InvMov*</span></span>

1. <span data-ttu-id="7d517-206">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="7d517-206">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="7d517-207">Dæmi</span><span class="sxs-lookup"><span data-stu-id="7d517-207">Example scenario</span></span>

<span data-ttu-id="7d517-208">Eftirfarandi aðstæður notar vöruhúsaforritið í fartæki til að gera *leiðréttingu á* birgðum á tveimur staðsetningum í vöruhúsinu.</span><span class="sxs-lookup"><span data-stu-id="7d517-208">The following scenario uses the warehouse app on a mobile device to make an inventory *adjustment in* to two locations in the warehouse.</span></span>

### <a name="add-inventory-to-locations"></a><span data-ttu-id="7d517-209">Bæta birgðum við staðsetningar</span><span class="sxs-lookup"><span data-stu-id="7d517-209">Add inventory to locations</span></span>

1. <span data-ttu-id="7d517-210">Skráðu þig inn í fartækið sem notandi sem er settur upp fyrir í vöruhús *51*.</span><span class="sxs-lookup"><span data-stu-id="7d517-210">Sign in to the mobile device as a user who is set up for warehouse *51*.</span></span>
1. <span data-ttu-id="7d517-211">Farið í **Birgðir \> Leiðrétta á**.</span><span class="sxs-lookup"><span data-stu-id="7d517-211">Go to **Inventory \> Adjust In**.</span></span>

    <span data-ttu-id="7d517-212">Nú verður fyrsta leiðrétting staðsetningar færð inn.</span><span class="sxs-lookup"><span data-stu-id="7d517-212">You will now enter the first location adjustment.</span></span>

1. <span data-ttu-id="7d517-213">Í verkinu **Leiðrétting á** skal velja staðsetninguna þar sem gera á birgðaleiðréttinguna.</span><span class="sxs-lookup"><span data-stu-id="7d517-213">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="7d517-214">Í reitnum **LOC** skal velja *LP-001*.</span><span class="sxs-lookup"><span data-stu-id="7d517-214">In the **LOC** field, select *LP-001*.</span></span>
1. <span data-ttu-id="7d517-215">Staðfesta staðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="7d517-215">Confirm the location.</span></span>
1. <span data-ttu-id="7d517-216">Sláðu inn kenni númeraplötu fyrir vöruna sem verður bætt við staðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="7d517-216">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="7d517-217">Í reitinn **LP** skal slá inn *LP00101*.</span><span class="sxs-lookup"><span data-stu-id="7d517-217">In the **LP** field, enter *LP00101*.</span></span>
1. <span data-ttu-id="7d517-218">Staðfesta númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="7d517-218">Confirm the license plate.</span></span>
1. <span data-ttu-id="7d517-219">Sláðu inn magn af vörunni sem verður bætt við númeraplötuna.</span><span class="sxs-lookup"><span data-stu-id="7d517-219">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="7d517-220">Í reitinn **ITEM** skal færa inn *M9201*.</span><span class="sxs-lookup"><span data-stu-id="7d517-220">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="7d517-221">Staðfesta atriði.</span><span class="sxs-lookup"><span data-stu-id="7d517-221">Confirm the item.</span></span>
1. <span data-ttu-id="7d517-222">Sláðu inn magn af vörunni sem verður bætt við.</span><span class="sxs-lookup"><span data-stu-id="7d517-222">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="7d517-223">Í reitinn **Magn** skaltu slá inn *10*.</span><span class="sxs-lookup"><span data-stu-id="7d517-223">In the **QTY** field, enter *10*.</span></span>
1. <span data-ttu-id="7d517-224">Staðfestu magnið.</span><span class="sxs-lookup"><span data-stu-id="7d517-224">Confirm the quantity.</span></span>

    <span data-ttu-id="7d517-225">Skilaboðin „Vinnu er lokið“ birtast.</span><span class="sxs-lookup"><span data-stu-id="7d517-225">You receive a "Work Completed" message.</span></span> <span data-ttu-id="7d517-226">Nú verður önnur leiðrétting staðsetningar færð inn.</span><span class="sxs-lookup"><span data-stu-id="7d517-226">You will now enter the second location adjustment.</span></span>

1. <span data-ttu-id="7d517-227">Í verkinu **Leiðrétting á** skal velja staðsetninguna þar sem gera á birgðaleiðréttinguna.</span><span class="sxs-lookup"><span data-stu-id="7d517-227">In the **Adjustment in** task, select the location to make the inventory adjustment for.</span></span> <span data-ttu-id="7d517-228">Í reitinn **LOC** skal velja *LP-002*.</span><span class="sxs-lookup"><span data-stu-id="7d517-228">In the **LOC** field, select *LP-002*.</span></span>
1. <span data-ttu-id="7d517-229">Staðfesta staðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="7d517-229">Confirm the location.</span></span>
1. <span data-ttu-id="7d517-230">Sláðu inn kenni númeraplötu fyrir vöruna sem verður bætt við staðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="7d517-230">Create a license plate ID for the item that will be added to the location.</span></span> <span data-ttu-id="7d517-231">Í reitinn **LP** skal slá inn *LP00201*.</span><span class="sxs-lookup"><span data-stu-id="7d517-231">In the **LP** field, enter *LP00201*.</span></span>
1. <span data-ttu-id="7d517-232">Staðfesta númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="7d517-232">Confirm the license plate.</span></span>
1. <span data-ttu-id="7d517-233">Sláðu inn magn af vörunni sem verður bætt við númeraplötuna.</span><span class="sxs-lookup"><span data-stu-id="7d517-233">Enter the item that will be added to the license plate.</span></span> <span data-ttu-id="7d517-234">Í reitinn **ITEM** skal færa inn *M9201*.</span><span class="sxs-lookup"><span data-stu-id="7d517-234">In the **ITEM** field, enter *M9201*.</span></span>
1. <span data-ttu-id="7d517-235">Staðfesta atriði.</span><span class="sxs-lookup"><span data-stu-id="7d517-235">Confirm the item.</span></span>
1. <span data-ttu-id="7d517-236">Sláðu inn magn af vörunni sem verður bætt við.</span><span class="sxs-lookup"><span data-stu-id="7d517-236">Enter the quantity of the item that will be added.</span></span> <span data-ttu-id="7d517-237">Í reitinn **Magn** skaltu slá inn *15*.</span><span class="sxs-lookup"><span data-stu-id="7d517-237">In the **QTY** field, enter *15*.</span></span>
1. <span data-ttu-id="7d517-238">Staðfestu magnið.</span><span class="sxs-lookup"><span data-stu-id="7d517-238">Confirm the quantity.</span></span>

    <span data-ttu-id="7d517-239">Skilaboðin „Vinnu er lokið“ birtast.</span><span class="sxs-lookup"><span data-stu-id="7d517-239">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="7d517-240">Veldu valmyndarhnappinn (stundum kallaður hamborgari eða hamborgarahnappur) og veldu síðan **Hætta við** til að loka verkinu **Leiðréttingar í**.</span><span class="sxs-lookup"><span data-stu-id="7d517-240">Select the Menu button (sometimes referred to as the hamburger or the hamburger button), and then select **Cancel** to exit the **Adjustment in** task.</span></span>

### <a name="consolidate-locations"></a><span data-ttu-id="7d517-241">Sameina staðsetningar</span><span class="sxs-lookup"><span data-stu-id="7d517-241">Consolidate locations</span></span>

1. <span data-ttu-id="7d517-242">Farið í **Vöruhúsakerfi \> Reglubundin verk \> Sameining vöru**.</span><span class="sxs-lookup"><span data-stu-id="7d517-242">Go to **Warehouse management \> Periodic tasks \> Item consolidation**.</span></span>
1. <span data-ttu-id="7d517-243">Í hausnum skal velja vöruhús þar sem gera á sameininguna.</span><span class="sxs-lookup"><span data-stu-id="7d517-243">In the header, select a warehouse to do the consolidation for.</span></span> <span data-ttu-id="7d517-244">Í reitinn **Vöruhús** skal slá inn *51*.</span><span class="sxs-lookup"><span data-stu-id="7d517-244">In the **Warehouse** field, enter *51*.</span></span>

    <span data-ttu-id="7d517-245">Færsla er sýnd fyrir hverja staðsetningu þar sem vara *M9201* var leiðrétt.</span><span class="sxs-lookup"><span data-stu-id="7d517-245">A record is shown for each location where item *M9201* was adjusted.</span></span> <span data-ttu-id="7d517-246">Dálkurinn **Nýtingarprósenta** sýnir rúmmálsnýtingu hverrar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="7d517-246">The **Utilization percentage** column shows the volumetric utilization of each location.</span></span>

1. <span data-ttu-id="7d517-247">Til að sameina birgðir skal velja allar sendingar sem á að sameina og síðan, á aðgerðasvæðinu, velja **Sameina birgðir**.</span><span class="sxs-lookup"><span data-stu-id="7d517-247">To consolidate inventory, select all the locations that must be consolidated, and then, on the Action Pane, select **Consolidate Inventory**.</span></span>
1. <span data-ttu-id="7d517-248">Í svarglugganum **Sameina birgðir** skal tilgreina staðsetninguna og hreyfingargerðina sem nota á til að búa til vinnu fyrir birgðahreyfingu.</span><span class="sxs-lookup"><span data-stu-id="7d517-248">In the **Consolidate inventory** dialog box, specify the location and movement type that should be used to create the work for inventory movement.</span></span> <span data-ttu-id="7d517-249">Stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="7d517-249">Set the following values:</span></span>

    - <span data-ttu-id="7d517-250">**Staðsetning:** *LP-001*</span><span class="sxs-lookup"><span data-stu-id="7d517-250">**Location:** *LP-001*</span></span>
    - <span data-ttu-id="7d517-251">**Kóði hreyfingargerðar:** *SAMEINA*</span><span class="sxs-lookup"><span data-stu-id="7d517-251">**Movement type code:** *CONSOLIDATE*</span></span>

1. <span data-ttu-id="7d517-252">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="7d517-252">Select **OK**.</span></span>
1. <span data-ttu-id="7d517-253">Þú færð upplýsingaboð sem sýna hreyfingarvinnu sem var búin til.</span><span class="sxs-lookup"><span data-stu-id="7d517-253">You receive an informational message that shows the movement work that was created.</span></span> <span data-ttu-id="7d517-254">Skráið niður kenni hreyfingarvinnu.</span><span class="sxs-lookup"><span data-stu-id="7d517-254">Make a note of the movement work ID.</span></span>

### <a name="view-movement-work"></a><span data-ttu-id="7d517-255">Skoða hreyfingarvinnu</span><span class="sxs-lookup"><span data-stu-id="7d517-255">View movement work</span></span>

1. <span data-ttu-id="7d517-256">Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnu**.</span><span class="sxs-lookup"><span data-stu-id="7d517-256">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="7d517-257">Skoða vinnuna sem var búin til.</span><span class="sxs-lookup"><span data-stu-id="7d517-257">View the work that was created.</span></span> <span data-ttu-id="7d517-258">Notið vinnukenni hreyfingar úr birgðasameiningunni til að sía eða leita í hnitaneti vinnu.</span><span class="sxs-lookup"><span data-stu-id="7d517-258">Use the movement work ID from the inventory consolidation to filter or search the work grid.</span></span>

    <span data-ttu-id="7d517-259">Í þessu dæmi var staðsetning sem hafði birgðir notuð sem samstæðustaðsetning birgða.</span><span class="sxs-lookup"><span data-stu-id="7d517-259">In this scenario, an existing location that had inventory was used as the inventory consolidation location.</span></span> <span data-ttu-id="7d517-260">Því er aðeins eitt vinnuauðkennið stofnað.</span><span class="sxs-lookup"><span data-stu-id="7d517-260">Therefore, only one work ID was created.</span></span>

    > [!NOTE]
   > <span data-ttu-id="7d517-261">Kerfið býr til eitt vinnuauðkenni fyrir hvern flutning sem þarf að ljúka.</span><span class="sxs-lookup"><span data-stu-id="7d517-261">The system creates one work ID for each move that must be completed.</span></span> <span data-ttu-id="7d517-262">Ef staðsetning sem inniheldur þegar birgðir er tilgreind er aðeins eitt vinnuauðkennið stofnað.</span><span class="sxs-lookup"><span data-stu-id="7d517-262">If you specify a location that already contains inventory, only one work ID is created.</span></span> <span data-ttu-id="7d517-263">Ef ný staðsetning er tilgreind eru tvö vinnuauðkenni stofnuð.</span><span class="sxs-lookup"><span data-stu-id="7d517-263">If you specify a new location, two work IDs are created.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]