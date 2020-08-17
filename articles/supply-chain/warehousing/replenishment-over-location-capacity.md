---
title: Áfylling yfir staðsetningargetu
description: Í þessu efnisatriði er að finna upplýsingar um eiginleikann fyrir áfyllingu yfir staðsetningargetu. Þessi eiginleiki gerir kleift að búa til alla áfyllingarvinnu sem krafist er fyrir daginn og stjórnar framboði þessarar áfyllingarvinnu til að tryggja að birgðir í tiltektarstaðsetningunni hvorki tæmist né fari yfir getu.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.7
ms.openlocfilehash: 5591af5fce4eb3fc901919b98f654faa5e160c54
ms.sourcegitcommit: 27233e0fda61dac541c5210ca8d94ab4ba74966f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/03/2020
ms.locfileid: "3652240"
---
# <a name="replenishment-over-location-capacity"></a><span data-ttu-id="0bef1-104">Áfylling yfir staðsetningargetu</span><span class="sxs-lookup"><span data-stu-id="0bef1-104">Replenishment over location capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0bef1-105">Sum vöruhús með mikið magn eða takmarkað rými verða að senda meira vörumagn á einu degi en sem kemst fyrir í tiltektarstaðsetningunni.</span><span class="sxs-lookup"><span data-stu-id="0bef1-105">Some high-volume or space-constrained warehouses must ship more quantity of an item in a day than will fit in the picking location.</span></span> <span data-ttu-id="0bef1-106">Eiginleikinn *Áfylling yfir staðsetningargetu* gerir kleift að búa til alla áfyllingarvinnu sem krafist er fyrir daginn og stjórnar framboði þessarar áfyllingarvinnu til að tryggja að birgðir í tiltektarstaðsetningunni hvorki tæmist né fari yfir getu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-106">The *Replenishment over location capacity* feature enables all replenishment work that will be required for the day to be created and manages availability of that replenishment work to ensure that the picking location neither runs out of inventory nor goes above capacity.</span></span>

<span data-ttu-id="0bef1-107">Eiginleikinn gerir klefit að búa til meiri áfyllingarvinnu en staðsetningin ræður við og hann kemur í veg fyrir að áfyllingarvinnu ljúki þegar staðsetningin er full.</span><span class="sxs-lookup"><span data-stu-id="0bef1-107">The feature enables more replenishment work to be created than will fit in a location, and it blocks replenishment work from being completed when the location is full.</span></span> <span data-ttu-id="0bef1-108">Þegar birgðir í tiltektarstaðsetningu fara niður fyrir skilgreind mörk verður boðið upp á meiri áfyllingarvinnu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-108">As inventory in the picking location drops below a configurable threshold, more replenishment work is made available.</span></span>

## <a name="turn-on-the-replenishment-over-location-capacity-feature"></a><span data-ttu-id="0bef1-109">Kveikja á eiginleikanum fyrir áfyllingu yfir staðsetningargetu</span><span class="sxs-lookup"><span data-stu-id="0bef1-109">Turn on the Replenishment over location capacity feature</span></span>

<span data-ttu-id="0bef1-110">Til að gera þennan eiginleika tiltækan skaltu kveikja á eftirfarandi eiginleika í [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (í þessari röð):</span><span class="sxs-lookup"><span data-stu-id="0bef1-110">To make this feature available, turn on the following features in [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) (in this order):</span></span>

1. <span data-ttu-id="0bef1-111">Vinnulokun fyrir allt fyrirtækið</span><span class="sxs-lookup"><span data-stu-id="0bef1-111">Organization-wide work blocking</span></span>
1. <span data-ttu-id="0bef1-112">Áfylling yfir staðsetningargetu</span><span class="sxs-lookup"><span data-stu-id="0bef1-112">Replenishment over location capacity</span></span>

## <a name="set-up-the-feature-for-the-example-scenario"></a><span data-ttu-id="0bef1-113">Setja upp eiginleikann fyrir þetta sýnidæmi</span><span class="sxs-lookup"><span data-stu-id="0bef1-113">Set up the feature for the example scenario</span></span>

<span data-ttu-id="0bef1-114">Í þessum hluta eru leiðbeiningar og dæmi sem sýna hvernig á að setja upp þennan eiginleika og undirbúa sýnigögn fyrir sýnidæmið sem kemur fyrir seinna í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="0bef1-114">This section provides guidelines and an example that shows how to set up this feature and prepare sample data for the example scenario that is provided later in this topic.</span></span>

### <a name="enable-sample-data"></a><span data-ttu-id="0bef1-115">Virkja gögn sýnishorna</span><span class="sxs-lookup"><span data-stu-id="0bef1-115">Enable sample data</span></span>

<span data-ttu-id="0bef1-116">Til að vinna í gegnum [sýniaðstæðurnar](#example-scenario) með því að nota sýnskrárnar og sýnigildin sem eru kynnt í þessu efnisatriði verður þú að vinna á kerfi þar sem venjulegu [sýnigögnin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) eru sett upp.</span><span class="sxs-lookup"><span data-stu-id="0bef1-116">To work through the [example scenario](#example-scenario) by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="0bef1-117">Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.</span><span class="sxs-lookup"><span data-stu-id="0bef1-117">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="location-profile"></a><span data-ttu-id="0bef1-118">Forstillingar staðsetningar</span><span class="sxs-lookup"><span data-stu-id="0bef1-118">Location profile</span></span>

<span data-ttu-id="0bef1-119">Kveikið á virkninni fyrir áfyllingu yfir staðsetningargetu í staðsetningarforstillingunni.</span><span class="sxs-lookup"><span data-stu-id="0bef1-119">Enable the replenish over capacity functionality on the location profile.</span></span>

1. <span data-ttu-id="0bef1-120">Fara í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Forstillingar staðsetningar**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-120">Go to **Warehouse management \> Setup \> Warehouse \> Locations profiles**.</span></span>
1. <span data-ttu-id="0bef1-121">Á svæðinu vinstra megin skal velja **PICK-06**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-121">In the left pane, select **PICK-06**.</span></span>
1. <span data-ttu-id="0bef1-122">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-122">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="0bef1-123">Í flýtiflipanum **Áfylling** skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="0bef1-123">On the **Replenishment** FastTab, set the following values:</span></span>

    - <span data-ttu-id="0bef1-124">**Fara yfir afkastagetu staðsetningar:** *Já*</span><span class="sxs-lookup"><span data-stu-id="0bef1-124">**Exceed Location Capacity:** *Yes*</span></span>

        <span data-ttu-id="0bef1-125">Þegar virkjuð heimilar áfyllingarvinna að farið sé umfram hámarksafköst staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="0bef1-125">When enabled, the maximum capacity of the location will be allowed to be exceeded by replenishment work.</span></span> <span data-ttu-id="0bef1-126">Þetta virkjar einnig aðra reiti í flýtiflipanum **Áfylling**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-126">This also enables other fields on the **Replenishment** FastTab.</span></span>

    - <span data-ttu-id="0bef1-127">**Gerð viðmiðunarmarka fyrir vinnuframboð:** *Magn*</span><span class="sxs-lookup"><span data-stu-id="0bef1-127">**Work availability threshold type:** *Quantity*</span></span>

        <span data-ttu-id="0bef1-128">Þessi reitur skilgreinir aðferðina sem er notuð til að ákvarða hvenær ætti að losa meiri vinnu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-128">This field defines the method that is used to determine when more work should be released.</span></span> <span data-ttu-id="0bef1-129">Hægt er að losa eftir annaðhvort magni eða prósentu:</span><span class="sxs-lookup"><span data-stu-id="0bef1-129">You can release by either quantity or a percentage:</span></span>

        - <span data-ttu-id="0bef1-130">*Prósenta* – Veljið þennan valkost til að nota prósentugetu sem byggir á birgðamörkum eða rúmmáli.</span><span class="sxs-lookup"><span data-stu-id="0bef1-130">*Percent* – Select this option to use percentage capacity that is based on stocking limits or volumetrics.</span></span> <span data-ttu-id="0bef1-131">Ef þessi valkostur er valinn, virkjar það reitinn **Prósenta yfirflæðis** og slekkur á reitunum tveimur sem tengjast magni, **Magn yfirflæðis** og **Eining yfirflæðis**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-131">Selecting this option enables the **Overflow percentage** field, and disables the two quantity related fields,  **Overflow quantity** and **Overflow unit**.</span></span>

            <span data-ttu-id="0bef1-132">Hægt er að nota þennan valkost ef tiltektarstaðsetningarnar nota rúmmál.</span><span class="sxs-lookup"><span data-stu-id="0bef1-132">You can use this option if the picking locations use volumetrics.</span></span>

            <span data-ttu-id="0bef1-133">Ef þessi valkostur er valinn skal stilla reitinn **Prósenta yfirflæðis** á þá prósentu þegar meiri áfyllingarvinna er gerð tiltæk.</span><span class="sxs-lookup"><span data-stu-id="0bef1-133">If this option is selected, set the **Overflow percentage** field to the percentage at which more replenishment work will be made available.</span></span>

        - <span data-ttu-id="0bef1-134">*Magn* – Veljið þennan valkost til að nota tiltekið gildi fyrir magn.</span><span class="sxs-lookup"><span data-stu-id="0bef1-134">*Quantity* – Select this option to use a specific quantity value.</span></span> <span data-ttu-id="0bef1-135">Ef þessi valkostur er valinn slokknar á **Prósenta yfirflæðis** og reitirnir **Magn yfirflæðis** og **Eining yfirflæðis** virkjast.</span><span class="sxs-lookup"><span data-stu-id="0bef1-135">Selecting this option disables the **Overflow percentage** field and enables **Overflow quantity** and **Overflow unit** fields.</span></span>

            <span data-ttu-id="0bef1-136">Notið þennan valkost þegar rúmmál er ekki notað fyrir staðsetningar sem fyllt er á, eða þegar birgðamagnið sem fyllt er á staðsetninguna er stöðugt.</span><span class="sxs-lookup"><span data-stu-id="0bef1-136">Use this option when you aren't using volumetrics for the locations that are being replenished, or when you have consistent quantities at which you want more inventory to be brought to the location.</span></span>

           <span data-ttu-id="0bef1-137">Ef þessi valkostur er valinn skal stilla magn reitina **Magn yfirflæðis** og **Eining yfirflæðis** á magnið og eininguna þegar meiri áfyllingarvinna er gerð tiltæk.</span><span class="sxs-lookup"><span data-stu-id="0bef1-137">If this option is selected, set the **Overflow quantity** and **Overflow unit** fields to the quantity and unit at which more replenishment work will be made available.</span></span>

    - <span data-ttu-id="0bef1-138">**Magn yfirflæðis:** *0,65*</span><span class="sxs-lookup"><span data-stu-id="0bef1-138">**Overflow quantity:** *0.65*</span></span>

        <span data-ttu-id="0bef1-139">Þessi reitur skilgreinir magnið þegar verður yfirflæði á staðsetningunni.</span><span class="sxs-lookup"><span data-stu-id="0bef1-139">This field defines the quantity at which the location overflows.</span></span>

        <span data-ttu-id="0bef1-140">Vinna verður alltaf tiltæk þegar samanlagt magn af lagerbirgðum á staðsetningunni og vinnumagni er undir þessu gildi.</span><span class="sxs-lookup"><span data-stu-id="0bef1-140">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this value.</span></span> <span data-ttu-id="0bef1-141">Öll áfyllingarvinna fyrir ofan þetta gildi verður lokað fyrir og verður að opna fyrir hana handvirkt.</span><span class="sxs-lookup"><span data-stu-id="0bef1-141">Any replenishment work above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="0bef1-142">Birgðamörk staðsetningar eru tekin til greina þegar vinnumagnið er reiknað.</span><span class="sxs-lookup"><span data-stu-id="0bef1-142">Location stocking limits are considered when the work quantity is calculated.</span></span>

    - <span data-ttu-id="0bef1-143">**Eining yfirflæðis:** *PL*</span><span class="sxs-lookup"><span data-stu-id="0bef1-143">**Overflow unit:** *PL*</span></span>

        <span data-ttu-id="0bef1-144">Þessi reitur skilgreinir eininguna sem tengist magni yfirflæðis.</span><span class="sxs-lookup"><span data-stu-id="0bef1-144">This field defines the unit that is associated with the overflow quantity.</span></span>

        <span data-ttu-id="0bef1-145">Í þessu tilfelli verður frekari áfyllingarvinna tiltæk þegar staðsetningin fer niður fyrir 0,65 bretti (PL).</span><span class="sxs-lookup"><span data-stu-id="0bef1-145">In this case, more replenishment work will be made available when the location gets down to 0.65 pallet (PL).</span></span>

    - <span data-ttu-id="0bef1-146">**Hlutfall yfirflæðis**</span><span class="sxs-lookup"><span data-stu-id="0bef1-146">**Overflow percentage**</span></span>

        <span data-ttu-id="0bef1-147">Þessi reitur skilgreinir hlutfallið þegar verður yfirflæði á staðsetningunni.</span><span class="sxs-lookup"><span data-stu-id="0bef1-147">This field defines the percentage at which the location overflows.</span></span>

        <span data-ttu-id="0bef1-148">Vinna verður alltaf tiltæk þegar samanlagt magn af lagerbirgðum á staðsetningunni og vinnumagni er undir þessu hlutfalli.</span><span class="sxs-lookup"><span data-stu-id="0bef1-148">Work will be available whenever the sum of the on-hand quantity in the location and the work quantity is below this percentage.</span></span> <span data-ttu-id="0bef1-149">Öll áfyllingarvinna fyrir ofan þetta hlutfall verður lokað fyrir og verður að opna fyrir hana handvirkt.</span><span class="sxs-lookup"><span data-stu-id="0bef1-149">Any replenishment work quantity percentage above this value will be blocked and must be manually unblocked.</span></span>

        <span data-ttu-id="0bef1-150">Birgðamörk staðsetningar eru tekin til greina þegar hlutfall vinnumagnsins er reiknað.</span><span class="sxs-lookup"><span data-stu-id="0bef1-150">Location stocking limits are considered when the work quantity percentage is calculated.</span></span> <span data-ttu-id="0bef1-151">Ef engin birgðamörk staðsetningar eru skilgreind, verður hlutfall vinnumagns reiknað eftir rúmmáli ef takmarkanir rúmmáls eru skilgreindar fyrir staðsetningarforstillinguna.</span><span class="sxs-lookup"><span data-stu-id="0bef1-151">If no location stocking limits are defined, the work quantity percentage is calculated by volume if volume constraints are defined for the location profile.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0bef1-152">Ef sýnigögnin eru notuð fyrir lögaðilann **USMF** og búið er að kveikja á eiginleikanum *Númeraplötustaða staðsetningar*, þarf að slökkva á stillingunni **Virkja staðsetningu númeraplötu** fyrir staðsetningarforstillinguna **BUK-06** til að ljúka skrefum fartækis í þessu sýnidæmi.</span><span class="sxs-lookup"><span data-stu-id="0bef1-152">If you're using the demo data for the **USMF** legal entity and previously turned on the *Location license plate positioning* feature, you must turn off the **Enable license plate positioning** setting for the **BULK-06** location profile to complete the mobile steps in the example scenario.</span></span>

### <a name="wave-step-code"></a><span data-ttu-id="0bef1-153">Kóði bylgjuskrefs</span><span class="sxs-lookup"><span data-stu-id="0bef1-153">Wave step code</span></span>

> [!NOTE]
> <span data-ttu-id="0bef1-154">Til að setja upp bylgjuskrefskóða eins og lýst er gæti fyrst þurft að nota [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á eiginleikanum sem kallast *Kóði bylgjuskrefs fyrir allt fyrirtækið*.</span><span class="sxs-lookup"><span data-stu-id="0bef1-154">To set up a wave step code as described here, you might first have to use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named *Organization wide wave step code*.</span></span>

1. <span data-ttu-id="0bef1-155">Fara í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjuskrefakóðar**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-155">Go to **Warehouse Management \> Setup \> Waves \> Wave step codes**.</span></span>
1. <span data-ttu-id="0bef1-156">Veljið **Nýtt** og stillið eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="0bef1-156">Select **New**, and set the following values:</span></span>

    - <span data-ttu-id="0bef1-157">**Kóði bylgjuskrefs:** *Áfyll*</span><span class="sxs-lookup"><span data-stu-id="0bef1-157">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="0bef1-158">**Lýsing á bylgjuskrefi:** *Áfylling*</span><span class="sxs-lookup"><span data-stu-id="0bef1-158">**Wave step description:** *Replenishment*</span></span>
    - <span data-ttu-id="0bef1-159">**Gerð bylgjuskrefs:** *Áfylling*</span><span class="sxs-lookup"><span data-stu-id="0bef1-159">**Wave step type:** *Replenishment*</span></span>

1. <span data-ttu-id="0bef1-160">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-160">Select **Save**.</span></span>

### <a name="replenishment-template"></a><span data-ttu-id="0bef1-161">Sniðmát áfyllingar</span><span class="sxs-lookup"><span data-stu-id="0bef1-161">Replenishment template</span></span>

<span data-ttu-id="0bef1-162">Áfyllingarsniðmát er safn af reglum sem stjórna því hvenær og hvernig fyllt er á staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-162">Replenishment templates are a set of rules that control when and how a location is replenished.</span></span>

1. <span data-ttu-id="0bef1-163">Fara í **Vöruhúsakerfi \> Uppsetningu \> Áfylling \> Áfyllingarsniðmát**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-163">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**.</span></span>
1. <span data-ttu-id="0bef1-164">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-164">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="0bef1-165">Í hlutanum **Yfirlit** skal velja línuna þar sem reiturinn **Áfyllingarsniðmát** er stilltur á *Áfylling samkvæmt eftirspurn*.</span><span class="sxs-lookup"><span data-stu-id="0bef1-165">In the **Overview** section, select the line where the **Replenish template** field is set to *Demand replenish*.</span></span>
1. <span data-ttu-id="0bef1-166">Stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="0bef1-166">Set the following values:</span></span>

    - <span data-ttu-id="0bef1-167">**Kóði bylgjuskrefs:** *Áfyll*</span><span class="sxs-lookup"><span data-stu-id="0bef1-167">**Wave step code:** *Replen*</span></span>
    - <span data-ttu-id="0bef1-168">**Leyfa bylgjueftirspurn að nota magn sem ekki er frátekið:** *Já*</span><span class="sxs-lookup"><span data-stu-id="0bef1-168">**Allow wave demand to use unreserved quantities:** *Yes*</span></span>

1. <span data-ttu-id="0bef1-169">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-169">Select **Save**.</span></span>

### <a name="wave-template"></a><span data-ttu-id="0bef1-170">Bylgjusniðmát</span><span class="sxs-lookup"><span data-stu-id="0bef1-170">Wave template</span></span>

1. <span data-ttu-id="0bef1-171">Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-171">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="0bef1-172">Á svæðinu vinstra megin skal stilla reitinn **Gerð bylgjusniðmáts** á *Sending*.</span><span class="sxs-lookup"><span data-stu-id="0bef1-172">In the left pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="0bef1-173">Veljið sniðmát **61 Sending** í listanum.</span><span class="sxs-lookup"><span data-stu-id="0bef1-173">Select template **61 Shipping** in the list.</span></span>
1. <span data-ttu-id="0bef1-174">Á aðgerðarúðunni skal velja **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-174">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="0bef1-175">Í flýtiflipanum **Almennt** skal stilla valkostinn **Gera losun áfyllingarvinnu sjálfvirka** á *Já*.</span><span class="sxs-lookup"><span data-stu-id="0bef1-175">On the **General** FastTab, set the **Automate replenishment work release** option to *Yes*.</span></span>

    <span data-ttu-id="0bef1-176">Stillið þennan valkost á *Já* til að stofna áfyllingarvinnu byggða á eftirspurn og losa hana sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="0bef1-176">Set this option to *Yes* to create demand-based replenishment work and release it automatically.</span></span> <span data-ttu-id="0bef1-177">Verður að bæta bylgjuaðferð áfyllingar við bylgjusniðmátið og stofna áfyllingarsniðmát af gerðinni **Bylgjueftirspurn**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-177">You must add the replenishment wave method to the wave template and create a replenishment template of the **Wave demand** type.</span></span> <span data-ttu-id="0bef1-178">Setjið upp áfyllingarsniðmát á síðunni **Áfyllingarsniðmát**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-178">Set up a replenishment template on the **Replenishment templates** page.</span></span> <span data-ttu-id="0bef1-179">Til að setja upp áfyllingarsniðmát þarf að bæta áfyllingaraðferðinni við bylgjusniðmátið.</span><span class="sxs-lookup"><span data-stu-id="0bef1-179">To set up a replenishment template, you must add the replenish method to the wave template.</span></span>

1. <span data-ttu-id="0bef1-180">Í flýtiflipanum **Aðferðir**, í dálknum **Valdar aðferðir**, skal finna eftirfarandi línu:</span><span class="sxs-lookup"><span data-stu-id="0bef1-180">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="0bef1-181">**Heiti aðferðar:** *fylla á*</span><span class="sxs-lookup"><span data-stu-id="0bef1-181">**Method name:** *replenish*</span></span>
    - <span data-ttu-id="0bef1-182">**Heiti:** *Áfylling*</span><span class="sxs-lookup"><span data-stu-id="0bef1-182">**Name:** *Replenishment*</span></span>

1. <span data-ttu-id="0bef1-183">Stillið reitinn **Kóði bylgjuskrefs** fyrir þessa línu á *Áfyll*.</span><span class="sxs-lookup"><span data-stu-id="0bef1-183">Set the **Wave step code** field for this line to *Replen*.</span></span>
1. <span data-ttu-id="0bef1-184">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-184">Select **Save**.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="0bef1-185">Dæmi</span><span class="sxs-lookup"><span data-stu-id="0bef1-185">Example scenario</span></span>

<span data-ttu-id="0bef1-186">Þegar búið er að gera öll sýnigögnin hér á undan tiltæk og setja þau upp, er hægt að fara í gegnum þetta sýnidæmi til að prófa eiginleikann *Áfylling yfir staðsetningargetu*.</span><span class="sxs-lookup"><span data-stu-id="0bef1-186">After you've made all the previously described sample data available and set it up, you can work through this scenario to try out the *Replenishment over location capacity* feature.</span></span> <span data-ttu-id="0bef1-187">Gildin sem eru sýnd í þessu sýnidæmi gera ráð fyrir því að verið sé að vinna með stöðluð sýnigögn, að lögaðilinn **USMF** hafi verið valinn og að sýniskrárnar sem lýst var fyrr í þessu efnisatriði hafi verið undirbúnar.</span><span class="sxs-lookup"><span data-stu-id="0bef1-187">The values that are shown in this scenario assume that you're working with the standard demo data, that you selected the **USMF** legal entity, and that you prepared the sample records that are described earlier in this topic.</span></span> <span data-ttu-id="0bef1-188">Þetta sýnidæmi er einnig dæmi um hvernig hægt er að nota eiginleikann í framleiðsluumhverfi.</span><span class="sxs-lookup"><span data-stu-id="0bef1-188">This scenario also serves as an example that shows how the feature can be used in a production setting.</span></span>

### <a name="create-replenishment-work"></a><span data-ttu-id="0bef1-189">Stofna áfyllingarvinnu</span><span class="sxs-lookup"><span data-stu-id="0bef1-189">Create replenishment work</span></span>

#### <a name="create-sales-order-1"></a><span data-ttu-id="0bef1-190">Stofna sölupöntun 1</span><span class="sxs-lookup"><span data-stu-id="0bef1-190">Create sales order 1</span></span>

1. <span data-ttu-id="0bef1-191">Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-191">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="0bef1-192">Á aðgerðasvæðinu skal velja **Ný** til að opna svarglugga til að stofna nýja sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="0bef1-192">On the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="0bef1-193">Í svarglugganum skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="0bef1-193">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="0bef1-194">**Viðskiptavinalykill:** *US-007*</span><span class="sxs-lookup"><span data-stu-id="0bef1-194">**Customer account:** *US-007*</span></span>
    - <span data-ttu-id="0bef1-195">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="0bef1-195">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="0bef1-196">Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="0bef1-196">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="0bef1-197">Ný sölupöntun opnast.</span><span class="sxs-lookup"><span data-stu-id="0bef1-197">The new sales order is opened.</span></span> <span data-ttu-id="0bef1-198">Hún inniheldur nýja, auða línu í flýtiflipanum **Sölupöntunarlína**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-198">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="0bef1-199">Stilltu eftirfarandi gildi á þessari línu:</span><span class="sxs-lookup"><span data-stu-id="0bef1-199">On this line, set the following values:</span></span>

    - <span data-ttu-id="0bef1-200">**Vörunúmer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="0bef1-200">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="0bef1-201">**Magn:** *40*</span><span class="sxs-lookup"><span data-stu-id="0bef1-201">**Quantity:** *40*</span></span>

1. <span data-ttu-id="0bef1-202">Í flýtiflipanum **Sölupöntunarlínur** skal velja **Birgðir \> Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-202">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="0bef1-203">Á síðunni **Frátekning** skal velja **Frátektarlota**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-203">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="0bef1-204">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0bef1-204">Close the page.</span></span>
1. <span data-ttu-id="0bef1-205">Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-205">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="0bef1-206">Upplýsingaboð birtast sem sýna auðkenni bylgju og sendingar sem voru búin til.</span><span class="sxs-lookup"><span data-stu-id="0bef1-206">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="0bef1-207">Áfyllingarbylgja er einnig stofnuð.</span><span class="sxs-lookup"><span data-stu-id="0bef1-207">A replenishment wave is also created.</span></span>

    <span data-ttu-id="0bef1-208">Einnig birtast viðvörunarboð sem segja: „Vinnukenni XXXX er ekki hægt að útiloka því að það er með ókláraða áfyllingarvinnu.“</span><span class="sxs-lookup"><span data-stu-id="0bef1-208">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-2"></a><span data-ttu-id="0bef1-209">Stofna sölupöntun 2</span><span class="sxs-lookup"><span data-stu-id="0bef1-209">Create sales order 2</span></span>

1. <span data-ttu-id="0bef1-210">Á síðunni **Allar sölupantanir**, á aðgerðasvæði, skal velja **Ný** til að opna svarglugga til að stofna nýja sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="0bef1-210">On the **All sales orders**, page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="0bef1-211">Í svarglugganum skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="0bef1-211">In the dialog box, set the following value:</span></span>

    - <span data-ttu-id="0bef1-212">**Viðskiptavinalykill:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="0bef1-212">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="0bef1-213">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="0bef1-213">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="0bef1-214">Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="0bef1-214">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="0bef1-215">Ný sölupöntun opnast.</span><span class="sxs-lookup"><span data-stu-id="0bef1-215">The new sales order is opened.</span></span> <span data-ttu-id="0bef1-216">Hún inniheldur nýja, auða línu í flýtiflipanum **Sölupöntunarlína**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-216">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="0bef1-217">Stilltu eftirfarandi gildi á þessari línu:</span><span class="sxs-lookup"><span data-stu-id="0bef1-217">On this line, set the following values:</span></span>

    - <span data-ttu-id="0bef1-218">**Vörunúmer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="0bef1-218">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="0bef1-219">**Magn:** *60*</span><span class="sxs-lookup"><span data-stu-id="0bef1-219">**Quantity:** *60*</span></span>

1. <span data-ttu-id="0bef1-220">Í flýtiflipanum **Sölupöntunarlínur** skal velja **Birgðir \> Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-220">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="0bef1-221">Á síðunni **Frátekning** skal velja **Frátektarlota**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-221">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="0bef1-222">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0bef1-222">Close the page.</span></span>
1. <span data-ttu-id="0bef1-223">Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-223">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="0bef1-224">Upplýsingaboð birtast sem sýna auðkenni bylgju og sendingar sem voru búin til.</span><span class="sxs-lookup"><span data-stu-id="0bef1-224">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="0bef1-225">Áfyllingarbylgja er einnig stofnuð.</span><span class="sxs-lookup"><span data-stu-id="0bef1-225">A replenishment wave is also created.</span></span>

    <span data-ttu-id="0bef1-226">Einnig birtast viðvörunarboð sem segja: „Vinnukenni XXXX er ekki hægt að útiloka því að það er með ókláraða áfyllingarvinnu.“</span><span class="sxs-lookup"><span data-stu-id="0bef1-226">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="create-sales-order-3"></a><span data-ttu-id="0bef1-227">Stofna sölupöntun 3</span><span class="sxs-lookup"><span data-stu-id="0bef1-227">Create sales order 3</span></span>

1. <span data-ttu-id="0bef1-228">Á síðunni **Allar sölupantanir**, á aðgerðasvæði, skal velja **Ný** til að opna svarglugga til að stofna nýja sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="0bef1-228">On the **All sales orders** page, on the Action Pane, select **New** to open a dialog box for creating a new sales order.</span></span>
1. <span data-ttu-id="0bef1-229">Í svarglugganum skal stilla eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="0bef1-229">In the dialog box, set the following values:</span></span>

    - <span data-ttu-id="0bef1-230">**Viðskiptavinalykill:** *US-004*</span><span class="sxs-lookup"><span data-stu-id="0bef1-230">**Customer account:** *US-004*</span></span>
    - <span data-ttu-id="0bef1-231">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="0bef1-231">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="0bef1-232">Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="0bef1-232">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="0bef1-233">Ný sölupöntun opnast.</span><span class="sxs-lookup"><span data-stu-id="0bef1-233">The new sales order is opened.</span></span> <span data-ttu-id="0bef1-234">Hún inniheldur nýja, auða línu í flýtiflipanum **Sölupöntunarlína**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-234">It includes a new, empty line on the **Sales order lines** FastTab.</span></span> <span data-ttu-id="0bef1-235">Stilltu eftirfarandi gildi á þessari línu:</span><span class="sxs-lookup"><span data-stu-id="0bef1-235">On this line, set the following values:</span></span>

    - <span data-ttu-id="0bef1-236">**Vörunúmer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="0bef1-236">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="0bef1-237">**Magn:** *30*</span><span class="sxs-lookup"><span data-stu-id="0bef1-237">**Quantity:** *30*</span></span>

1. <span data-ttu-id="0bef1-238">Í flýtiflipanum **Sölupöntunarlínur** skal velja **Birgðir \> Frátekning**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-238">On the **Sales order lines** FastTab, select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="0bef1-239">Á síðunni **Frátekning** skal velja **Frátektarlota**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-239">On the **Reservation** page, select **Reserve lot**.</span></span>
1. <span data-ttu-id="0bef1-240">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0bef1-240">Close the page.</span></span>
1. <span data-ttu-id="0bef1-241">Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-241">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="0bef1-242">Upplýsingaboð birtast sem sýna auðkenni bylgju og sendingar sem voru búin til.</span><span class="sxs-lookup"><span data-stu-id="0bef1-242">You receive informational messages that show the wave and shipment IDs that were created.</span></span> <span data-ttu-id="0bef1-243">Áfyllingarbylgja er einnig stofnuð.</span><span class="sxs-lookup"><span data-stu-id="0bef1-243">A replenishment wave is also created.</span></span>

    <span data-ttu-id="0bef1-244">Einnig birtast viðvörunarboð sem segja: „Vinnukenni XXXX er ekki hægt að útiloka því að það er með ókláraða áfyllingarvinnu.“</span><span class="sxs-lookup"><span data-stu-id="0bef1-244">You also receive a warning message that states, "Work ID XXXX cannot be unblocked because it has unfinished replenishment work."</span></span>

#### <a name="view-work-details"></a><span data-ttu-id="0bef1-245">Skoða vinnuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="0bef1-245">View work details</span></span>

1. <span data-ttu-id="0bef1-246">Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnu**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-246">Go to **Warehouse management \> Work \> Work details**.</span></span>
1. <span data-ttu-id="0bef1-247">Í hlutanum **Yfirlit** skal sía dálkinn **Vöruhús** fyrir vöruhús *61*.</span><span class="sxs-lookup"><span data-stu-id="0bef1-247">In the **Overview** section, filter the **Warehouse** column for warehouse *61*.</span></span>
1. <span data-ttu-id="0bef1-248">Þá ætti að sjást að sjö vinnukenni hafa verið búin til fyrir þrjár sölupantanir eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="0bef1-248">You should see that seven work IDs were created for the three demand sales orders.</span></span>

    - <span data-ttu-id="0bef1-249">Þrjú af þessum sjö vinnukennum eru með gildi **Gerð verkbeiðni** sem *Áfylling* og fjögur þeirra eru með gildi **Gerð verkbeiðni** sem *Sölupantanir*.</span><span class="sxs-lookup"><span data-stu-id="0bef1-249">Three of the seven work IDs have a **Work order type** value of *Replenishment*, and four have a **Work order type** value of *Sales orders*.</span></span>
    - <span data-ttu-id="0bef1-250">Öll þrjú vinnukennin sem eru með gildi **Gerð verkbeiðni** sem *Áfylling* eru með sömu staðsetningar fyrir *Tiltekt* og *Frágang* í hlutanum **Línur**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-250">All three work IDs that have a **Work order type** value of *Replenishment* have the same *Pick* and *Put* locations in the **Lines** section:</span></span>

        - <span data-ttu-id="0bef1-251">**Tiltekt:** *02A01R5S1B*</span><span class="sxs-lookup"><span data-stu-id="0bef1-251">**Pick:** *02A01R5S1B*</span></span>
        - <span data-ttu-id="0bef1-252">**Frágangur:** *06A01R2S1B*</span><span class="sxs-lookup"><span data-stu-id="0bef1-252">**Put:** *06A01R2S1B*</span></span>

    - <span data-ttu-id="0bef1-253">Tvö vinnukenni voru stofnuð fyrir sölupöntun 1.</span><span class="sxs-lookup"><span data-stu-id="0bef1-253">Two work IDs were created for sales order 1.</span></span>

1. <span data-ttu-id="0bef1-254">Skráið niður vinnukennin fyrir sölupantanirnar.</span><span class="sxs-lookup"><span data-stu-id="0bef1-254">Make a note of the work IDs for the sales orders.</span></span>

<span data-ttu-id="0bef1-255">Það fer eftir magni á lager, en það getur verið örlítill munur á vinnumagninu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-255">Depending on your on-hand quantities, the work quantities that are created might vary slightly.</span></span> <span data-ttu-id="0bef1-256">Hins vegar ættu vinnuhausarnir sem stofnaðir eru að samsvara þessu sýnidæmi.</span><span class="sxs-lookup"><span data-stu-id="0bef1-256">However, overall, the work headers that are created should match this scenario example.</span></span>

#### <a name="on-hand-inventory-license-plate-id"></a><span data-ttu-id="0bef1-257">Númeraplötukenni lagerbirgða</span><span class="sxs-lookup"><span data-stu-id="0bef1-257">On-hand inventory license plate ID</span></span>

<span data-ttu-id="0bef1-258">Síðar í þessu dæmi verður vöruhúsaforritið notað (eða hermiforrit), þar sem þarf að bera kennsl á númeraplötuna til að ljúka sýnidæmunum fyrir tiltekt og áfyllingu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-258">Later in this scenario, you will use the warehouse app (or an emulator), where you must identify the license plate to complete the picking and replenishment scenarios.</span></span>

<span data-ttu-id="0bef1-259">Til að finna númeraplötukennin sem þarf að nota seinna meir, skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="0bef1-259">To find the license plate IDs that you will need later, follow these steps.</span></span>

1. <span data-ttu-id="0bef1-260">Farið í **Birgðastjórnun \> Fyrirspurnir og skýrslur \> Lagerlisti**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-260">Go to **Inventory management \> Inquiries and reports \> On-hand list**.</span></span>
1. <span data-ttu-id="0bef1-261">Veljið hnappinn **Sýna síur** til að opna síusvæðið.</span><span class="sxs-lookup"><span data-stu-id="0bef1-261">Select the **Show filters** button to open the filter pane.</span></span>
1. <span data-ttu-id="0bef1-262">Sláið inn eftirfarandi síuskilyrði til að sækja númeraplöturnar fyrir dæmið.</span><span class="sxs-lookup"><span data-stu-id="0bef1-262">Enter the following filtering criteria to get the license plates for the scenario.</span></span> <span data-ttu-id="0bef1-263">Notið síuna *hefst á*.</span><span class="sxs-lookup"><span data-stu-id="0bef1-263">Use the *begins with* filter.</span></span>

    - <span data-ttu-id="0bef1-264">**Vörunúmer:** *T0100*</span><span class="sxs-lookup"><span data-stu-id="0bef1-264">**Item number:** *T0100*</span></span>
    - <span data-ttu-id="0bef1-265">**Vöruhús:** *61*</span><span class="sxs-lookup"><span data-stu-id="0bef1-265">**Warehouse:** *61*</span></span>

1. <span data-ttu-id="0bef1-266">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-266">Select **Apply**.</span></span>
1. <span data-ttu-id="0bef1-267">Á aðgerðasvæðinu skal velja **Víddir**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-267">On the Action Pane, select **Dimensions**.</span></span>
1. <span data-ttu-id="0bef1-268">Í svarglugganum **Birting vídda**, í hlutanum **Geymsluvíddir**, skal velja öll gildin.</span><span class="sxs-lookup"><span data-stu-id="0bef1-268">In the **Dimensions display** dialog box, in the **Storage Dimensions** section, select all the values.</span></span>
1. <span data-ttu-id="0bef1-269">Í hlutanum **Færslur** skal velja **Vörunúmer** og **Magn \<\> 0**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-269">In the **Transactions** section, select **Item number** and **Quantity \<\> 0**.</span></span>
1. <span data-ttu-id="0bef1-270">Þegar þessu er lokið skal velja **Í lagi** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="0bef1-270">When you've finished, select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="0bef1-271">Hnitanetið **Á lager** sýnir númeraplötunúmerin fyrir vöru *T0100* í hverri staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-271">The **On-hand** grid shows the license plate numbers for item *T0100* in each location.</span></span> <span data-ttu-id="0bef1-272">Skráið niður númeraplötuna sem er á hverri staðsetningu, því að nota þarf upplýsingarnar síðar.</span><span class="sxs-lookup"><span data-stu-id="0bef1-272">Make a note of the license plate that is in each location, because you will need this information later.</span></span>
1. <span data-ttu-id="0bef1-273">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0bef1-273">Close the page.</span></span>

### <a name="process-steps"></a><span data-ttu-id="0bef1-274">Ferlisskref</span><span class="sxs-lookup"><span data-stu-id="0bef1-274">Process steps</span></span>

<span data-ttu-id="0bef1-275">Áfylling á staðsetningu vöruhúss verður framkvæmd fyrir fyrstu tvö vinnukennin.</span><span class="sxs-lookup"><span data-stu-id="0bef1-275">You will perform the warehouse location replenishment for the first two work IDs.</span></span> <span data-ttu-id="0bef1-276">Lokað verður fyrir vinnu á þriðju áfyllingarvinnunni þar til birgðastaða tiltektarstaðsetningarinnar fer undir mörkin.</span><span class="sxs-lookup"><span data-stu-id="0bef1-276">Work on the third replenishment work will be blocked until the inventory level in the picking location falls below the threshold.</span></span>

#### <a name="replenishment"></a><span data-ttu-id="0bef1-277">Áfylling</span><span class="sxs-lookup"><span data-stu-id="0bef1-277">Replenishment</span></span>

1. <span data-ttu-id="0bef1-278">Skráðu þig inn í vöruhúsaforritið sem notandi í vöruhúsi *61*.</span><span class="sxs-lookup"><span data-stu-id="0bef1-278">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="0bef1-279">(Sláið inn *61* sem notandakennið og *1* sem aðgangsorðið.)</span><span class="sxs-lookup"><span data-stu-id="0bef1-279">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="0bef1-280">Farið í **Birgðir \> Áfylling**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-280">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="0bef1-281">Beðið er um að ljúka fyrstu áfyllingarvinnunni.</span><span class="sxs-lookup"><span data-stu-id="0bef1-281">You're prompted to complete the first replenishment work.</span></span> <span data-ttu-id="0bef1-282">Vörunúmerið, magnið og staðsetningin fyrir tiltektina er sýnt.</span><span class="sxs-lookup"><span data-stu-id="0bef1-282">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="0bef1-283">Í reitinn **NP** skal færa númeraplötunúmerið fyrir vöruna í staðsetningunni sem er sýnd.</span><span class="sxs-lookup"><span data-stu-id="0bef1-283">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="0bef1-284">Velja skal hnappinn **Í lagi** (gátmerkistákn).</span><span class="sxs-lookup"><span data-stu-id="0bef1-284">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="0bef1-285">Kerfið býr til númer marknúmeraplötu fyrir nýju númeraplötuna fyrir tínda vöru.</span><span class="sxs-lookup"><span data-stu-id="0bef1-285">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="0bef1-286">Veljið **Í lagi** til að staðfesta gildið.</span><span class="sxs-lookup"><span data-stu-id="0bef1-286">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="0bef1-287">Frágangsvinna er sýnd sem segir notandanum að setja marknúmeraplötuna á áfyllingarstaðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="0bef1-287">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="0bef1-288">Staðsetning *Frágangs* á að vera **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-288">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="0bef1-289">Staðfestið upplýsingar um frágang og veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-289">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="0bef1-290">Skilaboðin „Vinnu er lokið“ birtast og upplýsingar um næsta tiltektarverk áfyllingar eru sýndar: vörunúmerið, magnið og staðsetningin sem tína á úr.</span><span class="sxs-lookup"><span data-stu-id="0bef1-290">You receive a "Work Completed" message, and the details of the next replenishment pick task are shown: the item number, quantity, and location to pick from.</span></span> <span data-ttu-id="0bef1-291">Tiltektarstaðsetningin verður sú sama og fyrsta áfyllingarstaðsetningin.</span><span class="sxs-lookup"><span data-stu-id="0bef1-291">The picking location will be the same as the first replenishment location.</span></span> <span data-ttu-id="0bef1-292">Þess vegna verður númeraplatan með sama númeraplötukennið og var notað fyrir verk fyrstu áfyllingarvinnunnar.</span><span class="sxs-lookup"><span data-stu-id="0bef1-292">Therefore, the license plate will have the same license plate ID that was used for the first replenishment work task.</span></span>

1. <span data-ttu-id="0bef1-293">Endurtakið fyrri skref til að ljúka áfyllingarvinnu fyrir næsta vinnuverk.</span><span class="sxs-lookup"><span data-stu-id="0bef1-293">Repeat the preceding steps to complete the replenishment work for the second work task.</span></span> <span data-ttu-id="0bef1-294">Magn og marknúmeraplata verða frábrugðin magni og marknúmeraplötu fyrir fyrsta vinnuverkið.</span><span class="sxs-lookup"><span data-stu-id="0bef1-294">The quantity and target license plate will differ from the quantity and target license plate for the first work task.</span></span>

<span data-ttu-id="0bef1-295">Þegar næstu áfyllingarvinnu lýkur birtast skilaboðin „Vinnu er lokið“.</span><span class="sxs-lookup"><span data-stu-id="0bef1-295">After the second replenishment work is completed, you receive a "Work Completed" message.</span></span> <span data-ttu-id="0bef1-296">Fartækið upplýsir einnig að engin vinna er í boði, jafnvel þótt einhver áfyllingarvinna sé eftir.</span><span class="sxs-lookup"><span data-stu-id="0bef1-296">The mobile device also informs you that there is no work available, even though some replenishment work remains.</span></span> <span data-ttu-id="0bef1-297">Þessi hegðun gerist vegna þess að áfyllingarvinnan er með stöðuna *Í bið* og er þar af leiðandi merkt sem **Lokað fyrir**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-297">This behavior occurs because the replenishment work has an availability status of *Held* and is therefore marked as **Blocked**.</span></span>

<span data-ttu-id="0bef1-298">Staðan *Í bið* var ræst vegna þess að staðsetningarforstillingin fyrir tiltektarstaðsetninguna sem vinnunni er úthlutað á er með gildi á **Magn yfirflæðis** sem *0,65 PL*.</span><span class="sxs-lookup"><span data-stu-id="0bef1-298">The *Held* status was triggered because the location profile for the picking location that the work is being assigned to has an **Overflow quantity** value of *0.65 PL*.</span></span> <span data-ttu-id="0bef1-299">Tvö fyrri áfyllingarverkin fylltu staðsetninguna næstum upp að mörkum yfirflæðis fyrir vöru *T0100*.</span><span class="sxs-lookup"><span data-stu-id="0bef1-299">The two previous replenishment work tasks filled the location almost to its overflow limit for item *T0100*.</span></span> <span data-ttu-id="0bef1-300">(Umreikningur einingar fyrir vöruna er *1 PL = 100 ea*.) Eftirstandandi áfyllingarvinna myndir þar af leiðandi leiða til þess að staðsetningin færi yfir mörk yfirflæðis.</span><span class="sxs-lookup"><span data-stu-id="0bef1-300">(The unit conversion for the item is *1 PL = 100 ea*.) Therefore, the remaining replenishment work would cause the location to exceed its overflow limit.</span></span>

<span data-ttu-id="0bef1-301">Þar til nægar birgðir eru tíndar úr staðsetningunni til að koma henni undir mörk losunarvinnu í valmyndaratriði fartækis, verður áfram lokað fyrir þessa áfyllingarvinnu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-301">Until enough inventory is picked from the location to bring it below the work release threshold on the mobile device menu item, this replenishment work will remain blocked.</span></span>

#### <a name="sales-order-pick"></a><span data-ttu-id="0bef1-302">Tiltekt sölupöntunar</span><span class="sxs-lookup"><span data-stu-id="0bef1-302">Sales order pick</span></span>

<span data-ttu-id="0bef1-303">Áður en hægt er að ljúka við eftirstandandi áfyllingarvinnu verða birgðir tiltektarstaðsetningarinnar að minnka niður í það sem þarf til að opnað fyrir eftirstandandi áfyllingarvinnu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-303">Before the remaining replenishment work task can be completed, the picking location must be depleted of inventory to a level where the remaining replenishment work can be unblocked.</span></span> <span data-ttu-id="0bef1-304">Með öðrum orðum, samanlagt magn lagerbirgða í staðsetningunni og áfyllingarmagn má ekki fara yfir gildið **Magn yfirflæðis**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-304">In other words, the sum of the quantity of on-hand inventory in the location and the replenishment quantity can't exceed the **Overflow quantity** value.</span></span> <span data-ttu-id="0bef1-305">Þegar þetta samanlagða magn er minna en magn yfirflæðis, verður opnað fyrir eftirstandandi áfyllingarvinnu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-305">When this sum is less than the overflow quantity, the remaining replenishment work will be unblocked.</span></span>

1. <span data-ttu-id="0bef1-306">Skráðu þig inn í vöruhúsaforritið sem notandi í vöruhúsi *61*.</span><span class="sxs-lookup"><span data-stu-id="0bef1-306">Sign in to the warehouse app as a user in warehouse *61*.</span></span> <span data-ttu-id="0bef1-307">(Sláið inn *61* sem notandakennið og *1* sem aðgangsorðið.)</span><span class="sxs-lookup"><span data-stu-id="0bef1-307">(Enter *61* as the user ID and *1* as the password.)</span></span>
1. <span data-ttu-id="0bef1-308">Opnaðu **Á útleið \> Sölutiltekt**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-308">Go to **Outbound \> Sales Picking**.</span></span>
1. <span data-ttu-id="0bef1-309">Færið inn fyrsta vinnukennið fyrir sölupöntun 1.</span><span class="sxs-lookup"><span data-stu-id="0bef1-309">Enter the first work ID for sales order 1.</span></span>

    <span data-ttu-id="0bef1-310">Notið vinnukennin fyrir sölupantanir sem skráð voru niður hér á undan, á síðunni **Upplýsingar um vinnu**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-310">Refer to the work IDs for sales orders that you made a note of earlier, on the **Work details** page.</span></span> <span data-ttu-id="0bef1-311">Vinnukennið sem fært er inn hér býr til tiltektarvinnu fyrir magn upp á 10 ea frá tveimur aðskildum staðsetningum.</span><span class="sxs-lookup"><span data-stu-id="0bef1-311">The work ID that you enter here will generate pick work for a quantity of 10 ea from two separate locations.</span></span>

1. <span data-ttu-id="0bef1-312">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-312">Select **OK**.</span></span>

    <span data-ttu-id="0bef1-313">Verksíðan **Sölupantanir: Tiltekt** sýnir vörunúmerið, magnið og staðsetninguna sem tína á úr fyrir fyrstu staðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="0bef1-313">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the first location.</span></span>

1. <span data-ttu-id="0bef1-314">Í reitinn **NP** skal færa númeraplötunúmerið fyrir vöruna í staðsetningunni sem er sýnd.</span><span class="sxs-lookup"><span data-stu-id="0bef1-314">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="0bef1-315">Velja skal hnappinn **Í lagi** (gátmerkistákn).</span><span class="sxs-lookup"><span data-stu-id="0bef1-315">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="0bef1-316">Verksíðan **Sölupantanir: Tiltekt** sýnir vörunúmerið, magnið og staðsetninguna sem tína á úr fyrir næstu staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-316">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from for the next location.</span></span>

1. <span data-ttu-id="0bef1-317">Í reitinn **NP** skal færa númeraplötunúmerið fyrir vöruna í staðsetningunni sem er sýnd.</span><span class="sxs-lookup"><span data-stu-id="0bef1-317">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="0bef1-318">Velja skal hnappinn **Í lagi** (gátmerkistákn).</span><span class="sxs-lookup"><span data-stu-id="0bef1-318">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="0bef1-319">Síðan **Sölupantanir: Frágangur** gefur fyrirskipun um að ganga frá báðum loknu tiltektarvinnunum á geymslustaðsetningu á útleið.</span><span class="sxs-lookup"><span data-stu-id="0bef1-319">The **Sales orders: Put** page instructs you to put away both the completed picking works to the outbound staging location.</span></span>

1. <span data-ttu-id="0bef1-320">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-320">Select **OK**.</span></span>

    <span data-ttu-id="0bef1-321">Skilaboðin „Vinnu er lokið“ birtast.</span><span class="sxs-lookup"><span data-stu-id="0bef1-321">You receive a "Work Completed" message.</span></span>

1. <span data-ttu-id="0bef1-322">Færið inn næsta vinnukenni fyrir sölupöntun 1.</span><span class="sxs-lookup"><span data-stu-id="0bef1-322">Enter the second work ID for sales order 1.</span></span>

    <span data-ttu-id="0bef1-323">Aðeins er eitt tiltektarverk fyrir þetta vinnukenni.</span><span class="sxs-lookup"><span data-stu-id="0bef1-323">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="0bef1-324">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-324">Select **OK**.</span></span>

    <span data-ttu-id="0bef1-325">Verksíðan **Sölupantanir: Tiltekt** sýnir vörunúmerið, magnið og staðsetninguna sem tína á úr.</span><span class="sxs-lookup"><span data-stu-id="0bef1-325">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="0bef1-326">Í reitinn **NP** skal færa númeraplötunúmerið fyrir vöruna í staðsetningunni sem er sýnd.</span><span class="sxs-lookup"><span data-stu-id="0bef1-326">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="0bef1-327">Númeraplatan sem tilgreind er verður ein af númeraplötunum sem kerfið býr til í verkum áfyllingarvinnu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-327">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="0bef1-328">Til að ganga úr skugga um að rétt kenni númeraplötu sé sótt, skal athuga birgðirnar á síðunni **Lagerlisti** fyrir vöruna, staðsetninguna og magnið.</span><span class="sxs-lookup"><span data-stu-id="0bef1-328">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="0bef1-329">Velja skal hnappinn **Í lagi** (gátmerkistákn).</span><span class="sxs-lookup"><span data-stu-id="0bef1-329">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="0bef1-330">Staðfestið leiðbeiningar um frágangsverk á geymslustaðsetningu á útleið.</span><span class="sxs-lookup"><span data-stu-id="0bef1-330">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="0bef1-331">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-331">Select **OK**.</span></span>

    <span data-ttu-id="0bef1-332">Skilaboðin „Vinnu er lokið“ birtast.</span><span class="sxs-lookup"><span data-stu-id="0bef1-332">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="0bef1-333">Lokað er fyrir tiltekt fyrir sölupöntun 2 vegna þess að áfyllingarverkið sem hún er tengd við er ekki lokið.</span><span class="sxs-lookup"><span data-stu-id="0bef1-333">Sales order 2 is blocked from picking because the replenishment task that it's linked to isn't completed.</span></span> <span data-ttu-id="0bef1-334">Sem stendur er enn magn upp á 30 ea í tiltektarstaðsetningunni og áfyllingarmagnið fyrir sölupöntun 2 er 60 ea.</span><span class="sxs-lookup"><span data-stu-id="0bef1-334">Currently, there is still a quantity of 30 ea in the picking location, and the replenishment quantity for sales order 2 is 60 ea.</span></span> <span data-ttu-id="0bef1-335">Samtala lagerbirgða og áfyllingarbirgða (90 ea) fer yfir magn yfirflæðis upp á 0,65 PL (eða 65 ea).</span><span class="sxs-lookup"><span data-stu-id="0bef1-335">The sum of the on-hand inventory and the replenishment inventory (90 ea) exceeds the overflow quantity of 0.65 PL (or 65 ea).</span></span> <span data-ttu-id="0bef1-336">Áður en hægt er að ljúka við áfyllingarvinnu verður að tína sölupöntun 3.</span><span class="sxs-lookup"><span data-stu-id="0bef1-336">Before the replenishment work can be completed, sales order 3 must be picked.</span></span>

1. <span data-ttu-id="0bef1-337">Færið inn vinnukennið fyrir sölupöntun 3.</span><span class="sxs-lookup"><span data-stu-id="0bef1-337">Enter the work ID for sales order 3.</span></span>

    <span data-ttu-id="0bef1-338">Aðeins er eitt tiltektarverk fyrir þetta vinnukenni.</span><span class="sxs-lookup"><span data-stu-id="0bef1-338">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="0bef1-339">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-339">Select **OK**.</span></span>

    <span data-ttu-id="0bef1-340">Verksíðan **Sölupantanir: Tiltekt** sýnir vörunúmerið, magnið og staðsetninguna sem tína á úr.</span><span class="sxs-lookup"><span data-stu-id="0bef1-340">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="0bef1-341">Í reitinn **NP** skal færa númeraplötunúmerið fyrir vöruna í staðsetningunni sem er sýnd.</span><span class="sxs-lookup"><span data-stu-id="0bef1-341">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="0bef1-342">Númeraplatan sem tilgreind er verður ein af númeraplötunum sem kerfið býr til í verkum áfyllingarvinnu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-342">The license plate that you specify will be one of the system-generated license plates from the replenishment work tasks.</span></span> <span data-ttu-id="0bef1-343">Til að ganga úr skugga um að rétt kenni númeraplötu sé sótt, skal athuga birgðirnar á síðunni **Lagerlisti** fyrir vöruna, staðsetninguna og magnið.</span><span class="sxs-lookup"><span data-stu-id="0bef1-343">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="0bef1-344">Velja skal hnappinn **Í lagi** (gátmerkistákn).</span><span class="sxs-lookup"><span data-stu-id="0bef1-344">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="0bef1-345">Staðfestið leiðbeiningar um frágangsverk á geymslustaðsetningu á útleið.</span><span class="sxs-lookup"><span data-stu-id="0bef1-345">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="0bef1-346">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-346">Select **OK**.</span></span>

    <span data-ttu-id="0bef1-347">Skilaboðin „Vinnu er lokið“ birtast.</span><span class="sxs-lookup"><span data-stu-id="0bef1-347">You receive a "Work Completed" message.</span></span>

<span data-ttu-id="0bef1-348">Um leið og samtala lagerbirgða í tiltektarstaðsetningunni og áfyllingarmagns er undir mörkum, verður hægt að vinna úr eftirstandandi áfyllingarvinnu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-348">As soon as the sum of the on-hand quantity in the picking location and the replenishment quantity is below the threshold, you will be able to process the remaining replenishment work.</span></span>

<span data-ttu-id="0bef1-349">Farið aftur á síðuna **Upplýsingar um vinnu** og takið eftir að tiltækileiki áfyllingarvinnu fyrir síðasta hluta áfyllingar (fyrir sölupöntun 2) er *Opin*, því að nóg pláss er í staðsetningunni til að samþykkja áfyllinguna.</span><span class="sxs-lookup"><span data-stu-id="0bef1-349">Return to the **Work details** page, and notice that the replenishment work availability for the final piece of replenishment (for sales order 2) is *Open*, because there is now enough space in the location to accept the replenishment.</span></span>

<span data-ttu-id="0bef1-350">Nú er hægt að vinna þessa áfyllingarvinnu með fartækinu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-350">You can now process this replenishment work via the mobile device.</span></span>

1. <span data-ttu-id="0bef1-351">Farið í **Birgðir \> Áfylling**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-351">Go to **Inventory \> Replenishment**.</span></span>

    <span data-ttu-id="0bef1-352">Beðið er um að ljúka eftirstandandi áfyllingarvinnu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-352">You're prompted to complete the remaining replenishment work.</span></span> <span data-ttu-id="0bef1-353">Vörunúmerið, magnið og staðsetningin fyrir tiltektina er sýnt.</span><span class="sxs-lookup"><span data-stu-id="0bef1-353">The item number, quantity, and location to pick from are shown.</span></span>

1. <span data-ttu-id="0bef1-354">Í reitinn **NP** skal færa númeraplötunúmerið fyrir vöruna í staðsetningunni sem er sýnd.</span><span class="sxs-lookup"><span data-stu-id="0bef1-354">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>
1. <span data-ttu-id="0bef1-355">Velja skal hnappinn **Í lagi** (gátmerkistákn).</span><span class="sxs-lookup"><span data-stu-id="0bef1-355">Select the **OK** button (check mark symbol).</span></span>

    <span data-ttu-id="0bef1-356">Kerfið býr til númer marknúmeraplötu fyrir nýju númeraplötuna fyrir tínda vöru.</span><span class="sxs-lookup"><span data-stu-id="0bef1-356">The system generates a target license plate number for the new license plate for the picked item.</span></span>

1. <span data-ttu-id="0bef1-357">Veljið **Í lagi** til að staðfesta gildið.</span><span class="sxs-lookup"><span data-stu-id="0bef1-357">Select **OK** to confirm the value.</span></span>

    <span data-ttu-id="0bef1-358">Frágangsvinna er sýnd sem segir notandanum að setja marknúmeraplötuna á áfyllingarstaðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="0bef1-358">Put work is shown that instructs the user to put the target license plate into the replenishment location.</span></span> <span data-ttu-id="0bef1-359">Staðsetning *Frágangs* á að vera **06A01R2S1B**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-359">The *Put* location should be **06A01R2S1B**.</span></span>

1. <span data-ttu-id="0bef1-360">Staðfestið upplýsingar um frágang og veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-360">Confirm the put details, and select **OK**.</span></span>

    <span data-ttu-id="0bef1-361">Skilaboðin „Vinnu lokið“ og „Engin vinna tiltæk“ birtast.</span><span class="sxs-lookup"><span data-stu-id="0bef1-361">You receive "Work Completed" and "No Work Available" messages.</span></span>

<span data-ttu-id="0bef1-362">Þú getur nú valið sölupöntun 2.</span><span class="sxs-lookup"><span data-stu-id="0bef1-362">You can now pick sales order 2.</span></span> <span data-ttu-id="0bef1-363">Opnað var fyrir hana þegar áfyllingarvinnunni sem tengd er við sölupöntunina var lokið.</span><span class="sxs-lookup"><span data-stu-id="0bef1-363">It became unblocked when the replenishment work that is linked to the sales order was completed.</span></span>

1. <span data-ttu-id="0bef1-364">Færið inn vinnukennið fyrir sölupöntun 2.</span><span class="sxs-lookup"><span data-stu-id="0bef1-364">Enter the work ID for sales order 2.</span></span>

    <span data-ttu-id="0bef1-365">Aðeins er eitt tiltektarverk fyrir þetta vinnukenni.</span><span class="sxs-lookup"><span data-stu-id="0bef1-365">There is only one pick task for this work ID.</span></span>

1. <span data-ttu-id="0bef1-366">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-366">Select **OK**.</span></span>

    <span data-ttu-id="0bef1-367">Verksíðan **Sölupantanir: Tiltekt** sýnir vörunúmerið, magnið og staðsetninguna sem tína á úr.</span><span class="sxs-lookup"><span data-stu-id="0bef1-367">The **Sales orders: Pick** task page shows the item number, quantity, and location to pick from.</span></span>

1. <span data-ttu-id="0bef1-368">Í reitinn **NP** skal færa númeraplötunúmerið fyrir vöruna í staðsetningunni sem er sýnd.</span><span class="sxs-lookup"><span data-stu-id="0bef1-368">In the **LP** field, enter the license plate number for the item in the location that is shown.</span></span>

    <span data-ttu-id="0bef1-369">Númeraplatan sem tilgreind er verður númeraplatan sem kerfið býr til í verki áfyllingarvinnu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-369">The license plate that you specify will be the system-generated license plate from the replenishment work task.</span></span> <span data-ttu-id="0bef1-370">Til að ganga úr skugga um að rétt kenni númeraplötu sé sótt, skal athuga birgðirnar á síðunni **Lagerlisti** fyrir vöruna, staðsetninguna og magnið.</span><span class="sxs-lookup"><span data-stu-id="0bef1-370">To make sure that you capture the correct license plate ID, check the inventory on the **On-hand list** page for the item, location, and quantity.</span></span>

1. <span data-ttu-id="0bef1-371">Velja skal hnappinn **Í lagi** (gátmerkistákn).</span><span class="sxs-lookup"><span data-stu-id="0bef1-371">Select the **OK** button (check mark symbol).</span></span>
1. <span data-ttu-id="0bef1-372">Staðfestið leiðbeiningar um frágangsverk á geymslustaðsetningu á útleið.</span><span class="sxs-lookup"><span data-stu-id="0bef1-372">Confirm the instructions for the put task to the outbound staging location.</span></span>
1. <span data-ttu-id="0bef1-373">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="0bef1-373">Select **OK**.</span></span>

    <span data-ttu-id="0bef1-374">Skilaboðin „Vinnu er lokið“ birtast.</span><span class="sxs-lookup"><span data-stu-id="0bef1-374">You receive a "Work Completed" message.</span></span>

## <a name="notes-and-tips"></a><span data-ttu-id="0bef1-375">Athugasemdir og ábendingar</span><span class="sxs-lookup"><span data-stu-id="0bef1-375">Notes and tips</span></span>

- <span data-ttu-id="0bef1-376">Þessi aðgerði virkar með öllum gerðum áfyllingar: bylgjueftirspurn, lágmarki/hámarki, hleðslueftirspurn og hólfaskiptingu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-376">This functionality works with all types of replenishment: wave demand, min/max, load demand, and slotting.</span></span>
- <span data-ttu-id="0bef1-377">Hægt er að hnekkja tiltækileika áfyllingarvinnu handvirkt fyrir hvern vinnuhaus af síðunni **Upplýsingar um vinnu** ef þess er óskað.</span><span class="sxs-lookup"><span data-stu-id="0bef1-377">You can manually override the replenishment work availability for each work header from the **Work details** page if you want.</span></span>
- <span data-ttu-id="0bef1-378">Þegar kerfið stillir tiltækileika áfyllingarvinnu, tekur það allar birgðir til greina sem eru þegar í staðsetningunni áður en vinnu er lokið</span><span class="sxs-lookup"><span data-stu-id="0bef1-378">When the system sets the replenishment work availability, it considers any inventory that is already in the location before any work is completed</span></span>
- <span data-ttu-id="0bef1-379">Hver hluti sölupöntunarvinnu er tengdur við tiltekna áfyllingarvinnu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-379">Each piece of sales order work is linked to a specific replenishment work.</span></span> <span data-ttu-id="0bef1-380">Ekki er til nein samsvarandi virkni fyrir tiltækileika söluvinnu.</span><span class="sxs-lookup"><span data-stu-id="0bef1-380">There is no corresponding sales work availability functionality.</span></span>
